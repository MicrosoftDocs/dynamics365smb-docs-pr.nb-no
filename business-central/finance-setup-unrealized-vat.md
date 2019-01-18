---
title: Definere urealisert merverdiavgift | Microsoft-dokumentasjon
description: "Hvis du bruker kontantbasert regnskap, kan du angi hvordan urealisert MVA for salg og innkjøp skal håndteres."
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cash, VAT, unrealized, cash-based
ms.date: 11/15/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 1a460bed4be049ddd1eff7c33ae43c70e65ab403
ms.contentlocale: nb-no
ms.lasthandoff: 11/26/2018

---

# <a name="set-up-unrealized-vat-for-cash-based-accounting"></a>Definere urealisert merverdiavgift for kontantbasert regnskap
Hvis du bruker metoder for kontantbasert regnskap, kan du definere [!INCLUDE[d365fin](includes/d365fin_md.md)] for å håndtere urealisert MVA.

## <a name="to-use-general-ledger-accounts-for-unrealized-vat"></a>Slik bruker du finanskonti for urealisert MVA
Du kan beregne og bokføre mva-beløp til en midlertidig finanskonto når fakturaen bokføres, og deretter bokføre den til den riktige finanskontoen og inkludere den i mva-oppgaver når den faktiske betalingen av fakturaen bokføres. Før du kan gjøre dette, må du fullføre mva.-bokføringsoppsettet.

Hvis du vil bruke konti for urealisert MVA, gjør du følgende:
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, og angi **Finansoppsett**.
2. På siden **Finansoppsett** merker du av for **Urealisert mva**.
3. Velg ikonet **Søk etter side eller rapport** ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), og angi **Mva-bokføringsoppsett**.
4. På siden **Mva-bokføringsoppsett** velger du Mva-bokføringsgruppen, og velg deretter handlingen **Rediger**.
5. I feltet **Urealisert mva-type** velger du et alternativ for å angi hvordan betalinger skal knyttes til fakturabeløpet (ekskl. mva) og selve mva-beløpet, og hvordan mva-beløp skal overføres fra en urealisert mva-konto til en (realisert) mva-konto. Tabellen nedenfor beskriver alternativene.

| Alternativ | Beskrivelse |
| --- | --- |
| Tom | Velg dette alternativet hvis du ikke vil bruke funksjonen for urealisert MVA. |
| Prosent | Betalinger dekker både MVA og fakturabeløpet i forhold til prosenten av den totale fakturaen. Det betalte MVA-beløpet blir overført fra konto for urealisert MVA til kontoen for realisert MVA. |
| Første | Betalinger dekker mva først og deretter fakturabeløp. I dette feltet vil beløpet som er overført fra den urealiserte mva-kontoen til mva-kontoen, være likt betalingsbeløpet til hele mva. er betalt. |
| Siste | Betalinger dekker fakturabeløpet først og deretter mva. I dette tilfellet blir ingen beløp overført fra kontoen for urealisert mva. til mva-kontoen før det totale fakturabeløpet, eksklusive MVA, er betalt. |
| Først (fullt betalt) | Betalinger dekker MVA først (som alternativet _Først_), men ingen beløp vil bli overført til MVA-kontoen før hele MVA-beløpet er betalt. |
| Siste (fullt betalt) | Betalinger dekker først fakturabeløpet (som alternativet _Siste_), men ingen beløp vil bli overført til MVA-kontoen før hele MVA-beløpet er betalt. |

6. I feltet **Konto for ureal. utgående mva.** velger du kontoen for urealisert utgående mva.

    > [!NOTE]  
    > Mva-beløpet bokføres på denne kontoen, der det blir værende til kundens betaling er bokført. Beløpet overføres deretter til finanskontoen for utgående mva.
7. I feltet **Konto for ureal. inngående mva.** angir du finanskontoen for urealisert inngående mva.

> [!NOTE]  
> Mva-beløpet bokføres på denne kontoen, der det blir værende til kundens betaling er bokført. Beløpet overføres deretter til finanskontoen for inngående mva.

## <a name="see-also"></a>Se også
[Definere merverdiavgift](finance-setup-vat.md)

