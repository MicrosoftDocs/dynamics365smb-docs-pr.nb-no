---
title: Statusfelt i dokumenter
description: 'Lær om dokumentstatusen Åpen og Frigitt i tilbuds-, ordre- eller kreditnotadokumenter.'
author: brentholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: 'document, status, quote, order, credit memo, released, open, pending approval, pending prepayment,'
ms.search.form: null
ms.date: 09/19/2022
ms.author: bholtorf
---
# <a name="status-field-on-documents"></a><a name="status-field-on-documents"></a><a name="status-field-on-documents"></a>Statusfelt i dokumenter

Når du oppretter et tilbud, en ordre eller en kreditnota, viser feltet **Status** i dokumenthodet standardstatusen **Åpen**.

Når du har fylt ut dokumentet, kan du frigi det. [!INCLUDE[prod_short](includes/prod_short.md)] endrer verdien i **Status**-feltet til **Frigitt**. Denne statusen angir at ordren er klar for neste fase i behandlingen før den bokføres.

| Status | Description |
| ------ | ----------- |
| Åpne   | Du kan foreta endringer i dokumentet. |
| Frigitt | Dokumentet er frigitt til neste fase i behandlingen, og du kan ikke foreta endringer i linjer av typen *Vare* og *Aktiva*.<br /><br />Du kan åpne et frigitt dokument på nytt hvis du vil foreta endringer i innholdet. Hvis du vil flytte det justerte dokumentet til neste fase i behandlingen, må du frigi dokumentet på nytt. |
| Venter på godkjenning   | Dokumentet venter på godkjenning |
| Venter på forskudd | Det er bokført en forskuddsfaktura for dokumentet. |

## <a name="release-process"></a><a name="release-process"></a><a name="release-process"></a>Frigivelsesprosess

Du kan forenkle arbeidsflyten ved hjelp av frigivelsesprosessen. Den kan for eksempel hjelpe deg med å følge selskapets prosedyrer for godkjenninger eller for å starte lageraktiviteter.

### <a name="approval-procedures"></a><a name="approval-procedures"></a><a name="approval-procedures"></a>Godkjenningsprosedyrer

Selskapet kan ved hjelp av frigivelsesprosedyren vise at en annen bruker har godkjent dokumentet, eller at en ekstern kontakt kan oppfylle dokumentspesifikasjonene, som vist i eksemplene nedenfor.

* Du kan frigi en bestilling når leverandøren har gitt signal om at han kan innfri ordren.
* Du oppretter en bestilling og en annen bruker må godkjenne den, for eksempel av sikkerhetsmessige årsaker, før den kan frigis.
* Den som er ansvarlig for godkjenning av refusjoner, må frigi et kreditnota som du har opprettet.

Lær mer om godkjenningsarbeidsflyter under [Bruk arbeidsflyter](across-use-workflows.md).

### <a name="warehouse-activities"></a><a name="warehouse-activities"></a><a name="warehouse-activities"></a>Lageraktiviteter

Hvis ordrestatusen er **Åpen**, startes ikke leveringsforberedelsene på lageret, og det forventes ikke at varene skal mottas i en bestilling. Når du frigir ordren, angir du at den er klar, og at den kan inkluderes i lageraktivitetene.

## <a name="reopen-a-released-order"></a><a name="reopen-a-released-order"></a><a name="reopen-a-released-order"></a>Åpne en frigitt ordre på nytt

Du kan foreta endringer i en ordre som er frigitt hvis du åpner den på nytt. Du kan imidlertid bare øke antallet linjer som allerede er behandlet av lageret.

Når du har foretatt endringene og frigitt ordren på nytt, beregner [!INCLUDE [prod_short](includes/prod_short.md)] merverdiavgift (mva.) og fakturarabatten på nytt.

Hvis du foretar endringer i en frigitt ordre, må du gi lageret beskjed om endringene.

> [!NOTE]
> Hvis du vil bokføre én åpen ordre eller kreditnota uten først å frigi den, frigir [!INCLUDE [prod_short](includes/prod_short.md)] dokumentet automatisk når du bokfører det. Hvis du bokfører ordrer eller kreditnotaer ved hjelp av funksjonen for **massebokføring**, kan du velge å bare bokføre de ordrene eller kreditnotaene du har frigitt.

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se også

[Selg produkter med en kundeordre](sales-how-sell-products.md)  
[Registrer kjøp med kjøpsfakturaer](purchasing-how-record-purchases.md)  
[Levere varer](warehouse-how-ship-items.md)  
[Motta varer](warehouse-how-receive-items.md)  
[Bruke arbeidsflyter for godkjenning](across-how-use-approval-workflows.md)  
[Sortere, søke etter og filtrere oversikter](ui-enter-criteria-filters.md)  
[Arkivere dokumenter](across-how-to-archive-documents.md)  
[Generelle forretningsfunksjoner](ui-across-business-areas.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
