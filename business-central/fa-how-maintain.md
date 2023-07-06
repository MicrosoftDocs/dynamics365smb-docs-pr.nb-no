---
title: Vedlikehold aktiva
description: Du holder en vedlikeholdsoversikt over reparasjonene og servicen på et aktivum for å beholde verdien for dette aktivumet.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'repair, service'
ms.search.form: '5642, 5625'
ms.date: 06/15/2021
ms.author: edupont
---
# <a name="maintain-fixed-assets"></a><a name="maintain-fixed-assets"></a><a name="maintain-fixed-assets"></a>Vedlikehold aktiva

Vedlikeholdsutgifter er periodiske kostnader som er pådratt for å opprettholde aktivaverdien. I motsetning til kapitaløkninger bidrar de ikke til noen verdiøkning.

Du kan registrere og vedlikeholde en oppdateringsfil for vedlikehold av og service på aktivaet, slik at du har fullstendige vedlikeholdsposter for et aktiva lett tilgjengelig. Hver gang et aktiva sendes på service, registrerer du alle aktuelle opplysninger, for eksempel servicedato, leverandørnummer og serviceagentens telefonnummer. Det registreres vedlikehold for hvert enkelt aktiva på det aktuelle aktivakortet.

Indeksregulering brukes til å justere verdier for generelle endringer i prisnivået. Du bruker kjørselen **Indeksreg. aktiva** til å beregne vedlikeholdskostnadene på nytt.

## <a name="to-record-maintenance-work-on-a-fixed-asset"></a><a name="to-record-maintenance-work-on-a-fixed-asset"></a><a name="to-record-maintenance-work-on-a-fixed-asset"></a>Slik registrerer du vedlikeholdsarbeid på et anleggsmiddel:

Hver gang det er utført service for et aktiva, for eksempel et servicebesøk, kan du registrere dette på siden **Vedlikeholdsregistrering**.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Aktiva**, og velg deretter den relaterte koblingen.  
2. Velg aktivaet du vil registrere vedlikehold for, og velg deretter **Vedlikeholdsregistrering**.
3. På siden **Vedlikeholdsregistrering** fyller du ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-post-maintenance-costs-from-a-fixed-asset-gl-journal"></a><a name="to-post-maintenance-costs-from-a-fixed-asset-gl-journal"></a><a name="to-post-maintenance-costs-from-a-fixed-asset-gl-journal"></a>Slik bokfører du vedlikeholdskostnader fra en aktivafinanskladd:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Avskrivningstablå – oversikt**, og velg deretter den relaterte koblingen.  
2. Velg avskrivningstablået som er tilordnet til aktivaet, og velg deretter **Rediger**-handlingen.
3. På **Avskrivningstablåkort**-siden må du kontrollere at det ikke er merket av for **Vedlikehold**. Dette sikrer at vedlikeholdskostnader ikke bokføres til finans.
4. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Aktivafinanskladder**, og velg deretter den relaterte koblingen.  
5. Opprett en innledende kladdelinje, og fyll ut feltene etter behov.
6. I feltet **Aktivabokf.type** velger du **Vedlikehold**.
7. Velg **Sett inn aktivamotkonto**. En ny kladdelinje opprettes for motkontoen som er satt opp for vedlikeholdsbokføring.

    > [!NOTE]  
    >   Trinn 7 fungerer bare hvis du har definert følgende: På siden **Kort for bokf.grp.- aktiva** for bokføringsgruppen for aktivumet, inneholder **Vedlikeholdskonto**-feltet finansdebetkontoen og feltet **Motkonto for vedlikehold** inneholder finanskontoen du vil bokføre motposter for oppskrivning til. Hvis du vil ha mer informasjon, kan du se [Slik definerer du bokføringsgrupper for aktiva](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).
8. Velg handlingen **Bokfør**.

## <a name="to-follow-up-on-fixed-assets-service-visits"></a><a name="to-follow-up-on-fixed-assets-service-visits"></a><a name="to-follow-up-on-fixed-assets-service-visits"></a>Slik følger du opp servicebesøk for aktiva

Du kan skrive ut rapporten **Vedlikehold - neste service** for å se hvilke aktiva du har planlagt et servicebesøk for. Du kan også bruke denne rapporten når du oppdaterer feltet **Neste servicedato** på aktivakortene.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Vedlikehold neste service**, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene **Startdato** og **Sluttdato**.  
3. Velg knappen **Skriv ut** eller **Forhåndsvisning**.

## <a name="to-monitor-maintenance-costs"></a><a name="to-monitor-maintenance-costs"></a><a name="to-monitor-maintenance-costs"></a>Slik kontrollerer du vedlikeholdskostnader:

Du finner vedlikeholdskostnadene når du ser på aktivastatistikken.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Aktiva**, og velg deretter den relaterte koblingen.
2. Velg aktivaet du vil vise vedlikeholdskostnader for, og velg deretter **Avskrivningstablåer**.
3. På **Aktivaavskrivningstablå**-siden velger du det relevante aktivaavskrivningstablået, og velger deretter **Statistikk**-handlingen.
4. På **Aktivastatistikk**-siden velger du **Vedlikehold**-feltet.

**Vedlikeholdsposter**-siden åpnes med postene som utgjør beløpet i **Vedlikehold**-feltet.

## <a name="to-view-or-print-maintenance-costs-for-multiple-fixed-assets"></a><a name="to-view-or-print-maintenance-costs-for-multiple-fixed-assets"></a><a name="to-view-or-print-maintenance-costs-for-multiple-fixed-assets"></a>Slik viser eller skriver du ut vedlikeholdskostnader for flere aktiva:

I rapporten **Vedlikehold - analyse** kan du velge om du vil se vedlikehold basert på én, to eller tre vedlikeholdskoder for en angitt dato eller periode. Du kan også se summen av alle valgte aktiva eller summen for hvert aktiva.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Vedlikeholdsanalyse**, og velg deretter den relaterte koblingen.
2. Fyll ut feltene etter behov.
3. Velg knappen **Skriv ut** eller **Forhåndsvisning**.

## <a name="to-view-maintenance-ledger-entries"></a><a name="to-view-maintenance-ledger-entries"></a><a name="to-view-maintenance-ledger-entries"></a>Slik viser du vedlikeholdsposter

Du kan også studere vedlikeholdskostnadene ved å se på vedlikeholdspostene.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Aktiva**, og velg deretter den relaterte koblingen.
2. Velg aktivaet du vil vise poster for, og velg deretter **Avskrivningstablåer**.
3. På **Aktivaavskrivningstablå**-siden velger du det relevante aktivaavskrivningstablået, og velger deretter **Vedlikeholdsposter**-handlingen.

## <a name="to-view-or-print-maintenance-ledger-entries-for-multiple-fixed-assets"></a><a name="to-view-or-print-maintenance-ledger-entries-for-multiple-fixed-assets"></a><a name="to-view-or-print-maintenance-ledger-entries-for-multiple-fixed-assets"></a>Slik viser eller skriver du ut vedlikeholdsposter for flere aktiva:

I **Vedlikehold - detaljer**-rapporten kan du vise eller skrive ut vedlikeholdsposter for ett eller flere aktiva.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Vedlikeholdsdetaljer**, og velg deretter den relaterte koblingen.
2. Fyll ut feltene etter behov.
3. Velg knappen **Skriv ut** eller **Forhåndsvisning**.

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Se relatert [Microsoft-opplæring](/training/paths/manage-fixed-assets-maintenance-insurances/)

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se også

[Aktiva](fa-manage.md)  
[Definer aktiva](fa-setup.md)  
[Finans](finance.md)  
[Bli klar til å gjøre forretninger](ui-get-ready-business.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
