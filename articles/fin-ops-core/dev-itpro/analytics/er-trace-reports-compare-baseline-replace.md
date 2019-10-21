---
title: Verbesserungen bei der Nachverfolgung erstellter ER-Berichtsergebnisse und Vergleich mit Ausgangswerten
description: Dieses Thema enthält Informationen dazu, wie die ER-Grundlagenfunktion in Microsoft Dynamics 365 for Finance and Operations Version 10.0.3 verbessert wurde (Juni 2019).
author: NickSelin
manager: AnnBe
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: a260be0f8659106907b26bf69bee3b33b09d0c24
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2181334"
---
# <a name="improvements-in-tracing-the-results-of-generated-er-reports-and-comparing-them-with-baseline-values"></a>Verbesserungen bei der Nachverfolgung erstellter ER-Berichtsergebnisse und Vergleich mit Ausgangswerten

[!include[banner](../includes/banner.md)]

In diesem Thema wird der erste Satz an Verbesserungen beschrieben, die an der Grundlagenfunktion des Frameworks der elektronischen Berichterstattung (ER) erfolgt sind. Diese Verbesserungen sind in Microsoft Dynamics 365 for Finance and Operations Version 10.0.3 (Juni 2019) und später verfügbar.

## <a name="automate-the-setting-of-baseline-rules"></a>Automatisieren Sie die Struktur der Grundlagenregeln

Im Thema [Von Trace generierte Berichtergebnisse und deren Vergleich mit Grundwerten](er-trace-reports-compare-baseline.md) wird erläutert, wie das ER-Framework konfiguriert werden muss, um Informationen zu ER-Formatausführungen gesammelt und die Ergebnisse dieser Durchläufe bewertet werden. Das Beispiel in diesem Thema zeigt die Schritte an, die abgeschlossen werden müssen.

Beispiele für solche Schritte:

- Führen Sie ein ER-Format aus, um eine ausgehende Datei zu generieren, und speichern Sie die Datei lokal.
- Fügen Sie die lokal gespeicherten Datei als Anhang dem Grundwert hinzu, der für ein ER-Format hinzugefügt wurde.
- Konfigurieren Sie die Grundwertregel für die hinzugefügte Grundregel. Diese Konfiguration umfasst die folgenden Schritte:

    - Geben Sie ein ER-Formatelement an, das verwendet wird, um eine ausgehende Datei zu generieren.
    - Wählen Sie die Anlage aus, die auf die generierte ausgehende Datei verweist.

> [!NOTE]
> Diese Schritte müssen manuell ausgeführt werden, auch wenn sie durch die neuen ER-Funktionen automatisiert werden können. Weitere Informationen über diese Funktion erhalten Sie, wenn Sie das folgende Beispiel abschließen.

## <a name="example-automate-the-setting-of-baseline-rules"></a>Beispiel: Automatisieren Sie die Struktur der Grundlagenregeln

Um die Schritte dieses Beispiels abzuschließen, müssen Sie zunächst die Schritte im Beispiel im Thema [Nachverfolgung erstellter Berichtsergebnisse und Vergleich mit Ausgangswerten](er-trace-reports-compare-baseline.md) bis durch den Abschnitt „Fügen Sie eine neue Grundlage für ein entworfenes ER-Format hinzu“ abschließen.

### <a name="review-added-baseline"></a>Prüfung des hinzugefügten Grundwerts

1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.
2. Wählen Sie **Grundwerte** aus.

    > [!NOTE]
    > Die Schaltfläche **Grundwerte** im Aktivitätsbereich ist nur verfügbar, wenn der ER-Benutzerparameter **Ausführung im Debugmodus** für das aktuelle Unternehmen aktiviert ist.

Der Grundwert wurde für das ausgewählte Format **Format zum erlernen der ER-Grundwerte** hinzugefügt, aber die Grundwertregeln für diesen Grundwert wurden noch nicht hinzugefügt.

![Seite für die Formatgrundlage für elektronische Berichterstellung](media/GER-BaselineSample-AddBaseline2.PNG "Screenshot der Formatgrundlagen für elektronische Berichterstellung")

### <a name="make-a-new-baseline-rule"></a>Erstellen eines neuen Grundwertregel

1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.
2. Erweitern Sie in der Struktur **Modell zum erlernen der ER-Grundwerte**.
3. Wählen Sie in der Struktur das Format **Modell zum erlernen der ER-Grundwerte\\Format zum Erlernen des ER-Grundwerts** aus.
4. Wählen Sie im Inforegister **Versionen** **Ausführen** aus.
5. Geben Sie im Feld **Eingabe-Id** den Wert **1** ein.
6. Legen Sie die Option **Erstellen von Grundwertdateien** auf **Ja** fest.
7. Wählen Sie **OK**.

    ![Dialogfeld für elektronische Berichtsparameter](media/GER-BaselineSample-FormatRunToMakeBaselineFile3.PNG "Screenshot des Dialogfelds für elektronische Berichtsparameter")

8. Wählen Sie **Grundwerte** aus.

    ![Seite für die Formatgrundlage für elektronische Berichterstellung](media/GER-BaselineSample-ReviewAddedBaselineLine.PNG "Screenshot der Formatgrundlagen für elektronische Berichterstellung")

    Die generierte ausgehende Datei wird dem Grundwert des ausgeführten ER-Formats automatisch angefügt. Die Grundwertregel wurde diesem Grundwert automatisch hinzugefügt und enthält auch die Referenz zur zugeordneten Datei.

9. Geben Sie im Feld **Name** **Grundlage 1** ein.
10. Geben Sie im Feld **Dateinamenmaske** **.xml** ein.
11. Wählen Sie **Speichern**.

### <a name="run-the-format"></a>Das Format ausführen

Sie können nun die verbleibenden Schritte im Beispiel im Thema [Nachverfolgung erstellter Berichtsergebnisse und Vergleich mit Ausgangswerten](er-trace-reports-compare-baseline.md) abschließen. Sie können mit „Führen Sie das entworfene ER-Format aus und prüfen Sie das Protokoll, um die Ergebnisse zu analysieren“ beginnen.

> [!NOTE]
> Wenn Sie den automatisch auf dem Inforegister**Ausgangswerte** hinzugefügte Ausgangswert löschen, wird die referenzierte Zuordnung nicht automatisch gelöscht.

## <a name="configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a>Konfigurieren Sie den Ausgangswert, sodass er sich konstant ändernde Teile der ER-Ausgabe ignoriert.

Wenn ein ER-Format konzipiert wurde, um Informationen zu enthalten, die geändert werden, wenn das Format ausgeführt wird, muss das Format obligatorisch die ER-Ausgangswertfunktion verwenden, um die generierten Ergebnisse mit Ausgangswerten zu vergleichen. Bei den Informationen kann es sich beispielsweise um das Verarbeitungsdatum und die entsprechende Uhrzeit oder den eindeutigen Bezeichner eines generierten Dokuments in verschiedenen Formaten (globaler eindeutiger Bezeichner \[GUID\], usw.) handeln. Mit den neuen ER-Funktionen können Sie die Ausgangswertregel konfigurieren, sodass sie veränderbare Elemente eines ER-Formats ignoriert, wenn das Format ausgeführt wird. Dies dient dem Zweck eines Vergleichs von Ausgangswerten mit den Ergebnissen der Formatausführung. Weitere Informationen über diese Funktion erhalten Sie, wenn Sie das folgende Beispiel abschließen.

## <a name="example-configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a>Beispiel: Konfigurieren Sie den Ausgangswert, sodass er sich konstant ändernde Teile der ER-Ausgabe ignoriert.

Um die Schritte dieses Beispiels abzuschließen, müssen Sie zunächst die Schritte im Beispiel im Thema [Nachverfolgung erstellter Berichtsergebnisse und Vergleich mit Ausgangswerten](er-trace-reports-compare-baseline.md) abschließen.

### <a name="modify-a-configured-er-format"></a>Ändern eines konfigurierten ER-Formats

1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.
2. Erweitern Sie in der Struktur **Modell zum erlernen der ER-Grundwerte**.
3. Wählen Sie in der Struktur das Format **Modell zum erlernen der ER-Grundwerte\\Format zum Erlernen des ER-Grundwerts** aus.
4. Wählen Sie **Designer** aus.
5. Wählen Sie in der Struktur **Ausgabe\\Dokument** aus.
6. Wählen Sie **Hinzufügen** aus.
7. Im Drop-Down-Dialogfeld in der Struktur, wählen Sie **XML \\ Attribut** aus.
8. Geben Sie im Feld **Name** **ProcessingDateTime** ein.
9. Wählen Sie **OK**.
10. Wählen Sie auf der Registerkarte **Zuordnung** in der Struktur **Ausgabe \\Dokument\\ProcessingDateTime** aus.
11. Wählen Sie **Formel bearbeiten** aus.
12. Geben Sie im Feld **Formel** den folgenden Ausdruck ein: **DATETIMEFORMAT(NOW(), "O")**
13. Wählen Sie **Speichern** und dann **Test** aus.
14. Wählen Sie **Test** erneut aus, um den konfigurierten Ausdruck zu testen.

    ![Formeldesignerseite](media/GER-BaselineSample-DefineProcessingDTExpression.PNG "Screenshot der Formeldesignerseite")

    > [!NOTE]
    > Die Registerkarte **Testergebnis** gibt an, dass der konfigurierte Ausdruck einen unterschiedlichen Datums-und Uhrzeitwert zurückgibt, wenn sie angerufen wird.

15. Schließen Sie die Seite **Formeldesginer** und wählen Sie **Speichern** aus.

    ![Formatdesignerseite](media/GER-BaselineSample-FormatMappingDesign2.PNG "Screenshot der Formatdesignerseite")

16. Seite **Format-Designer** schließen.

### <a name="remove-an-existing-baseline-rule"></a>Entfernen Sie eine vorhandene Ausgangaswertregel

1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.
2. Wählen Sie **Ausgangswerte** aus.
3. In der Liste der Ausgangswerte wählen Sie den Ausgangswert aus, der für das Format **Format zum erlernen von ER-Ausgangswerten** konfiguriert wird.
4. Auf dem Inforegister **Ausgangswerte** wählen Sie **Löschen** aus, um die Ausgangswertregel zu entfernen, die Sie zuvor konfiguriert haben.

![Seite für die Formatgrundlage für elektronische Berichterstellung](media/GER-BaselineSample-AddBaseline3.PNG "Screenshot der Formatgrundlagen für elektronische Berichterstellung")

### <a name="define-replacements-for-bindings-of-designed-er-format"></a>Definieren Sie Ersatz für Bindungen eines entworfenen ER-Formats

1. Wählen Sie auf der Seite **Konfigurationen** auf dem Inforegister **Ersatz** die Option **Komponenten auswählen** aus.
2. In der Formatkomponentenstruktur erweitern Sie den Knoten **Ausgabe**, erweitern Sie **Ausgabe \\Dokument** und aktivieren Sie anschließend das Kontrollkästchen für **Ausgabe \\Dokument\\ProcessingDateTime**.

    ![Dialogfeld „Komponenten auswählen“](media/GER-BaselineSample-SelectComponentForBindingReplacement.PNG "Screenshot des Dialogfelds „Komponenten auswählen“")

3. Wählen Sie **OK**.

![Seite für die Formatgrundlage für elektronische Berichterstellung](media/GER-BaselineSample-AddBaseline4.PNG "Screenshot der Formatgrundlagen für elektronische Berichterstellung")

Die ausgewählte ER-Formatkomponente wurde der Liste der Komponenten auf dem Inforegister **Ersetzungen** hinzugefügt. Wenn das Basis-ER-Format in Debugmodus ausgeführt wird, wird die Bindung des Formats für jede Komponente durch die Bindung ersetzt, die in der Spalte **Binden** angezeigt wird. Um die Standardbindung für eine Komponente zu ändern, die im Inforegister **Ersetzungen** angezeigt wird, wählen Sie **Bearbeiten** aus.

### <a name="make-a-new-baseline-rule"></a>Erstellen eines neuen Grundwertregel

Führen Sie die Schritte im Abschnitt „Beispiel: Automatisieren Sie die Struktur der Grundlagenregeln“ oben in diesem Thema aus. Eine Benachrichtigung warnt Sie, dass die ausgehende Datei mit Ausgangswerteinstellungen erstellt wurde, und dass eine erzwungene Ersetzung der Formatbindungen aufgetreten ist.

![Benachrichtigung auf der Seite „Konfigurationen“](media/GER-BaselineSample-FormatRunToMakeBaselineFile4.PNG "Screenshot der Benachrichtigung auf der Seite „Konfigurationen“")

### <a name="suppress-warnings-about-the-replacement-of-format-bindings"></a>Warnungen zur Ersetzung von Formatbindungen unterdrücken

Durch das Festlegen bestimmter ER-Parameter können Sie Benachrichtigungen unterdrücken, die vor der Ersetzung von Formatbindungen warnen. Diese Unterdrückung kann hilfreich sein, wenn Formatbindungen in einem unbeaufsichtigten Modus ersetzt werden, indem Regression Suite Automation Tool verwndet wird. In diesem Fall kann die Warnung als ein Fehler des Testfalls, der ausgeführt wird, betrachtet werden.

1. Wählen Sie auf der Seite **Konfigurationen** im Aktivitätsbereich auf der Registerkarte **Konfigurationen** die Option **Benutzerparameter** aus.
2. Legen Sie die Option **Ausgangswertwarnungen unterdrücken** auf **Ja** fest, und wählen Sie dann **OK** aus.

![Benutzerparameterdialogfeld](media/GER-BaselineSample-ERUserParameters1.png "Screenshot des Benutzerparameterdialogfelds")

### <a name="review-the-generated-baseline-file"></a>Überprüfen Sie die erstellte Ausgangswertdatei

1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.
2. Wählen Sie **Ausgangswerte** aus.
3. Wählen Sie **Anhänge** aus.

    ![Anhangseite](media/GER-BaselineSample-AttachedBaselineFile.PNG "Screenshot der Anhangseite")

    > [!NOTE]
    > Die generierte Datei beinhaltet das Verarbeitungsdatum und den Zeittext (**"#"**) von der Bindung, die in der hinzugefügten Ausgangswertregel konfiguriert wurde, nicht aus der Bindung des Formats.

4. Schließen Sie die Seite **Anhänge**.

### <a name="run-the-designed-er-format-and-review-the-log-to-analyze-the-results"></a>Führen Sie das entworfene ER-Format aus und prüfen Sie das Protokoll, um die Ergebnisse zu analysieren

1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.
2. Erweitern Sie in der Struktur **Modell zum erlernen der ER-Grundwerte**.
3. Wählen Sie in der Struktur das Format **Modell zum erlernen der ER-Grundwerte\\Format zum Erlernen des ER-Grundwerts** aus.
4. Wählen Sie im Inforegister **Versionen** **Ausführen** aus.
5. Geben Sie im Feld **Eingabe-Id** den Wert **1** ein.
6. Wählen Sie **OK**.
7. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurations-Debug-Protokolle**.

Das Ausführungsprotokoll enthält Informationen über die Ergebnisse des Vergleichs der generierten Datei mit der konfigurierten Grundlage. Das Protokoll gibt an, dass die generierte Datei und der Ausgangswert gleich sind, auch wenn das ausgeführte Format die Bindung enthält, mit der ein sich ständig ändernder Datums-und Uhrzeitwert in der ausgehenden Datei eingeben wird.

> [!NOTE]
> Obgleich die ausgehende Datei mit Ausgangswerteinstellungen erstellt wurde, die die Ersetzung der Bindungen des Formats erzwingen, erhalten Sie keine Warnungen zur Ersetzung.

## <a name="exchange-baseline-settings-between-environments"></a>Ausgangswerteinstellungen zwischen Umgebungen austauschen

### <a name="export-baseline-settings"></a>Ausgangswerteinstellungen exportieren

Mit den neuen ER-Funktionen können Sie Ausgangswerteinstellungen für das ausgewählte ER-Format aus der aktuellen Umgebung exportieren und als XML-Dateien speichern. 

Um Ausgangswerteinstellungen zu exportieren,wählen Sie auf der Seite **Formatausgangswerte für elektronische Berichterstellung** **Exportieren** aus.

### <a name="import-baseline-settings"></a>Grundwerte-Einstellungen importieren

Exportierte Ausgangswerteinstellungen können in eine andere Umgebung importiert werden. Die Umgebung muss zuerst als ER-Format importiert werden. Sie können anschließend die Ausgangswerteinstellungen importieren.

Um Ausgangswerteinstellungen aus einer lokal gespeicherten XML-Datei zu importieren, wählen Sie auf der Seite **Formatausgangswerte für elektronische Berichterstellung** **Importieren** und anschließend **Durchsuchen** aus, um die XML-Datei auszuwählen.

![Dialogfeld „Ausgangswerteinstellungen importieren“](media/GER-BaselineSample-ImportBaseline1.PNG "Screenshot des Dialogfelds „Ausgangswerteinstellungen importieren“")

Um Ausgangswerteinstellungen aus einer XML-Datei zu importieren, die auf dem Microsoft SharePoint-Server gespeichert ist, wählen Sie basierend auf den aktuellen Einstellungen der Dokumentverwaltung und dem ausgewählten Dokumenttyp, auf Basis der aktuellen Dokumentverwaltungseinstellungen gespeichert wird und den ausgewählten Dokumenttyp auf der Seite **Formatausgangswerte für elektronische Berichterstellung** **Importieren aus Quelle** aus. Wählen Sie dann den Dokumenttyp und die XML-Datei aus. Der erforderliche Dokumenttyp, um auf den SharePoint-Ordner zuzugreifen, muss zuvor bereits konfiguriert werden.

![Dialogfeld „Importieren aus Quelle“](media/GER-BaselineSample-ImportBaseline2.PNG "Screenshot des Dialogfelds „Importieren aus Quelle“")

> [!NOTE]
> Sie können die Aufgabenaufzeichnung verwenden, um die Schritte zum Auswählen des erforderlichen Dokumenttyps und des Dateinamens im Dialogfeld **Importieren aus Quelle** zu erfassen. Auf diese Weise können Sie erforderliche Ausgangswerteinstellungen auf dem SharePoint-Server behalten und anschließend automatisch importieren, indem Sie eine Aufgabenaufzeichnung wiedergeben, wenn Sie automatisierte Tests ausführen, indem Sie Regression Suite Automation Tool verwenden.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Erstellte Berichtsergebnisse protokollieren und mit Ausgangswerten vergleichen](er-trace-reports-compare-baseline.md)
- [Aufgabenaufzeichnung](../user-interface/task-recorder.md)