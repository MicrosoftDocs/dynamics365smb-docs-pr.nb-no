---
title: Bruke automatisk datafangstsystem (ADFS) | Microsoft-dokumentasjon
description: Du kan bruke det automatiske datafangstsystemet (ADFS) til å registrere flyttingen av varer i lageret, og til å registrere noen kladdeaktiviteter, for eksempel antallsjusteringer i lagerets varekladd og beholdning.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: barcode
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 5fe40d26a9128b9f689c5ec4502af929d0af04c2
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3925350"
---
# <a name="use-automated-data-capture-systems-adcs"></a>Bruk ADCS (Se automatisk datahentesystem)

> [!NOTE]
> ADFS-løsningen (Automatisk datafangstsystem) gjør det mulig for [!INCLUDE[d365fin](includes/d365fin_md.md)] å kommunisere med håndholdte enheter gjennom webtjenester. Du må arbeide med en Microsoft-partner som kan opprette koblingen mellom webtjenesten og den bestemte håndholdte enheten. 

Du kan bruke det automatiske datafangstsystemet (ADFS) til å registrere flyttingen av varer i lageret, og til å registrere noen kladdeaktiviteter, for eksempel antallsjusteringer i lagerets varekladd og beholdning. ADFS innebærer vanligvis skanning av en strekkode.

Hvis du vil bruke ADFS, må du gi hver vare som er lagret på lager, en vare-ID. Du må også sette opp miniformer, funksjoner for håndholdte enheter, datautveksling og angi innstillinger for felt som kontrollerer ADFS. Du angir om du vil bruke ADFS på lokasjonskortet for et lager.

På bakgrunn av lagerets behov definerer du hvor mye som skal vises i miniformoppsettet for den bestemte enheten. Følgende er eksempler på informasjon som du kan vise:  

- Data fra tabeller i [!INCLUDE[d365fin](includes/d365fin_md.md)], for eksempel en liste over plukkdokumenter som brukeren kan velge fra.  
- Tekstinformasjon.  
- Meldinger for å vise bekreftelser eller feil om aktiviteter som er utført og registrert av brukeren av den håndholdte enheten.

## <a name="to-enable-web-services-for-adcs"></a>Slik aktiverer du webtjenester for ADFS
Du må aktivere ADFS-webtjenesten for å kunne bruke automatisisk datafangstsystem.  

## <a name="to-enable-and-publish-the-adcs-web-service"></a>Slik aktiverer og publiserer du ADFS-webtjenesten  

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Webtjenester**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Ny**.  
3. Skriv inn følgende informasjon på en ny linje på siden **Webtjenester**:  

    |Felt|Verdi|  
    |---------------------------------|-----------|  
    |**Type objekt**|Kodeenhet|  
    |**ID for objekt**|7714|  
    |**Tjenestenavn**|ADFS **Viktig:** Du må gi et navn til tjenesten **ADFS**.|  

5. Merk av for **Publisert**.  
6. Velg **OK**-knappen.  

## <a name="to-set-up-a-warehouse-to-use-adcs"></a>Slik konfigurerer du et lager til å bruke ADFS  
Hvis du vil bruke ADFS, må du angi hvilke lagerlokasjoner som bruker teknologien.  

> [!NOTE]  
>  Vi anbefaler at du ikke definerer et lager slik at det bruker ADFS hvis det også har et hyllekapasitetsprinsippet.

1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Lokasjoner**, og velg deretter den relaterte koblingen.
2.  Velg et lager i oversikten der du vil aktivere ADFS, og velg deretter **Rediger**-handlingen.
3. På siden **Lokasjonskort** merker du av for **Bruk ADFS**.  

## <a name="to-specify-an-item-to-use-adcs"></a>Slik angir du at en vare skal bruke ADFS:  
Hver lagervare som du vil bruke med ADFS, må være tilordnet en ID-kode for å knytte den til varenummer. Du kan for eksempel bruke varens strekkode som ID-kode. En vare kan også ha flere ID-koder. Dette kan være nyttig hvis en vare er tilgjengelig i ulike enheter, for eksempel stykk og paller. I dette tilfellet tilordner du en ID-kode til hver.    

1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Varer**, og velg deretter den relaterte koblingen.  
2.  Velg en vare fra oversikten som er del av ADFS-løsningen, og velg deretter **Rediger**-handlingen.
3. På siden **Varekort** velger du handlingen **Identifikatorer**.
4. På siden **Vare-IDer** velger du handlingen **Ny**.
5. Angi identifikatoren for varen i **Kode**-feltet. Identifikatoren kan for eksempel være varens strekkodenummer.  

    Du kan også angi en **Variantkode** og en **Enhetskode**.  

6. Angi om nødvendig flere koder for hver vare.
7. Velg **OK**.  
8.  Hvis du vil gå gjennom informasjonen, velger du **ID-kode**-feltet for å åpne **Vare-IDer**-siden.

## <a name="to-add-an-adcs-user"></a>Slik legger du til en ADFS-bruker:  
Du kan legge til enhver bruker som en bruker av et automatisk datafangstsystem (ADFS). Når du gjør dette, må brukeren også angi et passord. Du kan eventuelt også angi en forbindelse som identifiserer ADFS-brukeren som lageransatt. ADFS-brukerpassordet kan være forskjellig fra brukerens Windows-påloggingspassord. Hvis du vil ha mer informasjon, kan du se [Tilordne tillatelser til brukere og grupper](ui-define-granular-permissions.md).

1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **ADCS-brukere**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**.  
3.  Angi et navn for brukeren i **Navn**-feltet. Navnet kan ikke inneholde mer enn 20 tegn, inkludert mellomrom.  
4.  Angi et passord i **Passord**-feltet. Passordet er maskert.  

### <a name="to-specify-that-a-warehouse-employee-is-an-adcs-user"></a>Slik angir du at en lageransatt er ADFS-bruker:  
1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Lageransatte**, og velg deretter den relaterte koblingen.  
2.  Du kan om nødvendig legge til en ny lageransatt. Hvis du vil ha mer informasjon, kan du se [Definere lageransatte](warehouse-how-to-set-up-warehouse-employees.md).  
3.  Velg handlingen **Rediger oversikt**.  
4.  Velg en lageransatt fra oversikten. Velg rullegardinpilen i **ADFS-bruker**-feltet, og velg deretter navnet på en ADFS-bruker fra listen.  

> [!NOTE]  
>  Standardlageret for den ansatte må være et som bruker ADFS.

## <a name="to-create-and-customize-miniforms"></a>Slik oppretter og tilpasser du miniformer:
Du bruker miniformer til å beskrive informasjonen du vil presentere på en håndholdt enhet. Du kan for eksempel opprette miniformer for å støtte lageraktiviteten med å plukke varer. Når du har opprettet en miniform, kan du legge til funksjoner for vanlige handlinger som en bruker utfører med håndholdte enheter, for eksempel flytte opp eller ned en linje.  

> [!NOTE] 
> Hvis du vil implementere eller endre funksjonaliteten for en Miniform-funksjon, må du opprette en ny kodeenhet for feltet **Codeunit for håndtering** for å utføre handlingen eller svaret som er nødvendig. Du kan lære mer om ADFS-funksjonalitet ved å undersøke kodeenheter, for eksempel 7705, 7706, 7712 og 7713.  

### <a name="to-create-a-miniform-for-adcs"></a>Slik oppretter du Miniform for ADFS:  
1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Miniforms**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**.  
3.  I feltet **Kode** angir du en kode for miniformen. Angi eventuelt verdier i alle andre felt.  

    Merk av for **Start miniform** for å angi at miniformen er det første skjemaet brukeren ser ved pålogging.  

4.  Definer feltene som vises på miniformen, på hurtigfanen **Linjer**. Rekkefølgen som du registrerer linjer i, er rekkefølgen linjene vises i på den håndholdte enheten.  

Når du har opprettet en miniform, er de neste trinnene å opprette funksjoner og knytte til funksjonalitet for ulike tastaturinndata.  

### <a name="to-customize-miniform-functions"></a>Slik tilpasser du Miniform-funksjoner:  
1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Miniforms**, og velg deretter den relaterte koblingen.  
2.  Velg en miniform fra listen, og velg deretter handlingen **Rediger**.  
3.  Velg handlingen **Funksjoner**.  
4.  Velg en kode som skal representere funksjonen du vil knytte til miniformen, i rullegardinlisten **Funksjonskode**. Du kan for eksempel velge ESC, som gjør at funksjonalitet knyttes til trykk på ESC-tasten.  

## <a name="see-also"></a>Se også  
[Lagerstyring](warehouse-manage-warehouse.md)  
[Lager](inventory-manage-inventory.md)  
[Definere lagerstyring](warehouse-setup-warehouse.md)     
[Monteringsstyring](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyring](design-details-warehouse-management.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
