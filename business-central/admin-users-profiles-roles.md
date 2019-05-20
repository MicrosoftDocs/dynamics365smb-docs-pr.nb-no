---
title: Administrere brukere og roller | Microsoft-dokumentasjon
description: Finn ut hvordan du administrerer brukere og rollesentre i Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: profiles, users
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: fc52d943938616041881c55f70c510e4c63b5de6
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2019
ms.locfileid: "1245812"
---
# <a name="understanding-users-profiles-and-role-centers"></a>Forstå brukere, profiler og rollesentre

I [!INCLUDE[d365fin](includes/d365fin_md.md)] legges brukere til av en administrator som gir også brukere tilgang til deler av [!INCLUDE[d365fin](includes/d365fin_md.md)] som de trenger i arbeidet.  

Tilgang til funksjonene behandles gjennom *brukergrupper* og *profiler*. Du kan som administrator legge til og fjerne brukere som en del av [!INCLUDE[d365fin](includes/d365fin_md.md)]-abonnementet, og du kan tilordne brukertillatelser gjennom brukergrupper.  

## <a name="adding-users"></a>Legge til brukere

For å legge til brukere i [!INCLUDE[d365fin](includes/d365fin_md.md)] på nettet må selskapets Office 365-administrator først opprette brukere i administrasjonssenteret for Office 365. For mer informasjon, se [Legge til brukere i Office 365 for bedrifter](https://aka.ms/CreateOffice365Users).

Administrator kan deretter tilordne tillatelser til hver enkelt bruker og brukergruppe. Hvis du vil ha mer informasjon, kan du se [Administrere brukere og tillatelser](ui-how-users-permissions.md).  

De mest avanserte tillatelsene som en bruker kan ha, er SUPER-tillatelsessettet. Hvert selskap må ha minst én bruker med dette tillatelsessettet, men det er anbefalt å gi hver bruker tillatelser som samsvarer med arbeidsbehovet deres i [!INCLUDE[prodshort](includes/prodshort.md)] og ikke mer enn det. Dette sikrer at brukere bare har tilgang til data som er relevant for arbeidet deres, for eksempel.  

> [!TIP]
> Det er anbefalt å sikre at Office 365-administratoren også har SUPER-tillatelsen angitt i [!INCLUDE[prodshort](includes/prodshort.md)] fordi dette forenkler en rekke administrative oppgaver, inkludert oppsett av integrering med andre programmer.

### <a name="users-of-on-premises-deployments"></a>Brukere av lokale distribusjoner

For lokale distribusjoner av [!INCLUDE[d365fin](includes/d365fin_md.md)] kan systemansvarlig velge mellom forskjellige legitimasjonsgodkjenningsmekanismer for brukerne. Når du deretter oppretter en bruker, angir du ulike opplysninger avhengig av legitimasjonstypen du bruker i den spesifikke forekomsten av [!INCLUDE[server](includes/server.md)]. Hvis du vil ha mer informasjon, kan du se [Godkjenning og legitimasjonstyper](/dynamics365/business-central/dev-itpro/administration/users-credential-types) i Administrasjon-delen for utviklere og ITPro-innholdet for [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="profiles"></a>Profiler

Personene i selskapet som har tilgang til [!INCLUDE[d365fin](includes/d365fin_md.md)], er alle tilordnet en *profil* som gir dem tilgang til et *rollesenter*.

Profiler er samlinger av [!INCLUDE[d365fin](includes/d365fin_md.md)]-brukere som deler samme rollesenter. Et rollesenter er utgangspunktet og hjemmesiden for [!INCLUDE[d365fin](includes/d365fin_md.md)], som gir deg rask tilgang til de viktigste oppgavene og viser forskjellig innsikt og viktige ytelsesindikatorer (KPI-er) om arbeidet.  

> [!NOTE]  
>  I den gjeldende versjonen av [!INCLUDE[d365fin](includes/d365fin_md.md)] på nettet kan du legge til, endre eller slette profiler.  

### <a name="CreateProfile"></a>Opprette en profil

1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Profilliste**, og velg deretter den relaterte koblingen.  

2.  På siden **Profilliste** velger du handlingen **Ny** for å åpne **Nytt profilkort**-siden.  

3.  Skriv inn et navn som beskriver den tiltenkte rollen for brukerne, i **Profil-ID**-feltet.  

4.  I **Beskrivelse**-feltet angir du en beskrivelse av profil-IDen, for eksempel **Ordrebehandler**.  

5.  Sett **Rollesenter-ID**-felttet til rollesenteret du vil tilordne til profilen.  

Fremgangsmåten for å endre en eksisterende profil er det samme, bortsett fra at du velger en eksisterende profil på **Profilliste**-siden i stedet for å velge handlingen **Ny**.  


### <a name="copy-a-profile"></a>Kopiere en profil
Du kan spare tid ved å kopiere en profil hvis du vil bruke lignende innstillinger på en profil, og du bare vil endre noen innstillinger.

1.  Åpne profilen du vil kopiere, og velg deretter **Kopier profil**.

2.  I **Ny profil-ID**-feltet skriver du inn et navn for profilen du vil kopiere.

3.  Sett feltet **Nytt profilomfang** til ett av følgende:

    - **System** slik at den nye profilen blir tilgjengelig for alle leietakerdatabaser som bruker programmet.
    - **Leier** slik at den nye profilen blir tilgjengelig kun for den gjeldende leietakerdatabasen.
4. Når du er ferdig, velger du **OK**.

### <a name="ExportImportProfile"></a>Eksportere og importere profiler

Du kan eksportere og importere profiler som XML-filer til og fra en [!INCLUDE[d365fin](includes/d365fin_md.md)]-database. Du kan spare tid ved å eksportere og importere en profil når du konfigurerer brukergrensesnittet fordi du kan bruke en eksisterende profilkonfigurasjon i stedet for å konfigurere en profil på nytt. Hvis du har en profil som er konfigurert i en [!INCLUDE[d365fin](includes/d365fin_md.md)]-database, og du vil bruke på hele eller deler av det samme profil oppsettet i en annen database, kan du eksportere profilen til en XML-fil. Deretter kan du importere XML-filen for profilen til den andre databasen.

-   Hvis du vil eksportere en profil, kan du velge **Eksporter profiler**-handlingen fra **Profilliste**- eller **Profilkort**-siden, eller du kan søke etter og åpne **Eksporter profiler**-siden. Lagre XML-filen på datamaskinen eller i nettverket.

-   Hvis du vil importere en profil, kan du velge **Importer profil**-handlingen fra **Profilliste**-siden, eller du kan søke etter og åpne **Importer profiler**-siden. 

    > [!NOTE]  
    >  Du kan ikke importere en profil som allerede finnes i databasen, selv om XML-filen har et annet navn eller annet innhold. Du må slette den eksisterende profilen før du kan importere den nye profilen.


## <a name="configuration-and-personalization"></a>Konfigurasjon og tilpasning
<!--The concept of UI customization in [!INCLUDE[d365fin](includes/d365fin_md.md)] is divided in two:  

-   Configuration, performed by the administrator  

-   Personalization, performed by users  

The administrator configures the user interface for multiple users by customizing the user interface for a profile that the users are assigned to.  -->

Brukere tilpasser brukergrensesnittet i sin egen versjon ved å tilpasse brukergrensesnittet når de er logget på sine egne konti. Denne tilpasningen kan slettes av systemansvarlig. Hvis du vil ha mer informasjon, se [Tilpasse arbeidsområdet ](ui-personalization-user.md).  

## <a name="see-also"></a>Se også  
[Administrere brukere og tillatelser](ui-how-users-permissions.md)  
[Administrere tilpasning som Administrator](ui-personalization-manage.md)  
[Tilpasse arbeidsområdet](ui-personalization-user.md)  
