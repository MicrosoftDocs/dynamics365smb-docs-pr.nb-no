---
title: Regnskapsføreropplevelser i Business Central
description: Få informasjon om rollesenteret for regnskapsfører og selskapshuben som støtter interne og eksterne regnskapsførere i klientselskapet.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 5aaf2b72fc282eceabb6991345a2eac9508bdb13
ms.sourcegitcommit: aea079b66e35c447bf31a11ffc2069cfdaf2ef38
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/08/2020
ms.locfileid: "3970415"
---
# <a name="accountant-experiences-in-d365fin_long"></a>Regnskapsføreropplevelser i [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]

Alle virksomheter må føre regnskap og godkjenne regnskapet. Enkelte virksomheter bruker en ekstern regnskapsfører, og andre har en regnskapsfører ansatt. Uansett hvilken type regnskapsfører du er, kan du bruke rollesenteret **Revisor** som hjemmet ditt i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Herfra har du tilgang til alle sidene du trenger i arbeidet.  

## <a name="accountant-role-center"></a>Rollesenter for regnskapsfører

Rollesenteret er et instrumentbord med aktivitetsfliser som viser deg nøkkeltall i sanntid og gir deg rask tilgang til data. På båndet øverst på siden har du tilgang til flere handlinger, som åpne mest vanlig brukte finansrapporter og årsregnskap i Excel. I navigasjonsstolpen på toppen kan du raskt bytte mellom oversiktene du bruker mest. Her vises andre områder som **bokførte dokumenter** med de ulike dokumenttypene som er bokført i selskapet.  

Hvis [!INCLUDE[d365fin](includes/d365fin_md.md)] er nytt for deg, kan du vise en oversikt over videoer rett fra rollesenteret. Du kan også starte **Komme i gang**, som angir viktige områder.  

## <a name="company-hub"></a>Selskapshub

Hvis du arbeider i flere [!INCLUDE [prodshort](includes/prodshort.md)]-firmaer, kan det være nyttig å bruke **Selskapshub**-siden for å holde oversikt over arbeid.  Hvis du vil ha mer informasjon, kan du se [Administrere arbeid på tvers av flere selskaper i selskapshuben](company-hub.md).  

## <a name="inviting-your-external-accountant-to-your-d365fin"></a><a name="inviteaccountant"></a>Invitere den eksterne regnskapsføreren til [!INCLUDE[d365fin](includes/d365fin_md.md)]

Hvis du bruker en ekstern regnskapsfører til å administrere regnskap og finansrapportering, kan administratoren din invitere regnskapsføreren til [!INCLUDE[d365fin](includes/d365fin_md.md)], slik at vedkommende kan arbeide med regnskapsdataene. [!INCLUDE[d365fin](includes/d365fin_md.md)] inkluderer tre lisenser av typen ekstern regnskapsfører. For mer informasjon om lisensiering, se [Lisensieringsveiledning for Microsoft Dynamics 365 Business Central](https://go.microsoft.com/fwlink/?LinkId=871590).

Når regnskapsføreren har fått tilgang til [!INCLUDE[d365fin](includes/d365fin_md.md)], kan vedkommende bruke rollesenteret **Revisor**, som gir enkel tilgang til de mest relevante sidene for arbeidet. De kan også bruke selskapshuben i sin egen [!INCLUDE [prodshort](includes/prodshort.md)] for å håndtere arbeidet sitt. Hvis du vil ha mer informasjon, kan du se [Administrere arbeid på tvers av flere selskaper i selskapshuben](company-hub.md).  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4Fnyw?rel=0]

Vi har gjort det enkelt for deg å invitere den eksterne regnskapsføreren. Bare åpne **Brukere**-siden, og velg deretter **Inviter ekstern regnskapsfører** i båndet. En e-post er opprettet slik at du bare legger til regnskapsførerens arbeids-e-post og sender invitasjonen.  

> [!Note]  
> Dette krever at du har definert SMTP-e-post. Hvis du vil ha mer informasjon, kan du se [Konfigurer e-post](admin-how-setup-email.md).  

<!-- ![Invite your accountant](./media/finance-invite-accountant/invite-accountant.png)-->

> [!IMPORTANT]  
> Regnskapsførerens e-postadresse må være en jobbadresse som er basert på Azure Active Directory. Hvis regnskapsføreren bruker en annen type e-post, kan ikke invitasjonen sendes.
>
> Denne oppgaven krever tilgang for å behandle brukere og lisenser i Azure Active Directory. Brukeren som sender denne invitasjonen, må tilordnes rollen som **Global administrator** eller **Brukeradministrator** i administrasjonssenteret for Microsoft 365. Hvis du vil ha mer informasjon, se [Om administratorroller](/microsoft-365/admin/add-users/about-admin-roles) i Microsoft 365-administratorinnholdet.  

### <a name="adding-your-accountant-to-your-microsoft-365-in-the-azure-portal"></a>Legge til regnskapsføreren din i Microsoft 365 i Azure Portal

Hvis administratoren eller videresalgspartneren din ikke vil bruke veiledningen **Inviter ekstern regnskapsfører**, kan de legge til en ekstern bruker i Azure Portal og tilordne denne brukeren lisensen for *Ekstern regnskapsfører*. Hvis du vil ha mer informasjon, kan du se [Hurtigstart: Legge til gjestebrukere i katalogen i Azure-portalen](/azure/active-directory/b2b/b2b-quickstart-add-guest-users-portal).

#### <a name="to-add-your-accountant-as-a-guest-user"></a>Slik legger du til regnskapsføreren din som gjestebruker

1. Åpne [Azure-portalen](https://portal.azure.com/).
2. I den venstre ruten velger du **Azure Active Directory**.
3. Under **Administrer** velger du **Brukere**.
4. Velg **Ny gjestebruker**.
5. På siden **Ny bruker** velger du **Inviter bruker** og legger deretter til informasjon om den eksterne regnskapsføreren.  

   Du kan også inkludere en personlig velkomstmelding til regnskapsføreren for å la de vite at du legger de til i [!INCLUDE[prodshort](includes/prodshort.md)].

6. Velg **Inviter** for å sende invitasjonen automatisk. Det vises et varsel øverst til høyre om at **brukeren er invitert**. 
7. Når du har sendt invitasjonen, legges brukerkontoen automatisk til i mappen som gjest.

Deretter må du tilordne den nye gjestebrukeren en lisens til [!INCLUDE[prodshort](includes/prodshort.md)].

#### <a name="to-give-your-accountant-access-to-your-prodshort"></a>Slik gir du regnskapsføreren tilgang til [!INCLUDE[prodshort](includes/prodshort.md)]

1. I Azure-portalen velger du **Profil** for brukeren som nylig er lagt til,og deretter velger du **Rediger**.
2. Oppdater feltet **Brukssted** til det aktuelle landet, og velg deretter **Lagre**.
3. Velg **Lisenser**, og åpne deretter **Tilordninger**.
4. Velg lisensen **Dynamics 365 Business Central ekstern regnskapsfører**.  

    Hvis denne lisensen ikke er tilgjengelig, må du i stedet bruke en tilgjengelig lisensen av typen **Dynamics 365 Business Central for IW-er**.
5. Lagre tilordningen.

Hvis vellykket, er lisensen tilordnet til gjestebruker, og gjestekontoen er opprettet.

### <a name="importing-the-new-user-into-prodshort"></a>Importere den nye brukeren til [!INCLUDE[prodshort](includes/prodshort.md)]

Regnskapsføreren vil motta en e-post som varsler dem om at de har fått tilgang til Active Directory. Deretter må du gi dem tilgang til det rette selskapet i [!INCLUDE[prodshort](includes/prodshort.md)].

#### <a name="to-add-the-accountant-to-the-right-company"></a>Slik legger du til regnskapsføreren i det rette selskapet

1. Åpne [!INCLUDE[prodshort](includes/prodshort.md)]-selskapet du vil gi regnskapsføreren tilgang til, på [https://businesscentral.dynamics.com](https://businesscentral.dynamics.com).
2. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Brukere**, og velg deretter den relaterte koblingen.  
3. Velg handlingen **Hent nye brukere fra Office 365**.

Dette importerer brukerkontoen du opprettet i Azure-portalen, til selsksapet. Hvis du vil ha mer informasjon, kan du se [Slik legger du til en bruker i Business Central](ui-how-users-permissions.md#adduser).  

Hvis du vil gi tilgang til flere firmaer, må du logge deg på hvert firma og gjenta denne prosessen. Du kan også oppdatere tillatelsesgruppene for regnskapsførerens brukerprofil i [!INCLUDE[prodshort](includes/prodshort.md)], for eksempel tilordne dem *D365 Bus Premium*-brukergruppen. Hvis du vil ha mer informasjon, kan du se [Tilordne tillatelser til brukere og grupper](ui-define-granular-permissions.md).  

## <a name="see-also"></a>Se også

[Finans](finance.md)  
[Konfigurere finans](finance-setup-finance.md)  
[Finans og kontoplanen](finance-general-ledger.md)  
[Avslutte år og perioder](year-close-years-periods.md)  
[Arbeide med dimensjoner](finance-dimensions.md)  
[Analysere årsregnskap i Excel](finance-analyze-excel.md)  
[Administrere arbeid på tvers av flere selskaper i selskapshuben](company-hub.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Definere kontantstrømanalyse](finance-setup-cash-flow-analyses.md)  
