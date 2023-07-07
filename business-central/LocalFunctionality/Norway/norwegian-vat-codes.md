---
title: Norske mva-koder
description: I den norske versjonen av Business Central kan mva-behandlingsinformasjon enkelt defineres ved hjelp av standard norske mva-koder.
author: SorenGP
ms.topic: conceptual
ms.search.keywords: null
ms.search.form: '10602, 10697, 10698, 10604'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="norwegian-vat-codes"></a>Norske mva-koder

I [!INCLUDE[prod_short](../../includes/prod_short.md)] kan mva-behandlingsinformasjon enkelt defineres ved hjelp av norske standard mva-koder.. Tabellen nedenfor viser norske standard mva-koder.  

|**Kode**|**Beskrivelse**|  
|--------------|-------------------------------------------|  
|**0**|Salg - ingen mva.|  
|**1**|Innkjøp - mva.|  
|**2**|Innkjøp - mva. og inv.avg.|  
|**3**|Salg - mva|  
|**4**|Innkjøp - mva. og 0% lageravg.|  
|**11**|Innkjøp - full mva.|  
|**13**|Salg - full mva.|  
|**14**|Innkjøp - snudd avregning|  

Vanligvis angir du feltet **Mva-bokf.gruppe - firma** og **Mva-bokf.gruppe - vare** når du angir mva-behandlingen.  

Hvis du bare ønsker å bruke **Mva-kode**-feltet når du angir mva-behandlingen, kan du tilordne en mva-kode i **Mva-bokføringsoppsett**-tabellen, og bruke denne koden i stedet for bokføringsgruppefeltene. Mva-koden kan brukes som en snarvei i **Mva-bokføringsoppsett**-tabellen, og du kan bruke norske standard mva-koder samtidig,.  

## <a name="set-up-of-norwegian-vat-codes"></a>Definere norske mva-koder
Du må opprette norske mva-koder på **Mva-koder**-siden. Deretter tilordner du mva-kodene i **Mva-bokføringsoppsett**-tabellen ved hjelp av **Mva-kode**-feltet. Hvis du vil ha mer informasjon, kan du se [Bruke én mva-kode i kladder](how-to-use-one-vat-code-in-journals.md).  

## <a name="use-of-vat-codes"></a>Bruk av mva-koder
Når du angir en mva-kode, kan du velge informasjonen for mva-bokføringsoppsett for denne koden. Denne informasjonen brukes i kladder eller på dokumentlinjer når du angir mva-oppsettsinformasjonen. Hvis du bruker mva-koden i disse tilfellene, brukes bokføringsgruppefeltene med opplysningene fra tilsvarende opplysninger for mva-bokføringsoppsett.  

Eventuelt må du angi både feltet **Mva-bokf.gruppe - firma** og **Mva-bokf.gruppe - vare** når du velger eller endrer informasjon for mva-bokføringsoppsett på kladdelinjen eller dokumentlinjen.  

### <a name="example-using-vat-codes"></a>Eksempel: Bruke mva-koder
Det er to forskjellige forekomster av mva-bokføringsoppsett som kan brukes når du bokfører et salgsdokument.  

Ett scenario for mva-bokføringsoppsett beregner 24 prosent mva for innenlandske kunder:  

- Mva-bokf.gruppe - firma: INNLAND  
- Mva-bokføringsgruppe - vare: NORMAL  
- Mva-%: 24  
- Mva-kode: 3  

Ett scenario for mva-bokføringsoppsett vil beregne uten mva for internasjonale kunder:  

- MVA-bokf.gruppe – firma: EKSPORT  
- Mva-bokføringsgruppe - vare: NORMAL  
- Mva-%: 0  
- Mva-kode: 1  

Vanligvis når du angir mva-oppsettsinformasjon på en kladdelinje, må feltet **Mva-bokf.gruppe - firma** angis til **INNENLANDS** og feltet **Mva-bokf.gruppe - vare** angis til **NORMAL** for å kunne velge det innenlandske oppsettet.  

Hvis du bruker norske standard mva-koder, kan du angi **Mva-kode 3** for den innenlandske mva-bokføringsoppsettsinformasjonen, og **Mva-kode 1** for den internasjonale mva-bokføringsoppsettsinformasjonen. Dermed kan du velge mellom mva-bokføringsoppsettsinformasjonen ved hjelp av bare ett felt og de kjente norske mva-standardkodene.  

### <a name="example-restricting-the-use-of-vat-codes"></a>Eksempel: Begrense bruken av mva-koder
Standard norsk **mva-kode 3** brukes for salg inklusiv mva. Med mindre du begrenser bruken av denne mva-koden, kan den brukes for både salg og kjøp i [!INCLUDE[prod_short](../../includes/prod_short.md)].  

Du kan definere feltet **Bokføringstype** som et salg i **Finanskonto (analysevisning)**-tabellen. Denne generelle bokføringstypen vil brukes sammen med **Mva-kode 3**.  

Bokføringstypen behandles på to måter, avhengig av verdien i feltet **Test bokføringstype**.  

|Alternativ|Description|  
|-----------------------------------------|-------------------------------------------|  
|**Obligatorisk**|Bokføringstypen settes automatisk til **Salg** på kladdelinjer. Før du bokfører, verifiserer [!INCLUDE[prod_short](../../includes/prod_short.md)] om bokføringstypen er angitt, men det er ingen kontroll av om feltet settes til **Salg**.<br /><br /> **Mva-kode 3** kan brukes for både salgs- og kjøpsdokumenter.|  
|**Samme**|Bokføringstypen settes automatisk til **Salg** på kladdelinjer. Før du bokfører verifiserer [!INCLUDE[prod_short](../../includes/prod_short.md)] om bokføringstypen er satt til **Salg**.<br /><br /> **Mva-kode 3** kan brukes for salgsdokumenter, men ikke på kjøpsdokumenter.<br /><br /> Dette gjør det mulig å begrense bruken av mva-koder til forhåndsdefinerte bokføringstyper.|  

## <a name="see-also"></a>Se også
 [Norsk mva-rapportering](norwegian-vat-reporting.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
