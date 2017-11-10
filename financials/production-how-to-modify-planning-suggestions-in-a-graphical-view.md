---
title: Endre planleggingsforslag i en grafisk visning | Microsoft-dokumentasjon
description: "En typisk planleggingsaktivitet er å endre eller legge til planleggingsforslagslinjer for å endre de foreslåtte forsyningsordrene før du utfører dem, ved å kjøre funksjonen **Utfør handlingsmelding**. Et alternativ til å gjøre dette i planleggingsforslaget er å bruke en grafisk visning."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 6cdd86fb96e89e99ea2378221d2991bd640f887e
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-modify-planning-suggestions-in-a-graphical-view"></a>Endre planleggingsforslag i en grafisk visning
En typisk planleggingsaktivitet er å endre eller legge til planleggingsforslagslinjer for å endre de foreslåtte forsyningsordrene før du utfører dem, ved å kjøre funksjonen **Utfør handlingsmelding**. Et alternativ til å gjøre dette i planleggingsforslaget er å bruke en grafisk visning.

I vinduet **Varetilgjengelighet per tidslinje** kan du endre visse forsyningsordrer og forslag ved å dra elementer på x-aksen for å endre antallet eller på y-aksen for å endre forfallsdatoen.  

 I vinduet **Varetilgjengelighet per tidslinje** og vinduet **Planleggingsforslag** kan du gjøre følgende endringer:  

-   Endre en foreslått forsyningsordre som bare eksisterer som en planleggingslinje.  
-   Endre en eksisterende forsyningsordre som planleggingssystemet foreslår å endre.  
-   Opprett en ny foreslått forsyningsordre, og endre den.  

Hvis du vil ha mer informasjon om planleggingslinjetypene som vises, kan du se feltet Beskrivelse på hurtigfanen **Hendelsesendringer**.  

Når du velger **Lagre endringer** i vinduet **Varetilgjengelighet per tidslinje**, kopieres endringene du har gjort til planleggings- eller bestillingsforslaget. Du kan nå velge å implementere dem ved hjelp av funksjonen **Utfør handlingsmeldingplanen**.  

Følgende fremgangsmåte viser hvordan du endrer forsyningsforslag ved hjelp av dra og slipp. Som et alternativ kan du endre feltene **Forfallsdato** og **Antall** på hurtigfanen **Hendelsesendringer** og umiddelbart se endringene grafisk på hurtigfanen **Tidslinje** i vinduet **Planleggingsforslag**.  

## <a name="to-modify-suggested-supply-orders-in-the-graphical-view"></a>Endre foreslåtte forsyningsordrer i den grafiske visningen  
1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Varetilgjengelighet per tidslinje**, og velg deretter den relaterte koblingen.  

    Vinduet **Varetilgjengelighet per tidslinje** åpnes med varenummeret, lokasjonen og varianten av varen på den valgte planleggingslinjen forhåndsutfylt på hurtigfanen **Alternativer**. Hurtigfanen **Tidslinje** viser en grafisk fremstilling av varens beregnede beholdning, inkludert planleggingsforslag.  

2.  Kontroller at feltet **Inluder planleggingsforslag** er valgt.  
3.  Finn den foreslåtte forsyningsordren du vil endre. Den grønne sirkelen og diskikonet identifiserer elementer som kan endres. Hvis du vil ha mer informasjon om ulike symboler, kan du se "Symboler og ikoner" på hurtigfanen Tidslinje.  
4.  Plasser pekeren over den grønne sirkelen til den forstørres og pekeren endres til Flytt figur (fire piler).  
5.  Trykk og hold museknappen nede mens du drar pekeren opp elle ned for å endre antallet. Trykk og hold museknappen nede mens du drar pekeren til venstre eller høyre for å endre forfallsdatoen.  
6.  I tillegg til å flytte elementer ved å dra og slippe kan du endre planleggingsforslag ved å bruke flere ulike funksjoner på rullegardinmenyen. Åpne rullegardinmenyen på den grønne sirkelen til en foreslått forsyning og velg én av følgende funksjoner  

    |Funksjon|Beskrivelse|  
    |--------------|---------------------------------------|  
    |**Opprett ny forsyning**|Oppretter et nytt elementpunkt der du åpner rullegardinmenyen, som representerer en ny foreslått forsyningsordre. Det blir en ny linje i planleggingsforslaget når du velger **Lagre endringer**.<br /><br /> **OBS!** Hvis feltene **Lokasjonsfilter** eller **Variantfilter** på hurtigfanen **Alternativer** er tomt eller har flere filterverdier, blir den nye forsyningen opprettet og senere lagret i planleggings- eller bestillingsforslaget med følgende koder:<br /><br /> * Hvis filterfeltet er tomt, opprettes den nye forsyningen uten en lokasjons- eller variantkode.<br /><br /> * Hvis flere filterverdier er definert, opprettes den nye forsyningen for første filterverdi i henhold til sorteringsmetoden.<br /><br /> Hvis du vil bruke en annen variant- eller lokasjonskode, må du endre den manuelt på den nye planleggingslinjen.|  
    |**Autojuster forsyning**|Optimaliserer en ny forsyning som du har opprettet i diagrammet ved å sørge for at den resulterer i nullager til neste forsyning.|  
    |**Slett forsyning**|Sletter elementet på hurtigfanen **tidslinje** og sletter planleggingslinjen når du velger **Lagre endringer**. Ikonet endres til en disk med et rødt kryss når forsyningen er slettet.<br /><br /> **OBS!** Du kan bare slette en forsyning med en handlingsmelding av typen **Ny**. Når du velger **Lagre endringer**, må du manuelt slette den aktuelle planleggingslinjen i planleggings- eller bestillingsforslaget.|  

7.  Velg handlingen **Last inn på nytt** hvis du vil tilbakestille alle endringene du har gjort siden du sist åpnet vinduet **Varetilgjengelighet per tidslinje** eller valgte **Last inn på nytt**.  
8. Når elementene er plassert der du vil ha dem i diagrammet, kan du velge **Lagre endringer** for å kopiere endrede antall og datoendringer til planleggings- eller forslagslinjer som representerer de grafiske elementene.  

Hvis du vil implementere forsyningsplanendringene, må du følge de resulterende handlingsmeldingene fra planleggings- eller bestillingsforslaget. Hvis du vil ha mer informasjon, se Utfør handlingsmeldingplaner..

## <a name="symbols-and-icons-on-the-timeline-fasttab"></a>Symboler og ikoner på hurtigfanen Tidslinje
 |Symbol/ikon|Beskrivelse|  
 |------------------|---------------------------------------|  
 |Svart kryss|Bestillinger (både forsyning og behov).<br /><br /> - Kan ikke endres.<br />-   Vises når feltet **Vis beregnet beholdning** er valgt (oransje graf).|  
 |Rød sirkel|Eksisterende forsyningsordrer som ikke finnes i planleggingsforslag.<br /><br /> - Kan ikke endres.<br />-   Vises når feltet **Vis beregnet beholdning** er valgt (oransje graf).|  
 |Gul stjerne|Prognosekrav.<br /><br /> - Kan ikke endres.<br />- Vises når **Prognosenavn**-feltet har en verdi.<br /><br /> Når det er merket av for både **Vis beregnet beholdning** og **Inkluder planleggingsforslag**, har hver gule stjerne et tilknyttet motstykke i diagrammet rett overfor. Dette illustrerer hvordan en foreslått forsyning oppfyller prognostisert behov.|  
 |Grønn sirkel med et ikon som er formet som en disk med et rødt kryss|Foreslått forsyningsordre med handlingsmeldingen *Avbryt*.<br /><br /> - Kan ikke endres.<br />-   Vises når feltet **Inkluder planleggingsforslag** er valgt (grønn graf).|  
 |Grønn sirkel med et ikon som er formet som en disk med en stjerne|Foreslåtte forsyningsordrer med handlingsmeldingen *Ny*.<br /><br /> - Kan endres.<br />-   Vises når feltet **Inkluder planleggingsforslag** er valgt (grønn graf).|  
 |Grønn sirkel med et ikon som er formet som en disk med én eller to piler|Foreslåtte forsyningsordrer med handlingsmeldingen *Tidsplanlegg på nytt*, *Endre ant.* eller *Tidsplanl. på nytt og endre ant.*<br /><br /> - Kan endres.<br />-   Vises når feltet **Inkluder planleggingsforslag** er valgt (grønn graf).<br /><br /> Pilene gjenspeiler retningen for planleggingsforslaget. En venstrepil sammen med en oppoverpil gjenspeiler for eksempel handlingsmeldingen *Tidsplanl. på nytt og endre ant.*, som består av en ny planlegging bakover og en økning i antall.|  

Når du åpner rullegardinmenyen for hurtigfanen **Tidslinje**, vises følgende funksjoner avhengig av hva du velger:  

 |Funksjon|Beskrivelse|  
 |--------------|---------------------------------------|  
 |**Opprett ny forsyning**|Oppretter et nytt element på punktet der du åpner rullegardinmenyen, som representerer en ny foreslått forsyningsordre. Det blir en ny linje i planleggingsforslaget når du velger **Lagre endringer** på fanebladet **Prosess**.<br /><br /> Alle filterverdier som er definert i feltene **Lokasjonsfilter** eller **Variantfilter** i hurtigfanen **Alternativer**, vil bli brukt i den nye forsyningsordren. **Obs!** Hvis filterfeltene er tomme eller har flere filterverdier, opprettes den nye forsyningsordren ved hjelp av følgende koder. <ul><li>Hvis filterfeltet er tomt, opprettes den nye forsyningen uten en lokasjons- eller variantkode.</li><li>Hvis flere filterverdier er definert, opprettes den nye forsyningen ved hjelp av første filterverdi i henhold til sorteringsrekkefølgen.</li></ul> Hvis du vil bruke en annen variant- eller lokasjonskode i den nye forsyningsordren, må du endre den manuelt på den nye planleggingslinjen.|  
 |**Autojuster forsyning**|Optimaliserer en ny forsyning som du har opprettet i diagrammet ved å sørge for at de ligger på nullager til neste forsyning.|  
 |**Slett forsyning**|Sletter elementet på hurtigfanen **Tidslinje** og sletter planleggingslinjen når du velger **Lagre endringer** i kategorien **Prosess**. Ikonet endres til en plate som har et rødt kryss når forsyningen er slettet. **Obs!** Du kan bare slette en forsyning med en handlingsmelding av typen *Ny*. Når du velger **Lagre endringer** i fanebladet **Prosess**, må du manuelt slette den aktuelle planleggingslinjen i planleggings- eller bestillingsforslaget.|  
 |**Vis dokument**|Åpner ordren, planleggingslinjen eller prognosen som elementet representerer.|  
 |**Zoom ut (Ctrl++)**|Gjør skalaen på x-aksen større, slik at færre dager vises. **Obs!** Du kan også gjøre dette ved å trykke Ctrl + rulle på musehjulet.|  
 |**Zoom inn (Ctrl+-)**|Gjør skalaen på x-aksen mindre, slik at flere dager vises. **Obs!** Du kan også gjøre dette ved å trykke Ctrl + rulle på musehjulet.|  
 |**Tilbakestill zoom (Ctrl+0)**|Tilbakestiller skalaen på x-aksen til den som ble brukt før du zoomet.|  

I tillegg til tastaturhandlingene som ble nevnt tidligere, kan du også bruke følgende tastaturhandlinger på hurtigfanen **Tidslinje**.  

 |Tastaturhandling|Beskrivelse|  
 |---------------------|---------------------------------------|  
 |CTRL+Rull hjulet på musen|Endrer skalaen på x-aksen.|  
 |Velg et element og trykk deretter SKIFT + PIL|Flytter elementet i pilens retning.|  
 |TAB|Flytter til neste element.|  
 |Skift+TAB|Flytter til forrige element.|  
 |Trykk på Esc mens du flytter et element.|Kansellerer flyttingen. **Obs!** Fungerer ikke hvis du har sluppet museknappen.|

## <a name="see-also"></a>Se også  
[Planlegging](production-planning.md)   
[Definere produksjon](production-configure-production-processes.md)  
[Produksjon](production-manage-manufacturing.md)    
[Lager](inventory-manage-inventory.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Designdetaljer: Forsyningsplanlegging](design-details-supply-planning.md)   
[Anbefalte fremgangsmåter for oppsett: Forsyningsplanlegging](setup-best-practices-supply-planning.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

