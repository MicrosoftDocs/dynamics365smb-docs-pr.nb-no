---
title: Gi tilbud på et montere-til-ordre-salg
description: Du kan bruke monteringsstyring for å tilpasse en monteringsvare i henhold til en kundeforespørsel under salgsprosessen.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="quote-an-assemble-to-order-sale" />Gi tilbud på et montere-til-ordre-salg

Du kan bruke monteringsstyring for å tilpasse en monteringsvare i henhold til en kundeforespørsel under salgsprosessen. Hvis du vil ha mer informasjon, kan du se [Selge varer som er montert til ordre](assembly-how-to-sell-items-assembled-to-order.md).  

Etter hvert som du selger en hvilken som helst annen type vare, kan du også opprette et tilbud for en tilpasset monteringsvare før du konverterer det til en ordre. Denne prosessen omfatter flere ekstra trinn når du sammenligner den med å opprette et vanlig tilbud, og den bruker en variant av en koblet monteringsordre, som er et monteringstilbud.

> [!NOTE]  
>  I likhet med alle typer tilbud brukes ikke antallene på monteringstilbud i tilgjengelighet, planlegging eller reservasjoner.  

## <a name="to-create-a-sales-quote-for-an-assemble-to-order-item" />Slik oppretter du et tilbud for en montere-til-ordre-vare:

1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Tilbud**, og velg deretter den relaterte koblingen.  
2.  Opprette en ny tilbudslinje med én linje for en monteringsvare. Hvis du vil ha mer informasjon, kan du se [Gi salgstilbud](sales-how-make-offers.md).  
3.  Angi hele antallet i feltet **Ant. som skal monteres til ordre**.

    > [!NOTE]  
    >  Du bør ikke gi tilbud på et delvist antall. Du må derfor angi samme antall som du skrev inn i feltet **Antall** på tilbudslinjen.  

4.  På hurtigfanen **Linjer**, velg **Linje**, **Monter til ordre**, og deretter **Montere til ordre – linjer**. Du kan også merke feltet **Ant. som skal monteres til ordre** på linjen.  
5.  Gå gjennom eller endre monteringsordrelinjene i henhold til tilbudet kunden ber om, på siden **Montere til ordre – linjer**. Hvis du vil vise mer informasjon, velger du **Vis dokument** for å åpne hele rammetilbudsordren. Du kan ikke endre innholdet i de fleste av feltene, og du kan ikke bokføre.  
6.  Når du har justert monteringsordrelinjene i henhold til tilbudet, lukker du siden **Montere til ordre – linjer** for å gå tilbake til siden **Tilbud**.  
7.  Hvis kunden godtar tilbudet, oppretter du en ordre for den aktuelle monteringsvaren. Hvis du vil ha mer informasjon, kan du se [Gi salgstilbud](sales-how-make-offers.md). Det koblede monteringstilbudet og eventuelle tilpasninger knyttes til denne nye salgsordren for å klargjøre for montering av varen(e) som skal selges.  

## <a name="see-related-microsoft-trainingtrainingmodulesassemble-to-order-dynamics-365-business-central" />Se relatert [Microsoft-opplæring](/training/modules/assemble-to-order-dynamics-365-business-central/)

## <a name="see-also" />Se også

[Monteringsstyring](assembly-assemble-items.md)  
[Arbeid med monteringsstykklister](assembly-how-work-assembly-boms.md)  
[Lager](inventory-manage-inventory.md)  
[Oversikt over lagerstyring](design-details-warehouse-management.md)
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
