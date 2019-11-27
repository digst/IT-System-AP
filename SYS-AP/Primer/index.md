<style>
@media print {
  html { margin: 0cm 2cm 2cm 0cm; font-size: 80%; }
  /* DIGST fonts */
  body { font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;}
  h2,h3,h4, h4 dfn { font-family: "Garamond", serif; color: black; margin-bottom: 0; font-style: normal; font-weight: normal;}
  h2:not(#subtitle) { page-break-before: always; font-size: 250%; border-bottom: solid 0.5px black; padding-top: 20px; margin-bottom: 6px;}
  h3 { font-size: 145%;}
  h4 { font-size: 125%;}
  #toc {page-break-before: always;}
  /* DIGST-like frontpage */
  .head { width: 50%; margin-left: 24px; padding: 0px; background-color: #031D5C;}
  .head div { background-color: white; padding: 24px; }
  .head hr { display: none;}
  .head h1 { background-color: #031D5C; color: white; margin: 0px; padding: 50px 0px 50px 24px; font-weight: normal; }
  #subtitle { padding-left: 24px; background-color: #031D5C; color: #031D5C; }
  .head time { display: block; font-family: "Helvetica Neue", Helvetica, Arial; margin: 0px; background-color: #031D5C; font-size: 80%; color: white;}
  .toc li { line-height: 70%; font-family: "Helvetica Neue", Helvetica, Arial;
    font-weight: 600; font-size: 90%; }
  .self-link { display: none; }
  blockquote { font-size: 80%; font-style: italic; margin-left: 5%; width: 70%; border-left-width: 2px;}
	h2#abstract {display: none;}
	.p-summary {width: 50%; margin-left: 24px; padding: 0px;}
}
.new {
    border: solid 3px green;
    padding: 6px;
    margin: 18px 0px 18px 0px;
}
/* style til egne og andres definitioner rød/blå*/
</style>
<pre class="metadata">
Title: arkitektur.digst.dk Standard for beskrivelse af it-systemer (basisprofil)
Status: LD
URL: http://github.com/digst/IT-System-AP/SYS-AP/Primer/index.md
Editor: Digitaliseringsstyrelsen http://arkitektur.digst.dk

Abstract: 
Boilerplate: copyright no, conformance no, abstract no
Shortname: sys-ap
Max ToC Depth: 3
Markup Shorthands: markdown yes
Repository: digst/trust
Inline Github Issues: full
Logo: digst...
</pre>

<h1>Standard for beskrivelse af it-systemer (basisprofil)</h1>

Version 1.0.0

November 2019


Læsevejledning:

Dette dokument udgør en fællesoffentlig standard for beskrivelse af offentlige myndigheders it-systemer.

Kapitel 1 introducerer standardens formål, baggrund og den metode, hvormed standarden er blevet udarbejdet. Kapitel 2 og 3 beskriver standardens anvendelse ud fra forskellige indfaldsvinkler skitserer og udfordringerne ved at etablere et fælles sprog på området.

Kapitel 4 definerer standardens helt centrale begreb, 'it-system', og Kapitel 5 præsenterer indledningsvist en oversigt over standardens  underliggende emneområder, og hver sektion i dette kapitel dykker ned i et af emneområderne. I Kapitel 4 og 5 vil udvalgte begreber være markeret med **fed skrifttype** -- disse modelleres i den underliggende datamodel som klasser eller egenskaber og kan også ses i fx regnearksskabelon (Bilag B), maskinlæsbart format (Bilag C) og UML-modeller (Bilag E og F).

Kapitel 6 beskriver kort selve datamodellen. For en dybere gennemgang henvises til det selvstændige dokument 'Anvendelsesprofil for beskrivelse af it-systemer', som er selve datastandarden bag dette dokument målrettet dataarkitekter. Dette kapitel fortæller også, hvordan beskrivelser af it-systemer udarbejdet i henhold til standarden kan udveksles -- dels via regneark -- dels via et maskinfortolkeligt format.  Kapitel 7 indeholder en liste over eksisterende modellering på området og introducerer en overordnet mapning fra de eksisterende modeller til denne standard.

Kapitel 8 beskriver øvrige perspektiver ved anvendelsen af standarden, herunder potentialet ved sammenhængende modellering af data på tværs.

Bilagene kan inddeles i tre kategorier. Bilag A viser de klassifikationer/kontrollerede udfaldsrum, der anvendes i standarden, Bilag B og C giver skabeloner og vejledning til udfyldelse af oplysninger om it-systemer, og Bilag D-G omhandler den bagvedliggende begrebs- og datamodel.

|

1\. Introduktion
================

 |
|

Dette dokument udgør en fællesoffentlig standard for beskrivelse af offentlige myndigheders it-systemer. Standarden omfatter basisoplysninger om it-systemer, som fx it-systemnavn, it-systemejer, anvendelsesformål, ibrugtagningsdato mv., samt en ensartet struktur for disse oplysninger i et fælles udvekslingsformat, som gør det muligt at dele oplysninger om it-systemer på en effektiv måde. 

 |
|  |

1.1 Formål
----------

Der indsamles oplysninger om offentlige it-systemer mange steder og på mange forskelligartede måder. Derfor er der god værdi i at standardisere den måde, it-systemer beskrives på, og dermed understøtte højere grad af genbrugelighed og kvalitet i de indsamlede oplysninger. Standarden forventes at have bred anvendelighed hos offentlige organisationer i en lang række forskellige udvekslingssituationer. En fælles standard har endvidere til formål at bidrage til at skabe et fælles og tværgående sprog for overblik over anvendte it-systemer.

1.2 Baggrund
------------

Standarden er etableret og efter aftale med KL, Danske Regioner og Digitaliseringsstyrelsen som følge af relateret standardiseringsarbejde[[1]](file:///C:/Users/b025870/Desktop/Standard%20for%20beskrivelse%20af%20it-systemer%20-%20Basisprofil_CLA.docx#_ftn1) udført efter anbefaling af Kulturministeriets Arkivudvalg. Standarden skal understøtte at it-systemer kan beskrives på en ensartet måde, og at beskrivelsen kan dække de mest udbredte behov for udveksling af information om it-systemer i det offentlige. Første konkrete ibrugtagning af standarden vil være i forbindelse afgivelse af oplysninger om it-systemer til Rigsarkivet.

1.3 Metode
----------

Denne standard udgøres af en basisprofil (SYS-AP), som indeholder de basisoplysninger om it-systemer, der indgår i langt de fleste it-systembeskrivelser.  Basisoplysningerne udgør en fælles kerne, der kan udvides med yderligere kontekstafhængige oplysninger, i nye og mere specifikke anvendelsesprofiler. Informationer dannet på baggrund af to eller flere specifikke anvendelsesprofiler kan potentielt bringes til at hænge sammen via denne fælles kerne.

Den første anvendelsesprofil, som udvider basisprofilen, vil være målrettet arkivering (archvSYS-AP). Se også 'Standard for beskrivelse af it-systemer -- Arkivprofil'.

Selve udviklingsarbejdet er foretaget i henhold de Fællesoffentlige regler for begrebs- og datamodellering, og standarden udgøres af en basisprofil, der sammensætter flere eksisterende nationale og internationale modeller.

Denne profil anvender fx kernemodeller til beskrivelse af it-system ([SYS](http://data.gov.dk/model/core/itsystem.html)), datasæt ([DCAT](https://www.w3.org/TR/vocab-dcat-2/)), organisation ([ORG](https://www.w3.org/TR/vocab-org/)), juridiske ressourcer ([ELI](https://op.europa.eu/en/web/eu-vocabularies/eli)), kontakter ([FIBO](https://spec.edmcouncil.org/fibo/)), klassifikationer ([SKOS](https://www.w3.org/TR/skos-primer/)) m.fl. Se Dataspecifikationsdokumentet for yderligere oplysninger om disse modeller. Flere af de internationale kernemodeller er profileret i forhold til en dansk anvendelseskontekst. Her kan nævnes dataspecifikationerne [Anvendelsesprofil for organisation](https://arkitektur.digst.dk/rammearkitektur/datastandarder/anvendelsesprofil-organisationer), [Anvendelsesprofil for klassifikation,](https://arkitektur.digst.dk/rammearkitektur/datastandarder/anvendelsesprofil-klassifikationer) samt Anvendelsesprofil for Datasætkataloget. Flere af disse anvendelsesprofiler er mappet til OIO-standarderne.

Basisprofilen og arkivprofilen er blevet udarbejdet på baggrund af research- og udviklingsaktiviteter kombineret med feedback fra og sparring med en projektgruppe med medlemmer fra følgende interessentorganisationer: Rigsarkivet, KL, Danske Regioner, Organisationen Danske Arkiver, OS2Kitos og Digitaliseringsstyrelsen med repræsentanter fra Ministeriernes Kontor for it-styring og Center for Teknologi og Datastrategi. I forbindelse med researchaktiviteterne er flere eksisterede modeller og værktøjsunderstøttelse til registrering af it-systemer undersøgt nærmere, fx Model for porteføljestyring af statslige it-systemer, OS2Kitos og Rigsarkivets anmeldelses- og tilsynsskemaer. Læs mere om dette i Mapning til eksisterende modeller.

|

|

2\. Standardens anvendelse og afgrænsning
=========================================

 |
|

Basisprofilen danner grundlag for fællesoffentlig deling af oplysninger om it-systemer via emne- eller områdespecifikke anvendelsesprofiler. De specifikke profiler etableres med udgangspunkt i basisprofilen og efter behov.

 |
|  |

2.1 Afgrænsning
---------------

It-systemer kan beskrives ud fra flere forskellige aspekter eller emner. Basisprofilen indeholder oplysningstyper for en række aspekter af it-systemer. Med basisprofilen er det forsøgt at finde en passende balance mellem et indhold, der ikke bliver for omfattende, og et indhold, der berører organisatorisk væsentlige emner, og områder, der kan beskrives i mere specifikke profiler. Basisprofilen er altså ikke tænkt som en altfavnende beskrivelse af alle aspekter omkring it-systemer. Profilens model skal alene give en *overordnet* indgang til de it-systemer, en organisation anvender.

Uddybende beskrivelse af emner som eksempelvis kontraktstyring, infrastruktur og sikkerhed vil kræve andre modeller, udtrykt i andre mere specifikke anvendelsesprofiler. Basisprofilens model er skabt med fokus på at kunne lette integrationen mellem øvrige it-systembeskrivende modeller og profiler.

*Eksempelvis bidrager standarden med overordnede oplysninger om it-systemers tekniske indretning (jf afsnittet om teknisk indretning i Kapitel 4), men giver ikke i sig selv mulighed for at udtrykke detaljerede oplysninger om fx hardwareinstanser eller lignende.*

2.2 Anvendelse
--------------

Når der fremover defineres anvendelsesprofiler, hvor 'it-system' er det centrale emne, skal basisprofilen bruges som afsæt for den nye profil. I den nye profil skal basisprofilens elementer indgå i så stort et omfang som muligt for at give det bedst mulige grundlag for efterfølgende at skabe sammenhæng mellem datasæt etableret på baggrund af ellers forskelligartede it-system-profiler.

Basisprofilens elementer består af klasser, egenskaber (attributter), der beskriver den enkelte klasse, samt egenskaber (associationer), der beskriver relationer mellem klasser. Disse elementer enten kan eller skal genanvendes af de mere specifikke anvendelsesprofiler, der dannes på baggrund af basisprofilen. Angivelsen af, om og hvordan det enkelte element indgår i en ny anvendelsesprofil, angives forskelligt for klasser og for egenskaber.

### Anvendelse af klasser

For hver enkelt klasse, der er del af basisprofilen, angives det om klassen enten skal, bør eller kan indgå i en ny profil.

Klasser, der altid skal indgå i applikationsprofiler baseret på basisprofilen, markeres med en stereotypeangivelse kaldet <mandatory> (obligatorisk).

Klasser, der anbefales at indgå for at sikre det bredest mulige grundlag for sammenhæng mellem de enkelte profiler, er markeret med stereotypen <recommended> (anbefalet). Disse klasser bør i videst muligt omfang medtages, hvis der er datagrundlag for det i de datasæt de nye profiler rettes mod.

Klasser, der kan indgå, men ikke nødvendigvis skal indgå, markeres som <optional> (valgfri).

### Anvendelse af egenskaber

Basisprofilens egenskaber anvender ikke angivelserne <mandatory>, <recommended> og <optional>. For alle egenskaber, attributter og associationer angives i stedet egenskabens multiplicitet. Det vil sige; det angives, hvor mange der mindst skal være, og hvor mange der højest må være af en attribut eller en association.

I basisprofilen er de fleste multipliciteter holdt relativt åben ved at angive mindsteværdien som '0' (nul) og maksimumværdien som '*' (ubegrænset). Nye profiler baseret på basisprofilen kan altid indsnævre en multiplicitets udfaldsrum yderligere, men må ikke udvide den!

Der er indført visse grundlæggende krav til beskrivelse af it-systemer i basisprofilen i form af multipliciteter. Der *skal* udfyldes **it-systemnavn** og **it-systembeskrivelse**,. Disse krav er baseret på en vurdering af laveste fællesnævner for fremtidige profileringer. Øvrige oplysninger *kan* udfyldes. Se disse udfyldelseskrav i Bilag B eller se multipliciteterne i UML-diagrammerne,

### Ny anvendelsesprofil med udgangspunkt i basisprofilen

Princippet for oprettelse af nye profiler på baggrund af basisprofilen vises her i form af et eksempel, hvor anvendelsesprofilen for arkivering bruges som eksempel på en ny profil.

Med udgangspunkt i den eksisterende basisprofil vurderes anvendeligheden af de enkelte klasser og egenskaber ud fra de behov, der kendes til en arkiveringsprofil.

Når vurderingen er foretaget, har man en reduceret profil som illustreret på nedenstående diagram. Alle elementer markeret med grønt vil indgå i den nye arkivprofil, mens alle elementer markeret med rød ikke inddrages i profilen.

Derefter tilføjes de elementer der er nødvendige for arkivprofilen og der sættes eventuelle yderligere begrænsninger på multipliciteter. I nedenstående diagram er tilføjelser og multiplicitetsændringer markeret med orange.

2.3 Standardisering af deling af it-systemoplysninger
-----------------------------------------------------

Basisprofilen danner grundlag for entydige og præcise udvekslinger af it-systemoplysninger til en lang række formål. Oplysninger om offentlige it-systemer indsamles mange steder, men på forskellig vis. Med et fælles sprog, som profilen præsenterer, lægges fundamentet for en ensartet og konsistent udveksling af data om it-systemer. Brug af profilen vil ikke betyde, at eksisterende modeller eller interne registreringer skal laves om, men gør at de kan mappes til et fælles sprog, så data kan deles på en effektiv og entydig måde via et maskinlæsbart format uden behov for manuel behandling, eksempelvis for at opfylde informationsbehovet i forbindelse med afgivelse af systemoplysninger til hjemmelshavende myndigheder.

*Eksempelvis kan anvendelse af basisprofilen danne udgangspunkt for maskinlæsbar afgivelse af systemoplysninger til myndigheders interne it-systemoverblik og det statslige it-systemporteføljeoverblik jf. Strategi for it-styring i staten*[[2]](file:///C:/Users/b025870/Desktop/Standard%20for%20beskrivelse%20af%20it-systemer%20-%20Basisprofil_CLA.docx#_ftn2)*, da kerneinformationerne vil være omfattet af standarden allerede. Dette kunne gøres i form af en udvidelse i form af en mere specifik anvendelsesprofil til håndtering af de vurderingsspørgsmål, fx "I hvilken grad er der omskiftelighed i forretningsgrundlaget for it-systemet?". Der kan også arbejdes videre med disse systemoplysninger i forbindelse med udarbejdelse af fortegnelse over databehandlingsaktiviteter, jf. Datatilsynets Vejledning om fortegnelse[**[3]**](file:///C:/Users/b025870/Desktop/Standard%20for%20beskrivelse%20af%20it-systemer%20-%20Basisprofil_CLA.docx#_ftn3)*.

2.4 It-systemoversigt og Datamanagement
---------------------------------------

Standarden kan danne grundlag for, at en myndighed internt vedligeholder data omkring myndighedens it-systemer ét sted, samt eventuelt at lade disse sammenstilles med oplysninger fra andre relevante datakilder. Via sammenhængene modellering kan der udtrækkes forskellige datasæt til opfyldelse af forskellige indmeldingsforpligtelser og --krav. Ikke alle oplysningstyper vil være relevante til alle anvendelser, hvorfor yderligere profileringer og udvælgelse af relevante oplysningstyper kan være nødvendige til øvrige anvendelser.

Med en standardiseret model og format vil myndigheder også kunne dele informationer på tværs på frivillig basis. Denne deling kan eksempelvis ske i form af et fælles it-systemregister, hvor myndigheder kan finde informationer om it-systemer samt svar på en række spørgsmål som:

o *Hvilke andre myndigheder anvender system X?*

o *Hvor mange it-systemer har borgere som målgruppe?*

o *Hvilke it-systemer understøtter myndighedernes interne it-udvikling (FORM-opgave)?*

o *Hvilke databærende it-systemer skaber og eventuelt udstiller datasæt, der skal registreres i et fællesoffentligt datasætkatalog?*

o *Hvilke system-til-system-integrationer findes der, og kan de kritiske\
afhængigheder identificeres?*

o *Hvilke it-systemer indeholder fortrolige eller personfølsomme data?*

|

3\. Udfordringer
================

 |
|

Etableringen af et fælles sprog kan danne grundlag for effektiv udveksling af data om it-systemer, men standardisering har også nogle iboende udfordringer og kræver et overblik over eksisterende begreber og indfaldsvinkler

 |
|  |

3.1 Forskellige indfaldsvinkler
-------------------------------

Der indsamles oplysninger om offentlige it-systemer mange forskellige steder, men formålet og fokus kan variere meget, alt afhængig af om indfaldsvinklen er arkivering, forretnings- og samfundskritikalitet, drift og IT-service-management, kontraktstyring eller arkitekturbeskrivelse.

I forhold til basisoplysninger, som indgår i de eksisterende modeller, kan der fx være mange lighedspunkter og identiske begreber, men flere er ikke defineret på helt samme måde, og selvom termerne ofte er enslydende, er der også stor variation. Terminologien og begreberne, som de findes i de forskellige modeller, afspejler typisk indfaldsvinklen og den formelle ramme, som har dannet grundlag for modellen, og det formål, modellen er udarbejdet med. Læs mere om dette i Kapitel 7 om mapning til eksisterende modeller.

3.2 Hver specifik anvendelse kræver klar formålsbeskrivelse
-----------------------------------------------------------

Det vil være nødvendigt i forbindelse med hver specifik anvendelse at undersøge, hvilket formål profileringen af standarden skal løfte, samt hvilken delmængde af en potentielt meget stor mængde af mulige it-systemer der ønskes beskrevet.

Formål, detaljeringsgrad eller granularitet og relevante klassifikationer skal vurderes nøje, så relevante oplysninger om relevante it-systemer kan registreres, og så det er muligt at danne et overblik over it-systemer, der opfylder givne kriterier.

4\. Centrale begreber
=====================

 |
|

Begrebet 'it-system' udgør det centrale element i denne standard og defineres bredt for at kunne favne mange anvendelser. Ved at koble dette til relevante klassifikationer bliver det muligt med standarden at indsnævre mængden af de it-systemer, der skal beskrives.

 |
|  |

4.1 System, informationssystem, it-system og implementering
-----------------------------------------------------------

Et ***system*** defineres generelt som "*et system er en kombination af interagerende elementer, der er organiseret for at opnå et eller flere erklærende formål"* ligesom i[ISO/IEC 15288][[4]](file:///C:/Users/b025870/Desktop/Standard%20for%20beskrivelse%20af%20it-systemer%20-%20Basisprofil_CLA.docx#_ftn4).\
Det bemærkes også, at *"Et system er i denne sammenhæng menneskeskabt og består ikke blot af hardware, software og data, men også af mennesker, processer, procedurer, faciliteter og materialer og naturlige genstande".*

Ser vi alene på systemer til indsamling, organisering, lagring og kommunikation af information, har vi at gøre med informationssystemer, og når (computer)-teknologi anvendes til at behandle disse informationer eller data, har vi at gøre med it-systemer[[5]](file:///C:/Users/b025870/Desktop/Standard%20for%20beskrivelse%20af%20it-systemer%20-%20Basisprofil_CLA.docx#_ftn5).

|

Begrebet ***it-system* **defineres derfor i denne standard som\
*"system, der består af digitale informationsteknologier".*  

 |

Definitionen er bevist holdt meget bredt favnende for at kunne dække de mange definitioner på it-system, som standardarbejdet har mødt i offentligt regi. Eksempelvis defineres it-system i 'Model for porteføljestyring af statslige it-systemer' med teksten:

*"et produkt eller en ressource, der understøtter en eller flere forretningsprocesser og omfatter såvel applikationen som den nødvendige hardware og it-infrastruktur til brug for it-systemets afvikling af statslige it-systemer omfatter også it-systemer, hvor myndigheden har it-systemejerskabet, men hvor it-systemets drift forestås af en ekstern part, for eksempel Statens It eller en privat leverandør."*

Nærværende standards brede definition på et it-system inkluderer altså den mere specifikke, der anvendes af porteføljestyringsmodellen.

Det er også vigtigt at bemærke, at et givet it-system kan instantieres i forskellige it-miljøer. Et **instantieret it-system** kan derfor defineres som "*fysisk instans af et it-system i et bestemt it-miljø".* Fxet testmiljø eller et produktionsmiljø.

### Forskellige formål med beskrivelsen

Denne standard forventes at få bred anvendelse hos offentlige myndigheder til flere forskellige formål, hvorfor definitionen af begrebet 'it-system' har en så anvendelsesneutral og generel karakter som muligt inden for standardens rammer. Det betyder også, at definitionen som udgangspunkt favner mange flere instanser af it-systemer, end hvad et bestemt indmeldingsformål måtte have brug for. Derfor anvendes en række klassifikationer, som giver mulighed for at netop at udpege den delmængde af it-systemer, det er relevant at undersøge eller beskrive til et givet formål.

### Klassifikationer

Klassifikationerne vil blive introduceret og defineret under de relevante emneområder i det følgende kapitel.[[6]](file:///C:/Users/b025870/Desktop/Standard%20for%20beskrivelse%20af%20it-systemer%20-%20Basisprofil_CLA.docx#_ftn6)

Fælles for de nyetablerede klassifikationer er, at de alle er modelleret som selvstændige modeller iht. den internationale W3C-specifikation SKOS ([Simple Knowledge Organization System](https://www.w3.org/TR/skos-primer/)). Der er også udarbejdet en [dansk profil](https://arkitektur.digst.dk/rammearkitektur/datastandarder/anvendelsesprofil-klassifikationer) på baggrund af denne som også er mappet til OIO Klassifikation.

Det forventes, at de relevante myndigheder forretningsgodkender og overtager ansvaret for indholdet af de respektive klassifikationer.

### Hvornår er der tale om et nyt it-system?

I forhold til ibrugtagningen af et it-system i en organisation kan det i visse tilfælde være svært at vurdere, hvornår der er tale om, at organisationen overgår fra ét it-system til et andet, eksempelvis ved overgangen fra én version af et kommercielt produkt til en anden version. Her kan vurderingen tage udgangspunkt i, om it-systemet *leverer en anden service* end den oprindelige, hvilket ofte er forbundet med etableringen af en ny kontrakt med rettighedshaveren af det kommercielle produkt. Ny kontrakt vil altså ofte betyde nyt it-system, modsat løbende opdateringer og fejlrettelser til kørende it-systemer. I forhold til databærende systemer kan det også være relevant at se på, om fx hele den bagvedliggende databasestruktur er skiftet ud.

Som det blev beskrevet i foregående kapitel, kan man have behov for at beskrive it-systemer ud fra forskellige indfaldsvinkler, og denne indfaldsvinkel er også afgørende for hvad et it-systemoverblik skal indeholde. Tager man eksempelvis udgangspunkt i den overordnede it-service, som tilbydes slutbrugeren, kan det være tilstrækkeligt at se på it-systemet som et samlet hele, hvorimod det i forhold til drift, vedligehold og kritikalitet typisk er nødvendigt at beskrive it-systemets underliggende applikationskomponenter og afhængigheder, som tilsammen udgør it-systemet. 

4.2 Implementering og anvendelse; instantieret it-system
--------------------------------------------------------

Begrebet ***it-system*** udtrykker it-systemer i en organisation for -- som førnævnt -- at opnå et eller flere erklærede formål. Et konkret, implementeret eller 'instantieret' it-system kaldes et **'instantieret it-system'**. Et instantieret it-system kan i basisprofilen beskrives som havende relationer til en eller flere fysiske datasæt og/eller en eller flere services.

I basisprofilen ligger fokus på de oplysninger, der typisk udveksles, hvorfor yderligere infrastrukturoplysninger om hardware og software ikke indgår her. Basisprofilen er opbygget, så den kan danne udgangspunkt for en infrastrukturprofil med disse oplysninger.

4.3 It-systemets produktserie
-----------------------------

Det kan være praktisk at kunne omtale systemer, der, i deres udviklingsforløb, har mange versioner under en fælles betegnelse, der dækker alle versioner af systemet.

Hvis vi eksempelvis har systemet 'SuperSystem X', der eksisterer som 'SuperSystem X, version 1' 'SuperSystem X, version 2' og 'SuperSystem X, version 3', vil de tre systemer (og deres efterfølgere) ofte blot blive regeret til som 'SuperSystem X' -- uden versionsangivelse.

For at dække dette behov anvender basisprofilen klassen ***produktserie.***  

|

5\. Standardens emnemæssige relationer
======================================

 |
|

I det følgende gives en oversigt over standardens potentielle emnemæssige relationer og en beskrivelse af hvert underliggende emneområde

 |
|  |

It-systemer kan beskrives ud fra flere forskellige aspekter eller emner. De helt grundlæggende kerneinformationer ses i midten af figuren herunder, og de øvrige otte emneområder afspejler arkitekturprincipperne fra rammearkitekturen: styring, strategi, jura, sikkerhed, opgaver, information, applikation og infrastruktur, som beskrives i Hvidbog om fællesoffentlig digital arkitektur (FDA)[[7]](file:///C:/Users/b025870/Desktop/Standard%20for%20beskrivelse%20af%20it-systemer%20-%20Basisprofil_CLA.docx#_ftn7) .

Figur 5.1: Illustration af standardens emnemæssige

Disse otte emner dækker bredt, og for at dække en specifik anvendelseskontekst vil det typisk være nødvendigt at udvide basisprofilen med oplysninger fra forskellige emneområder. I tillæg til de otte emneområder eksisterer et metalag med informationer om myndighedens udveksling af disse oplysninger til et bestemt formål, men dette præciseres nærmere i de konkrete anvendelsesprofiler.

5.1 Kerneinformation
--------------------

Et it-system kan forsynes med en ***identifikator*** (et ID) der entydigt udpeger det konkrete it-system. Et it-system tilføjes et eller flere navne. Et af navnene vil være it-systemets primære eller ***foretrukne navn,*** men andre, fx kaldenavne, kan angives som ***alternative navne.***

Hvor et it-system kan beskrives som en implementering og ibrugtagning af et softwareprodukt tilhørende en bestemt produktserie, som fx Acadre eller F2, vil it-systemnavnet typisk være lig ***navnet på produktserien,* **som producenten har markedsført eller som anført i hovedkontrakten med leverandøren, men it-systemet kan også have andre lokale navne.

En produktserie kan have en overordnet ***beskrivelse af produktseriens*** egenskaber, som det fx ses i SKI-kataloget[[8]](file:///C:/Users/b025870/Desktop/Standard%20for%20beskrivelse%20af%20it-systemer%20-%20Basisprofil_CLA.docx#_ftn8), men i forbindelse med ibrugtagning er det også muligt at angive en ***it-systembeskrivelse,*** som i fritekst redegør for formålet med it-systemets anvendelse eller it-systemets nøglefunktion i en organisation. Derudover bør et it-systems ***anvendelsesformål*** også beskrives ved opmærkning ift. offentlige opgaver med klassifikationerne FORM/KLE, som det beskrives under emnet 'forretningsunderstøttelse'. Supplerende bemærkninger eller oplysninger kan også tilføjes som en ***kommentar*** i fritekst.

Som en del af kerneinformationerne hører ***ibrugtagningsdato*** og ***udfasningsdato,*** som tilsammen beskriver perioden fra den dato, hvor it-systemet blev taget i brug med delvis eller fuld funktionalitet, indtil den dato, hvor it-systemet endeligt bliver afviklet. Datoangivelserne kan eventuelt suppleres med en ***operationel status,*** som angiver, hvilken tilstand systemet befinder sig i, i forhold til ibrugtagning. Se udfaldsrummet i [[CL1]](file:///C:/Users/b025870/Desktop/Standard%20for%20beskrivelse%20af%20it-systemer%20-%20Basisprofil_CLA.docx#_msocom_1) , se Bilag A.

For at kunne identificere, hvilken version af softwareproduktet der er taget i anvendelse, eksempelvis i forhold til en bestemt kontrakt med en leverandør, kan det være relevant at angive et ***versionsnummer***. Hvis et versionsnummer er specificeret i kontrakten, bør dette anvendes.

*Eksempelvis kan der ved anvendelse af cBrains F2 angives version 5.3 (og ikke 5.3.0.41112)*

5.2 Opgaver
-----------

Et it-system yder en given it-service, som understøtter forretningens opgaver. Et it-system kan beskrives med et eller flere anvendelsesformål, der antages at være at understøtte en ***forvaltningsopgave***. Til dette formål anvendes en klassifikation over offentlige opgaver eller såkaldte forvaltningsopgavetyper såsom Den Fællesoffentlige Referencemodel (FORM) eller KL Emnesystematik (KLE).  KLE er en emnesystematik/journalplan, der dækker det kommunale område. FORM er en overordnet emnesystematik, der dækker opgaveporteføljen i hele den offentlige sektor -- dvs. staten, kommunerne og regionerne. KLE er som regel mere detaljeret end FORM på det kommunale område. Det foreslås, at KLE anvendes af kommunerne, og FORM af regioner og statslige administrative enheder -- som minimum på det øverste niveau (hhv. serviceområde i FORM og emnegruppe i KLE):

**Klassifikation KLE:** <http://www.kle-online.dk/soegning>

**Klassifikation FORM:** <http://www.form-online.dk/soegning>

*Eksempelvis kan en myndighed anvende Formpipes Acadre og cBrains F2 ESDH til at understøtte FORM-forvaltningsopgaven "65.50.05.05 Sagshåndtering" (FORM v.2.14) el. KLE-emnet "00.15.12. Kvalitetsstyringssystem, sagsbehandling" (KLE v. Aug. 2019)*

Bemærk, at produkter i SKI-kataloget allerede er opmærket med FORM samt internationale referencekoder såsom Common Procurement Vocabulary Codes (CPV)[[9]](file:///C:/Users/b025870/Desktop/Standard%20for%20beskrivelse%20af%20it-systemer%20-%20Basisprofil_CLA.docx#_ftn9) og United Nations Standard Product and Services Code (UNSPSC)[[10]](file:///C:/Users/b025870/Desktop/Standard%20for%20beskrivelse%20af%20it-systemer%20-%20Basisprofil_CLA.docx#_ftn10), som er klassifikationer for hhv. udbudte opgaver og varer og tjenesteydelser. Bemærk, at en sådan opmærkning angiver, at produktet har ***kapabilitet til at understøtte*** en given opgave. SKI anvender tillige STORM (Service- og Teknologireferencemodel)[[11]](file:///C:/Users/b025870/Desktop/Standard%20for%20beskrivelse%20af%20it-systemer%20-%20Basisprofil_CLA.docx#_ftn11) på trods af, at den ikke længere opdateres.

FORM og KLE indeholder henvisninger til de love og lovbekendtgørelser, som de offentlige opgaver udspringer fra, så ved at opmærke et it-system med FORM eksisterer der også indirekte en relation til retsgrundlaget for it-systemets anvendelse. Der er også muligt via FORM at se, hvilke myndigheder de forskellige opgaver tilhører. KLE indeholder, ud over love og lovbekendtgørelser, også bekendtgørelser. FORM mapper til paragraffer i finansloven og KLE, og KLE mapper til Social- og Indenrigsministeriets kontoplan.

Når en organisation skifter et it-system ud med et andet it-system til varetagelse af samme funktion, kan det tidligere it-system eksplicit angives som et såkaldt **forgængersystem.**

Bemærk, at en organisations portefølje af it-systemer kan være sammensat af dels organisationens internt-rettede it-systemer (fx et sagsbehandlingssystem til organisationens egne medarbejdere) og dets eksternt-rettede it-systemer (fx et borgerrettet selvbetjeningssystem). Med henblik på at kunne skelne mellem it-systemer med en snæver målgruppe og it-systemer med en bred målgruppe kan it-systemer klassificeres ift. en ***målgruppeklassifikation***, se Bilag A. Her angives, om it-systemet har en intern eller ekstern målgruppe set ift. organisationen.

5.3 Styring
-----------

Et it-system kan have mange forskellige relationer til aktører, som hver især har en særlig interesse i systemet, og som dermed udgør systemets interessenter. Aktørerne kan være personer eller organisationer, men det anbefales, i det omfang det er muligt, ikke at registrere oplysninger om fysiske personer, men derimod den relevante medarbejderrolle eller organisatoriske enhed.

På overordnet niveau angives ***it-systemejeren*** -- en person eller organisation med det overordnede ansvar for et givet it-systems drift, vedligehold og anvendelse. Ofte vil it-systemejeren være lig kontraktejeren og kan identificeres præcist i myndighedens kontraktstyring.

I en given organisations praktiske og tekniske forvaltning af et it-system er det også vigtigt at registrere ***it-systemforvalteren***, dvs. den organisatoriske enhed eller medarbejder, som administrerer og træffer afgørelser vedrørende tekniske anliggender ***på vegne af*** systemejeren. I forbindelse med større it-systemer kan forvalterrollen være opdelt i en intern forretningsmæssig forvalterrolle og en teknisk forvalterrolle hos en leverandør.

*Eksempelvis er Kontorchefen for Center for Systemforvaltning i Digitaliseringsstyrelsen it-systemejer for NemLog-in, mens it-systemet forvaltes af NemLog-in-teamet.*

For databærende it-systemer skal den ***dataansvarlige*** aktør også angives, dvs. den organisation som har det administrative ansvar for data. I forhold til persondata indsnævres denne definition yderligere til "*en fysisk eller juridisk person, en offentlig myndighed, en institution eller et andet organ, der alene eller sammen med andre afgør, til hvilke formål og med hvilke hjælpemidler der må foretages behandling af personoplysninger*", jf. GDPR[[12]](file:///C:/Users/b025870/Desktop/Standard%20for%20beskrivelse%20af%20it-systemer%20-%20Basisprofil_CLA.docx#_ftn12). Én myndighed kan være dataansvarlig for et system, mens det faktisk er ***databehandler,* **som behandler personoplysninger på den dataansvarliges vegne, der er i besiddelse af systemet og anvender det.  Det kan være en fordel at registrere begge oplysninger. I nogle tilfælde er der forskel på dataansvarlig og databehandler. I det omfang, at leverandører har fået instruks af den dataansvarlige til at behandle personoplysninger, betragtes disse også som databehandlere, jf. Datatilsynets vejledning om databehandlere og dataansvarlige[[13]](file:///C:/Users/b025870/Desktop/Standard%20for%20beskrivelse%20af%20it-systemer%20-%20Basisprofil_CLA.docx#_ftn13). Det kan også være relevant at angive den konkrete ***dataskaber***, dvs. den aktør, der har det primære ansvar for tilvejebringelsen af datasættet.

Et it-system kan dokumenteres ved hjælp af forskellige dokumenter, der hver har sit formål og målgruppe, fx via **dokumentationsreference** såsom arkitekturdokumentation, installationsvejledning og slutbrugervejledning.

5.4 Strategi
------------

Det strategiske perspektiv omhandler ønskede fremtidige tilstande for myndighedernes it-systemer. Ledelsen i offentlige myndigheder skal være skarpe på de it-systemer, de råder over, og hvordan it-systemerne bedst understøtter myndighedernes arbejde aktuelt og i fremtiden. Det giver bedre mulighed for løbende at gennemføre strategiske forbedringer, der fx kan være vigtige for datakvalitet, brugervenlighed og sikkerhed.

Et it-system kan således indgå i en overordnet kortlægning med henblik på udarbejdelse af ***tilknyttede*** ***handlingsplaner***. Denne oplysninger indgår ikke i basisprofilen, men ville være relevant at definere og medtage i en portefølgestyringsprofil.

5.5 Jura
--------

I forbindelse med ibrugtagning og anvendelse af et it-system kommer der typisk en lang række leverandørkontrakter i spil, men i denne standard fokuseres på leverandører, der leverer en ydelse ift. udvikling, vedligehold, drift og support af it-systemet. Disse oplysninger vil typisk være indsamlet og registreret i forbindelse med kontraktstyring.

Derudover vil det i denne standard også være muligt helt overordnet at angive it-systemets primære ***udviklingspart***, ***vedligeholdelsespart*** og ***driftspart***. 

Bemærk dog, at denne direkte angivelse af it-systemets primære leverandører skal betragtes som en forenkling, som typisk ville kunne udledes via kontraktens parter.

Bemærk også, at selvom interne -- både mundtlige og skriftlige -- aftaler vedrørende et mindre egenudviklet it-systems videreudvikling, vedligehold og drift ikke altid er beskrevet i formelle og juridisk bindende kontrakter, kan disse stadig betragtes som værende kontrakter, og beskrives som sådan.  

Allerede inden en givet produktserie tages i anvendelse, har produktserien typisk allerede en række relationer, som fx er registreret i OS2Kitos. De intellektuelle rettigheder til produkter i en produktserien besiddes af en ***rettighedshaver***, og myndighedens brugsret i forhold til it-systemets og dets komponenter kan variere i forhold til it-systemets type og aftalte kontraktforhold.

Et it-system kan være relateret til en lang række kontrakter, hvoraf der i denne standard fokuseres på de kontrakter, der vedrører it-systemets udvikling, vedligehold, drift og support. Som beskrevet ovenfor er det muligt blot at angive en overordnet relation fra et it-system til hhv. udviklingspart, vedligeholdelsespart el. driftspart, men en mere præcis beskrivelse af leverandørforhold kan opnås ved at beskrive sammenhængen til de formelle it-kontrakter.

Til beskrivelse af kontrakter anvendes et vokabular for finansielle forretninger, Financial Industry Business Ontology (FIBO)[[14]](file:///C:/Users/b025870/Desktop/Standard%20for%20beskrivelse%20af%20it-systemer%20-%20Basisprofil_CLA.docx#_ftn14), som er et fælles produkt fra OMG og Enterprise Data Management (EDM) Council.

For et it-system kan der angives referencer til kontrakternes ***identifikation*** i et kontraktstyringssystem, eventuelt suppleret med en kontrakttypeopmærkning ved hjælp af en ***it-kontrakttypeklassifikation***, se Bilag A.

Én kontrakt med en given leverandør kan også indeholde aftale om flere ydelser på én gang, fx en kombineret drifts- og vedligeholdelsesaftale. Softwarelicenskontrakter betragtes som værende af en særlig karakter. Anskaffelse af standardsoftware kræver typisk også, at de indkøbte licenser administreres, og at licensvilkår overholdes. Derfor kan det internt i en organisation kan være relevant at registrere mere detaljerede oplysninger om licenser. Derudover kan der efter behov tilføjes yderligere oplysninger vedrørende kontrakten såsom ***kontraktparter*** og ***kontraktperioder,*** som kan være særligt relevante ift. systemet forvaltning og vurdering af kontrakters udløbsdatoer etc. Disse masterdata vil dog typisk være at finde i et kontraktstyringssystem.

5.6 Information
---------------

De data, som et instantieret it-system ***skaber,*** kan betragtes som en specifik fysisk **repræsentation** af et ***datasæt*** -- en samling af oplysninger bestående af enkelte dele der forvaltes under et[[15]](file:///C:/Users/b025870/Desktop/Standard%20for%20beskrivelse%20af%20it-systemer%20-%20Basisprofil_CLA.docx#_ftn15), og beskrivelsen af datasæt og datasætrepræsentationer følger i denne sammenhæng W3Cs Data Catalogue Vocabulary (DCAT)[[16]](file:///C:/Users/b025870/Desktop/Standard%20for%20beskrivelse%20af%20it-systemer%20-%20Basisprofil_CLA.docx#_ftn16). Et datasæt og dets repræsentationer kan forsynes med en ***titel,*** og **første og sidste datatilføjelsesdato** kan angives for datasætrepræsentationen.  

Datasætrepræsentationer, som it-systemet ***udstiller*** og ***anvender,*** bør registreres ved reference til Datasætkataloget[[17]](file:///C:/Users/b025870/Desktop/Standard%20for%20beskrivelse%20af%20it-systemer%20-%20Basisprofil_CLA.docx#_ftn17). Det fællesoffentlige datasætkatalog er et katalog, der har til hensigt at samle metadata om myndigheders datasæt, hvilket blandt andet understøtter Lov om videreanvendelse af den offentlige sektors informationer (PSI-direktivet).[[18]](file:///C:/Users/b025870/Desktop/Standard%20for%20beskrivelse%20af%20it-systemer%20-%20Basisprofil_CLA.docx#_ftn18)

5.7 Sikkerhed
-------------

Emnet sikkerhed kan vedrøre mange forskellige aspekter, fx informationssikkerhed, persondatasikkerhed, forretnings- og samfundskritikalitet og fortrolighed.

I henhold til GDPR[[19]](file:///C:/Users/b025870/Desktop/Standard%20for%20beskrivelse%20af%20it-systemer%20-%20Basisprofil_CLA.docx#_ftn19) og Datatilsynets 'Vejledning om fortegnelse'[[20]](file:///C:/Users/b025870/Desktop/Standard%20for%20beskrivelse%20af%20it-systemer%20-%20Basisprofil_CLA.docx#_ftn20) er det for databærende it-systemer relevant at være opmærksom på ***datasletningsfristen***, dvs. førstkommende dato for, hvornår bestemte data i systemet skal være slettet forinden.

It-systemet kan opmærkes med en ***personoplysningskategori,*** som er beskrevet i Datadatatilsynets vejledning, og på denne måde oplyses det, hvorvidt systemet indeholder følsomme personoplysninger eller almindelige personoplysninger, herunder personnummeroplysninger og oplysninger om strafbare forhold. Dertil tilføjes en angivelse af fraværet af personoplysninger, se Bilag A. De følsomme oplysninger er udtømmende oplistet i databeskyttelsesforordningen, og alle andre oplysninger er derfor almindelige personoplysninger. Oplysninger om strafbare forhold og personnumre betragtes som almindelige personoplysninger, men databeskyttelsesloven fastsætter særlige regler om disse oplysninger. Som en hjælp til præcisering kunne en klassifikation med personoplysnings*underkategorier* eventuelt opstilles.

It-systemer skal kunne opmærkes ift. deres grad af kritikalitet ved hjælp af klassifikation for ***kritikalitetstyper***. Se bilag A. Myndigheden kan vælge at tage udgangspunkt i følgende definitioner af hhv. et samfundskritisk og et forretningskritisk it-system. Et** *samfundskritisk it-system* **er et it-system, som enten er vigtigt for den nationale sikkerhed eller for vigtig infrastruktur, hvor misbrug af data vil have store konsekvenser, eller hvor driftsforstyrrelser kan have stor betydning for økonomien i staten eller for mange borgere eller virksomheder.** *Et forretningskritisk it-system*** er et it-system, hvor driftsforstyrrelser kan medføre, at størstedelen af myndighedens medarbejdere ikke kan udføre deres arbejde, eller at myndigheden vanskeligt kan overholde sine forvaltningsmæssige forpligtelser.

Data i it-systemet kan klassificeres med flere forskellige klassifikationer ift. fortrolighed, fx ***Fortrolighedsgrad iht. ISO27002***[****[21]****](file:///C:/Users/b025870/Desktop/Standard%20for%20beskrivelse%20af%20it-systemer%20-%20Basisprofil_CLA.docx#_ftn21)eller ***Fortrolighedsgrad iht.******sikkerhedscirkulæret (EU/NATO)*[**[22]**](file:///C:/Users/b025870/Desktop/Standard%20for%20beskrivelse%20af%20it-systemer%20-%20Basisprofil_CLA.docx#_ftn22).** Se Bilag A. I forhold til klassifikation iht. sikkerhedscirkulæret kan tilføjes 'uklassificeret', så det kan angives, at der er taget stilling til fortrolighedsgraden.

*Eksempelvis kan data i beredskabssystemer eventuelt være opmærket med fortrolighedsgrad, og fortrolighed kan være et relevant aspekt ved indmelding af it-systemoplysninger såsom kritikalitetstype og systemernes tekniske tilstand. *

5.8 Applikation
---------------

Det er muligt, som nævnt i Kapitel 4,  at udpege den ***produktserie,*** it-systemets primære softwareprodukt tilhører, og derudover kan **it-systemanskaffelsestypen** (se Bilag A) angives, dvs. om it-systemet er udviklet i egen organisation, er bestillingsudviklet (fx ved udbud) eller anskaffet som et kommercielt (Commercial-of-the-shelf, COTS) eller open source-standardsystem.

Kommercielle produkter vil for eksempel ofte være beskrevet med metadata af producenten, som også kan indgå i SKI-kataloget, og dertil kan der være tilknyttet særlige leverandørforhold. Standardsystemer kunne eventuelt yderligere opdeles i standardsystemer, som umiddelbart kan anvendes til et givet formål, og standardsystemer, hvortil der er blevet udviklet lokale tilføjelser eller moduler.

Det skal kunne angives, gennem hvilke (logiske) dataservices et instantieret it-system ***udstiller*** og/eller ***anvender*** data. En dataservice forsynes med en URI, der angiver selve ***adgangspunktet,*** som anvendes ved interaktion, samt en ***beskrivelse*** af dataservicen.

5.9 Infrastruktur
-----------------

Denne standard bidrager med *overordnede* oplysninger om it-systemers tekniske indretning og infrastruktur. Efterfølgende kan udvikles en udvidet beskrivelse af den generelle anvendelsesprofil for it-system, samt en anvendelsesprofil for it-infrastruktur. Anvendelsesprofilen for it-infrastruktur forventes primært at fokusere på software, hardware og dataservices på et generaliserende niveau, med mulighed for yderligere specialiseringer og udvidelser.

It-systemer kan være taget i anvendelse i forskellige miljøer iht. systemets udviklingsforløb[[23]](file:///C:/Users/b025870/Desktop/Standard%20for%20beskrivelse%20af%20it-systemer%20-%20Basisprofil_CLA.docx#_ftn23), fx udvikling, afprøvning, præproduktion, produktion, se klassifikationen ***it-miljøtype*** i Bilag A. I forhold til arkivering er kun instanser af it-systemer i produktion relevante.

I en myndigheds interne it-systemoverblik er det i forbindelse med drift relevant at beskrive de relationer, som it-systemer og dets applikationskomponenter har til fx specifikke softwareprodukter, hardwareprodukter, servere, databaser mv, men her ligger fokus på de oplysninger, der typisk udveksles, hvorfor disse infrastrukturoplysninger ikke indgår. 

|

6\. Fælles datamodel og udvekslingsformat
=========================================

 |
|

Denne standard præsenterer et fælles udvekslingsformat til deling af oplysninger om it-systemer.

 |
|  |

6.1 Fælles datamodel
--------------------

Basisprofilens bagvedliggende datamodel udgør den fælles specifikation, hvortil eksisterende it-systembeskrivelser kan mappes. Det er også ud fra denne datamodel, at et maskinfortolkeligt format er blevet udviklet.

Der gives en overordnet beskrivelse af dennes indhold og sammensætning i bilaget 'Om datamodellen'. Her kan også ses to UML-diagrammer for hhv. basisprofilen og den første konkrete anvendelse i en arkivprofil. UML-modellerne er udstillet og kan tilgås via en webbrowser, hvor det er muligt at klikke sig gennem modellen. Bemærk, at modelelementernes metadata er registreret som tagged values.

- Link til webudgivelse af UML-modellerne:\
<http://data.gov.dk/document/itsystemspecification/v1/uml/>

Dataspecifikationen, der beskriver datamodellen i detaljer målrettet dataarkitekter, kan downloades via nedenstående link, og der findes også en oversigt over modellens elementer online.

- Link til online oversigt over modellens elementer:\
[https://data.gov.dk/model/profile/itsystemap#](https://data.gov.dk/rdf2html/index.htm?model=https%3A%2F%2Fdata.gov.dk%2Fmodel%2Fprofile%2Fitsystemap.rdf&sheet=transform2RDFreport_da-en.xsl)    

- Link til download af anvendelsesprofildokumentet [kommer]:\
<http://data.gov.dk/document/itsystemspecification/v1/dataspecification/>

6.2 Maskinfortolkeligt format
-----------------------------

Hvis data skal deles på tværs, bør det være *digitalt understøttet* i de systemer, der anvendes til registrering af systemoplysninger. Systemerne bør bygge på samme logik og standard, så systemerne er i stand til at udveksle data om it-systemer på tværs af organisatoriske skel. Det kan lade sig gøre, hvis data er maskinfortolkelige. Datamodellen er derfor udtrykt med UML med en bagvedliggende semantik med Resource Description Framework (RDF), der kan fortolkes af både mennesker og maskiner. Alle elementerne i datamodellen er derfor defineret inden for rammerne af RDF og har entydig identifikation, der kan anvendes direkte som metadatabeskrivelse af data. Data udtrykt med det maskinlæsbare udvekslingsformat kan også let valideres op imod den bagvedliggende datamodel og dermed sikre højere datakvalitet i de registrerede data.

Eksempeldata i maskinlæsbart format (RDF/XML) kan ses i Bilag C. Bemærk, at der også umiddelbart kan konverteres til andre serialiseringer såsom JSON-LD, Turtle, m.fl.

Godkendelsen af denne basisprofil omfatter ikke krav om anvendelse af det maskinlæsbare RDF-format og dets serialiseringer som JSON-LD, Turtle, RDF/XML

6.3 Skabelon til registrering i regneark
----------------------------------------

Der er også blevet udarbejdet en minimal regnearksskabelon til registrering af oplysninger om it-systemer. Overskrifterne vil svare til egenskaberne, som de er præsenteret i denne standard, og hver element vil entydigt kunne mappes til den bagvedliggende datamodel. Dette betyder også, at det vil være muligt fx at konvertere data eksporteret i csv-format til et maskinfortolkeligt format. I den minimale regnearksskabelon er ikke alle mulige 'felter' tilføjet, men blot de [[CL2]](file:///C:/Users/b025870/Desktop/Standard%20for%20beskrivelse%20af%20it-systemer%20-%20Basisprofil_CLA.docx#_msocom_2) 

Regnearket har den fordel, at det er let at anvende, men regneark har også den store ulempe, at det ofte kræver manuel oprettelse og videre import. Det kan også være svært at repræsentere den kompleksitet, der faktisk kan være tilstede i den bagvedliggende datamodel. Eksempelvis kan et givet it-system godt skabe flere forskellige datasæt, som hver især kan dække forskellige perioder og have forskellige dataansvarlige tilknyttet. I den aktuelle skabelon er det kun muligt at registrere ét datasæt per it-system. Et it-system kan også udstille flere forskellige datasæt, og disses id'er må registreres i samme felt, selvom dette ikke er ideelt. 

I bilaget 'Skabelon til registrering i regneark' kan ses en visning af et sådant regneark, men det kan også downloades fra:

[https://data.gov.dk/document/itsystemspecification/v1/templates/Excelformular_til_indtastning_af_it-systemoplysninger_basisprofil.xlsx](https://data.gov.dk/document/itsystemspecification/v1/templates/Excelformular_til_indtastning_af_it-systemoplysninger_basisprofil.xlsx%20)

|

7\. Mapning til eksisterende modeller
=====================================

 |
|

Som baggrund for udviklingen af denne standard er eksisterede modeller og værktøjsunderstøttelse til registrering af it-systemer blevet undersøgt.

 |
|  |

I dette kapitel refereres til en mapning til en række eksisterende modeller herunder bl.a. Kommunernes IT OverbliksSystem (OS2Kitos), Model for porteføljestyring af statslige it-systemer, Statens It Systemkort samt udvalgte oplysningstyper fra Rigsarkivets anmeldelses- og tilsynsskemaer.

Terminologien og begreberne, som de optræder i de forskellige modeller, afspejler typisk den formelle ramme, som har dannet grundlag for modellen, og det formål, modellen er udarbejdet til. Flere af de eksisterende modeller indeholder oplysninger til beskrivelse af it-systemer. Derudover har flere af dem en række oplysninger, som er specifikke for netop det anvendelsesformål, de hver især løfter.

*Eksempelvis anvender Rigsarkivets anmeldelses- og tilsynsskema termer og begreber omkring **(databærende)** **it-systemer,** som de optræder i de relevante bekendtgørelser ift. arkivering. Det statslige **it-systemporteføljeoverblik** tager afsæt i Strategi for it-styring i staten og har fokus på **samfundskritiske** og **forretningskritiske it-systemer**. Statens It har udarbejdet en indberetningsformular for **it-systemer** i forbindelse med"etablering af **nye løsninger**", der skal driftes af Statens IT, og i deres CMDB-system betragtes hele it-systemer som **business services**. I forhold til arkitekturbeskrivelse anvendes ofte betegnelse **applikationskomponent** fra TOGAF/ArchiMate om it-systemet som hele samt de komponenter, der indgår deri.*

Der er ikke hensigten, at denne standard som udgangspunkt skal kunne rumme alle disse specifikke oplysninger, men centrale oplysningstyper er blevet udvalgt med baggrund i standardens forventede anvendelse som beskrevet i Kapitel 2. Flere af de eksisterende modeller indeholder mange af de samme begreber eller oplysningstyper, selvom de ikke nødvendigvis er blevet kaldt det samme. Termerne varierer, og med denne standard gives et bud på foretrukne samt accepterede termer.

Oplysningstyperne i denne standard er mappet eller gennemgået ift. til følgende modeller.

Mapningsskema i form af et regneark, der kan downloades her:\
<https://data.gov.dk/document/itsystemspecification/v1/mappings/Mapning_it-system_oplysninger.xlsx>

- **Rigsarkivets anmeldelses- og tilsynsskemaer**\
*Skemaer vedr. statslige myndigheders, kommuner og regioners bevaring, kassation og aflevering af arkivalier*\
<https://www.sa.dk/da/offentlig-forvaltning/>\
(her mappes til egenskaber udvalgt af Rigsarkivet)

- **Datatilsynets vejledning om fortegnelse** jf. GDPR.\
*Datatilsynet har offentliggjort en skabelon for en databehandleraftale, der lever op til persondataforordningens minimumskrav. --* Datatilsynet 2018\
<https://www.datatilsynet.dk/media/6567/fortegnelse.pdf>

- **Kommunernes IT OverbliksSystem (OS2Kitos)**\
OS2Kitos er en cloud-baseret løsning, der anvendes af 78 kommuner. OS2Kitos skaber overblik over den samlede kommunale it-portefølje. *OS2Kitos består af 5 moduler: IT understøttelse af organisation, IT Projekter, IT Systemer, IT Kontrakter og IT Rapporter.* -- OS2Kitos Sekretariatet 2018\
[https://www.kitos.dk,](https://www.kitos.dk7/) <https://github.com/os2kitos/kitos>

- **Model for porteføljestyring af statslige it-systemer**\
*Regeringen har i efteråret 2017 ved "Et solidt it-fundament -- Strategi for it-styring i staten" indført en ny model for porteføljestyring af statslige it-systemer.*\
- Ministeriernes kontor for it-styring 2017\
<https://digst.dk/styring/systemstyring/model-for-portefoeljestyring-af-statslige-it-systemer/>  (her mappes til udvalgte egenskaber fra Datagrundlag v2.0)

- **Specifikation af Model for Organisation Version 2.0**\
Formålet med Organisationsmodellen er at tilbyde et fælles sprog for beskrivelse af formelle organer og de elementer, som indgår heri.

<https://arkitektur.digst.dk/sites/default/files/organisationsmodellen_version_2.0.pdf> - OIO 2017 (revideret 2018):\
(her mappes til egenskaber fra kapitlet It-system)

- **KOMBIT IT-system-overblik**

Et overblik over de it-systemer, der udvikles/forvaltes under kontrakt med KOMBIT, samt systemer, der berører disse. KOMBITs systemoverblik er logisk set en delmængde af OS2Kitos, men supplerer yderligere med en lang række informationer om blandt andet snitflader, fysiske instanser og dataadgang. (Datamodel ikke offentligt tilgængelig, modtaget på mail)

- **Systemindberetningsformular (Systemkort ServiceNow)-- IT systemer\
***Ved etablering og installation af nye løsninger hos Statens It sender myndigheden oplysninger om it-systemet til Statens IT via en systemindberetningsformular (ServiceNow Systemkort).* -- Statens-IT 2018: (materiale ikke tilgængelig online men modtaget på mail)

- **SKI-kataloget             **

*Staten og Kommunernes Indkøbsservice (SKI) laver indkøbsaftaler, der samler indkøb på tværs af det offentlige og afløfter udbudspligten, og via SKI-kataloget udstilles oplysninger om hardware- og softwareprodukter --* SKI 2018

<https://skikataloget.ski.dk/ski-kataloget/>

- **Configuration Management DataBase (CMDB)** /**IT Service Management (ITSM)**\
Datamodeller fx ServiceNow og BMC er overordnet blevet undersøgt for genbrugelige elementer.

- **Arkitekturdokumentation**, TOGAF-ArchiMate\
*ArchiMate er en international notationsstandard på enterprisearkitekturniveau, som er optaget som en åben standard under The Open Group. Der indgår forskellige såkaldte lag, hvor applikationslaget (Application Layer) anvendes til at modellere en organisations informationssystemarkitekturer, som det defineres i TOGAF-rammeværket ArchiMate.*

Den overordnede mapning går her ikke på egenskaberne, men på klasserne. Det primære element i applikationslaget (Application Layer) er applikationskomponenten. Dette element anvendes til både at modellere hele it-systemer og de komponenter, der indgår i deri. Standardens 'datasæt' kan mappes til ArchiMates 'dataobjekt', og 'snitflade' kan mappes til 'application interface'.

- **Fællesoffentlig Digital Arkitektur**

I den Fællesoffentlige Digitale Arkitektur (FDA) indgår grundlæggende arkitekturperspektiver, som udgør de tematiske emneområder og kapitler i denne standard. Dog er der pt. ikke medtaget oplysningstyper under perspektivet 'Strategi'.

|

8\. Referencer
==============

 |

Standarder

- [ISO/IEC CD 15288 ](https://www.iso.org/standard/63711.html)"Systems Engineering--- System Life Cycle Processes"

- [ISO/IEC 16350:2015(en) ](https://www.iso.org/obp/ui/#iso:std:iso-iec:16350:ed-1:v1:en)Information technology --- Systems and software engineering --- Application management

- [ISO/IEC TR 10000-1:1998(en)](https://www.iso.org/obp/ui/#iso:std:iso-iec:tr:10000:-1:ed-4:v1:en) "Information technology --- Framework and taxonomy of International Standardized Profiles --- Part 1: General principles and documentation framework"

- ISO/IEC TR 12182:2015 "Systems and software engineering -- Framework for categorization of IT systems and software, and guide for applying it"

- ISO/IEC/IEEE 42010 "Systems and software engineering --- Architecture description "

- ISO/IEC/IEEE DIS "42020 Enterprise, systems and software --- Architecture processes"

- ISO/IEC/IEEE DIS 42030 "Systems and Software Engineering --- Architecture Evaluation"

- ISO/IEC 27002:2013 Information technology -- Security techniques -- Code of practice for information security controls: <https://www.iso.org/standard/54533.html>

- [ITIL -  The Information Technology Infrastructure Library](http://www.itlibrary.org/)

- The TOGAF® Standard, Version 9.2, <https://publications.opengroup.org/standards/togaf/specifications/c182>

- ArchiMate® 3.0.1 Specification <https://publications.opengroup.org/standards/archimate/c179>

Datamodeller / klassifikationer / retningslinjer

- Datamodellen for [OS2Kitos ](https://www.kitos.dk/)(inkl. klassifikation af applikationstyper og forretningstyper)

- OIO specifikation af it-system i [modellen for Organisation](https://arkitektur.digst.dk/sites/default/files/organisationsmodellen_version_2.0.pdf)

- KMD KOSDY-datamodel)

- Datamodellen for ServiceNow ([IT Service Management-delen](https://www.servicenow.com/products/it-service-management.html)) /ITILs (CMDB)

- Statens-IT systemkort

- Datamodellen for BMC

- Retningslinjer for dokumentation og formidling af arkitektur i digitaliseringsprojekter. (baseret på ISO)

- Fællesoffentlig Referencemodel ([FORM](https://arkitektur.digst.dk/rammearkitektur/klassifikationer/form)),\
<https://arkitektur.digst.dk/rammearkitektur/klassifikationer/form>

- Kommunernes Emnesystematik (KLE)

- Service- og Teknologireferencemodel ([STORM](http://arkitekturguiden.digitaliser.dk/storm))

- KOMBIT Rollegalleri: <https://www.kombit.dk/sites/default/files/user_upload/documents/Videnscenter/Eksempel%20fra%20KOMBIT_Rollegalleri%20implementering.pdf>

- Referencearkitektur for deling af data og dokumenter:

https://arkitektur.digst.dk/sites/default/files/20180503_rad_v1.0_-_godkendt_af_sda.pdf

Lovgrundlag og tilhørende vejledninger:

- Bekendtgørelse nr. 183 af 26. januar 2018 om bevaring og kassation af digitalt skabte data og dokumenter <https://www.retsinformation.dk/eli/lta/2018/183>

- Bekendtgørelse nr. 266 af 23. marts 2015 om bevaring og kassation af arkivalier i regionerne\
<https://www.retsinformation.dk/eli/lta/2015/266>

- Vejledning til bekendtgørelse om bevaring og kassation af digitalt skabte data og dokumenter fra kommunerne\
<https://www.sa.dk/wp-content/uploads/2018/04/2007_IT_Vejledning-til-bekendtg%C3%B8relse_h%C3%B8ring-1.pdf>

- Vejledning om bevaring og kassation af arkivalier hos regionerne\
<https://www.sa.dk/wp-content/uploads/2015/06/Vejledning-til-regionsbekendtg%C3%B8relsen_juni-2015.pdf>

- Bekendtgørelse nr. 1007 af 20. august 2010 om arkiveringsversioner  <https://www.retsinformation.dk/eli/lta/2010/1007>

- Vejledning om kvalitetssikring i it-systemer -- Rigsarkivets minimumskrav og anbefalinger\
<https://www.sa.dk/wp-content/uploads/2016/02/Vejledning-om-kvalitetssikring.pdf>

- Arkivhåndbog for statslige myndigheder

- <https://www.kbharkiv.dk/images/files/Arkivering/Arkivhandbogen.pdf>

- Datatilsynets 'Vejledning om fortegnelse' <https://www.datatilsynet.dk/media/6567/fortegnelse.pdf>

- Sikkerhedscirkulæret (Cirkulære om sikkerhedsbeskyttelse af informationer af fælles interesse for landene i NATO eller EU, andre klassificerede informationer samt informationer af sikkerhedsmæssig beskyttelsesinteresse i øvrigt) <https://www.retsinformation.dk/eli/retsinfo/2014/10338>

- Databeskyttelsesloven (Lov om supplerende bestemmelser til forordning om beskyttelse af fysiske personer i forbindelse med behandling af personoplysninger og om fri udveksling af sådanne oplysninger ) <https://www.retsinformation.dk/eli/lta/2018/502>

- GDPR (generel forordning om databeskyttelse):\
<https://eur-lex.europa.eu/legal-content/DA/TXT/HTML/?uri=CELEX:32016R0679&from=EN>

9\. Bilag
=========

Bilag A: Overblik over relevante klassifikationer

-----------------------------------------------------

**Klassifikation KLE:** Distribution:[http://www.kle-online.dk/](http://www.kle-online.dk/soegning)**\
Klassifikation FORM:** Distribution:[http://www.form-online.dk/](http://www.form-online.dk/soegning)\
 Se de overordnede emner herunder:

|

FORM SERVICEOMÅRDER

 |  |

KLE EMNEOMRÅDER

 |
|

[2](http://www.form-online.dk/opgavenoegle/02/)

 |

Internationale aftaler

 |  |

[0](http://www.kle-online.dk/emneplan/00/)

 |

[Kommunens styrelse](http://www.kle-online.dk/emneplan/00/)

 |
|

[3](http://www.form-online.dk/opgavenoegle/03/)

 |

Udenrigstjeneste

 |  |

[1](http://www.kle-online.dk/emneplan/01/)

 |

[Fysisk planlægning og naturbeskyttelse](http://www.kle-online.dk/emneplan/01/)

 |
|

[5](http://www.form-online.dk/opgavenoegle/05/)

 |

Samfundsstruktur

 |  |

[2](http://www.kle-online.dk/emneplan/02/)

 |

[Byggeri](http://www.kle-online.dk/emneplan/02/)

 |
|

[6](http://www.form-online.dk/opgavenoegle/06/)

 |

Samfundsøkonomi, samfundsdigitalisering og statistik

 |  |

[3](http://www.kle-online.dk/emneplan/03/)

 |

[Boliger](http://www.kle-online.dk/emneplan/03/)

 |
|

[8](http://www.form-online.dk/opgavenoegle/08/)

 |

Borgerskab

 |  |

[4](http://www.kle-online.dk/emneplan/04/)

 |

[Parker, fritids-/idrætsanlæg og landskabspleje mv.](http://www.kle-online.dk/emneplan/04/)

 |
|

[10](http://www.form-online.dk/opgavenoegle/10/)

 |

Uddannelse og undervisning

 |  |

[5](http://www.kle-online.dk/emneplan/05/)

 |

[Veje og trafik](http://www.kle-online.dk/emneplan/05/)

 |
|

[12](http://www.form-online.dk/opgavenoegle/12/)

 |

Forskning

 |  |

[6](http://www.kle-online.dk/emneplan/06/)

 |

[Spildevand og vandløb](http://www.kle-online.dk/emneplan/06/)

 |
|

[14](http://www.form-online.dk/opgavenoegle/14/)

 |

Arbejdsmarked

 |  |

[7](http://www.kle-online.dk/emneplan/07/)

 |

[Affald og genanvendelse](http://www.kle-online.dk/emneplan/07/)

 |
|

[16](http://www.form-online.dk/opgavenoegle/16/)

 |

Kultur

 |  |

[8](http://www.kle-online.dk/emneplan/08/)

 |

[Havne og lufthavne](http://www.kle-online.dk/emneplan/08/)

 |
|

[17](http://www.form-online.dk/opgavenoegle/17/)

 |

Fritid og idræt

 |  |

[9](http://www.kle-online.dk/emneplan/09/)

 |

[Miljøbeskyttelse](http://www.kle-online.dk/emneplan/09/)

 |
|

[18](http://www.form-online.dk/opgavenoegle/18/)

 |

Kirke

 |  |

[13](http://www.kle-online.dk/emneplan/13/)

 |

[Forsyning](http://www.kle-online.dk/emneplan/13/)

 |
|

[20](http://www.form-online.dk/opgavenoegle/20/)

 |

Sundhed

 |  |

[14](http://www.kle-online.dk/emneplan/14/)

 |

[Beredskab](http://www.kle-online.dk/emneplan/14/)

 |
|

[24](http://www.form-online.dk/opgavenoegle/24/)

 |

Dagtilbud

 |  |

[15](http://www.kle-online.dk/emneplan/15/)

 |

[Arbejdsmarked og beskæftigelsesindsats](http://www.kle-online.dk/emneplan/15/)

 |
|

[26](http://www.form-online.dk/opgavenoegle/26/)

 |

Social service og omsorg

 |  |

[17](http://www.kle-online.dk/emneplan/17/)

 |

[Folkeskoleundervisning](http://www.kle-online.dk/emneplan/17/)

 |
|

[30](http://www.form-online.dk/opgavenoegle/30/)

 |

Skatter og afgifter

 |  |

[18](http://www.kle-online.dk/emneplan/18/)

 |

[Folkeoplysning og ungdomsskoler](http://www.kle-online.dk/emneplan/18/)

 |
|

[34](http://www.form-online.dk/opgavenoegle/34/)

 |

Erhverv

 |  |

[19](http://www.kle-online.dk/emneplan/19/)

 |

[Kulturhistoriske institutioner](http://www.kle-online.dk/emneplan/19/)

 |
|

[37](http://www.form-online.dk/opgavenoegle/37/)

 |

Miljø

 |  |

[20](http://www.kle-online.dk/emneplan/20/)

 |

[Kulturvirksomhed](http://www.kle-online.dk/emneplan/20/)

 |
|

[38](http://www.form-online.dk/opgavenoegle/38/)

 |

Natur og klima

 |  |

[21](http://www.kle-online.dk/emneplan/21/)

 |

[Biblioteker](http://www.kle-online.dk/emneplan/21/)

 |
|

[40](http://www.form-online.dk/opgavenoegle/40/)

 |

Politi

 |  |

[22](http://www.kle-online.dk/emneplan/22/)

 |

[Regulering af private erhverv](http://www.kle-online.dk/emneplan/22/)

 |
|

[42](http://www.form-online.dk/opgavenoegle/42/)

 |

Retspleje og domstole

 |  |

[23](http://www.kle-online.dk/emneplan/23/)

 |

[Borgerlige forhold](http://www.kle-online.dk/emneplan/23/)

 |
|

[44](http://www.form-online.dk/opgavenoegle/44/)

 |

Straffuldbyrdelse

 |  |

[24](http://www.kle-online.dk/emneplan/24/)

 |

[Erhvervsforhold](http://www.kle-online.dk/emneplan/24/)

 |
|

[46](http://www.form-online.dk/opgavenoegle/46/)

 |

Forsvar

 |  |

[25](http://www.kle-online.dk/emneplan/25/)

 |

[Beskatning](http://www.kle-online.dk/emneplan/25/)

 |
|

[47](http://www.form-online.dk/opgavenoegle/47/)

 |

Redningsberedskab

 |  |

[27](http://www.kle-online.dk/emneplan/27/)

 |

[Social service](http://www.kle-online.dk/emneplan/27/)

 |
|

[52](http://www.form-online.dk/opgavenoegle/52/)

 |

Fysisk planlægning og geodata

 |  |

[28](http://www.kle-online.dk/emneplan/28/)

 |

[Dagtilbud](http://www.kle-online.dk/emneplan/28/)

 |
|

[54](http://www.form-online.dk/opgavenoegle/54/)

 |

Ejendomme og byggeri

 |  |

[29](http://www.kle-online.dk/emneplan/29/)

 |

[Sundhed](http://www.kle-online.dk/emneplan/29/)

 |
|

[56](http://www.form-online.dk/opgavenoegle/56/)

 |

Energi- og vandforsyning

 |  |

[30](http://www.kle-online.dk/emneplan/30/)

 |

[Andre myndigheders opgaver](http://www.kle-online.dk/emneplan/30/)

 |
|

[58](http://www.form-online.dk/opgavenoegle/58/)

 |

Trafikinfrastruktur

 |  |

[32](http://www.kle-online.dk/emneplan/32/)

 |

[Kontante ydelser](http://www.kle-online.dk/emneplan/32/)

 |
|

[59](http://www.form-online.dk/opgavenoegle/59/)

 |

Trafik og transport

 |  |

[54](http://www.kle-online.dk/emneplan/54/)

 |

[Uddannelse](http://www.kle-online.dk/emneplan/54/)

 |
|

[60](http://www.form-online.dk/opgavenoegle/60/)

 |

Myndighedens personale og frivillige

 |  |

[81](http://www.kle-online.dk/emneplan/81/)

 |

[Kommunens personale](http://www.kle-online.dk/emneplan/81/)

 |
|

[62](http://www.form-online.dk/opgavenoegle/62/)

 |

Myndighedens bygninger og arealer

 |  |

[82](http://www.kle-online.dk/emneplan/82/)

 |

[Kommunens ejendomme og lokaler](http://www.kle-online.dk/emneplan/82/)

 |
|

[63](http://www.form-online.dk/opgavenoegle/63/)

 |

Myndighedens driftsmateriel, varer og tjenesteydelser

 |  |

[83](http://www.kle-online.dk/emneplan/83/)

 |

[Kommunens driftsmidler og inventar](http://www.kle-online.dk/emneplan/83/)

 |
|

[65](http://www.form-online.dk/opgavenoegle/65/)

 |

Myndighedens kommunikation og dokumentation

 |  |

[84](http://www.kle-online.dk/emneplan/84/)

 |

[Offentlige valg](http://www.kle-online.dk/emneplan/84/)

 |
|

[67](http://www.form-online.dk/opgavenoegle/67/)

 |

Myndighedens økonomi

 |  |

[85](http://www.kle-online.dk/emneplan/85/)

 |

[Kommunens administrative systemer](http://www.kle-online.dk/emneplan/85/)

 |
|

[68](http://www.form-online.dk/opgavenoegle/68/)

 |

Myndighedens it

 |  |

[86](http://www.kle-online.dk/emneplan/86/)

 |

[Kommunens selvforsyning og fremstillingsvirksomhed](http://www.kle-online.dk/emneplan/86/)

 |
|  |  |  |

[87](http://www.kle-online.dk/emneplan/87/)

 |

[Kommunens arbejdsmiljø](http://www.kle-online.dk/emneplan/87/)

 |
|  |  |  |

[88](http://www.kle-online.dk/emneplan/88/)

 |

[Kommunens indkøb og udbud](http://www.kle-online.dk/emneplan/88/)

 |

**Klassifikation: Offentlig organisationstype:\
**Klassifikation, der består af typer af offentlige organisationer set i forhold til styring og forvaltning i dansk administrativ og fællesoffentlig kontekst\
Forretningsområde: <http://www.form-online.dk/opgavenoegle/05/#05.05>

Juridisk kilde: <https://www.retsinformation.dk/eli/lta/2019/47>

Juridisk kilde: <https://www.retsinformation.dk/eli/lta/2017/319> 

Juridisk kilde: <https://www.retsinformation.dk/eli/lta/2006/653>

Juridisk kilde: <https://www.retsinformation.dk/eli/lta/2014/433>\
Distribution: [https://data.gov.dk/concept/profile/PublicOrganisationTypes.rdf](https://data.gov.dk/rdf2html/index.htm?model=https%3A%2F%2Fdata.gov.dk%2Fconcept%2Fprofile%2FPublicOrganisationTypes.rdf&sheet=transform2RDFreport_da-en.xsl)

|

Foretrukken term

 |

Definition

 |
|

**kommune**

 |

*mindste offentlige forvaltningsenhed, der styres af en kommunalbestyrelse som bekendtgjort i kommunebestyrelsesloven*

 |
|

**region**

 |

*regional forvaltningsenhed, der styres af et regionsråd, og som er bekendtgjort i regionsloven*

 |
|

**statslig myndighed**

 |

*statslig forvaltningsenhed, som administrerer lovgivning eller forvaltning af et bestemt område*

 |
|

**offentlig selvejende institution**

 |

*selvejende institutioner, foreninger, fonde m.v., der*

*1) er oprettet ved lov eller i henhold til lov, og*

*2) er oprettet på privatretligt grundlag, og som udøver offentlig virksomhed af mere omfattende karakter og er undergivet intensiv offentlig regulering, intensivt offentligt tilsyn og intensiv offentlig kontrol*

 |

**Klassifikation: Operationel status\
**Klassifikation, der består af typer af tilstande, et it-system kan have i forhold til ibrugtagning

Forretningsområde: <http://www.form-online.dk/opgavenoegle/68/#68.55.15>\
Kilde: <https://www.hci-itil.com/ITIL_v3/books/3_service_transition/service_transition_ch4_3.html>\
Kilde: <https://digst.dk/styring/systemstyring/model-for-portefoeljestyring-af-statslige-it-systemer/>\
Kilde: Statens-it Systemkort

|

Foretrukken term

 |

Definition

 |
|

**delvist ibrugtaget**

 |

*tilstand, hvor it-system er under opbygning, men allerede delvist ibrugtaget*

 |
|

**fuldt ibrugtaget**

 |

*tilstand, hvor it-systemet er i anvendelse*

 |
|

**udfaset**

 |

*tilstand, hvor it-systemet ikke længere anvendes*

 |

**Klassifikation: It-systemkritikalitetstyper\
**Klassifikation, der består af typer af kritikalitet, ud fra hvorvidt et it-systems driftsforstyrrelser udgør en særlig høj risiko

Forretningsområde: <http://www.form-online.dk/opgavenoegle/#68.55.15.15>

Kilde: <https://digst.dk/styring/systemstyring/model-for-portefoeljestyring-af-statslige-it-systemer/>\
Distribution: [https://data.gov.dk/concept/profile/ITSystemCriticalityTypes.rdf](https://data.gov.dk/rdf2html/index.htm?model=https%3A%2F%2Fdata.gov.dk%2Fconcept%2Fprofile%2FITSystemCriticalityTypes.rdf&sheet=transform2RDFreport_da-en.xsl)

|

Foretrukken term

 |

Definition

 |
|

**forretningskritisk**

 |

*it-system, hvor driftsforstyrrelser kan medføre, at størstedelen af myndighedens medarbejdere ikke kan arbejde, eller at myndigheden vanskeligt kan overholde sine forvaltningsmæssige forpligtelser.*

 |
|

**samfundskritisk**

 |

*it-system, hvor større driftsforstyrrelser resulterer i væsentlige udfordringer for samfundet som helhed i form af økonomiske tab hos stat, virksomheder eller borgere, større misbrug af personfølsomme data og rettigheder, længerevarende nedbrud af kritisk infrastruktur eller reelle trusler for den nationale sikkerhed*

 |
|

**ikke kritisk**

 |

*it-system, hvor større driftsforstyrrelser ikke resulterer i væsentlige udfordringer for samfundet eller for myndighedens forvaltningsmæssige forpligtelser*

 |

**Klassifikationen It-systemmålgrupper:**

Klassifikation, der består af typer af brugere, som et givet it-system henvender sig til

Forretningsområde: <http://www.form-online.dk/opgavenoegle/68/>

Distribution: <https://data.gov.dk/concept/profile/ITSystemTargetGroup.rdf>

|

Foretrukken term

 |

Definition

 |
|

**ekstern målgruppe**

 |

*Målgruppe, hvis medlemmer tilhører den samme organisation, som leverer it-servicen*

 |
|

**intern målgruppe**

 |

*Målgruppe, hvis medlemmer tilhører en anden organisation end den, som leverer it-servicen*

 |

**Klassifikation: It-kontrakttyper\
**Klassifikation, der består af typer af it-kontrakter direkte relevante for it-systemers udvikling, vedligehold, drift og support.\
Forretningsområde: <http://www.form-online.dk/opgavenoegle/68/#68.55.15>

Kilde:  <https://digst.dk/styring/systemstyring/dokumenter-vejledninger-og-vaerktoejer/>\
Kilde:  <https://www.fm.dk/~/media/files/nyheder/pressemeddelelser/2018/10/kommunerne-kan-frigoere-ressourcer-til-velfaerd/5-inspirationskatalog.ashx?la=da>

|

Foretrukken term

 |

Definition

 |
|

**udviklingskontrakt**

 |

*it-kontrakt, som omfatter udvikling af software, inklusive større tilpasninger af standardsystemer og udviklingsopgaver defineret som leveranceprojekter*

 |
|

**vedligeholdelseskontrakt**

 |

*it-kontrakt, som omfatter vedligeholdelse af software*

 |
|

**driftskontrakt**

 |

*it-kontrakt, som omfatter driftsydelser f.eks. serverdrift*

 |
|

**supportkontrakt**

 |

*it-kontrakt, som omfatter supportydelser udover alm. applikationsvedligehold*

 |
|

**licensaftale**

 |

*it-kontrakt, som omfatter køb eller leje af softwarelicenser inkl. løbende abonnement ifm. standardsoftware*

 |

**Klassifikation: It-miljøtyper\
**Klassifikation, der består af typer af it-miljø, som et it-system kan instantieres i

Forretningsområde: <http://www.form-online.dk/opgavenoegle/68/#68.55.15>\
Kilde: <https://en.wikipedia.org/wiki/Deployment_environment>\
Kilde: Statens-it Systemkort\
Kilde: <http://priocept.com/2018/01/30/software-environment-naming/>\
Kilde: <https://docs.microsoft.com/en-us/biztalk/technical-guides/planning-the-development-testing-staging-and-production-environments>

Distribution: [https://data.gov.dk/concept/profile/ITEnvironmentTypes.rdf](https://data.gov.dk/rdf2html/index.htm?model=https%3A%2F%2Fdata.gov.dk%2Fconcept%2Fprofile%2FITEnvironmentTypes.rdf&sheet=transform2RDFreport_da-en.xsl)

|

Foretrukken term

 |

Definition

 |
|

**demonstration**

 |

*miljø, der anvendes til at præsentere udviklingsmuligheder som et proof-of-concept*

 |
|

**udvikling**

 |

*miljø, hvor den initiale softwareudvikling finder sted*

 |
|

**test**

 |

*miljø, der anvendes til afprøvning og kvalitetssikring af ny eller opdateret kode*

 |
|

**præproduktion**

 |

*miljø, der anvendes til sidste test inden ibrugtagning, idet miljøet præcist afspejler det endelige produktionsmiljø*

 |
|

**produktion**

 |

*miljø, hvor it-systemet går live og kan anvendes af slutbrugerne*

 |
|

**disaster recovery**

 |

*miljø, som er et spejl af produktionsmiljøet, og som anvendes ifm. systemgendannelse*

 |
|

**træning**

 |

*miljø, der alene anvendes til oplæring af brugere af it-system*

 |

**Klassifikation: It-systemanskaffelsesstyper\
**Klassifikation der består af typer af anskaffelse af it-systemer\
Eksempler: fx om det er udviklet i egen organisation, bestillingsudviklet (fx ved udbud) eller er anskaffet som et kommercielt (Commercial-of-the-shelf, COTS) eller open source-standardsystem.

Forretningsområde: <http://www.form-online.dk/opgavenoegle/68/#68.55.15>

Kilde: <https://docs.servicenow.com/bundle/london-it-business-management/page/product/application-portfolio-management/task/manage-business-appln.html>

|

Foretrukken term

 |

Definition

 |
|

**egenudviklet      **

 |

*udviklet specielt til formålet i egen organisation*

 |
|

**bestillingsudviklet**

 |

*udviklet specielt til formålet af eksterne leverandører på baggrund af bestilling*

 |
|

**kommercielt**

 |

*udviklet som kommercielt standardsystem *(Commercial-of-the-shelf, COTS)

 |
|

**open-source**

 |

*udviklet med udgangspunkt i software hvis kildekode er frit tilgængeligt og evt. også kan videredistribueres eller ændres iht. "The Open Source Definition"*

 |

**Klassifikation: Personoplysningskategorier\
**Klassifikation, der består af kategorier af personoplysninger ud fra følsomhed, idet der gælder forskellige betingelser og procedurer for behandling af oplysningerne\
Forretningsområde:  <http://www.form-online.dk/opgavenoegle/05/#05.05.12.60>\
Juridisk kilde: <http://data.europa.eu/eli/reg/2016/679/oj>\
Juridisk kilde: <https://www.retsinformation.dk/eli/lta/2018/502>\
Kilde: <https://www.datatilsynet.dk/media/6567/fortegnelse.pdf>

Kommentar: De følsomme oplysninger er udtømmende oplistet i databeskyttelsesforordningen, og alle andre oplysninger er derfor almindelige personoplysninger. Bemærk, at oplysninger om strafbare forhold og personnumre betragtes som almindelige personoplysninger, men databeskyttelsesloven fastsætter særlige regler om disse oplysninger.\
Distribution: [https://data.gov.dk/concept/profile/PersonalDataCategories.rdf ](https://data.gov.dk/rdf2html/index.htm?model=https%3A%2F%2Fdata.gov.dk%2Fconcept%2Fprofile%2FPersonalDataCategories.rdf&sheet=transform2RDFreport_da-en.xsl)

|

Foretrukken term

 |

Definition

 |
|

**1\. almindelige personoplysninger**

 |

*personoplysninger, der ikke er klassificeret som særlige kategorier af oplysninger (følsomme personoplysninger).*

 |
|

**1.1 personnummeroplysninger**

 |

*almindelig personoplysning, om personnummer, som har selvstændigt behandlingshjemmel i databeskyttelseslovens § 11*

 |
|

**1.2 oplysninger om strafbare forhold**

 |

*almindelig personoplysning der vedrører straffedomme og lovovertrædelser eller tilknyttede sikkerhedsforanstaltninger (oplysninger om strafbare forhold er ikke følsomme oplysninger i databeskyttelsesforordningens forstand.)*

 |
|

**2\. følsomme personoplysninger**

 |

*personoplysninger om:*

*o                           Race og etnisk oprindelse*

*o                           Politisk overbevisning*

*o                           Religiøs eller filosofisk overbevisning*

*o                           Fagforeningsmæssige tilhørsforhold*

*o                           Genetiske data*

*o                           Biometriske data med henblik på entydig identifikation*

*o                           Helbredsoplysninger*

*o                           Seksuelle forhold eller seksuel orientering*

 |
|

**3\. ingen personoplysninger**

 |

*Personoplysningskategori, der angiver, at der ikke er informationer om identificerbare fysiske personer tilstede*

 |

**\
Klassifikation: Fortrolighedsgrader iht. sikkerhedscirkulæret (EU/NATO)\
**Klassifikation, der består af grader af fortrolighed, forstået som i hvilket omfang information kan videregives iht. sikkerhedscirkulæret (EU/NATO)\
Forretningsområde: <http://www.form-online.dk/opgavenoegle/68/#68.55.20>\
Kilde: <https://www.retsinformation.dk/eli/retsinfo/2014/10338>\
Distribution [https://data.gov.dk/concept/profile/ConfidentialityTypesNatoEU.rdf](https://data.gov.dk/rdf2html/index.htm?model=https%3A%2F%2Fdata.gov.dk%2Fconcept%2Fprofile%2FConfidentialityTypesNatoEU.rdf&sheet=transform2RDFreport_da-en.xsl)

|

Foretrukken term

 |

Definition

 |
|

**yderst hemmeligt**

 |

*Denne klassifikationsgrad skal anvendes om informationer, hvis videregivelse uden dertil indhentet bemyndigelse ville kunne forvolde Danmark eller landene i NATO eller EU overordentlig alvorlig skade.*

 |
|

**hemmeligt**

 |

*Denne klassifikationsgrad skal anvendes om informationer, hvis videregivelse uden dertil indhentet bemyndigelse ville kunne forvolde Danmark eller landene i NATO eller EU alvorlig skade.*

 |
|

**fortroligt**

 |

*Denne klassifikationsgrad skal anvendes om informationer, hvis videregivelse uden dertil indhentet bemyndigelse ville kunne forvolde Danmark eller landene i NATO eller EU skade.*

 |
|

**til tjenestebrug**

 |

*Denne klassifikationsgrad anvendes om informationer, der ikke må offentliggøres eller komme til uvedkommendes kendskab.*

 |
|

**må offentliggøres**

 |

*Denne klassifikationsgrad anvendes om informationer, som ikke er fortrolige, og som umiddelbart må offentliggøres*

 |

**\
**

**Klassifikation: Fortrolighedsgrad iht. ISO27002**\
Klassifikation af grader af fortrolighed, forstået som i hvilket omfang information kan videregives iht. informationssikkerhedsstandarden ISO/IEC 27002:2013 Information technology -- Security techniques -- Code of practice for information security controls.\
Forretningsområde:  <http://www.form-online.dk/opgavenoegle/68/#68.55.20>\
Kilde:  <https://www.iso.org/standard/54533.html>\
Kilde:  <https://di.dk/SiteCollectionDocuments/DI.Web/Vejledning%20-%20Dataklassifikation%20-%20Final.pdf>   

|

Foretrukken term

 |

Definition

 |
|

**alvorlig indvirkning**

 |

*Offentliggørelse har en alvorlig indvirkning på langsigtede strategiske målsætninger eller sætter organisationens overlevelse på spil*

 |
|

**væsentlig indvirkning**

 |

*Offentliggørelsen har en væsentlig kortsigtet indvirkning på driften eller taktiske målsætninger*

 |
|

**mindre væsentlig indvirkning**

 |

*Offentliggørelse forårsager mindre væsentlige problemer for driften*

 |
|

**ingen indvirkning**

 |

*Offentliggørelse forårsager ingen skade*

 |

**

**

Bilag B: Skabelon til registrering i regneark (udklip)
------------------------------------------------------

### Oversigt over **mulige** **oplysninger** i basisprofilen

|

Basisinformation

 |

Forklaring

 |

Udfyldelseskrav

 |
|

**it-systemidentifikator**

 |

angiv det ID, som entydigt identificerer it-systemet

 |

<<Kan udfyldes>>

 |
|

**it-systemnavn **

 |

angiv it-systemets foretrukne betegnelse\
(fx navn som anført i hovedkontrakten)

 |

<<Skal udfyldes>>

 |
|

**alternativt it-systemnavn**

 |

angiv eventuelt øvrige betegnelser eller kaldenavne for it-systemet

 |

<<Kan udfyldes>>

 |
|

**it-systembeskrivelse**

 |

Beskriv, til hvilket formål it-systemet er taget i brug i organisationen

 |

<<Skal udfyldes>>

 |
|

**operationel status**

 |

angiv, hvilken tilstand it-systemet har i forhold til ibrugtagning

 |

<<Kan udfyldes>>

 |
|

**ibrugtagningsdato**

 |

angiv dato, hvor it-systemet blev taget i brug med fuld eller delvis funktionalitet

 |

<<Kan udfyldes>>

 |
|

**udfasningsdato**

 |

angiv dato, hvor it-systemet blev endeligt blev afviklet

 |

<<Kan udfyldes>>

 |
|

**version**

 |

angiv eventuelt hvilken version der er taget i anvendelse

 |

<<Kan udfyldes>>

 |
|

**kommentar**

 |

angiv eventuelt supplerende bemærkninger eller oplysninger

 |

<<Kan udfyldes>>

 |
|

**indeholder data**

 |

Angiv, om it-systemet indeholder digitalt skabte data

 |

<<Kan udfyldes>>

 |
|

**dokumentationsreference**

 |

angiv reference(r) til dokumentation af it-systemet

 |

<<Kan udfyldes>>

 |
|

Opgaver

 |  |  |
|

**FORM-opgave(r)**

 |

angiv FORM-opgave(r), som it-systemet understøtter

 |

<<Kan udfyldes>>\
(for regioner og statslige administrative enheder)

 |
|

**KLE-emne(r)**

 |

angiv  KLE-emne(r), som it-systemet understøtter

 |

<<Kan udfyldes>>\
(for kommuner)

 |
|

**lovgrundlag**

 |

angiv reference(r) til juridisk ressource, som danner grundlag for systemets anvendelse

 |

<<Kan udfyldes>>

 |
|

**målgruppe(r)**

 |

angivelse af, hvilken gruppe af brugere it-systemet henvender sig til

 |

<<Kan udfyldes>>

 |
|

**kritikalitetstype**

 |

angiv, om it-systemets anvendelse er samfundskritisk, forretningskritisk eller ikke kritisk

 |

<<Kan udfyldes>>

 |
|

Styring

 |  |  |
|

**it-systemejer**

 |

angiv person eller organisation med det oveordnede ansvar for et givent it-systems drift, vedligehold og anvendelse

 |

<<kan udfyldes>>

 |
|

**it-systemforvalter**

 |

angiv organisatorisk enhed eller medarbejder, som administrerer og træffer afgørelser vedrørende tekniske anliggender på vegne af systemejeren

 |

<<Kan udfyldes>>

 |
|

Jura

 |  |  |
|

**kontraktreference(r)**

 |

angiv reference(r) til kontrakt relateret til it-systemets udvikling, vedligehold, drift eller support.

 |

<<Kan udfyldes>>

 |
|

**rettighedshaver**

 |

Organisation, der ejer eller har dispositionsretten over de intellektuelle rettigheder over it-systemets primære softwareprodukt

 |

<<Kan udfyldes>>

 |
|

**udviklingsleverandør**

 |

angiv den primære organisation, der har leveret udviklingsydelser ift. et it-system - herunder udvikling af software, inklusiv større tilpasninger af standardsystemer

 |

<<Kan udfyldes>>

 |
|

**vedligeholdelsesleverandør**

 |

angiv den primære organisation, der leverer vedligeholdelsesydelser ift. et it-system

 |

<<Kan udfyldes>>

 |
|

**driftsleverandør**

 |

angiv den primære organisation, der leverer driftsydelser ift. et it-system

 |

<<Kan udfyldes>>

 |
|

Infrastruktur

 |  |  |
|

**miljøtype**

 |

angiv miljøtypen, it-systemet er ibrugtaget i

 |

<<Kan udfyldes>>

 |
|

Applikation

 |

* (Applikationslaget af et instantieret it-system i et fysisk it-miljø)*

 |  |
|

**produktserie**

 |

angiv navnet på den produktserie, der udgør it-systemets primære softwareprodukt

 |

<<Kan udfyldes>>

 |
|

**udstiller**

 |

angiv det unikke ID for det eller de datasætrepræsentationer, som it-systemet udstiller (reference til Datasætkataloget)

 |

<<Kan udfyldes>>

 |
|

**anvender**

 |

angiv det unikke ID for det eller de datasætrepræsentationer, som it-systemet anvender (reference til Datasætkataloget)

 |

<<Kan udfyldes>>

 |
|

Information

 |

* (Informationslaget af et instantieret it-system i et fysisk it-miljø)*

 |  |
|

**datasætID**

 |

angiv datasættes unikke ID

 |

<<Kan udfyldes>>

 |
|

**dataansvarlig**

 |

angiv den organisation, som har dispositionsretten og træffer afgørelse om, hvordan data skal behandles

 |

<<Kan udfyldes>>

 |
|

**databehandler**

 |

angiv organisation(er), som behandler personoplysninger på vegne af den dataansvarlige

 |

<<Kan udfyldes>>

 |
|

**dataskaber**

 |

angiv den organisation, der har det primære ansvar for tilvejebringelsen af datasættet

 |

<<Kan udfyldes>>

 |
|

**titel**

 |

angiv datasættets navn (det eller de ord, der navngiver datasættet)

 |

<<Kan udfyldes>>

 |
|

**beskrivelse**

 |

beskriv datasættets formål og indhold (fx datasættet indeholder journalsager fra kommune x)

 |

<<Kan udfyldes>>

 |
|

**versionsnummer**

 |

angiv eventuelt datasættets versionsnummer

 |

<<Kan udfyldes>>

 |
|

**første datatilføjelse**

 |

angiv dato for første datatilføjelse

 |

<<Kan udfyldes>>

 |
|

**sidste datatilføjelse**

 |

angiv dato for sidste datatilføjelse

 |

<<Kan udfyldes>>

 |
|

**personoplysningskategori**

 |

angiv, om it-systemet indeholder almindelige personoplysninger, følsomme personoplysninger eller oplysninger om strafbare forhold (flere skal kunne vælges - udestår pt)

 |

<<Kan udfyldes>>

 |
|

**fortrolighedsgrad iht.\
        sikkerhedscirkulæret**

 |

angiv, i hvilket omfang information kan videregives iht. sikkerhedscirkulæret (EU/NATO)

 |

<<Kan udfyldes>>

 |
|

**fortrolighedsgrad iht.\
         ISO 27001**

 |

angiv, i hvilket omfang information kan videregives iht. informationssikkerhedsstandarden ISO 27002

 |

<<Kan udfyldes>>

 |

Bilag C: Eksempel maskinlæsbart format (RDF/XML)

----------------------------------------------------

(Her RDF-XML og Turtle, men andre serialiseringer mulige, herunder JSON-LD)\
EKSEMPELOUTPUT I TURTLE (Acadre anvendt i kommune X)\
NB: Ikke alle egenskaber medtaget i eksemplet

@prefix skos: <http://www.w3.org/2004/02/skos/core#> .

@prefix dc: <http://purl.org/dc/terms/> .

@prefix sys: <https://data.gov.dk/model/core/itsystem#> .

@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .

@prefix infra: <https://data.gov.dk/model/core/infrastructure#> .

@prefix dcat: <http://www.w3.org/ns/dcat#> .

@prefix dcat-dk: <https://data.gov.dk/model/core/dcat-dk#> .

<https://EXAMPLEURI1>

  a <https://data.gov.dk/model/core/itsystem#ITSystem> ;

 skos:prefLabel "Acadre "@da ;

  skos:altLabel "Acadre CM"@da ;

  dc:description "Acadre anvendes i kommune X til sagsstyring og ledelsesrapportering"@da ;

 sys:inUseFromDate "2019-01-01"^^xsd:date ;

  sys:hasApplicationPurposeFORM <http://www.form-online.dk/opgavenoegle/65/#65.50.05> ;

  sys:hasApplicationPurposeKLE <http://www.kle-online.dk/emneplan/85/#_85.02.10> ;

  sys:hasTargetGroup <https://data.gov.dk/model/classification/itsystemcriticalitytype#employees> ;

  sys:hasCriticality <https://data.gov.dk/model/classification/itsystemcriticalitytype#CriticalForBusiness> ;

  sys:hasAquisitionType <https://data.gov.dk/model/classification/itsystemaquisitiontype#Commercial-off-the-shelf> ;

  infra:instanceOfProductInSeries "Acadre CM"^^xsd:string ;

  sys:containsData True ;

  dc:hasPart <https://EXAMPLEURI2> .

<https://EXAMPLEURI3>

  a sys:InstantiatedITSystem ;

  sys:actsAs <https://data.gov.dk/model/classification/itenvironmenttype#Production> ;

  sys:instantiationOf <https://EXAMPLEURI1> ;

  sys:producesDataset <https://EXAMPLEURI4> .

<https://EXAMPLEURI2>

  a dcat:Dataset ;

  dcat-dk:dataResponsibleOrganisation "Kommune x"@da ;

  dcat-dk:personalDataCategory <https://data.gov.dk/model/classification/PersonalDataCategory#GeneralPersonalData> ;

 dc:description "Journalsager fra komnune x"@da ;

EKSEMPELOUTPUT I RDF/XML

<?xml version="1.0" encoding="utf-8"?><rdf:RDF xmlns:xsd="http://www.w3.org/2001/XMLSchema#"

  xmlns:rdf="http://www.w3.org/1999/02/22-rdf-syntax-ns#"

  xmlns:rdfs="http://www.w3.org/2000/01/rdf-schema#"

  xmlns:owl="http://www.w3.org/2002/07/owl#"

  xmlns:dc11="http://purl.org/dc/elements/1.1/"

  xmlns:voaf="http://purl.org/vocommons/voaf#"

  xmlns:dcterms="http://purl.org/dc/terms/"

  xmlns:dc="http://purl.org/dc/terms/"

  xmlns:dct="http://purl.org/dc/terms/"   

  xmlns:dcat="http://www.w3.org/ns/dcat#"

  xmlns:skos="http://www.w3.org/2004/02/skos/core#"

  xmlns:prov="http://www.w3.org/ns/prov#"

  xmlns:adms="http://www.w3.org/ns/adms#"

  xmlns:cv="http://data.europa.eu/m8g/"

  xmlns:eli="http://data.europa.eu/eli/ontology#"

  xmlns:schema="http://schema.org/"

  xmlns:dcat-dk="https://data.gov.dk/model/core/dcat-dk#" 

  xmlns:sys="https://data.gov.dk/model/core/itsystem#"

  xmlns:infra="https://data.gov.dk/model/core/infrastructure#"  >

<!-- IT-SYSTEM -->                   

<rdf:Description rdf:about="https://EXAMPLEURI1">

<rdf:type rdf:resource="https://data.gov.dk/model/core/itsystem#ITSystem"/>

<https://EXAMPLEURI2>

  a dcat:Dataset ;

  dcat-dk:dataResponsibleOrganisation "Kommune x"@da ;

  dcat-dk:personalDataCategory <https://data.gov.dk/model/classification/PersonalDataCategory#GeneralPersonalData> ;

 dc:description "Journalsager fra komnune x"@da ;

<skos:prefLabel xml:lang="da">Acadre </skos:prefLabel>

<skos:altLabel xml:lang="da">Acadre CM</skos:altLabel>

<dct:description xml:lang="da">Acadre anvendes i kommune X til sagsstyring og ledelsesrapportering</dct:description>

<sys:inUseFromDate rdf:datatype="http://www.w3.org/2001/XMLSchema#date">2019-01-01</sys:inUseFromDate>

<sys:hasApplicationPurposeFORM rdf:resource="http://www.form-online.dk/opgavenoegle/65/#65.50.05"/>

<sys:hasApplicationPurposeKLE rdf:resource="http://www.kle-online.dk/emneplan/85/#_85.02.10"/>

<sys:hasCriticality rdf:resource="https://data.gov.dk/model/classification/itsystemcriticalitytype#CriticalForBusiness"/>

<sys:hasAquisitionType rdf:resource="https://data.gov.dk/model/classification/itsystemaquisitiontype#Commercial-off-the-shelf"/>

<infra:instanceOfProductInSeries rdf:datatype="http://www.w3.org/2001/XMLSchema#string">Acadre CM</infra:instanceOfProductInSeries>

<sys:containsData rdf:datatype="http://www.w3.org/2001/XMLSchema#boolean">True</sys:containsData>

</rdf:Description>

<!-- IT-SYSTEMETS DATAINDHOLD (ET LOGISK DATASÆT)--> 

<rdf:Description rdf:about="https://EXAMPLEURI2">

<rdf:type rdf:resource="http://www.w3.org/ns/dcat#Dataset"/>

<dcat-dk:dataResponsibleOrganisation xml:lang="da">Kommune x</dcat-dk:dataResponsibleOrganisation>

<dcat-dk:personalDataCategory rdf:resource="https://data.gov.dk/model/classification/PersonalDataCategory#GeneralPersonalData"/>              

<dct:description xml:lang="da">Journalsager fra komnune x</dct:description>            

</rdf:Description>

<!-- IT-SYSTEMETS FYSISKE INSTANTIERING I ET IT-MILJØ -->

<rdf:Description rdf:about="https://EXAMPLEURI3">

    <rdf:type rdf:resource="https://data.gov.dk/model/core/itsystem#InstantiatedITSystem"/>

    <sys:actsAs rdf:resource="https://data.gov.dk/model/classification/itenvironmenttype#Production"/>

    <sys:instantiationOf rdf:resource="https://EXAMPLEURI1"/>

</rdf:Description>

</rdf:RDF>

Bilag D: Om datamodellen
------------------------

UML-modellerne er udstillet på nedenstående link[[24]](file:///C:/Users/b025870/Desktop/Standard%20for%20beskrivelse%20af%20it-systemer%20-%20Basisprofil_CLA.docx#_ftn24):\
<http://data.gov.dk/document/itsystemspecification/v1/uml/>

I det følgende gives en overordnet beskrivelse af modellens indhold:

Et it-system indgår ofte i en organisations it-systemportefølje for at understøtte en proces digitalt. For offentlige myndigheder vil it-systemet typisk have en relation til den forvaltningsopgave, som myndigheden udfører, samt det relaterede lovgrundlag. It-systemet kan anvendes internt i myndigheden eller være målrettet eksterne brugere. Det kan også angives, hvorvidt et it-systems anvendelse er forretningskritisk, samfundskritisk eller ikke kritisk.

Et it-system kan have mange forskellige relationer til aktører, som hver især har en særlig interesse i systemet, og som dermed udgør systemets interessenter, fx it-systemejer og it-systemforvalter.

Afhængig af hvordan it-systemet er anskaffet og taget i brug vil it-systemet have relationer til en række forskellige leverandører gennem kontraktforhold mellem ordregiver og leverandør om fx udvikling, vedligehold og drift. Er it-systemet anskaffet som et standardsystem i form af et softwareprodukt, kan rettighedshaver af produktet angives. Det er også muligt at angive den produktserie som produktet tilhører.

Det kan også være relevant at referere til dokumenter, der beskriver kravene, funktionaliteten, arkitekturen, anvendelsen, driften eller vedligeholdelsen af et it-system.

Et givet it-system kan instantieres i forskellige it-miljøer, fx et testmiljø eller et produktionsmiljø.

De data som logisk set er en del af it-systemet, kan betragtes som et datasæt. Disse datasæt bør beskrives på en ensartet måde med oplysninger om fx beskrivelse, dataansvarlig, personoplysningskategori, fortrolighedsgrad m.fl. Og konkrete fysiske repræsentationer af datasættet kan også forsynes med ensartede oplysninger ifm. udstilling som download eller via dataservices.

Oversigt over UML-modellens anvendelsesprofil, kernemodeller og klassifikationsmodeller

- Anvendelsesprofilen:

o [*IT System AP (Basic Profile)*](https://data.gov.dk/document/itsystemspecification/v1/uml/)

o [*IT System AP (Archive Profile)*](https://data.gov.dk/document/itsystemspecification/v1/uml/)*

*

- Anvendte kernemodeller

o [*Vokabular for it-system (SYS)*](https://data.gov.dk/rdf2html/index.htm?model=https%3A%2F%2Fdata.gov.dk%2Fmodel%2Fcore%2Fitsystem.rdf&sheet=transform2RDFreport_da-en.xsl)

o [*Vokabular for digital arkivering (ARCHV)*](https://data.gov.dk/rdf2html/index.htm?model=https%3A%2F%2Fdata.gov.dk%2Fmodel%2Fcore%2Fdigitalarchival.rdf&sheet=transform2RDFreport_da-en.xsl)

o [*Data Catalog Vocabulary (DCAT)*](https://www.w3.org/TR/vocab-dcat-2/)

o [*Simple Knowledge Organization System (SKOS)*](https://www.w3.org/TR/skos-primer/)

o [*European Legislation Identifier (ELI)*](http://data.europa.eu/eli/ontology)

o [*Financial Industry Business Ontology (FIBO)*](https://spec.edmcouncil.org/fibo/)

o [*Core Vocabulary (CV)*](http://data.europa.eu/m8g/)

o [*Dublin Core Terms (DCT**)*](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/)

o [*Organization Ontology (ORG**)*](https://www.w3.org/TR/vocab-org/)

o [*Core Public Service Vocabulary (*](https://joinup.ec.europa.eu/solution/core-public-service-vocabulary)*CPOV)*

o [*Friend of A Friend (FOAF)*](http://xmlns.com/foaf/spec/)

o [*SCHEMA.org (SCHEMA)*](https://schema.org/)*

*

- Anvendte klassifikationsmodeller

o *Forvaltningsopgavetype (Public Administrative Task Type) -- (*[*FORM*](http://www.form-online.dk/soegning) *&* [*KLE*](http://www.kle-online.dk/soegning)*)*

o [*Operationel status (Operational Status)*](https://data.gov.dk/rdf2html/index.htm?model=https%3A%2F%2Fdata.gov.dk%2Fconcept%2Fprofile%2FOperationalStatuses.rdf&sheet=transform2RDFreport_da-en.xsl)

o [*IT-miljøtype*](https://data.gov.dk/rdf2html/index.htm?model=https%3A%2F%2Fdata.gov.dk%2Fconcept%2Fprofile%2FITEnvironmentTypes.rdf&sheet=transform2RDFreport_da-en.xsl)* (IT Environment Type)*

o [*Fortrolighedsgrad (Data Confidentiality Type)*](https://data.gov.dk/rdf2html/index.htm?model=https%3A%2F%2Fdata.gov.dk%2Fconcept%2Fprofile%2FConfidentialityTypesNatoEU.rdf&sheet=transform2RDFreport_da-en.xsl)

o [*Personoplysningskategori (Personal Data Category)*](https://data.gov.dk/rdf2html/index.htm?model=https%3A%2F%2Fdata.gov.dk%2Fconcept%2Fprofile%2FPersonalDataCategories.rdf&sheet=transform2RDFreport_da-en.xsl)

o [*IT-systemkritikalitetstype (IT System Criticality Type)*](https://data.gov.dk/rdf2html/index.htm?model=https%3A%2F%2Fdata.gov.dk%2Fconcept%2Fprofile%2FITSystemCriticalityTypes.rdf&sheet=transform2RDFreport_da-en.xsl)

o *Målgruppe (Target Group)*

o *IT-systemkontrakttype (IT System Contract Type)*

Bilag E: UML-diagram: SYS-AP
----------------------------

**Namespace**: https://data.gov.dk/model/profile/itsystemap#,

**Modelnavn **(label): Anvendelsesprofil for it-systemer (SYS-AP)

**Modelansvarlig **(responsibleEntity): Digitaliseringsstyrelsen

**Versionnummer **(versionInfo): 1.0.1

**Seneste opdateringsdato** (dateModified): 11-11-2019

**Modelstatus **(modelStatus): Development

**Godkendelsesstatus **(approvalStatus): Afventer godkendelse\
**Modelomfang** (modelScope): Anvendelsesmodel

**Forretningsområde **(theme): [06.38.10.10 Arkitektur for den digitale infrastruktur](http://www.form-online.dk/opgavenoegle/06/#06.38.10.10)\
**Afledt af** (wasDerivedFrom): [https://data.gov.dk/model/concept/itsystem#](https://data.gov.dk/model/concept/itsystem)

**Kommentar **(comment):  Denne generelle anvendelsesprofil vil kunne anvendes til etablere et overordnet overblik og standardisere indsamlingen af oplysninger.

Bilag F: UML-diagram: SYS
-------------------------

**Namespace**: https://data.gov.dk/model/core/itsystem#,

**Modelnavn **(label): Vokabular til it-system (SYS)

**Modelansvarlig **(responsibleEntity): Digitaliseringsstyrelsen

**Versionnummer **(versionInfo): 1.0.0

**Seneste opdateringsdato** (dateModified): 11-11-2019

**Modelstatus **(modelStatus): Development

**Godkendelsesstatus **(approvalStatus): Afventer godkendelse

**Modelomfang** (modelScope): Kernemodel

**Forretningsområde **(theme): [06.38.10.10 Arkitektur for den digitale infrastruktur](http://www.form-online.dk/opgavenoegle/06/#06.38.10.10)\
**Afledt af** (wasDerivedFrom): [https://data.gov.dk/model/concept/itsystem#](https://data.gov.dk/model/concept/itsystem)

**Kommentar **(comment):  

**

**

Bilag G: Begrebsliste til Basisprofilen (SYS-AP)
------------------------------------------------

|

**Foretrukken dansk term**

 |

**Definition**

 |

**Juridisk kilde**

 |

**Kilde**

 |

**Tilhører emneområde**

 |

**Foretrukken engelsk term**

 |
| --- | --- | --- | --- | --- | --- |
|

**brugergrænseflade**

 |

*snitflade, hvorigennem mennesker kan få adgang til et it-system, som den viser sig i udformningen af skærmbilleder og skærmdialog*

 |  |  |

https://data.gov.dk/model/concept/itsystem#

 |

user interface

 |
|

**dataansvarlig**

 |

*organisation, som har det administrative ansvar for data*

 |  |  |  |

data responsible organisation

 |
|

**databehandler**

 |

*en fysisk eller juridisk person, en offentlig myndighed, en institution eller et andet organ, der behandler personoplysninger på den dataansvarliges vegne*

 |

http://data.europa.eu/eli/reg/2016/679/oj

 |  |

https://data.gov.dk/model/concept/dataprotection#

 |

data processor

 |
|

**dataservice**

 |

*Snitflade, hvorigennem it-systemer kan få adgang til et eller flere datasæt eller databehandlingsfunktioner*

 |  |

https://www.w3.org/TR/vocab-dcat/

 |

https://data.gov.dk/model/concept/dataset#

 |

data service

 |
|

**dataskaber**

 |

*organisation, der har det primære ansvar for tilvejebringelsen af datasættet*

 |  |

<https://joinup.ec.europa.eu/solution/dcat-application-profile-data-portals-europe>

 |

https://data.gov.dk/model/concept/dataset#

 |

data creator

 |
|

**datasletning**

 |

*sletning af alle link til eller kopier eller gengivelser af de pågældende personoplysninger*

 |

http://data.europa.eu/eli/reg/2016/679/oj

 |  |

https://data.gov.dk/model/concept/digitalarchival#

 |

data erasure

 |
|

**datasletningsfrist**

 |

*dato for, hvornår data i systemet forventes at skulle være slettet forinden*

 |

https://www.datatilsynet.dk/media/6560/dataansvarlige-og-databehandlere.pdf

 |

https://os2.eu/sites/default/files/documents/notat_om_felter_til_registrering_af_arkiveringsdata_i_kitos.pdf

 |

https://data.gov.dk/model/concept/digitalarchival#

 |

data erasure deadline

 |
|

**datasæt**

 |

*samling af data sammenstillet af en enkelt aktør*

 |  |

https://www.w3.org/TR/vocab-dcat/,

 |

https://data.gov.dk/model/concept/dataset#

 |

dataset

 |
|

**datasætrepræsentation**

 |

*specifik fysisk repræsentation af et datasæt*

 |  |

https://www.w3.org/TR/vocab-dcat/,

 |

https://data.gov.dk/model/concept/datasetdistribution#

 |

distribution

 |
|

**den registrerede**

 |

*person, om hvem oplysninger behandles*

 |

http://data.europa.eu/eli/reg/2016/679/oj

 |

Referencearkitektur for deling af data og dokumenter

 |

https://data.gov.dk/model/concept/dataprotection#

 |

data subject

 |
|

**forgængersystem**

 |

*system, der tidligere har varetaget samme funktion*

 |

https://www.retsinformation.dk/eli/lta/2010/1007

 |  |

https://data.gov.dk/model/concept/itsystem#

 |

predessor system

 |
|

**fortrolighedsgrad**

 |

*grad af fortrolighed, forstået som i hvilket omfang information kan videregives*

 |  |  |

https://data.gov.dk/model/concept/informationsecurity#

 |

confidentiality type

 |
|

**fortrolighedsgrad iht. ISO 27002**

 |

*fortrolighedsgrad, forstået som i hvilket omfang information kan videregives iht. informationssikkerhedsstandarden ISO/IEC 27002*

 |  |

https://www.iso.org/standard/54533.html

 |

https://data.gov.dk/model/concept/informationsecurity#

 |

ISO 27002 Data Classification

 |
|

**fortrolighedsgrad iht. Sikkerhedscirkulæret**

 |

*fortrolighedsgrad, forstået som i hvilket omfang information kan videregives iht. sikkerhedscirkulæret (Nato & EU Dataklassifikation)*

 |

https://www.retsinformation.dk/eli/retsinfo/2014/10338

 |  |

https://data.gov.dk/model/concept/informationsecurity#

 |

Nato & EU Data Classification

 |
|

**informationssystem**

 |

*system til indsamling, organisering, lagring og kommunikation af viden*

 |  |  |

https://data.gov.dk/model/concept/itsystem#

 |

information system

 |
|

**instantieret it-system**

 |

*fysisk instans af et it-system i et bestemt it-miljø*

 |  |  |

https://data.gov.dk/model/concept/itsysteInstancem#

 |

IT system instance

 |
|

**it-leverandør**

 |

*aktør, som leverer it-tjenester*

 |  |  |

https://data.gov.dk/model/concept/itsystem#

 |

IT supplier

 |
|

**it-miljøtype**

 |

*type af miljø, som et it-system kan ibrugtages i*

 |  |

https://en.wikipedia.org/wiki/Deployment_environment\
Statens-IT Systemkort

 |

https://data.gov.dk/model/concept/itsystem#

 |

environment type

 |
|

**it-system**

 |

*system, der består af digitale informationsteknologier*

 |  |

https://www.iso.org/standard/63711.html

 |

https://data.gov.dk/model/concept/itsystem#

 |

IT system

 |
|

**it-systemmålgruppe**

 |

*gruppe af brugere, som et givent it-system henvender sig til*

 |  |  |

https://data.gov.dk/model/concept/itsystem#

 |

IT system target group

 |
|

**it-systemejer**

 |

*person eller organisation med det overordnede ansvar for et givet it-systems drift, vedligehold og anvendelse*

 |  |

https://digst.dk/styring/systemstyring/model-for-portefoeljestyring-af-statslige-it-systemer/

 |

https://data.gov.dk/model/concept/itsystem#

 |

IT system owner

 |
|

**it-systemforvalter**

 |

*organisatorisk enhed eller medarbejder, som administrerer og træffer afgørelser vedrørende tekniske anliggender på vegne af systemejeren*

 |  |  |

https://data.gov.dk/model/concept/itsystem#

 |

IT system manager

 |
|

**kontrakt**

 |

*frivillig juridisk gældende aftale mellem to eller flere parter*

 |  |

https://spec.edmcouncil.org/fibo/FND/Agreements/Contracts/

 |

https://data.gov.dk/model/concept/contract#

 |

contract

 |
|

**kritikalitetstype**

 |

*type af* *kritikalitet ud fra hvorvidt et it-systems driftsforstyrelser udgør en særlig høj risiko*

 |  |

https://digst.dk/styring/systemstyring/model-for-portefoeljestyring-af-statslige-it-systemer/

 |

https://data.gov.dk/model/concept/itsystem#

 |

criticality type

 |
|

**leverandør**

 |

*kontraktpart, der har rollen som leverandør*

 |  |

https://spec.edmcouncil.org/fibo/FND/Agreements/Contracts/

 |

https://data.gov.dk/model/concept/contract#

 |

counter party

 |
|

**offentlig forvaltningsopgavetype**

 |

*type af opgave, der udføres af offentlige organisationer*

 |  |

<https://arkitektur.digst.dk/rammearkitektur/datastandarder/anvendelsesprofil-organisationer>

 |

https://data.gov.dk/model/concept/organisation#

 |

public administrative task type

 |
|

**ordregiver**

 |

*kontraktpart, der har rollen som ordregiver*

 |  |

https://spec.edmcouncil.org/fibo/FND/Agreements/Contracts/

 |

https://data.gov.dk/model/concept/contract#

 |

principal party

 |
|

**organisation**

 |

*samling mennesker, der er organiseret i et fællesskab eller anden social, kommerciel eller politisk struktur*

 |  |

http://www.w3.org/ns/org#;\
<https://arkitektur.digst.dk/rammearkitektur/datastandarder/anvendelsesprofil-organisationer>

 |

https://data.gov.dk/model/concept/organisation#

 |

organization

 |
|

**persondataansvarlig**

 |

*en fysisk eller juridisk person, en offentlig myndighed, en institution eller et andet organ, der alene eller sammen med andre afgør, til hvilke formål og med hvilke hjælpemidler der må foretages behandling af personoplysninger*

 |

http://data.europa.eu/eli/reg/2016/679/oj

 |

https://w3id.org/GDPRtEXT#Processor

 |

https://data.gov.dk/model/concept/dataprotection#

 |

controller

 |
|

**personoplysningskategori**

 |

*kategori af personoplysninger set i forhold til følsomhed, idet der gælder forskellige betingelser og procedurer for behandling af oplysningerne*

 |

http://data.europa.eu/eli/reg/2016/679/oj

 |

https://www.datatilsynet.dk/media/6567/fortegnelse.pdf

 |

https://data.gov.dk/model/concept/dataprotection#

 |

personal data category

 |
|

**personoplysningsunderkategori**

 |

*præcisering af, hvilken underkategori af persondata systemet indeholder*

 |  |

notat om GDPR-modul i KITOS

 |

https://data.gov.dk/model/concept/dataprotection#

 |

personal data subcategory

 |
|

**produktserie**

 |

*produkter eller varer markedsført som en serie*

 |  |  |

https://data.gov.dk/model/concept/itsystem#

 |

product series

 |
|

**retskilde**

 |

*intellektuelt værk, der fastsætter juridiske regler og retsbestemmelser*

 |  |

<https://publications.europa.eu/en/web/eu-vocabularies/model/-/resource/dataset/eli>

 |

https://data.gov.dk/model/concept/legalresource#

 |

legal resource

 |
|

**sagsområde**

 |

*kategori af sager iht. bekendtgørelser for bevaring og kassation af digitale arkivalier på det regionale eller kommunale område*

 |

https://www.retsinformation.dk/eli/lta/2003/591;

https://www.retsinformation.dk/eli/lta/2015/266; https://www.retsinformation.dk/eli/lta/2018/183; 

 |

https://www.sa.dk/da/offentlig-forvaltning/kommuner-og-regioner/bevaring-kassation-it-systemer/

 |

https://data.gov.dk/model/concept/digitalarchival#

 |

case area

 |
|

**system**

 |

*kombination af interagerende elementer, der er organiseret for at opnå et eller flere erklærede formål*

 |  |

ISO/IEC 15288: https://www.iso.org/standard/63711.html

 |

https://data.gov.dk/model/concept/system#

 |

system

 |
|

**systemdokumentation**

 |

*skriftligt materiale, der redegør for et bestemt aspekt af it-systemet, herunder forretningskrav, funktionalitet, arkitektur, drift, vedligeholdelse og anvendelse*

 |  |  |

https://data.gov.dk/model/concept/itsystem#

 |

system documentation

 |
|

**anskaffelsestype**

 |

*type af anskaffelse af et it-system*

 |  |

https://docs.servicenow.com/bundle/london-it-business-management/page/product/application-portfolio-management/task/manage-business-appln.html

 |

https://data.gov.dk/model/concept/itsystem#

 |

IT system aquisition type

 |

(se metadata og begrebsdiagrammer online:  <https://data.gov.dk/document/itsystemspecification/v1/uml/>)

|

Dette dokument udgør en fællesoffentlig standard for beskrivelse af offentlige myndigheders it-systemer. Der indsamles oplysninger om offentlige it-systemer mange steder, så der er god værdi i at standardisere den måde hvorpå it-systemer beskrives og dermed understøtte højere genbrug og kvalitet i de indsamlede oplysninger.

 |
|

arkitektur.digst.dk

 |

* * * * *

[[1]](file:///C:/Users/b025870/Desktop/Standard%20for%20beskrivelse%20af%20it-systemer%20-%20Basisprofil_CLA.docx#_ftnref1)   Et arbejder hvis mål nu eksisterer i form af 'Standard for beskrivelse af it-systemer -- Arkivprofil'

[[2]](file:///C:/Users/b025870/Desktop/Standard%20for%20beskrivelse%20af%20it-systemer%20-%20Basisprofil_CLA.docx#_ftnref2) https://digst.dk/strategier/strategi-for-it-styring-i-staten/

[[3]](file:///C:/Users/b025870/Desktop/Standard%20for%20beskrivelse%20af%20it-systemer%20-%20Basisprofil_CLA.docx#_ftnref3) https://www.datatilsynet.dk/media/6567/fortegnelse.pdf

[[4]](file:///C:/Users/b025870/Desktop/Standard%20for%20beskrivelse%20af%20it-systemer%20-%20Basisprofil_CLA.docx#_ftnref4) ISO/IEC 15288 (Systems and software engineering -- System life cycle processes)  

[[5]](file:///C:/Users/b025870/Desktop/Standard%20for%20beskrivelse%20af%20it-systemer%20-%20Basisprofil_CLA.docx#_ftnref5) Begrebet 'it-system' er altså en specialisering af 'system' fra ISO 15288, idet der fokuseres på IT-aspektet.\
Det vurderes derudover at definitionen er tråd med ISO/IEC TR 10000-1:1998(en)

Information technology --- Framework and taxonomy of International Standardized Profiles og ISO/IEC TR 12182:2015 (Systems and software engineering -- -- Framework for categorization of IT systems and software, and guide for applying it .

[[6]](file:///C:/Users/b025870/Desktop/Standard%20for%20beskrivelse%20af%20it-systemer%20-%20Basisprofil_CLA.docx#_ftnref6) Klassifikationer beskrives iht. anvendelsesprofil for klassifikation: <https://arkitektur.digst.dk/rammearkitektur/datastandarder/anvendelsesprofil-klassifikationer>

[[7]](file:///C:/Users/b025870/Desktop/Standard%20for%20beskrivelse%20af%20it-systemer%20-%20Basisprofil_CLA.docx#_ftnref7) <https://arkitektur.digst.dk/mandat-og-styring/hvidbog-om-faellesoffentlig-digital-arkitektur>

[[8]](file:///C:/Users/b025870/Desktop/Standard%20for%20beskrivelse%20af%20it-systemer%20-%20Basisprofil_CLA.docx#_ftnref8) https://skikataloget.ski.dk/ski-kataloget/

[[9]](file:///C:/Users/b025870/Desktop/Standard%20for%20beskrivelse%20af%20it-systemer%20-%20Basisprofil_CLA.docx#_ftnref9) Common Procurement Vocabulary er et fælles referencesystem for udbudte opgaver i EU https://udbudsportalen.dk/cpv-koder/

[[10]](file:///C:/Users/b025870/Desktop/Standard%20for%20beskrivelse%20af%20it-systemer%20-%20Basisprofil_CLA.docx#_ftnref10) United Nations Standard Product and Services Code) er et internationalt klassifikationssystem for varer og tjenesteydelser. http://unspsc.gs1.dk/find-din-kode/

[[11]](file:///C:/Users/b025870/Desktop/Standard%20for%20beskrivelse%20af%20it-systemer%20-%20Basisprofil_CLA.docx#_ftnref11) STORM er en taksonomi over it-servicestyper. På samme måde som FORM kategoriserer og beskriver det offentliges opgaver, er STORM udviklet til at give en overordnet klassifikation og beskrivelse af de it-systemer, der bruges i den offentlige forvaltning. STORM vedligeholdes ikke pt. http://arkitekturguiden.digitaliser.dk/storm og det er projektgruppens vurdering at den ikke umiddelbart kan tages i anvendelse i denne standard. Flere interessenter har dog i forbindelse med standardens udarbejdelse udtrykt et behov for en sådan klassifikation ifm. øvrige anvendelser. Dette bør analyseres nærmere.

[[12]](file:///C:/Users/b025870/Desktop/Standard%20for%20beskrivelse%20af%20it-systemer%20-%20Basisprofil_CLA.docx#_ftnref12) <http://data.europa.eu/eli/reg/2016/679/oj>:\
  <https://www.retsinformation.dk/eli/lta/2018/502>

[[13]](file:///C:/Users/b025870/Desktop/Standard%20for%20beskrivelse%20af%20it-systemer%20-%20Basisprofil_CLA.docx#_ftnref13) <https://www.datatilsynet.dk/media/6560/dataansvarlige-og-databehandlere.pdf>

[[14]](file:///C:/Users/b025870/Desktop/Standard%20for%20beskrivelse%20af%20it-systemer%20-%20Basisprofil_CLA.docx#_ftnref14) https://www.omg.org/hot-topics/finance.htm   & https://spec.edmcouncil.org/fibo/FND/Agreements/Contracts

[[15]](file:///C:/Users/b025870/Desktop/Standard%20for%20beskrivelse%20af%20it-systemer%20-%20Basisprofil_CLA.docx#_ftnref15) https://arkitektur.digst.dk/sites/default/files/20180503_rad_v1.0_-_godkendt_af_sda.pdf

[[16]](file:///C:/Users/b025870/Desktop/Standard%20for%20beskrivelse%20af%20it-systemer%20-%20Basisprofil_CLA.docx#_ftnref16) https://www.w3.org/TR/vocab-dcat/\
    (Bemærk at DCAT anvender et snævrere datasætbegreb end det der defineres i ISO 19115‑1:2014)

[[17]](file:///C:/Users/b025870/Desktop/Standard%20for%20beskrivelse%20af%20it-systemer%20-%20Basisprofil_CLA.docx#_ftnref17) https://arkitektur.digst.dk/det-faellesoffentlige-datasaetkatalog

[[18]](file:///C:/Users/b025870/Desktop/Standard%20for%20beskrivelse%20af%20it-systemer%20-%20Basisprofil_CLA.docx#_ftnref18) https://www.retsinformation.dk/eli/lta/2005/596.

[[19]](file:///C:/Users/b025870/Desktop/Standard%20for%20beskrivelse%20af%20it-systemer%20-%20Basisprofil_CLA.docx#_ftnref19) http://data.europa.eu/eli/reg/2016/679/oj\
  https://www.retsinformation.dk/eli/lta/2018/502

[[20]](file:///C:/Users/b025870/Desktop/Standard%20for%20beskrivelse%20af%20it-systemer%20-%20Basisprofil_CLA.docx#_ftnref20) https://www.datatilsynet.dk/media/6567/fortegnelse.pdf

[[21]](file:///C:/Users/b025870/Desktop/Standard%20for%20beskrivelse%20af%20it-systemer%20-%20Basisprofil_CLA.docx#_ftnref21) ISO/IEC 27002:2013 Information technology -- Security techniques -- Code of practice for information security controls: https://www.iso.org/standard/54533.html

[[22]](file:///C:/Users/b025870/Desktop/Standard%20for%20beskrivelse%20af%20it-systemer%20-%20Basisprofil_CLA.docx#_ftnref22) Sikkerhedscirkulæret https://www.retsinformation.dk/eli/retsinfo/2014/10338

[[23]](file:///C:/Users/b025870/Desktop/Standard%20for%20beskrivelse%20af%20it-systemer%20-%20Basisprofil_CLA.docx#_ftnref23) https://dltj.org/article/software-development-practice/

[[24]](file:///C:/Users/b025870/Desktop/Standard%20for%20beskrivelse%20af%20it-systemer%20-%20Basisprofil_CLA.docx#_ftnref24) Ved godkendelse af standarden, vil UML-modellerne blive udstillet som XMI og RDF/XML med de endelige httpURIer.

* * * * *

 [[CL1]](file:///C:/Users/b025870/Desktop/Standard%20for%20beskrivelse%20af%20it-systemer%20-%20Basisprofil_CLA.docx#_msoanchor_1)I hvad?

 [[CL2]](file:///C:/Users/b025870/Desktop/Standard%20for%20beskrivelse%20af%20it-systemer%20-%20Basisprofil_CLA.docx#_msoanchor_2)De hvad?

