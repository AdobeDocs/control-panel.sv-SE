---
product: campaign
solution: Campaign
title: Övervaka underdomäner
description: Övervaka dina underdomäner för att säkerställa att alla är korrekt konfigurerade för att fungera med Adobe Campaign.
feature: Control Panel
role: Architect
level: Experienced
exl-id: edd55d07-bf0b-44b0-8281-be69c698d5e8
source-git-commit: acf0334e894649d6b5edf0b96877c3f643894763
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 10%

---


# Övervaka underdomänerna {#monitoring-subdomains}

Det är viktigt att du övervakar dina underdomäner för att se till att alla är konfigurerade på rätt sätt för att fungera med Adobe Campaign.

Listan med underdomäner för var och en av dina produktionsinstanser är tillgänglig direkt när du väljer **[!UICONTROL Subdomains & Certificates]** kort.

The **[!UICONTROL Last verification]** kolumnen anger när en underdomän verifierades för senaste gången. Du kan starta en verifiering när som helst genom att klicka på **...** / **[!UICONTROL Verify subdomain]** -knappen.

![](assets/subdomain_verification.png)

>[!IMPORTANT]
>
>Adobe rekommenderar inte att du använder underdomäner utan certifikatdatum eftersom det kan innebära att dessa underdomäner kan ha leveransproblem.

När du startar en verifiering utförs flera åtgärder för att kontrollera att underdomänen är korrekt konfigurerad (instansklientkontroll, e-postsändningstest osv.) Om underdomänens verifiering misslyckas kontaktar du Adobe kundtjänst för ytterligare utredning.

**Relaterade ämnen:**

* [Förnya en underdomäns SSL-certifikat](../../subdomains-certificates/using/renewing-subdomain-certificate.md)
* [Märka underdomäner](../../subdomains-certificates/using/subdomains-branding.md)
