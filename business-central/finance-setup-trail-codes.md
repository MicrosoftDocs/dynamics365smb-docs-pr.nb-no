---
title: Definer koder for revisjonsspor
description: Finn ut mer om oppgavene for å konfigurere kildespor og årsaksspor som du kan bruke til å spore revisjonsspor.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'accounting, auditing, bookkeeping'
ms.search.form: '257, 259, 279'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="setting-up-source-codes-and-reason-codes-for-audit-trails"></a><a name="setting-up-source-codes-and-reason-codes-for-audit-trails"></a><a name="setting-up-source-codes-and-reason-codes-for-audit-trails"></a>Definere kildespor og årsaksspor for revisjonsspor

Alle bokførte poster tilordnes automatisk til et kildespor, slik at transaksjoner kan spores til utgangspunktet. Hvis du vil gi poster et ekstra kildespor, kan du bruke årsaksspor. Årsakssporene brukes til å vise hvorfor en post ble opprettet. Når du definerer årsaksspor, kan du tilordne dem til hele kladdemaler og kladder, og du kan også tilordne dem til individuelle kladdelinjer og dokumenter.  

For både kildespor og årsaksspor bruker du spor som er lette å huske, og som er beskrivende. Sporet må være unikt, og du kan definere så mange spor du vil.

## <a name="define-source-codes"></a><a name="define-source-codes"></a><a name="define-source-codes"></a>Definere kildespor

Noen ganger kan du ha behov for å se hvordan en spesiell post oppstod, for eksempel om den kom fra bokføring av en finanskladd eller en kjøpsfaktura. Et kildespor angir hvor en post ble opprettet. Postene opprettes når kladder og fakturaer bokføres og når visse kjørsler startes. Hver bokføringstype har et bestemt kildespor som tilordnes når posten opprettes.  

Bokføring av kladder, bestillinger, faktura eller kreditnota, og kjøring av ulike kjørsler oppretter poster i regnskapet. Siden **Kildespordefinisjon** inneholder én hurtigfane for hver modul. Hver hurtigfane inneholder kildesporene som kan brukes i den aktuelle modulen.

Når du bokfører eller starter en kjørsel, knyttes det riktige kildesporet til posten automatisk. Når du for eksempel bokfører fra en finanskladd, kodes posten som *FINKLD*. Du kan deretter filtrere **Finansposter**-siden for å vise hvilke poster som er bokført fra finanskladder eller salgsdokumenter, for eksempel

### <a name="to-define-source-codes"></a><a name="to-define-source-codes"></a><a name="to-define-source-codes"></a>Slik definerer du kildespor

1. Velg ikonet ![Søk etter side eller rapport.](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport") og angir **Kildespordefinisjon** og velger den relaterte koblingen.  

2. I vinduet **Kildespordefinisjon** angir du det aktuelle kildesporet for hver enkelt bokføringstype og kjørsel.  

Du kan endre innholdet i et felt senere, og denne endringen vil deretter påvirke fremtidige bokføringer.

## <a name="change-source-codes"></a><a name="change-source-codes"></a><a name="change-source-codes"></a>Endre kildespor

Noen ganger kan det være nødvendig å endre et kildespor. Du vil for eksempel endre kildesporet *FINKLD* til *FNK*.

### <a name="to-change-source-codes"></a><a name="to-change-source-codes"></a><a name="to-change-source-codes"></a>Slik endrer du kildespor

1. Velg ikonet ![Søk etter side eller rapport.](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport") og angi **Kildespor**, og velg deretter den relaterte koblingen.

2. På linjen med kildesporet som skal endres, velger du et spor i feltet **Spor**.

3. Angi den nye koden, og velg deretter **Ja**-knappen. Du kan også endre innholdet i feltet **Beskrivelse**.

Alle nye poster som bokføres fra finanskladden får det nye kildesporet.

## <a name="define-reason-codes"></a><a name="define-reason-codes"></a><a name="define-reason-codes"></a>Definere årsaksspor

Årsaksspor er et tillegg til kildesporene og brukes til å vise hvorfor en post ble opprettet. Du kan tildele årsaksspor på enkeltposter, og du kan overføre dem til poster og tilordne permanente koder til bestemte kladdemaler og kladder. Når et årsaksspor er tilknyttet en kladdelinje eller et salgs- og bestillingshode, merkes alle poster med årsakssporet når de bokføres.  

### <a name="to-set-up-reason-codes"></a><a name="to-set-up-reason-codes"></a><a name="to-set-up-reason-codes"></a>Slik setter du opp årsaksspor

1. Velg ikonet ![Søk etter side eller rapport.](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport")  og angi **Årsaksspor**, og velg deretter den relaterte koblingen.

2. Angi den første koden i **Spor**-feltet i **Årsaksspor**-vinduet. I feltet **Beskrivelse** skriver du inn en forklarende tekst.

Gjenta dette for hvert årsaksspor du vil bruke. Du kan opprette så mange årsaksspor du vil.

Følgende fremgangsmåte viser hvordan du legger til et årsaksspor i en kladdemal, men med lignende trinn gjelder det å legge til et årsaksspor i en kladdelinje eller varekladd.  

### <a name="to-assign-reason-codes-to-journal-templates"></a><a name="to-assign-reason-codes-to-journal-templates"></a><a name="to-assign-reason-codes-to-journal-templates"></a>Slik tilordner du årsaksspor til kladdemaler

1. Velg ikonet ![Søk etter side eller rapport.](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport")  og angi **Finanskladdmaler**, og velg deretter den relaterte koblingen.

2. På linjen med den valgte kladdemalen setter du inn ønsket spor i **Årsaksspor**-feltet.

3. Lukk kladdemalen.

Årsakssporet som er valgt overføres til nye kladder som opprettes med denne kladdemalen. Årsaksspor tilordnes kladdemaler i de andre modulene på samme måte.

### <a name="to-use-reason-codes-on-sales-and-purchase-documents"></a><a name="to-use-reason-codes-on-sales-and-purchase-documents"></a><a name="to-use-reason-codes-on-sales-and-purchase-documents"></a>Slik bruker du årsaksspor i salgs- og kjøpsdokumenter

1. Åpne det relevante salgs- eller kjøpsdokumentet.

2. Angi sporet i **Årsaksspor**-feltet i salgs- eller bestillingshodet.

Når fakturaen er bokført, overføres årsakssporet til hver finans-, kunde- og leverandørpost. Du kan ikke tilordne forskjellige årsaksspor til hver enkelt kjøps- og salgslinje, fordi alle linjene bokføres som én post.

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Se relatert [Microsoft-opplæring](/training/paths/set-up-financial-management-dynamics-365-business-central/)

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se også

[Finans](finance.md)  
[Avstemme bankkonter](bank-manage-bank-accounts.md)  
[Arbeid med dimensjoner](finance-dimensions.md)  
[Importere forretningsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Analysere kontantstrømmen i firmaet](finance-analyze-cash-flow.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]
