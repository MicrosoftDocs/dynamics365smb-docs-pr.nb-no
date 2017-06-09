---
title: Definere generell aktivainformasjon| Microsoft-dokumentasjon
description: Beskriver hvordan du setter opp systemet for administrasjon av aktiva.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/31/2016
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: bf5edf81ea0a95a3915588687d4222259970909c
ms.contentlocale: nb-no
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-set-up-general-fixed-assets-information"></a>Definere generell aktivainformasjon
Før du kan behandle aktiva, må du definere standard finanskonti, fordelingsnøkler, kladdemaler og kladder for aktivabokføring og -reklassifisering, og du kan klassifisere aktiva i klasser, for eksempel materielle og immaterielle.

## <a name="to-set-up-general-default-values-for-fixed-assets"></a>Slik definerer du generelle standardverdier for aktiva
Du definerer den generelle virkemåten eller aktivafunksjonaliteten og bilagsnummerserien i **Aktivaoppsett**-vinduet.

1. I øvre høyre hjørne, velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Aktivaoppsett**, og deretter velger du den beslektede koblingen.  
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-fixed-asset-posting-groups"></a>Slik definerer du bokføringsgrupper for aktiva:
Du bokfører grupper for å definere aktivagrupper. Poster for disse bokføringsgruppene bokføres på de samme finanskontiene.

1. I øvre høyre hjørne velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Bokf.grupper - aktiva**, og deretter velger du den beslektede koblingen.  
2. Velg handlingen **Ny**.
3. Fyll ut resten av feltene i vinduet **Kort for bokf.grp.- aktiva** etter behov.

    **Merk**: For å sikre at motkontoer for ulike aktivabokføringer settes inn automatisk når du velger handlingen **Sett inn aktivamotkonto** på kladdelinjer, følger du det neste trinnet, basert på oppskrivningsbokføring.
4. I hurtigfanen **Motkonto** i feltet **Motkonto for oppskrivning** velger du til hvilken finanskonto du vil bokføre motposter for oppskrivning.

Hvis du vil ha mer informasjon om hvordan du bruker handlingen **Sett inn aktivamotkonto** på aktivafinanskladdelinjer, kan du se for eksempel [Revaluere aktiva](fa-how-revalue.md).

## <a name="to-set-up-fixed-asset-allocation-keys"></a>Slik definerer du aktivafordelingsnøkler:
Ved hjelp av brukerdefinerte fordelingsnøkler kan du fordele transaksjoner på ulike avdelinger eller prosjekter. Du kan for eksempel definere en fordelingsnøkkel som fordeler avskrivningskostnader på biler med 35 prosent til administrasjonsavdelingen og 65 prosent til salgsavdelingen. Hvis du vil ha mer informasjon, kan du se [Bruke fordelingsnøkler i finanskladder](ui-how-use-allocation-keys-general-journals.md).

Fordelingsnøkler gjelder for aktivaklasser, ikke for individuelle aktiva.

1. I øvre høyre hjørne velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Bokf.grupper - aktiva**, og deretter velger du den beslektede koblingen.  
2. I vinduet **Bokf.grupper - aktiva** velger du handlingen **Fordelinger**, og velger deretter en bokføringstype.
3. I vinduet **Aktiva - fordelinger** fyller du ut feltene etter behov.
4. Gjenta trinn 2 og 3 for bokføringstypene du vil definere fordelingsnøkler for.

## <a name="to-set-up-fixed-asset-journal-templates"></a>Slik definerer du aktivakladdemaler:
En mal er et forhåndsdefinert oppsett for en kladd. Malen inneholder opplysninger om sporingskoder, rapporter og nummerserier. Hvis du vil ha mer informasjon, kan du se [Arbeide med finanskladder](ui-work-general-journals.md).

[!INCLUDE[d365fin](includes/d365fin_md.md)] oppretter automatisk en aktivakladdemal første gang du åpner **Aktivakladd**-vinduet, men du kan definere flere kladdemaler.  

1. I øvre høyre hjørne velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Aktivakladdemaler**, og deretter velger du den beslektede koblingen.  
2. Fyll ut feltene etter behov.

## <a name="to-set-up-fixed-asset-journal-batches"></a>Slik definerer du aktivakladder:
Du kan definere flere kladder, som vil si individuelle kladder for hver enkelt kladdemal. Ansatte kan for eksempel ha egne kladder der initialene til de ansatte brukes som kladdenavn. Hvis du vil ha mer informasjon, kan du se [Arbeide med finanskladder](ui-work-general-journals.md).  

1. I øvre høyre hjørne velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Aktivakladdemaler**, og deretter velger du den beslektede koblingen.  
2. Velg den aktuelle kladdemalen, og velg deretter **Kladder**-handlingen.
3. I vinduet **Aktivakladder** fyller du ut feltene etter behov.

## <a name="to-set-up-fixed-asset-reclassification-journal-templates"></a>Slik definerer du aktivareklassifiseringskladdemaler:
Du kan bruke dedikerte reklassifiseringskladder når du skal overføre, dele opp og knytte sammen aktiva. [!INCLUDE[d365fin](includes/d365fin_md.md)] oppretter automatisk en aktivareklassifiseringskladdemal første gang du åpner **Aktivareklass.kladd**-vinduet, men du kan definere flere reklassifiseringskladdemaler. Hvis du vil ha mer informasjon, kan du se [Arbeide med finanskladder](ui-work-general-journals.md).  

1. I øvre høyre hjørne velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Aktivareklass.kladdemaler**, og deretter velger du den beslektede koblingen.  
2. Fyll ut feltene etter behov.

## <a name="to-set-up-fixed-asset-reclassification-journal-batches"></a>Slik definerer du aktivareklassifiseringskladder:
Du kan definere flere kladder, som vil si individuelle kladder for hver reklassifiseringskladd. Ansatte kan for eksempel ha egne kladder for reklassifisering der initialene til den ansatte brukes som reklassifiseringskladdenavn. Hvis du vil ha mer informasjon, kan du se [Arbeide med finanskladder](ui-work-general-journals.md).

1. I øvre høyre hjørne velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Aktivareklass.kladdemaler**, og deretter velger du den beslektede koblingen.  
2. Velg den aktuelle kladdemalen, og velg deretter **Kladder**-handlingen.
3. I vinduet **Aktivareklass.kladder** fyller du ut feltene etter behov.

## <a name="to-set-up-fixed-asset-class-codes"></a>Slik definerer du aktivaklassekoder:
Aktivaklassekoder kan brukes til å gruppere aktiva, for eksempel i materielle og immaterielle aktiva.

1. I øvre høyre hjørne velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Aktivaklasser**, og deretter velger du den beslektede koblingen.
2. Angi koder og navn for klassene du vil opprette.

## <a name="to-set-up-fixed-asset-subclass-codes"></a>Slik definerer du aktivaunderklassekoder:
Du bruker aktivaunderklassekodene til å gruppere aktiva i kategorier, for eksempel bygninger, kjøretøy, møbler eller maskiner.  

1. I øvre høyre hjørne velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Aktivaunderklasser**, og deretter velger du den beslektede koblingen.
2. Angi koder og navn for klassene du vil opprette.

## <a name="to-set-up-fixed-asset-location-codes"></a>Slik definerer du aktivalokasjonskoder:
Du bruker aktivalokasjonskoder til å registrere aktivalokasjonen, for eksempel salgsavdeling, resepsjon, administrasjon, produksjon eller lager. Denne informasjonen er nyttig for forsikrings- og lagerformål.

1. I øvre høyre hjørne velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Aktivalokasjoner**, og deretter velger du den beslektede koblingen.
2. Angi koder og navn for aktivalokasjonene du vil opprette.

## <a name="to-register-opening-entries"></a>Slik registrerer du åpningsposter
Hvis du bruker aktiva i [!INCLUDE[d365fin](includes/d365fin_md.md)] for første gang, må du først definere modulen Finans før du kan definere aktiva. Hvordan du gjør dette, avhenger av om aktiva er integrert med finans.  

 Bruk følgende fremgangsmåte hvis aktivatransaksjoner skal bokføres i Finans.  

1. Kontroller at du har fullført grunnleggende prosedyrer for oppsett av aktiva.  
2. Opprett et aktivakort for hvert eksisterende aktiva.  
3. Definer aktivaavskrivningstablåer.  
4. Aktiver integrering med Finans ved å følge de neste trinnene.
5. Skriv inn **Avskrivningstablåer** i **Søk**-boksen, og velg deretter den relaterte koblingen.  
6. Velg det aktuelle avskrivningstablået. I fanebladet **Hjem**, under **Behandle**, velger du **Rediger liste** for å åpne **Avskrivningstablåkort**-vinduet.
7. På hurtigfanen **Integrering** må du kontrollere at alle feltene er tomme ved å fjerne alle haker. Hvis du har mer enn ett avskrivningstablå, aktiverer du integrasjon med Finans for hvert enkelt tablå.  
8. Skriv inn følgende linjer for hvert aktivum i aktivakladden:
   * En linje med anskaffelseskosten.
   * En linje med den akkumulerte avskrivningen til slutten av forrige regnskapsår.
   * En linje med den akkumulerte avskrivningen fra begynnelsen av gjeldende regnskapsår til datoen som [!INCLUDE[d365fin](includes/d365fin_md.md)] har angitt for å starte beregningen av avskrivningen.

Hvis du har andre åpningsbalanser, kan du også oppgi disse nå, for eksempel nedskrivning\- og oppskrivning.  

Hvis ikke aktivaene er integrert med Finans, utelater du trinn 4 til 7.

## <a name="see-also"></a>Se også
[Definere aktiva](fa-setup.md)  
[Anleggsmidler](fa-manage.md)  
[Finans](finance.md)  
[Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

