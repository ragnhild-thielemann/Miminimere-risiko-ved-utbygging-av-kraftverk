###

Vi ønsker å minimere avviket mellom produsert strøm og etterspurt strøm, altså minimere parameteren $D$

$$
D = \frac{1}{n} \sum_{i=1}^{n} (R_i - e_i)^2
$$ 


Den eneste størrelsen vi kan variere, er vektoren **w**, som representerer hvor stor andel kapasitet som bygges i hver vindpark. Optimaliseringen består derfor i å finne vektoren **w** som minimerer variansen $D$, under bibetingelsene om ønsket produksjonsnivå ( R = $w^{T}$ r ) , samt myndighetens og næringslivets vilje til invisteringsvilje i fornybar strøm ( $w^{T}$ = $\kappa$ ).

### Lagrange - oppsett

- **Minimeringsproblem** 

$$ D(w) = \frac{1}{n} \sum_{i=1}^{n} (R_i - e_i)^2 $$

- **Første bibetingelse**


$$ h(w) =  w^{T} r = R $$

- **Andre bibetingelse**

$$ k(w) = w^{T} = \kappa $$

### Utregning 

Man kan vise at 



$$
D = \frac{1}{n} \sum_{i=1}^{n} (R_i - e_i)^2 = w^{T} C w + (w^{T} r - \mu_{e})^2 + Var(E)
$$ 




som er et enklere utrykk å minimere. Fra utledningen av [kovariansen](https://github.com/ragnhild-thielemann/Miminimere-risiko-ved-utbygging-av-kraftverk/tree/main/Kovarians) til strømproduksjonen ved ulike vindkraftverk $r_{d}$ , så vi at den totale variansen $Var(R)$ var gitt ved 



$$ Var(R) = w^{T} C w $$ 


Dette gir 

$$ D = 
### Dette kan ansees som en lagrangeproblem med der vi ønsker å minimere 

 - E = energibehovet vi ønsker å dekke ved et gitt tidspunkt $t$. 



For å finne den allokeringen av vindparker **w** som gir minst murlig avvik mellom etterspørselen etter strøm strøm-produksjonen trenger vi først noen et utrykk for kovariansen mellom ulike produksjoner. 




, bruker vi lemmaet 


 $$
D = \frac{1}{n} \sum_{i=1}^{n} (R_i - e_i)^2 = w^{T} C w + (w^{T} r - \mu_{e})^2 + Var(E)
$$ 
