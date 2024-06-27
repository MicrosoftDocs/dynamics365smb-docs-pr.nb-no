---
ms.service: dynamics-365-business-central
---
> [!NOTE]
> Du kunne hente dataene fra ulike selskaper i én enkelt rapport med OData-nettjenester. Fra og med [!INCLUDE [prod_short](prod_short.md)] lanseringsbølge 2 for 2021 støttes imidlertid bare ODataV4. ODataV4 eksporterer ikke data fra flere selskaper. **$Expand**-funksjonen i Power BI som kunne tenkes å være en alternativ måte å opprette en rapport for flere selskaper på, kan heller ikke brukes. Den oppretter en kolonne med selskapsnavnet, men fyller den ikke ut med selskapsdataene etter en oppdatering.