---
product: campaign
solution: Campaign
title: Lagringsöversikt
description: Lär dig hur du på Kontrollpanelen övervakar olika Campaign-resurser som förbrukar databasutrymme på dina instanser.
feature: Control Panel, Monitoring
role: Admin
level: Experienced
exl-id: bb9e1ce3-2472-4bc1-a82a-a301c6bf830e
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 59%

---

# Lagringsöversikt {#storage-overview}

>[!CONTEXTUALHELP]
>id="cp_dbdetails_storagedetails"
>title="Om lagringsöversikt"
>abstract="På den här fliken kan du få detaljerad information om olika resurser i Campaign som förbrukar databasutrymme."

Området **[!UICONTROL Storage overview]** innehåller en grafisk representation av det utrymme som används av:

* **[!UICONTROL System resources]**

  Observera att om systemresurserna förbrukar en stor del av databasutrymmet rekommenderar vi att du kontaktar kundtjänst.

* **[!UICONTROL Out-of-the-box tables]** kommer som standard med dina instanser i Campaign,
* **[!UICONTROL Temporary tables]** som skapats av arbetsflöden och leveranser,
* **[!UICONTROL Non-out of the box tables]** som genererades när du skapade anpassade resurser.

![](assets/database-storage-overview.png)

Klicka på knappen **[!UICONTROL View details]** om du vill ha mer information om de olika resurser som förbrukar databasutrymme.

Du kan använda listrutan för att förfina dina söknings- och visningstabeller från en viss resurstyp (arbetsflöden, leveranser, mottagare).

![](assets/database-storage-details.png)

Observera att du på den här skärmen även kan övervaka arbetsflödesparametrar som kan kräva särskild uppmärksamhet för att undvika problem i dina instanser. Läs mer på [den här sidan](workflow-monitoring.md).
