---
title: Administrere kunder ved hjelp av Dynamics 365 Sales (inneholder video) | Microsoft Docs
description: Du kan bruke Dynamics 365 Sales fra Business Central med sømløs integrasjon og synkronisering i kundeemne-til-kontanter-prosessen.
documentationcenter: ''
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'integration, synchronize, map, Sales'
ms.search.forms: '9980, 5341, 5349, 5330, 1817, 5342, 5337, 5336, 5331, 5343, 5334, 5346, 5348, 5329, 5380, 5353, 5381, 5351, 5333, 5360, 5373, 5371, 5340, 5345, 5362, 1313, 5361, 1876, 5339, 5338, 5335, 5332, 6250'
ms.date: 09/16/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="use-dynamics-365-sales-from-business-central"></a>Bruk Dynamics 365 Sales fra Business Central
Hvis du bruker Dynamics 365 Sales for Customer Engagement, kan du dra nytte av sømløs integrering i kundeemne-til-kontanter-prosessen med [!INCLUDE[prod_short](includes/prod_short.md)] for serverdelaktiviteter som å behandle bestillinger, håndtering av lager og gjøre finansene.

Før du kan bruke integrasjonsfunksjonene, må systemansvarlig sette opp tilkoblingen og definere brukere i [!INCLUDE[crm_md](includes/crm_md.md)]. Hvis du vil ha mer informasjon, kan du se [Integrere med Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md).

> [!NOTE]
> Denne fremgangsmåten beskriver hvordan du integrerer elektroniske versjoner av [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[prod_short](includes/prod_short.md)]. Hvis du vil ha informasjon om lokal konfigurasjon, kan du se [Klargjøre Dynamics 365 Sales for lokal integrasjon](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration).

Integrering av programmene lar deg få tilgang til data i Sales fra [!INCLUDE[prod_short](includes/prod_short.md)], og i noen tilfeller omvendt. Du kan arbeide med og synkronisere data som begge tjenester har til felles, for eksempel kunder, kontakter og salgsinformasjon, og holde dataene oppdaterte i begge programmene.  

En selgeren i [!INCLUDE[crm_md](includes/crm_md.md)] kan for eksempel bruke prislister fra [!INCLUDE[prod_short](includes/prod_short.md)] når de oppretter en salgsordre. Når de legger til varen på salgsordrelinjen i [!INCLUDE[crm_md](includes/crm_md.md)], kan de se lagernivået (tilgjengelighet) av varen fra [!INCLUDE[prod_short](includes/prod_short.md)].

Og omvendt kan ordrebehandlere i [!INCLUDE[prod_short](includes/prod_short.md)] behandle ordrer som er automatisk eller manuelt overført fra [!INCLUDE[crm_md](includes/crm_md.md)]. De kan for eksempel opprette og bokføre ordrelinjer for varer eller ressurser som ble angitt i [!INCLUDE[crm_md](includes/crm_md.md)] som katalogprodukter. Hvis du vil ha mer informasjon, kan du se [Håndtere ordredata](marketing-integrate-dynamicscrm.md#handling-sales-order-data).

> [!IMPORTANT]  
> [!INCLUDE[prod_short](includes/prod_short.md)] integreres bare med [!INCLUDE[crm_md](includes/crm_md.md)]. Andre programmer i Dynamics 365 som endrer standard arbeidsflyt eller datamodell i [!INCLUDE[crm_md](includes/crm_md.md)], for eksempel Project Service Automation, kan bryte integrasjonen mellom [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE[crm_md](includes/crm_md.md)].

## <a name="coupling-records"></a>Koblingsposter
Assistert oppsett-veiledningen lar deg velge dataene som skal synkroiseres. Senere kan du også definere synkronisering for bestemte poster. Dette omtales som *kobling*. Du kan for eksempel koble en bestemt konto i [!INCLUDE[crm_md](includes/crm_md.md)] med en bestemt kunde i [!INCLUDE[prod_short](includes/prod_short.md)]. Denne delen beskriver hva du må ta hensyn til når du kobler poster.

Hvis du for eksempel vil vise kontoer i [!INCLUDE[crm_md](includes/crm_md.md)] som kunder i [!INCLUDE[prod_short](includes/prod_short.md)], må du koble to typer poster. For å gjøre det går du til **Kunder**-listesiden i [!INCLUDE[prod_short](includes/prod_short.md)] og bruker handlingen **Konfigurer kobling**. Deretter angir du hvilke [!INCLUDE[prod_short](includes/prod_short.md)]-kunder som skal samsvare med hvilke konti i [!INCLUDE[crm_md](includes/crm_md.md)].

Du kan også opprette (og koble) en konto i [!INCLUDE[crm_md](includes/crm_md.md)] basert på, for eksempel en kundepost i [!INCLUDE[prod_short](includes/prod_short.md)] ved hjelp av **Opprett konto i Dynamics 365 Sales**, eller omvendt, ved hjelp av **Opprett kunde i [!INCLUDE[prod_short](includes/prod_short.md)]**.

Når du oppretter kobling mellom to poster, kan du også manuelt be om at gjeldende post, for eksempel en kunde, vil bli overskrevet umiddelbart av kontodata fra Sales (eller fra [!INCLUDE[prod_short](includes/prod_short.md)]) ved hjelp av **Synkroniser nå**-handlingen. **Synkronisere nå**-handling som spør om overskriving av Sales- eller [!INCLUDE[prod_short](includes/prod_short.md)]-postdata.

I noen tilfeller må du koble enkelte datasett før andre datasett, som vist i følgende tabell.

|Data|Hva som skal kobles først|
|-----|----|
|Kunder og konti|Koble selgere med [!INCLUDE[crm_md](includes/crm_md.md)]-brukere|
|Varer og ressurser|Koble enheter med [!INCLUDE[crm_md](includes/crm_md.md)]-enhetsgrupper|
|Varer og ressurspriser|Koble kundeprisgrupper med [!INCLUDE[crm_md](includes/crm_md.md)]-priser|

> [!NOTE]  
> Hvis prisene eller kundene bruker utenlandsk valuta, må du kontrollere at du kobler valutaer til Sales-transaksjonsvalutaer.

I [!INCLUDE[crm_md](includes/crm_md.md)] avheger salgsordrer av informasjon som kunder, målenheter, valutaer, kundeprisgrupper og varer og/eller ressurser. For at integrasjonen med salgsordrer skal fungere, må du koble kunder, målenheter, valutaer, kundeprisgrupper og varer og/eller ressurser.

## <a name="fully-synchronizing-records"></a>Fullstendig synkronisering av oppføringer
På slutten av den assisterte oppsettguiden kan du velge handlingen **Kjør full synkronisering** for å starte synkronisering av alle [!INCLUDE[prod_short](includes/prod_short.md)]-poster med alle relaterte poster i [!INCLUDE[crm_md](includes/crm_md.md)]. På siden **Gjennomgang av full synkronisering for Dynamics 365 Sales** velger du **Start**-handlingen. Full synkronisering kan ta litt tid å utføre, men du kan fortsette å arbeide i [!INCLUDE[prod_short](includes/prod_short.md)] når den kjøres i bakgrunnen.

For å kontrollere fremdriften for individuelle prosjekter i en fullstendig synkronisering, velger du en oversikt for å vise detaljer, på siden **Gjennomgang av full synkronisering for Dynamics 365 Sales**. Oppdater siden for å oppdatere statusen under synkronisering.

Fra siden **Konfigurasjon for Microsoft Dynamics 365-tilkobling** kan du få detaljer om fullstendig synkronisering når som helst. Herfra kan du også åpne **Tilordninger for integreringstabell**-siden for å se detaljer om tabellene i [!INCLUDE[prod_short](includes/prod_short.md)] og i Sales som må synkroniseres.

## <a name="handling-sales-order-data"></a>Håndtere ordredata
Ordrer som personer sender i [!INCLUDE[crm_md](includes/crm_md.md)], blir automatisk overført til [!INCLUDE[prod_short](includes/prod_short.md)] hvis du merker av for **Opprett ordrer automatisk** på siden **Tilkoblingsoppsett for Microsoft Dynamics 365**.
Du kan eventuelt manuelt konvertere sendte ordrer fra [!INCLUDE[crm_md](includes/crm_md.md)] ved hjelp av handlingen **Opprett i [!INCLUDE[prod_short](includes/prod_short.md)]**-handlingen som er tilgjengelig på siden **Ordrer – Dynamics 365 for Sales**.
For slike ordrer blir **Navn**-feltet i den opprinnelige ordren overført og tilordnet feltet **Eksternt dokumentnummer** på ordren i [!INCLUDE[prod_short](includes/prod_short.md)].

Dette kan også fungere hvis den opprinnelige ordren inneholder produkter som ikke er i produktkatalogen, det vil si varer eller ressurser som ikke er registrert i en app. I så fall må du fylle ut feltene **Produkt som ikke er i produktkatalogen** og **Nummer på produktet som ikke er i produktkatalogen** på **Salgsoppsett**-siden, slik at salg for ikke-registrerte produkter er tilordnet til en bestemt vare eller ressurs.

> [!NOTE]
> Du kan ikke tilordne et produkt som ikke finnes i produktkatalogen, til en vare eller ressurs i [!INCLUDE[prod_short](includes/prod_short.md)] som er koblet til et produkt i [!INCLUDE[crm_md](includes/crm_md.md)]. For å tillate produkter som ikke er i produktkatalogen, anbefaler vi at du oppretter en vare eller ressurs spesielt for dette formålet og ikke kobler det med et produkt i [!INCLUDE[crm_md](includes/crm_md.md)]. 

Hvis varebeskrivelsen i den opprinnelige ordren er lang, kan en ekstra ordrelinje av typen **Merknad** opprettes som har plass til hele teksten i ordren i [!INCLUDE[prod_short](includes/prod_short.md)].

Oppdateringer av felt i salgsordrehoder, for eksempel feltene Siste leveringsdato eller Ønsket leveringsdato, som er tilordnet i integrasjonstabelltilordningen for **SALESORDER-ORDER**, synkroniseres med jevne mellomrom til [!INCLUDE[crm_md](includes/crm_md.md)]. Prosesser som å frigi en ordre, levere og fakturere en ordre, bokføres til ordretidslinjen i [!INCLUDE[crm_md](includes/crm_md.md)]. Hvis du vil ha mer informasjon, se [Innføring i aktivitetsfeeder](/dynamics365/sales-enterprise/manage-activities). Hvis du vil aktivere postering og aktiviteter for ordrer i [!INCLUDE[crm_md](includes/crm_md.md)], kan du se [Definer notatkontrollen for å få tilgang til informasjon om innlegg for en egendefinert enhet](/dynamics365/customerengagement/on-premises/customize/notes-control-legacy) i Customer Engagement-dokumentasjonen. Artikkelen viser til Customer Engagement on-premises, men trinnene er de samme for den nettbaserte versjonen. <!--The /dynamics365/sales-enterprise/developer/introduction-activity-feeds link was broken. Should this actually point to /dynamics365/sales-enterprise/manage-activities-->

> [!NOTE]  
> Periodisk synkronisering basert på integrasjonstabelltilordningen for **SALESORDER-ORDER** vil bare fungere når ordreintegrasjon er aktivert. Hvis du vil ha mer informasjon, kan du se [Tilkoblingsinnstillinger på siden for konfigurasjon av Sales-tilkobling](admin-prepare-dynamics-365-for-sales-for-integration.md). Bare ordrer som er opprettet fra sendte ordrer i [!INCLUDE[crm_md](includes/crm_md.md)], synkroniseres. Hvis du vil ha mer informasjon, se [Aktivere ordrebehandlingsintegrering](/dynamics365/sales-enterprise/developer/enable-sales-order-processing-integration).

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098170]

## <a name="handling-sales-quotes-data"></a>Håndtere tilbudsdata
Tilbud som aktiveres i [!INCLUDE[crm_md](includes/crm_md.md)], blir overført til [!INCLUDE[prod_short](includes/prod_short.md)] hvis du merker av for **Behandle tilbud automatisk** på siden **Tilkoblingsoppsett for Microsoft Dynamics 365**.
Du kan eventuelt manuelt konvertere aktiverte tilbud fra [!INCLUDE[crm_md](includes/crm_md.md)] ved hjelp av handlingen **Behandle i [!INCLUDE[prod_short](includes/prod_short.md)]**-handlingen, som er tilgjengelig på siden **Tilbud – Dynamics 365 Sales**.
For slike tilbud blir **Navn**-feltet i det opprinnelige tilbudet overført og tilordnet feltet **Eksternt dokumentnummer** på ordren i [!INCLUDE[prod_short](includes/prod_short.md)]. Også **Gjelder til**-feltet for tilbudet overføres og tilordnes til **Gyldig til-dato for tilbud**-feltet for tilbudet i [!INCLUDE[prod_short](includes/prod_short.md)].  

Tilbud går gjennom mange revisjoner når de ferdigstilles. Både manuell og automatisk behandling av tilbud i [!INCLUDE[prod_short](includes/prod_short.md)] sikrer at tidligere versjoner av tilbud arkiveres før behandling av nye revisjoner av tilbud fra [!INCLUDE[crm_md](includes/crm_md.md)].

Når du velger **Behandle** i [!INCLUDE[prod_short](includes/prod_short.md)] for et tilbud som har statusen **Vunnet**, opprettes en ordre i [!INCLUDE[prod_short](includes/prod_short.md)] bare hvis en tilsvarende ordre sendes i [!INCLUDE[crm_md](includes/crm_md.md)]. Ellers blir tilbudet bare frigitt i [!INCLUDE[prod_short](includes/prod_short.md)]. Hvis en tilsvarende ordre sendes i [!INCLUDE[crm_md](includes/crm_md.md)] senere, og det opprettes en ordre fra den, oppdateres **Tilbudsnr.** på ordren og tilbudet arkiveres.

## <a name="handling-posted-sales-invoices-customer-payments-and-statistics"></a>Håndtere bokførte salgsfakturaer, kundebetalinger og statistikk
Når du har fullført ordre, opprettes fakturaer for den. Når du fakturerer ordre, kan du overføre den bokførte salgsfakturaen til [!INCLUDE[crm_md](includes/crm_md.md)] hvis du velger **Opprett faktura i [!INCLUDE[crm_md](includes/crm_md.md)]**-avmerkingsboksen på siden **Bokført salgsfaktura**. Bokførte fakturaer overføres til [!INCLUDE[crm_md](includes/crm_md.md)] med statusen **Fakturert**.

Når kundebetalingen er mottatt for salgsfakturaen i [!INCLUDE[prod_short](includes/prod_short.md)], endres salgsfakturastatusen til **Betalt** med **Statusårsak**-feltet satt til **Delvis**, hvis delvis betalt, eller **Fullstendig** hvis fullstendig betalt, når du velger **Oppdater kontostatistikk**-handlingen på kundesiden i [!INCLUDE[prod_short](includes/prod_short.md)]. **Oppdater kontostatistikk**-funksjonen oppdaterer også verdier, for eksempel feltene **Saldo** og **Totalt salg** i **[!INCLUDE[prod_short](includes/prod_short.md)]-kontostatistikk**-faktaboksen i [!INCLUDE[crm_md](includes/crm_md.md)]. Alternativt kan du la de planlagte jobbene, kundestatistikken og POSTEDSALESINV-INV kjøre begge disse prosessene automatisk i bakgrunnen. 

## <a name="handling-sales-prices"></a>Håndtere salgspriser
> [!NOTE]
> I lanseringsbølge 2 i 2020 lanserte vi strømlinjeformede prosesser for å definere og håndtere priser og rabatter. Hvis du er en ny kunde som bruker denne versjonen, bruker du den nye opplevelsen. Hvis du er en eksisterende kunde, vil din bruk av den nye funksjonen avhenge av om administratoren har aktivert funksjonsoppdateringen **Ny salgsprisopplevelse** i **Funksjonsstyring**. Hvis du vil ha mer informasjon, kan du se [Aktivering av kommende funksjoner på forhånd](/dynamics365/business-central/dev-itpro/administration/feature-management).

Fremgangsmåten for å fullføre denne prosessen varierer avhengig av om administratoren har aktivert den nye prisopplevelsen. 

> [!NOTE]
> Hvis standard prissynkronisering ikke fungerer for deg, anbefaler vi at du bruker funksjoner for integreringstilpassing. Hvis du vil ha mer informasjon, kan du se [Tilpasse integrering med Microsoft Dataverse](/dynamics365/business-central/dev-itpro/administration/administration-custom-cds-integration).

#### [Nåværende opplevelse](#tab/current-experience/)
I gjeldende prisopplevelse synkroniserer [!INCLUDE[prod_short](includes/prod_short.md)] salgspriser som 

* Gjelder for alle kunder. Standard salgsprislister opprettes basert på prisen i **Enhetspris**-feltet på **Varekort**-siden for varene.
* Gjelder for en bestemt kundeprisgruppe. Dette kan for eksempel være salgspriser for detaljhandels- eller engroskundene. Gjør følgende for å synkronisere priser basert på en kundeprisgruppe:

    1. Koble sammen varene som kundeprisgruppen har angitt priser for.
    2. Koble sammen kundeprisgruppen på siden **Kundeprisgrupper** ved å velge **Relatert**, **Dynamics 365 Sales**, **Kobling** og deretter **Konfigurer kobling**. Koblingen oppretter en aktiv prisliste i [!INCLUDE[prod_short](includes/prod_short.md)] med same navn som kundeprisgruppen i [!INCLUDE[crm_md](includes/crm_md.md)] og synkroniserer automatisk alle varer som kundeprisgruppen definerer prisen for.

:::image type="content" source="media/customer-price-group.png" alt-text="Siden Kundeprisgruppe.":::

#### [Ny opplevelse](#tab/new-experience/)  

Den nye prisopplevelsen synkroniserer prislister som oppfyller følgende kriterier:

* **Tillat oppdatering av standarder** er deaktivert.
* Pristypen er Salg.
* Beløpstypen er Salg.
* Produkttypen på linjene må være Vare eller Ressurs. 
* Det er ikke angitt et minimumsantall.

[!INCLUDE[prod_short](includes/prod_short.md)] synkroniserer salgspriser som gjelder for alle kunder. Standard salgsprislister opprettes basert på prisen i **Enhetspris**-feltet på **Varekort**-siden for varene.

Du kan synkronisere prislister på siden **Salgsprisliste** ved å velge **Relatert**, **Dynamics 365 Sales**, **Kobling** og deretter **Konfigurer kobling**. 

:::image type="content" source="media/sales-price-list.png" alt-text="Siden Salgsprisliste.":::

---


## <a name="see-also"></a>Se også
[Integrere med Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Forbindelser](marketing-relationship-management.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Endre hvilke funksjoner som vises](ui-experiences.md)  
[Tildel tillatelser til brukere og grupper](ui-define-granular-permissions.md)    
[Oversikt over salg og salgshub](/dynamics365/customer-engagement/sales-enterprise/overview)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
