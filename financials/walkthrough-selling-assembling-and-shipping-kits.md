---
title: "Gjennomgang – Selge, montere og levere sett | Microsoft-dokumentasjon"
description: "Hvis du vil støtte JIT-lager (Just In Time) og muligheten til å tilpasse produkter til kundens ønsker, kan monteringsordrer opprettes og kobles automatisk så snart ordrelinjen opprettes. Koblingen mellom salgsbehovet og monteringsforsyningen gjør det mulig for salgsordrebehandlere å tilpasse monteringsvaren og bekrefte leveringsdatoer i henhold til komponenttilgjengelighet. I tillegg bokføres monteringsforbruk og -avgang automatisk med leveringen av den tilknyttede ordren."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 015acdfbbc349477b9e86225f2c971f993215000
ms.contentlocale: nb-no
ms.lasthandoff: 01/30/2018

---
# <a name="walkthrough-selling-assembling-and-shipping-kits"></a>Gjennomgang: Selge, montere og levere sett
Hvis du vil støtte JIT-lager (Just In Time) og muligheten til å tilpasse produkter til kundens ønsker, kan monteringsordrer opprettes og kobles automatisk så snart ordrelinjen opprettes. Koblingen mellom salgsbehovet og monteringsforsyningen gjør det mulig for salgsordrebehandlere å tilpasse monteringsvaren og bekrefte leveringsdatoer i henhold til komponenttilgjengelighet. I tillegg bokføres monteringsforbruk og -avgang automatisk med leveringen av den tilknyttede ordren.  

Det finnes spesiell funksjonalitet for å styre leveringen av monter-til-ordre-antall, både i grunnleggende og i avanserte lagerkonfigurasjoner. Når medarbeidere som er ansvarlige for montering, er ferdige med monteringen av deler av eller hele montere-til-ordre-antallet, registrerer de dette i feltet **Levere (antall)** på lagerleveringslinjen, i avanserte oppsett, og velger deretter **Bokfør følgeseddel**. Resultatet er at den tilsvarende monteringsavgangen bokføres, inkludert det relaterte komponentforbruket, og en følgeseddel for antallet bokføres for den tilknyttede ordren. Denne gjennomgangen illustrerer den avanserte lagerprosessen.  

I grunnleggende lageroppsett bokfører den overordnede lagermedarbeideren en lagerplukking for ordrelinjene når et montere-til-ordre-antall er klart til å leveres. Deretter blir det opprettet en lagerflytting for komponentene, og monteringsavgangen og ordreforsendelsen blir bokført. Hvis du vil ha mer informasjon, kan du se delen Håndtere montere-til-ordre-varer i lagerplukk i Lagerplukk.  

## <a name="about-this-walkthrough"></a>Denne gjennomgangen  
Denne gjennomgangen viser følgende oppgaver:  

### <a name="setting-up-assembly-items"></a>Definere monteringsvarer  
Monteringsvarer kjennetegnes av etterfyllingssystemet og monteringsstykklisten. Varens monteringsprinsipp kan enten være montere-til-ordre (ATO) eller montere-til-lager (ATS). Denne delen dekker følgende oppgaver:  

-   Angi riktig etterfyllingssystem og monteringsprinsipp på et nytt monteringsvarekort.  
-   Opprette en monteringsstykkliste som viser monteringskomponentene og ressursen som inngår i monteringsvaren.  

### <a name="selling-customized-assembly-items"></a>Selge tilpassede monteringsvarer  
[!INCLUDE[d365fin](includes/d365fin_md.md)]  gir deg fleksibilitet til å angi et både lagerantall og et montere-til-ordre-antall på én salgsordrelinje. Denne delen dekker følgende oppgaver:  

-   Opprette en ren ATO-ordrelinje der det fullstendige antallet er utilgjengelig og må være montert før levering.  
-   Tilpasse ATO-varer.  
-   Beregne salgsprisen for en tilpasset monteringsvare på nytt.  
-   Opprette en blandet ordrelinje der deler av salgsantallet kommer fra lageret, og der den gjenstående delen må være montert før levering.  
-   Forstå advarsler om ATO-tilgjengelighet.  

### <a name="planning-for-assembly-items"></a>Planlegge for monteringsvarer  
Monteringsbehov og -forsyning håndteres av planleggingssystemet, akkurat som for kjøp, overføring og produksjon. Denne delen dekker følgende oppgaver:  

-   Kjøre en replanlegging for varer med salgsbehov for montert forsyning.  
-   Genererer en monteringsordre for å innfri salgslinjeantallet innen behovsdatoen for leveringen.  

### <a name="assembling-items"></a>Montere varer  
Monteringsordrer virker på lignende måte som produksjonsordrer, bortsett fra at forbruket og avgagnen registreres og bokføres direkte fra ordren. Når varene er montert til lager, har monteringsarbeideren full tilgang til alle hode- og linjefelt. Når varene monteres til en ordre der det er gitt løfter om antall og dato til kunden, kan ikke bestemte felt på monteringsordren redigeres. I dette tilfellet utføres monteringsbokføringen fra lagerleveringen for den tilknyttede ordren. Denne delen dekker følgende oppgaver.  

-   Registrere og bokføre monteringsforbruk og avgang til lager.  
-   Tilgang til en lagerfølgeseddellinje fra en ATO-monteringsordre for å registrere monteringsarbeid.  
-   Tilgang til en ATO-monteringsordre fra en lagerfølgeseddellinje for å gå gjennom automatisk registrerte data.  

### <a name="shipping-assembly-items-from-stock-and-assembled-to-order"></a>Levering av monteringsvarer, fra lager og montert til ordre  
Det finnes spesiell funksjonalitet for å styre leveringen av monter-til-ordre-antall. Denne delen dekker følgende oppgaver:  

-   Opprette et lagerplukk for monteringsvarer på lager og for monteringskomponenter som skal monteres før levering.  
-   Registrere lagerplukk for monteringskomponenter og deretter for monteringsvarer.  
-   Tilgang til en monteringsordre fra en lagerlevering for å gå gjennom plukkede eller forbrukte komponenter.  
-   Levering av montere-til-ordre-antall.  
-   Levering av monteringsvare på lager.  

## <a name="roles"></a>Roller  
Denne gjennomgangen viser oppgaver som utføres av følgende brukerroller:  

-   Ordrebehandler  
-   Planlegger  
-   Monteringsarbeider  
-   Plukker  
-   Ansvarlig for forsendelse  

## <a name="prerequisites"></a>Forutsetninger  
Før du kan utføre oppgavene i gjennomgangen, må du gjøre følgende:  

-   Installere [!INCLUDE[d365fin](includes/d365fin_md.md)].  
-   Gjør deg til lageransatt på lokasjonen KR.SAND ved å følge disse trinnene:  

1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Lageransatte**, og velg deretter den relaterte koblingen.  
2.  Velg feltet **Bruker-ID**, og velg din egen brukerkonto i **Brukere**-vinduet.  
3.  Skriv inn KR.SAND i **Lokasjonskode**-feltet.  
4.  Velg **Standard**- feltet.  

Klargjør lokasjonen KR.SAND for monteringsbehandling ved å følge disse trinnene:  

1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Lokasjoner**, og velg deretter den relaterte koblingen.  
2.  Åpne lokasjonskortet for lokasjonen KR.SAND.  
3.  I **Hyller**-hurtigfanen angir du **W-10-0001** i feltet **Til-Hyllekode for montering**.  

    Ved å angi denne hyllekoden som ikke plukk, blir alle monteringsordrelinjer klar til å motta sine komponenter i hyllen.  

4.  I feltet **Fra-Hyllekode for montering** angir **W-01-0001**.  

    Ved å angi denne plukkhyllekoden avgår ferdige monteringsvarer til hyllen.  

Fjern standard leveringstid for interne prosesser ved å følge disse trinnene:  

1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Produksjonsoppsett**, og velg deretter den relaterte koblingen.  
2.  I **Produksjonsoppsett** vinduet i **Planlegging**-hurtigfanen fjerner du verdien i feltet **Standard sikkerhetstid**.  

Opprett lager for monteringskomponenter ved å følge delen "Klargjøre eksempeldata" i denne gjennomgangen.  

## <a name="story"></a>Hovedscenario  
Den 23. januar tar ordrebehandleren Susanna en ordre fra Lydeksperten på tre enheter av sett B, som er en ATO-vare. Alle de tre enhetene er tilpasset, og de må inneholde sterke grafikkort og en ekstra RAM-blokk. Diskstasjonene er oppgradert til DWD fordi CD-stasjonene ikke er tilgjengelige. Heidi vet at enhetene kan monteres med en gang, så hun beholder\\\ den foreslåtte leveringsdatoen på 23. januar.  

Samtidig bestiller kunden femten enheter av sett A med en spesiell forespørsel om at fem enheter tilpasses til å inneholde det kraftige grafikkortet. Selv om sett A vanligvis er en monter til lager-vare, kombinerer ordrebehandleren salgslinjeantallene for å selge ti enheter fra lageret og montere fem tilpassede enheter til ordren. De ti enhetene i sett A er utilgjengelige og må først forsynes til lager ved hjelp av en monteringsordre i samsvar med varenes monteringsprinsipp. Heidi informeres fra monteringsavdelingen om at sett A-enheter ikke kan fullføres i den gjeldende uken. Hun angir den andre salgsordrelinjens leveringsdato, for det blandede ATO- og lagerantallet, til 27. januar og informerer kunden om at 15 enheter av sett A blir levert fire dager senere enn de tre enhetene av sett B. For å signalisere til transportavdelingen at denne ordren krever monteringsbehandling, oppretter Susanna lagerfølgeseddelen fra ordren.  

Eduardo, planleggeren, kjører planleggingsforslaget og genererer en monteringsordre på ti standardenheter av sett A med en intern forfallsdato den 27. januar.  

Sammy, som er ansvarlig for levering, henter tre lagerleveringslinjer for ordren: én linje for de tre rene ATO-enhetene, én linje for fem ATO-enhetene på blandet-ordrelinjen og én linje for ti ATS-enheter på ordrelinjen for blandet salg. Han oppretter et plukkdokument for alle monteringskomponentene som trengs for å sette sammen totalt åtte ATO-enheter på lagerleveringsdokumentet.  

Plukkeren Joakim henter komponenter til alle ATO-antallene på leveringsdokumentet og bringer dem til monteringsområdet. Han angir håndteringsantallet og registrerer plukkingen.  

Jorunn monterer de tre ATO-enhetene i sett B. Komponentene er allerede plukket, og hun registrerer ikke avgangs- og forbruksantall og bokfører ikke ordren, fordi begge disse handlingene utføres automatisk gjennom de tilknyttede lagerleveringslinjene.  

Sammy registrerer monteringsantallet på lagerleveringslinjen og bokfører leveringen av tre enheter av sett B. Den første linjen på ordren oppdateres som levert. Den koblede monteringsordren forblir åpen til salgsordren er fullstendig fakturert. De to lagerleveringslinjene, én ATO (monter til ordre) og én ATS (monter til lager), for sett A med forfallsdato 27. januar forblir åpne.  

27 januar behandler Jorunn to monteringsordrer for sett A. Den første ordren er ATO-ordren på fem enheter, som hun behandler annerledes enn ATO-ordren for sett B som hun behandlet 23. januar. På denne ordren har hun autorisert tilgang til lagerleveringslinjen selv for å registrere det fullførte monteringsarbeidet. De nødvendige komponentene er klare i monteringsavdelingen, slik de ble plukket sammen med komponenter for Kit B.  

Den andre monteringsordren er ATS-ordren for ti enheter som ble opprettet av planleggingssystemet. På ATS-ordren utfører Jorunn alle handlingene som monteringsordren omfatter. Hun oppretter et plukkdokument for monteringskomponentene som er trengs for å montere de ti enhetene. Når datamaskinene er montert, bokfører Linda monteringsordren og signaliserer dermed at varene er tilgjengelige på lager og at de kan plukkes for levering.  

Sammy oppretter et lagerplukkdokument for eventuelle antall som gjenstår før lagerleveringen kan bokføres. Et plukkdokument opprettes for ti enheter av sett A som nettopp er fullført. Komponentene som trengs for å montere de fem enhetene i pakke A til en ordre der den plukkes på 23. januar.  

Joakim bringer de ti enhetene av sett A lageret til det angitte leveringsområdet, registrerer antallet som skal håndteres og registrerer deretter plukket.  

Sammy pakker ti ATS enheter med de fem ATO-enhetene som Jorunn monterte tidligere på dagen. Han fyller ut antallet som skal leveres, på begge linjene og bokfører deretter siste levering for Lydeksperten. Den relaterte monteringsordren for fem enheter i sett A posteres automatisk. Den andre linjen på ordren oppdateres som levert. To koblede monteringsordrer holdes åpne til ordren er fakturert og lukket.  

Når ordren senere bokføres som fullstendig fakturert, fjernes ordren og de tilknyttede monteringsordrene.  

## <a name="setting-up-the-sample-data"></a>Konfigurere eksempeldataene  

1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Lagervarekladder**, og velg deretter den relaterte koblingen.  
2.  Velg feltet **Bunkenavn**, og velg deretter standardkladden.  
3.  Opprette positive lagerjusteringer på HVIT-lokasjonen på arbeidsdatoen, 23. januar, ved å skrive inn følgende informasjon.  

    |**Varenr.**|**Sonekode**|**Hyllekode**|**Antall**|  
    |-----------------------------------|---------------------------------------|--------------------------------------|------------------------------------|  
    |80001|PLUKK|W-01-0001|20|  
    |80005|PLUKK|W-01-0001|20|  
    |80011|PLUKK|W-01-0001|20|  
    |80014|PICK|A-01-0001|20|  
    |80203|PICK|A-01-0001|20|  
    |80209|PICK|A-01-0001|20|  

4.  I fanebladet **Hjem**, under **Registrering**, velger du **Registrer** og deretter **Ja**.  

    Deretter synkroniserer du nye lagerposter med lageret.  

5.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Varekladder**, og velg deretter den relaterte koblingen. **Varekladd**-vinduet åpnes.  
6.  I fanebladet **Handlinger**, under **Funksjoner** velger du **Beregn lagerjustering**.  
7.  I vinduet **Beregn lagerjust.** velger du **OK**-knappen.  
8.  Velg **Bokfør** under **Funksjoner** i fanebladet **Handlinger** i **Varekladd**-vinduet, og klikk deretter **Ja**-knappen.  

### <a name="creating-the-assembly-items"></a>Opprette monteringsvarer  

1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Varer**, og velg deretter den relaterte koblingen.  
2.  I fanebladet **Hjem**, under **Behandle**, velger du **Ny**.  
3.  Opprette den første monteringsvaren basert på følgende informasjon.  

    |Felt|Verdi|  
    |---------------------------------|-----------|  
    |**Beskrivelse**|Sett A – enkel PC|  
    |**Lagerenhet**|STK|  
    |**Varekategorikode**|Div.|  
    |**Etterfyllingssystem**|Montering|  
    |**Monteringsprinsipp**|Monter til lager|  
    |**Gjenbestillingsprinsipp**|Parti for parti|  

    > [!NOTE]  
    >  Sett A forsynes vanligvis av montering til lager og har derfor et gjenbestillingsprinsipp for å gjøre det til en del av den generelle forsyningsplanleggingen.  

4.  I fanebladet **Naviger**, under **Montering/Produksjon**, velger du **Montering** og deretter **Monteringsstykkliste**.  
5.  Definer en monteringsstykkliste for sett A med følgende informasjon.  

    |**Type**|**Nr.**|**Antall per**|  
    |-------------------------------|------------------------------|---------------------------------------|  
    |Element|80001|1|  
    |Element|80011|1|  
    |Element|80209|1|  
    |Ressurs|Thea|1|  

6.  Opprette den andre monteringsvaren basert på følgende informasjon.  

    |Felt|Verdi|  
    |---------------------------------|-----------|  
    |**Beskrivelse**|Sett B – proff PC|  
    |**Lagerenhet**|STK|  
    |**Varekategorikode**|Div.|  
    |**Etterfyllingssystem**|Montering|  
    |**Monteringsprinsipp**|Monter til ordre|  

    > [!NOTE]  
    >  Sett B er forsynes vanligvis av montering til ordre og har derfor ingen gjenbestillingsprinsipp, fordi det ikke skal være en del av generell forsyningsplanlegging.  

7.  I fanebladet **Naviger**, under **Montering/Produksjon**, velger du **Montering** og deretter **Monteringsstykkliste**.  
8.  Definer en monteringsstykkliste for sett B med følgende informasjon.  

    |**Type**|**Nr.**|**Antall per**|  
    |-------------------------------|------------------------------|---------------------------------------|  
    |Element|80005|1|  
    |Element|80014|1|  
    |Element|80210|1|  
    |Ressurs|Thea|1|  

### <a name="selling-the-assembly-items"></a>Selge monteringsvarer  

1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Ordrer**, og velg deretter den relaterte koblingen.  
2.  I fanebladet **Hjem**, under **Behandle**, velger du **Ny**.  
3.  Opprett to ordrelinjer for kunde 62000, Lydeksperten, på arbeidsdatoen med følgende informasjon.  

    |**Type**|**Beskrivelse**|**Antall**|Ant. som skal monteres til ordre|Forsendelsesdato|  
    |--------------|---------------------|------------------|-------------------------------|-------------------|  
    |Vare|Sett B – proff PC|3|3|23. januar|  
    |Vare|Sett A – enkel PC|15|5|27. januar|  

    > [!NOTE]  
    >  Følgende tilgjengelighetsproblem foreligger for ordrelinjen for sett B:  
    >   
    >  -   Monteringskomponenten 80210 er ikke tilgjengelig. Dette betyr at de tre angitte enhetene av pakke B ikke kan monteres, som angitt av **0** i **Kan montere**-feltet i vinduet **Montering – tilgjengelighet**.  
    >   
    >  Følgende tilgjengelighetsproblem foreligger for ordrelinjen for sett A:  
    >   
    >  -   De ti enhetene i sett A er ikke tilgjengelige. Dette forteller planleggingssystemet at antallet må være montert til lager.  

    Deretter tilpasser du salgsordren.  

4.  Velg ordrelinjen for tre enheter av sett B.  
5.  På hurtigfanen **Linjer**, velg **Linje**, **Monter til ordre**, og deretter **Montere til ordre – linjer**.  
6.  I **Montere til ordre – linjer**-vinduet på monteringsordrelinjen for vare 80014 angir du **2** i **Antall per**-feltet.  
7.  På monteringsordrelinjen for vare 80210 velger du **Nr.**-feltet og velger deretter vare 80209 i stedet.  
8.  Opprett en ny monteringsordrelinje med følgende informasjon.  

    |Type|Nr.|Antall per|  
    |----------|---------|------------------|  
    |Element|80203|1|  

9. Lukk vinduet **Montere til ordre – linjer**.  

    Deretter oppdaterer du enhetsprisen for pakke B i henhold til tilpasningen du nettopp utførte. Legg merke til den gjeldende verdien i feltet **Salgspris Ekskl. mva**.  

10. På hurtigfanen **Linjer** velger du **Linje**, **Monter til ordre**, og deretter **Oppruller pris**.  
11. Velg **Ja**-knappen. Legg merke til den økte verdien i feltet **Salgspris Ekskl. mva**.  
12. Velg ordrelinjen for 15 enheter av sett A.  
13. På hurtigfanen **Linjer**, velg **Linje**, **Monter til ordre**, og deretter **Montere til ordre – linjer**.  
14. I vinduet **Montere til ordre – linjer** oppretter du en ny monteringsordre med følgende informasjon.  

    |Type|Nr.|Antall per|  
    |----------|---------|------------------|  
    |Vare|80203|1|  

     Deretter endrer du leveringsdatoen for den andre salgsordrelinjen i henhold til monteringsplanen.  

15. På ordrelinjen for 15 enheter av sett A angir du **27.01.2014** i **Forsendelsesdato**-feltet.  
16. I fanebladet **Handlinger**, under **Frigi** velger du **Frigi**.  
17. I fanebladet **Handlinger**, under **Lager** velger du **Opprett lagerlevering**.  
18. Lukk ordren.  

### <a name="planning-for-the-unavailable-ats-items"></a>Planlegge for utilgjengelig ATS-varer  

1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Planleggingsforslag**, og velg deretter den relaterte koblingen.  
2.  I fanebladet **Handling**, under **Funksjoner** velger du **Beregn replanlegging**.  
3.  Angi følgende filtre i **Beregn Plan**-vinduet.  

    |Startdato|Sluttdato|Nr.|  
    |-------------------|-----------------|---------|  
    |23.01.2014|27.01.2014|Sett A – enkel PC|  

4.  Velg **OK**-knappen.  

    En ny planleggingslinje opprettes for den nødvendige monteringsordren på ti varer med forfallsdato 27. januar. Den trenger ingen endringer, så du kan opprette ordren nå.  

5.  I fanebladet **Handlinger**, under **Funksjoner** velger du **Utfør handlingsmelding**.  
6.  Velg **Monteringsordre**-feltet i vinduet **Utfør handlingsmeld.**, og velg deretter **Lag monteringsordrer**.  
7.  Velg **OK**.  

### <a name="assembling-and-shipping-the-first-ato-quantity"></a>Montere og levere første ATO-antall  

1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Lagerlevering**, og velg deretter den relaterte koblingen.  

    > [!NOTE]  
    >  I denne delen er personen som er ansvarlig for levering, ansvarlig for å registrere fullført ATO-monteringsarbeid på lagerleveringslinjen. Denne arbeidsflyten kan oppstå i miljøer hvor monteringsarbeidet utføres av personen som er ansvarlig for levering, eller av monteringsarbeidere i leveringsområdet.  
    >   
    >  I denne delen utføres handlinger på monteringsordren indirekte fra lagerleveringslinjen. Hvis du vil ha mer informasjon om hvordan du behandler en monteringsordre direkte, kan du se delen "Monteringsvarer til lager" i denne gjennomgangen.  

2.  Åpne den nyeste lagerfølgeseddelen som er opprettet på lokasjonen KR.SAND.  

    Legg merke til de tre lagerleveringslinjene: én linje for ATO-antall av sett B som forfaller 23. januar. Én linje for ATO-antall av sett A som forfaller 27. januar. Én linje for varebeholdningen av sett A som forfaller 27. januar.  

    Feltet **Monter til ordre** angir monteringsmetoden.

    Deretter oppretter du et plukkdokument for alle ATO-monteringskomponentene er nødvendige på lagerleveringen.  

3.  I fanebladet **Handlinger**, under **Funksjoner** velger du **Opprett plukk** og deretter **OK**.  

    Deretter utfører du plukkerens siste oppgave.  

4.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Plukking**, og velg deretter den relaterte koblingen.  
5.  Åpne lagerplukkdokumentet som du opprettet i trinn 3 i denne delen.  

    Legg merke til verdien i **Kildedokument**-feltet og at alle plukklinjene er for monteringskomponenter.  

    Deretter registrerer du plukkingen uten å endre standardinformasjon.  

6.  I fanebladet **Handlinger**, under **Funksjoner** velger du **Autoutfyll ant. som skal hndt.**.  
7.  I fanebladet **Hjem**, under **Registrering**, velger du **Registrer plukk**.  

    Gå tilbake til å utføre leveringsoppgavene.  

8.  Åpne vinduet **Lagerlevering** på nytt.  

    Legg merke til at feltet **Plukket ant.** fortsatt er tomt på alle linjene. Dette er fordi du fortsatt ikke har plukket varene som skal leveres, men bare komponentene som kreves for å sette sammen ATO-antallene.  

    Fortsett med å se gjennom den tilknyttede monteringsordren.  

9. Velg leveringslinjen for tre enheter av sett B.  
10. På hurtigfanen **Linjer** velger du **Linje**, og deretter **Monter til ordre**. Vinduet **Monteringsordre** åpnes.  

    Legg merke til at flere felt på monteringsordren er utilgjengelige fordi ordren er koblet til en salgsordre.  

    Legg merke til at feltet **Plukket ant.** er fylt ut på monteringsordrelinjene. Dette er på grunn av plukkingen du registrerte i trinn 7 i denne delen.  

11. Prøv å angi en lavere verdi enn **3** i feltet **Antall å montere**.  

    Les feilmeldingen som forklarer hvorfor dette feltet bare kan fylles ut gjennom **Levere (antall)**-felt på den tilknyttede forsendelsen.  

    Feltet **Antall å montere** er redigerbart for å støtte situasjoner der du vil levere en beholdning delvis i stedet for å montere flere enheter til ordren. Hvis du vil ha mer informasjon, kan du se delen "Kombinasjonsscenarier" i [Forstå montere til ordre og montere til lager](assembly-assemble-to-order-or-assemble-to-stock.md).  

12. Lukk **Monteringsordre**-vinduet for å gå tilbake til **Lagerlevering**-vinduet.  
13. På leveringslinjen for tre enheter av sett B, i feltet **Levere (antall)**, angir du **3**.  
14. I fanebladet **Handlinger**, under **Bokføring** velger du **Bokfør følgeseddel** og deretter **Lever**.  

    Sammen med denne lagerleveringsbokføringen bokføres fullt forbruk og avgangsantall for den relaterte monteringsordren, og feltet **Restantall** er tomt. Salgsordrelinjen for sett B oppdateres og viser at de tre enhetene er levert.  

    Lageraktivitetene for å innfri den første ordrelinjen innen 23. januar, er fullført. Nå kan du oppfylle salgsordrelinjene som skal leveres 27. januar.  

### <a name="assembling-and-recording-the-second-ato-quantity"></a>Montere og registrere andre ATO-antall  

1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Monteringsordrer**, og velg deretter den relaterte koblingen.  

    Legg merke til at ATO-ordren for leverte enheter av sett B fremdeles er i listen, selv om **Restantall** er tomt. Dette er fordi den tilknyttede ordren fortsatt ikke er fullstendig fakturert.  

    > [!NOTE]  
    >  I denne delen er monteringsarbeideren ansvarlig for registrering av fullført ATO-monteringsarbeid på lagerleveringslinjen. Denne arbeidsflyten kan oppstå i miljøer hvor monteringsarbeidet utføres i en separat monteringsavdeling og monteringsarbeidere er autorisert til å endre lagerleveringslinjen.  

2.  Åpne ATO-monteringsordren for fem enheter av sett A  

    Legg merke til at feltet **Antall å montere** og **Antall som skal forbrukes** er tomt siden det ikke er registrert noe arbeid ennå.  

    Legg merke til at feltet **Plukket ant.** er fylt ut på monteringsordrelinjene. Dette er på grunn av plukkingen som ble registrert den 23. januar.  

    Deretter registrere du at monteringsordren er fullført.  

3.  I fanebladet **Naviger**, under **Lager**, velger du **Monter til ordre – lagerfølgeseddellinje**.  
4.  Angi **5** i feltet **Levere (antall)** i vinduet **Monter til ordre – lagerfølgeseddellinje**, og lukk deretter vinduet.  

    Legg merke til at i vinduet **Monteringsordre** er feltene **Antall å montere** og **Antall som skal forbrukes** nå fylt ut med avgangs- og forbruksantallene som vil bli bokført med leveringen.  

5.  Lukk vinduet **Monteringsordre**.  

### <a name="assembling-the-ats-quantity"></a>Montere ATS-antall  

1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Monteringsordrer**, og velg deretter den relaterte koblingen.  
2.  Åpne monteringsordren for ti enheter av sett A  

    Legg merke til at feltet **Antall å montere** er fylt ut med forventet antall.  

    Deretter oppretter du et plukkdokument for å hente de nødvendige komponentene.  

3.  I fanebladet **Handlinger**, under **Frigi** velger du **Frigi**.  
4.  I fanebladet **Handlinger**, under **Lager** velger du **Opprett plukk** og deretter **OK**.  

    Deretter utfører du plukkerens siste oppgave.  

5.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Plukking**, og velg deretter den relaterte koblingen.  
6.  Åpne lagerplukkdokumentet som du opprettet i trinn 4 i denne delen.  

     Fortsett med å registrere plukkingen uten å endre standardinformasjon.  

7.  I fanebladet **Handlinger**, under **Funksjoner** velger du **Autoutfyll ant. som skal hndt.**.  
8.  I fanebladet **Hjem**, under **Registrering**, velger du **Registrer plukk**.  

    Gå tilbake til monteringsfordren for å utføre den siste monteringsoppgaven.  

9. Velg **Bokfør** under **Bokføring** i fanebladet **Handlinger** i **Monteringsordre**, og velg deretter **Ja**-knappen.  

    Legg merke til at monteringsordren er fjernet fra listen over åpne ordrer.  

### <a name="shipping-the-remaining-items-partly-from-stock-and-partly-assembled-to-the-order"></a>Levering av gjenværende varer, delvis fra lager og delvis montert til ordre  

1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Lagerlevering**, og velg deretter den relaterte koblingen.  
2.  Åpne den nyeste lagerfølgeseddelen som er opprettet på lokasjonen KR.SAND.  

    Legg merke til at på linjen for ti enheter av sett A er feltene **Levere (antall)** og **Plukket ant.** tomme.  

    Deretter plukker du eventuelle gjenværende varer.  

3.  I fanebladet **Handlinger**, under **Funksjoner** velger du **Opprett plukk** og deretter **OK**.  

    Deretter utfører du plukkerens siste oppgave for denne lagerleveringen.  

4.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Plukking**, og velg deretter den relaterte koblingen.  
5.  Åpne lagerplukkdokumentet som du opprettet i trinn 3 i denne delen.  

    Legg merke til at dette plukkdokumentet er for monteringsvare, ikke for monteringskomponenter.  

    Deretter registrerer du plukkingen uten å endre standardinformasjon.  

6.  I fanebladet **Handlinger**, under **Funksjoner** velger du **Autoutfyll ant. som skal hndt.**.  
7.  I fanebladet **Hjem**, under **Registrering**, velger du **Registrer plukk** og deretter **Ja**.  

    Gå tilbake til lagerleveringen for å utføre den siste oppgaven.  

8.  Åpne vinduet **Lagerlevering** på nytt.  

    Legg merke til at feltet **Levere (antall)** og **Plukket ant.** på linjen for ti enheter av sett A i vinduet **Lagerlevering** nå inneholder **10**.  

9. I fanebladet **Handlinger**, under **Bokføring** velger du **Bokfør følgeseddel** og deretter **Levert**.  

    Lagerfølgeseddelen fjernes, som indikerer at de involverte lageraktivitetene er fullført. Deretter kontrollerer du at salgsordren har blitt behandlet.  

10. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Ordrer**, og velg deretter den relaterte koblingen.  
11. Åpne salgsordren for Lydeksperten.  

    Legg merke til at feltet **Levert (antall)** inneholder hele antallet på begge linjer.  

    Når Lydeksperten betaler for mottaket av 18 datamaskiner fra CRONUS, fjernes ordren og de tilknyttede monteringsordrene.  

## <a name="see-also"></a>Se også  
 [Forstå montere til ordre og montere til lager](assembly-assemble-to-order-or-assemble-to-stock.md)   
 [Montere elementer](assembly-how-to-assemble-items.md)   
 [Plukke varer for lagerlevering](warehouse-how-to-pick-items-for-warehouse-shipment.md)   
 [Selge varer som er montert til ordre](assembly-how-to-sell-items-assembled-to-order.md)   
 [Montere elementer](assembly-how-to-assemble-items.md)   
 [Designdetaljer: Bokføre monteringsordre](design-details-assembly-order-posting.md)   
 [Designdetaljer: Interne lagerflyter](design-details-internal-warehouse-flows.md)   
 [Designdetaljer: Utgående lagerflyt](design-details-outbound-warehouse-flow.md)   
 [Gjennomgang: planlegge forsyninger automatisk](walkthrough-planning-supplies-automatically.md)

