---
title: Optimaliser Outlook for innboks for virksomheten
description: Lær om ting du kan gjøre for å forbedre opplevelsen med innboksen for virksomhet i Microsoft Outlook.
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Outlook, Microsoft 365, inbox, business inbox, WebView2, Edge, addin, add-in'
ms.date: 12/06/2023
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---
# Optimaliser Outlook for innboks for virksomheten 

Denne artikkelen beskriver ting du kan gjøre for å få den best mulige opplevelsen med innboksen for virksomhet i Microsoft Outlook. 

## Oppdater Outlook

Oppdat til Outlook, versjon 2012 eller nyere.

> [!NOTE]
> Hvis du ikke kan oppdatere Outlook til versjon 2012 eller nyere, må du kontrollere at du minst oppdaterer til versjon 1905. Dette forhindrer at Outlook-tillegget kan kjøre ved å bruke eldre Internet Explorer-komponenter

### Slik kontrollerer du versjonen til Outlook

Hvis du bruker Office 2019 eller Microsoft 365, følger du denne veiledningen fra Microsofts kundestøtte for å kontrollere hvilken Outlook-versjon du har:  

[Om Office: Hvilken versjon av Office bruker jeg?](https://support.microsoft.com/office/about-office-what-version-of-office-am-i-using-932788b8-a3ce-44bf-bb09-e334518b8b19)

### Slik oppdaterer du Outlook

Hvis du vil oppdatere Outlook til den nyeste versjonen, følger du veiledningen fra Microsofts kundestøtte eller kontakter administratoren:

[Installer Office-oppdateringer](https://support.microsoft.com/office/install-office-updates-2ab296f3-7f03-43a2-8e50-46de917611c5)

## Installer Microsoft Edge WebView2

Kontroller at Microsoft Edge WebView2 er installert på enheten.

### Slik kontrollerer du om Microsoft Edge WebView2 er installert 

Hvis du vil kontrollere om du har Microsoft Edge WebView2 installert på en datamaskin, gjør du følgende:

Fra Start-menyen:

1. Velg **Start** ![Windows-start.](media/windows-start-icon.png "Windows Start-ikon") > **Innstillinger** ![Windows-innstillinger](media/windows-settings-icon.png "Ikon for Windows-innstillinger") > **Apper og funksjoner**.
2. Skriv inn **WebView2** i søkefeltet. Hvis Microsoft Edge WebView2 er installert, vises en oppføring kalt **Microsoft Edge WebView2 Runtime**.

Fra kontrollpanel:

1. Skriv inn **Kontrollpanel** i søkefeltet ved siden av **Start** ![Windows Start](media/windows-start-icon.png "Windows Start-ikon"), og velg deretter resultatet.
2. Velg **Programmer** > **Programmer og funksjoner**.
3. Skriv inn **WebView2** i søkefeltet. Hvis Microsoft Edge WebView2 er installert, vises en oppføring kalt **Microsoft Edge WebView2 Runtime**.

### Slik installerer du Microsoft Edge WebView2 

1. Gå til [https://developer.microsoft.com/microsoft-edge/webview2/](https://developer.microsoft.com/microsoft-edge/webview2/) i nettleseren.
2. Velg **Last ned**.
3. Angi **Velg arkitektur** for å samsvare med systemet ditt.
4. Velg **Last ned**.

> [!NOTE]
> Det kan hende at organisasjonen har begrensninger for hvilke komponenter som kan installeres på enheten. Kontakt systemansvarlig for å få hjelp.

## Bruk en nettleser som støttes

Du bør vurdere å bruke Outlook for nettet i en av nettleserne som støttes av Business Central. Hvis du vil se en liste over nettlesere som støttes, kan du se [Minimumskrav for bruk av Business Central](product-requirements.md#browsers).

## Se også

[Bli klar til å gjøre forretninger](ui-get-ready-business.md)  
[Få Business Central på mobilenheten](install-mobile-app.md)  
[Send dokumenter i e-post](ui-how-send-documents-email.md)  
[Finans](finance.md)  
[Salg](sales-manage-sales.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Minimumskrav for Outlook](product-requirements.md#outlook)  
[Bruk tillegg i Outlook på Internett](https://support.office.com/article/Using-Add-ins-in-Outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?appver=OWB150)  


[!INCLUDE[footer-include](includes/footer-banner.md)]