---
product: campaign
solution: Campaign
title: Övervaka underdomäners SSL-certifikat
description: Läs om hur man övervakar underdomäners SSL-certifikat
translation-type: tm+mt
source-git-commit: 168ae32d7931497bb37d63f7dd1d14eadbb4b1bf
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 24%

---


# Övervaka underdomänerna {#monitoring-subdomains}

Det är viktigt att du övervakar dina underdomäner för att se till att alla är konfigurerade på rätt sätt för att fungera med Adobe Campaign.

Listan med underdomäner för var och en av dina produktionsinstanser är tillgänglig direkt när du väljer **[!UICONTROL Subdomains & Certificates]** kortet.

Kolumnen anger **[!UICONTROL Last verification]** när en underdomän verifierades för senaste gången. Du kan starta en verifiering när som helst genom att klicka på **..** / **[!UICONTROL Verify subdomain]** .

![](assets/subdomain_verification.png)

>[!IMPORTANT]
>
>Adobe rekommenderar inte att du använder underdomäner utan certifikatdatum eftersom det kan innebära att dessa underdomäner kan ha leveransproblem.

När du startar en verifiering utförs flera åtgärder för att kontrollera att underdomänen är korrekt konfigurerad (instansklientkontroll, e-postsändningstest osv.)

Om underdomänens verifiering misslyckas kontaktar du Adobe kundtjänst för ytterligare utredning.

**Relaterade ämnen:**

* [Lägga till SSL-certifikat (video med självstudiekurser)](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/adding-ssl-certificates.html)
* [Förnya en underdomäns SSL-certifikat](../../subdomains-certificates/using/renewing-subdomain-certificate.md)
* [Märka underdomäner](../../subdomains-certificates/using/subdomains-branding.md)
