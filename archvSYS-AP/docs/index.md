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
  h2.heading.settled > a.self-link, h3.heading.settled > a.self-link, h4.heading.settled > a.self-link, h4.heading.settled > a.self-link, h5.heading.settled > a.self-link, h6.heading.settled > a.self-link { display: none; }
  blockquote { font-size: 80%; font-style: italic; margin-left: 5%; width: 70%; border-left-width: 2px;}
	h2#abstract {display: none;}
	.p-summary {width: 50%; margin-left: 24px; padding: 0px;}
}
.new {
    border: solid 3px green;
    padding: 6px;
    margin: 18px 0px 18px 0px;
}

h2.heading.settled > a.self-link, h3.heading.settled > a.self-link, h4.heading.settled > a.self-link, h4.heading.settled > a.self-link, h5.heading.settled > a.self-link, h6.heading.settled > a.self-link { display: none; }

	
	
/* style til egne og andres definitioner rød/blå*/
</style>

<pre class="metadata">
Title: Standard for beskrivelse af it-systemer - Arkivprofil
Status: LS
URL: https://github.com/digst/IT-System-AP/tree/master/archvSYS-AP
Editor: Digitaliseringsstyrelsen http://arkitektur.digst.dk
Editor: Rigsarkivet
Editor: KL
Editor: Danske Regioner
Editor: Organisationen Danske Arkiver
Editor: OS2KITOS
Abstract: Dette dokument 'Standard for beskrivelse af it-systemer - Arkivprofil (archvSYS-AP)' udgør en fællesoffentlig standard for beskrivelse af offentlige myndigheders it-systemer ifm. afgivelse af it-systemoplysninger til Rigsarkivet.
Boilerplate: copyright no, conformance no, abstract no
Shortname: archvSYS-AP
Revision: 1.0.0
Date: 2019-12-05
Max ToC Depth: 3
Markup Shorthands: markdown yes
Repository: digst/IT-System-AP/tree/master/archvSYS-AP
Inline Github Issues: full
Logo: digst...
</pre>

<h1>Standard for beskrivelse af it-systemer - Arkivprofil</h1>


Version 1.0.0

December 2019



**Læsevejledning:**

Dette dokument 'Standard for beskrivelse af it-systemer - Arkivprofil (archvSYS-AP)' udgør en fællesoffentlig standard for beskrivelse af offentlige myndigheders it-systemer ifm. afgivelse af it-systemoplysninger til Rigsarkivet.

Arkivprofilen anvender dele af og udvider en basisprofil 'Standard for beskrivelse af it-systemer' - Basisprofil (SYS-AP) med arkiveringsrelevante oplysninger, og specificer netop hvilke oplysninger der enten *skal* eller *kan* være til stede i forbindelse med afgivelse til Rigsarkivet.

<p align="center"><img src="img/Figur0-1-Forholdet_mellem-profilerne.png" alt="Forholdet mellem profilerne" title="Forholdet mellem profilerne" width="350"/></p>

Kapitel 1 introducerer standardens formål, baggrund og den metode, hvormed standarden er blevet udarbejdet. Kapitel 2 beskriver *anvendelse* af standarden til myndigheders afgivelse af oplysninger om it-systemer i forbindelse med arkivering.

Kapitel 3 omhandler standardens helt centrale begreber, såsom 'it-system' og 'databærende it-system', og Kapitel 4 præsenterer indledningsvist en oversigt over standardens  underliggende emneområder, og hver sektion i dette kapitel dykker ned i et af emneområderne.  I Kapitel 3 og 4 vil udvalgte begreber være markeret med **fed skrifttype** -- disse modelleres i den underliggende datamodel som klasser eller egenskaber og går også igen i hhv. regnearksskabelon og UML-model, som findes i bilag.

Kapitel 5 beskriver kort selve datamodellen og henviser til yderligere information. Dette kapitel fortæller også, hvordan beskrivelser af it-systemer udarbejdet i henhold til standarden kan udveksles -- dels via regneark - dels via et maskinfortolkeligt format.  

Bilagene kan inddeles i tre kategorier. Bilag A viser de klassifikationer/kontrollerede udfaldsrum, der anvendes i standarden, Bilag B-E giver eksempler på skabeloner/vejledning til udfyldelse af oplysninger om it-systemer, og Bilag F-I omhandler den bagvedliggende begrebs- og datamodel.


Introduktion
================

Dette dokument udgør en fællesoffentlig standard for beskrivelse af offentlige myndigheders it-systemer ifm. afgivelse af it-systemoplysninger til Rigsarkivet. Standarden omfatter basisoplysninger om it-systemer, som fx it-systemnavn, it-systemejer, ibrugtagningsdato mv., men udvides med arkiveringsspecifikke oplysninger. Standarden tilbyder også et forslag til en ensartet struktur for disse oplysninger i et fælles udvekslingsformat, som vil kunne gøre det muligt at dele it-systemoplysninger på en effektiv måde. 


Formål
----------

Standarden skal gøre det nemmere for myndigheder at afgive relevante oplysninger om deres it-systemer til Rigsarkivet, så de kan overholde deres arkivmæssige forpligtelser.

Baggrund
------------

Standarden er etableret på anbefaling fra Kulturministeriets Arkivudvalg og efter aftale med KL, Danske Regioner og Digitaliseringsstyrelsen. Standarden skal understøtte Rigsarkivets tilsyn med offentlige myndigheders digitale arkivdannelse, så det sikres, at it-systemer, der indeholder bevaringsværdige data, bliver identificeret og bevaret.

Metode
----------

Standarden er blevet udarbejdet på baggrund af research- og udviklingsaktiviteter kombineret med feedback fra og sparring med en projektgruppe med medlemmer fra følgende interessentorganisationer: Rigsarkivet, KL, Danske Regioner, Organisationen Danske Arkiver, OS2Kitos og Digitaliseringsstyrelsen med repræsentanter fra Ministeriernes Kontor for it-styring og Center for Teknologi og Datastrategi. I forbindelse med researchaktiviteterne er flere eksisterede modeller og værktøjsunderstøttelse til registrering af it-systemer undersøgt nærmere, fx Model for porteføljestyring af statslige it-systemer, OS2Kitos og Rigsarkivets anmeldelses- og tilsynsskemaer. Læs mere om dette i Kapitel 6 Mapning til eksisterende modeller.

Selve udviklingsarbejdet er foretaget i henhold de Fællesoffentlige regler for begrebs- og datamodellering, og standarden udgøres af en anvendelsesprofil, der sammensætter flere eksisterende modeller til denne specifikke arkiveringsanvendelse. Denne profil anvender fx kernemodeller til beskrivelse af it-system (SYS), datasæt (DCAT), organisation (ORG), juridiske ressourcer (ELI), kontakter (FIBO), klassifikationer (SKOS) m.fl. Se Dataspecifikationsdokumentet for yderligere oplysninger om disse modeller.


Standardens anvendelse
==========================

Denne arkivprofil er baseret på en basisprofil til beskrivelse af it-systemer, som rummer de helt grundlæggende oplysninger om it-systemer. Denne arkivprofil udvider basisprofilen med arkiveringsoplysninger og fastlægger, hvilke oplysninger der er krævede eller anbefalede i denne sammenhæng.

Standarden skal anvendes i forbindelse med afgivelse af systemoplysninger til Rigsarkivet. Standarden skal således standardisere afgivelsen og opdateringen af systemoplysninger i relation til regionernes og kommunernes arkivmæssige forpligtelser. Derudover vil standarden også blive anvendt ved kommende tilsyn på det statslige område. Anvendelsesprofilen indeholder netop det sæt af oplysningstyper, der er påkrævet i forbindelse med afgivelse af it-systemoplysninger til Rigsarkivet, samt yderligere anvendelsesspecifikke præciseringer.


Rigsarkivets interesse i it-systemer
----------------------------------------

Rigsarkivet vil anvende standarden i forbindelse med tilsyn med offentlige myndigheders it-systemer. Det betyder, at myndighederne ved at opmærke deres systemer med oplysningerne fra standarden vil få nemmere ved at besvare et tilsyn og kan få et overblik over, hvilke it-systemer hos dem som indeholder bevaringsværdige data. Det gør det lettere at sikre, at de arkivmæssige forpligtelser overholdes.

En udfordring for brug af standarden og for afgivelse af oplysninger er de tilfælde, hvor et it-system ikke bruges, som det er tiltænkt. Det kan både medføre, at et system, som normalt vil skulle bevares, alligevel ikke indeholder bevaringspligtige data, men også betyde, at et system, som normalt ikke skal arkiveres, vil indeholde bevaringspligtige data. Med standarden kan det registreres, hvilke typer af oplysninger der indgår i systemerne, hvorved det er muligt at identificere bevaringspligtige data.



Modenhed ift. beskrivelse af processer, services og datasæt
---------------------------------------------------------------

Et it-system yder en bestemt it-servicefor at understøtte en forretningsproces, og i den forbindelse skabes der ofte datasæt i den offentlige forvaltning.

I forbindelse med Rigsarkivets tilsyn med offentlige myndigheder er det konstateret, at det har været vanskeligt for myndighederne at vedligeholde et overblik over de systemer, som skal indberettes til Rigsarkivet i forbindelse med tilsyn.

Rigsarkivet har brug for at kunne identificere arkiveringspligtige datasæt på en pragmatisk måde, hvorfor det i de fleste tilfælde er mest hensigtsmæssig at begynde dialogen med de pågældende myndigheder på baggrund af et systemoverblik. Dette systemoverblik vil standarden danne basis for.  

Der kan være perspektiver i, at myndigheder fremover vedligeholder et overblik over datasæt, forretningsprocesser og services med en kobling til understøttende it-systemer, og således at dialogen omkring arkivering kan begynde dér. Systemoverblikket skal kunne samarbejde med de mest udbredte overblikssystemer, som myndighederne allerede har, således at de ikke skal vedligeholde flere overblik.

<p class="example">*Som eksempel kan nævnes OS2KITOS, som mange kommuner anvender som systemoverblik.*</p>


Centrale begreber
=====================

Begrebet *it-system* udgør det centrale element i denne standard, men dette specialiseres og kobles til relevante klassifikationer for at indsnævre den mængde af it-systemer, der skal afgives oplysninger om ifm. arkivering


System, informationssystem og it-system
-------------------------------------------

Et **system** defineres generelt som 'et system er en kombination af interagerende elementer, der er organiseret for at opnå et eller flere erklærende formål' ligesom i ISO/IEC 15288 (Systems and software engineering -- System life cycle processes).  

Det bemærkes også, at 'Et system er i denne sammenhæng menneskeskabt og består ikke blot af hardware, software og data, men også af mennesker, processer, procedurer, faciliteter og materialer og naturlige genstande'.

Ser vi alene på systemer til indsamling, organisering, lagring og kommunikation af information, har vi at gøre med informationssystemer, og når (computer)-teknologi anvendes til at behandle disse informationer eller data, har vi at gøre med it-systemer

<p class="note">Begrebet *it-system* er altså en specialisering af *system* fra ISO 15288, idet der fokuseres på IT-aspektet. Det vurderes derudover at definitionen er tråd med ISO/IEC TR 10000-1:1998(en) Information technology — Framework and taxonomy of International Standardized Profiles og ISO/IEC TR 12182:2015 (Systems and software engineering -- -- Framework for categorization of IT systems and software, and guide for applying it.</p>

Begrebet **it-system** defineres derfor i denne standard som 'system der består af digitale informationsteknologier'. Et it-system kan instantieres i forskellige it-miljøer. Et **instantieret it-system** kan derfor defineres som 'fysisk instans af et it-system i et bestemt it-miljø'. Det vil fx kun være relevant at arkivere data fra et it-system instantieret i et produktionsmiljø og ikke et testmiljø, men i forbindelse med afgivelse af it-systemoplysninger til Rigsarkivet bør dette fremgå klart.

I forhold til arkivering præciseres klassen **instantieret it-system** som værende et **databærende it-system** ved at sætte egenskaben 'databærende' til 'sand'.  

Begrebet databærende it-system defineres i denne standard som 'instantieret it-system, der indeholder digitalt skabte data eller dokumenter'.

I forbindelse med aflevering til Rigsarkivet eller kommunale stadsarkiver er der alene tale om data digitalt skabt af den offentlige forvaltning og domstolene.

Ifølge Rigsarkivets vejledninger i bevaring og kassation af arkivalier kan et databærende it-system fx være:
- et fagsystem, et register eller en database
- en elektronisk journal, som indeholder oplysninger om sager og dokumenter, men hvor selve dokumenterne findes på papir
- et elektronisk sags- og dokumenthåndteringssystem (ESDH-system), hvor både oplysninger om sager og dokumenter samt selve dokumenterne findes i digital form.

**Klassifikationer**

Denne standard anvender en række klassifikationer, som giver mulighed for at udpege en bestemt delmængde af databærende it-systemer. Klassifikationerne vil blive introduceret i det følgende kapitel

<p class="note">Klassifikationer beskrives iht. [Anvendelsesprofil for klassifikation](https://arkitektur.digst.dk/rammearkitektur/datastandarder/anvendelsesprofil-klassifikationer)</p>

**Hvornår er der tale om et nyt it-system?**

I forhold til ibrugtagningen af et it-system i en organisation kan det i visse tilfælde være svært at vurdere, hvornår der er tale om at organisationen overgår fra ét it-system til et andet, eksempelvis ved overgangen fra én version af et kommercielt produkt til en anden version. Her kan vurderingen eventuelt tage udgangspunkt i, om it-systemet *leverer en anden service* end den oprindelige, hvilket ofte er forbundet med etableringen af en ny kontrakt med rettighedshaveren af det kommercielle produkt. Ny kontrakt med rettighedshaveren kan altså ofte betyde nyt it-system, modsat løbende opdateringer og fejlrettelser til kørende it-systemer, men dette skal undersøges nøje for det konkrete it-system. I forhold til databærende systemer kan det også være relevant at se på, om fx hele den bagvedliggende databasestruktur er skiftet ud.


Standardens emneområder
===========================

I det følgende gives en oversigt over standardens omfang og kapabilitet

It-systemer kan beskrives ud fra flere forskellige aspekter eller emner. De grundlæggende kerneinformationer ses i midten af figuren herunder, og de øvrige otte emneområder afspejler arkitekturprincipperne fra rammearkitekturen: *strategi, styring, jura, sikkerhed, opgaver, information, applikation* og *infrastruktur*, som beskrives i FDA [Hvidbog om fællesoffentlig digital arkitektur](https://arkitektur.digst.dk/mandat-og-styring/hvidbog-om-faellesoffentlig-digital-arkitektur). 

Disse otte emner dækker bredt, og for at dække en specifik anvendelseskontekst vil det typisk være nødvendigt at udvide basisprofilen med oplysninger fra forskellige emneområder. I tillæg til de otte emneområder eksisterer et metalag med informa-tioner om myndighedens udveksling af disse oplysninger til et bestemt formål.

<p align="center"><img src="img/Figur4-1-Illustration-af-standardens-emneomraader.png" alt="Figur 4.1 Standardens emneområder" title="Figur 4.1 Standardens emneområder" width="600"/></p>Figur 4.1: Illustration af standardens emneområder\

Markeringen af emnerne *styring, opgaver, information* og *sikkerhed* i figuren ovenfor skal illustrere, at disse fire områder er definerende for arkivprofilens anvendelse til afgivelse af oplysninger om it-systemer til Rigsarkivet.

Afgivelse af it-systemoplysninger
-------------------------------------

Når der skal afgives oplysninger om it-systemer, som en given myndighed **anvender**, angives **myndighedens navn** samt den e-mailadresse, hvormed myndigheden primært kan kontaktes (**hovedmailadresse**). Derudover angives en **myndighedstype**, dvs. en kategorisering af offentlige organisationer ift. styringsniveau (region, kommune, statslig myndighed, offentlig selvejende institution). Indberetningen forsynes også med en datoangivelse for, hvornår oplysningerne blev indberettet (**afgivelsesdato**). Det er den dataansvarlige myndighed, der er forpligtet til at angive it-systemoplysninger til Rigsarkivet, jf. afsnittet Styring.

<p class="note">Myndigheder beskrives som organisationer iht. [Anvendelsesprofil for organisationer](https://arkitektur.digst.dk/rammearkitektur/datastandarder/anvendelsesprofil-organisationer)</pre>

Kerneinformation
--------------------

Et it-system forsynes med en **identifikator** (et ID), der entydigt udpeger det konkrete it-system. Et it-system tilføjes en eller flere navne. Et af navnene vil være it-systemets primære eller **foretrukne navn,** men andre, fx kaldenavne, kan angives som **alternative navne.**

Hvor et it-system kan beskrives som en implementering og ibrugtagning af et softwareprodukt tilhørende en bestemt produktserie, som fx Acadre eller F2, vil it-systemnavnet typisk være lig **navnet på produktserien**, som producenten har markedsført eller som anført i hovedkontrakten med leverandøren, men it-systemet kan også have andre lokale navne.

En produktserie kan have en overordnet **beskrivelse af produktseriens** egenskaber, som det fx ses i [SKI-kataloget]( https://skikataloget.ski.dk/ski-kataloget/), men i forbindelse med ibrugtagning er det også muligt at angive en ***it-systembeskrivelse*** som i fritekst redegør for formålet med it-systemets anvendelse eller it-systemets nøglefunktion i en organisation. Derudover bør et it-systems **anvendelsesformål** også beskrives ved opmærkning ift. offentlige opgaver med klassifikationerne FORM/KLE, som det beskrives under emnet 'forretningsunderstøttelse'. Supplerende bemærkninger eller oplysninger kan også tilføjes som en **kommentar** i fritekst

Som en del af kerneinformationerne hører **ibrugtagningsdato** og **udfasningsdato,** som tilsammen beskriver perioden fra den dato, hvor it-systemet blev taget i brug med delvis eller fuld funktionalitet, indtil den dato, hvor it-systemet endeligt bliver afviklet. Datoangivelserne kan eventuelt suppleres med en **operationel status,** som angiver, hvilken tilstand systemet befinder sig i, i forhold til ibrugtagning. Se udfaldsrummet i Bilag A.

For at kunne identificere, hvilken version af softwareproduktet der er taget i anvendelse, eksempelvis i forhold til en bestemt kontrakt med en leverandør, kan det være relevant at angive et **versionsnummer**. Hvis et versionsnummer er specificeret i kontrakten, bør dette anvendes.

<p class="example">Eksempelvis kan der ved anvendelse af cBrains F2 angives version 5.3 (og ikke 5.3.0.41112)</p>

It-systemer kan være taget i anvendelse i forskellige miljøer iht. systemets udviklingsforløb, fx udvikling, afprøvning, præproduktion, produktion, se klassifikationen **it-miljøtype** i Bilag A. I forhold til arkivering er kun instanser af it-systemer i produktion relevante.

Opgaver
-----------

Et it-system yder en given it-service, som understøtter forretningens opgaver.

Et it-system kan beskrives med et eller flere anvendelsesformål, der antages at være at understøtte en **forvaltningsopgave**. Til dette formål anvendes en klassifikation over offentlige opgaver eller såkaldte forvaltningsopgavetyper. Statslige myndigheder og regioner kan eksempelvis anvende Den Fællesoffentlige Referencemodel (FORM) -en overordnet emnesystematik, der dækker opgaveporteføljen i hele den offentlige sektor -- dvs. staten, kommunerne og regionerne. Kommuner kan anvende KL Emnesystematik (KLE) -- en emnesystematik/journalplan, der dækker det kommunale område. KLE er som regel mere detaljeret end FORM på det kommunale område. Det foreslås, at KLE anvendes af kommunerne, og FORM af regioner og statslige administrative enheder -- som minimum på det øverste niveau (hhv. serviceområde i FORM og emnegruppe i KLE):

**Klassifikation KLE:** [http://www.kle-online.dk/](http://www.kle-online.dk/soegning)

**Klassifikation FORM:** [http://www.form-online.dk](http://www.form-online.dk/soegning)

<p class="example">Eksempelvis kan en myndighed anvende Formpipes Acadre og cBrains F2 ESDH til at understøtte FORM-forvaltningsopgaven '65.50.05.05 Sagshåndtering' (FORM v.2.14) el. KLE-emnet '00.15.12. Kvalitetsstyringssystem, sagsbehandling' (KLE v. Aug. 2019)</p>

Bemærk, at produkter i SKI-kataloget allerede er opmærket med FORM.

FORM og KLE indeholder henvisninger til de love og lovbekendtgørelser, som de offentlige opgaver udspringer fra, så ved at opmærke et it-system med FORM eksisterer der også indirekte en relation til retsgrundlaget for it-systemets anvendelse. Der er også muligt via FORM at se, hvilke myndigheder de forskellige opgaver tilhører. KLE indeholder, ud over love og lovbekendtgørelser, også bekendtgørelser. FORM mapper til paragraffer i finansloven og KLE, og KLE mapper til Social- og Indenrigsministeriets kontoplan.

Kommunale it-systemer kan tilknyttes én eller flere specifikke kommunale sagsområder i henhold til [Bekendtgørelse om bevaring og kassation af digitalt skabte data og dokumenter fra kommunerne](https://www.retsinformation.dk/eli/lta/2018/183). Ligeledes kan regionale it-systemer tilknyttes én eller flere specifikke regionale sagsområder iht. [Bekendtgørelse om bevaring og kassation af arkivalier i regionerne](https://www.retsinformation.dk/eli/lta/2015/266). I klassifikationen Sagsområde i Bilag A er klassifikationerne samlet med angivelse af, hvilken myndighedstype der anvender hvilke sagsområder. Det bemærkes, at klassifikationen sagsområder har et vist overlap med hhv. FORM og KLE, men anvendelsen af netop dette udfaldsrum er fastlagt ved bekendtgørelse.

Når en organisation skifter et it-system ud med et andet it-system til varetagelse af samme funktion, kan det tidligere it-system eksplicit angives som et såkaldt **forgængersystem,** se også afsnit om arkivering og datakonvertering fra sådanne forgængersystemer.

Styring
-----------

Et it-system kan have mange forskellige relationer til aktører, som hver især har en særlig interesse i systemet, og som dermed udgør systemets interessenter. Aktørerne kan være personer eller organisationer, men det anbefales, i det omfang det er muligt, ikke at registrere oplysninger om fysiske personer men derimod den relevante medarbejderrolle eller organisatoriske enhed.

På overordnet niveau angives **it-systemejeren** -- en person eller organisation med det overordnede ansvar for et givet it-systems drift, vedligehold og anvendelse. Ofte vil it-systemejeren være lig kontraktejeren og kan identificeres præcist i myndighedens kontraktstyring.

<p class="example">Eksempelvis er Kontorchefen for Center for Systemforvaltning i Digitaliseringsstyrelsen it-systemejer for NemLog-in, mens it-systemet forvaltes af NemLog-in-teamet.</p>

For databærende it-systemer skal den **dataansvarlige** aktør også angives, dvs. den organisation, som har det administrative ansvar for data. I forhold til persondata indsnævres denne definition yderligere til '*en fysisk eller juridisk person, en offentlig myndighed, en institution eller et andet organ, der alene eller sammen med andre afgør, til hvilke formål og med hvilke hjælpemidler der må foretages behandling af personoplysninger*', jf. [GDPR](http://data.europa.eu/eli/reg/2016/679/oj) *[på dansk](https://www.retsinformation.dk/eli/lta/2018/502).* Én myndighed kan være dataansvarlig for et system, mens det faktisk er **databehandler**, som behandler personoplysninger på den dataansvarliges vegne, der er i besiddelse af systemet og anvender det. Det kan være en fordel at registrere begge oplysninger. I nogle tilfælde er der forskel på dataansvarlig og databehandler i betydningen, at de kan være forskellige organisationer. I det omfang, at leverandører har fået instruks af den dataansvarlige til at behandle personoplysninger, betragtes disse også som databehandlere, jf. [Datatilsynets vejledning om databehandlere og dataansvarlige]((https://www.datatilsynet.dk/media/6560/dataansvarlige-og-databehandlere.pdf). Det kan også være relevant at angive den konkrete **dataskaber**, dvs. den aktør, der har det primære ansvar for tilvejebringelsen af datasættet.

Et it-system kan dokumenteres ved hjælp af forskellige dokumenter, der hver har sit formål og målgruppe, fx arkitekturdokumentation, installationsvejledning og slutbrugervejledning.

Information
---------------

De data, som et instantieret it-system **skaber,** kan betragtes som en specifik fysisk **repræsentation** af et **datasæt**, og beskrivelsen af datasæt og datasætrepræsentationerfølger i denne sammenhæng W3Cs Data Catalogue Vocabulary (DCAT) (https://www.w3.org/TR/vocab-dcat/). Både det (logiske) datasæt og dets (fysiske) repræsentationer kan forsynes med en **titel.**

<p class="note">[Referencearkitektur for deling af data og dokumenter](https://arkitektur.digst.dk/sites/default/files/20180503_rad_v1.0_-_godkendt_af_sda.pdf) definerer datasæt som *en samling af oplysninger bestående af enkelte dele der forvaltes under ét*. Denne definition er i tråd med W3Cs definition *samling af data, udstillet eller forvaltet af en enkelt aktør*. Bemærk også at DCAT anvender et snævrere datasætbegreb end det der defineres i ISO 19115‑1:2014)</p>

### Arkivering

I forhold til arkivering er det vigtigt at vide, hvornår myndigheden er begyndt at tilføje data til it-systemet, og hvornår den er ophørt med at tilføje data. Til dette formål kan it-systemets generelle **ibrugtagningsdato*** og **udfasningsdato*** typisk anvendes som pejlemærke, men datatilføjelsesperioden bør også fremgå eksplicit, altså **første datatilføjelsesdato** og **sidste datatilføjelsesdato** for datasættets specifikke fysiske repræsentation.Disse oplysninger er især relevante, når myndigheden har konverteret data fra andre systemer ind i systemet. Dvs. i de tilfælde, hvor ibrugtagningsdato, udfasningsdato og datering af oplysninger i systemet ikke er den samme. Fx kan første datatilføjelsesdato være den dato, hvor de tidligste data er indtastet i det eller de systemer, som data er migreret fra.

For at gøre det lettere for myndigheder at afgive oplysninger om deres it-systemer til Rigsarkivet og dermed overholde deres arkivmæssige forpligtelser kan it-systemer og de datasætrepræsentationer, de skaber, forsynes med flere forskellige arkiveringsoplysninger ved hjælp af nærværende standard.

<p class="note">Læs mere om myndighedernes arkiveringsforpligtelse på Rigsakivets hjemmeside: [Rigsarkivet|Offentlig Forvaltning ](https://www.sa.dk/da/offentlig-forvaltning/)</p>

I forhold til arkivering af data bestemt til bevaring er det offentlige **databærende it-systemer,** der er i fokus, dvs. it-systemer, der indeholder data og dokumenter digitalt skabt af den offentlige forvaltning og domstolene, jf. [Arkivloven] (https://www.retsinformation.dk/eli/lta/2016/1201). Udover at det skal angives, om it-systemet er databærende, altså indeholder datasæt, kan det også præciseres, at nogle af disse data udgøres af dokumenter, ved at angive at it-systemet også er ***dokumentbærende***.

Hvorvidt den pågældende myndighed har pligt til at arkivere eller kassere data i it-systemet, kan angives med klassifikationen **arkiveringspligttype**, se Bilag A. Digitalt skabte data og dokumenter, som ikke skal bevares i henhold til gældende lovgivning, kasseres, når opbevaringspligten efter andre bestemmelser er opfyldt, og når de efter myndighedernes egen vurdering i øvrigt ikke længere har retlig eller administrativ betydning.

I forhold til aflevering af arkiveringsversioner skal det kunne angives, om data i it-systemet planlægges afleveret som et øjebliksbillede, en afgrænset periode eller ved afsluttet arkivperiode. Her anvendes klassifikationen **arkiveringsversionsperiodetype**, se Bilag A,som defineres i Bekendtgørelse om arkiveringsversioner. Arkiveringsversioner af data fra et it-system afleveres enten til Rigsarkivet eller et kommunalt eller regionalt stadsarkiv, som defineres i klassifikationen **arkiveringsinstitutionstype**.

Det angives, om der manuelt eller automatisk er **konverteret data og dokumenter** fra forgængersystemet ind i det nuværende system, og om **alle data** eller **udvalgte data er konverteret ind.** Et forgængersystem er i denne forbindelse et andet it-system, der tidligere har varetaget samme funktion.

Det kan også angives, om der tidligere er udarbejdet en arkiveringsversion af data i systemet.For arkiveringsversionen angives den periode, som den dækker. Dvs. det årstal, arkiveringsversionen først dækker, til det år, som arkiveringsversionen sidst dækker.

En **arkiveringsfrekvens** kan også registreres, dvs. den frekvens, med hvilken en myndighed fremstiller arkiveringsversion af et givet datasæt i et it-system.

Sikkerhed
-------------

Emnet sikkerhed kan vedrøre mange forskellige aspekter, fx informationssikkerhed, persondatasikkerhed, forretnings- og samfundskritikalitet og fortrolighed.

I henhold til [GDPR](https://www.retsinformation.dk/eli/lta/2018/502) og Datatilsynets [Vejledning om fortegnelse](https://www.datatilsynet.dk/media/6567/fortegnelse.pdf) er det for databærende it-systemer relevant at være opmærksom på **datasletningsfristen**, dvs. førstkommende dato for, hvornår bestemte data i systemet skal være slettet forinden.
It-systemet kan opmærkes med en **personoplysningskategori**, som er beskrevet i Datadatatilsynets vejledning, og på denne måde oplyses det, hvorvidt systemet indeholder følsomme personoplysninger eller almindelige personoplysninger, herunder personnummeroplysninger og oplysninger om strafbare forhold. Dertil tilføjes en angivelse af fraværet af personoplysninger, se Bilag A. De følsomme oplysninger er udtømmende oplistet i databeskyttelsesforordningen, og alle andre oplysninger er derfor almindelige personoplysninger. Oplysninger om strafbare forhold og personnumre betragtes som almindelige personoplysninger, men databeskyttelsesloven fastsætter særlige regler om disse oplysninger. Som en hjælp til præcisering kunne en klassifikation med personoplysnings*underkategorier* eventuelt opstilles.

Data i it-systemet kan klassificeres med flere forskellige klassifikationer ift. fortrolighed, fx **Fortrolighedsgrad iht. ISO27002** [ISO/IEC 27002:2013 Information technology -- Security techniques -- Code of practice for information security controls](https://www.iso.org/standard/54533.html) eller **Fortrolighedsgrad iht. sikkerhedscirkulæret (EU/NATO)**  [Sikkerhedscirkulæret](https://www.retsinformation.dk/eli/retsinfo/2014/10338). Se Bilag A. I forhold til klassifikation iht. sikkerhedscirkulæret kan tilføjes 'uklassificeret', så det kan angives, at der er taget stilling til fortrolighedsgraden.

<p class="example">Eksempelvis kan data i beredskabssystemer eventuelt være opmærket med fortrolighedsgrad, og fortrolighed kan være et relevant aspekt ved indmelding af it-systemoplysninger såsom kritikalitetstype og systemernes tekniske tilstand. </p>


Fælles datamodel og udvekslingsformat
=========================================

Denne standard præsenterer et udvekslingsformat i to repræsentationer til deling af oplysninger om it-systemer.

Fælles datamodel
--------------------

Basisprofilens datamodel udgør den fælles specifikation, som anvendes og udvides i arkivprofilens datamodel.

Der gives en overordnet beskrivelse af datamodellens indhold og sammensætning i bilaget 'Om datamodellen'. Her kan også ses UML-diagrammerne for både basisprofilen og arkivprofilen. UML-modellerne er udstillet og kan tilgås via en webbrowser, hvor det er muligt at klikke sig gennem modellen. Bemærk, at modelelementernes metadata er registreret som tagged values.

- Link til webudgivelse af UML-modellerne: [https://data.gov.dk/document/itsystem-ap/v1/uml/](https://data.gov.dk/document/itsystem-ap/v1/uml/)

Via nedenstående link findes der også en online oversigt over modellens elementer.

- Link til oversigt over modellens elementer: https://github.com/digst/IT-System-AP/tree/master/archvSYS-AP

Skabelon til registrering i regneark
----------------------------------------

Der er blevet udarbejdet en skabelon til registrering af oplysninger om it-systemer i et regneark. Overskrifterne vil svare til egenskaberne, som de er præsenteret i denne standard, og hver element vil entydigt kunne mappes til den bagvedliggende datamodel. Dette betyder også, at det vil være muligt fx at konvertere data eksporteret i csv-format til et maskinfortolkeligt format.

Regnearket har den fordel, at det er let at anvende, men regneark har også den store ulempe, at det ofte kræver manuel oprettelse og videre import. Det kan også være svært at repræsentere den kompleksitet, der faktisk kan være tilstede i den bagvedliggende datamodel. Eksempelvis kan et givet it-system godt skabe flere forskellige datasæt, som hver især kan dække forskellige perioder og have forskellige dataansvarlige tilknyttet. I den aktuelle skabelon er det kun muligt at registrere ét datasæt per it-system. Et it-system kan også udstille flere forskellige datasæt, og disses id'er må registreres i samme felt, selvom dette ikke er ideelt.  

I bilaget 'Skabelon til registrering i regneark' kan ses en visning af et sådant regneark, men det kan også downloades fra:

[https://data.gov.dk/document/itsystem-ap/v1/templates/Excelformular_til_indtastning_af_it-systemoplysninger_arkivprofil.xlsx](https://data.gov.dk/document/itsystem-ap/v1/template/Excelformular_til_indtastning_af_it-systemoplysninger_arkivprofil.xlsx)

Maskinfortolkeligt format
-----------------------------

Hvis data skal deles på tværs, bør det være *digitalt understøttet* i de systemer, der anvendes til registrering af systemoplysninger. Systemerne bør bygge på samme logik og standard, så systemerne er i stand til at udveksle data om it-systemer på tværs af organisatoriske skel. Det kan lade sig gøre, hvis data er maskinfortolkelige. Datamodellen er derfor udtrykt med UML med en bagvedliggende semantik med Resource Description Framework (RDF), der kan fortolkes af både mennesker og maskiner. Alle elementerne i datamodellen er derfor defineret inden for rammerne af RDF og har entydig identifikation, der kan anvendes direkte som metadatabeskrivelse af data. Data udtrykt med det maskinlæsbare udvekslingsformat kan også let valideres op imod den bagvedliggende datamodel og dermed sikre højere datakvalitet i de registrerede data.

Eksempeldata i maskinlæsbart format (RDF/XML) kan ses i bilag E. Bemærk, at der også umiddelbart kan konverteres til andre serialiseringer såsom JSON-LD, Turtle, m.fl.

Godkendelsen af denne arkivprofil omfatter ikke krav om anvendelse af det maskinlæsbare RDF-format og dets serialiseringer som JSON-LD, Turtle, RDF/XML.

Referencer
==============

**Standarder**

- [ISO/IEC CD 15288](https://www.iso.org/standard/63711.html)'Systems Engineering--- System Life Cycle Processes'
- [ISO/IEC 16350:2015(en)](https://www.iso.org/obp/ui/#iso:std:iso-iec:16350:ed-1:v1:en)Information technology --- Systems and software engineering --- Application management
- [ISO/IEC TR 10000-1:1998(en)](https://www.iso.org/obp/ui/#iso:std:iso-iec:tr:10000:-1:ed-4:v1:en) 'Information technology --- Framework and taxonomy of International Standardized Profiles --- Part 1: General principles and documentation framework'
- ISO/IEC TR 12182:2015 'Systems and software engineering -- Framework for categorization of IT systems and software, and guide for applying it'
- ISO/IEC/IEEE 42010 'Systems and software engineering --- Architecture description '
- ISO/IEC/IEEE DIS '42020 Enterprise, systems and software --- Architecture processes'
- ISO/IEC/IEEE DIS 42030 'Systems and Software Engineering --- Architecture Evaluation'
- [ISO/IEC 27002:2013](https://www.iso.org/standard/54533.html) Information technology -- Security techniques -- Code of practice for information security controls: 
- [ITIL](http://www.itlibrary.org/) The Information Technology Infrastructure Library
- [TOGAF](https://publications.opengroup.org/standards/togaf/specifications/c182) The TOGAF® Standard, Version 9.2, 
- [ARCHIMATE](https://publications.opengroup.org/standards/archimate/c179) ArchiMate® 3.0.1 Specification 

**Datamodeller / klassifikationer / retningslinjer**

- Datamodellen for [OS2Kitos ](https://www.kitos.dk/)(inkl. klassifikation af applikationstyper og forretningstyper)
- OIO specifikation af it-system i [modellen for Organisation](https://arkitektur.digst.dk/sites/default/files/organisationsmodellen_version_2.0.pdf)
- KMD KOSDY-datamodel)
- Datamodellen for ServiceNow ([IT Service Management-delen](https://www.servicenow.com/products/it-service-management.html)) /ITILs (CMDB)
- Statens-IT systemkort
- Datamodellen for BMC
- Retningslinjer for dokumentation og formidling af arkitektur i digitaliseringsprojekter. (baseret på ISO)
- Fællesoffentlig Referencemodel (FORM): https://arkitektur.digst.dk/rammearkitektur/klassifikationer/form;https://arkitektur.digst.dk/rammearkitektur/klassifikationer/form
- Kommunernes Emnesystematik (KLE)
- Service- og Teknologireferencemodel (STORM): http://arkitekturguiden.digitaliser.dk/storm
- KOMBIT Rollegalleri: https://www.kombit.dk/sites/default/files/user_upload/documents/Videnscenter/Eksempel%20fra%20KOMBIT_Rollegalleri%20implementering.pdf
- Referencearkitektur for deling af data og dokumenter: https://arkitektur.digst.dk/sites/default/files/20180503_rad_v1.0_-_godkendt_af_sda.pdf

**Retskilder og tilhørende vejledninger:**

- Bekendtgørelse nr. 183 af 26. januar 2018 om bevaring og kassation af digitalt skabte data og dokumenter https://www.retsinformation.dk/eli/lta/2018/183
- Bekendtgørelse nr. 266 af 23. marts 2015 om bevaring og kassation af arkivalier i regionerne https://www.retsinformation.dk/eli/lta/2015/266
- Vejledning til bekendtgørelse om bevaring og kassation af digitalt skabte data og dokumenter fra kommunerne https://www.sa.dk/wp-content/uploads/2018/04/2007_IT_Vejledning-til-bekendtg%C3%B8relse_h%C3%B8ring-1.pdf
- Vejledning om bevaring og kassation af arkivalier hos regionerne https://www.sa.dk/wp-content/uploads/2015/06/Vejledning-til-regionsbekendtg%C3%B8relsen_juni-2015.pdf
- Bekendtgørelse nr. 1007 af 20. august 2010 om arkiveringsversioner https://www.retsinformation.dk/eli/lta/2010/1007
- Vejledning om kvalitetssikring i it-systemer -- Rigsarkivets minimumskrav og anbefalinger https://www.sa.dk/wp-content/uploads/2016/02/Vejledning-om-kvalitetssikring.pdf
- Arkivhåndbog for statslige myndigheder https://www.kbharkiv.dk/images/files/Arkivering/Arkivhandbogen.pdf
- Datatilsynets 'Vejledning om fortegnelse' https://www.datatilsynet.dk/media/6567/fortegnelse.pdf
- Sikkerhedscirkulæret (Cirkulære om sikkerhedsbeskyttelse af informationer af fælles interesse for landene i NATO eller EU, andre klassificerede informationer samt informationer af sikkerhedsmæssig beskyttelsesinteresse i øvrigt) https://www.retsinformation.dk/eli/retsinfo/2014/10338
- Databeskyttelsesloven (Lov om supplerende bestemmelser til forordning om beskyttelse af fysiske personer i forbindelse med behandling af personoplysninger og om fri udveksling af sådanne oplysninger) https://www.retsinformation.dk/eli/lta/2018/502
- GDPR (generel forordning om databeskyttelse): https://eur-lex.europa.eu/legal-content/DA/TXT/HTML/?uri=CELEX:32016R0679&from=EN


Bilag
=========

Bilag A: Overblik over relevante klassifikationer
-------------------------------------------------

<p align="center"><img src="img/Bilag-A-Overblik-over-relevante-klassifikationer.png" alt="Overblik over relevante klassifikationer" title="Overblik over relevante klassifikationer" width="800"/></p>


### Klassifikation FORM:
- Distribution:[http://www.form-online.dk/](http://www.form-online.dk/soegning)
	Se de overordnede emner herunder:

02	Internationale aftaler
03	Udenrigstjeneste
05	Samfundsstruktur
06	Samfundsøkonomi, samfundsdigitalisering og statistik
08	Borgerskab
10	Uddannelse og undervisning
12	Forskning
14	Arbejdsmarked
16	Kultur
17	Fritid og idræt
18	Kirke
20	Sundhed
24	Dagtilbud
26	Social service og omsorg
30	Skatter og afgifter
34	Erhverv
37	Miljø
38	Natur og klima
40	Politi
42	Retspleje og domstole
44	Straffuldbyrdelse
46	Forsvar
47	Redningsberedskab
52	Fysisk planlægning og geodata
54	Ejendomme og byggeri
56	Energi- og vandforsyning
58	Trafikinfrastruktur
59	Trafik og transport
60	Myndighedens personale og frivillige
62	Myndighedens bygninger og arealer
63	Myndighedens driftsmateriel, varer og tjenesteydelser
65	Myndighedens kommunikation og dokumentation
67	Myndighedens økonomi
68	Myndighedens it

### Klassifikation KLE:
- Distribution:[http://www.kle-online.dk/](http://www.kle-online.dk/soegning)
	Se de overordnede emner herunder:

00	Kommunens styrelse
01	Fysisk planlægning og naturbeskyttelse
02	Byggeri
03	Boliger
04	Parker, fritids-/idrætsanlæg og landskabspleje mv.
05	Veje og trafik
06	Spildevand og vandløb
07	Affald og genanvendelse
08	Havne og lufthavne
09	Miljøbeskyttelse
13	Forsyning
14	Beredskab
15	Arbejdsmarked og beskæftigelsesindsats
17	Folkeskoleundervisning
18	Folkeoplysning og ungdomsskoler
19	Kulturhistoriske institutioner
20	Kulturvirksomhed
21	Biblioteker
22	Regulering af private erhverv
23	Borgerlige forhold
24	Erhvervsforhold
25	Beskatning
27	Social service
28	Dagtilbud
29	Sundhed
30	Andre myndigheders opgaver
32	Kontante ydelser
54	Uddannelse
81	Kommunens personale
82	Kommunens ejendomme og lokaler
83	Kommunens driftsmidler og inventar
84	Offentlige valg
85	Kommunens administrative systemer
86	Kommunens selvforsyning og fremstillingsvirksomhed
87	Kommunens arbejdsmiljø
88	Kommunens indkøb og udbud



###  Klassifikation Sagsområder:
Klassifikation, der består af typer af sagsområder i henhold til 'Bekendtgørelse om bevaring og kassation af digitalt skabte data og dokumenter fra kommunerne' og 'Bekendtgørelse om bevaring og kassation af arkivalier i regionerne' 

 **Administrative systemer**
  - ESDH-systemer med journalsager *(kommune og region)*
  - Elektroniske journaler *(kommune og region)*
  - Elektroniske sagshenvisnings- og advissystemer *(kommune)*

 **Systemer på økonomiområdet**
  - Økonomisystemer (kommune og region)

 **Systemer på social- og sundhedsområdet**
  - ESDH-systemer med personsager *(kommune)*
  - Daginstitutions- og børnepasningssystemer *(kommune)*
  - Omsorgssystemer *(kommune)*
  - Systemer vedr. institutioner for handicappede herunder døgninstitutioner, klientsystemer *(kommune og region)*
  - Systemer vedr. social- og psykiatribehandling herunder døgninstitutioner, klientsystemer *(kommune og region)*
  - Systemer vedr. forebyggelse og genoptræning *(kommune)*
  - Sundhedsplejesystemer* (kommune)*
  - Systemer vedr. misbrugsbehandling *(kommune)*

 **Systemer på miljø- og teknikområdet *****(kommune)***
  - ESDH-systemer med byggesager *(kommune)*
  - ESDH-systemer med sager vedr. miljøgodkendelser og miljøtilsyn (*kommune*)

 **Systemer på undervisningsområdet**
  - Elevadministrationssystemer (*kommune og region)*
  - Systemer vedr. specialundervisning (*kommune*)
  - PPR-systemer (*kommune*)

 **Byggeprojektstyringssystemer**
  - Byggeprojektstyringssystemer (*kommune og* *region*)

 **Systemer på social- og psykiatriområdet**
  - Elektroniske patientjournaler, der ikke indberetter til den fælles E-journal SUP *(region)*.
  - Forskningsdata (*region*)
  - Kliniske kvalitetsdatabaser  *(region)*

 **Systemer på natur- og miljøområdet**
  - Jordforureningssystemer, der ikke indberetter til et overordnet statsligt it-system (*region*)


- Forretningsområde: http://www.form-online.dk/opgavenoegle/65/#65.50.05.10 
- Juridisk kilde: https://www.retsinformation.dk/eli/lta/2003/591 
- Juridisk kilde: https://www.retsinformation.dk/eli/lta/2015/266 
- Juridisk kilde: https://www.retsinformation.dk/eli/lta/2018/183 
- Kilde: https://www.sa.dk/da/offentlig-forvaltning/kommuner-og-regioner/bevaring-kassation-it-systemer 


###  Klassifikation: Offentlige organisationstyper
*Klassifikation, der består af typer af offentlige organisationer set i forhold til styring og forvaltning i dansk administrativ og fællesoffentlig kontekst*
<dl class="def">
  <dt>kommune</dt><dd>mindste offentlige forvaltningsenhed, der styres af en kommunalbestyrelse som bekendtgjort i kommunebestyrelsesloven</dd>
  <dt>region</dt><dd>regional forvaltningsenhed, der styres af et regionsråd, og som er bekendtgjort i regionsloven</dd>
  <dt>statslig myndighed</dt><dd>statslig forvaltningsenhed, som administrerer lovgivning eller forvaltning af et bestemt område</dd>
  <dt>offentlig selvejende institution</dt><dd>selvejende institutioner, foreninger, fonde m.v., der 1) er oprettet ved lov eller i henhold til lov, og 2) er oprettet på privatretligt grundlag, og som udøver offentlig virksomhed af mere omfattende karakter og er undergivet intensiv offentlig regulering, intensivt offentligt tilsyn og intensiv offentlig kontrol</dd>	
</dl>
- Forretningsområde: http://www.form-online.dk/opgavenoegle/05/#05.05 
- Juridisk kilde: https://www.retsinformation.dk/eli/lta/2019/47 
- Juridisk kilde: https://www.retsinformation.dk/eli/lta/2017/319  
- Juridisk kilde: https://www.retsinformation.dk/eli/lta/2006/653 
- Juridisk kilde: https://www.retsinformation.dk/eli/lta/2014/433 
- Distribution: https://data.gov.dk/concept/profile/PublicOrganisationTypes.rdf


### Klassifikation: It-miljøtyper
*Klassifikation, der består af typer af it-miljø, som et it-system kan instantieres i*
<dl class="def">
<dt>demonstration</dt><dd>miljø, der anvendes til at præsentere udviklingsmuligheder som et proof-of-concept</dd>
<dt>udvikling</dt><dd>miljø, hvor den initiale softwareudvikling finder sted</dd>
<dt>test</dt><dd>miljø, der anvendes til afprøvning og kvalitetssikring af ny eller opdateret kode</dd>
<dt>præproduktion</dt><dd>miljø, der anvendes til sidste test inden ibrugtagning, idet miljøet præcist afspejler det endelige produktionsmiljø</dd>
<dt>produktion</dt><dd>miljø, hvor it-systemet går live og kan anvendes af slutbrugerne</dd>
<dt>disaster recovery</dt><dd>miljø, som er et spejl af produktionsmiljøet, og som anvendes ifm. systemgendannelse </dd>
<dt>træning</dt><dd>miljø, der alene anvendes til oplæring af brugere af it-system</dd>
</dl>

Forretningsområde: http://www.form-online.dk/opgavenoegle/68/#68.55.15 
- Kilde: https://en.wikipedia.org/wiki/Deployment_environment 
- Kilde: Statens-it Systemkort
- Kilde: http://priocept.com/2018/01/30/software-environment-naming/
- Kilde: https://docs.microsoft.com/en-us/biztalk/technical-guides/planning-the-development-testing-staging-and-production-environments
- Distribution: https://data.gov.dk/concept/profile/ITEnvironmentTypes.rdf

### Klassifikation: Personoplysningskategorier
*Klassifikation, der består af kategorier af personoplysninger ud fra følsomhed, idet der gælder forskellige betingelser og procedurer for behandling af oplysningerne*

<dl class="def"><dt>1. almindelige personoplysninger</dt><dd>personoplysninger, der ikke er klassificeret som særlige kategorier af oplysninger (følsomme personoplysninger).</dd>
<dt>1.1 personnummeroplysninger</dt><dd>almindelig personoplysning, om personnummer, som har selvstændigt behandlingshjemmel i databeskyttelseslovens § 11</dd>
<dt>1.2 oplysninger om strafbare forhold</dt><dd>almindelig personoplysning, der vedrører straffedomme og lovovertrædelser eller tilknyttede sikkerhedsforanstaltninger (oplysninger om strafbare forhold er ikke følsomme oplysninger i databeskyttelsesforordningens forstand.)</dd>
<dt>2. følsomme personoplysninger</dt><dd>"personoplysninger om:
personoplysninger om:
o Race og etnisk oprindelse
o Politisk overbevisning
o Religiøs eller filosofisk overbevisning
o Fagforeningsmæssige tilhørsforhold
o Genetiske data
o Biometriske data med henblik på entydig identifikation
o Helbredsoplysninger
o Seksuelle forhold eller seksuel orientering</dd>
<dt>3. ingen personoplysninger</dt><dd>Personoplysningskategori, der angiver, at der ikke er informationer om identificerbare fysiske personer tilstede</dd>
</dl>
- Forretningsområde: http://www.form-online.dk/opgavenoegle/05/#05.05.12.60 
- Juridisk kilde: http://data.europa.eu/eli/reg/2016/679/oj 
- Juridisk kilde: https://www.retsinformation.dk/eli/lta/2018/502 
- Kilde: https://www.datatilsynet.dk/media/6567/fortegnelse.pdf 
- Kommentar: De følsomme oplysninger er udtømmende oplistet i databeskyttelsesforordningen, og alle andre oplysninger er derfor almindelige personoplysninger. Bemærk, at oplysninger om strafbare forhold og per-sonnumre betragtes som almindelige personoplysninger, men databeskyttelsesloven fastsætter særlige regler om disse oplysninger.
- Distribution: https://data.gov.dk/concept/profile/PersonalDataCategories.rdf  

### Klassifikation: Fortrolighedsgrader iht. sikkerhedscirkulæret (EU/NATO)
*Klassifikation der består af grader af fortrolighed, forstået som i hvilket omfang information kan videregives iht. sikkerhedscirkulæret (EU/NATO)*
<dl class="def">
<dt>yderst hemmeligt</dt><dd>Denne klassifikationsgrad skal anvendes om informationer, hvis videregivelse uden dertil indhentet bemyndigelse ville kunne forvolde Danmark eller landene i NATO eller EU overordentlig alvorlig skade.</dd>
<dt>hemmeligt</dt><dd>Denne klassifikationsgrad skal anvendes om informationer, hvis videregivelse uden dertil indhentet bemyndigelse ville kunne forvolde Danmark eller landene i NATO eller EU alvorlig skade.</dd>
<dt>fortroligt</dt><dd>Denne klassifikationsgrad skal anvendes om informationer, hvis videregivelse uden dertil indhentet bemyndigelse ville kunne forvolde Danmark eller landene i NATO eller EU skade.</dd>
<dt>til tjenestebrug</dt><dd>Denne klassifikationsgrad anvendes om informationer, der ikke må offentliggøres eller komme til uvedkommendes kendskab.</dd>
<dt>må offentliggøres</dt><dd>Denne klassifikationsgrad anvendes om informationer, som ikke er fortrolige, og som umiddelbart må offentliggøres</dd>
</dl>
- Forretningsområde: http://www.form-online.dk/opgavenoegle/68/#68.55.20 
- Kilde: https://www.retsinformation.dk/eli/retsinfo/2014/10338 
- Distribution https://data.gov.dk/concept/profile/ConfidentialityTypesNatoEU.rdf


### Klassifikation: Arkiveringspligttyper
*Klassifikation, der består af typer af arkiveringspligt set i forhold til, om data skal bevares eller kasseres iht. gældende arkiveringsbestemmelser*
<dl class="def">
<dt>bevaring</dt><dd>arkiveringspligt til at sikre bevaringen af arkivalier, der har historisk værdi eller tjener til dokumentation af forhold af væsentlig administrativ eller retlig betydning for borgere og myndigheder iht. gældende arkiveringsbestemmelser</dd>
<dt>kassation</dt><dd>arkiveringspligt til at kassere ikkebevaringsværdige offentlige arkivalier iht. gældende arkiveringsbestemmelser</dd>
<dt>ved ikke</dt><dd>angivelse af, at arkiveringspligten er ukendt</dd>
</dl>
- Forretningsområde: http://www.form-online.dk/opgavenoegle/65/#65.50.05 
- Juridisk kilde: https://www.retsinformation.dk/eli/lta/2016/1201    


### Klassifikation: Arkiveringsversionsperiodetyper
*Klassifikation, der består af typer af arkiveringsperioder set i forhold til deres afgrænsning.
Kommentar: hvorvidt data i et it-system afleveres som et øjebliksbillede, en afgrænset periode eller ved af-sluttet arkivperiode*
<dl class="def">
<dt>afgrænset periode </dt><dd>Arkiveringsversion, der indeholder data fra en afgrænset periode, hvor der ikke længere rettes i eller tilføjes data</dd>
<dt>øjebliksbillede </dt><dd>Arkiveringsversion, der indeholder samtlige bevaringsværdige data og eventuelle dokumenter på et bestemt tidspunkt</dd>
<dt>afsluttede sager og dokumenter</dt><dd>Arkiveringsversion, der indeholder afsluttede sager og dokumenter</dd>
</dl>
- Forretningsområde: http://www.form-online.dk/opgavenoegle/65/#65.50.05
- Juridisk kilde: https://www.retsinformation.dk/eli/lta/2010/1007     

### Klassifikation: Arkivinstitutionstyper
*Klassifikation, der består af typer af offentlige institutioner, der har til opgave at bevare arkivalier*
<dl class="def">
<dt>stadsarkiv</dt><dd>arkivinstitution oprettet af kommune eller region </dd>
<dt>rigsarkiv</dt><dd>statslig arkivinstitution, som bistår myndigheder omfattet af arkivloven i arkivmæssig henseende</dd>
</dl>
- Forretningsområde: http://www.form-online.dk/opgavenoegle/65/#65.50.05.10 
- Juridisk kilde: https://www.retsinformation.dk/eli/lta/2016/1201 
- Kilde: https://ec.europa.eu/isa2/sites/isa/files/isa2_action_2017_01_standard_based_archival_data_manage-ment_final_report_v1.00.pdf 

### Klassifikation: Konverteringsstatusser
*Klassifikation, der består af statusser ift. konvertering set ud fra omfanget af et (manuelt eller automatisk) datakonverterings- og import forløb*
<dl class="def">
<dt>alle konverteret ind</dt><dd>alle data konverteret og importeret</dd>
<dt>udvalgte data konverteret ind</dt><dd>udvalgte data konverteret og importeret</dd>
<dt>ukendt omfang af import</dt><dd>data er konverteret og importeret, men omfanget er ukendt</dd>
</dl>
- Forretningsområde: http://www.form-online.dk/opgavenoegle/65/#65.50.05
- Kilde: https://www.sa.dk/da/offentlig-forvaltning/ 


Bilag B: Skabelon til registrering i regneark (arkivprofil)
-------------------------------------------------

Vejledning til udfyldelse af skabelon i regneark: 

Regnearksskabelonen kan downloades her: 

https://data.gov.dk/document/itsystem-ap/v1/templates/Excelformular_til_indtastning_af_it-systemoplysninger_arkivprofil.xlsx

Regnearket er et forsimplet forslag til, hvordan oplysningerne kan afgives i struktureret form til Rigsarkivet med anvendelse af det fælles sprog, som standarden etablerer.
I arkiveringssammenhæng er alene instantierede it-systemer i et produktionsmiljø relevante og derud-over kun databærende it-systemer, hvor data er digitalt skabt af den offentlige forvaltning og dom-stolene. Bemærk, at denne forsimplede repræsentation alene giver mulighed for at beskrivelse et it-systems samlede dataindhold (og ikke samtlige datasætrepræsentationer)
- it-system:  system, der består af digitale informationsteknologier
- instantieret it-system:  fysisk instans af et it-system i et bestemt it-miljø
- databærende it-system: instantieret it-system, der indeholder digitalt skabte data eller dokumenter


### Udfyldelse: Myndighedsoplysninger 
<dl class="def">
<dt>myndighedens navn</dt><dd>formel betegnelse for myndigheden (skal udfyldes) </dd>
<dt>myndighedens  hovedmailadresse</dt><dd>e-mailadresse, hvormed myndigheden primært kontaktes (skal udfyldes) </dd>
<dt>myndighedstype (regional, kommunal, statslig)</dt><dd>klassifikation af myndigheden ift. styringsniveau  (skal udfyldes) </dd>
<dt>afgivelsesdato</dt><dd>dato for, hvornår oplysningerne blev afgivet (skal udfyldes) </dd>
</dl>

### Udfyldelse: Basisinformation
<dl class="def">
<dt>it-systemidentifikator</dt><dd>angiv det ID, som entydigt identificerer it-systemet (kan udfyldes) </dd>
<dt>it-systemnavn (fx navn som anført i hovedkontrakten)</dt><dd>angiv it-systemets foretrukne betegnelse  (skal udfyldes) </dd>
<dt>alternativt it-systemnavn</dt><dd>angiv eventuelt øvrige betegnelser eller kaldenavne for it-systemet (kan udfyldes) </dd>
<dt>it-systembeskrivelse</dt><dd>beskriv, til hvilket formål it-systemet er taget i brug i organisationen (skal udfyldes) </dd>
<dt>ibrugtagningsdato </dt><dd>angiv dato, hvor it-systemet blev taget i brug med fuld eller delvis funktionalitet  (skal udfyldes) </dd>
<dt>udfasningsdato</dt><dd>angiv dato, hvor it-systemet blev endeligt blev afviklet (kan udfyldes) </dd>
<dt>version</dt><dd>angiv eventuelt, hvilken version der er taget i anvendelse (kan udfyldes) </dd>
<dt>kommentar</dt><dd>angiv, eventuelt supplerende bemærkninger eller oplysninger (kan udfyldes) </dd>
<dt>indeholder data</dt><dd>angiv om it-systemet indeholder digitalt skabte data (skal udfyldes) </dd>
<dt>indeholder dokumenter</dt><dd>angiv, om it-systemet indeholder digitalt skabte dokumenter (skal udfyldes) </dd>
<dt>dokumentationsreference</dt><dd>angiv reference(r) til dokumentation af it-systemet (kan udfyldes) </dd>
<dt>rettighedshaver</dt><dd>organisation, der ejer eller har dispositionsretten over de intellektuelle rettigheder over it-systemets primære softwareprodukt (kan udfyldes) </dd></dl>

### Udfyldelse: Opgaver
<dl class="def"> 
<dt>FORM-opgave(r)</dt><dd>(for regioner og statslige administrative enheder) angiv FORM-opgave(r), som it-systemet understøtter (fx 65.50.05.10 Sagsarkivering) el. overord-net serviceområde (kan udfyldes) </dd>
<dt>KLE-emne(r) </dt><dd>(for kommuner) angiv  KLE-emne(r) som it-systemet understøtter (fx 85.08.00 arkivering i almindelighed) el. overordnet emnegruppe (kan udfyldes) </dd>
<dt>lovgrundlag</dt><dd>angiv reference(r) til juridisk ressource, som danner grundlag for syste-mets anvendelse (kan udfyldes) </dd>
<dt>sagsområde(r) </dt><dd>angiv, hvilket sagsområde iht. bekendtgørelser for bevaring og kassation af digitale arkivalier it-systemet tilhører (kan udfyldes for regioner og kommuner) </dd>
<dt>forgængersystem</dt><dd>angiv it-system, der tidligere har varetaget samme funktion (kan udfyldes) </dd>
</dt><dd></dl>

### Udfyldelse: Styring
<dl class="def"></dt><dd> 
<dt>it-systemejer</dt><dd>angiv organisatorisk enhed eller person med det overordnede ansvar for et givent it-systems drift, vedligehold og anvendelse (kan udfyldes) </dd></dl>

### Udfyldelse: Information
<dl class="def"> 
<dt>datasætID</dt><dd>angiv datasættes unikke ID (kan udfyldes) </dd>
<dt>dataansvarlig</dt><dd>angiv den organisation, som har dispositionsretten og træffer afgørelse om hvordan data skal behandles (skal udfyldes) </dd>
<dt>dataskaber </dt><dd>angiv den organisation, der har det primære ansvar for tilvejebringelsen af datasættet (skal udfyldes) </dd>
<dt>titel</dt><dd>angiv datasættets navn (det eller de ord, der navngiver data i it-systemet) (kan udfyldes) </dd>
<dt>beskrivelse</dt><dd>beskriv datasættets formål og indhold (fx datasættet indeholder journal-sager fra kommune x) (kan udfyldes) </dd>
<dt>versionsnummer</dt><dd>angiv eventuelt datasættets versionsnummer (kan udfyldes) </dd>
<dt>personoplysningskategori</dt><dd>angiv, om it-systemet indeholder almindelige personoplysninger, følsom-me personoplysninger eller oplysninger om strafbare forhold (flere skal kunne vælges - udestår pt) (kan udfyldes) </dd>
<dt>fortrolighedsgrad  iht. sikkerhedscirkulæret</dt><dd>angiv, i hvilket omfang information kan videregives iht. sikkerhedscirkulæ-ret (EU/NATO) () </dd>
<dt>fortrolighedsgrad  iht. ISO 27001</dt><dd>angiv, i hvilket omfang information kan videregives iht. informationssik-kerhedsstandarden ISO 27002 (kan udfyldes) </dd>
<dt>arkiveringspligttype</dt><dd>angiv, hvorvidt data skal bevares eller kasseres iht. gældende arkiverings-bestemmelser (for data bestemt til bevaring skal der afleveres arkiveringsversioner til et offentligt arkiv) (kan udfyldes) </dd>
<dt>arkiveringsfrekvens</dt><dd>angiv, hvor ofte der fremstilles arkiveringsversioner af datasættet (kan udfyldes) </dd>
<dt>arkiveringsperiodetype</dt><dd>angiv, hvorvidt data afleveres som et øjebliksbillede, en afgrænset periode eller ved afsluttet arkivperiode  (kan udfyldes) </dd>
<dt>data konverteret fra  it-system</dt><dd> hvis der manuelt eller maskinelt er blevet konverteret data ind fra et andet it-system, så angiv navnet på dette it-system (kan udfyldes) </dd>
<dt>datakonverteringsstatus</dt><dd>angiv, om alle eller udvalgte data er konverteret ind fra forgængersystem (kan udfyldes) </dd>
<dt>første datatilføjelse</dt><dd>angiv dato for første datatilføjelse (skal udfyldes) </dd>
<dt>sidste datatilføjelse</dt><dd>angiv dato for sidste datatilføjelse (skal udfyldes) </dd>
<dt>næste datasletningsfrist</dt><dd>angiv  førstkommende dato for, hvornår bestemte data i it-systemet for-ventes at skulle være slettet forinden iht. GDPR (kan udfyldes) </dd>
<dt>tidligere arkivering</dt><dd>angivelse af, om data fra it-systemet tidligere er blevet arkiveret (kan udfyldes) </dd>
<dt>seneste arkivversion: startårstal</dt><dd>angiv det årstal, seneste arkiveringsversion først dækker (kan udfyldes) </dd>
<dt>seneste arkivversion: slutårstal</dt><dd>angiv det årstal, seneste arkiveringsversion sidst dækker (kan udfyldes) </dd>
</dl>




Bilag C: Eksempel på maskinlæsbart format 
-------------------------------------------------

(Her RDF-XML og Turtle, men andre serialiseringer mulige, herunder JSON-LD) 

### EKSEMPELOUTPUT I TURTLE (Acadre anvendt i kommune X)
```
	@prefix skos: <http://www.w3.org/2004/02/skos/core#> .
	@prefix dc: <http://purl.org/dc/terms/> .
	@prefix sys: <https://data.gov.dk/model/core/itsystem#> .
	@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .
	@prefix archv: <https://data.gov.dk/model/core/digitalarchival/> .
	@prefix infra: <https://data.gov.dk/model/core/infrastructure/> .
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
	  archv:applicableCaseArea <https://data.gov.dk/concept/core/ArchivalCaseArea#ESDH-systemMedJournalsager> ;
	  schema:audience <https://data.gov.dk/concept/core/itsystemcriticalitytype#employees> ;
	  sys:hasCriticality <https://data.gov.dk/concept/core/itsystemcriticalitytype#CriticalForBusiness> ;
	  sys:hasAquisitionType <https://data.gov.dk/concept/core/itsystemaquisitiontype#Commercial-off-the-shelf> ;
	  infra:instanceOfProductInSeries "Acadre CM"^^xsd:string ;
	  archv:containsData True ;
	  archv:containsDigitalDocuments True ;
	  dc:hasPart <https://EXAMPLEURI2> .

	<https://EXAMPLEURI2>
	  a dcat:Dataset ;
	  dcat-dk:dataResponsibleOrganisation "Kommune x"@da ;
	  dcat-dk:personalDataCategory <https://data.gov.dk/model/classification/PersonalDataCategory#GeneralPersonalData> ;
	  dc:description "Journalsager fra komnune x"@da ;
	  archv:archivalObligationType <https://data.gov.dk/concept/core/ArchivalObligationType#Archival> ;
	  archv:plannedArchiveType <https://data.gov.dk/concept/core/ArchivalFrequencyType#SpecificPeriod> ;
	  archv:plannedArchivalFrequency <https://data.gov.dk/concept/core/ArchivalFrequencyType#5> ;
	  archv:previousArchiving True .

	<https://EXAMPLEURI3>
	  a sys:InstantiatedITSystem ;
	  sys:actsAs <https://data.gov.dk/concept/coreitenvironmenttype#Production> ;
	  sys:instantiationOf <https://EXAMPLEURI1> ;
	  sys:producesDataset <https://EXAMPLEURI4> ;
	  archv:latestArchiveInformationPackage [
	    a archv:ArchiveInformationPackage ;
	    dc:hasPart <https://EXAMPLEURI5>
	  ] .

	<https://EXAMPLEURI4>
	  a dcat:Distribution ;
	  dc:issued "2019-02-01"^^xsd:date ;
	  dc:modified ""^^xsd:date .

	<https://EXAMPLEURI5>
	  a dcat:Distribution ;
	  dc:issued "2002"^^xsd:date ;
	  dc:modified "2007"^^xsd:date .
```

### EKSEMPELOUTPUT I RDF/XML
```
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
	  xmlns:sys="https://data.gov.dk/model/core/itsystem/"
	  xmlns:archv="https://data.gov.dk/model/core/digitalarchival/"
	  xmlns:infra="https://data.gov.dk/model/core/infrastructure/"  > 

	<!-- IT-SYSTEM -->                    
	<rdf:Description rdf:about="https://EXAMPLEURI1">
	<rdf:type rdf:resource="https://data.gov.dk/model/core/itsystem#ITSystem"/>
	<skos:prefLabel xml:lang="da">Acadre </skos:prefLabel>
	<skos:altLabel xml:lang="da">Acadre CM</skos:altLabel>
	<dct:description xml:lang="da">Acadre anvendes i kommune X til sagsstyring og ledelsesrapporte-ring</dct:description>
	<sys:inUseFromDate rdf:datatype="http://www.w3.org/2001/XMLSchema#date">2019-01-01</sys:inUseFromDate>
	<sys:hasApplicationPurposeFORM rdf:resource="http://www.form-online.dk/opgavenoegle/65/#65.50.05"/>
	<sys:hasApplicationPurposeKLE rdf:resource="http://www.kle-online.dk/emneplan/85/#_85.02.10"/>
	<archv:applicableCaseArea rdf:resource="https://data.gov.dk/concept/coreArchivalCaseArea#ESDH-systemMedJournalsager"/>
	<schema:audience rdf:resource="https://data.gov.dk/concept/coreitsystemcriticalitytype#employees"/>
	<sys:hasCriticality rdf:resource="https://data.gov.dk/concept/coreitsystemcriticalitytype#CriticalForBusiness"/>
	<sys:hasAquisitionType rdf:resource="https://data.gov.dk/concept/coreitsystemaquisitiontype#Commercial-off-the-shelf"/>
	<infra:instanceOfProductInSeries rdf:datatype="http://www.w3.org/2001/XMLSchema#string">Acadre CM</infra:instanceOfProductInSeries>
	<archv:containsData rdf:datatype="http://www.w3.org/2001/XMLSchema#boolean">True</archv:containsData>
	<archv:containsDigitalDocuments rdf:datatype="http://www.w3.org/2001/XMLSchema#boolean">True</archv:containsDigitalDocuments>
	<dct:hasPart rdf:resource="https://EXAMPLEURI2"/>
	 </rdf:Description>

	<!-- IT-SYSTEMETS DATAINDHOLD (ET LOGISK DATASÆT)-->  
	<rdf:Description rdf:about="https://EXAMPLEURI2">
	<rdf:type rdf:resource="http://www.w3.org/ns/dcat#Dataset"/>
	<dcat-dk:dataResponsibleOrganisation xml:lang="da">Kommune x</dcat-dk:dataResponsibleOrganisation>
	<dcat-dk:personalDataCategory rdf:resource="https://data.gov.dk/model/classification/PersonalDataCategory#GeneralPersonalData"/>	
	<dct:description xml:lang="da">Journalsager fra komnune x</dct:description>	
	<archv:archivalObligationType rdf:resource="https://data.gov.dk/concept/coreArchivalObligationType#Archival"/>
	<archv:plannedArchiveType rdf:resource="https://data.gov.dk/concept/coreArchivalFrequencyType#SpecificPeriod"/>
	<archv:plannedArchivalFrequency rdf:resource="https://data.gov.dk/concept/coreArchivalFrequencyType#5"/>
	<archv:previousArchiving rdf:datatype="http://www.w3.org/2001/XMLSchema#boolean">True</archv:previousArchiving>
	</rdf:Description>

	<!-- IT-SYSTEMETS FYSISKE INSTANTIERING I ET IT-MILJØ --> 
	<rdf:Description rdf:about="https://EXAMPLEURI3">
	    <rdf:type rdf:resource="https://data.gov.dk/model/core/itsystem#InstantiatedITSystem"/>
	    <sys:actsAs rdf:resource="https://data.gov.dk/concept/coreitenvironmenttype#Production"/>
	    <sys:instantiationOf rdf:resource="https://EXAMPLEURI1"/>

	<!-- DET INSTANTIEREDE IT-SYSTEMS KONKRETE DATA-->	
		<sys:producesDataset>
		<rdf:Description rdf:about="https://EXAMPLEURI4">
		  <rdf:type rdf:resource="http://www.w3.org/ns/dcat#Distribution"/>
		    <dct:issued rdf:datatype="http://www.w3.org/2001/XMLSchema#date">2019-02-01</dct:issued>
		    <dct:modified rdf:datatype="http://www.w3.org/2001/XMLSchema#date"></dct:modified>
		  </rdf:Description>
		</sys:producesDataset>	
		
	<!-- DET INSTANTIEREDE IT-SYSTEMS SENESTE KONKRETE ARKIVERINGSVERSION-->		
		<archv:latestArchiveInformationPackage>
		<archv:ArchiveInformationPackage>
		<dct:hasPart>
		  <rdf:Description rdf:about="https://EXAMPLEURI5">
		  <rdf:type rdf:resource="http://www.w3.org/ns/dcat#Distribution"/>
		    <dct:issued rdf:datatype="http://www.w3.org/2001/XMLSchema#date">2002</dct:issued>
		    <dct:modified rdf:datatype="http://www.w3.org/2001/XMLSchema#date">2007</dct:modified>
		  </rdf:Description>
		</dct:hasPart>
		</archv:ArchiveInformationPackage>
		</archv:latestArchiveInformationPackage>
	</rdf:Description>
	</rdf:RDF>
```

Bilag D: Om datamodellen
-------------------------------------------------
Selve UML-modellerne er udstillet her : 
https://data.gov.dk/document/itsystem-ap/v1/uml/


Bilag E: UML-diagram: Arkivprofil
-------------------------------------------------
- Namespace: https://data.gov.dk/model/profile/itsystemap-archv/ 
- Modelnavn (label): Indmeldelse af it-systemoplysninger til Rigsarkivet
- Modelansvarlig (responsibleEntity): Rigsarkivet (projektgruppen)
- Versionnummer (versionInfo): 1.0.0
- Seneste opdateringsdato (dateModified): 11-11-2019
- Modelstatus (modelStatus): Development
- Godkendelsesstatus (approvalStatus): Afventer godkendelse
- Modelomfang (modelScope): Anvendelsesmodel
- Forretningsområde (theme):  65.50.05.10 Sagsarkivering  
- Kommentar (comment): Anvendelsesprofil for det sæt af oplysningstyper, der er påkrævet eller anbefalet ifm. afgivelse af it-systemoplysninger til Rigsarkivet 

<p align="center"><img src="img/Bilag-E-UML-diagram-Arkivprofil.png" alt="UML-diagram" title="UML-diagram" width="800"/></p>


Bilag F: Begrebsliste til Arkivprofilen (archvSYS-AP)
-------------------------------------------------
- Namespace: https://data.gov.dk/concept/profile/itsystemap-archv/ 
- Modelnavn (label): Begrebsliste til arkivprofilen
- Modelansvarlig (responsibleEntity): Rigsarkivet (projektgruppen)
- Versionnummer (versionInfo): 1.0.0
- Seneste opdateringsdato (dateModified): 11-11-2019
- Modelstatus (modelStatus): development
- Godkendelsesstatus (approvalStatus): afventer godkendelse
- Forretningsområde (theme):  65.50.05.10 Sagsarkivering  
- Afledt af (wasDerivedFrom): https://data.gov.dk/concept/core/digitalarchival/ 
- Afledt af (wasDerivedFrom): https://data.gov.dk/concept/core/itsystem/
- Kommentar (comment): Samlet begrebsliste med begreber, der er relevante ifm. afgivelse af oplysninger om it-systemer til Rigsarkivet. Bemærk, at denne anvendelsesorienterede begrebsliste udvælger og sammensætter begreber fra forskellige emneområder, se fx begrebsmodellen for it-system og begrebsmodellen for digital arkivering, som er udstillet online. 


<table>
<thead>
<tr>
<td>
<p><strong>Foretrukken dansk term</strong></p>
</td>
<td>
<p><strong>Definition</strong></p>
</td>
<td>
<p><strong>Juridisk kilde</strong></p>
</td>
<td>
<p><strong>Kilde</strong></p>
</td>
<td>
<p><strong>Tilh&oslash;rer emneomr&aring;de</strong></p>
</td>
<td>
<p><strong>Foretrukken engelsk term </strong></p>
</td>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>arkiveringsfrekvens</strong></p>
</td>
<td>
<p><em>frekvens med hvilken arkiveringsversioner af datas&aelig;t fremstilles</em></p>
</td>
<td>&nbsp;</td>
<td>
<p>https://os2.eu/sites/default/files/documents/notat_om_felter_til_registrering_af_arkiveringsdata_i_kitos.pdf</p>
</td>
<td>
<p>https://data.gov.dk/model/concept/digitalarchival#</p>
</td>
<td>
<p>archiving frequency</p>
</td>
</tr>
<tr>
<td>
<p><strong>arkiveringsleverand&oslash;r</strong></p>
</td>
<td>
<p><em>leverand&oslash;r, som varetager fremstillingen af arkiveringsversionen</em></p>
</td>
<td>&nbsp;</td>
<td>
<p>https://os2.eu/sites/default/files/documents/notat_om_felter_til_registrering_af_arkiveringsdata_i_kitos.pdf</p>
</td>
<td>
<p>https://data.gov.dk/model/concept/digitalarchival#</p>
</td>
<td>
<p>archiving supplier</p>
</td>
</tr>
<tr>
<td>
<p><strong>arkiveringspligttype</strong></p>
</td>
<td>
<p><em>type af arkiveringspligt set ud fra, hvorvidt et it-system er arkiveringspligtigt eller ikke skal arkiveres</em></p>
</td>
<td>
<p>https://www.retsinformation.dk/eli/lta/2016/1201</p>
</td>
<td>
<p>https://os2.eu/sites/default/files/documents/notat_om_felter_til_registrering_af_arkiveringsdata_i_kitos.pdf</p>
</td>
<td>
<p>https://data.gov.dk/model/concept/digitalarchival#</p>
</td>
<td>
<p>archival obligation type</p>
</td>
</tr>
<tr>
<td>
<p><strong>arkiveringstestinstitution</strong></p>
</td>
<td>
<p><em>organisation, som tester arkiveringsversionen</em></p>
</td>
<td>&nbsp;</td>
<td>
<p>https://os2.eu/sites/default/files/documents/notat_om_felter_til_registrering_af_arkiveringsdata_i_kitos.pdf</p>
</td>
<td>
<p>https://data.gov.dk/model/concept/digitalarchival#</p>
</td>
<td>
<p>archive test organisation</p>
</td>
</tr>
<tr>
<td>
<p><strong>arkiveringsversion</strong></p>
</td>
<td>
<p><em>data eller dokumenter fra it-systemer skabt i en afgr&aelig;nset periode af den offentlige forvaltning og domstolene, og som af Rigsarkivet er bestemt til arkivering</em></p>
</td>
<td>
<p>https://www.retsinformation.dk/eli/lta/2010/1007</p>
</td>
<td>&nbsp;</td>
<td>
<p>https://data.gov.dk/model/concept/digitalarchival#</p>
</td>
<td>
<p>archive information package</p>
</td>
</tr>
<tr>
<td>
<p><strong>arkiveringsversionsperiode</strong></p>
</td>
<td>
<p><em>periode med angivelse af startdato og slutdato, i hvilken de afleverede data er skabt</em></p>
</td>
<td>&nbsp;</td>
<td>
<p>https://os2.eu/sites/default/files/documents/notat_om_felter_til_registrering_af_arkiveringsdata_i_kitos.pdf</p>
</td>
<td>
<p>https://data.gov.dk/model/concept/digitalarchival#</p>
</td>
<td>
<p>archive version periode</p>
</td>
</tr>
<tr>
<td>
<p><strong>arkiveringsversionsgodkendelsesstatus</strong></p>
</td>
<td>
<p><em>status, som indikerer, at arkiveringsversionen er blevet godkendt af den modtagende arkivinstitution</em></p>
</td>
<td>&nbsp;</td>
<td>
<p>https://os2.eu/sites/default/files/documents/notat_om_felter_til_registrering_af_arkiveringsdata_i_kitos.pdf</p>
</td>
<td>
<p>https://data.gov.dk/model/concept/digitalarchival#</p>
</td>
<td>
<p>archive version approval status</p>
</td>
</tr>
<tr>
<td>
<p><strong>arkiveringsversionsperiodetype</strong></p>
</td>
<td>
<p><em>type af arkiveringsperioder set i forhold til afgr&aelig;nsning i tid</em></p>
</td>
<td>
<p>https://www.retsinformation.dk/eli/lta/2010/1007</p>
</td>
<td>&nbsp;</td>
<td>
<p>https://data.gov.dk/model/concept/digitalarchival#</p>
</td>
<td>
<p>archive type</p>
</td>
</tr>
<tr>
<td>
<p><strong>arkivinstitution</strong></p>
</td>
<td>
<p><em>offentlig institution, der har til opgave at bevare arkivalier</em></p>
</td>
<td>&nbsp;</td>
<td>
<p>https://ec.europa.eu/isa2/sites/isa/files/isa2_action_2017_01_standard_based_archival_data_management_final_report_v1.00.pdf</p>
</td>
<td>
<p>https://data.gov.dk/model/concept/digitalarchival#</p>
</td>
<td>
<p>archive organisation</p>
</td>
</tr>
<tr>
<td>
<p><strong>arkivserie</strong></p>
</td>
<td>
<p><em>samlet gruppe af arkivalier</em></p>
</td>
<td>&nbsp;</td>
<td>
<p>https://www.ica.org/sites/default/files/CBPS_2000_Guidelines_ISAD%28G%29_Second-edition_EN.pdf</p>
</td>
<td>
<p>https://data.gov.dk/model/concept/digitalarchival#</p>
</td>
<td>
<p>archive series</p>
</td>
</tr>
<tr>
<td>
<p><strong>arkivskaber</strong></p>
</td>
<td>
<p><em>den eller de myndigheder, der har skabt arkivaliet. Kan ogs&aring; v&aelig;re organisatoriske enheder inden for en myndighed eller andre bidragydere til arkivaliet</em></p>
</td>
<td>
<p>https://www.retsinformation.dk/eli/lta/2010/1007</p>
</td>
<td>&nbsp;</td>
<td>
<p>https://data.gov.dk/model/concept/digitalarchival#</p>
</td>
<td>
<p>archive creator</p>
</td>
</tr>
<tr>
<td>
<p><strong>dataansvarlig </strong></p>
</td>
<td>
<p><em>organisation, som har det administrative ansvar for data </em></p>
</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>
<p>data responsible organisation</p>
</td>
</tr>
<tr>
<td>
<p><strong>databehandler</strong></p>
</td>
<td>
<p><em>en fysisk eller juridisk person, en offentlig myndighed, en institution eller et andet organ, der behandler personoplysninger p&aring; den dataansvarliges vegne</em></p>
</td>
<td>
<p>http://data.europa.eu/eli/reg/2016/679/oj</p>
</td>
<td>&nbsp;</td>
<td>
<p>https://data.gov.dk/model/concept/dataprotection#</p>
</td>
<td>
<p>data processor</p>
</td>
</tr>
<tr>
<td>
<p><strong>datakonvertering</strong></p>
</td>
<td>
<p><em>konvertering af data fra et format til et andet</em></p>
</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>
<p>https://data.gov.dk/model/concept/digitalarchival#</p>
</td>
<td>
<p>data conversion</p>
</td>
</tr>
<tr>
<td>
<p><strong>datakonverteringsstatus</strong></p>
</td>
<td>
<p><em>status ift. datakonverterings- og import forl&oslash;b</em></p>
</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>
<p>https://data.gov.dk/model/concept/digitalarchival#</p>
</td>
<td>
<p>data conversion status</p>
</td>
</tr>
<tr>
<td>
<p><strong>dataskaber</strong></p>
</td>
<td>
<p><em>organisation, der har det prim&aelig;re ansvar for tilvejebringelsen af datas&aelig;ttet</em></p>
</td>
<td>&nbsp;</td>
<td>
<p><a href="https://joinup.ec.europa.eu/solution/dcat-application-profile-data-portals-europe">https://joinup.ec.europa.eu/solution/dcat-application-profile-data-portals-europe</a></p>
</td>
<td>
<p>https://data.gov.dk/model/concept/dataset#</p>
</td>
<td>
<p>data creator</p>
</td>
</tr>
<tr>
<td>
<p><strong>datasletning</strong></p>
</td>
<td>
<p><em>sletning af alle link til eller kopier eller gengivelser af de p&aring;g&aelig;ldende personoplysninger</em></p>
</td>
<td>
<p>http://data.europa.eu/eli/reg/2016/679/oj</p>
</td>
<td>&nbsp;</td>
<td>
<p>https://data.gov.dk/model/concept/digitalarchival#</p>
</td>
<td>
<p>data erasure</p>
</td>
</tr>
<tr>
<td>
<p><strong>datasletningsfrist</strong></p>
</td>
<td>
<p><em>dato for, hvorn&aring;r data i systemet forventes at skulle v&aelig;re slettet forinden</em></p>
</td>
<td>
<p>https://www.datatilsynet.dk/media/6560/dataansvarlige-og-databehandlere.pdf</p>
</td>
<td>
<p>https://os2.eu/sites/default/files/documents/notat_om_felter_til_registrering_af_arkiveringsdata_i_kitos.pdf</p>
</td>
<td>
<p>https://data.gov.dk/model/concept/digitalarchival#</p>
</td>
<td>
<p>data erasure deadline</p>
</td>
</tr>
<tr>
<td>
<p><strong>datas&aelig;t</strong></p>
</td>
<td>
<p><em>samling af data sammenstillet af en enkelt akt&oslash;r</em></p>
</td>
<td>&nbsp;</td>
<td>
<p>https://www.w3.org/TR/vocab-dcat/,</p>
</td>
<td>
<p>https://data.gov.dk/model/concept/dataset#</p>
</td>
<td>
<p>dataset</p>
</td>
</tr>
<tr>
<td>
<p><strong>datas&aelig;trepr&aelig;sentation</strong></p>
</td>
<td>
<p><em>specifik fysisk repr&aelig;sentation af et datas&aelig;t</em></p>
</td>
<td>&nbsp;</td>
<td>
<p>https://www.w3.org/TR/vocab-dcat/,</p>
</td>
<td>
<p>https://data.gov.dk/model/concept/datasetdistribution#</p>
</td>
<td>
<p>distribution</p>
</td>
</tr>
<tr>
<td>
<p><strong>den registrerede</strong></p>
</td>
<td>
<p><em>person, om hvem oplysninger behandles</em></p>
</td>
<td>
<p>http://data.europa.eu/eli/reg/2016/679/oj</p>
</td>
<td>
<p>Referencearkitektur for deling af data og dokumenter</p>
</td>
<td>
<p>https://data.gov.dk/model/concept/dataprotection#</p>
</td>
<td>
<p>data subject</p>
</td>
</tr>
<tr>
<td>
<p><strong>forg&aelig;ngersystem</strong></p>
</td>
<td>
<p><em>system, der tidligere har varetaget samme funktion</em></p>
</td>
<td>
<p>https://www.retsinformation.dk/eli/lta/2010/1007</p>
</td>
<td>&nbsp;</td>
<td>
<p>https://data.gov.dk/model/concept/itsystem#</p>
</td>
<td>
<p>predessor system</p>
</td>
</tr>
<tr>
<td>
<p><strong>fortrolighedsgrad</strong></p>
</td>
<td>
<p><em>grad af fortrolighed, forst&aring;et som i hvilket omfang information kan videregives</em></p>
</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>
<p>https://data.gov.dk/model/concept/informationsecurity#</p>
</td>
<td>
<p>confidentiality type</p>
</td>
</tr>
<tr>
<td>
<p><strong>fortrolighedsgrad iht. Sikkerhedscirkul&aelig;ret</strong></p>
</td>
<td>
<p><em>fortrolighedsgrad, forst&aring;et som i hvilket omfang information kan videregives iht. Sikkerhedscirkul&aelig;ret (Nato &amp; EU Dataklassifikation)</em></p>
</td>
<td>
<p>https://www.retsinformation.dk/eli/retsinfo/2014/10338</p>
</td>
<td>&nbsp;</td>
<td>
<p>https://data.gov.dk/model/concept/informationsecurity#</p>
</td>
<td>
<p>Nato &amp; EU Data Classification</p>
</td>
</tr>
<tr>
<td>
<p><strong>informationssystem</strong></p>
</td>
<td>
<p><em>system til indsamling, organisering, lagring og kommunikation af viden</em></p>
</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>
<p>https://data.gov.dk/model/concept/itsystem#</p>
</td>
<td>
<p>information system</p>
</td>
</tr>
<tr>
<td>
<p><strong>instantieret it-system</strong></p>
</td>
<td>
<p><em>fysisk instans af et it-system i et bestemt it-milj&oslash;</em></p>
</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>
<p>https://data.gov.dk/model/concept/itsysteInstancem#</p>
</td>
<td>
<p>IT system instance</p>
</td>
</tr>
<tr>
<td>
<p><strong>it-milj&oslash;type</strong></p>
</td>
<td>
<p><em>type af it-milj&oslash;, som et it-system kan instantieres i</em></p>
</td>
<td>&nbsp;</td>
<td>
<p>https://en.wikipedia.org/wiki/Deployment_environment<br /> Statens-IT Systemkort</p>
</td>
<td>
<p>https://data.gov.dk/model/concept/itsystem#</p>
</td>
<td>
<p>environment type</p>
</td>
</tr>
<tr>
<td>
<p><strong>it-system</strong></p>
</td>
<td>
<p><em>system, der best&aring;r af digitale informationsteknologier</em></p>
</td>
<td>&nbsp;</td>
<td>
<p>https://www.iso.org/standard/63711.html</p>
</td>
<td>
<p>https://data.gov.dk/model/concept/itsystem#</p>
</td>
<td>
<p>IT system</p>
</td>
</tr>
<tr>
<td>
<p><strong>it-systemejer</strong></p>
</td>
<td>
<p><em>person eller organisation med det overordnede ansvar for et givet it-systems drift, vedligehold og anvendelse</em></p>
</td>
<td>&nbsp;</td>
<td>
<p>https://digst.dk/styring/systemstyring/model-for-portefoeljestyring-af-statslige-it-systemer/</p>
</td>
<td>
<p>https://data.gov.dk/model/concept/itsystem#</p>
</td>
<td>
<p>IT system owner</p>
</td>
</tr>
<tr>
<td>
<p><strong>retskilde</strong></p>
</td>
<td>
<p><em>intellektuelt v&aelig;rk, der fasts&aelig;tter juridiske regler og retsbestemmelser</em></p>
</td>
<td>&nbsp;</td>
<td>
<p><a href="https://publications.europa.eu/en/web/eu-vocabularies/model/-/resource/dataset/eli">https://publications.europa.eu/en/web/eu-vocabularies/model/-/resource/dataset/eli</a></p>
</td>
<td>
<p>https://data.gov.dk/model/concept/legalresource#</p>
</td>
<td>
<p>legal resource</p>
</td>
</tr>
<tr>
<td>
<p><strong>offentlig forvaltningsopgavetype</strong></p>
</td>
<td>
<p><em>type af opgave, der udf&oslash;res af offentlige organisationer</em></p>
</td>
<td>&nbsp;</td>
<td>
<p><a href="https://arkitektur.digst.dk/rammearkitektur/datastandarder/anvendelsesprofil-organisationer">https://arkitektur.digst.dk/rammearkitektur/datastandarder/anvendelsesprofil-organisationer</a></p>
</td>
<td>
<p>https://data.gov.dk/model/concept/organisation#</p>
</td>
<td>
<p>public administrative task type</p>
</td>
</tr>
<tr>
<td>
<p><strong>organisation</strong></p>
</td>
<td>
<p><em>samling mennesker, der er organiseret i et f&aelig;llesskab eller anden social, kommerciel eller politisk struktur</em></p>
</td>
<td>&nbsp;</td>
<td>
<p>http://www.w3.org/ns/org#;<br /><a href="https://arkitektur.digst.dk/rammearkitektur/datastandarder/anvendelsesprofil-organisationer">https://arkitektur.digst.dk/rammearkitektur/datastandarder/anvendelsesprofil-organisationer</a></p>
</td>
<td>
<p>https://data.gov.dk/model/concept/organisation#</p>
</td>
<td>
<p>organization</p>
</td>
</tr>
<tr>
<td>
<p><strong>persondataansvarlig</strong></p>
</td>
<td>
<p><em>en fysisk eller juridisk person, en offentlig myndighed, en institution eller et andet organ, der alene eller sammen med andre afg&oslash;r, til hvilke form&aring;l og med hvilke hj&aelig;lpemidler der m&aring; foretages behandling af personoplysninger</em></p>
</td>
<td>
<p>http://data.europa.eu/eli/reg/2016/679/oj</p>
</td>
<td>
<p>https://w3id.org/GDPRtEXT#Processor</p>
</td>
<td>
<p>https://data.gov.dk/model/concept/dataprotection#</p>
</td>
<td>
<p>controller</p>
</td>
</tr>
<tr>
<td>
<p><strong>personoplysningskategori</strong></p>
</td>
<td>
<p><em>kategori af personoplysninger set i forhold til f&oslash;lsomhed, idet der g&aelig;lder forskellige betingelser og procedurer for behandling af oplysningerne</em></p>
</td>
<td>
<p>http://data.europa.eu/eli/reg/2016/679/oj</p>
</td>
<td>
<p>https://www.datatilsynet.dk/media/6567/fortegnelse.pdf</p>
</td>
<td>
<p>https://data.gov.dk/model/concept/dataprotection#</p>
</td>
<td>
<p>personal data category</p>
</td>
</tr>
<tr>
<td>
<p><strong>personoplysningsunderkategori</strong></p>
</td>
<td>
<p><em>underkategori af personoplysningskategori, som pr&aelig;ciserer hvilken type af persondata systemet indeholder</em></p>
</td>
<td>&nbsp;</td>
<td>
<p>notat om GDPR-modul i KITOS</p>
</td>
<td>
<p>https://data.gov.dk/model/concept/dataprotection#</p>
</td>
<td>
<p>personal data subcategory</p>
</td>
</tr>
<tr>
<td>
<p><strong>sagsomr&aring;de</strong></p>
</td>
<td>
<p><em>kategori af sager iht. bekendtg&oslash;relser for bevaring og kassation af digitale arkivalier p&aring; det regionale eller kommunale omr&aring;de</em></p>
</td>
<td>
<p>https://www.retsinformation.dk/eli/lta/2003/591;</p>
<p>https://www.retsinformation.dk/eli/lta/2015/266; https://www.retsinformation.dk/eli/lta/2018/183;&nbsp;</p>
</td>
<td>
<p>https://www.sa.dk/da/offentlig-forvaltning/kommuner-og-regioner/bevaring-kassation-it-systemer/</p>
</td>
<td>
<p>https://data.gov.dk/model/concept/digitalarchival#</p>
</td>
<td>
<p>case area</p>
</td>
</tr>
<tr>
<td>
<p><strong>system</strong></p>
</td>
<td>
<p><em>kombination af interagerende elementer, der er organiseret for at opn&aring; et eller flere erkl&aelig;rede form&aring;l</em></p>
</td>
<td>&nbsp;</td>
<td>
<p>ISO/IEC 15288: https://www.iso.org/standard/63711.html</p>
</td>
<td>
<p>https://data.gov.dk/model/concept/system#</p>
</td>
<td>
<p>system</p>
</td>
</tr>
</tbody>
</table>

---


Dette dokument 'Standard for beskrivelse af it-systemer - Arkivprofil (archvSYS-AP)' udgør en fællesoffentlig standard for beskrivelse af offentlige myndigheders it-systemer ifm. afgivelse af it-systemoplysninger til Rigsarkivet.


arkitektur.digst.dk

---

<pre class=biblio>

{
	"[ISO15288]": {
		"href": "https://www.iso.org/standard/63711.html",
		"title": "ISO/IEC 15288 (Systems and software engineering -- System life cycle processes)",
		"publisher": "ISO"
		]
	}
}
</pre>

* * * * *



[[3]]() Information technology --- Framework and taxonomy of International Standardized Profiles og ISO/IEC TR 12182:2015 (Systems and software engineering -- -- Framework for categorization of IT systems and software, and guide for applying it .

[[4]]() Klassifikationer beskrives iht. anvendelsesprofil for klassifikation: <https://arkitektur.digst.dk/rammearkitektur/datastandarder/anvendelsesprofil-klassifikationer>

[[5]]() <https://arkitektur.digst.dk/mandat-og-styring/hvidbog-om-faellesoffentlig-digital-arkitektur>

[[6]]() Myndigheder skal beskrives som organisationer iht. anvendelsesprofil for organisationer: <https://arkitektur.digst.dk/rammearkitektur/datastandarder/anvendelsesprofil-organisationer> 

[[SKI Kataloget]]() https://skikataloget.ski.dk/ski-kataloget/

[[Software Development Practice]]() https://dltj.org/article/software-development-practice/

[[9]]() https://www.retsinformation.dk/eli/lta/2018/183

[[10]]() https://www.retsinformation.dk/eli/lta/2015/266

[[11]]() <http://data.europa.eu/eli/reg/2016/679/oj>:\
 <https://www.retsinformation.dk/eli/lta/2018/502>

[[12]]() <https://www.datatilsynet.dk/media/6560/dataansvarlige-og-databehandlere.pdf>

[[13]]() 'Referencearkitektur for deling af data og dokumenter' definerer datasæt som "en samling af oplysninger bestående af enkelte dele der forvaltes under et " <https://arkitektur.digst.dk/sites/default/files/20180503_rad_v1.0_-_godkendt_af_sda.pdf>. Denne definition er i tråd med W3Cs definition " samling af data, udstillet eller forvaltet af en enkelt aktør".

[[14]]() https://www.w3.org/TR/vocab-dcat/\
 (Bemærk at DCAT anvender et snævrere datasætbegreb end det der defineres i ISO 19115‑1:2014)

[[15]]() Læs mere på Rigsakivets hjemmeside: <https://www.sa.dk/da/offentlig-forvaltning/>

[[16]]() <https://www.retsinformation.dk/eli/lta/2016/1201>

[[17]]() http://data.europa.eu/eli/reg/2016/679/oj\
 https://www.retsinformation.dk/eli/lta/2018/502

[[18]]() https://www.datatilsynet.dk/media/6567/fortegnelse.pdf

[[19]]() ISO/IEC 27002:2013 Information technology -- Security techniques -- Code of practice for information security controls: https://www.iso.org/standard/54533.html

[[20]]() Sikkerhedscirkulæret https://www.retsinformation.dk/eli/retsinfo/2014/10338
