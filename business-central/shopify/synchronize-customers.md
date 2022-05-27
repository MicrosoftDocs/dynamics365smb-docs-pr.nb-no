---
title: Synkroniser kunder
description: Importer kunder fra eller eksporter til Shopify
ms.date: 05/11/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: 92ac46e9f7e69204b4c7edee4aa430a8786b6c0b
ms.sourcegitcommit: f071aef3660cc3202006e00f2f790faff849a240
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/18/2022
ms.locfileid: "8768159"
---
# <a name="synchronize-customers"></a>Synkroniser kunder

Når en ordre importeres fra Shopify, er informasjonen om kunden nødvendig for ytterligere behandling av dokumentet i [!INCLUDE[prod_short](../includes/prod_short.md)]. Det finnes to hovedalternativer og kombinasjoner av disse:

* Bruk spesiell kunde for alle ordrer.
* Importer faktiske kundeinformasjon fra Shopify. Dette alternativet er også tilgjengelig når du eksporterer kunde til Shopify fra [!INCLUDE[prod_short](../includes/prod_short.md)] først.

## <a name="how-connector-chooses-which-customer-to-use"></a>Slik velger koblingen hvilken kunde som skal brukes

*Import ordre fra Shopify*-funksjonen prøver å velge kunde i følgende rekkefølge:

1. Hvis **Standard kundenr.** er definert i **Shopify-kundemalen** for det tilsvarende landet, brukes deretter **Standard kundenr.** uavhengig av innstillingene i **Kundeimport fra Shopify** og **Kundetildeling**.
2. Hvis **Kundeimport fra Shopify** og **Standard kundenr.** er definert, brukes **Standard kundenr.** .

Neste trinn avhenger av **Kundetildelingstype**.

* **Ta alltid standardkunden** og bruk deretter kunden som er definert i feltet **Standard kundenr.** i vinduet **Shopify-butikkort**.
* **Via e-post/telefon** prøver koblingen å finne eksisterende kunde med ID først, deretter med e-post og så med telefon. Hvis kunden ikke blir funnet, oppretter koblingen en ny kunde.
* **Etter faktura til-informasjon** prøver koblingen å finne eksisterende kunde med ID først og deretter etter faktura til-adresseinformasjon. Hvis den ikke blir funnet, oppretter koblingen en ny kunde.

> [!NOTE]  
> Koblingen bruker opplysninger fra faktura til-adresse og oppretter faktura til-kunde i [!INCLUDE[prod_short](../includes/prod_short.md)]. Salg til-kunde er lik faktura faktura til-kunde.

## <a name="important-settings-when-importing-customers-from-shopify"></a>Viktige innstillinger når du importerer kunder fra Shopify

Enten du importerer kunder fra Shopify samtidig eller sammen med importen av ordrer, kan du styre prosessen med følgende innstillinger:

|Felt|Description|
|------|-----------|
|**Kundeimport fra Shopify**|Velg **Alle kunder** hvis du har tenkt å importere kunder fra Shopify samtidig, enten manuelt ved hjelp av **Synkroniser kunder**-handling eller via jobbkø for regelmessige oppdateringer. Uansett hvilket utvalg du velger, importeres alltid kundeinformasjon sammen med ordre. Bruken av denne informasjonen avhenger imidlertid av **Shopify-kundemaler** og innstillinger i feltet **Kundetildelingstype**.|
|**Kundetildelingstype**|Definer hvordan du vil at koblingen skal utføre tildelingen.<br>- **Via e-post/telefon** hvis du vil at koblingen skal tildele importert Shopify-kunde til eksisterende kunde i [!INCLUDE[prod_short](../includes/prod_short.md)] via e-post og telefon.</br>- **Etter faktura til-informasjon** hvis du vil at koblingen skal tildeles importert Shopify-kunden til eksisterende kunde i [!INCLUDE[prod_short](../includes/prod_short.md)] ved å bruke adresseinformasjon for parten som mottar fakturaen.</br>Velg **Ta alltid med standard kunde** hvis du vil at systemet skal bruke en kunde fra **Standard kundenr.** . |
|**Shopify kan oppdatere kunder**| Velg om du vil at koblingen skal oppdatere kunder som blir funnet, når alternativene **Via e-post/telefon** eller **Etter faktura til-informasjon** er valgt i feltet **Kundetildelingstype**.|
|**Opprett ukjente kunder automatisk**| Velg om du vil at koblingen skal opprette manglende kunder som blir funnet, når alternativene **Via e-post/telefon** eller **Etter faktura til-informasjon** er valgt i feltet **Kundetildelingstype**. En ny kunde opprettes ved hjelp av importerte data og **Kundemalkode** som er definert på sidene **Shopify-butikkort** eller **Shopify-kundemal**. Legg merke til at Shopify-kunden må ha minst én adresse. Hvis dette alternativet ikke er aktivert, må du opprette kunden manuelt og knytte det til Shopify-kunden. Du kan alltid starte oppretting av en kunde manuelt fra siden **Shopify-ordre**.|
|**Kundemalkode**|Brukes sammen med **Opprett ukjente kunder automatisk**.<br> Velg standardmalen som skal brukes for automatisk opprettede kunder. Du kan definere maler per land/område i vinduet **Shopify-kundemaler**, som er nyttig for å kunne foreta en riktig beregning av mva. Hvis du vil ha mer informasjon, kan du se [Avgiftsmerknader](synchronize-orders.md#tax-remarks).|

### <a name="customer-template-per-country"></a>Kundemal per land

Enkelte innstillinger kan defineres på nivået land/område, eller på nivået delstat/provins. Innstillingene kan konfigureres i [Forsendelse og levering](https://www.shopify.com/admin/settings/shipping) i Shopify.

**Shopify-kundemalen** gjør det mulig å gjøre følgende for hvert land:

1. Angi **Standard kundenr.**, som har høyere prioritet over det som er valgt i feltene **Kundeimport fra Shopify** og **Kundetildelingstype**. Den brukes i den importerte ordren.
2. Definere **kundemalkoden**, som brukes til å opprette manglende kunder, hvis **Opprett ukjente kunder automatisk** er aktivert. Hvis **kundemalkoden** er tom, bruker funksjonen **kundemalkode** som er definert på **Shopify-butikkort**.
3. I noen tilfeller er ikke **kundemalkode** per land nok til å sikre riktig beregning av mva. Det kan for eksempel være land med merverdiavgift.

> [!NOTE]  
> Landkodene er ISO 3166-1 for alpha-2-landkoder. Se [Landkode](https://help.shopify.com/en/api/custom-storefronts/storefront-api/reference/enum/countrycode) for mer informasjon.

## <a name="export-customers-to-shopify"></a>Eksporter kunder til Shopify

Eksisterende kunder kan eksporteres til Shopify samtidig. Resultatet er at en kunde og én standardadresse opprettes. Du kan behandle prosessen ved hjelp av følgende innstillinger:

|Felt|Description|
|------|-----------|
|**Eksporter kunder til Shopify**|Velg hvis du har tenkt å eksportere alle kunder med en gyldig e-postadresse fra [!INCLUDE[prod_short](../includes/prod_short.md)] til Shopify samtidig, enten manuelt ved hjelp av **Synkroniser kunder**-handling eller via jobbkø for regelmessige oppdateringer.|
|**Kan oppdatere Shopify-kunder**|Brukes sammen med **Eksporter kunde til Shopify**. Aktiver den hvis du vil generere oppdateringer senere [!INCLUDE[prod_short](../includes/prod_short.md)] for kunder som allerede finnes i Shopify.|

> [!NOTE]  
> Når du har opprettet kunder i Shopify, vil du kanskje sende direkteinvitasjoner til kunder. Det oppfordres til å aktivere kontoen.

### <a name="populate-customer-information-in-shopify"></a>Fyll ut kundeinformasjon i Shopify

En kunde i Shopify har fornavn, etternavn, e-post eller telefonnummer. Du kan fylle ut fornavnet og etternavnet basert på dataene fra kundekortet i [!INCLUDE[prod_short](../includes/prod_short.md)].

|Prioritet|Felt i kundekort|Description|
|------|------|-----------|
|1|**Kontaktnavn**|Høyeste prioritet hvis feltet **Kontaktnavn** er fylt ut og feltet **Kontaktkilde** på **Shopify-butikkortet** inneholder alternativene *Fornavn og etternavn* eller *Etternavn og fornavn*, som definerer hvordan verdiene skal deles.|
|2|**Navn 2**|Hvis feltet **Navn 2** er fylt ut og feltet **Navn 2-kilde** på **Shopify-butikkortet** inneholder alternativene *Fornavn og etternavn* eller *Etternavn og fornavn*, som definerer hvordan verdiene skal deles.|
|3|**Navn**|Laveste prioritet hvis feltet **Navn** er fylt ut og feltet **Navnkilde** på **Shopify-butikkortet** inneholder alternativene *Fornavn og etternavn* eller *Etternavn og fornavn*, som definerer hvordan verdiene skal deles.|

En kunde i Shopify har også en standardadresse, som i tillegg til fornavn, etternavn, e-post eller telefon kan inneholde firma og adresse. Du kan fylle ut **Selskap**- feltet basert på data fra kundekortet i [!INCLUDE[prod_short](../includes/prod_short.md)].

|Prioritet|Felt i kundekort|Description|
|------|------|-----------|
|1|**Navn**|Høyeste prioritet hvis feltet **Navnekilde** på **Shopify-butikkortet** inneholder *Selskapsnavn*.|
|2|**Navn 2**|Laveste prioritet hvis feltet **Navn 2-kilde** på **Shopify-butikkortet** inneholder *Selskapsnavn*.|

For adresser der land/område brukes, velger du *Kode* eller *Navn* i feltet **Landkilde** på **Shopify-butikkortet** for å angi hvilken type data som lagres i [!INCLUDE[prod_short](../includes/prod_short.md)] i feltet **Land**.

## <a name="sync-customers"></a>Synkroniser kunder

1. Gå til søkeikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Shopify-butikk**. Velg den relaterte koblingen.
2. Velg butikken du vil synkronisere kunder med for å åpne siden **Shopify-butikkort**.
3. Velg handlingen **Synkroniser kunder**.

Du kan også bruke handlingen **Start kundesynkronisering** i vinduet **Shopify-kunder** eller søk etter den satsvise jobben **Synkroniser kunder**.

## <a name="see-also"></a>Se også

[Kom i gang med koblingen for Shopify](get-started.md)  
