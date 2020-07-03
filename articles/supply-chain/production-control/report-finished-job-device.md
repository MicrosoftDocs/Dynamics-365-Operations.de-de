---
title: Vom Einzelvorgangskartengerät als erledigt melden
description: In diesem Thema wird beschrieben, wie Sie das System so konfigurieren, dass Benutzer eines Einzelvorgangskartengeräts fertige Produkte aus einem Fertigungsauftrag an das Inventar melden können.
author: johanhoffmann
manager: tfehr
ms.date: 05/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistrationSetupTouch
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: f5d34893ddc8adc3785ec50dbd72438cf8f68c5d
ms.sourcegitcommit: 52ba8d3e6af72df5dab6c04b9684a61454d353ad
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/26/2020
ms.locfileid: "3403261"
---
# <a name="report-as-finished-from-the-job-card-device"></a>Vom Einzelvorgangskartengerät als erledigt melden

[!include [banner](../includes/banner.md)]

Arbeiter benutzen die Seite **Fortschritt melden** auf dem Einzelvorgangskartengerät, um Mengen zu melden, die für einen Produktionsjob abgeschlossen wurden.

## <a name="control-whether-quantities-that-are-reported-as-finished-are-added-to-inventory"></a>Steuern Sie, ob Mengen, die als fertig gemeldet werden, dem Inventar hinzugefügt werden

Führen Sie die folgenden Schritte aus, um zu steuern, ob und wie die Mengen, die beim letzten Vorgang als fertig gemeldet wurden, zum Inventar hinzugefügt werden sollen.

1. Gehen Sie zu **Produktionssteuerung \> Einstellungen \> Fertigungssteuerung \> Produktionsparameterstandard**.
1. Auf der Registerkarte **Als fertig melden** stellen Sie das Feld **Aktualisieren Sie den fertigen Bericht online** auf einen der folgenden Werte:

    - **Nein** – Es wird keine Menge zum Inventar hinzugefügt, wenn Mengen bei der letzten Operation gemeldet werden. Der Status des Produktionsauftrags verändert sich jedoch nie.
    - **Status + Menge** – Der Status des Fertigungsauftrags ändert sich in *Als fertig gemeldet* und die Menge wird als fertig im Inventar gemeldet.
    - **Menge** – Die Menge wird im Bestand als fertig gemeldet, aber der Status des Produktionsauftrags ändert sich nie.
    - **Status** – Es ändert sich nur der Status des Produktionsauftrags. Es werden dem Bestand keine Mengen hinzugefügt, wenn Mengen beim letzten Vorgang gemeldet werden.

> [!NOTE]
> Mengen werden im Bestand nicht nachverfolgt, wenn die Vorgänge, für die sie als abgeschlossen gemeldet werden, nicht als letzte Vorgänge definiert sind. Diese Mengen können jedoch verwendet werden, um den Fortschritt anzuzeigen. Sie können auch in Regeln aufgenommen werden, die steuern, ob Mitarbeiter die nächste Operation starten können, bevor ein definierter Schwellenwert für die gemeldeten Mengen der vorherigen Operation erreicht ist. Sie können diese Regeln auf der Registerkarte **Mengenvalidierung** auf der Seite **Standard-Produkrtionsauftrag** definieren.

Weitere Informationen zum Arbeiten mit der Seite **Standardwerte für Fertigungsaufträge** finden Sie unter [Produktionsparameter in der Fertigungsausführung](production-parameters-manufacturing-execution.md).

## <a name="report-batch-controlled-items-as-finished"></a>Chargengesteuerte Artikel als fertig melden

Das Einzelvorgangskartengerät unterstützt drei Szenarien für die Berichterstellung für Chargenelemente. Diese Szenarien gelten sowohl für Artikel, die für erweiterte Lagerprozesse aktiviert sind, als auch für Artikel, die für erweiterte Lagerprozesse nicht aktiviert sind.

- **Manuell zugewiesene Chargennummern:** Die Mitarbeiter geben eine benutzerdefinierte Chargennummer ein. Diese Chargennummer stammt möglicherweise von einer externen Quelle, die dem System nicht bekannt ist.
- **Vordefinierte Chargennummern:** Arbeitskräfte wählen eine Chargennummer in einer Liste von Chargennummern aus, die das System automatisch generiert, bevor der Fertigungsauftrag an das Einzelvorgangskartengerät freigegeben wird.
- **Feste Chargennummern:** Die Mitarbeiter geben keine benutzerdefinierte Chargennummer ein oder wählen keine. Stattdessen weist das System dem Fertigungsauftrag automatisch eine Chargennummer zu, bevor er freigegeben wird.

Um ein Szenario zu aktivieren, führen Sie folgende Schritte aus.

1. Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**.
1. Wählen Sie das Produkt zum Konfigurieren.
1. Auf dem Inforegister **Bestand verwalten** im Feld **Chargennummerngruppe** wählen Sie die Nachverfolgungs-Nummerngruppe aus, die zur Unterstützung Ihres Szenarios eingerichtet ist.

> [!NOTE]
> Wenn einem chargengesteuerten Produkt keine Chargennummerngruppe zugeordnet ist, bietet das Einzelvorgangskartengerät standardmäßig eine manuelle Eingabe der Chargennummer, während der Berichterstellung als abgeschlossen gemeldet wird.

In den folgenden Unterabschnitten wird beschrieben, wie Sie Nachverfolgungs-Nummerngruppen einrichten, um jedes der drei Szenarien für die Berichterstellung für Chargenpositionen zu unterstützen.

### <a name="enable-batch-number-reporting-on-the-job-card-device"></a>Aktivieren Sie die Chargennummernberichterstattung auf dem Einzelvorgangskartengerät

Damit Ihre Einzelvorgangskartengeräte während der Berichterstellung eine Chargennummer als abgeschlossen akzeptieren können, müssen Sie die [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) verwenden, um die folgenden Funktionen zu aktivieren (in dieser Reihenfolge):

1. Verbesserte Benutzerfreundlichkeit für den Berichtsstatusdialog im Einzelvorgangs-Kartengerät
1. Aktivieren Sie diese Option, um Chargen- und Seriennummern einzugeben, während die Fertigmeldung vom Einzelvorgangs-Kartengerät (Vorschau) abgeschlossen wird

### <a name="set-up-a-tracking-number-group-that-lets-workers-manually-assign-a-batch-number"></a>Richten Sie eine Nachverfolgungs-Nummerngruppe ein, mit der Mitarbeiter manuell eine Chargennummer zuweisen können

Um Chargennummern manuell einzurichten, folgen Sie diesen Schritten, um ein Nachverfolgungs-Nummerngruppe einzurichten.

1. Gehen Sie zu **Bestandsverwaltung \> Installieren \> Ausmaße \> Nachverfolgung von Nummerngruppen**.
1. Erstellen oder wählen Sie die einzurichtende Nachverfolgungs-Nummerngruppe.
1. Auf dem Inforegister **Allgemein** stellen Sie die Option **Manuell** auf **Ja** fest.

    ![Seite mit den Nummerngruppen nachverfolgen](media/tracking-number-group-manual.png "Seite mit den Nummerngruppen nachverfolgen")

1. Stellen Sie andere Werte nach Bedarf ein und wählen Sie diese Nachverfolgungs-Nummerngruppe als Chargennummerngruppe für freigegebene Produkte aus, für die Sie dieses Szenario verwenden möchten.

Wenn Sie dieses Szenario verwenden, wird das Feld **Chargennummer** **Fortschritt melden** auf der Seite auf dem Einzelvorgangskartengerät ein Textfeld anzeigen, in das Mitarbeiter einen beliebigen Wert eingeben können.

![Fortschrittsseite mit einem Feld für manuelle Chargennummern melden](media/job-card-device-batch-manual.png "Fortschrittsseite mit einem Feld für manuelle Chargennummern melden")

### <a name="set-up-a-tracking-number-group-that-provides-a-list-of-predefined-batch-numbers"></a>Richten Sie eine Nachverfolgungs-Nummerngruppe ein, die eine Liste vordefinierter Chargennummern enthält

Um eine Liste vordefinierter Chargennummern einzurichten, folgen Sie diesen Schritten, um ein Nachverfolgungs-Nummerngruppe einzurichten.

1. Gehen Sie zu **Bestandsverwaltung \> Installieren > Ausmaße \> Nachverfolgung von Nummerngruppen**.
1. Erstellen oder wählen Sie die einzurichtende Nachverfolgungs-Nummerngruppe.
1. Auf dem Inforegister **Allgemein** stellen Sie die Option **Nur für Bestandtransaktionen** auf **Ja** fest.
1. Verwenden Sie das Feld **Pro Menge** zum Aufteilen der Chargennummern pro Menge, basierend auf dem von Ihnen eingegebenen Wert. Zum Beispiel haben Sie einen Fertigungsauftrag für zehn Stück und das Feld **Pro Menge** ist auf *2* festgesetzt. In diesem Fall werden dem Fertigungsauftrag beim Erstellen fünf Chargennummern zugewiesen.

    ![Seite mit den Nummerngruppen nachverfolgen](media/tracking-number-group-predefined.png "Die Seite mit den Nummerngruppen zum Nachverfolgen")

1. Stellen Sie andere Werte nach Bedarf ein und wählen Sie diese Nachverfolgungs-Nummerngruppe als Chargennummerngruppe für freigegebene Produkte aus, für die Sie dieses Szenario verwenden möchten.

Wenn Sie dieses Szenario verwenden, wird das Feld **Chargennummer**, das die Seite **Fortschritt melden** auf dem Einzelvorgangskartengerät bereitstellt, eine Dropdown-Liste anzeigen, in das Mitarbeiter einen beliebigen Wert eingeben können.

![Fortschrittsseite mit einer Liste von vordefinierten Chargennummern](media/job-card-device-batch-predefined.png "Fortschrittsseite mit einer Liste von vordefinierten Chargennummern")

### <a name="set-up-a-tracking-number-group-that-automatically-assigns-batch-numbers"></a>Richten Sie eine Nachverfolgungs-Nummerngruppe ein, die automatisch Chargennummern zuweist

Wenn Chargennummern ohne Eingabe durch den Mitarbeiter automatisch zugewiesen werden sollen, führen Sie die folgenden Schritte aus, um eine Nachverfolgungsnummerngruppe einzurichten.

1. Gehen Sie zu **Bestandsverwaltung \> Installieren \> Ausmaße \> Nachverfolgung von Nummerngruppen**.
1. Erstellen oder wählen Sie die einzurichtende Nachverfolgungs-Nummerngruppe.
1. Auf dem Inforegister **Allgemein** stellen Sie die Option **Nur für Bestandtransaktionen** auf **Nein** fest.
1. Stellen Sie die Option **Manuell** auf **Nein** ein.

    ![Seite mit den Nummerngruppen nachverfolgen](media/tracking-number-group-fixed.png "Seite mit den Nummerngruppen nachverfolgen")

1. Stellen Sie andere Werte nach Bedarf ein und wählen Sie diese Nachverfolgungs-Nummerngruppe als Chargennummerngruppe für freigegebene Produkte aus, für die Sie dieses Szenario verwenden möchten.

Wenn Sie dieses Szenario verwenden, wird das Feld **Chargennummer**, das die Seite **Fortschritt melden** anzeigt, auf dem Einzelvorgangskartengerät einem Wert anzeigen, aber die Mitarbeiter können diesen nicht bearbeiten.

![Fortschrittsseite mit einem Feld für eine feste Chargennummern melden](media/job-card-device-batch-fixed.png "Fortschrittsseite mit einem Feld für eine feste Chargennummern melden")

## <a name="report-as-finished-to-a-license-plate"></a>Als abgeschlossen an eine Kennzeichnung melden

Fortgeschrittene Lagerprozesse können die Kennzeichenabmessung verwenden, um den Lagerbestand an Lagerstandorten zu verfolgen, die für diesen Zweck eingerichtet wurden. In diesem Fall ist dies Kennzeichnung erforderlich, wenn ein Mitarbeiter Mengen als fertig meldet.

### <a name="enable-license-plate-reporting-and-label-printing"></a>Kennzeichenbeschriftungs und Druck aktivieren

Um die in diesem Abschnitt beschriebenen Funktionen nutzen zu können, müssen Sie die [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) verwenden, um die folgenden Funktionen zu aktivieren (in dieser Reihenfolge):

1. Das Kennzeichen für Fertigmeldung wurde zum Einzelvorgangslistengerät hinzugefügt.
1. Aktivieren Sie die automatische Generierung der Kennzeichennummer, wenn die Berichtserstellung im Einzelvorgangskartengerät abgeschlossen wurde
1. Beschriftung vom Einzelvorgangs-Kartengerät aus drucken

### <a name="set-up-reporting-as-finished-to-a-license-plate"></a>Legen Sie die Kennzeichnung als abgeschlossen fest

Führen Sie die folgenden Schritte aus, um zu steuern, ob Mitarbeiter eine vorhandene Kennzeichnung wiederverwenden oder eine neue Kennzeichnung erstellen sollen, wenn sie Mengen als fertig melden.

1. Wechseln Sie zu **Produktionssteuerung \> Einrichtung \> Fertigungssteuerung \> Einzelvorgangsliste für Geräte konfigurieren**.
2. Legen Sie folgende Optionen für jedes Gerät fest:

    - **Kennzeichen erstellen** – Setzen Sie diese Option auf **Ja**, um jedes Mal eine neue Kennzeichnung für jeden Bericht als beendet zu melden. Legen Sie es auf **Nein** fest, wenn eine bestehende Kennzeichnung als beendet verwendet werden soll.
    - **Etikett drucken** – Legen Sie diese Option auf **Ja** fest, wenn eine Arbeitskraft ein Kennzeichenetikett für jeden Bericht als beendet drucken muss. Legen Sie es auf **Nein** fest, wenn kein Etikett erforderlich ist. 

![Einzelvorgangsliste für Geräteseite](media/config-job-card-raf.png "Einzelvorgangsliste für Geräteseite")

> [!NOTE]
> Um das Etikett zu konfigurieren, gehen Sie zu **Lagerortverwaltung \> Einstellung \> Dokumentrouting \> Dokumentrouting**. Weitere Informationen finden Sie unter [Aktivieren Sie das Drucken von Kennzeichenetiketten](../warehousing/tasks/license-plate-label-printing.md).
