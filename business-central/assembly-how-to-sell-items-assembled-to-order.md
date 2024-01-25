---
title: Selge varer som er montert til ordre
description: Finn ut hvordan du selger en vare som er montert til ordre.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 11/23/2022
ms.search.keywords: 'kit, kitting, substitute items'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
ms.custom: bap-template
---
# Selg varer som er montert til ordre

Varer som er konfigurert for Monter til ordre, forventes ikke å være på lager og blir montert når den er inkludert i en ordre. En vare er definert for Monter til ordre når feltet **Monteringsprinsipp** på varekortet inneholder **Monter til ordre**. Når du angir varen på en ordrelinje, blir en monteringsordre automatisk opprettet og koblet til ordren.  

> [!NOTE]  
> Hvis montere-til-ordre-varer allerede er på lager, kan du trekke dette antallet fra monteringsordren og reservere det fra beholdningen. Finn ut mer under [Selg lagervarer i monter-til-ordre-flyter](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).  

I denne fremgangsmåten behandler du salget av en vare som skal monteres i henhold til spesifikasjonene kunden har bedt om. Trinnene omfatter følgende: 

* oppretting av en ordrelinje
* tilpasning av monteringsvaren ved å redigere komponentene og ressursene
* kontroll av tilgjengelighet for å etablere en leveringsdato
* frigivelse av ordren slik at den kan monteres og leveres umiddelbart  

> [!NOTE]  
> Følgende fremgangsmåte omfatter ikke trinnene for å opprette en standardordre som skjer før trinnet der du angir montere-til-ordre-varen på en ordrelinje. Finn ut mer om å opprette ordrer under [Selg produkter med en kundeordre](sales-how-sell-products.md).  

## Selge en vare som er montert til ordre

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Ordrer**, og velg deretter den relaterte koblingen.  
2. Opprett en ordre. 
3. I **Nr.** -feltet angir du en vare som er definert for å monteres til ordre.  
4. Definer hvilken lokasjon varen skal selges fra, i **Lokasjonskode**-feltet. Monteringsprosessen vil skje på den lokasjonen.  
5. Angi hvor mange enheter som skal selges, i **Antall**-feltet.  

    > [!NOTE]  
    >  Hvis en eller flere komponenter i det forespurte monteringsvareantallet ikke er tilgjengelige, åpnes en side med et tilgjengelighetsadvarsel. <!-- Check whether the field help would be useful. For more information, see Assembly Availability.  -->

    En montersordre opprettes og kobles til ordrelinjen. Forfallsdatoen for monteringsordren er forsendelsesdatoen på ordrelinjen.  

    Antallet som skal selges, kopieres til feltet **Ant. å montere til ordre**, som angir at vareoppsettet forventer at du monterer hele antallet på salgslinjen. Du kan redusere antallet som skal monteres, for eksempel hvis du vet at enkelte varer allerede er tilgjengelige. Finn ut mer under [Selg lagervarer i monter-til-ordre-flyter](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  

6. Hvis kunden ønsker en ekstra vare i et sett, går du til hurtigfanen **Linjer**, velger **Linje**, velger **Monter til ordre** og velger deretter **Montere til ordre-linjer** for å vise og endre standard monteringskomponenter. Du kan også merke feltet **Ant. som skal monteres til ordre**.  
7. Opprett en ny linje av typen **Vare** for tilleggsmonteringskomponenten i settet på siden **Montere til ordre – linjer**.  

    Du kan også tilpasse rekkefølgen ved å øke antallet for én standardvare i settet. Du kan gjøre dette ved å øke verdien i **Antall per**-feltet på den bestemte monteringsordrelinjen.  

    > [!NOTE]  
    >  Siden **Monteringsordrelinjene** inneholder de grunnleggende feltene for å tilpasse komponentlisten, legge til varesporingsnumre eller løse problemer med komponenttilgjengelighet. Hvis du vil legge til mer informasjon om monteringsordren, for eksempel startdatoen for den, velger du **Vis dokumenter**-handlingen. Dette åpner en full visning av monteringsordren som er knyttet til ordrelinjen. Du kan ikke endre innholdet i de fleste feltene i monteringsordretoppteksten, og du kan ikke bokføre monteringsutdata fra det. Du må bokføre levering av ordrelinjen.  
    >
    >  Bare **Startdato**-feltet kan endres i de koblede monteringsordrene. Hvis du endrer startdatoen, kan arbeidere angi at de starter monteringen tidligere enn forfallsdatoen. Alle feltene på linjene i den tilknyttede monteringsordren kan endres slik at lagermedarbeidere kan angi forbruksverdier under prosessen.  

8. Se gjennom eller reager på problemer med komponententilgjengelighet Velg for eksempel en erstatningsvare.  
9. Lukk siden **Montere til ordre – linjer**. Den koblede monteringsordren er nå klar, og arbeidere kan begynne å montere de tilpassede varene.  
10. På ordren velger du **Frigi** for å varsle monteringsavdelingen om at monteringsprosessen kan starte. Finn ut mer under [Monter varer](assembly-how-to-assemble-items.md).  

> [!NOTE]  
> Vareerstatninger erstatter ikke automatisk en vare med en annen vare, for eksempel når du oppretter en ordre eller i en stykkliste. I stedet blir du varslet om at en erstatning er tilgjengelig.

## Se også

[Monteringsstyring](assembly-assemble-items.md)  
[Arbeid med monteringsstykklister](assembly-how-work-assembly-boms.md)  
[Registrer nye varer](inventory-how-register-new-items.md)  
[Lager](inventory-manage-inventory.md)  
[Oversikt over lagerstyring](design-details-warehouse-management.md)
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]