# BESKRIVNING TOPOLOGI (FYSISK)
## GÄVLE (HK)

### Internet / ISP (Cloud)

Funktion: Representerar det externa Internet och företagets internetleverantör.\
Syfte i Topologin:
- Ger Gävle (HK) tillgång till Internet
- Extern åtkomst till Webserver
- Används för Kommunikation mellan Gävle och Falun (WAN/VPN)

(Ligger utanför företagets nät och kontrolleras inte av AURORA SENSORS AB)

## Edge-router | HK-EDGE-RTR

Funktion: Företagets router mot Internet
- routing mellan Gävle(HK)s interna nät och Internet
- WAN-Kommunikation med Falun 
- Trafik vidare till Brandvägg.

Routern är den första aktiva enheten som företaget kontrollerar själva.

## Brandvägg | HK-FW

Funktion: Skyddar hela Gävle (HK)s nätverk.\
- filtrering av trafik - in och ut,
- uppdelning av nätet i säkerhetszoner (Outside, Inside, DMZ)

Behövs för att:
- Skyddar interna servrar och klienter
- Tillåter endast kontrollerad trafik till webbservern
- Förhindrar att en komprometterad webbserver når det interna nätet.

## Core-switch | HK-CORE-SW

Funktion: Det centrala navet i Gävle (HK)s interna nätverk.\
Ansvarar för:
- All trafik samlar från:
  - Servernät
  - Kontorsnät
  - Konferens/WiFi
- Vidarebefodrar trafik mot brandvägg

Den behövs för att ge hög kapacitet, central och strukturerad trafikhantering och en tydlig hierarkisk nätverksdesign.

## Server-switch | HK-SRV-SW

Funktion: Dedikerad swtich för interna servrar.

Ansvarar för:
- Koppla samman alla interna servrar i Gävle HK.
- Isolera servertrafik från användartrafik.

Det ger bättre översikt, ökad stabilitet och en mer realistisk servermiljö.

## Interna servrar i Gävle HK.
- HK-DHCP-SRV 
  - Delar automatisk ut IP-addresser till, anställdas datorer, servrar och trådlösa klienter
- HK-FILE-SRV | Central filserver
  - Delade dokument, projektfiler, administrativ data
- HK-SYSLOG-SRV | Logghantering
  - Tar loggar ifrån routrar, switchar, brandvägg
  - Ger säkerhetsanalys, felsökning, övervakning
- HK-BACKUP-SRV | Backup-server
  - Säkerhetskopiering av datainsamling från Falun (FE)
  - Skydd mot dataförlust

## DMZ-switch | HK-DMZ-SW

Switch för DMZ-zonen\
Ansvarar för:
- Separat nät för externa tjänster
- Endast ansluten till brandväggens DMZ-port
- Håller externa servrar isolerade från det interna nätverket

## Webbserver | HK-WEB-SRV

Funktion: Extern webbserver

Används för:
- Företagsinformation
- Projektpresentationer
- Offentlig data till kunder

## Access-switchar | HK-ACC-SW1 & HK-ACC-SW2
Funktion: Kopplar samman användarnas datorer.

Ansvarar för:
- Arbetsstationer för alla anställda
- Trafik vidare till core-switchen

Två stycken ACC för lastfördelning, skalbarhet, bättre struktur.

## PC | HK-PC01 - HK-PC012
Arbetsstationer för:
- VD
- Administration
- Produktion
- Utveckling
- IT-Personal

## Acces-Point | HK-AP1
Funktion: Trådlöst nätverk i konferens och kontorsmiljö.

- Möten
- Bärbara datorer
- Gäster vid konferenser

# Sammanfattning
Gävle HK är uppbyggt med tydlig separation mellan edge, core, server-, DMZ- och access-lager. Designen ger god säkerhet, hög tillgänglighet och enkel administration, samtidigt som den stödjer företagets roll som huvudkontor och central IT-drift för hela organisationen.
