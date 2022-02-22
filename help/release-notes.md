---
product: campaign
solution: Campaign
title: Versioner av Kontrollpanelen
description: Senaste versionsinformation för Kontrollpanelen.
feature: Control Panel
role: Architect
level: Beginner
exl-id: 13aceffb-ceaa-4cfe-8741-95d66c5c6caa
source-git-commit: c52094b8145bdd84aa9e71430a811b8a7b32354d
workflow-type: tm+mt
source-wordcount: '882'
ht-degree: 68%

---

# Versioner av Kontrollpanelen {#control-panel-releases}

Här finns information om de senaste versionerna av Kontrollpanelen.

>[!NOTE]
>
>Kontrollpanelen är bara tillgänglig för administratörsanvändare. Läs mer om behörigheter i [det här avsnittet](https://experienceleague.adobe.com/docs/control-panel/using/discover-control-panel/managing-permissions.html?lang=sv#discover-control-panel).
>
>För Campaign Classic v7 måste din instans lagras på Amazon Web Services (AWS) och uppgraderas till den senaste [Stabilt kampanjbygge](https://experienceleague.adobe.com/docs/campaign-classic/using/release-notes/rn-overview.html?lang=sv#rn-statuses) (eller för att bygga 9032 eller senare). Läs om hur du kontrollerar din version i [det här avsnittet](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/starting-with-adobe-campaign/launching-adobe-campaign.html?lang=sv#getting-your-campaign-version). Följ stegen på [den här sidan](faq.md#hosted-aws) för att kontrollera om instanser har AWS som värd.

## Februari 2022 {#february-2022}

**Övervakning av arbetsflödesparametrar**

Du kan nu övervaka arbetsflödesparametrar som kan kräva särskild uppmärksamhet för att undvika problem i dina instanser. [Läs mer](performance-monitoring/using/workflow-monitoring.md).

## Januari 2022 {#january-2022}

**Övervaka aktiva frågor**

Med Kontrollpanelen kan du nu övervaka frågor som har körts längst på dina instanser. [Läs mer](performance-monitoring/using/database-active-queries.md)

**Genomflöden och fördröjningsövervakning**

Nu kan du övervaka hur leveransgenomflöden och fördröjning trendar över en tidsperiod för dina instanser. [Läs mer](performance-monitoring/using/thoughputs-latencies.md)

**SSL-certifikatåtgärder på nya underdomäner**

SSL-certifikatåtgärder kan nu utföras på en nyligen konfigurerad underdomän, även om en granskning av leveransen fortfarande pågår. [Läs mer](subdomains-certificates/using/renewing-subdomain-certificate.md)

## Oktober 2021 {#october-2021}

**Giltighetsperiod för IP-intervall och offentlig nyckel**

Det går nu att ange en varaktighet för tillgängligheten för IP-intervall och offentliga nycklar. Läs mer i [IP-intervall tillåter listning](sftp/using/ip-range-allow-listing.md#adding-ip-addresses-allow-list) och [Nyckelhantering](sftp/using/key-management.md#installing-ssh-key) -avsnitt.

**IP-intervall och publika nyckelutgåvor**

Nu kan du redigera [IP-intervall](sftp/using/ip-range-allow-listing.md#editing-ip-ranges) och [publika nycklar](sftp/using/key-management.md#editing-public-keys) som du skapar. Observera att den här funktionen inte är tillgänglig för objekt som skapats före den aktuella versionen av Kontrollpanelen.

**Varningar vid SFTP IP-intervall och utgångsdatum för offentlig nyckel**

Funktionen för e-postvarningar innehåller nu varningar om att SFTP IP-adresser tillåter listning av förfallodatum och att SFTP-offentlig nyckel förfaller. [Läs mer](performance-monitoring/using/email-alerting.md)

**Fullt stöd med Campaign v8**

The **Underdomän** och **Certifikat** hanteringsfunktioner stöds nu av Kontrollpanelen i Adobe Campaign v8.

## Augusti 2021 {#august-2021}

**Stöd för Campaign v8**

Kontrollpanelen är nu tillgänglig för Adobe Campaign v8, förutom **Underdomän** och **Certifikat** hanteringsfunktioner som ännu inte stöds. Läs mer i [Kampanjdokumentation v8](https://experienceleague.adobe.com/docs/campaign/campaign-v8/deploy/self-service.html){target=&quot;_blank&quot;}

## Oktober 2020 {#october-2020}

**Konfiguration av underdomäner med CNAME:er**

Med Kontrollpanelen kan du nu konfigurera en underdomän så att den fungerar med Adobe med CNAME:er direkt från gränssnittet. [Läs mer](subdomains-certificates/using/setting-up-new-subdomain.md)

**Förbättringar i databasövervakningen**

Databasövervakningen har förbättrats med ytterligare mätvärden som gör att du kan få detaljerad information om resurser som förbrukar utrymme i databasen. [Läs mer](performance-monitoring/using/database-monitoring.md)

## Juni 2020 {#june-2020}

**Granska en underdomäns levererbarhet**

När du har delegerat en ny underdomän kan du via Kontrollpanelen spåra den granskning som utförs av levererbarhetsteamet. [Läs mer](subdomains-certificates/using/setting-up-new-subdomain.md)

**Hantera GPG-nycklar**

Kontrollpanelen kan generera ett par GPG-nycklar vilket innebär att du enkelt kan dekryptera data som kommer till Campaign utifrån. Vi har dessutom lagt till en funktion som gör att du kan installera en offentlig GPG-nyckel för att kryptera data som skickas från Campaign. [Läs mer](instances-settings/using/gpg-keys-management.md)

**Övervaka aktiva profiler**

Via Kontrollpanelen kan du nu övervaka antalet aktiva profiler som används av dina instanser och räknas i faktureringssyfte. [Läs mer](performance-monitoring/using/active-profiles-monitoring.md)

>[!IMPORTANT]
>
>Att övervaka aktiva profiler i Kontrollpanelen finns tillgängligt som betaversion och kan ofta uppdateras och ändras utan föregående meddelande.

## Maj 2020 {#may-2020}

**Hantera certifikat för CNAME-underdomäner**

Via Kontrollpanelen kan du nu förnya SSL-certifikaten för dina underdomäner som har konfigurerats med CNAME-metoden. [Läs mer](subdomains-certificates/using/renewing-subdomain-certificate.md)

## April 2020 {#april-2020}

**Hantera Google TXT-poster**

Lägg till Google TXT-poster för webbplatsverifiering i alla dina underdomäner som används för att skicka e-postmeddelanden till Gmail-adresser via Kontrollpanelen i Campaign. [Läs mer](subdomains-certificates/using/managing-txt-records.md)

**Övervaka databasens diskutrymme**

Kontrollpanelen i Campaign är utrustad med funktioner för databasövervakning vilket gör att du kan se hur databasen utnyttjar diskutrymmet vid behov och över tid. [Läs mer](performance-monitoring/using/database-monitoring.md)

**E-postavisering**

Kontrollpanelen i Campaign är utrustad med funktioner för e-postavisering i realtid. Detta gör det möjligt att logga in på Kontrollpanelen och registrera dig för att få aviseringar om systemets prestanda riskerar att försämras eller om du behöver vidta åtgärder för att säkerställa hög prestanda i framtiden. [Läs mer](performance-monitoring/using/email-alerting.md)

## Januari 2020 {#january-2020}

*22 januari 2020*

Vi har lagt till nya funktioner för administratörsanvändare som nu kan konfigurera underdomäner och förnya SSL-certifikat via Kontrollpanelen.

Mer information finns på följande sidor:
* [Konfigurera en ny underdomän](subdomains-certificates/using/setting-up-new-subdomain.md)
* [Förnya en underdomäns SSL-certifikat](subdomains-certificates/using/renewing-subdomain-certificate.md)

>[!IMPORTANT]
>
>Funktionerna kommer att finnas i betaversionen och kan ofta uppdateras och ändras utan föregående meddelande.

## September 2019 {#september-2019}

*16 september 2019*

Vi har lagt till nya funktioner för administratörsanvändare som nu kan lägga till IP-adresser i tillåtelselistan för att ansluta till instanser i Campaign Classic.
Dessutom kan administratörsanvändare nu se listan över instanser i Campaign Classic och berättigande till uppgraderingar av builds.

Se den [särskilda dokumentationen](instances-settings/using/ip-allow-listing-instance-access.md) för mer information.

## Augusti 2019 {#august-2019}

Vi har lagt till nya funktioner för administratörsanvändare som nu kan få meddelanden innan SSL-certifikat för deras domäner upphör att gälla. Se den [detaljerade dokumentationen](subdomains-certificates/using/monitoring-ssl-certificates.md) för mer information.

Administratörsanvändare kan nu även ta bort SSH-nycklar som har lagts till för att komma åt SFTP-servrar.

## Juli 2019 {#july-2019}

Vi har lagt till nya funktioner som ger administratörsanvändare större kontroll över instansinställningarna i Campaign Classic. De nya funktionerna i Kontrollpanelen inkluderar möjligheten att lägga till URL:er som Adobe Campaign kan ansluta till för data-/filöverföringar.

Se den [detaljerade dokumentationen](instances-settings/using/url-permissions.md) för mer information.
