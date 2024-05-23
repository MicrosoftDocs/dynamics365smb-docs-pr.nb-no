---
title: Tildel e-dokumenter til bestillingslinjer med Copilot
description: Lær hvordan du bruker Copilot til å tilordne e-dokumenter til bestillingslinjer.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.collection:
  - get-started
  - bap-ai-copilot
ms.date: 04/10/2024
ms.custom: bap-template
---

# <a name="map-e-documents-to-purchase-order-lines-with-copilot-preview"></a>Tildel e-dokumenter til bestillingslinjer med Copilot (forhåndsversjon)

Etter hvert som innkjøpsprosessene blir mer digitale, spiller funksjonen for e-dokumenter i Business Central en nøkkelrolle i automatiseringen av mottak og behandling av leverandørfakturaer. Copilot kan hjelpe denne prosessen ved å forbedre tildelingen og samsvaret av leverandørfakturaer mot bestillinger. Dette reduserer tidkrevende oppgaver som normalt ville inkludere omfattende søk, oppslag og dataregistrering. Fordelen forsterkes av at leverandørfakturaer ofte ikke forholder seg nøyaktig til bestillinger, og i så fall er Copilot bedre posisjonert til å identifisere de tilsvarende innkjøpsordrene. Forbedrede samsvarsfunksjoner er spesielt til fordel for små og mellomstore organisasjoner som trenger effektiv dokumentsporing for bestillingslinjer. Copilot er den KI-drevne assistenten for arbeid som øker kreativiteten og forbedrer produktiviteten for Business Central-brukere.

> [!IMPORTANT]
> - Dette er en produksjonsklar evalueringsfunksjonalitet for produksjons- og sandkassemiljøer i alle landlokaliseringer, med unntak av Canada.
> - Produksjonsklare forhåndsversjoner er underlagt tilleggsvilkårene for bruk. Mer informasjon: [Tilleggsvilkår for bruk for prøveversjoner av Dynamics 365](https://go.microsoft.com/fwlink/?linkid=2105274)
> - Innhold generert av kunstig intelligens kan være feil.

I den første utgivelsen appen for **e-dokumenter** introduserte vi grunnleggende scenarioer for e-dokumenter for hele salgsprosessen. Det er imidlertid behov for forbedringer og automatisering i håndteringen av de mottatte dokumentene, spesielt i forbindelse med kjøpsprosesser. Copilot forbedrer måten du håndterer e-dokumenter på i kjøpsprosessen, spesielt når det gjelder bestillinger. Ved hjelp av rammeverket for e-dokumenter kan du angi hvilken type kjøpsdokument som skal opprettes for hver leverandør når du mottar e-fakturaer fra dem. Tidligere var det eneste alternativet å opprette en kjøpsfaktura, enten som et dokument eller en finanskladd.

Du kan nå oppdatere en eksisterende bestilling i Business Central med informasjonen som mottas i e-fakturaen.

<!--
> [!NOTE]
> - This feature is available as a production-ready preview for production and sandbox environments in any country localization, with the exception of Canada. Production-ready previews are subject to supplemental terms of use. For more information, see [Supplemental terms of use for Dynamics 365 preview](https://go.microsoft.com/fwlink/?linkid=2105274).
> - AI-generated content may be incorrect.-->

## <a name="to-activate-copilot"></a>Slik aktiverer du Copilot

Hvis du ikke aktiverte Copilot for **samsvarshjelp for e-dokument**, må du gjøre det manuelt. Følg denne fremgangsmåten for å aktivere kopiloten **Samsvarshjelp for e-dokument**: 

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Copilot og KI-funksjoner**, og velg deretter den relaterte koblingen. 
2. Velg **Samsvarshjelp for e-dokument** i listen over funksjoner, og endre statusen til **Aktiv**.  

Du kan begynne å bruke Copilot så snart den er aktivert. 

## <a name="identify-purchase-orders"></a>Identifiser bestillinger

Først kan du identifisere bestillingene som du kan samsvare automatisk. Hvis **leverandøren** har konfigurert feltet **Motta e-dokument til** til å fungere med **bestillinger**, gjøres følgende når det elektroniske dokumentet er opprettet i [!INCLUDE[prod_short](includes/prod_short.md)] (manuelt eller fra et eksternt endepunkt): [!INCLUDE[prod_short](includes/prod_short.md)] gjør følgende:

1. Hvis **bestillingen** for denne bestemte leverandøren *finnes, og det finnes et bestillingsnummer* i den mottatte **e-dokumentfilen**, kobler [!INCLUDE[prod_short](includes/prod_short.md)] dette **e-dokumentet** automatisk til den angitte **bestillingen**. **Dokumentstatusen** for dette **e-dokumentet** er **Pågår**, og **e-dokumentstatusen** på undersiden **Tjenestestatus** blir **Ordre koblet**.  
Denne koblingen vil være synlig i **Dokument**-feltet i dette spesifikke **e-dokumentet**. Hvis du må endre **bestillingen** som er koblet automatisk, kan du gjøre det ved å bruke handlingen **Oppdater bestillingskobling** og deretter velge manuelt en av de eksisterende bestillingene for denne leverandøren. Du kan bare gjøre dette før du samsvarer linjene mellom **e-dokument** og **bestilling**.  
2. Hvis **bestillingen** for denne bestemte leverandøren *finnes, men det ikke finnes et bestillingsnummer* i mottatt **e-dokumentfil**, hvis du lastet opp dette dokumentet manuelt, tillater [!INCLUDE[prod_short](includes/prod_short.md)] deg å velge fra en av de eksisterende bestillingene, noe som åpner listen **Bestillinger** fra ordrene du fikk fra leverandører som bare inneholder **e-dokumentet**, der du må velge **bestillingen** du vil bruke, og velge **OK**. Hvis du ikke velger riktig **bestilling** eller du fikk **e-dokumentet** automatisk fra et eksternt endepunkt ved hjelp av **prosjektkøen**, kobles ikke det nye **e-dokumentet** til noe kjøpsdokument, og **dokumentstatusen** vises som **Feil**, og **e-dokumentstatusen** på undersiden **Servicestatus** er **Feil ved behandling av importert dokument**. Når du skal fullføre tilknytningen til **bestillingen**, velger du handlingen **Oppdater bestillingskobling** og velger deretter en av de eksisterende bestillingene for denne leverandøren.  

## <a name="map-lines"></a>Tildel linjer

Copilot hjelper deg med å samsvare e-fakturalinjer med bestillingslinjer automatisk, og tilbyr ekstra samsvarende intelligens for å forbedre treffene.

Når de er samsvart og tilordnet, oppdaterer [!INCLUDE [prod_short](includes/prod_short.md)] den samsvarende bestillingen med relevant mottaksinformasjon for å sikre at de riktige antallene mottas på bestillingslinjene.

Du kan avstemme mottatte elektroniske dokumenter med bestillingslinjene fra to forskjellige steder, fra **E-dokumenter**-siden eller fra **Bestilling**-siden. Den enkleste måten å finne de allerede tilknyttede **bestillingene** på, er å bruke flisen **Koblede bestillinger** som del av **e-dokumentaktiviteter**. Du finner alle ikke-koblede dokumenter ved hjelp av flisen **Venter på e-fakturaer,** der du har en liste over **e-dokumenter** du må se gjennom.  

> [!NOTE]
> **E-dokumentaktivitetene** med disse to flisene finner du i følgende rollesentre: **Evaluering av forretningsleder**, **Forretningsleder**, **Regnskapsfører**, **Lagerleder** og **Levering og mottak**.

Når du vil kjøre samsvar fra bestillingen, velger du handlingen **Tildel e-dokumentlinjer**, som finnes både på bestillings- og bestillingslistesidene. Hvis du imidlertid vil kjøre samsvar fra siden **E-dokumenter**, velger du handlingen **Samsvar bestilling** fra denne siden. Følg denne fremgangsmåten for å fortsette med samsvar:

1. Velg handlingen **Tildel e-dokumentlinjer** eller **Avstem bestilling** for dokumenter som allerede er koblet.  
2. Du kan legge merke til at **Samsvarshjelp for e-dokument med Copilot**-spørringen fungerer, og du har siden **Bestillingssamsvar** i bakgrunnen. Det betyr at den samme prosessen skjer, men med automatisk støtte fra **Copilot**, som kjører prosessen med avstemming i stedet for deg. 
3. Etter noen sekunder vil **Samsvarshjelp for e-dokument med Copilot** foreslå linjer for avstemming med flere detaljer: 

    1. I spørringshodet finner du følgende informasjon: 

    |Feltnavn |Description |
    |--------|-----------------|
    |Automatisk avstemt | Angir antall avstemminger foreslått automatisk. Dette er basert på en strengsammenligning, og hvis det er 80 % eller mer overlappende beskrivelse, vil systemet avstemme disse beskrivelsene automatisk uten å bruke GPT-funksjoner. |
    |Avstemt med Copilot | Angir antall treff foreslått av Copilot ved hjelp av både strengsammenligning og semantisk sammenligning. |
    |E-dokumentnr. | Angir det tilknyttede e-dokumentnummeret. |
    |Totalbeløp for faktura ekskl. mva. | Angir det totale fakturabeløpet ekskl. mva. |
    |Avstemt totalbeløp inkl. mva. | Angir det avstemte beløpet ekskludert mva. |
    
    2. Hvis alle linjene er avstemt, ser du den grønne teksten øverst til høyre: **Alle linjene (100 %) avstemt. Gå gjennom avstemmingsforslag**.  
    3. I **Avstemt forslag**-linjene finner du følgende informasjon:  

    |Feltnavn |Description |
    |--------|-----------------|
    |E-dokumentlinjenr. | Angir linjenummeret for e-dokumentet (kommer fra den opprinnelige e-dokumentfilen). |
    |Beskrivelse av e-dokumentlinje | Angir beskrivelsen av e-dokumentet (kommer fra den opprinnelige e-dokumentfilen). |
    |Avstemt antall | Angir antallet som skal brukes på bestillingslinjen. |
    |Tilbud | Angir handlingen som er foreslått av kunstig intelligens, og disse foreslåtte handlingene er knyttet til avstemming av bestillingslinjene. |

    4. Alle fullstendig foreslåtte og avstemte linjer er merket med grønn farge. Hvis det er et problem, for eksempel en annen pris, men i den tillatte prisklassen, blir denne linjen være merket med gul farge, og hvis det er likhet mellom beskrivelsesfeltene, men prisforskjellen er større enn tillatt, blir denne linjen merket med rød farge. 
    5. Hvis du ikke er fornøyd med noen forslag, kan du slette dem ved hjelp av handlingen **Slett linje**.  
    6. Hvis du vil se forslagssamsvar, kan du velge koblingen i **Forslag**-kolonnen for å åpne siden **Samsvarsdetaljer for e-dokument**. 
    7. På siden **Samsvarsdetaljer for e-dokument** kan du sammenligne detaljer fra **e-dokumenter** og **bestillingen** for å være sikker på det foreslåtte samsvaret før du bekrefter det. 
    8. Lukk siden etter gjennomgang.   

4. Hvis du ikke er fornøyd med de fleste forslagene, eller hvis du ikke vil bruke funksjonen **Ordrelinjer for e-dokumentavstemminger med Copilot**, velger du **Forkast det**, og du kan fortsette med den [manuelle avstemmingen](finance-how-use-edocuments-purchase.md).  
5. Hvis du vil beholde forslag, velger du **Behold det**-knappen, så lagrer systemet alle forslag fra **Copilot**.  
6. [!INCLUDE[prod_short](includes/prod_short.md)] lukker Copilot-meldingen, og linjene på siden **Bestillingssamsvar** merkes som grønne, siden de allerede samsvarer.  
7. Fra nå av kan du fortsette å arbeide mens du utfører manuell avstemming, og det betyr at du kan fjerne avstemminger, manuelle avstemminger, tilbakestille samsvar, eller hvis det ikke er noen endringer du vil gjøre, velger du bare handlingen **Bruk på bestilling** og fortsetter å arbeide med **bestillingen**. 

> [!NOTE]
> Du kan også velge handlingen **Avstem med Copilot** fra siden **Bestillingssamsvar** på nytt, men i dette tilfellet blir du spurt om du vil overskrive de eksisterende avstemmingene, siden alle linjene allerede er avstemt.  

> [!NOTE]
> Pris-/kostanalyse, og kontrollen for tilgjengelig antall er en del av forhåndsbehandlingsaktiviteten. 

## <a name="see-also"></a>Se også

[Oversikt over e-dokumenter](finance-edocuments-overview.md)    
[Bruk e-dokumenter i salg](finance-how-use-edocuments.md)    
[Bruk e-dokumenter ved kjøp](finance-how-use-edocuments-purchase.md)   
[Feilsøk Copilot- og KI-funksjoner](ai-copilot-troubleshooting.md)    
[Vanlige spørsmål om ansvarlig kunstig intelligens for bankavstemmingshjelp](faqs-bank-reconciliation.md)    
