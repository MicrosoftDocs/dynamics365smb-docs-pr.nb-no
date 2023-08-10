---
title: Opprette produksjonsordrer fra ordrer
description: Lær de ulike måtene for å opprette produksjonsordrer for produserte varer direkte fra ordrer.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 02/27/2023
ms.custom: bap-template
ms.search.form: '99000883, 99000884,'
---
# <a name="create-production-orders-from-sales-orders"></a>Opprette produksjonsordrer fra ordrer

Du kan opprette produksjonsordrer for produserte varer direkte fra ordrer.  

## <a name="to-create-a-production-order-from-a-sales-order"></a>Slik oppretter du en produksjonsordre fra en ordre

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Ordrer**, og velg deretter den relaterte koblingen.  
2. Velg ordren du vil opprette en produksjonsordre for.  
3. Velg handlingen **Planlegging**. siden **Ordreplanlegging** viser tilgjengeligheten til varen.  
4. Velg handlingen **Opprett prod.ordre**.  
5. Angi status og ordretype.  
6. Velg knappen **Ja** for å opprette en eller flere produksjonsordrer for linjene med **Prod.ordre** i feltet **Etterfyllingssystem**.

    > [!NOTE]  
    > Behovslinjer som har **Prod.ordre** i feltet **Etterfyllingssystem**, representerer underliggende produksjonsordrer. Når du har generert disse produksjonsordrene, må du huske å identifisere et ikke oppfylt komponentbehov for dem. Bruk siden **Ordreplanlegging** eller handlingen **Planlegg på nytt** til å identifisere behov som ikke er oppfylt.
    >
    > Når du oppretter produksjonsordrer for ordrer med siden Ordreplanlegging, brukes koblinger for ordre-til-ordre mellom behov og forsyning. Når det finnes ordre-til-ordre-koblinger, inkluderer ikke planleggingssystemet koblet forsyning eller lager i balanseringsprosessen. Hvis du vil finne ut mer om balansering, kan du gå til [Ordre-til-ordre-koblinger](design-details-central-concepts-of-the-planning-system.md#order-to-order-links).

## <a name="order-type"></a>Ordretype

Tabellen nedenfor beskriver to måter å opprette produksjonsordrer på.

|Alternativ|Beskrivelse|
|------|-----------|
|Vareordre|Det opprettes en produksjonsordre for hver vare som representeres av en linje på siden **Ordreplanlegging**.|
|Prosjektordre|Det opprettes en produksjonsordre med flere linjer for alle vare som representeres av linjer på siden **Ordreplanlegging**. Når du bruker prosjektordrer, inneholder feltet **Kildetype** for produksjonsordren **salgshodet**. Ordren har én linje for hver salgslinjevare som må produseres.|

## <a name="see-also"></a>Se også

[Definere produksjon](production-configure-production-processes.md)  
[Produksjon](production-manage-manufacturing.md)  
[Lager](inventory-manage-inventory.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Designdetaljer: Forsyningsplanlegging](design-details-supply-planning.md)  
[Anbefalte fremgangsmåter for oppsett: Forsyningsplanlegging](setup-best-practices-supply-planning.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
