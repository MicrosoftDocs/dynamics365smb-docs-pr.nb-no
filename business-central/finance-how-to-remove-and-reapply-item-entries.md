---
title: Fjern vareposter og utligne dem på nytt
description: Du kan vise og manuelt endre bestemte vareutligningsposter som opprettes automatisk under lagertransaksjoner.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '506, 521, 9125'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Fjerne varefinansposter og utligne dem på nytt
På siden **Utligningsforslag** kan du vise og manuelt endre bestemte vareutligningsposter som opprettes automatisk under lagertransaksjoner.  

Når du bokfører en transaksjon der varer går inn på eller ut av lageret, blir det opprettet en vareutligning mellom hver lagerøkning og lagerreduksjon. Disse utligningene fastsetter kostflyten fra varene som mottas på lageret, til kosten for varer som går ut av lageret. På grunn av måten som enhetskostbeløpet beregnes på, kan en feil vareutligning føre til en skjev gjennomsnittskost og en skjev enhetskost. Hvis du vil ha mer informasjon, kan du se Designdetaljer: Vareutligning.

Følgende scenarier kan kreve at du må angre en utligning eller utligne vareposter på nytt:

- Du har glemt å opprette en fast utligning.
- Du har opprettet en feil fast utligning.
- Du må returnere en vare som et salg allerede er utlignet mot.

Hvis det er mulig, bruker du et dokument til å utligne en varepost på nytt. Hvis du for eksempel må opprette en bestillingsretur for en vare som et salg allerede er utlignet mot, kan du utligne på nytt ved ganske enkelt å opprette og bokføre bestillingsreturdokumentet ved å bruke den riktige utligningen i feltet **Utligningsvarepost** på bestillingsreturlinjen. Du kan bruke funksjonen **Hent bokførte dokumentlinjer som skal tilbakeføres** eller **Kopier fra dokument** i bestillingsreturdokumentet for å gjøre dette enklere. Når du bokfører dokumentet, utlignes vareposten automatisk på nytt. Hvis du vil ha mer informasjon, kan du se [Behandle bestillingsreturer eller annulleringer](purchasing-how-process-purchase-returns-cancellations.md).

Hvis du ikke kan bruke et dokument til å utligne på nytt, for eksempel når du må korrigere en fast utligning, bruker du siden **Utligningsforslag** til å korrigere en utligning.

> [!Warning]  
> Det er viktig å være oppmerksom på følgende når du arbeider med utligningsforslaget:
    - Du bør ikke la utligningen av utligningsposter være opphevet i lange tidsperioder, fordi andre brukere ikke kan behandle varene før du utligner utligningspostene på nytt eller lukker siden **Utligningsforslag**. Brukere som prøver å utføre handlinger som omfatter en manuelt opphevet utligningspost, får følgende feilmelding: "Du kan ikke utføre denne handlingen ettersom utligningen av poster for varen XXX er opphevet i Utligningsforslag av brukeren XXX."
    - Du bør bare utligne vareposter på nytt utenfor arbeidstiden for å unngå eventuelle konflikter med andre brukere som bokfører transaksjoner med de samme varene.
    - Når du lukker utligningsforslaget, utfører [!INCLUDE[prod_short](includes/prod_short.md)] en kontroll for å sikre at alle poster er utlignet. Hvis du for eksempel fjerner en antallsutligning, men ikke oppretter en ny utligning, og deretter lukker utligningsforslaget, opprettes en ny utligning. Dette er med på å holde kostbeløpet intakt. Hvis du imidlertid fjerner en fast utligning, opprettes ikke en ny fast utligning automatisk når du lukker forslaget. Du må gjøre dette manuelt ved å opprette en ny utligning i forslaget.
    - Du kan fjerne utligninger fra flere enn én post om gangen i utligningsforslaget. Siden utligning av poster påvirker settet med poster som er tilgjengelige for utligning, kan du imidlertid ikke opprette en utligning for flere enn én post om gangen.
    - Utligningsforslaget kan ikke opprette en utligning i følgende situasjon: Hvis det ikke er et stort nok antall på lager til å utligne, kan ikke utligningsforslaget opprette en utligning når du prøver å utligne en lagerreduksjonspost uten varesporingsinformasjon mot en lagerøkningspost med varesporingsinformasjon.

## Slik fjerner du en vareutligning med utligningsforslaget

1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Utligningsforslag**, og velg deretter den relaterte koblingen.  
2.  Siden **Utligningsforslag** åpnes med eksisterende vareposter for alle varer.  
3.  Angi filtre på hurtigfanen **Generelt** for å gjøre det enklere å finne vareposten du vil endre bruken for.  
4.  Velg vareposten, og velg deretter handlingen **Utlignede poster**. Siden **Vis utlignede poster – utlignede poster** åpnes med vareposten(e) som utlignes mot den valgte posten.  
5.  Velg vareposten som du vil fjerne utligningen for.  
6.  Velg handlingen **Fjern utligning**. Dermed fjernes vareutligningsposten som forbinder de to varepostene, og den flyttes til siden **Vis utlignede poster – Poster som skal utlignes**.  
7.  Lukk siden **Vis utlignede poster – Utlignede poster**.  

 **Restantall**-feltet for de to varepostene økes med antallet som utligningen er opphevet for. Den fjernede vareposten er nå tilgjengelig for ny utligning på siden **Vis utlignede poster – Poster som skal utlignes**.  

> [!IMPORTANT]  
>  Du bør ikke la utligningen av utligningsposter være opphevet i lange tidsperioder, fordi andre brukere ikke kan behandle de berørte varene før du utligner utligningspostene på nytt eller lukker siden **Utligningsforslag**. Følgende feilmelding vises hvis du prøver å utføre handlinger som involverer en manuelt opphevet utligningspost:  
>   
>  **Du kan ikke utføre denne handlingen ettersom utligningen av poster for varen \<item\> er opphevet i Utligningsforslag av brukeren \<user\>.**  

## Slik bruker du en vareutligning på nytt med utligningsforslaget

1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 2.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Utligningsforslag**, og velg deretter den relaterte koblingen.  
2.  Siden **Utligningsforslag** åpnes med eksisterende vareposter for alle varer.  
3.  Hvis du vil utligne poster som ble fjernet siden forslaget ble åpnet, på nytt, velger du varepost du vil utligne på nytt, og velg deretter handlingen **Utligne på nytt**.  

    > [!NOTE]  
    >  Denne nye utligningen mot den opprinnelige balansen skjer automatisk når du lukker siden **Utligningsforslag**.  
4.  Hvis du vil bruke en tilgjengelig åpen varepost med en annen oppføring, velger du vareposten du vil bruke. Velg handlingen **Poster som skal utlignes**. Siden **Vis utlignede poster – Poster som skal utlignes** åpnes.  
5.  Velg én eller flere vareposter du vil utligne mot posten som er valgt på siden **Utligningsforslag**, og klikk deretter på **OK**-knappen.  

     En vareutligningspost opprettes mellom de to varepostene. **Restantall**-feltene for de to postene reduseres med det utlignede antallet.  

    > [!NOTE]  
    >  Hvis du har valg å opprette en utligning som hadde forårsaket en uendelig sløyfe i kostjusteringsprosessen, opprettes ikke utligningen du foreslo. Dette kan skje når de opprinnelige postene opprettet negativ beholdning. Utligningen er ikke gjort. Du må derfor velge en annen post for utligningen.  
6.  Hvis du angir **Alltid** i feltet **Automatisk kostjustering** i **lageroppsettet**, kjører programmet automatisk kjørselen for kostjustering etter at du har opprettet en ny utligning. Ellers starter du kjørselen **Juster kostverdi - vareposter** for å sikre at all kost er oppdatert.  

## Se også

[Lukke åpne vareposter som er resultat av fast utligning i varekladden](finance-how-to-close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal.md)  
 [Behandle bestillingsreturer eller annulleringer](purchasing-how-process-purchase-returns-cancellations.md)  
 [Administrere lagerkostnader](finance-manage-inventory-costs.md)   
 [Designdetaljer: Vareutligning](design-details-item-application.md)  
 [Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]