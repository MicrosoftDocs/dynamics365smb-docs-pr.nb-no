---
title: Flytte varer uplanlagt i enkle lageroppsett
description: Denne artikkelen forklarer ikke-planlagte interne flyttinger mellom hyller uten behov fra et kildedokument.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 12/16/2022
ms.custom: bap-template
ms.search.form: '393, 7382'
---
# <a name="move-items-internally-in-basic-warehouse-configurations"></a>Flytt varer internt i grunnleggende lageroppsett

Du vil kanskje flytte varer mellom hyller uten behov fra et kildedokument. Det kan for eksempel være en del av følgende aktiviteter:

* Organiser lageret på nytt.
* Overføre varer til et inspeksjonsområde.
* Flytt ekstra varer til og fra et produksjonsområde. 

Hvordan du flytter varer avhenger av hvordan lageret er definert som lokasjon. Finn ut mer under [Definer lagerstyring](warehouse-setup-warehouse.md).

I lageroppsett der den **Hylle obligatorisk**-oppsett er aktivert, men ikke **Lagerstyring**, kan du registrere ikke-planlagte flyttinger på følgende sider:  

* På siden **Intern flytting**.
* På siden **Varereklassifiseringskladd**.  

## <a name="internal-movements"></a>Interne flyttinger

Med siden **Interne flyttinger** kan du angi Hent- og Plasser-linjer når det ikke er et behov fra et kildedokument. Siden Intern flytting er som et forslag til organisering av ting. Du kan ikke behandle den faktiske flyttingen direkte fra den. Når en linje er fylt ut, bruker du handlingen **Opprett lagerflytting** til å sende linjen til siden **Lagerflytting**, som er stedet der du behandler og registrerer flyttingen.

### <a name="to-move-items-as-an-internal-movement"></a>Flytte varer som en intern flytting

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Interne flyttinger**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**. Pass på at **Nr.** -feltet i hurtigfanen **Generelt** er fylt ut.
3. Angi lokasjonen der flyttingen finner sted, i **Lokasjonskode**-feltet.  

    Hvis lokasjonen er standardlokasjonen for deg som lageransatt, legges lokasjonskoden til automatisk.  
4. Angi koden for hyllen som du vil flytte varene til, i feltet **Til hylle-kode**.

    I produksjon kan hyllen for eksempel være den åpne produksjonshyllekoden, som definert på lokasjonskortet eller i arbeidssenteret.  
5. Angi datoen flyttingen må fullføres innen, i **Forfallsdato**-feltet.  
6. Fyll ut feltene på linjen på hver linje etter behov. Interne flyttedokumenter har én linje per flytting. Linjen inneholder både Ta- og Plasser-handlingene.
7. Velg **Varenr.**-feltet for å åpne siden **Hylleinnholdsoversikt**. Velg varen som skal flyttes, basert på tilgjengeligheten i hyller. Du kan også velge handlingen **Hent hylleinnhold** for å fylle ut de interne flyttelinjene basert på filtrene.  

    Når du har valgt varen, blir feltet **Fra hylle-kode** automatisk fylt ut i henhold til det valgte hylleinnholdet. Du kan velge en hvilken som helst hylle der varen er tilgjengelig. Feltene **Varenr.** og **Fra hylle-kode** er knyttet sammen. Hvis du endrer verdien i et felt, endres kanskje verdien i det andre feltet.  

    Feltet **Til hylle-kode** er fylt ut med verdien du angav i toppteksten. Du kan endre det på linjen til en hvilken som helst annen hyllekode som ikke er sperret eller dedikert til spesielle formål. Finn ut mer under [Feltet dedikert](warehouse-how-to-create-individual-bins.md#the-dedicated-field).  

8. Når du har definert hvilke hyller du vil flytte varene fra og til, angir du antallet som skal flyttes, i feltet **Antall**.  

    > [!NOTE]  
    > Antallet må være tilgjengelig i hyllen som er angitt i feltet **Fra hylle-kode**.  

9. Når du er klar til å behandle flyttingen, velger du handlingen **Opprett lagerflytting**.  

    > [!NOTE]  
    >  Når du har opprettet flyttingen, slettes linjene for intern flytting.  

Utfør resten av den uplanlagte flyttingen på siden **Lagerflytting** på samme måte som for en flytting basert på kildedokumenter.

### <a name="to-record-the-inventory-movement"></a>Slik registrerer du lagerflyttingen

1. Åpne dokumentet du vil registrere flyttingen for, på siden **Lagerflytting**.  
2. I **Hyllekode**-feltet på flyttelinjene er hyllen der varene skal plukkes fra der varen er tilgjengelig. Du kan endre hyllen ved behov.
3. Utfør flyttingen, og angi opplysninger om det flyttede antallet i feltet **Ant. som skal håndt**. Verdiene på Hent- og Plasser-linjene må være like. Eller kan du ikke registrere flyttingen.

    Hvis du må ta varene for en linje fra mer enn én hylle, for eksempel fordi hele antallet ikke er i hyllen, bruker du handlingen **Del linje** i hurtigfanen **Linjer**. Handlingen oppretter en linje der restantallet skal håndteres.  
4. Velg handlingen **Registrer lagerflytting**.  

Følgende skjer under bokføringsprosessen:

* Lagerposter angir at antallet overføres fra Hent-hyller til Plasser-hyllene.

## <a name="to-move-items-with-the-item-reclassification-journal"></a>Flytte varer med varereklassifiseringskladden

I stedet for å bruke flyttingsdokumenter kan du registrere flyttinger ved å reklassifisere hyllekodene på varer. Finn ut mer under [Telle, justere og reklassifisere lagerbeholdning ved hjelp av kladder](inventory-how-count-adjust-reclassify.md).

> [!NOTE]  
> Flyttinger bokført med reklassifiseringskladder gjør ikke flyttedokumentene klare til å flytte.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lagervarereklassif.kladd** og velg den relaterte koblingen.  
2. På hver kladdelinje kan du definere hyllene du vil flytte varene fra og til, ved å fylle ut feltene **Hyllekode** og **Ny hyllekode**.  

    1. Hvis du vil flytte hele hylleinnholdet fra en hylle til en annen, velger du handlingen **Hent hylleinnhold**.  
    2. Bruk filtrene for å finne hyllen som inneholder varene du vil flytte, og velg deretter **OK**. Kladdelinjene fylles ut med innholdet i hyllen.  
3. Fyll ut de gjenstående feltene på hver kladdelinje.
4. Bokfør reklassifiseringskladden.  

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## <a name="see-also"></a>Se også

[Oversikt over lagerstyring](design-details-warehouse-management.md)
[Lager](inventory-manage-inventory.md)  
[Definer lagerstyring](warehouse-setup-warehouse.md)  
[Monteringsstyring](assembly-assemble-items.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
