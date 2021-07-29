---
title: Behandle lagring ved å slette dokumenter eller komprimere data
description: Lær hvordan du håndterer samling av historiske dokumenter (og reduser mengden med data som er lagret i en database) ved å slette eller komprimere dem.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 06/14/2021
ms.author: edupont
ms.openlocfilehash: e29e3c0c4ce7b6cfc5ce3f38cd67781c377991ad
ms.sourcegitcommit: a486aa1760519c380b8cdc8fdf614bed306b65ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/13/2021
ms.locfileid: "6543048"
---
# <a name="manage-storage-by-deleting-documents-or-compressing-data"></a>Behandle lagring ved å slette dokumenter eller komprimere data

En sentral rolle, for eksempel programadministrator, må regelmessig håndtere oppsamlede historiske dokumenter ved å slette eller komprimere dem.  

> [!TIP]
> Hvis du vil ha informasjon om andre måter å redusere mengden data som er lagret i en database på, kan du se [Redusere data som er lagret i Business Central-databaser ](/dynamics365/business-central/dev-itpro/administration/database-reduce-data) i Hjelp for utviklere og IT-eksperter.

## <a name="delete-documents"></a>Slette dokumenter

I enkelte situasjoner kan det hende du må slette fakturerte bestillinger som ikke allerede er slettet. [!INCLUDE[prod_short](includes/prod_short.md)] kontrollerer at de slettede bestillingene er fullstendig fakturert. Du kan ikke slette bestillinger som ikke er fullstendig fakturert og mottatt.  

Ordrereturer slettes vanligvis etter at de er fakturert. Når du bokfører en faktura, overføres den til siden **Bokført kjøpskreditnota**. Hvis du merket av for **Returforsendelse i kreditnota** på **Kjøpsoppsett**-siden, overføres fakturaen til siden **Bokført returforsendelse**. Du kan slette dokumentene ved hjelp av kjørselen **Slett fakturerte best.returer**. Før du sletter, kontrollerer kjørselen om bestillingsreturer er fullstendig levert og fakturert.  

Rammebestillinger slettes ikke når du har behandlet og fakturert alle de relaterte bestillingene. Du kan slette rammebestillinger med kjørselen **Slett fakturerte rammebestillinger**.  

Fakturerte serviceordrer slettes vanligvis automatisk etter at de er fullstendig fakturert. Når en faktura bokføres, opprettes en tilhørende post på siden **Bokførte servicefakturaer**. Det bokførte dokumentet kan vises på siden **Bokført servicefaktura**.  

Serviceordrer slettes ikke automatisk hvis det totale antallet i ordren ikke er bokført fra selve serviceordren, men fra **Servicefaktura**-siden. Da må du kanskje slette fakturerte ordrer som ikke er slettet. Du kan gjøre dette ved hjelp av kjørselen **Slett fakturerte serviceordrer**.  

## <a name="compress-data-with-date-compression"></a>Komprimere data med datokomprimering

Du kan komprimere data i [!INCLUDE [prod_short](includes/prod_short.md)] slik at du sparer plass i databasen, som i [!INCLUDE [prod_short](includes/prod_short.md)] online til og med kan spare deg for penger. Komprimeringen er basert på datoer og fungerer ved å kombinere flere gamle poster til én ny post. Du kan bare komprimere poster fra avsluttede regnskapsår, og bare poster der feltet **Åpne** er satt til **Nei**.  

Leverandørposter fra tidligere regnskapsår kan for eksempel komprimeres slik at det bare er én debet- og kreditpost per konto per måned. Beløpet i den nye posten blir summen av alle de komprimerte postene. Datoen settes til startdatoen for den perioden som komprimeres, for eksempel 1. dag i måneden, hvis det komprimeres pr. måned. Etter komprimeringen kan du fremdeles se bevegelsen på hver konto i foregående regnskapsår.

Hvor mange poster det kommer ut av en datokomprimering, avhenger av hvor mange filtre du angir, hvilke felt som skal slås sammen, og hvilken periodelengde du velger. Det vil alltid være minst én post. Når kjørselen er ferdig, kan du se resultatet på siden **Datokomprim.journaler**.

Du kan komprimere følgende typer data ved hjelp av kjørsler. Det finnes en kjørsel for hver datatype.

* Finansposter – finansposter, mva-poster, bankkontoposter, finansbudsjettposter, kundeposter, leverandørposter.
* Lagerposter 
* Ressursposter
* Varebudsjettposter
* Aktiva – aktivaposter, vedlikeholdsposter for aktiva, forsikringsposter for aktiva.

Når du definerer kriterier for komprimeringen, kan du bruke alternativene under **Behold feltinnhold** til å beholde innholdet i bestemte felter. Hvilke felter som er tilgjengelige, avhenger av hvilke data du komprimerer.

> [!NOTE]
> Før du kan kjøre datokomprimering, må analysevisningene være oppdatert. Hvis du vil ha mer informasjon, kan du se [Slik oppdaterer du en analysevisning](/dynamics365/business-central/bi-how-analyze-data-dimension.md#to-update-an-analysis-view).

Etter komprimeringen beholdes alltid innholdet i følgende felt: **Bokføringsdato**, **Leverandørnr.**, **Bilagstype**, **Valutakode**, **Bokføringsgruppe**, **Beløp**, **Restbeløp**, **Opprinnelig beløp (NOK)**, **Restbeløp (NOK)**, **Beløp (NOK)**, **Kjøp (NOK)**, **Fakturarabatt (NOK)**, **Kont.rabatt gitt (NOK)** og **Mulig kont.rabatt**.

> [!NOTE]
> Komprimerte poster bokføres litt forskjellig fra standardbokføring. Dette er for å redusere antallet nye finansposter som opprettes ved hjelp av datokomprimering, og er spesielt viktig når du lagrer informasjon som dimensjoner og dokumentnumre. Datokomprimering oppretter nye oppføringer på følgende måte:
>* På siden **Finansposter** opprettes nye poster med nye postnumre for de komprimerte postene. **Beskrivelse**-feltet inneholder **Datokomprimert**, slik at de komprimerte postene er enkle å identifisere. 
>* På finanssider, for eksempel siden **Kundeposter**, opprettes det én eller flere poster med nye postnumre. 
> Bokføringsprosessen oppretter hull i nummerseriene for poster på siden **Finansposter**. Disse numrene tilordnes bare postene på finanssidene. Nummerintervallet som ble tilordnet til postene, er tilgjengelig på siden **Finansjournal** i feltene **Fra løpenr.** og **Til løpenr.** 

> [!NOTE]
> Når du har kjørt datokomprimering, låses alle kontoene i finans. Du kan for eksempel ikke oppheve utligning av leverandør- eller bankposter for noen konti i perioden der datoer er komprimert.

Hvor mange poster det kommer ut av en komprimeringskjørsel, avhenger av hvilke felt som skal slås sammen, og hvilken periodelengde du velger. Det vil alltid være minst én post. 

> [!WARNING]
> Datokomprimering sletter poster, du bør derfor alltid ta en sikkerhetskopi av databasen før du starter kjørselen.

### <a name="to-run-a-date-compression"></a>Slik kjører du en datokomprimering
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Dataadministrasjon**, og velg deretter den relaterte koblingen.
2. Gjør ett av følgende:
    1. Hvis du vil bruke en veiledning for assistert oppsett til å definere datokomprimering for en eller flere typer data, velger du **Dataadministrasjonsveiledning**.
    1. Hvis du vil konfigurere komprimering for en enkelt type data, velger du **Datokomprimering**, **Komprimer poster** og velger deretter dataene som skal komprimeres.

## <a name="see-also"></a>Se også

[Administrasjon](admin-setup-and-administration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]