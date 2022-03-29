---
product: campaign
solution: Campaign
title: Genomflöden och fördröjningsövervakning
description: Lär dig hur du övervakar genomflöden och fördröjning för dina Campaign-instanser på Kontrollpanelen.
feature: Control Panel
role: Architect
level: Experienced
exl-id: eddef17f-0667-4b43-bc56-2b1aeeae61bb
source-git-commit: 84fe0aeb10bc5e535a7ab54a3316a51a1a32b3ca
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 73%

---

# Genomflöden och fördröjningsövervakning {#throughputs-latency-monitoring}

>[!CONTEXTUALHELP]
>id="cp_performancemonitoring_throughputslatencies"
>title="Om genomflöden och fördröjningsövervakning "
>abstract="På den här fliken kan du övervaka hur leveransgenomflöden och fördröjning trendar över en tidsperiod på dina instanser."

Med Kontrollpanelen kan du övervaka leveransdataflöde och fördröjning för var och en av dina instanser.

>[!IMPORTANT]
>
>Den här funktionen är tillgänglig för alla Campaign Standards- och v8-kunder samt för Campaign V7-kunder med build-nummer 9032, 9330, 9346 eller 9349 som har [fristående](https://experienceleague.adobe.com/docs/campaign-classic/using/installing-campaign-classic/deployment-types-/standalone-deployment.html) distributioner (utan några mellaninstanser).

Det är viktigt att övervaka hur leveransgenomflöden och fördröjning trender över en tidsperiod för att förstå användningen av dina instanser och säkerställa att de presterar väl.

Den här informationen är tillgänglig på Kontrollpanelen för var och en av dina Campaign-instanser i kortet **[!UICONTROL Performance Monitoring]**, fliken **[!UICONTROL Throughputs & Latency]** (observera att det kan ta upp till en timme för Kontrollpanelen att visa siffrorna).

* Området **[!UICONTROL Throughput]** innehåller information om antalet meddelanden som skickas per timme från den valda Campaign-instansen för alla kommunikationskanaler som du är berättigad till.

   >[!NOTE]
   >
   >För Campaign v7/v8 är det dataflöde som uppnås från MID-instanser (mellanleverantörer). För fristående marknadsföringsdistributioner (MKT) (utan någon MID-instans) visas i stället dataflödet från MKT-instansen.

* Området **[!UICONTROL Latency]** innehåller information om fördröjningen som påträffas i den markerade instansen när transaktionsmeddelanden skickas i realtid. Fördröjningar hämtas och visualiseras vid percentilerna 95 och 99, vilket innebär att 95 % och 99 % av förfrågningarna ska vara snabbare än den angivna fördröjningen.

![](assets/throughput-latencies-overview.png)

>[!NOTE]
>
>Alla värden som presenteras i detta område är ungefärliga och endast i informationssyfte.

Som standard visas data för den aktuella dagen. Du kan ändra tidsperioden som visas genom att använda knapparna **[!UICONTROL 6 months]**, **[!UICONTROL 30 days]** och **[!UICONTROL 7 days]**.

Du kan också visa information i ett tabellformat med sorterbara kolumner i stället för i ett diagram. Du gör detta genom att klicka på knappen **[!UICONTROL Visualization settings]** och sedan välja **[!UICONTROL Table]**.

![](assets/throughput-latencies-table.png)
