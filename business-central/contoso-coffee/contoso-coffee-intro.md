---
title: Innføring i demodata for Contoso Coffee
description: Oversikt over scenarioer for hvordan Contoso Coffee-demo data kan hjelpe deg å lære hvordan du bruker funksjonene i Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 4760
author: edupont04
ms.author: andreipa
---

# <a name="introduction-to-contoso-coffee-demo-data"></a><a name="introduction-to-contoso-coffee-demo-data"></a><a name="introduction-to-contoso-coffee-demo-data"></a>Innføring i demodata for Contoso Coffee

Contoso Coffee er et fiktivt selskap som produserer forbrukerkaffemaskiner og kommersielle kaffemaskiner. **Contoso Coffee**-appene for Business Central legger til demonstrasjonsdata som du kan bruke til å lære hvordan du bruker funksjonene i Business Central.  


## <a name="set-up-contoso-coffee-data"></a><a name="set-up-contoso-coffee-data"></a><a name="set-up-contoso-coffee-data"></a>Konfigurer Contoso Coffee-data

For å kunne bruke Contoso Coffee-data må du installere to apper i det aktuelle selskapet i [!INCLUDE [prod_short](../includes/prod_short.md)]:  

- **Demodatasett for Contoso Coffee**  

    Denne appen inneholder demonstrasjonsdata for basisprogrammet.  
- **Demodatasett for Contoso Coffee (land-ID)**  

    Denne appen legger til landspesifikt innhold oppå basisprogrammet.

Legg til appene i et tomt selskap i et betalt abonnement eller som en del av en prøveversjon. Opprett for eksempel et nytt selskap uten eksempeldata fra den assisterte veiledningen **Opprett nytt selskap** som du kan åpne fra **Selskaper**-oversikten. Deretter legger du til appene fra [markedsplassen](../ui-extensions-install-uninstall.md#install), hvis de ikke allerede er oppført på siden **Utvidelsesbehandling**-side.  

Deretter bør du fullføre:
 - [Produksjonsoppsettet](manufacturing/contoso-coffee-manufacturing-intro.md) som skal forberedes for bruk av [produksjonsscenarioer](#manufacturing-scenarios)
 - [Lageroppsettet](warehousing/contoso-coffee-warehousing-intro.md) som skal forberedes for bruk av [lagerscenarioer](#warehousing-scenarios)

## <a name="manufacturing-scenarios"></a><a name="manufacturing-scenarios"></a><a name="manufacturing-scenarios"></a>Produksjonsscenarioer

Demodata for Contoso Coffee støtter nå følgende produksjonsscenarioer for test og opplæring:

1. [Opprett en ny produksjonsstykkliste og stykklisteversjon](manufacturing/create-new-production-bom-version.md)  
2. [Opprett en ny rute](manufacturing/create-new-routing.md)  
3. [Opprett en fast planlagt produksjonsordre og endre den](manufacturing/create-firm-planned-production-order-change.md)  
4. [Kombiner automatisk og manuell trekking](manufacturing/combine-automatic-manual-flushing.md)  
5. [Bruk ordreplanlegging til å opprette og reservere forsyning](manufacturing/order-planning-create-reserve-supply.md)  
6. [Definer og behandle en underleveranseoperasjon](manufacturing/set-up-process-subcontracting-operation.md)  
7. [Definer ny kapasitet](manufacturing/set-up-new-capacity.md)  
8. [Forutse behov for varevarianter med ulike stykklister tildelt](manufacturing/variants.md)  

Les trinnene for hvert scenario i den relevante artikkelen.  

> [!IMPORTANT]
> Disse produksjonsgjennomgangene krever at brukeropplevelsen er satt til *Premium* på siden **Firmainformasjon**.

## <a name="warehousing-scenarios"></a><a name="warehousing-scenarios"></a><a name="warehousing-scenarios"></a>Lagerscenarioer

Demodata for Contoso Coffee støtter nå følgende lagerscenarioer for test og opplæring:

1.  Konfigurer standardhyller, mottak og plassering med lagerplassering, plukking og levering med lagerplukk i ordre-etter-ordre-måte med [Gjennomgang av inngående og utgående flyt i grunnleggende lagerkonfigurasjoner](warehousing/warehouse-basic-flow-putaway-pick.md)
2.  Mottak og plassering av flere inngående ordrer samtidig med lagermottak, lever flere ordrer samtidig med lagerlevering, plukk med lagerplukk med [Gjennomgang av inngående og utgående flyt i blandede lageroppsett](warehousing/warehouse-mixed-flow-receive-pick-ship.md)
3.  Konfigurere faste hyller for vareenheten, brukerkryssoverføring til å redusere fysisk flytting av varer, optimalisere plassering av varer med hylleetterfylling, anbrekke store enheter til mindre enheter kan du distribuere plukking mellom lager som bruker plukkforslaget med [Gjennomgang av inngående og utgående flyt i avansert lageroppsett med lagerstyring](warehousing/warehouse-directed-flow.md)

Les trinnene for hvert scenario i den relevante artikkelen.
   
## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se også

[Produksjon](../production-manage-manufacturing.md)  
[Lagerstyring](../warehouse-manage-warehouse.md)  

