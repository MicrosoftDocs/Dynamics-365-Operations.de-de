---
title: ER-Formate zur Verwendung von Parametern konfigurieren, die pro juristischer Person angegeben werden
description: In diesem Artikel wird erläutert, wie Sie Elektronische Berichterstellungs(EB)-Formate konfigurieren können, um Parameter zu verwenden, die pro juristischer Person angegeben werden.
author: NickSelin
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.openlocfilehash: eb44422c4cdcc87989cdfb28dcd7d5cfea9002eb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858827"
---
# <a name="configure-er-formats-to-use-parameters-that-are-specified-per-legal-entity"></a>Konfigurieren von EB-Formaten zur Verwendung von Parametern, die pro juristischer Person angegeben werden

[!include[banner](../includes/banner.md)]

## <a name="overview"></a>Übersicht

In vielen der Elektronischen Berichterstellungs(EB)-Formate, die Sie gestalten, müssen Sie Daten mithilfe einer Gruppe von Werten filtern, die für jede juristische Person Ihrer Instanz (zum Beispiel, eine Gruppe von Steuercodes, um Steuertransaktionen zu filtern) spezifisch sind. Wenn dieser Typ momentan in einem EB-Format gefiltert wird, werden Werte, die von der juristischen Person abhängig sind (zum Beispiel Steuercodes) in Ausdrücken des EB-Formats verwendet, um Datenfilterungsregeln anzugeben. Daher wird das EB-Format an die juristischen Person angepasst. Um die erforderlichen Berichte zu erzeugen, müssen Sie abgeleitete Kopien des ursprünglichen EB-Formats für jede juristische Person erstellen, für die Sie das EB-Format ausgeführt haben. Jedes abgeleitete EB-Format muss bearbeitet werden, um Werte speziell für die juristische Person dort hinzuzufügen. Es muss umbasiert werden, sobald die ursprüngliche (Basis-)Version aktualisiert, sie aus einer Testumgebung exportiert und in eine Produktionsumgebung importiert wurde, wenn sie für die Verwendung in der Produktion bereitgestellt werden muss usw. Daher ist die Wartung dieses Typs der konfigurierten EB-Lösung aus verschiedenen Gründen komplex und zeitaufwändig:

-   Je mehr juristische Personen vorhanden sind, desto mehr EB-Formatkonfigurationen müssen verwaltet werden.
-   Die Verwaltung von EB-Konfigurationen setzt voraus, dass geschäftliche Benutzer EB-Wissen haben.

Mit der anwendungsspezifischen EB-Parameterfunktion können Poweruser die Datenenfilterung in einem EB-Format konfigurieren, damit sie auf einer Gruppe von abstrakten Regeln basiert. Diese Gruppe von Regeln kann so konfiguriert werden, dass sie die Datenquellen nutzt, die in einem EB-Format verfügbar sind. Geschäftliche Benutzer können echte Regeln über das EB-Rahmenwerk hinaus angeben, indem sie die Benutzeroberfläche, die automatisch anhand der Einstellungen des entsprechenden EB-Formats erzeugt wird, und die aktuellen Daten der juristischen Person verwenden, auf die über die Datenquellen des EB-Formats zugegriffen werden kann. Die Gruppe von Regeln, die für ein EB-Format angegeben ist, kann aus der aktuellen juristischen Person der Dynamics 365 Finance (Finance)-Instanz exportiert werden. Sie können dann in eine andere juristische Entität entweder derselben Finance-Instanz oder eine andere Instanz als Gruppe von Regeln für dasselbe EB-Format importiert werden.

## <a name="prerequisites"></a>Voraussetzungen

Um die Beispiele in diesem Artikel abzuschließen, müssen Sie für eine der folgenden Rollen Zugriff auf die Instanz der Regulatory Configuration Services (RCS) haben, der für denselben Mandanten wie Finance bereitgestellt wurde:

- Entwickler für elektronische Berichterstellung
- Funktionaler Berater für elektronische Berichterstellung
- Systemadministrator

Es wird empfohlen, dass Sie die Schritte im Artikel [Unterstützen parametrisierter Aufrufe von EB-Datenquellen des Typs BERECHNETES FELD](er-calculated-field-type.md) ausführen. Wenn Sie diese Schritte bereits abgeschlossen haben, können Sie die Schritte im Abschnitt **Importieren von EB-Konfigurationen in RCS** überspringen, der darauf folgt.

## <a name="import-er-configurations-into-rcs"></a>Importieren von EB-Konfigurationen in RCS

Laden Sie die folgenden ER-Konfigurationen herunter und speichern Sie sie lokal.

| **Inhaltsbeschreibung**                        | **Dateiname**                                        |
|------------------------------------------------|------------------------------------------------------|
| Beispiel-**EB-Datenmodell**-Konfigurationsdatei    | [Model to learn parameterized calls.version.1.xml](https://download.microsoft.com/download/2/d/b/2db913a0-3622-494e-91a2-97fc494af9b9/Modeltolearnparameterizedcalls.version.1.xml)     |
| Beispiel-**EB-Metadaten**-Konfigurationsdatei      | [Metadata to learn parameterized calls.version.1.xml](https://download.microsoft.com/download/1/b/3/1b343968-5a47-4000-b5a8-6487698ef4c0/Metadatatolearnparameterizedcalls.version.1.xml)  |
| Beispiel-**EB-Modellzuordnungs**-Konfigurationsdatei | [Mapping to learn parameterized calls.version.1.1.xml](https://download.microsoft.com/download/8/6/6/866e0ab6-2e05-4d98-9d52-d2da2038f6e4/Mappingtolearnparameterizedcalls.version.1.1.xml) |
| Beispiel-**EB-Format**-Konfiguration             | [Format to learn parameterized calls.version.1.1.xml](https://download.microsoft.com/download/e/3/9/e392eadc-b9b4-4834-95c3-b8066dd00b9c/Formattolearnparameterizedcalls.version.1.1.xml)  |

Melden Sie sich als Nächstes bei Ihrer RCS-Instanz an.

In diesem Beispiel erstellen Sie eine Konfiguration für das Beispielunternehmen Litware, Inc. Bevor Sie diese Prozedur abschließen können, müssen Sie zunächst die Schritte im RCS-Artikel [Konfigurationsanbieter erstellen und als aktiv markieren](tasks/er-configuration-provider-mark-it-active-2016-11.md) abschließen.

1.  Wählen Sie im Standard-Dashboard **Elektronische Berichterstellung** aus.
2.  Wählen Sie **Berichterstellungskonfigurationen** aus.
3.  Importieren Sie die EB-Konfigurationen, die Sie zuvor in RCS heruntergeladen haben, in der folgenden Reihenfolge: Datenmodell, Metadaten, Modellzuordnung und Format. Führen Sie für jede EB-Konfiguration die folgenden Schritte aus:

    1.  Wählen Sie **Wechselkurs** aus.
    2.  Wählen Sie **Aus XML-Datei laden** aus.
    3.  Wählen Sie **Durchsuchen** aus, um die Datei für die erforderliche EB-Konfiguration im XML-Format auszuwählen.
    4.  Wählen Sie **OK**.

## <a name="review-the-er-solution-that-is-provided"></a>Überprüfen der bereitgestellten EB-Lösung

1.  Erweitern Sie in der Konfigurationsstruktur die Inhalte des Elements **Modell zum Ermitteln parametrisierter Aufrufe**.
2.  Wählen Sie das Element **Format zum Ermitteln parametrisierter Aufrufe** aus.
3.  Wählen Sie **Designer** aus.
4.  Wählen Sie **Erweitern/Reduzieren** aus.

    Das EB-Format **Format zum Ermitteln parametrisierter Anrufe** ist so gestaltet, dass ein Steuerauszug im XML-Format erzeugt wird, der verschiedene Besteuerungsstufen (regulär, reduziert und keine) enthält. Jede Stufe hat eine andere Anzahl von Details.

    ![Mehrere Ebenen des EB-Formats, Format zum Erlernen parametrisierter Anrufe.](./media/RCS-AppSpecParms-ReviewFormat.PNG)

5.  Erweitern Sie auf der Registerkarte **Zuordnung** die Elemente **Modell**, **Daten** und **Zusammenfassung**.

    Die Datenquelle **Model.Data.Summary** gibt die Liste der Steuertransaktionen zurück. Diese Transaktionen werden anhand des Steuercodes zusammengefasst. Für diese Datenquelle wurde das berechnete Feld **Model.Data.Summary.Level** so konfiguriert, dass es den Code für die Besteuerungsstufe jedes zusammengefassten Datensatzes zurückgibt. Für jeden Steuercode, der zur Laufzeit aus der Datenquelle **Model.Data.Summary** abgerufen werden kann, gibt das berechnete Feld den Besteuerungsstufencode (**Regulär**, **Reduziert**, **Keine** oder **Sonstige**) als Textwert zurück. Das berechnete Feld **Model.Data.Summary.Level** wird verwendet, um Datensätze der Datenquelle **Model.Data.Summary** zu filtern, und geben Sie die gefilterten Daten in jedes XML-Element ein, das eine Besteuerungsstufe darstellt, indem Sie die Felder **Model.Data2.Level1**, **Model.Data2.Level2** und **Model.Data2.Level3** verwenden.

    ![Die Model.Data.Summary-Datenquellenliste der Steuertransaktionen.](./media/RCS-AppSpecParms-ReviewFormat-Data2Fld.PNG)

    Das berechnete Feld **Model.Data.Summary.Level** wurde so konfiguriert, dass es einen EB-Ausdruck enthält. Steuercodes (**VAT19**, **InVAT19**, **VAT7**, **InVAT7**, **THIRD** und **InVAT0**) sind in dieser Konfiguration hartcodiert. Daher hängt dieses EB-Format von der juristischen Person ab, in der diese Steuercodes konfiguriert wurden.

    ![Das berechnete Feld Model.Data.Summary.Level mit fest codierten Steuercodes.](./media/RCS-AppSpecParms-ReviewFormat-LevelFld.PNG)

    Um einen andere Gruppe von Steuercodes für die einzelnen juristischen Person zu unterstützen, müssen die folgenden Schritte ausgeführt werden:

    - Erstellen Sie eine abgeleitete Version des EB-Formats für jede juristische Person.
    - Aktualisieren Sie die Steuercodes im berechneten Feld **Model.Data.Summary.Level** basierend auf den Einstellungen für die juristische Person.

6.  Seite **Format-Designer** schließen.

## <a name="create-a-derived-format"></a>Erstellen eines abgeleiteten Formats

Verwenden Sie als Nächstes die anwendungsspezifische EB-Parameterfunktion, um eine andere Gruppe von Steuercodes für jede juristische Person in einem einzelnen EB-Format zu unterstützen.

1.  Erweitern Sie in der Konfigurationsstruktur die Inhalte des Elements **Modell zum Ermitteln parametrisierter Aufrufe**.
2.  Wählen Sie das Element **Format zum Ermitteln parametrisierter Aufrufe** aus.
3.  Wählen Sie **Konfiguration erstellen**.
4.  Wählen Sie die Option **Von Name ableiten: Formatieren zum Ermitteln parametrisierter Aufrufe, Microsoft** aus.
5.  Geben Sie im Feld **Name** **Format zum Ermitteln der Vorgehensweise bei der Suche von Daten zu juristischen Personen** ein.
6.  Wählen Sie **Konfiguration erstellen**.

## <a name="configure-a-derived-format"></a>Konfigurieren eines abgeleiteten Formats

### <a name="add-a-format-enumeration"></a>Hinzufügen einer Formatenumeration

Danach fügen Sie eine neue EB-Formatenumeration hinzu. Die Werte dieser Formatenumeration werden geschäftlichen Benutzern dargestellt, die für die verschiedenen Besteuerungsstufen, die im EB-Format verwendet werden, Gruppen von Steuercodes angeben, die von der juristischen Person abhängig sind.

1.  Wählen Sie **Designer** aus.
2.  Wählen Sie **Formatenumerationen** aus.
3.  Wählen Sie **Hinzufügen** aus.
4.  Geben Sie im Feld **Name** **Liste der Besteuerungsstufen** ein.
5.  Wählen Sie **Speichern**.
6.  Wählen Sie auf der Registerkarte **Formatenumerationswerte** die Option **Hinzufügen** aus.
7.  Geben Sie im Feld **Name** **Reguläre Besteuerung** ein.
8.  Wählen Sie erneut **Hinzufügen** aus.
9.  Geben Sie im Feld **Name** **Reduzierte Besteuerung** ein.
10. Wählen Sie erneut **Hinzufügen** aus.
11. Geben Sie im Feld **Name** **Keine Besteuerung** ein.
12. Wählen Sie erneut **Hinzufügen** aus.
13. Geben Sie im Feld **Name** **Sonstige** ein.

    ![Neuer Datensatz auf der Seite „Formatenumerationen“.](./media/RCS-AppSpecParms-ConfigureFormat-Enum.PNG)

    Da die geschäftlichen Benutzer möglicherweise unterschiedliche Sprachen verwenden, um Gruppen von Steuercodes anzugeben, die von der juristischen Person abhängig sind, empfiehlt es sich, die Werte dieser Enumeration in die Sprachen zu übersetzen, die als bevorzugte Sprachen für diese Benutzer in Finance konfiguriert werden.

14. Wählen Sie den Datensatz **Keine Besteuerung** aus.
15. Klicken Sie in das Feld **Label**.
16. Wählen Sie **Übersetzen** aus.
17. Geben Sie im Bereich **Textübersetzung** im Feld **Beschriftungskennung** **LBL_LEVELENUM_NO** ein.
18. Geben Sie im Feld **Text in Standardsprache** **Keine Besteuerung** ein.
19. Wählen Sie im Feld **Sprache** **DE** aus.
20. Geben Sie im Feld **Übersetzter Text** **Keine Besteuerung** ein.
21. Wählen Sie **Übersetzen** aus.

    ![Textübersetzungsauszug.](./media/RCS-AppSpecParms-ConfigureFormat-EnumTranslate.PNG)

22. Wählen Sie **Speichern** aus.
23. Schließen Sie die Seite **Formatenumerationen**.

### <a name="add-a-new-lookup-data-source"></a>Hinzufügen einer neuen Datenquelle für die Suche

Danach fügen Sie eine neue Datenquelle hinzu, um anzugeben, wie geschäftliche Benutzer Regeln angeben, die von der juristischen Person abhängig sind, um die korrekte Besteuerungsstufe für jeden zusammengefassten Transaktionsdatensatz zu erkennen.

1.  Wählen Sie auf der Registerkarte **Zuordnung** die Option **Hinzufügen** aus.
2.  Wählen Sie **Formatenumeration\Suche** aus.

    Sie haben gerade ermittelt, dass jede Regel, die geschäftliche Benutzer für die Erkennung der Besteuerungsstufe angeben, einen Wert einer EB-Formatenumeration zurückgibt. Beachten Sie, dass der Datenquellentyp **Suche** über **Datenmodell** und **Dynamics 365 for Operations**-Blöcke sowie den Block **Formatenumeration** aufgerufen werden kann. Daher können EB-Datenmodellenumerationen und Anwendungsenumerationen verwendet werden, um den Typ der Werte anzugeben, der für Datenquellen dieses Typs zurückgegeben wird. Mehr über **Such**-Datenquellen finden Sie in [Suchdatenquellen für die Verwendung anwendungsspezifischer EB-Parameter konfigurieren](er-lookup-data-sources.md).
    
3.  Geben Sie im Feld **Name** **Auswahl** ein.
4.  Wählen Sie im Feld **Formatenumeration** die Option **Liste der Besteuerungsstufen** ein.

    Sie haben angegeben, dass geschäftliche Benutzer für jede in dieser Datenquelle angegebene Regel einen der Werte der Formatenumeration **Liste der Besteuerungsstufen** als zurückgegebenen Wert auswählen müssen.
    
5.  Wählen Sie **Suche bearbeiten** aus.
6.  Wählen Sie **Spalten** aus.
7.  Erweitern Sie das Element **Model**.
8.  Erweitern Sie das Element **Daten**.
9.  Erweitern Sie das Element **Steuer**.
10. Wählen Sie das Element **Model.Data.Tax.Code** aus.
11. Wählen Sie die Schaltfläche **Hinzufügen** (rechter Pfeil) aus.

    ![Spaltenauszug.](./media/RCS-AppSpecParms-ConfigureFormat-Lookup1.PNG)

    Sie haben gerade angegeben, dass geschäftliche Benutzer für jede in dieser Datenquelle für die Erkennung der Besteuerungsstufe angegebene Regel einen der Steuercodes als Bedingung auswählen müssen. Die Liste der Steuercodes, die geschäftliche Benutzer auswählen können, wird von der Datenquelle **Model.Data.Tax** zurückgegeben. Da diese Datenquelle das Feld **Name** enthält, wird der Name des Steuercodes für jeden Steuercodewert in der Suche angezeigt, der dem geschäftlichen Benutzer angezeigt wird.
    
12. Wählen Sie **OK** aus.

    ![Such-Designer-Seite.](./media/RCS-AppSpecParms-ConfigureFormat-Lookup2.PNG)

    Geschäftliche Benutzer können mehrere Regeln als Datensätze dieser Datenquelle hinzufügen. Jeder Datensatz wird mithilfe eines Positionscodes nummeriert. Regeln werden mit zunehmender Positionsnummer ausgewertet.

    Da Sie das Feld **Steuercode** als Bedingung für Regeln in dieser Suchdatenquelle ausgewählt haben und **Steuercode** als Feld des Datentyps **Zeichenfolge** eingerichtet ist, wird jede Regel während der Laufzeit ausgewertet, indem der Steuercode, der an die Datenquelle übergeben wird, mit dem Steuercode verglichen wird, der in diesem Datensatz der Datenquelle definiert wird.

    Wenn eine Regel, die die konfigurierte Bedingung erfüllt, gefunden wird, gibt diese Datenquelle den Suchwert der Regel zurück, die im Feld **Suchenergebnis** definiert ist. Wenn keine Regel gefunden wird, wird eine Ausnahme ausgelöst, um den Benutzer zu informieren, dass die aktuelle Datenquelle keinen korrekten Wert zurückgegeben kann.

13. Wählen Sie **Speichern**.
14. Schließen Sie die Seite **Such-Designer**.
15. Wählen Sie **OK**.

    Beachten Sie, dass Sie eine neue Datenquelle hinzugefügt haben, die die Besteuerungsstufe als Wert der Formatenumeration **Liste der Besteuerungsstufen** für jeden Steuercode zurückgibt, der an die Datenquelle als Argument des Parameters **Code** des Datentyps **Zeichenfolge** weitergegeben wird.
    
    ![Format-Designer-Seite mit einer neuen Datenquelle.](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFld.PNG)

    Die Bewertung hängt von konfigurierten Regeln vom Datentyp der Felder ab, die ausgewählt wurden, um die Bedingungen dieser Regeln zu definieren. Wenn Sie ein Feld auswählen, das als Feld des Datentyps **Numerisch** oder **Datum** konfiguriert wird, weichen die Kriterien von den Kriterien ab, die zuvor für den Datentyp **Zeichenfolge** beschrieben wurden. Für die Felder **Numerisch** und **Datum** muss die Regel als Wertebereich angegeben werden. Die Bedingung der Regel wird dann als erfüllt angesehen, wenn ein Wert, der an die Datenquelle weitergegeben wird, sich im konfigurierten Bereich befindet.
    
    Die folgende Abbildung zeigt ein Beispiel für diesen Einrichtungstyp. Zusätzlich zu dem Feld **Model.Data.Tax.Code** des Datentyps **Zeichenfolge** wird das Feld **Model.Tax.Summary.Base** des Datentyps **Gleitkommazahl** verwendet, um die Bedingungen für eine Suchendatenquelle anzugeben.
    
    ![Such-Designer-Seite mit zusätzlichen Spalten.](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFld2.PNG)

    Da die Felder **Model.Data.Tax.Code** und **Model.Tax.Summary.Base** für diese Suchendatenquelle ausgewählt werden, wird jede Regel diese Datenquelle folgendermaßen konfiguriert:
    
    -   In der angezeigten Liste muss der Wert der Formatenumeration **Liste der Besteuerungsstufen** als zurückgegebener Wert ausgewählt werden.
    -   Der Steuercode muss als Bedingung dieser Regel eingegeben werden. Nur Steuercodes, die von der Datenquelle **Model.Data.Tax** bereitgestellt werden, sind verfügbar.
    -   Mindest- und Höchstwerte des Steuergrundlagebetrags müssen als Bedingungen dieser Regel eingegeben werden.

    So wird jede Regel dieser Datenquelle während der Laufzeit ausgewertet:
    -   Entspricht der Code des Datentyps **Zeichenfolge**, der an diese Datenquelle weitergegeben wurde, dem Steuercode einer Regel?
    -   Fällt der Wert des Datentyps **Gleitkommazahl**, der an diese Datenquelle weitergegeben wurde, zwischen bestimmte Mindest- und Höchstwerte?

    Eine Regel gilt als anwendbar, wenn beide Bedingungen erfüllt sind.

### <a name="translate-the-label-of-the-lookup-data-source-that-was-added"></a>Übersetzen der Bezeichnung der Suchendatenquelle, die hinzugefügt wurde

Da die geschäftlichen Benutzer möglicherweise unterschiedliche Sprachen verwenden, um Gruppen von Steuercodes anzugeben, die von der juristischen Person abhängig sind, empfiehlt es sich, die Bezeichnung jeder Suchdatenquelle zu übersetzen, die Sie hinzufügen, damit sie in der bevorzugten Sprache auf der entsprechenden Seite jedes Benutzers angezeigt wird.

1.  Wählen Sie die Datenquelle **Model.Data.Selector** aus.
2.  Wählen Sie **Bearbeiten** aus.
3.  Klicken Sie in das Feld **Label**.
4.  Wählen Sie **Übersetzen** aus.
5.  Geben Sie im Bereich **Textübersetzung** im Feld **Beschriftungskennung** **LBL_SELECTOR_DS** ein.
6.  Geben Sie im Feld **Text in Standardsprache** **Steuerstufe anhand des Steuercodes auswählen** ein.
7.  Wählen Sie im Feld **Sprache** **DE** aus.
8.  Geben Sie im Feld **Übersetzter Text** **Steuerebene für Steuerkennzeichen auswählen** ein.
9.  Wählen Sie **Übersetzen** aus.
10. Wählen Sie **OK** aus.

    ![Datenquelleneigenschaften-Auszug.](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFldTranslate.PNG)

### <a name="add-a-new-field-to-consume-the-configured-lookup"></a>Hinzufügen eines neues Felds, um die konfigurierte Suche zu verarbeiten

1.  Erweitern Sie das Element **Model.Data**.
2.  Wählen Sie das Element **Model.Data.Summary** aus.
3.  Wählen Sie **Hinzufügen** aus.
4.  Wählen Sie das **Feld „Funktionen/Berechnet“** aus.
5.  Geben Sie im Feld **Name** **LevelByLookup** ein.
6.  Wählen Sie **Formel bearbeiten** aus.
7.  Geben Sie im **Formularfeld** **Model.Selector(Model.Data.Summary.Code)** ein.
8.  Wählen Sie **Speichern** aus.

    ![Hinzufügen von Model.Selector(Model.Data.Summary.Code) zur Formel-Designer-Seite.](./media/RCS-AppSpecParms-ConfigureFormat-AddLevelByLookupFld.PNG)

9.  Schließen Sie die Seite **Formel-Editor**.
10. Wählen Sie **OK** aus.

    ![Format-Designer-Seite mit neuer hinzugefügter Formel.](./media/RCS-AppSpecParms-ConfigureFormat-AddLevelByLookupFld2.PNG)

    Beachten Sie, dass das berechnete Feld **LevelByLookup**, das Sie hinzugefügt haben, die Besteuerungsstufe als Wert der Formatenumeration **Liste der Besteuerungsstufen** für jeden zusammengefassten Steuertransaktionsdatensatz zurückgibt. Der Steuercode des Datensatzes wird an die Suchdatenquelle **Model.Selector** weitergegeben, und die Gruppe von Regeln für diese Datenquelle wird verwendet, um die korrekte Besteuerungsstufe auszuwählen.

### <a name="add-a-new-format-enumeration-based-data-source"></a>Hinzufügen einer neuen Datenquelle, die auf einer Formatenumeration basiert

Danach fügen Sie eine neue Datenquelle hinzu, die auf die Formatenumeration verweist, die Sie zuvor hinzugefügt haben. Werte dieser Datenquelle werden später in einem EB-Formatausdruck verwendet.

1.  Wählen Sie **Stamm hinzufügen** aus.
2.  Wählen Sie **Formatenumerationen\Enumeration** aus.
3.  Geben Sie im Feld **Name** **TaxationLevel** ein.
4.  Wählen Sie im Feld **Formatenumeration** die Option **Liste der Besteuerungsstufen** ein.
5.  Wählen Sie **Speichern**.

### <a name="modify-an-existing-field-to-start-to-use-the-lookup"></a>Ändern eines vorhandenen Felds, um mit der Verwendung der Suche zu beginnen

Danach ändern Sie das vorhandene berechnete Feld, sodass es die konfigurierte Suchendatenquelle verwendet, um je nach Steuercode den korrekten Besteuerungsstufenwert zurückzugeben.

1.  Wählen Sie das Element **Model.Data.Summary.Level** aus.
2.  Wählen Sie **Bearbeiten** aus.
3.  Wählen Sie **Formel bearbeiten** aus.

    Beachten Sie, dass der aktuelle Ausdruck des Felds **Model.Data.Summary.Level** die folgenden hartcodierten Steuercodes enthält:
    
    CASE (@.Code, „VAT19“, „Regulär“, „InVAT19“, „Regulär“, „VAT7“, „Reduziert“, „InVAT7“, „Reduziert“, „THIRD“, „Keine“, „InVAT0“, „Keine“, „Sonstige“)

4.  Geben Sie im Feld **Formel** **CASE(@.LevelByLookup, TaxationLevel.'Reguläre Besteuerung', „Regulär“, TaxationLevel.'Reduzierte Besteuerung', „Reduziert“, TaxationLevel.'Keine Besteuerung', „Keine“, „Sonstige“)**.

    ![Seite für EB-Arbeitsgangdesigner.](./media/RCS-AppSpecParms-ConfigureFormat-ChangeLookupFld.PNG)
    
    Beachten Sie, dass der Ausdruck des Felds **Model.Data.Summary.Level** jetzt die Besteuerungsstufe zurückgibt, die auf dem Steuercode des aktuellen Datensatzes und der Gruppe von Regeln basiert, die ein geschäftlicher Benutzer in der Suchdatenquelle **Model.Data.Selector** konfiguriert.
    
5.  Wählen Sie **Speichern**.
6.  Schließen Sie die Seite **Formeldesigner**.
7.  Wählen Sie **OK**.
8.  Wählen Sie **Speichern**.
9.  Seite **Format-Designer** schließen.

## <a name="complete-the-draft-version-of-a-derived-format"></a>Abschließen der Entwurfsversion eines abgeleiteten Formats

1.  Wählen Sie im Inforegister **Versionen** **Status ändern** aus.
2.  Wählen Sie **Abgeschlossen** aus.
3.  Wählen Sie **OK**.

## <a name="export-completed-version-of-modified-format"></a>Exportieren der abgeschlossenen Version eines bearbeiteten Formats

1.  Wählen Sie in der Konfigurationsstruktur das Element **Format zum Ermitteln der Vorgehensweise bei der Suche von Daten zu juristischen Personen** aus.
2.  Wählen Sie im Inforegister **Versionen** den Datensatz mit dem Status **Abgeschlossen** aus.
3.  Wählen Sie **Wechselkurs** aus.
4.  Wählen Sie **Als XML-Datei exportieren** aus.
5.  Wählen Sie **OK**.
6.  Der Webbrowser lädt eine XML-Datei **Format zum Ermitteln der Vorgehensweise bei der Suche von Daten zu juristischen Personen** herunter. Speichern Sie die Datei lokal.

Wiederholen Sie die Schritte in diesem Abschnitt für übergeordnete Elemente des Formats **Format zum Ermitteln der Vorgehensweise bei der Suche von Daten zu juristischen Personen** und speichern Sie die folgenden Dateien lokal:

-   Format zum Ermitteln parametrisierter Anrufe.xml
-   Zuordnung zum Ermitteln parametrisierter Aufrufe.xml
-   Modell zum Lernern parametrisierter Aufrufe.xml

Um mehr darüber zu erfahren, wie Sie das konfigurierte EB-Format **Format zum Ermitteln der Vorgehensweise bei der Suche von Daten zu juristischen Personen** für die Einrichtung von Gruppen von Steuercodes verwenden, die von juristischen Personen abhängen, um Steuertransaktionen anhand von unterschiedlichen Besteuerungsstufen zu filtern, führen Sie die Schritte im Artikel [Parameter eines EB-Formats pro juristischer Person einrichten](er-app-specific-parameters-set-up.md) aus.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Formeldesigner in der elektronischen Berichterstellung](general-electronic-reporting-formula-designer.md)

[Parameter eines ER-Formats pro juristischer Person einrichten](er-app-specific-parameters-set-up.md)

[Suchdatenquellen für die Funktion zur Verwendung anwendungsspezifischer EB-Parameter konfigurieren](er-lookup-data-sources.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
