---
title: Koble til Microsoft Dataverse (inneholder video)
description: Konfigurer en kobling mellom Business Central og Dataverse. Selskaper oppretter vanligvis tilkoblingen for å integrere data med en annen Dynamics 365-forretningsapp.
author: brentholtorf
ms.topic: conceptual
ms.workload: na
ms.search.keywords: null
ms.search.forms: '7200, 7201'
ms.date: 09/28/2023
ms.author: bholtorf
---
# <a name="connect-to-microsoft-dataverse"></a>Koble til Microsoft Dataverse

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Denne artikkelen beskriver hvordan du setter opp en tilkobling mellom [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Vanligvis oppretter selskaper tilkoblingen for å integrere og synkronisere data med en annen Dynamics 365-forretningsapp, for eksempel [!INCLUDE[crm_md](includes/crm_md.md)].  

## <a name="before-you-start"></a>Før du begynner

Før du oppretter tilkoblingen, er det noen få opplysninger du må ha klar:  

* URL-adressen til [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-miljøet du vil koble til. Hvis du bruker veiledningen for assistert oppsett **Tilkoblingsoppsett for Dataverse** til å opprette tilkoblingen, finner vi miljøene dine. Du kan også skrive inn nettadressen til et annet miljø i leietakeren din.  
* Brukernavnet og passordet for en konto som har administratorrettigheter i [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  
* Hvis du har en lokal [!INCLUDE[prod_short](includes/prod_short.md)] 2020 lanseringsbølge 1, versjon 16.5, kan du lese artikkelen [Noen kjente problemer](/dynamics365/business-central/dev-itpro/upgrade/known-issues#wrong-net-assemblies-for-external-connected-services). Du må fullføre den beskrevne løsningen før du kan opprette tilkoblingen til [!INCLUDE[cds_long_md](includes/cds_long_md.md)].
* De lokale valutaene som hvert selskap bruker. [!INCLUDE [prod_short](includes/prod_short.md)]-selskaper kan koble til et [!INCLUDE [cds_long_md](includes/cds_long_md.md)]-miljø som har en standardvaluta som skiller seg fra den lokale valutaen. Hvis du vil vite mer om hvordan du håndterer oppsett med flere valutaer, kan du gå til [Tillat for ulike valutaer](#allow-for-different-currencies).

> [!IMPORTANT]
> [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-miljøet ditt må ikke være i administrasjonsmodus. Administrasjonsmodus vil føre til at tilkoblingen mislykkes fordi integrasjonsbrukerkontoen for tilkoblingen ikke har administratortilgang. Se også [Administrasjonsmodus](/power-platform/admin/admin-mode) for mer informasjon.

> [!Note]
> Følgende trinn beskriver fremgangsmåten for [!INCLUDE[prod_short](includes/prod_short.md)] på nett.
> Hvis du bruker [!INCLUDE[prod_short](includes/prod_short.md)] lokalt og ikke bruker Microsoft Entra-kontoen til å koble til [!INCLUDE [cds_long_md](includes/cds_long_md.md)], må du også angi brukernavn og passord for en brukerkonto for integrasjonen. Denne kontoen kalles kontoen for "integrasjonsbruker". Hvis du bruker en Microsoft Entra-konto, er ikke brukerkontoen for integrasjon nødvendig eller vist. Brukeren for integrasjon konfigureres automatisk og krever ikke en lisens.

## <a name="allow-for-different-currencies"></a>Tillate ulike valutaer

[!INCLUDE [prod_short](includes/prod_short.md)]-selskaper kan koble til et [!INCLUDE [cds_long_md](includes/cds_long_md.md)]-miljø som har en standardvaluta som skiller seg fra den lokale valutaen.

> [!NOTE]
> Synkronisering av flere valutaer krever at du bruker en ensrettet synkronisering, fra [!INCLUDE [prod_short](includes/prod_short.md)] til [!INCLUDE [cds_long_md](includes/cds_long_md.md)].

Hvis du vil ha mer informasjon om standardvalutaen [!INCLUDE [cds_long_md](includes/cds_long_md.md)], kan du gå til [Transaksjonsvaluta-enhet](/powerapps/developer/data-platform/transaction-currency-currency-entity). 

Hvis du vil finne ut mer om valutaer i [!INCLUDE [prod_short](includes/prod_short.md)], kan du gå til [Valutaer i Business Central](finance-currencies.md).

Hvis du vil tillate forskjellige valutaer, må du kontrollere at du har angitt følgende innstillinger før du kobler til:

* Innstillingen for basistransaksjonsvaluta i [!INCLUDE [cds_long_md](includes/cds_long_md.md)] har valutakoden som er angitt på **Valutaer**-siden i [!INCLUDE [prod_short](includes/prod_short.md)].
* Det er minst én valutakurs angitt for valutaen i [!INCLUDE [prod_short](includes/prod_short.md)] på siden **Valutakurser**.

Når du aktiverer tilkoblingen til [!INCLUDE [cds_long_md](includes/cds_long_md.md)] legger den lokale valutaen til [!INCLUDE [prod_short](includes/prod_short.md)], legger det til lokal valuta i enheten **Valuta** i [!INCLUDE [cds_long_md](includes/cds_long_md.md)]. Den lokale valutaen bruker valutakursen fra feltet **Valutafaktor** på siden **Valutakurser**.

Fordi valutasynkronisering er enveis, fra [!INCLUDE [prod_short](includes/prod_short.md)] til [!INCLUDE [cds_long_md](includes/cds_long_md.md)], konverteres og synkroniseres pengebeløp på følgende måte:

* I [!INCLUDE [cds_long_md](includes/cds_long_md.md)] standardvalutaen konverteres beløp til [!INCLUDE [prod_short](includes/prod_short.md)] lokal valuta basert på den siste valutakursen som er synkronisert fra [!INCLUDE [prod_short](includes/prod_short.md)].
* I [!INCLUDE [prod_short](includes/prod_short.md)] lokal valuta synkroniseres beløpene med [!INCLUDE [prod_short](includes/prod_short.md)] lokal valuta i en av de andre ikke-standardvalutaene i [!INCLUDE [cds_long_md](includes/cds_long_md.md)].

## <a name="set-up-a-connection-to-"></a>Konfigurer en tilkobling til [!INCLUDE[cds_long_md](includes/cds_long_md.md)]

For andre godkjenningstyper enn Microsoft 365-godkjenning definerer du en tilkobling til [!INCLUDE[cds_long_md](includes/cds_long_md.md)] på siden **Tilkoblingsoppsett for Dataverse**. For Microsoft 365-godkjenning anbefales det å bruke den assisterte oppsettsveiledningen for **Konfigurasjon for Dataverse-tilkobling**. Veiledningen gjør det enklere å opprette tilkoblingen og angi avanserte funksjoner, for eksempel eierskapsmodell og første synkronisering.  

> [!IMPORTANT]
> Under oppsettet av tilkoblingen til [!INCLUDE[cds_long_md](includes/cds_long_md.md)] blir administrator bedt om å gi følgende tillatelse til å registrere et Azure-program kalt [!INCLUDE[prod_short](includes/prod_short.md)]-integrering til [!INCLUDE[cds_long_md](includes/cds_long_md.md)]:
>
> * Tillatelsen **Gå til [!INCLUDE[cds_long_md](includes/cds_long_md.md)] som deg** kreves, slik at [!INCLUDE[prod_short](includes/prod_short.md)] kan, på vegne av administratoren, automatisk opprette en ikke-lisensiert, ikke-interaktiv [!INCLUDE[prod_short](includes/prod_short.md)] Integration-appbruker, tilordne sikkerhetsroller til denne brukeren og distribuere [!INCLUDE[prod_short](includes/prod_short.md)] Integration-løsningen til [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Denne tillatelsen brukes bare én gang under oppsett av kobling til [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  
> * Tillatelse for å **ha full tilgang til Dynamics 365 [!INCLUDE[prod_short](includes/prod_short.md)]** kreves, slik at den automatisk opprettede programbrukeren for [!INCLUDE[prod_short](includes/prod_short.md)]-integrering har tilgang til [!INCLUDE[prod_short](includes/prod_short.md)]-data som skal synkroniseres.  
> * Tillatelse for å **logge på og lese profilen din** kreves for å bekrefte at brukeren som logger på, faktisk har sikkerhetsrollen for systemansvarlig tilordnet i [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  
>
> Ved å gi samtykke på vegne av organisasjonen, gir administrator det registrerte Azure-programmet som kalles [!INCLUDE[prod_short](includes/prod_short.md)]-integrering med [!INCLUDE[cds_long_md](includes/cds_long_md.md)], rett til å synkronisere data ved hjelp av automatisk opprettet legitimasjon for programbruker for [!INCLUDE[prod_short](includes/prod_short.md)]-integrering.

### <a name="to-use-the-dataverse-connection-setup-assisted-setup-guide"></a>Slik bruker du den assisterte oppsettsveiledningen for Konfigurasjon for Dataverse-tilkobling

Oppsettveiviseren for konfigurasjon av Dataverse-tilkobling kan gjøre det enklere å koble til programmene, og kan til og med hjelpe deg med å kjøre en innledende synkronisering. Hvis du velger å kjøre innledende synkronisering, vil [!INCLUDE[prod_short](includes/prod_short.md)] se gjennom dataene i begge programmene og gi anbefalinger for hvordan innledende synkronisering skal utføres. Tabellen nedenfor beskriver anbefalingene.

|Anbefaling  |Beskrivelse  |
|---------|---------|
|**Full synkronisering**|Dataene finnes bare i [!INCLUDE[prod_short](includes/prod_short.md)] eller bare i [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Anbefalingen er å synkronisere alle data fra tjenesten som har de, til den andre tjenesten.|
|**Ingen synkronisering**|Dataene finnes i begge programmene, og det vil duplisere dataene ved å kjøre full synkronisering. Anbefalingen er å koble poster.|
|**Avhengighet ikke tilfredsstilt**|Dataene finnes i begge programmene, men raden eller tabellen kan ikke synkroniseres, fordi den avhenger av en rad eller tabell som har anbefaling om ingen synkronisering. Hvis for eksempel kundene ikke kan synkroniseres, kan heller ikke data for kontakter som er avhengige av kundedata, synkroniseres.|

> [!IMPORTANT]
> Vanligvis bruker du bare full synkronisering når du integrerer programmene for første gang, og bare ett program inneholder data. Full synkronisering kan være nyttig i et demonstrasjonsmiljø fordi det automatisk oppretter og kobler poster i hvert program, noe som gjør det raskere å begynne å arbeide med synkroniserte data. Du må derimot bare utføre en full synkronisering hvis du vil ha én rad i [!INCLUDE[prod_short](includes/prod_short.md)] for hver rad i [!INCLUDE[cds_long_md](includes/cds_long_md.md)] for de gitte tabelltilordningene. Hvis ikke kan resultatet være dupliserte poster.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Assistert oppsett** og velger den relaterte koblingen.
2. Velg **Konfigurer en tilkobling til Microsoft Dataverse** for å starte assistert oppsettsveiledning.
3. Fyll ut feltene etter behov.

> [!NOTE]
> Hvis du ikke blir bedt om å logge på med administratorkontoen, skyldes det trolig at popup-vinduer er blokkert. Hvis du vil logge på, må du tillate popup-vinduer fra `https://login.microsoftonline.com`.

### <a name="to-create-or-maintain-the-connection-manually"></a>Opprette eller vedlikeholde tilkoblingen manuelt

Følgende fremgangsmåte beskriver hvordan du konfigurerer tilkoblingen manuelt på siden **Konfigurasjon for Dataverse-tilkobling**. Du håndterer integrasjonsinnstillinger på siden **Tilkoblingsoppsett for Dataverse**.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Dataverse-tilkoblingsoppsett** og velger den relaterte koblingen.
2. Skriv inn følgende informasjon for tilkoblingen fra [!INCLUDE[prod_short](includes/prod_short.md)] til [!INCLUDE[cds_long_md](includes/cds_long_md.md)].

    |Felt|Beskrivelse|
    |-----|-----|
    |**URL-adresse for miljø**|Hvis du eier miljøer i [!INCLUDE[cds_long_md](includes/cds_long_md.md)], finner vi dem for deg når du kjører installasjonsveiledningen. Hvis du vil koble til et annet miljø i en annen leier, kan du angi administratorlegitimasjon for miljøet slik at vi kan finne det. |
    |**Aktivert**|Begynn å bruke integrasjonen. Hvis du ikke aktiverer tilkoblingen nå, lagres tilkoblingsinnstillingene, men brukerne vil ikke ha tilgang til [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-data fra [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan gå tilbake til denne siden og aktivere tilkoblingen senere.  |

3. I feltet **Eierskapsmodell** velger du om du vil ha en teamtabell i [!INCLUDE[cds_long_md](includes/cds_long_md.md)] til egne nye poster, eller én eller flere bestemte brukere. Hvis du velger **Person**, må du angi hver bruker. Hvis du velger **Team**, vil standard forretningsenhet vises i feltet **Koblet konsern**.

    <!--Need to verify the details in this table, are these specific to Sales maybe?  IK: No they are not and no longer relevant 
    Enter the following advanced settings.-->

    <!-- |Field|Description|
    |-----|-----|
    |**[!INCLUDE[prod_short](includes/prod_short.md)] Users Must Map to CDS Users**|If you're using the Person ownership model, specify whether [!INCLUDE[prod_short](includes/prod_short.md)] user accounts must have a matching user accounts in [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. The **Microsoft 365 Authentication Email** of the [!INCLUDE[prod_short](includes/prod_short.md)] user must be the same as the **Primary Email** of the [!INCLUDE[crm_md](includes/crm_md.md)] user.<br /><br /> If you set the value to **Yes**, [!INCLUDE[prod_short](includes/prod_short.md)] users who don't have a matching [!INCLUDE[crm_md](includes/crm_md.md)] user account won't have [!INCLUDE[prod_short](includes/prod_short.md)] integration capabilities in the user interface. Access to [!INCLUDE[crm_md](includes/crm_md.md)] data directly from [!INCLUDE[prod_short](includes/prod_short.md)] is done on behalf of the [!INCLUDE[crm_md](includes/crm_md.md)] user account.<br /><br /> If you set the value to **No**, all [!INCLUDE[prod_short](includes/prod_short.md)] users will have [!INCLUDE[crm_md](includes/crm_md.md)] integration capabilities in the user interface. Access to [!INCLUDE[crm_md](includes/crm_md.md)] data is done on behalf of the [!INCLUDE[crm_md](includes/crm_md.md)] connection (integration) user.|
    |**Current Business Central Salesperson is Mapped to a User**|Indicates whether your user account is mapped to an account in [!INCLUDE[crm_md](includes/crm_md.md)] double check the name of this field|-->
4. Hvis du vil teste tilkoblingsinnstillingene, velger du **Tilkobling** og deretter **Test tilkobling**.  

    > [!NOTE]  
    > Hvis datakryptering ikke er aktivert i [!INCLUDE[prod_short](includes/prod_short.md)], får du bli spurt om du vil aktivere den. Hvis du vil aktivere datakryptering, velger du **Ja** og angir nødvendig informasjon. Ellers velger du **Nei**. Du kan aktivere datakryptering senere. Hvis du vil ha mer informasjon, kan du se [Kryptere data i Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-encrypting-data) i hjelpen for utviklere og administrasjon.  
5. Hvis [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-synkronisering ikke allerede er satt opp, vil du bli spurt om du vil bruke standard synkroniseringsoppsett. Avhengig av om du vil beholde postene som er justert i [!INCLUDE[cds_long_md](includes/cds_long_md.md)] og [!INCLUDE[prod_short](includes/prod_short.md)], velger du **Ja** eller **Nei**.

<!--
## <a name="show-me-the-process"></a>Show Me the Process

The following video shows the steps to connect [!INCLUDE[prod_short](includes/prod_short.md)] and [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. <br>
  
> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4ArlP]

-->

## <a name="customize-the-match-based-coupling"></a>Tilpass samsvarsbasert kobling

Fra og med lanseringsbølge 2 for 2021 kan en administrator angi vilkår for å koble poster basert på samsvar. Du kan starte algoritmen for samsvarende poster fra følgende steder i [!INCLUDE [prod_short](includes/prod_short.md)]:

* Vis sider som viser poster som er synkronisert med [!INCLUDE [cds_long_md](includes/cds_long_md.md)], for eksempel sidene Kunder og Varer.  

    Velg flere poster, og velg deretter **Relatert**-handling, velg **Dataverse**, velg **Kobling** og velg deretter lik **Samsvartbasert kobling**.

    Når du starter den samsvarsbaserte koblingsprosessen fra en hoveddatakilde, blir en koblingsjobb planlagt etter at du har angitt koblingskriteriene.  
* Siden **Gjennomgang av full synkronisering for Dataverse**.  

    Når den fullstendige synkroniseringsprosessen oppdager at du har poster som ikke er koblet, i [!INCLUDE [prod_short](includes/prod_short.md)] og [!INCLUDE [cds_long_md](includes/cds_long_md.md)], vises en **Velg koblingskriterier**-kobling for integreringstabellen.  

    Du kan starte prosessen **Kjør full synkronisering** fra sidene **Tilkoblingsoppsett for Dataverse** og **Tilkoblingsoppsett for Dynamics 365**. Du kan også starte veiledningen for assistert oppsett **Konfigurer en tilkobling til Dataverse** når du full fører installasjonen.  

    Når du starter den samsvarsbaserte koblingsprosessen fra siden **Gjennomgang av full synkronisering for Dataverse**, blir en koblingsjobb planlagt etter at du har fullført oppsettet.  
* Listen **Tilordninger for integreringstabell**.  

    Velg en tilordning, velg **Kobling**-handlingen, og velg deretter **Samsvarsbasert kobling**.

    Når du starter den samsvarende koblingsprosessen fra en tilordning for integreringstabell, kjøres en koblingsjobb for alle ikke-koblede poster i tildelingen. Du kan også merke av for frakoblede poster i listen for å kjøre jobben bare for disse postene.

I alle tre tilfeller åpnes siden **Velg koblingskriterier**, slik at du kan definere relevante koblingskriterier. På denne siden tilpasser du koblingen med følgende oppgaver:

* Velg feltene som skal brukes til å samsvare [!INCLUDE [prod_short](includes/prod_short.md)]-poster med [!INCLUDE [cds_long_md](includes/cds_long_md.md)]-enheter. Du kan angi om samsvaret skiller mellom store og små bokstaver.  

* Angi om du vil synkronisere etter at du har koblet poster. Hvis poster bruker toveistildeling, kan du også angi hva som skal skje hvis det er konflikter på listen, på siden **Løs oppdateringskonflikter**.  

* Prioriter rekkefølgen du søker etter poster i, ved å angi en *samsvarsprioritet* for de relevante tilordningsfeltene. [!INCLUDE [prod_short](includes/prod_short.md)] vil søke etter samsvar i stigende rekkefølge basert på verdien i feltet **Samsvarsprioritet**. En tom verdi i feltet **Samsvarsprioritet** er lik prioritet 0, som er den høyeste prioriteten. Felter som har prioriteten 0, vurderes først.  

* Angi om det skal opprettes en ny enhetsforekomst i [!INCLUDE [cds_long_md](includes/cds_long_md.md)] i tilfelle det ikke finnes unikt, ikke-koblet samsvar ved å bruke samsvarskriteriene. Hvis du vil aktivere denne funksjonen, velger du **Opprett ny hvis det ikke finnes et samsvar**-handling.  

### <a name="view-the-results-of-the-coupling-job"></a>Vis resultatene av koblingsjobben

Hvis du vil vise resultatene av koblingsjobben, åpner du siden **Tilordninger for integreringstabell**, velger den relevante tilordningen, velger handlingen **Kobling** og velger handlingen **Logg for koblingsjobb for integrering**.  

Hvis poster ikke ble koblet, kan du velge verdien i kolonnen **Mislyktes** for å åpne en liste over feil som beskriver hvorfor det skjedde.  

Kobling kan vanligvis mislykkes av følgende årsaker:

* Ingen samsvarende kriterier ble definert

    Kjør den samsvarsbaserte koblingen på nytt, men husk å definere koblingskriterier.

* Fant ingen treff for feltene som er angitt i samsvarskriteriene

    Gjenta koblingen ved å bruke andre felter.

* Fant flere treff for flere poster, basert på feltene angitt i samsvarkriteriene  

    Gjenta koblingen ved å bruke andre felter.

* Fant et treff, men den samsvarende posten er allerede koblet med en post i [!INCLUDE [prod_short](includes/prod_short.md)]  

    Gjenta koblingen ved å bruke andre felter, eller undersøker hvorfor [!INCLUDE [cds_long_md](includes/cds_long_md.md)]-enheten er koblet med posten i [!INCLUDE [prod_short](includes/prod_short.md)].

> [!TIP]
> Hvis du vil ha hjelp til å få en oversikt over fremdriften til koblingen, viser feltet **Koblet til Dataverse**om en post er koblet til en [!INCLUDE [cds_long_md](includes/cds_long_md.md)]-enhet. Du kan bruke feltet **Koblet til Dataverse** til å filtrere listen over poster du synkroniserer.

## <a name="upgrade-connections-from-business-central-online-to-use-certificate-based-authentication"></a>Oppgrader tilkoblinger fra Business Central Online for å bruke sertifikatbasert godkjenning

> [!NOTE]
> Denne delen er bare relevant for [!INCLUDE[prod_short](includes/prod_short.md)] online-leiere som kjører på Microsoft. Online-leietakere som kjører på ISV-er, og lokale installasjoner, påvirkes ikke.

I april 2022 avskriver [!INCLUDE[cds_long_md](includes/cds_long_md.md)] Office365-godkjenningstypen (brukernavn/passord). Hvis du vil ha mer informasjon, kan du se [Avskriving av Office365-godkjenningstypen](/power-platform/important-changes-coming#deprecation-of-office365-authentication-type-and-organizationserviceproxy-class-for-connecting-to-dataverse). I mars 2022 avskriver [!INCLUDE[prod_short](includes/prod_short.md)] bruken av klienthemmelighetsbasert tjeneste-til-tjeneste-godkjenning for nettbaserte leietakere. Du må bruke sertifikatbasert tjeneste-til-tjeneste-godkjenning for tilkoblinger til [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. [!INCLUDE[prod_short](includes/prod_short.md)]-nettleietakere som driftes av ISV-er og lokale installasjoner, kan fortsette å bruke klienthemmeligheter for godkjenning.

For å unngå å forstyrrende integreringer _må du oppgradere_ tilkoblingen for å kunne bruke sertifikatbasert godkjenning. Selv om endringen er planlagt i mars 2022, anbefaler vi på det sterkeste at du oppgraderer så snart som mulig. Følgende trinn beskriver hvordan du oppgraderer til sertifikatbasert godkjenning. 

### <a name="to-upgrade-your-business-central-online-connection-to-use-certificate-based-authentication"></a>Slik oppgraderer du tilkoblinger for Business Central online til å bruke sertifikatbasert godkjenning

1. Avhengig av om du integrerer med Dynamics 365 Sales, gjør du et av følgende:
   * Hvis du gjør det, åpner du siden **Tilkoblingsoppsett for Microsoft Dynamics 365**.
   * Hvis du ikke gjør det, åpner du siden **Tilkoblingsoppsett for Dataverse**.
2. Velg **Tilkobling** og deretter **Bruk sertifikatgodkjenning** for å oppgradere tilkoblingen til å bruke sertifikatbasert godkjenning.
3. Logg på med administratorlegitimasjon for Dataverse. Det skal ta under ett minutt å logge seg på.

> [!NOTE]
> Du må gjenta disse trinnene i hvert [!INCLUDE[prod_short](includes/prod_short.md)]-miljø, for eksempel både produksjons- og sandkassemiljøer, og i hvert selskap der du er koblet til i [!INCLUDE[cds_long_md](includes/cds_long_md.md)].

## <a name="connecting-on-premises-versions"></a>Koble til lokale versjoner

Hvis du vil koble [!INCLUDE[prod_short](includes/prod_short.md)] lokalt til [!INCLUDE[cds_long_md](includes/cds_long_md.md)], må du angi informasjon på siden **Tilkoblingsoppsett for Dataverse**.

Du må registrere et program i Microsoft Entra-ID for å koble til med en Microsoft Entra-konto. Du må oppgi program-ID-en, hemmeligheten for nøkkelhvelv og nettadressen som skal brukes. Nettadressen for omdirigering er forhåndsutfylt og skal fungere for de fleste installasjoner. Du må konfigurere installasjonen til å bruke HTTPS. Hvis du vil ha mer informasjon, kan du se [Konfigurere SSL for å sikre nettklienttilkoblingen for Business Central](/dynamics365/business-central/dev-itpro/deployment/configure-ssl-web-client-connection). Hvis du konfigurerer serveren slik at den har en annen hjemmeside, kan du endre nettadressen. Klienthemmeligheten vil bli lagret som en kryptert streng i databasen. 

### <a name="to-register-an-application-in-microsoft-entra-id-for-connecting-from-business-central-to-dataverse"></a>Slik registrerer du et program i Microsoft Entra ID for tilkobling fra Business Central til Dataverse

Fremgangsmåten nedenfor forutsetter at du bruker Microsoft Entra ID til å administrere identiteter og tilgang. Hvis du vil ha mer informasjon om hvordan du registrerer et program i Microsoft Entra ID, kan du se [Hurtigstart: Registrere et program i Microsoft Identity Platform](/azure/active-directory/develop/quickstart-register-app). 

1. Velg **Godkjenning** i Azure-portalen under **Behandle** i navigasjonsruten.  
2. Under **nettadresser for omdirigering** legger du til nettadressen for omdirigering som foreslås på siden **Tilkoblingsoppsett for Dataverse** i [!INCLUDE[prod_short](includes/prod_short.md)].
3. Velg **API-tillatelser** under **Behandle**.
4. Under **Konfigurerte tillatelser** velger du **Legg til tillatelse**, og deretter legger du til delegerte tillatelser i kategorien **Microsoft API-er** på følgende måte:
    * For Business Central legger du til tillatelsene **Financials.ReadWrite.All**.
    * For Dynamics CRM legger du til tillatelsene **user_impersonation**.  

    > [!NOTE]
    > Navnet på Dynamics CRM-API-et kan endres.

5. Under **Behandle** velger du **Sertifikater og hemmeligheter**, og deretter oppretter du en ny hemmelighet for appen. Du bruker hemmeligheten i [!INCLUDE[prod_short](includes/prod_short.md)], i feltet **Klienthemmelighet** på siden **Tilkoblingsoppsett for Dataverse**, eller du lagrer på en sikker lagringsplass og angir det i et hendelsesabonnent, som beskrevet tidligere i dette emnet.
6. Velg **Oversikt**, og finn deretter verdien **ID (klient) for programmet**. Denne ID-en er klient-ID-en for programmet. Du må angi den på siden **Tilkoblingsoppsett for Dataverse** i feltet **Klient-ID**, eller lagre den på en sikker lagringsplass og angi den i et hendelsesabonnent.
7. I [!INCLUDE[prod_short](includes/prod_short.md)], på siden **Tilkoblingsoppsett for Dataverse** i feltet **Nettadresse for miljø**, angir du nettadressen for [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-miljøet.
8. Hvis du vil aktivere tilkoblingen til [!INCLUDE[cds_long_md](includes/cds_long_md.md)], aktiverer du alternativet **Aktivert**.
9. Logg på med administratorkontoen din for Microsoft Entra ID (denne kontoen må ha en gyldig lisens for [!INCLUDE[cds_long_md](includes/cds_long_md.md)] og være administrator i ditt [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-miljø). Når du har logget på, blir du bedt om å tillate at det registrerte programmet kan logge på [!INCLUDE[cds_long_md](includes/cds_long_md.md)] på vegne av organisasjonen. Du må gi samtykke for å fullføre oppsettet.

   > [!NOTE]
   > Hvis du ikke blir bedt om å logge på med administratorkontoen, skyldes det trolig at popup-vinduer er blokkert. Hvis du vil logge på, må du tillate popup-vinduer fra `https://login.microsoftonline.com`.

### <a name="to-disconnect-from-"></a>For å koble fra [!INCLUDE[cds_long_md](includes/cds_long_md.md)]

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Dataverse-tilkoblingsoppsett** og velger den relaterte koblingen.
2. På siden **Konfigurasjon for Dataverse-tilkobling** deaktiverer du alternativet **Aktivert**.  

## <a name="see-also"></a>Se også

[Vise statusen for en synkronisering](admin-how-to-view-synchronization-status.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
