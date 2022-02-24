---
title: Definere gjentakelsesgrupper
description: I feltet Kode for gjentakelsesgruppe på Rammebestillinger-siden defineres datoformler som kan brukes både som mal og til å opprette salgsordrer basert på datointervaller.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 0e4ae2fec7636072d2b27f1ecac0d1057a19b938
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3181020"
---
# <a name="set-up-recurring-groups"></a>Opprette gjentakelsesgrupper
I feltet **Kode for gjentakelsesgruppe** på **Rammebestillinger**-siden defineres datoformler som kan brukes både som mal og til å opprette salgsordrer basert på datointervaller. Du må opprette gjentakelsesgrupper før du kan opprette gjentakelsesordrer.  

## <a name="to-set-up-recurring-groups"></a>Slik oppretter du gjentakelsesgrupper:  

1.  Velg ikonet ![Søk etter side eller rapport](../../media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Gjentakelsesgrupper**, og velg deretter den relaterte koblingen.  
2.  Velg handlingen **Ny**.  
3.  I hurtigfanen **Generelt** fyller du ut feltene som beskrevet i tabellen nedenfor.  

    |Felt|Description|  
    |---------------------------------|---------------------------------------|  
    |**Kode**|Skriv inn en kode for å identifisere gjentakelsesgruppen.|  
    |**Beskrivelse**|Skriv inn en beskrivelse for gjentakelsesgruppen.|  
    |**Datoformel**|Angi en datoformel for å beregne tidsintervallet mellom ordrene.|  
    |**Opprett bare den siste**|Velg dette alternativet hvis du vil at bare den siste gjentakelsesordren skal opprettes når gjentakelsesgruppeintervallet som er opprettet av **Datoformel**, er overskredet.<br /><br /> Hvis ordredatoen på rammeordren er overskredet med mer enn én intervallperiode, vil du ved å merke av for dette alternativet forhindre hvordan alle ordrer opprettes, bortsett fra den siste ordren.|  
    |**Startdato**|Angi den første datoen for gjentakelsesgruppen.|  
    |**Sluttdato**|Angi den siste datoen for gjentakelsesgruppen.|  

4.  I hurtigfanen **Oppdater** fyller du ut feltene som beskrevet i tabellen nedenfor.  

    |Felt|Description|  
    |---------------------------------|---------------------------------------|  
    |**Oppdater bilagsdato**|Velg ett av følgende alternativer for å oppdatere bilagsdatoen:<br /><br /> -   **Bokføringsdato** - bilagsdatoen beregnes på bakgrunn av bokføringsdatoen og datoformelen som er angitt i feltet **Bilagsdatoformel**.<br />-   **Behandlingsdato** - bilagsdatoen beregnes på bakgrunn av behandlingsdatoen og datoformelen som er angitt i feltet **Bilagsdatoformel**.|  
    |**Bilagsdatoformel**|Angi en datoformel for å beregne bilagsdatoen i ordren.|  
    |**Leveringsdatoformel**|Angi en datoformel for å beregne leveringsdatoen i ordren.|  
    |**Oppdater pris**|Velg ett av følgende alternativer for å oppdatere priser på nye ordrer:<br /><br /> -   **Fast** - prisen som benyttes i en ny ordre, er den samme som angis i rammeordren.<br />-   **Beregn på nytt** - prisen i en ny ordre beregnes på nytt for å gjenspeile gjeldende pris for kunden.<br />-   **Tilbakestill** - prisen i en ny ordre slettes for å angi en ny pris.|  
    |**Oppdater antall**|Velg ett av følgende alternativer for å håndtere antallet som er angitt i den opprinnelige ordren:<br /><br /> -   **Konstant** - antallet i rammeordren holder seg uendret. Dette gjør det mulig for deg å lage ordrer på ubestemt tid fra rammeordren.<br />-   **Reduser** - antallet som er angitt i den nye ordren, trekkes fra antallet i rammeordren. Behandlingen av gjentakelsesordren stanser når antallet som er angitt i rammeordren, blir brukt på nye ordrer.|  
    |**Tilbakestill levering**|Velg dette alternativet for å tilbakestille leveringsalternativene for gjentakelsesgruppen.|  

5.  Velg **OK**.  

## <a name="see-also"></a>Se også  
 [Gjentakelsesordrer](recurring-orders.md)   
 [Definere gjentakelsesordrer](how-to-set-up-recurring-orders.md)   
 [Opprett gjentakelsesordrer](how-to-create-recurring-orders.md)
