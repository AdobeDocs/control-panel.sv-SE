---
product: campaign
solution: Campaign
title: Övervaka underdomäner
description: Övervaka dina underdomäner för att säkerställa att alla är korrekt konfigurerade för att fungera med Adobe Campaign.
feature: Control Panel
role: Architect
level: Experienced
exl-id: edd55d07-bf0b-44b0-8281-be69c698d5e8
source-git-commit: f0c3df4727e89e3f6127fe4563908b955ccb820c
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 7%

---

# Övervaka underdomäner {#monitoring-subdomains}

>[!CONTEXTUALHELP]
>id="cp_subdomain_undelegate"
>title="Ta bort underdomänsdelegering"
>abstract="På den här skärmen kan du ta bort delegeringen av en underdomän till Adobe. Tänk på att den här processen inte kan ångras eller stoppas när den har skickats.<br><br>Om du försöker ta bort delegeringen av en primär domän för den valda instansen blir du ombedd att välja den domän som ska ersätta den."

Det är viktigt att du övervakar dina underdomäner för att se till att alla är konfigurerade på rätt sätt för att fungera med Adobe Campaign.

Listan med underdomäner för var och en av dina produktionsinstanser är tillgänglig direkt när du väljer **[!UICONTROL Subdomains & Certificates]** kort.

The **[!UICONTROL Last verification]** kolumnen anger när en underdomän verifierades för senaste gången. Du kan starta en verifiering när som helst genom att klicka på **...** / **[!UICONTROL Verify subdomain]** -knappen.

![](assets/subdomain_verification.png)

>[!IMPORTANT]
>
>Adobe rekommenderar inte att du använder underdomäner utan certifikatdatum eftersom det kan innebära att dessa underdomäner kan ha leveransproblem.

När du startar en verifiering utförs flera åtgärder för att kontrollera att underdomänen är korrekt konfigurerad (instansklientkontroll, e-postsändningstest osv.)

Om underdomänens verifiering misslyckas kontaktar du Adobe kundtjänst för ytterligare utredning.

**Relaterade ämnen:**

* [Förnya en underdomäns SSL-certifikat](../../subdomains-certificates/using/renewing-subdomain-certificate.md)
* [Märka underdomäner](../../subdomains-certificates/using/subdomains-branding.md)
