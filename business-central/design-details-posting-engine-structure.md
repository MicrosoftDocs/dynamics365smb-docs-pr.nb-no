---
title: Designdetaljer – Strukturen til bokføringsmotoren | Microsoft-dokumentasjon
description: Bokføringsgrensesnittet og enkelte andre funksjoner i kodeenhet 12 bruker bokføringsmotorfunksjoner til å klargjøre og sette inn finansposter og mva-poster. Bokføringsmotoren er også ansvarlig for opprettelse av finansjournal.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 80482301e9a6a5c30c631ffa936517919bbeb848
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/09/2021
ms.locfileid: "6214956"
---
# <a name="design-details-posting-engine-structure"></a>Designdetaljer: Strukturen til bokføringsmotoren
Bokføringsgrensesnittet og enkelte andre funksjoner i kodeenhet 12 bruker bokføringsmotorfunksjoner til å klargjøre og sette inn finansposter og mva-poster. Bokføringsmotoren er også ansvarlig for opprettelse av finansjournal.  
  
 Funksjonene i tabellen nedenfor gir et standard rammeverk for utforming av bokføringsprosedyrer (for eksempel Code, CustPostApplyCustledgEntry, VendPostApplyVendLedgEntry, UnapplyCustLedgEntry, UnapplyVendLedgEntry og Reverse) og alenetilgang til tabell 17, Finanspost.  
  
|Rutine|Beskrivelse|  
|-------------|---------------------------------------|  
|StartPosting|Initialiserer bokføringsbufferen TempGLEntryBuf, låser tabellene Finanspost og Mva-post og initialiserer Regnskapsperiode, Finansjournal og Valutakurs. Bør bare kalles én gang, og deretter er NextEntryNo lik 0.|  
|ContinuePosting|Kontrollerer og bokfører urealisert mva for forrige transaksjonsøkning NextTransactionNo og klargjør bokføring av neste linje.|  
|FinishPosting|Fullfører bokføring ved å sette inn finansposter fra midlertidig buffer til databasetabell. Brukes alltid sammen med StartPosting. Kontrollerer om det finnes inkonsekvenser.|  
|InitGLEntry|Brukes til å initialisere ny finanspost for finanskladdelinje. Returnerer GLEntry som parameter.|  
|InitGLEntryVAT|Samme som InitGLEntry, men tilordner også Motkontonr. og SummarizeVAT.|  
|InitGLEntryVATCopy|Ligner på InitGLEntryVAT, men kopierer også bokføringsgruppedata fra mva-post før SummarizeVAT.|  
|InsertGLEntry|Den eneste funksjonen som setter inn finanspost i den globale tabellen TempGLEntryBuf. Bruk alltid denne funksjonen til å sette inn.|  
|CreateGLEntry|Utfører InitGLEntry, tilordner tilleggsvalutabeløp og utfører deretter InsertGLEntry. Erstatter flere kodelinjer med ett funksjonskall.|  
|CreateGLEntryBalAcc|Samme som CreateGLEntry, men tilordner også Motkontotype og Motkontonr.|  
|CreateGLEntryVAT|Samme som CreateGLEntry, men med ekstra behandling for bokføringsgrupper samt lagring til midlertidig mva-buffer:<br /><br /> `GLEntry.CopyPostingGroupsFromDtldCVBuf(DtldCVLedgEntryBuf,GenJnlLine."Gen. Posting Type");`<br /><br /> `InsertVATEntriesFromTemp(DtldCVLedgEntryBuf,GLEntry);`|  
|CreateGLEntryVATCollectAdj|Samme som CreateGLEntry, men med en ekstra samling justeringer samt lagring til midlertidig mva-buffer:<br /><br /> `CollectAdjustment(AdjAmount,GLEntry.Amount,GLEntry."Additional-Currency Amount",OriginalDateSet);`<br /><br /> `InsertVATEntriesFromTemp(DtldCVLedgEntryBuf,GLEntry);`|  
|CreateGLEntryFromVATEntry|Samme som CreateGLEntry, men kopierer også bokføringsgrupper fra mva-post.|  
  
## <a name="see-also"></a>Se også  
 [Designdetaljer: Strukturen til bokføringsgrensesnittet](design-details-posting-interface-structure.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]