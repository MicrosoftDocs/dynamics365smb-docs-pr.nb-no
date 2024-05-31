---
title: Definer generell aktivainformasjon
description: 'Før du kan arbeide med aktiva, må du definere standard finanskonti, bokføringsgrupper, fordelingsnøkler, kladdemaler og kladder samt klassekoder.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.search.form: '5623, 5615, 5661, 5662, 5627, 5616, 5620, 5629, 5633, 5609, 5631, 5630, 5617, 5612, 5613, 5608, 5609, 5635, 9277'
ms.date: 03/25/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="set-up-general-fixed-assets-information"></a>Konfigurer generell aktivainformasjon

Før du kan administrere aktiva, må du definere standard finanskontoer, fordelingsnøkler og kladdemaler samt partier for å bokføre og klassifisere aktiva på nytt. Du kan også definere et klassifiseringshierarki (klasser og underklasser) for å strukturere ressursene og, om nødvendig, definere lokasjonene der du lagrer ressurser.

## <a name="to-set-up-general-behavior-for-fixed-assets-functionality"></a>Slik definerer du generelle virkemåte for aktivafunksjonalitet

Definer den generelle virkemåten til aktivafunksjonaliteten og bilagsnummerserien på siden **Aktivaoppsett**.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Aktivaoppsett** og velger den relaterte koblingen.  
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-fixed-asset-posting-groups"></a>Slik definerer du bokføringsgrupper for aktiva:

Bruk bokføringsgrupper for å definere aktivagrupper. Poster for disse bokføringsgruppene bokføres på de samme finanskontoene.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Bokføringsgrupper – aktiva**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**.
3. Fyll ut resten av feltene på siden **Kort for bokf.grp.- aktiva** etter behov.

    > [!NOTE]  
    >   For å sikre at motkontoer for ulike aktivabokføringer settes inn automatisk når du velger handlingen **Sett inn aktivamotkonto** på kladdelinjer, følger du det neste trinnet, basert på oppskrivningsbokføring.
4. I hurtigfanen **Motkonto** i feltet **Motkonto for oppskrivning** velger du til hvilken finanskonto du vil bokføre motposter for oppskrivning.

Hvis du vil ha mer informasjon om hvordan du bruker handlingen **Sett inn aktivamotkonto** på aktivafinanskladdelinjer, kan du se [Revaluer aktiva](fa-how-revalue.md).

## <a name="to-set-up-fixed-asset-journal-templates"></a>Slik definerer du aktivakladdemaler:

En mal er et forhåndsdefinert oppsett for en kladd. Malen inneholder opplysninger om sporingskoder, rapporter og nummerserier. Hvis du vil ha mer informasjon, kan du se [Arbeide med finanskladder](ui-work-general-journals.md).

[!INCLUDE[prod_short](includes/prod_short.md)] oppretter automatisk en aktivakladdemal første gang du åpner **Aktivakladd**-siden, men du kan definere andre kladdemaler.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Aktivakladdemaler**, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene etter behov.

## <a name="to-set-up-fixed-asset-class-and-subclass-codes"></a>Slik definerer du aktivaklasser og -underklassekoder

I aktiva kan du definere et klassifiseringshierarki som kan brukes til å gruppere aktiva. Hierarkiet har to nivåer: klasser og underklasser.

### <a name="fixed-asset-class-codes"></a>Aktivaklassekoder

Aktivaklasser er postene på øverste nivå i klassifiseringshierarkiet der du grupperer aktiva. Bruk for eksempel klasser til å dele aktiva i materielle eller immaterielle aktiva. Du må opprette minst én aktivaklasse i oppsettet.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Aktivaklasser**, og velg deretter den relaterte koblingen.
2. Angi koder og navn for aktivaklassene du vil opprette.

### <a name="fixed-asset-subclass-codes"></a>Koder for aktivaunderklasse

Aktivaunderklasser er postene på andre nivå i klassifiseringshierarkiet der du grupperer aktiva. Hver underklasse peker på en klasse på øverste nivå. Bruk aktivaunderklassekodene til å gruppere aktiva i mer bestemte kategorier, for eksempel bygninger, kjøretøy, møbler eller maskiner. Du må opprette minst én aktivaunderklasse i oppsettet.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Aktivaunderklasser**, og velg deretter den relaterte koblingen.
2. Angi koder og navn for aktivaunderklassene du vil opprette.

## <a name="start-to-register-assets"></a>Begynn å registrere aktiva

Hvis du bruker aktiva i [!INCLUDE[prod_short](includes/prod_short.md)] for første gang, må du først definere modulen Finans før du kan definere aktiva. Hvordan du gjør det, avhenger av om du integrerer aktiva med finans.  

Bruk følgende fremgangsmåte hvis aktivatransaksjoner skal bokføres i Finans.  

1. Fullføre de grunnleggende oppsettene for aktiva.  
2. Fyll ut et aktivakort for hvert eksisterende aktiva.  
3. Opprett et aktivaavskrivningstabl for hvert avskrivningsformål (for eksempel skatteoppgaver og regnskap). Definer vilkår og betingelser for hvert avskrivningstablå, for eksempel integrasjon med finans.

    Aktiver integrering med Finans ved å følge de neste trinnene. Kontroller først at finansintegreringen ikke er aktivert for alle avskrivningstablåer, bokfør deretter åpningsposter og aktiver til slutt finansintegrering.  
4. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Avskrivningstablåer**, og velg deretter den relaterte koblingen.  
5. Velg det aktuelle avskrivningstablåkortet, og velg deretter **Rediger**-handlingen for å åpne siden **Avskrivningstablåkort**.
6. Deaktiver alle veksleknappene på hurtigfanen **Integrering**. Hvis du har mer enn ett avskrivningstablå, gjentar du dette trinnet for hvert tablå.  
7. Skriv inn følgende linjer for hvert aktivum i aktivakladden:
   * En linje med anskaffelseskosten.
   * En linje med den akkumulerte avskrivningen til slutten av forrige regnskapsår.
   * En linje med den akkumulerte avskrivningen fra begynnelsen av gjeldende regnskapsår til datoen som [!INCLUDE[prod_short](includes/prod_short.md)] har angitt for å starte beregningen av avskrivningen.

    Hvis du har andre åpningsbalanser, kan du også oppgi disse nå, for eksempel nedskrivning og oppskrivning.  
8. Når du angir og bokfører kladdelinjene for hvert aktivum, aktiverer du integrasjon med Finans i avskrivningstablåene.

Hvis ikke aktivaene er integrert med finans, hopper du over trinn seks og åtte.

## <a name="to-set-up-fixed-asset-location-codes-optional"></a>Slik definerer du aktivalokasjonskoder (valgfritt)

Aktivalokasjonskoder definerer identifikatorer for hvor aktiva kan finnes, for eksempel salgsavdeling, resepsjon, administrasjon, produksjon eller lager. Du kan bruke dem til å registrere lokasjonen til et aktivum. Denne informasjonen er nyttig for forsikrings- og lagerformål.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Aktivalokasjoner**, og velg deretter den relaterte koblingen.
2. Angi koder og navn for aktivalokasjonene du vil opprette.

## <a name="to-set-up-fixed-asset-allocation-keys-optional"></a>Slik definerer du aktivafordelingsnøkler (valgfritt)

Bruk fordelingsnøkler til å fordele transaksjoner til ulike avdelinger eller prosjekter. Du kan for eksempel definere en fordelingsnøkkel som fordeler kjøretøyavskrivningskostnader med 35 prosent til administrasjonsavdelingen og 65 prosent til salgsavdelingen. Hvis du vil ha mer informasjon, kan du se [Fordele kostnader og inntekter](year-allocate-costs-income.md).

Fordelingsnøkler gjelder for aktivaklasser, ikke for individuelle aktiva.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Bokføringsgrupper – aktiva**, og velg deretter den relaterte koblingen.  
2. På siden **Bokf.grupper - aktiva** velger du handlingen **Fordelinger**, og velger deretter en bokføringstype.
3. På siden **Aktiva - fordelinger** fyller du ut feltene etter behov.
4. Gjenta trinn 2 og 3 for bokføringstypene du vil definere fordelingsnøkler for.

## <a name="to-set-up-fixed-asset-journal-batches-optional"></a>Slik definerer du aktivakladder (valgfritt)

Du kan definere flere kladder, som vil si individuelle kladder for hver enkelt kladdemal. Ansatte kan for eksempel ha egne kladder der initialene til de ansatte brukes som kladdenavn. Hvis du vil ha mer informasjon, kan du se [Arbeide med finanskladder](ui-work-general-journals.md).  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Aktivakladdemaler**, og velg deretter den relaterte koblingen.  
2. Velg den aktuelle kladdemalen, og velg deretter **Kladder**-handlingen.
3. På siden **Aktivakladder** fyller du ut feltene etter behov.

## <a name="to-set-up-fixed-asset-reclassification-journal-templates-optional"></a>Slik definerer du aktivareklassifiseringskladdemaler (valgfritt)

Bruk dedikerte reklassifiseringskladder til å overføre, dele opp og knytte sammen aktiva. [!INCLUDE[prod_short](includes/prod_short.md)] oppretter automatisk en aktivareklassifiseringskladdemal første gang du åpner siden **Aktivareklass.kladd**, men du kan definere andre reklassifiseringskladdemaler. Hvis du vil ha mer informasjon, kan du se [Arbeide med finanskladder](ui-work-general-journals.md).  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Kladdemaler for aktivareklassifisering**, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene etter behov.

## <a name="to-set-up-fixed-asset-reclassification-journal-batches-optional"></a>Slik definerer du aktivareklassifiseringskladder (valgfritt)

Du kan definere flere kladder, som vil si individuelle kladder for hver reklassifiseringskladd. Ansatte kan for eksempel ha egne kladder for reklassifisering der initialene til den ansatte brukes som reklassifiseringskladdenavn. Hvis du vil ha mer informasjon, kan du se [Arbeide med finanskladder](ui-work-general-journals.md).

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Kladdemaler for aktivareklassifisering**, og velg deretter den relaterte koblingen.  
2. Velg den aktuelle kladdemalen, og velg deretter **Kladder**-handlingen.
3. På siden **Aktivareklass.kladder** fyller du ut feltene etter behov.

## <a name="see-also"></a>Se også

[Definer aktiva](fa-setup.md)  
[Oversikt over aktiva](fa-manage.md)  
[Finans](finance.md)  
[Bli klar til å gjøre forretninger](ui-get-ready-business.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
