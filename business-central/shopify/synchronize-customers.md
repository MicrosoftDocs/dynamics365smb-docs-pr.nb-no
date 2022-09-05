---
title: Synkroniser kunder
description: Importer kunder fra eller eksporter til Shopify
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 30105, 30106, 30107, 30108, 30109,
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: d4ff86179fa5b82bcc398ee58cf92fc121c486d8
ms.sourcegitcommit: 38b1272947f64a473de910fe81ad97db5213e6c3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/29/2022
ms.locfileid: "9361425"
---
# <a name="synchronize-customers"></a>Synkroniser kunder

Når en ordre importeres fra Shopify, er det nødvendig å hente informasjonen om kunden for ytterligere behandling av dokumentet i [!INCLUDE[prod_short](../includes/prod_short.md)]. Det finnes to hovedalternativer for å gjøre dette, og kombinasjoner av disse:

* Bruk en spesiell kunde for alle ordrer.
* Importer faktiske kundeinformasjon fra Shopify. Dette alternativet er også tilgjengelig når du eksporterer kunder til Shopify fra [!INCLUDE[prod_short](../includes/prod_short.md)] først.

## <a name="how-the-connector-chooses-which-customer-to-use"></a>Slik velger koblingen hvilken kunde som skal brukes

*Import ordre fra Shopify*-funksjonen prøver å velge kunder i følgende rekkefølge:

1. Hvis **Standard kundenr.** feltet er definert i **Shopify-kundemalen** for det tilsvarende landet, brukes deretter **Standard kundenr.** uavhengig av innstillingene i feltene **Kundeimport fra Shopify** og **Kundetildeling**. Finn ut mer under [Kundemal per land](synchronize-customers.md#customer-template-per-country).
2. Hvis **Kundeimport fra Shopify** er angitt til *Ingen* og **Standard kundenr.** er definert på siden **Shopify-butikkort**, brukes **Standard kundenr.** .

Neste trinn avhenger av **Kundetildelingstype**.

* Hvis det er **Ta alltid standardkunden**, bruker tilkoblingen deretter kunden som er definert i feltet **Standard kundenr.** på siden **Shopify-butikkort**.
* Hvis det er **Via e-post/telefon**, prøver koblingen å finne eksisterende kunde med ID først, deretter med e-post og så med telefonnummer. Hvis kunden ikke blir funnet, oppretter koblingen en ny kunde.
* Hvis det er **Etter faktura til-informasjon**, prøver koblingen å finne eksisterende kunde med ID først og deretter etter faktura til-adresseinformasjon. Hvis kunden ikke blir funnet, oppretter koblingen en ny kunde.

> [!NOTE]  
> Koblingen bruker opplysninger fra faktura til-adresse og oppretter faktura til-kunde i [!INCLUDE[prod_short](../includes/prod_short.md)]. Salg til-kunden er den samme som faktura til-kunden.

## <a name="important-settings-when-importing-customers-from-shopify"></a>Viktige innstillinger når du importerer kunder fra Shopify

Enten du importerer kunder fra Shopify samtidig eller på samme tid som du importerer ordrer, kan du styre prosessen med følgende innstillinger:

|Felt|Description|
|------|-----------|
|**Kundeimport fra Shopify**|Velg **Alle kunder** hvis du har tenkt å importere kunder fra Shopify samtidig, enten manuelt ved hjelp av **Synkroniser kunder**-handling eller via jobbkø for regelmessige oppdateringer. Uansett hvilket utvalg du velger, importeres alltid kundeinformasjon sammen med ordre. Bruken av denne informasjonen avhenger imidlertid av **Shopify-kundemaler** og innstillinger i feltet **Kundetildelingstype**.|
|**Kundetildelingstype**|Definer hvordan du vil at koblingen skal utføre tildelingen.<br>- **Via e-post/telefon** hvis du vil at koblingen skal tildele importert Shopify-kunde til eksisterende kunde i [!INCLUDE[prod_short](../includes/prod_short.md)] via e-post og telefon.</br>- **Etter faktura til-informasjon** hvis du vil at koblingen skal bruke adressen til fakturamottakeren til å tildele importert Shopify-kunden til en eksisterende kunde i [!INCLUDE[prod_short](../includes/prod_short.md)].</br>- Velg **Ta alltid med standard kunde** hvis du vil at systemet skal bruke en kunde fra **Standard kundenr.** . |
|**Shopify kan oppdatere kunder**| Velg dette feltet om du vil at koblingen skal oppdatere kundene den finner, når alternativene **Via e-post/telefon** eller **Etter faktura til-informasjon** er valgt i feltet **Kundetildelingstype**.|
|**Opprett ukjente kunder automatisk**| Velg dette feltet om du vil at koblingen skal opprette manglende kunder som blir funnet, når alternativene **Via e-post/telefon** eller **Etter faktura til-informasjon** er valgt i feltet **Kundetildelingstype**. En ny kunde opprettes ved hjelp av importerte data og **Kundemalkode** som er definert på sidene **Shopify-butikkort** eller **Shopify-kundemal**. Legg merke til at Shopify-kunden må ha minst én adresse. Hvis dette alternativet ikke er aktivert, må du opprette en kunde manuelt og knytte det til Shopify-kunden. Du kan alltid starte oppretting av en kunde manuelt fra siden **Shopify-ordre**.|
|**Kundemalkode**|Dette feltet brukes sammen med **Opprett ukjente kunder automatisk**.<br>- Velg standardmalen som skal brukes for automatisk opprettede kunder. Kontroller at den valgte malen inneholder de obligatoriske feltene, for eksempel **Bokføringsgruppe – firma**, **Bokføringsgruppe – kunde**, merverdiavgiftsrelaterte (mva.) eller avgiftsrelaterte felter.<br>- Du kan definere maler per land/område på siden **Shopify-kundemaler**, som er nyttig for å kunne foreta en riktig beregning av mva. <br>- Finn ut mer under [Definer avgifter](setup-taxes.md).|

### <a name="customer-template-per-country"></a>Kundemal per land

Enkelte innstillinger kan defineres på nivået land/område, eller på nivået delstat/provins. Innstillingene kan konfigureres i [Forsendelse og levering](https://www.shopify.com/admin/settings/shipping) i Shopify.

Du kan gjøre følgende for hver kunde ved å bruke **Shopify-kundemalen**:

1. Angi **Standard kundenr.**, som har høyere prioritet over det som er valgt i feltene **Kundeimport fra Shopify** og **Kundetildelingstype**. Den brukes i den importerte ordren.
2. Definere **kundemalkoden**, som brukes til å opprette manglende kunder, hvis **Opprett ukjente kunder automatisk** er aktivert. Hvis **kundemalkoden** er tom, bruker funksjonen **kundemalkoden** som er definert på **Shopify-butikkort**.
3. Definere om priser skal inngå i mva./avgift for importerte ordrer.
4. I noen tilfeller er ikke **kundemalkoden** som er definert for et land, nok til å sikre riktig beregning av avgifter (f.eks. for land med mva.). I dette tilfellet kan det være nyttig å ta med **mva-områdene**.

> [!NOTE]  
> Landkodene er ISO 3166-1 for alpha-2-landkoder. Finn ut mer under [Landskode](https://help.shopify.com/en/api/custom-storefronts/storefront-api/reference/enum/countrycode).

## <a name="export-customers-to-shopify"></a>Eksporter kunder til Shopify

Eksisterende kunder kan eksporteres til Shopify samtidig. I hvert tilfellet opprettes det en kunde og én standardadresse. Du kan administrere prosessen ved å bruke følgende innstillinger:

|Felt|Description|
|------|-----------|
|**Eksporter kunder til Shopify**|Velg dette hvis du planlegger å eksportere alle kunder med en gyldig e-postadresse fra [!INCLUDE[prod_short](../includes/prod_short.md)] til Shopify samtidig. Du kan gjøre det manuelt ved hjelp av handlingen **Synkroniser kunder** eller automatisk ved å bruke en jobbkø for regelmessige oppdateringer.<br> Når du eksporterer kunder med adresser som omfatter provinser/stater, må du passe på at **ISO-koden** er fylt ut for land/områder.|
|**Kan oppdatere Shopify-kunder**|Dette brukes sammen med innstillingen **Eksporter kunde til Shopify**. Aktiver den hvis du vil generere oppdateringer senere [!INCLUDE[prod_short](../includes/prod_short.md)] for kunder som allerede finnes i Shopify.|

> [!NOTE]  
> Når du har opprettet kundene i Shopify, kan du sende dem direkteinvitasjoner og oppmuntre dem til å aktivere kontoene sine.

### <a name="populate-customer-information-in-shopify"></a>Fyll ut kundeinformasjon i Shopify

En kunde i Shopify har fornavn, etternavn, e-post eller telefonnummer. Du kan fylle ut fornavn og etternavn fra kundekortet i [!INCLUDE[prod_short](../includes/prod_short.md)].

|Prioritet|Felt i kundekort|Description|
|------|------|-----------|
|1|**Kontaktnavn**|Høyeste prioritet hvis feltet **Kontaktnavn** er fylt ut og feltet **Kontaktkilde** på **Shopify-butikkortet** inneholder et av alternativene *Fornavn og etternavn* eller *Etternavn og fornavn* for å definere hvordan verdiene skal deles.|
|2|**Navn 2**|Hvis feltet **Navn 2** er fylt ut og feltet **Navn 2-kilde** på **Shopify-butikkortet** inneholder alternativene *Fornavn og etternavn* eller *Etternavn og fornavn* for å definere hvordan verdiene skal deles.|
|3|**Navn**|Laveste prioritet hvis feltet **Navn** er fylt ut og feltet **Navnkilde** på **Shopify-butikkortet** inneholder alternativene *Fornavn og etternavn* eller *Etternavn og fornavn* for å definere hvordan verdiene skal deles.|

En kunde i Shopify har også en standardadresse, som kan inneholde et selskap og en adresse i tillegg til fornavn, etternavn, e-post eller telefon. Du kan fylle ut **Selskap**- feltet basert på data fra kundekortet i [!INCLUDE[prod_short](../includes/prod_short.md)].

|Prioritet|Felt i kundekort|Description|
|------|------|-----------|
|1|**Navn**|Høyeste prioritet hvis feltet **Navnekilde** på **Shopify-butikkortet** inneholder *Selskapsnavn*.|
|2|**Navn 2**|Laveste prioritet hvis feltet **Navn 2-kilde** på **Shopify-butikkortet** inneholder *Selskapsnavn*.|

For adresser der land/område brukes, velger du *Kode* eller *Navn* i feltet **Landkilde** på **Shopify-butikkortet**. Dette angir datatypen som er lagre i [!INCLUDE[prod_short](../includes/prod_short.md)] i feltet **Land**.

## <a name="sync-customers"></a>Synkroniser kunder

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Shopify-butikk** og velger den relaterte koblingen.
2. Velg den bestemte butikken du vil synkronisere kunder med.
3. Velg handlingen **Synkroniser kunder**.

Du kan også bruke handlingen **Start kundesynkronisering** i vinduet **Shopify-kunder** eller søk etter den satsvise jobben **Synkroniser kunder**.

Du kan planlegge at oppgaven skal utføres på en automatisk måte. Finn ut mer under [Planlegg gjentakende oppgaver](background.md#to-schedule-recurring-tasks).

## <a name="see-also"></a>Se også

[Kom i gang med koblingen for Shopify](get-started.md)  
