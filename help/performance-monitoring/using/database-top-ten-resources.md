---
product: campaign
solution: Campaign
title: De 10 viktigaste tillfälliga resurserna
description: Lär dig hur du på Kontrollpanelen övervakar de 10 största tillfälliga resurserna som genereras av arbetsflöden och leveranser i din Campaign-databas.
feature: Control Panel, Monitoring
role: Admin
level: Experienced
exl-id: 2fa2ffbb-102b-42c4-8feb-b0263ee9c930
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 69%

---

# De 10 viktigaste tillfälliga resurserna {#top-10}

I **[!UICONTROL Top 10 temporary resources]**-området visas de 10 största tillfälliga resurserna som genereras av arbetsflöden och leveranser.

Övervakning av arbetsflöden och leveranser som genererar stora tillfälliga resurser är ett viktigt steg för att övervaka databasen. Om någon tillfällig resurs förbrukar för mycket databasutrymme bör du kontrollera att arbetsflödet eller leveransen är nödvändig och vid behov navigera till instansen för att stoppa den.

>[!IMPORTANT]
>
>Den allmänna rekommendationen är att undvika att ha **fler än 40 kolumner** i resurser som inte är färdiga. Om ett arbetsflöde har ett stort antal tabeller eller en stor databas rekommenderar vi att du granskar arbetsflödet för att ta reda på varför det genererar så mycket data.
>
>Riktlinjer för Campaign Standard och klassiska finns även i [den här sidan](database-preventing-overload.md) för att förhindra databasöverbelastning.

![](assets/database-top10.png)

The **[!UICONTROL View all]** kan du komma åt **[!UICONTROL Storage overview]** information för att få detaljerad information om dessa tillfälliga resurser. Mer information finns på [den här sidan](database-storage-overview.md).
