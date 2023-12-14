---
title: Avstemme bankkontoer ved hjelp av avstemmingshjelp
description: Finn ut hvordan du bruker Copilot til å avstemme bankkonti i Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.collection: get-started
ms.date: 10/25/2023
ms.custom: bap-template
---

# <a name="reconcile-bank-accounts-with-copilot-preview"></a>Avstemme bankkontoer med Copilot (forhåndsversjon)

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

Denne artikkelen forklarer hvordan du bruker bankkontoavstemmingshjelpen til å avstemme banktransaksjoner med poster i Business Central.

## <a name="about-bank-account-reconciliation-assist"></a>Om bankkontoavstemmingshjelpen

Bankkontoavstemmingshjelpen er et sett med KI-drevne funksjoner som hjelper deg med å avstemme bankkontoer. Bankkontoavstemmingshjelpen gir deg to forskjellige oppgaver gjennom Copilot:

- Forbedret samsvaring av transaksjoner med poster

   Du er kanskje allerede kjent med handlingen **Avstem automatisk** på siden **Bankkontoavstemming** som automatisk avstemmer de flere transaksjoner med poster. Vi kaller denne operasjonen *autoavstem*. Selv om autoavstem fungerer bra, kan algoritmene den bruker, noen ganger resultere i mange uavstemte transaksjoner. Copilot bruker KI-teknologi til å inspisere gjenværende transaksjoner og identifisere flere treff basert på datoer, beløp og beskrivelser. Hvis for eksempel flere fakturaer ble betalt som ett engangsbeløp av en kunde, avstemmer Copilot den ene bankkontoutdragslinjen med flere fakturaposter.
   
   Gå til [Avstemme bankkontoer med Copilot](#reconcile-bank-accounts-with-copilot).

- Foreslåtte finanskontoer

  For gjenværende banktransaksjoner som ikke kan samsvares med noen poster, sammenligner Copilot transaksjonsbeskrivelsen med finanskontonavn og foreslår den mest sannsynlige finanskontoen å bokføre til. Copilot kan for eksempel foreslå at transaksjoner med informasjonen «Drivstoffstopp 24» bokføres på «Transport»-kontoen.
  
   Gå til [Overføre banktransaksjoner uten samsvar til foreslåtte finanskonti](#transfer-unmatched-bank-transactions-to-suggested-general-ledger-accounts).


   
## <a name="prerequisites"></a>Forutsetninger

- Bankkontoavstemmingshjelpen aktiveres og startes. Denne oppgaven utføres av en administrator. [Finn ut mer om aktivering av Copilot- og KI-funksjoner](enable-ai.md).
- Bankkonti i Business Central som du vil avstemme, er koblet til en nettbankkonto eller konfigurert med importformat for bankkontoutdrag. 
- Du er kjent med bankkontoavstemming i Business Central, som beskrevet i [Avstemme bankkontoer](bank-how-reconcile-bank-accounts-separately.md). 

<!--H2s. Required. A how-to article explains how to do a task. The bulk of each H2 should be a procedure.-->
## <a name="reconcile-bank-accounts-with-copilot"></a>Avstemme bankkontoer med Copilot

<!-- Similar to the **Match Automatically** capability on the **Bank Acc. Reconciliation** page, Bank account reconciliation assist can also automatically matches transactions in banks statements with bank entries. The difference is that **Match Automatically** uses a native rules-based algorithm, while Bank account reconciliation assist is based AI technology though Copilot. Bank account reconciliation assist is intended to supplement the **Match Automatically** capability. While **Match Automatically** is fairly successful at matching transactions, there are some instances where it can't&mdash;which is where Bank account reconciliation assist comes. By using the **Reconcile with Copilot** action on **Bank Acc. Reconciliation** page, you can find even more matches.-->

Copilot i bankkontoavstemming er ment å brukes som et supplement til autoavstem-operasjonen. Når du bruker Copilot, kjøres derfor autoavstemmingoperasjonen først for å utføre de første treffene. Deretter kjører Copilot for å prøve å samsvare med transaksjoner som autoavstemmingsoperasjonen ikke håndterte.   

Det finnes to fremgangsmåter for å avstemme bankkontoer med Copilot. Du kan bruke Copilot til å starte en ny avstemming på en bankkonto direkte fra **bankkontoavstemmingslisten**, eller du kan bruke Copilot på en ny eller eksisterende avstemming på **bankkontoavstemmingskortet**.

# [Fra bankkontoavstemmingslisten](#tab/fromlist) 

Med denne fremgangsmåten kan du opprette og avstemme en ny bankkontoavstemming fra grunnen av. Denne fremgangsmåten krever at du velger bankkontoen og importerer bankkontoutdragsfilen hvis bankkontoen ikke er knyttet til en Internett-konto.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") angi **Bankkontoavstemming**, og velg deretter den relaterte koblingen. 
1. Velg handlingen **Avstem med Copilot** for å åpne vinduet **Avstem med Copilot**.
1. Sett feltet **Utfør avstemming for denne bankkontoen** til bankkontoen du vil avstemme.

   ![Viser vinduet for avstem med copilot for avstemming fra grunnen av](media/reconcile-bank-accounts-new-copilot.svg) 
 
1. Hvis den valgte bankkontoen ikke er knyttet til en nettbankkonto, må du importere bankkontoutdragsfilen. Hvis du vil importere filen, velger du enten verdien i feltet **Bruk transaksjonsdata fra**, eller du velger bindersknappen ved siden av **Generer**-knappen. Deretter bruker du **Velg filen som skal importeres** til å importere bankkontoutdragsfilen ved å dra den fra enheten eller bla gjennom enheten.
1. Hvis du vil avstemme med Copilot, velger du **Generer**.

   Copilot begynner å generere foreslåtte treff. Når det er fullført, åpner vinduet Avstem med Copilot resultatene av samsvarsprosessen.

1. Se gjennom de foreslåtte samsvarene som beskrives i delen nedenfor.

# [Fra et bankkontoavstemmingkort](#tab/fromcard) 

Med denne fremgangsmåten bruker du Copilot enten på en ny bankkontoavstemming som du oppretter manuelt, eller ved å redigere en eksisterende avstemming. 


1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") angi **Bankkontoavstemming**, og velg deretter den relaterte koblingen. 
1. Gjør ett av følgende:

   - Velg **Ny** for å starte en ny avstemming. 
   - Velg og åpne en eksisterende avstemming fra listen.
1. I kortet **Bankkontoavstemming** velger du **Avstem med Copilot**

   ![Viser avstemmingen med copilot-handlingen på bankkontoavstemmingskortet](media/bank-reconciliation-copilot-card.svg) 

   Copilot begynner å generere foreslåtte treff. Når det er fullført, åpner vinduet **Avstem med Copilot** resultatene av samsvarsprosessen. 

1. Se gjennom de foreslåtte samsvarene som beskrives i delen nedenfor. 
---

### <a name="review-save-or-discard-proposed-matches"></a>Gå gjennom, lagre eller forkast foreslåtte samsvar

Når du har kjørt Copilot, viser vinduet **Avstem med Copilot** de detaljerte resultatene, inkludert eventuelle foreslåtte samsvar. På dette tidspunktet er ingen treff som er foreslått av Copilot, lagret, så det gir deg muligheten til å inspisere forslagene og lagre eller forkaste i henhold til det du vil.

![Viser vinduet for avstem med copilot med foreslåtte samsvar](media/bank-reconciliation-copilot-window.png) 

Copilot-vinduet er delt inn i to deler. Den øvre delen gir noen generelle detaljer om resultatet, som beskrevet i tabellen nedenfor.  Den nedre delen for **foreslåtte samsvar** viser samsvarene som er foreslått av Copilot.

|Felt|Description|
|-|-|
|Automatisk avstemt|Angir hvor mange linjer i kontoutskriften som samsvares av autoavstemmingsoperasjonen. Velg verdien for å vise avstemmingskortet.  |
|Avstemt med Copilot|Angir hvor mange linjer i kontoutskriften der Copilot har forslag til samsvar. Du kan se detaljer om samsvarene i delen for **foreslåtte avstemminger**.|
|Utdrag – sluttsaldo|Angir sluttsaldoen på bankkontoutdraget som du avstemmer mot|
|Bokfør hvis fullstendig avstemt|Slå på denne bryteren hvis du vil bokføre bankkontoavstemmingen automatisk når alle linjene (100 %) samsvarer og du har valgt **Behold den**.|

#### <a name="save-or-discard-proposed-matches"></a>Lagre eller forkast foreslåtte samsvar

Gå gjennom de foreslåtte treffene linje for linje i delen for **foreslåtte samsvar**, og utfør deretter den aktuelle handlingen:

- Hvis du vil forkaste ett enkelt foreslått treff, merker du det i listen og velger deretter handlingen **Slett linje**.

- Hvis du vil forkaste alle foreslåtte treff og lukke Copilot-vinduet, velger du kast-knappen (papirkurv) ![Viser papirkurvikonet for sletting av alle Copilot-forslag om bankkontoavstemming](media/copilot-delete-trash-can.png) ved siden av **Behold den**-knappen nederst i vinduet.

   > [!NOTE]
   > Hvis du startet Copilot fra **Bankkontoavstemming**-kortet for en ny eller eksisterende avstemming, slettes bare Copilots foreslåtte samsvar. Samsvarene som er laget av autoavstemmingsoperasjonen, er allerede lagret.
   > 
   > Hvis du startet Copilot fra listen for **bankkontoavstemminger**, lagres ingenting, inkludert de importerte bankkontoutdragslinjene, autosamsvarene og Copilots foreslåtte samsvar.

- Hvis du vil bokføre den fullstendige avstemmingen automatisk når du lagrer den, slår du på bryteren **Bokfør hvis fullstendig avstemt**.  
- Hvis du vil lagre treffene som vises i Copilot-vinduet, velger du **Behold den**.


## <a name="transfer-unmatched-bank-transactions-to-suggested-general-ledger-accounts"></a>Overføre banktransaksjoner uten samsvar til foreslåtte finanskonti

I denne delen lærer du hvordan du bruker Copilot til å overføre ikke-avstemte bankkontoutdrag fra bankkontoposten til en finanskonto. Denne oppgaven kan bare utføres fra en eksisterende avstemming. 

1. Gå til listen **Bankkontoavstemminger**, og åpne den eksisterende avstemmingen som inneholder de ikke-avstemte linjene.

   Start med å åpne en eksisterende bankkontoavstemming. Dette trinnet gir deg en klar oversikt over eventuelle ikke-avstemte bankkontoutdragslinjer som må overføres til finanskontoen.

2. I ruten **Bankkontoutdragslinjer** identifiserer du ruten med bankutdragslinjer som ikke samsvarer, og velger én eller flere linjer du vil avstemme.

   Disse linjene er utdragslinjene som Copilot fokuserer på for overføring til finanskontoen.

3. Velg **Overfør til finanskonto** for å starte prosessen.

   ![Viser handlingen overføring til finanskonto på bankkontoavstemmingskortet](media/bank-reconciliation-transfer-gl-copilot-card.svg) 

   Dette trinnet ber Copilot om å begynne å generere forslag til overføringen.

4. Når Copilot er ferdig med å generere forslag, åpnes vinduet **Copilot-forslag til finanskontooverføring**.

   Dette vinduet viser forslagene i delen **foreslåtte samsvar**. Opplevelsen ligner på avstemming med Copilot.

   ![Viser overføringen til finans med siden for copilots foreslåtte samsvar for bankkontoavstemming](media/bank-reconciliation-gl-transfer-proposed-matches.png) 

5. Gå gjennom hvert forslag linje for linje for å sikre nøyaktigheten av de foreslåtte overføringene.

   - Hvis du driller ned på forslaget ved å velge det i listen, blir du tatt til en liste over kontoer. Herfra kan du velge en annen konto. Denne typen manuell korrigering er bare mulig når du bruker flyten **Overfør til finanskonto**, ikke i samsvarende flyt. 
   - Hvis du velger **Lagre...** ved siden av et forslag, kan du legge til tilordningen på siden **Tekst-til-konto-tilordning**, slik at neste gang denne teksten vises under samsvarsoperasjonen, blir den tilordnet den foreslåtte kontoen.

6. Forkast eller lagre forslag.

   - Hvis du vil forkaste et spesifikt forslag, velger du det i listen og velger deretter **Slett linje**. Hvis du vil forkaste alle forslag og avslutte Copilot, velger du forkast-knappen (papirkurv) ![Viser papirkurvikonet for sletting av alle Copilot-forslag om bankkontoavstemming](media/copilot-delete-trash-can.png) ved siden av **Behold den**-knappen nederst i vinduet.
   
   - Hvis forslagene oppfyller kravene dine og du vil lagre dem, velger du **Behold den**. 

      Dette trinnet bekrefter overføringen av de valgte forslagene fra bankkontoposten til finanskontoen. Den bokfører nye betalinger til de foreslåtte finanskontiene og bruker tilsvarende linjer på de resulterende bankkontopostene.

## <a name="next-steps"></a>Neste trinn

[Validere bankkontoavstemmingen](bank-how-reconcile-bank-accounts-separately.md#validate-your-bank-reconciliation)  

## <a name="see-also"></a>Se også
[Feilsøk Copilot- og KI-funksjoner](ai-copilot-troubleshooting.md)  
[Vanlige spørsmål om ansvarlig kunstig intelligens for bankavstemmingshjelp](faqs-bank-reconciliation.md)  
[Konfigurere banktjenester](bank-setup-banking.md)  
[Avstem bankkontoer](bank-how-reconcile-bank-accounts-separately.md)  
[Utligne betalinger automatisk og avstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md) 
