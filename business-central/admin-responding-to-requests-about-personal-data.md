---
title: Svare på forespørsler om brukers personopplysninger
description: Denne artikkelen forklarer hvordan du svarer på forespørsler om personopplysninger.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.date: 04/25/2023
ms.custom: bap-template
---

# <a name="responding-to-requests-about-users-personal-data"></a>Svare på forespørsler om brukers personopplysninger

Dataemner kan be om flere typer handlinger med hensyn til sine personopplysninger. For eksempel under enkelte personvernlover og -regler har de rett til å be om eksport, sletting og endring av personopplysninger. Disse forespørslene kalles *Dataemneforespørsler*. Hvis du har klassifisert følsomhetsnivået for dataene og er sikker på at de er riktige, kan en administrator svare på forespørsler ved hjelp av alternativene i fanen **Datavern** i rollesenteret **IT-sjef**. Hvis du vil ha mer informasjon om klassifisering av data og datafølsomhet i [!INCLUDE[prod_long](includes/prod_long.md)], går du til følgende artikler:

* [Klassifisere data](/dynamics-nav/classifying-data?toc=/dynamics365/business-central/toc.json) 
* [Klassifisere datasensitivitet](admin-classifying-data-sensitivity.md)  

## <a name="types-of-requests"></a>Typer forespørsler

Tabellen nedenfor inneholder eksempler på ulike typer forespørsler administratorer kan svare på.

> [!Note]
> Vi gir mulighet til å svare på denne typen forespørsler og dermed tilgang til personopplysninger, og det er ditt ansvaret å sikre at personopplysninger og sensitive data er lagret og klassifisert på riktig måte.

|Type forespørsel|Beskrivelse og foreslått svar|
|-----|-----|
|Portabilitetsforespørsler|Et dataemne kan gjøre en forespørsel om dataportabilitet. Du må eksportere de personlige dataene for dataemnet fra systemene og gi dem i et strukturert, vanlig brukt format. Hvis du vil svare på disse forespørslene, kan du bruke **verktøyet for personverndata** til å eksportere personopplysninger til en Excel-fil eller en RapidStart-konfigurasjonspakke. Ved hjelp av Excel kan du redigere personopplysningene og lagre dem i et vanlig maskinlesbart format, for eksempel CSV eller XML. For RapidStart-konfigurasjonspakker kan du konfigurere hoveddatatabeller og tilhørende tabeller som inneholder personopplysninger. <br><br> **Obs!** Når du eksporterer data, kan du angi et minimum sensitivitetsnivå. Eksporten inkluderer minimum og alle sensitivitetsnivåer over det. Hvis du for eksempel vil eksportere data som er klassifisert som personlige, omfatter eksporten også data som er klassifisert som Sensitive. <br><br>Når du eksporterer data som er knyttet til et dataemne, ser **Verktøy for personverndata** etter direkte relasjoner mellom dataemnet og data knyttet til dataemnet. Indirekte relasjoner mellom data knyttet til dataemnet og andre data eksporteres ikke automatisk av **verktøyet for personverndata**. For eksempel, tabellen Kontakt har direkte relaterte kontaktprofilsvardata og tabellen Kontaktprofilsvar er ytterligere relatert til profilspørsmålsdata. Hvis du vil eksportere profilspørsmålene også, må du legge til denne tabellen manuelt som en rad med de aktuelle filtrene i konfigurasjonspakken som **verktøyet for personverndata** oppretter.|
|Forespørsler om sletting|Et dataemne kan be om at du kan sletter deres personopplysninger. Det finnes flere metoder for å slette personopplysninger ved hjelp av funksjonene for tilpassing, men avgjørelsen og implementeringen er ditt ansvar. I noen tilfeller kan du velge å redigere dataene direkte. Slett for eksempel en kontakt og kjør deretter kjørselen Slett annullerte samhandlingsposter for å slette samhandlinger for kontakten. <br><br> **Obs!** Hvis du har angitt en dato i feltet **Tillat sletting av dokument før** på siden **Salgsoppsett** eller **Kjøpsoppsett** sider, må du kanskje endre datoen, slik at du kan slette bokførte salgs- og kjøpsdokumenter som har bokføringsdatoer på eller før denne datoen.|
|Forespørsler om korrigering|Et dataemne kan be om at du kan korrigerer feile personopplysninger. Det er flere måter å gjøre dette på. I noen tilfeller kan du eksportere lister til Excel for rask samleredigering av flere poster, og deretter importere de oppdaterte dataene. Hvis du vil ha mer informasjon, kan du se [Eksportere forretningsdataene til Excel](about-export-data.md). Du kan også manuelt redigere felt som inneholder personopplysninger, for eksempel redigere opplysninger om en kunde i kundekortet. Poster som finans, kunde og mva-poster er imidlertid viktige. Hvis du lagrer personopplysninger i forretningstransaksjonsposter, bør du vurdere å bruke funksjonene for tilpassing for å endre slike personopplysninger.|

## <a name="restrict-data-processing-for-a-data-subject"></a>Begrens databehandling for et dataemne

Et dataemne kan be om at du midlertidig stopper behandling av deres personopplysninger. Hvis du vil overholde slike forespørsler, kan du merke posten som blokkert på grunn av personvern for å stoppe behandling av opplysningene deres. Når en post er merket som blokkert, kan du ikke opprette nye transaksjoner som bruker denne posten. Du kan for eksempel ikke opprette en ny faktura for en kunde når kunden eller selgeren er blokkert. Hvis du vil merke et dataemne som blokkert, åpner du kortet for dataemnet, for eksempel kunde-, leverandør- eller kontaktkortet, og merker av for **Personvern sperret**. Du må kanskje velge **Vis mer** for å vise feltet.  

## <a name="handling-data-subject-requests-when-using-a-trial-version"></a>Håndter dataemneforespørsler når du bruker en prøveversjon

Visse typer personopplysninger er en del av en Microsoft 365-konto, og bare administratorer kan eksportere dataene. Prosessen for å håndtere dataemneforespørsler er forskjellig avhengig av typen [!INCLUDE[prod_short](includes/prod_short.md)]-leietaker.

Hvis du har et betalt abonnement for [!INCLUDE[prod_short](includes/prod_short.md)], må brukere kontakte organisasjonens leietakeradministrator for å opprette en dataemneforespørsel. Administratorer har administrasjonsrettigheter og verktøy for å oppfylle dataemneforespørselen.

Hvis du registrerte deg for [!INCLUDE[prod_short](includes/prod_short.md)] fra siden [Prøveversjoner](https://trials.dynamics.com/) og du fortsatt bruker prøveversjonen, kan brukerne laste ned og eksportere sine egne data på [personvernsiden for arbeid og skole i Azure Portal](https://portal.azure.com#blade/Microsoft_AAD_IAM/GDPRViralBlade).

På personvernsiden for arbeid og skole kan du også lukke kontoen. Vi anbefaler imidlertid at du eksporterer og sletter alle data først. Hvis du sletter kontoen, mister du tilgang til [!INCLUDE[prod_short](includes/prod_short.md)].

Du kan fortsatt merke personer som blokkert på grunn av personvern og eksportere, redigere eller slette transaksjoner som beskrevet et annet sted i denne artikkelen.  

## <a name="exporting-data-from-tables-not-classified-by-data-subject"></a>Eksport av data fra tabellene som ikke er klassifisert etter dataemne

Hvis du må eksportere data som ikke er klassifisert slik at de eksporteres automatisk, for eksempel dataene fra tabellen Profilsvar, må du gjøre følgende handlinger:

* Tenk over om du virkelig må eksportere tilleggsdata som ikke er direkte knyttet til kontakten.
* Legg til tabellen og relasjonen manuelt i Rapid Start-pakken, og eksporter den direkte fra Rapid Start-pakken. Vi genererer en Rapid Start-pakke for deg slik at du kan tilpasse den i slike situasjoner.

## <a name="handling-data-about-minors"></a>Håndter data om mindreårige

Hvis en kontaktperson alderen er lavere enn alderen for juridiske samtykke i henhold til lovene i ditt område, kan du angi dette ved å merke av for **Mindreårig** på **Kontakt**-kortet. Når du gjør dette merkes det automatisk av for **Personvern sperret**. Når du mottar samtykke fra den mindreåriges forelder eller juridiske verge, kan du merke av for **Samtykke fra foreldre mottatt** for å oppheve blokkeringen av kontakten. Selv om du kan behandle personopplysninger for mindreårige, kan du ikke bruke profileringsfunksjonaliteten i Dynamics 365 Sales.

> [!Note]
> Endringsloggen kan registrere opplysninger om for eksempel når og hvem som merket av for **Samtykke fra foreldre mottatt**. Administrator kan konfigurere dette ved å bruke veiledningen **Endringsloggoppsett** og også merke av for **Logge endring for samtykke fra foreldre mottatt** på **Kontakt**-kortet. Hvis du vil ha mer informasjon, kan du se [Logge endringer](across-log-changes.md).  

### <a name="see-also"></a>Se også

[Klassifisere data](/dynamics-nav/classifying-data?toc=/dynamics365/business-central/toc.json)  
[Klassifisere datasensitivitet](admin-classifying-data-sensitivity.md)  
[Eksportere forretningsdataene til Excel](about-export-data.md)  
[Logge endringer](across-log-changes.md)  
[Dataemneforespørsler](/microsoft-365/compliance/gdpr-data-subject-requests)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
