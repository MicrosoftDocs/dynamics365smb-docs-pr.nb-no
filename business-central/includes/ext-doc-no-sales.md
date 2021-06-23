---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 05/27/2021
ms.author: edupont
ms.openlocfilehash: 50b4b331f00bdcdf030bac2332ffb5dafdfd2de6
ms.sourcegitcommit: f9a190933eadf4608f591e2f1b04c69f1e5c0dc7
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115985"
---
I salgsdokumenter og kladder kan du angi et dokumentnummer som viser til kundens nummereringssystem. <!--You can enter a maximum of ten characters, both numbers and letters.--> Bruk dette feltet til å registrere nummeret som kunden har knyttet til ordren, fakturaen eller kreditnotaen. Du kan deretter bruke nummeret senere hvis du trenger å søke etter den bokførte oppføring ved hjelp av dette nummeret.  

Feltet **Obligatorisk nr. for eksternt dokument** på siden **Salgsoppsett** angir om det er obligatorisk å angi et eksternt dokumentnummer i feltet **Eksternt dokumentnr.** i et salgshode og feltet **Eksternt dokumentnr.** på en finanskladdelinje.

Hvis du velger dette feltet, vil det ikke være mulig å bokføre en faktura eller en kladdelinje uten et eksternt dokumentnummer.

Det eksterne dokumentnummeret inkluderes i bokførte dokumenter der du kan søke etter det aktuelle nummeret. Du kan også søke ved hjelp av det eksterne dokumentnummeret når du navigerer i kundeposter.

En annen måte å håndtere eksterne dokumentnumre på, er å bruke feltet **Deres referanse**. Hvis du bruker feltet **Deres referanse**, inkluderes nummeret i bokførte dokumenter, og du kan søke etter det på samme måte som for verdier fra feltet **Eksternt dokumentnr.**. Men feltet er ikke tilgjengelig på kladdelinjer.
