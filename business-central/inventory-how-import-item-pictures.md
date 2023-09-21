---
title: Importer mange varebilder fra en ZIP-fil
description: 'For å importere flere varebilder gir du bildefilene navn som svarer til dine varenumre, komprimerer dem til en zip-fil, og bruker Importer varebilder-siden.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'product, image'
ms.search.form: '30, 461'
ms.date: 06/16/2021
ms.author: bholtorf
---
# <a name="import-multiple-item-pictures"></a>Importere flere varebilder
Du kan importere flere varebilder på én gang. Bare gi bildefilene navn som svarer til dine varenumre, komprimer dem til en zip-fil, og bruk Importer varebilder-siden til å behandle hvilke varebilder som skal importeres.

Alle vanlige filformater støttes.

## <a name="to-name-picture-files-by-the-item-names-and-prepare-the-zip-file"></a>Navngi bildefiler etter varenavn og klargjøre zip-filen
1. På lokasjonen der varebildene lagres, navngir du hver fil i henhold til nummeret på den tilknyttede varen. Eksempel:

    |Varenr.|Filnavn|
    |-|-|
    |1000|1000.bmp|
    |1001|1001.bmp|
    |1002|1002.bmp|

2. Samle alle filer i en zip-fil. For eksempel i Windows Explorer velger du filene og deretter **Send til**, **Komprimert (zippet) mappe**.     

## <a name="to-import-item-pictures"></a>Importere varebilder
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lageroppsett** og velg den relaterte koblingen.
2. Velg handlingen **Importer varebilder**.
3. I feltet **Velg en ZIP-fil** velger du den aktuelle zip-mappen, og deretter velger du **Åpne**-knappen.

    Det opprettes en linje for hver vare og hvert bilde som opprettes på siden **Importer varebilder**.

    > [!NOTE]
    > For varekort som allerede har et bilde, er det merket av for **Bildet finnes allerede**. Hvis du ikke vil at eksisterende bilder skal byttes ut, fjerner du merket for **Erstatt bilder**. Hvis du ikke vil at individuelle eksisterende bilder skal byttes ut, kan du slette de aktuelle linjene.

3. Velg handlingen **Importer bilder**.

Feltet **Importer status** oppdateres for å vise om bildeimporten ble hoppet over eller fullført.       

## <a name="see-also"></a>Se også
[Registrere nye varer](inventory-how-register-new-items.md)  
[Opprette nummerserier](ui-create-number-series.md)  
[Lager](inventory-manage-inventory.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Salg](sales-manage-sales.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
