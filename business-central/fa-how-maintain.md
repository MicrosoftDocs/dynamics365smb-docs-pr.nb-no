---
title: Vedlikehold aktiva
description: Registrer reparasjoner og service på et aktiva for å bevare verdien.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'repair, service'
ms.search.form: '5642, 5625'
ms.date: 05/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="maintain-fixed-assets"></a>Vedlikehold aktiva

Vedlikeholdskostnader er driftsutgifter for tingene du gjør for å bevare tilstanden til dine faste aktiva. I motsetning til kapitalforbedringer øker ikke vedlikehold verdien av aktivaene dine.

Hver gang du sender et aktiva på service, registrerer du alle aktuelle opplysninger, for eksempel servicedato, leverandøren som utførte arbeidet, og serviceagentens telefonnummer. Du angir vedlikeholdsinformasjon på flere sider:

* Aktivakort
* Bestilling
* Kjøpsfaktura
* Aktiva finanskladd

Indeksregulering brukes til å justere verdier for generelle endringer i prisnivået. Bruk handlingen **Indeksreg. aktiva** til å beregne vedlikeholdskostnadene på nytt.

## <a name="record-a-maintenance-cost-directly-on-a-fixed-asset"></a>Registrer en vedlikeholdskostnad direkte på et anleggsmiddel

Hver gang det er utført vedlikehold for et aktivum, for eksempel et servicebesøk, kan du registrere dette på siden **Vedlikeholdsregistrering**.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Aktiva**, og velg deretter den relaterte koblingen.  
2. Velg aktivaet du vil registrere vedlikehold for, og velg deretter **Vedlikeholdsregistrering**.
3. På siden **Vedlikeholdsregistrering** fyller du ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="post-maintenance-costs-from-a-fixed-asset-gl-journal"></a>Bokfør vedlikeholdskostnader fra en aktivafinanskladd

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Avskrivningstablå – oversikt**, og velg deretter den relaterte koblingen.  
2. Velg avskrivningstablået som er tilordnet til aktivaet, og velg deretter **Rediger**-handlingen.
3. På siden **Avskrivningstablåkort** kontrollerer du at det ikke er merket av for **Vedlikehold**, slik at du ikke bokfører vedlikeholdskostnader i Finans.
4. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Aktivafinanskladder**, og velg deretter den relaterte koblingen.  
5. Opprett en innledende kladdelinje, og fyll ut feltene etter behov.
6. I feltet **Aktivabokf.type** velger du **Vedlikehold**.
7. Velg **Sett inn aktivamotkonto**. En ny kladdelinje opprettes for motkontoen som er satt opp for vedlikeholdsbokføring.

    > [!NOTE]  
    > Trinn 7 fungerer bare hvis du har definert følgende: På siden **Kort for bokf.grp.- aktiva** for bokføringsgruppen for aktivumet, inneholder **Vedlikeholdskonto**-feltet finansdebetkontoen og feltet **Motkonto for vedlikehold** inneholder finanskontoen du vil bokføre motposter for oppskrivning til. Hvis du vil ha mer informasjon, kan du se [Slik definerer du bokføringsgrupper for aktiva](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).
8. Velg handlingen **Bokfør**.

## <a name="record-maintenance-cost-from-a-purchase-invoice"></a>Registrer vedlikeholdskostnader fra en kjøpsfaktura

Trinnene nedenfor beskriver hvordan du registrerer vedlikeholdskostnader for et aktivum fra en kjøpsfaktura. Trinnene er de samme for bestillinger.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Kjøpsfaktura**, og velg deretter den relaterte koblingen.
2. Fyll ut feltene i hurtigfanen **Generelt** etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. På hurtigfanen **Linjer**, i **Type**-feltet, velger du **Aktiva**.
4. I **Nr.** -feltet velger du aktivumet, og deretter angir du antall og kostnad.
5. I feltet **Aktivabokf.type** velger du **Vedlikehold**.
6. Bokfør kjøpsfakturaen.

## <a name="follow-up-on-service-visits"></a>Følg opp på servicebesøk

Du kan skrive ut rapporten **Vedlikehold - neste service** for å føre op aktivaene som er planlagt for service. Du kan også bruke denne rapporten når du vil oppdatere feltet **Neste servicedato** på aktivakortene.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Vedlikehold neste service**, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene **Startdato** og **Sluttdato**.  
3. Velg knappen **Skriv ut** eller **Forhåndsvisning**.

## <a name="monitor-maintenance-costs"></a>Overvåk vedlikeholdskostnader

Du kan vise statistikk for å overvåke vedlikeholdskostnader.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Aktiva**, og velg deretter den relaterte koblingen.
2. Velg aktivaet du vil vise vedlikeholdskostnader for, og velg deretter **Avskrivningstablåer**.
3. På **Aktivaavskrivningstablå**-siden velger du det relevante aktivaavskrivningstablået, og velger deretter **Statistikk**-handlingen.
4. På **Aktivastatistikk**-siden velger du **Vedlikehold**-feltet.

Bruk **Vedlikeholdsposter**-siden åpnes til å se postene som utgjør beløpet i **Vedlikehold**-feltet.

## <a name="view-or-print-maintenance-costs-for-multiple-fixed-assets"></a>Vis eller skriv ut vedlikeholdskostnader for flere aktiva

I rapporten **Vedlikehold - analyse** kan du velge om du vil undersøke vedlikehold basert på én, to eller tre vedlikeholdskoder for en spesifikk dato eller periode. Rapporten kan vise summen for alle valgte aktiva eller summen for hvert aktiva.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Vedlikeholdsanalyse**, og velg deretter den relaterte koblingen.
2. Fyll ut feltene etter behov.
3. Velg knappen **Skriv ut** eller **Forhåndsvisning**.

## <a name="view-maintenance-ledger-entries"></a>Vis vedlikeholdsposter

Du kan også utforske vedlikeholdskostnadene ved å se på vedlikeholdspostene.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Aktiva**, og velg deretter den relaterte koblingen.
2. Velg aktivaet du vil vise poster for, og velg deretter **Avskrivningstablåer**.
3. På **Aktivaavskrivningstablå**-siden velger du det relevante aktivaavskrivningstablået, og velger deretter **Vedlikeholdsposter**-handlingen.

## <a name="view-or-print-maintenance-ledger-entries-for-multiple-fixed-assets"></a>Vis eller skriv ut vedlikeholdsposter for flere aktiva

I **Vedlikehold - detaljer**-rapporten kan du vise eller skrive ut vedlikeholdsposter for ett eller flere aktiva.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Vedlikeholdsdetaljer**, og velg deretter den relaterte koblingen.
2. Fyll ut feltene etter behov.
3. Velg knappen **Skriv ut** eller **Forhåndsvisning**.

## <a name="see-also"></a>Se også

[Aktiva](fa-manage.md)  
[Definer aktiva](fa-setup.md)  
[Finans](finance.md)  
[Bli klar til å gjøre forretninger](ui-get-ready-business.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
