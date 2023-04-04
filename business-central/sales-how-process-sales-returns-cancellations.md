---
title: Behandle ordrereturer eller annulleringer
description: 'Beskriver hvordan du oppretter en salgskreditnota for å behandle en retur, kansellering eller refusjon for varer eller tjenester du har mottatt betaling for.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'undo, credit memo, return'
ms.search.form: '44, 134, 143, 6629, 6630, 6633, 6662, 9302, 9304, Report_6646'
ms.date: 09/27/2021
ms.author: edupont
---
# Behandle ordrereturer eller annulleringer

Hvis en kunde vil returnere varer eller bli refundert for varer eller tjenester du har solgt og mottatt betaling for, må du opprette og bokføre en salgskreditnota som angir den ønskede endringen. Hvis du vil ta med de riktige salgsfakturaopplysningene, kan du gjøre følgende:  

- Opprett salgskreditnotaen direkte fra den bokførte salgsfakturaen.
- Opprett en ny salgskreditnota med kopiert fakturainformasjon.

Hvis du trenger mer kontroll over ordrereturprosessen, for eksempel lagerdokumenter for varehåndtering eller bedre oversikt når du mottar varer fra flere salgsdokumenter med en ordreretur, kan du opprette ordrereturer. En ordreretur utsteder automatisk den relaterte salgskreditnotaen, og andre returrelaterte dokumenter, for eksempel en erstatningsordre om nødvendig. Hvis du vil ha mer informasjon, kan du se [Behandle ordrereturer](sales-how-process-sales-returns-orders.md).

> [!NOTE]  
> Hvis en bokført salgsfaktura ennå ikke er betalt, kan du bruke funksjonen **Korriger** eller **Annuller** på den bokførte salgsfakturaen for å tilbakeføre transaksjonene. Disse funksjonene fungerer bare for ubetalte fakturaer, og de støtter ikke delvise returer eller annulleringer. Hvis du vil ha mer informasjon, kan du se [Korrigere eller annullere ubetalte salgsfakturaer](sales-how-correct-cancel-sales-invoice.md).

En returnert vare eller refusjon kan være knyttet til bare noen av varene eller tjenestene på den opprinnelige salgsfakturaen. I så fall må du redigere opplysningene på linjene på salgskreditnotaen eller ordrereturen. Når du bokfører salgskreditnotaen eller ordrereturen, tilbakeføres salgsdokumentene som påvirkes av endringen og en refusjonsbetaling kan opprettes for kunden. Hvis du vil ha mer informasjon, kan du se [Utføre betalinger](payables-make-payments.md).  

Bokføringen av kreditnotaen tilbakefører også eventuelle varegebyr som var tilordnet det bokførte dokumentet, slik at varens verdiposter er de samme som før varegebyret ble tilordnet.

> [!NOTE]
> Bokføringsaspekter ved ordrereturer, for eksempel betaling til kunder som refusjoner, anses som bokføringsarbeid og er ikke beskrevet her. Hvis du vil ha mer informasjon, kan du se [Administrere skyldige beløp](payables-manage-payables.md).

## Opprette en ny salgskreditnota fra en bokført salgsfaktura  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Bokførte salgsfakturaer**, og velg deretter den relaterte koblingen.  
2. På siden **Bokførte salgsfakturaer** velger du den bokførte salgsfakturaen som du vil tilbakeføre, velg handlingen **Avbryt** og deretter velger du **Opprett korrigerende kreditnota**.

    For salgskreditnotahodet inneholder noen opplysninger fra den bokførte salgsfakturaen. Du kan redigere dette, for eksempel med ny informasjon som gjenspeiler returavtalen.  
3. Redigere informasjonen på linjene i henhold til avtalen, for eksempel antall varer som returneres, eller beløpet som skal refunderes.
4. Velg handlingen **Klargjør**, og velg deretter handlingen **Utlign poster**.
5. På siden **Utlign kundeposter** velger du linjen med det bokførte salgsdokumentet du vil utligne salgskreditnotaen mot, og deretter velger du handlingen **Utlignings-ID**.

    ID-en på salgskreditnotaen vises i feltet **Utlignings-ID**.
6. I feltet **Beløp som skal utlignes** skriver du inn beløpet som du vil utligne hvis mindre enn det opprinnelige beløpet.  

    Nederst på siden **Utlign kundeposter** kan du se det totale beløpet som skal utlignes for å tilbakeføre alle involverte poster, nemlig når verdien i **Saldo**-feltet er null.
7. Velg **OK**. Når du bokfører salgskreditnotaen, brukes den på de bokførte salgsdokumentene.

    Når du har opprettet eller redigert salgskreditnotalinjene, og ett eller flere programmer er angitt, kan du fortsette med å bokføre salgskreditnotaen.  
8. Velg handlingen **Bokføring**, og velg deretter handlingen **Bokfør og send**.  

Dialogboksen **Bokfør og send bekreftelse** åpnes, og viser den foretrukne sendemetoden for kunden. Du kan endre sendemetoden ved å velge oppslagsknappen for feltet **Send dokument til**. Hvis du vil ha mer informasjon, kan du se [Definere en profil for dokumentsending](sales-how-setup-document-send-profiles.md).  

De bokførte salgsdokumentene som du utlignet kreditnotaen mot, tilbakeføres, og en refusjonsbetaling kan opprettes for kunden. Salgskreditnotaen fjernes og erstattes med et nytt dokument i listen over bokførte salgskreditnotaer.

## Opprette en salgskreditnota ved å kopiere en bokført salgsfaktura

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Salgskreditnotaer**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Ny** for å åpne en ny, tom salgskreditnota.
3. I feltet **Kundenavn** angir du navnet på en eksisterende kunde.
4. Velg handlingen **Klargjør**, og velg deretter handlingen **Kopier dokument**.
5. Velg **Bokført faktura** i **Bilagstype**-feltet på siden **Kopier salgsdokument**.
6. Velg feltet **Bilagsnr.** for å åpne siden **Bokførte salgsfakturaer**, og velg deretter den bokførte salgsfakturaposten som inneholder linjer du vil tilbakeføre.
7. Merk av for  **Gjenberegn linjer**  hvis du vil at de kopierte bokførte salgsfakturalinjene skal oppdateres med endringer i varepris og enhetskost etter at fakturaen er bokført.
8. Velg **OK**. De kopierte fakturalinjene settes inn i salgskreditnotaen.
9. Fullfør salgskreditnotaen som forklart i [Opprette en salgskreditnota fra en bokført salgsfaktura](sales-how-process-sales-returns-cancellations.md#to-create-a-sales-credit-memo-from-a-posted-sales-invoice).

## Slik oppretter du en salgsrabatt
Du kan sende en kunde en kreditnota med prisreduksjon hvis kunden har mottatt ukurante varer eller har mottatt varene for sent.  
Du kan bokføre den reduserte prisen som et varegebyr i en kreditnota eller en ordreretur, og knytte den til den bokførte følgeseddelen. Det følgende beskriver den for en salgskreditnota, men de samme trinnene gjelder en ordreretur.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Salgskreditnotaer**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Ny** for å åpne en ny, tom salgskreditnota.
3. Fyll ut kreditnotahodet med aktuelle opplysninger om kunden du vil gi salgsrabatt til.  
4. På hurtigfanen **Linjer**, i **Type**-feltet, velger du **Gebyr (vare)**.  
5. I feltet **Nr.** -feltet velger du den aktuelle varegebyrverdien.  
     Det kan hende du vil opprette et eget varegebyrnummer for å dekke salgsrabatter.  
6. I feltet **Antall** angir du **1**.  
7. I feltet **Salgspris eks. mva** angir du beløpet i salgsrabatten.  
8. Du kan  tilordne salgsrabatten som et varegebyr til varene i den bokførte leveringen. Hvis du vil ha mer informasjon, kan du se [Bruke varegebyr til å gjøre rede for ekstra handelskostnader](payables-how-assign-item-charges.md). Når du har tilordnet rabatten, går du tilbake til **Salgskreditnota**-siden.  

Når du bokfører ordrereturen, legges salgsrabatten til i det aktuelle salgsbeløpet. Dermed kan du opprettholde en nøyaktig lagerverdisetting.

## Slå sammen retursedler
Du kan slå sammen retursedler hvis kunden returnerer flere varer som dekkes av ulike ordrereturer.  

Når du mottar varene på lageret, bokfører du de aktuelle ordrereturene som mottatt. Dette oppretter bokførte returmottak.  

Når du er klar til å fakturere denne kunden, kan du i stedet for å fakturere hver enkelt ordreretur separat, opprette en salgskreditnota og automatisk kopiere de bokførte returmottakslinjene til dette dokumentet. Deretter kan du bokføre salgskreditnotaen, og helt enkelt fakturere alle åpne ordrereturer samtidig.  

Du kombinerer retursedler ved å merke av for **Opprett samlefaktura** på siden **Kundekort**.  

### Slik slår du sammen retursedler manuelt  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Salgskreditnotaer**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**.
3. Fyll ut feltene i hurtigfanen **Generelt** etter behov.  
4. Velg handlingen **Hent returmottakslinjer**.  
5. Velg returmottakslinjene du vil ta med i kreditnotaen:  

    - Du setter inn alle linjene ved å merke dem og velge **OK**.  

    - Du setter inn bestemte linjer ved å merke dem og velge **OK**.  
6.  Hvis du valgte en feil følgeseddellinje, eller du vil starte på nytt, kan du ganske enkelt slette linjene på kreditnotaen og kjøre funksjonen **Hent returseddellinjer** på nytt.  
7.  Bokfør fakturaen.  

### Slik slår du sammen retursedler automatisk:

Du kan slå sammen retursedler automatisk og velge å bokføre kreditnotaene automatisk ved hjelp av funksjonen **Slå sammen retursedler**.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Slå sammen retursedler**, og velg deretter den relaterte koblingen.
2. På siden **Slå sammen retursedler** fyller du ut feltene for å velge de aktuelle returmottakene.
3. Merk av for **Bokfør kreditnotaer**. Hvis ikke må du manuelt bokføre de endelige kjøpskreditnotaene.
4. Velg **OK**.  

### Slik fjerner du mottatte og fakturerte ordrereturer

Når du fakturerer retursedler på denne måten, eksisterer fortsatt ordrereturene som retursedlene ble bokført fra, selv om de er fullstendig mottatt og fakturert.  

Når retursedler slås sammen på en kreditnota og bokføres, opprettes en bokført salgskreditnota for den eller de krediterte linjene. **Fakturert (antall)**-feltet på den opprinnelige ordrereturen oppdateres ut fra det fakturerte antallet.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Slett fakturerte ordrereturer**, og velg deretter den relaterte koblingen.  
2. Angi hvilke ordrer som skal slettes, i **Nr.** -filterfeltet.  
3. Velg **OK**-knappen.  

Du kan også slette individuelle ordrereturer manuelt.  

## Beholdning og kostberegning

For å beholde riktig lagerverdi vil du vanligvis sette returnerte varene tilbake i lageret med enhetskosten som de er solgt på, ikke på gjeldende enhetskost. Dette kalles opprinnelig kostpris.

Det finnes to funksjoner du kan bruke til å tilordne opprinnelig kosttilbakeføring automatisk:  

|Funksjon|Beskrivelse|  
|------------------|---------------------------------------|  
|Funksjonen **Hent bokførte dokumentlinjer som skal tilbakeføres** på siden **Ordreretur**|Kopierer linjer i en eller flere bokførte dokumenter som skal tilbakeføres til ordrereturen. Hvis du vil ha mer informasjon, kan du se [Opprett en ordreretur basert på et eller flere bokførte salgsdokumenter](sales-how-process-sales-returns-orders.md#create-a-sales-return-order-based-on-one-or-more-posted-sales-documents).|  
|**Kopier dokument**-funksjonen på sidene **Salgskreditnota** og **Ordreretur**|Kopierer både hodet og linjene i et bokført bilag som skal tilbakeføres.<br /><br /> Krever at du merker av for **Bruk opprinnelig kostpris** på siden **Salgsoppsett**.|

For å tilordne opprinnelig kostpris manuelt, må du velge feltet **Utlignet fra-varepost** på alle typer returdokumentlinjer, og deretter velge nummeret på den opprinnelige salgsposten. Dermed knyttes salgskreditnotaen eller ordrereturen til den opprinnelige salgsposten, og verdien av varen fastsettes til opprinnelig enhetskost.

Hvis du vil ha mer informasjon, kan du se [Kostberegning for beholdning](design-details-inventory-costing.md).

## Se relatert [Microsoft-opplæring](/training/paths/return-items-dynamics-365-business-central/)

## Se også

[Salg](sales-manage-sales.md)  
[Sette opp salg](sales-setup-sales.md)  
[Administrere skyldige beløp](payables-manage-payables.md)  
[Send dokumenter i e-post](ui-how-send-documents-email.md)  
[Behandle bestillingsreturer eller annulleringer](purchasing-how-process-purchase-returns-cancellations.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
