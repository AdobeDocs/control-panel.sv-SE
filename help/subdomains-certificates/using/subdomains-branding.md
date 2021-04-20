---
product: campaign
solution: Campaign
title: Märka underdomäner
description: Läs mer om att märka underdomäner
feature: Control Panel
role: Architect
level: Intermediate
translation-type: tm+mt
source-git-commit: 4b8020dfd5d1f81a81d0e20025cfabe734744d34
workflow-type: tm+mt
source-wordcount: '698'
ht-degree: 79%

---


# Märka underdomäner {#subdomains-branding}

>[!CONTEXTUALHELP]
>id="cp_certificate_management"
>title="Om underdomäner och SSL-certifikat"
>abstract="Övervaka dina underdomäner och associerade SSL-certifikat."
>additional-url="https://docs.adobe.com/content/help/sv-SE/control-panel/using/subdomains-and-certificates/monitoring-ssl-certificates.html" text="Så övervakar du dina underdomäners SSL-certifikat"

## Varför konfigurera underdomäner? {#why-setting-up-subdomains}

>[!IMPORTANT]
>
>Underdomänskonfigurationen från Kontrollpanelen är tillgänglig som betaversion och kan uppdateras ofta och ändras utan föregående meddelande.

En underdomän är en division av domänen som kan användas för att isolera varumärken eller olika typer av trafik (transaktionsmeddelanden, marknadsföringsinformation osv.).

Låt oss ta exemplet med domänen ”mybrand.com” som används för att skicka både transaktions- och marknadsföringskommunikation. I det här fallet kan du konfigurera två underdomäner:

* underdomänen ”info.mybrand.com” för transaktionskommunikation (inköpsbekräftelser och lösenordsåterställning osv.) och
* underdomänen ”marketing.mybrand.com” för dina e-postmeddelanden till möjliga kunder.

På så sätt kan du bevara domänens och andra underdomäners rykte. Om t.ex. underdomänen ”marketing.mybrand.com” läggs till i blockeringslistan hos internetleverantörer på grund av dålig levererbarhet förhindrar detta att hela domänen ”mybrand.com” och underdomänen ”info.mybrand.com” läggs till i blockeringslistan.

## Konfigurationsmetoder för underdomäner {#subdomain-delegation-methods}

Med subdomänkonfigurationen kan du konfigurera en undersektion till din domän (tekniskt en &quot;DNS-zon&quot;) för användning med Adobe Campaign. Tillgängliga installationsmetoder är:

* **Fullständig delegering av underdomäner till Adobe Campaign** (rekommenderas): underdomänen delegeras helt till Adobe. Adobe kan leverera Campaign som en hanterad tjänst genom att kontrollera och underhålla alla aspekter av DNS som krävs för att leverera, återge och spåra e-postkampanjer.

* **Användning av CNAME**: Skapa en underdomän och använd CNAME:er för att peka på Adobe-specifika poster. Med den här konfigurationen delar både Adobe och kunden ansvaret för att underhålla DNS:er.

Tabellen nedan tillhandahåller en sammanfattning av hur dessa metoder fungerar samt den troliga ansträngningsnivån:

| Konfigurationsmetod | Så fungerar det | Ansträngningsnivå |
|---|---|---|
| **Fullständig delegering** | Skapa underdomänen och posten för namnrymden. Adobe konfigurerar sedan alla DNS-poster som krävs för Adobe Campaign.<br/><br/>I den här konfigurationen är Adobe helt ansvarigt för att hantera underdomänen och alla DNS-poster. | Låg |
| **CNAME och anpassad metod** | Skapa underdomänen och posten för namnrymden. Adobe tillhandahåller sedan de poster som ska placeras i DNS-servrarna och konfigurerar motsvarande värden i Adobe Campaign DNS-servrar.<br/><br/>I den här konfigurationen delar både du och Adobe ansvaret för att underhålla DNS:er. | Hög |

Ytterligare information om domänkonfiguration finns i [den här dokumentationen](https://helpx.adobe.com/se/campaign/kb/domain-name-delegation.html).

Om du har några frågor om konfigureringsmetoder för subdomäner kan du kontakta Adobe Deliverability Team eller så småningom kontakta Kundtjänst för att få rådgivning om slutprodukten.

## Användningsexempel för underdomäner (Campaign Classic){#subdomains-use-cases}

När du konfigurerar underdomäner för Campaign Classic-instanser måste du välja det användningsfall som underdomänen ska användas för (se [Konfigurera en ny underdomän](../../subdomains-certificates/using/setting-up-new-subdomain.md)).

Möjliga användningsområden är:

* **Marknadsföringskommunikation**: kommunikation som är avsedd för kommersiellt bruk. Exempel: försäljningskampanj via e-post.

* **Transaktions- och verksamhetskommunikation**: transaktionskommunikation innehåller information som syftar till att slutföra en process som mottagaren har startat med dig. Exempel: inköpsbekräftelse och e-post för lösenordsåterställning. Organisationskommunikation rör utbyte av information, idéer och åsikter utan kommersiellt syfte. Detta gäller både inom och utanför organisationen .

**Att dela upp underdomänerna per användningsfall är bästa praxis för levererbarhet**. På så sätt isoleras och skyddas varje underdomäns rykte. Om till exempel din underdomän för marknadsföringskommunikation läggs till i blockeringslistan hos internetleverantörer påverkas inte den för transaktionskommunikation och kan fortsätta att skicka kommunikation.

**Du kan konfigurera en underdomän för både Marketing och Transactional use-fall**:

* I användningsfall för Marknadsföring konfigureras underdomäner på **MID**-instanser (mid-sourcing).
* I användningsfall för Transaktioner konfigureras underdomäner på ALLA **RT**-instanser (meddelandecenter/realtidsmeddelanden) för att säkerställa anslutningen. Underdomänerna fungerar därför med alla RT-instanser.

>[!NOTE]
>
>Om du använder Campaign Classic kan du via Kontrollpanelen se vilka RT/MID-instanser som är anslutna till den marknadsföringsinstans du arbetar med. Se avsnittet [Information om instanser](../../instances-settings/using/instance-details.md) för mer information.

**Relaterade ämnen:**

* [Konfigurera en ny underdomän ](../../subdomains-certificates/using/setting-up-new-subdomain.md)
* [Övervaka underdomänerna](../../subdomains-certificates/using/monitoring-subdomains.md)
