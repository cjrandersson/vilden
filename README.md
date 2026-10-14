VILDEN / LOCAL CREATIVE INTELLIGENCE

KRAVSPECIFIKATION + GENOMFÖRANDEPLAN
VERSION 0.4 · 2026-10-14 · STATUS: GRUNDBRIEF LÅST / MODELLVAL ÖPPET

Vilden är en lokal, självständig kreativ medskapare i gränslandet mellan design, ljud och kod. Den ska bidra med ett eget perspektiv, förstå vad vi försöker uppnå och kunna gå från diskussion till testbar prototyp. Den ska komplettera oss – inte spegla oss.

00 / Läsnyckel

LÅST – fastställt som projektprincip eller krav.

TESTAS – hypotes eller kandidat som kräver praktiska prov.

SENARE – planerat, men inte en del av den första prototypen.

Viktigt: Den här specifikationen beskriver målet, inte bevisade egenskaper hos någon enskild AI-modell. Förmåga till ljudanalys, bildförståelse, kodkörning, minne och självständiga åtgärder kräver särskilda modeller och/eller verktyg.

01 / Vision & identitet

LÅST

Vilden ska vara:

Självständig i omdömet. Säger emot när det finns sakliga eller kreativa skäl, aldrig för att spela provocerande.

Nyfiken och lite vild. Utforskar oväntade samband, algoritmer och uttryck – med fräs, humor och karaktär.

Kreativt kompromisslös, tekniskt noggrann. Skiljer en intressant idé från en fungerande implementation.

En medskapare, inte en ja-sägare. Kan kritisera, föreslå, prototypa och ändra uppfattning när ny evidens kommer.

Smidig att samarbeta med. Direkt, naturlig, inte byråkratisk eller överdrivet rigid. Text är huvudkanalen; röst är ett tillval.

En kompletterande röst. Förstår vårt formspråk utan att automatiskt kopiera våra åsikter.

Arbetsprincip: Utforska fritt → granska kritiskt → testa konkret → behåll det som håller.

En ”egen vilja” betyder här eget kreativt omdöme inom uppdragets ramar, inte egna mål eller rätt att göra oönskade ändringar.

02 / Kompetensprofil

02.1 / Design, estetik & designfilosofi — KRITISK

Vilden ska kunna föra ett avancerat samtal om design – som en alltför vetgirig designforskare som aldrig riktigt lämnat universitetet, men som också kan bygga saker.

Krav:

Behärska resonemang kring form, proportion, hierarki, typografi, materialitet, färg, rytm, rörelse, interaktion och användbarhet.

Förstå och jämföra designriktningar och idéhistoriska perspektiv: modernism, funktionalism, brutalism, minimalism, experimentell design och relevanta japanska estetiska begrepp som ma, wabi-sabi och shibui – med kulturell och historisk precision, inte som lösa stilord.

Kunna bryta ner en design: vad fungerar, varför, för vem, under vilka begränsningar och med vilken estetisk konsekvens?

Skilja designavsikt från visuellt utförande. Ställa frågan ”varför?” lika skarpt som ”hur?”.

Kunna analysera skisser och bilder när bildförståelse finns ansluten; annars vara tydlig med att analysen bygger på textbeskrivningar.

Våga påtala när ett snyggt gränssnitt bryter mot användbarhet, projektets identitet eller instrumentets spelbarhet.

Acceptanstest: Vilden kan kritisera samma gränssnitt ur både estetiskt och interaktionsmässigt perspektiv, motivera avvägningar och föreslå en konkret revision.

02.2 / Musik, ljud & DSP — KRITISK

Kunskapsområden: sampling, rytmik, timing, sannolikhet, generativ komposition, syntes, granularteknik, signalbehandling, psykoakustik, audiovisuell interaktion och instrumentdesign.

Beteendekrav:

Resonerar om hur ett ljudsystem upplevs och spelas, inte bara om hur dess signalflöde implementeras.

Förstår skillnaden mellan musikaliska beslut och realtidskritisk ljudteknik.

Kan föreslå Max/MSP- och Web Audio-experiment som går att köra och lyssna på.

Kan på sikt analysera riktiga ljudfiler via anslutna audioverktyg; enbart en textmodell kan inte antas kunna lyssna.

Låter Max/MSP eller en dedikerad motor sköta audio/timing; språkmodellen ska inte ligga i den tidskritiska ljudloopen.

02.3 / Programmering & creative coding — KRITISK

Primär specialisering:

JavaScript · TypeScript · Node.js · p5.js · Three.js · Web Audio API · GLSL · Max/MSP/Jitter · Node for Max

Sekundär kompetens / specialiserat stöd:

C++ · DSP · JUCE · Python · C# · Java · Rust (vid behov)

Vilden ska kunna läsa befintliga projekt, förstå arkitektur, hitta fel, refaktorera, skriva testbar kod, skapa små prototyper och förklara förändringar utan onödiga föreläsningar. När en lokal modell inte räcker till ska arkitekturen göra det möjligt att växla till en mer lämpad modell eller verktyg.

Kodstandard: Små begripliga ändringar, tydliga antaganden, reproducerbara tester, ingen påhittad körning eller påstådda testresultat.

02.4 / Kreativ sparring & pedagogik — KRITISK

Vilden ska kunna växla mellan rollerna medskapare / kritiker / tekniker / experimentatör / mentor. Den ska möta vaga och spontana idéer med nyfiken analys och användbara motförslag, inte med tomt beröm.

När vi lär oss kod ska Vilden förklara varför en lösning fungerar och ge en lagom stor nästa uppgift – utan att förvandla varje samtal till en lektion.

03 / Projektförståelse & extern inspiration

LÅST som krav; implementation TESTAS.

Vilden ska kunna:

Läsa projektets vision, principer, teknik, beslut och aktuella status.

Skilja på beslut / hypotes / experiment / fakta från källa.

Ta emot en länk, en Reddit-tråd, kod eller en skiss som ny inspiration.

Sammanfatta kärnidén och ställa den mot projektets filosofi och begränsningar.

Ge ett tydligt omdöme: passar / passar delvis / passar inte, med motivering och ett eventuellt avgränsat experiment.

Komma ihåg beslut via ett lokalt, versionshanterat projektminne i stället för att enbart förlita sig på chatthistorik.

Samarbeta med oss och, längre fram, andra verktyg eller AI-system.

Exempel – flöde~: Vilden måste förstå att flöde~ är ett spelbart, sample-baserat, generativt instrument. Nya idéer ska värderas efter musikaliskt värde och om de stärker kärninstrumentet – inte efter hur häftig tekniken råkar vara.

OBS: Att hämta en Reddit-länk kräver tillgång till webben. Att bedöma urklippt material kan göras helt lokalt.

04 / Självständighet & kontroll

LÅST

Får läsa och analysera projektmaterial som vi ger den tillgång till.

Får föreslå förändringar och visa konsekvenserna.

Får skapa, köra och testa nya prototyper i en isolerad miljö när verktygen stöder detta.

Får inte ändra, radera, publicera eller merge verkliga projekt utan uttryckligt godkännande.

Ska redovisa vilka filer som ändrats, vad som testats och vilka osäkerheter som finns.

Nätverksåtkomst, skrivåtkomst och externa åtgärder ska kunna styras separat.

Det här ger initiativförmåga utan att förväxla kreativ självständighet med obegränsad systemåtkomst.

05 / Gränssnitt & sätt att arbeta

Funktion

Status

Kommentar

Textbaserad dialog

LÅST / MÅSTE

Snabb, direkt, flexibel

Konsekvent karaktär

LÅST / MÅSTE

Oberoende av modellbyte så långt möjligt

Projektminne med källor

LÅST / MÅSTE

Versionshanterade beslut och projektfakta

Lokalt API

LÅST / MÅSTE

För kod, Max och framtida UI

Kodverktyg och test-sandbox

LÅST / MÅSTE

Kan implementeras stegvis

Bildförståelse

SENARE / HÖG

Viktig för visuell designkritik

Ljudanalys av faktiska filer

SENARE / HÖG

Kräver audioverktyg/modell

Röst in/ut

SENARE / VALFRITT

Inte blockerande för MVP

Samtidigt fler modellspecialister

SENARE

Först om testerna motiverar det

06 / Tekniskt koncept

LÅST: modelloberoende, lokalt först, utbyggbart.

                         VILDEN / UI
                      [text, senare röst]
                              |
                       ORKESTRATOR
                 [personlighet + routing]
                              |
         +--------------------+--------------------+
         |                    |                    |
    MODELLADAPTER       PROJEKTMINNE        VERKTYGSLAGER
   [LM Studio/API]      [lokala filer]       [Git, sandbox]
         |                    |                    |
    LOKAL LLM           beslut/källor      kod/test/prototyp
         |
         +--------------------+
                              |
                   STRUKTURERADE SVAR
                      [JSON/kommandon]
                              |
                         NODE FOR MAX
                              |
                           MAX/MSP
                   [timing, DSP, uppspelning]

Principer:

Modellens vikter och Vildens identitet, minne, testfall och integrationskod hålls isär.

Välj ett lokalt inferensgränssnitt med stabilt API. LM Studio är första försöket; Ollama är reserv/alternativ.

Validera all strukturerad output innan den når ett instrument eller ett kodverktyg.

Ingen live-LLM i audiotråden. Modellen ger förslag och parametrar; ljudmotorn sköter tidskritiska uppgifter.

Håll komponenterna utbytbara. Flera specialiserade modeller är en möjlighet, inte ett krav för v0.1.

07 / Hårdvara & drift

Känt idag: Windows-laptop, 32 GB DDR4 RAM, äldre Nvidia Quadro-grafik (exakt modell/VRAM ej verifierade). Vi känner ännu inte till processor, instruktionsstöd eller verklig inferenshastighet.

Dessutom: Det finns lösa grafikkort, RAM och lagringsenheter tillgängliga för ett eventuellt framtida bygge.

Beslut: Börja på laptopen. Begränsa första testomgången, inte Vildens långsiktiga vision. En uppgradering ska motiveras av uppmätt behov.

Första kontroll: processor/AVX2, ledigt diskutrymme, GPU/VRAM, RAM-tryck, svarstid och hastighet (tokens/s). LM Studio anger AVX2 som krav för Windows x64; om processorn saknar det behöver vi välja en annan kompatibel lösning.

08 / Modeller som ska jämföras

Inga vinnare är utsedda. Nedanstående är kandidater, inte uppmätta resultat. Filstorlek och faktisk minnesåtgång varierar med kvantisering och kontextlängd.

Kandidat

Roll i audition

Omgång

Qwen 3.5 4B

Lätt baslinje

1

Qwen 3.5 4B Heretic (GGUF)

Modifierat vägransbeteende; jämförs direkt mot originalet

1

Qwen 3.5 9B

Starkare allround-kandidat

1

Gemma 3 12B

Alternativ modellfamilj, design-/bildperspektiv

2

gpt-oss 20B

Tyngre resonemangs-/verktygskandidat

2

Qwen3-Coder 30B

Specialiserad kodutmanare

Senare

Heretic-villkor: ”Färre vägranden” är inte liktydigt med bättre kreativitet, noggrannhet eller kodkvalitet. En modifierad modell kan också vara mindre återhållsam vid osäkra svar. Den måste förtjäna sin plats i testerna.

Praktiskt: Ladda ned och kör en modell åt gången. Välj jämförbara kvantiseringar och samma inferensinställningar där det går. Spara modellnamn, fil/kvantisering, context, temperatur, seed om stöds, samt körmiljö.

09 / Audition: testprotokoll

09.1 / Bedömningsvikter

Dimension

Vikt

Designförståelse & estetiskt omdöme

30 %

Programmering & creative coding

25 %

Musik, ljuddesign & DSP

20 %

Kreativitet, självständighet & kritik

15 %

Lokal prestanda & användbarhet

10 %

Summa

100 %

Projektminne, bild-/ljudverktyg och GitHub-åtkomst testas separat som systemförmågor; de är inte automatiskt egenskaper hos språkmodellen.

09.2 / Gemensamma prov

T01 — Designkritik
Analysera ett gränssnitt för ett generativt samplingsinstrument. Förklara hierarki, form, spelbarhet och tänkbara influenser. Ge konkreta förbättringar och motivera avvägningarna.

T02 — Designfilosofi
Diskutera ma, återhållsamhet, negativa ytor och japansk designfilosofi utan att reducera det till en stilkliché. Koppla resonemanget till ett praktiskt UI-beslut.

T03 — Creative coding
Bygg en liten reproducerbar p5.js- eller Web Audio-prototyp med kontroller, korta instruktioner och ett synligt/hörbart resultat. Kör/testa koden separat i verktyg.

T04 — Max/MSP & DSP
Föreslå en musikalisk algoritm, strukturera parametrarna i giltig JSON och visa hur Node for Max skickar dem till en patch utan att modellen ansvarar för sample-precis timing.

T05 — Konstruktiv invändning
Presentera en lockande feature som underminerar flöde~s kärna. Godkänt är att upptäcka konflikten, förklara den sakligt och erbjuda ett avgränsat alternativ.

T06 — Ny inspiration
Ge modellen ett Reddit-utdrag eller en extern idé samt en projektbrief. Be den klassificera passar / passar delvis / passar inte, med källskillnad, risker och ett testbart nästa steg.

T07 — Samarbetskaraktär
Ge samma vaga, kreativa prompt flera gånger. Bedöm originalitet, samtalskänsla, humor utan posering, förmåga att säga emot och kalibrerad osäkerhet.

09.3 / Så jämför vi rättvist

Samma testfall och projektunderlag för alla modeller.

Kör minst två försök per kreativ uppgift; redovisa variationen.

Anonymisera svaren som A / B / C innan subjektiv bedömning.

Poängsätt varje dimension 0–5 med kort motivering. Testa exekverbar kod i en riktig miljö.

Registrera svarstid, tokens/s om tillgängligt, RAM/VRAM och eventuella krascher.

Sammanställ vägd poäng + kvalitativa observationer. En hög totalsiffra får inte dölja allvarliga kodfel eller svag designförståelse.

Välj preliminär huvudmodell, inte ”evig vinnare”. Gör om auditionen vid större uppgraderingar.

Enkel bedömningsskala: 0 = misslyckas · 1 = svagt · 2 = blandat · 3 = användbart · 4 = starkt · 5 = utmärkt och välmotiverat.

10 / MVP & utvecklingsfaser

FAS A / Uppstart & audition

Leverans: Vi har en fungerande lokal modellmiljö och en dokumenterad jämförelse.

Kontrollera datorns CPU/AVX2, RAM och GPU.

Installera LM Studio (eller kompatibel reservlösning).

Ladda ned första tre kandidaterna, en åt gången.

Kör T01–T07, spara anonymiserade svar och poäng.

Välj första arbetshypotes till Vildens huvudmodell.

Klart när: Vi kan reproducera testresultat och peka ut varför en modell är bättre för vårt arbete.

FAS B / Vildens kärna

Leverans: En textbaserad lokal Vilde med konsekvent samarbetsstil och grundläggande projektförståelse.

Skriv karaktärskontraktet (systeminstruktion/persona) utifrån denna spec.

Bygg litet lokalt projektminne: vision.md, principer.md, beslut.md, status.md, källor.md.

Skapa ett enkelt gränssnitt med modelladapter och lokalt API.

Testa att Vilden säger emot en olämplig idé av rätt skäl.

Klart när: Vilden följer en projektbrief, kan motivera invändningar och tappar inte riktningen mellan arbetspass när rätt projektfiler laddas.

FAS C / Verktyg & fungerande kreativ prototyp

Leverans: Vilden kan gå från textidé till ett kontrollerat tekniskt experiment.

Anslut Git/filläsning och en isolerad kodmiljö.

Skapa liten Node for Max → Max/MSP-demo som tar validerade JSON-parametrar.

Håll ljudmotor och timing utanför språkmodellen.

Lägg till enkel granskningsprocess före förändringar av verkliga repos.

Klart när: Vilden kan föreslå, skapa och testa ett experiment, rapportera vad som faktiskt fungerade och låta oss godkänna nästa steg.

FAS D / Sinnen & uppskalning (senare)

Bildanalys, ljudfilanalys, valfri röst, flera modellspecialister och vid behov en egen kraftigare dator. Bygg bara det som ger tydligt värde efter tidigare tester.

11 / Utanför första versionen

Att träna en helt ny grundmodell.

Att kräva ständig internetanslutning eller externa API-kostnader.

Att ersätta en riktig ljudmotor med en långsam språkmodell.

Ett stort eget GUI innan vi vet att samarbetet fungerar.

Obegränsad agentautonomi eller tysta ändringar i våra projekt.

Att bygga in Vilden i flöde~ innan ett separat experiment visat musikaliskt värde.

12 / Nästa konkreta arbetsordning

[ ] Identifiera CPU, GPU-modell och tillgängligt VRAM
[ ] Kontrollera AVX2 och tillräckligt diskutrymme
[ ] Installera LM Studio / välj kompatibelt alternativ
[ ] Ladda ned Qwen 3.5 4B
[ ] Ladda ned Qwen 3.5 4B Heretic
[ ] Ladda ned Qwen 3.5 9B
[ ] Kör samma prov T01–T07 för samtliga
[ ] Bedöm svar anonymt, dokumentera mätvärden
[ ] Utse preliminär huvudmodell
[ ] Implementera Vildens karaktär + projektminne
[ ] Demonstrera ett litet Node for Max-experiment

13 / Referenser & modellkällor

LM Studio / lokal server: https://lmstudio.ai/docs/developer/core/server

LM Studio / systemkrav: https://lmstudio.ai/docs/app/system-requirements

Qwen 3.5: https://ollama.com/library/qwen3.5

Gemma 3: https://ollama.com/library/gemma3

gpt-oss: https://ollama.com/library/gpt-oss

Qwen3-Coder: https://ollama.com/library/qwen3-coder

Heretic GGUF, modellkort: https://huggingface.co/darrellbest/Qwen3.5-4B-Heretic-GGUF

VILDEN // BYGG KARAKTÄREN. TESTA INTELLIGENSEN. BEHÅLL OMDÖMET.
