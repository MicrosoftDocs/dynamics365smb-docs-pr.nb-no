---
title: Grunnleggende rapporter og dokumenter gir rask start
description: 'Business Central tilbyr innebygde maler for rapporter og dokumenter, med mange tilpasningsalternativer for å tilpasse dem til selskapets behov.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: quickstart
ms.search.form: null
ms.date: 05/17/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Grunnleggende rapporter og dokumenter gir rask start

For å tilpasse [!INCLUDE[prod_short](includes/prod_short.md)] til bedriftens behov kan du angi og bruke rapporter og egendefinerte dokumenter som er egnet for forretningens prosesser og visuell identitet.

## Legg til selskapslogoen på dokumenter

[!INCLUDE[prod_short](includes/prod_short.md)] har maler angitt til å bruke selskapets logo for å spare tid på å tilpasse dokumenter som fakturaer, ordrer og oppgaver.

1. Velg ikonet ![tannhjulikonet for å åpne Innstillinger-menyen.](media/ui-experience/settings_icon_small.png) velg handlingen **Selskapsopplysninger**.
2. Velg handlingen **Bilde** og deretter **Velg**.
3. Velg bildefilen på enheten.

Når bildet vises i **Bilde-feltet, kan du lukke siden Selskapsopplysninger**  **·** .

## Kjør rapporter

Rapporter organiserer informasjon fra ulike kilder i [!INCLUDE[prod_short](includes/prod_short.md)] og presenterer den på en lesbar måte som lett kan skrives ut eller deles. Rapporter kan finnes på sidene de er kontekstmessig tilknyttet. **Varer**-siden viser for eksempel rapporter som er knyttet til lagernivåer, kjøp, salg og annet.

1. Åpne siden som er knyttet til den aktuelle rapporten, for eksempel **Varer**-siden.
2. Velg rapporten **Vare – topp 10-liste** på **Rapporter**-menyen.
3. På rapportforespørselssiden definerer du filtre for å begrense datointervallet eller endre referanseenheten som brukes i rapporten.
4. Velg **Skriv ut**-handlingen, og følg enhetens utskriftstrinn.
    1. Du kan eventuelt velge **Forhåndsvis**-handlingen hvis du vil vise rapporten på skjermen.

Lær mer om filtrering av data, planlegging av rapporter med mer under [Kjør og skriv ut rapporter](ui-work-report.md).

## Lagre rapporter som PDF-, Excel- eller Word-dokumenter

Du kan raskt dele rapporter ved å lagre [!INCLUDE[prod_short](includes/prod_short.md)]-rapporter direkte i PDF-, Microsoft Excel- eller Microsoft Word-dokumenter.

1. Gjenta trinn 1 til 3 fra delen [Kjør rapporter](#run-reports) ovenfor.
2. Velg handlingen **Send til**.
3. Velg filtypen, og velg deretter **OK**.
r Den genererte rapportfilen lagres automatisk i nettleseren nedlastingsmappe.

### Endre rapport- og dokumentoppsett

[!INCLUDE[prod_short](includes/prod_short.md)] leveres med mange innebygde oppsett for rapporter og andre genererte dokumenter, for eksempel salgsfakturaer. Du kan bruke programmer som Microsoft Word eller Excel til å redigere oppsettsmalene for dokumenter og rapporter, som beskrevet i følgende eksempel:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Rapportoppsett**, og velg deretter den relaterte koblingen.
2. På siden **Rapportoppsett** velger du handlingen **Søk** for å velge *StandardSalesInvoice.docx*-oppsettet, og deretter velger du handlingen **Eksporter oppsett** for å laste ned oppsettsmalfilen.

    Et Word-dokument lagres på enheten med samme filnavn som vises på siden **Rapportoppsett**.
3. Åpne oppsettfilen i Microsoft Word, og rediger dokumentet, for eksempel ved å flytte datofeltet (*DocumentDate*) eller logoen eller ved å endre skriftstørrelsene. Lagre deretter filen.
4. Velg handlingen **Nytt oppsett** på siden **Rapportoppsett**.
5. På siden **Legg til nytt oppsett for en rapport** skriver du inn et navn og en beskrivelse i feltene **Oppsettnavn** og **Beskrivelse** for å gjøre oppsettet lett å finne.
6. Velg alternativet **Word** i feltet **Formatalternativer**, og velg deretter **OK**.
7. På siden **Velg Word-oppsett** velger du **Velg** for å åpne den redigerte oppsettfilen på enheten.
8. Test det nye oppsettet ved å velge **Kjør rapport**-handlingen.

Lær mer om hvordan du tilpasser rapporter og dokumenter til forretningsbehov i [Rapport- og dokumentoppsett](ui-manage-report-layouts.md).

## Se også

[Bruk rapporter i daglig arbeid](reports-use-reports.md)  
[Tilgjengelige rapporter i [!INCLUDE[prod_short](includes/prod_short.md)]](reports-available-reports.md)  
[Dokumentrapportvalg](across-report-selections.md)  
[Hurtigstart for Business Central](quick-start-business-central.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
