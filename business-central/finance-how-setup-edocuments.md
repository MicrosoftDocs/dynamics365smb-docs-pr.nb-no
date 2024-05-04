---
title: Konfigurere e-dokumenter
description: Lær hvordan du konfigurerer funksjonen for e-dokumenter.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'electronic document, electronic invoice, e-document, e-invoice'
ms.search.form: '359, 360, 6103, 6133'
ms.date: 04/10/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# <a name="set-up-e-documents"></a>Konfigurere e-dokumenter

> [!IMPORTANT]
> Kjernemodulen for e-dokumenter er et rammeverk. Som standard finnes det ikke noe felt for **Tjenesteintegrering**. Hvis du finner **Dokumentformat**-alternativene som standard, må du være oppmerksom på at de tilbys som et eksempel, og at lokalisering må gi et detaljert format. Disse detaljene er en del av lokaliseringsapper, fordi de er spesifikke for lokale krav.

> [!NOTE]
> Fra og med versjon 23.2 legges et standard PEPPOL-dokumentformat til som et globalt format i **Dokumentformat**-feltet. Husk at du sannsynligvis ikke kan bruke dette formatet som det er. Det er et W1-format som er gitt for å vise hvordan du bruker denne funksjonen. Vi anbefaler at du tester det eksisterende PEPPOL-formatet før du begynner å bruke dette formatet.

Det første trinnet i konfigurasjonen av elektroniske dokumenter (e-dokumenter) er å konfigurere tjenesten for e-dokumenter, der du konfigurerer den fullstendige virkemåten til systemet når det gjelder kommunikasjon med e-dokumenter.

## <a name="set-up-the-e-document-service"></a>Konfigurer e-dokumenttjenesten

Følg disse trinnene for å konfigurere e-dokumenttjenesten.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **E-dokumenttjenester**, og velg deretter den relaterte koblingen.
2. Velg **Ny**, og konfigurer deretter feltene som beskrevet i tabellen nedenfor i hurtigfanen **Generelt** på siden **E-dokumenttjenester**.

    | Felt | Description |
    |-------|-------------|
    |  - kode | Velg konfigurasjonskoden for elektronisk eksport. |
    | Description | Angir en kort beskrivelse av det elektroniske eksportoppsettet. |
    | Dokumentformat | <p>Eksportformatet for det elektroniske eksportoppsettet.</p><p>Som standard er det to alternativer i dette feltet. Du kan velge **PEPPOL BIS 3** som et generelt kodebasert format eller **Data Exchange** når du må sette opp forhåndsdokumenter med spesifikke formater på hurtigfanen **Datautvekslingsdefinisjon**.</p> |
    | Tjenesteintegrering | Velg integreringskoden for det elektroniske eksportoppsettet. I bølge 1 er det eneste alternativet **Ingen integrasjon**. |
    | Bruk bunkebehandling | Angi om tjenesten bruker bunkebehandling for eksport. |

3. Konfigurer feltene som beskrevet i tabellen nedenfor, i hurtigfanen **Importerte parametere**:

    | Felt | Description |
    |-------|-------------|
    | Valider mottaksselskap | Angir om mottaksselskapsinformasjon må valideres under import. |
    | Løs enhet | Angi om enheten skal løses under importen. |
    | Varereferanse for oppslag | Angi om det skal søkes etter en vare med varereferansen under import. |
    | Vare-GTIN for oppslag | Angi om det skal søkes etter en vare etter Global Trade Item Number (GTIN) under import. |
    | Tildelingskonto for oppslag | Angi om det skal søkes etter en konto i **Kontotildelingen** etter den innkommende teksten under importen. |
    | Valider linjerabatt | Angir om en linjerabatt skal valideres under import. |
    | Bruk fakturarabatt | Angi om en fakturarabatt skal brukes under import. |
    | Kontroller totaler | Angi om en fakturatotal skal verifiseres under import. |
    | Oppdater ordre | Angi om tilsvarende bestilling må oppdateres. |
    | Opprett kladdelinjer | Angi om en kladdelinje må opprettes i stedet for et kjøpsdokument. Velg dette alternativet når du vil bruke kladder som mål for fakturaene. |
    | Finanskladdemalnavn | Angi navnet på finanskladdemalen som brukes til oppretting av kladdelinjer. Dette feltet gjelder når du vil bruke kladder som mål for fakturaene. |
    | Finanskladdenavn | Angi navnet på finanskladden som brukes til oppretting av kladdelinjer. Dette feltet gjelder når du vil bruke kladder som mål for fakturaene. |
    | Importer automatisk | Angi om dokumenter skal importeres automatisk fra tjenesten. |
    | Starttidspunkt for bunke | Angi starttidspunktet for importjobber. |
    | Minutter mellom kjøringer | Angi antall minutter mellom importjobbkjøringer. |

4. Hvis du valgte **Datautveksling** i **Dokumentformat**-feltet i **Generelt**-hurtigfanen, bruker du **Datautvekslingsdefinisjon**-hurtigfanen til å angi følgende felter.

    | Felt | Description |
    |-------|-------------|
    | Dokumenttype | Angi dokumenttypen som skal bruke datautveksling til å importere og eksportere dataene. Eksempler inkluderer **salgsfaktura**, **salgskreditnota** og **kjøpsfaktura**. |
    | Importer kode for datautvekslingsdef. | Angi datautvekslingskoden som brukes til å importere dataene. Bruk dette feltet bare for å motta et dokument i kjøpsprosessen. |
    | Eksporter kode for datautvekslingsdef. | Angi datautvekslingskoden som brukes til å eksportere dataene. Bruk dette feltet bare til å levere dokumenter i salgsprosessen. |

> [!NOTE]
> Det er utarbeidet datautvekslingsdefinisjoner for PEPPOL-formatet som er relatert til standard salgs- og kjøpsdokument. Du kan imidlertid sannsynligvis ikke bruke disse definisjonene som de er. De er alle i W1-formater som er gitt for å vise hvordan du bruker denne funksjonen. Vi anbefaler at du tester det eksisterende PEPPOL-formatet før du begynner å bruke dem.

Hvis du har konfigurert formatet **Datautvekslingsdefinisjon** i lokaliseringen, kan du legge til en linje for hver dokumenttype du trenger. Legg til linjer som samsvarer med standard datautvekslingseksempel for W1 PEPPOL-formatet. Velg imidlertid først alternativet **Dokumenttype** for hver linje du trenger. For hver datatype velger du verdien for **Importer Kode for datautveksl.def.** eller **Eksporter Kode for datautveksl.def.** du vil bruke.

Hvis du ikke bruker **Datautvekslingsdefinisjon**-formatet, kan du opprette og konfigurere formater ved å bruke [grensesnittet](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments). Juster informasjonen på linjene **Eksporter tildeling** og **Importer tildeling**, der du kan finne tabellene og feltene som skal konfigureres transformasjonsregler. I dette tilfellet må du legge til et nytt alternativ i **Dokumentformat**-feltet som er relatert til formatet ditt.  

### <a name="supported-document-types"></a>Støttede dokumenttyper

Støttede dokumenttyper er basert på det valgte **dokumentformatet**. Hvis du vil sjekke hvilke dokumenttyper som støttes, velger du handlingen **Støttede dokumenttyper** på siden **E-dokumenttjenester**. **Støttede dokumenttyper for e-dokumenttjeneste** åpnes og i kolonnen **Kildedokumenttype** kan du velge ulike dokumenttyper for å gjøre dem støttet for formatet du planlegger å bruke. Pass på at du ikke bruker dokumenttypen hvis dokumentet ikke er valgt på denne siden.   

## <a name="set-up-a-document-sending-profile"></a>Konfigurere en profil for dokumentsending

Du kan definere en foretrukket metode for å sende salgsdokumenter for hver kunde. På denne måten trenger du ikke å velge et sendealternativ hver gang du velger handlingen **Bokfør og send**. På siden **Profiler for dokumentsending** definerer du ulike sendingsprofiler som velger blant dem i feltet **Profil for dokumentsending** på et kundekort. Du kan merke av for **Standard** for å angi at profilen for en dokumentsending er standardprofilen for alle kunder, bortsett fra kunder der feltet **Profil for dokumentsending** er satt til en annen sendingsprofil.

Denne funksjonaliteten brukes til å konfigurere automatisering av elektronisk fakturering. Når du velger **Bokfør og send** i et salgsdokument, viser dialogboksen **Bokfør og send bekreftelse** sendingsprofilen som brukes, enten profilen som er satt opp for kunden, eller standardprofilen for alle kunder.

Følg disse trinnene for å sette opp en dokumentsendingsprofil.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") angi **Profil for dokumentsending**, og velg deretter den relaterte koblingen.
2. På siden **Profiler for dokumentsending** velger du **Ny**.
3. På hurtigfanen **Generelt** velger eller angir du feltinformasjon etter behov.
4. I hurtigfanen **Sendealternativer** konfigurerer du feltene som beskrevet i tabellen nedenfor.

    | Felt | Description |
    |-------|-------------|
    | Elektronisk dokument | Angi om dokumentet blir sendt som et e-dokument som kunden kan importere til systemet når du velger **Bokfør og send**-knappen. Hvis du vil bruke dette alternativet, må du også angi feltet **Format** eller **Flytkode for elektronisk dokumenttjeneste**. Filen kan eventuelt lagres på disken. |
    | Format | Angi formatet som skal brukes til å sende et e-dokument. Dette feltet er påkrevd hvis du velger **Gjennom dokumentutvekslingstjeneste** i feltet **Elektronisk dokument**. |
    | Flytkode for elektronisk dokumenttjeneste | Angi den elektroniske tjenesteflyten som brukes til sending av dokumenter. Dette feltet er påkrevd hvis du velger **Utvidet e-dokumenttjenesteflyt** i feltet **Elektronisk dokument**. |

    > [!NOTE]
    > Hvis du velger **Utvidet e-dokumenttjenesteflyt** i feltet **Elektronisk dokument** , må du allerede ha arbeidsflyten konfigurert for e-dokumentene.

## <a name="set-up-the-workflow"></a>Konfigurere arbeidsflyten

Følg disse trinnene for å konfigurere arbeidsflyten som brukes i e-dokumentfunksjonalitet.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Arbeidsflytmaler**, og velg deretter den relaterte koblingen.
2. Hvis du ikke finner **vMaler for e-dokumentarbeidsflyt** på siden **Arbeidsflytmaler** , velger du **Tilbakestill Microsoft-maler**. **Maler for e-dokumentarbeidsflyt** skal da vises. Lukk siden.
3. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Arbeidsflyter**, og velg deretter den relaterte koblingen.
4. Velg handlingen **Ny arbeidsflyt fra mal** for å velge en mal for e-dokumentprosessen. De tilgjengelige malene er **Send til én tjeneste** og **Send til flere tjenester**.
5. Velg **OK** for å fullføre arbeidsflytoppsettet.
6. I feltet **Så svar** velger du **Send e-dokument ved hjelp av installasjonsprogrammet** for å konfigurere arbeidsflytsvarene.
7. Velg e-dokumenttjenesten du opprettet som et alternativ, velg **OK**, og aktiver deretter arbeidsflyten.

> [!NOTE]
> Du kan opprette din egen arbeidsflyt for e-dokumenter uten å bruke forhåndsdefinerte arbeidsflytmaler. Hvis du har flere tjenester, kan du bruke forskjellige arbeidsflyter.

For å bruke flere arbeidsflytprosesser må du konfigurere dem gjennom profilene for dokumentsending for forskjellige kunder. Når du setter opp arbeidsflyten, må du angi profilen for dokumentsending i **On Condition**-kolonnen på **Arbeidsflyttrinn**-hurtigfanen fordi du ikke kan ha to tjenester som bruker samme profil for dokumentsending i arbeidsflytprosesser.

Når du konfigurerer arbeidsflyten på **Arbeidsflytprosesser**-siden, peker du på **Ved betingelse**-feltet på **Arbeidsflyttrinn**-hurtigfanen. På **Hendelsesbetingelser**-siden i **Filter**-feltet velger du profilen for dokumentsending som du vil bruke.

## <a name="set-up-a-retention-policy-for-e-documents"></a>Konfigurere en oppbevaringspolicy for e-dokumenter

E-dokumenter kan være underlagt ulike lokale lover som er knyttet til perioden som e-dokumentene oppbevares. Derfor har vi lagt til et oppsett for oppbevaringspolicy for all viktig informasjon som er knyttet til e-dokumenter. Administratorer kan definere oppbevaringspolicyer som angir hvor ofte Dynamics 365 Business Central sletter utdaterte poster som er relatert til e-dokumenter. Hvis du vil finne ut mer om oppbevaringspolicyer, kan du se [Definer oppbevaringspolicyer](admin-data-retention-policies.md).

Hvis du vil konfigurere e-dokumentrelaterte oppbevaringspolicyer, gjør du følgende.

1. Velg handlingen **Oppbevaringspolicy** på siden **E-dokumenttjenester**.
2. Når handlingen er fullført, velger du en av følgende oppbevaringspolicyer for å konfigurere:

    - E-dokumentlogg
    - Logg for e-dokumentintegrering
    - Tildelingslogg for e-dokument
    - Datalager for e-dokument

## <a name="e-documents-demo-data"></a>Demonstrasjonsdata for e-dokumenter

> [!NOTE]
> Fra Business Central, versjon 24.0 er det mulig å definere demodata for e-dokumenter.

For å kunne tilby enklere måter å teste og demonstrere funksjonene i **e-dokumenter** opprettet Microsoft en ny demomodul for elektroniske dokumenter. Følg fremgangsmåten for å aktivere denne modulen:  

1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Demoverktøy for Contoso**, og velg deretter den relaterte koblingen.  
2.  Før du aktiverer **Contoso-modulen for e-dokument**, må du på grunn av avhengigheter ha aktivert følgende moduler: **Fellesmodul** og **Lagermodul**. 
3.  Når du har aktivert disse modulene, velger du **Contoso-modulen for e-dokumenter**, og deretter velger du handlingen **Generer**. 
4.  Følg fremgangsmåten.  
5.  Lukk siden.   

Når du har en aktivert modul, har du opprettet nye demovarer, importert seks elektroniske dokumenter (basert på Peppol BIS 3) og allerede konfigurert **E-dokumenttjenester** med opprettede arbeidsflytprosesser.  

## <a name="see-also"></a>Se også

[Slik bruker du e-dokumenter i salg](finance-how-use-edocuments.md)    
[Slik bruker du e-dokumenter i kjøp](finance-how-use-edocuments-purchase.md)  
[Slik utvider du e-dokumenter i Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments)    
[Økonomistyring](finance.md)    
[Fakturere salg](sales-how-invoice-sales.md)    
[Registrer kjøp med kjøpsfakturaer og ordrer](purchasing-how-record-purchases.md)    
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
