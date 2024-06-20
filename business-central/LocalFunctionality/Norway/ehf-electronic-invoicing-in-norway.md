---
title: EHF – Elektronisk fakturering i Norge
description: Selskaper som må sende salgsfakturaer og kreditnotaer elektronisk til norsk offentlig sektor i Elektronisk Handelsformat (EHF) basert på UBL (Universal Business Language).
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: '21, 459'
ms.date: 06/18/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# EHF – Elektronisk fakturering i Norge
Selskaper som må sende salgsfakturaer og kreditnotaer elektronisk til norsk offentlig sektor i Elektronisk Handelsformat (EHF) basert på UBL (Universal Business Language). Hvis et selskap ikke sender dokumentene elektronisk, kan myndighetene nekte betaling. Standardformatet som støttes for elektronisk utveksling mellom parter, er formatet Ehandel.no. Hvis du vil ha mer informasjon om EHF elektronisk fakturering, kan du se [Anskaffelser.no](https://www.anskaffelser.no).  

## Implementering i [!INCLUDE[prod_short](../../includes/prod_short.md)]  
Fra januar 2019 vil kravene for å sende elektroniske fakturaer være basert på PEPPOL BIS Billing 3.0-standarden. Hvis du vil ha mer informasjon, kan du se siden [EHF Billing 3.0](https://test-vefa.difi.no/ehf/g3/billing-3.0/norway/) fra Direktoratet for forvaltning og ikt. Selskaper som allerede sender elektroniske dokumenter i før-2019-format, kan fortsette å gjøre dette i 2019.

Hvis du vil sende dokumenter elektronisk, må du tilordne EAN-lokasjonsnumre (European Article Numbering) og kontokoder til de aktuelle kundene på **Kundekort**-siden. Du finner mer informasjon under [Sette opp kunder for EHF](how-to-set-up-customers-for-ehf.md). Disse numrene inkluderes når du oppretter, bokfører eller utsteder dokumenter. Nå dokumentene bokføres eller utstedes, kan du opprette elektroniske versjoner som sendes til kunder.  

[!INCLUDE[prod_short](../../includes/prod_short.md)] eksporterer enkelte elektroniske dokumenter i EHF versjon 3.0, som bruker UBL versjon 2.1. Du kan sende følgende typer dokumenter:  

- Salgs- og servicefakturaer
- Salgs- og servicekreditnotaer

[!INCLUDE[prod_short](../../includes/prod_short.md)] eksporterer andre elektroniske dokumenter i versjon 1.6, som bruker UBL versjon 2.0. Du kan sende følgende typer dokumenter:  

- Rentenota  
- Purring  

Du kan angi hvor du skal lagre elektroniske dokumenter, på siden **Salgsoppsett**. Du kan også bruke [dokumentutvekslingsfunksjonaliteten](../../across-how-to-set-up-electronic-document-sending-and-receiving.md) til å generere og sende dem.

## Mva-justering  
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

## MVA-skjema
Kontroller at du har definert den riktige verdien i feltet **Mva-skjema** på siden **Land/regioner**.

## Se også  
[Sette opp kunder for EHF](how-to-set-up-customers-for-ehf.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]