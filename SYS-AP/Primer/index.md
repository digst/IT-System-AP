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

