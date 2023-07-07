---
title: Konfigurere sending og mottak av elektroniske dokumenter | Microsoft-dokumentasjon
description: 'Som et alternativ til å sende forretningsdokumenter som filvedlegg via e-post, kan du sende og motta dem elektronisk.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="set-up-electronic-document-sending-and-receiving"></a>Konfigurere sending og mottak av elektroniske dokumenter

Som et alternativ til å sende forretningsdokumenter som filvedlegg via e-post, kan du sende og motta dem elektronisk. Med elektronisk dokument menes en standard\-kompatibel fil som representerer et forretningsdokument, for eksempel en faktura fra en leverandør som kan mottas og konverteres til en kjøpsfaktura i [!INCLUDE[prod_short](includes/prod_short.md)]. Utvekslingen av elektroniske dokumenter mellom to handelspartnere uføres ved hjelp av en ekstern leverandør av dokumentutvekslingstjenester. Den generelle versjonen av [!INCLUDE[prod_short](includes/prod_short.md)] kan sende og motta elektroniske fakturaer og kreditnotaer i PEPPOL-format, som støttes av de største leverandørene av dokumentutvekslingstjenester. En større leverandør av dokumentutvekslingstjenester er forhåndskonfigurert og klar til å bli definert for firmaet.  

Fra PDF- eller bildefiler som representerer inngående dokumenter, kan du få en ekstern OCR-tjeneste (optisk tegngjenkjenning) til å opprette elektroniske dokumenter som du deretter kan konvertere til dokumentposter i [!INCLUDE[prod_short](includes/prod_short.md)], på samme måte som for elektroniske PEPPOL-dokumenter. Når du for eksempel mottar en faktura i PDF-format fra leverandøren, kan du sende den til OCR-tjenesten fra siden **Inngående dokumenter**. Etter noen få sekunder får du filen tilbake som en elektronisk faktura som kan konverteres til en kjøpsfaktura for leverandøren. Hvis du sender filen til OCR-tjenesten via e-post, opprettes deretter en ny post for inngående dokument automatisk når du får det elektroniske dokumentet tilbake.  

Det elektroniske dokumentformatet **PEPPOL** er forhåndskonfigurert, slik at du kan sende elektroniske fakturaer og kreditnotaer i PEPPOL-formatet. Først må du definere forskjellige hoveddata, for eksempel firmainformasjon, kunder, varer og enheter. Disse brukes til å identifisere forretningspartnere og elementer ved konvertering av data i feltene i [!INCLUDE[prod_short](includes/prod_short.md)] til elementene i den utgående dokumentfilen. Til slutt må du velge formatet på siden **Elektronisk dokumentformat** for hver kunde du vil sende elektroniske PEPPOL-dokumenter til. Hvis du vil ha mer informasjon, kan du se [Sende elektroniske dokumenter](sales-how-to-send-electronic-documents.md).  

Datautvekslingsdefinisjonene **PEPPOL – faktura** og **PEPPOL – kreditnota** er forhåndskonfigurert, slik at du kan motta elektroniske fakturaer og kreditnotaer i PEPPO-formatet. Først må du definere forskjellige hoveddata, for eksempel firmainformasjon, leverandører, varer og enheter. Disse brukes til å identifisere forretningspartnere og elementer ved konvertering av data i elementer i den innkommende dokumentfilen til felt i [!INCLUDE[prod_short](includes/prod_short.md)]. Til slutt må du velge datautvekslingsdefinisjonen på siden **Innkommende dokumenter** for hvert innkommende elektroniske dokument som du vil konvertere til et kjøpsdokument i [!INCLUDE[prod_short](includes/prod_short.md)].  

Datautvekslingsdefinisjonen **OCR – faktura** er forhåndskonfigurert slik at du kan motta elektroniske dokumenter som genereres av OCR-tjenesten. Hvis du for eksempel vil motta en faktura som et elektronisk OCR-dokument, definerer du hoveddato og behandler deretter dokumentet som når du mottar et elektronisk PEPPOL-dokument. Hvis du vil ha mer informasjon, kan du se [Bruke OCR til å konvertere PDF- og bildefiler til elektroniske dokumenter](across-how-use-ocr-pdf-images-files.md).  

De forhåndskonfigurerte tjenestene for dokumentutveksling og OCR må være aktivert før du sender eller mottar. Hvis du vil ha mer informasjon, kan du se [Konfigurere en dokumentutvekslingstjeneste](across-how-to-set-up-a-document-exchange-service.md).  

Dette emnet inneholder følgende fremgangsmåter:  

* Slik konfigurerer du selskapet for sending og mottak av elektroniske dokumenter  
* Slik konfigurerer du mva-bokføring for sending og mottak av elektroniske dokumenter  
* Slik konfigurerer du land/områder for sending og mottak av elektroniske dokumenter  
* Slik konfigurerer du varer for sending og mottak av elektroniske dokumenter  
* Slik konfigurerer du enheter for sending og mottak av elektroniske dokumenter  
* Slik konfigurerer du kunder for sending og mottak av elektroniske dokumenter  
* Slik velger du det elektroniske **PEPPOL**-dokumentformat for sending av elektroniske dokumenter  
* Slik konfigurerer du leverandører for mottak av elektroniske dokumenter  
* Slik velger du datautvekslingsdefinisjonen **PEPPOL – faktura** for mottak av elektroniske dokumenter  
* Slik konfigurerer du finanskontoen til bruk på nye kjøpsfakturalinjer for ikke\--identifiserbare varer og elementer \-som ikke er varer  

### <a name="to-set-up-the-company-for-electronic-document-sending-and-receiving"></a>Slik konfigurerer du selskapet for sending og mottak av elektroniske dokumenter

1. Skriv inn **Selskapsinformasjon** i **Søk**-boksen, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene som beskrevet i tabellen nedenfor, i hurtigfanen **Generelt**.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**GLN**|Identifisere firmaet.<br /><br /> Når du for eksempel sender elektroniske fakturaer i PEPPOL-formatet, brukes verdien i dette feltet til å fylle ut **EndPointID**-elementet under **AccountingSupplierParty**-noden i filen. Nummeret er basert på GS1-standarden, som er i samsvar med ISO-6523.|  
    |**Organisasjonsnr.**|Angi firmaets organisasjonsnummer.|  
    |**Ansvarssenter**|Hvis firmaet er konfigurert med et ansvarssenter, må du kontrollere at feltet **Lands-/regionskode** er fylt ut.|  

### <a name="to-set-up-vat-posting-for-electronic-document-sending-and-receiving"></a>Slik konfigurerer du mva-bokføring for sending og mottak av elektroniske dokumenter

1. Skriv inn **Mva-bokføringsoppsett** i **Søk**-boksen, og velg deretter den relaterte koblingen.  
2. Fylle ut feltet som beskrevet i tabellen nedenfor, for alle mva-bokføringsoppsett som skal brukes for elektroniske dokumenter.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Avgiftskategori**|Angi mva-kategorien.<br /><br /> Når du for eksempel sender elektroniske fakturaer i PEPPOL-formatet, brukes verdien i dette feltet til å fylle ut **TaxApplied**-elementet under **AccountingSupplierParty**-noden i filen. Nummeret er basert på UNCL5305-standarden.|  

### <a name="to-set-up-countriesregions-for-electronic-document-sending-and-receiving"></a>Slik konfigurerer du land/områder for sending og mottak av elektroniske dokumenter

1. Skriv inn **Land/områder** i **Søk**-boksen, og velg deretter den relaterte koblingen.  
2. Fylle ut feltet som beskrevet i tabellen nedenfor, for alle land/områder som skal utveksle elektroniske dokumenter med.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**MVA-skjema**|Identifisere det nasjonale organet som utsteder organisasjonsnummeret for landet\/området i forbindelse med sending av elektroniske dokumenter.<br /><br /> Når du for eksempel sender elektroniske fakturaer i PEPPOL-formatet, brukes verdien i dette feltet til å fylle ut **SchemeID**-attributtet for **EndPointID**-elementet under **AccountingSupplierParty**-noden og **AccountingCustomerParty** i filen.<br /><br /> Feltet **MVA-skjema** brukes bare hvis feltet **GLN** på siden **Selskapsopplysninger** ikke er fylt ut. **Obs!**  Verdien i feltet **Kode** på siden **Land\/regioner** må være i overensstemmelse med ISO 3166\-1:Alpha2.|  

### <a name="to-set-up-items-for-electronic-document-sending-and-receiving"></a>Slik konfigurerer du varer for sending og mottak av elektroniske dokumenter

1. Skriv inn **Varer** i **Søk**-boksen, og velg deretter den relaterte koblingen.  
2. Fylle ut feltet som beskrevet i tabellen nedenfor, for alle varer som du kjøper eller selger med elektroniske dokumenter.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**GTIN**|Identifiserer elementet i forbindelse med sending og mottak av elektroniske dokumenter. For PEPPOL-format brukes feltet slik:<br /><br /> Hvis **StandardItemIdentification\/ID**-elementet har **SchemeID**-attributtet satt til **GTIN**, blir elementet deretter tilordnet feltet **GTIN** på varekortet.|  

### <a name="to-set-up-units-of-measure-for-electronic-document-sending-and-receiving"></a>Slik konfigurerer du enheter for sending og mottak av elektroniske dokumenter

1. Skriv inn **Enheter** i **Søk**-boksen, og velg deretter den relaterte koblingen.  
2. Fylle ut feltet som beskrevet i tabellen nedenfor, for alle enheter som skal brukes for varer i elektroniske dokumenter.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Internasjonal standardkode**|Angi enhetskode som uttrykt i henhold til UNECERec20, som er standard i forbindelse med sending av elektroniske dokumenter.<br /><br /> Når du for eksempel sender elektroniske fakturaer i PEPPOL-formatet, brukes verdien i dette feltet til å fylle ut **unitCode**-attributtet for **InvoicedQuantity**-elementet under **InvoiceLine**-noden. **Obs!**  Hvis feltet **Enhet** på salgslinjen er tomt, blir standardverdien for UNECERe20 for "Del" \(H87\) satt inn som standard. Hvis du vil ha mer informasjon og en liste over gyldige enhetskoder, kan du se [Anbefaling Nr. 20 \- enheter som brukes i internasjonal handel](https://www.unece.org/fileadmin/DAM/cefact/recommendations/rec20/rec20_rev3_Annex2e.pdf).|  

### <a name="to-set-up-customers-for-electronic-document-sending"></a>Slik konfigurerer du kunder for sending og mottak av elektroniske dokumenter

1. Skriv inn **Kunder** i **Søk**-boksen, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene som beskrevet i tabellen nedenfor, for alle kunder som du skal sende elektroniske dokumenter til.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**GLN**|Identifisere kunden.<br /><br /> Når du for eksempel sender elektroniske fakturaer i PEPPOL-formatet, brukes verdien i dette feltet til å fylle ut **EndPointID**-elementet under **AccountingCustomerParty**-noden i filen. Nummeret er basert på GS1-standarden, som er i samsvar med ISO-6523.<br /><br /> Hvis feltet **GLN** er tomt, brukes verdien i feltet **Organisasjonsnr.**.|  
    |**Organisasjonsnr.**|Angi kundens organisasjonsnummer. **Tips** I støttede lokaliserte versjoner velger du DrillDown-knappen for å bruke webtjenesten som kontrollerer om nummeret finnes i det nasjonale selskapsregisteret.|  
    |**Ansvarssenter**|Hvis kunden er konfigurert med et ansvarssenter, må du kontrollere at feltet **Lands-/regionskode** er fylt ut.|  

    Du kan definere hver kunde med en foretrukket metode for sending av forretningsdokumenter, slik at du ikke trenger å velge et alternativ for sending hver gang du sender et dokument til kunden. Hvis du vil ha mer informasjon, kan du se [Definere en profil for dokumentsending](sales-how-setup-document-send-profiles.md).  

### <a name="to-select-the-peppol-electronic-document-format-for-electronic-document-sending"></a>Slik velger du det elektroniske PEPPOL-dokumentformat for sending av elektroniske dokumenter
1. Skriv inn **Profiler for dokumentsending** i **Søk**-boksen, og velg deretter den tilknyttede koblingen.  
2. Åpne et eksisterende dokument, sende profilen, eller opprette en ny. Hvis du vil ha mer informasjon, kan du se [Definere en profil for dokumentsending](sales-how-setup-document-send-profiles.md).  
3. På siden **Profil for dokumentsending** velger du **Elektronisk format**, velger linjen for PEPPOL og velger deretter **OK**.  
4. I feltet **Elektronisk dokument** velger du **Ja (Gjennom dokumentutvekslingstjeneste)**.  

    > [!NOTE]  
    >  [!INCLUDE[prod_short](includes/prod_short.md)] oppdager automatisk om dokumentet er en faktura eller kreditnota, og bruker PEPPOL-formatet i henhold til dette.  

5. Hvis du vil angi at denne profilen for dokumentsending skal gjelde for alle kunder, merker du av for **Standard** i hurtigfanen **Generelt**. Hvis du vil gjøre det gjeldende bare for bestemte kunder, kan du fylle ut feltet **Profil for dokumentsending** på de aktuelle kundekortene. Hvis du vil ha mer informasjon, kan du se [Definere en profil for dokumentsending](sales-how-setup-document-send-profiles.md).  

    Du kan nå sende det elektroniske dokumentet med konverterte data. Hvis du vil ha mer informasjon, kan du se [Sende elektroniske dokumenter](sales-how-to-send-electronic-documents.md).  

### <a name="to-set-up-vendors-for-electronic-document-receiving"></a>Slik konfigurerer du leverandører for mottak av elektroniske dokumenter
1. Skriv inn **Leverandører** i **Søk**-boksen, og velg deretter den relaterte koblingen.  
2. Fylle ut feltene som beskrevet i tabellen nedenfor, for alle leverand;rer som du skal motta elektroniske dokumenter fra.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**GLN**|Identifisere leverandøren.<br /><br /> Når du for eksempel mottar elektroniske fakturaer i PEPPOL-formatet, brukes verdien i dette feltet til å fylle ut **EndPointID**-elementet under **AccountingSupplierParty**-noden i filen. Nummeret er basert på GS1-standarden, som er i samsvar med ISO-6523.<br /><br /> Hvis feltet **GLN** er tomt, brukes verdien i feltet **Organisasjonsnr.**.|  
    |**Organisasjonsnr.**|Angi leverandørens organisasjonsnummer. **Tips** I støttede lokaliserte versjoner velger du DrillDown-knappen for å bruke webtjenesten som kontrollerer om nummeret finnes i det nasjonale selskapsregisteret.|  
    |**Ansvarssenter**|Hvis leverandøren er konfigurert med et ansvarssenter, må du kontrollere at feltet **Lands-/regionskode** er fylt ut.|  

### <a name="to-select-the-peppol---invoice-data-exchange-definition-for-electronic-document-receiving"></a>Slik velger du datautvekslingsdefinisjonen PEPPOL – faktura for mottak av elektroniske dokumenter
1. Skriv inn **Innkommende dokumenter** i **Søk**-boksen, og velg deretter den relaterte koblingen.  
2. På linjen for det elektroniske dokumentet som du vil motta og konvertere, velger du feltet **Datautvekslingstype**, og deretter velger du **PEPPOLINVOICE**.  

     Hvis dokumentet du skal motta, er en kreditnota, velger du **PEPPOLCREDITMEMO**.  

    Du kan nå motta det elektroniske dokumentet ved å starte datakonverteringsprosessen på siden **Inngående dokumenter**. Hvis du vil ha mer informasjon, kan du se [Motta og konvertere elektroniske dokumenter](purchasing-how-to-receive-and-convert-electronic-documents.md).  

### <a name="to-set-up-the-gl-account-to-use-on-new-purchase-invoice-lines-for-non-identifiable-items-and-non-items"></a>Slik konfigurerer du finanskontoen til bruk på nye kjøpsfakturalinjer for ikke-identifiserbare varer og elementer som ikke er varer
1. Skriv inn **Kjøpsoppsett** i **Søk**-boksen, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene som beskrevet i tabellen nedenfor, i hurtigfanen **Standardkontoer** .  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Finanskonto for linjer som ikke er varer**|Angir finanskontoen som settes automatisk inn på bestillingslinjer som er opprettet fra elektroniske dokumenter, når den innkommende dokumentlinjen ikke inneholder et element kan identifiseres. Alle inngående dokumentlinjer som ikke har en GTIN eller leverandørens varenummer, skal konverteres til en bestillingslinje av typen **Finanskonto**, og feltet **Nr.** på bestillingslinjen vil inneholde kontoen du velger i feltet **Finanskonto for linjer som ikke er varer**.<br /><br /> Hvis du lar feltet **Finanskonto for linjer som ikke er varer** stå tomt, og det inngående dokumentet har linjer uten identifiserbare varer, blir ikke kjøpsdokumentet opprettet. En feilmelding ber deg om å fylle ut feltet **Finanskonto for linjer som ikke er varer** før du kan fullføre oppgaven.|  

## <a name="see-related-microsoft-training"></a>Se relatert [Microsoft-opplæring](/training/modules/electronic-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også
[Utveksle data elektronisk](across-data-exchange.md)   
[Fakturere salg](sales-how-invoice-sales.md)   
[Registrere kjøp](purchasing-how-record-purchases.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
