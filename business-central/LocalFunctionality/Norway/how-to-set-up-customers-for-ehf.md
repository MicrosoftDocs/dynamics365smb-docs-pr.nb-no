---
title: Sette opp kunder for EHF
description: Hvis du vil opprette dokumenter i Elektronisk Handelsformat (EHF) for kunder i offentlig sektor, må du legge til EHF-informasjon for de aktuelle kundene.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 7a4c552ea0eef3f0ce93774a501f4e17724af9f9
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/08/2021
ms.locfileid: "6438974"
---
# <a name="set-up-customers-for-ehf"></a>Sette opp kunder for EHF
Hvis du vil opprette dokumenter i Elektronisk Handelsformat (EHF) for kunder i offentlig sektor, må du legge til EHF-informasjon for de aktuelle kundene.  

Dette emnet beskriver bare felt som gjelder EHF. Hvis du vil ha mer informasjon om hvordan du konfigurerer kunder generelt, se [Registrere nye kunder](../../sales-how-register-new-customers.md).  

## <a name="to-set-up-a-customer-that-uses-elektronisk-handelsformat"></a>Slik definerer du en kunde som bruker Elektronisk Handelsformat:  

1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Kunder** og velger den relaterte koblingen.  
2.  Åpne kunden du vil aktivere for EHF.  
3.  I hurtigfanen **Fakturering** fyller du ut feltene som beskrevet i tabellen nedenfor.  

    |Felt|Description|  
    |---------------------------------|---------------------------------------|  
    |**GLN**|Påkrevd. Angi det globale lokasjonsnummeret (GLN) for kunden.|  
    |**Kontokode**|Angi kontokoden for kunden.<br /><br /> Kunder i offentlig sektor gir en kontokode når de plasserer en ordre eller rekvisisjon. Basert på verdien i dette feltet, inkluderes kontokoden i EHF-dokumentene du oppretter i [!INCLUDE[prod_short](../../includes/prod_short.md)]. Se Kontokode for mer informasjon.|  
    |**E-faktura**|Merk av for å bruke elektronisk fakturering med kunden.|  
    |**Ansvarssenter**|Kontroller at ansvarssenteret du har valgt, har angitt en lands-/regionkode.|  

Disse feltene er spesifikke for EHF. Verdiene brukes i alle EHF-dokumenter du oppretter for denne kunden. Hvis du vil ha mer informasjon, se [EHF – Elektronisk fakturering i Norge](ehf-electronic-invoicing-in-norway.md).  

## <a name="see-also"></a>Se også  
 [Opprette elektroniske dokumenter for EHF](how-to-create-electronic-documents-for-ehf.md)   
 [Angi EHF](how-to-set-up-ehf.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]