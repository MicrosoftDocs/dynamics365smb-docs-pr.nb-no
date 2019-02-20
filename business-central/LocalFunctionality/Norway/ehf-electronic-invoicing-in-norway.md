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
ms.sourcegitcommit: 5e8dfa9572b84360bfcc5087bc3b0b9b9ed9182f
ms.openlocfilehash: 10d2a7bb82e4d364f808494b78546a911a1d8a12
ms.contentlocale: nb-no
ms.lasthandoff: 01/03/2019

---
# <a name="ehf-electronic-invoicing-in-norway"></a>EHF – Elektronisk fakturering i Norge
Selskaper som må sende salgsfakturaer og kreditnotaer elektronisk til norsk offentlig sektor i Elektronisk Handelsformat (EHF) basert på UBL (Universal Business Language). Hvis et selskap ikke sender dokumentene elektronisk, kan myndighetene nekte betaling. Standardformatet som støttes for elektronisk utveksling mellom parter, er formatet Ehandel.no. Hvis du vil ha mer informasjon om EHF elektronisk fakturering, kan du se [E-innkjøp](https://www.anskaffelser.no/public-procurement-information-english).  

## <a name="implementation-in-included365finincludesd365finmdmd"></a>Implementering i [!INCLUDE[d365fin](../../includes/d365fin_md.md)]  
Fra januar 2019 vil kravene for å sende elektroniske fakturaer være basert på PEPPOL BIS Billing 3.0-standarden. Hvis du vil ha mer informasjon, kan du se siden [EHF Billing 3.0](https://test-vefa.difi.no/ehf/g3/billing-3.0/norway/) fra Direktoratet for forvaltning og ikt. Selskaper som allerede sender elektroniske dokumenter i før-2019-format, kan fortsette å gjøre dette i 2019.

Hvis du vil sende dokumenter elektronisk, må du tilordne EAN-lokasjonsnumre (European Article Numbering) og kontokoder til de aktuelle kundene på **Kundekort**-siden. Du finner mer informasjon under [Sette opp kunder for EHF](how-to-set-up-customers-for-ehf.md). Disse numrene inkluderes når du oppretter, bokfører eller utsteder dokumenter. Nå dokumentene bokføres eller utstedes, kan du opprette elektroniske versjoner som sendes til kunder.  

[!INCLUDE[d365fin](../../includes/d365fin_md.md)] eksporterer enkelte elektroniske dokumenter i EHF versjon 3.0, som bruker UBL versjon 2.1. Du kan sende følgende typer dokumenter:  

- Salgs- og servicefakturaer
- Salgs- og servicekreditnotaer

[!INCLUDE[d365fin](../../includes/d365fin_md.md)] eksporterer andre elektroniske dokumenter i versjon 1.6, som bruker UBL versjon 2.0. Du kan sende følgende typer dokumenter:  

- Rentenota  
- Purring  

Du kan angi hvor du skal lagre elektroniske dokumenter, på siden **Salgsoppsett**. Du kan også bruke [dokumentutvekslingsfunksjonaliteten](../../across-how-to-set-up-electronic-document-sending-and-receiving.md) til å generere og sende dem.

## <a name="vat-treatment"></a>Mva-justering  
Mva-prosenter og transaksjonstypen bestemmer mva-typen som eksporteres i det elektroniske dokumentet.  

|XML|Type| 
|---------|----------|  
|S|Utgående mva, vanlige sats|
|H|Utgående mva, redusert sats – matvarer og drikkevarer|
|R|Utgående mva, redusert sats – rå fisk|
|AA|Utgående mva, lav sats|
|AE|Snudd avregning|
|L|Kanariøyene, generell indirekte mva|
|M|Mva for produksjon, tjenester og import for Ceuta og Melilla|
|G|Gratis eksportvare, avgift betales ikke|
|O|Tjenester utenfor området for mva|
|Ø|Mva-fritak|
|Z|Mva-fritak (varer og tjenester som ikke omfattes av mva-bestemmelsene)|
|K|Mva-fritak for intra-EU-levering av varer og tjenester|

## <a name="see-also"></a>Se også  
[Sette opp kunder for EHF](how-to-set-up-customers-for-ehf.md)

