---
title: Märka underdomäner
description: Läs mer om att märka underdomäner
translation-type: ht
source-git-commit: 80b35e82116b064a7b141d957ab79ecfc9a99026
workflow-type: ht
source-wordcount: '467'
ht-degree: 100%

---


# Märka underdomäner {#subdomains-branding}

>[!CONTEXTUALHELP]
>id="cp_certificate_management"
>title="Om underdomäner och SSL-certifikat"
>abstract="Övervaka dina underdomäner och associerade SSL-certifikat."
>additional-url="https://docs.adobe.com/content/help/sv-SE/control-panel/using/subdomains-and-certificates/monitoring-ssl-certificates.html" text="Så övervakar du dina underdomäners SSL-certifikat"

>[!IMPORTANT]
>
>Att delegera underdomäner i Kontrollpanelen finns tillgängligt som en betaversion och kan ofta uppdateras och ändras utan föregående meddelande.

## Varför konfigurera underdomäner? {#why-setting-up-subdomains}

En underdomän är en division av domänen som kan användas för att isolera varumärken eller olika typer av trafik (transaktionsmeddelanden, marknadsföringsinformation osv.).

Låt oss ta exemplet med domänen ”mybrand.com” som används för att skicka både transaktions- och marknadsföringskommunikation. I det här fallet kan du konfigurera två underdomäner:

* underdomänen ”info.mybrand.com” för transaktionskommunikation (inköpsbekräftelser och lösenordsåterställning osv.) och
* underdomänen ”marketing.mybrand.com” för dina e-postmeddelanden till möjliga kunder.

På så sätt kan du bevara domänens och andra underdomäners rykte. Om t.ex. underdomänen ”marketing.mybrand.com” läggs till i blockeringslistan hos internetleverantörer på grund av dålig levererbarhet förhindrar detta att hela domänen ”mybrand.com” och underdomänen ”info.mybrand.com” läggs till i blockeringslistan.

## Delegeringsmetoder för underdomäner {#subdomain-delegation-methods}

Delegering via underdomän låter dig delegera en undersektion av domänen (tekniskt sett en ”DNS-zon”) som ska användas med Adobe Campaign. Tillgängliga installationsmetoder är:

* **Fullständig delegering av underdomäner till Adobe Campaign** (rekommenderas): underdomänen delegeras helt till Adobe. Adobe kan leverera Campaign som en hanterad tjänst genom att kontrollera och underhålla alla aspekter av DNS som krävs för att leverera, återge och spåra e-postkampanjer.

* **Att använda CNAME:er** (rekommenderas inte och stöds inte via Kontrollpanelen): skapa en underdomän och använd CNAME:er för att peka till specifika Adobe-poster. Med den här konfigurationen delar både Adobe och kunden ansvaret för att underhålla DNS:er.

Tabellen nedan tillhandahåller en sammanfattning av hur dessa metoder fungerar samt den troliga ansträngningsnivån:

| Delegeringsmetod | Så fungerar det | Ansträngningsnivå |
|---|---|---|
| **Fullständig delegering** | Skapa underdomänen och posten för namnrymden. Adobe konfigurerar sedan alla DNS-poster som krävs för Adobe Campaign.<br/><br/>I den här konfigurationen är Adobe helt ansvarigt för att hantera underdomänen och alla DNS-poster. | Låg |
| **CNAME och anpassad metod** | Skapa underdomänen och posten för namnrymden. Adobe tillhandahåller sedan de poster som ska placeras i DNS-servrarna och konfigurerar motsvarande värden i Adobe Campaign DNS-servrar.<br/><br/>I den här konfigurationen delar både du och Adobe ansvaret för att underhålla DNS:er. | Hög |

Ytterligare information om domändelegering finns i [den här dokumentationen](https://helpx.adobe.com/se/campaign/kb/domain-name-delegation.html).

Kontakta Adobes levererbarhetsteam om du har några frågor gällande delegeringsmetoder för underdomäner. I annat fall kan du kontakta Kundtjänst för att få rådgivning om levererbarhet.

**Relaterade ämnen:**

* [Konfigurera en ny underdomän ](../../subdomains-certificates/using/setting-up-new-subdomain.md)
* [Delegera underdomäner (video med självstudiekurser)](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/subdomain-delegation.html)
* [Övervaka underdomänerna](../../subdomains-certificates/using/monitoring-subdomains.md)
