---
title: Senaste versionen
description: På den här sidan visas alla nya funktioner och förbättringar för Kontrollpanelen
exl-id: 13aceffb-ceaa-4cfe-8741-95d66c5c6caa
source-git-commit: e0b0daba3a5820dc80b35d8c83ffc9143d547529
workflow-type: tm+mt
source-wordcount: '501'
ht-degree: 55%

---

# Senaste versionen {#control-panel-releases}

På den här sidan visas alla nya funktioner och förbättringar för Kontrollpanelen.

## Juni 2022 {#june-2022}

### Nyheter?

<table>
<thead>
<tr>
<th><strong>De 10 viktigaste filerna tar upp utrymme på SFTP-servrar</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Nu kan du identifiera de 10 mest använda filerna på en SFTP-server. <a href="../sftp/using/sftp-storage-management.md">Läs mer</a></p>
<img src="../assets/do-not-localize/sftp.gif"/>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Påminnelser om servicekalender</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Med Service Calendar kan du nu ange påminnelser så att de kan meddelas via e-post innan en händelse inträffar på dina instanser. <a href="../instances-settings/using/external-accounts.md">Läs mer</a></p>
<img src="../assets/do-not-localize/reminders.gif"/>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Förbättrad CSR-generering för underdomäner</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Flera förbättringar har gjorts i CSR-genereringsprocessen. <a href="../subdomains-certificates/using/renewing-subdomain-certificate.md">Läs mer</a></p><ul><li>När du genererar en CSR kan du nu välja en av de inkluderade underdomänerna som Gemensamt namn.</li><li>Nu kan du kopiera CSR-sammanfattningen innan du genererar CSR.</li><li>När en CSR har skapats kan du hämta den igen från jobbloggarna. Den här funktionen gäller inte certifikat som genererats före den här versionen.</li></ul><p>
<img src="../assets/do-not-localize/CSR.gif"/>
</td>
</tr>
</tbody>
</table>

### Förbättringar

**Instansinställningar**

* Det högsta antalet GPG-tangenter på Kontrollpanelen har ökats till 60 tangenter. [Läs mer](../instances-settings/using/gpg-keys-management.md)

## Maj 2022 {#may-2022}

<table>
<thead>
<tr>
<th><strong>Kontrollpanelens tillgänglighet för hybridvärdmodell</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Kontrollpanelen är nu tillgänglig för kunder med hybridvärdmodell. Dessa kunder kan utnyttja funktionerna i Kontrollpanelen genom att tillhandahålla URL:en för MID/RT-instansen som konfigurerats i deras marknadsinstans på Kontrollpanelen.</p><p>Mer information finns i den <a href="../instances-settings/using/external-accounts.md">detaljerade dokumentationen.</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Övervakningsuppdateringar om genomflöden och fördröjningar</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Övervakningsfunktioner av genomflöden och fördröjningar har förbättrats:<ul><li>Nu kan du identifiera ID:n för de fem vanligaste leveranserna som bidrar till genomflödet av din instans.</li><li>Campaign Classic v7-/v8-kunder kan nu visualisera fördröjning för en viss kanal.</p></li><p>Mer information finns i den <a href="../performance-monitoring/using/thoughputs-latencies.md">detaljerade dokumentationen.</a></p>
</td>
</tr>
</tbody>
</table>


## April 2022 {#april-2022}

<table>
<thead>
<tr>
<th><strong>Övervaka viktiga kontakter och händelser i instanserna</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Du kan nu övervaka tidigare och kommande versioner och servicegranskningar som görs i instanserna, samt få tillgång till en lista över viktiga kontakter hos Adobe för alla förfrågningar och problem.</p><p>Mer information finns i den <a href="../service-events/service-events.md">detaljerade dokumentationen.</a></p>
</td>
</tr>
</tbody>
</table>

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
<p>Dataströmmar och fördröjningsövervakning är nu tillgängliga för alla Campaign Standards- och v8-kunder och för Campaign V7-kunder med build-nummer 9032, 9330, 9346 eller 9349 som har fristående driftsättningar (utan några mellaninstanser).</p><p>Mer information finns i den <a href="../performance-monitoring/using/thoughputs-latencies.md">detaljerade dokumentationen.</a></p>
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
<p>Du kan nu övervaka arbetsflödesparametrar som kan kräva särskild uppmärksamhet för att undvika problem i dina instanser. </p><p>Mer information finns i den <a href="../performance-monitoring/using/workflow-monitoring.md">detaljerade dokumentationen</a>.</p>
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
<p>Med Kontrollpanelen kan du nu övervaka frågor som har körts längst på dina instanser.</p><p>Mer information finns i den <a href="../performance-monitoring/using/database-active-queries.md">detaljerade dokumentationen</a>.</p>
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
<p>Nu kan du övervaka hur leveransgenomflöden och fördröjning trendar över en tidsperiod för dina instanser.</p><p>Mer information finns i den <a href="../performance-monitoring/using/thoughputs-latencies.md">detaljerade dokumentationen</a>.</p>
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
<p>SSL-certifikatåtgärder kan nu utföras på en nyligen konfigurerad underdomän, även om en granskning av leveransen fortfarande pågår.</p><p>Mer information finns i den <a href="../subdomains-certificates/using/renewing-subdomain-certificate.md">detaljerade dokumentationen</a>.</p>
</td>
</tr>
</tbody>
</table>
