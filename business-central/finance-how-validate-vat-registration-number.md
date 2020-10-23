---
title: Validere et organisasjonsnummer | Microsoft-dokumenter
description: Validere et organisasjonsnummer
author: andregu
ms.service: dynamics365-business-central
ms.topic: article
ms.reviewer: edupont
ms.search.keywords: VAT, posting, tax, value-added tax
ms.date: 10/01/2020
ms.author: andregu
ms.openlocfilehash: 130449368e5b96e3c9e6cb6274dcd6e06f568114
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3916979"
---
# <a name="validate-a-vat-registration-number"></a>Validere et organisasjonsnummer

Det er viktig at organisasjonsnumrene du har for kunder, leverandører og kontakter, er gyldige. For eksempel selskaper noen ganger endre status for mva-ansvar, og i noen land kan skattemyndighetene ber deg om å gi rapporter, for eksempel rapporten EU-salgslisten som listen mva registreringsnumre du bruker når du gjør forretninger.

EU-kommisjonen gir tjenesten EU-mva-nummer validering på webområdet sitt, som er felles og gratis. [!INCLUDE[d365fin](includes/d365fin_md.md)] kan spare deg for et trinn, og du kan bruke tjenesten VIES til å validere og spore mva-numre for kunder, leverandører og kontakter direkte fra kunde-, leverandør- og kontaktkort. Tjenesten i [!INCLUDE[d365fin](includes/d365fin_md.md)] kalles **Tjeneste for validering av EU-organisasjonsnr.**. Tjenesten er tilgjengelig på siden **Tjenestetilkoblinger**, og du kan begynne å bruke den med en gang. Tjenestetilkoblingen er gratis, og registrering er ikke nødvendig.

## <a name="to-verify-vat-registration-numbers"></a>Slik bekrefter du organisasjonsnumre

For å aktivere **Tjeneste for validering av EU-organisasjonsnr.** åpner du oppføringen på siden **Tjenestetilkobling**. Feltet **Endepunkt for tjeneste** skal allerede være utfylt. Hvis ikke kan du bruke handlingen **Angi standard endepunkt**. Deretter angir du **Aktivert**-feltet og kan gå videre.

> [!NOTE]
> Aktivere EU-organisasjonsnr. Valideringstjeneste, du må ha administratortilgang.

Når du bruker tjenestetilkoblingen vår, registrerer vi en logg over mva-numre og bekreftelser for hver kunde, leverandør eller kontakt i **Organisasjonsnummerlogg**, så du kan enkelt spore dem. Loggen er spesifikk for hver kunde. Loggen er for eksempel nyttig for å bevise at du har bekreftet at gjeldende mva-nummeret er riktig. Når du godkjenner et mva-nummer, gjenspeiler kolonnen **ID for forespørsel** i loggen at du har gjort noe.

Du kan vise loggen mva-registrering på kortene for kunde, leverandør eller kontakt på den **fakturering** hurtigfanen, ved å velge oppslagsknappen i feltet **Organisasjonsnr.**  

Tjenesten kan også spare deg tid når du oppretter en kunde eller leverandør. Hvis du vet organisasjonsnummeret til kunden, kan du angi den i feltet **Organisasjonsnr.** på kortene for kunden eller leverandøren og vi skal fylle ut kundenavnet for deg. Noen land gir også firmaadresser i et strukturert format. I disse landene fyller vi ut adressen også.  

Det er et par ting å merke seg når det gjelder EU-mva-nummer validering-tjenesten:

* Denne webtjenesten bruker HTTP-protokollen, som betyr at data som overføres via tjenesten, ikke er kryptert.  
* Du kan oppleve nedetid for denne tjenesten som Microsoft ikke er ansvarlig. Tjenesten er en del av en omfattende EU-nettverk av nasjonale mva-registre.

> [!IMPORTANT]
> Det er ditt ansvar å kontrollere at dataene er gyldige. Av og til returneres dataene med feil av EU-mva-nummervalideringstjenesten. Hvis valideringen mislykkes, validerer du organisasjonsnummer på [webområdet ](https://ec.europa.eu/taxation_customs/vies/), skriver ut resultatet eller lagrer det på en delt plassering, og deretter legger du til koblingen til posten for kunden, leverandøren eller kontakten. Se [Behandle vedlegg, koblinger og merknader på kort og dokumenter](ui-how-add-link-to-record.md) hvis du vil ha mer informasjon.

## <a name="see-also"></a>Se også

[Definere merverdiavgift (mva)](finance-setup-vat.md)  
[Definere urealisert merverdiavgift](finance-setup-unrealized-vat.md)  
[Rapportere mva til skattemyndighetene](finance-how-report-vat.md)  
[Arbeide med mva på kjøp og salg](finance-work-with-vat.md)  
[Lokal funksjonalitet i Business Central](about-localization.md)  
