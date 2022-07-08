---
title: Selge varer som er montert til ordre
description: Hvis varen er definert for Monter til ordre, forventes varen ikke å være på lager, og den må monteres spesifikt for en ordre.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting, substitute items
ms.search.form: 900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905
ms.date: 07/29/2021
ms.author: edupont
ms.openlocfilehash: b66efde55918886132def51ad898fa9e89054c02
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/29/2022
ms.locfileid: "9077348"
---
# <a name="sell-items-assembled-to-order"></a>Selge varer som er montert til ordre

Hvis **Monteringsprinsipp**-feltet på varekortet for en monteringsvare er **Monter til ordre**, forventes varen ikke å være på lager, og den må monteres spesifikt for en ordre. Når du angir varen på en ordrelinje, blir en monteringsordre automatisk opprettet og koblet til ordren.  

> [!NOTE]  
>  Hvis noen montere-til-ordre-varer allerede er på lager, kan du trekke dette antallet fra monteringsordren og reservere det fra beholdningen. Hvis du vil ha mer informasjon, kan du se [Selge lagervarer i montere-til-ordre-flyter](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).  

I denne fremgangsmåten behandler du salget av en vare som skal monteres i henhold til spesifikasjonene kunden har bedt om. Trinnene inkluderer start av ordrelinjen, tilpasning av monteringsvaren ved å redigere tilhørende komponenter og ressurser, kontroll av tilgjengeligheten for å fastsette en leveringsdato og frigivelse av ordren for montering og umiddelbar levering.  

> [!NOTE]  
>  Følgende fremgangsmåte omfatter ikke standardtrinnene for ordrer før trinnet der du angir montere-til-ordre-varen på en ordrelinje.  

## <a name="to-sell-an-item-that-is-assembled-to-order"></a>Selge en vare som er montert til ordre

1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Ordrer**, og velg deretter den relaterte koblingen.  
2.  Opprett en ordre. Hvis du vil ha mer informasjon, kan du se [Selge produkter](sales-how-sell-products.md).  
3.  I feltet **Nr.** -feltet angir du en vare som er definert for å monteres til ordre.  
4.  Definer hvilken lokasjon varen skal selges fra, i **Lokasjonskode**-feltet. Monteringsprosessen vil skje på den lokasjonen.  
5.  Angi hvor mange enheter som skal selges, i **Antall**-feltet.  

    > [!NOTE]  
    >  Hvis én eller flere komponenter i det forespurte monteringsvareantallet ikke er tilgjengelige, åpnes en side med et tilgjengelighetsadvarsel. Hvis du vil ha mer informasjon, se Montering – tilgjengelighet.  

    En montersordre opprettes nå automatisk og kobles til ordrelinjen. Forfallsdatoen for denne monteringsordren synkroniseres med forsendelsesdatoen på ordrelinjen.  

    Antallet som skal selges, kopieres til feltet **Ant. å montere til ordre**, som angir at vareoppsettet forventer at hele antallet på salgslinjen skal monteres til ordren. Du kan redusere antallet for montere til ordre, for eksempel hvis du vet at enkelte varer allerede er tilgjengelige. Hvis du vil ha mer informasjon, kan du se [Selge lagervarer i montere-til-ordre-flyter](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  

6.  For å gjenspeile at kunden ønsker en ekstra vare i et sett, går du til hurtigfanen **Linjer**, velger **Linje**, velger **Monter til ordre** og velger deretter **Montere til ordre-linjer** for å vise og endre standard monteringskomponenter. Du kan også merke feltet **Ant. som skal monteres til ordre**.  
7.  Opprett en ny linje av typen **Vare** for det forespurte tilleggsinnholdet i settet på siden **Montere til ordre – linjer**. Linjen representerer en ekstra monteringskomponent.  

    Du kan også tilpasse rekkefølgen ved å øke antallet for én standardvare i settet. Du kan gjøre dette ved å øke verdien i **Antall per**-feltet på den bestemte monteringsordrelinjen.  

    > [!NOTE]  
    >  Siden **Monteringsordrelinjene** inneholder de grunnleggende feltene som en selger forventes å bruke for å tilpasse komponentlisten, legge til varesporingsnumre eller løse problemer med komponenttilgjengelighet. Hvis du vil vise mer informasjon om monteringsordren, for eksempel startdatoen for den, velger du **Vis dokumenter**-handlingen. Dette åpner en full visning av monteringsordren som er knyttet til ordrelinjen. Du kan ikke endre innholdet i de fleste av feltene i monteringsordrehodet, og du kan ikke bokføre monteringsavgang herfra fordi du må bruke leveringsbokføring for ordrelinjen.  
    >   
    >  I hodet til koblede monteringsordrer der det bare **Startdato**-feltet som kan endres for at monteringsarbeidere kan angi en tidligere dato enn forfallsdatoen når de vil starte prosessen. Alle feltene på linjene i den tilknyttede monteringsordren kan endres slik at lagermedarbeidere kan angi forbruksverdier under prosessen.  

8.  Se gjennom eller reager på problemer med komponententilgjengelighet Velg for eksempel en tilgjengelig erstatningsvare.  
9. Lukk siden **Montere til ordre – linjer**. Den koblede monteringsordren er nå klar til å begynne å montere de tilpassede elementene etter forfallsdatoen.  
10. På ordren velger du **Frigi** for å varsle monteringsavdelingen om at monteringsprosessen kan starte.  
11. Utfør trinnene for montering av varer som selges i denne fremgangsmåten, i monteringsavdelingen. Hvis du vil ha mer informasjon, kan du se [Montere varer](assembly-how-to-assemble-items.md).  

> [!NOTE]  
> Vær oppmerksom på at vareerstatninger ikke automatisk fører til at en vare erstattes av en annen vare, for eksempel når du oppretter en ordre eller i en stykkliste. I stedet blir du varslet om at en erstatning er tilgjengelig for deg.

## <a name="see-related-training-at-microsoft-learn"></a>Se relatert opplæring på [Microsoft Learn](/learn/modules/assemble-to-order-dynamics-365-business-central/)

## <a name="see-also"></a>Se også

[Monteringsstyring](assembly-assemble-items.md)  
[Arbeid med stykklister](inventory-how-work-BOMs.md)  
[Lager](inventory-manage-inventory.md)  
[Designdetaljer: Warehouse Management](design-details-warehouse-management.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Registrere nye varer](inventory-how-register-new-items.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
