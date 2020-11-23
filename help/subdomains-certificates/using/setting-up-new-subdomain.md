---
product: campaign
solution: Campaign
title: Konfigurera en ny underdomän
description: Läs om hur man skapar en ny underdomän för instanser i Campaign
translation-type: tm+mt
source-git-commit: 317b4c1cee34667a36f5e1a1197649bfd69c151a
workflow-type: tm+mt
source-wordcount: '1140'
ht-degree: 47%

---


# Konfigurera en ny underdomän {#setting-up-subdomain}

>[!CONTEXTUALHELP]
>id="cp_subdomain_management"
>title="Konfigurera nya underdomäner och hantera certifikat"
>abstract="Du måste konfigurera en ny underdomän och hantera dina underdomäners SSL-certifikat för att kunna börja skicka e-postmeddelanden eller publicera landningssidor med Adobe Campaign."
>additional-url="https://docs.adobe.com/content/help/sv-SE/control-panel/using/subdomains-and-certificates/monitoring-ssl-certificates.html" text="Så övervakar du dina underdomäners SSL-certifikat"

>[!IMPORTANT]
>
>Underdomänskonfigurationen från Kontrollpanelen är tillgänglig som betaversion och kan uppdateras ofta och ändras utan föregående meddelande.

Den här sidan innehåller information om hur du konfigurerar nya underdomäner med fullständig underdomändelegering eller CNAME. Globala koncept för dessa två metoder beskrivs i detta avsnitt: [Märke](../../subdomains-certificates/using/subdomains-branding.md)för underdomäner.

**Relaterat ämne:**

* [Övervaka underdomänerna](../../subdomains-certificates/using/monitoring-subdomains.md)

## Måste läsas {#must-read}

### Val av instans

Subdomain configuration is available for **production** instances only.

Om instansen som du väljer i guiden inte har några tidigare konfigurerade underdomäner, kommer den första konfigurerade underdomänen att bli den **primära underdomänen** för den instansen och du kommer inte att kunna ändra den i framtiden.

Därför kommer **omvända DNS-poster** att skapas för andra underdomäner som använder den här primära underdomänen. **Svars- och returadresser för andra underdomäner genereras från den primära underdomänen.**

### Konfiguration av namnservrar

Se till att du **aldrig delegerar din rotunderdomän till Adobe** när du konfigurerar namnservrar. Om du gör detta fungera domänen endast med Adobe. Att använda den på annat sätt – såsom att skicka interna e-postmeddelanden till företagets anställda – blir omöjligt.

Skapa **inte heller någon separat zonfil** för den nya underdomänen.

## Fullständig delegering av underdomäner {#full-subdomain-delegation}

Följ stegen nedan om du vill delegera en underdomän till Adobe Campaign helt.

![](assets/do-not-localize/how-to-video.png) Upptäck den här funktionen i video med [Campaign Classic](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/subdomains-and-certificates/subdomain-delegation.html?lang=en#subdomains-and-certificates) eller [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/subdomains-and-certificates/subdomain-delegation.html?lang=en#subdomains-and-certificates)

1. Välj önskad produktionsinstans på **[!UICONTROL Subdomains & Certificates]**-kortet och klicka sedan på **[!UICONTROL Setup new subdomain]**.

   ![](assets/subdomain1.png)

1. Klicka på **[!UICONTROL Next]** för att bekräfta den fullständiga delegeringsmetoden.

   ![](assets/subdomain3.png)

1. Skapa den önskade underdomänen och namnservrar i värdlösningen som används av organisationen. Gör detta genom att kopiera och klistra in Adobe Nameserver-informationen som visas i guiden. Se [videon med självstudiekurser](https://video.tv.adobe.com/v/30175?captions=swe) för mer information om hur du skapar en underdomän i en värdlösning.

   ![](assets/subdomain4.png)

1. Skapa underdomänen med motsvarande Adobe Nameserver-information och klicka sedan på **[!UICONTROL Next]**.

1. Om du har valt en Campaign Classic-instans väljer du önskat användningsfall för underdomänen: **Marknadsföringskommunikation** eller **Transactional &amp; Operational Communications**. Globala koncept för underdomäners användning presenteras i [det här avsnittet](../../subdomains-certificates/using/subdomains-branding.md#about-subdomains-use-cases).

   ![](assets/subdomain5.png)

1. Öppna den underdomän du skapade i din värdlösning och klicka sedan på **[!UICONTROL Submit]**.

   Se till att du anger det **fullständiga namnet** på den underdomän som ska delegeras. Om du till exempel vill delegera underdomänen ”usoffers.email.weretail.com” ska du skriva ”usoffers.email.weretail.com”.

   ![](assets/subdomain6.png)

När underdomänen har skickats utförs olika kontroller och konfigurationssteg av Kontrollpanelen. Mer information finns i [Underdomänskontroller och konfiguration](#subdomain-checks-and-configuration).

## Konfiguration av underdomäner med CNAME:er {#use-cnames}

Följ stegen nedan för att konfigurera en underdomän med CNAME.

![](assets/do-not-localize/how-to-video.png) Upptäck den här funktionen i video med [Campaign Classic](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/subdomains-and-certificates/delegating-subdomains-using-cname.html?lang=en#subdomains-and-certificates) eller [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/subdomains-and-certificates/delegating-subdomains-using-cname.html?lang=en)

1. Välj önskad produktionsinstans på **[!UICONTROL Subdomains & Certificates]**-kortet och klicka sedan på **[!UICONTROL Setup new subdomain]**.

   ![](assets/subdomain1.png)

1. Select the **[!UICONTROL CNAME]** method, then click **[!UICONTROL Next]**.

   ![](assets/cname-method-selection.png)

1. Om du har valt en Campaign Classic-instans väljer du önskat användningsfall för underdomänen: **Marknadsföringskommunikation** eller **Transactional &amp; Operational Communications**. Globala koncept för underdomäners användning presenteras i [det här avsnittet](../../subdomains-certificates/using/subdomains-branding.md#about-subdomains-use-cases).

   ![](assets/cname-use-case.png)

1. Öppna den underdomän du skapade i din värdlösning och klicka sedan på **[!UICONTROL Next]**.

   Make sure you fill in the **full name** of the subdomain to setup. Om du till exempel vill konfigurera underdomänen &quot;usoffers.email.weretail.com&quot; skriver du &quot;usoffers.email.weretail.com&quot;.

   ![](assets/cname-submit.png)

1. Listan med poster som ska placeras på dina DNS-servrar visas. Kopiera dessa poster, antingen en efter en, eller genom att hämta en CSV-fil, och navigera sedan till din värdlösning för domänen för att generera matchande DNS-poster.

   ![](assets/cname-generate-record.png)

1. Se till att alla DNS-poster från tidigare steg har genererats i domänens värdlösning. Om allt är korrekt konfigurerat markerar du den första satsen och klickar sedan på **[!UICONTROL Submit]** för att bekräfta.

   ![](assets/cname-confirmation.png)

   >[!NOTE]
   >
   >Om du vill skapa posterna och skicka konfigurationen för underdomänen senare, väljer du den andra satsen och klickar sedan på **[!UICONTROL Submit later]**. Du kan sedan återuppta konfigurationen av underdomänen direkt från **[!UICONTROL Processing]** underdomänshanteringen.
   >
   >Observera att DNS-poster som ska placeras på servern kommer att behållas av Kontrollpanelen i 30 dagar. Efter den perioden måste du konfigurera underdomänen från grunden.

När underdomänen har skickats utförs olika kontroller och konfigurationssteg av Kontrollpanelen. Mer information finns i [Underdomänskontroller och konfiguration](#subdomain-checks-and-configuration).

## Underdomänskontroller och konfiguration {#subdomain-checks-and-configuration}

1. När en underdomän har skickats kontrollerar kontrollpanelen att den pekar korrekt på Adobe NS-poster och att posten Start of Authority (SOA) inte finns för den här underdomänen.

   >[!NOTE]
   >
   >Observera att medan konfigurationen av underdomäner körs, kommer andra förfrågningar via Kontrollpanelen att ställas i kö och utföras först när konfigurationen av underdomänen har slutförts, för att undvika prestandaproblem.

1. Om kontrollerna är godkända börjar Kontrollpanelen konfigurera underdomänen med DNS-poster, ytterligare URL:er och inkorgar osv.

   ![](assets/subdomain7.png)

   You can get more details on the configuration progress by clicking the subdomain configuration **[!UICONTROL Details]** button.

   ![](assets/subdomain_audit.png)

1. Slutligen kommer **Levererbarhetsteamet** att meddelas om den nya underdomänen för att kunna granska den. Granskningsprocessen kan ta upp till 10 arbetsdagar efter att underdomänen har konfigurerats.

   >[!IMPORTANT]
   >
   >Leveranskontrollerna som utförs omfattar feedbackslingor och slingtest av skräppostklagomål. Vi rekommenderar därför inte att du använder underdomänen innan granskningen har slutförts eftersom det kan leda till ett dåligt rykte för underdomänen.

1. Vid slutet av processen konfigureras underdomänerna så att de fungerar med instansen i Adobe Campaign och elementen nedan skapas:

   * **Underdomänen med följande DNS-poster**: SOA, MX, CNAME(:er), DKIM, SPF, TXT.
   * **Ytterligare underdomäner** för värdspegling, resurser, spårningssidor och domännycklar.
   * **Inkorgar**: avsändare, fel, svara till.

   Som standard är inkorgen ”Svara till” på Kontrollpanelen konfigurerad till att rensa e-postmeddelanden och kan inte granskas. Använd en annan adress om du vill övervaka din ”Svara till”-inkorg för marknadsföringskampanjerna.

Du får mer information om underdomänen genom att klicka på knapparna **[!UICONTROL Subdomain details]** och **[!UICONTROL Sender info]**.

![](assets/detail_buttons.png)

![](assets/subdomain_details.png)

![](assets/sender_info.png)

## Felsökning {#troubleshooting}

* I vissa fall går subdomänkonfigurationen igenom, men det är inte säkert att underdomänen kan verifieras korrekt. Underdomänen blir kvar i **[!UICONTROL Configured]**-listan med en jobblogg med information om felet. Kontakta kundtjänsten om du behöver hjälp med att lösa problemet.
* Starta en ny verifiering av underdomäner (**…**/**[!UICONTROL Verify subdomain]**) om underdomänen visas som ”Ej verifierad” efter att den har konfigurerats. Om den fortfarande har samma status kan det bero på att det anpassningar utförs i mottagarschemat som inte kan verifieras med standardprocesser. Försök skicka en kampanj med den underdomänen.
* Om konfigurationen av underdomänen vid granskning av leveransen tar för lång tid (mer än tio arbetsdagar) ska du kontakta Kundtjänst.
