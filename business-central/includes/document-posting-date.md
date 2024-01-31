---
author: brentholtorf
ms.topic: include
ms.date: 11/14/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

Feltene **Bilagsdato** og **Bokføringsdato**  på salgs- og kjøpsdokumenter kan hjelpe deg med å overholde regnskapsstandarder og sikre nøyaktige økonomiske beregninger. Feltene har ulike formål:

- For at [!INCLUDE [prod_short](prod_short.md)] skal kunne beregne rentebelastning og det forfalte beløpet på salgsfakturaer, må **dokumentdatoen** samsvare med én av følgende datoer:

   - Datoen på salgsfakturaen du sendte til kunden. 
   - Datoen på kjøpsfakturaen du mottok fra leverandøren.
- **Bokføringsdatoen** viser når et dokument ble registrert i [!INCLUDE [prod_short](prod_short.md)]. Mange regnskapsstandarder og forskrifter krever at bedrifter registrerer og rapporterer økonomiske transaksjoner basert på datoen de skjedde.

Avhengig av forretningsprosessene kan det hende at disse datoene er de samme. Hvis de er like, kan du angi at [!INCLUDE [prod_short](prod_short.md)] skal oppdatere dokumentdatoen på salgs- og kjøpsdokumenter med datoen du bokførte dem.  
  
Hvis du vil sette dokumentdatoer automatisk til bokføringsdatoer, går du til **Salgsoppsett** og **Kjøpsoppsett** og aktiverer veksleknappen **Knytt dokumentdato til bokføringsdato**.

> [!NOTE]
> Innstillingen påvirker ikke salgs- eller kjøpskladder.