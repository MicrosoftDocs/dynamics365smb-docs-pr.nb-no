---
title: Lag et tilbud til en kunde
description: Beskriver hvordan du oppretter et tilbud eller et tilbudsforespørselsdokument for å registrere tilbudet til en kunde og selge produkter under visse betingelser.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: rfq
ms.date: 05/27/2021
ms.author: edupont
ms.openlocfilehash: a538b7099521b10227bf5aeaefad0a9c60971068
ms.sourcegitcommit: f9a190933eadf4608f591e2f1b04c69f1e5c0dc7
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115543"
---
# <a name="make-sales-quotes"></a>Gi salgstilbud

Du kan opprette et tilbud for å registrere tilbudet til en kunde om å selge bestemte produkter på bestemte leverings- og betalingsbetingelser. Du kan sende tilbudet til kunden for å formidle tilbudet. Du kan sende dokumentet i e-post som et PDF-vedlegg. Du kan også få brødteksten i e-posten forhåndsutfylt med et sammendrag av tilbudet. Hvis du vil ha mer informasjon, kan du se [Sende dokumenter i e-post](ui-how-send-documents-email.md).

Mens du forhandler med kunden, kan du endre og sende tilbudet på nytt så ofte som nødvendig. Når kunden godkjenner tilbudet, kan du konvertere tilbudet til en salgsfaktura eller ordre som du behandler salget i. Hvis du vil ha mer informasjon, kan du se [Fakturere salg](sales-how-invoice-sales.md) eller [Selge produkter](sales-how-sell-products.md).

Du kan fylle kundefelt i tilbudet på to måter, avhengig av om kunden allerede er registrert. Se trinn 2 og 3 i fremgangsmåten nedenfor.

## <a name="to-create-a-sales-quote"></a>Slik oppretter du et tilbud

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Tilbud**, og velg deretter den relaterte koblingen.
2. I feltet **Kunde** angir du navnet på en eksisterende kunde.

   Andre felt på siden **Tilbud** inneholder nå standardinformasjon om den valgte kunden.  

    [!INCLUDE [sales-create-customer](includes/sales-create-customer.md)]

    Flere felt i tilbudet er nå fylt ut med informasjon du har angitt på det nye kundekortet.  
3. Fyll ut resten av feltene på siden **Tilbud** etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Du er nå klar til å fylle ut ordrelinjene for produktene du selger til kunden eller for noen transaksjon med kunden som du vil registrere i en finanskonto.  

    Hvis du har definert gjentakende salgslinjer for kunden, for eksempel en månedlig etterfyllingsordre, kan du sette inn disse linjene på ordren ved å velge handlingen **Hent gjentakende salgslinjer**.  

4. På **Linjer**-hurtigfanen i **Type**-feltet velger du typen produkt, tillegg eller transaksjon som du vil legge til for kunden med salgslinjen.
5. I **Nr.** velger du en post skal bokføres, i henhold til verdien i **Type**-feltet.

    La feltet **Nr.** stå tomt i følgende tilfeller:
    - Hvis linjen er for en kommentar. Skriv inn kommentaren i **Beskrivelse**-feltet.
    - Hvis linjen er for en katalogvare. Velg handlingen **Velg katalogvarer**. Hvis du vil ha mer informasjon, kan du se [Arbeide med katalogvarer](inventory-how-work-nonstock-items.md).

6. I **Antall**-feltet angir du hvor mange enheter av produktet, gebyret eller transaksjonen som linjen skal registrere for kunden.

    > [!NOTE]  
    >  Hvis varen er av typen **Service** eller **Type**-feltet inneholder **Ressurs**, er antallet en tidsenhet, for eksempel timer, som angitt i feltet **Enhetskode** på linjen. Hvis du vil ha mer informasjon, kan du se [Definere vareenheter](inventory-how-setup-units-of-measure.md)

    Verdien i **Linjebeløp**-feltet beregnes som *salgspris* x *antall*.  

    Prisen og linjebeløpene er med eller uten mva, avhengig av hva du valgte i feltet **Priser inkludert merverdiavgift** på kundekortet.  
7. Hvis du vil gi en rabatt, skriver du inn en prosentandel i feltet **Linjerabatt-%**. Verdien i feltet **Linjebeløp** oppdateres tilsvarende.  

    Hvis du har konfigurert varepriser i hurtigfanen **Salgspriser og salgslinjerabatter** i kunde- eller varekortet, oppdateres prisen og beløpet på salgslinjen automatisk hvis de avtalte priskriteriene er oppfylt. Hvis du vil ha mer informasjon, kan du se [Registrere avtaler om salgspris, rabatt og betaling](sales-how-record-sales-price-discount-payment-agreements.md).  
8. Gjenta trinn 4 til 7 for hvert produkt som du vil tilby til kunden.

    Totaler under linjene beregnes automatisk når du oppretter eller endrer linjer.  
9. I feltet **Fakturarabattbeløp** angir du et beløp som skal trekkes fra verdien som vises i feltet **Totalt inkl. mva.**.

    Hvis du har definert fakturarabatter for kunden, settes den angitte prosentverdien automatisk inn i feltet **Fakturarabatt %** hvis kriteriene er oppfylt, og det relaterte beløpet settes inn i feltet **Fakturarabattbeløp før mva.**. Hvis du vil ha mer informasjon, kan du se [Registrere avtaler om salgspris, rabatt og betaling](sales-how-record-sales-price-discount-payment-agreements.md).

    > [!TIP]
    > For at **Gyldig til-dato for tilbud** skal fylles ut automatisk med et bestemt antall dager etter oppretting av tilbud, kan du fylle ut feltet **Beregning av tilbudets gyldighet** på siden **Salg**.

10. Når tilbudslinjene er fullført, kan du velge handlingen **Send via e-post**.
11. På siden **Send e-post** fyller du ut resten av feltene, og gå gjennom det innebygde tilbudet. Hvis du vil ha mer informasjon, kan du se [Sende dokumenter i e-post](ui-how-send-documents-email.md).
12. Hvis kunden godtar tilbudet, velger du handlingen **Lag faktura** eller **Lag ordre**.

Tilbudet er fjernet fra databasen. Det opprettes en salgsfaktura eller ordre basert på informasjonen i tilbudet der du kan behandle salget. I feltet **Tilbudsnr.** på salgsfakturaen eller ordren kan du se nummeret på tilbudet den ble laget fra. Hvis du vil ha mer informasjon, kan du se [Fakturere salg](sales-how-invoice-sales.md) eller [Selge produkter](sales-how-sell-products.md).  

## <a name="external-document-number"></a>Eksternt dokumentnummer

[!INCLUDE [ext-doc-no-sales](includes/ext-doc-no-sales.md)]

## <a name="see-also"></a>Se også

[Salg](sales-manage-sales.md)  
[Sette opp salg](sales-setup-sales.md)  
[Send dokumenter i e-post](ui-how-send-documents-email.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]