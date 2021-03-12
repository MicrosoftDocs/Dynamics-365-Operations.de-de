---
title: Überblick über automatisierte Kreditorenabrechnungsprozesse
description: In diesem Thema werden die Funktionen zur Automatisierung der Verarbeitung Ihrer Kreditorenrechnungen und die Vorteile der Verwendung eines automatisierten Prozesses beschrieben.
author: abruer
manager: AnnBe
ms.date: 11/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-30
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 9a033258feeccf172f1e2c03a9f49305054b24c2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972130"
---
# <a name="automated-vendor-invoicing-processes-overview"></a>Überblick über automatisierte Kreditorenabrechnungsprozesse

[!include [banner](../includes/banner.md)]

In diesem Thema werden die Funktionen zur Automatisierung der Verarbeitung Ihrer Kreditorenrechnungen und die Vorteile der Verwendung eines automatisierten Prozesses beschrieben. Die Funktionen hierfür werden in der Funktionsverwaltung aktiviert. Diese Funktionen gelten nur für Kreditorenrechnungen, nicht für Rechnungen, die über die **Rechnungserfassung** oder die Seite **Rechnungsbucherfassung** verarbeitet werden.

Organisationen arbeiten häufig mit Dritten zusammen, um Papierrechnungen mithilfe einer optischen Zeichenerkennung (OCR) von einem Dienstanbieter zu verarbeiten. Vom Dienstanbieter erhalten sie dann maschinenlesbare Rechnungsmetadaten. Um die Automatisierung zu unterstützen, können Sie mit den Automatisierungsfunktionen für die Kreditorenkonten diese Artefakte aus den Kreditorenkonten verwenden.

Sie können einige Kreditorenabrechnungsprozesse für Kreditorenkonten automatisieren. Diese Prozesse umfassen das Übermitteln importierter Kreditorenrechnungen an das Workflowsystem und das Abgleichen der gebuchten Produktzugangspositionen mit ausstehenden Kreditorenrechnungspositionen. Der automatisierte Prozess zeigt Informationen über den Fortschritt einer Kreditorenrechnung an, während diese die einzelnen Prozesse durchläuft. Diese Funktion kann Sachbearbeitern und Mangern von Kreditorenkonten helfen, Kreditorenrechnungen effizienter zu bearbeiten. Sie trägt auch dazu bei, die Fehler und Ineffizienzen zu reduzieren, die bei der manuellen Eingabe und Verarbeitung von Informationen auftreten können.

Die Automatisierungsprozesse können verwendet werden, um folgende Aufgaben auszuführen:

- Senden Sie importierte Rechnungen automatisch an das Workflowsystem.
- Gleichen Sie Produktzugänge mit ausstehenden Kreditorenrechnungspositionen ab.
- Simulieren Sie die Buchung, bevor eine Kreditorenrechnung gebucht wird.
- Zeigen Sie schnell und effizient den Workflow- und Automationsverlauf an.
- Zeigen Sie die Ergebnisse der Automatisierung der Verarbeitung von Kreditorenrechnungen an und analysieren Sie sie.
- Setzen Sie die automatisierte Verarbeitung für mehrere Rechnungen fort.

## <a name="vendor-invoice-automation--submit-imported-vendor-invoices-to-the-workflow-system"></a>Automatisierung von Kreditorenrechnungen – Senden von importierten Kreditorenrechnungen an das Workflowsystem

Im Rahmen eines berührungslosen Rechnungsstellungsprozesses für Kreditorenkonten können Sie das System automatisch eine importierte Rechnung an das Workflowsystem senden lassen. Der Prozess wird im Hintergrund mit einer von Ihnen angegebenen Häufigkeit (entweder stündlich oder täglich) ausgeführt. Um importierte Rechnungen automatisch an das Workflowsystem senden zu können, muss Ihr Prozess mit einer importierten Rechnung beginnen. Um sicherzustellen, dass die Rechnung ohne manuellen Eingriff von Anfang bis Ende verarbeitet werden kann, muss eine automatisierte Buchungsaufgabe in der Workflowkonfiguration enthalten sein.

Rechnungen, die sich auf Bestellungen beziehen, sowie Rechnungen, die eine Beschaffungskategorie ohne Bestellung und nicht vorrätige Positionen enthalten, können automatisch an das Workflow-System gesendet werden. Rechnungen, die manuell eingegeben werden, und Rechnungen, die über den Arbeitsbereich **Kreditorkooperationsrechnungen** erstellt werden, müssen manuell an das Workflowsystem gesendet werden.

Die Automatisierungsfunktion stellt ein flexibles Framework bereit, mit dem Sie unternehmensspezifische Regeln für das Senden importierter Kreditorenrechnungen an das Workflowsystem und das Abgleichen gebuchter Produktzugangspositionen mit ausstehenden Kreditorenrechnungspositionen definieren können.

## <a name="vendor-invoice-automation--match-product-receipts-to-invoice-lines-that-have-a-three-way-matching-policy"></a>Kreditorenrechnungsautomatisierung – Abgleichen von gebuchten Produktzugängen mit Rechnungspositionen, für die eine dreiseitige Abgleichsrichtlinie gilt

Das System kann gebuchte Produktzugänge automatisch mit Rechnungspositionen abgleichen, für die eine dreiseitige Abgleichsrichtlinie definiert ist. Der Prozess wird ausgeführt, bis die abgeglichene Produktzugangsmenge der Rechnungsmenge entspricht. Im Rahmen dieses Prozesses können Sie für das System die maximale Anzahl der versuchten Abgleiche der Produktzugänge mit einer Rechnungsposition festlegen, bevor das System zu dem Schluss kommt, dass der Prozess fehlgeschlagen ist. Der Prozess wird entweder stündlich oder täglich im Hintergrund ausgeführt. Sie können den automatisierten Abgleichprozess im Rahmen des Prozesses zum Senden von Rechnungen an das Workflowsystem ausführen. Alternativ können Sie den Prozess auch als eigenständigen Prozess ausführen.

## <a name="vendor-invoice-automation--pre-validate-vendor-invoice-posting"></a>Kreditorenrechnungsautomatisierung – Überprüfen von Kreditorenrechnungen vor der Buchung

Die Buchungssimulation schließt die Prüfungsschritte ab, die während des Buchungsprozesses für Kreditorenrechnungen ausgeführt werden. Dabei werden jedoch keine Konten aktualisiert. Um den Prozess auszuführen, können Sie auf der Seite **Ausstehende Kreditorenrechnungen** entweder eine einzelne Rechnung oder mehrere Rechnungen auswählen.

## <a name="vendor-invoice-automation--enhanced-experience-for-viewing-workflow-and-automation-historical-information-for-vendor-invoices"></a>Kreditorenrechnungsautomatisierung – verbesserte Erfahrung beim Anzeigen von Informationen aus des Workflow- und Automationsverlauf für Kreditorenrechnungen

Es wird eine übersichtliche Ansicht der Workflowhistorie der Kreditorenrechnung bereitgestellt. Auf die Ansicht der Workflowhistorie kann direkt über die Kreditorenrechnung zugegriffen werden. Daher sind weniger Mausklicks erforderlich, um diese Informationen zu finden. Wenn Ihre Organisation die Möglichkeit aktiviert hat, importierte Kreditorenrechnungen automatisch an den Workflow zu senden, wird der Automationsverlauf für die importierten Rechnungen bereitgestellt. Mithilfe des Automationsverlaufs können Sie den aktuellen Prozessschritt sowie die bereits abgeschlossenen Schritte identifizieren. Wenn ein Schritt nicht erfolgreich ist, bietet das System detaillierte Informationen, damit Sie den Grund für den Fehler besser verstehen.

## <a name="vendor-invoice-automation--analytics-and-metrics"></a>Kreditorenrechnungsautomatisierung – Analysen und Metriken

Der Arbeitsbereich **Kreditorenrechnungseintrag** ermöglicht die Fokussierung auf Kreditorenrechnungen, die den automatisierten Prozess nicht durchlaufen haben. Kacheln im Arbeitsbereich enthalten Informationen zu Kreditorenrechnungen, die nicht erfolgreich an das Workflowsystem gesendet, importiert oder mit Produktzugängen abgeglichen wurden. Darüber hinaus werden Microsoft Power BI-Metriken bereitgestellt, um den Mangern von Kreditorenkonten einen Einblick in die Effizienz der Automatisierung von Kreditorenrechnungen zu geben.

## <a name="vendor-invoice-automation---resume-automation-processing-for-multiple-invoices"></a>Automation von Kreditorenrechnungen – Setzen Sie die Automationsverarbeitung für mehrere Rechnungen fort
Wenn eine importierte Rechnung während des automatisierten Prozesses nicht erfolgreich an den Workflow gesendet wird, wird sie vom System aus der weiteren automatisierten Verarbeitung entfernt. Ein Kreditorenbuchhalter kann die Rechnung überprüfen und bearbeiten, bevor der automatisierte Prozess sie erneut an den Workflow übermittelt. Wenn ein Fehlergrund durch dieselbe Behebung für mehrere Rechnungen behoben werden kann, können Sie den automatisierten Prozess auf der Seite **Automatisierte Rechnungsverarbeitung fortsetzen** neu starten. 
