---
title: Versionsinformation för 2023
description: Denna sida listar alla 2023-versioner av Kontrollpanelen.
feature: Control Panel, Release Notes
role: Admin
level: Experienced
exl-id: 9a83e32a-4c11-4784-a6fe-341ce9ebc7a7
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: ht
source-wordcount: '341'
ht-degree: 100%

---

# Versionsinformation för 2023 {#rn-2023}

## September 2023 {#september-2023}

<table>
<thead>
<tr>
<th><strong>Hantering av DMARC- och BIMI-poster</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><p>Nu kan du lägga till DMARC- och BIMI-poster direkt från kontrollpanelen:

<ul><li><strong>DMARC-poster</strong> tillhandahåller ett sätt att autentisera avsändarens domän och förhindra obehörig användning av domänen för skadliga syften. <a href="../subdomains-certificates/using/dmarc.md">Lär dig hur du lägger till DMARC-poster</a></li>
<li><strong>BIMI-poster</strong> gör att du kan visa en godkänd logotyp bredvid dina e-postmeddelanden i e-postleverantörernas inkorgar för att förbättra varumärkesigenkänningen och förtroendet för dem. <a href="../subdomains-certificates/using/bimi.md">Lär dig hur du lägger till BIMI-poster</a></li></ul>
</td>
</tr>
</tbody>
</table>

## Juni 2023 {#june-2023}

* Nu kan du delegera SSL-certifikat för redan delegerade underdomäner till Adobe direkt från listan över underdomäner. [Läs mer](../subdomains-certificates/using/delegate-ssl.md)

* Avsändaren av e-postmeddelanden med varningar har ändrats till `"alert@notifications.campaign.adobe.com"`.

## Förbättringar i maj 2023 {#may-2023}

**Underdomäners SSL-certifikatdelegering till Adobe**

Nu kan du låta Adobe hantera dina underdomäners SSL-certifikat. Om du använder CNAME:er för att konfigurera din underdomän, kommer certifikatposter att genereras automatiskt och tillhandahållas för att generera ett certifikat till din värdlösning.

Observera att den här funktionen bara är tillgänglig när du konfigurerar en ny underdomän. Du kan inte delegera certifikat för befintliga delegerade underdomäner. [Läs mer](../subdomains-certificates/using/setting-up-new-subdomain.md)

>[!NOTE]
>
>SSL som hanteras av Adobe är en kostnadsfri funktion som är tillgänglig för användare utan kostnad.

## Mars 2023 {#march-2023}

**Borttagning av delegering av underdomän för CNAME:er**

Nu kan du ta bort delegeringen av underdomäner som har konfigurerats med CNAME:er. [Läs mer](../subdomains-certificates/using/remove-delegated-subdomains.md)

## Februari 2023 {#february-2023}

**Delegeringsborttagning för underdomäner som delegerats till Adobe**

Du kan nu ta bort delegeringen av en underdomän som är helt delegerad till Adobe. [Läs mer](../subdomains-certificates/using/remove-delegated-subdomains.md)

>[!NOTE]
>
>Delegeringsborttagning är för närvarande inte tillgängligt för underdomäner som har konfigurerats med CNAME.

**Servicekalender**

Servicekalendern innehåller nu en kalendervy som håller reda på viktiga händelser som inträffar i dina instanser. Information har dessutom lagts till med meddelanden som skickas till användare som prenumererar på varningar på Kontrollpanelen. [Läs mer](../service-events/service-events.md)

![](assets/do-not-localize/gif-calendar.gif)

## Januari 2023 {#january-2023}

**Ny funktion för hybridvärdmodell**

Kunder med hybridvärdmodell kan nu lägga till IP-adresser till tillåtelselistan för att få tillgång till MID-instanser. [Läs mer](../instances-settings/using/ip-allow-listing-instance-access.md)

**Förbättring av CSR (Certificate Signing Request)**

Fältet Stad/Ort är nu valfritt vid generering av begäran om certifikatsignering.
