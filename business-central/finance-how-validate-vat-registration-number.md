---
title: Valider organisasjonsnumre
description: 'La Business Central validere organisasjonsnumre for kontaktene, kundene og leverandørene, basert på EU-tjenesten VIES VAT Number Validation.'
author: andregu
ms.topic: conceptual
ms.reviewer: edupont
ms.search.keywords: 'VAT, posting, tax, value-added tax'
ms.search.form: '249, 575, 1279'
ms.date: 06/16/2021
ms.author: andregu
---

# <a name="validate-vat-registration-numbers"></a>Valider organisasjonsnumre

Det er viktig at organisasjonsnumrene du har for kunder, leverandører og kontakter, er gyldige hvis du bruker [!INCLUDE [prod_short](includes/prod_short.md)] i et land som bruker merverdiavgift. For eksempel selskaper noen ganger endre status for mva-ansvar, og i noen land kan skattemyndighetene ber deg om å gi rapporter, for eksempel rapporten **EU-salgsliste** som viser mva registreringsnumrene du bruker når du gjør forretninger.

EU-kommisjonen gir tjenesten EU-mva-nummer validering på webområdet sitt, som er felles og gratis. [!INCLUDE [prod_short](includes/prod_short.md)] kan spare deg for et trinn, og du kan bruke tjenesten VIES til å validere og spore mva-numre og annen bedriftsinformasjon for kunder, leverandører og kontakter. Tjenesten i [!INCLUDE [prod_short](includes/prod_short.md)] kalles **Tjeneste for validering av EU-organisasjonsnr.**. Tjenesten er tilgjengelig på siden **Tjenestetilkoblinger**, og du kan begynne å bruke den med en gang. Tjenestetilkoblingen er gratis, og ekstra registrering er ikke nødvendig.

## <a name="configure-the-service-to-verify-vat-registration-numbers-automatically"></a>Konfigurer tjenesten til å bekrefte mva-registreringsnummer automatisk

For å aktivere **Tjeneste for validering av EU-organisasjonsnr.** åpner du oppføringen på siden **Tjenestetilkobling**. Hvis feltet **Endepunkt for tjeneste** ikke allerede er utfylt, bruker du handlingen **Angi standard endepunkt**. Deretter angir du **Aktivert**-feltet og kan gå videre.  

> [!IMPORTANT]
> For å aktivere valideringstjenesten må du ha administratortilgang.

Du kan eventuelt definere maler for typene mva-relaterte data som du vil at tjenesten også skal kontrollere. Se delen [Valideringsmaler](#validation-templates) hvis du vil ha mer informasjon.

Når du bruker tjenestetilkoblingen vår, registrerer vi en logg over mva-numre og bekreftelser for hver kunde, leverandør eller kontakt i **Organisasjonsnummerlogg**, så du kan enkelt spore dem. Loggen er spesifikk for hver kunde. Loggen er for eksempel nyttig for å bevise at du har bekreftet at gjeldende mva-nummeret er riktig. Når du godkjenner et mva-nummer, gjenspeiler kolonnen **ID for forespørsel** i loggen at du har gjort noe.

Du kan vise loggen mva-registrering på kortene for kunde, leverandør eller kontakt på den **fakturering** hurtigfanen, ved å velge oppslagsknappen i feltet **Organisasjonsnr.**  

Det er et par ting å merke seg når det gjelder EU-mva-nummer validering-tjenesten:

* Denne webtjenesten bruker HTTP-protokollen, som betyr at data som overføres via tjenesten, ikke er kryptert.  
* Du kan oppleve nedetid for denne tjenesten som Microsoft ikke er ansvarlig. Tjenesten er en del av en omfattende EU-nettverk av nasjonale mva-registre.

> [!IMPORTANT]
> Det er ditt ansvar å kontrollere at dataene er gyldige. Av og til returneres dataene med feil av EU-mva-nummervalideringstjenesten. Hvis valideringen mislykkes, validerer du organisasjonsnummer på [webområdet ](https://ec.europa.eu/taxation_customs/vies/), skriver ut resultatet eller lagrer det på en delt plassering, og deretter legger du til koblingen til posten for kunden, leverandøren eller kontakten. Se [Behandle vedlegg, koblinger og merknader på kort og dokumenter](ui-how-add-link-to-record.md) hvis du vil ha mer informasjon.

## <a name="validation-templates"></a>Valideringsmaler

Du kan bruke VIES-tjenesten til også å kontrollere annen firmainformasjon, for eksempel adressen, i tillegg til organisasjonsnummeret. På siden **Maler for validering av mva-organisasjonsnummer** oppretter du en oppføring for hvert land du vil ha ytterligere validering for, og angir deretter informasjonen du vil skal bekreftes automatisk.  

Du kan for eksempel legge til en post for Spania, der du vil ha validering for navn, gate, by og postnummer, og deretter en annen post for Tyskland der du for eksempel vil ha validering for post nummer. Deretter angir du standardmalen på siden **Oppsett av tjeneste for validering av EU-organisasjonsnr.**.  

> [!NOTE]
> Sørg alltid for at standardmalen fungerer for dine behov. Du kan endre standarden slik at den samsvarer med dine behov, for eksempel få validering for alle felt eller ingen felt.

Neste gang du angir et organisasjonsnummer, validerer tjenesten nummeret og eventuelle tilleggsopplysninger som er angitt i valideringsmalene. Hvis de angitte verdiene er forskjellige fra verdiene som returneres av tjenesten, vil du se detaljene på siden **Valideringsdetaljer**, der du kan godta eller tilbakestille verdiene.  

## <a name="see-also"></a>Se også

[Definere merverdiavgift (mva)](finance-setup-vat.md)  
[Definere urealisert merverdiavgift](finance-setup-unrealized-vat.md)  
[Rapportere mva til skattemyndighetene](finance-how-report-vat.md)  
[Arbeide med mva på kjøp og salg](finance-work-with-vat.md)  
[Lokal funksjonalitet i Business Central](about-localization.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
