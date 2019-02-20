---
title: Opprette kontaktselskaper | Microsoft-dokumentasjon
ddescription: Outlines the tasks to create contact companies, including assigning relevant data about prospects and defining the business relationships you have with companies.
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 12/07/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 8a73de1aa2f4a0f633c401ea341bb7bde6579723
ms.openlocfilehash: 9699fc2194befcbca0610bb44d2a86d16d183cc6
ms.contentlocale: nb-no
ms.lasthandoff: 12/11/2018

---
# <a name="creating-contact-companies"></a>Opprette kontaktselskaper
Bedriften din møter regelmessig potensielle bedrifter som vanligvis utvikler seg til fremtidige forretningsforhold. Når bedriften har fått en ny kontakt, må denne informasjonen legges inn, slik at kommunikasjonen kan opprettholdes.

Ved å tilordne så mye data som mulig om en bestemt bedrift sørger du for effektiv kommunikasjon. Hvis du for eksempel tilordner den relevante bransjegruppen, sørger du for at spesifikke bedrifter inkluderes i all relevant kommunikasjon.

Du kan også definere forretningsforholdet du har med en kontakt. En kontakt kan for eksempel være et prospekt, en bank eller en leverandør.

## <a name="creatinge-contact-companies"></a>Opprette kontaktselskaper
Du kan opprette en kontakt for hvert nytt selskap du utfører en samhandling med, for eksempel kunder, leverandører, prospektive kunder, banker, advokatfirmaer, konsulenter og så videre.

Det er to måter å opprette en kontakt på: fra grunnen av eller fra en eksisterende kunde, leverandør eller bankkonto.

Før du oppretter en kontakt, bør du kontrollere innstillingene på siden **Markedsføringsoppsett**. Hvis du vil ha mer informasjon, kan du se [Sette opp forbindelser](marketing-setup-marketing.md).

### <a name="to-create-a-company-contact-from-scratch"></a>Slik oppretter du en selskapskontakt fra bunnen av
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Kontakter**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Ny**.
3. Angi et nummer på kontakten i feltet **Nr.**.

    Hvis du har definert en nummerserie for kontakter på siden **Markedsføringsoppsett**, kan du eventuelt trykke Enter-tasten for å velge det neste tilgjengelige kontaktnummeret.  
4. Sett **Type** til **Selskap**.
5. Fyll ut de andre feltene etter behov:

### <a name="to-create-a-company-contact-from-a-customer-vendor-or-bank-account"></a>Opprette en selskapskontakt fra en kunde, leverandør eller bankkonto
Hvis du allerede har definert en rekke kunder, leverandører og bankkonti, kan du opprette kontakter på grunnlag av de eksisterende dataene. Når du oppretter en kontakt på denne måten, synkroniseres kontaktinformasjonen med informasjon om kunden, leverandøren eller bankkontoen.

> [!NOTE]  
>   Før du kan opprette kontaktselskaper på denne måten, må du angi en kode for forretningsforbindelse for kunder, leverandører og bankkonti, på siden **Markedsføringsoppsett**. Hvis du vil opprette kontakter fra en bankkonto, må du også angi nummerserie for bankkonti på siden **Finansoppsett**.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi ett av følgende, alt etter hvor du vil opprette kontakter fra, og velg deretter den relaterte koblingen.
   * **Opprett kontakter fra kunder**
   * **Opprett kontakter fra leverandører**
   * **Opprett kontakter fra bankkonti**
2. Hvis du bare vil opprette kontakter fra bestemte kunder, leverandører eller bankkonti, definerer du filtre i inndelingen **Kunde**, **Leverandør** eller **Bankkonto** på siden for kjørselen som åpnes.
3. Velg **OK** for å starte oppretting av kontrakter.

    De neste kontaktnumrene i nummerserien tilordnes de nye kontaktene. Forretningsforbindelsen for leverandører som er angitt på siden **Markedsføringsoppsett**, tilordnes til nyopprettede kontakter.

> [!TIP]  
>   Du kan også opprette en kunde, leverandør eller bankkonto fra en kontakt. Hvis du vil ha mer informasjon, kan du se [Opprette en kunde, leverandør eller bankkonto fra en kontakt](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).

## <a name="synchronizing-contacts-with-customers-vendors-and-bank-accounts"></a>Synkronisere kontakter med kunder, leverandører og bankkonti
Hvis en del av kontaktene også er kunder, leverandører eller bankkonti, kan du synkronisere kontaktinformasjonen med relatert kunde, leverandør eller bankkonto. Synkronisering gjør at informasjon som er felles mellom kontakter og kunder, leverandører eller bankkonto, er den samme.  

Før du kan synkronisere kontaktene med kunder, leverandører eller bankkonti, må du angi en kode for forretningsforbindelse for kunder, leverandører og bankkonti på siden **Markedsføringsoppsett**. Hvis du vil ha mer informasjon, kan du se [Sette opp forbindelser](marketing-setup-marketing.md).

### <a name="different-ways-to-synchronize-contacts-with-customers-vendors-and-bank-accounts"></a>Ulike metoder for å synkronisere kontakter med kunder, leverandører og bankkonti
Du kan synkronisere kontaktene med kunder, leverandører eller bankkonti ved hjelp av tre metoder:

* Koble kontakter til eksisterende kunder, leverandører og/eller bankkonti fra kontaktkortet. Hvis du vil ha mer informasjon, kan du se [Knytte kontakter til kunder, leverandører og bankkonti](marketing-how-link-contact.md).
* Opprett kunder, leverandører eller bankkonti fra kontakten. Hvis du vil ha mer informasjon, kan du se [Opprette en kunde, leverandør eller bankkonto fra en kontakt](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).
* Opprett kontakter fra kunder, leverandører eller bankkonti. Hvis du vil ha mer informasjon, kan du se [Opprette en selskapskontakt fra kunde, leverandør eller bankkonto](marketing-how-create-contact-companies.md).

### <a name="consequences-of-synchronization"></a>Konsekvensene av synkronisering
Når kontakten synkroniseres med kunde, leverandør, bankkonto:

* Du trenger du bare å oppdatere opplysninger på ett sted. Hvis du for eksempel endrer telefonnummeret på kontakten, blir telefonnummeret automatisk oppdatert med de samme endringene på kunden, leverandøren eller bankkontoen.
* Hvis du har angitt en nummerserie for kontakter, opprettes det automatisk et kontaktkort for kunden, leverandøren eller bankkontoen når du oppretter et kundekort, leverandørkort eller bankkontokort.
* Du kan du opprette tilbud og ordrer og forespørsler og bestillinger fra kontakten.
* Du kan angi at samhandlinger registreres når du utfører handlinger, for eksempel når du skriver ut ordrer, rammeordrer, oppretter serviceordrer, sender e-post og så videre.
* Hvis du sletter en kontakt som er koblet til en kunde, leverandør eller bankkonto, er det bare kontakten som fjernes. Kunden, leverandøren eller bankkontoen beholdes.
* Hvis du sletter en kunde, leverandør eller bankkonto som er koblet til en kontakt, beholdes kontakten.

> [!NOTE]  
>   Noen detaljer, for eksempel fakturerings- og bokføringsopplysninger, vises ikke på kontaktkortet. Du vil derfor kanskje legge dem til manuelt på kundekortet, leverandørkortet eller bankkontokortet når du oppretter kontakter som kunder, leverandører eller bankkonti.

## <a name="linking-contacts-with-customers-vendors-and-bank-accounts"></a>Knytte kontakter til kunder, leverandører og bankkonti
Hvis du har kontakt og enten en kunde, leverandør eller bankkonto for samme selskap, kan du knytte sammen de to enhetene. Tilknytning av de to enhetene lar deg synkronisere data som er felles, slik at det er de samme i begge steder.

### <a name="to-link-a-contact-to-an-existing-customer-vendor-or-bank-account"></a>Slik knytter du en kontakt til en eksisterende kunde, leverandør eller bankkonto
1. Åpne kontakten du vil tilknytte.
2. Velg handlingen **Knytt til eksisterende**, og velg deretter **Kunde**, **Leverandør** eller **Bank**.
3. Velg kunde, leverandør eller bankkonto å tilknytte.

   I **Gjeldende hovedfelt** angir du hvilke felt som skal prioriteres hvis det er motstridende opplysninger i felt som er felles for kontakten og kunden, leverandøren eller kontoen. Hvis selgerkoden for eksempel er forskjellig i kontakten og kunden, kan du angi å bruke informasjonen i kontakten, ved å velge **Kontakt**.

## <a name="creating-a-customer-vendor-or-bank-account-from-a-contact"></a>Opprette en kunde, leverandør eller bankkonto fra en kontakt
   Du ønsker kanskje å registrere noen av de eksisterende kontaktene som kunder, leverandører eller bankkonti. Oppretting av en kunde, leverandør eller bankkonto fra en kontakt, lar deg bruke eksisterende data. Når du oppretter en kunde, leverandør eller bankkonto på denne måten, synkroniseres den med kontakten. Synkronisering gjør at informasjon som er felles mellom kontakter og kunder, leverandører eller bankkonto, er den samme.

   Før du kan registrere kontakter på denne måten, må du angi en forretningsforbindelseskode for kunder, leverandører og bankkonti, på siden **Markedsføringsoppsett**. Hvis du vil registrere kontakter som bankkonti, må du også angi nummerserie for bankkonti på siden **Finansoppsett**.

### <a name="to-create-a-contact-as-a-customer-vendor-or-bank-account"></a>Slik oppretter du en kontakt som en kunde, leverandør eller bankkonto
   1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Kontakter**, og velg deretter den relaterte koblingen.
   2. Velg kontakten du vil opprette som en kunde, leverandør eller bankkonto.
   3. Velg handlingen **Opprett som**, og velg deretter **Kunde**, **Leverandør** eller **Bank**.
   4. Bekreft meldingen som vises.

   Kontaktinformasjonen er overført fra **Kontakt**-kortet til **Bankkonto**-kortet, **Kunde**-kortet eller **Leverandør**-kortet. Noen ganger kan det være nødvendig å legge til spesifikke opplysninger på hvert kort, for eksempel fakturerings- og betalingsopplysninger.

## <a name="setting-up-business-relations-on-contact-companies"></a>Definere forretningsforbindelser for kontaktselskaper
Du kan bruke forretningsforbindelser blir brukt til å angi hvilket forretningsforhold du har til kontaktene, for eksempel prospekter, banker, konsulenter, serviceleverandører og så videre.

Bruk av forretningsforbindelser på kontakter er en totrinnsprosess. Først må definere du koden for forretningsforbindelsen. Du trenger bare utføre dette trinnet én gang for hver forretningsforbindelse. Når du har en kode for forretningsforbindelse, kan du begynne å tilordne koden til kontaktselskaper.

> [!NOTE]  
>   Hvis du planlegger å synkronisere kontaktene med leverandører, kunder eller bankkonti i andre deler av programmet, bør du definere en forretningsforbindelse for disse.

### <a name="to-define-a-business-relation-code"></a>Definere en kode for forretningsforbindelse
Koden for forretningsforbindelsen definerer en kategori eller type for forretningsforbindelsen, for eksempel BANK eller Juridisk. Du kan ha flere forretningsforbindelseskoder. Hvis du vil definere forretningsforbindelsen, bruker du siden **Forretningsforbindelser**.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Forretningsforbindelser**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Ny**, og fyll ut en kode og en beskrivelse. Koden kan bestå av opptil 11 tegn, og kan inneholde en kombinasjon av tall og bokstaver.

### <a name="AssignBusRelContact"></a> Tilordne forretningsforbindelser til en kontakt
Du kan ikke tilordne forretningsforbindelser til en kontaktperson, bare selskaper.

1. Åpne kontakten.
2. Velg handlingen **Selskap**, og deretter handlingen **Forretningsforbindelser**.

    Siden **Kontaktens forretn.forbind.** åpnes.
3. Velg forretningsforbindelsen du vil tilordne, i feltet **Forretn.forbindelseskode**.

Gjenta disse trinnene hvis du vil tilordne flere forretningsforbindelser. Du kan også tilordne forretningsforbindelser fra kontaktlisten ved å følge samme fremgangsmåte.

Antall forretningsforbindelser du har tilordnet kontakten, vises i feltet **Ant. forretningsforbindelser** i inndelingen **Segmentering** på siden **Kontakt**.

Når du har tilordnet forretningsforbindelser til kontaktene, kan du bruke disse opplysningene til å velge kontakter for segmentene. Hvis du vil ha mer informasjon, kan du se [Legge til kontakter i segmenter](marketing-add-contact-segment.md).

## <a name="see-also"></a>Se også
[Opprette kontaktpersoner](marketing-create-contact-persons.md)   
[Arbeide med Business Central](ui-work-product.md)

