---
title: Opprett godkjenningsarbeidsflyter for å koble til oppgaver
description: Finn ut hvordan du oppretter arbeidsflytprosesser som kobler oppgaver som utføres av forskjellige personer i forretningsprosesser.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 04/24/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="create-workflows-to-connect-tasks-in-business-processes"></a>Opprett arbeidsflyter for å koble til oppgaver i forretningsprosesser

Du kan opprette arbeidsflyter som kobler til oppgaver i forretningsprosesser som utføres av forskjellige brukere. Du kan inkludere systemoppgaver, for eksempel automatisk bokføring, som trinn i arbeidsflyter som kommer før eller etter av brukeroppgaver. Å be om og gi godkjenning til å opprette nye oppføringer er typiske arbeidsflyttrinn.  

På **Arbeidsflyt**-siden oppretter du en arbeidsflyt ved å føre opp trinnene på linjene. Hvert trinn består av en utløser og et svar:

* En hendelse som angir betingelsene som skal starte arbeidsflyten.
* Et arbeidsflytsvar som definerer hva arbeidsflyten gjør.

[!INCLUDE[workflow](includes/workflow.md)]

Når du oppretter arbeidsflyter, kan du kopiere trinnene fra eksisterende arbeidsflyter eller arbeidsflytmaler. Arbeidsflytmaler er ikke-redigerbare arbeidsflyter [!INCLUDE[prod_short](includes/prod_short.md)] gir. Identifikatorene for arbeidsflytmaler har prefikset MS-, som i MS PIW. Finn ut mer under [Opprett arbeidsflyter fra arbeidsflytmaler](across-how-to-create-workflows-from-workflow-templates.md).  

> [!NOTE]  
> Alle varsler om arbeidsflyttrinn sendes via en jobbkø. Kontroller at jobbkøen gjenspeiler dine forretningsbehov. Finn ut mer under [Bruk jobbkøer til å planlegge oppgaver](admin-job-queues-schedule-tasks.md).  

:::image type="content" source="media/Workflows/workflow-example.png" alt-text="Bilde av eksempel på en arbeidsflyt.":::

En arbeidsflyt er delt inn i tre deler:

1. **Når hendelse**  
   Det er der utløseren velges.  
   Eksempler på en utløser:
   * En hoveddataoppføring endres
   * En kladdelinje opprettes
   * Et innkommende dokument opprettes eller frigis
   * Det er bedt om godkjenning av et dokument
2. **Ved betingelse**  
   **Betingelsene** er knyttet til hendelsen og tillater at det opprettes filtre for å bestemme hvordan arbeidsflyten fortsetter.
3. **Så svar**  
   **Svarene** angir de neste trinnene i arbeidsflyten.

Alternativene for hendelser og svar er systemdefinert. Hvis du vil legge til nye alternativer, må du utarbeide en utvidelse.

## <a name="to-create-a-workflow"></a>Slik oppretter du en arbeidsflyt:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Arbeidsflyter**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**. Siden **Arbeidsflyt** åpnes.  
3. I **Kode**-feltet angir du maksimalt 20 tegn for å identifisere arbeidsflyten.  
4. For å opprette en arbeidsflyt fra en arbeidsflytmal, velg **Ny arbeidsflyt fra mal** på **Arbeidsflyter**-siden. Finn ut mer under [Opprett arbeidsflyter fra arbeidsflytmaler](across-how-to-create-workflows-from-workflow-templates.md).  
5. I **Beskrivelse**-feltet beskriver du arbeidsflyten.  
6. I feltet **Kategori**, angi hvilken kategori arbeidsflyten tilhører.  
7. I **Når hendelse**-feltet angir du hendelsen som må inntreffe for å starte arbeidsflyttrinnet.  

   Når du velger feltet, viser siden **Arbeidsflythendelser** alle tilgjengelige arbeidsflythendelser.  
8. I feltet **Ved forutsetning av** angir du én eller flere betingelser som må oppfylles før hendelsen i feltet **Når hendelse** kan forekomme.  

   Når du velger feltet **Hendelsesbetingelser**, kan listefilterfelter være betingelser for hendelsen. Du kan legge til nye filterfelter hvis du vil.  

   Hvis arbeidsflythendelsen er en endring av et bestemt felt i en post, bruker du **Hendelsesvilkår**-siden for å velge feltet og typen endring.  

   1. For å angi en feltendring for hendelsen, velger du feltet som endres på **Hendelsesvilkår**-siden i **Felt**-feltet.  
   2. I **Operator**-feltet velger du enten **Redusert**, **Økt** eller **Endret**.  
9. I feltet **Så svar** angir du svaret som skal følge når arbeidsflythendelsen inntreffer.  

   Når du velger feltet, viser siden **Arbeidsflytsvar** alle tilgjengelige arbeidsflytsvar og svaralternativer.  
10. På hurtigfanen **Alternativer for det valgte svaret** angir du alternativer for arbeidsflytsvaret ved å velge verdier i ulike felt som vises, på følgende måte:  

    1. Hvis du vil angi alternativer for et arbeidsflytsvar som involverer sending av en melding, fyller du ut feltene som beskrevet i følgende tabell.  

    > [!NOTE]
    > Disse feltene varierer avhengig av svaret du har valgt.

       |Felt|Description|
       |-----|-----------|
       |**Varsle avsender**|Angi om godkjenningsanmoderen skal varsles i stedet for mottakeren av godkjenningsforespørselen. Hvis du setter en hake i avmerkingsboksen, deaktiveres feltet **Bruker-ID for mottaker**, fordi godkjenningsanmoderen, avsenderen, blir varslet i stedet. Navnet på arbeidsflytsvarendringene endres i henhold til dette til **Opprett varsel for &lt;avsender&gt;**. Hvis det ikke er merket av i avmerkingsboksen, er navnet på arbeidsflytsvaret **Opprett varsel for &lt;Bruker&gt;**.|
       |**Bruker-ID for mottaker**|Angi brukeren meldingen må sendes til. **Obs!** Dette alternativet er bare tilgjengelig for arbeidsflytsvar med en plassholder for en bestemt bruker. For arbeidsflytsvar uten plassholdere for brukere er varslingsmottakeren vanligvis definert av **Brukeroppsett for godkjenning**.|
       |**Posttype for varsling**|Angi en utløser for arbeidsflytvarslingen. Utløseren kan være en post endring, en godkjenningsforespørsel eller en forfalt frist.|
       |**Kobling til målside**|Angi hvilken side koblingen i varselet åpner. Siden må ha samme kildetabell som den aktuelle posten.|
       |**Egendefinert kobling**|Angi nettadressen til en kobling inkludert i meldingen i tillegg til koblingen til siden.|

    2. Hvis du vil angi alternativer for et arbeidsflytsvar som involverer oppretting av en godkjenningsforespørsel, fyller du ut feltene som beskrevet i følgende tabell.  

       |Felt|Description|  
       |-----|-----------|  
       |**Forfallsdatoformel**|Angi antall dager godkjenneren har på seg til å løse forespørselen. Perioden starter når forespørselen sendes.|
       |**Deleger etter**|Angi om og når en forespørsel om godkjenning er delegert automatisk til stedfortrederen. Du kan velge å automatisk delegere en, to, eller fem dager etter datoen da godkjenningen ble forespurt.|
       |**Godkjennertype**|Angi hvem godkjenneren er, i henhold til oppsettet for godkjenningsbrukere og arbeidsflytbrukere. Når feltet er angitt til **Selger/innkjøper**, kan brukeren angitt i feltet **Selger/innkjøper – kode** på siden **Brukeroppsett for godkjenning**, bestemme godkjenneren. Godkjenningsforespørselsposter blir deretter opprettet i henhold til verdien i feltet **Godkjennergrensetype**. Finn ut mer under [Definer godkjenningsbrukere](across-how-to-set-up-workflow-users.md).|
       |**Vis bekreftelsesmelding**|Angi om det skal vises en bekreftelsesmelding etter at brukere ber om en godkjenning.|
       |**Godkjennergrensetype**|Angi effekten av grenser for godkjennere. En godkjenners godkjenningsgrense må være over verdien i forespørselen. Følgende alternativer finnes: <ol><li>**Godkjennerkjede** angir at godkjenningsforespørselsposter er opprettet for alle bestillerens godkjennere opptil og inkludert den første kvalifiserte godkjenneren</li><li>**Direkte godkjenner** angir at en godkjenningsforespørselspost bare opprettes for anmoderens umiddelbare godkjenner, uavhengig av godkjennerens godkjenningsgrense</li><li>**Første kvalifiserte godkjenner** angir at en godkjenningsforespørselspost bare opprettes for anmoderens første godkjenner.</li><li>**Bestemt godkjenner** angir at du varsler brukeren som er valgt i feltet **Godkjenner-ID**.</li></ol>|

    3. Hvis du vil angi alternativer for et arbeidsflytsvar som involverer oppretting av kladdelinjer, fyller du ut feltene som beskrevet i følgende tabell.  

       |Felt|Description|  
       |-----|-----------|  
       |**Finanskladdemalnavn**|Angi navnet på finanskladdemalen som de angitte kladdelinjene er opprettet i.|  
       |**Finanskladdenavn**|Angi navnet på finanskladden som de angitte kladdelinjene er opprettet i.|  

11. Velg knappene **Øk innrykk** og **Reduser innrykk** for å rykke inn hendelsesnavnet i **Når**-feltet for å definere plasseringen av trinnet i arbeidsflyten.  

    1. Rykk inn hendelsen under navnet på forrige trinn for å angi at det er neste trinn.  
    2. Angi at trinnet er et av flere alternative trinn som kan starte avhengig av tilstanden, ved å plassere hendelsesnavnet ved samme innrykk for å samsvare med de andre alternative trinnene. Ordne slike valgfrie trinn etter prioritet ved å plassere det viktigste trinnet først.  

    > [!NOTE]  
    >  Du kan bare endre innrykket for et trinn som ikke har et senere trinn.  

12. Gjenta trinn 7 til 11 for å legge til flere arbeidsflyttrinn, enten før eller etter trinnet du nettopp opprettet.  
13. Slå på vekslebryteren **Aktivert** for å angi at arbeidsflyten starter når hendelsen på det første trinnet av typen **Innpunkt** inntreffer. Finn ut mer under [Bruk arbeidsflyter](across-use-workflows.md).  

> [!NOTE]  
> Ikke aktiver en arbeidsflyt før du er sikker på at den er klar.  

> [!TIP]  
> Hvis du vil utforske relasjonen mellom tabellene som brukes i arbeidsflyter, velger du ikonet ![lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir deretter **Arbeidsflyt – tabellrelasjoner**.  

## <a name="example-of-creating-a-new-workflow-using-existing-events"></a>Eksempel på oppretting av ny arbeidsflyt ved bruk av eksisterende hendelser

I eksemplet nedenfor opprettes det en ny arbeidsflyt for å endre navnet på en leverandør:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Arbeidsflyter**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**. Siden **Arbeidsflyt** åpnes.
3. I arbeidsflytdelen fyller du ut feltene som beskrevet i tabellen nedenfor.

    |Felt  |Verdi  |
    |---------|---------|
    |**Kode**|**VENDAPN-01**|
    |**Beskrivelse**|**Godkjenning av leverandørnavnendring** |
    |**Kategori**|**INNKJØP**|

4. Gjør følgende for å opprette det første trinnet i arbeidsflyten.

    1. I feltet **Når hendelse** angir du *En leverandørpost endres*.  
    2. I **Ved forutsetning av**-feltet velger du ordet **Alltid**. Deretter på siden **Hendelsesbetingelse** velger du koblingen **Legg til en betingelse for når en feltverdi endres**, og deretter velger du feltet **Navn**. Resultatet av dette trinnet er at betingelsen leser som *Navn endres*.  
    3. I feltet **Så svar** velger du koblingen **Velg svar**. På siden **Arbeidsflytsvar**, i feltet **Velg svar**, velger du svaret **Tilbakestill verdien for fetlet \<Field\> på posten og lagre endringen**. Deretter angir du **Navn**-feltet i delen **Alternativer for valgt svar**.  
    4. Velg koblingen **Legg til flere svar**, og legg deretter til en oppføring for svaret **Opprett en godkjenningsforespørsel for posten med godkjenningstype <%1> og <%2>**.  
    5. I delen **Alternativer for det valgte svaret** for det nye svaret endrer du feltet **Godkjenningstype** til **Arbeidsflytbrukergruppe**. I feltet **Arbeidsflytbrukergruppe** angir du brukergruppen. Finn ut mer under [Definer godkjenningsbrukere](across-how-to-set-up-approval-users.md).  
    6. Legg til et tredje svar, **Send godkjenningsforespørsler for posten, og opprett et varsel**.  
    7. Legg til et fjerde svar, **Vis melding %1**. Angi deretter **En godkjenningsforespørsel er sendt** i **Melding**-feltet under **Alternativer for det valgte svaret**.  
    8. Velg **OK** for å gå tilbake til arbeidsflyttrinnet.  

5. I den neste linjen legger du til et nytt arbeidsflyttrinn for hendelsen **En godkjenningsforespørsel er godkjent**.

    1. Angi **En godkjenningsforespørsel er godkjent** i feltet **Når hendelse**.  
    2. Velg linjemenyen, og velg deretter **Øk innrykk**.  
    3. I **Ved forutsetning av**-feltet velger du **Alltid**. Angi **0** i feltet **Ventende godkjenninger**. Betingelsen leses som **Venter på godkjenning:0** for å angi at forespørselen ikke krever flere godkjennere.  
    4. I feltet **Så svar** velger du koblingen **Velg svar**. Deretter velger du svaret **Send godkjenningsforespørsel for posten og opprett et varsel** på siden **Arbeidsflytsvar** i feltet **Velg svar**.  
    5. Velg **OK**.  
6. I den neste linjen legger du til enda et arbeidsflyttrinn for hendelsen **En godkjenningsforespørsel er godkjent**.  

    1. Angi **En godkjenningsforespørsel er godkjent** i feltet **Når hendelse**.
    2. I **Ved forutsetning av**-feltet velger du **Alltid**. Angi **>0** i feltet **Ventende godkjenninger**. Betingelsen leses som **Venter på godkjenning:>0** for å angi at dette ikke er den siste godkjenneren.  
    3. I feltet **Så svar** velger du koblingen **Velg svar**. Deretter velger du svaret **Send godkjenningsforespørsel for posten og opprett et varsel** på siden **Arbeidsflytsvar** i feltet **Velg svar**.  
    4. Velg **OK**.  
7. I den neste linjen legger du til et arbeidsflyttrinn for hendelsen **En godkjenningsforespørsel er delegert**.  

    1. Angi **En godkjenningsforespørsel er delegert** i feltet **Når hendelse**.  
    2. I **Ved forutsetning av**-feltet lar du verdien være **Alltid**.  
    3. I feltet **Så svar** velger du koblingen **Velg svar**. Deretter velger du svaret **Send godkjenningsforespørsel for posten og opprett et varsel** på siden **Arbeidsflytsvar** i feltet **Velg svar**.  
    4. Velg **OK**.  
8. I den neste linjen legger du til enda et arbeidsflyttrinn for hendelsen **En godkjenningsforespørsel er avvist**.  

    1. Angi **En godkjenningsforespørsel er avvist** i feltet **Når hendelse**.  
    2. I **Ved forutsetning av**-feltet lar du verdien være **Alltid**.  
    3. I feltet **Så svar** velger du koblingen **Velg svar**. På siden **Arbeidsflytsvar** i **Velg svar**-feltet velger du svaret **Forkast de nye verdiene**.  
    4. Velg koblingen **Legg til flere svar**, og legg deretter til en oppføring for svaret **Avvis godkjenningsforespørselen for posten og opprett et varsel**
    5. Velg **OK**.  
9. For å aktivere arbeidsflyten må du slå på vekslebryteren **Aktivert**.  

Illustrasjonen nedenfor gir en oversikt over resultatet av denne prosedyren.  

:::image type="content" source="media/Workflows/workflow-example-2.png" alt-text="Bilde av godkjenningsarbeidsflyten for leverandørnavn.":::

Nå tester du arbeidsflyten ved å åpne en eksisterende leverandørkort og endre navnet. Bekreft at det sendes en godkjenningsforespørsel om å endre leverandørnavnet.

## <a name="see-also"></a>Se også

[Opprett arbeidsflyter fra arbeidsflytmaler](across-how-to-create-workflows-from-workflow-templates.md)  
[Konfigurer godkjenningsbrukere](across-how-to-set-up-approval-users.md)  
[Konfigurering av godkjenningsarbeidsflytvarsler](across-setting-up-workflow-notifications.md)  
[Vis arkiverte forekomster av arbeidsflyttrinn](across-how-to-view-archived-workflow-step-instances.md)  
[Slett godkjenningsarbeidsflyter](across-how-to-delete-workflows.md)  
[Gjennomgang: Definer og bruk en arbeidsflyt for kjøpsgodkjenning](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Konfigurer godkjenningsarbeidsflyter](across-set-up-workflows.md)  
[Bruk godkjenningsarbeidsflyter](across-use-workflows.md)  
[Arbeidsflyt](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
