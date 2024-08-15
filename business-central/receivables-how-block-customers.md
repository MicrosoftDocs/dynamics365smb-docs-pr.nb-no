---
title: Slik blokkerer du salg til kunder
description: 'Hvis du må, kan du sperre en kunde fra å bli inkludert i salgsdokumenter og andre salgstransaksjoner.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 07/05/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Blokker kunder
Du kan sperre en kunde, for eksempel på grunn av insolvens, slik at kunden ikke kan legges til i salgsdokumenter, eller slik at ingen transaksjoner kan bokføres for kunden.

I tillegg til å sperre en kunde kan du angi at fordringstransaksjoner for kunden skal settes på vent i forbindelse med purringer. Hvis du vil ha mer informasjon, kan du se [Innkreve utestående saldi](receivables-collect-outstanding-balances.md).   

Tabellen nedenfor beskriver alternativene for å sperre kunder.  

|Alternativ|Beskrivelse|  
|--------------------|------------|  
|**Tom**|Transaksjoner er tillatt for denne kunden.|
|**Levere**|Nye ordrer og nye forsendelser kan ikke opprettes for denne kunden. Eksisterende leveringer som ennå ikke er fakturert, kan faktureres.|  
|**Fakturering**|Det kan ikke opprettes nye ordrer, nye leveringer og nye fakturaer for denne kunden. Eksisterende forsendelser som ennå ikke er fakturert, kan ikke faktureres. Du kan fortsatt sende purringer og rentenotaer til kunden.|  
|**Alle**|Ingen transaksjoner er tillatt for denne kunden, inkludert betalinger.|  

## Slik sperrer du en kunde:  
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Kunder** og velger den relaterte koblingen.
2. Velg en kunde, og velg handlingen **Rediger**.
3. I **Sperret**-feltet velger du hva som skal sperres, som beskrevet i tabellen ovenfor.

## Se også  
[Registrer nye kunder](sales-how-register-new-customers.md)  
[Innkrev utestående saldoer](receivables-collect-outstanding-balances.md)  
[Håndtere fordringer](receivables-manage-receivables.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]