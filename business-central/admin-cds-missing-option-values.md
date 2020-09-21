---
title: Håndtere manglende alternativverdier
description: Finn ut hvordan du kan hindre at full synkronisering mislykkes fordi alternativene er forskjellige i tilordnede felt.
author: bholtorf
ms.author: bholtorf
ms.custom: na
ms.reviewer: na
ms.service: dynamics365-business-central
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 5f914904aaa1ec568b396a830ebc18a0fe4e40c1
ms.sourcegitcommit: 79d6d270325f1cc88bd4e9a273f9ff859ceadcbc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/13/2020
ms.locfileid: "3693027"
---
# <a name="handling-missing-option-values"></a>Håndtere manglende alternativverdier
[!INCLUDE[d365fin](includes/cds_long_md.md)] inneholder bare tre alternativsettfelt som inneholder alternativverdier som du kan tilordne til [!INCLUDE[d365fin](includes/d365fin_md.md)]-felt av typen Alternativ<!-- Option type, not enum? @Onat can you vertify this? --> for automatisk synkronisering. Under synkroniseringen ignoreres ikke-tilordnede alternativer, og de manglende alternativene legges til i den relaterte [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabellen og legges til i systemtabellen **Tilordning av CDS-alternativ** for å behandles manuelt senere. Det kan for eksempel være å legge til de manglende alternativene i hvert produkt og deretter oppdatere tilordningen. Dette avsnittet beskriver hvordan det fungerer.

Siden **Tilordning for integreringstabell** inneholder tre tilordninger for felt som inneholder én eller flere tilordnede alternativverdier. Etter en full synkronisering inneholder siden **Tilordning av CDS-alternativ** de ikke-tilordnede alternativene i respektive tre felt.

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

Innholdet på siden **Tilordning av CDS-alternativ** er basert på opplistingsverdier i tabellen **CDS-konto**. I [!INCLUDE[d365fin](includes/cds_long_md.md)] blir følgende felt i kontoenheten tilordnet til felt i kunde- og leverandørpostene:

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

Alle opplistingene i [!INCLUDE[d365fin](includes/d365fin_md.md)] ovenfor tilordnes til alternativsett i [!INCLUDE[d365fin](includes/cds_long_md.md)].

### <a name="extending-option-sets-in-d365fin"></a>Utvide alternativsett i [!INCLUDE[d365fin](includes/d365fin_md.md)]
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
> Du må bruke de samme ID-verdiene for alternativ fra [!INCLUDE[d365fin](includes/cds_long_md.md)] når du utvider opplistingen i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Ellers mislykkes synkroniseringen.

> [!IMPORTANT]  
> Ikke bruk tegnet «,» i opplistingsverdiene og bildetekstene. Dette støttes for øyeblikket ikke av [!INCLUDE[d365fin](includes/d365fin_md.md)]-kjøretiden.

> [!NOTE]
> De første ti tegnene i navnene på og tekstene for de nye alternativverdiene må være unike. To alternativer, for eksempel Overføring av 20 virkedager og Overføring av 20 kalenderdager, vil forårsake feil fordi begge har de samme 10 første tegnene ("Overføring"). Gi dem for eksempel navnet "Ovf 20 vrk" og "Ovf 20 kad".

### <a name="update-d365fin-option-mapping"></a>Oppdater Tilordning av [!INCLUDE[d365fin](includes/cds_long_md.md)]-alternativ
Nå kan du gjenopprette tilordningen mellom [!INCLUDE[d365fin](includes/cds_long_md.md)]-alternativer og [!INCLUDE[d365fin](includes/d365fin_md.md)]-poster.

På siden **Tilordning for integreringstabell** velger du linjen for tilordningen **Betalingsbetingelser**, og deretter velger du handlingen **Synkroniser endrede poster**. Siden **Tilordning av CDS-alternativ** oppdateres med tilleggspostene nedenfor.

|         Post                 | Alternativverdi   | Tittel for alternativverdi |
|--------------------------------|----------------|----------------------|
| Betalingsbetingelser: NET30           | 1              | Net 30               |
| Betalingsbetingelser: 2%10NET30       | 2              | 2% 10; Net 30        |
| Betalingsbetingelser: NET45           | 3              | Net 45               |
| Betalingsbetingelser: NET60           | 4              | Net 60               | 
| **Betalingsbetingelser: CASH PAYME**  | **779800001**  | **Cash Payment**     |
| **Betalingsbetingelser: TRANSFER**    | **779800002**  | **Overføring**         |

Tabellen **Betalingsbetingelser** i [!INCLUDE[d365fin](includes/d365fin_md.md)] viser da nye poster for [!INCLUDE[d365fin](includes/cds_long_md.md)]-alternativene. I følgende tabell er det nye alternativer med fet skrift. Rader i kursiv representerer alle alternativer som nå kan synkroniseres. Gjenstående rader representerer alternativer som ikke er i bruk og vil bli ignorert under synkronisering. Du kan fjerne eller utvide CDS-alternativer med samme navn.)

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
