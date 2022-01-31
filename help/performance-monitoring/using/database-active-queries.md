---
product: campaign
solution: Campaign
title: Övervaka aktiva frågor
description: Lär dig hur du övervakar aktiva frågor i Campaign-instanser på Kontrollpanelen.
feature: Control Panel
role: Architect
level: Experienced
exl-id: bb9e1ce3-2472-4bc1-a82a-a301c6bf830e
source-git-commit: 6922e132321f67e1e8122e33ead3c5e54c639763
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 0%

---

# Övervaka aktiva frågor {#long-running-queries}

The **[!UICONTROL Active queries]** området från **[!UICONTROL Databases]** På -fliken visas de fem frågor som har körts längst på den valda instansen.

![](assets/active-queries.png)

The **[!UICONTROL Duration]** kolumner anger hur länge en fråga har körts på instansen. Längden visas i följande format: `hh:mm:ss.ms`.

>[!IMPORTANT]
>
>Om någon av frågorna har varit aktiv i mer än 24 timmar kan du kontakta kundtjänst så att de kan identifiera och lösa problemet. I så fall måste du förse dem med **[!UICONTROL PID]** kolumnvärde, som är en unik identifierare för frågan.
