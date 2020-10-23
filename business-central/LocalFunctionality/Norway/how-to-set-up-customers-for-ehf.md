---
title: Sette opp kunder for EHF
description: Hvis du vil opprette dokumenter i Elektronisk Handelsformat (EHF) for kunder i offentlig sektor, må du legge til EHF-informasjon for de aktuelle kundene.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: e7437d2f9cf812f6a098648f6359fd7f0b489e94
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3919773"
---
# <a name="set-up-customers-for-ehf"></a>Sette opp kunder for EHF
Hvis du vil opprette dokumenter i Elektronisk Handelsformat (EHF) for kunder i offentlig sektor, må du legge til EHF-informasjon for de aktuelle kundene.  

Dette emnet beskriver bare felt som gjelder EHF. Hvis du vil ha mer informasjon om hvordan du konfigurerer kunder generelt, se [Registrere nye kunder](../../sales-how-register-new-customers.md).  

## <a name="to-set-up-a-customer-that-uses-elektronisk-handelsformat"></a>Slik definerer du en kunde som bruker Elektronisk Handelsformat:  

1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](../../media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kunder**, og velg deretter den relaterte koblingen.  
2.  Åpne kunden du vil aktivere for EHF.  
3.  I hurtigfanen **Fakturering** fyller du ut feltene som beskrevet i tabellen nedenfor.  

    |Felt|Description|  
    |---------------------------------|---------------------------------------|  
    |**GLN**|Påkrevd. Angi det globale lokasjonsnummeret (GLN) for kunden.|  
    |**Kontokode**|Angi kontokoden for kunden.<br /><br /> Kunder i offentlig sektor gir en kontokode når de plasserer en ordre eller rekvisisjon. Basert på verdien i dette feltet, inkluderes kontokoden i EHF-dokumentene du oppretter i [!INCLUDE[d365fin](../../includes/d365fin_md.md)]. Se Kontokode for mer informasjon.|  
    |**E-faktura**|Merk av for å bruke elektronisk fakturering med kunden.|  
    |**Ansvarssenter**|Kontroller at ansvarssenteret du har valgt, har angitt en lands-/regionkode.|  

Disse feltene er spesifikke for EHF. Verdiene brukes i alle EHF-dokumenter du oppretter for denne kunden. Hvis du vil ha mer informasjon, se [EHF – Elektronisk fakturering i Norge](ehf-electronic-invoicing-in-norway.md).  

## <a name="see-also"></a>Se også  
 [Opprette elektroniske dokumenter for EHF](how-to-create-electronic-documents-for-ehf.md)   
 [Angi EHF](how-to-set-up-ehf.md)
