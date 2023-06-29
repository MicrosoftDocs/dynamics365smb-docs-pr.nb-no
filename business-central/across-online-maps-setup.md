---
title: Konfigurer Online Maps
description: Lær hvordan du konfigurerer Business Central til å tilby instruksjoner og stedsinformasjon med en nettbasert karttjeneste.
author: rubenseishima
ms.service: dynamics365-business-central
ms.topic: article
ms.search.form: '800, 804'
ms.date: 07/15/2022
ms.author: a-reishima
---
# <a name="set-up-online-maps"></a><a name="set-up-online-maps"></a>Konfigurer Online Maps

Når du planlegger å besøke en adressen lagret på et kort, for eksempel en kunde, kan du anskaffe et kart fra en nettjeneste med veianvisninger beskrevet på ønsket språk. Hvis du vil være sikker på at denne nettbaserte karttjenesten finner riktig kart og veianvisninger, må du konfigurere den i [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="set-up-the-online-map-feature"></a><a name="set-up-the-online-map-feature"></a>Konfigurer Online Map-funksjonen

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Online Map-oppsett** og velger den relaterte koblingen.
2. På siden **Online Map-oppsett** må du fylle ut feltene. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]
3. Aktiver **Aktivert**-bryteren.

### <a name="customize-the-online-map-provider-features"></a><a name="customize-the-online-map-provider-features"></a>Tilpass funksjonene for leverandøren av Online Map

Hvis du vil tilpasse Online Map-funksjonen mer enn alternativene oppført på siden **Online Map-oppsett** eller bruke en annen kartleverandør, følger du denne fremgangsmåten:

1. På siden **Online Map-oppsett** velger du handlingen **Parameteroppsett**.
2. På siden **Online Map-parameteroppsett** velger du handlingen **Ny**.
3. Fyll ut feltene for å tilpasse hvordan [!INCLUDE[prod_short](includes/prod_short.md)] vil generere nettadressene for de tilgjengelige tjenestene. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]
   * Se i listen over **erstatningsparametere for Online Map** i **faktaboksen** for dataene som er tilgjengelige for å generere nettadresser.

## <a name="see-also"></a><a name="see-also"></a>Se også

[Bruk Online Maps til å finne plasseringer og veibeskrivelser](across-online-maps.md)  
[Bli klar til å gjøre forretninger](ui-get-ready-business.md)  
[Administrasjon](admin-setup-and-administration.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
