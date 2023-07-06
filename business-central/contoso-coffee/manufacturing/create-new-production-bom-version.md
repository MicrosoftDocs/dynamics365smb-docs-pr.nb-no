---
title: Opprett en ny produksjonsstykkliste og stykklisteversjon
description: Gjennomgang for å lære hvordan du legger til en ny kaffemaskin i Contoso Coffees produktserie i Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
---
# <a name="walkthrough-create-a-new-production-bom-and-bom-version"></a><a name="walkthrough-create-a-new-production-bom-and-bom-version"></a><a name="walkthrough-create-a-new-production-bom-and-bom-version"></a>Gjennomgang: Opprett en ny produksjonsstykkliste og stykklisteversjon

I denne artikkelen leder vi deg gjennom trinnene for å bruke Contoso Coffee-demodataene for å arbeide med stykkliste i produksjonsprosesser.  

## <a name="scenario"></a><a name="scenario"></a><a name="scenario"></a>Scenario

Contoso Coffee har besluttet å legge en ny kaffemaskin mot produktlinjen: **SP-SCM1008 Airpot Lite**. Denne kaffemaskinen er identisk med den eksisterende varen **SP-SCM1009 Airpot**, bortsett fra at den ikke har varmeplaten, **SP-BOM1104**. I et separat trinn fjernes av/på-lyset, **SP-BOM1106** for en versjon av Airpot Lite-stykklisten.

Oscar, prosessingeniøren hos Contoso Coffee, må definere en ny produksjonsstykkliste for å definere de innledende komponentkravene for den Airpot Lite. Oscar må deretter definere en ny stykklisteversjon, med start datoen 1. juli, for å samkjøre med ytterligere planer om å frigi en annen utgave.

## <a name="steps"></a><a name="steps"></a><a name="steps"></a>Trinn

1. Opprett en ny produksjonsstykkliste for Airpot Lite.

    1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Produksjonsstykkliste**, og velg deretter den relaterte koblingen.  

    2. Velg handlingen **Ny** og fyll deretter ut feltene som beskrevet i tabellen nedenfor.  

        |Felt  |Verdi  |
        |---------|---------|
        |**Nr.** |SP-SCM1008|
        |**Beskrivelse** |Airpot Lite|
        |**Enhetskode**|STK  |

2. Kopier stykklistekomponentene fra produksjonsstykklisten **SP-SCM1009**.

    1. Velg handlingen **Kopier stykkliste**.

    2. På siden **Produksjonsstykklister** velger du linjen for **SP-SCM1009, Airpot** og velg deretter **OK**-knappen.

3. Endre komponentene for den nye produksjonsstykklisten slik det er beskrevet i scenarioet.

    1. På hurtigfanen **Linjer** velger du linjen for varen **SP-BOM1104** og deretter velger du handlingen **Slett linje**.  

4. Godkjenn den nye stykklisten.  

    1. I feltet **Status** velger du *Sertifisert*.  

5. Opprett en produksjonsstykklisteversjon for Airpot Lite.

    1. Velg handlingen **Versjoner**.

    2. På siden **Prod.stykkl. – versjonsoversikt** velger du handlingen **Ny** og fyller deretter ut feltene som beskrevet i tabellen nedenfor.  

        |Felt  |Verdi  |
        |---------|---------|
        |**Versjonskode** |02|
        |**Beskrivelse** |Airpot Lite, v2|
        |**Enhetskode**|STK  |  
        |**Startdato**|1. juli  |  

6. Kopier komponentlinjene fra produksjonsstykklisten til den nye stykklisteversjonen.

    1. Velg **Kopier stykkliste**-handling, og velg deretter **Ja** for å kopiere komponentene fra den opprinnelige produksjonsstykklisten.

7. Fjern varen **SP-BOM1106, Av/på-lys** fra versjonskomponentene.

8. Godkjenn den nye stykklisteversjonen.

    1. I feltet **Status** velger du *Sertifisert*.  

    2. Lukk stykklisteversjonen

Den nye kaffemaskinen er nå definert som en produksjonsstykkliste med én versjon.  

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se også

[Innføring i demodata for Contoso Coffee](../contoso-coffee-intro.md)  
