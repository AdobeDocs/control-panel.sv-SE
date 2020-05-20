---
title: SFTP-lagringshantering
description: Lär dig övervaka och hantera din SFTP-servers lagring
translation-type: tm+mt
source-git-commit: 834adb7c937a9927901f91e257a8df44e72ca45b
workflow-type: tm+mt
source-wordcount: '351'
ht-degree: 3%

---


# SFTP-lagringshantering {#sftp-storage-management}

>[!CONTEXTUALHELP]
>id="cp_storage"
>title="Om lagringskapacitet"
>abstract="På den här fliken kan du visa information om lagringskapacitet och utnyttjande för dina SFTP-servrar. Endast SFTP-servrar som du har åtkomst till visas här. Kontakta administratören för att begära åtkomst till andra SFTP-servrar."
>additional-url="https://images-tv.adobe.com/mpcv3/8a977e03-d76c-44d3-853c-95d0b799c870_1560205338.1920x1080at3000_h264.mp4" text="Se filmen"

Du kan ha olika lagringskapacitet som tillhandahålls på SFTP-servern, beroende på dina avtalsvillkor.

Det är viktigt att du regelbundet övervakar tillgängligt utrymme för var och en av dina SFTP-servrar. Annars kanske du inte längre kan spara några ytterligare filer på servern eller köra arbetsflöden som är beroende av uppdateringarna från den här servern.

**Relaterade ämnen:**

* [Självstudievideo om Campaign Standard](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/monitoring-server-capacity-whitelisting-adding-ssh-key.html)
* [Kampanj - klassisk självstudievideo](https://docs.adobe.com/content/help/en/campaign-learn/campaign-classic-tutorials/administrating/control-panel-acc/managing-sftp-servers.html)

## Åtkomst till information om lagringskapacitet {#accessing-storage-capacity-information}

Information om det utrymme som används av alla instanser som du har åtkomst till finns på fliken **[!UICONTROL Storage]** i SFTP-kortet. Den uppdateras varje gång sidan uppdateras.

![](assets/control_panel_space.png)

För varje instans visas en visuell varning som anger när dess lagringskapacitet överskrider sin kapacitet:

* **Orange**: instansen överskred 80 % av sin kapacitet,
* **Röd**: förekomsten överstiger 90 % av sin kapacitet.

Det finns även fler tips som hjälper dig att veta hur du ska gå vidare när servern närmar sig sin kapacitet.

## Bästa tillvägagångssätt när lagringskapaciteten tar slut {#best-practices-when-capacity-runs-out}

1. **Rensa SFTP-servern från gamla eller onödiga filer**. Mer information om hur du får åtkomst till din SFTP-servermapp finns i [det här avsnittet](../../sftp/using/logging-into-sftp-server.md).
1. Kontrollera att **arbetsflödena** som rensar dina SFTP-servrar körs. Mer information om tekniska arbetsflöden i Adobe Campaign finns i de dedikerade dokumenten för [Campaign Classic](https://docs.campaign.adobe.com/doc/AC/en/WKF__General_operation_Building_a_workflow.html#Technical_workflows) och [Campaign Standard](https://helpx.adobe.com/campaign/standard/administration/using/technical-workflows.html) .
1. Kontakta ditt kontoteam för att **begära mer lagringsutrymme** (extra avgifter kan tillkomma).
1. Kontakta **kundtjänst** om du tror att det är något problem.
