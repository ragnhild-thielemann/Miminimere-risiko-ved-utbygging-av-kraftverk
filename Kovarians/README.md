
 ## Kovariansmatrisen
 For å finne den allokeringen av vindparker **w** som gir minst mulig avvik mellom etterspørsel og strømproduksjon (minimere parameteren $D$) , må vi først beskrive hvordan produksjonen ved ulike vindparker samvarierer. Dette gjør vi ved å konstruere en kovariansmatrise for produksjonen.

 La $r_{i}$ være strømproduksjonen ved vindpark $i$ . Kovaransen mellom vindpark $i$ og $j$ er gitt ved : 

 $$
\text{Cov}(r_i, r_j) = \mathbb{E}[(r_i - \mu_i)(r_j - \mu_j)]
$$

Dette gir en kovariansmatrise $C$ lik


$$
\Sigma =
\begin{pmatrix}
\text{Var}(r_1) & \text{Cov}(r_1,r_2) & \dots & \text{Cov}(r_1,r_d) \\
\text{Cov}(r_2,r_1) & \text{Var}(r_2) & \dots & \text{Cov}(r_2,r_d) \\
\vdots & \vdots & \ddots & \vdots \\
\text{Cov}(r_d,r_1) & \text{Cov}(r_d,r_2) & \dots & \text{Var}(r_d)
\end{pmatrix}
$$

Her ligger variansene langs diagonalen, da vi har:


$$
\text{Var}(r_i) = \text{Cov}(r_i,r_i)
$$

mens elementene utenfor diagonalen er kovarianser mellom ulike vindparker.

### Viktig poeng om diversifisering

Dersom produksjonen ved alle vindparkene hadde variert helt likt – for eksempel dersom vinden økte og falt samtidig overalt – ville kovariansene vært like store som variansene. I så fall ville vi ikke fått noen risikoreduserende effekt av å spre investeringene.

Imidlertid varierer vindforholdene geografisk (for eksempel mellom kyst og innland, eller mellom nord og sør), slik at  kovariansen mellom to parker typisk være lavere enn variansen til hver enkelt park:


$$ |\text{Var}(r_i)|< \text{Cov}(r_i,r_i)$$

Dersom produksjonen til og med hadde beveget seg motsatt vei noen ganger (for eksempel høy produksjon ett sted når det er lav produksjon et annet sted), kunne kovariansen blitt enda lavere, eventuelt negativ. Dette reduserer den samlede variansen i porteføljen og gir en mer stabil totalproduksjon.

Dette er selve kjernen i Markowitz-tankegangen anvendt på inversteringer i fornybar energi: 

#### Geografisk spredning reduserer samlet risiko fordi kovariansene er lavere enn variansene. 


### Variansen til den totale vindparken R

Når vi skal finne variansen til den totale vindkraftporteføljen, må vi ta hensyn til både hvor mye vi investerer i hver park og hvordan produksjonen samvarierer mellom parkene.

**w** er vektvektoren for investeringene, og C er kovariansmatrisen for produksjonen. Variansen til den totale produksjoeen er gitt ved 

$$
\mathrm{Var}(R_{tot})
=
\sum_{i=1}^{d} \sum_{j=1}^{d}
w_i w_j \, \mathrm{Cov}(r_i, r_j)
$$

som tilsvarer skalaproduktet

$$
\mathrm{Var}(R_{tot}) = \mathbf{w}^{\top} C \mathbf{w}
$$

Dette gir den totale variansen for alle vindparkene vi har invesert i, altså $Var(R)$ . 

