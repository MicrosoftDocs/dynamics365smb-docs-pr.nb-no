---
title: Administrative oppgaver i Business Central
description: 'Enkelte oppgaver i Business Central krever sentral administrasjon og oppsett. Se hva de er, og finn ut hva som må gjøres.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 01/11/2023
ms.custom: bap-template
---
# <a name="administration-tasks"></a>Administrasjonsoppgaver

Sentrale administrasjonsoppgaver utføres vanligvis av én rolle i selskapet. Omfanget av disse oppgavene kan avhenge av selskapets størrelse og administrators jobbansvar. Disse oppgavene kan omfatte administrasjon av databasesynkronisering for jobb- og e-postkøer, oppsett av brukere og tilpassing av brukergrensesnittet.  

Det å angi riktige oppsettverdier for begynnelsen av er viktig for suksessen til all ny forretningsprogramvare. [!INCLUDE[prod_short](includes/prod_short.md)] inkluderer flere oppsettveiledninger som hjelper deg med å konfigurere kjernedata. Hvis du vil ha mer informasjon, kan du se [Definere Business Central](setup.md).

> [!NOTE]
> Du kan bruke dataoverføringsverktøyene til å overføre eksisterende data til [!INCLUDE [prod_short](includes/prod_short.md)] på nettet. Du kan alternativt opprette et nytt selskap i [!INCLUDE[prod_short](includes/prod_short.md)] med konfigurasjonspakker for å forkorte distribusjonstiden, forbedre kvaliteten på implementeringen, introdusere en implementeringsmetode som kan gjentas og øke produktiviteten ved å automatisere og forenkle regelmessige oppgaver. Hvis du vil ha mer informasjon, kan du se [Overfør lokale data til Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data).

Du kan støtte oppsettsbeslutningene dine med noen generelle anbefalinger for valgte felter som er kjent for å kunne forårsake at løsningen blir ineffektiv hvis feilaktig definert.  

En superbruker eller en administrator kan opprette et rammeverk for datautveksling slik at brukere kan eksportere og importere data i bank- og lønnsfiler, for eksempel for forskjellige bankstyringsprosesser. Hvis du vil ha mer informasjon, kan du se [Utveksle data elektronisk](across-data-exchange.md).

Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til artiklene som beskriver dem.  

|**Hvis du vil**|**Se**|  
|------------|-------------|
|Definer hvem som kan logge på [!INCLUDE[prod_short](includes/prod_short.md)] ved å opprette brukere på administrasjonssenteret for Microsoft 365 i henhold til produktlisensene.|[Opprette brukere i henhold til lisenser](ui-how-users-permissions.md)|
|Tilordne tillatelser til brukerne, endre tillatelsessett, og gruppere brukere for enkel behandling av tillatelser.|[Tilordne tillatelser til brukere og grupper](ui-how-users-permissions.md)|
|Legg til brukere, behandle tillatelser og tilgang til data, tilordne roller.|[Administrere profiler](admin-users-profiles-roles.md)|
|Behandle brukerinnstillinger, for eksempel firma, rolle, språk, region og tidssone.|[Brukerinnstillinger](admin-manage-user-settings-preferences.md)|
|Konfigurer skrivere, og angi hvilke rapporter som skal skrives ut på hvilke skrivere.|[Konfigurere skrivere](ui-specify-printer-selection-reports.md)|
|Klassifisere datafølsomheter for feltene slik at du kan svare på forespørsler fra dataobjekter relatert til personlig informasjon.|[Klassifiser datasensitivitet](admin-classifying-data-sensitivity.md)|
|Svare på forespørsler fra dataobjekter relatert til personlig informasjon.|[Svar på forespørsler om personopplysninger](admin-responding-to-requests-about-personal-data.md)|
|Konfigurere et nytt konsern ved hjelp av maler|[Opprett nye selskaper](about-new-company.md)|
|Spore alle direkte endringer som brukere gjør i data i databasen, for å finne ut hvor feil og dataendringer oppstår.|[Logge endringer](across-log-changes.md)|  
|Legge inn enkeltstående eller gjentakende forespørsler om å kjøre rapporter eller kodeenheter.|[Bruk jobbkøer til å planlegge oppgaver](admin-job-queues-schedule-tasks.md)|  
|Administrere, slette eller komprimere dokumenter|[Slett dokumenter](admin-manage-documents.md)|  
|Vis sider, kodeenheter og spørringer som web-tjenester.|[Publiser en nettjeneste](across-how-publish-web-service.md)|
|Som en del av å opprette Connect apps mellom [!INCLUDE[prod_short](includes/prod_short.md)] og tredjepartløsninger gjennom REST-API-er, må du definere maler som brukes til å fylle ut tomme egenskaper på en enhet når du oppretter en POST-handling gjennom et API.|[Konfigurer API-maler](admin-configuring-api-template.md)|
|Krypter data på [!INCLUDE[prod_short](includes/prod_short.md)]-serveren ved å generere nye eller importere eksisterende krypteringsnøkler som du aktiverer på serveren.|[Administrer datakryptering](admin-manage-data-encryption.md)|
|Koble Dynamics 365 Sales med [!INCLUDE[prod_short](includes/prod_short.md)] for å få en sømløs integrasjon mellom kunderelasjoner og ordrebehandling i interessent-til-kontanter-prosessen.|[Integrere med Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)|
|Endre hvilke felt og handlinger som skal vises i brukergrensesnittet, slik at det passer ditt selskaps forretningsprosesser, og utvid løsningen med apper.|[Tilpass [!INCLUDE[prod_short](includes/prod_short.md)]](ui-customizing-overview.md)|

## <a name="administration-in-the-admin-center"></a>Administrasjon i administrasjonssenteret

Interne og delegerte administratorer har tilgang til [!INCLUDE [prod_short](includes/prod_short.md)]-administrasjonssenteret der de kan konfigurere, overvåke og feilsøke [!INCLUDE [prod_short](includes/prod_short.md)]-miljøer. Tabellen nedenfor beskriver noen av hovedoppgavene, og har koblinger til artiklene som beskriver dem.  

|**Hvis du vil**|**Se**|  
|------------|-------------|
|Finn ut om verktøyene som kan hjelpe deg å feilsøke.|[Teknisk støtte](/dynamics365/business-central/dev-itpro/technical-support)|
|Overvåk bruk og feilsøk økter|[Miljøtelemetri i administrasjonssenteret for Business Central](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-telemetry)|
|Behandle brukerøkter, inkludert avbryte en økt, hvis brukeren er blokkert.|[Administrer økter](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-sessions)|
|Konfigurer leieren til å sende telemetridata til Azure Application Insights for bedre analyse og feilsøking.|[Aktiver sending av telemetri til Application Insights](/dynamics365/business-central/dev-itpro/administration/telemetry-enable-application-insights)|

## <a name="see-related-microsoft-training"></a>Se relatert [Microsoft-opplæring](/training/paths/deploy-configure-dynamics-365-business-central/)

## <a name="see-also"></a>Se også

[Forretningsfunksjoner](across-business-functionality.md)  
[Generelle forretningsfunksjoner](ui-across-business-areas.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Bli klar til å gjøre forretninger](ui-get-ready-business.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]
