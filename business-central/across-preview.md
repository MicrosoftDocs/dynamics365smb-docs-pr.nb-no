---
title: "Få forhåndsvisningen i nye markeder"
description: "Finn ut mer om å få tilgang til forhåndsvisninger av Business Central."
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: preview, trial, sandbox
ms.date: 10/01/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 50d1429a58b878766c76ed97f65936db78191ee0
ms.contentlocale: nb-no
ms.lasthandoff: 09/28/2018

---
# <a name="access-to-the-included365finlongincludesd365finlongmdmd-preview"></a>Få tilgang til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]-forhåndsvisningen
Fra og med våren 2018 blir [!INCLUDE[d365fin](includes/d365fin_md.md)] tilgjengelig i nye land. For å sikre at [!INCLUDE[d365fin](includes/d365fin_md.md)] er riktig løsning for disse kundene tilbyr vi en forhåndsvisningsversjon av tjenesten før vårlanseringen. Forhåndsvisningen for Danmark ble tilgjengelig i januar 2018, og flere markeder støttes snart.  

## <a name="getting-started-with-previews-and-sandboxes"></a>Komme i gang med forhåndsvisninger og sandkasser
Forhåndsvisninger og sandkasser er gode måter å komme i gang med [!INCLUDE[d365fin](includes/d365fin_md.md)]. En forhåndsvisningsforekomst viser funksjonalitet som er i tillegg til hva som er tilgjengelig i gjeldende versjon. Forhåndsvisninger gir partnere og kunder mulighet til å prøve og gi tilbakemelding om funksjonene som vi har tenkt å lansere. Selv om forhåndsvisninger hovedsakelig er ment for partnerne, er kunder også velkomne til å bruke dem i en begrenset periode. Gjeldende forhåndsvisning av [!INCLUDE[d365fin](includes/d365fin_md.md)] inneholder de fleste funksjonene som finnes i Dynamics NAV 2018, som vanligvis krever hjelp fra en partner å konfigurere.

Hvis du vil komme i gang med en forhåndsvisning, kan du gå til [denne siden](https://go.microsoft.com/fwlink/?linkid=866045) og angi e-postadressen for arbeid. Hvis du vil finne ut mer om [!INCLUDE[d365fin](includes/d365fin_md.md)] og funksjonene som tilbys, kan du se i dokumentasjonen på nettstedet.

Du kan tenke på en sandkasse som et ikke-produksjonsmiljø som du kan bruke i tillegg til produksjons- eller forhåndsvisningsforekomsten av [!INCLUDE[d365fin](includes/d365fin_md.md)]. En sandkasse lar deg trygt bygge og teste utvidelser og utvikle nye funksjoner for å tilpasse tjenesten uten å påvirke data og innstillinger for produksjons- eller forhåndsvisningsforekomstene. Akkurat nå kan alle kunder som har en produksjons- eller forhåndsvisningsversjon bruke en sandkasse.

Hvis du vil finne ut hvordan du kommer i gang med en sandkasse, kan du se instruksjonene nedenfor.

## <a name="creating-a-sandbox-environment"></a>Opprette et sandkassemiljø
Hvis du vil arbeide i et sandkassemiljø, må du ha et abonnement på [!INCLUDE[d365fin](includes/d365fin_md.md)]. Det kan være bare én sandkasse per abonnement.

### <a name="advanced-functionality-available-in-a-sandbox-environment"></a>Avanserte funksjoner i sandkassemiljøet
Sandkasser inneholde en klientutformingsfunksjon som lar deg utforme sider ved hjelp av et dra-og-slipp-grensesnitt, og bygge utvidelser i selve klienten ved å legge til og ordne felt.

Hvis du vil ha mer informasjon, kan du se [Bruke utformingen](https://docs.microsoft.com/en-us/dynamics-nav/developer/devenv-inclient-designer).

### <a name="to-create-a-sandbox-environment"></a>Slik oppretter du et sandkassemiljø
1.  Logg på din produksjons- eller forhåndsvisningsforekomst av [!INCLUDE[d365fin](includes/d365fin_md.md)].  
2.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Sandkassemiljø**, og velg deretter den relaterte koblingen.
3.  Velg **Opprett**. Det åpnes en fane der du kan fullføre konfigurasjonen av sandkassen.

    > [!Note]
    > Hvis popup-blokkering er aktivert i nettleseren, endrer du den til å tillate URL-adresser fra adressen *.businesscentral.dynamics.com*.  

4.  Når sandkassen er klar, vises en velkomstside.  
5.  Hvis du vil lese mer om scenarier som kan du prøve i en sandkasse, for eksempel hvordan du utvikler utvidelser, velger du koblingen **Finn ut mer**. Eller velger du **Lukk** for å fortsette til rollesenteret i [!INCLUDE[d365fin](includes/d365fin_md.md)]-sandkasseforekomsten.  
6.  Øverst i rollesenteret vises en melding som varsler deg at dette er en sandkasse. Du kan også se typen miljø på tittellinjen i klienten.

    > [!Note]
    > Sandkassen inneholder demonstrasjonsdata for det fiktive selskapet CRONUS. Ingen data kopieres eller blir ellers overført fra produksjonsmiljøet.  

7.  Du kan når som helst kan du gå tilbake til siden Sandkassemiljøer for å tilbakestille sandkassen.

    > [!Note]
    > Tilbakestilling av en sandkasse fjerner den fullstendig, og deretter opprettes den på nytt med standard demonstrasjonsdata.  

8.  Hvis du vil veksle mellom produksjonsmiljøet og sandkassen, kan du bruke Dynamics 365-menyen eller Dynamics-hjemmesiden.

    > [!Note]
    > En administrator eller en annen bruker, kan begrense eller blokkere brukertilgang til sandkassen ved hjelp av standard sikkerhetsfunksjoner i [!INCLUDE[d365fin](includes/d365fin_md.md)], for eksempel brukerkort, brukergrupper og tillatelsessett.  

### <a name="building-new-solutions-and-intellectual-property"></a>Bygge nye løsninger og immaterielle rettigheter
[!INCLUDE[d365fin](includes/d365fin_md.md)] inneholder et sett med utviklingsverktøy og en moderne plattform å bygge på, slik at du kan opprette dine egne tilleggsapper og bygge inn løsninger for å koble eller utvide [!INCLUDE[d365fin](includes/d365fin_md.md)].

[!INCLUDE[d365fin](includes/d365fin_md.md)] inneholder verktøy som du kan bruke til å implementere dine egne tillegg og bygge inn funksjoner for å legge til nye bransjespesifikke ende-til-ende-opplevelser eller integrere løsninger fra tredjeparter. Du kan for eksempel bruke en API til å bygge en tilkoblet app for datautveksling mellom [!INCLUDE[d365fin](includes/d365fin_md.md)] og din lønnsapp. Tilkoblingsapper kan også bruke utvidelser for å opprette sider som skal brukes for oppsett, konfigurasjon eller appspesifikke støttefunksjoner. Hvis du vil ha mer informasjon, kan du se [Utvikle apper for [!INCLUDE[d365fin](includes/d365fin_md.md)]](https://aka.ms/getstartedwithapps).

## <a name="see-also"></a>Se også
[Komme i gang](product-get-started.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

