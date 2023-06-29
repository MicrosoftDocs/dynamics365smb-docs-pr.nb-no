---
title: Hurtigstart for økonomisk informasjon
description: Få selskapet klart til å gjøre forretninger ved å sette opp økonomisk informasjon i Business Central.
author: rubenseishima
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: quickstart
ms.search.form: null
ms.date: 08/25/2022
ms.author: a-reishima
---

# <a name="financial-information-quick-start"></a><a name="financial-information-quick-start"></a>Hurtigstart for økonomisk informasjon

Når du har skrevet inn grunnleggende selskapsopplysninger i [!INCLUDE[prod_short](includes/prod_short.md)], er et av de neste trinnene å fylle ut økonomidelen. Dette gjør du ikke bare for å motta eller foreta betalinger, men du må også håndtere og rapportere firmanumrene på riktig måte.

## <a name="the-chart-of-accounts"></a><a name="the-chart-of-accounts"></a>Kontoplanen

Kontoplanen gir en oversikt over firmaets økonomi, viser kontoer i strukturerte grupper, for eksempel eiendeler, gjeld, inntekt, solgte varers kost og utgifter. [!INCLUDE[prod_short](includes/prod_short.md)] inneholder en standard kontoplan du kan tilpasse etter virksomhetens regnskapsprinsipper.

## <a name="set-up-the-chart-of-accounts"></a><a name="set-up-the-chart-of-accounts"></a>Definere kontoplanen

I denne videoen får du vite hvordan du definerer kontoplanen i [!INCLUDE[prod_short](includes/prod_short.md)].

<br /><br />

> [!Video https://www.microsoft.com/videoplayer/embed/RE43KO9?rel=0]

### <a name="add-an-account-to-the-chart-of-accounts"></a><a name="add-an-account-to-the-chart-of-accounts"></a>Legg til en konto i kontoplanen

Hvis du vil legge til en konto som ikke er inkludert som standard i [!INCLUDE[prod_short](includes/prod_short.md)], for eksempel hagetjenester, bare følger du denne fremgangsmåten:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Kontoplan** og velger deretter den relaterte koblingen.
2. Velg handlingen **Ny** for å åpne **Finanskontokort**-siden.
3. Angi følgende data i tilsvarende felter i hurtigfanen **Generelt**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   | Felt | Data |
   | --- | --- |
   | **Nr.** | 61250 |
   | **Navn** | Hagetjenester |
   | **Resultat/Balanse** | Resultatregnskap |
   | **Kontokategori** | Utgift |
   | **Kontodelkategori** | Utgift for reparasjon og vedlikehold |
   | **Debet/Kredit** | Begge |
   | **Kontotype** | Bokføring |

4. Skriv inn følgende data på hurtigfanen **Bokføring**:

   | Felt | Data |
   | --- | --- |
   | **Generell bokføringstype** | Kjøp |
   | **Bokføringsgruppe - firma** | Innenlands |
   | **Bokføringsgruppe – vare** | Tjenester |

5. Fyll ut gjenværende felter på **Finanskontokort** etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="get-an-overview-of-the-chart-of-accounts"></a><a name="get-an-overview-of-the-chart-of-accounts"></a>Få en oversikt over kontoplanen

Hvis du trenger en mer kompakt visning av kontoplanen, uten for eksempel kolonner for bokføringsgrupper, bokføringstype eller kosttype, viser listen **Oversikt over kontoplan** hovedinformasjonen for hver konto i en mindre tabell. I tillegg kan du skjule eller vise grupper for å skjule kontoene i dem.

Hvis du vil vise oversikten, velger du **Oversikt over kontoplan**-handling på **Kontoplan**-siden, eller du kan søke etter funksjonen ved hjelp ![Lyspære som åpner Fortell meg-funksjonen 1.](media/ui-search/search_small.png "Fortell hva du vil gjøre").

Lær mer om kontoplanen og finans under [Forstå Finans og Kontoplan](finance-general-ledger.md).

## <a name="set-up-bank-accounts"></a><a name="set-up-bank-accounts"></a>Opprett bankkontoer

Bankkontoer i [!INCLUDE[prod_short](includes/prod_short.md)] registrere banktransaksjoner og knyttes til poster i kontoplanen. I denne videoen får du vite hvordan du definerer bankkontoer.

<br /><br />

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Vhpl?rel=0]

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Bankkontoer**, og velg deretter den relaterte koblingen.
2. På siden **Bankkonti** velger du handlingen **Ny**.
3. I **Nr.** feltet angis det automatisk en identifikator som *B010* hvis det er angitt en nummerert serieliste angitt for bankkontoer. Hvis ikke angir du en unik kombinasjon.

   Feltet er forskjellig fra feltet **Bankkontonr.** også tilgjengelig på hurtigfanen **Generelt**.
4. Fyll ut feltene på siden **Leverandørs bankkort** etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-related-training-at-microsoft-learn"></a><a name="see-related-training-at-microsoft-learn"></a>Se relatert opplæring på [Microsoft Learn](/learn/paths/set-up-financial-management-dynamics-365-business-central/).

## <a name="see-also"></a><a name="see-also"></a>Se også

[Definer kontoplanen](finance-setup-chart-accounts.md)  
[Opprett bankkonti](bank-how-setup-bank-accounts.md)  
[Kjør og skriv ut rapporter](ui-work-report.md)  
[Hurtigstart for Business Central](quick-start-business-central.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
