---
title: Oppdatere egendefinerte rapportoppsett
description: Lær hvordan du oppdaterer et egendefinert rapportoppsett som brukes i en rapport når det for eksempel finnes utformingsendringer i rapportens datasett.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '9652, 9650'
ms.date: 06/24/2021
ms.author: edupont
---
# <a name="legacy-update-custom-report-layouts" />(Eldre) Oppdater egendefinerte rapportoppsett

[!INCLUDE[legacy-custom-layouts](includes/legacy-custom-layouts.md)]

Noen ganger må du kanskje oppdatere et egendefinert rapportoppsett som brukes i en rapport. Dette er nødvendig når det er en endring i utformingen av rapportens datasett, for eksempel hvis et felt som brukes i oppsettet, er fjernet fra rapportdatasettet. Hvis et rapportoppsett må oppdateres, får du en feilmelding når du prøver å forhåndsvise, skrive ut eller lagre rapporten.  

Du kan oppdatere automatisk et rapportoppsettet fra feilmeldingen som vises når du kjører rapporten, ved å velge **Ja**-knappen på feilmeldingen. Eller du kan oppdatere bestemte rapportoppsett eller alle tilpassede rapportoppsett som kan bli påvirket av endringer i datasettet, før du kjører rapportene.  

Du har også muligheten til å teste oppdateringer uten å bruke de nødvendige endringene på de egendefinerte rapportoppsettene. Dette gjør det mulig å se hvilke endringer som vil bli brukt på rapportoppsettet og identifisere mulige problemer i prosessen. Fra testresultatene kan du åpne de egendefinerte rapportoppsettene direkte for redigering for å rette opp eventuelle problemer. Vi anbefaler at du tester oppdateringen av rapportoppsettet før du bruker oppdateringene.  

Ikke alle endringer i rapportdatasettet kan oppdateres automatisk i et rapportoppsettene. Noen endringer krever at du manuelt redigerer rapportoppsettet. Hvis du vil ha mer informasjon, se [Begrensninger i oppdateringen for egendefinert rapportoppsett](ui-update-report-layouts.md#UpdateLimitations).  

## <a name="to-update-one-or-more-custom-report-layouts" />Slik oppdaterer du én eller flere egendefinerte rapportoppsett

1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Rapportoppsettsvalg**, og velg deretter den relaterte koblingen.  

2.  Hvis du vil oppdatere en bestemt rapport, velger du oppsettet fra listen på siden **Valg av rapportoppsett**, og velger deretter **Oppdater oppsett**. Hvis du vil oppdatere alle egendefinerte rapportoppsett for selskapet, velger du **Oppdater alle oppsett**-handlingen.  

Hvis det ikke oppstår noen feil, brukes oppdateringene på rapportoppsettene. Hvis det oppstår feil, vises en melding som inneholder feilene. Du må deretter manuelt redigere det egendefinerte rapportoppsettet for å rette opp feilen. Hvis du vil ha mer informasjon, kan du se [Rette feil](ui-update-report-layouts.md#FixErrors).  

## <a name="to-test-custom-report-layout-updates" />Slik tester du oppdateringer for egendefinert rapportoppsett:

1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Rapportoppsettsvalg**, og velg deretter den relaterte koblingen.  

2.  På siden **Rapportoppsettsvalg** velger du handlingen **Test oppdateringer av oppsett**.  

 Endringer i rapportoppsettene testes, men brukes ikke i de faktiske rapportoppsettene. Siden **Oppdateringslogg for rapportoppsett** åpnes og viser statusen for mulige oppdateringer for hvert rapportoppsett. Hvis det er feil i et rapportoppsett, kan du åpne rapportoppsettet direkte for redigering fra meldingen for å løse eventuelle problemer. Hvis du vil ha mer informasjon, kan du se [Rette feil](ui-update-report-layouts.md#FixErrors).  

## <a name="limitations-of-the-custom-report-layout-update" /><a name="UpdateLimitations"></a> Begrensninger i oppdateringen for egendefinert rapportoppsett
 Det finnes flere typer endringer som den automatiske oppdateringen kan bruke på egendefinert rapportoppsett, for eksempel et felt som brukes i oppsettet, er fjernet fra rapportdatasettet. Den automatiske oppdateringen kan imidlertid ikke håndtere følgende endringer i et rapportdatasett.  

1.  Slettede felt, etiketter eller dataelementer.  

2.  Dupliserte feltnavn i rapportoppsettet etter at et felt har fått nytt navn i datasettet. Dette bør behandles som en utformingsfeil.  

3.  Oppgraderingsscenarier der det er flere gjentakelser i et rapportoppsett som fører til flere handlinger for å gi nytt navn i de samme feltene, etikettene eller dataelementene.  

 Hvis oppdateringsprosessen oppdager ett av disse problemene, kan ikke oppdateringen brukes. Du må rette opp problemene manuelt, for eksempel ved å redigere rapportoppsettet i Word, eller programmatisk ved hjelp av oppgraderingskodeenheter.  

## <a name="fixing-errors" /><a name="FixErrors"></a> Rette feil
 Hvis du får en feilmelding når du oppdaterer eller tester oppdateringer av rapportoppsett, må du mest sannsynlig endre rapportoppsettet for å løse problemet. Les feilmeldingen for å gjøre det enklere å finne årsaken til problemet.  

 De vanligste problemet oppstår når et felt som brukes på oppsettet, fjernes fra rapportdatasettet. I dette tilfellet vises en linje om at et element er fjernet, i feilmeldingen. Hvis du vil løse dette problemet, må du endre oppsettet og fjerne det aktuelle feltet.  

 Hvis du vil ha mer informasjon, kan du se [Opprette og endre et egendefinert rapportoppsett](ui-how-create-custom-report-layout.md#ModifyCustomLayout).  

Når du har endret oppsettet, kan du prøve å oppdatere det på nytt.  

## <a name="see-related-microsoft-training" />Se relatert [Microsoft-opplæring](/training/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also" />Se også
 [Håndtere rapportoppsett](ui-manage-report-layouts.md)  
 [Arbeid med rapporter, satsvise jobber og XMLport-er](ui-work-report.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
