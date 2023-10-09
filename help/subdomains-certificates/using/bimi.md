---
product: campaign
solution: Campaign
title: Lägg till BIMI-poster
description: Läs mer om hur du lägger till en BIMI-post för en underdomän.
feature: Control Panel
role: Architect
level: Experienced
exl-id: eb7863fb-6e6d-4821-a156-03fee03cdd0e
source-git-commit: 64ea5e26786eea107983ee5025025c81334b0a91
workflow-type: ht
source-wordcount: '494'
ht-degree: 100%

---

# Lägg till BIMI-poster {#dmarc}

## Om BIMI-poster {#about}

Brand Indicators for Message Identification (BIMI) är en branschstandard som gör att en godkänd logotyp kan visas bredvid en avsändares e-postadress i e-postleverantörens inkorgar för att förbättra varumärkesigenkänning och -förtroende. Det förebygger e-postförfalskning och nätfiske genom att verifiera avsändarens identitet via DMARC-autentisering, vilket gör det svårare för oseriösa aktörer att personifiera giltiga varumärken i e-postmeddelanden.

Detaljerad information om BIMI-implementering finns i [Användarhandbok om bästa levererbarhetspraxis i Adobe](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-bimi.html?lang=sv)

![](assets/bimi-example.png){width="70%" align="center"}

## Begränsningar och förhandskrav {#limitations}

* SPF-, DKIM- och DMARC-poster är nödvändiga för att du ska kunna skapa en BIMI-post.
* BIMI-poster kan bara läggas till för underdomäner med fullständig underdomändelegering. [Läs mer om konfigurationsmetoder för underdomäner](subdomains-branding.md#subdomain-delegation-methods)
* Förhandskrav för DMARC-poster:

   * Postprinciptypen för underdomänen måste anges som antingen Karantän eller Avvisa. Det går inte att skapa BIMI-poster med DMARC-principtypen inställd på Ingen.
   * Procentandelen e-postmeddelanden som DMARC-principen tillämpas på måste vara 100 %. BIMI stöder inte DMARC-principer där procentandelen är mindre än 100 %.

[Läs mer om att konfigurera DMARC-poster](dmarc.md)

## Lägg till en BIMI-post för en underdomän {#add}

Följ de här stegen för att lägga till en BIMI-post för en underdomän:

1. Klicka på ellipsknappen bredvid önskad underdomän i listan över underdomäner och välj **[!UICONTROL Subdomain details]**.

1. Klicka på knappen **[!UICONTROL Add TXT record]** och välj sedan **[!UICONTROL BIMI]** från rullgardinsmenyn **[!UICONTROL Record type]**.

   ![](assets/bimi-add.png)

1. I **[!UICONTROL Company Logo URL]** anger du URL-adressen till den SVG-fil som innehåller logotypen.

1. Även om **[!UICONTROL Certificate URL]** är valfritt behövs den för vissa e-postleverantörer som Gmail och Apple som täcker 80 % av e-postmarknaden. Därför rekommenderar vi att du skaffar ett Verified Mark Certificate (VMC) för att verkligen utnyttja BIMI.

   +++Hur skaffar jag ett VMC?

   De viktigaste stegen för att hämta ett VMC är följande:

   1. Registrera din logotyp som ett varumärke på ett immaterialrättskontor som godkänts av VMC-utfärdare. Om du har ett juridiskt team rekommenderar vi att du arbetar med dem för att få din logotyp varumärkesskyddad eller verifiera att den redan är varumärkesskyddad.

   1. När du har verifierat att logotypen är varumärkesskyddad kontaktar du DigiCert eller Entrust Certificate Authority (CA) för att begära ett VMC.

   1. När ditt VMC har godkänts får du en PEM-fil (Privacy Enhanced Mail) för entitetscertifikatet. Lägg till eventuella andra mellanliggande certifikat som du får från certifikatutfärdaren till den här PEM-filen. Ladda upp PEM-filen (tillsammans med bifogade filer) till den offentliga webbservern och notera PEM-filens URL. Du använder URL:en i TXT-posten i BIMI.

   1. När BIMI-posten visas på sidan med information om underdomäner för en viss underdomän kan du använda BIMI Inspector som finns tillgänglig [här](https://bimigroup.org/bimi-generator/) för att kontrollera att BIMI-posten fungerar som den ska.

   Detaljerad information om BIMI-implementering finns i [Standarddokumentation för BIMI](https://bimigroup.org/implementation-guide/)
+++

1. Klicka på **[!UICONTROL Add]** för att bekräfta att du vill skapa BIMI-posten.

När skapandet av BIMI-posten har bearbetats (ungefär 5 minuter) visas den på informationsskärmen i underdomänerna. [Läs mer att övervaka TXT-poster för dina underdomäner](gs-txt-records.md#monitor)
