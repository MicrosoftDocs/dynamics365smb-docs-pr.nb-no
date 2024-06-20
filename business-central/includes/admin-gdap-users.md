---
author: brentholtorf
ms.topic: include
ms.date: 05/09/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
Du vil kanskje se andre brukere i listen **Brukere** i tillegg til fra ditt eget selskap. Når en delegert administrator fra et forhandlerselskap logger seg på et [!INCLUDE [prod_short](prod_short.md)]-miljø på vegne av kunden, opprettes de automatisk som en bruker i [!INCLUDE [prod_short](prod_short.md)]. På denne måten logges [!INCLUDE [prod_short](prod_short.md)]-handlingene som utføres av en delegert administrator, for eksempel bokføringsdokumenter og tilknyttet bruker-ID-en.  

Med *detaljert delegert administratortilgang (GDAP)* vises brukeren i **Brukere**-listen, og kan tildeles alle tillatelser. De vises ikke med navn og andre personlige opplysninger, men med firmanavn og en unik ID. Både interne og eksterne administratorer kan se disse brukerne i **Brukere**-listen, og de har full gjennomsiktighet i hva disse brukerne gjør gjennom [endringsloggen](../across-log-changes.md) for eksempel. Men de kan ikke se det faktiske navnet på disse brukerne. GDAP-brukere vises med brukernavn i følgende format: `User123456@partnerdomain.com`. De kan ha et brukernavn som gjenspeiler partnerens firmanavn, og e-postadressen er ikke den faktiske e-postadressen til personen. På denne måten avslører ikke GDAP-brukerkontoer personlig informasjon. Hvis du trenger å finne ut hvem personen bak et slikt pseudonym er, må du kontakte selskapet som denne brukeren arbeider for eller har arbeidet for.  
