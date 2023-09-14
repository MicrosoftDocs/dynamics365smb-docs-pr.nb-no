---
title: Fakturere bestillinger i Business Central
description: Dette emnet forklarer hvordan du kan utføre massefakturering fra Microsoft Bookings i Business Central.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'invoicing, bookings'
ms.search.form: '1638, 6702, 6704'
ms.date: 05/20/2022
ms.author: bholtorf
---
# <a name="bulk-invoicing-for-microsoft-bookings-in-"></a>Massefakturering for Microsoft Bookings i [!INCLUDE[prod_short](includes/prod_short.md)]

Hvis selskapet ditt bruker Bookings-appen i Microsoft 365, kan du foreta massefakturering for avtaler. Siden **Bestillinger som ikke er fakturert** i [!INCLUDE[prod_short](includes/prod_short.md)] gir en oversikt over selskapets fullførte bestillinger. På denne siden kan du raskt velge avtalene du vil fakturere, og opprette fakturakladder for de leverte tjenestene.  

## <a name="connect-to-bookings"></a>Koble til Bookings

For å kunne koble [!INCLUDE[prod_short](includes/prod_short.md)] til Bookings må du angi Bookings-firmaet, hva som skal synkroniseres med Bookings, hvor ofte du vil synkronisere, og hvilke maler som skal brukes. Du definerer denne informasjonen på siden **Oppsett for synkronisering av Bookings**, som du kan åpne fra siden **Konfigurasjon av Exchange-synkronisering**, som du finner via [Søk](ui-search.md).  

Hvis du for eksempel vil synkronisere kunder mellom Bookings og [!INCLUDE[prod_short](includes/prod_short.md)], må du angi standardmalen som skal brukes til å legge til nye kunder i [!INCLUDE[prod_short](includes/prod_short.md)], basert på kundene i Bookings-firmaet ditt.  

> [!NOTE]
> Bookings-appen er utformet for å legge inn avtaler for enkeltkunder i stedet for selskaper. Synkroniseringen med [!INCLUDE[prod_short](includes/prod_short.md)] vil derfor bare synkronisere kundekontakter av typen *Person*. En e-postadresse kreves også for at kontakten skal synkroniseres.  

På samme måte, hvis du for eksempel vil synkronisere servicevarer mellom Bookings og [!INCLUDE[prod_short](includes/prod_short.md)], må du angi standardmalen som skal brukes til å legge til nye servicevarer i [!INCLUDE[prod_short](includes/prod_short.md)], basert på tjenestene i Bookings-firmaet ditt.  

> [!NOTE]
> Bare elementer av typen *Tjeneste* synkroniseres mellom Bookings og [!INCLUDE[prod_short](includes/prod_short.md)]. Malen du konfigurerer på siden **Konfigurasjonsmaler** slik at den kan brukes for varesynkroniseringen, må defineres som *Tjeneste*.

## <a name="invoice-appointments"></a>Fakturaavtaler

Når tiden er inne for å sende fakturaer for de fullførte bestillingene, går du til siden **Bestillinger som ikke er fakturert**. Listen er lang eller kort avhengig av hvor ofte informasjonen synkroniseres. Du kan opprette fakturaer for alle bestillingene i listen eller én bestilling om gangen. Du kan velge én eller flere poster i listen og fakturere bare disse.  

Støtten for fakturering av avtaler fra Bookings er enklere enn den mer fullstendige arbeidsflyten der du arbeider med tilbud, ordrer og salgsfakturaer. Hvis du vil ha mer informasjon, kan du se [Fakturere salg](sales-how-invoice-sales.md). Du kan velge å selge tjenestene ved å bruke [!INCLUDE[prod_short](includes/prod_short.md)] eller velge å bruke Bookings, avhengig av forretningsbehovene dine.  

> [!NOTE]
> I mai kan 2022 oppdaget vi et problem i integrasjonen med bestillinger. For øyeblikket krever synkroniseringen fra Bestillinger til [!INCLUDE [prod_short](includes/prod_short.md)] at du manuelt knytter fakturaene til kunder i [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="see-also"></a>Se også

[Finans](finance.md)  
[Fakturere salg](sales-how-invoice-sales.md)  
[Sette opp salg](sales-setup-sales.md)  
[Microsoft Bookings](https://products.office.com/business/scheduling-and-booking-app)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
