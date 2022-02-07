---
product: campaign
solution: Campaign
title: De 10 viktigaste tillfälliga resurserna
description: Lär dig hur du på Kontrollpanelen övervakar de 10 största tillfälliga resurserna som genereras av arbetsflöden och leveranser i din Campaign-databas.
feature: Control Panel
role: Architect
level: Experienced
source-git-commit: 12e9326ba220776874654705587152bf3978949c
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# De 10 viktigaste tillfälliga resurserna {#top-10}

I **[!UICONTROL Top 10 temporary resources]**-området visas de 10 största tillfälliga resurserna som genereras av arbetsflöden och leveranser.

Övervakning av arbetsflöden och leveranser som genererar stora tillfälliga resurser är ett viktigt steg för att övervaka databasen. Om någon tillfällig resurs förbrukar för mycket databasutrymme bör du kontrollera att arbetsflödet eller leveransen är nödvändig och vid behov navigera till instansen för att stoppa den.

>[!IMPORTANT]
>
>Den allmänna rekommendationen är att undvika att ha **fler än 40 kolumner** i resurser som inte är färdiga.

![](assets/database-top10.png)

>[!NOTE]
>
>Om ett arbetsflöde har ett stort antal tabeller eller en stor databas rekommenderar vi att du granskar arbetsflödet för att ta reda på varför det genererar så mycket data.
>
>Resurser för att förhindra databasöverbelastning i Campaign Standard och Classic finns också tillgängliga i slutet av den här sidan.

Med knappen **[!UICONTROL View all]** får du åtkomst till detaljerad information om de här tillfälliga resurserna.

![](assets/database-top10-view.png)

Värdet i kolumnen **[!UICONTROL Keep interim results]** anger om alternativet är aktiverat (&quot;1&quot;) eller inaktiverat (&quot;0&quot;) i Campaign. Du kan spara resultatet av övergångarna mellan de olika aktiviteterna i ett arbetsflöde (se dokumentationen om [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/executing-a-workflow/managing-execution-options.html?lang=sv) och [Campaign Classic](https://experienceleague.adobe.com/docs/campaign-classic/using/automating-with-workflows/introduction/workflow-best-practices.html?lang=sv#logs) ).

>[!IMPORTANT]
>
>Det här alternativet får aldrig kontrolleras i ett produktionsarbetsflöde. Det används för att analysera resultaten och är endast avsett för testning och ska därför endast användas i utvecklings- eller stagingmiljöer.
>
>Om värdet på Kontrollpanelen anger att alternativet är aktiverat för ett av dina arbetsflöden rekommenderar vi att du inaktiverar det i Campaign.
