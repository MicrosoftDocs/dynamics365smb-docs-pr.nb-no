---
title: Opprette XML-porter på XML-skjemaer | Microsoft-dokumentasjon
description: Bruk XML-skjemaer til å konfigurere rammeverket for dokumentutveksling.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: bac8d19bd48d9b7ad981c75dc54b155c8fe765a5
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2019
ms.locfileid: "1245053"
---
# <a name="use-xml-schemas-to-prepare-data-exchange-definitions"></a>Bruke XML-skjemaer til å klargjøre datautvekslingsdefinisjoner
Du kan gjøre det mulig å importere/eksportere data i XML-filer via rammeverket for datautveksling [!INCLUDE[d365fin](includes/d365fin_md.md)] ved å bruke XML-skjemaer til å definere hvilke dataelementer du vil utveksle med [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du kan gjøre dette på siden **Visningsprogram for XML-skjema** ved å laste inn XML-skjemafilen, velge de aktuelle dataelementene og deretter initialisere en datautvekslingsdefinisjon eller en XMLport.  

 Når du har angitt hvilke dataelementer som skal inkluderes basert på XML-skjemaet, kan du bruke handlingen **Generer XMLport** til å opprette XMLport-objektet.  

 Du kan eventuelt bruke handlingen **Generer datautvekslingsdefinisjon** for å initialisere en datautvekslingsdefinisjon basert på de valgte dataelementene, som du deretter fullfører i rammeverket for datautveksling. Dermed opprettes en post på siden **Definisjoner av bokføringsutveksling**, der du fortsetter ved å definere hvilke felt i [!INCLUDE[d365fin](includes/d365fin_md.md)] som elementene i filen skal tilordnes til. Hvis du vil ha mer informasjon, kan du se [Definere datautvekslingsdefinisjoner](across-how-to-set-up-data-exchange-definitions.md)  

 Dette emnet inneholder følgende fremgangsmåter:  

-   Slik laster du inn en XML-skjemafil:  

-   Slik velger eller fjerner du noder i et XML-skjema:  

-   Slik genererer du en datautvekslingsdefinisjon som er basert på et XML-skjema:  

-   Slik genererer du en XMLport for filen som er basert på et XML-skjema  

-   Slik importerer du en XMLport til Object Designer  

### <a name="to-load-an-xml-schema-file"></a>Slik laster du inn en XML-skjemafil:  

1.  Kontroller at den aktuelle XML-skjemafilen er tilgjengelig. Filtypen er XSD.  

2.  Skriv inn **XML-skjemaer** i **Søk**-boksen, og velg deretter den relaterte koblingen.  

3.  I fanen **Hjem** under **Ny** velger du **Ny**.  

4.  Fyll ut feltene som beskrevet i tabellen nedenfor.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Kode**|Angi en kode som identifiserer XML-skjemaet.|  
    |**Beskrivelse**|Angi en beskrivelse av XML-skjemaet.|  

     Feltet **Målnavneområde** angir eventuelle navneområder i XML-skjemafilen som er lastet inn for linjen.  

5.  Velg **Last inn skjema** under **Prosess** i fanebladet **Hjem**, og velg deretter XML-skjemafilen.  

     Når filen er lastet inn, fylles resten av feltene på linjen med informasjon fra filen, og det merkes av for **Skjemaet er lastet inn**.  

    > [!NOTE]  
    >  Treet i det innlastede XML-skjemaet er skjult som standard. Du utvider hver node ved å velge **+**-knappen på noden. Hvis du vil utvide alle noder, velger du **Utvid alle** på båndet.  

### <a name="to-select-or-clear-nodes-in-an-xml-schema"></a>Slik velger eller fjerner du noder i et XML-skjema:  

1.  Skriv inn **Visningsprogram for XML-skjema** i **Søk**-boksen, og velg deretter den relaterte koblingen.  

2.  Fyll ut feltene i hodet som beskrevet i tabellen nedenfor.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**XML-skjemakode**|Angi XML-skjemafilen du lastet inn i trinn 5 under "Slik laster du inn en XML-skjemafil".|  
    |**Ny XMLport nr.**|Angi nummeret på XMLport som opprettes fra dette XML-skjemaet når du velger handlingen **Generer XMLport**.|  

     Linjene er nå fylt med noder som representerer alle elementene i XML-skjemaet. Noder for elementer som er obligatoriske i henhold til XML-skjemaet blir valgt som standard.  

3.  På den første linjen i **Nodenavn**-kolonnen viser du **Dokument**-noden, og deretter viser du gradvis de underliggende nodene som du vil se gjennom.  

     Du kan også høyreklikke en node, og deretter velge **Vis alle**.  

4.  I kategorien **Hjem** i **Vis**-gruppen velger du én av følgende handlinger for å endre hvilke noder som skal vises.  

    |**Handling**|Beskrivelse|  
    |----------------|---------------------------------------|  
    |**Vis alle**|Alle noder vises.|  
    |**Skjul ikke-obligatorisk**|Det vises bare noder som representerer elementer som er nødvendig i henhold til XML-skjemaet. Disse nodene er vanligvis angitt med **1** i feltet **MinOccurs**.<br /><br /> Velg **Vis alle** for å reversere visningen.|  
    |**Skjul ikke-valgt**|Det vises bare noder der det er merket av for **Valgt**.<br /><br /> Velg **Vis alle** for å reversere visningen.|  

5.  I fanen **Hjem** under **Behandle** velger du **Rediger**.  

6.  I avmerkingsboksen **Valgt** angir du for hver node om du vil at elementet skal støttes i datautvekslingsdefinisjonen for den relaterte SEPA-bankfilen.  

    > [!NOTE]  
    >  Når du merker en obligatorisk underordnet node, merkes også alle overordnede noder ovenfor.  

7.  Velg handlingen **Merk alle obligatoriske elementer** for å merke på nytt alle noder som representerer elementer som er obligatoriske i henhold til XML-skjemaet.  

8.  Velg handlingen **Fjern all merking** for å fjerne all merking.  

     **Valg**-feltet angir at noden har to eller flere likestilte noder som fungerer som alternativer.  

### <a name="to-generate-a-data-exchange-definition-that-is-based-on-an-xml-schema"></a>Slik genererer du en datautvekslingsdefinisjon som er basert på et XML-skjema:  

1.  Skriv inn **XML-skjemaer** i **Søk**-boksen, og velg deretter den relaterte koblingen.  

2.  Velg det aktuelle XML-skjemaet, og velg deretter **Åpne XML-skjemavisning** under **Prosess** i fanebladet **Hjem**.  

3.  Kontroller at de aktuelle nodene er valgt. Hvis du vil ha mer informasjon, kan du se avsnittet "Slik velger eller fjerner du noder i et XML-skjema".  

4.  På siden **Visningsprogram for XML-skjema**, på **Hjem**-fanen, i **Prosess**-gruppen velger du **Generer datautvekslingsdefinisjon**.  

 En datautvekslingsdefinisjon opprettes på siden **Definisjoner av bokføringsutveksling**, som du kan fullføre ved å angi hvilke elementer som er tilordnet hvilke felt i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hvis du vil ha mer informasjon, kan du se [Definere datautvekslingsdefinisjoner](across-how-to-set-up-data-exchange-definitions.md)  

> [!NOTE]  
>  Du kan også bruke **Hent filstruktur**-funksjonen fra siden **Definisjoner av bokføringsutveksling**, som bruker funksjonaliteten på siden **Visningsprogram for XML-skjema** til å forhåndsutfylle hurtigfanen **Kolonnedefinisjoner**.  

### <a name="to-generate-an-xmlport-that-is-based-on-an-xml-schema"></a>Slik genererer du en XMLport som er basert på et XML-skjema  

1.  Skriv inn **XML-skjemaer** i **Søk**-boksen, og velg deretter den relaterte koblingen.  

2.  Velg det aktuelle XML-skjemaet, og velg deretter **Åpne XML-skjemavisning** under **Prosess** i fanebladet **Hjem**.  

3.  I feltet **Ny XMLport nr.** angir du nummeret som det nye XMLport-objektet blir gitt når det genereres.  

4.  Kontroller at de aktuelle nodene er valgt. Hvis du vil ha mer informasjon, kan du se avsnittet "Slik velger eller fjerner du noder i et XML-skjema".  

5.  I kategorien **Hjem** i **Prosess**-gruppen velger du **Generer XMLport**, og deretter lagrer du objektet som en TXT-fil på ønsket plassering.  

6. Importer den nye XMLport i [!INCLUDE[d365fin](includes/d365fin_md.md)]-utviklingsmiljøet, og kompiler den.

## <a name="see-also"></a>Se også  
[Definere datautvekslingsdefinisjoner](across-how-to-set-up-data-exchange-definitions.md)   
[Eksportere betalinger til en bankfil](payables-how-export-payments-bank-file.md)   
[Innkreve betalinger med SEPA direct debit](finance-collect-payments-with-sepa-direct-debit.md)   
[Rammeverket for datautveksling](across-about-the-data-exchange-framework.md)
