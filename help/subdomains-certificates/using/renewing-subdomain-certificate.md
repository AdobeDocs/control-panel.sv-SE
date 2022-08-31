---
product: campaign
solution: Campaign
title: Förnya en underdomäns SSL-certifikat
description: Läs om hur man förnyar underdomäners SSL-certifikat
feature: Control Panel
role: Architect
level: Experienced
exl-id: e9b7c67d-6afa-44f9-b19d-39c0ec9a7edd
source-git-commit: 963c2af5cdca80ebc2cd79e0708dc4dfe8c6ec1e
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 100%

---

# Förnya ett SSL-certifikat {#renewing-subdomains-ssl-certificates}

>[!CONTEXTUALHELP]
>id="cp_add_ssl_certificate"
>title="Förnyelse av SSL-certifikat"
>abstract="För att förnya ett SSL-certifikat måste du generera en CSR, köpa SSL-certifikatet för dina underdomäner och installera certifikatpaketet."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html?lang=sv#generating-csr" text="Generera en begäran om certifikatsignering (CSR)"
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html?lang=sv#installing-ssl-certificate" text="Installera ett SSL-certifikat"

Processen gällande förnyelse av SSL-certifikat omfattar tre steg:

1. **Generering av CSR (Certificate Signing Request)**

   Begäran om certifikatsignering måste genereras för den instans och de underdomäner som du planerar att skydda innan du köper ett certifikat.  Du måste ange viss information som krävs för att generera en Begäran om certifikatsignering (såsom ett nätverksnamn, organisationsnamn och adress osv.). [Läs mer](generate-csr.md)

1. **Köp av SSL-certifikatet**

   När CSR har skapats kan du använda den för att köpa SSL-certifikatet från den certifikatutfärdare som ditt företag godkänner.

1. **Installation av SSL-certifikatet**

   Installera det köpta SSL-certifikatet på den önskade underdomänen för att skydda den. [Läs mer](install-ssl-certificate.md)

![](assets/do-not-localize/how-to-video.png) Upptäck denna funktion genom video med [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/subdomains-and-certificates/adding-ssl-certificates.html?lang=sv#subdomains-and-certificates) eller [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/subdomains-and-certificates/adding-ssl-certificates.html?lang=sv#adding-ssl-certificates)

**Relaterade ämnen:**

* [Guide för bästa praxis vid leverans – SSL-certifikatbegäran för Adobe Campaign](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/campaign/ac-ssl-certificate-request.html?lang=sv)
* [Märka underdomäner](../../subdomains-certificates/using/subdomains-branding.md)
* [Övervaka underdomäner](../../subdomains-certificates/using/monitoring-subdomains.md)
