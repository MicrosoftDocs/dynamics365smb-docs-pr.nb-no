---
title: Plassere varer med lagerplasseringer
description: Finn ut mer om de ulike måtene å bruke lagerplasseringer for å plassere mottatte varer.
author: bholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 01/24/2023
ms.custom: bap-template
ms.search.forms: '7352, 7333'
---
# <a name="put-items-away-with-warehouse-put-aways"></a>Plassere varer med lagerplasseringer

I [!INCLUDE[prod_short](includes/prod_short.md)] mottar du varer og plasserer dem ved å bruke en av fire metoder, som beskrevet i tabellen nedenfor.

|Prinsipp|Inngående prosess|Krev kvitteringer|Krev plasseringer|Kompleksitetsnivå (Finn ut mer under [Oversikt over Warehouse Management](design-details-warehouse-management.md))|  
|------------|---------------------|--------------|----------------|------------|  
|A|Bokføre mottak og plassering fra ordrelinjen|||Ingen dedikert lageraktivitet.|  
|B|Bokføre mottak og plassering fra et lagerplasseringsdokument||Slått på|Grunnleggende: ordre for ordre.|  
|U|Bokføre mottak og plassering fra et lagermottaksdokument|Slått på||Grunnleggende: konsolidert mottak/levering for flere ordrer.|  
|D|Bokføre mottak fra et lagermottaksdokument og bokføre plassering fra et lagerplasseringsdokument|Slått på|Slått på|Avansert|  

Finn ut mer under [Inngående lagerflyt](design-details-inbound-warehouse-flow.md).

Denne artikkelen henviser til metode D i tabellen og antar at mottaket allerede har skjedd. Finn ut mer under [Motta varer](warehouse-how-receive-items.md).

Når en lokasjon er definert til å bruke plasseringsbehandling og lagermottaksbehandling, må du bruke plasseringsdokumenter til å styre hvordan varer plasseres. Når du bokfører et lagermottak, oppdateres kildedokumenter som kjøp, inngående overføring eller ordrereturer. Det mottatte antallet posteres til vareposten, og linjene for de mottatte varene sendes til plasseringsfunksjonen i lageret.

Avhengig av verdien i feltet **Bruk plasseringsforslag** på siden **Lokasjonskort**, gjøres linjene tilgjengelig for plasseringsforslaget eller brukes til å generere plasseringsdokumenter umiddelbart. Finn ut mer under [Definer lagerstyring](warehouse-setup-warehouse.md).  

I tillegg til standardmåter å opprette plasseringer på, som er beskrevet i denne artikkelen, kan du opprette plasseringer fra det relaterte bokførte lagermottaket. Dette er nyttig hvis du har slettet plasseringslinjer, eller hvis du bestemmer deg for ikke å bruke plasseringsforslaget, fordi du kan opprette eller gjenopprette plasseringsinstruksjoner fra de bokførte mottakslinjene.

## <a name="zone-and-bin-codes"></a>Sone- og hyllekoder

På lokasjoner som er definert for å bruke lagerstyring, er følgende innstillinger nødvendige for å fastslå det beste stedet å plassere varene:  

* En plasseringsmal konfigureres. Finn ut mer under [Definer plasseringsmaler](warehouse-how-to-set-up-put-away-templates.md).  
* Vekten, kubikkinnholdet og spesielle lagringskrav for varen eller lagerføringsenheten er definert.
* Kapasiteten, hylletypen og hylleprioritering er definert for hyllene.  

Hylleprioriteringen brukes når flere enn én hylle samsvarer med kriteriene på plasseringsmalen. Hvis både plasseringsmalkriteriene og hylleprioriteringen er den samme for flere hyller, velges hyllen med det høyeste nummeret.

## <a name="to-create-put-away-documents-in-bulk-with-the-put-away-worksheet"></a>Slik oppretter du plasseringsdokumenter i bulk med plasseringsforslaget

Du kan opprette plasseringsdokumenter for flere mottak samtidig på siden **Plasseringsforslag**.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Plasseringsforslag** og velg den relaterte koblingen.  
2. Velg handlingen **Hent lagerdokumenter**. **Plasseringsutvalg**-siden åpnes.  

    Oversikten inneholder alle bokførte mottak som er klare til å plasseres, inkludert de som det allerede er opprettet plasseringsinstruksjoner for. Dokumenter med plasseringslinjer som er fullstendig plassert og registrert, blir ikke vist i denne oversikten.  
3. Velg dokumentene du vil arbeide med. Du kan arbeide med linjer fra flere dokumenter samtidig.  

    > [!NOTE]  
    >  Hvis du velger et mottaksdokument eller internplasseringsdokument der du allerede har opprettet instruksjoner for alle linjene, informerer [!INCLUDE[prod_short](includes/prod_short.md)]] deg om at det ikke er noe å håndtere.  

4. Fyll ut feltet **Sorteringsmetode** for å sortere linjene.  

    > [!NOTE]  
    >  Måten linjene blir sortert på i forslaget, overføres ikke automatisk ved plasseringsinstruksen. Det finnes imidlertid de samme mulighetene for sortering og hylleprioritering. Du kan opprette linjeordren på nytt du planlegger i forslaget, når du oppretter plasseringsinstruksjonene eller sorterer i plasseringsinstruksjonene.

5. Fyll ut feltet **Ant. som skal håndt.**. Velg handlingen **Autoutfyll ant. som skal hndt.**, eller fyll ut feltene manuelt.  
6. Du kan redigere linjene manuelt om nødvendig. Du kan slette linjer, for eksempel hvis noen varer må plasseres i en hylle som er langt borte fra hyllene for de andre varene.  

    > [!NOTE]  
    > Når du sletter linjer, slettes de bare fra dette forslaget. De slettes ikke fra plasseringsvalget.  

7. Velg handlingen **Opprett plassering**. Siden **Opprett dokument** åpnes. Her kan du tilføye mer informasjon for den plasseringen du oppretter.  

    * Du kan tilordne plasseringen til en bestemt ansatt.  
    * Du kan sortere plasseringsinstruksjonslinjene på samme måte som i forslaget eller etter hylleprioritering. Når du sorterer etter hylleprioriteringen, vises *Hent*-linjene først, fordi de fleste mottakshyllene har en rangering på 0 hyller. *Plasser*-linjene vises sist og begynner med de hyllene som har lavest hylleprioritering. Hvis du har strukturert lageret slik at hyller med lignende hylleprioritering er side ved side, blir jobben enklere for de lageransatte ved at de slipper å utføre enkelte trinn.  
    * Du kan velge ikke å ta med linjene som [!INCLUDE[prod_short](includes/prod_short.md)]] opprettet da det konverterte en større enhet til mindre enheter, ved å merke av i **Angi anbrekksfilter**-feltet. Finn ut mer om anbrekk under [Aktivere automatisk samlet oppbryting med lagerstyring og plukk](warehouse-enable-automatic-breaking-bulk-with-directed-put-away-and-pick.md)  
    * Du kan velge at feltet **Ant. som skal håndt.** ikke fylles automatisk ut i plasseringsinstruksjonene.  
    * Du kan velge å skrive ut dokumentet umiddelbart.  

8. Velg **OK** for å opprette plasseringen.  

## <a name="to-create-a-put-away-from-a-posted-receipt"></a>Slik oppretter du en plassering fra et bokførte mottak:

Hvis en lokasjon bruker både plasserings- og mottaksbehandling og du har slettet plasseringslinjer, eller hvis du bruker lagerstyring og har bestemt deg for å ikke bruke plasseringsforslaget, kan du opprette eller gjenopprette plasseringsinstruksjoner for de bokførte mottakslinjene på følgende måte:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Bokførte lagermottak**, og velg deretter den relaterte koblingen.  
2. Velg et bokført mottak som skal plasseres.  
3. Velg handlingen **Kort**.  

    Hvis feltet **Dokumentstatus** er tomt, er mottaket ikke plassert. Ellers indikerer feltet om mottaket er delvis eller fullstendig plassert.  

4. Hvis mottaket er delvis plassert eller ikke plassert, klikker du på handlingen **Opprett plassering**.  
5. Fyll ut feltene etter behov, og klikk deretter **OK**.  

## <a name="to-put-items-away"></a>Slik plasserer du varer

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lagerplasseringer** og velg den relaterte koblingen.

2. Åpne lagerplasseringen som er klar til å håndtere.  
3. Hvis lageret krever det, angir du bruker-ID-en når du begynner å arbeide med en plassering.  

    Du kan sortere plasseringslinjene etter ulike kriterier, for eksempel etter vare, hyllenummer eller forfallsdato. Sortering kan bidra til å optimalisere plasseringsprosessen, for eksempel:

    * Hvis Hent- og Plasser-linjene for hvert mottak ikke følger umiddelbart etter hverandre, og du vil at de skal gjøre det, kan du sortere linjene ved å velge **Vare** i feltet **Sorteringsmetode**.  
    * Hvis hylleprioritering gjenspeiler det fysiske oppsettet av lageret, kan du bruke sorteringsmetoden **hylleprioriteringen** til å organisere arbeidet etter hyllelokasjoner.

4. Utfør handlingene.

    Hvis en hyllekode er obligatorisk for lokasjonene, blir alle mottakslinjer minst to linjer i lagerplasseringen, som vist nedenfor.  

    * Den første linjen, med **Hent** i **Handlingstype**-feltet, angir hvor varene er plassert i mottaksområdet. Du kan ikke endre sonen og hyllen på denne linjen.  
    * Den neste linjen, med **Plasser** i **Handlingstype**-feltet, viser hvor du må plassere varene i lageret. Hvis du mottar et stort antall varer på én mottakslinje, kan det hende du må plassere varene i flere hyller, det finnes derfor en Plass-linje for hver hylle. 

    > [!NOTE]
    > Hvis du må plassere varene for én linje i mer enn én hylle, for eksempel fordi den angitte hyllen er full, bruker du handlingen **Del linje** i hurtigfanen **Linjer**. Handlingen oppretter en linje der restantallet skal håndteres.

5. Når du har plassert alle varene i hyller i henhold til instruksjonen, velger du handlingen **Registrer plassering**.  

## <a name="see-related-microsoft-training"></a>Se relatert [Microsoft-opplæring](/training/modules/receive-put-away-items/)

## <a name="see-also"></a>Se også

[Oversikt over lagerstyring](design-details-warehouse-management.md)
[Lager](inventory-manage-inventory.md)  
[Definer lagerstyring](warehouse-setup-warehouse.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
