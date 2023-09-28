---
product: campaign
solution: Campaign
title: Lägg till DMARC-poster
description: Lär dig hur du lägger till en DMARC-post för en underdomän.
feature: Control Panel
role: Architect
level: Experienced
source-git-commit: fc026f157346253fc79bde4ce624e7efa3373af2
workflow-type: tm+mt
source-wordcount: '535'
ht-degree: 0%

---


# Lägg till DMARC-poster {#dmarc}

## Om DMARC-poster {#about}

Domänbaserad Message Authentication, Reporting and Conformance (DMARC) är en protokollstandard för e-postautentisering som hjälper organisationer att skydda sina e-postdomäner från nätfiskeattacker och bedrägeri. Det gör att du kan bestämma hur en postlådeleverantör ska hantera e-postmeddelanden som inte godkänns vid SPF- och DKIM-kontroller, vilket ger ett sätt att autentisera avsändarens domän och förhindra obehörig användning av domänen i skadliga syften.

## Begränsningar och krav {#limitations}

* SPF- och DKIM-poster är nödvändiga för att skapa en DMARC-post.
* DMARC-poster kan bara läggas till för underdomäner med fullständig underdomändelegering. [Läs mer om konfigurationsmetoder för underdomäner](subdomains-branding.md#subdomain-delegation-methods)

## Lägga till en DMARC-post för en underdomän {#add}

Så här lägger du till en DMARC-post för en underdomän:

1. Klicka på ellipsknappen bredvid önskad underdomän i listan över underdomäner och välj **[!UICONTROL Subdomain details]**.

1. Klicka på **[!UICONTROL Add TXT record]** knapp och sedan välja **[!UICONTROL DMARC]** från **[!UICONTROL Record Type]** listruta.

   ![](assets/dmarc-add.png)

1. Välj **[!UICONTROL Policy Type]** som mottagarservern bör följa när ett av dina e-postmeddelanden misslyckas. Tillgängliga principtyper är:

   * Ingen,
   * Karantän (placering av skräppostmapp),
   * Avvisa (blockera e-postmeddelandet).

   Om din underdomän precis har konfigurerats rekommenderar vi att du anger det här värdet som Ingen tills din underdomän är helt konfigurerad och dina e-postmeddelanden skickas korrekt. När allt är korrekt konfigurerat kan du ändra policytypen till &quot;Karantän&quot; eller &quot;Avvisa&quot;.

   >[!NOTE]
   >
   > Det går inte att skapa BIMI-poster med principtypen Ingen för DMARC-post.

1. Fyll i de e-postadresser som ska ta emot DMARC-rapporterna. När ett av dina e-postmeddelanden misslyckas skickas DMARC-rapporter automatiskt till den e-postadress du väljer:

   * Aggregate-DMARC-rapporter ger högnivåinformation, t.ex. antalet e-postmeddelanden som misslyckades under en viss period.
   * Forensiska DMARC-felrapporter ger detaljerad information, till exempel vilken IP-adress som den misslyckade e-postadressen kommer från.

1. Som standard tillämpas den valda DMARC-principen på alla e-postmeddelanden. Du kan ändra den här parametern så att den endast används för en viss procentandel av e-postmeddelanden.

   När du distribuerar DMARC gradvis kan du börja med en liten andel av dina meddelanden. I takt med att fler meddelanden från din domänpass-autentisering med mottagande servrar uppdateras din post med en högre procentandel tills du når 100 procent.

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