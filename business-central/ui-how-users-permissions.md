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
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 58077ae917d7943e6dd2da06847dfbb0eef5defd
ms.contentlocale: nb-no
ms.lasthandoff: 09/28/2018

---
# <a name="managing-users-and-permissions"></a>Administrere brukere og tillatelser
For å legge til brukere i [!INCLUDE[d365fin](includes/d365fin_md.md)] må selskapets Office 365-administrator først opprette brukere i administrasjonssenteret for Office 365. For mer informasjon, se [Legge til brukere i Office 365 for bedrifter](https://aka.ms/CreateOffice365Users).

Når brukere er opprettet i Office 365, kan de leses inn i vinduet **Brukere** i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Brukere er tilordnet tillatelsessett avhengig av planen som er tilordnet til brukeren i Office 365. For mer detaljert informasjon om lisensiering, se [Lisensieringsveiledning for Microsoft Dynamics 365 Business Central](https://aka.ms/BusinessCentralLicensing).

Du kan deretter fortsette med å tildele tillatelser til brukere til å definere hvilke databaseobjekter, og dermed hvilke grensesnittelementer, de har tilgang til, og i som bedrifter. Du kan legge til brukere i grupper. Dette gjør det enklere å tilordne samme tillatelsessett til flere brukere.

Et tillatelsessett er en samling tillatelser for bestemte objekter i databasen. Alle brukere må være tilordnet ett eller flere tillatelsessett før de kan åpne [!INCLUDE[d365fin](includes/d365fin_md.md)].

Fra vinduet **Brukerkort** kan du åpne vinduet **Gyldige tillatelser** for å se hvilke tillatelser brukeren har, og gjennom hvilke tillatelsessett de er gitt. Her kan du også endre tillatelsesdetaljer for tillatelsessett av typen **Brukerdefinert**. Hvis du vil ha mer informasjon, kan du se delen "Slik viser eller redigerer du en brukers tillatelser".

Administratorer kan bruke vinduet **Brukeroppsett** til å definere hvor lenge angitte brukere skal kunne bokføre, og også angi om systemet skal logge hvor lenge brukere er logget på.

Et annet system som definerer hvilke brukere som har tilgang til opplevelsesinnstillingen. Hvis du vil ha mer informasjon, se [Endre hvilke funksjoner som vises](ui-experiences.md).

## <a name="to-add-a-user-in-business-central"></a>Slik legger du til en bruker i Business Central
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Brukere**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Hent brukere fra Office 365**.

Alle nye brukere som allerede er opprettet for ditt Office 365-abonnement, legges til i **Brukere**-vinduet.

## <a name="to-group-users-in-a-user-group"></a>Slik grupperer du brukere i en brukergruppe
Du kan definere brukergrupper til å administrere tillatelsessett for grupper av brukere i firmaet.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Brukergrupper**, og velg deretter den relaterte koblingen.
2. Du kan også gå til vinduet **Brukere** og velge handlingen **Brukergrupper**.
3. Gå til vinduet **Brukergruppe** og velg handlingen **Brukergruppemedlemmer**.
4. Gå til vinduet **Brukergruppemedlemmer** og velg handlingen **Legg til brukere**.

Når brukere eller brukergrupper er opprettet, må du tilordne tillatelsessett for hver for å definere hvilket objekt en bruker har tilgang til. Du må først organisere relevante tillatelser i tillatelsessett. Hvis du vil ha mer informasjon, kan du se delen "Slik oppretter eller viser du et tillatelsessett".

## <a name="to-copy-a-user-group-and-all-its-permission-sets"></a>Slik kopierer du en brukergruppe og alle tillatelsessettene
For å definere en ny brukergruppe raskt kan du kopiere alle tillatelsessett fra en eksisterende brukergruppe til den nye brukergruppen.

Brukergruppemedlemmene kopieres ikke til den nye brukergruppen. Du må legge dem til manuelt etterpå.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Brukergrupper**, og velg deretter den relaterte koblingen.
2. Velg brukergruppen du vil kopiere, og velg deretter handlingen **Kopier brukergruppe**.
3. I feltet **Ny brukergruppekode** angir du et navn på gruppen, og velger deretter **OK**-knappen.

Den nye brukergruppen legges til i **Brukergrupper**-vinduet. Fortsett med å legge til brukere. Hvis du vil ha mer informasjon, kan du se delen Slik grupperer du brukere i brukergrupper.  

## <a name="to-set-up-user-time-constraints"></a>Slik definerer du tidsbegrensninger for brukere:
Administratorer kan definere hvor lenge angitte brukere skal kunne bokføre, og også angi om systemet skal logge hvor lenge brukere er logget på. Administratorer kan også tilordne ansvarssentre til brukere. Hvis du vil ha mer informasjon, kan du se [Arbeide med ansvarssentre](inventory-responsibility-centers.md).

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Brukeroppsett**, og velg deretter den relaterte koblingen.
2. I vinduet **Brukeroppsett** velger du handlingen **Ny**.
3. I feltet **Bruker-ID** angir du ID-en for en bruker eller velger feltet for å vise alle gjeldende Windows-brukere i systemet.
4. Fyll ut feltene etter behov.

## <a name="to-create-or-edit-a-permission-set"></a>Slik oppretter eller redigerer du et tillatelsessett
Tillatelsessett fungerer som beholdere med tillatelser, slik at du enkelt kan behandle flere tillatelser i én post. Når du har opprettet et tillatelsessett, må du legge til de aktuelle tillatelsene. Hvis du vil ha mer informasjon, kan du se delen "Slik oppretter eller viser du tillatelsessett".

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

1. I vinduet **Tillatelsessett** merker du linjen for et tillatelsessett du vil kopiere, og velger deretter handlingen **Kopier tillatelsessett**.
2. I vinduet **Kopier tillatelsessett** angir du navnet på det nye tillatelsessettet, og velg deretter **OK**-knappen.
3. Merk av for **Varsle ved endret tillatelsessett** hvis du vil opprettholde en kobling mellom det opprinnelige og det kopierte tillatelsessettet. Koblingen brukes deretter til å varsle deg om navnet eller innholdet i det opprinnelige tillatelsessettet endres i en en fremtidig versjon som løsningen oppgraderes til senere.

Det nye tillatelsessettet, som inneholder alle tillatelsene i det kopierte tillatelsessettet, legges til som en ny linje i vinduet **Tillatelsessett**. Legg merke til at linjene sorteres alfabetisk innen hver type.

## <a name="to-create-or-edit-permissions"></a>Slik oppretter eller redigerer du tillatelser
1. I vinduet **Tillatelsessett** merker du linjen for et tillatelsessett, og velger deretter handlingen **Tillatelser**.
2. I vinduet **Tillatelser** oppretter du en ny linje eller redigerer feltene i en eksisterende linje.

I hvert av de fem tilgangstypefeltene, **Lesetillatelse**, **Innsettingstillatelse**, **Endringstillatelse**, **Slettetillatelse** og **Kjøringstillatelse**, kan du velge ett av følgende tre tillatelsesalternativer:

|Alternativ|Description|Rangering|
|------|-----------|
|**Ja**|Brukeren kan utføre handlingen for det aktuelle objektet.|Høyeste|
|**Indirekte**|Brukeren kan utføre handlingen for det aktuelle objektet, men bare via et annet tilknyttet objekt som brukeren har full tilgang til.|Nest høyeste|
|**Tom**|Brukeren kan ikke utføre handlingen for det aktuelle objektet.|Laveste|

> [!NOTE]  
> Når du redigerer en tillatelse og dermed det relaterte tillatelsessettet, gjelder endringene også for andre brukere som har tillatelsessettet tilordnet.

## <a name="to-assign-permission-sets-to-users-or-user-groups"></a>Slik tilordner du tillatelsessett til brukere eller grupper
Du kan tilordne tillatelser til brukere på to måter:
- Definere tillatelsessett på en brukers brukerkort.
- Merk av i boksen for en bruker, på en kolonne, for et relatert tillatelsessett, i en rad, i vinduet **Tillatelsessett etter bruker**.
    Med denne metoden kan du også tilordne tillatelsessett til brukergrupper.

### <a name="to-assign-a-permission-set-on-a-user-card"></a>Slik tilordner du et tillatelsesett på et brukerkort
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Brukere**, og velg deretter den relaterte koblingen.
2. Velg brukeren du vil tilordne tillatelse til.
Eventuelle tillatelsessett som allerede er tilordnet til brukeren, vises i faktaboksen **Tillatelsessett**.
3. Velg handlingen **Rediger** for å åpne **Brukerkort**-vinduet.
4. På hurtigfanen **Brukertillatelsessett** fyller du ut feltene etter behov på en ny linje. Hvis du vil ha mer informasjon, kan du se delen "Slik oppretter eller viser du et tillatelsessett".

### <a name="to-assign-a-permission-set-in-the-permission-set-by-user-window"></a>Slik tilordner du et tillatelsessett i vinduet **Tillatelsessett etter bruker**  
Fremgangsmåten nedenfor beskriver hvordan du kan tildele tillatelsessett til en bruker i vinduet **Tillatelsessett etter bruker**. Trinnene er like i vinduet **Tillatelsessett etter brukergruppe**.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Brukere**, og velg deretter den relaterte koblingen.
2. I vinduet **Brukere** velger du den aktuelle brukeren, og velger deretter handlingen **Tillatelsessett etter bruker**.
3. I vinduet **Tillatelsessett etter bruker** merker du av for **[brukernavn]** for en linje for det aktuelle tillatelsessettet for å tilordne settet til brukeren.
4. Merk av for **Alle brukere** for å tilordne tillatelsessettet til alle brukere.

## <a name="to-view-or-edit-a-users-permissions"></a>Slik viser eller redigerer du en brukers tillatelser
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Brukere**, og velg deretter den relaterte koblingen.
2. Åpne kortet til den relevante brukeren.
3. Velg handlingen **Gyldige tillatelser**.

    Delen **Tillatelser** viser alle databaseobjektene som brukeren har tilgang til. Du kan ikke redigere denne delen.

    Delen **Etter tillatelsessett** viser de tilordnede tillatelsessettene som brukes til å gi tillatelser til brukeren, kilden og typen tillatelsessett og i hvilken grad de ulike tilgangstypene er tillatt.

    For hver rad du velger i delen **Tillatelser**, viser **Etter tillatelsessett** hvilke tillatelsessett som tillatelsen blir gitt via. I denne delen kan du redigere verdien i hvert av de fem tilgangstypefeltene, **Lesetillatelse**, **Innsettingstillatelse**, **Endringstillatelse**, **Slettetillatelse** og **Kjøringstillatelse**.   

    > [!NOTE]  
    > Bare tillatelsessett av typen **Brukerdefinert** kan redigeres.<br /><br />
    > Rader for kilderettighet er hentet fra abonnementsplanen. Tillatelsesverdiene for rettigheten overstyrer verdier i andre tillatelsessett hvis de har en høyere rangering. En verdi i et ikke-berettiget tillatelsessett som har en høyere rangering enn den relaterte verdien i berettigelsen, vil stå i parenteser for å angi at den ikke er gyldig, siden den er overstyrt av berettigelsen. For en forklaring av rangering kan du se delen "Slik oppretter eller viser du tillatelsessett".  

4. Hvis du vil redigere et tillatelsessett, går du til delen **Etter tillatelsessett** og linjen for et relevant tillatelsessett av typen **Brukerdefinerte** og velger ett av de fem tilgangstypefeltene og en annen verdi.

5. Hvis du vil redigere enkelttillatelser i tillatelsessettene, kan du velge verdien i feltet **Tillatelsessett** for å åpne **Tillatelser**-vinduet. Følg trinnene beskrevet under "Slik oppretter eller redigerer du tillatelser".  

> [!NOTE]  
> Når du redigerer et tillatelsessett, gjelder endringene også for andre brukere som har tillatelsessettet tilordnet.

## <a name="see-also"></a>Se også
[Bli klar til å gjøre forretninger](ui-get-ready-business.md)  
[Endre hvilke funksjoner som vises](ui-experiences.md)   
[Administrasjon](admin-setup-and-administration.md)  
[Legge til brukere i Office 365 for business](https://aka.ms/CreateOffice365Users)  
[Lisensieringsveiledning for Microsoft Dynamics 365 Business Central](https://aka.ms/BusinessCentralLicensing)

