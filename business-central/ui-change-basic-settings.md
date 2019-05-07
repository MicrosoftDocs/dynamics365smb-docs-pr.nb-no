---
title: Vise og redigere grunnleggende innstillinger | Microsoft-dokumentasjon
description: Finn ut hvordan du kan endre noen av de grunnleggende innstillingene, for eksempel rollesenteret, selskapet eller arbeidsdatoen.
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: change Role Center, notification, change company, change work date
ms.date: 04/01/2019
ms.author: solsen
ms.openlocfilehash: d95d2f609129e4bdba35deda726323dbed2ba67a
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2019
ms.locfileid: "916225"
---
# <a name="changing-basic-settings"></a>Endre grunnleggende innstillinger
På siden [**Mine innstillinger**](https://businesscentral.dynamics.com?page=9176 "Gå direkte til siden med brukerinnstillinger i Business Central") kan du se og endre grunnleggende innstillinger for [!INCLUDE[d365fin](includes/d365fin_md.md)]. Endringene du gjør, påvirker bare arbeidsområdet, ikke arbeidsområdene til andre brukere.  

## <a name="role-center"></a> Rollesenter
Rollesenteret representerer hjemmesiden, et startskjermbilde som er tilpasset behovene til en spesifikk rolle i en organisasjon. Avhengig av rollen din gir rollesenteret deg en oversikt over bedriften, avdelingen eller dine egne oppgaver. Det kan også hjelpe deg med å navigere til daglige oppgaver og finne arbeid som er tilordnet til deg.

-   Øverst i navigeringen kan du veksle mellom kunder, leverandører, varer og andre viktige lister med opplysninger. På samme måte kan handlinger la deg opprette oppgaver, for eksempel opprette en ny salgsfaktura direkte fra rollesenteret.

-   I midten finner du **Aktiviteter**. Aktiviteter viser gjeldende data og kan klikkes eller trykkes for å vise mer detaljerte opplysninger. Sentrale ytelsesindikatorer kan settes opp til å vise et valgt diagram for en visuell fremstilling av, for eksempel kontantstrøm eller inntekter og utgifter. Du kan også bygge opp en liste over favorittkunder på hjemmesiden for forretningsforbindelser som du gjør forretninger med ofte eller må vie spesiell oppmerksomhet.

### <a name="to-change-role-center"></a>Endre rollesenter
Standard rollesenter er **Forretningsleder**, men du kan velge et annet rollesenteret som passer bedre til dine behov.
1. I øvre høyre hjørne velger du **Innstillinger**-ikonet ![Innstillinger](media/ui-experience/settings_icon_small.png "Innstillinger-ikonet for rollesenter"), og velg deretter **Mine innstillinger**.
2. På siden **Mine innstillinger**, i feltet **Rollesenter**, velger du rollesenteret som du vil angi som standard. Velg for eksempel **Revisor**.
3. Velg **OK**-knappen.

## <a name="company"></a>Selskap
Et selskap fungerer som en beholder for data i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Det kan være flere firmaer i en database, men du kan velge bare ett om gangen.

Standardfirma kalles CRONUS og inneholder demonstrasjonsdata bare.

> [!TIP]  
>   Hvis du vil vise et annet navn for selskapet i programmet (for eksempel i rollesenteret), angir du **Navn**-feltet på siden **Selskapsopplysninger** eller **Visningsnavn** på **Selskaper**-siden.  

## <a name="work-date"></a>Arbeidsdato
Standard arbeidsdato er vanligvis dagens dato. Du må kanskje endre arbeidsdatoen midlertidig for å utføre oppgaver, for eksempel å fylle ut transaksjoner for en dato som ikke er gjeldende dato.

> [!TIP]  
>   Skriv inn **a** hvis du raskt vil angi arbeidsdatoen i et datofelt. Skriv inn **i** hvis du hurtig vil angi gjeldende dato i datofeltet.

> [!IMPORTANT]  
>   Når du endrer arbeidsdatoen, og hvis du logger ut eller bytter til et annet selskap, reverteres arbeidsdataene til standard arbeidsdato. Så neste gang du logger deg på eller bytter tilbake til det opprinnelige selskapet, må du kanskje angi arbeidsdatoen på nytt. 

### <a name="work-date-indication"></a>Arbeidsdatoindikasjon
<!--
Whenever the work date is not set to the current day (today), there are two indicators on pages that you open for editing:

- A reminder appears at the top of the page that tells you what the work date is set to. The reminder provides a direct link to the work date setting on the **My Settings** page so you change the date if you want. From the reminder, you can also choose to dismiss the reminder for the rest of your session. Unless you change the work date to "today", the reminder will appear the next time you sign in. 

- If you dismiss the reminder, the work date will appear in the title of the page.  
-->
Hvis arbeidsdatoen ikke er angitt til gjeldende dag (i dag), vil gjeldende arbeidsdato vises øverst til venstre på siden på alle sider der kan du redigere data.
  
## <a name="region"></a> Region

**Område**-innstillingen bestemmer hvordan datoer, klokkeslett, numre og valutaer vises eller formateres.


## <a name="language"></a> Språk
Endre visningsspråket. Dette feltet vises bare når det er mer enn ett språk som kan velges. 

Det første språket bestemmes enten av systemansvarlig eller leserinnstillingene når du registrerer deg for [!INCLUDE[d365fin](includes/d365fin_md.md)]. Språket som du har angitt, vil bli brukt på alle enhetene du logger på fra, for eksempel telefon eller nettbrett.

## <a name="changing-when-i-receive-notifications"></a>Endre når jeg mottar varsler
Velg denne koblingen for å vise eller endre varslingene som du får om bestemte hendelser eller endringer i status, når du for eksempel er i ferd med fakturere en kunde som har en forfalt saldo, eller den disponible beholdningen er lavere enn antallet du vil selge. Hvis du vil ha mer informasjon, kan du se [Smarte varsler](ui-smart-notifications.md).

## <a name="see-also"></a>Se også
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Endre hvilke funksjoner som vises](ui-experiences.md)  
