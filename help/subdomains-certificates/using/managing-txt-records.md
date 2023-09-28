---
product: campaign
solution: Campaign
title: Lägg till verifieringsposter för Google Site för en underdomän
description: Lär dig hur du lägger till en Google Site Verification-post för en underdomän för domänägarskapsverifiering.
feature: Control Panel
role: Architect
level: Experienced
exl-id: 547ca6f2-720f-4d58-b31b-5b2611ba9156
source-git-commit: 355abf48cce3036d1c3e0f6c5fe3ca8fb63cf645
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 73%

---

# Lägg till verifieringsposter för Google-webbplatser {#adding-a-google-txt-record}

För att säkerställa ett stort antal verkliga e-postmeddelanden och ett lågt antal skräppostmeddelanden kräver vissa tjänster såsom Google att du lägger till en TXT-post i domäninställningarna för att verifiera att du faktiskt äger domänen.

Gmail är för närvarande en av de populäraste e-postadressleverantörerna. För att säkerställa en god levererbarhet och framgångsrik leverans av e-post till Gmail-adresser kan du med Adobe Campaign lägga till särskilda TXT-poster för Googles webbplatsverifiering i underdomänerna för att säkerställa att de verifieras.

Följ dessa steg för att lägga till en Google TXT-post i en underdomän som används för att skicka e-post via Gmail-adresser:

1. Klicka på ellipsknappen bredvid önskad underdomän i listan över underdomäner och välj **[!UICONTROL Subdomain details]**.

1. Klicka på **[!UICONTROL Add TXT record]** knapp och sedan välja **[!UICONTROL Google Site Verification]** från **[!UICONTROL Record Type]** listruta.

1. Ange det värde som genererats i G Suite Admin tools. Se [hjälp för G Suite-administratörer](https://support.google.com/a/answer/183895) för mer information om detta.

   ![](assets/txt_addtxt.png)

1. Bekräfta genom att klicka på knappen **[!UICONTROL Add]**.

   ![](assets/txt_txtadded.png)

När TXT-posten har lagts till måste den verifieras av Google. Navigera till G Suites administratörsverktyg och starta sedan verifieringssteget för att utföra verifieringen (se [hjälp för G Suite-administratörer](https://support.google.com/a/answer/183895)).

För att ta bort en post markerar du den i postlistan och klickar sedan på knappen Ta bort.

>[!NOTE]
>
>Den enda post du kan ta bort från listan över DNS-poster är den som du tidigare har lagt till (i vårt fall Google TXT-posten).

![](assets/do-not-localize/how-to-video.png) Upptäck denna funktion genom video med [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/subdomains-and-certificates/google-txt-record-management.html#subdomains-and-certificates) eller [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/subdomains-and-certificates/google-txt-record-management.html#subdomains-and-certificates)
