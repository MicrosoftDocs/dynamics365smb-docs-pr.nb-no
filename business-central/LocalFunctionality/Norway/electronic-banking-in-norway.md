---
title: Elektroniske banktjenester i Norge
description: Denne artikkelen beskriver forbedringene i den norske Business Central for håndtering av elektroniske banktjenester med mange operasjoner i den norske versjonen av Business Central.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 11/21/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="electronic-banking-in-norway"></a>Elektroniske banktjenester i Norge
[!INCLUDE[prod_short](../../includes/prod_short.md)] omfatter forbedringer i den norske versjonen for elektroniske banktjenester. Denne funksjonaliteten kan brukes til å utføre følgende operasjoner:  

- Motta elektroniske betalinger basert på en OCR-betalings-ID (optisk tegngjenkjenning).  
- Skrive ut kunde-ID-numre (KID) på salgsdokumenter.  
- Sende elektroniske betalinger til leverandører.  

## <a name="customer-identification-numbers"></a>Kundeidentifikasjonsnummer
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

## <a name="see-also"></a>Se også
 [Funksjonalitet som er spesifikk for norske brukere](norway-local-functionality.md)   
 [Norsk giro og OCR-B-skrift](norwegian-giro-and-ocr-b-font.md)   
 [Opprette KID-numre på salgsdokumenter](how-to-set-up-kid-numbers-on-sales-documents.md)   
 [Opprette OCR-betalinger](how-to-set-up-ocr-payments.md)   
 [Importere og bokføre OCR-betalinger](how-to-import-and-post-ocr-payments.md)   
 [Elektroniske betalinger til leverandører i Norge](electronic-payments-to-vendors-in-norway.md)   
 [Skrive ut rapporten OCR-kladd - test](how-to-print-the-ocr-journal-test-report.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
