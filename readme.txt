SCSS

Za koriscenje boja (primarna, sekundarna, tercijarna), neophodno izmjeniti file scss/abstracts/_variables.scss tako da prilagodite boje projektu.

Kompajliranje scss fajlova nakon izmjene boja:

1. Instalirati scripte tako sto cete otvoriti terminal/cmd u ovom folderu pokrenuti "npm install"

2. Nakon sto je instalacija neophodnih package-a zavrsena, u terminalu/cmd pokrenuti scriptu "npm run build"

(neophodno je imati node.js i node package manager(npm). Dovoljno je sa zvanicnog sajta instalirati node.js, npm je included u default instalaciji)
______________________________________________________

ABSTRACTS
---------

_mixins.scss

1. Mixins za media queries

usage: "@include sm" - media query max-width 576px
usage custom: "@include rwd(*zeljena width*)" 

................................................

_variables.scss

1. 3 boje: primarna, sekundarna, tercijarna kao i njihove 2 varijante, tamnija i svjetlija. Korisno za hover efekat.

2. Util boje: korisno za light grey pozadine, bordere itd

........................................................

COMPONENTS
----------

U components folder idu custom scss component fajlovi

______________________________________________________

UTILS
-----

_fonts.scss

velicina fonta - format imena klase f-s-px (font-size-pixel) - 10-20, 22-30(22,24,26,28,30) - 35-50 (35,40,45,50)

*velicina fonta je relativna, kada je screen width ispod 576px font se automatski smanjuje

font-weight - format imena klase f-w-debljina - od 300 do 900

boje:

.text-color-primary - primarna boja sajta
.text-color-secondary - sekundarna boja sajta
.text-color-tertiary - tercijarna boja sajta

.text-color-font - #434343

.text-color-lg - light grey
.text-color-mg - mediumg grey

.text-color-black
.text-color-white
............................................................................................

_grid.scss

Bootstrap klase - izmjenjen container da ima max-width 1340px umjesto 1140px

...................................................................

_normalize.scss

Resetovanje svih defaultnih margina i paddinga u radi sto blizeg prikazivanja stranice u razlicitim browserima.

.................................................................

_utils.scss

1. ::-moz-selection - pozadina i boja fonta prilikom selekcije texta na stranici. primarna boja iz mixins fajla.

2. postavljanje fonta citavog html dokumenta na 62.5% radi omogucavanja prakticnog koriscenja relativnih unita (rem). Na 576px se smanjuje na 50%, radi lakse responsive optimizacije

3. no-scroll klasa za body - koristiti npr kad je modal aktivan

4. clearfix klasa

5. text-align klase (left,center,right)

.......

Pozicija Elemenata:

.p-r - position:relative;

.p-a - position: absolute;

.p-f - position: fixed;

.top-0 - top:0;
.top-50 - top:50%;

.right-0 - right:0;
.right-50 - right:50%;

.bottom-0 - bottom:0;
.bottom-50 - bottom:50%;

.left-0 - left:0;
.left-50 - left:50%;

Centriranje Elemenata:

Horizontalno:

.center-margin - margin: 0 auto;

.center-r-h - relativno centriranje *left:50%; transform: translateX(-50%);

.center-a-h - absolute centriranje *left:50%; transform: translateX(-50%); - koristiti sa "top" klasama

.center-f-h - fixed centriranje *left:50%; transform: translateX(-50%); - koristiti sa "top" klasama


Vertikalno:

.center-r-v - relativno centriranje *top:50%; transform: translateY(-50%);

.center-a-v - absolute centriranje *top:50%; transform: translateY(-50%); - koristiti sa "left" ili "right" klasama

.center-f-v - fixed centriranje *top:50%; transform: translateY(-50%); - koristiti sa "left" ili "right" klasama


centriranje:

.center-r-b - relativno centriranje *top:50%;left50%; transform: translate(-50%,-50%);

.center-a-b - absolute centriranje *top:50%;left50%; transform: translate(-50%,-50%);

.center-f-b - fixed centriranje *top:50%;left50%; transform: translate(-50%,-50%);

Margins:

.mt - margin-top
.mr - margin-right
.mb - margin-bottom
.ml - margin-left

format klase: .mt-br pixela (.mt-5) *relative units koristeni

Padding:

.pt - padding-top
.pr - padding-right
.pb - padding-bottom
.pl - padding-left
.pa - padding all
.ptb - padding-top, padding-bottom
.prl - padding-left, padding-right

format klase: .pt-br pixela (.pt-5) *relative units koristeni

*relative units koristeni

...................................

BORDER RADIUS

.br-r- od 1 do 20 -- (br-r-20) - border-radius:20px;

.....................................

BUTTON

.btn - outline:none, text-decoration:none

.btn-primary - padding:.5rem 2rem background-color: primary color - default hover 10% tamnija boja
.btn-secondary - padding:.5rem 2rem background-color: secondary color - default hover 10% tamnija boja
.btn-tertiary - padding:.5rem 2rem background-color: tertiary color - default hover 10% tamnija boja

........................................

TRANSITIONS

.transition- od 1 do 10 - 1=0.1s, 10=1s

.......................................

BACKGROUND

.bg-primary - background-color: primarna
.bg-secondary - background-color: primarna
.bg-tertiary - background-color: primarna

.bg-lg-1 - background-color: #eee
.bg-lg-2 - background-color: #ccc
.bg-lg-3 - background-color: #999
