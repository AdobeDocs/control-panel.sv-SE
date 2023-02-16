---
title: Versionsinformation för 2022
description: Denna sida listar alla 2022-versioner av Kontrollpanelen.
exl-id: 9fb18bb6-c4e4-48aa-849c-d9129add5266
source-git-commit: e0eb0bba95bcd02fef8f9bac4e9605711d3a9c30
workflow-type: ht
source-wordcount: '0'
ht-degree: 100%

---

# Versionsinformation för 2022 {#rn-2022}

## Oktober 2022 {#october-2022}

E-postavisering meddelar dig nu när ett av dina SSL-certifikat upphör att gälla inom 30 dagar eller mindre. [Läs mer](../performance-monitoring/using/email-alerting.md)

## September 2022 {#september-2022}

Kunder med hybridvärdmodell kan nu konfigurera nya underdomäner. [Läs mer](../subdomains-certificates/using/setting-up-new-subdomain.md)

## Augusti 2022 {#august-2022}

* Kunder med hybridvärdmodell kan nu verifiera sina underdomäner. [Läs mer](../subdomains-certificates/using/monitoring-subdomains.md)
* Fältet Organisationsenhet (OU) är nu valfritt i CSR (Certificate Generation Request). [Läs mer](../subdomains-certificates/using/renewing-subdomain-certificate.md)

## Juli 2022 {#july-2022}

<table>
<thead>
<tr>
<th><strong>Installation av underdomäners certifikat för hybridvärdmodell</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><p>Kunder med hybridvärdmodell kan nu förnya underdomänernas SSL-certifikat från Kontrollpanelen.</p><p>Mer information finns i den <a href="../subdomains-certificates/using/renewing-subdomain-certificate.md">detaljerade dokumentationen.</a></p>
</td>
</tr>
</tbody>
</table>

## Juni 2022 {#june-2022}

### Nyheter?

<table>
<thead>
<tr>
<th><strong>De 10 mest utrymmeskrävande filerna på SFTP-servrar</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Nu kan du identifiera de 10 mest utrymmeskrävande filerna på en SFTP-server. <a href="../sftp/using/sftp-storage-management.md">Läs mer</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Servicekalender-påminnelser</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Med Servicekalendern kan du nu ange påminnelser så att du kan meddelas via e-post innan en händelse inträffar på dina instanser. <a href="../service-events/service-events.md">Läs mer</a></p>
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
<th><strong>Uppdateringar av genomflöden och fördröjningsövervakning</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Övervakningsfunktioner av genomflöden och fördröjningar har förbättrats:<ul><li>Nu kan du identifiera ID:n för de fem vanligaste leveranserna som bidrar till genomflödet av din instans.</li><li>Campaign Classic v7-/v8-kunder kan nu visualisera fördröjning för en viss kanal.</p></li><p>Mer information finns i den <a href="../performance-monitoring/using/throughputs-latencies.md">detaljerade dokumentationen.</a></p>
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
<th><strong>Tillgänglighet av genomflöden och fördröjningsövervakning</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Genomflödes- och fördröjningsövervakning är nu tillgänglig för alla Campaign Standard- och v8-kunder, och för Campaign V7-kunder med build-nummer 9032,9330, 9346 eller 9349 som har fristående distributioner (utan någon mellaninstans).</p><p>Mer information finns i den <a href="../performance-monitoring/using/throughputs-latencies.md">detaljerade dokumentationen.</a></p>
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
<p>Nu kan du övervaka hur leveransgenomflöden och fördröjning trendar över en tidsperiod för dina instanser.</p><p>Mer information finns i den <a href="../performance-monitoring/using/throughputs-latencies.md">detaljerade dokumentationen</a>.</p>
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
