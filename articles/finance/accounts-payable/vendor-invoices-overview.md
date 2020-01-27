---
title: Überblick über Kreditorenrechnungen
description: Dieses Thema enthält allgemeine Informationen zu Kreditorenrechnungen. Kreditorenrechnungen sind Zahlungsaufforderungen für Produkte und Dienste, die empfangen wurden. Kreditorenrechnungen können eine Rechnung für laufende Dienstleistungen darstellen oder auf Bestellungen für bestimmte Artikel und Dienstleistungen basieren.
author: abruer
manager: AnnBe
ms.date: 07/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13971
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 411daa5bc08df530750fd5c09ca8b54bf537b548
ms.sourcegitcommit: ba1c76497acc9afba85257976f0d4e96836871d1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/04/2019
ms.locfileid: "2890326"
---
# <a name="vendor-invoices-overview"></a>Überblick über Kreditorenrechnungen

[!include [banner](../includes/banner.md)]

Dieses Thema enthält allgemeine Informationen zu Kreditorenrechnungen. Kreditorenrechnungen sind Zahlungsaufforderungen für Produkte und Dienste, die empfangen wurden. Kreditorenrechnungen können eine Rechnung für laufende Dienstleistungen darstellen oder auf Bestellungen für bestimmte Artikel und Dienstleistungen basieren.

## <a name="vendor-invoices"></a>Kreditorenrechnungen

Eine Kreditorenrechnung für eine Bestellung ist eine Rechnung, die produziert wird, wenn Produkte oder Dienstleistungen gemäß einer vom Kreditor getätigten Bestellung zugestellt wurden. Die Kreditorenrechnung enthält eine Kopfzeile und eine oder mehrere Positionen für Artikel oder Dienstleistungen. Mit der Kreditorenrechnung wird der Zyklus aus Bestellung, Produktempfang und Kreditorenrechnung abgeschlossen.

Obwohl einige Kreditorenrechnungen mit einer Bestellung verbunden sind, können Kreditorenrechnungen auch Positionen enthalten, die nicht den Bestellpositionen entsprechen. Sie können auch Kreditorenrechnungen erstellen, die keinen Bestellungen zugeordnet sind. Diese Kreditorenrechnungen stellen möglicherweise laufende Dienstleistungen dar, wie eine Nutzungsrechnung. Wenn Sie diese hinzufügen, muß sie nicht auf eine Bestellung verweisen.

Es gibt mehrere Möglichkeiten, eine Kreditorenrechnung einzugeben:

- Über das Kreditorenrechnungsbuch können Sie schnell Rechnungen eingeben, die auf keine Bestellung verweisen, und so die Ausgaben antizipieren. Mit der Rechnungsgenehmigungserfassung für Kreditoren können Sie diese Rechnungen auswählen und als Kreditorensaldo buchen, um die Abgrenzungsbeträge zurückzusetzen.
- In der Kreditorenrechnungserfassung können Sie Rechnungen, die nicht auf eine Bestellung verweisen, schnell in einem Einzelschritt eingeben.
- Zusammen mit dem Kreditorenrechnungspool, ermöglicht Ihnen das Kreditorenrechnungsregister, Rechnungen zum Antizipieren der Ausgaben schnell zu eingeben, . Sie können die zugeordneten Bestellungen später öffnen, um die Rechnung für das Ausgabenkonto zu buchen.
- Auf den Seiten **Offene Kreditorenrechnungen** und **Ausstehende Kreditorenrechnungen** können Sie Kreditorenrechnung auf Basis bestätigter Bestellungen erstellen.

In der nachstehenden Erläuterung finden Sie weitere Informationen dazu, wie Sie **Offene Kreditorenrechnungen** oder **Ausstehende Kreditorenrechnungen** verwenden, um eine Kreditorenrechnung aus einer Bestellung zu erstellen.

## <a name="understanding-invoice-line-quantities"></a>Rechnungspositionsmengen verstehen

Wenn Sie eine Kreditorenrechnung für eine entsprechenden Bestellung öffnen, werden die Rechnungspositionen aus der Bestellung erstellt. Standardmäßig werden die Mengen aus der Produktzugangsmenge übernommen. Allerdings können Sie jedes der folgenden Standardverhalten verwenden:

- **Menge der aktuellen Lieferung** - Verwenden Sie diese Option für Teillieferungen. Der Standardwert im Feld **Menge** stammt von der Menge, die im Feld **Aktuelle Lieferung** der Bestellung angegeben ist.
- **Bestellte Menge** - Verwenden Sie diese Option für vollständige Lieferungen. Der Standardwert im Feld **Menge** stammt von der Menge, die im Feld **Bestellt** der Bestellung angegeben ist.
- **Erfasste Menge** - Verwenden Sie diese Option, wenn der Artikel erfasst werden muss, wie auf der Seite **Lagersteuerungsgruppen** angegeben. Bei dem Standardwert im Feld **Menge** handelt es sich um die registrierte physische Aktualisierungsmenge.
- **Produktzugangsmenge** – Verwenden Sie diese Option, wenn für den Auftrag bereits ein Produktzugang eingegangen ist. Beim Standardwert im Feld **Menge** handelt es sich um die Gesamtmenge der verfügbaren Produktzugänge.
- **Erfasste Menge und Services** – Verwenden Sie diese Option, wenn Mengen für gelagerte oder nicht gelagerte Artikel in der Wareneingangserfassungen registriert wurden. Diese Option schließt auch registrierte und nicht registrierte Dienstleistungen ein.

Wenn Ihre juristische Person den Rechnungsabgleich verwendet, können Sie die Ergebnisse der Menge anzeigen, die mit der Spalte **Produktzugang-Mengenabgleich** übereinstimmt. Sie können auch die Schaltfläche **Detailabgleich** auf der Registerkarte **Prüfen** des Aktivitätsbereichs verwenden, um die Ergebnisse des Mengenabgleichens anzuzeigen.

## <a name="adding-a-line-that-wasnt-on-the-purchase-order"></a>Eine Position hinzufügen, die nicht in der Bestellung war

Sie können der Kreditorenrechnung eine Position hinzuzufügen, die nicht in der Bestellung enthalten war. Sie müssen eine Artikelnummer oder eine Beschaffungskategorie auswählen. Sie können nun Mengen, Preise und Beträge der Position hinzufügen. Die Position wird nur in die Abgleichsrichtlinien für Rechnungssummen einbezogen.

## <a name="submitting-a-vendor-invoice-for-review"></a>Senden einer Kreditorenrechnung zur Prüfung

Möglicherweise werden in der Organisation Workflows zur Verwaltung des Prüfprozesses für Kreditorenrechnungen verwendet. Der Prüfungsworkflow kann für den Rechnungskopf und/oder die Rechnungsposition erforderlich sein. Die Steuerelemente des Workflows werden je nachdem, worauf der Fokus beim Auswählen auf das Steuerelement lag, auf die Kopfzeile oder die Position angewendet. Statt der Schaltfläche **Buchen** finden Sie eine **Übermitteln** Schaltfläche, die Sie verwenden können, um die Kreditorenrechnung durch den Prüfprozess zu senden.

## <a name="matching-vendor-invoices-to-product-receipts"></a>Abgleichen von Kreditorenrechnungen mit Produktzugängen

Sie können Informationen zu Kreditorenrechnungen eingeben und speichern, und Sie können Rechnungspositionen mit Produktzugangspositionen abgleichen. Für eine Position können auch Teilmengen abgeglichen werden.

Sie können eine Kreditorenrechnung basierend auf den über das aktuelle Datum empfangenen Artikeln der Produktzugangspositionen erstellen, auch wenn noch nicht alle Artikel einer bestimmten Bestellung eingegangen sind. Das kann der Fall sein, wenn ein Kreditor monatlich eine Rechnung sendet, um alle Lieferungen abzudecken, die während des betreffenden Monats geliefert wurden. Jeder Produktzugang stellt eine teilweise oder vollständig abgeschlossene Artikellieferung für die Bestellung dar.

Durch Buchen der Rechnung wird die Menge des **Rechnungsrestbetrags** jedes Artikels mit der Summe der eingegangenen Mengen aus den ausgewählten Produktzugängen aktualisiert. Wenn sowohl die Menge für den **Rechnungsrestbetrag** als auch die Menge **Rest liefern** für alle Artikel des Auftrags gleich 0 (Null) ist, wird der Status der Bestellung zu **In Rechnung gestellt** geändert. Ist die Menge des **Rechnungsrestbetrags** nicht 0 (Null), bleibt der Status der Bestellung unverändert, und es können weitere Rechnungen für den Auftrag erstellt werden.

Für die folgende Option wird vorausgesetzt, dass für die Bestellung mindestens ein Produktzugang gebucht wurde. Die Kreditorenrechnung basiert auf diesen Produktzugängen und enthält die auf den Lieferscheinen angegebenen Mengen. Die Finanzinformationen für die Rechnung basieren auf den beim Buchen der Rechnung eingegebenen Informationen.

Weitere Informationen finden Sie unter [Eingang von Kreditorenrechnungen erfassen und mit dem Wareneingang abgleichen](../accounts-payable/tasks/record-vendor-invoice-match-against-received-quantity.md).

## <a name="working-with-multiple-invoices"></a>Arbeiten mit mehreren Rechnungen

Mehrere Rechnungen können zur gleichen Zeit bearbeitet und gleichzeitig gebucht werden. Wenn Sie mehrere Rechnungen erstellen müssen, verwenden Sie die Seite **Ausstehende Kreditorenrechnungen**. Wenn sie mehrere Kreditorenrechnungen buchen und drucken müssen, verwenden Sie die Rechnungsgenehmigungserfassung. Wenn Sie die Rechnungsgenehmigungserfassung verwenden, muss mindestens ein Produktzugang der Bestellung und eine Rechnung für die Bestellung in einem Rechnungsbuch gebucht sein. Die Finanzdaten für die Rechnung stammen aus der im Register gebuchten Rechnung.

## <a name="recovering-vendor-invoices-that-are-being-used"></a>Wiederherstellen von Kreditorenrechnungen, die gerade verwendet werden

Während eine Kreditorenrechnung verwendet wird, kann sie von keinem anderen Benutzer bearbeitet werden. Allerdings könnte der Zustand einer Rechnung manchmal anzeigen, dass die Rechnung gerade verwendet wird, auch wenn diese nicht aktiv bearbeitet wird. Beispielsweise antwortet die Anwendung möglicherweise nicht mehr, weil die Rechnung bearbeitet wurde, oder weil ein Benutzer möglicherweise versehentlich die Rechnung in der Anwendung offen gelassen hat.

Sie können die Seite **Kreditorenrechnung wiederherstellen** verwenden, um Kreditorenrechnungen wiederherzustellen oder freizugeben, die mehr als vier Stunden verwendet wurden, sodass sie bearbeitet werden können. Sie können diese Seite in der Navigation **Periodische Aufgabe** oder eine Kachel im Feld **Kreditorenrechnungseintrag** im Arbeitsbereich öffnen. Nachdem die Rechnung wiederhergestellt ist, wird sie zur Verarbeitung auf der Seite **Kreditorenrechnung** verfügbar.

Auf die Seite **Wiederherstellen von Kreditorenrechnungen** kann nur zugegriffen werden, wenn die Sicherheitsberechtigung und die Rechte für das **Wiederherstellen der Kreditorenrechnungen in Bearbeitung** Ihnen zugewiesen wurde. Zudem muss der Parameter **Zulassen der Kreditorenrechnungswiederherstellung** auf der Seite **Kreditorenkontenparameter** aktiviert werden.

## <a name="resetting-the-workflow-status-for-vendor-invoices-from-unrecoverable-to-draft"></a>Zurücksetzen des Workflowstatus für Kreditorenrechnungen von „Nicht behebbar“ zu „Entwurf“

Eine Workflowinstanz, die aufgrund eines nicht behebbaren Fehlers beendet wurde, hat ein Workflowstatus **Nicht behebbar**. Wenn der Status eines Kreditorenrechnungsworkflows **Nicht behebbar** ist, können Sie ihn auf **Entwurf** zurücksetzen, indem Sie **Rückruf** auswählen. Sie können dann die Kreditorenrechnung bearbeiten. Diese Funktion ist verfügbar, wenn der Parameter **Entwurfsstatus für den Kreditorenrechnungs-Workflow zurücksetzen** auf der Seite **Funktionsverwaltung** aktiviert ist.

Sie können die Seite **Workflowhistorie** verwenden, um den Workflowstatus auf **Entwurf** zurückzusetzen. Sie können diese Seite über **Kreditorenrechnung** oder die Navigation **Allgemein > Abfragen > Workflow** öffnen. Um den Workflowstatus auf **Entwurf** zurückzusetzen, wählen Sie **Rückruf** aus. Sie können den Workflowstatus auch auf „Entwurf“ zurücksetzen, indem Sie die Aktivität **Rückruf** auf der Seite **Kreditorenrechnung** oder **Ausstehende Kreditorenrechnungen** auswählen. Nachdem der Workflowstatus auf **Entwurf** zurückgesetzt ist, wird er zur Verarbeitung auf der Seite **Kreditorenrechnung** verfügbar.



## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Kreditorenrechnungsrichtlinien einrichten](../accounts-receivable/tasks/set-up-vendor-invoice-policies.md)
- [Entscheidende Rechnungsdaten im Kreditorensystem mithilfe der Kreditorenrechnung](tasks/key-invoice-data-ap-system-vendor-invoice.md)
- [Rechnungsdaten mit einer Genehmigungserfassung in Kreditorenkonten eingeben](tasks/key-invoice-data-into-ap-system-approval-journal.md)
- [Rechnungsdaten mit dem Rechnungspool in das Kreditorensystem eingeben](tasks/key-invoice-data-into-ap-system-invoice-pool.md)
- [Eine Kreditorenrechnung in der Rechnungserfassung erfassen](tasks/record-vendor-invoice-invoice-journal.md)
