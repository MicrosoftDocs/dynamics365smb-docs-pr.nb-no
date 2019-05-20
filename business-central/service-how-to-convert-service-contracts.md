---
title: Konvertere servicekontrakter | Microsoft-dokumentasjon
description: Siden verktøyet for endring av mva-sats ikke kan konverteres til servicekontrakter, må du konvertere disse kontraktene manuelt. Dette emnet beskriver flere alternative metoder som du kan bruke for servicekontraktkonvertering.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 82c7e19c2c493df77094bd3b6e4d2e5835a278bb
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2019
ms.locfileid: "1250782"
---
# <a name="convert-service-contracts-that-include-vat-amounts"></a>Konvertere servicekontrakter som inkluderer mva-beløp
Siden verktøyet for endring av mva-sats ikke kan konverteres til servicekontrakter, må du konvertere disse kontraktene manuelt. Dette emnet beskriver flere alternative metoder som du kan bruke for servicekontraktkonvertering.  

> [!NOTE]  
>  Dette emnet gir en arbeidsflyt på høyt nivå.  

 Følgende fremgangsmåte beskriver hvordan du korrigerer en faktura for en forhåndsbetalt servicekontrakt som er opprettet et år i forveien.  

> [!NOTE]  
>  I dette eksemplet må du endre arbeidsdatoen til 01.01.2017.  

### <a name="to-correct-an-invoice-for-a-prepaid-service-contract"></a>Slik retter du opp en faktura for en forhåndsbetalt servicekontrakt:  
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kontrakthåndtering**, og velg deretter den relaterte koblingen.  
2. Velg **Servicekontrakter** under **Oversikter**.  
3. Opprett en ny forhåndsbetalt servicekontrakt. Angi **01.01.2017** som startdato, og angi et fakturaperiodår for kunde **20000**.  
4. Denne kontrakten må signeres. I fanebladet **Hjem**, under **Prosess** velger du **Signer kontakt**.  
5. Opprett en servicefaktura.
6. Fakturaen er oppført som en ikke-bokført servicefaktura. Hvis du vil vise servicefakturaen, velger du **Service**, **Kontrakthåndtering** og deretter **Servicefakturaer**.  
7. Bokfør servicefakturaen.  

> [!NOTE]  
>  Ikke endre fakturaen som ikke er bokført. Siden servicepostene opprettes når fakturaen opprettes, vil ikke en endring i den ikke-bokførte fakturaen endre de allerede opprettede servicepostene. Mva-postene opprettes imidlertid når fakturaen er bokført. Dette lar deg endre varebokføringsgruppen og GSP-varebokføringsgruppen på den ikke-bokførte servicefakturaen.  

### <a name="to-create-a-credit-memo-for-vat-difference"></a>Slik oppretter du en kreditnota for mva-differanse:  
Følgende fremgangsmåte beskriver hvordan du oppretter en kreditnota som bare inneholder mva-differansen for den allerede fakturerte perioden som starter **01.07.2017**. I dette eksemplet bokføres mva-beløpet bare i Økonomistyring-modulen, ikke i Service-modulen. Mva-postene som er knyttet til serviceposten, blir ikke korrigert.  

1. Opprett en ny finanskonto for mva-differansen. Denne kontoen brukes til direkte bokføring av mva-korrigering.  
2. Legg til en ny linje i mva-bokføringsoppsettet.  

### <a name="to-create-contract-expiration-dates-in-contract-lines"></a>Slik oppretter du kontraktutløpsdatoer i kontraktlinjer:  
Følgende fremgangsmåte beskriver hvordan du oppretter nye kontrakter ved å arbeide med kontraktenes utløpsdatoer på servicekontraktlinjer.  

1. Angi **30.06.2017** for utløpsdatoen for kontrakten på siden **Servicekontakt**.  
2. Velg handlingen **Opprett kreditnota** for å automatisk opprette en kreditnota for juli 2017 til desember 2017.  
3. Siden kontrakten er utløpt, må du opprette en ny kontrakt for perioden med den nye mva-satsen for 1. juli 2017 til 31. desember 2017.  

### <a name="to-create-a-new-credit-memo"></a>Slik oppretter du en ny kreditnota  
Følgende fremgangsmåte beskriver hvordan du oppretter en ny kreditnota ved hjelp av kjørselen **Hent forh.bet. kontraktposter**. Poster som du ikke vil rette fra januar 2017 til juni 2017, vil bli slettet.  

1. Kjør verktøyet for endring av mva-sats 1. juli 2017. Varebokføringsgruppen eller mva-varebokføringsgruppen endrets. Hvis du vil ha mer informasjon, kan du se [Arbeide med mva på kjøp og salg](finance-work-with-vat.md).  
2. Når du har kjørt verktøyet for endring av mva-satsen, angir du en utløpsdato for servicekontrakten. Du kan nå slette servicekontraktlinjen og opprette en ny linje som er identisk med den gamle.  
3. Opprett en ny faktura for perioden januar 2017 til desember 2012 ved hjelp av den nye mva-satsen.  
4. Hvis du vil opprette en annen kreditnota, velger du siden **Salgskreditnotaer (service)** og **Ny** for å opprette en ny salgskreditnota (service).  
5. Velg handlingen **Hent forh.bet. kontraktposter**.  
6. Når konverteringen er fullført, vil MVA-poster og serviceposter være riktige.  

## <a name="see-also"></a>Se også  
[Arbeide med servicekontrakter og servicekontrakttilbud](service-how-to-create-service-contracts-and-service-contract-quotes.md)  
[Finans](finance.md)  
[Rapportere mva til skattemyndighetene](finance-how-report-vat.md)  
[Arbeide med mva på kjøp og salg](finance-work-with-vat.md)  
