---
title: Svare på forespørsler om personopplysninger
description: Du må svare på forespørsler fra dataemner.
author: bholtorf
ms.service: dynamics365-business-central
ms.author: bholtorf
ms.custom: na
ms.date: 11/06/2018
ms.reviewer: na
ms.topic: article
ms.openlocfilehash: f7a217bd61b185586c71d5982d783840dd7ffd2e
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2019
ms.locfileid: "803381"
---
# <a name="responding-to-requests-about-personal-data"></a>Svare på forespørsler om personopplysninger  
Dataemner kan be om flere typer handlinger med hensyn til sine personopplysninger. For eksempel under EUs personvernforordning (GDPR) har innbyggere i EU rett til å be om eksport, sletting og endring av personlig informasjon. Dette kalles *dataemneforespørsel*. Hvis du har klassifisert sensitiviteten til dataene dine og er sikker på at de er riktige, kan administrator svare på forespørsler ved hjelp av alternativene under **Datavern** i rollesenteret **Administrasjon av brukere, brukergrupper og tillatelser** eller, hvis du bruker Windows-klienten, i rollesenteret **IT-sjef**. Hvis du vil ha mer informasjon om klassifisering av data og klassifisering av datasensitivitet i [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)], kan du se [Klassifisere data](/dynamics-nav/classifying-data?toc=/dynamics365/business-central/toc.json) og [Klassifisere datasensitivitet](admin-classifying-data-sensitivity.md).  

## <a name="types-of-requests"></a>Typer forespørsler

Tabellen nedenfor inneholder eksempler på ulike typer forespørsler du kan svare på.

> [!Note]
> Vi gir mulighet til å svare på denne typen forespørsler og dermed tilgang til personopplysninger, og det er ditt ansvaret å sikre at personopplysninger og sensitive data er lagret og klassifisert på riktig måte.

|Type forespørsel|Beskrivelse og foreslått svar|
|-----|-----|
|Portabilitetsforespørsler|Et dataemne kan forespørre en forespørsel og dataportabilitet, som delvis betyr at du må eksportere dataemnet personopplysninger fra systemene dine og levere dem i et strukturert vanlig format. Hvis du vil svare på disse forespørslene, kan du bruke **verktøyet for personverndata** til å eksportere personopplysninger til en Excel-fil eller en RapidStart-konfigurasjonspakke. Ved hjelp av Excel kan du redigere personopplysningene og lagre dem i et vanlig maskinlesbart format, for eksempel CSV eller XML. For RapidStart-konfigurasjonspakker kan du konfigurere hoveddatatabeller og tilhørende tabeller som inneholder personopplysninger. <br><br> **Obs!** Når du eksporterer data, kan du angi et minimum sensitivitetsnivå. Eksporten inkluderer minimum og alle sensitivitetsnivåer over det. Hvis du for eksempel vil eksportere data som er klassifisert som personlige, omfatter eksporten også data som er klassifisert som Sensitive. <br><br>Når du eksporterer data som er knyttet til et dataemne, ser **Verktøy for personverndata** etter direkte relasjoner mellom dataemnet og data knyttet til dataemnet. Indirekte relasjoner mellom data knyttet til dataemnet og andre data eksporteres ikke automatisk av **verktøyet for personverndata**. For eksempel, tabellen Kontakt har direkte relaterte kontaktprofilsvardata og tabellen Kontaktprofilsvar er ytterligere relatert til profilspørsmålsdata. Hvis du vil eksportere profilspørsmålene også, må du legge til denne tabellen manuelt som en rad med de aktuelle filtrene i konfigurasjonspakken som **verktøyet for personverndata** oppretter.|
|Forespørsler om sletting|Et dataemne kan be om at du kan sletter deres personopplysninger. Det finnes flere metoder for å slette personopplysninger ved hjelp av funksjonene for tilpassing, men avgjørelsen og implementeringen er ditt ansvar. I noen tilfeller kan du redigere data direkte, for eksempel slette en kontakt og deretter utføre kjørselen Slett annullerte samhandlingsposter for å slette samhandlinger for kontakten. <br><br> **Obs!** Hvis du har angitt en dato i feltet **Tillat sletting av dokument før** på siden **Salgsoppsett** eller **Kjøpsoppsett** sider, må du kanskje endre datoen, slik at du kan slette bokførte salgs- og kjøpsdokumenter som du har skrevet ut og som har bokføringsdatoer på eller før denne datoen.|
|Forespørsler om korrigering|Et dataemne kan be om at du kan korrigerer feile personopplysninger. Det er flere måter å gjøre dette på. I noen tilfeller kan du eksportere lister til Excel for rask samleredigering av flere poster, og deretter importere de oppdaterte dataene. Hvis du vil ha mer informasjon, kan du se [Eksportere forretningsdataene til Excel](about-export-data.md). Du kan også manuelt redigere felt som inneholder personopplysninger, for eksempel redigere opplysninger om en kunde i kundekortet. Imidlertid er transaksjonsposter, for eksempel kunde- og mva-poster, viktig for integriteten til ressursplanleggingssystemet til virksomheten. Hvis du lagrer personopplysninger i forretningstransaksjonsposter, bør du vurdere å bruke funksjonene for tilpassing for å endre slike personopplysninger.|

## <a name="restrict-data-processing-for-a-data-subject"></a>Begrense databehandling for et dataemne
Et dataemne kan be om at du midlertidig stopper behandling av deres personopplysninger. Hvis du vil overholde slike forespørsler, kan du merke posten som blokkert på grunn av personvern for å stoppe behandling av opplysningene deres. Når en post er merket som blokkert, kan du ikke opprette nye transaksjoner som bruker denne posten. Du kan for eksempel ikke opprette en ny faktura for en kunde når kunden eller selgeren er blokkert. Hvis du vil merke et dataemne som blokkert, åpner du kortet for dataemnet, for eksempel kunde-, leverandør- eller kontaktkortet, og merker av for **Personvern sperret**. Du må kanskje velge **Vis mer** for å vise feltet.  

## <a name="handling-data-subject-requests-while-in-trial"></a>Håndtere dataemneforespørsler ved prøveversjon
Enkelte typer personopplysninger inngår i Office 365-kontoen og krever administratortilgang for å eksporteres hvis du får en dataemneforespørsel fra en bruker angående denne typen personopplysninger under EUs personvernforordning (GDPR). Prosessen for å håndtere dataemneforespørsler er forskjellig avhengig av typen [!INCLUDE[d365fin](includes/d365fin_md.md)]-leietaker.  

Hvis du har et betalt abonnement for [!INCLUDE[d365fin](includes/d365fin_md.md)], må du kontakte organisasjonens leietakeradministrator for å opprette en dataemneforespørsel. Administratoren har administrasjonsrettigheter og verktøy for å oppfylle forespørselen.  

Hvis du har registrert deg for [!INCLUDE[d365fin](includes/d365fin_md.md)] fra siden med [prøveversjoner](https://trials.dynamics.com/), og du ikke har flyttet fra denne prøveversjonsopplevelsen gjennom et betalt abonnement av organisasjonens leietakeradministrator, kan du oppfylle din egen dataemneforespørsel på [personvernsiden for arbeid og skole i Azure-portalen](https://portal.azure.com#blade/Microsoft_AAD_IAM/GDPRViralBlade). Her kan du eksportere og laste ned dine egne persondata.

På personvernsiden for arbeid og skole kan du også lukke kontoen. Vi anbefaler imidlertid at du sørger for at du har eksportert og slettet alle data først siden sletting av kontoen betyr at du mister tilgang til [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Du kan fortsatt merke personer som blokkert på grunn av personvern og eksportere, redigere eller slette transaksjoner som beskrevet et annet sted i denne artikkelen.  

## <a name="exporting-data-from-tables-not-classified-by-data-subject"></a>Eksportere data fra tabellene som ikke er klassifisert etter dataemne
Hvis du har en situasjon der du må eksportere data som ikke er klassifisert slik at de eksporteres automatisk, for eksempel dataene fra tabellen Profilsvar, må du gjøre følgende:
-   Vurder om du virkelig vil eller må eksportere disse tilleggsdataene som ikke er knyttet til kontakten, det vil si at de er ikke direkte knyttet til den
-   Legg til denne tabellen og relasjonen manuelt i hurtigstartpakken, og eksporter dem direkte fra hurtigstartpakken. Derfor generere vi hurtigstartpakken for deg, slik at du kan endre den i situasjoner som denne.

## <a name="handling-data-about-minors"></a>Håndtere opplysninger om mindreårige
Hvis en kontaktperson alderen er lavere enn alderen for juridiske samtykke i henhold til lovene i ditt område, kan du angi dette ved å merke av for **Mindreårig** på **Kontakt**-kortet. Når du gjør dette merkes det automatisk av for **Personvern sperret**. Når du mottar samtykke fra den mindreåriges forelder eller juridiske verge, kan du merke av for **Samtykke fra foreldre mottatt** for å oppheve blokkeringen av kontakten. Selv om du kan behandle personopplysninger for mindreårige, kan du ikke bruke profileringsfunksjonaliteten i Microsoft Dynamics 365 for Sales.

> [!Note]
> Endringsloggen kan registrere opplysninger om for eksempel når og hvem som merket av for **Samtykke fra foreldre mottatt**. Administrator kan konfigurere dette ved å bruke veiledningen **Endringsloggoppsett** og også merke av for **Logge endring for samtykke fra foreldre mottatt** på **Kontakt**-kortet. Hvis du vil ha mer informasjon, kan du se [Logge endringer](across-log-changes.md).  

## <a name="see-also"></a>Se også
[Klassifisere data](/dynamics-nav/classifying-data?toc=/dynamics365/business-central/toc.json)  
[Klassifisere datasensitivitet](admin-classifying-data-sensitivity.md)  
[Eksportere forretningsdataene til Excel](about-export-data.md)  
[Logge endringer](across-log-changes.md)  
[Dataemneforespørsler for GDPR](/microsoft-365/compliance/gdpr-data-subject-requests)  
