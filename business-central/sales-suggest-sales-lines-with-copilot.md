---
title: Foreslå salgslinjer med Copilot
description: Lær hvordan du foreslå linjer i ordrer med Copilot.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: 'Copilot, AI, sell'
ms.search.form: null
ms.date: 02/02/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
ms.collection: bap-ai-copilot
---

# <a name="suggest-lines-on-sales-documents-with-copilot-preview"></a>Foreslå linjer i salgsdokumenter med Copilot (forhåndsversjon)

[!INCLUDE[preview-banner](includes/preview-banner.md)]

Denne artikkelen forklarer hvordan du oppretter salgsdokumenter raskere ved å la Copilot foreslå hvilke varer som skal legges til på linjer i salgsdokumenter for kundene dine.

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

## <a name="about-sales-line-suggestions-with-copilot"></a>Om salgslinjeforslag med Copilot

Salgslinjeforslag med Copilot kan hjelpe deg med å opprette linjer i salgsdokumenter, for eksempel tilbud, ordrer og fakturaer, basert på strukturerte inndata eller naturlig språk. Funksjonen er ikke en generell chat, men en svært spesifikk og integrert opplevelse som du kan bruke i salgsdokumenter. Funksjonen tilbyr to forskjellige kompetanser som hjelper deg med å finne data om individuelle produkter eller de fullstendige dokumentene.

* Finn produkter

  Informasjon som beskriver produkter, er lagret flere steder i [!INCLUDE [prod_short](includes/prod_short.md)]. Varenumre og beskrivelser er for eksempel lagret i **Vare**-tabellen, mange strekkoder er lagret i **Varereferanse**-tabellen, og produktegenskaper er lagret i **Vareattributter**-tabellen. Selv om du kanskje ber om *rød sykkel*, kan det faktiske produktet være *Crimson tourer*, der *sykkel* er en produktkategori og *rød* er et attributt.

* Finn dokumenter etter referanse

  Folk gjentar ofte en tidligere ordre, eller i det minste bruker den som utgangspunkt. Men det kan være vanskelig å finne riktig ordre i en bunke med ordrer. Du husker kanskje litt av ordre-ID-en, som kan være et selskapsnummer eller et referansenummer som er mottatt fra en kunde. Du kan bruke ledetekster som *Trenger siste faktura fra april*, og dette bør hjelpe deg med å finne en bestilling raskere.

## <a name="available-languages"></a>Forutsetninger

* Salgslinjeforslag med Copilot aktiveres av en administrator. Hvis du vil lære mer om hvordan du aktiverer KI-funksjoner, kan du gå til [Konfigurer Copilot- og KI-funksjoner](enable-ai.md).
* Du er kjent med oppretting av ordrer.

## <a name="prerequisites"></a>Geografisk tilgjengelighet

Tabellen nedenfor viser de geografiske Microsoft Azure-områdene der denne funksjonen er tilgjengelig.

|Azure-område for miljø  |Azure OpenAI-tjenestegeografi   |Administratorhandling kreves for å få tilgang til Copilot  |
|---------|---------|---------|
|Tyskland (nord, vest-sentralt)     | Sverige eller Sveits        |  Ja       |
|Norge (øst, vest)     | Sverige eller Sveits        | Ja     |
|Singapore     |         |         |
|Sør-Afrika (nord, vest)     |   USA      |   Ja      |
|Sveits (nord, vest)     |  Sverige eller Sveits       |    Ja     |
|De forente arabiske emirater (nord, vest)     |    USA     |   Ja     |
|USA (sentral, øst, nord-sentral, sør-sentral, vest)     |   USA      |   Nei      |
|Europa (vest, nord)     |   Sverige eller Sveits      |   Ja      |
|Asia/Stillehavskysten     |         |         |
|Australia (sør-øst)     |   USA      |    Ja     |
|Sør-Amerika     |         |         |
|India (sentralt, sør)     |    USA     |   Ja      |
|Japan (øst, vest)     |    USA     |    Ja     |
|Frankrike (sentralt, sør)     |    Sverige eller Sveits     |    Ja     |
|Korea (sentralt, sør)     |    USA     |    Ja     |

## <a name="examples-of-prompts"></a>Eksempler på ledetekster

Foreslå salgslinjer med Copilot kan håndtere et bredt spekter av ledetekstinndata. Denne delen inneholder noen eksempler på ledetekster for ulike scenarioer vi har testet.

### <a name="sample-inquiry-to-repeat-the-past-document"></a>Eksempelforespørsel for å gjenta det siste dokumentet

Ledetekst: *Trenger alle produktene fra faktura 103031*

### <a name="during-phone-call-user-quickly-types-list-of-required-products-and-quantities-not-always-accurate-enough-or-using-internal-product-names"></a>Under telefonsamtalen lister brukeren raskt opp nødvendige produkter og mengder, ikke alltid nøyaktig nok eller ved hjelp av interne produktnavn

Ledetekst: *2 røde syykler for bran*

Merk at ledeteksten fungerer, selv med flere skrivefeil.

### <a name="a-user-copies-an-inquiry-from-an-inbound-communication-and-pastes-it-to-the-sales-lines-suggestions-page"></a>En bruker kopierer en forespørsel fra en innkommende kommunikasjon og limer den inn på siden Salgslinjeforslag

Ledetekst: *Hei, jeg er interessert i å kjøpe tilbehør til min XXXX bærbare datamaskin, for eksempel en trådløs mus, et tastaturdeksel og en bærbar veske. Jeg lurer på om dere har noen anbefalinger eller forslag til disse elementene. Har dere noen spesialtilbud eller rabatter for lojale kunder som meg? Vennlig hilsen M*

Merk at XXXX bærbar datamaskin ikke er inkludert i søk.

## <a name="suggest-lines-on-a-sales-document"></a>Foreslå linjer i et salgsdokument

Denne prosessen beskriver hvordan du foreslår linjer i en ordre. Trinnene er de samme for tilbud og fakturaer.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Ordre**, og velg deretter den relaterte koblingen.
1. Åpne ordren.
1. På hurtigfanen **Linjer** velger du **Hent linjeforslag**.
1. I vinduet **Foreslå linjer med Copilot** skriver du inn ledeteksten eller velger en fra veiledningene.

## <a name="review-save-discard-or-regenerate-suggestions"></a>Gå gjennom, lagre, forkast eller generer forslag på nytt

Når Copilot har foreslått elementene du vil legge til på linjer, kan du se gjennom forslagene og avgjøre om du vil bruke dem:

* Hvis du vil forkaste én enkelt foreslått linje, merker du den i listen og velger deretter handlingen **Slett linje**.
* Hvis du vil forkaste alle foreslåtte linjer og lukke Copilot-vinduet, velger du Forkast-knappen (papirkurven) ved siden av **Behold den**-knappen.
* Hvis du vil overføre linjene som vises i Copilot-vinduet, velger du **Behold den**. 

Det er et **Pålitelighet**-felt som viser poengsummene **Høy (80+)**, **Middels (60-80)** og **Lav (60-)**, og peker deg til linjer som trenger oppmerksomhet.

Dette trinnet bekrefter at du vil overføre linjene til et salgsdokument. Du kan slette eller redigere de overførte linjene der også, eller slette hele dokumentet.

## <a name="see-also"></a>Se også

[Vanlige spørsmål om salgslinjeforslag med Copilot](faq-sales-suggest-sales-lines-with-copilot.md)
[Konfigurer Copilot- og KI-funksjoner](enable-ai.md)
