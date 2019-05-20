---
title: Tilordne eller redigere brukertillatelser | Microsoft-dokumentasjon
description: Beskriver hvordan du legger til Office 365-brukere i Business Central og deretter tilordner tillatelser, tilgangsrettigheter og sikkerhetsinnstillinger.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 4a9bbc34893f1af257908558122f8e8cbe6ce757
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2019
ms.locfileid: "1250115"
---
# <a name="managing-users-and-permissions"></a>Administrere brukere og tillatelser
For å legge til brukere i [!INCLUDE[d365fin](includes/d365fin_md.md)] må selskapets Office 365-administrator først opprette brukere i administrasjonssenteret for Office 365. For mer informasjon, se [Legge til brukere i Office 365 for bedrifter](https://aka.ms/CreateOffice365Users).

Når brukere er opprettet i Office 365, kan de leses inn på siden **Brukere** i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Brukere er tilordnet tillatelsessett avhengig av planen som er tilordnet til brukeren i Office 365. For mer detaljert informasjon om lisensiering, se [Lisensieringsveiledning for Microsoft Dynamics 365 Business Central](https://aka.ms/BusinessCentralLicensing).

Du kan deretter fortsette med å tildele tillatelser til brukere til å definere hvilke databaseobjekter, og dermed hvilke grensesnittelementer, de har tilgang til, og i som bedrifter. Du kan legge til brukere i grupper. Dette gjør det enklere å tilordne samme tillatelsessett til flere brukere.

Et tillatelsessett er en samling tillatelser for bestemte objekter i databasen. Alle brukere må være tilordnet ett eller flere tillatelsessett før de kan åpne [!INCLUDE[d365fin](includes/d365fin_md.md)].

Fra siden **Brukerkort** kan du åpne siden **Gyldige tillatelser** for å se hvilke tillatelser brukeren har, og gjennom hvilke tillatelsessett de er gitt. Her kan du også endre tillatelsesdetaljer for tillatelsessett av typen **Brukerdefinert**. Hvis du vil ha mer informasjon, kan du se [For å få en oversikt over en brukers tillatelser](ui-how-users-permissions.md#to-get-an-overview-of-a-users-permissions).

Administratorer kan bruke siden **Brukeroppsett** til å definere hvor lenge angitte brukere skal kunne bokføre, og også angi om systemet skal logge hvor lenge brukere er logget på.

Et annet system som definerer hvilke brukere som har tilgang til opplevelsesinnstillingen. Hvis du vil ha mer informasjon, se [Endre hvilke funksjoner som vises](ui-experiences.md).

## <a name="to-add-a-user-in-business-central"></a>Slik legger du til en bruker i Business Central
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Brukere**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Hent brukere fra Office 365**.

Alle nye brukere som allerede er opprettet for ditt Office 365-abonnement, legges til på siden **Brukere**.

## <a name="to-group-users-in-user-groups"></a>Slik grupperer du brukere i brukergrupper
Du kan definere brukergrupper til å administrere tillatelsessett for grupper av brukere i firmaet.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Brukergrupper**, og velg deretter den relaterte koblingen.
2. Du kan også gå til siden **Brukere** og velge handlingen **Brukergrupper**.
3. Gå til siden **Brukergruppe** og velg handlingen **Brukergruppemedlemmer**.
4. Velg **Legg til brukere** på siden **Brukergruppemedlemmer**.

Når brukere eller brukergrupper er opprettet, må du tilordne tillatelsessett for hver for å definere hvilket objekt en bruker har tilgang til. Du må først organisere relevante tillatelser i tillatelsessett. Hvis du vil ha mer informasjon, kan du se [For å få en oversikt over en brukers tillatelser](ui-how-users-permissions.md#to-get-an-overview-of-a-users-permissions).

## <a name="to-copy-a-user-group-and-all-its-permission-sets"></a>Slik kopierer du en brukergruppe og alle tillatelsessettene
For å definere en ny brukergruppe raskt kan du kopiere alle tillatelsessett fra en eksisterende brukergruppe til den nye brukergruppen.

Brukergruppemedlemmene kopieres ikke til den nye brukergruppen. Du må legge dem til manuelt etterpå.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Brukergrupper**, og velg deretter den relaterte koblingen.
2. Velg brukergruppen du vil kopiere, og velg deretter handlingen **Kopier brukergruppe**.
3. I feltet **Ny brukergruppekode** angir du et navn på gruppen, og velger deretter **OK**-knappen.

Den nye brukergruppen legges til på **Brukergrupper**-siden. Fortsett med å legge til brukere. Hvis du vil ha mer informasjon, kan du se [Slik grupperer du brukere i brukergrupper](ui-how-users-permissions.md#to-group-users-in-user-groups).  

## <a name="to-set-up-user-time-constraints"></a>Slik definerer du tidsbegrensninger for brukere:
Administratorer kan definere hvor lenge angitte brukere skal kunne bokføre, og også angi om systemet skal logge hvor lenge brukere er logget på. Administratorer kan også tilordne ansvarssentre til brukere. Hvis du vil ha mer informasjon, kan du se [Arbeide med ansvarssentre](inventory-responsibility-centers.md).

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Brukeroppsett**, og velg deretter den relaterte koblingen.
2. På siden **Brukeroppsett** velger du handlingen **Ny**.
3. I feltet **Bruker-ID** angir du ID-en for en bruker eller velger feltet for å vise alle gjeldende Windows-brukere i systemet.
4. Fyll ut feltene etter behov.

## <a name="to-create-or-modify-a-permission-set"></a>Opprette eller endre et tillatelsessett
Tillatelsessett fungerer som beholdere med tillatelser, slik at du enkelt kan behandle flere tillatelser i én post. Når du har opprettet et tillatelsessett, må du legge til de aktuelle tillatelsene. Hvis du vil ha mer informasjon, kan du se [Opprette eller endre tillatelser manuelt](ui-how-users-permissions.md#to-create-or-modify-permissions-manually).

> [!NOTE]  
> En [!INCLUDE[d365fin](includes/d365fin_md.md)]-løsningen inneholder vanligvis et antall forhåndsdefinerte tillatelsessett som legges til av Microsoft eller programvareleverandøren. Disse tillatelsessettene er av typen **System** eller **Utvidelse**. Du kan ikke opprette eller redigere disse typene tillatelsessett eller tillatelsene i dem. Du kan imidlertid kopiere dem for å definere dine egne tillatelsessett og tillatelser. <br /><br />
Tillatelse som brukere oppretter, fra nye eller som kopier, er av typen **Brukerdefinert** og kan redigeres.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Tillatelsessett**, og velg deretter den relaterte koblingen.
2. Velg **Ny**-handlingen for å opprette et nytt tillatelsessett.
3. Fyll ut feltene etter behov på den nye linjen. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="to-copy-a-permission-set"></a>Slik kopiere du et tillatelsessett
Når du oppretter nye tillatelsessett, kan du bruke en kopieringsfunksjon til å overføre alle tillatelser i et annet tillatelsessett til et nytt tillatelsessett raskt.

> [!NOTE]  
> Hvis et systemtillatelsessett som du har kopiert, endres, vil du bli varslet (avhengig av hva du velger), slik at du kan ta hensyn til om endringene er relevante for å kopieres eller skrives inn i det brukerdefinerte tillatelsessettet ditt.

1. På siden **Tillatelsessett** merker du linjen for et tillatelsessett du vil kopiere, og velger deretter handlingen **Kopier tillatelsessett**.
2. På siden **Kopier tillatelsessett** angir du navnet på det nye tillatelsessettet, og velg deretter **OK**-knappen.
3. Merk av for **Varsle ved endret tillatelsessett** hvis du vil opprettholde en kobling mellom det opprinnelige og det kopierte tillatelsessettet. Koblingen brukes deretter til å varsle deg om navnet eller innholdet i det opprinnelige tillatelsessettet endres i en en fremtidig versjon som løsningen oppgraderes til senere.

Det nye tillatelsessettet, som inneholder alle tillatelsene i det kopierte tillatelsessettet, legges til som en ny linje på siden **Tillatelsessett**. Legg merke til at linjene sorteres alfabetisk innen hver type.

## <a name="to-create-or-modify-permissions-manually"></a>Opprette eller endre tillatelser manuelt
Denne fremgangsmåten beskriver hvordan du legger til eller redigerer tillatelser manuelt. Du kan også generere et tillatelsessett automatisk fra handlingene i grensesnittet. Hvis du vil ha mer informasjon, kan du se [Opprette eller endre tillatelsessett ved å registrere handlingene dine](ui-how-users-permissions.md#to-create-or-modify-permission-sets-by-recording-your-actions).

1. På siden **Tillatelsessett** merker du linjen for et tillatelsessett og velger deretter handlingen **Tillatelser**.
2. På siden **Tillatelser** oppretter du en ny linje eller redigerer feltene i en eksisterende linje.

I hvert av de fem tilgangstypefeltene, **Lesetillatelse**, **Innsettingstillatelse**, **Endringstillatelse**, **Slettetillatelse** og **Kjøringstillatelse**, kan du velge ett av følgende tre tillatelsesalternativer:

|Alternativ|Description|Rangering|
|------|-----------|
|**Ja**|Brukeren kan utføre handlingen for det aktuelle objektet.|Høyeste|
|**Indirekte**|Brukeren kan utføre handlingen for det aktuelle objektet, men bare via et annet tilknyttet objekt som brukeren har full tilgang til.|Nest høyeste|
|**Tom**|Brukeren kan ikke utføre handlingen for det aktuelle objektet.|Laveste|

### <a name="example---indirect-permission"></a>Eksempel - indirekte tillatelse
Du kan tilordne en indirekte tillatelse til å bruke et objekt, bare via et annet objekt.
En bruker kan for eksempel ha tillatelse til å kjøre kodeenhet 80, Sales-Post. Kodeenheten Sales-Post utfører mange oppgaver, inkludert å endre tabell 37, salgslinjen. Når du bokfører et salgsdokument, codeunit Sales-Post, kontrollerer [!INCLUDE[d365fin](includes/d365fin_md.md)] om brukeren har tillatelse til å endre Salgslinje-tabellen. Hvis ikke kan ikke kodeenheten fullføre oppgavene, og brukeren får en feilmelding. Hvis dette er tilfelle, kjører kodeenheten uten problemer.

Brukeren trenger imidlertid ikke full tilgang til tabellen Salgslinje for å kunne kjøre kodeenheten. Hvis brukeren har indirekte tillatelse til Salgslinje-tabellen, kjører codeunit Sales-Post uten problemer. Når en bruker har indirekte tillatelse, kan vedkommende bare endre tabellen Salgslinje ved å kjøre kodeenheten Sales-Post eller et annet objekt som har tillatelse til å endre tabellen Salgslinje. Brukeren kan bare endre Salgslinje-tabellen når det gjøres fra moduler som støttes. Brukeren kan ikke kjøre funksjonen ved en feiltakelse eller med onde hensikter ved hjelp av andre metoder.

### <a name="to-limit-a-users-access-to-specific-records-in-a-table"></a>Slik begrenser du brukerens adgang til bestemte poster i en tabell
For sikkerhet på postnivå i [!INCLUDE[d365fin](includes/d365fin_md.md)] bruker du sikkerhetsfiltrene til å begrense en brukers tilgang til data i en tabell. Du oppretter sikkerhetsfiltre på tabelldata. Et sikkerhetsfilter beskriver et sett med poster i en tablle som en bruker har tilgang til. Du kan for eksempel angi at en bruker bare kan lese poster som inneholder informasjon om en bestemt kunde. Dette betyr at brukeren ikke har tilgang til postene som inneholder informasjon om andre kunder. Hvis du vil ha mer informasjon, kan du se [Bruke sikkerhetsfiltre](/dynamics365/business-central/dev-itpro/security/security-filters) hjelpen for utviklere og IT-eksperter.


## <a name="to-create-or-modify-permission-sets-by-recording-your-actions"></a>Hvis du vil opprette eller endre tillatelsen angis ved makroregistreringen
1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Tillatelsessett**, og velg deretter den relaterte koblingen.
2.  Du kan også gå til siden **Brukere** og velge handlingen **Tillatelsessett**.
3.  På siden **Tillatelsessett** velger du handlingen **Ny**.
4.  Fyll ut feltene etter behov på en ny linje.
5.  Velg handlingen **Tillatelser**.
6.  På **Tillatelser**-siden velger du **Registrer tillatelser**-handlingen, og velg deretter **Start**-handlingen.

    Dette starter en innspillingsprosess som fanger opp alle handlingene dine i brukergrensesnittet.
7.  Gå til de ulike sidene og aktivitetene i [!INCLUDE[d365fin](includes/d365fin_md.md)] som du vil at brukere med dette tillatelsessettet skal få tilgang til. Du må utføre oppgaver som du vil registrere tillatelser for.
8.  Når du vil avslutte opptaket, gå tilbake til **Tillatelser**-siden, og velg deretter **Stopp**-handlingen.
9.  Velg **Ja**-knappen for å legge til registrerte rettigheter til det nye tillatelsessettet.
10. Angi om brukere skal kunne sette inn, endre eller slette poster i tabeller som er registrert for hvert objekt i listen over registrerte.

> [!NOTE]  
> Når du redigerer en tillatelse og dermed det relaterte tillatelsessettet, gjelder endringene også for andre brukere som har tillatelsessettet tilordnet.

## <a name="to-assign-permission-sets-to-users-or-user-groups"></a>Slik tilordner du tillatelsessett til brukere eller grupper
Du kan tilordne tillatelser til brukere på to måter:
- Definere tillatelsessett på en brukers brukerkort.
- Merk av i boksen for en bruker, på en kolonne, for et relatert tillatelsessett, i en rad, på siden **Tillatelsessett etter bruker**.
    Med denne metoden kan du også tilordne tillatelsessett til brukergrupper.

### <a name="to-assign-a-permission-set-on-a-user-card"></a>Slik tilordner du et tillatelsesett på et brukerkort
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Brukere**, og velg deretter den relaterte koblingen.
2. Velg brukeren du vil tilordne tillatelse til.
Eventuelle tillatelsessett som allerede er tilordnet til brukeren, vises i faktaboksen **Tillatelsessett**.
3. Velg handlingen **Rediger** for å åpne **Brukerkort**-siden.
4. På hurtigfanen **Brukertillatelsessett** fyller du ut feltene etter behov på en ny linje. Hvis du vil ha mer informasjon, kan du se [Slik oppretter eller viser du et tillatelsessett](ui-how-users-permissions.md#to-create-or-modify-a-permission-set).

### <a name="to-assign-a-permission-set-on-the-permission-set-by-user-page"></a>Slik tilordner du et tillatelsessett på siden **Tillatelsessett etter bruker**  
Fremgangsmåten nedenfor beskriver hvordan du kan tildele tillatelsessett til en bruker på siden **Tillatelsessett etter bruker**. Trinnene er like på siden **Tillatelsessett etter brukergruppe**.

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Brukere**, og velg deretter den relaterte koblingen.
2. På siden **Brukere** velger du den aktuelle brukeren, og velger deretter handlingen **Tillatelsessett etter bruker**.
3. På siden **Tillatelsessett etter bruker** merker du av for **[brukernavn]** for en linje for det aktuelle tillatelsessettet for å tilordne settet til brukeren.
4. Merk av for **Alle brukere** for å tilordne tillatelsessettet til alle brukere.

## <a name="to-get-an-overview-of-a-users-permissions"></a>For å få en oversikt over en brukers tillatelser
1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Brukere**, og velg deretter den relaterte koblingen.
2. Åpne kortet til den relevante brukeren.
3. Velg handlingen **Gyldige tillatelser**.

    Delen **Tillatelser** viser alle databaseobjektene som brukeren har tilgang til. Du kan ikke redigere denne delen.

    Delen **Etter tillatelsessett** viser de tilordnede tillatelsessettene som brukes til å gi tillatelser til brukeren, kilden og typen tillatelsessett og i hvilken grad de ulike tilgangstypene er tillatt.

    For hver rad du velger i delen **Tillatelser**, viser **Etter tillatelsessett** hvilke tillatelsessett som tillatelsen blir gitt via. I denne delen kan du redigere verdien i hvert av de fem tilgangstypefeltene, **Lesetillatelse**, **Innsettingstillatelse**, **Endringstillatelse**, **Slettetillatelse** og **Kjøringstillatelse**.   

    > [!NOTE]  
    > Bare tillatelsessett av typen **Brukerdefinert** kan redigeres.<br /><br />
    > Rader for kilderettighet er hentet fra abonnementsplanen. Tillatelsesverdiene for rettigheten overstyrer verdier i andre tillatelsessett hvis de har en høyere rangering. En verdi i et ikke-berettiget tillatelsessett som har en høyere rangering enn den relaterte verdien i berettigelsen, vil stå i parenteser for å angi at den ikke er gyldig, siden den er overstyrt av berettigelsen. For en forklaring av rangering kan du se [Slik oppretter eller viser du tillatelsessett manuelt](ui-how-users-permissions.md#to-create-or-modify-permissions-manually).  

4. Hvis du vil redigere et tillatelsessett, går du til delen **Etter tillatelsessett** og linjen for et relevant tillatelsessett av typen **Brukerdefinerte** og velger ett av de fem tilgangstypefeltene og en annen verdi.

5. Hvis du vil redigere enkelttillatelser i tillatelsessettene, kan du velge verdien i feltet **Tillatelsessett** for å åpne **Tillatelser**-siden. Følg trinnene beskrevet under [Slik oppretter eller redigerer du tillatelser](ui-how-users-permissions.md#to-create-or-modify-permissions-manually).  

> [!NOTE]  
> Når du redigerer et tillatelsessett, gjelder endringene også for andre brukere som har tillatelsessettet tilordnet.

## <a name="see-also"></a>Se også
[Sikkerhet og beskyttelse i Business Central](/dynamics365/business-central/dev-itpro/security/security-and-protection)  
[Forstå brukere, profiler og rollesentre](admin-users-profiles-roles.md)  
[Bli klar til å gjøre forretninger](ui-get-ready-business.md)  
[Endre hvilke funksjoner som vises](ui-experiences.md)  
[Administrasjon](admin-setup-and-administration.md)  
[Legge til brukere i Office 365 for business](https://aka.ms/CreateOffice365Users)  
[Lisensveiledning for Microsoft Dynamics 365 Business Central](https://aka.ms/BusinessCentralLicensing)
