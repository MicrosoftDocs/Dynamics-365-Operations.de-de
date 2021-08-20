---
title: Planen des Wellenetikettendrucks während der Welle
description: Dieses Thema beschreibt, wie Sie die Funktionalität für aufgabenbasierten Wellenetikettendruck festlegen und verwenden.
author: MSFTGarm
ms.date: 06/09/2021
ms.topic: article
ms.search.form: WHSPostMethod, WHSWavePostMethodTaskConfig, WHSWaveTemplateTable, WHSParameters, WHSWaveTableListPage, WHSWorkTableListPage, WHSWorkTable, BatchJobEnhanced, WHSPlannedWorkOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-obaranov
ms.search.validFrom: 2021-06-09
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 652e6fb3f586fc873ffabf2c741e5c99216931461f159a42f08f9922e756280f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6735895"
---
# <a name="schedule-wave-label-printing-during-wave"></a>Planen des Wellenetikettendrucks während der Welle

[!include [banner](../../includes/banner.md)]

Verwenden Sie die Funktion *Aufgabenbasierter Wellenetikettendruck* als Teil Ihres Wellenprozesses, um die Effizienz zu verbessern und um das System Wellenetiketten erstellen und in separaten Aufgaben arbeiten zu lassen.

Der Prozess der Konfiguration des Wellenetikettendrucks ist komplex und hängt von genauen Konfigurations- und Stammdaten ab. Es ist nicht ungewöhnlich, dass die Erzeugung von Datensätzen für Wellenetiketten fehlschlägt, und wenn dies geschieht, wird die gesamte Wellenverarbeitung zurückgesetzt. Die Funktion *Aufgabenbasierter Wellenetikettendruck* hilft Ihnen zu vermeiden, dass Sie jedes Mal, wenn ein Wellenetikett fehlerhaft gedruckt wird, Arbeits- und Arbeitszeilen neu erstellen müssen.

Wenn Sie die Funktion *Aufgabenbasierter Wellenetikettendruck* verwenden, erstellt das System zunächst Arbeits- und Arbeitszeilen. Dann erstellt und druckt es Wellenetiketten. Wenn die Wellenetiketten korrekt erstellt wurden, gibt es schließlich die Arbeit und die Welle zum Kommissionieren frei.

## <a name="turn-on-the-task-based-wave-label-printing-feature-in-feature-management"></a>Aktivieren Sie die Funktion „Aufgabenbasierter Wellenetikettendruck“ in der Funktionsverwaltung

Um die Funktionen zu verwenden, die in diesem Thema beschrieben werden, müssen sie für Ihr System eingeschaltet werden. Verwenden Sie den Arbeitsbereich [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), um die Funktionen in der folgenden Reihenfolge zu aktivieren:

1. *Wellenetikettendruck* – Diese Funktion ist erforderlich, um das Wellenprozessverfahren für den Wellenetikettendruck zu aktivieren.
1. *Organisationsweite Arbeitssperrung* – Diese Funktion ist sowohl für die manuelle als auch für die automatische Konfiguration der geplanten Arbeitserstellung erforderlich.
1. *Aufgabenbasierter Wellenetikettendruck* – Diese Funktion ist erforderlich, um den Wellenetikettendruck in einen separaten Transaktionsbereich abzuspalten.

## <a name="manually-enable-the-new-wave-step-method"></a>Manuelles Aktivieren der neuen Wellenschrittmethode

Sie müssen zunächst die neue Wellenschrittmethode erstellen und sie für die parallele, asynchrone Aufgabenverarbeitung aktivieren.

1. Wechseln Sie zu  **Lagerortverwaltung \> Setup \> Wellen \> Wellenverarbeitungsmethoden**.
1. Wählen Sie im Aktionsbereich **Methode neu generieren**. Beachten Sie, dass *waveLabelPrinting* der Liste der Wellenschrittmethoden hinzugefügt wird, die Sie in Ihren Versandwellenvorlagen verwenden können.
1. Wählen Sie den Datensatz, bei dem das Feld **Methodenname** auf *waveLabelPrinting* festgelegt ist, und wählen Sie dann im Aktionsbereich **Aufgabenkonfiguration**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Zeile zum Raster hinzuzufügen. Legen Sie für die neue Zeile die folgenden Felder fest:

    - **Lagerort** – Wählen Sie den Lagerort aus, den Sie für die Planung der Verarbeitung der Arbeitserstellung verwenden werden. (Wenn Sie Demo-Daten zu Testzwecken verwenden, können Sie Lagerort *24* wählen).
    - **Maximale Anzahl von Batch-Aufgaben** – Geben Sie eine maximale Anzahl von Batch-Aufgaben an. In den meisten Fällen sollte der Wert zwischen *8* und *16* liegen. Wir empfehlen jedoch, dass Sie experimentieren, um die optimale Einstellung für Ihre Szenarien zu finden.
    - **Batch-Gruppe für die Wellenverarbeitung** – Wählen Sie eine dedizierte Batch-Gruppe für die Wellenverarbeitung, um die Verarbeitung von Batch-Warteschlangen zu optimieren.

Sie können nun eine bestehende Wellenvorlage so aktualisieren, dass sie die *Wellenetikettendruck* Wellenverarbeitungsmethode verwendet. Alternativ können Sie auch eine neue Wellenvorlage erstellen, die diese Methode verwendet.

1. Wechseln Sie zu  **Lagerortverwaltung \> Einstellungen \> Wellen \> Wellenvorlagen**.
1. Wählen Sie im Aktionsbereich **Bearbeiten** aus.
1. Wählen Sie im Listenbereich die Wellenvorlage aus, die Sie aktualisieren möchten. (Wenn Sie Demodaten zu Testzwecken verwenden, können Sie *24 Versand Standard* wählen).
1. Wählen Sie im Inforegister **Methoden** in der Spalte **Restliche Methoden** die Zeile, in der das Feld **Name** auf *waveLabelPrinting* festgelegt ist.
1. Wählen Sie **Hinzufügen** (rechte Pfeiltaste), um die ausgewählte Zeile in die Spalte **Ausgewählte Methoden** zu verschieben.
1. Geben Sie in das Feld **Wellenschrittcode** einen Wellenschrittcode ein, der verwendet wird, um die Wellenvorlage mit einer Wellenetikettenvorlage zu verbinden.

## <a name="set-wave-task-processing-threshold-data"></a>Festlegen der Schwellenwertdaten für die Verarbeitung von Wellenaufgaben

Wenn ein Wellenprozess zum ersten Mal unter Verwendung einer beliebigen aufgabenbasierten Verarbeitung ausgeführt wird, erstellt das System Standardschwellwertdaten für die Wellenaufgabenverarbeitung. Diese Daten werden verwendet, um zu steuern, ob die Wellenverarbeitung asynchron und taskbasiert ausgeführt wird, so dass sie Wellenlabel parallel verarbeiten und erstellen kann.

Die Standarddaten verwenden zunächst einen Schwellenwert von *1* für die minimale Anzahl von Work-IDs (`MinimumWorkThresholdForLabelPrinting`). Wenn das System also eine Welle verarbeitet, die mehr als eine Arbeits-ID hat, verwendet es die aufgabenbasierte Verarbeitung von Wellenetiketten in einer separaten Transaktion. Sie können diese Daten in der Tabelle `WHSWaveTaskProcessingThresholdParameters` in Ihren Testumgebungen manuell einfügen oder aktualisieren. Um die Einstellung in einer Produktionsumgebung zu ändern, müssen Sie sich an den Microsoft Support wenden, um die Aktualisierung anzufordern.

## <a name="changes-to-the-wave-processing-logic-when-task-based-wave-label-printing-is-used"></a>Änderungen an der Wellenverarbeitungslogik, wenn der aufgabenbasierte Wellenetikettendruck verwendet wird

Wenn die Verarbeitung der Wellenetiketten den Schwellenwert für die aufgabenbasierte Wellenverarbeitung überschreitet, wird die aufgabenbasierte Verarbeitung eingeleitet. In der nächsten Wellenverarbeitung, die zur Wellenvorlage passt, wird der Wellenetikettendruck in einer eigenständigen *ttsbegin*/*ttscommit* Transaktion unmittelbar nach der Arbeitsfreigabe ausgeführt. Wenn die Arbeitsfreigabe (Entsperrung) auf der Wellenvorlage so konfiguriert ist, dass sie automatisch ausgeführt wird, erfolgt sie erst nach erfolgreichem Abschluss des Wellenetikettendrucks.

Wenn die Erzeugung von Wellenetiketten fehlschlägt (z. B. wenn die Umwandlung der Arbeitsmenge in die Wellenetikettenmenge fehlschlägt und einen Fehler auslöst), schlägt nur die entsprechende Transaktion fehl. Die Arbeit, die zuvor erstellt wurde, bleibt eingefroren. Um den Fehler zu beheben und die Wellenetiketten zu drucken, gehen Sie wie folgt vor.

1. Wechseln Sie zu **Lagerortverwaltung \> Ausgehende Wellen \> Lieferungswellen \> Alle Wellen**.
1. Wählen Sie die entsprechende Welle im Raster aus.
1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Welle** in der Gruppe **Drucken** auf **Serienetiketten**.
1. Befolgen Sie die Anweisungen auf dem Bildschirm, um die Etiketten zum Drucken zu senden.
1. Wählen Sie im Aktionsbereich auf der Registerkarte **Welle** in der Gruppe **Welle** die Option **Freigeben**, um die Arbeit für die ausgewählte Welle manuell freizugeben.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Wellenbeschriftungsdruck](configure-wave-label-printing.md)
- [Arbeitserstellung während Welle planen](configure-wave-schedule-work-creation.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
