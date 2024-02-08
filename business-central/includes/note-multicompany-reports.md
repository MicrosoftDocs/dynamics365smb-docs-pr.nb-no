---
ms.service: dynamics-365-business-central
---
> [!NOTE]
> Det var mulig å hente dataene fra ulike selskaper i én enkelt rapport med OData-nettjenester. Men siden lanseringsbølge 2 i 2021 for [!INCLUDE [prod_short](prod_short.md)], støttes bare ODataV4, som ikke eksporterer data fra flere selskaper. **$Expand**-funksjonen i Power BI som du tror kan være en alternativ måte å opprette en rapport for flere selskaper, kan heller ikke brukes. Den oppretter en kolonne med selskapsnavnet, men fyller den ikke med selskapsdataene etter en oppdatering.