---
title: Definer generell aktivainformasjon
description: 'Før du kan arbeide med aktiva, må du definere standard finanskonti, bokføringsgrupper, fordelingsnøkler, kladdemaler og kladder samt klassekoder.'
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '5623, 5615, 5661, 5662, 5627, 5616, 5620, 5629, 5633, 5609, 5631, 5630, 5617, 5612, 5613, 5608, 5609, 5635, 9277'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="set-up-general-fixed-assets-information"></a><a name="set-up-general-fixed-assets-information"></a>Definere generell aktivainformasjon

Før du kan behandle aktiva, må du definere standard finanskonti, fordelingsnøkler, kladdemaler og kladder for aktivabokføring og -reklassifisering, og du kan klassifisere aktiva i klasser, for eksempel materielle og immaterielle.

## <a name="to-set-up-general-default-values-for-fixed-assets"></a><a name="to-set-up-general-default-values-for-fixed-assets"></a>Slik definerer du generelle standardverdier for aktiva

Du definerer den generelle virkemåten eller aktivafunksjonaliteten og bilagsnummerserien på **Aktivaoppsett**-siden.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Aktivaoppsett** og velger den relaterte koblingen.  
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-fixed-asset-posting-groups"></a><a name="to-set-up-fixed-asset-posting-groups"></a>Slik definerer du bokføringsgrupper for aktiva:

Du bokfører grupper for å definere aktivagrupper. Poster for disse bokføringsgruppene bokføres på de samme finanskontiene.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Bokføringsgrupper – aktiva**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**.
3. Fyll ut resten av feltene på siden **Kort for bokf.grp.- aktiva** etter behov.

    > [!NOTE]  
    >   For å sikre at motkontoer for ulike aktivabokføringer settes inn automatisk når du velger handlingen **Sett inn aktivamotkonto** på kladdelinjer, følger du det neste trinnet, basert på oppskrivningsbokføring.
4. I hurtigfanen **Motkonto** i feltet **Motkonto for oppskrivning** velger du til hvilken finanskonto du vil bokføre motposter for oppskrivning.

Hvis du vil ha mer informasjon om hvordan du bruker handlingen **Sett inn aktivamotkonto** på aktivafinanskladdelinjer, kan du for eksempel se [Revaluere aktiva](fa-how-revalue.md).

## <a name="to-set-up-fixed-asset-allocation-keys"></a><a name="to-set-up-fixed-asset-allocation-keys"></a>Slik definerer du aktivafordelingsnøkler:

Ved hjelp av brukerdefinerte fordelingsnøkler kan du fordele transaksjoner på ulike avdelinger eller prosjekter. Du kan for eksempel definere en fordelingsnøkkel som fordeler avskrivningskostnader på biler med 35 prosent til administrasjonsavdelingen og 65 prosent til salgsavdelingen. Hvis du vil ha mer informasjon, kan du se [Fordele kostnader og inntekter](year-allocate-costs-income.md).

Fordelingsnøkler gjelder for aktivaklasser, ikke for individuelle aktiva.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Bokføringsgrupper – aktiva**, og velg deretter den relaterte koblingen.  
2. På siden **Bokf.grupper - aktiva** velger du handlingen **Fordelinger**, og velger deretter en bokføringstype.
3. På siden **Aktiva - fordelinger** fyller du ut feltene etter behov.
4. Gjenta trinn 2 og 3 for bokføringstypene du vil definere fordelingsnøkler for.

## <a name="to-set-up-fixed-asset-journal-templates"></a><a name="to-set-up-fixed-asset-journal-templates"></a>Slik definerer du aktivakladdemaler:

En mal er et forhåndsdefinert oppsett for en kladd. Malen inneholder opplysninger om sporingskoder, rapporter og nummerserier. Hvis du vil ha mer informasjon, kan du se [Arbeide med finanskladder](ui-work-general-journals.md).

[!INCLUDE[prod_short](includes/prod_short.md)] oppretter automatisk en aktivakladdemal første gang du åpner **Aktivakladd**-siden, men du kan definere flere kladdemaler.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Aktivakladdemaler**, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene etter behov.

## <a name="to-set-up-fixed-asset-journal-batches"></a><a name="to-set-up-fixed-asset-journal-batches"></a>Slik definerer du aktivakladder:

Du kan definere flere kladder, som vil si individuelle kladder for hver enkelt kladdemal. Ansatte kan for eksempel ha egne kladder der initialene til de ansatte brukes som kladdenavn. Hvis du vil ha mer informasjon, kan du se [Arbeide med finanskladder](ui-work-general-journals.md).  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Aktivakladdemaler**, og velg deretter den relaterte koblingen.  
2. Velg den aktuelle kladdemalen, og velg deretter **Kladder**-handlingen.
3. På siden **Aktivakladder** fyller du ut feltene etter behov.

## <a name="to-set-up-fixed-asset-reclassification-journal-templates"></a><a name="to-set-up-fixed-asset-reclassification-journal-templates"></a>Slik definerer du aktivareklassifiseringskladdemaler:

Du kan bruke dedikerte reklassifiseringskladder når du skal overføre, dele opp og knytte sammen aktiva. [!INCLUDE[prod_short](includes/prod_short.md)] oppretter automatisk en aktivareklassifiseringskladdemal første gang du åpner **Aktivareklass.kladd**-siden, men du kan definere flere reklassifiseringskladdemaler. Hvis du vil ha mer informasjon, kan du se [Arbeide med finanskladder](ui-work-general-journals.md).  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Kladdemaler for aktivareklassifisering**, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene etter behov.

## <a name="to-set-up-fixed-asset-reclassification-journal-batches"></a><a name="to-set-up-fixed-asset-reclassification-journal-batches"></a>Slik definerer du aktivareklassifiseringskladder:

Du kan definere flere kladder, som vil si individuelle kladder for hver reklassifiseringskladd. Ansatte kan for eksempel ha egne kladder for reklassifisering der initialene til den ansatte brukes som reklassifiseringskladdenavn. Hvis du vil ha mer informasjon, kan du se [Arbeide med finanskladder](ui-work-general-journals.md).

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Kladdemaler for aktivareklassifisering**, og velg deretter den relaterte koblingen.  
2. Velg den aktuelle kladdemalen, og velg deretter **Kladder**-handlingen.
3. På siden **Aktivareklass.kladder** fyller du ut feltene etter behov.

## <a name="to-set-up-fixed-asset-class-codes"></a><a name="to-set-up-fixed-asset-class-codes"></a>Slik definerer du aktivaklassekoder:

Aktivaklassekoder kan brukes til å gruppere aktiva, for eksempel i materielle og immaterielle aktiva.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Aktivaklasser**, og velg deretter den relaterte koblingen.
2. Angi koder og navn for klassene du vil opprette.

## <a name="to-set-up-fixed-asset-subclass-codes"></a><a name="to-set-up-fixed-asset-subclass-codes"></a>Slik definerer du aktivaunderklassekoder:

Du bruker aktivaunderklassekodene til å gruppere aktiva i kategorier, for eksempel bygninger, kjøretøy, møbler eller maskiner.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Aktivaunderklasser**, og velg deretter den relaterte koblingen.
2. Angi koder og navn for klassene du vil opprette.

## <a name="to-set-up-fixed-asset-location-codes"></a><a name="to-set-up-fixed-asset-location-codes"></a>Slik definerer du aktivalokasjonskoder:

Du bruker aktivalokasjonskoder til å registrere aktivalokasjonen, for eksempel salgsavdeling, resepsjon, administrasjon, produksjon eller lager. Denne informasjonen er nyttig for forsikrings- og lagerformål.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Aktivalokasjoner**, og velg deretter den relaterte koblingen.
2. Angi koder og navn for aktivalokasjonene du vil opprette.

## <a name="to-register-opening-entries"></a><a name="to-register-opening-entries"></a>Slik registrerer du åpningsposter

Hvis du bruker aktiva i [!INCLUDE[prod_short](includes/prod_short.md)] for første gang, må du først definere modulen Finans før du kan definere aktiva. Hvordan du gjør dette, avhenger av om aktiva er integrert med finans.  

 Bruk følgende fremgangsmåte hvis aktivatransaksjoner skal bokføres i Finans.  

1. Kontroller at du har fullført grunnleggende prosedyrer for oppsett av aktiva.  
2. Opprett et aktivakort for hvert eksisterende aktiva.  
3. Opprett et aktivaavskrivningstabl for hvert avskrivningsformål (for eksempel skatteoppgaver og regnskap). Du må definere vilkår og betingelser for hvert avskrivningstablå, for eksempel integrasjon med Finans.  

    Aktiver integrering med Finans ved å følge de neste trinnene. Kontroller først at Finans-integreringen deaktiveres for alle avskrivningstablåer, bokføre deretter åpningsposter og aktiver til slutt Finans-integrering.  
4. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Avskrivningstablåer**, og velg deretter den relaterte koblingen.  
5. Velg det aktuelle avskrivningstablåkortet, og velg deretter **Rediger**-handlingen for å åpne siden **Avskrivningstablåkort**.
6. På hurtigfanen **Integrering** må du kontrollere at alle feltene er tomme ved å fjerne alle haker. Hvis du har mer enn ett avskrivningstablå, deaktiverer du integrasjon med Finans for hvert enkelt tablå.  
7. Skriv inn følgende linjer for hvert aktivum i aktivakladden:
   * En linje med anskaffelseskosten.
   * En linje med den akkumulerte avskrivningen til slutten av forrige regnskapsår.
   * En linje med den akkumulerte avskrivningen fra begynnelsen av gjeldende regnskapsår til datoen som [!INCLUDE[prod_short](includes/prod_short.md)] har angitt for å starte beregningen av avskrivningen.

    Hvis du har andre åpningsbalanser, kan du også oppgi disse nå, for eksempel nedskrivning og oppskrivning.  
8. Når du har angitt og bokført kladdelinjene for hvert aktivum, aktiverer du integrasjon med Finans i avskrivningstablåene.

Hvis ikke aktivaene er integrert med Finans, hopper du over trinn 6 og 8.

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Se relatert [Microsoft-opplæring](/training/paths/set-up-fixed-assets-management/)

## <a name="see-also"></a><a name="see-also"></a>Se også

[Definer aktiva](fa-setup.md)  
[Aktiva](fa-manage.md)  
[Finans](finance.md)  
[Bli klar til å gjøre forretninger](ui-get-ready-business.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
