---
title: VIA-metoder for å beregne og registrere prosjektfremdrift
description: 'Beskriver de forskjellige VIA-metodene (varer i arbeid) du kan bruke til å bokføre, overvåke og beregne økonomiske opplysninger for prosjekter som pågår.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'work in process, work in progress, calculate project WIP'
ms.search.form: 1010
ms.date: 04/01/2021
ms.author: bholtorf
---
# Forstå VIA-metoder i prosjektstyring

Under fremdriften av et prosjekt forbrukes materialer, ressurser og andre utgifter som må bokføres til prosjektet. Med funksjonen Varer i arbeid (VIA) kan du beregne den økonomiske verdien av prosjekter i Finans mens prosjektene pågår. I mange tilfeller vil du kanskje bokføre utgifter for et prosjekt før du fakturerer et prosjekt. Når bare utgifter er bokført, vil årsregnskapet bli unøyaktig.

Hvis du vil spore verdien i Finans, kan du beregne VIA og bokføre verdien i Finans. Hvis du vil ha mer informasjon, se [Overvåke prosjektfremdrift og -ytelse](projects-how-monitor-progress-performance.md).

[!INCLUDE[prod_short](includes/prod_short.md)] støtter følgende måter å beregne og registrere verdien av varer i arbeid på.

| VIA-metode | Beregningsformel | Beskrivelse av beregning |
| --- | --- | --- |
| Kostverdi |Ført inntekt = fakturerbar fakturert pris <br /><br />Budsjett (kostforhold) = budsjett (kostbeløp) / budsjett (salgsbeløp) <br /><br />Anslått kostbeløp = fakturerbart (salgsbeløp) x budsjett (kostforhold) <br /><br />Løpende = forbruk (kostbeløp) / budsjett (kostbeløp) <br /><br />Fakturert % = fakturerbar (fakturert pris) / fakturerbar (salgsbeløp) <br /><br />VIA-kost = (løpende – fakturert %) x anslått kostbeløp <br /><br />Ført kost = forbruk (kostbeløp) – VIA-kost|Kostverdiberegninger starter med å beregne verdien av det som er oppgitt, ved å ta en andel av anslått kostbeløp basert på prosent fullført. Fakturert kost trekkes fra ved å ta en andel av anslått kostbeløp basert på fakturert prosent.<br /><br />Denne beregningen krever at det fakturerbare salgsbeløpet, budsjettsalgsbeløpet og budsjettkostbeløpet angis riktig for hele prosjektet. |
| Kostnad for salg |Ført inntekt = fakturerbar fakturert pris<br /><br /> Ført kost = budsjett (kostbeløp) x fakturert prosent<br /><br /> Fakturert % = fakturerbar (fakturert pris) / fakturerbar (salgsbeløp)<br /> (Fakturert % finnes som en kolonne på prosjektoppgavelinjer)<br /><br /> VIA-kost = forbruk (kostbeløp) - ført kost |Beregning av solgte varers innkjøps- eller produksjonspris begynner ved å beregne ført kost. Kost føres proporsjonalt basert på budsjettkostbeløp.<br /><br /> Denne beregningen krever at det fakturerbare salgsbeløpet og budsjettkostbeløpet angis riktig for hele prosjektet. |
| Salgsverdi |Ført kost = forbruk (kostbeløp)<br /><br /> Ført inntekt = forbruk (salgsbeløp) x forventet faktureringsforhold<br /><br /> Kostgjenopprettingsprosent = fakturerbar (salgsbeløp) / budsjett (salgsbeløp)<br /><br /> VIA-salg = ført salg - fakturerbar (fakturert pris) |Salgsverdiberegninger fører inntekt proporsjonalt basert på forbruk (kostbeløp) og forventet kostgjenopprettingsforhold.<br /><br /> Denne beregningen krever at det fakturerbare salgsbeløpet og budsjettsalgsbeløpet angis riktig for hele prosjektet. |
| Løpende |Ført kost = forbruk (kostbeløp)<br /><br /> Ført inntekt = fakturerbar (salgsbeløp) x løpende<br /><br /> Løpende = forbruk (kostbeløp) / budsjett (kostbeløp)<br /> (Registrert i feltet **Ferdiggjørelsesprosent for kost** på prosjektoppgavelinjer)<br /><br /> VIA-salg = ført salg - fakturerbar (fakturert pris) |Beregninger av Løpende fører inntekt proporsjonalt basert på prosent fullført, det vil si forbruk (kostbeløp) i forhold til budsjettkost.<br /><br /> Denne beregningen krever at det fakturerbare salgsbeløpet og budsjettkostbeløpet angis riktig for hele prosjektet. |
| Ved avslutning |VIA-beløp = VIA-kostbeløp = Forbruk (kostbeløp)<br /><br /> VIA-salgsbeløp = fakturerbar (fakturert pris) |Ved avslutning fører ikke inntekt og kost før prosjektet er ferdig. Det kan hende du ønsker å gjøre dette når det er stor usikkerhet rundt overslagene for kost og inntekt for prosjektet.<br /><br /> Alt forbruk bokføres i VIA-forbrukskontoen (aktiva), og alt fakturert salg bokføres i VIA-kontoen for fakturert salg (gjeld) til prosjektet er ferdig. |

## Se relatert [Microsoft-opplæring](/training/paths/calculate-post-job-wip/)

## Se også

[Prosjektstyring](projects-manage-projects.md)  
[Finans](finance.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Salg](sales-manage-sales.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
