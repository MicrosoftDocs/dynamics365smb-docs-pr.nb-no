---
title: Integrer med Microsoft Dynamics 365 Field Service
description: Lær hvordan du integrerer Business Central med Field Service.
ms.date: 02/21/2024
ms.topic: article
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.custom: bap-template
---

# <a name="integrate-with-microsoft-dynamics-365-field-service"></a>Integrer med Microsoft Dynamics 365 Field Service

Serviceorganisasjoner krever en front-to-back-program der økonomi, lager og innkjøp er tett koblet sammen med tjenestelevering. De genererer økonomiske data med hver transaksjon. Hver arbeidsordre representerer kostnader og inntekter, og hver ressurs genererer fortjeneste og tap. Kundesamhandlinger legger til poster i finans. Integrasjonen mellom [!INCLUDE [prod_short](includes/prod_short.md)] og [!INCLUDE [field-service-short](includes/field-service-short.md)] effektiviserer ende-til-ende-prosessen med å administrere serviceoperasjoner og sikrer en jevn flyt av informasjon mellom de to systemene.  

Du kan enkelt opprette og administrere arbeidsordrer i [!INCLUDE [field-service-short](includes/field-service-short.md)], spore fremdriften for serviceoppgaver, tildele ressurser og registrere forbruksdetaljer. Når du fullfører en arbeidsordre i [!INCLUDE [field-service-short](includes/field-service-short.md)], muliggjør integreringen problemfri overføring av data for [!INCLUDE [prod_short](includes/prod_short.md)] videre behandling.  

Integreringen forenkler også fakturering og oppfyllelse av arbeidsordrer i [!INCLUDE [prod_short](includes/prod_short.md)]. Du kan generere nøyaktige fakturaer basert på serviceaktivitetene og forbruket som er registrert i [!INCLUDE [field-service-short](includes/field-service-short.md)].  

Ved å integrere [!INCLUDE [prod_short](includes/prod_short.md)] med [!INCLUDE [field-service-short](includes/field-service-short.md)] trenger du ikke å skrive inn data manuelt eller duplisere innsats. Integreringen gir også en omfattende oversikt over servicedrift og økonomi, noe som muliggjør bedre beslutningstaking og driftseffektivitet.

## <a name="prerequisites"></a>Forutsetninger

Fordi [!INCLUDE [field-service-short](includes/field-service-short.md)] er bygd på toppen av Dynamics 365 Sales, må du [konfigurere en tilkobling til Dataverse](/dynamics365/business-central/admin-how-to-set-up-a-dynamics-crm-connection#to-use-the-dataverse-connection-setup-assisted-setup-guide) og [aktivere integrering med Dynamics 365 Sales](/dynamics365/business-central/admin-prepare-dynamics-365-for-sales-for-integration#connection-settings-in-the-setup-guide).

### <a name="permissions-and-security-roles-for-user-accounts"></a>Tillatelser og sikkerhetsroller for brukerkontoer

Når du installerer integrasjonsløsningen, konfigureres tillatelser for integrasjonsbrukerkontoen. Hvis disse tillatelsene endres, er det mulig at du må tilbakestille dem. Dette kan du gjøre ved å installere integrasjonsløsningen på nytt fra siden **Konfigurasjon for Dynamics 365-tilkobling** på siden **Distribuer integreringsløsning på nytt**. Delene nedenfor viser tillatelsene og sikkerhetsrollene som løsningen ruller ut for hver app.

#### <a name="sales"></a>Salg

* Integreringsadministrator for Dynamics 365 [!INCLUDE [prod_short](includes/prod_short.md)]/
* Integreringsbruker for Dynamics 365 [!INCLUDE [prod_short](includes/prod_short.md)]
* Produkttilgjengelighetsbruker for Dynamics 365 [!INCLUDE [prod_short](includes/prod_short.md)]

#### <a name="business-central"></a>Business Central

Brukere som bokfører prosjektkladder, må ha følgende tillatelsessett:

* Dynamics 365 Sales-integrering

#### <a name="field-service"></a>Service hos kunde

Brukere må ha følgende sikkerhetsrolle for å kunne bruke de integrerte dataene:

* Business Central Field Service-integrering

Brukere må for eksempel ha denne rollen for å koble arbeidsordrer til [!INCLUDE [prod_short](includes/prod_short.md)] for behandling.

> [!NOTE]
> Sikre at brukere er tildelt til standard sikkerhetsroller og profiler i [!INCLUDE [field-service-short](includes/field-service-short.md)].  
>
> Hvis du vil lære mer om sikkerhetsprofiler for kolonner i [!INCLUDE [field-service-short](includes/field-service-short.md)], kan du gå til [Sikkerhetsroller i Field Service](/dynamics365/field-service/users-licenses-permissions#field-service-security-roles).
>
> Administratorer må legge til én av de aktuelle kolonnesikkerhetsprofilene for brukere i Power Platform. Hvis du vil ha mer informasjon, kan du gå til [Legg til team eller brukere i en kolonnesikkerhetsprofil for å kontrollere tilgang](/power-platform/admin/add-teams-users-field-security-profile).

> [!NOTE]
> Hvis du vil bruke handlingen **Åpne i Business Central** i Sales, må du ha følgende rettigheter for følgende tabeller:
>
>* Du må ha **lesetillatelse** for tabellen **Dynamics 365 Business Central-tilkobling** (nav_connection).
>* Du må ha **lese-**, **skrive-** og **slettetillatelser** for tabellen **Standard Dynamics 365 Business Central-tilkobling** (nav_defaultconnection).

### <a name="other-settings-in-field-service"></a>Andre innstillinger i Field Service

Angi følgende innstillinger på siden **Field Service-innstilling**:

* Fjern merket for **Bruk av produkter ikke på lager** i fanen **Kjøp**. Ellers kan du få en utsolgt-advarsel når du velger et produkt som ikke er på lager i [!INCLUDE [field-service-short](includes/field-service-short.md)], men som er på lager i [!INCLUDE [prod_short](includes/prod_short.md)].
* I fanen **Arbeidsordre/bestilling** deaktiverer du veksleknappene **Beregn pris** og **Beregn kost**. I feltet **Fakturaoppretting for arbeidsordre** velger du **Aldri**.

> [!NOTE]
> Hvis du definerer en tilkobling til [!INCLUDE [field-service-short](includes/field-service-short.md)], fjernes koblingen mellom ressurser og produkter. Hvis du vil gjøre [!INCLUDE [prod_short](includes/prod_short.md)]-varer tilgjengelige i [!INCLUDE [field-service-short](includes/field-service-short.md)], oppdaterer du feltet **Produkttype for Field Service** slik at det samsvarer med feltet **Type** på varene i [!INCLUDE [prod_short](includes/prod_short.md)]. Hvis du vil vite mer, kan du gå til [Opprett et produkt eller en tjeneste](/dynamics365/field-service/create-product-or-service#create-a-product-or-service).

## <a name="set-up-the-integration-in-business-central"></a>Konfigurer integreringen i Business Central

Når du har en tilkobling til Dataverse og Sales, kan du konfigurere integreringen til [!INCLUDE [field-service-short](includes/field-service-short.md)]. Velg **Konfigurer integrering til Dynamics 365 Field Service**på siden **Assistert oppsett** i [!INCLUDE [prod_short](includes/prod_short.md)] for å kjøre veiledningen for assistert oppsett. Denne delen beskriver nøkkelinnstillingene i veiledningen.

Hvis du vil la personer bokføre forbruk av varer og tjenester i [!INCLUDE [field-service-short](includes/field-service-short.md)]-arbeidsordrer, angir du **prosjektkladdemalen** og **prosjektkladden** som skal brukes til å bokføre forbruk av produkter og tjenester.

Siden tjenester uttrykkes i varighet i [!INCLUDE [field-service-short](includes/field-service-short.md)], angir du **timeenheten** som skal brukes til å konvertere varigheter til antall i [!INCLUDE [prod_short](includes/prod_short.md)].

Du kan også angi når arbeidsordreprodukter og tjenestelinjer synkroniseres til [!INCLUDE [prod_short](includes/prod_short.md)]. De kan for eksempel synkroniseres når arbeidsordrelinjer brukes, eller når noen fullfører en arbeidsordre. Velg riktig alternativ i feltet **Synkroniser arbeidsordreprodukter/-tjenester**.

Når arbeidsordreprodukter og -tjenester synkroniseres til prosjektkladder i [!INCLUDE [prod_short](includes/prod_short.md)], kan du velge om du vil bokføre prosjektkladdene manuelt. Velg riktig alternativ i feltet **Bokfør prosjektkladdelinjer automatisk**:

* når en arbeidsordre er fullført
* når arbeidsordreprodukter eller -tjenester brukes

Når du er ferdig med oppsettet, kjører du en fullstendig synkronisering fra siden **Oppsett for Dynamics 365 Field Service-integrering**. Denne handlingen synkroniserer tabelltilknytninger for ting som:

* Prosjektoppgaver for prosjekter med **Bruk forbrukskobling** valgt. Denne synkroniseringen gjør [!INCLUDE [prod_short](includes/prod_short.md)]-prosjekter tilgjengelige for valg i [!INCLUDE [field-service-short](includes/field-service-short.md)].
* Ressurser som ikke er blokkert, har ikke **Bruk timeliste** valgt og har **Timer** angitt som enhet på siden **Oppsett for Dynamics 365 Field Service-integrering**.
* Servicevarer (krever at du bruker Premium-opplevelsen i [!INCLUDE [prod_short](includes/prod_short.md)]).

## <a name="standard-field-service-entity-mapping-for-synchronization"></a>Standard Field Service-enhetstildeling for synkronisering

Det grunnleggende for å synkronisere data er å tilordne tabeller og felter i [!INCLUDE [prod_short](includes/prod_short.md)] med tabeller og kolonner i Dataverse slik at de kan utveksle data. Tilordning skjer gjennom integrasjonstabeller. Hvis du vil lære mer om tabelltilknytninger, kan du gå til [Tilknytt tabellene og feltene som skal synkroniseres](/dynamics365/business-central/admin-how-to-modify-table-mappings-for-synchronization).

Integrering med [!INCLUDE [field-service-short](includes/field-service-short.md)] innfører følgende standard integreringstabelltilknytninger.

* **PJLINE-WORDERPRODUCT** – Knytter arbeidsordreprodukter i [!INCLUDE [field-service-short](includes/field-service-short.md)] til prosjektkladdelinjer i [!INCLUDE [prod_short](includes/prod_short.md)].
* **PJLINE-WORDERSERVICE** – Knytter arbeidsordretjenester i [!INCLUDE [field-service-short](includes/field-service-short.md)] til prosjektkladdelinjer i [!INCLUDE [prod_short](includes/prod_short.md)].
* **PROJECTTASK** – Knytter prosjekter og prosjektoppgaver i [!INCLUDE [prod_short](includes/prod_short.md)] til produkter i eksterne prosjekter i [!INCLUDE [field-service-short](includes/field-service-short.md)].
* **RESOURCE-BOOKABLERSC** – Knytter ressurser i [!INCLUDE [prod_short](includes/prod_short.md)] til ressurser som kan reserveres, i [!INCLUDE [field-service-short](includes/field-service-short.md)].
* **SVCITEM-CUSTASSET** – (bare Premium-opplevelse) Knytter servicevarer i [!INCLUDE [prod_short](includes/prod_short.md)] til kundeobjekter i [!INCLUDE [field-service-short](includes/field-service-short.md)].

## <a name="use-data-in-both-applications"></a>Bruk data i begge programmene

De følgende avsnittene beskriver funksjonene der du kan bruke dataene som kommer fra [!INCLUDE [prod_short](includes/prod_short.md)] og [!INCLUDE [field-service-short](includes/field-service-short.md)].

### <a name="field-service-1"></a>Service hos kunde

Du kan [opprette arbeidsordrer](/dynamics365/field-service/create-work-order) ved hjelp av **tjenestekontoen** og **faktureringskontoen** fra [!INCLUDE [prod_short](includes/prod_short.md)]. På arbeidsordrer må du velge **Business Central-prosjektoppgaven** i feltet **Eksternt prosjekt**. Ved å velge et prosjekt kan du synkronisere arbeidsordreprodukter og -tjenester til den aktuelle prosjektoppgaven i [!INCLUDE [prod_short](includes/prod_short.md)].

Du kan legge til lagervarer og ikke-lagervarer som **arbeidsordreprodukter** i arbeidsordrer og få antallet på lager og kostnader og priser fra [!INCLUDE [prod_short](includes/prod_short.md)]. Hvis du vil ha mer informasjon, kan du gå til [Opprett en arbeidsordre fra arbeidsordreskjemaet og oppføringslisten](/dynamics365/field-service/create-work-order#create-a-work-order-from-the-work-order-form-and-record-list).

Du kan legge til vare av typen service som **arbeidsordretjenester**, og få kostnader og priser fra [!INCLUDE [prod_short](includes/prod_short.md)]. Hvis du vil vite mer, kan du gå til [fanen Produkter og tjenester](/dynamics365/field-service/work-order-experience#products-and-services-tab).

> [!NOTE]
> Når produktet eller tjenesten i en arbeidsordrestatus endres fra **Beregnet** til **Brukt** i [!INCLUDE [field-service-short](includes/field-service-short.md)], synkroniseres de til prosjektkladdelinjer i [!INCLUDE [prod_short](includes/prod_short.md)].

Du kan bestille en ressurs og knytte **bestillingene** til arbeidsordretjenester ved hjelp av en **ressurs som kan reserveres** fra [!INCLUDE [prod_short](includes/prod_short.md)].

### <a name="business-central-1"></a>Business Central

Når arbeidsordrer inkluderer produkter og tjenester, overføres og bokføres forbruksinformasjon ved hjelp av en **prosjektkladd** i [!INCLUDE [prod_short](includes/prod_short.md)], avhengig av innstillingene på siden **Oppsett av Field Service-integrering**.

Verdiene **Antall å fakturere** og **Varighet å fakturere** kopieres til feltet **Ant. som skal overføres til faktura**. Basert på disse verdiene kan du opprette og bokføre salgsfakturaer i [!INCLUDE [prod_short](includes/prod_short.md)] for å fakturere kunden. Når fakturaen er bokført eller forbruket er behandlet i [!INCLUDE [prod_short](includes/prod_short.md)], vises fakturert antall og brukt antall i fanen [!INCLUDE [prod_short](includes/prod_short.md)] på sidene **Arbeidsordreprodukt** og **Arbeidsordretjeneste**.  

Bruk siden **Prosjektplanleggingslinjer** til å spore bokføring og fakturering av forbruk i arbeidsordrer. Fra siden **Prosjektplanleggingslinjer** kan du opprette og bokføre salgsfakturaer i [!INCLUDE [prod_short](includes/prod_short.md)]. Etterpå kan du synkronisere dem med [!INCLUDE [field-service-short](includes/field-service-short.md)] og holde oversikt over statusen til fakturaene.

> [!NOTE]
> Arbeidsordretjenester med en bestilling som bruker en ressurs som kan reserveres, og som er koblet til en [!INCLUDE [prod_short](includes/prod_short.md)]-ressurs, synkroniseres til to prosjektkladdelinjer. Én linje av typen **Budsjett** for den tilknyttede ressursen, og en annen linje av typen **Fakturerbar** for varen som betjenes .
>
> Produktet som er valgt i arbeidsordretjenesten, må være koblet til en vare av typen **Service** i [!INCLUDE [prod_short](includes/prod_short.md)]. Lagerenheten for varen må også settes til **Timer-enheten** som er valgt på siden **Oppsett for Dynamics 365 Field Service-integreringsoppsett**.
>
> Du kan opprette en faktura for en vare av typen **Service** fra den fakturerbare prosjektplanleggingslinjen og bruke budsjettprosjektplanleggingslinjen til å registrere kostnader med ressursen.

## <a name="see-also"></a>Se også

[Integrer med Microsoft Dataverse via datasynkronisering](admin-common-data-service.md)  
[Tilordne tabellene og feltene som skal synkroniseres](admin-how-to-modify-table-mappings-for-synchronization.md)
