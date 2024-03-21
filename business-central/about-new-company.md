---
title: Opprett nye selskaper med en automatisk oppsettguide
description: 'Det er enkelt å opprette et nytt, tomt selskap i Business Central. En guide for assistert oppsett hjelper deg gjennom trinnene, og du kan importere forretningsdataene.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 04/14/2023
ms.custom: bap-template
ms.search.keywords: 'company, setup wizard'
ms.search.form: '1803, 9020, 9022, 9026, 9027, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017'
ms.service: dynamics-365-business-central
---
# <a name="create-new-companies-in-"></a>Opprett nye selskaper i [!INCLUDE[prod_short](includes/prod_short.md)]

I [!INCLUDE[prod_short](includes/prod_short.md)] kalles beholderen for forretningsdataene som hører til en konsern eller juridisk enhet et *selskap*. Når du registrerer deg for [!INCLUDE[prod_short](includes/prod_short.md)], får du et demoselskap og et tomt selskap, *Mitt selskap*. Bytte mellom selskaper er enkelt: simpelthen gå til **Mine innstillinger**, og bytt til det andre selskapet. Du kan også opprette nye selskaper i [!INCLUDE[prod_short](includes/prod_short.md)], avhengig av forretningsbehovene.  

> [!NOTE]
> Hvis du vil opprette et nytt selskap, må du være tildelt tillatelsessettet **Super**.

Når du oppretter et nytt selskap, gir en guide for assistert oppsett deg det grunnleggende. Deretter kan du importere aktuelle data fra det gamle systemet eller et annet selskap i [!INCLUDE[prod_short](includes/prod_short.md)].  

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

## <a name="choose-the-right-template"></a>Velg riktig mal

Hvis du vil legge til et selskap til din [!INCLUDE[prod_short](includes/prod_short.md)], kan du bruke den assisterte oppsettsveiledningen **Opprett nytt selskap** for å komme i gang. Oppsettsveiledningen er tilgjengelig fra **Selskaper**-siden og fra oppslaget i **Selskap**-feltet på siden **Mine innstillinger**.  

Oppsettsveiledningen har to maler og et tomt alternativ:

- **Evaluering – eksempeldata**  
    Dette oppretter et selskap som ligner på demoselskapet, med eksempeldata og oppsettsdata. Denne typen selskap er tilgjengelig for deg uten å bytte til en 30-dagers prøveperiode, som de andre typene har.  
- **Produksjon - bare oppsettsdata**  
    Dette oppretter et selskap som ligner på **Mitt selskap**, med oppsettsdata, men uten eksempeldata. Du kan bruke dette selskapet i en 30-dagers prøveperiode.  
- **Opprett nytt- ingen data**  
    Dette oppretter et tomt selskap uten oppsettsdata. Du kan bruke dette selskapet i en 30-dagers prøveperiode.  

Hvis du ønsker å begynne med et nytt selskap, må du velge **Produksjon - Bare oppsettsdata** og deretter importere egne forretningsdata, for eksempel kunder, varer og leverandører. Velg **Ny**-malen hvis du vil definere alt fra begynnelsen. I så fall kan du bruke veiviseren **Selskapsoppsett** med assistert oppsettsveiledning for å komme i gang med grunnleggende oppsettsdata.  

> [!NOTE]  
> Når du oppretter et nytt selskap, tar litt tid før du kan bruke det i [!INCLUDE[prod_short](includes/prod_short.md)]. Statusen for oppsettet på siden **Selskaper** viser når det nye selskapet er klart. Deretter du kan bytte til et nytt selskap ved hjelp av **Mine innstillinger**.  

Du kan opprette så mange nye selskaper under 30 dagers prøveperioden, men de er bare tilgjengelige under prøveperioden. Ta kontakt med din [!INCLUDE[prod_short](includes/prod_short.md)]-partner for mer informasjon. Se også artikkelen [Vanlige spørsmål om prøveversjonen av Dynamics 365 Business Central](trial-faq.md).  

Administratoren kan finne ut mer om prøveversjoner og abonnementer [her](/dynamics365/business-central/dev-itpro/administration/trials-subscriptions).  

## <a name="copy-a-company"></a>Kopier et selskap

På siden **Selskaper** kan du bruke **Kopier**-handlingen til å opprette et annet selskap basert på innholdet i et eksisterende selskap. Dette er for eksempel nyttig når du vil teste et selskap uten å forstyrre produksjonsdata.

> [!Important]
> Ikke bruk kopieringshandlingen til å ta en sikkerhetskopi av et selskap. Hvis du vil ta en sikkerhetskopi, begynner du ved å eksportere databasen som en bacpac-fil. Hvis du vil ha mer informasjon, kan du se [Eksportere databaser](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-database-export) i hjelpen for utvikling og administrasjon.

[!INCLUDE [email-copy-company](includes/email-copy-company.md)]

## <a name="set-up-the-company"></a>Konfigurer selskapet

Når du logger deg på et nytt selskap, kjøres veiviseren **Selskapsoppsett** automatisk og hjelper deg med å komme i gang. Du blir bedt om informasjon om selskapet, for eksempel adressen, bankdetaljer og lagerkostmetoden. Vi ber om opplysningene fordi de brukes som grunnlag for mange områder i [!INCLUDE[prod_short](includes/prod_short.md)], som du ikke kan definere senere manuelt.  

[!INCLUDE [prod_short](includes/prod_short.md)] omfatter for eksempel selskapsadressen i fakturaer og andre dokumenter og bankinformasjonen i betalinger. Etterkalkuleringsmetoden brukes til å beregne priser og lagerverdisetting.  

Når du har det grunnleggende på plass, kan du definere gjenstående kjerneområder. Deretter er du klar til å legge til forretningsdataene, for eksempel kunder og leverandører. Hvis du vil ha mer informasjon, kan du se [Konfigurer [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md).  

## <a name="companies-and-environments"></a>Selskaper og miljøer

[!INCLUDE [company_environment](includes/company_environment.md)]

Hvis du vil ha mer informasjon, kan du se [Bytte til et annet selskap eller miljø](ui-organization-switch.md). Hvis du vil ha mer informasjon om miljøer, kan du se [Forstå infrastrukturen til Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-environment-topology) (bare på engelsk).  

## <a name="changing-a-companys-name"></a>Endre et selskaps navn

Når et selskap er opprettet, kan du ikke endre navnet på det. Du kan imidlertid endre **visningsnavnet**, som er tekst som skal vises for selskapet i programmet.  

> [!TIP]
> Du kan gi et selskap nytt navn hvis du bruker [!INCLUDE[prod_short](includes/prod_short.md)] lokalt.

## <a name="add-contoso-coffee"></a>Legg til Contoso Coffee

Contoso Coffee-appen tilbyr demonstrasjonsdata som kan hjelpe deg med å finne avanserte funksjoner i [!INCLUDE [prod_short](includes/prod_short.md)]. Finn appen i AppSource, og installer den i et tomt selskap, for eksempel et selskap i et sandkassemiljø. Hvis du vil ha mer informasjon, kan du se [Innføring i demodata for Contoso Coffee](contoso-coffee/contoso-coffee-intro.md).  

## <a name="see-also"></a>Se også

[Tilpasse Business Central](ui-customizing-overview.md)  
[Konfigurere [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Importer forretningsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Endre grunnleggende innstillinger](ui-change-basic-settings.md)  
[Bli klar til å gjøre forretninger](ui-get-ready-business.md)  
[Forstå infrastrukturen til Business Central Online (bare på engelsk)](/dynamics365/business-central/dev-itpro/administration/tenant-environment-topology)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
