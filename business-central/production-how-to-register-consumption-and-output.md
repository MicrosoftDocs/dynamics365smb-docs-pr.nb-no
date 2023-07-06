---
title: Registrer forbruksavgang for produksjonsordre
description: Dette emnet forklarer hvordan du registrerer forbruk og avgang for en frigitt produksjonsordrelinje som vises på siden Produksjonskladd.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 5510
ms.date: 03/08/2023
ms.author: edupont
---
# <a name="register-consumption-and-output-for-one-released-production-order-line"></a><a name="register-consumption-and-output-for-one-released-production-order-line"></a><a name="register-consumption-and-output-for-one-released-production-order-line"></a>Registrere forbruk og avgang for én frigitt produksjonsordrelinje

Denne oppgaven utføres på **Produksjonskladd**-siden. Kladden kombinerer funksjonene fra separate forbrukskladder og ferdigmeldingskladder i én kladd. Den kombinerte kladden åpnes direkte fra en frigitt produksjonsordre. Hovedformålet er manuell bokføring av komponentforbruk, antall produserte sluttvarer og tiden som brukes på operasjoner. Verdiene bokføres i poster under den frigitte produksjonsordren. Forbruksantall bokføres som negative vareposter, avgangsantall bokføres som positive poster, og tidsforbruk bokføres som kapasitetsposter. Slike bokførte verdier kan også vises nederst i kladden som faktisk antall.  

> [!NOTE]  
> Ettersom forbruksdata behandles sammen med avgangsdata, gir denne kladden mulighet til å vise koblede komponenter og operasjoner i en logisk prosesstruktur. komponenter er rykket inn under de respektive operasjonene. Dette krever at du bruker rutekoblingskoder.  

> [!NOTE]  
> Komponenter uten rutekoblingskoder står oppført først i kladden.  

## <a name="to-register-consumption-and-output"></a><a name="to-register-consumption-and-output"></a><a name="to-register-consumption-and-output"></a>Slik registrerer du forbruk og avgang

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Frigitte produksjonsordrer** og velg den relaterte koblingen.  
2. Åpne en frigitt produksjonsordrelinje som er klar for registrering. På hurtigfanen **Linjer** velger du **Linje**-handlingen, og deretter velger du handlingen **Produksjonskladd**.  

    **Produksjonskladd**-siden åpnes med kladdelinjer for produksjonsordrelinjen i henhold til sidene **Prod.ordrekomponent** og **Prod.ordrerute**. Disse linjene stammer fra produksjonsstykklisten og ruten som er tilordnet varen som blir produsert. Hvis du vil ha mer informasjon, kan du se [Opprette produksjonsstykklister](production-how-to-create-routings.md).  

3. I **Bokføringsdato**-feltet øverst i kladden angir du en bokføringsdato som gjelder for alle linjene. Arbeidsdatoen er satt inn som standard. Feltet er ment som en rask måte å justere bokføringsdatoer for alle linjer på, hvis dette er relevant.  

    > [!NOTE]  
    >  Bokføringsdatoer som er angitt på individuelle linjer, vil overstyre dette feltet.  

4. I feltet **Filter for trekkmetode** øverst i kladden kan du også velge å vise forbruk og avgang som er bokført automatisk i henhold til trekkmetodene som er definert for henholdsvis varen og ressursen. Hvis du vil ha mer informasjon, kan du se [Aktivere lagertrekk av komponenter i henhold til operasjonsavgang](production-how-to-flush-components-according-to-operation-output.md).

5. Fortsett med å angi det relevante forbruks- og avgangsantallet i de redigerbare feltene.  
  
    For hver linjetype i kladden vises bare relevante felt. Resten er tomme og skrivebeskyttet.  

    Når kladden åpnes, er den forhåndsdefinert med antallene som skal bokføres. Hvis ingenting er bokført så langt, vil alle antallsfeltene som standard vise de forventede antallene fra produksjonsordren. Hvis delvise bokføringer er foretatt, vil antallsfeltene på linjene vise de gjenstående antallene. Antallene og tidene som allerede er bokført for ordren, vises som faktiske poster nederst i kladden.  

    Når det gjelder antallene i **Avgangsantall**-feltet, kan du definere hvilke verdier som skal forhåndsdefineres første gang kladden åpnes. Det gjør du fra **Produksjonsoppsett**-siden, hurtigfanen **Generelt**, i feltet **Forhåndsdefinert avgangsantall**.

    > [!NOTE]  
    >  Bare avgangsmengden på den siste kladdelinjen for posttypen **Avgang** vil justere lagernivået ved bokføring av kladden. Derfor må du ikke bokføre kladden med det forventede avgangsantallet forhåndsdefinert på den siste avgangslinjen, før alle sluttvarene faktisk er produsert.  

6. Velg **Ferdig**-feltet på avgangslinjene for å angi at operasjonen er ferdig. Dette feltet er relatert til **Rutestatus**-feltet på en rutelinje i en produksjonsordre.  
7. Velg **Bokfør**-handlingen for å registrere antallene du har angitt, og lukk deretter kladden.  

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

    Hvis det gjenstår verdier som skal bokføres, inneholder kladden de gjenstående verdiene neste gang den åpnes. Bokførte verdier vises som faktiske verdier nederst i kladden.  

    > [!NOTE]  
    >  Hvis en vare som forbrukes, blir sperret, vil ikke kladden bokføre forbruksantall for varen. Hvis en maskin eller et arbeidssenter blir sperret, vil ikke kladden bokføre avgangsantall eller behandlingstider for den aktuelle avgangslinjen.  

    > [!NOTE]  
    > Hvis du lukker kladden uten bokføring, vil endringene gå tapt.  

> [!WARNING]  
> Siden **Produksjonskladd** kan ikke brukes av to brukere samtidig. Dette betyr at hvis Bruker 2 åpner siden og skriver inn data når Bruker 1 allerede jobber på siden, kan Bruker 2 miste data når Bruker 1 lukker siden.  

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se også

[Produksjon](production-manage-manufacturing.md)  
[Definere produksjon](production-configure-production-processes.md)  
[Planlegging](production-planning.md)  
[Lager](inventory-manage-inventory.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
