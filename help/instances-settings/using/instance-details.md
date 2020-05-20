---
title: Instansinformation
description: Lär dig övervaka instansinformationen på Kontrollpanelen
translation-type: tm+mt
source-git-commit: a2c19296894ff893987290cb287dc7002ab999e5
workflow-type: tm+mt
source-wordcount: '554'
ht-degree: 2%

---


# Instansinformation {#instance-details}

>[!CONTEXTUALHELP]
>id="cp_instancesettings_instancedetails"
>title="Om instansinformation"
>abstract="Visa information om dina Adobe Campaign-instanser: typer, namn, bygginformation och möjliga uppgraderingsrekommendationer."
>additional-url="https://docs.adobe.com/content/help/en/campaign-classic/using/release-notes/latest-release.html" text="Versionsinformation för Campaign Classic"
>additional-url="https://docs.adobe.com/content/help/en/campaign-standard/using/release-notes/release-notes.html" text="Versionsinformation för Campaign Standard"

>[!IMPORTANT]
>
>Den här funktionen är endast tillgänglig för Campaign Classic-instanser.

## Om instansinformation {#about-instance-details}

Instansarkitekturen i Adobe Campaign Classic kan innehålla flera servrar för att möjliggöra flexibilitet i marknadsföringsaktiviteter. Du kan t.ex. ha servrar för marknadsföring, realtid (eller meddelandecenter) och MID-källor som stöder din instans.

Med funktionen Instansinformation kan du visa instansens platta arkitektur. Förutom serverinformation kan du även ta reda på om instansbygget är aktuellt eller inte, samt rekommendera uppgraderingar när det behövs.

>[!NOTE]
>
>Vi rekommenderar att du uppgraderar dina instanser minst en gång per år för att undvika prestandaförsämringar och kan utnyttja de senaste funktionerna och korrigeringarna som Adobe Campaign Classic har att erbjuda.

**Relaterade ämnen:**

* [Utföra en bygguppgradering](https://docs.campaign.adobe.com/doc/AC/getting_started/EN/buildUpgrade.html)
* [Uppdatera Adobe Campaign](https://docs.campaign.adobe.com/doc/AC/en/PRO_Updating_Adobe_Campaign_Introduction.html)

## Hämtar information om dina instanser {#retrieving-information-about-instances}

Följ de här stegen för att få information om servrarna som är anslutna till dina instanser:

1. Öppna **[!UICONTROL Instances Settings]**-kortet för att öppna fliken **[!UICONTROL Instance Details]**.

   >[!NOTE]
   >
   >Om instansinställningskortet inte visas på kontrollpanelens startsida innebär det att ditt IMS-ORG-ID inte är kopplat till några Adobe Campaign Classic-instanser

1. Välj önskad Campaign Classic-instans i den vänstra rutan.

   >[!NOTE]
   >
   >Alla Campaign-instanser visas i listan i den vänstra rutan. Eftersom funktionen Instansinformation endast är avsedd för Campaign Classic-instanser visas meddelandet&quot;Ej tillämpbar instans&quot; om du väljer en Campaign Standard-instans.

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

**Jag ser inte MID-servern på min instansarkitektur, innebär det att mina instanser inte fungerar som de ska? Behöver jag RT-instansen för något jag inte kan göra idag?**

Din egen instans kan se väldigt annorlunda ut, den kanske inte har alla typer av servrar, eller så kan den ha flera av samma server. Att du inte har en typ av server eller en annan innebär inte att du inte kan skicka ett realtidsmeddelande eller utföra andra typer av aktiviteter. Du kan begära ytterligare serverkapacitet, ytterligare avgifter tillkommer.

Kontakta kundtjänst om du tror att vissa servrar inte visas på sidan Instansinformation. Observera den specifika instansens URL i meddelandet.
