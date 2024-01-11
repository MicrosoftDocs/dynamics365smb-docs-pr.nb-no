---
title: Innføring i Contoso Coffee-prosjektstyring
description: Denne artikkelen gir deg en innføring i demonstrasjonsdataene Consoso Coffee for jobber og prosjektledelse.
author: andreipanko
ms.author: andreipa
ms.topic: how-to
ms.date: 05/31/2023
ms.custom: bap-template
---

# Innføring i Contoso Coffee-jobber og -prosjektstyring

Contoso Coffee er et fiktivt selskap som produserer forbrukerkaffemaskiner og kommersielle kaffemaskiner. **Contoso Coffee**-appene for Business Central legger til demonstrasjonsdata som du kan bruke til å lære hvordan du bruker jobb- og prosjektstyringsfunksjonene i Business Central.

Denne appen inneholder flere elementer som brukes til hovedgjennomgangene:

- Ressurser med tilordnede ferdigheter og soner
- Varer som er konfigurert til å opprette servicevarer

> [!IMPORTANT]
> Før du kjører noen av scenarioene for Contoso Coffee, må du bokføre eventuelle varekladdelinjer med åpningssaldoer. Hvis du vil ha flere krav, kan du se [Konfigurer Contoso Coffee-data](#set-up-contoso-coffee-jobs-and-project-management-data).
>
> 
## Sette opp Contoso Coffee-jobber og prosjektstyringsdata

[!INCLUDE [contoso-coffee-app-install](../contoso-coffee-app-install.md)].

Når de relevante appene er installert, går du til [Prosjektdemodata for Contoso Coffee](https://businesscentral.dynamics.com/?page=4767)-siden i [!INCLUDE [prod_short](../../includes/prod_short.md)] og endrer standardinnstillingene etter behov. Tabellene nedenfor beskriver innstillingene:  

|Felt  |Beskrivelse  |
|---------|---------|
|**Startår** |Angir det første året du vil bruke for Contoso Coffee-demondataene. Året er enten et kalenderår eller et regnskapsår, avhengig av firmaoppsettet.|
|**Kundenr.**  |Kunden som skal brukes i scenarioer i salgsoperasjoner.|
|**Vare 1 nr.**  |Tilleggsvaren som skal brukes for kontraktscenarioene.|
|**Vare 2 nr.**  |Varen som skal brukes for ødelagt-reparer-scenarioene.|
|**Lokal ressurs 1 nr.**  |Ressursen som skal brukes for kontraktscenarioene.|
|**Ekstern ressurs 1 nr.**  |Ressursen som skal brukes for ødelagt-reparer-scenarioene.|
|**Bokføringsgruppe - kunde**|Angir en firmakode for innenlandske kunder. Firmakodene brukes når transaksjoner bokføres. |
|**Kunde – generell firmabokføringsgrupper**|Angir en firmakode for innenlandske kunder. Firmakodene brukes når transaksjoner bokføres. |
|**Innenlands – generell firmabokføringsgrupper**|Angir en firmakode for innenlandske kunder og leverandører. Firmakodene brukes når transaksjoner bokføres. |
|**Videresalg – lagerbokføringsgruppe**    |Angir en kode for varer som må brukes for bokføring av videresalg.|
|**Detalj – generell varebokføringsgruppe**    |Angir en kode for varer som må brukes for bokføring av detaljhandel.|
|**Mva-bokføringsgruppe - vare**    |Angir en mva-produktkode for varer for bokføring av mva. hvis mva. er aktivert.|
|**Prisfaktor**     |Angir en faktor for å konvertere en pris fra USD/EUR til den lokale valutaen. *1* betyr at prisen er det samme beløpet i hvilken som helst valuta. Et høyere nummer brukes til å hente prisen i lokal valuta. |
|**Avrundingspresisjon**  |Definerer hvordan beregnet forbruksantall avrundes når de er angitt på forbrukskladdelinjer. Antall som er mindre enn 0,5 vil bli rundet ned. Antall som er større eller lik 0,5 vil bli rundet opp.|

Når du er klar, velger du **Opprett demonstrasjonsdata**-handling. Det tar noen minutter å legge til dataene i den underliggende databasen, men da er du klar til å kjøre de ulike scenarioene.  

## Se også
