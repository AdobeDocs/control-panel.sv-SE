---
title: Vanliga frågor om kontrollpanelen
description: Vanliga frågor om kontrollpanelen
translation-type: tm+mt
source-git-commit: 7bde86a86fbd128f4eb7bf029e58b0f95964390b
workflow-type: tm+mt
source-wordcount: '625'
ht-degree: 8%

---


# Vanliga frågor {#faq}

## IMS-organisations-ID {#ims-org-id}

**Vad är ett IMS-organisations-ID?**

Det är ett unikt ID som ges till din instans när du först loggar in på Adobe Experience Cloud. Den ska ha följande format: xxx@AdobeOrg.

Mer information finns i dokumentationen [för](https://marketing.adobe.com/resources/help/en_US/mcloud/organizations.html)Adobe Experience Cloud.

**Var hittar jag mitt IMS-Org-ID?**

Ett sätt är att navigera till [startsidan för Adobe Experience Cloud](https://experiencecloud.adobe.com/) > **[!UICONTROL Administration]**. Du hittar ditt IMS-organisations-ID längst ned i administrationsavsnittet **[!UICONTROL Quick Access]**. Mer detaljerad information finns i dokumentationen för [Adobe Experience Cloud](https://marketing.adobe.com/resources/help/en_US/mcloud/organizations.html).

Det andra sättet är att starta **Admin Console**. Ditt IMS-organisations-ID visas i din URL. Det ska se ut ungefär så här: https://adminconsole.adobe.com/xxx@AdobeOrg/overview.

**Varför behöver jag känna till mitt IMS-Org-ID?**

För att du ska kunna hantera inställningar för din instans måste du se till att du får rätt information för rätt instans om du använder flera instanser för ditt företag.

**Vad händer om jag har flera IMS-organisations-ID:n?**

Du kan ha fler än ett IMS-organisation-ID om du har tillgång till flera Adobe-lösningar. I det här fallet bör du använda rätt IMS-organisations-ID under Adobe Campaign-instansen.

>[!NOTE]
>
>Om du har samma IMS-organisation-ID för Adobe Campaign och Adobe Analytics är detta bra. Att ha ett IMS-organisationsnummer mellan Analytics och Campaign är ett krav om ni tänker integrera lösningarna för att utnyttja komplexa användningsexempel som att kunden överger kundvagnen (för AA + AC).
>
>Om du har olika IMS-organisationsnummer för Adobe Campaign och Adobe Analytics kan du kontakta kundtjänst för att få dem anpassade.

**Hur vet jag att AWS är värd för min Adobe Campaign-instans?**

Följ de här stegen för att kontrollera om din instans finns på AWS:

1. Hämta din inloggnings-URL. Det är den URL du använder för att logga in på Campaign-instansen, som oftast avslutas med &quot;.campaign.adobe.com&quot; eller&quot;.neolane.net&quot;.
1. Öppna terminalen och kör sedan en **[!DNL nslookup]** åtgärd på din inloggnings-URL.

   `doe-macOS% nslookup myinstance.campaign.adobe.com`

1. Svaret returnerar information om din instans.

   ```
   doe-macOS% nslookup myinstance.campaign.adobe.com
   Server:     12.34.5.678
   Address:    12.34.5.678#99
   
   Non-authoritative answer:
   myinstance.campaign.adobe.com
   canonical name = myinstance-mkt-prod1.campaign.adobe.com.
   myinstance-mkt-prod1.campaign.adobe.com
   canonical name = myinstance-mkt-prod1-1.campaign.adobe.com.
   Name: myinstance-mkt-prod1-1.campaign.adobe.com
   Address: 12.34.567.89
   ```

1. Kör en **nslookup** -åtgärd på den returnerade IP-adressen.

   `doe-macOS% nslookup 12.34.567.89`

1. Kontrollera &quot;name&quot;-värdet i det returnerade resultatet. Om den innehåller &quot;amazonaws.com&quot; innebär det att din instans lagras på AWS.

   ```
   doe-macOS% nslookup 12.34.567.89
   Server:     12.34.5.678
   Address:    12.34.5.678#99
   
   Non-authoritative answer:
   89.567.34.12.in-addr.arpa   name = ec2-12-34-567-89.address.amazonaws.com.
   ```

>[!NOTE]
>
>Om du vill migrera till AWS startar du processen genom att kontakta din Customer Success Manager.

## Kontrollpanelen {#control-panel}

**Vad är Kontrollpanelen?**

Kontrollpanelen ger produktadministratörer möjlighet att direkt hantera olika inställningar och övervaka kapaciteten för SFTP-servrar som är anslutna till Adobe Campaign.

**Vilka är de aktuella funktionerna i Kontrollpanelen?**

Med kontrollpanelen kan du spåra lagring, vitlista IP-adresser och hantera SSH-nycklar för dina SFTP-servrar utifrån dina behov och andra åtgärder.

Mer information finns i dokumentationen för åtgärder som stöds på Kontrollpanelen.

**Är Kontrollpanelen endast för Adobe Campaign?**

Ja, du kan bara hantera inställningar för Adobe Campaign på Kontrollpanelen.

**Kan jag använda Kontrollpanelen?**

Kontrollpanelen är bara öppen för produktadministratörer för våra nuvarande kunder som har Adobe Campaign som värd på AWS. Observera att hybridmiljöer ännu inte stöds.

Om du inte är administratör, men vill ha åtkomst, kontaktar du produktadministratören för att få hjälp med att lägga till dig som administratör.

**Hur kommer jag åt Kontrollpanelen?**

Följ de detaljerade instruktionerna i Åtkomst till dokumentationen på Kontrollpanelen.

**Är det en extra avgift att använda Kontrollpanelen?**

Nej, det kostar inget om du är Adobe Campaign-kund.
