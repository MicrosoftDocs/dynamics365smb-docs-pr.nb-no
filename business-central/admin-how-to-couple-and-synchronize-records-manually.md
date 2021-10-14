---
title: Kobling og synkronisering
description: Synkronisering av en integrert tabelltilordning gjør det mulig å synkronisere data i alle poster i en tabell i Business Central og Dynamics 365 Sales-tabell som er koblet.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: crm, sales, couple, decouple, synchronize
ms.date: 10/01/2021
ms.author: bholtorf
ms.openlocfilehash: 8e2b36b4b90e1cc348ef381a6d0f6145a87ed043
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2021
ms.locfileid: "7588729"
---
# <a name="coupling-and-synchronizing-records-between-dataverse-and-business-central"></a>Kobling og synkronisering av poster mellom Dataverse og Business Central

Dette emnet beskriver hvordan du kobler sammen én eller flere poster i [!INCLUDE[prod_short](includes/prod_short.md)] med poster i Dataverse eller [!INCLUDE[crm_md](includes/crm_md.md)]. Kobling av poster lar deg vise Dataverse-informasjon fra [!INCLUDE[prod_short](includes/prod_short.md)], og omvendt. Kopling lar deg også synkronisere data mellom postene. Du kan koble eksisterende poster, eller du kan opprette og koble nye poster.

> [!Note]
> Kobling og synkronisering av data er bare tilgjengelig hvis systemansvarlig har opprettet en kobling mellom [!INCLUDE[prod_short](includes/prod_short.md)] og Dataverse eller [!INCLUDE[crm_md](includes/crm_md.md)]. En rask måte å kontrollere på, er å åpne **Kunde**-kortet og se etter handlingen **Konfigurer kobling**. Hvis handlingen er tilgjengelig, er appene koblet.   

## <a name="video-example"></a>Videoeksempel

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098376]

## <a name="to-couple-a-record"></a>Koble en post  
1.  I [!INCLUDE[prod_short](includes/prod_short.md)] åpner du kortet for posten du vil koble. For eksempel kunde- eller kontaktkortet.  

    Du kan også bare åpne listesiden og velge posten du vil koble.  

2.  Velg handlingen **Konfigurer kobling**.  
3.  Fyll ut feltene, og klikk deretter **OK**.  

## <a name="to-synchronize-a-single-record"></a>Synkronisere en enkeltoppføring  
1.  I [!INCLUDE[prod_short](includes/prod_short.md)] åpner du kortet for posten du vil koble. For eksempel kunde- eller kontaktkortet.  
2.  Velg **Synkroniser nå**-handlingen.  
3.  Hvis en post kan synkroniseres i én retning, velger du alternativet som angir retningen for dataoppdatering, og deretter velger du **OK**.  

## <a name="to-synchronize-a-single-record-from-crm_md"></a>Slik synkroniserer du en enkeltoppføring fra [!INCLUDE[crm_md](includes/crm_md.md)]  
1.  I [!INCLUDE[crm_md](includes/crm_md.md)] åpner du skjemaet for posten du vil koble. Det kan for eksempel være skjema for kontokort eller kontaktkort.  
2.  Velg **[!INCLUDE[prod_short](includes/prod_short.md)]-** handlingen på båndet for å åpne og koble til posten automatisk.

> [!Note]
> Du kan synkronisere én post fra [!INCLUDE[crm_md](includes/crm_md.md)] automatisk bare når det ikke er merket av for **Synkroniser bare koblede poster** og synkroniseringsretningen er satt til Toveis eller Fra integreringstabell på siden **Tilordning for integreringstabell** for posten. Hvis du vil ha mer informasjon, kan du se [Tilordne tabellene og feltene som skal synkroniseres](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records).     

## <a name="to-couple-multiple-records-using-match-based-coupling"></a>Slik lagrer du flere poster ved å bruke samsvarsbasert kobling

Du kan angi hvilke data som skal synkroniseres for en enhet, for eksempel en kunde eller kontakt, ved å koble poster basert på samsvar. Du kan begrense samsvarene ved å skille mellom store og små bokstaver og angi en prioritet for hvert samsvar. Hvis det ikke finnes noen samsvar, kan du også angi om du vil opprette enheten i Dataverse. Se [Tilpass samsvarsbasert kobling](admin-how-to-set-up-a-dynamics-crm-connection.md#customize-the-match-based-coupling) hvis du vil ha mer informasjon.  

1. I [!INCLUDE[prod_short](includes/prod_short.md)] åpner du listesiden for posten, for eksempel listesiden for kunder eller kontakter.
2. Velg handlingen **Samsvarsbasert kobling**.
3. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-synchronize-multiple-records"></a>Synkronisere flere poster  
1.  I [!INCLUDE[prod_short](includes/prod_short.md)] åpner du listesiden for posten, for eksempel listesiden for kunder eller kontakter.  
2.  Velg postene som skal synkroniseres, og velg deretter **Synkroniser nå**-handlingen.  
3.  Hvis poster kan synkroniseres i én retning, velger du alternativet som angir retningen, og deretter velger du **OK**.  

## <a name="uncoupling-records"></a>Oppheve kobling av poster
Du kan slette én eller flere poster fra listesider eller siden **Feil ved synkronisering av koblede data** ved å velge én eller flere linjer og velge **Slett kobling**. Du kan også fjerne alle koblingene for én eller flere tabelltilordninger på siden **Tilordninger for integreringstabell**.

## <a name="see-also"></a>Se også  
[Bruke Dynamics 365 Sales fra Business Central](marketing-integrate-dynamicscrm.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]