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
ms.date: 12/02/2019
ms.author: edupont
ms.openlocfilehash: c575c0e482ebe4d34c9b699b22747486651efe04
ms.sourcegitcommit: b6e506a45a1cd632294bafa1c959746cc3a144f6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/06/2019
ms.locfileid: "2896136"
---
# <a name="accountant-experiences-in-included365fin_longincludesd365fin_long_mdmd"></a>Regnskapsføreropplevelser i [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]
Alle virksomheter må føre regnskap og godkjenne regnskapet. Enkelte virksomheter bruker en ekstern regnskapsfører, og andre har en regnskapsfører ansatt. Uansett hvilken type regnskapsfører du er, kan du bruke rollesenteret **Revisor** som hjemmet ditt i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Herfra har du tilgang til alle sidene du trenger i arbeidet.  

## <a name="accountant-role-center"></a>Rollesenter for regnskapsfører
Rollesenteret er et instrumentbord med aktivitetsfliser som viser deg nøkkeltall i sanntid og gir deg rask tilgang til data. På båndet øverst på siden har du tilgang til flere handlinger, som åpne mest vanlig brukte finansrapporter og årsregnskap i Excel. I navigasjonsstolpen på toppen kan du raskt bytte mellom oversiktene du bruker mest. Her vises andre områder som **bokførte dokumenter** med de ulike dokumenttypene som er bokført i selskapet.  

Hvis [!INCLUDE[d365fin](includes/d365fin_md.md)] er nytt for deg, kan du vise en oversikt over videoer rett fra rollesenteret. Du kan også starte **Komme i gang**, som angir viktige områder.  

## <a name="inviteaccountant"></a>Invitere den eksterne regnskapsføreren til [!INCLUDE[d365fin](includes/d365fin_md.md)]
Hvis du bruker en ekstern regnskapsfører til å administrere regnskap og finansrapportering, kan du invitere regnskapsføreren til [!INCLUDE[d365fin](includes/d365fin_md.md)], slik at vedkommende kan arbeide med regnskapsdataene.

Når regnskapsføreren har fått tilgang til [!INCLUDE[d365fin](includes/d365fin_md.md)], kan vedkommende bruke rollesenteret **Revisor**, som gir enkel tilgang til de mest relevante sidene for arbeidet.  

Vi har gjort det enkelt for deg å invitere den eksterne regnskapsføreren. Bare åpne **Brukere**-siden, og velg deretter **Inviter ekstern regnskapsfører** i båndet. En e-post er opprettet slik at du bare legger til regnskapsførerens arbeids-e-post og sender invitasjonen.  
> [!Note]  
> Dette krever at du har definert SMTP-e-post. Hvis du vil ha mer informasjon, kan du se [Konfigurer e-post](admin-how-setup-email.md).   

![Invitere regnskapsføreren din](./media/finance-invite-accountant/invite-accountant.png)

> [!IMPORTANT]  
> Regnskapsførerens e-postadresse må være en jobbadresse som er basert på Azure Active Directory. Hvis regnskapsføreren bruker en annen type e-post, kan ikke invitasjonen sendes.  

### <a name="behind-the-scenes"></a>I bakgrunnen
[!INCLUDE[d365fin](includes/d365fin_md.md)] inkluderer tre lisenser av typen ekstern regnskapsfører. Hvis selskapet bruker en ekstern regnskapsfører, kan du gi tilgang til [!INCLUDE[d365fin](includes/d365fin_md.md)] ved å tilordne dem en slik lisens. Hvis du vil ha mer informasjon om lisensiering, se [Lisensieringsveiledning for Microsoft Dynamics 365 Business Central](https://go.microsoft.com/fwlink/?LinkId=871590). 

Hvis abonnementet fortsatt har en tilgjengelig lisens, kan systemansvarlig eller videresalgspartneren legge til en ekstern bruker via Azure Portal og tilordne denne brukeren den eksterne regnskapsførerlisensen. Hvis du vil ha mer informasjon, se [Legge til Azure Active Directory B2B-samarbeidsbrukere i Azure Portal](/azure/active-directory/b2b/add-users-administrator).

Deretter kan du invitere regnskapsføreren fra innsiden av [!INCLUDE[d365fin](includes/d365fin_md.md)] ved å bruke den assisterte oppsettsveiledningen **Invitere ekstern regnskapsfører**. Ettersom denne oppgaven krever tilgang for å behandle brukere og lisenser i Azure Active Directory, må imidlertid brukeren som sender denne invitasjonen, tilordnes rollen **Global administrator** eller **Brukeradministrator** i Office 365-administrasjonssenteret. Hvis du vil ha mer informasjon, se [Om administratorroller](/office365/admin/add-users/about-admin-roles) i Office 365-administratorinnholdet. 

## <a name="accountant-hub"></a>Accountant Hub
Hvis du er en regnskapsfører med flere klienter, kan du bruke [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)] for å få en bedre oversikt over klientene dine. Herfra har du tilgang til hver klients leier i [!INCLUDE[d365fin](includes/d365fin_md.md)], og du kan bruke rollesenter for regnskapsfører som beskrevet ovenfor. Hvis du vil ha mer informasjon, kan du se [Velkommen til [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)]](/dynamics365/accountants/index).  

> [!NOTE]
> [!INCLUDE [d365acc_long_md](includes/d365acc_long_md.md)] er for øyeblikket i en offentlig forhåndsversjon i et begrenset antall markeder.

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
[Dynamics 365 – Accountant Hub på Microsoft.com](https://www.microsoft.com/dynamics365/financial-insights-for-accountants)  
