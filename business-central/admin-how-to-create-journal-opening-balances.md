---
title: Opprette inngående balanser for kladd | Microsoft-dokumentasjon
description: Business Central omfatter mange kjørsler som er gitt for å hjelpe i overføringen av eldre kontobalanser til et nylig konfigurert selskap. Du kan enkelt overføre disse dataene med kladdebokføringer.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 2c42e87db1e0dd792d9b4444db3cfe5d1a05ed48
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3187151"
---
# <a name="create-journal-opening-balances"></a>Opprette inngående balanser for kladd
[!INCLUDE[d365fin](includes/d365fin_md.md)] omfatter mange kjørsler som er gitt for å hjelpe i overføringen av eldre kontobalanser til et nylig konfigurert selskap. Du kan enkelt overføre disse dataene med kundekladden, leverandørkladden, varekladden eller finanskladden.

Det første trinnet er å opprette en konfigurasjonspakke som inneholder oppsettstabellene for disse kladdene. Følgende fremgangsmåte forutsetter at dette trinnet er fullført. Du finner mer informasjon under [Definere selskapskonfigurasjon](admin-set-up-company-configuration.md). Denne fremgangsmåten beskriver de påfølgende trinnene, blant annet å bruke pakken som er levert av en partner.  

Før du begynner, må du kontrollere at du bruker rollesentersiden for administrasjon, fordi denne gir riktig kontekst for konfigurasjonsarbeidet. Hvis du vil ha mer informasjon, kan du se [Endre grunnleggende innstillinger](ui-change-basic-settings.md).

## <a name="to-apply-the-entries-in-a-journal-to-a-new-company"></a>Slik utligner du poster i en kladd mot et nytt selskap:  
1. Konfigurer og bruk en konfigurasjonspakke for det. Hvis du vil ha mer informasjon, kan du se [Konfigurere et selskap med RapidStart-veiviseren](admin-how-to-configure-a-company-with-the-rapidstart-wizard.md).  

    Det nye selskapet inneholder ikke informasjon om inngående balanser for kladd.  

2. Åpne konfigurasjonsforslaget og importer eksisterende data om kunder, varer, leverandører og finans. Hvis du vil ha mer informasjon, kan du se [Flytte kundedata](admin-migrate-customer-data.md).  
3. Velg for eksempel handlingen **Opprett finanskladdelinjer**.  
4. Fyll ut det som er aktuelt i hurtigfanen **Alternativer**, og angi filtre etter behov. Skriv for eksempel inn et navn i **Kladdemal**-feltet.  
5. Velg **OK**-knappen. Nå er postene i kladden, men beløpene er tomme.  
6. Eksporter kladdetabellen til Excel, og angi informasjon om bokføring og motkonto fra eldre data manuelt.
7. Importere og bruke tabellinformasjon for det nye selskapet. Kladdelinjene er klare for bokføring.  
8. Velg kladdelinjetabellen i konfigurasjonsforslaget, og velg deretter handlingen **Databasedata**.  
9. Se gjennom informasjonen, og velg deretter **Bokfør**-handlingen.  
10. Gjenta trinnene for å importere og bokføre eventuelle åpningssaldoer.  

## <a name="see-also"></a>Se også  
[Bruke konfigurasjoner for nye selskaper](admin-apply-configuration-to-new-companies.md)  
[Konfigurere et selskap med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administrasjon](admin-setup-and-administration.md)
