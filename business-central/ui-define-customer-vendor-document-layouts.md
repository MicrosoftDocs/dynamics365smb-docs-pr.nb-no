---
title: Tilordne spesielle dokumentoppsett til kunder eller leverandører | Microsoft Docs
description: Når egendefinerte rapportoppsett er definert, kan du velge dem fra kunde- og leverandørkortene for å angi at de valgte oppsettene skal brukes for dokumenter du oppretter for den aktuelle kunden eller leverandøren.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: ed8b60c5b49502251f6ab6e61d22fd860af0915f
ms.sourcegitcommit: 32bfc2acaaf3693afc9aeb86feea505fd328caa1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/19/2021
ms.locfileid: "5024541"
---
# <a name="define-document-layouts-for-customers-and-vendors"></a>Definere dokumentoppsett for kunder og leverandører
Når egendefinerte rapportoppsett er definert, kan du velge dem fra kunde- og leverandørkortene for å angi hvilke oppsett som skal brukes for ulike typer dokumenter du oppretter for den aktuelle kunden eller leverandøren. Verdien i feltet **Bruk** definerer hvilken prosess dokumentoppsettet skal brukes til, for eksempel **Purring**, **Levering** og **Bekreftelse**.

I tillegg til å definere hvilke oppsett som skal brukes for hvilket dokument, kan du spare tid når du sender dokumenter til ulike kunde- eller leverandørkontakter ved å angi at e-postadressene til bestemte kontakter skal brukes med bestemte dokumenter. Kundeutdrag vil for eksempel bli sendt til regnskapsførerkontakter, ordrer til kundens innkjøpere og bestillinger til leverandørers selgere eller kundeansvarlige.

Når du definerer et dokumentoppsett for en kunde eller en leverandør, kan du også angi e-postadressen til kontaktpersonen som må motta dokumentet. Du kan raskt gjøre dette med funksjonen **Velg e-post fra kontakter**, som automatisk filtrerer på e-postadresser som er registrert for den aktuelle kunden eller leverandøren.

Før du kan definere hvilket dokumentoppsett du vil bruke for hvilke prosesser, og hvilken kontakt du skal sende dokumentet til, må du laste alle tilgjengelige rapporter (dokumenter) fra siden **Rapportvalg**. Du kan raskt gjøre dette ved hjelp av funksjonen **Kopier fra Rapportutvalg**.

Nedenfor finner du en beskrivelse av hvordan du definerer salgsdokumentoppsett fra et kundekort. Trinnene er de samme for oppsett av kjøpsdokumenter fra et leverandørkort.

## <a name="to-enable-all-available-sales-documents-for-a-customer"></a>Slik aktiverer du alle tilgjengelige salgsdokumenter for en kunde
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kunder**, og velg deretter den relaterte koblingen.
2. Åpne kortet til kunden du vil definere dokumentoppsett per forretningsprosess for.
3. På siden **Kundekort** velger du siden **Dokumentoppsett**.
4. På siden **Dokumentoppsett** velger du handlingen **Kopier fra Rapportutvalg**.

Siden **Dokumentoppsett** for den aktuelle kunden fylles ut med alle rapportoppsettene for salg som finnes i systemet. Hvis du vil ha mer informasjon om hvor de ble opprettet, kan du se [Opprette og endre et egendefinert rapportoppsett](ui-how-create-custom-report-layout.md).

Du kan nå fortsette med å justere oversikten med alle egendefinerte rapportoppsett eller e-postadresser for kontaktene som dokumentene må sendes til.

## <a name="to-select-a-custom-report-layout-to-use-for-the-sales-document-layout"></a>Slik velger du et egendefinert rapportoppsett som skal brukes for salgsdokumentoppsettet
Hvis ett eller flere av rapportoppsettene som er definert på siden **Dokumentoppsett** for kunden, ikke har definert et egendefinert rapportoppsett, kan du raskt gjøre dette.

1. På siden **Dokumentoppsett**, på linjen for et rapportoppsett som du vil bruke et egendefinert oppsett for, velger du feltet **Beskrivelse av egendefinert oppsett**. Feltet er enten fylt ut hvis kundeoppsett allerede er valgt, eller tomt.
2. På siden **Egendefinerte rapportoppsett** velger du det spesielle dokumentoppsettet du vil bruke for den aktuelle salgsdokumenttypen. Hvis du vil ha mer informasjon, kan du se [Opprette og endre et egendefinert rapportoppsett](ui-how-create-custom-report-layout.md).

## <a name="to-set-up-which-contact-receives-which-document-layout-for-a-customer"></a>Slik oppretter du hvilken kontakt som mottar et dokumentoppsett for en kunde
Du kan spare tid når du sender dokumenter til forskjellige kunder eller leverandørkontakter, ved å angi e-postadresser for kontakter på de ulike linjene på siden **Dokumentoppsett**. Kundeutdrag kan for eksempel bli sendt til regnskapsførerkontakter, ordrer til kundens innkjøpere og bestillinger til leverandørers selgere eller kundeansvarlige.

1. På siden **Dokumentoppsett**, på linjen for rapportoppsett som du vil sende til en bestemt kontakt for kunden, velger du handlingen **Velg e-post fra kontakter**.
2. På siden **Kontakter** velger du linjen for den aktuelle kontakten, og deretter klikker du **OK**.

E-postadressen til kontakten settes nå inn på dokumentoppsettlinjen, slik at det aktuelle salgsdokumentet, for eksempel purringer, alltid sendes til den kontakten hos kunden.

## <a name="see-also"></a>Se også  
[Oppdatere egendefinerte rapportoppsett](ui-update-report-layouts.md)  
[Opprette og endre et egendefinert rapportoppsett](ui-how-create-custom-report-layout.md)  
[Importere og eksportere en egendefinert rapport eller et egendefinert dokumentoppsett](ui-how-import-and-export-report-layout.md)  
[Sende dokumenter i e-post](ui-how-send-documents-email.md)  
[Håndtere rapportoppsett](ui-manage-report-layouts.md)  
[Arbeide med rapporter, satsvise jobber og XML-porter](ui-work-report.md)  
[Arbeide med rapporter, satsvise jobber og XML-porter](ui-work-report.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]