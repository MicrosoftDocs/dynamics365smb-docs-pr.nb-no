---
title: Bruke profiler til å klassifisere kontakter
description: Les om hvordan du definerer profilspørreskjemaer for å bidra til å klassifisere forretningskontaktenes profiler.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'contacts, profiles'
ms.search.form: '5109, 5110'
ms.author: edupont
ms.date: 05/20/2022
---

# <a name="use-profile-questionnaires-to-classify-business-contacts"></a><a name="use-profile-questionnaires-to-classify-business-contacts"></a>Bruke profilspørreskjemaer til å klassifisere forretningskontakter

Du kan rangere et prospekt slik at du kan identifisere de ideelle prospektene du skal fokusere salgskampanjen på. Du kan definere profilspørreskjemaer du vil bruke når du angir opplysninger om profiler for kontaktene. Du kan definere de ulike spørsmålene du vil spørre kontaktene om, i hvert enkelt spørreskjema. På denne måten kan du gruppere kontakter slik at det blir mer sannsynlig at kampanjene når de riktige personene basert på kriteriene du definerer med spørreskjemaene.  

Med de riktige spørreskjemaene kan du rangere prospektene og gruppere dem i kategorier. Du kan bruke eksisterende spørsmål og svar og kombinere dem med nye spørsmål og svar og la disse danne et grunnlag for rangeringen. Hvert svar i rangeringen får en poengverdi, og avhengig av intervallet du definerer for kategoriene (*Fra verdi* og *Til verdi*), grupperer rangeringssystemet kontaktene i kategoriene du har definert. Dette kan være *ABC*-kunder, leverandører med *høy/lav lojalitet* eller prospekter med status *platina/gull/sølv*.  

Du kan også kjøre spørreskjemaet for å besvare noen av spørsmålene automatisk basert på data om kontakter, kunder eller leverandører.  

## <a name="to-add-a-profile-questionnaire"></a><a name="to-add-a-profile-questionnaire"></a>Slik legger du til et profilspørreskjema:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Spørreskjemaoppsett**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**.  
3. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-add-questions-to-a-profile-questionnaire"></a><a name="to-add-questions-to-a-profile-questionnaire"></a>Slik legger du til spørsmål i et profilspørreskjema:

1. Velg det aktuelle profilspørreskjemaet, og velg handlingen **Rediger spørreskjemaoppsett**.  
2. På den første tomme linjen, i **Type**-feltet, velger du **Spørsmål** og skriver inn spørsmålet i **Beskrivelse**-feltet. Fyll ut de andre feltene på denne linjen.  

    Du kan også legge til detaljer i spørsmålet.

    1. Velg linjen med spørsmålet, og velg deretter **Spørsmålsdetaljer** på **Linje**- menyen.  

    2. På hurtigfanen **Klassifisering** i siden **Profilspørsmålsopplysninger** velger du feltet **Automatisk kontaktklassifisering**.  

    3. Velg alternativet **Rangering** i feltet **Kontaktklass.felt**.  

    4. Fyll ut feltet **Min. av spm. som må besv. (%)**. Standarden er **0**.  

        Dette angir antall spørsmål i prosenter som må besvares for at denne rangeringen skal kunne beregnes.

    5. I fane **Handlinger** i gruppen **Side** velger du **Poengberegning**. Angi poengene du vil gi hvert svar som vises i siden **Poengberegning**.

        Hvis du vil ha en oversikt over poengene du har tildelt hvert svar, velger du handlingen **Poengberegning**.

    6. Hvis du vil kjøre en oppdatering, går du tilbake til siden **Profilspørreskjema – oppsett**. I menyen **Handlinger** i gruppen **Funksjoner** velger du **Oppdater klassifisering**.

    På siden **Profilspørreskjema – oppsett** vises antall kontakter som oppfyller disse vilkårene i **Ant. kontakter**-feltet. De vises også på **Kontaktkort** for hver kontakt.

3. På den neste tomme linjen, i **Type**-feltet, velger du **Svar** og skriver inn svaret i **Beskrivelse**-feltet.  
4. Velg prioriteten i **Prioritet**-feltet. Definer et punktområde i feltene **Fra verdi** og **Til verdi**. Kontakter som får poeng innenfor det definerte intervallet, vil motta svaret.  

Gjenta disse trinnene hvis du vil angi alle spørsmål og svar i profilspørreskjemaene.

Når du har opprettet et spørreskjema, kan du bruke det til å vurdere og klassifisere kontaktene dine. Du kan også lage spørsmål som rangeres automatisk basert på informasjon på kontaktkortet.  

> [!NOTE]
> Hvis du angir et spørsmål som skal besvares automatisk, velger du **Linje**, og deretter velger du **Spørsmålsopplysninger** for å angi hvilke kriterier som skal brukes til å besvare spørsmålet.

## <a name="apply-questionnaires-to-contacts"></a><a name="apply-questionnaires-to-contacts"></a>Bruk spørreskjemaer på kontakter

Du kan bruke spørreskjemaene på kontakter manuelt. Åpne det relevante kontaktkortet, og velg deretter handlingen **Profil**. Så snart du har brukt spørreskjemaene du vil bruke, kan du begynne å bruke kategoriene i kampanjene.  

## <a name="the-automatic-classification-of-contacts"></a><a name="the-automatic-classification-of-contacts"></a>Automatisk klassifisering av kontakter

Du kan klassifisere kontaktene automatisk etter opplysninger om kunde, leverandør og kontakt. Det gjør du ved å definere automatisk besvarte profilspørsmål på siden **Profilspørreskjema - oppsett**.  

> [!NOTE]
> Det er bare kontakter som er registrert som kunder og leverandører, som kan tilordnes en klassifisering som er basert på henholdsvis kunde- og leverandørdata. Den automatiske klassifiseringen blir ikke automatisk oppdatert. Du bør derfor oppdatere profilspørreskjemaene etter at du har oppdatert kunde-, leverandør- eller kontaktdataene som skjemaene er basert på.  

Etter at du har definert automatisk besvaring av profilspørsmål, tilordner [!INCLUDE[prod_short](includes/prod_short.md)] automatisk riktige svar for en kontakt hvis du tilordner profilspørreskjemaet som inneholder disse spørsmålene, til kontakten.  

## <a name="example"></a><a name="example"></a>Eksempel

Du kan klassifisere kontakter etter hvor mye de handler:

|Svar|Gjelder|
|--- |--- |
|A|kontakter som kjøpte for NOK 500 000 eller mer|
|B|kontakter som kjøpte for LV 100 000 til 499 999|
|U|kontakter som kjøpte for LV 99 999 eller mindre|

Du gjør dette ved å fylle ut siden **Profilspørreskjema - oppsett** slik:

| Type     | Beskrivelse        | Automatisk klassifisering     | Fra verdi | Til verdi |
|----------|--------------------|------------------------------|------------|----------|
| Spørsmål | ABC-klassifisering | Klikk for å sette en hake |            |          |
| Svar   | A                  |                              | 500,000    |          |
| Svar   | B                  |                              | 100,000    | 499,999  |
| Svar   | U                  |                              |            | 99,999   |

Fyll deretter ut siden **Profilspørsmålsopplysninger** på følgende måte:

| Felt                         | Verdi         |
|-------------------------------|---------------|
| Kundeklassifiseringsfelt | Salg (LV)   |
| Klassifiseringsmåte         | Definert verdi |

Når du tilordner profilspørreskjemaet som inneholder dette spørsmålet, til en kontakt, angir programmet automatisk riktig svar for denne kontakten på profillinjene på kontaktkortet.

## <a name="see-also"></a><a name="see-also"></a>Se også

[Opprette kontakter](marketing-create-contact-companies.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
