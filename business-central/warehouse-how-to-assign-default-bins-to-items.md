---
title: Tilordne standardhyller til varer
description: 'Hvis du bruker hyller i en lokasjon, kan du tilordne standardhyller til varene for å gjøre levering, mottak og flytting av varene enklere.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: '7371, 7374, 7379'
ms.date: 06/25/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="assign-default-bins-to-items"></a>Tilordne standardhyller til varer
Hvis du bruker hyller i en lokasjon, kan du tilordne standardhyller til varene for å gjøre levering, mottak og flytting av varene enklere. Når en standardhylle tilordnes en vare, foreslås denne hyllen hver gang du oppretter en transaksjon for denne varen. Standardhyller defineres på siden **Hylleinnhold**.  

## <a name="to-assign-a-default-bin-to-an-item"></a>Tilordne en standardhylle til en vare
1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Hylleinnholdopprett. – forslag**, og velg deretter den relaterte koblingen.  
2.  Fyll ut hyllekoden og opplysninger om varen for hver hylle du vil definere som standard for en vare. Pass på å velge **Standard**-feltet.  
3.  Velg **Opprett hylleinnhold**-handlingen. Standardhyllene tilordnes for varen.  

> [!NOTE]  
>  Hvis en vare ikke er tilordnet en standardhylle når den plasseres, vil hyllen der varen plasseres, tilordnes som standardhylle.  

## <a name="to-change-the-default-bin-for-an-item"></a>Slik endrer du standardhyllen for en vare
Det kan hende du må endre tilordningen av standardhylle for en vare eller tilordne en standardhylle til en ny vare.
1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Hylleinnhold** og velg den relaterte koblingen.  
2.  I feltet **Lokasjonsfilter** velger du den riktige lokasjonskoden.  
3.  Finn den gjeldende posten med standard hylleinnhold for varen, og fjern avmerkingen for **Standardhylle**.  
4.  Finn hylleinnholdslinjen for hyllen som du vil bruke som ny standardhylle. Merk av for **Standardhylle**.  

> [!NOTE]  
>  Hvis en vare ikke er tilordnet en standardhylle når den plasseres første gang, vil systemet tilordne hyllen der varen plasseres, som standardhylle.  

## <a name="see-also"></a>Se også
[Oversikt over lagerstyring](design-details-warehouse-management.md)
[Lager](inventory-manage-inventory.md)  
[Definer lagerstyring](warehouse-setup-warehouse.md) 
[Monteringsstyring](assembly-assemble-items.md)
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
