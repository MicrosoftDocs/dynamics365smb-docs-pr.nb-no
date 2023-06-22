---
title: Elektroniske banktjenester i Norge
description: Dette emnet beskriver forbedringene i den norske Business Central for håndtering av elektroniske banktjenester med flere operasjoner i den norske versjonen av Business Central.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/18/2021
ms.author: edupont
---
# <a name="electronic-banking-in-norway" />Elektroniske banktjenester i Norge
[!INCLUDE[prod_short](../../includes/prod_short.md)] omfatter forbedringer i den norske versjonen for elektroniske banktjenester. Denne funksjonaliteten kan brukes til å utføre følgende operasjoner:  

- Motta elektroniske betalinger basert på en OCR-betalings-ID (optisk tegngjenkjenning).  
- Skrive ut kunde-ID-numre (KID) på salgsdokumenter.  
- Sende elektroniske betalinger til leverandører.  

## <a name="customer-identification-numbers" />Kundeidentifikasjonsnummer
 Kunde-ID (KID) er et kundeidentifikasjonsnummer som inneholder en betalingsreferanse til leverandøren, og sikrer at betalingen bokføres riktig hos leverandøren. Hvis leverandørdokumentene inneholder KID-nummer, må du bruke dette nummeret fordi det kan påløpe et tilleggsgebyr for betalingen hvis du ikke bruker nummeret.  

 KID kan angis på følgende lokasjoner:  

- Salgsfakturaer  
- Rentenotaer  
- Purringer  
- Bestillinger  
- Kjøpsfakturaer  
- Kjøpskladder  
- Remitteringskladder  

> [!NOTE]  
>  KID-nummeret kan ikke brukes på kreditnotaer. Hvis en kreditnota er en del av betalingen, må fakturaene i den samme betalingen behandles som betalinger uten KID-nummer.  

## <a name="see-also" />Se også
 [Funksjonalitet som er spesifikk for norske brukere](norway-local-functionality.md)   
 [Norsk giro og OCR-B-skrift](norwegian-giro-and-ocr-b-font.md)   
 [Opprette KID-numre på salgsdokumenter](how-to-set-up-kid-numbers-on-sales-documents.md)   
 [Opprette OCR-betalinger](how-to-set-up-ocr-payments.md)   
 [Importere og bokføre OCR-betalinger](how-to-import-and-post-ocr-payments.md)   
 [Elektroniske betalinger til leverandører i Norge](electronic-payments-to-vendors-in-norway.md)   
 [Skrive ut rapporten OCR-kladd - test](how-to-print-the-ocr-journal-test-report.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
