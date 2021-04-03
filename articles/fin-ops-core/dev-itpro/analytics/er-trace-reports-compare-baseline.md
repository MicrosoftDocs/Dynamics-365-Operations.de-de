---
title: Erstellte Berichtsergebnisse protokollieren und mit Ausgangswerten vergleichen
description: Dieses Thema erklärt, wie Sie die Ergebnisse von generierten Berichten für elektronische Berichterstellung (ER) mit Basisberichtswerten vergleichen können.
author: NickSelin
manager: AnnBe
ms.date: 06/17/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 3141e285f694f8778c7ac886d3f7e289fd76c648
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568924"
---
# <a name="trace-generated-report-results-and-compare-them-with-baseline-values"></a>Erstellte Berichtsergebnisse protokollieren und mit Ausgangswerten vergleichen

[!include[banner](../includes/banner.md)]

Sie können die Ergebnisse von Formaten für die elektronische Berichterstellung (ER) protokollieren, die ausgehende elektronische Dokumente erstellen. Wenn die Protokollgenerierung eingeschaltet ist (mittels des ER-Benutzerparameters **Im Debugmodus ausführen**), wird bei jeder Ausführung eines ER-Reports ein neuer Protokolldatenatz im Ausführungsprotokoll des ER-Formats erzeugt. In jeder erzeugten Protokollierung werden die folgenden Details gespeichert:

- Alle Warnungen, die von Validierungsregeln generiert wurden
- Alle Fehler, die durch Validierungsregeln generiert wurden
- Alle erzeugten Dateien, die als Anlagen des Protokolldatensatzes gespeichert sind.

Sie können einzelne Basisanwendungsdateien für jedes ER-Format speichern. Dateien gelten als Basisdateien, wenn sie die erwarteten Ergebnisse von Berichten beschreiben, die ausgeführt werden. Wenn eine Basisdatei für ein ER-Format verfügbar ist, das bei eingeschalteter Protokollgenerierung ausgeführt wird, speichert die Protokollierung zusätzlich zu den bereits erwähnten Details das Ergebnis des Vergleichs des erzeugten elektronischen Dokuments mit der Basisdatei. Mit einem Klick erhalten Sie auch das generierte elektronische Dokument und seine Basisdatei in einer einzigen Zip-Datei. Sie können dann einen detaillierten Vergleich durchführen, indem Sie ein externes Tool wie WinDiff verwenden.

Sie können die Protokollierung auswerten, um zu analysieren, ob die erzeugten elektronischen Dokumente den erwarteten Inhalt enthalten. Sie können diese Auswertung in einer UAT-Umgebung (User Acceptance Testing) durchführen, wenn die Codebasis geändert wurde (z. B. wenn Sie auf eine neue Instanz der Anwendung migriert, Hotfixpakete installiert oder Code-Änderungen implementiert haben). Auf diese Weise können Sie sicherstellen, dass die Auswertung keine Auswirkungen auf die Ausführung der verwendeten ER-Berichte hat. Bei vielen ER-Berichten kann die Auswertung im unbeaufsichtigten Modus erfolgen.

Um mehr über diese Funktion zu erfahren, spielen Sie die Aufgabenleitfäden **ER Berichte erstellen und Ergebnisse vergleichen (Teil 1)** und **ER Berichte erstellen und Ergebnisse vergleichen (Teil 2)** ab, die Teil des **7.5.4.3 Test IT-Services/Lösungen (10679)** Geschäftsprozess sind und im [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684) heruntergeladen werden können. Diese Aufgabenleitfäden führen Sie durch den Prozess der Konfiguration des ER-Frameworks zur Verwendung von Basisdateien für die Auswertung generierter elektronischer Dokumente.

## <a name="example-trace-generated-report-results-and-compare-them-with-baseline-values"></a>Beispiel: Nachverfolgung erstellter Berichtsergebnisse und Vergleich mit Ausgangswerten

Dieses Verfahren erklärt, wie das ER-Framework konfiguriert wird, um Informationen zu ER-Formatausführungen zu sammeln und die Ergebnisse dieser Durchläufe dann auszuwerten. Als Teil dieser Bewertung werden generierte Dokumente mit ihren Basisdateien verglichen. In diesem Beispiel erstellen Sie die erforderlichen ER-Konfigurationen für das Beispielunternehmen Litware, Inc. Diese Prozedur ist für Benutzer bestimmt, die die Rolle des Systemadministrators oder des elektronischen Berichtsentwicklers haben, die ihnen zugewiesen sind. Die Schritte können abgeschlossen werden, indem Sie einen beliebigen Dataset verwenden.

Um die Schritte in diesem Beispiel abzuschließen, müssen Sie zunächst die Schritte unter [Konfigurationsanbieter anlegen ausführen und als aktiv markieren](tasks/er-configuration-provider-mark-it-active-2016-11.md).

1. Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.
2. Überprüfen Sie auf der Seite **Lokalisierungskonfigurationen** im Abschnitt **Konfigurationsanbieter**, ob der Konfigurationsanbieter für das Litware, Inc.-Beispielunternehmen aufgeführt ist und als **Aktiv** markiert ist. Wenn Sie diesen Konfigurationsanbieter nicht sehen, führen Sie die Schritte unter [Konfigurationsanbieter erstellen aus und markieren Sie ihn als aktiv](tasks/er-configuration-provider-mark-it-active-2016-11.md).

### <a name="configure-document-management-parameters"></a>Parameter der Dokumentverwaltung konfigurieren

1. Wechseln Sie zu **Organisationsverwaltung** \> **Dokumentverwaltung** \> **Dokumenttypen**, und erstellen Sie einen neuen Dokumenttyp, um Basisdateien zu speichern.
2. Geben Sie im Feld **Klasse** die Option **Datei zuordnen** an.
3. Geben Sie im Feld **Gruppe** die Option **Datei** an.

![Seite „Dokumenttypen”](media/GER-BaselineSample-SetupDocumentType.PNG "Screenshot der Seite Dokumenttypen")

> [!NOTE]
> Einen neuer Dokumenttyp mit dem gleichen Namen muss für jeden Datensatz konfiguriert werden, in dem Sie die ER-Basisfunktion verwenden möchten.

### <a name="configure-er-parameters-to-start-to-use-the-baseline-feature"></a>Konfigurieren Sie die ER-Parameter, um mit der Verwendung der Basisfunktion zu beginnen

1. Wählen Sie im Arbeitsbereich **Elektronische Berichterstellung** im Abschnitt **Zugehörige Links** **Elektronische Berichterstellungsparameter** aus.

    ![Elektronische Berichterstellung – Arbeitsbereich](media/GER-BaselineSample-ERWorkspace.PNG "Screenshot des Arbeitsbereichs Elektronische Berichterstattung")

2. Auf der Registerkarte **Anhänge** im Feld **Berechnungsgrundlage** wählen Sie den Dokumenttyp aus, den Sie soeben erstellt haben.

    ![Registerkarte Anhänge auf der Seite Elektronische Berichtsparameter](media/GER-BaselineSample-ERParameters.PNG "Screenshot der elektronischen Berichtsparameter")

3. Wählen Sie **Speichern** aus und schließen Sie dann die Seite **Elektronische Berichterstellungsparameter**.

### <a name="add-a-new-er-model-configuration"></a>Neue ER-Modellkonfiguration hinzufügen

1. Im Arbeitsbereich **Elektronische Berichterstellung** im Abschnitt **Konfigurationen** wählen Sie die Kachel **Berichterstellungskonfigurationen** aus.
2. Wählen Sie im Aktivitätsbereich **Konfiguration erstellen** aus.
3. Geben Sie im Drop-Down-Dialogfeld im Feld **Name** **Modell zum Erlernen von ER-Grundlagen** ein.
4. Wählen Sie **Konfiguration erstellen** aus, um die Erstellung eines neuen ER-Datenmodelleintrags zu bestätigen.

![Konfigurations-Dropdown-Dialogfeld erstellen](media/GER-BaselineSample-ModelAdd.PNG "Screenshot des Dropdown-Dialogfensters Konfiguration erstellen")

### <a name="design-a-data-model"></a>Entwerfen eines Datenmodells

1. Wählen Sie auf der Seite **Konfigurationen** im Aktivitätsbereich **Designer** aus.
2. Wählen Sie **Neu** aus.
3. Geben Sie im Drop-Down-Dialogfeld im Feld **Name** **Stamm** ein.
4. Wählen Sie **Hinzufügen** aus.
5. Wählen Sie **Stammreferenz** aus.
6. Wählen Sie **OK** und dann **Speichern** aus.
7. Schließen Sie die Seite **Modelldesigner**.
8. Wählen Sie **Status ändern** aus.
9. Wählen Sie **Abschließen** und dann **OK** aus.

![Konfigurationsseite](media/GER-BaselineSample-ModelComplete.PNG "Screenshot der Seite Konfigurationen")

### <a name="add-a-new-er-format-configuration"></a>Neues ER-Modellformat hinzufügen

1. Wählen Sie auf der Seite **Konfigurationen** im Aktivitätsbereich **Konfiguration ersellen** aus.
2. Im Drop-Down-Dialogfeld in der Feldgruppe **Neu**, wählen Sie die Option **Format basierend auf Datenmodell 'Modell zum Erlernen von ER-Grundlagen'** aus.
3. Wählen Sie im Feld **Name** den Text **Format zum Erlernen der ER-Grundlagen** ein.
4. Wählen Sie **Konfiguration erstellen** aus, um die Erstellung eines neuen ER-Formateintrags zu bestätigen.

![Konfigurations-Dropdown-Dialogfeld erstellen](media/GER-BaselineSample-FormatAdd.PNG "Screenshot des Dropdown-Dialogfensters Konfiguration erstellen")

### <a name="design-a-format"></a>Entwerfen eines Formats

Bei diesem Beispiel erstellen Sie ein einfaches ER-Format, um XML-Dokumente zu generieren.

1. Wählen Sie auf der Seite **Konfigurationen** im Aktivitätsbereich **Designer** aus.
2. Wählen Sie **Stamm hinzufügen** aus.
2. Führen Sie im Drop-Down-Dialogfeld die folgenden Schritte aus:

    1. Wählen Sie in der Struktur **Allgemein\\Datei** aus.
    2. Geben Sie im Feld **Name** die Bezeichnung **Ausgabe** ein.
    3. Wählen Sie **OK**.

3. Wählen Sie **Hinzufügen** aus.
4. Führen Sie im Drop-Down-Dialogfeld die folgenden Schritte aus:

    1. Wählen Sie in der Struktur **XML\\Element**.
    2. Geben Sie im Feld **Name** die Bezeichnung **Dokument** ein.
    3. Wählen Sie **OK**.

5. Wählen Sie in der Struktur **Ausgabe\\Dokument** aus.
6. Wählen Sie **Hinzufügen** aus.
7. Führen Sie im Drop-Down-Dialogfeld die folgenden Schritte aus:

    1. Wählen Sie in der Struktur **XML\\Attribut** aus.
    2. Geben Sie im Feld **Name** **ID** ein.
    3. Wählen Sie **OK**.

    ![Formatdesignerseite](media/GER-BaselineSample-FormatLayoutDesign.PNG "Screenshot der Format Designer Seite")

8. Auf der Registerkarte **Zuordnung** wählen Sie **Löschen** aus.
9. Wählen Sie **Stamm hinzufügen** aus.
10. Wählen Sie im Drop-Down-Dialogfeld in der Struktur die Option **Allgemein\\Benutzereingabeparameter** aus, und führen Sie dann die folgenden Schritte aus:

    1. Geben Sie im Feld **Name** **ID** ein.
    2. Geben Sie im Feld **Bezeichnung** **Eingabe-ID** ein.
    3. Wählen Sie **OK**.

11. Wählen Sie in der Struktur **Ausgabe\\Dokument\\Id** aus.
12. Wählen Sie **Binden** und dann **Speichern** aus.

![Formatdesignerseite](media/GER-BaselineSample-FormatMappingDesign.PNG "Screenshot der Format Designer Seite")

Auf Grundlage die entworfenen Struktur generiert das konfigurierte Format eine XML-Datei. Diese XML enthält das Element **Stamm** mit dem Attribut **ID**, das auf den Wert festgelegt wird, den der Benutzer im ER-Laufzeitdialogfeld eingibt.

### <a name="generate-a-new-baseline-file-for-a-designed-er-format"></a>Generieren einer neuen Grundlagendatei für ein entworfenes ER-Format

1. Wählen Sie auf der Seite **Konfigurationen** auf dem Inforegister **Versionen** die Option **Ausführen** aus.
2. Geben Sie im Feld **Eingabe-ID** den Wert **1** ein.
3. Wählen Sie **OK**.

    ![Dialogfeld für elektronische Berichtsparameter ](media/GER-BaselineSample-FormatRunToMakeBaselineFile1.PNG "Screenshot des Dialogfensters Elektronische Berichtsparameter")

4. Speichern Sie eine lokale Kopie der Datei **out.Admin.xml**, die erzeugt wird, damit Sie sie später als Grundlage für dieses ER-Format verwenden können.

    ![Benachrichtigung über die generierte Datei auf der Seite Konfigurationen](media/GER-BaselineSample-FormatRunToMakeBaselineFile2.PNG "Screenshot der Benachrichtigung über die generierte Datei auf der Seite Konfigurationen")

### <a name="configure-er-parameters-to-use-the-baseline-feature"></a>Konfigurieren Sie die ER-Parameter, um die Grundlagenfunktion zu verwenden

1. Wählen Sie auf der Seite **Konfigurationen** im Aktivitätsbereich auf der Registerkarte **Konfigurationen** die Option **Benutzerparameter** aus.
2. Legen Sie die Option **In Debugmodus ausführen** auf **Ja** fest.
3. Wählen Sie **OK**.

![Benutzerparameter-Dialogfeld](media/GER-BaselineSample-ERUserParameters.PNG "Screenshot des Dialogfensters Benutzerparameter")

### <a name="add-a-new-baseline-for-designed-er-format"></a>Fügen Sie eine neue Grundlage für ein entworfenes ER-Format hinzu

1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.
2. Wählen Sie im Aktivitätsbereich **Grundlagen** aus.

    ![Baselines-Schaltfläche auf der Seite Konfigurationen](media/GER-BaselineSample-OpenBaselinePage.PNG "Screenshot der Schaltfläche Baselines auf der Seite Konfigurationen")

3. Wählen Sie im Aktivitätsbereich **Neu** aus.
4. Wählen Sie das ER-Format **Format zum Erlernen der ER-Grundlagen** aus, die Sie zuvor entworfen haben.
5. Wählen Sie **Speichern**.

![Elektronisches Berichtsformat Basislinien Seite](media/GER-BaselineSample-AddBaseline.PNG "Screenshot der Seite Baselines des elektronischen Berichtsformats")

Die Grundlegende wird für das Format **Format zum Erlernen von ER-Grundlagen** hinzugefügt.

### <a name="configure-a-baseline-rule-for-the-added-baseline"></a>Konfigurieren Sie eine Grundlagenregel für die hinzugefügte Grundlage

1. Auf der Seite **Formatgrundlagen für elektronische Berichterstellung** wählen Sie im Aktivitätsbereich die Schaltfläche **Anhänge** (das Büroklammersymbol) aus.
2. Wählen Sie im Aktivitätsbereich **Neu** \> **Datei** aus. In den ER-Parametern sollte der Dokumenttyp **Datei** zuvor als ausgewählt worden sein, da der Dokumenttyp zum Speichern von Grundlagendateien verwendet wird.
3. Wählen Sie **Durchsuchen** und die Datei **out.Admin.xml** aus, die generiert wurde, als Sie die zuvor das konfigurierte ER-Format ausgeführt haben.

    ![Anhänge-Seite](media/GER-BaselineSample-UploadBaselineFile.PNG "Screenshot der Seite Anlagen")

4. Schließen Sie die Seite **Anhänge**.
5. Auf dem Inforegister **Grundlagen** wählen Sie **Neu** aus.
6. Geben Sie im Feld **Name** **Grundlage 1** ein.
7. Geben Sie im Feld **Dateikomponentenname** **Ausgabe** aus oder wählen Sie sie aus. Dieser Wert gibt an, dass die konfigurierte Grundlage mit einer Datei verglichen wird, die mithilfe des Formatelements **Ausgabe** generiert wird.
8. Geben Sie im Feld **Dateinamenmaske** **\*.xml** ein.

    > [!NOTE]
    > Sie können die Dateinamenmaske definieren. Wenn die Dateinamenmaske definiert ist, wird der Grundlagendatensatz verwendet, um die generierte Ausgabe zu bewerten, wenn der Name der Ausgabedatei, die erzeugt werden soll, der Maske entspricht.

9. Wenn die konfigurierte Grundlage nur verwendet werden soll, wenn das ER-Format **Format zum Erlernen von ER-Grundlagen** von Benutzern ausgeführt wird, die in bestimmten Unternehmen angemeldet sind, wählen Sie diese Unternehmen im Feld **Unternehmen** aus.
10. Geben Sie im Feld **Grundlage** den Anhang **out.Admin** ein oder wählen Sie ihn aus.
11. Wählen Sie **Speichern**.

![Elektronisches Berichtsformat Basislinien Seite](media/GER-BaselineSample-SetupBaselineLine.PNG "Screenshot der Seite Baselines des elektronischen Berichtsformats")

### <a name="run-the-designed-er-format-and-review-the-log-to-analyze-the-results"></a>Führen Sie das entworfene ER-Format aus und prüfen Sie das Protokoll, um die Ergebnisse zu analysieren

1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.
2. In der Struktur erweitern Sie **Modell zum Erlernen von ER-Grundlagen** und dann wählen Sie **Modell zum Erlernen von ER-Grundlagen\\Format zum Erlernen von ER-Grundlagen** aus.
3. Wählen Sie im Inforegister **Versionen** **Ausführen** aus.
4. Geben Sie im Feld **Eingabe-ID** den Wert **1** ein.
5. Wählen Sie **OK**.
6. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurations-Debug-Protokolle**.

    ![Elektronische Berichterstellung Laufprotokolle Seite](media/GER-BaselineSample-ReviewBaselineComparison1.PNG "Screenshot der Seite mit den Protokollen für die elektronische Berichterstattung")

    > [!NOTE]
    > Das Ausführungsprotokoll enthält Informationen über die Ergebnisse des Vergleichs der generierten Datei mit der konfigurierten Grundlage. In diesem Beispiel gibt das Protokoll an, dass die generierte Datei und die Grundlage gleich sind.

7. Wählen Sei **Alle löschen** aus.

### <a name="run-the-designed-er-format-and-review-the-log-to-analyze-the-results"></a>Führen Sie das entworfene ER-Format aus und prüfen Sie das Protokoll, um die Ergebnisse zu analysieren

1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.
2. In der Struktur erweitern Sie **Modell zum Erlernen von ER-Grundlagen** und dann wählen Sie **Modell zum Erlernen von ER-Grundlagen\\Format zum Erlernen von ER-Grundlagen** aus.
3. Wählen Sie im Inforegister **Versionen** **Ausführen** aus.
4. Geben Sie im Feld **Eingabe-ID** den Wert **2** ein.
5. Wählen Sie **OK**.
6. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurations-Debug-Protokolle**.

    ![Elektronische Berichterstellung Laufprotokolle Seite](media/GER-BaselineSample-ReviewBaselineComparison2.PNG "Screenshot der Seite mit den Protokollen für die elektronische Berichterstattung")

    > [!NOTE]
    > Das Ausführungsprotokoll enthält Informationen über die Ergebnisse des Vergleichs der generierten Datei mit der konfigurierten Grundlage. In diesem Beispiel gibt das Protokoll an, dass die generierte Datei und die Grundlage unterschiedlich sind.

7. Wählen Sie **Vergleichen** aus.

> [!NOTE]
> Die generierte Datei und die Grundlagendatei werden als ZIP-Datei angeboten. Sie können externe Vergleichstools wie WinDiff verwenden, um die Dateien zu vergleichen und die Unterschiede zu prüfen.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Konfigurieren Sie das Electronic Reporting (ER) Framework](electronic-reporting-er-configure-parameters.md).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]