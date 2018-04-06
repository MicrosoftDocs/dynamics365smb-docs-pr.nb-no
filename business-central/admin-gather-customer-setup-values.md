---
title: Samle oppsettsverdier for kunde | Microsoft-dokumentasjon
description: "Du kan bruke konfigurasjonsspørreskjemaet til å redusere arbeidsbelastningen ved implementering ved å strømlinjeforme oppgaven med å sette opp det nye firmaet. Du kan generere konfigurasjonsspørreskjemaet i Business Central og deretter gi det til kunden som en Excel-fil (XLS) eller en XML-fil."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/07/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: a1333567069d24bc5eff48d668dca8b480b85914
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="gather-customer-setup-values"></a>Samle oppsettsverdier for kunde
Du kan bruke konfigurasjonsspørreskjemaet til å redusere arbeidsbelastningen ved implementering ved å strømlinjeforme oppgaven med å sette opp det nye firmaet. Du kan generere konfigurasjonsspørreskjemaet i [!INCLUDE[d365fin](includes/d365fin_md.md)] og deretter gi det til kunden som en Excel- eller XML-fil.  

Du kan endre alle standardverdier i et spørreskjema slik at de er mer i samsvar med kundebehov.  

> [!TIP]  
>  Hvis du vil ha mer informasjon om hvordan du definerer oppsettsverdier i felt for forsyningsplanlegging, kan du se [Anbefalte fremgangsmåter for oppsett: Forsyningsplanlegging](setup-best-practices-supply-planning.md).  

Når kunden fullfører spørreskjemaet, kan du importere filen til kundens nye [!INCLUDE[d365fin](includes/d365fin_md.md)]-selskap. Du og kunden validerer svarene i spørreskjemaet før du kan bruke dem til selskapet.

## <a name="to-create-a-configuration-questionnaire"></a>Opprette et konfigurasjonsspørreskjema
Du kan bruke et spørreskjema som hjelper deg med å fastslå omfanget av og behovet for konfigurasjon. Du kan opprette et nytt spørreskjema eller endre et eksisterende spørreskjema ved å legge til nye spørsmål eller spørsmålsområder.  

 Du kan opprette spørreskjemaer bare for tabeller av typen oppsett. Du kan for eksempel bruke verktøyet til å gi informasjon til følgende vinduer:  

-   Selskapsopplysninger  
-   Aktivaoppsett  
-   Finansoppsett  
-   Lageroppsett  
-   Monteringsoppsett
-   Produksjonsoppsett  
-   Kjøpsoppsett  
-   Markedsføringsoppsett  
-   Serviceoppsett  
-   Oppsett av kunde- og leverandørkonto  
-   Lagerstyringsoppsett  

> [!NOTE]  
>  Hvis du vil vise en fullstendig liste over oppsettstabeller, velger du ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angir **Oppsett** og velger deretter den relaterte koblingen. Hvis du vil fastslå omfanget av postdataflytting, kan du bruke funksjonaliteten for flytting. Hvis du vil ha mer informasjon, kan du se [Flytte kundedata](admin-migrate-customer-data.md).  

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Konfigurasjonsspørreskjema**, og velg den relaterte koblingen.  
2. Velg handlingen **Ny**. Vinduet **Konfig.spørreskjema** åpnes.  
3. Velg handlingen **Spørsmålsområder**. Vinduet **Spørsmålsområder** åpnes.  
4. Velg handlingen **Ny**. Vinduet **Konfig. spørsmålsområde** åpnes.  
5. I **Tabell-ID**-feltet velger du ID-en for tabellen du vil samle inn informasjon for. Feltet **Tabellnavn** fylles ut automatisk.  
6. Velg handlingen **Oppdater spørsmål**. Hvert felt i tabellen legges til i spørreskjemaet med et spørsmålstegn etter etiketten.

Du kan omformulere etiketten for å tydeliggjøre hvordan spørsmålet skal besvares. Hvis et felt for eksempel kalles "Navn", kan du redigere det slik at det står Hva er navnet på <data being collected>? Du kan også angi veiledningen i **Referanse**-feltet, inkludert en URL-adresse til en side som inneholder tilleggsinformasjon.  

Du kan også slette spørsmål som du ikke vil inkludere i spørreskjemaet.  

> [!NOTE]  
>  Feltet **Svaralternativ** beskriver typen og formatet på datasvaret som er riktig. **Svar**-feltet inneholder brukerspesifikk informasjon.  
>   
>  Etter behov kan du også definere standardsvar i **Svar**-feltet. Disse verdiene brukes som standard for tilpasset installasjon. Personen som fyller ut spørreskjemaet, kan imidlertid endre og oppdatere svaret.  

## <a name="to-complete-the-configuration-questionnaire"></a>Fullføre konfigurasjonsspørreskjemaet
Du bruker konfigurasjonsspørreskjema for å strukturere og dokumentere en detaljert diskusjon om kundens spesifikke behov. Du bruker det også til å innhente oppsettsdata fra kunden for å konfigurere de relevante [!INCLUDE[d365fin](includes/d365fin_md.md)]-oppsettstabellene, for eksempel finans, lager og kunder.  

> [!NOTE]  
>  Du kan også opprette ditt eget konfigurasjonsspørreskjema slik du vil ha det.  

1. Åpne selskapet du vil fullføre spørreskjemaet for.
2. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Konfigurasjonsspørreskjema**, og velg deretter den relaterte koblingen.  
3. Velg spørreskjemaet for selskapet, og velg deretter handlingen **Eksporter til Excel**, eventuelt **Eksporter til XML**.
4. Få kunden til å fullføre konfigurasjonsspørreskjemaet ved å skrive inn svarene i Excel-arbeidsboken. Det finnes forslag for hvert spørsmålsområde som er opprettet for spørreskjemaet.   
5. Velg handlingen **importer fra Excel**, og velg deretter XLSX-filen med kundens svar.  
6. Velg handlingen **Spørsmålsområder** for å starte prosessen med å validere og bruke svarene på konfigurasjonsspørreskjemaet.  

## <a name="to-complete-a-questionnaire-from-the-configuration-worksheet"></a>Slik fullfører du et spørreskjema fra konfigurasjonsforslaget:  
Fremgangsmåten nedenfor gir en alternativ måte å få tilgang til konfigurasjonsspørreskjemaer på. Det antar at konfigurasjonpakken du har fått in har blitt oppgitt inkluderer spørreskjemaer.  

1. Når du har importert en konfigurasjonspakke, åpner du konfigurasjonsforslaget.  
2. For hver tabell som det er et spørsmålsområde velger du handlingen **Spørsmål**. Spørreskjemasiden åpnes.  
3. Svar på spørsmålene, og velg deretter handlingen **Bruk svar**.  
4. Velg **OK**-knappen for å lukke spørreskjemaet.

## <a name="to-validate-the-configuration-questionnaire"></a>Validere konfigurasjonsspørreskjemaet
Det er viktig å validere konfigurasjonsspørreskjemaet før du bruker det på [!INCLUDE[d365fin](includes/d365fin_md.md)]-formatet. Det er også en måte å kontrollere at dataformateringen bevares under importen fra Excel.  

En vanlig valideringsoppgave er å kontrollere at tekststrenger ikke blir lagt inn i datofeltene. Denne kontrollprosessen er nødvendig fordi formatet for svaret i spørreskjemaet ikke bekreftes automatisk når du kjører funksjonen **Bruk svar**.  

> [!NOTE]  
>  Vanligvis er validering av konfigurasjonsspørreskjemaet en manuell prosess. Det foretas imidlertid kontroll av inkonsekvens i regional formatering. I tillegg får du feil hvis strukturen i [!INCLUDE[d365fin](includes/d365fin_md.md)]-databasen ikke samsvarer med strukturen i flyttingsdatabasen.  

1. I vinduet **Konfigurasjonsspørreskjema** velger du det aktuelle spørreskjemaet, og deretter velger du handlingen **Spørsmålsområder**.  
2. Åpne det aktuelle spørsmålsområdet.  
3. For hvert spørsmål validerer du at verdien i **Svar**-feltet svarer til formatet i **Svaralternativ**-feltet. Bekreft for eksempel at adressen til et selskap er i tekstformat.  
4. Hvis du finner feil, kan du feilsøke og korrigere i Excel ved å eksportere spørreskjemaet og deretter importere det på nytt. Du kan også rette opp feil direkte i [!INCLUDE[d365fin](includes/d365fin_md.md)] etter hvert som du ser gjennom svarene i vinduet **Konfig. spørsmålsområde**.  
5. Gjenta disse trinnene for hvert spørsmålsområde.  

Når du har fullført valideringen, er dataene klar til å bli brukt i databasen.  

## <a name="to-apply-answers-from-the-configuration-questionnaire"></a>Bruke svar fra konfigurasjonsspørreskjemaet
Når du har importert og validert informasjon fra et konfigurasjonsspørreskjema, kan du overføre eller bruke oppsettsdataene i de tilsvarende tabellene i [!INCLUDE[d365fin](includes/d365fin_md.md)]-databasen.  

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Konfigurasjonsspørreskjema**, og velg deretter den relaterte koblingen. Vinduet **Konfig.spørreskjema** åpnes.  
2. Velg et konfigurasjonsspørreskjema fra listen, og velg deretter handlingen **Rediger oversikt**.  
3. Du kan bruke svar på én av to måter.  

- Hvis du vil bruke hele spørreskjemaet, velger du handlingen **Bruk svar**.  
- Hvis du vil bruke svarene for bare et bestemt **spørsmålsområde**, velger du handlingen **Spørsmålsområder**, velger et **spørsmålsområde** i listen, og deretter velger handlingen **Bruk svar**.  

### <a name="to-verify-that-answers-have-been-applied-successfully"></a>Slik kontrollerer du at svar er brukt:  
1. Kontroller oppsettsvinduer for de ulike funksjonelle områdene av [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hvis du vil finne vinduet, velger du ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angir navnet på oppsettvinduet og velger deretter den relaterte koblingen.  
2. Kontroller at feltene er fylt ut med de riktige dataene fra de ulike spørsmålsområdene i konfigurasjonsspørreskjemaet.  

Du har nå konfigurert et oppsett med kundens forretningsinformasjon og regler.

## <a name="see-also"></a>Se også  
[Konfigurere et selskap med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administrasjon](admin-setup-and-administration.md)

