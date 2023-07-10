---
title: Versionsinformation för 2023
description: Denna sida listar alla 2023-versioner av Kontrollpanelen.
exl-id: 9a83e32a-4c11-4784-a6fe-341ce9ebc7a7
source-git-commit: 40654418f0c5b298cc4fbd66a5d835355876a12c
workflow-type: ht
source-wordcount: '242'
ht-degree: 100%

---

# Versionsinformation för 2023 {#rn-2023}

## Förbättringar i maj 2023 {#june-2023}

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
