---
product: campaign
solution: Campaign
title: Övervaka databaser
description: Lär dig övervaka Campaign-databasen på Kontrollpanelen
translation-type: tm+mt
source-git-commit: 2d84a5ebe8dbf42264c94f882a51180aae2a58a6
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Övervaka databaser {#database-monitoring}

## Om instansdatabaser {#about-instances-databases}

Enligt ditt avtal har var och en av era Campaign-instanser ett visst databasutrymme.

Databaser innehåller alla **resurser**, **arbetsflöden** och **data** som lagras i Adobe Campaign.

Med tiden kan databaserna nå sin maximala kapacitet, särskilt om de lagrade resurserna aldrig tas bort från instansen eller om många arbetsflöden är i pausat läge.

Överflödig instansdatabas kan leda till flera problem (oförmåga att logga in, skicka e-post osv.). Övervakning av instansens databaser är därför nödvändigt för att säkerställa optimala prestanda.

>[!NOTE]
>
>Om mängden tillgängligt databasutrymme som visas på Kontrollpanelen inte motsvarar mängden som anges i ditt avtal kan du kontakta Kundtjänst.

## Övervaka databasanvändning {#monitoring-instances-database}

![](assets/do-not-localize/how-to-video.png) Upptäck den här funktionen i video med  [Campaign ](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/performance-monitoring/monitoring-databases.html?lang=en#performance-monitoring) Classic  [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/performance-monitoring/monitoring-databases.html?lang=en#performance-monitoring)

På Kontrollpanelen kan du övervaka databasanvändningen för var och en av dina Campaign-instanser. Det gör du genom att öppna **[!UICONTROL Performance Monitoring]**-kortet och sedan välja fliken **[!UICONTROL Databases]**.

Välj önskad instans i **[!UICONTROL Instance List]** om du vill visa information om instansens databaskapacitet och hur mycket utrymme som används.

![](assets/databases_dashboard.png)

>[!NOTE]
>
>Observera att data från den här instrumentpanelen uppdateras baserat på **[!UICONTROL Database cleanup technical workflow]** som körs på din Campaign-instans (se [Campaign Standard](https://docs.adobe.com/help/en/campaign-standard/using/administrating/application-settings/technical-workflows.html#list-of-technical-workflows) och [Campaign Classic](https://docs.adobe.com/help/en/campaign-classic/using/monitoring-campaign-classic/data-processing/database-cleanup-workflow.html)-dokumentation).
>
>Du kan kontrollera den senaste gången arbetsflödet kördes under **[!UICONTROL Used Space]**- och **[!UICONTROL Provided Space]**-måtten. Observera att om arbetsflödet inte har körts sedan mer än tre dagar rekommenderar vi att du kontaktar Adobe kundtjänst så att de undersöker varför arbetsflödet inte körs.

Ytterligare mätvärden, som beskrivs nedan, finns på den här instrumentpanelen för att hjälpa dig att analysera användningen av instansens databas:

* [Databasanvändning](../../performance-monitoring/using/database-monitoring.md#database-utilization)
* [Lagringsöversikt](../../performance-monitoring/using/database-monitoring.md#storage-overview)
* [De 10 viktigaste tillfälliga resurserna](../../performance-monitoring/using/database-monitoring.md#top-10)

### Databasanvändning {#database-utilization}

Området **[!UICONTROL Database utilization]** ger en grafisk representation av minsta, genomsnittliga och högsta databasanvändning under de senaste 7 dagarna samt tröskelvärdet på 90 % för databasanvändning som representeras av en röd prickad kurva.

Om du vill ändra tidsperioden använder du de filter som finns i diagrammets övre högra hörn.

För bättre läsbarhet kan du även markera en eller flera kurvor i diagrammet. Om du vill göra det väljer du dem i **[!UICONTROL Aggregation Type]**-förklaringen.

Om du vill ha mer information om en viss tidsperiod håller du pekaren över diagrammet för att visa information om databasanvändningen som har gjorts just nu.

![](assets/databases_dashboard_detail.png)

### Lagringsöversikt {#storage-overview}

Området **[!UICONTROL Storage overview]** innehåller en grafisk representation av det utrymme som används av:

* **[!UICONTROL System resources]**

   Observera att om systemresurserna förbrukar en stor del av databasutrymmet rekommenderar vi att du kontaktar Kundtjänst.

* **[!UICONTROL Out-of-the-box tables]** som standard med era Campaign-instanser,
* **[!UICONTROL Temporary tables]** som skapats av arbetsflöden och leveranser,
* **[!UICONTROL Non-out of the box tables]** genereras när du har skapat anpassade resurser.

![](assets/database-storage-overview.png)

Klicka på knappen **[!UICONTROL View details]** om du vill ha mer information om de olika resurser som förbrukar databasutrymme.

![](assets/database-storage-details.png)

Använd filtret för att förfina sök- och visningstabeller från en viss resurstyp.

![](assets/database-storage-overview-filter.png)

### De 10 viktigaste tillfälliga resurserna {#top-10}

I **[!UICONTROL Top 10 temporary resources]**-området visas de tio största temporära resurserna som genereras av arbetsflöden och leveranser.

Övervakning av arbetsflöden och leveranser som skapar stora tillfälliga resurser är ett viktigt steg för att övervaka databasen. Om någon temporär resurs förbrukar för mycket databasutrymme bör du kontrollera att arbetsflödet eller leveransen är nödvändig och till slut navigera till instansen för att stoppa den.

>[!IMPORTANT]
>
>Den allmänna rekommendationen är att undvika att ha **fler än 40 kolumner** utanför rutresurserna.

![](assets/database-top10.png)

>[!NOTE]
>
>Om ett arbetsflöde har ett stort antal tabellräkningar eller databasstorlek rekommenderar vi att du granskar arbetsflödet för att ta reda på varför det genererar så mycket data.
>
>Campaign Standard och klassiska resurser finns också tillgängliga i slutet av den här sidan för att förhindra databasöverbelastning.

Med knappen **[!UICONTROL View all]** får du tillgång till detaljerad information om de här tillfälliga resurserna.

![](assets/database-top10-view.png)

>[!NOTE]
>
>Värdet i kolumnen **[!UICONTROL Keep interim results]** anger om alternativet är aktiverat (&quot;1&quot;) eller inaktiverat (&quot;0&quot;) i Campaign. Alternativet **[!UICONTROL Keep interim results]** är tillgängligt i arbetsflödenas egenskaper. Du kan spara resultatet av övergångarna mellan de olika aktiviteterna i ett arbetsflöde (se [Campaign Standard](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/executing-a-workflow/managing-execution-options.html) och [Campaign Classic](https://docs.adobe.com/content/help/en/campaign-classic/using/automating-with-workflows/general-operation/workflow-best-practices.html#logs)-dokumentationen).
>
>Om alternativet är aktiverat för ett av dina arbetsflöden, kan inte arbetsflödet för databasrensning frigöra det utrymme som används av mellanliggande resultat. Vi rekommenderar därför att du granskar arbetsflödet för att kontrollera om alternativet kan inaktiveras.

## Förhindrar databasöverlagring {#preventing-database-overload}

Campaign Standard och Classic erbjuder olika sätt att förhindra överförbrukning av databasdiskutrymme.

Avsnittet nedan innehåller användbara resurser från Campaign-dokumentationen som hjälper dig att optimera databasanvändningen:

**Övervakning av arbetsflöden**

* [Bästa praxis](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/workflow-general-operation/best-practices-workflows.html)  för arbetsflöden (Campaign Standard)
* [Övervaka arbetsflödeskörning](https://docs.adobe.com/help/en/campaign-classic/using/automating-with-workflows/monitoring-workflows/monitoring-workflow-execution.html)  (Campaign Classic)

**Databasunderhåll**

* Teknisk arbetsgång för databasrensning ([Campaign Standard](https://docs.adobe.com/help/en/campaign-standard/using/administrating/application-settings/technical-workflows.html#list-of-technical-workflows) / [Campaign Classic](https://docs.adobe.com/help/en/campaign-classic/using/monitoring-campaign-classic/data-processing/database-cleanup-workflow.html))
* [Underhållshandbok](https://docs.adobe.com/content/help/en/campaign-classic/using/monitoring-campaign-classic/database-maintenance/recommendations.html)  för databas (Campaign Classic)
* [Felsökning](https://docs.adobe.com/content/help/en/campaign-classic/using/monitoring-campaign-classic/troubleshooting/database-performances.html)  av databasprestanda (Campaign Classic)
* [Databasrelaterade alternativ](https://docs.adobe.com/help/en/campaign-classic/using/installing-campaign-classic/appendices/configuring-campaign-options.html#database)  (Campaign Classic)
* Datalagring ([Campaign Standard](https://docs.adobe.com/help/en/campaign-standard/using/administrating/application-settings/data-retention.html) / [Campaign Classic](https://docs.adobe.com/help/en/campaign-classic/using/configuring-campaign-classic/data-model/data-model-best-practices.html#data-retention))

>[!NOTE]
>
>Dessutom kan du få meddelanden när någon av dina databaser når sin kapacitet. Om du vill göra det prenumererar du på [e-postaviseringar](../../performance-monitoring/using/email-alerting.md).
