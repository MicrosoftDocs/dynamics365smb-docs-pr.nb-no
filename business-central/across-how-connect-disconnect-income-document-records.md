---
title: Opprett innkommende dokumentposter fra dokumenter
description: Du kan lagre eksterne forretningsdokumenter ved å knytte dokumentfilene til de relaterte innkommende dokumentpostene.
author: jswymer
ms.topic: how-to
ms.search.keywords: 'electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice'
ms.date: 02/27/2024
ms.author: jswymer
ms.reviewer: jswymer
ms-service: dynamics-365-business-central
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Opprette innkommende dokumentposter direkte fra dokumenter og poster

Du kan lagre eksterne forretningsdokumenter i [!INCLUDE[prod_short](includes/prod_short.md)] ved å knytte dokumentfilene til de relaterte innkommende dokumentpostene. Hvis dokumentet, for eksempel en kjøpsfaktura, ikke ble opprettet som en innkommende dokumentpost, kan du likevel opprette og koble en innkommende dokumentpost til det senere. Du kan også knytte inngående dokumentfiler til bokførte kjøps- og salgsdokumenter og til leverandør-, kunde- og finansposter ved hjelp av faktaboksen **Inngående dokumentfiler**, for eksempel på siden **Bokførte kjøpsfakturaer** og **Leverandørposter**.

Fra sidene **Kontoplan** og **Finansposter** kan du bruke søkefunksjonen til å finne finansposter for bokførte kjøps- og salgsdokumenter som ikke har innkommende dokumentposter, og deretter sentralt koble eksisterende poster eller opprette nye med vedlagte dokumentfiler. Hvis du vil ha mer informasjon, kan du se [Finne bokførte dokumenter uten innkommende dokumentposter](across-how-find-posted-documents-without-income-document-records.md).

De følgende fremgangsmåtene viser hvordan du knytter en fil til en leverandørpost eller eksisterende kjøpsfaktura som ikke ble opprettet fra en innkommende dokumentpost. Å knytte en en fil til bokførte kjøps- eller salgsdokumenter fungerer på en lignende måte.

[!INCLUDE [incoming-doc-archived-doc](includes/incoming-doc-archived-doc.md)]

## Opprett og koble til en innkommende dokumentpost fra en kjøpsfaktura

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Kjøpsfakturaer**, og velg deretter den relaterte koblingen.
2. Velg linjen for en kjøpsfaktura du vil knytte en fil til, og velg deretter handlingen **Opprett inngående dokument fra fil**.
3. Du kan eventuelt velge linjen for en kjøpsfaktura du vil knytte en fil til, og deretter velge handlingen **Tilknytt fil**.
4. På siden **Sett inn fil** gjør du et av følgende trinn for å legge ved en fil som representerer det innkommende dokumentet:

   [!INCLUDE[file-upload](includes/file-upload.md)]


## Opprett og koble en innkommende dokumentpost fra en leverandørpost

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , skriv inn **Leverandørposter**, og velg deretter den relaterte koblingen.
2. Velg en linje for en leverandørpost du vil knytte en fil til, og velg deretter handlingen **Opprett inngående dokument fra fil**.
3. Du kan eventuelt velge en linje for en leverandørpost du vil knytte en fil til, og deretter velge handlingen **Tilknytt fil**.
4. På siden **Sett inn fil** gjør du et av følgende trinn for å legge ved en fil som representerer det innkommende dokumentet:

   [!INCLUDE[file-upload](includes/file-upload.md)]


## Fjern en tilkobling fra en innkommende dokumentpost til et bokført dokument

Du kan fjerne filvedlegg fra ikke-bokførte dokumenter når som helst ved å slette den relaterte innkommende dokumentposten. Hvis dokumentet er bokført, må du først fjerne tilkoblingen fra den innkommende dokumentposten.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Innkommende dokumenter**, og velg deretter den relaterte koblingen.
2. Velg linjen for en inngående dokumentpost som er koblet til et bokført dokument du vil fjerne, og velg deretter handlingen **Fjern referanse til post**.

Tilkoblingen til det bokførte dokumentet fjernes. Nå kan du fortsette med å koble en annen innkommende dokumentpost til det bokførte dokumentet, som beskrevet i denne artikkelen.

## Se også

[Opprett innkommende dokumentposter](across-how-create-income-document-records.md)
[Bruk OCR til å gjøre PDF- og bildefiler om til elektroniske dokumenter](across-how-use-ocr-pdf-images-files.md)
[Finn bokførte dokumenter uten innkommende dokumentposter](across-how-find-posted-documents-without-income-document-records.md)
[Innkommende dokumenter](across-income-documents.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
