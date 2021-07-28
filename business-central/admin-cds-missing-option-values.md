---
title: Håndtere manglende alternativverdier
description: Finn ut hvordan du kan hindre at full synkronisering mislykkes fordi alternativene er forskjellige i tilordnede felt. Denne prosessen krever hjelp av en utvikler.
author: bholtorf
ms.author: bholtorf
ms.custom: na
ms.reviewer: na
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 06/14/2021
ms.openlocfilehash: 894414ca22ec960c228f9519cb54d9044790a87b
ms.sourcegitcommit: e562b45fda20ff88230e086caa6587913eddae26
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/30/2021
ms.locfileid: "6324078"
---
# <a name="handling-missing-option-values"></a>Håndtere manglende alternativverdier
[!INCLUDE[prod_short](includes/cc_data_platform_banner.md)]

Dette emnet er ment for en teknisk målgruppe. Prosessene som beskrives, krever hjelp av en utvikler.

[!INCLUDE[prod_short](includes/cds_long_md.md)] inneholder tre alternativsettfelt som inneholder verdier du kan tilordne til [!INCLUDE[prod_short](includes/prod_short.md)]-felt av typen Alternativ for automatisk synkronisering. Under synkroniseringen ignoreres ikke-tilordnede alternativer, og de manglende alternativene legges til i den relaterte [!INCLUDE[prod_short](includes/prod_short.md)]-tabellen og legges til i systemtabellen **Tilordning av Dataverse-alternativ** for å behandles manuelt senere. Det kan for eksempel være å legge til de manglende alternativene i hvert produkt og deretter oppdatere tilordningen.

Siden **Tilordning for integreringstabell** inneholder tre felt som inneholder én eller flere tilordnede alternativverdier. Etter en full synkronisering inneholder siden **Tilordning av Dataverse-alternativ** de ikke-tilordnede alternativene i de tre feltene.

|         Post             | Alternativverdi | Tittel for alternativverdi |
|----------------------------|--------------|----------------------|
| Betalingsbetingelser: NET30       | 1            | Net 30               |
| Betalingsbetingelser: 2%10NET30   | 2            | 2% 10; Net 30        |
| Betalingsbetingelser: NET45       | 3            | Net 45               |
| Betalingsbetingelser: NET60       | 4            | Net 60               |
| Leveringsmåte: FOB       | 1            | FOB                  |
| Leveringsmåte: NOCHARGE  | 2            | No Charge            |
| Transportør: AIRBORNE   | 1            | Airborne             |
| Transportør: DHL        | 2            | DHL                  |
| Transportør: FEDEX      | 3            | FedEx                |
| Transportør: UPS        | 4            | UPS                  |
| Transportør: POSTALMAIL | 5            | Postal Mail          |
| Transportør: FULLLOAD   | 6            | Full Load            |
| Transportør: WILLCALL   | 7            | Will Call            |

Innholdet på siden **Tilordning av Dataverse-alternativ** er basert på opplistingsverdier i tabellen **CRM-konto**. I [!INCLUDE[prod_short](includes/cds_long_md.md)] blir følgende felt i kontotabellen tilordnet til felt i kunde- og leverandørpostene:

- **Adresse 1: Fraktvilkår** for datatypen Opplisting, der verdier defineres som følger:

```
enum 5335 "CDS Shipment Method Code"
{
    Extensible = true;
    value(0; " ") { Caption = ' '; }
    value(1; "FOB") { Caption = 'FOB'; }
    value(2; "NoCharge") { Caption = 'No Charge'; }
}
```

- **Adresse 1: Leveringmåte** for datatypen Opplisting, der verdier defineres som følger:

```
enum 5336 "CDS Shipping Agent Code"
{
    Extensible = true;
    value(0; " ") { Caption = ' '; }
    value(1; "Airborne") { Caption = 'Airborne'; }
    value(2; "DHL") { Caption = 'DHL'; }
    value(3; "FedEx") { Caption = 'FedEx'; }
    value(4; "UPS") { Caption = 'UPS'; }
    value(5; "PostalMail") { Caption = 'Postal Mail'; }
    value(6; "FullLoad") { Caption = 'Full Load'; }
    value(7; "WillCall") { Caption = 'Will Call'; }
}
```

- **Betalingsbetingelser** for datatypen Opplisting, der verdier defineres som følger:

```
enum 5334 "CDS Payment Terms Code"
{
    Extensible = true;
    value(0; " ") { Caption = ' '; }
    value(1; "Net30") { Caption = 'Net 30'; }
    value(2; "2%10Net30") { Caption = '2% 10; Net 30'; }
    value(3; "Net45") { Caption = 'Net 45'; }
    value(4; "Net60") { Caption = 'Net 60'; }
}
```

Alle opplistingene i [!INCLUDE[prod_short](includes/prod_short.md)] ovenfor tilordnes til alternativsett i [!INCLUDE[prod_short](includes/cds_long_md.md)].

### <a name="extending-option-sets-in-prod_short"></a>Utvide alternativsett i [!INCLUDE[prod_short](includes/prod_short.md)]
1. Opprett en ny AL-utvidelse.

2. Legg til en opplistingsutvidelse for alternativene du vil utvide. Sørg for at du bruker samme verdi. 

```
enumextension 50100 "CDS Payment Terms Code Extension" extends "CDS Payment Terms Code"
{
    value(779800001; "Cash Payment") { Caption = 'Cash Payment'; }
    value(779800002; "Transfer") { Caption = 'Transfer'; }
}
```

> [!IMPORTANT]  
> Du må bruke de samme ID-verdiene for alternativ fra [!INCLUDE[prod_short](includes/cds_long_md.md)] når du utvider opplistingen i [!INCLUDE[prod_short](includes/prod_short.md)]. Ellers mislykkes synkroniseringen.

> [!IMPORTANT]  
> Ikke bruk tegnet «,» i opplistingsverdiene og bildetekstene. Dette støttes for øyeblikket ikke av [!INCLUDE[prod_short](includes/prod_short.md)]-kjøretiden.

> [!NOTE]
> De første ti tegnene i navnene på og tekstene for de nye alternativverdiene må være unike. To alternativer, for eksempel Overføring av 20 virkedager og Overføring av 20 kalenderdager, vil forårsake feil fordi begge har de samme 10 første tegnene ("Overføring"). Gi dem for eksempel navnet "Ovf 20 vrk" og "Ovf 20 kad".

### <a name="update-prod_short-option-mapping"></a>Oppdater Tilordning av [!INCLUDE[prod_short](includes/cds_long_md.md)]-alternativ
Nå kan du gjenopprette tilordningen mellom [!INCLUDE[prod_short](includes/cds_long_md.md)]-alternativer og [!INCLUDE[prod_short](includes/prod_short.md)]-poster.

På siden **Tilordning for integreringstabell** velger du linjen for tilordningen **Betalingsbetingelser**, og deretter velger du handlingen **Synkroniser endrede poster**. Siden **Tilordning av Dataverse-alternativ** oppdateres med tilleggspostene nedenfor.

|         Post                 | Alternativverdi   | Tittel for alternativverdi |
|--------------------------------|----------------|----------------------|
| Betalingsbetingelser: NET30           | 1              | Net 30               |
| Betalingsbetingelser: 2%10NET30       | 2              | 2% 10; Net 30        |
| Betalingsbetingelser: NET45           | 3              | Net 45               |
| Betalingsbetingelser: NET60           | 4              | Net 60               | 
| **Betalingsbetingelser: CASH PAYME**  | **779800001**  | **Cash Payment**     |
| **Betalingsbetingelser: TRANSFER**    | **779800002**  | **Overføring**         |

Tabellen **Betalingsbetingelser** i [!INCLUDE[prod_short](includes/prod_short.md)] viser da nye poster for [!INCLUDE[prod_short](includes/cds_long_md.md)]-alternativene. I følgende tabell er det nye alternativer med fet skrift. Rader i kursiv representerer alle alternativer som nå kan synkroniseres. Gjenstående rader representerer alternativer som ikke er i bruk og vil bli ignorert under synkronisering. Du kan fjerne eller utvide Dataverse-alternativer med samme navn.)

|  - kode       | Beregning av forfallsdato | Beregning av kontantrabattdato | Rabattprosent | Beregn kontantrab. for kred.nota | Beskrivelse       |
|------------|----------------------|---------------------------|------------|-------------------------------|-------------------|
| 10 DAGER    | 10D                  |                           | 0.         | USANN                         | 10 dager netto       |
| 14 DAGER    | 14D                  |                           | 0.         | USANN                         | 14 dager netto       |
| 15 DAGER    | 15D                  |                           | 0.         | USANN                         | 15 dager netto       |
| 1M(8D)     | 1M                   | 8D                        | 2.         | USANN                         | 1 måned/2% 8 dager |
| 2 DAGER     | 2D                   |                           | 0.         | USANN                         | 2 dager netto        |
| *2%10NET30* |                      |                           | 0.         | USANN                         |                   |
| 21 DAGER    | 21D                  |                           | 0.         | USANN                         | 21 dager netto       |
| 30 DAGER    | 30D                  |                           | 0.         | USANN                         | 30 dager netto       |
| 60 DAGER    | 60D                  |                           | 0.         | USANN                         | 60 dager netto       |
| 7 DAGER     | 7D                   |                           | 0.         | USANN                         | 7 dager netto        |
| ***CASH PAYME*** |                      |                           | 0.         | USANN                         |                   |
| LM         | LM                   |                           | 0.         | USANN                         | Gjeldende måned     |
| KVL        | 0D                   |                           | 0.         | USANN                         | Kontant ved levering  |
| *NET30*      |                      |                           | 0.         | USANN                         |                   |
| *NET45*      |                      |                           | 0.         | USANN                         |                   |
| *NET60*      |                      |                           | 0.         | USANN                         |                   |
| ***TRANSFER*** |                      |                           | 0.         | USANN                         |                   |

## <a name="see-also"></a>Se også
[Tilordne tabellene og feltene som skal synkroniseres](admin-how-to-modify-table-mappings-for-synchronization.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]