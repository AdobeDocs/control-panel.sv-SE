---
product: campaign
solution: Campaign
title: Lägg till DMARC-poster
description: Lär dig hur du lägger till en DMARC-post för en underdomän.
feature: Control Panel
role: Architect
level: Experienced
exl-id: 2ca66983-5beb-495a-9639-a31905500cff
source-git-commit: 64ea5e26786eea107983ee5025025c81334b0a91
workflow-type: tm+mt
source-wordcount: '714'
ht-degree: 0%

---

# Lägg till DMARC-poster {#dmarc}

## Om DMARC-poster {#about}

Domänbaserad Message Authentication, Reporting and Conformance (DMARC) är en protokollstandard för e-postautentisering som hjälper organisationer att skydda sina e-postdomäner från nätfiskeattacker och bedrägeri. Det gör att du kan bestämma hur en postlådeleverantör ska hantera e-postmeddelanden som inte godkänns vid SPF- och DKIM-kontroller, vilket ger ett sätt att autentisera avsändarens domän och förhindra obehörig användning av domänen i skadliga syften.

Detaljerad information om DMARC-implementering finns i [Adobe Deliverability Best Practice Guide](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html)

## Begränsningar och krav {#limitations}

* SPF- och DKIM-poster är nödvändiga för att skapa en DMARC-post.
* DMARC-poster kan bara läggas till för underdomäner med fullständig underdomändelegering. [Läs mer om konfigurationsmetoder för underdomäner](subdomains-branding.md#subdomain-delegation-methods)

## Lägga till en DMARC-post för en underdomän {#add}

Så här lägger du till en DMARC-post för en underdomän:

1. Klicka på ellipsknappen bredvid önskad underdomän i listan över underdomäner och välj **[!UICONTROL Subdomain details]**.

1. Klicka på **[!UICONTROL Add TXT record]** knapp och sedan välja **[!UICONTROL DMARC]** från **[!UICONTROL Record Type]** listruta.

   ![](assets/dmarc-add.png)

1. Välj **[!UICONTROL Policy Type]** som mottagarservern bör följa när ett av dina e-postmeddelanden misslyckas. Tillgängliga principtyper är:

   * **[!UICONTROL None]**,
   * **[!UICONTROL Quarantine]** (placering av skräppostmapp),
   * **[!UICONTROL Reject]** (blockera e-postmeddelandet).

   Som en god praxis rekommenderas att långsamt införa DMARC-implementering genom att eskalera din DMARC-policy från p=none till p=karantän, till p=reject när du får DMARC-förståelse för DMARC:s potentiella påverkan.

   * **Steg 1:** Analysera den feedback du får och använder (p=none), som instruerar mottagaren att inte utföra några åtgärder mot meddelanden som inte kan autentiseras, men ändå skicka e-postrapporter till avsändaren. Granska och åtgärda även problem med SPF/DKIM om legitimt meddelande inte kan autentiseras.

   * **Steg 2:** Kontrollera om SPF och DKIM är justerade och skickar autentisering för alla giltiga e-postmeddelanden, och flytta sedan principen till (p=karantän), vilket anger att den mottagande e-postservern ska placera e-postmeddelanden som inte kan autentiseras (detta innebär vanligtvis att meddelandena placeras i skräppostmappen). Om policyn är inställd på att sätta den i karantän rekommenderar vi att du börjar med en liten andel av dina e-postmeddelanden.

   * **Steg 3:** Justera princip till (p=avvisa). Obs! Använd den här profilen med försiktighet och kontrollera om den passar din organisation. p= avvisningsprincipen innebär att mottagaren helt nekar (studsar) alla e-postmeddelanden för domänen som inte kan autentiseras. När den här principen är aktiverad har bara e-post som verifieras som 100 % autentiserad av din domän en chans att skickas till Inkorgen.

   >[!NOTE]
   >
   > Det går inte att skapa BIMI-poster med principtypen Ingen för DMARC-post.

1. Fyll i de e-postadresser som ska ta emot DMARC-rapporterna. När ett av dina e-postmeddelanden misslyckas skickas DMARC-rapporter automatiskt till den e-postadress du väljer:

   * Aggregate-DMARC-rapporter ger högnivåinformation, t.ex. antalet e-postmeddelanden som misslyckades under en viss period.
   * Forensiska DMARC-felrapporter ger detaljerad information, till exempel vilken IP-adress som den misslyckade e-postadressen kommer från.

1. Om DMARC-profilen är inställd på Ingen anger du ett procentvärde som gäller för 100 % av e-postmeddelandena.

   Om profilen är inställd på Avvisa eller Karantän rekommenderar vi att du börjar med en liten andel av dina e-postmeddelanden. I takt med att fler e-postmeddelanden från domänpass autentiseras med mottagande servrar kan du uppdatera posten långsamt med en högre procentandel.

   >[!NOTE]
   >
   >Om din domän använder BIMI måste din DMARC-princip ha ett procentvärde på 100 %. BIMI stöder inte DMARC-profiler där värdet är mindre än 100 %.

   ![](assets/dmarc-add2.png)

1. DMARC-rapporter skickas var 24: e timme. Du kan ändra rapportens sändningsfrekvens i dialogrutan **[!UICONTROL Reporting Interval]** fält. Minsta tillåtna intervall är 1 timme, medan högsta tillåtna värde är 2 190 timmar (dvs. 3 månader).

1. I **SPF** och **[!UICONTROL DKIM Identifier Alignment]** ska du ange hur strikt mottagarservrarna ska vara när du kontrollerar SPF- och DKIM-autentiseringar för ett e-postmeddelande.

   * **[!UICONTROL Relaxed]** läge: servern accepterar autentisering även om e-postmeddelandet skickas från en underdomän,
   * **[!UICONTROL Strict]** I läget accepteras autentisering endast när avsändardomänen matchar exakt med en SPF- och DKIM-domän.

   Säg att vi jobbar med `http://www.luma.com` domän. I&quot;Avslappnad&quot;-läge kommer e-post från `marketing.luma.com` underdomänen kommer att auktoriseras av servern medan de kommer att refuseras i strikt läge.

1. Klicka **[!UICONTROL Add]** för att bekräfta att DMARC-posten har skapats.

När DMARC-postgenereringen har bearbetats (ungefär 5 minuter) visas den på informationsskärmen i underdomänerna. [Lär dig övervaka TXT-poster för dina underdomäner](gs-txt-records.md#monitor)
