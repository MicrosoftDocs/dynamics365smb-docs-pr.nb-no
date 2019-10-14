---
title: Legge til vedlegg, koblinger og merknader i poster | Microsoft Docs
description: Legg til en hyperkobling i et dokument eller et webområde til en bestemt post, for eksempel en kunde eller et dokument.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 84d58193fa7ee272b372403d63702348fbfb1f77
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2019
ms.locfileid: "2315279"
---
# <a name="manage-attachments-links-and-notes-on-cards-and-documents"></a>Behandle vedlegg, koblinger og merknader på kort og dokumenter

I faktaboksen på de fleste kort og dokumenter kan du legge ved filer, legge til koblinger og skrive merknader. For koblinger og merknader kan du også gjøre dette på listesiden ved først å merke den tilknyttede linjen.

Hvis du vil vise eller endre noen av disse vedlagte informasjonstypene, må du først åpne **Vedlegg**-kategorien i faktaboksen. Nummeret bak kategoritittelen angir hvor mange vedlagte filer, koblinger eller merknader som finnes for kortet eller dokumentet.

Vedlegg, koblinger og merknader forblir tilknyttet når kortet eller dokumentet behandles i andre statuser, for eksempel fra en pågående ordre til en bokført salgsfaktura. Vær imidlertid oppmerksom på at ingen av vedleggstypene blir skrevet ut fra systemet, for eksempel ved utskrift eller lagring til en fil.

## <a name="to-attach-a-file-to-a-purchase-invoice"></a>Knytte en fil til en kjøpsfaktura
Du kan legge ved alle typer filer, som inneholder tekst, bilder eller video, i et kort eller dokument. Dette er for eksempel nyttig når du vil lagre fakturaen for en leverandør som en PDF-fil på den relaterte kjøpsfakturaen i [!INCLUDE[d365fin](includes/d365fin_md.md)].

> [!NOTE]
> Filer som er knyttet til funksjonen for innkommende dokumenter, tas ikke med i kategorien **Vedlegg**. Se [Innkommende dokumenter](across-income-documents.md) for mer informasjon.

Følgende fremgangsmåte er basert på en ordre. Trinnene er lignende for alle andre støttede dokumenter og kort.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Kjøpsfakturaer**, og velg deretter den relaterte koblingen.
2. Åpne salgsordren som du vil legge til en fil i.
3. Åpne fanen **Vedlegg** i faktaboksen.
4. Velg verdien bak feltet **Dokumenter**, for eksempel 0.
5. På **Vedlagte dokumenter**-siden i **Vedlegg**-feltet velger du **Velg fil**-knappen.
5. Velg en fil fra en hvilken som helst plassering, og velg deretter **Åpne**-knappen.

Filen er nå knyttet til kjøpsfakturaen.

## <a name="to-add-a-link-from-an-item-card"></a>Legge til en kobling fra varekortet
Du kan legge til en kobling fra et kort eller et dokument i en hvilken som helst URL-adresse eller bane. Dette er nyttig når du for eksempel vil knytte et varekort til leverandørens varekatalog.

Følgende fremgangsmåte er basert på et varekort. Trinnene er lignende for alle andre støttede kort og dokumenter.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Varer**, og velg deretter den relaterte koblingen.
2. Velg varen du vil legge til en kobling fra, og velg deretter kategorien **Vedlegg** i faktaboksen.
3. I **Koblinger** velger du **+**-ikonet.
4. I vinduet **Koblingsadresse** angir du koblingen.

    - Hvis du vil koble til en fil på datamaskinen eller nettverket, angir du fullstendig bane og filnavn, for eksempel **C:\My Documents\invoice1.doc**.
    - Hvis du vil koble til et webområde, angir du Internett-adressen (URL-adressen), for eksempel **www.microsoft.com**.
    - Hvis du vil koble til et program, angir du en bestemt streng for å åpne programmet. For eksempel hvis du vil åpne Outlook med en ny, tom e-post til et bestemt alias, skriver du inn **mailto:testalias**.  

5. I **Beskrivelse**-feltet angir du informasjon om koblingen.  
6. Velg **OK**-knappen.

Koblingen er nå knyttet til varekortet.  

## <a name="to-write-a-note-on-a-sales-order"></a>Skrive en merknad på en ordre
Du kan skrive et notat på et dokument eller kort, for eksempel for å formidle spesielle instruksjoner til andre brukere av dokumentet eller kortet. Du kan inkludere filkoblinger og URL-adresser i notater.

> [!NOTE]
> Merknader i kategorien **Vedlegg** er ikke knyttet til interne notatfunksjoner, som hovedsakelig brukes til å kommunisere mellom arbeidsflytbrukere. Hvis du vil ha mer informasjon, kan du se [Konfigurere arbeidsflytvarsler](across-setting-up-workflow-notifications.md).

Følgende fremgangsmåte er basert på en ordre. Trinnene er lignende for alle andre støttede dokumenter og kort.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Ordrer**, og velg deretter den relaterte koblingen.
2. Velg ordren du vil skrive en merknad på, og velg deretter kategorien **Vedlegg** i faktaboksen.
3. I delen **Merknader** velger du **+**-ikonet.
4. I **Merknad**-feltet skriver du hva som helst, for eksempel "Dette er en hasteordre".
5. Velg **OK**-knappen.

Merknaden er nå knyttet til ordren.

## <a name="see-also"></a>Se også  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Inngående dokumenter](across-income-documents.md)  
[Konfigurere arbeidsflytvarsler](across-setting-up-workflow-notifications.md)  
