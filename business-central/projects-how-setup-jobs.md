---
title: Konfigurere prosjekter, priser og prosjektbokføringsgrupper
description: Beskriver hvordan du definerer generell prosjektinformasjon og definerer priser for prosjektvarer, ressurser og finanskonti og prosjektbokføringsgrupper.
author: edupont04
ms.topic: conceptual
ms.workload: na
ms.search.keywords: project management
ms.search.form: 211, 463, 1012
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: d4880f91c53e8618db9be5e0bcdbfa396cbf21fd
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2022
ms.locfileid: "8137448"
---
# <a name="set-up-jobs-prices-and-job-posting-groups"></a>Konfigurere prosjekter, priser og prosjektbokføringsgrupper

Som prosjektleder kan du sette opp prosjekter som definerer alle prosjekter du administrerer i [!INCLUDE[prod_short](includes/prod_short.md)]. På siden **Prosjektoppsett** må du angi hvordan du vil bruke bestemte prosjektfunksjoner.

For hver jobb angir du deretter individuelle jobbkort med informasjon om priser for prosjektvarer, prosjektressurser og finanskonti, og må du definere prosjektbokføringsgrupper.

## <a name="to-set-general-information-for-jobs"></a>Slik angir du generell informasjon for prosjekter
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Prosjektoppsett** og velg den relaterte koblingen.
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> Feltet **Bruk forbrukskobling som standard** angir om prosjektposter er koblet til prosjektplanleggingslinjer som standard. Velg feltet hvis du vil bruke denne innstillingen på alle nye prosjekter du oppretter. Du kan aktivere eller deaktivere sporing av prosjektforbruk for et bestemt prosjekt ved å endre verdien i feltet **Bruk forbrukskobling** på det enkelte prosjektkortet. Konsekvensene forklares i delen nedenfor.

### <a name="to-set-up-job-usage-tracking"></a>Slik konfigurerer du sporing av prosjektforbruk

Når du arbeider på et prosjekt, vil du kanskje vite hvordan forbruket forløper seg i forhold til planen. Du kan enkelt gjøre dette ved å opprette en kobling mellom jobbplanleggingslinjene og det faktiske forbruket. Dette lar deg spore kostnader og enkelt se hvor mye arbeid som gjenstår. Linjetypen for prosjektplanlegging er som standard *Budsjett*, men bruk av linjetypen **Både Budsjett og Fakturerbar** har lignende virkning.

Etter at du har konfigurert forbrukssporing ved å velge feltet **Bruk forbrukskobling**, kan du se gjennom informasjon om prosjektplanleggingslinjen. Du kan angi antallet for ressursen, varen eller finanskontoen og deretter angi antallet du vil overføre til prosjektkladden. Feltet **Restantall** på prosjektplanleggingslinjen angir det som gjenstår å overføres og bokføres til prosjektkladden.

>[!NOTE]
> Hvis **Bruk forbrukskobling** er valgt for enkeltprosjektet og feltet **Linjetype** på prosjektkladdelinjen eller kjøpslinjen er *Fakturerbar*, opprettes det nye prosjektplanleggingslinjer av linjetypen *Budsjett* når du bokfører prosjektkladden eller kjøpsdokumentet.  
> Hvis du vil ha mer informasjon, kan du se [Registrere forbruk for prosjekter](projects-how-record-job-usage.md) og [Administrere prosjektforsyninger](projects-how-manage-project-supplies.md)

> [!IMPORTANT]
> Hvis feltet **Linjetype** på prosjektkladdelinjen eller kjøpslinjen er tomt, opprettes det ingen prosjektplanleggingslinjer når du bokfører prosjektkladden eller kjøpsdokumentet.

<!--
>[!Important]
If job usage tracking is enabled on the individual job and the **Line Type** field on the job journal or purchase line line is blank, then new job planning lines of line type *Budget* are created when you post job journal or purchase document.
If job usage tracking is not enabled and the **Line Type** field on the job journal line or purchase line is blank, then no job planning lines are created when you post job journal or purchase document.
-->


## <a name="to-set-up-prices-for-resources-items-and-general-ledger-accounts-for-jobs"></a>Slik definerer du priser for ressurser, varer og finanskonti for jobber
> [!NOTE]
> I lanseringsbølge 2 for 2020 lanserte vi nye fremgangsmåter for å definere og håndtere priser og rabatter. Hvis du er en ny kunde, bruker du den nye opplevelsen. Hvis du er en eksisterende kunde, vil din bruk av den nye funksjonen avhenge av om administratoren har aktivert funksjonsoppdateringen **Ny salgsprisopplevelse** i **Funksjonsstyring**. Hvis du vil ha mer informasjon, kan du se [Aktivering av kommende funksjoner på forhånd](/dynamics365/business-central/dev-itpro/administration/feature-management).

Du kan definere priser for varene, ressursene og finanskontiene som er relatert til en jobb. 

#### <a name="current-experience"></a>[Nåværende opplevelse](#tab/current-experience)
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Prosjekter** og velg den relaterte koblingen.  
2. Velg jobben, og velg deretter handlingen **Ressurs**, **Vare** eller **Finanskonto**.
3. Fyll ut feltene etter behov på sidene **Ressurspriser for prosjekt**, **Varepriser for prosjekt** og **Finanskontopriser for prosjekt**.

Tabellen nedenfor viser hvordan opplysningene i de valgfrie feltene vil bli brukt på prosjektplanleggingslinjer og kladder når ressursen, varen eller finanskontoen er valgt for prosjektet.

|Kolonne 1  |Kolonne 2  |
|---------|---------|
|**Prosjektressurser**|Feltene **Prosjektoppgavenr.**, **Arbeidstype**, **Valutakode**, **Linjerabatt-%** og **Enhetskostfaktor**. Verdien i feltet **Salgspris** for ressursen blir brukt på prosjektplanleggingslinjene og i prosjektkladder når du angir denne ressursen, en ressurs som er tilordnet ressursgruppen, eller en hvilken som helst ressurs. Legg merke til at denne prisen overstyrer alltid eventuelle priser som er definert i de eksisterende sidene **Ressurssalgspris/Ressursgruppepriser**.|
|**Prosjektvarer**|Feltene **Prosjektoppgavenr.**, **Valutakode** og **Linjerabatt-%**. Verdien i feltet **Salgspris** for varen blir brukt på prosjektplanleggingslinjene og i prosjektkladder når du angir denne varen. Merk at denne prisen overstyrer alltid den vanlige kundeprisen (funksjonen for "beste pris") for varer. Hvis du vil bruke de vanlige kundeprismekanismene, må du ikke opprette prosjektvarepriser for prosjektet.|
|**Finanskonti**|Informasjonen i feltene **Prosjektoppgavenr.**, **Arbeidstype**, **Valutakode**, **Linjerabatt-%** og **Enhetskost** blir brukt på prosjektplanleggingslinjene og i prosjektkladdene når denne finanskontoen angis og legges til i et prosjekt. Verdien i feltet **Salgspris** for finansprosjektutgiften blir brukt på prosjektplanleggingslinjene og i prosjektkladder når denne finanskontoen angis.|

---
#### <a name="new-experience"></a>[Ny opplevelse](#tab/new-experience)
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Prosjekter** og velg den relaterte koblingen.  
2. Velg det aktuelle prosjektet, og velg deretter handlingen **Salgsprislister**.

---

## <a name="to-set-up-job-posting-groups"></a>Slik definerer du prosjektbokføringsgrupper
Ett aspekt ved prosjektplanlegging er å bestemme hvilke bokføringskontoer som skal brukes for prosjektkostnader. Du må definere konti for bokføring for hver prosjektbokføringsgruppe for å kunne bokføre prosjekter. En bokføringsgruppe representerer en kobling mellom jobben og hvordan den skal behandles i finans. Når du oppretter en jobb, angir du en bokføringsgruppe, og hver oppgave du oppretter for prosjektet, knyttes som standard til denne bokføringsgruppen. Når du oppretter oppgaver, kan du imidlertid overstyre standardinnstillingen og velge en bokføringsgruppe som er mer hensiktsmessig.  

> [!NOTE]  
>   De nødvendige kontiene i kontoplanen må defineres før du definerer bokføringsgrupper. Hvis du vil ha mer informasjon, kan du se [Definere eller endre kontoplanen](finance-setup-chart-accounts.md).  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Prosjektbokføringsgrupper**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny** og fyll deretter ut kontofeltene som beskrevet i tabellen nedenfor.  

| Kontofelt | Beskrivelse |
| --- | --- |
| **Kode** |En kode for bokføringsgruppen. Du kan angi opptil 10 tegn, medregnet mellomrom. |
| **VIA-forbrukskonto** |VIA-kontoen for beregnet kost for VIA for prosjekt. Dette er en balansekonto for kapitalaktiva. |
| **VIA-salgskonto** |En konto for metoden Kostverdi eller Kostnad for salg i VIA-beregning, som er en gjeldskonto for påløpte utgifter i balansen. Det bokføres til denne når VIA-justeringen krever at forbrukskostbeløpene som bokføres i resultatregnskapet, økes. |
| **Forbrukskonto (resultat) for prosjekt** |En motkonto for VIA-forbrukskontoen. Dette er en motkonto for negativ utgift. |
| **Konto for utlignede varekostnader** |En motkonto for VIA-forbrukskontoen. Dette er en motkonto for negativ utgift. |
| **Konto for utlignede ressurskostnader** |En motkonto for VIA-forbrukskontoen. Dette er en motkonto for negativ utgift. |
| **Forbrukskonto (resultat)** |En motkonto for VIA-forbrukskontoen. Dette er en motkonto for negativ utgift. |
| **Salgskonto for prosjekt** |Motkontoen for VIA-salgskontoen. Dette er en utgiftskonto. |
| **Salgsutgiftskonto (budjett)** |Salgskontoen som skal brukes til finansutgifter i prosjektoppgaver med denne bokføringsgruppen. Hvis du lar dette feltet stå tomt, brukes finanskontoen som er angitt på prosjektplanleggingslinjen. |
| **VIA-konto for påløpt salg** |VIA-kontoen for beregnet salgsverdi for VIA for prosjekt. Dette er en balansekonto for påløpt inntekt. Det bokføres på denne når VIA-justeringen krever at ført inntekt skal økes. |
| **VIA-konto for fakturert salg** |Kontoen for den fakturerte salgsverdien for VIA som ikke kan føres. Dette er en balanse for ikke tjent inntekt. |
| **Konto for utlignet salg for prosjekt** |Motkontoen for VIA-kontoen for fakturert salg. Dette er en motkonto for inntekt. |
| **Salgsjusteringskonto for prosjekt** |Motkontoen for VIA-prosjektsalgskontoen. Dette er en inntektskonto. |
| **Konto for ført kost** |Utgiftskontoen som inneholder de førte kostbeløpene for prosjektet. Dette er som regel en debitutgiftskonto. |
| **Konto for ført salg** |Inntektskontoen som inneholder ført inntekt for prosjektet. Dette er som regel en kreditinntektskonto. |

## <a name="see-also"></a>Se også

[Konfigurere prosjektstyring](projects-setup-projects.md)  
[Video: Opprette et prosjekt i Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw)  
[Administrere prosjekter](projects-manage-projects.md)  
[Finans](finance.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Salg](sales-manage-sales.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
