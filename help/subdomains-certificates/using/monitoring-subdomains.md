---
product: campaign
solution: Campaign
title: Övervaka underdomäners SSL-certifikat
description: Läs om hur man övervakar underdomäners SSL-certifikat
feature: Control Panel
role: Architect
level: Experienced
exl-id: edd55d07-bf0b-44b0-8281-be69c698d5e8
source-git-commit: 8dce5b9d1eb59b7ebc8ef1f73f7552dcf61077a1
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 21%

---

# Övervaka underdomäner {#monitoring-subdomains}

>[!AVAILABILITY]
>
>Den här funktionen finns inte i Campaign v8.

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
