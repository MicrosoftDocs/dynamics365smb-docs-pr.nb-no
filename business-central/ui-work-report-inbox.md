---
title: Del og eksporter rapporter med rapportinnboksen
description: 'Bruk siden Rapportinnboks til å laste ned, dele og eksportere rapporter i Business Central.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'task, process, report, print, schedule, save, Excel, PDF, dataset, export, report inbox, onedrive,'
ms.search.form: 680
ms.date: 08/08/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="share-and-export-reports-with-the-report-inbox"></a>Del og eksporter rapporter med rapportinnboksen

Siden **Rapportinnboks** viser planlagte rapporter som er generert av brukeren i [!INCLUDE[prod_short](includes/prod_short.md)], og kan bare brukes til å få tilgang til de genererte rapportene, men også til å dele og åpne filene i OneDrive for Business.

> [!TIP]
> Følgende handlinger er også tilgjengelige i delen **Rapportinnboks** i rollesenteret. Hvis delen ikke vises i ditt grensesnitt, kan du lære hvordan du tilpasser rollesenteret her: [Tilpass arbeidsområdet](ui-personalization-user.md).

## <a name="download-generated-reports"></a>Last ned genererte rapporter

Hvis du vil lagre tidligere rapporter, åpner du tabellen **Rapportinnboks** ved å følge denne fremgangsmåten:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Rapportinnboks**, og velg deretter den relaterte koblingen.  
2. Velg ønsket rapport på **Rapportinnboks**-siden.

> [!NOTE]
> Siden viser ikke tidligere rapporter generert ved hjelp av handlingen **Skriv ut** eller lagret som en fil på **Rapporter**-menyen.
>
> De genererte filene lagres i formatet som er definert ved planlegging av rapporten, og kan endres på siden **Prosjektkøposter**, sammen med regelmessighet og andre innstillinger. Lær hvordan du endrer rapportfilformat og angir flere alternativer under [Administrer planlagte, gjentatte rapporter](ui-work-report.md#manage-scheduled-recurring-reports).

## <a name="open-generated-reports-in-onedrive"></a>Åpne genererte rapporter i OneDrive

Hvis du vil eksportere rapportfilen til Microsoft OneDrive for Business, merker du rapporten på siden **Rapportinnboks** og velger **Åpne i OneDrive**-handlingen. Rapporten blir da kopiert til [!INCLUDE[prod_short](includes/prod_short.md)]-mappen i OneDrive og åpnet i et nytt nettleservindu, der du kan skrive ut og håndtere dokumentfilen.

> [!IMPORTANT]
>
> Rapporter angitt til å utløpe på **Planlegg en rapport**-side og kopiert til OneDrive, fjernes ikke automatisk fra den delte mappen.

## <a name="share-scheduled-reports"></a>Del planlagte rapporter

Det er også mulig å dele rapporter med samarbeidspartnere på **Rapportinnboks**-siden. Velg rapporten og velg handlingen **Del**. På siden **Send kobling** velger du hvem som kan åpne filen, definerer redigeringstillatelser, og deretter velger du **Send** til å sende en kobling for å få tilgang til den lagrede rapporten.

> [!NOTE]
> Hvis du vil ha mer informasjon om OneDrive-integrering og -funksjoner på [!INCLUDE[prod_short](includes/prod_short.md)], inkludert førstegangsoppsett og alternativer for å håndtere konflikter ved filnavn, kan du lese artikkelen [Åpne og del filer i OneDrive](across-share-onedrive.md).
>
> Når du bruker **Del**-handlingen, blir den genererte rapportfilen tilgjengelig for andre brukere bare i OneDrive for Business, og den planlagte rapporten vises ikke i **rapportinnboksen**.

## <a name="see-also"></a>Se også

[Kjør og skriv ut rapporter](ui-work-report.md)  
[Tilgjengelige rapporter i [!INCLUDE[prod_short](includes/prod_short.md)]](reports-available-reports.md)  
[Bruk rapporter i daglig arbeid](reports-use-reports.md)  
[Oversikt over forretningsanalyse og rapportering](reports-bi-reporting.md)  
[Konfigurere skrivere](ui-specify-printer-selection-reports.md)  
[Arbeid med datoer og klokkeslett i kalenderen](ui-enter-date-ranges.md)  
[Administrer rapport- og dokumentoppsett](ui-manage-report-layouts.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] og OneDrive-integrering](across-onedrive-overview.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
