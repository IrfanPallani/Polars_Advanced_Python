Polars-fördjupning


Om Projektet
Det här är min fördjupningsuppgift i kursen Avancerad Python för Data Scientist på EC Utbildning.
Jag har tittat närmare på Polars, som är ett DataFrame-bibliotek för Python. Jag har framför allt testat hur man arbetar med data i Polars och jämfört det med Pandas i både syntax och prestanda.

Vad projektet gör:
Projektet består av en Jupyter-notebook, polars_fordjupning. ipynb, där jag:
•	läser in en CSV-fil med elförbrukningsdata
•	filtrerar och sorterar data
•	räknar ut nya kolumner
•	grupperar och summerar data per region, sektor och månad
•	testar lazy evaluation med scan_csv()
•	jämför Polars mot Pandas på en testfil med en miljon rader
Datan är syntetisk och föreställer daglig elförbrukning för fem svenska städer under 2025. Datan är uppdelad på hushåll, industri och kommersiell verksamhet.

Installation
Öppna terminalen och kör:
pip install polars pandas numpy jupyter
Så kör du projektet
1. Klona repot eller ladda ner projektmappen.
2. Öppna terminalen i projektmappen.
3. Starta Jupyter:
jupyter notebook
4. Öppna filen polars_fordjupning.ipynb.
5. Kör notebookens celler uppifrån och ner.
Notebooken skapar och tar bort en temporär testfil, stor_testfil.csv, under prestandatestet.


Bibliotek
•	polars
•	pandas
•	numpy
•	jupyter
Versionerna som användes när notebooken kördes:
•	Polars 1.44.2
•	Pandas 3.0.2
•	Python 3.12.10

Data
Filen elforbrukning.csv ligger i projektet.
Datan är syntetisk och skapad för uppgiften. Den innehåller säsongsvariation och några medvetet saknade värden i temperaturkolumnen.

Kolumner
datum – datum under 2025
region – Stockholm, Göteborg, Malmö, Uppsala eller Umeå
sektor – Hushåll, Industri eller Kommersiell
forbrukning_kwh – förbrukning i kWh
pris_sek_per_kwh – elpris i kr/kWh
temperatur_c – medeltemperatur i grader Celsius

Källor
Polars dokumentation:
https://docs.pola.rs/
Polars GitHub:
https://github.com/pola-rs/polars
Pandas dokumentation:
https://pandas.pydata.org/docs/
