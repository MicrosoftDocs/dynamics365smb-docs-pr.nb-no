---
title: "Arbeide med stykklister for å håndtere komponenter | Microsoft-dokumentasjon"
description: "Du oppretter en monteringsstykkliste for å angi komponentene eller ressursene som kreves for å sette sammen varen som monteringsstykklisten representerer, og du kan vise komponentene for en monteringsvare."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 05/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: e6aef60ee5b206b0ae978f72b92e6f8778290509
ms.contentlocale: nb-no
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-work-with-bills-of-material"></a>Arbeide med stykklister
> [!NOTE]  
>   Gjeldende versjon av [!INCLUDE[d365fin](includes/d365fin_md.md)] inneholder bare den første delen av funksjonen for monteringsstyring. Nå kan du opprette bare monteringsstykklister og håndtere de relaterte overordnede varene som vanlige varer. Du kan behandle den faktiske samlingen av varer fra komponenter, enten i montering til lager eller montering til ordreflyter i en fremtidig oppdatering, og du kan selge komponenter som sett.

Du kan bruke stykklister til å strukturere overordnede varer som selges som sett som består av komponenter for den overordnede varen, eller som du monterer til bestilling eller lager.

I [!INCLUDE[d365fin](includes/d365fin_md.md)] er en stykkliste referert til som en "monteringsstykkliste". Monteringsstykklister angir hvilke komponenter som inngår i overordnede varer. En overordnet vare blir referert til som en "monteringsvare" i denne dokumentasjonen.

Monteringsstykklister inneholder vanligvis varer, men kan også inneholde en eller flere ressurser som trengs for å sette monteringsvaren sammen.

Monteringsstykklister kan ha flere nivåer, noe som betyr at en komponent i monteringsstykklisten selv kan være en monteringsvare. I så fall skal **Monteringsstykkliste**-feltet på monteringsstykklistelinjen inneholde **Ja**.

Spesielle krav gjelder for varer i monteringsstykklister med hensyn til tilgjengelighet. Hvis du vil ha mer informasjon, kan du se delen «Vise tilgjengeligheten til en vare etter bruk i monteringsstykklister» i [Vise tilgjengeligheten av varer](inventory-how-availability-overview.md).

> [!NOTE]  
>   Denne funksjonen krever at opplevelsen er satt til **Løsning**. Hvis du vil ha mer informasjon, kan du se [Tilpasse Financials-opplevelsen](ui-experiences.md).

## <a name="to-create-an-assembly-bom"></a>Slik oppretter du en monteringsstykkliste:
Hvis du vil definere en overordnet vare som består av andre varer, og potensielt av ressursene som kreves for å sette sammen den overordnede varen, må du opprette en monteringsstykkliste.  

Oppretting av en monteringsstykkliste foregår i to trinn:
- Definere en ny vare
- Definere stykklistestrukturen for monteringsvaren.

1. Definer en ny vare. Hvis du vil ha mer informasjon, kan du se [Registrere nye varer](inventory-how-register-new-items.md).

    Fortsette med å registrere komponenter eller ressurser i monteringsstykklisten.  
2. I vinduet **Varekort** for en monteringsvare velger du **Montering** og velger deretter **Monteringsstykkliste**.
3. Fyll ut feltene etter behov i vinduet **Monteringsstykkliste**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-view-the-components-of-an-assembly-item-indented-according-to-the-bom-structure"></a>Vise komponentene i en monteringsvare som er rykket inn i henhold til stykklistestrukturen
Fra vinduet **Monteringsstykkliste** kan du åpne et eget vindu som viser komponentene og ressurser som er rykket inn, i henhold til deres stykklisteposisjon under monteringsvaren.

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Varer**, og velg deretter den relaterte koblingen.
2. Åpne kortet for en monteringsvare. (Feltet **Monteringsstykkliste** i vinduet **Varer** inneholder **Ja**.)
3. I vinduet **Varekort** velger du **Montering** og velger deretter **Monteringsstykkliste**.
4. I vinduet **Monteringsstykkliste** velger du handlingen **Vis stykkliste**.

## <a name="to-buy-sell-or-transfer-assembly-items"></a>Kjøpe, selge eller overføre monteringsvarer
Fordi den gjeldende versjonen av [!INCLUDE[d365fin](includes/d365fin_md.md)] bare inneholder muligheten til å definere og tilordne monteringsstykklister til varer, kan du bare håndtere monteringsvarer på dokumentlinjene som vanlige varer.

**Forsiktig**: Lagerantallet av stykklistekomponenter vil ikke bli justert hvis du gjør dette.

## <a name="see-also"></a>Se også
[Registrere nye varer](inventory-how-register-new-items.md)  
[Vise tilgjengeligheten av varer](inventory-how-availability-overview.md)     
[Lager](inventory-manage-inventory.md)  
[Arbeide med [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)

