---
title: Einrichten von Parametern eines EB-Formats pro juristischer Person
description: In diesem Thema wird erläutert, wie Sie die Parameter eines Elektronische Berichterstellungs(EB)-Formats pro juristischer Entität konfigurieren können.
author: NickSelin
manager: AnnBe
ms.date: 10/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: b51a7ae8587a3cbb65efc4af574929efcbc8fbf8
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681471"
---
# <a name="set-up-the-parameters-of-an-er-format-per-legal-entity"></a>Einrichten von Parametern eines EB-Formats pro juristischer Person

[!include[banner](../includes/banner.md)]

## <a name="prerequisites"></a>Voraussetzungen

Um diese Schritte auszuführen, müssen Sie zuerst die Schritte im Thema [Konfigurieren von EB-Formaten zur Verwendung von Parametern, die pro juristischer Person angegeben werden](er-app-specific-parameters-configure-format.md) ausführen.

Um die Beispiele in diesem Thema abzuschließen, müssen Sie für eine der folgenden Rollen Zugriff auf Microsoft Dynamics 365 Finance (Finance) haben:

- Entwickler für elektronische Berichterstellung
- Funktionaler Berater für elektronische Berichterstellung
- Systemadministrator

## <a name="import-er-configurations"></a>ER Konfigurationen importieren

1.  Melden Sie sich in Ihrer Umgebung an.
2.  Wählen Sie im Standard-Dashboard **Elektronische Berichterstellung** aus.
3.  Wählen Sie **Berichterstellungskonfigurationen** aus.
4.  Importieren Sie die Konfigurationen, die Sie während der Ausführung der Schritte im Thema [Konfigurieren von EB-Formaten zur Verwendung von Parametern, die pro juristischer Person angegeben werden](er-app-specific-parameters-configure-format.md) aus Regulatory Configuration Service (RCS) exportiert haben, in die aktuelle Instanz von Finance. Führen Sie diese Schritte für jede Konfiguration der elektronischen Berichterstellung (EB) in der folgenden Reihenfolge aus: Datenmodell, Modellzuordnung und Formate.

    1. Wählen Sie **Austausch \> Aus XML-Datei laden** aus.
    2. Wählen Sie **Durchsuchen** aus, um die Datei für die erforderliche EB-Konfiguration im XML-Format auszuwählen.
    3. Wählen Sie **OK**.
    
    Die folgende Abbildung zeigt die Konfigurationen, die Sie haben müssen, wenn Sie fertig sind.

    ![ER-Konfigurationsseite](./media/GER-AppSpecParms-ImportedConfigurations.PNG)

## <a name="set-up-parameters-for-the-demf-company"></a>Einrichten von Parametern für das DEMF-Unternehmen

Sie können das EB-Framework verwenden, um anwendungsspezifische Parameter für ein EB-Format einzurichten.

1.  Wählen Sie die juristische Person **DEMF** aus.
2.  Wählen Sie in der Konfigurationsstruktur das Format **Format zum Ermitteln der Vorgehensweise bei der Suche von Daten zu juristischen Personen** aus.
3.  Wählen Sie im Aktivitätsbereich auf der Registerkarte **Konfigurationen** in der Gruppe **Anwendungsspezifische Parameter** die Option **Einrichten** aus.

    ![Seite für anwendungsspezifische EB-Parameter](./media/GER-AppSpecParms-LookupForm.PNG)
    
    Auf der Seite **Anwendungsspezifische Parameter** können Sie die Regeln für die Datenquelle **Auswahl** des Formats **Format zum Ermitteln der Vorgehensweise bei der Suche von Daten zu juristischen Personen** konfigurieren.
    
    Wenn das Basis-EB-Format mehrere Datenquellen des Typs **Suche** enthält, müssen Sie die gewünschte Datenquelle im Inforegister **Suchen** auswählen, bevor Sie beginnen können, die Gruppe von Regeln für die Datenquelle zu konfigurieren.
    
    Für jede Datenquelle können Sie separate Regeln für jede Version des ausgewählten EB-Formats konfigurieren.
    
    Die gesamten Regeln für alle Suchendatenquellen, die in der ausgewählten Version des Basis-EB-Formats zur Verfügung stehen, stellen die anwendungsspezifischen Parameter für das EB-Format dar.

4.  Wählen Sie Version **1.1.1** des EB-Formats aus.
5.  Auf dem Inforegister **Bedingungen** wählen Sie **Hinzufügen** aus.
6.  Wählen Sie im Feld **Code** des neuen Datensatzes den Dropdown-Pfeil aus, um die Suche zu öffnen.

    Die Suche zeigt die Liste der Steuercodes für die Auswahl an. Diese Liste wird durch die Datenquelle **Model.Data.Tax** zurückgegeben, die im Basis-EB-Format konfiguriert wurde. Da diese Datenquelle das Feld **Name** enthält, wird der Name jedes Steuercodes in der Suche angezeigt.

    ![Seite für anwendungsspezifische EB-Parameter](./media/GER-AppSpecParms-LookupForm-CodeFldPicker.PNG)
    
7.  Wählen Sie den Steuercode **VAT19** aus.
8.  Wählen Sie im Feld **Suchergebnis** des neuen Datensatzes den Dropdown-Pfeil aus, um die Suche zu öffnen. Die Suche zeigt die Liste der Werte für die TaxationLevel-Formatenumeration zur Auswahl an.

    Hinweis: Wenn Deutsch als bevorzugte Sprache des Benutzers ausgewählt wird, als der Sie angemeldet sind, werden die Beschriftungen der Werte in der Suche auf Deutsch angezeigt, sofern sie im Basis-EB-Format übersetzt wurden. Darüber hinaus erscheint die Beschriftung in der bevorzugten Sprache des Benutzers auf der Registerkarte **Suchen**, wennn die Beschriftung einer Suchendatenquelle übersetzt wurde.

    ![Seite für anwendungsspezifische EB-Parameter](./media/GER-AppSpecParms-LookupForm-LookupFldPicker.PNG)

9.  Wählen Sie den Wert **Reguläre Besteuerung** aus.

    Wenn Sie diesen Datensatz hinzufügen, legen Sie die folgende Regel fest: Sobald die Suchendatenquelle **Auswahl** angefordert wird und der Steuercode **VAT19** als Argument weitergegeben wird, wird **Reguläre Besteuerung** als erforderliche Besteuerungsstufe zurückgegeben.

10. Wählen Sie **Hinzufügen** aus und führen Sie die folgenden Schritte aus:

    1. Wählen Sie im Feld **Code** den Steuercode **InVAT19** aus.
    2. Wählen Sie im Feld **Suchergebnis** den Wert **Reguläre Besteuerung** aus.
    
11. Wählen Sie erneut **Hinzufügen** aus und führen Sie die folgenden Schritte aus:

    1. Wählen Sie im Feld **Code** den Steuercode **VAT7** aus.
    2. Wählen Sie im Feld **Suchergebnis** den Wert **Reduzierte Besteuerung** aus.
    
12. Wählen Sie erneut **Hinzufügen** aus und führen Sie die folgenden Schritte aus:

    1. Wählen Sie im Feld **Code** den Steuercode **InVAT7** aus.
    2. Wählen Sie im Feld **Suchergebnis** den Wert **Reduzierte Besteuerung** aus.
    
13. Wählen Sie erneut **Hinzufügen** aus und führen Sie die folgenden Schritte aus:

    1. Wählen Sie im Feld **Code** den Steuercode **THIRD** aus.
    2. Wählen Sie im Feld **Suchergebnis** den Wert **Keine Besteuerung** aus.
    
14. Wählen Sie erneut **Hinzufügen** aus und führen Sie die folgenden Schritte aus:

    1. Wählen Sie im Feld **Code** den Steuercode **InVAT0** aus.
    2. Wählen Sie im Feld **Suchergebnis** den Wert **Keine Besteuerung** aus.
    
15. Wählen Sie erneut **Hinzufügen** aus und führen Sie die folgenden Schritte aus:

    1. Wählen Sie im Feld **Code** die Option **\*Nicht leer\*** aus.
    2. Wählen Sie im Feld **Suchergebnis** den Wert **Sonstige** aus.
    
    Wenn Sie diesen letzten Datensatz hinzufügen, legen Sie die folgende Regel fest: Sobald der Steuercode, der als Argument weitergegeben wird, keine der vorherigen Regeln erfüllt, gibt die Suchdatenquelle **Sonstige** als erforderliche Besteuerungsstufe zurück.

    ![Seite für anwendungsspezifische EB-Parameter](./media/GER-AppSpecParms-LookupForm-RulesSet.PNG)
    
16. Wählen Sie im Feld **Status** die Option **Abgeschlossen** aus.

    Wenn Sie eine EB-Formatversion ausführen, die entweder über den Status **Abgeschlossen** oder **Geteilt** verfügt, muss diese Gruppe von Regeln im Status **Abgeschlossen** sein. Andernfalls wird Ausführung des Basis-EB-Formats unterbrochen, wenn das Format versucht, Daten aus dieser Gruppe von Regeln zu laden, während die Suchdatenquelle **Auswahl** ausgeführt wird.
    
    Wenn Sie eine EB-Formatversion ausführen, die den Status **Entwurf** hat, kann das Basis-EB-Format unabhängig von deren Status auf diese Gruppe von Regeln zugreifen.
    
17. Wählen Sie **Speichern**.
18. Schließen Sie die Seite **Anwendungsspezifische Parameter**.

## <a name="run-the-er-format-in-the-demf-company"></a>Ausführen des EB-Formats im Unternehmen DEMF

1.  Wählen Sie in der Konfigurationsstruktur das Format **Format zum Ermitteln der Vorgehensweise bei der Suche von Daten zu juristischen Personen** aus.
2.  Wählen Sie im Aktivitätsbereich auf **Ausführen**.
3.  Im angezeigten Dialogfeld wählen Sie **OK** aus.
4.  Laden Sie den erzeugten Auszug herunter und speichern Sie ihn lokal.

    Beachten Sie, dass im generierten Auszug die Zusammenfassung des Steuercodes **InVAT7** auf die Ebene **Reduziert** festgelegt wurde, und Zusammenfassungen der Steuercodes **VAT19** und **InVA19** auf die Ebene **Regulär** festgelegt wurden. Dieses Verhalten wird von der Konfiguration in der Gruppe von Regeln bestimmt, die von juristischen Entitäten abhängen.
    
5.  Gehen Sie zu **Steuer \> Indirekte Steuern \> Mehrwertsteuer \> Mehrwertsteuercodes**.
6.  Wählen Sie den Steuercode **InVAT7** aus.
7.  Wählen Sie im Aktivitätsbereich auf der Registerkarte **Mehrwertsteuercode** in der Gruppe **Abfragen** die Option **Gebuchte Mehrwertsteuer** aus, um Informationen zum Steuerwert und dem angewendeten Steuersatz pro Steuercode anzuzeigen.

    ![Veröffentlichte Umsatzsteuer-Seite](./media/GER-AppSpecParms-Statement.PNG)

8.  Schließen Sie die Seite „Gebuchte Mehrwertsteuer“.

## <a name="set-up-parameters-for-the-usmf-company"></a>Einrichten von Parametern für das USMF-Unternehmen

1.  Wählen Sie die juristische Person **USMF** aus.
2.  Wechseln Sie zu **Organisationsverwaltung \> Elektronische Berichterstellung \> Konfigurationen**.
3.  Erweitern Sie in der Konfigurationsstruktur das Element **Modell zum Lernern parametrisierter Aufrufe**, erweitern Sie das Element **Format zum Ermitteln parametrisierter Anrufe**, und wählen Sie das Format **Format zum Ermitteln der Vorgehensweise bei der Suche von Daten zu juristischen Personen** aus.
4.  Wählen Sie im Aktivitätsbereich auf der Registerkarte **Konfigurationen** in der Gruppe **Anwendungsspezifische Parameter** die Option **Einrichten** aus.
5.  Wählen Sie Version **1.1.1** des ausgewählten EB-Formats aus.
6.  Auf dem Inforegister **Bedingungen** wählen Sie **Hinzufügen** aus.
7.  Wählen Sie im Feld **Code** des neuen Datensatzes den Dropdown-Pfeil aus, um die Suche zu öffnen.

    Die Suche zeigt nun die Liste der Steuercodes für die Steuer des **USMF**-Unternehmens zur Auswahl an.

    ![Seite für anwendungsspezifische EB-Parameter](./media/GER-AppSpecParms-LookupForm-CodeFldPicker2.PNG)
    
8.  Wählen Sie den Steuercode **BEFREIT** aus.
9.  Wählen Sie im Feld **Suchergebnis** des neuen Datensatzes den Wert **Keine Besteuerung** aus.
10. Wählen Sie erneut **Hinzufügen** aus.
11. Wählen Sie im Feld **Code** des neuen Datensatzes die Option **\*Nicht leer\*** aus.
12. Wählen Sie im Feld **Suchergebnis** des neuen Datensatzes den Wert **Reguläre Besteuerung** aus.
13. Wählen Sie im Feld **Status** die Option **Abgeschlossen** aus.
14. Wählen Sie **Speichern**.

    ![Seite für anwendungsspezifische EB-Parameter](./media/GER-AppSpecParms-LookupForm-RulesSet2.PNG)
    
15. Schließen Sie die Seite **Anwendungsspezifische Parameter**.

## <a name="run-the-er-format-in-the-usmf-company"></a>Ausführen des EB-Formats im Unternehmen USMF

1.  Wählen Sie in der Konfigurationsstruktur das Format **Format zum Ermitteln der Vorgehensweise bei der Suche von Daten zu juristischen Personen** aus.
2.  Wählen Sie im Aktivitätsbereich auf **Ausführen**.
3.  Im angezeigten Dialogfeld wählen Sie **OK** aus.
4.  Laden Sie den erzeugten Auszug herunter und speichern Sie ihn lokal.

    Beachten Sie, dass Sie nun im generierten Auszug dasselbe EB-Format wieder für eine andere juristische Person verwendet haben, ohne jedoch Änderungen am EB-Format vorzunehmen.

## <a name="reuse-legal-entitydependent-parameters"></a>Wiederverwenden von Parametern, die von juristischen Personen abhängen

### <a name="export-parameters"></a>Exportieren von Parametern

1.  Wechseln Sie zu **Organisationsverwaltung  \>Arbeitsbereiche \>  Elektronische Berichterstellung**.
2.  Wählen Sie **Berichterstellungskonfigurationen** aus.
3.  Wählen Sie in der Konfigurationsstruktur das Format **Format zum Ermitteln der Vorgehensweise bei der Suche von Daten zu juristischen Personen** aus.
4.  Wählen Sie im Aktivitätsbereich auf der Registerkarte **Konfigurationen** in der Gruppe **Anwendungsspezifische Parameter** die Option **Einrichten** aus.
5.  Wählen Sie Version **1.1.1** des EB-Formats aus.
6.  Wählen Sie im Aktivitätsbereich **Exportieren** aus.
7.  Laden Sie die erzeugte Datei herunter und speichern Sie sie lokal.

    Die konfigurierte Gruppe von anwendungsspezifischen Parametern wurde nun als XML-Datei exportiert.

### <a name="import-parameters"></a>Importieren von Parametern

1.  Wählen Sie Version **1.1.2** des EB-Formats aus.
2.  Wählen Sie im Aktivitätsbereich **Importieren** aus.
3.  Wählen Sie **Ja** aus, um zu bestätigen, dass Sie die vorhandenen anwendungsspezifischen Parameter für diese Formatversion überschreiben möchten.
4.  Wählen Sie **Durchsuchen** aus, um die Datei zu suchen, die die exportierten anwendungsspezifischen Parameter für Version **1.1.1** enthält.
5.  Wählen Sie **OK**.

    Version **1.1.2** des EB-Formats verfügt jetzt über die gleichen anwendungsspezifischen Parameter, die Sie ursprünglich für Version **1.1.1** konfiguriert haben.
    
    Beachten Sie, dass die anwendungsspezifischen Parameter eines EB-Formats von der juristischen Person abhängen. Um die anwendungsspezifischen Parameter wieder zu verwenden, die für eine juristische Person in einer anderen juristischen Person konfiguriert wurden, müssen Sie sie exportieren, während Sie in der ersten juristischen Person angemeldet sind, und sie dann importieren, nachdem Sie sich in der anderen juristischen Person angemeldet haben.

    Sie können diesen Ansatz auch verwenden, um EB-Format-zugehörige anwendungsspezifische Parameter, die ursprünglich in einer Instanz von Finance konfiguriert wurden, in eine andere Instanz von Finance zu übertragen.

    Beachten Sie, dass die vorhandenen anwendungsspezifischen Parameter nicht für die importierte Version angewendet werden, wenn Sie anwendungsspezifische Parameter für eine Version eines EB-Formats konfigurieren und eine höhere Version desselben Formats in die aktuelle Finance-Instanz importieren.
    
    Beachten Sie auch, dass, wenn Sie eine Datei für den Import auswählen, die Struktur der anwendungsspezifischen Parameter in dieser Datei mit der Struktur der entsprechenden Datenquelle des Typs **Suche** im EB-Format verglichen wird, die für den Import ausgewählt wird. Der Import ist erledigt, wenn die Struktur jedes anwendungsspezifischen Parameters mit der Struktur der entsprechenden Datenquelle im EB-Format übereinstimmt, die für den Import ausgewählt ist. Wenn die Strukturen nicht übereinstimmen, erhalten Sie eine Warnmeldung, die angibt, dass der Import nicht ausgeführt werden kann. Wenn Sie den Abschluss des Imports erzwingen, werden die vorhandenen anwendungsspezifischen Parameter für das ausgewählte EB-Format bereinigt, und Sie müssen Sie noch einmal neu einrichten.

## <a name="relationship-between-application-specific-parameters-and-an-er-format"></a>Beziehung zwischen anwendungsspezifischen Parametern und einem EB-Format

Die Beziehung zwischen einem EB-Format und seinen anwendungsspezifischen Parametern wird durch den instanzunabhängigen eindeutigen Kennungscode der EB-Instanz bestimmt. Wenn Sie also ein EB-Format aus Finance entfernen, werden die anwendungsspezifischen Parameter, die für das EB-Format konfiguriert werden, in der aktuelle Instanz von Finance beibehalten. Auf sie kann zugegriffen werden, sobald das Basis-EB-Format wieder in diese Finance-Instanz importiert wird.

## <a name="access-application-specific-parameters-by-using-the-er-framework"></a>Zugreifen auf anwendungsspezifische Parameter durch Verwendung des EB-Frameworks

Im vorherigen Beispiel haben Sie auf anwendungsspezifische Parameter eines EB-Formats zugegriffen, indem Sie das EB-Framework verwendet haben. Durch diesen Ansatz können Sie den Zugriff auf die anwendungsspezifischen Parameter eines bestimmten EB-Formats nicht einschränken. Wenn Sie solche Einschränkungen anwenden möchten, gehen Sie folgendermaßen vor. 

1.  Verwenden Sie entweder eine vorhandene Menüoption **ERSolutionAppSpecificParametersDesigner** erneut oder implementieren Sie Ihre eigene Menüoption **ERSolutionAppSpecificParametersDesigner**.

    ![Visual Studio-Seite](./media/GER-AppSpecParms-LookupForm-Access1.PNG)
    
2.  Führen Sie einen dieser Schritte aus:

    1.  Erstellen Sie eine neue Menüoptionsschaltfläche und verknüpfen Sie diese mit dem gewünschten Datensatz aus der Tabelle **ERSolutionTable**, indem Sie die Eigenschaft **Datenquelle** auf **ERSolutionTable** festlegen.
    
        ![Visual Studio-Seite](./media/GER-AppSpecParms-LookupForm-Access2.PNG)
        
    2.  Erstellen Sie eine einfache Schaltfläche und überschreiben Sie die Methode **Geklickt** wie im folgenden Beispiel veranschaulicht.
    
        Wenn Sie diesen Ansatz verwenden, können Sie eine eindeutige Lösungskennung angeben (definiert über den Wert **GUID** ), um den Zugriff auf die anwendungsspezifischen Parameter eines bestimmten EB-Formats und nachfolgenden Kopien zuzulassen, die davon abgeleitet wurden.
        
        ```xpp
        public void clicked()
            {
                super();

                ERSolutionTable solutionTableRecord = ERSolutionTable::findByGUID(str2Guid('ADACCB2F-EFD1-4C90-877D-7E1E5D1AEE92'));

                Args args = new Args();
                args.record(solutionTableRecord);
                args.caller(this);

                new MenuFunction(menuItemDisplayStr(ERSolutionAppSpecificParametersDesigner), MenuItemType::Display)
                    .run(args);
            }
        ```

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Formeldesigner in der elektronischen Berichterstellung](general-electronic-reporting-formula-designer.md)

[Konfigurieren von ER-Formaten zur Verwendung von Parametern, die pro juristischer Person angegeben werden](er-app-specific-parameters-configure-format.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]