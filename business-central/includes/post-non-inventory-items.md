---
author: brentholtorf
ms.topic: include
ms.date: 09/21/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

Lageransatte kan levere og motta ikke-lagervarer sammen med fysiske varer i ordrer og bestillinger. Ikke-lagervarer er immaterielle eiendeler, for eksempel forsikring eller ekstra kostnader.

Ordrer og bestillinger har ofte ulike typer ting på linjen. Ordrer kan for eksempel omfatte finansvarer, kontoer og aktiva. Hvis du bruker lagerdokumenter til å håndtere fysiske varer, kan du også bokføre noen typer ikke-lagervarer. Følgende er eksempler på lagerdokumenter:

* Lagerplasseringer
* Lagermottak
* Lagerplukk
* Lagerleveringer

Hvis du vil at lagerarbeidere skal kunne levere og motta varer som ikke er lagervarer, fyller du ut **Bokfør ikke-lager via lager automatisk.** -feltet på sidene **Salgsoppsett** og **Kjøpsoppsett** . Feltet inneholder følgende alternativer:

|Alternativ  |Description  |
|---------|---------|
|Ingen     |Ikke lever eller motta varer som ikke er lagervarer.         |
|Vedlagt/tildelt     | Bokfør varegebyrer og andre varelinjer som ikke er lagervarer, som er tilordnet eller knyttet til fysiske varer. Hvis du vil knytte ikke-lagerlinjer til fysiske varer, bruker du handlingen **Knytt til lagerlinje** .        |
|Alle     | Bokfør alle ikke-lagerlinjer i kildedokumentet så snart minst én vare er bokført av lagerdokumentet.        |

> [!NOTE]
> Alternativet **Komplett** i feltet **Leveringsrådgivning** i ordren har prioritet over valget i feltet **Bokfør ikke-lager via lager automatisk.** -feltet på siden **Salgsoppsett**.