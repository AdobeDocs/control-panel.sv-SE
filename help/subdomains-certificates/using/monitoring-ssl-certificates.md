---
product: campaign
solution: Campaign
title: Övervaka underdomäners SSL-certifikat
description: Läs om hur man övervakar underdomäners SSL-certifikat
feature: Control Panel
role: Architect
level: Experienced
exl-id: a7888e1c-259d-4601-951b-0f1062d90dc2
source-git-commit: 40654418f0c5b298cc4fbd66a5d835355876a12c
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Övervaka underdomäners SSL-certifikat {#monitoring-ssl-certificates}

## Om SSL-certifikat {#about-ssl-certificates}

Adobe Campaign rekommenderar att du säkrar de underdomäner som är värdar för dina landningssidor. Särskilt de som samlar in känslig information om kunder.

**SSL-kryptering (Secure Socket Layer)** ser till att de underdomäner som du har konfigurerat för att arbeta med Adobe är säkra. När kunden fyller i ett webbformulär eller besöker en landningssida som Adobe Campaign är värd för skickas informationen som standard via ett osäkert protokoll (HTTP). För att garantera ytterligare säkerhet måste information som skickas skyddas med ett HTTPS-protokoll. Underdomänadressen ”http://info.mywebsite.com/” blir istället ”https://info.mywebsite.com/”.

**SSL-certifikat är inte installerade på de konfigurerade underdomänerna själva**. De installeras på associerade underdomäner och då främst på de som är värdar för landningssidor, resurssidor och andra.

**SSL-certifikat tillhandahålls under en viss tidsperiod** (1 år, 60 dagar osv.). När ett certifikat upphör att gälla kan problem uppstå med att komma åt landningssidorna eller använda resurser från underdomänen. För att förhindra detta kan du via Kontrollpanelen övervaka underdomänernas SSL-certifikat samt starta förnyelseprocessen.

![](assets/no_certificate.png)

## Delegera underdomäners SSL-certifikat till Adobe

Vi rekommenderar att du delegerar dina underdomäners SSL-certifikat till Adobe eftersom Adobe automatiskt skapar certifikatet och förnyar det varje år innan certifikatet upphör att gälla. [Lär dig hur du delegerar underdomäners SSL-certifikat till Adobe](delegate-ssl.md)

## Övervaka SSL-certifikat  {#monitoring-certificates}

>[!CONTEXTUALHELP]
>id="cp_subdomain_details"
>title="Information om underdomäner"
>abstract="Hämta information om dina underdomäners SSL-certifikat."

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

**Relaterade ämnen:**

* [Förnya en underdomäns SSL-certifikat](../../subdomains-certificates/using/renewing-subdomain-certificate.md)
* [Märka underdomäner](../../subdomains-certificates/using/subdomains-branding.md)
