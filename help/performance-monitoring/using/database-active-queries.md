---
product: campaign
solution: Campaign
title: Övervaka aktiva frågor
description: Lär dig hur du övervakar aktiva frågor i Campaign-instanser på Kontrollpanelen.
feature: Control Panel
role: Architect
level: Experienced
exl-id: bb9e1ce3-2472-4bc1-a82a-a301c6bf830e
source-git-commit: efad3b82a498cfc88a06479e40c3e5c75d814740
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 100%

---

# Övervaka aktiva frågor {#long-running-queries}

Området **[!UICONTROL Active queries]** från fliken **[!UICONTROL Databases]** visar de fem frågor som har körts längst på den valda instansen.

![](assets/active-queries.png)

Kolumnerna **[!UICONTROL Duration]** anger hur länge en fråga har körts på instansen. Längden visas i följande format: `hh:mm:ss.ms`.

>[!IMPORTANT]
>
>Om någon av frågorna har varit aktiv i mer än 24 timmar kan du kontakta kundtjänst så att de kan identifiera och lösa problemet. Du måste förse dem med värdet i kolumnen **[!UICONTROL PID]** som är en unik identifierare för frågan.
