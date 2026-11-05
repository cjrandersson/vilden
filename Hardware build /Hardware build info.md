Att bygga en "Frankenstein-rigg" för lokal AI är en av de roligaste grenarna inom hårdvaruhacking. Eftersom lokala språkmodeller ställer helt andra krav än traditionellt spelande (där man vill ha extrem 3D-fps på ett enda monsterkort) kan man komma undan med ganska vilda kombinationer av äldre och nyare delar.  
Här är en genomgång av hur andra brukar bygga, de gyllene reglerna, dolda fallgropar och var du hittar bästa nördkunskapen.

### **1\. Hur ser andra Frankenstein-byggen ut? (Visuell anatomi)**

Om du kikar in i communityn för hemmasnickrade AI-server/arbetsstationer brukar man i regel se tre stilar:

* **"Open-Air Test Bench" (Öppna mekbord):** Många skippar vanliga chassin helt och bygger ställningar i aluminiumprofiler eller trä. Eftersom flertaliga grafikkort drar enormt mycket värme och ofta inte passar i standardchassin ger detta maximalt luftflöde och enkel åtkomst till kablar.  
* **Det fullsmäckade Workstation-chassit:** Ett stort, ljuddämpat mid- eller fulltower (precis som ditt Antec-chassi) där den nedre hårddiskburen har monterats bort för att ge plats åt ett långt sekundärt grafikkort, ibland med modifierade fläktar eller externa fläktkontroller.  
* **Server-chassi i rack (4U):** Vissa bygger om gamla Dell- eller HP-serverlådor för att få plats med breda gamingkort och kraftiga nätaggregat.

### **2\. De gyllene reglerna för multi-GPU / Blandad hårdvara**

> 1. **VRAM är den enda valutan som räknas** När det gäller LLM:er spelar det ingen roll om det ena kortet är ett sprillans nytt RTX-kort och det andra är ett äldre GTX-kort. Det som avgör vilken modell du kan köra är den **sammanlagda mängden VRAM**. Modellen bryr sig inte om estetik eller arkitekturmix – så länge båda stöder CUDA (NVIDIA) delar de på bördan.  
> 2. **Inferens är inte träning (Bandbredden är sällan en flaskhals)** Många tror att man behöver ddyra PCIe-bryggor (som gamla SLI-bryggor) eller blixtsnabba x16-platser för båda korten. För *inferens* (när modellen svarar på dina prompter) läses modellvikterna in en gång i VRAM och stannar där. Att korten sitter i olika hastigheter (t.ex. ett i x16 och ett i x4) märks knappt av, förutom att det tar några sekunder extra att ladda modellen i början.  
> 3. **Modellens kvantisering måste passa den svagaste länken** Eftersom minnet delas upp i lager över dina kort (t.ex. 24 lager på 3060 och 12 lager på GTX 980\) måste alla inblandade kort stödja de instruktioner som llama.cpp / LM Studio skickar ut. Håll dig till samma tillverkare (NVIDIA över hela brädet) så slipper du drivrutinskrockar.

### **3\. Det som är viktigt mer än det uppenbara (Dolda fallgropar)**

* **"Blower-fläktar" vs öppna kylare:** Ditt GTX 980 på bilden är av referenstyp med en så kallad *blower-fläkt* (turbinfläkt som blåser ut luften på baksidan av chassit). I en trång Frankenstein-rigg med två kort dikt an mot varandra är faktisk blower-kort *bättre* som det undre kortet, eftersom de inte kapslar in varmluften på samma sätt som öppna fläktar som bara rör runt luften internt. Nackdelen är att de låter som jetplan när de pressas.  
* **Aggregatets 12V-linor (Rails) och "Daisy-Chain":** När du kör flera strömkrävande kort samtidigt, koppla **aldrig** båda strömkablarna från en och samma sladd från nätaggregat (så kallad daisy-chain där en kabel delar sig i två kontakter). Använd alltid två helt separata kablar från nätaggregatet till det kraftfullare kortet för att undvika spänningsfall och att säkringar löser ut.  
* **PCIe-strömförsörjning via moderkortet:** Ett standardmoderkort kan skicka upp till 75W genom själva PCIe-porten. När du trycker in flera tunga grafikkort drar de mycket ström direkt ur moderkortets platser. Se till att moderkorts-extra strömkontakter (om sådana finns, t.ex. en extra 4-pin/6-pin på äldre enthusiast-kort) är inkopplade.

### **4\. Var vill du lära dig mer? (Rekommenderade resurser)**

Om du vill grotta ner dig i hur communityn bygger sina lokala AI-riggar och optimerar mjukvaran finns det tre självklara stopp:

* **Reddit – r/LocalLLaMA:** Den absolut bästa platsen på internet för det här ämnet. Sök på *"multi-gpu Frankenstein"* eller *"mixed VRAM setup"* så hittar you trådar där folk delar med sig av sina udda hårdvarukombinationer, mätvärden (tokens/s) och lösningar på vanliga problem.  
* **GitHub – ggerganov/llama.cpp:** Under huven är det detta bibliotek som driver nästan all lokal AI (inklusive LM Studio). Deras dokumentation kring \--tensor-split och hur man fördelar lager mellan olika GPU:er är ovärderlig när man vill förstå exakt hur hårdvaran kommunicerar.  
* **LM Studio Developer Documentation:** Har utmärkta, pedagogiska guider för hur man sätter upp hårdvaruacceleration och felsöker när en modell vägrar ladda över flera enheter.
