---
title: Registrer bærekraftsposter
description: Finn ut hvordan du registrerer klimagassutslipp.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Sustainability, ESG, emission, GHG, CSRD, journal'
ms.search.form: '6216, 6219, 6220'
ms.date: 05/07/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="record-sustainability-entries"></a>Registrer bærekraftsposter

Den eneste måten å registrere klimagassutslipp i bærekraftsposten på for øyeblikket er å bruke bærekraftskladder.

## <a name="sustainability-journals"></a>Bærekraftskladder

Bærekraftskladder er utformet for å spore og registrere bærekraftrelaterte aktiviteter ved hjelp av samme brukeropplevelse som andre kladder i Business Central. Brukere som har den nødvendige informasjonen, kan legge inn utslipp i en kladd manuelt. Hvis de mangler informasjonen, kan de bruke innebygde formler til å beregne utslipp nøyaktig basert på spesifikke kjente parametere som svarer til ulike typer kilder og kontoer.

Informasjonen du angir i en kladd, er midlertidig og kan endres mens den fortsatt er i denne kladden. Når du bokfører kladden, overføres informasjonen til bærekraftsposter på individuelle bærekraftskontoer, der de ikke kan endres. Du kan imidlertid bokføre tilbakeførings- eller korrigeringsposter.

### <a name="use-journal-templates-and-batches"></a>Bruk kladder og kladdemaler

Det finnes som standard to bærekraftkladdemaler: standardmalen og den gjentakende malen.

Du kan definere dine egne personlige kladder som en kladd for hver enkelt kladdemal. Du gjør dette ved å velge **Kladder**-handlingen på siden **Bærekraftskladdemaler** og deretter opprette den nye **bærekraftskladden** på den nye siden. Du kan for eksempel definere din egen kladd for hvert utslippsområde ved hjelp av alternativet **Utslippsområde** og deretter velge blant tre eksisterende områder. Du kan legge til eller endre verdiene for **Kildekode** og **Årsakskode** for hver kladd.

> [!TIP]
> Hvis du har mange linjer, kan du bidra til å redusere risikoen for feil ved å ha en kladd for hver utslippstype. Du kan alternativt bruke felleskladden for alle utslippstyper.

### <a name="validate-sustainability-journals"></a>Valider bærekraftskladder

Du kan aktivere en bakgrunnskontroll på siden **Bærekraftsoppsett** for å forhindre bokføringsforsinkelser. Hvis det oppstår feil mens du arbeider med bærekraftskladden, varsler valideringen deg og forhindrer deg fra å bokføre kladden.

Når du aktiverer valideringen, viser faktaboksen **Kladdkontroll** feil på nåværende linje og i hele kladden. Valideringen forekommer når du laster inn en kladd, og når du velger en annen kladdelinje. Flisen **Totalt antall problemer** i faktaboksen viser totalt antall problemer som [!INCLUDE [prod_short](includes/prod_short.md)] har funnet. Du kan velge flisen for å åpne en oversikt over problemene.

### <a name="work-with-sustainability-journals"></a>Arbeid med bærekraftskladder

Følg denne fremgangsmåten for å begynne å arbeide med bærekraftskladder:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 3.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Bærekraftskladd**, og velg deretter den relaterte koblingen.
2. På siden **Bærekraftkladd** angir du så mange linjer som du har tenkt å bokføre i samme kladd.
3. Du kan la **Bilagstype**-feltet stå tomt, eller du kan velge **Faktura** eller **Kreditnota**.
4. I feltet **Kontonr.** kan du bare velge ikke-blokkerte bærekraftskontoer der feltet **Direkte bokføring** er valgt og **Bokføring** er angitt i feltet **Regnskapstype**. Kontoene må også konfigureres med en kategori og en underkategori.

    > [!NOTE]
    > Hvis du bruker en kladd der utslippsområdet er konfigurert, må verdien for **Utslippsområde** i bærekraftskontoen være lik verdien for **Utslippsområde** i kladden.

5. Du kan enten bokføre mengdene manuelt eller bruke formler.

    - Hvis du har nøyaktig informasjon om utslippet og vil bokføre det (det vil si hvis du har informasjonen på den mottatte fakturaen), velger du feltet **Manuelle inndata** for å angi at du registrerer mengdene manuelt. I dette tilfellet kan du ikke angi dataene direkte i feltene **Drivstoff/elektrisitet**, **Avstand**, **Egendefinert mengde**, **Installasjonsmultiplikator** og **Tidsfaktor**, fordi de ikke kan redigeres. Du kan imidlertid redigere feltene **Utslipp CO2**, **Utslipp CH4** og **Utslipp N2O**, og du kan angi dataene dine direkte i dem.
    - Hvis du ikke har nøyaktig kunnskap om utslippet og må beregne det, må du la være å velge feltet **Manuelle inndata**. Feltene **Utslipp CO2**, **Utslipp CH4** og **Utslipp N2O** kan i dette tilfellet ikke redigeres. Du kan imidlertid angi beregningsdetaljer basert på formelen du bruker. Finn ut mer om formlene som er brukt og definert i **bærekraftskontokategorien**, i [Bærekraftskontoplan og finans](finance-sustainability-accounts-ledger.md#account-categories).

6. Velg **Bokfør**-handlingen for å bokføre kladden. Når du bokfører i en bærekraftskladd, genereres poster i bærekraftsposten.

Hvis formelen er basert på alternativet **Beregn fra økonomimodul** i bærekraftskontokategorien, må du bruke handlingen **Samle inn beløp fra finansposter** før du bokfører kladden, for å beregne utslipp basert på denne datakilden. Hvis du har gjort endringer i utslippsfaktorene etter at du fylte ut kladdelinjene, må du i tillegg velge handlingen **Beregn på nytt** for å få riktig beløp i kladden.

### <a name="recurring-journals"></a>Gjentakelseskladder

En gjentakelseskladd er en bærekraftskladd som har spesifikke felter for håndtering av transaksjoner du bokfører ofte, med få eller ingen endringer. Eksempler omfatter bærekraftstransaksjoner som elektrisitet eller varme eller andre lignende transaksjoner. Du kan bruke gjentakelseskladder til å bokføre faste og variable beløp.

Når du bruker en gjentakelseskladd, trenger du bare å opprette poster du bokfører regelmessig, én gang. Informasjon som kontoer, dimensjoner og dimensjonsverdier forblir i kladden etter bokføring. Du kan foreta eventuelle nødvendige endringer hver gang du bokfører.

Feltet **Gjentakelsesprinsipp** er viktig. Det angir hvordan beløpet på kladdelinjen håndteres etter bokføring. Hvis du for eksempel bruker samme beløp hver gang du bokfører linjen, kan du velge alternativet **F Fast** for å beholde beløpet etter bokføring. Hvis du vil bruke de samme kontoene og samme tekst på linjen, men at beløpet varierer hver gang du bokfører, kan du velge alternativet **V Variabel** for å slette beløpet etter bokføring.

Feltet **Gjentakelsesintervall** er også viktig og må angis. Det er et datoformelfelt som angir hvor ofte posten på kladdelinjen skal bokføres. Finn ut mer i [Bruk datoformler](ui-enter-date-ranges.md#use-date-formulas).

Feltet **Utløpsdato** angir datoen når linjen skal bokføres for siste gang. Linjen tas ikke med i bokføringen etter denne datoen. Fordelen med å bruke feltet **Utløpsdato** er at linjen ikke slettes fra kladden med en gang. Du kan angi en senere dato slik at du kan bruke linjen i fremtiden. Hvis feltet er tomt, bokføres linjen hver gang du bokfører, helt til den slettes fra kladden.

## <a name="see-also"></a>Se også

[Finans](finance.md)  
[Oversikt over bærekraftsadministrasjon](finance-manage-sustainability.md)  
[Bærekraftsoppsett](finance-sustainability-setup.md)  
[Bærekraftskontoplan og finans](finance-sustainability-accounts-ledger.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
