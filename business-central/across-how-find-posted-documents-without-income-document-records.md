---
title: Finne bokførte dokumenter uten innkommende dokumenter
description: Du kan søke etter finansposter for bokførte kjøps- og salgsdokumenter som ikke har inngående elektroniske dokumenter, for eksempel importerte fakturaer.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/14/2022
ms.author: edupont
ms.openlocfilehash: ad50260df068d38cb8266e04434eb4faf4d052f3
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/29/2022
ms.locfileid: "9076048"
---
# <a name="find-posted-documents-without-incoming-document-records"></a>Finne bokførte dokumenter uten innkommende dokumentposter

Fra sidene **Kontoplan** og **Finansposter** kan du bruke søkefunksjonen til å finne finansposter for bokførte kjøps- og salgsdokumenter som ikke har innkommende dokumentposter, og deretter sentralt koble eksisterende poster eller opprette nye med vedlagte dokumentfiler.

## <a name="to-find-posted-documents-without-incoming-document-records"></a>Slik finner du bokførte dokumenter uten innkommende dokumentposter:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Kontoplan** og velger deretter den relaterte koblingen.
2. Velg en linje for en finanskonto som du vil vise bokførte kjøps- og salgsdokumenter for uten innkommende dokumentposter, og velg deretter handlingen **Bokførte dokumenter uten inngående dokument**.
3. Du kan også velge handlingen **Poster**.
4. På siden **Finansposter** velger du handlingen **Bokførte dokumenter uten inngående dokumenter**.

Siden **Bokførte dokumenter uten innkommende dokument** åpnes med bokførte kjøps- og salgsdokumenter uten innkommende dokumentposter representert av finansposter på finanskontoen som du åpnet siden for. Siden kan vise maksimalt 1000 linjer. Som standard inneholder derfor feltet **Datofilter** et filter som begrenser linjene til poster med bokføringsdatoer fra begynnelsen av regnskapsperioden til arbeidsdatoen.

## <a name="to-connect-found-documents-to-existing-incoming-document-records"></a>Slik kobler du dokumenter som blir funnet, til eksisterende innkommende dokumentposter:

1. På siden **Bokførte dokumenter uten inngående dokument** velger du linjen for et bokført dokument du vil koble til en eksisterende innkommende dokumentpost, og deretter velger du handlingen **Velg inngående dokument**.
2. På siden **Inngående dokumenter** velger du den innkommende dokumentposten som du vil koble til det bokførte dokumentet som ble funnet, og deretter velger du **OK**-knappen.
3. På siden **Bokførte dokumenter uten inngående dokument** er den valgte inngående dokumentposten nå koblet til det bokførte dokumentet, som du kan se i faktaboksen **Filer for inngående dokument**.

Hvis en relevant innkommende dokumentpost ikke finnes på siden **Inngående dokumenter**, kan du opprette den. Hvis du vil ha mer informasjon, kan du se [Opprette innkommende dokumentposter](across-how-create-income-document-records.md).

## <a name="see-related-training-at-microsoft-learn"></a>Se relatert opplæring på [Microsoft Learn](/learn/modules/incoming-documents-dynamics-365-business-central/)

## <a name="see-also"></a>Se også

[Opprett innkommende dokumentposter](across-how-create-income-document-records.md)
[Bruk OCR til å gjøre PDF- og bildefiler om til elektroniske dokumenter](across-how-use-ocr-pdf-images-files.md)
[Opprett innkommende dokumentposter direkte fra dokumenter og enheter](across-how-connect-disconnect-income-document-records.md)
[Innkommende dokumenter](across-income-documents.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]