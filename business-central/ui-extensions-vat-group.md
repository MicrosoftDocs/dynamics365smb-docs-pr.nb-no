---
title: Utvidelsen for mva-gruppestyring for Storbritannia
description: Du kan kommunisere med andre bedrifter for å danne en mva-gruppe der alle medlemmene rapporterer mva. i én enkelt retur.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'VAT, value added tax, report'
ms.search.form: '4700, 4701, 4703, 4704, 4705, 4706, 4707, 4708, 4709,'
ms.date: 06/03/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="the-vat-group-management-extension-for-the-united-kingdom"></a>Utvidelsen for mva-gruppestyring for Storbritannia

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Du kan koble sammen et eller flere selskaper i Storbritannia for å kombinere merverdiavgiftrapportering (mva.) under ett enkelt registreringsnummer. Denne typen oppsett kalles en *mva-gruppe*. Du kan samarbeide med gruppen som medlem eller grupperepresentant.

## <a name="forming-a-vat-group"></a>Danne en mva-gruppe

MVA-gruppemedlemmer og grupperepresentanten kan bruke den assisterte oppsettsveiledningen for **Konfigurer mva-gruppestyring** til å både definere samarbeidet med gruppen og opprette en forbindelse mellom deres [!INCLUDE[prod_short](includes/prod_short.md)]-leietakere. Gruppemedlemmene bruker denne tilkoblingen til å sende omsetningsoppgavene deres til grupperepresentanten. Grupperepresentanten bruker deretter én omsetningsoppgave til å sende gruppens mva. til skattemyndighetene.

[!INCLUDE[prod_short](includes/prod_short.md)] støtter sendinger av omsetningsoppgaver internt i gruppen for selskaper som bruker den lokale eller nettbaserte versjonen av [!INCLUDE[prod_short](includes/prod_short.md)], i en hvilken som helst kombinasjon som påvirker kommunikasjonsoppsettet mellom virksomheter. Denne artikkelen beskriver ulike gruppeoppsett.

### <a name="license-requirements"></a>Lisenskrav

Deltakere i gruppen må være lisensierte for å bruke [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan ikke bruke gjestekontoer i mva-grupper.

* For å beregne og sende omsetningsoppgaver må brukeren være en fullstendig [!INCLUDE[prod_short](includes/prod_short.md)]-bruker.
* Hvis du vil logge på og utføre grunnleggende oppgaver, for eksempel opprette kontoer, trenger du en lisens for [!INCLUDE[prod_long](includes/prod_long.md)] Team Member.

## <a name="set-up-a-vat-group"></a>Konfigurer en mva-gruppe

Nedenfor er den anbefalte rekkefølgen av trinnene en administratorer bruker til å konfigurere en mva-gruppe:

1. Opprett oppsettet i [Microsoft Entra ID-oppsett for gruppemedlemmene](#microsoft-entra-id-setup-for-group-members).
2. Del de tekniske opplysningene som mva-gruppemedlemmer og grupperepresentanten må ha for å koble sine [!INCLUDE[prod_short](includes/prod_short.md)]-leietakere. Vanligvis har grupperepresentanten denne informasjonen, for eksempel [API-nettadressen](#group-api-setup) og navnet på miljøet for mva-grupperepresentanten som mva-gruppemedlemmene skal sende mva til.
3. Opprett brukere som mva-gruppemedlemmer bruker til å godkjenne når de kobler seg til mva-grupperepresentantens [!INCLUDE[prod_short](includes/prod_short.md)]. Brukerne må ha en fullstendig brukerlisens for [!INCLUDE[prod_short](includes/prod_short.md)].
4. Kjør assistert oppsettsveiledning for **Konfigurer mva-gruppestyring** for å koble sammen mva-gruppemedlemmene.

   Mva-grupperepresentanten må angi visse opplysninger for å gruppere medlemmene for å fullføre oppsettet. (Finn ut mer i delen [Konfigurer mva-gruppemedlemmer](#set-up-vat-group-members) nedenfor.) Merk deg **gruppemedlems-ID-en** for hvert mva-gruppemedlem. Grupperepresentanten trenger disse ID-ene for å legge til selskapene i mva-gruppen.
5. Definer utvidelsen for mva-gruppestyring i mva-grupperepresentantens [!INCLUDE[prod_short](includes/prod_short.md)] ved hjelp av den assisterte oppsettsveiledningen for **Konfigurer mva-gruppestyring**.

> [!NOTE]
> For å kunne koble til mva-grupperepresentanten må gruppemedlemmer ha en brukerkonto med tilgang til mva-grupperepresentantens [!INCLUDE[prod_short](includes/prod_short.md)]. Mva-grupperepresentanten må opprette minst én bruker for denne. Av sikkerhetsmessige årsaker anbefales det imidlertid at de oppretter en bruker for hvert enkelt mva-gruppemedlem, som kan være en systembrukerkonto som ikke er knyttet til en faktisk person. Pass på at du distribuerer brukerlegitimasjonen til mva-gruppemedlemmer på en sikker måte.

### <a name="microsoft-entra-id-setup-for-group-members"></a>Microsoft Entra ID-konfigurasjon for gruppemedlemmer

Når mva-grupperepresentanten bruker [!INCLUDE[prod_short](includes/prod_short.md)] online eller lokalt, må mva-gruppemedlemmene bruke Microsoft Entra ID til å godkjenne brukere når de sender omsetningsoppgaver til mva-grupperepresentanten. For den lokale versjonen av [!INCLUDE[prod_short](includes/prod_short.md)] må medlemmer konfigurere enkel pålogging. Finn ut mer under [Konfigurer Microsoft Entra-godkjenning med WS-Federation](/dynamics365/business-central/dev-itpro/administration/authenticating-users-with-azure-active-directory?tabs=singletenant%2Cadmintool).

Hvis medlemmene i mva-gruppen også bruker [!INCLUDE[prod_short](includes/prod_short.md)] online, kan medlemmet godkjenne med den angitte brukerlegitimasjonen og påloggingsinformasjonen angitt av grupperepresentanten. Finn ut mer i delen [Konfigurer mva-gruppemedlemmer](#set-up-vat-group-members) nedenfor.

Mva-gruppemedlemmer som har [!INCLUDE[prod_short](includes/prod_short.md)] lokalt, må konfigurere en appregistrering i Microsoft Entra ID for mva-grupperepresentantens [!INCLUDE[prod_short](includes/prod_short.md)]-leietaker. Appregistreringen gjør at mva-grupperepresentantens nettversjon av [!INCLUDE[prod_short](includes/prod_short.md)] kan godkjenne gruppemedlemmet. Finn ut mer under [Hurtigstart: Registrere et program i Microsoft Identity Platform](/azure/active-directory/develop/quickstart-register-app).

Når administrator for mva-gruppemedlem oppretter appregistreringen i Microsoft Entra ID, må de angi følgende informasjon.

* I **Godkjenning**-delen legger du til **Nett** som en plattform og bruker følgende **Omdirigeringsnettadresse**: `https://businesscentral.dynamics.com/OAuthLanding.htm`.
* I delen **Godkjenning** i alternativet for å velge **Støttede kontotyper** velger du **Kontoer i en hvilken som helst organisasjonskatalog (enhver Microsoft Entra-katalog – flere leietakere)**.
* Opprett en ny klienthemmelighet i delen **Sertifikater og hemmeligheter**, og noter verdien. Mva-gruppemedlemmene trenger hemmeligheten når de konfigurerer tilkoblingen til grupperepresentanten.
* I delen **API-tillatelser** legger du til tillatelser til [!INCLUDE[prod_short](includes/prod_short.md)]. Aktiver delegert tilgang til **Financials.ReadWrite.All** og **user_impersonation**.
* I **Oversikt**-delen, noter **ID for program (klient)**. Mva-gruppemedlemmene trenger ID-en når de konfigurerer tilkoblingen til grupperepresentanten.

### <a name="group-api-setup"></a>API-oppsett for gruppe

Mva-grupperepresentanten oppretter og forsyner en API til gruppemedlemmer. Medlemmene bruker denne API-en til å koble seg til representantens [!INCLUDE[prod_short](includes/prod_short.md)]-leietaker og sende omsetningsoppgaver. Mva-gruppemedlemmer bruker ofte [!INCLUDE[prod_short](includes/prod_short.md)] i separate Microsoft Entra-leietakere. Derfor trengs det oppsett for koble sammen mva-gruppemedlemmet og -representantens [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]
> Dette oppsettet krever legitimasjon for en administratorkonto som har en fullstendig brukerlisens for [!INCLUDE[prod_short](includes/prod_short.md)].

1. Velg fanen **Miljøer** i administrasjonssenteret for Business Central for representantens leietaker.
1. Velg representantens miljø.
1. Kopier **nettadressen** i delen **Detaljer**.
1. Åpne Notepad og lim inn nettadressen. Bytt ut `https://businesscentral.dynamics.com` med `https://api.businesscentral.dynamics.com/v2.0`.

## <a name="set-up-vat-group-members"></a>Konfigurer mva-gruppemedlemmer

Mva-gruppemedlemmer kobles til representanten ved å ringe en webtjeneste i leieren for mva-grupperepresentanten. Anroperen må godkjennes ved hjelp av OAuth2. Når utvidelsen for mva-gruppestyring er definert, blir medlemmene bedt om å godkjenne til mva-grupperepresentanten for å få og lagre et tilgangstoken. Dette tilgangstokenet brukes ved sending av omsetningsoppgaver til mva-grupperepresentanten.

> [!IMPORTANT]
> Medlemsselskapene i mva-gruppen trenger ikke å koble til HMRC fordi de rapporterer gjennom gruppens representant.

Før mva-gruppemedlemmer starter oppsettet (oppført nedenfor), må de kontakte mva-grupperepresentanten for følgende informasjon om [!INCLUDE[prod_short](includes/prod_short.md)]-leieren:

* URL-adressen for API-et
* Navnet på selskapet deres
* Påloggingslegitimasjon for den dedikerte brukeren

1. I øvre høyre hjørne velger du ikonet **Innstillinger** ![Innstillinger.](media/ui-experience/settings_icon_small.png "Innstillinger-ikon for rollesenter") og deretter handlingen **Assistert oppsett**.
2. Velg handlingen **Konfigurer mva-gruppestyring**.
3. I feltet **Mva-grupperolle** velger du **medlem** og deretter **Neste**.
4. Kopier verdien i feltet **Gruppemedlems-ID**, og del den med mva-grupperepresentanten, slik at de kan legge til selskapet ditt som et godkjent medlem av gruppen.
5. I feltet **Produktversjon for grupperepresentant** angir du hvilken versjon av [!INCLUDE[prod_short](includes/prod_short.md)] representanten bruker.
6. Skriv inn API-nettadressen som er angitt av mva-grupperepresentanten, i feltet **API-nettadresse**. Vanligvis er URL-adressen formatert som følger: `https://api.businesscentral.dynamics.com/v2.0/[TENANT-ID]/[ENVIRONMENTNAME]`. Eksempel: `https://api.businesscentral.dynamics.com/v2.0/907869c3-b252-4aca-b9cb-17a15d25477b/UKRepresentative`.
7. I feltet **Grupperepresentantselskap** skriver du inn firmanavnet for mva-grupperepresentanten, som **CRONUS UK Ltd**.
8. I **Godkjenningstype**-feltet velger du alternativet for **OAuth2**. Hvis mva-grupperepresentanten bruker nettversjonen av [!INCLUDE[prod_short](includes/prod_short.md)], aktiverer du vekslebryteren **grupperepresentanten bruker Business Central Online**, og deretter velger du **Neste**.

   Følg deretter fremgangsmåten i avsnittene [Mva-grupperepresentant bruker Business Central Online](ui-extensions-vat-group.md#vat-group-representative-uses-business-central-online) eller [Mva-grupperepresentant bruker Business Central On-Premises](ui-extensions-vat-group.md#vat-group-representative-uses-business-central-on-premises) nedenfor.

### <a name="vat-group-representative-uses-business-central-online"></a>Mva-grupperepresentanten bruker Business Central Online

1. Skriv inn brukerlegitimasjonen som ble levert av mva-grupperepresentanten, og legg til de nødvendige tillatelsene for å generere tilgangstokenet.
2. Velg konfigurasjonen av mva-rapporten du bruker til å sende omsetningsoppgaver til skattemyndighetene i Storbritannia. 

Når du har fullført oppsettet, oppretter [!INCLUDE[prod_short](includes/prod_short.md)] en ny konfigurasjon basert på dette alternativet slik at du kan sende omsetningsoppgaver til mva-grupperepresentanten.

### <a name="vat-group-representative-uses-business-central-on-premises"></a>Mva-grupperepresentanten bruker Business Central On-Premises

1. Skriv inn bruker legitimasjonen fra mva-grupperepresentanten, og velg **Neste**.
2. I feltet **Klient-ID** angir du klient-IDen fra appregistreringen i [Microsoft Entra ID-oppsett for gruppemedlemmer](#microsoft-entra-id-setup-for-group-members).
3. I feltet **Klienthemmelighet** angir du klienthemmeligheten fra appregistreringen i Microsoft Entra ID.
4. I feltet **Godkjenningsendepunkt for OAuth 2.0** angir du `https://login.microsoftonline.com/common/oauth2`.
5. I feltet **Ressursnettadresse for OAuth 2.0** angir du `https://api.businesscentral.dynamics.com/`.
6. I feltet **Omdirigeringsnettadresse for OAuth 2.0** angir du `https://businesscentral.dynamics.com/OAuthLanding.htm`.
7. Velg **Neste** når du har angitt de ulike feltene, og bekreft deretter at godkjenningstilkoblingen genererer tilgangstokenet.
8. Velg konfigurasjonen av mva-rapporten du bruker til å sende omsetningsoppgaver til skattemyndighetene i Storbritannia.

## <a name="set-up-the-vat-group-representative"></a>Konfigurer mva-grupperepresentanten

> [!NOTE]
> For lokale versjoner støtter [!INCLUDE[prod_short](includes/prod_short.md)] bare én enkelt leierforekomst av grupperepresentanten.

> [!IMPORTANT]
> Representantselskapet må aktivere **Mva-oppsett for HMRC** på siden **Tjenestetilkoblinger**. Representanter må også laste ned mva-returperioder fra HMRC.

1. I øvre høyre hjørne velger du **Innstillinger**-ikonet ![Innstillinger.](media/ui-experience/settings_icon_small.png "Innstillinger-ikon for rollesenter"), og velg deretter handlingen **Assistert oppsett**.
2. Velg handlingen **Konfigurer mva-gruppestyring**.
3. I feltet **va-grupperolle** velger du **representant** som skal fungere som mva-grupperepresentant, og deretter velger du **Neste**.
4. I feltet **Gruppeoppgjørskonto** angir du avregningskontoen som skal brukes i de gruppemedlemmets mva-beløp. Denne kontoen må ha **Aktiva** som **Kontokategori**.
5. I feltet **Mva-oppgjørskonto** angir du kontoen du vil bruke til mva-oppgjør. Denne kontoen må ha **Gjeld** som **Kontokategori**.
6. I **Feltnr. for mva-forfallsdato** feltet angir du boksen som representerer det totale mva-beløpet som skal betales, fra en mva-gruppesending.
7. I feltet **Finanskladdemal for gruppeoppgjør** angir du finanskladdemalen som er brukt for å opprette dokumentet med som grupperepresentanten bruker til å bokføre gruppe-mva. for oppgjørskontoen.
8. Feltet **Godkjente medlemmer** viser antall gruppemedlemmer som er definert til å sende omsetningsoppgaver til grupperepresentanten. Hvis du vil legge til nye medlemmer, velger du nummeret for å åpne siden **Godkjente medlemmer for mva-gruppe** og legger til følgende informasjon:
    1. I feltet **Gruppemedlems-ID** angir du en ID for gruppemedlemmet, som vist under gruppemedlemsoppsettet (finn ut mer i delen [Oppsett av mva-gruppemedlem](#set-up-vat-group-members) ovenfor).
    2. I feltet **Navn på gruppemedlem** angir du navnet på gruppemedlemmet.
    3. I feltet **Selskap** angir du selskapet som gruppemedlemmet sender omsetningsoppgaver fra i [!INCLUDE[prod_short](includes/prod_short.md)], som **CRONUS UK Ltd**.
    4. Angi kontaktinformasjonen for selskapet.

## <a name="use-the-vat-group-management-features"></a>Bruk funksjonene for mva-gruppestyring

Mva-gruppemedlemmer bruker standardprosessene til å forberede omsetningsoppgaver. Den eneste forskjellen er at medlemmer må velge rapportversjonen **MVA-GRUPPE** på siden **Omsetningsoppgave** for å sende omsetningsoppgaven til mva-grupperepresentanten i stedet for myndighetene. Finn ut mer under [Om rapporten Omsetningsoppgave](finance-how-report-vat.md#vatreturn).

> [!NOTE]
> Mva-gruppemedlemmer kan korrigere innsendte omsetningsoppgaver så lenge grupperepresentanten ikke har frigitt omsetningsoppgaven for gruppen. For å foreta en korrigering må mva-gruppemedlemmet opprette en ny omsetningsoppgave for omsetningsoppgaveperioden og sende den til mva-grupperepresentanten. På mva-grupperepresentantens side vil medlemmets siste omsetningsoppgave bli erstattet av den forrige og blir inkludert på **Omsetningsoppgaver**-siden.

Følgende deler beskriver oppgavene som mva-grupperepresentanter må utføre for å sende gruppens omsetningsoppgave.

### <a name="review-vat-member-submissions"></a>Se gjennom mva-medlemssendinger

Siden **Mva-gruppesendinger** viser omsetningsoppgavene som medlemmene har sendt. Siden fungerer som en kladd for sendingene før mva-grupperepresentanten inkluderer dem i en omsetningsoppgave for gruppen. Representanten kan åpne innsendingene for å kontrollere de enkelte boksene som inneholder beløpet rapportert av hvert mva-gruppemedlemmene.

> [!TIP]
> På siden **Mva-returperioder** viser feltet **Gruppemedlemssendinger** hvor mange returer medlemmer har sendt. Du sikrer at dette tallet er oppdatert ved å velge handlingen **Hent omsetningsoppgaver**.

### <a name="create-a-group-vat-return"></a>Opprett en omsetningsoppgave for gruppe

Hvis du vil rapportere mva for gruppen, oppretter du en omsetningsoppgave bare for selskapet ditt på siden **Omsetningsoppgaver**. Etterpå tar du med de siste mva-innsendingene fra mva-gruppemedlemmene ved å velge **Inkluder gruppe-mva**-handlingen.  

Når grupperepresentanten har sendt inn gruppens omsetningsoppgave til myndighetene, kjører representanten vanligvis handlingen **Beregn og bokfør mva-oppgjør**. Handlingen lukker åpne mva-poster og overfører beløp til mva-oppgjørskontoen. Denne handlingen tar for øyeblikket ikke hensyn til gruppeinnsendingene. Bare mva-postene for mva-grupperepresentanten blir bokført. Innsendingsbeløpene for mva-gruppemedlemmer må bokføres ved hjelp av handlingen **Bokfør mva-gruppeoppgjør** .

> [!IMPORTANT]
> Funksjonen for mva-gruppe støttes bare i de markeder der [!INCLUDE[prod_short](includes/prod_short.md)] bruker et mva-rammeverk som består av mva-returer og mva-returperioder. Du kan ikke bruke mva-grupper i markeder med andre implementeringer av lokal mva-rapportering, for eksempel Østerrike, Tyskland, Italia, Spania og Sveits.

## <a name="issue-with-enabling-multifactor-authentication-mfa"></a>Problem med aktivering av flerfaktorautentisering (MFA)

Hvis du får en feilmelding relatert til autorisasjon under fornyelsen av **OAuth2-token** på siden **Mva-rapportoppsett** etter at du har aktivert MFA, følger du denne fremgangsmåten.  

1. Logg på **Azure Portal** som godkjenningsadministrator.  
2. Gå til **Microsoft Entra ID**.   
3. Gå til **Brukere**, og velg brukeren du vil skal utføre en handling.  
4. Velg **Godkjenningsmetodene**, og på toppen av siden velger du **Krev ny registrering av flerfaktorautentisering**. 
5. Gå tilbake til Dynamics 365 Business Central, og velg å fornye tokenet fra **Mva-rapportoppsett**.  

Dette bør være et engangsoppsett etter at du har aktivert godkjenning med flere faktorer for brukeren som er valgt i **Mva-rapportoppsett**.  

## <a name="see-also"></a>Se også

[Lokal funksjonalitet for Storbritannia i den britiske versjonen](LocalFunctionality/unitedkingdom/united-kingdom-local-functionality.md)  
[Making Tax Digital i Storbritannia](LocalFunctionality/UnitedKingdom/making-tax-digital-submit-vat-return.md)  
[Arbeid med mva. på kjøp og salg](finance-work-with-vat.md)  
[Definere merverdiavgift (mva)](finance-setup-vat.md)  
[Arbeid med mva. på kjøp og salg](finance-work-with-vat.md)  
[Konsolider finansielle data fra flere selskaper](finance-consolidated-company-reporting.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
