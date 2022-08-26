# Semesteroppgave-i-valgfag-programmering

Oppgaven ligger ute her: https://caesarchiffer.netlify.app/

## Hvorfor valgte jeg å lage dette?

Vel, kryptografi er kult og utvikling av nettsider er kult. Det var da jeg fikk tanken om å bare lage en nettside der en bruker kunne putte inn tekst, og få det kryptert med en cæsarchiffer. Til alle kryptografere som leser dette, jeg vet at cæsarchiffer teoretisk sett, ikke kan kalles for kryptering fordi den gir deg lik null sikkerhet. Dermed, ikke legg inn meldinger og kryper de her for å sende til andre, i sammenheng til kriminalitet og tro at ingen vet hva du sier.

Jeg er klar over at nettsiden er inne i en index.html fil, og at det ikke er noen style.css eller script.js. Jeg valgte å bare legge alt inne i index.html for å få litt bedre overskrift. Dette er ikke "best practise", men jeg overlever for denne gang. 

# Forklarning av koden _jeg bare viser det som er viktig, ikke det som er åpenlyst_

## Cæsarchiffer Boksen

Vi starter først å lage en cæsarchiffer classe for å endre på utseende senere i css. Jeg har lagt inn en h1 for å skrive inn overskriften. Under den kommer paragrafen som "p" der jeg skrev inn litt infromasjon om hva en cæsarchiffer er. På enden av denne paragrafen legger jeg inn en hyperlink til ordet Wikipedia siden det var der jeg fant informasjonen. 
```Html
<div class="cæsarchiffer">
    <h1>Cæsarchiffer</h1>
      <p class="p-padding">
        Innen kryptografi er cæsarchiffer, også kjent som Caesars chiffer, skiftchiffer, Cæsars kode og cæsarskift, en av de enkleste og mest kjente krypteringsteknikker. Det er en type substitusjonschiffer der hver bokstav i klarteksten erstattes med en annen bokstav et gitt antall steg lenger ut i alfabetet. <a href="https://no.wikipedia.org/wiki/C%C3%A6sarchiffer" target="_blank">Wikipedia</a>.
      </p>
```
Etter paragrafen legger jeg inn et tekstområde, der en bruker kan skrive inn tekst. Dette er feltet vi skal hente informasjonen ifra, og kryptere senere. Jeg gir denne id-en text. En <br> la jeg også inn for å få litt pusterom før neste blokk kommer inn.   
```Html
 <textarea id="text" placeholder="Skriv tekst her!" tabindex="12"></textarea>
      <br>
```
Her legger jeg inn et nytt felt, men kan bare ta imot nummer siden den har typen "number". Siden cæsarchiffer lar deg skifte teksten med hvor mange bokstaver det er i alfabetet legger jeg inn en maks verdi i dette feltet på 25, og en minnimum på 1. Det går ikke an å skifte en bokstav null ganger. Hvis du har fått det til, gi en beskjed til meg. For å ha mest mulig brukervennlighet velger jeg også at den verdien som er inni feltet når du laster inn nettsiden, blir null ved å sette verdien til "blank". Teksten du skriver inn her blir lagret i variabelen "rot". Det sees med at den har id="rot".
```Html
 <label>Skift:</label>
      <input type="number" id="rot" min="1" max="25" value="blank">
      <br>
```
Så legger jeg inn krypter knappen, og gir den classen rgb for å gi den en regnbue-effekt senere i css. Når du trykker denne knappen sender den funksjonen "rot()", ned til JavaScript koden for å kryptere meldingen.  
```Html
 <button onclick="rot()" class="rgb">ENCRYPT</button>
```
Under denne knappen kommer resultatet/den ferdig krypterte meldingen. Denne legger jeg inn som en h3, for å den litt større.
```Html
 <h3>Resultat:</h3>
```
Så kommer selve resultatet. Denne bare printer ut "result" som blir sendt ifra krypteringskoden som er helt på bunnen av koden. </div> lukker selve cæsarchiffer div-en, og markerer enden på den første boksen 
```Html
 <p id="result"></p>
</div>
```
Med alt dette (+ litt css) ser boksen slik ut. 

[![image](https://www.linkpicture.com/q/Skjermbilde-2022-04-30-200201.png)](https://www.linkpicture.com/view.php?img=LPic626d79a8ad128316846195)

## Om koderen

Jeg viser bare den første her. Alt det samme gjelder for de andre boksene utenom h2 overskriften, og selve teksten inne i paragrafen.

Alle boksene er satt i samme div, det er derfor det kan se ut som det er en eksta bare på starten. Tilbake til koden. Alle boksene er koblet opp til flere klasser for å klare å effektivt endre utseende og padding på alle sammen, istedenfor å gå inn å redigere på hver enkelte. Overskriften er h2 for å gi litt volum til teksten. Paragrafen får klassen "p-padding" for å kunne redigere paddingen enkelt på alle paragrafene. Linkene henviser til hvor jeg jobber, hva fag dette her er, og LinkedIn profilen min. To <br> etter et avsnitt passet bra, for å gi de litt rom for å puste.   

```Html
<div>
        <div class="hovedboks">
            <div class="hovedboks-padding">
                 <div class="enkelboks">
                    <div class="enkelboks-padding">
                        <h2 class="h2-overskrift">Om koderen</h2>
                        <p class="p-padding">
                            Daniel Boye er en elev ifra 10-klasse som liker å tenke fremover. Han engasjerer seg alt for mye i blokkjedeteknologi og utvinning av kryptovaluta. Han er ekstremt engasjert i sikkerhet og personvern, og leser seg opp på nye smarte løsninger til full personvern rundt penger.
                            <br>
                            <br>
                            Daniel jobber i <a href="https://www.konciv.com/" target="_blank">Konicv</a> og driver med cybersikkerhet og softwareutvikling på fritiden. 
                            <br>
                            <br>
                            Et av hans første prosjekt er nemlig denne nettsiden som er en semesteroppgave i valgfaget <a href="https://www.udir.no/lk20/prg01-02/kompetansemaal-og-vurdering/kv304" target="_blank">programmering</a> på ungdomsskolen. 
                            <br>
                            <br>
                            Daniel Boye finner du på<a href="https://www.linkedin.com/in/danielboye/" target="_blank">LinkedIn</a>.
                        </p>
                    </div>
                </div>
```

Denne boksen som vist over er bare for "Om koderen" men det samme gjelder for alle de andre boksene, bare paragrafen og overskriften er endret. 

Med alt dette sammen (+ litt css) ser boksene slik ut.

[![image](https://www.linkpicture.com/q/Skjermbilde-2022-04-30-205526.png)](https://www.linkpicture.com/view.php?img=LPic626d8632266e2917369912)

_jeg hopper over css, det er ikke relevant til oppgaven_

## Javascript

Her aktiveres funksjonen rot(). Som du sikker husker, blir denne aktivert med å trykke på "Encrypt" knappen. Når funksjonen blir igangsatt deklarerer vi noen variabler, arrays og setter grenser til at det er bare ASCII karakterer som aksepteres. 

```JavaScript
  function rot() {
  var rotCharArray = [];
  var regEx = /[A-Z]/;
```

Str variabelen bare henter inn teksten som du har skrevet i html filen, og returnerer verdien i teksten i store bokstaver, pluss splitter opp array-en.

```JavaScript
  var str = document.getElementById("text").value.toUpperCase().split("");
```

Result variabelen bare lagrer resultatet, som senere kommer til å bli sendt ut til paragrafen med id="result"

```JavaScript
  var result = document.getElementById("result");
```

Returnerer elementet som representerer id-en, og matcher stringen. Denne blir lagret i variabelen rot. Rot er nummeret du skrev inn med hvor mange skift du vil at meldingen din skal ha.

```JavaScript
  var rot = Number(document.getElementById("rot").value);
```

En loop for å dobbeltsjekke om du har skrevet noe inn. Hvis ikke, sjekker den om tallet du skrev inn er imellom 1 og 25 ved å bruke logikk operatorene ||. || betyr at begge to sidene må være sanne før koden kan gå videre.  

```JavaScript
if (str.length < 1) {
    result.innerHTML = "Skriv noe inn!";
  } else if (rot < 1 || rot > 25) {
    result.innerHTML = "Skift må være et tall mellom 1 og 25!";
```

Etter vi har fått bekreftet at alt er innenfor reglene vi lagte, kan vi begynne på selve krypteringen.

Den starter med en enkel for loop. if loopen er der for å kryptere meldingen. JavaScript opererer i ASCII verdier, noe som vil si at bokstaven egentlig er et tall. Hver eneste bokstav har ett tall til seg, så for å forskyve ordet trenger vi bare å addere sammen ordet og "forskyvningstall" vårt. Dette skjer ved å bruke 65 (som er starten for a i ASCII) og addere sammen variabelen "rot" som inneholder vårt "forskyvningstall", og blir lagret i rotCharArray etterpå.

```JavaScript
        rotCharArray.push(((str[x].charCodeAt() - 65 + rot) % 26) + 65);
      } else {
        rotCharArray.push(str[x].charCodeAt());
      }
    }
```

Hele krypterings loopen vår ser slik ut. 

```JavaScript
if (str.length < 1) {
    result.innerHTML = "Skriv noe inn!";
  } else if (rot < 1 || rot > 25) {
    result.innerHTML = "Skift må være et tall mellom 1 og 25!";
  } else {
    for (var x in str) {
      if (regEx.test(str[x])) {
        rotCharArray.push(((str[x].charCodeAt() - 65 + rot) % 26) + 65);
      } else {
        rotCharArray.push(str[x].charCodeAt());
      }
    }
```

Til slutt må vi printe ut svaret vi fikk til nettsiden. Dette gjøres med å hente inn rotCharArray, og legge den inn i variabelen "str". Vi printer ut "str" (altså svaret) til nettsiden ved å kople opp paragrafen med id="result" i html filen.  

```JavaScript
str = String.fromCharCode.apply(String, rotCharArray);
    result.innerHTML = str;
```
---

Jeg kommer senere til å legge ut nettsiden på et domene, som du slipper å ha filen lokalt på pc-en. Følg meg på [LinkedIn](https://www.linkedin.com/in/danielboye/) for oppdateringer rundt nettsiden. 
