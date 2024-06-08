---
title: Behandle brukerinnstillinger og innstillinger som administrator
description: Behandle brukerinnstillinger og innstillinger i Dynamics 365 Business Central.
author: sorenfriisalexandersen
ms.topic: get-started
ms.devlang: al
ms.reviewer: bholtorf
ms.search.keywords: 'user settings, preferences, language, region, time zone, regional settings'
ms.search.form: '9204,'
ms.date: 04/01/2021
ms.author: soalex
ms.service: dynamics-365-business-central
---
# <a name="manage-user-settings-and-preferences"></a>Behandle brukerinnstillinger og innstillinger

Du kan som administrator konfiguree brukerinnstillinger i [!INCLUDE[prod_short](includes/prod_short.md)], på samme måte som enkeltbrukere kan behandle sine egne innstillinger på siden **Mine innstillinger**.  

Få en oversikt over alle brukerne i listen **Brukere**, og endre individuelle innstillinger ved å velge handlingen **Brukerinnstillinger** for den aktuelle brukeren.

> [!TIP]
> I listen **Brukerinnstillinger** vises gjeldende innstillinger for hver enkelt bruker. Hvis du vil vise eller redigere enkelte brukere, velger du handlingen **Vis** eller **Rediger**.

Siden **Kort for brukerinnstillinger** ligner på siden **Mine innstillinger** som hver bruker har tilgang til, og det er et kraftig verktøy du for eksempel kan bruke til å angi standardinnstillinger og fjerne personlige sider.  

## <a name="types-of-user-settings"></a>Typer brukerinnstillinger

*Brukerinnstillinger* er ikke det samme som *brukeroppsett*, som er om brukeren som en enhet og brukerens tilgang i systemet. I tillegg har brukerinnstillinger ingenting å gjøre med en brukers tilpassing, for eksempel ved å gjøre endringer i brukergrensesnittet. Brukerinnstillinger bestemmer de forhåndsdefinerte innstillingene for hver bruker i ulike deler av måten programmet vises på for brukeren. Det følgende avsnittet inneholder de fem typene brukerinnstillinger og innstillinger som kan angis av enkeltbrukeren eller sentralt av administratoren:

* **Selskap**  

  Denne innstillingen bestemmer hvilket selskap som skal logges på ved neste pålogging. En bruker kan ha tilgang til flere selskaper og kan være aktive i flere selskaper.

* **Rolle**  

  Rollen, eller profilen, beskriver brukerens funksjon i selskapet, for eksempel *Salgssjef*, *Regnskapsfører* eller *Innkjøper*. Profilen bestemmer deretter brukerens rollesenter, hjemmesiden som brukerne vil se når de logger på. Profilen påvirker ikke tilgangsrettigheter til funksjoner i [!INCLUDE[prod_short](includes/prod_short.md)].  

* **Språk**  

  Definerer programspråket som [!INCLUDE[prod_short](includes/prod_short.md)] presenterer tekst, titler og feilmeldinger i. Hvis [!INCLUDE[prod_short](includes/prod_short.md)]-brukere synkroniseres fra Microsoft 365, brukes språkinnstillinger fra Microsoft 365, og det antas at brukeren vil bruke de samme innstillingene i Office-produkter og [!INCLUDE[prod_short](includes/prod_short.md)]. Systemansvarlig kan endre standardinnstillingen, og hver bruker kan velge mellom tilgjengelige språk på siden Mine innstillinger. Men de tilbakestilles til verdien fra Microsoft 365 når neste synkronisering er utført.

  Hvis språkinnstillingen fra Microsoft 365 samsvarer med et språk som støttes i [!INCLUDE[prod_short](includes/prod_short.md)], velges dette språket for brukeren.  

  > [!NOTE]
  > Du må kanskje installere en språkapp for [!INCLUDE[prod_short](includes/prod_short.md)] for å kunne vise språket. Det er derfor en god praksis å installere de nødvendige språkappene før alle brukere logger på for første gang, slik at de får en god opplevelse den første dagen. Hvis du vil ha mer informasjon, kan du se listen over [språk som støttes](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations).  
  
* **Område**  

  Definerer hvordan datoer og numre presenteres i [!INCLUDE[prod_short](includes/prod_short.md)]-klienten, for eksempel om det skal brukes europeiske eller amerikanske datoformater, eller hvordan desimaltegn og tusenskilletegn skal vises i beløp. Hvis [!INCLUDE[prod_short](includes/prod_short.md)]-brukere synkroniseres fra Microsoft 365, brukes områdeinnstillinger fra Microsoft 365, og det antas at brukeren vil bruke de samme innstillingene i Office-produkter og [!INCLUDE[prod_short](includes/prod_short.md)]. En administrator eller bruker kan endre disse innstillingene manuelt i [!INCLUDE[prod_short](includes/prod_short.md)], men de tilbakestilles til verdien fra Microsoft 365 når den neste synkroniseringen blir utført.

* **Tidssone**  

  Definerer tidssonen brukeren befinner seg i. Dette synkroniseres for øyeblikket ikke fra Microsoft 365 og må angis manuelt.  

* **Læringstips**

  [!INCLUDE [ua-teachingtips](includes/ua-teachingtips.md)] Som administrator kan du slå av læringstips for alle brukere, for eksempel hvis du er i ferd med å introdusere brukere som allerede er kjent med [!INCLUDE [prod_short](includes/prod_short.md)].  

> [!NOTE]
> Hvis det gjøres en Microsoft 365-brukersynkronisering mens brukerne er logget på [!INCLUDE[prod_short](includes/prod_short.md)], må disse brukerne oppdatere nettleseren eller logge av og på [!INCLUDE[prod_short](includes/prod_short.md)] for å se et mulig språk som er angitt av synkroniseringshandlingen.

## <a name="overview-of-all-user-specific-changes"></a>Oversikt over alle brukerspesifikke endringer

Som administrator kan du få oversikt over individuelle endringer i [!INCLUDE [prod_short](includes/prod_short.md)] som de enkelte brukerne kan ha gjort på ulike sider i [!INCLUDE [prod_short](includes/prod_short.md)]. Når brukere endrer opplevelsen i [!INCLUDE [prod_short](includes/prod_short.md)], vil disse endringene gjenspeiles i listen **Brukertilpassinger**. <!--Administrators can also set these settings for users before they log in the first time, so users do not have to do it themselves, providing them a better *getting started* experience.-->

<!-- >[!NOTE]
> User personalizations do not have anything to do with the *personal* lightweight changes a user can make to the user experience.-->

## <a name="to-review-or-delete-user-personalizations"></a>Slik går du gjennom eller sletter brukertilpassinger

1. Velg ikonet ![Søk etter side eller rapport.](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport") og angi **Tilpassede sider**, og velg deretter den relaterte koblingen.
2. Dette viser listen over brukere og deres tilpassede sider. Hvis du vil fjerne en brukertilpassing, klikker du den aktuelle raden eller velger **Administrer**, og deretter velger du **Slett**.

Dette sletter brukertilpassingen, og brukerens opplevelse av den relevante siden går tilbake til standardtilstanden.

## <a name="see-also"></a>Se også

[Bli klar til å gjøre forretninger](ui-get-ready-business.md)  
[Land-/områdetilgjengelighet og støttede oversettelser](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations)  
[Endre språk og nasjonal innstilling](about-locale-language.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
