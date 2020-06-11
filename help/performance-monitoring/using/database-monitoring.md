---
title: Databasövervakning
description: Lär dig övervaka Campaign-databasen på Kontrollpanelen
translation-type: tm+mt
source-git-commit: b2447b30314f4bd46b2b6e144f7f713ff2f1ec59
workflow-type: tm+mt
source-wordcount: '443'
ht-degree: 1%

---


# Databasövervakning {#database-monitoring}

## About instances databases {#about-instances-databases}

According to your contract, each of your Campaign instances is provisioned with a specific amount of database space.

Databases include all **assets**, **workflows** and **data** that is stored in Adobe Campaign.

Over time, databases can reach their maximum capacity, especially if the stored resources are never deleted from the instance, or if there are many workflows in a paused state.

Överflödig instansdatabas kan leda till flera problem (oförmåga att logga in, skicka e-post osv.). Övervakning av instansens databaser är därför nödvändigt för att säkerställa optimala prestanda.

>[!NOTE]
>
>Mängden databasutrymme som visas på Kontrollpanelen kanske inte motsvarar mängden databasutrymme som anges i kontraktet. I de flesta fall får du tillfälligt större databasutrymme för att säkerställa systemets prestanda.

## Övervaka databasanvändning {#monitoring-instances-database}

På Kontrollpanelen kan du övervaka databasanvändningen för var och en av dina Campaign-instanser. Gör så här:

1. Öppna **[!UICONTROL Performance Monitoring]**-kortet och välj fliken **[!UICONTROL Databases]**.

1. Markera önskad instans i **[!UICONTROL Instance List]**.

   Det övre området innehåller information om instansens databaskapacitet och hur mycket utrymme som används.

   ![](assets/databases_dashboard.png)

   Det undre området ger en grafisk representation av minsta, genomsnittliga och högsta databasanvändning under de senaste 7 dagarna, samt tröskelvärdet på 90 % databasanvändning, som representeras av en röd prickad kurva.

   Du kan ändra den tidsperiod som visas med de tillgängliga filtren i det övre högra hörnet.

   För bättre läsbarhet kan du även markera en eller flera kurvor i diagrammet. Om du vill göra det väljer du dem i **[!UICONTROL Aggregation Type]** teckenförklaringen.

   Genom att hålla pekaren över diagrammet kan du få detaljerad information om den valda tidsperioden.

   ![](assets/databases_dashboard_detail.png)

>[!NOTE]
>
>Utöver den här instrumentpanelen kan du få meddelanden när någon av dina databaser når sin kapacitet. Prenumerera på [e-postaviseringar för att göra detta](../../performance-monitoring/using/email-alerting.md)

## Förhindra databasöverlagring {#preventing-database-overload}

Campaign Standard och Classic erbjuder olika sätt att förhindra överförbrukning av databasdiskutrymme.

Avsnittet nedan innehåller användbara resurser från Campaign-dokumentationen som hjälper dig att optimera databasanvändningen:

**Övervakning av arbetsflöden**

* [Bästa praxis](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/workflow-general-operation/best-practices-workflows.html) för arbetsflöden (Campaign Standard)
* [Övervaka arbetsflödeskörning](https://docs.adobe.com/help/en/campaign-classic/using/automating-with-workflows/monitoring-workflows/monitoring-workflow-execution.html) (Campaign Classic)

**Databasunderhåll**

* Tekniskt arbetsflöde för databasrensning ([Campaign Standard](https://docs.adobe.com/help/en/campaign-standard/using/administrating/application-settings/technical-workflows.html#list-of-technical-workflows) / [Campaign Classic](https://docs.adobe.com/help/en/campaign-classic/using/monitoring-campaign-classic/data-processing/database-cleanup-workflow.html))
* [Underhållshandbok](https://docs.adobe.com/content/help/en/campaign-classic/using/monitoring-campaign-classic/database-maintenance/recommendations.html) för databas (Campaign Classic)
* [Felsökning](https://docs.adobe.com/content/help/en/campaign-classic/using/monitoring-campaign-classic/troubleshooting/database-performances.html) av databasprestanda (Campaign Classic)
* [Databasrelaterade alternativ](https://docs.adobe.com/help/en/campaign-classic/using/installing-campaign-classic/appendices/configuring-campaign-options.html#database) (Campaign Classic)
