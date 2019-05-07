---
title: Om produksjonsordrer | Microsoft-dokumentasjon
description: Produksjonsordrer brukes til å håndtere konverteringen av kjøpt materiale til produserte varer. Produksjonsordrer (prosjekt- eller arbeidsordrer) dirigerer arbeid gjennom ulike innretninger (arbeidssentre eller produksjonsressurser) i produksjonen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: b02aa262089d5c341fb3b535f2af82c7085e99ee
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2019
ms.locfileid: "937924"
---
# <a name="about-production-orders"></a>Om produksjonsordrer
Produksjonsordrer brukes til å håndtere konverteringen av kjøpt materiale til produserte varer. Produksjonsordrer dirigerer arbeid gjennom ulike arbeidssentre eller produksjonsressurser i produksjonen.  

Før videre produksjon utfører de fleste firmaer forsyningsplanlegging, vanligvis én gang i uken, for å beregne hvor mange produksjonsordrer og bestillinger som skal utføres for å dekke ukens salgsbehov. Bestillinger gir komponentene som er nødvendige i henhold til produksjonsstykklisten, for å produsere sluttvarene.

Produksjonsordrer er de sentrale komponentene i programmets produksjonsfunksjonalitet og inneholder følgende informasjon:  

-   produkter som er planlagt for produksjon  
-   materialer som trengs i den planlagte produksjonen  
-   produkter som nettopp er produsert  
-   materialer som allerede er valgt ut  
-   produkter som har blitt produsert tidligere  
-   materialer som ble brukt i tidligere produksjonsoperasjoner  

Produksjonsordrer er utgangspunkt for:  

-   planlegging av fremtidig produksjon  
-   styring av gjeldende produksjon  
-   sporing av ferdig produksjon  

## <a name="production-order-creation"></a>Opprette produksjonsordrer  
Produksjonsordrer kan opprettes manuelt etter hvert som det er behov for dem, på **Produksjonsordre**-siden, eller de kan genereres fra siden **Salgsordreplanlegging** eller **Ordreplanlegging**. Du kan opprette flere ordrer på **Planleggingsforslag**-siden.  

Produksjonsordrer opprettes ved å bruke informasjon fra:  

- Varer  
- Prod.stykklister
- Ruter  
- Produksjonsressurser  
- Arbeidssentre  

## <a name="limitations-on-production-order-creation"></a>Begrensninger på oppretting av produksjonsordrer  
Produksjonsordrer blir automatisk reservert og sporet til kilden når:  

-   de opprettes fra **Planleggingsforslag**  
-   De opprettes med ordrefunksjonen på **Ordreplanlegging**-siden  
-   De opprettes fra **Ordreplanlegging**-siden  
-   funksjonen **Planlegg på nytt** brukes på produksjonsordrer  

Hvis du vil ha mer informasjon, kan du se [Spore relasjoner mellom behov og forsyning](production-how-track-demand-supply.md).

Produksjonsordrer som opprettes på andre måter, blir ikke automatisk reservert og sporet.   

## <a name="production-order-status"></a>Produksjonsordrestatus  
Statusen for produksjonsordren styrer hvordan produksjonsordren skal fungere i programmet. Produksjonsformen og -innholdet dikteres av ordrens status. Produksjonsordrene vises på forskjellige sider i henhold til statusen. Du kan ikke endre statusen til en produksjonsordre manuelt. Du må bruke **Endre status**-funksjonen.  

### <a name="simulated-production-order"></a>Simulert produksjonsordre  
Den simulerte produksjonsordren er unik basert på følgende egenskaper:  

- Som navnet antyder er den en simulasjon, og den brukes hovedsakelig i forbindelse med tilbud og kost, for eksempel når avdelingen for forskning og utvikling vil ha en kostberegning for en foreslått vare. En simulert produksjonsordre fungerer som et eksempel på en produksjonsordre.  
- Den påvirker ikke planleggingen av ordrer. Planlegging (MPS og MRP) verken tar hensyn til eller påvirkes av simulerte produksjonsordrer. En simulert produksjonsordre kan heller ikke brukes som en mal siden den forsvinner når du endrer statusen til den.  

### <a name="planned-production-order"></a>Planlagt produksjonsordre  
Den planlagte produksjonsordren er unik på grunn av følgende egenskaper:  

- Du kan opprette en planlagt produksjonsordre automatisk fra en ordre.  
- Planlagte produksjonsordrer er som frigitte produksjonsordrer og sender inndata til kapasitetsplanlegging ved å vise samlet kapasitetsbehov etter arbeidssenter eller produksjonsressurs.  
- Planlagte produksjonsordrer representerer det beste overslaget av fremtidig belastning for arbeidssenteret eller produksjonsressursbelastning basert på tilgjengelig informasjon. De genereres vanligvis fra planlegging, men de kan også opprettes manuelt. Siden de slettes av etterfølgende planleggingsgenereringer, er ikke manuell oppretting praktisk.  
- Når de genereres i planleggingen, blir resultatet en foreslått "planlagt ordrefrigivelse" som inkluderer antall, frigivelsesdato og forfallsdato. Logikken i planleggingssystemet er basert på etterfyllingssystemet, gjenbestillingsprinsippene og ordremodifikatorene som oppstår i nettobehovsplanleggingen.  
- Hvis du vil vise påvirkningen deres, kan du undersøke belastningen på hvert arbeidssenter eller hver produksjonsressurs i den planlagte produksjonsordrens rute.  

### <a name="firm-planned-production-order"></a>Fast planlagt produksjonsordre  
Den fast planlagte produksjonsordren er unik på grunn av følgende egenskaper:  

- Du kan opprette en fast planlagt produksjonsordre automatisk fra en ordre.  
- En fast planlagt produksjonsordre fungerer som en plassholder i planleggingstidsplanen for et fremtidig prosjekt som frigis til produksjon.  
- En fast planlagt produksjonsordre kan genereres fra planlegging eller opprettes manuelt eller fra ordrer. De slettes ikke under etterfølgende planlegging.  
- Når de genereres i planleggingen, blir resultatet en foreslått "planlagt ordrefrigivelse" som inkluderer antall, frigivelsesdato og forfallsdato. Logikken i planleggingssystemet er basert på etterfyllingssystemet, gjenbestillingsprinsippene og ordremodifikatorene som oppstår i nettobehovsplanleggingen.  
- Hvis du vil vise påvirkningen deres, kan du undersøke belastningen på hvert arbeidssenter eller hver produksjonsressurs i den fast planlagte produksjonsordrens rute.  

### <a name="released-production-order"></a>Frigitt produksjonsordre  
Den frigitte produksjonsordren er unik basert på følgende egenskaper:  

- Du kan opprette en frigitt produksjonsordre automatisk fra en ordre.  
- Når en produksjonsordre er frigitt, betyr det ikke nødvendigvis at materialer er plukket, eller at prosjektet er fysisk flyttet til den første operasjonen.  
- I et produser-til-ordre-miljø er det ikke uvanlig å opprette en frigitt produksjonsordre like etter posten for ordren.  
- Faktisk materialforbruk og produktavgang kan registreres manuelt i en frigitt produksjonsordre. I tillegg oppstår automatisk lagertrekk for forbruk og produktavgang bare for frigitte produksjonsordrer.  

### <a name="finished-production-order"></a>Ferdig produksjonsordre  
Den ferdige produksjonsordren er unik basert på følgende egenskaper:  

- En ferdig produksjonsordre er vanligvis en som er produsert.  
- Det er viktig å gjøre ferdig produksjonsordren for å fullføre kostlivssyklusen til varen som produseres. Når du gjør ferdig en produksjonsordre, kan kost justeres og avstemmes.  
- Ferdige produksjonsordrer brukes til statistisk rapportering og bidrar til funksjonen for tilbakesporing til for eksempel ordrer, produksjonsordrer eller bestillinger. Funksjonen for tilbakesporing til en ferdig produksjonsordre gir deg muligheten til å gå gjennom den detaljerte historikken.  
- Ferdige produksjonsordrer kan aldri endres.  

## <a name="production-order-execution"></a>Produksjonsordreutførelse  
Når en produksjonsordre er opprettet og planlagt, må den frigis til produksjonen for å bli utført. Under utførelse av ordren, registrerer du:  

- materialer som er plukket eller forbrukt  
- hvor lenge det har vært arbeidet på ordren  
- antall overordnede varer som er produsert  

Denne informasjonen kan registreres manuelt eller via automatisk rapportering i henhold til vareoppsettet i feltet Trekkmetode.  

### <a name="material-consumption"></a>Materialforbruk  
Programmet har mange ulike alternativer for hvordan et produksjonsselskap kan registrere materialforbruk. Materialforbruk kan for eksempel registreres manuelt, noe som kan være aktuelt hvis komponenter erstattes regelmessig eller vrakmengden er større enn forventet.  

Forbruk av materialer kan behandles gjennom forbrukskladden, men det kan også registreres automatisk av programmet, noe som kalles automatisk rapportering. Rapporteringsmetodene er:  

-   Manuell  
-   Fremover  
-   Bakover  

Manuell forbruksrapportering bruker forbrukskladden til å angi materialplukking.  

Forbruksrapportering fremover forutsetter at det forventede antallet av alt materiale for hele ordren forbrukes automatisk ved frigivelsen av en produksjonsordre, med mindre rutekoblingskoder brukes. Når rutekoblingskoder brukes, forbrukes materialet etter at begynnelsen på operasjonstrinnet er registrert i ferdigmeldingskladden. Du må gjøre to ting for å utføre lagertrekk fremover for hele produksjonsordren:  

- Lagertrekk fremover må være valgt på varekortene for alle varer i produksjonsstykklisten på øverste nivå.  
- Alle rutekoblingskoder i produksjonsstykklisten må fjernes.  

Forbruksrapportering bakover rapporterer det faktiske antallet av alt materiale som plukkes eller forbrukes når statusen til en produksjonsordre endres til *Ferdig*, med mindre rutekoblingskoder brukes. Når rutekoblingskoder brukes, forbrukes materialet etter at et antall av den overordnede varen registreres for operasjonstrinnet i ferdigmeldingskladden.  

Når produksjonsordren fornyes, kopieres trekkmetoden fra varekortet. Siden trekkmetoden for hver produksjonsordrekomponent kontrollerer hvordan og når forbruket registreres, er det viktig å være oppmerksom på at du kan endre trekkmetoden for bestemte varer direkte i produksjonsordren.  

#### <a name="automatic-consumption-posting-flushing"></a>Automatisk forbruksbokføring (lagertrekk)  
Fordelen med automatisk lagertrekk er at det i sterk grad reduserer registrering av data. Når du har muligheten til å trekke en operasjon automatisk, kan hele registreringen av forbruk og avgang automatiseres. Ulempen ved å bruke automatisk lagertrekk er at du kanskje ikke nøyaktig registrerer - eller til og med ikke legger merke til - vrak. De automatiske rapporteringsmetodene er:  

- Lagertrekk fremover for hele ordren  
- Lagertrekk fremover etter operasjon  
- Lagertrekk bakover etter operasjon  
- Lagertrekk bakover for hele ordren  

#### <a name="automatic-reporting---forward-flush-the-entire-order"></a>Automatisk rapportering - lagertrekk fremover for hele ordren  
Hvis du utfører lagertrekk fremover for produksjonsordren ved begynnelsen på prosjektet, ligner virkemåten til programmet svært mye på manuelt forbruk. Den store forskjellen er at forbruket skjer automatisk.  

- Hele innholdet i produksjonsstykklisten forbrukes og trekkes fra beholdningen når den frigitte produksjonsordren fornyes.  
- Forbruksantallet er antallet per montering som er angitt i produksjonsstykklisten, ganget med antallet overordnede varer du lager.  
- Du trenger ikke å registrere informasjon i forbrukskladden hvis alle varene skal trekkes.  
- Når varer fra lageret forbrukes, har tidspunktet for registrering av poster i ferdigmeldingskladden ingen betydning siden ferdigmeldingskladden ikke påvirker denne måten å bokføre forbruk på.  
- Ingen rutekoblingskoder kan defineres.  

Lagertrekk fremover for en hel ordre er egnet for produksjonsmiljøer med:  

-   et lavt antall defekter  
-   et lavt antall operasjoner  
-   høyt komponentforbruk i tidlige operasjoner  

#### <a name="automatic-reporting---forward-flushing-by-operation"></a>Automatisk rapportering - lagertrekk fremover etter operasjon  
Lagertrekk etter operasjon gir deg muligheten til å trekke fra beholdningen under en bestemt operasjon i ruten for den overordnede varen. Materiale er knyttet til ruten ved hjelp av rutekoblingskoder, som svarer til rutekoblingskoder som er knyttet til komponenter i produksjonsstykklisten.  

Lagertrekket skjer når operasjonen som har samme rutekoblingskode, startes. Det som menes med startes, er at en aktivitet registreres i ferdigmeldingskladden for operasjonen. Og denne aktiviteten er kanskje bare registreringen av en oppstillingstid.  

Lagertrekksantallet er antallet per montering som er angitt i produksjonsstykklisten, ganget med antallet overordnede varer som skal lages (forventet antall).  

Denne teknikken er best egnet når det er mange operasjoner og enkelte komponenter ikke trengs før sent i monteringssekvensen. Et JIT-oppsett (Just In Time) har kanskje ikke engang varene tilgjengelige når den frigitte produksjonsordren er begynt.  

Materiale kan forbrukes under operasjoner ved hjelp av rutekoblingskoder. Noen komponenter kan kanskje ikke brukes før de siste monteringsoperasjonene finner sted, og må ikke trekkes fra beholdningen før da.  

#### <a name="automatic-reporting---back-flushing-by-operation"></a>Automatisk rapportering - lagertrekk bakover etter operasjon  
Lagertrekk bakover etter operasjon registrerer forbruk etter at operasjonen er bokført i ferdigmeldingskladden.  

Fordelen med denne metoden er at antallet ferdige overordnede deler i operasjonen er kjent.  

Materiale i produksjonsstykklisten er knyttet til ruteposter ved hjelp av rutekoblingskoder. Lagertrekket bakover skjer når en operasjon med en bestemt rutekoblingskode bokføres med et ferdig antall.  

Lagertrekksantallet er antallet per montering som er angitt i produksjonsstykklisten, ganget med antallet overordnede varer som ble bokført som avgangsantall i denne operasjonen. Dette kan være forskjellig fra det forventede antallet.  

#### <a name="automatic-reporting---back-flushing-the-entire-order"></a>Automatisk rapportering - lagertrekk bakover for hele ordren  
Denne rapporteringsmetoden tar ikke hensyn til rutekoblingskoder.  

Ingen komponenter plukkes før statusen til den frigitte produksjonsordren endres til *Ferdig*. Lagertrekksantallet er antallet per montering som er angitt i produksjonsstykklisten, ganget med antallet overordnede varer som ble ferdige og plassert på lager.  

Lagertrekk bakover for hele produksjonsordren krever samme oppsett som for lagertrekk fremover: Rapporteringsmetoden må settes til bakover på hvert varekort for alle varer i den overordnede stykklisten som skal rapporteres. I tillegg må alle rutekoblingskoder fjernes fra produksjonsstykklisten.  

### <a name="production-output"></a>Produksjonsavgang  
Programmet gir deg muligheten til å spore hvor lenge det arbeides på en produksjonsordre, i tillegg til å registrere antallet som produseres. Denne informasjonen kan hjelpe deg med å fastsette produksjonskosten mer nøyaktig. Produsenter som bruker et standardkostsystem, vil kanskje registrere faktisk informasjon for å bidra til utvikling av bedre standarder.  

Avgang kan behandles gjennom ferdigmeldingskladden, men kan også registreres automatisk av programmet. Programmet kopierer trekkmetoden fra produksjonsressurs- eller arbeidssenterkortet til produksjonsordreruten ved fornying. Som med materialforbruk er det tre rapporteringsmetoder for avgang:  

- Manuell  
- Fremover  
- Bakover  

Den manuelle metoden metoden bruker ferdigmeldingskladden til å angi tidsforbruk og produsert antall.  

Fremovermetoden registrerer forventet avgang (og tid), som registreres automatisk ved frigivelsen av en produksjonsordre. Rutekoblingskoder er ikke en faktor i lagertrekk fremover for avgangen.  

Bakover-metoden bokfører den forventede avgangen (og tiden), som registreres automatisk når en produksjonsordre er ferdig. Rutekoblingskoder er ikke en faktor i lagertrekk bakover for avgangen.  

### <a name="posting-consumption-and-output"></a>Bokføre forbruk og avgang  
Du kan bruke en hvilken som helst kombinasjon av automatisk lagertrekk og manuelt registrert informasjon for både forbruk og avgang. Det kan for eksempel være aktuelt å utføre automatisk lagertrekk fremover for komponenter, men fortsatt bruke forbrukskladden til å registrere vrak. Likeledes kan det være aktuelt å registrere avgang automatisk, men bruke ferdigmeldingskladden til å registrere vrak for den overordnede varen eller ekstra tid som er brukt på ordren.  

Hvis du registrerer forbruk og avgang manuelt, må du til slutt avgjøre hvilken rekkefølge du skal registrere denne informasjonen i. Du kan registrere forbruk først og bruke en kortfattet metode til å registrere informasjonen som er basert på forventet avgangsantall. Eller du kan registrere avgang først ved å bruke **Utfold rute**-funksjonen. Du kan da registrere forbruk basert på faktisk avgangsantall.  

### <a name="production-journal"></a>Produksjonskladd  
I produksjonskladden kombineres funksjonene i forbrukskladden og ferdigmeldingskladden i én kladd, som du har direkte tilgang til fra den frigitte produksjonsordren.  

Formålet med produksjonskladden er å gi deg ett enkelt grensesnitt for registrering av forbruk og avgang fra en produksjonsordre.  

Produksjonskladden har en enkel visning og gir deg muligheten til å:  

- enkelt registrere avgang og forbruk som er knyttet til en produksjonsordre  
- knytte komponentene til operasjoner  
- knytte faktiske operasjonsdata til standardoverslagene på rute- og komponentlinjene i produksjonsordren  
- bokføre og skrive ut en oversikt over registrerte operasjonsdata for produksjonsordren  

Produksjonskladden utfører mange av de samme funksjonene som forbruks- og ferdigmeldingskladdene. Dimensjoner, varesporing og hylleinnhold håndteres på samme måte som i forbruks- og ferdigmeldingskladdene.  

Produksjonskladden er imidlertid forskjellig fra forbruks- og avgangskladdene på følgende måter:  

- Den kalles direkte fra en frigitt produksjonsordrelinje og er forhåndsdefinert med de aktuelle dataene.  
- Du kan bruke kladden til å definere hvilke typer komponenter du vil håndtere, basert på et filter for trekkmetode i kladden.  
- Antallet og hvor mange ganger ordren allerede er bokført, vises nederst i kladden som faktiske poster.  
- Felt der dataregistrering ikke er aktuelt, er tomme og kan ikke redigeres.  
- Brukeren kan definere måten avgangsantall skal forhåndsdefineres på i kladden, for eksempel at den siste operasjonen må ha null som avgangsantall.  
- Hvis du skulle gå ut av kladden uten å ha bokført endringene dine, vises en forespørselsmelding som lar deg bli værende i kladden.  
- Den viser operasjoner og komponenter sammen i en logisk struktur som gir en oversikt over produksjonsprosessen.  

I produksjonskladden bokføres forbruksantall som negative vareposter, avgangsantall som positive poster og tidsforbruk som kapasitetsposter.  

## <a name="see-also"></a>Se også
[Produksjon](production-manage-manufacturing.md)    
[Definere produksjon](production-configure-production-processes.md)  
[Planlegging](production-planning.md)      
[Lager](inventory-manage-inventory.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
