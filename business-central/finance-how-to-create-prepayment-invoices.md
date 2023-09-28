---
title: Opprette forskuddsfakturaer
description: 'Håndter situasjoner der du eller leverandøren krever forskuddsbetaling. Bruk standardprosentene for hver salgslinje eller bestillingslinje, eller juster beløpet etter behov.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bhielse
ms.topic: how-to
ms.date: 02/02/2023
ms.custom: bap-template
ms.search.form: '42, 50, 9305, 9307'
---
# <a name="create-prepayment-invoices"></a>Opprette forskuddsfakturaer

Hvis du krever at kundene skal betale før du leverer ordren, kan du bruke forskuddsfunksjonene. Det samme gjelder hvis leverandøren krever at du betaler før de leverer en ordre til deg.  

Du kan starte betalingsprosessen når du oppretter en ordre eller bestilling. Standard forskuddsprosent for en vare på bestillingen eller for kunden eller leverandøren blir inkludert i forskuddsfakturaen. Du kan også angi en forskuddsprosent for hele dokumentet.

Når du har opprettet en ordre eller bestilling, kan du opprette en forskuddsfaktura for den. Bruk standardprosentene for hver salgslinje eller bestillingslinje, eller juster beløpet. Du kan for eksempel angi et totalbeløp for hele ordren.  

Fremgangsmåten nedenfor beskriver hvordan du fakturerer et forskudd for en ordre. Trinnene er de samme for bestillinger.  

## <a name="to-create-a-prepayment-invoice"></a>Slik oppretter du en forskuddsfaktura:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Ordrer**, og velg deretter den relaterte koblingen.  
2. Opprett en ny ordre for den aktuelle kunden. Hvis du vil ha mer informasjon, kan du se [Selge produkter](sales-how-sell-products.md).  

    I hurtigfanen **Forskudd** angir feltet **Forskuddsprosent** prosenten som skal brukes til å beregne forskuddsbeløpet. Hvis det er angitt en standard forskuddsprosent på kundekortet, fylles feltet ut automatisk. Du kan endre prosenten. <!--This percentage is applied to lines where the item on that line does not already specify a prepayment percentage. The prepayment percentage is only copied from the header to lines that do not copy the default prepayment percentage from the item.-->  

    Velg feltet **Komprimer forskudd** hvis du vil opprette linjer på forskuddsfakturaen som kombinerer linjer fra ordren, hvis:  

    - De har samme finanskonto for forskudd, som definert i det generelle bokføringsoppsettet.  
    - De har samme dimensjoner.  

    Hvis du vil definere en forskuddsfaktura med én linje for hver ordrelinje som har en forskuddsprosent, velger du ikke feltet **Komprimer forskudd**.  

    Forskuddsdatoen for forskuddet beregnes automatisk basert på verdien i feltet **Kode for betalingsbetingelser for forskudd**.

    > [!NOTE]
    > Når noen linjer på en faktura krever 100 % forskuddsbetaling og andre linjer ikke gjør det, og det er mva. på forskuddskontoen, kan det avrundede beløpet forårsake en feil når du oppretter en forskuddsfaktura. Feilen oppstår fordi forskuddsfakturabeløpet er høyere enn beløpene på dokumentlinjene. Du kan løse problemet ved å endre beløpene på en av eller alle linjene som krever 100 % forskuddsbetaling. Endringen beregner mva-beløpet på nytt og bruker den akkumulerte avrundingsdifferansen på den siste endrede linjen.
    >
    > Det er to måter til å løse problemet på:
    >
    > * Opprett en separat mva-produktbokføringsgruppe og et mva-bokføringsoppsett med en separat mva-type, og bruk denne for varene eller linjene som krever 100 % forskuddsbetaling. Avrunding utføres for hver mva-type, så separat avrunding blir utført for varer som er tildelt til mva-produktbokføringsgruppen.
    > * Bruk en separat faktura for varene eller linjene som skal benyttes og som ikke krever 100 % forskuddsbetaling.

3. Fyll ut salgslinjene.  

    Hvis du har angitt en standard forskuddsprosent for kunden eller i hurtigfanen **Forskudd** for dette dokumentet, blir denne verdien kopiert til hver linje. Du kan endre verdien i **Forskuddsprosent**-feltet på linjen.  

    > [!TIP]
    > Hvis du ikke ser feltet **Forskuddsprosent**, kan du legge det til ved hjelp av personalisering.  Hvis du vil ha mer informasjon, kan du se [Tilpasse arbeidsområdet](ui-personalization-user.md).

4. Du kan vise det totale forskuddsbeløpet ved å velge **Statistikk**-handlingen.

    Hvis du vil justere det totale forskuddsbeløpet for ordren, kan du endre verdien i **Forskuddsbeløp**-feltet på **Ordrestatistikk**-siden.  

    Hvis feltet **Priser inkl. mva.** er valgt, kan du redigere feltet **Forskuddsbeløp inkl. mva**.  

    Hvis du endrer verdien i **Forskuddsbeløp**-feltet, blir beløpet fordelt proporsjonalt mellom alle linjene, unntatt linjer som har **0** i **Forskuddsprosent**-feltet.  

5. Hvis du vil skrive ut en testrapport før du bokfører forskuddsfakturaen, velger du **Forskuddsbetaling** og velger deretter **Testrapport for forskudd**.  
6. Hvis du vil bokføre forskuddsfakturaen, velger du **Forskuddsbetaling** og velger deretter **Bokfør forskuddsfaktura**.  

    Hvis du vil bokføre og skrive ut forskuddsfakturaen, velger du handlingen **Bokfør og skriv ut forskuddsfaktura**.  

Du kan utstede andre forskuddsfakturaer for ordren. Hvis du vil utstede en ny faktura, må du øke forskuddsbeløpet på en eller flere linjer, justere dokumentdatoen om nødvendig, og bokføre forskuddsfakturaen. Det opprettes en ny faktura for differansen mellom forskuddsbeløpene som er fakturert hittil, og det nye forskuddsbeløpet.  

> [!NOTE]  
> Hvis du befinner deg i Nord-Amerika, kan du ikke endre forskuddsprosenten når den forskuddsbetalte fakturaen er bokført. Dette er ikke tillatt i Nord-Amerika-versjonen av [!INCLUDE[prod_short](includes/prod_short.md)] fordi beregningen av merverdiavgift ellers blir feil.  

 Når du er klar til å bokføre resten av fakturaen, bokfører du den som en hvilken som helst annen faktura, og forskuddsbeløpet blir automatisk trukket fra forfallsbeløpet.  

## <a name="update-the-status-of-prepaid-orders-and-invoices-automatically"></a>Oppdater statusen for forhåndsbetalte bestillinger og fakturaer automatisk

Du kan øke bestillings- og fakturabehandlingen ved å definere jobbkøposter som automatisk oppdaterer statusen for disse dokumentene. Når en forskuddsfaktura betales, kan jobbkøposter automatisk endre dokumentstatusen fra **Venter på forskudd** til **Frigitt**. Når du definerer jobbkøpostene, er codeunits du trenger å bruke, **383 Oppdater ventende forskuddssalg** og **383 Oppdater ventende forskuddskjøp**. Vi anbefaler at du planlegger at postene skal kjøre ofte, for eksempel hvert minutt. Hvis du vil ha mer informasjon, kan du se [Bruk jobbkøer til å planlegge oppgaver](admin-job-queues-schedule-tasks.md).

## <a name="see-also"></a>Se også

[Fakturer forskuddsbetalinger](finance-invoice-prepayments.md)  
[Gjennomgang: Konfigurer og fakturer salgsforskudd](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Finans](finance.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Tilpasse arbeidsområdet](ui-personalization-user.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
