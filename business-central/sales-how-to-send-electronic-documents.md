---
title: Sende elektroniske dokumenter
description: Lær hvordan du bruker Business Central til å sende elektroniske fakturaer og kreditnotaer i PEPPOL-format.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/23/2021
ms.author: edupont
---
# <a name="send-electronic-documents"></a><a name="send-electronic-documents"></a><a name="send-electronic-documents"></a>Sende elektroniske dokumenter

Den generelle versjonen av [!INCLUDE[prod_short](includes/prod_short.md)] kan sende elektroniske fakturaer og kreditnotaer i PEPPOL-format, et format som de største leverandørene av dokumentutvekslingstjenester støtter. En leverandør av dokumentutvekslingstjenester fordeler elektroniske dokumenter mellom handelspartnere. Hvis du vil ha støtte for andre elektroniske dokumentformater, kan du bruke rammeverket for datautveksling.  

 I den generelle versjonen av [!INCLUDE[prod_short](includes/prod_short.md)] er en dokumentutvekslingstjeneste forhåndskonfigurert og klar til å bli definert for firmaet. Hvis du vil ha mer informasjon, kan du se [Konfigurere en dokumentutvekslingstjeneste](across-how-to-set-up-a-document-exchange-service.md). I noen tilfeller må du imidlertid installere en app. Hvis du vil ha mer informasjon, se [Vanlige spørsmål om elektronisk fakturering](faq-electronic-invoicing.yml).  

 Hvis du vil sende en salgsfaktura som et elektronisk PEPPOL-dokument, velger du alternativet **Elektronisk dokument** i dialogboksen **Bokfør og send**. Du kan også angi kundens standardprofil for dokumentsending fra den dialogboksen. Først må du definere forskjellige hoveddata, for eksempel firmainformasjon, kunder, varer og enheter. Disse brukes til å identifisere forretningspartnere og elementer ved konvertering av data i feltene [Konfigurere sending og mottak av elektroniske dokumenter](across-how-to-set-up-electronic-document-sending-and-receiving.md).  

### <a name="to-send-an-electronic-sales-invoice"></a><a name="to-send-an-electronic-sales-invoice"></a><a name="to-send-an-electronic-sales-invoice"></a>Slik sender du en elektronisk salgsfaktura:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Salgsfakturaer**, og velg deretter den relaterte koblingen.  

2. Opprett en ny salgsfaktura.  

3. Når salgsfakturalinjene er klare til å bli fakturert, kan du velge handlingen **Bokfør og send**.  

     Hvis kundens standard sendeprofil er **Elektronisk dokument**, vil den vises i dialogboksen **Legg inn og send bekreftelse**. På denne måten må du bare velge **Ja** for å bokføre og sende fakturaen elektronisk i det valgte formatet.  

4. I dialogboksen **Bokfør og send bekreftelse** velger du AssistEdit-knappen til høyre for feltet **Send dokument til**.  

5. I dialogboksen **Send dokument til** i feltet **Elektronisk dokument** velger du **Gjennom dokumentutvekslingstjeneste**.  

6. I **Format**-feltet velger du **PEPPOL**.  

7. Velg **OK**-knappen. Dialogboksen **Bokfør og send bekreftelse** vises. **Elektronisk dokument (PEPPOL)** legges til i **Send dokument til**-feltet.  

8. Velg **Ja**-knappen.  

     Salgsfakturaen bokføres og sendes til kunden i formatet PEPPOL.  

    > [!NOTE]  
    >  Du kan også sende en bokført salgsfaktura som et elektronisk dokument. Fremgangsmåten er den samme som beskrevet i dette emnet for ikke-bokførte salgsdokumenter. På siden **Bokført salgsfaktura** velger du **Aktivitetslogg**-handlingen for å vise statusen for det elektroniske dokumentet.  

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Se relatert [Microsoft-opplæring](/training/modules/electronic-documents-dynamics-365-business-central/index)

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se også

[Fakturere salg](sales-how-invoice-sales.md)  
[Definere en profil for dokumentsending](sales-how-setup-document-send-profiles.md)  
[Konfigurer sending og mottak av elektroniske dokumenter](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[Konfigurere en dokumentutvekslingstjeneste](across-how-to-set-up-a-document-exchange-service.md)  
[Definere datautvekslingsdefinisjoner](across-how-to-set-up-data-exchange-definitions.md)  
[Utveksle data elektronisk](across-data-exchange.md)  
[Vanlige spørsmål om elektronisk fakturering](faq-electronic-invoicing.yml)  
[Generelle forretningsfunksjoner](ui-across-business-areas.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
