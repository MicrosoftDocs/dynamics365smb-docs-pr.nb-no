---
title: Legg til markedsføringstekst i varer
description: Skrive markedsføringstekst for varer i Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 06/10/2024
ms.custom: bap-template
ms.collection:
  - bap-ai-copilot
ms.search.form: 5839_Primary
---

# Legg til markedsføringstekst i varer

For alle varer som er registrert i Business Central, kan du skrive *markedsføringstekst* for varen. Selv om markedsføringstekst er en slags beskrivelse, er den forskjellig fra en vares **Beskrivelse**-felt. **Beskrivelse**-feltet brukes vanligvis som et konsekvent visningsnavn for å identifisere produktet raskt. Markedsføringsteksten er derimot en mer omfattende og beskrivende tekst. Formålet er å legge til markedsførings- og kampanjeinnhold, også kalt *kopi*. Denne teksten kan deretter publiseres med varen hvis den er publisert i en nettbutikk, som Shopify, eller limt inn i e-post eller annen kommunikasjon med kundene dine.

Det finnes to måter å opprette markedsføringstekst på. Den enkleste måten å komme i gang på er å bruke Copilot, som foreslår tekst generert av kunstig intelligens for deg. Den andre måten er å starte fra grunnen av. 

## <a name=copilot></a>Få markedsføringstekstforslag med Copilot

Med Copilot får du raskt et tekstforslag som genereres automatisk for deg. Teksten generert av kunstig intelligens er skreddersydd for varen og gir et bra utgangspunkt. Teksten er basert på en del av følgende informasjon:

- Attributter som er definert for varen &mdash; som beskrivelse, farge, dimensjoner, materiale og så videre. [Finn ut mer om vareattributter](inventory-how-work-item-attributes.md).
- Varens **Beskrivelse**-felt.
- Varekategorien. [Finn ut mer om å kategorisere varer](inventory-how-categorize-items.md).
- Valgbare stilinnstillinger som ordlyd, format og lengde.

Copilot er utformet for å spare tid og hjelpe deg med å skrive kreativ og engasjerende tekst som gjenspeiler varemerket ditt, og som er konsekvent på tvers av produktserien. Begynn med å generere et forslag, og endre den foreslåtte teksten etter behov.

### Tilgjengelige språk

[!INCLUDE[copilot-supported-languages.md](includes/copilot-supported-languages.md)]

### Forutsetninger

Funksjonen for forslag til markedsføringstekst er aktivert i miljøet ditt. Denne oppgaven utføres vanligvis av en administrator. Hvis du vil ha mer informasjon, kan du gå til [Konfigurer Copilot og KI-funksjoner](enable-ai.md).

### Opprett første utkast med Copilot

Følg fremgangsmåten nedenfor for å legge til markedsføringstekst i en eksisterende vare. Hvis du vil ha mer informasjon om hvordan du oppretter en ny vare, kan du gå til [Registrer nye varer](inventory-how-register-new-items.md).

1. I Business Central åpner du varen du vil endre, ved å fullføre følgende trinn:

   - Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen 22.](media/ui-search/search_small.png "Fortell hva du vil gjøre") øverst til høyre og angi **Varer**, og velg deretter relatert kobling for å vise en liste over tilgjengelige varer.

   - Dobbeltklikk på varen, eller velg verdien i **Nr.** .

1. Fra varekortet kan du komme i gang med å skrive markedsføringstekst med Copilot på to måter: fra faktaboksen **Markedsføringstekst** eller ved hjelp av handlingen **Markedsføringstekst**. Disse metodene angis i figuren nedenfor på et varekort.  

   [![Viser et varekort med ruten Markedsføringstekst](media/create-with-copilot.svg)](media/create-with-copilot.svg#lightbox)

   Hvis du vil opprette det første utkastet for en vare, gjør du et av følgende:

   - Velg **Opprett utkast med Copilot** i ruten **Markedsføringstekst** i faktaboksen til høyre på siden. 

     Copilot begynner å utarbeide markedsføringsteksten.

   - Velg handlingen **Markedsføringstekst** øverst på siden, og velg deretter **Utkast med Copilot** i vinduet **Rediger markedsføringstekst**.  Vinduene **Lag utkast til markedsføringstekst med Copilot** vises med en liste over alle tilgjengelige attributter for varen.
1. Velg attributtene du vil at Copilot-baseforslag skal brukes på, og velg deretter **Generer**. Du kan endre de valgte attributtene og andre alternativer senere. Copilot begynner å utarbeide markedsføringsteksten. 

   ![Viser vinduet for redigering av markedsføringstekst](media/marketing-text-copilot-attributes.svg)

1. Når Copilot fullfører utkastet, vises teksten i Copilot-redigeringsvinduet som du kan gå gjennom og redigere.

   [![Viser vinduene Opprett med Copilot](media/create-with-copilot-window.svg)](media/create-with-copilot-window.svg#lightbox)

   Nå kan du få flere forslag, forsøke å forbedre forslagene du får, redigere tekst med mer. Gå til [Se gjennom, rediger og lagre](#review-edit-and-save-text) for mer informasjon.

### Se gjennom, rediger og lagre teksten

Når du har det første utkastet, må du se gjennom det og gjøre endringer i teksten for å få den klar til publisering. Dette arbeidet gjøres fra Copilot-redigering, som lar deg få flere forslag, endre innstillingene til å påvirke forslagene og manuelt gjøre endringer og legge på stil i teksten.

> [!IMPORTANT]
> Teksten genererte med kunstig intelligens fra Copilot er bare et forslag og kan ha feil. Den krever menneskelig overstyring og gjennomgang for å sikre at den er nøyaktig og passende Se gjennom eventuell foreslått tekst, og rediger etter behov før du lagrer og publiserer den til offentlig bruk.

Bruk følgende retningslinjer for å fullføre og lagre markedsføringsteksten.

1. Gjør endringer i teksten direkte i tekstboksen. Bruk verktøylinjen langs bunnen av boksen til å formatere tekst, legge til koblinger med mer.
2. Hvis du vil ha et nytt forslag, velger du **Generer på nytt**.
3. Hvis du ikke er fornøyd med forslagene, kan du forbedre tekstforslagene ved hjelp av innstillingsalternativene **Tone**, **Format** og **Utheving**.

   <!--Select **More Settings**, change the options that are shown under **Choose how Copilot creates suggestions**, then select **Create draft** to get a new suggestion.-->

   For å få veiledning om hvordan du kan forbedre forslagene, kan du gå til [Forbedre og skreddersy tekstforslag](#improve-and-tailor-text-suggestions).

4. For å gå frem og tilbake gjennom forslag, bruk forrige og neste lenke øverst på siden (*x* **av** *y*). <!-- or select the **...** (More formatting options) along the bottom of the window, then select **Undo**. Select **Redo** to go back.-->
5. Se nøye gjennom teksten for nøyaktighet og relevant:

   - Hvis du vil lagre teksten, velger du **Behold den**. 
   - Hvis du ikke vil lagre, velger du forkast-knappen (papirkurv) ![Viser papirkurvikonet for sletting av alle Copilot-forslag for bankkontoavstemming](media/copilot-delete-trash-can.png).

### Forbedre og skreddersy tekstforslag

Det finnes et par trinn du kan gjøre for å forbedre tekstforslagene og endre dem slik at de passer til personlige innstillinger eller firmainnstillinger.

1. Endre vareattributtene som brukes av Copilot.

   Copilot-forslat er delvis basert på attributtene som er tildelt til varen. Hvis du vil vise de tilgjengelige attributtene og gjeldende innstillinger, velger du ![Viser redigeringsikonet i Copilot-vinduet for å endre attributtikonet](media/edit-pencil.png) øverst til venstre. På siden **Vareattributter** velger du attributtene som er best samkjørt med egenskapene du vil promotere. Jo mer relevante attributtene du inkluderer er, jo mer omfattende blir resultatet. Hvis du mener at du mangler noen viktige attributter, legger du til flere. Hvis du vil ha mer informasjon om attributter, kan du gå til [Arbeid med vareattributter](inventory-how-work-item-attributes.md)
1. Endre innstillingene for alternativene **Tone**, **Format** og **Utheving**.

   |Alternativ|Description|
   |-|-|
   |Tone |Bruk dette alternativet til å påvirke hva slags ord, fraser og tegnsetting som brukes til å engasjere målgruppen. Du kan velge blant flere forhåndsdefinerte ordlyder, fra **Formell** (som gir en forretningsmessig ordlyd) til **Kreativ** (som resulterer i en uformell ordlyd). |
   |Format og lengde|Bruk dette alternativet til å styre den generelle strukturen for teksten, som består av tre deler, dekket av fire ulike alternativer: <ul><li>**Slagord** – et uttrykk eller en kort setning som identifiserer varen eller merket.</li><li>**Avsnitt** – ett enkelt avsnitt med flytende og detaljert tekst, som består av flere fullstendige setninger.</li><li>**Slagord + avsnitt** – et slagord etterfulgt av et avsnitt</li><li>**Kort** – en innledende setning, som ligner på en beskrivelse, etterfulgt av en punktliste med viktige nøkkelpunkter.</li></ul> |
   |Vektlegging|Bruk dette alternativet til å velge fra en liste over forhåndsdefinerte kvaliteter som du vil fremheve i teksten. Velg en kvalitet som best samkjøres med typen vare du skriver om. Egenskapene samsvarer ikke direkte med varens attributter, beskrivelse eller kategori. **Kvalitet** kan for eksempel være et godt valg for både en sykkel eller et skrivebord, mens **Hastighet** passer til en sykkel, men ikke et skrivebord.|

1. Forbedre **Beskrivelse**-feltet på varekortet.

   Teksten i **Beskrivelse**-feltet blir brukt som den er mange steder i den foreslåtte teksten, så det er viktig at beskrivelsen best viser hvordan du vil at det skal henvises til varen i markedsføringsteksten. 

1. Kontroller at feltet **Varekategorikode** på varekortet er satt til en riktig kategori.

   Copilot finner ord og uttrykk som er knyttet til kategorien, og arbeide dem i den foreslåtte teksten.

### Arbeid med flere språk 

Tekst genereres alltid på språket som er definert av [brukerinnstillingene](ui-change-basic-settings.md#language). Hvis organisasjonen din driver og legger inn data i Business Central på et annet språk, eller hvis Business Central er koblet til nettbutikken din, for eksempel Shopify, kan dette føre til publisering av innhold som ikke samsvarer med lignende markedsføringsinnhold.

## Opprett tekst fra grunnen av

1. I Business Central åpner du varen du vil endre, slik:

    1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen 22.](media/ui-search/search_small.png "Fortell hva du vil gjøre") øverst til høyre og angi **Varer**, og velg deretter relatert kobling for å vise en liste over tilgjengelige varer.
    2. Hvis du vil åpne varen, dobbeltklikker du på den eller velger nummeret i feltet **Nr.** .

2. Gjør ett av følgende:

   - Velg **Rediger** i ruten **Markedsføringstekst** i faktaboksen til høyre på siden.
   - Velg handlingen **Markedsføringstekst**.
3. Gjør endringer i teksten direkte i boksen **Markedsføringstekst**. Bruk verktøylinjen langs bunnen av boksen til å formatere tekst, legge til koblinger med mer.
4. Velg **OK** når du er ferdig for å lagre teksten.

## Se også

[Oversikt over forslag til markedsføringstekst](ai-overview.md)  
[Feilsøk Copilot- og KI-funksjoner](ai-copilot-troubleshooting.md)  
[Vanlige spørsmål om forslag til markedsføringstekst](faqs-marketing-text.md)  
[Konfigurer Copilot- og KI-funksjoner](enable-ai.md)  
[Registrer nye varer](inventory-how-register-new-items.md)  
