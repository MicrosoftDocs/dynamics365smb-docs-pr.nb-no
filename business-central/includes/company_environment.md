---
author: brentholtorf
ms.topic: include
ms.date: 04/01/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
[!INCLUDE[prod_short](prod_short.md)]-brukere støtter noen ganger mer enn én avdeling eller underorganisasjon i en forretningsenhet. Det kan for eksempel hende at en bedrift har salgskontorer i andre byer og flere land/områder, så det har opprettet en separat forretningsenhet for hvert kontor. Kontorene som er i samme land/område, defineres som separate *selskaper* i et delt *miljø*. Andre kontorer opprettes som selskaper i separate miljøer fordi de er i geografisk plassert i andre land/områder.

- Hva er et selskap?

  Tenk på et *selskap* som en beholder som inneholder informasjon om en juridisk enhet. Ifølge eksemplet ovenfor har en bedrift et salgskontor i Bergen og et annet i Oslo, så det opprettes et selskap i [!INCLUDE[prod_short](prod_short.md)] for hvert kontor, slik at det kan håndtere drift for hvert kontor separat.

- Hva er et miljø?

  Firmaer i [!INCLUDE[prod_short](prod_short.md)] på nettet finnes i det som kalles *miljøer*. Det finnes to typer miljøer, **produksjon** og **sandkasse**. Produksjonsmiljøer inneholder for eksempel aktive forretningsdata, og sandkassemiljøer brukes som et sikkert sted til å teste ting som nye forretningsprosesser eller funksjoner. Hvis du vil ha mer informasjon, kan du se [Typer miljøer](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#types-of-environments) (bare på engelsk). Hvis du har tilgang til et selskap, har du tilgang til miljøet det er i. Hvis du har tilgang til mer enn ett selskap, og disse selskapene har forskjellige miljøer, må du angi hvilket miljø du vil arbeide med når du logger på [!INCLUDE[prod_short](prod_short.md)]. Miljøer er spesielt for et gitt land/område, så hvis organisasjonen arbeider i flere land/områder, trenger du egne miljøer for hvert land/område. Hvis du vil ha mer informasjon, kan du se [Miljøer og selskaper](/dynamics365/business-central/dev-itpro/administration/tenant-environment-topology#environments-and-companies) (bare på engelsk).
