---
title: Designdetaljer – Inngående lagerflyt
description: 'Lær hvordan du mottar varer på lageret, og registrer og match dem med inngående kildedokumenter.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: warehouse
ms.date: 09/18/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="design-details-inbound-warehouse-flow"></a>Designdetaljer: Inngående lagerflyt

Den inngående flyten på et lager begynner når varene ankommer på lageret på selskapslokasjonen, enten de mottas fra eksterne kilder eller fra en annen selskapslokasjon. Du kan motta fysiske varer og varer som ikke er lagervarer. Hvis du vil vite mer om mottak av ikke-lagervarer, kan du gå til [Bokføre ikke-lagervarer](#post-non-inventory-items).

I prinsippet består mottaksprosessen av inngående ordrer av to aktiviteter:

* Motta varer på i mottakssonen, identifiserer dem, samsvare dem med et kildedokument og registrere det mottatte antallet.
* Plasser varer på lager, og registrer stedet du plasserer dem på.

Kildedokumentene for inngående lagerflyt er:

* Bestillinger  
* Inngående overføringsordrer  
* Ordrereturer  

> [!NOTE]
> Produksjons- og monteringsutdata representerer også inngående kildedokumenter. Finn ut mer om håndtering av produksjons- og monteringsutdata for interne prosesser under [Designdetaljer: Interne lagerflyter](design-details-internal-warehouse-flows.md).  

I [!INCLUDE[prod_short](includes/prod_short.md)] mottar du varer og plasserer dem ved å bruke en av fire metoder, som beskrevet i tabellen nedenfor.

|Prinsipp|Inngående prosess|Krev kvitteringer|Krev plasseringer|Kompleksitetsnivå (Finn ut mer under [Oversikt over Warehouse Management](design-details-warehouse-management.md))|  
|------------|---------------------|--------------|----------------|------------|  
|A|Bokføre mottak og plassering fra ordrelinjen|||Ingen dedikert lageraktivitet.|  
|B|Bokføre mottak og plassering fra et lagerplasseringsdokument||Slått på|Grunnleggende: ordre for ordre.|  
|U|Bokføre mottak og plassering fra et lagermottaksdokument|Slått på||Grunnleggende: konsolidert mottak/levering for flere ordrer.|  
|D|Bokføre mottak fra et lagermottaksdokument og bokføre plassering fra et lagerplasseringsdokument|Slått på|Slått på|Avansert|  

Hvilken metode som er aktuell å velge, avhenger av selskapets vanlige praksis og organisasjonens kompleksitet. Nedenfor følger noen eksempler som kan hjelpe deg med å bestemme.

* I et lagringsmiljø for ordre for ordre, der mesteparten av lagerpersonellet arbeider direkte med ordredokumenter, kan det hende du bestemmer deg for å bruke metode A. 
* Et ordre for ordre-lager som har en mer komplisert plasseringsprosess, eller der lagerpersonell skiller plasseringsaktivitetene fra ordredokumentet, kan bruke metode B.
* Selskaper som trenger å planlegge håndteringen av flere ordrer, kan finne det nyttig å bruke lagermottaksdokumenter, metode C og D.  

I metode A, B og C kombineres mottak og plassering i ett trinn når dokumenter bokføres som mottatt. I metode D blir mottaket bokført først for å registrere lagerøkningen og at varer er tilgjengelige for salg. Lagermedarbeideren registrerer deretter plasseringen for å gjøre varene tilgjengelige for utgående ordrer. 

> [!NOTE]
> Selv om lagerplasseringer og lagerplasseringer høres ut, er de forskjellige dokumenter og brukes i forskjellige prosesser.
> * Lagerplasseringen som brukes i metode B sammen med informasjon om plasseringsinformasjon, bokfører også mottaket av kildedokumentet.
> * Lagerplasseringen som brukes i metode D, kan ikke bokføres, og den registrerer bare plasseringen. Registreringen gjør varene tilgjengelig for videre behandling, men bokfører mottaket. I inngående flyt krever lagerplasseringen et lagermottak.

## <a name="no-dedicated-warehouse-activity"></a>Ingen dedikert lageraktivitet

Følgende artikler inneholder informasjon om hvordan du behandler mottak for kildedokumenter hvis du ikke har egne lageraktiviteter.

* [Registrere kjøp](purchasing-how-record-purchases.md)
* [Overføringsordrer](inventory-how-transfer-between-locations.md)
* [Behandle ordrereturer](sales-how-process-sales-returns-orders.md)

## <a name="basic-warehouse-configurations"></a>Enkle lageroppsett

I et enkle lageroppsett er alternativet **Krever plassering aktivert**, men **Krev mottak** er slått av på siden **Lokasjonskort** for lokasjonen.

Diagrammet nedenfor illustrerer inngående lagerflyter etter dokumenttype i grunnleggende lagerkonfigurasjoner. Tallene i diagrammet svarer til trinnene nedenfor diagrammet.  

:::image type="content" source="media/design_details_warehouse_management_inbound_basic_flow.png" alt-text="Enkel inngående flyt i et lager.":::

### <a name="1-release-a-source-document-to-create-a-request-for-an-inventory-put-away"></a>1: Frigi et kildedokument for å opprette en forespørsel om en lagerplassering

Når du mottar varer, frigir du kildedokumentet, for eksempel en bestilling eller en inngående overføringsordre. Når du frigir dokumentet, blir varene tilgjengelige for plassering. Du kan også opprette lagerplasseringsdokumenter for enkelte ordrelinjene med en push-metode, basert på hyller og antall som skal håndteres.  

### <a name="2-create-an-inventory-put-away"></a>2: Opprett en lagerplassering

På siden **Lagerplassering** kan du hente de ventende kildedokumentlinjene basert på inngående lagerforespørsler. Ved hjelp av send kan du også opprette lagerplasseringslinjer når du oppretter kildedokumentet.  

### <a name="3-post-an-inventory-put-away"></a>3: Bokfør en lagerplassering

På hver linje for varer som er plassert, helt eller delvis, fyller du ut feltet **Antall** og bokfører deretter lagerplasseringen. Kildedokumenter som er knyttet til lagerplasseringen, bokføres som mottatt.  

* Det blir opprettet positive vareposter.
* Lagerposter opprettes for lokasjoner som krever en hyllekode for alle varetransaksjoner.
* Plasseringsforespørselen slettes hvis den er fullstendig håndtert. Eksempel: Feltet **Mottatt (antall)** i den inngående kildedokumentlinjen oppdateres.
* Det opprettes et postert mottaksdokument som for eksempel gjenspeiler bestillingen og de mottatte varene.  

## <a name="advanced-warehouse-configurations"></a>Avanserte lageroppsett

For å bruke avansert lageroppsett slår du på vekslebryteren **Krev mottak** på siden Lokasjonskort for lokasjonen. Veksleknappen **Krev plassering** er valg fri.

Diagrammet nedenfor illustrerer inngående lagerflyter etter dokumenttype. Tallene i diagrammet svarer til trinnene nedenfor diagrammet.  

:::image type="content" source="media/design_details_warehouse_management_inbound_advanced_flow.png" alt-text="Den avanserte inngående flyt i et lager.":::

### <a name="1-release-the-source-document"></a>1: Frigi kildedokumentet

Når du mottar varer, frigir du kildedokumentet, for eksempel bestillingen eller en inngående overføringsordre. Når du frigir dokumentet, blir varene tilgjengelige for plassering. Plasseringen inneholder referanser til kildedokumenttype og -nummer.

### <a name="2-create-a-warehouse-receipt"></a>2: Opprett et lagermottak

Hent de inngående kildedokumentlinjene på siden **Lagermottak**. Du kan kombinere flere kildedokumentlinjer i ett lagermottaksdokument. Fyll ut feltet **Ant. som skal håndt.** og velg om nødvendig mottakssonen og hyllen.  

### <a name="3-post-the-warehouse-receipt"></a>3: Bokfør lagermottaket

Bokfør lagermottak for å opprette positive vareposter. Feltet **Mottatt (antall)** i den inngående kildedokumentlinjen oppdateres.  

Hvis veksleknappen **Krev plassering** er slått på på lokasjonskortet, er dette der prosessen stopper. Ellers gjør bokføring av det inngående kildedokumentet at varene blir tilgjengelige for plassering. Plasseringen inneholder referanser til kildedokumenttype og -nummer.  

### <a name="4-optional-generate-put-away-worksheet-lines"></a>4: (Valgfritt) Generer plasseringsforslagslinjer

Hent lagerplasseringslinjer i **Plasseringsforslaget** basert på bokførte lagermottak eller operasjoner som produserer avgang. På linjene som skal plasseres, angi følgende informasjon:

* Hyllen som varene skal hentes fra.
* Hyllene varene skal plasseres i.
* Antall enheter som skal håndteres.

Hyllene kan være forhåndsdefinert av definisjonen av lagerlokasjonen eller ressursen som utførte operasjonen.  

Når alle plasseringer er planlagt og tilordnet til lagermedarbeidere, genereres lagerplasseringsdokumentene. Fullstendig tildelte plasseringslinjer blir slettet fra **plasseringsforslaget**.  

> [!NOTE]  
> Hvis veksleknappen **Bruk plasseringsforslag** ikke er slått på på lokasjonskortet, blir lagerplasseringsdokumenter opprettet direkte basert på bokførte lagermottak. I dette tilfellet er ikke dette trinnet nødvendig.  

### <a name="5-create-a-warehouse-put-away-document"></a>5: Opprett et lagerplasseringsdokument

Opprett et lagerplasseringsdokument i en hentemåte, basert på det bokførte lagermottaket. Opprett lagerplasseringsdokumentet og tildel det til en lagermedarbeider med en push-metode.  

### <a name="6-register-a-warehouse-put-away"></a>6: Registrer en lagerplassering

På hver linje for varer som er plassert, helt eller delvis, fyller du ut feltet **Antall** på siden **Plassering**, og registrerer deretter plasseringen.  

* Lagerposter opprettes for lokasjoner som krever en hyllekode for alle varetransaksjoner.
* Lagerplasseringslinjene slettes hvis de er fullstendig håndtert.
* Lagerplasseringsdokumentet holdes åpent til hele antallet for det tilknyttede bokførte lagermottaket er registrert.
* Feltet **Plassert ant.** på bokførte lagermottaksordrelinjer oppdateres.

## <a name="related-tasks"></a>Beslektede oppgaver

Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til artiklene som beskriver dem.

|**Hvis du vil**|**Se**|  
|------------|-------------|  
|Motta varer på lagerlokasjoner med et lagermottak for helt eller delvis automatisert lagerbehandling.|[Motta varer](warehouse-how-receive-items.md)|
|Plasser varer bestilling for bestilling, og bokfør mottaket i én aktivitet, i et grunnleggende lageroppsett.|[Plassere varer med lagerplasseringer](warehouse-how-to-put-items-away-with-inventory-put-aways.md)|  
|Plasser varer som mottas fra flere kjøp, salgsreturer, overføringsordrer i et avansert lageroppsett.|[Plasser varer med lagerplasseringer](warehouse-how-to-put-items-away-with-warehouse-put-aways.md)|  

## <a name="post-non-inventory-items"></a>Bokfør ikke-lagervarer

[!INCLUDE [post-non-inventory-items](includes/post-non-inventory-items.md)]

## <a name="see-also"></a>Se også

[!INCLUDE[footer-include](includes/footer-banner.md)]
