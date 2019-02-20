---
title: Definere informasjon for kontakter | Microsoft-dokumentasjon
description: "Skisserer oppgavene for å angi informasjon og koder, for eksempel om bransjegrupper og forretningsrelasjoner, før du konfigurerer kontakter."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 12/07/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 8a73de1aa2f4a0f633c401ea341bb7bde6579723
ms.openlocfilehash: 1f186a1eb1386d1f54b27a7ee9a9b3445c19e469
ms.contentlocale: nb-no
ms.lasthandoff: 12/11/2018

---
# <a name="setting-up-contacts"></a>Konfigurere kontakter
Når du oppretter kontakter, kan du legge inn spesifikk informasjon, for eksempel bransjen der kontaktbedriftene hører til, og forretningsforholdet ditt med kontaktene.

Før du oppretter kontakter og registrerer detaljer om forretningsforhold, må du sette opp de ulike kodene du vil bruke til å tilordne disse opplysningene til kontaktbedriftene og -personene. Koder kan settes opp for postgrupper, bransjegrupper, forretningsrelasjoner, webkilder, organisasjonsnivåer og ansvarsområder.

Når disse opplysningene er satt opp, kan du opprette kontakter på en mye mer organisert måte, og du kan finne alle kontakter basert på en bestemt gruppe på en mer effektiv måte. Alle grupper i bedriften kan finne disse opplysningene, noe som gir mer vellykket kommunikasjon med kontaktene.

I forbindelse med konfigurasjon av kontakter må du definere forretningsforbindelser til kontakter, for eksempel prospekter, banker, konsulenter og serviceleverandører. Hvis du vil ha mer informasjon, se [Definere forretningsforbindelser i kontaktselskaper](marketing-business-relations.md).

## <a name="setting-up-industry-groups-for-contact-companies"></a>Definere bransjegrupper for kontaktselskaper
Du bruker bransjegrupper for å angi hvilken bransje kontaktene tilhører, for eksempel detaljistbransjen eller bilbransjen.

Bruk av bransjegrupper på kontakter er en totrinnsprosess. Først må definere du koden for bransjegruppen. Du trenger bare utføre dette trinnet én gang for hver bransjegruppe. Når du har en kode for bransjegruppe, kan du begynne å tilordne koden til kontaktselskaper.

> [!NOTE]  
>   Hvis du planlegger å synkronisere kontaktene med leverandører, kunder eller bankkonti i andre deler av programmet, bør du definere en forretningsforbindelse for disse.

### <a name="to-define-an-industry-group-code"></a>Definere en kode for bransjegruppe
Koden for bransjegruppen definerer typen eller kategorien for gruppen, for eksempel REKLAME for reklame, eller PRESSE, for TV og radio. Du kan ha flere koder for bransjegruppe. Hvis du vil definere bransjegrupper, bruker du siden **Bransjegrupper**.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bransjegrupper**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Ny**, og fyll ut en kode og en beskrivelse. Koden kan bestå av opptil 11 tegn, og kan inneholde en kombinasjon av tall og bokstaver.

### <a name="AssignIndustryGroupContact"></a> Tilordne bransjegrupper til en kontakt
Du kan ikke tilordne bransjegrupper til en kontaktperson, bare selskaper.

1. Åpne kontakten.
2. Velg handlingen **Selskap**, og deretter handlingen **Bransjegrupper**. Siden **Kontaktbransjegrupper** åpnes.
3. Velg bransjegruppen du vil tilordne, i feltet **Bransjegruppe - kode**.

Gjenta disse trinnene hvis du vil tilordne flere bransjegrupper. Du kan også tilordne bransjegrupper fra kontaktlisten ved å følge samme fremgangsmåte.

Antallet bransjegrupper du har tilordnet kontakten, vises i feltet **Ant. bransjegrupper** i inndelingen **Segmentering** på siden **Kontakt**.

Når du har tilordnet bransjegrupper til kontaktene, kan du bruke disse opplysningene til å velge kontakter for segmentene. Hvis du vil ha mer informasjon, kan du se [Legge til kontakter i segmenter](marketing-add-contact-segment.md).

## <a name="setting-up-mailing-groups-for-contacts"></a>Definere postgrupper for kontakter
Du kan bruke postgrupper til å identifisere grupper av kontakter som du ønsker skal motta like opplysninger. Du kan for eksempel definere en postgruppe for kontaktene du vil sende en melding om kontorflytting til, eller en annen gruppe for sending av julegavene.

Bruk av postgrupper på kontakter er en totrinnsprosess. Først må definere du koden for postgruppen. Du trenger bare utføre dette trinnet én gang for hver postgruppe. Når du har en kode for postgruppe, kan du begynne å tilordne koden til kontaktselskaper.

### <a name="to-define-mailing-group-codes"></a>Definere postgruppekoder
Koden for postgruppen definerer typen eller kategori for gruppen, for eksempel FLYTTE for kontorflytting eller GAVE julegave. Du kan ha flere koder for bransjegruppe. Hvis du vil definere bransjegrupper, bruker du siden **Postgrupper**.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Postgrupper**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Ny**, og fyll ut en kode og en beskrivelse. Koden kan bestå av opptil 11 tegn, og kan inneholde en kombinasjon av tall og bokstaver.

### <a name="AssignMailGroupContact"></a> Slik tilordner du postgrupper til en kontakt
1. Åpne kontakten.
2. Velg handlingen **Postgrupper**. Siden **Kontaktens postgrupper** åpnes.
3. Velg postgruppen du vil tilordne, i feltet **Postgruppekode**.

Gjenta disse trinnene hvis du vil tilordne flere postgrupper. Ved å følge samme fremgangsmåte kan du også tilordne postgrupper fra kontaktlisten.

Antallet postgrupper du har tilordnet kontakten, vises i feltet **Ant. postgrupper** i inndelingen **Segmentering** på siden **Kontakt**.

Når du har tilordnet postgrupper til kontaktene, kan du bruke disse opplysningene til å velge kontakter for segmentene. Hvis du vil ha mer informasjon, kan du se [Legge til kontakter i segmenter](marketing-add-contact-segment.md).

## <a name="setting-up-alternate-addresses-for-contacts"></a>Definerer alternative adresser for kontakter
Du kan tilordne en alternativ adresse hvis det hender at du for eksempel sender post og informasjon til kontaktens sommerhus. Hvis du vil angi når hver enkelt adresse er gyldig, kan du også tilordne ett eller flere datointervall til hver alternative adresse du har angitt for kontaktene.

### <a name="to-assign-an-alternate-address"></a>Slik tilordner du en alternativ adresse
1. Åpne kontakten.
2. Velg handlingen **Alternativ adresse**, og velg deretter **Kort**. Siden **Kontaktens alt. adresse - oversikt** åpnes.
3. Angi en ny alternativ adresse, og fyll ut feltene på siden for **alternativ adresse til kontakt**.

Gjenta disse trinnene hvis du vil tilordne flere alternative adresser. For hver alternative adresse bør du angi ett eller flere datointervaller.

Ved å følge samme fremgangsmåte kan du også tilordne alternative adresser fra kontaktlistesiden.

### <a name="to-assign-an-alternate-address-date-range"></a>Slik tilordner du datointervall for alternativ adresse
1. Åpne kontakten.
2. Velg handlingen **Alternativ adresse**, og velg deretter **Datointervall**. Siden **Datointervall for kontaktens alt. adr.** åpnes.
3. Velg handlingen **Ny**.
4. I feltet **Kontaktens alt. adresse - kode** velger du en alternativ adresse for denne kontakten, og deretter fyller du ut feltene **Startdato** og **Sluttdato**.

Gjenta disse trinnene hvis du vil tilordne flere datointervaller.

## <a name="setting-up-job-responsibilities-for-contact-persons"></a>Definere ansvarsområder for kontaktpersoner
Du kan legge til informasjon om ansvarsområder for kontaktpersoner for å angi hva kontaktpersonen har ansvaret for i selskapet, for eksempel IT, ledelse eller produksjon. Du kan bruke denne informasjonen når du oppgir opplysninger om kontaktene.

Bruk av ansvarsområder på kontakter er en totrinnsprosess. Først må definere du koden for ansvarsområdet. Du trenger bare utføre dette trinnet én gang for hvert ansvarsområde. Når du har en kode for ansvarsområde, kan du begynne å tilordne koden til kontaktpersoner.

### <a name="to-define-a-job-responsibility-code"></a>Definere en kode for ansvarsområde
Koden for ansvarsområde definerer jobbtype eller -kategori, for eksempel MARKEDSFØRING eller INNKJØP. Du kan ha flere koder for ansvarsområde. Hvis du vil definere ansvarsområde, bruker du siden **Ansvarsområder**.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Ansvarsområder**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Ny**, og fyll ut en kode og en beskrivelse. Koden kan bestå av opptil 11 tegn, og kan inneholde en kombinasjon av tall og bokstaver.

### <a name="to-assign-job-responsibilities-to-a-contact-person"></a>Tilordne ansvarsområder til en kontaktperson
Du kan ikke tilordne ansvarsområder til kontaktselskaper.

1. Åpne kontaktpersonen.
2. Velg handlingen **Person**, og velg deretter handlingen **Ansvarsområder**. Siden **Kontaktens ansvarsområder** åpnes.
3. Velg ansvarsområdet som du vil tilordne, i feltet **Ansvarsområde - kode**.

Gjenta disse trinnene hvis du vil tilordne flere ansvarsområder. Ved å følge samme fremgangsmåte kan du også tilordne ansvarsområder fra kontaktlisten.

Antallet ansvarsområder du har tilordnet kontakten, vises i feltet **Ant. ansvarsområder** i inndelingen **Segmentering** på siden **Kontakt**.

Når du har tilordnet ansvarsområder til kontaktene, kan du bruke disse opplysningene til å velge kontakter for segmentene. Hvis du vil ha mer informasjon, kan du se [Legge til kontakter i segmenter](marketing-add-contact-segment.md).

## <a name="setting-up-organizational-levels-for-contact-persons"></a>Definere organisasjonsnivåer for kontaktpersoner
Du kan bruke organisasjonsnivåer på kontaktene for å angi hvilken stilling de har i selskapet, for eksempel en stilling i toppledelsen. Du kan bruke denne informasjonen når du oppgir opplysninger om kontaktene.

Bruk av organisasjonsnivåer på kontakter er en totrinnsprosess. Først må du definere koden for organisasjonsnivået. Du trenger bare utføre dette trinnet én gang for hvert organisasjonsnivå. Når du har en kode for organisasjonsnivå, kan du begynne å tilordne koden til kontaktpersoner.

### <a name="to-define-an-organizational-level-code"></a>Slik definerer du en kode for organisasjonsnivå
Koden for organisasjonsnivå definerer jobbtype eller -kategori for organisasjonsnivået, for eksempel ADMDIR eller ØKDIR. Du kan ha flere koder for organisasjonsnivå. Hvis du vil definere organisasjonsnivået, bruker du siden **Organisasjonsnivåer**.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Organisasjonsnivåer**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Ny**, og fyll ut en kode og en beskrivelse. Koden kan bestå av opptil 11 tegn, og kan inneholde en kombinasjon av tall og bokstaver.

### <a name="to-assign-organizational-levels-to-a-contact-person"></a>Slik tilordner du organisasjonsnivåer til en kontaktperson
Du kan bare tilordne organisasjonsnivåer til kontaktpersoner, ikke selskaper. Du kan bare tilordne ett organisasjonsnivå til hver enkelt kontakt.

1. Åpne kontakten.
2. I feltet **Organisasjonsnivåer** velger du koden du vil tilordne.

Når du har tildelt organisasjonsnivåer til kontaktene, kan du bruke disse opplysningene til å opprette segmenter.

Når du har tilordnet ansvarsområder til kontaktene, kan du bruke disse opplysningene til å velge kontakter for segmentene. Hvis du vil ha mer informasjon, kan du se [Legge til kontakter i segmenter](marketing-add-contact-segment.md).

## <a name="setting-up-web-sources-for-contact-companies"></a>Definere webkilder for kontaktselskaper
Du kan for eksempel bruke webkilder med kontaktselskaper for å identifisere søkemotorer og webområder på Internett, som du vil bruke til å søke etter informasjon om kontaktene. Når du tilordner webkilder, angir du hvilken søkemotor og søkeord programmet skal bruke for å finne de forespurte opplysningene.

Bruk av webkilder på kontakter er en totrinnsprosess. Først må du definere koden for webkilden. Du trenger bare utføre dette trinnet én gang for hver webkilde. Når du har en kode for webkilde, kan du begynne å tilordne koden til kontaktpersoner.

### <a name="to-define-a-web-source-code"></a>Slik definerer du en kode for webkilde
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Webkilder**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Ny**.
3. Fyll ut feltene **Kode**, **Beskrivelse** og **URL**.

    Skriv inn %1 i feltet **Nettadresse** for å sette inn en plassholder for et søkeord i nettadressen. Når du starter webkilden fra et kontaktkort, erstattes %1 med søkeordet (for eksempel navnet på selskapet) som du angav på siden **Kontaktens webkilder**.

Gjenta disse trinnene hvis du vil definere flere webkilder.

### <a name="to-assign-web-sources-to-a-contact-company"></a>Slik tilordner du webkilder til et kontaktselskap
Når du tilordner webkilder, angir du hvilken søkemotor og søkeord som programmet skal bruke for å finne de forespurte opplysningene.

1. Åpne kontakten.
2. Velg handlingen **Selskap**, og velg deretter handlingen **Webkilder**. Siden **Kontaktens webkilder** åpnes.
3. Velg webkilden du vil tilordne i feltet **Webkilde - kode**.
4. I feltet **Søkeord** angir du et søkeord som du vil bruke for å finne opplysningene.

Gjenta disse trinnene hvis du vil tilordne flere webkilder.

Ved å følge samme fremgangsmåte kan du også tilordne webkilder på siden **Kontaktoversikt**.

## <a name="see-also"></a>Se også
[Administrere kontakter](marketing-contacts.md)  
[Håndtere salgsmuligheter](marketing-manage-sales-opportunities.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

