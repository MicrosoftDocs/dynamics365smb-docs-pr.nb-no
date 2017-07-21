---
title: "Regnskapsføreropplevelsen i Financials | Microsoft-dokumentasjon"
description: "Få informasjon om regnskapsførerportalen for Dynamics 365 for Financials og rollesenter for regnskapsfører som støtter regnskapsføreren i klientselskapet."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 06/20/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: bef1e9097a958c2f447e64ff33c7081a1d305f38
ms.contentlocale: nb-no
ms.lasthandoff: 07/07/2017


---
# <a name="accountant-experiences-in-included365finincludesd365finmdmd"></a>Regnskapsføreropplevelser i [!INCLUDE[d365fin](includes/d365fin_md.md)]
Alle virksomheter må føre regnskap og godkjenne regnskapet. Enkelte virksomheter bruker en ekstern regnskapsfører, og andre har en regnskapsfører ansatt. Uansett hvilken type regnskapsfører du er, kan du bruke rollesenteret **Revisor** som hjemmet ditt i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Herfra har du tilgang til alle vinduene du trenger i arbeidet.  

## <a name="accountant-role-center"></a>Rollesenter for regnskapsfører
Rollesenteret er et instrumentbord med aktivitetsfliser som viser deg nøkkeltall i sanntid og gir deg rask tilgang til data. På båndet øverst i vinduet har du tilgang til flere handlinger. I navigasjonsruten til venstre kan du raskt bytte mellom oversiktene du bruker mest. Hvis du utvider **Hjem**-menyen i navigasjonsruten, vises andre områder, for eksempel **Bokførte bilag** med de ulike bilagstypene selskapet har bokført.  

Hvis [!INCLUDE[d365fin](includes/d365fin_md.md)] er nytt for deg, kan du vise en oversikt over videoer rett fra hjemmesiden. Du kan også starte **Komme i gang**, som angir viktige områder.  

> [!NOTE]  
>  Denne funksjonen krever at opplevelsen er satt til **Løsning**. Hvis du vil ha mer informasjon, kan du se [Tilpasse Financials-opplevelsen](ui-experiences.md).  

### <a name="get-invited-to-a-clients-included365finincludesd365finmdmd"></a>Bli invitert til en klients [!INCLUDE[d365fin](includes/d365fin_md.md)]
Et selskap som bruker [!INCLUDE[d365fin](includes/d365fin_md.md)], kan invitere deg til [!INCLUDE[d365fin](includes/d365fin_md.md)] som deres eksterne regnskapsfører. Dette krever at en administrator legger til din e-postadresse for arbeid i Active Directory-leieren sin, og vi anbefaler at de kontakter [!INCLUDE[d365fin](includes/d365fin_md.md)]-partneren for å få hjelp. Vi anbefaler også at du angir e-postadressen du har tenkt å bruke i regnskapsarbeidet. På denne måten kan du velge om du vil bruke *me@accountant.com* eller *me@client.com*  

Det kan dermed hende at du mottar to e-postmeldinger:

-   Én fra Microsoft Invitations med en kobling for å legge til deg selv i klientens organisasjon  
-   Én fra klienten med en kobling til deres [!INCLUDE[d365fin](includes/d365fin_md.md)]  

Du har deretter tilgang til de økonomiske dataene deres fra rollesenteret **Revisor**. Hvis du bruker utvidelsen **Regnskapsførerportal**, kan du også legge til denne klienten i oversikten over klienter på instrumentbordet i regnskapsførerportalen.  

## <a name="accountant-portal"></a>Regnskapsførerportal
Hvis du er en regnskapsfører med flere klienter, kan du bruke regnskapsførerportalen som instrumentbord for å få en bedre oversikt over klientene dine. Herfra har du tilgang til hver klients leier i [!INCLUDE[d365fin](includes/d365fin_md.md)], og du kan bruke rollesenter for regnskapsfører som beskrevet ovenfor.  

Regnskapsførerportalen er en dedikert versjon av [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du får tilgang til portalen ved å registrere deg fra [Financials for regnskapsførere på Microsoft.com](https://www.microsoft.com/en-us/dynamics365/financial-insights-for-accountants), og ved å legge til [utvidelsen Regnskapsførerportal](ui-extensions-accountant-portal.md) i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

> [!TIP]  
>  Når du registrerer deg for regnskapsførerportalen, må du angi e-postadressen din for arbeid, for eksempel *me@accountant.com*. Vi anbefaler at du bruker samme e-postadresse når du arbeider i klientenes [!INCLUDE[d365fin](includes/d365fin_md.md)], slik at du enkelt kan bytte mellom klienter.  

Når du logger på regnskapsførerportalen første gang, vises en eksempelklient på instrumentbordet for å hjelpe deg å komme i gang. Du kan fjerne eksempelklienten når du føler at du ikke lenger trenger den.  

### <a name="working-with-individual-clients"></a>Arbeide med individuelle klienter
Instrumentbordet viser de viktigste opplysningene om hver klient.  
[![Regnskapsførerportal](./media/ui-extensions-accportal/accountant-portal.png)](https://go.microsoft.com/fwlink/?linkid=851257)

Kolonnen **Klientnavn** viser navnene på klientene dine, og kolonnen **Selskapsnavn** viser alle selskapene, hvis klienten har flere selskaper i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du kan tilpasse instrumentbordet slik at de ønskede datapunktene vises, ved å legge til eller fjerne kolonner. Du kan for eksempel vise avgifter som er forfalt, hvor mange åpne salgsdokumenter hver klient har, eller antall kjøpsfakturaer som forfaller neste uke. Du kan konfigurere visningen etter behov. Hvis du har mange klienter, kan du bruke filtre til å sortere visningen.  

De tre ellipsene ved siden av klientnavnet viser en kort meny:

-   Oppdater gjeldende selskap og hent nye data for klienten  
-   Gå til klientens [!INCLUDE[d365fin](includes/d365fin_md.md)]  
-   Velg flere klienter  

Likeledes kan du for eksempel bruke rullegardinmenyen **Klientsammendrag** til å oppdatere alle selskapene.  

Alt annet arbeid du gjør for hver kunde, kan du gjøre i rollesenter for regnskapsfører i deres [!INCLUDE[d365fin](includes/d365fin_md.md)].  

> [!TIP]  
>  Du får tilgang til en klients [!INCLUDE[d365fin](includes/d365fin_md.md)] ved å velge menyelementet **Gå til klient**. Du logges på automatisk.

### <a name="adding-clients"></a>Legge til klienter
Du kan legge til en klient ved å bruke **Klienter**-vinduet, som du kan åpne ved å velge handlingen **Administrer klienter** på båndet. Velg ganske enkelt **Ny**, og fyll deretter ut feltene.  

Dataene på kortet for hver klient angis av deg, og du kan endre dem etter behov. Feltet **URL-adresse til klient** er avgjørende – det er slik du får tilgang til hver klients [!INCLUDE[d365fin](includes/d365fin_md.md)]. Bruk handlingen **Test URL-adresse til klient** på båndet for å teste at du har angitt riktig kobling. URL-adressen du må angi, peker mot klientens [!INCLUDE[d365fin](includes/d365fin_md.md)], for eksempel *https://mybusiness.financials.dynamics.com*. Denne URL-adressen brukes deretter når du velger menyelementet **Gå til klient**.  

<!--If you have been invited to a client's [!INCLUDE[d365fin](includes/d365fin_md.md)] and signed in with your work account, then the client will be added to your dashboard in the accountant portal. -->

## <a name="see-also"></a>Se også
[Finans](finance.md)  
[Konfigurere finans](finance-setup-finance.md)  
[Finans og kontoplanen](finance-general-ledger.md)  
[Avslutte år og perioder](year-close-years-periods.md)  
[Sortering](ui-sorting.md)  
[Angi vilkår i filtre](ui-enter-criteria-filters.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Invitere den eksterne regnskapsføreren til [!INCLUDE[d365fin](includes/d365fin_md.md)]](finance-invite-external-accountant.md)  
[Financials for regnskapsførere på Microsoft.com](https://www.microsoft.com/en-us/dynamics365/financial-insights-for-accountants)  

