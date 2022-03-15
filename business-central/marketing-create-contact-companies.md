---
title: Opprett forretningskontakter
description: Her finner du en disposisjon over oppgavene der du oppretter kontakter og definerer forretningsrelasjoner på kontaktkortet.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 07/08/2021
ms.author: edupont
ms.openlocfilehash: 7f25c192c43823c1f3594f21097fe7bd7081f889
ms.sourcegitcommit: 5a02f8527faecdffcc54f9c5c70cefe8c4b3b3f4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/04/2022
ms.locfileid: "8383562"
---
# <a name="create-contacts"></a>Opprette kontakter

Når du utvikler en forretningsforbindelse til noen i et annet selskap, legger du dem til som en kontakt i [!INCLUDE[prod_short](includes/prod_short.md)]. Deretter legger du til informasjon om dem, eller selskapet, som kan være nyttig for fremtidig kommunikasjon. På siden **Kontaktkort** kan du opprette følgende kontakttyper:

* **Person** – Vanligvis når du har hatt direkte kontakt med noen, og har kontaktopplysningene deres.
* **Selskap** – For eksempel hvis kontakten ikke er en enkeltperson, men en enhet, for eksempel en entreprenør eller en bank. 

Informasjonen som er relevant for hver type kontakt, er forskjellig, så feltene og handlingene som er tilgjengelige, er ulike. Du kan for eksempel bare tilordne ansvarsområder til en person og en bransjegruppe til et selskap. 

Du kan endre verdien i feltet **Type** senere. Du kan også bruke feltene på hurtigfanen **Arv** på siden **Markedsføringsoppsett** til å angi hvilke data som skal deles mellom en person og selskapet deres. Hvis du vil ha mer informasjon, kan du se [Konfigurere kontakter](marketing-setup-contacts.md).

Når en kontakt for eksempel konverteres til en kunde, blir kontaktpersonen eller kontaktselskapet navnet på kunden. Posten for kontakten beholdes, og du kan koble kontakten og kunden slik at dataene synkroniseres fremover.

> [!NOTE]
> Hvis du aktiverer [funksjonsoppdateringen for konverteringsmaler](/dynamics365-release-plan/2020wave2/smb/dynamics365-business-central/use-conversion-templates-convert-contacts-vendors-employees), kan du også opprette leverandører eller ansatte fra forretningskontakter.
>
> Hvis du allerede bruker den innebygde funksjonaliteten til å opprette kunder eller varer automatisk, støtter imidlertid ikke denne funksjonsoppdateringen egendefinerte felter, og nylig opprettede kunder eller varer vil ikke inneholde slike data.

## <a name="to-create-a-contact-manually"></a>Slik oppretter du en kontakt manuelt
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Kontakter**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Ny**.
3. I **Nr.** -feltet angir du et nummer på kontakten.

    Hvis du har definert en nummerserie for kontakter på siden **Markedsføringsoppsett**, kan du eventuelt trykke **Enter** for å sette inn det neste tilgjengelige kontaktnummeret.  
5. Fyll ut feltene som gjenstår, etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-create-a-contact-from-a-customer-vendor-or-bank-account"></a>Slik oppretter du en kontakt fra en kunde, leverandør eller bankkonto
Hvis du har kunder, leverandører og bankkonti du vil opprette kontaktkort for, kan du bruke de satsvise jobbene **Opprett kontakter fra** til å opprette kontakter fra de eksisterende dataene. Når du oppretter en kontakt på denne måten, synkroniseres kontaktinformasjonen etterpå med relatert informasjon om kunden, leverandøren eller bankkontoen. Hvis du vil ha mer informasjon, kan du se [Synkronisere kontaktene med kunder, leverandører og bankkonti](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-employees-and-bank-accounts).

> [!NOTE]  
> Før du kan opprette kontakter basert på eksisterende data, må du angi en kode for forretningsforbindelse for kunder, leverandører eller bankkonti på **Samhandlinger**-hurtigfanen på siden **Markedsføringsoppsett**. Hvis du vil ha mer informasjon, kan du se [Definere kontakter](marketing-setup-contacts.md).

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn ett av følgende, avhengig av hvor du vil opprette kontakter fra, og velg deretter den relaterte koblingen.
   * **Opprett kontakter fra kunder**
   * **Opprett kontakter fra leverandører**
   * **Opprett kontakter fra bankkonti**
2. Hvis du bare vil opprette kontakter fra bestemte kunder, leverandører eller bankkonti, definerer du filtre i inndelingen **Kunde**, **Leverandør** eller **Bankkonto** på forespørselssiden som åpnes.
3. Velg **OK** for å starte oppretting av kontrakter.

De neste kontaktnumrene i nummerserien tilordnes de nye kontaktene. Forretningsforbindelsene som er angitt på siden **Markedsføringsoppsett**, tilordnes til nyopprettede kontakter.

> [!TIP]  
> Du kan også gjøre dette på motsatt måte, ved å opprette en kunde, leverandør eller bankkonto fra en kontakt. Hvis du vil ha mer informasjon, kan du se [Slik oppretter du en kontakt som en kunde, leverandør eller bankkonto](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).

## <a name="to-create-a-customer-vendor-employee-or-bank-account-from-a-contact"></a>Opprette en kunde, leverandør, ansatt eller bankkonto fra en kontakt
Hvis du har en kunde, leverandør, ansatt eller bankkonto for selskapet som du vil opprette en kontakt for, kan du bruke handlingen **Opprett som**. Når du oppretter en kontakt på denne måten, synkroniseres kontaktinformasjonen etterpå med relatert informasjon om kunden, leverandøren, den ansatte eller bankkontoen. Hvis du vil ha mer informasjon, kan du se [Synkronisere kontaktene med kunder, leverandører og bankkonti](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-employees-and-bank-accounts).

> [!NOTE]  
> Før du kan opprette kunder, leverandører, ansatte eller bankkontoer fra kontakter, må du angi en kode for forretningsforbindelse på siden **Markedsføringsoppsett** på **Samhandlinger**-hurtigfanen. Hvis du vil ha mer informasjon, kan du se [Konfigurere kontakter](marketing-setup-contacts.md).

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Kontakter**, og velg deretter den relaterte koblingen.
2. Velg kontakten du vil opprette som en kunde, leverandør, ansatt eller bankkonto.
3. Velg handlingen **Opprett som**, og velg deretter **Kunde**, **Leverandør**, **Bank** eller **Ansatt**.
4. Velg **OK**-knappen.

Kontaktinformasjonen overføres fra kontaktkortet til et nytt kunde-, leverandør-, ansatt- eller bankkontokort. Noen ganger kan det være nødvendig å legge til spesifikke opplysninger på hvert kort, for eksempel fakturerings- og betalingsopplysninger. Hvis du vil ha mer informasjon, kan du for eksempel se [Registrere nye kunder](sales-how-register-new-customers.md).

## <a name="to-link-a-contact-to-an-existing-customer-vendor-employee-or-bank-account"></a>Slik knytter du en kontakt til en eksisterende kunde, leverandør, ansatt eller bankkonto
Hvis du har en kontakt og enten en kunde, leverandør, ansatt eller bankkonto for samme selskap, kan du knytte de to enhetene, slik at data synkroniseres.

1. Åpne kontakten du vil tilknytte.
2. Velg handlingen **Knytt til eksisterende**, og velg deretter handlingen **Kunde**, **Leverandør**, **Bank** eller **Ansatt**.
3. Velg kunde, leverandør, ansatt eller bankkonto å tilknytte på siden som åpnes.
4. I feltet **Gjeldende hovedfelt** angir hvem sine felt som skal prioriteres hvis det er motstridende opplysninger i felt som er felles for kontakten og kunden, leverandøren, den ansatte eller bankkontoen. Hvis for eksempel selgerkodene er forskjellige for kontakten og kunden, kan du velge å beholde det på kontaktkortet ved å velge **Kontakt**.
5. Velg **OK**-knappen.

## <a name="to-remove-a-link-between-a-contact-and-an-existing-customer-vendor-employee-or-bank-account"></a>Slik fjerner du en kobling mellom en kontakt og en eksisterende kunde, leverandør, ansatt eller bankkonto

Hvis du feilaktig har knyttet en kontakt til en kunde, leverandør, ansatt eller bankkonto, fjerner du koblingen mellom enhetene slik at data ikke lenger synkroniseres.

1. Åpne kontakten som har feil kobling.  
2. Velg handling **Forretningsforbindelser**.  
3. Velg kunde, leverandør, ansatt eller bankkonto som du vil fjerne kobling fra, på siden som åpnes.  
4. Velg handlingen **Slett**.  

> [!NOTE]  
> Du må ikke bruke vinduet **Forretningsforbindelser** når du skal endre eksisterende relasjoner. Du må i stedet fjerne relasjonen og bruke handlingen **Koble med eksisterende**. Hvis du vil ha mer informasjon, kan du se [Slik knytter du en kontakt til en eksisterende kunde, leverandør eller bankkonto](marketing-create-contact-companies.md#to-link-a-contact-to-an-existing-customer-vendor-employee-or-bank-account).

## <a name="synchronizing-contacts-with-customers-vendors-employees-and-bank-accounts"></a>Synkronisere kontakter med kunder, leverandører, ansatte og bankkonti
Hvis en del av kontaktene også er kunder, leverandører, ansatte eller bankkonti, kan du synkronisere dem med data fra kontakten og få følgende fordeler:

* Du trenger du bare å oppdatere opplysninger på ett sted. Hvis du for eksempel endrer telefonnummeret på kontakten, blir telefonnummeret automatisk oppdatert for kunden, leverandøren, den ansatte eller bankkontoen.
* Hvis du har angitt en nummerserie for kontakter, opprettes det automatisk en kontakt når du oppretter et kunde-, leverandør-, ansatt- eller bankkontokort.
* Du kan du opprette tilbud og ordrer og forespørsler og bestillinger fra kontakten.
* Du kan registrere samhandlingene, for eksempel når du skriver ut ordrer, rammeordrer, oppretter serviceordrer, sender e-post og så videre.
* Hvis du sletter en kontakt som er koblet til en kunde, leverandør, ansatt eller bankkonto, er det bare kontakten som fjernes. Kunden, leverandøren, den ansatte eller bankkontoen beholdes.
* Hvis du sletter en kunde, leverandør, ansatt eller bankkonto som er koblet til en kontakt, beholdes kontakten.

> [!NOTE]  
> Noen detaljer, for eksempel fakturerings- og bokføringsopplysninger, er ikke tilgjengelige for kontakter. Når du oppretter kontakter som kunder, leverandører, ansatte eller bankkonti, vil du kanskje legge dem til manuelt.

Det er tre måter du kan aktivere datasynkronisering på mellom kontakter og kunder, leverandører, ansatte eller bankkonti:

* Når du oppretter kontakter fra kunder, leverandører, ansatte eller bankkonti. Se [Slik oppretter du en kontakt fra en kunde, leverandør eller bankkonto](marketing-create-contact-companies.md#to-create-a-contact-from-a-customer-vendor-or-bank-account).
* Når du oppretter kunder, leverandører, ansatte eller bankkonti fra kontakter. Se [Opprette en kunde, leverandør eller bankkonto fra en kontakt](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).
* Når du knytter kontakter til eksisterende kunder, leverandører, ansatte eller bankkonti fra kontaktkortet. Se [Slik knytter du en kontakt til en eksisterende kunde, leverandør eller bankkonto](marketing-create-contact-companies.md#to-link-a-contact-to-an-existing-customer-vendor-employee-or-bank-account).

## <a name="to-view-which-customer-vendor-employee-or-bank-account-a-contact-is-related-to"></a>Slik viser du hvilken kunde, leverandør, ansatt eller bankkonto en kontakt er relatert til
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Kontakter**, og velg deretter den relaterte koblingen.
2. Velg linjen for en kontakt, velg handlingen **Relatert informasjon**, og velg deretter **Kunde-/leverandør-/bankkonto/ansatt**.

## <a name="see-also"></a>Se også
[Administrere kontakter](marketing-contacts.md)  
[Konfigurere kontakter](marketing-setup-contacts.md)  
[Arbeide med Business Central](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]