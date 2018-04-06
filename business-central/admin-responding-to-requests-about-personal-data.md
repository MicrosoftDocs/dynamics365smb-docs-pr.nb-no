---
title: "Svare på forespørsler om personopplysninger"
description: "Du må svare på forespørsler fra dataemner."
author: bholtorf
ms.author: bholtorf
ms.custom: na
ms.date: 03/13/2018
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 89f53f24f74401ce384b54d04fbeb473aedad96d
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---

# <a name="responding-to-requests-about-personal-data"></a>Svare på forespørsler om personopplysninger  
Dataemner kan be om flere typer handlinger med hensyn til sine personopplysninger. Hvis du har klassifisert sensitiviteten til dataene dine og er sikker på at de er riktig, kan administrator svare på forespørsler ved hjelp av dataklassifiseringsforslaget i rollesenteret **Administrasjon av brukere, brukergrupper og tillatelser**eller, hvis du bruker Windows-klienten, i rollesenteret **IT-sjef**. Hvis du vil ha mer informasjon om klassifisering av data og klassifisering av datasensitivitet, kan du se [Klassifisere data](/dynamics-nav/classifying-data) og [Klassifisere datasensitivitet](admin-classifying-data-sensitivity.md).

Tabellen nedenfor inneholder eksempler på ulike typer forespørsler du kan svare på.

> [!Note]
> Vi gir mulighet til å svare på denne typen forespørsler og dermed tilgang til personopplysninger, og det er ditt ansvaret å sikre at personopplysninger og sensitive data er lagret og klassifisert på riktig måte.

|Type forespørsel|Beskrivelse og foreslått svar|
|-----|-----|
|Portabilitetsforespørsler|Et dataemne kan forespørre en forespørsel og dataportabilitet, som delvis betyr at du må eksportere dataemnet personopplysninger fra systemene dine og levere dem i et strukturert vanlig format. Hvis du vil svare på disse forespørslene, kan du bruke verktøyet for personverndata til å eksportere personopplysninger til en Excel-fil. Ved hjelp av Excel kan du redigere personopplysningene og lagre dem i et vanlig maskinlesbart format, for eksempel CSV eller XML. Administratorer kan også eksportere data ved hjelp av RapidStart-konfigurasjonspakker og deretter konfigurere hoveddatatabeller og tilhørende tabeller som inneholder personopplysninger. |
|Forespørsler om sletting|Et dataemne kan be om at du kan sletter deres personopplysninger. Det finnes flere metoder for å slette personopplysninger ved hjelp av funksjonene for tilpassing, men avgjørelsen og implementeringen er ditt ansvar. I noen tilfeller kan du redigere data direkte, for eksempel slette en kontakt og deretter utføre kjørselen Slett annullerte samhandlingsposter for å slette samhandlinger for kontakten. <br><br> **Obs!** Hvis du har angitt en dato i feltet **Tillat sletting av dokument før** på siden **Salgsoppsett** eller **Kjøpsoppsett** sider, må du kanskje endre datoen, slik at du kan slette bokførte salgs- og kjøpsdokumenter som du har skrevet ut og som har bokføringsdatoer på eller før denne datoen.|
|Forespørsler om korrigering|Et dataemne kan be om at du kan korrigerer feile personopplysninger. Det er flere måter å gjøre dette på. I noen tilfeller kan du eksportere lister til Excel for rask samleredigering av flere poster, og deretter importere de oppdaterte dataene. Hvis du vil ha mer informasjon, kan du se [Eksportere forretningsdataene til Excel](https://docs.microsoft.com/en-us/dynamics-nav-app/about-export-data). Du kan også manuelt redigere felt som inneholder personopplysninger, for eksempel redigere opplysninger om en kunde i kundekortet. Imidlertid er transaksjonsposter, for eksempel kunde- og mva-poster, viktig for integriteten til ressursplanleggingssystemet til virksomheten. Hvis du lagrer personopplysninger i forretningstransaksjonsposter, bør du vurdere å bruke funksjonene for tilpassing for å endre slike personopplysninger.|

## <a name="restrict-data-processing-for-a-data-subject"></a>Begrense databehandling for et dataemne
Et dataemne kan be om at du midlertidig stopper behandling av deres personopplysninger. Hvis du vil overholde slike forespørsler, kan du merke posten som blokkert på grunn av personvern for å stoppe behandling av opplysningene deres. Når en post er merket som blokkert, kan du ikke opprette nye transaksjoner som bruker denne posten. Du kan for eksempel ikke opprette en ny faktura for en kunde når kunden eller selgeren er blokkert. Hvis du vil merke et dataemne som blokkert, åpner du kortet for dataemnet, for eksempel kunde-, leverandør- eller kontaktkortet, og merker av for **Personvern sperret**. Du må kanskje velge **Vis mer** for å vise feltet.

## <a name="handling-data-about-minors"></a>Håndtere opplysninger om mindreårige
Hvis en kontaktperson alderen er lavere enn alderen for juridiske samtykke i henhold til lovene i ditt område, kan du angi dette ved å merke av for **Mindreårig** på **Kontakt**-kortet. Når du gjør dette merkes det automatisk av for **Personvern sperret**. Når du mottar samtykke fra den mindreåriges forelder eller juridiske verge, kan du merke av for **Samtykke fra foreldre mottatt** for å oppheve blokkeringen av kontakten. Selv om du kan behandle personopplysninger for mindreårige, kan du ikke bruke profileringsfunksjonaliteten i Microsoft Dynamics 365 for Sales.

> [!Note]
> Endringsloggen kan registrere opplysninger om for eksempel når og hvem som merket av for **Samtykke fra foreldre mottatt**. Administrator kan konfigurere dette ved å bruke veiledningen **Endringsloggoppsett** og også merke av for **Logge endring for samtykke fra foreldre mottatt** på **Kontakt**-kortet. Hvis du vil ha mer informasjon, kan du se [Logge endringer](/dynamics-nav-app/across-log-changes).  

## <a name="see-also"></a>Se også
[Klassifisere data](https://docs.microsoft.com/en-us/dynamics-nav/classifying-data)  
[Klassifisere datasensitivitet](admin-classifying-data-sensitivity.md)  
[Eksportere forretningsdataene til Excel](https://docs.microsoft.com/en-us/dynamics-nav-app/about-export-data)  

