---
title: Anskaff aktiva
description: 'Du kan definere et aktivum, tilordne et avskrivningstablå og registrere anskaffelseskosten for aktivumet.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: purchase fixed asset
ms.search.form: '5605, 5551, 5600, 5628, 5629, 5633'
ms.date: 05/15/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="acquire-fixed-assets"></a>Anskaff aktiva

 **Bruk siden Aktivakort** til å angi opplysninger om et aktiva. Du kan definere bygninger eller produksjonsutstyr som hovedaktiva i en komponentoversikt, og du kan gruppere dem på forskjellige måter, som etter klasse, avdeling eller lokasjon. Du må definere og tilordne et avskrivningstablå til hvert aktiva før du kan anskaffe det.

Når du har definert et aktiva og tilordnet et avskrivningstablå, må du anskaffe aktivaet. For å anskaffet et aktiva registrerer du anskaffelseskosten i den relevante finanskontoen, bankkontoen eller leverandøren ved å bokføre en anskaffelsestransaksjon fra **Aktiva finanskladd**-siden. Du kan bruke **Assistert aktivaanskaffelse**-siden for å opprette og bokføre de nødvendige finanskladdelinjene automatisk.

Bruk indeksregulering til å justere verdier for generelle endringer i prisnivået. Bruk kjørselen **Indeksreg. aktiva** til å beregne anskaffelseskostnader og erstatningskostnader.

## <a name="add-a-fixed-asset-to-your-list-of-fixed-assets"></a>Legge til et aktiva i listen over aktiva

Før du kan anskaffe et aktiva, må du legge det til i aktivalisten. Du kan legge til aktiva i listen på flere måter:

* Angi informasjon om aktivaene på **siden Aktivakort** .
* Bruk handlingen **Rediger i Excel** til å laste ned listen over aktiva til et regneark, legge til nye aktiva i listen og deretter publisere oppdateringen til [!INCLUDE [prod_short](includes/prod_short.md)].
* Bruke en bestilling til å legge til ressurser.
* Bruk handlingen **Kopier aktiva** .

Når du har lagt til aktiva i listen, er neste trinn å anskaffe dem, slik at du kan bruke dem i transaksjoner. Finn ut mer på [Anskaffe et aktiva](#acquire-fixed-assets).

### <a name="add-a-fixed-asset-on-the-fixed-asset-card-page"></a>Legge til et aktiva på siden Aktivakort

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Aktiva**, og velg deretter den relaterte koblingen.  
2. Velg **Ny**, og deretter fyller du ut feltene i **Generelt**-hurtigfanen etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. På hurtigfanen **Avskrivningstablå** fyller du ut feltene etter behov. Dette trinnet tilordner et avskrivningstablå til aktivaet.  
4. Hvis du vil tilordne mer enn ett avskrivningstablå til aktivaet, velger du **Legg til flere avskrivningstablåer**. Hvis du vil vite mer, kan du gå til [Slik tilordner du et avskrivningstablå til et aktiva](fa-how-setup-depreciation.md#to-assign-a-depreciation-book-to-a-fixed-asset).

    Når du har fylt ut de nødvendige feltene, vises **vises Du er klar til å kjøpe aktivaet.** Varselet vises øverst på siden. Hvis du er klar til å anskaffe innholdselementet nå, velger du handlingen **Hent** . Følg trinnene på **siden Assistert aktivaanskaffelse** for å fullføre anskaffelsen. Hvis du ikke er klar, kan du alltid kjøpe eiendelen senere.

### <a name="use-edit-in-excel-to-add-assets"></a>Bruke Rediger i Excel til å legge til aktiva

Hvis du vil legge til mange aktiva, er Rediger i Excel et flott verktøy å bruke. Verktøyet laster ned den gjeldende aktivalisten i et regneark som inneholder de fleste feltene som er tilgjengelige på siden Aktivakort. Du kan fylle ut noen av eller alle feltene på raden for hvert innholdselement, og publisere endringene for å legge dem til i listen [!INCLUDE [prod_short](includes/prod_short.md)]. Hvis du ikke kan fylle ut alle obligatoriske felt, er det greit. Du kan oppdatere dem når [!INCLUDE [prod_short](includes/prod_short.md)] du er klar.

> [!NOTE]
> Hvis du vil bruke handlingen Rediger i Excel, må du ha Office-tillegget Microsoft Dynamics installert. Tillegget oppretter koblingen mellom Excel og [!INCLUDE [prod_short](includes/prod_short.md)]. Hvis du vil ha mer informasjon, kan du gå til [Få Business Central-tillegget for Excel](admin-deploy-excel-addin.md).

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Aktiva**, og velg deretter den relaterte koblingen.
2.  :::image type="content" source="media/share-icon.png" alt-text="Velg ikonet Del denne siden med andre brukere eller apper."::: -ikonet, og velg **deretter Rediger i Excel**.
3. Åpne den nedlastede filen, og skriv inn informasjon om de nye aktivaene.

   > [!TIP]
   > Du trenger ikke å angi en identifikator i nummeret **.** . Når du publiserer oppdateringen, [!INCLUDE [prod_short](includes/prod_short.md)]  tilordnes det en identifikator basert på nummerserien du bruker for aktiva.

4. Hvis du vil oppdatere [!INCLUDE [prod_short](includes/prod_short.md)], velger du **Microsoft Dynamics** Publiser **i** ruten.

### <a name="add-a-fixed-asset-from-a-purchase-order-or-invoice"></a>Legge til et aktiva fra en bestilling eller faktura

Trinnene nedenfor beskriver hvordan du legger til et aktiva fra en bestilling. Fremgangsmåten er den samme for en kjøpsfaktura.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Bestillinger**, og velg deretter den relaterte koblingen.
2. Velg **Ny** for å opprette en ny bestilling.
3. Fyll ut feltene i hurtigfanen **Generelt** etter behov. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)]
4. Velg Aktiva **i Type-feltet**  **på** hurtigfanen Linjer. **·**
5. I **Nr.** -feltet, velger du enten et eksisterende aktiva for å legge til en utgift, eller velger **Ny** for å legge til et nytt aktiva.
6. Når du har angitt opplysningene for det nye aktivaet og bestillingen, velger du **Bokfør**.

## <a name="acquire-a-fixed-asset-by-using-a-fixed-asset-gl-journal"></a>Anskaffe et aktiva ved hjelp av en aktivafinanskladd

Fremgangsmåten nedenfor beskriver hvordan du anskaffer ved å opprette og bokføre de nødvendige finanskladdelinjene for aktiva. Du kan også opprette og bokføre kladdelinjene manuelt. Hvis du vil ha mer informasjon, kan du gå til [Anskaffe et aktiva ved hjelp av en aktivafinanskladd](#acquire-a-fixed-asset-by-using-a-fixed-asset-gl-journal).

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Aktiva**, og velg deretter den relaterte koblingen.
1. Velg aktivaet du vil anskaffe, og velg deretter handlingen **Hent** .
1. Følg trinnene på **siden Assistert aktivaanskaffelse** for å fullføre anskaffelsen.

> [!NOTE]  
> Du kan også bokføre anskaffelseskosten som et kreditbeløp. Husk i så fall at verdien i **Anskaffelseskost inkl. mva**-feltet må ha et minustegn for å angi et kreditbeløp.

Når du velger **Fullfør**, fylles feltet **Bokført verdi** ut på **siden Aktivakort**, som angir at aktivaet ble anskaffet til den angitte anskaffelseskosten.  

## <a name="to-post-a-fixed-asset-acquisition-manually-with-a-fixed-asset-gl-journal"></a>Slik bokfører du en aktivaanskaffelse manuelt med en aktivafinanskladd:

Følgende fremgangsmåte beskriver hvordan du anskaffer et aktiva manuelt ved å opprette og bokføre linjer på **Aktiva finanskladd**-siden. Du kan også anskaffe et aktiva automatisk på **siden Aktivakort** ved å velge **handlingen Hent aktiva** . Hvis du vil vite mer, kan du gå til [Anskaffe et aktiva](#acquire-fixed-assets).

> [!NOTE]  
> Du kan også bokføre anskaffelseskosten som et kreditbeløp. Husk i så fall at verdien i **Beløp**-feltet må ha et minustegn for å angi et kreditbeløp.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Aktivafinanskladder** og velger den relaterte koblingen.
2. På **Aktiva finanskladd**-siden i **Aktivabokf.type**-feltet velger du **Anskaffelseskost**.
3. Fyll ut feltene som gjenstår, etter behov.
4. Velg handlingen **Bokfør**.  

> [!TIP]  
> Hvis du fyller ut forsikringsnummeret **.**  [!INCLUDE[prod_short](includes/prod_short.md)] -feltet bokfører også anskaffelseskosten for aktivaet i forsikringsdekningsposten. Hvis du vil vite mer, kan du gå til [Forsikre aktiva](fa-how-insure.md).

## <a name="to-set-up-a-component-list-for-a-main-asset"></a>Slik definerer du en komponentoversikt for et hovedaktiva:

Du kan gruppere aktiva i hovedaktiva og komponenter i hovedaktivaene. Det kan for eksempel tenkes at du har en produksjonsmaskin som består av flere deler som du vil gruppere på denne måten.  

Du må definere hovedaktivaet og alle komponentene som individuelle aktiva. Når du har definert en komponentoversikt, [!INCLUDE[prod_short](includes/prod_short.md)]  fylles feltene **Hovedaktiva/komponent** og **Komponenter til hovedaktiva** automatisk ut i aktivaene.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Aktiva**, og velg deretter den relaterte koblingen.
2. Velg aktivaet som er hovedaktivaet, og velg deretter **Hovedaktivakomponenter**-handlingen.
3. På siden **Hovedaktivakomponenter** velger du feltet **Aktivanr.** og velger deretter aktivaet du vil legge til som en komponent av hovedaktivaet.
4. Lukk siden.
5. Gjenta trinnene 3 og 4 for hvert komponentaktiva som du vil legge til.
6. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Aktivaoppsett** og velger den relaterte koblingen.
7. Aktiver veksleknappen **Tillat bokføring til hovedaktiva** .

## <a name="to-cancel-an-acquisition-cost-posting-for-one-fixed-asset"></a>Slik kansellerer du en anskaffelseskostbokføring for ett aktiva:

Hvis du gjør en feil når du bokfører en anskaffelseskostnad, kan du fjerne posten via kjørselen **Kanseller aktivaposter** og deretter bokføre den riktige anskaffelsesposten. Feilaktige poster overføres til **Aktivafeilposter**-siden.

Hvis du for eksempel bokfører en anskaffelse med feil dato, må du korrigere den så snart som mulig fordi aktivabokføringsdatoen brukes for mange beregninger.

> [!IMPORTANT]  
> Du kan ikke bruke handlingen **Tilbakefør transaksjon** for aktivaposter.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , skriv inn **Aktivaposter**, og velg deretter den relaterte koblingen.  
2. På siden **Aktivaposter** velger du posten eller postene du vil kansellere.  
3. Velg menyen **Handlinger**, og velg deretter handlingen **Kanseller poster**.
4. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Velg **OK**-knappen for å kjøre kjørselen.
6. Når feil post eller poster er kansellert, fortsetter du med å bokføre riktig anskaffelseskost.

## <a name="to-post-the-salvage-value-together-with-the-acquisition-cost"></a>Slik bokfører du skrapverdien sammen med anskaffelseskosten:

Skrapverdien er restverdien for et aktiva som ikke lenger kan brukes. Du kan bokføre skrapverdien samtidig som du bokfører anskaffelseskosten. Hvis du vil ha mer informasjon, kan du gå til [Avskrive eller amortisere aktiva](fa-how-depreciate-amortize.md).

Du kan bokføre skrapverdien sammen med anskaffelseskosten fra en aktivakladd.

> [!NOTE]
> Denne prosessen krever kanskje at du tilpasser tabellen Aktivakladder ved å legge til feltet Skrapverdi. Som standard vises ikke feltet på siden. Hvis du vil vite mer, kan du gå til [Tilpasse arbeidsområdet](ui-personalization-user.md).

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Aktivakladder** og velger den relaterte koblingen.
2. På siden **Aktivakladder** oppretter du anskaffelseslinjen. Hvis du vil ha mer informasjon, kan du gå til [Slik bokfører du en aktivaanskaffelse manuelt med en aktivafinanskladd](#to-post-a-fixed-asset-acquisition-manually-with-a-fixed-asset-gl-journal).
3. I **Skrapverdi**-feltet på kladdelinjen angir du beløpet for skrapverdien som et kreditbeløp (med et minustegn foran, for eksempel **-** 100).
4. Velg handlingen **Bokfør**.

> [!NOTE]
> Hvis det finnes en skrapverdi for et aktiva, brukes denne verdien i avskrivningsbokføring i stedet for verdien i **feltet Slutt bokført verdi** på **siden Aktivaavskrivningstablå** . Hvis du vil vite mer, kan du gå til [Slik administrerer du den bokførte sluttverdien](fa-how-depreciate-amortize.md#to-manage-the-ending-book-value).

## <a name="see-also"></a>Se også

[Aktiva](fa-manage.md)  
[Definer aktiva](fa-setup.md)  
[Utformingsdetaljer om ikke-fradragsberettiget mva-innvirkning på aktiva](design-details-nondeductible-vat.md)  
[Finans](finance.md)  
[Bli klar til å gjøre forretninger](ui-get-ready-business.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
