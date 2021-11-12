---
title: Geschäftspartnerbenutzer auf B2B-E-Commerce-Websites verwalten
description: In diesem Thema wird beschrieben, wie Administratoren Geschäftspartnerbenutzer auf Business-to-Business(B2B)-E-Commerce-Websites hinzufügen, bearbeiten und löschen können.
author: josaw1
ms.date: 10/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 090dc9af49840e559b4c1ad1500718fde9764aa2
ms.sourcegitcommit: 6bf9e18989e6d77497a9dda1c362f324b3c2fbf2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2021
ms.locfileid: "7713692"
---
# <a name="manage-business-partner-users-on-b2b-e-commerce-websites"></a>Geschäftspartnerbenutzer auf B2B-E-Commerce-Websites verwalten

[!include [banner](../../includes/banner.md)]

In diesem Thema wird beschrieben, wie Administratoren Geschäftspartnerbenutzer auf Business-to-Business(B2B)-E-Commerce-Websites hinzufügen, bearbeiten und löschen können.

Für B2B-E-Commerce-Websites müssen sich Organisationen registrieren, um Geschäftspartner zu werden. Nachdem eine Organisation Registrierungsdaten an eine B2B-E-Commerce-Website übermittelt hat, durchläuft sie einen Qualifizierungsprozess. Wenn die Organisation erfolgreich qualifiziert ist, wird sie als Geschäftspartner eingebunden.

Nachdem eine Organisation als Geschäftspartner eingebunden wurde, wird der Organisationsbenutzer, der die Anforderung zum Geschäftspartner initiiert hat, als Administrator identifiziert und erhält die Berechtigung, zusätzliche autorisierte Benutzer der B2B-E-Commerce-Website einzubeziehen. Diese autorisierten Benutzer können dann im Namen des Geschäftspartners Bestellungen aufgeben.

## <a name="turn-on-the-b2b-e-commerce-capabilities-feature-in-commerce-headquarters"></a>Aktivieren Sie die Funktion für B2B-E-Commerce-Funktionen in der Commerce-Zentralverwaltung

Mit der Funktion für B2B-E-Commerce-Funktionen in der Commerce-Zentralverwaltung können Unternehmen Geschäftspartner einbeziehen und Administratorbenutzer definieren. Mit dieser Funktion können Administratoren auch Benutzer und Teams von Geschäftspartnern erstellen, verwalten und ihnen bestimmte Rollen zuweisen. Schließlich können Geschäftspartnerbenutzer Auftragsvorlagen erstellen und vorhandene Aufträge zum Nachbestellen von Produkten verwenden.

Um die Funktion für B2B-E-Commerce-Funktionen in der Commerce-Zentralverwaltung zu aktivieren, befolgen Sie diese Schritte:

1. Wechseln Sie zu **Arbeitsbereiche \> Datenverwaltung**.
1. Filtern Sie auf der **Alle**-Registerkarte im **Modul**-Feld unter Verwendung des Begriffs **Einzelhandel und Handel**.
1. Suchen Sie die Funktion namens **Die Verwendung von B2B-E-Commerce-Funktionen aktivieren** und wählen Sie sie aus. Wählen Sie dann **Jetzt aktivieren** aus.

## <a name="create-a-number-sequence-and-add-it-to-commerce-shared-parameters"></a>Eine Zahlenfolge erstellen und den gemeinsam genutzten Commerce-Parametern hinzufügen

Nummernkreise dienen zum Generieren von lesbaren, eindeutigen Bezeichnern für Masterdatensätze und Buchungsdatensätze, die Bezeichner benötigen. Weitere Informationen zu Nummernsquenzen finden Sie unter [Überblick über Nummernsequenzen](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md).

Führen Sie die folgenden Schritte aus, um eine Zahlenfolge zu erstellen und den gemeinsam genutzten Commerce-Parametern in der Commerce-Zentralverwaltung hinzuzufügen.

1. Wechseln Sie zu **Einzelhandel und Handel \> Zentralverwaltungseinrichtung \> Zahlenfolgen \> Zahlenfolgen** und erstellen Sie eine Zahlenfolge.
1. Wechseln Sie zu **Einzelhandel und Handel \>Zentralverwaltungseinrichtung \> Parameter \> Gemeinsame Commerce-Parameter** und fügen Sie die neue Zahlenfolge der **Kundenhierarchie-ID**-Referenz hinzu.

## <a name="set-up-the-administrator-user-for-a-new-business-partner"></a>Den Administratorbenutzer für einen neuen Geschäftspartner einrichten

Potenzielle Geschäftspartner können den Onboarding-Prozess für eine B2B-E-Commerce-Website initiieren, indem sie eine Onboarding-Anfrage über einen Link auf der Website senden. Nachdem ein potenzieller Geschäftspartner den Link ausgewählt hat, kann er die Details bereitstellen, die für das Onboarding und die Anmeldung erforderlich sind. Nachdem die Anfrage gesendet wurde, wird eine Bestätigungsseite für die Einreichung angezeigt. Wenn die Übermittlung genehmigt wird, wird der Anforderer (d. h. der Benutzer, der die Onboarding-Anforderung initiiert hat) zum Administrator des Geschäftspartners.

Führen Sie die folgenden Schritte aus, um einen Administratorbenutzer eines Geschäftspartners in der Commerce-Zentralverwaltung zu genehmigen und einzurichten.

1. Wechseln Sie zu **Einzelhandel und Handel \> Vertriebsplan**.
1. Führen Sie den **P-0001**-Auftrag aus, um alle Onboarding-Anfragen von Geschäftspartnern in die Commerce-Zentralverwaltung zu ziehen.
1. Nach dem der **P-0001**-Auftrag erfolgreich ausgeführt wurde, wechseln Sie zu **Einzelhandel und Handel IT \> Kunde** und führen Sie die **Kunden und Geschäftspartner im asynchronen Modus synchronisieren**-Auftrag aus. Nachdem dieser Auftrag erfolgreich ausgeführt wurde, werden die Onboarding-Anforderungen als Interessentendatensätze in der Commerce-Zentralverwaltung erstellt. Das **Typ-ID**-Feld dieser Datensätze ist auf **B2B-Interessent** festgelegt.
1. Wechseln Sie zu **Kunden \> Alle Interessenten** und öffnen Sie die Seite mit den Interessenten.
1. Wählen Sie den Interessentendatensatz für den neuen Geschäftspartner aus, um die Seite mit den Interessentendetails zu öffnen.
1. Wählen Sie auf der **Allgemein**-Registerkarte **Konvertieren \> Genehmigen/ablehnen** aus, um die Onboarding-Anfrage zu genehmigen oder abzulehnen. Wenn eine Bestätigungsmeldung angezeigt wird, bestätigen Sie, dass Sie mit dem Vorgang fortfahren möchten, und genehmigen Sie die Anforderung. Anschließend wird eine E-Mail an die E-Mail-Adresse des Anforderers gesendet, um zu bestätigen, dass seine Organisation als Geschäftspartner genehmigt wurde.

    Nachdem Sie die Anfrage genehmigt haben, wird das **Status**-Feld des Interessentendatensatzes auf **Genehmigt** festgelegt. Zusätzlich werden zwei neue Kundendatensätze im System erstellt: ein **Typ: Organisation**-Kundendatensatz für die Geschäftspartnerorganisation und ein **Typ: Person**-Kundendatensatz für den Anforderer. Ein Kundenhierarchiedatensatz für den Geschäftspartner wird ebenfalls erstellt. <!--(Please refer to the Org modeling of B2B customer section in this document for more information)-->

1. Wechseln Sie zu **Einzelhandel und Handel IT \> Verteilungsplan** und führen Sie den **1010** (**Kunden**)-Auftrag zum pushen der neu erstellten Kunden- und Kundenhierarchiedatensätze in die Kanaldatenbank aus.

Nachdem die Anfrage genehmigt und die Kunden- und Kundenhierarchiedatensätze mit der Kanaldatenbank synchronisiert wurden, kann sich der Anforderer unter Verwendung der E-Mail-Adresse, die er bei der Übermittlung der Anfrage angegeben hat, bei der B2B-E-Commerce-Website anmelden. Benutzer können den Anmelde-Flow verwenden, um das Kennwort für ihr Konto zu definieren. Um den Identitätsanbieter zu aktivieren (Azure AD B2C)-Datensatz, der mit dem B2B-Kundendatensatz verknüpft werden soll, der bei der Anmeldung oder Anmeldung erstellt wurde, folgen Sie den Anweisungen in [Aktivieren Sie die automatische Verknüpfung von Identitätsdatensätzen mit Kundenkonten](../identity-record-linking.md).

## <a name="notify-b2b-prospects-when-they-are-approved-or-rejected"></a>Benachrichtigen von B2B-Interessenten, wenn sie genehmigt oder abgelehnt werden

Wenn Sie eine Onboarding-Anfrage eines B2B-Interessenten genehmigen oder ablehnen, können Sie automatisch eine E-Mail-Benachrichtigung an den Interessenten senden. 

Führen Sie die folgenden Schritte aus, um E-Mail-Benachrichtigungen in der Commerce-Zentrale für Ereignisse der Benachrichtigungsart B2B-Interessent genehmigt oder B2B-Interessent abgelehnt einzurichten.

1. Erstellen Sie E-Mail-Vorlagen für E-Mails, die an potenzielle Kunden gesendet werden, wenn der Benachrichtigungstyp B2B-Interessent genehmigt oder B2B-Interessent abgelehnt ausgelöst wird.

    Informationen zu den Platzhaltern, die von Benachrichtigungstypen B2B-Interessenten genehmigt und vom B2B-Interessenten abgelehnt unterstützt werden, finden Sie unter [Benachrichtigungsarten](../email-templates-transactions.md#notification-types). Informationen zum Erstellen von E-Mail-Vorlagen finden Sie unter [Erstellen einer E-Mail-Vorlage](../email-templates-transactions.md#create-an-email-template). 

1. Fügen Sie die Benachrichtigungstypen B2B-Interessenten genehmigt und B2B-Interessenten abgelehnt Ihrem E-Mail-Benachrichtigungsprofil hinzu und ordnen Sie sie den von Ihnen erstellten E-Mail-Vorlagen zu. Weitere Informationen zu E-Mail-Benachrichtigungsprofilen finden Sie unter [Richten Sie ein E-Mail-Benachrichtigungsprofil ein](../email-notification-profiles.md). 

## <a name="onboard-additional-business-partner-users"></a>Onboarding zusätzlicher Geschäftspartnerbenutzer durchführen

Der Administratorbenutzer des Geschäftspartners kann bei Bedarf weitere Benutzer des Geschäftspartners in die B2B-E-Commerce-Website integrieren.

Führen Sie die folgenden Schritte aus, um weitere Geschäftspartnerbenutzer in eine B2B-E-Commerce-Website einzubinden.

1. Melden Sie sich als Administrator auf der B2B-E-Commerce-Website an.
1. Wechseln Sie zu **Mein Konto \> Organisationsbenutzer \> Details anzeigen** und wählen Sie **Einen Benutzer hinzufügen** aus.
1. Geben Sie erforderlichen Informationen ein, und wählen Sie **Speichern** aus. Der Status des neuen Benutzers wird auf **Ausstehend** festgelegt.

    Nachdem die Aufträge **P-0001** und **Kunden und Geschäftspartner im asynchronen Modus synchronisieren** ausgeführt wurden, wird Sie für den neuen Benutzer ein Kundendatensatz **Typ: Person** in der Commerce-Zentralverwaltung erstellt. Dieser Kundendatensatz ist auch dem Kundenhierarchiedatensatz des jeweiligen Geschäftspartners zugeordnet. Darüber hinaus wird eine E-Mail an die E-Mail-Adresse des neuen Benutzers gesendet, um ihn darüber zu informieren, dass er als Benutzer der Geschäftspartnerorganisation hinzugefügt wurde und sich jetzt auf der B2B-E-Commerce-Website anmelden kann.

1. Führen Sie den Auftrag **1010** (**Kunden**) aus, um den neuen Geschäftspartnerbenutzer mit der Kanaldatenbank zu synchronisieren.

Nach der Synchronisierung des Kundendatensatzes wird der Status des Benutzers auf der B2B-E-Commerce-Website auf **Aktiv** festgelegt und der neue Benutzer kann sich unter Verwendung seiner E-Mail-Adresse bei der B2B-E-Commerce-Website anmelden. Benutzer können den Anmelde-Flow verwenden, um das Kennwort für ihr Konto zu definieren. Um den Identitätsanbieter zu aktivieren (Azure AD B2C)-Datensatz, der mit dem B2B-Kundendatensatz verknüpft werden soll, der bei der Anmeldung oder Anmeldung erstellt wurde, folgen Sie den Anweisungen in [Aktivieren Sie die automatische Verknüpfung von Identitätsdatensätzen mit Kundenkonten](../identity-record-linking.md).

## <a name="edit-business-partner-user-details"></a>Die Benutzerdetails des Geschäftspartners bearbeiten

Führen Sie die folgenden Schritte aus, um die Details der Benutzer von Geschäftspartnern zu bearbeiten.

1. Melden Sie sich als Administrator auf der B2B-E-Commerce-Website an.
1. Wechseln Sie zu **Mein Konto \> Organisationsbenutzer \> Details anzeigen**, wählen Sie **Bearbeiten** aus (Stiftsymbol), nehmen Sie die erforderlichen Änderungen vor und wählen Sie dann aus **Speichern**. Die Änderungen werden erst wirksam, nachdem die Aufträge **P-0001**, **Kunden und Geschäftspartner im asynchronen Modus synchronisieren** und **1010** (**Kunden**) ausgeführt wurden.

## <a name="remove-a-business-partner-user"></a>Einen Geschäftspartnerbenutzer entfernen

Bei Bedarf kann ein Administrator vorhandene Benutzer einer Geschäftspartnerorganisation aus der Liste der Benutzer entfernen, die auf die B2B-E-Commerce-Website zugreifen können.

Führen Sie die folgenden Schritte aus, um einen Geschäftspartnerbenutzer zu entfernen.

1. Melden Sie sich als Administrator auf der B2B-E-Commerce-Website an.
1. Wechseln Sie zu **Mein Konto \> Organisationsbenutzer \> Details anzeigen** und wählen Sie die Schaltfläche **Entfernen** (X-Symbol) aus. Wenn eine Bestätigungsmeldung angezeigt wird, bestätigen Sie, dass Sie den Benutzer entfernen möchten. Die Änderung wird erst wirksam, nachdem die Aufträge **P-0001**, **Kunden und Geschäftspartner im asynchronen Modus synchronisieren** und **1010** (**Kunden**) ausgeführt wurden.

> [!NOTE]
> Wenn Sie einen Benutzer aus der Liste der Benutzer, die auf die B2B-E-Commerce-Website zugreifen können, entfernen, wird der entsprechende Kundendatensatz aus dem Kundenhierarchiedatensatz des Geschäftspartners entfernt. Der Kundendatensatz selbst wird jedoch nicht aus der Commerce-Zentralverwaltung gelöscht.

## <a name="onboard-business-partner-and-users-in-commerce-headquarters"></a>Onboarding von Geschäftspartnern und Benutzern in der Commerce-Zentralverwaltung durchführen

Administratoren können ein Onboarding von Geschäftspartnern und Benutzern direkt in der Commerce-Zentralverwaltung durchführen.

Führen Sie diese Schritte aus, um ein Onboarding von Geschäftspartnern und Benutzern in der Commerce-Zentralverwaltung durchführen.

1. Erstellen Sie einen **Typ: Organisation**-Kundendatensatz für die Geschäftspartnerorganisation.
1. Erstellen Sie **Typ: Person**-Kundendatensätze für Geschäftspartnerbenutzer. Stellen Sie sicher, dass für jeden Kunden eine primäre E-Mail-Adresse angegeben ist.
1. Für jeden **Typ: Person** -Kundendatensatz, der als Administratorbenutzer der Geschäftspartnerorganisation auf der Website angegeben werden muss, legen Sie im Inforegister **Einzelhandel** die Option **B2B-Administrator** auf **Ja** fest.
1. Erstellen Sie eine Kundenhierarchiekennung. Geben Sie im Feld **Name** einen Namen ein.
1. Geben Sie im Feld **Organisation** den Geschäftspartnerorganisationskunden ein.
1. Wählen Sie **Hinzufügen** und dann im Feld **Name** einen Kunden aus.
1. Wiederholen Sie diesen Prozess, um der Hierarchie weitere Kunden hinzuzufügen.

## <a name="additional-information"></a>Weitere Informationen

- Alle in diesem Thema genannten Aufträge können so konfiguriert werden, dass sie nach einem Zeitplan im Stapelformat ausgeführt werden. Es wird erwartet, dass Geschäftspartner Stapelaufträge nach Bedarf konfigurieren.
- Derzeit kann nur ein Benutzer/Kundendatensatz als Administratorbenutzer festgelegt werden, und diese Rolle kann nur in der Commerce-Zentralverwaltung geändert werden. Es gibt keine Unterstützung für Self-Service-Funktionen, mit denen Geschäftspartner mehrere Administratoren bestimmen oder Administratoren von B2B-E-Commerce-Websites wechseln können.
<!--- The modules and labels of the different fields referenced in the screenshots for e-commerce are only for illustration purposes. Customers have complete control on the placement of the B2B related modules and the labels.-->
- Obwohl Ausgabenlimits für Benutzer definiert werden können, wurde die Durchsetzung von Ausgabenlimits während des Auftragserfassungsprozesses noch nicht implementiert.
- Die gesamte Geschäftslogik und Validierung für die Benutzererfahrung auf einer B2B-E-Commerce-Website basiert auf der Konfiguration des Kundendatensatzes, der dem Benutzer in der Commerce-Zentralverwaltung zugeordnet ist.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Eine B2B-E-Commerce-Website einrichten](set-up-b2b-site.md)

[Erstellen von Organisationsmodellierungshierarchien für B2B-Organisationen](org-model.md)

[Konfigurieren der Zahlungsmethode des Kundenkontos für B2B-E-Commerce-Websites](payment-method.md)

[Festlegen von Produktmengenbeschränkungen für B2B-E-Commerce-Websites](quantity-limits.md)

[Nummernkreise – Übersicht](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
