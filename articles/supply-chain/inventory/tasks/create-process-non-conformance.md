---
title: Erstellen und Verarbeiten von Qualitätsmängeln
description: Dieses Thema beschreibt, wie Sie das Management von Qualitätsmängeln auf der Basis eines bestehenden Qualitätsprüfungsauftrags durchführen können.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 032f5b712c2be5312524129cd25e655e778f5f44
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7580863"
---
# <a name="create-and-process-nonconformances"></a>Erstellen und Verarbeiten von Qualitätsmängeln

[!include [banner](../../includes/banner.md)]

Dieses Thema beschreibt, wie Sie das Management von Qualitätsmängeln auf der Basis eines bestehenden Qualitätsprüfungsauftrags durchführen können. Typischerweise wird das Qualitätsmangel-Management von einem Qualitätssachbearbeiter durchgeführt. Als Voraussetzung müssen Sie einen Qualitätsprüfungsauftrag zur Verfügung haben. (Informationen zum Erstellen eines Qualitätsprüfungsauftrags finden Sie unter [Prüfen der Qualität von Waren](inspect-quality-goods.md).)

Bevor ein Benutzer die Genehmigung eines Qualitätsmangels verarbeiten kann, muss ihm ein worker im Feld **Person** auf der Seite **Benutzer** zugewiesen werden. Zusätzlich muss in den Benutzeroptionen die Option **Dokumentenbearbeitung aktivieren** auf *Ja* festgelegt werden, bevor der Benutzer die Dokumentennotizen verwenden kann.

## <a name="create-a-nonconformance"></a>Erstellen einer Nichtübereinstimmung

Um einen Qualitätsmangel zu erstellen, gehen Sie wie folgt vor.

1. Gehen Sie zu **Bestandsverwaltung \> Periodische Aufgaben \> Qualitätsmanagement \> Nichtkonformitäten**.
1. Wählen Sie im Aktivitätsbereich **Neu**.
1. Wählen Sie im Dialogfeld **Nichtkonformität erstellen** im Feld **Problemtyp** die Art des Problems, das während des Inspektionsprozesses gefunden wurde.
1. Wählen Sie **OK**.

## <a name="approve-or-reject-a-nonconformance"></a>Einen Qualitätsmangel genehmigen oder ablehnen

Um einen Qualitätsmangel zu genehmigen oder abzulehnen, führen Sie diese Schritte aus.

1. Gehen Sie zu **Bestandsverwaltung \> Periodische Aufgaben \> Qualitätsmanagement \> Nichtkonformitäten**.
1. Wählen Sie in der Liste den Qualitätsmangel, den Sie aktualisieren möchten.

    > [!NOTE]
    > Sie können eine Korrektur nur zu Qualitätsmängeln hinzufügen, die genehmigt sind.

1. Wählen Sie im Aktivitätsbereich **Funktionen \> Qualitätsmangel genehmigen**, um den Qualitätsmangel zu genehmigen oder **Funktionen \> Qualitätsmangel ablehnen**, um ihn abzulehnen. Sie können genehmigte Qualitätsmängel mit [verwandten Vorgängen](../quality-operations.md) verknüpfen. Auf diese Weise können Sie die Arbeit, die im Rahmen der Behandlung von Qualitätsmängeln und der Verarbeitung von Korrekturen geleistet wird, in Datensätzen festhalten.
1. Sie werden aufgefordert, Ihre Auswahl zu bestätigen. Wählen Sie **Ja** aus, um fortzufahren.

## <a name="add-operations-and-other-details-to-nonconformances"></a>Hinzufügen von Vorgängen und anderen Details zu Qualitätsmängeln

Nachdem Sie einen Qualitätsmangel erstellt haben, können Sie beginnen, verwandte Vorgänge hinzuzufügen und zusätzliche Informationen zu diesen Vorgängen anzugeben. Sie können verwandte Vorgänge nur für Qualitätsmängel hinzufügen, die genehmigt sind.

Neben den Basisinformationen können Sie einem Vorgang die folgenden Details hinzufügen:

- **Elemente** – Sie können eine Liste von Elementen erstellen, die verbraucht werden, um die Korrektur durchzuführen. Bei den Elementen kann es sich z. B. um Produkte handeln, die zur Reparatur von Geräten benötigt werden, oder um Zutaten, die zur Nachbearbeitung eines Fertigprodukts benötigt werden.
- **Qualitätsbelastungen** – Sie können eine Liste von Belastungen erstellen, die angefallen sind oder nach außen abgerechnet wurden.
- **Arbeitszeitnachweis** – Sie können ein Protokoll über die Zeit erstellen, die jeder worker mit dem Vorgang verbringt.

Die übrigen Einstellungen sind optional. Die Kosten für jedes Element, die Qualitätsbelastungen und die Zeittabelle werden summiert und auf dem Vorgang angezeigt. Sie können das Feld **Kalkulation** im Vorgang nicht direkt bearbeiten.

### <a name="create-an-operation-for-a-nonconformance"></a>Erzeugen eines Vorgangs für einen Qualitätsmangel

Um einen Vorgang für einen Qualitätsmangel zu erstellen, folgen Sie diesen Schritten.

1. Gehen Sie zu **Bestandsverwaltung \> Periodische Aufgaben \> Qualitätsmanagement \> Nichtkonformitäten**.
1. Wählen Sie in der Liste den Qualitätsmangel, den Sie aktualisieren möchten.

    > [!NOTE]
    > Sie können Vorgänge nur für Qualitätsmängel, die genehmigt sind, hinzufügen oder aktualisieren.

1. Wählen Sie im Aktivitätsbereich **Bezogene Vorgänge**.
1. Wählen Sie auf der Seite **Bezogene Vorgänge** im Aktivitätsbereich **Neu**, um dem Raster eine Zeile hinzuzufügen. Legen Sie für die neue Zeile die folgenden Felder fest:

    - **Vorgang** – Wählen Sie den Code des Vorgangs, der für den Qualitätsmangel durchgeführt wird.
    - **Grund** – Geben Sie eine detaillierte Beschreibung ein, die erklärt, warum der Vorgang erforderlich ist.
    - **Verkaufsauftrag** – Wenn sich der gewählte Vorgangscode auf die Art des Verkaufsauftrags bezieht, wählen Sie den Verkaufsauftrag, mit dem Sie den Vorgang verknüpfen.
    - **Einkaufsbestellung** – Wenn der gewählte Vorgangscode mit der Art der Bestellung zusammenhängt, wählen Sie die Einkaufsbestellung, mit der Sie den Vorgang verknüpfen.

1. Schließen Sie die Seiten.

### <a name="add-items-to-an-operation"></a>Hinzufügen von Elementen zu einem Vorgang

Um Elemente zu einem Vorgang hinzuzufügen, führen Sie diese Schritte aus.

1. Gehen Sie zu **Bestandsverwaltung \> Periodische Aufgaben \> Qualitätsmanagement \> Nichtkonformitäten**.
1. Wählen Sie in der Liste den Qualitätsmangel, den Sie aktualisieren möchten.

    > [!NOTE]
    > Sie können Vorgänge nur für Qualitätsmängel, die genehmigt sind, hinzufügen oder aktualisieren.

1. Wählen Sie im Aktivitätsbereich **Bezogene Vorgänge**.
1. Wählen Sie auf der Seite **Verknüpfte Vorgänge** den Vorgang aus, dem Sie Elemente hinzufügen wollen.
1. Klicken Sie im Aktivitätsbereich auf **Artikel**.
1. Wählen Sie auf der Seite **Bezogene Vorgänge** im Aktivitätsbereich **Neu**, um dem Raster eine Zeile hinzuzufügen. Legen Sie dann die folgenden Felder für die neue Zeile fest:

    - **Elementnummer** – Wählen Sie das Produkt, das als Teil des gewählten Vorgangs verbraucht wird.
    - **Menge** – Geben Sie die Anzahl der Elemente an, die verbraucht werden sollen.

    > [!NOTE]
    > Sie können die Kosten für das Element im Feld **Kosten** auf der Registerkarte **Allgemein** anzeigen. Die Kosten, die dort angezeigt werden, stammen von der Kalkulation, die auf der Seite **Freigegebenes Produkt** festgelegt ist. Die Kalkulation kann nicht direkt auf der Seite **Bezogener Vorgang Element** aktualisiert werden. Die Kosten aller Elemente, die auf der Seite **Bezogene Vorgangselemente** hinzugefügt werden, werden automatisch zum Feld **Kosten** auf der Seite **Bezogene Vorgänge** hinzugefügt.

1. Wiederholen Sie den vorherigen Schritt für jedes zusätzliche Element, das Sie hinzufügen müssen.
1. Schließen Sie die Seiten.

### <a name="add-quality-charges-to-an-operation"></a>Hinzufügen von Qualitätsbelastungen zu einem Vorgang

Um Qualitätsbelastungen zu einem Vorgang hinzuzufügen, führen Sie diese Schritte aus.

1. Gehen Sie zu **Bestandsverwaltung \> Periodische Aufgaben \> Qualitätsmanagement \> Nichtkonformitäten**.
1. Wählen Sie in der Liste den Qualitätsmangel, den Sie aktualisieren möchten.

    > [!NOTE]
    > Sie können Vorgänge nur für Qualitätsmängel, die genehmigt sind, hinzufügen oder aktualisieren.

1. Wählen Sie im Aktivitätsbereich **Bezogene Vorgänge**.
1. Wählen Sie auf der Seite **Verbundene Vorgänge** den Vorgang aus, dem Sie Qualitätsbelastungen hinzufügen wollen.
1. Wählen Sie im Aktionsbereich **Qualitätsbelastungen**.
1. Wählen Sie auf der Seite **Bezogene Vorgänge Belastungen** im Aktivitätsbereich die Option **Neu**, um dem Raster eine Zeile hinzuzufügen. Legen Sie für die neue Zeile die folgenden Felder fest:

    - **Gebührencode** – Wählen Sie die Qualitätsgebühr, die Sie hinzufügen möchten.
    - **Beschreibung** – Geben Sie eine detaillierte Beschreibung der Gebühr ein.
    - **Gebührenwert** – Geben Sie den Betrag der Gebühr ein.

1. Wiederholen Sie den vorherigen Schritt für jede zusätzliche Gebühr, die Sie hinzufügen müssen.
1. Schließen Sie die Seiten.

> [!NOTE]
> Der Betrag im Feld **Gebührenwert** wird automatisch für alle Qualitätsbelastungen summiert und zu allen anderen Beträgen im Feld **Kosten** auf der Seite **Bezogene Vorgänge** addiert.

### <a name="create-a-timesheet-on-an-operation"></a>Erstellen eines Stundenzettels für einen Vorgang

Führen Sie diese Schritte aus, um einem Vorgang einen Stundenzettel hinzuzufügen.

1. Gehen Sie zu **Bestandsverwaltung \> Periodische Aufgaben \> Qualitätsmanagement \> Nichtkonformitäten**.
1. Wählen Sie in der Liste den Qualitätsmangel, den Sie aktualisieren möchten.

    > [!NOTE]
    > Sie können Vorgänge nur für Qualitätsmängel, die genehmigt sind, hinzufügen oder aktualisieren.

1. Wählen Sie im Aktivitätsbereich **Bezogene Vorgänge**.
1. Wählen Sie auf der Seite **Verknüpfte Vorgänge** den Vorgang aus, zu dem Sie einen Stundenzettel hinzufügen möchten.
1. Wählen Sie im Aktivitätsbereich **Zeitplan**.
1. Wählen Sie auf der Seite **Zugehörige Vorgänge** im Aktivitätsbereich **Neu**, um dem Raster eine Zeile hinzuzufügen. Legen Sie für die neue Zeile die folgenden Felder fest:

    - **Datum** – Geben Sie das Datum an, an dem die Arbeit ausgeführt wurde. Standardmäßig ist dieses Feld auf das aktuelle Datum festgelegt.
    - **Arbeiter** – Wählen Sie den Mitarbeiter aus, der die Arbeit ausgeführt hat. Standardmäßig ist dieses Feld auf den worker festgelegt, der dem aktuellen Benutzer zugewiesen ist.
    - **Vorgangsstunden** – Geben Sie die Anzahl der Stunden ein, die an dem gewählten Vorgang gearbeitet wurden.
    - **Fakturiert** – Aktivieren Sie dieses Kontrollkästchen, wenn die Zeit einem Kunden oder Lieferanten auf einer Rechnung in Rechnung gestellt wurde.

    > [!NOTE]
    > Sie können die Kalkulation im Feld **Kosten** auf der Registerkarte **Allgemein** sehen. Die Kalkulation erfolgt mit dem Satz, den Sie auf der Seite **Parameter der Bestandsverwaltung** definieren.

1. Wiederholen Sie den vorigen Schritt für jede zusätzliche Zeile, die Sie hinzufügen müssen.
1. Schließen Sie die Seiten.

> [!NOTE]
> Der Betrag im Feld **Kosten** wird für alle Timesheet-Zeilen summiert und zu allen anderen Beträgen im Feld **Kosten** auf der Seite **Bezogene Vorgänge** addiert.

## <a name="add-a-correction-to-a-nonconformance"></a>Hinzufügen einer Korrektur zu einem Qualitätsmangel

Um eine Korrektur zu einem Qualitätsmangel hinzuzufügen, gehen Sie wie folgt vor.

1. Gehen Sie zu **Bestandsverwaltung \> Periodische Aufgaben \> Qualitätsmanagement \> Nichtkonformitäten**.
1. Wählen Sie in der Liste den Qualitätsmangel, den Sie aktualisieren möchten.

    > [!NOTE]
    > Sie können eine Korrektur nur zu Qualitätsmängeln hinzufügen, die genehmigt sind.

1. Wählen Sie im Aktivitätsbereich **Korrekturen**.
1. Wählen Sie auf der Seite **Korrekturen** im Aktivitätsbereich **Neu**, um dem Raster eine Zeile hinzuzufügen. Legen Sie für die neue Zeile die folgenden Felder fest:

    - **Diagnose** – Wählen Sie den Diagnosetyp, der die Art der Korrektur, die Sie erstellen, identifiziert.
    - **Mitarbeiter** – Wählen Sie die Person, die für die Korrektur verantwortlich ist.
    - **Korrekturpriorität** – Wählen Sie eine Option, um anzugeben, wie die Korrektur priorisiert werden soll (*Niedrig*, *Normal* oder *Hoch*).
    - **Anforderungsdatum** – Geben Sie das Datum ein, an dem die Korrekturmaßnahme angefordert wurde.
    - **Plan-Datum** – Geben Sie das Datum ein, an dem die Korrektur voraussichtlich abgeschlossen sein wird.
    - **Kurzfristige Lösung** – Aktivieren Sie dieses Kontrollkästchen, wenn die Korrekturmaßnahme den Qualitätsmangel nur für kurze Zeit korrigiert.

1. Schließen Sie die Seiten.

## <a name="mark-a-correction-as-completed"></a>Markieren Sie eine Korrektur als abgeschlossen

Um eine Korrektur eines Qualitätsmangels als abgeschlossen zu markieren, gehen Sie wie folgt vor.

1. Gehen Sie zu **Bestandsverwaltung \> Periodische Aufgaben \> Qualitätsmanagement \> Nichtkonformitäten**.
1. Wählen Sie in der Liste den Qualitätsmangel, den Sie aktualisieren möchten.

    > [!NOTE]
    > Sie können eine Korrektur nur zu Qualitätsmängeln hinzufügen, die genehmigt sind.

1. Wählen Sie im Aktivitätsbereich **Korrekturen**.
1. Wählen Sie auf der Seite **Korrekturen** im Raster die Korrektur aus, die Sie als erledigt markieren wollen.
1. Wählen Sie im Aktivitätsbereich **Erledigt markieren**.
1. Sie werden aufgefordert, Ihre Auswahl zu bestätigen. Wählen Sie **OK**, um fortzufahren. Das Feld **Erledigungsdatum und -uhrzeit** ist auf das aktuelle Datum und die aktuelle Uhrzeit festgelegt, und das Kontrollkästchen **Erledigt** ist aktiviert.
1. Schließen Sie die Seite.

## <a name="reopen-a-completed-correction"></a>Erneutes Öffnen einer abgeschlossenen Korrektur

Um eine abgeschlossene Korrektur erneut zu öffnen, führen Sie diese Schritte aus.

1. Gehen Sie zu **Bestandsverwaltung \> Periodische Aufgaben \> Qualitätsmanagement \> Nichtkonformitäten**.
1. Wählen Sie in der Liste den Qualitätsmangel, den Sie aktualisieren möchten.
1. Wählen Sie im Aktivitätsbereich **Korrekturen**.
1. Wählen Sie auf der Seite **Korrekturen** im Raster die Korrektur aus, die Sie wieder öffnen möchten.
1. Wählen Sie im Aktivitätsbereich **Wieder öffnen**.
1. Sie werden aufgefordert, Ihre Auswahl zu bestätigen. Wählen Sie **OK**, um fortzufahren. Der Wert im Feld **Erledigungsdatum und -uhrzeit** wird gelöscht, und das Kontrollkästchen **Erledigt** wird deaktiviert.
1. Schließen Sie die Seite.

Sie können jetzt zusätzliche Bearbeitungen oder Aktualisierungen an der Korrektur vornehmen. Wenn Sie fertig sind, können Sie die Korrektur wieder als abgeschlossen markieren.

## <a name="close-a-nonconformance"></a>Qualitätsmangel schließen

Um einen Qualitätsmangel zu schließen, führen Sie diese Schritte aus.

1. Wechseln Sie zu **Bestandsverwaltung \> Periodische Aufgaben \> Qualitätsmanagement \> Qualitätsprüfungsaufträge**.
1. Wählen Sie einen Qualitätsprüfungsauftrag im Raster aus.
1. Wählen Sie im Aktivitätsbereich **Abfragen \> Nichtkonformitäten**.
1. Wählen Sie auf der Seite **Nichtkonformitäten** die Ziel-Qualitätsmängel im Raster aus.
1. Wählen Sie im Aktivitätsbereich **Funktionen \> Nichtkonformität schließen**.
1. Sie werden aufgefordert, Ihre Auswahl zu bestätigen. Wählen Sie **Ja** aus, um fortzufahren.
1. Schließen Sie die Seiten.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Qualitätsmanagement – Übersicht](../quality-management-processes.md)
- [Qualitäts- und Qualitätsmangel-Management aktivieren](../enable-quality-management.md)
- [Mitarbeiter, der für die Genehmigung von Qualitätsmängeln verantwortlich ist](../quality-responsible-workers.md)
- [Quarantänezonen für Qualitätsmängel](../quality-quarantine-zones.md)
- [Diagnosetypen für Qualitätsmängel](../quality-diagnostic-types.md)
- [Qualitätsbelastungen für Qualitätsmängel](../quality-charges.md)
- [Vorgänge für Qualitätsmängel](../quality-operations.md)
- [Qualitätsmanagement für Lagerortprozesse](../quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
