---
title: Opprette produksjonsstykklister
description: En produksjonsstykkliste inneholder hoveddata som beskriver komponenter og halvfabrikata som brukes i produksjonen av en overordnet vare. Når en produksjonsordre opprettes for den overordnede varen, styrer produksjonsstykklisten beregningen av materialbehovet slik det er representert på siden **Prod.ordrekomponenter**.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 01/05/2020
ms.author: edupont
ms.openlocfilehash: 5c9f2fa03f5f20e533237e60762dc60fc679d0d0
ms.sourcegitcommit: cdba82235c0c07497bd04b9bd5134ef245d92c09
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/07/2021
ms.locfileid: "4838485"
---
# <a name="create-production-boms"></a>Opprette produksjonsstykklister

En produksjonsstykkliste inneholder hoveddata som beskriver komponenter og halvfabrikata som brukes i produksjonen av en overordnet vare. Når en produksjonsordre opprettes for den overordnede varen, styrer produksjonsstykklisten beregningen av materialbehovet slik det er representert på siden **Prod.ordrekomponenter**.

[!INCLUDE[prod_short](includes/prod_short.md)] støtter også monteringsstykklister. Du bruker monteringsordrer for å produsere sluttvarer fra komponenter i en enkel prosess som kan utføres av én eller flere grunnleggende ressurser, som ikke er produksjonsressurser eller arbeidssentre, eller uten noen ressurser. En monteringsprosess kan for eksempel være å plukke to flasker vin og én kaffepose og deretter pakke dem som en gave. Hvis du vil ha mer informasjon, kan du se [Monteringsstykklister eller produksjonsstykklister](inventory-how-work-boms.md#assembly-boms-or-production-boms).  

Før du kan definere en rute, må følgende være på plass:  

- Varekort er opprettet for overordnede varer som inngår i produksjonen. Hvis du vil ha mer informasjon, kan du se [Registrere nye varer](inventory-how-register-new-items.md).
- Produksjonsressurser er definert. Hvis du vil ha mer informasjon, kan du se [Konfigurere arbeidssentre og produksjonsressurser](production-how-to-set-up-work-and-machine-centers.md).

## <a name="to-create-a-production-bom"></a>Slik oppretter du en produksjonsstykkliste  
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Produksjonsstykkliste**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**.  
3. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Hvis du vil kunne redigere stykklisten, setter du **Status**-feltet til **Ny** eller **Under utvikling**. Hvis du vil aktivere den, setter du **Status**-feltet til **Sertifisert**.  

    Fortsett med å fylle ut produksjonsstykklistelinjene.
5. I **Type**-feltet velger du om varen på denne stykklistelinjen er en vanlig vare eller en produksjonsstykkliste. Hvis varen på linjen er en produksjonsstykkliste, må den allerede finnes som en sertifisert produksjonsstykkliste.  
6.  I **Nr.** -feltet velger du varen eller produksjonsstykklisten, eller skriver den inn i feltet.  
7.  I **Antall per**-feltet angir du hvor mange enheter av varen som skal høre til den overordnede varen, for eksempel 4 hjul for 1 bil.  
8.  I feltet **Vrak-%** kan du registrere en fast prosentandel for komponenter som vrakes under produksjon. Når komponentene er klare til bruk i en frigitt produksjonsordre, legges denne prosentandelen til i det forventede antallet feltet **Forbruksantall** i en produksjonskladd. Hvis du vil ha mer informasjon, kan du se [Registrere forbruk og avgang](production-how-to-register-consumption-and-output.md).  

    > [!NOTE]  
    >  Denne vrakprosenten representerer komponenter som vrakes under produksjon når de plukkes fra lageret, mens vrakprosenten for rutelinjer representerer vraket avgang før de ble plassert på lageret.  

9.  I feltet **Rutekoblingskode** registrerer du en kode for å koble komponenten til en bestemt operasjon. Hvis du vil ha mer informasjon, kan du se [Slik oppretter du rutekoblinger](production-how-to-create-routings.md#to-create-routing-links).
10. Hvis du vil kopiere linjer fra en eksisterende produksjonsstykkliste, velger du **Kopier stykkl.** for å velge eksisterende linjer.  
11.  Godkjenn produksjonsstykklisten.  
12.  Nå kan du knytte den nye produksjonsstykklisten til kortet for den aktuelle overordnede varen. Hvis du vil ha mer informasjon, kan du se [Registrere nye varer](inventory-how-register-new-items.md).  

> [!NOTE]  
> [!INCLUDE [bom-standard-cost](includes/bom-standard-cost.md)] Hvis du vil beregne varens standardkost fra varekortet, velger du **Produksjon** og deretter **Beregn standardkost**.  

## <a name="to-create-a-new-versions-of-a-production-bom"></a>Slik oppretter du nye versjoner av en produksjonsstykkliste
Nye versjoner av produksjonsstykklister brukes for eksempel når en vare erstattes av en annen vare, eller når en kunde krever en spesialversjon av et produkt. Versjonsprinsippet gjør det mulig å håndtere flere versjoner av en produksjonsstykkliste. Strukturen i produksjonsstykklisteversjonen tilsvarer strukturen i produksjonsstykklistene. Hovedforskjellen ligger i versjonenes tidsgyldighet. Gyldigheten defineres av startdatoen.  

Startdatoen angir starten på perioden som denne versjonen er gyldig i. I alle andre tilfeller er startdatoen et filterkriterium for beregninger og evalueringer. Stykklisteversjonen er gyldig til neste versjon blir gyldig.  

1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Produksjonsstykkliste**, og velg deretter den relaterte koblingen.  
2.  Velg produksjonsstykklisten som skal kopieres, og velg deretter **Versjoner**-handlingen.  
3.  Velg handlingen **Ny**.  
4. Fyll ut feltene etter behov.
5. I feltet **Versjonskode** angir du versjonens unike identifikasjon. Alle kombinasjoner av tall og bokstaver er tillatt.  

    Den nye versjonen får automatisk statusen **Ny**.
6. Når stykklisteversjonen er fullført, kan du angi **Status**-feltet til **Sertifisert**.  

Tidsgyldigheten for versjonen angis i feltet **Startdato**.  

> [!NOTE]  
>  Velg alternativet **Vare** i **Type**- feltet for å bruke en vare fra varehoveddataene i produksjonsstykklisten. Hvis varen også har en produksjonsstykkliste, der feltet **Produksjonsstykklistenummer** er fylt ut på varekortet, tas det også hensyn til denne produksjonsstykklisten.  
>   
>  Velg alternativet **Produksjonsstykkliste** hvis du vil bruke en fantomproduksjonsstykkliste på linjen.  
>   
>  Fantomproduksjonsstykklister skal strukturere produkter. Slike produksjonsstykklister fører aldri frem til ferdige produkter, men brukes bare til å bestemme det avhengige behovet. Fantomproduksjonsstykklister har ikke egne varehoveddata.

## <a name="quantity-calculation-formula-on-production-boms"></a>Formelen for beregning av antallet på produksjonsstykklister  
Antallet beregnes på bakgrunn av forskjellige dimensjoner som også er angitt på produksjonsstykklistelinjene. Dimensjonene viser til en ordreenhet av varen. Lengden, bredden, dybden og vekten kan angis som dimensjoner.  

Kolonnene Beregningsformel, Lengde, Dybde, Høyde og Vekt vises ikke, fordi de bare brukes av noen brukere. Hvis du vil beregne antallet, må du først vise disse kolonnene.  

Sammenhengen mellom de enkelte komponentene defineres av beregningsformelen. Følgende muligheter kan brukes som beregningsformel:  

-  **Tom** - Det tas ikke hensyn til dimensjoner. (Antall = Antall per.)  
-  **Lengde** - Antall = Antall per * Lengde  
-  **Lengde x Bredde** - Antall = Antall per * Lengde x Bredde  
-  **Lengde x Bredde x Dybde** - Antall = Antall per x Lengde x Bredde x Dybde  
-  **Wekt** - Antall = Antall per x Weight  

### <a name="example"></a>Eksempel  
I en produksjonsstykkliste kreves det sytti metalldeler med dimensjonslengde = 0,20 m og bredde = 0,15 m. Verdiene angis slik: Beregningsformel = Lengde x Bredde, Lengde = 20, Bredde = 15, Antall per = 70. Antallet angis av Antall per x Lengde x Bredde, det vil si Antall = 70 x 0,20 m x 0,15 m = 2,1 m2.  

## <a name="see-also"></a>Se også  
[Opprette ruter](production-how-to-create-routings.md)   
[Definere produksjon](production-configure-production-processes.md)  
[Produksjon](production-manage-manufacturing.md)    
[Planlegging](production-planning.md)   
[Lager](inventory-manage-inventory.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]