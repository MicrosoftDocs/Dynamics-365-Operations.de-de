---
title: Einrichten Inkassi
description: In diesem Artikel wird beschrieben, wie Inkassofunktionen eingerichtet werden.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustCollectionsActivitiesListPage
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14031
ms.assetid: dcc6da2f-9af5-4f1d-abaa-b72967b66979
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 58d3e7f66ab5816849d393098d073ea7629e6b7c
ms.sourcegitcommit: 6a70f9ac296158edd065d52a12703b3ce85ce5ee
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3013162"
---
# <a name="set-up-collections"></a>Einrichten Inkassi

[!include [banner](../includes/banner.md)]

In diesem Artikel wird beschrieben, wie Inkassofunktionen eingerichtet werden. Sie müssen einige Einrichtungsschritte ausführen, wenn Sie die Inkassofähigkeit verwenden. Es gibt auch einige optionale Funktionen, einschließlich Debitorenpools und Inkassoteams. 

- Zahlungsfristdefinitionen
- Fälligkeitsmomentaufnahmen
- Journale
- Ursachencode für Abschreibungsbuchungen
- Inkassobeauftragte
- Abschreibungskonto
- Information: Keine Deckung
- Outlook-Einstellungen für Benutzer, die die Seite **Inkassi** verwenden
- E-Mail-Adressen

Diese Punkte werden im weiteren Verlauf dieses Themas ausführlicher behandelt. 

<a name="set-up-aging-period-definitions"></a>Zahlungsfristdefinitionen einrichten
-------------------------------

Eine Zahlungsfristdefinition einrichten. Eine Zahlungsfristdefinition legt die in den Listenseiten **Saldenrückblick**, **Inkassoaktivitäten** und **Inkassofälle** angezeigten Spalten fest. Sie definiert auch die Perioden, die auf der Seite **Inkassi** angezeigt werden. Beim Einrichten eines Debitorenpools wird die Zahlungsfristdefinition für den Pool verwendet. Werden keine Pools eingerichtet, wird die standardmäßige Zahlungsfristdefinition verwendet, die auf der Seite **Debitorenparameter** angegeben ist. Ist keine standardmäßige Zahlungsfristdefinition angegeben, wird die erste Zahlungsfristdefinition auf der Seite **Zahlungsfristdefinitionen** verwendet.

## <a name="create-an-aging-snapshot"></a>Erstellen einer Fälligkeitsmomentaufnahme
Sie können Datensätze mit einer Fälligkeitsmomentaufnahme für alle Debitoren oder für die Debitoren in einem Debitorenpool erstellen. Informationen zu Fälligkeitsmomentaufnahmen werden auf der Listenseite **Saldenrückblick** und auf der Seite **Inkassi** angezeigt. Sie müssen zuerst eine Fälligkeitsmomentaufnahme erstellen, bevor Sie die Listenseite verwenden können. Auf der Listenseite werden nur Informationen für Debitoren angezeigt, für die eine Fälligkeitsmomentaufnahme erstellt wurde.

## <a name="optional-set-up-customer-pools"></a>Optional: Einrichten von Debitorenpools
Sie können Debitorenpools für Gruppen von Debitoren einrichten. Auf den Listenseiten **Inkassi**, auf der Seite **Inkassi** oder beim Erstellen von Fälligkeitsmomentaufnahmen können Debitorenpools als Filter für Debitoreninformationen verwendet werden.

## <a name="optional-create-a-collections-team"></a>Optional: Erstellen eines Inkassoteams
Wenn mehrere Personen in der Organisation mit Inkassi beschäftigt sind, können Sie ein Inkassoteam einrichten. Sie können das Team auf der Seite **Debitorenparameter** auswählen. Wenn Sie kein Inkassoteam erstellen, wird beim Einrichten von Inkassobeauftragten auf der Seite **Inkassobeauftragter** automatisch ein Team erstellt.

## <a name="set-up-a-collections-case-category"></a>Einrichten einer Kategorie für Inkassoanfragen
Wenn Sie Ihre Inkassoaktivitäten nach Anfragen organisieren, richten Sie eine Anfragenkategorie mit dem Kategorietyp **Inkassi** ein. Diese Einrichtung ist nur erforderlich, wenn Sie die Anfragefunktion auf der Seite **Inkassi** verwenden möchten.

## <a name="set-up-journal-names-settlement-writeoff-and-nsf"></a>Einrichten von Journalen (Ausgleich, Abschreibung und KD)
Richten Sie die Namen der Erfassungen ein, die verwendet werden, wenn Buchungen auf der Seite **Inkassi** verarbeitet werden. Zu dieser Verarbeitung gehören der Ausgleich einer Buchung, das Abschreiben einer Buchung und das Verarbeiten einer Zahlung ohne ausreichende Deckung.

| Beschreibung | Journaltyp     |
|-------------|------------------|
| Ausgleich  | Debitorenzahlung |
| Abschreiben   | Täglich            |
| KD         | Debitorenzahlung |

## <a name="set-up-a-reason-code-for-writeoff-transactions"></a>Einrichten eines Ursachencodes für Abschreibungsbuchungen
Richten Sie den Standardursachencode ein, der verwendet wird, wenn Buchungen auf die Seite **Inkassi** abgeschrieben werden. Sie können den Code während des Tilgungsprozesses ändern.

## <a name="set-up-a-folder-for-email-attachments-and-create-email-templates"></a>Einrichten eines Ordners für E-Mail-Anhänge und Erstellen von E-Mail-Vorlagen
Wenn Sie E-Mail-Nachrichten von der Seite **Inkasso** senden, die Microsoft Excel-Anlagen haben, können Sie optionale E-Mail-Vorlagen für diese Nachrichten erstellen.

## <a name="set-up-accounts-receivable-parameters-for-collections"></a>Einrichten von Debitorenparametern für Inkassi
Richten Sie die Debitorenparameter ein, die auf der Registerkarte **Inkassi** erscheinen.

## <a name="optional-set-up-collections-agents"></a>Optional: Einrichten von Inkassobeauftragten
Wenn mehrere Personen in der Organisation mit Inkassi beschäftigt sind, können Sie Inkassobeauftragte einrichten. Inkassobeauftragte sind Arbeitskräfte, die auf der Seite **Benutzerbeziehungen** als Benutzer eingerichtet sind. Sie können Inkassobeauftragten zur besseren Strukturierung ihrer Arbeit Debitorenpools (Debitorenanfragen) zuweisen. Die Inkassobeauftragten werden dem Team hinzugefügt, das auf der Seite **Debitorenparameter** ausgewählt ist. Ist auf dieser Seite kein Team ausgewählt, wird automatisch ein neues Team mit dem Namen **Inkassi** erstellt, und die Inkassobeauftragten werden diesem Team hinzugefügt.

## <a name="set-up-a-writeoff-account"></a>Einrichten eines Abschreibungskontos
Richten Sie das Abschreibungskonto ein, das beim Abschreiben einer Buchung für den Hauptbuch-Abschreibungseintrag verwendet werden soll. Dieses Konto wird im Debitoren-Buchungsprofil gespeichert.

## <a name="set-up-nsf-information-for-bank-accounts"></a>Einrichten von KD-Informationen für Bankkonten
Aktualisieren Sie Bankkonten, sodass sie die richtige Erfassung haben, wenn NSF-Zahlungen auf der Seite **Inkassi** identifiziert werden. Wählen Sie auf der Registerkarte **Währungsverwaltung** im Feld **KD-Zahlungserfassung** eine Zahlungserfassung aus.

## <a name="set-up-outlook-settings-for-users-of-the-collections-page"></a>Einrichten von Outlook-Einstellungen für Benutzer der Seite "Inkassi"
Damit Arbeitskräfte mit der Seite **Inkasso** Aktivitäten erstellen oder E-Mail-Nachrichten senden können, müssen Sie zuerst sicherstellen, dass der Konfigurationsschlüssel **Microsoft Outlook-Synchronisierung** ausgewählt und die Outlook-Synchronisierung für diese Arbeitskräfte eingerichtet ist.

## <a name="set-up-email-and-addresses"></a>E-Mail und Adressen einrichten
Mithilfe von E-Mail können Sie mit Kunden und Verkäufern über Inkassoprobleme kommunizieren, um E-Mail-Nachrichten von der Seite **Inkassi** zu senden. 

### <a name="set-up-email-and-address-settings-for-collections-customer-contacts"></a>Einrichten von E-Mail-Einstellungen für Inkassokontakte von Debitoren
Richten Sie E-Mail-Adressen für Debitorenkontakte ein, wenn Sie mit der Seite **Inkassi** E-Mail-Nachrichten an diese Kontakte senden möchten. Der Inkassokontakt wird als Standardkontakt auf der Seite **Inkassi** verwendet. Sie können eine Adresse für Aufstellungen einrichten, wenn der Debitor Aufstellungen unter einer anderen als der primären Adresse erhalten soll. 

Wählen Sie auf dem Inforegister **Kredit und Inkasso** für einen Debitor im Feld **Kontakt für Inkasso** die Person in der Organisation des Debitors aus, die mit Ihrem Inkassobeauftragten zusammenarbeitet. Diese Person wird als Standardkontakt auf der Seite **Inkassi** verwendet und ist der Empfänger der E-Mail-Nachrichten. 

> [!NOTE] 
> Wenn kein Inkassokontakt für einen Debitor angegeben ist, wird der Primärkontakt für den Debitor verwendet. Falls kein Primärkontakt angegeben ist, werden E-Mails an die erste Adresse auf der Seite **Kontakte** gesendet.

### <a name="set-up-email-settings-for-salespeople"></a>Einrichten von E-Mail-Einstellungen für Verkäufer
Richten Sie E-Mail-Adressen für Verkäufer ein, wenn Sie mit der Seite **Inkassi** E-Mail-Nachrichten an Verkäufer senden möchten. Richten Sie für jeden Verkäufer in allen Provisionsverkaufsgruppen eine E-Mail-Adresse ein. Der Verkäufer, für den die Option **Kontakt** aktiviert ist, fungiert als Standardverkäufer, an den E-Mail-Nachrichten gesendet werden. 

Ist kein Verkäufer angegeben, wird der primäre Verkäufer für die Organisation des Debitors verwendet. Falls kein primärer Verkäufer angegeben ist, werden E-Mails an den ersten auf der Seite aufgeführten Verkäufer gesendet.


Weitere Informationen finden Sie in folgenden Themen:

 - [Mahnschreibensequenzen einrichten](tasks/create-collection-letter-sequence.md)

 - [Mahnschreiben verarbeiten](tasks/process-collection-letters.md)

 - [Inkassoinformationen überprüfen](tasks/review-collections-information.md)

