---
product: campaign
solution: Campaign
title: Ta bort delegering av underdomäner
description: Läs mer hur du tar bort delegeringen av underdomäner till Adobe.
feature: Control Panel
role: Architect
level: Experienced
source-git-commit: dbd1b2dd31cf732609f8a515e9adc1c43cbf39c6
workflow-type: tm+mt
source-wordcount: '808'
ht-degree: 59%

---

# Ta bort delegering av underdomäner till Adobe {#remove-delegated--subdomains}

>[!CONTEXTUALHELP]
>id="cp_subdomain_undelegate"
>title="Ta bort delegering av underdomäner"
>abstract="På den här skärmen kan du ta bort delegeringen av en underdomän till Adobe. Tänk på att den här processen inte kan ångras och att den är oåterkallelig tills körningen är slutförd.<br><br>Om du försöker ta bort delegeringen av en primär domän för den valda instansen blir du ombedd att välja den domän som ska ersätta den."

Med kontrollpanelen kan du ta bort delegeringen av en underdomän som har delegerats till Adobe eller delegerats med CNAME.

## Viktiga anteckningar {#important}

Innan du fortsätter bör du noggrant överväga vilka konsekvenser som uppstår när borttagningsprocessen har startats:

* När processen har startats går det inte att ångra borttagningen av underdomäner och den är oåterkallelig tills processen har slutförts.
* Ingen annan delegering av underdomäner kan tas bort när en liknande process pågår i en annan underdomän.
* En delegering som tagits bort från en underdomän kan inte delegeras på nytt förrän tre dagar efter borttagningen.

## Ta bort en delegering av underdomäner {#steps}

Följ de här stegen för att ta bort delegeringen av en underdomän till Adobe:

1. Klicka på ellipsknappen bredvid den domändelegering som du vill ta bort och klicka sedan på **[!UICONTROL Remove delegated subdomain]**.

   ![](assets/undelegate-subdomain.png)

1. Granska ansvarsfriskrivningen och bekräfta borttagningen av domändelegeringen till Adobe.

1. Granska information om instansen som underdomänen är kopplad till, inklusive relaterade IP-tillhörigheter och varumärkeskonfigurationer.

   Om du tar bort delegeringen av den primära domänen för den valda instansen måste du välja den domän som ska ersätta den med listan **[!UICONTROL Replacement Domain]**.

   Klicka på **[!UICONTROL Next]** för att fortsätta med borttagningen.

   ![](assets/undelegate-subdomain-details.png)

1. Om du tar bort en delegering av CNAME-typ eller om du ersätter en primär domän med en domän som delegerats med CNAME, kan du lägga till ytterligare **[!UICONTROL Action]** visas för att hantera DNS-poster. [Läs mer i det här avsnittet](#dns)

1. Granska sammanfattningen som visas. Bekräfta borttagningen genom att ange URL:en för den domän som du vill ta bort delegeringen för och klicka på **[!UICONTROL Submit]**.

   ![](assets/undelegate-submit.png)

När delegeringsborttagningen har startats visas det väntande jobbet i jobbloggarna tills det är klart.

![](assets/undelegate-job.png)

## Hantering av DNS-poster {#dns}

Om du vill konfigurera en domändelegering med CNAME måste du lägga till specifika poster på DNS-servern på Kontrollpanelen. [Lär dig hur du konfigurerar underdomäner med CNAMEs](setting-up-new-subdomain.md#use-cnames)

När du tar bort en delegering av CNAME-typ måste du **ta bort dessa DNS-poster** från servern för att undvika problem. Om du dessutom vill ta bort delegeringen av en primär underdomän och ersätta den med en domän som har delegerats med CNAME, kan du behöva **lägg till DNS-poster** på servern, beroende på vilka IP-tillhörigheter som har angetts för underdomänen.

Tabellen nedan visar vilka åtgärder som ska utföras beroende på vilken typ av delegering du tar bort och vilken typ av delegering som används för att konfigurera ersättningsdomänen.

| Borttagen delegering | Ersättningsdomän | Åtgärd krävs |
|  ---  |  ---  |  ---  |
| Fullständig | Ingen ersättningsdomän | Ingen åtgärd krävs |
| Fullständig | CNAME | Lägg till DNS-poster (valfritt baserat på IP-tillhörigheter) |
| Fullständig | Fullständig | Ingen åtgärd krävs |
| CNAME | Ingen ersättningsdomän | Ta bort DNS-poster |
| CNAME | CNAME | Ta bort och lägga till DNS-poster (valfritt baserat på IP-tillhörigheter) |
| CNAME | Fullständig | Ta bort DNS-poster |

För att göra detta finns ytterligare en **[!DNL Action]** visas innan delegeringsborttagningen bekräftas. På den här skärmen visas de DNS-poster som ska tas bort eller läggas till, beroende på sammanhanget.

![](assets/action-step.png)

### Ta bort DNS-poster

1. Navigera till din DNS-server och ta bort posterna som visas på Kontrollpanelen.
1. Gå tillbaka till Kontrollpanelen och klicka på **[!UICONTROL Next]** om du vill fortsätta med borttagningen av delegeringen.

### Lägg till DNS-poster

1. Navigera till din DNS-server och lägg till de poster som visas på Kontrollpanelen.
1. Vänta tills DNS-tillägget börjar gälla.
1. Gå tillbaka till Kontrollpanelen och klicka på **[!UICONTROL Verify]**.
1. Klicka på **[!UICONTROL Next]** om du vill fortsätta med borttagningen av delegeringen.

## Felkoder {#FAQ}

I det här avsnittet visas felmeddelanden som du kan stöta på när du försöker ta bort delegeringen av en underdomän:

| Felkod | Meddelande | Beskrivning |
|  ---  |  ---  |  ---  |
| 8002 | Begärd delegerad domänborttagning kan inte åtgärdas eftersom en liknande överlappande begäran pågår. Försök igen efter tre dagar | Ett borttagningsjobb för underdomändelegering pågår redan för den valda instansen. Vänta i tre dagar innan du startar ett nytt borttagningsjobb. |
| 8003 | Begärd delegerad domänborttagning stöds inte för den här instansen. | Delegeringsborttagning stöds inte för den valda underdomänen på grund av ett tekniskt problem. Kontakta kundtjänst. |
| 8004 | Begärd delegerad domänborttagning tillåts inte eftersom det bara finns en domän i den här instansen. | Endast en underdomän har delegerats för den valda instansen. Delegeringsborttagning tillåts inte. |
| 8005 | Begärd delegerad domänborttagning stöds inte för den här konfigurationen. | Delegeringsborttagning stöds inte för den valda underdomänen på grund av ett tekniskt problem. Kontakta kundtjänst. |
| 8006 | Begärd delegerad domänborttagning tillåts inte på grund av okända orsaker. Kontakta kundtjänst. | Delegeringsborttagning stöds inte för den valda instansen på grund av okända problem. Kontakta kundtjänst. |
