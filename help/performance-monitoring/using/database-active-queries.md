---
product: campaign
solution: Campaign
title: Övervaka aktiva frågor
description: Lär dig hur du övervakar aktiva frågor i Campaign-instanser på Kontrollpanelen.
feature: Control Panel, Monitoring
role: Admin
level: Experienced
exl-id: a1ea14f9-ec1d-4e10-89ef-846065512e8c
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 100%

---

# Övervaka aktiva frågor {#long-running-queries}

Området **[!UICONTROL Active queries]** från fliken **[!UICONTROL Databases]** visar de fem frågor som har körts längst på den valda instansen.

![](assets/active-queries.png)

Kolumnerna **[!UICONTROL Duration]** anger hur länge en fråga har körts på instansen. Längden visas i följande format: `hh:mm:ss.ms`.

>[!IMPORTANT]
>
>Om någon av frågorna har varit aktiv i mer än 24 timmar kan du kontakta kundtjänst så att de kan identifiera och lösa problemet. Du måste förse dem med värdet i kolumnen **[!UICONTROL PID]** som är en unik identifierare för frågan.
