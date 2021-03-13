---
title: Planen Sie der Arbeitserstellung während der Welle
description: In diesem Thema wird beschrieben, wie Sie die Wellenverarbeitungsmethode „Arbeitserstellung planen“ einrichten und verwenden.
author: perlynne
manager: mirzaab
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPostMethod, WHSWavePostMethodTaskConfig, WHSWaveTemplateTable, WHSParameters, WHSWaveTableListPage, WHSWorkTableListPage, WHSWorkTable, BatchJobEnhanced, WHSPlannedWorkOrder
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ed8f43c7db139b7b16ac6901d5db56ba2f021690
ms.sourcegitcommit: b7a7a14f8650913f6797ae1c4a82ad8adfe415fd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/28/2021
ms.locfileid: "5078264"
---
# <a name="schedule-work-creation-during-wave"></a>Planen Sie der Arbeitserstellung während der Welle

[!include [banner](../includes/banner.md)]

Verwenden Sie die Funktion *Arbeitserstellung planen* als Teil Ihres Wellenprozesses, um den Wellenverarbeitungsdurchsatz zu erhöhen, indem das System Arbeit mit paralleler Verarbeitung erstellt.

Wenn die Funktionalität aktiviert ist, werden geplante Arbeiten automatisch erstellt, die das System schließlich verarbeitet, um tatsächliche Arbeiten zu erstellen. Wenn die Anzahl der Wellenladungspositionen einen vorgegebenen Schwellenwert erreicht, erstellt das System durch parallele asynchrone Verarbeitung schneller tatsächliche Arbeit.

## <a name="enable-the-schedule-work-creation-feature"></a>Aktivieren der Funktion zum Erstellen von Arbeit

### <a name="enable-the-feature-in-feature-management"></a>Aktivieren der Funktion in der Funktionsverwaltung

Bevor Sie die Funktion *Arbeitserstellung planen* verwenden können, muss sie in Ihrem System eingeschaltet werden. Administratoren können mit der Einstellung [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) den Status der Funktion überprüfen und ggf. aktivieren. Dort wird die Funktion folgendermaßen aufgelistet:

- **Module:** *Lagerortverwaltung*
- **Funktionsname:** *Arbeitserstellung planen*

> [!NOTE]
> Die Funktion *Organisationsweite Arbeitssperre* muss aktiviert sein, bevor Sie *Arbeitserstellung planen* aktivieren können.

### <a name="manually-enable-batch-processing-of-waves"></a>Die Stapelverarbeitung von Wellen manuell aktivieren

Um eine parallele asynchrone Methode zum Erstellen von Lagerarbeiten nutzen zu können, muss Ihr Wellenprozess im Stapel ausgeführt werden. So richten Sie dies ein:

1. Wechseln Sie zu  **Lagerortverwaltung \>  Einstellungen \> Lagerortverwaltungsparameter**.

1. Setzen Sie auf der Registerkarte **Allgemein** die Option **Wellen in einem Stapel verarbeiten** auf *Ja*. Optional können Sie auch eine dedizierte **Stapelverarbeitungsgruppe Wellenverarbeitung** auswählen, um zu verhindern, dass Ihre Stapelwarteschlangenverarbeitung gleichzeitig mit anderen Prozessen ausgeführt wird.

1. Stellen Sie die Zeit von **Auf Sperre warten (ms)** ein, die gilt, wenn das System mehrere Wellen gleichzeitig verarbeitet. Für die meisten größeren Wellenprozesse empfehlen wir einen Wert von *60000*.

### <a name="manually-enable-the-new-wave-step-method-for-existing-wave-templates"></a>Manuelles Aktivieren der neuen Wellenschrittmethode für vorhandene Wellenvorlagen

Erstellen Sie zunächst die neue Wellenschrittmethode, und aktivieren Sie sie für die parallele asynchrone Aufgabenverarbeitung.

1. Wechseln Sie zu  **Lagerortverwaltung \> Setup \> Wellen \> Wellenverarbeitungsmethoden**.

1. Wählen Sie  **Methode erneut generieren** aus, und beachten Sie, dass *WHSScheduleWorkCreationWaveStepMethod* der Liste der Wellenprozessmethoden hinzugefügt wurde, die Sie in Ihren Versandwellenvorlagen verwenden können.

1. Wählen Sie den Datensatz mit dem **Methodennamen** *WHSScheduleWorkCreationWaveStepMethod* und dann **Aufgabenkonfiguration** aus.

1. Wählen Sie im Aktivitätsbereich **Neu** aus, um dem Raster eine Zeile hinzuzufügen, und verwenden Sie die folgenden Einstellungen:

    - **Lagerort** – Wählen Sie das Lager aus, in dem Sie die Verarbeitung der Arbeitserstellung planen möchten.

    - **Maximale Anzahl an Stapelverarbeitungsaufgaben** – Geben Sie eine maximale Anzahl von Stapelverarbeitungsaufgaben an. In den meisten Fällen sollte dieser Wert im Bereich von 8 bis 16 liegen. Wir empfehlen jedoch, mit der optimalen Einstellung basierend auf Ihren Szenarien zu experimentieren.

    - **Stapelverarbeitungsgruppe Wellenverarbeitung** – Wählen Sie eine dedizierte Stapelverarbeitungsgruppe der Wellenverarbeitung aus, um die Verarbeitung Ihrer Stapelverarbeitungswarteschlange zu optimieren.

Jetzt können Sie eine vorhandene Wellenvorlage aktualisieren (oder eine neue erstellen), um die Wellenverarbeitungsmethode *Arbeitserstellung planen* zu verwenden.

1. Wechseln Sie zu  **Lagerortverwaltung \> Einstellungen \> Wellen \> Wellenvorlagen**.

1. Wählen Sie im Aktionsbereich **Bearbeiten** aus.

1. Wählen Sie im Listenbereich die Wellenvorlage aus, die Sie aktualisieren möchten (wenn Sie mit Demodaten testen, können Sie *Standard-24-Lieferung* verwenden).

1. Erweitern Sie das Inforegister **Methoden**, und wählen Sie die Zeile mit dem **Namen** *Arbeitserstellung planen* im Raster **Verbleibende Methoden** aus.

1. Wählen Sie den Pfeil aus, der auf die Spalte **Ausgewählte Methoden** zeigt, um die ausgewählte Zeile in diese Spalte zu verschieben. (Sie können jeweils nur eine ausgewählte Methode haben, die entweder *WHSScheduleWorkCreationWaveStepMethod* oder *createWork* verwendet, sodass die vorhandene Zeile mit **Methodenname** *createWork* automatisch in das Raster **Verbleibende Methoden** verschoben wird.)

## <a name="set-wave-task-processing-threshold-data"></a>Festlegen der Schwellenwertdaten für die Verarbeitung von Wellenaufgaben

Das System erstellt beim ersten Ausführen eines Wellenprozesses mit einer aufgabenbasierten Verarbeitung Standardschwellenwertdaten für die Verarbeitung von Wellenaufgaben. Die Daten werden verwendet, um zu steuern, wann die Wellenverarbeitung asynchron ausgeführt wird und aufgabenbasiert ist, wodurch Arbeit parallel verarbeitet und erstellt werden kann.

Die Standarddaten verwenden zunächst einen Schwellenwert von 15 für die Mindestanzahl von Ladungspositionen (MINIMUMWAVELOADLINES). Dies bedeutet, dass das System bei der Verarbeitung einer Welle mit mehr als 15 Ladungspositionen die asynchrone Aufgabenverarbeitung verwendet. Sie können diese Daten manuell in die Tabelle **WHSWaveTaskProcessingThresholdParameters** in Ihren Testumgebungen einfügen oder dort aktualisieren. Wenn Sie diese Einstellung jedoch in einer Produktionsumgebung ändern müssen, müssen Sie sich an den Microsoft-Support wenden, um die Aktualisierung anzufordern.

## <a name="work-with-the-feature"></a>Arbeiten mit der Funktion

Wenn die Funktion *Arbeitserstellung planen* aktiviert ist, erstellt die Wellenverarbeitung geplante Arbeiten, die schließlich vom neuen Arbeitserstellungsprozess verwendet werden. Während der Arbeitserstellung wird die Arbeit mit der Funktion *Organisationsweite Arbeitssperre* gesperrt.

Das folgende Flussdiagramm zeigt, wie geplante Arbeiten während der Wellenverarbeitung erstellt werden.

![Arbeitserstellung planen](media/schedule-work-creation-process.png)

### <a name="planned-work"></a>Geplante Arbeit

Die Seite **Details der geplanten Arbeit** (**Lagerort verwaltung \> Arbeit \> Details der geplanten Arbeit**) zeigt Informationen über die geplante Arbeit an, die anfänglich während der Wellenverarbeitung erstellt werden. Die folgenden **Prozessstatus**-Werte sind verfügbar:

- **In Warteschlange** – Die geplante Arbeit wartet darauf, zur Erstellung von Arbeit verwendet zu werden.
- **Abgeschlossen** – Die geplante Arbeit wurde verwendet, um Arbeit zu erstellen.
- **Fehlgeschlagen** – Die Wellenverarbeitung ist fehlgeschlagen. Beachten Sie, dass die geplante Arbeit mit oder ohne zugehörige tatsächliche Arbeit in einem Status **Fehlgeschlagen** sein kann. Wenn der eigentliche Arbeitserstellungsprozess fehlschlägt, bleibt die eigentliche Arbeit im Status *Storniert*.

### <a name="batch-job-for-the-work-creation-process"></a>Stapelverarbeitungsauftrag für den Arbeitserstellungsprozess

Um die Stapelverarbeitungsaufträge für die Verarbeitung von Wellen anzuzeigen, wählen Sie **Stapelverarbeitungsaufträge** im Aktionsbereich auf der Seite **Alle Wellen** aus.

Von hier aus können Sie alle Details der Stapelverarbeitungsaufgabe für jede der Stapelverarbeitungsauftrags-IDs anzeigen.
