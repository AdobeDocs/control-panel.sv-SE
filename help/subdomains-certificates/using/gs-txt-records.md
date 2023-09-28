---
product: campaign
solution: Campaign
title: Hantera TXT-poster
description: Läs mer om hur man hanterar TXT-poster för verifiering av domänägarskap.
feature: Control Panel
role: Architect
level: Experienced
source-git-commit: 118fa4d722980e507d15647453e96a8b6189f837
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 25%

---


# Kom igång med TXT-poster {#managing-txt-records}

>[!CONTEXTUALHELP]
>id="cp_siteverification_add"
>title="Hantera TXT-poster"
>abstract="TXT-poster är en typ av DNS-poster som används för att tillhandahålla textinformation om en domän som kan läsas av externa källor. Med kontrollpanelen kan du lägga till tre typer av poster i dina underdomäner: Google Site Verification-, DMARC- och BIMI-poster."

## Om TXT-poster {#about}

TXT-poster är en typ av DNS-poster som används för att tillhandahålla textinformation om en domän som kan läsas av externa källor. På Kontrollpanelen kan du lägga till tre typer av poster i dina underdomäner:

* **Google TXT-poster** gör att du kan intyga att du äger din domän och säkerställa höga inkorgsfrekvenser och låga skräppostfrekvenser för dina e-postmeddelanden. [Lär dig hur du lägger till Google TXT-poster](managing-txt-records.md)
* **DMARC-poster** tillhandahåller ett sätt att autentisera avsändarens domän och förhindra obehörig användning av domänen för skadliga syften. [Lär dig hur du lägger till DMARC-poster](dmarc.md)
* **BIMI-poster** gör att du kan visa en godkänd logotyp bredvid dina e-postmeddelanden i e-postleverantörernas inkorgar för att förbättra varumärkesigenkänningen och förtroendet för dem. [Lär dig hur du lägger till BIMI-poster](bimi.md)

## Övervaka underdomänernas arkiv {#monitor}

Du kan övervaka alla TXT-poster som har lagts till för varje underdomän genom att gå till informationen för underdomänerna.

På den här skärmen visas alla poster av TXT-typ för den valda underdomänen, med information i kolumnen Värde om konfigurationen. Om du vill ta bort en Google TXT-, DMARC- eller BIMI-post klickar du på ellipsknappen och väljer Ta bort. Du kan även redigera DMARC- och BIMI-poster om det behövs.

![](assets/txt-records.png)
