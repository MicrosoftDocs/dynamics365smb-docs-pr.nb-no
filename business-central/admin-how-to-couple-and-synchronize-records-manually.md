---
title: Kobling og synkronisering (inneholder video)
description: Synkronisering av en integrert tabelltilordning gjør det mulig å synkronisere data i alle poster i en tabell i Business Central og Dynamics 365 Sales-tabell som er koblet.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.date: 03/31/2023
ms.custom: bap-template
ms.search.keywords: 'crm, sales, couple, decouple, synchronize'
ms.search.form: '6250,'
---

# Koble og synkroniser poster mellom Dataverse og Business Central

Dette emnet beskriver hvordan du kobler sammen én eller flere poster i [!INCLUDE[prod_short](includes/prod_short.md)] med poster i Dataverse eller [!INCLUDE[crm_md](includes/crm_md.md)]. Kobling av poster lar deg vise Dataverse-informasjon fra [!INCLUDE[prod_short](includes/prod_short.md)], og omvendt. Kopling lar deg også synkronisere data mellom postene. Du kan koble eksisterende poster, eller du kan opprette og koble nye poster.

> [!NOTE]
> Kobling og synkronisering av data er bare tilgjengelig hvis systemansvarlig har opprettet en kobling mellom [!INCLUDE[prod_short](includes/prod_short.md)] og Dataverse eller [!INCLUDE[crm_md](includes/crm_md.md)]. En rask måte å kontrollere på, er å åpne **Kunde**-kortet og se etter handlingen **Konfigurer kobling**. Hvis handlingen er tilgjengelig, er appene koblet.

## Videoeksempel

Denne videoen viser koblings- og synkroniseringsdata i konteksten til en integrering med [!INCLUDE[crm_md](includes/crm_md.md)].

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098376]

## Koble en post  

1. I [!INCLUDE[prod_short](includes/prod_short.md)] åpner du kortet for posten du vil koble. For eksempel kunde- eller kontaktkortet.  

    Du kan også bare åpne listesiden og velge posten du vil koble.  

2. Velg handlingen **Konfigurer kobling**.  
3. Fyll ut feltene, og klikk deretter **OK**.  

## Synkronisere en enkeltoppføring  

1. I [!INCLUDE[prod_short](includes/prod_short.md)] åpner du kortet for posten du vil koble. For eksempel kunde- eller kontaktkortet.  
2. Velg **Synkroniser nå**-handlingen.  
3. Hvis en post kan synkroniseres i én retning, velger du alternativet som angir retningen for dataoppdatering, og deretter velger du **OK**.  

## Slik synkroniserer du en enkeltoppføring fra [!INCLUDE[crm_md](includes/crm_md.md)]  

1. I [!INCLUDE[crm_md](includes/crm_md.md)] åpner du skjemaet for posten du vil koble. Det kan for eksempel være skjema for kontokort eller kontaktkort.  
2. Velg **[!INCLUDE[prod_short](includes/prod_short.md)]-** handlingen på båndet for å åpne og koble til posten automatisk.

    > [!Note]
    > Du kan synkronisere én post fra [!INCLUDE[crm_md](includes/crm_md.md)] automatisk bare når det ikke er merket av for **Synkroniser bare koblede poster** og synkroniseringsretningen er satt til **Toveis** eller **Fra integreringstabell** på siden **Tildeling for integreringstabell for posten**. Hvis du vil ha mer informasjon, kan du se [Tilordne tabellene og feltene som skal synkroniseres](admin-how-to-modify-table-mappings-for-synchronization.md#create-new-records).

## Slik lagrer du flere poster ved å bruke samsvarsbasert kobling

Angi hvilke data som skal synkroniseres for en enhet, for eksempel en kunde eller kontakt, ved å koble poster basert på samsvar. Begrens samsvarene ved å skille mellom store og små bokstaver og angi en prioritet for hvert samsvar. Hvis det ikke finnes noen samsvar, kan du også angi om du vil opprette enheten i Dataverse. Gå til [Tilpass samsvarsbasert kobling](admin-how-to-set-up-a-dynamics-crm-connection.md#customize-the-match-based-coupling) hvis du vil ha mer informasjon.  

> [!NOTE]
> Prosessen for den treffbaserte koblingen hopper over poster som allerede er tilordnet. Hvis du vil ta med disse postene når du kjører treffbasert kobling, kobler du fra postene og prøver på nytt. Hvis du vil lære mer om frakobling av poster, går du til [Koble fra poster](#uncoupling-records).

1. I [!INCLUDE[prod_short](includes/prod_short.md)] åpner du listesiden for posten, for eksempel listesiden for kunder eller kontakter.
2. Velg handlingen **Samsvarsbasert kobling**.
3. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## Synkronisere flere poster  

1. I [!INCLUDE[prod_short](includes/prod_short.md)] åpner du listesiden for posten, for eksempel sidene for kunder eller kontakter.  
2. Velg postene som skal synkroniseres, og velg deretter **Synkroniser nå**-handlingen.  
3. Hvis poster kan synkroniseres i én retning, velger du alternativet som angir retningen, og deretter velger du **OK**.  

## Masseinnsett og koble poster

Hvis du har et stort antall Dataverse-enheter som tilsvarer poster i [!INCLUDE [prod_short](includes/prod_short.md)], kan du sette inn og koble dem i bulk. Det kan for eksempel hende at du vil sette inn og koble poster når du skal konfigurere synkronisering for første gang.

Du bruker **veiviseren for dataimport** i **Microsoft Power Platform-administrasjonssenteret**.

Følgende eksempel beskriver hvordan du masseinnsetter og kobler kunder med kontoer i Dataverse. Bruk samme fremgangsmåte for andre typer enheter, for eksempel leverandører, varer og ressurser.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Kunder** og velger den relaterte koblingen.
2. Velg handlingen **Åpne i Excel** for å åpne kundedata i Excel. <!--Don't they need to choose the customers that they want to import to Dataverse?-->
3. Hvis du vil tildele og importere data til **Konto**-enheten i Dataverse, følger du fremgangsmåten som er beskrevet i [Import data (alle oppføringstyper) fra flere kilder](/power-platform/admin/import-data-all-record-types).  

    Hvis Konto-enheten har en **bcbi_companyid**-kolonne når du tildeler datakolonnene, kontrollerer du at importen tildeler den riktige selskaps-ID-en i kolonnen for hver importerte post. Gjør følgende for å finne selskaps-ID-en i [!INCLUDE [prod_short](includes/prod_short.md)]:

    1. Åpne siden **Tildelinger for integreringstabell**.
    2. Velg **KUNDE**-tildelingen, og velg handlingen **Rediger liste**.
    3. Rull til høyre, og velg redigeringsprogramknappen :::image type="icon" source="media/assist-edit-icon.png" border="false"::: i feltet **Integreringstabellfilter**. Dette viser standardfilteret for kundetildeling, og det inneholder selskaps-ID-en. Selskaps-ID-en er den første delen av verdien. Kopier bare denne delen, og se bort fra nullene. Eksemplet nedenfor merker delen som skal kopieres.

    :::image type="content" source="media/dataverse-company-id-guid.png" alt-text="Viser delen av selskaps-ID-en som skal kopieres.":::

    > [!NOTE]
    > Ikke alle navn på Dataverse-enheter og Business Central-poster samsvarer. Avhengig av hva du skal importere, bør du dobbeltsjekke at følgende kolonner har følgende verdier etter import:
    >
    >* For kunder skal **CustomerTypeCode**-kolonnen inneholde **Kunde**.
    >* For leverandører skal **CustomerTypeCode**-kolonnen inneholde **Leverandører**. 
    >* For varer skal **ProductTypeCode**-kolonnen inneholde **Salgsbeholdning**.
    >* For ressurser skal **ProductTypeCode**-kolonnen inneholde **Service**.
 
4. Når du har importert data til Dataverse-miljøet, i [!INCLUDE [prod_short](includes/prod_short.md)] følger du trinnene [Slik kobler du flere poster ved å bruke treffbasert kobling](#to-couple-multiple-records-using-match-based-coupling) for å koble Dataverse-enhetene med [!INCLUDE [prod_short](includes/prod_short.md)]-poster. 

## Oppheve kobling av poster

Du kan slette én eller flere poster fra listesider eller siden **Feil ved synkronisering av koblede data** ved å velge én eller flere linjer og velge **Slett kobling**. Du kan også fjerne alle koblingene for én eller flere tabelltilordninger på siden **Tilordninger for integreringstabell**.

## Se også  

[Bruk Dynamics 365 Sales fra Business Central](marketing-integrate-dynamicscrm.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]