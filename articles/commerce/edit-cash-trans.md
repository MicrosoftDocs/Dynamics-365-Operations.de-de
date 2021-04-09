---
title: Abholungs- und Bargeldverwaltungstransaktionen bearbeiten und prüfen
description: In diesem Thema wird beschrieben, wie Abholungs- und Zahlungsmanagementtransaktionen in Microsoft Dynamics 365 Commerce bearbeitet und überwacht werden.
author: josaw1
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7a9086da036712fc8c63498d95dc9f71f32f75c6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792728"
---
# <a name="edit-and-audit-cash-and-carry-and-cash-management-transactions"></a>Abholungs- und Bargeldverwaltungstransaktionen bearbeiten und prüfen

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wie Abholungs- und Zahlungsmanagementtransaktionen in Microsoft Dynamics 365 Commerce bearbeitet und überwacht werden.

## <a name="overview"></a>Übersicht

Dynamics 365 Commerce-Kunden verwenden sowohl eine Erstanbieter-POS-Anwendung (Point-of-Sale) als auch Drittanbieter-POS-Anwendungen. Mit der POS-Anwendung von Microsoft werden Shoptransaktionen über einen Stapelverarbeitungsvorgang aus den Kanälen in die Commerce-Zentralverwaltung geholt. Bei Anwendungen von Drittanbietern werden Transaktionen über die Integration in die Commerce-Zentralverwaltung geholt. In beiden Fällen muss nach dem Abrufen von Transaktionen in die Commerce-Zentralverwaltung eine Konsistenzprüfung durchgeführt werden. Dieser Prozess führt mehrere Überprüfungen für die Transaktionen aus, wobei nur Transaktionen, die erfolgreich validiert wurden, in die Anweisung geholt werden, damit sie in der Commerce-Zentralverwaltung gebucht werden können.

Commerce-Transaktionen können aus verschiedenen Gründen die Prüfung nicht bestehen. Ein Fehler im Integrationscode oder in der POS-Anwendung kann zu inkonsistenten Daten führen. Alternativ kann ein Benutzerfehler zu inkonsistenten Daten führen. Beispielsweise löscht ein Benutzer ein Produkt, nachdem es mit dem Kanal synchronisiert wurde, oder ein Benutzer schließt einen Finanzzeitraum, ohne Transaktionen für diesen Zeitraum zu buchen. Obwohl diese Transaktionen markiert und von den Aufstellungen ausgeschlossen werden, können sie den laufenden Prozess der täglichen Buchung von Umsätzen im Rechnungswesen eines Kunden stören. In Commerce können Sie die Transaktionen bearbeiten, die die Prüfung nicht bestehen. Gleichzeitig werden alle Änderungen geprüft.

## <a name="edit-transactions"></a>Buchungen bearbeiten

In der Commerce-Version 10.0.5 sind Abholungstransaktionen wie Verkäufe und Rückgaben die einzigen Transaktionen, die bearbeitet werden können. Debitorenaufträge und Onlinebestellungen können nicht bearbeitet werden. In Commerce Version 10.0.6 und höher können auch Bargeldverwaltungstransaktionen bearbeitet werden.

Führen Sie die folgenden Schritte aus, um Transaktionen in der Commerce-Zentralverwaltung zu bearbeiten.

1. Installieren Sie das [Microsoft Dynamics Office-Add-In](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview).
1. Öffnen Sie in der Commerce-Zentralverwaltung den Arbeitsbereich **Finanzdaten für Shop**. Die Kachel **Transaktionsüberprüfungsfehler** bietet eine vorgefilterte Ansicht der Transaktionsseite, die eine oder mehrere der Überprüfungsregeln nicht bestanden hat.
1. Öffnen Sie die Transaktionsseite, wählen Sie den Datensatz aus, dessen Überprüfung fehlgeschlagen ist, wählen Sie **Office Add-In** und anschließend **Ausgewählte Transaktion bearbeiten** aus. Es öffnet sich eine Excel-Datei mit den Details der ausgewählten Transaktion. Diese Datei enthält folgende Arbeitsblätter:

    - **Positionen** – Dieses Arbeitsblatt enthält den Kopf, die Produktpositionen und die Daten der Transaktion.
    - **Zahlungen** – Dieses Arbeitsblatt enthält die Details der Zahlungspositionen der Transaktion.
    - **Rabatte** – Dieses Arbeitsblatt enthält die rabattbezogenen Details der Transaktion.
    - **Steuern** – Dieses Arbeitsblatt enthält die steuerlichen Details für die Transaktion.
    - **Gebühren** – Dieses Arbeitsblatt enthält die belastungsbezogenen Daten der Transaktion.

1. Ändern Sie die entsprechenden Felder in der Excel-Datei, und laden Sie die Daten dann mit Hilfe der Veröffentlichungsfunktion des Dynamics Excel-Add-Ins wieder in die Commerce-Zentralverwaltung hoch. Sobald die Daten veröffentlich sind, werden die Änderungen im System berücksichtigt. Während der Veröffentlichung wird keine Überprüfung der von den Benutzern vorgenommenen Änderungen durchgeführt.
1. Sie können sich ein vollständiges Protokoll der Änderungen anzeigen lassen, indem Sie **Audit-Trail anzeigen** in der **Einzelhandelstransaktion**-Kopfzeile (Änderungen auf Kopfzeilenebene) oder in den entsprechenden Abschnitt und Datensatz auswählen. Beispielsweise werden alle Änderungen, die sich auf Verkaufspositionen beziehen, auf der Seite **Verkaufstransaktionen** angezeigt, und alle Änderungen, die sich auf Zahlungen beziehen, werden auf der Seite **Zahlungstransaktionen** angezeigt. Die folgenden Prüfungsdetails werden für die Änderungen beibehalten:

    - Änderungsdatum und -uhrzeit
    - Feld
    - Alter Wert
    - Neuer Wert
    - Geändert von

1. Sobald Sie Ihre Änderungen vorgenommen und veröffentlicht haben, führen Sie die Option **Geschäftsbuchungen überprüfen** aus, um die Konsistenz und Gültigkeit der von Ihnen vorgenommenen Änderungen zu überprüfen.

> [!NOTE]
> Sie können nur Transaktionen bearbeiten, bei denen die Prüfung fehlgeschlagen ist. Wenn Sie eine Transaktion bearbeiten möchten, die die Prüfung bestanden hat, ändern Sie den Überprüfungsstatus der Transaktion in **Fehler** oder **Keine**. Veröffentlichen Sie anschließend die Änderung. Sie können dann die Daten in der Kopfzeile oder in anderen untergeordneten Datensätzen der Transaktion bearbeiten und die Kopfzeile oder die Datensätze veröffentlichen.

## <a name="bulk-edit-transactions-that-are-linked-to-a-statement"></a>Massenbearbeitung von Transaktionen, die mit einer Anweisung verknüpft sind

Ab Commerce-Version 10.0.6 und höher wird die Möglichkeit der Massenbearbeitung von Transaktionen auf Anweisungsebene unterstützt.

Führen Sie die folgenden Schritte aus, um Transaktionen, die mit einer Anweisung in der Commerce-Zentralverwaltung verknüpft sind, in großen Mengen zu bearbeiten.

1. Öffnen Sie die Seite **Anweisungen** und wählen Sie die Anweisung aus, die die Transaktionen enthält, die bearbeitet werden müssen.
1. Wählen Sie die Schaltfläche **In Microsoft Office öffnen** aus.
1. Wählen Sie, je nachdem, was bearbeitet werden muss, eine der folgenden Optionen aus:

    - **Abholungstransaktionen bearbeiten** – Mit dieser Option können Sie alle in der Anweisung enthaltenen Abholungstransaktionen bearbeiten. Folgende Excel-Arbeitsblätter sind verfügbar:

        - **Transaktion** – Dieses Arbeitsblatt enthält auf Kopfzeilenebene alle Informationen für die Verkaufstransaktionen.
        - **Verkaufstransaktion** – Dieses Arbeitsblatt enthält auf Positionsebene alle Informationen für die Verkaufstransaktionen.
        - **Zahlungstransaktionen** – Dieses Arbeitsblatt enthält alle Informationen zu den Zahlungspositionen für die Verkaufstransaktionen.
        - **Rabatttransaktionen** – Dieses Arbeitsblatt enthält alle Informationen zu den Rabattpositionen für die Verkaufstransaktionen.
        - **Steuertransaktionen** – Dieses Arbeitsblatt enthält alle Informationen zu den Steuerpositionen für die Verkaufstransaktionen.
        - **Gebührentransaktionen** – Dieses Arbeitsblatt enthält alle Informationen zu den Belastungspositionen für die Verkaufstransaktionen.

    - **Bargeldverwaltungstransaktionen bearbeiten** – Mit dieser Option können Sie alle in der Anweisung enthaltenen Bargeldverwaltungstransaktionen bearbeiten. Folgende Excel-Arbeitsblätter sind verfügbar:

        - **Transaktion** – Dieses Arbeitsblatt enthält alle Informationen auf Kopfzeilenebene für die Bargeldverwaltungstransaktionen.
        - **Bankzahlungsmitteltransaktionen**: Dieses Arbeitsblatt enthält alle Details zu den Bankeinzahlungstransaktionen.
        - **Sichere Zahlungsmitteltransaktionen** – Dieses Arbeitsblatt enthält alle Details zu sicheren Einzahlungstransaktionen.
        - **Zahlungsmitteldeklaration** – Dieses Arbeitsblatt enthält alle Details zu Zahlungsmitteldeklarationstransaktionen.
        - **Einnahmen/Ausgaben-Transaktionen** – Dieses Arbeitsblatt enthält alle Details zu Einnahmen/Ausgaben-Transaktionen.
        - **Zahlungstransaktionen** – Dieses Arbeitsblatt enthält alle zahlungsrelevanten Informationen für den **Rechnungszahlung**-Vorgang und die Einnahmen-Ausgaben-Transaktion.

1. Bearbeiten Sie die erforderlichen Transaktionen.

    > [!NOTE]
    > Wenn Sie massenbearbeitete Transaktionen veröffentlichen, werden keine Prüfungen durchgeführt. Sie müssen sicherstellen, dass Ihre Bearbeitungen korrekt sind und die Datengenauigkeit in den Arbeitsblättern erhalten bleibt. Wenn Sie beispielsweise für Szenarien, in denen der Finanzzeitraum oder die Lagerbuchungsperiode für die offenen Transaktionen abgeschlossen ist, das Transaktionsdatum ändern möchten, müssen Sie das Datum in allen Excel-Arbeitsblättern ändern, die die Spalte **Geschäftsdatum** haben. Sie können Transaktionen nach der Bearbeitung prüfen, wenn Sie **Transaktionen neu prüfen** auf der Seite **Aufstellungen** auswählen. Warten Sie, bis der Prüfungsauftrag abgeschlossen ist, bevor Sie die Anweisung buchen.

1. Wenn die Aggregation bereits generiert wurde, öffnen Sie die Seite **Aggregierte Transaktionen** und wählen Sie **Auftrags-XML neu generieren** aus.

## <a name="bulk-edit-transactions-that-arent-linked-to-a-statement"></a>Massenbearbeitung von Transaktionen, die nicht mit einer Anweisung verknüpft sind

Commerce Version 10.0.10 und höher unterstützt die Option zur Massenbearbeitung von Transaktionen, bei denen die Prüfung fehlschlägt, die jedoch nicht mit einer Anweisung verknüpft sind.

Führen Sie die folgenden Schritte aus, um Transaktionen, die nicht mit einer Anweisung in der Commerce-Zentralverwaltung verknüpft sind, in großen Mengen zu bearbeiten.

1. Öffnen Sie die Seite **Alle Shops**, und wählen Sie den Shop aus, für den Transaktionen bearbeitet werden müssen.
1. Wählen Sie die Schaltfläche **In Microsoft Office öffnen** und anschließend **Abholungstransaktionen bearbeiten** aus.
1. Bearbeiten Sie die erforderlichen Transaktionen, und veröffentlichen Sie sie anschließend.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Onlineauftrag und asynchrone Debitorenauftragstransaktionen bearbeiten und prüfen](edit-order-trans.md)

[Finanzdimensionen für Einzelhandelstransaktionen bearbeiten](edit-financial-dim.md)

[Excel-Arbeitsmappe zum Bearbeiten von Einzelhandelstransaktionen erstellen](create-excel-edit.md)

[Einer Excel-Arbeitsmappe zum Bearbeiten von Einzelhandelstransaktionen Felder hinzufügen](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]