---
title: Administrer OneDrive-integrering med Business Central
description: Finn ut mer om ting du kan gjøre for å administrere integrering mellom Business Central og OneDrive for Business.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'OneDrive, share, browser'
ms.date: 02/28/2022
ms.author: jswymer
---
# <a name="managing-onedrive-integration-with-business-central"></a><a name="managing-onedrive-integration-with-business-central"></a>Administrer OneDrive-integrering med Business Central

Denne artikkelen gir en oversikt over hva en administrator kan gjøre for å styre OneDrive for Business-integrasjon med [!INCLUDE[prod_short](includes/prod_short.md)]. [!INCLUDE[prod_short](includes/prod_short.md)] online-kunder får fordeler fra automatisk integrasjon, uten at det kreves ekstra oppsett for å bruke og dele OneDrive-funksjoner. Ved hjelp av veiledningen for assistert oppsett av **OneDrive-oppsett** kan du gi brukere tilgang til enda flere OneDrive-funksjoner, som å åpne Excel-filen i  OneDrive eller til og med deaktivere alle funksjoner.  

## <a name="configure-onedrive-for-integration-with-business-central"></a><a name="configure-onedrive-for-integration-with-business-central"></a>Konfigurere OneDrive for integrering med Business Central

Denne delen omhandler krav som må oppfylles i OneDrive for Business for å konfigurere integrasjon med Business Central og oppgave du kan gjøre for å administrere integreringen.

### <a name="minimum-requirements"></a><a name="minimum-requirements"></a>Minstekrav

* Hver bruker må ha en lisens for [!INCLUDE[prod_short](includes/prod_short.md)] og OneDrive som en del av en Microsoft 365-plan.
* OneDrive må konfigureres for hver bruker.

### <a name="managing-privacy"></a><a name="managing-privacy"></a>Administrer personvern

> [!IMPORTANT]
> Hvis du har valgt å distribuere Business Central OneDrive til forskjellige land eller regioner, kan det hende at filene som genereres av Business Central og plassert i OneDrive, kanskje krysser datalagringsgrenser. Kontroller at du bekrefter organisasjonens policyer og krav til offentlig samsvar for datalagring før du aktiverer tilkoblingen til OneDrive.

Administratorer og sluttbrukere kontrollerer innholdet som er lagret i OneDrive, og disse dataene eies bare av organisasjonen. Hvis du vil ha mer informasjon, kan du se [Hvordan SharePoint og OneDrive sikrer dataene i skyen](/sharepoint/safeguarding-your-data). Du kan også se [Microsofts personvernerklæring](https://privacy.microsoft.com/en-us/privacystatement), som forklarer dataene som Microsoft behandler, hvordan Microsoft behandler dem, og til hva slags formål.

Hvis du aktiverer denne tjenestetilkoblingen, godtar du følgende:

(a) å dele data fra Dynamics 365 Business Central med tjenesteleverandøren, som bruker dem i henhold til vilkårene og personvernerklæringen, (b) at samsvarsnivåene for tjenesteleverandøren kan være forskjellig fra Dynamics 365 Business Central, og (c) at Microsoft kan dele kontaktinformasjonen din med denne tjenesteleverandøren hvis det er nødvendig for at den skal fungere, og feilsøke tjenesten.

## <a name="configure-business-central"></a><a name="configure-business-central"></a>Konfigurer Business Central

Med Business Central online blir forbindelsen mellom Business Central og OneDrive automatisk konfigurert, og OneDrive-funksjonene er lett tilgjengelig for brukere som standard. Hvis du vil deaktivere noen av eller alle funksjonene, kan du bruke veiledning for assistert oppsett for **OneDrive** i Business Central-klienten.

Konfigurasjon av Business Central on-premises er forskjellig, fordi tilkoblingen mellom Business Central og OneDrive ikke er konfigurert for deg. Du må gjøre dette manuelt. Hvis du vil ha mer informasjon, kan du se [Konfigurere OneDrive-integrasjon med Business Central On-premises](admin-onedrive-integration-onpremises.md).

### <a name="about-multiple-environments"></a><a name="about-multiple-environments"></a>Om flere miljøer

OneDrive-integrasjon konfigureres per miljø, det vil si at innstillingene gjelder for alle selskaper i det aktuelle miljøet. Hvis organisasjonen har mer enn ett miljø, må du konfigurere OneDrive-integreringen for hver enkelt.

### <a name="prerequisites"></a><a name="prerequisites"></a>Forutsetninger

- Indirekte, endre og slette tillatelse (IMD) i tabell **Dokumenttjenestescenario** som et minimum

### <a name="configure-onedrive-using-onedrive-setup"></a><a name="configure-onedrive-using-onedrive-setup"></a>Konfigurer OneDrive ved hjelp av OneDrive-oppsett

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **OneDrive-oppsett** og velger den relaterte koblingen. 
2. Første gang du kjører assistert oppsett, vi ldu se **Personvern**. Les informasjonen psiden, og hvis du samtykker velger du **Godta** for å fortsette.
3. På siden **Konfigurer filbehandling** kan du velge mellom følgende alternativer:

   [!INCLUDE[onedrive-feature-options](includes/onedrive-feature-options.md)]
4. Velg **Neste**>**Ferdig**.

### <a name="switching-to-new-onedrive-integration-after-upgrade"></a><a name="switching-to-new-onedrive-integration-after-upgrade"></a>Bytte til ny OneDrive-integrering etter oppgraderingen

Installasjonsprogrammet for **OneDrive-oppsett** ble introdusert i lanseringsbølge 2 for 2022, versjon 21.0. Tidligere brukte OneDrive-integreringen **Oppsett for SharePoint-tilkobling**, som er avskrevet og vil bli fjernet i lanseringsbølge 2 for 2023, versjon 23.0. Etter at du har oppgradert til versjon 21, vil OneDrive fortsatt fungere som tidligere. Men vi anbefaler at du bytter til den nye OneDrive-integreringen. Denne bryteren gjør nå det enklere når **Tilkoblingsoppsett for SharePoint** blir fjernet. I tillegg kan du bruke assistert oppsettsveiledning for **OneDrive-oppsett** til å håndtere OneDrive-funksjonene som er tilgjengelige for brukerne. Assistert oppsett for **OneDrive**-oppsettet gjør overgangen fra det eldre SharePoint-oppsettet enkel og sømløs.

Hvis du vil bytte, åpner og kjører du det assosterte oppsettet for **OneDrive-oppsett** direkte eller du åpner **Tilkoblingn for SharePoint-oppsett** -siden og velger **Gå til nytt OneDrive-oppsett** i varslingen øverst på siden. Følg installasjonsveiledningen som beskrevet i forrige del.

## <a name="restoring-onedrive-and-"></a><a name="restoring-onedrive-and-"></a>Gjenopprett OneDrive og [!INCLUDE[prod_short](includes/prod_short.md)]

Som en del av en nødgjenopprettingsøvelse kan det hende at administratorer må gjenopprette et [!INCLUDE[prod_short](includes/prod_short.md)]-onlinemiljø til en sikkerhetskopi fra et tidspunkt i fortiden og synkronisere OneDrive-lagring med det samme tidspunktet. OneDrive inneholder ulike gjenopprettingsverktøy, for eksempel gjenoppretting av en brukers OneDrive til et tidligere tidspunkt, gjenoppretting av en tidligere versjon av en enkelt fil eller gjenoppretting av slettede filer. Hvis du vil ha mer informasjon, kan du se disse artiklene:

* For [!INCLUDE[prod_short](includes/prod_short.md)]: se [Gjenopprett et miljø i administrasjonssenteret](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-backup-restore).
* For OneDrive: se [gjenopprett din OneDrive](https://support.microsoft.com/en-us/office/restore-your-onedrive-fa231298-759d-41cf-bcd0-25ac53eb8a15?ui=en-us&rs=en-us&ad=us)

## <a name="governance"></a><a name="governance"></a>Styring

SharePoint-administrasjonssenteret gir omfattende kontroll over policyer som styrer bruken av OneDrive i hele organisasjonen. Globale administratorer eller brukere som har rollen SharePoint-administrator, kan konfigurere policyer som bestemmer hvem som kan få tilgang til OneDrive, hvor dataene er plassert, livssyklusen til innholdet og mye annet. Følgende koblinger gir informasjon om ofte brukte funksjoner og innstillinger som kan forbedre integreringen med [!INCLUDE[prod_short](includes/prod_short.md)]. 

* [Administrer delingsinnstillinger](/sharepoint/turn-external-sharing-on-or-off)
* [Bruk informasjonsbarrierer med SharePoint](/sharepoint/information-barriers)
* [Finn ut mer om hindring av datatap](/microsoft-365/compliance/dlp-learn-about-dlp)
* [Angi standard lagringsplass for OneDrive-brukere](/onedrive/set-default-storage-space)
* [Legg til og fjern administratorer for en brukers OneDrive](/sharepoint/manage-user-profiles#add-and-remove-admins-for-a-users-onedrive)
* [Deaktiver OneDrive-oppretting for enkelte brukere](/sharepoint/manage-user-profiles#disable-onedrive-creation-for-some-users)
* [Funksjoner for flere geografiske plasseringer i OneDrive og SharePoint Online](/microsoft-365/enterprise/multi-geo-capabilities-in-onedrive-and-sharepoint-online-in-microsoft-365)

> [!NOTE]
> Noen funksjoner er kanskje bare tilgjengelige for bestemte planer.

## <a name="see-also"></a><a name="see-also"></a>Se også

[Business Central og OneDrive for Business-integrering](across-onedrive-overview.md)  
[Åpne Business Central-filer i OneDrive](across-share-onedrive.md)  
[Vanlige spørsmål om OneDrive](admin-onedrive-faq.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
