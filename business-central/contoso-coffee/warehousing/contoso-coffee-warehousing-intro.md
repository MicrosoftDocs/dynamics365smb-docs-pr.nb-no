---
title: Innføring i Contoso Coffee
description: Oversikt over scenarioer for hvordan Contoso Coffee-demo data kan hjelpe deg å lære hvordan du bruker lagerfunksjonene i Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 4760
author: brentholtorf
ms.author: bholtorf
---

# <a name="introduction-to-contoso-coffee-warehousing"></a>Innføring i Contoso Coffee-lager

Contoso Coffee er et fiktivt selskap som produserer forbrukerkaffemaskiner og kommersielle kaffemaskiner. **Contoso Coffee**-appene for Business Central legger til demonstrasjonsdata som du kan bruke til å lære hvordan du bruker lagerfunksjonene i Business Central. Du kan konfigurere lagerfunksjoner på ulike måter, se [Oversikt over forskjellige konfigurasjonsalternativer](../../design-details-warehouse-management.md#overview-of-different-configuration-options).

Appen har tre lokasjoner som er optimalisert for ulike scenarioer:

- **SØLV**  

  Denne lokasjonen er konfigurert for bruk av hyller. Den kan lett konfigureres til å støtte grunnleggende eller avanserte. 

- **GULT**  

  Denne lokasjonen bruker avansert lageroppsett, men bruker ikke hyller. Den kan konfigureres på nytt for å støtte grunnleggende oppsett.

- **KR.SAND**  

  Denne lokasjonen bruker avansert lageroppsett med lagerstyring, som gir mer avanserte regler for hvordan varer flytter seg gjennom lageret.

## <a name="set-up-contoso-coffee-warehousing-data"></a>Konfigurer Contoso Coffee-lagerdata

For å kunne bruke Contoso Coffee-lagerdemodata må du installere to apper i det aktuelle selskapet i [!INCLUDE [prod_short](../../includes/prod_short.md)]:  

- **Demodatasett for Contoso Coffee**  

    Denne appen inneholder demonstrasjonsdata for basisprogrammet.  
- **Demodatasett for Contoso Coffee (land-ID)**  

    Denne appen legger til landspesifikt innhold oppå basisprogrammet.

Legg til appene i et tomt selskap i et betalt abonnement eller som en del av en prøveversjon. Opprett for eksempel et nytt selskap uten eksempeldata fra den assisterte veiledningen **Opprett nytt selskap** som du kan åpne fra **Selskaper**-oversikten. Deretter legger du til appene fra [markedsplassen](../../ui-extensions-install-uninstall.md#install), hvis de ikke allerede er oppført på siden **Utvidelsesbehandling**-side.  

Når de relevante appene er installert, går du til [Demodata for Contoso Coffee-lager](https://businesscentral.dynamics.com/?page=4761)-siden i [!INCLUDE [prod_short](../../includes/prod_short.md)] og endrer standardinnstillingene etter behov. Tabellen nedenfor beskriver innstillingene:  

|Felt  |Beskrivelse  |
|---------|---------|
|**Startår** |Angir det første året du vil bruke for Contoso Coffee-demondataene. Året er enten et kalenderår eller et regnskapsår, avhengig av firmaoppsettet.|
|**Lokasjonshylle**  |Lokasjonen som skal brukes for scenarioer for grunnleggende lokasjon.|
|**Avansert logistikk for lokasjon**  |Lokasjonen som skal brukes for scenarioer for enkel logistikk.|
|**Lagerstyring for lokasjon**  |Lokasjonen som skal brukes for scenarioer for avansert logistikk.|
|**Lokasjon i transitt**  |Lokasjonen som skal brukes for i transitt-lokasjonen i overføringsscenarioer.|
|**Kundenr.**  |Kunden som skal brukes i grunnleggende og enkle scenarioer i salgsoperasjoner.|
|**Leverandørnr.**  |Leverandøren som skal brukes i alle scenarioer i innkjøpsoperasjoner.|
|**Hovedvarenr.**  |Varen som skal brukes i alle scenarioer i salgsoperasjoner.|
|**Vare 1 nr.**  |Hovedvaren som skal brukes for alle scenarioene.|
|**Vare 2 nr.**  |Tilleggsvaren som skal brukes for alle scenarioene.|
|**Bokføringsgruppe - kunde**|Angir en firmakode for innenlandske kunder. Firmakodene brukes når transaksjoner bokføres. |
|**Kunde – generell firmabokføringsgrupper**|Angir en firmakode for innenlandske kunder. Firmakodene brukes når transaksjoner bokføres. |
|**Bokføringsgruppe - leverandør**|Angir en firmakode for innenlandske kunder og leverandører. Firmakodene brukes når transaksjoner bokføres. |
|**Leverandør – generell firmabokføringsgrupper**|Angir en firmakode for innenlandske kunder og leverandører. Firmakodene brukes når transaksjoner bokføres. |
|**Innenlands – mva-firmabokføringsgrupper**|Angir en mva-firmabokføringsgruppe for kunder og leverandører for bokføring av mva. hvis mva. er aktivert.|
|**Videresalg – lagerbokføringsgruppe**    |Angir en kode for varer som må brukes for bokføring av videresalg.|
|**Detalj – generell varebokføringsgruppe**    |Angir en kode for varer som må brukes for bokføring av detaljhandel.|
|**Mva-bokføringsgruppe - vare**    |Angir en mva-produktkode for varer for bokføring av mva. hvis mva. er aktivert.|
|**Prisfaktor**     |Angir en faktor for å konvertere en pris fra USD/EUR til den lokale valutaen. *1* betyr at prisen er det samme beløpet i hvilken som helst valuta. Et høyere nummer brukes til å hente prisen i lokal valuta. |
|**Avrundingspresisjon**  |Definerer hvordan beregnet forbruksantall avrundes når de er angitt på forbrukskladdelinjer. Antall som er mindre enn 0,5 vil bli rundet ned. Antall som er større eller lik 0,5 vil bli rundet opp.|

Når du er klar, velger du **Opprett demonstrasjonsdata**-handling. Det tar noen minutter å legge til dataene i den underliggende databasen, men da er du klar til å kjøre de ulike scenarioene.  

> [!IMPORTANT]
> Hvis du kjører scenarioene, kan det være lurt å kontrollere at brukeren er lagt til for bestemte lokasjoner. Hvis du vil ha mer informasjon, kan du se [Definere lageransatte](../../warehouse-how-to-set-up-warehouse-employees.md).

## <a name="scenarios"></a>Scenarier

Demodata for Contoso Coffee-lager støtter nå følgende scenarioer for test og opplæring:

1.  [Gjennomgang av inngående og utgående flyt i grunnleggende lageroppsett](warehouse-basic-flow-putaway-pick.md)
2.  [Gjennomgang av inngående og utgående flyt i blandede lageroppsett](warehouse-mixed-flow-receive-pick-ship.md)
3.  [Gjennomgang av inngående og utgående flyt i avansert lageroppsett med lagerstyring](warehouse-directed-flow.md)

Les trinnene for hvert scenario i den relevante artikkelen.  

## <a name="see-also"></a>Se også

[Definer lagerbeholdning](../../inventory-setup-inventory.md) 
[Slik definerer du lokasjoner](../../inventory-how-setup-locations.md) 
[Lagerstyring](../../warehouse-manage-warehouse.md) 
[Utformingsdetaljer](../../design-details-warehouse-overview.md) 
