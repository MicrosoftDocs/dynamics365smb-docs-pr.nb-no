---
title: Opprett arbeidsflyter for å koble til oppgaver
description: Du kan opprette arbeidsflyter som kobler forretningsprosessoppgaver som utføres av forskjellige brukere, og som omfatter systemoppgaver, for eksempel automatisk bokføring, som arbeidsflyttrinn.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/30/2021
ms.author: edupont
ms.openlocfilehash: b4f6894c0d9c5a23445f70b2a50fcd677b17be66
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/08/2021
ms.locfileid: "6438410"
---
# <a name="create-workflows-to-connect-business-process-tasks"></a>Opprett arbeidsflyter for å koble til forretningsprosessoppgaver

Du kan opprette arbeidsflyter som kobler forretningsprosessoppgaver som utføres av forskjellige brukere. Systemoppgaver, for eksempel automatisk bokføring, kan tas med som trinn i arbeidsflyter, før eller etterfulgt av brukeroppgaver. Å be om og gi godkjenning til å opprette nye oppføringer er typiske arbeidsflyttrinn.  

På **Arbeidsflyt**-siden oppretter du en arbeidsflyt ved å føre opp de involverte trinnene på linjene. Hvert trinn består av en arbeidsflythendelse endret av hendelsesbetingelsene og et arbeidsflytsvar med svaralternativer. Du definerer arbeidsflyttrinn ved å fylle ut felt på arbeidsflytlinjer fra faste lister over verdier for hendelse og svar som representerer scenarier som støttes av programkoden.  

Når du oppretter arbeidsflyter, kan du kopiere trinnene fra eksisterende arbeidsflyter eller arbeidsflytmaler. Arbeidsflytmaler representerer ikke-redigerbare arbeidsflyter som finnes i den generelle versjonen av [!INCLUDE[prod_short](includes/prod_short.md)]. Koden for arbeidsflytmaler som er lagt inn av Microsoft, har prefikset "MS-", som i "MS PIW". Hvis du vil ha mer informasjon, kan du se [Opprette arbeidsflyter fra arbeidsflytmaler](across-how-to-create-workflows-from-workflow-templates.md).  

Hvis forretningsscenarioet krever arbeidsflythendelser eller svar som ikke støttes, må en Microsoft-partner implementere dem ved å opprette en utvidelse som implementerer den relevante arbeidsflythendelsen.  

> [!NOTE]  
> Alle varsler om arbeidsflyttrinn sendes via en jobbkø. Kontroller at jobbkøen gjenspeiler dine forretningsbehov. Hvis du vil ha mer informasjon, kan du se [Bruke jobbkøer til å planlegge oppgaver](admin-job-queues-schedule-tasks.md).  

:::image type="content" source="media/Workflows/workflow-example.png" alt-text="Bilde av eksempel på en arbeidsflyt.":::

Arbeidsflyten er delt inn i tre deler:

1) **Når hendelse** Det er der utløseren velges.
    Eksempler på utløser kan være:
    - En hoveddataoppføring endres
    - En kladdelinje opprettes
    - et innkommende dokument opprettes eller frigis
    - Det er bedt om godkjenning av et dokument

2) **Under forutsetning av** **Betingelsene** er knyttet til hendelsen og åpnes for å opprette filtre når hendelsen utløses
3) **Så svar** **Svarene** svarer på hva det neste trinnet i arbeidet er.

For begge hendelsestypene er hendelsene system definert. Nye hendelser må legges til gjennom utviklingen av en utvidelse.

## <a name="to-create-a-workflow"></a>Slik oppretter du en arbeidsflyt:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Arbeidsflyter**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**. Siden **Arbeidsflyt** åpnes.  
3. I **Kode**-feltet angir du maksimalt 20 tegn for å identifisere arbeidsflyten.  
4. For å opprette en arbeidsflyt fra en arbeidsflytmal, velg **Opprett arbeidsflyt fra mal** på **Arbeidsflyter**-siden. Hvis du vil ha mer informasjon, kan du se [Opprette arbeidsflyter fra arbeidsflytmaler](across-how-to-create-workflows-from-workflow-templates.md).  
5. I **Beskrivelse**-feltet beskriver du arbeidsflyten.  
6. I feltet **Kategori**, angi hvilken kategori arbeidsflyten tilhører.  
7. I **Når hendelse**-feltet angir du hendelsen som må inntreffe for å starte arbeidsflyttrinnet.  

    Når du velger feltet, åpnes siden **Arbeidsflythendelser**, der du kan velge fra alle arbeidsflythendelser som finnes.  
8. I feltet **Betingelse** angir du én eller flere betingelser som må oppfylles før hendelsen i feltet **Når hendelse** kan forekomme.  

    Når du velger feltet, åpnes siden **Hendelsesbetingelser** der du velger fra en liste over filterfelt som er aktuelle som betingelser for den aktuelle hendelsen. Du kan legge til nye filterfelt som du vil bruke som vilkår for hendelsen. Du kan angi filtre for hendelsesbetingelse på samme måte som du angir filtre på rapportforespørselssider.  

    Hvis arbeidsflythendelsen er en endring av et bestemt felt i en post, åpnes **Hendelsesvilkår**-siden med alternativer for å velge feltet og typen endring.  

    1. For å angi en feltendring for hendelsen, velger du feltet som endres på **Hendelsesvilkår**-siden i **Felt**-feltet.  
    2. I **Operator**-feltet velger du enten **Redusert**, **Økt** eller **Endret**.  
9. I feltet **Så svar** angir du svaret som skal følge når arbeidsflythendelsen inntreffer.  

     Når du velger feltet, åpnes siden **Arbeidsflytsvar**, der du kan velge fra alle arbeidsflytsvar som finnes, og angi svaralternativer for det valgte svaret.  
10. På hurtigfanen **Alternativer for det valgte svaret** angir du alternativer for arbeidsflytsvaret ved å velge verdier i ulike felt som vises, på følgende måte:  

    1. Hvis du vil angi alternativer for et arbeidsflytsvar som involverer sending av en melding, fyller du ut feltene som beskrevet i følgende tabell.  

        |Felt|Beskrivelse|  
        |-----|-----------|  
        |**Varsle avsender**|Angi om godkjenningsanmoderen skal varsles i stedet for mottakeren av godkjenningsforespørselen. Hvis du setter en hake i avmerkingsboksen, deaktiveres feltet **Bruker-ID for mottaker**, fordi godkjenningsanmoderen, avsenderen, blir varslet i stedet. Navnet på arbeidsflytsvarendringene endres i henhold til dette til **Opprett varsel for &lt;avsender&gt;**. Hvis det ikke er merket av i avmerkingsboksen, er navnet på arbeidsflytsvaret **Opprett varsel for &lt;Bruker&gt;**.
        |**Bruker-ID for mottaker**|Angi brukeren som meldingen må sendes til. **Obs!** Dette alternativet er bare tilgjengelig for arbeidsflytsvar med en plassholder for en bestemt bruker. For arbeidsflytsvar uten plassholdere for brukere er varslingsmottakeren vanligvis definert av brukeroppsettet for godkjenning.|  
        |**Posttype for varsling**|Angir om arbeidsflytvarslingen utløses av en postendring, en godkjenningsforespørsel eller en forfalt data.|
        |**Kobling til målside**|Angi en annen side som koblingen i meldingen åpner i stedet for standardsiden. Merk at siden må ha samme kildetabell som den aktuelle posten.|
        |**Egendefinert kobling**|Angi URL-adressen til en kobling som legges til i meldingen i tillegg til koblingen til en side.|  

    2. Hvis du vil angi alternativer for et arbeidsflytsvar som involverer oppretting av en godkjenningsforespørsel, fyller du ut feltene som beskrevet i følgende tabell.  

        |Felt|Beskrivelse|  
        |-----|-----------|  
        |**Forfallsdatoformel**|Angi hvor mange dager som gjenstår før godkjenningsforespørselen må løses fra datoen da den ble sendt.|
        |**Deleger etter**|Angi om og når en forespørsel om godkjenning skal delegeres automatisk til relevant stedfortreder. Du kan velge å automatisk delegere en, to, eller fem dager etter datoen da godkjenningen ble forespurt.|
        |**Godkjennertype**|Angi hvem godkjenneren er, i henhold til oppsettet for godkjenningsbrukere og arbeidsflytbrukere. Når feltet er angitt til **Selger/innkjøper** angir innstillingen at brukeren som er definert i feltet **Selger/innkjøper - kode** på siden **Brukeroppsett for godkjenning**, bestemmer godkjenneren. Godkjenningsforespørselsposter blir deretter opprettet i henhold til verdien i feltet **Godkjennergrensetype**. Hvis du vil ha mer informasjon, kan du se [Konfigurere godkjenningsbrukere](across-how-to-set-up-workflow-users.md).|
        |**Vis bekreftelsesmelding**|Angi om en bekreftelsesmelding skal vises til brukere når de ber godkjenning.|
        |**Godkjennergrensetype**|Angi hvordan godkjenneres godkjenningsgrenser påvirker når godkjenningsforespørselsposter opprettes for dem. En kvalifisert godkjenner er en godkjenner med en godkjenningsgrense som er høyere enn verdien på forespørselen. Du har følgende alternativer: <ol><li>**Godkjennerkjede** angir at godkjenningsforespørselsposter er opprettet for alle bestillerens godkjennere opptil og inkludert den første kvalifiserte godkjenneren</li><li>**Direkte godkjenner** angir at en godkjenningsforespørselspost bare opprettes for anmoderens umiddelbare godkjenner, uavhengig av godkjennerens godkjenningsgrense</li><li>**Første kvalifiserte godkjenner** angir at en godkjenningsforespørselspost bare opprettes for anmoderens første kvalifiserte godkjenner.</li></ol>|
    3. Hvis du vil angi alternativer for et arbeidsflytsvar som involverer oppretting av kladdelinjer, fyller du ut feltene som beskrevet i følgende tabell.  

        |Felt|Beskrivelse|  
        |-----|-----------|  
        |**Finanskladdemalnavn**|Angi navnet på finanskladdemalen som de angitte kladdelinjene er opprettet i.|  
        |**Finanskladdenavn**|Angi navnet på finanskladden som de angitte kladdelinjene er opprettet i.|  

11. Velg knappene **Øk innrykk** og **Reduser innrykk** for å rykke inn hendelsesnavnet i **Når**-feltet for å definere plasseringen av trinnet i arbeidsflyten.  

    1. Angi at trinnet er det neste i arbeidsflytrekkefølgen ved å rykke inn hendelsesnavnet under hendelsesnavnet i det forrige trinnet.  
    2. Angi at trinnet er ett av flere alternative trinn som kan starte avhengig av tilstanden, ved å plassere hendelsesnavnet ved samme innrykk som de andre alternative trinnene. Ordne slike valgfrie trinn etter prioritet ved å plassere det viktigste trinnet først.  

    > [!NOTE]  
    >  Du kan bare endre innrykket for et trinn som ikke har et senere trinn.  

12. Gjenta trinn 7 til 11 for å legge til flere arbeidsflyttrinn, enten før eller etter trinnet du nettopp opprettet.  
13. Merk av for **Aktivert** for å angi at arbeidsflyten starter så snart hendelsen på det første trinnet av typen **Innpunkt** inntreffer. Hvis du vil ha mer informasjon, kan du se [Bruke arbeidsflyter](across-use-workflows.md).  

> [!NOTE]  
> Ikke aktiver en arbeidsflyt før du er sikker på at arbeidsflyten er fullført og at de involverte arbeidsflyttrinnene kan starte.  

> [!TIP]  
> Hvis du vil vise relasjoner mellom tabeller som brukes i arbeidsflyter, velger du ikonet ![lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir deretter **Arbeidsflyt – tabellrelasjoner**.  

## <a name="example-of-creating-a-new-workflow-using-existing-events"></a>Eksempel på oppretting av ny arbeidsflyt ved bruk av eksisterende hendelser

I eksemplet nedenfor lages det en ny arbeidsflyt for å godkjenne endringer i navnet på en eksisterende leverandør:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Arbeidsflyter**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**. Siden **Arbeidsflyt** åpnes.
3. I arbeidsflytdelen fyller du ut feltene som beskrevet i tabellen nedenfor.

    |Felt  |Verdi  |
    |---------|---------|
    |**Kode**|**VENDAPN-01**|
    |**Beskrivelse**|**Godkjenning av leverandørnavnendring** |
    |**Kategori**|**INNKJØP**|

4. Følg denne fremgangsmåten for å opprette det første trinnet i arbeidsflyten.

    1. I feltet **Når hendelse** angir du *En leverandørpost endres*.  
    2. I feltet **Under forutsetning av** velger du ordet **Alltid**, og deretter på siden **Hendelsesbetingelse** velger du koblingen **Legg til en betingelse for når en feltverdi endres**, og deretter velger du feltet *Navn*.  

      Resultatet av dette trinnet er at betingelsen leser som *Navn endres*.  
    3. I feltet **Så svar** velger du koblingen **Velg svar** , og deretter på siden **Arbeidsflytsvar**, i feltet **Velg svar** velger du svaret *Tilbakestill verdien for feltet <Field> på posten og lagre endringen*. Deretter i delen **Alternativer for valgt svar** angi du feltet *Navn*.  
    4. Velg koblingen **Legg til flere svar**, og legg deretter til en oppføring for *Opprett en godkjenningsforespørsel for posten med godkjenningstype <%1> og <%2>.* svar  
    5. I delen **Alternativer for det valgte svaret** for det nye svaret endrer du feltet **Godkjennertype** til *Arbeidsflytbrukergruppe*, og deretter angir du den aktuelle brukergruppen i feltet **Arbeidsflytbrukergruppe**.  

    Hvis du vil ha mer informasjon, kan du se [Konfigurere godkjenningsbrukere](across-how-to-set-up-approval-users.md).  
    6. Legg til et tredje svar, *Send godkjenningsforespørsler for posten, og opprett et varsel.*  
    7. Legg til et fjerde svar, *Vis melding %1*, og angi deretter **En godkjenningsforespørsel er sendt** i Melding-feltet under **Alternativer for det valgte svaret**.  
    8. Velg OK-knappen for å gå tilbake til arbeidsflyttrinnet.  

5. I den neste linjen legger du til et nytt arbeidsflyttrinn for hendelsen *En godkjenningsforespørsel er godkjent.* .  

    1. Angi **En godkjenningsforespørsel er godkjent** i feltet *Når hendelse*.  
    2. Velg linjemenyen, og velg deretter **Øk innrykk**.  
    3. I **Ved forutsetning av**-feltet velger du ordet **Alltid**, og angir *0* i feltet **Venter på godkjenning**.  

      Resultatet av dette trinnet er at betingelsen leses som *Venter på godkjenning:0* for å angi at dette er den siste godkjenneren.  
    4. I feltet **Så svar** velger du **Velg svar**-koblingen, og deretter velger du svaret **Send godkjenningsforespørsel for posten og opprett et varsel** på siden **Arbeidsflytsvar** i feltet *Velg svar*.  
    5. Velg OK-knappen.  
6. I den neste linjen legger du til enda et arbeidsflyttrinn for hendelsen *En godkjenningsforespørsel er godkjent*.  

    1. Angi **En godkjenningsforespørsel er godkjent** i feltet *Når hendelse*.
    2. I **Ved forutsetning av**-feltet velger du ordet **Alltid**, og angir du *>0* i feltet **Venter på godkjenning**.  

      Resultatet av dette trinnet er at betingelsen leses som *Venter på godkjenning:>0* for å angi at dette *ikke* er den siste godkjenneren.  
    3. I feltet **Så svar** velger du **Velg svar**-koblingen, og deretter velger du svaret **Send godkjenningsforespørsel for posten og opprett et varsel** på siden **Arbeidsflytsvar** i feltet *Velg svar*.  
    4. Velg OK-knappen.  
7. I den neste linjen legger du til et arbeidsflyttrinn for hendelsen *En godkjenningsforespørsel er avvist*.  

    1. Angi **En godkjenningsforespørsel er avvist** i feltet *Når hendelse*.  
    2. I **Ved forutsetning av**-feltet lar du verdien være *Alltid*.  
    3. I feltet **Så svar** velger du **Velg svar**-koblingen, og deretter velger du svaret **Forkast de nye verdiene** på siden **Arbeidsflytsvar** i feltet *Velg svar*.  
    4. Velg koblingen **Legg til flere svar**, og legg deretter til en oppføring for svaret *Avvis godkjenningsforespørselen for posten og opprett et varsel*.
    5. Velg OK-knappen.  
8. I den neste linjen legger du til enda et arbeidsflyttrinn for hendelsen *En godkjenningsforespørsel er avvist*.  

    1. Angi **En godkjenningsforespørsel er avvist** i feltet *Når hendelse*.  
    2. I **Ved forutsetning av**-feltet lar du verdien være *Alltid*.  
    3. I feltet **Så svar** velger du **Velg svar**-koblingen, og deretter velger du svaret **Send godkjenningsforespørsel for posten og opprett et varsel** på siden **Arbeidsflytsvar** i feltet *Velg svar*.  
    4. Velg OK-knappen.  
9. Du aktiverer arbeidsflyten ved å velge **Aktivert**-feltet.  

Illustrasjonen nedenfor gir en oversikt over resultatet av denne prosedyren.  

:::image type="content" source="media/Workflows/workflow-example-2.png" alt-text="Bilde av godkjenningsarbeidsflyten for leverandørnavn.":::

Nå må du teste arbeidsflyten ved å åpne en eksisterende leverandør og endre navnet. Bekreft at det gjøres en godkjenningsforespørsel om å endre leverandørnavnet.

## <a name="see-also"></a>Se også

[Opprette arbeidsflyter fra arbeidsflytmaler](across-how-to-create-workflows-from-workflow-templates.md)  
[Konfigurere godkjenningsbrukere](across-how-to-set-up-approval-users.md)  
[Konfigurere arbeidsflytvarsler](across-setting-up-workflow-notifications.md)  
[Vise arkiverte forekomster av arbeidsflyttrinn](across-how-to-view-archived-workflow-step-instances.md)  
[Slette arbeidsflyter](across-how-to-delete-workflows.md)  
[Gjennomgang: Definere og bruke en arbeidsflyt for kjøpsgodkjenning](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Konfigurere arbeidsflyter](across-set-up-workflows.md)  
[Bruke arbeidsflyter](across-use-workflows.md)  
[Arbeidsflyt](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
