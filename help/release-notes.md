---
product: campaign
solution: Campaign
title: Versioner av Kontrollpanelen
description: På den här sidan visas alla nya funktioner och förbättringar för Kontrollpanelen
exl-id: 13aceffb-ceaa-4cfe-8741-95d66c5c6caa
source-git-commit: 35b849725711bfee9852cf8f503bc599f6d8eaff
workflow-type: tm+mt
source-wordcount: '1022'
ht-degree: 63%

---

# Versioner av Kontrollpanelen {#control-panel-releases}

På den här sidan visas alla nya funktioner och förbättringar för Kontrollpanelen.

>[!NOTE]
>
>Kontrollpanelen är bara tillgänglig för administratörsanvändare. Läs mer om behörigheter i [det här avsnittet](https://experienceleague.adobe.com/docs/control-panel/using/discover-control-panel/managing-permissions.html?lang=sv#discover-control-panel).
>
>För Campaign v7 måste din instans lagras på Amazon Web Services (AWS) och uppgraderas till den senaste [Stabilt kampanjbygge](https://experienceleague.adobe.com/docs/campaign-classic/using/release-notes/rn-overview.html?lang=sv#rn-statuses) (eller för att bygga 9032 eller senare). Läs om hur du kontrollerar din version i [det här avsnittet](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/starting-with-adobe-campaign/launching-adobe-campaign.html?lang=sv#getting-your-campaign-version). Följ stegen på [den här sidan](faq.md#hosted-aws) för att kontrollera om instanser har AWS som värd.

## Mars 2022 {#march-2022}

<table>
<thead>
<tr>
<th><strong>Tillgänglighet för genomströmning och fördröjningsövervakning</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Dataströmmar och fördröjningsövervakning är nu tillgängliga för alla Campaign Standards- och v8-kunder och för Campaign V7-kunder med build-nummer 9032, 9330, 9346 eller 9349 som har fristående driftsättningar (utan några mellaninstanser).</p><p>Mer information finns i den <a href="performance-monitoring/using/thoughputs-latencies.md">detaljerade dokumentationen.</a></p>
</td>
</tr>
</tbody>
</table>

## Februari 2022 {#february-2022}

<table>
<thead>
<tr>
<th><strong>Övervakning av arbetsflödesparametrar</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Du kan nu övervaka arbetsflödesparametrar som kan kräva särskild uppmärksamhet för att undvika problem i dina instanser. </p><p>Mer information finns i den <a href="performance-monitoring/using/workflow-monitoring.md">detaljerade dokumentationen</a>.</p>
</td>
</tr>
</tbody>
</table>

## Januari 2022 {#january-2022}

<table>
<thead>
<tr>
<th><strong>Övervaka aktiva frågor</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Med Kontrollpanelen kan du nu övervaka frågor som har körts längst på dina instanser.</p><p>Mer information finns i den <a href="performance-monitoring/using/database-active-queries.md">detaljerade dokumentationen</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Genomflöden och fördröjningsövervakning</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Nu kan du övervaka hur leveransgenomflöden och fördröjning trendar över en tidsperiod för dina instanser.</p><p>Mer information finns i den <a href="performance-monitoring/using/thoughputs-latencies.md">detaljerade dokumentationen</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>SSL-certifikatåtgärder på nya underdomäner</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>SSL-certifikatåtgärder kan nu utföras på en nyligen konfigurerad underdomän, även om en granskning av leveransen fortfarande pågår.</p><p>Mer information finns i den <a href="subdomains-certificates/using/renewing-subdomain-certificate.md">detaljerade dokumentationen</a>.</p>
</td>
</tr>
</tbody>
</table>

## Oktober 2021 {#october-2021}

<table>
<thead>
<tr>
<th><strong>Giltighetsperiod för IP-intervall och offentlig nyckel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Det går nu att ange en varaktighet för tillgängligheten för IP-intervall och offentliga nycklar. </p><p>Mer information finns i <a href="sftp/using/ip-range-allow-listing.md#adding-ip-addresses-allow-list">IP-intervall tillåter listning</a> och <a href="sftp/using/key-management.md#installing-ssh-key">Nyckelhantering</a> -avsnitt.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>IP-intervall och publika nyckelutgåvor</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Nu kan du redigera <a href="sftp/using/ip-range-allow-listing.md#editing-ip-ranges">IP-intervall</a> och <a href="sftp/using/key-management.md#editing-public-keys">publika nycklar</a> som du skapar. Observera att den här funktionen inte är tillgänglig för objekt som skapats före den aktuella versionen av Kontrollpanelen.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Varningar vid SFTP IP-intervall och utgångsdatum för offentlig nyckel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Funktionen för e-postvarningar innehåller nu varningar om att SFTP IP-adresser tillåter listning av förfallodatum och att SFTP-offentlig nyckel förfaller.</p><p>Mer information finns i den <a href="performance-monitoring/using/email-alerting.md">detaljerade dokumentationen</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Fullt stöd med Campaign v8</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>The <strong>Underdomän</strong> och <strong>Certifikat</strong> hanteringsfunktioner stöds nu av Kontrollpanelen i Adobe Campaign v8.</a>.</p>
</td>
</tr>
</tbody>
</table>

## Augusti 2021 {#august-2021}

<table>
<thead>
<tr>
<th><strong>Stöd för Campaign v8</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Kontrollpanelen är nu tillgänglig för Adobe Campaign v8, förutom <strong>Underdomän</strong> och <strong>Certifikat</strong> hanteringsfunktioner som ännu inte stöds.</p><p>Mer information finns i <a href="https://experienceleague.adobe.com/docs/campaign/campaign-v8/deploy/self-service.html" target="blank">Kampanjdokumentation v8</a>.</p>
</td>
</tr>
</tbody>
</table>

## Oktober 2020 {#october-2020}

<table>
<thead>
<tr>
<th><strong>Konfiguration av underdomäner med CNAME</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Med Kontrollpanelen kan du nu konfigurera en underdomän så att den fungerar med Adobe med CNAME:er direkt från gränssnittet.</p><p>Mer information finns i den <a href="subdomains-certificates/using/setting-up-new-subdomain.md">detaljerade dokumentationen</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Förbättringar i databasövervakningen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Databasövervakningen har förbättrats med ytterligare mätvärden som gör att du kan få detaljerad information om resurser som förbrukar utrymme i databasen.</p><p>Mer information finns i den <a href="performance-monitoring/using/database-monitoring.md">detaljerade dokumentationen</a>.</p>
</td>
</tr>
</tbody>
</table>

## Juni 2020 {#june-2020}

<table>
<thead>
<tr>
<th><strong>Granska en underdomäns levererbarhet</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>När du har delegerat en ny underdomän kan du via Kontrollpanelen spåra den granskning som utförs av levererbarhetsteamet.</p><p>Mer information finns i den <a href="subdomains-certificates/using/setting-up-new-subdomain.md">detaljerade dokumentationen</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Hantera GPG-nycklar</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Kontrollpanelen kan generera ett par GPG-nycklar vilket innebär att du enkelt kan dekryptera data som kommer till Campaign utifrån. Vi har dessutom lagt till en funktion som gör att du kan installera en offentlig GPG-nyckel för att kryptera data som skickas från Campaign.</p><p>Mer information finns i den <a href="instances-settings/using/gpg-keys-management.md">detaljerade dokumentationen</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Aktiv profilövervakning</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Via Kontrollpanelen kan du nu övervaka antalet aktiva profiler som används av dina instanser och räknas i faktureringssyfte.</p><p>Mer information finns i den <a href="performance-monitoring/using/active-profiles-monitoring.md">detaljerade dokumentationen</a>.</p>
</td>
</tr>
</tbody>
</table>

>[!IMPORTANT]
>
>Att övervaka aktiva profiler i Kontrollpanelen finns tillgängligt som betaversion och kan ofta uppdateras och ändras utan föregående meddelande.

## Maj 2020 {#may-2020}

<table>
<thead>
<tr>
<th><strong>Hantera certifikat för CNAME-underdomäner</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Via Kontrollpanelen kan du nu förnya SSL-certifikaten för dina underdomäner som har konfigurerats med CNAME-metoden.</p><p>Mer information finns i den <a href="subdomains-certificates/using/renewing-subdomain-certificate.md">detaljerade dokumentationen</a>.</p>
</td>
</tr>
</tbody>
</table>

## April 2020 {#april-2020}

<table>
<thead>
<tr>
<th><strong>Hantera Google TXT-poster</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Lägg till Google TXT-poster för webbplatsverifiering i alla dina underdomäner som används för att skicka e-postmeddelanden till Gmail-adresser via Kontrollpanelen i Campaign.</p><p>Mer information finns i den <a href="subdomains-certificates/using/managing-txt-records.md">detaljerade dokumentationen</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Övervaka databasens diskutrymme</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Kontrollpanelen i Campaign är utrustad med funktioner för databasövervakning vilket gör att du kan se hur databasen utnyttjar diskutrymmet vid behov och över tid.</p><p>Mer information finns i den <a href="performance-monitoring/using/database-monitoring.md">detaljerade dokumentationen</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>E-postavisering</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Kontrollpanelen i Campaign är utrustad med funktioner för e-postavisering i realtid. Detta gör det möjligt att logga in på Kontrollpanelen och registrera dig för att få aviseringar om systemets prestanda riskerar att försämras eller om du behöver vidta åtgärder för att säkerställa hög prestanda i framtiden.</p><p>Mer information finns i den <a href="performance-monitoring/using/email-alerting.md">detaljerade dokumentationen</a>.</p>
</td>
</tr>
</tbody>
</table>

## Januari 2020 {#january-2020}

Vi har lagt till nya funktioner för administratörsanvändare som nu kan konfigurera underdomäner och förnya SSL-certifikat via Kontrollpanelen.

Mer information finns på följande sidor:
* [Konfigurera en ny underdomän](subdomains-certificates/using/setting-up-new-subdomain.md)
* [Förnya en underdomäns SSL-certifikat](subdomains-certificates/using/renewing-subdomain-certificate.md)

>[!IMPORTANT]
>
>Funktionerna kommer att finnas i betaversionen och kan ofta uppdateras och ändras utan föregående meddelande.

## September 2019 {#september-2019}

Vi har lagt till nya funktioner för administratörsanvändare att lägga till IP-adresser i tillåtelselista för att ansluta till Campaign v7/v8-instanser.
Administratörsanvändare kan nu även visa listan över Campaign v7/v8-instanser och behörighet att bygga uppgraderingar.

Se den [särskilda dokumentationen](instances-settings/using/ip-allow-listing-instance-access.md) för mer information.

## Augusti 2019 {#august-2019}

Vi har lagt till nya funktioner för administratörsanvändare som nu kan få meddelanden innan SSL-certifikat för deras domäner upphör att gälla. Se den [detaljerade dokumentationen](subdomains-certificates/using/monitoring-ssl-certificates.md) för mer information.

Administratörsanvändare kan nu även ta bort SSH-nycklar som har lagts till för att komma åt SFTP-servrar.

## Juli 2019 {#july-2019}

Vi har lagt till nya funktioner för att ge administratörsanvändare större kontroll över instansinställningarna för Campaign v7/v8. De nya funktionerna i Kontrollpanelen inkluderar möjligheten att lägga till URL:er som Adobe Campaign kan ansluta till för data-/filöverföringar.

Se den [detaljerade dokumentationen](instances-settings/using/url-permissions.md) för mer information.
