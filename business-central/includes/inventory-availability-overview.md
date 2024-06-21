---
author: brentholtorf
ms.topic: include
ms.date: 04/23/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

Øk effektiviteten på lageret med nøyaktig sanntidsinformasjon om faktorer som kan påvirke tilgjengelige antall. Eksempel: 

* Lagernivåer
* Lokasjoner
* Behandle faser
* Varer i karantene
* Reservasjoner

Du kan få tilgang til informasjon om varetilgjengelighet fra følgende kildedokumenter:

* Ordrer
* Produksjonsordrer
* Monteringsordrer
* Prosjekter

Informasjonen respekterer også andre faktorer som påvirker tilgjengeligheten. Det kan for eksempel være dedikerte hyller, låste hyller og varer som ikke er tilgjengelige for plukking. Varer kan for eksempel være reservert, eller i påvente av plasserings- eller leveringsoperasjoner. På siden **Plukksammendrag** kan du se gjennom varene som [!INCLUDE [prod_short](prod_short.md)] ikke var med i plukkdokumentene, og utføre de nødvendige handlingene.

> [!NOTE]
> Denne funksjonen krever at du aktiverer veksleknappen for **lagerstyring og plukk** for lokasjonene du bruker i plukkprosessen.

### Definere forhåndsvisninger

Hvis du vil ha detaljer om hva som plukkes og hva som ikke plukkes, aktiverer du veksleknappen **Vis sammendrag (lagerstyring)** på forespørselssidene **Lagerkilde - opprett dokument** eller **Lagerlevering - opprett plukk**.

### Bestem antallet du kan plukke

På linjer på siden **Opprett lagerplukksammendrag** viser feltet **Ant. som skal håndt. (l.enh)**  hvilke og hvor mange varer [!INCLUDE [prod_short](prod_short.md)] som prøvde å plukke. Faktaboksen **Sammendrag** inneholder flere detaljer.

For enkle undersøkelser kan **Plukkbart antall** gi deg nok informasjon. Feltet viser hvor mange varer som er tilgjengelige. Hvis antallet som kan plukkes, er mindre enn forventet, utforsker du hylleinnholdet.

Det **Plukkbart antall** er det maksimale antallet som [!INCLUDE [prod_short](prod_short.md)] kan vurdere for plukking. Dette antallet består av varer i hyller som kan plukkes. Antallet ekskluderer antall som er i blokkerte eller dedikerte hyller, eller varer som blir plukket i lagerplukkdokumenter. Hvis varen du vil plukke, krever varesporing, utelates sperrede parti- eller serienumre som er lagret i hyller som kan plukkes, fra antallet som kan plukkes.

Hvis antallet som kan plukkes, er forskjellig fra antallet i hyller som kan plukkes, kan det være et problem. Utforsk hylleinnholdet for å finne blokkerte hyller eller antall i aktive dokumenter.

Feltet **Antall på lager** viser det totale antallet du finner på lageret hvis du foretar en fysisk opptelling. Du kan drille ned til lagerpostene fra dette feltet. Hvis feltet viser et antall som er mindre enn antallet i feltet Antall i **Plukkbare hyller**, er det en feiljustering mellom antall lager og lager. I så fall bruker du handlingen **Beregn lagerjustering** på **Varekladd**-siden, og deretter oppretter du lagerplukkingen på nytt.

Bildet nedenfor illustrerer det maksimale antallet som vurderes for plukking.

:::image type="content" source="../media/pickable-qty.png" alt-text="Maksimalt antall vurdert for plukking.":::

**Forklaring**

|Bokstav  |Description  |
|---------|---------|
|P     |Hyller med innhold av typen Plukk         |
|D     |Hyller med innhold av typen Plukk merket som Dedikerte hyller        |
|A     |Hyller med innhold av typen Plukk i de aktive dokumentene (som en annen plukking)       |
|T     |Hyller med innhold av typen Plukk med varer med sperret sporing         |
|B     |Hyller med innhold av typen Plukk med sperret utgående flytting         |
|O     |Andre hyller         |

### Reservasjoner

Hvis det er reservasjoner for varen som plukkes, fortsetter beregningen. Tanken er at reservert behov har høyere prioritet enn ikke-reservert, noe som betyr at plukking for ikke-reservert behov ikke skal hindre plukking for reservert behov senere.

Hvis du vil kontrollere at antallet kan dekke et behov, sammenligner du verdien for **Plukkbart antall** i faktaboksen **Sammendrag** med verdien i feltet **Ant. som skal håndt. (l.enh)** på linjene.

Du finner reservasjoner i feltet **Totalt reservert antall i lager**. Reserverte antall som allerede er plukket og er klare for levering, bruk eller forbruk, påvirker ikke tilgjengeligheten. Feltet **Reservert antall i plukk/leveringshylle** viser dette antallet.

Feltet **Disp. antall ekskl. leveringshylle** viser antallet som er tilgjengelig, ekskludert antall der følgende er tilfelle:

* De er allerede plukket for forsendelser.
* De er i blokkerte varepartier eller serienumre.
* De er i blokkerte søppelkasser.
* De er i dedikerte hyller.

Disse antallene kan være tilgjengelige, men du kan kanskje ikke plukke dem ennå. De kan fortsatt være i mottaks-, lagrings- eller kvalitetssikringsområdene. Du kan flytte dem til plukkområdet ved å behandle et plasserings- eller flytteforslag.

Differansen mellom **Disp. antall ekskl. leveringshylle** og reservert antall på lager er antallet som er tilgjengelig for plukking uten at det påvirker reservert lagerbeholdning.

Følgende bildet illustrerer tildeling av tilgjengelig antall for reservert antall.

:::image type="content" source="../media/Warehouse_Reservation_Pick.png" alt-text="Maksimalt antall som vurderes for plukking når reservasjon er involvert.":::

**Forklaring**

|Bokstav  |Description  |
|---------|---------|
|P     |Antall som skal plukkes         |
|TR    |Totalt reservert antall på lager.         |
|RS    |Reserverte antall som allerede er plukket og er klare for levering, bruk eller forbruk       |
|A     |Disp. antall ekskl. leveringshylle         |
|B     |Antall i dedikerte eller blokkerte hyller, blokkerte varepartier eller serienumre         |

Selv om det er nok tilgjengelig antall på lageret til å oppfylle plukkingen fullstendig, fører det til at det totale reserverte antallet fordeles mot antallene i dedikerte eller blokkerte hyller, noe som forhindrer plukking for dette behovet. Fordi reservert behov har høyere prioritet, reduserer [!INCLUDE [prod_short](prod_short.md)] antallet som skal plukkes, for å hindre negativ innvirkning, for eksempel manglende evne til å plukke, på reservert behov.

### Annen informasjon

Hvis varer krever varesporing, kan du også finne antallet i blokkerte partier eller serienumre, noe som fører til følgende reduksjoner:

* Det plukkbare antallet
* Tilgjengelig antall, eksklusiv forsendelseshylle
* Det reserverte antallet på lager 

Hvis du plukker samme vare for flere kildedokumenter eller linjer, noe som også er tilfelle når du velger serienumre, vises også informasjon om plukking for andre linjer, fordi det reduserer det plukkbare antallet.
