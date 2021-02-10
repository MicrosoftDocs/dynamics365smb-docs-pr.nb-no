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
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 0d13ffa03e4a123158e2f350ff9eab5e274741b5
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4760570"
---
# <a name="manage-attachments-links-and-notes-on-cards-and-documents"></a>Behandle vedlegg, koblinger og merknader på kort og dokumenter

I faktaboksen på de fleste kort og dokumenter kan du legge ved filer, legge til koblinger og skrive merknader. For koblinger og merknader kan du også gjøre dette på listesiden ved først å merke den tilknyttede linjen.

Hvis du vil vise eller endre noen av disse vedlagte informasjonstypene, må du først åpne **Vedlegg**-kategorien i faktaboksen. Nummeret bak kategoritittelen angir hvor mange vedlagte filer, koblinger eller merknader som finnes for kortet eller dokumentet.

Vedlegg, koblinger og merknader forblir tilknyttet når kortet eller dokumentet behandles i andre statuser, for eksempel fra en pågående ordre til en bokført salgsfaktura. Ingen av vedleggstypene blir imidlertid skrevet ut fra systemet, for eksempel ved utskrift eller lagring til en fil.

> [!NOTE]
> Når du delvis sender og fakturerer en ordre eller bestilling, blir vedlegget bare knyttet til den endelige fakturaen for den ordren. På samme måte, når du fakturerer ved hjelp av Periodiseringer-funksjonen, knyttes vedlegget bare til finanspostene for bilaget, men ikke for periodiseringspostene.

## <a name="to-attach-a-file-to-a-purchase-invoice"></a>Knytte en fil til en kjøpsfaktura
Du kan legge ved alle typer filer, som inneholder tekst, bilder eller video, i et kort eller dokument. Dette er for eksempel nyttig når du vil lagre fakturaen for en leverandør som en PDF-fil på den relaterte kjøpsfakturaen i [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]
> Filer som er knyttet til funksjonen for innkommende dokumenter, tas ikke med i kategorien **Vedlegg**. Se [Innkommende dokumenter](across-income-documents.md) for mer informasjon.

Følgende fremgangsmåte er basert på en kjøpsfaktura. Trinnene er lignende for alle andre støttede dokumenter og kort.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kjøpsfakturaer**, og velg deretter den relaterte koblingen.
2. Åpne salgsordren som du vil legge til en fil i.
3. Åpne fanen **Vedlegg** i faktaboksen.
4. Velg verdien bak feltet **Dokumenter**, for eksempel 0.
5. På **Vedlagte dokumenter**-siden i **Vedlegg**-feltet velger du **Velg fil**-handlingen.
5. Velg en fil fra en hvilken som helst plassering, og velg deretter **Åpne**-knappen.

Filen er nå knyttet til kjøpsfakturaen.

## <a name="to-view-an-attached-file"></a>Slik ser du en vedlagt fil
1. Åpne fanen **Vedlegg** i faktaboksen.
2. Velg verdien bak feltet **Dokumenter**, for eksempel 1.
3. På siden **Vedlagte dokumenter** velger du handlingen **Forhåndsvis**.
4. Åpne den nedlastede filen.

## <a name="to-save-a-document-as-a-pdf-attachment"></a>Slik lagrer du et dokument som et PDF-vedlegg
Når du skal lagre et dokument som en fil, kan du bruke handlingen **Legg ved som PDF** til å lagre gjeldende dokumentinnhold som en PDF-fil som er knyttet til faktaboksen for dokumentet. Dette er for eksempel nyttig når dokumenter følger flere trinn i en prosess, for eksempel en salgsprosess eller en godkjenningsarbeidsflyt, og du vil referere til en utskrift av forrige trinn.

Følgende fremgangsmåte er basert på en ordre. Trinnene er de samme for alle støttede dokumenter.

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Ordrer**, og velg deretter den relaterte koblingen.
2. Velg en ordre, og velg deretter handlingen **Legg ved som PDF**.

En PDF-fil med gjeldende ordreinnhold legges til i fanen **Vedlegg** i faktaboksen.

## <a name="to-add-a-link-from-an-item-card"></a>Legge til en kobling fra varekortet
Du kan legge til en kobling fra et kort eller et dokument i en hvilken som helst URL-adresse eller bane. Dette er nyttig når du for eksempel vil knytte et varekort til leverandørens varekatalog.

Følgende fremgangsmåte er basert på et varekort. Trinnene er lignende for alle andre støttede kort og dokumenter.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Varer**, og velg deretter den relaterte koblingen.
2. Velg varen du vil legge til en kobling fra, og velg deretter kategorien **Vedlegg** i faktaboksen.
3. I **Koblinger** velger du **+**-ikonet.
4. I vinduet **Koblingsadresse** angir du koblingen.

    Koblingen må være en gyldig URL-adresse for Internett eller intranett.

5. I **Beskrivelse**-feltet angir du informasjon om koblingen.  
6. Velg **OK**-knappen.

Koblingen er nå knyttet til varekortet.  

## <a name="to-write-a-note-on-a-sales-order"></a>Skrive en merknad på en ordre
Du kan skrive et notat på et dokument eller kort, for eksempel for å formidle spesielle instruksjoner til andre brukere av dokumentet eller kortet. Du kan inkludere filkoblinger og URL-adresser i notater.

> [!NOTE]
> Merknader i kategorien **Vedlegg** er ikke knyttet til interne notatfunksjoner, som hovedsakelig brukes til å kommunisere mellom arbeidsflytbrukere. Hvis du vil ha mer informasjon, kan du se [Konfigurere arbeidsflytvarsler](across-setting-up-workflow-notifications.md).

Følgende fremgangsmåte er basert på en ordre. Trinnene er lignende for alle andre støttede dokumenter og kort.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Ordrer**, og velg deretter den relaterte koblingen.
2. Velg ordren du vil skrive en merknad på, og velg deretter kategorien **Vedlegg** i faktaboksen.
3. I delen **Merknader** velger du **+**-ikonet.
4. I **Merknad**-feltet skriver du hva som helst, for eksempel "Dette er en hasteordre".
5. Velg **OK**-knappen.

Merknaden er nå knyttet til ordren.

## <a name="see-also"></a>Se også  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Inngående dokumenter](across-income-documents.md)  
[Konfigurere arbeidsflytvarsler](across-setting-up-workflow-notifications.md)  
