---
title: Arbeide med sjekker| Microsoft-dokumentasjon
description: Arbeide med sjekker
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment journal, print check, vendor payment, creditor, debt, balance due, AP
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 6debfe7d1f5e9726ba1f70d023076d73f123ef24
ms.contentlocale: nb-no
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-work-with-checks"></a>Arbeide med sjekker
Du kan utstede elektroniske og manuelle sjekker i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Begge metodene bruker utbetalingskladden til å utstede sjekker til leverandører. Du kan også kansellere sjekker og vise sjekkposter.

Prosessen med å utstede sjekker foreslår utbetalinger, oppretter poster og skriver ut de maskinelle sjekkene.

**Merk**: For å være sikker på at banken bare fjerner validerte sjekker og beløp kan du sende dem en fil som inneholder informasjon om leverandør, sjekk og betaling. Hvis du vil ha mer informasjon, kan du se [Eksportere en Positive Pay-fil](finance-how-positive-pay.md).

Skriveren må være riktig konfigurert for sjekkskjemaene, og du må definere hvilke sjekkoppsett som skal brukes. Hvis du vil ha mer informasjon, kan du se [Definere sjekkoppsett](finance-how-define-check-layouts.md)

## <a name="to-issue-checks"></a>Utstede sjekker
1. I øvre høyre hjørne velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Utbetalingskladder**, og deretter velger du den beslektede koblingen.
2. Fyll ut kladden med relevante betalinger, for eksempel ved hjelp av funksjonen Betalingsforslag - leverandør. Hvis du vil ha mer informasjon, kan du se [Betalingsforslag - leverandør](payables-how-suggest-vendor-payments.md).
3. I **Bankbetalingstype**-feltet på kladdelinjer for betaling som du vil gjøre med sjekker, velger du ett av følgende alternativer:

   * **Maskinell sjekk**: Velg dette alternativet hvis du vil at programmet skal opprette og senere skrive ut en sjekk på beløpet på betalingskladdelinjen. Du må skrive ut sjekkene før du kan bokføre kladdelinjene. Du kan bare velge **Maskinell sjekk** hvis **Motkontotype** eller **Kontotype** er **Bankkonto**.
   * **Manuell sjekk**: Velg dette alternativet hvis du manuelt har skrevet en sjekk og vil at programmet skal opprette en tilhørende sjekkpost på dette beløpet. Når du bruker dette alternativet, kan du ikke skrive ut sjekker fra [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du kan bare velge **Manuell sjekk** hvis **Motkontotype** eller **Kontotype** er **Bankkonto**.

     **Merk**: Du må skrive ut maskinelle sjekkene før du kan bokføre de relaterte kladdelinjene.
4. Velg **Skriv ut sjekk** for maskinelle sjekker.
5. Fyll ut feltene etter behov i vinduet **Sjekk**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Velg **Skriv ut**.

**Merk**: Hvis du vil skrive ut sjekker i flere valutaer fra forskjellige bankkonti, må du utføre kjørselen **Skriv ut sjekk** separat for hver enkelt valuta og angi riktig bankkonto.

## <a name="to-cancel-printed-checks-that-are-not-posted"></a>Kansellere utskrevne sjekker som ikke er bokført
Du kan kansellere ikke-bokførte sjekker etter at de er skrevet ut, ved hjelp av handlingen **Kanseller sjekk** i vinduet **Betalingskladd**.

1. I vinduet **Betalingskladd** velger du **Kanseller sjekk**, og deretter velger du hvilke sjekker som skal kanselleres.

## <a name="to-void-checks"></a>Kansellere sjekker
Når sjekkbetaliner er bokført, kan du bare kansellere (void) sjekker fra de resulterende bankpostene.

1. I øvre høyre hjørne, velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Bankkonti**, og deretter velger du den beslektede koblingen.
2. Velg relevant bankkonto, velg handlingene **Rediger** og **Sjekkposter**.
3. I vinduet **Sjekkposter** velger du handlingen **Kanseller sjekk**.
4. Merk av for **Kanseller sjekk**.
5. Velg **OK**-knappen.

## <a name="see-also"></a>Se også
[Administrere skyldige beløp](payables-manage-payables.md)  
[Konfigurere banktjenester](bank-setup-banking.md)  
[Eksportere en Positive Pay-fil](finance-how-positive-pay.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

