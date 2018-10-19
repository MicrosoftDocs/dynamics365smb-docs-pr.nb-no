---
title: Koble fra poster til ekstern informasjon eller eksterne programmer | Microsoft-dokumentasjon
description: "Legg til en hyperkobling i et dokument eller et webområde til en bestemt post, for eksempel en kunde eller et dokument."
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: c2e70ad534a28cf5062e9e54a2dfbd3af6afaa39
ms.contentlocale: nb-no
ms.lasthandoff: 09/28/2018

---
# <a name="adding-links-to-websites-documents-or-programs-on-records"></a>Legge til koblinger i webområder, dokumenter eller programmer i poster
Du kan legge til en kobling i et eksternt dokument, et webområde eller et program i en bestemt post som kunde, dokument eller ordre. Du kan også legge til en kobling som du kan velge for å åpne en ny, tom e-post til en bestemt mottaker. Kortsiden for noen poster, for eksempel kunde- og leverandørkort, har et **Hjemmeside**-felt der du kan angi en nettadresse (URL). Du kan bruke metoden som er beskrevet i denne artikkelen, for å inkludere andre koblinger.

Et annet eksempel kan være når du mottar papirfakturaer fra leverandører. Du kan skanne og lagre dem som PDF-filer på et SharePoint-område. Deretter kan du opprette en kobling fra en kjøpsfaktura i [!INCLUDE[d365fin_md](includes/d365fin_md.md)] til den tilsvarende fakturaen på SharePoint. Du kan også opprette en kobling fra et varekort til den tilsvarende siden i leverandørens elektroniske katalog.

## <a name="to-add-a-link-on-a-record"></a>Slik legger du til en kobling i en post   

1.  Åpne posten du vil knytte koblingen til, for eksempel et kundekort eller en ordre. Hvis du vil knytte koblingen til en bestemt linje, for eksempel en kladdelinje, merker du linjen.  

2.  Velg **Koblinger** for å åpne **Koblinger**-vinduer som viser alle gjeldende koblinger som er lagt til posten.

3. Hvis du vil legge til en ny kobling, velger du **+ny**.

4.  I vinduet **Koblingsadresse** angir du

    -   Hvis du vil koble til en fil på datamaskinen eller nettverket, angir du fullstendig bane og filnavn som **C:My Documentsinvoice1.doc**.
    -   Hvis du vil koble til et webområde, angir du Internett-adressen (URL-adressen), for eksempel **www.microsoft.com**.
    -   Hvis du vil koble til et webområde, angir du Internett-adressen (URL-adressen), for eksempel **www.microsoft.com**.
    -   Hvis du vil koble til et program, angir du en bestemt streng for å åpne programmet. Hvis du for eksempel vil åpne OneNote på en bestemt side, skriver du inn **C:My Documentstest.one**. Eller hvis du vil åpne Outlook med en ny, tom e-post til et bestemt alias, skriver du inn **mailto:testalias**.  

5.  Fyll ut **Beskrivelse**-feltet med informasjon om koblingen.  

6.  Velg **Lagre**-knappen.  

## <a name="to-delete-a-link-from-a-record"></a>Slik sletter du en kobling fra en post  

Hvis du vil slette en kobling, i vinduet **Koblinger**, kan du velge **...** og deretter **Slett**.

Hvis du sletter én enkelt post, for eksempel en ordrelinje, en ordre eller en kunde, slettes alle koblingene som er knyttet til posten. Hvis du imidlertid sletter poster ved å bruke en kjørsel, for eksempel kjørselen **Slett fakturerte ordrer**, lagres koblingene i databasen. Hvis du vil slette koblingene fra databasen, kjører du kodeenheten **Slett koblinger til løse poster**. For å gjøre dette velger du ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angir **Slett koblinger til løse poster** og velger deretter den relaterte koblingen.   

<!-- ### To run delete orphaned record links  

1.  Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Data Deletion**, and then choose the related link.  

2.  In the **Data Deletion** window, choose **Tasks**, and then choose **Delete Orphaned Record Links**.  -->

## <a name="see-also"></a>Se også  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

