---
title: Behandle lagring ved å slette dokumenter eller komprimere data
description: Lær hvordan du håndterer samling av historiske dokumenter (og reduser mengden med data som er lagret i en database) ved å slette eller komprimere dem.
author: brentholtorf
ms.topic: conceptual
ms.search.form: '107, 9035, 9040'
ms.date: 09/14/2022
ms.author: bholtorf
---
# <a name="manage-storage-by-deleting-documents-or-compressing-data"></a>Behandle lagring ved å slette dokumenter eller komprimere data

En sentral rolle, for eksempel programadministrator, må regelmessig håndtere oppsamlede historiske dokumenter ved å slette eller komprimere dem.  

> [!TIP]
> Hvis du vil ha informasjon om andre måter å redusere mengden data som er lagret i en database på, kan du se [Redusere data som er lagret i Business Central-databaser ](/dynamics365/business-central/dev-itpro/administration/database-reduce-data) i dokumentasjonen for utviklere og IT-eksperter.

## <a name="delete-documents"></a>Slette dokumenter

I enkelte situasjoner kan det hende du må slette fakturerte bestillinger. Du kan imidlertid ikke slette dem med mindre du har fullstendig fakturert og mottatt varene i bestillingene. [!INCLUDE[prod_short](includes/prod_short.md)] hjelper deg med å se etter det.

Ordrereturer slettes vanligvis etter at de er fakturert. Når du bokfører en faktura, overføres den til siden **Bokført kjøpskreditnota**. Hvis du merket av for **Returforsendelse i kreditnota** på **Kjøpsoppsett**-siden, overføres fakturaen til siden **Bokført returforsendelse**. Du kan slette dokumentene ved hjelp av kjørselen **Slett fakturerte best.returer**. Før du sletter, kontrollerer kjørselen om bestillingsreturer er fullstendig levert og fakturert.  

Rammebestillinger slettes ikke automatisk når du har behandlet og fakturert alle de relaterte bestillingene. I stedet kan du slette dem med kjørselen **Slett fakturerte rammebestillinger**.  

Fakturerte serviceordrer slettes vanligvis automatisk etter at de er fullstendig fakturert. Når en faktura bokføres, opprettes en tilhørende post som vises på siden **Bokførte servicefakturaer**.  

Serviceordrer slettes imidlertid ikke automatisk hvis det totale antallet i ordren ikke er bokført fra siden **Servicefaktura** i stedet for fra selve serviceordren. Du må kanskje slette slike fakturerte ordrer manuelt ved å utføre kjørselen **Slett fakturerte serviceordrer**.  

## <a name="compress-data-with-date-compression"></a>Komprimere data med datokomprimering

Du kan komprimere data i [!INCLUDE [prod_short](includes/prod_short.md)] for å spare plass i databasen, som i [!INCLUDE [prod_short](includes/prod_short.md)] online til og med kan spare deg for penger. Komprimeringen, som er basert på datoer og funksjoner, fungerer ved å kombinere flere gamle poster til én ny post.

Du kan komprimere oppføringer som samsvarer med følgende betingelser:

* De er fra avsluttede regnskapsår.
* **Åpen**-feltet settes til **Nei**.
* De er minst fem år gamle. Hvis du vil komprimere data som er mindre enn fem år gamle, kontakter du Microsoft-partneren din.

Leverandørposter fra tidligere regnskapsår kan for eksempel komprimeres slik at det bare er én debet- og kreditpost per konto per måned. Beløpet i den nye posten blir summen av alle de komprimerte postene. Datoen som tilordnes, er startdatoen for den komprimerte perioden, for eksempel første dagen i måneden (hvis postene komprimeres per måned). Etter komprimeringen kan du fremdeles se bevegelsen på hver konto i foregående regnskapsår.

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

## <a name="posting-compressed-entries"></a>Bokføre komprimerte poster

Komprimerte poster bokføres litt forskjellig fra standardbokføring. Dette er for å redusere antallet nye finansposter som opprettes ved hjelp av datokomprimering, og er spesielt viktig når du lagrer informasjon som dimensjoner og dokumentnumre. Datokomprimering oppretter nye oppføringer på følgende måte:

* På siden **Finansposter** opprettes nye poster for de komprimerte postene. **Beskrivelse**-feltet inneholder **Datokomprimert**, slik at de komprimerte postene er enkle å identifisere. 
* På finanssider, for eksempel siden **Kundeposter**, opprettes det én eller flere nye poster. 

Bokføringsprosessen oppretter hull i nummerseriene for poster på siden **Finansposter**. Disse numrene tilordnes bare postene på finanssidene. Nummerintervallet som ble tilordnet til postene, er tilgjengelig på siden **Finansjournal** i feltene **Fra løpenr.** og **Til løpenr.** 

> [!NOTE]
> Når du har kjørt datokomprimering, låses alle kontoene i finans. Det betyr at du ikke kan for eksempel oppheve utligning av leverandør- eller bankposter for konti som påvirkes av komprimeringen.

Hvor mange poster det kommer ut av en datokomprimering, avhenger av hvor mange filtre du angir, hvilke felt som skal slås sammen, og hvilken periodelengde du velger. Det vil alltid være minst én post.

> [!WARNING]
> Datokomprimering sletter poster, du bør derfor alltid ta en sikkerhetskopi av databasen før du starter kjørselen.

### <a name="to-run-a-date-compression"></a>Slik kjører du en datokomprimering

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Dataadministrasjon**, og velg deretter den relaterte koblingen.
2. Gjør ett av følgende:
    * Hvis du vil bruke en assistert veiledning for å sette opp datokomprimering for en eller flere typer data, velger du **Dataadministrasjonsveiledning**.
    * Hvis du vil konfigurere komprimering for en enkelt type data, velger du **Datokomprimering**, **Komprimer poster** og velger deretter dataene som skal komprimeres.

   > [!NOTE]
   > Du kan bare komprimere data som er mer enn fem år gamle. Hvis du vil komprimere data som er mindre enn fem år gamle, kontakter du Microsoft-partneren din.

## <a name="see-also"></a>Se også

[Administrasjon](admin-setup-and-administration.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
