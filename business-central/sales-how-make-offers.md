---
title: Lag tilbud
description: Les om hvordan du oppretter et tilbud eller et tilbudsforespørselsdokument for å registrere tilbudet til en kunde eller et kundeemne og selge produkter under visse betingelser.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: rfq
ms.search.form: '41, 9300'
ms.date: 02/05/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="make-sales-quotes"></a>Lag tilbud

Du kan opprette et tilbud for å registrere tilbudet til en kunde eller et kundeemne om å selge bestemte produkter på bestemte leverings- og betalingsbetingelser. Du kan sende tilbudet til kunden for å formidle tilbudet. Du kan sende dokumentet i e-post som et PDF-vedlegg. Du kan også få brødteksten i e-posten forhåndsutfylt med et sammendrag av tilbudet. Hvis du vil ha mer informasjon, kan du se [Sende dokumenter i e-post](ui-how-send-documents-email.md#to-send-documents-by-email).

Mens du forhandler med kunden eller kundeemnet, kan du endre og sende tilbudet på nytt så ofte som nødvendig. Når kunden godkjenner tilbudet, kan du konvertere tilbudet til en salgsfaktura eller ordre som du behandler salget i. Hvis du vil ha mer informasjon, kan du se [Fakturere salg](sales-how-invoice-sales.md) eller [Selge produkter](sales-how-sell-products.md).

I de fleste tilfeller sender du tilbud til kundeemner. Du har ofte en kontaktperson du forhandler med. Hvis de deretter godtar tilbudet, gjør du tilbudet om til en ordre og registrerer kundeemnet som kunde i [!INCLUDE [prod_short](includes/prod_short.md)]. I denne fremgangsmåten fokuserer vi på kontakter, men du kan også sende tilbud til eksisterende kunder.  

## <a name="to-create-a-sales-quote"></a>Slik oppretter du et tilbud

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Tilbud**, og velg deretter den relaterte koblingen.
2. Angi kontakten eller kunden som du vil sende tilbudet til.

    - Hvis tilbudet er for en eksisterende kontakt, angir du navnet i **Kontaktnr.** -feltet.  

        Hvis tilbudet er for en eksisterende kunde, angir du kunden i **Kunde**-feltet.
    - Hvis kontakten ikke er registrert, følger du denne fremgangsmåten:

        1. I feltene **Kontaktnr.** velger du Rediger-knappen :::image type="icon" source="media/assist-edit-icon.png" border="false":::.
        2. Velg den nye handlingen i dialogboksen om å velge kontakten, velg handlingen **Ny** og fyll deretter ut de aktuelle feltene. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] Hvis du vil ha mer informasjon, kan du se [Opprette kontakter](marketing-create-contact-companies.md).  
        3. Når du har fylt ut kontaktkortet, velger du den nylig opprettede kontakten i oversikten over kontakter, og deretter klikker du på OK for å gå tilbake til tilbudet.

        Flere felt i tilbudet er nå fylt ut med informasjon du har angitt på det nye kontaktkortet.

        > [!NOTE]
        > Hvis du vil beregne avgifter på riktig måte for et tilbud, må du velge den aktuelle kundemalen i feltet **Kundemalkode**. Malen blir brukt til å konvertere kontakten til en kunde når tilbudet er konvertert til en ordre eller en faktura.
    -  Hvis tilbudet er for ny kunde, må du legge til kunden. Hvis du vil ha mer informasjon, kan du se [Registrere nye kunder](sales-how-register-new-customers.md).  

3. Fyll ut resten av feltene på siden **Tilbud** etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Du er nå klar til å fylle ut ordrelinjene for produktene du selger eller for noen transaksjon med kunden eller kundeemnet som du vil registrere i en finanskonto.  

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
8. Gjenta trinn 4 til 7 for hvert produkt som du vil tilby til kontakten.

    Totaler under linjene beregnes automatisk når du oppretter eller endrer linjer.  
9. I feltet **Fakturarabattbeløp** angir du et beløp som skal trekkes fra verdien som vises i feltet **Totalt inkl. mva.**.

    Hvis du har definert fakturarabatter for kunden, settes den angitte prosentverdien automatisk inn i feltet **Fakturarabatt %** hvis kriteriene er oppfylt, og det relaterte beløpet settes inn i feltet **Fakturarabattbeløp før mva.**. Hvis du vil ha mer informasjon, kan du se [Registrere avtaler om salgspris, rabatt og betaling](sales-how-record-sales-price-discount-payment-agreements.md).

    > [!TIP]
    > For at **Gyldig til-dato for tilbud** skal fylles ut automatisk med et bestemt antall dager etter oppretting av tilbud, kan du fylle ut feltet **Beregning av tilbudets gyldighet** på siden **Salg**.

10. Når tilbudslinjene er fullført, kan du velge handlingen **Send via e-post**.
11. På siden **Send e-post** fyller du ut resten av feltene, og gå gjennom det innebygde tilbudet. Hvis du vil ha mer informasjon, kan du se [Sende dokumenter i e-post](ui-how-send-documents-email.md#to-send-documents-by-email).
12. Hvis kontakten godtar tilbudet, velger du **Lag ordre**-handlingen.  

    Hvis organisasjonen foretrekker det, kan du også velge handlingen **Lag faktura**.  
    > [!NOTE]
    > Hvis du har lagt til en kunde i trinn 2, blir du bedt om å bekrefte konverteringen av tilbudet til en ordre.  
    >
    > Hvis du la til en kontakt fra et kundeemne i trinn 2, blir du bedt om å gjøre følgende:
    >
    >  - Konverter kontakten eller kundeemnet til en kunde ved å velge en av kontaktkonverteringsmalene. Hvis du vil ha mer informasjon, kan du se [Slik oppretter du en kontakt, leverandør, ansatt eller bankkonto fra en kontakt](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).  
    > - Bekreft konverteringen av tilbudet til en ordre.

Konverteringen fjerner tilbudet fra databasen. Det opprettes en salgsfaktura eller ordre basert på informasjonen i tilbudet slik at du kan behandle salget. I feltet **Tilbudsnr.** på salgsfakturaen eller ordren kan du se nummeret på tilbudet den ble laget fra. Hvis du vil ha mer informasjon, kan du se [Fakturere salg](sales-how-invoice-sales.md) eller [Selge produkter](sales-how-sell-products.md).  

## <a name="external-document-number"></a>Eksternt dokumentnummer

[!INCLUDE [ext-doc-no-sales](includes/ext-doc-no-sales.md)]

## <a name="see-also"></a>Se også

[Salg](sales-manage-sales.md)  
[Sette opp salg](sales-setup-sales.md)  
[Send dokumenter via e-post](ui-how-send-documents-email.md#to-send-documents-by-email)  
[Arkiver dokumenter](across-how-to-archive-documents.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
