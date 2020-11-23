---
product: campaign
solution: Campaign
title: Versioner av Kontrollpanelen
translation-type: tm+mt
source-git-commit: 1e1421494e5a6e357e56a77ee192475a03d18a28
workflow-type: tm+mt
source-wordcount: '590'
ht-degree: 95%

---


# Versioner av Kontrollpanelen {#control-panel-releases}

Här finns information om de senaste versionerna av Kontrollpanelen.

>[!NOTE]
>
>Observera att Kontrollpanelen endast är tillgänglig för kunder som har AWS som värd med undantag för hybridmiljöer som ännu inte stöds. Du behöver inte uppgradera för att komma åt Kontrollpanelen. Se till att du är en administratörsanvändare för att få åtkomst.

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
>
>Funktionen är tillgänglig för kunder som har AWS som värd från Campaign Standard build 10368 och Campaign Classic build 8931. Om du använder en tidigare build måste du uppgradera för att kunna använda den här funktionen.

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
* [Konfigurera en ny underdomän ](subdomains-certificates/using/setting-up-new-subdomain.md)
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
