---
title: Behandle lagring ved å slette dokumenter eller komprimere data
description: Lær hvordan du håndterer samling av historiske dokumenter (og reduser mengden med data som er lagret i en database) ved å slette eller komprimere dem.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.form: '107, 9035, 9040'
ms.date: 04/16/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Behandle lagring ved å slette dokumenter eller komprimere data

En sentral rolle, for eksempel programadministrator, må regelmessig håndtere oppsamlede historiske dokumenter ved å slette eller komprimere dem.  

> [!TIP]
> Hvis du vil ha informasjon om andre måter å redusere mengden data som er lagret i en database på, kan du se [Redusere data som er lagret i Business Central-databaser ](/dynamics365/business-central/dev-itpro/administration/database-reduce-data) i dokumentasjonen for utviklere og IT-eksperter.

## Slette dokumenter

I enkelte situasjoner kan det hende du må slette fakturerte bestillinger. Du kan imidlertid ikke slette dem med mindre du har fullstendig fakturert og mottatt varene i bestillingene. [!INCLUDE[prod_short](includes/prod_short.md)] hjelper deg med å se etter det.

Virksomheter sletter vanligvis returordrer etter at de er fakturert. Når du bokfører en faktura, overfører [!INCLUDE [prod_short](includes/prod_short.md)] den til siden **Bokført kjøpskreditnota**. Hvis du merket av for **Returforsendelse i kreditnota** på **Kjøpsoppsett**-siden, overføres fakturaen til siden **Bokført returforsendelse**. Du kan slette dokumentene ved hjelp av kjørselen **Slett fakturerte best.returer**. Før den sletter dokumenter, kontrollerer satsjobben om bestillingsreturer er fullstendig levert og fakturert.  

Rammebestillinger slettes ikke automatisk når du har behandlet og fakturert alle de relaterte bestillingene. I stedet kan du slette dem med kjørselen **Slett fakturerte rammebestillinger**.  

Virksomheter sletter vanligvis fakturerte serviceordrer automatisk etter at de er fullstendig fakturert. Når en faktura bokføres, opprettes en tilhørende post som vises på siden **Bokførte servicefakturaer**.  

Serviceordrer slettes imidlertid ikke automatisk hvis det totale antallet i ordren ikke ble bokført fra siden **Servicefaktura** i stedet for fra selve serviceordren. Du må kanskje slette slike fakturerte ordrer manuelt ved å utføre satsjobben **Slett fakturerte serviceordrer**.  

## Komprimere data med datokomprimering

Du kan komprimere data i [!INCLUDE [prod_short](includes/prod_short.md)] for å spare plass i databasen, som i [!INCLUDE [prod_short](includes/prod_short.md)] online til og med kan spare deg for penger. Komprimeringen, som er basert på datoer og funksjoner, fungerer ved å kombinere flere gamle poster til én ny post.

Du kan komprimere oppføringer som samsvarer med følgende betingelser:

* De er fra avsluttede regnskapsår.
* **Åpen**-feltet settes til **Nei**.
* De er minst fem år gamle. Hvis du vil komprimere data som er mindre enn fem år gamle, kontakter du Microsoft-partneren din.

Leverandørposter fra tidligere regnskapsår kan for eksempel komprimeres slik at det bare er én debet- og kreditpost per konto per måned. Beløpet i den nye posten blir summen av alle de komprimerte postene. Datoen som tildeles, er startdatoen for den komprimerte perioden, for eksempel første dagen i måneden (hvis du komprimerer postene per måned). Etter komprimeringen kan du fremdeles se bevegelsen på hver konto i foregående regnskapsår.

Hvor mange poster det kommer ut av en datokomprimering, avhenger av hvor mange filtre du angir, hvilke felt som skal slås sammen, og hvilken periodelengde du velger. Det finnes alltid minst én post. Når kjørselen er ferdig, kan du se resultatet på siden **Datokomprim.journaler**.

Du kan komprimere følgende typer data ved hjelp av kjørsler.

* Finansposter – finansposter, mva-poster, bankkontoposter, finansbudsjettposter, kundeposter og leverandørposter.
* Lagerposter
* Ressursposter
* Varebudsjettposter
* Aktivaposter, vedlikeholdsposter for aktiva og forsikringsposter for aktiva.

Når du definerer kriterier for komprimeringen, kan du bruke beholde innholdet av bestemte felt med alternativene under **Behold feltinnhold**. Hvilke felter som er tilgjengelige, avhenger av hvilke data du komprimerer.

> [!NOTE]
> Før du kan kjøre datokomprimering, må analysevisningene være oppdatert. Hvis du vil ha mer informasjon, kan du se delen [Oppdatere en analysevisning](bi-how-analyze-data-dimension.md#update-an-analysis-view).

Etter komprimeringen beholdes alltid innholdet i følgende felt: **Bokføringsdato**, **Leverandørnr.**, **Bilagstype**, **Valutakode**, **Bokføringsgruppe**, **Beløp**, **Restbeløp**, **Opprinnelig beløp (LV)**, **Restbeløp (LV)**, **Beløp (LV)**, **Kjøp (LV)**, **Fakturarabatt (LV)**, **Kont.rabatt gitt (LV)** og **Mulig kont.rabatt**.

## Bokføre komprimerte poster

Komprimerte poster bokføres litt forskjellig fra standardbokføring. Denne forskjellen er for å redusere antallet nye finansposter som opprettes ved hjelp av datokomprimering, og er spesielt viktig når du lagrer informasjon som dimensjoner og dokumentnumre. Datokomprimering oppretter nye oppføringer på følgende måte:

* På siden **Finansposter** opprettes nye poster for de komprimerte postene. **Beskrivelse**-feltet inneholder **Datokomprimert**, slik at de komprimerte postene er enkle å identifisere. 
* På finanssider, for eksempel siden **Kundeposter**, opprettes det én eller flere nye poster. 

Bokføringsprosessen oppretter hull i nummerseriene for poster på siden **Finansposter**. Disse numrene tilordnes bare postene på finanssidene. Nummerintervallet som ble tilordnet til postene, er tilgjengelig på siden **Finansjournal** i feltene **Fra løpenr.** og **Til løpenr.** 

> [!NOTE]
> Når du har kjørt datokomprimering, kan du ikke tilbakeføre leverandør- eller bankposter for transaksjoner som påvirkes av komprimeringen.

Hvor mange poster det kommer ut av en datokomprimering, avhenger av hvor mange filtre du angir, hvilke felt som skal slås sammen, og hvilken periodelengde du velger. Det finnes alltid minst én post.

> [!WARNING]
> Datokomprimering sletter poster, du bør derfor alltid ta en sikkerhetskopi av databasen før du starter kjørselen.

### Slik kjører du en datokomprimering

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Dataadministrasjon**, og velg deretter den relaterte koblingen.
2. Gjør et av følgende, avhengig av behovene:
    * Hvis du vil bruke en assistert veiledning for å sette opp datokomprimering for en eller flere typer data, velger du **Dataadministrasjonsveiledning**.
    * Hvis du vil konfigurere komprimering for en enkelt type data, velger du **Datokomprimering**, **Komprimer poster** og velger deretter dataene som skal komprimeres.

   > [!NOTE]
   > Du kan bare komprimere data som er mer enn fem år gamle. Hvis du vil komprimere data som er mindre enn fem år gamle, kontakter du Microsoft-partneren din. De må bruke `OnSetMinimumNumberOfYearsToKeep`-hendelsen i Datokomprimering-codeunit til å angi terskelen.


## Se også

[Administrasjon](admin-setup-and-administration.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
