---
title: Utvidelse for mva-gruppestyring | Microsoft-dokumenter
description: Du kan samarbeide med andre bedrifter for å danne en mva-gruppe, og opptre enten som medlem eller representant for gruppen ved rapportering av mva.
author: bholtorf
manager: annbe
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: VAT, value added tax, report
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 093b361bf2d3f02d08dc6b8d53ad4b58a086f88b
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5771290"
---
# <a name="the-vat-group-management-extension"></a>Utvidelsen for mva-gruppestyring

Du kan knytte sammen ett eller flere selskaper i landet for å konsolidere mva-rapportering under ett enkelt registreringsnummer. Denne typen oppsett kalles en *mva-gruppe*. Du kan samarbeide med gruppen som medlem eller grupperepresentant.

## <a name="forming-a-vat-group"></a>Danne en mva-gruppe
MVA-gruppemedlemmer og grupperepresentanten kan bruke den assisterte oppsettsveiledningen for **Oppsett av mva-gruppestyring** til å definere samarbeidet med gruppen, og opprette en forbindelse mellom deres [!INCLUDE[prod_short](includes/prod_short.md)]-leietakere. Gruppemedlemmene bruker tilkoblingen til å sende omsetningsoppgavene deres til grupperepresentanten. Representanten sender mva til skattemyndighetene på vegne av gruppen med én enkelt omsetningsoppgave. 

## <a name="vat-group-constellations"></a>Mva-gruppekonstellasjoner
Kommunikasjonen skjer fra gruppemedlemmer til representanten. Grupperepresentanten viser en API som gjør at medlemmene kan sende omsetningsoppgaver til mva-grupperepresentanten. 
[!INCLUDE[prod_short](includes/prod_short.md)] støtter sendinger av omsetningsoppgaver internt i gruppen for selskaper som bruker [!INCLUDE[prod_short](includes/prod_short.md)] lokalt eller online, og i en hvilken som helst kombinasjon. Oppsettet av kommunikasjonen avhenger av konstellasjonen. Følgende avsnitt beskriver hvordan du definerer ulike gruppekonstellasjoner.

Følgende oversikt viser den anbefalte rekkefølgen av trinnene for å definere en mva-gruppe:

1. Opprett oppsettet i Azure Active Directory. Hvis du vil ha mer informasjon, kan du se [Krav for godkjenning](ui-extensions-vat-group.md#requirements-for-authentication).
2. Del de tekniske opplysningene som mva-gruppemedlemmer og representanten må ha for å koble sine [!INCLUDE[prod_short](includes/prod_short.md)]-leietakere. Vanligvis har mva-grupperepresentanten denne informasjonen, for eksempel navnet på miljøet for mva-grupperepresentanten som mva-gruppemedlemmene skal sende mva til.
3. Opprett brukere i mva-grupperepresentantens [!INCLUDE[prod_short](includes/prod_short.md)] som mva-gruppemedlemmer kan bruke til å godkjenne og koble til.
4. Kjør assistert oppsettsveiledning for **Konfigurer mva-gruppestyring** for å koble sammen mva-gruppemedlemmene.

  Veiledningen krever noe informasjon fra mva-grupperepresentanten. Se delen [Oppsett av mva-gruppemedlem](#vat-group-member-setup) hvis du vil ha mer informasjon. Merk deg **Gruppemedlems-ID**-en for hvert enkelt medlem i mva-gruppen. Representanten trenger disse ID-ene for å legge til selskapene i mva-gruppen.
5. Definer utvidelsen for mva-gruppestyring i mva-grupperepresentantens [!INCLUDE[prod_short](includes/prod_short.md)] ved hjelp av den assisterte oppsettsveiledningen for **Konfigurer mva-gruppestyring**. 

> [!NOTE]
> For å kunne koble til mva-grupperepresentanten trenger gruppemedlemmer en bruker med tilgang til mva-grupperepresentantens [!INCLUDE[prod_short](includes/prod_short.md)]. MVA-grupperepresentanten må opprette minst én bruker for dette, men av sikkerhetsmessige grunner anbefales det at du oppretter en bruker for hvert enkelt mva-gruppemedlem. Pass på at du distribuerer legitimasjonen for disse brukerne til mva-gruppemedlemmer på en sikker måte.

## <a name="understanding-the-vat-group-management-setup"></a>Forstå oppsettet av mva-gruppestyring

Mva-grupperepresentanten viser en API som mva-gruppemedlemmene kan bruke til å koble seg til sin [!INCLUDE[prod_short](includes/prod_short.md)]-leietaker og sende omsetningsoppgaver. Mva-gruppemedlemmer vil ofte bruke [!INCLUDE[prod_short](includes/prod_short.md)] i separate Azure Active Directory-leietakere. Derfor trengs det mer oppsett for å opprette en forbindelse mellom mva-gruppemedlemmet og -representantens [!INCLUDE[prod_short](includes/prod_short.md)]. 
  
Mva-gruppemedlemmer kobles til representanten ved å ringe en webtjeneste i leieren for mva-grupperepresentanten. Anroperen må godkjennes ved hjelp av OAuth. Når utvidelsen for mva-gruppestyring er definert, blir du bedt om å godkjenne til mva-grupperepresentanten for å få og lagre et tilgangstoken. Dette tilgangstokenet brukes ved sending av omsetningsoppgaver til mva-grupperepresentanten. 

Godkjenning blir håndtert av Azure Active Directory, så oppsettet må gjøres i mva-grupperepresentantens Azure Active Directory for å tillate tilkoblinger. En Azure Active Directory-appregistrering må konfigureres med tilgang til mva-grupperepresentantens [!INCLUDE[prod_short](includes/prod_short.md)]. Dette gjelder også hvis mva-grupperepresentanten bruker [!INCLUDE[prod_short](includes/prod_short.md)] lokalt. I tillegg må du konfigurere enkel pålogging hvis mva-grupperepresentanten bruker [!INCLUDE[prod_short](includes/prod_short.md)] lokalt.

> [!NOTE]
> I en begrenset periode støttes også godkjenning med en tilgangsnøkkel for webtjeneste. Hvis du vil ha mer informasjon, se [Avskrevne funksjoner i 2021 lanseringsbølge 1](/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-w1#deprecated-features-in-2021-release-wave-1).

## <a name="requirements-for-authentication"></a>Krav til godkjenning 
Når mva-grupperepresentanten bruker [!INCLUDE[prod_short](includes/prod_short.md)] online eller lokalt, bruker mva-gruppemedlemmene Azure Active Directory til å godkjenne når de sender omsetningsoppgaver til mva-grupperepresentanten. Hvis medlemmene i mva-gruppen også bruker [!INCLUDE[prod_short](includes/prod_short.md)] online, kan mva-gruppemedlemmet godkjenne ved å bruke den angitte brukerlegitimasjonen og informasjonen om endepunkt. Se [Oppsett av mva-gruppemedlem](ui-extensions-vat-group.md#vat-group-member-setup) hvis du vil ha mer informasjon.

Mva-gruppemedlemmer som har [!INCLUDE[prod_short](includes/prod_short.md)] lokalt, må konfigurere en appregistrering i Azure Active Directory for mva-grupperepresentantens [!INCLUDE[prod_short](includes/prod_short.md)]-leietaker. Appregistreringen gjør at mva-grupperepresentantens [!INCLUDE[prod_short](includes/prod_short.md)] online kan godkjenne gruppemedlemmet. Hvis du vil ha mer informasjon, kan du se [Hurtigstart: Registrere et program i Microsoft Identity Platform](/azure/active-directory/develop/quickstart-register-app).

Når du oppretter appregistreringen i Azure Active Directory, må du angi følgende.

* I **Godkjenning**-delen legger du til **Web** som en plattform og bruker følgende **Omdirigerings-URL**: https://businesscentral.dynamics.com/OAuthLanding.htm.
* I delen **Godkjenning** i alternativet for å velge **Støttede kontotyper** velger du **Kontoer i en hvilken som helst organisasjonskatalog (enhver Azure AD-katalog – flere leietakere)**.
* Opprett en ny klienthemmelighet i delen **Sertifikater og hemmeligheter**, og noter verdien. Mva-gruppemedlemmene trenger hemmeligheten når de konfigurerer tilkoblingen til grupperepresentanten.
* I delen **API-tillatelser** legger du til tillatelser til [!INCLUDE[prod_short](includes/prod_short.md)]. Aktiver delegert tilgang til **Financials.ReadWrite.All** og **user_impersonation**.
* I **Oversikt**-delen, noter **ID for program (klient)**. Mva-gruppemedlemmene trenger ID-en når de konfigurerer tilkoblingen til grupperepresentanten. 

## <a name="vat-group-member-setup"></a>Oppsett av mva-gruppemedlem
Konfigurer mva-gruppemedlemmet ved å starte assistert oppsettsveiledning for **Konfigurer mva-gruppestyring**. 

> [!NOTE]
> Før du begynner må du kontakte representanten for mva-gruppen for å få følgende informasjon om deres [!INCLUDE[prod_short](includes/prod_short.md)]-leier:
>
> * URL-adressen for API-et
> * Navnet på selskapet deres 
> * Klient-ID
> * Klienthemmelighet
> * Påloggingslegitimasjon for den dedikerte brukeren 

1. Hvis du vil definere selskapets mva-grupperolle, velger du **Medlem** og velger deretter **Neste**.
2. Kopier verdien i feltet **Gruppemedlems-ID**, og del den med mva-grupperepresentanten, slik at de kan legge til selskapet ditt som et godkjent medlem av gruppen.
3. Legg til **Nettadresse for API** fra mva-grupperepresentanten. Vanligvis er URL-adressen formatert som følger: `https://api.businesscentral.dynamics.com/v2.0/[TENANT-ID]/[ENVIRONMENTNAME]`. Eksempel: `https://api.businesscentral.dynamics.com/v2.0/907869c3-b252-4aca-b9cb-17a15d25477b/UKRepresentative`. 
4. Legg til [!INCLUDE[prod_short](includes/prod_short.md)]-firmanavnet for mva-grupperepresentanten, for eksempel *CRONUS UK Ltd*.
5. Velg **Godkjenningstype**, velg **OAuth2**, og velg deretter **Neste**.
6. Skriv inn ID-en som er angitt av mva-grupperepresentanten, i feltet **Klient-ID**.
7. I feltet **Klienthemmelighet angitt av mva-grupperepresentant** skriver du inn hemmeligheten fra mva-grupperepresentanten.
8. I feltet **Godkjenningsendepunkt for OAuth 2.0** angir du *https://login.microsoftonline.com/common/oauth2*.
9. I feltet **Ressursnettadresse for OAuth 2.0** angir du *https://api.businesscentral.dynamics.com/*.
10. I feltet **Omdirigeringsnettadresse for OAuth 2.0** angir du *https://businesscentral.dynamics.com/OAuthLanding.htm*. 
11. Når du har angitt de ulike feltene, velger du **Neste**, og skriv deretter inn brukerlegitimasjonen som ble gitt av mva-grupperepresentanten.
12. Velg konfigurasjonen for mva-rapporten du bruker til å rapportere mva til myndighetene i landet.

  I Storbritannia blir for eksempel konfigurasjonen av mva-rapporten definert til å rapportere mva til HMRC. Utvidelsen for mva-gruppestyring kopierer dette oppsettet, men erstatter codeuniten for sending med en som støtter sending til mva-grupperepresentanten i stedet for skattemyndighetene. Codeuniten leveres av Microsoft. Velg **Neste** når du er ferdig.

## <a name="using-the-vat-group-management-features"></a>Bruke funksjonene for mva-gruppestyring

Mva-gruppemedlemmer bruker standardprosessene til å forberede omsetningsoppgaver. Den eneste forskjellen er å velge rapportversjonen **MVA-GRUPPE**, som sender omsetningsoppgaven til mva-grupperepresentanten i stedet for myndighetene. Hvis du vil ha mer informasjon, kan du se [Om rapporten Omsetningsoppgave](finance-how-report-vat.md#about-the-vat-return-report).

Følgende deler beskriver oppgavene som mva-grupperepresentanter må utføre.

### <a name="vat-group-submissions"></a>Mva-gruppesendinger

Siden **Mva-gruppesendinger** viser omsetningsoppgavene som medlemmene har sendt. Siden fungerer som en kladd for sendingene før mva-grupperepresentanten inkluderer dem i en omsetningsoppgave for gruppen. Du kan åpne innsendingene for å kontrollere mva-en for de enkelte boksene som er rapportert av mva-gruppemedlemmene.

### <a name="creating-a-group-vat-return"></a>Opprette en omsetningsoppgave for gruppe

Hvis du vil rapportere mva på vegne av gruppen, oppretter du en omsetningsoppgave bare for selskapet ditt på siden **Omsetningsoppgaver**. Etterpå tar du med de siste mva-innsendingene fra mva-gruppemedlemmene ved å velge **Inkluder gruppe-mva**-handlingen.  

Når mva-grupperepresentantens omsetningsoppgave er sendt til myndighetene på vegne av hele gruppen, kjører du vanligvis handlingen **Beregn og bokfør mva-oppgjør**. Handlingen lukker åpne mva-poster og overfører beløp til mva-oppgjørskontoen. Denne handlingen tar for øyeblikket ikke hensyn til gruppeinnsendingene. Dette betyr at bare mva-postene i selskapet for mva-grupperepresentanten vil bli bokført. Innsendingsbeløpene for mva-gruppemedlemmer må bokføres til mva-oppgjørsbeløpet manuelt, slik at mva-oppgjørskontoen til mva-grupperepresentanten gjenspeiler gjelden for det som ble rapportert til myndighetene. Denne virkemåten vil endres i en kommende oppdatering av [!INCLUDE[prod_short](includes/prod_short.md)], slik at hele gruppens mva (det totale beløpet på rapportlinjer i omsetningsoppgaven) blir utlignet. 

> [!NOTE]
> Mva-gruppemedlemmer kan korrigere innsendte omsetningsoppgaver så lenge grupperepresentanten ikke har frigitt omsetningsoppgaven for gruppen. For å foreta en korrigering må mva-gruppemedlemmet opprette en ny omsetningsoppgave for omsetningsoppgaveperioden og sende den til mva-grupperepresentanten. På mva-grupperepresentantens side vil den siste omsetningsoppgaven bli inkludert på **Omsetningsoppgaver**-siden. 

> [!IMPORTANT]
> Funksjonen for mva-gruppe støttes bare i de markeder der [!INCLUDE[prod_short](includes/prod_short.md)] bruker et mva-rammeverk som består av mva-returer og mva-returperioder. Du kan ikke bruke mva-grupper i andre markeder som har andre implementeringer av lokal mva-rapportering, for eksempel Østerrike, Tyskland, Italia, Spania og Sveits. 

## <a name="see-also"></a>Se også
[Arbeide med mva på kjøp og salg](finance-work-with-vat.md)  
[Definere merverdiavgift (mva)](finance-setup-vat.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
