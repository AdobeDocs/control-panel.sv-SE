---
title: Kontrollpanelsversioner
translation-type: tm+mt
source-git-commit: 98f2fa0b3e943026bda28b615f0f11db54c404a6
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 0%

---


# Kontrollpanelsversioner {#control-panel-releases}

Här finns information om de senaste versionerna av Kontrollpanelen.

>[!NOTE]
>
>Observera att Kontrollpanelen endast är tillgänglig för kunder som har AWS som värd, med undantag för hybridmiljöer som ännu inte stöds. Du behöver inte uppgradera för att komma åt Kontrollpanelen. Se till att du är en admin-användare för att få tillgång till den.

## Maj 2020 (#may-2020)

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

Vi har lagt till nya funktioner för administratörsanvändare som vitlistar IP-adresser för att ansluta till Campaign Classic-instanser.
Dessutom kan administratörsanvändare nu visa en lista över Campaign Classic-instanser och behörighet för uppgraderingar.

Mer information finns i den [dedikerade dokumentationen](instances-settings/using/ip-whitelisting-instance-access.md).

## Augusti 2019 {#august-2019}

Vi har lagt till nya funktioner så att administratörsanvändare kan ta emot meddelanden innan SSL-certifikat för sina domäner upphör att gälla. Mer information finns i den [detaljerade dokumentationen](subdomains-certificates/using/monitoring-ssl-certificates.md).

Administratörsanvändare kan nu även ta bort SSH-nycklar som har lagts till för att komma åt SFTP-servrar.

## Juli 2019 {#july-2019}

Vi har lagt till nya funktioner som ger administratörsanvändare större kontroll över instansinställningarna för Campaign Classic. De nya funktionerna i Kontrollpanelen innefattar möjligheten att lägga till URL:er som Adobe Campaign ansluter till för data-/filöverföringar.

Mer information finns i den [detaljerade dokumentationen](instances-settings/using/url-permissions.md).
