---
title: Administrer tilgang til Business Central
description: Administratorer bruker en lagvis tilnærming for å styre tilgang til Business Central og tilhørende funksjoner.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: jswymer
ms.topic: overview
ms.date: 04/04/2023
ms.custom: bap-template
---

# <a name="manage-access-to-business-central" />Administrer tilgang til Business Central

Denne artikkelen gir administratorer og programutviklere en oversikt på høyt nivå over hvordan du kan styre tilgangen til [!INCLUDE [prod_short](includes/prod_short.md)] og funksjonene. Bruk koblingene for å gå til andre artikler som inneholder flere detaljer om emnene.

## <a name="layered-access" />Lagdelt tilgang

[!INCLUDE [prod_short](includes/prod_short.md)] bruker en lagvis tilnærming til program sikkerhet, som beskrevet i følgende diagram. Hvis du vil finne ut mer om hvert lag, går du til [Programsikkerhet i Business Central](/dynamics365/business-central/dev-itpro/security/security-application).

:::image type="content" source="media/security-overview.png" alt-text="Lagdelt programsikkerhet i Business Central.":::

## <a name="licenses" />Lisenser

Tildel [!INCLUDE [prod_short](includes/prod_short.md)]-brukere til en **Dynamics 365 Business Central**-lisens slik at de kan vise, endre og handle med forretningsdata fra et hvilket som helst brukergrensesnitt. Hvis du vil vite mer om lisenser, går du til [Lisensiering i Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/deployment/licensing).

Personer som av og til trenger skrivebeskyttet tilgang til informasjon i [!INCLUDE [prod_short](includes/prod_short.md)], kan bruke en **Microsoft 365**-lisens. Hvis du vil vite mer om å gi begrenset tilgang, går du til [Business Central-tilgang med Microsoft 365-lisenser](admin-access-with-m365-license.md).

Hvis du vil ha omfattende informasjon om de ulike typene lisenser og hvordan lisensiering fungerer i [!INCLUDE[prod_short](includes/prod_short.md)], kan du se [Last ned lisensieringsveiledningen for Dynamics 365](https://go.microsoft.com/fwlink/?LinkId=866544).

## <a name="business-central-administrator-tasks" />Administrative oppgaver i Business Central

Tabellen nedenfor viser hvordan administratorer kan styre tilgang til [!INCLUDE [prod_short](includes/prod_short.md)] og funksjonene som skal brukes. Noen av oppgavene bidrar også til å holde tilgangsinnstillingene oppdatert.

|Oppgave| Finn ut mer |
|--|--|--|
|Hver person må ha en brukerkonto før de kan logge seg på [!INCLUDE [prod_short](includes/prod_short.md)]. Den enkleste måten å definere brukere på er å legge dem til én om gangen i [Microsoft 365-administrasjonssenteret](https://go.microsoft.com/fwlink/p/?linkid=2024339). |[Legg til brukere og tildel lisenser samtidig](/microsoft-365/admin/add-users/add-users)|
|Administrer tilgang for alle brukere på miljønivå. Opprett en Azure Active Directory-sikkerhetsgruppe (Azure AD) og tildel den til miljøet.<br><br> Du kan også bruke sikkerhetsgrupper til å behandle tilgang for bestemte brukergrupper. | [Administrer tilgang til miljøer](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-access)<br><br>[Styr tilgang til Business Central ved å bruke sikkerhetsgrupper](ui-security-groups.md) |
|Opprett brukere i [!INCLUDE [prod_short](includes/prod_short.md)], og angi hvem som kan logge seg på. | [Opprett brukere i henhold til lisenser](ui-how-users-permissions.md) |
|Sammen med brukerlisenser definerer tillatelser objektene som en bruker har tilgang til i hver database eller hvert miljø. Angi om personer kan lese, endre eller angi data i de valgte databaseobjektene. |[Tildel tillatelser til brukere og grupper](ui-define-granular-permissions.md)|
|Hvis en ekstern regnskapsfører administrerer tablåene og finansrapporteringen, inviterer du dem til [!INCLUDE [prod_short](includes/prod_short.md)]. De kan samarbeide tettere med deg om regnskapsdataene.|[Regnskapsføreropplevelser i [!INCLUDE[prod_long](includes/prod_long.md)]](finance-accounting.md)|
|Hvis du er en videresalgspartner for [!INCLUDE [prod_short](includes/prod_short.md)], kan du sende en e-post til en kunde for å be om en forhandlerrelasjon. Du kan inkludere delegerte administrasjonsrettigheter for Azure Active Directory og Microsoft 365 i e-postmeldingen.| [Delegert administratortilgang til Business Central Online](/dynamics365/business-central/dev-itpro/administration/delegated-admin)|
|En Azure-tjenestekode representerer en gruppe med IP-adresser som trafikken for en tjeneste kan komme fra eller gå til. Bruk tjenestekoder til å konfigurere brannmurer til å tillate trafikk bare fra bestemte tjenester. Med **Dynamics365BusinessCentral**-koden kan du bruke grupperegler for brannmur og nettverkssikkerhet for å begrense trafikk til og fra [!INCLUDE [prod_short](includes/prod_short.md)].| [Tjenestekoder for Azure-sikkerhet](/dynamics365/business-central/dev-itpro/security/security-service-tags)|
|Når du bruker Azure Active Directory-godkjenning med [!INCLUDE [prod_short](includes/prod_short.md)], anbefales det at du drar nytte av [Flerfaktorautentisering (MFA) for Azure AD](/azure/active-directory/authentication/concept-mfa-howitworks). MFA sikrer ytterligere tilgang til programmet og dataene.|[Flerfaktorautentisering for Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/security/multifactor-authentication)|

## <a name="business-central-developer-tasks" />Business Central-utvikleroppgaver

Det finnes også en utviklerartikkel for å administrere tilgang til [!INCLUDE [prod_short](includes/prod_short.md)]. Utviklere og administratorer kan for eksempel bygge og koble programmer til [!INCLUDE [prod_short](includes/prod_short.md)] som er til fordel for bedriften:  

* Effektiviser forretningsprosesser
* Forbedre kundesamhandlinger
* Ta bedre beslutninger, raskere

Tabellen nedenfor kobler til informasjon om hvordan du gir apper og utvidelser tilgang til [!INCLUDE [prod_short](includes/prod_short.md)]-data.

| Oppgave | Finn ut mer |
|--|--|
|De to hovedkonseptene for definisjon av tilgang til funksjoner er rettigheter og tillatelser. Rettigheter gir bred tilgang til objekter i henhold til lisenser eller Azure Active Directory-roller. Med tillatelser og tillatelsessett kan du finjustere tilgangen til objekter. |[Oversikt over rettigheter og tillatelsessett](/dynamics365/business-central/dev-itpro/developer/devenv-entitlements-and-permissionsets-overview)|

## <a name="see-also" />Se også

[Sikkerhet i Business Central](/dynamics365/business-central/dev-itpro/security/security-and-protection)
