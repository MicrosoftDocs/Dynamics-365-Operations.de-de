---
title: Parameter eines ER-Formats pro juristischer Person einrichten
description: In diesem Artikel wird erläutert, wie Sie die Parameter eines Elektronische Berichterstellungs(EB)-Formats pro juristischer Entität konfigurieren können.
author: NickSelin
ms.date: 03/25/2022
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
ms.openlocfilehash: dbcf968dde432da182b5bd2d6a7bcb9f83dad6fa
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890211"
---
# <a name="set-up-the-parameters-of-an-er-format-per-legal-entity"></a>Einrichten von Parametern eines EB-Formats pro juristischer Person

[!include[banner](../includes/banner.md)]

## <a name="prerequisites"></a>Voraussetzungen

Um diese Schritte auszuführen, müssen Sie zuerst die Schritte in [Konfigurieren von EB-Formaten zur Verwendung von Parametern, die pro juristischer Person angegeben werden](er-app-specific-parameters-configure-format.md) ausführen.

Um die Beispiele in diesem Artikel abzuschließen, müssen Sie für eine der folgenden Rollen Zugriff auf Microsoft Dynamics 365 Finance haben:

- Entwickler für elektronische Berichterstellung
- Funktionaler Berater für elektronische Berichterstellung
- Systemadministrator

## <a name="import-er-configurations"></a>ER Konfigurationen importieren
Führen Sie für den Imort von EB-Konfiguration die folgenden Schritte aus: 

1. Melden Sie sich in Ihrer Umgebung an.
2. Wählen Sie im Standard-Dashboard **Elektronische Berichterstellung** aus.
3. Wählen Sie **Berichterstellungskonfigurationen** aus.
4. Importieren Sie die Konfigurationen, die Sie während der Ausführung der Schritte in [Konfigurieren von EB-Formaten zur Verwendung von Parametern, die pro juristischer Person angegeben werden](er-app-specific-parameters-configure-format.md) aus Regulatory Configuration Services (RCS) exportiert haben, in die aktuelle Instanz von Finance. Führen Sie diese Schritte für jede Konfiguration der [elektronischen Berichterstellung (EB)](general-electronic-reporting.md) in der folgenden Reihenfolge aus: Datenmodell, Modellzuordnung und Formate.

    1. Wählen Sie **Austausch \> Aus XML-Datei laden** aus.
    2. Wählen Sie **Durchsuchen** aus, um die Datei für die erforderliche EB-Konfiguration im XML-Format auszuwählen.
    3. Wählen Sie **OK**.

    Die folgende Abbildung zeigt die Konfigurationen, die Sie haben müssen, wenn Sie fertig sind.

    ![EB-Konfigurationsseite.](./media/GER-AppSpecParms-ImportedConfigurations.PNG)

## <a name="set-up-parameters-for-the-demf-company"></a>Einrichten von Parametern für das DEMF-Unternehmen

Sie können das EB-Framework verwenden, um anwendungsspezifische Parameter für ein EB-Format einzurichten.

1. Wählen Sie die juristische Person **DEMF** aus.
2. Wählen Sie in der Konfigurationsstruktur das Format **Format zum Ermitteln der Vorgehensweise bei der Suche von Daten zu juristischen Personen** aus.
3. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Konfigurationen** in der Gruppe **Anwendungsspezifische Parameter** die Option **Einrichten** aus.

    ![Anwendungsspezifische ER-Parameterseite zum Einrichten von Parametern.](./media/GER-AppSpecParms-LookupForm.PNG)

    Auf der Seite **Anwendungsspezifische Parameter** können Sie die Regeln für die Datenquelle **Auswahl** des Formats **Format zum Ermitteln der Vorgehensweise bei der Suche von Daten zu juristischen Personen** konfigurieren.

    Wenn das Basis-EB-Format mehrere Datenquellen des Typs **Suche** enthält, müssen Sie die gewünschte Datenquelle im Inforegister **Suchen** auswählen, bevor Sie beginnen können, die Gruppe von Regeln für die Datenquelle zu konfigurieren.

    Für jede Datenquelle können Sie separate Regeln für jede Version des ausgewählten EB-Formats konfigurieren.

    Die gesamten Regeln für alle Suchendatenquellen, die in der ausgewählten Version des Basis-EB-Formats zur Verfügung stehen, stellen die anwendungsspezifischen Parameter für das EB-Format dar.

4. Wählen Sie Version **1.1.1** des EB-Formats aus.
5. Auf dem Inforegister **Bedingungen** wählen Sie **Hinzufügen** aus.
6. Wählen Sie im Feld **Code** des neuen Datensatzes den Dropdown-Pfeil aus, um die Suche zu öffnen.

    Die Suche zeigt die Liste der Steuercodes für die Auswahl an. Diese Liste wird durch die Datenquelle **Model.Data.Tax** zurückgegeben, die im Basis-EB-Format konfiguriert wurde. Da diese Datenquelle das Feld **Name** enthält, wird der Name jedes Steuercodes in der Suche angezeigt.

    ![Codefeldsuche auf der Seite für anwendungsspezifische ER-Parameter.](./media/GER-AppSpecParms-LookupForm-CodeFldPicker.PNG)

7. Wählen Sie den Steuercode **VAT19** aus.
8. Wählen Sie im Feld **Suchergebnis** des neuen Datensatzes den Dropdown-Pfeil aus, um die Suche zu öffnen. Die Suche zeigt die Liste der Werte für die TaxationLevel-Formatenumeration zur Auswahl an.

    Hinweis: Wenn Sie Deutsch als bevorzugte Sprache des Benutzers auswählen, als der Sie angemeldet sind, werden die Beschriftungen der Werte in der Suche auf Deutsch angezeigt, sofern sie im Basis-EB-Format übersetzt wurden. Darüber hinaus erscheint die Beschriftung in der bevorzugten Sprache des Benutzers auf der Registerkarte **Suchen**, wennn die Beschriftung einer Suchendatenquelle übersetzt wurde.

    ![In Deutsch übersetztes Suchfeld auf der anwendungsspezifischen ER-Parameterseite.](./media/GER-AppSpecParms-LookupForm-LookupFldPicker.PNG)

9. Wählen Sie den Wert **Reguläre Besteuerung** aus.

    Wenn Sie diesen Datensatz hinzufügen, legen Sie die folgende Regel fest: Sobald die Suchendatenquelle **Auswahl** angefordert wird und der Steuercode **VAT19** als Argument weitergegeben wird, wird **Reguläre Besteuerung** als erforderliche Besteuerungsstufe zurückgegeben.

10. Wählen Sie **Hinzufügen** aus und führen Sie die folgenden Schritte aus:

    1. Wählen Sie im Feld **Code** den Steuercode **InVAT19** aus.
    2. Wählen Sie im Feld **Suchergebnis** den Wert **Reguläre Besteuerung** aus.

11. Wählen Sie **Hinzufügen** aus und führen Sie die folgenden Schritte aus:

    1. Wählen Sie im Feld **Code** den Steuercode **VAT7** aus.
    2. Wählen Sie im Feld **Suchergebnis** den Wert **Reduzierte Besteuerung** aus.

12. Wählen Sie **Hinzufügen** aus und führen Sie die folgenden Schritte aus:

    1. Wählen Sie im Feld **Code** den Steuercode **InVAT7** aus.
    2. Wählen Sie im Feld **Suchergebnis** den Wert **Reduzierte Besteuerung** aus.

13. Wählen Sie **Hinzufügen** aus und führen Sie die folgenden Schritte aus:

    1. Wählen Sie im Feld **Code** den Steuercode **THIRD** aus.
    2. Wählen Sie im Feld **Suchergebnis** den Wert **Keine Besteuerung** aus.

14. Wählen Sie **Hinzufügen** aus und führen Sie die folgenden Schritte aus:

    1. Wählen Sie im Feld **Code** den Steuercode **InVAT0** aus.
    2. Wählen Sie im Feld **Suchergebnis** den Wert **Keine Besteuerung** aus.

15. Wählen Sie **Hinzufügen** aus und führen Sie die folgenden Schritte aus:

    1. Wählen Sie im Feld **Code** die Option **\*Nicht leer\*** aus.
    2. Wählen Sie im Feld **Suchergebnis** den Wert **Sonstige** aus.

    Wenn Sie diesen letzten Datensatz hinzufügen, legen Sie die folgende Regel fest: Sobald der Steuercode, der als Argument weitergegeben wird, keine der vorherigen Regeln erfüllt, gibt die Suchdatenquelle **Sonstige** als erforderliche Besteuerungsstufe zurück.

    ![Letzter auf der Seite für anwendungsspezifische ER-Parameter hinzugefügter Datensatz.](./media/GER-AppSpecParms-LookupForm-RulesSet.PNG)

16. Wählen Sie im Feld **Status** die Option **Abgeschlossen** aus.

    Wenn Sie eine EB-Formatversion ausführen, die entweder über den Status **Abgeschlossen** oder **Geteilt** verfügt, muss diese Gruppe von Regeln im Status **Abgeschlossen** sein. Andernfalls wird Ausführung des Basis-EB-Formats unterbrochen, wenn das Format versucht, Daten aus dieser Gruppe von Regeln zu laden, während die Suchdatenquelle **Auswahl** ausgeführt wird.

    Wenn Sie eine EB-Formatversion ausführen, die den Status **Entwurf** hat, kann das Basis-EB-Format unabhängig von deren Status auf diese Gruppe von Regeln zugreifen.

17. Wählen Sie **Speichern**.
18. Schließen Sie die Seite **Anwendungsspezifische Parameter**.

## <a name="run-the-er-format-in-the-demf-company"></a>Ausführen des EB-Formats im Unternehmen DEMF
Um das ER-Format im DEMF-Unternehmen auszuführen, folgen Sie diesen Schritten: 

1. Wählen Sie in der Konfigurationsstruktur das Format **Format zum Ermitteln der Vorgehensweise bei der Suche von Daten zu juristischen Personen** aus.
2. Wählen Sie im Aktivitätsbereich auf **Ausführen**.
3. Im angezeigten Dialogfeld wählen Sie **OK** aus.
4. Laden Sie den erzeugten Auszug herunter und speichern Sie ihn lokal.

    Beachten Sie, dass im generierten Auszug die Zusammenfassung des Steuercodes **InVAT7** auf die Ebene **Reduziert** festgelegt ist, und Zusammenfassungen der Steuercodes **VAT19** und **InVA19** auf die Ebene **Regulär** festgelegt ist. Dieses Verhalten wird von der Konfiguration in der Gruppe von Regeln bestimmt, die von juristischen Entitäten abhängen.

5. Gehen Sie zu **Steuer \> Indirekte Steuern \> Mehrwertsteuer \> Mehrwertsteuercodes**.
6. Wählen Sie den Steuercode **InVAT7** aus.
7. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Mehrwertsteuercode** in der Gruppe **Abfragen** die Option **Gebuchte Mehrwertsteuer** aus, um Informationen zum Steuerwert und dem angewendeten Steuersatz pro Steuercode anzuzeigen.

    ![Veröffentlichte Umsatzsteuer-Seite.](./media/GER-AppSpecParms-Statement.PNG)

8. Schließen Sie die Seite **Gebuchte Mehrwertsteuer**.

## <a name="set-up-parameters-for-the-usmf-company"></a>Einrichten von Parametern für das USMF-Unternehmen
Führen Sie die folgenden Schritte aus, um Parameter für die USMF-Firma einzurichten: 

1. Wählen Sie die juristische Person **USMF** aus.
2. Wechseln Sie zu **Organisationsverwaltung \> Elektronische Berichterstellung \> Konfigurationen**.
3. Erweitern Sie in der Konfigurationsstruktur das Element **Modell zum Lernern parametrisierter Aufrufe**, erweitern Sie das Element **Format zum Ermitteln parametrisierter Anrufe**, und wählen Sie das Format **Format zum Ermitteln der Vorgehensweise bei der Suche von Daten zu juristischen Personen** aus.
4. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Konfigurationen** in der Gruppe **Anwendungsspezifische Parameter** die Option **Einrichten** aus.
5. Wählen Sie Version **1.1.1** des ausgewählten EB-Formats aus.
6. Auf dem Inforegister **Bedingungen** wählen Sie **Hinzufügen** aus.
7. Wählen Sie im Feld **Code** des neuen Datensatzes den Dropdown-Pfeil aus, um die Suche zu öffnen.

    Die Suche zeigt nun die Liste der Steuercodes für die Steuer des **USMF**-Unternehmens zur Auswahl an.

    ![Steuercodes für die USMF-Unternehmenssteuer.](./media/GER-AppSpecParms-LookupForm-CodeFldPicker2.PNG)

8. Wählen Sie den Steuercode **BEFREIT** aus.
9. Wählen Sie im Feld **Suchergebnis** des neuen Datensatzes den Wert **Keine Besteuerung** aus.
10. Wählen Sie **Hinzufügen** aus.
11. Wählen Sie im Feld **Code** des neuen Datensatzes die Option **\*Nicht leer\*** aus.
12. Wählen Sie im Feld **Suchergebnis** des neuen Datensatzes den Wert **Reguläre Besteuerung** aus.
13. Wählen Sie im Feld **Status** die Option **Abgeschlossen** aus.
14. Wählen Sie **Speichern** aus.

    ![Seite für anwendungsspezifische EB-Parameter.](./media/GER-AppSpecParms-LookupForm-RulesSet2.PNG)

15. Schließen Sie die Seite **Anwendungsspezifische Parameter**.

## <a name="run-the-er-format-in-the-usmf-company"></a>Ausführen des EB-Formats im Unternehmen USMF
Um das ER-Format im USMF-Unternehmen auszuführen, schließen Sie diese Schritte ab:

1. Wählen Sie in der Konfigurationsstruktur das Format **Format zum Ermitteln der Vorgehensweise bei der Suche von Daten zu juristischen Personen** aus.
2. Wählen Sie im Aktivitätsbereich auf **Ausführen**.
3. Im angezeigten Dialogfeld wählen Sie **OK** aus.
4. Laden Sie den erzeugten Auszug herunter und speichern Sie ihn lokal.

    Beachten Sie, dass Sie nun im generierten Auszug dasselbe EB-Format wieder für eine andere juristische Person verwendet haben, ohne jedoch Änderungen am EB-Format vorzunehmen.

## <a name="reuse-legal-entitydependent-parameters"></a>Wiederverwenden von Parametern, die von juristischen Personen abhängen

### <a name="duplicate-existing-parameters"></a>Vorhandene Parameter duplizieren

#### <a name="export-parameters"></a>Exportieren von Parametern
Um Parameter zu exportieren, führen Sie die folgenden Schritte aus:

1. Wechseln Sie zu **Organisationsverwaltung \> Arbeitsbereiche \> Elektronische Berichterstellung**.
2. Wählen Sie **Berichterstellungskonfigurationen** aus.
3. Wählen Sie in der Konfigurationsstruktur das Format **Format zum Ermitteln der Vorgehensweise bei der Suche von Daten zu juristischen Personen** aus.
4. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Konfigurationen** in der Gruppe **Anwendungsspezifische Parameter** die Option **Einrichten** aus.
5. Wählen Sie Version **1.1.1** des EB-Formats aus.
6. Wählen Sie im Aktivitätsbereich **Exportieren** aus.
7. Laden Sie die erzeugte Datei herunter und speichern Sie sie lokal.

    Die konfigurierte Gruppe von anwendungsspezifischen Parametern wurde nun als XML-Datei exportiert.

#### <a name="import-parameters"></a>Importieren von Parametern
Um Parameter zu importieren, führen Sie die folgenden Schritte aus:

1. Wählen Sie Version **1.1.2** des EB-Formats aus.
2. Wählen Sie im Aktivitätsbereich **Importieren** aus.
3. Wählen Sie **Ja** aus, um zu bestätigen, dass Sie die vorhandenen anwendungsspezifischen Parameter für diese Formatversion überschreiben möchten.
4. Wählen Sie **Durchsuchen** aus, um die Datei zu suchen, die die exportierten anwendungsspezifischen Parameter für Version **1.1.1** enthält.
5. Wählen Sie **OK**.

    Version **1.1.2** des EB-Formats verfügt jetzt über die gleichen anwendungsspezifischen Parameter, die Sie ursprünglich für Version **1.1.1** konfiguriert haben.

##### <a name="applicability-considerations"></a>Überlegungen zur Anwendbarkeit

Die anwendungsspezifischen Parameter eines EB-Formats hängen von der juristischen Person ab. Um die anwendungsspezifischen Parameter wieder zu verwenden, die für eine juristische Person in einer anderen juristischen Person konfiguriert wurden, müssen Sie sie exportieren, während Sie in der ersten juristischen Person angemeldet sind. Importieren Sie sie dann, nachdem Sie sich bei der anderen juristischen Person angemeldet haben.

Sie können diesen Export/Import-Ansatz auch verwenden, um EB-Format-zugehörige anwendungsspezifische Parameter, die ursprünglich in einer Instanz von Finance konfiguriert wurden, in eine andere Instanz von Finance zu übertragen.

Wenn Sie anwendungsspezifische Parameter für eine Version eines ER-Formats konfigurieren und dann eine spätere Version desselben Formats in die aktuelle Finance-Instanz importieren, werden die vorhandenen anwendungsspezifischen Parameter nicht auf die importierte Version angewendet, es sei denn, Sie verwenden die **Anwendungsspezifische Parameter aus früheren Versionen von ER-Formaten verwenden**-Funktion. Weitere Informationen finden Sie im Abschnitt [Vorhandene Parameter wiederverwenden](#reuse-existing-parameters) weiter unten in diesem Artikel.

Wenn Sie eine Datei für den Import auswählen, wird die Struktur der anwendungsspezifischen Parameter in dieser Datei mit der Struktur der entsprechenden Datenquellen des Typs **Suche** im ER-Format verglichen, die für den Import ausgewählt wird. Standardmäßig ist der Import nur abgeschlossen, wenn die Struktur jedes anwendungsspezifischen Parameters mit der Struktur der entsprechenden Datenquelle im ER-Format übereinstimmt, die für den Import ausgewählt ist. Wenn die Strukturen nicht übereinstimmen, informiert Sie eine Warnmeldung, dass der Import nicht abgeschlossen werden kann. Wenn Sie den Import erzwingen, werden die vorhandenen anwendungsspezifischen Parameter für das ausgewählte ER-Format bereinigt, und Sie müssen Sie noch einmal neu einrichten.


Ab Finance-Version 10.0.24 können Sie das Standardverhalten ändern und das Erhalten einer Warnmeldung vermeiden, indem Sie die **Anwendungsspezifische ER-Parameter beim Importieren ausrichten**-Funktion im **Funktionsverwaltung**-Arbeitsbereich aktivieren. Wenn diese Funktion aktiviert ist, sofern die Struktur der anwendungsspezifischen Parameter, die Sie importieren, sich von der Struktur der entsprechenden Datenquellen im Ziel ER-Format unterscheiden, das für den Import ausgewählt wird, ist der Import in folgenden Fällen erfolgreich:

- Die Struktur des Ziel-ER-Formats wurde geändert, indem allen vorhandenen Datenquellen des Typs **Suche** neue Bedingungsspalten hinzugefügt wurden. Wenn der Import abgeschlossen ist, werden die anwendungsspezifischen Parameter aktualisiert. In allen importierten Datensätzen anwendungsspezifischer Parameter werden die Werte in jeder hinzugefügten Bedingungsspalte mit dem Standardwert für den [Datentyp](er-formula-supported-data-types-primitive.md) dieser Spalte initialisiert.
- Die Struktur des Ziel-ER-Formats wurde geändert, indem einige Bedingungsspalten von allen vorhandenen Datenquellen des Typs **Suche** entfernt wurden. Wenn der Import abgeschlossen ist, werden die anwendungsspezifischen Parameter aktualisiert. In allen importierten Datensätzen anwendungsspezifischer Parameter werden die Werte in jeder entfernten Bedingungsspalte gelöscht.
- Die Struktur des Ziel-ER-Formats wurde geändert, indem neue Datenquellen des Typs **Suche** hinzugefügt wurden. Wenn der Import abgeschlossen ist, werden hinzugefügte Suchen den anwendungsspezifischen Parametern angefügt.
- Die Struktur des Ziel-ER-Formats wurde geändert, indem einige der vorhandenen Datenquellen des Typs **Suche** entfernt wurden. Wenn der Import abgeschlossen ist, werden alle Artefakte, die sich auf die Datenquellen des **Suche**-Typs beziehen, die aus dem Ziel-ER-Format entfernt wurden, aus den importierten anwendungsspezifischen Parametern gelöscht.

Nach Abschluss des Imports wird zusätzlich zu den eben beschriebenen Änderungen der Zustand der importierten anwendungsspezifischen Parameter auf **In Bearbeitung** geändert. Eine Warnmeldung weist Sie darauf hin, dass die automatisch angepassten anwendungsspezifischen Parameter manuell bearbeitet werden müssen.

#### <a name="replicate-parameters"></a>Parameter replizieren

Ab Finance-Version 10.0.27 können Sie die Parameter, die Sie in einem Unternehmen konfiguriert haben, gleichzeitig auf andere Unternehmen kopieren.

Um Parameter zu kopieren, führen Sie die folgenden Schritte aus.

1. Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.
2. Wählen Sie **Berichterstellungskonfigurationen** aus.
3. Wählen Sie in der Konfigurationsstruktur das Format **Format zum Ermitteln der Vorgehensweise bei der Suche von Daten zu juristischen Personen** aus.
4. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Konfigurationen** in der Gruppe **Anwendungsspezifische Parameter** die Option **Einrichten** aus.
5. Wählen Sie Version **1.1.1** des EB-Formats aus.
6. Wählen Sie im Aktivitätsbereich **Replizieren** aus.
7. Wählen Sie im **Replizieren**-Dialogfeld auf der **Unternehmen**-Registerkarte die Unternehmen aus, in die Sie Parameter kopieren möchten.

    > [!NOTE]
    > Die Liste der Zielunternehmen wird nur Benutzern angeboten, denen ein Sicherheits-[Rolle](../sysadmin/role-based-security.md#security-roles) zugewiesen ist, die so konfiguriert ist, dass sie allen Organisationen Zugriff gewährt.

8. Wählen Sie **OK** aus.

    > [!NOTE]
    > Der Bestätigungsdialog informiert Sie, wenn einige Zielfirmen bereits konfigurierte Parameter für die ausgewählte Version eines ER-Formats enthalten. Wählen Sie **Ja** aus, um die Parameter zu überschreiben, indem Sie sie aus der aktuellen Firma kopieren.

    Der konfigurierte Satz anwendungsspezifischer Parameter wird nun auf die ausgewählten Firmen kopiert.

### <a name="reuse-existing-parameters"></a>Vorhandene Parameter wiederverwenden

Ab Finance-Version 10.0.23 können Sie anwendungsspezifische Parameter wiederverwenden, die für eine Version eines ER-Formats konfiguriert wurden, wenn Sie eine höhere Version desselben Formats ausführen. Aktivieren Sie zum Wiederverwenden vorhandener Parameter die **Anwendungsspezifische Parameter aus früheren Versionen von ER-Formaten verwenden**-Funktion im **Funktionsverwaltung**-Arbeitsbereich. Wenn diese Funktion aktiviert ist und Sie eine Version eines ER-Formats ausführen, die versucht, anwendungsspezifische Parameter zu lesen, versucht ER, anwendungsspezifische Parameter zu finden, die für die ausgeführte Version des Formats konfiguriert wurden. Wenn sie nicht verfügbar sind, versucht ER, sie für die nächst niedrigere Version des Formats zu finden.

> [!NOTE]
> Anwendungsspezifische Parameter können Sie nur im Geltungsbereich der aktuellen juristischen Person wiederverwenden.
>
> Zur Laufzeit wird ein Fehler angezeigt, wenn Sie eine höhere Version eines ER-Formats ausführen, die versucht, anwendungsspezifische Parameter wiederzuverwenden, die für eine niedrigere Version des gleichen Formats konfiguriert wurden, und die Struktur mindestens einer Datenquelle des **Suche**-Typs in der höheren Formatversion geändert wurden.

## <a name="relationship-between-application-specific-parameters-and-an-er-format"></a>Beziehung zwischen anwendungsspezifischen Parametern und einem EB-Format

Die Beziehung zwischen einem EB-Format und seinen anwendungsspezifischen Parametern wird durch den instanzunabhängigen eindeutigen Kennungscode der EB-Instanz bestimmt. Wenn Sie also ein EB-Format aus Finance entfernen, werden die anwendungsspezifischen Parameter, die für das EB-Format konfiguriert werden, in der aktuelle Instanz von Finance beibehalten. Auf sie kann zugegriffen werden, sobald das Basis-EB-Format wieder in diese Finance-Instanz importiert wird.

## <a name="access-application-specific-parameters-by-using-the-er-framework"></a>Zugreifen auf anwendungsspezifische Parameter durch Verwendung des EB-Frameworks

Im vorherigen Beispiel haben Sie auf anwendungsspezifische Parameter eines EB-Formats zugegriffen, indem Sie das EB-Framework verwendet haben. Durch diesen Ansatz können Sie den Zugriff auf die anwendungsspezifischen Parameter eines bestimmten EB-Formats nicht einschränken. Wenn Sie solche Einschränkungen anwenden möchten, gehen Sie folgendermaßen vor. 

1. Verwenden Sie entweder eine vorhandene Menüoption **ERSolutionAppSpecificParametersDesigner** erneut oder implementieren Sie Ihre eigene Menüoption **ERSolutionAppSpecificParametersDesigner**.

    ![Menüpunktanzeige des ERSolutionAppSpecificParametersDesigner.](./media/GER-AppSpecParms-LookupForm-Access1.PNG)

2. Führen Sie einen dieser Schritte aus:

    1. Erstellen Sie eine neue Menüoptionsschaltfläche und verknüpfen Sie diese mit dem gewünschten Datensatz aus der Tabelle **ERSolutionTable**, indem Sie die Eigenschaft **Datenquelle** auf **ERSolutionTable** festlegen.

        ![Anzeige neuer Menüpunkt-Einstellungen.](./media/GER-AppSpecParms-LookupForm-Access2.PNG)

    2. Erstellen Sie eine einfache Schaltfläche und überschreiben Sie die Methode **Geklickt** wie im folgenden Beispiel veranschaulicht.

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
