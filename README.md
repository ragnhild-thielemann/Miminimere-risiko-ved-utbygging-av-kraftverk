

# Indroduksjon

Verden står overfor en nødvendig klimaomstilling som krever store investeringer i fornybare energikilder. I motsetning til tradisjonelle kraftverk basert på kull eller olje, er det vanskelig å kontrollere strømproduksjonen fra fornybare kilder. For eksempel produserer vindkraftverk mer strøm når det blåser, og mindre når vinden stilner. Dette skaper utfordringer for å opprettholde en stabil energiforsyning til både husholdninger og bedrifter, siden strøm er en ferskvare med begrensede muligheter for lagring.

Værforhold som vind og skydekke varierer geografisk, og produksjonen kan derfor svinge fra sted til sted. Langs kysten blåser det ofte mer enn innlandet, og forholdene i Nord-Norge kan være svært ulike fra Sør-Norge.

For å møte disse utfordringene kan vi anvende Markowitz’ porteføljeteori på energiinvesteringer. Målet er å finne en optimal kombinasjon av fornybare kraftverk som høy strømproduksjon og variasjon, slik at vi sikrer høyest mulig, stabil strømproduksjon over tid.

### Konstanter vi kjenner

 - $\mu_{\text{e}}$ = Forventet verdi for energibehovet vi ønsker å dekke. Dette er et estimat basert på historiske data, og er en estimert konstant. 

 - **r** = ( $r_{\text{1}}$ , $r_{\text{2}}$ ... $r_{\text{d}}$ ) $^{T}$ er en vektor, der hver indeks  $r_{\text{d}}$ represetnerer for $kapasitetsfaktoren$ for vindparken i lokasjon  $d$ . 
 
  - **w** = ($w_{\text{1}}$ , $w_{\text{2}}$ ... $w_{\text{d}}$ ) $^{T}$ . $w_{\text{d}}$ er hvor stor andel av investeringene man har gjort i hver vindpark $d$. 
  
  Dette gjør at produksjonen av strøm fra alle vindparkene er gitt ved 

  $$ R = w^{T} r = \frac{1}{T}\sum_{t=1}^{T} w_{d} r_{d} $$
  
  Vi antar at myndighetene har et krav om at en viss menge kapasitet med fornybar energi skal instaleres, og vi betegner dette som et konstant tall $\kappa$ . 
  
   slik at $w^{T}$ 1 = $\sum{i=1}^{d}$ = $\kappa$ . I motsetning til Markowitz’ porteføljeteori, krever vi at $w_{\text{d}}$ > 0, da det ikke gir mening å ha en negativ vindmølle (negative verdier for  $w_{\text{d}}$ gir i portefølgeinveseringer mening dersom man shorter aksjene. 
  
 



### Dette kan ansees som en lagrangeproblem med der vi ønsker å minimere 

 - E = energibehovet vi ønsker å dekke ved et gitt tidspunkt $t$. 