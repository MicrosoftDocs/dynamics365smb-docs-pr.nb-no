---
title: Slik blokkerer du salg til kunder
description: 'Hvis du må, kan du sperre en kunde fra å bli inkludert i salgsdokumenter og andre salgstransaksjoner.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="block-customers"></a><a name="block-customers"></a><a name="block-customers"></a>Sperre kunder
Du kan sperre en kunde, for eksempel på grunn av insolvens, slik at kunden ikke kan legges til i salgsdokumenter, eller slik at ingen transaksjoner kan bokføres for kunden.

I tillegg til å sperre en kunde kan du angi at fordringstransaksjoner for kunden skal settes på vent i forbindelse med purringer. Hvis du vil ha mer informasjon, kan du se [Innkreve utestående saldi](receivables-collect-outstanding-balances.md).   

Tabellen nedenfor beskriver alternativene for å sperre kunder.  

|Alternativ|Beskrivelse|  
|--------------------|------------|  
|**Tom**|Transaksjoner er tillatt for denne kunden.|
|**Levering**|Det kan ikke opprettes nye ordrer og nye leveringer for denne kunden. Eksisterende leveringer som ennå ikke er fakturert, kan faktureres.|  
|**Fakturering**|Det kan ikke opprettes nye ordrer, nye leveringer og nye fakturaer for denne kunden. Eksisterende leveringer som ennå ikke er fakturert, kan ikke faktureres. Du kan fortsatt sende purringer og rentenotaer til kunden.|  
|**Alle**|Ingen transaksjoner er tillatt for denne kunden, inkludert betalinger.|  

## <a name="to-block-a-customer"></a><a name="to-block-a-customer"></a><a name="to-block-a-customer"></a>Slik sperrer du en kunde:
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Kunder** og velger den relaterte koblingen.
2. Velg en kunde, og velg handlingen **Rediger**.
3. I **Sperret**-feltet velger du hva som skal sperres, som beskrevet i tabellen ovenfor.

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se også
[Registrere nye kunder](sales-how-register-new-customers.md)  
[Innkreve utestående saldi](receivables-collect-outstanding-balances.md)  
[Håndtere fordringer](receivables-manage-receivables.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
