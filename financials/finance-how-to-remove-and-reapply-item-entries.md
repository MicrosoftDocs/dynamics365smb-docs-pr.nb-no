---
title: "Fjerne varefinansposter og utligne dem på nytt | Microsoft-dokumentasjon"
description: Du kan vise og manuelt endre bestemte vareutligningsposter som opprettes automatisk under lagertransaksjoner.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 12bde7fc508bb29e56ad63d76b526a80b5073f03
ms.contentlocale: nb-no
ms.lasthandoff: 01/30/2018

---
# <a name="remove-and-reapply-item-ledger-entries"></a>Fjerne varefinansposter og utligne dem på nytt
I vinduet **Utligningsforslag** kan du vise og manuelt endre bestemte vareutligningsposter som opprettes automatisk under lagertransaksjoner.  

Når du bokfører en transaksjon der varer går inn på eller ut av lageret, blir det opprettet en vareutligning mellom hver lagerøkning og lagerreduksjon. Disse utligningene fastsetter kostflyten fra varene som mottas på lageret, til kosten for varer som går ut av lageret. På grunn av måten som enhetskostbeløpet beregnes på, kan en feil vareutligning føre til en skjev gjennomsnittskost og en skjev enhetskost. Hvis du vil ha mer informasjon, kan du se Designdetaljer: Vareutligning.

Følgende scenarier kan kreve at du må angre en utligning eller utligne vareposter på nytt:

- Du har glemt å opprette en fast utligning.
- Du har opprettet en feil fast utligning.
- Du må returnere en vare som et salg allerede er utlignet mot.

Hvis det er mulig, bruker du et dokument til å utligne en varepost på nytt. Hvis du for eksempel må opprette en bestillingsretur for en vare som et salg allerede er utlignet mot, kan du utligne på nytt ved ganske enkelt å opprette og bokføre bestillingsreturdokumentet ved å bruke den riktige utligningen i feltet **Utligningsvarepost** på bestillingsreturlinjen. Du kan bruke funksjonen **Hent bokførte dokumentlinjer som skal tilbakeføres** eller **Kopier dokument** i bestillingsreturdokumentet for å gjøre dette enklere. Når du bokfører dokumentet, utlignes vareposten automatisk på nytt. Hvis du vil ha mer informasjon, kan du se [Behandle bestillingsreturer eller annulleringer](purchasing-how-process-purchase-returns-cancellations.md).

Hvis du ikke kan bruke et dokument til å utligne på nytt, for eksempel når du må korrigere en fast utligning, bruker du vinduet **Utligningsforslag** til å korrigere en utligning.

> [!Warning]  
> Det er viktig å være oppmerksom på følgende når du arbeider med utligningsforslaget:
    - Du bør ikke la utligningen av utligningsposter være opphevet i lange tidsperioder, fordi andre brukere ikke kan behandle varene før du utligner utligningspostene på nytt eller lukker vinduet **Utligningsforslag**. Brukere som prøver å utføre handlinger som omfatter en manuelt opphevet utligningspost, får følgende feilmelding: "Du kan ikke utføre denne handlingen ettersom utligningen av poster for varen XXX er opphevet i Utligningsforslag av brukeren XXX."
    - Du bør bare utligne vareposter på nytt utenfor arbeidstiden for å unngå eventuelle konflikter med andre brukere som bokfører transaksjoner med de samme varene.
    - Når du lukker utligningsforslaget, utfører [!INCLUDE[d365fin](includes/d365fin_md.md)] en kontroll for å sikre at alle poster er utlignet. Hvis du for eksempel fjerner en antallsutligning, men ikke oppretter en ny utligning, og deretter lukker utligningsforslaget, opprettes en ny utligning. Dette er med på å holde kostbeløpet intakt. Hvis du imidlertid fjerner en fast utligning, opprettes ikke en ny fast utligning automatisk når du lukker forslaget. Du må gjøre dette manuelt ved å opprette en ny utligning i forslaget.
    - Du kan fjerne utligninger fra flere enn én post om gangen i utligningsforslaget. Siden utligning av poster påvirker settet med poster som er tilgjengelige for utligning, kan du imidlertid ikke opprette en utligning for flere enn én post om gangen.
    - Utligningsforslaget kan ikke opprette en utligning i følgende situasjon: Hvis det ikke er et stort nok antall på lager til å utligne, kan ikke utligningsforslaget opprette en utligning når du prøver å utligne en lagerreduksjonspost uten varesporingsinformasjon mot en lagerøkningspost med varesporingsinformasjon.

## <a name="to-remove-an-item-application-by-using-the-application-worksheet"></a>Slik fjerner du en vareutligning med utligningsforslaget  
1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Utligningsforslag**, og velg deretter den relaterte koblingen.  
2.  Vinduet **Utligningsforslag** åpnes med eksisterende vareposter for alle varer.  
3.  Angi filtre på hurtigfanen **Generelt** for å gjøre det enklere å finne vareposten du vil endre bruken for.  
4.  Velg vareposten, og velg deretter handlingen **Utlignede poster**. Vinduet **Vis utlignede poster – utlignede poster** åpnes med vareposten(e) som utlignes mot den valgte posten.  
5.  Velg vareposten som du vil fjerne utligningen for.  
6.  Velg handlingen **Fjern utligning**. Dermed fjernes vareutligningsposten som forbinder de to varepostene, og den flyttes til vinduet **Vis utlignede poster – Poster som skal utlignes**.  
7.  Lukk vinduet **Vis utlignede poster – Utlignede poster**.  

 **Restantall**-feltet for de to varepostene økes med antallet som utligningen er opphevet for. Den fjernede vareposten er nå tilgjengelig for ny utligning i vinduet **Vis utlignede poster – Poster som skal utlignes**.  

> [!IMPORTANT]  
>  Du bør ikke la utligningen av utligningsposter være opphevet i lange tidsperioder, fordi andre brukere ikke kan behandle de berørte varene før du utligner utligningspostene på nytt eller lukker vinduet **Utligningsforslag**. Følgende feilmelding vises hvis du prøver å utføre handlinger som involverer en manuelt opphevet utligningspost:  
>   
>  **Du kan ikke utføre denne handlingen ettersom utligningen av poster for varen <item> er opphevet i Utligningsforslag av brukeren <user>.**  

## <a name="to-reapply-an-item-application-by-using-the-application-worksheet"></a>Slik bruker du en vareutligning på nytt med utligningsforslaget  
1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Utligningsforslag**, og velg deretter den relaterte koblingen.  
2.  Vinduet **Utligningsforslag** åpnes med eksisterende vareposter for alle varer.  
3.  Hvis du vil utligne poster som ble fjernet siden forslaget ble åpnet, på nytt, velger du varepost du vil utligne på nytt. I fanebladet **Handlinger**, under **Funksjoner** velger du **Utligne på nytt**.  

    > [!NOTE]  
    >  Denne nye utligningen mot den opprinnelige balansen skjer automatisk når du lukker vinduet **Utligningsforslag**.  
4.  Hvis du vil bruke en tilgjengelig åpen varepost med en annen oppføring, velger du vareposten du vil bruke. Velg handlingen **Poster som skal utlignes**. Vinduet **Vis utlignede poster – Poster som skal utlignes** åpnes.  
5.  Velg én eller flere vareposter du vil utligne mot posten som er valgt i vinduet **Utligningsforslag**, og klikk deretter på **OK**-knappen.  

     En vareutligningspost opprettes mellom de to varepostene. **Restantall**-feltene for de to postene reduseres med det utlignede antallet.  

    > [!NOTE]  
    >  Hvis du har valg å opprette en utligning som hadde forårsaket en uendelig sløyfe i kostjusteringsprosessen, opprettes ikke utligningen du foreslo. Dette kan skje når de opprinnelige postene opprettet negativ beholdning. Utligningen er ikke gjort. Du må derfor velge en annen post for utligningen.  
6.  Hvis du angir **Alltid** i feltet **Automatisk kostjustering** i **lageroppsettet**, kjører programmet automatisk kjørselen for kostjustering etter at du har opprettet en ny utligning. Ellers starter du kjørselen **Juster kostverdi - vareposter** for å sikre at all kost er oppdatert.  

## <a name="see-also"></a>Se også  
[Lukke åpne vareposter som er resultat av fast utligning i varekladden](finance-how-to-close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal.md)  
 [Behandle bestillingsreturer eller annulleringer](purchasing-how-process-purchase-returns-cancellations.md)  
 [Administrere lagerkostnader](finance-manage-inventory-costs.md)   
 [Designdetaljer: Vareutligning](design-details-item-application.md)  
 [Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

