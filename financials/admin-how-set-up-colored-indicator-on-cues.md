---
title: "Angi fargede indikatorer for å tilpasse visuelle signaler om aktiviteten for et bunke-ikon for selskapet eller individuelle brukere | Microsoft-dokumentasjon"
description: "Som administrator kan du definere bunke-ikoner med en indikator som endrer farge basert på dataverdiene i bunke-ikonene. Du kan gjøre dette for bunke-ikoner som vises i rollesentrene for brukerne."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 17daf9dfa367907d10dd5101f1001ac2aaf7ea03
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-a-colored-indicator-on-cues-for-the-company-or-individual-users"></a>Definere en farget indikator for bunke-ikoner for selskapet eller enkeltbrukere
Som administrator kan du definere bunke-ikoner med en indikator som endrer farge basert på dataverdiene i bunke-ikonene. Du kan gjøre dette for bunke-ikoner som vises i rollesentrene for brukerne.  
  
Indikatoren vises som en farget linje langs øverste kant av bunkeflisen. Den gir et visuelt signal om statusen for aktiviteten for bunke-ikonet, som kan angi fordelaktige eller ufordelaktige tilstander som ber brukeren om å gjøre noe. Hvis det for eksempel vises pågående salgsfakturaer på et bunke-ikon, kan du angi at indikatoren skal være grønn (fordelaktig) når antall pågående salgsfakturaer er under 10, og at den skal være rød (ufordelaktig) når det totale antallet er over 20.  
  
Du bruker vinduet **Oppsett for bunke-ikon** til å definere indikatorer for alle bunke-ikonene som er tilgjengelige i selskapsdatabasen. Du kan definere indikatorene skal gjelde for alle brukere i firmaet eller en individuell bruker. Indikatorinnstillingene i vinduet **Oppsett for bunke-ikon** fungerer som standardinnstillingene for indikatoren. Hvis vinduet **Oppsett for bunke-ikon, sluttbruker** gjøres tilgjengelig for brukere, kan de tilpasse innstillingene for indikatorer du definerer i vinduet **Oppsett for bunke-ikon**.  
  
Hvis du vil definere indikatoren, kan du angi opptil to terskelverdier som definerer tre områder med dataverdier (lav, middels og høy) som du kan bruke en annen farge (eller stil) med.  
  
### <a name="to-set-up-colored-indicators-on-cues"></a>Slik definerer du fargede indikatorer for bunke-ikoner  
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Oppsett for bunke-ikon**, og velg deretter den relaterte koblingen.  
  
     Vinduet **Oppsett for bunke-ikon** vises. Vinduet viser indikatorer som er definert for bunker. Indikatorer som gjelder for alle brukere i firmaet, har et tomt **Brukernavn**-felt. Indikatorene som gjelder for en bestemt bruker, inkluderer brukernavnet i **Brukernavn**-feltet.  
  
    > [!NOTE]  
    >  Hvis du definerer en indikator for hele selskapet og en bruker endrer indikatoren senere, vises en egen oppføring for indikatoren i listen for denne brukeren.  
  
2. Velg handlingen **Rediger oversikt**.  
3. Hvis du vil definere en indikator for et bunke-ikon som ikke er oppført i vinduet, velger du **Ny**, og deretter fyller du ut feltene som beskrevet nedenfor. Hvis du vil endre en eksisterende indikator, går du til neste trinn.  
  
    |  Felt  |  Beskrivelse  |    
    |---------|---------------|  
    |**Brukernavn**|La dette feltet stå tomt hvis du vil definere indikatoren for alle brukerne.<br /><br /> Hvis du vil definere indikatoren for en bestemt bruker, angir du brukernavnet i dette feltet.|  
    |**Tabellnr.**|Angir IDen til tabellobjektet som inneholder bunke-ikonet. Bruk rullegardinlisten til å finne tabellen. Rullegardinlisten inneholder alle bunketabeller i firmadatabasen.<br /><br /> Feltet **Tabellnavn** vil automatisk fylles ut basert på valget ditt.|  
    |**Feltnr.**|Angir IDen for bunke-ikonet du vil definere en indikator på. Bruk rullegardinlisten til å finne bunke-ikonet du vil bruke. **Obs!**  Bunke-ID-en samsvarer med feltnummeret som er tilordnet til bunken i tabellen. <br /><br /> Feltet **Feltnavn** fylles ut automatisk basert på valget ditt.|  
  
4. Hvis du vil definere indikatoren for et bunke-ikon, angir du feltene som beskrevet i følgende tabell.  
  
    |  Felt  |  Beskrivelse  |    
    |---------|---------------|  
    |**LowStyle**|Angir fargen på indikatoren når bunke-ikonets verdi er lavere enn verdien i **Terskel 1**-feltet.|  
    |**LowThreshold**|Angir verdien som får indikatoren til å endre farge til den som er angitt i feltet **Stil for midterste område**, når den aktuelle verdien er lik eller overskrider denne verdien.|  
    |**MiddleStyle**|Angir fargen på indikatoren når bunke-ikonets verdi er større enn eller lik verdien i **Terskel 1**-feltet, men mindre enn eller lik verdien i **Terskel 2**-feltet.|  
    |**HighThreshold**|Angir verdien som får indikatoren til å endre farge til den som er angitt i feltet **Stil for øvre område**, når den aktuelle verdien overskrider denne verdien.|  
    |**HighStyle**|Angir fargen som skal brukes når bunke-ikonets verdi er større enn verdien i **Terskel 2**-feltet.|  
  
     Tabellen nedenfor viser fargene som tilsvarer alternativene i feltene **LowStyle**, **MiddleStyle** og **HighStyle**.  
  
    |  Alternativ  |  Farge  |  
    |----------|---------|  
    |**Ingen**|Ingen farge (samme farge som bunkeflisen)|  
    |**Fordelaktig**|Grønn|  
    |**Ufordelaktig**|Rød|  
    |**Tvetydig**|Gul|  
    |**Underordnet**|Grå|  
  
## <a name="see-also"></a>Se også  
[Definere en farget indikator for bunke-ikoner i arbeidsområdet](ui-how-setup-colored-indicator-cues.md)  
