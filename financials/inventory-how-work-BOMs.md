---
title: Arbeide med stykklister| Microsoft-dokumentasjon
description: "Monteringsstykklister angir hvilke komponenter eller ressurser som er nødvendige for å montere varen som monteringsstykklisten representerer. Monteringsstykklister inneholder vanligvis varer, men kan også inneholde en eller flere ressurser som utfører monteringsarbeidet."
services: project-madeira
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
ms.sourcegitcommit: ce75a9d292e12c58efc51c4db2fbc5a37b7553c7
ms.openlocfilehash: f55dcf4b391ae42ab46a22b729597a96645d9b71
ms.contentlocale: nb-no
ms.lasthandoff: 05/05/2017


---
# <a name="how-to-work-with-bills-of-materials"></a>Arbeide med stykklister
**Merk**: Gjeldende versjon av [!INCLUDE[d365fin](includes/d365fin_md.md)] inneholder bare den første delen av funksjonen for behandling av samlingen. Nå kan du opprette bare monteringsstykklister og håndtere de relaterte overordnede varene som vanlige varer. Du kan behandle den faktiske samlingen av varer fra komponenter, enten i montering til lager eller montering til ordreflyter i en fremtidig oppdatering, og du kan selge komponenter som sett.

Du kan bruke stykklister til å strukturere overordnede varer som selges som sett som består av komponenter for den overordnede varen, eller som du monterer til bestilling eller lager.

I [!INCLUDE[d365fin](includes/d365fin_md.md)] er en stykkliste referert til som en "monteringsstykkliste". Monteringsstykklister angir hvilke komponenter som inngår i overordnede varer. En overordnet vare blir referert til som en "monteringsvare" i denne dokumentasjonen.

Monteringsstykklister inneholder vanligvis varer, men kan også inneholde en eller flere ressurser som trengs for å sette monteringsvaren sammen.

Monteringsstykklister kan ha flere nivåer, noe som betyr at en komponent i monteringsstykklisten selv kan være en monteringsvare. I så fall skal **Monteringsstykkliste**-feltet på monteringsstykklistelinjen inneholde **Ja**.

Spesielle krav gjelder for varer i monteringsstykklister med hensyn til tilgjengelighet. Hvis du vil ha mer informasjon, se delen "Vise tilgjengeligheten til en vare etter bruk i monteringsstykklister" i [Få en oversikt over tilgjengelighet](inventory-how-availability-overview.md).

**Merk**: Denne funksjonen krever at opplevelsen er satt til **Løsning**. Hvis du vil ha mer informasjon, se [Tilpasse Financials-opplevelsen](ui-experiences.md).

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

1. I øvre høyre hjørne, velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Varer**, og deretter velger du den beslektede koblingen.
2. Åpne kortet for en monteringsvare. (Feltet **Monteringsstykkliste** i vinduet **Varer** inneholder **Ja**.)
3. I vinduet **Varekort** velger du **Montering** og velger deretter **Monteringsstykkliste**.
4. I vinduet **Monteringsstykkliste** velger du handlingen **Vis stykkliste**.

## <a name="to-buy-sell-or-transfer-assembly-items"></a>Kjøpe, selge eller overføre monteringsvarer
Fordi den gjeldende versjonen av [!INCLUDE[d365fin](includes/d365fin_md.md)] bare inneholder muligheten til å definere og tilordne monteringsstykklister til varer, kan du bare håndtere monteringsvarer på dokumentlinjene som vanlige varer.

**Forsiktig**: Lagerantallet av stykklistekomponenter vil ikke bli justert hvis du gjør dette.

## <a name="see-also"></a>Se også
[Registrere nye varer](inventory-how-register-new-items.md)  
[Få en oversikt over tilgjengelighet](inventory-how-availability-overview.md)     
[Lager](inventory-manage-inventory.md)  
[Arbeide med [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)

