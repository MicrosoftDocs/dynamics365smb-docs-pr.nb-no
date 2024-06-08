---
title: Bruk e-dokumenter i kjøpsprosessen
description: Lær hvordan du bruker funksjoner for e-dokument som er knyttet til fakturaer og bestillinger.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'electronic document, electronic invoice, e-document, e-invoice, receive, purchase, matching, mapping, Copilot'
ms.search.form: '50, 51, 138, 6103, 6133, 6121, 6167, 9307, 9308'
ms.date: 05/02/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# <a name="use-e-documents-in-the-purchases-process"></a>Bruk e-dokumenter i kjøpsprosessen

Du kan bruke konfigurerte elektroniske dokumenter (e-dokumenter) med kjøpsdokumentene.

Du kan bruke følgende kjøpsdokumenter med e-dokumentfunksjonalitet:  

- Kjøpsfakturaer
- Bestillinger (fra versjon 24.0)
- Kjøpskreditnotaer
- Finanskladder

> [!NOTE]
> Fra [!INCLUDE[prod_short](includes/prod_short.md)], versjon 24.0 er det mulig å koble **bestillinger** til de mottatte **e-dokumentene**.  

## <a name="e-documents-in-purchases"></a>E-dokumenter ved kjøp

Mottak av e-dokumenter i Dynamics 365 Business Central kan utføres som en kjørsel eller manuelt.  

### <a name="how-to-set-up-vendors-to-work-with-different-purchase-documents"></a>Slik konfigurerer du leverandører til å arbeide med ulike kjøpsdokumenter

Følg denne fremgangsmåten for å konfigurere leverandører til å fungere riktig med innkommende elektroniske fakturaer: 

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Leverandører** og velg den relaterte koblingen. 
2. Velg leverandøren du vil konfigurere.   
3. Finn feltet **Motta e-dokument til** i hurtigfanen **Mottak** for å angi standard kjøpsdokument som skal genereres fra det mottatte e-dokumentet. 

   > [!NOTE]
   > I feltet **Motta e-dokument til** kan brukerne velge en **kjøpsfaktura** eller en **bestilling** basert på hva de vil ha opprettet fra den mottatte e-fakturaen. Dette valget påvirker ikke opprettingen av korrigerende dokumenter. I begge scenarioer genererer systemet en **kreditnota**.  

   > [!NOTE]
   > Hvis brukeren velger alternativet **Bestilling** i feltet **Motta e-dokument til**, prøver systemet å oppdatere en av de eksisterende bestillingene, men hvis bestillingen for en leverandør i det mottatte **e-dokumentet** ikke finnes, oppretter [!INCLUDE[prod_short](includes/prod_short.md)] en ny **bestilling** på samme måte som oppretting av de nye **kjøpsfakturaene** som forklares på denne siden senere.  

4. Velg et av alternativene du vil bruke for den valgte leverandøren. 
5. Lukk siden.   

### <a name="to-work-with-purchase-invoices"></a>Slik arbeider du med kjøpsfakturaer

#### <a name="run-the-batch-job"></a>Kjør kjørselen

> [!NOTE]
> Denne kjørselen er for automatisk innsamling av innkommende fakturaer. Den kan bare fungere i et land eller område der funksjonaliteten finnes.  

Hver gang en **Jobbkø** er valgt å kjøre, og den eksterne tjenesten har innkommende fakturaer som ble sendt fra leverandøren, samler systemet inn og importerer disse fakturaene. Følg disse trinnene for å fullføre prosessen: 

1. Når kjørselen er ferdig, vises de nylig importerte fakturaene på siden **E-dokumenter** sammen med grunnleggende detaljinformasjon. 
2. Hvis du vil vise flere detaljer, åpner du et bestemt e-dokument.   
3. Hvis det ikke var noen feil eller problemer i e-dokumentet, tildeler feltet **Post** dokumentnummeret på kjøpsfakturaen, hvis dette er konfigurer på siden **Leverandørkort** (som systemet opprettet automatisk). Velg koblingen for å åpne dokumentet.
 
   > [!NOTE]
   > Dette systemopprettede dokumentet er ikke det bokførte dokumentet. 

4. Hvis du vil gå direkte til kjøpsdokumentet, velger du **Post**-feltet. Når du har åpnet **Kjøpsfaktura**-siden, kontrollerer du dokumentet. Hvis alt er riktig, bokfør dokumentet.  
5. Når du bokfører kjøpsdokumentet, oppdateres **Post**-feltet i **E-dokumentet** fra **Faktura** til **Kjøpsfaktura**, og nummeret på det bokførte kjøpsdokumentet er tilgjengelig. Du kan velge nummeret for å åpne den bokførte kjøpsfakturaen. 

Detaljer om logger er de samme som i salgsprosessen for e-dokumenter.  

Siden feil i salgsprosessen for det meste er knyttet til tilgjengeligheten til tjenesten, kan det inngående dokumentet inneholde flere årsaker. Den vanligste årsaken til en feil er at systemet ikke kan gjenkjenne linjene på e-dokumentet du fikk fra leverandøren. Derfor kan den ikke angi linjer i kjøpsfakturaen. 

Det er to vanlige feil:  

- Hvis du vil bruke denne bestemte linjen fra leverandørfakturaen som ble bokført direkte på finanskontoen, må du ha konfigurert verdien for **Tilordningstekst** riktig. For å omgå denne feilen hvis du vil bruke finanskonti, velger du **Tildel tekst til konto** for å opprette en bestemt tildelingen av verdien **Tildelingstekst** med verdien **Debetkontonummer** du vil bruke. 
- Hvis du vil spore lagerbeholdningen og bruke linjer fra leverandørfakturaen til å fylle ut varene på dokumentlinjene, må du ha konfigurert **Varereferansenr.** på riktig måte. For å unngå denne feilen, tilordner du det eksterne elementet med varenumrene ved hjelp av varereferanselisten. Se [Bruke varereferanser](inventory-how-use-item-cross-refs.md) for mer informasjon. 

Når du har rettet feilene og advarslene, kan du angi manuelt når systemet skal opprette en kjøpsfaktura basert på oppsettet ditt ved å velge **Opprett dokument**.   

#### <a name="manually-import-invoices"></a>Importere fakturaer manuelt

Hvis du vil importere eksterne e-dokumenter manuelt, følger du denne fremgangsmåten:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **E-dokumenttjeneste**, og velg deretter den relaterte koblingen. 
2. Velg den aktive tjenesten på siden **E-dokumentservice**.   
3. Velg **Motta**, og last opp e-dokumentfilen du fikk fra leverandøren. 
4. Hvis det oppstår en feilmelding, åpner du e-dokumentet for å løse problemene. 
5. Når du er ferdig med å løse problemene, velger du **Opprett dokument** i gruppen **Importer manuelt**.  
6. Når dokumentet er opprettet i [!INCLUDE[prod_short](includes/prod_short.md)], endres ikke måten du viser det på, når du bruker en satsjobb. 

### <a name="e-documents-with-purchase-orders"></a>E-dokumenter med bestillinger

#### <a name="to-link-purchase-orders-with-the-received-e-documents"></a>Slik kobler du bestillinger til mottatte e-dokumenter

Hvis **leverandøren** har konfigurert feltet **Motta e-dokument til** til å fungere med **bestillinger**, gjøres følgende når et elektronisk dokument er opprettet i [!INCLUDE[prod_short](includes/prod_short.md)] (manuelt eller fra et eksternt endepunkt): [!INCLUDE[prod_short](includes/prod_short.md)] gjør følgende:  

1. Hvis **bestillingen** for denne bestemte leverandøren finnes og det finnes et bestillingsnummer i **e-dokumentfilen** for mottak, kobler [!INCLUDE[prod_short](includes/prod_short.md)] automatisk dette **e-dokumentet** til den nevnte **bestillingen**, og **dokumentstatusen** for dette **e-dokumentet** er **Pågår**, og **e-dokumentstatusen** på undersiden **Servicestatus** er **Ordre koblet**. Denne koblingen vil være synlig i **Dokument**-feltet i dette spesifikke **e-dokumentet**. Hvis du må endre **bestillingen** som er koblet automatisk, kan du gjøre det ved hjelp av handlingen **Oppdater bestillingskobling** og velge manuelt en av de eksisterende bestillingene for denne leverandøren. Du kan bare gjøre det før du samsvarer linjene mellom **e-dokument** og **bestilling**.  

2. Hvis **bestillingen** for denne bestemte leverandøren finnes, men det ikke finnes noe bestillingsnummer i den mottatte **e-dokument**-filen, vil [!INCLUDE[prod_short](includes/prod_short.md)] gjøre det mulig å velge en av de eksisterende bestillingene når og hvis du laster opp dette dokumentet manuelt. Dermed åpnes listen **Bestillinger** med bestillinger bare for leverandøren du mottok **e-dokumentet** fra. Du må velge **Bestillingen** du vil ha, og deretter velge **OK**. Hvis du ikke klarte å velge riktig **bBestilling**, eller hentet **E-dokumentet** automatisk fra et eksternt endepunkt ved hjelp av **Jobbkø**, vil ikke et nytt **E-dokument** ikke bli koblet til noe kjøpsdokument. **Dokumentstatus** vil vise **Feil**, og **e-dokument** på delsiden **Tjenestestatus** vil også vise **Feil ved behandling av importert dokument**. Når du skal fullføre tilknytningen til **Bestillingen**, velger du handlingen **Oppdater bestillingskobling** og velger deretter en av de eksisterende bestillingene for denne leverandøren. 

3. Hvis **Bestillingen** for denne bestemte leverandøren ikke eksisterer når et nytt **E-dokument** opprettes, oppretter [!INCLUDE[prod_short](includes/prod_short.md)] en ny **Bestilling** med samme opprettingsmodell som allerede finnes for nye **Kjøpsfakturaer**. **Dokumentstatusen** for dette **e-dokumentet** er **Behandles**, og **e-dokumentstatusen** på undersiden **Tjenestestatus** blir **Importert dokument er opprettet**. Denne koblingen vil være synlig i **Dokument**-feltet i dette spesifikke **e-dokumentet**.   

#### <a name="matching-lines-from-received-e-document-with-purchase-order"></a>Avstemming av linjer fra mottatt e-dokument med bestilling

Du kan avstemme mottatte elektroniske dokumenter med bestillingslinjer fra to forskjellige steder: fra **E-dokument**-siden eller fra **Bestilling**-siden. Den enkleste måten å finne de allerede tilknyttede **bestillingene** på, er å bruke flisen **Koblede bestillinger** som en del av **e-dokumentaktiviteter**. Du finner alle ikke-koblede dokumenter ved hjelp av flisen **Venter på e-fakturaer,** der du har en liste over **e-dokumenter** du må se gjennom.  

> [!NOTE]
> **E-dokumentaktivitetene** med disse to flisene finner du i følgende **rollesentre**: Evaluering av forretningsleder, Forretningsleder, Regnskapsfører, Lagerleder og Levering og mottak.  

> [!NOTE]
> Hvis mva-prosenten er forskjellig mellom det inngående dokumentet og selskapets mva-prosent, kan ikke avstemte dokumenter brukes i et miljø med flere land.  

##### <a name="matching-lines-from-purchase-order"></a>Avstemming av linjer fra bestilling

Du kan avstemme linjene fra **bestillingslisten** eller fra en av de åpnede **bestillingene**. Hvis du vil starte dette, bruker du utføre følgende fremgangsmåte:  

1. Velg flisen **Tilknyttede bestillinger** i rollesenteret hvis det finnes et nummer. 
2. Velg en av de to alternativene for avstemming: 

   - Hvis du vil avstemme linjene fra listen **Bestillinger**, velger du **Bestilling** du vil avstemme, og velger handlingen **Tildel e-dokumentlinjer**.  
   - Hvis du først vil åpne **Bestilling**, åpner du dokumentet og velger deretter handlingen **Tildel e-dokumentlinjer**. 

3. Siden begge alternativene har samme prosess, åpner du **Bestillingssamsvar**-siden med følgende innhold: 

    1. I hodet finner du følgende informasjon som kan hjelpe deg med å tildele linjene enklere: 

       |Feltnavn |Description |
       |--------|-----------------|
       |Leverandørnavn |Angir navnet på leverandøren for det elektroniske dokumentet. |
       |E-dokumentnr. |Angir det tilknyttede elektroniske dokumentnummeret. |
       |E-dokumentdato |Angir datoen for det tilknyttede elektroniske dokumentet.  |
       |E-dokumentbeløp |Angir totalen for det tilknyttede e-dokumentet inkludert mva. |

    2. I linjene finner du linjene som er importert fra **E-dokument**-filen på venstre side og linjene fra den eksisterende **Bestillingen** på høyre side.  
    3. Alle linjene på begge sider har varenumre og beskrivelser, sammen med **Direkte enhetskost** og **Linjerabattprosent**.  
    4. På siden **Importerte linjer** kan du også finne feltet **Antall** som et totalt antall fra e-fakturaen, og feltet **Avstemt antall** som angir antallet som allerede er avstemt med bestillingslinjene. 
    5. På **Bestillingslinjer**-siden finner du også **Disponibelt antall** som antall som kan avstemmes med denne linjen (mottatt, men ikke fakturert antall) og **Ant. som skal fakt.** som angir antallet som allerede er avstemt med denne linjen. 
    6. Hvis du vil avstemme linjer, velger du linjene på begge sider som du vil avstemme, og velger handlingen **Avstem manuelt**. De avstemte linjene merkes med grønt. 
    7. Det er mulig å avstemme én til én, men det er også mulig å avstemme mange til én eller én til mange, ved å velge flere linjer på en eller annen side før du velger handlingen **Avstem manuelt**. 
    8. Du kan også velge handlingen **Avstem automatisk** for automatisk å avstemme alle linjer med samme **Type**, **Nr.**, **Enhetspris**, **Rabatt** og **Enhet**. 
    9. Hvis du gjør en feil, kan du velge handlingen **Fjern avstemming** for å fjerne de avstemte linjene på bestillingssiden, eller velge handlingen **Tilbakestill samsvar** for å tilbakestille alt som er avstemt. 
    10. Hvis **e-dokumentet** har mange linjer, kan du under avstemmingen velge handlingen **Vis ventende linjer** for å fjerne alle e-dokumentlinjene hvis de allerede er avstemt. Hvis du vil se alle linjene, kan du alltid velge handlingen **Vis alle linjer**. 

4. Når du er ferdig med avstemmingen, må du velge handlingen **Bruk på bestilling**.   
5. Når du har brukt avstemmingen på **bestillingen**, oppdaterer [!INCLUDE[prod_short](includes/prod_short.md)] følgende felter:

    1. **Leverandørs fakturanr.** og **Dokumentdato** i dokumenthodet oppdateres med verdier fra det elektroniske dokumentet du har mottatt og koblet. 
    2. **Ant. som skal fakt.** i linjer oppdateres med verdiene fra kolonnen **Ant. som skal fakt.** fra siden **Bestillingssamsvar**, basert på avstemmingen du har gjort. 
    3. Du kan nå bokføre dokumentet ved å velge handlingen **Bokfør**.  
    4. Når du bokfører dokumentet, endres verdien i **Dokument**-feltet på **E-dokument**-siden, og den vil være relatert til den **bokførte kjøpsfakturaen**. 
    5. Lukk siden.  

> [!IMPORTANT]
> Som standard kan du bare avstemme linjene som har samme totalbeløp i begge dokumentene. Dette betyr at **direkte enhetskost** sammen med den utlignede **linjerabattprosenten** må være den samme, siden du i et dokument kan ha et beløp uten rabatt og i et annet dokument med rabatt.  

Hvis du vil legge til litt toleranse og tillate forskjellen mellom linjene i **E-faktura** og **Bestilling**, følger du denne fremgangsmåten:   

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Kjøpsoppsett**, og velg deretter den relaterte koblingen.  
2. Du vil tillate toleranse i feltet **Avstemmingsdifferanse for e-dokument i prosent** og angir den maksimalt tillatte prosenten av kostnadsdifferansen når du avstemmer innkommende **e-dokumentlinje** med **bestillingslinjen**. 
3. Dette oppsettet gjelder for alle avstemte linjer, men igjen vurderes toleranse for totalbeløpet, som for **Direkte enhetskost**, sammen med utlignet **linjerabattprosent**.  
4. Lukk siden.   

##### <a name="matching-lines-from-e-document"></a>Avstemming av linjer fra e-dokument

Du kan avstemme linjene på **E-dokument**-siden. Hvis du vil starte, bruker du utføre følgende fremgangsmåte:  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **E-dokumenter**, og velg deretter den relaterte koblingen. 
2. Velg **e-dokumentet** du vil avstemme.   
3. Velg handlingen **Avstem bestilling** for å åpne siden **Bestillingssamsvar**.  
4. Gjenta dem samme fremgangsmåten som du brukte da du startet avstemming fra bestillinger.

### <a name="e-document-matching-assistance-copilot"></a>Kopiloten Samsvarshjelp for e-dokument

> [!NOTE]
> Kopiloten **Samsvarshjelp for e-dokument** er for øyeblikket i fasen produksjonsklar forhåndsversjon, og den er tilgjengelig globalt bortsett fra i Canada. Den fungerer bare på engelsk. 

> [!NOTE]
> Copilot er assistenten med kunstig intelligens som hjelper personer i hele organisasjonen med å frigjøre kreativiteten og automatisere kjedelige oppgaver. Kopiloten **Samsvarshjelp for e-dokument** hjelper brukere med å enkelt avstemme mottatte elektroniske fakturaer med eksisterende bestillingslinjer, ved hjelp av den store språkmodellen for å avstemme linjer mellom to forskjellige dokumenter. 

#### <a name="to-activate-the-copilot"></a>Slik aktiverer du kopiloten

Hvis du ikke aktiverte kopiloten **Samsvarshjelp for e-dokument**, må du gjøre det manuelt. Følg denne fremgangsmåten for å aktivere kopiloten **Samsvarshjelp for e-dokument**: 

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Copilot og KI-funksjoner**, og velg deretter den relaterte koblingen. 
2. Velg **Samsvarshjelp for e-dokument** i listen over funksjoner, og endre statusen til **Aktiv**.  

Når kopiloten er aktivert, kan du begynne å bruke den.

#### <a name="use-the-e-document-matching-assistance-copilot"></a>Bruk kopiloten Samsvarshjelp for e-dokument

Hvis kopiloten er aktivert, vil eksisterende handlinger **Tildel e-dokumentlinjer** på bestillinger og **Avstem bestilling** på **E-dokument**-siden få forskjellige ikoner, som symboliserer KI-funksjonalitet. Du kan kjøre disse handlingene (det samme som i tidligere eksempler fra listen over bestillinger), fra en av **bestillingene** eller fra **e-dokumentet**. Alle trinn for kjøring er de samme, men når du kjører denne handlingen, blir resultatet annerledes, og du må følge følgende fremgangsmåte:  

1. Velg handlingen **Tildel e-dokumentlinjer** eller **Avstem bestilling** for dokumenter som allerede er koblet.  
2. Legg merke til at **Samsvarshjelp for e-dokument med Copilot**-spørringen fungerer, og du har siden **Bestillingssamsvar** i bakgrunnen. Det betyr at den samme prosessen skjer, men med automatisk støtte fra **Copilot**, som kjører prosessen med avstemming i stedet for deg. 
3. Etter noen sekunder vil **Samsvarshjelp for e-dokument med Copilot** foreslå linjer for avstemming med noen tilleggsdetaljer: 

    1. I spørringshodet finner du følgende informasjon: 

       |Feltnavn |Description |
       |--------|-----------------|
       |Automatisk avstemt | Angir antall avstemminger foreslått automatisk. Dette er basert på en strengsammenligning, og hvis det er 80 % eller mer overlappende beskrivelse, vil systemet avstemme disse beskrivelsene automatisk uten å bruke GPT-funksjoner. |
       |Avstemt med Copilot | Angir antall treff foreslått av kopiloten ved hjelp av både strengsammenligning og semantisk sammenligning. |
       |E-dokumentnr. | Angir det tilknyttede e-dokumentnummeret. |
       |Totalbeløp for faktura ekskl. mva. | Angir det totale fakturabeløpet ekskl. mva. |
       |Avstemt totalbeløp inkl. mva. | Angir det avstemte beløpet inkludert mva. |
    
    2. Hvis alle linjene er avstemt, ser du den grønne teksten øverst til høyre: **Alle linjene (100 %) avstemt. Gå gjennom avstemmingsforslag**.  
    3. I **Avstemt forslag**-linjene finner du følgende informasjon:  

       |Feltnavn |Description |
       |--------|-----------------|
       |E-dokumentlinjenr. | Angir linjenummeret for e-dokumentet (kommer fra den opprinnelige e-dokumentfilen). |
       |Beskrivelse av e-dokumentlinje | Angir beskrivelsen av e-dokumentet (kommer fra den opprinnelige e-dokumentfilen). |
       |Avstemt antall | Angir antallet som skal brukes på bestillingslinjen. |
       |Tilbud | Angir handlingen som er foreslått av kunstig intelligens, og disse foreslåtte handlingene er knyttet til avstemming av bestillingslinjene. |

    4. Alle fullstendig foreslåtte og avstemte linjer er merket med grønn farge. Hvis det er et problem, det vil si en annen pris, men i den tillatte prisklassen, vil denne linjen være merket som gul, og hvis det er likhet mellom beskrivelsesfeltene, men prisforskjellen er større enn tillatt, vil denne linjen bli merket som rød. 
    5. Hvis du ikke er fornøyd med noen forslag, kan du slette dem ved hjelp av handlingen **Slett linje**.  
    6. Hvis du vil se forslagssamsvar, kan du velge koblingen i **Forslag**-kolonnen for å åpne siden **Samsvarsdetaljer for e-dokument**. 
    7. På siden **Samsvarsdetaljer for e-dokument** kan du sammenligne detaljer fra **e-dokumentet** og **bestillingen** for å være sikker på det foreslåtte samsvaret før du bekrefter det. 
    8. Lukk siden etter gjennomgang.   

4. Hvis du ikke er fornøyd med de fleste forslagene, eller hvis du ikke vil bruke funksjonen **Ordrelinjer for e-dokumentavstemminger med Copilot**, velger du **Forkast det**, og du kan fortsette med den manuelle avstemmingen som forklart tidligere.  
5. Hvis du vil beholde forslag, velger du **Behold det**-knappen, så lagrer systemet alle forslag fra **Copilot**.  
6. [!INCLUDE[prod_short](includes/prod_short.md)] lukker Copilot-meldingen, og linjene på siden **Bestillingssamsvar** merkes som grønne, siden de allerede samsvarer. 
7. Nå kan du fortsette å arbeide mens du utfører manuelt samsvar. Det betyr at du kan fjerne treff, samsvare manuelt eller tilbakestille samsvar. Hvis du ikke vil gjøre endringer, velger du bare handlingen **Bruk på bestilling** og fortsetter å arbeide med **bestillingen**. 

> [!NOTE]
> Du kan velge handlingen **Avstem med Copilot** på siden **Bestillingssamsvar** på nytt, men i dette tilfellet blir du spurt om du vil overskrive de eksisterende avstemmingene, siden alle linjene allerede er avstemt.  

> [!NOTE]
> Pris-/kostanalyse, og kontrollen for tilgjengelig antall er en del av forhåndsbehandlingsaktiviteten.   

## <a name="overview-of-e-document-statuses"></a>Oversikt over e-dokumentstatuser

Hvis du vil ha en bedre oversikt over alle e-dokumenter i selskapet, kan du velge rollesenteret **Regnskapsfører** der det finnes e-dokumentstatuser. Der kan du finne e-dokumentaktiviteter som har følgende statuser:

- **Innkommende e-dokumenter:**

    - Behandlet
    - Pågår
    - Feil


## <a name="see-also"></a>Se også

[Konfigurere e-dokumenter](finance-how-setup-edocuments.md)    
[Bruk e-dokument i salgsprosessen](finance-how-use-edocuments.md)   
[Utvid funksjonaliteten for e-dokumenter](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments)    
[Økonomistyring](finance.md)    
[Fakturer salg](sales-how-invoice-sales.md)    
[Registrere kjøp med kjøpsfakturaer og ordrer](purchasing-how-record-purchases.md)    
[Arbeid med Business Central](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]

