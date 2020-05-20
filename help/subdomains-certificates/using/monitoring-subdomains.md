---
title: Övervaka underdomäners SSL-certifikat
description: Lär dig övervaka dina underdomäners SSL-certifikat
translation-type: tm+mt
source-git-commit: a2c19296894ff893987290cb287dc7002ab999e5
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 0%

---


# Övervaka dina underdomäner {#monitoring-subdomains}

Det är viktigt att ni övervakar era underdomäner för att se till att alla är korrekt konfigurerade för att fungera med Adobe Campaign.

Listan med underdomäner för var och en av dina produktionsinstanser är tillgänglig direkt när du väljer **[!UICONTROL Subdomains & Certificates]** kortet.

Kolumnen anger **[!UICONTROL Last verification]** när en underdomän verifierades för senaste gången. Du kan starta en verifiering när som helst genom att klicka på **..** / **[!UICONTROL Verify subdomain]** .

![](assets/subdomain_verification.png)

>[!IMPORTANT]
>
>Adobe rekommenderar inte att du använder underdomäner utan certifikatdatum eftersom det kan innebära att dessa underdomäner kan ha leveransproblem.

När du startar en verifiering utförs flera åtgärder för att kontrollera att underdomänen är korrekt konfigurerad (instansklientkontroll, e-postsändningstest osv.)

Om underdomänens verifiering misslyckas kontaktar du Adobes kundtjänst för mer information.

**Relaterade ämnen:**

* [Lägga till SSL-certifikat (självstudievideo)](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/adding-ssl-certificates.html)
* [Förnya en underdomäns SSL-certifikat](../../subdomains-certificates/using/renewing-subdomain-certificate.md)
* [Märke för underdomäner](../../subdomains-certificates/using/subdomains-branding.md)
