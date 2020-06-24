---
title: Kontrollpanelsversioner
translation-type: tm+mt
source-git-commit: a83309bfb6e42db231fe970f47475fb85d6d441b
workflow-type: tm+mt
source-wordcount: '605'
ht-degree: 0%

---


# Kontrollpanelsversioner {#control-panel-releases}

Här finns information om de senaste versionerna av Kontrollpanelen.

>[!NOTE]
>
>Observera att Kontrollpanelen endast är tillgänglig för kunder som har AWS som värd, med undantag för hybridmiljöer som ännu inte stöds. Du behöver inte uppgradera för att komma åt Kontrollpanelen. Se till att du är en admin-användare för att få tillgång till den.

## Juni 2020 {#june-2020}

**Granskning av deldomänsleverans**

När du har delegerat en ny underdomän kan du via Kontrollpanelen nu spåra den granskning som utförts av gruppen Deliverability. [Läs mer](subdomains-certificates/using/setting-up-new-subdomain.md)

**Hantering av GPG-nycklar**

Med Kontrollpanelen kan ni nu generera ett par GPG-nycklar, så att ni enkelt kan dekryptera data som kommer till Campaign utifrån. Dessutom har vi lagt till en funktion så att du kan installera en offentlig GPG-nyckel för att kryptera data som skickas från Campaign. [Läs mer](instances-settings/using/gpg-keys-management.md)
* [Campaign Standard, självstudievideo](https://docs.adobe.com/content/help/en/campaign-standard-learn/tutorials/administrating/control-panel/generating-and-installing-gpg-keys.html)
* [Campaign Classic - videokurs](https://docs.adobe.com/content/help/en/campaign-classic-learn/tutorials/administrating/control-panel-acc/generating-and-installing-gpg-keys.html)

**Borttagning av vitlista/svartlista**

Både&quot;vitlista&quot; och&quot;svartlista&quot; har tagits bort från Adobe Campaign dokumentation. Vissa förekomster av dessa termer kan fortfarande förekomma i produktgränssnittet, alternativnamn och intern kod, men kommer att ersättas i kommande Campaign-versioner med blocklist och allowlist.

**Övervakning av aktiva profiler**

Med kontrollpanelen kan du nu övervaka antalet aktiva profiler som används av dina instanser och räknas i faktureringssyfte. [Läs mer](performance-monitoring/using/active-profiles-monitoring.md)

>[!IMPORTANT]
>
>Övervakning av aktiva profiler från Kontrollpanelen finns i betaversion och kan uppdateras ofta och ändras utan föregående meddelande.
>
>Funktionen är tillgänglig för kunder som har AWS som värd från Campaign Standard 10368 build och Campaign Classic 8931 build. Om du använder en tidigare version måste du uppgradera för att kunna använda den här funktionen.

## Maj 2020 {#may-2020}

**Certifikathantering för CNAME-underdomäner**

Med kontrollpanelen kan du nu förnya SSL-certifikaten för dina underdomäner som har delegerats med CNAME-metoden. [Läs mer](subdomains-certificates/using/renewing-subdomain-certificate.md)

## April 2020 {#april-2020}

**Google TXT-posthantering**

Lägg till Google TXT-webbplatsverifieringspost i alla dina underdomäner som används för att skicka e-post till Gmail-adresser via Kontrollpanelen för Campaign. [Läs mer](subdomains-certificates/using/managing-txt-records.md)

**Övervakning av databasutrymme**

Campaign Control Panel är utrustad med funktioner för databasövervakning, vilket gör att du kan visa databasens utrymmesutnyttjande vid behov och över tid. [Läs mer](performance-monitoring/using/database-monitoring.md)

**E-postavisering**

Campaign Control Panel är utrustad med funktioner för e-postavisering i realtid, så att du kan logga in på Kontrollpanelen och registrera dig för att få aviseringar när datorn riskerar att försämras eller om du behöver vidta åtgärder för att få höga prestanda i framtiden. [Läs mer](performance-monitoring/using/email-alerting.md)

## Januari 2020 {#january-2020}

*22 januari 2020*

Vi har lagt till nya funktioner för administratörsanvändare att delegera underdomäner och förnya SSL-certifikat från Kontrollpanelen.

Mer information finns på följande sidor:
* [Konfigurera en ny underdomän](subdomains-certificates/using/setting-up-new-subdomain.md)
* [Förnya en underdomäns SSL-certifikat](subdomains-certificates/using/renewing-subdomain-certificate.md)

>[!IMPORTANT]
>
>Funktionerna kommer att finnas i betaversionen och kan uppdateras ofta och ändras utan föregående meddelande.

## September 2019 {#september-2019}

*16 september 2019*

Vi har lagt till nya funktioner för administratörsanvändare att lägga till IP-adresser i listan över tillåtna för att ansluta till instanser i Campaign Classic.
Dessutom kan administratörsanvändare nu visa en lista över instanser i Campaign Classic och behörighet för uppgraderingar.

Mer information finns i den [dedikerade dokumentationen](instances-settings/using/ip-whitelisting-instance-access.md).

## Augusti 2019 {#august-2019}

Vi har lagt till nya funktioner så att administratörsanvändare kan ta emot meddelanden innan SSL-certifikat för sina domäner upphör att gälla. Mer information finns i den [detaljerade dokumentationen](subdomains-certificates/using/monitoring-ssl-certificates.md).

Administratörsanvändare kan nu även ta bort SSH-nycklar som har lagts till för att komma åt SFTP-servrar.

## Juli 2019 {#july-2019}

Vi har lagt till nya funktioner som ger administratörsanvändare större kontroll över instansinställningarna i Campaign Classic. De nya funktionerna i Kontrollpanelen innefattar möjligheten att lägga till URL:er som Adobe Campaign ansluter till för data-/filöverföringar.

Mer information finns i den [detaljerade dokumentationen](instances-settings/using/url-permissions.md).
