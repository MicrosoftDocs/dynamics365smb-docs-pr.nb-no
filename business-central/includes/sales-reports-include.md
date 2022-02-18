---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: f25e82f8276715d8d5e945bd5d6a309e12502f8e
ms.sourcegitcommit: 2c972dfc94d27245eaa99efcf638d030dedafb22
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/09/2022
ms.locfileid: "8104148"
---
Tabellen nedenfor beskriver noen av nøkkelrapportene i salgsrapportering.

|Rapport |Objekt-ID|Beskrivelse  |
|---------|---------|---------|
|**Kunde – ordrebeholdning**|107| Viser vareoppgjøret med det antallet som ikke ennå er levert, for hver kunde i tre perioder på 30 dager hver, fra og med den angitte datoen. Det vises dessuten kolonner med ordrer som skal leveres før og etter de 3 periodene og en kolonne med ordrebeholdningen pr. kunde i alt. Bruk rapporten til analyse av firmaets forventede omsetning. |
|**Kunde – ti på topp-liste**|111| Viser informasjon om kundenes kjøp og saldoer for en bestemt periode. Du kan angi antall kunder som skal være med i rapporten. Bare kundene som har kjøp i perioden eller saldo ved slutten av perioden, vises i rapporten.<br>Kundene sorteres etter beløp, og du bestemmer selv om de skal sorteres etter salgsbeløp eller saldo. Rapporten gir et raskt overblikk over hvilke kunder som kjøper eller skylder mest.|
|**Kunde/vare-statistikk**|113|Viser en oversikt over varesalg for hver kunde i en bestemt tidsperiode. Rapporten inneholder informasjon om antall, salgsbeløp, fortjeneste og eventuelle rabatter. Den kan for eksempel brukes til å analysere et selskaps kundegrupper.|
|**Vare – kundestatistikk**|713|En oversikt fra lagerperspektivet. Dette er en annen visning sammenlignet med rapporten **Kunde/vare-statistikk**, og den viser først varen og deretter kunden som kjøpte dette produktet.|
|**Kunde – salgsoversikt**|119|Viser kundesalg for en periode. Den brukes til å rapportere til toll- og avgiftsmyndighetene. Du kan velge å inkludere bare kunder med totalsalg som overstiger et minimumsbeløp. Du kan også angi om du vil at rapporten skal vise adresseopplysninger for hver kunde.<br>Rapporten baseres på registrert salg (LV) fra kundeposter. Nederst i vinduet med rapporten vises det totalt rapporterte salget i LV. Totalsummen er basert på kundene du har tatt med i rapporten, det vil si kunder som er i samsvar med filteret på hurtigfanen Kunder, og som har et totalsalg som er høyere enn beløpet som er angitt i feltet **Beløp (LV) større enn** på hurtigfanen **Alternativer**.|
|**Kunde – saldo per dato**|121|Viser en detaljert saldo for utvalgte kunder. Bruk rapporten for eksempel ved slutten av en regnskapsperiode eller et regnskapsår.|
|**Kunde – saldoliste**|129|Viser en saldo for bestemte kunder. Du kan bruke rapporten til å bekrefte at saldoen for en bestemt kundebokføringsgruppe er lik saldoen i den tilsvarende finanskontoen på en bestemt dato. Bruk rapporten for eksempel ved slutten av en regnskapsperiode eller et regnskapsår. Hvis du trenger en mer detaljert versjon av denne rapporttypen, bruker du rapporten **Kundeutdrag – saldoliste** (104).|
|**Salgsstatistikk**|112|[!INCLUDE [reports-sales-statistics](reports-sales-statistics.md)] |
|**Salgsreserv. – tilgjengelighet**|209|Viser tilgjengeligheten av varer til levering på salgsbilag. Du bestemmer om rapporten skal angi status for hvert bilag eller for hver salgslinje. Når du skriver ut rapporten, kan du også oppdatere antallet som er tilgjengelig for levering i feltet **Levere (antall)** på salgslinjene. Deretter kan du bruke rapporten til å angi hvilke bilag som skal bokføres.<br>Det finnes også en funksjon der du kan definere antallet varer som skal leveres. **Obs**! Denne rapporten er ikke tilgjengelig for avanserte lagerfunksjoner.|
|**Lagerleveringsstatus**|7313|Denne rapporten kan brukes for alle lokasjoner der feltet **Levering nødv.** er valgt. Rapporten **Lagerleveringsstatus** viser alle uposterte lagerleveringsdokumenter, inkludert lokasjoner, hyllekoder, dokumentstatus, antall og så videre. Denne rapporten er perfekt for å få en oversikt.|
|**Lagerplukkliste**|813|Viser en oversikt over ordrer der en vare er inkludert. Følgende informasjon vises for hver vare: ordrelinje med kundenavn, variantkode, lokasjonskode, hyllekode, leveringsdato, mengde som skal leveres og enhet. Mengden som skal leveres legges sammen for hver vare. Rapporten kan for eksempel brukes når det skal hentes varer fra lageret.<br>**Obs**! Denne rapporten er ikke tilgjengelig for avanserte lagerfunksjoner.|
|**Vare – restordrer til kunder**|718|Viser en oversikt over ordrelinjer der leveringsdatoen er oversteget. Følgende informasjon vises for hver vare: nummer, kundenavn, kundens telefonnummer, leveringsdato, ordreantall og antall i restordre. Rapporten viser også om kunden har andre varer i restordre.|
|**Varer i ordrer**|708|Viser en oversikt over ordrene som ennå ikke er levert, samt varene i ordrene. Den viser ordrenummer, kundens navn, leveringsdato, ordreantall, antall forsinket, restantall, salgspris samt eventuell rabattprosent og -beløp. Antall i restordrer, restantall og beløp legges sammen for hver vare. Bruk rapporten til å vise om det finnes akutte eller kommende leveringsproblemer.|