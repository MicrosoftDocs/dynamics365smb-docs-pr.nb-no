---
title: "Regnskapsføreropplevelsen i Dynamics 365 | Microsoft-dokumentasjon"
description: "Lære om Accountant Hub for Dynamics 365."
author: edupont04
ms.service: dynamics365-accountant
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 05/09/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 75501b9402bb1c14fcfeb2fc6e61f055a2247493
ms.openlocfilehash: 8901216a843440e922ae4df9d7508b543a6c1322
ms.contentlocale: nb-no
ms.lasthandoff: 05/15/2018

---
# <a name="get-started-with-include-d365acclongincludesd365acclongmdmd"></a>Kom i gang med [!INCLUDE [d365acc_long](includes/d365acc_long_md.md)]
[!INCLUDE [d365fin_early_release](includes/d365fin_early_release.md.md)]

Alle virksomheter må føre regnskap og godkjenne regnskapet. Enkelte virksomheter bruker en ekstern regnskapsfører, og andre har en regnskapsfører ansatt. Hvis du er en regnskapsfører med flere klienter, kan du bruke [!INCLUDE [d365acc](includes/d365acc_md.md)] som instrumentbord for å få en bedre oversikt over klientene dine.  

Du kan få tilgang til [!INCLUDE [d365acc](includes/d365acc_md.md)] ved å registrere deg fra [Dynamics 365 – Accountant Hub på Microsoft.com](https://www.microsoft.com/en-us/dynamics365/financial-insights-for-accountants).  

> [!TIP]
>  Når du registrerer deg for [!INCLUDE [d365acc](includes/d365acc_md.md)], må du angi et e-postadressen din, for eksempel <em>me@accountant.com</em>. Vi anbefaler at du bruker den samme e-postadressen når du arbeider i dine kunders [!INCLUDE [d365fin_long](includes/d365fin_long_md.md)], slik at du kan bytte mellom klienter. E-postadressen må være en jobbadresse som er basert på Active Directory.

## <a name="working-with-individual-clients"></a>Arbeide med individuelle klienter
Instrumentbordet viser de viktigste opplysningene om hver klient.  
![Accountant Hub](./media/accountant-get-started/accountant-dashboard-tasks.png)

Kolonnen **Klientnavn** viser navnene på klientene dine, og kolonnen **Selskapsnavn** viser alle selskapene, hvis klienten har flere selskaper i [!INCLUDE [d365fin_long](includes/d365fin_long_md.md)]. Det finnes også felt som viser oppgavene som er tilordnet til deg i kundens selskap, inkludert forfalte oppgaver.  

Du kan tilpasse instrumentbordet slik at de ønskede datapunktene vises, ved å legge til eller fjerne kolonner. Du kan for eksempel vise avgifter som er forfalt, hvor mange åpne salgsdokumenter hver klient har, eller antall kjøpsfakturaer som forfaller neste uke. Du kan konfigurere visningen etter behov. Hvis du har mange klienter, kan du bruke filtre til å sortere visningen.  

Ellipsen (...) ved siden av klientnavnet viser en kort meny:

- Oppdater gjeldende selskap og hent nye data for klienten  
- Gå til klientens [!INCLUDE [d365fin](includes/d365fin_md.md)]  
- Velg flere klienter  

Likeledes kan du for eksempel bruke rullegardinmenyen **Klientsammendrag** til å oppdatere alle selskapene.  

> [!TIP]
>  Du får tilgang til en klients [!INCLUDE [d365fin](includes/d365fin_md.md)] ved å velge menyelementet **Gå til klient**. Du logges på automatisk.

## <a name="company-details"></a>Opplysninger om selskap
Du finner mer informasjon om dataene til klientene dine ved å velge navnet på selskapet som du vil lære mer om. Dette åpnes **Selskapsnavn**-ruten, der du kan se mer informasjon, for eksempel følgende:  

* Saldo for kontantkontoer  
* Kontantstrømprognose  
* Forfalte kjøpsfakturaer  
* Forfalte salgsfakturaer  

![Klientselskapsdetaljer i regnskapsførerens instrumentbord](./media/accountant-get-started/accountant-company-details.png)

Teknisk sett du har nå logget deg på kundens [!INCLUDE [d365fin](includes/d365fin_md.md)], og dataene du ser, er aktive data. Hvis du vil se nærmere på dataene, for eksempel en forfalt kjøpsfaktura, velger du koblingen, og du kommer til klientselskapet.  

> [!TIP]
>  Du kan starte forhåndsdefinerte Excel-arbeidsbøker fra **Rapporter**-fanen på båndet. Disse Excel-arbeidsbøkene er utformet som klare til å skrive ut viktige regnskap og rapporter, men du kan også endre dem. etter behov. Hvis du vil ha mer informasjon, se [Analysere årsregnskap i Microsoft Excel](/dynamics365/business-central/finance-analyze-excel?toc=/dynamics365/accountants/toc.json) for hjelp om [!INCLUDE [d365fin](includes/d365fin_md.md)].  

Ellers kan du lukke detaljervinduet og gå videre til neste klient.  

## <a name="assigned-tasks"></a>Tilordnede oppgaver
I klientens [!INCLUDE [d365fin](includes/d365fin_md.md)] kan du tilordne oppgaver til deg selv og andre, og andre kan tilordne oppgaver til deg. Instrumentbordet i [!INCLUDE [d365acc](includes/d365acc_md.md)] gir deg en oversikt over tilordnede oppgaver for hver klient, og du får også tilgang til en oversikt over alle tilordnede oppgaver ved å velge **Mine brukeroppgaver** til venstre.  

I klientselskapet har du også bunker som fremheve oppgaver som er tilordnet til deg i denne bestemte klienten.

![Oppgavene som er tilordnet regnskapsføreren i klientselskapet](./media/accountant-get-started/accountant-company-details-tasks.png)

### <a name="my-user-tasks"></a>Mine brukeroppgaver
**Mine brukeroppgaver**-listen i [!INCLUDE [d365acc](includes/d365acc_md.md)] hjelper deg med å prioritere dagen ved å vise mer informasjon om oppgaver som er tilordnet til deg, for alle kundene dine.  

![Oversikt over oppgavene som er tilordnet til meg som en ekstern regnskapsfører](./media/accountant-get-started/accountant-tasklist.png)

Du kan sortere etter forfallsdato, for eksempel, eller andre typer data som hjelper deg med å prioritere dagen. Oversikten viser alle aktiviteter som er tilordnet til deg, som standard, men du kan definere filtre for bare å vise oppgaver som for eksempel er merket med høy prioritet.

For å plukke opp en oppgave, velger du den ganske enkelt fra listen over ventende brukeroppgaver. I båndet åpner **Gå til oppgaveelement**-koblingen vinduet der du kan gjøre oppgaven.  

Når du har fullført en oppgave, merker du den som fullført.  

## <a name="see-also"></a>Se også
[Legge til klienter på skrivebordet i [!INCLUDE[d365acc](includes/d365acc_md.md)]](add-client.md)  
[Velkommen til [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)]](index.md)  
[Analysere årsregnskap i Microsoft Excel](/dynamics365/business-central/finance-analyze-excel?toc=/dynamics365/accountants/toc.json)   
[Regnskapsføreropplevelser i [!INCLUDE[d365fin](includes/d365fin_md.md)]](/dynamics365/business-central/finance-accounting?toc=/dynamics365/accountants/toc.json)  
[Dynamics 365: Accountant Hub på Microsoft.com](https://www.microsoft.com/en-us/dynamics365/financial-insights-for-accountants)  

