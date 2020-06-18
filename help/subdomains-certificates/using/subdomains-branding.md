---
title: Märke för underdomäner
description: Läs mer om varumärken för underdomäner
translation-type: tm+mt
source-git-commit: 198c974d269289a6a9e5a87314662dba0bc85aff
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 0%

---


# Märke för underdomäner {#subdomains-branding}

>[!CONTEXTUALHELP]
>id="cp_certificate_management"
>title="Om underdomäner och SSL-certifikat"
>abstract="Övervaka dina underdomäner och associerade SSL-certifikat."
>additional-url="https://docs.adobe.com/content/help/en/control-panel/using/subdomains-and-certificates/monitoring-ssl-certificates.html" text="Övervaka dina underdomäners SSL-certifikat"

>[!IMPORTANT]
>
>Delegering av underdomäner från Kontrollpanelen är tillgänglig som betaversion och kan uppdateras ofta och ändras utan föregående meddelande.

## Varför konfigurera underdomäner? {#why-setting-up-subdomains}

En underdomän är en division av din domän som kan användas för att isolera dina varumärken eller olika typer av trafik (transaktionsmeddelanden, marknadsföringsinformation osv.).

Låt oss ta exemplet med domänen &quot;mybrand.com&quot;, som används för att skicka både transaktions- och marknadsföringskommunikation. I det här fallet kan du bestämma dig för att konfigurera två underdomäner:

* underdomänen &quot;info.mybrand.com&quot; för din transaktionskommunikation (inköpsbekräftelse, lösenordsåterställning osv.),
* Underdomänen&quot;marketing.mybrand.com&quot; för dina prospekterande e-postmeddelanden.

Genom att göra det kan du bevara domänens och andra underdomäners anseende. Om t.ex. underdomänerna&quot;marketing.mybrand.com&quot; läggs till i blocklistan av Internetleverantörerna på grund av felaktig leverans, förhindrar detta att hela domänen&quot;mybrand.com&quot; och underdomänen&quot;info.mybrand.com&quot; läggs till i blocklistan.

## Delegeringsmetoder för underdomäner {#subdomain-delegation-methods}

Med delegering via underdomän kan du delegera en undersektion till din domän (tekniskt en &quot;DNS-zon&quot;) som ska användas med Adobe Campaign. Tillgängliga installationsmetoder:

* **Fullständig delegering av underdomäner till Adobe Campaign** (rekommenderas): Underdomänen har delegerats till Adobe. Adobe kan leverera Campaign som en hanterad tjänst genom att kontrollera och underhålla alla aspekter av DNS som krävs för att leverera, återge och spåra e-postkampanjer.

* **Användning av CNAME** (rekommenderas inte och stöds inte via Kontrollpanelen): Skapa en underdomän och använd CNAME för att peka på Adobe-specifika poster. Med den här konfigurationen delar både Adobe och kunden ansvaret för att underhålla DNS.

Tabellen nedan innehåller en sammanfattning av hur dessa metoder fungerar samt den underförstådda ansträngningsnivån:

| Delegeringsmetod | Så här fungerar det | Ansträngningsnivå |
|---|---|---|
| **Fullständig delegering** | Skapa post för underdomän och namnområde. Adobe konfigurerar sedan alla DNS-poster som krävs för Adobe Campaign.<br/><br/>I den här konfigurationen är Adobe helt ansvarigt för att hantera underdomänen och alla DNS-poster. | Låg |
| **CNAME, anpassad metod** | Skapa post för underdomän och namnområde. Adobe tillhandahåller sedan de poster som ska placeras i dina DNS-servrar och konfigurerar motsvarande värden i Adobe Campaign DNS-servrar.<br/><br/>I den här konfigurationen delar både du och Adobe ansvaret för att underhålla DNS. | Hög |

Ytterligare information om domändelegering finns i [den här dokumentationen](https://helpx.adobe.com/campaign/kb/domain-name-delegation.html).

Om du har några frågor om delegeringsmetoder för underdomäner kan du kontakta Adobe Deliverability Team eller så småningom kontakta Kundtjänst för att få rådgivning om slutprodukter.

**Relaterade ämnen:**

* [Konfigurera en ny underdomän](../../subdomains-certificates/using/setting-up-new-subdomain.md)
* [Delegera underdomäner (video med självstudiekurser)](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/subdomain-delegation.html)
* [Övervaka dina underdomäner](../../subdomains-certificates/using/monitoring-subdomains.md)
