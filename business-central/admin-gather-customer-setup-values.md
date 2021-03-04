---
title: Samle oppsettsverdier for kunde | Microsoft-dokumentasjon
description: Du kan bruke konfigurasjonsspørreskjemaet til å redusere arbeidsbelastningen ved implementering ved å strømlinjeforme oppgaven med å sette opp det nye firmaet. Du kan generere konfigurasjonsspørreskjemaet i Business Central og deretter gi det til kunden som en Excel-fil (xlsx) eller en XML-fil.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: ffe9e73312142f8cb7848620fd4acbfbb2db9798
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4752778"
---
# <a name="gather-customer-setup-values"></a>Samle oppsettsverdier for kunde
Du kan bruke konfigurasjonsspørreskjemaet til å redusere arbeidsbelastningen ved implementering ved å strømlinjeforme oppgaven med å sette opp det nye firmaet. Du kan generere konfigurasjonsspørreskjemaet i [!INCLUDE[prod_short](includes/prod_short.md)] og deretter gi det til kunden som en Excel- eller XML-fil.  

Du kan endre alle standardverdier i et spørreskjema slik at de er mer i samsvar med kundebehov.  

> [!TIP]  
>  Hvis du vil ha mer informasjon om hvordan du definerer oppsettsverdier i felt for forsyningsplanlegging, kan du se [Anbefalte fremgangsmåter for oppsett: Forsyningsplanlegging](setup-best-practices-supply-planning.md).  

Når kunden fullfører spørreskjemaet, kan du importere filen til kundens nye [!INCLUDE[prod_short](includes/prod_short.md)]-selskap. Du og kunden validerer svarene i spørreskjemaet før du kan bruke dem til selskapet.

## <a name="to-create-a-configuration-questionnaire"></a>Opprette et konfigurasjonsspørreskjema
Du kan bruke et spørreskjema som hjelper deg med å fastslå omfanget av og behovet for konfigurasjon. Du kan opprette et nytt spørreskjema eller endre et eksisterende spørreskjema ved å legge til nye spørsmål eller spørsmålsområder.  

<!-- A configuration questionnaire has the following structure
* The name of the questionnaire itself
* Question Areas that group questions about a similar subject. For example, you might create a question area that focuses on entering company informtion. Typically, configuration questionnaires have many question groups
* Questions that are closed ended, meaning that the customer must choose an answer, and can choose only one. -->

 Du kan opprette spørreskjemaer bare for tabeller av typen oppsett. Du kan for eksempel bruke verktøyet til å gi informasjon til følgende sider:  

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
>  Hvis du vil se en fullstendig liste over oppsettstabeller, velger du ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angir **Oppsett** og velger deretter den relaterte koblingen. Hvis du vil fastslå omfanget av postdataflytting, kan du bruke funksjonaliteten for flytting. Hvis du vil ha mer informasjon, kan du se [Flytte kundedata](admin-migrate-customer-data.md).  

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Konfigurasjonsspørreskjema**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**.   
3. På siden **Konfigurasjonsspørreskjema**, i **Kode**-feltet, angir du ... 
<!--4. In the **Name** field, enter...
5. Choose the **Question Areas** action. .
6. On the **Config. Question Areas** page, in the **Code** field, enter...
  
    > [!Note]  
    > The code is alphanumeric, and must start with a letter of the alphabet.
7. In the Table ID field, choose the table to which to apply the answer to the question. Your selection will determine the fields that are available for the questions, and thereby the answer selections.
  
    > [!Tip]
    > The list of table objects is long. If you know the name of the table, use **Search** in the upper left to find it in the list.
8. In the **Description** field, enter text that indicates the subject of the question group.
9. In the **No.** field, enter a number to define where the question appears in the sequence of questions.
10. In the **Field ID** field, choose the field the the customer's answer will be applied to. You can choose from the fields on the table you chose in the **Table ID** field.
  
    When you choose a field, [!INCLUDE[prod_short](includes/prod_short.md)] provides a suggestion in the **Question** field. You can edit the question if needed.
11. To add more questions to the questionnaire, repeat steps seven through 10.

> [!Tip]
> If at some point you change a question, or add a new one, choose the **Update Questions** action to update the list.

-->

3. Velg handlingen **Spørsmålsområder**. Siden **Spørsmålsområder** åpnes.  
4. Velg handlingen **Ny**. Siden **Konfig. spørsmålsområde** åpnes.  
5. I **Tabell-ID**-feltet velger du ID-en for tabellen du vil samle inn informasjon for. Feltet **Tabellnavn** fylles ut automatisk.  
6. Velg handlingen **Oppdater spørsmål**. Hvert felt i tabellen legges til i spørreskjemaet med et spørsmålstegn etter etiketten.

Du kan omformulere etiketten for å tydeliggjøre hvordan spørsmålet skal besvares. Hvis et felt for eksempel kalles "Navn", kan du redigere det slik at det står Hva er navnet på <data being collected>? Du kan også angi veiledningen i **Referanse**-feltet, inkludert en URL-adresse til en side som inneholder tilleggsinformasjon.  

Du kan også slette spørsmål som du ikke vil inkludere i spørreskjemaet.  

> [!NOTE]  
>  Feltet **Svaralternativ** beskriver typen og formatet på datasvaret som er riktig. **Svar**-feltet inneholder brukerspesifikk informasjon.  
>   
>  Etter behov kan du også definere standardsvar i **Svar**-feltet. Disse verdiene brukes som standard for tilpasset installasjon. Personen som fyller ut spørreskjemaet, kan imidlertid endre og oppdatere svaret.  

## <a name="to-complete-the-configuration-questionnaire"></a>Fullføre konfigurasjonsspørreskjemaet
Du bruker konfigurasjonsspørreskjema for å strukturere og dokumentere en detaljert diskusjon om kundens spesifikke behov. Du bruker det også til å innhente oppsettsdata fra kunden for å konfigurere de relevante [!INCLUDE[prod_short](includes/prod_short.md)]-oppsettstabellene, for eksempel finans, lager og kunder.  

> [!NOTE]  
>  Du kan også opprette ditt eget konfigurasjonsspørreskjema slik du vil ha det.  

1. Åpne selskapet du vil fullføre spørreskjemaet for.
2. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Konfigurasjonsspørreskjema**, og velg deretter den relaterte koblingen.  
3. Velg spørreskjemaet for selskapet, og velg deretter handlingen **Eksporter til Excel**, eventuelt **Eksporter til XML**.
4. Få kunden til å fullføre konfigurasjonsspørreskjemaet ved å skrive inn svarene i Excel-arbeidsboken. Det finnes forslag for hvert spørsmålsområde som er opprettet for spørreskjemaet.   
5. Lagre Excel-arbeidsboken som *XML-data*. Velg handlingen **Importer fra XML**, og velg deretter XML-filen med kundens svar.
6. Velg handlingen **Spørsmålsområder** for å starte prosessen med å validere og bruke svarene på konfigurasjonsspørreskjemaet.  

## <a name="to-complete-a-questionnaire-from-the-configuration-worksheet"></a>Slik fullfører du et spørreskjema fra konfigurasjonsforslaget:  
Fremgangsmåten nedenfor gir en alternativ måte å få tilgang til konfigurasjonsspørreskjemaer på. Det antar at konfigurasjonpakken du har fått in har blitt oppgitt inkluderer spørreskjemaer.  

1. Når du har importert en konfigurasjonspakke, åpner du konfigurasjonsforslaget.  
2. For hver tabell som det er et spørsmålsområde velger du handlingen **Spørsmål**. Spørreskjemasiden åpnes.  
3. Svar på spørsmålene, og velg deretter handlingen **Bruk svar**.  
4. Velg **OK**-knappen for å lukke spørreskjemaet.

## <a name="to-validate-the-configuration-questionnaire"></a>Validere konfigurasjonsspørreskjemaet
Det er viktig å validere konfigurasjonsspørreskjemaet før du bruker det på [!INCLUDE[prod_short](includes/prod_short.md)]-formatet. Det er også en måte å kontrollere at dataformateringen bevares under importen fra Excel.  

En vanlig valideringsoppgave er å kontrollere at tekststrenger ikke blir lagt inn i datofeltene. Denne kontrollprosessen er nødvendig fordi formatet for svaret i spørreskjemaet ikke bekreftes automatisk når du kjører funksjonen **Bruk svar**.  

> [!NOTE]  
>  Vanligvis er validering av konfigurasjonsspørreskjemaet en manuell prosess. Det foretas imidlertid kontroll av inkonsekvens i regional formatering. I tillegg får du feil hvis strukturen i [!INCLUDE[prod_short](includes/prod_short.md)]-databasen ikke samsvarer med strukturen i flyttingsdatabasen.  

1. På siden **Konfigurasjonsspørreskjema** velger du det aktuelle spørreskjemaet, og deretter velger du handlingen **Spørsmålsområder**.  
2. Åpne det aktuelle spørsmålsområdet.  
3. For hvert spørsmål validerer du at verdien i **Svar**-feltet svarer til formatet i **Svaralternativ**-feltet. Bekreft for eksempel at adressen til et selskap er i tekstformat.  
4. Hvis du finner feil, kan du feilsøke og korrigere i Excel ved å eksportere spørreskjemaet og deretter importere det på nytt. Du kan også rette opp feil direkte i [!INCLUDE[prod_short](includes/prod_short.md)] etter hvert som du ser gjennom svarene på siden **Konfig. spørsmålsområde**.  
5. Gjenta disse trinnene for hvert spørsmålsområde.  

Når du har fullført valideringen, er dataene klar til å bli brukt i databasen.  

## <a name="to-apply-answers-from-the-configuration-questionnaire"></a>Bruke svar fra konfigurasjonsspørreskjemaet
Når du har importert og validert informasjon fra et konfigurasjonsspørreskjema, kan du overføre eller bruke oppsettsdataene i de tilsvarende tabellene i [!INCLUDE[prod_short](includes/prod_short.md)]-databasen.  

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Konfigurasjonsspørreskjema**, og velg deretter den relaterte koblingen. Siden **Konfig.spørreskjema** åpnes.  
2. Velg et konfigurasjonsspørreskjema fra listen, og velg deretter handlingen **Rediger oversikt**.  
3. Du kan bruke svar på én av to måter.  

- Hvis du vil bruke hele spørreskjemaet, velger du handlingen **Bruk svar**.  
- Hvis du vil bruke svarene for bare et bestemt **spørsmålsområde**, velger du handlingen **Spørsmålsområder**, velger et **spørsmålsområde** i listen, og deretter velger handlingen **Bruk svar**.  

### <a name="to-verify-that-answers-have-been-applied-successfully"></a>Slik kontrollerer du at svar er brukt:  
1. Kontroller oppsettssider for de ulike funksjonelle områdene av [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan finne siden ved å velge ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi navnet på konfigurasjonssiden og deretter velge den relaterte koblingen.  
2. Kontroller at feltene er fylt ut med de riktige dataene fra de ulike spørsmålsområdene i konfigurasjonsspørreskjemaet.  

Du har nå konfigurert et oppsett med kundens forretningsinformasjon og regler.

## <a name="see-also"></a>Se også  
[Konfigurere et selskap med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administrasjon](admin-setup-and-administration.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]