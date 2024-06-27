---
title: Lag direkte levering
description: 'Beskriver hvordan du oppretter en ordre som er koblet til en bestilling, for å sikre levering direkte fra leverandøren til kunden.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: direct shipment
ms.date: 05/28/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Lag direkte levering

En direkte levering er levering av varer fra en av leverandørene dine, direkte til en av kundene dine.

Når en ordre er merket for direkte levering, og du oppretter en bestilling for kunden i **Forsendelsesadresse**-feltet, **Kundeadresse**, kan du koble de to dokumentene og instruere leverandøren til å levere direkte til kunden.
<br><br>  
  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4mOyM?rel=0]

## Slik oppretter du en ordre med direkte levering:

Hvis du vil klargjøre en direkte levering, kan du opprette en ordre og vise på salgslinjen at salget krever direkte levering.

1. Opprett en ordre for en vare. Hvis du vil ha mer informasjon, kan du se [Selge produkter](sales-how-sell-products.md).
2. På ordrelinjen for direkte levering, merker du av for **Direkte levering**. Du kan eventuelt velg en kjøpskode som **Direkte levering**-feltet er valgt for, i **Kjøpskode**-feltet.

> [!TIP]
> Avmerkingsboksen for direkte levering og kjøpskode er som standard ikke tilgjengelig på linjene. Hvis de ikke er det, kan du legge dem til ved å tilpasse inndelingen på siden som inneholder linjene. Hvis du vil ha mer informasjon, kan du se [Tilpasse arbeidsområdet](ui-personalization-user.md).

## Slik oppretter du bestillingen med direkte levering:

For å klargjøre en direkte levering angir du på bestilling at den må leveres til kunden, ikke til deg selv.

1. Opprett en bestilling. Ikke fyll ut noen felt på linjene. Hvis du vil ha mer informasjon, kan du se [Registrere kjøp](purchasing-how-record-purchases.md).
2. I **Forsendelsesadresse**-feltet velger du **Kundeadresse**.
3. I **Kunde**-feltet velger du kunden som du selger til.
4. Velg **Direkte levering**-handlingen, og velg deretter **Hent ordre**-handlingen.
5. På siden **Salgsliste** merker du ordren som du har forberedt i [Slik oppretter du en ordre med direkte levering](#to-create-a-sales-order-for-drop-shipment).
6. Velg **OK**.

Linjeinformasjonen fra ordren settes inn på bestillingslinjene.

Nå kan du be leverandøren om å sende varene direkte til kunden. Du kan for eksempel sende dem bestillingen via e-post.

Hvis leverandøren oppgir ekstra informasjon, for eksempel et sporingsnummer, kan du legge til informasjonen som en kommentar på en bestillingslinje. Hvis du vil legge til en kommentar på en linje, går du til **Type**-feltet, velger **Kommentar** og skriver inn informasjonen i **Beskrivelse**-feltet.  

## Slik oppretter du flere bestillinger med direkte leveringer

Du kan også bruke bestillingsforslaget til å opprette bestillinger. Fordelen med å bruke bestillingsforslaget er at det kan opprette bestillinger for alle utestående direkte leveringer. Det betyr at du ikke trenger å opprette hver bestilling for seg.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Bestillingsforslag**, og velg deretter den relaterte koblingen.
2. Velg **Direkte levering**-handlingen, og velg deretter **Hent ordre**-handlingen.
3. Hvis det er nødvendig, angir du filterkriterier for bestillingene du vil ha, og deretter velger du **OK**-knappen.
4. Se gjennom bestillingslinjene, og velg leverandøren som leverer varene, i feltet **Leverandørnummer**.
5. Velg handlingen **Utfør handlingsmelding** for å konvertere linjene til en bestilling.

## Slik viser du den tilknyttede bestillingen fra ordren:

Velg ordrelinjen med direkte levering, velg **Ordre**-handlingen, velg **Direkte levering**-handlingen, og velg deretter **Bestilling**-handlingen.

## Bokføre en direkte levering

Når leverandøren har levert varene, kan du bokføre ordren som levert. Du kan også bokføre bestillingen, men bare med **Motta**-alternativet til ordren er fakturert.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Ordrer**, og velg deretter den relaterte koblingen.
2. Åpne ordren du opprettet i [Slik oppretter du en ordre med direkte levering:](#to-create-a-sales-order-for-drop-shipment).
3. I **Levere (antall)**-feltet angir du hvor mye av ordreantallet som skal leveres, hele eller deler av ordreantallet.
4. Velg handlingen **Bokfør** eller **Bokfør og send**.
5. Velg **Levere** hvis du vil fakturere senere, eller **Levere og fakturere** hvis du vil fakturere med en gang.

> [!TIP]
> Ikke glem at du må bokføre bestillingsfakturaen.

## Se også

[Opprett spesialbestillinger](sales-how-to-create-special-orders.md)  
[Kjøpvarer for et salg](purchasing-how-purchase-products-sale.md)  
[Selg produkter](sales-how-sell-products.md)  
[Registrere kjøp](purchasing-how-record-purchases.md)  
[Salg](sales-manage-sales.md)  
[Lager](inventory-manage-inventory.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
