---
title: Vanlige spørsmål om forslagssalgslinjer med Copilot
description: Disse vanlige spørsmålene gir informasjon om KI-teknologien som brukes i Business Central.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: article
ms.search.form: null
ms.date: 02/02/2024
ms.service: dynamics-365-business-central
ms.collection: bap-ai-copilot
ms.custom: responsible-ai-faqs
---

# <a name="faq-for-sales-line-suggestions-with-copilot-preview"></a>Vanlige spørsmål om salgslinjeforslag med Copilot (forhåndsversjon)

[!INCLUDE[preview-banner](includes/preview-banner.md)]

Disse vanlige spørsmålene beskriver virkningen av kunstig intelligens for funksjonen for salgslinjeforslag i [!INCLUDE [prod_short](includes/prod_short.md)].

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

## <a name="what-is-sales-line-suggestions-with-copilot"></a>Hva er salgslinjeforslag med Copilot?

Salgslinjeforslag med Copilot kan hjelpe deg med å opprette linjer i salgsdokumenter, for eksempel tilbud, ordrer og fakturaer, basert på strukturerte inndata eller naturlig språk. Funksjonen er ikke en generell chat, men en svært spesifikk og integrert opplevelse som du kan bruke i salgsdokumenter. Funksjonen tilbyr to forskjellige kompetanser som hjelper deg med å finne data om individuelle produkter eller de fullstendige dokumentene.

## <a name="what-are-capabilities-of-sales-line-suggestions-with-copilot"></a>Hva er mulighetene for salgslinjeforslag med Copilot?

* Finn produkter

  Informasjon som beskriver produkter, er lagret flere steder i [!INCLUDE [prod_short](includes/prod_short.md)]. Varenumre og beskrivelser er for eksempel lagret i **Vare**-tabellen, mange strekkoder er lagret i **Varereferanse**-tabellen, og produktegenskaper er lagret i **Vareattributter**-tabellen. Selv om du kanskje ber om *rød sykkel*, kan det faktiske produktet være *Crimson tourer*, der *sykkel* er en produktkategori og *rød* er et attributt.

* Finn et dokument etter referanse

  Folk gjentar ofte en tidligere ordre, eller i det minste bruker den som utgangspunkt. Men det kan være vanskelig å finne riktig ordre i en bunke med ordrer. Du husker kanskje litt av ordre-ID-en, som kan være et selskapsnummer eller et referansenummer som er mottatt fra en kunde. Du kan bruke ledetekster som *Trenger siste faktura fra april*, og dette bør hjelpe deg med å finne en bestilling raskere.

## <a name="what-is-the-intended-use-of-sales-line-suggestions-with-copilot"></a>Hva er den tiltenkte bruken av salgslinjeforslag med Copilot?

* Finn produkter

  Ment å svare på brukerspørringer om å finne produkter basert på vage, ufullstendige eller unøyaktige beskrivelser.

  Fordi gjennomsnittlig antall varer (produkter/tjenester) for [!INCLUDE [prod_short](includes/prod_short.md)]-kunder er 10 000, kan det være vanskelig å finne de rette uten tidligere erfaring eller kunnskap. Måten data lagres på i [!INCLUDE [prod_short](includes/prod_short.md)] gjør ikke ting enklere, fordi du må gjøre flere søk eller filtreringsøvelser på de forskjellige sidene som lagrer produktdata.

  Copilot trekker ut de forespurte produktene og mengdene og identifiserer de viktigste søkeordene og attributtene, slik at du kan skrive inn spørringen raskere. Deretter utfører Copilot et avansert søk gjennom flere relaterte tabeller, bruker synonymer, retter skrivefeil og evaluerer kvaliteten på søkeresultatene.

* Finn et dokument etter referanse

  Ment å svare på brukerhenvendelser for å finne eksisterende salgsdokumenter for en bestemt kunde ved hjelp av delvis eller omtrentlig informasjon.

  I B2B-miljøer håndterer folk ofte tilbakevendende forespørsler, og ordrebehandlere kan få henvendelser om å gjenta et tidligere dokument eller i det minste bruke det som utgangspunkt. Men det kan være vanskelig å finne en av flere grunner:

  - Gjennom hele livssyklusen kan et salgsdokument utvikle seg fra tilbud til ordre til bokført faktura eller levering. Dokumenter kan også arkiveres.
  - Du kan ha en nøyaktig identifikator, men kan ikke si hva den representerer. Er det for eksempel ordrenummer, fakturanummer eller ekstern referanse?
  - Noen ganger har du en dato eller en periode, men ikke en ID for dokument.

  Hvis du vil finne et kildedokument manuelt, må du åpne flere sider og bruke søk og filtrering flere ganger. Copilot kan imidlertid forenkle dette i en enkel spørring på naturlig språk som lar deg uttrykke det du leter etter på din egen måte. 

  * *Hent produkter fra bestilling 103031*
  * *Trenger produkter fra siste faktura i august*

## <a name="how-was-sales-line-suggestions-with-copilot-evaluated-what-metrics-are-used-to-measure-performance"></a>Hvordan ble salgslinjeforslag med Copilot evaluert? Hvilke målinger brukes til å måle ytelse?

Funksjonen gjennomgikk omfattende testing der mange spørringer på amerikansk engelsk representerer både typisk bruk og bruk av dårlige aktører. Testingen var basert på [!INCLUDE [prod_short](includes/prod_short.md)]s demonstrasjonsdata og en stor merket produktkatalog tilgjengelig som åpen kildekode.

Denne funksjonen er bygget i samsvar med Microsoft-standarden for ansvarlig kunstig intelligens. [Finn ut mer om ansvarlig kunstig intelligens fra Microsoft](https://aka.ms/RAI).

## <a name="what-are-the-limitations-of-sales-line-suggestions-with-copilot-how-can-users-minimize-the-impact-of-the-sales-line-suggestions-with-copilot-limitations-when-using-the-system"></a>Hva er begrensningene til salgslinjeforslag med Copilot? Hvordan kan brukere minimere virkningen av begrensningene for salgslinjeforslag med Copilot når de bruker systemet?

* Finn produkter
  
  Finn produkter fungerer best på engelsk. Selv om du kan bruke denne funksjonen på hvilket som helst av språkene som [!INCLUDE [prod_short](includes/prod_short.md)] støtter, kan varesøk på andre språk være mindre nøyaktige.

Hvis bransjen eller domenet overlapper med det Microsoft anser som sensitive emner (f.eks. narkotika, vold, underholdning for voksne osv), kan Copilot gi nøytrale, samlede svar eller gi unøyaktige svar.

Salgslinjeforslag fyller bare ut feltene **Type** som **Vare**, **Nr.** og **Antall** som beskrevet. Andre felter, inkludert **Enhet**, **Salgspris** og **Lokasjon**, bruker nåværende logikk og fylles ut enten basert på vareinnstillinger eller arvede verdier fra dokumenthodet.

**Variantkoden** støttes ikke for øyeblikket. Hvis du for eksempel kan sende et produkt i to forskjellige farger, finner Copilot det nødvendige produktet, men lar feltet **Variantkode** stå tomt. Du må fylle ut manuelt.

Hvordan du navngir produktene dine, kan påvirke resultatet. For eksempel kan bruk av kryptiske forkortelser kontra egendefinerte navn redusere resultatkvaliteten.

Når det gjelder produkter, viser tabellen nedenfor tabellene og feltene som Copilot søker i.

|Bord  |Felter  |
|---------|---------|
|**Varer**     |  * Nr.<br>* Beskrivelse<br>* Beskrivelse 2<br>* Søkbeskrivelse<br>* GTIN<br>* Leverandørvarenummer       |
|**Varevariant**     | * Kode<br>* Beskrivelse<br>* Beskrivelse 2          |
|**Varereferanse**     | * Referansenr.<br>* Beskrivelse<br>* Beskrivelse 2        |
|**Vareattributter**     | * Navn<br>* Verdi        |
|**Varekategori**     |  * Kode<br>* Beskrivelse<br>* Overordnet kategori – 1 nivå           |
|**Vareoversettelse**     | * Språk<br>* Beskrivelse<br>* Beskrivelse 2          |
|**Vare-ID**     |  * Kode       |
|**Utvidet tekstlinje**     |  * Tekst      |

* Finn dokumenter etter referanse

  For øyeblikket kan du starte salgslinjeforslag fra ordrer, fakturaer og tilbud og søke i følgende dokumenter:

  * Ordrer
  * Tilbud
  * Salgsfakturaer
  * Bokførte salgsfakturaer
  * Bokførte følgesedler

  Copilot søker i følgende felter

  * Dokumentnr.
  * Eksternt dokumentnr.
  * Deres referanse
  * Forespørselsnr.
  * Dokumentdato
  * Salg til-kundenr.

  Copilot returnerer ikke alle linjer av typen Vare. Bare varenumre, variantkoder og antall overføres. Antall fra kildedokumentet konverteres til **salgsenheten**.

## <a name="in-which-geographies-and-languages-is-sales-lines-suggestions-available"></a>I hvilke geografiske områder og på hvilke språk er salgslinjeforslag tilgjengelig?

Med unntak av Canada er denne funksjonen tilgjengelig for alle lokaliseringer for land-/områdemiljøer og på alle språk som støttes. På grunn av begrenset språkstøtte er ikke funksjonen i utgangspunktet tilgjengelig for kanadiske kunder fordi den ikke oppfyller regelverket for språkoverholdelse. Hvis denne funksjonen skal være tilgjengelig for kundemiljøer i land/områder der Azure OpenAI-tjenesten ikke er tatt i bruk, må administratorer først samtykke til å tillate flytting av dataene over grenser for at [!INCLUDE [prod_short](includes/prod_short.md)] skal koble til Azure OpenAI-tjenesten.  

## <a name="what-operational-factors-and-settings-allow-for-effective-and-responsible-use-of-the-feature"></a>Hvilke driftsfaktorer og innstillinger gjør at det går an å bruke funksjonen på en effektiv og ansvarlig måte?

KI-drevne forslag kan noen ganger være feil eller ufullstendige. Du bør alltid vurdere nøyaktigheten av Copilots forslag før du velger om du vil beholde dem. Copilots forslag lagres ikke i [!INCLUDE [prod_short](includes/prod_short.md)]-databasen før du velger **Behold det**-knappen og avslutter Copilot-vinduet. Du kan redigere og korrigere eventuelle forslag før du velger å beholde dem, eller etter at de er satt inn i et salgsdokument.

### <a name="what-is-expected-of-administrators-and-end-users-when-using-sales-lines-suggestions"></a>Hva forventes av administratorer og sluttbrukere når de bruker salgslinjeforslag?

Hver enkelt bruker velger om de vil bruke **salgslinjeforslag** eller ikke. Selv når funksjonen er aktivert av administratorer og tilgjengelig, kan du fortsatt velge å bruke den alltid, noen ganger eller aldri.  

Det er administratorene som avgjør om Copilot-funksjoner i [!INCLUDE [prod_short](includes/prod_short.md)] skal brukes. Hvis administratorer aktiverer Copilot, bør de sørge for at de gir tilgang til de riktige brukerne.   

> [OBS!]
> - Vi støtter ikke denne funksjonen i [!INCLUDE [prod_short](includes/prod_short.md)] lokalt eller i privat sky.
> - Partnere kan ikke utvide denne funksjonen. Dette betyr at partnerutviklere ikke kan endre, erstatte eller utvide den.

## <a name="is-copilot-the-only-means-to-create-sales-lines"></a>Er Copilot den eneste måten å opprette salgslinjer på?

Nei, bruk av Copilot er valgfritt. [!INCLUDE [prod_short](includes/prod_short.md)] tilbyr ikke-KI-drevne måter å sette inn salgslinjer eller kopiere dokumenter på. Organisasjoner kan bruke begge tilnærmingene samtidig.  

## <a name="how-do-i-give-feedback-about-ai-generated-content"></a>Hvordan gir jeg tilbakemelding om KI-generert innhold?

Hver gang Copilot gir forslag, kan du gi tilbakemelding til Microsoft direkte fra Copilot-vinduet, ved hjelp av Liker- og Liker ikke-kontrollene. Din tilbakemelding er anonym, og vi bruker disse dataene til å forbedre kvaliteten på tjenesten.  

## <a name="see-also"></a>Se også

[Foreslå linjer i ordrer med Copilot](sales-suggest-sales-lines-with-copilot.md)  
[Konfigurer Copilot- og KI-funksjoner](enable-ai.md)  
[Vanlige spørsmål om ansvarlig kunstig intelligens for Dynamics 365 Business Central](responsible-ai-overview.md)  
