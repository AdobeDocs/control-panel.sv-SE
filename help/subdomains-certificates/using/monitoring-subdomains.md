---
product: campaign
solution: Campaign
title: Övervaka underdomäners SSL-certifikat
description: Läs om hur man övervakar underdomäners SSL-certifikat
translation-type: tm+mt
source-git-commit: 317b4c1cee34667a36f5e1a1197649bfd69c151a
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Övervaka underdomänerna {#monitoring-subdomains}

Det är viktigt att du övervakar dina underdomäner för att se till att alla är konfigurerade på rätt sätt för att fungera med Adobe Campaign.

Listan med underdomäner för var och en av dina produktionsinstanser är tillgänglig direkt när du väljer **[!UICONTROL Subdomains & Certificates]**-kortet.

Kolumnen **[!UICONTROL Last verification]** anger när en underdomän verifierades för senaste gången. Du kan starta en verifiering när som helst genom att klicka på **..** / **[!UICONTROL Verify subdomain]** knapp.

![](assets/subdomain_verification.png)

>[!IMPORTANT]
>
>Adobe rekommenderar inte att du använder underdomäner utan certifikatdatum eftersom det kan innebära att dessa underdomäner kan ha leveransproblem.

När du startar en verifiering utförs flera åtgärder för att kontrollera att underdomänen är korrekt konfigurerad (instansklientkontroll, e-postsändningstest osv.)

Om underdomänens verifiering misslyckas kontaktar du Adobe kundtjänst för ytterligare utredning.

**Relaterade ämnen:**

* [Förnya en underdomäns SSL-certifikat](../../subdomains-certificates/using/renewing-subdomain-certificate.md)
* [Märka underdomäner](../../subdomains-certificates/using/subdomains-branding.md)
