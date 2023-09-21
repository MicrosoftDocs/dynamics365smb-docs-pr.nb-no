---
title: Flere språk og oversettelse
description: Finn ut hvordan språk og område påvirker opplevelsen i Business Central. Endre språket i brukergrensesnittet i Mine innstillinger.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'language, locale, localization, culture, region, regional settings'
ms.search.form: '9020, 9022, 9026, 9027, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017'
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="changing-language-and-region"></a>Endre språk og område

[!INCLUDE[prod_short](includes/prod_short.md)] er tilgjengelig i mange markeder og språk over hele verden. I markedene der [!INCLUDE[prod_short](includes/prod_short.md)] er tilgjengelig, er lovmessige funksjoner tilgjengelige for å hjelpe selskaper med samsvar med lovgivning. [!INCLUDE[prod_short](includes/prod_short.md)] kan vises på forskjellige språk. Du kan også endre språket som brukes til å vise tekster. Endringen er umiddelbar når du har blitt automatisk logget av og på igjen. Innstillingen gjelder for deg og ikke alle andre i bedriften.  

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

Du bruker for eksempel den kanadiske versjonen av [!INCLUDE[prod_short](includes/prod_short.md)]. Det betyr at du kan se bruker grensesnittet på engelsk, tysk, fransk eller annet språk, men det er likevel den kanadiske versjonen av [!INCLUDE[prod_short](includes/prod_short.md)]. Det er ikke det samme som [!INCLUDE[prod_short](includes/prod_short.md)] i Tyskland, der funksjonaliteten er tilpasset kravene i dette markedet.  

Hvis du vil endre språk i brukergrensesnittet, går du til **Mine innstillinger**-siden. Hvis du vil ha mer informasjon, kan du se [Endre grunnleggende innstillinger](ui-change-basic-settings.md#language). 

> [!NOTE]  
> Valget av språk tilbakestilles til innstillingen i Microsoft 365-profilen hvis administrator synkroniserer brukere fra Microsoft 365 til [!INCLUDE[prod_short](includes/prod_short.md)].

Du kan ikke endre tekstene som er lagret som appdata. Eksempler på slike tekster er navn på lagervarer eller merknader til en kunde. Denne type tekst blir med andre ord ikke oversatt.  

> [!NOTE]  
> [!INCLUDE[prod_short](includes/prod_short.md)] støtter bare ett tegnsett for data. Det kan derfor forekomme at enkelte tegn ikke støttes i miljøet ditt, noe som kan føre til at det oppstår problemer når du henter data som ble registrert med et annet tegnsett. Miljøet støtter for eksempel kanskje bare engelske og russiske tegn. Hvis du skriver inn data på et annet språk, lagres de derfor kanskje ikke som de skal. Du må kontakte systemansvarlig for å være sikker på at du forstår hvilke språk som støttes i [!INCLUDE[prod_short](includes/prod_short.md)].  

## <a name="changing-your-region-setting"></a>Endre områdeinnstillingen

Område er forskjellig fra både språket og de juridiske kravene i lokale markeder. Område bestemmer hvordan dataene vises, for eksempel desimaltegnet og hvordan teksten justeres til venstre eller høyre. Området bestemmer også noen systemelementer i nettleseren, for eksempel handlingen til å opprette et nytt element i en liste.  

Du kan endre området i nettleserfanen som du bruker til å arbeide i [!INCLUDE[prod_short](includes/prod_short.md)]. Endringen gjelder bare for deg og ikke for andre brukere i selskapet.  Valget av område tilbakestilles til innstillingen i Microsoft 365-profilen hvis administrator synkroniserer brukere fra Microsoft 365 til [!INCLUDE[prod_short](includes/prod_short.md)].

> [!IMPORTANT]  
> Når du endrer området, vises en lang liste over språk og områder. Språket påvirkes imidlertid ikke av områdevalget.  

Hvis du vil endre område, går du til **Mine innstillinger**-siden. Hvis du vil ha mer informasjon, kan du se [Endre grunnleggende innstillinger](ui-change-basic-settings.md).  

## <a name="changing-the-region-setting-for-customers-contacts-and-vendors"></a>Endre områdeinnstillingen for kunder, kontakter og leverandører

Enkelte bedrifter bruker en ekstern tjeneste som validerer adresseinformasjon i landet eller området. Når du må oppdatere adresseinformasjon, er det imidlertid ikke sikkert at den strukturerte fremgangsmåten som disse tjenestene bruker, alltid er det som er riktig for enkelte scenarioer. Business Central tilbyr en mer fleksibel måte å angi adresseinformasjon på.

Hvis du aktiverer feltet **Krev land-/områdekode i adressen** på siden **Finansoppsett**, tilbakestilles endringer i feltet **Land-/områdekode** for adresser til kunder, kontakter eller leverandører til verdiene i andre adressefelter.

## <a name="application-version"></a>Programversjon

På siden **Hjelp og støtte** kan du se versjonen av [!INCLUDE[prod_short](includes/prod_short.md)] som firmaet er basert på. Hvis du vil basere et selskap på en annen versjon, kan systemansvarlig opprette et nytt produksjonsmiljø. Hvis du vil ha mer informasjon, kan du se [Opprette et nytt produksjonsmiljø](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#create-a-new-production-environment) i utvikler- og IT Pro-innholdet.  

## <a name="languages-of-the--help"></a>Språkene i Hjelpen for [!INCLUDE[prod_short](includes/prod_short.md)]

Hjelpeinnholdet for standardversjonen av [!INCLUDE[prod_short](includes/prod_short.md)] publiseres på Microsoft Learn. Innholdet er tilgjengelig på forskjellige språk. Hvis du har tilgang til dokumentasjonen fra [!INCLUDE[prod_short](includes/prod_short.md)], vises innholdet på ditt eget språk. Hvis en bestemt side ikke ennå er tilgjengelig på ditt eget språk, vises den som standard på engelsk.

### <a name="how-do-i-change-the-language-of-the-microsoft-learn-site"></a>Hvordan endrer jeg språket for Microsoft Learn-området?

Det er enkelt - bla nederst på weblesersiden, og velg verden symbolet nederst til venstre.

> [!NOTE]  
> Oversikten viser alle språk som støttes av Microsoft Learn-området. [!INCLUDE[prod_short](includes/prod_short.md)] er tilgjengelig i et begrenset antall land/områder, og hjelpeinnholdet for [!INCLUDE [prod_short](includes/prod_short.md)] er ikke tilgjengelig på alle språk som Microsoft Learn-området støtter.

## <a name="see-also"></a>Se også

[Ressurser for hjelp og støtte](product-help-and-support.md)  
[Endre grunnleggende innstillinger](ui-change-basic-settings.md)  
[Bli klar til å gjøre forretninger](ui-get-ready-business.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
