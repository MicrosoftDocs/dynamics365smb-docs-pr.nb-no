---
title: Styr tilgang ved hjelp av sikkerhetsgrupper
description: Denne artikkelen beskriver hvordan du bruker sikkerhetsgrupper til å definere brukertillatelser.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'access, right, security, permissions'
ms.search.form: '1, 119, 8930, 9800, 9807, 9808, 9830, 9831, 9802, 9855, 9862'
ms.date: 02/08/2023
---

# Styr tilgang til Business Central ved å bruke sikkerhetsgrupper

[!INCLUDE [2023rw1-sec-group-long](includes/2023rw1-sec-group-long.md)]

Sikkerhetsgrupper gjør det enklere for administratorer å håndtere brukertillatelser i Dynamics 365-programmene, som SharePoint Online, CRM Online og nettversjonen av [!INCLUDE [prod_short](includes/prod_short.md)]. Administratorer legger til tillatelser i sikkerhetsgruppene, og når de legger til brukere i gruppen, gjelder tillatelsene for alle medlemmer. En administrator kan for eksempel opprette en sikkerhetsgruppe som gir selgere muligheten til å opprette og bokføre ordrer. Eller du kan la innkjøpere gjøre det samme for bestillinger.

Opprett sikkerhetsgruppene i administrasjonssenteret for Microsoft 365 eller Azure Active Directory. Denne artikkelen beskriver fremgangsmåten i administrasjonssenteret for Microsoft 365, men fremgangsmåten er lignende i begge.

## Legg til en sikkerhetsgruppe i administrasjonssenteret for Microsoft 365

1. Gå til siden **Aktive team og grupper** i administrasjonssenteret for Microsoft 365.
2. Velg **Legg til en gruppe**.
3. Velg gruppetypen **Sikkerhet** og velg deretter **Neste**.
4. Angi det grunnleggende for gruppen.
5. Valgfritt: Gjør medlemmene i gruppen tilgjengelig for rolletildeling. Hvis du vil lære mer om tildelingene, går du til [Bruk Azure AD-grupper til å behandle rolletildelinger](/azure/active-directory/roles/groups-concept).
6. Åpne gruppen, og bruk deretter fanen **Legg til medlemmer** til å inkludere personer i gruppen.

## Legg til en sikkerhetsgruppe i Business Central

I [!INCLUDE [prod_short](includes/prod_short.md)] oppretter du en sikkerhetsgruppe og kobler den til sikkerhetsgruppen i administrasjonssenteret for Microsoft 365. Den nye gruppen inneholder medlemmene du har lagt til i administrasjonssenteret for Microsoft 365.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Sikkerhetsgrupper**, og velg deretter den relaterte koblingen.
2. Velg **Opprett** for å opprette en gruppe.
3. Angi et navn for gruppen i **Navn**-feltet.
4. I feltet **Navn på AAD-sikkerhetsgruppe** skriver du inn navnet på sikkerhetsgruppen nøyaktig slik det vises i administrasjonssenteret for Microsoft 365. [!INCLUDE [prod_short](includes/prod_short.md)] vil finne den gruppen og koble den til denne gruppen.

> [!NOTE]
> Brukerne vises bare på **Medlemmer**-kortet i faktaboksen eller siden **Sikkerhetsgruppemedlemmer** hvis de er lagt til som brukere i [!INCLUDE [prod_short](includes/prod_short.md)]. Hvis du vil finne ut mer om å legge til brukere, går du til [Slik legger du til brukere eller oppdaterer brukerinformasjon og lisenstildelinger i Business Central](ui-how-users-permissions.md#adduser).  

### Tildel tillatelser til gruppen

1. På siden **Sikkerhetsgrupper** velger du gruppen og deretter handlingen **Tillatelser**.
1. Tildel tillatelser på følgende måter:
    * Hvis du vil tildele tillatelsessett enkeltvis, velger du tillatelsene som skal tildeles, i feltet **Tillatelsessett**.
    * Hvis du vil tildele flere tillatelsessett, velger du handlingen **Velg tillatelsessett**, og deretter velger du settene som skal tildeles.

## Gå gjennom tillatelsene i en sikkerhetsgruppe

På siden **Sikkerhetsgrupper** viser faktaboksen **tillatelsessettene** som er tildelt gruppen. Alle brukerne som er oppført på **Medlemmer**-kortet, har disse tillatelsene. Handlingen **Tillatelsessett etter sikkerhetsgruppe** gir en mer detaljert visning. Der kan du også utforske de enkelte tillatelsene i hver sikkerhetsgruppe.

Tillatelser er også tilgjengelige på **Brukere**-siden. Faktaboksen viser kortene **Tillatelsessett fra sikkerhetsgrupper** og **Medlemskap** for den valgte brukeren.

## Sikkerhetsgrupper og brukergrupper

Hvis du har brukergrupper, kan du konvertere gruppene til tillatelsessett i leieren ved å bruke veiledningen for assistert oppsett **Brukergruppeoverføring**. Når du skal starte veiledningen, finner du **Funksjon: Konverter brukergruppetillatelser** på siden **Funksjonsstyring**, og deretter velger du **Alle brukere** i feltet **Aktivert for**. Veiledningen for assistert oppsett inneholder følgende alternativer for konverteringen.

|Alternativ  |Beskrivelse  |
|---------|---------|
|Tildel til bruker     | Tildel tillatelsene i brukergrupper direkte til brukerne som ble tildelt til gruppen, og fjern brukergruppetildelingene.        |
|Konverter til et tillatelsessett     | Opprett en ny tillatelse for tillatelsene i hver brukergruppe. Det nye tillatelsessettet tildeles alle medlemmene i hver brukergruppe.          |

## Se også

[Opprette brukere i henhold til lisenser](ui-how-users-permissions.md)  
[Konfigurer Business Central-tilgang i Teams med Microsoft 365-lisenser](admin-access-with-m365-license-setup.md)  
[Finn ut mer grupper og tilgangsrettigheter i Azure Active Directory](/azure/active-directory/fundamentals/concept-learn-about-groups)  
[Sikkerhetsgrupper for Active Directory](/windows-server/identity/ad-ds/manage/understand-security-groups)  