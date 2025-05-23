---
product: campaign
solution: Campaign
title: Instansinformation
description: Läs om hur man övervakar information om instanser i Kontrollpanelen
feature: Control Panel, Monitoring
role: Admin
level: Experienced
exl-id: 02819bfc-9886-43fc-8014-9bfe64c42048
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 69%

---

# Instansinformation {#instance-details}

>[!CONTEXTUALHELP]
>id="cp_instancesettings_instancedetails"
>title="Om instansinformation"
>abstract="Visa information om dina Adobe Campaign-instanser: typer, namn, bygginformation och möjliga uppgraderingsrekommendationer."

## Om instansinformation {#about-instance-details}

>[!IMPORTANT]
>
>Den här funktionen är endast tillgänglig för Campaign v7-/v8-instanser.

Instansarkitekturen i Adobe Campaign kan innehålla flera servrar för att möjliggöra flexibilitet i marknadsföringsaktiviteter. Du kan t.ex. ha servrar för marknadsföring, realtid (eller meddelandecenter) samt mid-sourcing som har stöd för din instans.

Funktionaliteten i Instansinformationen låter dig se instansens platta arkitektur. Förutom serverinformation får du även reda på om instansens build är aktuell eller inte samt rekommendationer om uppgraderingar när det behövs.

>[!NOTE]
>
>Vi rekommenderar att dina instanser uppgraderas minst en gång per år för att undvika prestandaförsämringar och att du kan utnyttja de senaste funktionerna och korrigeringarna som Adobe Campaign v7/v8 har att erbjuda.

**Relaterade ämnen:**

* [Utföra en uppgradering av din build](https://experienceleague.adobe.com/docs/campaign-classic/using/monitoring-campaign-classic/updating-adobe-campaign/build-upgrade.html?lang=sv-SE)
* [Uppdatera Adobe Campaign](https://experienceleague.adobe.com/docs/campaign-classic/using/monitoring-campaign-classic/updating-adobe-campaign/introduction.html?lang=sv-SE)

## Hämtar information om dina instanser {#retrieving-information-about-instances}

Följ dessa steg för att få information om servrarna som är anslutna till dina instanser:

1. Öppna **[!UICONTROL Instances Settings]**-kortet för att öppna fliken **[!UICONTROL Instance Details]**.

   >[!NOTE]
   >
   >Om instansinställningskortet inte visas på kontrollpanelens hemsida innebär det att ditt företags-ID inte är kopplat till några Adobe Campaign v7/v8-instanser

1. Välj önskad Campaign-instans i den vänstra rutan.

   >[!NOTE]
   >
   >Alla instanser i Campaign visas i listan i det vänstra fönstret. Eftersom funktionen Instansinformation endast är dedikerad till Campaign v7/v8-instanser visas meddelandet&quot;Ej tillämpbar instans&quot; om du markerar en Campaign Standard.

1. Servrarna som är anslutna till instansen visas.

   ![](assets/instance_details.png)

Tillgänglig information är:

* **[!UICONTROL Type]**: servertypen. Möjliga värden är MKT (marknadsföring), MID (mid-sourcing) och RT (meddelandecenter/realtidsmeddelanden).
* **[!UICONTROL Name]**: serverns namn.
* **[!UICONTROL Build:]** den version som är installerad på servern.
* **[!UICONTROL Upgrade info]**: den här kolumnen informerar dig om eventuell uppdatering som krävs för servern.
   * Grön: din server är aktuell och ingen uppgradering krävs.
   * Gul: du bör överväga att uppgradera. Du saknar de senaste funktionerna och korrigeringarna.
   * Röd: uppgradera så snart som möjligt. Du saknar nya funktioner och serverprestandan kanske inte är optimal.

Om någon av dina servrar behöver uppgraderas finns mer information om hur du fortsätter i [den här dokumentationen](https://experienceleague.adobe.com/docs/campaign-classic/using/monitoring-campaign-classic/updating-adobe-campaign/build-upgrade.html?lang=sv-SE).

## Vanliga frågor {#common-questions}

**Jag kan inte se MID-servern i min instansarkitektur. Betyder detta att mina instanser inte fungerar som de ska? Behöver jag RT-instansen för något jag inte kan göra idag?**

Din egen instans kan se väldigt annorlunda ut. Den kanske inte har alla typer av servrar eller kan den ha flera av samma server. Även om du inte har en typ av server kan du fortfarande skicka ett realtidsmeddelande eller utföra andra typer av aktiviteter. Du kan begära ytterligare serverkapacitet. Ytterligare avgifter tillkommer i detta fall.

Kontakta Kundtjänst om du tror att vissa servrar inte visas på sidan Instansinformation. Inkludera den instansens specifika URL i meddelandet.
