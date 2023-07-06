---
author: edupont04
ms.topic: include
ms.date: 02/15/2022
ms.author: edupont
---

> [!NOTE]
> Delene nedenfor forutsetter at du har administratortilgang for Exchange Online.

Før du kan opprette e-postpålogging må du klargjøre Office 365 med [fellesmapper](/exchange/collaboration-exo/public-folders/public-folders). Du kan gjøre dette i [Administrasjonssenter for Exchange](/exchange/exchange-admin-center?preserve-view=true), eller du kan bruke [Exchange Online PowerShell](/powershell/exchange/exchange-online-powershell?view=exchange-ps&?preserve-view=true).

> [!TIP]
> Hvis du vil bruke [Exchange Online PowerShell](/powershell/exchange/exchange-online-powershell?view=exchange-ps&preserve-view=true), kan du finne inspirasjon for hvordan du konfigurerer skriptet i et eksempelskript som vi publiserte i [BCTech repo](https://github.com/microsoft/BCTech/tree/master/samples/EmailLogging).

Følg fremgangsmåten nedenfor for å konfigurere Exchange Online, med koblinger til der du kan finne ut mer.

### <a name="create-an-admin-role-group"></a><a name="create-an-admin-role-group"></a><a name="create-an-admin-role-group"></a>Opprett en administratorrollegruppe

Opprett en administratorrollegruppe for fellesmapper basert på informasjonen i følgende tabell:

|Egenskap        |Verdi                     |
|----------------|--------------------------|
|Name            |Administrasjon av fellesmapper |
|Valgte roller  |Fellesmapper            |
|Valgte brukere  |E-postadressen til brukerkontoen som Business Central bruker til å kjøre loggføringsjobben for e-post|

Hvis du vil ha mer informasjon, kan du se [Administrer rollegrupper i Exchange Online](/exchange/permissions-exo/role-groups).

### <a name="create-a-new-public-folder-mailbox"></a><a name="create-a-new-public-folder-mailbox"></a><a name="create-a-new-public-folder-mailbox"></a>Opprett en ny postboks for fellesmapper

Opprett en ny postboks for fellesmapper basert på informasjonen i følgende tabell:

|Egenskap        |Verdi                     |
|----------------|--------------------------|
|Name            |Fellespostboks            |

Hvis du vil ha mer informasjon, kan du se [Opprette en postboks for fellesmapper](/exchange/collaboration-exo/public-folders/create-public-folder-mailbox).

### <a name="create-new-public-folders"></a><a name="create-new-public-folders"></a><a name="create-new-public-folders"></a>Opprette nye fellesmapper

1. Opprett en ny fellesmappe med navnet **Loggføring av e-post** i roten, slik at hele banen til mappen blir `\Email Logging\`.
2. Opprett to undermapper slik at resultatet er følgende fullstendige baner til mappene:

    - `\Email Logging\Queue\`
    - `\Email Logging\Storage\`

Hvis du vil ha mer informasjon, kan du se [Opprett en fellesmappe](/exchange/collaboration-exo/public-folders/create-public-folder).

### <a name="set-public-folder-ownership"></a><a name="set-public-folder-ownership"></a><a name="set-public-folder-ownership"></a>Angi eierskap for fellesmappe

Angi e-postloggingsbrukeren som eier av både fellesmapper, *Kø* og *Lagring*.

Hvis du vil ha mer informasjon, kan du se [Tilordne tillatelser til fellesmapper](/exchange/collaboration-exo/public-folders/set-up-public-folders#step-3-assign-permissions-to-the-public-folder).

### <a name="mail-enable-the-queue-public-folder"></a><a name="mail-enable-the-queue-public-folder"></a><a name="mail-enable-the-queue-public-folder"></a>Aktiver e-post for fellesmappen *Kø*

  Hvis du vil ha mer informasjon, kan du se [Aktiver eller deaktiver e-post for en fellesmappe](/exchange/collaboration-exo/public-folders/enable-or-disable-mail-for-public-folder).

### <a name="mail-enable-sending-emails-to-the-queue-public-folder"></a><a name="mail-enable-sending-emails-to-the-queue-public-folder"></a><a name="mail-enable-sending-emails-to-the-queue-public-folder"></a>Aktiver sending av e-post til fellesmappen *Kø*

Aktivere e-post for å sende e-post til fellesmappen *Kø* ved bruk av Outlook eller Exchange Management Shell.

Hvis du vil ha mer informasjon, kan du se [Tillat at anonyme brukere kan sende e-post til en fellesmappe som e-post er aktivert for](/exchange/collaboration-exo/public-folders/enable-or-disable-mail-for-public-folder#allow-anonymous-users-to-send-email-to-a-mail-enabled-public-folder?preserve-view=true).

### <a name="create-mail-flow-rules"></a><a name="create-mail-flow-rules"></a><a name="create-mail-flow-rules"></a>Opprett regler for e-postflyt

Opprett to nye regler for e-postflyt basert på informasjonen i følgende tabell:

|Formål  |Name |Bruk denne regelen hvis ...             |Gjør følgende ...                          |
|---------|-----|----------------------------------|---------------------------------------------|
|Regel for innkommende e-post |Logge e-post sendt til denne organisasjonen|*Avsenderen* befinner seg *utenfor organisasjonen*, og *mottakeren* befinner seg *i organisasjonen*|Sende blindkopi til e-postkontoen som er angitt for fellesmappen *Kø*|
|Regel for utgående e-post | Logge e-post sendt fra denne organisasjonen |*Avsenderen* befinner seg *i organisasjonen*, og *mottakeren* befinner seg *utenfor organisasjonen*|Sende blindkopi til e-postkontoen som er angitt for fellesmappen *Kø*|

Hvis du vil ha mer informasjon, kan du se [Administrer regler for e-postflyt i Exchange Online](/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules?preserve-view=true) og [Regelhandlinger for e-postflyt i Exchange Online](/exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions?preserve-view=true).

> [!NOTE]
> Hvis du utfører endringer i Exchange Management Shell, blir endringene synlige i Administrasjonssenter for Exchange etter en forsinkelse. Endringene som er gjort i Exchange, vil også være tilgjengelige i [!INCLUDE[prod_short](prod_short.md)] etter en forsinkelse. Forsinkelsen kan være på flere timer.
