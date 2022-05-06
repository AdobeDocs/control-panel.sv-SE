---
product: campaign
solution: Campaign
title: Connect MID/RT-instanser
description: Lär dig hur du ansluter MID/RT-instanser till Kontrollpanelen.
feature: Control Panel
role: Architect
level: Intermediate
source-git-commit: 1b712300bd7a1ef8dc784fa977f938bacc4c5e5b
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 5%

---


# Connect MID/RT-instanser

>[!CONTEXTUALHELP]
>id="cp_externalaccounts_url"
>title="Information om underdomäner"
>abstract="På den här skärmen kan kunder med en hybridvärdmodell tillhandahålla sina MID/RT-instanser i sin marknadsinstans för att utföra specifika åtgärder på Kontrollpanelen."

Kontrollpanelen gör det möjligt för kunder med en hybridvärdmodell att utföra specifika åtgärder på Kontrollpanelen genom att tillhandahålla sina MID/RT-instanser i sin marknadsföringsinstans. Mer information om värdmodeller finns i [Campaign Classic dokumentation](https://experienceleague.adobe.com/docs/campaign-classic/using/installing-campaign-classic/architecture-and-hosting-models/hosting-models-lp/hosting-models.html).

## Anslut en MID/RT-instans {#connect}

>[!CONTEXTUALHELP]
>id="cp_externalaccounts_operator"
>title="Information om underdomäner"
>abstract="ID för den operator som används i klientkonsolen för att lägga till MID/RT-instansen i marknadsföringsinstansen."

>[!CONTEXTUALHELP]
>id="cp_externalaccounts_password"
>title="Information om underdomäner"
>abstract="Lösenord för den operator som används i klientkonsolen för att lägga till MID/RT-instansen i marknadsföringsinstansen."

Följ de här stegen för att ange en MID/RT-instans på kontrollpanelen:

1. I **[!UICONTROL Instances Settings]** välj **[!UICONTROL External Accounts]** -fliken.

1. Markera marknadsinstansen i listrutan och klicka sedan på **[!UICONTROL Add new URL]**.

   ![](assets/external-account-addbutton.png)

1. Ange information om MID/RT-instansen som ska anslutas:
   * **[!UICONTROL URL]**: Instansens URL
   * **[!UICONTROL Operator]** / **[!UICONTROL Password]**: Autentiseringsuppgifter för den operator som används i klientkonsolen för att lägga till MID/RT-instansen i marknadsföringsinstansen.

   ![](assets/external-account-add.png)

1. Klicka **[!UICONTROL Save]** för att bekräfta.

Din instans är nu ansluten till Kontrollpanelen. Du kan när som helst ta bort eller inaktivera en anslutning genom att markera den i listan.

![](assets/external-account-edit.png)

## Tillgängliga funktioner för MID/RT-instanser {#capabilities}

När en MID/RT-instans är ansluten till kontrollpanelen kan du använda funktionerna som listas nedan för att övervaka den:

* [Visa din instansinformation](../../instances-settings/using/instance-details.md),
* [Lägg till IP-adresser i tillåtelselistan för att komma åt dina instanser](../../instances-settings/using/ip-allow-listing-instance-access.md),
* [Visa information om delegerade underdomäner](../../subdomains-certificates/using/setting-up-new-subdomain.md),
* [Visa information om SSL-certifikat](../../subdomains-certificates/using/monitoring-ssl-certificates.md).
