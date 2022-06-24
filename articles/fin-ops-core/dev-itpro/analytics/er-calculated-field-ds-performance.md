---
title: Verbessern Sie die Leistung von EB-Lösungen, indem Sie parametrisierte CALCULATED FIELD-Datenquellen hinzufügen
description: Dieser Artikel erklärt, wie Sie die Leistung von Electronic Reporting (ER)-Lösungen verbessern können, indem Sie parametrisierte CALCULATED FIELD-Datenquellen hinzufügen.
author: NickSelin
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8c2c0499ac3d41c9bb6026cc05f971087799c28f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850113"
---
# <a name="improve-the-performance-of-er-solutions-by-adding-parameterized-calculated-field-data-sources"></a>Verbessern Sie die Leistung von EB-Lösungen, indem Sie parametrisierte CALCULATED FIELD-Datenquellen hinzufügen

[!include [banner](../includes/banner.md)]

In diesem Artikel wird erklärt, wie Sie [Leistungsnachverfolgungen](trace-execution-er-troubleshoot-perf.md) von [Elektronische Berichterstellung (EB)](general-electronic-reporting.md)-Formaten übernehmen können, die ausgeführt werden, und die dann die Informationen aus diesen Nachverfolgungen verwenden, um die Leistung durch das Konfigurieren eines Parameters zu verbessern, indem die **Berechnetes Feld**-Datenquelle parameterisiert wird.

Im Rahmen des Prozesses, EB-Konfigurationen zu entwerfen, um Geschäftsdokumente zu generieren, definieren Sie die Methode, mit der Daten aus der Anwendung abgerufen werden und in der generierten Ausgabe eingegeben werden. Durch das Entwerfen einer parametrisierten EB-Datenquelle des Typs **Berechnetes Feld** können Sie die Anzahl der Datenbankaufrufe reduzieren und den Zeit- und Kostenaufwand für das Sammeln der Details der Ausführung des EB-Formats erheblich reduzieren.

## <a name="prerequisites"></a>Voraussetzungen

- Um die Beispiele in diesem Artikel abzuschließen, müssen Sie den Zugriff auf eine der folgenden [Rollen](../sysadmin/tasks/assign-users-security-roles.md) haben:

    - Entwickler für elektronische Berichterstellung
    - Funktionaler Berater für elektronische Berichterstellung
    - Systemadministrator

- Das Unternehmen muss auf **DEMF** festgelegt sein.
- Folgen Sie den Schritten in [Anhang 1](#appendix1) dieses Artikels, um die Komponenten der Microsoft-EB-Beispiellösung herunterzuladen, die zum Abschließen der Beispiele in diesem Artikel erforderlich ist.
- Befolgen Sie die Schritte in [Anlage 2](#appendix2) dieses Artikels, um den minimalen Satz von EB-Parametern zu konfigurieren, der zur Verwendung des EB-Frameworks erforderlich ist, um die Leistung der Microsoft EB-Beispiellösung zu verbessern.

## <a name="import-the-sample-er-solution"></a>EB-Beispiellösung importieren

Stellen Sie sich vor, Sie müssen eine neue EB-Lösung entwerfen, um einen neuen Bericht zu generieren, der Kreditorentransaktionen zeigt. Aktuell können Sie die Transaktionen für einen ausgewählten Kreditor auf der Seite **Kreditorenbuchungen** suchen (wechseln Sie zu **Kreditor** \> **Kreditoren** \> **Alle Kreditoren**, wählen Sie einen Kreditor aus, und dann, im Aktivitätsbereich unter der Registerkarte **Kreditor** in der Gruppe **Transaktionen** wählen Sie **Transaktionen**). Sie möchten jedoch alle Kreditorenbuchungen zusammen in einem elektronischen Dokument im XML-Format haben. Diese Lösung besteht aus mehreren EB-Konfigurationen, die das erforderliche Datenmodell, die Modellzuordnung und Formatkomponenten enthalten.

Der erste Schritt besteht darin, die Beispiel-EB-Lösung zu importieren, um einen Bericht über Lieferantentransaktionen zu erstellen.

1. Melden Sie sich bei der Instanz von Microsoft Dynamics 365 Finance an, die für Ihr Unternehmen bereitgestellt wurde.
2. In diesem Artikel erstellen und ändern Sie Konfigurationen für das Beispielunternehmen **Litware, Inc.**. Stellen Sie sicher, dass dieser Konfigurationsanbieter Ihrer Finance-Instanz hinzugefügt wurde und als aktiv markiert wurde. Weitere Informationen finden Sie unter [Konfigurationsanbieter erstellen und als aktiv markieren](tasks/er-configuration-provider-mark-it-active-2016-11.md).
3. Im Arbeitsbereich **Elektronische Berichterstellung** wählen Sie die Kachel **Berichterstellungskonfigurationen** aus.
4. Auf der Seite **Konfigurationen** importieren Sie die EB-Konfigurationen, die Sie als Voraussetzung nach Finance heruntergeladen haben, in der folgenden Reihenfolge: Datenmodell, Modellzuordnung, Format. Führen Sie für jede Konfiguration die folgenden Schritte aus:

    1. Wählen Sie im Aktivitätsbereich **Austausch** \> **Aus XML-Datei laden** aus.
    2. Wählen Sie **Durchsuchen** aus, und wählen Sie die entsprechende Datei für die erforderliche EB-Konfiguration im XML-Format auszuwählen.
    3. Wählen Sie **OK** aus.

![Importierte Konfigurationen auf der Seite „Konfigurationen“.](./media/er-calculated-field-ds-performance-imported-configurations.png)

## <a name="review-the-sample-er-solution"></a>Die EB-Beispiellösung überprüfen

### <a name="review-the-model-mapping"></a>Die Modellzuordnung überprüfen

1. Erweitern Sie auf der Seite **Konfigurationen** in der Konfigurationsstruktur **Leistungsverbesserungsmodell** und wählen Sie dann **Leistungsverbesserungszuordnung** aus.
2. Wählen Sie im Aktivitätsbereich **Designer** aus.
3. Wählen Sie auf der Seite **Modell für Datenquellenzuordnung** im Aktionsbereich **Designer** aus.

    Diese EB-Modellzuordnung ist für die Durchführung der folgenden Aktionen vorgesehen:

    - Rufen Sie die Liste der Lieferantentransaktionen ab, die in der VendTrans-Tabelle gespeichert sind (**Trans**-Datenquelle).
    - Rufen Sie für jede Transaktion aus der VendTable-Tabelle den Datensatz eines Anbieters ab, für den die Transaktion gebucht wurde (**\#Vend**-Datenquelle).

    > [!NOTE]
    > Die **\#Vend**-Datenquelle ist so konfiguriert, dass der entsprechende Lieferantendatensatz unter Verwendung der vorhandenen n:1-Beziehung **\@.'\>Relations'.VendTable\_AccountNum** abgerufen wird.

    Die Modellzuordnung in dieser Konfiguration implementiert das Basisdatenmodell für alle EB-Formate, für die dieses Modell erstellt und in Finance ausgeführt wird. Demzufolge wird der Inhalt der **Trans** -Datenquellen für EB-Formate wie abstrakte **Modell**-Datenquellen bereitgestellt.

    ![Trans-Datenquelle auf der Modellzuordnungsdesigner-Seite.](media/er-calculated-field-ds-performance-mapping-1.png)

4. Schließen Sie die Seite **Modellzuordnungsdesigner**.
5. Schließen Sie die Seite **Zuordnung Modell zu Datenquelle**.

### <a name="review-format"></a>Überprüfen des Formats

1. Erweitern Sie auf der Seite **Konfigurationen** in der Konfigurationsstruktur **Leistungsverbesserungsmodell** und wählen Sie dann **Leistungsverbesserungsformat** aus.
2. Wählen Sie im Aktivitätsbereich **Designer** aus.
3. Auf der Seite **Formatdesigner** wählen Sie auf der Registerkarte **Zuordnung** **Erweitern/Reduzieren** aus.
4. Erweitern Sie die Elemente **Modell**, **Daten,** und **Transaktion**.

    Dieses EB-Format dient zum Generieren eines Lieferantentransaktionsberichts im XML-Format.

    ![Formatieren Sie Datenquellen und konfigurierte Bindungen von Formatelementen auf der Seite Format-Designer.](media/er-calculated-field-ds-performance-format.png)

5. Seite **Format-Designer** schließen.

## <a name="run-the-sample-er-solution-to-trace-execution"></a>Ausführen der EB-Beispiellösung, um Ausführung nachzuverfolgen

Stellen Sie sich vor, dass Sie das Entwerfen der ersten Version der EB-Lösung beendet haben. Jetzt möchten Sie die Lösung in Ihrer Finance-Instanz testen und die Ausführungsleistung analysieren.

### <a name="turn-on-the-er-performance-trace"></a>Aktivieren der EB-Leistungsnachverfolgung

1. Wählen Sie das Unternehmen **DEMF** aus.
2. Befolgen Sie die Schritte in [Aktivieren der EB-Leistungsverfolgung](trace-execution-er-troubleshoot-perf.md#turn-on-the-er-performance-trace), um eine Leistungsverfolgung zu generieren, während ein EB-Format ausgeführt wird.

    ![Benutzerparameter-Dialogfeld.](media/er-calculated-field-ds-performance-format-user-parameters.png)

### <a name="run-the-er-format"></a><a id="run-format"></a>Das EB-Format ausführen

1. Wechseln Sie zu **Organisationsverwaltung** \> **Elektronische Berichterstellung** \> **Konfigurationen**.
2. Auf der Seite **Konfigurationen** in der Konfigurationsstruktur wählen Sie das Element **Leistungsverbesserungsformat** aus.
3. Wählen Sie im Aktivitätsbereich auf **Ausführen**.

## <a name="use-the-performance-trace-to-analyze-model-mapping-performance"></a>Verwenden Sie die Leistungsverfolgung, um die Leistung der Modellzuordnung zu analysieren

1. Auf der Seite **Konfigurationen** in der Konfigurationsstruktur wählen Sie das Element **Leistungsverbesserungszuordnung** aus.
2. Wählen Sie im Aktivitätsbereich **Designer** aus.
3. Wählen Sie auf der Seite **Modellzuordnung** im Aktionsbereich **Designer** aus.
4. Auf der Seite **Modellzuordnungsdesigner** im Aktivitätsbereich wählen Sie **Leistungsnachverfolgung** aus.
5. Wählen Sie die zuletzt generierte Nachverfolgung aus und wählen Sie dann **OK**.

Neue Informationen sind jetzt für einige Datenquellelemente der aktuellen Modellzuordnung verfügbar:

- Tatsächlicher Zeitaufwand für das Abrufen von Daten mithilfe der Datenquelle
- Die gleiche Zeit, ausgedrückt als Prozentsatz der gesamten Zeit, die für das Ausführen der gesamten Modellzuordnung aufgewendet wurde

![Details zur Ausführungszeit auf der Seite „Modellzuordnungsdesigner“.](./media/er-calculated-field-ds-performance-mapping-2.png)

Das **Leistungsstatistik**-Raster zeigt, dass die **Trans**-Datenquelle die VendTrans-Tabelle einmal aufruft. Der Wert **\[265\]\[M: 265\]** der **Trans**-Datenquelle gibt an, dass 265 Lieferantentransaktionen aus der Anwendungstabelle abgerufen und an das Datenmodell zurückgegeben wurden.

Das **Leistungsstatistik**-Raster zeigt auch, dass die aktuelle Modellzuordnung die Datenbankanforderungen dupliziert, während die **\#Vend**-Datenquelle ausgeführt wird. Diese Verdopplung tritt aus folgenden Gründen auf:

- Die Lieferantentabelle wird für jede der 265 durchlaufenen Lieferantentransaktionen zweimal aufgerufen, was insgesamt 530 Aufrufen entspricht:

    - Ein Anruf wird getätigt, um die Lieferantenkontonummer einzugeben.
    - Ein Anruf wird getätigt, um den Lieferantennamen einzugeben.

- Die Lieferantentabelle wird für jede durchlaufene Lieferantentransaktion aufgerufen, obwohl die abgerufenen Transaktionen nur für fünf Lieferanten gebucht wurden. Von den 530 Anrufen sind 525 Duplikate. Die folgende Abbildung zeigt die Nachricht, die Sie über doppelte Aufrufe (Datenbankanforderungen) erhalten.

![Meldung zu doppelten Datenbankanforderungen auf der Seite Modellzuordnungsdesigner.](./media/er-calculated-field-ds-performance-mapping-2a.png)

Beachten Sie, dass mehr als 80 Prozent (ungefähr sechs Sekunden) der Gesamtausführungszeit für die Modellzuordnung (ca. acht Sekunden) für das Abrufen von Werten aus der VendTable-Anwendungstabelle aufgewendet wurden. Dieser Prozentsatz ist zu groß für zwei Attribute von fünf Anbietern im Vergleich zum Informationsvolumen aus der VendTrans-Anwendungstabelle.

Um die Anzahl der Anrufe zu verringern, die getätigt werden, um die Lieferantendetails für jede Transaktion abzurufen, und um die Leistung der Modellzuordnung zu verbessern, können Sie Caching für die **\#Vend**-Datenquelle verwenden.

> [!NOTE]
> Die **Trans\\\#Vend**-Datenquelle wird im Rahmen der aktuellen Transaktion der **Trans**-Datenquelle zur Laufzeit zwischengespeichert.

Durch das Zwischenspeichern der **\#Vend**-Datenquelle reduzieren die Anzahl der doppelten Anrufe von 525 auf 260, beseitigen die Duplizierung jedoch nicht vollständig. Um die Verdopplung vollständig zu vermeiden, können Sie eine neue parametrisierte Datenquelle des Typs **Berechnetes Feld** konfigurieren.

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a>Verbessern der Modellzuordnung auf der Grundlage von Informationen aus der Ausführungsnachverfolgung

### <a name="change-the-logic-of-the-model-mapping"></a>Die Logik der Modellzuordnung ändern

Befolgen Sie diese Schritte, um das Caching und eine Datenquelle des Typs **Berechnetes Feld** zu verwenden, um doppelte Aufrufe der Datenbank zu vermeiden.

1. Auf der Seite **Konfigurationen** in der Konfigurationsstruktur wählen Sie das Element **Leistungsverbesserungszuordnung** aus.
2. Wählen Sie im Aktivitätsbereich **Designer** aus.
3. Wählen Sie auf der Seite **Modellzuordnung** im Aktionsbereich **Designer** aus.
4. Befolgen Sie auf der **Modellzuordnungsdesigner**-Seite diese Schritte, um eine Datenquelle des Typs **Tabellendatensätze** hinzuzufügen, um auf Datensätze in der VendTable-Anwendungstabelle zuzugreifen:

    1. Erweitern Sie im Bereich **Datenquellentypen** den Eintrag **Dynamics 365 for Operations** und wählen Sie **Tabellendatensätze** aus.
    2. Wählen Sie **Stamm hinzufügen** aus.
    3. Geben Sie im Drop-Down-Dialogfeld im Feld **Name** **Vend** ein.
    4. Geben Sie im Feld **Tabelle** den Eintrag **VendTable** ein.
    5. Wählen Sie **OK**.

5. Sie können Aufrufe von Datenquellen des Typs **Berechnetes Feld** nur prameterisieren, wenn sich diese Datenquellen in einem Container befinden. Befolgen Sie daher diese Schritte, um eine Datenquelle des Typs **Leerer Container** hinzuzufügen, um eine neue parametrisierte Datenquelle des Typs **Berechnetes Feld** zu speichern:

    1. Erweitern Sie im Bereich **Datenquellentypen** den Eintrag **Allgemein** und wählen Sie **Leerer Container** aus.
    2. Wählen Sie **Stamm hinzufügen** aus.
    3. Geben Sie im Drop-Down-Dialogfeld im Feld **Name** **Box** ein.
    3. Wählen Sie **OK** aus.

    ![Box-Datenquelle auf der Seite „Modellzuordnungsdesigner“.](./media/er-calculated-field-ds-performance-mapping-3.png)

6. Befolgen Sie diese Schritte, um eine parametrisierte Datenquelle des Typs **Berechnetes Feld** hinzuzufügen:

    1. Wählen Sie **Box** im Bereich **Datenquellen** aus.
    2. Erweitern Sie im Bereich **Datenquellentypen** **Funktionen**, und wählen Sie **Berechnetes Feld** aus.
    3. Wählen Sie **Hinzufügen** aus.
    4. Geben Sie im Drop-Down-Dialogfeld im Feld **Name** **Vend** ein.
    5. Wählen Sie **Formel bearbeiten** aus.
    6. Wählen Sie auf der **Formeldesigner**-Seite **Parameter**, um die Parameter anzugeben, die beim Aufruf dieser Datenquelle angegeben werden müssen.
    7. Wählen Sie im Dialogfeld **Parameter** **Neu** aus.
    8. Geben Sie im Feld **Name** **parmVendAccNumber** ein.
    9. Wählen Sie im Feld **Typ** **Zeichenfolge** aus.
    10. Wählen Sie **OK**.
    11. Geben Sie im **Formel**-Feld **FIRSTORNULL(FILTER(Vend, Vend.AccountNum=parmVendAccNumber))** ein.
    12. Wählen Sie **Speichern** und schließen Sie die Seite **Formeldesginer**.
    13. Wählen Sie **OK** aus, um die neue Datenquelle hinzuzufügen.

7. Führen Sie die folgenden Schritte aus, um die hinzugefügte Datenquelle während der Ausführung als zwischengespeichert zu markieren:

    1. Wählen Sie im Bereich **Datenquellen** den Eintrag **Box\\Vend** aus.
    2. Wählen Sie **Cache** aus.

    > [!NOTE]
    > Die **Box\\Vend**-Datenquelle wird im Rahmen aller Kreditorenbuchungsseite der **Trans**-Datenquelle zur Laufzeit zwischengespeichert.

8. Befolgen Sie diese Schritte, um die verschachtelte **Trans\\\#Vend**-Datenquelle zu aktualisieren, so dass die **Box\\Vend**-Datenquelle verwendet wird:

    1. Erweitern Sie im Bereich **Datenquellen** den Eintrag **Trans**.
    2. Wählen Sie die **Trans\\\#Vend**-Datenquelle, und wählen Sie dann **Bearbeiten** \> **Formel bearbeiten**.
    3. Geben Sie auf der **Formeldesigner**-Seite im **Formel**-Feld **Box.Vend(\@.AccountNum)** ein.
    4. Wählen Sie **Speichern** und dann schließen Sie die Seite **Formeldesginer**.
    5. Wählen Sie **OK**, um Ihre Änderungen an der ausgewählten Datenquelle abzuschließen.

9. Wählen Sie **Speichern** aus.

    ![Vend-Datenquelle auf der Seite „Modellzuordnungsdesigner“.](./media/er-calculated-field-ds-performance-mapping-4.png)

10. Schließen Sie die Seite **Modellzuordnungsdesigner**.
11. Schließen Sie die Seite **Modellzuordnungen**.

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a>Die geänderte Version der EB-Modellzuordnung abschließen

1. Auf der Seite **Konfigurationen** im Inforegister **Versionen** wählen Sie die Version **1.2** der Konfiguration **Leistungsverbesserungszuordnung** aus.
2. Wählen Sie **Status ändern** \> **Abschließen** und dann **OK**.

## <a name="run-the-modified-er-solution-to-trace-execution"></a>Ausführen der geänderten EB-Lösung, um Ausführung nachzuverfolgen

Wiederholen Sie die Schritte im Abschnitt [Das EB-Format ausführen](#run-format) weiter oben in diesem Artikel, um eine neue Leistungsnachverfolgung zu generieren.

## <a name="use-the-performance-trace-to-analyze-adjustments-to-the-model-mapping"></a>Verwenden Sie die Leistungsüberwachung, um Regulierungen der Modellzuordnung zu analysieren 

1. Auf der Seite **Konfigurationen** in der Konfigurationsstruktur wählen Sie das Element **Leistungsverbesserungszuordnung** aus.
2. Wählen Sie im Aktivitätsbereich **Designer** aus.
3. Wählen Sie auf der Seite **Modellzuordnung** im Aktionsbereich **Designer** aus.
4. Auf der Seite **Modellzuordnungsdesigner** im Aktivitätsbereich wählen Sie **Leistungsnachverfolgung** aus.
5. Wählen Sie die zuletzt generierte Nachverfolgung aus und wählen Sie dann **OK**.

Beachten Sie, dass die Regulierungen, die Sie an der Modellzuordnung vorgenommen haben, doppelte Abfragen an eine Datenbank beseitigt haben. Die Anzahl der Aufrufe an Datenbanktabellen und Datenquellen für diese Modellzuordnung ist auch reduziert worden.

![Überwachungsinformationen auf der Seite „Modellzuordnungsdesigner 1“.](./media/er-calculated-field-ds-performance-mapping-5.png)

Die Gesamtausführungszeit wurde ungefähr 20 Mal reduziert (von ungefähr 8 Sekunden auf ungefähr 400 Millisekunden). Daher wurde die Leistung der gesamten EB-Lösung verbessert.

![Überwachungsinformationen auf der Seite „Modellzuordnungsdesigner 2“.](./media/er-calculated-field-ds-performance-mapping-5a.png)

## <a name="appendix-1-download-the-components-of-the-sample-microsoft-er-solution"></a><a name="appendix1"></a>Anhang 1: Laden Sie die Komponenten der Microsoft EB-Beispiellösung herunter

Sie müssen die folgenden Dateien herunterladen und lokal speichern.

| Datei                                        | Inhalt |
|---------------------------------------------|---------|
| Leistungsverbesserung model.version.1     | [Beispiel-EB-Datenmodell-Konfiguration](https://download.microsoft.com/download/4/6/f/46f0f3fa-782b-414a-8f7b-b6c64a388661/Performance_improvement_model.version.1.xml) |
| Leistungsverbesserung mapping.version.1.1 | [Beispiel-EB-Modellzuordnungskonfiguration](https://download.microsoft.com/download/8/9/1/8913a763-afb8-4bf4-aaf1-95ad793ffc5a/Performance_improvement_mapping.version.1.1.xml) |
| Leistungsverbesserung format.version.1.1  | [Beispiel-EB-Formatkonfiguration](https://download.microsoft.com/download/9/0/c/90c75963-bc78-4edc-9096-556bbe281f10/Performance_improvement_format.version.1.1.xml) |

## <a name="appendix-2-configure-the-er-framework"></a><a name="appendix2"></a>Anhang 2: Konfigurieren des EB-Frameworks

Bevor Sie das EB-Framework verwenden können, um die Leistung der Microsoft EB-Beispiellösung zu verbessern, müssen Sie den minimalen Satz von EB-Parametern konfigurieren.

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a>Parameter der elektronischen Berichterstellung konfigurieren

1. Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.
2. Wählen Sie auf der Seite **Lokalisierungskonfigurationen** im Bereich **Zugehörige Links** die Option **Parameter für elektronische Berichterstellung** aus.
3. Auf der Seite **Parameter für elektronische Berichterstellung** legen Sie auf der Registerkarte **Allgemein** die Option **Entwurfsmodus aktivieren** auf **Ja** fest.
4. Legen Sie auf der Registerkarte **Anhänge** die folgenden Parameter fest:

    - Wählen Sie im Feld **Konfigurationen** den **Dateityp** für das **DEMF**-Unternehmen aus.
    - Wählen Sie in den Feldern **Einzelvorgangsarchiv**, **Temporär**, **Grundlage** und **Andere** den **Dateityp** aus.

Weitere Informationen zu EB-Parametern finden Sie unter [Konfigurieren des EB-Frameworks](electronic-reporting-er-configure-parameters.md).

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a>Aktivieren eines EB-Konfigurationsanbieters

Jede hinzugefügte EB-Konfiguration wird als Eigentum eines EB-Konfigurationsanbieters markiert. Der EB-Konfigurationsanbieter, der im Arbeitsbereich **Elektronische Berichterstellung** aktiviert ist, wird zu diesem Zweck verwendet. Daher müssen Sie im Arbeitsbereich **Elektronische Berichterstellung** einen EB-Konfigurationsanbieter aktivieren, bevor Sie mit dem Hinzufügen oder Bearbeiten von EB-Konfigurationen beginnen.

> [!NOTE]
> Nur der Besitzer einer EB-Konfiguration kann die Konfiguration bearbeiten. Daher muss im Arbeitsbereich **Elektronische Berichterstellung** der entsprechende EB-Konfigurationsanbieter aktiviert werden, bevor eine EB-Konfigurationen bearbeitet werden kann.

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a>Überprüfen der Liste der EB-Konfigurationsanbieter

1. Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.
2. Wählen Sie auf der Seite **Lokalisierungskonfigurationen** im Bereich **Zugehörige Links** die Option **Konfigurationsanbieter** aus.
3. Auf der Seite **Konfigurationsanbietertabelle** hat jeder Anbieterdatensatz einen eindeutigen Namen und eine eindeutige URL. Überprüfen Sie den Inhalt dieser Seite. Wenn bereits ein Datensatz für **Litware, Inc.** vorhanden ist, überspringen Sie die nächste Prozedur [Hinzufügen eines neuen EB-Konfigurationsanbieters](#ActivateProvider).

#### <a name="add-a-new-er-configuration-provider"></a><a id="ActivateProvider"></a>Hinzufügen eines neuen EB-Konfigurationsanbieters

1. Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.
2. Wählen Sie auf der Seite **Lokalisierungskonfigurationen** im Bereich **Zugehörige Links** die Option **Konfigurationsanbieter** aus.
3. Wählen Sie auf der Seite **Konfigurationsanbieter** die Option **Neu** aus.
4. Geben Sie im Feld **Name** **Litware, Inc.** ein.
5. Geben Sie im Feld **Internetadresse** `https://www.litware.com` ein.
6. Wählen Sie **Speichern** aus.

#### <a name="activate-an-er-configuration-provider"></a><a id="ActivateAddedProvider"></a>Aktivieren eines EB-Konfigurationsanbieters

1. Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.
2. Wählen Sie auf der Seite **Lokalisierungskonfigurationen** im Bereich **Konfigurationsanbieter** die Kachel **Litware, Inc.** aus. Wählen Sie dann **Als aktiv festlegen** aus.

Weitere Informationen zu EB-Konfigurationsanbietern finden Sie unter [Erstellen von Konfigurationsanbietern und Markieren als aktiv](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Überblick über die elektronische Berichterstellung](general-electronic-reporting.md)
- [Überwachen der Ausführung von ER-Formaten zur Behebung von Leistungsproblemen](trace-execution-er-troubleshoot-perf.md)
- [Unterstützen parametrisierter Aufrufe von ER-Datenquellen des Typs „Berechnetes Feld“](er-calculated-field-type.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
