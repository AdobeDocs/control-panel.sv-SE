---
product: campaign
solution: Campaign
title: Logga in på SFTP-servern
description: Lär dig logga in på SFTP-servern
translation-type: tm+mt
source-git-commit: 168ae32d7931497bb37d63f7dd1d14eadbb4b1bf
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 5%

---


# Logga in på SFTP-servern {#logging-into-sft-server}

Stegen nedan visar hur du ansluter en SFTP-server via ditt SFTP-klientprogram.

Innan du loggar in på servern bör du kontrollera att:

* SFTP-servern är **värd för Adobe**.
* Ditt **användarnamn** har konfigurerats för servern. You can check this information directly in the Control Panel, in the **Key management** tab from the SFTP Card.
* Du har ett **privat och offentligt nyckelpar** för att logga in på SFTP-servern. Mer information om hur du lägger till SSH-nyckeln finns i [det här avsnittet](../../sftp/using/key-management.md) .
* Din **offentliga IP-adress har lagts till tillåtelselista** på SFTP-servern. Om inte, se [det här avsnittet](../../sftp/using/ip-range-allow-listing.md) för mer information om hur du lägger till IP-intervallet i tillåtelselista.
* Du har åtkomst till en **SFTP-klientprogramvara**. Du kan kontakta din IT-avdelning för SFTP-klientprogram som de rekommenderar att använda, eller söka efter ett på Internet om det är tillåtet enligt din företagspolicy.

Så här ansluter du till SFTP-servern:

1. Launch the Control Panel, then select the **[!UICONTROL Key Management]** tab from the **[!UICONTROL SFTP]** card.

   ![](assets/sftp_card.png)

1. Starta SFTP-klientprogrammet och kopiera och klistra sedan in serveradressen från Kontrollpanelen, följt av&quot;campaign.adobe.com&quot;, och fyll sedan i ditt användarnamn.

   ![](assets/do-not-localize/connect1.png)

1. I **[!UICONTROL SSH Private Key]** fältet väljer du den privata nyckelfil som finns lagrad på datorn. Den motsvarar en textfil som har samma namn som den offentliga nyckeln, utan tillägget&quot;.pub&quot; (t.ex.&quot;enable&quot;).

   ![](assets/do-not-localize/connect2.png)

   Fältet fylls **[!UICONTROL Password]** automatiskt i med den privata nyckeln från filen.

   ![](assets/do-not-localize/connect3.png)

   Du kan kontrollera att nyckeln som du försöker använda sparas på Kontrollpanelen genom att jämföra fingeravtrycket för den privata eller offentliga nyckeln med fingeravtrycket för tangenterna som visas på fliken Nyckelhantering på SFTP-kortet.

   ![](assets/fingerprint_compare.png)

   >[!NOTE]
   >
   >Om du använder en Mac-dator kan du visa fingeravtrycket för den privata nyckel som finns på datorn genom att köra följande kommando:
   >
   >`ssh-keygen -lf <path of the privatekey>`

1. När all information är ifylld klickar du för **[!UICONTROL Connect]** att logga in på SFTP-servern.

   ![](assets/do-not-localize/sftpconnected.png)
