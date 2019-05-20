---
title: Kopiere og lime inn data
description: Kopier felt og rader fra Business Central-sider og lim inn et annet sted.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accessibility, shortcuts, keyboarding
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 2db4fb00567c98b1133cd031a3d7d9f1d1955626
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2019
ms.locfileid: "1250897"
---
# <a name="copying-and-pasting"></a>Kopiere og lime inn
Du kan kopiere en eller flere rader fra en oversikt eller ett enkelt felt på en side og deretter lime inn det du kopierte, på samme side, en annen side eller et eksternt dokument (som Microsoft Excel og Outlook-e-post). Kort sagt, for å kopiere trykker du CTRL+C (cmd+C i macOS) på tastaturet. For å lime inn trykker du CTRL+V (cmd+V i macOS).

Det finnes flere tastatursnarveier for å kopiere og lime inn som sparer tid når du registrerer data. Hvis du vil ha mer informasjon om disse, kan du se [Hurtigtaster](keyboard-shortcuts.md#CopyRows).

Denne artikkelen svarer på vanlige spørsmål du måtte ha om å kopiere og lime inn.  

## <a name="what-can-i-copy-and-paste"></a>Hva kan jeg kopiere og lime inn?
-   Kopier én eller flere rader i [!INCLUDE[d365fin](includes/d365fin_md.md)] til samme liste eller til en liste med identiske kolonner.
-   Kopier én eller flere rader i [!INCLUDE[d365fin](includes/d365fin_md.md)] og lim inn i Excel eller andre programmer.
-   Kopier én eller flere rader i Excel og lim inn i en [!INCLUDE[d365fin](includes/d365fin_md.md)]-liste.
-   Kopier verdien for et individuelt felt i [!INCLUDE[d365fin](includes/d365fin_md.md)] og lim inn hvor som helst.

## <a name="how-do-i-copy-rows"></a>Hvordan kopierer jeg rader?
Hvis du vil kopiere én rad, merker du den og trykk Ctrl+C.

Hvis du vil kopiere flere rader, kan du:
-   Trykke Ctrl+klikk på på annen rad eller Skift+klikk for å merke raden og alle rader i mellom. Se [Tastatursnarveier](keyboard-shortcuts.md#CopyRows) for flere mus- og tastaturkombinasjoner for å velge rader.
-   Velg ![Vis flere alternativer](media/show-more-options-icon.png "Vis flere alternativer-ikonet") i den første kolonnen i en rad, velg **Velg flere**, merk av for hver rad du vil kopiere, og trykk Ctrl+C.

## <a name="how-do-i-paste-rows"></a>Hvordan limer jeg inn rader?
Velg en tom rad, og trykk CTRL+V. Hvis du vil erstatte eksisterende rader, velger du radene og trykker CTRL+V. I dette tilfellet kan du bare lime inn samme antall rader som du har valgt.

<!-- Rows are pasted directly where your cursor is located. If you paste into an empty line, any existing subsequent lines will be moved after the pasted lines. If you paste into an existing line or lines, this will be overwritten.-->

## <a name="can-i-paste-rows-into-an-outlook-email-or-onenote"></a>Kan jeg lime inn rader i Outlook-e-post eller OneNote?
Ja. Dette limes inn som en flott formatert tabell som beholder innrykk, numerisk justering og farger, på samme måte som du ville sett det i [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="does-copy-and-paste-work-with-tiles"></a>Fungerer kopiering og innliming med fliser?
Nei. Listen må vises som rader (listevisning) for at du skal kunne kopiere og lime inn.

## <a name="in-which-lists-can-i-copy-and-paste-rows"></a>I hvilke lister kan jeg kopiere og lime inn rader?
Du kan kopiere rader i en hvilken som helst type liste, inkludert forslag, faktabokser eller lister som er bygd inn på en side (for eksempel linjer i en ordre). For å kunne lime inn rader må listen imidlertid kunne redigeres.

I enkelte sider kan programmetutformingen forhindre deg fra å lime inn rader. Kontakt systemansvarlig eller programvareutvikleren for å endre den [redigerbare egenskapen](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/properties/devenv-editable-property) på siden eller [PasteIsValid-egenskapen](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/properties/devenv-pasteisvalid-property) i kildetabellen.

## <a name="on-which-clients-is-copy-and-paste-available"></a>På hvilke klienter er kopiering innliming tilgjengelig?
Kopiering og innliming er tilgjengelig i nettleseren eller [!INCLUDE[d365fin](includes/d365fin_md.md)]-appen for Windows 10.

## <a name="what-is-the-maximum-number-of-rows-that-can-be-copied"></a>Hva er maksimalt antall rader som kan kopieres?
Du kan kopiere så mange rader du har rullet inn i visningen. For eksempel hvis du vil kopiere alle 1000 rader på en side, må du først rulle nederst på siden og vente til radene vises, før du kopierer. Det maksimale antallet rader som du kan kopiere, begrenses bare av minnet på enheten.

## <a name="must-i-have-the-exact-same-number-of-columns-when-pasting-rows"></a>Må jeg ha nøyaktig samme antall kolonner når jeg limer inn rader?
Ja. Om du kopierer fra [!INCLUDE[d365fin](includes/d365fin_md.md)], fra Excel eller en annen tabellkilde, må radene du limer inn ha nøyaktig antall tilsvarende kolonner – hverken færre eller flere.

## <a name="why-do-i-get-errors-when-pasting-rows"></a>Hvorfor får jeg feil når jeg limer inn rader?
Når du limer inn i [!INCLUDE[d365fin](includes/d365fin_md.md)], kontrolleres hver rad slik at verdiene i hver kolonne er gyldig. Hvis en kolonne inneholder en verdi som ikke er gyldig, stopper innlimingen, og det vises en feilmelding. Kontroller at kolonnene har gyldige verdier før du limer dem inn, for å unngå dette.


## <a name="see-also"></a>Se også
[Hjelpefunksjoner](ui-accessibility.md)  
[Komme i gang](product-get-started.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Vanlige spørsmål](across-faq.md)  
