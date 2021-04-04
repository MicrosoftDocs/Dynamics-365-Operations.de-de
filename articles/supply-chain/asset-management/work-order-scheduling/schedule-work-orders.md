---
title: Arbeitsaufträge terminieren
description: In diesem Abschnitt wird erläutert, wie Sie Arbeitsaufträge im Anlagenmanagement planen.
author: josaw1
manager: tfehr
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderSchdulePreviewPart, EntAssetWorkOrderScheduleExclusively, EntAssetWorkOrderSchduleInfoPart, EntAssetWorkOrderScheduleListPage, EntAssetWorkOrderSchedule, EntAssetWorkOrderScheduleDelete
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6c9a15d90d2cb5d24bcc18f8cbd4f0076efaf6a8
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263831"
---
# <a name="schedule-work-orders"></a>Arbeitsaufträge terminieren

[!include [banner](../../includes/banner.md)]

 

In diesem Abschnitt wird erläutert, wie Sie Arbeitsaufträge im Anlagenmanagement planen. 

Die erforderliche Stundenanzahl für einen Arbeitsauftrag ergibt sich aus der Summe der prognostizierten Stunden auf abzüglich der gebuchten Stunden. Wenn mehr Zeit benötigt wird, muss die Prognose entsprechend angepasst werden. In **Anlagenmanagement** > **Allgemein** > **Arbeitsaufträge** > **Alle Arbeitsaufträge** oder **Aktive Arbeitsaufträge** können Sie Prognosen zu einem Arbeitsauftrag einsehen oder bearbeiten, indem Sie den Arbeitsauftrag auswählen und **Prognose** auf der Registerkarte **Arbeitsauftrag** anklicken. Wenn Arbeitsaufträge erstellt und geschätzt wurden, ist der nächste Schritt in der Ausführung der Arbeitsaufträge, die erforderlichen Wartungsarbeiter und Werkzeuge zuzuweisen.

Es können nur Arbeitsaufträge mit einem Arbeitsauftragslebenszyklusstatus terminiert werden, der eine Terminierung ermöglicht. Die Zulassungsplanung ist in **Anlagenmanagement** > **Einrichtung** > **Arbeitsaufträge** > **Lebenszykluszustände** > **Allgemein** FastTab > **Zulässige Planung** Umschalt-Schaltfläche eingerichtet.

1. Klicken Sie auf **Anlagenmanagement** > **Allgemein** > **Arbeitsaufträge** > **Alle Arbeitsaufträge**.

2. Wählen Sie in der Liste die Arbeitsaufträge aus, die Sie terminieren möchten. Sie können die Liste beispielsweise nach **Aktueller Lebenszykluszustand** sortieren.

3. Klicken Sie auf der Registerkarte **Allgemein** auf **Terminplan**.

4. Im Dialog **Arbeitsaufträge terminieren** können Sie bei Bedarf Auswahlmöglichkeiten bezüglich erwartetem Starttermin und Servicelevel hinzufügen. Wenn der Planungsprozess Kapazitätsengpässe bei bereits für andere Jobs eingeplanten Ressourcen beachten soll, stellen Sie sicher, dass die Umschalttasten **Anlage**, **Werkzeug** und **Arbeiter** auf „Ja“ gesetzt sind.

    [!NOTE]
    Wenn Sie die Schaltflächen **Anlage**, **Werkzeug** und **Arbeiter** auf „Nein“ umschalten, werden bestehende Reservierungen ignoriert. Im Infolog wird eine Liste der sich überschneidenden Arbeitsauftragspläne angezeigt, und Sie können auf die Nachrichten klicken, um einen Arbeitsauftrag zu öffnen und bei Bedarf neu zu terminieren.

5. Um detaillierte Informationen über den Planungsprozess zu erhalten, wählen Sie „Ja“ auf der Umschalttaste **Lang**. Das bedeutet, dass detaillierte Informationen über die berechneten Werte der Arbeitsaufträge und Wartungspersonal im Infolog angezeigt werden.

6. Klicken Sie auf **OK**, um den Planungsprozess zu starten.

7. Wenn die Planung abgeschlossen ist, zeigt ein Infolog die Anzahl der geplanten Arbeitsaufträge sowie detailliertere Informationen, wenn die Umschalttaste **Lang** auf „Ja“ gesetzt wurde.

>[!NOTE]
>Arbeitsaufträge werden in einem Zyklus pro Arbeitsauftrag geplant, nicht pro Arbeitsauftrag. Sie können den Dialog **Arbeitsaufträge planen** auch direkt in **Anlagenmanagement** > **Periodisch** > **Arbeitsaufträge** > **Arbeitsaufträge terminieren** öffnen. Treffen Sie Ihre Auswahl und klicken Sie auf **OK**, um die Arbeitsvorbereitung zu starten. Es ist möglich, die Arbeitsvorbereitung als Batch-Job im Dialog **Arbeitsaufträge einplanen** > der **Ausführung im Hintergrund** FastTab einzurichten.

*Beispiel:* In der folgenden Abbildung wird die Formel, die in das Feld **Erwarteter Start** eingefügt wird, eine Arbeitsauftragsplanung für alle Arbeitsaufträge mit erwartetem Startdatum in einer Woche von heute und später erzeugen. Diese Formel kann nützlich sein, wenn Sie die Arbeitsauftragsplanung fortlaufend durchführen, aber Sie möchten sicherstellen, dass die für die nächsten 5-6 Tage geplanten Arbeitsaufträge nicht verschoben werden.

![Abbildung 1](media/03-work-order-scheduling.png)

Die auf Arbeitsaufträge bezogene Arbeitsauftragsart kann die Terminierung für einen Wartungsmitarbeiter einrichten (**Anlagenmanagement** > **Einrichtung** > **Aufträge** > **Auftragsarten** > **Ein Wartungsmitarbeiter** Umschalttaste auf „Ja“ eingestellt). Das bedeutet, dass, wenn die Auftragsart auf einem Arbeitsauftrag verwendet wird, die Umschalttaste **Ein Wartungsarbeiter** automatisch auf „Ja“ auf der Seite **Alle Arbeitsaufträge** Detailseite > **Kopf** Ansicht > **Terminplan** FastTab gesetzt wird. Bei der Arbeitsauftragsplanung werden alle auf dem Arbeitsauftrag erstellten Arbeitsaufträge anschließend auf den gleichen Instandhalter eingeplant. Bei Bedarf können Sie die Auswahl über die Schaltfläche **Ein Wartungsarbeiter** Umschalten in **Alle Arbeitsaufträge** bearbeiten, um die Planung mehrerer Mitarbeiter oder eines Mitarbeiters auf den Arbeitsaufträgen zu ermöglichen.

Der Terminierungsprozess im Anlagenmanagement berücksichtigt mehrere Faktoren in der Terminberechnung:

- Berechnung der Ergebnisse sowohl für Arbeitsaufträge als auch für Wartungspersonal. Die Werte für Arbeitsaufträge und Wartungspersonal sind in **Anlagenmanagementparameter** hinterlegt. 
- Überprüfung auf übereinstimmende Kompetenzen, d.h. Fähigkeiten und Zertifikate, die zur Erfüllung der Aufgabe erforderlich sind. Fähigkeiten und Zertifikate sind auf Wartungspersonal im Modul **Personalressourcen** (**Personalressourcen** > **Arbeiter** > **Arbeiter** > ausgewählte Mitarbeiter in der Liste **Arbeiter** Tab > **Kompetenzen** Abschnitt > **Skills** und **Zertifikate** Schaltflächen) eingerichtet. Außerdem können Fähigkeiten und Zertifikate zu den Arten von Wartungsaufträgen und Wartungsaufträgen hinzugefügt werden. Weitere Informationen zu Kompetenzen und Wartungsauftragsarten finden Sie unter [Wartungsauftragsartenkategorien und Wartungsauftragsarten, Varianten von Wartungsauftragsarten, Wartungsauftragsgewerke und Wartungschecklisten](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).  

## <a name="scores-used-in-work-order-scheduling"></a>Bewertungen für die Arbeitsvorbereitung

Die Berechnung der Punktzahlen für einen Arbeitsauftrag basiert auf dem erwarteten Startdatum und dem Servicelevel des Arbeitsauftrags.

**Startdatum** Berechnung: Für jedes zukünftige Datum, das aus dem erwarteten Startdatum berechnet wird, wird der Startdatumswert subtrahiert und mit dem Wert multipliziert, der in den folgenden Beispielen „10“ ist.

**Kritik** Berechnung: Kritikalitätswert multipliziert mit der kritischen Größe des Arbeitsauftrags.

**Service Level** Kalkulation: Service-Level-Wert geteilt durch den Service-Level auf dem Arbeitsauftrag.

In den folgenden Beispielen ist der kritische Wert „2“ und die Service Level Werte „5“ und „100“.

**Beispiel 1:** Übersicht

| Arbeitsauftrags-ID | Erwartetes Anfangsdatum | Kritische Arbeitsaufträge | Arbeitsauftrags-Leistungsebene | Herstellkostenkalkulation               | Punktzahl      |
|---------------|---------------------|------------------------|--------------------------|---------------------------|------------|
| WO-00010816   | Morgen            | 2                      | 20              | (-1 \* 10) + (2 \* 2) + 5 / 20     | \- 5.75    |
| WO-00010817   | In zwei Tagen   | 2                      | 20              | (-2 \* 10) + (2 \* 2) + 5 / 20     | \- 15.75   |
| WO-00010818   | In zwei Tagen   | 3                      | 5               | (-2 \* 10) + (2 \* 3) + 5 / 5      | \- 13      |

Die Arbeitsaufträge werden in der folgenden Reihenfolge eingeplant: WO-000108 **16**, WO-000108 **18**, WO-000108 **17**.

**Beispiel 2:**

| Arbeitsauftrags-ID | Erwartetes Anfangsdatum | Kritische Arbeitsaufträge | Arbeitsauftrags-Leistungsebene | Herstellkostenkalkulation                 | Punktzahl    |
|---------------|---------------------|------------------------|---------------------|----------------------------------|----------|
| WO-00010816   | Morgen            | 2                      | 20                  | (-1 \* 10) + (2 \* 2) + 100 / 20 | \- 1     |
| WO-00010817   | In zwei Tagen   | 2                      | 20                  | (-2 \* 10) + (2 \* 2) + 100 / 20 | \- 11    |
| WO-00010818   | In zwei Tagen   | 3                      | 5                   | (-2 \* 10) + (2 \* 3) + 100 / 5  | 6        |

Wenn der Service Level Wert auf'100' statt '5' erhöht wird, wird der Terminierungsauftrag erstellt: WO-000108 **18**, WO-000108 **16**, WO-000108 **17**.

Die Bewertungspunkte für die Berechnung, welche Wartungsmitarbeiter an den Arbeitsaufträgen arbeiten sollen, sind alle als Zahlen festgelegt, die bei der Arbeitsauftragsplanung zu jeder Kalkulation des Wartungsmitarbeiters hinzugefügt werden. Der Wartungsarbeiter mit der höchsten Punktzahl wird im Arbeitsauftrag ausgewählt. Hier ist eine kurze Beschreibung der Ergebnisse der Wartungsarbeiten:

| Bewertung für Wartungsarbeiter| Beschreibung |
|---|---|
| Verantwortliche Arbeitskraft | Wenn der Wartungsarbeiter im Arbeitsauftrag als verantwortlicher Mitarbeiter ausgewählt wird, wird die Note hinzugefügt. |
| Zuständige Wartungsarbeitergruppe | Wenn der Wartungsarbeiter Teil der zuständigen Wartungsarbeitsgruppe auf dem Arbeitsauftrag ist, wird die Note hinzugefügt. |
| Bevorzugter Wartungsarbeiter         | Wenn der Arbeiter als bevorzugter Wartungsarbeiter für die Anlage ausgewählt wird, wird die Punktzahl hinzugefügt. |
| Bevorzugte Wartungsarbeitergruppe   | Wenn der Arbeiter Teil der bevorzugten Wartungsarbeitsgruppe auf der Anlage ist, wird die Punktzahl hinzugefügt.  |
| Ort  | Wenn Ihr Unternehmen Technische Standorte verwendet, erhalten Wartungsmitarbeiter die volle Punktzahl, wenn sie sich auf dem mit der Anlage verbundenen Technischen Standorts befinden. Wenn der Technische Standort der Anlage einen übergeordneten Standort hat, erhalten die Wartungsmitarbeiter auf diesem Technischen Standort die 1/2 Punktzahl. Wenn dieser Standort auch ein übergeordnetes Objekt hat, erhalten die Wartungsmitarbeiter an diesem Standort 1/3 der Punkte. Wenn dieser Standort auch eine übergeordnete Position hat, erhalten die Wartungsmitarbeiter an diesem Standort 1/4 Punktzahl, und so weiter. Wenn Ihr Unternehmen Anlagenstandorte verwendet, die wir nicht empfehlen, werden Standort, Fläche und Zone zur Berechnung der Standortwerte herangezogen. Arbeitskräfte erhalten volle Punkte, wenn sie sich am selben Standort, im selben Bereich und der selben Zone befinden, wie die zugeordnete Anlage. Wenn der Standort des Arbeiters nur mit Standort und Fläche übereinstimmt, beträgt der Bewertungswert für den Wartungsarbeiter 2/3 der Gesamtpunktzahl. Wenn der Standort des Wartungspersonals nur mit dem Standort übereinstimmt, beträgt der Bewertungswert für den Wartungsperson 1/3 der Gesamtpunktzahl. |
| Startdatum der Arbeitskraft  | Für jedes Datum, an dem das geplante Startdatum nach dem erwarteten Startdatum liegt, wird der Wert subtrahiert.  |

>[!NOTE]
>Wenn ein Wert auf „0“ gesetzt wird, wird dieser Wert nicht berechnet. Dies ist z.B. dann sinnvoll, wenn Sie den verantwortlichen Mitarbeiter nicht in Ihre Planung einbeziehen wollen.

## <a name="competencies-used-in-work-order-scheduling"></a>Kompetenzen für die Arbeitsvorbereitung

Qualifikationen und Zertifikatsanforderungen können auf Instandhaltungsjobtypen (**Anlagenmanagement** > **Einrichtung** > **Jobs** > **Wartungsjobtypen**) und Instandhaltungsaufträge (**Anlagenmanagement** > **Einrichtung** > **Aufträge** > **Instandhaltungsauftragswechsel**) eingerichtet werden. 

Wartungsauftragsarten und Wartungsauftragsarten werden bei Arbeitsaufträgen ausgewählt. Wenn Fähigkeiten oder Zertifikate für eine Wartungsauftragsart oder eine Wartungsauftragsart ausgewählt wurden und diese Wartungsauftragsart oder diese Wartungsauftragsart für eine Auftragsarbeit verwendet wird, werden nur Wartungsarbeiter mit übereinstimmenden Fähigkeiten und Zertifikaten für die Arbeit an der Auftragsarbeit vorgesehen.

<a name="gantt"></a>

## <a name="work-with-scheduled-work-orders-using-a-gantt-chart"></a>Arbeiten mit geplanten Arbeitsaufträgen mithilfe eines Gantt-Diagramms

Die Funktion **Gantt-Diagramm für geplante Arbeitsaufträge** bietet eine grafische Oberfläche, über die Sie Ihre Arbeitsaufträge anzeigen und neu planen können.

So zeigen Sie das Gantt-Diagramm an und arbeiten damit:

1. Wechseln Sie zu **Anlagenverwaltung > Arbeitsaufträge > Gantt-Diagramm für geplante Arbeitsaufträge**.

1. Verwenden Sie die Dropdownlisten und Felder im Abschnitt **Einstellungen**, um festzulegen, welcher funktionale Standort, welche Zeitspanne und welche Zeitskala im Gantt-Diagramm angezeigt werden sollen.

1. Wählen Sie **Anwenden** aus.

    - Das Gantt-Diagramm wird aktualisiert, um die geplanten Arbeitsaufträge anzuzeigen, die Ihren Einstellungen entsprechen. Jeder Arbeitsauftrag wird durch ein blaues Rechteck dargestellt.
    - Um einen angezeigten Arbeitsauftrag neu zu planen, wählen Sie ihn aus und ziehen Sie ihn auf das entsprechende neue Datum und die entsprechende neue Uhrzeit.

1. Wenn Sie Änderungen vorgenommen haben, wählen Sie im Aktivitätsbereich **Speichern** aus, um sie zu speichern.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]