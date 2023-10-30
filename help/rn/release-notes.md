---
title: Senaste versionen
description: På den här sidan listas alla nya funktioner och förbättringar för Kontrollpanelen
feature: Control Panel, Release Notes
role: Admin
level: Experienced
exl-id: 13aceffb-ceaa-4cfe-8741-95d66c5c6caa
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 100%

---

# Senaste versionen {#control-panel-releases}

På den här sidan listas de nya funktionerna och förbättringarna för Kontrollpanelen.

## Oktober 2023 {#october-2023}

**Användargränssnitt**

* Kontrollpanelen finns nu på ytterligare språk. [Läs mer](../discover/using/discovering-the-interface.md#supported-languages-languages)

**Övervaka aktiva profiler**

* Du kan nu övervaka antalet aktiva profiler som du är berättigad till för din organisation och det totala antalet profiler som används i din organisation i alla instanser, om du använder flera instanser. [Läs mer](../performance-monitoring/using/active-profiles-monitoring.md)

**DMARC-poster**

* Flera e-postadresser kan nu ta emot en aggregatrapport och e-postmeddelanden med felrapporter. [Läs mer](../subdomains-certificates/using/dmarc.md)
* Ändringar har gjorts om det finns både DMARC- och BIMI-poster för en underdomän:

   * DMARC-poster kan inte tas bort. Om du vill radera en måste du först radera BIMI-posten.
   * DMARC-poster kan redigeras, men principnedgraderingen till Ingen tillåts inte och dess procentvärde måste vara 100.

