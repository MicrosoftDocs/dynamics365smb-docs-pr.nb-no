---
title: Advarsler og feilmeldinger
description: Lær hvordan du kan feilsøke og finne løsninger på feilmeldinger når du arbeider i Business Central.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.date: 03/08/2024
ms.service: dynamics-365-business-central
ms.custom: bap-temeplate
---
# <a name="warnings-and-error-messages"></a>Advarsler og feilmeldinger

I løpet av arbeidsdagen kan du se meldinger i [!INCLUDE [prod_short](includes/prod_short.md)] om at noe gikk galt, eller at det ikke er mulig å bokføre noe, for eksempel. I mange tilfeller gjør meldingen det enkelt å løse eller tilbakestille eventuelle endringer du har gjort. I andre tilfeller har du kanskje ikke de opplysningene du trenger for å fjerne blokkeringen. Denne artikkelen inneholder tips for hvordan du går frem.  

## <a name="in-product-user-assistance"></a>Innebygd brukerstøtte

Standardversjonen av [!INCLUDE [prod_short](includes/prod_short.md)] omfatter beskrivelser for de fleste feltene, kolonnene og handlingene du får tilgang til når du velger navnet. I kombinasjon med læringstips for viktige sider, beskrivende tekster og instruksjonstekster, er disse verktøytipsene, eller bildeforklaringene, vår nåværende implementering av *innebygd brukerstøtte*, som er et viktig prinsipp i dagens programvaredesign.  

Hvis du har spørsmål om et felt eller et annet element i brukergrensesnittet, velger du navnet for å lese en kort beskrivelse. Velg **Spør Copilot**-koblingen hvis det ikke er nok. Du kan også bruke hjelperuten i produktet til å finne svar på spørsmålene dine.  

Hvis du vil ha mer informasjon, kan du se [Brukerstøttemodell for Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/user-assistance) i administrasjonsinnholdet for [!INCLUDE [prod_short](includes/prod_short.md)].  

## <a name="help-and-support-page"></a>Hjelp og støtte-siden

I [!INCLUDE[prod_short](includes/prod_short.md)] gir Hjelp-menyelementet (spørsmålstegnet øverst til høyre) tilgang til **Hjelp og støtte**-siden, der du finner koblinger til ressurser som kan hjelpe deg med å finne svar på spørsmålene dine. Hvis du vil ha mer informasjon, kan du se [Ressurser for hjelp og støtte](product-help-and-support.md).  

## <a name="help-others"></a>Hjelpe andre

Hvis du er administrator eller en superbruker, kan du hjelpe andre ved å slå opp feilmeldinger på siden **Feilmeldingsregister** eller i administrasjonssenteret. I mange tilfeller handler advarselen eller feilmeldingen om installasjoner eller mangel på tillatelser og lignende som superbrukeren eller administratoren enkelt kan hjelpe med. I andre tilfeller kan det hende du må sjekke sider for å finne årsaken. Hvis du vil ha mer informasjon, kan du se [Finne teknisk informasjon](/dynamics365/business-central/dev-itpro/administration/manage-technical-support#finding-technical-information) i administrasjonsinnholdet for [!INCLUDE [prod_short](includes/prod_short.md)].  

## <a name="share-error-details-for-faster-assistance"></a>Del feildetaljer for raskere hjelp

Bruk ekspertisen til kolleger eller fageksperter for å overvinne hindringer og minimere nedetid. Når du er blokkert av en feil, kan du enkelt dele feildetaljene når du får hjelp.

Detaljene inkluderer feilmeldingen, feilkoden og annen informasjon som er nyttig når du feilsøker en feil. Ved å dele feildetaljene kan du effektivt kommunisere det spesifikke problemet du står overfor, noe som hjelper kollegene dine med å hjelpe deg.  

Du kan kopiere detaljer ved å velge **Del-ikonet** i innebygde valideringsdialogbokser, eller **Del detaljer**-menyen i feildialogbokser.  

I tillegg til å kopiere feildetaljer kan du også velge å dele detaljer via Microsoft Teams ved å velge **Del detaljer til Teams** for å gjøre følgende:

* Kopier feildetaljene.
* Åpne vinduet **Del til Teams**, der du kan lime inn feildetaljene du kopierte, og angi hvem du vil be om hjelp. [!INCLUDE [prod_short](includes/prod_short.md)] legger til en kobling til siden der du opplevde feilen, for å gjøre feilsøking enklere.

Du kan også velge å dele detaljer via e-post ved å velge **Del detaljer via e-post** for å gjøre følgende:

* Kopier feildetaljene.
* Åpne standard redigeringsprogram for e-post, der du kan lime inn feildetaljene du kopierte, og angi hvem du vil be om hjelp. [!INCLUDE [prod_short](includes/prod_short.md)] legger til en kobling til siden der du opplevde feilen.

## <a name="help-yourself"></a>Hjelp deg selv

Feilmeldinger gir informasjon og handlinger som gjør det enklere å forstå, gå til og løse feil som kommer fra plattformen.

Feilmeldingene som [!INCLUDE [prod_short](includes/prod_short.md)]-plattformen genererer, inneholder de fullstendige tekniske detaljene, inkludert feltnavn, i delen **Detaljert feilmelding**. Velg ikonet **Kopier detaljer** ved interne valideringsfeil eller i en feilmelding for å få tilgang til den tekniske informasjonen.

Handlinger i feilmeldinger tar deg direkte til siden der et felt forårsaker feilen. Du trenger ikke å bruke tid på finne siden eller feltet selv. For å løse feilen, bare velg handlingen i feilmeldingen, så tar [!INCLUDE [prod_short](includes/prod_short.md)] deg til riktig sted.

Følgende video viser hvordan du bruker handlingsbare feilmeldinger til å oppheve blokkeringen.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RW1l2sM]

### <a name="tip-for-developers"></a>Tips for utviklere

Hvis du er en utvikler, når du kaller opp [TestField](/dynamics365/business-central/dev-itpro/developer/methods-auto/record/record-testfield-joker-joker-errorinfo-method)-metoden, men ikke sender inn |`ErrorInfo`-objektet, genererer [!INCLUDE [prod_short](includes/prod_short.md)] automatisk en kobling til en side der en bruker kan løse problemet. [!INCLUDE [prod_short](includes/prod_short.md)] henter først oppslags- eller neddrillingssiden for posten, og finner deretter kortsiden eller oppslagssiden og legger til en navigasjonskobling på kortsiden. [!INCLUDE [prod_short](includes/prod_short.md)] legger ikke til en kobling i følgende situasjoner:

* Hvis feilen er på siden som er åpen.
* Hvis brukeren ikke har tillatelse til å endre den underliggende posten.

## <a name="see-also"></a>Se også

[Ressurser for hjelp og støtte](product-help-and-support.md)  
[Vanlige spørsmål](across-faq.yml)  
[Vanlige spørsmål om Fortell meg](ui-search-faq.md)  
[Vanlige spørsmål om søk og filtrering](ui-search-filter-faq.yml)  
[Vanlige spørsmål om kopiere og lime inn](faq-copy-paste.yml)  
[Endre grunnleggende innstillinger](ui-change-basic-settings.md)  
[Bli klar til å gjøre forretninger](ui-get-ready-business.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
