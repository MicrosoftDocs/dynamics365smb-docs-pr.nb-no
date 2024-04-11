---
title: Definer aktiva
description: 'Få informasjon om sekvensen av oppgaver du må gjøre for å definere aktiva, for eksempel maskiner eller bygninger.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.search.keywords: 'machinery, buildings'
ms.search.form: '5607,'
ms.date: 03/25/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Definer aktiva

Før du kan arbeide med aktiva, må du definere et par ting:  

* hvordan du avskriver aktiva  
* hvordan du registrerer anskaffelseskostnader, avskrivinger og andre verdier i finans  
* eventuelt hvordan du registrerer forsikring og vedlikehold på aktiva

Avsnittene i denne artikkelen inneholder flere opplysninger om hvordan du definerer aktiva. Når du er ferdig med oppsettet, kan du begynne å arbeide med aktiva. Hvis du vil ha mer informasjon, kan du se [Bruk aktiva](fa-manage.md).  

> [!NOTE]  
> Du kan registrere aktivatransaksjoner på siden **Aktivafinanskladd** eller **Aktivakladd**, avhengig av om transaksjonene er for finansrapportering eller intern håndtering. Hjelpartikkelen for aktiva beskriver bare hvordan du bruker siden **Aktiva finanskladd**.  

Når du aktiverer et aktiva i delen **Finansintegrasjon** på siden **Avskrivningstablåkort**, brukes siden **Aktivafinanskladd** til å bokføre transaksjoner for aktiviteten.

## Obligatoriske oppsettsoppgaver

Tabellen nedenfor inneholder en rekke oppgaver for å definere aktiva og koblinger til relaterte artikler.

| Til | Se |
|---|---|
| Definer standard finanskonti, fordelingsnøkler, kladdemaler og kladder for aktivabokføring, og definer aktivaklasser og underklasser, for eksempel materielle og immaterielle. |[Definere generell aktivainformasjon](fa-how-setup-general.md) |
| Opprette avskrivningstablåer, definere diverse avskrivningsmetoder, integrere med Finans, og gjøre det mulig å duplisere poster i flere avskrivningstablåer. |[Konfigurer aktivumavskrivninger](fa-how-setup-depreciation.md) |

## Valgfrie oppsettsoppgaver (forsikring, vedlikehold og brukerdefinerte avskrivningsmetoder)

Tabellen nedenfor inneholder en rekke valgfrie oppgaver for å definere aktiva, for eksempel metoder for forsikring, vedlikehold og avskriving til relaterte artikler. 

| Til | Se |
|---|---|
| Aktivere forsikring av aktiva, definere generelle forsikringsopplysninger, et forsikringskort per polise, og forberede kladder for bokføring av forsikringskostnader. |[Definere aktivaforsikring](fa-how-setup-insurance.md) |
| Aktivere vedlikehold av aktiva, definere generell vedlikeholdsinformasjon, definere kontoer for postering av vedlikehold, og definere typer av vedlikeholdsarbeid. |[Konfigurer aktivumvedlikehold](fa-how-setup-maintenance.md) |
| Lær mer om hvordan du bruker avskrivningsmetoder. |[Konfigurer brukerdefinerte avskrivningsmetoder](fa-how-setup-user-defined-depreciation-method.md) |

## Se også

[Oversikt over aktiva](fa-manage.md)  
[Finans](finance.md)  
[Bli klar til å gjøre forretninger](ui-get-ready-business.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
