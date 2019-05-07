---
title: Bokføre serviceordrer | Microsoft-dokumentasjon
description: Når du har opprettet en serviceordre, fylt ut alle nødvendige opplysninger og foretatt eventuelle endringer, kan du bokføre serviceordren. Ordren må inneholde minst én servicevarelinje og én servicelinje før du kan bokføre den. Hvis ordren inneholder mer enn én servicelinje, bokføres alle linjene samtidig.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 7ebec9a0a93fcbcd2f3e761fdf2410ee4d5a07db
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2019
ms.locfileid: "918437"
---
# <a name="post-service-orders-and-credit-memos"></a>Bokføre serviceordrer og kreditnotaer
Når du har opprettet en serviceordre, fylt ut alle nødvendige opplysninger og foretatt eventuelle endringer, kan du bokføre serviceordren. Ordren må inneholde minst én servicevarelinje og én servicelinje før du kan bokføre den. Hvis ordren inneholder mer enn én servicelinje, bokføres alle linjene samtidig.  

Hvis du har en stort antall serviceordrer, kan du spare tid ved å bruke en kjørsel til å bokføre dem samtidig. Du kan kjøre kjørselen fra en serviceordre.

> [!Tip]
> Før du bokfører et servicedokument, er det lurt å bruke handlingen **Kontrollrapport** for å søke etter alle feil eller manglende opplysninger. Hvis det oppstår feil, må du løse problemet. Du kan skrive ut en ny kontrollrapport for å kontrollere løsningen og deretter bokføre dokumentet.
  
## <a name="to-post-a-service-order"></a>Slik bokfører du en serviceordre    
1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Serviceordrer**, og velg deretter den relaterte koblingen.  
2. Åpne den aktuelle serviceordren.  
3. I vinduet **Serviceordre** velger du én av handlingene nedenfor.  
  
    |**Handling**|**Resultat**|  
    |------------------|----------------|  
    |**Kontrollrapport** | Kontrollerer alle delene i dokumentet, og presenterer resultatet i en rapport. Hvis rapporten angir feil eller manglende opplysninger, må du løse problemet. Deretter skriver du ut en ny kontrollrapport.|  
    |**Bokfør** | Ordren bokføres uten at det skrives ut noen følgeseddel eller faktura.|  
    |**Bokfør og skriv ut** | Ordren bokføres og det blir skrevet ut en følgeseddel (hvis du leverer ordren uten å fakturere den) eller en faktura (hvis du fakturerer ordren).|  
    |**Massebokfør** | Bokfører flere serviceordrer samtidig én gang.|  
  
4. Når du bokfører ordren, må du angi ett av alternativene nedenfor for hvordan du vil bokføre bestillingen.  
  
    |**Bokføringsalternativ**|**Resultat**|  
    |------------------------|----------------|  
    |**Levere** | Bokfører levering av varer.|  
    |**Fakturering** | Varer som allerede er levert, faktureres.|  
    |**Lever og fakturer** | Varene faktureres og leveres.|  
    |**Lever og forbruk** | Bokfører levering og forbruk på ordren. Det oppdaterer de aktuelle antallene på ordrens servicelinjes og på servicefølgeseddelen som tidligere ble bokført.|  
  
Du kan bokføre forbruk bare hvis linjen inneholder et antall som er levert men ikke fakturert eller forbrukt.  
  
Når du bokfører ordren, opprettes tilhørende poster og bokførte dokumenter. De relevante feltene oppdateres i serviceordredokumentet.  

## <a name="to-batch-post-service-orders"></a>Slik massebokfører du serviceordrer
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Serviceordrer**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Massebokfør**.  
3.  Du kan angi et filter for å velge bestemte serviceordrenumre eller en rekke med ordrenumre som kjørselen skal behandle.  
4.  Velg **OK** når du vil starte den satsvise jobben.  

## <a name="to-post-a-service-credit-memo"></a>Slik bokfører du en servicekreditnota  
Når du har opprettet en servicekreditnota og fylt den ut, kan du bokføre kreditnotaen. Hvis det er feil eller manglende opplysninger i kreditnotaen under bokføringen, avbrytes behandlingen med en feilmelding.  
   
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Servicekreditnotaer**, og velg deretter den relaterte koblingen.  
2. Opprett en servicekreditnota. I fanebladet **Hjem** under **Ny** velger du **Ny**.  
3. Fyll ut de nødvendige feltene.  
4. I fanebladet **Handlinger**, under **Bokføring** velger du **Bokfør**. Hvis du vil skrive ut kreditnotaen samtidig som du bokfører, velger du i stedet **Bokfør og skriv ut**.  
5. Hvis du vil teste kreditnotaer før du bokfører dem, velger du **Kontrollrapport**. Når du kjører rapporten, kontrolleres bokføringsdatoene som er angitt i dokumentet.  
6. Bokfør flere servicereditnotaer på en gang. kjør kjørselen **Massebokfør salgskreditnotaer \(service\)**. Dette kan være en fordel hvis du har en stort antall kreditnotaer som må bokføres.  
  
> [!NOTE]  
>  Det er viktig å skrive inn all nødvendig informasjon på kreditnotaene før de bokføres. Ellers er det mulig at de ikke vil bli bokført. Når den satsvise jobben er ferdig bokført, viser en melding hvor mange av servicekreditnotaene som er bokført.  

## <a name="to-post-consumption-from-a-service-order"></a>Slik bokfører du forbruk fra en serviceordre  
Fremgangsmåten nedenfor beskriver hvordan du bokfører varer, ressurstimer og/eller kost som er brukt i en bestemt serviceoperasjon som kunden ikke skal betale for. Merk at du bare kan bokføre forbrukt(e) varer, timer eller kost for en bokført følgesedler som ikke har fakturaer eller forbruk bokført.  

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Serviceordrer**, og velg deretter den relaterte koblingen.  
2. Åpne serviceordren du vil bokføre forbruk for.  
3. Velg servicevaren. Velg **Handlinger**, **Ordre** og deretter **Servicelinjer**.  
4. Finn de nødvendige postene, og angi antallene som du vil bokføre forbruk av i feltet **Antall til forbruk**. Antallet kan ikke være større enn allerede levert antall og gjenstående antall som ikke er fakturert etter delfakturering av leveringen.  
  
    > [!NOTE]  
    >  Hvis du vil registrere forbruk for et prosjekt, fyller du ut feltene **Prosjektnr.**, **Prosjektoppgavenr.** og **Prosjektlinjetype** i servicelinjen.  
  
5. Velg linjene som skal bokføres, og velg deretter handlingen **Bokfør**. Velg **Lever og forbruk** på siden som åpnes.  
  
Servicen bokføres som forbrukt, enten delvis eller fullstendig, avhengig av verdien i feltet **Antall til forbruk**, og de aktuelle postene blir opprettet. I tillegg oppdateres tidligere bokførte servicefølgeseddeldokumenter kronologisk med forbrukt antall. De relevante antallene blir oppdatert på servicelinjene i ordren.  

## <a name="to-post-shipments-from-service-orders"></a>Slik bokfører du følgesedler fra serviceordrer  
Når du har angitt detaljene for en service, kan du justere og bokføre antall brukte varer, tidsbruk og påløpt kost. Som følge av dette gjør [!INCLUDE[d365fin](includes/d365fin_md.md)] nødvendige endringer for å gjenspeile den nye statusen for lagerbeholdningen og gjeldende status for den aktuelle ordrebehandlingen.  
  
Følgende fremgangsmåte viser hvordan du bokfører levering av servicelinjevarer på lokasjoner som ikke er definert slik at lagerhåndtering kreves.  

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Serviceordre**, og velg deretter den relaterte koblingen. 2. På siden for den valgte serviceordren velger du **Handlinger**, **Ordre**, **Servicelinjer**.  
3. Finn de nødvendige postene på siden **Servicelinjer**, og angi antallet som skal bokføres, i feltet **Levere (antall)**.  
  
   > [!NOTE]  
   >  Verdien for antall som skal leveres, avhenger av om du vil bokføre leveringen fullstendig eller delvis. Hvis du velger å levere fullstendig, må verdien i feltet **Levere (antall)** være lik verdien i **Antall**-feltet. Når du bokfører en dellevering, må du angi antallet du vil levere innledningsvis. Hvis du allerede har levert deler av servicen i ordren, må du notere deg verdien i feltet **Levert (antall)**. Du kan ikke angi et antall i feltet **Levere (antall)** som er høyere enn antall enheter som ennå ikke er levert.  
  
4. Velg **Handlinger**, **Bokføring** og **Bokfør**. Velg **Levere** på siden som vises.  
  
[!INCLUDE[d365fin](includes/d365fin_md.md)] oppretter poster (i garantiposten, vareposten, serviceposten eller Finans). I tillegg produseres det bokførte servicefølgeseddeldokumentet, og relevante felt i servicelinjene i serviceordren oppdateres.  
  
Hvis lokasjonen er definert slik at lagerhåndtering kreves, fungerer levering og flytting av servicelinjevarer på samme måte som for andre kildedokumenter. Den eneste forskjellen er at servicelinjevarer kan forbrukes eksternt eller internt, og krever derfor to forskjellige frigivelsesfunksjoner.  
  
Hvis du vil ha informasjon om hvordan du leverer servicelinjevarer i avansert lageroppsett, kan du se [Plukke varer for lagerlevering](warehouse-pick-items.md).  

## <a name="to-undo-posted-consumption"></a>Slik angrer du bokført forbruk  
Du kan annullere forbruket i serviceordrene. For eksempel fordi det er bokført ved en feil.  

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bokførte servicefølgesedler**, og velg deretter den relaterte koblingen.  
2. Åpne den bokførte servicefølgeseddelen som det feilaktige forbruket er bokført for.  
3. Velg **Handlinger**, **Levering** og **Servicefølgeseddellinjer**.  
4. Velg linjene som inneholder det feilaktige forbruket, og velg deretter handlingen **Angre forbruk**.  
  
 En motsvarende servicefølgeseddellinje settes inn med negative verdier i antallsfeltene for de merkede linjene.  
  
> [!NOTE]  
>  Du kan ikke angre serviceforbruket hvis:  

>    * Serviceordren er lukket.  
>    * Den er bokført i Prosjekter-modulen, slik at det finnes poster for prosjekt som er knyttet til den.  
  
## <a name="to-post-service-lines"></a>Slik bokfører du servicelinjer  
Hvis du må arbeide med en serviceordre i lengre tid uten å bokføre den, kan det være ønskelig å bokføre noen av de tilkoblede servicelinjene, for eksempel for å holde lagerbeholdningen oppdatert. Du kan bokføre ved å angi relevante antall på linjene som skal bokføres. Du kan velge å bokføre linjene hver for seg eller ved å velge flere linjer samtidig.  
  
Fremgangsmåten nedenfor beskriver leveringsbokføring direkte fra en serviceordre på lokasjoner uten oppsett av lagerhåndtering. Hvis lokasjonen er definert slik at lagerhåndtering kreves, skjer leveringsbokføringen i et annet lagerdokument, avhengig av lokasjonsoppsettet.
  
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Serviceordrer**, og velg deretter den relaterte koblingen.  
2. Åpne serviceordren, og velg deretter handlingen **Servicelinjer**.  
4. På linjene som skal bokføres, fyller du ut feltene **Levere (antall)**, **Fakturer (antall)** og/eller **Antall til forbruk**, avhengig av hvordan du vil bokføre linjene.  
5. Velg handlingen **Bokfør**.
  
## <a name="see-also"></a>Se også  
[Bokføring i servicehåndtering](service-service-posting.md)  
[Opprette en serviceordre](service-how-to-create-service-orders.md)  
