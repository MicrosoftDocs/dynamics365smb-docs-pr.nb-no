---
title: Slik registrerer du bærekraftsposter
description: Finn ut hvordan du registrerer klimagassutslipp.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD, journal'
ms.search.form: '6216, 6219, 6220'
ms.date: 04/02/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# Slik registrerer du bærekraftsposter  

I dette øyeblikket er den eneste måten å registrere klimagassutslipp til **bærekraftsposten** på å bruke **bærekreaftskladdene**.   

## Bærekraftskladd  

**Bærekraftskladder** er utformet for å spore og registrere bærekraftrelaterte aktiviteter ved hjelp av samme brukeropplevelse som andre kladder i Business Central. I kladden har brukerne muligheten til å legge inn utslipp manuelt hvis de har den nødvendige informasjonen. Alternativt, hvis de mangler disse dataene, kan de bruke innebygde formler for å nøyaktig beregne utslipp basert på spesifikke kjente parametere som tilsvarer ulike typer kilder og kontoer. 

Opplysningene du angir i en kladd, er midlertidige og kan endres mens de fortsatt befinner seg i kladden. Når du bokfører kladden, overføres opplysningene til **bærekraftsposter** i individuelle **bærekraftskontoer**, der de ikke kan endres. Du kan imidlertid bokføre tilbakeførings- eller korrigeringsposter.  

### Bruk kladder og kladdemaler 

Det finnes to **bærekraftkladdemaler** som standard, standard og gjentakende. Du kan definere dine egne personlige kladder som en kladd for hver enkelt kladdemal. Dette gjør du ved å velge handlingen **Kladder** på siden **Bærekraftkladdemaler** og opprette den nye **bærekraftskladden** på den nye siden. Du kan for eksempel definere din egen kladd for hvert utslippsområde ved hjelp av alternativet **Utslippsområde**, der du kan velge mellom tre eksisterende områder. Du kan også legge til eller endre **kildekoden** og **årsakskoden** for hver av kladdene. 

>[!TIP]
>Du kan ha en kladd for hver utslippstype hvis du har mange linjer, da det kan redusere sjansen for å gjøre feil, men du kan også bruke felles kladd for alle typer utslipp.   

### Validering av bærekraftskladder 

Du kan aktivere en bakgrunnskontroll på siden **Bærekraftsoppsett** som bidrar til å forhindre forsinkelser ved bokføring. Sjekken gir deg beskjed når det er en feil mens du arbeider i **bærekraftskladden**, og dette hindrer deg i å bokføre kladden.  

Når du aktiverer valideringen, viser faktaboksen **Kladdkontroll** feil i nåværende linje og i hele kladden. Valideringen skjer når du laster inn en kladd, og når du velger en annen kladdelinje. Flisen **Totalt antall problemer** i faktaboksen viser totalt antall problemer som [!INCLUDE [prod_short](includes/prod_short.md)] har funnet, og du kan velge den for å åpne en oversikt over problemene. 

### Arbeid med bærekraftskladder 

Følg fremgangsmåten for å begynne å jobbe med **bærekraftskladdene**:   

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 3.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Bærekraftskladd**, og velg deretter den relaterte koblingen. 
2. På siden **Bærekraftkladd** kan du angi så mange linjer som du planlegger å bokføre med samme kladd.  
3. Som **dokumenttype** kan du beholde det tomme alternativet, eller du kan velge å bruke **faktura** eller **kreditnota**.  
4. I feltet **Kontonr.** kan du bare velge **Bærekraftskontoer** med valgt **Direkte bokføring**-felt, **Bokføring** som **regnskapstype** og ikke-sperret konto. Kontoer må også ha konfigurert med kategori og underkategori.  

>[!NOTE]
>Hvis du bruker partiet der utslippsområdet er konfigurert, må **utslippsområdet** i **bærekraftskontoen** være lik **utslippsområdet** i den brukte kladden.  

5. Du har to alternativer: enten bokføre mengdene manuelt eller bruke formler.   

    1. Hvis du har nøyaktig informasjon om utslippet, du vil bokføre det (dvs. ha det på den mottatte fakturaen), må du velge feltet **Manuelle inndata** for å angi at mengdene skal legges inn manuelt. I dette tilfellet kan du ikke fylle ut dataene i feltene **Brensel/elektrisitet**, **Avstand**, **Egendefinert mengde**, **Installasjonsmultiplikator** og **Tidsfaktor**, siden de ikke kan redigeres for dette valget. Men feltene **Utslipp CO2**, **Utslipp CH4** og **Utslipp N2O** kan redigeres, og du kan fylle ut dataene dine direkte der. 
    2. Hvis du ikke vet utslippet ditt nøyaktig, må du beregne det, og du må ikke ha valgt feltet **Manuelle inndata**, og i dette tilfellet vil feltene **Utslipp CO2**, **Utslipp CH4** og **Utslipp N2O** ikke kunne redigeres, men du kan angi beregningsdetaljene basert på formelen du bruker. Du finner mer om formlene som er brukt og definert i **bærekraftskontokategorien** her i [Bærekraftskontoplan og finans](finance-sustainability-accounts-ledger.md#account-categories).
    
7. Velg handlingen **Bokfør** for å bokføre kladden. Når du bokfører i en **bærekraftskladd**, genereres poster i **bærekraftsposten**. 

Hvis formelen er basert på alternativet **Beregn fra finans** i **Bærekraftskontokategori**, må du bruke handlingen **Samle inn beløp fra finansposter** før du bokfører kladden til å beregne utslipp basert på denne datakilden. Hvis du har gjort noen endringer i utslippsfaktorene etter at du fylte ut kladdelinjene, må du også velge handlingen **Beregn på nytt** for å få riktig beløp i kladden.  

### Gjentakelseskladder 

En gjentakende kladd er en **bærekraftskladd** med spesifikke felter for håndtering av transaksjoner du bokfører ofte, med få eller ingen endringer. Eksempel: bærekraftstransaksjoner som elektrisitet, varme eller andre lignende transaksjoner. Ved hjelp av gjentakelseskladder kan du bokføre faste og variable beløp. Når kladden er en gjentakende kladd, oppretter du poster som skal bokføres jevnlig, én gang. Kontoer, dimensjoner og dimensjonsverdier og så videre blir for eksempel liggende i kladden etter bokføring. Hvis det trengs endringer, kan du gjøre det hver gang du bokfører. 

Feltet **Gjentakelsesprinsipp** er viktig. Det angir hvordan beløpet på kladdelinjen skal behandles etter bokføring. Hvis du for eksempel bruker samme beløp hver gang du bokfører linjen, kan du la beløpet stå, og i dette tilfellet bør du bruke **F Fast** som et alternativ. Hvis du vil bruke samme konto og tekst på linjen, men at beløpet vil variere hver gang du bokfører, kan du velge å slette beløpet etter bokføring, og i dette tilfellet velger du alternativet **V Variabel**. 

Du må også konfigurere feltet **Gjentakelsesintervall**, siden dette datoformelfeltet bestemmer hvor ofte posten skal bokføres på kladdelinjen, og det må fylles ut. Finn ut mer under [Bruk datoformler](ui-enter-date-ranges.md#use-date-formulas).  

Feltet **Utløpsdato** angir når linjen skal bokføres for siste gang. Linjen tas ikke med i bokføringen etter denne datoen. Fordelen med å bruke feltet **Utløpsdato** er at linjen ikke slettes fra kladden med en gang. Du kan angi en senere dato slik at du kan bruke linjen i fremtiden. Hvis feltet er tomt, bokføres linjen hver gang du bokfører, helt til den slettes fra kladden.  

## Se også  
[Finans](finance.md)    
[Oversikt over bærekraftsbehandling](finance-manage-sustainability.md)   
[Bærekraftsoppsett](finance-sustainability-setup.md)   
[Bærekraftskontoplan og finans](finance-sustainability-accounts-ledger.md)   
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)   

[!INCLUDE[footer-include](includes/footer-banner.md)]
