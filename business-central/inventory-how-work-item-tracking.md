---
title: 'Spore varer med serie-, parti- og pakkenumre'
description: 'Du kan legge til serie-, parti- og pakkenumre i ethvert utgående eller inngående dokument, og tilhørende bokførte varesporingsposter vises i de relaterte varepostene.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.forms: '6503, 6515, 6513, 6512, 6502, 6506, 6501, 6510, 6507, 6500, 6505, 6508, 9126, 6526, 6516, 6511, 6504, 6509, 163, 6550,'
ms.date: 03/13/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="track-items-with-serial-lot-and-package-numbers"></a>Spor varer med serie-, parti- og pakkenumre

Du kan tilordne serie-, parti- og pakkenumre i ethvert utgående eller inngående dokument, og tilhørende bokførte varesporingsposter vises i de relaterte varepostene. Du sporer elementer på siden **Varesporingslinjer**, som du kan åpne fra et inngående eller utgående dokumenter.

Antallsfeltene øverst på siden **Varesporingslinjer** gir en oversikt over antallene og summene til varesporingsnumrene som defineres på linjene. Antallene må samsvare med dem som finnes på dokumentlinjene, som er indikert med en 0 i **Udefinert**-feltene.

[!INCLUDE [prod_short](includes/prod_short.md)] oppdaterer tilgjengelighetsinformasjonen på siden **Varesporingslinjer** når du åpner siden. Det oppdaterer ikke informasjonen mens du har siden åpen, selv om det forekommer endringer på lageret eller i andre dokumenter i løpet av denne tiden.

> [!NOTE]  
> For at funksjonene som er beskrevet i denne artikkelen, skal fungere må du definere varesporing. Hvis du vil ha mer informasjon, kan du se [Konfigurer varesporing med serie-, parti- og pakkenumre](inventory-how-setup-item-tracking.md).

## <a name="item-tracking-availability"></a>Varesporingstilgjengelighet

Når du arbeider med serie-, parti- og pakkenumre, beregner [!INCLUDE[prod_short](includes/prod_short.md)] tilgjengelighetsinformasjon og viser den på de ulike varesporingssidene. Dette viser hvor mye av et parti-, pakke- eller serienummer som brukes på andre dokumenter. Denne informasjonen bidrar til å redusere antall feil og usikkerhet forårsaket av doble tildelinger.

På siden **Varesporingslinjer** kan det vises et advarselsikon i **Tilgjengelighet, Partinr** eller **Tilgjengelighet, Serienr.**-feltet av følgende årsaker:

* Hvis noe av eller hele antallet du har valgt, allerede er brukt i andre dokumenter.
* Hvis parti- eller serienummeret ikke er tilgjengelig.

Sidene **Partinr. / Serienr.oversikt**, **Partinr. / Tilgjengelighet for serienummer** og **Varesporing - velg poster** viser antallet av en vare i bruk. Tabellen nedenfor viser de relevante feltene.

|Felt|Description|
|-----|-----------|  
|**Antall i alt**|Totalt antall varer av en vare på lager.|
|**Ønsket antall i alt**|Totalt antall varer som det er ønske om i dette eller andre dokumenter.|
|**Gjeldende antall i kø**|Antallet ønskede varer som forespørres i det gjeldende dokumentet, men ikke er bokført.|
|**Gjeldende ønsket antall**|Antallet ønskede varer som vil bli brukt i det gjeldende dokumentet|
|**Totalt disp. antall**|Totalt antall varer på lager minus antallet av varen som det er ønske om å bruke i dette og andre dokumenter (ønsket antall i alt), og minus antallet som det er ønske om å bruke, men som ennå ikke er bokført i dette dokumentet (gjeldende antall i kø).|

Hvis du arbeider på siden **Varesporingslinjer** i en lang periode, eller hvis det skjer mye med varen du arbeider med, kan du velge handlingen **Oppdater tilgjengelighet**. I tillegg kontrolleres tilgjengeligheten av varen automatisk på nytt når du lukker siden, for å bekrefte at det ikke finnes noen tilgjengelighetsproblemer.

## <a name="to-assign-serial-or-lot-numbers-during-an-inbound-transaction"></a>Slik tilordner du serie- eller partinumre ved en inngående transaksjon

Det kan være lurt å spore varer fra det øyeblikket de ankommer. Da er bestillingen ofte det sentrale dokumentet. Du kan imidlertid håndtere varesporing fra hvilket som helst innkomende dokument og tilhørende bokførte poster vises i de relaterte varepostene.

Sporingsnumrene overføres automatisk til alle utgående lageraktiviteter.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Bestillinger**, og velg deretter den relaterte koblingen.  
2. Åpne en eksisterende bestilling eller opprett en ny bestilling.
3. Velg dokumentlinjen, og på hurtigfanen **Linjer** velger du handlingen **Linje** og deretter **Varesporingslinjer** for å åpne siden **Rediger – Varesporingslinjer**.  

   Du kan tilordne serie- eller partinumre på følgende måter:  
   * Automatisk, ved å velge **Behandle** og deretter **Tilordne serienr.** eller **Tilordne partinr.** for å tilordne serie-/partinumre fra forhåndsdefinerte nummerserier.  
   * Automatisk, ved å velge **Behandle** og deretter **Opprett egendefinert s.nr.** hvis du vil at programmet skal tilordne serie-/partinumre basert på nummerserier som er definert spesielt for de mottatte varene.  
   * Manuelt, ved å angi serie- eller partinumre direkte, for eksempel leverandørens numre.  
   * Manuelt ved å tilordne hver vareenhet et bestemt nummer.  

4. Hvis du vil tilordne automatisk, velger du **Opprett egendefinert s.nr.**  
5. I feltet **Egendef. serienr.** angir du startnummeret på en beskrivende serienummerserie. For eksempel **S/N-Vend0001**.  
6. I feltet **Økning** angir du 1 for å angi at hvert nye nummer skal økes med én.  

    Feltet **Ant. som skal oppr.** inneholder linjeantallet som standard, men du kan endre det.  

7. Merk av for **Opprett nytt partinr.** hvis du vil samle de nye serienumrene i et parti.  
8. Velg **OK**-knappen.  

[!INCLUDE [prod_short](includes/prod_short.md)] oppretter et partinummer med individuelle serienumre i henhold til vareantallet på dokumentlinjen. Tallet innledes med verdien du angav i feltet **Egendef. serienr.** . For eksempel med start fra **S/N-Vend0001**.  

Antallsfeltene i hodet gir en dynamisk oversikt over antallene og summene til varesporingsnumrene som du definerer på siden. Antallene må samsvare med dem som finnes på dokumentlinjene, som er indikert med en **0** i **Udefinert**-feltet.  

Når du bokfører dokumentet, overfører varesporingsoppføringene varepostene.

### <a name="to-handle-serial-and-lot-numbers-when-getting-receipt-lines-from-a-purchase-invoice"></a>Slik håndterer du serie- og partinumre ved henting av mottakslinjer fra en kjøpsfaktura

Når du bruker henter bokførte mottaks- eller leveringslinjer fra relaterte fakturaer eller kreditnotaer, overføres alle varesporingslinjer i lagerdokumentene automatisk. De behandles imidlertid på en spesiell måte.

Funksjonen støtter følgende inngående prosesser:  

* **Hent mottakslinjer** - fra en kjøpsfaktura.  
* **Hent returforsendelseslinjer** - fra en kjøpskreditnota.  

Funksjonen støtter følgende utgående prosesser:  

* **Hent følgeseddellinje** - fra en salgsfaktura eller samlede følgesedler.  
* **Hent returseddellinjer** - fra en salgskreditnota.  

I disse tilfellene overføres varesporingslinjene til fakturaen eller kreditnotaen, men siden **Varesporingslinjer** tillater ikke endringer i serie- eller partinumre. Du kan bare endre antallene.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Kjøpsfakturaer**, og velg deretter den relaterte koblingen.  
2. Åpne en kjøpsfaktura for varene som er kjøp med serie- eller partinumre.  
3. Velg **Hent mottakslinjer** på hurtigfanen **Linjer** fra en kjøpsfakturalinje.  
4. Velg en mottakslinje som har varesporingslinjer, på siden **Hent mottakslinjer**, og klikk deretter **OK**.  

    Kildedokumentet kopieres til kjøpsfakturaen som en ny linje, og varesporingslinjene i dokumentet kopieres til den underliggende siden **Varesporingslinjer**.  

5. Velg den overførte mottakslinjen på kjøpsfakturaen.  
6. På hurtigfanen **Linjer** velger du **Linje** og deretter handlingen **Varesporingslinjer** for å se de overførte varesporingslinjene.  

Du kan ikke endre **Serienr.** og **Partinr.**. Du kan imidlertid slette hele linjer eller endre antallene slik at de samsvarer med endringer på kildelinjen.  

## <a name="to-assign-a-serial-or-lot-number-during-an-outbound-transaction"></a>Slik tilordner du et serie-/partinummer ved en utgående transaksjon

Utgående håndtering av serie-/partinumre er en oppgave som utføres under mange ulike lagerprosesser. Det finnes to måter å legge til serie- og partinumre i utgående transaksjoner:  

- Velg mellom eksisterende serie-/partinumre. Dette er aktuelt når det allerede er tilordnet varesporingsnumre i en inngående transaksjon.
- Tilordne nye serie- eller partinumre for utgående transaksjoner. Dette gjelder når varesporingsnumrene ikke tilordnes varer før de er solgt og klar for levering.

### <a name="to-select-from-existing-serial-or-lot-numbers"></a>Slik velger du mellom eksisterende serie-/partinumre

Når du arbeider med varer som krever varesporing, og du oppretter utgående transaksjoner, må du vanligvis velge parti- eller serienumrene som allerede finnes.

1. Merk linjen du vil velge serie- eller partinumre for, i et utgående dokument.  
2. På hurtigfanen **Linjer** velger du **Linje**-handlingen, deretter **Relatert informasjon**, og deretter velger du **Varesporingslinjer**.  
3. På siden **Varesporingslinjer** har du tre alternativer for å angi parti- eller serienummer:  

   * Velg feltet **Serienr.**, og velg et nummer fra siden **Serienr.oversikt**.
   * Velg feltet **Partinr.**, og velg et nummer på siden **Partinr.oversikt**. Velg deretter feltet **Serienr.**, og velg et nummer fra siden **Serienr.oversikt**.
   * Velg handlingen **Behandle** og deretter **Velg poster**. **Velg poster**-siden inneholder alle parti- og serienumre sammen med tilgjengelighetsinformasjon.

4. I **Valgt antall**-feltet angir du antallet for hvert parti- eller serienummer du vil bruke.
5. Velg **OK**-knappen. Varesporingsinformasjonen overføres til siden **Varesporingslinjer**.  

Antallsfeltene i hodet gir en dynamisk oversikt over antallene og summene til varesporingsnumrene som du definerer på siden. Antallene må samsvare med dem som finnes i dokumentlinjen, som er indikert med en **0** i feltet **Udefinert**.  

Når du bokfører dokumentlinjen, overføres varesporingsinformasjonen til de tilhørende varepostene.

### <a name="to-assign-new-serial-or-lot-numbers"></a>Slik tilordner du nye serie- eller partinumre

Denne prosessen gjelder når varer ikke har serie- eller partinumre mens de er på lager. I stedet tilordner du varesporingsnumrene når varene er solgt og klar for levering. I dette tilfellet tilordner du vanligvis numrene fra en forhåndsdefinert nummerserie.

1. Velg det relevante dokumentet, for eksempel en salgsfaktura eller ordre, og velg **Linjer**-handlingen på hurtigfanen, handlingen **Linjer**, deretter **Relatert informasjon**, og velg deretter handlingen **Varesporingslinjer**.  

    Du kan tilordne varesporingsnumre på følgende måter:  
    * Automatisk fra forhåndsdefinerte nummerserier: Velg **Tilordne serienr.** eller **Tilordne partinr.**  
    * Automatisk, basert på parametere som du har definert spesielt for utgående vare: Velg **Opprett egendefinert s.nr.**  
    * Manuelt, ved å angi serie- eller partinumre uten å bruke en nummerserie.  

2. For denne fremgangsmåten tilordner du et serienummer automatisk ved å velge **Tilordne serienr.**  

    Feltet **Ant. som skal oppr.** inneholder linjeantallet som standard, men du kan endre det.  
3. Velg feltet **Opprett nytt partinr.** hvis du vil samle de nye serienumrene i et parti.  
4. Velg **OK**-knappen for å opprette et partinummer og nye serienumre i henhold til vareantallet på den aktuelle dokumentlinjen.  

Antallsfeltet øverst gir en dynamisk oversikt over antallene og summene til de varesporingsnumrene som du definerer på siden. Antallene må samsvare med dem som finnes i dokumentlinjen, som er indikert med en **0** i feltet **Udefinert**.  

Når dokumentet bokføres, overfører varesporingsoppføringene varepostene.

### <a name="assign-tracking-numbers-on-source-documents"></a>Tilordne sporingsnumre i kildedokumenter

Noen selskaper definerer bestemte serie- eller partinumre i kildedokumentet, for eksempel ordrer. For eksempel, hvis en kunde ber om et bestemt parti. Når du oppretter lagerplukk- eller plukkdokumentet fra et utgående kildedokument der serie- eller partinumre allerede er definert, kan du ikke endre felt på siden **Varesporingslinjer** under lagerplukkingen. Det eneste unntaket er feltet **Ant. som skal håndt**. I så fall angir lagerplukklinjene varesporingsnumrene på individuelle hentings- og plasseringslinjer. Antallet er allerede delt inn i unike serie- eller partinummerkombinasjoner, fordi ordren spesifiserer varesporingsnumrene som skal leveres.

## <a name="to-handle-serial-and-lot-numbers-on-transfer-orders"></a>Slik håndterer du serie- og partinumre på overføringsordrer

Framgangsmåten for håndteringen av serie- og partinumre som overføres mellom ulike lokasjoner, er omtrent den samme som for kjøp og salg av varer.  

Overføringsordrer er unike på den måten at både levering og mottak gjøres fra samme overføringslinje og bruker samme kjøring av siden **Varesporingslinjer**. Varesporingsnumrene som leveres fra en lokasjon, må mottas uendret på den andre lokasjonen.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Overføringsordrer**, og velg deretter den relaterte koblingen.  
2. Åpne overføringsordren du vil behandle. På hurtigfanen **Linjer** velger du **Linje**, velger **Varesporingslinjer** og velger deretter **Levering**.  
3. På siden **Varesporingslinjer** tilordner du eller velger serie-/partinumre som for en hvilken som helst annen utgående varetransaksjon.  

    Når du håndterer serie- og partinumre for overføringsvarer, er varene oftest allerede tilordnet numre. Derfor kan du ofte velge mellom eksisterende serie- eller partinumre.  

4. Bokfør overføringsordren, først levering og deretter mottak, slik at varene overføres med riktige varesporingsposter.  

Under overføringen kan du ikke endre verdiene på siden **Varesporingslinjer**.  

## <a name="to-record-additional-serial-or-lot-number-information"></a>Slik registrerer du tilleggsopplysninger om serie-/partinumre

Hvis du trenger å knytte spesielle opplysninger til et varesporingsnummer, for eksempel av kvalitetshensyn, kan du gjøre dette på kortet med serie- eller partinummeropplysninger.

1. Åpne et dokument som har serie- eller partinumre tilordnet.
2. Åpne siden **Varesporingslinjer** for varen du vil angi informasjon for.
3. Velg **Linje**-handlingen, og velg deretter for eksempel handlingen **Informasjonskort for serienr.**.  
4. Velg plusstegnet **(+)** øverst i listen for å opprette en ny oppføring. **Serienr.**- og **Partinr.**-feltet blir forhåndsutfylt fra varesporingslinjen.
5. Skriv inn litt informasjon i **Beskrivelse**-feltet, for eksempel om tilstanden til varen.  
6. Velg **Relatert**-handlingen, velg handlingen **Serienr.**, og velg deretter handlingen **Merknad** for å opprette en egen kommentarpost.  
7. Velg feltet **Sperret** for å utelate serie- eller partinummeret fra alle transaksjoner.  

<!--If you create serial numbers in bulk by using the **Create Customized SN** or **Assign Serial No.** actions, you can enable **Create SN Information** and an information card will be created for each tracking line.

Alternatively, you can create an information card when you post journals or documents. On the **Item Tracking Code** page, turn on the **Create SN Info. on posting** or **Create SN Info. on posting** toggles. -->

Du kan endre opprettede seriekort eller partiinformasjonskort senere.

## <a name="to-modify-existing-serial-or-lot-number-information"></a>Slik endrer du eksisterende informasjon om serie- eller partinumre

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Varer** og velg den relaterte koblingen.  
2. Velg en vare som har en varesporingskode, og som har informasjon om serie- eller partinumre.
3. Fra **Varekort**-siden velger du **Poster** og deretter **Poster**.
4. Velg feltet **Partinr.** eller **Serienr.** Hvis det finnes informasjon for dette varesporingsnummeret, åpnes siden **Informasjonsoversikt for partinummer** eller **Informasjonsoversikt for serienummer**.  
5. Velg et kort, og velg deretter **Informasjonskort for partinr. eller Informasjonskort for serienr.**  
6. Endre teksten for kort beskrivelse, merknadsposten eller **Sperret**-feltet.  

Du kan ikke endre serie- eller partinumre eller antall. Du må reklassifisere vareposten for å gjøre dette. Hvis du vil lære mer om å reklassifisere, går du til [Reklassifisere parti- eller serienumre](inventory-how-work-item-tracking.md#to-reclassify-serial-or-lot-numbers).

## <a name="to-reclassify-serial-or-lot-numbers"></a>Slik reklassifiserer du serie- eller partinumre

Å reklassifisere varesporing for en vare betyr å endre et parti- eller serienummer til et nytt parti- eller serienummer eller endre utløpsdatoen til en ny utløpsdato. Hvis du bruker partier, kan du også slå sammen flere partier til ett. Bruke vareoverføringskladden til å utføre disse oppgavene.

> [!NOTE]
> [!INCLUDE [prod_short](includes/prod_short.md)] kontrollerer at hver linje har en unik kombinasjon av serie-, parti- eller pakkenumre. Hvis du vil dele opp et parti, en pakke eller et parti og en pakke i flere partier eller pakker, må du bruke flere kladdelinjer.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lagervarereklassif.kladd** og velg den relaterte koblingen.  
2. Fyll ut linjen med de aktuelle opplysningene. Hvis du vil ha mer informasjon, se [Telle lagerbeholdning ved hjelp av dokumenter](inventory-how-count-inventory-with-documents.md) eller [Telle, justere og reklassifisere lagerbeholdning ved hjelp av kladder](inventory-how-count-adjust-reclassify.md).
3. Velg **Varesporingslinjer**.  
4. I feltet **Serienr.** eller **Partinr.** velger du gjeldende serie- eller partinummer.  
5. Hvis du vil angi et nytt varesporingsnummer, angir du det i feltet **Nytt serienr.** eller **Nytt partinr.**. Hvis du vil, kan du slå sammen ett eller flere partier til ett nytt eller eksisterende parti.  

    > [!NOTE]  
    > Når du reklassifiserer utløpsdatoer, blir varer med de tidligste utløpsdatoene for utgående transaksjoner foreslått først. Hvis du vil vite mer, går du til [Plukking etter FEFO](warehouse-picking-by-fefo.md).  

6. Hvis du vil angi en ny utløpsdato for serie- eller partinummeret, angir du det i feltet **Ny utløpsdato**.  

    > [!IMPORTANT]  
    > * Hvis du reklassifiserer et parti til det samme partinummeret, men med en annen utløpsdato, må du reklassifisere hele partiet og bruke én linje i vareoverføringskladden.
    > * Hvis du reklassifiserer flere enn ett parti til et nytt partinummer, som betyr at du slår sammen flere enn ett parti i ett nytt parti, må du angi samme utløpsdato for alle partiene. 
    > * Hvis du reklassifiserer ett eksisterende parti til et annet eksisterende parti med en annen utløpsdato, må du bruke utløpsdatoen fra det andre partiet. 
    > * Hvis du lar feltet **Ny utløpsdato** stå tomt, reklassifiseres parti- eller serienummeret med en tom utløpsdato.  

7. Hvis du har eksisterende informasjon for det gamle serie- eller partinummeret, kan du kopiere den til det nye serie- eller partinummeret.  

    1. På siden **Varesporingslinjer** velger du **Ny informasjon om serienummer** eller **Ny informasjon om partinummer**.  
    2. Hvis du vil kopiere informasjon fra det gamle parti- eller serienummeret, velger du **Kopier informasjon**.  
    3. Velg parti- eller serienummeret som du vil kopiere fra, på siden for informasjonsoversikt, og velg **OK**-knappen.  

8. Hvis du vil endre den eksisterende informasjonen for parti- eller serienummeret, kan du registrere parti- eller serienummerinformasjon.  
9. Bokfør kladden for å knytte de nye varesporingsnumrene eller utløpsdatoene til den tilhørende vareposten

## <a name="scan-barcodes-with-the-business-central-mobile-app"></a>Skanne strekkoder med Business Central-mobilappen

[!INCLUDE [barcode-mobile-app](includes/barcode-mobile-app.md)]

Hvis du vil skanne flere serie-, parti- eller pakkestrekkoder på siden **Varesporingslinjer**, kan du bruke handlingen **Skann flere** . Etter at du har skannet en strekkode, angis verdien i feltet på siden, og neste hurtiginntastingsfelt blir tilgjengelig. Du kan også bruke strekkodeskannerikonet til å fylle ut bestemte felt.

Tabellene nedenfor inneholder en oversikt over sidene som støtter strekkodeskanning for varesporing fra mobilappen [!INCLUDE [prod_short](includes/prod_short.md)].

|Side  |Feltverdier du kan skanne  |
|---------|---------|
|Varesporingslinjer     |* Serienr.<br><br>* Nytt serienr.<br><br>* Partinr.<br><br>* Nytt partinr.<br><br>* Pakkesporingsnr.<br><br>* Nytt pakkenr.|
|Rollesenter for Varesporingslinjer     |* Serienr.<br><br>* Nytt serienr.<br><br>* Partinr.<br><br>* Nytt partinr.<br><br>* Pakkesporingsnr.<br><br>* Nytt pakkenr.|
|Varesporing     |* Serienr.filter<br><br>* Partinr.filter<br><br>* Pakkesporingsnr. Filter |
|Varekladd     |* Serienr.<br><br>* Partinr.<br><br>* Pakkesporingsnr.     |
|Lageraktivitetslinje     |* Serienr.<br><br>* Partinr.<br><br>* Pakkesporingsnr.<br><br>**Merknad**: Følgende sider bruker siden Lageraktivitetslinje:<br><br>* side 5780 "Lager. Velg delskjema"<br><br>* side 7378 "Lager. Velg delskjema"<br><br>* side 5771 "Lager. Plassering Subform"<br><br>* side 7316 "Lagerflytting Subform"<br><br>* side 7376 "Lager. Plassering delskjema"<br><br>* side 7383 "Lager. Flytting subform"        |
|Rollesenter for Lageropptellingskladd     |* Serienr.<br><br>* Partinr.<br><br>* Pakkesporingsnr.         |

## <a name="see-also"></a>Se også

[Konfigurer varesporing med serie-, parti- og pakkenumre](inventory-how-setup-item-tracking.md)  
[Spore varesporede varer](inventory-how-to-trace-item-tracked-items.md)  
[Lager](inventory-manage-inventory.md)  
[Designdetaljer: Varesporing](design-details-item-tracking.md)  
[Designdetaljer: Varesporing og reservasjoner](design-details-item-tracking-and-reservations.md)  
[Reservere varer](inventory-how-to-reserve-items.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
