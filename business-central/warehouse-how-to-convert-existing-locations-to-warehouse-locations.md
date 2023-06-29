---
title: Konvertere eksisterende lokasjoner til lagerlokasjoner
description: 'Du kan definere at en eksisterende lokasjon skal bruke soner og hyller, og at den skal fungere som en lagerlokasjon.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: 15
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="convert-existing-locations-to-warehouse-locations"></a><a name="convert-existing-locations-to-warehouse-locations"></a>Konvertere eksisterende lokasjoner til lagerlokasjoner
Du kan definere at en eksisterende lokasjon skal bruke soner og hyller, og at den skal fungere som en lagerlokasjon.  

Kjørselen for å aktivere en lokasjon for lageroperasjoner oppretter startlagerposter for lagerjusteringshyllen for alle varer som har lager på lokasjonen. Disse startpostene balanseres når vareopptellingsposter for lageret registreres etter at kjørselen er utført.  

Du kan opprette soner og hyller før eller etter konverteringen. Den eneste hyllen du må opprette før konverteringen, er hyllen som skal brukes som fremtidig justeringshylle.  

> [!IMPORTANT]  
>  Når du skal tømme all negativ beholdning og eventuelle åpne lagerdokumenter før du konverterer lokasjonen for lagerhåndtering, kjører du en rapport for å identifisere varene med negativ beholdning og åpne lagerdokumenter for lokasjonen. Du finner mer informasjon under Kontroll for negativ beholdning.  

## <a name="to-enable-an-existing-location-to-operate-as-a-warehouse-location"></a><a name="to-enable-an-existing-location-to-operate-as-a-warehouse-location"></a>Slik definerer du en eksisterende lokasjon som lagerlokasjon
1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Opprett lagerlokasjon** og velg den relaterte koblingen.  
2.  Angi lokasjonen du vil aktivere for lagerbehandling, i **Lokasjonskode**-feltet.  
3.  Angi hyllen i lokasjonen der usynkroniserte lagerposter lagres, i feltet **Hyllekode for justering**. Hvis du vil ha mer informasjon, kan du se [Slik synkroniserer du de justerte lagerpostene med de tilhørende varepostene](inventory-how-count-adjust-reclassify.md#to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries).  

    Når du bruker åpne vareposter for den angitte lokasjonen, opprettes det lagerkladdelinjer som summerer alle kombinasjoner av Varenr, Variantkode, Enhetskode og om nødvendig Partinr. og Serienr, i varepostene. Lagerkladdelinjene blir deretter bokført. Under bokføringen opprettes det lagerposter som plasserer lageret i lagerjusteringshyllen. **Hyllekode for justering** på lokasjonskortet angis også.  

4.  Hvis du vil se hvilke varer som ble lagt til i justeringshyllen under kjørselen, kan du kjøre rapporten **Lagerjustering - hylle**.  
5.  Når den satsvise jobben **Opprett lagerlokasjon** er fullført, må du utføre og bokføre en vareopptelling for lageret. Hvis du vil ha mer informasjon, se [Telle, justere og reklassifisere lagerbeholdning ved hjelp av kladder](inventory-how-count-adjust-reclassify.md)  

> [!NOTE]  
>  Det anbefales at du utfører kjørselen **Opprett lagerlokasjon** når den ikke påvirker den daglige driften i systemet. Kjørselen behandler hver post i tabellen **Varepost**, og hvis det finnes et stort antall vareposter, kan det hende jobben tar flere timer.  

 Du må åpne på nytt og frigi eventuelle kildedokumenter som ble delvis mottatt eller delvis levert før konverteringen, for lokasjonene som ikke brukte lagerstyringsdokumenter før konverteringen.  

## <a name="see-also"></a><a name="see-also"></a>Se også
[Oversikt over lagerstyring](design-details-warehouse-management.md)
[Lager](inventory-manage-inventory.md)  
[Definer lagerstyring](warehouse-setup-warehouse.md)     
[Monteringsstyring](assembly-assemble-items.md)    
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
