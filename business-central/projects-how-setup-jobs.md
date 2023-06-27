---
title: 'Konfigurere prosjekter, priser og prosjektbokføringsgrupper'
description: Beskriver hvordan du definerer generell informasjon om prosjekter.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 04/25/2023
ms.custom: bap-template
ms.search.keywords: project management
ms.search.form: '211, 463, 1012'
---
# <a name="set-up-jobs-prices-and-job-posting-groups" />Konfigurere prosjekter, priser og prosjektbokføringsgrupper

Som prosjektleder kan du sette opp prosjekter som definerer alle prosjekter du administrerer i [!INCLUDE[prod_short](includes/prod_short.md)]. Bruk siden **Prosjektoppsett** til å definere hvordan du skal bruke prosjektfunksjoner.

Angi ulike opplysninger for hvert prosjekt:

* Priser for prosjektvarer
* Prosjektressurser
* Finanskontoer for prosjekt
* Prosjektbokføringsgrupper (obligatorisk)

## <a name="to-set-general-information-for-jobs" />Slik angir du generell informasjon for prosjekter

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Prosjektoppsett** og velg den relaterte koblingen.
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> Vekslebryteren **Bruk forbrukskobling som standard** på siden **Prosjektoppsett** angir om prosjektposter er koblet til prosjektplanleggingslinjer som standard. Slå på vekslebryteren for å bruke denne innstillingen på alle nye prosjekter. Du kan aktivere eller deaktivere sporing av prosjektforbruk for et bestemt prosjekt ved slå av eller på vekslebryteren **Bruk forbrukskobling** på siden **Prosjektkort**.

### <a name="to-set-up-job-usage-tracking" />Slik konfigurerer du sporing av prosjektforbruk

Når du arbeider på et prosjekt, vil du kanskje vite hvordan forbruket forløper seg i forhold til planen. Du kan utforske forbruket ved å opprette en kobling mellom jobbplanleggingslinjene og det faktiske forbruket. Med koblingen kan du holde oversikt over kostnadene og forstå hvor mye arbeid som gjenstår. Som standard er prosjektplanleggingslinjetypen **Budsjett**, men bruk av linjetypen **Både Budsjett og Fakturerbar** har liknende effekter.

Etter at du har konfigurert forbrukssporing ved å slå på vekslebryteren **Bruk forbrukskobling som standard**, kan du se gjennom informasjon om prosjektplanleggingslinjen. Du kan for eksempel definere antallet for ressursen, varen eller finanskontoen. Du kan også angi antallet du vil overføre til prosjektkladden. Feltet **Restantall** på prosjektplanleggingslinjen viser hva som gjenstår å overføres og bokføres til prosjektkladden.

>[!NOTE]
> Hvis **Bruk forbrukskobling** er valgt for prosjektet og feltet **Linjetype** på prosjektkladdelinjen eller kjøpslinjen er **Fakturerbar**, opprettes det nye prosjektplanleggingslinjer av linjetypen **Både budsjett og fakturerbar** når du bokfører prosjektkladden eller kjøpsdokumentet.  
>
> Hvis du vil ha mer informasjon, kan du se [Registrere forbruk for prosjekter](projects-how-record-job-usage.md) og [Administrere prosjektforsyninger](projects-how-manage-project-supplies.md)

> [!IMPORTANT]
> Hvis du ikke angir en verdi i feltet **Linjetype** på prosjektkladdelinjen eller kjøpslinjen, opprettes det ingen prosjektplanleggingslinjer når du bokfører prosjektkladden eller kjøpsdokumentet.

## <a name="to-set-up-prices-for-resources-items-and-general-ledger-accounts-for-jobs" />Slik definerer du priser for ressurser, varer og finanskonti for jobber

> [!NOTE]
> I lanseringsbølge 2 for 2020 lanserte vi nye fremgangsmåter for å definere og håndtere priser og rabatter. Hvis du er en ny kunde, bruker du den nye opplevelsen. Hvis du er en eksisterende kunde, vil din bruk av den nye funksjonen avhenge av om administratoren har aktivert funksjonsoppdateringen **Ny salgsprisopplevelse** i **Funksjonsstyring**. Hvis du vil ha mer informasjon, kan du se [Aktivering av kommende funksjoner på forhånd](/dynamics365/business-central/dev-itpro/administration/feature-management).

Du kan definere priser for varene, ressursene og finanskontiene som er relatert til en jobb. 

#### [Nåværende opplevelse](#tab/current-experience)

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Prosjekter** og velg den relaterte koblingen.  
2. Velg jobben, og velg deretter handlingen **Ressurs**, **Vare** eller **Finanskonto**.
3. Fyll ut feltene etter behov på sidene **Ressurspriser for prosjekt**, **Varepriser for prosjekt** og **Finanskontopriser for prosjekt**.

Når du velger en ressurs, en vare eller en finanskonto for et prosjekt, bruker [!INCLUDE [prod_short](includes/prod_short.md)] informasjon i de valgfrie feltene på prosjektplanleggingslinjene og i prosjektkladdene. Tabellen nedenfor forklarer hvordan.

|Kolonne 1  |Kolonne 2  |
|---------|---------|
|**Prosjektressurser**|Feltene **Prosjektoppgavenr.**, **Arbeidstype**, **Valutakode**, **Linjerabatt-%** og **Enhetskostfaktor**. Verdien i feltet **Salgspris** for ressursen brukes på prosjektplanleggingslinjer og i prosjektkladder når du angir en ressurs eller en ressurs som er tildelt til ressursgruppen. Denne prisen overstyrer priser angitt på siden **Ressurssalgspris/Ressursgruppepriser**.|
|**Prosjektvarer**|Feltene **Prosjektoppgavenr.**, **Valutakode** og **Linjerabatt-%**. Verdien i feltet **Salgspris** for varen blir brukt på prosjektplanleggingslinjene og i prosjektkladder når du angir denne varen. Denne prisen overstyrer den vanlige kundeprisen (funksjonen for «beste pris») for varer. Hvis du vil bruke den vanlige kundeprisen, må du ikke angi prosjektvarepriser for prosjektet.|
|**Finanskonti**|Informasjonen i feltene **Prosjektoppgavenr.**, **Arbeidstype**, **Valutakode**, **Linjerabatt-%** og **Enhetskost** blir brukt på prosjektplanleggingslinjene og i prosjektkladdene når denne finanskontoen angis og legges til i et prosjekt. N du velger en finanskonto, bruker prosjektplanleggingslinjer og prosjektkladder verdien i feltet **Salgspris** for finansprosjektutgiften.|

#### [Ny opplevelse](#tab/new-experience)

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Prosjekter** og velg den relaterte koblingen.  
2. Velg det aktuelle prosjektet, og velg deretter handlingen **Salgsprislister**.

---

## <a name="to-set-up-job-posting-groups" />Slik definerer du prosjektbokføringsgrupper

Ett aspekt ved prosjektplanlegging er å bestemme hvilke bokføringskontoer som skal brukes for prosjektkostnader. Du må definere konti for bokføring for hver prosjektbokføringsgruppe for å kunne bokføre prosjekter. En bokføringsgruppe representerer en kobling mellom jobben og hvordan den skal behandles i finans. Når du oppretter en jobb, angir du en bokføringsgruppe, og hver oppgave du oppretter for prosjektet, knyttes som standard til denne bokføringsgruppen. Når du oppretter oppgaver, kan du imidlertid overstyre standardinnstillingen og velge en bokføringsgruppe som er mer hensiktsmessig.  

> [!NOTE]  
> Du må konfigurere kontoene i kontoplanen før du definerer bokføringsgrupper. Hvis du vil ha mer informasjon, kan du se [Definere eller endre kontoplanen](finance-setup-chart-accounts.md).  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Prosjektbokføringsgrupper**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny** og fyll deretter ut feltene som beskrevet i tabellen nedenfor.  

| Kontofelt | Description |
| --- | --- |
| **Kode** |En identifikator for bokføringsgruppen. Du kan angi opptil 10 tegn, medregnet mellomrom. |
| **VIA-forbrukskonto** |VIA-kontoen for beregnet kost for VIA for prosjekt. Dette er en balansekonto for kapitalaktiva. |
| **VIA-salgskonto** |En konto for beregning av kostverdi eller salgspris for VIA-beregning. Denne kontoen er for påløpte utgifter på balansen. Når en VIA-justering krever at du øker forbrukskostnadene som du bokfører i resultatregnskapet, bokfører du til denne kontoen. |
| **Forbrukskonto (resultat) for prosjekt** |En motkonto for VIA-forbrukskontoen. Dette er en motkonto for negativ utgift. |
| **Konto for utlignede varekostnader** |En motkonto for VIA-forbrukskontoen. Dette er en motkonto for negativ utgift. |
| **Konto for utlignede ressurskostnader** |En motkonto for VIA-forbrukskontoen. Dette er en motkonto for negativ utgift. |
| **Forbrukskonto (resultat)** |En motkonto for VIA-forbrukskontoen. Dette er en motkonto for negativ utgift. |
| **Salgskonto for prosjekt** |Motkontoen for VIA-salgskontoen. Dette er en utgiftskonto. |
| **Salgsutgiftskonto (budjett)** |Salgskontoen som skal brukes til finansutgifter i prosjektoppgaver med denne bokføringsgruppen. Hvis du lar dette feltet stå tomt, brukes finanskontoen som er angitt på prosjektplanleggingslinjen. |
| **VIA-konto for påløpt salg** |VIA-kontoen for beregnet salgsverdi for VIA for prosjekt, som er en påløpt balansekonto for balansen. Når en VIA-justering krever at du øker ført inntekt, bokfører du til denne kontoen. |
| **VIA-konto for fakturert salg** |Kontoen for den fakturerte salgsverdien for VIA som ikke kan føres. Dette er en balanse for ikke tjent inntekt. |
| **Konto for utlignet salg for prosjekt** |Motkontoen for VIA-kontoen for fakturert salg. Dette er en motkonto for inntekt. |
| **Salgsjusteringskonto for prosjekt** |Motkontoen for VIA-prosjektsalgskontoen. Dette er en inntektskonto. |
| **Konto for ført kost** |Utgiftskontoen som inneholder de førte kostbeløpene for prosjektet. Dette er som regel en debitutgiftskonto. |
| **Konto for ført salg** |Inntektskontoen som inneholder ført inntekt for prosjektet. Dette er som regel en kreditinntektskonto. |

## <a name="see-related-microsoft-training" />Se relatert [Microsoft-opplæring](/training/paths/set-up-jobs-resources/)

## <a name="see-also" />Se også

[Konfigurere prosjektstyring](projects-setup-projects.md)  
[Video: Opprett et prosjekt i Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw)  
[Administrere prosjekter](projects-manage-projects.md)  
[Finans](finance.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Salg](sales-manage-sales.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
