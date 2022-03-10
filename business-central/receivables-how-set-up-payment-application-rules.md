---
title: Regler for automatisk utligning av betalinger
description: Les mer om hvordan du definerer regler for den automatiske utligning av betalinger på siden Betalingsutligningsregler.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, direct payment posting, reconcile payment, expenses, cash receipts
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: 44e1868529d2f0852c0f21b7279f7d75df174efa
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2022
ms.locfileid: "8137214"
---
# <a name="set-up-rules-for-automatic-application-of-payments"></a>Definere regler for automatisk utligning av betalinger

På siden **Betalingsutligningsregler** definerer du regler for å styre hvordan betalingstekst (på banktransaksjoner) utlignes automatisk med teksten på relaterte åpne (ubetalte) fakturaer, kreditnotaer eller andre oppføringer når du bruker funksjonen **Utlign automatisk** på siden **Betalingsavstemmingskladd**. Hvis du vil ha mer informasjon, kan du se [Avstemme betalinger ved hjelp av automatisk utligning](receivables-how-reconcile-payments-auto-application.md).

Du kan definere nye utligningsregler for betaling ved å velge hvilke typer data i en kladdelinje for betalingsavstemming som må samsvare med data i én eller flere åpne poster, før den relaterte betalingen automatisk utlignes mot de åpne postene. Kvaliteten på hver automatiske utligning vises som verdien **Lav** til **Høy** i feltet **Konfidensintervall** på siden **Betalingsavstemmingskladd** i henhold til utligningsregelen for betaling som ble brukt.

Hver rad på siden **Betalingsutligningsregler** representerer en betalingsutligningsregel. Regler brukes i rekkefølgen som er angitt i feltet **Sorteringsrekkefølge**. Hvis flere regler brukes samtidig, brukes konfidensintervallet for den høyest sorterte regelen.

Den automatiske utligningsfunksjonen er basert på prioriterte søkekriterier. Først prøver funksjonen, i prioritert rekkefølge, å finne samsvar mellom tekst i de fem **Relatert part**-feltene på en kladdelinje og tekst på bankkontoen, i navnet eller i adressen til kunder eller leverandører med ubetalte dokumenter som representerer åpne poster. Deretter prøver funksjonen å samsvare tekst i feltene **Transaksjonstekst** og **Mer transaksjonsinformasjon** på en kladdelinje med tekst i feltene **Eksterndokumentnr.** og **Bilagsnr.** i åpne poster. Til sist prøver funksjonen å finne samsvar mellom beløpet i feltet **Utdragsbeløp** på en kladdelinje og beløpet i åpne poster.

> [!NOTE]
> Tekstsamsvar er bare mulig for tekst som er lengre enn fire tegn.

I tillegg til søkekriteriene gjelder følgende med hensyn til fortegnet for betalingsbeløpet:

- For negative beløp blir det først avstemt mot åpne poster som representerer kundefakturaer og deretter mot leverandørkreditnotaer.
- For positive beløp blir det først avstemt mot åpne poster som representerer leverandørfakturaer og deretter mot kundekreditnotaer.

## <a name="to-set-up-a-payment-application-rule"></a>Slik definerer du en utligningsregel for betaling
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Betalingsutligningsregler** og velge den relaterte koblingen.
2. Definer en ny eller redigert utligningsregel for betaling ved å fylle ut feltene på en linje, som beskrevet i tabellen nedenfor.

|Felt|Beskrivelse|
|-|-|
|**Konfidensintervall**|Angir din tillit til utligningsregelen som du definerer på linjen. <br /></br>Verdien du angir i dette feltet, vises i feltet **Konfidensintervall** på siden **Betalingsavstemmingskladd** i henhold til kvaliteten på den automatiske betalingsutligningen på kladdelinjen.|
|**Prioritet**|Angir prioriteten til utligningsregelen i forhold til andre utligningsregler som er definert som linjer på siden **Betalingsutligningsregler**. 1 representerer den høyeste prioriteten.|
|**Treff på relatert part**|Angir hvor mye informasjon om kunden eller leverandøren, for eksempel adresse, stedsnavn og bankkontonummer, på kladdelinjen for betalingsavstemming som må samsvare med informasjonen om den åpne posten før utligningsregelen brukes til å utligne betalingen automatisk mot den åpne posten.|
|**Treff på dok.nr. / ekst. dok.nr.**|Angir om teksten på linjen for betalingsavstemmingskladd må samsvare med verdien i feltet **Bilagsnr.** eller feltet **Eksterndokumentnr.** i den åpne posten før utligningsregelen blir brukt til å utligne betalingen til den åpne posten automatisk.|
|**Treff på beløp inkludert toleranse**|Angir hvor mange poster for en kunde eller leverandør som må samsvare med beløpet inklusive betalingstoleranse før utligningsregelen brukes til å utligne en betaling automatisk mot den åpne posten.|
|**Gjennomgang obligatorisk**|Angir om den automatiske betalingsutligningen anbefales for manuell gjennomgang av brukeren før postering. Hvis du velger feltet **Linjer som skal gjennomgås** på siden **Betalingsutligningskladd**, startes en veiledet opplevelse der du enkelt kan gå gjennom flere utligninger i rekkefølge, på siden **Se gjennom betalingsutligning**.|

Tabellen nedenfor beskriver standardreglene for betalingsutligning i [!INCLUDE[prod_short](includes/prod_short.md)].

> [!Important]
> Utligningsreglene for betaling kan være annerledes i din implementering av [!INCLUDE[prod_short](includes/prod_short.md)].

| Konfidensintervall | Prioritet | Treff på relatert part | Treff på dok.nr. / ekst. dok.nr.   | Treff på beløp inkludert toleranse |
|------------------|----------|-----------------------|--------------------------------|--------------------------------|
| Høy             | 1        | Fullstendig                 | Ja - flere                 | Ett treff                      |
| Høy             | 2        | Fullstendig                 | Ja - flere                 | Flere treff               |
| Høy             | 3        | Fullstendig                 | Ja                            | Ett treff                      |
| Høy             | 4        | Fullstendig                 | Ja                            | Flere treff               |
| Høy             | 5        | Delvis             | Ja - flere                 | Ett treff                      |
| Høy             | 6        | Delvis             | Ja - flere                 | Flere treff               |
| Høy             | 7        | Delvis             | Ja                            | Ett treff                      |
| Høy             | 8        | Fullstendig                 | Nei                             | Ett treff                      |
| Høy             | 9        | Nei                    | Ja - flere                 | Ett treff                      |
| Høy             | 10       | Nei                    | Ja - flere                 | Flere treff               |
| Middels           | 1        | Fullstendig                 | Ja - flere                 | Vurderes ikke                 |
| Middels           | 2        | Fullstendig                 | Ja                            | Vurderes ikke                 |
| Middels           | 3        | Fullstendig                 | Nei                             | Flere treff               |
| Middels           | 4        | Delvis             | Ja - flere                 | Vurderes ikke                 |
| Middels           | 5        | Delvis             | Ja                            | Vurderes ikke                 |
| Middels           | 6        | Nei                    | Ja                            | Ett treff                      |
| Middels           | 7        | Nei                    | Ja - flere                   | Vurderes ikke                 |
| Middels           | 8        | Delvis             | Nei                             | Ett treff                      |
| Middels           | 9        | Nei                    | Ja                            | Vurderes ikke                 |
| Lav              | 1        | Fullstendig                 | Nei                             | Ingen treff                     |
| Lav              | 2        | Delvis             | Nei                             | Flere treff               |
| Lav              | 3        | Delvis             | Nei                             | Ingen treff                     |
| Lav              | 4        | Nei                    | Nei                             | Ett treff                      |
| Lav              | 5        | Nei                    | Nei                             | Flere treff               |

## <a name="see-related-training-at-microsoft-learn"></a>Se relatert opplæring på [Microsoft Learn](/learn/modules/reconciliation-journals-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også
[Avstemme betalinger ved hjelp av automatisk utligning](receivables-how-reconcile-payments-auto-application.md)  
[Håndtere fordringer](receivables-manage-receivables.md)  
[Salg](sales-manage-sales.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]