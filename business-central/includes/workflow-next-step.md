---
author: brentholtorf
ms.topic: include
ms.date: 03/27/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

> [!IMPORTANT]
> Når du endrer når-hendelsen for et arbeidsflyttrinn, endres også så-svarene. Noen ganger refererer så-svar fra andre når-hendelser til disse så-svarene som neste trinn i arbeidsflyten. Når du har endret en når-hendelse, må du kontrollere at de neste trinnene for så-hendelsene er riktige.  
>
> Arbeidsflytmalen **Arbeidsflyt for godkjenning av leverandør** har for eksempel en primær når-hendelse: **Det bes om godkjenning av en leverandør**. Denne når-hendelsen har en så-hendelse: **Send godkjenningsforespørsler for posten, og opprett et varsel**, som andre så-hendelser refererer til. Hvis du endrer den primære når-hendelsen, **Det bes om godkjenning av en leverandør**, til for eksempel **En leverandørpost endres**, fjernes så-svaret sammen med referansene.
>
> Så-svarene for når-hendelsene **En godkjenningsforespørsel er delegert** og **En godkjenningsforespørsel er godkjent** (med **Ved betingelse** av typen **Ventende godkjenninger >0**) er eksempler på tilfeller der endring av en primær når-hendelse kan forårsake problemer. Så-svarene har et neste trinn som refererer til så-svaret **Send godkjenningsforespørsler for posten, og opprett et varsel** for når-hendelsen **Det bes om godkjenning av en leverandør**. Fordi så-svaret for når-hendelsen **Det bes om godkjenning av en leverandør** ikke lenger er tilgjengelig, vil de innrykkede når-hendelsene ikke fungere som forventet.
>
> Du må angi de neste trinnene for så-svarene for når-hendelsene som refererte til den endrede når-hendelsen.