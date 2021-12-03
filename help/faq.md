---
product: campaign
solution: Campaign
title: Vanliga frågor och svar om Kontrollpanelen
description: Vanliga frågor om Kontrollpanelen
feature: Control Panel
role: Architect
level: Intermediate
exl-id: 4f329764-ed8b-4939-affc-ed994fd6101d
source-git-commit: 47a57b38e9af8b03d277bf9ee6922b19f0298944
workflow-type: ht
source-wordcount: '771'
ht-degree: 100%

---

# Vanliga frågor och svar {#faq}

## Kontrollpanelen {#control-panel}

### Vad är Kontrollpanelen?

Med Kontrollpanelen kan produktadministratörer hantera olika inställningar direkt och övervaka kapaciteten hos SFTP-servrar som är anslutna till Adobe Campaign.

### Vilka funktioner finns på Kontrollpanelen just nu?

Med kontrollpanelen kan du spåra lagring, lägga till IP-adresser i tillåtelselistan och hantera SSH-nycklar för dina SFTP-servrar baserat på dina behov samt andra åtgärder.

Mer information finns i dokumentationen om åtgärder som Kontrollpanelen har stöd för.

### Finns det vissa funktioner som ännu inte stöds i Campaign v8 men som är tillgängliga i Campaign Classic v7?{#v8-restrictions}

Nej. Alla funktioner som är tillgängliga på Campaign Classic v7 stöds nu även via Kontrollpanelen i Campaign v8, inklusive funktioner som rör hantering av underdomäner och certifikat.

### Fungerar Kontrollpanelen bara för Adobe Campaign?

Ja, du kan bara hantera inställningar för Adobe Campaign via Kontrollpanelen.

### Kan jag använda Kontrollpanelen?

Kontrollpanelen kan endast användas av produktadministratörer för våra nuvarande kunder där AWS är värd för Adobe Campaign. Observera att hybridmiljöer ännu inte stöds.

Kontakta produktadministratören om du inte är administratör men vill ha åtkomst. De hjälper dig genom att lägga till dig som administratör.

### Vad krävs för att som Campaign Classic v7-användare få tillgång till Kontrollpanelen? {#v7-restrictions}

Kontrollpanelen är bara tillgänglig för administratörsanvändare. [Läs mer](https://experienceleague.adobe.com/docs/control-panel/using/discover-control-panel/managing-permissions.html?lang=sv#discover-control-panel).

Observera att för Campaign Classic v7 måste din instans ha Amazon Web Services (AWS) som värd och vara uppgraderad till den senaste [Campaign GA](https://experienceleague.adobe.com/docs/campaign-classic/using/release-notes/rn-overview.html?lang=sv#rn-statuses)-versionen. Läs om hur du kontrollerar din version av Campaign Classic i [det här avsnittet](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/starting-with-adobe-campaign/launching-adobe-campaign.html?lang=sv#getting-your-campaign-version). Följ stegen i [det här avsnittet](#hosted-aws) för att kontrollera om din instans av Campaign Classic har AWS som värd.

### Hur kommer jag åt Kontrollpanelen?

Följ de detaljerade instruktionerna i dokumentationen för hur du kommer åt Kontrollpanelen.

### Kostar det mer att använda Kontrollpanelen?

Nej, du kan använda den utan någon extra kostnad om du just nu är Adobe Campaign-kund.

## IMS-organisations-ID {#ims-org-id}

### Vad är ett IMS-organisations-ID?

Det är ett unikt ID som ges till instansen när du först loggar in på Adobe Experience Cloud. Den ska ha följande format: xxx@AdobeOrg.

Se [dokumentationen om Adobe Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=sv) för mer information.

### Var hittar jag mitt IMS-organisations-ID?

Ett sätt är att navigera till [startsidan för Adobe Experience Cloud](https://experiencecloud.adobe.com/) > **[!UICONTROL Administration]**. Du hittar ditt IMS-organisations-ID längst ned i administrationsavsnittet **[!UICONTROL Quick Access]**. Mer detaljerad information finns i dokumentationen för [Adobe Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=sv).

Det andra sättet är att starta **Administratörskonsolen**. Ditt IMS-organisations-ID visas i din URL. Det bör se ut ungefär så här: https://adminconsole.adobe.com/xxx@AdobeOrg/overview.

### Varför behöver jag känna till mitt IMS-organisations-ID?

För att du ska kunna hantera inställningarna för din instans vill vi försäkra oss om att du har rätt information för rätt instans ifall du använder flera instanser för ditt företag.

### Vad händer om jag har flera IMS-organisations-ID:n?

Du kan ha mer än ett IMS-organisation-ID om du har tillgång till flera Adobe-lösningar. I det här fallet bör du använda det IMS-organisations-ID du ser under din instans i Adobe Campaign.

>[!NOTE]
>
>Det är perfekt om du har samma IMS-organisations-ID för Adobe Campaign och Adobe Analytics. Att ha ett IMS-organisations-ID för både Analytics och Campaign är ett krav om du planerar att integrera lösningarna för att utnyttja komplexa användningsområden såsom övergivna kundvagnar (för AA + AC).
>
>Om du har olika IMS-organisations-ID:n för Adobe Campaign och Adobe Analytics ska du kontakta kundtjänst för att få dem korrigerade.

### Hur vet jag att AWS är värd för min Adobe Campaign-instans?{#hosted-aws}

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
