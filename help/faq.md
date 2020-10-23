---
title: Vanliga frågor och svar om Kontrollpanelen
description: Vanliga frågor om Kontrollpanelen
translation-type: ht
source-git-commit: 35723590195ef54df42d1d1df5b37490787f8836
workflow-type: ht
source-wordcount: '629'
ht-degree: 100%

---


# Vanliga frågor och svar {#faq}

## IMS-organisations-ID {#ims-org-id}

**Vad är ett IMS-organisations-ID?**

Det är ett unikt ID som ges till instansen när du först loggar in på Adobe Experience Cloud. Den ska ha följande format: xxx@AdobeOrg.

Se [dokumentationen om Adobe Experience Cloud](https://docs.adobe.com/content/help/sv-SE/core-services/interface/manage-users-and-products/organizations.translate.html) för mer information.

**Var hittar jag mitt IMS-organisations-ID?**

Ett sätt är att navigera till [startsidan för Adobe Experience Cloud](https://experiencecloud.adobe.com/) > **[!UICONTROL Administration]**. Du hittar ditt IMS-organisations-ID längst ned i administrationsavsnittet **[!UICONTROL Quick Access]**. Mer detaljerad information finns i dokumentationen för [Adobe Experience Cloud](https://docs.adobe.com/content/help/sv-SE/core-services/interface/manage-users-and-products/organizations.translate.html).

Det andra sättet är att starta **Administratörskonsolen**. Ditt IMS-organisations-ID visas i din URL. Det bör se ut ungefär så här: https://adminconsole.adobe.com/xxx@AdobeOrg/overview.

**Varför behöver jag känna till mitt IMS-organisations-ID?**

För att du ska kunna hantera instansinställningar måste du se till att ha rätt information för rätt instans om du använder flera instanser för ditt företag.

**Vad händer om jag har flera IMS-organisations-ID:n?**

Du kan ha mer än ett IMS-organisation-ID om du har tillgång till flera Adobe-lösningar. I det här fallet bör du använda det IMS-organisations-ID du ser under din instans i Adobe Campaign.

>[!NOTE]
>
>Det är perfekt om du har samma IMS-organisations-ID för Adobe Campaign och Adobe Analytics. Att ha ett IMS-organisations-ID för både Analytics och Campaign är ett krav om du planerar att integrera lösningarna för att utnyttja komplexa användningsområden såsom övergivna kundvagnar (för AA + AC).
>
>Om du har olika IMS-organisations-ID:n för Adobe Campaign och Adobe Analytics ska du kontakta kundtjänst för att få dem korrigerade.

**Hur vet jag att AWS är värd för min instans i Adobe Campaign?**

Följ dessa steg för att kontrollera om AWS är värd för din instans:

1. Hämta din inloggnings-URL. Det är den URL du använder för att logga in på instansen i Campaign och som oftast avslutas med ”.campaign.adobe.com” eller ”.neolane.net”.
1. Öppna terminalen och kör sedan en **[!DNL nslookup]**-åtgärd på din inloggnings-URL.

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

1. Kör en **nslookup**-åtgärd på den returnerade IP-adressen.

   `doe-macOS% nslookup 12.34.567.89`

1. Kontrollera värdet på namnet i det returnerade resultatet. Om det innehåller ”amazonaws.com” innebär det att AWS är värd för din instans.

   ```
   doe-macOS% nslookup 12.34.567.89
   Server:     12.34.5.678
   Address:    12.34.5.678#99
   
   Non-authoritative answer:
   89.567.34.12.in-addr.arpa   name = ec2-12-34-567-89.address.amazonaws.com.
   ```

>[!NOTE]
>
>Kontakta din Customer Success Manager för att starta processen att migrera till AWS.

## Kontrollpanelen {#control-panel}

**Vad är Kontrollpanelen?**

Kontrollpanelen ger produktadministratörer möjligheten att direkt hantera olika inställningar och övervaka kapaciteten hos SFTP-servrar som är anslutna till Adobe Campaign.

**Vilka är de aktuella funktionerna i Kontrollpanelen?**

Med kontrollpanelen kan du spåra lagring, lägga till IP-adresser i tillåtelselistan och hantera SSH-nycklar för dina SFTP-servrar baserat på dina behov samt andra åtgärder.

Mer information finns i dokumentationen om åtgärder som Kontrollpanelen har stöd för.

**Är Kontrollpanelen endast för Adobe Campaign?**

Ja, du kan endast hantera inställningarna för Adobe Campaign via Kontrollpanelen.

**Kan jag använda Kontrollpanelen?**

Kontrollpanelen kan endast användas av produktadministratörer för våra nuvarande kunder där AWS är värd för Adobe Campaign. Observera att hybridmiljöer ännu inte stöds.

Kontakta produktadministratören om du inte är administratör men vill ha åtkomst. De hjälper dig genom att lägga till dig som administratör.

**Hur får jag åtkomst till Kontrollpanelen?**

Följ de detaljerade instruktionerna i dokumentationen om åtkomst till Kontrollpanelen.

**Finns det en extra avgift för att använda Kontrollpanelen?**

Du kan använda den utan extra kostnad om du för närvarande är kund hos Adobe Campaign.
