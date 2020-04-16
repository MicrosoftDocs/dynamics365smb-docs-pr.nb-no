---
title: Forstå Varetyper| Microsoft-dokumentasjon
description: Du kan justere lagerverdien for en vare, for eksempel med lagermetoden FIFO eller Gjennomsnitt, når varekost endres av andre årsaker enn transaksjoner.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: ab3da8450586928a02d17ccce14c704ed6d7c8fe
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3182399"
---
# <a name="about-item-types"></a>Om varetyper
I feltet **Type** på siden **Varekort** kan du velge hva varen brukes for i din bedrift, og derfor hvordan den håndteres i programmet. Det finnes tre alternativer:

|Alternativ|Vanlig formål|
|------|-----------|
|Lager|En fysisk enhet, for eksempel en sykkel, for full selskapsstøtte.|
|Ikke-lagervarer|En fysisk enhet, for eksempel en bolt, for begrenset selskapsstøtte, for eksempel fordi varen bare brukes internt og har en lav kostnad.|
|Tjeneste|En arbeidstidsenhet, for eksempel en konsulenttime, for begrenset selskapsstøtte.|

**Lager**-typen omfatter fullstendig sporing av lagerantall og verdi. Derfor støttes alle varetransaksjonstyper, og varer av typen Lager kan brukes med alle funksjoner for håndtering av varer.

Typene **Service** og **Ikke-lagervarer** involverer ikke sporing av lagerantall og verdi. Derfor støttes bare utvalgte varetransaksjonstyper og funksjoner.

De tre varetypene støtter disse funksjonene henholdsvis.

|Varetype|Salg|Kjøp|Jobbforbruk|Serviceforbruk|Monteringsforbruk|Produksjon Forbruk|Monteringsavgang|Produksjonsavgang|Lokasjon, Overføring|Fysisk opptelling|Revaluering av lager|Beholdning og kostberegning|Varesporing|Reservasjon|Lagerstyring|Planlegging|
|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|Lager|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|
|Ikke-lagervarer|Ja|Ja|Ja|Ja|Ja|Ja|Nei|Nei|Nei|Nei|Nei|Nei|Nei|Nei|Nei|Nei|
|Tjeneste|Ja|Ja|Ja|Nei|Nei|Nei|Nei|Nei|Nei|Nei|Nei|Nei|Nei|Nei|Nei|Nei|

> [!NOTE]
> Varer som du tilbyr kunder, men som du ikke vil administrere i systemet før du begynner å selge dem, kan defineres som katalogvarer. Katalogvarer må ikke forveksles med vanlige varer av typen Ikke-lagervarer. Hvis du vil ha mer informasjon, kan du se [Arbeide med katalogvarer](inventory-how-work-nonstock-items.md).

> [!NOTE]
> Kundenes varer som du utfører service på, for eksempel en skriver, kalles servicevarer. Servicevarer har ikke noe å gjøre med vanlige varer eller katalogvarer. Servicekomponentene kan imidlertid være vanlige varer. Hvis du vil ha mer informasjon, se [Definere servicevarer og servicevarekomponenter](service-how-setup-service-items.md).

## <a name="see-also"></a>Se også
[Registrere nye varer](inventory-how-register-new-items.md)  
[Definere lager](inventory-setup-inventory.md)  
[Administrere lagerkostnader](finance-manage-inventory-costs.md)  
[Lager](inventory-manage-inventory.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
