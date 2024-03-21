---
title: Slik sperrer du varer eller Varevarianter fra salg eller kjøp
description: 'Du kan blokkere varer og varevarianter fra å bli lagt inn på linjer i salgs- eller bestillingsdokumenter, og du kan blokkere den fra å bli bokført i en transaksjon.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.search.keywords: 'item, variant, product'
ms.date: 08/22/2023
ms.service: dynamics-365-business-central
---
# Sperre varer eller Varevarianter fra salg eller kjøp

Du kan blokkere varer og varevarianter fra å bli lagt inn på linjer i salgs- eller bestillingsdokumenter, og du kan blokkere den fra å bli bokført i transaksjoner. Dette er for eksempel nyttig når en vare har en kjent defekt. Hvis noen velger en sperret vare eller variant på et salgs- eller kjøpsdokument, vil en melding gi beskjed om at varen er sperret.

Tabellen nedenfor beskriver hva som skjer når varer eller varianter er sperret.  

|Alternativ|Description|  
|--------------------|------------|  
|**Salg sperret**|Du kan ikke velge varen eller varianten i et salgsdokument eller i en salgsvarekladd.|  
|**Kjøp sperret**|Du kan ikke velge varen eller varianten i et kjøpsdokument, i en varekladd for kjøp eller i kjøpsplanleggingsprosesser.|  
|**Sperret**|Du kan ikke ta med varen eller varianten når du bokfører transaksjoner.|  

> [!NOTE]
> Sperrede varer kan returneres. Dette betyr at ingen av innstillingene ovenfor gjelder returordrer og kreditnotaer.

Når du bruker handlingen **Kopier fra dokument** til å opprette nye dokumenter som er basert på eksisterende dokumenter, blir du varslet hvis det blir sperret varer eller varianter på kildedokumentlinjene. De sperrede dokumentlinjene utelates fra det nye dokumentet, og en melding viser en oversikt over alle dokumentlinjene som er sperret i kildedokumentet.

## Slik blokkerer du en vare  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Varer** og velg den relaterte koblingen.  
2. Avhengig av hva du vil gjøre, velger du en vare, og velger deretter én eller flere av følgende avmerkingsbokser:
    * **Sperret**
    * **Salg sperret**
    * **Kjøp sperret**  

## Slik blokkerer du en variant  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Varer** og velg den relaterte koblingen.  
2. Velg varen som har en variant du vil blokkere, velg **Varianter**, og velg deretter én eller flere av følgende avmerkingsbokser:  
    * **Sperret**
    * **Salg sperret**
    * **Kjøp sperret**

## Se også  

[Registrer nye varer](inventory-how-register-new-items.md)  
[Lager](inventory-manage-inventory.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]