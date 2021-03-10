---
product: campaign
solution: Campaign
title: Om SFTP-hantering
description: Läs mer om SFTP-hantering på Kontrollpanelen
testing: SSECD-836 2
feature: 'Kontrollpanelen  '
role: Arkitekt
level: Mellanliggande
translation-type: tm+mt
source-git-commit: 4b8020dfd5d1f81a81d0e20025cfabe734744d34
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 4%

---


# Om SFTP-hantering {#about-sftp-management}

På Kontrollpanelen kan du interagera med alla SFTP-servrar som är anslutna till Campaign-instanser som du har tillgång till. De flesta instanser har anslutna SFTP-servrar (i vissa fall är det inte säkert att utvecklings- och sceninstanser är anslutna till några SFTP-servrar).

Åtkomst till SFTP-servrar görs via en SFTP-klientprogramvara som du kan hitta och hämta online. För att kunna ansluta till en server, antingen via ett sådant klientprogram eller ett API, måste du konfigurera en offentlig SSH-nyckel och lägga till den IP-adress som ansluter till SFTP-servern till tillåtelselista.

Med kontrollpanelen kan du utföra åtgärderna nedan för att hantera dina SFTP-servrar:

* övervaka deras **lagringskapacitet**,
* Hantera **IP-adresser tillåter listning**: lägga till eller ta bort IP-adressintervall för en eller flera servrar,
* Hantera **publika SSH-nycklar** för att komma åt dina servrar.

Detaljerad information om dessa åtgärder finns i avsnitten nedan.
