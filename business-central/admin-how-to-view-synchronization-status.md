---
title: Vise statusen for synkroniseringsjobber (inneholder video)
description: Bruk siden Feil ved synkronisering av koblede data for å vise statusen til synkroniseringsjobber som har blitt kjørt for koblede poster i integreringer.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'sales, crm, integration, sync, synchronize'
ms.search.form: 6250
ms.date: 06/14/2021
ms.author: bholtorf
---

# <a name="view-the-status-of-synchronization-jobs"></a><a name="view-the-status-of-synchronization-jobs"></a><a name="view-the-status-of-synchronization-jobs"></a>Vise statusen til synkroniseringsjobber


Bruk siden **Feil ved synkronisering av koblede data** for å vise statusen til synkroniseringsjobber som har blitt kjørt for koblede poster i en Dataverse- eller [!INCLUDE[crm_md](includes/crm_md.md)]-integrasjon. Dette inkluderer jobber som ble kjørt fra jobbkøen, og manuelle synkroniseringsjobber som kjørte på poster fra [!INCLUDE[prod_short](includes/prod_short.md)]. Det kan for eksempel være nyttig å vise statusen deres når du feilsøker, fordi det gir deg tilgang til detaljer om feil relatert til koblede poster. Vanligvis er disse feiltypene forårsaket av brukerhandlinger, for eksempel når følgende er tilfelle:  

* To personer foretok en endring i de samme dataene i begge bedriftsappene.
* Noen slettet data i en av appene, men ikke i begge.

> [!Note]
> Siden **Feil ved synkronisering av koblede data** viser informasjon om jobber relatert til koblede poster. Hvis du løser alle feilene, men poster fremdeles ikke synkroniseres, kan det ha noe å gjøre med en innstilling for integrasjonen. Vanligvis må disse feiltypene løses av administratoren.   

## <a name="example"></a><a name="example"></a><a name="example"></a>Eksempel
Denne videoen viser et eksempel på hvordan du feilsøker feil som skjedde under synkronisering med [!INCLUDE[prod_short](includes/cds_long_md.md)]. Prosessen vil være den samme for alle integreringer. 

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2097304]


## <a name="to-view-and-resolve-synchronization-errors-for-coupled-records"></a><a name="to-view-and-resolve-synchronization-errors-for-coupled-records"></a><a name="to-view-and-resolve-synchronization-errors-for-coupled-records"></a>Slik viser du og løser synkroniseringsfeil for koblede poster
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Feil ved synkronisering av koblede data**, og velg deretter den relaterte koblingen.
2. Siden **Feil ved synkronisering av koblede data** viser problemer som oppstod da du synkroniserte koblede poster. Følgende tabell inneholder handlinger som du kan bruke til å løse problemer ett etter ett:

|Handling|Beskrivelse|
|----|----|
|**Fjern kobling**|Opphever kobling av postene, og de vil ikke lenger synkroniseres. Hvis du vil starte synkroniseringen på nytt, må du koble dem sammen på nytt. |
|**Prøv på nytt** og **Prøv alle på nytt**|For hver post der det oppdages en feil, blir synkronisering hoppet over med mindre du løser problemet. Prøv på nytt vil inkludere den valgte posten i neste synkronisering, og **Prøv alle på nytt** inkluderer alle oppføringene.|
|**Synkroniser**|Appen vil prøve å løse en konflikt der data ble endret i begge bedriftsappene. Du kan velge dataene som skal brukes.|
|**Gjenopprett poster** og **Slett poster**|Dette er nyttig i tilfeller der en post ble slettet i en av forretningsappene. Slett poster sletter posten eller raden i appen der den fortsatt finnes. Gjenopprett poster gjenskaper posten eller raden i forretningsappen der den ble slettet.|

> [!NOTE]
> Hvis du vil redusere antall konflikter du må løse, kan du konfigurere integreringstabelltilordningene for å bruke disse handlingene automatisk. Hvis du vil ha mer informasjon, kan du se [Tilordne integrasjonstabeller](admin-how-to-modify-table-mappings-for-synchronization.md#mapping-integration-tables).

## <a name="to-view-the-synchronization-log-for-a-specific-manually-synchronized-record"></a><a name="to-view-the-synchronization-log-for-a-specific-manually-synchronized-record"></a><a name="to-view-the-synchronization-log-for-a-specific-manually-synchronized-record"></a>Slik viser du synkroniseringsloggen for en bestemt (manuelt synkronisert) post
1. Åpne for eksempel en kunde, vare eller en annen post som synkroniserer data mellom [!INCLUDE[prod_short](includes/prod_short.md)] og Dataverse eller [!INCLUDE[crm_md](includes/crm_md.md)].
2. Velg **Synkroniseringslogg**-handlingen for å vise synkroniseringsloggen for en valgt post. For eksempel en bestemt kunde du synkroniserte manuelt.

## <a name="remove-couplings-between-records"></a><a name="remove-couplings-between-records"></a><a name="remove-couplings-between-records"></a>Fjerne koblinger mellom poster
Når noe går galt i integrasjonen din, og du må frakoble poster for å stoppe synkroniseringen av dem, kan du gjøre det for én eller flere poster om gangen. Du kan slette én eller flere poster fra listesider eller siden **Feil ved synkronisering av koblede data** ved å velge én eller flere linjer og velge **Slett kobling**. Du kan også fjerne alle koblingene for én eller flere tabelltilordninger på siden **Tilordninger for integreringstabell**. 

Hvis en enhet med enveis kobling slettes i [!INCLUDE[prod_short](includes/prod_short.md)], må du slette den brutte koblingen manuelt. Du gjør dette ved å velge handlingen **Søk etter slettede** på siden **Feil ved synkronisering av koblede data** og deretter slette koblingene.

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se også
[Sette opp brukerkontoer for integrasjon med Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md)  
[Bruk Dynamics 365 Sales fra Business Central](marketing-integrate-dynamicscrm.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
