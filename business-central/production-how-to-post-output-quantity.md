---
title: Massebokføre produksjonsavgang og operasjonstider
description: Avgangsantallet representerer arbeidsfremdriften i form av ferdig antall og brukt kapasitet for arbeidssenter eller produksjonsressurs.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '99000773, 99000778, 99000823, 99000827'
ms.date: 03/08/2023
ms.author: edupont
---
# <a name="batch-post-output-and-run-times"></a><a name="batch-post-output-and-run-times"></a>Bokføre avgang og operasjonstid

Avgangsantallet representerer arbeidsfremdriften i form av ferdig antall og brukt kapasitet for arbeidssenter eller produksjonsressurs.

Du kan bruke ferdigmeldingskladden til å:

* Justere lagerbeholdningen i forbindelse med avgang av ferdige varer fra produksjonen.
* Registrere antall og vrak for hver operasjon i produksjonsrutingen.
* Registrere oppsett og kjøretid for arbeidssentre og produksjonsressurser.

> [!NOTE]
> Hvis produksjonsruting brukes, oppdateres lageret bare når du bokfører avgangsantall i den siste operasjonen.

Med siden **Produksjonskladd** kan du gjøre de samme oppgavene som på siden **Ferdigmeldingskladd**, og også utføre forbruksbokføringsoppgaver. Hvis du vil ha mer informasjon, kan du se [Registrere forbruk og avgang for én frigitt produksjonsordrelinje](production-how-to-register-consumption-and-output.md).

## <a name="to-post-output-quantities-andor-register-run-times-for-one-or-more-production-order-lines"></a><a name="to-post-output-quantities-andor-register-run-times-for-one-or-more-production-order-lines"></a>Slik bokfører du avgangsantall og/eller registrerer kjøretider for en eller flere produksjonsordrelinjer

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Ferdigmeldingskladd** og velg den relaterte koblingen.  
2. Fyll ut feltene med produksjonsordre- og avgangsdata og/eller kjøretid. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
  
    Du kan bruke funksjonen **Utfold rute** til å generere kladdelinjer fra produksjonsordrer.
  
3. Hvis operasjonen er fullført, velger du **Ferdig**-feltet.  
4. Velg handlingen **Bokfør** for å bokføre operasjonene.

    Kapasitetsposter oppdateres for det brukte arbeidssenteret eller produksjonsressursene med informasjon om tid og antall av avgang og vrak. Hvis du bokførte den siste operasjonen, blir varen lagt til i lageret.

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## <a name="see-also"></a><a name="see-also"></a>Se også

[Bokføre vrak manuelt](production-how-to-post-scrap.md)
[Tilbakeføre utgående bokføring](production-how-to-reverse-output-posting.md)
[Produksjon](production-manage-manufacturing.md)
[Definer produksjon](production-configure-production-processes.md)  
[Planlegging](production-planning.md)  
[Lager](inventory-manage-inventory.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
