---
title: Avstemme bankkontoer med Copilot (forhåndsversjon)
description: Finn ut hvordan du bruker Copilot til å avstemme bankkonti i Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.collection:
  - get-started
  - bap-ai-copilot
ms.date: 06/13/2024
ms.custom: bap-template
---

# <a name="reconcile-bank-accounts-with-copilot-preview"></a>Avstemme bankkontoer med Copilot (forhåndsversjon)

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

Denne artikkelen forklarer hvordan bankkontoavstemmingshjelpen kan hjelpe deg med å avstemme banktransaksjoner med poster i Microsoft Dynamics 365 Business Central.

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

## <a name="about-bank-account-reconciliation-assist"></a>Om bankkontoavstemmingshjelpen

Bankkontoavstemmingshjelpen er et sett med KI-drevne funksjoner som hjelper deg med å avstemme bankkontoer. Den har to distinkte oppgaver gjennom Copilot:

- Forbedret samsvaring av transaksjoner med poster

    Du er kanskje allerede kjent med knappen **Avstem automatisk** på siden **Bankkontoavstemming**, som automatisk avstemmer de flere transaksjoner med poster. Vi kaller denne operasjonen *autoavstem*. Selv om autoavstem fungerer bra, kan algoritmene den bruker, noen ganger resultere i mange uavstemte transaksjoner. Copilot bruker KI-teknologi til å inspisere ikke-avstemte transaksjoner og identifisere flere treff basert på datoer, beløp og beskrivelser. Hvis for eksempel en kunde betalte flere fakturaer som ett engangsbeløp, avstemmer Copilot den ene bankkontoutdragslinjen med flere fakturaposter.

    [Finn ut mer om denne oppgaven](#reconcile-bank-accounts-with-copilot).

- Foreslåtte finanskontoer

    For gjenværende banktransaksjoner som ikke kan samsvares med noen poster, sammenligner Copilot transaksjonsbeskrivelsen med finanskontonavn og foreslår deretter den mest sannsynlige finanskontoen å bokføre til. Hvis transaksjoner uten avstemming har informasjonen *Drivstoffstopp 24*, kan Copilot foreslå at du bokfører dem på *Transport*-kontoen.

    [Finn ut mer om denne oppgaven](#post-unmatched-bank-transaction-amounts-to-suggested-gl-accounts).

## <a name="available-languages"></a>Tilgjengelige språk

[!INCLUDE[bank-recon-assist-language-support](includes/bank-recon-assist-language-support.md)]

## <a name="prerequisites"></a>Forutsetninger

- Bankkontoavstemmingshjelpen aktiveres. En administrator må utføre denne oppgaven. [Finn ut mer om hvordan du konfigurerer Copilot- og KI-funksjoner](enable-ai.md).
- Bankkontoene i Business Central som du vil avstemme, er koblet til en nettbankkonto eller konfigurert med et importformat for bankkontoutdrag.
- Du er kjent med bankkontoavstemming i Business Central, som beskrevet i [Avstemme bankkontoer](bank-how-reconcile-bank-accounts-separately.md).

## <a name="reconcile-bank-accounts-with-copilot"></a>Avstem bankkontoer med Copilot

<!-- Similar to the **Match Automatically** capability on the **Bank Acc. Reconciliation** page, Bank account reconciliation assist can also automatically matches transactions in banks statements with bank entries. The difference is that **Match Automatically** uses a native rules-based algorithm, while Bank account reconciliation assist is based AI technology though Copilot. Bank account reconciliation assist is intended to supplement the **Match Automatically** capability. While **Match Automatically** is fairly successful at matching transactions, there are some instances where it can't&mdash;which is where Bank account reconciliation assist comes. By using the **Reconcile with Copilot** action on **Bank Acc. Reconciliation** page, you can find even more matches.-->

Copilot i bankkontoavstemming er ment som et supplement til autoavstem-operasjonen. Når du bruker Copilot, kjøres derfor autoavstemmingoperasjonen først for å utføre de første treffene. Deretter kjører Copilot for å prøve å samsvare med transaksjoner som autoavstemmingsoperasjonen ikke håndterte.

Du kan bruke to fremgangsmåter for å avstemme bankkontoer med Copilot:

- Bruk Copilot til å starte en ny avstemming på en bankkonto, direkte fra Bankkontoavstemming-listen **·** .
- Bruk Copilot på en ny eller eksisterende avstemming på et **Bankkontoavstemming**-kort.

# [Fra Bankkontoavstemming-listen](#tab/fromlist)

For denne tilnærmingen kan du opprette og avstemme en ny bankkontoavstemming fra grunnen av. Denne fremgangsmåten krever at du velger bankkontoen. Hvis bankkontoen ikke er knyttet til en Internett-konto, må du også importere bankkontoutdragsfilen.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bankkontoavstemming**, og velg deretter den relaterte koblingen.
1. Velg **Avstem med Copilot** for å åpne vinduet **Avstem med Copilot**.
1. Sett feltet **Utfør avstemming for denne bankkontoen** til bankkontoen du vil avstemme.

    ![Skjermbilde som viser vinduet Avstem med Copilot for avstemming fra grunnen av.](media/reconcile-bank-accounts-new-copilot.svg)

1. Hvis den valgte bankkontoen ikke er knyttet til en nettbankkonto, må du importere bankkontoutdragsfilen. Hvis du vil importere filen, velger du enten verdien i feltet **Bruk transaksjonsdata fra**, eller du velger bindersknappen ved siden av **Generer**-knappen. Bruk deretter **Velg filen som skal importeres** til å importere bankkontoutdragsfilen ved å dra den fra enheten eller bla gjennom enheten.
1. Hvis du vil avstemme med Copilot, velger du **Generer**.

    Copilot begynner å generere foreslåtte treff. Når det er fullført, vises resultatene av samsvarsprosessen i vinduet **Avstem med Copilot** .

1. Se gjennom de foreslåtte samsvarene som beskrives i delen nedenfor.

# [Fra et bankkontoavstemmingkort](#tab/fromcard)

Med denne fremgangsmåten bruker du Copilot enten på en ny bankkontoavstemming som du oppretter manuelt, eller ved å redigere en eksisterende avstemming.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") angi **Bankkontoavstemming**, og velg deretter den relaterte koblingen.
1. Følg et av disse trinnene:

    - Velg **Ny** for å starte en ny avstemming.
    - Velg og åpne en eksisterende avstemming i listen.

1. På kortet **Bankkontoavstemming** velger du **Avstem med Copilot**.

    ![Skjermbilder som viser knappen Avstem med Copilot på et bankkontoavstemmingskort.](media/bank-reconciliation-copilot-card.svg)

    Copilot begynner å generere foreslåtte treff. Når det er fullført, vises resultatene av samsvarsprosessen i vinduet **Avstem med Copilot** .

1. Se gjennom de foreslåtte samsvarene som beskrives i delen nedenfor.
---

### <a name="review-save-or-discard-proposed-matches"></a>Gå gjennom, lagre eller forkast foreslåtte samsvar

Når du har kjørt Copilot, viser vinduet **Avstem med Copilot** de detaljerte resultatene, inkludert eventuelle foreslåtte samsvar. På dette tidspunktet er ingen treff som Copilot har foreslått, lagret. Derfor har du en mulighet til å inspisere forslagene og lagre eller forkaste dem etter eget ønske.

![Skjermbilde som viser foreslått samsvar i vinduet Avstem med Copilot.](media/bank-reconciliation-copilot-window.png)

Vinduet **Avstem med Copilot** er delt inn i to deler. Den øvre delen gir noen generelle detaljer om resultatet. Den nedre delen, **Avstemmingsforslag**, viser avstemmingene som er foreslått av Copilot.

Tabellen nedenfor beskriver feltene i den øvre delen.

| Felt | Description |
|---|---|
| Automatisk avstemt | Antall linjer i kontoutskriften som ble avstemt av autoavstemmingsoperasjonen. Velg verdien for å vise avstemmingskortet. |
| Avstemt med Copilot | Antall linjer i kontoutskriften som Copilot foreslo avstemming for. Du kan se detaljer om avstemmingene i delen **Avstemmingsforslag**. |
| Utdrag – sluttsaldo | Sluttsaldoen som vises på bankkontoutdraget som du avstemmer mot. |
| Bokfør hvis fullstendig avstemt | Aktiver dette atlernativet hvis du vil bokføre bankkontoavstemmingen automatisk når alle linjene (100 prosent) samsvarer og du velger **Behold den**. |

I delen **Avstemmingsforslag** går du gjennom de foreslåtte avstemmingene linje for linje. Ta deretter de nødvendige tiltakene:

- Hvis du vil forkaste ett enkelt foreslått treff, merker du det i listen og velger deretter **Slett linje**.
- Hvis du vil forkaste alle foreslåtte treff og lukke vinduet **Avstem med Copilot**, velger du Forkast-knappen (papirkurven) ![Forkast-knapp.](media/copilot-delete-trash-can.png) ved siden **Behold den**-knappen nederst i vinduet.
- Hvis du vil bokføre den fullstendige avstemmingen automatisk når du lagrer den, slår du på alternativet **Bokfør hvis fullstendig avstemt**.
- Hvis du vil lagre treffene som vises i vinduet **Avstem med Copilot**, velger du **Behold den**.

## <a name="post-unmatched-bank-transaction-amounts-to-suggested-gl-accounts"></a>Bokfør banktransaksjonsbeløp uten samsvar til foreslåtte finanskontoer

Denne delen forklarer hvordan du bruker Copilot til å bokføre ikke-avstemte bankkontoutdragslinjebeløp (angitt i feltet **Differanse**) til en finanskonto. Denne oppgaven kan bare utføres fra en eksisterende avstemming.

1. Gå til listen **Bankkontoavstemminger**, og åpne den eksisterende avstemmingen som inneholder de ikke-avstemte linjene.

    Dette trinnet gir deg en klar oversikt over eventuelle ikke-avstemte bankkontoutdragslinjer som må overføres til finanskontoen.

1. I ruten **Bankkontoutdragslinjer** identifiserer du bankutdragslinjer som ikke samsvarer, og velger én eller flere linjer du vil avstemme.

    Copilot fokuserer på de valgte linjene for å bokføre nye betalinger til finanskontoen.

1. Velg **Bokfør differanse til finanskonto** for å starte prosessen.

    ![Skjermbilde som viser knappen Bokfør differanse til finanskonto på Bankkontoavstemming-kortet.](media/bank-reconciliation-transfer-gl-copilot-card.png)

    Copilot begynner å generere forslag til bokføring av nye betalinger.

1. Når Copilot er ferdig med å generere forslag, vises vinduet **Copilot-forslag til bokføring av differanse til finanskontoer**.

    Forslagene vises i delen **Avstemmingsforslag** i dette vinduet. Opplevelsen ligner opplevelsen for avstemming med Copilot.

    ![Skjermbilde som viser vinduet Copilot-forslag for bokføring av differanser på finanskontoer.](media/bank-reconciliation-gl-transfer-proposed-matches.png)

1. Gå gjennom forslagene linje for linje for å sikre nøyaktigheten av de foreslåtte betalingene som skal bokføres.

    - Hvis du driller ned på forslaget ved å velge det i listen, blir du tatt til en liste over kontoer. Derfra kan du velge en annen konto. Du kan bare utføre denne typen manuell korrigering når du bruker flyten **Bokfør differanse til finanskonto**, ikke avstemmingsflyten.
    - Hvis du velger **Lagre** ved siden av et forslag, kan du legge til tilordningen på siden **Tekst-til-konto-tilordning**. Neste gang denne teksten vises under avstemming, tilordnes den til den foreslåtte kontoen.

1. Forkast eller lagre forslag.

    - Hvis du vil forkaste et spesifikt forslag, velger du det i listen og velger deretter **Slett linje**. Hvis du vil forkaste alle forslag og lukke Copilot, velger du Forkast-knappen (papirkurven) ![Forkast-knapp.](media/copilot-delete-trash-can.png) ved siden **Behold den**-knappen nederst i vinduet.
    - Hvis forslagene oppfyller kravene dine og du vil lagre dem, velger du **Behold den**.

         Dette trinnet bekrefter overføringen av de valgte forslagene fra bankkontoposten til finanskontoen. Det bokfører nye betalinger til de foreslåtte finanskontiene og bruker tilsvarende linjer på de resulterende bankkontopostene.

## <a name="next-steps"></a>Neste trinn

[Validere bankkontoavstemmingen](bank-how-reconcile-bank-accounts-separately.md#validate-your-bank-reconciliation)

## <a name="see-also"></a>Se også

[Feilsøk Copilot- og KI-funksjoner](ai-copilot-troubleshooting.md)  
[Vanlige spørsmål om ansvarlig kunstig intelligens for bankavstemmingshjelp](faqs-bank-reconciliation.md)  
[Konfigurere banktjenester](bank-setup-banking.md)  
[Avstem bankkontoer](bank-how-reconcile-bank-accounts-separately.md)  
[Utligne betalinger automatisk og avstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md)
