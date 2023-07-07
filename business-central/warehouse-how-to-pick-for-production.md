---
title: 'Plukk eller flytt varer for produksjon, montering eller jobber i enkle lageroppsett'
description: 'Når lagerlokasjonen krever at du behandler plukk, men ikke leveringer, bruker du siden Lagerplukk til å organisere og registrere komponentene som ble plukket.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 12/16/2022
ms.custom: bap-template
ms.search.forms: '9330, 931, 990008, 89, 900, 902'
---
# <a name="pick-for-production-assembly-or-jobs-in-basic-warehouse-configurations"></a>Plukke for produksjon, montering eller jobber i enkle lageroppsett

Hvordan du plukker komponenter for produksjon, jobber eller monteringsordrer avhenger av hvordan lageret er definert som lokasjon. Finn ut mer under [Definer lagerstyring](warehouse-setup-warehouse.md).

I et enkelt lageroppsett for utgående flyt (plukk) slår du på **Plukk nødv.**, men slår av **Levering nødv.** på siden **Lokasjonskort** for lokasjonen.

Bruk følgende dokumenter for interne operasjoner:

* Lagerplukk
* Lagerflytting

## <a name="inventory-picks"></a>Lagerplukk

* Når du registrerer en lagerplukking for en intern operasjon, for eksempel produksjon eller et prosjekt, bokføres forbruket av de plukkede komponentene samtidig.
* Vekslebryteren **Hylle obligatorisk** på siden **Lokasjonskort** er valgfri.
* Når du bruker lagerplukk, definerer feltet **Hyllekode** på en produksjonsordrekomponentlinje eller prosjektplanleggingslinjer *Hent*-hyllen. Komponenter reduseres i Hent-hyllen når du bokfører forbruk.

## <a name="inventory-movements"></a>Lagerflyttinger

* Lagerflyttinger krever at du aktivere **Hylle obligatorisk** på siden **Lokasjonskort** for lokasjonen.
* Lagerflyttinger fungerer bare med produksjonsordrekomponentlinjer og monteringsordrelinjer.
* Når du registrerer en lagerflytting for en intern operasjon, registrerer du bare den fysiske flyttingen av komponentene til en hylle i operasjonsområdet. Du bokfører ikke forbruk.
* Når du bruker lagerflyttinger, definerer feltet **Hyllekode** på en produksjonsordrekomponentlinjer *Plasser*-hyllen i operasjonsområdet. Plasser-hyllen er der lageransatte må plassere komponentene.
* Registrer forbruket av de plukkede komponentene separat ved å bokføre en forbrukskladd eller en monteringsordre.

>[!NOTE]
> Selv om vekselbryteren **Plukk nødv.** er deaktivert, kan du bruke et **lagerplukkdokument**. Lagerplukkdokumenter ligner på **lagerplukkdokumenter**. Dette er nyttig hvis du vil bruke plukking i operasjoner og levere i utgående lagerflyter.

### <a name="production"></a>Produksjon

Bruk **lagerplukkdokumenter** for plukking av produksjonskomponenter i flyten til produksjon.

For en lokasjon som bruker hyller, kan du forlenge flyten til produksjon ved å bruke **lagerflyttingsdokumenter**. Lagerflytteringer er spesielt nyttige for komponenttrekk. Hvis du vil ha mer informasjon om hvordan komponentforbruk er trekkes fra hyller til produksjon eller åpne produksjonshyller, kan du gå til [Trekk produksjonskomponenter i et enkelt lageroppsett](#flushing-production-components-in-a-basic-warehouse-configuration).

### <a name="assembly"></a>Montering

Bruk **lagerflyttingsdokumenter** til å flytte monteringskomponenter til monteringsområdet.

> [!NOTE]
> **Lagerflyttingsdokument** krever hyller.

[!INCLUDE [prod_short](includes/prod_short.md)] støtter monter-til-lager- og monter-til-ordre-typer for monteringsflyter. Hvis du vil lære mer om monter-til-ordre i utgående lagerflyt, kan du gå til [Håndtering av monter-til-ordre-varer med lagerplukk](warehouse-how-to-pick-items-with-inventory-picks.md#handling-assemble-to-order-items-with-inventory-picks).

### <a name="project-management"></a>Prosjektstyring

Bruk **lagerplukkdokumenter** til å plukke jobbkomponenter i flyten til prosjektstyring.

For lokasjoner som bruker hyller, kan du forlenge flyten til prosjekter med **lagerflyttingsdokumenter**.

> [!NOTE]
> Muligheten til å plukke komponenter for prosjektplanleggingslinjer ble lagt til [!INCLUDE[d365fin](includes/d365fin_md.md)] i lanseringsbølge 2 i 2022. Hvis du starter å bruke funksjonen, må en administrator aktivere **Funksjonsoppdatering: Aktiver lager og lagerplugg fra prosjekter** på **Funksjonsstyring**-siden.
>
> [!INCLUDE[prod_short](includes/prod_short.md)] bruker verdien i **Restantall**-feltet på prosjektplanleggingslinjen når det opprettes lagerplukk. Hvis du vil bruke lagerplukk for prosjekter, må du aktivere **Bruk forbrukskobling** på siden **Jobbkort** for prosjektet. Dette gjør at du kan spore forbruk mot planen din. Hvis du ikke aktiverer/deaktiverer, vil restantallet være **0** og lagerplukkingen opprettes ikke. Finn ut mer under [Slik definerer du sporing av prosjektbruk](projects-how-setup-jobs.md?tabs=current-experience#to-set-up-job-usage-tracking).

## <a name="pick-or-move-for-production-assembly-and-jobs-in-a-basic-warehouse-configuration"></a>Plukk eller flytt for produksjon, montering eller prosjekter i et enkelt lageroppsett

Du kan opprette lagerplukk eller lagerflytting på tre måter:  

* Fra selve kildedokumentet.  
* For flere kildedokumenter samtidig ved å bruke en satsvis jobb.  
* I to trinn. Frigi kildedokumentet for å gjøre kildedokumentet klart for plukking. Opprett lagerplukk eller -flytting fra dokumeneter for **lagerplukk** eller **lagerflytting**. Lagerplukk eller -flytting er basert på kildedokumentet.  

### <a name="to-create-an-inventory-pick-from-the-source-document"></a>Slik oppretter du et lagerplukk fra kildedokumentet

1. I kildedokumentet, som kan være en produksjonsordre eller et prosjekt, må du velge **Opprett lagerplassering/-plukking**-handling.  
2. Merk av for **Opprett lagerplukking**.
3. Velg **OK**-knappen.

### <a name="to-create-an-inventory-movement-from-the-source-document"></a>Slik oppretter du en lagerflytting fra kildedokumentet

1. I kildedokumentet, som kan være en produksjonsordre, monteringsordre eller et prosjekt, må du velge **Opprett lagerplassering/-plukking**-handling.  
2. Merk av for **Opprett lagerflytting**.
3. Velg **OK**-knappen.

### <a name="to-create-multiple-inventory-picks-or-movements-with-a-batch-job"></a>Slik oppretter du flere lagerplukk eller -flyttinger med en kjørsel

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Opprett plassering/plukk/flytting for lager**, og velg deretter den relaterte koblingen.  
2. På hurtigfanen **Lagerforespørsel** bruker du filtrene **Kildedokumentet** og **Kildenr.** for å filtrere etter dokumenttyper eller dokumentnummerintervaller. Du kan for eksempel bare opprette plukk for produksjonsordrer.
3. På hurtigfanen **Alternativer** slår du vekslebryterne **Opprett lagerplassering** eller **Opprett lagerflytting**.
4. Velg **OK**-knappen.

### <a name="to-create-inventory-picks-or-movements-in-two-steps"></a>Slik oppretter du lagerplukk eller -flyttinger i to trinn

Når du skal plukke eller flytte komponenter for kildedokumenter i to trinn, må du frigi kildedokumentet for å gjøre det klart for plukking. Frigi kildedokumenter for interne operasjoner på følgende måter.  

|Kildedokument|Frigivelsesmetode|  
|---------------------|--------------------|  
|Produksjonsordre|På siden **Planlagt produksjonsordre** endrer du statusen til en ordre til **Frigitt**, eller bruker siden **Frigitt produksjonsordre** til å opprette en frigitt produksjonsordre.|  
|Monteringsordre|Endre statusen for en monteringsordre til **Frigitt**.|
|Prosjekter | Endre et prosjekts status til **Åpen** eller opprett jobb med statusen Åpen med en gang.|  

En lageransatt som er tildelt til plukkende varer, kan opprette et lagerplasseringsdokument for kildedokumentet.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lagerplukk** eller **Lagerflytting**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**.  
3. Velg hvilken type kildedokument plasseringen er for, i **Kildedokument**-feltet.

    > [!NOTE]
    > Du kan ikke bruke **lagerplukkdokumenter** til å plukke monteringskomponenter.
4. Velg kildedokumentet i **Kildenr.**-feltet.  
5. Du kan også velge handlingen **Hent kildedokument** for å velge dokumentet fra en liste over inngående kildedokumenter som er klare for plukking på lokasjonen.  
6. Velg **OK**-knappen for å fylle ut plukk- eller flyttelinjene i henhold til det valgte kildedokumentet.  

## <a name="to-record-the-inventory-pick"></a>Slik registrerer du lagerplukk

1. Åpne dokumentet du vil registrere et plukk for, på siden **Lagerplukk**.  
2. I **Hyllekode**-feltet på plukklinjene må hyllen der varene skal plukkes fra, være hyllen der varen er tilgjengelig. Du kan endre hyllen ved behov.
3. Utfør plukkingen, og angi deretter faktisk antall plukket, i feltet **Ant. som skal håndt.**.

    Hvis du må plukke varene for en linje fra mer enn én hylle, for eksempel fordi en hylle ikke inneholder hele antallet, bruker du handlingen **Del linje** i hurtigfanen **Linjer**. Handlingen oppretter en linje der restantallet skal håndteres.  
4. Velg handlingen **Bokfør**.  

Følgende skjer under bokføringsprosessen:

* Bokfør forbruket av kildedokumentlinjene som ble plukket.
* Hvis lokasjonen bruker hyller, oppretter bokføringen også lagerposter for bokføring av endringene i hylleantallet.

[!INCLUDE [preview-posting-warehouse](includes/preview-posting-warehouse.md)]

## <a name="to-record-the-inventory-movement"></a>Slik registrerer du lagerflyttingen

1. Åpne dokumentet du vil registrere en flytting for, på siden **Lagerflytting**.  
2. I **Hyllekode**-feltet på flyttelinjene foreslås hyllen det skal plukkes fra, basert på varens standardhylle og tilgjengelighet. Du kan endre hyllen ved behov.  
3. Utfør flyttingen, og angi deretter faktisk antall flyttet, i feltet **Ant. som skal håndt.**. Verdiene på Hent- og Plasser-linjene må være like. Eller kan du ikke registrere flyttingen.

    Hvis du må ta varene for en linje fra mer enn én hylle, for eksempel fordi en hylle ikke inneholder hele antallet, bruker du handlingen **Del linje** i hurtigfanen **Linjer**. Handlingen oppretter en linje der restantallet skal håndteres.  
4. Velg handlingen **Registrer lagerflytting**.  

Følgende skjer under bokføringsprosessen:

* Lagerposter indikerer nå at komponentene er i hyllene som er angitt på kildedokumentordrelinjer. For eksempel monteringsordre, produksjonskomponent eller prosjektplanleggingslinje.

>[!NOTE]
> I motsetning til når du flytter komponenter lagerplukkinger, bokføres ikke forbruk når du registrerer en lagerflytting. Du registrerer forbruk som et separat trinn ved å bokføre kildedokumentet.

## <a name="flushing-production-components-in-a-basic-warehouse-configuration"></a>Trekk produksjonskomponenter i et grunnleggende lageroppsett

Trekkmetodene påvirker flyten av komponenter i produksjon. Finn ut mer under [Lagertrekk komponenter i henhold til operasjonsavgang](production-how-to-flush-components-according-to-operation-output.md). Avhengig av trekkmetoden du valgte, kan du plukke komponenter for produksjon på følgende måter:

* Bruk et **lagerplukkdokument** til å registrere plukkingen for varer som bruker **manuell**  trekkmetode. Når du registrerer et lagerplukk, bokføres forbruket for de plukkede komponentene. 
* Bruk et **lagerflyttingsdokument** med en referanse til et kildedokument til å registrere plukk for komponenter som bruker trekkmetoden **Manuell**. Du må registrere forbruk separat. Finn ut mer under [Massebokføre produksjonsforbruk](production-how-to-post-consumption.md). 
* Bruk et **lagerflyttingsdokument** med en referanse til et kildedokument til å registrere plukk for komponenter som bruker trekkmetoden **Plukk + fremover**, **Plukk + bakover**. Forbruk av komponentene utføres automatisk enten når du endrer statusen for produksjonsordren, eller ved å starte eller avslutte en operasjon. Alle obligatoriske komponenter må være tilgjengelig. Ellers stoppes bokføring av trukket forbruk for komponenten.
* Bruk et **lagerflyttingsdokument** uten referanse til et kildedokument eller andre måter å registrere flytting av komponenter som bruker trekkmetoden **Fremover** eller **Bakover**. Forbruk av komponentene utføres automatisk enten når du endrer statusen for produksjonsordren, eller ved å starte eller avslutte en operasjon. Alle obligatoriske komponenter må være tilgjengelig. Ellers stoppes bokføring av trukket forbruk for komponenten. Finn ut mer under [Flytt varer internt i grunnleggende lageroppsett](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).

### <a name="example"></a>Eksempel

Du har en produksjonsordre for 15 STK av varen SP-SCM1004. Noen av varene i komponentoversikten må trekkes manuelt i en forbrukskladd, og andre varer kan plukkes og trekkes automatisk ved hjelp av trekkmetoden **Plukk + Bakover**.  

Fremgangsmåten nedenfor gir et eksempel på handlingene ulike personer gjør og relaterte svar:  

1. Verkstedlederen frigir produksjonsordren. Varer med trekkmetoden **Fremover** og ingen rutekobling, trekkes fra den åpne produksjonshylle.  
2. Butikklederen velger handlingen **Opprett lager plassering/-plukking** på produksjonsordren og aktiverer deretter vekslebryterne **Opprett lagerplukk** og **Opprett lagerflytting**. Et lagerplukkdokument opprettes for varer med trekkmetoden **Manuell**, og det opprettes en lagerflytting for varer med trekkmetodene **Plukk + bakover** og **Plukk + trekk**.
3. Lagerlederen tildeler plukkingene og flyttinger til en lagermedansatt.
4. Den lageransatte plukker varene fra aktuelle hyller og plasserer dem i hyllen til produksjon eller i hyllen som er angitt i lagerflyttingen. Hyllen kan være en hylle for arbeidssenter eller produksjonsressurs.  
5. Den lageransatte bokfører plukkingen. Antallet trekkes fra hyllene.
6. Den lageransatte bokfører flyttingen. Antallet trekkes fra plukkhyllene og legges til forbrukshyllen. **Plukket ant.**-feltet oppdateres i komponentoversikten for alle plukkede varer.  
7. Maskinoperatøren gir produksjonssjefen beskjed om at sluttvarene er ferdige.  
8. Butikklederen bruker ferdigmeldingskladden eller produksjonskladden til å bokføre avgangen. Antallet komponentvarer som bruker trekkmetoden **Plukk + fremover** eller **Plukk + bakover** med rutekoblinger, trekkes fra til hyllen til produksjon.
9. Produksjonssjefen endrer statusen for produksjonsordren til **Ferdig**. Antallet komponentvarer som bruker trekkmetoden **Bakover**, trekkes fra den åpne produksjonshyllen, og antallet komponentvarer som bruker trekkmetoden **Plukk + Bakover**, og ingen rutekobling trekkes fra hyllen til produksjon.  

 Illustrasjonen nedenfor viser når **Hyllekode**-feltet i komponentoversikten fylles i henhold til lokasjonsoppsettet eller oppsettet for produksjonsressurs/arbeidssenter.  

:::image type="content" source="media/binflow.png" alt-text="Oversikt over når og hvordan Hyllekode-feltet fylles ut.":::

## <a name="see-related-microsoft-training"></a>Se relatert [Microsoft-opplæring](/training/paths/pick-ship-items-business-central/)

## <a name="see-also"></a>Se også

[Lager](inventory-manage-inventory.md)  
[Definer lagerstyring](warehouse-setup-warehouse.md)  
[Monteringsstyring](assembly-assemble-items.md)  
[Oversikt over lagerstyring](design-details-warehouse-management.md)
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
