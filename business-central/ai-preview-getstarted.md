---
title: Kom i gang med en Business Central-forhåndsversjon for Copilot
description: Forklarer hvordan du får et Business Central-miljø med den nye KI-funksjonen for generering av tekstforslag for vare-/produktbeskrivelser.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 03/16/2023
ms.custom: bap-template
---

# Kom i gang med en Business Central-forhåndsversjon for Copilot

[!INCLUDE[ai-preview](includes/ai-preview.md)]

Du kan prøve varemarkedsføringstekst drevet av kunstig intelligens med Copilot om du er en eksisterende Business Central-kunde eller en potensiell kunde, det vil si noen som bare er interessert i å utforske Business Central og prøve ut den nye funksjonaliteten. For å komme i gang trenger du tilgang til en Business Central online-versjon som støtter den nye funksjonaliteten. Fullfør avsnittet nedenfor som gjelder for deg.

## Organisasjonen bruker allerede Business Central

Som en eksisterende kunde eller partner trenger du en administrator med tilgang til administrasjonssenteret for Business Central for å kunne konfigurere et miljø som kjører forhåndsversjonen som inneholder Copilot. Når miljøet er i gang, kan brukerne prøve ut den nye funksjonen.

Hvis du er miljøadministrator, går du gjennom følgende fremgangsmåte:

1. Logg deg på administrasjonssenteret for Business Central.
2. Velg **Miljøer** > **Opprett**.
3. I ruten **Opprett miljø** angir du et navn på det nye miljøet i feltet **Miljønavn**.
4. Angi **Miljøtype** til **Sandkasse** eller **Produksjon**.
5. Angi **Land** til et land/region i oversikten, men vær oppmerksom på at i forhåndsversjonen er markedsføringsteksten generert av kunstig intelligens fra Copilot bare på engelsk.
6. I **Versjon**-boksen velger du en versjon 22 eller nyere fra listen.

   <!--
   > [!IMPORTANT]
   > You must use **22.0.54157.54311 (Preview - Copilot edition)** to experience Copilot.
   -->
7. Velg **Opprett**.  

Hvis du vil ha mer informasjon om hvordan du oppretter miljøer, går du til [Opprett et miljø](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#create-a-new-environment).

> [!IMPORTANT]
> Hvis du har forhåndsversjonssandkasser som kjører på **22.0.54157.54311 (forhåndsversjon – Copilot-utgave)**, må du være klar over at disse miljøene bare er tilgjengelige frem til 1. mai 2023. Etter denne datoen må du klargjøre et nytt miljø eller oppgradere et hvilket som helst av de andre miljøene til versjon 22.0 eller nyere, for å fortsette å prøve forhåndsversjonen av varemarkedsføringsteksten drevet av kunstig intelligens.

## Organisasjonen bruker ikke Business Central

Hvis du ikke er en Business Central-kunde, registrerer du deg for en prøveversjon for å prøve ut de nye funksjonene for kunstig intelligens. Det er enkelt å registrere seg for prøveversjonen. Du blir veiledet gjennom noen få trinn der du må oppgi informasjon, for eksempel e-postadresse, telefonnummer og navn. Fullfør trinnene nedenfor for å skaffe deg prøveversjonen:

1. Gå til [dette prøvenettstedet](https://go.microsoft.com/fwlink/?linkid=2227167) for å komme i gang med registreringsprosessen.
2. Følg instruksjonene på skjermen.

   Du blir bedt om å oppgi informasjon som e-postadresse, navn og telefonnummer. Den nøyaktige funksjonen kan variere, avhengig av hvilken type informasjon du oppgir. <!--But here are a couple important points to be aware of as you run through the sign-up process:--> Bruk e-postadressen du bruker for jobb eller skole. Vi etablerer prøveversjonen på organisasjonens konto. Du kan ikke bruke e-postadresser oppgitt av forbruker-e-posttjenester eller telekommunikasjonsleverandører, som outlook.com, hotmail.com, gmail.com og andre.
   
   <!-- When you get to the option for **Country or region** be sure to set this **United States**.

      > [!IMPORTANT]
      > You must set **Country or region** to **United States**; otherwise the AI-powered item marketing text with Copilot won't be available in Business Central.  -->
3. Når du kommer til trinnet **Bekreftelsesdetaljer**, er du klar til å starte prøveversjonen.

   - Hvis du vil gå direkte til Business Central, velger du **Hopp over og gå til Dynamics 365 Business Central** > **Kom i gang**.
   - Du har også muligheten til å invitere andre i organisasjonen til prøveversjonen også. Bare skriv inn e-postadresser for hver person, og velg **Send invitasjoner**. Velg **Kom i gang** for å gå til Business Central.  

   Du blir omdirigert til prøveversjonen på [https://businesscentral.dynamics.com/](https://businesscentral.dynamics.com/). Det kan ta flere minutter før prøveversjonen blir klar første gang du logger deg på.

<!--
1. On the **Let's get you started** step, enter your work or school email address, then select **Next**.

   Use your work or school email address. We'll establish your trial on your organization's account. You can't use email addresses provided by consumer email services or telecommunication providers, such as outlook.com, hotmail.com, gmail.com, and others.
3. When asked what kind of email you have, select **I got it from my organization** > **Next**.
4. On the **Create your account** step, you provide information that will help use set up a trial version of Business Central that you can sign in to.

   1. Provide a telephone number that we can use to send you a verification code. Enter a country code and number that isn't VoIP or toll free.
   2. Choose how you want us to send the verification code:
      - Select **Text me** to get the verification code in a text message.
      - Select **Call me** to get the code in a voice message.
   3. Select **Send verification code**. 
   4. When you get the code, type it in the **Enter your verification code** box, then select **Verify**.

      Once you're verified, we'll send you an email with another verification code that you'll use in the next step to complete creating your account.
   5. Fill in your first and last name.
   6. Set **Country or region** to **United States**.

      > [!IMPORTANT]
      > You must set **Country or region** to **United States**; otherwise the AI-powered item marketing text with Copilot won't be available in Business Central.  

   7. Enter a valid phone umber in the **Business telephone number** box.
   8. In the **Create password** and **Confirm password** boxes, enter a password that you want to use to sign in to Business Central. The password must at least eight characters and include at least one number, an uppercase letter, and a lower case letter.
   9. In the **Verification code** box, enter the verification code we sent you in an email, then select **Next**.
   10. When you get a prompt that your account is successfully created, select **Sign in**.
-->

4. Når du er logget på, ser du startsiden for Business Central, som kalles rollesenteret, som ligner på følgende figur:

   [![Viser rollesenteret for Business Central og sjekklisten for Copilot](media/copilot-checklist.png)](media/copilot-checklist.png#lightbox)

5. Hvis du vil ha en veiledende innføring i å opprette en varemarkedsføringstekst drevet av kunstig intelligens med Copilot, velger du **Opprett med Copilot** > **Start innføring** nesten øverst på siden under **Sjekklisten**. Følg deretter instruksjonene på skjermen.

   > [!TIP]
   > Hvis du ikke ser **Sjekklisten**, velger du knappen **Vis demoinnføringer** først.

## Neste trinn

KI-funksjonene som leveres av Copilot, må være aktivert før du eller andre kan bruke Copilot. Hvis du vil aktivere KI-funksjonene, må en administrator samtykke i vilkårene for [forhåndsversjonen](https://dynamics.microsoft.com/legaldocs/supp-dynamics365-preview/) og [Microsofts personvernerklæring](https://go.microsoft.com/fwlink/?LinkId=521839) på vegne av organisasjonen.

> [!NOTE]
> Hvis du bruker en prøveversjon, er du administratoren. Hvis du har invitert andre personer i organisasjonen til prøveversjonen under registreringen, kan de ikke bruke Copilot før du godtar vilkårene.

Det finnes to måter å samtykke på som administrator:

- Den enkleste måten er å bruke Copilot. Første gang du bruker Copilot som administrator, blir du bedt om å se gjennom vilkårene og deretter samtykke eller avslå. Hvis du vil lære hvordan du bruker Copilot, går du til [Legg til markedsføringstekst i varer](item-marketing-text.md).  

- Den andre måten er å bruke **statussiden for personvernerklæringer** i Business Central og godta Azure-integrasjonen **OpenAI** for alle brukere. Hvis du vil finne ut mer, går du til [Samtykk i vilkår](enable-ai.md#consent-to-or-reject-preview-and-privacy-terms-and-conditions-for-all-users).

## Se også

[Oversikt over varemarkedsføringstekst drevet av kunstig intelligens med Copilot](ai-overview.md)  
[Konfigurer varemarkedsføringstekst drevet av kunstig intelligens med Copilot som administrator](enable-ai.md)  
[Opprett markedsføringstekst til varer ved hjelp av Copilot](item-marketing-text.md)  
[Vanlige spørsmål om varemarkedsføringstekst drevet av kunstig intelligens (forhåndsversjon) med Copilot](ai-faq.md)  