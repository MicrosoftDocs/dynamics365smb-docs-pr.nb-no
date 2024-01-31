---
title: Utvikling av rapportoppsett og datasett
description: Gir en oversikt over Business Central-data.
author: kennieNP
ms.topic: conceptual
ms.devlang: al
ms.reviewer: bholtorf
ms.search.keywords: feature overview
ms.date: 02/03/2022
ms.author: kepontop
ms.service: dynamics-365-business-central
---

# Utvikling av Business Central-rapportoppsett og -datasett

En rapport i [!INCLUDE[prod_short](includes/prod_short.md)] består av et rapportobjekt som definerer _datasettet_ for rapporten (hvilke data som er tilgjengelige) og en rekke _rapportoppsett_ (hvordan data presenteres).  

## Utvikling av rapportoppsett

Kanskje du vil endre eksisterende rapportoppsett i [!INCLUDE[prod_short](includes/prod_short.md)]? Avhengig av teknologien som brukes for oppsettet, er det noe du kanskje kan gjøre (Excel og kanskje også Word-oppsett), eller du trenger kanskje en utvikler for å gjøre det (Pixel-Perfect RDLC-oppsett).

| Hvis du vil | Se |
|--|--|
| Finn ut mer om de forskjellige oppsettstypene (Word, Excel og RDLC) | [Oppsettyper (Word, Excel og RDLC)](ui-manage-report-layouts.md) |
| Finn ut mer om hvordan du kan opprette et nytt rapportoppsett. | [Opprett et nytt oppsett](ui-how-create-custom-report-layout.md) |
| Finn ut mer om hvilke skrifter som er installert i nettversjonen av [!INCLUDE[prod_short](includes/prod_short.md)] slik at de kan brukes i rapportoppsett. | [Bruk skrifter i oppsett](ui-fonts.md) |
| For å finne ut hvordan du arbeider med Word-oppsett. | [Arbeid med Word-oppsett](ui-how-add-fields-word-report-layout.md) |
| For å finne ut hvordan du importerer/eksporterer oppsettfiler. | [Importer/eksporter et oppsett](ui-how-import-and-export-report-layout.md) |
| For å finne ut hvordan du oppdaterer en oppsettdefinisjon i [!INCLUDE[prod_short](includes/prod_short.md)] med en ny oppsettsfil. | [Importer/eksporter et oppsett](ui-how-import-and-export-report-layout.md) |
| For å finne ut hvordan du endrer standardoppsettet for en rapport. | [Endre standardoppsettet](ui-how-change-layout-currently-used-report.md) |
<!-- | For å finne ut hvordan du arbeider med Excel-oppsett | [Arbeid med Excel-oppsett](ui-how-add-fields-word-report-layout.md) | -->

## Utvikling av rapportdatasett

 Hvis du vil endre datasettdefinisjonene som definerer hvilke data som er tilgjengelige i rapporten, trenger du en utvikler som vet om AL-programmeringsspråket og verktøyene til å utvikle rapportobjekter og rapportutvidelser.

| Hvis du vil | Se |
|--|--|
| Finn ut hvordan du program rapporterer i AL | [Veiledning for rapportutvikling](/dynamics365/business-central/dev-itpro/developer/devenv-reports) |
| Finn ut hvordan får rapporter til å yte | [Veiledning for justering av rapportytelse](/dynamics365/business-central/dev-itpro/performance/performance-developer#writing-efficient-reports) |

## Se også

[Oversikt over Business Intelligence og rapportering](reports-use-reports.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]