---
title: Om produksjonsordrer
description: Finn ut mer om produksjonsordrer og hvordan de brukes til å håndtere konverteringen av kjøpt materiale til produserte varer.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '99000813, 99000814, 99000815, 99000816, 99000829, 99000830, 99000831, 99000832, 99000833, 99000838, 99000839, 99000867, 99000868, 99000882, 99000897, 99000898, 99000900, 99000912, 99000913, 99000914, 99000917'
ms.date: 08/09/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="about-production-orders"></a>Om produksjonsordrer

Produksjonsordrer brukes til å håndtere konverteringen av kjøpt materiale til produserte varer. Produksjonsordrer dirigerer arbeid gjennom ulike arbeidssentre eller produksjonsressurser i produksjonen.  

Før de fortsetter med produksjon, utfører de fleste firmaer forsyningsplanlegging, vanligvis én gang i uken, for å beregne hvor mange produksjonsordrer og bestillinger som skal utføres for å dekke ukens salgsbehov. Bestillinger gir komponentene som er nødvendige i henhold til produksjonsstykklisten, for å produsere sluttvarene.

Produksjonsordrer er de sentrale komponentene i produksjonsfunksjonalitet og inneholder følgende informasjon:  

- produkter som er planlagt for produksjon  
- materialer som trengs i den planlagte produksjonen  
- produkter som er produsert  
- materialer som allerede er valgt ut  
- produkter som har blitt produsert tidligere  
- materialer som ble brukt i tidligere produksjonsoperasjoner  

Produksjonsordrer er utgangspunkt for:  

- planlegging av fremtidig produksjon  
- styring av gjeldende produksjon  
- sporing av ferdig produksjon  

## <a name="production-order-creation"></a>Oppretting av produksjonsordrer

Du kan opprette produksjonsordrer manuelt etter hvert som det er behov for dem, på **Produksjonsordre**-siden, eller generere dem fra siden **Salgsordreplanlegging** eller **Ordreplanlegging**. Du kan også opprette flere ordrer på **Planleggingsforslag**-siden.  

Du kan oroduksjonsordrer ved å bruke informasjon fra:  

- Varer  
- Prod.stykklister
- Ruter  
- Produksjonsressurser  
- Arbeidssentre  

## <a name="limitations-on-creating-production-orders"></a>Begrensninger på oppretting av produksjonsordrer

Produksjonsordrer blir automatisk reservert og sporet til kilden når:  

- de opprettes fra [Planleggingsforslag](production-how-to-run-mps-and-mrp.md)  
- de opprettes fra [Ordreplanlegging](production-how-to-create-production-orders-from-sales-orders.md)-siden  
- De opprettes fra [Ordreplanlegging](production-how-to-plan-for-new-demand.md)-siden  
- funksjonen [Planlegg på nytt](production-how-to-replan-refresh-production-orders.md) brukes på produksjonsordrer  

Hvis du vil ha mer informasjon, kan du se [Spore relasjoner mellom behov og forsyning](production-how-track-demand-supply.md).

Produksjonsordrer som opprettes på andre måter, blir ikke automatisk reservert og sporet.

## <a name="production-order-status"></a>Produksjonsordrestatus

Statusen for produksjonsordren styrer hvordan produksjonsordren skal fungere i programmet. Ordrestatysen styrer produksjonsformen og -innholdet. Produksjonsordrene vises på forskjellige sider i henhold til statusen. Du kan ikke endre statusen for en produksjonsordre manuelt. Du må bruke funksjonen **Endre status** i den individuelle produksjonsordren eller på siden **Endre produksjonsordrestatus**.  

### <a name="simulated-production-order"></a>Simulert produksjonsordre

En simulert produksjonsordre er unik, basert på følgende egenskaper:  

- Som navnet antyder, er dette en simulering du kan bruke til tilbud og kostnader. For eksempel når avdelingen for forskning og utvikling ønsker å få et kostnadsoverslag for en foreslått vare. En simulert produksjonsordre fungerer som et eksempel på en produksjonsordre.  
- De påvirker ikke planleggingen av ordrer. Planlegging (MPS og MRP) tar ikke hensyn til og påvirkes ikke av simulerte produksjonsordrer. En simulert produksjonsordre kan heller ikke brukes som en mal siden den forsvinner når du endrer statusen til den.  

### <a name="planned-production-order"></a>Planlagt produksjonsordre

En planlagt produksjonsordre er unik på grunn av følgende egenskaper:  

- Du kan opprette en planlagt produksjonsordre automatisk fra en ordre.  
- Planlagte produksjonsordrer er som frigitte produksjonsordrer og sender inndata til kapasitetsplanlegging ved å vise samlet kapasitetsbehov etter arbeidssenter eller produksjonsressurs.  
- Planlagte produksjonsordrer representerer det beste overslaget av fremtidig belastning for arbeidssenteret eller produksjonsressursbelastning basert på tilgjengelig informasjon. De genereres vanligvis fra planlegging, men de kan også opprettes manuelt. Siden de slettes av etterfølgende planleggingsgenereringer, er ikke manuell oppretting praktisk.  
- Når de genereres i planleggingen, blir resultatet en foreslått "planlagt ordrefrigivelse" som inkluderer antall, frigivelsesdato og forfallsdato. Logikken i planleggingssystemet er basert på etterfyllingssystemet, gjenbestillingsprinsippene og ordremodifikatorene som oppstår i nettobehovsplanleggingen.  
- Hvis du vil vise innvirkningen deres, kan du undersøke belastningen på hvert arbeidssenter eller hver produksjonsressurs i den planlagte produksjonsordrens rute.  

### <a name="firm-planned-production-order"></a>Fast planlagt produksjonsordre

En fast planlagt produksjonsordre er unik på grunn av følgende egenskaper:  

- Du kan opprette en fast planlagt produksjonsordre automatisk fra en ordre.  
- En fast planlagt produksjonsordre fungerer som en plassholder i planleggingstidsplanen for et fremtidig prosjekt som frigis til produksjon.  
- En fast planlagt produksjonsordre kan genereres fra planlegging eller opprettes manuelt eller fra ordrer. De slettes ikke under etterfølgende planlegging.  
- Når de genereres i planleggingen, blir resultatet en foreslått "planlagt ordrefrigivelse" som inkluderer antall, frigivelsesdato og forfallsdato. Logikken i planleggingssystemet er basert på etterfyllingssystemet, gjenbestillingsprinsippene og ordremodifikatorene som oppstår i nettobehovsplanleggingen.  
- Hvis du vil vise innvirkningen deres, kan du undersøke belastningen på hvert arbeidssenter eller hver produksjonsressurs i den fast planlagte produksjonsordrens rute.  

### <a name="released-production-order"></a>Frigitt produksjonsordre

Den frigitte produksjonsordren er unik, basert på følgende egenskaper:  

- Du kan opprette en frigitt produksjonsordre automatisk fra en ordre.  
- Når en produksjonsordre er frigitt, betyr det ikke nødvendigvis at materialer er plukket, eller at prosjektet er fysisk flyttet til den første operasjonen.  
- I et produser-til-ordre-miljø er det ikke uvanlig å opprette en frigitt produksjonsordre like etter posten for ordren.  
- Faktisk materialforbruk og produktavgang kan registreres manuelt i en frigitt produksjonsordre. I tillegg oppstår automatisk lagertrekk for forbruk og produktavgang bare for frigitte produksjonsordrer.  

### <a name="finished-production-order"></a>Ferdig produksjonsordre

En ferdig produksjonsordre er unik, basert på følgende egenskaper:  

- En ferdig produksjonsordre er vanligvis en som er produsert.  
- Det er viktig å gjøre ferdig produksjonsordren for å fullføre kostlivssyklusen til varen som produseres. Når du har fullført en produksjonsordre, kan du justere og avstemme kostnadene.  
- Ferdige produksjonsordrer brukes til statistisk rapportering og bidrar til funksjonen for tilbakesporing til for eksempel ordrer, produksjonsordrer eller bestillinger. Funksjonen for tilbakesporing til en ferdig produksjonsordre gir deg muligheten til å gå gjennom den detaljerte historikken.  
- Ferdige produksjonsordrer kan aldri endres.  

## <a name="production-order-execution"></a>Produksjonsordreutførelse

Når du har opprettet og planlagt en produksjonsordre, må den frigis til produksjonen for å bli utført. Under utførelse av ordren, registrerer du:  

- materialene som ble plukket eller forbrukt  
- hvor lenge det har vært arbeidet på ordren  
- antall overordnede varer som er produsert  

Du kan registrere denne informasjonen manuelt eller gjennom automatisk rapportering. Metoden avhenger av oppsettet i feltet Trekkmetode for varen og arbeidssenteret.  

### <a name="material-consumption"></a>Materialforbruk

[!INCLUDE [prod_short](includes/prod_short.md)] inneholder ulike alternativer for hvordan materialforbruk registreres. Materialforbruk kan for eksempel registreres manuelt, noe som kan være aktuelt hvis komponenter erstattes regelmessig eller vrakmengden er større enn forventet.  

Forbruk av materialer kan behandles gjennom [forbrukskladden](production-how-to-post-consumption.md), men det kan også registreres automatisk av [!INCLUDE [prod_short](includes/prod_short.md)], kjent som automatisk rapportering (trekking). Rapporteringsmetodene Manuell, Fremover og Bakover er tilgjengelige.

Manuell forbruksrapportering bruker forbrukskladden til å angi materialplukking.  

Forbruksrapportering fremover forutsetter at det forventede antallet av alt materiale for hele ordren forbrukes automatisk ved frigivelsen av en produksjonsordre, med mindre rutekoblingskoder brukes. Når du bruker rutekoblingskoder, forbrukes materialet etter at begynnelsen på operasjonstrinnet er registrert i ferdigmeldingskladden. Du må gjøre to ting for å utføre lagertrekk fremover for hele produksjonsordren:  

- Lagertrekk fremover må være valgt på varekortene for alle varer i produksjonsstykklisten på øverste nivå.  
- Alle rutekoblingskoder i produksjonsstykklisten må fjernes.  

Forbruksrapportering bakover rapporterer det faktiske antallet av alt materiale som plukkes eller forbrukes når statusen til en produksjonsordre endres til *Ferdig*, med mindre rutekoblingskoder brukes. Når du bruker rutekoblingskoder, forbrukes materialet etter at et antall av den overordnede varen registreres for operasjonstrinnet i ferdigmeldingskladden.  

Når produksjonsordren fornyes, kopieres trekkmetoden fra varekortet. Siden trekkmetoden for hver produksjonsordrekomponent kontrollerer hvordan og når forbruket registreres, er det viktig å være oppmerksom på at du kan endre trekkmetoden for bestemte varer direkte i produksjonsordren. Hvis du vil ha mer informasjon, kan du se [Lagertrekke komponenter i henhold til operasjonsavgang](production-how-to-flush-components-according-to-operation-output.md).

### <a name="production-output"></a>Produksjonsavgang

[!INCLUDE [prod_short](includes/prod_short.md)] gir deg muligheten til å spore hvor lenge det arbeides på en produksjonsordre, i tillegg til å registrere antallet som produseres. Denne informasjonen kan hjelpe deg med å fastsette produksjonskosten mer nøyaktig. Produsenter som bruker et standardkostsystem, vil kanskje registrere faktisk informasjon for å bidra til utvikling av bedre standarder.  

Avgang kan behandles gjennom [ferdigmeldingskladden](production-how-to-post-output-quantity.md), men kan også registreres automatisk. [!INCLUDE [prod_short](includes/prod_short.md)] kopierer trekkmetoden fra produksjonsressurs- eller arbeidssenterkortet til produksjonsordreruten ved fornying. Som med materialforbruk er de tre rapporteringsmetodene for avgang, Manuell, Fremover og Bakover, tilgjengelige.

Den manuelle metoden metoden bruker ferdigmeldingskladden til å angi tidsforbruk og produsert antall.  

Fremovermetoden registrerer forventet avgang (og tid), som registreres automatisk ved frigivelsen av en produksjonsordre. Rutekoblingskoder er ikke en faktor i lagertrekk fremover for avgangen.  

Bakover-metoden bokfører den forventede avgangen (og tiden), som registreres automatisk når en produksjonsordre er ferdig. Rutekoblingskoder er ikke en faktor i lagertrekk bakover for avgangen.  

### <a name="posting-consumption-and-output"></a>Bokføre forbruk og avgang

Du kan bruke en hvilken som helst kombinasjon av automatisk lagertrekk og manuelt registrert informasjon for både forbruk og avgang. Det kan for eksempel være aktuelt å utføre automatisk lagertrekk fremover for komponenter, men fortsatt bruke en forbrukskladd til å registrere vrak. Likeledes kan det være aktuelt å registrere avgang automatisk, men bruke en ferdigmeldingskladd til å registrere vrak for den overordnede varen eller ekstra tid som er brukt på ordren.  

Hvis du registrerer forbruk og avgang manuelt, må du til slutt avgjøre hvilken rekkefølge du skal registrere denne informasjonen i. Du kan registrere forbruk først og bruke en kortfattet metode til å registrere informasjonen som er basert på forventet avgangsantall. Eller du kan registrere avgang først ved å bruke **Utfold rute**-funksjonen. Du kan da registrere forbruk basert på faktisk avgangsantall.  

### <a name="production-journal"></a>Produksjonskladd

I [produksjonskladden](production-how-to-register-consumption-and-output.md) kombineres funksjonene i forbrukskladden og ferdigmeldingskladden i én kladd, som du har direkte tilgang til fra den frigitte produksjonsordren.  

Formålet med en produksjonskladd er å gi deg ett enkelt grensesnitt for registrering av forbruk og avgang fra en produksjonsordre.  

Produksjonskladder har en enkel visning og gir deg muligheten til å:  

- enkelt registrere avgang og forbruk som er knyttet til en produksjonsordre  
- knytte komponentene til operasjoner  
- knytte faktiske operasjonsdata til standardoverslagene på rute- og komponentlinjene i en produksjonsordre  
- bokføre og skrive ut en oversikt over registrerte operasjonsdata for en produksjonsordre  

Produksjonskladden utfører mange av de samme funksjonene som forbruks- og ferdigmeldingskladdene. Dimensjoner, varesporing og hylleinnhold håndteres på samme måte.  

Produksjonskladder er imidlertid forskjellige fra forbruks- og avgangskladdene på følgende måter:  

- Den kalles direkte fra en frigitt produksjonsordrelinje og er forhåndsdefinert med de aktuelle dataene.  
- Du kan bruke kladden til å definere hvilke typer komponenter du vil håndtere, basert på et filter for trekkmetode i kladden.  
- Antallet og hvor mange ganger ordren allerede er bokført, vises nederst i kladden som faktiske poster.  
- Felter der dataregistrering ikke er aktuelt, er tomme og kan ikke redigeres.  
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
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
