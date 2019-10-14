---
title: Opprette kontaktselskaper | Microsoft-dokumentasjon
ddescription: Outlines the tasks to create contact companies, including assigning relevant data about prospects and defining the business relationships you have with companies.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: f4bf8e694a7b034eb601c3bf39bd420ff61ab73a
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2019
ms.locfileid: "2309319"
---
# <a name="create-contacts"></a>Opprette kontakter
Du møter regelmessig personer fra andre selskaper som kan utvikle seg til forretningsforhold, for eksempel en kunderelasjon. Når du får en ny kontakt, må så mye informasjon som mulig registreres på et kontaktkort, slik at kommunikasjonen kan opprettholdes.

Du kan opprette kontakten som typen **Selskap**, for eksempel, hvis relasjonen ikke er en person, men en enhet, for eksempel en entreprenør eller en bank. Du kan også opprette kontakten som typen **Person**. Funksjonaliteten er mer eller mindre den samme for begge typer, og begge kan endres etter hvert som forholdet utvikles.

Når et kontaktkort for eksempel konverteres til et kundekort, blir kontaktpersonen eller kontaktselskapet navnet på kunden. Kontaktkortet beholdes, og data på de to kortene synkroniseres fremover når du kobler dem sammen.

## <a name="person-or-company"></a>Person eller selskap
Du kan opprette en kontakt som en person eller et selskap, vanligvis avhengig av om du vil vite navnet på kontaktpersonen ved oppretting. Du gjør dette når du fyller ut feltet **Type** på **Kontaktkort**-siden. Du kan også vedlikeholde kontaktkort for både et selskap og én eller flere personer som jobber i selskapet. Dette skjer automatisk når du fyller ut feltet **Selskapsnavn** på et kontaktkort av typen **Person**.

Funksjonaliteten er den samme for begge typer, bortsett fra at alternativene for tilleggsinformasjon endres avhengig av typen. Du kan for eksempel bare tilordne ansvarsområder til en person og bransjegruppe til et selskap. Dette angis i grensesnittet ved å grå ut feltene og handlingene som ikke gjelder. Du kan endre verdien for **Type**-feltet senere, eller du kan bruke feltene på **Arv**-hurtigfanen på **Markedsføringsoppsett**-siden til å styre hvilke data som deles mellom en person og personens relaterte selskap. Hvis du vil ha mer informasjon, kan du se [Konfigurere kontakter](marketing-setup-contacts.md).

## <a name="to-create-a-contact-manually"></a>Slik oppretter du en kontakt manuelt
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Kontakter**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Ny**.
3. I **Nr.** -feltet angir du et nummer på kontakten.

    Hvis du har definert en nummerserie for kontakter på siden **Markedsføringsoppsett**, kan du eventuelt trykke Enter-tasten for å sette inn det neste tilgjengelige kontaktnummeret.  
5. Fyll ut feltene som gjenstår, etter behov. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-create-a-contact-from-a-customer-vendor-or-bank-account"></a>Slik oppretter du en kontakt fra en kunde, leverandør eller bankkonto
Hvis du har kunder, leverandører og bankkonti du vil opprette kontaktkort for, kan du bruke de satsvise jobbene **Opprett kontakter fra** til å opprette kontakter på grunnlag av de eksisterende dataene. Når du oppretter en kontakt på denne måten, synkroniseres kontaktinformasjonen etterpå med relatert informasjon om kunden, leverandøren eller bankkontoen. Hvis du vil ha mer informasjon, kan du se [Synkronisere kontaktene med kunder, leverandører og bankkonti](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-and-bank-accounts).

> [!NOTE]  
> Før du kan opprette kontakter basert på eksisterende data, må du angi en kode for forretningsforbindelse for kunder, leverandører eller bankkonti på **Samhandlinger**-hurtigfanen på siden **Markedsføringsoppsett**. Hvis du vil ha mer informasjon, kan du se [Definere kontakter](marketing-setup-contacts.md).

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi ett av følgende, alt etter hva du vil opprette kontakter fra, og velg deretter den relaterte koblingen.
   * **Opprett kontakter fra kunder**
   * **Opprett kontakter fra leverandører**
   * **Opprett kontakter fra bankkonti**
2. Hvis du bare vil opprette kontakter fra bestemte kunder, leverandører eller bankkonti, definerer du filtre i inndelingen **Kunde**, **Leverandør** eller **Bankkonto** på forespørselssiden som åpnes.
3. Velg **OK** for å starte oppretting av kontrakter.

De neste kontaktnumrene i nummerserien tilordnes de nye kontaktene. Forretningsforbindelsene som er angitt på siden **Markedsføringsoppsett**, tilordnes til nyopprettede kontakter.

> [!TIP]  
> Du kan også gjøre dette på motsatt måte, ved å opprette en kunde, leverandør eller bankkonto fra en kontakt. Hvis du vil ha mer informasjon, kan du se [Slik oppretter du en kontakt som en kunde, leverandør eller bankkonto](marketing-create-contact-companies.md#to-create-a-customer-vendor-or-bank-account-from-a-contact).

## <a name="to-create-a-customer-vendor-or-bank-account-from-a-contact"></a>Opprette en kunde, leverandør eller bankkonto fra en kontakt
Hvis du har en kunde, leverandør eller bankkonto for selskapet som du vil opprette en kontakt for, kan du bruke **Opprett som**-funksjonen. Når du oppretter en kontakt på denne måten, synkroniseres kontaktinformasjonen etterpå med relatert informasjon om kunden, leverandøren eller bankkontoen. Hvis du vil ha mer informasjon, kan du se [Synkronisere kontaktene med kunder, leverandører og bankkonti](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-and-bank-accounts).

> [!NOTE]  
> Før du kan opprette kunder, leverandører eller bankkontoer fra kontakter, må du angi en kode for forretningsforbindelse for kunder, leverandører eller bankkonti på **Samhandlinger**-hurtigfanen på siden **Markedsføringsoppsett**. Hvis du vil ha mer informasjon, kan du se [Konfigurere kontakter](marketing-setup-contacts.md).

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kontakter**, og velg deretter den relaterte koblingen.
2. Velg kontakten du vil opprette som en kunde, leverandør eller bankkonto.
3. Velg handlingen **Opprett som**, og velg deretter **Kunde**, **Leverandør** eller **Bank**.
4. Velg **OK**.

Kontaktinformasjonen overføres fra kontaktkortet til et nytt kunde-, leverandør- eller bankkontokort. Noen ganger kan det være nødvendig å legge til spesifikke opplysninger på hvert kort, for eksempel fakturerings- og betalingsopplysninger. Hvis du vil ha mer informasjon, kan du for eksempel se [Registrere nye kunder](sales-how-register-new-customers.md).

## <a name="to-link-a-contact-to-an-existing-customer-vendor-or-bank-account"></a>Slik knytter du en kontakt til en eksisterende kunde, leverandør eller bankkonto
Hvis du har en kontakt og enten en kunde, leverandør eller konto for samme selskap, kan du knytte de to enhetene, slik at vanlige data synkroniseres.

1. Åpne kontakten du vil tilknytte.
2. Velg handlingen **Knytt til eksisterende**, og velg deretter handlingen **Kunde**, **Leverandør** eller **Bank**.
3. Velg kunde, leverandør eller bankkonto å tilknytte på siden som åpnes.
4. I feltet **Gjeldende hovedfelt** angir hvem sine felt som skal prioriteres hvis det er motstridende opplysninger i felt som er felles for kontakten og kunden, leverandøren eller kontoen. Hvis for eksempel selgerkodene er forskjellige på kontaktkortet og kundekortet, kan du velge å beholde det på kontaktkortet ved å velge **Kontakt**.
5. Velg **OK**-knappen.

## <a name="synchronizing-contacts-with-customers-vendors-and-bank-accounts"></a>Synkronisere kontakter med kunder, leverandører og bankkonti
Hvis en del av kontaktene også er kunder, leverandører eller bankkonti, kan du synkronisere kontaktinformasjonen med relatert kunde, leverandør eller bankkonto.

Følgende fordeler finnes når en kontakt synkroniseres med en kunde, leverandør eller bankkonto.

* Du trenger du bare å oppdatere opplysninger på ett sted. Hvis du for eksempel endrer telefonnummeret på kontakten, blir telefonnummeret automatisk oppdatert med de samme endringene på kunden, leverandøren eller bankkontoen.
* Hvis du har angitt en nummerserie for kontakter, opprettes det automatisk et kontaktkort for kunden, leverandøren eller bankkontoen når du oppretter et kundekort, leverandørkort eller bankkontokort.
* Du kan du opprette tilbud og ordrer og forespørsler og bestillinger fra kontakten.
* Du kan angi at samhandlinger registreres når du utfører handlinger, for eksempel når du skriver ut ordrer, rammeordrer, oppretter serviceordrer, sender e-post og så videre.
* Hvis du sletter en kontakt som er koblet til en kunde, leverandør eller bankkonto, er det bare kontakten som fjernes. Kunden, leverandøren eller bankkontoen beholdes.
* Hvis du sletter en kunde, leverandør eller bankkonto som er koblet til en kontakt, beholdes kontakten.

> [!NOTE]  
> Noen detaljer, for eksempel fakturerings- og bokføringsopplysninger, vises ikke på kontaktkortet. Du vil derfor kanskje legge dem til manuelt på kundekortet, leverandørkortet eller bankkontokortet når du oppretter kontakter som kunder, leverandører eller bankkonti.

Synkronisering av vanlige data mellom kontakter og de relaterte kundene, leverandørene eller bankkontiene aktiveres på tre måter:

* Når du oppretter kontakter fra kunder, leverandører eller bankkonti. Se [Slik oppretter du en kontakt fra en kunde, leverandør eller bankkonto](marketing-create-contact-companies.md#to-create-a-contact-from-a-customer-vendor-or-bank-account).
* Når du oppretter kunder, leverandører eller bankkonti fra kontakter. Se [Opprette en kunde, leverandør eller bankkonto fra en kontakt](marketing-create-contact-companies.md#to-create-a-customer-vendor-or-bank-account-from-a-contact).
* Når du knytter kontakter til eksisterende kunder, leverandører eller bankkonti fra kontaktkortet. Se [Slik knytter du en kontakt til en eksisterende kunde, leverandør eller bankkonto](marketing-create-contact-companies.md#to-link-a-contact-to-an-existing-customer-vendor-or-bank-account).

## <a name="to-view-which-customer-vendor-or-bank-account-a-contact-is-related-to"></a>Slik viser du hvilken kunde, leverandør eller bankkonto en kontakt er relatert til
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Kontakter**, og velg deretter den relaterte koblingen.
2. Velg linjen for en kontakt, valg handlingen **Relatert informasjon**, og velg deretter **Kunde-/leverandør-/bankkonto**.

Siden for det relaterte kortet åpnes.

## <a name="see-also"></a>Se også
[Administrere kontakter](marketing-contacts.md)  
[Konfigurere kontakter](marketing-setup-contacts.md)  
[Arbeide med Business Central](ui-work-product.md)
