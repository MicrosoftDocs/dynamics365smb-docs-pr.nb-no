---
title: Bærekraftskontoplan og finans
description: 'Finn ut hvordan du administrerer bærekraftskontoplan, kategorier og underkategorier og detaljer om bærekraftsposter.'
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD, CoA, Chart, Account, Ledger'
ms.search.form: '6210, 6213, 6214, 6220'
ms.date: 04/02/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# <a name="chart-of-sustainability-accounts-and-ledger"></a>Bærekraftskontoplan og finans

## <a name="chart-of-sustainability-accounts"></a>Bærekraftskontoplan

**Bærekraftskontoplanen** danner den grunnleggende strukturerte listen som brukes til å registrere alle utslippsdata. Den fungerer som et rammeverk som kategoriserer og organiserer bærekraftskontoer basert på attributter, for eksempel område eller andre grupperinger. Hver konto er vanligvis tildelt en unik kode eller et nummer for enkel referanse og sporing, etter samme struktur som en tradisjonell **kontoplan**, men tilpasset spesielt for overvåking av bærekraftrelaterte data og beregninger i en organisasjon. 
 
Brukere kan legge til **kontokategorier** og **underkategorier** for å definere hvordan systemet oppfører seg, ved å velge dedikerte utslipp for sporing, utslippsfaktorer, formler og lignende konfigurasjoner.  

>[!NOTE]
>Hvis du vil bli kjent med områdene, basert på standardene for klimagass, er det tre utslippsområder:  
>- **Utslipp i område 1**: inkluderer utslipp som slippes ut fra stasjonær og mobil forbrenning samt fra utilsiktede flyktige utslipp. 
>- **Utslipp i område 2**: inkluderer indirekte utslipp fra produksjonen av energi som kjøpes fra strømleverandører. 
>- **Utslipp i område 3**: inkluderer et bredt spekter av utslipp, fra kjøpte varer og tjenester og kapitalvarer, brensel- og energirelaterte aktiviteter, oppstrøms og nedstrøms transport, generert avfall, forretningsreiser og pendling for ansatte osv. 

Fra **bærekraftskontoplanen** kan du gjøre ting som:  

-   Vise rapporter som viser bærekraftsposter og saldoer. 
-   Åpne **bærekraftskontokortet** for å legge til eller endre innstillinger.  
-   Se kategorien og underkategorien for den aktuelle kontoen.   
-   Vis separate saldoer for hvert av utslippene for én konto. 
-   Legg til en eller flere **dimensjoner** i hver av kontoene, og angi dimensjonsfilter. 
    
Du kan legge til, endre eller slette **bærekraftskontoer**. Hvis du vil unngå avvik kan du imidlertid ikke slette en **bærekraftkonto** hvis det er en eller flere poster knyttet til denne kontoen.  

### <a name="add-or-change-accounts"></a>Legg til eller endre kontoer

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 3.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Bærekraftskontoplan** og velg deretter den relaterte koblingen. 
2. På siden **Bærekraftskontoplan** kan du åpne **bærekraftskontoen** og legge til eller endre innstillinger. Hold markøren over et felt for å lese en kort beskrivelse. 

Når det gjelder konti av typen **Total** må du fylle ut feltet **Sammentelling**. På konti av typen **Til-sum**, fylles dette feltet ut automatisk av funksjonen Innrykking. Når du har definert alle kontoene, velger du handlingen **Innrykk bærekraftskontoplan** for å gjøre det.  

>[!IMPORTANT]
>Hvis du har angitt definisjoner i feltet **Sammentelling** for konti av typen **Til-sum** før du utfører innrykkingen, må du skrive dem inn på nytt fordi funksjonen overskriver verdiene i alle **Til-sum**-feltene.  

### <a name="delete-accounts"></a>Slett kontoer

Du kan slette en **bærekraftskonto**. Før du sletter den, må du imidlertid være sikker på at det er en eller flere poster knyttet til denne kontoen, siden Business Central vil hindre deg i å slette en **bærekraftskonto** i denne situasjonen.  

## <a name="account-categories"></a>Kontokategorier

Brukere må legge til **bærekraftskontokategorien** i hver av **bærekraftskontoene** for å definere hvordan systemet oppfører seg, velge utslippsområde, dedikerte utslipp for sporing, formler og lignende konfigurasjoner.  

Hvis du vil se gjennom **bærekraftskontokategorier**, følger du denne fremgangsmåten: 

1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 3.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Bærekraftskontokategorier** og velg deretter den relaterte koblingen. 
2.  På siden **Bærekraftskontokategorier** kan du redigere den eksisterende listen eller opprette en ny kategori. Hvis du vil opprette en ny kategori, velger du handlingen **Opprett**.  
3.  Fyll ut feltene **Kode** og **Beskrivelse**.   
4.  Definer feltet **Utslippsområde** og velg et av områdealternativene .  
5.  Velg gassutslippene du vil spore. For øyeblikket kan du bruke et av alternativene: **CO2**, **CH4** eller **N2O**. Du kan velge hvilken som helst kombinasjon du vil spore, men du må ha minst ett utslipp for sporing.  
6.  I feltet **Beregningsgrunnlag** kan du velge en hvilken som helst formel du vil bruke, i tilfelle du ikke vet den nøyaktige utslippsmengden. Her kan du angi beregningsgrunnlaget (formelen) for utslippsberegningen. Du kan velge et av følgende alternativer: **Brensel/elektrisitet**, **Avstand**, **Installasjon** eller **Egendefinert**. 
7.  Hvis du velger **egendefinert** formel, kan du konfigurere egendefinert beskrivelse i feltet **Egendefinert verdi**.  

>[!NOTE]
>Hvis dette settet med tilbudte formler i **Beregningsgrunnlag**-feltet ikke er nok, kan du utvide dette feltet og legge til flere beregninger i systemet som skal brukes i **bærekraftkladdene**.  

Hvis du bruker **beregningsgrunnlaget** (formler), er det en forklaring, hvordan systemet vil beregne basert på alternativet du har valgt (**EF** er **utslippsfaktoren** som du kan konfigurere på siden **Underkategori for bærekraftskonto**): 

|  Utslippstype  |  Beregningsgrunnlag  |  Formel         | Merknad      |
|------------|--------------|------------------------------|---------------------------------|
| **OMRÅDE 1**  |
| Stasjonær forbrenning | Drivstoff/elektrisitet | Utslipp = Drivstoff * EF | _dvs. drivstoff = mengde drivstoff brukt til kjeler, varmeovner, termiske oksidasjonsmidler ..._ |
| Mobil forbrenning | Drivstoff/elektrisitet | Utslipp = Drivstoff * EF | _dvs. drivstoff = mengde drivstoff brukt for kjøretøy på vei eller utenfor vei, jernbane ..._ |
|  |  |  Utslipp = Avstand * EF | _dvs. avstand = kjørelengde for kjøretøy på vei eller utenfor vei, jernbane ..._ |
| Flyktige utslipp | Installasjon | Utslipp = Installasjonsmultiplikator * Egendefinert mengde / 100 * Tidsfaktor | _dvs. egendefinert mengde = monteringstap, årlig lekkasjerate ..._ |
| **OMRÅDE 2**  |
| Kraftleverandører | Drivstoff/elektrisitet | Utslipp = elektrisitet * EF | _dvs. drivstoff/elektrisitet = elektrisitetsmengde, dampmengde, varmeenhet ..._ |
|  | Egendefinert | Utslipp = egendefinert mengde * EF | _dvs. egendefinert beløp = termisk enhet, tonntime..._ |
| **OMRÅDE 3**  |
| Kjøpte varer og tjenester, og kapitalvarer | Egendefinert | Utslipp = egendefinert mengde * EF | _dvs. egendefinert mengde = kostnad (finans) ..._ |
| Oppstrøms transport og distribusjon | Avstand | Utslipp = Avstand * EF |  |
|  | Avstand | Utslipp = Avstand * Multiplikator * EF | _Multiplikator = Tonn last_ |
| Nedstrøms transport og distribusjon | Avstand | Utslipp = Avstand * EF |  |
|  | Avstand | Utslipp = Avstand * Multiplikator * EF | _Multiplikator = Tonn last_ |
| Avfall generert i drift og sluttbehandling av solgte produkter | Egendefinert | Utslipp = egendefinert mengde * EF | _dvs. egendefinert mengde = avfall_ |
| Forretningsreiser og pendling for ansatte | Avstand | Utslipp = Avstand * EF | _dvs. avstand = kjørelengde av brukt firmabil, leiebil, tog, fly ..._ |
|  | Egendefinert | Utslipp = egendefinert mengde * EF | _dvs. egendefinert beløp = hotellopphold ..._ |
|  | Drivstoff/elektrisitet | Utslipp = Drivstoff * EF | _dvs. drivstoff = Mengde drivstoff brukt i firmabilen, leiebil ..._ |

## <a name="account-subcategories"></a>Kontounderkategori

Brukerne må legge til **underkategorien for bærekraftskonto** i hver av **bærekraftskontoene** for å definere utslippsfaktorer som skal brukes i formlene, men den er basert på valget for utslippssporing i **Bærekraftskontokategori**.  

Hvis du vil se gjennom **Underkategorier for bærekraftskonto**, følger du denne fremgangsmåten:  

1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 3.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Underkategorier for bærekraftskonto** og velg deretter den relaterte koblingen. 
2.  På siden **Underkategorier for bærekraftskonto** kan du redigere den eksisterende listen eller opprette en ny kategori. Hvis du vil opprette en ny kategori, velger du handlingen **Opprett**.  
3.  Fyll ut feltene **Kode** og **Beskrivelse**.   
4.  Basert på gassutslippene du vil spore i **bærekraftskontokategorien** og koble denne underkategorien til, kan du også fylle ut en eller flere utslippsfaktorer: 

   - **Utslippsfaktor CO2** – Angir utslippsfaktoren for CO2-utslipp.  
   - **Utslippsfaktor CH4** – Angir utslippsfaktoren for CH4-utslipp. 
   - **Utslippsfaktor N2O** – Angir utslippsfaktoren for N2O-utslipp.  

5.  Hvis denne underkategorien er relatert til fornybar energi, velger du feltet **Fornybar energi**.   

>[!NOTE]
>Feltene **Importer data** og **Importer fra** er ment for potensiell integrering med eksterne systemer som brukes til å samle inn utslippsfaktorer, men i **lanseringsbølge 1 i 2024** kan de ikke brukes som en funksjon som standard.  

## <a name="sustainability-ledger-entries"></a>Bærekraftsposter

**Bærekraftspost** lagrer historikken til alle bokførte bærekraftstransaksjoner, og organiserer alle utslippsdata i henhold til **bærekraftskontoplanen**. Når en bruker bokfører **bærekraftskladden**, blir alle viktige data registrert der. Alle aktive rapporter genereres basert på **bærekraftspostene**.   

Brukeren kan åpne denne posten for én bestemt konto ved hjelp av handlingen **Poster** fra siden **Bærekraftskontoplan**, eller for å åpne alle postene, velge ikonet ![Lyspære som åpner funksjonen Fortell meg 3.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skrive inn **Bærekraftsposter** og velge den relaterte koblingen. Hold markøren over et felt for å lese en kort beskrivelse.  

>[!IMPORTANT]
>Når du har bokført dataene dine i bærekraftsposten, kan du ikke slette dem. Hvis du har gjort en feil, kan du bokføre den tilbakeførte transaksjonen med de samme detaljene, men ved å bruke negativt fortegn for beløp.  

## <a name="see-also"></a>Se også
[Finans](finance.md)    
[Oversikt over bærekraftsbehandling](finance-manage-sustainability.md)
[Bærekraftsoppsett](finance-sustainability-setup.md)
[Slik registrerer du utslipp](finance-sustainability-journal.md)
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
