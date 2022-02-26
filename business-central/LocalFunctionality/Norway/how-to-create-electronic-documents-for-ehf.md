---
title: Opprette elektroniske dokumenter for EHF
description: Når du selger varer eller tjenester til en kunde i offentlig sektor, må du sende dokumenter elektronisk.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 697e28bb05e6c06513f10eb60657c6c5d52091d7
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/08/2021
ms.locfileid: "6445065"
---
# <a name="create-electronic-documents-for-ehf"></a>Opprette elektroniske dokumenter for EHF
Når du selger varer eller tjenester til en kunde i offentlig sektor, må du sende dokumenter elektronisk.  I [!INCLUDE[prod_short](../../includes/prod_short.md)] kan du opprette elektroniske dokumenter for fakturaer, kreditnotaer, purringer og rentenotaer. Før du kan opprette elektroniske dokumenter, må du angi filplasseringen og opplysninger om kundene. Hvis du vil ha mer informasjon, kan du se [Sette opp EHF](how-to-set-up-ehf.md) og [Sette opp kunder for EHF](how-to-set-up-customers-for-ehf.md).

Du kan bare opprette elektroniske dokumenter etter at et dokument er bokført eller utstedt. Følgende fremgangsmåte viser hvordan du bokfører en salgsfaktura med nødvendig informasjon og deretter oppretter en elektronisk salgsfaktura, men de samme trinnene gjelder også for salgskreditnotaer, purringer, rentenotaer, servicefakturaer og servicekreditnotaer.  

> [!NOTE]  
>  Summen av linjene i et eksportert elektronisk dokument gjenspeiler ikke fakturaavrunding, selv om det er aktivert. I stedet summerer [!INCLUDE[prod_short](../../includes/prod_short.md)] linjene uten avrunding.  

## <a name="to-post-a-sales-invoice"></a>Slik bokfører du en salgsfaktura:  

1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Salgsfakturaer**, og velg deretter den relaterte koblingen.  
2.  Velg salgsfakturaen du vil bokføre, og velg deretter **Rediger**.  
3.  På **Generelt**-hurtigfanen kontrollerer du at disse feltene inneholder verdier:  

    - **Eksterndokumentnr.**  
    - **Deres referanse**  

    **Eksterndokumentnr.**-feltet viser dokumentnummeret som kunden har oppgitt.  

4.  På **Fakturering**-hurtigfanen kontrollerer du at disse feltene inneholder verdier:  

    - **GLN-nr.**  
    - **Kontokode**  
    - **Faktura til-kundenr.**  
    - **Forsendelsesdato**  

    Merk av for **E-faktura**.  

    Standardverdien i feltet **Forsendelsesdato** er bokføringsdatoen for dokumentet.  

    > [!NOTE]  
    >  For purringer og rentenotaer er feltet **GLN-nr.**, **Kontokode** og **E-faktura** på **Bokføring**-hurtigfanen.  

5.  Velg handlingen **Bokfør** for å bokføre fakturaen.  

## <a name="to-create-an-electronic-sales-invoice"></a>Slik oppretter du en elektronisk salgsfaktura:  

1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Bokførte salgsfakturaer**, og velg deretter den relaterte koblingen.  
2.  Velg den aktuelle salgsfakturaen.  
3.  Velg handlingen **Opprett elektronisk faktura**.  

    > [!IMPORTANT]  
    >  Du må merke av for **E-faktura** på fakturaen hvis du vil opprette en elektronisk faktura.  

4.  Hvis du vil, kan du angi flere filtre på kjørselssiden **Opprett elektroniske fakturaer**.  
5.  Velg **OK**.  

En XML-fil opprettes og lagres på lokasjonen som er definert på **Salgsoppsett**-siden. Du kan nå sende dokumentet til kunden.  

## <a name="see-also"></a>Se også  
 [EHF – Elektronisk fakturering i Norge](ehf-electronic-invoicing-in-norway.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]