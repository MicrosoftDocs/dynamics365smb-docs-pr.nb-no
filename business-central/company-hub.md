---
title: Administrere arbeid på tvers av flere selskaper i selskapshuben
description: Lær om selskapshuben i Dynamics 365 Business Central som du bruker til å håndtere arbeidet i flere selskaper.
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'accountant, accounting, financial report'
ms.search.form: '1151, 1154, 1165, 1166'
ms.date: 04/01/2021
ms.author: bholtorf
---

# <a name="manage-work-across-multiple-companies-in-the-company-hub"></a>Administrere arbeid på tvers av flere selskaper i selskapshuben

Noen personer arbeider i flere selskaper i [!INCLUDE [prod_short](includes/prod_short.md)], og noen arbeider også i mer enn én organisasjon, for eksempel eksterne regnskapsførere eller ansatte og ledere i selskaper med flere datterselskaper. For disse brukerne, og mange andre, fungerer firmahuben som en målside som gir en økonomisk oversikt over selskaper og miljøer. Den gir brukerne et verktøy for å administrere arbeid på tvers av de forskjellige miljøene de arbeider i, på tvers av selskaper, miljøer og områder.  

Du får tilgang til selskapshuben ved å bytte til **Selskapshub**-rollen i Mine innstillinger eller ved å åpne **Selskapshub**-siden direkte. Du kan gjøre samme arbeid på begge steder, men handlingene er plassert litt forskjellig på menyene.  

[![Viser siden for selskapssenteret som viser alle selskaper.](media/company-hub.png)](media/company-hub.png#lightbox)  

> [!NOTE]
> Du kan koble selskapssenteret til så mange selskaper du vil. Du kan imidlertid bare koble selskapssenteret til selskaper som er driftet i [!INCLUDE [prod_short](includes/prod_short.md)] på nett.

## <a name="company-hub-home-page"></a>Hjemmeside for selskapshub

Hvis du bruker rollen **Selskapshub**, viser hjemmesiden en liste over selskaper du har tilgang til, inkludert informasjon om interessepunktdata (KPI), og koblinger for å åpne hvert enkelt selskap. <!--You can customize the dashboard to show the data points that you want to see by adding or removing columns. For example, you might want to see taxes that are due, how many open sales documents each company has, or the number of purchase invoices that are due next week. You can configure the view to suit your needs. If you have added many companies, you can use filters to sort your view.--> Velg **Selskapshub**-handlingen for å åpne selskapshuben, der du kan arbeide nærmere med hvert selskap.  

> [!TIP]
> Hvis du vil ha tilgang til et bestemt selskap i [!INCLUDE [prod_short](includes/prod_short.md)], velger du navnet på selskapet eller velger menyelementet **Gå til selskap**, og du logges inn automatisk i en ny nettleserkategori.

:::image type="content" source="media/company-hub-company-list-actions.png" alt-text="Handlinger for et selskap som er oppført i selskapshuben.":::

Du kan legge til nye selskaper, for eksempel når du får en ny klient, eller når bedriften legger til et nytt datterselskap. Hvis du vil ha mer informasjon, kan du se [Legge til selskaper i selskapshuben](company-hub-add-company.md).  

> [!TIP]
> Hvis du vil oppdatere dataene i selskapshuben, må du ha tilgang til dataene i selskapene som dataene kommer fra.

<!--## Company details

In the **Company Hub** page, you can see more information about each company by choosing the name of the company that you want to learn more about. This opens the **Company Details** pane, where you can see additional information, such as the following:  

* Cash account balances  
* Cash flow forecast  
* Overdue purchase invoices  
* Overdue sales invoices  

> [!TIP]
> You can launch predefined Excel workbooks from the **Reports** tab in the ribbon. These Excel workbooks are designed as ready-to-print key financial statements and reports, but you can also modify them to fit your needs. For more information, see [Analyzing Financial Statements in Microsoft Excel](finance-analyze-excel.md).  

Otherwise, close the details pane and continue to the next company.  -->

## <a name="assigned-tasks"></a>Tilordnede oppgaver

I [!INCLUDE [prod_short](includes/prod_short.md)] kan du tilordne oppgaver til deg selv og andre, og andre kan tilordne oppgaver til deg. Selskapshuben gir deg en oversikt over tilordnede oppgaver for hvert selskap, og du får også tilgang til en oversikt over alle tilordnede oppgaver ved å velge **Mine brukeroppgaver** på **Start**-siden.  

<!--In the client company, you also have cues that call out tasks assigned to you in this particular client.  -->

### <a name="my-user-tasks"></a>Mine brukeroppgaver

**Mine brukeroppgaver**-listen hjelper deg med å prioritere dagen ved å vise mer informasjon om oppgaver som er tilordnet til deg, for alle selskapene dine.  

Du kan sortere etter forfallsdato, for eksempel, eller andre typer data som hjelper deg med å prioritere dagen. Oversikten viser alle aktiviteter som er tilordnet til deg, som standard, men du kan definere filtre for bare å vise oppgaver som for eksempel er merket med høy prioritet.  

For å plukke opp en oppgave, velger du den fra listen over ventende brukeroppgaver. I båndet åpner **Gå til oppgaveelement**-koblingen siden der du kan gjøre oppgaven.  

Når du har fullført en oppgave, merker du den som fullført.  

Hvis du vil ha mer informasjon om selskaper og miljøer, kan du se [Miljøkoblinger](company-hub-add-company.md#environment-links).  

## <a name="access-the-company-hub"></a>Tilgang til selskapshuben

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

For å få tilgang til selskapshuben må du ha tilgang via enten brukergruppen *D365-SELSKAPSHUB* eller via tillatelsessettet *D365-SELSKAPSHUB*. Du må også ha tilgang til selskapene som er oppført i firmahuben, noe som betyr at du må være en bruker i disse selskapene. Hvis du vil ha mer informasjon, se [Opprette brukere i henhold til lisenser](ui-how-users-permissions.md).  

> [!IMPORTANT]
> Selskapshuben er en liste over hele bedriften, så alle brukere som har tilgang til selskapshuben, kan se alle selskaper i sin egen [!INCLUDE [prod_short](includes/prod_short.md)]-leietaker, og alle KPI-er for selskapene de har tilgang til.

Hvis du ikke finner selskapshuben, og du vet at du har fått tilgang til den, kan du kontakte systemansvarlig hvis selskapshuben er oppført på siden **Administrasjon av utvidelse**. Hvis du vil ha mer informasjon, kan du se [Tilpasse Business Central med utvidelser](ui-extensions.md).  

## <a name="set-up-the-company-hub"></a>Konfigurere selskapshuben

Når du skal begynne å bruke selskapshuben, må du legge til ett eller flere selskaper på instrumentbordet. Hvis du vil ha mer informasjon, kan du se [Legge til selskaper i selskapshuben](company-hub-add-company.md).  

Men hvis du vil legge til et selskap, må du ha fått tilgang til én eller flere forekomster av [!INCLUDE [prod_short](includes/prod_short.md)] i tillegg til selskapet som du bruker selskapshuben i.  

Hvis du for eksempel er regnskapsfører, kan klientene dine invitere deg til sine [!INCLUDE [prod_short](includes/prod_short.md)]. Hvis du vil ha mer informasjon, kan du se [Invitere den eksterne regnskapsføreren til Business Central](finance-accounting.md#inviteaccountant).  

Administratorer kan bruke samme assisterte oppsettsveiledning for å legge deg til i sine [!INCLUDE [prod_short](includes/prod_short.md)], eller de kan legge deg til i den relevante Azure AD-kontoen i administrasjonssenteret for Microsoft 365. Hvis du vil ha mer informasjon, kan du se [Administrere brukere og grupper](/microsoft-365/admin/add-users/?view=o365-worldwide&preserve-view=true).  

## <a name="see-also"></a>Se også

[Legge til selskaper i selskapshuben](company-hub-add-company.md)  
[Regnskapsføreropplevelser i Business Central](finance-accounting.md)  
[Utvidelsen Selskapshub for Business Central](ui-extensions-company-hub.md)  
[Endre grunnleggende innstillinger](ui-change-basic-settings.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
