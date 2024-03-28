---
title: Definere informasjon for kontakter | Microsoft-dokumentasjon
description: 'Skisserer oppgavene for å angi informasjon og koder, for eksempel om bransjegrupper og forretningsrelasjoner, før du konfigurerer kontakter.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'relationship, prospect'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Definere kontakter
Når du oppretter kontakter, kan du legge inn spesifikk informasjon, for eksempel bransjen der kontakten hører til, og forretningsforholdet ditt med kontaktene.

Før du oppretter kontakter og registrerer detaljer om forretningsforhold, må du sette opp de ulike kodene du vil bruke til å tilordne disse opplysningene til kontaktbedriftene og -personene. Koder kan settes opp for postgrupper, bransjegrupper, forretningsrelasjoner, webkilder, organisasjonsnivåer og ansvarsområder. Du kan konfigurere dette ved å velge **Ny**-handlingen når du slår opp i listene fra kontaktkortet.  

Når disse opplysningene er satt opp, kan du opprette kontakter på en mye mer organisert måte, og du kan finne alle kontakter basert på en bestemt gruppe på en mer effektiv måte. Alle grupper i bedriften kan finne disse opplysningene, noe som gir mer vellykket kommunikasjon med kontaktene.

##  Tilordne bransjegrupper til en kontakt
Du bruker bransjegrupper for å angi hvilken bransje kontaktene tilhører, for eksempel detaljistbransjen eller bilbransjen.

> [!NOTE]
> Dette er bare mulig for kontakter av typen **Selskap**.

Koden for bransjegruppen definerer typen eller kategorien for gruppen, for eksempel REKLAME for reklame, eller PRESSE, for TV og radio. Du kan ha flere koder for bransjegruppe. Hvis du vil definere bransjegrupper, bruker du siden **Bransjegrupper**.

1. Åpne det relevante kontaktkortet.
2. Velg handlingen **Selskap**, og deretter handlingen **Bransjegrupper**. Siden **Kontaktbransjegrupper** åpnes.
3. Velg bransjegruppen du vil tilordne, i feltet **Bransjegruppe - kode**.

Gjenta disse trinnene hvis du vil tilordne flere bransjegrupper. Du kan også tilordne bransjegrupper fra kontaktlisten ved å følge samme fremgangsmåte.

Antallet bransjegrupper du har tilordnet kontakten, vises i feltet **Ant. bransjegrupper** i inndelingen **Segmentering** på siden **Kontaktkort**.

Når du har tilordnet bransjegrupper til kontaktene, kan du bruke disse opplysningene til å velge kontakter for segmentene. Hvis du vil ha mer informasjon, kan du se [Legge til kontakter i segmenter](marketing-add-contact-segment.md).

##  Slik tilordner du postgrupper til en kontakt
Du kan bruke postgrupper til å identifisere grupper av kontakter som du ønsker skal motta like opplysninger. Du kan for eksempel definere en postgruppe for kontaktene du vil sende en melding om kontorflytting til, eller en annen gruppe for sending av julegavene.

Koden for postgruppen definerer typen eller kategori for gruppen, for eksempel FLYTTE for kontorflytting eller GAVE julegave. Du kan ha flere koder for bransjegruppe. Hvis du vil definere bransjegrupper, bruker du siden **Postgrupper**.

1. Åpne det relevante kontaktkortet.
2. Velg handlingen **Postgrupper**. Siden **Kontaktens postgrupper** åpnes.
3. Velg postgruppen du vil tilordne, i feltet **Postgruppekode**.

Gjenta disse trinnene hvis du vil tilordne flere postgrupper. Ved å følge samme fremgangsmåte kan du også tilordne postgrupper fra kontaktlisten.

Antallet postgrupper du har tilordnet kontakten, vises i feltet **Ant. postgrupper** i inndelingen **Segmentering** på siden **Kontaktkort**.

Når du har tilordnet postgrupper til kontaktene, kan du bruke disse opplysningene til å velge kontakter for segmentene. Hvis du vil ha mer informasjon, kan du se [Legge til kontakter i segmenter](marketing-add-contact-segment.md).

## Slik definerer du en kontakts alternative adresse
Du kan tilordne en alternativ adresse hvis kontakten noen ganger for eksempel ønsker å motta post og informasjon til kontaktens sommerhus. Hvis du vil angi når hver enkelt adresse er gyldig, kan du også tilordne ett eller flere datointervall til hver alternative adresse du har angitt for kontaktene.

1. Åpne det relevante kontaktkortet.
2. Velg handlingen **Alternativ adresse**, og velg deretter **Kort**-handlingen.

    Hvis du vil definere at den alternative adressen gjelder i en bestemt periode, kan du velge **Datointervall**-handlingen i stedet.
3. På siden **Kontaktens alt. adresse - oversikt** angir du en ny alternativ adresse og fyller ut feltene på siden for **alternativ adresse til kontakt**.

Gjenta disse trinnene hvis du vil tilordne flere alternative adresser. For hver alternative adresse bør du angi ett eller flere datointervaller.

## Slik tilordner du ansvarsområder til en kontakt
Du kan legge til informasjon om ansvarsområder for kontaktpersoner for å angi hva kontaktpersonen har ansvaret for i selskapet, for eksempel IT, ledelse eller produksjon. Du kan bruke denne informasjonen når du oppgir opplysninger om kontaktene.

> [!NOTE]
> Dette er bare mulig for kontakter av typen **Person**.

Koden for ansvarsområde definerer jobbtype eller -kategori, for eksempel MARKEDSFØRING eller INNKJØP. Du kan ha flere koder for ansvarsområde. Hvis du vil definere ansvarsområde, bruker du siden **Ansvarsområder**.

1. Åpne det relevante kontaktkortet.
2. Velg handlingen **Person**, og velg deretter handlingen **Ansvarsområder**. Siden **Kontaktens ansvarsområder** åpnes.
3. Velg ansvarsområdet som du vil tilordne, i feltet **Ansvarsområde - kode**.

Gjenta disse trinnene hvis du vil tilordne flere ansvarsområder. Ved å følge samme fremgangsmåte kan du også tilordne ansvarsområder fra kontaktlisten.

Antallet ansvarsområder du har tilordnet kontakten, vises i feltet **Ant. ansvarsområder** i inndelingen **Segmentering** på siden **Kontakt**.

Når du har tilordnet ansvarsområder til kontaktene, kan du bruke disse opplysningene til å velge kontakter for segmentene. Hvis du vil ha mer informasjon, kan du se [Legge til kontakter i segmenter](marketing-add-contact-segment.md).

## Slik tilordner du organisasjonsnivåer til en kontakt
Du kan bruke organisasjonsnivåer på kontaktene for å angi hvilken stilling de har i selskapet, for eksempel en stilling i toppledelsen. Du kan bruke denne informasjonen når du oppgir opplysninger om kontaktene.

> [!NOTE]
> Dette er bare mulig for kontakter av typen **Person**.

Koden for organisasjonsnivå definerer jobbtype eller -kategori for organisasjonsnivået, for eksempel ADMDIR eller ØKDIR. Du kan ha flere koder for organisasjonsnivå. Hvis du vil definere organisasjonsnivået, bruker du siden **Organisasjonsnivåer**.

1. Åpne det relevante kontaktkortet.
2. I feltet **Organisasjonsnivåer** velger du koden du vil tilordne.

Når du har tildelt organisasjonsnivåer til kontaktene, kan du bruke disse opplysningene til å opprette segmenter.

Når du har tilordnet ansvarsområder til kontaktene, kan du bruke disse opplysningene til å velge kontakter for segmentene. Hvis du vil ha mer informasjon, kan du se [Legge til kontakter i segmenter](marketing-add-contact-segment.md).

## Slik tilordner du webkilder til en kontakt
Du kan for eksempel bruke webkilder med kontaktselskaper for å identifisere søkemotorer og webområder på Internett, som du vil bruke til å søke etter informasjon om kontaktene. Når du tilordner webkilder, angir du hvilken søkemotor og søkeord programmet skal bruke for å finne de forespurte opplysningene.

> [!NOTE]
> Dette er bare mulig for kontakter av typen **Selskap**.

Når du tilordner webkilder, angir du hvilken søkemotor og søkeord som programmet skal bruke for å finne de forespurte opplysningene.

1. Åpne det relevante kontaktkortet.
2. Velg handlingen **Selskap**, og velg deretter handlingen **Webkilder**. Siden **Kontaktens webkilder** åpnes.
3. Velg webkilden du vil tilordne i feltet **Webkilde - kode**.
4. I feltet **Søkeord** angir du et søkeord som du vil bruke for å finne opplysningene.

Gjenta disse trinnene hvis du vil tilordne flere webkilder.

##  Tilordne forretningsforbindelser til en kontakt
Du kan bruke forretningsforbindelser blir brukt til å angi hvilket forretningsforhold du har til kontaktene, for eksempel prospekter, banker, konsulenter, serviceleverandører og så videre.

> [!NOTE]
> Dette er bare mulig for kontakter av typen **Selskap**.

1. Åpne det relevante kontaktkortet.
2. Velg handlingen **Selskap**, og deretter handlingen **Forretningsforbindelser**.
3. På siden **Kontaktens forretn.forbind.** i **Forretn.forbindelseskode**-feltet velger du forretningsforbindelsen du vil tilordne.

Gjenta disse trinnene hvis du vil tilordne flere forretningsforbindelser.

Antall forretningsforbindelser du har tilordnet kontakten, vises i feltet **Ant. forretningsforbindelser** i inndelingen **Segmentering** på siden **Kontakt**.

Når du har tilordnet forretningsforbindelser til kontaktene, kan du bruke disse opplysningene til å velge kontakter for segmentene. Hvis du vil ha mer informasjon, kan du se [Legge til kontakter i segmenter](marketing-add-contact-segment.md).

## Automatisk kopiere spesifikk informasjon fra kontaktselskapene til kontaktpersonene
Noen opplysninger om kontaktselskaper er identiske med opplysningene om kontaktpersonene som arbeider i disse selskapene, for eksempel opplysninger om adresse. På hurtigfanen **Arv** på siden **Markedsføringsoppsett** kan du angi hvilke felt på kontaktkortet for et firma som skal kopieres til kontaktkortet for en person hver gang du oppretter en kontaktperson for kontaktselskapet.

Når du endrer ett av disse feltene på kortet for kontaktselskapet, oppdateres de samme feltene på kortet til kontaktpersonen med mindre du har endret feltet manuelt på dette kortet.

Hvis du vil ha mer informasjon, kan du se [Opprette kontakter](marketing-create-contact-companies.md).

## Bruk forhåndsdefinerte standarder på nye kontakter
Du kan angi at hver gang du oppretter en ny kontakt, skal det automatisk tilordnes en bestemt språkkode, distriktskode, selgerkode og lands-/regionkode som standard. Du kan også angi en standard salgssykluskode som automatisk tilordnes hver nye salgsmulighet du oppretter. Du definere dette i **Standardverdier**-hurtigfanen på **Markedsføringsoppsett**-siden

Arv av felt overskriver standardverdiene du har definert. Hvis du for eksempel har definert norsk som standardspråk, men ett av kontaktselskapene bruker tysk, tildeles automatisk tysk som språkkode for de kontaktpersonene som står registrert for dette selskapet.

## Synkronisere kontakter med kunder, leverandører og bankkonti
Hvis du vil synkronisere kontaktkortet med en tilknyttet kunde, leverandør eller bankkontokortet, må du fylle ut det aktuelle feltet i inndelingen **Forr.forbindelseskode for** på **Samhandlinger**-hurtigfanen på **Markedsføringsoppsett**-siden.  

Hvis du vil ha mer informasjon, kan du se [Synkronisere kontakter med kunder, leverandører og bankkonti](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-employees-and-bank-accounts).

## Søke etter duplikatkontakter
Du kan angi at programmet skal foreta automatisk søk etter duplikater hver gang du oppretter en kontakt, eller du kan velge å søke manuelt etter at du har opprettet kontakter. Du kan også angi at programmet skal oppdatere søkestrengene automatisk hver gang du endrer kontaktopplysninger eller oppretter en kontakt. Du kan selv bestemme søketreffprosenten, det vil si hvor høy prosentandel to kontakter må ha av like strenger før de betraktes som duplikater. Du definerer dette på **Duplikater**-hurtigfanen på **Markedsføringsoppsett**-siden.

Når du har funnet en duplisert kontakt, kan du bruke siden **Slå sammen duplikat** til å flette det inn i en eksisterende kontaktpost som du vil beholde. Hvis du vil ha mer informasjon, se [Slå sammen dupliserte poster](sales-how-merge-duplicate-records.md).

## Se også
[Administrere kontakter](marketing-contacts.md)  
[Opprette kontakter](marketing-create-contact-companies.md)  
[Håndtere salgsmuligheter](marketing-manage-sales-opportunities.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]