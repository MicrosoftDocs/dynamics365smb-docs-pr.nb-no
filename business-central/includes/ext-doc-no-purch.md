---
author: edupont04
ms.topic: include
ms.date: 05/27/2021
ms.author: edupont
ms.openlocfilehash: f1c6ead7a776d11ccc8917944c3752ec6ac43c66
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2022
ms.locfileid: "8132657"
---
I kjøpsdokumenter og kladder kan du angi et dokumentnummer som viser til leverandørens nummereringssystem. Bruk dette feltet til å registrere nummeret som leverandøren har knyttet til ordren, fakturaen eller kreditnotaen. Du kan deretter bruke nummeret senere hvis du trenger å søke etter den bokførte oppføring ved hjelp av dette nummeret.

Feltet **Obligatorisk nr. for eksternt dokument** i feltet **Kjøpsoppsett** angir om det er obligatorisk å angi et eksternt dokumentnummer i følgende situasjoner:

* I feltet **Leverandørs fakturanr.**, feltet **Leverandørs bestillingsnr.** , eller feltet **Leverandørs kreditnotanr.** i et bestillingshode

* I feltet **Eksternt dokumentnr.** på en finanskladdelinje der innholdet i feltet **Bilagstype** er angitt til *Faktura*, *Kreditnota* eller *Rentenota*, og innholdet i feltet **Kontotype** er angitt til *Leverandør*.

Hvis du velger dette feltet, vil det ikke være mulig å bokføre en faktura, en kreditnota eller den type finanskladdelinje som er beskrevet ovenfor, uten at et eksternt dokumentnummer er fylt ut.

Det eksterne dokumentnummeret inkluderes i bokførte dokumenter der du kan søke etter det aktuelle nummeret. Du kan også søke ved hjelp av det eksterne dokumentnummeret når du navigerer i leverandørposter.

En annen måte å håndtere eksterne dokumentnumre på, er å bruke feltet **Deres referanse**. Hvis du bruker feltet **Deres referanse**, inkluderes nummeret i bokførte dokumenter, og du kan søke etter det på samme måte som for verdier fra feltet **Eksternt dokumentnr.**. Men feltet er ikke tilgjengelig på kladdelinjer.
