---
product: campaign
solution: Campaign
title: Övervaka aktiva profiler
description: Läs mer om hur man får information i realtid om den senaste och historiska användningen gällande aktiva profiler och utvecklingen för var och en av sina instanser i Campaign.
feature: Control Panel, Monitoring
role: Admin
level: Experienced
exl-id: a157cc27-577f-490f-8c4f-0f203219cfb5
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 40%

---

# Övervaka aktiva profiler {#active-profiles-monitoring}

## Om aktiva profiler {#about-active-profiles}

>[!IMPORTANT]
>
>Aktiv profilövervakning i Kontrollpanelen finns tillgängligt som betaversion och kan ofta uppdateras och ändras utan föregående meddelande. Den är tillgänglig från Campaign Standard 10368-versionen.

Enligt avtalet har var och en av instanserna i Campaign ett visst antal aktiva profiler som räknas för faktureringsändamål. Se ditt senaste avtal som referens om antalet köpta aktiva profiler.

”Profil” innebär ett register över information (såsom en post i nmsRecipient-tabellen eller en extern tabell som innehåller ett cookie-ID, Kund-ID, mobilidentifierare eller annan information som är relevant för en viss kanal) som representerar en slutkund, potentiell kund eller framtida kund.

Profiler anses vara aktiva om de har riktats in på eller kommunicerats med under de senaste tolv månaderna via någon kanal.

>[!NOTE]
>
>Facebook- och Twitter-kanaler beaktas inte.

Mer information om aktiva profiler finns i [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/profiles-and-audiences/managing-profiles/active-profiles.html) och [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/profile-management/about-profiles.html#active-profiles) dokument.

## Övervaka användningen av aktiva profiler {#monitoring-active-profiles}

>[!CONTEXTUALHELP]
>id="cp_performancemonitoring_active_profile"
>title="Om övervakning av aktiva profiler"
>abstract="På den här fliken kan du få information i realtid om den senaste och historiska aktiva profilanvändningen och utvecklingen för varje profil i era Campaign-instanser och i er organisation."

Information om användning av aktiva profiler uppdateras på Kontrollpanelen baserat på dedikerad [!DNL Campaign] tekniska arbetsflöden som körs varje dag på dina instanser:
* Arbetsflödet [”Fakturering”](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/technical-workflows.html?lang=sv) i Campaign Standard,
* The [Antal aktiva faktureringsprofiler](https://experienceleague.adobe.com/docs/campaign-classic/using/automating-with-workflows/advanced-management/about-technical-workflows.html?lang=sv) arbetsflöde för Campaign v7/v8.


Om du vill övervaka din aktiva profilanvändning på Kontrollpanelen går du till **[!UICONTROL Performance Monitoring]** kort > **[!UICONTROL Active Profiles]** och väljer önskad instans på **[!UICONTROL Instance List]**.

Det visas information om hur du använder aktiva profiler.

![](assets/active-profiles-graph.png)

I det övre avsnittet visas följande information:

* Antalet aktiva profiler som för närvarande används i den valda instansen, tillsammans med tidsstämpeln för den senaste körningen av faktureringsarbetsflödet för instansen.

* Det totala antalet aktiva profiler som används i hela organisationen inom alla instanser.

  >[!NOTE]
  >
  >Det här avsnittet visas bara om du har flera instanser kopplade till din organisation.

* Det totala antalet aktiva profiler som har tilldelats din organisation.

I det nedre avsnittet visas hur den aktiva profilen har använts under de senaste 30 dagarna. Du kan ändra den här tidsramen till 1 år med filtret i det övre högra hörnet. Genom att hålla pekaren över diagrammet kan du få det exakta antalet aktiva profiler som används för den valda perioden.
