---
title: Instansinformation
description: Lär dig övervaka instansinformationen på Kontrollpanelen
translation-type: tm+mt
source-git-commit: 35723590195ef54df42d1d1df5b37490787f8836
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Instansinformation {#instance-details}

>[!CONTEXTUALHELP]
>id="cp_instancesettings_instancedetails"
>title="Om instansinformation"
>abstract="Visa information om dina Adobe Campaign-instanser: typer, namn, bygginformation och möjliga uppgraderingsrekommendationer."
>additional-url="https://docs.adobe.com/content/help/en/campaign-classic/using/release-notes/latest-release.html" text="Versionsinformation för Campaign Classic"
>additional-url="https://docs.adobe.com/content/help/en/campaign-standard/using/release-notes/release-notes.html" text="Versionsinformation om Campaign Standard"

>[!IMPORTANT]
>
>Den här funktionen är endast tillgänglig för instanser i Campaign Classic.

## Om instansinformation {#about-instance-details}

Instansarkitekturen i Adobe Campaign Classic kan innehålla flera servrar för att möjliggöra flexibilitet i marknadsföringsaktiviteter. Du kan t.ex. ha servrar för marknadsföring, realtid (eller meddelandecenter) och MID-källor som stöder din instans.

Med funktionen Instansinformation kan du visa instansens platta arkitektur. Förutom serverinformation kan du även ta reda på om instansbygget är aktuellt eller inte, samt rekommendera uppgraderingar när det behövs.

>[!NOTE]
>
>Vi rekommenderar att du uppgraderar dina instanser minst en gång per år för att undvika prestandaförsämringar och att du kan utnyttja de senaste funktionerna och korrigeringarna som Adobe Campaign Classic har att erbjuda.

**Relaterade ämnen:**

* [Utföra en bygguppgradering](https://docs.campaign.adobe.com/doc/AC/getting_started/EN/buildUpgrade.html)
* [Uppdaterar Adobe Campaign](https://docs.campaign.adobe.com/doc/AC/en/PRO_Updating_Adobe_Campaign_Introduction.html)

## Hämtar information om dina instanser {#retrieving-information-about-instances}

Följ de här stegen för att få information om servrarna som är anslutna till dina instanser:

1. Öppna **[!UICONTROL Instances Settings]**-kortet för att öppna fliken **[!UICONTROL Instance Details]**.

   >[!NOTE]
   >
   >Om instansinställningskortet inte visas på kontrollpanelens hemsida innebär det att ditt IMS-organisations-ID inte är kopplat till några Adobe Campaign Classic-instanser

1. Markera den önskade Campaign Classic-instansen i den vänstra rutan.

   >[!NOTE]
   >
   >Alla Campaign-instanser visas i listan i den vänstra rutan. Eftersom funktionen Instansinformation endast är avsedd för instanser i Campaign Classic visas meddelandet&quot;Icke-tillämpbar instans&quot; om du markerar en instans i Campaign Standarden.

1. Servrarna som är anslutna till instansvisningen.

   ![](assets/instance_details.png)

Tillgänglig information är:

* **[!UICONTROL Type]**: servertypen. Möjliga värden är MKT (Marketing), MID (Mid sourcing) och RT (Message Center/Real-time Messaging).
* **[!UICONTROL Name]**: serverns namn.
* **[!UICONTROL Build:]** den version som är installerad på servern.
* **[!UICONTROL Upgrade info]**: den här kolumnen informerar dig om någon uppdatering krävs för servern.
   * Grön: din server är aktuell, ingen uppgradering krävs.
   * Gul: du bör överväga att uppgradera. Du saknar de senaste funktionerna och korrigeringarna.
   * Röd: uppgradera så snart som möjligt. Du saknar nya funktioner och serverprestandan kanske inte är optimal.

Om någon av dina servrar behöver uppgraderas finns mer information om hur du fortsätter i [den här dokumentationen](https://docs.campaign.adobe.com/doc/AC/getting_started/EN/buildUpgrade.html) .

## Vanliga frågor {#common-questions}

**Jag kan inte se MID-servern på min instansarkitektur. Betyder det att mina instanser inte fungerar som de ska? Behöver jag RT-instansen för något jag inte kan göra idag?**

Din egen instans kan se väldigt annorlunda ut, den kanske inte har alla typer av servrar, eller så kan den ha flera av samma server. Att du inte har en typ av server eller en annan innebär inte att du inte kan skicka ett realtidsmeddelande eller utföra andra typer av aktiviteter. Du kan begära ytterligare serverkapacitet, ytterligare avgifter tillkommer.

Kontakta kundtjänst om du tror att vissa servrar inte visas på sidan Instansinformation. Observera den specifika instansens URL i meddelandet.
