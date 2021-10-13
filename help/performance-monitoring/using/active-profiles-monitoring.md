---
product: campaign
solution: Campaign
title: Övervaka aktiva profiler
description: Läs mer om hur man får information i realtid om den senaste och historiska användningen gällande aktiva profiler och utvecklingen för var och en av sina instanser i Campaign.
feature: Control Panel
role: Architect
level: Experienced
exl-id: a157cc27-577f-490f-8c4f-0f203219cfb5
source-git-commit: 62ad3edb604ebd9fab6a3f930b7c79af6b9ca968
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 78%

---

# Övervaka aktiva profiler {#active-profiles-monitoring}

## Om aktiva profiler {#about-active-profiles}

>[!IMPORTANT]
>
>Att övervaka aktiva profiler i Kontrollpanelen finns tillgängligt som betaversion och kan ofta uppdateras och ändras utan föregående meddelande. Den är tillgänglig från Campaign Standard 10368-versionen.

Enligt avtalet har var och en av instanserna i Campaign ett visst antal aktiva profiler som räknas för faktureringsändamål. Se ditt senaste avtal som referens om antalet köpta aktiva profiler.

”Profil” innebär ett register över information (såsom en post i nmsRecipient-tabellen eller en extern tabell som innehåller ett cookie-ID, Kund-ID, mobilidentifierare eller annan information som är relevant för en viss kanal) som representerar en slutkund, potentiell kund eller framtida kund.

Profiler anses vara aktiva om de har riktats in på eller kommunicerats med under de senaste tolv månaderna via någon kanal.

>[!NOTE]
>
>Facebook- och Twitter-kanaler beaktas inte.

Mer information om aktiva profiler finns i [Campaign Standard](https://https://experienceleague.adobe.com/docs/campaign-standard/using/profiles-and-audiences/managing-profiles/active-profiles.html) och [Campaign Classic v7](https://https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/profile-management/about-profiles.html#active-profiles)-dokumentation.

## Övervaka aktiva profiler {#monitoring-active-profiles}

>[!CONTEXTUALHELP]
>id="cp_performancemonitoring_active_profile"
>title="Om övervakning av aktiva profiler"
>abstract="På den här fliken kan du få information i realtid om den senaste och historiska aktiva profilanvändningen och utvecklingen för var och en av era Campaign-instanser."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/performance-monitoring/about-performance-monitoring.html?lang=en" text="Prestandaövervakning"

Kontrollpanelen låter dig övervaka användningen av aktiva profiler för var och en av instanserna i Campaign.

Följ dessa steg för att göra detta:

1. Öppna **[!UICONTROL Performance Monitoring]**-kortet och välj fliken **[!UICONTROL Active Profiles]**.

1. Välj önskad instans i **[!UICONTROL Instance List]**.

1. Antalet aktiva profiler som används av instansen visas liksom den senaste gången faktureringens arbetsflöde kördes på instansen.

![](assets/active-profiles-graph.png)

>[!NOTE]
>
>Aktiva profiler räknas baserat på dedikerade tekniska arbetsflöden som körs varje dag på instanserna:
>
>* Arbetsflödet [”Fakturering”](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/technical-workflows.html?lang=sv) i Campaign Standard,
>* Arbetsflödet [”Antal aktiva faktureringsprofiler”](https://experienceleague.adobe.com/docs/campaign-classic/using/automating-with-workflows/advanced-management/about-technical-workflows.html) i Campaign Classic.


Det nedre området visar de aktiva profilernas användning under de senaste 30 dagarna. Du kan ändra den tidsperiod som visas upp till ett år med de tillgängliga filtren i det övre högra hörnet.

Håll muspekaren över ett av diagrammen för att få det exakta antalet aktiva profiler som använts för den valda tidsperioden.
