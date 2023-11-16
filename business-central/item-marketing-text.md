---
title: Legg til markedsføringstekst i varer
description: Skriv markedsføringstekst for varer i Business Central
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 03/22/2023
ms.custom: bap-template
---

# <a name="add-marketing-text-to-items"></a>Legg til markedsføringstekst i varer

For alle varer som er registrert i Business Central, kan du skrive *markedsføringstekst* for varen. Selv om markedsføringstekst er en slags beskrivelse, er den forskjellig fra en vares **Beskrivelse**-felt. **Beskrivelse**-feltet brukes vanligvis som et konsekvent visningsnavn for å identifisere produktet raskt. Markedsføringsteksten er derimot en mer omfattende og beskrivende tekst. Formålet er å legge til markedsførings- og kampanjeinnhold, også kalt *kopi*. Denne teksten kan deretter publiseres med varen hvis den er publisert i en nettbutikk som Shopify.

Det finnes to måter å opprette markedsføringstekst på. Den enkleste måten å komme i gang på er å bruke Copilot, som foreslår tekst generert av kunstig intelligens for deg. Den andre måten er å starte fra grunnen av. 

## <a name="get-marketing-text-suggestions-with-copilot"></a><a name=copilot></a>Opprett markedsføringstekst generert av kunstig intelligens (forhåndsversjon) med Copilot

[!INCLUDE[ai-preview](includes/ai-preview.md)]

Med Copilot får du raskt et tekstforslag som genereres automatisk for deg. Teksten generert av kunstig intelligens er skreddersydd for varen og gir et bra utgangspunkt. Teksten er basert på en del av følgende informasjon:

- Attributter som er definert for varen, som beskrivelse, farge, dimensjoner, materiale og så videre.
- Valgbare stilinnstillinger som ordlyd, format og lengde.

Copilot er utformet for å spare tid og hjelpe deg med å skrive kreativ og engasjerende tekst som gjenspeiler varemerket ditt, og som er konsekvent på tvers av produktserien. Begynn med å generere et forslag, og endre den foreslåtte teksten etter behov.

> [!NOTE]
> I forhåndsversjonen av Business Central er tekst generert av kunstig intelligens bare på engelsk.

### <a name="prerequisites"></a>Forutsetninger

- Du bruker en [forhåndsversjon](ai-preview-getstarted.md) av Business Central som er aktivert for Copilot. Aktivering av Copilot gjøres av en administrator. Hvis du vil ha mer informasjon, kan du gå til [Konfigurer varemarkedsføringstekst drevet av kunstig intelligens med Copilot](enable-ai.md).
- Språket du bruker i Business Central må være engelsk. Alle tilgjengelige engelske nasjonale innstillinger fungerer, for eksempel engelsk (USA), engelsk (Storbritannia) eller engelsk (Sør-Afrika).

   Hvis du vil endre språket, velger du **Innstillinger**-ikonet øverst til venstre ![Innstillinger](media/ui-experience/settings_icon_small.png "Innstillinger-ikon for rollesenter") > **Mine innstillinger** > **Språk**. Hvis du vil ha mer informasjon, kan du gå til [Endre grunnleggende innstillinger](ui-change-basic-settings.md#language).
- Se gjennom [vanlige spørsmål for Copilot](ai-faq.md) for å finne ut mer om tekstforslag generert av kunstig intelligens fra Copilot og hvordan du bruker dem.

### <a name="create-first-draft-with-copilot"></a>Opprett første utkast med Copilot

1. Åpne varen du vil endre, i Business Central. Gjør følgende for å åpne en vare:

   1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen 22.](media/ui-search/search_small.png "Fortell hva du vil gjøre") øverst til høyre og angi **Varer**, og velg deretter relatert kobling for å vise en liste over tilgjengelige varer.
   2. Hvis du vil åpne varen, dobbeltklikker du på den eller velger verdien i kolonnen **Nr.** .

   Hvis du vil ha mer informasjon om hvordan du oppretter varer, kan du gå til [Registrer nye varer](inventory-how-register-new-items.md).

   [![Viser et varekort med ruten Markedsføringstekst](media/create-with-copilot.png)](media/create-with-copilot.png#lightbox)

2. Fra varekortet kan du komme i gang med å skrive markedsføringstekst med Copilot på to måter:

   - Bruk ruten **Markedsføringstekst** i faktaboksen til høyre på siden. Følg denne fremgangsmåten:

     1. Velg **Opprett med Copilot** i ruten **Markedsføringstekst**.

        Den foreslåtte teksten vises i ruten.
     2. Hvis du vil ha et annet forslag, velger du **Opprett med Copilot** på nytt. Hvis du ikke liker et forslag, velger du **Lukk** for å tømme ruten.

        Du kan gjøre dette trinnet flere ganger til du får et forslag som er et godt utgangspunkt. Husk at det nåværende forslaget overskrives, og at du ikke får det tilbake. Hvis du liker det nåværende forslaget, går du til neste trinn. Du vil fortsatt ha mulighet til å hente flere forslag senere, og til og med forbedre forslagene hvis du vil.
      3. Velg **Se gjennom og lagre forslaget** eller **Rediger** for å se gjennom, redigere og lagre teksten.

         Dette trinnet tar deg til siden **Opprett med Copilot**. Gå til neste del.

         > [!NOTE]
         > Teksten lagres ikke før du gjør dette trinnet.

   - Velg handlingen **Markedsføringstekst** øverst på varekortsiden for å gå direkte til siden **Opprett med Copilot**.

     Fra siden **Opprett med Copilot** velger du **Opprett med Copilot** for å få det første forslaget. Deretter kan du få flere forslag, forsøke å forbedre forslagene du får, redigere tekst med mer. Gå til [Se gjennom, rediger og lagre](#review-edit-and-save-text) for mer informasjon.

   > [!TIP]
   > [Hvor kommer forslagene fra?](ai-faq.md#how-does-copilot-work-where-does-the-suggested-text-come-from)

### <a name="review-edit-and-save-text"></a>Se gjennom, rediger og lagre teksten

Når du har det første utkastet, må du se gjennom det og gjøre endringer i teksten for å få den klar til publisering. Dette gjøres fra siden **Opprett med Copilot**. Nåværende tekst vises i boksen **Markedsføringstekst**. På siden kan du få flere forslag, endre innstillingene til å påvirke forslagene og manuelt gjøre endringer og legge på stil i teksten.

[![Viser vinduene Opprett med Copilot](media/create-with-copilot-window.png)](media/create-with-copilot-window.png#lightbox)

> [!IMPORTANT]
> Teksten genererte med kunstig intelligens fra Copilot er bare et forslag og kan ha feil. Den krever menneskelig overstyring og gjennomgang for å sikre at den er nøyaktig og passende Se gjennom eventuell foreslått tekst, og rediger etter behov før du lagrer og publiserer den til offentlig bruk.

Bruk følgende retningslinjer for å fullføre og lagre markedsføringsteksten.

1. Gjør endringer i teksten direkte i boksen **Markedsføringstekst**. Bruk verktøylinjen langs bunnen av boksen til å formatere tekst, legge til koblinger med mer.
2. Hvis du vil ha et nytt forslag, velger du **Opprett utkast**.
3. Hvis du ikke er fornøyd med forslagene, kan du forbedre tekstforslagene basert på innstillingene.

   Velg **Flere innstillinger**, endre alternativene som vises under **Velg hvordan Copilot oppretter forslag**, og velg deretter **Opprett kladd** for å få et nytt forslag.

   For å få veiledning om hvordan du kan forbedre forslagene, kan du gå til [Forbedre og skreddersy tekstforslag](#improve-and-tailor-text-suggestions).

4. Hvis du vil gå tilbake til forrige forslag, velger du **Angre**.
5. Se nøye gjennom teksten for nøyaktighet og relevant, og velg deretter **OK** for å lagre den.

### <a name="improve-and-tailor-text-suggestions"></a>Forbedre og skreddersy tekstforslag

Det finnes et par trinn du kan gjøre for å forbedre tekstforslagene og endre dem slik at de passer til personlige innstillinger eller firmainnstillinger.

1. Bruk alternativene øverst på siden **Opprett med Copilot** til å påvirke utfallet av teksten generert av kunstig intelligens: 

   |Alternativ|Beskrivelse|
   |-|-|
   |Attributter som skal inkluderes|Bruk dette alternativet til å basere forslaget delvis, på attributtene som er tildelt til varen. Velg attributtene som er best samkjørt med egenskapene du vil promotere. Jo mer relevante attributtene du inkluderer er, jo mer omfattende blir resultatet. Hvis du mener at du mangler noen viktige attributter, legger du til flere. Hvis du vil ha mer informasjon om attributter, kan du gå til [Arbeid med vareattributter](inventory-how-work-item-attributes.md) |
   |Fremhev en kvalitet|Bruk dette alternativet til å velge fra en liste over forhåndsdefinerte kvaliteter som du vil fremheve i teksten. Velg en kvalitet som best samkjøres med typen vare du skriver om. Egenskapene samsvarer ikke direkte med varens attributter, beskrivelse eller kategori. **Kvalitet** kan for eksempel være et godt valg for både en sykkel eller et skrivebord, mens **Hastighet** passer til en sykkel, men ikke et skrivebord.|
   |Ordlyd|Bruk dette alternativet til å påvirke hva slags ord, fraser og tegnsetting som brukes til å engasjere målgruppen. Du kan velge blant flere forhåndsdefinerte ordlyder, fra **Formell** (som gir en forretningsmessig ordlyd) til **Kreativ** (som resulterer i en uformell ordlyd). |
   |Format og lengde|Bruk dette alternativet til å styre den generelle strukturen for teksten, som består av tre deler, dekket av fire ulike alternativer: <ul><li>**Slagord** – et uttrykk eller en kort setning som identifiserer varen eller merket.</li><li>**Avsnitt** – ett enkelt avsnitt med flytende og detaljert tekst, som består av flere fullstendige setninger.</li><li>**Slagord + avsnitt** – et slagord etterfulgt av et avsnitt</li><li>**Kort** – en innledende setning, som ligner på en beskrivelse, etterfulgt av en punktliste med viktige nøkkelpunkter.</li></ul> |

2. Forbedre **Beskrivelse**-feltet på varekortet.

   Teksten i **Beskrivelse**-feltet blir brukt som den er mange steder i den foreslåtte teksten, så det er viktig at beskrivelsen best viser hvordan du vil at det skal henvises til varen i markedsføringsteksten. 

3. Kontroller at feltet **Varekategorikode** på varekortet er satt til en riktig kategori.

   Copilot vil finne ord og uttrykk som er knyttet til kategorien, og arbeide dem i den foreslåtte teksten.

## <a name="create-text-from-scratch"></a>Opprett markedsføringstekst fra grunnen av

1. I Business Central åpner du varen du vil endre, slik:

    1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen 22.](media/ui-search/search_small.png "Fortell hva du vil gjøre") øverst til høyre og angi **Varer**, og velg deretter relatert kobling for å vise en liste over tilgjengelige varer.
    2. Hvis du vil åpne varen, dobbeltklikker du på den eller velger nummeret i **Nr.** .

2. Gjør ett av følgende:

   - Velg **Rediger** i ruten **Markedsføringstekst** i faktaboksen til høyre på siden.
   - Velg handlingen **Markedsføringstekst**.
3. Gjør endringer i teksten direkte i boksen **Markedsføringstekst**. Bruk verktøylinjen langs bunnen av boksen til å formatere tekst, legge til koblinger med mer.
4. Velg **OK** når du er ferdig for å lagre teksten.

## <a name="see-also"></a>Se også

[Oversikt over varemarkedsføringstekst drevet av kunstig intelligens med Copilot](ai-overview.md)  
[Konfigurer varemarkedsføringstekst drevet av kunstig intelligens med Copilot](enable-ai.md)  
[Vanlige spørsmål om varemarkedsføringstekst drevet av kunstig intelligens med Copilot](ai-faq.md)  
[Registrere nye varer](inventory-how-register-new-items.md)  
