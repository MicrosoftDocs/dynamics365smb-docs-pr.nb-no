---
title: Bruke profiler til å klassifisere kontakter
description: Konfigurere profilspørreskjemaer til å klassifisere forretningskontaktene
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: contacts, profiles
ms.author: edupont
ms.date: 04/01/2020
ms.openlocfilehash: 9cf4817cd85951f193ffadbcd3e7ebc971bcca36
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3181583"
---
# <a name="use-profile-questionnaires-to-classify-business-contacts"></a>Bruke profilspørreskjemaer til å klassifisere forretningskontakter
Du kan definere profilspørreskjemaer du vil bruke når du angir opplysninger om profiler for kontaktene. Du kan definere de ulike spørsmålene du vil spørre kontaktene om, i hvert enkelt spørreskjema.  

Du kan også kjøre spørreskjemaet for å besvare noen av spørsmålene automatisk basert på data om kontakter, kunder eller leverandører.  

## <a name="to-add-a-profile-questionnaire"></a>Slik legger du til et profilspørreskjema:
1.  Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Spørreskjemaoppsett**, og velg deretter den relaterte koblingen.  
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

Etter at du har definert automatisk besvaring av profilspørsmål, tilordner [!INCLUDE[d365fin](includes/d365fin_md.md)] automatisk riktige svar for en kontakt hvis du tilordner profilspørreskjemaet som inneholder disse spørsmålene, til kontakten.  

## <a name="example"></a>Eksempel
Du kan klassifisere kontakter etter hvor mye de handler:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Svar</strong></th>
<th><strong>Gjelder</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>A</p></td>
<td><p>kontakter som kjøpte for NOK 500 000 eller mer</p></td>
</tr>
<tr class="even">
<td><p>B</p></td>
<td><p>kontakter som kjøpte for NOK 100 000 til 499 999</p></td>
</tr>
<tr class="odd">
<td><p>U</p></td>
<td><p>kontakter som kjøpte for NOK 99 999 eller mindre</p></td>
</tr>
</tbody>
</table>

Du gjør dette ved å fylle ut siden **Profilspørreskjema - oppsett** slik:


<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Type</strong></th>
<th><strong>Beskrivelse</strong></th>
<th><strong>Automatisk klassifisering</strong></th>
<th><strong>Fra verdi</strong></th>
<th><strong>Til verdi</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Spørsmål</p></td>
<td><p>ABC-klassifisering</p></td>
<td><p>Klikk for å sette en hake</p></td>
<td><p> </p></td>
<td><p> </p></td>
</tr>
<tr class="even">
<td><p>Svar</p></td>
<td><p>A</p></td>
<td><p> </p></td>
<td><p>500,000</p></td>
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p>Svar</p></td>
<td><p>B</p></td>
<td><p> </p></td>
<td><p>100,000</p></td>
<td><p>499,999</p></td>
</tr>
<tr class="even">
<td><p>Svar</p></td>
<td><p>U</p></td>
<td><p> </p></td>
<td><p> </p></td>
<td><p>99,999</p></td>
</tr>
</tbody>
</table>

Fyll deretter ut siden **Profilspørsmålsopplysninger** på følgende måte:
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Felt</strong></th>
<th><strong>Verdi</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Kundeklassifiseringsfelt</strong></td>
<td><emphasis>Salg (NOK)</emphasis></td>
</tr>
<tr>
<td><strong>Klassifiseringsmåte</strong></td>
<td><emphasis>Definert verdi</emphasis></td>
</tr>
</tbody>
</table>

Når du tilordner profilspørreskjemaet som inneholder dette spørsmålet, til en kontakt, angir programmet automatisk riktig svar for denne kontakten på profillinjene på kontaktkortet.

## <a name="see-also"></a>Se også
[Opprette kontakter](marketing-create-contact-companies.md)  
