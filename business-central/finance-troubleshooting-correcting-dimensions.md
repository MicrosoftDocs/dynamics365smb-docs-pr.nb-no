---
title: Feilsøke og korrigere dimensjoner
description: Finn ut hvordan du feilsøker vanlige dimensjonsfeil, og hvordan du korrigerer dimensjonene etter at de er brukt på bokførte transaksjoner.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dimension, correction, correct, business intelligence
ms.search.form: 116, 540, 2588
ms.date: 09/27/2021
ms.author: bholtorf
ms.openlocfilehash: 2f9662df035851c1700a3b5ca01b71a418832dbf
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/19/2022
ms.locfileid: "9532839"
---
# <a name="troubleshooting-and-correcting-dimensions"></a>Feilsøke og korrigere dimensjoner

Finansrapportering og analysevisninger er ofte avhengige av data fra dimensjoner. Til tross for de tilgjengelige beskyttelsestiltakene oppstår det av og til en feil som kan føre til unøyaktighet. Dette emnet beskriver noen av de vanligste feilene og forklarer hvordan du korrigerer dimensjonstilordninger på bokførte transaksjoner, slik at finansrapporter blir nøyaktige.

## <a name="troubleshooting-dimensions-errors"></a>Feilsøke dimensjonsfeil

Når du bokfører dokumenter eller kladdelinjer som inneholder dimensjoner, kan det oppstå ulike feil, men de er vanligvis knyttet til en uriktig dimensjonskonfigurasjon eller -tilordning.

> [!NOTE]
> I følgende oversikt over potensielle feilmeldinger er *%X*-kodene plassholdere for datavariablene som den faktiske meldingen inneholder i brukergrensesnittet, avhengig av konteksten. For eksempel *%1 %2 er sperret.* kan vises i grensesnittet som "Dimensjonskoden OMRÅDE er sperret.".  

|Problem|Feilmelding|Mulig løsning|
|-----|-------------|-----------------|
|Sperret dimensjon|%1 %2 er sperret.|- Finne ikke-bokførte dokumenter som inneholder dimensjonssettet med den sperrede dimensjonen, og oppheve sperringen.<br />- Fjerne dimensjonssettet for den sperrede dimensjonen.|
|Slettet dimensjon|Finner ikke %1 %2.|- Gjenopprette den manglende dimensjonen.<br />- Finne ikke-bokførte dokumenter som inneholder dimensjonssettet med den manglende dimensjonen, og legge den til.<br />- Fjerne dimensjonssettet for den manglende dimensjonen.|
|Sperret dimensjonsverdi|%1 %2 - %3 er sperret.|- Finne ikke-bokførte dokumenter som inneholder dimensjonssettet med den sperrede dimensjonsverdien, og oppheve sperringen.<br />- Fjerne dimensjonssettet for den sperrede dimensjonsverdien.|
|Slettet dimensjonsverdi|    %1 for %2 mangler.|- Gjenopprette den manglende dimensjonsverdien.<br />- Finne ikke-bokførte dokumenter som inneholder dimensjonssettet med den manglende dimensjonsverdien, og legge den til.<br />- Fjerne dimensjonssettet for den manglende dimensjonsverdien.|
|Ikke tillatt dimensjonsverdi|Dimensjonsverditypen for %1 %2 - %3 kan ikke være %4.|- Endre **Dimensjonsverditype**-feltet på siden **Dimensjonsverdier** til **Standard** eller **Fra-sum**.<br />- Fjerne dimensjonssettet for den sperrede dimensjonsverdien.|
|Blokkert dimensjonskombinasjon|Dimensjonene %1 og %2 kan ikke brukes samtidig.|- Finne ikke-bokførte dokumenter som inneholder dimensjonssettet med den sperrede dimensjonskombinasjon, og oppheve sperringen.<br />- Endre en av de motstridende tillatelsessettlinjene for dimensjonskombinasjonen.|
|Blokkert dimensjonsverdikombinasjon|Dimensjonskombinasjonene %1 - %2 og %3 - %4 kan ikke brukes samtidig.|- Finne ikke-bokførte dokumenter som inneholder dimensjonssettet med den sperrede dimensjonsverdikombinasjonen, og oppheve sperringen.<br />- Endre en av de motstridende tillatelsessettlinjene for dimensjonsverdikombinasjonen.|
|Tom dimensjonsverdikoden for standarddimensjon, der feltet **Verdibokføring** inneholder **Obligatorisk kode**|- Velg en %1 for %2 %3.<br />- Velg en %1 for %2 %3 for %4 %5.|- Endre feltet **Verdibokføring** på siden **Standarddimensjon**.<br />- Angi en ikke-tom dimensjonsverdi for dimensjonen som er i konflikt i dimensjonssettet.|
|Feil dimensjonsverdikoden for standarddimensjon, der feltet **Verdibokføring** inneholder **Samme kode**|- Velg %1 %2 for %3 %4.<br />- Velg %1 %2 for %3 %4 for %5 %6.|- Endre feltet **Verdibokføring** på siden **Standarddimensjon**.<br />- Angi nødvendig dimensjonsverdi for dimensjonen som er i konflikt i dimensjonssettet.|
|Ikke-tom dimensjonsverdikoden for tom standarddimensjon, der feltet **Verdibokføring** inneholder **Samme kode**|- %1 %2 må være tom.<br />- %1 %2 må være tom for %3 %4.|- Endre feltet **Verdibokføring** på siden **Standarddimensjon**.<br />- Angi en tom dimensjonsverdikode for dimensjonen som er i konflikt i dimensjonssettet.|
|Uventet dimensjonsverdi for standarddimensjon, der feltet **Verdibokføring** inneholder **Ingen kode**|- %1 %2 skal ikke nevnes.<br />- %1 %2 må ikke nevnes for %3 %4|- Endre feltet **Verdibokføring** på siden **Standarddimensjon**.<br />- Fjerne den motstridende linjen fra dimensjonssettet.|
|En dimensjonskorrigering ble ikke fullført på riktig måte.||-Velg **Tilbakestill** for å tilbakestille korrigeringen til en utkasttilstand. Endringene tilbakestilles, og du kan kjøre korrigeringen på nytt.|

## <a name="changing-dimension-assignments-after-posting"></a>Endre dimensjonstilordninger etter bokføring

Hvis du oppdager at en feil dimensjon er blitt brukt i bokførte finansposter, kan du korrigere dimensjonsverdiene og oppdatere analysevisningene. Det vil bidra til å bevare økonomiske rapporter og analyse nøyaktig.

> [!IMPORTANT]
> Funksjonene for å korrigere dimensjoner er bare ment å gjøre finansrapportering nøyaktig. Dimensjonskorrigeringer gjelder bare for finansposter. De endrer ikke dimensjonene som er knyttet til postene i andre poster for den samme transaksjonen. Det oppstår en konflikt mellom dimensjonene som er tilordnet i Finans og underfinans.

### <a name="setting-up-dimension-corrections"></a>Konfigurere dimensjonskorrigeringer

Det er to ting å ta hensyn til når du definerer dimensjonskorrigeringer:

* Er det dimensjoner du ikke vil tillate at andre endrer? På siden **Innstillinger for dimensjonskorrigering** angir du hvilke dimensjoner du vil blokkere for endringer.
* Hvem vil du tillate å endre dimensjoner? Hvis du vil tillate at brukerne gjør endringer, tilordner du tillatelsen **D365-DIMENSJONSKORRIGERING** til brukerne. Tillatelsene gjør det mulig å opprette dimensjonskorrigeringer, kjøre dem og angre om nødvendig. De kan også angi sperrede dimensjoner. Hvis du vil ha mer informasjon, kan du se [Tilordne tillatelser til brukere og grupper](ui-define-granular-permissions.md). 

### <a name="correcting-a-dimension"></a>Korrigere en dimensjon

Du kan velge én eller flere finansposter manuelt eller bruke filtre til å velge sett med poster. Om nødvendig kan du også legge til eller slette dimensjoner. 

1. Bruk én av følgende sider for å starte en dimensjonskorrigering:

    * Velg et register på siden **Finansjournal**, og velg deretter handlingen **Korriger dimensjoner**. Dette starter en korrigering for postene i den valgte journalen.
    * På siden **Finansposter** velger du handlingen **Dimensjonskorrigering**. 

2. I feltet **Beskrivelse** angir du informasjon om endringen. Andre brukere kan bruke denne informasjonen senere til å forstå hva som ble gjort.
3. I hurtigfanen **Valgte finansposter** velger du de aktuelle postene.

    > [!IMPORTANT]
    > Når du endrer en markering, tilbakestilles verdiene i hurtigfanen **Endringer av dimensjonskorrigering**. Derfor må du alltid velge postene før du angir endringer i dimensjonsverdi.

   Tabellen nedenfor beskriver alternativene.

   |Alternativ  |Beskrivelse  |
   |---------|---------|
   |Legge til relaterte poster     |Legge til finansposter som er i samme finansjournal.|   
   |Legge til etter filter     |Bruke filterkriterier når du legger til finansposter.|
   |Manuelt valg     |Velg bestemte finansposter.         |
   |Legge til etter dimensjoner     |Filtrere finansposter etter dimensjoner.         |
   |Fjerne poster     |Oppheve valg av finansposter.         |
   |Behandle utvalgskriterier     |Hold styr på utvalgsprosessen, og angre valg om nødvendig.         |

4. I hurtigfanen **Endringer av dimensjonskorrigering** velger du dimensjonen du vil endre, i feltet **Dimensjonskode**, og deretter velger du den nye verdien i feltet **Ny dimensjonsverdikode**.
5. Hvis du vil bekrefte at korrigeringen er endret, velger du **Valider dimensjonsendringer**. Hvis du vil ha mer informasjon, kan du se [Validering av dimensjonskorrigeringer](finance-troubleshooting-correcting-dimensions.md#validating-dimension-corrections).
6. Velg **Kjør**.

### <a name="validating-dimension-corrections"></a>Validering av dimensjonskorrigeringer

Før du kjører en korrigering, er det lurt å validere den først. Valideringskontrollen kontrollerer restriksjoner for verdibokføring for finanskontiene, restriksjoner for dimensjoner og om dimensjonsverdiene er sperret. Under valideringen settes statusen for korrigeringen til **Validering pågår**. Når du har validert en korrigering, vises resultatet i feltet **Valideringsstatus**. Hvis det ble funnet feil, kan du bruke handlingen **Vis feil** til å undersøke dem. Når du har rettet en feil, må du bruke handlingen **Åpne på nytt** for å kjøre korrigeringen eller en ny validering.

Du kan enten kjøre en korrigering umiddelbart, eller du kan angi at den skal kjøres senere. Hvis du kjører korrigeringer i et stort datasett, anbefales det at du planlegger det for å kjøre utenom arbeidstiden. Hvis du vil ha mer informasjon, kan du se [Dimensjonskorrigeringer i store datasett](finance-troubleshooting-correcting-dimensions.md#dimension-corrections-on-large-data-sets).

### <a name="undoing-a-correction"></a>Angre en korrigering

Når du har korrigert en dimensjon, og du ikke liker det du ser, kan du bruke handlingen **Angre** til å tilbakestille den forrige verdien. Du kan imidlertid bare angre den siste korrigeringen. Før du angrer en korrigering, kan du bekrefte endringene som angrer vil gjøre. Dette er for eksempel nyttig hvis dimensjonsrestriksjoner er endret etter at korrigeringen ble utført.

Hvis handlingen Angre ikke er tilgjengelig, for eksempel fordi du har foretatt mange korrigeringer, kan du bruke handlingen **Kopier til utkast** til å starte en ny korrigering for de samme postene.

### <a name="dimension-corrections-on-large-data-sets"></a>Dimensjonskorrigeringer i store datasett

Vær forsiktig når du korrigerer store sett med poster, for eksempel sett som inkluderer mer enn 10 000 poster. Hvis du kan, anbefales det at du bruker filtrene til å kjøre korrigeringene på mindre datasett. Det kan også være lurt å kjøre korrigeringer utenfor normal arbeidstid. 

### <a name="use-analysis-views-with-dimension-corrections"></a>Bruk analysevisninger med dimensjonskorrigeringer

Hvis **Oppdatering ved bokføring** er aktivert for en analysevisning, kan [!INCLUDE[prod_short](includes/prod_short.md)] vise visningen når dokumenter og kladder bokføres. Du kan også oppdatere visninger med denne innstillingen aktivert med resultater for dimensjonskorrigeringer. Dette gjør du ved å aktivere **Oppdater analysevisninger**. Når du oppdaterer analysevisninger, kan det påvirke ytelsen, spesielt for store datasett, så det anbefales at du oppdaterer analysevisninger bare for små datasett.  

### <a name="viewing-historical-dimension-corrections"></a>Vise historiske dimensjonskorrigeringer

Hvis en finanspost er korrigert, kan du undersøke endringene ved hjelp av handlingen **Historikk for dimensjonskorrigeringer**.

### <a name="handling-incomplete-corrections"></a>Behandle ufullstendige korrigeringer

Hvis en korrigering ikke blir fullført, vises det en advarsel på korrigeringskortet. Hvis dette skjer, kan du bruke handlingen **Tilbakestill** til å tilbakestille korrigeringen til en kladdestatus og angre endringene. Deretter kan du kjøre korrigeringen på nytt.

> [!NOTE]
> Tilbakestilling av en ufullstendig korrigering påvirker ikke oppdateringer for analysevisninger, ettersom de skjer på slutten av korrigeringsprosessen.

### <a name="use-cost-accounting-with-corrected-gl-entries"></a>Bruk kostnadsregnskap med korrigerte finansposter

Når du har korrigert dimensjoner, vil dataene for kostnadsregnskap være usynkronisert. Kostnadsregnskap bruker dimensjoner til å aggregere beløp for kostsentre og kostobjekter, og til å kjøre kostnadsfordelinger. Når du endrer dimensjoner for finansposter, betyr det sannsynligvis at du må kjøre kostnadsregnskapsmodellene på nytt. Enten du bare trenger å slette noen få kostposter og kjøre tildelinger på nytt, eller hvis du skal slette alt og kjøre alle modellene på nytt, er avhengig av hvilke data som er oppdatert og hvordan dine kostnadsregnskapsfunksjoner er definert. Du må manuelt identifisere hvor dimensjonskorrigeringer vil påvirke kostnadsregnskap og hvor nødvendige oppdateringer er nødvendig. [!INCLUDE[prod_short](includes/prod_short.md)] har for øyeblikket ikke noen automatisert måte å gjøre dette på.

## <a name="see-related-microsoft-training"></a>Se relatert [Microsoft-opplæring](/training/modules/dimensions-dynamics-365-business-central/)

## <a name="see-also"></a>Se også

[Arbeid med dimensjoner](finance-dimensions.md)  
[Analysere data etter dimensjoner](bi-how-analyze-data-dimension.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
