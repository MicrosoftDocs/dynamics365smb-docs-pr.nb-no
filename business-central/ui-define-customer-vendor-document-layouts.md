---
title: Tildel dokumentoppsett til kunder eller leverandører
description: Bruk dokumentoppsett til å kontrollere utseendet og formatet til dokumenter som fakturaer og ordrer du sender til kunder og leverandører.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '21, 9650'
ms.date: 07/05/2024
ms.service: dynamics-365-business-central
---
# <a name="define-document-layouts-for-customers-and-vendors"></a>Definer dokumentoppsett for kunder og leverandører

Dokumentoppsett bruker rapportoppsett til å definere utseendet til dokumenter du sender til kunder og leverandører. Business Central tilbyr standardoppsett, men du kan også skreddersy egendefinerte oppsett for hver av forretningspartnerne dine. Hvis du vil ha mer informasjon, kan du se [Opprette og endre et egendefinert rapportoppsett](ui-how-create-custom-report-layout.md). Du velger standard og egendefinerte dokumentoppsett fra kunde- og leverandørkort ved å velge handlingen **Dokumentoppsett**. Verdien i **Bruk**-feltet definerer prosessen som dokumentoppsettet brukes for. For kunder kan du for eksempel bruke typene **Purring**, **Levering** og **Bekreftelse** for dokumentoppsett.

Ved hjelp av dokumentoppsett kan du også spare tid når du sender dokumenter til kunde- eller leverandørkontakter via e-post. For hvert oppsett du tilordner til kunden eller kontakten, kan du angi en eller flere e-postadresser for kontakter. Du kan for eksempel sende en faktura til kundens kjøps- og lagerkontakter. Det er enkelt å legge til e-postadresser for kontakter. Med **·**  handlingen Velg Send e-post fra kontakter **på Dokumentoppsett-siden** kan du velge fra en liste over kontakt-e-postadressene du registrerte for kunden eller leverandøren. Du kan også legge til e-postadresser manuelt. Hvis du skriver inn flere adresser, skiller du dem med et semikolon og legger ikke til mellomrom mellom adressene.

Før du kan definere hvilket dokumentoppsett du vil bruke for hvilke prosesser, og hvilken kontakt du skal sende dokumentet til, må du laste alle tilgjengelige rapporter (dokumenter) fra siden **Rapportvalg**. Du kan raskt laste inn dokumentene ved hjelp av handlingen **Kopier fra rapportvalg** på siden **Dokumentoppsett**.

Trinnene nedenfor beskriver hvordan du definerer salgsdokumentoppsett fra siden **Kundekort**. For leverandører er trinnene de samme fra siden **Leverandørkort**.

## <a name="to-load-the-standard-document-layouts-for-sales-documents-for-a-customer"></a>Slik laster du inn standard dokumentoppsett for salgsdokumenter for en kunde

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Kunder** og velger den relaterte koblingen.
2. Åpne siden **Kundekort** for kunden, og velg deretter handlingen **Dokumentoppsett**.
3. På siden **Dokumentoppsett** velger du handlingen **Kopier fra Rapportutvalg**.

Siden **Dokumentoppsett** viser alle oppsett som er tilgjengelige for salgsdokumenter. 

## <a name="to-select-a-custom-report-layout-to-use-for-the-sales-document-layout"></a>Slik velger du et egendefinert rapportoppsett som skal brukes for salgsdokumentoppsettet

Fremgangsmåten nedenfor forutsetter at du allerede har et egendefinert rapportoppsett for dokumenttypen. Hvis du ikke allerede har et egendefinert rapportoppsett, må du opprette et først. Hvis du vil ha mer informasjon, kan du se [Opprette og endre et egendefinert rapportoppsett](ui-how-create-custom-report-layout.md).

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Kunder** og velger den relaterte koblingen.
2. Åpne siden **Kundekort** for kunden, og velg deretter handlingen **Dokumentoppsett**.
3. På siden **Dokumentoppsett**, på linjen for et rapportoppsett som du vil bruke et egendefinert oppsett for, velger du feltet **Beskrivelse av egendefinert oppsett**.

   > [!TIP]
   > Som standard er feltet Beskrivelse av egendefinert oppsett skjult. Hvis feltet ikke er tilgjengelig, kan du tilpasse siden for å legge den til. Hvis du vil tilpasse siden, velger du Innstillinger-ikonet :::image type="content" source="media/ui-experience/settings_icon_small.png" alt-text="."::: -ikonet, og velg **deretter Tilpass**. Hvis du vil lære mer om hvordan du tilpasser sider, kan du gå til [Tilpasse arbeidsområdet](ui-personalization-user.md).

1. På siden **Egendefinerte rapportoppsett** velger du dokumentoppsettet du vil bruke for salgsdokumenttypen. Hvis du vil ha mer informasjon, kan du se [Opprette og endre et egendefinert rapportoppsett](ui-how-create-custom-report-layout.md).

## <a name="to-specify-which-contact-receives-which-document-layout-for-a-customer"></a>Slik angir du hvilken kontakt som skal motta hvilket dokumentoppsett for en kunde:

Hvis du vil spare tid når du sender dokumenter til kunde- og leverandørkontakter via e-post, angir du e-postadressene i dokumentoppsett. Du kan for eksempel alltid sende kundeutdrag til regnskapskontaktene og salgsordrene til innkjøperne, eller bestillinger til leverandørselgere.

1. På siden **Dokumentoppsett**, på linjen for rapportoppsett som du vil sende til en bestemt kontakt for kunden, velger du handlingen **Velg e-post fra kontakter**.
2. På siden **Kontakter** velger du en eller flere kontakter, og deretter klikker du på **OK**.

## <a name="see-also"></a>Se også

[Oppdater egendefinerte rapportoppsett](ui-update-report-layouts.md)  
[Opprette og endre et egendefinert rapportoppsett](ui-how-create-custom-report-layout.md)  
[Importere og eksportere en egendefinert rapport eller et egendefinert dokumentoppsett](ui-how-import-and-export-report-layout.md)  
[Send dokumenter i e-post](ui-how-send-documents-email.md)  
[Håndtere rapportoppsett](ui-manage-report-layouts.md)  
[Arbeid med rapporter, satsvise jobber og XMLport-er](ui-work-report.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
