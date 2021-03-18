---
title: Definere betalingsbetingelser
description: Bruk betalingsbetingelser i basisversjonen av Business Central til å håndtere forfallsdatoer og kontantrabatter.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: ''
ms.date: 01/21/2021
ms.author: edupont
ms.openlocfilehash: dfed018a58897b5e51f90fcce725c9060c32f3ea
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5383403"
---
# <a name="set-up-payment-terms"></a>Definer betalingsbetingelser

Betalingsbetingelser bestemmer hvordan du håndterer forfallsdatoer og kontantrabatter. Du kan definere et ubegrenset antall betalingsbetingelseskoder, og bruke datoformler til å definere betalingsbetingelsene. Når du først registrerer deg for [!INCLUDE [prod_short](includes/prod_short.md)], gir demonstrasjonsselskapet noen betalingsmåter som virksomheter ofte bruker. Du kan imidlertid legge til så mange du trenger.  

Du kan knytte betalingsbetingelser til kunder og leverandører slik at de samme betingelsene alltid brukes på salgs- og kjøpsdokumenter du oppretter for dem. Om nødvendig kan du endre betingelsene på salgs- eller kjøpsdokumentet, for eksempel hvis du vil at en bestemt kunde skal betale deg innen 7 dager i stedet for standard 14 dager. Dette endrer ikke standard betalingsbetingelsen som er knyttet til kunden. Samme betalingsbetingelser er tilgjengelige for salgs- og kjøpsdokumenter.

Når du deretter bokfører en faktura, beregner [!INCLUDE [prod_short](includes/prod_short.md)] kontantrabatten på grunnlag av betalingsbetingelsene. Kontantrabattdatoen, altså den siste datoen kunden kan betale og få rabatt på betalingen, beregnes samtidig.  

Når du bokfører en kreditnota, beregner [!INCLUDE [prod_short](includes/prod_short.md)] mulige kontantrabatter på bakgrunn av betalingsbetingelsene. Rabatten på kreditnotaer beregnes etter de samme prinsippene som ved kontantrabatter på fakturaer. Der en kreditnota er utlignet mot en faktura, reduseres det mulige kontantrabattbeløpet for fakturaen med kontantrabattbeløpet for kreditnotaen.  

Hvis du vil sende kundene purringer om forfalte betalinger, må du definere purregrader og betingelser. Hvis du vil ha mer informasjon, kan du se [Definer betingelser og grader for purringer](finance-setup-reminders.md).  

## <a name="to-set-up-payment-terms"></a>Slik definerer du betalingsbetingelser

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Betalingsbetingelser**, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Når du har definert betalingsbetingelsene, tilordner du dem til kunder og leverandører. Du kan eventuelt tilordne betalingsbetingelser til betalingsmåtene.  

> [!TIP]
> I grunnversjonen av [!INCLUDE [prod_short](includes/prod_short.md)] støttes ikke betalingsbetingelser med delvise betalinger. Du må i stedet bruke funksjonene for forskuddsbetaling. Hvis du vil ha mer informasjon, kan du se [Definere forskudd](finance-set-up-prepayments.md).
>
> I visse land *kan* du definere betalingsbetingelser med delvise betalinger. Hvis du vil finne ut om denne funksjonen støttes i ditt land, kan du se delen **Lokale funksjoner** i navigasjonsruten til venstre på nettstedet [Docs.microsoft.com ](about-localization.md).

## <a name="see-also"></a>Se også

[Definer betalingsmåter](finance-payment-methods.md)  
[Definerer forskudd](finance-set-up-prepayments.md)  
[Konfigurere finans](finance-setup-finance.md)  
[Registrere nye kunder](sales-how-register-new-customers.md)  
[Registrere nye leverandører](purchasing-how-register-new-vendors.md)  
[Salg](sales-manage-sales.md)  
[Innkjøp](purchasing-manage-purchasing.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]