---
product: campaign
solution: Campaign
title: Lägg till MID/RT-instanser (hybridmodell)
description: Lär dig hur du lägger till MID/RT-instanser på Kontrollpanelen med hybridvärdmodellen.
feature: Control Panel, Access Management
role: Admin
level: Intermediate
exl-id: ff64acbe-d8cb-499b-b20f-b0934fb0f695
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 100%

---

# Lägg till MID/RT-instanser (hybridmodell){#add-mid-rt-instances-hybrid-model}

>[!CONTEXTUALHELP]
>id="cp_externalaccounts"
>title="Externa konton"
>abstract="På den här skärmen kan kunder med hybridvärdmodell tillhandahålla URL:en för MID/RT-instansen som konfigurerats i marknadsinstansen på Kontrollpanelen för att utnyttja funktionerna på Kontrollpanelen."

Kontrollpanelen gör det möjligt för kunder med hybridvärdmodeller att utnyttja särskilda funktioner i Kontrollpanelen. För att göra detta måste du:

* [Ange URL för MID/RT-instans](#add) konfigurerad i din marknadsföringsinstans på Kontrollpanelen,
* [Lägg till IP-adressen för MID/RT-instansen i tillåtelselistan](#ip) så att marknadsinstansen kan ansluta till den.

Mer information om värdmodeller finns i [Dokumentation för Campaign Classic](https://experienceleague.adobe.com/docs/campaign-classic/using/installing-campaign-classic/architecture-and-hosting-models/hosting-models-lp/hosting-models.html?lang=sv).

## Lägg till en MID/RT-instans {#add}

>[!CONTEXTUALHELP]
>id="cp_externalaccounts_url"
>title="URL"
>abstract="URL för instansen, som finns i klientkonsolen för Campaign i menyn Administration > Plattform > Externa konton."

>[!CONTEXTUALHELP]
>id="cp_externalaccounts_operator"
>title="Operatör"
>abstract="ID för den operator som tillhandahålls efter inledande etablering av Adobe Admin."

>[!CONTEXTUALHELP]
>id="cp_externalaccounts_password"
>title="Lösenord"
>abstract="Lösenord för den operator som tillhandahålls efter inledande etablering av Adobe Admin."

Hybridkunder bör ansluta till Kontrollpanelen via Experience Cloud. Första gången du öppnar Kontrollpanelen visas bara två kort på hemsidan.

![](assets/hybrid-homepage.png)

>[!NOTE]
>
>Om du stöter på eventuella problem med att komma åt Kontrollpanelen är det troligast att din marknadsföringsinstans inte har mappats med ditt [organisations-ID](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=sv) än. Kontakta kundtjänst för att slutföra den här installationen och fortsätta. När anslutningen lyckas visas startsidan för Kontrollpanelen.

För att kunna komma åt funktioner på Kontrollpanelen måste du ange din information för MID/RT-instansen i kortet **[!UICONTROL Instances Settings]**. Följ stegen nedan för att göra detta.

1. I kortet **[!UICONTROL Instances Settings]** väljer du fliken **[!UICONTROL External Accounts]**.

1. Välj önskad marknadsinstans i rullgardinsmenyn och klicka sedan på **[!UICONTROL Add new URL]**.

   ![](assets/external-account-addbutton.png)

1. Ange information om MID/RT-instansen som ska läggas till.

   ![](assets/external-account-add.png)

   * **[!UICONTROL URL]**: URL för instansen som finns i klientkonsolen för Campaign i menyn **[!UICONTROL Administration]** > **[!UICONTROL Platform]** > **[!UICONTROL External Accounts]**.

     ![](assets/external-account-url.png)

   * **[!UICONTROL Operator]** / **[!UICONTROL Password]**: autentiseringsuppgifter för den operatör som tillhandahålls efter inledande etablering av Adobe Admin.

     >[!NOTE]
     >
     >Kontakta kundtjänst om dessa uppgifter inte är tillgängliga.

1. Klicka på **[!UICONTROL Save]** för att bekräfta.

När du lägger till MID/RT-URL aktiveras en asynkron process för att validera URL-adressernas korrekthet. Den här processen kan ta några minuter. Jobbet väntar tills URL:en för MID/RT-instansen har verifierats. Du kan bara komma åt huvudfunktionerna i Kontrollpanelen när valideringen är klar.

![](assets/external-account-pending.png)

Du kan när som helst ta bort eller inaktivera URL:en för MID/RT-instansen genom att markera den i listan.

![](assets/external-account-edit.png)

Observera att du kan övervaka alla åtgärder som utförs i fliken **[!UICONTROL External Accounts]** på en URL för MID/RT-instans från **[!UICONTROL Job Logs]**:

![](assets/external-account-logs.png)

## Lägg till IP-adressen i tillåtelselistan {#ip}

När MID/RT-instansen har lagts till måste du lägga till dess IP-adress i tillåtelselistan så att din marknadsinstans kan ansluta till den.

Detta kan utföras från fliken **[!UICONTROL IP Allow Listing]** på **[!UICONTROL Instances Settings]**-kortet. [Lär dig hur du lägger till IP-adresser i tillåtelselistan](ip-allow-listing-instance-access.md)

När du är klar kan du använda funktionerna i Kontrollpanelen med MID/RT-instansen.

## Tillgängliga funktioner för hybridkunder {#capabilities}

När du har lagt till en MID/RT-instans på Kontrollpanelen kan du utnyttja funktionerna som listas nedan:

* [Övervaka viktiga kontakter och händelser](../../service-events/service-events.md)
* [Visa din instansinformation](../../instances-settings/using/instance-details.md),
* [Lägga till IP-adresser i tillåtelselistan](../../instances-settings/using/ip-allow-listing-instance-access.md),
* [Konfigurera nya underdomäner](../../subdomains-certificates/using/setting-up-new-subdomain.md),
* [Förnya underdomäners SSL-certifikat](../../subdomains-certificates/using/renewing-subdomain-certificate.md).
