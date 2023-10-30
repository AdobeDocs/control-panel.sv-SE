---
product: campaign
solution: Campaign
title: Övervaka underdomäners SSL-certifikat
description: Läs om hur man övervakar underdomäners SSL-certifikat
feature: Control Panel, Subdomains and Certificates
role: Admin
level: Experienced
exl-id: a7888e1c-259d-4601-951b-0f1062d90dc2
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '567'
ht-degree: 64%

---

# Övervaka underdomäners SSL-certifikat {#monitoring-ssl-certificates}

## Om SSL-certifikat {#about-ssl-certificates}

Adobe Campaign rekommenderar att du säkrar de underdomäner som är värdar för dina landningssidor. Särskilt de som samlar in känslig information om kunder.

**SSL-kryptering (Secure Socket Layer)** ser till att de underdomäner som du har konfigurerat för att arbeta med Adobe är säkra. När kunden fyller i ett webbformulär eller besöker en landningssida som Adobe Campaign är värd för skickas informationen som standard via ett osäkert protokoll (HTTP). För att garantera ytterligare säkerhet måste information som skickas skyddas med ett HTTPS-protokoll. Underdomänadressen ”http://info.mywebsite.com/” blir istället ”https://info.mywebsite.com/”.

**SSL-certifikat har inte installerats på de konfigurerade underdomänerna själva**. De installeras på associerade underdomäner och då främst på de som är värdar för landningssidor, resurssidor och andra.

**SSL-certifikat tillhandahålls under en viss tidsperiod** (1 år, 60 dagar osv.). När ett certifikat upphör att gälla kan problem uppstå med att komma åt landningssidorna eller använda resurser från underdomänen. För att förhindra detta kan du via Kontrollpanelen övervaka underdomänernas SSL-certifikat samt starta förnyelseprocessen.

![](assets/no_certificate.png)

## Hantering av SSL-certifikat {#management}

Övervakning av SSL-certifikat är avgörande för att säkerställa att dina underdomäner är säkra. Med Kontrollpanelen kan du installera och förnya dina underdomäners SSL-certifikat direkt av dig själv eller delegera dem till Adobe så att den här processen utförs automatiskt utan att du behöver göra något.

Vi rekommenderar att du delegerar hanteringen av dina underdomäners SSL-certifikat till Adobe, eftersom Adobe automatiskt skapar certifikatet och förnyar det varje år innan det upphör att gälla. Detta minskar risken för fel som kan uppstå när certifikat hanteras manuellt. [Lär dig hur du delegerar underdomäners SSL-certifikat till Adobe](delegate-ssl.md)

Nedan finns en omfattande lista över de konsekvenser som är förknippade med manuell certifikathantering i motsats till att delegera denna åtgärd till Adobe:

|       | Kundhanterat certifikat | Certifikat som hanteras av Adobe |
|  ---  |  ---  |  ---  |
| Certifikatleverantör | Certifikatutfärdare från tredje part | Adobe via AWS certifikatshanterare |
| Manuella steg | CSR-generering, inköp och installation av certifikat | Ingen |
| Förnyelseprocess | Kundens ansvar | Hanteras automatiskt av Adobe |
| Underdomänsäkerhet | Domänen kan ha oskyddade underdomäner (spårning, spegling och uppspelning) såvida du inte installerar/förnyar certifikat. | Alla nya domäner (om de väljs för Adobe-hanterad) kommer att ha alla underdomäner skyddade som standard. |
| Certifikatkostnad | Kunden ansvarar för kostnaden för certifikat | Kostnadsfritt |

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
