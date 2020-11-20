---
product: campaign
solution: Campaign
title: Övervaka underdomäners SSL-certifikat
description: Läs om hur man övervakar underdomäners SSL-certifikat
translation-type: tm+mt
source-git-commit: 168ae32d7931497bb37d63f7dd1d14eadbb4b1bf
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 93%

---


# Övervaka underdomäners SSL-certifikat {#monitoring-ssl-certificates}

## Om SSL-certifikat {#about-ssl-certificates}

Adobe Campaign rekommenderar att du säkrar de underdomäner som är värdar för dina landningssidor. Särskilt de som samlar in känslig information om kunder.

**SSL-kryptering** (Secure Socket Layer) garanterar att de underdomäner som du har konfigurerat för att arbeta med Adobe är säkra. När kunden fyller i ett webbformulär eller besöker en landningssida som Adobe Campaign är värd för skickas informationen som standard via ett osäkert protokoll (HTTP). För att garantera ytterligare säkerhet måste information som skickas skyddas med ett HTTPS-protokoll. Underdomänadressen ”http://info.mywebsite.com/” blir istället ”https://info.mywebsite.com/”.

**SSL-certifikat är inte installerade på de konfigurerade underdomänerna själva**. De installeras på associerade underdomäner och då främst på de som är värdar för landningssidor, resurssidor och andra.

**SSL-certifikat tillhandahålls under en viss tidsperiod** (1 år, 60 dagar osv.). När ett certifikat upphör att gälla kan problem uppstå med att komma åt landningssidorna eller använda resurser från underdomänen. För att förhindra detta kan du via Kontrollpanelen övervaka underdomänernas SSL-certifikat samt starta förnyelseprocessen.

![](assets/no_certificate.png)

## Övervaka SSL-certifikat {#monitoring-certificates}

>[!CONTEXTUALHELP]
>id="cp_subdomain_details"
>title="Information om underdomäner"
>abstract="Hämta information om underdomänerna."

Statusen för underdomänernas SSL-certifikat finns tillgänglig direkt från listan över underdomäner när du väljer **[!UICONTROL Subdomains & Certificates]**-kortet.

Underdomäner ordnas per det närmaste förfallodatumet för SSL-certifikatet med visuell information om förfallodatumet i antal dagar:

* **Grön**: underdomänen har inte något certifikat som upphör att gälla inom de närmaste 60 dagarna.
* **Orange**: en eller flera underdomäner har ett certifikat som upphör att gälla inom 60 dagar.
* **Orange**: en eller flera underdomäner har ett certifikat som upphör att gälla inom 30 dagar.
* **Grå**: inget certifikat har installerats för underdomänen.

![](assets/subdomains_list.png)

Klicka på knappen **[!UICONTROL Subdomain Details]** om du vill ha mer information om en underdomän.
Listan över alla relaterade underdomäner visas. Den omfattar vanligtvis underdomäner till bland annat landningssidor och resurssidor.

Fliken innehåller information om de konfigurerade inkorgarna (avsändare, svara till och felaktiga e-postmeddelanden). **[!UICONTROL Sender info]**

![](assets/subdomain_details.png)

Om en av underdomänernas SSL-certifikat är på väg att löpa ut kan du förnya det direkt i Kontrollpanelen. Se avsnittet [Förnya en underdomäns SSL-certifikat](../../subdomains-certificates/using/renewing-subdomain-certificate.md) för mer information om detta.

>[!IMPORTANT]
>
>Certifikatförnyelse i Kontrollpanelen finns tillgängligt som en betaversion och kan ofta uppdateras och ändras utan föregående meddelande.

**Relaterade ämnen:**

* [Lägga till SSL-certifikat (video med självstudiekurser)](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/adding-ssl-certificates.html)
* [Förnya en underdomäns SSL-certifikat](../../subdomains-certificates/using/renewing-subdomain-certificate.md)
* [Märka underdomäner](../../subdomains-certificates/using/subdomains-branding.md)
