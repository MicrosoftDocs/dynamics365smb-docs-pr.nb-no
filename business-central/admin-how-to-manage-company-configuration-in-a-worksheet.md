---
title: Behandle selskapskonfigurasjon i et forslag
description: Hvis du bruker RapidStart Services, er konfigurasjonsforslaget den sentrale plasseringen der du kan planlegge, spore og utføre selskapskonfigurasjonsarbeidet ditt.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.form: 8632
ms.date: 06/14/2021
ms.author: edupont
ms.openlocfilehash: c678d48b202043110627a2c8b29ae12be045d38d
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2022
ms.locfileid: "8514203"
---
# <a name="manage-company-configuration-in-a-worksheet-with-rapidstart-services"></a>Behandle selskapskonfigurasjon i et forslag med RapidStart Services

Konfigurasjonsforslaget er den sentrale plasseringen der du kan planlegge, spore og utføre konfigurasjonsarbeidet ditt. Du kan opprette et forslag for hvert selskap du arbeider med, eller du kan opprette et standard konfigurasjonsforslag som kan brukes til å konfigurere flere identiske selskaper.  

Det første trinnet for klargjøring av en konfigurasjonspakke er å velge et selskap som du allerede har definert og endret i henhold til løsningsbehovene dine. Dette selskapet fungerer som grunnlag for konfigurasjon av nye selskaper. I forslaget angir du tabellene du vil at konfigurasjonen skal kontrollere og håndtere. Siden de fleste tabeller i [!INCLUDE[prod_short](includes/prod_short.md)] har relasjoner og avhengigheter til andre tabeller, bør du også inkludere disse relaterte tabellene etter behov. Sammen fungerer disse tabellene som strukturen du bygger et nytt selskap rundt. De etterfølgende trinnene hjelper deg med å pakke og distribuere konfigurasjonen.  

For å forenkle sporing og gjennomgang av arbeidet bruker du faktaboksen **Konfig.pakketabell** til å vise informasjon om poster. Bruk av faktaboksen **Konfig.relatert tabeller** for å overvåke tabellrelasjoner.  

Fremgangsmåtene nedenfor viser hvordan du legger til og tilpasser tabellinformasjon for konfigurasjonen.  

## <a name="to-open-the-configuration-worksheet"></a>Åpne konfigurasjonsforslaget

1.  I [!INCLUDE[prod_short](includes/prod_short.md)] åpner du selskapet som er grunnlinjen for konfigurasjonen.  
2.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Konfigurasjonsforslag**, og velg deretter den relaterte koblingen.  

## <a name="to-add-a-table-to-the-worksheet"></a>Legge til en tabell i forslaget  
1.  På siden **Konfigurer forslag** velger du **Rediger oversikt**-handlingen.  
2.  På den første tilbudslinjen i feltet **Linjetype** velger du **Tabell**.  
4.  Velg tabellen du vil legge til i konfigurasjonen, i feltet **Tabell-ID**.  
5.  I feltet **Side-ID** angi ID-en for siden som er knyttet til tabellen. For standardtabeller fylles denne verdien ut automatisk. For egendefinerte tabeller må du angi ID-en.
6.  I feltet **Referanse** angir du en URL-adresse til en dokumentasjonsside, for eksempel i Hjelp, som inneholder informasjon om anbefalte fremgangsmåter eller instruksjoner for hvordan du definerer tabellen.  
7.  Hvis du vil legge til relaterte tabeller, velger du handlingen **Hent relaterte tabeller**.  

    > [!NOTE]  
    > Relaterte tabeller legges ikke til med handlingen **Hent relaterte tabeller** hvis noe av det følgende gjelder:
    > - Relasjonen er betinget.  
    >     Eksempel: Hvis du får relaterte tabeller for **Kunde**-tabellen, blir ikke **Lokasjon**-tabellen lagt til siden den bare er betinget relatert til **Kunder**-tabellen, nemlig hvis feltet **Lokasjonskode** i **Kunder**-tabellen er fylt ut.  
    > - Den tilknyttede tabellen filtreres.  
    >     Eksempel: Et felt i den relaterte tabellen har en WHERE-setningsdel. Årsaken til dette er at den involverte relasjonsinformasjon er lagret i systemtabellen **Felt**, som ikke er fullstendig tilgjengelig for programmet.  
    > Du må legge til slike tabelltyper manuelt ved å følge trinn 4 i denne fremgangsmåten.  

8.  Hvis du vil endre listen over tabeller, merker du en tabell som du vil fjerne, og deretter velger du handlingen **Slett**.  
9. Gjenta trinnene for hver tabell du vil legge til i konfigurasjonen.  
10. Du kan fjerne duplisert tabellinformasjon, som kan skyldes bruk av handlingen **Hent relaterte tabeller**, ved å velge handlingen **Slett dupliserte linjer**. Dermed fjernes like tabeller som har samme pakkekode.  

## <a name="to-add-multiple-tables-to-the-configuration-worksheet"></a>Slik legger du til flere tabeller i konfigurasjonsforslaget:  
1. Velg handlingen **Hent tabeller**. Kjørselssiden **Hent konfig.tabeller** åpnes.  
2. På hurtigfanen **Alternativer** angir du hvilke tabelltyper du vil legge til i konfigurasjonen, som beskrevet i tabellen nedenfor.

    |Alternativ|Description|  
    |----------------------------------|---------------------------------------|  
    |**Inkluder bare med data**|Merk avmerkingsboksen for å bare inkludere tabeller som inneholder data. Du vil for eksempel kanskje ta med en tabell som allerede definerer de typiske betalingsbetingelsene som løsningen støtter.|  
    |**Inkluder relaterte tabeller**|Merk avmerkingsboksen for å inkludere alle relaterte tabeller. Hvis du vil legge til et delsett med relaterte tabeller, kan du se trinn 3 i denne prosedyren.|  
    |**Inkluder dimensjonstabeller**|Merk avmerkingsboksen for å inkludere dimensjonstabeller.|  
    |**Inkluder bare lisensierte tabeller**|Velg avmerkingsboksen for å bare inkludere tabeller som lisensen du oppretter regnearket under gir deg tilgang til.|

3. På hurtigfanen **Objekt** definerer du filtre etter behov for å angi hvilke tabelltyper du vil inkludere eller ekskludere.  
4. Velg **OK**-knappen. [!INCLUDE[prod_short](includes/prod_short.md)]-tabeller legges til i regnearket. Hver post i listen har linjetypen **Tabell**.  
5. Du kan fjerne duplisert tabellinformasjon, som kan skyldes bruk av handlingen **Hent tabeller**, ved å velge handlingen **Slett dupliserte linjer**. Dermed fjernes like tabeller som har samme pakkekode.  
6. Du kan legge til tabeller i forslaget som er relatert til en tabell du har valgt. Se gjennom opplysningene i faktaboksen **Relaterte tabeller** for å se om det er manglende tabeller. Hvis du vil legge til relaterte tabeller for en bestemt tabell, velger du tabellen i listen. Deretter velger du handlingen **Hent relaterte tabeller**.  

    > [!NOTE]  
    > Relaterte tabeller legges ikke til med handlingen **Hent relaterte tabeller** hvis noe av det følgende gjelder:
    > - Relasjonen er betinget.  
    > Eksempel: Hvis du får relaterte tabeller for **Kunde**-tabellen, blir ikke **Lokasjon**-tabellen lagt til siden den bare er betinget relatert til **Kunder**-tabellen, nemlig hvis feltet **Lokasjonskode** i **Kunder**-tabellen er fylt ut.  
    > - Den tilknyttede tabellen filtreres.  
    > Eksempel: Et felt i den relaterte tabellen har en WHERE-setningsdel. Årsaken til dette er at den involverte relasjonsinformasjonen er lagret i den virtuelle tabellen **Felt** og ikke er tilgjengelig på sider, for eksempel konfigurasjonsregnearket for ytelseshensyn.  
    > Du må legge til relaterte tabeller med slike komplekse relasjoner manuelt ved å følge trinn 4 i [Legge til en tabell i forslaget](admin-how-to-manage-company-configuration-in-a-worksheet.md#to-add-a-table-to-the-worksheet).

7. Hvis du vil slette tabeller i listen over tabeller, merker du en tabell som du vil fjerne, og deretter velger du handlingen **Slett**.  

Bruk den neste fremgangsmåten til å angi hvilke tabellfelt som skal inkluderes. Når du har angitt denne spesifikasjonen, kan du eksportere tabellen til Excel og bruke tabellstrukturen som en mal for innsamling av kundedata. Hvis du vil ha mer informasjon, kan du se [Klargjøre for å flytte kundedata](admin-use-templates-to-prepare-customer-data-for-migration.md).  

## <a name="to-specify-a-set-of-fields-and-records-for-a-configuration-table"></a>Slik angir du et sett med felt og poster for en konfigurasjonstabell:  
1. Velg en tabell i listen over konfigurasjonstabeller, og velg deretter handlingen **Rediger oversikt**.  
2. Velg en tabell du vil endre angi feltinformasjon for og deretter handlingen **Felt**.  
3. Hvis du bare vil velge felt du vil inkludere, velger du handlingen **Fjern inkludert**. Hvis du vil legge til alle felt, velger du handlingen **Sett inkludert**.  
4. Hvis du vil angi at feltdataene ikke skal valideres, fjerner du merket for **Valider felt** for feltet.  
5. Velg **OK**-knappen.  
6. Når du skal filtrere et bestemt sett med poster som skal tas med i konfigurasjonsforslaget, velger du handlingen **Filtre** og angir deretter filterverdiene du vil bruke.

Du kan opprette funksjonalitetsområder og grupper med tabeller i forslaget for å plassere lignende funksjonalitet sammen. Når du oppretter kontoplanen for konfigurasjonen, kan du for eksempel opprette en gruppe med bokføringstabeller. Områder brukes vanligvis til å gruppere et sett med tabeller som svarer til et funksjonsområde. Hvert område kan inneholde grupper. En gruppe kan brukes til å ordne tabeller som har en felles betydning, sammen.  

Følgende fremgangsmåte beskriver hvordan du legger til område- og gruppebetegnelser etter at du har opprettet den første listen over tabeller. Når du har lagt til disse kategoriene, kan du fortsette å legge til og endre listen over tabeller.  

## <a name="to-categorize-and-group-functionality-in-the-worksheet"></a>Slik kategoriserer og grupperer du funksjonalitet i forslaget:  
1. I begynnelsen av et område kan du sette inn en ny linje i regnearket.  
2. Velg **Område** i **Linjetype**-feltet. Angi et navn for området i feltet **Navn**.  
3. I begynnelsen av en gruppering av tabeller kan du sette inn en ny linje i regnearket.  
4. Velg **Gruppe** i **Linjetype**-feltet. Angi et navn for området i feltet **Navn**. Gruppenavnet rykkes inn automatisk.  
5. Hvis du vil flytte tabeller til den aktuelle kategorien, velger du tabellen du vil flytte, og deretter velger du handlingen **Flytt opp** eller **Flytt ned**. Du kan også slette en forslagslinje og sette inn tabellen på nytt på den påkrevde plasseringen.  

Noen [!INCLUDE[prod_short](includes/prod_short.md)]-tabeller er standard, og dataene i dem endrer seg sannsynligvis ikke fra implementering til implementering. For å hjelpe kunden med å fokusere kan du derfor fjerne disse tabellene fra forslaget etter at du har inkludert dem i konfigurasjonspakken. Når tabellene er lagt til, forblir de en del av konfigurasjonspakken.  

## <a name="to-remove-a-standard-table-in-the-worksheet"></a>Fjerne en standardtabell i regnearket  
Når du har lagt til alle nødvendige tabeller i en konfigurasjonspakke, kan du bestemme hvilke tabeller som ikke vil kreve kundens oppmerksomhet.  
1.  Velg tabellene, og deretter slette dem ved å velge handlingen **Slett**.  

    > [!NOTE]  
    >  Tabellene blir pakken selv om de slettes fra forslaget.  

## <a name="to-review-and-customize-existing-database-data"></a>Se gjennom og tilpasse eksisterende databasedata
Når du oppretter en konfigurasjonpakke for en løsning, kan du vise og tilpasse de tilgjengelige databasedataene etter kundens behov. Databasetabellen må ha en tilknyttet side.  

## <a name="to-customize-data-in-the-database"></a>Slik tilpasser du data i databasen:  

1.  På siden **Konfigurasjonsforslag** identifiserer du tabellene med data som du vil vise eller tilpasse.  

    > [!NOTE]  
    >  Kontroller at hver tabell er tilordnet en side-ID. For standard [!INCLUDE[prod_short](includes/prod_short.md)]-tabeller, fylles denne verdien ut automatisk. For egendefinerte tabeller må du oppgi ID\-en.  

2.  Velg handlingen **Databasedata**.  

     Siden [!INCLUDE[prod_short](includes/prod_short.md)] for siden åpnes.  

3.  Se gjennom informasjonen som er tilgjengelig. Endre den etter behov ved å slette poster som ikke er relevante eller ved å legge til nye.

## <a name="see-also"></a>Se også  
[Definere selskapskonfigurasjon](admin-set-up-company-configuration.md)  
[Konfigurere et selskap med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administrasjon](admin-setup-and-administration.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]