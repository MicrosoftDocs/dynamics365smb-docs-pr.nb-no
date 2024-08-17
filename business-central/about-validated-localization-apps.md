---
title: Utvikling av validerte lokaliseringsapper
description: Overhold forskriftsmessige krav i Dynamics 365 Business Central som en validert lokaliseringsapp.
author: altotovi
ms.date: 06/04/2024
ms.reviewer: bholtorf
ms.topic: conceptual
ms.author: altotovi
---

# <a name="development-of-validated-localization-apps"></a>Utvikling av validerte lokaliseringsapper

Denne artikkelen beskriver kravene og retningslinjene for utvikling av en validert lokaliseringsapp for [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="what-is-a-validated-localization-app"></a>Hva er en validert lokaliseringsapp?

[!INCLUDE[prod_short](includes/prod_short.md)] er tilgjengelig [globalt på over 170 markeder](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json). I et sett med markeder samarbeider Microsoft med ISV-partnere for å lokalisere [!INCLUDE[prod_short](includes/prod_short.md)] gjennom lokaliseringsapper som er tilgjengelige på [Microsoft AppSource](https://go.microsoft.com/fwlink/?linkid=2081646). For disse områdene kan lokaliseringer være tilgjengelige via foretrukket app-program for lokalisering. Foretrukket app-program for lokalisering gjenkjenner disse appene, som er bygd i henhold til Microsofts spesifikke retningslinjer for kvalitet. ISV-partnere som overholder disse programkravene og retningslinjene, kan dra teknisk og kommersiell nytte av å betjene forhandlerne og kundene sine.  

I avsnittene nedenfor finner du krav og retningslinjer. Du kan kontakte programteamet hvis du vil delta i dette programmet og overholder kravene nedenfor, ved å kontakte oss via [Microsofts lokaliseringsteam](mailto:d365bcloc@microsoft.com).   

> [!IMPORTANT]
> Initiativet for validerte lokaliseringsapper for [!INCLUDE[prod_short](includes/prod_short.md)] rulles for tiden ut som et pilotprogram. Krav og fordeler nedenfor kan endres basert på tilbakemeldinger fra partnere og kunder.  

Apper i pilotprogrammet for validert lokalisering inneholder et sett med funksjoner som håndterer lokale forskriftsmessige krav, og som faller innenfor en av kategoriene i listen nedenfor.  

- **Forskriftsmessige krav** – lokal funksjonalitet som hjelper bedrifter med å oppfylle de juridiske kravene, for eksempel skatterapportering, lokale e-faktureringsformater, lokale regnskapsprinsipper og andre forskriftsmessige krav.
- **Krav til nasjonale standarder** – lokal funksjonalitet som håndterer lokale standarder, for eksempel adresseformater, nasjonale bankformater eller lokale tolkninger av globale standarder.
- **Lokalt språk** - lokalt språk i lokaliseringsappen, men også for en basisapp hvis dette språket for øyeblikket ikke er i listen over [støttede språk](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json).

> [!NOTE]
> Lokale markedsbehov eller bransjekrav bør ikke inkluderes i de foretrukne lokaliseringsappene. Hvis apper inneholder disse funksjonene, kan ikke appene godkjennes som validerte lokaliseringsapper.

> [!NOTE]
> Lokal funksjonalitet er gunstig for produktivitetsforretningsprosessene i et land og tilfører dermed verdi til virksomheten, men kreves ikke fra et forskriftsmessig perspektiv, for eksempel spesifikke bank- og betalingsformater, utgiftsrapporter, personalfunksjoner, lønn og lignende mindre eller større, og kjekt å ha-funksjoner bør isoleres i andre apper. Hvis apper inneholder disse funksjonene, kan de ikke godkjennes som validerte lokaliseringsapper.   

## <a name="validated-localization-app-business-requirements"></a>Forretningskrav for validert lokaliseringsapp

- Leverandøren av validert lokaliseringsapp oppfyller alle krav for å være en indirekte CSP-leverandør.  
- Leverandøren av validert lokaliseringsapp lanserer et minimum tilbud i fem land/områder, som leverer Dynamics 365 Business Central sammen med en validert lokaliseringsapp. 
- Leverandøren for validert lokaliseringsapp har minst ti [!INCLUDE[prod_short](includes/prod_short.md)]-nettkunder med produksjonsmiljøer som aktivt bruker den validerte lokaliseringsappen. 
- Leverandøren av validert lokaliseringsapp sender årlig en forretningsplan til programmets v-team. Dette inkluderer planlagte markedsførings- og klargjøringsaktiviteter for å markedsføre det samlede tilbudet med indirekte CSP-forhandlere i aktuelle land/områder. Planen kan sendes i begynnelsen av hvert kvartal til [Microsofts lokaliseringsteam](mailto:d365bcloc@microsoft.com).  
- Validerte lokaliseringsapper gjøres tilgjengelige for alle kunder og partnere som ønsker å dra nytte av det.     
- Leverandøren av validert lokaliseringsapp engasjerer seg i gjentakende arbeidsflyter med Microsoft.

## <a name="validated-localization-app-functional-and-technical-requirements"></a>Funksjonelle og tekniske krav til validert lokaliseringsapp

### <a name="functionality-requirements"></a>Krav til funksjonalitet

Bortsett fra å oppfylle de tekniske kravene for den foretrukne lokaliseringsappen, er det minste levedyktige produktomfanget for foretrukket lokaliseringsapp:  

- Lokale forskriftsmessige funksjoner:   
  - Juridiske krav.   
  - Offisielt obligatoriske funksjoner. 
  - Bare horisontale funksjoner (ikke bransjespesifikke).  
  - Gjelder i de fleste virksomheter.  
  - Innenfor følgende rammeverk:   
    - Områder med de hyppigste lovendringene. 
    - Spores allerede som en lokalisering i Microsoft-lokaliseringer. 
    - Funksjonsreferanser – sjelden nye.  
    - Ingen leverandør-/bankspesifikke formater, lønn eller lignende. 
    - Ingen globale funksjoner hvis de ikke er utviklet av Microsoft. 
- Oversettelser: 
  - Oversettelse av en lokaliseringsapp til lokale språk. 
  - Oversettelse av en basisapp til lokale språk – hvis språket ikke allerede [støttes](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json).  
  - Oversettelse av lokaliseringsappens dokumentasjon til lokale språk. 
- Selv om de begge er en del av lokaliseringen, anbefales det at nasjonale standardfunksjoner (lokal del) bygges som separate apper fra lokale forskriftsmessige funksjoner. 
- Demodata på det lokale språket som gjelder for det spesifikke markedet.   
- Alle funksjoner må utformes for å holde forenklet brukergrensesnitt, merk at de primært er ment for markedet for små og mellomstore bedrifter.  
- Unngå å bygge nye funksjoner hvis det allerede finnes de samme eller lignende funksjoner i basisappen, for eksempel elektronisk fakturering, revisjonseksport, mva-funksjoner, datautveksling og andre der det meste av funksjonaliteten er felles for alle land/områder, men det finnes enkelte lokale regler eller forretningsformater som er utvidelser av globale rammeverk eller formater. I stedet for å bygge nye funksjoner kan du utvide eksisterende.  
- Klargjør oppsettsveiledninger (veivisere) for områder som er komplekse å konfigurere, for å hjelpe brukere med å aktivere, oppdage og ha god førsteopplevelse med å bruke lokaliseringsappen.  
- Partnere må sørge for funksjonell dokumentasjon for alle aspekter ved lokaliseringen.  

### <a name="technical-requirements"></a>Tekniske krav

Nedenfor ser du en liste over krav du må oppfylle før du sender den validerte lokaliseringsappen som en utvidelse for validering. Denne listen endrer ikke den [tekniske valideringslisten](/dynamics365/business-central/dev-itpro/developer/devenv-checklist-submission) og utvider bare kravene derfra.  

- Leverandørene av validert lokaliseringsapp må bygge den validerte lokaliseringsappen basert på W1-basisappen.  
- Leverandørene av validert lokaliseringsapp må følge Microsofts policyer for livssyklus og kundestøtte.   
- Obligatorisk testautomatisering må dekke minst 80 % av koden, og alle forretningsprosesser som endres med validert lokaliseringsapp må dekkes av testautomatisering.  
- Leverandørene av validert lokaliseringsapp må oppdatere eller teste validert lokaliseringsapp før den offisielle lanseringen av ny versjon (minimum med RC før ny utgivelse) for å bekrefte at det ikke er noen problemer. 
- Alle objekter i koden for validert lokaliseringsapp må være på engelsk.   
- Leverandørene av validert lokaliseringsapp må følge Microsofts policy for foreldede objekter og brytende endringer og anbefalte fremgangsmåter for avskrivning av AL-koden.  
- Leverandører av validert lokaliseringsapp bør legge til nye hendelser hvis det kreves av markedet (andre implementeringspartnere eller kunder) hvis det er fornuftig forretningsmessig å følge Microsofts retningslinjer og praksis. Ellers må leverandørene av validert lokaliseringsapp svare på slike henvendelser med riktig begrunnelse for hvorfor det ikke gir rimelig forretningsmessig mening å legge til. 
- Leverandørene av validert lokaliseringsapp må tilby skriftlige testscenarioer på engelsk og gjøre det mulig for Microsoft å utføre manuell testing hvis det kreves av Microsoft.  
- Hvis en validert lokaliseringsapp utvider [!INCLUDE[prod_short](includes/prod_short.md)]-datamodellen med nye tabeller eller felter, må leverandøren av validert lokaliseringsapp angi **DataClassification**-egenskapen riktig.

> [!NOTE]  
> Du kan også opprette en integrering hvis du synes det er fordelaktig å ha noe funksjonalitet plassert utenfor [!INCLUDE[prod_short](includes/prod_short.md)]-miljøet og i stedet koble til [!INCLUDE[prod_short](includes/prod_short.md)] ved hjelp av for eksempel API-er eller nettjenester.

## <a name="see-also"></a>Se også

[Teknisk validering](/dynamics365/business-central/dev-itpro/developer/devenv-checklist-submission)  
[Utvikling av en standard lokaliseringsløsning](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-develop-localization)  
[Land-/områdetilgjengelighet og støttede oversettelser](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations)  
[Hva er Lokal funksjonalitet i Dynamics 365 [!INCLUDE[prod_short](includes/prod_short.md)]?](about-localization.md)  
[Internasjonal tilgjengelighet for Microsoft Dynamics 365](/dynamics365/get-started/availability)  
[Samsvarsoversikt](compliance/compliance-overview.md)  
[Geografisk tilgjengelighet for Dynamics 365](https://releaseplans.microsoft.com/availability-reports/?report=productgeoreport/)  
