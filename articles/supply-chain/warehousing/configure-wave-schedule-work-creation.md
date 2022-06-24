---
title: Arbeitserstellung während Zyklus planen
description: In diesem Artikel wird beschrieben, wie Sie die Wellenverarbeitungsmethode „Arbeitserstellung planen“ einrichten und verwenden.
author: Mirzaab
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSPostMethod, WHSWavePostMethodTaskConfig, WHSWaveTemplateTable, WHSParameters, WHSWaveTableListPage, WHSWorkTableListPage, WHSWorkTable, BatchJobEnhanced, WHSPlannedWorkOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 8b4505d66c37134bc8f672b38d195f4f677df9bc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852069"
---
# <a name="schedule-work-creation-during-wave"></a>Planen Sie der Arbeitserstellung während der Welle

[!include [banner](../../includes/banner.md)]

Verwenden Sie die Funktion *Arbeitserstellung planen* als Teil Ihres Wellenprozesses, um den Wellenverarbeitungsdurchsatz zu erhöhen, indem das System Arbeit mit paralleler Verarbeitung erstellt.

Wenn die Funktionalität aktiviert ist, werden geplante Arbeiten automatisch erstellt, die das System schließlich verarbeitet, um tatsächliche Arbeiten zu erstellen. Wenn die Anzahl der Wellenladungspositionen einen vorgegebenen Schwellenwert erreicht, erstellt das System durch parallele asynchrone Verarbeitung schneller tatsächliche Arbeit.

## <a name="turn-on-the-scheduled-work-creation-features-in-feature-management"></a>Funktionen zur geplanten Arbeitserstellung in der Funktionsverwaltung aktivieren

Um die in diesem Artikel beschriebenen Funktionen nutzen zu können, müssen sie für Ihr System aktiviert sein. Benutzen Sie den Arbeitsbereich [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), um die folgenden Funktionen in der folgenden Reihenfolge zu aktivieren:

1. **Organisationsweite Arbeitssperre** – Erforderlich für die manuelle und automatische Konfiguration der geplanten Arbeitserstellung. (Ab Supply Chain Management Version 10.0.21 ist diese Funktion obligatorisch, daher ist sie standardmäßig aktiviert und kann nicht wieder deaktiviert werden.)
1. **Arbeitserstellung planen** – Erforderlich für die manuelle und automatische Konfiguration der geplanten Arbeitserstellung.
1. **Organisationsweite Wellenmethode „Arbeitserstellung planen“**  – Erforderlich für die manuelle und automatische Konfiguration der geplanten Arbeitserstellung. Sie benötigen diese Funktion nicht, wenn Sie nur die manuelle Konfiguration verwenden.

<a name="Auto-enable-schedule-work-creation"></a>

## <a name="automatically-configure-scheduled-work-creation"></a>Die geplante Arbeitserstellung automatisch konfigurieren

Wenn Sie die Funktion *Organisationsweite Wellenmethode „Arbeitserstellung planen“* aktiviert haben, passiert auf Ihrem System automatisch Folgendes:

- Die Wellenmethode *Arbeitserstellung planen* (`WHSScheduleWorkCreationWaveStepMethod`) wird hinzugefügt und so konfiguriert, dass sie für alle juristischen Personen parallel ausgeführt wird.
- Bei Wellenvorlagen von allen juristischen Personen, bei denen der **Wellenvorlagentyp** auf *Versand* und **Vorlagenstatus** auf *Gültig* eingestellt ist, wird die Methode *Arbeit erstellen* durch die Methode *Arbeitserstellung planen* ersetzt. Wellenvorlagen von juristischen Personen, bei denen die Methode *Arbeit erstellen* wiederholbar sein darf, werden nicht geändert.
- Aufgabenkonfigurationen für die Methode *Arbeitserstellung planen* werden für alle Lagerorte von allen juristischen Personen erstellt, bei denen **Lagerortverwaltungsprozesse verwenden** aktiviert ist. Dies bedeutet, dass die Methode *Arbeitserstellung planen* jetzt standardmäßig parallel ausgeführt wird. Bestehende Lagerorte, für die Sie **Lagerortverwaltungsprozesse verwenden** von *Nein* auf *Ja* ändern, führen diese Methode standardmäßig auch parallel aus.
- Alle juristischen Personen verarbeiten Wellen in einem Stapel und **Auf Sperre (ms) warten** wird auf einen Standardwert von *60.000* ms gesetzt, wenn sie vorher auf *0* ms eingestellt waren.
- Alle neuen Wellenvorlagen, die Sie erstellen, haben die Wellenmethode *Arbeitserstellung planen* anstelle der Methode *Arbeit erstellen*.

Die vorhandenen Aufgaben- und Wellenverarbeitungskonfigurationen werden auch für alle juristischen Personen beibehalten, die bereits für die Stapelverarbeitung von Wellen konfiguriert sind, sowie für alle Lagerorte, die bereits für die parallele Verwendung der Methode *Arbeitserstellung erstellen* konfiguriert sind.

Bei Bedarf können Sie einige oder alle Einstellungen, die beim Aktivieren von der Funktion *Organisationsweite Wellenmethode „Arbeitserstellung planen“* automatisch vorgenommen wurden, manuell zurücksetzen, indem Sie Folgendes tun:

- Wechseln Sie für Wellenvorlagen zu **Lagerortverwaltung \> Einstellungen \> Wellen \> Wellenvorlagen**. Ersetzen Sie die Methode *Arbeitserstellung planen* mit *Arbeit erstellen*.
- Gehen Sie für Lagerortparameter zu **Warehouse Management \> Einstellungen \> Lagerortverwaltungsparameter**. Wenden Sie auf der Registerkarte **Wellenverarbeitung** Ihre bevorzugten Werte für **Wellen in einem Stapel verarbeiten** und **Auf Sperre (ms) warten**.
- Wechseln Sie für die Wellenmethoden zu **Lagerortverwaltung \> Einstellungen \> Wellen \> Wellenverarbeitungsmethoden**. Wählen Sie `WHSScheduleWorkCreationWaveStepMethod` und dann im Aktivitätsbereich **Aufgabenkonfiguration** aus. Ändern oder löschen Sie nach Bedarf die Anzahl der Stapelverarbeitungsaufgaben und die zugewiesene Wellengruppe für die einzelnen aufgeführten Lagerorte.

## <a name="manually-configure-scheduled-work-creation"></a>Die geplante Arbeitserstellung manuell konfigurieren

Wenn Sie die [Funktion *Organisationsweite Wellenmethode „Arbeitserstellung planen“*](#Auto-enable-schedule-work-creation) aktiviert haben, können Sie die in diesem Abschnitt beschriebenen Prozeduren verwenden, um die geplante Arbeitserstellung nach Bedarf manuell zu konfigurieren.

### <a name="manually-enable-batch-processing-of-waves"></a>Die Stapelverarbeitung von Wellen manuell aktivieren

Um eine parallele asynchrone Methode zum Erstellen von Lagerarbeiten nutzen zu können, muss Ihr Wellenprozess im Stapel ausgeführt werden. So richten Sie dies ein:

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerortverwaltungsparameter**.
1. Setzen Sie auf der Registerkarte **Allgemein** die Option **Wellen in einem Stapel verarbeiten** auf *Ja*. Optional können Sie auch eine dedizierte **Stapelverarbeitungsgruppe Wellenverarbeitung** auswählen, um zu verhindern, dass Ihre Stapelwarteschlangenverarbeitung gleichzeitig mit anderen Prozessen ausgeführt wird.
1. Stellen Sie die Zeit von **Auf Sperre warten (ms)** ein, die gilt, wenn das System mehrere Wellen gleichzeitig verarbeitet. Für die meisten größeren Wellenprozesse empfehlen wir einen Wert von *60000*.

### <a name="manually-enable-the-new-wave-step-method-for-existing-wave-templates"></a>Manuelles Aktivieren der neuen Wellenschrittmethode für vorhandene Wellenvorlagen

Erstellen Sie zunächst die neue Wellenschrittmethode, und aktivieren Sie sie für die parallele asynchrone Aufgabenverarbeitung.

1. Wechseln Sie zu **Lagerortverwaltung \> Setup \> Wellen \> Wellenverarbeitungsmethoden**.
1. Wählen Sie **Methode erneut generieren** aus und beachten Sie, dass *WHSScheduleWorkCreationWaveStepMethod* der Liste der Wellenprozessmethoden hinzugefügt wurde, die Sie in Ihren Versandwellenvorlagen verwenden können.
1. Wählen Sie den Datensatz mit dem **Methodennamen** *WHSScheduleWorkCreationWaveStepMethod* und dann **Aufgabenkonfiguration** aus.
1. Wählen Sie im Aktivitätsbereich **Neu** aus, um dem Raster eine Zeile hinzuzufügen, und verwenden Sie die folgenden Einstellungen:

    - **Lagerort** – Wählen Sie das Lager aus, in dem Sie die Verarbeitung der Arbeitserstellung planen möchten.
    - **Maximale Anzahl an Stapelverarbeitungsaufgaben** – Geben Sie eine maximale Anzahl von Stapelverarbeitungsaufgaben an. In den meisten Fällen sollte dieser Wert im Bereich von 8 bis 16 liegen. Wir empfehlen jedoch, mit der optimalen Einstellung basierend auf Ihren Szenarien zu experimentieren.
    - **Stapelverarbeitungsgruppe Wellenverarbeitung** – Wählen Sie eine dedizierte Stapelverarbeitungsgruppe der Wellenverarbeitung aus, um die Verarbeitung Ihrer Stapelverarbeitungswarteschlange zu optimieren.

Jetzt können Sie eine vorhandene Wellenvorlage aktualisieren (oder eine neue erstellen), um die Wellenverarbeitungsmethode *Arbeitserstellung planen* zu verwenden.

1. Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Wellen \> Wellenvorlagen**.
1. Wählen Sie im Aktionsbereich **Bearbeiten** aus.
1. Wählen Sie im Listenbereich die Wellenvorlage aus, die Sie aktualisieren möchten (wenn Sie mit Demodaten testen, können Sie *Standard-24-Lieferung* verwenden).
1. Erweitern Sie das Inforegister **Methoden**, und wählen Sie die Zeile mit dem **Namen** *Arbeitserstellung planen* im Raster **Verbleibende Methoden** aus.
1. Wählen Sie den Pfeil aus, der auf die Spalte **Ausgewählte Methoden** zeigt, um die ausgewählte Zeile in diese Spalte zu verschieben. (Sie können jeweils nur eine ausgewählte Methode haben, die entweder `WHSScheduleWorkCreationWaveStepMethod` oder `createWork` verwendet, sodass die vorhandene Zeile mit **Methodenname** `createWork` automatisch in das Raster **Verbleibende Methoden** verschoben wird.)

## <a name="set-wave-task-processing-threshold-data"></a>Festlegen der Schwellenwertdaten für die Verarbeitung von Wellenaufgaben

Das System erstellt beim ersten Ausführen eines Wellenprozesses mit einer aufgabenbasierten Verarbeitung Standardschwellenwertdaten für die Verarbeitung von Wellenaufgaben. Die Daten werden verwendet, um zu steuern, wann die Wellenverarbeitung asynchron ausgeführt wird und aufgabenbasiert ist, wodurch Arbeit parallel verarbeitet und erstellt werden kann.

Die Standarddaten verwenden zunächst einen Schwellenwert von 15 für die Mindestanzahl von Ladungspositionen (`MINIMUMWAVELOADLINES`). Dies bedeutet, dass das System bei der Verarbeitung einer Welle mit mehr als 15 Ladungspositionen die asynchrone Aufgabenverarbeitung verwendet. Sie können diese Daten manuell in die Tabelle `WHSWaveTaskProcessingThresholdParameters` in Ihren Testumgebungen einfügen bzw. dort aktualisieren. Wenn Sie diese Einstellung in einer Produktionsumgebung ändern müssen, müssen Sie sich an den Microsoft-Support wenden, um das Update anzufordern.

## <a name="work-with-the-scheduled-work-creation"></a>Mit der geplanten Arbeitserstellung arbeiten

Ausführliche Informationen zum Arbeiten mit der geplanten Arbeitserstellung finden Sie unter [Wellen erstellen und verarbeiten](wave-processing.md). 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
