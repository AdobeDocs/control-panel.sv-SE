---
product: campaign
solution: Campaign
title: Hantera SFTP-lagring
description: Läs om hur man övervakar och hanterar SFTP-serverns lagring
feature: Control Panel
role: Architect
level: Experienced
exl-id: eaf67573-f088-47d9-8a25-273d08dc541a
source-git-commit: cca04cd965c00a9e2bc496de632ee41ce53a166a
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 93%

---

# Hantera SFTP-lagring {#sftp-storage-management}

>[!CONTEXTUALHELP]
>id="cp_storage"
>title="Om lagringskapacitet"
>abstract="Den här fliken visar information om lagringskapacitet och utnyttjande för SFTP-servrarna. Endast SFTP-servrar som du har åtkomst till visas här. Kontakta din administratör för att begära åtkomst till andra SFTP-servrar."
>additional-url="https://images-tv.adobe.com/mpcv3/8a977e03-d76c-44d3-853c-95d0b799c870_1560205338.1920x1080at3000_h264.mp4" text="Se demovideon"

Olika lagringskapaciteter kan tillhandahållas på SFTP-servern beroende på dina avtalsvillkor.

Det är viktigt att du regelbundet övervakar tillgängligt utrymme för var och en av SFTP-servrarna. I annat fall kan det vara omöjligt att spara ytterligare filer på servern eller köra arbetsflöden som är beroende av uppdateringarna från den här servern.

![](assets/do-not-localize/how-to-video.png) Upptäck den här funktionen via video med [Campaign Classic](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/sftp-management/monitoring-server-capacity.html#sftp-management) eller [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/sftp-management/monitoring-server-capacity.html#sftp-management)

## Åtkomst till information om lagringskapacitet {#accessing-storage-capacity-information}

**[!UICONTROL Storage]**-fliken på SFTP-kortet visar information om det diskutrymme som används av alla instanser som du har åtkomst till. Den uppdateras varje gång sidan uppdateras.

![](assets/control_panel_space.png)

För varje instans visas en visuell varning som anger när dess lagring överskrider kapaciteten:

* **Orange**: instansen överskred 80 % av sin kapacitet.
* **Röd**: instansen överskred 90 % av sin kapacitet.

Det finns även fler tips som hjälper dig med vad du bör göra när servern närmar sig sin maximala kapacitet.

## Bästa praxis när lagringskapaciteten tar slut {#best-practices-when-capacity-runs-out}

1. **Rensa SFTP-servern från gamla eller onödiga filer**. Se [det här avsnittet](../../sftp/using/logging-into-sftp-server.md) för mer information om hur du får åtkomst till SFTP-serverns mapp.
1. Se till att **arbetsflödena** som rensar SFTP-servrarna körs. Se den särskilda dokumentationen om [Campaign Classic](https://experienceleague.adobe.com/docs/campaign-classic/using/automating-with-workflows/advanced-management/about-technical-workflows.html) och [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/technical-workflows.html?lang=sv) för mer information om tekniska arbetsflöden i Adobe Campaign.
1. Kontakta ditt kontoteam för att **begära mer lagringsutrymme** (extra avgifter kan tillkomma).
1. Kontakta **Kundtjänst** om du tror att det är något problem.
