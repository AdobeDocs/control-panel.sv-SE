---
title: Övervaka aktiva profiler
description: Läs mer om hur man får information i realtid om den senaste och historiska användningen gällande aktiva profiler och utvecklingen för var och en av sina instanser i Campaign.
translation-type: ht
source-git-commit: 024eb750021ff2446b34d648b5abfb016eabc289
workflow-type: ht
source-wordcount: '389'
ht-degree: 100%

---


# Övervaka aktiva profiler {#active-profiles-monitoring}

>[!IMPORTANT]
>
>Att övervaka aktiva profiler i Kontrollpanelen finns tillgängligt som betaversion och kan ofta uppdateras och ändras utan föregående meddelande.
>
>Funktionen är tillgänglig för kunder som har AWS som värd från Campaign Standard build 10368 och Campaign Classic build 8931. Om du använder en tidigare build måste du uppgradera för att kunna använda den här funktionen.

## Om aktiva profiler {#about-active-profiles}

Enligt avtalet har var och en av instanserna i Campaign ett visst antal aktiva profiler som räknas för faktureringsändamål. Se ditt senaste avtal som referens om antalet köpta aktiva profiler.

”Profil” innebär ett register över information (såsom en post i nmsRecipient-tabellen eller en extern tabell som innehåller ett cookie-ID, Kund-ID, mobilidentifierare eller annan information som är relevant för en viss kanal) som representerar en slutkund, potentiell kund eller framtida kund.

Profiler anses vara aktiva om de har riktats in på eller kommunicerats med under de senaste tolv månaderna via någon kanal.

>[!NOTE]
>
>Facebook- och Twitter-kanaler beaktas inte.

Se dokumentationen för [Campaign Standard](https://docs.adobe.com/content/help/sv-SE/campaign-standard/using/profiles-and-audiences/managing-profiles/active-profiles.html) och [Campaign Classic](https://docs.adobe.com/content/help/sv-SE/campaign-classic/using/getting-started/profile-management/about-profiles.html#active-profiles) för mer information om aktiva profiler.

## Övervaka aktiva profiler {#monitoring-active-profiles}

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
>* Arbetsflödet [”Fakturering”](https://docs.adobe.com/help/sv-SE/campaign-standard/using/administrating/application-settings/technical-workflows.html) i Campaign Standard,
>* Arbetsflödet [”Antal aktiva faktureringsprofiler”](https://docs.adobe.com/content/help/sv-SE/campaign-classic/using/automating-with-workflows/technical-workflows/deliveries.html) i Campaign Classic.


Det nedre området visar de aktiva profilernas användning under de senaste 30 dagarna. Du kan ändra den tidsperiod som visas upp till ett år med de tillgängliga filtren i det övre högra hörnet.

Håll muspekaren över ett av diagrammen för att få det exakta antalet aktiva profiler som använts för den valda tidsperioden.
