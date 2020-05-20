---
title: Hantera TXT-poster
description: Lär dig hur du hanterar TXT-poster för verifiering av domänägarskap.
translation-type: tm+mt
source-git-commit: 7c2dd60c70b5f9c0b2567df289582b972a7f76b8
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 0%

---


# Hantera TXT-poster {#managing-txt-records}

>[!CONTEXTUALHELP]
>id="cp_siteverification_add"
>title="Hantera TXT-poster"
>abstract="Vissa tjänster, som Google, kräver att du lägger till en TXT-post i domäninställningarna för att verifiera att du äger domänen."

## Om TXT-poster {#about-txt-records}

TXT-poster är en typ av DNS-poster som används för att tillhandahålla textinformation om en domän, som kan läsas av externa källor.

För att säkerställa höga inkorgstariffer och låga skräppostnivåer kräver vissa tjänster som Google att du lägger till en TXT-post i domäninställningarna för att verifiera att du äger domänen.

Gmail är för närvarande en av de vanligaste e-postadressleverantörerna. Adobe Campaign gör att du kan lägga till särskilda TXT-poster för Google Site verification i dina underdomäner för att säkerställa att de verifieras och att e-postmeddelandena kan levereras på ett bra sätt och skickas till Gmail-adresserna.

Ytterligare resurser:

* [Självstudievideo om Campaign Standard](https://docs.adobe.com/content/help/en/campaign-standard-learn/tutorials/administrating/control-panel/google-txt-record-management.html)
* [Kampanj - klassisk självstudievideo](https://docs.adobe.com/content/help/en/campaign-classic-learn/tutorials/administrating/control-panel-acc/google-txt-record-management.html)

## Lägga till en Google TXT-post för en underdomän {#adding-a-google-txt-record}

Så här lägger du till en Google TXT-post i din underdomän som används för att skicka Gmail-adresser:

1. Navigate to the **[!UICONTROL Subdomain and Certificates]** card.

1. Markera instansen och öppna sedan informationen om den underdomän som du vill lägga till en DNS-post i.

   ![](assets/txt_subdomaindetails.png)

1. Klicka på **[!UICONTROL Add TXT record]** knappen och ange sedan det värde som genererats i G Suite Admin tools. Mer information finns i [administrationshjälpen](https://support.google.com/a/answer/183895)för G Suite.

   ![](assets/txt_addtxt.png)

1. Bekräfta genom att klicka på **[!UICONTROL Add]** knappen.

   ![](assets/txt_txtadded.png)

När TXT-posten har lagts till måste den verifieras av Google. Det gör du genom att navigera till G Suite Admin-verktygen och sedan starta verifieringssteget (se [administrationshjälpen](https://support.google.com/a/answer/183895)för G Suite).

Om du vill ta bort en post markerar du den i postlistan och klickar sedan på knappen Ta bort.

>[!NOTE]
>
>Den enda post som du kan ta bort från listan över DNS-poster är den som du tidigare har lagt till (i vårt fall Google TXT-posten).
