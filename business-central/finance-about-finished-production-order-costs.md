---
title: Om fullførte produksjonsordrekostnader | Microsoft-dokumentasjon
description: Det er viktig å gjøre ferdig produksjonsordren for å fullføre kostlivssyklusen til varen som produseres. De endelige kostbeløpene, herunder avvik i et standardkostmiljø, faktiske beløp i et kostmiljø av typen FIFO, gjennomsnitt eller LIFO, beregnes ved hjelp av kjørselen Juster kostverdi - vareposter.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 509ee1cdbcf9c0ddd362435ed4d2319561a9e731
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2019
ms.locfileid: "2302647"
---
# <a name="about-finished-production-order-costs"></a>Om fullførte produksjonsordrekostnader
Det er viktig å gjøre ferdig produksjonsordren for å fullføre kostlivssyklusen til varen som produseres. De endelige kostbeløpene, herunder avvik i et standardkostmiljø, faktiske beløp i et kostmiljø av typen FIFO, gjennomsnitt eller LIFO, beregnes ved hjelp av kjørselen **Juster kostverdi - vareposter**, som tillater økonomisk avstemming av kostbeløpene for vareproduksjon. For at en produksjonsordre skal kunne behandles ved kostjustering, må statusen være **Ferdig**. Derfor er det avgjørende at statusen til en produksjonsordre endres til **Ferdig** når ordren er fullført.  

## <a name="example"></a>Eksempel  
 Når du i et standardkostmiljø forbruker materiale for å produsere en vare, inngår varekostnaden pluss arbeid og indirekte kostnader i VIA. Når varen er produsert, reduseres VIA med standardkostbeløpet for varen. Disse kostbeløpene nettoføres vanligvis ikke til null. For at disse kostnadene skal kunne nettoføres til null må du utføre kjørselen **Juster kostverdi - vareposter** og legge merke til at bare produksjonsordrer med status **Ferdig** vil tas med i beregningen ved justering.  

## <a name="see-also"></a>Se også  
[Administrere lagerkostnader](finance-manage-inventory-costs.md)  
[Produksjon](production-manage-manufacturing.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
