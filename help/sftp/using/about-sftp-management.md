---
title: Om SFTP-hantering
description: Läs mer om SFTP-hantering på Kontrollpanelen
testing: SSECD-836
translation-type: tm+mt
source-git-commit: 9fe5f25ef2f3d7dafe9ae63d430279c354fce25a
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 3%

---


# Om SFTP-hantering {#about-sftp-management}

På Kontrollpanelen kan du interagera med alla SFTP-servrar som är anslutna till Campaign-instanser som du har tillgång till. De flesta instanser har anslutna SFTP-servrar (i vissa fall är det inte säkert att utvecklings- och sceninstanser är anslutna till några SFTP-servrar).

Åtkomst till SFTP-servrar görs med en SFTP-klientprogramvara som du kan hitta och hämta online. För att kunna ansluta till en server, antingen via ett sådant klientprogram eller ett API, måste du konfigurera en offentlig SSH-nyckel och lägga till den IP-adress som ansluter till SFTP-servern till tillåtelselista.

Med kontrollpanelen kan du utföra åtgärderna nedan för att hantera dina SFTP-servrar:

* övervaka deras **lagringskapacitet**,
* Hantera **IP-adresser som kan listas**: lägga till eller ta bort IP-adressintervall för en eller flera servrar,
* Hantera **offentliga SSH-nycklar** för att komma åt dina servrar.

Detaljerad information om dessa åtgärder finns i avsnitten nedan.
