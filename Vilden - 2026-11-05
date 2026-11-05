## VILDEN // PROJEKTKONTEXT & HANDLINGSPLAN

**Status:** Pausad / Väntar på hårdvaruleverans (2–3 veckor)

**Skapad:** 2026-11-05

## 01 / PROJEKTETS VISIONS- OCH KARAKTÄRSKÄRNA

* **Namn:** Vilden (Local Creative Intelligence).

* **Syfte:** En lokal, självständig kreativ medskapare inom gränslandet mellan design, ljud/musikteknik och creative coding (JS/TS, Node for Max, Web Audio API, p5.js, Three.js).

* **Personlighet:** Eget omdöme, konstruktivt utmanande (inte en ja-sägare), nyfiken, estetiskt och tekniskt kompromisslös.

* **Arbetsprincip:** Utforska fritt → granska kritiskt → testa konkret → behåll det som håller.

* **Arkitekturprincip:** Helt lokal körning (LM Studio / Ollama API). Vikter, personlighet och projektminne hålls isär. Språkmodellen ligger aldrig i den realtidskritiska ljudloopen utan styr/parameteriserar via JSON.

## 02 / BEKRÄFTAD HÅRDVARA & MILJÖ

* **Huvuddator (Stationär - Hämta inom 2–3 veckor):**

  * AMD Ryzen-processor med bra kylning.

  * 16 GB DDR4 RAM.

  * Chassi (Antec) med Noctua-kylare & Corsair CX750M (750W) PSU.

  * Flera SSD-enheter (\~400 GB st) + SATA-diskar.

* **Grafikkort setup (Frankenstein Multi-GPU):**

  1. **Primärt:** ASUS TUF Gaming GeForce RTX 3060 (8 GB VRAM).

  2. **Sekundärt:** NVIDIA GeForce GTX 980 (4 GB VRAM, Blower-fläkt).

  * *Totalt tillgängligt VRAM:* **12 GB** uppdelat över 2 kort för LLM-lageravlastning.

* **Övrigt i reserv:** ASUS ROG Maximus VII Hero (Z97), Intel i7/i5 (DDR3), GTX 700-kort (ligger på hyllan tills vidare).

## 03 / SAMMANFATTNING AV VÅRA DISKUSSIONER & BESLUT

1. **Multi-GPU Strategi:**

   Vi utnyttjar båda korten via LM Studio (`llama.cpp`-lageruppdelning). RTX 3060 tar merparten av lagren, GTX 980 avlastar sista 30% så vi får plats med 9B–12B-modeller i snabbt VRAM.

2. **Arkitektur- & Kodsäkring (Node for Max / Tools):**

   * Använd **Zod-scheman** i JS/TS-bryggan för att validera Vildens JSON-output innan den når Max/MSP.

   * Bygg en **Node.js Mock-miljö** för att testa logik offline innan körning i faktiska Max-patchar.

   * Sätt upp en lokal **MCP-server eller kontextinjektor** för att ladda `vision.md`, `principer.md` etc. i Vildens systemprompt utan manuell copy-paste.

3. **Inköp & Bevakningsstrategi:**

   * Vi har upprättat schemalagda sökningar och prompter för att hålla utkik på SweClockers marknad, Tradera och Blocket efter billig begagnad hårdvara (t.ex. Tesla P40, RTX 2080 Ti, X99-plattformar, kraftiga nätaggregat).

## 04 / FAS A: NÄSTA STEG NÄR DATORN ÄR PÅ PLATS

När datorn är hemma och skruvad drar vi i gång följande sekvens:

* \[ \] **Steg 1: Montering & Hårdvarukontroll**

  * Installera Ryzen-moderkortet i chassit.

  * Montera RTX 3060 (slot 1) och GTX 980 (slot 2).

  * Verifiera att Corsair CX750M kör separata PCIe 8-pin/6-pin-kablar till varje kort (ingen daisy-chaining på 3060-kortet).

  * Konfigurera SSD-enheter (System-SSD + Dedikerad AI-modell-SSD).

* \[ \] **Steg 2: Drivrutiner & Mjukvara**

  * Installera Windows/Linux + senaste NVIDIA Unified Drivers.

  * Verifiera båda korten i Enhetshanteraren/NVIDIA Control Panel.

  * Installera LM Studio.

* \[ \] **Steg 3: Modell-Audition (T01–T07)**

  * Konfigurera multi-GPU GPU Offload i LM Studio.

  * Ladda ned och kör testerna i specifikationen:

    1. *Qwen 3.5 4B* (Baslinje, extremt snabb)

    2. *Qwen 3.5 4B Heretic* (Jämförelse av vägransbeteende)

    3. *Qwen 3.5 9B* (Huvudkandidat, kräver Multi-GPU för full fart)

    4. *Gemma 3 12B* (Om minnet medger)

* \[ \] **Steg 4: Implementera Vildens Kärna & Systemprompt**

  * Skriva Vildens karaktärskontrakt utifrån specen.

  * Bygga det lokala Markdown-projektminnet.

## 05 / INSTRUKTION FÖR ÅTERSTART AV SESSION

*Klistra in eller referera till denna fil när du återvänder till chatten om 2–3 veckor med meddelandet:*

> *"Nu är Ryzen-burken och korten på plats! Läs in `vilden_project_context.md` och låt oss börja med Steg 1 i Fas A."*
