---
title: Unterstützen parametrisierter Aufrufe von EB-Datenquellen des Typs „Berechnetes Feld“
description: Dieser Artikel enthält Informationen zum Verwenden des Typs „Berechnetes Feld“ für EB-Datenquellen.
author: kfend
ms.date: 01/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 512ef44d0b0867227ebdc56f83cd6560be64c026
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276017"
---
# <a name="support-parameterized-calls-of-er-data-sources-of-the-calculated-field-type"></a>Unterstützen parametrisierter Aufrufe von EB-Datenquellen des Typs „Berechnetes Feld“

[!include [banner](../includes/banner.md)]

In diesem Artikel wird erläutert, wie Sie eine Datenquelle für die elektronische Berichterstellung (EB) mithilfe des Typs **Berechnetes Feld** entwerfen können. Diese Datenquelle enthält ggf. einen ER-Ausdruck, der bei Ausführung durch die Werte der Parameterargumente gesteuert werden kann, die in einer Bindung konfiguriert sind, die diese Datenquelle aufruft. Wenn Sie parametrisierte Aufrufe einer solchen Datenquelle konfigurieren, können Sie eine einzelne Datenquelle in vielen Bindungen wiederverwenden, wodurch die Gesamtanzahl der Datenquellen verringert wird, die in ER-Modellzuordnungen oder in ER-Formaten konfiguriert werden müssen. Außerdem wird die konfigurierte ER-Komponente vereinfacht, wodurch sich die Instandhaltungskosten sowie die Kosten für die Verwendung durch andere Verbraucher verringern.

## <a name="prerequisites"></a>Voraussetzungen
Um die Beispiele in diesem Artikel abzuschließen, müssen Sie den folgenden Zugriff haben:

- Zugreifen auf eine dieser Rollen:

    - Entwickler für elektronische Berichterstellung
    - Funktionaler Berater für elektronische Berichterstellung
    - Systemadministrator

- Zugriff auf Regulatory Configuration Services (RCS), die für denselben Mandanten wie Finanzen und Betrieb für eine der folgenden Rollen bereitgestellt wurden:

    - Entwickler für elektronische Berichterstellung
    - Funktionaler Berater für elektronische Berichterstellung
    - Systemadministrator

Sie müssen auch die folgenden Dateien herunterladen und lokal speichern.

| **Inhalt**                           | **Dateiname**                                        |
|---------------------------------------|------------------------------------------------------|
| Beispiel-EB-Datenmodell-Konfiguration    | [Model to learn parameterized calls.version.1.xml](https://download.microsoft.com/download/e/5/c/e5c0d3f9-1818-47c7-ae75-46efcbb1314f/Modeltolearnparameterizedcallsversion.1.xml)     |
| Beispiel-EB-Metadatenkonfiguration      | [Metadata to learn parameterized calls.version.1.xml](https://download.microsoft.com/download/8/3/a/83a910a5-bf65-4509-bec4-6737a81ecc45/Metadatatolearnparameterizedcalls.version.1.xml)  |
| Beispiel-EB-Modellzuordnungskonfiguration | [Mapping to learn parameterized calls.version.1.1.xml](https://download.microsoft.com/download/b/f/d/bfd8cbd8-0370-44d1-a1b1-66d021c580ca/Mappingtolearnparameterizedcalls.version.1.1.xml) |
| Beispiel-EB-Formatkonfiguration        | [Format to learn parameterized calls.version.1.1.xml](https://download.microsoft.com/download/8/1/d/81deb6d8-a768-4fcf-bbbe-8f84d2dac3eb/Formattolearnparameterizedcalls.version.1.1.xml)  |

## <a name="sign-in-to-your-rcs-instance"></a>Anmelden bei Ihrer RCS-Instanz
In diesem Beispiel erstellen Sie eine Konfiguration für die Musterfirma Litware, Inc. Zunächst müssen Sie im RCS die Schritte in der Prozedur [Konfigurationsanbieter anlegen durchführen und als aktiv markieren](tasks/er-configuration-provider-mark-it-active-2016-11.md):

1. Wählen Sie im Standard-Dashboard **Elektronische Berichterstellung** aus.
2. Wählen Sie **Berichterstellungskonfigurationen** aus.
3. Importieren Sie die heruntergeladenen Konfigurationen in der folgenden Reihenfolge in RCS: Datenmodell, Metadaten, Modellzuordnung, Format. Führen Sie die folgenden Schritte für jede ER-Konfiguration aus:

    1. Wählen Sie **Wechselkurs** aus.
    2. Wählen Sie **Aus XML-Datei laden** aus.
    3. Wählen Sie **Durchsuchen** und dann die erforderliche EB-Konfiguration im XML-Format aus.
    4. Wählen Sie **OK** aus.

## <a name="review-the-provided-er-solution"></a>Überprüfen der bereitgestellten ER-Lösung

### <a name="review-model-mapping"></a>Überprüfen der Modellzuordnung

1. Erweitern Sie in der Konfigurationsstruktur den Inhalt des Elements **Modell zum Ermitteln parametrisierter Aufrufe**.
2. Wählen Sie **Zuordnung zum Ermitteln parametrisierter Aufrufe** aus.
3. Wählen Sie **Designer** aus.
4. Wählen Sie **Designer** aus.  
   
    Diese ER-Modellzuordnung ist für die folgenden Aktionen vorgesehen:

    - Holen Sie sich die Liste der Steuercodes (**Steuern** Datenquelle), die sich in der Tabelle **Steuertabelle** befinden.
    - Holen Sie sich die Liste der Steuertransaktionen (**Trans** Datenquelle), die sich in der Tabelle **TaxTrans** befinden:
    
        - Gruppieren Sie die Liste der abgerufenen Transaktionen (**GR**-Datenquelle) nach Steuercode.
        - Berechnen Sie für gruppierte Transaktionen nach aggregierten Werten pro Steuercode:

            - Summe der Steuerbasiswerte
            - Summe der Steuerwerte
            - Mindestwert des angewendeten Steuersatzes

    Die Datenzuordnung in dieser Konfiguration implementiert das Basisdatenmodell für jedes der ER-Formate, die für dieses Modell erstellt und in Finanzen und Betrieb ausgeführt werden. Demzufolge wird der Inhalt der **Steuer**- und **GR**-Datenquellen für ER-Formate wie abstrakte Datenquellen bereitgestellt.

    ![Seite „Modellzuordnungsdesigner“ mit Steuer- und GR-Datenquellen.](media/er-calculated-field-type-01.png)

5.  Schließen Sie die Seite **Modellzuordnungsdesigner**.
6.  Schließen Sie die Seite **Modellzuordnung**.

### <a name="review-format"></a>Überprüfen des Formats

1. Erweitern Sie in der Konfigurationsstruktur den Inhalt des Elements **Modell zum Ermitteln parametrisierter Aufrufe**.
2. Wählen Sie **Format zum Ermitteln parametrisierter Anrufe** aus.
3. Wählen Sie **Designer** aus. Dieses ER-Format ist für die folgenden Aktionen vorgesehen:

    - Generieren Sie einen Steuerauszug im XML-Format.
    - Stellen Sie die folgenden Besteuerungsstufen im Steuerauszug dar: „Regulär“, „Reduziert“ und „Keine“.
    - Stellen Sie mehrere Details für jedes Besteuerungsniveau dar, die jeweils eine andere Anzahl von Details auf jeder Stufe aufweisen.

    ![Formatdesignerseite.](media/er-calculated-field-type-02.png)

4. Wählen Sie **Zuordnung** aus.
5. Erweitern Sie die Elemente **Modell**, **Daten,** und **Zusammenfassung**. 

    Das berechnete Feld **Model.Data.Summary.Level** enthält den Ausdruck, der den Code des Besteuerungsniveaus (**Regulär**, **Reduziert**, **Kein,** oder **Sonstige**) als Textwert für jeden Steuercode zurückgibt, der zur Laufzeit aus der Datenquelle **Model.Data.Summary** abgerufen werden kann.

    ![Seite „Formatdesigner“ mit Details des Datenmodells „Modell zum Lernen parametrisierter Aufrufe“.](media/er-calculated-field-type-03.png)

6. Erweitern Sie das Element **Modell**.**Data2**.
7. Erweitern Sie das Element **Modell**.**Data2.Summary2**.
   
    Die Datenquelle **Modell**.**Data2.Summary2** ist zum Gruppieren der Transaktionsdetails der Datenquelle **Model.Data.Summary** nach Besteuerungsniveau (die vom berechneten Feld **Model.Data.Summary.Level** zurückgegeben werden) und zum Berechnen der Aggregationen konfiguriert.

    ![Die Seite „Formatdesigner“ mit Details der Datenquelle „Model.Data2.Summary2“.](media/er-calculated-field-type-04.png)

8. Überprüfen Sie die berechneten Felder **Model**.**Data2.Level1**, **Model**.**Data2.Level2** und **Model**.**Data2.Level3.** Diese berechneten Felder werden verwendet, um die Datensatzliste **Model**.**Data2.Summary2** zu filtern und nur Datensätze zurückzugeben, die ein bestimmtes Besteuerungsniveau darstellen.
9. Seite **Format-Designer** schließen.

## <a name="create-a-derived-format"></a>Erstellen eines abgeleiteten Formats
Sie können das bereitgestellte Format verbessern, indem Sie ein berechnetes Feld hinzufügen, um das erforderliche Besteuerungsniveau zu filtern, anstatt die vorhandenen drei Felder zu verwenden: **Modell**.**Data2.Level1**, **Modell**.**Data2.Level2** und **Modell**.**Data2.Level3**. Das erforderliche Besteuerungsniveau kann an dem Ort festgelegt werden, an dieses neue berechnete Feld aufgerufen wird.

1. Erweitern Sie in der Konfigurationsstruktur den Inhalt des Elements **Modell zum Ermitteln parametrisierter Aufrufe**.
2. Wählen Sie **Format zum Ermitteln parametrisierter Anrufe** aus.
3. Wählen Sie **Konfiguration erstellen**.
4. Wählen Sie **Von Name ableiten: Formatieren zum Ermitteln parametrisierter Aufrufe, Microsoft** aus.
5. Geben Sie im Feld **Name** den Text **Format zum Ermitteln parametrisierter Aufrufe (benutzerdefiniert)** ein.
6. Wählen Sie **Konfiguration erstellen** aus.

## <a name="configure-a-parameterized-calculated-field-that-returns-a-list-of-records"></a>Konfigurieren eines parametrisierten berechneten Felds, das eine Liste der Datensätze zurückgibt

### <a name="start-adding-a-new-calculated-field"></a>Hinzufügen eines neuen berechneten Felds

1. Wählen Sie **Designer** aus.
2. Wählen Sie **Erweitern/Reduzieren** aus, um alle Formatelemente zu erweitern.
3. Wählen Sie **Zuordnung** aus.
4. Erweitern Sie das Element **Model**.
5. Wählen Sie das Element **Modell.Data2** aus.
6. Wählen Sie **Hinzufügen** aus.
7. Wählen Sie das Feld **Funktionen\\Berechnet** aus.
8. Geben Sie im Feld **Name** **Ebenen** ein.
9. Wählen Sie **Formel bearbeiten** aus.

### <a name="define-a-parameter-for-adding-a-calculated-field"></a>Definieren eines Parameters für das Hinzufügen eines berechneten Felds

1. Wählen Sie **Parameter** aus.
2. Wählen Sie **Neu** aus.
3. Geben Sie im Feld **Name** **Besteuerungsniveau** ein.
4. Wählen Sie im Feld **Typ** **Zeichenfolge** aus.

    Es können nur primitive Datentypen verwendet werden, um das Argument des Parametertyps anzugeben. Daher können die Typen **Datensatzliste**, **Datensatz** und **Enumeration** nicht für diesen Zweck verwendet werden.

    Für ein einzelnes berechnetes Feld können maximal 8 Parameter angegeben werden.

    ![Liste der Parameterdatenquellen.](media/er-calculated-field-type-05.png)

5. Wählen Sie **OK** aus.

Durch das Hinzufügen dieses Parameters legen Sie die Bedingung fest, die vorliegen muss, um dieses berechnete Feld aufzurufen. Wenn Sie dieses berechnete Feld aufrufen, müssen Sie das Argument des Paramaters **Besteuerungsniveau** als Wert mit dem Format **Zeichenfolge** angeben.

   Stellen Sie sicher, dass Sie Parameter nur für die berechneten Felder definieren, die sich in einem Container (**Datensatzliste**, **Datensatz** oder **Container**) befinden.

   Der konfigurierte Parameter ist in der Liste der Datenquellen für dieses berechnete Feld verfügbar. Sie können dem konfigurierten Ausdruck den Parameter hinzuzufügen, indem Sie **Datenquelle hinzufügen** auswählen.

   ![Datenquellenfelder.](media/er-calculated-field-type-06.png)

### <a name="define-an-expression-for-adding-a-calculated-field"></a>Definieren eines Ausdrucks für das Hinzufügen eines berechneten Felds

1. Geben Sie im Feld **Formel** Folgendes ein: 

    **WHERE(\@.Summary2, \@.Summary2.grouped.Level =**
    
2. Wählen Sie den Parameter **Besteuerungsniveau** in der Liste der Datenquellen aus.
3. Wählen Sie **Datenquelle hinzufügen** aus:
4. Stellen Sie den Ausdruck im Feld **Formel** folgendermaßen fertig:  

    **WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Taxation Level')**

5. Wählen Sie **Speichern** aus.

    ![Informationen zu Datenquellenfeldern.](media/er-calculated-field-type-07.png)

6. Schließen Sie die Seite **Formeldesigner**.

### <a name="finish-adding-a-new-calculated-field"></a>Abschließen des Hinzufügens eines neuen berechneten Felds

- Wählen Sie **OK**.

Für das konfigurierte, parametrisierte berechnete Feld **Ebenen** auf der Seite **Formatdesigner** ist ein Argument vom Typ **Zeichenfolge** erforderlich.

![Erweiterte Liste der Ebenen des berechneten Felds.](media/er-calculated-field-type-08.png)

### <a name="use-the-configured-calculated-field-for-binding-format-elements"></a>Verwenden Sie das berechnete Feld für konfigurierte verbindliche Formatelemente

1. Wählen Sie **Model.Data2.Levels** aus, um das konfigurierte berechnete Feld auszuwählen.
2. Wählen Sie das Formatelement **Statement.Taxation.Regular** aus.
3. Wählen Sie **Bindung** aus.
4. Wählen Sie **Ja** aus, um die Ersetzung der derzeit verwendeten Datenquelle **Level1** durch die neue Datenquelle **Ebenen** in allen geschachtelten Formatelementen des ausgewählten Formatelements zu bestätigen.

    Die angewendete Bindung wurde als Aufruf des parametrisierten berechneten Felds erstellt. Standardmäßig wird der Name des gebundenen Formatelements als Argument für das parametrisierte berechnete Feld unter den folgenden Bedingungen erstellt:

      - Das berechnete Feld ist für die Verwendung eines einzelnen Parameters konfiguriert.
      - Der Datentyp dieses Parameters ist als **Zeichenfolge** definiert.

    Wenn der Name des gebundenen Formatelements leer ist, wird der Datenquellenname dieses Elements in der angewendeten Bindung verwendet.

5. Wählen Sie das Formatelement **Statement.Taxation.Reduced** aus.
6. Wählen Sie **Bindung** aus.
7. Wählen Sie **Ja** aus, um die Ersetzung der derzeit verwendeten Datenquelle **Level2** durch die neue Datenquelle **Ebenen** in allen geschachtelten Formatelementen unter dem ausgewählten Formatelement zu bestätigen.
8. Wählen Sie das Formatelement **Statement.Taxation.None** aus.
9. Wählen Sie **Bindung** aus.
10. Wählen Sie **Ja** aus, um die Ersetzung der derzeit verwendeten Datenquelle **Level3** durch die neue Datenquelle **Ebenen** in allen geschachtelten Formatelementen unter dem ausgewählten Formatelement zu bestätigen.

   Wenn Sie das Argument des parametrisierten berechneten Felds für das XML-Element angeben, das das Besteuerungsniveau darstellt (z. B. **Model.Data2.Levels("Reduced")** als Textwert), müssen Sie diesen Schritt nicht für die geschachtelten XML-Attribute ausführen. Deren Bindungen übernehmen den Wert des auf der übergeordneten Ebene zugeordneten Arguments (**Model.Data2.Levels.aggregated.Base**, nicht **Model.Data2.Levels("Reduced").aggregated.Base**).

Wiederkehrende Aufrufe von parametrisierten berechneten Feldern werden nicht unterstützt.

Sie können **Formel bearbeiten** auswählen und das standardmäßig übernommene Argument des parametrisierten berechneten Felds in der ausgewählten Bindung ändern. Wenn dieses Argument nicht vorhanden ist, kann dies zu Fehlern während der Laufzeit kommen. Benutzer werden über solch eine Situation informiert, wenn das aktuelle Format überprüft wird.

![Benachrichtigung zu Überprüfungswarnungen.](media/er-calculated-field-type-10.png)

## <a name="configure-a-parameterized-calculated-field-to-return-a-record"></a>Konfigurieren eines parametrisierten berechneten Felds für die Rückgabe eines Datensatzes
Wenn ein parametrisiertes berechnetes Feld einen Datensatz zurückgibt, müssen Sie die Bindung einzelner Felder dieses Datensatzes zu Formatelementen unterstützen. In solchen Fällen ist keine übergeordnete Bindung vorhanden, die den Wert eines Arguments zum Aufrufen eines parametrisierten berechneten Felds enthält. Dieser Wert muss in der Bindung des Felds einen einzelnen Datensatz definiert werden.

### <a name="start-adding-a-new-calculated-field"></a>Hinzufügen eines neuen berechneten Felds

1. Wählen Sie das Element **Modell.Data2** aus.
2. Wählen Sie **Hinzufügen** aus.
3. Wählen Sie das Feld **Funktionen\\Berechnet** aus.
4. Geben Sie im Feld **Name** die Bezeichnung **LevelRecord** ein.
5. Wählen Sie **Formel bearbeiten** aus.

### <a name="define-a-parameter-for-adding-a-calculated-field"></a>Definieren eines Parameters für das Hinzufügen eines berechneten Felds

1. Wählen Sie **Parameter** aus.
2. Wählen Sie **Neu** aus.
3. Geben Sie im Feld **Name** **Besteuerungsniveau** ein.
4. Wählen Sie im Feld **Typ** **Zeichenfolge** aus.
5. Wählen Sie **OK**.

### <a name="define-an-expression-for-adding-a-calculated-field"></a>Definieren eines Ausdrucks für das Hinzufügen eines berechneten Felds

1. Geben Sie im Feld **Formel** Folgendes ein:  
    
    **FIRSTORNULL(\@.Levels(**

2. Wählen Sie den Parameter **Taxation Level** aus.
3. Wählen Sie **Datenquelle hinzufügen** aus:
4. Hängen Sie im Feld **Formel** **'Taxation Level'))** an die Eingabe in Schritt 1 an, um den Ausdruck abzuschließen:  
    
    **FIRSTORNULL(\@.Levels('Taxation Level'))**

5. Wählen Sie **Speichern**.
6. Schließen Sie die Seite **Formeldesigner**.

### <a name="finish-adding-a-new-calculated-field"></a>Abschließen des Hinzufügens eines neuen berechneten Felds

-   Wählen Sie **OK**.

### <a name="use-the-configured-calculated-field-to-bind-format-elements"></a>Verwenden des konfigurierten berechneten Felds zum Binden von Formatelementen

1. Erweitern Sie **Model.Data2.LevelRecord**, um das konfigurierte berechnete Feld auszuwählen.
2. Erweitern Sie den Container **Model.Data2.LevelRecord.aggregated** des konfigurierten berechneten Felds.
3. Wählen Sie das Feld **Model.Data2.LevelRecord.aggregated.Base** aus.
4. Wählen Sie das Formatelement **Statement.Taxation.None** aus.
5. Wählen Sie **Bindung aufheben** aus.
6. Wählen Sie das Formatelement **Statement.Taxation.None.Base** aus.
7. Wählen Sie **Bindung** aus.
8. Wählen Sie **Formel bearbeiten** aus.
9. Ändern Sie den Ausdruck in **Model.Data2.LevelRecord("None").aggregated.Base**.

![Aktualisierter Ausdruck.](media/er-calculated-field-type-11.png)

## <a name="remove-calculated-fields-that-are-not-used"></a>Entfernen von berechneten Feldern, die nicht verwendet werden

1. Wählen Sie **Model.Data2.Level1** aus.
2. Wählen Sei **Löschen**.
3. Wählen Sie **Model.Data2.Level2** aus.
4. Wählen Sei **Löschen**.
5. Wählen Sie **Model.Data2.Level3** aus.
6. Wählen Sei **Löschen**.
7. Wählen Sie **Speichern**.

  > [!NOTE]
  > Sie haben dasselbe berechnete Feld **Model.Data2.Levels** mehrmals in Formatbindungen verwendet. Es ist viel einfacher, ein einzelnes berechnetes Feld zu verwenden und beizubehalten, anstatt diesen Schritt für mehrere ähnliche Felder auszuführen.

8. Seite **Format-Designer** schließen.

## <a name="complete-adjusted-version-of-a-derived-format"></a>Abschließen der angepassten Version eines abgeleiteten Formats

1. Wählen Sie im Inforegister **Versions** **Status ändern** aus.
2. Wählen Sie **Abgeschlossen** aus.

## <a name="export-completed-version-of-a-derived-format"></a>Exportieren der abgeschlossenen Version eines abgeleiteten Formats

1. Wählen Sie in der Konfigurationsstruktur **Format zum Ermitteln parametrisierter Aufrufe (benutzerdefiniert)** aus.
2. Wählen Sie im Inforegister **Versionen** die abgeschlossene Version 1.1.1 aus.
3. Wählen Sie **Wechselkurs** aus.
4. Wählen Sie **Als XML-Datei exportieren** aus.
5. Speichern Sie die lokal heruntergeladene Konfiguration im XML-Format.

## <a name="test-er-formats"></a>Testen von ER-Formaten 
Sie können die anfänglichen und verbesserten ER-Formate ausführen, um sicherzustellen, dass parametrisierte berechnete Felder, die konfiguriert sind, ordnungsgemäß funktionieren.

### <a name="import-er-configurations"></a>ER Konfigurationen importieren
Sie können überprüfte Konfigurationen aus RCS importieren, indem Sie das ER-Repository des Typs **RCS** verwenden. Wenn Sie die Schritte im Artikel [Importieren von elektronischen Berichtskonfigurationen (EB-Konfigurationen) aus Regulatory Configuration Services (RCS)](rcs-download-configurations.md) bereits durchgeführt haben, verwenden Sie das konfigurierte EB-Repository, um die zuvor in diesem Artikel beschriebenen Konfigurationen in Ihre Umgebung zu importieren. Andernfalls führen Sie die folgenden Schritte aus:

1. Wählen Sie das Unternehmen **DEMF** und im Standard-Dashboard die Option **Elektronische Berichterstellung** aus.
2. Wählen Sie **Berichterstellungskonfigurationen** aus.
3. Importieren Sie die Konfigurationen aus dem Microsoft Download Center in der folgenden Reihenfolge: Datenmodell, Modellzuordnung, Format. Führen Sie die folgenden Schritte für jede ER-Konfiguration aus:

    1. Wählen Sie **Wechselkurs** aus.
    2. Wählen Sie **Aus XML-Datei laden** aus.
    3. Wählen Sie **Durchsuchen** aus, um die erforderliche EB-Konfiguration im XML-Format auszuwählen.
    4. Wählen Sie **OK**.

4. Importieren Sie die aus RCS exportierte abgeschlossene Version 1.1.1 des Formats **Format zum Ermitteln parametrisierter Aufrufe (benutzerdefiniert)**:

    1. Wählen Sie **Wechselkurs** aus.
    2. Wählen Sie **Aus XML-Datei laden** aus.
    3. Wählen Sie **Durchsuchen** aus, um die lokal gespeicherte Datei **Format zum Ermitteln parametrisierter Anrufe (benutzerdefiniert)** im XML-Format auszuwählen.
    4. Wählen Sie **OK**.

### <a name="run-er-formats"></a>Ausführen von ER-Formaten

1. Erweitern Sie in der Konfigurationsstruktur den Inhalt des Elements **Modell zum Ermitteln parametrisierter Aufrufe**.
2. Wählen Sie **Format zum Ermitteln parametrisierter Anrufe** aus.
3. Wählen Sie im oberen Menüband **Ausführen** aus.
4. Speichern Sie das lokal generierte Ergebnis.
5. Wählen Sie das Element **Format zum Ermitteln parametrisierter Aufrufe (benutzerdefiniert)** aus.
6. Wählen Sie im oberen Menüband **Ausführen** aus.
7. Speichern Sie das generierte Ergebnis lokal. 
8. Vergleichen Sie den Inhalt der generierten Ergebnisse.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Formeldesigner in der elektronischen Berichterstellung (EB)](general-electronic-reporting-formula-designer.md)
- [Verbessern Sie die Leistung von EB-Lösungen, indem Sie parametrisierte CALCULATED FIELD-Datenquellen hinzufügen](er-calculated-field-ds-performance.md)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

