---
title: Annullere betalinger
description: Forbedringer i den norske versjonen gjør det mulig å annullere betalinger.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 37a54b4d0d13f18bea07700fd35890bd72cdc415
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2019
ms.locfileid: "826995"
---
# <a name="cancel-payments"></a>Annullere betalinger
[!INCLUDE[d365fin](../../includes/d365fin_md.md)] inneholder forbedringer i den norske versjonen, som gjør det mulig å annullere betalinger. Hvis betalingen er sendt til banken, må banken kontaktes, for å sørge for at remitteringen banken har mottatt, blir annullert.  

- Et betalingsoppdrag kan annulleres hvis banken ikke mottar betalingen, og det må utføres en ny remittering. Du kan også annullere et oppdrag hvis du ikke vil overføre betalingene til banken, for eksempel hvis åpne oppdrag er feil. Bare åpne betalingsoppdrag kan avbrytes.  

- En enkeltstående betaling kan annulleres hvis banken ikke kan behandle betalingen, og det må utføres en ny remittering. Du kan også annullere en betaling hvis du ikke vil behandle betalingen. Oppgjorte betalinger kan ikke annulleres.  

## <a name="to-cancel-a-payment-order"></a>Slik annullerer du et oppdrag:  

1.  Velg ikonet ![Søk etter side eller rapport](../../media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Remitteringsoppdrag**, og velg deretter den relaterte koblingen.  
2.  Velg oppdraget, velg **Eksportere**, og velg deretter handlingen **Annullere oppdrag**.  
3.  Velg **Ja**-knappen.  

## <a name="to-cancel-a-payment"></a>Slik annullerer du en betaling:  

1.  Velg ikonet ![Søk etter side eller rapport](../../media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Ventekladd**, og velg deretter den relaterte koblingen.  
2.  Velg betalingen, og velg deretter handlingen **Annullere betaling**.  
3.  Velg **Ja**-knappen.  

## <a name="see-also"></a>Se også  
 [Elektroniske betalinger til leverandører i Norge](electronic-payments-to-vendors-in-norway.md)   
 [Sette opp remitteringsavtaler](how-to-set-up-remittance-agreements.md)   
 [Opprette remitteringskontoer](how-to-create-remittance-accounts.md)   
 [Angi leverandører for remittering](how-to-set-up-vendors-for-remittance.md)   
 [Mottakerreferansekoder](recipient-reference-codes.md)   
 [Opprette remitteringsforslag](how-to-create-remittance-suggestions.md)   
 [Opprette manuelle remitteringsoppdrag](how-to-create-manual-remittance-payments.md)   
 [Definere betalingslinjeinformasjon](how-to-set-up-payment-line-information.md)   
 [Kontrollere remitteringsoppdrag](how-to-test-remittance-payments.md)   
 [Eksportere remitteringsoppdrag](how-to-export-remittance-payments.md)   
 [Typer betalingsreturfiler](types-of-payment-returns-files.md)   
 [Importere betalingsreturdata](how-to-import-payment-return-data.md)   
 [Slette remitteringsoppdrag](how-to-delete-remittance-payment-orders.md)   
 [Remitteringsfeil](remittance-errors.md)   
 [Vise remitteringsfeilkoder](how-to-view-remittance-error-codes.md)
