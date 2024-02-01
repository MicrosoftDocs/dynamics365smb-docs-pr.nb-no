---
title: Standard gjentakende kjøpslinjer
description: Definere ofte brukte kjøpslinjer for å sette dem inn i kjøpsdokumenter og fylle ut linjene raskt med standardinformasjon.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'trade, purchase, replenishment'
ms.search.form: 177
ms.date: 07/06/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Opprett gjentakende kjøpslinjer

Hvis du ofte må opprette kjøpslinjer med lignende informasjon, kan du definere standardlinjer du deretter kan sette inn på gjentakende kjøpsdokumenter, for eksempel for gjentakende etterfyllingsordrer.

## Konfigurer gjentakende kjøpslinjer

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Gjentakende kjøpslinjer**, og velg deretter den relaterte koblingen.
2. På siden **Gjentakende kjøpslinjer** velger du handlingen **Ny**.
3. Fyll ut feltene i hurtigfanen **Generelt** etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. I hurtigfanen **Linjer** angir du informasjonen i feltene som gjenspeiler standardlinjene du forventer å bruke som gjentakende linjer i kjøpsdokumenter.

> [!NOTE]
> Du kan ikke definere priser på gjentakende kjøpslinjer, fordi priser, rabatter og så videre. beregnes på de faktiske salgsdokumentene etter at du setter inn de gjentakende kjøpslinjene.

[!INCLUDE [line-no-info](includes/line-no-info.md)]

## Tildel gjentakende kjøpslinjer til en leverandør

Tilordne én eller flere gjentakende kjøpslinjer til en leverandør, slik at de kan settes inn i kjøpsdokumenter fra leverandøren.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Leverandører** og velger den relaterte koblingen.
2. Åpne kortet for den aktuelle leverandøren.
3. Velg handlingen **Gjentakende kjøpslinjer**.
4. På siden **Gjentakende kjøpslinjer** velger du kodene for de gjentakende kjøpslinjene som du vil sette inn i kjøpsdokumenter for leverandøren.
5. Fyll ut de andre feltene for å definere når, hvordan og hvor de gjentakende kjøpslinjene skal brukes.
6. I de fire feltene der du velger hvordan linjene settes inn på hver dokumenttype, kan du velge ett av følgende alternativer:

|Alternativ|Description|
|------|-----------|
|**Manuell**|Du må manuelt slå opp og sette inn en gjentakende kjøpslinje for leverandøren.|
|**Automatisk**|Hvis det finnes flere gjentakende kjøpslinjer for leverandøren, får du melding om hvor du kan velge en som kan settes inn. Hvis det bare finnes én gjentakende kjøpslinje, settes den inn automatisk.<br /><br />Dette bare fungerer hvis det nye dokumentet ble opprettet fra en dokumentliste, for eksempel ved å velge **Ny**-handlingen på **Bestillinger**-siden. Den fungerer imidlertid ikke hvis dokumentet ble opprettet fra for eksempel et leverandørkort.|
|**Be alltid om bekreftelse**|Det vises en melding, og alle gjentakende kjøpslinjer vises slik at du kan velge én.

## Sett inn gjentakende kjøpslinjer på en kjøpsfaktura

Hvis det finnes gjentakende kjøpslinjer for leverandøren, kan du legge dem til automatisk på alle typer kjøpsdokumenter, for eksempel en kjøpsfaktura. Hvis du har aktivert alternativene for **Be alltid om bekreftelse** mens du tildeler gjentakende kjøpslinjer til leverandører, blir du informert om det finnes gjentakende kjøpslinjer.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Kjøpsfakturaer**, og velg deretter den relaterte koblingen.
2. Åpne kjøpsfakturaen du vil sette inn én eller flere standard kjøpslinjer på.
3. Velg handlingen **Hent gjentakende kjøpslinjer**.
4. På siden **Gjentakende kjøpslinjer** velger du oppslagsknappen i **Kode**-feltet, og deretter velger du et sett med standard kjøpslinjer.
5. Velg **OK** for å sette inn de standard kjøpslinjene på fakturaen, der du kan bruke informasjonen på nytt som den er eller redigere den.

## Se også

[Innkjøp](purchasing-manage-purchasing.md)  
[Definer kjøp](purchasing-setup-purchasing.md)  
[Opprett gjentakende salg](sales-how-work-standard-lines.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]