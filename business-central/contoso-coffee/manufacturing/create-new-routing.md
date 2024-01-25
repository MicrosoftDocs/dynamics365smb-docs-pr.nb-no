---
title: Opprett en ny rute
description: Gjennomgang for å lære hvordan du angir all informasjon for en ny rute manuelt i Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics-365-business-central
author: brentholtorf
ms.author: bholtorf
---
# <a name="walkthrough-create-a-new-routing"></a>Gjennomgang: Opprett en ny rute

I denne artikkelen leder vi deg gjennom trinnene for å bruke Contoso Coffee-demodataene til å definere en ny produksjonsrute manuelt i [!INCLUDE [prod_short](../../includes/prod_short.md)].  

## <a name="scenario"></a>Scenario

Oscar, prosessingeniøren hos Contoso Coffee, bestemmer hvordan de oppretter en ny rute med navnet *Ny bane*. Siden denne ruten er i motsetning til andre ruter hos Contoso Coffee, må Oscar manuelt angi all informasjonen for ruten.  

## <a name="steps"></a>Trinn

1. Opprett rutehodet.  

    1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Ruter**, og velg deretter den relaterte koblingen.  

    2. Velg handlingen **Ny** og fyll deretter ut feltene som beskrevet i tabellen nedenfor.  

        |Felt  |Verdi  |
        |---------|---------|
        |**Nr.** |1099|
        |**Beskrivelse** |Ny bane|
2. Opprett rutelinjene.

    1. I hurtigfanen **Linjer** legger du til en ny linje, og deretter fyller du ut feltene som beskrevet i tabellen nedenfor.  

        |Felt  |Verdi  |
        |---------|---------|
        |**Operasjonsnr.** |10|
        |**Type** |Arbeidssenter|
        |**Nr.** |100|
        |**Oppstillingstid** |20|
        |**Kjøretid** |15|

    2. Legg til en ny linje og fyll deretter ut feltene som beskrevet i tabellen nedenfor.  

        |Felt  |Verdi  |
        |---------|---------|
        |**Operasjonsnr.** |20|
        |**Type** |Arbeidssenter|
        |**Nr.** |200|
        |**Oppstillingstid** |30|
        |**Kjøretid** |5|
3. Godkjenn ruten.

    1. I feltet **Status** velger du *Sertifisert*.  

Den nye ruten er nå definert.  

## <a name="see-also"></a>Se også

[Innføring i demodata for Contoso Coffee](../contoso-coffee-intro.md)  
