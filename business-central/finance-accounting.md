---
title: Regnskapsføreropplevelsen i Business Central | Microsoft-dokumentasjon
description: Få informasjon om regnskapsførerportalen for Business Central og rollesenter for regnskapsfører som støtter interne og eksterne regnskapsførere i klientselskapet.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 05/02/2019
ms.author: edupont
ms.openlocfilehash: f088e1319684b9a18a2b0c8ab5305f73747f6889
ms.sourcegitcommit: dac212009aadf3227e54c99976c438f6e56f182a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/02/2019
ms.locfileid: "1446925"
---
# <a name="accountant-experiences-in-included365finlongincludesd365finlongmdmd"></a>Regnskapsføreropplevelser i [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]
Alle virksomheter må føre regnskap og godkjenne regnskapet. Enkelte virksomheter bruker en ekstern regnskapsfører, og andre har en regnskapsfører ansatt. Uansett hvilken type regnskapsfører du er, kan du bruke rollesenteret **Revisor** som hjemmet ditt i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Herfra har du tilgang til alle sidene du trenger i arbeidet.  

## <a name="accountant-role-center"></a>Rollesenter for regnskapsfører
Rollesenteret er et instrumentbord med aktivitetsfliser som viser deg nøkkeltall i sanntid og gir deg rask tilgang til data. På båndet øverst på siden har du tilgang til flere handlinger, som åpne mest vanlig brukte finansrapporter og årsregnskap i Excel. I navigasjonsstolpen på toppen kan du raskt bytte mellom oversiktene du bruker mest. Her vises andre områder som **bokførte dokumenter** med de ulike dokumenttypene som er bokført i selskapet.  

Hvis [!INCLUDE[d365fin](includes/d365fin_md.md)] er nytt for deg, kan du vise en oversikt over videoer rett fra rollesenteret. Du kan også starte **Komme i gang**, som angir viktige områder.  

## <a name="accountant-hub"></a>Accountant Hub
Hvis du er en regnskapsfører med flere klienter, kan du bruke [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)] for å få en bedre oversikt over klientene dine. Herfra har du tilgang til hver klients leier i [!INCLUDE[d365fin](includes/d365fin_md.md)], og du kan bruke rollesenter for regnskapsfører som beskrevet ovenfor. Hvis du vil ha mer informasjon, kan du se [Velkommen til [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)]](/dynamics365/accountants/index).

## <a name="inviting-your-external-accountant-to-your-included365finincludesd365finmdmd"></a>Invitere den eksterne regnskapsføreren til [!INCLUDE[d365fin](includes/d365fin_md.md)]
Hvis du bruker en ekstern regnskapsfører til å administrere regnskap og finansrapportering, kan du invitere regnskapsføreren til [!INCLUDE[d365fin](includes/d365fin_md.md)], slik at vedkommende kan arbeide med regnskapsdataene.

Når regnskapsføreren har fått tilgang til [!INCLUDE[d365fin](includes/d365fin_md.md)], kan vedkommende bruke rollesenteret **Revisor**, som gir enkel tilgang til de mest relevante sidene for arbeidet.  

Vi har gjort det enkelt for deg å invitere den eksterne regnskapsføreren. Bare åpne **Brukere**-siden, og velg deretter **Inviter ekstern regnskapsfører** i båndet. En e-post er opprettet slik at du bare legger til regnskapsførerens arbeids-e-post og sender invitasjonen.  

![Invitere regnskapsføreren din](./media/finance-invite-accountant/invite-accountant.png)

> [!TIP]  
>  Dette krever at du har definert SMTP-e-post. Du kan gjøre dette selv eller be din [!INCLUDE[d365fin](includes/d365fin_md.md)]-partner. I tillegg du må være logge på [!INCLUDE[d365fin](includes/d365fin_md.md)] som brukeradministrator, ikke som bedriftseier eller andre brukere. Til slutt må du ha igjen prøveselskapet slik at du har en administrator for Azure Active Directory.  

> [!IMPORTANT]  
> Regnskapsførerens e-postadresse må være en jobbadresse som er basert på Azure Active Directory. Hvis regnskapsføreren bruker en annen type e-post, kan ikke invitasjonen sendes.  

### <a name="separate-license"></a>Egen lisens
Regnskapsføreren blir lagt til i Active Directory-leietakeren din bakgrunnen. Systemansvarlig kan kontrollere at regnskapsføreren godtar invitasjonen og tilordnes riktig lisens. Fremgangsmåten for å gjøre dette er avhengig av kontotypen du brukte da du registrerte deg for [!INCLUDE[d365fin](includes/d365fin_md.md)]. Dette emnet er basert på bruken av en Office 365-konto, som bruker Microsoft Azure Active Directory.  

Hvis du har aktivert abonnementet på [!INCLUDE[d365fin](includes/d365fin_md.md)] og ikke lenger bruker evalueringsselskapet, har du en Azure Active Directory-leier. Administratoren eller [!INCLUDE[d365fin](includes/d365fin_md.md)]-partneren administrerer denne leieren i vinduet [Azure Portal](https://portal.azure.com). Det er her nye brukere legges til og lisenser brukes og fjernes. Hvis du vil ha mer informasjon, kan du se [Oversikt over Microsoft Azure Portal](https://docs.microsoft.com/en-us/azure/azure-portal-overview).  

En av lisenstypene for [!INCLUDE[d365fin](includes/d365fin_md.md)] er lisensen *Ekstern regnskapsfører*. Denne lisenstypen er beregnet på brukere som eksterne regnskapsførere. Dette betyr at du slipper å kjøpe en ekstra plass i Active Directory eller bruke en av de eksisterende [!INCLUDE[d365fin](includes/d365fin_md.md)]-brukerkontiene på den eksterne regnskapsføreren. Hvis det gjeldende Office 365-abonnementet ditt omfatter ti brukere for [!INCLUDE[d365fin](includes/d365fin_md.md)], og du bruker ti *Fullstendig bruker*-lisenser, kan systemansvarlig ganske enkelt legge til den eksterne regnskapsføreren som en gjestebruker i Azure Portal og tilordne denne brukeren til lisensen *Ekstern regnskapsfører* uten ekstra kostnad. Du kan imidlertid bare ha én bruker med lisensen *Ekstern regnskapsfører*. Hvis du vil legge til flere brukere, må du oppdatere Office 365-abonnementet tilsvarende.

## <a name="see-also"></a>Se også
[Finans](finance.md)  
[Konfigurere finans](finance-setup-finance.md)  
[Finans og kontoplanen](finance-general-ledger.md)  
[Avslutte år og perioder](year-close-years-periods.md)  
[Arbeide med dimensjoner](finance-dimensions.md)  
[Analysere årsregnskap i Excel](finance-analyze-excel.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Definere kontantstrømanalyse](finance-setup-cash-flow-analyses.md)  
[Velkommen til [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)]](/dynamics365/accountants/index)  
[Dynamics 365 – Accountant Hub på Microsoft.com](https://www.microsoft.com/en-us/dynamics365/financial-insights-for-accountants)  
