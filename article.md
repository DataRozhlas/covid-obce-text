title: "Největší ohniska i poslední ostrůvky bez zjištěné nákazy. Sledujte, jak rychle se šíří koronavirus ve vaší obci"
perex: "Na základě dat, která ministerstvo zdravotnictví až do poloviny října tajilo, připravil server iROZHLAS.cz interaktivní aplikaci a mapu. Můžete si v nich porovnat, kde a s jakou rychlostí přibývá, či ubývá pozitivně testovnaých a kde je aktuálně nejvíc aktivních případů nemoci covid-19."
styles: ["https://fonts.googleapis.com/css2?family=Asap", "https://data.irozhlas.cz/covid-obce/tabulka.css"]
libraries: [] #jquery, d3, highcharts, datatables
options: [noheader, nopic] #wide, noheader (, nopic)
---

V Česku na konci minulého týdne [přibývalo každý den přes 100 nově diagnostikovaných případů nákazy koronavirem na 100 tisíc obyvatel](https://ourworldindata.org/coronavirus-data-explorer?zoomToSelection=true&time=2020-03-01..latest&country=~CZE&region=World&casesMetric=true&interval=smoothed&perCapita=true&smoothing=7&pickerMetric=total_cases&pickerSort=desc). „Takovou rychlost šíření jsme dosud neviděli skoro nikde jinde,“ [komentoval to Max Roser](https://twitter.com/MaxCRoser/status/1318863783146721281) z univerzity v Oxfordu, zakladatel [respektované databáze](https://ourworldindata.org/coronavirus) zachycující průběh pandemie. „Počet testů je přitom *(v ČR ve srovnání s jinými státy - pozn. red.)* velmi nízký. A hodně rychle stoupá i počet úmrtí,“ doplnil.

Na „semaforu“ ministerstva zdravotnictví [zčervenaly všechny okresy](https://onemocneni-aktualne.mzcr.cz/covid-19/stupne-pohotovosti), obtížně kontrolovatelný komunitní přenos nákazy už se tedy i podle hygieniků rozběhl v celé republice.

Přesto jsou v rychlosti, s jakou epidemie podle dostupných dat postupuje, patrné rozdíly: v okresech Zlín, Prostějov či Plzeň-sever vyšlo za posledních sedm dní více než tisíc pozitivních testů na sto tisíc obyvatel, v okresech Most, Karviná nebo Cheb méně než 500.

<div id="datarozhlas-covid-obce-tabulka-okresy"></div>
<script src="https://data.irozhlas.cz/covid-obce/build/tabulka-okresy.js"></script>


Aplikace je inspirovaná [projektem New York Times](https://www.nytimes.com/interactive/2020/us/coronavirus-us-cases.html). Každý den se automaticky aktualizuje a najdete v ní poslední údaje nejen z okresů, ale po rozkliknutí i ve všech obcích daného okresu. Seřadit podle různých kritérií si je můžete kliknutím na název sloupce.

České občany pozitivně testované na koronavirus aplikace sčítá podle místa jejich trvalého pobytu. Součty se proto mohou lišit od výsledků zveřejňovaných krajskými hygienickými stanicemi, pro něž není určující bydliště nemocných, ale místo výskytu nákazy.

Čísla nevypovídají jen o rychlosti šíření nemoci covid-19, ale také o finanční či dopravní dostupnosti testů a ochotě lidí je podstupovat. Podrobné údaje o provedených testech, které by umožnily vliv těchto faktorů odfiltrovat, však české úřady nepublikují.

## Podrobnosti by vyvolaly paniku

Také tato [nyní již veřejná](https://share.uzis.cz/s/dCZBiARJ27ayeoS) data o pozitivně testovaných lidech podle obce, kde jsou přihlášeni k trvalému pobytu, ministerstvo zdravotnictví dlouho tajilo.

Server iROZHLAS.cz o ně podle zákona o svobodném přístupu k informacím [požádal poprvé v dubnu](https://www.irozhlas.cz/zpravy-domov/soud-uzis-nzis-statistika-covid-koronavirus_2008030705_cib), úřad mu však ani po odvolání nevyhověl. Jeho argumentace se točila kolem [jediné věty](https://www.zakonyprolidi.cz/cs/2011-372/zneni-20190424#p73-7), kterou do zákona o zdravotních službách před dvěma lety prosadil poslanec ČSSD a hejtman kraje Vysočina Jiří Běhounek. V důvodové zprávě uvedl, že poskytování dat z Národního zdravotnického informačního systému veřejnosti by mohlo vést k „zavádějícím informacím o zdravotním stavu a vyvolávat u laického občana zbytečné obavy“.

Datoví novináři iROZHLASu o stejná data adresněji znovu [požádali v srpnu](https://www.irozhlas.cz/zpravy-domov/data-uzis-covid-19-cisla-informace_2009231251_cib), kdy je úřad začal poskytovat v méně podrobném členění, a to pouze starostům obcí. Ministerští právníci žádost opět smetli ze stolu, protože by podle nich detailní čísla vyvolala paniku a chaos. „Nezastupitelnou roli při řešení nastalé pandemie přitom ministerstvo sehrává rovněž při zklidňování veřejnosti a vysvětlování této celospolečenské, bezprecedentní, situace,“ napsali do zdůvodnění.

<wide>
<h2>Kolik lidí má testem potvrzený covid-19 ve vaší obci</h2>

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/leaflet/1.7.1/leaflet.css" integrity="sha512-xodZBNTC5n17Xt2atTPuE1HxjVMSvLVW9ocqUKLsCC5CXdbqCmblAshOMAS6/keqq/sMZMZ19scR4PsZChSR7A==" crossorigin="anonymous" />

<script src="https://cdnjs.cloudflare.com/ajax/libs/leaflet/1.7.1/leaflet.js" integrity="sha512-XQoYMqMTK8LvdxXYG3nZ448hOEQiglfqkJs1NOQV44cWnUrBc8PkAOcXy20w0vlaXaVUearIOBhiXZ5V3ynxwA==" crossorigin="anonymous"></script>
  
<script src="https://cdnjs.cloudflare.com/ajax/libs/topojson/3.0.2/topojson.min.js" integrity="sha512-4UKI/XKm3xrvJ6pZS5oTRvIQGIzZFoXR71rRBb1y2N+PbwAsKa5tPl2J6WvbEvwN3TxQCm8hMzsl/pO+82iRlg==" crossorigin="anonymous"></script>

<style>
    #covid_mapa { width:100%; height: 60vh; }
    .stylesel, #inp-btn {
      background-color:#ffffff;
      border-radius:6px;
      border:1px solid #dcdcdc;
      display:inline-block;
      cursor:pointer;
      color:#666666;
      font-size:12px;
      padding:3px 12px;
      margin: 1px;
      text-decoration:none;
    }
    #inp-geocode {
      background-color:#ffffff;
      border-radius:6px;
      border:1px solid #dcdcdc;
      display:inline-block;
      color:#666666;
      font-size:12px;
      padding:3px 12px;
      margin: 1px;
      text-decoration:none;
    }
</style>

<div id="style_select">
  <button type="button" class="stylesel aktual">Aktuální stav</button> 
  <button type="button" class="stylesel tyden">Před týdnem</button> 
  <button type="button" class="stylesel dva">Před dvěma týdny</button> 
  <button type="button" class="stylesel mesic">Před měsícem</button> 
  <button type="button" class="stylesel prazd_stop">Konec prázdnin</button> 
  <button type="button" class="stylesel prazd_start">Začátek prázdnin</button> 
  <button type="button" class="stylesel velik">Velikonoce</button>
</div>

<form action="?" id='geocoder'>
  <div class="inputs">
      <input type="text" id="inp-geocode" placeholder="Zadejte obec či adresu...">
      <input type="submit" id="inp-btn" value="Najít">
  </div>
</form>

<div id='covid_mapa'></div>

<script src="https://data.irozhlas.cz/covid-obce-mapa/mapa.js"></script>
<em>Kliknutím na oběc v mapě zobrazíte podrobnosti.</em>
</wide>

Změnu v komunikační strategii přinesl až nástup ministra zdravotnictví Romana Prymuly na konci září. „Nebráním se tomu, abychom publikovali vše, o co bude zájem,“ prohlásil na tiskové konferenci 16. října a v následujících dnech se skutečně v zákoutích ministerského webu začala objevovat některá z dat, která byla dříve pro laickou, ale i velkou část odborné veřejnosti úřadem zapovězena.

V té době už ale byla epidemie na českém území rozjetá a republika se propracovávala do čela celosvětových statistik. Jak ukazují data, z nichž je sestaven následující žebříček a mapa všech obcí, v Česku nezůstává mnoho míst, kde se nákaza dosud neprokázala. Sice téměř pětina obcí neměla v neděli 25. října mezi svými trvale hlášenými obyvateli žádný aktivní případ koronaviru, bez výjimky šlo o malé obce, v nichž dohromady žije jen něco přes dvě procenta obyvatel ČR. Absence pozitivně testovaných navíc neznamená, že se v nich nákaza nevyskytuje.  

<div id="datarozhlas-covid-obce-tabulka"></div>
<script src="https://data.irozhlas.cz/covid-obce/build/tabulka.js"></script>