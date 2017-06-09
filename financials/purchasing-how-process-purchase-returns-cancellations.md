---
title: Behandle bestillingsreturer eller annulleringer| Microsoft-dokumentasjon
description: Behandle bestillingsreturer eller annulleringer
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cancel, undo, correct
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: f87b51ac746c6586e4ebb3b09aaa8d5ee7ac391d
ms.contentlocale: nb-no
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-process-purchase-returns-or-cancellations"></a>Behandle bestillingsreturer eller annulleringer
Hvis du vil returnere varer til leverandøren eller avbryte tjenester du har kjøpt, kan du opprette og bokføre en kjøpskreditnota som angir den ønskede endringen med hensyn til den opprinnelige kjøpsfakturaen. Du kan opprette kjøpskreditnotaen fra den bokførte kjøpsfakturaen for å ta med de riktige opplysningene for kjøpsfakturaen, eller bruke en kopifunksjon.

**Merk**: Hvis en bokført kjøpsfaktura ennå ikke er betalt, kan du bruke funksjonen **Korriger** eller **Annuller** på den bokførte kjøpsfakturaen til å reversere de involverte transaksjonene automatisk. Disse funksjonene fungerer bare for ubetalte fakturaer, og de støtter ikke delvise returer eller annulleringer. Hvis du vil ha mer informasjon, kan du se [Korrigere eller annullere ubetalte kjøpsfakturaer](purchasing-how-correct-cancel-unpaid-purchase-invoices.md).

Vanligvis oppretter du en kjøpskreditnota i relasjon til en kreditnota du har mottatt fra en leverandør. Kjøpskreditnotaen fungerer som den interne dokumentasjonen av kreditnotaprosessen for regnskapsformål.

Endringen kan relateres til alle produktene på den opprinnelige kjøpsfakturaen eller bare noen av produktene. Du kan derfor delvis returnere mottatte varer eller kreve delvis refusjon av mottatte tjenester. I det tilfellet må du redigere informasjon om den kopierte kjøpsfakturaen.

I tillegg til den opprinnelige bokførte kjøpsfakturaen, kan du bruke kjøpskreditnotaen for andre kjøpsdokumenter, for eksempel en annen bokført kjøpsfaktura, fordi du også returnerer varer som leveres med denne fakturaen.

## <a name="to-create-a-purchase-credit-memo-from-a-posted-purchase-invoice"></a>Opprett en kjøpskreditnota fra en bokført kjøpsfaktura
1. I øvre høyre hjørne, velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Kjøpskreditnotaer**, og deretter velger du den beslektede koblingen.  
2. I vinduet Bokførte **Kjøpsfakturaer** velger du den bokførte kjøpsfakturaen som du vil tilbakeføre, og deretter velger du handlingen **Opprett korrigerende kreditnota**.

    De fleste feltene på kjøpskreditnotahodet fylles ut med informasjon fra den bokførte kjøpsfakturaen. Du kan redigere alle feltene, for eksempel med ny informasjon som gjenspeiler returavtalen.
3. Redigere informasjonen på linjene i henhold til avtalen, for eksempel antall varer som returneres, eller beløpet som skal refunderes.
4. Velg handlingen **Utlign poster**.
5. I vinduet **Utlign leverandørposter** velger du linjen med det bokførte kjøpsdokumentet du vil utligne kjøpskreditnotaen mot, og deretter velger du handlingen **Utlignings-ID**. Nummeret på kjøpskreditnotaen settes inn i feltet **Utlignings-ID**.
6. I feltet **Beløp som skal utlignes** skriver du inn beløpet som du vil utligne hvis mindre enn det opprinnelige beløpet.

    Nederst i vinduet **Utlign leverandørposter** kan du se det totale beløpet som skal utlignes for å tilbakeføre alle involverte poster, nemlig når verdien i **Saldo** -feltet er null.
7. Velg **OK**-knappen. Når du bokfører kjøpskreditnotaen, brukes den på de angitte bokførte kjøpsdokumenter.

    Når du har opprettet eller redigert nødvendige kjøpskreditnotalinjer og ett eller flere programmer er angitt, kan du fortsette med å bokføre kjøpskreditnotaen.
8. Velg handlingen **Bokfør**.

De bokførte kjøpsfakturaene du utligner kreditnotaen mot, er nå tilbakeført. Hvis du allerede har betalt den opprinnelige fakturaen, skal leverandøren nå refundere betalingen til deg. Hvis kreditnotaen bare er en del av produktet på den opprinnelige fakturaen, kan du bare betale det resterende beløpet på den opprinnelige kjøpsfakturaen for å lukke den.

Kjøpskreditnotaen fjernes og erstattes med et nytt dokument i listen over bokførte kjøpskreditnotaer.

## <a name="to-create-a-purchase-credit-memo-from-scratch"></a>Opprette en kjøpskreditnota fra bunnen av
1. I øvre høyre hjørne, velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Bokførte kjøpsfakturaer**, og deretter velger du den beslektede koblingen.
2. Velg handlingen **Ny** for å åpne en ny, tom kjøpskreditnota.
3. I feltet **Leverandør** angir du navnet på en eksisterende leverandør.
4. Velg handlingen **Kopier dokument**.
5. Velg **Bokført faktura** i **Bilagstype**-feltet i vinduet **Kopier kjøpsdokument**.
6. Velg **Dokumentnr.** -feltet for å åpne vinduet **Bokførte kjøpsfakturaer**, og velg deretter den bokførte kjøpsfakturaen som inneholder linjer du vil tilbakeføre.
7. Merk av for  **Gjenberegn linjer**  hvis du vil at de kopierte bokførte kjøpsfakturalinjene skal oppdateres med endringer i varepris og enhetskost etter at fakturaen er bokført.
8. Velg **OK**-knappen. De kopierte fakturalinjene settes inn i kjøpskreditnotaen.
9. Fullføre kjøpskreditnotaen som forklart i den avsnittet "Opprette en kjøpskreditnota fra en bokført kjøpsfaktura" i dette emnet.

## <a name="see-also"></a>Se også
[Innkjøp](purchasing-manage-purchasing.md)  
[Registrere kjøp](purchasing-how-record-purchases.md)  
[Korrigere eller annullere ubetalte kjøpsfakturaer](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

