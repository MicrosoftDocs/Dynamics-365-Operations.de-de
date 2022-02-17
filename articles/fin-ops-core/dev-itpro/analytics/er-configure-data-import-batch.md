---
title: Importieren von Daten aus manuell ausgewählten Dateien im Batch-Modus
description: In diesem Thema wird erklärt, wie Sie Daten aus manuell ausgewählten Dateien im Batch-Modus importieren.
author: NickSelin
ms.date: 01/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERImportFormatSourceTable, ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2022-01-01
ms.dyn365.ops.version: Release 10.0.25
ms.openlocfilehash: 8615b5a0623fd696c64f4ec03e481a2bcb16c0ac
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8075611"
---
# <a name="import-data-from-manually-selected-files-in-batch-mode"></a>Importieren von Daten aus manuell ausgewählten Dateien im Batch-Modus

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

Um das [Electronic Reporting (ER)](general-electronic-reporting.md) Framework zum Importieren von Daten aus manuell ausgewählten eingehenden Dateien im Batch-Modus zu verwenden, konfigurieren Sie ein ER [Format](er-overview-components.md#format-component), das den Import unterstützt. Führen Sie dann eine [Modellzuordnung](er-overview-components.md#model-mapping-component) vom Typ **Ziel** aus, die dieses Format als Datenquelle verwendet. Um Daten zu importieren, navigieren Sie zu der Datei, die Sie importieren möchten, und wählen Sie sie manuell aus. 

Die neue Funktionalität von ER, die den Datenimport im Batch-Modus unterstützt, ermöglicht es, diesen Prozess als unbeaufsichtigt zu konfigurieren. Sie können ER-Konfigurationen verwenden, um den Datenimport durchzuführen, indem Sie einen neuen Batchauftrag über die ER-Benutzeroberfläche (UI) einplanen.

In diesem Thema wird erklärt, wie Sie den Datenimport aus einer manuell ausgewählten Datei im Batch-Modus abschließen. Die Beispiele verwenden Kreditorenbuchungen als Geschäftsdaten. Die Schritte dieser Beispiele können in der Firma **USMF** ausgeführt werden. Eine Codierung ist nicht erforderlich.

## <a name="prerequisites"></a>Voraussetzungen

Um die Beispiele in diesem Thema abzuschließen, müssen Sie den folgenden Zugriff haben:

- Eine der folgenden Rollen:

    - Entwickler für elektronische Berichterstellung
    - Funktionaler Berater für elektronische Berichterstellung
    - Systemadministrator

- ER Format- und Modellkonfigurationen für 1099 Zahlungen

### <a name="create-the-required-er-configurations"></a>Erzeugen Sie die erforderlichen ER-Konfigurationen

Um die erforderlichen ER-Konfigurationen zu erstellen und andere Voraussetzungen zu schaffen, folgen Sie einem dieser Schritte:

- Geben Sie die Aufgabenleitfäden **Daten aus einer Microsoft Excel-Datei mit EB importieren** wieder, die Teil des **7.5.4.3 IT-Dienstleistungs-/-Lösungskomponenten anschaffen/entwickeln (10677)**-Geschäftsprozess sind. Diese Anleitungen führen Sie durch den Prozess der Erstellung und Verwendung von ER-Konfigurationen, die interaktiv Transaktionen von Kreditoren aus Microsoft Excel-Dateien importieren. Weitere Informationen finden Sie unter [Eingangsdokumente im Excel-Format analysieren](parse-incoming-documents-excel.md).
- Vervollständigen Sie die Beispiele in [Konfigurieren Sie den Datenimport aus SharePoint](er-configure-data-import-sharepoint.md). Diese Beispiele führen Sie durch die Entwicklung und Verwendung von ER-Konfigurationen, die interaktiv Kreditor-Transaktionen aus Excel-Dateien importieren, die in einem SharePoint-Ordner gespeichert sind.

### <a name="download-the-required-er-configurations"></a>Laden Sie die erforderlichen ER-Konfigurationen herunter

1. Laden Sie die folgenden ER-Konfigurationen herunter, und speichern Sie sie lokal.

    | Inhaltsbeschreibung | Datei |
    |---------------------|------|
    | **1099-Zahlungsmodell** ER-Datenmodell-Konfiguration | [1099model.xml](https://download.microsoft.com/download/b/d/9/bd9e8373-d558-4ab8-aa9b-31981adc97ea/1099model.xml) |
    | **Für den Import von Transaktionen von Kreditoren (Excel)** ER-Formatkonfiguration | [1099format-import-from-excel.xml](https://download.microsoft.com/download/b/3/8/b38faf0a-fbaf-4e9e-84c2-dedae7464880/1099format-import-from-excel.xml) |

2. Verwenden Sie die Option [Laden aus XML-Datei](er-defer-sequence-element.md#import-the-sample-er-configurations) ER, um die heruntergeladenen ER-Konfigurationen in der folgenden Reihenfolge in Ihre Instanz von Dynamics 365 Finance zu importieren:

    1. ER-Datenmodell-Konfiguration
    2. ER-Formatkonfiguration

### <a name="download-the-required-excel-files"></a>Laden Sie die erforderlichen Excel-Dateien herunter

- Laden Sie das folgende Beispieldataset herunter, und speichern Sie es lokal.

    | Inhaltsbeschreibung | Datei |
    |---------------------|------|
    | Eingehende **1099import-data.xlsx** Datei, die Beispieldaten für den Import enthält | [1099import-data.xlsx](https://download.microsoft.com/download/f/f/4/ff4dbce9-8364-4391-adee-877945ff01f7/1099import-data.xlsx) |

### <a name="review-the-prerequisites"></a>Überprüfen Sie die Voraussetzungen

1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.
2. Überprüfen Sie auf der Seite **Konfigurationen** die vorbereitete ER-Lösung für den Datenimport im Batch-Modus.
3. Überprüfen Sie die Konfiguration des Formats **Für den Import von Transaktionen der Kreditor (Excel)**.

    - Die Formatkomponente dieser Konfiguration ist so konzipiert, dass sie eine eingehende Excel-Datei analysiert.
    - Die Datenzuordnung in dieser Konfiguration dient dazu, das Basisdatenmodell mit Daten aus der geparsten Excel-Datei zu füllen.

    ![ER-Formatkonfiguration für den Import von Daten im Batch-Modus von der ER UI aus.](./media/er-configure-data-import-batch-configurations-1.png)

4. Überprüfen Sie die Konfiguration des **1099-Zahlungsmodells** Datenmodells.

    - Die Modellkomponente dieser Konfiguration stellt die Struktur des Datenmodells dar, das zur Weitergabe von Daten zwischen ausgeführten ER-Komponenten verwendet wird.
    - Die Komponente für die Modellzuordnung dieser Konfiguration wird verwendet, um Daten aus der ausgeführten Formatkomponente zu ziehen und dann die Anwendungstabellen zu aktualisieren.

    ![ER-Datenmodellkonfiguration für den Import von Daten im Batch-Modus aus der ER-Benutzeroberfläche.](./media/er-configure-data-import-batch-configurations-2.png)

5. Öffnen Sie die Datei **1099import-data.xlsx** in Excel.

    ![Excel-Beispieldatei mit Daten für den Import im Batch-Modus.](./media/er-configure-data-import-batch-excel-content.png)

## <a name="enable-batch-data-import-for-er-from-the-ui"></a>Aktivieren Sie den Batch-Datenimport für ER über die Benutzeroberfläche

1. Wechseln Sie zu **Systemverwaltung** \> **Arbeitsbereiche** \> **Datenverwaltung**.
2. Markieren Sie im Arbeitsbereich **Funktionsverwaltung** die Funktion **ER-Import von manuell hochgeladenen Belegen im Batch ausführen** und wählen Sie dann **Jetzt aktivieren**.

## <a name="import-data-from-manually-selected-excel-files"></a>Importieren von Daten aus manuell ausgewählten Excel-Dateien

1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.
2. Wählen Sie auf der Seite **Konfigurationen** die Konfiguration des Datenmodells **1099 Zahlungen**.
3. Auf der Registerkarte **Konfigurationskomponenten** Inforegister, wählen Sie den Link **Für 1099 manuelle Transaktionen importieren**.
4. Auf der Seite **Modell-zu-Datenquelle Zuordnung** ist die **Für 1099 manuelle Transaktionen importieren** Modellzuordnung vorausgewählt. Wählen Sie **Ausführen** aus.
5. Auf der Registerkarte **Parameter** wählen Sie **Durchsuchen**. Suchen und wählen Sie die Datei **1099import-data.xlsx** und wählen Sie dann **OK**.
6. Geben Sie in das Feld **Belegnummer eingeben** **V-00001** ein.
7. Legen Sie auf der Registerkarte **Im Hintergrund ausführen** die Option **Batch-Verarbeitung** auf **Ja** fest.

    Beachten Sie, dass das Feld **Aufgabenbeschreibung** auf **Modellzuordnung 'Für 1099 manuelle Transaktionen importieren', Konfiguration '1099 Zahlungen Modell'** festgelegt ist. Dieser Wert gibt an, dass die Ausführung der ausgewählten Modellzuordnung als neuer Batchauftrag geplant wird.

    ![Angeben der Details des Datenimports im Batch-Modus im Dialogfeld Parameter für elektronische Berichte.](./media/er-configure-data-import-batch-execution-parameters.png)

8. Wählen Sie **OK** aus. Eine Nachricht benachrichtigt Sie, dass ein neuer Batchauftrag geplant wurde.

    ![Nachricht über einen neuen geplanten Batch-Auftrag auf der Seite Zuordnung von Modell zu Datenquelle.](./media/er-configure-data-import-batch-scheduled-job-info.png)

## <a name="review-the-data-import-results-on-the-batch-job-page"></a>Überprüfen Sie die Ergebnisse des Datenimports auf der Seite Batchauftrag

1. Wechseln Sie zu **Allgemeines** \> **Anfragen** \> **Batchaufträge** \> **Meine Batchaufträge**.
2. Filtern Sie auf der Seite **Batchauftrag** die Liste der Batchaufträge, um den geplanten Batch zu finden, und wählen Sie ihn dann aus.
3. Wählen Sie den Link **Auftrags-ID**, um die Auftragsdetails zu überprüfen.
4. Wählen Sie auf der Seite **Batch-Aufgaben** Inforegister **Protokoll**.

    ![Schaltfläche Protokollieren auf der Seite Batchauftrag.](./media/er-configure-data-import-batch-scheduled-job-record.png)

5. Überprüfen Sie die Ausführungsdetails.

    ![Ausführungsprotokoll des geplanten Batchauftrags auf der Seite Batchauftrag.](./media/er-configure-data-import-batch-scheduled-job-log.png)

## <a name="change-the-data-import-parameters"></a>Ändern Sie die Parameter für den Datenimport

Nachdem Ihr Batch geplant wurde und solange er noch nicht ausgeführt wurde, können Sie die Parameter des geplanten Datenimports ändern.

1. Wechseln Sie zu **Allgemeines** \> **Anfragen** \> **Batchaufträge** \> **Meine Batchaufträge**.
2. Filtern Sie auf der Seite **Batchauftrag** die Liste der Batchaufträge, um den geplanten Batch zu finden, und wählen Sie ihn dann aus.
3. Wählen Sie **Status ändern** aus.
4. Wählen Sie in der Dialogbox **Neuen Status auswählen** die Option **Zurückhalten** und wählen Sie dann **OK**.
5. Wählen Sie den Link **Job ID**, um auf die Auftragsdetails zuzugreifen.
6. Wählen Sie auf der Registerkarte **Batch-Aufgaben** Inforegister **Parameter**.
7. Führen Sie im Dialogfeld **Elektronische Berichtsparameter** die folgenden Schritte aus:

    1. Wählen Sie **Durchsuchen**, um die alternative Datei für den Datenimport auszuwählen.
    2. Wählen Sie **Belegnummer eingeben**, um die Belegnummer für den Import von Kreditor-Transaktionen zu ändern.

        ![Ändern Sie die Parameter des Datenimports für den geplanten Batchauftrag im Dialogfeld Parameter für elektronische Berichte.](./media/er-configure-data-import-batch-scheduled-job-parameters.png)

    3. Wählen Sie **OK** aus.

8. Vergewissern Sie sich, dass der Batch noch ausgewählt ist, und wählen Sie dann erneut **Status ändern**.
9. In der Dialogbox **Neuen Status auswählen** wählen Sie **Warten** und dann **OK**.

## <a name="review-the-data-import-results-on-the-er-source-page"></a>Überprüfen Sie die Ergebnisse des Datenimports auf der Seite ER-Quelle

1. Gehen Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstattung** \> **Elektronische Berichtsquelle**.
2. Wählen Sie den Datensatz **Für den Import von Transaktionen der Kreditoren (Excel)**, der beim Datenimport automatisch erstellt wurde.

    ![Datensatz für die Konfiguration für den Import von Transaktionen von Kreditoren (Excel) auf der Seite Quelle für elektronische Berichte.](./media/er-configure-data-import-batch-files-source-1.png)

3. Wählen Sie **Dateistatus für die Quellen**.
4. Überprüfen Sie auf den Seiten **Dateien** und **Quellenprotokolle für das Importformat** Inforegister die Importdetails.
5. Wählen Sie auf dem Inforegister **Dateien** den Datensatz aus. Beachten Sie, dass die importierte Datei an diesen Datensatz angehängt ist.

    ![Importierte Datei im Anhang des Datensatzes auf der Seite Dateistatus für die Quellen.](./media/er-configure-data-import-batch-files-source-2.png)

6. Wählen Sie **Anhänge**, um die importierte Datei zu überprüfen.

    ![Importierte Datei auf der Seite Dokumentenansicht.](./media/er-configure-data-import-batch-files-source-3.png)

    > [!TIP]
    > Um diese Anhänge aufzubewahren, verwendet das ER Framework einen Beleg-Typ, der für die aktuelle Firma im Feld **Sonstiges** der ER-Parameter [festgelegt](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) ist.

## <a name="review-the-data-import-results-on-the-vendor-settlement-for-1099s-page"></a>Überprüfen Sie die Ergebnisse des Datenimports auf der Seite Kreditor Abrechnung für 1099s

1. Gehen Sie zu **Kreditorenbuchhaltung** \> **Periodische Aufgaben** \> **Steuer 1099** \> **Kreditor-Abrechnung für 1099s**.
2. Geben Sie in das Feld **Ausgangsdatum** den Wert **12/31/2017** (31. Dezember 2017) ein.
3. Wählen Sie **Manuelle 1099 Transaktionen**.

    ![Importierte Kreditor-Transaktionen auf der Seite Tax 1099 Transaktionen.](./media/er-configure-data-import-batch-imported-data.png)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Überblick über die elektronische Berichterstellung](general-electronic-reporting.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
