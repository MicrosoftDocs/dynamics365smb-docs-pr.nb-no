---
title: Designdetaljer – Varesporing og reservasjoner | Microsoft-dokumentasjon
description: Dette emnet handler om varesporing og reservasjoner og beskriver konseptene bak to.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: bfa2706b4d6d44a6f565685a66668c336b7a20e3
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3185111"
---
# <a name="design-details-item-tracking-and-reservations"></a>Designdetaljer: Varesporing og reservasjoner
Samtidig bruk av reservasjon og bestemt varesporing er uvanlig, fordi begge oppretter en kobling mellom forsyning og behov. Med unntak av tilfeller der en kunde- eller produksjonsplanlegger ber om et bestemt parti, er det sjelden fornuftig å reservere lagervarer som allerede har varesporingsnumre for et bestemt utligning. Selv om det er mulig å reservere varer som krever en bestemt varesporing, kreves det spesialfunksjoner for å unngå tilgjengelighetskonflikter mellom ordrebehandlere som krever de samme varesporede varene.  
  
Begrepet om sen binding sikrer at en ikke-spesifikk reservasjon av et serienummer eller partinummer holdes løst koblet før bokføring. På bokføringstidspunktet kan reservasjonssystemet stokke om på ikke-spesifikke reservasjoner for å sikre at fast utligning er mulig mot serie- eller partinummeret som faktisk plukkes. I mellomtiden gjøres serie- eller partinumre tilgjengelige for bestemte reservasjon i andre dokumenter som krever det bestemte serie- eller partinummeret.  
  
En ikke-spesifikk reservasjon er en reservasjon der brukeren ikke bryr deg om hvilken bestemt vare som velges, og en spesifikk reservasjon er en reservasjon der brukeren bryr seg.  
  
> [!NOTE]  
>  Funksjonen for sen binding gjelder bare for varer som er definert med spesifikk varesporing, og den gjelder bare for reservasjoner mot lager, ikke mot inngående forsyningsordrer.  
  
Reservasjon av varesporingsnumre faller innenfor to kategorier, som vist i tabellen nedenfor.  
  
|Reservasjon|Beskrivelse|  
|-----------------|---------------------------------------|  
|Serienummer|Du velger et bestemt serie- eller partinummer når du reserverer lagervaren fra et behov, for eksempel en ordre.<br /><br /> Dette er en vanlig reservasjon. Det er en streng kobling mellom forsyning og behov som begge har serie- eller partinummer. **Obs!** Behovet har serie- eller partinumre. <br /><br /> Du vil for eksempel reservere et spann med blå maling fra parti A fordi kunden ber om det. Et spann med blå maling fra serie A leveres til kunden.|  
|Ikke-spesifikk|Du velger ikke et bestemt serie- eller partinummer når du reserverer lagervaren fra et behov, for eksempel en ordre.<br /><br /> Dette er en tilstand som en reservasjonspost pålegges for serie- eller partinumre som ikke spesifikt velges. **Obs!** Behovet har ikke serie- eller partinumre. <br /><br /> Hvis du for eksempel vil reservere et spann med blå maling fra et hvilket som helst parti for ordren. Et spann med blå maling fra en tilfeldig serie- eller partinummer leveres til kunden.|  
  
Hovedforskjellen på spesifikk og ikke-spesifikk reservasjon angis av serie- eller partinumre som finnes på behovssiden, som vist i følgende tabell.  
  
||||  
|-|-|-|  
||**Forsyning**|**Behov**|  
|**Serienummer**|Serie- eller partinummer.|Serie- eller partinummer.|  
|**Ikke-spesifikk**|Serie- eller partinummer.|Ingen serie- eller partinumre.|  
  
Når du reserverer lagerantall fra en linje i et utgående dokument for en vare som har fått tilordnet varesporingsnumre, og er opprettet for spesifikk varesporing, blir du ledet gjennom ulike arbeidsflyter på **Reservasjon**-siden, avhengig av behovet for serie- eller partinumrene.  
  
## <a name="specific-reservation"></a>Spesifikk reservasjon  
Når du velger **Reserver** på linjen i det utgående dokumentet, vises en dialogboks der du blir spurt om du vil reservere bestemte serie- eller partinumre. Hvis du velger **Ja**, vil det vises en liste med alle serie- eller partinumrene som er tilordnet til dokumentlinjen. Siden **Reservasjon** åpnes når du har valg et av serie- eller partinumrene, og deretter kan du reservere blant de valgte serie- eller partinumrene på vanlig måte.  
  
Hvis noen av de spesifikke varesporingsnumre som du prøver å reservere holdes i ikke-spesifikke reservasjoner, vil en melding nederst på siden **Reservasjon** informere deg om hvor mange av totalt reservert antall som holdes i ikke-spesifikke reservasjoner og om de fremdeles er tilgjengelige.  
  
## <a name="nonspecific-reservation"></a>Ikke-spesifikk reservasjon  
Hvis du velger **Ingen** i dialogboksen som vises, åpnes siden **Reservasjon**, og dette lar deg reservere blant alle serie- eller partinumre i lageret.  
  
På grunn av strukturen i reservasjonssystemet må systemet velge bestemte vareposter å reservere mot, når du plasserer en uspesifisert reservasjon på en varesporet vare. Siden varepostene inneholder varesporingsnumrene, reserverer reservasjonen indirekte bestemte serie- eller partinumre, selv om du ikke hadde tenkt å gjøre dette. For å håndtere denne situasjonen prøver reservasjonssystemet å stokke om ikke-spesifikke reservasjonsposter før bokføring.  
  
Systemet reserverer faktisk fortsatt mot bestemte poster, men deretter bruker det en omstokkingsmekanisme når det er et bestemt behov for parti- eller serienummeret i den ikke-spesifikke reservasjonen. Dette kan være tilfellet når du bokfører en behovstransaksjon, for eksempel en ordre, forbrukskladd eller overføringsordre, for serie- eller partinummeret, eller når du prøver spesifikt å reservere serie- eller partinummer. Systemet stokker om reservasjoner for å gjøre parti- eller serienummeret tilgjengelig for behovet eller den bestemte reservasjonen, og plasserer dermed et annet parti- eller serienummer i den ikke-spesifikke reservasjonen. Hvis det er utilstrekkelig antall på lager, stokker systemet om på så mye som mulig, og du får feilmeldingen om tilgjengelighet hvis det fortsatt ikke er tilstrekkelig antall på bokføringstidspunktet.  
  
> [!NOTE]  
>  Parti- eller serienummerfeltet er tomt i reservasjonsposten i en ikke-spesifikk reservasjon, som peker på behovet, for eksempel salget.  
  
## <a name="reshuffle"></a>Stokke om  
Når en bruker bokfører et utgående dokument etter å ha plukket feil serie- eller partinummer, blir andre ikke-spesifikke reservasjoner stokket om for å gjenspeile det faktiske serie- eller partinummeret som er plukket. Dette tilfredsstiller bokføringsmotoren med en fast utligning mellom forsyning og behov.  
  
For alle støttede forretningsscenarier er omstokking bare mulig mot positive vareposter som inneholder reservasjons og serie-/partinumre, men uten definert serie-/partinumre på behovssiden.  
  
## <a name="supported-business-scenarios"></a>Forretningsscenarier som støttes  
Funksjonen for sen binding støtter følgende forretningsscenarier:  
  
* Angi et bestemte serie- eller partinummer for et utgående dokument med ikke-spesifikk reservasjon av feil serie- eller partinummer.  
* Reservere et spesifikt serie- eller partinummer.  
* Bokføre et utgående dokument med ikke-spesifikk reservasjon av serie- eller partinummer.  
  
### <a name="entering-serial-or-lot-numbers-on-an-outbound-document-with-wrong-nonspecific-reservation"></a>Angi serie- eller partinumre på et utgående dokument med feil ikke-spesifikk reservasjon  
Dette er det vanligste av de tre scenariene som støttes. I slike tilfeller vil funksjonen for sen sikre at en bruker kan angi et serie- eller partinummer, som faktisk er plukket, på et utgående dokument som allerede har en ikke-spesifikk reservasjon på et annet serie- eller partinummer.  
  
Behovet oppstår for eksempel når en ordrebehandler har foretatt en ikke-spesifikk reservasjon av et serie- eller partinummer. Senere, når varen faktisk plukkes fra lager, må det plukkede serie- eller partinummeret angis på ordren før den bokføres. Den ikke-spesifikke reservasjonen stokkes om ved bokføring for å sikre at det plukkede serie- eller partinummeret kan registreres uten at reservasjonen går tapt, og for å sikre at det plukkede serie- eller partinummeret kan utlignes og bokføres fullstendig.  
  
### <a name="reserve-specific-serial-or-lot-numbers"></a>Reservere spesifikke serie- eller partinumre  
I dette forretningsscenariet vil funksjonen for sen binding sikre at en bruker som prøver å reservere et bestemt serie- eller partinummer som er ikke reservert for øyeblikket, kan gjøre dette. En ikke-spesifikk reservasjon stokkes om på tidspunktet for reservasjonen for å frigjøre serie- eller partinummer for den bestemte forespørselen.  
  
Omstokkingen skjer automatisk, men innebygd Hjelp vises nederst på **Reservasjon**-siden og inneholder følgende tekst:  
  
**XX av totalt reservert antall er ikke-spesifikt og kan være disponibelt.**  
  
I tillegg vil feltet **Ikke-spesifikt reservert antall** vise hvor mange reservasjonsposter som er ikke-spesifikke. Dette feltet er ikke synlige for brukerne som standard.  
  
### <a name="posting-an-outbound-document-with-nonspecific-reservation-of-serial-or-lot-numbers"></a>Bokføre et utgående dokument med ikke-spesifikk reservasjon av serie- eller portnumre.  
Dette forretningsscenariet støttes med funksjonen for sen binding som gjør det mulig å foreta fast utligning og utgående bokføring av det som faktisk plukkes, ved å stokke om en annen ikke-spesifikk reservasjon av et serie- eller partinummer. Hvis det ikke er mulig å stokke om, vises følgende standardfeilmelding når brukeren prøver å bokføre leveringen:  
  
**Vare XX kan ikke utlignes fullstendig.**  
  
## <a name="see-also"></a>Se også  
[Designdetaljer: Varesporing](design-details-item-tracking.md)