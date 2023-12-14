---
title: Oversikt over oppgaver for å håndtere salg
description: 'Les alt om hvordan du bruker Business Centrals tjenester til å administrere kunders salgsaktiviteter med kunder med salgsfakturaer, ordrer, tilbud og mer.'
author: brentholtorf
ms.topic: overview
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'trade, sell'
ms.search.form: 253
ms.date: 09/02/2022
ms.author: bholtorf
---
# <a name="sales"></a>Salg

Du kan opprette en salgsfaktura eller ordre for å registrere avtalen med en kunde om å selge bestemte produkter på bestemte leverings- og betalingsbetingelser.

Du må bruke ordrer hvis salgsprosessen krever at du sender deler av et bestillingsantall, for eksempel fordi det fullstendige antallet ikke er tilgjengelig med en gang. Hvis du selger varer ved å levere direkte fra leverandøren til kunden, som en direkte levering, må du også å bruke ordrer. I alle andre henseender fungerer ordrer på samme måte som salgsfakturaer. Med ordrer kan du også bruke funksjonen for ordrebekreftelse for å kommunisere bestemte leveringsdatoer til kunder.  

Du kan forhandle med kunden ved først å opprette et tilbud, som du kan konvertere til en salgsfaktura eller ordre når dere blir enige om salget. Etter at kunden har bekreftet avtalen, kan du sende en ordrebekreftelse for å registrere din forpliktelse til å levere produktene som avtalt.

Du kan enkelt korrigere eller annullere en bokført salgsfaktura før den er betalt. Dette er praktisk hvis du vil rette en skrivefeil, eller hvis kunden ber om en endring tidlig i ordreprosessen. Hvis den bokførte salgsfakturaen er betalt, må du opprette en salgskreditnota eller ordreretur for å reversere salget.

God salgs- og markedsføringspraksis handler om å ta de rette avgjørelsene til rett tid. Markedsføringsfunksjoner i [!INCLUDE[prod_short](includes/prod_short.md)] gir deg en nøyaktig oversikt over kontaktinformasjonen når du har behov for den, slik at du kan ta deg av potensielle kunder på en mer effektiv måte, og øke kundetilfredsheten. Finn ut mer under [Forbindelser](marketing-relationship-management.md).

Hvis du bruker Microsoft Dynamics 365 Sales for Customer Engagement, kan du dra nytte av sømløs integrering i kundeemne-til-kontanter-prosessen med Business Central for serverdelaktiviteter som å behandle bestillinger, håndtere lager og gjøre finansene. Finn ut mer under [Bruk Dynamics 365 Sales fra Business Central](marketing-integrate-dynamicscrm.md).

I forretningsmiljøer der kunden må betale før produkter leveres, for eksempel i detaljhandel, må du vente til mottak av betalingen før du leverer produktene. I de fleste tilfeller kan du behandle innkommende betalinger noen uker etter levering ved å utligne betalingene mot deres tilknyttede bokførte, ubetalte salgsfakturaer. Finn ut mer under [Avstem betalinger ved hjelp av automatisk utligning](receivables-how-reconcile-payments-auto-application.md).

Salgsdokumenter kan sendes som PDF-filer vedlagt i e-post. Brødteksten i e-posten inneholder et utdrag av salgsdokument, for eksempel produkter, totalt beløp og en kobling til PayPal-nettstedet. Finn ut mer under [Send dokumenter i e-post](ui-how-send-documents-email.md).

Du kan inkludere en godkjenningsarbeidsflyt for alle salgsprosesser, for eksempel hvis du vil kreve at store salg til bestemte kunder godkjennes av regnskapssjefen. Finn ut mer under [Bruk arbeidsflyter](across-use-workflows.md).

Tabellen nedenfor beskriver en sekvens av oppgaver og har koblinger til artiklene som beskriver dem.

| Til | Se |
| --- | --- |
|Opprett et kundekort for hver kunde du selger til.|[Registrere nye kunder](sales-how-register-new-customers.md)|
| Opprett et tilbud for å tilby produkter på betingelser det kan forhandles om, før du konverterer tilbudet til en salgsfaktura. |[Gi salgstilbud](sales-how-make-offers.md) |
| Opprett en salgsfaktura for å registrere avtalen med en kunde om å selge vedkommende bestemte produkter på bestemte leverings- og betalingsbetingelser. |[Fakturere salg](sales-how-invoice-sales.md) |
| Behandle en ordre som involverer delvis levering eller direkte levering. |[Selge produkter](sales-how-sell-products.md) |
|Forstå hva som skjer når du bokfører salgsdokumenter.|[Bokføre salg](ui-post-sales.md)|
|Klargjør for å plukke varer for levering.|[Skriv ut plukklisten](sales-how-print-picking-list.md)|
| Oppfyll en ordre med flere delleveringer. | [Behandle delleveringer](sales-how-send-partial-shipments.md) |
|Definere standard salgs- eller kjøpslinjer som du raskt kan sette inn i dokumenter, for eksempel for gjentakende etterfyllingsordrer.|[Opprette gjentakende salgs- og kjøpslinjer](sales-how-work-standard-lines.md)|  
| Koble en ordre til en bestilling for å selge en vare med direkte levering som skal leveres direkte fra leverandøren til kunden. |[Foreta direkte leveringer](sales-how-drop-shipment.md) |
|Få en katalogvare levert fra en leverandør til lageret ditt slik at du kan sende varen videre til kunden.|[Opprette spesialbestillinger](sales-how-to-create-special-orders.md)|
| Utfør en handling på en ubetalt bokført salgsfaktura for å opprette en kreditnota automatisk og enten annullere salgsfakturaen eller opprette den på nytt, slik at du kan foreta korrigeringer. |[Korrigere eller annullere ubetalte salgsfakturaer](sales-how-correct-cancel-sales-invoice.md) |
| Opprett en salgskreditnota for å tilbakestille en bestemt bokført salgsfaktura for å vise produktene kunden returnerer, og betalingsbeløpet du vil refundere. |[Behandle ordrereturer eller annulleringer](sales-how-process-sales-returns-cancellations.md) |
|Håndter kundens forpliktelse til å kjøpe store antall levert i flere forsendelser over tid.|[Arbeide med rammeordrer](sales-how-to-create-blanket-sales-orders.md)|
|Selg monteringsvarer som ikke er tilgjengelige for øyeblikket, ved å opprette koblet monteringsordre for å levere hele eller en del av ordreantallet.|[Selge varer som er montert til ordre](assembly-how-to-sell-items-assembled-to-order.md)|
|Fakturer en kunde én gang for flere leveringer ved å kombinere følgesedler på én faktura.|[Kombinere leveringer på én faktura](sales-how-to-combine-shipments-on-a-single-invoice.md)|
|Informer kundene om ordreleveringsdatoer ved å beregne første mulige forsendelsesdato eller tilgjengelig for ordre-datoen.|[Beregne ordrebekreftelsesdatoer](sales-how-to-calculate-order-promising-dates.md)|
|Løs forvirring når det finnes to eller flere poster for samme kunde.|[Slå sammen dupliserte poster](sales-how-merge-duplicate-records.md)|

## <a name="see-also"></a>Se også

[Sette opp salg](sales-setup-sales.md)  
[Registrer nye kunder](sales-how-register-new-customers.md)  
[Håndtere fordringer](receivables-manage-receivables.md)  
[Administrere skyldige beløp](payables-manage-payables.md)  
[Prosjektstyring](projects-manage-projects.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Generelle forretningsfunksjoner](ui-across-business-areas.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
