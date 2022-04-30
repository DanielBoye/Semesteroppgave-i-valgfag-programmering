# Semesteroppgave-i-valgfag-programmering


## Hvorfor valgte jeg å lage dette?

Vel, kryptografi er kult og utvikling av nettsider er kult. Det var da jeg fikk tanken om å bare lage en nettside der en bruker kunne putte inn tekst, og få det kryptert med en cæsarchiffer. Til alle kryptografere som leser dette, jeg vet at cæsarchiffer teoretisk sett, ikke kan kalles for kryptering fordi den gir deg lik null sikkerhet. Dermed, ikke legg inn meldinger og kryper de her for å sende til andre, i sammenheng til kriminalitet og tro at ingen vet hva du sier.


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
