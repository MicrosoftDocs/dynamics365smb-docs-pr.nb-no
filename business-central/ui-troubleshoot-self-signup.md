---
title: Feilsøke registrering for Self-Service | Microsoft-dokumentasjon
description: Finn ut mer om de vanligste årsakene til at du kanskje ikke kan fullføre registreringen for Business Central og hvordan du kan løse dem.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="troubleshooting-self-service-sign-up"></a>Feilsøke registrering for Self-Service
Registrering for [!INCLUDE[prod_short](includes/prod_short.md)] er enkelt og kan gjøres svært raskt. Du kan opprette en gratis konto selv om du er en eksisterende organisasjon. Denne artikkelen beskriver problemer som kan oppstå under registrering.

## <a name="what-email-address-can-i-use-with-business-central"></a>Hvilken e-postadresse kan jeg bruke med Business Central?
[!INCLUDE[prod_short](includes/prod_short.md)] krever at du bruker en e-postadresse for arbeid eller skole for å registrere deg. [!INCLUDE[prod_short](includes/prod_short.md)] støtter ikke e-postadressene levert av e-posttjenester for forbrukere eller telekommunikasjonsleverandører. Dette inkluderer outlook.com, hotmail.com, gmail.com og andre.

Hvis du prøver å registrere deg med en personlig e-postadresse, får du en melding om å bruke en e-postadresse for arbeid eller skole.

## <a name="troubleshooting"></a>Feilsøking
I mange tilfeller kan du registrere deg for [!INCLUDE[prod_short](includes/prod_short.md)] ved å følge registreringsprosessen nedenfor. Det er imidlertid flere grunner til hvorfor du ikke kanskje ikke kan fullføre registrering for Self-Service. Tabellen nedenfor viser en oversikt over noen av de vanligste årsakene som du ikke kanskje kan fullføre registreringen og metoder for midlertidig løsning av disse problemene.

| Symptom/feilmelding | Årsak og løsning |
| --------------------- | -------------------- |
| For e-postadresser for Microsoft 365 som ikke er registrert i et land som støttes, kan du få en melding som følgende, under registrering:<br /><br />**Dette fungerte ikke. Vi støtter ikke landet eller området ennå.** |[!INCLUDE[prod_short](includes/prod_short.md)] støtter for øyeblikket bare e-postkontoer for Microsoft 365 som er registrert i et begrenset antall markeder. Hvis du vil ha mer informasjon, kan du se [Tilgjengelighet i områder](#regional-availability). |
| Personlige e-postadresser, som nancy@gmail.com, støttes ikke. Du får en feilmelding som følgende, under registrering:<br /><br />**Du har angitt en personlig e-postadresse: Skriv inn e-postadressen for arbeid, slik at vi kan lagre firmaets data på en sikker måte.**<br> eller <br> **Dette ser ut som en personlig e-postadresse. Skriv inn adressen til arbeid, slik at vi kan koble til andre i firmaet. Og ikke bekymre deg. Vi deler ikke adressen din med andre.** |[!INCLUDE[prod_short](includes/prod_short.md)] støtter ikke e-postadressene levert av e-posttjenester for forbrukere eller telekommunikasjonsleverandører. Hvis du vil fullføre registreringen, kan du prøve på nytt med en e-postadresse som er tilordnet arbeid eller skole. Hvis du fremdeles ikke kan registrere deg og er villig til å fullføre et mer avansert oppsett, kan du registrere for et nytt prøveabonnement for Microsoft 365 og bruke den e-postadressen til å registrere deg. |
| .gov- eller .mil e-postadresser Du mottar en melding som følgende, under registrering:<br /><br />**[!INCLUDE[prod_short](includes/prod_short.md)] ikke tilgjengelig: [!INCLUDE[prod_short](includes/prod_short.md)] er ikke tilgjengelig for brukere med e-postadressene .gov eller .mil på dette tidspunktet. Bruk en annen e-postadresse for arbeid eller kom tilbake senere.** <br>eller <br>**Vi kan ikke fullføre registreringen din. Det ser ut som [!INCLUDE[prod_short](includes/prod_short.md)] ikke er tilgjengelig for arbeid eller skole.** |[!INCLUDE[prod_short](includes/prod_short.md)] støtter ikke .gov- eller .mil-adresser på dette tidspunktet. |
| Registrering for Self-service er ikke aktivert. Du får en feilmelding som følgende, under registrering:<br /><br />**Vi kan ikke fullføre registreringen din. IT-avdelingen har deaktivert registrering for [!INCLUDE[prod_short](includes/prod_short.md)]. Kontakt dem for å fullføre registreringen.** <br>eller <br> **Dette ser ut som en personlig e-postadresse. Skriv inn adressen til arbeid, slik at vi kan koble til andre i firmaet. Og ikke bekymre deg. Vi deler ikke adressen din med andre.** |Organisasjonens systemansvarlige har deaktivert registrering for Self-service for [!INCLUDE[prod_short](includes/prod_short.md)]. Hvis du vil fullføre registreringen, kontakter du systemansvarlig og ber om å følge instruksjonene på [denne siden](/dynamics365/business-central/dev-itpro/developer/devenv-business-central-manage-selfservice-signups), slik at eksisterende brukere kan registrere seg for [!INCLUDE[prod_short](includes/prod_short.md)] og nye brukere kan bli med i eksisterende leietaker. Du kan også oppleve dette problemet hvis du registrerte deg for Microsoft 365 via en partner. |
| E-postadressen er ikke en Microsoft 365-ID. Du får en feilmelding som følgende, under registrering:<br /><br />**Vi finner deg ikke på contoso.com. Bruker du en annen ID på arbeid eller skole? Prøv å logge på med denne, og hvis det ikke fungerer, kan du kontakte IT-avdelingen.** |Organisasjonen din bruker ID-er til å logge på Microsoft 365 og andre Microsoft-tjenester, som er forskjellig fra e-postadressen din. E-postadressen din kan for eksempel være Nancy.Smith@contoso.com, men ID-en er nancys@contoso.com. Hvis du vil fullføre registreringen, kan du bruke ID-en som organisasjonen har tilordnet for å logge på Microsoft 365 eller andre Microsoft-tjenester. Hvis du ikke vet hva dette er, kontakter du systemansvarlig. Hvis du fremdeles ikke kan registrere deg og kan fullføre et mer avansert oppsett, kan du registrere for et nytt prøveabonnement for Microsoft 365 og bruke den e-postadressen til å registrere deg. |
| Hvis Microsoft 365-kontoen er registrert i et land som støttes og du registrerer deg for [!INCLUDE[prod_short](includes/prod_short.md)] når du er i et annet land, vises en melding under registreringen:<br /><br />**Dette fungerte ikke. Vi støtter ikke landet eller området ennå.**| Organisasjonens Microsoft 365-abonnement er registrert i et bestemt land i administrasjonsportalen for Microsoft 365. Registreringsopplevelsen for [!INCLUDE[prod_short](includes/prod_short.md)] bruker språket og de nasjonale innstillingene som gjeldende nettleser bruker, og derfor kan du få du feilmelding selv om du er i et land som støttes. Be IT-ansvarlig om å kontrollere landet som er angitt i organisasjonsprofilen i [Microsoft 365-administrasjonsportalen](https://portal.office.com/adminportal/home#/companyprofile). Det kan hende du må bruke en annen konto for [!INCLUDE[prod_short](includes/prod_short.md)].|

## <a name="regional-availability"></a>Tilgjengelighet i området

[!INCLUDE[prod_short](includes/prod_short.md)] er tilgjengelig i flere land eller områder med lokalisering gitt av Microsoft eller en godkjent lokaliseringspartner. Hvis du vil se hele oversikten over støttede land og regioner, kan du se [Land-/områdetilgjengelighet og støttede oversettelser](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json).  

For en oversikt over markeder som støttes på tvers av Dynamics 365, kan du se [Internasjonal tilgjengelighet for Microsoft Dynamics 365](/dynamics365/get-started/availability). For en oversikt over lokal funksjonalitet i [!INCLUDE[prod_short](includes/prod_short.md)], se [Lokal funksjonalitet](about-localization.md)-målsiden.  

## <a name="see-also"></a>Se også

[Registrer deg for en Dynamics 365 Business Central-prøveversjon](trial-signup.md)  
[Vanlige spørsmål om prøversjonen av Dynamics 365 Business Central](trial-faq.md)  
[Velkommen til [!INCLUDE[prod_short](includes/prod_long.md)]](welcome.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Lokal funksjonalitet](about-localization.md)  
[Land-/områdetilgjengelighet og støttede oversettelser](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json)  
[Internasjonal tilgjengelighet for Microsoft Dynamics 365](/dynamics365/get-started/availability)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
