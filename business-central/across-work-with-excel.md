---
title: Vise og redigere i Excel fra Business Central (inneholder video)
description: Lær om hvordan du åpner sidene i Microsoft Excel fra Business Central for bedre dataanalyser.
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.form: 1480
ms.search.keywords: 'accountant, accounting, financial report'
ms.date: 04/01/2021
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a>Vise og redigere i Excel fra Business Central

Med sider som viser en oversikt over poster i rader og kolonner, som en liste over kunder, ordrer eller fakturaer, kan du også eksportere listen til Microsoft Excel og vise den der. Avhengig av hvilken side du har, kan du vise to alternativer i Excel. Begge alternativene er tilgjengelige fra **Del**-ikonet ![Del en side i en annen app.](media/share-icon.png) øverst på en side. Du kan enten velge **Åpne i Excel**-handling eller **Rediger i Excel**-handlingen på siden. Denne artikkelen beskriver de to handlingene.

## <a name="open-in-excel"></a>Åpne i Excel

Med handlingen **Åpne i Excel** kan du gjøre endringer i postene i Excel, men du kan ikke publisere endringene tilbake til [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan bare lagre endringene i Excel-filen, uten at det påvirker dataene i [!INCLUDE[prod_short](includes/prod_short.md)].

- Med denne handlingen respekterer Excel filtre på siden som avgrenser postene som vises. Excel-arbeidsboken inneholder de samme radene og kolonnene som vises på siden i [!INCLUDE[prod_short](includes/prod_short.md)].

- Denne handlingen fungerer både i Windows- og macOS.
- [!INCLUDE[open-edit-excel](includes/open-and-edit-excel.md)]

> [!IMPORTANT]
> For [!INCLUDE[prod_short](includes/prod_short.md)] lokalt er handlingen **Åpne i Excel** tilgjengelig som standard. Hvis du konfigurerer [!INCLUDE[prod_short](includes/prod_short.md)] lokalt for redigering av data i Excel, erstattes handlingen **Åpne i Excel** med handlingen **Rediger i Excel**.

[!INCLUDE [send-report-excel](includes/send-report-excel.md)] 

> [!NOTE]
> I Excel har hele tall i kolonner et desimaltegn på slutten (som et punktum `.` eller komma `,`), selv om desimaltegnet ikke vises i Business Central. Desimalsymbolet er avhengig av enhetens områdeinnstillinger. I Business Central kan for eksempel `10` vises som `10.` eller `10,` i Excel. Du kan endre formatet i Excel ved å velge verdiene og deretter velge <kbd>Ctrl</kbd>+<kbd>1</kbd>. Hvis du vil ha mer informasjon om hvordan du endrer tallformatet i Excel, kan du gå til [Formatnumre](https://support.microsoft.com/office/format-numbers-f27f865b-2dc5-4970-b289-5286be8b994a).


## <a name="edit-in-excel"></a>Rediger i Excel

Handlingen **Rediger i Excel** er tilgjengelig i de fleste listene, men ikke alle. Med handlingen **Rediger i Excel** kan du gjøre endringer i postene i Excel og deretter publisere endringene tilbake til [!INCLUDE[prod_short](includes/prod_short.md)]. Når Excel åpnes, vises ruten for **Excel-tillegg** til høyre.

- Med denne handlingen respekterer Excel de fleste filtre på siden som begrenser postene som vises, slik at Excel-arbeidsboken vil inneholde nesten de samme postene og kolonnene.

- Du får de siste dataene fra [!INCLUDE[prod_short](includes/prod_short.md)] ved å velge **Oppdater** i ruten Excel-tillegg.
- [!INCLUDE[open-edit-excel](includes/open-and-edit-excel.md)]

### <a name="first-time-sign-in"></a>Første pålogging

Handlingen **Rediger i Excel** krever at Business Central-tillegget er installert i Excel. I noen tilfeller har administratoren kanskje ordnet det slik at tillegget installeres automatisk. I dette tilfellet må du bare logge deg på Business Central i ruten **Excel-tillegg** med brukernavn og passord. Ellers åpnes ruten **Ny Office-tillegg**. Hvis du vil installere tillegget, velger du **Klarer dette tillegget**, noe som installerer tillegget direkte fra Office store.

Hvis tillegget ikke blir installert, kontakter du administratoren eller prøver å installere det manuelt. Hvis du vil ha mer informasjon, kan du se [Installer tillegget manuelt for egen bruk](admin-deploy-excel-addin.md#install).

### <a name="work-across-environments-and-companies"></a>Arbeide på tvers av miljøer og selskaper

Du kan bytte ut selskapet du arbeider med. Hvis du vil bytte selskap, velger du ikonet **Alternativer** ![Alternativer for Excel-tillegg.](media/cogwheel.png "Alternativer for Excel-tillegg") i ruten Excel-tillegg og velger selskapet fra feltet **Selskap**.  

> [!IMPORTANT]
> Når du endrer firmaet, må du sørge for at **Miljø**-feltet ikke er tomt. Hvis det er det, setter du det til ett av de tilgjengelige alternativene. Hvis ikke, vil ikke tillegget fungere som det skal.  

Hvis du gjør endringer i tillegget, må du laste det inn på nytt for å oppdatere tilkoblingen. Du kan laste inn på nytt ved å bruke menyen for ![tillegg i Excel](media/excel-addin-menu.png "Meny for Excel-tillegg") øverst til høyre for tillegget. Hvis du ikke kan laste inn tillegget, kontakter du systemansvarlig. Hvis du er administrator, kan du se [Hent Business Central-tillegget for Excel](admin-deploy-excel-addin.md).

> [!NOTE]
> Tillegget fungerer med Excel for nettet (online) fra alle enheter så lenge du bruker en nettleser som støttes. Det fungerer også med Excel-appen for Windows (PC), men ikke for macOS.
>
> For [!INCLUDE[prod_short](includes/prod_short.md)] lokalt er handlingen **Rediger i Excel** bare tilgjengelig hvis Excel-tillegget er konfigurert av systemansvarlig, og den er bare tilgjengelig for webklienten. For administratorer, hvis du vil vite hvordan du installerer Excel-tilleggskomponenten, se [Definere Excel-tillegget for redigering av Business Central-data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).

### <a name="limits-when-using-excel-for-the-web"></a>Begrensninger når du bruker Excel for nettet

Når **Rediger i Excel** brukes på listesider for tabeller med mange kolonner, kan den resulterende arbeidsboken inneholde for mange kolonner for at filen kan vises i Excel for nettet. [!INCLUDE[prod_short](includes/prod_short.md)] begrenser automatisk den eksporterte arbeidsboken til 100 kolonner når OneDrive er konfigurert for systemfunksjoner. 

<!--## See the differences between the options
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]-->

## <a name="see-also"></a>Se også

[Analyser årsregnskap i Microsoft Excel](finance-analyze-excel.md)  
[Arbeid med Business Central](ui-work-product.md)  
[Forbedringer i Excel-integrasjon i 2019 lanseringsbølge 2](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
