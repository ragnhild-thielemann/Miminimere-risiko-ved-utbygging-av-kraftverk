

# Indroduksjon


![Lagrange_problem](https://github.com/ragnhild-thielemann/Miminimere-risiko-ved-utbygging-av-kraftverk/blob/main/images/vindmøller.png)


Verden står overfor en nødvendig klimaomstilling som krever store investeringer i fornybare energikilder. I motsetning til tradisjonelle kraftverk basert på kull eller olje, er det vanskelig å kontrollere strømproduksjonen fra fornybare kilder. For eksempel produserer vindkraftverk mer strøm når det blåser, og mindre når vinden stilner. Dette skaper utfordringer for å opprettholde en stabil energiforsyning til både husholdninger og bedrifter, siden strøm er en ferskvare med begrensede muligheter for lagring.

Værforhold som vind og skydekke varierer geografisk, og produksjonen kan derfor svinge fra sted til sted. Langs kysten blåser det ofte mer enn innlandet, og forholdene i Nord-Norge kan være svært ulike fra Sør-Norge.

For å møte disse utfordringene kan vi anvende Markowitz’ porteføljeteori på energiinvesteringer. Målet er å finne en optimal kombinasjon av fornybare kraftverk som høy strømproduksjon og variasjon, slik at vi sikrer høyest mulig, stabil strømproduksjon over tid.

## Forventet strømproduksjon

Vi antar at vi investerer i vindparker på ulike lokasjoner $d$ . 


 - **w** = ($w_{\text{1}}$ , $w_{\text{2}}$ ... $w_{\text{d}}$ ) $^{T}$ Vektorens komponenteter $w_{\text{d}}$ viser hvor stor andel av investeringene man har gjort i hver vindpark $d$.

 - **r** = ( $r_{\text{1}}$ , $r_{\text{2}}$ ... $r_{\text{d}}$ ) $^{T}$ er en vektor, der hver indeks  $r_{\text{d}}$ represetnerer for $kapasitetsfaktoren$ for vindparken i lokasjon  $d$ . 
 
  
  
  Dette gjør at total strømproduksjon fra alle vindparkene er gitt ved skalarproduktet mellom investeringene i hver enkelt vindpark og kapasitetesfaktoren til vindparken, som gir oss: 

  $$ R = w^{T} r = \sum_{i=1}^{d} w_{i} r_{i} $$


  Vi antar at myndighetene har et krav om at en viss menge kapasitet med fornybar energi skal instaleres, og vi betegner dette som et konstant $\kappa$. Dermed blir summen av investeringene 

  $$  w^{T} 1 = \sum_{i=1}^{d} w_{i} = \kappa $$
  
I motsetning til Markowitz’ porteføljeteori, krever vi at $w_{\text{d}}$ > 0, da det ikke gir mening å ha en negativ vindmølle (negative verdier for  $w_{\text{d}}$ gir i portefølgeinveseringer mening dersom man shorter aksjene). 


  
 
### Beste allokering av vindparker for å minimere sløsing og risiko for å kutte strømnettet

Da strøm har svært begrensede murligheter for oppbevaring, ønsker vi allokeringen som gir minst murlig varians i strømproduksjonen, samtidig som vi møter etterspørselen $E$ etter kraft. 

#### Parametere

 - $E$ er befolkningenes etterspørsel etter kraft ved tidspunktet $t$. Vi anser variabelen som usikker, da etterspørselen etter strøm varierer med tiden på døgnet, temperaturen ute og vedprisene. 
 - $\mu_{\text{e}}$ er  forventet etterspørsel etter strøm, basert på historiske data. 
 - $\sigma_{\text{e}}^2$ er variansen i etterspøselen, basert på historiske data. 
 - **w** er vektoren som utrykker inversteringene i hvert kraftverk $d$ .
 - R = $w^{T}$ r er total strømproduksjon. 

Vi betegner differansen $D$ i tidspunktet $i$ som 

$$D = R_{\text{i}} - e_{\text{i}} $$


altså differansen mellom produsert kraft og etterspurt kraft ved tidspunktet $i$ = 1,2,3,4 ...n . Denne størrelsen uttrykker ubalansen i kraftmarkedet til enhver tid. Dersom $D_{i}$ > 0, vil det produseres med strøm enn det markedet etterspør, og strømmen må "kastes på havet", da det er begrenset med langringsmurligheter for strøm. 

Dersom $D_{i}$ < 0 oppstår det derimot et kraftunderskudd. Når tilbudet ikke dekker etterspørselen, presses prisene oppover, noe vi så tydelig under energikrisen vinteren 2021–2022. Russlands invasjon av Ukraina resulterte i at Europa sanksjonerte russiske gassleveranser, samtidig som det var lite vind. Når både gassforsyningen sviktet og vindkraftproduksjonen var svak, oppstod det et betydelig negativt $D_{i}$ , noe som førte til kraftig økning i strømprisene.


![Lagrange_problem](https://github.com/ragnhild-thielemann/Miminimere-risiko-ved-utbygging-av-kraftverk/blob/main/images/EU.png)


Mimimeringsproblemet vi øsner å løse er at det totale avviket mellom $R_{\text{i}}$ og $e_{\text{i}}$ , altså at total strømproduksjon er likest murlig etterspørselen ved etthvert tidspunkt $i$ . Da R = $w^{T}$ r , vil vi finne den allokeringen av inveseringer i vindparker, slik at utrykket

$$
D = \frac{1}{n} \sum_{i=1}^{n} (R_i - e_i)^2
$$ 

blir minst murlig. Dette er et minimeringsproblem under bibetingelser, som vi løser i mappen 
[Lagrange_problem](https://github.com/ragnhild-thielemann/Miminimere-risiko-ved-utbygging-av-kraftverk/tree/main/Lagrange_problem) . 
Målet er å minimere den totale risikoen i kraftproduksjonen, gitt et krav til forventet strømproduksjon. Risikoen modelleres ved hjelp av en kovariansmatrise, som beskriver hvordan produksjonen fra ulike vindparker samvarierer.

Den eneste størrelsen vi kan variere, er vektoren **w**, som representerer hvor stor andel kapasitet som bygges i hver vindpark. Optimaliseringen består derfor i å finne den vekten w som minimerer variansen ($w^{T}$ $\Sigma$ w), under bibetingelsen om ønsket produksjonsnivå ( R = $w^{T}$ r ) , samt myndighetens og næringslivets vilje til investeringer ( $w^{T}$ = $\kappa$ ) . 





