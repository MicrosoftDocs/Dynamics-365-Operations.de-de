---
title: Überblick über automatisierte Kreditorenabrechnungsprozesse
description: In diesem Artikel werden die Funktionen zur Automatisierung der Verarbeitung Ihrer Kreditorenrechnungen und die Vorteile der Verwendung eines automatisierten Prozesses beschrieben.
author: abruer
ms.date: 02/12/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-30
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: d2c629ed2d064a3350ec8ffe53940098d12ab0b5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883444"
---
# <a name="automated-vendor-invoicing-processes-overview"></a>Überblick über automatisierte Kreditorenabrechnungsprozesse

[!include [banner](../includes/banner.md)]

In diesem Artikel werden die Funktionen zur Automatisierung der Verarbeitung Ihrer Kreditorenrechnungen und die Vorteile der Verwendung eines automatisierten Prozesses beschrieben. Die Funktionen hierfür werden in der Funktionsverwaltung aktiviert. Diese Funktionen gelten nur für Kreditorenrechnungen, nicht für Rechnungen, die mit der **Rechnungserfassung** oder der Seite **Rechnungsbucherfassung** verarbeitet werden.

Organisationen arbeiten häufig mit Dritten zusammen, um Papierrechnungen mithilfe einer optischen Zeichenerkennung (OCR) von einem Dienstanbieter zu verarbeiten. Vom Dienstanbieter erhalten sie dann maschinenlesbare Rechnungsmetadaten. Um die Automatisierung zu unterstützen, können Sie mit den Automatisierungsfunktionen für die Kreditorenkonten diese Artefakte aus den Kreditorenkonten verwenden.

Sie können einige Kreditorenabrechnungsprozesse für Kreditorenkonten automatisieren. Diese Prozesse umfassen das Übermitteln importierter Kreditorenrechnungen an das Workflowsystem und das Abgleichen der gebuchten Produktzugangspositionen mit ausstehenden Kreditorenrechnungspositionen. Der automatisierte Prozess zeigt Informationen über den Fortschritt einer Kreditorenrechnung an, während diese die einzelnen Prozesse durchläuft. Diese Funktion kann Sachbearbeitern und Mangern von Kreditorenkonten helfen, Kreditorenrechnungen effizienter zu bearbeiten. Sie trägt auch dazu bei, die Fehler und Ineffizienzen zu reduzieren, die bei der manuellen Eingabe und Verarbeitung von Informationen auftreten können.

Die Automatisierungsprozesse können verwendet werden, um folgende Aufgaben auszuführen:

- Vorauszahlung für Kreditorenrechnungen automatisch anwenden
- Senden Sie importierte Rechnungen automatisch an das Workflowsystem.
- Gleichen Sie Produktzugänge mit ausstehenden Kreditorenrechnungspositionen ab.
- Simulieren Sie die Buchung, bevor eine Kreditorenrechnung gebucht wird.
- Zeigen Sie schnell und effizient den Workflow- und Automationsverlauf an.
- Zeigen Sie die Ergebnisse der Automatisierung der Verarbeitung von Kreditorenrechnungen an und analysieren Sie sie.
- Setzen Sie die automatisierte Verarbeitung für mehrere Rechnungen fort.

## <a name="submit-imported-vendor-invoices-to-the-workflow-system"></a>Importierte Kreditorenrechnungen an das Workflowsystem senden

Als Teil eines berührungslosen Rechnungsstellungsprozesses für Debitorenrechnungen kann eine importierte Rechnung automatisch an das Workflow-System gesendet werden. Der Prozess wird im Hintergrund mit einer von Ihnen angegebenen Häufigkeit (entweder stündlich oder täglich) ausgeführt. Um importierte Rechnungen automatisch an das Workflowsystem senden zu können, muss Ihr Prozess mit einer importierten Rechnung beginnen. Um sicherzustellen, dass die Rechnung ohne manuellen Eingriff von Anfang bis Ende verarbeitet werden kann, muss eine automatisierte Buchungsaufgabe in der Workflowkonfiguration enthalten sein.


Rechnungen, die sich auf Bestellungen beziehen, sowie Rechnungen, die eine Beschaffungskategorie ohne Bestellung und nicht vorrätige Positionen enthalten, können automatisch an das Workflow-System gesendet werden. Rechnungen, die manuell eingegeben werden, und Rechnungen, die mit dem Arbeitsbereich **Kreditorkooperationsrechnungen** erstellt werden, müssen manuell an das Workflowsystem gesendet werden. Die Bearbeitung von Vorauszahlungsanträgen muss für importierte Rechnungen manuell durchgeführt werden. Sie können Vorauszahlungen vor oder nach dem Buchen der importierten Rechnung manuell vornehmen. Sie können Vorauszahlungen manuell auf nicht gebuchte Standardrechnungen anwenden, indem Sie die Seite **Kreditorenrechnungen** verwenden. Nach der Buchung steht die abgerechnete Vorauszahlung zur Verfügung, um sie manuell auf andere Rechnungen dieses Lieferanten auf der Seite **Kreditor** anzuwenden (**Kreditorenkonten \> Allgemein \> Kreditoren \> Alle Kreditoren \> Rechnungsregisterkarte \> Anwenden**).

Die Automatisierungsfunktion stellt ein flexibles Framework bereit, mit dem Sie unternehmensspezifische Regeln für das Senden importierter Kreditorenrechnungen an das Workflowsystem und das Abgleichen gebuchter Produktzugangspositionen mit ausstehenden Kreditorenrechnungspositionen definieren können.

## <a name="match-product-receipts-to-invoice-lines-that-have-a-three-way-matching-policy"></a>Produktzugänge mit Rechnungsposten abgleichen, für die eine dreiseitige Abgleichsrichtlinie gilt

Gebuchte Produktzugänge können automatisch mit Rechnungszeilen abgeglichen werden, für die eine Richtlinie für den dreifachen Abgleich definiert ist. Der Prozess wird ausgeführt, bis die abgeglichene Produktzugangsmenge der Rechnungsmenge entspricht. Im Rahmen dieses Prozesses können Sie für das System die maximale Anzahl der versuchten Abgleiche der Produktzugänge mit einer Rechnungsposition festlegen, bevor das System zu dem Schluss kommt, dass der Prozess fehlgeschlagen ist. Der Prozess wird entweder stündlich oder täglich im Hintergrund ausgeführt. Sie können den automatisierten Abgleichprozess im Rahmen des Prozesses zum Senden von Rechnungen an das Workflowsystem ausführen. Alternativ können Sie den Prozess auch als eigenständigen Prozess ausführen.

## <a name="pre-validate-vendor-invoice-posting"></a>Buchung der Kreditorenrechnung vorab überprüfen

Die Buchungssimulation schließt die Prüfungsschritte ab, die während des Buchungsprozesses für Kreditorenrechnungen ausgeführt werden. Dabei werden jedoch keine Konten aktualisiert. Um den Prozess auszuführen, können Sie auf der Seite **Ausstehende Kreditorenrechnungen** entweder eine einzelne Rechnung oder mehrere Rechnungen auswählen.

## <a name="enhanced-experience-for-viewing-workflow-and-automation-historical-information-for-vendor-invoices"></a>Verbesserte Erfahrung beim Anzeigen von Informationen aus der Workflow- und Automatisierungshistorie für Kreditorenrechnungen

Es wird eine übersichtliche Ansicht der Workflowhistorie der Kreditorenrechnung bereitgestellt. Auf die Ansicht der Workflowhistorie kann direkt über die Kreditorenrechnung zugegriffen werden. Daher sind weniger Mausklicks erforderlich, um diese Informationen zu finden. Wenn Ihre Organisation die Möglichkeit aktiviert hat, importierte Kreditorenrechnungen automatisch an den Workflow zu senden, wird der Automationsverlauf für die importierten Rechnungen bereitgestellt. Mithilfe des Automationsverlaufs können Sie den aktuellen Prozessschritt sowie die bereits abgeschlossenen Schritte identifizieren. Wenn ein Schritt nicht erfolgreich ist, werden detaillierte Informationen angezeigt, damit Sie den Grund für den Fehler nachvollziehen können.

## <a name="analytics-and-metrics"></a>Analysen und Metriken

Der Arbeitsbereich **Kreditorenrechnungseintrag** ermöglicht die Fokussierung auf Kreditorenrechnungen, die den automatisierten Prozess nicht durchlaufen haben. Kacheln im Arbeitsbereich enthalten Informationen zu Kreditorenrechnungen, die nicht erfolgreich an das Workflowsystem gesendet, importiert oder mit Produktzugängen abgeglichen wurden. Darüber hinaus werden Microsoft Power BI-Metriken bereitgestellt, um den Managern von Kreditorenkonten einen Einblick in die Effizienz der Automatisierung von Kreditorenrechnungen zu geben.


## <a name="resume-automation-processing-for-multiple-invoices"></a>Automatisierte Verarbeitung für mehrere Rechnungen fortsetzen

Wenn eine importierte Rechnung mit dem automatisierten Prozess nicht erfolgreich an den Workflow gesendet wird, wird sie vom System aus der weiteren automatisierten Verarbeitung entfernt. Ein Kreditorenbuchhalter kann die Rechnung überprüfen und bearbeiten, bevor der automatisierte Prozess sie erneut an den Workflow übermittelt. Wenn ein Fehlergrund durch dieselbe Behebung für mehrere Rechnungen behoben werden kann, können Sie den automatisierten Prozess auf der Seite **Automatisierte Rechnungsverarbeitung fortsetzen** neu starten. 

## <a name="tracking-the-invoice-received-date-value"></a>Wert des Rechnungseingangsdatums verfolgen

Der Wert **Rechnungseingangsdatum** gibt das Datum an, an dem das Unternehmen die Rechnung vom Lieferanten erhalten hat. Es bietet einen Ausgangspunkt für die Verfolgung des Rechnungsfortschritts während der Automatisierungsprozesse. Dieser Wert kann in die importierten Daten für eine Kreditorenrechnung aufgenommen werden. Für Rechnungen, die manuell erstellt wurden, können Sie das Datum angeben. Wenn kein Wert eingegeben wird, wird standardmäßig das aktuelle Datum verwendet.


## <a name="tracking-the-imported-invoice-amount-and-imported-sales-tax-amount-values"></a>Nachverfolgung der Werte für den importierten Rechnungsbetrag und den importierten Umsatzsteuerbetrag

Die Werte **Importierter Rechnungsbetrag** und **Importierter Umsatzsteuerbetrag** für Kreditorenrechnungen können in der Importdatei für Kreditorenrechnungen angegeben werden. In der Regel stammen diese Werte aus einer Rechnung, die von einem externen Anbieter gescannt und in die Importdatei aufgenommen wurde. Wenn die Rechnung in den Debitorenrechnungen verarbeitet wird, werden die Werte auf der Grundlage der Rechnungsdaten berechnet. Die Rechnung kann nur gebucht werden, wenn die importierten Werte mit den berechneten Werten übereinstimmen. Übereinstimmende Werte stellen sicher, dass die Rechnung den dem Lieferanten zustehenden Betrag genau wiedergibt. Wenn Ihre Organisation zulässt, dass importierte Rechnungen automatisch an das Workflow-System gesendet werden, können Sie optional verlangen, dass die importierten Summen mit den berechneten Summen übereinstimmen, bevor die Rechnung an das Workflow-System gesendet werden kann.

## <a name="vendor-invoice-automation---resume-automation-processing-for-multiple-invoices"></a>Automation von Kreditorenrechnungen – Setzen Sie die Automationsverarbeitung für mehrere Rechnungen fort
Wenn eine importierte Rechnung nicht erfolgreich durch den automatisierten Prozess an den Workflow gesendet wird, wird sie von der weiteren automatisierten Verarbeitung ausgeschlossen. Ein Kreditorenbuchhalter kann die Rechnung überprüfen und bearbeiten, bevor der automatisierte Prozess sie erneut an den Workflow übermittelt. Wenn ein Fehlergrund durch dieselbe Behebung für mehrere Rechnungen behoben werden kann, können Sie den automatisierten Prozess auf der Seite **Automatisierte Rechnungsverarbeitung fortsetzen** neu starten. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
