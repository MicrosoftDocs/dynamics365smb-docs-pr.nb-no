---
title: Konfigurer e-postskrivere
description: Beskrivelse av Slik gjør du det
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 01/26/2023
ms.custom: bap-template
---
# <a name="set-up-email-printers" />Konfigurer e-postskrivere

Denne artikkelen forklarer hvordan du konfigurerer e-postaktiverte skrivere i [!INCLUDE[prod_short](includes/prod_short.md)]. Med disse skriverne sender [!INCLUDE[prod_short](includes/prod_short.md)] utskriftsjobber til skriveren ved å bruke e-postadressen til skriveren.

> [!TIP]
> Gå til [Oversikt over utskriftsbehandling](admin-printer-setup-overview.md) for å finne ut mer om andre skrivermuligheter. 

## <a name="prerequisites" />Forutsetninger

- Lanseringsbølge 1 eller nyere for [!INCLUDE[prod_short](includes/prod_short.md)] 2020
- Utvidelsen **Sende til e-postskriver** blir installert

    Denne utvidelsen er installert som standard. Finn ut mer om å installere utvidelser under [Installer og avinstaller utvidelser i Business Central](ui-extensions-install-uninstall.md).
- E-postfunksjonalitet er konfigurert.

   Finn ut mer under [Definer e-post](admin-how-setup-email.md).

## <a name="add-an-email-printer" />Legg til en e-postskriver

Siden **Utskriftsbehandling** viser skriverne som for øyeblikket er konfigurert. På denne siden får du også tilgang til siden **Innstillinger** for hver skriver for å redigere et eksisterende oppsett eller konfigurere en ny skriver.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Utskriftsbehandling**, og velg deretter den relaterte koblingen.
2. Velg **E-postutskrift**, og velg deretter **Legg til en e-postskriver**.
3. Fyll ut de nødvendige feltene på siden **Innstillinger for e-postskriver**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > Du må velge riktig papirstørrelse manuelt for en skriver, ettersom ingen lokale skrivere eller brukerinnstillinger kan lagres.
    >
    > Vær oppmerksom på at utvidelsen for e-postskriver er satt til papirstørrelsen **A4** som standard, noe som for eksempel ikke passer i Nord-Amerika.

## <a name="privacy-notice" />Personvernerklæring

Hvis du bruker utvidelsen E-postskriver, vil alle eller enkelte utskriftsjobber bli sendt til e-postadressen du har konfigurert for skriveren. Det anbefales på det sterkeste at en unik e-post-ID knyttes til en skriverenhet med bare de offisielle tjenestene fra maskinvareprodusenten, for eksempel HP ePrint, KonicaMinolta EveryonePrint eller Epson E-Mail Printing.

Ta alle nødvendige forholdsregler for personvern, inkludert å sørge for at utskriftsløsningen for e-post har riktig konfigurerte tillatelser, personverninnstillinger og oppbevaringspolicyer. Det er ditt ansvar å oppgi en riktig, bekreftet og fungerende e-postadresse. Finn ut mer under [Microsofts personvernerklæringen](https://privacy.microsoft.com/privacystatement).

## <a name="next-steps" />Neste trinn

[Konfigurer standardskrivere](ui-specify-printer-selection-reports.md)

## <a name="see-also" />Se også

[Oversikt over utskriftsbehandling](admin-printer-setup-overview.md)  
[Konfigurer skrivere for Universell utskrift](admin-printer-setup-universal-print.md)
[Skriv ut en rapport](ui-work-report.md#PrintReport)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Kjøre kjørsler](ui-how-run-batch-jobs.md)  
