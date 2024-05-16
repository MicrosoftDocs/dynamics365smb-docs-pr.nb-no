---
title: Synkroniser kunder og selskaper
description: Importer kunder fra eller eksporter til Shopify.
ms.date: 03/25/2024
ms.topic: article
ms.service: dynamics-365-business-central
ms.search.form: '30105, 30106, 30107, 30108, 30109,'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
---

# <a name="synchronize-customers-and-companies"></a>Synkroniser kunder og selskaper

Når du importerer en ordre fra Shopify, er det nødvendig å hente informasjonen om kunden for ytterligere behandling av dokumentet i [!INCLUDE[prod_short](../includes/prod_short.md)]. Det finnes to hovedalternativer for å gjøre dette og flere kombinasjoner:

* Bruk en spesiell kunde for alle ordrer.
* Importer kundeinformasjonen fra Shopify. Dette alternativet er også tilgjengelig når du eksporterer kunder til Shopify fra [!INCLUDE[prod_short](../includes/prod_short.md)].

Shopify lar deg drive B2B- og DTC-virksomheten din fra ett sted med kraften og brukervennligheten til Shopify-alt-i-ett-plattformen. Shopify Connector fungerer også med forskjellige typer e-handel.

Shopify har to enheter, kunde og selskap, men [!INCLUDE[prod_short](../includes/prod_short.md)] har bare kundeenheten, noe som påvirker hvordan synkronisering fungerer.

Når du kjører DTC, opprettes kjøperen i Shopify som en kunde. Kunden importeres deretter til [!INCLUDE[prod_short](../includes/prod_short.md)] som en Shopify-kunde og kobles til eller konverteres til en kunde.

Hvis du driver B2B, opprettes kjøperen i Shopify som en kunde som er knyttet til et selskap. Kunden importeres til [!INCLUDE[prod_short](../includes/prod_short.md)] som en Shopify-kunde, og selskapet importeres til [!INCLUDE[prod_short](../includes/prod_short.md)] som et Shopify-selskap og knyttes til eller konverteres til en kunde.

Hvis du vil eksportere en kunde fra [!INCLUDE[prod_short](../includes/prod_short.md)] til Shopify, er fremgangsmåten forskjellig avhengig av hva du vil gjøre:

* Eksporter en kunde som en Shopify-kunde for DTC.
* Eksporter en kunde som selskap og kundepar for B2B-flyten.

## <a name="important-settings-when-importing-dtc-customers-from-shopify"></a>Viktige innstillinger når du importerer DTC-kunder fra Shopify

Enten du masseimporterer kunder fra Shopify eller når du importerer ordrer, kan du styre prosessen med følgende innstillinger:

|Felt|Beskrivelse|
|------|-----------|
|**Kundeimport fra Shopify**|Velg **Alle kunder** hvis du har tenkt å importere kunder fra Shopify samtidig, enten manuelt ved hjelp av **Synkroniser kunder**-handling eller via jobbkø for regelmessige oppdateringer. Uansett hvilket utvalg du velger, importeres alltid kundeinformasjon sammen med ordre. Bruken av denne informasjonen avhenger imidlertid av **Shopify-kundemaler** og innstillinger i feltet **Kundetildelingstype**.|
|**Kundetildelingstype**|Definer hvordan du vil at koblingen skal utføre tildelingen.</br></br>- **Via e-post/telefon** hvis du vil at koblingen skal bruke informasjon om e-postkonto og telefon til å tilordne den importerte Shopify-kunden til en kunde i Business Central.</br></br>- **Etter faktura til-informasjon** hvis du vil at koblingen skal bruke adressen til fakturamottakeren til å tilordne den importerte Shopify-kunden til en eksisterende kunde i Business Central.</br></br>- **Ta alltid med standard kunde** hvis du vil at systemet skal bruke en kunde fra **Standard kundenr.** . |
|**Shopify kan oppdatere kunder**| Velg dette feltet om du vil at koblingen skal oppdatere kundene den finner, når alternativene **Via e-post/telefon** eller **Etter faktura til-informasjon** er valgt i feltet **Kundetildelingstype**.|
|**Opprett ukjente kunder automatisk**| Velg dette feltet om du vil at koblingen skal opprette manglende kunder som blir funnet, når alternativene **Via e-post/telefon** eller **Etter faktura til-informasjon** er valgt i feltet **Kundetildelingstype**. En ny kunde opprettes ved hjelp av importerte data og **Kundemalkode** som er definert på sidene **Shopify-butikkort** eller **Shopify-kundemal**. Legg merke til at Shopify-kunden må ha minst én adresse. Ordrer som er opprettet via Shopify-salgsstedssalgskanalen, mangler ofte adresseopplysninger. Hvis dette alternativet ikke er aktivert, må du opprette en kunde manuelt og knytte den til Shopify-kunden.|
|**Kode for kunde-/selskapsmal**|Bruk dette feltet sammen med **Opprett ukjente kunder automatisk**.</br></br>Velg standardmalen som skal brukes for automatisk opprettede kunder. Kontroller at den valgte malen inneholder de obligatoriske feltene, for eksempel **Bokføringsgruppe – firma**, **Bokføringsgruppe – kunde**, merverdiavgiftsrelaterte (mva.) eller avgiftsrelaterte felter.</br></br>Du kan definere maler per land/område på siden **Shopify-kundemaler**, som foretar en riktig beregning av mva.</br></br>Finn ut mer under [Definer avgifter](setup-taxes.md).|

### <a name="customer-template-per-countryregion"></a>Kundemal per land/område

Enkelte innstillinger kan defineres på nivået land/område, eller på nivået delstat/provins. Innstillingene kan konfigureres i [Forsendelse og levering](https://www.shopify.com/admin/settings/shipping) i Shopify.

Du kan gjøre følgende for hver kunde ved å bruke **Shopify-kundemalen**:

1. Angi **Standard kundenr.**, som har høyere prioritet over det som er valgt i feltene **Kundeimport fra Shopify** og **Kundetildelingstype**. Den brukes i den importerte ordren.
2. Definere **kundemalkoden**, som brukes til å opprette manglende kunder, hvis **Opprett ukjente kunder automatisk** er aktivert. Hvis **kundemalkoden** er tom, bruker funksjonen **kundemalkoden** som er definert på **Shopify-butikkort**. Systemet prøver først å finne en mal for **fylkes-/områdekode** for standardadressen. Hvis det ikke finnes noen mal, brukes den første adressen.
3. I noen tilfeller er ikke **kundemalkoden** som er definert for et land/område, nok til å sikre riktig avgiftsberegninger (f.eks. for land/område med mva.). I dette tilfellet kan det være nyttig å ta med **avgiftsområde**.
4. **Avgiftsområde**-feltet inneholder også et par for **landskode** og **fylkesnavn**. Dette paret er nyttig når koblingen må konvertere en kode til et navn, eller omvendt.

> [!NOTE]  
> Landkodene er ISO 3166-1 for alpha-2-landkoder. Finn ut mer under [Landskode](https://help.shopify.com/en/api/custom-storefronts/storefront-api/reference/enum/countrycode).

## <a name="important-settings-when-exporting-dtc-customers-to-shopify"></a>Viktige innstillinger når du eksporterer DTC-kunder til Shopify

Du kan eksportere eksisterende kunder til Shopify samtidig. I hvert tilfellet opprettes det en kunde og én standardadresse. Du kan administrere prosessen ved å bruke følgende innstillinger:

|Felt|Description|
|------|-----------|
|**Kan oppdatere Shopify-kunder**| Aktiver dette alternativet hvis du vil generere oppdateringer senere fra Business Central for kunder som allerede finnes i Shopify.|

Følgende er krav for å eksportere en kunde:

* Kunden må ha en gyldig e-postadresse.
* Når du eksporterer kunder med adresser som omfatter provinser/stater, må du passe på at **ISO-koden** er fylt ut for land/områder.|
* Når et land/område er valgt på kundekortet, må du kontrollere at **ISO-kode** er angitt. For lokale kunder med tomt land/område bruker Shopify-koblingen landet/området som er angitt på siden **Selskapsinformasjon**.
* Hvis kunden har et telefonnummer, må nummeret være unikt siden Shopify ikke godtar en ny kunde med det samme telefonnummeret.
* Hvis kunden har et telefonnummer, må det være i E.164-formatet. Det er støtte for forskjellige formater hvis de representerer et tall som kan slås fra hvor som helst i hele verden. Følgende formater er gyldige:

  * xxxxxxxxxx
  * +xxxxxxxxxxx
  * (xxx)xxx-xxxx
  * +x xxx-xxx-xxxx

Når du har opprettet kundene i Shopify, kan du sende dem direkteinvitasjoner for å oppmuntre dem til å aktivere kontoene sine.

### <a name="populate-customer-information-in-shopify"></a>Fyll ut kundeinformasjon i Shopify

En kunde i Shopify har fornavn, etternavn, e-post eller telefonnummer. Du kan angi fornavn og etternavn fra kundekortet i [!INCLUDE[prod_short](../includes/prod_short.md)].

|Prioritet|Felt i kundekortet|Description|
|------|------|-----------|
|1|**Kontaktnavn**|Høyeste prioritet hvis feltet **Kontaktnavn** er fylt ut og feltet **Kontaktkilde** på **Shopify-butikkortet** inneholder et av alternativene *Fornavn og etternavn* eller *Etternavn og fornavn* for å definere hvordan verdiene skal deles.|
|2|**Navn 2**|Hvis feltet **Navn 2** er fylt ut og feltet **Navn 2-kilde** på **Shopify-butikkortet** inneholder alternativene *Fornavn og etternavn* eller *Etternavn og fornavn* for å definere hvordan verdiene skal deles.|
|3|**Navn**|Laveste prioritet hvis feltet **Navn** er fylt ut og feltet **Navnkilde** på **Shopify-butikkortet** inneholder alternativene *Fornavn og etternavn* eller *Etternavn og fornavn* for å definere hvordan verdiene skal deles.|

En kunde i Shopify har i tillegg en standard adresse. Adressen kan inneholde et selskap og en adresse i tillegg til fornavn, etternavn, e-post og/eller telefonnummer. Du kan fylle ut **Selskap**- feltet basert på data fra kundekortet i [!INCLUDE[prod_short](../includes/prod_short.md)].

|Prioritet|Felt i kundekortet|Description|
|------|------|-----------|
|1|**Navn**|Høyeste prioritet hvis feltet **Navnekilde** på **Shopify-butikkortet** inneholder *Selskapsnavn*.|
|2|**Navn 2**|Laveste prioritet hvis feltet **Navn 2-kilde** på **Shopify-butikkortet** inneholder *Selskapsnavn*.|

For adresser der land/område brukes, velger du **Kode** eller **Navn** i feltet **Fylkeskilde** på siden **Shopify-butikkortet**. Koden eller navnet angir datatypen som er lagret i [!INCLUDE[prod_short](../includes/prod_short.md)] i feltet **Fylke**. Husk å starte kundemaler per land/område, slik at landskode/navnetildeling er klar. 

## <a name="export-dtc-customers-to-shopify"></a>Eksporter DTC-kunder til Shopify

### <a name="initial-sync-of-customers-from-business-central-to-shopify"></a>Første synkronisering av kunder fra Business Central til Shopify

1. Gå til søkeikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Shopify-kunder**. Velg den relaterte koblingen.
2. Velg handlingen **Legg til kunde**.
3. I feltet **Butikkode** angir du koden. Hvis du åpner vinduet **Shopify-kunder** fra siden **Butikkort**, fylles butikkoden ut automatisk.
4. Definer filtre for kunder etter behov. Du kan for eksempel filtrere etter land-/områdekode.
5. Velg **OK**.

De resulterende kundene opprettes automatisk i Shopify med adresser.

> [!NOTE]  
> Den innledende synkronisering av kunder fra [!INCLUDE[prod_short](../includes/prod_short.md)] til Shopify tar ikke hensyn til innstillingene under **Kan oppdatere Shopify-kunder**.

### <a name="sync-customers"></a>Synkroniser kunder

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Shopify-butikk** og velger den relaterte koblingen.
2. Velg den bestemte butikken du vil synkronisere kunder med.
3. Velg handlingen **Synkroniser kunder**.

Du kan også bruke handlingen **Start kundesynkronisering** i vinduet **Shopify-kunder** eller søk etter den satsvise jobben **Synkroniser kunder**.

Du kan planlegge at oppgaven skal utføres på en automatisk måte. Finn ut mer under [Planlegg gjentakende oppgaver](background.md#to-schedule-recurring-tasks).

## <a name="b2b-companies"></a>B2B-selskaper

Hvis du bruker B2B i Shopify, kan du opprette selskaper i tillegg til kunder. Du kan knytte én eller flere enkeltkunder til et selskap. Du kan også definere betalingsbetingelser, lokasjoner og kataloger.

## <a name="important-settings-when-importing-b2b-companies-from-shopify"></a>Viktige innstillinger når du importerer B2B-selskaper fra Shopify

Enten du masseimporterer selskaper fra Shopify eller når du importerer ordrer, kan du bruke innstillingene i følgende tabell til å styre prosessen.

|Felt|Beskrivelse|
|------|-----------|
|**Selskapsimport fra Shopify**|Velg **Alle selskaper** hvis du har tenkt å importere kunder fra Shopify samtidig, enten manuelt ved hjelp av **Synkroniser selskaper**-handlingen eller via jobbkøen for regelmessige oppdateringer. Uansett hva du velger, importeres alltid kundeinformasjon sammen med ordren. Bruken av denne informasjonen avhenger imidlertid av **Shopify-selskapsmaler** og innstillinger i feltet **Tildelingstype for selskap**.|
|**Tildelingstype for selskap**|Definer hvordan du vil at koblingen skal utføre tildelingen.</br></br>- **Via e-post/telefon** hvis du vil at koblingen skal tildele de importerte Shopify-selskapene til en eksisterende kunde i Business Central ved å bruke e-post og telefon fra hovedkontakten.</br></br>- Velg **Ta alltid standardselskapet** hvis du vil at systemet skal bruke selskapet i **Standard selskapsnr.** . |
|**Shopify kan oppdatere selskap**| Velg dette feltet hvis du vil at koblingen skal oppdatere kundene den finner, når alternativet **Via e-post/telefon** er valgt i feltet **Tildelingstype for selskap**.|
|**Opprett ukjente selskaper automatisk**| Velg dette feltet hvis du vil at koblingen skal opprette nye kunder når alternativet **Via e-post/telefon** er valgt i feltet **Tildelingstype for selskap**. En ny kunde opprettes ved hjelp av de importerte dataen og **Kunde-/selskapsmalkode** som er definert på sidene **Shopify-butikkort** eller **Shopify-kundemal**.|
|**Kode for kunde-/selskapsmal**|Bruk dette feltet sammen med **Opprett ukjent selskap automatisk**.</br></br>- Velg standardmalen som skal brukes for automatisk opprettede kunder. Kontroller at de obligatoriske feltene er fylt ut i malen, for eksempel **Bokføringsgruppe - firma**, **Bokføringsgruppe - kunde**, **Merverdiavgift (mva)**, eller andre avgiftsrelaterte felter.</br></br>- Du kan definere maler per land/område på siden **Shopify-kundemaler**, som er nyttig for å kunne foreta en riktig beregning av mva.</br></br>Finn ut mer under [Definer avgifter](setup-taxes.md).|

> [!NOTE]  
> Selskapet må ha en hovedkontakt. Ellers hopper koblingen til selskap.
> Bare én eldste lokasjon importeres.
> Det er bare hovedkontakten som importeres.

## <a name="important-settings-when-exporting-b2b-companies-to-shopify"></a>Viktige innstillinger når du eksporterer B2B-selskaper til Shopify

Du kan eksportere eksisterende kunder til Shopify samtidig som et selskap. I hvert tilfelle opprettes det et selskap og én standardlokasjon, og én hovedkontakt. Det er også mulig å opprette en katalog.

|Felt|Description|
|------|-----------|
|**Kan oppdatere Shopify-selskaper**| Aktiver dette alternativet hvis du vil generere oppdateringer senere fra Business Central for selskaper som allerede finnes i Shopify.|
|**Standard kontakttillatelser**| Angi hvilke tillatelser som må tilordnes til hovedkontakten. Du kan velge mellom **Ingen**, **Bare bestilling** og **Lokasjonsadministrator**.|
|**Opprett katalog automatisk**| Aktiver dette alternativet hvis du vil opprette en katalog som inneholder alle produktene. Det opprettes en katalog for hvert eksporterte selskap.|

## <a name="export-a-b2b-company-to-shopify"></a>Eksporter et B2B-selskap til Shopify

### <a name="initial-sync-of-b2b-companies-from-business-central-to-shopify"></a>Første synkronisering av B2B-selskaper fra Business Central til Shopify

1. Gå til søkeikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Shopify-selskap**. Velg den relaterte koblingen.
2. Velg handlingen **Legg til selskap**.
3. I feltet **Butikkode** angir du koden. Hvis du åpner vinduet **Shopify-selskap** fra siden **Butikkort**, fylles butikkoden ut automatisk.
4. Definer filtre for kunden etter behov. Du kan for eksempel filtrere etter land-/områdekode.
5. Velg **OK**.

Resulterende selskap og kunder opprettes automatisk i Shopify.

> [!NOTE]  
> Innledende synkronisering av selskaper fra [!INCLUDE[prod_short](../includes/prod_short.md)] til Shopify tar ikke hensyn til innstillingene under **Kan oppdatere Shopify-selskap**.

### <a name="sync-b2b-company"></a>Synkroniser B2B-selskap

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Shopify-butikk** og velger den relaterte koblingen.
2. Velg den bestemte butikken du vil synkronisere kunder med.
3. Velg handlingen **Synkroniser selskap**.

Du kan også bruke handlingen **Start synkronisering av selskap** på siden **Shopify-selskap** eller søke etter den satsvise jobben **Synkroniser selskap**.

Du kan planlegge at oppgaven skal kjøres på en automatisk måte. Finn ut mer under [Planlegg gjentakende oppgaver](background.md#to-schedule-recurring-tasks).

## <a name="see-also"></a>Se også

[Kom i gang med koblingen for Shopify](get-started.md)  
