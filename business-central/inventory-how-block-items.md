---
title: Slik sperrer du varer fra salg eller kjøp
description: Du kan hindre at en vare brukes, for eksempel i salgs- og kjøpsdokumenter.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: fb80cecd119cf061b3102d94f586da4c103bd21c
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/09/2020
ms.locfileid: "3784816"
---
# <a name="block-items-from-sales-or-purchasing"></a>Blokkere varer fra salg eller kjøp
Du kan blokkere en vare fra å bli lagt inn på linjer i salgs- eller bestillingsdokumenter, og du kan blokkere den fra å bli bokført i en transaksjon. Dette er for eksempel nyttig når en vare har en kjent defekt. Hvis noen velger en sperret vare på et salgs- eller kjøpsdokument, vil en melding gi beskjed om at varen er sperret.

Tabellen nedenfor beskriver hva som skjer når varer er sperret.  

|Alternativ|Beskrivelse|  
|--------------------|------------|  
|**Sperret salg**|Du kan ikke legge inn varen i et salgsdokument eller i en salgsvarekladd.|  
|**Innkjøp blokkert**|Du kan ikke legge inn varen i et kjøpsdokument, i en varekladd for kjøp eller i kjøpsplanleggingsprosesser.|  
|**Sperret**|Du kan ikke bruke varen til noen varetransaksjon.|  

> [!NOTE]
> Sperrede varer kan returneres. Dette betyr at ingen av innstillingene ovenfor gjelder når varen brukes i returordrer og kreditnotaer.

Når du bruker funksjonen **Kopier fra dokument** til å opprette nye dokumenter som er basert på eksisterende dokumenter, blir du varslet hvis det blir sperret varer på kildedokumentlinjene. De sperrede dokumentlinjene utelates fra det nye dokumentet, og en melding viser en oversikt over alle dokumentlinjene som er sperret i kildedokumentet.

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a>Sperre en vare fra å legges inn på salgslinjer  
1.  Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Varer**, og velg deretter den relaterte koblingen.  
2.  Velg varen du vil sperre, og velg deretter avmerkingsboksen **Sperret salg**.  

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a>Sperre en vare fra å legges inn på kjøpslinjer  
1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Varer**, og velg deretter den relaterte koblingen.  
2.  Velg varen du vil sperre, og velg deretter avmerkingsboksen **Sperret kjøp**.  

## <a name="to-block-an-item-from-being-posted"></a>Sperre en vare fra å bli bokført
1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Varer**, og velg deretter den relaterte koblingen.
2. Velg varen du vil sperre, og velg deretter avmerkingsboksen **Sperret**.

## <a name="see-also"></a>Se også  
[Registrere nye varer](inventory-how-register-new-items.md)  
[Lager](inventory-manage-inventory.md)  
