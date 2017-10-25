---
title: Bruke Image Analyzer-utvidelsen | Microsoft-dokumentasjon
description: "Du kan bruke denne utvidelsen til å analysere bilder av kontaktpersoner og varer for å finne attributter, slik at du kan raskt tilordne dem i Financials."
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: API, extension, Cognitive Services, image, computer vision, attribute, tag, recognition
ms.date: 06/19/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: c981c5528c7a622f9d78ed6a77c27e2ceeba44e3
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---

# <a name="the-image-analyzer-extension-for-microsoft-dynamics-365-for-financials"></a>Image Analyzer-utvidelsen for Microsoft Dynamics 365 for Financials
Image Analyzer-utvidelsen bruker kraftig bildeanalyse fra API-et for visuelt innhold for Microsoft Cognitive Services til å registrere attributter på bilder du importerer for varer og kontaktpersoner, slik at du enkelt kan gå gjennom og tilordne dem. Når det gjelder varer, kan attributter angi om varen er et bord eller en bil og om den er rød eller blå. Når det gjelder kontaktpersoner, kan attributter være kjønn eller alder.

Image Analyzer foreslår attributter basert på koder som API-et for visuelt innhold finner, og et konfidensnivå. Den foreslår som standard attributter bare hvis det er minst 80 % sannsynlighet for at attributtet er riktig. Du kan om nødvendig angi et annet konfidensnivå. Hvis du vil vite mer om hvordan kodene og konfidensnivået fastsettes, kan du se [API for visuelt innhold](https://go.microsoft.com/fwlink/?linkid=851476).  

Image Analyzer er gratis i [!INCLUDE[d365fin](includes/d365fin_md.md)], men det er en grense for hvor mange varer du kan analysere i en bestemt tidsperiode. Du kan som standard analysere 100 bilder per måned.

Når du har aktivert utvidelsen, kjører Image Analyzer hver gang du importerer et bilde til en vare eller kontaktperson. Attributter, konfidensnivå og detaljer vises med en gang, og du bestemmer hva du vil gjøre med hvert attributt. Hvis du importerte bilder før du aktiverte Image Analyzer-utvidelsen, må du gå til vare- eller kontaktkortene og velge handlingen **Analyser bilde**.  

>   [!NOTE]  
>   Når du aktiverer denne utvidelsen, godtar du at Microsoft kan lagre dataene dine og bruke dem til å forbedre Microsoft-tjenestene, for eksempel gjøre API-et for visuelt innhold bedre. For å bidra til å ivareta personvernet ditt iverksetter vi tiltak for å gjøre dataene dine anonyme og holde dem sikre. Vi publiserer ikke dataene dine eller lar andre bruke dem. Du kan fjerne bildet fra varen i [!INCLUDE[d365fin](includes/d365fin_md.md)], men API-et for visuelt innhold har fortsatt bildet i uidentifiserbar form. Hvis du vil ha mer informasjon, kan du se [Microsoft Trust Center](https://go.microsoft.com/fwlink/?linkid=851463).

## <a name="requirements"></a>Krav
Noen få krav er gjeldende for bildene:

* Bildeformater: JPEG, PNG, GIF, BMP  
* Maksimum filstørrelse: mindre enn 4 MB  
* Bildedimensjoner: større enn 50 x 50 piksler  

## <a name="blacklisting-suggested-attributes"></a>Svarteliste foreslåtte attributter
Hvis analysen foreslår et attributt du ikke vil se, kan du svarteliste attributtet. Du må imidlertid være forsiktig. Svartelistede attributter blir heller ikke foreslått for andre varer eller kontaktpersoner. Hvis du angrer at du svartelistet et attributt, kan du velge **Svartelistede attributter** og deretter slette attributtet fra oversikten.

## <a name="to-enable-image-analyzer"></a>Aktivere Image Analyzer
Image Analyzer-utvidelsen er bygd inn i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du trenger bare å aktivere den.

> [!NOTE]  
> Du må være en administrator for å kunne aktivere Image Analyzer-utvidelsen. Kontroller at du er tilordnet brukertillatelsessettet **SUPER**.

1. Gjør ett av følgende for å aktivere Image Analyzer-utvidelsen:
  
* Åpne et vare- eller kontaktkort. Velg **Analyser bilder** på varslingslinjen, og følge deretter fremgangsmåten i den assisterte oppsettsveiledningen.  
* Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Tjenestetilkoblinger**, og velg deretter **Oppsett for bildeanalyse**. Merk av for **Aktiver Image Analyzer**, og fullfør deretter fremgangsmåten i den assisterte oppsettsveiledningen.  

>   [!TIP]  
>   På siden **Oppsett for bildeanalyse** kan du også endre graden av konfidens for attributtforslag. Hvis du for eksempel vil kreve en større grad av konfidens, kan du angi en høyere prosentsats. 

## <a name="to-analyze-an-image-of-an-item"></a>Analysere et bilde av en vare
Fremgangsmåten nedenfor beskriver hvordan du analyserer et bilde som ble importert før du aktiverte Image Analyzer-utvidelsen.  

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Varer**, og velg deretter den relaterte koblingen.  
2. Velg varen, og velg deretter handlingen **Analyser bilde**.  
3. Siden **Image Analyzer-attributter** viser de registrerte attributtene, konfidensnivået og annen informasjon om attributtet. Bruk alternativene for **Action to perform** til å angi det du vil gjøre med attributtet.  

>   [!TIP]  
>   Du kan legge til navnet på attributtet i varebeskrivelsen ved å velge **Legg til i varebeskrivelse**. Dette kan for eksempel være nyttig for å legge til detaljer raskt.  

## <a name="to-analyze-a-picture-of-a-contact-person"></a>Analysere et bilde av en kontaktperson
Fremgangsmåten nedenfor beskriver hvordan du analyserer et bilde som ble importert før du aktiverte Image Analyzer-utvidelsen.  

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Kontakter**, og velg deretter den relaterte koblingen.  
2. Velg kontaktpersonen, og velg deretter handlingen **Analyser bilde**.  
3. I hurtigfanen **Profilspørreskjema** går du gjennom forslagene og foretar korrigerer om nødvendig.  

## <a name="to-use-your-own-account-for-the-computer-vision-api"></a>Bruke din egen konto for API-et for visuelt innhold
Du kan også bruke din egen konto for API-et for visuelt innhold, for eksempel hvis du vil analysere flere bilder enn det vi tillater.  
  
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Image Analyzer-oppsett**, og velg deretter den relaterte koblingen.  
2. Angi **API-URI** og **API-nøkkel** som du har fått for API-et for visuelt innhold.  
  
>   [!NOTE]  
>   Du må legge til **/analyze** på slutten av API-URI-en, hvis det ikke allerede står der. Eksempel: ```https://cronus.api.cognitive.microsoft.com/vision/v1.0/analyze```.

## <a name="to-see-how-many-analyses-you-have-left-in-the-current-period"></a>Se hvor mange analyser har du igjen i den gjeldende perioden
Du kan vise hvor mange analyser du har gjort, og hvor mange du fortsatt kan gjøre, i den gjeldende perioden.  
  
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Image Analyzer-oppsett**, og velg deretter den relaterte koblingen.  
2. **Grensetype**, **Grenseverdi** og **Utførte analyser** gir bruksinformasjonen.  

## <a name="to-stop-using-the-image-analyzer-extension"></a>Slutte å bruke Image Analyzer-utvidelsen
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Tjenestetilkoblinger**, og velg deretter **Image Analyzer-oppsett**.  
2. Fjern merket for **Aktiver Image Analyzer**.  

## <a name="see-also"></a>Se også
[Arbeide med vareattributter](inventory-how-work-item-attributes.md)  
[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjelp av utvidelser](ui-extensions.md)  
[Velkommen til [!INCLUDE[d365fin](includes/d365fin_md.md)]](index.md)  


