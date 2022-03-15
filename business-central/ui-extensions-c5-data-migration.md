---
title: Bruke C5-utvidelse for dataoverføring | Microsoft-dokumentasjon
description: Bruk denne utvidelsen til å overføre kunder, leverandører, varer og finanskonti fra Microsoft Dynamics C5 2012 til Business Central.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, C5, import
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 6f8c90eeb5b99f5591db7847e9d48124c910e328
ms.sourcegitcommit: 5a02f8527faecdffcc54f9c5c70cefe8c4b3b3f4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/04/2022
ms.locfileid: "8381117"
---
# <a name="the-c5-data-migration-extension"></a>Utvidelsen C5-datamigrering

Denne utvidelsen gjør det enkelt å overføre kunder, leverandører, varer og konti fra Microsoft Dynamics C5 2012 til [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan også overføre historiske poster for finanskonti.

> [!Note]
> Selskapet i [!INCLUDE[prod_short](includes/prod_short.md)]kan ikke inneholde data. I tillegg, når du starter en migrering, bør du ikke opprette kunder, leverandører, varer eller kontoer til migreringen er ferdig.

## <a name="what-data-is-migrated"></a>Hvilke data overføres?
Følgende data overføres for hver enhet:

### <a name="customers"></a>Kunder

* Kontakter  
* Lokasjon
* Land
* Dimensjoner for kunde (avdeling, senter, formål)
* Leveringsmåte
* Selger
* Betalingsbetingelser
* Betalingsmåte
* Kundeprisgruppe
* Kundefakturarabatt

Hvis du overfører konti, overføres også følgende data:

* Bokføringsgruppe – kunde
* Finanskladd
* Åpne transaksjoner (kundeposter)

### <a name="vendors"></a>Leverandører

* Kontakter
* Lokasjon
* Land
* Dimensjoner for leverandør (avdeling, senter, formål)
* Fakturarabatt
* Leveringsmåte
* Innkjøper
* Betalingsbetingelser
* Betalingsmåte
* Leverandørfakturarabatt

Hvis du overfører konti, overføres også følgende data:

* Bokføringsgruppe – leverandør
* Finanskladd
* Åpne transaksjoner (leverandørposter)

### <a name="items"></a>Varer

* Lokasjon
* Land
* Dimensjoner for vare (avdeling, senter, formål)
* Salgslinjerabatter
* Kunderabattgrupper
* Varerabattgrupper
* Salgspris
* Tariffnummer
* Enheter
* Varesporingskode
* Kundeprisgruppe
* Monteringsstykklister

Hvis du overfører konti, overføres også følgende data:

* Lagerbokføringsoppsett
* Generelt bokføringsoppsett
* Varekladd
* Åpne transaksjoner (vareposter)

> [!Note]
> Hvis det finnes åpne transaksjoner som bruker utenlandske valutaer, overføres også valutakursene for de aktuelle valutaene. Andre valutakurser overføres ikke.

### <a name="chart-of-accounts"></a>Kontoplan

* Standarddimensjoner: Avdeling, kostsenter, formål  
* Historiske finanstransaksjoner  

> [!Note]
> Historiske finanstransaksjoner behandles på en litt annen måte. Når du overfører data, angir du parameteren **Inneværende periode**. Denne parameteren angir hvordan finanstransaksjoner behandles. Transaksjoner etter denne datoen overføres individuelt. Transaksjoner før denne datoen samles per konto og overføres som et enkelt beløp. La oss for eksempel si at det finnes transaksjoner i 2015, 2016, 2017, 2018, og du angir 1. januar 2017 i feltet Innværende periode. For hver konto samles beløpene for transaksjonene på eller før 31. desember 2106 i én finanskladdlinje for hver finanskonto. Alle transaksjoner etter denne datoen overføres individuelt.

## <a name="file-size-requirements"></a>Filstørrelseskrav

Den største størrelsen du kan laste opp til [!INCLUDE[prod_short](includes/prod_short.md)], er 150 MB. Hvis filen du eksporterer fra C5, er større enn det, vurder å overføre dataene i flere filer. For eksempel kan du eksportere én eller to typer enheter fra C5, for eksempel kunder og leverandører, til en fil, og deretter eksportere varer til en annen fil, og så videre. Du kan importere filer individuelt i [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="to-migrate-data"></a>Migrere data

Det tar kun noen få trinn å eksportere data fra C5 og importere dataen inn i [!INCLUDE[prod_short](includes/prod_short.md)]:  

1. I C5 bruker du **Eksportere databasen**-funksjonen for å eksportere dataene. Deretter sender du eksportmappen til en komprimert (pakket) mappe.  
2. I [!INCLUDE[prod_short](includes/prod_short.md)] velger du ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Dataoverføring**, og deretter velger du **Dataoverføring**.  
3. Fullfør trinnene i den assisterte oppsettsveiledningen. Pass på at du velger **Importer fra Microsoft Dynamcis C5 2012** som datakilde.  

## <a name="viewing-the-status-of-the-migration"></a>Se statusen for migreringen

Bruk siden **Oversikt over datamigrering** for å overvåke migreringen. Siden viser informasjon om hvor mange enheter som er inkludert i migreringen, status til migreringen, antall varer som er migrert, og om migreringen var vellykket. Den viser også antall feil, gir deg mulighet til å undersøke hva som gikk feil, og gjør det enkelt å gå til enheten for å løse problemene. Hvis du vil ha mer informasjon, kan du se neste avsnitt i dette emnet.  

> [!Note]
> Mens du venter på resultatet av overføringen, må du oppdatere siden for å vise resultatet.

## <a name="how-to-avoid-double-posting"></a>Slik unngår du dobbel bokføring

For å unngå dobbel bokføring i Finans brukes følgende balansekonti for åpne transaksjoner:  

* Vi bruker leverandørgjeldskonto for leverandører fra leverandørbokføringsgruppen.  
* Vi bruker kundefordringskonto for kunder fra kundebokføringsgruppen.  
* For varer oppretter vi et generelt bokføringsoppsett, der justeringskontoen er kontoen som er angitt som lagerkonto i lagerbokføringsoppsettet.  

## <a name="correcting-errors"></a>Feilkorrigering

Hvis det oppstår en feil, viser **Status**-feltet **Fullført med feil**, og **Feilantall** viser hvor mange feil som oppsto. For å se en oversikt over feilene, kan du åpne siden **Datamigreringsfeil** ved å velge:  

* Tallet i feltet **Feilantall** for enheten.  
* Enheten og velg deretter handlingen **Vis feil**.  

For å korrigere en feil kan du velge en feilmelding på siden **Datamigreringsfeil** og deretter velge **Rediger post** for å vise de migrerte dataene for enheten. Hvis du har flere feil som må løses, kan du velge **Massereparasjon av feil** for å redigere enhetene i en liste. Du må fortsatt åpne enkeltposter hvis årsaken til feilen blr forårsaket av en relatert post. For eksempel overføres en leverandør ikke hvis en e-postadresse til en av kontaktene har ugyldig format.

Etter at du har korrigert én eller flere feil, kan du velge **Migrer** for å migrere enheten du har korrigert, uten å starte hele migrerringen på nytt.  

> [!Tip]
> Hvis du har korrigert én eller flere feil, kan du bruke funksjonen **Velg mer** for å velge flere linjer til som skal migreres. Hvis det finnes feil som ikke er viktige å korrigere, kan du velge dem og så velge **Hopp over valg**.

> [!Note]
> Hvis du har varer som er inkludert i en stykkliste, må du kanskje migrere mer enn én gang hvis den opprinnelige varen ikke er opprettet før variantene som refererer til den. Hvis en varevariant opprettes først, kan referansen til den opprinnelige varen føre til en feilmelding.  

## <a name="verifying-data-after-migrating"></a>Kontrollere dataene etter migrering

Du kan kontrollere at dataene er overført riktig ved å se på følgende sider i C5 og [!INCLUDE[prod_short](includes/prod_short.md)].

|Microsoft Dynamics C5 2012 | Dynamics 365 Business Central| Kjørsel som skal brukes |
|---------------------------|------------------------------|------------------|
|Kundeposter| Finanskladder| CUSTMIGR |
|Leverandørposter| Finanskladder| VENDMIGR|
|Vareposter| Varekladder| ITEMMIGR |
|Finansposter| Finanskladder| GLACMIGR |

## <a name="stopping-data-migration"></a>Stoppe datamigrering

Du kan stoppe datamigreringen ved å velge **Stopp alle migreringer**. Hvis du gjør dette, blir alle ventende migreringer også stoppet.

## <a name="see-also"></a>Se også

[Tilpasse [!INCLUDE[prod_short](includes/prod_short.md)] ved hjelp av utvidelser](ui-extensions.md)  
[Bli klar til å gjøre forretninger](ui-get-ready-business.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]