---
title: Definer lagerføringsenheter
description: Bruk lagerføringsenheter til å registrere opplysninger om varer for en bestemt lokasjon eller en bestemt variant.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 04/19/2023
ms.custom: bap-template
ms.search.forms: '5704, 5700, 5702, 5701'
---

# <a name="set-up-stockkeeping-units"></a>Konfigurer lagerføringsenheter

Bruk lagerføringsenheter til å registrere opplysninger om varer for en bestemt lokasjon eller en variant. De gjør det mulig å legge til ulike opplysninger om en vare for en bestemt lokasjon, for eksempel:

* et lager eller distribusjonssenter
* Varianter, for eksempel forskjellige hyllenumre og annen etterfyllingsinformasjon, for den samme varen  

## <a name="to-set-up-a-stockkeeping-unit"></a>Slik definerer du lagerføringsenheter

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lagerføringsenheter**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**.  
3. Fyll ut feltene etter behov. Følgende felt er obligatoriske: **Varenr.**, **Lokasjonskode** og/eller **Variantkode**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Når du har definert den første lagerføringsenheten for en vare, blir det merket av for **Lagerføringsenhet** på **varekortet**.  

Hvis du vil opprette flere lagerføringsenheter for en vare, bruker du kjørselen **Opprett lagerføringsenhet**. Hvis du vil finne ut mer om satsvise jobber, kan du gå til [Bruk jobbkøer til å planlegge oppgaver](admin-job-queues-schedule-tasks.md).  

> [!NOTE]  
> Opplysningene på **lagerføringsenhetskortet** har høyere prioritet enn opplysningene på **varekortet**.

> [!Warning]
> Hvis lagerføringsenheten angis via produksjon, brukes ikke **Kostpris (standard)**-feltet når faktisk kost for den produserte varen faktureres og justeres. I stedet bruker [!INCLUDE [prod_short](includes/prod_short.md)] verdien i **Standardkostnad**-feltet på det underliggende varekortet, og eventuelle avvik beregnes mot kostandelene for denne varen.<br><br>
> Selvom du kan tildele produksjonsstykklister og rutinger til lagerføringssenheter, er ikke opprulling av enhetskost og den relaterte beregningen av kostandeler tilgjengelig på lagerføringsenheter. Hvis du vil finne ut mer om standardkostnader, går du til [Om beregne standardkostnad](finance-about-calculating-standard-cost.md)

## <a name="see-related-microsoft-training"></a>Se relatert [Microsoft-opplæring](/training/modules/control-inventory-multiple-locations/)

## <a name="see-also"></a>Se også

[Registrere nye varer](inventory-how-register-new-items.md)  
[Definer lagerstyring](warehouse-setup-warehouse.md)  
[Oversikt over lagerstyring](design-details-warehouse-management.md)
[Lager](inventory-manage-inventory.md)  
[Monteringsstyring](assembly-assemble-items.md)    
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
