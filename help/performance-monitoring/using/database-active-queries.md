---
product: campaign
solution: Campaign
title: Övervaka aktiva frågor
description: Lär dig hur du övervakar aktiva frågor i Campaign-instanser på Kontrollpanelen.
feature: Control Panel
role: Architect
level: Experienced
source-git-commit: 12e9326ba220776874654705587152bf3978949c
workflow-type: ht
source-wordcount: '118'
ht-degree: 100%

---

# Övervaka aktiva frågor {#long-running-queries}

Området **[!UICONTROL Active queries]** från fliken **[!UICONTROL Databases]** visar de fem frågor som har körts längst på den valda instansen.

![](assets/active-queries.png)

Kolumnerna **[!UICONTROL Duration]** anger hur länge en fråga har körts på instansen. Längden visas i följande format: `hh:mm:ss.ms`.

>[!IMPORTANT]
>
>Om någon av frågorna har varit aktiv i mer än 24 timmar får du ett e-postmeddelande om du prenumererar på [e-postavisering](email-alerting.md).
>
>Kontakta i så fall kundtjänst så att de kan identifiera och lösa problemet. Du måste förse dem med värdet i kolumnen **[!UICONTROL PID]** som är en unik identifierare för frågan.
