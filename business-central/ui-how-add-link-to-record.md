---
title: 'Legge til vedlegg, koblinger og merknader i poster'
description: 'Legg til en hyperkobling i et dokument eller et nettsted til en bestemt post, for eksempel en kunde eller et dokument.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: how-to
ms.date: 09/15/2023
ms.custom: bap-template
ms-service: dynamics365-business-central
---
# <a name="manage-attachments-links-and-notes-on-cards-and-documents"></a>Behandle vedlegg, koblinger og notater på kort og dokumenter

På de fleste listesider, kort og dokumenter kan du legge ved filer, legge til koblinger og skrive merknader på fanen **Vedlegg** i ruten **Faktaboks**. Nummeret bak fanetittelen angir hvor mange vedlagte filer, koblinger eller merknader som finnes for kortet eller dokumentet.

På hurtigfanen **Linjer** kan du også bruke handlingen **Vedlegg** til å knytte dokumenter til en bestemt linje. Det kan for eksempel hende at du vil knytte utformingsspesifikasjonene til en vare på en kjøpsfaktura.

Vedlegg, koblinger og notater forblir tilknyttet kortet eller dokumentet mens det behandles i andre tilstander. Det kan for eksempel være fra en pågående ordre til en bokført salgsfaktura. Ingen av vedleggstypene blir imidlertid skrevet ut fra systemet, for eksempel ved utskrift eller lagring til en fil.

Du kan også legge til vedlegg i e-postmeldingene du sender fra [!INCLUDE [prod_short](includes/prod_short.md)]. Når du sender en e-postmelding direkte fra et dokument, for eksempel et tilbud, lar handlingen **Legg til fil fra kildedokument** deg velge filer som er knyttet til det. Du kan bare velge filer som er knyttet til dokumentet. Du kan ikke velge filer som er knyttet til linjer.

> [!NOTE]
> Når du delvis sender og fakturerer en salgsordre eller bestilling, blir vedlegget bare knyttet til den endelige fakturaen for ordren. Når du på samme måte fakturerer ved hjelp av periodisering, knyttes vedlegget til finanspostene for bilaget, men ikke for periodiseringspostene.
>
> Hvis du sletter en ordre før den faktureres, fjernes også vedlegget.
>
> Når du bruker handlingen **Hent mottakslinjer** på en kjøpsfaktura, blir vedlegget på den relaterte bestillingen lagt til i kjøpsfakturaen.

## <a name="to-attach-a-file-to-a-purchase-invoice"></a>Knytte en fil til en kjøpsfaktura

Du kan legge ved alle typer filer, som tekst, bilder eller videofiler, i et kort, et dokument eller en linje i et dokument. Dette er for eksempel nyttig når du vil lagre fakturaen for en leverandør som en PDF-fil på den relaterte kjøpsfakturaen i [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]
> Filer som er knyttet til funksjonen for innkommende dokumenter, tas ikke med i fanen **Vedlegg**. Se [Innkommende dokumenter](across-income-documents.md) for mer informasjon. Dette gjelder filer som er knyttet til linjer i dokumenter.

Følgende fremgangsmåte er basert på en kjøpsfaktura. Trinnene er lignende for alle andre støttede dokumenter og kort.

> [!TIP]
> Hvis vedlegget er spesifikt for en linje i et dokument, kan du knytte det til linjen. Velg linjen og velg deretter handlingen **Vedlegg**.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Kjøpsfakturaer**, og velg deretter den relaterte koblingen.
2. Åpne kjøpsfakturaen som du vil legge til en fil i.
3. Åpne fanen **Vedlegg** i ruten **Faktaboks**.
4. Velg verdien bak feltet **Dokumenter**, for eksempel 0.
5. På siden **Vedlagte dokumenter**, i feltet **Vedlegg**.
6. I dialogboksen **Tilknytt et dokument** gjør du ett av følgende for å legge ved en fil:

   [!INCLUDE[file-upload](includes/file-upload.md)]

Filen er nå knyttet til kjøpsfakturaen.

## <a name="to-view-an-attached-file"></a>Slik ser du en vedlagt fil

1. Åpne fanen **Vedlegg** i faktaboksen.
2. Velg verdien bak feltet **Dokumenter**, for eksempel 1.
3. På siden **Vedlagte dokumenter** velger du handlingen **Forhåndsvis**.
4. Åpne den nedlastede filen.

## <a name="to-save-a-document-as-a-pdf-attachment"></a>Slik lagrer du et dokument som et PDF-vedlegg

Når du skal lagre et dokument som en fil, kan du bruke handlingen **Legg ved som PDF** til å lagre gjeldende dokumentinnhold som en PDF-fil som er knyttet til faktaboksen for dokumentet. Dette er for eksempel nyttig når dokumenter følger flere trinn i en prosess, for eksempel en salgsprosess eller en godkjenningsarbeidsflyt, og du vil referere til en utskrift av forrige trinn.

Følgende fremgangsmåte er basert på en ordre. Trinnene er de samme for alle støttede dokumenter.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Ordrer**, og velg deretter den relaterte koblingen.
2. Velg en ordre, og velg deretter handlingen **Legg ved som PDF**.

En PDF-fil med gjeldende ordreinnhold legges til i fanen **Vedlegg** i faktaboksen.

## <a name="to-add-a-link-from-an-item-card"></a>Legge til en kobling fra varekortet

Du kan legge til en kobling fra et kort eller et dokument i en hvilken som helst URL-adresse. Dette er nyttig når du for eksempel vil knytte et varekort til leverandørens varekatalog.

Følgende fremgangsmåte er basert på et varekort. Trinnene er lignende for alle andre støttede kort og dokumenter.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Varer** og velg den relaterte koblingen.
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

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Ordrer**, og velg deretter den relaterte koblingen.
2. Velg ordren du vil skrive en merknad på, og velg deretter kategorien **Vedlegg** i faktaboksen.
3. I delen **Merknader** velger du **+**-ikonet.
4. I **Merknad**-feltet skriver du hva som helst, for eksempel "Dette er en hasteordre".
5. Velg **OK**-knappen.

Merknaden er nå knyttet til ordren.

## <a name="see-also"></a>Se også
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Inngående dokumenter](across-income-documents.md)  
[Konfigurer arbeidsflytvarsler](across-setting-up-workflow-notifications.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
