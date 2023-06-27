---
title: Synkroniser kunder
description: Importer kunder fra eller eksporter til Shopify
ms.date: 06/06/2023
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '30105, 30106, 30107, 30108, 30109,'
author: andreipa
ms.author: andreipa
ms.reviewer: bholtorf
---

# <a name="synchronize-customers"></a>Synkroniser kunder

Når du importerer en ordre fra Shopify, er det nødvendig å hente informasjonen om kunden for ytterligere behandling av dokumentet i [!INCLUDE[prod_short](../includes/prod_short.md)]. Det finnes to hovedalternativer for å gjøre dette og flere kombinasjoner:

* Bruk en spesiell kunde for alle ordrer.
* Importer faktiske kundeinformasjon fra Shopify. Dette alternativet er også tilgjengelig når du eksporterer kunder til Shopify fra [!INCLUDE[prod_short](../includes/prod_short.md)] først.

## <a name="important-settings-when-importing-customers-from-shopify"></a>Viktige innstillinger når du importerer kunder fra Shopify

Enten du masseimporterer kunder fra Shopify eller når du importerer ordrer, kan du styre prosessen med følgende innstillinger:

|Felt|Beskrivelse|
|------|-----------|
|**Kundeimport fra Shopify**|Velg **Alle kunder** hvis du har tenkt å importere kunder fra Shopify samtidig, enten manuelt ved hjelp av **Synkroniser kunder**-handling eller via jobbkø for regelmessige oppdateringer. Uansett hvilket utvalg du velger, importeres alltid kundeinformasjon sammen med ordre. Bruken av denne informasjonen avhenger imidlertid av **Shopify-kundemaler** og innstillinger i feltet **Kundetildelingstype**.|
|**Kundetildelingstype**|Definer hvordan du vil at koblingen skal utføre tildelingen.<br>- **Via e-post/telefon** hvis du vil at koblingen skal tildele importert Shopify-kunde til eksisterende kunde i [!INCLUDE[prod_short](../includes/prod_short.md)] via e-post og telefon.</br>- **Etter faktura til-informasjon** hvis du vil at koblingen skal bruke adressen til fakturamottakeren til å tildele importert Shopify-kunden til en eksisterende kunde i [!INCLUDE[prod_short](../includes/prod_short.md)].</br>- Velg **Ta alltid med standard kunde** hvis du vil at systemet skal bruke en kunde fra **Standard kundenr.** . |
|**Shopify kan oppdatere kunder**| Velg dette feltet om du vil at koblingen skal oppdatere kundene den finner, når alternativene **Via e-post/telefon** eller **Etter faktura til-informasjon** er valgt i feltet **Kundetildelingstype**.|
|**Opprett ukjente kunder automatisk**| Velg dette feltet om du vil at koblingen skal opprette manglende kunder som blir funnet, når alternativene **Via e-post/telefon** eller **Etter faktura til-informasjon** er valgt i feltet **Kundetildelingstype**. En ny kunde opprettes ved hjelp av importerte data og **Kundemalkode** som er definert på sidene **Shopify-butikkort** eller **Shopify-kundemal**. Legg merke til at Shopify-kunden må ha minst én adresse. Ordrer som er opprettet via Shopify-salgsstedssalgskanalen, mangler ofte adresseopplysninger. Hvis dette alternativet ikke er aktivert, må du opprette en kunde manuelt og knytte det til Shopify-kunden.|
|**Kundemalkode**|Dette feltet brukes sammen med **Opprett ukjente kunder automatisk**.<br>- Velg standardmalen som skal brukes for automatisk opprettede kunder. Kontroller at den valgte malen inneholder de obligatoriske feltene, for eksempel **Bokføringsgruppe – firma**, **Bokføringsgruppe – kunde**, merverdiavgiftsrelaterte (mva.) eller avgiftsrelaterte felter.<br>- Du kan definere maler per land/område på siden **Shopify-kundemaler**, som er nyttig for å kunne foreta en riktig beregning av mva. <br>- Finn ut mer under [Definer avgifter](setup-taxes.md).|

### <a name="customer-template-per-country"></a>Kundemal per land

Enkelte innstillinger kan defineres på nivået land/område, eller på nivået delstat/provins. Innstillingene kan konfigureres i [Forsendelse og levering](https://www.shopify.com/admin/settings/shipping) i Shopify.

Du kan gjøre følgende for hver kunde ved å bruke **Shopify-kundemalen**:

1. Angi **Standard kundenr.**, som har høyere prioritet over det som er valgt i feltene **Kundeimport fra Shopify** og **Kundetildelingstype**. Den brukes i den importerte ordren.
2. Definere **kundemalkoden**, som brukes til å opprette manglende kunder, hvis **Opprett ukjente kunder automatisk** er aktivert. Hvis **kundemalkoden** er tom, bruker funksjonen **kundemalkoden** som er definert på **Shopify-butikkort**. Systemet prøver først å finne en mal for **fylkes-/områdekode** for standardadressen. Hvis det ikke finnes noen mal, brukes den første adressen.
3. I noen tilfeller er ikke **kundemalkoden** som er definert for et land, nok til å sikre riktig avgiftsberegninger (f.eks. for land med mva.). I dette tilfellet kan det være nyttig å ta med **avgiftsområde**.
4. **Avgiftsområde**-feltet inneholder også et par for **landskode** og **fylkesnavn**. Dette paret er nyttig når koblingen må konvertere en kode til et navn, eller omvendt.

> [!NOTE]  
> Landkodene er ISO 3166-1 for alpha-2-landkoder. Finn ut mer under [Landskode](https://help.shopify.com/en/api/custom-storefronts/storefront-api/reference/enum/countrycode).

## <a name="export-customers-to-shopify"></a>Eksporter kunder til Shopify

Du kan eksportere eksisterende kunder til Shopify samtidig. I hvert tilfellet opprettes det en kunde og én standardadresse. Du kan administrere prosessen ved å bruke følgende innstillinger:

|Felt|Beskrivelse|
|------|-----------|
|**Eksporter kunder til Shopify**|Velg dette alternativet hvis du planlegger å eksportere alle kunder fra [!INCLUDE[prod_short](../includes/prod_short.md)] til Shopify samtidig. Du kan gjøre det manuelt ved hjelp av handlingen **Synkroniser kunder** eller automatisk ved å bruke en jobbkø for regelmessige oppdateringer.<br> Når du eksporterer kunder med adresser som omfatter provinser/stater, må du passe på at **ISO-koden** er fylt ut for land/områder.|
|**Kan oppdatere Shopify-kunder**|Dette brukes sammen med innstillingen **Eksporter kunde til Shopify**. Aktiver dette alternativet hvis du vil generere oppdateringer senere [!INCLUDE[prod_short](../includes/prod_short.md)] for kunder som allerede finnes i Shopify.|

Følgende er krav for å eksportere en kunde:

* Kunden må ha en gyldig e-postadresse.
* Land/område er valgt på kundekortet, for lokale kunder, med tomt land/område som er angitt på siden **Selskapsopplysninger**, må ha en definert ISO-kode.
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

For adresser der land/område brukes, velger du **Kode** eller **Navn** i feltet **Fylkeskilde** på siden **Shopify-butikkortet**. Koden eller navnet angir datatypen som er lagret i [!INCLUDE[prod_short](../includes/prod_short.md)] i feltet **Fylke**. Husk å starte kundemaler per land, slik at landskode/navnetildeling er klar. 


## <a name="sync-customers"></a>Synkroniser kunder

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Shopify-butikk** og velger den relaterte koblingen.
2. Velg den bestemte butikken du vil synkronisere kunder med.
3. Velg handlingen **Synkroniser kunder**.

Du kan også bruke handlingen **Start kundesynkronisering** i vinduet **Shopify-kunder** eller søk etter den satsvise jobben **Synkroniser kunder**.

Du kan planlegge at oppgaven skal utføres på en automatisk måte. Finn ut mer under [Planlegg gjentakende oppgaver](background.md#to-schedule-recurring-tasks).

## <a name="see-also"></a>Se også

[Kom i gang med koblingen for Shopify](get-started.md)  
