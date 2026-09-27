Fördjupningsuppgift: Polars i Python

Fördjupningsuppgift i Avancerad Python, kursen Data Scientist, EC Utbildning.
Ämnet är biblioteket Polars för Python — grunderna i att läsa, filtrera, sortera och sammanställa 
data, lazy evaluation, samt en jämförelse mot Pandas i både syntax och prestanda.


Innehåll och besrkivning av filerna i mappen

polars_fordjupning.ipynb Jupyter-notebook med all kod, körd och förklarad steg för steg
Polars_rapport.pdf	Den skriftliga rapporten (valt område, fokus, praktisk del, relevans, avgränsning, slutsats, källor)
Polars_presentation.pptx Presentation för muntlig redovisning av uppgiften
elforbrukning.csv Exempeldatan som notebooken använder
README.md Den här filen
Vad uppgiften går igenom
Läsa in data med pl.read_csv() och utforska den (schema, saknade värden, statistik)
Filtrera rader utifrån villkor
Sortera data på en och flera kolumner
Beräkningar av nya kolumner, inklusive villkorsbaserade beräkningar med pl.when().then()
Gruppering och aggregering (group_by / agg) på en eller flera kolumner
Lazy evaluation med pl.scan_csv() och .collect(), samt hur man kan läsa den optimerade planen med .explain()
En direkt jämförelse mellan Polars och Pandas, både i syntax och i hastighet, med en egen benchmark på en miljon rader
Om datan

elforbrukning.csv är inte hämtad från någon extern källa — det är en egen påhittad (syntetisk) datamängd som skapades för att ha något konkret att öva på. Den innehåller daglig elförbrukning för fem svenska städer (Stockholm, Göteborg, Malmö, Uppsala, Umeå) under 2025, uppdelat på sektorerna hushåll, industri och kommersiell verksamhet, med en inbyggd säsongsvariation (högre förbrukning vintertid) och ett antal medvetet saknade temperaturvärden att öva filtrering på.

Riktig svensk elstatistik finns öppet hos bland annat:

SCB:s statistikdatabas - elanvändning i Sverige
Energimyndigheten - statistikansvarig myndighet för elstatistik

Kolumner i elforbrukning.csv:

Kolumn	Beskrivning
datum	Datum (2025-01-01 till 2025-12-31)
region	Stad: Stockholm, Göteborg, Malmö, Uppsala eller Umeå
sektor	Hushåll, Industri eller Kommersiell
forbrukning_kwh	Förbrukning i kWh den dagen
pris_sek_per_kwh	Elpris i kr/kWh
temperatur_c	Medeltemperatur den dagen i °C (vissa värden saknas)

Benchmark-delen i notebooken skapar dessutom en egen, tillfällig testfil med en miljon slumpade rader (stor_testfil.csv) för att jämföra prestanda mellan Polars och Pandas. Den filen tas bort igen automatiskt av notebooken efter att testet är klart, så den finns inte kvar i mappen.

Hur man kör notebooken

Behöver Python 3 samt bibliotekena polars, pandas och numpy:

bash
pip install polars pandas numpy

Öppna sedan polars_fordjupning.ipynb i Jupyter (eller VS Code / valfri notebook-miljö) och kör cellerna i ordning. Notebooken förväntar sig att elforbrukning.csv ligger i samma mapp, vilket den gör här direkt. Benchmark-delen mot en miljon rader kan ta någon sekund extra att köra beroende på datorns prestanda.

Källor
Polars officiella dokumentation: https://docs.pola.rs/
Polars på GitHub: https://github.com/pola-rs/polars
Pandas officiella dokumentation: https://pandas.pydata.org/docs/