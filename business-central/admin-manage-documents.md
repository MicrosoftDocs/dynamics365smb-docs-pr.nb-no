---
title: Behandle lagring ved å slette dokumenter eller komprimere data
description: Lær hvordan du kan beholde de historiske dataene dine ved å komprimere poster eller slette dem.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: b17e4df039ef713bf5c0048d258aefd175157ba4
ms.sourcegitcommit: a9d48272ce61e5d512a30417412b5363e56abf30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/04/2021
ms.locfileid: "5493050"
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

Du kan komprimere data i [!INCLUDE [prod_short](includes/prod_short.md)] slik at du sparer plass i databasen, som i [!INCLUDE [prod_short](includes/prod_short.md)] online til og med kan spare deg for penger. Komprimeringen er basert på datoer og fungerer ved å kombinere flere gamle poster til én ny post. Du kan bare komprimere poster fra avsluttede regnskapsår, og bare leverandørposter der feltet **Åpne** er satt til *Nei*.  

Leverandørposter fra tidligere regnskapsår kan for eksempel komprimeres slik at det bare er én debet- og kreditpost per konto per måned. Beløpet i den nye posten blir summen av alle de komprimerte postene. Datoen settes til startdatoen for den perioden som komprimeres, for eksempel 1. dag i måneden, hvis det komprimeres pr. måned. Etter komprimeringen kan du fremdeles se bevegelsen på hver konto i foregående regnskapsår.

Hvor mange poster det kommer ut av en datokomprimering, avhenger av hvor mange filtre du angir, hvilke felt som skal slås sammen, og hvilken periodelengde du velger. Det vil alltid være minst én post. Når kjørselen er ferdig, kan du se resultatet på siden **Datokomprim.journaler**.

Du kan komprimere følgende typer data i [!INCLUDE [prod_short](includes/prod_short.md)] ved hjelp av kjørsler:

* Bankkontoposter

  Etter komprimeringen kan du ved hjelp av funksjonen **Beholde feltinnhold** også velge å beholde innholdet i feltene **Bilagsnr., Vår kontakt**, **Kode for global dimensjon 1** og **Kode for global dimensjon 2**.
* Leverandørposter

> [!NOTE]
> Komprimerte poster for kunder, leverandører, bank og FA-underposter bokføres på en litt annen måte enn standard bokføring. Dette er for å redusere antallet nye finansposter som opprettes ved hjelp av datokomprimering, og er spesielt viktig når du lagrer informasjon som dimensjoner og dokumentnumre. Datokomprimering oppretter nye oppføringer på følgende måte:
>* På siden **Finansposter** opprettes nye poster med nye postnumre for de komprimerte postene. **Beskrivelse**-feltet inneholder **Datokomprimert**, slik at de komprimerte postene er enkle å identifisere. 
>* På finanssider, for eksempel siden **Kundeposter**, opprettes det én eller flere poster med nye postnumre. 
> Bokføringsprosessen oppretter hull i nummerseriene for poster på siden **Finansposter**. Disse numrene tilordnes bare postene på finanssidene. Nummerintervallet som ble tilordnet til postene, er tilgjengelig på siden **Finansjournal** i feltene **Fra løpenr.** og **Til løpenr.** 

Etter komprimeringen beholdes alltid innholdet i følgende felt: **Bokføringsdato**, **Leverandørnr.**, **Bilagstype**, **Valutakode**, **Bokføringsgruppe**, **Beløp**, **Restbeløp**, **Opprinnelig beløp (NOK)**, **Restbeløp (NOK)**, **Beløp (NOK)**, **Kjøp (NOK)**, **Fakturarabatt (NOK)**, **Kont.rabatt gitt (NOK)** og **Mulig kont.rabatt**.

  Ved hjelp av funksjonen **Behold feltinnhold** kan du også beholde innholdet i følgende felt: **Bilagsnr.**, **Kjøp fra-leverandørnr.**, **Innkjøperkode**, **Kode for global dimensjon 1** og **Kode for global dimensjon 2**.

> [!NOTE]
> Når du har kjørt datokomprimering, låses alle kontoene i finans. Du kan for eksempel ikke oppheve utligning av leverandør- eller bankposter for noen konti i perioden der datoer er komprimert.

<!--* General ledger entries
* Customer ledger entries-->
<!--* Fixed asset ledger entries
* G/L budget entries
* VAT entries

  After the compression the contents of the following fields are always retained: **Posting Date**, **Type**, **Closed**, **Gen. Bus. Posting Group**, **Gen. Prod. Posting Group**, **VAT Calculation Type**, **Base**, and **Amount**.

  With the **Retain Field Contents** facility, you can also retain the contents of the following additional fields: **Document No.**, **Bill-to/Pay-to No.**, **EU 3-Party Trade**, **Country/Region Code**, and **Internal Ref. No.**.
* Insurance ledger entries
* Maintenance ledger entries
* Resource ledger entries

  After the compression, the contents of the following fields are retained: **Posting Date**, **Resource No.**, **Resource Group No.**, **Entry Type**, **Quantity**, **Total Cost**, **Total Price**, and **Chargeable**.

  With the **Retain Field Contents** facility, you can also retain the contents of the following additional fields: **Document No.**, **Work Type Code**, **Job No.**, **Unit of Measure Code**, **Source Type**, **Source No.**. **Chargeable**, **
* Warehouse entries

  After the compression the contents of the following fields are always retained: **Registering Date**, **Location Code**, **Zone Code**, **Bin Code**, **Item No.**, **Quantity**, **Qty. (Base)**, **Bin Type Code**, **Entry Type**, **Variant Code**, **Qty. per Unit of Measure**, **Unit of Measure Code**, **Warranty Date**, **Expiration Date**, **Cubage**, and **Weight**.

  With the **Retain Field Contents** facility, you can also retain the contents of the **Serial No.** and **Lot No.** fields. -->

Hvor mange poster det kommer ut av en komprimeringskjørsel, avhenger av hvilke felt som skal slås sammen, og hvilken periodelengde du velger. Det vil alltid være minst én post. 

> [!WARNING]
> Datokomprimering sletter poster, du bør derfor alltid ta en sikkerhetskopi av databasen før du starter kjørselen.

Tabellen nedenfor inneholder en oversikt over feltene i hurtigfanen **Alternativer** som er tilgjengelige i alle kjørsler. Delen **Behold feltinnhold** inkluderer flere felt som er beskrevet ovenfor.

|Felt  |Beskrivelse  |
|-------|-------------|
|Startdato     |Angi den første datoen som skal være med i datokomprimeringen. Komprimeringen vil påvirke alle postene fra denne datoen og frem til sluttdatoen.|
|Sluttdato     |Angi den siste datoen som skal være med i datokomprimeringen. Komprimeringen vil påvirke alle postene fra startdatoen og frem til denne datoen.|
|Periodelengde |Velg lengden på perioden som postene skal komprimeres i. Velg feltet for å vise alternativene. Hvis du valgte *Kvartal*, *Måned* eller *Uke*, komprimeres bare poster som befinner seg i samme regnskapsperiode.|
|Behold feltinnhold     |Sett haker i avmerkingsboksene hvis du vil beholde innholdet i feltene selv om postene komprimeres. Jo flere felt du velger, jo mer detaljert vil de komprimerte postene være. Hvis du ikke velger noen felt, lager kjørselen én post per dag, uke eller annen periode, alt etter tidsinndelingen i feltet **Periodelengde**. |

## <a name="see-also"></a>Se også

[Administrasjon](admin-setup-and-administration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]