---
title: Ein ER-Format zum Paginieren von in Excel generierten Dokumenten entwerfen
description: In diesem Artikel wird erläutert, wie Sie ein elektronisches Berichtsformat entwerfen, das ein in Microsoft Excel generiertes Dokument paginiert.
author: NickSelin
ms.date: 09/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-08-01
ms.dyn365.ops.version: Version 10.0.22
ms.openlocfilehash: e8edc8bba62f74b4f81d423cf75b5fb87c01e43f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909277"
---
# <a name="design-an-er-format-to-paginate-generated-documents-in-excel"></a>Ein ER-Format zum Paginieren von in Excel generierten Dokumenten entwerfen

[!include [banner](../includes/banner.md)]

In diesem Artikel wird erläutert, wie Benutzer mit der Rolle „Systemadministrator“ oder „Funktionaler Berater für elektronische Berichterstellung“ ein Format für die [Elektronische Berichterstellung](general-electronic-reporting.md) zum Generieren ausgehender Dokumente in Microsoft Excel und zum Verwalten der Paginierung von Dokumenten konfigurieren können.

In diesem Beispiel ändern Sie das von Microsoft bereitgestellte ER-Format, das zum Drucken des Kontrollberichts verwendet wird, wenn die Intrastat-Meldung [generiert](../../../finance/localizations/tasks/eur-00002-eu-intrastat-declaration.md) wird. Mit diesem Bericht können Sie gemeldete Intrastat-Transaktionen beobachten. Mit Ihren Änderungen können Sie die Paginierung der generierten Kontrollberichte verwalten.

Die Verfahren in diesem Artikel können im **DEMF**-Unternehmen abgeschlossen werden. Eine Codierung ist nicht erforderlich. Bevor Sie beginnen, laden Sie die folgenden Dateien herunter und speichern Sie sie.

| Beschreibung       | Dateiname |
|-------------------|-----------| 
| Berichtsvorlage 1 | [ERIntrastatReportDemo1.xlsx](https://download.microsoft.com/download/7/2/a/72ae292a-8bb2-4b9d-8397-9764218f6fa8/ERIntrastatReportDemo1%20.xlsx) |
| Berichtsvorlage 2 | [ERIntrastatReportDemo2.xlsx](https://download.microsoft.com/download/7/d/1/7d15858d-6260-4afa-9dda-d8b955e59b1a/ERIntrastatReportDemo2.xlsx) |

## <a name="configure-the-er-framework"></a>Konfigurieren des EB-Frameworks

Befolgen Sie die Schritte in [ER-Framework konfigurieren](er-quick-start2-customize-report.md#ConfigureFramework), um den minimalen Satz von ER-Parametern einzurichten. Sie müssen diese Einrichtung abschließen, bevor Sie mit der Verwendung des ER-Frameworks beginnen, um eine benutzerdefinierte Version eines standardmäßigen ER-Formats zu entwerfen.

## <a name="import-the-standard-er-format-configuration"></a>Die standardmäßige ER-Formatkonfiguration importieren

Befolgen Sie die Schritte in [ER-Standard-Formatkonfiguration importieren](er-quick-start2-customize-report.md#ImportERSolution1), um die ER-Standardkonfigurationen Ihrer aktuellen Instanz von Dynamics 365 Finance hinzuzufügen. Importieren Sie **1.9** der **Intrastat-Berichts**-Formatkonfiguration. Basisversion 1 der **Intrastat-Modell**-Basiskonfiguration wird automatisch aus dem Repository importiert.

## <a name="customize-the-standard-er-format"></a>Anpassen des standardmäßigen EB-Formats

### <a name="create-the-custom-er-format"></a>Das benutzerdefinierte ER-Format erstellen

In diesem Szenario sind Sie der Mitarbeiter von Litware, Inc., das derzeit als aktiver ER-Konfigurationsanbieter ausgewählt ist. Sie müssen eine neue ER-Formatkonfiguration erstellen, indem Sie die Konfiguration des **Intrastat-Berichts** als Basis verwenden.

1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.
2. Erweitern Sie auf der Seite **Konfigurationen** in der Konfigurationsstruktur im linken Bereich den Punkt **Intrastat-Modell**, und wählen Sie **Intrastat-Bericht** aus. Litware, Inc. verwendet Version 1.9 dieser EB-Formatkonfiguration als Basis für die benutzerdefinierte Version.
3. Wählen Sie **Konfiguration erstellen** aus, um das Dropdown-Dialogfeld zu öffnen. Sie können dieses Dialogfeld verwenden, um eine neue Konfiguration für ein benutzerdefiniertes Zahlungsformat zu erstellen.
4. Wählen Sie in der Feldgruppe **Neu** die Option **Von Name ableiten: Intrastat-Bericht, Microsoft** aus.
5. Geben Sie im Feld **Name** den Begriff **Intrastat-Bericht Litware** ein.
6. Wählen Sie **Konfiguration erstellen** aus, um das neue Format zu erstellen.

Version 1.9.1 der EB-Formatkonfiguration **Intrastat-Bericht Litware** wird erstellt. Diese Version hat den [Status](general-electronic-reporting.md#component-versioning) **Entwurf** und kann bearbeitet werden. Der aktuelle Inhalt Ihres benutzerdefinierten EB-Formats entspricht dem Inhalt des von Microsoft bereitgestellten Formats.

### <a name="make-the-custom-format-runnable"></a>Das benutzerdefinierte Format als ausführbar entwickeln

Nachdem die erste Version Ihres benutzerdefinierten Formats mit dem Status **Entwurf** erstellt wurde, können Sie das Format zu Testzwecken ausführen. Um den Bericht auszuführen, verarbeiten Sie eine Kreditorenzahlung mithilfe der Zahlungsmethode, die sich auf Ihr benutzerdefiniertes EB-Format bezieht. Beim Aufrufen eines EB-Formats aus der Anwendung werden standardmäßig nur Versionen mit dem Status **Abgeschlossen** oder **Freigegeben** [berücksichtigt](general-electronic-reporting.md#component-versioning). Dieses Verhalten verhindert, dass EB-Formate mit unfertigen Designs verwendet werden. Für Ihre Testläufe können Sie die Anwendung jedoch zwingen, die Version Ihres EB-Formats mit dem Status **Entwurf** zu verwenden. Auf diese Weise können Sie die aktuelle Formatversion anpassen, falls Änderungen erforderlich sind. Weitere Informationen finden Sie unter [Anwendbarkeit](electronic-reporting-destinations.md#applicability).

Um die Entwurfsversion eines EB-Formats zu verwenden, müssen Sie das EB-Format explizit markieren.

1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.
2. Auf der Seite **Konfigurationen** im Aktivitätsbereich, auf der Registerkarte **Konfigurationen** in der Gruppe **Erweiterte Einstellungen** wählen Sie **Benutzerparameter** aus.
3. Legen Sie im Dialogfeld **Benutzerparameter** die Option **Testlaufeinstellungen** auf **Ja** fest und wählen Sie dann **OK** aus.
4. Wählen Sie **Bearbeiten** aus, um die aktuelle Seite bei Bedarf bearbeiten zu können.
5. Wählen Sie in der Konfigurationsstruktur im linken Bereich **Intrastat-Bericht Litware** aus.
6. Stellen Sie die Option **Entwurf ausführen** auf **Ja**, und wählen Sie dann **Speichern** aus.

    ![Option „Entwurf ausführen“ auf der Konfigurationsseite.](./media/er-paginate-excel-reports-derived-format-configuration.png)

## <a name="set-up-foreign-trade-parameters-to-use-the-custom-er-format"></a>Außenhandelsparameter zur Verwendung des benutzerdefinierten ER-Formats einrichten

Führen Sie diese Schritte aus, um Außenhandelsparameter zu konfigurieren, damit Sie das benutzerdefinierte Format verwenden können.

1. Navigieren Sie zu **Steuer** \> **Einstellungen** \> **Außenhandel** \> **Außenhandelsparameter**.
2. Wählen Sie auf der Seite **Außenhandelsparameter** im Inforegister **Elektronische Berichterstellung** im Feld **Dateiformatzuordnung** die Option **Intrastat-Bericht Litware** aus.
3. Wählen Sie im Feld **Berichtformatzuordnung** die Option **Intrastatbericht Litware** aus.
4. Wählen Sie **Speichern** aus.

## <a name="configure-the-custom-format-to-use-the-downloaded-report-template"></a>Das benutzerdefinierte Format konfigurieren, um die heruntergeladene Berichtsvorlage zu verwenden

### <a name="review-the-first-downloaded-excel-template"></a>Die erste heruntergeladene Excel-Vorlage überprüfen

1. Öffnen Sie in der Excel-Desktopanwendung die Vorlagendatei **ERIntrastatReportDemo1.xlsx**, die Sie zuvor heruntergeladen haben.
2. Stellen Sie sicher, dass die Vorlage benannte Bereiche enthält, um Berichtskopfzeilen, Berichtsdetails und Berichtsfußzeilenabschnitte in generierten Dokumenten zu erstellen.

    ![Layout der Excel-Vorlage 1 in der Desktopanwendung](./media/er-paginate-excel-reports-template1.gif)

### <a name="replace-the-current-excel-template-in-the-custom-er-format"></a><a id="replace-template"></a>Die aktuelle Excel-Vorlage im benutzerdefinierten ER-Format ersetzen

Sie müssen dem benutzerdefinierten ER-Format eine neue Excel-Vorlage hinzufügen.

1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.
2. Erweitern Sie auf der Seite **Konfigurationen** im linken Bereich **Intrastat-Modell** \> **Intrastat-Bericht**, und wählen Sie die Konfiguration **Intrastat-Bericht Litware** aus.
3. Wählen Sie **Designer** aus.
4. Wählen Sie auf der Seite **Formatdesigner** im Aktionsbereich die Option **Details anzeigen** aus.
5. Stellen Sie sicher, dass die **Intrastat: Excel**-Root-Formatkomponente ausgewählt ist. Wählen Sie dann im Aktionsbereich auf der Registerkarte **Importieren** in der Gruppe **Importieren** die Option **Aus Excel aktualisieren** aus.
6. Wählen Sie im Dialogfeld **Aus Excel aktualisieren** die Option **Vorlage aktualisieren** aus.
7. Navigieren Sie im Dialogfeld **Öffnen** zur Datei **ERIntrastatReportDemo1.xlsx**, die Sie zuvor heruntergeladen haben, und wählen Sie sie aus. Wählen Sie anschließend **Öffnen** aus.
8. Wählen Sie **OK** aus.
9. Wählen Sie **Speichern** aus.

![Formatstruktur im ER-Formatdesigner nach dem Hinzufügen der neuen Excel-Vorlage](./media/er-paginate-excel-reports-format1.png)

## <a name="change-the-data-binding-to-show-the-item-description-on-a-generated-report"></a>Die Datenbindung ändern, um die Artikelbeschreibung in einem generierten Bericht anzuzeigen

1. Auf der Seite **Formatdesigner** wählen Sie die Registerkarte **Zuordnung** aus.
2. Erweitern Sie **Intrastat** \> **Berichtszeilen**, und wählen Sie die Komponente **Warencode** aus.
3. Wählen Sie **Formel bearbeiten** aus.
4. Ändern Sie die Bindungsformel von `@.CommodityCode` in `CONCATENATE(@.CommodityCode, " ", @.ProductName)`.
5. Wählen Sie **Speichern** aus.

![Konfigurierte Bindung zum Anzeigen der Artikelbeschreibung im ER-Formatdesigner](./media/er-paginate-excel-reports-format1a.png)

## <a name="generate-an-intrastat-declaration-control-report"></a><a id="generate-intrastat-control-report"></a>Einen Kontrollbericht für eine Intrastat-Meldung generieren

Stellen Sie zunächst sicher, dass Sie über Intrastat-Transaktionen für die Berichterstattung auf der Seite **Intrastat** verfügen.

![Transaktionen auf der Seite „Intrastat“](./media/er-paginate-excel-reports-transactions1.gif)

Verwenden Sie dann das benutzerdefinierte ER-Format, um den Kontrollbericht der Intrastat-Meldung zu generieren.

1. Wechseln Sie zu **Steuer** \> **Meldungen** \> **Außenhandel** \> **Intrastat**.
2. Wählen Sie auf der Seite **Intrastat** im Aktionsbereich **Ausgabe** \> **Bericht** aus.
3. Befolgen Sie im Dialogfeld **Intrastat-Bericht** diese Schritte zum Ausführen des Berichts:

    1. Legen Sie die Felder **Startdatum** und **Enddatum** fest, um bestimmte Intrastat-Transaktionen in den Bericht aufzunehmen.
    2. Legen Sie die Option **Datei generieren** auf **Nein** fest.
    3. Legen Sie die Option **Bericht generieren** auf **Ja** fest.
    4. Wählen Sie **OK** aus.

4. Laden Sie das generierte Dokument herunter und speichern Sie es.
5. Öffnen Sie das Dokument in Excel, und prüfen Sie es.

    ![Generiertes Excel-Dokument in der Desktopanwendung](./media/er-paginate-excel-reports-document1.png)

## <a name="configure-the-custom-format-to-paginate-generated-documents"></a>Das benutzerdefinierte Format konfigurieren, um generierte Dokumente zu paginieren

### <a name="review-the-second-downloaded-excel-template"></a>Die zweite heruntergeladene Excel-Vorlage überprüfen

1. Öffnen Sie in Excel die Vorlagendatei **ERIntrastatReportDemo2.xlsx**, die Sie zuvor heruntergeladen haben.
2. Vergleichen Sie diese Vorlage mit der Vorlage **ERIntrastatReportDemo1.xlsx**, und prüfen Sie, ob sie mehrere neue Excel-Namen enthält, um seitenspezifische Abschnitte in generierten Dokumenten zu erstellen und auszufüllen:

    - Der Bereich **ReportPageHeader** wird hinzugefügt, um Seitenüberschriften zu erstellen.
    - Der Bereich **ReportPageFooter** wird hinzugefügt, um Seitenfußzeilen zu erstellen.
    - Die Zelle **ReportPageFooter\_PageLines** ist so konfiguriert, dass sie die Anzahl der Transaktionen pro Seite anzeigt.
    - Die Zelle **ReportPageFooter\_PageAmount** ist so konfiguriert, dass Sie die Gesamtanzahl der Transaktionen pro Seite anzeigt.
    - Die Zelle **ReportPageFooter\_PageWeight** ist so konfiguriert, dass sie das Gesamtgewicht der Transaktionen pro Seite anzeigt.
    - Die Zelle **ReportPageFooter\_RunningCounterLines** ist so konfiguriert, dass sie den laufenden Zähler für Transaktionen vom Anfang des Berichts bis zur aktuellen Seite anzeigt.
    - Die Zelle **ReportPageFooter\_RunningTotalAmount** ist so konfiguriert, dass sie die laufende Summe für alle Transaktionen vom Anfang des Berichts bis zur aktuellen Seite anzeigt.
    - Die Zelle **ReportPageFooter\_RunningTotalWeight** ist so konfiguriert, dass sie die laufende Summe für das Gewicht für alle Transaktionen vom Anfang des Berichts bis zur aktuellen Seite anzeigt.

    ![Layout der Excel-Vorlage 2 in der Desktopanwendung](./media/er-paginate-excel-reports-template2a.gif)

    Die Zelle **CommodityCode** dieser Vorlage ist für den Zeilenumbruch konfiguriert. Da die Zeile mit Transaktionsdetails so konfiguriert ist, dass sie automatisch der Höhe einer Zeile entspricht, muss sich die Höhe der gesamten Zeile automatisch ändern, wenn für den Text in der Zelle **CommodityCode** ein Zeilenumbruch erfolgt.

    ![CommodityCode-Zelle, die für den Zeilenumbruch konfiguriert ist](./media/er-paginate-excel-reports-template2b.gif)

### <a name="repeat-the-replacement-of-the-current-excel-template-in-the-custom-er-format"></a>Das Ersetzen der aktuellen Excel-Vorlage im benutzerdefinierten ER-Format wiederholen

1. Befolgen Sie die Schritte im Abschnitt [Die aktuelle Excel-Vorlage im benutzerdefinierten EB-Format ersetzen](#replace-template) in diesem Artikel. Wählen Sie jedoch in Schritt 7 die Datei **ERIntrastatReportDemo2.xlsx** aus.
2. Erweitern Sie auf der Seite **Formatdesigner** die Option **Intrastat**.
3. Benennen Sie die [Bereich](er-fillable-excel.md#range-component)-Formatkomponenten, die dem bearbeitbaren ER-Format hinzugefügt wurden, um die Struktur mit der Struktur der angewendeten Excel-Vorlage zu synchronisieren:

    1. Wählen Sie die **Bereich**-Komponente aus, die dem Excel-Namen **ReportPageHeader** zugewiesen ist.
    2. Geben Sie auf der Registerkarte **Format** im Feld **Name** **Kopfzeile der Berichtsseite** ein.
    3. Wählen Sie die **Bereich**-Komponente aus, die dem Excel-Namen **ReportPageFooter** zugewiesen ist.
    4. Geben Sie auf der Registerkarte **Format** im Feld **Name** **Fußzeile der Berichtsseite** ein.

4. Wählen Sie **Speichern** aus.

![Formatstruktur im ER-Formatdesigner nach dem Ersetzen der Excel-Vorlage](./media/er-paginate-excel-reports-format2.png)

### <a name="change-the-format-structure-to-implement-document-pagination"></a>Die Formatstruktur ändern, um die Dokument-Paginierung zu implementieren

1. Wählen Sie auf der Seite **Formatdesigner** in der Formatstruktur im linken Bereich die Root-Komponente **Intrastat** aus.
2. Wählen Sie **Hinzufügen** aus.
3. Wählen Sie im Dialogfeld **Hinzufügen** die [Seite](er-fillable-excel.md#page-component)-Komponente in der **Excel**-Gruppe der Komponenten aus.
4. Geben Sie im Dialogfeld **Komponenteneigenschaften** im Feld **Name** **Berichtsseite** ein. Wählen Sie dann **OK** aus.
5. Um die Komponente **Kopfzeile der Berichtsseite** als Kopfzeile der Seite auf jeder generierten Seite zu verwenden, gehen Sie wie folgt vor:

    1. Wählen Sie die Komponente **Kopfzeile der Berichtsseite** und dann **Ausschneiden** aus.
    2. Wählen Sie die Komponente **Berichtsseite** und dann **Einfügen** aus.
    3. Erweitern Sie **Berichtsseite**.
    4. Um zu erzwingen, dass die **Seite**-Komponente diesen Bereich als Kopfzeile der Seite [berücksichtigt](er-fillable-excel.md#page-component-structure), wählen Sie **Kopfzeile der Berichtsseite** und dann auf der Registerkarte **Format** im Feld **Replikationsrichtung** die Option **Keine Replikation** aus.

6. Gehen Sie folgendermaßen vor, um ein generiertes Dokument zu paginieren, damit der Inhalt der Berichtszeilen berücksichtigt wird:

    1. Wählen Sie die Komponente **Berichtszeilen** und dann **Ausschneiden** aus.
    2. Wählen Sie die Komponente **Berichtsseite** und dann **Einfügen** aus.

7. Gehen Sie folgendermaßen vor, um die Berichtsfußzeile nach Berichtszeilen, aber vor der letzten Seitenfußzeile einzuschließen:

    1. Wählen Sie die Komponente **Berichtsfußzeile** und dann **Ausschneiden** aus.
    2. Wählen Sie die Komponente **Berichtsseite** und dann **Einfügen** aus.

8. Um die Komponente **Fußzeile der Berichtsseite** als Fußzeile der Seite auf jeder generierten Seite zu verwenden, gehen Sie wie folgt vor:

    1. Wählen Sie die Komponente **Fußzeile der Berichtsseite** und dann **Ausschneiden** aus.
    2. Wählen Sie die Komponente **Berichtsseite** und dann **Einfügen** aus.
    3. Um zu erzwingen, dass die **Seite**-Komponente diesen Bereich als Fußzeile der Seite [berücksichtigt](er-fillable-excel.md#page-component-structure), wählen Sie **Fußzeile der Berichtsseite** und dann auf der Registerkarte **Format** im Feld **Replikationsrichtung** die Option **Keine Replikation** aus.

![Formatstruktur im ER-Formatdesigner nach dem Implementieren der Dokumentpaginierung](./media/er-paginate-excel-reports-format3.png)

### <a name="add-data-sources-to-calculate-page-footer-totals"></a>Datenquellen hinzufügen, um die Gesamtmenge der Seitenfußzahlen zu berechnen

Sie müssen neue Datenquellen konfigurieren, um die Gesamtanzahl der Seiten, den laufenden Zähler und die laufenden Gesamtwerte zu berechnen und im Bereich der Seitenfußzeile anzuzeigen. Wir empfehlen Ihnen, die Datenquellen [Datensammlung](er-data-collection-data-sources.md) für diesen Zweck zu verwenden.

1. Auf der Seite **Formatdesigner** wählen Sie die Registerkarte **Zuordnung** aus.
2. Wählen Sie **Root hinzufügen** aus , und führen Sie die folgenden Schritte aus:

    1. Wählen Sie im Dialogfeld **Datenquelle hinzufügen** im Abschnitt **Allgemein** die Option **Leerer Container** aus.
    2. Geben Sie im Dialogfeld **Datenquelleneigenschaften „Leerer Container“** im Feld **Name** **Gesamt** ein.
    3. Wählen Sie **OK** aus.

3. Wählen Sie die Datenquelle **Gesamt** und dann **Hinzufügen** aus, und führen Sie dann diese Schritte aus:

    1. Wählen Sie im Dialogfeld **Datenquelle hinzufügen** im Abschnitt **Allgemein** die Option **Leerer Container** aus.
    2. Geben Sie im Dialogfeld **Datenquelleneigenschaften „Leerer Container“** im Feld **Name** **Seite** ein.
    3. Wählen Sie **OK** aus.

4. Wählen Sie erneut **Hinzufügen** aus und führen Sie die folgenden Schritte aus:

    1. Wählen Sie im Dialogfeld **Datenquelle hinzufügen** im Abschnitt **Allgemein** die Option **Leerer Container** aus.
    2. Geben Sie im Dialogfeld **Datenquelleneigenschaften „Leerer Container“** im Feld **Name** **Wird ausgeführt** ein.
    3. Wählen Sie **OK** aus.

5. Wählen Sie die Datenquelle **Total.Page** und dann **Hinzufügen** aus, und führen Sie dann diese Schritte aus:

    1. Wählen Sie im Dialogfeld **Datenquelle hinzufügen** im Abschnitt **Funktionen** die Option **Datensammlung** aus.
    2. Geben Sie im Dialogfeld **Datenquelleneigenschaften „Datensammlung“** im Feld **Name** **Betrag** ein.
    3. Wählen Sie im Feld **Artikeltyp** **Gleitkommazahl** aus.
    4. Legen Sie die Option **Alle Werte erfassen** auf **Ja** fest.
    5. Wählen Sie **OK** aus.

6. Wählen Sie erneut **Hinzufügen** aus und führen Sie die folgenden Schritte aus:

    1. Wählen Sie im Dialogfeld **Datenquelle hinzufügen** im Abschnitt **Funktionen** die Option **Datensammlung** aus.
    2. Geben Sie im Dialogfeld **Datenquelleneigenschaften „Datensammlung“** im Feld **Name** **Gewicht** ein.
    3. Wählen Sie im Feld **Artikeltyp** **Gleitkommazahl** aus.
    4. Legen Sie die Option **Alle Werte erfassen** auf **Ja** fest.
    5. Wählen Sie **OK** aus.

7. Wählen Sie die Datenquelle **Total.Running** und dann **Hinzufügen** aus, und führen Sie dann diese Schritte aus:

    1. Wählen Sie im Dialogfeld **Datenquelle hinzufügen** im Abschnitt **Funktionen** die Option **Datensammlung** aus.
    2. Geben Sie im Dialogfeld **Datenquelleneigenschaften „Datensammlung“** im Feld **Name** **Betrag** ein.
    3. Wählen Sie im Feld **Artikeltyp** **Gleitkommazahl** aus.
    4. Legen Sie das Feld **Alle Werte erfassen** auf **Ja** fest.
    5. Wählen Sie **OK** aus.

8. Wählen Sie erneut **Hinzufügen** aus und führen Sie die folgenden Schritte aus:

    1. Wählen Sie im Dialogfeld **Datenquelle hinzufügen** im Abschnitt **Funktionen** die Option **Datensammlung** aus.
    2. Geben Sie im Dialogfeld **Datenquelleneigenschaften „Datensammlung“** im Feld **Name** **Gewicht** ein.
    3. Wählen Sie im Feld **Artikeltyp** **Gleitkommazahl** aus.
    4. Legen Sie das Feld **Alle Werte erfassen** auf **Ja** fest.
    5. Wählen Sie **OK** aus.

9. Wählen Sie erneut **Hinzufügen** aus und führen Sie die folgenden Schritte aus:

    1. Wählen Sie im Dialogfeld **Datenquelle hinzufügen** im Abschnitt **Funktionen** die Option **Datensammlung** aus.
    2. Geben Sie im Dialogfeld **Datenquelleneigenschaften „Datensammlung“** im Feld **Name** **Zeilen** ein.
    3. Wählen Sie im Feld **Artikeltyp** die Option **Integer** aus.
    4. Legen Sie das Feld **Alle Werte erfassen** auf **Ja** fest.
    5. Wählen Sie **OK** aus.

10. Wählen Sie **Speichern** aus.

### <a name="add-data-sources-to-control-page-footer-visibility"></a>Datenquellen zur Steuerung der Sichtbarkeit der Seitenfußzeilen hinzufügen

Wenn Sie die Sichtbarkeit der Seitenfußzeile steuern möchten und die Fußzeile nicht auf der letzten Seite einfügen möchten, wenn sie Transaktionen enthält, konfigurieren Sie eine neue Datenquelle, um den erforderlichen laufenden Zähler zu berechnen.

1. Auf der Seite **Formatdesigner** wählen Sie die Registerkarte **Zuordnung** aus.
2. Wählen Sie die Datenquelle **Total.Running** und dann **Hinzufügen** aus.
3. Wählen Sie im Dialogfeld **Datenquelle hinzufügen** im Abschnitt **Funktionen** die Option **Datensammlung** aus.
4. Geben Sie im Dialogfeld **Datenquelleneigenschaften „Datensammlung“** im Feld **Name** **Zeilen2** ein.
5. Wählen Sie im Feld **Artikeltyp** die Option **Integer** aus.
6. Legen Sie die Option **Alle Werte erfassen** auf **Ja** fest.
7. Wählen Sie **OK** aus.
8. Wählen Sie **Speichern** aus.

![Datenquellen im ER-Formatdesigner hinzugefügt](./media/er-paginate-excel-reports-format4.png)

### <a name="configure-bindings-to-collect-total-values"></a>Bindungen zum Erfassen von Gesamtwerten konfigurieren

1. Erweitern Sie auf der Seite **Formatdesigner** in der Formatstruktur die Komponente **Berichtszeilen**, und wählen Sie die verschachtelte Komponente **Rechnungswert** aus.
2. Wählen Sie **Formel bearbeiten** aus.
3. Ändern Sie die Bindungsformel von `NUMBERVALUE(NUMBERFORMAT(@.InvoiceValue, "F"&TEXT(model.Parameters.IntrastatAmountDecimals)), ".", "")` in `Total.Page.Amount.Collect(NUMBERVALUE(NUMBERFORMAT(@.InvoiceValue, "F"&TEXT(model.Parameters.IntrastatAmountDecimals)), ".", ""))`.

    > [!NOTE]
    > Zusätzlich zum Einfügen des Betragswerts in eine Excel-Zelle für jede iterierte Transaktion sammelt diese Bindung den Wert in der Datensammlung **Total.Page.Amount**.

4. Wählen Sie das verschachtelte Komponente **Gewicht** aus.
5. Wählen Sie **Formel bearbeiten** aus.
6. Ändern Sie die Bindungsformel von `@.'$RoundedWeight'` in `Total.Page.Weight.Collect(@.'$RoundedWeight')`.

    > [!NOTE]
    > Zusätzlich zum Einfügen des Gewichtswerts in eine Excel-Zelle für jede iterierte Transaktion sammelt diese Bindung den Wert in der Datensammlung **Total.Page.Weight**.

![Konfigurierte Bindungen zum Erfassen von Gesamtwerten im ER-Formatdesigner](./media/er-paginate-excel-reports-format5.png)

### <a name="configure-bindings-to-fill-in-page-footer-totals"></a>Bindungen zum Ausfüllen der Seiten-Fußzeilennummern

1. Erweitern Sie auf der Seite **Formatdesigner** in der Formatstruktur die Komponente **Fußzeile der Berichtsseite**, wählen Sie die verschachtelte Komponente **Bereich** aus, die sich auf die Excel-Zeile **ReportPageFooter\_PageAmount** bezieht, und führen Sie dann die folgenden Schritte aus:

    1. Wählen Sie in der Datenquellenstruktur im rechten Bereich das Element **Total.Page.Amount.Sum()** aus.
    2. Wählen Sie **Bindung** aus.
    3. Wählen Sie **Formel bearbeiten** aus.
    4. Aktualisieren Sie die Formel in `Total.Page.Amount.Sum(false)`.

    > [!NOTE]
    > Sie müssen das Argument dieser Funktion als **False** angeben, um die gesammelten Daten für die aktuelle Seite zu behalten, da diese Daten erforderlich sind, um die laufende Summe, die Gesamtzahl der Zeilen pro Seite und den laufenden Zähler der Zeilen zu berechnen.

2. Wählen Sie in der Formatstruktur der verschachtelten **Bereich**-Komponente aus, die sich auf die Excel-Zeile **ReportPageFooter\_PageWeight** bezieht, und führen Sie dann die folgenden Schritte aus:

    1. Wählen Sie in der Datenquellenstruktur im rechten Bereich das Element **Total.Page.Weight.Sum()** aus.
    2. Wählen Sie **Bindung** aus.
    3. Wählen Sie **Formel bearbeiten** aus.
    4. Aktualisieren Sie die Formel in `Total.Page.Weight.Sum(false)`.

### <a name="configure-bindings-to-fill-in-page-running-totals"></a>Bindungen zum Ausfüllen der Gesamtanzahl der Seitenausführungen

1. Erweitern Sie auf der Seite **Formatdesigner** in der Formatstruktur die Komponente **Fußzeile der Berichtsseite**, wählen Sie die verschachtelte Komponente **Bereich** aus, die sich auf die Excel-Zeile **ReportPageFooter\_RunningTotalAmount** bezieht, und führen Sie dann die folgenden Schritte aus:

    1. Wählen Sie in der Datenquellenstruktur im rechten Bereich das Element **Total.Running.Amount.Collect()** aus.
    2. Wählen Sie **Bindung** aus.
    3. Wählen Sie **Formel bearbeiten** aus.
    4. Aktualisieren Sie die Formel in `Total.Running.Amount.Sum(false)+Total.Running.Amount.Collect(Total.Page.Amount.Sum(true))`.

    > [!NOTE]
    > Der Operand `Total.Running.Amount.Sum(false)` gibt die zuvor erfasste Gesamtanzahl der Ausführungen zurück. Der Operand `Total.Running.Amount.Collect(Total.Page.Amount.Sum(true))` gibt die Gesamtanzahl der aktuellen Seite zurück. Sie müssen das Argument der verschachtelten Funktion des zweiten Operanden als **True** angeben, um die Datensammlung `Total.Page.Amount` zurückzusetzen, sobald dieser Wert in die laufende Gesamtsammlung `Total.Running.Amount` eingegeben wird. Das angegebene Argument muss mit der Erfassung der nächsten Seitensumme ab einem Wert von 0 (Null) beginnen.
    >
    > Die Funktion `Total.Running.Amount.Sum(false)` wird aufgerufen, um die laufende Summe des Betrags in der Excel-Zelle **ReportPageFooter\_ RunningTotalAmount** auf der aktuellen Seite einzugeben.

2. Wählen Sie in der Formatstruktur der verschachtelten **Bereich**-Komponente aus, die sich auf die Excel-Zeile **ReportPageFooter\_RunningTotalWeight** bezieht, und führen Sie dann die folgenden Schritte aus:

    1. Wählen Sie in der Datenquellenstruktur im rechten Bereich das Element **Total.Running.Weight.Collect()** aus.
    2. Wählen Sie **Bindung** aus.
    3. Wählen Sie **Formel bearbeiten** aus.
    4. Aktualisieren Sie die Formel in `Total.Running.Weight.Sum(false)+Total.Running.Weight.Collect(Total.Page.Weight.Sum(true))`.

### <a name="configure-bindings-to-fill-in-the-page-running-counter"></a>Bindungen zum Ausfüllen des Zählers der Seitenausführungen konfigurieren

1. Erweitern Sie auf der Seite **Formatdesigner** in der Formatstruktur die Komponente **Fußzeile der Berichtsseite**, wählen Sie die verschachtelte Komponente **Bereich** aus, die sich auf die Excel-Zeile **ReportPageFooter\_RunningCounterLines** bezieht, und führen Sie dann die folgenden Schritte aus:
2. Wählen Sie **Formel bearbeiten** aus.
3. Fügen Sie die Formel `Total.Running.Lines.Collect(COUNT(Total.Page.Amount.Result))` hinzu.

    > [!NOTE]
    > Diese Formel gibt die Anzahl der gesammelten Betragswerte für den gesamten Bericht zurück. Diese Zahl entspricht der Anzahl der Transaktionen, die im aktuellen Moment iteriert wurden. Gleichzeitig sammelt die Formel den zurückgegebenen Wert in der Sammlung **Total.Running.Lines**.

### <a name="configure-bindings-to-fill-in-the-page-footer-counter"></a>Bindungen zum Ausfüllen des Zählers der Seitenfußzeilen konfigurieren

1. Erweitern Sie auf der Seite **Formatdesigner** in der Formatstruktur die Komponente **Fußzeile der Berichtsseite**, wählen Sie die verschachtelte Komponente **Bereich** aus, die sich auf die Excel-Zeile **ReportPageFooter\_PageLines** bezieht, und führen Sie dann die folgenden Schritte aus:
2. Wählen Sie **Formel bearbeiten** aus.
3. Fügen Sie die Formel `COUNT(Total.Page.Amount.Result)-Total.Running.Lines.Sum(false)` hinzu.

    > [!NOTE]
    > Diese Formel berechnet die Anzahl der Transaktionen auf der aktuellen Seite als Differenz zwischen der Anzahl der gesammelten Transaktionen, die in **Total.Page.Amount.Result** für den gesamten Bericht und die Anzahl der zu diesem Zeitpunkt gespeicherten Transaktionen in **Total.Running.Lines.Sum** gespeichert wurden. Da die Anzahl der Transaktionen für die aktuelle Seite in **Total.Running.Lines** in der Bindung der **Bereich**-Komponente gespeichert ist, die sich auf die Excel-Zelle **ReportPageFooter\_ RunningCounterLines** bezieht, ist die Anzahl der Transaktionen auf der aktuellen Seite noch nicht enthalten. Daher entspricht dieser Unterschied der Anzahl der Transaktionen auf der aktuellen Seite.

![Konfigurierte Bindungen zum Ausfüllen des Seitenfußzählers im ER-Formatdesigner](./media/er-paginate-excel-reports-format6.png)

### <a name="configure-component-visibility"></a>Sichtbarkeit der Komponente konfigurieren

Sie können die Sichtbarkeit der Kopf- und Fußzeile der Seite auf einer bestimmten Seite eines generierten Dokuments ändern, um die folgenden Elemente auszublenden:

- Die Seitenkopfzeile auf der ersten Seite, da die Kopfzeile des Berichts bereits Spaltentitel enthält
- Die Seitenkopfzeile auf jeder Seite, die keine Transaktionen enthält, die für die letzte Seite auftreten können
- Die Seitenfußzeile auf jeder Seite, die keine Transaktionen enthält, die für die letzte Seite auftreten können

Um die Sichtbarkeit zu ändern, aktualisieren Sie die Eigenschaft **Aktiviert** der Komponenten **Kopfzeile der Berichtsseite** und **Fußzeile der Berichtsseite**.

1. Erweitern Sie auf der Seite **Formatdesigner** in der Formatstruktur die Komponente **Berichtsseite**, wählen Sie die verschachtelte Komponente **Kopfzeile der Berichtsseile** aus, und führen Sie diese folgenden Schritte aus:

    1. Wählen Sie **Bearbeiten** für das Feld **Aktiviert** aus.
    2. Geben Sie auf der Seite **Formeldesigner** im Feld **Formel** den folgenden Ausdruck ein:

        `AND(`<br>
        `COUNT(Total.Page.Amount.Result)<>0,`<br>
        `COUNT(Total.Page.Amount.Result)<>COUNT(model.CommodityRecord)`<br>
        `)`

2. Wählen Sie in der Formatstruktur die verschachtelte Komponente **Fußzeile der Berichtsseite** aus, und führen Sie dann die folgenden Schritte aus:

    1. Wählen Sie **Bearbeiten** für das Feld **Aktiviert** aus.
    2. Geben Sie auf der Seite **Formeldesigner** im Feld **Formel** den folgenden Ausdruck ein:

        `(`<br>
        `COUNT(Total.Page.Amount.Result)-Total.Running.Lines2.Sum(false)+`<br>
        `0*Total.Running.Lines2.Collect(COUNT(Total.Page.Amount.Result))`<br>
        `)<>0`

    > [!NOTE]
    > Die Konstruktion `COUNT(Total.Page.Amount.Result)-Total.Running.Lines2.Sum(false)` wird verwendet, um die Anzahl der Transaktionen auf der aktuellen Seite zu berechnen. Die Konstruktion `0*Total.Running.Lines2.Collect(COUNT(Total.Page.Amount.Result)` wird verwendet, um die Anzahl der Transaktionen auf der aktuellen Seiten der Sammlung hinzuzufügen, um die Sichtbarkeit der nächsten Seitenfußzeile korrekt zu handhaben.
    >
    > Die Sammlung `Total.Running.Lines` kann hier nicht erneut verwendet werden, da die Eigenschaft **Aktiviert** einer Basiskomponente verarbeitet wird, **nachdem** die Bindungen der verschachtelten Komponenten verarbeitet wurden. Wenn die Eigenschaft **Aktiviert** verarbeitet wird, wird die Sammlung `Total.Running.Lines` bereits durch die Anzahl der Transaktionen auf der aktuellen Seite erhöht.

3. Wählen Sie **Speichern** aus.

## <a name="generate-an-intrastat-declaration-control-report-updated"></a>Einen Kontrollbericht für eine Intrastat-Meldung generieren (aktualisiert)

1. Stellen Sie sicher, dass Sie über 24 Transaktionen auf der Seite **Intrastat** verfügen. Wiederholen Sie die Schritte im Abschnitt [Einen Kontrollbericht für eine Intrastat-Meldung generieren](#generate-intrastat-control-report) in diesem Artikel, um den Kontrollbericht zu generieren und zu prüfen.

    Alle Transaktionen werden auf der ersten Seite dargestellt. Die Seitensummen und Zähler entsprechen den Berichtssummen und Zählern. Der Bereich der Seitenkopfzeile ist auf der ersten Seite ausgeblendet, da die Kopfzeile des Berichts bereits Spaltentitel enthält. Die Kopf- und Fußzeile der Seite werden auf der zweiten Seite ausgeblendet, da diese Seite keine Transaktionen enthält.

    ![Generiertes Excel-Dokument in der Desktopanwendung](./media/er-paginate-excel-reports-document2.gif)

2. Aktualisieren Sie die zwei Transaktionen auf der Seite **Intrastat**, indem Sie den Code **Artikelnummer** von **D00006** in **L0010** ändern. Beachten Sie, dass der Produktname des neuen Artikels **Aktives Stereo-Lautsprecherpaar** länger als der Produktname des Originalartikels **Standardlautsprecher** ist. Diese Situation erzwingt den Textumbruch in der entsprechenden Zelle des generierten Dokuments. Die Dokumenten-Paginierung und das seitenbezogene Summieren und Zählen müssen nun aktualisiert werden. Wiederholen Sie die Schritte im Abschnitt [Einen Kontrollbericht für eine Intrastat-Meldung generieren](#generate-intrastat-control-report), um den Kontrollbericht zu generieren und zu prüfen.

    Derzeit werden Transaktionen auf zwei Seiten dargestellt und Seitensummen und Zähler werden korrekt berechnet. Der Bereich der Seitenkopfzeile wird auf der ersten Seite korrekt ausgeblendet und ist auf der zweiten Seite sichtbar. Die Seitenfußzeile ist auf beiden Seiten sichtbar, da sie Transaktionen enthalten.

    ![Aktualisiertes generiertes Excel-Dokument in der Desktopanwendung](./media/er-paginate-excel-reports-document3.gif)

## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen

### <a name="is-there-any-way-to-recognize-when-the-final-page-is-processed-by-the-page-format-component"></a>Gibt es eine Möglichkeit zu erkennen, wann die letzte Seite von der Seitenformatkomponente verarbeitet wird?

Die **Seite**-Komponente [legt keine Informationen](er-fillable-excel.md#page-component-limitations) zur Anzahl der verarbeiteten Seite und der Gesamtanzahl der Seiten in einem generierten Dokument offen. Trotzdem können Sie ER-[Formeln](er-formula-language.md) konfigurieren, um die letzte Seite zu erkennen. Hier ist ein Beispiel:

- Berechnen Sie die Gesamtzahl der Transaktionen, die bereits verarbeitet wurden, indem Sie die Komponente **Berichtsseite** verwenden. Sie können diese Berechnung durch Verwendung der Formel `COUNT(Total.Page.Amount.Result)` durchführen. 
- Berechnen Sie die Gesamtzahl der Transaktionen, die basierend auf der Bindung `model.CommodityRecord` verarbeitet werden müssen, die für die Komponente **Berichtszeilen** konfiguriert ist. Sie können diese Berechnung durch Verwendung der Formel `COUNT(model.CommodityRecord)` durchführen.
- Vergleichen Sie zwei Zahlen, um die letzte Seite zu erkennen. Wenn beide Werte gleich sind, wird die letzte Seite generiert.

> [!NOTE]
> Wir empfehlen, diesen Ansatz nur zu verwenden, wenn die Eigenschaft **Aktiviert** der Komponente **Berichtszeilen** keine Formel enthält, die [False](er-formula-supported-data-types-primitive.md#boolean) zur Laufzeit für einige der iterierten [Aufzeichnungen](er-formula-supported-data-types-composite.md#record) der gebundenen [Aufnahmeliste](er-formula-supported-data-types-composite.md#record-list) zurückgeben könnte.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Eine Konfiguration zur Generierung von Dokumenten im Excel-Format entwerfen](er-fillable-excel.md)
- [Verwendung von DATA COLLECTION Datenquellen in elektronischen Berichtsformaten](er-data-collection-data-sources.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
