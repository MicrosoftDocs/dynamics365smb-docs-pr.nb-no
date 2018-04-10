---
title: Konfigurere ny selskaper ved hjelp av en Cmdlet | Microsoft-dokumentasjon
description: "I en rekke scenarier bør du laste ned og importere en konfigurasjonspakke uten å involvere brukerne eller bruke brukergrensesnittet i RapidStart Services. Du kan gjøre dette ved å bruke en Windows PowerShell-cmdlet."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/06/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 9d248f2f8676c392451ae4a6f99932145f354f5b
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="configure-new-companies-using-a-cmdlet"></a>Konfigurere ny selskaper ved hjelp av en Cmdlet
I en rekke scenarier bør du laste ned og importere en konfigurasjonspakke uten å involvere brukerne eller bruke brukergrensesnittet i RapidStart Services. Du kan gjøre dette ved å bruke en Windows PowerShell-cmdlet. Dette kan være nyttig i følgende scenarier:  

- Utføre import på tvers av flere [!INCLUDE[d365fin](includes/d365fin_md.md)]-installasjoner.
- Konfigurere flere programområder for flere kunder.  

## <a name="to-deploy-a-configuration-package-using-a-cmdlet"></a>Slik distribuerer du en konfigurasjonspakke ved å bruke en cmdlet:  

1. Forberede en pakke RapidStart Services. Du kan for eksempel opprette en pakke for å importere bestemte verdier og navnene på tabellen og feltene som verdiene skal settes inn i.  
2. Plasser pakken på en datamaskin der du vil kjøre cmdleten.  
3. Åpne administrasjonsskallet for [!INCLUDE[d365fin](includes/d365fin_md.md)].  
4. Angi **Invoke-NAVCodeUnit**, og angi informasjon som ligner følgende eksempel.  
    ```powershell  
    Invoke-NAVCodeunit -Tenant Default -CompanyName "CRONUS International Ltd." -CodeunitId 8620 -MethodName ImportRapidStartPackage -Argument "C:TEMPRS_CONFIG.rapidstart" -ServerInstance DynamicsNAV71  

    ```
Cmdleten importerer pakken til hvert selskap. Brukere kan begynne å bruke den nye funksjonaliteten umiddelbart.  

## <a name="see-also"></a>Se også  
[Konfigurere nye selskaper](admin-how-to-configure-new-companies.md)  
[Bruke konfigurasjoner for nye selskaper](admin-apply-configuration-to-new-companies.md)  
[Konfigurere et selskap med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administrasjon](admin-setup-and-administration.md)  
[Microsoft Dynamics NAV Windows PowerShell-cmdleter](/dynamics-nav/microsoft-dynamics-nav-windows-powershell-cmdlets)

