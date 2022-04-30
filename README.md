# Semesteroppgave-i-valgfag-programmering


## Hvorfor valgte jeg å lage dette?

Vel, kryptografi er kult og utvikling av nettsider er kult. Det var da jeg fikk tanken om å bare lage en nettside der en bruker kunne putte inn tekst, og få det kryptert med en cæsarchiffer. Til alle kryptografere som leser dette, jeg vet at cæsarchiffer teoretisk sett, ikke kan kalles for kryptering fordi den gir deg lik null sikkerhet. Dermed, ikke legg inn meldinger og kryper de her for å sende til andre, i sammenheng til kriminalitet og tro at ingen vet hva du sier.


# Forklarning av koden

_jeg bare viser det som er viktig, ikke det som er åpenlyst_


### Cæsarchiffer Boksen

[![image](https://www.linkpicture.com/q/Skjermbilde-2022-04-30-200201.png)](https://www.linkpicture.com/view.php?img=LPic626d79a8ad128316846195)

```Html
<div class="cæsarchiffer">
    <h1>Cæsarchiffer</h1>
      <p class="p-padding">
        Innen kryptografi er cæsarchiffer, også kjent som Caesars chiffer, skiftchiffer, Cæsars kode og cæsarskift, en av de enkleste og mest kjente krypteringsteknikker. Det er en type substitusjonschiffer der hver bokstav i klarteksten erstattes med en annen bokstav et gitt antall steg lenger ut i alfabetet. <a href="https://no.wikipedia.org/wiki/C%C3%A6sarchiffer" target="_blank">Wikipedia</a>.
      </p>
      <textarea id="text" placeholder="Skriv tekst her!" tabindex="12"></textarea>
      <br>
      <label>Skift:</label>
      <input type="number" id="rot" min="1" max="25" value="blank">
      <br>
      <button onclick="rot()" class="rgb">ENCRYPT</button>
      <h3>Resultat:</h3>
      <p id="result"></p>
    </div>
```
Som du ser her
