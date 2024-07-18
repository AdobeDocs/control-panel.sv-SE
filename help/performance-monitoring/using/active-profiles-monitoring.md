---
product: campaign
solution: Campaign
title: Övervaka aktiva profiler
description: Läs mer om hur man får information i realtid om den senaste och historiska användningen gällande aktiva profiler och utvecklingen för var och en av sina instanser i Campaign.
feature: Control Panel, Monitoring
role: Admin
level: Experienced
exl-id: a157cc27-577f-490f-8c4f-0f203219cfb5
source-git-commit: 73cf3102c0926728595e975ee4c85bf110f2a23d
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 100%

---

# Övervaka aktiva profiler {#active-profiles-monitoring}

## Om aktiva profiler {#about-active-profiles}

>[!IMPORTANT]
>
>Aktiv profilövervakning i Kontrollpanelen finns tillgängligt som betaversion och kan ofta uppdateras och ändras utan föregående meddelande. Den är tillgänglig från Campaign Standard, build 10368.

Enligt avtalet har var och en av instanserna i Campaign ett visst antal aktiva profiler som räknas för faktureringsändamål. Se ditt senaste avtal som referens om antalet köpta aktiva profiler.

”Profil” innebär ett register över information (såsom en post i nmsRecipient-tabellen eller en extern tabell som innehåller ett cookie-ID, Kund-ID, mobilidentifierare eller annan information som är relevant för en viss kanal) som representerar en slutkund, potentiell kund eller framtida kund.

Profiler anses vara aktiva om de har riktats in på eller kommunicerats med under de senaste tolv månaderna via någon kanal.

>[!NOTE]
>
>Facebook- och X-kanaler (tidigare Twitter) beaktas inte.

För mer om aktiva profiler, se dokumentationen om [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/profiles-and-audiences/managing-profiles/active-profiles.html?lang=sv) och [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/profile-management/about-profiles.html?lang=sv#active-profiles).

## Övervaka användningen av aktiva profiler {#monitoring-active-profiles}

>[!CONTEXTUALHELP]
>id="cp_performancemonitoring_active_profile"
>title="Om övervakning av aktiva profiler"
>abstract="På den här fliken kan du få realtidsinformation om både den senaste och den historiska profilanvändningen samt utvecklingen för var och en av dina instanser i Campaign och din organisation."

Om du vill övervaka din aktiva profilanvändning på Kontrollpanelen går du till fliken **[!UICONTROL Performance Monitoring]** kort > **[!UICONTROL Active Profiles]** och väljer önskad instans på **[!UICONTROL Instance List]**.

Det visas information om hur du använder aktiva profiler.

![](assets/active-profiles-graph.png)

I det övre avsnittet visas följande information:

* Antalet aktiva profiler som för närvarande används i den valda instansen, tillsammans med tidsstämpeln för den senaste körningen av faktureringsarbetsflödet för instansen.

* Det totala antalet aktiva profiler som används i hela organisationen inom alla instanser.

  >[!NOTE]
  >
  >Det här avsnittet visas bara om du har flera instanser kopplade till din organisation.

* Det totala antalet aktiva profiler som har tilldelats din organisation.

Den nedre delen ger en visuell representation av aktiv profilanvändning under de senaste 30 dagarna. Du kan ändra den här tidsramen till ett år med filtret i det övre högra hörnet. Genom att hålla muspekaren över grafen kan du få det exakta antalet aktiva profiler som används under den valda perioden.

Information om användning av aktiva profiler uppdateras på Kontrollpanelen baserat på dedikerade tekniska arbetsflöden för Fakturering i [!DNL Campaign] som körs regelbundet på dina instanser:

| Campaign-version | Tekniskt arbetsflöde | Körningar |
|  ---  |  ---  |  ---  |
| Campaign Standard | [Fakturering](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/technical-workflows.html?lang=sv) | Dagligen |
| Campaign v7/v8 | [Fakturering](https://experienceleague.adobe.com/docs/campaign-classic/using/automating-with-workflows/advanced-management/about-technical-workflows.html?lang=sv) | Månatligen |

