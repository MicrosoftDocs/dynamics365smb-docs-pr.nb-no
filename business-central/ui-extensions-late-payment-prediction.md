---
title: Forutsi forsinket betaling for salgsdokumenter | Microsoft-dokumentasjon
description: Bruk prognosemodellen vår til å forutse om en faktura blir betalt i tide.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customer, payment, invoice, sales, invoice, quote
ms.date: 10/01/2018
ms.author: bholtorf
ms.openlocfilehash: 4e47858bf1f7253f8fb8951fe8ea3cb611138852
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2019
ms.locfileid: "803524"
---
# <a name="the-late-payment-prediction-extension"></a>Utvidelsen Prognose for forsinket betaling  
Effektiv administrasjon av salg er viktig for den generelle økonomiske tilstanden statusen til en bedrift. Utvidelsen Prognose for forsinket betaling kan hjelpe deg med å redusere utestående og finjustere innkrevingsstrategien din ved å forutse om salgsfakturaer blir betalt i tide. Hvis en betaling er forutsatt å bli sen, kan du bestemme deg for å justere betalingsbetingelsene eller betalingsmåten for kunden.

## <a name="what-are-predictions-based-on"></a>Hva er prognoser basert på?  
Utvidelsen Prognose for forsinket betaling bruker en prognosemodell vi utviklet i Azure Machine Learning Studio og lærte opp ved hjelp av data som er representative for en rekke små og mellomstore bedrifter. Selv om vi allerede har opplært og evaluert den, fortsetter prognosemodellen vår å lære fra dataene dine. Jo mer du bruker modellen, og jo flere data du mater inn i den, jo mer nøyaktige blir prognosene. Som standard vurderer utvidelsen modellen og oppdaterer prognosene på ukentlig basis. Du kan imidlertid oppdatere prognoser når som helst ved å velge **Oppdater prognose**-handlingen på siden **Kundeposter**.  

> [!Note]
> Vi bruker litt av databehandlingstiden din hver uke når vi evaluerer modellen og oppdaterer prognosene. I tillegg til å oppdatere prognosene manuelt er andre handlinger også bruke databehandlingstid når du lærer opp modellen (som du kan gjøre hvis du nylig har lagt inn data), og når dur evaluere modellen (som undersøker kvaliteten på modellen).

## <a name="getting-started"></a>Komme i gang
Utvidelsen er gratis i [!INCLUDE[d365fin](includes/d365fin_md.md)], og vi tilbyr et abonnement på Azure Machine Learning. Abonnementet tilbyr 30 minutter databehandlingstid per måned. Hvis du trenger mer enn det, kan du opprette en egen prognosemodell og bruke den i stedet. Hvis du vil ha mer informasjon, kan du se delen _Bygge din egen prognosemodell_ senere i dette emnet.  

Når du åpner et bokført salgsdokument, vises en melding øverst på siden. Hvis du vil bruke utvidelsen Prognose for forsinket betaling, kan du velge dette ved å velge **Aktiver** i meldingen. Du kan også du sette opp utvidelsen manuelt. For eksempel hvis du angrer på at du lukket meldingen.  

Hvis du vil aktivere utvidelsen manuelt, følger du denne fremgangsmåten:

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Tjenestetilkoblinger**, og velg deretter den relaterte koblingen.  
2. Velg **Oppsett av prognose for forsinket betaling**, og deretter fyller du ut feltene etter behov.

## <a name="viewing-all-payment-predictions"></a>Vis alle betalingsprognoser
Hvis du aktiverer utvidelsen, er flisen **Betalinger forutsatt til å være forsinket** tilgjengelig i **Forretningsleder**-rollesenteret. Flisen viser hvor mange betalinger som er forutsatt å bli sene, og lar deg åpne siden **Kundeposter**, der du kan se nærmere på de bokførte fakturaene. Det finnes tre kolonner til å være oppmerksom:  

* **Sen betaling** - angir om betalingen av fakturaen forutsettes å bli forsinket.
* **Prognosekonfidens** - angir hvor pålitelig du bør vurdere prognosen til å være. **Høy** betyr at prognosen er minst 90 % sikker, **Middels** er mellom 80 og 90 % og **Lav** er under 80 %.
* **Prognosekonfidens %** - viser den faktiske prosenten bak prognoserangeringen. Denne kolonnen vises ikke som standard, men kan du legge den til hvis du vil. Hvis du vil ha mer informasjon, se [Tilpasse arbeidsområdet ](ui-personalization-user.md).

> [!Tip]
> Kundeposter-siden viser også en faktaboks på høyre side. Når du ser prognoser, informasjon i vinduet **Kundeinformasjon** kan være nyttig. Når du velger fakturaen i oversikten, viser delen informasjon om kunden. Du kan også agere umiddelbart. Hvis en kunde ofte glemmer å betale, kan du åpne kundekortet fra faktaboksen og sperre kunden for fremtidig salg.  

## <a name="viewing-a-payment-prediction-for-a-specific-sales-document"></a>Vise en betalingsprognose for et spesifikt salgsdokument
Du kan også forutse sen betalinger direkte. På sidene **Tilbud**, **Ordrer** og **Salgsfakturaer** kan du bruke feltet **Forutsi betaling** til å generere en prognose for salgsdokumentene du ser på.

<!--## Scheduling Payment Predictions
On the **Late Payment Prediction Setup** page you can schedule updates to payment predictions for a time that is convenient for you. -->

## <a name="building-your-own-predictive-model"></a>Bygge din egen prognosemodell
Er du interessert i å bygge din egen prognosemodell? Du kan bruke Azure Machine Learning Studio til å bygge din egen prognosemodell og bruke den i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hvis du vil bruke din egen modell, må du abonnere på Azure Machine Learning. Hvis du vil ha mer informasjon, se [Dokumentasjon for Azure Machine Learning Studio](https://go.microsoft.com/fwlink/?linkid=861765).  

Vi tilbyr imidlertid en enklere måte for deg å opprette og bruke din egen prognosemodell. Du kan dele data fra fakturaene dine med prognoseeksperimentet vårt i Azure Machine Learning, og la eksperimentet opprette og lære opp en prognisemodell basert på dataene dine. Hvis du vil dele dataene, går du til siden **Oppsett av prognose for forsinket betaling** og velger **Opprett min modell**. Senere prognoser baserer seg på modellen og dataene dine, ikke våre.  

> [!Note]
>   Kvaliteten på modellen er viktig. Når prognoseeksperimentet vårt bruker dataene dine til å lære opp en modell, fastsetter det en kvalitsverdi for modellen i prosent. Modellkvaliteten angir hvor nøyaktig modellens prognoser sannsynligvis vil være. Flere faktorer kan påvirke kvaliteten på en modell. Dette kan for eksempel være at det ikke er nok data eller dataene ikke inneholder nok variasjon. Du kan vise kvaliteten på modellen du bruker, på siden **Oppsett av prognose for forsinket betaling**. Du kan også angi e minimumsgrense for modellkvaliteten. Modeller med en kvalitetsverdi under grensen, vil ikke produsere prognoser.  

### <a name="to-use-your-model-instead-of-ours"></a>Slik bruker din modellen din i stedet for vår  
Hvis du oppretter din egen modell i Azure Machine Learning Studio, uten å bruke verktøyene i [!INCLUDE[d365fin](includes/d365fin_md.md)], må du angi legitimasjon slik at [!INCLUDE[d365fin](includes/d365fin_md.md)] får tilgang til modellen. Det er et par trinn for å gjøre dette:

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Oppsett av prognose for forsinket betaling**, og velg deretter den relaterte koblingen.  
2. Merk av for **Bruk Azure-abonnementet mitt**.  
3. I vinduet **Valgt modell** velger du **Min modell**.  
4. På hurtigfanen **Legitimasjon for min modell** angir API URL-adressen og API-nøkkelen for modellen.  

## <a name="see-also"></a>Se også  
[Dokumentasjon for Azure Machine Learning Studio](https://go.microsoft.com/fwlink/?linkid=861765)  
[Tilpasse Business Central for med utvidelser](ui-extensions.md)  
[Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
