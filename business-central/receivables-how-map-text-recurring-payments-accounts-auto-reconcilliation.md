---
title: Definer tekst-til-konto-tilordning for gjentakende betalinger
description: 'Knytt tekst på betalinger til bestemte konti, slik at betalinger bokføres på kontiene når du bokfører betalingsavstemmingskladden.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'account linking, direct payment posting, automatic payment processing, reconcile payment, recurring expense, recurring cash receipt'
ms.search.form: '1290, 1294, 1287'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="map-text-on-recurring-payments-to-accounts-for-automatic-reconciliation"></a>Tilordne tekst på gjentakende betalinger til kontoer for automatisk avstemming

På siden **Tekst-til-konto-tilordning**, som du åpner fra siden **Betalingsavstemmingskladd**, kan du definere tilordninger mellom tekst på betalinger og bestemte debet-, kredit- og motkonti, slik at slike betalinger bokføres på de angitte kontiene når du bokfører kladden for betalingsavstemming.

Det finnes liknende funksjon hvis du vil avstemme overskytende beløp på linjene for betalingsavstemmingskladd på ad hoc-basis. Hvis du vil ha mer informasjon, kan du se [Avstemme betalinger som ikke kan utlignes automatisk](receivables-how-reconcile-payments-cannot-apply-auto.md)

Betalinger som bokføres basert på tekst-til-kontotilordning, utlignes ikke mot åpne poster, men bokføres bare på bestemte konti, i tillegg til at de oppretter bankkontoposter. Tekst-til-kontotilordning er dermed egnet til gjentakende innbetalinger eller utgifter, for eksempel hyppige kjøp av drivstoff til bil eller bankgebyrer og renter, som regelmessig oppstår på bankkontoutdraget og ikke trenger et tilknyttet forretningsdokument. Hvis du vil ha mer informasjon, kan du se avsnittet "Eksempel – tekst-til-kontotilordning for drivstoffutgifter" i dette emnet.

> [!NOTE]  
>   Betalinger på avstemmingskladdelinjene settes bare til bokføring i henhold til tekst-til-kontotilordning hvis funksjonen for automatisk utligning bare kan gi samsvarskonfidensen **Lav** eller **Middels**. Hvis funksjonen for automatisk utligning gir konfidensintervallet Høy, utlignes betalingen automatisk mot én eller flere åpne poster, og betalingen bokføres ikke på kontiene som er angitt på siden **Tekst-til-konto-tilordning**. Samsvarskonfidensen **Høy** overstyrer med andre ord tekst-til-kontotilordning.

På en linje i betalingsavstemmingskladden der betalingen er satt til bokføring i henhold til tekst-til-kontotilordning, inneholder **Konfidensintervall**-feltet **Høy – tekst-til-kontotilordning**, og **Kontotype**- og **Kontonummer** de tilordnede kontoene.

## <a name="to-map-text-on-recurring-payments-to-accounts-for-automatic-reconciliation"></a>Tilordne tekst på gjentakende betalinger til kontoer for automatisk avstemming

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Betalingsavstemmingskladder** og velg den relaterte koblingen.
2. Åpne en kladd for betalingsavstemming. Hvis du vil ha mer informasjon, kan du se [Avstemme betalinger ved hjelp av automatisk utligning](receivables-how-reconcile-payments-auto-application.md).
3. Velg handlingen **Tilordne tekst til konto**. Siden **Tekst-til-konto-tilordning** åpnes.
4. Skriv inn tekst som forekommer på betalinger du vil bokføre på bestemte konti uten å utligne mot en åpen post, i **Tilordningstekst**-feltet. Du kan angi opptil 50 tegn.

    > [!NOTE]  
    >   Hvis ingen andre betalinger finnes med den aktuelle tilordningsteksten, skjer tekst-til-konto-tilordningen selv når bare en del av teksten på betalingen finnes som tilordningstekst.
5. I feltet **Leverandørnummer** angir du leverandøren som betalingene bokføres til.
6. Angi om betalingen skal bokføres på en finanskonto eller en kunde- eller leverandørkonto, i feltet **Saldokildetype**.
7. I **Saldokildenummer**-feltet angir du kontoen som betalingen skal bokføres på, i feltet Saldokildetype, avhengig av hva du valgte i feltet **Saldokildetype**.

    > [!NOTE]
    > Ikke bruk **Debetkontonummer**- og **Kreditkontonummer**-feltet i forbindelse med betalingsavstemmingen. De brukes bare for inngående dokumenter. Hvis du vil ha mer informasjon, kan du se [Bruke OCR til å konvertere PDF- og bildefiler til elektroniske dokumenter](across-how-use-ocr-pdf-images-files.md).

8. Gjenta trinn 3 til og med 7 for all tekst på betalinger du vil tilordne til kontoer for direkte bokføring uten utligning.

Neste gang du importerer en bankkontoutdragsfil eller velger handlingen **Utlign automatisk** på siden **Betalingsavstemmingskladd**, inneholder kladdelinjene for betalinger som inneholder den angitte tilordningsteksten, de tilordnede kontiene i feltene **Kontotype** og **Kontonummer**. Feltet **Konfidensintervall** inneholder **Høy – tekst-til-konto-tilordning**. Dette er under forutsetning av at automatiske utligningsfunksjonen bare kan gi samsvarskonfidensen **Lav** eller **Middels**.

## <a name="example-text-to-account-mapping-for-bank-fees"></a>Eksempel: Tekst-til-konto-tilordning for bankgebyrer

Hvis du alltid vil bokføre utgifter som er knyttet til gebyrer fra en bestemt bank, MyBank, til finanskontoen for bankgebyrer og gebyrer (konto 60400), fyller du ut en linje på siden **Tekst-til-konto-tilordning** på følgende måte:

| Tilordningstekst | Debetkontonummer | Kreditkontonummer | Saldokildetype | Saldokildenummer |
| --- | --- | --- | --- | --- |
| MyBank |TOM |60400|Finanskonto |TOM |

## <a name="see-related-microsoft-training"></a>Se relatert [Microsoft-opplæring](/training/modules/use-journals-dynamics-365-business-central/)

## <a name="see-also"></a>Se også

[Håndtere fordringer](receivables-manage-receivables.md)  
[Salg](sales-manage-sales.md)  
[Konfigurer Envestnet Yodlee Bank Feeds-tjenesten](bank-how-setup-bank-statement-service.md)  
[Tilpass [!INCLUDE[prod_short](includes/prod_short.md)] ved hjelp av utvidelser](ui-extensions.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
