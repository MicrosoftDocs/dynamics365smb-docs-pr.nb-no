---
title: Bruk en Power Automate-flyt for varsler om enhetsendringer
description: Lær hvordan du kan opprette en flyt i Power Automate slik at du blir varslet når en enhet endres i Dataverse-miljø.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Power Automate, Flow, Dataverse'
ms.search.form: null
ms.date: 09/05/2022
ms.author: bholtorf
---
# <a name="use-a-power-automate-flow-for-alerts-to-dataverse-entity-changes"></a>Bruk en Power Automate-flyt for varsler om Dataverse-enhetsendringer

Administratorer kan opprette en automatisk flyt i Power Automate som varsler [!INCLUDE[prod_short](includes/prod_short.md)] om endringer i poster i [!INCLUDE [cds_long_md](includes/cds_long_md.md)]-organisasjonen.

> [!NOTE]
> Denne artikkelen tar utgangspunkt i den nettbaserte versjonen av [!INCLUDE[prod_short](includes/prod_short.md)] med [!INCLUDE [cds_long_md](includes/cds_long_md.md)] og tidsstyrt synkronisering mellom de to appene.

## <a name="import-the-flow-template"></a>Importer flytmalen

> [!TIP]
> For å gjøre det enklere å definere flyten har vi opprettet en mal som definerer flytutløseren og flytbetingelsen for deg. Følg fremgangsmåten i denne delen for å bruke malen. Du kan opprette flyten selv ved å hoppe over denne delen og starte med trinnene i [Definer flytutløseren](#define-the-flow-trigger).

1. Logg på [Power Automate](https://powerautomate.microsoft.com).
2. Velg **Maler** og søk etter **Varsle Business Central**.

:::image type="content" source="media/power-automate-import-template.png" alt-text="Nøkkelord for å finne flytmalen.":::
3. Velg malen **Varsle Business Central når en konto endres**.
4. Fortsett med trinnene i delen [Varsel Business Central om en endring](#notify-business-central-about-a-change).

## <a name="define-the-flow-trigger"></a>Definer flytutløseren

1. Logg deg på [Power Automate](https://flow.microsoft.com).
2. Opprett en automatisk skyflyt som starter når en rad for en [!INCLUDE [cds_long_md](includes/cds_long_md.md)]-enhet legges til, endres eller slettes. Hvis du vil ha mer informasjon, kan du se [Utløs flyter når en rad legges til, endres eller slettes](/power-automate/dataverse/create-update-delete-trigger). I dette eksemplet brukes enheten **Kontoer**. Bildet nedenfor viser innstillingene for det første trinnet ved å definere en flytutløser.

:::image type="content" source="media/power-automate-flow-dataverse-trigger.png" alt-text="Innstillinger for flytens utløser":::
3. Bruk knappen **AssistEdit (...)** i øvre høyre hjørne til å legge til tilkoblingen i [!INCLUDE [cds_long_md](includes/cds_long_md.md)]-miljøet.
4. Velg **Vis avanserte alternativer**, og angi **customertypecode eq 3** eller **customertypecode eq 11**og **statecode eq 0** i feltet **Filtrer rader**. Disse verdiene betyr at utløseren bare skal reagere når det gjøres endringer i aktive kontoer av typen **kunde** eller **leverandør**.

## <a name="define-the-flow-condition"></a>Definer flytbetingelsen

Data synkroniseres mellom [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE [cds_long_md](includes/cds_long_md.md)] gjennom en integreringsbrukerkonto. Hvis du vil ignorere endringene som er gjort i synkroniseringen, oppretter du et betingelsestrinn i flyten som utelukker endringer som er gjort av integreringsbrukerkontoen.  

1. Legg til trinnet **Hent en rad etter ID fra Dataverse** etter flytutløseren med følgende innstillinger. Hvis du vil ha mer informasjon, kan du se [Hent en rad etter ID fra Dataverse](/power-automate/dataverse/get-row-id).

    1. Velg **Brukere** i **Tabellnavn**-feltet
    2. I **Rad-ID**-feltet velger du **Endret av (verdi)** fra flytutløseren.  

2. Legg til et betingelsestrinn med følgende **eller**-innstillinger for å identifisere integreringsbrukerkontoen.
    1. Brukerens **primære e-postadresse** inneholder **contoso.com**
    2. Brukeren **fulle navn** inneholder **[!INCLUDE[prod_short](includes/prod_short.md)]**.

3. Legg til en avslutningskontroll for å stoppe flyten hvis enheten ble endret av integreringsbrukerkontoen.

Bildet nedenfor viser hvordan du definerer flytutløseren og flytbetingelsen.

:::image type="content" source="media/power-automate-flow-dataverse.png" alt-text="Oversikt over innstillinger for flytutløser og flytbetingelse":::

## <a name="notify-business-central-about-a-change"></a>Varsle Business Central om en endring

Hvis flyten ikke stoppes av betingelsen, må du varsle [!INCLUDE[prod_short](includes/prod_short.md)] om at det oppstod en endring. Bruk [!INCLUDE[prod_short](includes/prod_short.md)]-koblingen til å gjøre det.

1. I **Nei**-forgrening av betingelsestrinnet legger du til en handling og søker etter **Dynamics 365 [!INCLUDE[prod_short](includes/prod_short.md)]**. Velg koblingsikonet i listen
2. Velg handlingen **Opprett oppføring (V3)**.

:::image type="content" source="media/power-automate-flow-dataverse-connector.png" alt-text="Innstillinger for [!INCLUDE[prod_short](includes/prod_short.md)]-koblingen":::

3. Bruk knappen **redigeringsprogram (...)** i øvre høyre hjørne til å legge til tilkoblingen i [!INCLUDE[prod_short](includes/prod_short.md)].
4. Når du er tilkoblet, fyller du ut feltene **Miljønavn** og **Firmanavn**.
5. I feltet **API-kategori** angir du **microsoft/dataverse/v1.0**.
6. Angi **dataverseEntityChanges** i **Tabellnavn**-feltet.
7. Skriv inn **konto** i feltet **entityName**.
8. Lagre flyten.

Bildet nedenfor viser hvordan flyten skal se.

:::image type="content" source="media/power-automate-flow-dataverse-summary.png" alt-text="Oversikt over alle innstillinger for flyten":::

Når du legger til, sletter eller endrer en konto i [!INCLUDE [cds_long_md](includes/cds_long_md.md)]-miljøet, vil denne flyten gjøre følgende handlinger:

1. Kalle opp [!INCLUDE[prod_short](includes/prod_short.md)]‑miljøet du angav i [!INCLUDE[prod_short](includes/prod_short.md)]-koblingen.
2. Bruk [!INCLUDE[prod_short](includes/prod_short.md)]-API-en til å sette inn en post med **entityName** satt til **konto** i tabellen **Dataverse-enhetsendring**. Denne parameteren er det nøyaktige navnet på Dataverse-enheten du oppretter flyten for.
3. [!INCLUDE[prod_short](includes/prod_short.md)] vil starte prosjektkøoppføringen som synkroniserer kunder med kontoer.

## <a name="see-also"></a>Se også

[Bruk Business Central i Power Automate-flyter](across-how-use-financials-data-source-flow.md)  
[Konfigurer automatiserte arbeidsflyter](/business-central/dev-itpro/powerplatform/automate-workflows)  
[Integrere med Microsoft Dataverse](admin-common-data-service.md)  
[Synkroniser data i Business Central med Microsoft Dataverse](admin-synchronizing-business-central-and-sales.md)  
