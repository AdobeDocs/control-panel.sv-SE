---
title: IP-intervall tillåter listning
description: Lär dig hur du lägger till IP-intervall i tillåtelselista för SFTP-serveråtkomst
translation-type: tm+mt
source-git-commit: d96c044e83d37f020b5fd6ea55199c1223b9fa39
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# IP-intervall tillåter listning {#ip-range-allow-listing}

>[!CONTEXTUALHELP]
>id="cp_ip_whitelist"
>title="Om listning av tillåtna IP-adresser"
>abstract="På den här fliken kan du lägga till IP-intervall till tillåtelselista för att upprätta en anslutning till SFTP-servrarna. Endast SFTP-servrar som du har åtkomst till visas här. Kontakta administratören för att begära åtkomst till andra SFTP-servrar."
>additional-url="https://images-tv.adobe.com/mpcv3/8a977e03-d76c-44d3-853c-95d0b799c870_1560205338.1920x1080at3000_h264.mp4#t=98" text="Se filmen"

SFTP-servrar är skyddade. För att kunna komma åt dem för att kunna visa filer eller skriva nya måste du lägga till den offentliga IP-adressen för det system eller den klient som kommer åt servrarna till tillåtelselista.

## Om CIDR-formatet {#about-cidr-format}

CIDR (Classless Inter-Domain Routing) är det format som stöds när du lägger till IP-intervall med kontrollpanelens gränssnitt.

Syntaxen består av en IP-adress, följt av tecknet &#39;/&#39; och ett decimaltal. Formatet och syntaxen för det finns detaljerad information i [den här artikeln](https://whatismyipaddress.com/cidr).

Du kan söka på Internet efter kostnadsfria onlineverktyg som hjälper dig att konvertera det aktuella IP-intervallet till CIDR-format.

## God praxis {#best-practices}

Se till att du följer rekommendationerna och begränsningarna nedan när du lägger till IP-adresser till tillåtelselista på Kontrollpanelen.

* **Lägg till IP-intervall till tillåtelselista** i stället för till enskilda IP-adresser. Om du vill lägga till en enda IP-adress till tillåtelselista lägger du till en /32 för att ange att intervallet bara innehåller en enda IP-adress.
* **Lägg inte till så breda intervall i tillåtelselista**, t.ex. > 265 IP-adresser. Kontrollpanelen ignorerar alla CIDR-formatintervall som är mellan /0 och /23.
* Endast **offentliga IP-adresser** kan läggas till i tillåtelselista.
* Se till att du **regelbundet tar bort IP-adresser** som du inte längre behöver från tillåtelselista.

## Lägga till IP-adresser i tillåtelselista {#adding-ip-addresses-allow-list}

>[!CONTEXTUALHELP]
>id="cp_sftp_iprange_add"
>title="Lägg till nytt IP-intervall"
>abstract="Definiera de IP-intervall som du vill lägga till i tillåtelselista för att ansluta till SFTP-servrarna."

Så här lägger du till ett IP-intervall till tillåtelselista:

1. Öppna **[!UICONTROL SFTP]**-kortet och välj fliken **[!UICONTROL IP Allow Listing]**.
1. Listan med IP-adresser på tillåtelselista visas för varje instans. Markera önskad instans i den vänstra listan och klicka sedan på **[!UICONTROL Add new IP range]** .

   ![](assets/control_panel_add_range.png)

1. Definiera IP-intervallet som du vill lägga till i tillåtelselista, i CIDR-format, och definiera sedan etiketten som ska visas i listan.

   >[!NOTE]
   >
   >Dessa specialtecken är tillåtna i fältet Etikett:
   > `. _ - : / ( ) # , @ [ ] + = & ; { } ! $`

   ![](assets/control_panel_add_range2.png)

   >[!IMPORTANT]
   >
   >Ett IP-intervall får inte överlappa ett befintligt intervall på tillåtelselista. I så fall tar du först bort det intervall som innehåller den överlappande IP-adressen.
   >
   >Det går att lägga till ett intervall på tillåtelselista för flera instanser. Det gör du genom att trycka på nedpilen eller skriva de första bokstäverna i den önskade instansen och sedan markera den i listan med förslag.

   ![](assets/control_panel_add_range3.png)

1. Klicka på **[!UICONTROL Save]** knappen. IP-tillägg till tillåtelselista kommer att visas som VÄNTANDE tills begäran har behandlats fullständigt. Detta tar bara några sekunder.

Om du vill ta bort IP-intervall från tillåtelselista markerar du dem och klickar sedan på **[!UICONTROL Delete IP range]** .

![](assets/control_panel_delete_range2.png)

>[!NOTE]
>
>Det går för närvarande inte att redigera ett intervall på tillåtelselista. Om du vill ändra ett IP-intervall tar du bort det och skapar sedan ett som passar dina behov.

## Övervaka ändringar {#monitoring-changes}

På kontrollpanelens startsida kan du övervaka alla ändringar som har gjorts i IP-adresser på tillåtelselista. **[!UICONTROL Job Logs]**

Mer information om gränssnittet på Kontrollpanelen finns i [det här avsnittet](../../discover/using/discovering-the-interface.md).

![](assets/control_panel_ip_log.png)
