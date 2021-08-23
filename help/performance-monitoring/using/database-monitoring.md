---
product: campaign
solution: Campaign
title: Övervaka databaser
description: Läs om hur du övervakar din Campaign-databas i Kontrollpanelen
feature: 'Kontrollpanelen  '
role: Architect
level: Experienced
exl-id: bb9e1ce3-2472-4bc1-a82a-a301c6bf830e
source-git-commit: c29b6d4bf59628a10f6b8e402176b1835770fc54
workflow-type: tm+mt
source-wordcount: '956'
ht-degree: 85%

---

# Övervaka databaser {#database-monitoring}

## Om instansdatabaser {#about-instances-databases}

Enligt ditt avtal har var och en av dina instanser i Campaign ett visst databasutrymme.

Databaser innehåller alla **resurser**, **arbetsflöden** och **data** som lagras i Adobe Campaign.

Med tiden kan databaserna nå sin maximala kapacitet, särskilt om de lagrade resurserna aldrig tas bort från instansen eller om många arbetsflöden är i ett pausat läge.

En överfull instansdatabas kan leda till flera problem (oförmåga att logga in, skicka e-post osv.). Övervakning av instansens databaser är därför nödvändigt för att säkerställa optimala prestanda.

>[!NOTE]
>
>Om mängden tillgängligt databasutrymme som visas på Kontrollpanelen inte motsvarar mängden som anges i ditt avtal ska du kontakta kundtjänst.

## Övervaka databasanvändning {#monitoring-instances-database}

![](assets/do-not-localize/how-to-video.png) Upptäck den här funktionen via video med [Campaign Classic](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/performance-monitoring/monitoring-databases.html?lang=sv#performance-monitoring) eller [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/performance-monitoring/monitoring-databases.html?lang=sv#performance-monitoring)

Kontrollpanelen låter dig övervaka användningen av databaser för var och en av instanserna i Campaign. Det gör du genom att öppna kortet **[!UICONTROL Performance Monitoring]** och sedan välja fliken **[!UICONTROL Databases]**.

Välj önskad instans i **[!UICONTROL Instance List]** om du vill visa information om instansens databaskapacitet och hur mycket utrymme som används.

![](assets/databases_dashboard.png)

>[!NOTE]
>
>Observera att data från den här instrumentpanelen uppdateras baserat på **[!UICONTROL Database cleanup technical workflow]** som körs på din instans i Campaign (se dokumentationen om [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/technical-workflows.html?lang=en#list-of-technical-workflows) och [Campaign Classic](https://experienceleague.adobe.com/docs/campaign-classic/using/monitoring-campaign-classic/data-processing/database-cleanup-workflow.html?lang=en)).
>
>Du kan också få meddelanden när en av dina databaser når sin kapacitet efter senaste gången arbetsflödet kördes, under måtten **[!UICONTROL Used Space]** och **[!UICONTROL Provided Space]** Observera att om arbetsflödet inte har körts sedan mer än tre dagar rekommenderar vi att du kontaktar kundtjänsten hos Adobe så att de undersöker varför arbetsflödet inte körs.

Ytterligare mätvärden, som beskrivs nedan, är tillgängliga på den här instrumentpanelen för att hjälpa dig att analysera hur instansens databas används.

### Databasanvändning {#database-utilization}

Området **[!UICONTROL Database utilization]** ger en grafisk representation av den minsta, genomsnittliga och högsta databasanvändningen under de senaste 7 dagarna samt tröskelvärdet för 90 % av databasanvändning som representeras av en röd prickad kurva.

Om du vill ändra tidsperioden använder du de filter som finns i diagrammets övre högra hörn.

För bättre läsbarhet kan du även markera en eller flera kurvor i diagrammet. Om du vill göra det väljer du dem i förklaringen **[!UICONTROL Aggregation Type]**.

Om du vill ha mer information om en viss tidsperiod håller du pekaren över diagrammet för att visa information om databasanvändningen under den perioden.

![](assets/databases_dashboard_detail.png)

### Lagringsöversikt {#storage-overview}

Området **[!UICONTROL Storage overview]** innehåller en grafisk representation av det utrymme som används av:

* **[!UICONTROL System resources]**

   Observera att om systemresurserna förbrukar en stor del av databasutrymmet rekommenderar vi att du kontaktar kundtjänst.

* **[!UICONTROL Out-of-the-box tables]** kommer som standard med dina instanser i Campaign,
* **[!UICONTROL Temporary tables]** som skapats av arbetsflöden och leveranser,
* **[!UICONTROL Non-out of the box tables]** som genererades när du skapade anpassade resurser.

![](assets/database-storage-overview.png)

Klicka på knappen **[!UICONTROL View details]** om du vill ha mer information om de olika resurser som förbrukar databasutrymme.

![](assets/database-storage-details.png)

Använd filtret för att förfina sökningen och bara visa tabeller från en viss resurstyp.

![](assets/database-storage-overview-filter.png)

### De 10 viktigaste tillfälliga resurserna {#top-10}

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

Värdet i kolumnen **[!UICONTROL Keep interim results]** anger om alternativet är aktiverat (&quot;1&quot;) eller inaktiverat (&quot;0&quot;) i Campaign. Du kan spara resultatet av övergångarna mellan de olika aktiviteterna i ett arbetsflöde (se dokumentationen om [Campaign Standard](https://https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/executing-a-workflow/managing-execution-options.html) och [Campaign Classic](https://https://experienceleague.adobe.com/docs/campaign-classic/using/automating-with-workflows/general-operation/workflow-best-practices.html#logs) ).

>[!IMPORTANT]
>
>Det här alternativet får aldrig kontrolleras i ett produktionsarbetsflöde. Det används för att analysera resultaten och är endast avsett för testning och ska därför endast användas i utvecklings- eller stagingmiljöer.
>
>Om värdet på Kontrollpanelen anger att alternativet är aktiverat för ett av dina arbetsflöden rekommenderar vi att du inaktiverar det i Campaign.

## Förhindra databasöverbelastning {#preventing-database-overload}

Campaign Standard och Classic erbjuder olika sätt att förhindra överanvändning av databasens diskutrymme.

Avsnittet nedan innehåller användbara resurser från dokumentationen om Campaign som hjälper dig att optimera databasanvändningen:

**Övervakning av arbetsflöden**

* [God praxis för arbetsflöden](https://https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/workflow-general-operation/best-practices-workflows.html) (Campaign Standard)
* [Övervaka arbetsflödeskörning](https://experienceleague.adobe.com/docs/campaign-classic/using/automating-with-workflows/monitoring-workflows/monitoring-workflow-execution.html?lang=en) (Campaign Classic)

**Databasunderhåll**

* Teknisk arbetsgång för databasrensning: [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/technical-workflows.html?lang=en#list-of-technical-workflows) - [Campaign Classic](https://experienceleague.adobe.com/docs/campaign-classic/using/monitoring-campaign-classic/data-processing/database-cleanup-workflow.html?lang=en)
* [Användarhandbok om databasunderhåll](https://https://experienceleague.adobe.com/docs/campaign-classic/using/monitoring-campaign-classic/database-maintenance/recommendations.html) (Campaign Classic)
* [Felsökning av databasprestanda](https://experienceleague.adobe.com/docs/campaign-classic/using/monitoring-campaign-classic/troubleshooting-toc/database-issues-toc/database-performances.html?lang=sv) (Campaign Classic)
* [Databasrelaterade alternativ](https://experienceleague.adobe.com/docs/campaign-classic/using/installing-campaign-classic/appendices/configuring-campaign-options.html?lang=en#database) (Campaign Classic)
* Datalagring: [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/data-retention.html?lang=en) - [Campaign Classic](https://experienceleague.adobe.com/docs/campaign-classic/using/configuring-campaign-classic/data-model/data-model-best-practices.html?lang=en#data-retention)

>[!NOTE]
>
>Dessutom kan du få meddelanden när någon av dina databaser nästan är nått full kapacitet. Om du vill göra det ska du prenumerera på [e-postaviseringar](../../performance-monitoring/using/email-alerting.md).
