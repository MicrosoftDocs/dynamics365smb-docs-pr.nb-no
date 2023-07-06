---
title: Kombiner automatisk og manuell trekking
description: 'Gjennomgang for en produksjonsplanlegger hos Contoso Coffee, som vil kombinere automatisk og manuelt lagertrekk.'
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
---

# <a name="walkthrough-combine-automatic-and-manual-flushing"></a><a name="walkthrough-combine-automatic-and-manual-flushing"></a><a name="walkthrough-combine-automatic-and-manual-flushing"></a>Gjennomgang: Kombiner automatisk og manuell trekking

I denne artikkelen tar vi deg gjennom trinnene for å bruke Contoso Coffee-demodataene i trekk.  

## <a name="scenario"></a><a name="scenario"></a><a name="scenario"></a>Scenario

Du er produksjonsplanleggeren hos Contoso Coffee. Du må opprette en ny produksjonsordre for ti enheter av varen SP-SCM1004, AutoDrip. Noen komponenter og operasjoner vil bli tømt, og andre avrundet basert på ulike betingelser.

## <a name="steps"></a><a name="steps"></a><a name="steps"></a>Trinn

> [Obs!] Husk å justere lageret ved å postere varekladd med åpningssaldoer.

1. Opprett en fast planlagt produksjonsordre for fem enheter av varen **SP-SCM1004, AutoDrip** på lokasjonen *NORD*. For veiledning kan du se [Gjennomgang: Opprett en fast planlagt produksjonsordre og endre den](create-firm-planned-production-order-change.md).  

2. Frigi produksjonsordren.

    1. Velg handlingen **Endre status**.  

    2. Sett det feltet **Ny status** til *Frigitt* på siden som vises, og klikk deretter på **Ja**-knappen.  

        En melding med en statuslinje vises og henviser til automatisk forbruk. Dette etterfølges av en bekreftelsesmelding om at ordren endres for å få statusen *Frigitt*.  

    3. Velg **OK**-knappen for å lukke bekreftelsesmeldingen.

3. Se gjennom vare- og kapasitetspostene for produksjonsordren.

    1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Frigitt produksjonsordre**, og velg deretter den relaterte koblingen.  

    2. Åpne produksjonsordren med fem enheter av AutoDrip-kaffemaskinen.  

    3. Velg handlingen **Vareposter**.  

        Varen **SP-BOM1305 Screw Hex M3 Zink** tømmes umiddelbart med hele forventet antall. Lukk **Vareposter**-siden.  

    4. Velg handlingen **Kapasitetsposter**.  Vær oppmerksom på at en oppføring i enhetsmonteringsoperasjoner også ble fullført da ordren ble frigitt. Lukk vinduet **Kapasitetsposter**.

    Du kan tømme komponentvarer manuelt ved å bruke forbruks- eller produksjonskladden. Manuell trekking gjør det mulig å justere antall før bokføring. Hvis for eksempel tilleggsantallet er nødvendig for å dekke råmaterialer med lav kvalitet.
4. Trekk komponenter manuelt.  
    1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Forbrukskladd** og velg den relaterte koblingen.  

    2. Velg handlingen **Beregn forbruk**.  

    3. På **Beregn forbruk**-forespørselsiden på hurtigfanen **Produksjonsordre** definerer du et filter for den bestemte ordren i **Ordrenr.**-feltet og deretter **OK**-knappen. Når forespørselssiden for den satsvise jobben lukkes, kan du se at **Forbrukskladd**-siden fylles ut med komponenter som krever manuelt forbruk.

    4. Velg handlingen **Bokfør**. Lukk forbrukskladden.

5. Registrer utdata manuelt for elektriske ledninger.  

    Du må manuelt fylle ut feltene **Oppstillingstid** og **Operasjonstid**. Du kan også angi faktisk produsert antall og svinn. Angi *3* som avgangsantallet, og bokfør avgangen.

    1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Ferdigmeldingskladd** og velg den relaterte koblingen.  

    2. På **Ferdigmeldingskladd**-siden oppretter du en ny kladdelinje.  

    3. I **Ordrenr.**-feltet angir du ordren.  

    4. Velg **Utfold rute**-handlingen.  

        Siden **Ferdigmeldingskladd** fyller bare ut med operasjonslinjen for elektriske ledninger.

    5. Sett **Kjøretid**-feltet til *10*.  

    6. Endre **Antall**-feltet fra *5* til *3*.

    7. Velg **Bokfør**.  
    8. Lukk ferdigmeldingskladden.

6. Se gjennom varepostene for produksjonsordren.

    1. På siden for produksjonsordren velger du handlingen **Vareposter**.  

    Varen **SP-BOM1302, kontrollpanelvisning** bokføres med et antall på *3*, basert på den faktiske avgangen, mens **SP-BOM1303, knapp** bokføres med hele det forventede antallet. Lukk **Vareposter**-siden.

7. Fullfør produksjonsordren.  

    1. Velg handlingen **Endre status**.
    2. Sett det feltet **Ny status** til *Fullført* på siden som vises, og klikk deretter på **Ja**-knappen.  

        Det vises en melding med en statuslinje som gjenspeiler det automatiske forbruket. Dette etterfølges av en bekreftelsesmelding om at ordren endres til en ordre med statusen *Fullført*. Den fullførte produksjonsordren har samme nummer som den med statusen *Frigitt*.
    3. Velg **OK**-knappen for å lukke bekreftelsesmeldingen.

8. Se gjennom vare- og kapasitetspostene for produksjonsordren på nytt.

    1. Velg handlingen **Kapasitetsposter**.  

        Pakkeoperasjonsposten ble fullført nå da ordren ble frigitt. Produsert antall (avgang) er *5*, uavhengig av avgangen i forrige trinn. Lukk siden **Kapasitetsposter**.

    2. Velg handlingen **Vareposter**.  

        Antallet i varepostene av typen *Avgang* er lik avgangsantallet i kapasitetsposten. Det forbrukte antallet for **SP-BOM1301, AutoDrip for hus** og **SP-BOM1304, termokaraffel i rustfritt stål** er 5 for begge, fordi forventet avgang og den faktiske avgangen er like. 

    3. Lukk **Vareposter**-siden.  

Det er for manuell og automatisk lagertrekk av komponenter.

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se også

[Lagertrekk komponenter i henhold til operasjonsavgang](../../production-how-to-flush-components-according-to-operation-output.md)  
[Innføring i demodata for Contoso Coffee](contoso-coffee-manufacturing-intro.md)  
