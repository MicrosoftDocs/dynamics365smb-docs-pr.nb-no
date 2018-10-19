---
title: "EHF – Elektronisk fakturering i Norge"
description: "Selskaper som må sende salgsfakturaer og kreditnotaer elektronisk til norsk offentlig sektor i Elektronisk Handelsformat (EHF) basert på UBL (Universal Business Language)."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 6f6c9af3f85c8125a67a83c426ad3c124c60677c
ms.contentlocale: nb-no
ms.lasthandoff: 09/28/2018

---
# <a name="ehf-electronic-invoicing-in-norway"></a>EHF – Elektronisk fakturering i Norge
Selskaper som må sende salgsfakturaer og kreditnotaer elektronisk til norsk offentlig sektor i Elektronisk Handelsformat (EHF) basert på UBL (Universal Business Language). Hvis et selskap ikke sender dokumentene elektronisk, kan myndighetene nekte betaling. Standardformatet som støttes for elektronisk utveksling mellom parter, er formatet Ehandel.no.  

Hvis du vil ha mer informasjon om EHF elektronisk fakturering, kan du se [E-innkjøp](https://www.anskaffelser.no/public-procurement-information-english).  

## <a name="implementation-in-included365finincludesd365finmdmd"></a>Implementering i [!INCLUDE[d365fin](../../includes/d365fin_md.md)]  
 Gjeldende krav for å sende elektroniske fakturaer er basert på standarden Universal Business Language (UBL) versjon 2.1. Hvis du vil ha mer informasjon, kan du se nettstedet til https://aka.ms/OasisUblSite. De genererte XML-dokumentene kan deretter sendes til kunden.  

 Hvis du vil sende dokumenter elektronisk, må du tilordne EAN-lokasjonsnumre (European Article Numbering) og kontokoder til de aktuelle kundene i **Kundekort**-vinduet. Du finner mer informasjon under [Sette opp kunder for EHF](how-to-set-up-customers-for-ehf.md). Disse numrene inkluderes når du oppretter dokumenter, og bokfører eller utsteder dem. Nå dokumentene er bokført eller utstedt, kan du opprette elektroniske versjoner som skal sendes til kunden.  

 [!INCLUDE[d365fin](../../includes/d365fin_md.md)] eksporterer enkelte elektroniske dokumenter i versjon 2.0, som bruker UBL versjon 2.1. Du kan sende følgende typer dokumenter:  

- Salgsfaktura  
- Servicefaktura  
- Salgskreditnota  
- Salgskreditnota (service)  

 [!INCLUDE[d365fin](../../includes/d365fin_md.md)] eksporterer andre elektroniske dokumenter i versjon 1.6, som bruker UBL versjon 2.0. Du kan sende følgende typer dokumenter:  

- Rentenota  
- Purring  

De elektroniske dokumentene lagres i lokasjonene som defineres i vinduet Salgsoppsett.  

## <a name="vat-treatment"></a>Mva-justering  
 Mva-prosenter og transaksjonstypen bestemmer mva-typen som eksporteres i det elektroniske dokumentet.  

|XML|Type|Prosentsats|  
|---------|----------|---------------------|  
|S|Utgående mva, vanlige sats|25|  
|H|Utgående mva, redusert sats – matvarer og drikkevarer|15|  
|R|Utgående mva, redusert sats – rå fisk|11.11|  
|AA|Utgående mva, lav sats|8|  
|Ø|Mva-fritak|0|  
|Z|Mva-fritak (varer og tjenester som ikke omfattes av mva-bestemmelsene)|Ingen, rapporteres som 0|  
|K|Utslippstillatelser for private og offentlige bedrifter – kjøperen beregner mva|Ingen, rapporteres som 0|  

## <a name="see-also"></a>Se også  
 [Sette opp kunder for EHF](how-to-set-up-customers-for-ehf.md)

