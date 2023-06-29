---
title: Arbeid med gjentakelsesomsetning
description: Finn ut mer om de tilgjengelige alternativene for å automatisere sending av abonnementsfakturaer til kundene og registrere gjentakelsesomsetning.
author: AndreiPanko
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'recurring, invoicing, subscription, billing'
ms.search.form: 283
ms.reviewer: edupont
ms.date: 04/01/2021
ms.author: andreipa
---
# <a name="work-with-recurring-revenue-in-"></a><a name="work-with-recurring-revenue-in-"></a>Arbeide med gjentakelsesomsetning i [!INCLUDE[prod_short](includes/prod_short.md)]

Mange selskaper flytter fra en bedriftsomsetningsmodell der omsetningen foretas fra en kundes engangskjøps til en abonnementsmodell der omsetningen er regelmessig i bytte mot konsekvent tilgang til levering av en vare eller tjeneste.
[!INCLUDE[prod_short](includes/prod_short.md)] har følgende alternativer for å automatiskere hvordan du sender abonnementsfakturaer til kundene og registrere gjentakelsesomsetning. 

## <a name="register-revenue-with-a-recurring-general-journal"></a><a name="register-revenue-with-a-recurring-general-journal"></a>Registrere omsetning med en gjentakende finanskladd

En gjentakelseskladd er en finanskladd med spesifikke felt for håndtering av transaksjoner du bokfører ofte, med få eller ingen endringer, for eksempel leie, abonnementer, elektrisitet eller varme. Hvis du bruker disse feltene for gjentatte transaksjoner, kan du bokføre både faste og variable beløp. Når kladden er en gjentakelseskladd, trenger du bare å fylle ut feltene som skal bokføres jevnlig, én gang. Det vil si at kontiene, dimensjonene og dimensjonsverdiene og så videre som du angir, forblir i kladden etter bokføring. Hvis eventuelle justeringer er nødvendig, kan du gjøre det ved hver bokføring.

### <a name="why-use-this-option"></a><a name="why-use-this-option"></a>Hvorfor bruke dette alternativet

Med dette alternativet kan du definere fleksible faktureringsperioder med [datoformler](ui-enter-date-ranges.md#use-date-formulas).

Med dette alternativet kan du imidlertid ikke skrive ut og sende fakturaer i standardversjonen av [!INCLUDE[prod_short](includes/prod_short.md)].  

Hvis du vil ha mer informasjon, kan du se [Arbeid med gjentakelseskladder](ui-work-general-journals.md#work-with-recurring-journals).  

## <a name="create-multiple-invoices-based-on-a-recurring-job-journal"></a><a name="create-multiple-invoices-based-on-a-recurring-job-journal"></a>Opprette flere fakturaer basert på en gjentakende prosjektkladd

Den gjentakende prosjektkladden er et mer avansert alternativ til finanskladden. Du kan definere varer, ressurser og finanskonti, som skal gjentas for hvert prosjekt, og du angir hyppigheten for regelmessighet.  

Når du har bokført en gjentakende prosjektkladd, kan du opprette flere fakturaer med **Opprett salgsfaktura for prosjekt**. Du kan gå gjennom og bokføre opprettede fakturaer på **Salgsfakturaer**-siden.

### <a name="why-use-this-option-1"></a><a name="why-use-this-option-1"></a>Hvorfor bruke dette alternativet

Med dette alternativet følger du standard faktureringsprosedyre med alle fordelene med dette, inkludert standard- og kundeoppsett for kommunikasjonsinnstillinger. Du kan også definere priser for hvert enkelt prosjekt individuelt.

For hver ny kunde må du imidlertid opprette et nytt prosjekt og legge til linjer i gjentakelseskladden. 

Hvis du vil ha mer informasjon, kan du se [Opprette prosjektkladdelinjer](projects-how-record-job-usage.md#to-create-job-journal-lines-manually) og [Opprette flere salgsfakturaer for prosjekt](projects-how-invoice-jobs.md#to-create-multiple-job-sales-invoices).

## <a name="create-multiple-invoices-based-on-recurring-sales-lines"></a><a name="create-multiple-invoices-based-on-recurring-sales-lines"></a>Opprette flere fakturaer basert på gjentakende salgslinjer

Hvis du ofte må opprette salgs- og kjøpslinjer med lignende informasjon, kan du definere gjentakende salgslinjer du deretter kan sette inn på gjentakende salgs- og kjøpsdokumenter, for eksempel for gjentakende etterfyllingsordrer. Bruk kjørselen **Opprett gjentakende salgsfakturaer** til å opprette salgsfakturaer i henhold til gjentakende salgslinjer som er tilordnet til kundene, og med bokføringsdatoer innenfor gyldig-fra- og gyldig til-datoer du angir på gjentakende salgslinjer.  

### <a name="why-use-this-option-2"></a><a name="why-use-this-option-2"></a>Hvorfor bruke dette alternativet

Med dette alternativet kan du tilordne de samme gjentakelseslinjene til flere kunder. Du kan definere gyldighetsperioden for gjentakende salgslinjer for en bestemt kunde. Du kan tilordne flere gjentakelseslinjer til samme kunde, og alle blir tatt med i fakturaen.

Det er imidlertid ingen måte å definere faste priser for varer på fordi [!INCLUDE[prod_short](includes/prod_short.md)] vil bruke de faktiske prisene og den gyldige rabatt på bilagsdatoen og prøve å finne den beste kombinasjonen som gir den laveste prisen.  

Hvis du vil ha mer informasjon, kan du se [Opprette gjentakende salgs- og kjøpslinjer](sales-how-work-standard-lines.md).

## <a name="recurring-invoices-with-service-contract"></a><a name="recurring-invoices-with-service-contract"></a>Gjentakende fakturaer med servicekontrakt

En servicekontrakt inneholder servicekontraktavtalene mellom kundene og selskapet. En servicekontrakt omfatter servicenivåavtaler og servicevarene som du vedlikeholder som en del av kontrakten.  

Du kan definere startdatoen for kontrakten, fakturaperioden, om kontrakten er forhåndsbetalt eller ikke, prisoppdateringsspesifikasjoner hvis du har tenkt å endre priser mens kontrakten er aktiv. Du kan bruke både servicevarer eller varer i servicekontraktlinjer.
Du kan opprette kontraktmaler for å definere hvordan du oppretter bestemte typer kontrakter.  

### <a name="why-use-this-option-3"></a><a name="why-use-this-option-3"></a>Hvorfor bruke dette alternativet

Med dette alternativet kan du bruke en del av den avanserte servicestyringsfunksjonaliteten som ikke er begrenset til å utstede gjentakende fakturaer, men som har støtte for verksteds- og feltserviceoperasjoner.

Dette alternativet krever imidlertid Premium-lisens. Det kan hende at konfigurasjon av servicestyring og -vedlikehold ikke gir store fordeler i enklere abonnementsscenarioer.  

Hvis du vil ha mer informasjon, kan du se [Arbeide med servicekontrakter og servicekontrakttilbud](service-how-to-create-service-contracts-and-service-contract-quotes.md) og [Fakturere flere servicekontrakter](service-how-create-invoices.md#to-invoice-several-service-contracts).

## <a name="related-features"></a><a name="related-features"></a>Relaterte funksjoner
Det finnes flere relaterte funksjoner i [!INCLUDE[prod_short](includes/prod_short.md)].

### <a name="blanket-sales-orders"></a><a name="blanket-sales-orders"></a>Rammeordrer

En rammeordre utgjør rammene for en langsiktig avtale mellom selskapet og kunden.
En rammeordre opprettes som regel når en kunde har forpliktet seg til å kjøpe store antall som skal leveres i flere mindre leveringer over en bestemt tidsperiode. Rammeordrer dekker ofte bare én vare med forhåndsbestemte leveringsdatoer. Hovedgrunnen til å bruke en rammeordre i stedet for en salgsordre er at antallene som angis på en rammeordre ikke påvirker tilgjengeligheten, men den kan brukes til planleggingsformål.

#### <a name="why-use-this-option-4"></a><a name="why-use-this-option-4"></a>Hvorfor bruke dette alternativet

Med dette alternativet bruker du forventet behov, slik at informasjonen vurderes i de vanlige planleggingsrutinene. Hvis du vil ha mer informasjon, kan du se [Behovsprognoser og rammeordrer](design-details-central-concepts-of-the-planning-system.md#demand-forecasts-and-blanket-orders).  

Standardversjonen har imidlertid ingen standard mulighet til å behandle flere rammeordrer gruppevis.

Hvis du vil ha mer informasjon, kan du se [Arbeide med rammeordrer](sales-how-to-create-blanket-sales-orders.md).

### <a name="recurring-orders-norway"></a><a name="recurring-orders-norway"></a>Gjentakelsesordrer (Norge)

Du kan bruke gjentakelsesordrer til å opprette rammeordremaler slik at salgsordrer kan opprettes basert på datointervallene du definerer. Hvis du for eksempel leverer den samme salgsordren annenhver uke, kan du bruke en rammeordre til å opprette gjentakelsesordrer.
Du kan bruke gjentakelsesordrer til å definere en rekke parametere som viser hvordan du oppretter ordrene. Disse gruppene knyttes til rammeordrer som skal opprettes jevnlig. For å opprette gjentakelsesordrer, må du kjøre prosessen med å opprette gjentakelsesordrer med jevne mellomrom. 

#### <a name="why-use-this-option-5"></a><a name="why-use-this-option-5"></a>Hvorfor bruke dette alternativet

Med dette alternativet kan du velge mellom faste og beste priser.

Dette alternativet er imidlertid bare tilgjengelig i Norge. Gyldighetsperioden kan defineres på gjentakende gruppenivå.

Hvis du vil ha mer informasjon, kan du se [Gjentakelsesordrer](LocalFunctionality/Norway/recurring-orders.md).

### <a name="recurring-revenue-and-subscription-billing-by-other-providers"></a><a name="recurring-revenue-and-subscription-billing-by-other-providers"></a>Gjentakelsesomsetning og abonnementsfakturering av andre leverandører

På [AppSource.microsoft.com](https://appsource.microsoft.com/) kan du få utvidelser for Business Central. Noen utvidelser leveres av Microsoft, og andre utvidelser leveres av andre selskaper. Listen over utvidelser fra andre selskaper, vokser hver måned. Så følg med på [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646), og få apper som kan hjelpe deg med arbeidet i Business Central.  

## <a name="see-also"></a><a name="see-also"></a>Se også

[Datoformler](ui-enter-date-ranges.md#use-date-formulas)  
[Arbeid med gjentakelseskladder](ui-work-general-journals.md#work-with-recurring-journals)  
[Opprett prosjektkladdelinjer](projects-how-record-job-usage.md#to-create-job-journal-lines-manually)  
[Opprette flere salgsfakturaer for prosjekt](projects-how-invoice-jobs.md#to-create-multiple-job-sales-invoices)  
[Opprette gjentakende salgs- og kjøpslinjer](sales-how-work-standard-lines.md)  
[Arbeide med servicekontrakter og servicekontrakttilbud](service-how-to-create-service-contracts-and-service-contract-quotes.md)  
[Fakturere flere servicekontrakter](service-how-create-invoices.md#to-invoice-several-service-contracts)  
[Behovsprognoser og rammeordrer](design-details-central-concepts-of-the-planning-system.md#demand-forecasts-and-blanket-orders)  
[Arbeide med rammeordrer](sales-how-to-create-blanket-sales-orders.md)  
[Gjentakelsesordrer (Norge)](LocalFunctionality/Norway/recurring-orders.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
