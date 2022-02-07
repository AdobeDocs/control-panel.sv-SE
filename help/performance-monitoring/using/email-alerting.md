---
product: campaign
solution: Campaign
title: E-postavisering
description: Lär dig hur du tar emot e-postmeddelanden i händelse av problem med dina Campaign-instanser
feature: Control Panel
role: Architect
level: Experienced
exl-id: 7942d2b1-d28f-4760-aa25-5ba94a627fd0
source-git-commit: ec83878e93536c979c39da52ed07b465f4fbbcb1
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 1%

---

# E-postavisering {#email-alerting}

Kontrollpanelen är utrustad med e-postaviseringsfunktioner i realtid för att ge större flexibilitet i arbetet.

Så här prenumererar du på dessa aviseringar:

1. Klicka på **[!UICONTROL Alerting notifications]** som är tillgängliga från valfri plats på Kontrollpanelen och sedan klickar du på **[!UICONTROL Subscribe]**.

   ![](assets/subscribing.png)

1. Ett e-postmeddelande skickas för att bekräfta din prenumeration.

   ![](assets/email_subscription.png)

1. Efter prenumerationen kommer Kontrollpanelen att meddela om systemproblem och rekommendera vilka åtgärder som ska vidtas. E-postaviseringar skickas till alla som har anmält sig för **alla instanser** som de är administratörer för.

   ![](assets/alert_sample.png)

Listan med varningar är följande:

* **SFTP-lagringsanvändning**: En av dina SFTP-servrar har nått 80 % eller mer av sin kapacitet. Se [SFTP-lagringshantering](../../sftp/using/sftp-storage-management.md).

* **Databasanvändning**: En av instansdatabaserna har nått 80 % eller mer av sin kapacitet. Se [Databasövervakning](../../performance-monitoring/using/database-monitoring.md).

* **SSL-certifikatets förfallodatum**: En av dina underdomäners SSL-certifikat har gått ut eller går ut om 60 dagar eller mindre. Se [Övervaka underdomäners SSL-certifikat](../../subdomains-certificates/using/monitoring-ssl-certificates.md).

* **SFTP IP-listan tillåter att listan går ut**: Ett av IP-intervallen som du har definierat har gått ut eller går ut om 10 dagar eller mindre. Se [IP-intervall tillåter listning](../../sftp/using/ip-range-allow-listing.md).

* **SFTP-utgångsdatum för offentlig nyckel**: En av de offentliga nycklarna som du har definierat har gått ut eller går ut om 10 dagar eller mindre. Se [Nyckelhantering](../../sftp/using/key-management.md).

* **Långa frågor**: En fråga har körts i över 24 timmar på en av dina förekomster. Se [Övervaka aktiva frågor](database-active-queries.md).