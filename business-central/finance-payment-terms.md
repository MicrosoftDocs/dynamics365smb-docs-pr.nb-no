---
title: Konfigurer betalingsbetingelser
description: Bruk betalingsbetingelser til å administrere forfallsdatoer og kontantrabatter.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.form: '4,'
ms.date: 06/13/2024
ms.service: dynamics-365-business-central
---
# Konfigurer betalingsbetingelser

Betalingsbetingelser bestemmer hvordan du håndterer forfallsdatoer og kontantrabatter. Du kan bruke datoformler til å definere betalingsbetingelsene. Når du først registrerer deg for [!INCLUDE [prod_short](includes/prod_short.md)], gir demonstrasjonsselskapet noen betalingsmåter som virksomheter ofte bruker. Du kan imidlertid legge til så mange du trenger.  

Hvis du knytte betalingsbetingelser til kunder og leverandører, brukes de samme betingelsene alltid på salgs- og kjøpsdokumenter du oppretter for dem. Det er dokumentdatoene på salgs- og kjøpsdokumentene, ikke bokføringsdatoene for betalingene, som brukes til å beregne forfallsdatoer for betalinger. Hvis det er nødvendig, kan du endre betingelsene på salgs- eller kjøpsdokumentet. Hvis du for eksempel vil at en bestemt kunde skal betale deg innen 7 dager i stedet for standard 14 dager. Selv om du endrer betingelsene i dokumentet, endres ikke standard betalingsbetingelse som er tildelt kunden. Samme betalingsbetingelser er tilgjengelige for salgs- og kjøpsdokumenter.

Når du bokfører en faktura, beregner [!INCLUDE [prod_short](includes/prod_short.md)] kontantrabatten på grunnlag av betalingsbetingelsene. Datoen for kontantrabatten er den siste datoen som kunden kan motta en rabatt på. Datoen beregnes også når du bokfører en faktura.  

Når du bokfører en kreditnota, beregner [!INCLUDE [prod_short](includes/prod_short.md)] kontantrabatter på bakgrunn av betalingsbetingelsene. Den beregner rabatten på kreditnotaer på samme måte som kontantrabatter på fakturaer. Når du utligner en kreditnota på en faktura, reduserer [!INCLUDE [prod_short](includes/prod_short.md)] rabattbeløpet for fakturaen med kreditnotaens rabattbeløp.  

Hvis du vil sende kundene purringer om forfalte betalinger, må du definere purregrader og betingelser. Hvis du vil lære mer om purringer, kan du gå til [Konfigurer påminnelsesbetingelser og -nivåer](finance-setup-reminders.md)  

## Slik definerer du betalingsbetingelser

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Betalingsbetingelser**, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Når du har definert betalingsbetingelsene, tilordner du dem til kunder og leverandører. Du kan eventuelt tilordne betalingsbetingelser til betalingsmåtene.  

> [!TIP]
> I grunnversjonen av [!INCLUDE [prod_short](includes/prod_short.md)] støtter ikke betalingsbetingelser delvise betalinger. Du må i stedet bruke funksjonene for forskuddsbetaling. Hvis du vil ha mer informasjon om forskuddsbetalinger, går du til [Definer forskuddsbetalinger](finance-set-up-prepayments.md).
>
> I noen land/områder *kan* du definere betalingsbetingelser med delvise betalinger. Hvis du vil finne ut om denne funksjonen støttes i ditt land/område, kan du gå til delen **Lokale funksjoner** i innholdsfortegnelsen til venstre for en [Microsoft Learn](about-localization.md)-artikkel.

## Se også

[Konfigurer betalingsmåter:](finance-payment-methods.md)  
[Konfigurer forskudd](finance-set-up-prepayments.md)  
[Konfigurere finans](finance-setup-finance.md)  
[Registrere nye kunder](sales-how-register-new-customers.md)  
[Registrere nye leverandører](purchasing-how-register-new-vendors.md)  
[Salg](sales-manage-sales.md)  
[Innkjøp](purchasing-manage-purchasing.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
