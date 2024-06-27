---
title: Definer en fakturabokføringspolicy for brukere
description: Bruk fakturabokføringspolicyer til å kontrollere om en bruker kan bokføre salgs- og kjøpsfakturaer.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 06/12/2024
ms.custom: bap-template
ms.search.forms: '119, 9807,'
ms.service: dynamics-365-business-central
---

# <a name="define-an-invoice-posting-policy-for-users"></a>Definer en fakturabokføringspolicy for brukere

Selskaper har ofte unike prosesser for bokføring av salgs- og kjøpsfakturaer og leveringer. Prosesser kan for eksempel variere fra én person som bokfører alt i en bestilling, til flere ansatte. Du kan begrense brukere fra å bokføre fakturaer, eller kreve at fakturaer bokføres sammen med leveringer eller mottak.

## <a name="to-specify-a-posting-policy"></a>Slik angir du en bokføringspolicy

På siden **Brukeroppsett** i feltene **Bokføringspolicy for salgsfaktura** og **Bokføringspolicy for kjøpsfaktura**, velger du et av følgende alternativer:

* **Tillatt** (standard) – Behold gjeldende virkemåte, der en bruker kan velge hvilket bokføringsalternativ som skal brukes, for eksempel **Lever**, **Fakturer** og **Lever og fakturer**. 
* **Forbudt** – Hindre brukeren i å bokfører fakturaer. [!INCLUDE [prod_short](includes/prod_short.md)] viser en bekreftelsesdialogboks som bare inneholder alternativene **Lever** og **Motta**.
* **Obligatorisk** – la brukeren bokføre fakturaer sammen med mottak eller leveringer. [!INCLUDE [prod_short](includes/prod_short.md)] viser en bekreftelsesdialog med alternativene **Lever og fakturer** eller **Motta og fakturer**.

## <a name="effect-on-documents"></a>Innvirkning på dokumenter

Tabellen nedenfor beskriver hvordan fakturabokføringspolicyer påvirker dokumenter.

> [!NOTE]
> Når du bokfører salgs- og kjøpsfakturaer og kreditnotaer, har du ingen bokføringsalternativer. Dokumentene bokfører alltid de fysiske og økonomiske transaksjonene sammen. Du kan ikke delvis bokføre fakturaer og kreditnotaer.

|Dokument | Alternativ 1: Tillat <br>Viser en rekke alternativer| Alternativ 2: Forbudt <br>Bekreftelsesdialogboks | Alternativ 3: Obligatorisk <br>Bekreftelsesdialogboks|
|--|--|--|--|
|Ordre |- Lever <br>- Fakturer <br>- Lever og fakturer |Vil du bokføre leveringen? |Vil du bokføre leveringen og fakturaen?|
|Salgfaktura|Ingen alternativer| Bokføring er forbudt per brukeroppsett|Vil du bokføre fakturaen?|
|Salgskreditnota|Ingen alternativer|Bokføring er forbudt per brukeroppsett|Vil du bokføre kreditnotaen?|
|Ordreretur |- Motta <br>- Fakturer <br>- Motta og fakturer |Vil du bokføre mottaket? |Vil du bokføre mottaket og fakturaen?|
|Lagerplukk |- Lever <br>- Lever og fakturer |Vil du bokføre leveringen? |Vil du bokføre leveringen og fakturaen?|
|Bestilling |- Motta <br>- Fakturer <br>- Motta og fakturer |Vil du bokføre mottaket? |Vil du bokføre mottaket og fakturaen?|
|Kjøpsfaktura|Ingen alternativer|Bokføring er forbudt per brukeroppsett|Vil du bokføre fakturaen?|
|Kjøpskreditnota|Ingen alternativer|Bokføring er forbudt per brukeroppsett|Vil du bokføre kreditnotaen?|
|Bestillingsretur |- Lever <br>- Fakturer <br>- Lever og fakturer |Vil du bokføre leveringen? |Vil du bokføre leveringen og fakturaen?|
|Lagerplassering |- Motta <br>- Motta og fakturer |Vil du bokføre mottaket? |Vil du bokføre mottaket og fakturaen?|
|Lagerlevering |- Lever <br>- Lever og fakturer | Vil du bokføre leveringen? |Vil du bokføre leveringen og fakturaen?|

   > [!Note]
   > Innstillingen påvirker ikke bokføring av finanskladdelinjer der du kan velge **Fakturer** i feltet **Dokumenttype**.

## <a name="see-also"></a>Se også

[Fakturere salg](sales-how-invoice-sales.md)  
[Registrere kjøp med kjøpsfakturaer og ordrer](purchasing-how-record-purchases.md)  
[Kjøp varer for et salg ved å opprette kjøpsfakturaer](purchasing-how-purchase-products-sale.md)
[Gjør deg klar til å gjøre forretninger](ui-get-ready-business.md)  
