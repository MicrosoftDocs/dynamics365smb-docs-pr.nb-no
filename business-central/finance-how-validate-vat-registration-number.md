---
title: Validere et organisasjonsnummer | Microsoft-dokumenter
description: Validere et organisasjonsnummer
author: andregu
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, posting, tax, value-added tax
ms.date: 04/01/2020
ms.author: andregu
ms.openlocfilehash: 4b282d8819851fd6529f901f44a39777a8b8e74c
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3183071"
---
# <a name="validate-a-vat-registration-number"></a>Validere et organisasjonsnummer

## <a name="to-verify-vat-registration-numbers"></a>Slik bekrefter du organisasjonsnumre
Det er viktig at organisasjonsnumrene du har for kunder, leverandører og kontakter, er gyldige. For eksempel selskaper noen ganger endre status for mva-ansvar, og i noen land kan skattemyndighetene ber deg om å gi rapporter, for eksempel rapporten EU-salgslisten som listen mva registreringsnumre du bruker når du gjør forretninger.

EU-kommisjonen gir tjenesten EU-mva-nummer validering på webområdet sitt, som er felles og gratis. [!INCLUDE[d365fin](includes/d365fin_md.md)] kan spare deg for et trinn, og du kan bruke tjenesten VIES til å validere og spore mva-numre for kunder, leverandører og kontakter direkte fra kunde-, leverandør- og kontaktkort. Tjenesten i [!INCLUDE[d365fin](includes/d365fin_md.md)] kalles **Tjeneste for validering av EU-organisasjonsnr.**. Tjenesten er tilgjengelig på siden **Tjenestetilkoblinger**, og du kan begynne å bruke den med en gang. Tjenestetilkoblingen er gratis, og registrering er ikke nødvendig.

For å aktivere **Tjeneste for validering av EU-organisasjonsnr.** åpner du oppføringen på siden **Tjenestetilkobling**. Feltet **Endepunkt for tjeneste** skal allerede være utfylt. Hvis ikke kan du bruke handlingen **Angi standard endepunkt**. Deretter angir du **Aktivert**-feltet og kan gå videre.

> [!Note]
> Aktivere EU-organisasjonsnr. Valideringstjeneste, du må ha administratortilgang.

Når du bruker tjenestetilkoblingen vår, registrerer vi en logg over mva-numre og bekreftelser for hver kunde, leverandør eller kontakt i **Organisasjonsnummerlogg**, så du kan enkelt spore dem. Loggen er spesifikk for hver kunde. Loggen er for eksempel nyttig for å bevise at du har bekreftet at gjeldende mva-nummeret er riktig. Når du godkjenner et mva-nummer, gjenspeiler kolonnen **ID for forespørsel** i loggen at du har gjort noe.

Du kan vise loggen mva-registrering på kortene for kunde, leverandør eller kontakt på den **fakturering** hurtigfanen, ved å velge oppslagsknappen i feltet **Organisasjonsnr.**  

Tjenesten kan også spare deg tid når du oppretter en kunde eller leverandør. Hvis du vet organisasjonsnummeret til kunden, kan du angi den i feltet **Organisasjonsnr.** på kortene for kunden eller leverandøren og vi skal fylle ut kundenavnet for deg. Noen land gir også firmaadresser i et strukturert format. I disse landene fyller vi ut adressen også.  

Det er et par ting å merke seg når det gjelder EU-mva-nummer validering-tjenesten:

* Denne webtjenesten bruker HTTP-protokollen, som betyr at data som overføres via tjenesten, ikke er kryptert.  
* Du kan oppleve nedetid for denne tjenesten som Microsoft ikke er ansvarlig. Tjenesten er en del av en omfattende EU-nettverk av nasjonale mva-registre.

## <a name="see-also"></a>Se også  
[Definere merverdiavgift (mva)](finance-setup-vat.md)  
[Definere urealisert merverdiavgift](finance-setup-unrealized-vat.md)      
[Rapportere mva til skattemyndighetene](finance-how-report-vat.md)  
[Arbeide med mva på kjøp og salg](finance-work-with-vat.md)  
[Lokal funksjonalitet i Business Central](about-localization.md)
