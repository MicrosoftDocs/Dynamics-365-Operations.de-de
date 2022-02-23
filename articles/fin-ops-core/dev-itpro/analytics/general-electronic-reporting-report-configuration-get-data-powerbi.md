---
title: Konfigurieren elektronischer Berichterstattung (EB), um Daten in Power BI einzubeziehen
description: In diesem Thema wird erläutert, wie Sie die Konfiguration der elektronischen Berichterstellung (EB) verwenden können, um die Übertragung von Daten aus Ihrer Instanz zu den Power BI-Diensten zu veranlassen.
author: NickSelin
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 34d4ad9106b2751c77db4fd03d83932e587a5332
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680119"
---
# <a name="configure-electronic-reporting-er-to-pull-data-into-power-bi"></a>Konfigurieren elektronischer Berichterstattung (EB), um Daten in Power BI einzubeziehen

[!include [banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie die Konfiguration der elektronischen Berichterstellung (EB) verwenden können, um die Übertragung von Daten aus Ihrer Instanz zu den Power BI-Diensten zu veranlassen. Als Beispiel verwendet dieses Thema Intrastat-Buchungen als Geschäftsdaten, die übertragen werden müssen. Die Power BI-Zuordnungsvisualisierung verwendet diese Intrastat-Buchungsdaten, um eine Ansicht zur Analyse von Import-/Exportaktivitäten von Unternehmen im Power BI-Bericht darzustellen.

## <a name="overview"></a>Übersicht

Microsoft Power BI ist eine Sammlung von Softwaredienstleistungen, Apps und Konnektoren, die zusammenarbeiten, um externe Quellen von Daten in zusammenhängende, visuell anschauliche und interaktive Überblicke zu verwandeln. Mit der elektronischen Berichterstellung (EB) können Benutzer leicht Datenquellen konfigurieren und die Übertragung von Daten der Anwendung zu Power BI veranlassen. Die Daten werden als Dateien im OpenXML-Arbeitsblattformat (Microsoft Excel-Arbeitsmappendatei) übertragen. Die übertragenen Dateien werden auf einem Microsoft SharePoint Server gespeichert, der für diesen Zweck konfiguriert wurde. Die gespeicherten Dateien werden in Power BI verwendet, um Berichte zu erstellen, die Visualisierungen enthalten (Tabellen, Diagramme, Karten usw.). Power BI-Berichte werden für Power BI-Benutzer freigegeben, und auf sie wird in Power BI-Dashboards und auf den Anwendungsseiten zugegriffen. In diesem Thema werden die folgenden Aufgaben erläutert:

- Konfigurieren von Microsoft Dynamics 365 Finance
- Bereiten Sie die Formatkonfiguration Ihrer elektronischen Berichterstellung vor, um Daten aus der Finance-Anwendung abzurufen.
- Konfigurieren Sie die EB-Umgebung, um Daten nach Power BI zu übertragen.
- Verwenden Sie übertragene Daten, um einen Power BI-Bericht zu erstellen.
- Machen Sie den Power BI-Bericht in Finance zugänglich.

## <a name="prerequisites"></a>Voraussetzungen
Um das Beispiel in diesem Thema abzuschließen, müssen Sie den folgenden Zugriff haben:

- Zugriff für eine der folgenden Rollen:

    - Entwickler für elektronische Berichterstellung
    - Funktionaler Berater für elektronische Berichterstellung
    - Systemadministrator

- Zugriff auf die SharePoint Server, die für die Verwendung mit der Anwendung konfiguriert ist
- Zugriff auf das Power BI-Framework

## <a name="configure-document-management-parameters"></a>Parameter der Dokumentverwaltung konfigurieren
1. Konfigurieren Sie auf der Seite **Parameter für Dokumentverwaltung** den Zugriff auf SharePoint Server, der im Unternehmen verwendet wird, bei dem Sie sich angemeldet haben (in diesem Beispiel das Unternehmen DEMF).
2. Testen Sie die Verbindung zum SharePoint Server, um sicherzustellen, dass Ihnen der Zugriff gewährt wurde.

    [![Seite "Parameter der Dokumentverwaltung"](./media/ger-power-bi-sharepoint-server-setting-1024x369.png)](./media/ger-power-bi-sharepoint-server-setting.png)

3. Öffnen Sie die konfigurierte SharePoint-Site. Erstellen Sie einen neuen Ordner, in dem die elektronische Berichterstellung Excel-Dateien speichert, die die Geschäftsdaten umfassen, die Power BI-Berichte als Quelle von Power BI-Datasets benötigen.
4. Erstellen Sie auf der Seite **Dokumenttypen** einen neuen Dokumenttyp, der für den Zugriff auf den SharePoint-Ordner verwendet wird, den Sie soeben erstellt haben. Geben Sie **Datei** in das Feld **Gruppe** und **SharePoint** in das Feld **Standort** ein, und geben Sie dann die Adresse des SharePoint-Ordners ein.

    [![Seite „Dokumenttypen”](./media/ger-power-bi-sharepoint-document-type-1024x485.png)](./media/ger-power-bi-sharepoint-document-type.png)

## <a name="configure-er-parameters"></a>Parameter der elektronischen Berichterstellung konfigurieren
1. Klicken Sie im Arbeitsbereich **Elektronische Berichterstellung** auf den Link **Parameter der elektronischen Berichterstellung**.
2. Wählen Sie auf der Registerkarte **Anhänge** den Dokumenttyp **Datei** für alle Felder aus.
3. Machen Sie im Arbeitsbereich **Elektronische Berichterstellung** den erforderlichen Anbieter aktiv, indem Sie auf **Auf "aktiv" festlegen** klicken. Um weitere Informationen zu erhalten, geben Sie den Aufgabenleitfaden **Elektronische Berichterstellung – Dienstanbieter auswählen** wieder.

## <a name="use-an-er-data-model-as-the-source-of-data"></a>Verwenden eines Datenmodells zur elektronischen Berichterstellung als die Datenquelle
Sie müssen ein Datenmodell zur elektronischen Berichterstellung als Quelle von Geschäftsdaten haben, die bei Power BI-Berichten verwendet werden. Dieses Datenmodell wir vom Konfigurationsrepository der elektronischen Berichterstellung hochgeladen. Weitere Informationen finden Sie unter [Elektronische Berichterstellungskonfigurationen des Downloads von Lebenszyklusdiensten](download-electronic-reporting-configuration-lcs.md), oder geben Sie den Aufgabenleitfaden **Elektronische Berichterstellung – Importieren einer Konfiguration aus den Lebenszyklusdiensten** wieder. Wählen Sie **Intrastat** als das Datenmodell aus, das vom ausgewählten Konfigurationsrepository der elektronischen Berichterstellung hochgeladen wird. (In diesem Beispiel wird Version 1 des Modells verwendet). Sie können die **Intrastat** ER-Modell-Konfiguration auf der **Konfigurationen** Seite zugreifen.

[![Seite "Konfigurationen"](./media/ger-power-bi-data-model-1024x371.png)](./media/ger-power-bi-data-model.png)

## <a name="design-an-er-format-configuration"></a>Eine Formatkonfiguration für die elektronische Berichterstellung entwerfen
Sie müssen eine neue Formatkonfiguration für elektronische Berichterstellung erstellen, die das Datenmodell **Intrastat** als Quelle von Geschäftsdaten verwendet. Diese Formatkonfiguration muss Ausgabeergebnisse als elektronische Dokumente im OpenXML-(Excel-Datei)-Format erstellen. Für weitere Informationen geben Sie den Aufgabenleitfaden **Elektronische Berichterstellung – Eine Konfiguration für Berichte im OPENXML-Format erstellen** wieder. Benennen Sie die neue Konfiguration **Aktivitäten importieren / exportieren**, wie in der folgenden Abbildung dargestellt. Verwenden Sie die [Daten der elektronischen Berichterstellung – Details importieren und exportieren](https://go.microsoft.com/fwlink/?linkid=845208) Excel-Datei als Vorlage, wenn Sie das Format der elektronischen Berichterstellung entwerfen. (Um weitere Informationen darüber zu erhalten, wie eine Formatvorlage importiert wird, geben Sie den Aufgabenleitfaden wieder.)

![[Aktivitätenkonfiguration importieren / exportieren](media/ger-power-bi-format-configuration.png)](media/ger-power-bi-format-configuration.png)

Um das Format **Import-/Exportaktivitäten** zu ändern, führen Sie die folgenden Schritte aus.

1. Klicken Sie auf **Designer**.
2. Auf der Registerkarte **Formate** benennen Sie das Dateielement für dieses Format **Excel-Ausgabedatei**.

    [![Excel-Ausgabedateielement](./media/ger-power-bi-format-configuration-file-element-name-1024x395.png)](./media/ger-power-bi-format-configuration-file-element-name.png)

3. Geben Sie auf der Registerkarte **Zuordnung** den Namen der Excel-Datei an, die jedes Mal generiert wird, wenn dieses Format ausgeführt wird. Konfigurieren Sie den zugehörigen Ausdruck, um den Wert **Details importieren und exportieren** zurückzugeben (die .xlsx-Dateinamenerweiterung wird automatisch hinzugefügt).

    [![Formatdesigner](./media/ger-power-bi-format-configuration-output-file-name-1024x396.png)](./media/ger-power-bi-format-configuration-output-file-name.png)

4. Fügen Sie ein neues Datenquellelement für dieses Format hinzu. (Diese Enumeration ist für weitere Datenbindung erforderlich.)

    1. Benennen Sie die Datenquelle **direction\_enum**.
    2. Wählen Sie **Datenmodellenumeration** als den Datenquellentyp aus.
    3. Verweisen Sie auf die Datenmodellenumeration **Richtung**.

    [![direction_enum](./media/ger-power-bi-format-configuration-mapping-added-enum-1024x454.png)](./media/ger-power-bi-format-configuration-mapping-added-enum.png)

5. Schließen Sie die Bindung der Elemente des **Intrastat**-Datenmodells und der Elemente des entworfenen Formats ab, wie in der folgenden Abbildung dargestellt.

    [![Die Bindung abschließen](./media/ger-power-bi-format-configuration-mapping-details-1024x454.png)](./media/ger-power-bi-format-configuration-mapping-details.png)

Nachdem diese ausgeführt ist, generiert das Format der elektronischen Berichterstellung das Ausgabeergebnis im Excel-Format. Es sendet die Details der Intrastat-Buchungen zum Ausgabeergebnis und trennt sie als Transaktionen, die entweder Importaktivitäten oder Exportaktivitäten beschreiben. Klicken Sie **Ausführen** auf, um das neue Format der elektronischen Berichterstellung für die Liste von **Intrastat**-Buchungen auf der Seite Intrastat zu testen (**Steuer** &gt; **Meldungen** &gt; **Außenhandel** &gt; **Intrastat)**.

![[Intrastat-Seite](./media/ger-power-bi-format-test-run-transactions-1024x322.png)](./media/ger-power-bi-format-test-run-transactions.png)

Das folgende Ausgabeergebnis wird generiert. Die Datei wird **Import- und Exportdetails.xlsx** benannt, wie Sie in den Formateinstellungen angegeben haben.

[![Import- und Exportdetails.xlsx](./media/ger-power-bi-format-test-run-output-1024x472.png)](./media/ger-power-bi-format-test-run-output.png)

## <a name="configure-the-er-destination"></a>Das Ziel der elektronischen Berichterstellung konfigurieren
Sie müssen das Framework der elektronischen Berichterstellung so konfigurieren, dass es das Ausgabeergebnis der neuen Formatkonfiguration der elektronischen Berichterstellung auf besondere Weise sendet.

- Das Ausgabeergebnis muss zum Ordner des ausgewählten SharePoint Servers gesendet werden.
- Bei jeder Ausführung der Formatkonfiguration muss eine neue Version derselben Excel-Datei erstellt werden.

Klicken Sie auf der Seite **Elektronische Berichterstellung** (**Organizationsverwaltung** &gt; **Elektronische Berichterstellung**) auf das Element **Elektronisches Berichterstellungsziel** und fügen Sie ein neues Ziel hinzu. Wählen Sie im Feld **Referenz** die Formatkonfiguration **Import-/Exportaktivitäten** aus, die Sie zuvor erstellt haben. Gehen Sie folgendermaßen vor, um einen neuen Dateiziel-Datensatz für die Referenz hinzufügen.

1. Geben Sie im Feld **Name** den Titel des Dateiziels ein.
2. Wählen Sie im Feld **Dateiname** den Namen **Excel-Ausgabedatei** für die Excel-Dateiformatkomponente aus.

Klicken Sie auf die Schaltfläche **Einstellungen** für den neuen Zieldatensatz. Führen Sie dann im Dialogfeld **Zieleinstellungen** die folgenden Schritte aus.

1. Auf der Registerkarte **Power BI** legen Sie die Option **Aktiviert** auf **Ja** fest.
2. Wählen Sie im Feld **SharePoint** den Dokumenttyp **Freigegeben** aus, den Sie zuvor erstellt haben.

## <a name="schedule-execution-of-the-configured-er-format"></a>Zeitplanausführung des konfigurierten Formats der elektronischen Berichterstellung
1. Wählen Sie auf der Seite **Konfigurationen** (**Organisationsverwaltung** &gt; **Elektronische Berichterstellung** &gt; **Konfigurationen**) in der Konfigurationsstruktur die Konfiguration Aktivitäten **importieren / exportieren** aus, die Sie zuvor erstellt haben.
2. Ändern Sie den Status von Version 1.1 von **Entwurf** auf **Abgeschlossen**, um dieses Format zur Verwendung bereitzustellen.

    [![Seite "Konfigurationen"](./media/ger-power-bi-format-configuration-complete-1024x401.png)](./media/ger-power-bi-format-configuration-complete.png)

3. Wählen Sie abgeschlossene Version der Konfiguration **Aktivitäten importieren / exportieren** aus, und klicken Sie dann auf **Ausführen**. Beachten Sie, dass das konfigurierte Ziel auf das Ausgabeergebnis angewendet wird, das im Excel-Format generiert wird.
4. Legen Sie die Option **Stapelverarbeitung** auf **Ja** fest, um diesen Bericht im unbeaufsichtigten Modus auszuführen.
5. Klicken Sie auf **Wiederholung**, um die obligatorische Wiederholung dieser Stapelverarbeitung zu planen. Die Wiederholung definiert, wie oft die aktualisierten Daten nach Power BI übertragen werden.

    [![Dialogfeld Parameter für elektronische Berichterstellung](./media/ger-power-bi-format-configuration-run-to-schedule-1024x413.png)](./media/ger-power-bi-format-configuration-run-to-schedule.png)

6. Nachdem dieser konfiguriert ist, können Sie den Berichtsausführungseinzelvorgang der elektronischen Berichterstellung auf der Seite **Batchaufträge** finden (**Systemverwaltung &gt; Abfragen &gt; Batchaufträge**).

    [![Seite Batchaufträge](./media/ger-power-bi-format-configuration-running-job-1024x410.png)](./media/ger-power-bi-format-configuration-running-job.png)

7. Wenn dieser Einzelvorgang erstmals ausgeführt wird, erstellt das Ziel eine neue Excel-Datei, die den konfigurierten Namen im ausgewählten SharePoint-Ordner aufweist. An jedem darauf folgenden Zeitpunkt, an dem der Einzelvorgang ausgeführt wird, erstellt das Ziel eine neue Version dieser Excel-Datei.

    [![Neue Version der Excel-Datei](./media/ger-power-bi-output-file-in-sharepoint-server-folder-2-1024x412.png)](./media/ger-power-bi-output-file-in-sharepoint-server-folder-2.png)

## <a name="create-a-power-bi-dataset-by-using-the-output-result-of-the-er-format"></a>Ein Power BI-Dataset mithilfe des Ausgabeergebnisses des Formats der elektronischen Berichterstellung erstellen
1. Melden Sie sich bei Power BI an, und öffnen Sie entweder eine vorhandene Power BI-Gruppe (Arbeitsbereich) oder erstellen Sie eine neue Gruppe. Klicken Sie entweder auf **Hinzufügen** unter **Dateien** im Bereich **Importieren oder mit Daten verbinden**, oder klicken Sie auf das Pluszeichen (**+**) neben **Datasets** im linken Bereich.

    [![Ein Dataset erstellen](./media/ger-power-bi-add-dataset-1024x524.png)](./media/ger-power-bi-add-dataset.png)

2. Wählen Sie die Option **SharePoint – Teamwebsites** aus, und geben Sie dann den Pfad von SharePoint Server ein, den Sie verwenden (in unserem Beispiel `https://ax7partner.litware.com`).
3. Navigieren Sie dann zum Ordner **/Freigegebene Dokumente/GER-Daten/PowerBI**, und wählen Sie die Excel-Datei aus, die Sie als Datenquelle für das neue Power BI-Dataset erstellt haben.

    [![Auswählen der Excel-Datei](./media/ger-power-bi-add-dataset-select-excel-file-1024x522.png)](./media/ger-power-bi-add-dataset-select-excel-file.png)

4. Klicken Sie auf **Verbinden** und klicken Sie dann auf **Importieren**. Ein neues Dataset wird erstellt, das auf der ausgewählten Excel-Datei basiert. Das Dataset kann auch automatisch der dem neu erstellten Dashboard hinzugefügt werden.

    [![Dataset auf dem Dashboard](./media/ger-power-bi-added-dataset-1024x489.png)](./media/ger-power-bi-added-dataset.png)

5. Konfigurieren Sie den Aktualisierungszeitplan für dieses Dataset, um ein periodisches Update zu erzwingen. Periodische Aktualisierungen ermöglichen die Nutzung neuer Geschäftsdaten, die eingehen, und zwar mittels der periodischen Ausführung des Berichts der elektronischen Berichterstellung durch neue Versionen der Excel-Datei, die auf dem SharePoint Server erstellt werden.

## <a name="create-a-power-bi-report-by-using-the-new-dataset"></a>Einen Power BI-Bericht mithilfe des neuen Datasets erstellen
1. Klicken Sie auf das Power BI-Dataset **Import- und Exportdetails**, das Sie erstellt haben.
2. Konfigurieren Sie dann die Visualisierung. Wählen Sie beispielsweise die Visualisierung **Ausgefüllte Zuordnung** aus, und konfigurieren Sie sie wie folgt:

    - Weisen Sie das Datasetfeld **CountryOrigin** dem Feld **Lagerplatz** in der Zuordnungsvisualisierung zu.
    - Weisen Sie das Datasetfeld **Betrag** dem Feld **Farbsättigung** der Zuordnungsvisualisierung zu.
    - Fügen Sie die Datasetfelder **Aktivität** und **Jahr** der Feldersammlung **Filter** der Zuordnungsvisualisierung hinzu.

3. Speichern Sie den Power BI-Bericht als **Import- und Exportdetailbericht**.

    [![Import- und Exportdetailbericht.xlsx](./media/ger-power-bi-added-report-1024x498.png)](./media/ger-power-bi-added-report.png)

    Beachten Sie, dass die Zuordnung das Land/die Region anzeigt, die in der Excel-Datei erwähnt werden (Österreich und die Schweiz in diesem Beispiel). Diese Länder/Regionen werden gefärbt, um den Anteil der fakturierten Beträge für jede(s) von ihnen anzuzeigen.

4. Aktualisieren Sie die Liste der Intrastat-Buchungen. Die Exportbuchung, die ihren Ursprung in Italien hat, wurde hinzugefügt.

    [![Intrastat-Buchungsliste](./media/ger-power-bi-new-run-new-transaction-1024x321.png)](./media/ger-power-bi-new-run-new-transaction.png)

5. Warten Sie auf die nächste geplante Ausführung des Berichts der elektronischen Berichterstellung und das nächste geplante Update des Power BI-Dataset. Überprüfen Sie dann den Power BI-Bericht (wählen Sie aus, dass nur Importbuchungen angezeigt werden). Die aktualisierte Zuordnung zeigt jetzt Italien an.

    [![Aktualisierte Zuordnung](./media/ger-power-bi-new-run-new-map-1024x511.png)](./media/ger-power-bi-new-run-new-map.png)

## <a name="access-power-bi-report-in-finance"></a>Zugreifen auf den Power BI-Bericht in Finance
Einrichten der Integration in Power BI. Weitere Informationen finden Sie unter [Konfiguration der Power BI-Integration für Workspaces](configure-power-bi-integration.md).

1. Auf der Arbeitsbereichsseite **Elektronische Berichterstellung**, die die Power BI-Integration unterstützt (**Organisationsverwaltung** &gt; **Arbeitsbereiche** &gt; **Arbeitsbereich der elektronischen Berichterstellung**), klicken Sie auf **Optionen** &gt; **Berichtskatalog öffne**.
2. Wählen Sie den Power BI-Bericht **Import- und Exportdetails** aus, den Sie erstellt haben, um diesen Bericht als Aktivitätselement auf der ausgewählten Seite anzuzeigen.
3. Klicken Sie auf das Aktivitätselement, um die Seite zu öffnen, die den Bericht anzeigt, den Sie in Power BI entworfen haben.

    [![Import- und Exportdetailbericht.xlsx](./media/ger-power-bi-review-bi-report-in-ax-form-1024x586.png)](./media/ger-power-bi-review-bi-report-in-ax-form.png)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Ziele für elektronische Berichterstellung (EB)](electronic-reporting-destinations.md)

[Überblick über die elektronische Berichterstellung (Electronic reporting, ER)](general-electronic-reporting.md)
