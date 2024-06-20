---
title: Betalingspraksisrapport
description: Lær hvordan du enkelt oppretter rapporten Betalingspraksiser for leverandører og kunder.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment, practices, vendor, customer, report'
ms.search.form: '686, 687, 689'
ms.date: 04/23/2024
ms.author: altotovi
ms.reviewer: bholtorf
--- 

# Betalingspraksisrapport  

Noen land/områder krever at selskaper rapporterer betalingstider for leverandørene sine, slik det er definert av lokale myndigheter. Denne rapporteringen kan være basert på ulike kilder og kan sortere leverandører basert på størrelse eller definerte betalingsbetingelser og gir rapportering for leverandører for følgende som kreves av lokale myndigheter:  

- Gjennomsnittlig avtalt betalingsperiode.  
- Gjennomsnittlig faktisk betalingsperiode.   
- Andelen fakturaer betalt etter utløpet av den avtalte betalingsperioden. 

Brukere kan velge perioden de vil kjøre en beregning for, og finne detaljer basert på en gruppering de velger. For hver av disse grupperingene kan du finne kildeoppføringer. 

> [!NOTE]
> Denne rapporteringen er foreløpig påkrevd i noen land, men dette er en global funksjon og kan brukes overalt. For tiden må svenske selskaper med 250 eller flere ansatte hvert år rapportere til det svenske selskapsregistreringsverket hvilke betalingstider de har for kjøp fra selskaper som er mindre enn dem selv. Lignende handlinger finnes i Storbritannia, Australia og New Zealand.  

## Generer rapporten 

Bruk følgende fremgangsmåte for å kjøre rapporten **Betalingspraksiser**:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Betalingspraksiser** og velg den relaterte koblingen. 
2. Velg **Ny**.
3. Angi verdiene i følgende felter på hurtigfanen **Generelt**:

   | Felt | Description |
   |---------|-----------------------------------|
   | Nr. | Angir nummeret for oppføringen eller posten for rapporten. |
   | Samlingstype | Angi hvordan data aggregeres. Hvis du velger alternativet **Periode**, er rapporten basert på ulike perioder, men hvis du velger alternativet **Selskapsstørrelse**, opprettes rapporten basert på selskapsstørrelser som er konfigurert i feltet **Selskapsstørrelseskode** på **Leverandør**-kortet. |
   | Toppteksttype | Angir kilden for poster i betalingspraksisen, og du kan velge Leverandører, Kunder eller begge. |
   | Startdato | Angir startdatoen for betalingspraksisen. |
   | Sluttdato | Angir sluttdatoen for betalingspraksisen. |

> [!NOTE]
> Hvis du bestemmer deg for å bruke alternativet **Selskapsstørrelse**, må du først opprette poster på siden **Selskapsstørrelser** og legge dem til i alle leverandørene du vil spore med denne metoden.

4. Når du fyller ut alle feltene i overskriften, må du kjøre handlingen **Generer** for å generere data på linjene og statistikken for valgt rapporteringstype.
5. Basert på **aggregasjonstypen** får du forskjellige linjer. Du kan endre noen av verdiene manuelt, men i dette tilfellet merkes hver av de endrede linjene og hele rapporten som **Endret manuelt**.
6. Fra alle beregnede felter kan du gå dypere for å se hvordan dette resultatet er beregnet, ved å åpne siden **Liste over betalingspraksisdata**.
7. Hvis du vil skrive ut dokumentet, kan du gjøre det ved å kjøre handlingen **Skriv ut**.

## Se også

[Finansrapporter](finance-reports.md)  
[Analyser årsregnskap i Microsoft Excel](finance-analyze-excel.md)  
[Rapporter og analyse av utestående fordringer](receivables-reports.md)  
[Rapporter og analyse av leverandørgjeld](payables-reports.md)  
[Konfigurere finans](finance-setup-finance.md)  
[Finans](finance.md)  
[Oversikt over lokale funksjoner](about-localization.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
