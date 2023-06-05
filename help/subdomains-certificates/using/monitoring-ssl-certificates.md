---
product: campaign
solution: Campaign
title: Övervaka underdomäners SSL-certifikat
description: Läs om hur man övervakar underdomäners SSL-certifikat
feature: Control Panel
role: Architect
level: Experienced
exl-id: a7888e1c-259d-4601-951b-0f1062d90dc2
source-git-commit: 0628e9eb12da4dcc33b2ea21c9ef31bb7ba4f9c4
workflow-type: tm+mt
source-wordcount: '478'
ht-degree: 70%

---

# Övervaka underdomäners SSL-certifikat {#monitoring-ssl-certificates}

## Om SSL-certifikat {#about-ssl-certificates}

Adobe Campaign rekommenderar att du säkrar de underdomäner som är värdar för dina landningssidor. Särskilt de som samlar in känslig information om kunder.

**SSL-kryptering (Secure Socket Layer)** ser till att de underdomäner som du har konfigurerat för att arbeta med Adobe är säkra. När kunden fyller i ett webbformulär eller besöker en landningssida som Adobe Campaign är värd för skickas informationen som standard via ett osäkert protokoll (HTTP). För att garantera ytterligare säkerhet måste information som skickas skyddas med ett HTTPS-protokoll. Underdomänadressen ”http://info.mywebsite.com/” blir istället ”https://info.mywebsite.com/”.

**SSL-certifikat är inte installerade på de konfigurerade underdomänerna själva**. De installeras på associerade underdomäner och då främst på de som är värdar för landningssidor, resurssidor och andra.

**SSL-certifikat tillhandahålls under en viss tidsperiod** (1 år, 60 dagar osv.). När ett certifikat upphör att gälla kan problem uppstå med att komma åt landningssidorna eller använda resurser från underdomänen. För att förhindra detta kan du via Kontrollpanelen övervaka underdomänernas SSL-certifikat samt starta förnyelseprocessen.

![](assets/no_certificate.png)

## Delegera underdomäners SSL-certifikat till Adobe

När du konfigurerar en ny underdomän kan SSL-certifikatet hanteras av Adobe. Vi rekommenderar starkt att du gör det eftersom Adobe automatiskt skapar certifikatet och förnyar det varje år innan certifikatet upphör att gälla.

Om du använder CNAME för att konfigurera en delegering av underdomäner, kommer Adobe att tillhandahålla certifikatposter som kan användas i din värdlösning för domäner för att generera ditt certifikat.

>[!NOTE]
>
>SSL-certifikatdelegering är bara tillgängligt när du konfigurerar en ny underdomän. Den är inte tillgänglig för redan delegerade underdomäner.

SSL-certifikatdelegering aktiveras när en ny underdomän skapas. Lär dig hur du fortsätter i [det här avsnittet](setting-up-new-subdomain.md).

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
