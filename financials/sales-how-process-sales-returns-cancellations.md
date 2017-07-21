---
title: "Bruke en salgskreditnota til å behandle ordrereturer eller annulleringer | Microsoft-dokumentasjon"
description: "Beskriver hvordan du oppretter en salgskreditnota for å behandle en retur, kansellering eller refusjon for varer eller tjenester du har mottatt betaling for."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 06/21/2016
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: f08526054e99f742cedfefe036d8903304e54a56
ms.contentlocale: nb-no
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-process-sales-returns-or-cancellations"></a>Behandle ordrereturer eller annulleringer
Hvis en kunden vil returnere eller bli refundert for varer eller tjenester du har solgt og mottatt betaling for, må du opprette og bokføre en salgskreditnota som angir den ønskede endringen. Du kan opprette salgskreditnotaen fra den bokførte salgsfakturaen for å ta med de riktige opplysningene for salgsfakturaen, eller bruke en kopifunksjon.  

> [!NOTE]  
>   Hvis en bokført salgsfaktura ennå ikke er betalt, kan du bruke funksjonen **Korriger** eller **Annuller** på den bokførte salgsfakturaen for å tilbakeføre transaksjonene. Disse funksjonene fungerer bare for ubetalte fakturaer, og de støtter ikke delvise returer eller annulleringer. Hvis du vil ha mer informasjon, kan du se [Korrigere eller annullere ubetalte salgsfakturaer](sales-how-correct-cancel-sales-invoice.md).

I tillegg til den opprinnelige bokførte salgsfakturaen, kan du bruke salgskreditnotaen for andre salgsdokumenter, for eksempel en annen bokført salgsfaktura, fordi kunden også returnerer varer som leveres med denne fakturaen.

En returnert vare eller refusjon kan være knyttet til bare noen av varene eller tjenestene på den opprinnelige salgsfakturaen. I så fall må du redigere opplysningene på linjene på salgskreditnotaen. Når du bokfører salgskreditnotaen, tilbakeføres salgsdokumentene som påvirkes av endringen og en refusjonsbetaling kan opprettes for kunden.  

Du kan sende den bokførte salgskreditnotaen til kunden for å bekrefte returen eller annulleringen, og formidle at den tilknyttede verdien blir refundert, for eksempel når varene returneres.

Bokføringen av kreditnotaen tilbakefører også eventuelle varegebyr som var tilordnet det bokførte dokumentet, slik at varens verdiposter er de samme som før varegebyret ble tilordnet.

## <a name="to-create-a-sales-credit-memo-from-a-posted-sales-invoice"></a>Opprette en ny salgskreditnota fra en bokført salgsfaktura
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Bokførte salgsfakturaer**, og velg deretter den relaterte koblingen.  
2. I vinduet Bokførte **salgsfakturaer** velger du den bokførte salgsfakturaen som du vil tilbakeføre, og deretter velger du **Opprett korrigerende kreditnota**.

    For salgskreditnotahodet inneholder noen opplysninger fra den bokførte salgsfakturaen. Du kan redigere dette, for eksempel med ny informasjon som gjenspeiler returavtalen.  
3. Redigere informasjonen på linjene i henhold til avtalen, for eksempel antall varer som returneres, eller beløpet som skal refunderes.
4. Velg handlingen **Utlign poster**.
5. I vinduet **Utlign kundeposter** velger du linjen med det bokførte salgsdokumentet du vil utligne salgskreditnotaen mot, og deretter velger du handlingen **Utlignings-ID**.

    ID-en på salgskreditnotaen vises i feltet **Utlignings-ID**.
6. I feltet **Beløp som skal utlignes** skriver du inn beløpet som du vil utligne hvis mindre enn det opprinnelige beløpet.  

    Nederst i vinduet **Utlign kundeposter** kan du se det totale beløpet som skal utlignes for å tilbakeføre alle involverte poster, nemlig når verdien i **Saldo** -feltet er null.
7. Velg **OK**. Når du bokfører salgskreditnotaen, brukes den på de bokførte salgsdokumentene.

    Når du har opprettet eller redigert salgskreditnotalinjene, og ett eller flere programmer er angitt, kan du fortsette med å bokføre salgskreditnotaen.   
8. Velg handlingen **Bokfør og send**.  

Dialogboksen **Bokfør og send bekreftelse** åpnes, og viser den foretrukne sendemetoden for kunden. Du kan endre sendemetoden ved å velge oppslagsknappen for feltet **Send dokument til**. Hvis du vil ha mer informasjon, kan du se [Definere en profil for dokumentsending](sales-how-setup-document-send-profiles.md).  

De bokførte salgsdokumentene som du utlignet kreditnotaen mot, tilbakeføres, og en refusjonsbetaling kan opprettes for kunden. Salgskreditnotaen fjernes og erstattes med et nytt dokument i listen over bokførte salgskreditnotaer.

## <a name="to-create-a-sales-credit-memo-from-scratch"></a>Opprette en salgskreditnota fra bunnen av
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Salgskreditnotaer**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Ny** for å åpne en ny, tom salgskreditnota.
3. I feltet **Kunde** angir du navnet på en eksisterende kunde.
4. Velg handlingen **Kopier dokument**.
5. Velg **Bokført faktura** i **Bilagstype**-feltet i vinduet **Kopier salgsdokument**.
6. Velg **Dokumentnr.** -feltet for å åpne vinduet **Bokførte salgsfakturaer**, og velg deretter den bokførte salgsfakturaen som inneholder linjer du vil tilbakeføre.
7. Merk av for  **Gjenberegn linjer**  hvis du vil at de kopierte bokførte salgsfakturalinjene skal oppdateres med endringer i varepris og enhetskost etter at fakturaen er bokført.
8. Velg **OK**. De kopierte fakturalinjene settes inn i salgskreditnotaen.
9. Fullføre salgskreditnotaen som forklart i den avsnittet "Opprette en salgskreditnota fra en bokført salgsfaktura" i dette emnet.

## <a name="see-also"></a>Se også
[Salg](sales-manage-sales.md)  
[Sette opp salg](sales-setup-sales.md)  
[Sende dokumenter i e-post](ui-how-send-documents-email.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

