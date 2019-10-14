---
title: Fakturere bestillinger i Business Central | Microsoft-dokumentasjon
description: Finn ut hvordan du kan foreta massefakturering fra Microsoft Bookings i Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: invoicing, bookings
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: 4dd32dee8a670a5774de3b9c4afe8367cc44d0fb
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2019
ms.locfileid: "2302563"
---
# <a name="bulk-invoicing-for-microsoft-bookings-in-included365finincludesd365fin_mdmd"></a>Massefakturering for Microsoft Bookings i [!INCLUDE[d365fin](includes/d365fin_md.md)]
Hvis selskapet ditt bruker Bookings-appen i Office 365, kan du foreta massefakturering for avtaler. Siden **Ufakturerte Bookings** i [!INCLUDE[d365fin](includes/d365fin_md.md)] gir en oversikt over selskapets fullførte bestillinger. På denne siden kan du raskt velge avtalene du vil fakturere, og opprette fakturakladder for de leverte tjenestene.  

## <a name="connect-to-bookings"></a>Koble til Bookings
For å kunne koble [!INCLUDE[d365fin](includes/d365fin_md.md)] til Bookings må du angi Bookings-firmaet, hva som skal synkroniseres med Bookings, hvor ofte du vil synkronisere, og hvilke maler som skal brukes. Du definerer denne informasjonen på siden **Oppsett for synkronisering av Bookings**, som du kan åpne fra siden **Konfigurasjon av Exchange-synkronisering**, som du finner via [Søk](ui-search.md).  

Hvis du for eksempel vil synkronisere kunder mellom Bookings og [!INCLUDE[d365fin](includes/d365fin_md.md)], må du angi standardmalen som skal brukes til å legge til nye kunder i [!INCLUDE[d365fin](includes/d365fin_md.md)], basert på kundene i Bookings-firmaet ditt.  

> [!NOTE]
> Bookings-appen er utformet for å legge inn avtaler for enkeltkunder i stedet for selskaper. Synkroniseringen med [!INCLUDE[d365fin](includes/d365fin_md.md)] vil derfor bare synkronisere kundekontakter av typen "Person". En e-postadresse kreves også for at kontakten skal synkroniseres.  

På samme måte, hvis du for eksempel vil synkronisere servicevarer mellom Bookings og [!INCLUDE[d365fin](includes/d365fin_md.md)], må du angi standardmalen som skal brukes til å legge til nye servicevarer i [!INCLUDE[d365fin](includes/d365fin_md.md)], basert på tjenestene i Bookings-firmaet ditt.  

> [!NOTE]
> Bare elementer av typen *Tjeneste* synkroniseres mellom Bookings og [!INCLUDE[d365fin](includes/d365fin_md.md)]. Malen du konfigurerer på siden **Konfigurasjonsmaler** slik at den kan brukes for varesynkroniseringen, må defineres som *Tjeneste*.

## <a name="invoice-appointments"></a>Fakturaavtaler
Når tiden er inne for å sende fakturaer for de fullførte bestillingene, går du til siden **Ufakturerte Bookings**. Listen er lang eller kort avhengig av hvor ofte informasjonen synkroniseres. Du kan opprette fakturaer for alle bestillingene i listen eller én bestilling om gangen. Du kan velge én eller flere poster i listen og fakturere bare disse.  

Støtten for fakturering av avtaler fra Bookings er enklere enn den mer fullstendige arbeidsflyten der du arbeider med tilbud, ordrer og salgsfakturaer. Hvis du vil ha mer informasjon, kan du se [Fakturere salg](sales-how-invoice-sales.md). Du kan velge å selge tjenestene ved å bruke [!INCLUDE[d365fin](includes/d365fin_md.md)] eller velge å bruke Bookings, avhengig av forretningsbehovene dine.  

## <a name="see-also"></a>Se også
[Finans](finance.md)  
[Fakturere salg](sales-how-invoice-sales.md)  
[Sette opp salg](sales-setup-sales.md)  
[Microsoft Bookings](https://products.office.com/en-us/business/scheduling-and-booking-app)  
