---
title: Opprette dimensjoner| Microsoft-dokumentasjon
description: "Du kan definere dimensjonene og dimensjonsverdiene du vil bruke til å kategorisere i kladder og dokumenter, for eksempel salgsordrer og bestillinger."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 03/28/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 0da77c5be3b49f715384752ad61fc072aea8525c
ms.contentlocale: nb-no
ms.lasthandoff: 05/04/2017


---
# <a name="setting-up-dimensions"></a>Opprette dimensjoner
Du kan definere dimensjonene og dimensjonsverdiene for å kategorisere i kladder og dokumenter, for eksempel salgsordrer og bestillinger. Du definerer dimensjoner i **Dimensjoner**-vinduet der du oppretter én linje for hver dimensjon, som *Prosjekt*, *Avdeling*, *Område* og *Selger*.

Du også definere verdier for dimensjoner. Verdier kan for eksempel være avdelinger i firmaet. Dimensjonsverdier kan defineres i en hierarkisk struktur som ligner på kontoplanen, slik at data kan brytes ned i ulike størrelsesnivåer, og delsett med dimensjonsverdier kan legges sammen. Du kan definere så mange dimensjoner og dimensjonsverdier som du trenger, og alle i firmaet kan bruke dem.

Du kan også definere globale dimensjoner og snarveisdimensjoner:  

* **Globale dimensjoner** brukes som filtre, for eksempel i rapporter og kjørsler. Du kan bruke bare to globale dimensjoner, så velge dimensjonene du vil bruke ofte.
* **Snarveisdimensjoner** er tilgjengelige som felt på journal- og dokumentlinjer. Du kan opprette opptil seks av disse.  

**Merk**: Denne funksjonen krever at opplevelsen er satt til **Løsning**. Hvis du vil ha mer informasjon, se [Tilpasse din [!INCLUDE[d365fin](includes/d365fin_md.md)]-opplevelse](ui-experiences.md).

## <a name="set-up-default-dimensions-for-customers-vendors-and-other-accounts"></a>Definere standarddimensjoner for kunder, leverandører og andre kontoer
Du kan tilordne en standarddimensjon for en spesifikk konto. Dimensjonen kopieres til kladden eller bilaget når du angi nummeret på en linje, men du kan slette eller endre koden på linjen, hvis aktuelt. Du kan også gjøre en dimensjon som er nødvendige for postering av en oppføring for en bestemt type konto.  

## <a name="translate-the-names-of-dimensions"></a>Oversette navnene på mål
Når du oppretter en dimensjon, og spesielt en snarveisdimensjon, er hva du faktisk oppretter en egendefinert overskrift for feltet eller kolonnen. Hvis din bedrift er internasjonal, kan du gi oversettelser for navnet på dimensjonen. Dokumenter som inneholder dimensjonen skal bruke det oversatte navnet, der det er aktuelt.   

## <a name="example"></a>Eksempel
La oss si at selskapet ønsker å spore transaksjoner som er basert på organisasjonsstruktur og geografiske steder. Hvis du vil gjøre dette, kan du definere to dimensjoner i **Dimensjoner**-vinduet:

* **OMRÅDE**  
* **AVDELING**  

|  - kode | Name | Kodetekst | Filtertekst |
| --- | --- | --- | --- |
| DISTRIKT |Distrikt |Områdekode |Områdefilter |
| AVDELING |Avdeling |Avdelingskode |Avdelingsfilter |

For **OMRÅDE** legger du til følgende dimensjonsverdier:

|  - kode | Name | Dimensjonsverditype |
| --- | --- | --- |
| 10 |Amerika |Fra-sum |
| 2.0 |Nord-Amerika |Standard |
| 30 |Stillehavet |Standard |
| 40 |Sør-Amerika |Standard |
| 50 |Amerika, totalt |Til-sum |
| 60 |Europa |Fra-sum |
| 70 |EU |Standard |
| 80 |Ikke-EU |Standard |
| 90 |Europa, totalt |Til-sum |

For de to viktigste geografiske områdene, Amerika og Europa, kan du legge til underkategorier for områder ved å rykke inn dimensjonsverdiene. Dette gjør at du kan rapportere på salg- eller utgifter i områder, og få totaler for større geografiske områder. Du kan også velge å bruke land eller regioner som dine dimensjonsverdier, eller regioner eller byer, avhengig av virksomheten din.  
**Merk**: Hvis du vil definere et hierarki, må kodene være i alfabetisk rekkefølge. Dette inkluderer kodene for dimensjonsverdiene som tilbys i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

For **AVDELING** legger du til følgende dimensjonsverdier:

|  - kode | Name | Dimensjonsverditype |
| --- | --- | --- |
| ADMIN |Administrasjon |Standard |
| PROD |Produksjon |Standard |
| SALG |Salg |Standard |

Med dette satt opp, du deretter legge til de to dimensjonene som to globale dimensjoner i den **Finansoppsett** vindu. Dette betyr at du kan bruke område og avdeling som filtre for finansposter og alle rapporter og kontoskjemaer. Begge de globale dimensjonene blir også automatisk tilgjengelige til å brukes på postlinjer, i dokumenthoder og som snarveisdimensjoner.  

Med dette satt opp, kan du begynne å legge til dimensjoner i dokumenter og kladder. Hvis du vil ha mer informasjon, kan du se [Dimensjoner](finance-dimensions.md).  

## <a name="see-also"></a>Se også
[Dimensjoner](finance-dimensions.md)  
[Konfigurere finans](finance-setup-finance.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

