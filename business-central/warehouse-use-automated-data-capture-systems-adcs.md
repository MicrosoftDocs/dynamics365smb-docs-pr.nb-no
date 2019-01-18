---
title: Bruke automatisk datafangstsystem (ADFS) | Microsoft-dokumentasjon
description: "Du kan bruke det automatiske datafangstsystemet (ADFS) til å registrere flyttingen av varer i lageret, og til å registrere noen kladdeaktiviteter, for eksempel antallsjusteringer i lagerets varekladd og beholdning."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/04/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 4d378e4407ce0023ab0f089f7a8a218605c4cf7d
ms.contentlocale: nb-no
ms.lasthandoff: 11/26/2018

---
# <a name="use-automated-data-capture-systems-adcs"></a>Bruk ADCS (Se automatisk datahentesystem)

> [!NOTE]
> I standardversjonen av [!INCLUDE[d365fin](includes/d365fin_md.md)] fungerer ADFS bare på lokale distribusjoner. En Microsoft-partner kan imidlertid få den til å fungere i nettdistribusjoner ved å bruke PowerApps eller lignende.

Du kan bruke det automatiske datafangstsystemet (ADFS) til å registrere flyttingen av varer i lageret, og til å registrere noen kladdeaktiviteter, for eksempel antallsjusteringer i lagerets varekladd og beholdning.  

Hvis du vil bruke ADFS, må du gi hver vare som er lagret på lager, en vare-ID. Du må også sette opp miniformer, funksjoner for håndholdte enheter, datautveksling og angi innstillinger for felt som kontrollerer ADFS. Du angir om du vil bruke ADFS på lokasjonskortet for et lager.

På bakgrunn av lagerets behov definerer du hvor mye som skal vises i miniformoppsettet for den bestemte enheten. Følgende er eksempler på informasjon som du kan vise:  

- Data fra tabeller i [!INCLUDE[d365fin](includes/d365fin_md.md)], for eksempel en liste over plukkdokumenter som brukeren kan velge fra.  
- Tekstinformasjon.  
- Meldinger for å vise bekreftelser eller feil om aktiviteter som er utført og registrert av brukeren av den håndholdte enheten.

Hvis du vil ha mer informasjon, se [Konfigurere et automatisk datafangstsystem](/dynamics-nav/Configuring-Automated-Data-Capture-System) i hjelpen for utviklere og IT-eksperter.

## <a name="to-set-up-a-warehouse-to-use-adcs"></a>Slik konfigurerer du et lager til å bruke ADFS  
Hvis du vil bruke ADFS, må du angi hvilke lagerlokasjoner som bruker teknologien.  

> [!NOTE]  
>  Vi anbefaler at du ikke definerer et lager slik at det bruker ADFS hvis det også har et hyllekapasitetsprinsippet.

1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Lokasjoner**, og velg den relaterte koblingen.
2.  Velg et lager i oversikten der du vil aktivere ADFS, og velg deretter **Rediger**-handlingen.
3. På siden **Lokasjonskort** merker du av for **Bruk ADFS**.  

## <a name="to-specify-an-item-to-use-adcs"></a>Slik angir du at en vare skal bruke ADFS:  
Hver lagervare som du vil bruke med ADFS, må være tilordnet en ID-kode for å knytte den til varenummer. Du kan for eksempel bruke varens strekkode som ID-kode. En vare kan også ha flere ID-koder. Dette kan være nyttig hvis en vare er tilgjengelig i ulike enheter, for eksempel stykk og paller. I dette tilfellet tilordner du en ID-kode til hver.    

1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Varer**, og velg deretter den relaterte koblingen.  
2.  Velg en vare fra oversikten som er del av ADFS-løsningen, og velg deretter **Rediger**-handlingen.
3. På siden **Varekort** velger du handlingen **Identifikatorer**.
4. På siden **Vare-IDer** velger du handlingen **Ny**.
5. Angi identifikatoren for varen i **Kode**-feltet. Identifikatoren kan for eksempel være varens strekkodenummer.  

    Du kan også angi en **Variantkode** og en **Enhetskode**.  

6. Angi om nødvendig flere koder for hver vare.
7. Velg **OK**.  
8.  Hvis du vil gå gjennom informasjonen, velger du **ID-kode**-feltet for å åpne **Vare-IDer**-siden.

## <a name="to-add-an-adcs-user"></a>Slik legger du til en ADFS-bruker:  
Du kan legge til enhver bruker som en bruker av et automatisk datafangstsystem (ADFS). Når du gjør dette, må brukeren også angi et passord. Du kan eventuelt også angi en forbindelse som identifiserer ADFS-brukeren som lageransatt. ADFS-brukerpassordet kan være forskjellig fra brukerens Windows-påloggingspassord. Hvis du vil ha mer informasjon, kan du se [Administrere brukere og tillatelser](ui-how-users-permissions.md).

1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **ADFS-brukere**, og velg deretter den relaterte koblingen.  
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

Hvis du vil implementere eller endre funksjonaliteten for en Miniform-funksjon, må du opprette en ny kodeenhet eller endre en eksisterende for å utføre handlingen eller svaret som er nødvendig. Du kan finne ut mer om ADFS-funksjonalitet ved å kontrollere kodeenheter som 7705, som er håndteringskodeenheten for påloggingsfunksjonalitet. Kodeenhet 7705 viser hvordan en miniform av typen kort fungerer.  

### <a name="to-create-a-miniform-for-adcs"></a>Slik oppretter du Miniform for ADFS:  
1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Miniformer**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**.  
3.  I feltet **Kode** angir du en kode for miniformen. Angi eventuelt verdier i alle andre felt.  

    Merk av for **Start miniform** for å angi at miniformen er det første skjemaet brukeren ser ved pålogging.  

4.  Definer feltene som vises på miniformen, på hurtigfanen **Linjer**. Rekkefølgen som du registrerer linjer i, er rekkefølgen linjene vises i på den håndholdte enheten.  

Når du har opprettet en miniform, er de neste trinnene å opprette funksjoner og knytte til funksjonalitet for ulike tastaturinndata.  

### <a name="to-add-support-for-a-function-key"></a>Slik legger du til støtte for en funksjonstast:  
1.  Legg til kode som ligner på følgende eksempel, i XSL-filen for plugin-modulen. Dette oppretter en funksjon for **F6**-tasten. Tastesekvensinformasjonen kan fås fra enhetsprodusenten.  
    ```xml  
    <xsl:template match="Function[.='F6']">  
      <Function Key1="27" Key2="91" Key3="49" Key4="55" Key5="126" Key6="0"><xsl:value-of select="."/></Function>  
    </xsl:template>  
    ```  
2.  Åpne tabell 7702 i utviklingsmiljøet for [!INCLUDE[d365fin](includes/d365fin_md.md)], og legg til en kode som representerer den nye nøkkelen. I dette eksemplet oppretter du en nøkkel kalt **F6**.  
3.  Legg til C/AL-kode for funksjonen som er relevant for den miniformsspesifikke kodeenheten, for å håndtere funksjonstasten.  

### <a name="to-customize-miniform-functions"></a>Slik tilpasser du Miniform-funksjoner:  
1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Miniformer**, og velg deretter den relaterte koblingen.  
2.  Velg en miniform fra listen, og velg deretter handlingen **Rediger**.  
3.  Velg handlingen **Funksjoner**.  
4.  Velg en kode som skal representere funksjonen du vil knytte til miniformen, i rullegardinlisten **Funksjonskode**. Du kan for eksempel velge ESC, som gjør at funksjonalitet knyttes til trykk på ESC-tasten.  

Rediger koden for feltet **Kodeenhet for håndtering** i utviklingsmiljøet for [!INCLUDE[d365fin](includes/d365fin_md.md)] for å opprette eller endre koden for å utføre nødvendig handling eller svar.

Hvis du vil ha mer informasjon, se [Konfigurere et automatisk datafangstsystem](/dynamics-nav/Configuring-Automated-Data-Capture-System) i hjelpen for utviklere og IT-eksperter.

## <a name="see-also"></a>Se også  
[Lagerstyring](warehouse-manage-warehouse.md)  
[Lager](inventory-manage-inventory.md)  
[Definere lagerstyring](warehouse-setup-warehouse.md)     
[Monteringsstyring](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyring](design-details-warehouse-management.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

