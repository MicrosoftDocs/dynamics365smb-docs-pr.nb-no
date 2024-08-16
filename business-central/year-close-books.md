---
title: Lukker bøkene
description: 'Finn ut hvordan du lukker tablåene for et regnskapsår eller en regnskapsperiode, og hva som skjer etter at du har lukket ved utgangen av året.'
author: jswymer
ms.topic: overview
ms.devlang: al
ms.search.keywords: 'year closing, close accounting period, close fiscal year, bank account detailed trial balance'
m.search.form: 100
ms.date: 08/05/2024
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---

# <a name="closing-the-books"></a>Lukker bøkene
Når du har kontrollert at alle kontiene er oppdatert og har fordelt kost og inntekt, kan du lukke tablåene for et regnskapsår eller en periode.

Du trenger ikke å avslutte et år, men hvis du gjør det, blir det enklere å arbeide i systemet, ettersom du kan dra nytte av de praktiske filtreringsalternativene. Du trenger heller ikke å bekymre deg om å miste detaljer i transaksjoner når du avslutter, ettersom alle detaljer beholdes, selv etter at du har avsluttet året.

## <a name="closing-book-process"></a>Avslutning av bokprosess
Prosessen for å avslutte tablået omfatter disse hovedoppgaver:

1. Avslutte regnskapsperioden.

    Et regnskapsår er definert som én eller flere åpne perioder, som definert på siden **Regnskapsperioder**. Et vanlig regnskapsår består av 12 perioder på én måned hver, men du kan også velge en annen metode for å definere et år.

    Hvis du vil ha mer informasjon, kan du se [Avslutte regnskapsperioder](year-close-account-periods.md).
2. Registrere etterposter.

    Når du lukker et regnskapsår, må du angi flere administrative transaksjoner (for eksempel forhåndsbetalte og påløpte varer). Disse transaksjonene kalles justeringsposter. Der er ingen spesielle regler for bokføring av disse postene, og de (som andre poster) inneholder en hake i **Etterpost-feltet** hvis de er bokført på en dato i et lukket regnskapsår. Selv om et regnskapsår er avsluttet, kan du bokføre finansposter i det.
3. Overføre saldi fra resultatregnskapskontiene til balansen.

    Når et regnskapsår er lukket og alle etterposter er bokført, må resultatregnskapskontiene lukkes og nettoinntekten for året overføres til en konto under eiernes egenkapital i balansen. Bruk kjørselen Lukk resultatregnskapet til dette formålet. Kjørselen behandler alle finanskonti av typen Resultatregnskap og oppretter poster som tilbakefører saldiene. Disse postene er plassert i en kladd de kan bokføres fra. Kjørselen bokfører dem ikke automatisk, med unntak av når en tilleggsrapporteringsvaluta brukes. Når en tilleggsrapporteringsvaluta brukes, bokfører kjørselen direkte mot Finans.

    Hvis du vil ha mer informasjon,kan du se [Avslutte resultatregnskap](year-close-income-statement.md).
4. Bokføring av avslutningsposten for årsslutt sammen med motregning av poster på egenkapitalkontoen.

    Når kjørselen Avslutt resultatregnskapet er fullført, kan du bokføre poster som er generert av jobben. Hvis du ikke har angitt en konto for fri egenkapital i kjørselen, angir du én linje med en balansepost som bokfører nettoinntekten til riktig generell finanskonto under eiernes egenkapital i balansen. Til slutt bokfører du kladden.

    Hvis du vil ha mer informasjon, kan du se [Bokføre avslutningspost for årets slutt](year-how-post-year-end-close-entry.md).

## <a name="what-happens-when-you-close"></a>Dette skjer når du avslutter

Når du avslutter ved utgangen av året, flyttes egenkapitalen fra beregnet egenkapital til kontoen for fri egenkapital. Regnskapsåret merkes også som avsluttet, og alle etterfølgende poster for det avsluttede året merkes som etterposter.

Deretter genereres det en avslutningspost, men posten bokføres ikke automatisk. Du får muligheten til å lage motregningen eller egenkapitalkontopostene, slik at du kan bestemme hvordan du tildeler avslutningsposten. Hvis selskapet for eksempel har flere divisjoner, kan du generere en enkelt avslutningspost for alle divisjonene, og deretter kan du lage en motregningspost for egenkapitalkontoen til hver enkelt divisjon.

Du kan bokføre i et tidligere regnskapsår, selv etter at resultatkontoene er avsluttet, hvis du kjører kjørselen Lukk resultatregnskapet på nytt etterpå.

## <a name="see-also"></a>Se også

[Arbeide med regnskapsperioder og regnskapsår](finance-accounting-periods-and-fiscal-years.md)    
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)    


[!INCLUDE[footer-include](includes/footer-banner.md)]
