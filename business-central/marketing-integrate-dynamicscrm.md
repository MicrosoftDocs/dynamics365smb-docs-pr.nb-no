---
title: Administrere kunder ved hjelp av Dynamics 365 Sales | Microsoft Docs
description: Du kan bruke Dynamics 365 Sales fra Business Central for å tilordne data og få sømløs integrasjon og synkronisering i kundeemne-til-kontanter-prosessen.
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: integration, synchronize, map, Sales
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 1e45a480e8fdcc508de8ac82a6d2860147d76cec
ms.sourcegitcommit: 877af26e3e4522ee234fbba606615e105ef3e90a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/28/2020
ms.locfileid: "2991787"
---
# <a name="using-dynamics-365-sales-from-business-central"></a>Bruke Dynamics 365 Sales fra Business Central
Hvis du bruker Dynamics 365 Sales for Customer Engagement, kan du dra nytte av sømløs integrering i kundeemne-til-kontanter-prosessen med [!INCLUDE[d365fin](includes/d365fin_md.md)] for serverdelaktiviteter som å behandle bestillinger, håndtering av lager og gjøre finansene.

Før du kan bruke integrasjonsfunksjonene, må du sette opp tilkoblingen og definere brukere i [!INCLUDE[crm_md](includes/crm_md.md)]. Hvis du vil ha mer informasjon, kan du se [Integrere med Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md).

> [!NOTE]
> Denne fremgangsmåten beskriver hvordan du integrerer elektroniske versjoner av [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hvis du vil ha informasjon om lokal konfigurasjon, kan du se [Klargjøre Dynamics 365 Sales for lokal integrasjon](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration).

Integrering av programmene lar deg få tilgang til data i Sales fra [!INCLUDE[d365fin](includes/d365fin_md.md)], og i noen tilfeller omvendt. Du kan arbeide med og synkronisere data som begge tjenester har til felles, for eksempel kunder, kontakter og salgsinformasjon, og holde dataene oppdaterte i begge programmene.  

Selgeren i Sales kan for eksempel bruke prislister fra [!INCLUDE[d365fin](includes/d365fin_md.md)] når de oppretter en salgsordre. Når de legger til varen på salgsordrelinjen i Sales, kan de se lagernivået (tilgjengelighet) av varen fra [!INCLUDE[d365fin](includes/d365fin_md.md)].

Og omvendt kan ordrebehandlere i [!INCLUDE[d365fin](includes/d365fin_md.md)] behandle ordrer som er automatisk eller manuelt overført fra salg. De kan for eksempel opprette og bokføre ordrelinjer for varer eller ressurser som ble angitt i Sales som katalogprodukter. Hvis du vil ha mer informasjon, kan du se [Håndtere ordredata](marketing-integrate-dynamicscrm.md#handling-sales-order-data).

> [!IMPORTANT]  
> [!INCLUDE[d365fin](includes/d365fin_md.md)] integreres bare med Dynamics 365 Sales. Andre programmer i Dynamics 365 som endrer standard arbeidsflyt eller datamodell i Sales, for eksempel Project Service Automation, kan bryte integrasjonen mellom [!INCLUDE[d365fin](includes/d365fin_md.md)] og Sales.

### <a name="coupling-records"></a>Koblingsposter
Assistert oppsett-veiledningen lar deg velge dataene som skal synkroiseres. Senere kan du også definere synkronisering for bestemte poster. Dette omtales som *kobling*. Du kan for eksempel koble en bestemt konto i Sales med en bestemt kunde i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Denne delen beskriver hva du må ta hensyn til når du kobler poster.

Hvis du for eksempel vil vise Sales-kontoer som kunder i [!INCLUDE[d365fin](includes/d365fin_md.md)], må du koble de to typene poster. For å gjøre det går du til **Kunder**-listesiden i [!INCLUDE[d365fin](includes/d365fin_md.md)] og bruker handlingen **Konfigurer kobling**. Deretter angir du hvilke [!INCLUDE[d365fin](includes/d365fin_md.md)]-kunder som skal samsvare med hvilke konti i Sales.

Du kan også opprette (og koble) en konto i Sales basert på, for eksempel, kundeposten i [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjelp av **Opprett konto i Dynamics 365 Sales**, eller omvendt, ved hjelp av **Opprett kunde i [!INCLUDE[d365fin](includes/d365fin_md.md)]**.

Når du oppretter kobling mellom to poster, kan du også manuelt be om at gjeldende post, for eksempel en kunde, vil bli overskrevet umiddelbart av kontodata fra Sales (eller fra [!INCLUDE[d365fin](includes/d365fin_md.md)]) ved hjelp av **Synkroniser nå**-handlingen. **Synkronisere nå**-handling som spør om overskriving av Sales- eller [!INCLUDE[d365fin](includes/d365fin_md.md)]-postdata.

I noen tilfeller må du koble enkelte datasett før andre datasett, som vist i følgende tabell.

|Data|Hva som skal kobles først|
|-----|----|
|Kunder og konti|Koble selgere med Sales-brukere|
|Varer og ressurser|Koble målenhet med Sales-enhetsgrupper|
|Varer og ressurspriser|Koble kundeprisgrupper med Sales-priser|

> [!NOTE]  
> Hvis prisene eller kundene bruker utenlandsk valuta, må du kontrollere at du kobler valutaer til Sales-transaksjonsvalutaer.

Sales-salgsordrer avhenger av informasjon som kunder, målenheter, valutaer, kundeprisgrupper og varer og/eller ressurser. For at integrasjonen med salgsordrer skal fungere, må du koble kunder, målenheter, valutaer, kundeprisgrupper og varer og/eller ressurser.

### <a name="fully-synchronizing-records"></a>Fullstendig synkronisering av oppføringer
På slutten av den assisterte oppsettguiden kan du velge **Kjør full synkronisering** for å starte synkronisering av alle [!INCLUDE[d365fin](includes/d365fin_md.md)]-poster med alle relaterte poster i Sales. På siden **Gjennomgang av full synkronisering for Dynamics 365 Sales** velger du **Start**-handlingen. Full synkronisering kan ta litt tid å utføre, men du kan fortsette å arbeide i [!INCLUDE[d365fin](includes/d365fin_md.md)] når den kjøres i bakgrunnen.

For å kontrollere fremdriften for individuelle prosjekter i en fullstendig synkronisering, velger du en oversikt for å vise detaljer, på siden **Gjennomgang av full synkronisering for Dynamics 365 Sales**. Oppdater siden for å oppdatere statusen under synkronisering.

Fra siden **Konfigurasjon for Microsoft Dynamics 365-tilkobling** kan du få detaljer om fullstendig synkronisering når som helst. Herfra kan du også åpne **Tilordninger for integreringstabell**-siden for å se detaljer om tabellene i [!INCLUDE[d365fin](includes/d365fin_md.md)] og i Sales som må synkroniseres.

## <a name="handling-sales-order-data"></a>Håndtere ordredata
Ordrer som personer sender i [!INCLUDE[crm_md](includes/crm_md.md)], blir automatisk overført til [!INCLUDE[d365fin](includes/d365fin_md.md)] hvis du merker av for **Opprett ordrer automatisk** på siden **Tilkoblingsoppsett for Microsoft Dynamics 365**.
Du kan eventuelt manuelt konvertere sendte ordrer fra [!INCLUDE[crm_md](includes/crm_md.md)] ved hjelp av handlingen **Opprett i [!INCLUDE[d365fin](includes/d365fin_md.md)]**-handlingen som er tilgjengelig på siden **Ordrer – Dynamics 365 for Sales**.
For slike ordrer blir **Navn**-feltet i den opprinnelige ordren overført og tilordnet feltet **Eksternt dokumentnummer** på ordren i [!INCLUDE[d365fin](includes/d365fin_md.md)].

Dette kan også fungere hvis den opprinnelige ordren inneholder produkter som ikke er i produktkatalogen, det vil si varer eller ressurser som ikke er registrert i en app. I så fall må du fylle ut feltene **Produkt som ikke er i produktkatalogen** og **Nummer på produktet som ikke er i produktkatalogen** på **Salgsoppsett**-siden, slik at alle slike ikke-registrerte produktsalg er tilordnet til en bestemt vare/ressurs for finansanalyse.

Hvis varebeskrivelsen i den opprinnelige ordren er lang, kan en ekstra ordrelinje av typen **Merknad** opprettes som har plass til hele teksten i ordren i [!INCLUDE[d365fin](includes/d365fin_md.md)].

Oppdateringer i ordrehodefelt, for eksempel Siste leveringsdato eller Ønsket leveringsdato, som er tilordnet i **Tilordninger for integreringstabell** for SALESORDER-ORDER, synkroniseres med jevne mellomrom til [!INCLUDE[crm_md](includes/crm_md.md)]. Prosesser som å frigi en ordre og levere eller fakturere en ordre, bokføres til ordretidslinjen i [!INCLUDE[crm_md](includes/crm_md.md)]. Hvis du vil ha mer informasjon, se [Innføring i aktivitetsfeeder](/dynamics365/customer-engagement/developer/introduction-activity-feeds).

> [!NOTE]  
> Periodisk synkronisering basert på **Tilordninger for integreringstabell** for SALESORDER-ORDER vil bare fungere når ordreintegrasjon er aktivert. Hvis du vil ha mer informasjon, kan du se [Koble til Dynamics 365 Sales](admin-how-to-set-up-a-dynamics-crm-connection.md). Bare ordrer som er opprettet fra sendte ordrer i [!INCLUDE[crm_md](includes/crm_md.md)], synkroniseres. Hvis du vil ha mer informasjon, se [Aktivere ordrebehandlingsintegrering](/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration).

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098170]

## <a name="handling-sales-quotes-data"></a>Håndtere tilbudsdata
Tilbud som aktiveres i [!INCLUDE[crm_md](includes/crm_md.md)], blir overført til [!INCLUDE[d365fin](includes/d365fin_md.md)] hvis du merker av for **Behandle tilbud automatisk** på siden **Tilkoblingsoppsett for Microsoft Dynamics 365**.
Du kan eventuelt manuelt konvertere aktiverte tilbud fra [!INCLUDE[crm_md](includes/crm_md.md)] ved hjelp av handlingen **Behandle i [!INCLUDE[d365fin](includes/d365fin_md.md)]**-handlingen, som er tilgjengelig på siden **Tilbud – Dynamics 365 Sales**.
For slike tilbud blir **Navn**-feltet i det opprinnelige tilbudet overført og tilordnet feltet **Eksternt dokumentnummer** på ordren i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Også **Gjelder til**-feltet for tilbudet overføres og tilordnes til **Gyldig til-dato for tilbud**-feltet for tilbudet i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Tilbud går gjennom mange revisjoner når de ferdigstilles. Både manuell og automatisk behandling av tilbud i [!INCLUDE[d365fin](includes/d365fin_md.md)] sikrer at tidligere versjoner av tilbud arkiveres før behandling av nye revisjoner av tilbud fra [!INCLUDE[crm_md](includes/crm_md.md)].

## <a name="handling-posted-sales-invoices-customer-payments-and-statistics"></a>Håndtere bokførte salgsfakturaer, kundebetalinger og statistikk
Når du har fullført ordre, opprettes fakturaer for den. Når du fakturerer ordre, kan du overføre den bokførte salgsfakturaen til [!INCLUDE[crm_md](includes/crm_md.md)] hvis du velger **Opprett faktura i [!INCLUDE[crm_md](includes/crm_md.md)]**-avmerkingsboksen på siden **Bokført salgsfaktura**. Bokførte fakturaer overføres til [!INCLUDE[crm_md](includes/crm_md.md)] med statusen **Fakturert**.

Når kundebetalingen er mottatt for salgsfakturaen i [!INCLUDE[d365fin](includes/d365fin_md.md)], endres salgsfakturastatusen til **Betalt** med **Statusårsak**-feltet satt til **Delvis**, hvis delvis betalt, eller **Fullstendig** hvis fullstendig betalt, når du velger **Oppdater kontostatistikk**-handlingen på kundesiden i [!INCLUDE[d365fin](includes/d365fin_md.md)]. **Oppdater kontostatistikk**-funksjonen oppdaterer også verdier, for eksempel feltene **Saldo** og **Totalt salg** i **[!INCLUDE[d365fin](includes/d365fin_md.md)]-kontostatistikk**-faktaboksen i [!INCLUDE[crm_md](includes/crm_md.md)]. Alternativt kan du la de planlagte jobbene, kundestatistikken og POSTEDSALESINV-INV kjøre begge disse prosessene automatisk i bakgrunnen.

## <a name="see-also"></a>Se også
[Integrere med Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Forbindelser](marketing-relationship-management.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Endre hvilke funksjoner som vises](ui-experiences.md)  
[Tilordne tillatelser til brukere og grupper](ui-define-granular-permissions.md)    
[Oversikt over salg og salgshub](/dynamics365/customer-engagement/sales-enterprise/overview)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
