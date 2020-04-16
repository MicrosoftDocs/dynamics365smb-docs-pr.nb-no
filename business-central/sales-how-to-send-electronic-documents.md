---
title: Sende elektroniske dokumenter | Microsoft-dokumentasjon
description: Lær hvordan du sender fakturaer elektronisk.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 110c81bdf6de02e16a1e1185028f6b803290f3d7
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3192665"
---
# <a name="send-electronic-documents"></a>Sende elektroniske dokumenter
Den generelle versjonen av [!INCLUDE[d365fin](includes/d365fin_md.md)] kan sende elektroniske fakturaer og kreditnotaer i PEPPOL-format, som støttes av de største leverandørene av dokumentutvekslingstjenester. En leverandør av dokumentutvekslingstjenester fordeler elektroniske dokumenter mellom handelspartnere. Hvis du vil ha støtte for andre elektroniske dokumentformater, kan du bruke rammeverket for datautveksling.  

 I den generelle versjonen av [!INCLUDE[d365fin](includes/d365fin_md.md)] er en dokumentutvekslingstjeneste forhåndskonfigurert og klar til å bli definert for firmaet. Hvis du vil ha mer informasjon, kan du se [Konfigurere en dokumentutvekslingstjeneste](across-how-to-set-up-a-document-exchange-service.md).  

 Hvis du vil sende en salgsfaktura som et elektronisk PEPPOL-dokument, velger du alternativet **Elektronisk dokument** i dialogboksen **Bokfør og send**, der du også kan konfigurere kundens standardprofil for dokumentsending. Først må du definere forskjellige hoveddata, for eksempel firmainformasjon, kunder, varer og enheter. Disse brukes til å identifisere forretningspartnere og elementer ved konvertering av data i feltene [Konfigurere sending og mottak av elektroniske dokumenter](across-how-to-set-up-electronic-document-sending-and-receiving.md).  

### <a name="to-send-an-electronic-sales-invoice"></a>Slik sender du en elektronisk salgsfaktura:  

1.  Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Salgsfakturaer**, og velg deretter den relaterte koblingen.  

2.  Opprett en ny salgsfaktura.  

3.  Når salgsfakturalinjene er klare til å bli fakturert, kan du velge handlingen **Bokfør og send**.  

     Hvis kundens standard sendingsprofil er **Elektronisk dokument**, vil den vises i dialogboksen **Bokfør og send bekreftelse**, og du trenger bare å velge **Ja**-knappen for å bokføre og sende fakturaen elektronisk i det valgte formatet.  

4.  I dialogboksen **Bokfør og send bekreftelse** velger du AssistEdit-knappen til høyre for feltet **Send dokument til**.  

5.  I dialogboksen **Send dokument til** i feltet **Elektronisk dokument** velger du **Gjennom dokumentutvekslingstjeneste**.  

6.  I **Format**-feltet velger du **PEPPOL**.  

7.  Velg **OK**-knappen. Dialogboksen **Bokfør og send bekreftelse** vises. **Elektronisk dokument (PEPPOL)** legges til i **Send dokument til**-feltet.  

8.  Velg **Ja**-knappen.  

     Salgsfakturaen bokføres og sendes til kunden som et elektronisk dokument i formatet PEPPOL.  

    > [!NOTE]  
    >  Du kan også sende en bokført salgsfaktura som et elektronisk dokument. Fremgangsmåten er den samme som beskrevet i dette emnet for ikke-bokførte salgsdokumenter. På siden **Bokført salgsfaktura** velger du **Aktivitetslogg**-handlingen for å vise statusen for det elektroniske dokumentet. Hvis du vil ha mer informasjon, kan du se **Aktivitetslogg**.  

## <a name="see-related-training-at-microsoft-learn"></a>Se relatert opplæring på [Microsoft Learn](/learn/modules/electronic-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også  
[Fakturere salg](sales-how-invoice-sales.md)  
[Definere en profil for dokumentsending](sales-how-setup-document-send-profiles.md)  
[Konfigurere sending og mottak av elektroniske dokumenter](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[Konfigurere en dokumentutvekslingstjeneste](across-how-to-set-up-a-document-exchange-service.md)  
[Definere datautvekslingsdefinisjoner](across-how-to-set-up-data-exchange-definitions.md)  
[Utveksle data elektronisk](across-data-exchange.md)  
[Generelle forretningsfunksjoner](ui-across-business-areas.md)  
