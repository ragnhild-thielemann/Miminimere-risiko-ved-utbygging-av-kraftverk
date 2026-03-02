

# Indroduksjon

Verden står overfor en nødvendig klimaomstilling som krever store investeringer i fornybare energikilder. I motsetning til tradisjonelle kraftverk basert på kull eller olje, er det vanskelig å kontrollere strømproduksjonen fra fornybare kilder. For eksempel produserer vindkraftverk mer strøm når det blåser, og mindre når vinden stilner. Dette skaper utfordringer for å opprettholde en stabil energiforsyning til både husholdninger og bedrifter, siden strøm er en ferskvare med begrensede muligheter for lagring.

Værforhold som vind og skydekke varierer geografisk, og produksjonen kan derfor svinge fra sted til sted. Langs kysten blåser det ofte mer enn innlandet, og forholdene i Nord-Norge kan være svært ulike fra Sør-Norge.

For å møte disse utfordringene kan vi anvende Markowitz’ porteføljeteori på energiinvesteringer. Målet er å finne en optimal kombinasjon av fornybare kraftverk som høy strømproduksjon og variasjon, slik at vi sikrer høyest mulig, stabil strømproduksjon over tid.

### Konstanter vi kjenner

 - $\mu_{\text{e}}$ = Forventet verdi for energibehovet vi ønsker å dekke. Dette er et estimat basert på historiske data, og er en konstant vi kjenner. 

 - **r** = vektor for $kapasitetsfaktoren$ for vindkraft i $d$ forskjellige geografiske lokasjoner. Hver indeks vil være $r_{\text{d}}$ vil være hvor mye av  kapasiteten hver vindlokasjon klarer å utnytte. 
 
  - **w** = vektor, der hver komponent er hvor stor andel av total inversting i vindkraftverkene vi har i hver vinpark. Vi antar at inversteingsviljen er et konstant tall $\kappa$, slik at $**w**^{T}$ $\cdot$ 1 = $\sum{i=1}^{d}$ = $\kappa$

  - vi ønsker å minimere  



### Dette kan ansees som en lagrangeproblem med der vi ønsker å minimere 

 - E = energibehovet vi ønsker å dekke ved et gitt tidspunkt $t$. 