---
author: edupont04
ms.service: dynamics365-accountant
ms.topic: include
ms.date: 10/02/2020
ms.author: edupont
ms.openlocfilehash: 1b9f60eab5b0bcf812343e82389087ac5535301a
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4749783"
---
Før du kan opprette e-postpålogging må du klargjøre Exchange Online med [fellesmapper](/exchange/collaboration/public-folders/public-folders?view=exchserver-2019&preserve-view=true ). Du kan gjøre dette i [Administrasjonssenter for Exchange](/Exchange/architecture/client-access/exchange-admin-center?view=exchserver-2019&preserve-view=true ), eller du kan bruke [Exchange Management Shell](/powershell/exchange/exchange-management-shell?view=exchange-ps&preserve-view=true ).  

> [!TIP]
> Hvis du vil bruke [Exchange Management Shell](/powershell/exchange/exchange-management-shell?view=exchange-ps&preserve-view=true ), kan du finne inspirasjon for hvordan du konfigurerer skriptet i et eksempelskript som vi publiserte i [BCTech repo](https://github.com/microsoft/BCTech/tree/master/samples/EmailLogging).

Listen nedenfor beskriver de viktigste trinnene med koblinger for å finne ut mer.  

- Opprett en administratorrolle for fellesmapper basert på informasjonen i følgende tabell:

  |Egenskap        |Verdi                     |
  |----------------|--------------------------|
  |Name            |Administrasjon av fellesmapper |
  |Valgte roller  |Fellesmapper            |
  |Valgte medlemmer|E-postadressen til brukerkontoen som Business Central bruker til å kjøre loggføringsjobben for e-post|

  Hvis du vil ha mer informasjon, kan du se [Administrere rollegrupper](/exchange/permissions/role-groups?view=exchserver-2019&preserve-view=true).

- Opprett en ny postboks for fellesmapper basert på informasjonen i følgende tabell:

  |Egenskap        |Verdi                     |
  |----------------|--------------------------|
  |Name            |Fellespostboks            |

  Hvis du vil ha mer informasjon, kan du se [Opprette en postboks for fellesmapper i Exchange Server](/exchange/collaboration/public-folders/create-public-folder-mailboxes).  

- Opprette nye fellesmapper

  - Opprett en ny fellesmappe med navnet *Loggføring av e-post* i roten, slik at hele banen til mappen blir ```\Email Logging\```
  - Opprett to undermapper slik at resultatet er følgende fullstendige baner til mappene:
    - ```\Email Logging\Queue\```
    - ```\Email Logging\Storage\```

  Hvis du vil ha mer informasjon, kan du se [Opprette en fellesmappe](/exchange/collaboration/public-folders/create-public-folders?view=exchserver-2019&preserve-view=true).

- Aktiver e-post for fellesmappen *Kø*

  Hvis du vil ha mer informasjon, kan du se [Aktivere eller deaktivere e-post for en fellesmappe](/exchange/collaboration/public-folders/mail-enable-or-disable?view=exchserver-2019&preserve-view=true)

- Aktivere e-post for å sende e-post til fellesmappen *Kø* ved bruk av Outlook eller Exchange Management Shell

  Hvis du vil ha mer informasjon, kan du se [Tillat at anonyme brukere kan sende e-post til en fellesmappe som e-post er aktivert for](/exchange/collaboration/public-folders/mail-enable-or-disable#allow-anonymous-users-to-send-email-to-a-mail-enabled-public-folder?view=exchserver-2019&preserve-view=true)

- Angi brukeren for loggføring av e-post som eier av fellesmappene *Kø* og *Lagring* ved hjelp av Outlook eller Exchange Management Shell, basert på informasjonen i følgende tabell:

  |Egenskap        |Verdi                     |
  |----------------|--------------------------|
  |Bruker            |E-postadressen til brukerkontoen som Business Central bruker til å kjøre loggføringsjobben for e-post|
  |Tillatelsesnivå|Eier                     |

  Hvis du vil ha mer informasjon, kan du se [Tilordne tillatelser til fellesmapper](/exchange/collaboration-exo/public-folders/set-up-public-folders#step-3-assign-permissions-to-the-public-folder).

- Opprett to nye regler for e-postflyt basert på informasjonen i følgende tabell:

  |Formål  |Name |Betingelser                        |Handling                                       |
  |---------|-----|----------------------------------|---------------------------------------------|
  |Regel for innkommende e-post |Logge e-post sendt til denne organisasjonen|*Avsenderen* befinner seg *utenfor organisasjonen*, og *mottakeren* befinner seg *i organisasjonen*|Sende blindkopi til e-postkontoen som er angitt for fellesmappen *Kø*|
  |Regel for utgående e-post | Logge e-post sendt fra denne organisasjonen |*Avsenderen* befinner seg *i organisasjonen*, og *mottakeren* befinner seg *utenfor organisasjonen*|Sende blindkopi til e-postkontoen som er angitt for fellesmappen *Kø*|
  
  Hvis du vil ha mer informasjon, kan du se [Administrere regler for e-postflyt i Exchange Online](/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules) og [Regelhandlinger for e-postflyt i Exchange Online](/exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions).

> [!NOTE]
> Hvis du utfører endringer i Exchange Management Shell, blir endringene synlige i Administrasjonssenter for Exchange etter en forsinkelse. Endringene som er gjort i Exchange, vil også være tilgjengelige i [!INCLUDE[prod_short](prod_short.md)] etter en forsinkelse.
