---
title: Utvidelsen for mva-gruppestyring for Storbritannia
description: Du kan kommunisere med andre bedrifter for å danne en mva-gruppe der alle medlemmene rapporterer mva. i én enkelt retur.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, value added tax, report
ms.search.forms: ''
ms.date: 05/24/2022
ms.author: bholtorf
ms.openlocfilehash: c5757a78a44e3cdc2f6100c42b5105734928837b
ms.sourcegitcommit: 7a6efcbae293c024ca4f6622c82886decf86c176
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/02/2022
ms.locfileid: "8841923"
---
# <a name="the-vat-group-management-extension-for-the-united-kingdom"></a>Utvidelsen for mva-gruppestyring for Storbritannia

Du kan koble sammen et eller flere selskaper i landet for å kombinere mva-rapportering under ett enkelt registreringsnummer. Denne typen oppsett kalles en *mva-gruppe*. Du kan samarbeide med gruppen som medlem eller grupperepresentant.

## <a name="forming-a-vat-group"></a>Danne en mva-gruppe
MVA-gruppemedlemmer og grupperepresentanten kan bruke den assisterte oppsettsveiledningen for **Oppsett av mva-gruppestyring** til å definere samarbeidet med gruppen, og opprette en forbindelse mellom deres [!INCLUDE[prod_short](includes/prod_short.md)]-leietakere. Gruppemedlemmene bruker tilkoblingen til å sende omsetningsoppgavene deres til grupperepresentanten. Representanten bruker én omsetningsoppgave til å sende mva. til skattemyndighetene for gruppen. 

## <a name="license-requirements"></a>Lisenskrav
Deltakere i gruppen må være lisensierte for å bruke [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan ikke bruke gjestekontoer i mva-grupper. 

* For å beregne og sende omsetningsoppgaver må brukeren være en fullstendig Business Central-bruker.
* Hvis du vil logge på og utføre grunnleggende oppgaver, for eksempel opprette kontoer, kan du ha lisens for Dynamics 365 Business Central-gruppemedlemmer.

## <a name="vat-group-constellations"></a>Mva-gruppekonstellasjoner
Kommunikasjonen skjer fra gruppemedlemmer til representanten. Grupperepresentanten viser en API-nettadresse som gjør at medlemmene kan sende omsetningsoppgaven til mva-grupperepresentanten. 
[!INCLUDE[prod_short](includes/prod_short.md)] støtter sendinger av omsetningsoppgaver internt i gruppen for selskaper som bruker [!INCLUDE[prod_short](includes/prod_short.md)] lokalt eller online, og i en hvilken som helst kombinasjon. Oppsettet av kommunikasjonen avhenger av konstellasjonen. Denne artikkelen beskriver ulike gruppesammensetninger.

Følgende oversikt viser den anbefalte rekkefølgen av trinnene for å definere en mva-gruppe:

1. Opprett oppsettet i Azure Active Directory. Hvis du vil ha mer informasjon, kan du se [Krav for godkjenning](ui-extensions-vat-group.md#requirements-for-authentication).
2. Del de tekniske opplysningene som mva-gruppemedlemmer og representanten må ha for å koble sine [!INCLUDE[prod_short](includes/prod_short.md)]-leietakere. Vanligvis har mva-grupperepresentanten denne informasjonen, for eksempel navnet på miljøet for mva-grupperepresentanten som mva-gruppemedlemmene skal sende mva til.
3. Opprett brukere som mva-gruppemedlemmer kan bruke til å godkjenne når de kobler seg til mva-grupperepresentantens [!INCLUDE[prod_short](includes/prod_short.md)]. Brukerne må ha en fullstendig brukerlisens for [!INCLUDE[prod_short](includes/prod_short.md)].
4. Kjør assistert oppsettsveiledning for **Konfigurer mva-gruppestyring** for å koble sammen mva-gruppemedlemmene.

  Veiledningen krever noe informasjon fra mva-grupperepresentanten. Se [Oppsett av mva-gruppemedlemmer](#set-up-vat-group-members) hvis du vil ha mer informasjon. Merk deg **Gruppemedlems-ID**-en for hvert enkelt medlem i mva-gruppen. Representanten trenger disse ID-ene for å legge til selskapene i mva-gruppen.
5. Definer utvidelsen for mva-gruppestyring i mva-grupperepresentantens [!INCLUDE[prod_short](includes/prod_short.md)] ved hjelp av den assisterte oppsettsveiledningen for **Konfigurer mva-gruppestyring**. 

> [!NOTE]
> For å kunne koble til mva-grupperepresentanten må gruppemedlemmer ha en brukerkonto med tilgang til mva-grupperepresentantens [!INCLUDE[prod_short](includes/prod_short.md)]. MVA-grupperepresentanten må opprette minst én bruker for dette, men av sikkerhetsmessige grunner anbefales det at du oppretter en bruker for hvert enkelt mva-gruppemedlem. Pass på at du distribuerer legitimasjonen for disse brukerne til mva-gruppemedlemmer på en sikker måte. Dette er en systembrukerkonto som ikke er knyttet til en faktisk person.

## <a name="about-the-vat-group-management-setup"></a>Om oppsettet av mva-gruppestyring

Mva-grupperepresentanten viser en API til gruppemedlemmer. Medlemmene bruker API-en til å koble seg til representantens [!INCLUDE[prod_short](includes/prod_short.md)]-leietaker og sende omsetningsoppgaver. Mva-gruppemedlemmer bruker ofte [!INCLUDE[prod_short](includes/prod_short.md)] i separate Azure Active Directory-leietakere. Derfor trengs det oppsett for koble sammen mva-gruppemedlemmet og -representantens [!INCLUDE[prod_short](includes/prod_short.md)]. 
  
Mva-gruppemedlemmer kobles til representanten ved å ringe en webtjeneste i leieren for mva-grupperepresentanten. Anroperen må godkjennes ved hjelp av OAuth2. Når utvidelsen for mva-gruppestyring er definert, blir du bedt om å godkjenne til mva-grupperepresentanten for å få og lagre et tilgangstoken. Dette tilgangstokenet brukes ved sending av omsetningsoppgaver til mva-grupperepresentanten. 

## <a name="construct-the-api-url"></a>Konstruer API-nettadressen
1. Velg fanen **Miljøer** i administrasjonssenteret for Business Central for representantens leietaker.
2. Kopier **nettadressen** i delen **Detaljer**.
3. Åpne Notepad og lim inn nettadressen. Bytt ut **https://businesscentral.dynamics.com** med **https://api.businesscentral.dynamics.com/v2.0**.

## <a name="requirements-for-authentication"></a>Krav til godkjenning 
> [!NOTE]
> Dette krever legitimasjon for en administratorkonto som har en fullstendig brukerlisens for [!INCLUDE[prod_short](includes/prod_short.md)].

Når mva-grupperepresentanten bruker [!INCLUDE[prod_short](includes/prod_short.md)] online eller lokalt, må mva-gruppemedlemmene bruke Azure Active Directory til å godkjenne brukere når de sender omsetningsoppgaver til mva-grupperepresentanten. For den lokale versjonen av [!INCLUDE[prod_short](includes/prod_short.md)] må medlemmer konfigurere enkel pålogging. Hvis du vil ha mer informasjon, kan du se [Konfigurer Azure Active Directory-godkjenning med WS-Federation](/dynamics365/business-central/dev-itpro/administration/authenticating-users-with-azure-active-directory?tabs=singletenant%2Cadmintool). Hvis medlemmene i mva-gruppen også bruker [!INCLUDE[prod_short](includes/prod_short.md)] online, kan mva-gruppemedlemmet godkjenne ved å bruke den angitte brukerlegitimasjonen og informasjonen om endepunkt. Se [Oppsett av mva-gruppemedlemmer](ui-extensions-vat-group.md#set-up-vat-group-members) hvis du vil ha mer informasjon.

Mva-gruppemedlemmer som har [!INCLUDE[prod_short](includes/prod_short.md)] lokalt, må konfigurere en appregistrering i Azure Active Directory for mva-grupperepresentantens [!INCLUDE[prod_short](includes/prod_short.md)]-leietaker. Appregistreringen gjør at mva-grupperepresentantens nettversjon av [!INCLUDE[prod_short](includes/prod_short.md)] kan godkjenne gruppemedlemmet. Hvis du vil ha mer informasjon, kan du se [Hurtigstart: Registrere et program i Microsoft Identity Platform](/azure/active-directory/develop/quickstart-register-app).

Når du oppretter appregistreringen i Azure Active Directory, må du angi følgende informasjon.

* I **Godkjenning**-delen legger du til **Web** som en plattform og bruker følgende **Omdirigerings-URL**: https://businesscentral.dynamics.com/OAuthLanding.htm.
* I delen **Godkjenning** i alternativet for å velge **Støttede kontotyper** velger du **Kontoer i en hvilken som helst organisasjonskatalog (enhver Azure AD-katalog – flere leietakere)**.
* Opprett en ny klienthemmelighet i delen **Sertifikater og hemmeligheter**, og noter verdien. Mva-gruppemedlemmene trenger hemmeligheten når de konfigurerer tilkoblingen til grupperepresentanten.
* I delen **API-tillatelser** legger du til tillatelser til [!INCLUDE[prod_short](includes/prod_short.md)]. Aktiver delegert tilgang til **Financials.ReadWrite.All** og **user_impersonation**.
* I **Oversikt**-delen, noter **ID for program (klient)**. Mva-gruppemedlemmene trenger ID-en når de konfigurerer tilkoblingen til grupperepresentanten. 

## <a name="set-up-vat-group-members"></a>Konfigurer mva-gruppemedlemmer
> [!IMPORTANT]
> Medlemsselskapene i mva-gruppen trenger ikke å koble til HMRC fordi de rapporterer gjennom gruppens representant.

Før du begynner må du kontakte representanten for mva-gruppen for å få følgende informasjon om deres [!INCLUDE[prod_short](includes/prod_short.md)]-leier:

* URL-adressen for API-et
* Navnet på selskapet deres 
* Klient-ID
* Klienthemmelighet
* Påloggingslegitimasjon for den dedikerte brukeren 

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Konfigurer mva-gruppestyring**, og velg deretter den relaterte koblingen.
2. I feltet **Mva-grupperolle** angir du om du er medlem av gruppen eller gruppens representant. Velg **Medlem** for å fungere som et gruppemedlem og sende omsetningsoppgavene til grupperepresentanten i stedet for skattemyndighetene, og velg **Neste**.
3. Kopier verdien i feltet **Gruppemedlems-ID**, og del den med mva-grupperepresentanten, slik at de kan legge til selskapet ditt som et godkjent medlem av gruppen.
4. I feltet **Produktversjon for grupperepresentant** angir du hvilken versjon av [!INCLUDE[prod_short](includes/prod_short.md)] representanten bruker.
5. I feltet **Grupperepresentantselskap** skriver du inn firmanavnet for mva-grupperepresentanten. Eksempel: **CRONUS UK Ltd**.
6. I **Godkjenningstype**-feltet velger du alternativet for **OAuth2**. Hvis mva-grupperepresentanten bruker nettversjonen av [!INCLUDE[prod_short](includes/prod_short.md)], angir du at **grupperepresentanten bruker Business Central Online**, og deretter velger du **Neste**. Avhengig av om representanten bruker nettversjonen eller den lokale versjonen av [!INCLUDE[prod_short](includes/prod_short.md)], må du følge fremgangsmåten i avsnittene [Mva-grupperepresentant bruker Business Central Online](ui-extensions-vat-group.md#vat-group-representative-uses-business-central-online) eller [Mva-grupperepresentant bruker Business Central On-Premises](ui-extensions-vat-group.md#vat-group-representative-uses-business-central-on-premesis).

### <a name="vat-group-representative-uses-business-central-online"></a>Mva-grupperepresentanten bruker Business Central Online
1. Skriv inn brukerlegitimasjonen som ble levert av mva-grupperepresentanten, og legg til de nødvendige tillatelsene.
2. Velg konfigurasjonen av mva-rapporten som for øyeblikket brukes til å sende omsetningsoppgaver til skattemyndighetene. Når du har fullført oppsettet, oppretter [!INCLUDE[prod_short](includes/prod_short.md)] en ny konfigurasjon basert på dette alternativet og bruker konfigurasjonen til å sende omsetningsoppgaver til mva-grupperepresentanten.  
3. Legg til **Nettadresse for API** fra mva-grupperepresentanten. Vanligvis er URL-adressen formatert som følger: `https://api.businesscentral.dynamics.com/v2.0/[TENANT-ID]/[ENVIRONMENTNAME]`. Eksempel: `https://api.businesscentral.dynamics.com/v2.0/907869c3-b252-4aca-b9cb-17a15d25477b/UKRepresentative`.

### <a name="vat-group-representative-uses-business-central-on-premesis"></a>Mva-grupperepresentanten bruker Business Central On-Premises
1. I feltet **Klient-ID** angir du klient-ID-en fra appregistreringen i Azure Active Directory.
2. I feltet **Klienthemmelighet** angir du klienthemmeligheten fra appregistreringen i Azure Active Directory.
3. I feltet **Godkjenningsendepunkt for OAuth 2.0** angir du `https://login.microsoftonline.com/common/oauth2`.
4. I feltet **Ressursnettadresse for OAuth 2.0** angir du `https://api.businesscentral.dynamics.com/`.
5. I feltet **Omdirigeringsnettadresse for OAuth 2.0** angir du `https://businesscentral.dynamics.com/OAuthLanding.htm`.
6. Når du har angitt de ulike feltene, velger du **Neste**, og skriv deretter inn brukerlegitimasjonen som ble gitt av mva-grupperepresentanten.
7. Velg konfigurasjonen for mva-rapporten du bruker til å rapportere mva til myndighetene i landet.

## <a name="set-up-the-vat-group-representative"></a>Konfigurer mva-grupperepresentanten
> [!NOTE]
> For lokale versjoner støtter vi bare én enkelt leierforekomst av grupperepresentanten.

> [!IMPORTANT]
> Representantselskapet må aktivere **Mva-oppsett for HMRC** på siden **Tjenestetilkoblinger**. Representanter må også laste ned mva-returperioder fra HMRC.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Konfigurer mva-gruppestyring**, og velg deretter den relaterte koblingen.
2. I feltet **Mva-grupperolle** angir du om du er medlem av gruppen eller gruppens representant. Velg **Representant** for å fungere som mva-grupperepresentanten og sende omsetningsoppgavene til skattemyndighetene for gruppen, og velg **Neste**.
3. I feltet **Mva-oppgjørskonto** angir du kontoen du vil bruke til mva-oppgjør.
4. I **Feltnr. for mva-forfallsdato** feltet angir du boksen som representerer det totale mva-beløpet som skal betales, fra en mva-gruppesending.
5. I feltet **Finanskladdemal for gruppeoppgjør** angir du finanskladdemalen som er brukt i dokumentet, til å bokføre gruppe-mva. for oppgjørskontoen.
6. Feltet **Godkjente medlemmer** viser antall gruppemedlemmer som er definert til å sende omsetningsoppgaver til representanten. Hvis du vil legge til nye medlemmer, velger du nummeret for å åpne siden **Godkjente medlemmer**.
7. Hvis du vil legge til nye medlemmer, legger du til følgende informasjon på siden **Godkjente medlemmer for mva-gruppe**:
    1. I feltet **Gruppemedlems-ID** angir du en identifikator for gruppemedlemmet.
    2. I feltet **Navn på gruppemedlem** angir du navnet på gruppemedlemmet. 
    3. I feltet **Selskap** angir du selskapet som gruppemedlemmet skal sende omsetningsoppgaver fra i [!INCLUDE[prod_short](includes/prod_short.md)]. Eksempel: **CRONUS UK Ltd**.
    4. Angi kontaktinformasjonen for selskapet.

## <a name="use-the-vat-group-management-features"></a>Bruk funksjonene for mva-gruppestyring
Mva-gruppemedlemmer bruker standardprosessene til å forberede omsetningsoppgaver. Den eneste forskjellen er å velge rapportversjonen **MVA-GRUPPE**, som sender omsetningsoppgaven til mva-grupperepresentanten i stedet for myndighetene. Hvis du vil ha mer informasjon, kan du se [Om rapporten Omsetningsoppgave](finance-how-report-vat.md#vatreturn).

Følgende deler beskriver oppgavene som mva-grupperepresentanter må utføre.

### <a name="vat-group-submissions"></a>Mva-gruppesendinger

Siden **Mva-gruppesendinger** viser omsetningsoppgavene som medlemmene har sendt. Siden fungerer som en kladd for sendingene før mva-grupperepresentanten inkluderer dem i en omsetningsoppgave for gruppen. Du kan åpne innsendingene for å kontrollere mva-en for de enkelte boksene som er rapportert av mva-gruppemedlemmene. 

> [!TIP]
> På siden **Mva-returperioder** viser feltet **Gruppemedlemssendinger** hvor mange returer medlemmer har sendt. Du sikrer at dette tallet er oppdatert ved å velge handlingen **Hent omsetningsoppgaver**.

### <a name="creating-a-group-vat-return"></a>Opprette en omsetningsoppgave for gruppe

Hvis du vil rapportere mva for gruppen, oppretter du en omsetningsoppgave bare for selskapet ditt på siden **Omsetningsoppgaver**. Etterpå tar du med de siste mva-innsendingene fra mva-gruppemedlemmene ved å velge **Inkluder gruppe-mva**-handlingen.  

Når mva-grupperepresentantens omsetningsoppgave er sendt til myndighetene for gruppen, kjører du vanligvis handlingen **Beregn og bokfør mva-oppgjør**. Handlingen lukker åpne mva-poster og overfører beløp til mva-oppgjørskontoen. Denne handlingen tar for øyeblikket ikke hensyn til gruppeinnsendingene. <!--Has this changed?--> Bare mva-postene for mva-grupperepresentanten blir bokført. Innsendingsbeløpene for mva-gruppemedlemmer må bokføres til mva-oppgjørsbeløpet manuelt, slik at mva-oppgjørskontoen til mva-grupperepresentanten gjenspeiler gjelden for det som ble rapportert til myndighetene. Denne virkemåten vil endres i en kommende oppdatering av [!INCLUDE[prod_short](includes/prod_short.md)], slik at hele gruppens mva (det totale beløpet på rapportlinjer i omsetningsoppgaven) blir utlignet. <!--Has this behavior changed?-->

> [!NOTE]
> Mva-gruppemedlemmer kan korrigere innsendte omsetningsoppgaver så lenge grupperepresentanten ikke har frigitt omsetningsoppgaven for gruppen. For å foreta en korrigering må mva-gruppemedlemmet opprette en ny omsetningsoppgave for omsetningsoppgaveperioden og sende den til mva-grupperepresentanten. På mva-grupperepresentantens side vil den siste omsetningsoppgaven bli inkludert på **Omsetningsoppgaver**-siden. 

> [!IMPORTANT]
> Funksjonen for mva-gruppe støttes bare i de markeder der [!INCLUDE[prod_short](includes/prod_short.md)] bruker et mva-rammeverk som består av mva-returer og mva-returperioder. Du kan ikke bruke mva-grupper i andre markeder som har andre implementeringer av lokal mva-rapportering, for eksempel Østerrike, Tyskland, Italia, Spania og Sveits. 

## <a name="see-also"></a>Se også
[Lokal funksjonalitet for Storbritannia i den britiske versjonen](LocalFunctionality/unitedkingdom/united-kingdom-local-functionality.md)  
[Making Tax Digital i Storbritannia](LocalFunctionality/UnitedKingdom/making-tax-digital-submit-vat-return.md)  
[Arbeide med mva på kjøp og salg](finance-work-with-vat.md)  
[Definere merverdiavgift (mva)](finance-setup-vat.md)  
[Arbeid med mva. på kjøp og salg](finance-work-with-vat.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
