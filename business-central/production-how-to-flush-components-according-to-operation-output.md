---
title: Lagertrekke komponenter i henhold til operasjonsavgang
description: Dette emnet beskriver hvordan du tømmer komponenter i henhold til operasjonsavgang og andre trekkmetoder som gjelder.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/22/2021
ms.author: bholtorf
---
# <a name="flush-components-according-to-operation-output"></a>Lagertrekke komponenter i henhold til operasjonsavgang
Du kan definere forskjellige lagerstrategier for å automatisere registrering av forbruk av komponenter. 

Denne funksjonaliteten er nyttig av følgende årsaker:  

- **Lagerverdisetting**

    Verdipostene for avgang og forbruk opprettes parallelt ettersom produksjonsordren går fremover. Uten rutekoblingskoder vil lagerverdien øke etter hvert som avgangen bokføres og deretter reduseres på et senere tidspunkt når verdien for komponentforbruk bokføres sammen med den ferdige produksjonsordren.  
- **Lagertilgjengelighet**

    Med gradvis forbruksbokføring er komponentvarenes tilgjengelighet mer oppdatert, noe som er viktig for å opprettholde den interne balansen mellom behov og forsyning. Uten rutekoblingskoder kan andre behov for komponenten tro at den er tilgjengelig så lenge den venter på en forsinket forbruksbokføring.  
- **Til rett tid**

    Med evnen til å tilpasse produktene til kundens ønsker kan du minimere svinn ved å kontrollere at arbeids- og systemendringer bare forekommer når det er nødvendig.  

- **Reduser dataregistrering**

    Når du har muligheten til å trekke en operasjon automatisk, kan hele registreringen av forbruk og avgang automatiseres. Ulempen ved å bruke automatisk lagertrekk er at du kanskje ikke nøyaktig registrerer - eller til og med ikke legger merke til - vrak.

## <a name="automatic-consumption-posting-flushing-methods"></a>Metoder for automatisk forbruksbokføring (lagertrekk)

- Lagertrekk fremover for hele ordren  
- Lagertrekk fremover etter operasjon  
- Lagertrekk bakover etter operasjon  
- Lagertrekk bakover for hele ordren  

### <a name="automatic-reporting---forward-flush-the-entire-order"></a>Automatisk rapportering - lagertrekk fremover for hele ordren
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

### <a name="automatic-reporting---forward-flushing-by-operation"></a>Automatisk rapportering - lagertrekk fremover etter operasjon
Lagertrekk etter operasjon gir deg muligheten til å trekke fra beholdningen under en bestemt operasjon i ruten for den overordnede varen. Materiale er knyttet til ruten ved hjelp av rutekoblingskoder, som svarer til rutekoblingskoder som er knyttet til komponenter i produksjonsstykklisten.  

Lagertrekket skjer når operasjonen som har samme rutekoblingskode, startes. Det som menes med startes, er at en aktivitet registreres i ferdigmeldingskladden for operasjonen. Og denne aktiviteten er kanskje bare registreringen av en oppstillingstid.  

Lagertrekksantallet er antallet per montering som er angitt i produksjonsstykklisten, ganget med antallet overordnede varer som skal lages (forventet antall).  

Denne teknikken er best egnet når det er mange operasjoner og enkelte komponenter ikke trengs før sent i monteringssekvensen. Et JIT-oppsett (Just In Time) har kanskje ikke engang varene tilgjengelige når den frigitte produksjonsordren er begynt.  

Materiale kan forbrukes under operasjoner ved hjelp av rutekoblingskoder. Noen komponenter kan kanskje ikke brukes før de siste monteringsoperasjonene finner sted, og må ikke trekkes fra beholdningen før da.  

### <a name="automatic-reporting---back-flushing-by-operation"></a>Automatisk rapportering - lagertrekk bakover etter operasjon
Lagertrekk bakover etter operasjon registrerer forbruk etter at operasjonen er bokført i ferdigmeldingskladden.  

Fordelen med denne metoden er at antallet ferdige overordnede deler i operasjonen er kjent.  

Materiale i produksjonsstykklisten er knyttet til ruteposter ved hjelp av rutekoblingskoder. Lagertrekket bakover skjer når en operasjon med en bestemt rutekoblingskode bokføres med et ferdig antall.  

Lagertrekksantallet er antallet per montering som er angitt i produksjonsstykklisten, ganget med antallet overordnede varer som ble bokført som avgangsantall i denne operasjonen. Dette kan være forskjellig fra det forventede antallet.  

### <a name="automatic-reporting---back-flushing-the-entire-order"></a>Automatisk rapportering - lagertrekk bakover for hele ordren
Denne rapporteringsmetoden tar ikke hensyn til rutekoblingskoder.  

Ingen komponenter plukkes før statusen til den frigitte produksjonsordren endres til *Ferdig*. Lagertrekksantallet er antallet per montering som er angitt i produksjonsstykklisten, ganget med antallet overordnede varer som ble ferdige og plassert på lager.  

Lagertrekk bakover for hele produksjonsordren krever samme oppsett som for lagertrekk fremover: Rapporteringsmetoden må settes til bakover på hvert varekort for alle varer i den overordnede stykklisten som skal rapporteres. I tillegg må alle rutekoblingskoder fjernes fra produksjonsstykklisten. 



Hvis en produksjonsordre om å produsere 800 meter for eksempel krever 8 kg av en komponent, bokføres 2 kg automatisk som forbruk når du bokfører 200 meter som avgang. Du kan oppnå det ved å kombinere metoden for lagertrekk bakover og rutekoblingskoder slik at lagertrekksantallet for hver operasjon er proporsjonalt med den faktiske avgangen for den fullførte operasjonen. For varer som er definert med trekkmetoden Bakover, er standard virkemåte å beregne og bokføre komponentforbruk når du endrer statusen for en frigitt produksjonsordre til **Ferdig**. Hvis du også definerer rutekoblingskoder, skjer beregning og bokføring når hver operasjon er fullført, og antallet som faktisk ble forbrukt i operasjonen, bokføres. Hvis du vil ha mer informasjon, kan du se [Opprette ruter](production-how-to-create-routings.md).  

## <a name="to-flush-components-according-to-operation-output"></a>Slik utfører du lagertrekk i henhold til operasjonsavgang:

1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Varer** og velg den relaterte koblingen.  
2.  Velg handlingen **Rediger**.  
3.  I hurtigfanen **Etterfylling** velger du **Bakover** i feltet **Trekkmetode**.  

    > [!NOTE]  
    >  Velg **Plukk + Bakover** hvis komponenten er brukt på en lokasjon som er konfigurert for lagerstyring.  

4.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Ruter**, og velg deretter den relaterte koblingen.  
5.  Definer rutekoblingskoder for hver operasjon som forbruker komponenten. Hvis du vil ha mer informasjon, kan du se [Opprette ruter](production-how-to-create-routings.md).  
    > [!IMPORTANT]  
    > Du må ikke bruke samme rutekobling for forskjellige operasjoner i ruten, fordi den fører til registrering av komponentens forbruk for hver tilknyttede operasjon.  
6.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Produksjonsstykkliste**, og velg deretter den relaterte koblingen.  
7.  Definer rutekoblingskoder fra hver forekomst av komponenten til operasjonen der den er brukt.

Forbruket bokføres automatisk når du registrerer avgang. Hvis du vil ha mer informasjon, kan du se [Bokføre avgang og operasjonstid](production-how-to-post-output-quantity.md)

## <a name="flushing-methods"></a>Trekkmetoder

Tabellen nedenfor beskriver de tilgjengelige alternativene for trekkmetode som du kan angi på ulike kort for **Vare** og kort for **Lagerføringsenhet**.

|Alternativ|Beskrivelse|
|------------|-------------|  
|Manuell|Krever at du angir og bokfører forbruk manuelt i forbrukskladden.|
|Fremover|Bokfører forbruk automatisk i henhold til komponentlinjene i produksjonsordren. <br><br>Som standard foregår bokføring av komponentforbruket når du endrer statusen for en frigitt produksjonsordre til **Frigitt**. Hvis du imidlertid bruker feltet **Rutekobling** på komponentlinjer for produksjonsordrer, skjer bokføringen per operasjon når operasjonen starter. Hvis du vil ha mer informasjon, kan du se [Opprette rutekoblinger](production-how-to-create-routings.md#to-create-routing-links). <br><br> **Merk**<br>For lagertrekk fremover er den operasjonsspesifikke bokføringen som du oppnår med rutekoblingskoder, basert på det forventede antallet som er definert på komponentlinjen. Hvis du vil ha informasjon om operasjonsspesifikk lagertrekk basert på faktisk avgang, kan du se beskrivelsen av **Bakover** i dette emnet.<br><br>Hvis lokasjonen eller ressursene der denne komponenten forbrukes, er definert med en standard hyllestruktur, forbrukes varen fra **Åpen produksjonshyllekode**. Hvis du vil ha mer informasjon, kan du se [Opprette grunnleggende lagre med operasjonsområder](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md). <br><br> **Viktig!** <br>Lagertrekk fremover skjer også når du velger **Oppdater** på en frigitt produksjonsordre som ble opprettet fra grunnen av. Du kan ikke endre hylleinformasjon på disse frigitte produksjonsordrene som er opprettet direkte, fordi produksjonsordrekomponentlinjene genereres når du fornyer ordren, som samtidig trekker komponentene fremover. Hvis du vil endre hylleinformasjon på produksjonsordrekomponentlinjer før lagertrekk fremover skjer, må denne ordren derfor opprettes med statusen *Planlagt* eller *Fast planlagt*.|
|Bakover|Beregner og bokfører forbruk automatisk i henhold til komponentlinjene i produksjonsordren.<br><br> Som standard foregår beregning og bokføring av komponentforbruket når du endrer statusen for en frigitt produksjonsordre til **Ferdig**. Hvis du imidlertid bruker feltet **Rutekoblingskode** på komponentlinjene for produksjonsordrer, skjer beregningen og bokføringen når hver operasjon er ferdig.<br><br> **Merk** <br>Lagertrekk bakover og rutekoblingskoder kan kombineres, slik at lagertrekksantallet per operasjon er proporsjonalt med den faktiske avgangen for denne operasjonen. Hvis du vil ha mer informasjon, kan du se [Lagertrekke komponenter i henhold til operasjonsavgang](#to-flush-components-according-to-operation-output).<br><br> Hvis lokasjonen eller maskinsenteret der denne komponenten forbrukes, er definert med en standard hyllestruktur, forbrukes varen fra **Åpen produksjonshyllekode**.|
|Plukk + fremover|Samme som for lagertrekk fremover, med unntak av at det bare fungerer for lokasjoner som bruker enten avansert lagerkonfigurasjon eller grunnleggende lagerkonfigurasjon med obligatoriske hyller.<br><br> Forbruk beregnes og bokføres fra hyllen som er definert i feltet **Til-Hyllekode for produksjon** på lokasjonen eller produksjonsressursen, etter at komponenten er plukket fra lageret.<br><br> **Merk** <br>Hvis en komponent er definert med Plukk + trekkmetoden Fremover, kan den ikke ha en rutekoblingskode som er definert med trekkmetoden Fremover. Komponenten vil deretter tømmes automatisk når du starter operasjonen, noe som gjør det umulig å be om plukkaktiviteten.|
|Plukk + bakover|Samme som for lagertrekk bakover, med unntak av at det bare fungerer for lokasjoner som bruker enten avansert lagerkonfigurasjon eller grunnleggende lagerkonfigurasjon med obligatoriske hyller.<br><br> Forbruk beregnes og bokføres fra hyllen som er definert i feltet **Til-Hyllekode for produksjon** på lokasjonen eller produksjonsressursen, etter at komponenten er plukket fra lageret.|

## <a name="see-also"></a>Se også

[Opprette produksjonsstykklister](production-how-to-create-production-boms.md)  
[Definere produksjon](production-configure-production-processes.md)  
[Produksjon](production-manage-manufacturing.md)  
[Planlegging](production-planning.md)  
[Lager](inventory-manage-inventory.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
