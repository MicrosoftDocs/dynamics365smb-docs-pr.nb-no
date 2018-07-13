---
title: Bruke Image Analyzer-utvidelsen | Microsoft-dokumentasjon
description: "Du kan bruke denne utvidelsen til å analysere bilder av kontaktpersoner og varer for å finne attributter, slik at du kan raskt tilordne dem i Business Central."
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: API, extension, Cognitive Services, image, computer vision, attribute, tag, recognition
ms.date: 06/12/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 3331849cf94c70d0597ae5f37d3109451947c9fc
ms.openlocfilehash: f40f51ffec0d052e26bcaf34c928ef63e9adde4d
ms.contentlocale: nb-no
ms.lasthandoff: 06/20/2018

---

# <a name="the-image-analyzer-extension-for-microsoft-business-central"></a>Image Analyzer-utvidelsen for Business Central
Image Analyzer-utvidelsen bruker kraftig bildeanalyse fra API-et for visuelt innhold for Microsoft Cognitive Services til å registrere attributter på bilder du importerer for varer og kontaktpersoner, slik at du enkelt kan gå gjennom og tilordne dem. Når det gjelder varer, kan attributter angi om varen er et bord eller en bil og om den er rød eller blå. Når det gjelder kontaktpersoner, kan attributter være kjønn eller alder.

Image Analyzer foreslår attributter basert på koder som API-et for visuelt innhold finner, og et konfidensnivå. Den foreslår som standard attributter bare hvis det er minst 80 % sannsynlighet for at attributtet er riktig. Du kan om nødvendig angi et annet konfidensnivå. Hvis du vil vite mer om hvordan kodene og konfidensnivået fastsettes, kan du se [API for visuelt innhold](https://go.microsoft.com/fwlink/?linkid=851476).  

Image Analyzer er gratis i [!INCLUDE[d365fin](includes/d365fin_md.md)], men det er en grense for hvor mange varer du kan analysere i en bestemt tidsperiode. Du kan som standard analysere 100 bilder per måned.

Når du har aktivert utvidelsen, kjører Image Analyzer hver gang du importerer et bilde til en vare eller kontaktperson. Attributter, konfidensnivå og detaljer vises med en gang, og du bestemmer hva du vil gjøre med hvert attributt. Hvis du importerte bilder før du aktiverte Image Analyzer-utvidelsen, må du gå til vare- eller kontaktkortene og velge handlingen **Analyser bilde**.  

## <a name="privacy-notice"></a>Personvernerklæring 
Denne utvidelsen bruker API-en for visuelt innhold fra Microsoft Cognitive Services, som kan ha andre typer samsvarsforpliktelser enn [!INCLUDE[d365fin](includes/d365fin_md.md)]. Når du aktiverer Image Analyzer-utvidelsen, sendes kundedata, for eksempel kontaktbilde eller varebilde, til API-en for visuelt innhold. Ved å installere denne utvidelsen godtar du at dette begrensede settet med data sendes til API-en for visuelt innhold. Vær oppmerksom på at du kan deaktivere samt avinstallere, Image Analyzer-utvidelsen når som helst for å slutte å bruke denne funksjonen. Hvis du vil ha mer informasjon, kan du se [Microsoft Trust Center](https://go.microsoft.com/fwlink/?linkid=851463).

## <a name="requirements"></a>Krav
Noen få krav er gjeldende for bildene:

* Bildeformater: JPEG, PNG, GIF, BMP  
* Maksimum filstørrelse: mindre enn 4 MB  
* Bildedimensjoner: større enn 50 x 50 piksler  

## <a name="to-enable-image-analyzer"></a>Aktivere Image Analyzer
Image Analyzer-utvidelsen er bygd inn i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du trenger bare å aktivere den.

> [!NOTE]  
> Du må være en administrator for å kunne aktivere Image Analyzer-utvidelsen. Kontroller at du er tilordnet brukertillatelsessettet **SUPER**.

1. Gjør ett av følgende for å aktivere Image Analyzer-utvidelsen:

* Åpne et vare- eller kontaktkort. Velg **Analyser bilder** på varslingslinjen, og følge deretter fremgangsmåten i den assisterte oppsettsveiledningen.  
* Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Tjenestetilkoblinger**, og velg deretter **Oppsett for bildeanalyse**. Merk av for **Aktiver Image Analyzer**, og fullfør deretter fremgangsmåten i den assisterte oppsettsveiledningen.  

    > [!TIP]  
    > På siden **Oppsett for bildeanalyse** kan du også endre graden av konfidens for attributtforslag. Hvis du for eksempel vil kreve en større grad av konfidens, kan du angi en høyere prosentsats.

## <a name="to-analyze-an-image-of-an-item"></a>Analysere et bilde av en vare
Fremgangsmåten nedenfor beskriver hvordan du analyserer et bilde som ble importert før du aktiverte Image Analyzer-utvidelsen.  

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Varer**, og velg deretter den relaterte koblingen.  
2. Velg varen, og velg deretter handlingen **Analyser bilde**.  
3. Siden **Image Analyzer-attributter** viser de registrerte attributtene, konfidensnivået og annen informasjon om attributtet. Bruk alternativene for **Action to perform** til å angi det du vil gjøre med attributtet.  

    > [!TIP]  
    > Du kan legge til navnet på attributtet i varebeskrivelsen ved å velge **Legg til i varebeskrivelse**. Dette kan for eksempel være nyttig for å legge til detaljer raskt.  

## <a name="to-analyze-a-picture-of-a-contact-person"></a>Analysere et bilde av en kontaktperson
Fremgangsmåten nedenfor beskriver hvordan du analyserer et bilde som ble importert før du aktiverte Image Analyzer-utvidelsen.  

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Kontakter**, og velg deretter den relaterte koblingen.  
2. Velg kontaktpersonen, og velg deretter handlingen **Analyser bilde**.  
3. I hurtigfanen **Profilspørreskjema** går du gjennom forslagene og foretar korrigerer om nødvendig.  

## <a name="blacklisting-suggested-attributes"></a>Svarteliste foreslåtte attributter
Hvis analysen foreslår et attributt du ikke vil se, kan du svarteliste attributtet. Du må imidlertid være forsiktig. Svartelistede attributter blir heller ikke foreslått for andre varer eller kontaktpersoner. Hvis du angrer at du svartelistet et attributt, kan du velge **Svartelistede attributter** og deretter slette attributtet fra oversikten.

## <a name="to-use-your-own-account-for-the-computer-vision-api"></a>Bruke din egen konto for API-et for visuelt innhold
Du kan også bruke din egen konto for API-et for visuelt innhold, for eksempel hvis du vil analysere flere bilder enn det vi tillater.  

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Image Analyzer-oppsett**, og velg deretter den relaterte koblingen.  
2. Angi **API-URI** og **API-nøkkel** som du har fått for API-et for visuelt innhold.  

    > [!NOTE]  
    > Du må legge til **/analyze** på slutten av API-URI-en, hvis det ikke allerede står der. Eksempel: ```https://cronus.api.cognitive.microsoft.com/vision/v1.0/analyze```.

## <a name="to-see-how-many-analyses-you-have-left-in-the-current-period"></a>Se hvor mange analyser har du igjen i den gjeldende perioden
Du kan vise hvor mange analyser du har gjort, og hvor mange du fortsatt kan gjøre, i den gjeldende perioden.  

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Image Analyzer-oppsett**, og velg deretter den relaterte koblingen.  
2. **Grensetype**, **Grenseverdi** og **Utførte analyser** gir bruksinformasjonen.  

## <a name="to-stop-using-the-image-analyzer-extension"></a>Slutte å bruke Image Analyzer-utvidelsen
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Tjenestetilkoblinger**, og velg deretter **Image Analyzer-oppsett**.  
2. Fjern merket for **Aktiver Image Analyzer**.  

## <a name="see-also"></a>Se også
[Arbeide med vareattributter](inventory-how-work-item-attributes.md)  
[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjelp av utvidelser](ui-extensions.md)  
[Komme i gang](product-get-started.md)  

