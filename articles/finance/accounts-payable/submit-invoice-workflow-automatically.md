---
title: Rechnungen an das Workflow-System senden und Produktzugangspositionen abgleichen (Vorschau)
description: In diesem Thema wird erläutert, wie Lieferantenrechnungen an das Workflow-System gesendet und gebuchte Produktzugangspositionen automatisch mit Lieferantenrechnungen abgeglichen werden.
author: abruer
manager: AnnBe
ms.date: 09/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: cde164ee89b542d769d81d8d483049fb7ca001c4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4443417"
---
# <a name="submit-invoices-to-the-workflow-system-and-match-product-receipt-lines-preview"></a>Rechnungen an das Workflow-System senden und Produktzugangspositionen abgleichen (Vorschau)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

In diesem Thema wird erläutert, wie Lieferantenrechnungen an das Workflow-System gesendet und gebuchte Produktzugangspositionen automatisch mit Lieferantenrechnungen abgeglichen werden.

## <a name="submitting-imported-vendor-invoices-to-the-workflow-system-and-matching-posted-product-receipt-lines-to-pending-vendor-invoice-lines"></a>Senden importierter Lieferantenrechnungen an das Workflow-System und Abgleichen der gebuchten Produktzugangspositionen mit ausstehenden Lieferantenrechnungszeilen

Im Rahmen eines berührungslosen Rechnungsstellungsprozesses für Kreditorenkonten können Sie das System automatisch eine importierte Rechnung an das Workflowsystem senden lassen. Sie können den Prozess zum Übermitteln importierter Rechnungen an das Workflow-System auf der Registerkarte **Automatisierung von Lieferantenrechnungen** der Seite **Kreditorenkontoparameter** (**Kreditorenkonten \> Setup\> Kreditorenparameter**) konfigurieren. Der Submit-to-Workflow-Prozess wird im Hintergrund mit einer von Ihnen angegebenen Häufigkeit (entweder stündlich oder täglich) ausgeführt.

Wenn Sie Rechnungen automatisch an das Workflow-System senden, müssen Sie mit einer importierten Rechnung beginnen. Um sicherzustellen, dass die Rechnung ohne manuellen Eingriff von Anfang bis Ende verarbeitet werden kann, müssen Sie eine automatisierte Buchungsaufgabe in die Workflow-Konfiguration aufnehmen. Rechnungen, die sich auf Bestellungen beziehen, sowie Rechnungen, die eine Beschaffungskategorie ohne Bestellung und nicht vorrätige Positionen enthalten, können automatisch an das Workflow-System gesendet werden. Manuell eingegebene Rechnungen müssen manuell an das Workflow-System gesendet werden.

Der Wert **Eingereicht von** im Workflow ist die Benutzer-ID, die für die Hintergrundaufgabe **Kreditorenrechnungen an Workflow einreichen** auf der Seite **Prozessautomatisierung** eingegeben wurde. Der Benutzer mit dieser Benutzer-ID kann die Rechnung nach Bedarf aus dem Workflow-System abrufen.

## <a name="matching-posted-product-receipts-to-invoice-lines-that-have-a-three-way-matching-policy"></a>Abgleich gebuchter Produktzugänge mit Rechnungsposten, für die eine dreiseitige Abgleichsrichtlinie gilt

Im Rahmen eines berührungslosen Rechnungsstellungsprozesses für Kreditorenkonten kann das System gebuchte Produktzugänge automatisch Rechnungspositionen zuordnen. Für diese Aufgabe muss eine dreiseitige Abgleichsrichtlinie definiert werden. Diese Funktion ist verfügbar, wenn die Funktion **Automatisierung von Lieferantenrechnungen** auf der Seite **Funktionsverwaltung** aktiviert wurde.

Der Prozess wird ausgeführt, bis die abgeglichene Produktzugangsmenge der Rechnungsmenge entspricht. Im Rahmen dieses Prozesses können Sie für das System die maximale Anzahl der versuchten Abgleiche der Produktzugänge mit einer Rechnungsposition festlegen, bevor das System zu dem Schluss kommt, dass der Prozess fehlgeschlagen ist. Der Prozess wird entweder stündlich oder täglich im Hintergrund ausgeführt. Sie können den automatisierten Abgleichprozess im Rahmen des Prozesses zum Senden von Rechnungen an das Workflowsystem ausführen. Alternativ können Sie den Prozess auch als eigenständigen Prozess ausführen. Die Einstellungen für den Abgleich von Produktzugängen mit Rechnungspositionen werden auf der Registerkarte **Automatisierung von Kreditorenrechnungen** der Seite **Kreditorenkontenparameter** konfiguriert (**Kreditorenkonten \> Setup \> Kreditorenkontenparameter**).

Rechnungsposten mit einer dreiseitige Abgleichsrichtlinie, bei der die abgeglichene Zugangsmenge geringer als die Rechnungsmenge ist, werden in den automatisierten Abgleich von Produkt zum Produktzugang einbezogen.

Zum Anzeigen des Status **Letzter Abgleich** für Rechnungen, die nicht Teil des automatisierten Submit-to-Workflow-Prozesses sind, öffnen Sie die Rechnung über die Seite **Kreditorenrechnungen**. Wenn Sie die Rechnung anzeigen, werden die abgeglichenen Validierungsinformationen aktualisiert.

Eine Rechnungsposition wird von der automatisierten Verarbeitung ausgeschlossen, wenn eine der folgenden Bedingungen erfüllt ist:

- Der Wert **Status des automatisierten Zugangsabgleichs** der Rechnungsposition ist **Fehlgeschlagen**.
- Die Rechnung wird verwendet.
- Die Rechnung befindet sich im Workflow-System.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]