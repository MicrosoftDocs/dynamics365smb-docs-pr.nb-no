---
title: Bruke profiler til å klassifisere kontakter
description: Les om hvordan du definerer profilspørreskjemaer for å bidra til å klassifisere forretningskontaktenes profiler.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: contacts, profiles
ms.author: edupont
ms.date: 06/22/2021
ms.openlocfilehash: 42ef7c92d138d717f10eb98a7fa9208eaf73ef54
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2022
ms.locfileid: "8140868"
---
# <a name="use-profile-questionnaires-to-classify-business-contacts"></a>Bruke profilspørreskjemaer til å klassifisere forretningskontakter
Du kan definere profilspørreskjemaer du vil bruke når du angir opplysninger om profiler for kontaktene. Du kan definere de ulike spørsmålene du vil spørre kontaktene om, i hvert enkelt spørreskjema.  

Du kan også kjøre spørreskjemaet for å besvare noen av spørsmålene automatisk basert på data om kontakter, kunder eller leverandører.  

## <a name="to-add-a-profile-questionnaire"></a>Slik legger du til et profilspørreskjema:
1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Spørreskjemaoppsett**, og velg deretter den relaterte koblingen.  
2.  Velg handlingen **Ny**.  
3.  Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-add-questions-to-a-profile-questionnaire"></a>Slik legger du til spørsmål i et profilspørreskjema:
1.  Velg det aktuelle profilspørreskjemaet, og velg handlingen **Rediger spørreskjemaoppsett**.  
2.  På den første tomme linjen, i **Type**-feltet, velger du **Spørsmål** og skriver inn spørsmålet i **Beskrivelse**-feltet. Fyll ut de andre feltene på denne linjen.  
3.  På den neste tomme linjen, i **Type**-feltet, velger du **Svar** og skriver inn svaret i **Beskrivelse**-feltet.  
4.  Velg prioriteten i **Prioritet**-feltet. Definer et punktområde i feltene **Fra verdi** og **Til verdi**. Kontakter som får poeng innenfor det definerte intervallet, vil motta svaret.  

Gjenta disse trinnene hvis du vil angi alle spørsmål og svar i profilspørreskjemaene.

Når du har opprettet et spørreskjema, må du opprette kontaktrangeringer for å klassifisere kontaktene dine. Du kan også lage spørsmål som rangeres automatisk basert på informasjon på kontaktkortet.  

> [!NOTE]
> Hvis du angir et spørsmål som skal besvares automatisk, velger du <STRONG>Linje</STRONG>, og deretter velger du <STRONG>Spørsmålsopplysninger</STRONG> for å angi hvilke kriterier som skal brukes til å besvare spørsmålet.

## <a name="the-automatic-classification-of-contacts"></a>Automatisk klassifisering av kontakter
Du kan klassifisere kontaktene automatisk etter opplysninger om kunde, leverandør og kontakt. Det gjør du ved å definere automatisk besvarte profilspørsmål på siden **Profilspørreskjema - oppsett**.  

> [!NOTE]
> Det er bare kontakter som er registrert som kunder og leverandører, som kan tilordnes en klassifisering som er basert på henholdsvis kunde- og leverandørdata. Den automatiske klassifiseringen blir ikke automatisk oppdatert. Du bør derfor oppdatere profilspørreskjemaene etter at du har oppdatert kunde-, leverandør- eller kontaktdataene som skjemaene er basert på.  

Etter at du har definert automatisk besvaring av profilspørsmål, tilordner [!INCLUDE[prod_short](includes/prod_short.md)] automatisk riktige svar for en kontakt hvis du tilordner profilspørreskjemaet som inneholder disse spørsmålene, til kontakten.  

## <a name="example"></a>Eksempel

Du kan klassifisere kontakter etter hvor mye de handler:

|Svar|Gjelder|
|--- |--- |
|A|kontakter som kjøpte for LV 500 000 eller mer|
|B|kontakter som kjøpte for LV 100 000 til 499 999|
|U|kontakter som kjøpte for LV 99 999 eller mindre|

Du gjør dette ved å fylle ut siden **Profilspørreskjema - oppsett** slik:

| Type     | Beskrivelse        | Automatisk klassifisering     | Fra verdi | Til verdi |
|----------|--------------------|------------------------------|------------|----------|
| Spørsmål | ABC-klassifisering | Klikk for å sette en hake |            |          |
| Svar   | A                  |                              | 500,000    |          |
| Svar   | B                  |                              | 100,000    | 499,999  |
| Svar   | U                  |                              |            | 99,999   |

Fyll deretter ut siden **Profilspørsmålsopplysninger** på følgende måte:

| Felt                         | Verdi         |
|-------------------------------|---------------|
| Kundeklassifiseringsfelt | Salg (LV)   |
| Klassifiseringsmåte         | Definert verdi |

Når du tilordner profilspørreskjemaet som inneholder dette spørsmålet, til en kontakt, angir programmet automatisk riktig svar for denne kontakten på profillinjene på kontaktkortet.

## <a name="see-also"></a>Se også

[Opprette kontakter](marketing-create-contact-companies.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]