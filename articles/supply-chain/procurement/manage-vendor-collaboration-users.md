---
title: "Benutzer für Kreditor-Kooperationen verwalten"
description: "In diesem Thema wird beschrieben, wie Sie die Bereitstellung neuer Kreditorenzusammenarbeitsbenutzer anfordern können und wie neue Kreditorenzusammenarbeitkontakte hinzugefügt werden."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: smmContactPerson, VendVendorContactPerson, VendVendorPortalUser
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 220744
ms.assetid: edc19ad0-3565-4d47-98ac-dda6098f63ac
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 80374d6dce8aa5d5f2e5afc0656b42236ac974ec
ms.openlocfilehash: 036e8079bd976087514a074529dd4593c5a2b0a5
ms.contentlocale: de-de
ms.lasthandoff: 03/13/2018

---

# <a name="manage-vendor-collaboration-users"></a>Benutzer für Kreditor-Kooperationen verwalten

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie die Bereitstellung neuer Kreditorenzusammenarbeitsbenutzer anfordern können und wie neue Kreditorenzusammenarbeitkontakte hinzugefügt werden. 

Die Benutzeroberfläche für Kreditor-Kooperationen in Microsoft Dynamics 365 for Finance and Operations zeigt Informationen zu Bestellungen, Rechnungen und Lieferbestand externer Kreditoren an. Sie können neue Kreditorenzusammenarbeitkontakte erstellen und anfordern, dass neuen Benutzer bereitgestellt werden, wenn Sie als externer Kreditor mit der Sicherheitsrolle **Kreditorenadministrator (extern)** oder einer ähnlichen Berechtigung arbeiten. Sie können diese Aufgaben auch ausführen, wenn Sie als Beschaffungsspezialist arbeiten. In diesem Thema bezieht sich diese Rolle auf einen Beschaffungsspezialisten, der im Unternehmen arbeitet, das die Instanz von Finance and Operations besitzt. Weitere Informationen dazu, wie Kreditorenzusammenarbeit, wenn Sie ein externer Anbieter sind, finden Sie unter [Kreditoren mit Debitoren](vendor-collaboration-work-customers-dynamics-365-operations.md).  

Weitere Informationen dazu, wie Kreditorenzusammenarbeit, wenn Sie ein Beschaffungsprofil sind, finden Sie unter [Kreditorenzusammenarbeit mit für externe Kreditoren](vendor-collaboration-work-external-vendors.md).

## <a name="add-new-vendor-collaboration-contacts"></a>Hier können Sie neue Kreditorenzusammenarbeitkontakte hinzufügen
Wenn Sie jemandem Zugriff auf die Kreditorenzusammenarbeit gewähren möchten, müssen sie die Person zunächst als Kreditorenzusammenarbeitskontakt hinzufügen. Sie sollten auch Kontakte für Mitarbeiter Ihres Unternehmens hinzufügen, die die Kreditorenzusammenarbeit nicht verwenden werden. So könnten sie beispielsweise der Punkt der Kontaktperson für andere Arten von  Beschaffungsinformationen sein. Neue Kontakten werden auf der Seite **Alle Kontakte** hinzugefügt, auf die Sie über das Menü **Kreditorenzusammenarbeit**&gt; **Kontakte** zugreifen. Hinzufügen eines neuen Kontakts:

1.  Klicken Sie auf **Neu.**
2.  Geben Sie die Details der Kontaktperson ein.
3.  Wählen Sie, welche juristische Person sie in Ihrem Unternehmen vertritt und mit welcher juristischen Person sie im Unternehmen zusammenarbeiten wird. Dazu wählen Sie das Paar **Juristische Person in meinen Unternehmen** / **Juristische Personen im Kundenunternehmen** aus.
4.  Klicken Sie auf **Erstellen.**

Wenn Sie einen Kontakt löschen möchten, ist es nur möglich, jene zu löschen, die Sie erstellt haben.

## <a name="vendor-collaboration-user-requests"></a>Benutzeranforderungen für Kreditor-Kooperationen
Kreditorenzusammenarbeitbenutzeranforderungen können von einem Beschaffungsspezialisten oder einem Administrator des externen Lieferanten verwendet werden.

-   Wenn Sie ein externer Anbieter sind, übermitteln Sie Anforderungen von der Seite **Alle Kontakte**  innerhalb des Moduls **Kreditorenzusammenarbeit**.
-   Wenn Sie ein Beschaffungsspezialist sind, übermitteln Sie Anforderungen von der Seite **Kontakte anzeigen**. Dazu wählen Sie im Kreditorendatensatz im Abschnitt **Einstellungen** den Aktivitätsbereich und wählen **Kontakte**&gt; **Kontakte anzeigen** aus.

Sie können eine Anfrage für die Bereitstellung eines Benutzers machen, ihn deaktivieren oder die Sicherheitsrollen ändern. Wenn Sie Administrator des externen Kreditors sind, müssen Sie für die Kreditorenkonten als Kontaktperson erfasst werden, für die Sie Bnutzeranforderungen erstellen möchten und Sie müssen Zugang zur Kreditorenzusammenarbeitschnittstelle für die Kreditorenkonten haben.  

Wird eine Anforderung übermittelt, wird sie der **Kreditorenzusammenarbeit-Benutzeranforderungsliste** im Modul **Kreditorenzusammenarbeit** und der Liste **Kreditorenzusammenarbeits-Benutzeranfrage**  im Modul **Beschaffung** hinzugefügt (das Beschaffungsmodul ist für externe Nutzer nicht zugänglich)

### <a name="provision-a-user"></a>Benutzer bereitstellen

Bevor Sie anfordern können, dass ein neuer Benutzer bereitgestellt wird, muss diese Person als Kontakt für einen oder mehrere Kreditoren eingerichtet werden. Um eine Anfrage für einen neuen Kreditorenzusammenarbeitsbenutzer zu erstellen:

1. Wählen die Seite **Alle Kontakte** und klicken Sie auf **Breitstellung Kreditorenbenutzer**.
2. Hier geben Sie die E-Mail-Adresse des Benutzers ein. Diese Adresse wird vom Benutzer verwendet, um sich bei Finance and Operations anzumelden. Wenn die E-Mail-Adresse einer Domäne angehört, die als Mandant mit Microsoft Azure erfasst wurde, muss die E-Mail-Adresse ein vorhandenes Azure Active Directory (AAD) Konto sein, um den Bereitstellungsprozess erfolgreich abzuschließen. Wenn die E-Mail-Adresse keiner Domäne angehört, die mit Microsoft Azure erfasst wird, wird ein ADD-Konto als Teil des Bereitstellungsprozesses erstellt und der neue Benutzer wird eine Einladungsmail erhalten. Verbraucheradressen mit Domänen wie @hotmail.com, @gmail.com oder @comcast.net können nicht dazu verwendet werden, um einen Finance and Operations-Benutzer zu erfassen.
3. Setzen Sie die Option **Kreditorenzusammenarbeitzugriff zulässig** auf **Ja** für alle juristischen Personen, auf die der Benutzer zugreifen muss.
4. Wählen Sie im Abschnitt **Benutzerrollen zuweisen** das Kontrollkästen **Zuweisen** für die Sicherheitsrollen, die der neue Benutzer besitzen sollte.
5. Klicken Sie auf **Absenden**.

Wenn die Kreditorenbenutzeranforderung übermittelt wird, wird das Feld **Kreditorenzusammenarbeit erlaubt** für das ausgewählte Kreditorenkonto auf **Ja** festgelegt und es wird ein Benutzeranforderungsworkflow gestartet. Im Rahmen des Workflows wird ein neuer Benutzer in Finance and Operations erstellt und die Sicherheitsrollen zugewiesen. Darüber hinaus ist eine Azure B2B-Dienstleistung aktiviert, die die Interaktion mit dem Azure Portal initiiert und ein neues oder vorhandenes AAD-Konto dem Finance and Operations-Benutzer zuordnet. Weitere Informationen finden Sie unter[Was ist Azure AD-B2B-Zusammenarbeit?](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-b2b-what-is-azure-ad-b2b).

### <a name="inactivate-a-user"></a>Benutzer deaktivieren

Es gibt zwei Möglichkeiten, den Zugriff auf die Kreditorenzusammenarbeit für einen Benutzer zu entfernen:

-   Auf der Seite **Kontakte** für den Kreditor, legen Sie die Option **Kreditorenzusammenarbeitzugriff erlaubt** auf **Nein** für den Kontakt fest. Dies kann einzeln pro juristische Person erfolgen, für die die Person als Kontakt fungiert. Diese Option kann nur von Beschaffungsspezialisten verwendet werden.
-   Deaktivieren Sie das gesamte Benutzerkonto, indem Sie eine Anforderung **Kreditorenbenutzer deaktivieren** übermitteln.

Um das Deaktivieren eines Benutzers anzufordern:

1.  Wählen die Seite **Alle Kontakte** und klicken Sie auf **Kreditorenbenutzer** **deaktivieren**.
2.  Schreiben Sie einen Kommentar im Feld **Geschäftsbegründung**.
3.  Klicken Sie auf **Absenden**.

### <a name="modify-security-roles"></a>Sicherheitsrollen ändern

Die Seite **Kreditorenbenutzerrollen verwalten** ist dieselbe wie die Seite **Kreditorenbenutzer bereitstellen**, außer dass die Liste der Sicherheitsrollen bearbeitet werden kann.  

Um anzufordern, dass die Sicherheitsrollen für einen Benutzer geändert werden:

1.  Wählen Sie die Seite **Alle Kontakte** und klicken Sie auf **Kreditorenbenutzerrollen** **verwalten**.
2.  Schreiben Sie einen Kommentar im Feld **Geschäftsbegründung**.
3.  Wählen Sie im Abschnitt **Verwalten von Benutzerrollen** die Sicherheitsrollen aus, die Sie zuordnen möchten, und deaktivieren Sie jene, die Sie entfernen möchten.
4.  Klicken Sie auf **Absenden**.





