---
title: Tilordne varegebyr til salg og kjøp (inneholder video)
description: 'Tildel varegebyrer når du trenger lagervarer for å overføre kostnader, for eksempel frakt og fysisk håndtering.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'transportation, added cost, landed cost'
ms.search.form: '5709, 5800, 5805, 5814'
ms.date: 11/08/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="use-item-charges-to-account-for-additional-trade-costs"></a>Bruk varegebyr til å gjøre rede for ekstra handelskostnader

For å sikre riktig verdisetting må lagervarene bære eventuelle ekstra kostnader, for eksempel frakt, fysisk håndtering, forsikring og transport, som du pådrar deg når du kjøper eller selger varer. Når det gjelder kjøp, består netto innkjøpspris for en vare av innkjøpsprisen fra leverandøren samt alle andre direkte varegebyr som kan tilordnes enkeltstående mottak eller returforsendelser. Når det gjelder salg, kan det være like viktig for selskapet ditt å være klar over kostnaden ved å levere solgte varer som netto innkjøpspris for kjøpte varer.

I tillegg til å registrere den ekstra kostnaden i lagerverdien kan du bruke varegebyr til følgende oppgaver:

* Identifisere netto innkjøpspris for en vare og dermed foreta mer nøyaktige beslutninger om hvordan distribusjonsnettverket skal optimaliseres.
* Analysere enhetskosten eller salgsprisen til en vare, slik at de kan brukes til analyseformål.
* Ta med kjøpsrabatter i enhetskosten og salgsrabatter i salgsprisen.

Før du kan tildele varegebyr, må du definere varegebyrnumrene for de ulike typene varegebyr. Numrene omfatter hvilke finanskontoer du kan bokføre kostnader i forbindelse med salg, kjøp og lagerjusteringer. Et varegebyrnummer inneholder en kombinasjon av varebokføringsgruppe, mva-gruppekode, mva-varebokføringsgruppe og varegebyr. Når du angir varegebyrnummeret i et kjøps- eller salgsdokument, hentes finanskontoen. Kontoen som hentes, velges basert på oppsettet av varegebyrnummeret og opplysningene i dokumentet.

Du kan tilordne et varegebyr på to måter for både kjøps- og salgsdokumenter:

* I dokumentet som inneholder varene som varegebyret er relatert til Vanligvis gjør du dette for dokumenter som ennå ikke er fullstendig bokført.
* På en separat faktura ved å knytte varegebyret til et bokført mottak eller en bokført følgeseddel der varene som varegebyret er knyttet til, er oppført.

> [!NOTE]  
> Du kan tilordne varegebyr til ordrer, fakturaer og kreditnotaer både for kjøp og salg. De følgende fremgangsmåtene viser hvordan du arbeider med varegebyr for en kjøpsfaktura. Trinnene er lignende for alle andre kjøps- og salgsdokumenter.

## <a name="example"></a>Eksempel

Denne videoen viser hvordan du håndterer en ekstra leveringskostnad som del av lageretterkalkulering.
<br><br>  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4b0SB?rel=0]

## <a name="to-set-up-item-charge-numbers"></a>Definere varegebyrnumre

Du bruker varegebyrnumre til å skille mellom de ulike typene varegebyr.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Varegebyr** og velg den relaterte koblingen.
2. Velg handlingen **Ny** på **Varegebyr**-siden for å opprette en ny linje.
3. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-assign-an-item-charge-directly-to-the-purchase-invoice-for-the-item"></a>Tilordne et varegebyr direkte til kjøpsfakturaen for varen

Hvis du vet varegebyret når du bokfører en kjøpsfaktura for varen, følger du denne fremgangsmåten.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Kjøpsfakturaer**, og velg deretter den relaterte koblingen.
2. Opprett en ny kjøpsfaktura. Hvis du vil ha mer informasjon, kan du se [Registrere kjøp](purchasing-how-record-purchases.md).
3. Kontroller at kjøpsfakturaen har én eller flere linjer av typen Vare.
4. Velg **Gebyr (vare)** i **Type**-feltet på en ny linje.
5. I feltet **Antall** angir du antall enheter for varegebyret du er fakturert for.
6. I feltet **Direkte enhetskost** angir du beløpet for varegebyret.
7. Fyll ut feltene som gjenstår, etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Gjør følgende fremgangsmåte for å utføre den faktiske tildelingen. Før varegebyret er fullstendig tilordnet, vises verdien i feltet **Ant. som skal tilordnes** i rød skrift.
8. I **Linjer**-fanen velger du handlingen **Varegebyrtilordning**.

    Siden **Varegebyrtilordning** åpnes, der én linje vises for hver linje av typen Vare på kjøpsfakturaen. Hvis du vil tilordne varegebyret til én eller flere fakturalinjer, kan du bruke en funksjon som tilordner og distribuerer den for deg, eller du kan fylle ut feltet **Ant. som skal tilordnes** manuelt. Fremgangsmåten nedenfor beskriver hvordan du bruker funksjonen Foreslå varegebyrtilordning.

9. På siden **Varegebyrtilordning** velger du handlingen **Foreslå varegebyrtilordning**.
10. Hvis det er flere fakturalinjer av typen Vare, velger du ett av de fire distribusjonsalternativene.  

Hvis varegebyret er fullstendig tilordnet, er verdien i feltet **Ant. som skal tilordnes** på kjøpsfakturaen null.

Varegebyret er nå tilordnet til kjøpsfakturaen. Når du bokfører mottaket av kjøpsfakturaen, oppdateres varens lagerverdier med varegebyrkostnaden.  

## <a name="to-assign-an-item-charge-from-a-separate-invoice-to-the-purchase-invoice-for-the-item"></a>Tilordne et varegebyr fra en separat faktura til kjøpsfakturaen for varen

Hvis du mottar en faktura for varegebyret etter at du har bokført det opprinnelige kjøpsmottaket, følger du denne fremgangsmåten.

1. Gjenta trinn 1 til og med 8 i [Tilordne et varegebyr direkte til kjøpsfakturaen for varen](payables-how-assign-item-charges.md#to-assign-an-item-charge-directly-to-the-purchase-invoice-for-the-item).
2. På siden **Varegebyrtilordning** velger du handlingen **Hent mottakslinjer**.
3. På siden **Mottakslinjer** velger du det bokførte kjøpsmottaket for varen du vil tilordne varegebyret til, og deretter velger du **OK**.
4. Velg handlingen **Foreslå varegebyrtilordning**.

Varegebyret på den separate kjøpsfakturaen er nå tilordnet til varen på det bokførte kjøpsmottaket og oppdaterer derved lagerverdien for varen med varegebyrkostnaden.

## <a name="handle-item-charges-for-partial-receipts"></a>Håndter varegebyrer for delvise mottak

La oss undersøke et eksempel på hvordan varegebyr for et delvis mottak skal håndteres.

Du har en bestilling med tre linjer:

* Det finnes to linjer for varer.
* En linje registrerer varegebyrer som er fordelt på tvers av varer per beløp.

Når varene er levert, finner du ut at én av varene mangler, slik at du ikke kan merke denne linjen som mottatt. Du kan bare motta og bokføre kjøpsfakturaen for den andre varen og håndtere den manglende varen senere.

Hvis du vil håndtere varekostnaden for delvis mottak, angir du **0** i feltet **Antall som skal håndteres** i linjen for den manglende varen på siden **Varegebyrtildeling**. Kopier deretter verdien fra feltet **Varegebyrantall som skal håndteres** til feltet **Fakturer (antall)** på bestillingslinjene.

Når du er klar til å håndtere varen som mangler, oppdaterer du feltet **Antall som skal håndteres** og bokfører bestillingen.

## <a name="see-also"></a>Se også

[Administrere skyldige beløp](payables-manage-payables.md)  
[Registrer kjøp](purchasing-how-record-purchases.md)  
[Fakturer salg](sales-how-invoice-sales.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
