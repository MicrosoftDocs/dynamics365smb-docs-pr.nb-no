---
title: Norsk mva-rapportering [NO]
description: Forbedringer i den norske versjonen av Business Central gjør det mulig for deg å beregne og rapportere mva. til de norske skattemyndighetene.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 737, 738, 10601, 10604
ms.date: 01/25/2022
ms.author: edupont
ms.openlocfilehash: a215c79e822b4c5f146380a3a313228e8269a360
ms.sourcegitcommit: 66c78f6f04bfca6c0794b3299241ed65037b1c08
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/26/2022
ms.locfileid: "8029528"
---
# <a name="norwegian-vat-reporting-in-the-norwegian-version"></a>Norsk mva-rapportering i den norske versjonen

[!INCLUDE[prod_short](../../includes/prod_short.md)] har funksjoner i den norske versjonen som gjør at du kan beregne og rapportere omsetningsoppgaver til de norske skattemyndighetene.  

Dette emnet forklarer de vanlige trinnene du skal følge når du rapporterer norsk mva.  

## <a name="set-up-business-central-to-generate-and-submit-electronic-vat-returns"></a>Konfigurere Business Central for å generere og sende inn elektroniske omsetningsoppgaver

For å kunne sende omsetningsoppgaver til norske skattemyndigheter må en administrator opprette en tilkobling til ID-porten hos Digitaliseringsdirektoratet.  

> [!TIP]
> Vi anbefaler at du alltid bruker [!INCLUDE [prod_short](../../includes/prod_short.md)] i en nettleser til å konfigurere tilkoblingen til ID-porten.

### <a name="register-your-company-with-id-porten"></a>Registrere selskapet i ID-porten
Hvis du vil registrere selskapet i ID-porten, følger du fremgangsmåten i [Samarbeidsportalen](https://samarbeid.digdir.no/id-porten/ta-i-bruk-id-porten/94). Legg merke til følgende informasjon etter at du har registrert deg. Du trenger denne når du bruker den assisterte oppsettsveiledningen til å autorisere [!INCLUDE[prod_short](../../includes/prod_short.md)] for tilgang til ID-porten.

* Gyldige URI-er for omdirigering
* Klient-ID
* Klienthemmelighet

> [!IMPORTANT]
> Det er viktig å lagre klient-ID-en og klienthemmeligheten for integrasjonspunktet trygt.

### <a name="set-up-the-integration-point"></a>Konfigurere integrasjonspunktet
Når du har registrert selskapet i ID-porten, er neste trinn å opprette et integrasjonspunkt i selskapets konto i ID-porten. Hvis du vil ha mer informasjon, kan du se [integrasjonspunkt](https://docs.digdir.no/oidc_index.html).

1. Logg på [Skatteetaten](https://skatteetaten.github.io/mva-meldingen/english/idportenauthentication/).
2. Velg **Integrasjoner** i navigasjonsruten, og velg **Ver 2** under **Produksjon**.
3. Velg **Ny integrasjon** for å legge til et nytt integrasjonspunkt.
4. Fyll ut feltene som beskrevet i tabellen nedenfor.

| Parameternavn (norsk) |  Parameterbeskrivelse | Parameterverdi |
|---|---|---|---|
| Difi-tjeneste | Velg tjenesten som skal tilordnes til de riktige scopene. | Velg **API-klient**. |
| Scopes | API-ene (programmeringsgrensesnitt) / ressursene som integrasjonen har tilgang til. | <p>Velg de følgende scopene:</p><ul><li>**openid**</li><li>**skatteetaten:mvameldinginnsending**</li><li>**skatteetaten:mvameldingvalidering**</li></ul> |
| Kundens org.nr. | Organisasjonsnummeret til tjenesteeieren. | Du trenger ikke å angi en verdi i dette feltet. Den nødvendige verdien angis automatisk når konfigurasjonen av integrasjonspunktet lagres. |
| Integrasjonens identifikator | Den unike identifikatoren for tjenesten. | Du trenger ikke å angi en verdi i dette feltet. Den nødvendige verdien angis automatisk når konfigurasjonen av integrasjonspunktet lagres. |
| Navn på integrasjonen | Navnet på integrasjonen slik det vises i påloggingsvinduet. | Angi **Microsoft Dynamics 365 Finance**. |
| Beskrivelse | En kort beskrivelse av tjenesten (for eksempel «Møteportal for NN kommune»). | Angi **Integrasjon med Microsoft Dynamics 365 Finance**. |
| Tillatte grant types | Et grant representerer brukerens samtykke til å hente et tilgangstoken. Når du velger bestemte grants, gir du samtykke til de tilsvarende metodene for å hente et tilgangstoken. | <p>Velg følgende grant types:</p><ul><li>**authorization_code**</li><li>**refresh_token**</li></ul> |
| Klientautentiseringsmetode | Autentiseringsmetoden for klienten. | Angi **client_secret_post**. |
| Applikasjonstype | Applikasjonen (eller klienttypen) er typen kjøretidsmiljø som klienten kjører under. OAuth2 kapittel 2.1 viser de tilgjengelige alternativene. Valget av klienttype er en sikkerhetsvurdering som kunden foretar. | Velg **web**. |
| Gyldig(e) redirect uri-er | Denne parameteren gjelder bare for integrasjoner for personlig pålogging. Den angir URI-ene som klienten kan gå til etter pålogging. | URI-en er en kombinasjon av basis-URI-en og OAuthLanding.htm. Denne verdien varierer avhengig av om du bruker Business Central Online eller lokalt. Når det gjelder Online, bruker du følgende URI: http://www.businesscentral.dynamics.com/OAuthLanding.htm. Følgende er et eksempel på en URI for lokalt: `http://<hostname>/OAuthLanding.htm`. |
| Gyldig(e) post logout redirect uri-er | Denne parameteren gjelder bare for integrasjoner for personlig pålogging. Den angir URI-ene som klienten kan gå til etter avlogging. | Angi `https://skatteetaten.no`. |
| Frontchannel logout uri | URI-en som leverandøren sender en forespørsel til, ved avlogging som utløses av en annen klient i samme økt. Hvis du ikke angir denne parameteren, er det en risiko for at brukeren forblir logget på tjenesten din etter at vedkommende har logget av ID-porten. | Angi `https://skatteetaten.no`. |
| Frontchannel logout krever sesjons-id | Denne parameteren gjelder bare for integrasjoner for personlig pålogging. Den er et flagg som fastsetter om parameterne for utsteder og økt-ID sendes sammen med **frontchannel_logout_uri**. | La denne avmerkingsboksen være tom. |
| Tilbake-uri | Denne parameteren gjelder bare for integrasjoner for personlig pålogging. Den angir URI-en som brukeren sendes tilbake til når vedkommende avbryter pålogging. | Angi `https://skatteetaten.no`. |
| Authorization levetid (sekunder) | Levetiden til den registrerte autorisasjonen. I en OpenID Connect-kontekst blir denne autorisasjonen tilgang til «userinfo»-endepunktet. Verdien må angis i sekunder. | Angi **31536000** (= ett år). |
| Access token levetid (sekunder) | Levetiden til det utstedte **access_token** i sekunder. | Angi **7200** (= to timer). |
| Refresh token levetid (sekunder) | Levetiden til det utstedte **refresh_token** i sekunder. | Angi **0** (null). |
| Refresh token type | <ul><li>**Engangs** – Du får et nytt **refresh_token** ved hver oppdatering av **access_token**.</li><li>**Gjenbrukbart** – En oppdatering av **access_token** endrer ikke **refresh_token**.</li></ul> | Angi **Engangs**. |

:::image type="content" source="../../media/nor-vat-return-integration-point.png" alt-text="Innstillinger for integrasjonspunkt for norsk mva":::

### <a name="set-up-electronic-vat-reporting"></a>Konfigurere elektronisk mva-rapportering
For å gjøre det enklere å konfigurere mva-rapportering har [!INCLUDE[prod_short](../../includes/prod_short.md)] den assisterte oppsettsveiledningen **Konfigurer en elektronisk mva-sending**. 

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Assistert oppsett** og velger den relaterte koblingen.
2. Velg **Konfigurer en elektronisk mva-sending** for å starte den assisterte oppsettsveiledningen. Veiledningen hjelper deg med følgende trinn:

* Autoriser [!INCLUDE[prod_short](../../includes/prod_short.md)] for tilkobling til ID-porten.

    På siden **Elektronisk mva-oppsett** angir du **Klient-ID**, **Klienthemmelighet** og **Omdirigerings-URI** fra selskapets registrering i ID-porten. Velg deretter handlingen **Åpne siden for OAuth 2.0-oppsett**. Velg handlingen **Be om autorisasjonskode** på siden **OAuth 2.0-oppsett** for å motta tokenet du må koble til. Dette krever identifikasjonsnummeret, passordet og PIN-koden for en bruker som kan sende inn omsetningsoppgaver. Når du har angitt denne legitimasjonen, velger du **MinID** som den elektroniske ID-en.
* Kontroller at du bruker det riktige organisasjonsnummer for selskapet.

    Du får en melding om å åpne siden Selskapsopplysninger, der du kan dobbeltsjekke organisasjonsnummeret for oppsettet.
* Oppdater satsene for mva-kodene som må rapporteres.

    [!INCLUDE[prod_short](../../includes/prod_short.md)] har 32 mva-koder, men noen mva-koder trenger du ikke å rapportere mva for. Du kan oppdatere satsene for mva-koder automatisk. Mva-koder kan dessuten variere, for eksempel for ulike bransjer eller virksomhetstyper. På siden **Mva-koder** kan du bruke handlingen **Rediger oversikt** og deretter tilordne eller fjerne kodene og satsene som er relevante for virksomheten. 
  
    > [!NOTE]
    > Oppdateringen tilordner satsene som var gyldige i desember 2021. Du har ansvaret for å sikre at disse satsene fortsatt er gyldige.

* Definer mva-bokføringsoppsettet for å sikre at mva-beløp bokføres på de riktige kontiene. Hvis du vil ha mer informasjon, kan du se [Definer beregninger og bokføringsmetoder for merverdiavgift](../../finance-setup-vat.md).
* Opprett en mva-oppgave for å tilordne mva-bokføringsgruppen for firma til mva-bokføringsgruppen for vare. 

    Tilordningen bestemmer hvordan du bokfører og sporer mva i [!INCLUDE[prod_short](../../includes/prod_short.md)]. Du kan tilordne mva-kodene til bruk for salg og kjøp.

> [!NOTE]
> I tillegg til innstillingene som er beskrevet ovenfor, oppretter vi automatisk en mva-rapportkonfigurasjon for å sende oppgaver og få svar. Du kan vise konfigurasjonen på siden **Konfigurasjon av mva-rapporter**.

## <a name="create-and-submit-a-vat-return"></a>Opprette og sende en omsetningsoppgave
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Omsetningsoppgaver**, og velg deretter den relaterte koblingen.
2. Velg **Ny**.
3. I **Versjon**-feltet velger du **Elektronisk mva**.
4. Valgfritt: Angi et betalingsidentifikasjonsnummer i **KID**-feltet.
5. Velg **Foreslå linjer** for å åpne siden **Forespørselsside for mva-rapport**, der du angir kriterier for generering av linjer for rapporten.
6. Når du har angitt kriteriene, velger du **OK**.  
7. På siden **Mva-oppgjør** velger du **Frigi**. Dette validerer at informasjonen kan sendes til de norske skattemyndighetene.
8. Hvis du vil sende omsetningsoppgaven, velger du **Send**. Statusen for omsetningsoppgaven endres til **Sendt**.
9. Hvis du vil se om skattemyndighetene har godtatt innsendingen, velger du **Motta svar**.

   > [!NOTE]
   > Svaret fra skattemyndighetene blir ikke tilgjengelig med en gang.  

## <a name="troubleshoot-your-connection-to-id-porten"></a>Feilsøke tilkoblingen til ID-porten
Hvis du ikke får noe svar etter at du har sendt inn oppgaven, for eksempel innen 24 timer, kan du kontakte ID-porten og be dem om bekrefte at de har mottatt oppgaven din. Hvis du vil hjelpe dem å identifisere oppgaven, kan du sende verdien fra feltet Meldings-ID. Feltet er skjult som standard, men du kan bruke sideinspeksjon til å hente verdien. Hvis du vil ha mer informasjon, kan du se [Kontrollere sider i Business Central](../../across-inspect-page.md). 

Du kan også sende en kopi av XML-filene for innsendingen din og svaret du mottok. Du kan hente filene ved å velge handlingene **Last ned sendingsmelding** og **Last ned svarmelding** på siden **Omsetningsoppgave**.  

## <a name="close-vat-periods"></a><a name="vat-periods"></a>Avslutt mva-perioder

Hvis du vil innrette etter juridiske krav, skal mva-perioder lukkes etter at du har utlignet. Vanligvis består et regnskapsår av seks mva-perioder, nummerert fra 1 til 6. Når mva. utlignes, lukkes perioden for ytterligere bokføring.  

> [!TIP]
> Ikke alle organisasjoner bruker standard seks mva-perioder. Hvilke perioder den gjeldende organisasjonen bruker, er definert på siden **Mva-periode**.

Du kan vise informasjon om utlignede perioder på siden **Utlignet mva-periode**. De lukkede periodene opprettes med rapporten **Beregn og bokfør mva-oppgjør** når du bokfører mva. Hvis du vil bokføre i den lukkede mva-perioden, kan du åpne perioden på nytt ved å fjerne merket i feltet **Lukket**.  

## <a name="tradesettlement-report"></a>Rapport for omsetningsoppgave

Før januar 2022 brukte du rapporten **Omsetningsoppgave** til å rapportere mva. Denne rapporten er ikke lenger beskrevet i denne artikkelen, men du kan lese om den i [Dynamics NAV 2018-dokumentasjonen](/previous-versions/dynamicsnav-2016/dn283106(v=nav.90)).  

## <a name="see-also"></a>Se også

[Norske mva-koder](norwegian-vat-codes.md)  
[Forholdsmessig MVA](proportional-vat.md)  
[Funksjonalitet som er spesifikk for norske brukere](norway-local-functionality.md)  
[Arbeid med mva. på kjøp og salg](../../finance-work-with-vat.md)  
[Definer beregninger og bokføringsmetoder for merverdiavgift](../../finance-setup-vat.md)  
[Utvidelsen for mva-gruppestyring](../../ui-extensions-vat-group.md)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
