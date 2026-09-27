# Fördjupningsuppgift: Polars i Python

Fördjupningsuppgift i kursen Avancerad Python för Data Scientist, EC Utbildning.
Ämnet handlar om **Polars** som är ett bibliotek för dataanalys i Python, liknande Pandas men med 
fokus på prestanda och effektivitet. Polars är byggt på Rust och erbjuder snabbare databehandling, 
särskilt för stora dataset. Med Polars kan man läsa in data, filtrera, sortera och sammanställa 
data på ett effektivt sätt.  


## Innehållet i mappen finns följande filer:

| Fil | Beskrivning |
|---|---|
| `polars_fordjupning_enkel.ipynb` | Jupyter-notebook med all kod, körd och förklarad steg för steg |
| `Polars_rapport_enkel.pdf` | Den skriftliga rapporten (valt område, fokus, praktisk del, relevans, avgränsning, slutsats, källor) |
| `elforbrukning.csv` | Exempeldatan som notebooken använder |
| `README.md` | Den här filen |

## Vad uppgiften går igenom

- Läsa in data med `pl.read_csv()`
- Utforska data (antal rader/kolumner, datatyper, saknade värden)
- Filtrera rader utifrån villkor
- Sortera data
- Räkna ut en ny kolumn med `.with_columns()`
- Gruppera och summera med `.group_by()` / `.agg()`
- En enkel jämförelse med Pandas, både i hur koden skrivs och hur lång tid den tar att köra


## Om datan

`elfrobruknin.csv` är inte hämtad från någon extern källa - det är en egen påhittad (syntetisk)
datamängd som skapades för att ha något konkret att öva på. Den innehåller daglig elförbrukning för
fem svenska städer (Stockholm, Göteborg, Malmö, Uppsala, Umeå) under 2025, uppdelat på sektorerna
hushåll, industri och kommersiell verksamhet, med en inbyggd säsongsvariation och ett antal 
medvetet saknade temperaturvärden att öva filtrering på.
Riktig svensk elstatistik finns öppet hos bland annat:
- [SCB:s statistikdatabas](https://www.statistikdatabasen.scb.se/) - elanvändning i Sverige
- [Energimyndigheten](https://www.energimyndigheten.se/) - statistikansvarig myndighet för elstatistik

Kolumner i `elforbrukning.csv`:

| Kolumn | Beskrivning |
|---|---|
| `datum` | Datum (2025-01-01 till 2025-12-31) |
| `region` | Stad: Stockholm, Göteborg, Malmö, Uppsala eller Umeå |
| `sektor` | Hushåll, Industri eller Kommersiell |
| `forbrukning_kwh` | Förbrukning i kWh den dagen |
| `pris_sek_per_kwh` | Elpris i kr/kWh |
| `temperatur_c` | Medeltemperatur den dagen i °C (vissa värden saknas) |

## Hur man kör notebooken

Behöver Python 3 samt bibliotekena `polars` och `pandas`:

```bash
pip install polars pandas
```

ÖPppna sedan `polars_fordjupning_enkel.ipynb` i Jupyter (eller VS Code / valfri notebook-miljö) 
och kör cellerna i ordning. Notebooken förväntar sig att `elforbrukning.csv` ligger i samma mapp, 
vilket den gör här direkt.


## Källor

- Polars officiella dokumentation: https://docs.pola.rs/
- Polars på GitHub: https://github.com/pola-rs/polars