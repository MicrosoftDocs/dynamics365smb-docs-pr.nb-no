---
title: Arbeid med stykklister
description: Du oppretter en monteringsstykkliste eller produksjonsstykkliste for å spesifisere komponenter eller ressurser som kreves for å sette sammen varen som stykklisten representerer.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'bills of material, assembly BOM, production BOM,'
ms.search.form: null
ms.date: 06/06/2024
ms.service: dynamics-365-business-central
---
# Arbeid med stykklister

Du bruker stykklister til å strukturere overordnede varer som må monteres fra andre varer eller produseres av ressurser eller produksjonsressurser fra komponenter.

## Monteringsstykklister eller produksjonsstykklister

[!INCLUDE[prod_short](includes/prod_short.md)] støtter to ulike stykklistetyper:

| Stykklistetype | Generell kategori | Eksempel |
| -------- | ---------------- | ------- |
| [Monteringsstykklister](assembly-how-work-assembly-boms.md) | Lager/montering | Varer som består av andre varer, sammen med enkle eller ingen ressurser. |
| [Prod.stykklister](production-how-to-create-production-boms.md) | Produksjon | Varer som består av ulike komponenter og halv fabrikater, produsert i et arbeidssenter eller en produksjonsressurs. |

Bruk monteringsordrer til å produsere sluttvarer fra komponenter i en enkel prosess som kan utføres av én eller flere grunnleggende ressurser, som ikke er produksjonsressurser eller arbeidssentre, eller uten noen ressurser. En monteringsprosess kan for eksempel være å plukke to flasker vin og én kaffepose og deretter pakke dem som en gave.  

En monteringsstykkliste er hoveddataene som definerer hvilke komponentvarer som inngår i en montert sluttvare, og hvilke ressurser som brukes til å montere monteringselementet. Når du angir en monteringsvare og et antall i hodet i en ny monteringsordre, fylles monteringsordrelinjene automatisk ut i henhold til monteringsstykklisten, med én monteringsordrelinje per komponent eller ressurs. Finn ut mer under [Monteringsstyring](assembly-assemble-items.md).

Du bruker produksjonsordrer for å produsere sluttvarer fra komponenter i en kompleks prosess som krever en produksjonsrute og arbeidssentre eller produksjonsressurser, som representerer produksjonskapasitet. En produksjonsprosess kan for eksempel være å skjære stålplater i én operasjon, sveise dem sammen i neste operasjon og male sluttvaren i siste operasjon. Finn ut mer under [Produksjon](production-manage-manufacturing.md).

En produksjonsstykkliste er hoveddata som definerer en produksjonsvare og komponentene som inngå i den. For monteringsvarer må produksjonsstykklisten sertifiseres og tilordnes til produksjonsvaren før den kan brukes i en produksjonsordre. Når du angir produksjonsvaren på en produksjonsordrelinje, enten manuelt eller ved å fornye ordren, vil innholdet i produksjonsstykklisten gjøres til produksjonsordrekomponentene. Finn ut mer under [Opprett produksjonsstykklister](production-how-to-create-production-boms.md).

Konseptet med ressurser i produksjon er mye mer avansert enn i monteringsstyring. Arbeidssentre og produksjonsressurser fungerer som ressurser. Operasjonene som er tilordnet ressurser i produksjonsruter, representerer produksjonstrinn. Finn ut mer i artikkelen [Opprett ruter](production-how-to-create-routings.md).

Både monteringsordrer og produksjonsordrer kan kobles direkte til salgsordrer. Du kan imidlertid bare bruke monteringsordrer til å tilpasse sluttvaren direkte for en kundeforespørsel med ordren.

## Se også

[Arbeid med monteringsstykklister](assembly-how-work-assembly-boms.md)  
[Opprette produksjonsstykklister](production-how-to-create-production-boms.md)  
[Registrere nye varer](inventory-how-register-new-items.md)  
[Behandle produktvarianter](inventory-item-variants.md)  
[Lager](inventory-manage-inventory.md)  
[Produksjon](production-manage-manufacturing.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
