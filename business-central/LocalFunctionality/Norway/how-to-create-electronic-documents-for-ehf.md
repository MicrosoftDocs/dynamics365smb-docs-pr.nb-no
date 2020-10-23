---
title: Opprette elektroniske dokumenter for EHF
description: Når du selger varer eller tjenester til en kunde i offentlig sektor, må du sende dokumenter elektronisk.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: cd2a13b7949a6f79772d924c0f90101d3919a8d7
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3919793"
---
# <a name="create-electronic-documents-for-ehf"></a>Opprette elektroniske dokumenter for EHF
Når du selger varer eller tjenester til en kunde i offentlig sektor, må du sende dokumenter elektronisk.  I [!INCLUDE[d365fin](../../includes/d365fin_md.md)] kan du opprette elektroniske dokumenter for fakturaer, kreditnotaer, purringer og rentenotaer. Før du kan opprette elektroniske dokumenter, må du angi filplasseringen og opplysninger om kundene. Hvis du vil ha mer informasjon, kan du se [Sette opp EHF](how-to-set-up-ehf.md) og [Sette opp kunder for EHF](how-to-set-up-customers-for-ehf.md).

Du kan bare opprette elektroniske dokumenter etter at et dokument er bokført eller utstedt. Følgende fremgangsmåte viser hvordan du bokfører en salgsfaktura med nødvendig informasjon og deretter oppretter en elektronisk salgsfaktura, men de samme trinnene gjelder også for salgskreditnotaer, purringer, rentenotaer, servicefakturaer og servicekreditnotaer.  

> [!NOTE]  
>  Summen av linjene i et eksportert elektronisk dokument gjenspeiler ikke fakturaavrunding, selv om det er aktivert. I stedet summerer [!INCLUDE[d365fin](../../includes/d365fin_md.md)] linjene uten avrunding.  

## <a name="to-post-a-sales-invoice"></a>Slik bokfører du en salgsfaktura:  

1.  Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](../../media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Salgsfakturaer**, og velg deretter den relaterte koblingen.  
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

1.  Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](../../media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bokførte salgsfakturaer**, og velg deretter den relaterte koblingen.  
2.  Velg den aktuelle salgsfakturaen.  
3.  Velg handlingen **Opprett elektronisk faktura**.  

    > [!IMPORTANT]  
    >  Du må merke av for **E-faktura** på fakturaen hvis du vil opprette en elektronisk faktura.  

4.  Hvis du vil, kan du angi flere filtre på kjørselssiden **Opprett elektroniske fakturaer**.  
5.  Velg **OK**.  

En XML-fil opprettes og lagres på lokasjonen som er definert på **Salgsoppsett**-siden. Du kan nå sende dokumentet til kunden.  

## <a name="see-also"></a>Se også  
 [EHF – Elektronisk fakturering i Norge](ehf-electronic-invoicing-in-norway.md)
