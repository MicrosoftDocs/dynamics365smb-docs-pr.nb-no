---
title: Definere lageransatte
description: 'Hver bruker som utfører lageraktiviteter, må defineres som en lageransatt tilordnet til én standardlokasjon og eventuelt flere ikke-standardlokasjoner.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 03/09/2023
ms.custom: bap-template
ms.search.form: '7328, 7348'
---
# <a name="set-up-warehouse-employees"></a>Definere lageransatte

Hver bruker som utfører lageraktiviteter, må defineres som en lageransatt tilordnet til en standardlokasjon. [!INCLUDE [prod_short](includes/prod_short.md)] filtrerer lageraktiviteter på den ansattes standardlokasjon. De kan bare utføre lageraktiviteter på lokasjonen. Du kan også tildele en bruker til andre lokasjoner. De kan få tilgang til, men ikke utføre aktiviteter på disse lokasjonene.

## <a name="to-set-up-warehouse-employees"></a>Slik definerer du lageransatte

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lageransatte**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**.  
3. Velg **Bruker-ID**-feltet, og velg deretter brukeren som skal legges til som lageransatt. Velg **OK**-knappen.  
4. I feltet **Lokasjonskode** skriver du inn koden for lokasjonen der brukeren skal arbeide.  
5. Slå på **Standard** for å angi at det er den eneste lokasjonen der den ansatte kan utføre lageraktiviteter.  
6. Gjenta disse trinnene for å tilordne andre ansatte til lokasjoner, eller for å tilordne andre lokasjoner til eksisterende lageransatte.  

## <a name="see-related-microsoft-training"></a>Se relatert [Microsoft-opplæring](/training/modules/get-started-warehouse-management/)

## <a name="see-also"></a>Se også

[Oversikt over lagerstyring](design-details-warehouse-management.md)
[Lager](inventory-manage-inventory.md)  
[Definer lagerstyring](warehouse-setup-warehouse.md)  
[Monteringsstyring](assembly-assemble-items.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Definer en fakturabokføringspolicy for brukere](admin-setup-invoice-posting-policy.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
