---
title: Importer og eksporter en rapport og et dokumentoppsett
description: Du kan importere og eksportere et eksisterende egendefinert rapportoppsett som en fil til og fra en plassering på datamaskinen og nettverket.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '9652, 9650'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="legacy-import-and-export-custom-report-layouts"></a>(Eldre) Importere og eksportere en egendefinert rapportoppsett

[!INCLUDE[legacy-custom-layouts](includes/legacy-custom-layouts.md)]

Du kan importere og eksportere et eksisterende egendefinert rapportoppsett som en fil til og fra en plassering på datamaskinen og nettverket. Du kan for eksempel eksportere et rapportoppsett og deretter sende filen til en annen person som skal endre det. Vedkommende kan deretter gjøre endringer i oppsettet og returnere filen til deg slik at du kan importere den tilbake.  

> [!IMPORTANT]  
>  Du kan ikke importere eller eksportere innebygde rapportoppsett.  

### <a name="to-export-a-report-layout-to-a-file"></a>Slik eksporterer du et rapportoppsett til en fil

1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Rapportoppsettsvalg**, og velg deretter den relaterte koblingen.  

2.  Velg raden for rapporten som inneholder det egendefinerte rapportoppsettet du vil eksportere, og velg deretter handlingen **Egendefinerte oppsett**.  

3.  På siden **Rapportoppsett** velger du rapportoppsettet du vil eksportere til en fil, og velger deretter **Eksporter oppsett**.  

4.  Velg **Lagre** i dialogboksen **Eksporter fil**, og lagre deretter filen et sted på datamaskinen eller nettverket.  

### <a name="to-import-a-report-layout-file"></a>Slik importerer du en rapportoppsettfil

1.  Kontroller at den aktuelle filen som definerer rapportoppsettet, er tilgjengelig på datamaskinen eller nettverket.  

     En Word-rapportoppsettfil må filen ha filtypen DOCX. En RDLC-rapportoppsettfil må filen ha filtypen RDLC eller RDL.  

2.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Rapportoppsettsvalg**, og velg deretter den relaterte koblingen.  

3.  Velg raden for rapporten du vil importere rapportoppsettet til, og velg deretter handlingen **Egendefinerte oppsett**.  

4.  På siden **Rapportoppsett** velger du rapportoppsettet du vil impportere filen til, og velger deretter **Importer oppsett**.  

5.  Velg dokumentet som definerer rapportoppsettet, i dialogboksen **Importer**, og velg deretter **Åpne**.  

 Det opprinnelige egendefinerte rapportoppsettet erstattes med det importerte rapportoppsettet.  

## <a name="see-also"></a>Se også

[Opprette og endre et egendefinert rapportoppsett](ui-how-create-custom-report-layout.md)   
[Administrer rapport- og dokumentoppsett](ui-manage-report-layouts.md)  
[Arbeid med rapporter, satsvise jobber og XMLport-er](ui-work-report.md)    


[!INCLUDE[footer-include](includes/footer-banner.md)]
