---
product: campaign
solution: Campaign
title: E-postavisering
description: Lär dig hur du tar emot e-postmeddelanden i händelse av problem med dina Campaign-instanser
feature: Control Panel
role: Architect
level: Experienced
exl-id: 7942d2b1-d28f-4760-aa25-5ba94a627fd0
source-git-commit: 80a96152ffcfa184fbeb6fc5cddcb119655ffab1
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 2%

---

# E-postavisering {#email-alerting}

Kontrollpanelen är utrustad med e-postaviseringsfunktioner i realtid för att ge större flexibilitet i arbetet.

## Lista över aviseringar {#list}

Listan med varningar är följande:

* **SFTP-lagringsanvändning**: En av dina SFTP-servrar har nått 80 % eller mer av sin kapacitet. Se [Hantering av SFTP-lagring](../../sftp/using/sftp-storage-management.md).

* **Databasanvändning**: En av instansdatabaserna har nått 80 % eller mer av sin kapacitet. Se [Databasövervakning](../../performance-monitoring/using/database-monitoring.md).

* **SFTP IP-listan tillåter att listan går ut**: Ett av IP-intervallen som du har definierat har gått ut eller går ut om 10 dagar eller mindre. Se [IP-intervall tillåter listning](../../sftp/using/ip-range-allow-listing.md).

* **SFTP-utgångsdatum för offentlig nyckel**: En av de offentliga nycklarna som du har definierat har gått ut eller går ut om 10 dagar eller mindre. Se [Nyckelhantering](../../sftp/using/key-management.md).

* **SSL-certifikatets förfallodatum**: En av dina underdomäners SSL-certifikat har gått ut eller går ut om 30 dagar eller mindre. Se [Övervaka underdomäners SSL-certifikat](../../subdomains-certificates/using/monitoring-ssl-certificates.md).

<!--* **Long running Queries**: A query has been running for more than 24 hours on one of your instances. See [Monitoring active queries](database-active-queries.md).-->

>[!NOTE]
>
>På Kontrollpanelen kan du dessutom **ange påminnelser** för att kunna meddelas via e-post innan en händelse inträffar i dina instanser (releaser och servicegranskningar).
>
>Om du vill göra det måste du prenumerera på e-postaviseringar och ställa in en påminnelse för de kommande händelserna. [Lär dig hur du ställer in påminnelser för kommande evenemang](../../service-events/service-events.md#reminders)

## Prenumerera på aviseringar {#subscribe}

Så här prenumererar du på dessa aviseringar:

1. Klicka på **[!UICONTROL Alerting notifications]** som är tillgängliga från valfri plats på Kontrollpanelen och sedan klickar du på **[!UICONTROL Subscribe]**.

   ![](assets/subscribing.png)

1. Ett e-postmeddelande skickas för att bekräfta din prenumeration.

   ![](assets/email_subscription.png)

1. Efter prenumerationen kommer Kontrollpanelen att meddela om systemproblem och rekommendera vilka åtgärder som ska vidtas. E-postaviseringar skickas till alla som har anmält sig för **alla instanser** som de är administratörer för.

   ![](assets/alert_sample.png)
