---
title: Vanlige spørsmål om listevisninger
description: Detaljert informasjon om lagring av filtre som listevisninger.
author: mikebcMSFT
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: list, filter, pane, views
ms.date: 10/01/2020
ms.author: mikebc
ms.openlocfilehash: 17d7c909865bc077097ba4299e07ed2dd9cedb22
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5392477"
---
# <a name="list-views-faq"></a>Vanlige spørsmål om listevisninger
Denne artikkelen gir svar på spørsmål som våre avanserte brukere ofte spør om arbeid med listevisninger og lagring av filtre.  

### <a name="how-do-views-handle-expressions"></a>Hvordan håndterer visninger uttrykk?

Når du lagrer en visning som inkluderer filtre med uttrykk (for eksempel datointervaller, operatorer, nøkkelord eller filterkoder), lagres bare uttrykket og ikke resultatverdiene. Hvis du for eksempel lagrer en visning som filtrerer etter **Opprettingsdato**-feltet med uttrykket `-1W..today`, finner du alltid poster relatert til gjeldende dato, selv når visningen åpnes neste måned.

### <a name="where-are-list-views-saved"></a>Hvor lagres listevisninger?

På samme måte som når du skjuler et felt eller gjenbestiller av navigasjonsmenyen, er listevisninger en del av brukertilpasningene, og lagres i databasen. Når du fjerner all tilpasning i en liste, fjernes også personlige visninger og annen tilpasning permanent, for eksempel omorganisering av visninger. Hvis du vil ha mer informasjon, kan du se [Tilpasse arbeidsområdet](ui-personalization-user.md).

### <a name="why-dont-i-have-a-save-icon"></a><a name="save"></a>Hvorfor har jeg ikke et lagringsikon?

Det kan være et par årsaker til at du ikke ser lagringsikonet og alternativmenyen ved siden av visninger i filtreringsruten.

Én årsak kan være at den personlige tilpasningen ikke er aktivert for din brukerrolle. I dette tilfellet har du fortsatt tilgang til systemvisninger som er en standarddel av sidene. Du kan endre disse visningene, som å endre eller legge til filtre. Du kan bare ikke lagre endringene. En annen grunn kan være at siden du ser på, er en side av typen *forslag* og ikke en liste.

### <a name="on-which-page-types-can-i-use-list-views"></a>På hvilke sidetyper kan jeg bruke listevisninger?

Visninger er bare tilgjengelige på listesider.

### <a name="how-do-i-know-whether-im-on-list-type-page"></a>Hvordan vet jeg om jeg er på listetypeside?

Bruk sideinspeksjon. Trykk på CTRL + ALT + F1 for å åpne sideinspeksjon. Deretter kan du i feltet **Side** se etter ordet **Liste** i parentesen på slutten.

### <a name="are-views-also-available-on-other-form-factors"></a>Er visninger også tilgjengelige i andre formfaktorer?

Ja. Visninger du lagrer på skrivebordsleseren eller skrivebordsappen, vil også være tilgjengelige på nettbrettet eller smarttelefonen. Du kan ikke endre eller tilpasse visninger på mobile enheter.

### <a name="are-my-personal-views-always-accessible"></a>Er personlige visninger alltid tilgjengelige?

Visningene er tilgjengelige på en listeside hvis du åpner den fra navigasjonsmenyen, ved å bruke **Fortell meg**-vinduet eller via en URL-kobling til listesiden. Visninger er ikke tilgjengelige i listedeler, oppslag eller når en listeside vises som en dialogboks.

### <a name="how-do-i-return-a-view-to-its-original-filters-after-modifying-them"></a>Hvordan returnerer jeg en visning til opprinnelig filtre etter at de er endret?

Nederst i filtreringsruten velger du **Tilbakestill filtre**-handlingen for å fjerne filterendringer du har gjort i visningen, og gå tilbake til de opprinnelige filterfeltene og filterkriteriene.

### <a name="what-is-the-difference-between-hiding-and-removing-views"></a>Hva er forskjellen på å skjule og fjerne visninger?

Når du fjerner en visning, slettes denne visningen permanent. Når du skjuler en visning, kan du skjule den midlertidig fra filtreringsruten, men du kan vise den igjen senere ved å velge **Vis**-handlingen.

### <a name="how-can-i-share-my-views-with-others"></a>Hvordan kan jeg dele visningene med andre?

[!INCLUDE[prod_short](includes/prod_short.md)] gir ikke en måte å dele den nøyaktige listevisningen på. Du kan imidlertid dele nåværende filtre slik at andre brukere kan se en lignende liste med poster. I skrivebordsleseren kan du ganske enkelt kopiere URL-adressen og dele den med kollegene dine. Det er ikke garantert at deling av filtre gir mottakeren et identisk sett med filtre som du ser i nettleseren.

### <a name="can-i-search-for-views-in-the-tell-me-window"></a>Kan jeg søke etter visninger i Fortell meg-vinduet?

Nei. Vinduet **Fortell meg** viser bare søkeresultater for siden, men du er bare et trinn unna å komme til favorittvisningen når du har navigert til siden.

### <a name="what-is-shared-layout"></a>Hva er delt oppsett?

Alle visninger på en listeside deler et felles kolonneoppsett. Oppsettet omfatter hvilke kolonner som vises, rekkefølgen deres, bredde, frysingsrute og innstillinger for hurtigoppføring. Når du tilpasser kolonneoppsett, påvirkes også andre visninger som deler samme oppsett på listesiden.

Noen systemvisninger kan ha unike oppsett av kolonnene i listen. De kan for eksempel ordne kolonner på nytt, slik at bare kolonnene som er mest relevante for visningen, vises. Du kan identifisere hvilke visninger som har unike oppsett, ved å velge ikonet ![Vis flere alternativer](media/show-more-options-icon.png "Vis flere alternativer") og observere at avmerkingsboksen for **Delt oppsett** ikke er valgt. Som bruker kan du tilpasse kolonneoppsettet for en visning med et eget oppsett uten at det påvirker noen av de andre visningene på listesiden. Bare utviklere kan definere et unikt kolonneoppsett for en visning som i utgangspunktet har et delt oppsett.

### <a name="what-does-the-show-system-filters-link-do"></a>Hva gjør koblingen Vis systemfiltre?

På noen listesider viser filterruten **Vis systemfiltre** nederst, særlig når siden inneholder filtre som er angitt av systemet. Disse spesialfiltrene brukes vanligvis til å vise poster basert på gjeldende kontekst. Det kan for eksempel være at en ordreliste må filtreres for en bestemt kunde.

Systemfiltre angis av programutviklere, som de angir ved å bruke filtergruppe 0. Hvis du vil mer informasjon om systemet, se [Filtergruppemetode](/dynamics365/business-central/dev-itpro/developer/methods-auto/record/record-filtergroup-method).

### <a name="i-see-multiple-views-on-my-page-but-i-didnt-create-them-where-did-they-come-from"></a>Jeg ser flere visninger på siden, men jeg opprettet dem ikke. Hvor kom de fra?

Visningene du ser i en hvilken som helst liste, er en kombinasjon av personlige visninger og systemvisninger. Det kan hende at systemvisninger kommer fra forretningsprogrammet, fra utvidelser eller er rollespesifikke hvis listen ble tilpasset for din rolle.

### <a name="why-do-some-views-provide-fewer-options"></a>Hvorfor gir noen visninger færre alternativer?

Enkelte visninger gir deg bare muligheten til å lagre en kopi av visningen, mens andre ikke tillater lagring av endringer i visningen. Hvordan visningen ble opprettet, bestemmer hvilke alternativer som er tilgjengelige for denne visningen. Visninger kan opprettes på flere måter:

- Personlige visninger du har lagret
- Systemvisninger som er en standard del av forretningsapplikasjonen eller er lagt til av utvidelser eller rollespesifikke visninger. I motsetning til personlige visninger kan du ikke lagre endringer i filtre tilbake til systemvisningen.
- Eldre systemvisninger som er en standard del av forretningsprogrammet, men som er opprettet med eldre versjoner av [!INCLUDE[prod_short](includes/prod_short.md)]. Disse visningene gir færre alternativer. Du kan bare lagre dem som en ny visning og ikke skjule eller endre rekkefølgen på dem. Eldre systemvisninger avvikles i en fremtidig oppdatering av [!INCLUDE[prod_short](includes/prod_short.md)].

### <a name="how-do-i-convert-legacy-system-views"></a>Hvordan konverterer jeg eldre systemvisninger?

Eldre systemvisninger er listevisninger som ble opprettet av utviklere i eldre versjoner av [!INCLUDE[prod_short](includes/prod_short.md)] ved å plassere dem på rollesentersiden. Disse visningene vises nå direkte på listesiden, men tilbyr en redusert opplevelse og færre alternativer. Du kan konvertere en eldre systemvisning til en personlig visning som kan tilpasses fullstendig, ved ganske enkelt å lagre den eldre visningen som en ny visning. Systemansvarlige kan også velge å konvertere rollespesifikke eldre systemvisninger ved å tilpasse brukerrollen og lagre den gamle visningen som en ny rollespesifikk visning.

Eldre systemvisninger avvikles i en fremtidig oppdatering av [!INCLUDE[prod_short](includes/prod_short.md)].

### <a name="others-in-my-organization-need-similar-list-views-as-standard-what-can-i-do"></a>Andre i organisasjonen min trenger lignende listevisninger som standard. Hva kan jeg gjøre?

Det å arbeide med personlige visninger er raskt og effektivt, men [!INCLUDE[prod_short](includes/prod_short.md)] inneholder andre verktøy for å definere listevisninger som kreves av bestemte brukerroller eller alle brukere i organisasjonen.
 - Utviklere kan tilpasse miljøet og opprette listevisninger i utvidelser for alle brukere i organisasjonen.
 - Personer som ikke koder, som administratorer eller avdelingsledere, kan opprette rollespesifikke listevisninger ved tilpasning av en rolle fra siden **Profiler (roller)**.

### <a name="i-work-with-multiple-languages-how-do-i-translate-the-name-of-the-view"></a>Jeg arbeider med flere språk: hvordan oversetter jeg navnet på visningen?

Når du lagrer en ny visning eller gir nytt navn til en eksisterende visning, må du angi et gjenkjennelig og beskrivende navn for denne visningen. Navnet lagres for det gjeldende språket ditt og vises også når du eller andre brukere arbeider med [!INCLUDE[prod_short](includes/prod_short.md)] på forskjellige språk. Hvis du vil angi oversatte visningsnavn, bytter du språk ved hjelp av siden **Mine innstillinger**. Gi deretter nytt navn til visningen, som vil lagre det oversatte navnet på det nye språket.

### <a name="do-views-with-expressions-work-in-all-languages"></a>Fungerer visninger med uttrykk på alle språk?

Uttrykk som bare bruker symboler, for eksempel `|` eller `..`, anses som trygge for brukere å få tilgang til alle språk. Alle visninger med uttrykk som inneholder bokstaver, nøkkelord eller filterkoder, fungerer bare for språket de ble laget i.

### <a name="see-also"></a>Se også

[Lagre og tilpasse listevisninger](ui-views.md)  
[Finne funksjoner og informasjon](ui-search.md)  
[Sortere, søke etter og filtrere](ui-enter-criteria-filters.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]