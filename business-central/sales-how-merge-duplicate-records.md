---
title: Slå sammen dupliserte kunde- eller leverandørposter
description: Beskriver hvordan du konsoliderer informasjon om kunder eller leverandører når du har duplikate poster om noen av dem.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: client
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="merge-duplicate-records"></a>Slå sammen dupliserte poster

Siden ulike brukere oppretter nye kunde-, leverandør- eller kontaktkort over tid eller de nye postene opprettes automatisk under overføringen, kan en kunde, leverandør eller kontakt være representert i systemet med mer enn én post. I så fall kan du bruke siden **Slå sammen duplikat** fra kortet til posten du vil beholde. Siden siden gir deg en oversikt over dupliserte feltverdier og inneholder funksjoner for å velge hvilke verdier du vil beholde eller forkaste når du slår sammen to poster til én.

> [!NOTE]
> Bare brukere med tillatelsessettet Slå sammen duplikater kan bruke denne funksjonaliteten.

> [!TIP]
> Siden **Slå sammen duplikat** viser alle felt der verdiene er forskjellige for de to postene som sammenlignes. Derfor er et duplikat angitt ved at siden viser svært få felt. Men hvis siden viser mange felt, vil er den mistenkte posten trolig ikke et duplikat.

Følgende fremgangsmåte er basert på et kundekort. Trinnene er de samme for en leverandør og kontaktkort.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Kunder** og velger den relaterte koblingen.
2. Angi kunden som du vet eller mistenker at det finnes en duplisert post for, og velg deretter **Rediger**-handlingen.
3. På siden **Kundekort** velger du handlingen **Slå sammen med**.
4. På siden **Slå sammen duplikat** i feltet **Slå sammen med** velger du kunden som du mener er et duplikat av kunden du har åpnet, som er angitt i feltet **Gjeldende**.

    Hurtigfanen **Felt** viser felt der verdiene er ulike for de to kundene. Dette betyr at hvis den valgte kunden virkelig er et duplikat, vil bare svært få felt være oppført, for eksempel skrivefeil og andre dataregistreringsfeil.

    Hurtigfanen **Relaterte tabeller** inneholder en oversikt over tabeller der det finnes felt med en relasjon til begge kunder. Feltene **Gjeldende antall** og **Duplikatantall** viser hvor mange felt i de relaterte tabellene der **Nr.**-verdien for både den gjeldende og dupliserte kunder brukes. På siden **Slå sammen duplikat** er denne delen bare til informasjon, men hvis det oppstår flettekonflikter, løser du dem på siden **Slå sammen duplikate konflikter**. Se trinn 8 til 12.   

5. For hvert felt der du vil bruke en annen verdi enn den gjeldende, merker du av for **Overstyr**. Verdien i feltet **Alternativ verdi** overføres deretter til den gjeldende posten når du fullfører prosessen.
6. Når du er ferdig med å velge hvilke verdier som skal beholdes eller overstyres, velger du **Flett**-handlingen.

    Systemet kontrollerer om flettingen av verdier for den dupliserte kunden til den gjeldende kunden fører til konflikter. Det finnes en konflikt hvis en verdi i minst ett primærnøkkelfelt er den samme for begge kunder mens verdien i **Nei**-feltet er forskjellige for de to kundene.

7. Hvis det ikke finnes noen konflikter, velger du **Ja**-knappen i bekreftelsesmeldingsboksen.

    Navnet på den dupliserte kunden endres, slik at all bruk av **Nr.**-verdien i alle felt med tilknytninger til kundetabellen erstattes med **Nr.**-verdien til den gjeldende kunden.
8. Hvis det finnes konflikter, velger du **Løs (%1) konflikter før sammenslåing**-handlingen på hurtigfanen **Konflikter**, som vises ved konflikter.
9. På siden **Slå sammen duplikate konflikter** velger du linjen for en relatert tabell med en konflikt, og deretter velger du **Vis detaljer**- handlingen.

    Siden **Slå sammen duplikat** viser nå feltene i den valgte tabellen som forårsaker en sammenslåingskonflikt mellom de to kundepostene. Merk at i både de summert verdiene i feltene **Gjeldende** og **Konflikter med** og på linjene at minst ett primærnøkkelfelt er det samme for begge kunder, og at verdien for **Nr.**-feltet er forskjellig for de to kundene.   
10. Hvis du ikke vil beholde den dupliserte kundeposten, velger du handlingen **Fjern duplikat**, og deretter velger du **Lukk**-knappen.

    Andre identiske feltverdier enn verdien i feltet **Nr.** fjernes fra den supliserte posten og settes inn på gjeldende post.
11. Hvis du vil beholde den dupliserte kundeposten etter flettingen, velger du **Gi nytt navn til duplikat**.
12. På linjene, ikke for feltet **Nr.**, der feltet har samme verdi i begge postene, endres verdien i feltet **Alternativ verdi**, og deretter velger du **Lukk**-knappen.

    Den motstridende feltverdien oppdateres på den dupliserte posten, slik at den kan slås sammen med den gjeldende posten. Den dupliserte posten finnes fortsatt etter sammenslåingen.
13. Gjenta trinn 8 til og med 12 helt til alle konflikter er løst. Hurtigfanen **Konflikter** forsvinner.
14. På siden **Slå sammen duplikat** velger du **Slå sammen**-handlingen på nytt, og deretter velger du **Ja**-knappen i bekreftelsesmeldingsboksen.

> [!NOTE]
> For kontakter kan du bruke funksjonaliteten for å finne duplikate kontakter før du bruker siden **Slå sammen duplikat**. Hvis du vil ha mer informasjon, se [Søke etter duplikatkontakter](marketing-setup-contacts.md#searching-for-duplicate-contacts).

## <a name="see-related-microsoft-training"></a>Se relatert [Microsoft-opplæring](/training/modules/trade-master-data-dynamics-365-business-central/)

## <a name="see-also"></a>Se også

[Salg](sales-manage-sales.md)  
[Definere kontakter](marketing-setup-contacts.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
