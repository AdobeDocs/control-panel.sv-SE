---
product: campaign
solution: Campaign
title: Förnya en underdomäns SSL-certifikat
description: Läs om hur man förnyar underdomäners SSL-certifikat
feature: Control Panel
role: Architect
level: Experienced
exl-id: e9b7c67d-6afa-44f9-b19d-39c0ec9a7edd
source-git-commit: 5a5ac1a604fe5bdce07479ff84184abdb2e0ddba
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 28%

---

# Förnya ett SSL-certifikat {#renewing-subdomains-ssl-certificates}

>[!CONTEXTUALHELP]
>id="cp_add_ssl_certificate"
>title="Förnyelse av SSL-certifikat"
>abstract="Om du vill förnya ett SSL-certifikat måste du generera en CSR, köpa SSL-certifikatet för dina underdomäner och installera certifikatpaketet."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html#generating-csr" text="Generera en begäran om certifikatsignering"
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html#installing-ssl-certificate" text="Installera ett SSL-certifikat"

>[!IMPORTANT]
>
>SSL-certifikatförnyelse från Kontrollpanelen är tillgänglig som betaversion och kan uppdateras ofta och ändras utan föregående meddelande.
>
>Om du använder en instans med en hybridvärdmodell kan du bara visa certifikat som är kopplade till de delegerade underdomänerna och kan inte förnya dem.

Processen gällande förnyelse av SSL-certifikat omfattar tre steg:

1. **Generering av CSR (Certificate Signing Request)**

   Begäran om certifikatsignering måste genereras för den instans och de underdomäner som du planerar att skydda innan du köper ett certifikat.  Du måste ange viss information som krävs för att generera en Begäran om certifikatsignering (såsom ett nätverksnamn, organisationsnamn och adress etc.). [Läs mer](generate-csr.md)

1. **Köp av SSL-certifikatet**

   När CSR:n har skapats kan du använda den för att köpa SSL-certifikatet från den certifikatutfärdare som ditt företag godkänner.

1. **Installation av SSL-certifikatet**

   Installera det köpta SSL-certifikatet på den önskade underdomänen för att skydda dem. [Läs mer](install-ssl-certificate.md)

![](assets/do-not-localize/how-to-video.png) Upptäck den här funktionen i video med [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/subdomains-and-certificates/adding-ssl-certificates.html#subdomains-and-certificates) eller [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/subdomains-and-certificates/adding-ssl-certificates.html#adding-ssl-certificates)

**Relaterade ämnen:**

* [Guide för bästa praxis vid leverans - SSL-certifikatbegäran för Adobe Campaign](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/campaign/ac-ssl-certificate-request.html)
* [Märka underdomäner](../../subdomains-certificates/using/subdomains-branding.md)
* [Övervaka underdomäner](../../subdomains-certificates/using/monitoring-subdomains.md)
