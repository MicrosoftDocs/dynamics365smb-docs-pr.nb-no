---
title: Definer rentenotabetingelser
description: Finn ut hvordan du konfigurerer Business Central slik at du kan informere kunder om tilleggsgebyrer ved å sende rentenotaer.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment due, debt, overdue, fee, charge'
ms.search.form: '6, 494'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Definer rentenotabetingelser

Når en kunde ikke betaler innen forfallsdatoen, kan du beregne renter automatisk og legge dem til de forfalte beløpene på kundekontoen. Du kan informere kunder om tilleggsgebyr ved å sende rentenotaer. Du må først definere en kode som representerer de ulike måtene du vil at programmet skal beregne renter på. Deretter kan du angi denne koden i feltet Kode for rentenotabetingelser på kundekort.  

## Rentenotabetingelser

Du må definere rentenotabetingelser for hver rentenotaberegning og deretter tilordne betingelsene til kunden i feltet **Kode for rentenotabetingelser** på siden **Kunde**.

Renter kan beregnes ved hjelp av enten gjennomsnittlig dagssaldo eller forfalt beløp.

* Gjennomsnitt daglig saldo  
  
  Det er tatt hensyn til hvor mange dager betalingen er forsinketl:  
  *Metoden Gjennomsnittlig daglig saldo* - *Rente* = *Forfalt beløp* x *(Dager forfalt / Renteperiode)* x *(Rentesats / 100)*

* Forfalt saldo  
  
  Rentegebyret er en prosent av forfalt beløp:  
  *Forfalt saldo-metode* - *Rente* = *Forfalt beløp* x *(Rentesats / 100)*

I tillegg er hver betingelse i tabellen Rentenotatekst knyttet til en undertabell, tabellen Rentenotatekst. For hver rentebetingelse kan du definere en start- og/eller sluttekst som kommer ut på rentenotaen.

### Definere rentenotabetingelser

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Rentenotabetingelser**, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene etter behov.
3. Hvis du vil bruke flere kombinasjoner av rentebetingelser, definerer du en kode for hver kombinasjon.

    For hver rentebetingelse kan du spesifisere individuelle betingelser, som kan inkludere tilleggsgebyrer både i LV og i utenlandsk valuta. Du kan definere tilleggsgebyrer i fremmed valuta for hver betingelse på siden **Rentenotabetingelser**.
4. Velg handlingen **Valutaer**.
5. På siden **Valuta for rentenotabeting.** definerer du en valutakode og et tilleggsgebyr for hver betingelse.

    > [!NOTE]  
    > Når du oppretter renter i en utenlandsk valuta, brukes betingelsene for utenlandsk valuta du definerer her, til å opprette rentenotaer. Hvis det ikke er definert noen betingelser for rentenotaer i utenlandsk valuta, brukes rentenotabetingelsene for LV som er spesifisert på siden **Rentenotabetingelser**, og deretter konverteres de til den relevante valutaen.

    For hver rentenotabetingelse kan du angi tekst som skal skrives ut før (**Starttekst**) eller etter (**Sluttekst**), i postene i rentenotaen.  
6. Velg henholdsvis handlingen **Starttekst** eller **Sluttekst**, og fyll ut siden **Rentenotatekst**.
7. Hvis du vil sette inn relaterte verdier automatisk i den resulterende rentenotateksten, angir du plassholderne nedenfor i **Tekst**-feltet.

|Plassholder|Verdi|  
|-----------------|-----------|  
|%1|Innholdet i **Bilagsdato**-feltet i rentenotahodet|  
|%2|Innholdet i **Forfallsdato**-feltet i rentenotahodet|  
|%3|Innholdet i feltet **Rentesats** på de relaterte rentenotabetingelsene|  
|%4|Innholdet i **Restbeløp**-feltet i rentenotahodet|  
|%5|Innholdet i **Rentebeløp**-feltet i rentenotahodet|  
|%6|Innholdet i **Tilleggsgebyr**-feltet i rentenotahodet|  
|%7|Purringens totalbeløp|  
|%8|Innholdet i **Valutakode**-feltet i rentenotahodet|  
|%9|Innholdet i **Bokføringsdato**-feltet i rentenotahodet|  

## Se også

[Innkreve utestående saldi](receivables-collect-outstanding-balances.md)  
[Definer betingelser og grader for purringer](finance-setup-reminders.md)  
[Konfigurere finans](finance-setup-finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
