---
title: Vise og redigere grunnleggende innstillinger | Microsoft-dokumentasjon
description: Finn ut hvordan du kan endre noen av de grunnleggende innstillingene, for eksempel rollesenteret, selskapet eller arbeidsdatoen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: change Role Center, notification, change company, change work date
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 61d0ddfd19dede42497607dd0f1897598ac61b80
ms.sourcegitcommit: 35f7e24c301926b39094aa64fe608afd04fdb8e1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/10/2021
ms.locfileid: "5573329"
---
# <a name="change-basic-settings"></a>Endre grunnleggende innstillinger

På siden **Mine innstillinger** kan du vise og endre grunnleggende innstillinger for [!INCLUDE[prod_short](includes/prod_short.md)]. Endringene du gjør, påvirker bare ditt arbeidsområde, ikke arbeidsområdene til andre brukere.  

## <a name="role-center"></a><a name="role-center"></a> Rollesenter

Rollesenteret representerer hjemmesiden eller startskjermbildet. Den er utformet for behovene til en bestemt rolle i en organisasjon. Avhengig av rollen din gir rollesenteret deg en oversikt over bedriften, avdelingen eller dine egne oppgaver. Rollesenteret kan også hjelpe deg med å navigere til daglige oppgaver og finne arbeid som er tilordnet til deg.

- Øverst i navigeringen kan du veksle mellom kunder, leverandører, varer og andre viktige lister med opplysninger. På samme måte kan handlinger la deg starte oppgaver, for eksempel opprette en ny salgsfaktura direkte fra rollesenteret.

- I midten finner du **Aktiviteter**-området, som viser gjeldende data. Du kan velge eller trykke på dataene for å vise mer detaljert informasjon. Sentrale ytelsesindikatorer (KPIer) kan settes opp for å vise et valgt diagram for en visuell fremstilling av for eksempel kontantstrøm eller inntekter og utgifter. Du kan også bygge opp en liste over favorittkunder i rollesenteret, for forretningsforbindelser som du gjør forretninger med ofte, eller som må vies spesiell oppmerksomhet.

### <a name="to-change-the-role"></a>Endre rollen

Standardrollen er **Forretningsleder**, men du kan velge en annet rolle for å bruke et rollesenter som passer bedre til dine behov.
1. I øvre høyre hjørne velger du **Innstillinger**-ikonet ![Innstillinger](media/ui-experience/settings_icon_small.png "Innstillinger-ikon for rollesenter"), og velg deretter handlingen **Mine innstillinger**.
2. På siden **Mine innstillinger**, i feltet **Rolle**, velger du rollen som du vil angi som standard. Velg for eksempel **Revisor**.
3. Velg **OK**-knappen.

## <a name="company"></a><a name="company"></a>Selskap

Et selskap fungerer som en beholder for data i [!INCLUDE[prod_short](includes/prod_short.md)]. Det kan være flere firmaer i en database, men du kan velge bare ett om gangen.

Standardfirma kalles CRONUS og inneholder demonstrasjonsdata bare. Du kan opprette et nytt selskap med egendefinerte data. Hvis du vil ha mer informasjon, kan du se [Opprette nye selskaper](about-new-company.md).

## <a name="to-change-the-company-name"></a>Endre selskapsnavnet

Selskapsnavnet vises alltid øverst i venstre hjørne. Det fungerer som en handling du kan velge å gå tilbake til rollesenteret. Du kan endre dette navnet på siden **Selskapsinformasjon**.

1. Velg ikonet ![Sprocket-ikon for å åpne Innstillinger-meny](media/ui-experience/settings_icon_small.png), og velg deretter handlingen **Selskapsinformasjon**.
2. Skriv inn det nye selskapsnavnet i feltet **Navn**.
3. Forlat siden. Systemet starter på nytt og viser det nye selskapet i øvre venstre hjørne.

## <a name="to-display-a-company-badge-for-quick-access-to-company-information"></a><a name="badge"></a>Vise et selskapsmerke for rask tilgang til selskapsinformasjon

Du kan legge til et tilpasset merke i øvre høyre hjørne, som du kan velge for å raskt vise selskapsinformasjon og leietakerinformasjon i en popup-boks. Selskapsmerket er også nyttig når [!INCLUDE[prod_short](includes/prod_short.md)] er innebygd i et annet program, for eksempel Microsoft Teams eller i et annet nettprogram. I slike tilfeller, siden [!INCLUDE[web_client](includes/web_client.md)] viser mindre omkringliggende kontekstinformasjon, fungerer firmamerket som den eneste måten å avgjøre hvilket selskap eller hvilket miljø en post tilhører.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Selskapsopplysninger**, og velg deretter den relaterte koblingen.
2. På hurtigfanen **Selskapsmerke** fyller du ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

> [!NOTE]
> Hvis et selskapsmerke er definert, kan du ikke endre selskapsnavnet slik det er beskrevet i [Endre selskapsnavn](ui-change-basic-settings.md#to-change-the-company-name)

## <a name="work-date"></a><a name="work-date"></a>Arbeidsdato

Den mest brukte arbeidsdatoen er i dag. Du må kanskje endre arbeidsdatoen midlertidig for å utføre oppgaver, for eksempel å fylle ut transaksjoner for en dato som ikke er i dag.

> [!TIP]  
> I alle dataofelt skriver du inn **i** for å raskt angi i dag, og **a** for å raskt angi arbeidsdato, som er verdien i feltet **Arbeidsdato** på siden **Mine innstillinger**.

> [!IMPORTANT]  
>  Når du endrer arbeidsdatoen, og hvis du logger ut eller bytter til et annet selskap, reverteres arbeidsdataene til standard arbeidsdato. Så neste gang du logger deg på eller bytter tilbake til det opprinnelige selskapet, må du kanskje angi arbeidsdatoen på nytt.

### <a name="work-date-indication"></a>Arbeidsdatoindikasjon

Arbeidsdatoen er viktig på sider som kan redigeres. Når arbeidsdatoen ikke er satt til dagens dato på en redigerbar side, vises to typer indikatorer på siden:

- Det vises en påminnelse øverst på siden som forteller deg hva arbeidsdatoen er satt til. Påminnelsen gir en direkte kobling til arbeidsdatoinnstillingen på siden **Mine innstillinger**, slik at du kan endre datoen hvis du vil. Fra purringen kan du også velge å lukke påminnelsen for resten av økten. Med mindre du endrer arbeidsdatoen til "i dag", vil påminnelsen vises neste gang du logger på.

- Hvis du lukker purringen, vises arbeidsdatoen vises i tittelen på siden.  

Hvis arbeidsdatoen ikke er angitt til gjeldende dag (i dag), vil gjeldende arbeidsdato vises øverst til venstre på alle sider der kan du redigere data.

## <a name="region"></a><a name="region"></a> Region

**Område**-innstillingen bestemmer hvordan datoer, klokkeslett, numre og valutaer vises eller formateres.

## <a name="language"></a><a name="language"></a> Språk

Endre visningsspråket. Dette feltet vises bare når det er mer enn ett språk som kan velges.

Det første språket bestemmes enten av systemansvarlig eller leserinnstillingene når du registrerer deg for [!INCLUDE[prod_short](includes/prod_short.md)]. Språket som du har angitt, vil bli brukt på alle enhetene du logger på fra, for eksempel telefon eller nettbrett.

Flere språk for [!INCLUDE[prod_short](includes/prod_short.md)] kan installeres fra AppSource. Alle støttede visningsspråk vises i listen. Systemansvarlig må installere den relevante språkappen før brukere kan bytte til det nye språket i [!INCLUDE[prod_short](includes/prod_short.md)].  

## <a name="changing-when-i-receive-notifications"></a>Endre når jeg mottar varsler

Velg denne koblingen for å vise eller endre varslene om bestemte hendelser eller endringer i status. Du kan for eksempel få et varsel om når du er i ferd med fakturere en kunde som har en forfalt saldo, eller den disponible beholdningen er lavere enn antallet du vil selge. Hvis du vil ha mer informasjon, kan du se [Administrere varsler](ui-smart-notifications.md).

## <a name="see-related-training-at-microsoft-learn"></a>Se relatert opplæring på [Microsoft Learn](/learn/modules/personalize-ui-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også
[Opprette nye seleskaper](about-new-company.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Endre hvilke funksjoner som vises](ui-experiences.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]