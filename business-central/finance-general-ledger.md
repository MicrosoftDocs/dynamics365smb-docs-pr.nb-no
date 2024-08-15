---
title: Forstå Finans og kontoplanen
description: 'Beskriver Finans, kontoplanen og kontokategoriene. Bruk siden Finansoppsett til å angi hvordan du håndterer bestemte regnskapssaker i firmaet.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'analysis, history, track'
ms.search.form: '18, 20, 37, 65, 99, 312, 314, 313, 395, 552, 569, 570, 634, 790, 791, 1158'
ms.date: 04/19/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="understand-the-general-ledger-and-chart-of-accounts"></a>Forstå Finans og kontoplanen

Økonomimodulen lagrer dine økonomiske data, og kontoplanen viser kontoene som du bokfører finansposter til. [!INCLUDE[prod_short](includes/prod_short.md)] inneholder en standard kontoplan som er klar til å støtte forretningsvirksomheten din.

## <a name="general-ledger-setup-and-general-posting-setup"></a>Finansoppsett og generelt bokføringsoppsett

Oppsettet av finans er i kjernen av økonomiske prosesser fordi den definerer hvordan du kan legge inn data. Spesielt to sider spiller en viktig del av konfigurasjonen av økonomiprosessene:  

* **Finansoppsett**
* **Generelt bokføringsoppsett**

### <a name="the-general-ledger-setup-page"></a>Siden **Finansoppsett**

Bruk siden **Finansoppsett** til å angi hvordan du håndterer bestemte regnskapssaker i firmaet, for eksempel:  

* Detaljopplysninger om fakturaavrunding  
* Adresseformater  
* Finansrapportering

> [!TIP]
> Siden **Finansoppsett** inneholder generelle felter og felter som er spesifikke for landet eller området ditt. Hvis du ikke er sikker på betydningen av et felt, foreslår vi at du arbeider med regnskapsføreren for å finne ut om det er av relevans for organisasjonen. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

Hvis du vil åpne siden nå, bruker du følgende kobling [Finansoppsett](https://businesscentral.dynamics.com/?page=118).

### <a name="the-general-posting-setup-page"></a>Siden **Generelt bokføringsoppsett**

Bruk siden **Generelt bokføringsoppsett** til å konfigurere kombinasjoner av firma- og varebokføringsgrupper. Bokføringsgrupper tilordner enheter som kunder, leverandører, varer, ressurser og salgs- og kjøpsdokumenter til finanskonti. Fyll ut en linje for hver kombinasjon av firma- og varebokføringsgrupper. Men du kan også åpne hver linje i et eget bokføringsoppsettskort. Finn ut mer under [Oppsett av bokføringsgrupper](finance-posting-groups.md).  

> [!TIP]
> Hvis du ikke kan se feltene du leter etter, på siden **Generelt bokføringsoppsett**, bruker du det vannrette rullefeltet nederst på siden til å bla til høyre.  

Hvis du vil åpne siden nå, bruker du følgende kobling [Generelt bokføringsoppsett](https://businesscentral.dynamics.com/?page=314).

## <a name="the-chart-of-accounts"></a>Kontoplanen

Siden **Kontoplanen** viser alle finanskontoer. Fra kontoplanen kan du gjøre ting som:  

* Vise rapporter som viser finansposter og saldoer.  
* Lukke resultatregnskapet.  
* Åpne finanskontokortet for å legge til eller endre innstillinger.  
* Vise en liste over bokføringsgrupper for kontoen.
* Vise separate debet- og kreditsaldoer for én konto.

Hvis du vil finne ut mer, kan du gå til [Forstå kontoplanen](finance-chart-of-accounts.md).

## <a name="account-categories"></a>Kontokategorier

Du kan tilpasse strukturen i kontoutskrifter ved å tilordne finanskontoer til kontokategorier.  

Siden **Finanskontokategorier** viser kategoriene og underkategoriene dine samt finanskontiene som er tilordnet til dem. Du kan opprette nye underkategorier og tilordne disse kategoriene til eksisterende kontoer.  

Du kan opprette en kategorigruppe ved å rykke inn andre underkategorier under en linje på siden **Finanskontokategorier**. Kategorigrupper gjør det enkelt for deg å få en oversikt, fordi hver gruppering viser den totale saldoen. Du kan opprette underkategorier for ulike typer aktiva, og deretter opprette kategorigrupper for aktiva kontra omløpsmidler.  

Du kan definere om spesifikke typer rapporter må inkluderes i bestemte typer rapporter. Kontokategoriene bidra til å definere oppsettet for regnskapsoppgjør.  

### <a name="example"></a>Eksempel

Standard saldoutdrag har for eksempel en underkategori for *kontanter* under *gjeldende aktiva*. Hvis du vil at saldoutdraget skal ta hensyn til håndkasse og sjekker, utfører du følgende trinn:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Finanskontokategorier**, og velg deretter den relaterte koblingen.
   1. Alternativet kan du [åpne siden her](https://businesscentral.dynamics.com/?page=790).
2. Velg handlingen **Rediger oversikt**.
3. Legg til to nye underkategorier: Én for håndkassen og én for sjekkontoen:
   1. Velg kategorien **Gjeldende aktiva**.
   2. Velg handlingen **Ny**.
   3. Angi underkategorinavn i feltet **Beskrivelse**.
   4. I feltet **Finanskontoer i kategori** velger du riktig finanskonto.
   5. I feltet **Definisjon av tilleggsrapport** velger du **Kontantkontoer**-alternativet.
4. Rykk inn dem under **Kontanter**-underkategori.
   1. Velg underkategorien som ble opprettet i trinn 3.
   2. Velg handlingen **Rykk inn**.
   3. Velg handlingen **Flytt ned**.
   4. Velg handlingen **Rykk inn** for å rykke inn under under kategorien **Kontant**.

Når du velger handlingen **Generer finansrapporter**, eller neste gang rapporten genereres, viser saldoutdraget følgende linjer:

* Total saldo på kontanter.
* Linjer med saldoer for håndkasse og sjekkkontoen.  

> [!NOTE]
> Hvis du oppretter en finanskonto uten å tildele en kontokategori, tildeler [!INCLUDE[prod_short](includes/prod_short.md)] automatisk kontokategorien fra finanskontoen rett over kontoen i kontoplanen når du tildeler kontoen til en bokføringsgruppe. Hvis du vil ta med den nye kontoen i finansrapportene, må du imidlertid velge handlingen **Generer finansrapporter** på siden **Finanskontokategorier**. Du kan også åpne siden Finanskontokort, angi kontokategorien og deretter generere finansrapporten på nytt.

## <a name="access-to-create-and-edit-gl-accounts-and-account-categories"></a>Tilgang til å opprette og redigere finanskontoer og kontokategorier

I en liten organisasjon, for eksempel CRONUS-demoselskapet, kan de fleste brukere redigere finansposter som finanskontoer, kontokategorier og kontoplanen, unntatt brukere med en gruppemedlemslisens. Større organisasjoner bruker vanligvis roller og tillatelser til å begrense redigering av disse enhetene. Hvis du er administrator eller har rollen som *Forretningssjef* eller *Regnskapsfører*, kan du kontrollere brukertillatelsene for å gi de riktige personene tilgang til relevante tabeller. Hvis du vil ha mer informasjon, kan du gå til [Få en oversikt over en brukers tillatelser](ui-define-granular-permissions.md#get-an-overview-of-a-users-permissions).  

## <a name="use-dimensions-to-simplify-your-chart-of-accounts"></a>Bruk dimensjoner til å forenkle kontoplanen

Dimensjoner er attributter og verdier som kategoriserer poster slik at du kan spore og analysere dem på dokumenter, for eksempel ordrer. Dimensjoner kan for eksempel angi hvilket prosjekt eller hvilken avdeling en post kommer fra. I stedet for å opprette separate finanskonti for hver avdeling og hvert prosjekt, kan du for eksempel bruke dimensjoner som grunnlag for analyse og unngå å måtte opprette en komplisert kontoplan.

Hvis du vil finne ut mer om dimensjoner, kan du gå til [Definer standarddimensjoner for kunder, leverandører og andre kontoer](finance-dimensions.md#to-set-up-default-dimensions-for-customers-vendors-and-other-accounts).

## <a name="see-also"></a>Se også

[Forstå kontoplanen](finance-chart-of-accounts.md)  
[Arbeid med dimensjoner](finance-dimensions.md)  
[Tildel tillatelser til brukere og grupper](ui-define-granular-permissions.md)  
[Forretningsintelligens](bi.md)  
[Finans](finance.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
