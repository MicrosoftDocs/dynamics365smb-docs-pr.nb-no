---
title: "La Dynamics 365 for Financials foreslå verdier | Microsoft-dokumentasjon"
description: "Beskriver hvordan du får systemet til å forhåndsutfylle valgte felt med verdier som du ellers måtte beregne og fylle ut manuelt."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 03/15/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 785ad537f81b8388aa14654f375599a13b66e3c5
ms.contentlocale: nb-no
ms.lasthandoff: 05/04/2017


---
# <a name="letting-dynamics-365-for-financials-suggest-values"></a>La Dynamics 365 for Financials foreslå verdier
[!INCLUDE[d365fin](includes/d365fin_md.md)] kan hjelpe deg med å fullføre oppgaver raskere og mer riktig ved å forhåndsutfylle felt eller hele linjer med data som du ellers måtte beregne og skrive inn selv. Selv om slik automatisk dataregistrering alltid er riktig, kan du endre den senere ved behov.

Funksjonalitet som angir feltverdiene for deg tilbys vanligvis for oppgaver der du skriver inn store mengder transaksjonsdata og vil unngå feil og spare tid. Dette emnet inneholder et utvalg av slik funksjonalitet. Flere avsnitt vil bli lagt til i fremtidige oppdateringer av [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="the-suggest-balancing-amount-check-box-in-the-general-journal-batches-window"></a>Avmerkingsboksen **Foreslå motkontobeløp** i vinduet **Finanskladder**
Når du for eksempel angir finanskladdlinjer for flere utgifter som alle må bokføres til samme bankkonto, kan du få **Beløp**-feltet på bankkontolinjen oppdateres automatisk til beløpet som balanserer utgiftene, hver gang du angir en ny kladdelinje for en utgift. Hvis du vil ha mer informasjon om hvordan du arbeider med finanskladder, kan du se [Arbeide med finanskladder](ui-work-general-journals.md).

### <a name="to-have-the-amount-field-on-balancing-general-journal-lines-filled-automatically"></a>Fylle ut **Beløp**-feltet automatisk på finanskladdlinjer for motkonto
1. I øvre høyre hjørne velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Finanskladder**, og deretter velger du den beslektede koblingen.
2. På linjen for din foretrukne finanskladd kan du merke av for **Foreslå motkontobeløp**.
3. Åpne finanskladden, og fortsett med å registrere og bokføre transaksjoner ved hjelp av funksjonen som er beskrevet for automatisk registrering av en feltverdi.       

Hvis du vil ha informasjon om hvordan du konfigurerer en personlig finanskladd, for eksempel for håndtering av utgifter, kan du se [Arbeide med finanskladder](ui-work-general-journals.md).

## <a name="the-automatically-fill-date-received-field-in-the-payment-registration-window"></a>Feltet **Fyll ut mottaksdato automatisk** i vinduet **Betalingsregistrering**
Vinduet **Betalingsregistrering** viser utestående innkommende betalinger som linjer som representerer salgsdokumenter der et beløp er forfalt til betaling. Hvis du vil ha mer informasjon om utligning av kundebetalinger, kan du se [Avstemme kundebetalinger manuelt fra en liste over ubetalte salgsdokumenter](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md)

De viktigste handlingene i vinduet er å merke av for **Betaling utført** og fylle ut feltet **Mottatt den**. Du kan definere at [!INCLUDE[d365fin](includes/d365fin_md.md)] automatisk angir arbeidsdatoen i feltet **Mottatt den** når du merker av for **Betaling utført**.

### <a name="to-have-the-date-received-field-in-the-payment-registration-window-filled-automatically"></a>Fylle ut feltet **Mottatt den** automatisk i vinduet **Betalingsregistrering**
1. I øvre høyre hjørne, velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Betalingsregistreringsoppsett**, og deretter velger du den beslektede koblingen.
2. Merk av for **Fyll ut mottaksdato automatisk**.
3. Åpne vinduet **Betalingsregistrering**, og fortsett med å behandle inngående kundebetalinger ved hjelp av funksjonen som er beskrevet for automatisk registrering av en feltverdi.

## <a name="see-also"></a>Se også
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Finans](Finance.md)


