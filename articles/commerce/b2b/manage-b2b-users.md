---
title: Geschäftspartnerbenutzer auf B2B-E-Commerce-Websites verwalten
description: In diesem Artikel wird beschrieben, wie Sie Geschäftspartnerbenutzer auf Business-to-Business(B2B)-E-Commerce-Websites von Microsoft Dynamics 365 Commerce hinzufügen, Löschen und bearbeiten können.
author: josaw1
ms.date: 04/19/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.search.industry: retail
ms.search.form: ''
ms.openlocfilehash: a59220c16e195ff36980517baec6fb8246a18115
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281171"
---
# <a name="manage-business-partner-users-on-b2b-e-commerce-websites"></a>Geschäftspartnerbenutzer auf B2B-E-Commerce-Websites verwalten

[!include [banner](../../includes/banner.md)]

In diesem Artikel wird beschrieben, wie Sie Geschäftspartnerbenutzer auf Business-to-Business(B2B)-E-Commerce-Websites von Microsoft Dynamics 365 Commerce hinzufügen, Löschen und bearbeiten können.

> [!NOTE]
> - Der Artikel [B2B-Geschäftspartner mithilfe von Kundenhierarchien verstehen](partners-customer-hierarchies.md) ist für dieses Dokument Voraussetzung.
> - Stellen Sie sicher, dass Sie die Dokumenttypenentität in der Commerce-Zentralverwaltung initialisieren, indem Sie das **Dokumenttypen**-Formular unter **Organisationsverwaltung \> Dokumentverwaltung \> Dokumenttypen** öffnen.

Für B2B-E-Commerce-Websites müssen sich Organisationen registrieren, um Geschäftspartner zu werden. Nachdem eine Organisation Registrierungsdaten an eine B2B-E-Commerce-Website übermittelt hat, durchläuft die Registrierungsanforderung einen Qualifizierungsprozess. Wenn die Organisation erfolgreich qualifiziert ist, wird sie als Geschäftspartner eingebunden.

Nachdem eine Organisation als Geschäftspartner eingebunden wurde, wird der Organisationsbenutzer, der die Anforderung zum Geschäftspartner initiiert hat, als Administrator identifiziert und erhält die Berechtigung, zusätzliche autorisierte Benutzer der B2B-E-Commerce-Website einzubeziehen. Diese autorisierten Benutzer können dann im Namen des Geschäftspartners Bestellungen aufgeben.

## <a name="set-up-the-administrator-user-for-a-new-business-partner"></a>Den Administratorbenutzer für einen neuen Geschäftspartner einrichten

Potenzielle Geschäftspartner können den Onboarding-Prozess für eine B2B-E-Commerce-Website initiieren, indem sie eine Onboarding-Anfrage über einen Link auf der B2B-Website senden. Sie können dann das anpassbare Formular verwenden, um die Details anzugeben, die für das Onboarding und die Anmeldung erforderlich sind. Nachdem die Anfrage gesendet wurde, wird eine Bestätigungsseite für die Einreichung angezeigt. Wenn die Einreichung genehmigt wird, wird das Unternehmen, für das die Anforderung eingereicht wurde, ein Geschäftspartner und der Anforderer (d. h. der Benutzer, der die Onboarding-Anforderung initiiert hat) der Administrator des Geschäftspartners.

Gehen Sie wie folgt vor, um die Anforderung eines Geschäftspartners in der Commerce-Zentralverwaltung zu genehmigen.

1. Wechseln Sie zu **Einzelhandel und Handel \> Vertriebsplan**.
1. Führen Sie den **P-0001**-Auftrag aus, um alle Onboarding-Anfragen von Geschäftspartnern in die Commerce-Zentralverwaltung zu ziehen.
1. Nach dem der **P-0001**-Auftrag erfolgreich ausgeführt wurde, wechseln Sie zu **Einzelhandel und Handel IT \> Kunde** und führen Sie den Auftrag **Kunden und Kanalanforderungen synchronisieren** aus. Nachdem dieser Auftrag erfolgreich ausgeführt wurde, werden die Onboarding-Anforderungen als Interessenten vom Typ **B2B-Interessant** in der Commerce-Zentralverwaltung erstellt. 
1. Gehen Sie zu **Kunden \> Alle Interessenten** und wählen Sie den Interessentendatensatz für den neuen Geschäftspartner aus, um die Seite mit den Interessentendetails zu öffnen.
1. Wählen Sie auf der **Allgemein**-Registerkarte **Konvertieren \> Genehmigen/ablehnen** aus, um die Onboarding-Anfrage zu genehmigen. Wenn die Bestätigungsmeldung angezeigt wird, bestätigen Sie, dass Sie mit dem Vorgang fortfahren möchten, und genehmigen Sie dann die Anforderung. Die Genehmigung ändert das Feld **Status** des Interessentendatensatzes auf **Genehmigt**. Anschließend wird eine E-Mail an die E-Mail-Adresse des Anforderers gesendet, um zu bestätigen, dass seine Organisation als Geschäftspartner genehmigt wurde. Außerdem wird eine Kundenhierarchie erstellt, in der der Anforderer als Administrator für den Geschäftspartner hinzugefügt wird.

    > [!NOTE]
    > Derzeit wird die Bestätigungs-E-Mail sofort nach Genehmigung gesendet. Zukünftige Commerce-Funktionen werden es dem Administrator jedoch ermöglichen, die E-Mails manuell auszulösen.

1. Wechseln Sie zu **Einzelhandel und Handel IT \> Verteilungsplan** und führen Sie den Auftrag **1010 (Kunden)** zum Pushen der neuen Kunden- und Kundenhierarchiedatensätze in die Kanaldatenbank aus.

> [!NOTE]
> Um sicherzustellen, dass die neuen Kundendatensätze an die Kanaldatenbank gesendet werden, sollte mindestens eines der Adressbücher, die dem Kunden zugeordnet sind, in dem Kundenadressbuch enthalten sein, das dem Onlineshop zugeordnet ist. Sie können diesen Prozess automatisieren, indem Sie das Adressbuch für den Standardkunden des Onlineshops so konfigurieren, dass das System den Adressbuchwert für jeden neuen Kunden kopiert.

Nachdem die Kundenhierarchiedatensätze mit der Kanaldatenbank synchronisiert wurden, kann sich der Anforderer unter Verwendung der E-Mail-Adresse, die er bei der Übermittlung der Onboarding-Anforderung angegeben hat, bei der B2B-E-Commerce-Website anmelden. Benutzer können den Anmelde-Flow verwenden, um das Kennwort für ihr Konto zu definieren. Informationen zum Aktivieren des Azure Active Directory (Azure AD) B2C-Identitätsanbieterdatensatz, der mit dem B2B-Kundendatensatz verknüpft werden soll, der bei der Genehmigung des Interessenten erstellt wurde, finden Sie unter [Automatische Verknüpfung aktivieren](../identity-record-linking.md).

## <a name="notify-b2b-prospects-when-they-are-approved-or-rejected"></a>Benachrichtigen von B2B-Interessenten, wenn sie genehmigt oder abgelehnt werden

Wenn Sie eine Onboarding-Anfrage eines B2B-Interessenten genehmigen oder ablehnen, kann automatisch eine E-Mail-Benachrichtigung an den Interessenten gesendet werden.

Führen Sie die folgenden Schritte aus, um E-Mail-Benachrichtigungen in der Commerce headquarters für Ereignisse der Benachrichtigungsart **B2B-Interessent genehmigt** oder **B2B-Interessent abgelehnt** einzurichten.

1. Erstellen Sie E-Mail-Vorlagen für E-Mails, die an Interessenten gesendet werden, wenn entweder der Benachrichtigungstyp **B2B-Interessent genehmigt** oder **B2B-Interessent abgelehnt** ausgelöst wird. Informationen zu den Platzhaltern, die diese Benachrichtigungstypen unterstützen, finden Sie unter [Benachrichtigungstypen](../email-templates-transactions.md#notification-types). Informationen zum Erstellen von E-Mail-Vorlagen finden Sie unter [Erstellen einer E-Mail-Vorlage](../email-templates-transactions.md#create-an-email-template).
1. Fügen Sie die Benachrichtigungstypen **B2B-Interessenten genehmigt** und **B2B-Interessenten abgelehnt** Ihrem E-Mail-Benachrichtigungsprofil hinzu und ordnen Sie sie dann den von Ihnen erstellten E-Mail-Vorlagen zu. Weitere Informationen zu E-Mail-Benachrichtigungsprofilen finden Sie unter [Richten Sie ein E-Mail-Benachrichtigungsprofil ein](../email-notification-profiles.md).

## <a name="onboard-additional-business-partner-users"></a>Onboarding zusätzlicher Geschäftspartnerbenutzer durchführen

Der Administratorbenutzer des Geschäftspartners kann bei Bedarf weitere Benutzer des Geschäftspartners in die B2B-E-Commerce-Website integrieren.

Führen Sie die folgenden Schritte aus, um weitere Geschäftspartnerbenutzer in eine B2B-E-Commerce-Website einzubinden.

1. Melden Sie sich als Administrator auf der B2B-E-Commerce-Website an.
1. Wechseln Sie zu **Mein Konto \> Organisationsbenutzer \> Details anzeigen** und wählen Sie **Einen Benutzer hinzufügen** aus.
1. Geben Sie erforderlichen Informationen ein, und wählen Sie **Speichern** aus. Der Status des neuen Benutzers wird auf **Ausstehend** festgelegt.

Nachdem die Aufträge **P-0001** und **Kunden und Kanalanforderungen synchronisieren** ausgeführt wurden, wird für den neuen Benutzer ein Kundendatensatz vom Typ **Person** in der Commerce-Zentralverwaltung erstellt. Dieser Kundendatensatz ist auch dem Kundenhierarchiedatensatz des jeweiligen Geschäftspartners zugeordnet. Darüber hinaus wird eine E-Mail an die E-Mail-Adresse des neuen Benutzers gesendet, um ihn darüber zu informieren, dass er als Benutzer der Geschäftspartnerorganisation hinzugefügt wurde und sich jetzt auf der B2B-E-Commerce-Website anmelden kann.

Führen Sie als Nächstes den Auftrag **1010 (Kunden)** aus, um den neuen Geschäftspartnerbenutzer mit der Kanaldatenbank zu synchronisieren.

Nach der Synchronisierung des Kundendatensatzes wird der Status des Benutzers auf der B2B-E-Commerce-Website auf **Aktiv** festgelegt und der neue Benutzer kann sich unter Verwendung seiner E-Mail-Adresse bei der B2B-E-Commerce-Website anmelden. Benutzer können den Anmelde-Flow verwenden, um das Kennwort für ihr Konto zu definieren. Informationen zum Aktivieren des Azure AD B2C-Identitätsanbieterdatensatz, der mit dem B2B-Kundendatensatz verknüpft werden soll, der in der Commerce-Zentralverwaltung erstellt wurde, finden Sie unter [Automatische Verknüpfung aktivieren](/dynamics365/commerce/identity-record-linking.md).

## <a name="edit-business-partner-user-details"></a>Die Benutzerdetails des Geschäftspartners bearbeiten

Führen Sie die folgenden Schritte aus, um die Details der Benutzer von Geschäftspartnern zu bearbeiten.

1. Melden Sie sich als Administrator auf der B2B-E-Commerce-Website an.
1. Wechseln Sie zu **Mein Konto \> Organisationsbenutzer \> Details anzeigen**, wählen Sie **Bearbeiten** aus (Stiftsymbol), nehmen Sie die erforderlichen Änderungen vor und wählen Sie dann aus **Speichern**. Die Änderungen werden erst wirksam, nachdem die Aufträge **P-0001**, **Kunden und Kanalanforderungen synchronisieren** und **1010 (Kunden)** ausgeführt wurden.

## <a name="remove-a-business-partner-user"></a>Einen Geschäftspartnerbenutzer entfernen

Bei Bedarf kann ein Administrator vorhandene Benutzer einer Geschäftspartnerorganisation aus der Liste der Benutzer entfernen, die auf die B2B-E-Commerce-Website zugreifen können.
Führen Sie die folgenden Schritte aus, um einen Geschäftspartnerbenutzer zu entfernen.
- Melden Sie sich als Administrator auf der B2B-E-Commerce-Website an.
- Wechseln Sie zu **Mein Konto > Organisationsbenutzer \> Details anzeigen** und wählen Sie die Schaltfläche **Entfernen** (X-Symbol) aus. Wenn eine Bestätigungsmeldung angezeigt wird, bestätigen Sie, dass Sie den Benutzer entfernen möchten. Die Änderung wird erst wirksam, nachdem die Aufträge **P-0001**, **Kunden und Kanalanforderungen synchronisieren** und **1010 (Kunden)** ausgeführt wurden.

> [!NOTE]
> Wenn Sie einen Benutzer aus der Liste der Benutzer, die auf die B2B-E-Commerce-Website zugreifen können, entfernen, wird der entsprechende Kundendatensatz aus dem Kundenhierarchiedatensatz des Geschäftspartners entfernt. Der Kundendatensatz selbst wird jedoch nicht aus der Commerce-Zentralverwaltung gelöscht.

## <a name="onboard-existing-customers-as-business-partners-on-the-b2b-e-commerce-website"></a>Onboarding bestehender Kunden als Geschäftspartner auf der B2B-E-Commerce-Website durchführen

Administratoren können ein Onboarding von Geschäftspartnern und Benutzern direkt in der Commerce-Zentralverwaltung durchführen. Diese Funktion hilft beim Onboarding Ihrer bestehenden Geschäftspartner auf der B2B-E-Commerce-Website.

Führen Sie diese Schritte aus, um ein Onboarding von Geschäftspartnern und Benutzern in der Commerce-Zentralverwaltung durchführen.

1. Erstellen oder wählen Sie einen Kunden vom Typ **Organisation** aus, den Sie einem Geschäftspartner hinzufügen möchten.
1. Erstellen oder wählen Sie einen Kunden vom Typ **Person** aus, die Sie dem Geschäftspartner als Administrator oder Benutzer hinzufügen möchten. Stellen Sie sicher, dass mit den Kunden primäre E-Mail-Adressen verbunden sind. Diese E-Mail-Adressen werden verwendet, um sich auf der Website anzumelden. 

    > [!NOTE]
    > Das System muss in der Lage sein, einen eindeutigen Kundendatensatz für Benutzer zu finden, die sich auf der Website anmelden können sollen. Wenn das System mehr als einen Kunden findet, der in der juristischen Person dieselbe primäre E-Mail-Adresse hat, kann sich der Benutzer nicht bei der Website anmelden.

1. Erstellen Sie eine Kundenhierarchiekennung.
1. Geben Sie im Feld **Name** einen Namen ein.
1. Geben Sie im Feld **Organisation** den Geschäftspartnerorganisationskunden ein.
1. Auf dem Inforegister **Hierarchie** wählen Sie **Hinzufügen** aus.
1. Wählen Sie im Feld **Name** einen Kunden vom Typ **Person** aus.
1. Wählen Sie für die Rolle **Administrator** den Kunden aus, der als Administrator festgelegt werden soll.
1. Wiederholen Sie diesen Prozess, um der Hierarchie mehr Kunden hinzuzufügen.

## <a name="additional-information"></a>Zusätzliche Informationen

- Alle in diesem Artikel genannten Aufträge können so konfiguriert werden, dass sie nach einem Zeitplan im Stapelformat ausgeführt werden. Es wird erwartet, dass Geschäftspartner Stapelaufträge nach Bedarf konfigurieren.
- Derzeit kann nur ein Benutzer/Kundendatensatz als Administratorbenutzer festgelegt werden, und diese Rolle kann nur in der Commerce-Zentralverwaltung geändert werden. Es gibt keine Unterstützung für Self-Service-Funktionen, mit denen Geschäftspartner mehrere Administratoren bestimmen oder Administratoren von B2B-E-Commerce-Websites wechseln können.
- Obwohl Ausgabenlimits für Benutzer definiert werden können, wurde die Durchsetzung von Ausgabenlimits während des Auftragserfassungsprozesses noch nicht implementiert.
- Die gesamte Geschäftslogik und Validierung für die Benutzererfahrung auf einer B2B-E-Commerce-Website basiert auf der Konfiguration des Kundendatensatzes, der dem Benutzer in der Commerce-Zentralverwaltung zugeordnet ist.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Website für B2B-E-Commerce einrichten](set-up-b2b-site.md)

[B2B-Geschäftspartner mithilfe von Kundenhierarchien verstehen](partners-customer-hierarchies.md)

[Konfigurieren der Zahlungsmethode des Kundenkontos für B2B-E-Commerce-Websites](payment-method.md)

[Festlegen von Produktmengenbeschränkungen für B2B-E-Commerce-Websites](quantity-limits.md)

[Nummernkreise – Übersicht](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
