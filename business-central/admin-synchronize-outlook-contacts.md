---
title: Dele kontakter mellom Business Central og Outlook| Microsoft Docs
description: Denne tjenesten er tett integrert med Office 365 slik at du kan dele kontakter mellom Outlook og Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: contacts, Office 365
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: 93acc30c501b099b829a304650b09b356d2243e7
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2019
ms.locfileid: "1244196"
---
# <a name="synchronize-contacts-in-business-central-with-contacts-in-microsoft-outlook"></a>Synkronisere kontakter i Business Central med kontakter i Microsoft Outlook
Du kan se de samme kontaktene i [!INCLUDE[d365fin](includes/d365fin_md.md)] som du ser i Outlook, hvis du definerer kontaktsynkronisering. Hvis for eksempel du er selger, gjør du kanskje noe arbeid i Outlook og noen av arbeidet i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hvis kontaktene er de samme begge steder, er arbeidet mer enkelt.  

En egen mappe i Outlook gjør at kontakter er lette å finne, og du kan angi et filter for å synkronisere bare kontaktene fra [!INCLUDE[d365fin](includes/d365fin_md.md)] som du vil vise i Outlook. Når kontaktsynkroniseringen er definert, kan du starte synkroniseringen manuelt eller sette opp automatisk synkronisering som vil holde kontaktene synkronisert regelmessig.  

## <a name="set-up-synchronization"></a>Definere synkronisering
Du definerer hvordan du vil synkronisere kontaktene med Outlook på siden **Konfigurasjon av Exchange-synkronisering** i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Det er en forutsetning at brukerprofilen din i [!INCLUDE[d365fin](includes/d365fin_md.md)] må angi din e-postkonto for Office 365. Du kan kontrollere dette i **Office 365-godkjenning**-delen av brukerprofilen din i **Brukere**-listen.  

Deretter på **Konfigurasjon av Exchange-synkronisering**-siden kan du validere at tilkoblingen til Exchange fungerer, og deretter definere kontaktsynkronisering. Åpne siden **Oppsett for synkronisering av kontakt**, og start synkroniseringen. Du kan også angi et filter for hvilke kontakter som skal synkroniseres mellom [!INCLUDE[d365fin](includes/d365fin_md.md)] og Outlook. Du kan for eksempel angi et filter på navn, type, selskap eller lignende. Du kan også endre standardnavnet på mappen som kontaktene skal synkroniseres til i Outlook. Standardnavnet er *Business Central*.  

Når synkroniseringen er definert, blir endringer som du gjør i kontakten i Outlook eller i [!INCLUDE[d365fin](includes/d365fin_md.md)], synkronisert til den andre.  

Hver av kollegaene kan også konfigurere sin egen Exchange-synkronisering og definere sitt eget filter for kontaktene som skal synkroniseres.  

## <a name="synchronize-contacts"></a>Synkronisere kontakter
Hvis du er vant med å arbeide med kontakter i [!INCLUDE[d365fin](includes/d365fin_md.md)], vil du synes det er enkelt å starte synkroniseringen manuelt når det passer deg, fra **Kontakter**-listen. Velg bare **Synkroniser med Office 365**-handlingen, og bestem om du vil endre filteret du har definert. Når du velger OK-knappen, starter synkroniseringen umiddelbart, og de siste endringene brukes på kontaktene i Outlook.  

I **Kontakter**-listen kan du synkronisere kontakter på to måter:

* **Synkroniser med Office 365**

  Denne handlingen synkroniserer alle endringer fra [!INCLUDE[d365fin](includes/d365fin_md.md)] til Office 365 siden den forrige synkroniseringen, basert på dato med siste endring. Alle nye kontakter fra Office 365 synkroniseres tilbake til [!INCLUDE[d365fin](includes/d365fin_md.md)] også. Dette er vanligvis raskere enn å utføre en fullstendig synkronisering.  

* **Synkroniser fullstendig med Office 365**

  Denne handlingen synkroniserer alle kontaktene i begge retninger uavhengig av den siste synkroniseringsdatoen og datoen for siste endring.  

I begge tilfeller synkroniseres bare kontakter fra Outlook hvis de har utfylt de obligatoriske feltene. Obligatoriske felt som skal synkroniseres til Office 365, er **Navn**, **E-postadresse** og de må være av typen Person. [!INCLUDE[d365fin](includes/d365fin_md.md)] er hovedtabellen for kontaktopplysningene, slik at [!INCLUDE[d365fin](includes/d365fin_md.md)]-kontaktinformasjonen lagres i tilfelle duplikater.  

I Outlook vises kontaktene fra [!INCLUDE[d365fin](includes/d365fin_md.md)] i en mappe under **Andre kontakter** i **Personer**-visningen. Hvis du ikke kjenner til Personer-visningen i Outlook, kan få tilgang til den fra navigasjonsvalgene nederst til venstre i Outlook.  

## <a name="see-also"></a>Se også
[Komme i gang](product-get-started.md)  
[Finans](finance.md)  
[Salg](sales-manage-sales.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Bruke kontakter (personer) i Outlook på Internett](https://support.office.com/en-us/article/Using-contacts-People-in-Outlook-on-the-web-1e3438c7-26b2-420c-87de-3cea9d31b5cb?appver=OWB150)  
