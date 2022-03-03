---
title: Om fullførte produksjonsordrekostnader
description: Etterbehandling av produksjonsordren er nøkkelen til å fullføre kostlivssyklusen for en produksjonsvare. Endelige kostnader beregnes i kjørselen Juster kostverdi – vareposter.
author: SorenGP
ms.topic: conceptual
ms.search.form: 99000867
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: dd9010e055e5e24cafb87846b8eed98f54d83474
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2022
ms.locfileid: "8147833"
---
# <a name="about-finished-production-order-costs"></a>Om fullførte produksjonsordrekostnader

Det er viktig å gjøre ferdig produksjonsordren for å fullføre kostlivssyklusen til varen som produseres. De endelige kostbeløpene, herunder avvik i et standardkostmiljø, faktiske beløp i et kostmiljø av typen FIFO, gjennomsnitt eller LIFO, beregnes ved hjelp av kjørselen **Juster kostverdi - vareposter**, som tillater økonomisk avstemming av kostbeløpene for vareproduksjon. For at en produksjonsordre skal kunne behandles ved kostjustering, må statusen være **Ferdig**. Derfor er det avgjørende at statusen til en produksjonsordre endres til **Ferdig** når ordren er fullført.  

## <a name="example"></a>Eksempel

Når du i et standardkostmiljø forbruker materiale for å produsere en vare, inngår varekostnaden pluss arbeid og indirekte kostnader i VIA. Når varen er produsert, reduseres VIA med standardkostbeløpet for varen. Disse kostbeløpene nettoføres vanligvis ikke til null. For at disse kostnadene skal kunne nettoføres til null må du utføre kjørselen **Juster kostverdi - vareposter** og legge merke til at bare produksjonsordrer med status **Ferdig** vil tas med i beregningen ved justering.  

## <a name="see-also"></a>Se også

[Administrere lagerkostnader](finance-manage-inventory-costs.md)  
[Produksjon](production-manage-manufacturing.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]