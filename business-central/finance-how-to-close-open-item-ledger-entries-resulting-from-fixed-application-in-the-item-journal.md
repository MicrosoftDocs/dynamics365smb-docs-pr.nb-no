---
title: Lukk vareposter som kom fra bruk av fast utligning
description: Finn ut hvordan du kan opprette en fast utligning manuelt mellom en inngående transaksjon og den opprinnelige utgående transaksjonen i varekladden.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: 40
ms.date: 07/30/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal"></a>Lukke åpne vareposter som er et resultat av fast utligning i varekladden

Du kan bruke feltet **Utlignet fra-post** på siden **Varekladd** til å opprette en fast utligning manuelt mellom en inngående transaksjon og den opprinnelige utgående transaksjonen. Du kan for eksempel bruke det til å rette den utgående transaksjonen eller behandle returen.  

> [!IMPORTANT]  
> Faste utligninger som gjøres på denne måten, bruker bare kostnader, ikke antallet. Den bokførte positive vareposten vil på samme måte ikke lukke den brukte utgående posten og vil selv forbli åpen. Dette gjelder også når du bokfører en fast utligning for en positiv post til en negativ post som ikke er lukket av en vanlig positiv post – da vil både den negative og den positive posten forbli åpne.  
>
> Dette betyr at du ikke kan lukke en lagerperiode hvis det finnes en slik post.  

Under visse betingelser kan du endre og utligne utligningsposter på nytt ved å bruke siden **Utligningsforslag**.  

Følgende fremgangsmåte viser hvordan du lukker slike poster ved å utføre to korrigerende bokføringer i varekladden.  

## <a name="to-close-open-item-ledger-entries-that-result-from-a-fixed-application-in-the-item-journal"></a>Slik lukker du åpne vareposter som er resultater fra en fast utligning i varekladden:

1. Bruk feltet **Utlignet-fra post** til å bokføre en oppjustering med tilsvarende antall. Dette lukker den opprinnelige negative korreksjonsposten med en fast utligning.  

    Feltet **Utlignet fra-post** angir nummeret på den utgående finansposten som har kostnader som er videresendt til den inngående vareposten, når du bokfører en inngående transaksjon av typen **Oppjustering** eller **Kjøp** med varekladden.  
2. Bruk feltet **Utligningspost** til å bokføre en nedjustering. Dette lukker den opprinnelige positive korreksjonsposten med en fast utligning.  

    Feltet **Utligningspost** angir om antallet på varekladdelinjen skal utlignes mot et bilag som allerede er bokført. I så fall angir du løpenummeret på vareposten som varekladdelinjen skal utlignes mot.

## <a name="see-also"></a>Se også

[Fjerne og utligne vareposter på nytt](finance-how-to-remove-and-reapply-item-entries.md)    
[Behandle salgsreturer og kanselleringer](sales-how-process-sales-returns-cancellations.md)    
[Definere lagerverdi og kostberegning](finance-set-up-inventory-valuation-and-costing.md)    
[Administrere lagerkostnader](finance-manage-inventory-costs.md)    
[Designdetaljer: Kostmetoder](design-details-costing-methods.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
