---
product: campaign
solution: Campaign
title: E-postavisering
description: Lär dig hur du tar emot e-postmeddelanden i händelse av problem med dina Campaign-instanser
feature: Control Panel, Monitoring
role: Admin
level: Experienced
exl-id: 7942d2b1-d28f-4760-aa25-5ba94a627fd0
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 2%

---

# E-postavisering {#email-alerting}

Kontrollpanelen är utrustad med e-postaviseringsfunktioner i realtid för att ge större flexibilitet i arbetet.

## Lista över aviseringar {#list}

Listan med varningar är följande:

* **SFTP-lagringsanvändning**: En av dina SFTP-servrar har nått 80 % eller mer av sin kapacitet. Se [Hantering av SFTP-lagring](../../sftp/using/sftp-storage-management.md).

* **Databasanvändning**: En av instansdatabaserna har nått 80 % eller mer av sin kapacitet. Se [Databasövervakning](../../performance-monitoring/using/database-monitoring.md).

* **SFTP IP tillåter att listan över IP-intervall upphör**: Ett av IP-intervallen som du har definierat har gått ut eller går ut om 10 dagar eller mindre. Se [Lista över tillåtna IP-intervall](../../sftp/using/ip-range-allow-listing.md).

* **Giltighetstid för offentlig SFTP-nyckel**: En av de offentliga nycklarna som du har definierat har gått ut eller går ut om 10 dagar eller mindre. Se [Nyckelhantering](../../sftp/using/key-management.md).

* **SSL-certifikatets förfallodatum**: En av dina underdomäners SSL-certifikat har gått ut eller går ut om 30 dagar eller mindre. Se [Övervaka underdomäners SSL-certifikat](../../subdomains-certificates/using/monitoring-ssl-certificates.md).

<!--* **Long running Queries**: A query has been running for more than 24 hours on one of your instances. See [Monitoring active queries](database-active-queries.md).-->

>[!NOTE]
>
>På Kontrollpanelen kan du dessutom **ställa in påminnelser** så att du kan meddelas via e-post innan en händelse inträffar på dina instanser (releaser och servicegranskningar).
>
>Om du vill göra det måste du prenumerera på e-postaviseringar och ställa in en påminnelse för de kommande händelserna. [Lär dig hur du ställer in påminnelser för kommande evenemang](../../service-events/service-events.md#reminders)

## Prenumerera på aviseringar {#subscribe}

Så här prenumererar du på dessa aviseringar:

1. Klicka på knappen **[!UICONTROL Alerting notifications]** som är tillgänglig från valfri plats på kontrollpanelen och klicka sedan på **[!UICONTROL Subscribe]**.

   ![](assets/subscribing.png)

1. Ett e-postmeddelande skickas för att bekräfta prenumerationen.

   ![](assets/email_subscription.png)

1. Efter prenumerationen kommer Kontrollpanelen att meddela om systemproblem och rekommendera vilka åtgärder som ska vidtas. E-postaviseringar skickas till alla som har registrerat sig för **alla instanser** som de är administratörer för.

   ![](assets/alert_sample.png)
