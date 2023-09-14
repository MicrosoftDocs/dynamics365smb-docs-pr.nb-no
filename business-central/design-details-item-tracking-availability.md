---
title: Designdetaljer – Varesporingstilgjengelighet
description: 'Sidene Varesporingslinjer og Varesporingssummering inneholder dynamisk tilgjengelighetsinformasjon for serie- eller partinumre, noe som øker gjennomsiktigheten for brukere.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/15/2021
ms.author: bholtorf
---
# <a name="design-details-item-tracking-availability"></a>Designdetaljer: Varesporingstilgjengelighet
Sidene **Varesporingslinjer** og **Varesporingssummering** inneholder dynamisk tilgjengelighetsinformasjon for serie- eller partinumre. Hensikten med dette er å gjøre utgående dokumenter, for eksempel ordrer, klarere for brukere ved å vise dem serienumrene eller antallet partinumre som for øyeblikket er tilordnet i andre åpne dokumenter. Dette reduserer usikkerhet som skyldes doble tildelinger og vekker tillit hos ordrebehandlere om at varesporingsnumrene og datoene de bekrefter på ikke-bokførte ordrer, kan oppfylles. Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Side for varesporingslinjer](design-details-item-tracking-lines-window.md).  

 Når du åpner siden **Varesporingslinjer**, hentes tilgjengelighetsdata fra **Varepost**-tabellen og **Reservasjonspost**-tabellen uten noe datofilter. Når du velger **Serienr.**-feltet eller **Partinr.**-feltet, åpnes siden **Varesporingssummering** med et sammendrag av varesporingsinformasjonen i **Reservasjonspost**-tabellen. Sammendraget inneholder følgende informasjon om hvert serie- eller partinummer på varesporingslinjen:  

|Felt|Beskrivelse|  
|---------------------------------|---------------------------------------|  
|**Antall i alt**|Det totale antallet for serie- eller partinummeret som for øyeblikket er på lager.|  
|**Ønsket antall i alt**|Det totale antallet for serie- eller partinummeret som for øyeblikket er forespurt i alle dokumenter.|  
|**Gjeldende antall i kø**|Antallet som registreres i gjeldende forekomst av siden **Varesporingslinjer**, men som ikke er lagret i databasen ennå.|  
|**Totalt disp. antall**|Antallet for serie- eller partinummeret som brukeren kan be om.<br /><br /> Dette antallet blir beregnet fra andre felt på siden, slik:<br /><br /> totalt antall – (ønsket antall i alt + gjeldende antall i kø).|  

> [!NOTE]  
>  Du kan også vise informasjonen i den foregående tabellen ved å bruke funksjonen **Velg poster** på siden **Varesporingslinjer**.  

 For å bevare databaseytelsen hentes tilgjengelighetsdata bare én gang fra databasen når du åpner siden **Varesporingslinjer** og når du bruker funksjonen **Oppdater tilgjengelighet** på siden.  

## <a name="calculation-formula"></a>Beregningsformel
 Tilgjengeligheten av et bestemt serie- eller partinummer beregnes på følgende måte, som beskrevet i den forrige tabellen.  

 totalt disponibelt antall = antallet på lager – (alle behov + antallet som ennå ikke er lagret i databasen)  

> [!IMPORTANT]  
>  Denne formelen innebærer at tilgjengelighetsberegningen for serie- eller partinumre bare tar hensyn til beholdning og ignorerer forventede mottak. Levering som ennå ikke er bokført på lager, påvirker derfor ikke varesporingstilgjengelighet, i motsetning til vanlig varedisposisjon der forventede mottak er inkludert.  

## <a name="see-also"></a>Se også
 [Designdetaljer: Varesporing](design-details-item-tracking.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
