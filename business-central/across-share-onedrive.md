---
title: Åpne Business Central-filer i OneDrive
description: Finn ut hvordan du kan dele Business Central-data via OneDrive for Business.
author: jswymer
ms.topic: conceptual
ms.workload: na
ms.search.keywords: null
ms.date: 08/03/2022
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# Åpne og dele Business Central-filer i Microsoft OneDrive

[!INCLUDE[prod_short](includes/prod_short.md)] gjør det enkelt å lagre, behandle og dele filer med andre personer via Microsoft OneDrive for Business. På de fleste sider der filer er tilgjengelige, for eksempel rapportinnboksen eller når filer er knyttet til poster, finner du handlingene **Åpen i OneDrive** og **Del**.


:::image type="content" source="media/onedrive-overview-report-inbox-w-outline.png" alt-text="Handlingene Åpne i OneDrive og Del for rapporter":::


:::image type="content" source="media/one-drive-attachments-w-outline.png" alt-text="Handlingene Åpne i OneDrive og Del for vedlegg":::


## Åpne i OneDrive

Handlingen **Åpne i OneDrive** kopierer filen til OneDrive og åpner deretter filen i en app som Microsoft Excel online, online, Microsoft Word online eller Microsoft PowerPoint online. 

<!--## Working with different types of files-->

Når du velger **Åpne i OneDrive**, identifiserer [!INCLUDE[prod_short](includes/prod_short.md)] Excel-, Word- og PowerPoint-filer og åpner dem i nettprogrammene, det vil si Excel online, Word online og PowerPoint online. 

Ved hjelp av de elektroniske versjonene av disse programmene kan du sette inn merknader, redigere og samarbeide med andre uten å forlate webleseren.

For andre populære filtyper, for eksempel PDF-filer, tekstfiler og bilder inneholder OneDrive filvisningsprogrammer som tilbyr funksjoner for utskrift, deling og mer. Hvis en fil ikke kan vises i OneDrive, kan det hende du blir bedt om å laste den ned.

## Del

Handlingen **Del** kopierer filen til OneDrive slik at du kan se hvem du allerede har delt den med, og dele filen med andre. Når du velger **Del**-handlingen, åpnes neste side.

:::image type="content" source="media/share-to-onedrive-dialog-v2.PNG" alt-text="Del fil i OneDrive":::

Hvis du er vant med OneDrive, kan du gjenkjenne siden det refereres til over. Du vuk se to alternativer for deling av filen: **Send kobling** og **Kopier kobling**.

- **Send kobling** lar deg dele filene med bestemte personer. Personene du deler filen med, får en e-postmelding med en kobling til filen. Filen vil også vises i delen **Delt** i OneDrive. Begynn med å skrive inn e-postadresser eller kontaktnavn i feltet **Navn, gruppe eller e-post**. Ta med en melding under **Navn, gruppe eller e-post** hvis du vil.

  > [!TIP]
  > Hvis du vil skrive meldingen i Outlook, velger du **Outlook**-knappen. Koblingen settes inn i en kladde-e-post, og alle du angir å dele med, vil være i **Til**-listen. Med dette alternativet kan du redigere e-post ved hjelp av alle funksjonene i Outlook, blant annet formateringstekst, legge til andre vedlegg, sette inn bilder eller tabeller og legge til Kopi- eller Blindkopi-mottakere.

- **Kopier kobling** kopierer en filkobling du kan bruke til å dele filen gjennom programmer som Facebook, Twitter eller e-post. 

Før du sender eller kopierer en filkobling, må du angi tillatelsesfilen du vil at folk skal ha. Du kan se nåværende innstilling under **Send kobling** eller **Kopier kobling**. I de fleste tilfeller vil det være **Alle med koblingen kan redigere**, avhengig av administratorinnstillingene. Hvis du vil endre tillatelsene, merker du koblingen og gjør endringer på siden **Koblingsinnstillinger**.

Delingsfunksjonen i Business Central er basert på OneDrive. Lær mer om OneDrive-deling og -tillattelser på [Dele OneDrive-filer og -mapper](https://support.microsoft.com/en-us/office/share-onedrive-files-and-folders-9fcc2f7d-de0c-4cec-93b0-a82024800c07).

> [!NOTE]
> Handlingen **Del** er ikke tilgjengelig i Business Central-appen for mobilenheter.

## Førstegangs pålogging fra Business Central

Når du bruker handlingen **Åpne i OneDrive** eller **Del** for første gang, gjør [!INCLUDE[prod_short](includes/prod_short.md)] følgende:

1. Åpner siden **Se gjennom vilkårene**. Les siden, og velg deretter **Godta** for å fortsette hvis du godtar vilkårene.
2. Oppretter en mappe med navnet [!INCLUDE[prod_short](includes/prod_short.md)] i OneDrive. 
3. I [!INCLUDE[prod_short](includes/prod_short.md)]-mappen opprettes det en mappe med samme navn som selskapet du arbeider i. Hvis du arbeider i flere enn ett selskap, oppretter [!INCLUDE[prod_short](includes/prod_short.md)] en mappe for hvert selskap du arbeider med, når du bruker handlingen **Åpne i OneDrive** og **Del**. 
4. Lagrer en kopi av filen du valgte i selskapsnavnmappen, og åpner deretter filen. 

Neste gang du bruker **Åpne i OneDrive** eller **Del**-handlingen, kopierer og åpner [!INCLUDE[prod_short](includes/prod_short.md)] bare filen. 

## Behandle flere kopier av en fil

Når du velger **Åpne i OneDrive** eller **Del**, kopieres filen fra [!INCLUDE[prod_short](includes/prod_short.md)] til mappen i OneDrive. Hvis du redigerer filen i OneDrive, vil den være annerledes enn [!INCLUDE[prod_short](includes/prod_short.md)]-filen. Hvis du vil oppdatere [!INCLUDE[prod_short](includes/prod_short.md)] med den siste filversjonen, fjerner du den eksisterende filen fra [!INCLUDE[prod_short](includes/prod_short.md)], og laster du opp den siste kopien.

Hvis det allerede finnes en fil med samme navn i OneDrive, får du følgende valg:

- **Bruk eksisterende**

  Dette alternativet åpner eller deler filen som allerede er lagret OneDrive, i stedet for å kopiere filen fra Business Central.
  
- **Erstatt**
  
  Dette alternativet erstatter den eksisterende filen i OneDrive med filen du valgte fra Business Central. Den opprinnelige filen går ikke tapt, du kan vise og gjenopprette den ved å bruke versjonsloggen i OneDrive. Lære mer om å [Gjenopprette en tidligere versjon av en fil som er lagret i OneDrive](https://support.microsoft.com/office/restore-a-previous-version-of-a-file-stored-in-onedrive-159cad6d-d76e-4981-88ef-de6e96c93893).

- **Behold begge**

  Dette alternativet beholder den eksisterende filen som den er, og lagrer filen du valgte fra Business Central, med et annet navn. Det nye navnet ligner på det eksisterende navnet, med unntak av suffiksnummeret, for eksempel "Varer (2). xlsx".

## Om Business Central-mappen på OneDrive

Mappen og innholdet er private helt til du bestemmer deg for å dele det med andre. Du kan for eksempel velge å dele innhold med en eller flere av kollegene dine, eller til og med personer utenfor organisasjonen. 

Du får tilgang til OneDrive fra **Mine innstillinger**-siden ved å velge koblingen i **Skylagring**-feltet. Lær mer ved [Dele OneDrive-filer og -mapper](https://support.microsoft.com/en-us/office/share-onedrive-files-and-folders-9fcc2f7d-de0c-4cec-93b0-a82024800c07).

:::image type="content" source="media/my-settings-cloud-storage.PNG" alt-text="Skylagring-feltet i Mine innstillinger":::

<!--## Extending the Connection to OneDrive
You can create an extension and connect it to... For more information, see...-->

## Se også

[Business Central og OneDrive-integrering](across-onedrive-overview.md)  
[Administrere OneDrive-integrering med Business Central](admin-onedrive-integration.md)  
[Vanlige spørsmål om OneDrive](admin-onedrive-faq.md)
