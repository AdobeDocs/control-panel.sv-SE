---
product: campaign
solution: Campaign
title: Förnya en underdomäns SSL-certifikat
description: Läs om hur man förnyar underdomäners SSL-certifikat
feature: Control Panel, Subdomains and Certificates
role: Admin
level: Experienced
exl-id: e9b7c67d-6afa-44f9-b19d-39c0ec9a7edd
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '993'
ht-degree: 100%

---

# Förnya SSL-certifikat {#renewing-subdomains-ssl-certificates}

>[!CONTEXTUALHELP]
>id="cp_add_ssl_certificate"
>title="Förnyelse av SSL-certifikat"
>abstract="För att förnya ett SSL-certifikat måste du generera en CSR, köpa SSL-certifikatet för dina underdomäner och installera certifikatpaketet. Den här åtgärden krävs bara om du väljer att hantera certifikat manuellt i stället för att delegera det till Adobe. "

>[!NOTE]
>
>Du behöver bara förnya SSL-certifikaten för dina underdomäner om du väljer att hantera certifikat själv i stället för att delegera processen till Adobe. Vi rekommenderar att du delegerar hanteringen av dina underdomäners SSL-certifikat till Adobe, eftersom Adobe automatiskt skapar certifikatet och förnyar det varje år innan det upphör att gälla. [Läs mer om hantering av SSL-certifikat](monitoring-ssl-certificates.md#management)

Processen gällande förnyelse av SSL-certifikat omfattar tre steg:

1. **Generering av CSR (Certificate Signing Request)**

   Begäran om certifikatsignering måste genereras för den instans och de underdomäner som du planerar att skydda innan du köper ett certifikat.  Du måste ange viss information som krävs för att generera en Begäran om certifikatsignering (såsom ett nätverksnamn, organisationsnamn och adress osv.). [Läs mer](#generate)

1. **Köp av SSL-certifikatet**

   När CSR har skapats kan du använda den för att köpa SSL-certifikatet från den certifikatutfärdare som ditt företag godkänner.

1. **Installation av SSL-certifikatet**

   Installera det köpta SSL-certifikatet på den önskade underdomänen för att skydda den. [Läs mer](#install)

![](assets/do-not-localize/how-to-video.png) Upptäck denna funktion genom video med [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/subdomains-and-certificates/adding-ssl-certificates.html?lang=sv#subdomains-and-certificates) eller [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/subdomains-and-certificates/adding-ssl-certificates.html?lang=sv#adding-ssl-certificates)

**Relaterade ämnen:**

* [Guide för bästa praxis vid leverans – SSL-certifikatbegäran för Adobe Campaign](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/campaign/ac-ssl-certificate-request.html?lang=sv)
* [Märka underdomäner](../../subdomains-certificates/using/subdomains-branding.md)
* [Övervaka underdomäner](../../subdomains-certificates/using/monitoring-subdomains.md)

## Generera CSR {#generate}

>[!CONTEXTUALHELP]
>id="cp_generate_csr"
>title="CSR-generering"
>abstract="Begäran om certifikatsignering måste genereras för den instans och de underdomäner som du planerar att skydda innan du köper ett certifikat."

>[!CONTEXTUALHELP]
>id="cp_select_subdomains"
>title="Välj underdomänerna för din begäran om certifikatsignering"
>abstract="Du kan välja att inkludera alla eller endast vissa underdomäner i din begäran om certifikatsignering. Endast valda underdomäner certifieras via inköpt SSL-certifikat."

Följ dessa steg för att skapa en begäran om certifikatsignering:

1. Markera den önskade instansen på **[!UICONTROL Subdomains & Certificates]**-kortet och klicka sedan på knappen **[!UICONTROL Manage Certificate]**.

   ![](assets/renewal1.png)

1. Välj **[!UICONTROL 1 - Generate a CSR]** och klicka sedan på **[!UICONTROL Next]** för att starta guiden som leder dig genom genereringsprocessen till din begäran om certifikatsignering.

   ![](assets/renewal2.png)

1. Ett formulär visas med all information som krävs för att generera din begäran om certifikatsignering.

   Se till att du fyller i den begärda informationen på ett fullständigt och korrekt sätt. I annat fall kanske inte certifikatet förnyas (kontakta vid behov ditt interna team samt säkerhets- och IT-team). Klicka sedan på **[!UICONTROL Next]**.

   * **[!UICONTROL Organization]**: officiellt organisationsnamn.
   * **[!UICONTROL Organization Unit]**: enhet som är länkad till underdomänen (exempel: marknadsföring och IT).
   * **[!UICONTROL Instance]** (förfylld): URL till Campaign-instansen som är associerad med underdomänen.
   * **[!UICONTROL Common name]**: det vanliga namnet är markerat som standard, du kan välja en av underdomänerna om det behövs.

   ![](assets/renewal3.png)

1. Välj underdomäner som ska ingå i din begäran om certifikatsignering och klicka sedan på **[!UICONTROL OK]**.

   ![](assets/renewal4.png)

1. De valda underdomänerna visas i listan. För var och en av dem ska du välja de underdomäner som ska inkluderas och sedan klicka på **[!UICONTROL Next]**.

   ![](assets/renewal5.png)

1. En sammanfattning av de underdomäner som ska inkluderas i din begäran om certifikatsignering visas. Klicka på **[!UICONTROL Submit]** för att bekräfta din begäran.

   ![](assets/renewal6.png)

   >[!NOTE]
   >
   >Med knappen **[!UICONTROL Copy CSR content]** kan du kopiera all information som rör CSR (organisations-ID, instans, organisationsnamn, eget namn, inkluderade underdomäner osv.)

1. Filen med filnamnstillägget .csr som motsvarar ditt val genereras och hämtas automatiskt. Du kan nu använda den för att köpa SSL-certifikatet från den certifikatutfärdare som ditt företag har godkänt. Om du behöver hämta CSR igen följer du stegen som beskrivs i [det här avsnittet](#download).

När CSR har skapats och hämtats kan du använda den för att köpa ett SSL-certifikat från en certifikatutfärdare som har godkänts av organisationen.

När SSL-certifikatet har köpts kan du installera det på din instans för att skydda din underdomän. [Läs mer](#install)

## Hämta CSR {#download}

För att kunna köpa ett SSL-certifikat måste du först hämta begäran om certifikatsignering. CSR hämtas automatiskt när den har skapats. Du kan också hämta den igen när som helst från jobbloggarna:

1. I **[!UICONTROL Job Logs]** väljer du fliken **[!UICONTROL Finished]** och filtrerar sedan listan för att visa jobb som är relaterade till hantering av underdomäner.

   ![](assets/renewal-download.png)

1. Öppna jobbet som motsvarar CSR-genereringen och klicka sedan på länken **[!UICONTROL Downbload]** för att hämta csr-filen.

   ![](assets/renewal-download-button.png)

## Installera SSL-certifikatet {#install}

>[!CONTEXTUALHELP]
>id="cp_install_ssl_certificate"
>title="Installation av SSL-certifikat"
>abstract="Installera SSL-certifikatet som du har köpt från den certifikatutfärdare som har godkänts av din organisation."

När ett SSL-certifikat har köpts kan du installera det på din instans. Innan du fortsätter ska du se till att du är medveten om förutsättningarna nedan:

* Din begäran om certifikatsignering måste ha genererats från Kontrollpanelen. I annat fall kan du inte installera certifikatet från Kontrollpanelen.
* Din begäran om certifikatsignering (CSR) bör matcha underdomänen som har konfigurerats för att fungera med Adobe. Den kan till exempel inte innehålla fler underdomäner än den som har konfigurerats.
* Certifikatet ska ha dagens datum. Det går inte att installera certifikat med datum i framtiden och de får inte ha förfallit (dvs. giltiga start- och slutdatum).
* Certifikatet måste utfärdas av en betrodd certifikatutfärdare (CA) såsom Comodo, DigiCert eller GoDaddy osv.
* Certifikatets storlek ska vara 2 048 bitar och algoritmen RSA.
* Certifikatet ska vara i formatet X.509 PEM.
* SAN-certifikat stöds.
* Wildcard-certifikat stöds inte.
* ZIP-filen eller certifikatet får inte vara lösenordsskyddade.
* ZIP-filen ska endast innehålla följande och helst i enskilda filer:
   * Slutenhetscertifikat.
   * Mellanliggande certifikatkedja (i rätt ordning).
   * Rotcertifikat (valfritt).

Följ dessa steg för att installera certifikatet:

1. Markera den önskade instansen på **[!UICONTROL Subdomains & Certificates]**-kortet och klicka sedan på knappen **[!UICONTROL Manage Certificate]**.

   ![](assets/renewal1.png)

1. Välj **[!UICONTROL 3 - Install Certificate Bundle]** och klicka sedan på **[!UICONTROL Next]** för att starta guiden som leder dig genom certifikatets installationsprocess.

   ![](assets/install1.png)

1. Välj .zip-filen som innehåller det certifikat som ska installeras och klicka sedan på **[!UICONTROL Submit]**.

   ![](assets/install2.png)

>[!NOTE]
>
>Certifikatet installeras på alla domäner/underdomäner som ingår i din begäran om certifikatsignering. Eventuella ytterligare domäner/underdomäner i certifikatet beaktas inte.

När SSL-certifikatet har installerats uppdateras certifikatets giltighetsdatum och statusikon i enlighet med detta.
