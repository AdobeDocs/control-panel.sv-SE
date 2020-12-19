---
product: campaign
solution: Campaign
title: E-postavisering
description: Lär dig hur du tar emot e-postmeddelanden i händelse av problem med dina Campaign-instanser
translation-type: tm+mt
source-git-commit: 168ae32d7931497bb37d63f7dd1d14eadbb4b1bf
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 2%

---


# E-postavisering {#email-alerting}

Kontrollpanelen är utrustad med e-postaviseringsfunktioner i realtid för att ge större flexibilitet i arbetet.

Så här prenumererar du på dessa aviseringar:

1. Klicka på knappen **[!UICONTROL Alerting notifications]** som är tillgänglig från valfri plats på kontrollpanelen och klicka sedan på **[!UICONTROL Subscribe]**.

   ![](assets/subscribing.png)

1. Ett e-postmeddelande skickas för att bekräfta din prenumeration.

   ![](assets/email_subscription.png)

1. Efter prenumerationen kommer Kontrollpanelen att meddela om systemproblem och rekommendera vilka åtgärder som ska vidtas. E-postaviseringar skickas till alla som har registrerat sig för **alla instanser** som de är administratörer för.

   ![](assets/alert_sample.png)


Listan med varningar är följande:

* **Användning** av SFTP-lagring: En av dina SFTP-servrar har nått 80 % eller mer av sin kapacitet. Se [SFTP-lagringshantering](../../sftp/using/sftp-storage-management.md).

* **Databasanvändning**: En av instansdatabaserna har nått 80 % eller mer av sin kapacitet. Se [Databasövervakning](../../performance-monitoring/using/database-monitoring.md).

* **SSL-certifikatets förfallodatum**: En av dina underdomäners SSL-certifikat har gått ut eller går ut om 60 dagar eller mindre. Se [Övervaka underdomäners SSL-certifikat](../../subdomains-certificates/using/monitoring-ssl-certificates.md).

