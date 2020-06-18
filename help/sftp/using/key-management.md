---
title: Nyckelhantering
description: Lär dig hur du hanterar nycklar för att ansluta till SFTP-servrar
translation-type: tm+mt
source-git-commit: 3faeb9651681a9edd18cf889fff65b02644cb690
workflow-type: tm+mt
source-wordcount: '601'
ht-degree: 4%

---


# Nyckelhantering {#key-management}

>[!CONTEXTUALHELP]
>id="cp_key_management"
>title="Om nyckelhantering"
>abstract="På den här fliken kan du hantera dina offentliga nycklar."
>additional-url="https://images-tv.adobe.com/mpcv3/8a977e03-d76c-44d3-853c-95d0b799c870_1560205338.1920x1080at3000_h264.mp4#t=166" text="Se filmen"

Adobe rekommenderar att alla kunder upprättar anslutningar till sina SFTP-servrar med ett **nyckelpar med offentlig och privat nyckel**.

Stegen för att generera en offentlig SSH-nyckel och lägga till den för att få åtkomst till SFTP-servern beskrivs nedan, samt rekommendationer om autentisering.

Once access to the server is set up, remember to **add the IP addresses that will require access to the server to the allow list** so that you can connect to it. For more on this, refer to [this section](../../instances-settings/using/ip-whitelisting-instance-access.md).

>[!NOTE]
>
>Det går för närvarande inte att ta bort en offentlig SSH-nyckel.

## God praxis {#best-practices}

**Om den offentliga SSH-nyckeln**

Se till att du alltid använder samma autentisering för att ansluta till servern, och du använder ett format som stöds för nyckeln.

**API-integrering med användarnamn och lösenord**

I mycket sällsynta fall aktiveras lösenordsbaserad autentisering på vissa SFTP-servrar. Adobe rekommenderar att du använder nyckelbaserad autentisering eftersom den här metoden är mer effektiv och säker. Du kan begära att få byta till nyckelbaserad autentisering genom att kontakta Kundtjänst.

>[!IMPORTANT]
>
>Om ditt lösenord förfaller, även om det finns nycklar installerade på datorn, kan du inte logga in på dina SFTP-konton.

![](assets/control_panel_passwordexpires.png)

## Installing the SSH key {#installing-ssh-key}

>[!CONTEXTUALHELP]
>id="cp_sftp_publickey_add"
>title="Lägg till ny offentlig nyckel"
>abstract="Add a new public key for an instance."

>[!IMPORTANT]
>
>Stegen nedan är ett exempel på hur du bara skapar SSH-nycklar. Följ riktlinjerna för din organisation när det gäller SSH-nycklar. Exemplet nedan är bara ett exempel på hur detta kan göras och fungerar som en bra referenspunkt för att kommunicera krav till ditt team eller din interna nätverksgrupp.

1. Navigera till fliken **[!UICONTROL Key Management]** och klicka sedan på knappen **[!UICONTROL Add new public key]**.

   ![](assets/key0.png)

1. I dialogrutan som öppnas väljer du det användarnamn som du vill skapa den offentliga nyckeln för och den server som du vill aktivera nyckeln för.

   >[!NOTE]
   >
   >Gränssnittet kontrollerar om ett visst användarnamn är aktivt för en viss instans och ger dig möjlighet att aktivera nyckeln för en eller flera instanser.
   >
   >En eller flera offentliga SSH-nycklar kan läggas till för varje användare.

   ![](assets/key1.png)

1. Kopiera och klistra in den offentliga SSH-nyckeln. Om du vill generera en offentlig nyckel följer du stegen nedan för ditt operativsystem:

   >[!NOTE]
   >
   >Den offentliga SSH-nyckelstorleken ska vara **2 048 bitar**.

   **Linux och Mac:**

   Använd Terminal för att generera ett nyckelpar för offentlig och privat nyckel:
   1. Ange det här kommandot: `ssh-keygen -m pem -t rsa -b 2048 -C "your_email@example.com"`.
   1. Ge nyckeln ett namn när du uppmanas till det. Om ssh-katalogen inte finns skapas en åt dig.
   1. Ange och ange sedan en lösenfras igen när du uppmanas till det. Den kan också lämnas tom.
   1. Ett nyckelpar, &quot;name&quot; och &quot;name.pub&quot;, skapas av systemet. Sök efter filen &quot;name.pub&quot; och öppna den. Den ska ha en alfanumerisk sträng som slutar med den e-postadress som du har angett.
   **Windows:**

   Du kan behöva installera ett tredjepartsverktyg som hjälper dig att generera nyckelpar för privat/offentlig nyckel i samma format,&quot;name.pub&quot;.

1. Öppna .pub-filen och kopiera och klistra sedan in hela strängen med början från&quot;ssh..&quot;. till Kontrollpanelen.

   ![](assets/publickey.png)

1. Skapa nyckeln genom att klicka på **[!UICONTROL Save]** knappen. Kontrollpanelen sparar den publika nyckeln och tillhörande fingeravtryck, som är krypterat med SHA256-formatet.

Du kan använda fingeravtryck för att matcha privata nycklar som har sparats på datorn med motsvarande offentliga nycklar som har sparats på Kontrollpanelen.

![](assets/fingerprint_compare.png)

&quot;**..**&quot; kan du ta bort en befintlig nyckel eller kopiera tillhörande fingeravtryck till Urklipp.

![](assets/key_options.png)
