# AURORA-2026  
## Nätverkssäkerhet och Systemadministration – GDT34Z LP3 2026

Detta repository innehåller dokumentation och nätverksdesign för projektet **AURORA-2026**, ett examinerande projekt inom kursen **Nätverkssäkerhet och Systemadministration (GDT34Z)** vid **AURORA SENSORS AB**.

Projektet bygger på ett realistiskt industriscenario och omfattar design, implementation, testning och dokumentation av en **säker, skalbar och verksamhetsanpassad IT- och nätverksinfrastruktur** för ett fiktivt företag med verksamhet på två geografiskt åtskilda orter.

---

## 🏢 Företagspresentation

**AURORA SENSORS AB** är ett svenskt teknikföretag som utvecklar och tillverkar robusta IoT-sensorer för användning i skogs- och naturmiljöer. Företagets kunder återfinns inom:

- Skogsindustri  
- Miljöforskning  
- Energibranschen  
- Offentliga aktörer  

Företaget bedriver verksamhet på två huvudsakliga orter:

- **Gävle (HK)** – Huvudkontor och produktionsenhet  
- **Falun (FE)** – Forsknings- och dataanalysenhet  

All forskning bedrivs på uppdragsbasis, där externa kunder beställer mätkampanjer och analyser baserade på data som samlas in via företagets egenutvecklade sensorer.

---

## 🎯 Projektets syfte

Syftet med projektet är att, ur ett studentperspektiv, ta fram en **helhetslösning för företagets IT- och nätverksinfrastruktur** som uppfyller höga krav på:

- Tillgänglighet  
- Integritet  
- Konfidentialitet  

Projektet ska resultera i en lösning som är:

- Säker  
- Skalbar  
- Kostnadseffektiv  
- Byggd på realistiska tekniska val  

---

## 🏭 Verksamhetsbeskrivning

### Gävle – Huvudkontor och tillverkning (HK)

Huvudkontoret i Gävle ansvarar för:

- Tillverkning och kvalitetssäkring av IoT-sensorer  
- Företagsledning och administration  
- Central IT-drift och IT-tjänster  
- Kundkontakt kopplad till försäljning och leverans  

**Personal:** 12 personer  
Alla anställda har egna arbetsstationer. Lokalerna innehåller även konferensrum samt ett mindre serverrum.

**Servrar i Gävle:**
- DHCP-server  
- Central filserver  
- SYSLOG-/övervakningsserver  
- Backup-server för Faluns datainsamlingsdata  
- Extern webbserver (placerad i DMZ)  

---

### Falun – Forsknings- och analysenhet (FE)

Forskningsenheten i Falun ansvarar för:

- Mottagning av mätdata från sensorer i skogsmiljö  
- Lagring och analys av stora datamängder  
- Rapportering till uppdragsgivare  
- Test och validering av nya sensorgenerationer  

**Personal:** 10 personer  
All personal har egna datorer. Lokalerna inkluderar:

- Analysrum med kraftfulla arbetsstationer  
- Separat nät för test av nya sensorer  
- Trådlöst nätverk för både personal och gästforskare  

**Servrar i Falun:**
- DHCP-server  
- Datainsamlingsserver (IoT-backend)  
- Analys- och databasserver  

---

## 🌲 IoT- och dataflöden (övergripande)

- Sensorer placeras i skogsmiljöer i Falu-regionen  
- Sensorerna skickar mätdata via privata WiFi-nät  
- All kommunikation är krypterad och autentiserad  
- Data tas emot i Falun, lagras och analyseras  
- Resultat och rapporter levereras via säkra tjänster  
- Gävle ansvarar för drift, uppdateringar och övervakning av sensorerna  

---

## 🧱 Projektets omfattning

Projektet omfattar bland annat:

- Site-to-site VPN mellan Gävle och Falun  
- Säker intern kommunikation (trådbundet och WiFi)  
- Säker IoT-kommunikation mellan sensorer och Falun  
- Segmentering av nät baserat på roller och funktion  
- Skydd av känsliga forskningsdata  
- Säker administration av nät, servrar och klienter  
- Loggning, övervakning och spårbarhet  

Lösningen ska bygga på befintlig utrustning där så är möjligt.

---

## 🧪 Dokumentation och testning

Projektet ska dokumenteras i form av en teknisk rapport som:

- Är pedagogiskt utformad och begriplig även för icke-tekniker  
- Är strukturerad enligt tekniskt-vetenskaplig standard  
- Innehåller tydliga problemformuleringar och åtgärdsplaner  
- Redovisar implementering med kodexempel  
- Innehåller verifiering och testning enligt **User Story-metoden**  

Rapporten avslutas med **framtida rekommendationer** baserade på CIA-triangeln.

---

## 📦 Innehåll i detta repository

Detta repository innehåller:

- Nätverksdesign och topologier  
- Dokumentation av fysisk och logisk nätverksstruktur  
- Projektbeskrivning och tekniska resonemang  
- Underlag för rapport och praktisk demonstration  

---

## 📚 Kursinformation

- **Kurs:** GDT34Z – Nätverkssäkerhet och Systemadministration   
- **Projekt:** AURORA-2026  
- **Lärosäte:** Högskolan Dalarna  

---

*Projektet är framtaget i utbildningssyfte och baseras på ett fiktivt företag.*
