---
title: Kreditorenzusammenarbeit einrichten und verwalten
description: In diesem Thema wird erläutert, wie Kreditorenzusammenarbeit in Dynamics 365 Supply Chain Management eingerichtet werden. Außerdem wird erläutert, wie Sie neue Benutzer für die Zusammenarbeit mit Anbietern bereitstellen und die Sicherheitsrollen für diese Benutzer verwalten.
author: GalynaFedorova
ms.date: 12/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DirExternalRole, SysUserRequestListPage, VendVendorPortalUsers, WorkflowTableListPageRnr
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: 220774
ms.assetid: 69d05e8b-7dc2-48ea-bc24-bea9ac963579
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 4b59513d86426d3c1bfd759b9aabc331e58d5423
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8677561"
---
# <a name="set-up-and-maintain-vendor-collaboration"></a>Kreditorenzusammenarbeit einrichten und verwalten

[!include [banner](../includes/banner.md)]

Die Kreditorenzusammenarbeitsschnittstelle zeigt eine begrenzte Menge an Informationen zu Bestellungen, Rechnungen und Lieferbestand für externe Kreditorenbenutzer an. Von dieser Schnittstelle aus kann ein Lieferant auch auf Angebotsanfragen (RFQs) antworten und grundlegende Unternehmensinformationen anzeigen und bearbeiten.

In diesem Thema wird erläutert, wie Kreditorenzusammenarbeit in Dynamics 365 Supply Chain Management eingerichtet werden. Außerdem wird erläutert, wie Sie einen Workflow einrichten, der neue Benutzer für die Zusammenarbeit mit Anbietern bereitstellt und die Sicherheitsrollen für diese Benutzer verwaltet.

> [!NOTE]
> Die Informationen zum Einrichten von Sicherheitsrollen für die Zusammenarbeit mit Anbietern gelten nur für die aktuelle Version von Finance and Operations. In Microsoft Dynamics AX 7.0 (Februar 2016) und Microsoft Dynamics AX-Anwendungsversion 7.0.1 (Mai 2016) arbeiten Sie mit Kreditoren zusammen, indem Sie das Modul **Kreditorenportal** verwenden. Informationen zu Benutzerberechtigungen für das Vendor-Portal in Microsoft Dynamics AX finden Sie unter [Benutzersicherheit des Kreditorenportals](configure-security-vendor-portal-users.md).

## <a name="set-up-vendor-collaboration-security-roles"></a>Sicherheitsrollen für Kreditorenzusammenarbeit einrichten

Ein Beschaffungsexperte oder ein Anbieter mit ausreichenden Berechtigungen kann anfordern, dass eine Kontaktperson als Benutzer bereitgestellt wird, indem er **Anbieterbenutzer bereitstellen** im Kontaktdatensatz aktiviert. Während des Bereitstellungsprozesses werden Benutzerberechtigungen für den neuen externen Benutzer ausgewählt und die neue Kreditorenbenutzeranforderung wird gesendet. Es ist wichtig, dass Sie die Benutzerberechtigungen, die in der Benutzeranfrage des Anbieters zur Auswahl stehen, richtig einrichten. Andernfalls wird Lieferanten möglicherweise Zugriff auf Informationen gewährt, auf die sie im Supply Chain Management keinen Zugriff haben sollten.

### <a name="set-up-the-security-roles-that-are-available-for-selection-when-a-new-user-request-is-used-for-a-contact-person"></a>Richten Sie die Sicherheitsrollen ein, die zur Auswahl stehen, wenn eine neue Benutzeranfrage für einen Ansprechpartner verwendet wird

1. Wählen Sie **Systemverwaltung** &gt; **Sicherheit** &gt; **Externe Rollen**.
2. Wählen Sie **Neu**, und wählen Sie dann eine Sicherheitsrolle und die Parteirolle **Kreditor** aus.

Vielleicht möchten Sie die Rollen **Kreditorverwaltung (extern)** und **Anbieter (extern)** hinzufügen, die im Supply Chain Management bereitgestellt werden. Alternativ können Sie Sicherheitsrollen verwenden, die Ihr Unternehmen erstellt hat.

Sie sollten die Rolle **Anbieteradministrator (extern)** nur verfügbar machen, wenn Kreditoren in der Lage sein sollen, neue Kontakte zu erstellen, Benutzeranfragen für die Zusammenarbeit mit Kreditoren für neue Benutzer und Änderungen an Benutzerinformationen zu senden und diese Anfragen über einen Workflow zu bearbeiten.

Wenn Sie Anbieterkontakte und Benutzer manuell einrichten möchten, können Sie nur die **Rolle des Lieferanten (extern)** erhältlich machen. Diese Rolle ist dann die einzige Rolle, die über eine Kreditorenbenutzeranforderung angefordert werden kann.

> [!NOTE]
> Die Rolle **SystemUser** wird automatisch gewährt, wenn Sie manuell ein neues Benutzerkonto erstellen. Daher müssen Sie diese Rolle entfernen und die Rolle **SystemExternalUser** zuweisen. Wenn neue Benutzerkonten über den Workflow erstellt werden, der durch eine Kreditorenbenutzeranfrage zur Bereitstellung eines neuen Benutzers initiiert wird, eine oder mehrere der Rollen, die Sie für die Zusammenarbeit mit Kreditoren eingerichtet haben, und die **SystemExternalUser**-Rolle zugewiesen wird.

#### <a name="vendor-admin-external-security-role"></a>Sicherheitsrolle des Anbieteradministrators (extern)

Die Rolle **Anbieteradministrator (extern)** Rolle kann für externe Kreditoren verwendet werden, die Kontaktinformationen von Kreditoren pflegen und Anfragen stellen, um neue Benutzer für die Zusammenarbeit mit Kreditoren bereitzustellen. Externe Benutzer mit dieser Sicherheitsrolle können die folgenden Aufgaben ausführen:

- Informationen zur Kontaktperson anzeigen und ändern, z. B. den Titel, die E-Mail-Adresse und die Telefonnummer der Person.
- Fügen Sie eine neue oder vorhandene Kontaktperson zu den Kreditorenkonten hinzu, für die sie ein Kontakt sind.
- Löschen Sie alle Kontaktpersonen, die sie erstellt haben.
- Aktivieren oder deaktivieren Sie die Verknüpfung zwischen einer Kontaktperson und einem Kreditorenkonto. Nachdem die Verknüpfung zwischen einer Kontaktperson und einem Kreditorenkonto deaktiviert wurde, kann die Kontaktperson in neuen Bestellungen oder anderen Dokumenten nicht mehr genannt werden.
- Verweigern oder erlauben Sie einer Kontaktperson den Zugriff auf Dokumente auf der Schnittstelle für die Kreditorenzusammenarbeit, die für das Kreditorenkonto spezifisch sind. Nachdem die Verknüpfung zwischen einer Kontaktperson und einem Kreditorenkonto deaktiviert wurde, wird der Zugriff auf Dokumente, die spezifisch für das Kreditorenkonto sind, immer verweigert.
- Fordern Sie ein neues Benutzerkonto für einen Ansprechpartner an, indem Sie die Aktion **Benutzer bereitstellen** verwenden.
- Fordern Sie die Deaktivierung des Benutzerkontos einer Kontaktperson an.
- Fordern Sie an, dass das Benutzerkonto einer Kontaktperson geändert wird, um Sicherheitsrollen hinzuzufügen oder zu entfernen.
- RFQs nzeigen.

#### <a name="vendor-external-security-role"></a>Sicherheitsrolle des Anbieters (extern)

Die **Rolle des Lieferanten (extern)** kann für externe Lieferanten verwendet werden, die mit Bestellungen arbeiten. Externe Benutzer mit dieser Sicherheitsrolle können die folgenden Aufgaben ausführen:

- Beantworten und Anzeigen von Informationen zu Bestellungen.
- Kreditor-Kooperationsrechnungen verwalten.
- Lieferbestand anzeigen.
- Anzeigen von Beantworten von RFQs.
- Kreditordaten anzeigen.

## <a name="set-up-security-roles-that-are-used-when-prospective-vendors-are-onboarded"></a>Richten Sie Sicherheitsrollen ein, die beim Onboarding potenzieller Anbieter verwendet werden

Um Kreditoren einzubinden, die über eine Registrierungsanforderung für potenzielle Kreditoren initiiert werden, müssen Sie eine externe Sicherheitsrolle einrichten. Diese Rolle wird neuen Benutzern während des Bereitstellungsprozesses zugewiesen, der durch den Workflow des Typs **Workflow für Benutzeranfragen (Plattform)** gesteuert wird. Weitere Informationen finden Sie im Abschnitt [Einrichten von Workflows zur Verarbeitung von Benutzeranfragen zur Zusammenarbeit mit Anbietern](#set-up-workflows-to-process-vendor-collaboration-user-requests) weiter unten in diesem Thema.

Informationen zum Onboarding potenzieller Anbieter finden Sie unter [Onboarding für Anbieter durchführen](vendor-onboarding.md).

### <a name="set-up-a-security-role-that-is-used-when-a-new-prospective-vendor-user-request-is-submitted"></a>Richten Sie eine Sicherheitsrolle ein, die verwendet wird, wenn eine neue potenzielle Anbieterbenutzeranfrage gesendet wird

1. Wählen Sie **Systemverwaltung** > **Sicherheit** > **Externe Rollen**.
2. Wählen Sie **Neu**, und wählen Sie dann eine Sicherheitsrolle und die Parteirolle **Künftiger Kreditor** aus.

Sie sollten die Rolle **Künftiger Kreditor (extern)** hinzufügen, die im Supply Chain Management bereitgestellt wird.

Die Sicherheitsrolle gewährt nur Zugriff auf den Assistenten für die Registrierung neuer Kreditoren.

## <a name="set-up-workflows-to-process-vendor-collaboration-user-requests"></a>Einrichten von Workflows zur Verarbeitung von Benutzeranfragen zur Zusammenarbeit mit Anbietern

Um sicherzustellen, dass alle relevanten Aufgaben abgeschlossen sind und die entsprechenden Genehmigungen erteilt werden, müssen Sie Workflows einrichten, um Benutzeranfragen zur Zusammenarbeit mit Lieferanten zu bearbeiten.

Benutzeranfragen für die Zusammenarbeit mit Anbietern werden entweder von externen Anbietern eingereicht, die über die Sicherheitsrolle **Anbieteradministrator (extern)** oder ähnlichen Berechtigungen verfügen oder von Beschaffungsfachleuten in Ihrem Unternehmen. Sie können auch aus potenziellen Anbieterregistrierungsanfragen während des Anbieter-Onboarding-Prozesses generiert werden.

Es gibt drei Typen von Anfragen:

- Anfragen zur Bereitstellung eines neuen Benutzers
- Anfragen zur Inaktivierung eines bestehenden Benutzers
- Anfragen zum Ändern der Sicherheitsrollen eines vorhandenen Benutzers

Weitere Informationen zu Benutzeranfragen zur Kreditorezusammenarbeit finden Sie unter [Kreditorenzusammenarbeitbenutzer verwalten](manage-vendor-collaboration-users.md).

Sie müssen zwei oder mehr Workflows erstellen, um alle drei Arten von Benutzeranfragen für die Zusammenarbeit mit Kreditoren zu verarbeiten. Neue Workflows werden auf der Seite **Benutzerworkflows** erstellt.

### <a name="example-of-a-workflow-for-provisioning-new-users-and-modifying-security-roles"></a>Beispiel für einen Workflow zum Bereitstellen neuer Benutzer und Ändern von Sicherheitsrollen

Um Anforderungen von Anbieterbenutzern zum Erstellen neuer Benutzer und Ändern von Sicherheitsrollen zu bearbeiten, können Sie eine Verzweigungsbedingung an den Anfang des Workflows setzen. Auf diese Weise wird ein anderer Zweig des Workflows verwendet, je nachdem, ob ein neuer Benutzer angelegt oder ein bestehender Benutzer geändert werden soll.

Um diese Verzweigung einzurichten, erstellen Sie einen neuen Workflow vom Typ **Workflow für Benutzeranfragen (Plattform)**. Die Zweige dieses Workflows können die folgenden Elemente enthalten.

#### <a name="branch-to-provision-new-users"></a>Verzweigen, um neue Benutzer bereitzustellen

1. Weisen Sie der Person, die für die Genehmigung verantwortlich ist, dass neuen Benutzern Zugriff auf Informationen zur Kreditorenzusammenarbeit gewährt werden soll, eine Genehmigungsaufgabe zu.
2. Weisen Sie der Person, die für die Anforderung neuer Microsoft Azure Active Directory (Azure AD) Benutzerkonten im Azure-Portal zuständig ist, eine Aufgabe zu. Verwenden Sie die vordefinierte Aufgabe **Senden Sie eine Azure B2B-Benutzereinladung** für diesen Schritt. B2B-Benutzer können automatisch in Azure AD exportiert werden. Verwenden Sie die vordefinierten **Azure AD B2B-Nutzer bereitstellen**. Weitere Informationen finden Sie unter [B2B-Benutzer in Azure AD exportieren](../../fin-ops-core/dev-itpro/sysadmin/implement-b2b.md).
3. Weisen Sie der Person, die in Azure hochlädt, eine Genehmigungsaufgabe zu. Wenn ein Konto nicht erfolgreich erstellt wurde, lehnt diese Person die Aufgabe ab und beendet den Workflow. Diese Genehmigungsaufgabe kann übersprungen werden, wenn Sie den Schritt eingefügt haben, der automatisch neue Benutzerkonten über die B2B-Anwendungsprogrammierschnittstelle (API) nach Azure exportiert.
4. Fügen Sie eine automatisierte Aufgabe hinzu, die einen neuen Benutzer bereitstellt. Verwenden Sie die vordefinierte Aufgabe **Benutzer automatisch bereitstellen** für diesen Schritt.
5. Fügen Sie eine Aufgabe hinzu, die den neuen Benutzer benachrichtigt. Möglicherweise möchten Sie dem neuen Benutzer eine Willkommens-E-Mail senden, die eine URL für Supply Chain Management enthält. Diese E-Mail kann eine Vorlage verwenden, die Sie auf der Seite **E-Mail-Nachrichten** erstellen und wählen dann auf der Seite **Benutzer-Workflow-Parameter** auswählen. Die Vorlage kann das Tag **%portalURL%** umfassen. Wenn die Willkommens-E-Mail generiert wird, wird dieses Tag durch die URL des Supply Chain Management-Mandanten ersetzt.

    > [!NOTE]
    > Dieser Workflow kann in mehreren Szenarien verwendet werden, die das Onboarding von Benutzern beinhalten. Es kann beispielsweise verwendet werden, wenn potenzielle Kreditoren oder Ansprechpartner ein Kreditorenkollaborationskonto benötigen. Daher sollten Sie die E-Mail als allgemeine Aussage formulieren, die für mehrere Zwecke verwendet werden kann.

#### <a name="branch-to-modify-security-roles"></a>Verzweigen, um Sicherheitsrollen zu ändern

1. Weisen Sie der Person, die für die Genehmigung von Änderungen an Sicherheitsrollen verantwortlich ist, eine Genehmigungsaufgabe zu.
2. Fügen Sie eine automatisierte Aufgabe hinzu, die die relevanten Sicherheitsrollen hinzufügt oder entfernt. Verwenden Sie die Aufgabe **Benutzer automatisch bereitstellen** für diesen Schritt.

### <a name="example-of-a-workflow-for-inactivating-a-user"></a>Beispiel für einen Workflow zum Deaktivieren eines Benutzers

Erstellen Sie einen Workflow des Typs **Workflow-Plattform für Benutzeranfragen deaktivieren** und fügen Sie dann die folgenden Aufgaben hinzu.

1. Weisen Sie der Person, die für das Annehmen von Anfragen an inaktive Benutzer verantwortlich ist, eine Genehmigungsaufgabe zu. Sie können Bedingungen hinzufügen, um diesen Genehmigungsschritt zu automatisieren.
2. Fügen Sie eine automatisierte Aufgabe hinzu, die den Benutzer deaktiviert. Verwenden Sie die Aufgabe **Automatische Benutzerinaktivierung** für diesen Schritt.
3. Fügen Sie alle erforderlichen Bereinigungsaufgaben hinzu. Sie können beispielsweise eine Aufgabe hinzufügen, die das Konto aus Ihrem Verzeichnis im Azure-Portal entfernt.

## <a name="enable-vendor-collaboration-for-a-specific-vendor"></a>Aktivieren Sie die Kreditorenzusammenarbeit für einen bestimmten Kreditor

Bevor Sie ein Benutzerkonto für jemanden, der die Kreditorzusammenarbeit verwenden wird, erstellen, müssen Sie den Kreditor einrichten, um die Kreditorzusammenarbeit zu verwenden. Legen Sie auf der Seite **Kreditoren** auf der Registerkarte **Allgemein** das Feld **Zusammenarbeitsaktivierung** fest. Die folgenden Optionen stehen zur Verfügung:

- **Aktiv (Bestellung wird automatisch bestätigt)** – Bestellungen werden automatisch bestätigt, wenn der Kreditor diese akzeptiert ohne Änderungen anzufragen.
- **Aktiv (Bestellung wird nicht automatisch bestätigt)** – Ihre Organisation muss Bestellungen manuell bestätigen, nachdem der Kreditor diese akzeptiert hat.

> [!NOTE]
> Auch Einkaufsprofis in Ihrem Unternehmen können diese Aufgabe übernehmen.

## <a name="troubleshoot-the-provisioning-of-new-vendor-collaboration-users"></a>Fehlerbehebung bei der Bereitstellung neuer Benutzer für die Zusammenarbeit mit Anbietern

Neue Kreditorzusammenarbeitsbenutzer werden über den Workflow bereitgestellt, den Sie eingerichtet haben, um Anfragen von Kreditorzusammenarbeitsbenutzern des Typs **Anbieterbenutzer bereitstellen**.

Wenn die E-Mail-Adresse eines neuen Benutzers für die Zusammenarbeit mit Anbietern zu einer Domäne gehört, die bei Azure als Mandant registriert ist (d. h., wenn es sich um ein verwaltetes Domänenkonto handelt), muss die E-Mail-Adresse ein bereits vorhandenes Azure AD-Konto sein. Andernfalls kann der Bereitstellungsprozess nicht abgeschlossen werden.

Weitere Informationen zum Verfahren, das in der Aufgabe **Senden Sie eine Azure B2B-Benutzereinladung** im Workflow für Azure AD-Kontoverwaltung verwendet wird, finden Sie unter [Azure Active Directory B2B-Zusammenarbeit](/azure/active-directory/external-identities/what-is-b2b).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Zusammenarbeit mit externen Kreditoren](vendor-collaboration-work-external-vendors.md)

Sehen Sie sich ein kurzes Video zum Onboarding-Prozess des Anbieters an: [Onboarding eines neuen Anbieters](https://www.youtube.com/watch?v=0KUc3AGaTKk&feature=youtu.be)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
