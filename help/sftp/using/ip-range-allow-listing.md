---
product: campaign
solution: Campaign
title: Tillåtelselista med IP-intervall
description: Läs om hur man lägger till IP-intervall i tillåtelselistan för SFTP-serveråtkomst
feature: Control Panel, SFTP Management
role: Admin
level: Experienced
exl-id: 45a3bfcd-500c-4139-b610-d39989260ab7
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '1027'
ht-degree: 35%

---

# Tillåtelselista för IP-intervall {#ip-range-allow-listing}

>[!CONTEXTUALHELP]
>id="cp_ip_whitelist"
>title="Om att tillåtelselista med IP-adresser"
>abstract="På den här fliken kan du lägga till IP-intervall till tillåtelselistan för att upprätta en anslutning till SFTP-servrarna. Endast SFTP-servrar som du har åtkomst till visas här. Kontakta din administratör för att begära åtkomst till andra SFTP-servrar."
>additional-url="https://images-tv.adobe.com/mpcv3/8a977e03-d76c-44d3-853c-95d0b799c870_1560205338.1920x1080at3000_h264.mp4#t=98" text="Se demovideon"

SFTP-servrar är skyddade. För att kunna komma åt dem för att visa filer eller skriva nya måste du lägga till den offentliga IP-adressen för det system eller den klient som kommer åt servrarna till tillåtelselista.

![](assets/do-not-localize/how-to-video.png) Upptäck denna funktion genom video med [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/sftp-management/adding-ip-range-to-allow-list.html?lang=sv-SE#sftp-management) eller [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/sftp-management/adding-ip-range-to-allow-list.html?lang=sv-SE#sftp-management)

## Om CIDR-formatet {#about-cidr-format}

CIDR (Classless Inter-Domain Routing) är det format som stöds när ett IP-intervall läggs till via Kontrollpanelens gränssnitt.

Syntaxen består av en IP-adress följt av tecknet / och ett decimaltal. Formatet och syntaxen för det finns detaljerad information i [den här artikeln](https://whatismyipaddress.com/cidr){target="_blank"}.

Du kan söka på Internet efter kostnadsfria onlineverktyg som hjälper dig att konvertera det aktuella IP-intervallet till CIDR-format.

## Bästa praxis {#best-practices}

Se till att du följer rekommendationerna och begränsningarna nedan när du lägger till IP-adresser i tillåtelselistan i Kontrollpanelen.

* **Lägg till IP-intervall i tillåtelselistan** i stället för enskilda IP-adresser. För att lägga till en enda IP-adress till tillåtelselista ska du lägga till /32 för att ange att intervallet bara innehåller en enda IP-adress.
* **Lägg inte till väldigt stora intervall i tillåtelselistan** såsom > 265 IP-adresser. Kontrollpanelen avvisar alla CIDR-formatintervall som är mellan /0 och /23.
* Endast **offentliga IP-adresser** kan läggas till i tillåtelselistan.
* **Ta regelbundet bort IP-adresser** som du inte längre behöver från tillåtelselista.

## Lägga till IP-adresser i tillåtelselista {#adding-ip-addresses-allow-list}

>[!CONTEXTUALHELP]
>id="cp_sftp_iprange_add"
>title="IP-intervallkonfiguration"
>abstract="Definiera de IP-intervall som du vill lägga till i tillåtelselistan för att ansluta till dina SFTP-serverar."

Följ dessa steg för att lägga till ett IP-intervall i tillåtelselistan:

1. Öppna **[!UICONTROL SFTP]**-kortet och välj fliken **[!UICONTROL IP Allow Listing]**.
1. Listan med IP-adresser i tillåtelselistan visas för varje instans. Välj önskad instans i den vänstra listan och klicka sedan på **[!UICONTROL Add new IP range]**.

   ![](assets/control_panel_add_range.png)

1. Definiera IP-intervallet som du vill lägga till i tillåtelselista. Det här fältet accepterar endast IP-intervall i CIDR-format, till exempel *192.150.5.0/24*.

   ![](assets/control_panel_add_range4.png)

   >[!IMPORTANT]
   >
   >Ett IP-intervall får inte överlappa ett befintligt intervall på tillåtelselistan. I detta fall måste du först ta bort det intervall som innehåller den överlappande IP-adressen.

1. Det går att lägga till ett intervall i tillåtelselista för flera instanser. Gör detta genom att trycka på nedpilen eller ange de första bokstäverna i den önskade instansen och sedan markera den i listan över förslag.

   ![](assets/control_panel_add_range3.png)

1. Definiera etiketten som ska visas för det här IP-intervallet i listan.

   ![](assets/control_panel_add_range2.png)

   >[!NOTE]
   >
   >Följande specialtecken är tillåtna i fältet **[!UICONTROL Label]**:
   > `. _ - : / ( ) # , @ [ ] + = & ; { } ! $`

1. Om du vill hantera IP-tillåtelselista bättre kan du ange en längd för tillgängligheten för varje IP-intervall. Om du vill göra det väljer du en enhet i listrutan **[!UICONTROL Type]** och definierar en varaktighet i motsvarande fält. Mer information om IP-intervallets förfallodatum finns i [det här avsnittet](#expiry).

   ![](assets/control_panel_add_range5.png)

   >[!NOTE]
   >
   >Som standard är fältet **[!UICONTROL Type]** inställt på **[!UICONTROL Unlimited]**, vilket innebär att IP-intervallet aldrig upphör att gälla.

1. I fältet **[!UICONTROL Comment]** kan du ange en orsak till att det här IP-intervallet tillåts (varför, för vem, osv.).

1. Klicka på knappen **[!UICONTROL Save]**. IP-intervallet som läggs till tillåtelselista visas som **[!UICONTROL Pending]** tills begäran har bearbetats helt, vilket bara tar några sekunder.

   ![](assets/control_panel_add_range6.png)

>[!IMPORTANT]
>
>Om du försöker ansluta dina SFTP-servrar till ett nytt system, och därmed lägger till nya IP-intervall till tillåtelselista, kan du behöva ange nya offentliga nycklar för att slutföra anslutningen. Mer information finns i [det här avsnittet](key-management.md).

## Hantera IP-intervall {#managing-ip-ranges}

IP-intervallen som du skapar visas på fliken **[!UICONTROL IP Allow Listing]**.

Du kan sortera objekten baserat på skapandedatum eller utgåvedatum, på den användare som skapade eller redigerade dem och på IP-intervallets förfallodatum.

Du kan också söka efter ett IP-intervall genom att börja skriva en etikett, ett intervall, ett namn eller en kommentar.

![](assets/control_panel_allow_list_sort.png)

Mer information om hur du redigerar ett eller flera IP-intervall finns i [det här avsnittet](#editing-ip-ranges).

Om du vill ta bort ett eller flera IP-intervall från tillåtelselista markerar du dem och klickar sedan på knappen **[!UICONTROL Delete IP range]**.

![](assets/control_panel_delete_range.png)

### Förfaller {#expiry}

Kolumnen **[!UICONTROL Expires]** visar hur många dagar som återstår tills IP-intervallet upphör att gälla.

Om du prenumererar på [e-postavisering](../../performance-monitoring/using/email-alerting.md) får du meddelanden via e-post 10 dagar och 5 dagar innan ett IP-intervall upphör att gälla och den dag det ska gå ut. När du får aviseringen kan du [redigera IP-intervallet](#editing-ip-ranges) och vid behov förlänga dess giltighetsperiod.

Ett IP-intervall som har gått ut tas bort automatiskt efter 7 dagar. Det visas som **[!UICONTROL Expired]** i kolumnen **[!UICONTROL Expires]**. Inom denna 7-dagarsperiod:

* Ett IP-intervall som har gått ut kan inte längre användas för att komma åt SFTP-servrarna.

* Du kan inte skapa ett annat IP-intervall som överlappar ett intervall som har gått ut. Du måste först ta bort det utgångna IP-intervallet innan du skapar det nya.

* Du kan [redigera](#editing-ip-ranges) ett IP-intervall som har gått ut och uppdatera dess varaktighet så att det blir tillgängligt igen.

* Du kan ta bort den från tillåtelselista.

## Redigera IP-intervall {#editing-ip-ranges}

>[!CONTEXTUALHELP]
>id="cp_sftp_iprange_update"
>title="Uppdatera IP-intervall"
>abstract="Uppdatera de valda IP-intervallen som tillåts ansluta till SFTP-servern."

Följ stegen nedan om du vill redigera IP-intervall.

>[!NOTE]
>
>Du kan bara redigera IP-intervall som har skapats sedan Kontrollpanelen i oktober 2021-versionen.

<!--Edition is not available for IP ranges that have been created before the Control Panel October 2021 release.-->

1. Välj ett eller flera IP-intervall i listan **[!UICONTROL IP Allow Listing]**.

1. Klicka på knappen **[!UICONTROL Update IP range]**.

   ![](assets/control_panel_edit_range.png)

1. Du kan bara redigera IP-intervallets förfallodatum och/eller lägga till en ny kommentar.

   >[!NOTE]
   >
   >Om du vill ändra CIDR-formatet, dess etikett eller redigera de relaterade instanserna måste du först ta bort IP-intervallet och skapa ett nytt som passar dina behov.

   ![](assets/control_panel_edit_range2.png)

1. Spara ändringarna.

## Övervaka ändringar {#monitoring-changes}

Med **[!UICONTROL Job Logs]** på kontrollpanelens startsida kan du spåra och övervaka alla ändringar som har gjorts i IP-adresser på tillåtelselista.

Se [det här avsnittet](../../discover/using/discovering-the-interface.md) för mer information om kontrollpanelens gränssnitt.

![](assets/control_panel_ip_log.png)
