---
title: Oversikt over selskapsinformasjon
description: 'Siden Selskapsopplysninger angir grunnleggende informasjon om en forretningsenhet, for eksempel navn, adresser og leveringsinformasjon.'
author: brentholtorf
ms.topic: conceptual
ms.search.form: 1
ms.date: 08/31/2022
ms.author: bholtorf
---

# Oversikt over selskapsinformasjon

[!INCLUDE[prod_short](includes/prod_short.md)] organiserer forretningsenheter i *selskaper*. For hvert selskap må du fylle ut noen av de grunnleggende selskapsdetaljene og relevant informasjon på siden **Selskapsopplysninger**. Opplysningene på siden [**Selskapsopplysninger**](https://businesscentral.dynamics.com/?page=1) brukes i dokumenter, blant annet fakturahoder. Du kan opprette mer enn ett selskap, for eksempel et morselskap og et datterselskap.  

Hvis selskapets lager befinner seg på en annen adresse enn selskapets hovedkvarter, kan du fylle ut de ulike leveringsfeltene og feltet **Lokasjonskode** i hurtigfanen **Levering**. Deretter vil informasjonen i disse feltene bli skrevet ut på for eksempel bestillinger slik at leverandørene sender varene til riktig adresse.  

For hvert selskap du konfigurerer, må du fylle ut siden **Selskapsopplysninger** sammen med siden **Finansoppsett**. Du må også definere hvert område i [!INCLUDE [prod_short](includes/prod_short.md)], for eksempel siden **Salgsoppsett** for hvert selskap. Lær mer på [Oversikt over oppgaver for å definere [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md).  

**Selskapsopplysninger**-siden inneholder forskjellige felter og hurtigfaner, avhengig av landet/området. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] Følgende tabell beskriver de mest brukte hurtigfanene.

[!INCLUDE [admin-company-info-fasttabs](includes/admin-company-info-fasttabs.md)]

Når du er ferdig med å fylle ut informasjonen, kan du lukke siden.  

## Arbeide med flere selskaper

Hvis [!INCLUDE [prod_short](includes/prod_short.md)] har flere selskaper, kan det være at brukerne ønsker å bruke *selskapskort* til å hjelpe dem med å raskt identifisere og holde oversikt over hvilket selskap de arbeider med for øyeblikket. Hvis du vil ha mer informasjon, kan du se [Vise et selskapsmerke](#badge).

Det finnes noen funksjoner du kan bruke til å bytte mellom selskap mens du arbeider, for eksempel bytting av selskap (<kbd>Ctrl</kbd>+<kbd>O</kbd>). Lær mer på [Bytt til et annet selskap eller miljø](ui-organization-switch.md).

## <a name="badge"></a>Vise et firmakort

Når det er mer enn ett selskap eller miljø, vil du se at bytting av selskap øverst til høyre på programlinjen, nær søkeikonet på App-linjen. Som standard bruker bytting av selskap et standard selskapsikon, for eksempel ![startprogram for selskap-ikon.](media/ui-experience/company-icon.png "Viser ikonet for bytting av selskap som brukes når det er et enkelt miljø") og ![ompany-icon-mult-env](media/ui-experience/company-icon-multi-env.png "Viser ikonet for bytting av selskap som brukes når det er flere miljøer").

:::image type="content" source="media/ui-experience/company-switch-2.png" alt-text="Viser ikonet for bytting av selskap i overskriften til Business Central-klienten.":::  

Ved hjelp av siden **Selskapsinformasjon**kan du erstatte standard selskapsikon med et egendefinert kort per firma, hvis firmaskiltet gjør det enklere for brukerne å identifisere hvilket selskap de arbeider med.

1. På hurtigfanen **Selskapsmerke** fyller du ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
2. Når du er ferdig, oppdaterer du leseren (velg <kbd>Ctrl</kbd>+<kbd>F5</kbd>) for å oppdatere skiltet i klienten.  

> [!NOTE]
> Bytting av selskap ble innført i lanseringsbølge 2 for 2022, versjon 21. I tidligere versjoner brukes ikke firmamerket til å bytte mellom selskaper. Den vises øverst til høyre på de fleste sider, selv når det bare er ett selskap. Hvis du velger dette, vises hele firmanavnet og miljønavnet.

## Endre selskapsnavnet

Selskapsnavnet vises alltid øverst i venstre hjørne og fungerer som en handling du kan velge for å gå tilbake til rollesenteret. Du kan endre dette navnet på siden **Selskapsinformasjon**.

1. Velg ikonet ![tannhjulikonet for å åpne Innstillinger-menyen.](media/ui-experience/settings_icon_small.png) og velg handling **Selskapsopplysninger**.
2. Skriv inn det nye selskapsnavnet i feltet **Navn**.
3. Forlat siden. Systemet starter på nytt og viser det nye selskapet i øvre venstre hjørne.

## Opplevelse

Standard brukeropplevelse i en [!INCLUDE [prod_short](includes/prod_short.md)]-prøveversjon viser ikke alle funksjonene. Du kan bytte til full opplevelser på siden **Selskapsopplysninger**. Hvis du vil ha mer informasjon, kan du se [Endre hvilke funksjoner som vises](ui-experiences.md).  

## Se også

[Oversikt over oppgaver for å definere [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Hurtigstart for selskapsopplysninger](quick-start-company-information.md)  
[Konfigurer firmainformasjon i Italia](LocalFunctionality/Italy/how-to-set-up-company-information.md)  
[Endre grunnleggende innstillinger](ui-change-basic-settings.md)  
[Endre hvilke funksjoner som vises](ui-experiences.md)  
[Opprette nye selskaper](about-new-company.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
