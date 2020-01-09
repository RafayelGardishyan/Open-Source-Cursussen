## Python voor gevorderde beginners


### Een Cursus voor DJOG

* Voor de wiki-versie van de cursus ga naar: [https://github.com/RafayelGardishyan/PvGB/wiki](https://github.com/RafayelGardishyan/PvGB/wiki)

**Waarschuwing: De wiki-versie is nog niet af**


## Inleiding

Hallo en welkom bij de cursus “Python voor gevorderde beginners”. Veel plezier! 

Je hebt de volgende dingen nodig:



*   Een Computer
*   Python 3.6+ geïnstalleerd op de computer
*   * Basiskennis van CMD/Terminal (Als cd, ls, rm, mk, mkdir enz.) 
*   Heel veel zin om iets nieuws te leren

    * Optioneel. Nodig als je je programma vanuit CMD/Terminal wil starten, bewerken en maken. Je gaat ook “pip” gebruiken (De package manager van Python) in CMD/Terminal.

*   Rafayel Gardishyan


## Basiskennis van Python


### Alles waar je mee moet beginnen


## Print, Input, Variables en Comments

Net zoals in andere programmeertalen heb je in Python de mogelijkheid om waarden op het scherm te printen. Dat doe je met de `print()` functie. Om de gebruiker informatie te laten invoeren kan je gebruik maken van de `input()` functie. Variabelen zijn nog simpeler. Je declareert ze zo: `naam = "waarde"`. Hier is bijvoorbeeld een programma waarin al deze begrippen worden gebruikt:


```python
print(input("Toets wat in: "))
var1 = input("Voer een woord in: ")
print(var1)
```


Ook in Python net als in andere programmeertalen heb je comments. Comments op een regel geef je aan met een `#` en comment op meerdere lijnen open/sluit je met `"""`

Voorbeeld:


```python
print("Dit wordt uitgevoerd")
# print("Dit wordt niet uitgevoerd")
"""
print("1")
print("2")
print("3 regels worden niet uitgevoerd")
"""
```



## Logica

In Python is logica heel simpel te programmeren. Je heb dan maar een paar woorden nodig. Het zijn `if`, `elif `en `else.` Je gebruikt het zo: (Belangrijk is om te weten dat alles wat in de is/elif/else statements zit een ident nodig heeft, dus een tab afstand van de if. En vergeet de dubbele punt niet.)


```python
if input() == "Hallo":
    print("Hoi") 
```


Wat dit programma doet is “Hoi” printen als de gebruiker Hallo intoetst.


## Type Converters

Alle variabelen hebben een type. Het kan een String(tekst), Integer(Rond getal) etc zijn. Maar als je verschillende operaties wil doen met variabelen van verschillende types kan het soms mis gaan. Bijvoorbeeld als je dit doet:


```python
print("5" + 5)
```


Krijg je deze foutmelding:


    Traceback (most recent call last): \
  File "python", line 1, in <module> \
TypeError: must be str, not int

Dat betekent dat je een integer probeert op te tellen bij een string. Dat kan natuurlijk nooit goed gaan en om dat te voorkomen heb je converters nodig. Hier zijn de simpelste.

`str()`: Converteert elke soort variabele naar een string

`int()`: Converteert een variabele waar de waarde van een getal bevat naar een integer

`naam_var.upper()`: Converteert een string naar HOOFDLETTERS

`naam_var.lower()`: Converteert een string naar kleine letters

**Optionneel:**

Je hebt ook:

`float()`: Converteert een variabele die getallen bevat naar een float (Kommagetal)

`bool()`: Converteert een variabele naar een boolean (True/False (Waar/Onwaar))

`tuple()`: Converteert een variabele naar een tuple (Een constante lijst)

`list()`: Converteert een variabele naar een array (Een lijst)

`bin()`: Converteert een getal naar een binair getal (Binair == `1001111 == 79`)

`oct()`: Converteert een getal naar een octaal getal (Octaal == `117 == 79`)

`hex()`: Converteert een getal naar een hexadecimaal getal (Hexadecimaal == `4F == 79`)

Dit zijn er al veel maar er zijn nog veel meer en je kunt ze zelf maken, wat we later ook zeker gaan doen.


```
Opdracht 1:
Deze kennis is genoeg om je eerste opdracht te voltooien:
Je opdracht is om een rekenmachine te maken. Het moet kunnen optellen, aftrekken, vermenigvuldigen en delen.
```



## Loops

Net zoals in vele andere programmeertalen heb je in Python 2 soorten loops. De While loop en de For loop. Ze zijn net zo makkelijk als de if/elif/else statements. 


### While loop

Hier is een voorbeeld met uitleg:


```python
x = 0
while x <= 10:
    print("X is gelijk aan " + str(x) + " en kleiner dan 11")
    x = x + 1
```


Wat dit programma doet is waarschijnlijk makkelijk te raden. Het print 10 keer “X is gelijk aan (waarde van x) en kleiner dan 11” en na elke herhaling maakt het x groter met 1.

Dit is het while loop. 


### For loop

Er is ook een for loop. Bij een for loop krijg je een variabele die elke herhaling veranderd. Hier is hetzelfde programma als hierboven maar dan met een for loop:


```python
for x in range(11):
    print("X is gelijk aan" + str(x) + " en kleiner dan 11")
```


Zo simpel is het. Als je later weet wat arrays en dictionaries zijn kan je veel meer met for loops, zoals elke element van een lijst uitprinten.


```
Tip 🙋:
Als je een oneindige loop wil maken kan je while True gebruiken.
```



## Functies


### Gewone functies

Een functie is een stukje herbruikbare code waarmee je de mate van hergebruik van je code hoger maakt. Simpeler gezegd is het een klein programma in je programma die je steeds opnieuw kan gebruiken.

In Python is het heel makkelijk in gebruik. Net als de logische operaties en de loops geef je het aan met een dubbele punt, ident en het sleutelwoord `def`. Ook moet je na de naam van je functie haakjes met daarin de argumenten of parameters die je functie nodig heeft plaatsen. Bijvoorbeeld:


```python
def zeg_iets(woord):
    print(woord)
```


Dit noemen we een void. Een functie die niks teruggeeft. Als je functie iets “returnt” noemen we het anders. (Kijk bijvoorbeeld naar functies van Java). In Python is return ook heel makkelijk. Hier is bijvoorbeeld een functie die de som van 2 argumenten teruggeeft:


```python
def som(a, b):
    return a + b
```


Deze functie kan je gebruiken bijvoorbeeld om het uit te printen:


```python
def som(a, b):
    return a + b

print(som(5, 36))
```



### Éénregelfuncties

Je kan ook functies maken die maar één regel hebben. Dat is handig als je een kleine functie hebt en je je code zo simpel mogelijk wil houden. Bijvoorbeeld de som functie van hierboven kan je ook zo declareren:


```python
def som(a, b): return a + b
```


En dit zal net als een gewone functie werken.


### Lambdas (Anonieme functies)

In Python kun je ook éénregelfuncties maken die geen naam hebben. Deze noem je anonieme functies (Of lambdas). Dat is handig als je bijvoorbeeld geen extra geheugen wil verspillen aan opslaan van de functie. Lambdas geef je zo aan:


```python
lambda x: x**2
```


Maar je kan deze functie dus straks niet meer gebruiken als je het niet opslaat onder een naam of als je het niet doorgeeft. Het kan bijvoorbeeld door het aanmaken van een variabele:


```python
s = lambda x: x**2
```


En als je deze functie dus wil gaan gebruiken moet je de variabele “s” gebruiken:


```python
s = lambda x: x**2
print(s(10))
```



```
Opdracht 2:
Nu kan je behoorlijk zelfstandig simpele programma's maken. Probeer je creativiteit te uiten en een hele simpele programma te maken. Het maakt niet uit wat als het maar de bovenstaande kennis gebruikt.
Maak een programma die de bovenstaande kennis gebruikt


Ideeën voor je programma:
Chatbot
Geavanceerde rekenmachine
Verhaal generator
Overhoorprogramma
Text-Game 
Virtueel huisdier
      etc.

```



## Import, Namespaces, Random


### Import

Je kan natuurlijk programma’s maken met standaard functies en instrumenten van Python maar het is veel makkelijker om modules, programma’s die al doen wat je wilt te gebruiken. Bijvoorbeeld de “Turtle” module. Daarmee kan je heel makkelijk tekeningen maken. Soms kun je iets ook niet zonder een module (Behalve als je er zelf één maakt). Bijvoorbeeld een GUI (Graphical User Interface) maken. Dat kan in Python bijvoorbeeld door “Tkinter”, “PyQt” en nog veel meer modules.

Je kan modules installeren door middel van “PIP”. Pip is de package manager van Python. Daarmee kan je modules heel snel installeren en deïnstalleren. Open je CMD/Terminal en typ in:


```python
pip install django
```


Django is een web-framework die we later gaan gebruiken. Nu hoef je nog niet te weten wat het is. Maar als je nu een nieuw bestand aanmaakt kan je de sleutelwoord `import `met de naam van het pakket (In dit geval  `django`) gebruiken zonder foutmeldingen:


```python
import django
```


Door middel van import kan je ook functies uit je eigen bestanden die zich in dezelfde folder bevinden importeren. Dus als dit je fileboom is:


```
./
 /main.py
 /other_file.py
```


Kan je in main.py dus `import .other_file` gebruiken

Je kunt ook specifieke functies, variabelen en objecten importeren uit modules. Om dat te doen komt er nog een sleutelwoord bij: `from`

Stel je voor je wilt alleen de functie randint importeren uit de module random. Dan doe je dit:


```python
from random import randint
```


Dit zorgt ervoor dat alleen de functie randint geïmporteerd wordt en je programma minder RAM nodig heeft voor het uitvoeren, waardoor het sneller gaat werken (Maar hier merk je nu niet zo veel van omdat je hele kleine programma's maakt).

Je kan ook alles uit een module importeren door een `*` te gebruiken:


```python
from random import *
```



```
Tip 🙋:
Het is overzichtelijker voor jou en andere programmeurs als je alle imports aan het begin van je bestand doet
```



### Namespaces

Variabelen zijn namen die wijzen naar een object. Een namespace is een “woordenboek” voor namen van de variabelen (Keys) en de bijpassende waarden (Values).

Een functie/statement kan gebruik maken van globale en lokale namespaces. Python denkt standaard dat als je een variabele declareert in een functie, loop etc. dat het een lokale variabele is en gaat je programma niet werken. Bijvoorbeeld hier:


```python
Geld = 2000
def PlusGeld():
   Geld = Geld + 1

print(Geld)
PlusGeld()
print(Geld)
```


Om het te laten werken moet je in de functie PlusGeld() aangeven dat variabele Geld globaal is. Dat kan met het sleutelwoord “`global`”:


```python
Geld = 2000
def PlusGeld():
   global Geld
   Geld = Geld + 1

print(Geld)
PlusGeld()
print(Geld)
```


Hetzelfde geldt voor loops (Vaak hoeft het niet bij loops).

Modules, dus pakketten en bestanden die je importeert door import hebben dus ook een eigen namespace.


### Random

Om je te laten zien hoe modules werken is hier een voorbeeld van de “Random” module:


```python
import random
print(random.randint(0, 15))
```


Wat deze stukje code doet is een pseudo random getal uitprinten tussen 0 en 15.


```
Opdracht 3:
Je hebt weer veel kennis bijgekregen. Maar weet je ook welke modules er allemaal bestaan? 
Zoek op internet naar een paar simpele modules en maak een programma met gebruik van de module die je hebt gekozen
Maak zelf een bestand met functies aan en gebruik die functies in een andere programma.
Probeer nu meerdere imports te doen. Combineer je eigen bestanden met modules van buitenaf.
Bereid je programma uit opdracht 2 uit met gebruik van modules.
```



## Werken met bestanden

In python is het heel makkelijk om informatie op te slaan in bestanden. Je hoeft zelfs niks te importeren. Kijk naar de voorbeeld en lees daarna wat het doet en waarom:


```python
file = open("test.txt", 'w+')
file.write("This is a test file with test text")
file.close()
file1 = open("test.txt", 'r')
print(file1.read())
file1.close
```


Nu gaan we langs elke regel:



1. Je maakt een variabele waarin je een object “File” als waarde plaatst. Dat doe je met functie open en je geeft de volgende argumenten door: naam van de bestand en de modus waarmee je het opent. Als het duidelijk is wat je met het bestand moet doen, kan het wat moeilijker zijn om te begrijpen hoe de modussen werken. Hier een overzicht:
    1. r: Open het bestand alleen om te lezen en aan het begin 
    2. r+: Open het bestand om te lezen en te schrijven en aan het begin` `
    3. w: Open het bestand alleen om te schrijven en aan het begin
    4. w+: Open het bestand om te schrijven en te lezen en aan het begin 
    5. a: Open het bestand alleen om te schrijven en aan het einde 
2. Schrijf in het bestand de tekst `"This is a test file with test text" `
3. Sluit het verbinding af met het bestand. Zo is het bestand nu beschikbaar voor andere programma’s
4. Open hetzelfde bestand maar dit keer alleen om te lezen
5. Print uit wat het bestand bevat
6. Sluit het verbinding af met het bestand. 

Als je dit te weinig informatie vindt over bestanden, bezoek dan deze website: 

[Programmeren in Python - Bestanden(Wikibooks)](https://nl.wikibooks.org/wiki/Programmeren_in_Python/Bestanden)


## Classes (Klasse)


```
Info🙌:
Object-Georienteerd programmeren (OOP) is het gebruiken van het concept van "objecten" die gegevens kunnen bevatten in vorm van velden, vaak attributen genoemd en code, in de vorm van procedures, vaak methods genoemd.
bron: Object-oriented programming(wikipedia)

Python is een Object-Georienteerde programmeertaal en heeft dus Classes (Klassen).
Een class in een uitbreidbare programmacode-sjabloon voor het maken van objecten, het leveren van beginwaarden (lidvariabelen) en implementaties van gedrag (lidfuncties of -methoden). 
bron: Class(wikipedia) 
```


In Python geef je een class aan met het sleutelwoord class, de naam van je class en de dubbele punt. De attributen die bij de class behoren worden in een tab blok gezet. Alle niet-statische functies van een class worden methods genoemd en moeten het argument `self` als het eerste argument bevatten. Een class kan ook een `__init__` functie hebben. Deze functie wordt uitgevoerd zodra een object van die class wordt aangemaakt. In een method moeten de lidvariabelen met een `self.` komen. Hier is een voorbeeld van een class voor een school:


```python
class School:
    name = ""
    pupil-count = 0
    
    def __init__(self, name, pupil-count):
        self.name = name
        self.pupil-count = pupil-count
    
    def get_attributes(self):
        return (self.name, self.pupil-count)
```


Dit is alleen maar basiskennis over klassen. Meer zul je later leren, wanneer je echt gaat programmeren.


```
Opdracht 4 (Afsluiting van 1e hoofdstuk):
Je bent bijna bij het eindpunt van het 1e hoofdstuk. Hierna komen er meerdere hoofdstukken maar hier heb je als je basiskennis gekregen. Gefeliciteerd!
Maar voor dat je verder gaat stel ik je voor om een simpel administratieprogramma te maken waarin je kan bijhouden hoeveel geld je hebt en waaraan je het hebt besteed/waarvandaan je het hebt gekregen.
Maak een administratieprogramma (In tekstformaat) waarmee je kan:
Bijhouden hoeveel geld je hebt
Hoeveel heb je uitgegeven
En waaraan
Hoeveel geld je hebt gekregen
En waarvandaan

Veel plezier! En vergeet niet: ["Hip!", "Hip!"] (Hip Hip Array) 
```



## Algoritmes

Programmeren is niet alleen code schrijven, maar ook logisch nadenken en betere oplossingen bedenken. Heel veel dingen kun handmatig doen, maar is het niet leuker om de computer alles voor jou te laten doen? Bijvoorbeeld een lijst met getallen sorteren van groot naar klein. Of vinden waar een getal zich bevindt. Dat is allemaal mogelijk te doen met algoritmes. Eigenlijk is alle code die een programmeur schrijft een reeks van algoritmes, maar sommige algoritmes worden door iedereen gebruikt en zijn de beste in hun soort.


## Binary search

**Note: _Deze algoritme werkt alleen met gesorteerde lijsten. Dat houdt in dat de getallen gesorteerd zijn van klein naar groot of andersom_**

In de afdeling hiervoor over Python heb je geleerd wat lijsten (arrays) zijn. In die lijsten kun je alle soort data bewaren maar stel je voor hebt de volgende lijst:


```python
list = [-9, 6, 8, 14, 15, 36, 47, 48, 78, 105]
```


en je wil weten wat de index (De adres waarmee je de getal kan krijgen **Note: **In _bijna _alle programmeertalen beginnen de indexen bij 0, dus als ik wil de -9 uit deze lijst wil halen moet ik dus `list[0]` gebruiken) van het getal 14 is? Ik kan natuurlijk met een functie de hele lijst gaan doorzoeken en als ik 14 vind dat teruggeven, maar stel je voor dat je een lijst hebt van 4000000000 (4 miljard) getallen en 14 bevindt zich helemaal aan het einde. Dan zou je de hele lijst door moeten gaan en 4000000000 keer controleren of het de juiste getal is. Daar zal je computer eventjes over doen. Om dat te voorkomen bestaat er een hele simpele algoritme die “Binary Search” heet.

Wat het doet is de volgende:

Pak de middelste getal; Kijk of het groter of kleiner is dan de getal die wij zoeken; Als het groter is dan ga je dezelfde doen maar dan met de kleinere helft van de lijst; Als het groter is dan ga je dezelfde doen maar dan met de grotere helft van de lijst; Herhaal dit totdat je bij jouw getal aankomt.

Met de lijst hierboven zou het er zo uitzien:


```
[-9, 6, 8, 14, 15, 36, 47, 48, 78, 105] -> [-9, 6, 8, 14, 15, 36] -> 14
```


Of je zoekt bijvoorbeeld naar 78:


```
[-9, 6, 8, 14, 15, 36, 47, 48, 78, 105] -> [36, 47, 48, 78, 105] -> [48, 78, 105] -> 78
```


Zo zie je dus dat je in plaats van 9 iteraties maar 3 nodig hebt om een getal helemaal aan het einde te vinden.

Je kunt zelf berekenen hoeveel iteraties er nodig zijn om het te vinden. In de slechtste geval (worst case) is de formule **log<sub>2</sub>(n)** waar n gelijk is aan de lengte van de lijst.

Hier een voorbeeld van hoe erg het helpt om je programma sneller te laten werken:


<table>
  <tr>
   <td>Lengte lijst
   </td>
   <td>Hoeveel iteraties Gewoon de lijst doorzoeken
   </td>
   <td>Hoeveel iteraties Binary Search
   </td>
   <td>Hoeveel x verschil
   </td>
  </tr>
  <tr>
   <td><strong>5</strong>
   </td>
   <td> <strong>n = 5</strong>
   </td>
   <td><strong>log<sub>2</sub>(n) = ±3</strong>
   </td>
   <td><strong>±2</strong>
   </td>
  </tr>
  <tr>
   <td><strong>1000</strong>
   </td>
   <td> <strong>n = 1000</strong>
   </td>
   <td><strong>log<sub>2</sub>(n) = ±10</strong>
   </td>
   <td><strong>±100</strong>
   </td>
  </tr>
  <tr>
   <td><strong>4000000000</strong>
   </td>
   <td><strong> n = 4000000000</strong>
   </td>
   <td><strong>log<sub>2</sub>(n) = ±32</strong>
   </td>
   <td><strong>±125000000</strong>
   </td>
  </tr>
</table>



## Gui’s met Python


### Oftewel Knopjes en Invoervelden


```
Info🙌:
GUI's (Graphical User Interface) zijn de programma's die je gewent bent te gebruiken. Kijk bijvoorbeeld naar Word, Google Chrome etc. Het zijn dus programma's die de gebruiker kan gebruiken door te klikken op grafische elementen. Tot nu toe heb je console applications gemaakt. Die kan je alleen gebruiken in CMD/Terminal, dus is het moeilijk om een interactief programma te maken. Nu ga je bezig met GUI's. Veel plezier!
Hieronder zie je een voorbeeld van een GUI in Java 
bron: GUI Examples(Google Images)

```



## Tkinter

Tkinter is de simpelste framework voor GUI’s in Python. Het is al ingebouwd dus hoef je het niet zelf te installeren. 

Als je een complete documentatie wil van tkinter kan je [deze ](https://docs.python.org/3/library/tk.html)link openen.

Om een simpele interface te maken net als hierboven moeten we nog simpeler beginnen of beter gezegd, helemaal aan het begin. 

Tkinter is een module dus het eerste wat we moeten doen is het importeren:


```python
from tkinter import *
```


Nu maken we een `Tk()` object aan, dat wordt ons “scherm”, die noemen we `root`


```python
from tkinter import *

root = Tk()
```


Nu hebben we al een frame(zie plaatje hierboven). Om het te kunnen zien moeten we nog 1 lijn code toevoegen:


```python
from tkinter import *

root = Tk()

root.mainloop()
```




<p id="gdcalert1" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/Python-voor0.png). Store image on your image server and adjust path/filename if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert2">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/Python-voor0.png "image_tooltip")


Om tekst toe te voegen gebruiken we de widget “Label”. De naam zegt al alles over geze widget. Om een label te plaasten in ons frame moeten we de volgende code toevoegen:


```python
from tkinter import *

root = Tk()

w = Label(root, text="Hello, world!")
w.pack()

root.mainloop()
```


Als we dit nu opstarten zien we dit:



<p id="gdcalert2" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/Python-voor1.gif). Store image on your image server and adjust path/filename if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert3">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/Python-voor1.gif "image_tooltip")


Wat we deden is dus een object van de Class Label aanmaken en die “pack”en in de root frame. Zo kun je met bijna alle widgets omgaan. 


```
Opdracht 1:
Je opdracht nu is om zelfstandig op zoek te gaan naar andere widgets van Tkinter en een applicatie te maken die je leuk vindt.
Maak een app met Tkinter, zoek naar widgets op internet

```



## Einde

Zoals je hebt gemerkt is deze cursus niet zo lang maar je weet nu alles om zelf verder te gaan. Je weet hoe syntax van Python werkt, hoe je simpele gui’s kan maken en hoe je informatie op internet kan opzoeken. Nu is het aan jou wat je verder met deze kennis gaat doen en hoe je het gaat exploiteren. Ik ben trots op je als je tot hier bent gekomen!


### Nuttige websites:



1. GOOGLE!!!!!
2. Stackoverflow
3. GitHub
4. W3 Schools
5. Reddit
6. Pastebin
7. Google Developers
