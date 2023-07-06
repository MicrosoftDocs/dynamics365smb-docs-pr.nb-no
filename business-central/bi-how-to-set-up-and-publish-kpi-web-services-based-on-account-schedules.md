---
title: Konfigurere og publisere KPI-webtjenester basert på finansrapporter
description: Denne artikkelen beskriver hvordan du viser finansrapporten KPI-data som er basert på finansrapporter.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 12/16/2022
ms.custom: bap-template
ms.search.form: '103, 104, 108, 195, 196, 197, 198, 489, 490, 764, 765, 766'
---
# <a name="set-up-and-publish-kpi-web-services-based-on-financial-reports"></a><a name="set-up-and-publish-kpi-web-services-based-on-financial-reports"></a><a name="set-up-and-publish-kpi-web-services-based-on-financial-reports"></a>Konfigurere og publisere KPI-webtjenester basert på finansrapporter

På siden **Oppsett av KPI-webtjeneste for finansrapport** definerer du hvordan du vil vise finansrapportens KPI-data og hvilke bestemte finansrapporter KPI-ene skal baseres på. Når du velger **Publiser webtjeneste**, legges finansrapportens angitte KPI-data til i listen over publiserte webtjenester i vinduet over publiserte webtjenester på siden **Webtjenester**.

> [!NOTE]
> Når du bruker denne nettjenesten, tas ikke avslutningsdatoer med i datasettet. Du kan bruke filtre i Power BI til å analysere ulike tidsperioder.

## <a name="set-up-and-publish-a-kpi-web-service-based-on-financial-reports"></a><a name="set-up-and-publish-a-kpi-web-service-based-on-financial-reports"></a><a name="set-up-and-publish-a-kpi-web-service-based-on-financial-reports"></a>Konfigurere og publisere KPI-webtjenester basert på finansrapporter
  
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Oppsett av KPI-nettjeneste for finansrapporter**, og velg deretter den relaterte koblingen.
2. Fyll ut feltene på hurtigfanen **Generelt**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Fyll ut feltene på hurtigfanen **Raddimensjoner**.
4. Gjenta trinn 3 for alle finansrapportene som du vil basere webtjenesten for finansrapporter-KPI på.  
5. Hvis du vil vise eller redigere den valgte finansrapporten, velger du hurtigfanen **Raddefinisjoner** og deretter handlingen **Rediger raddefinisjon**.
6. Hvis du vil vise finansrapport-KPI-data som du har definert, velger du **KPI-webtjeneste for finansrapport**.
7. Hvis du vil publisere KPI-webtjenesten for finansrapporten, velger du **Publiserer webtjeneste**.

Du kan nå opprette finansrapporter i Power BI basert på nettjenesten, eller tjenester, som du har opprettet.

> [!NOTE]  
> Du kan også publisere KPI-webtjenesten ved å velge sideobjektet **Oppsett av KPI-webtjeneste for finansrapport** fra **Webtjenester**-siden. Lære mer om [publisering av en webtjeneste](across-how-publish-web-service.md).

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se også

[Finansforretningsanalyse](bi.md)  
[Finans](finance.md)  
[Konfigurere finans](finance-setup-finance.md)  
[Finans og kontoplanen](finance-general-ledger.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
