---
title: Länderkontextabhängige ER-Modellzuordnungen konfigurieren
description: In diesem Thema wird erläutert, wie Sie ER-Modellzuordnungen so einrichten können, dass sie vom Länder-/Regionalkontext der juristischen Person abhängen, die ihre Verwendung kontrolliert.
author: NickSelin
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.2
ms.openlocfilehash: 64963348ef2cf850477d03fcb9a40d3a167c715bea86eca1d756f01f54472d5a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6718550"
---
# <a name="configure-country-context-dependent-er-model-mappings"></a>Länderkontextabhängige ER-Modellzuordnungen konfigurieren

[!include[banner](../includes/banner.md)]

Sie können Electronic Reporting (ER) Modellzuordnungen so konfigurieren, dass sie ein generisches ER-Datenmodell implementieren, aber spezifisch für Dynamics 365 Finance sind. In diesem Thema wird erläutert, wie Sie mehrere ER-Modellzuordnungen für ein ER-Datenmodell entwerfen, um zu steuern, wie sie von entsprechenden ER-Formaten verwendet werden, die von Unternehmen mit unterschiedlichen Länder-/Regionalkontexten betrieben werden.

## <a name="prerequisites"></a>Voraussetzungen

Um die Beispiele in diesem Thema abzuschließen, müssen Sie den folgenden Zugriff haben:

- Zugriff auf Finance für eine der folgenden Rollen:
    - Entwickler für elektronische Berichterstellung
    - Funktionaler Berater für elektronische Berichterstellung
    - Systemadministrator

- Zugriff auf die Instanz von Regulatory Configuration Services (RCS), die für den gleichen Mandanten wie Finance für eine der folgenden Rollen bereitgestellt wurde:
    - Entwickler für elektronische Berichterstellung
    - Funktionaler Berater für elektronische Berichterstellung
    - Systemadministrator

Einige Schritte in diesem Thema erfordern die Ausführung eines ER-Formats. In einigen Fällen wird die Ausführung eines ER-Formats durch den Länder-/Regionalkontext des Unternehmens beeinflusst, bei dem Sie derzeit angemeldet sind. Sie können ein ER-Format in der aktuellen RCS-Instanz ausführen, wenn die Firma, die den erforderlichen Länder-/Regionskontext hat, im RCS verfügbar ist. Andernfalls müssen Sie eine fertige Version der ER-Modellzuordnung und ER-Formatkonfigurationen, die das ER-Datenmodell verwenden, in Ihre Finance-Instanz hochladen und dann das ER-Format in dieser Finance-Instanz ausführen. Informationen zum Importieren von Konfigurationen, die sich im RCS befinden, in eine Finance-Instanz finden Sie unter [Importieren von Konfigurationen aus RCS](rcs-download-configurations.md).

## <a name="single-model-mapping-case"></a>Einzelmodell-Zuordnung Fall

Führen Sie die Schritte in [Anhang 1](#appendix1) zu diesem Thema aus, um die erforderlichen ER-Komponenten zu entwerfen. Sie haben nun die **Zuordnung (Allgemein)** Modellzuordnungskonfiguration, die das Modellzuordnung für die Definition **Eingangspunkt 1** enthält.

![EB-Konfigurationsseite.](./media/RCS-Context-specific-mapping-Tree.PNG)

### <a name="run-the-configured-format"></a>Ausführen des konfigurierten Formats

1.  Wählen Sie auf der Seite **Konfigurationen**, auf der Seite **Versionen** Inforegister **Ausführen**.
2.  Wählen Sie **OK**.

Beachten Sie, dass der Webbrowser anbietet, die Textdatei herunterzuladen, die durch das ausgeführte ER-Format erzeugt wurde. Da dieses Format für die Verwendung der Definition **Eingangspunkt 1** konfiguriert wurde und für das Basismodell derzeit nur ein einziges Modellmapping verfügbar ist, das ein Zuordnung für diese Definition enthält, verwendete das ausgeführte ER-Format das **Zuordnung (Allgemein)**-Modellmapping der Konfiguration **Zuordnung (Allgemein)** als Datenquelle. Daher enthält die heruntergeladene Datei den Text **Generische Funktionalität 1**.

## <a name="multiple-shared-model-mappings-case"></a>Fall von mehreren gemeinsamen Modellzuordnungen

Führen Sie die Schritte in [Anhang 2](#appendix2) zu diesem Thema aus, um die erforderlichen ER-Komponenten zu entwerfen. Sie haben nun **Zuordnung (Allgemein)** und **Zuordnung (Allgemein) benutzerdefinierte** Modellzuordnungskonfigurationen, von denen jede die Modellzuordnung für die Definition von **Einstiegspunkt 1** enthält.

![EB-Konfigurationsseite.](./media/RCS-Context-specific-mapping-TreeCustom.PNG)

### <a name="run-the-configured-format"></a>Ausführen des konfigurierten Formats

1.  Wählen Sie auf der Seite **Konfigurationen** im Konfigurationsbaum **Format, um Zuordnung zu lernen**.
2.  Wählen Sie im Inforegister **Versionen** **Ausführen** aus.
3.  Wählen Sie **OK**.

Beachten Sie, dass die Ausführung des ausgewählten ER-Formats erfolglos ist. Eine Fehlermeldung informiert Sie darüber, dass es mehr als ein Modellzuordnung für das **Modell zum Erlernen von Zuordnungs** Modell und den **Einstiegspunkt 1** Definition in den Konfigurationen **Zuordnung (Allgemein)** und **Zuordnung (Allgemein) benutzerdefiniert** Modellzuordnung gibt. Die Meldung empfiehlt auch, dass Sie eine dieser Konfigurationen als Standardkonfiguration auswählen.

![EB-Konfigurationsseite.](./media/RCS-Context-specific-mapping-FormatRunCustomFailed.PNG)

### <a name="define-a-default-mapping-configuration"></a>Definieren Sie eine Standardzuordnungskonfiguration.

Führen Sie diese Schritte aus, um die Konfiguration **Zuordnung (Allgemein) custom** Modellzuordnung als Standardkonfiguration zu definieren, so dass ihre Zuordnungen als Datenquellen für das ER-Format **Format verwendet werden können, um Zuordnungen zu lernen**.

1.  Wählen Sie auf der Seite **Konfigurationen** im Konfigurationsbaum **Zuordnung (Allgemein) benutzerdefiniert**.
2.  Wählen Sie bei Bedarf **Bearbeiten**, um die aktuelle Seite für die Bearbeitung bereit zu machen.
3.  Hier können Sie die Option **Standard für Modellzuordnung** auf **Ja** festlegen.
4.  Wählen Sie **Speichern** aus.

![EB-Konfigurationsseite.](./media/RCS-Context-specific-mapping-MappingsCustomDefault.PNG)

### <a name="run-the-configured-format"></a>Ausführen des konfigurierten Formats

1.  Wählen Sie auf der Seite **Konfigurationen** im Konfigurationsbaum **Format, um Zuordnung zu lernen**.
2.  Wählen Sie im Inforegister **Versionen** **Ausführen** aus.
3.  Wählen Sie **OK**.

Beachten Sie, dass die Ausführung des ausgewählten ER-Formats erfolgreich ist. Der Webbrowser bietet den Download der Textdatei an, die im ausgeführten ER-Format erzeugt wurde. Da dieses Format konfiguriert wurde, um die Definition des **Eingangspunkts 1** zu verwenden, und die Konfiguration des **Zuordnung (Allgemein) benutzerdefiniert** Modellzuordnung als Standardkonfiguration ausgewählt wurde, verwendete das ausgeführte ER-Format die Kopie **Zuordnung (Allgemein)** Modellzuordnung der Konfiguration **Zuordnung (Allgemein) benutzerdefiniert** als Datenquelle. Daher enthält die heruntergeladene Datei den Text **Generische Funktionalität 1 benutzerdefiniert**.

> [!NOTE]
> Wenn Sie die Firma, bei der Sie aktuell angemeldet sind, ändern und dieses ER-Format erneut ausführen, erhalten Sie den gleichen Inhalt in der generierten Datei, da die standardmäßige ER-Modellzuordnungskonfiguration keine unternehmensabhängigen Einschränkungen enthält.

## <a name="multiple-mixed-model-mappings-case"></a>Mehrere gemischte Modellzuordnungen Fallbeispiele

Führen Sie die Schritte in [Anhang 3](#appendix3) zu diesem Thema aus, um die erforderlichen ER-Komponenten zu entwerfen. Sie haben nun **Zuordnung (Allgemein)**, **Zuordnung (Allgemein) benutzerdefiniert** und **Zuordnung (FR) Modellzuordnung** Konfigurationen, die die Modellzuordnung für die Definition von **Einstiegspunkt 1** enthalten.

Beachten Sie, dass die Version 1 der Modellzuordnungskonfiguration **Zuordnung (FR)** so konfiguriert ist, dass sie nur für ER-Formate des **Modells gilt, um Zuordnung Modell zu lernen**, die in Finance-Firmen ausgeführt werden, die einen französischen Länder/Regionen-Kontext haben.

![EB-Konfigurationsseite.](./media/RCS-Context-specific-mapping-TreeFR.PNG)

### <a name="run-the-configured-format"></a>Ausführen des konfigurierten Formats

1.  Ändern Sie die Firma auf **FRSI**.
2.  Wählen Sie auf der Seite **Konfigurationen** im Konfigurationsbaum **Format, um Zuordnung zu lernen**.
3.  Wählen Sie im Inforegister **Versionen** **Ausführen** aus.
4.  Wählen Sie **OK**.

Beachten Sie, dass die Ausführung des ausgewählten ER-Formats erfolgreich ist. Der Webbrowser bietet den Download der Textdatei an, die durch das ausgeführte ER-Format erzeugt wurde. Da dieses Format konfiguriert wurde, um die Definition des **Eingangspunkts 1** zu verwenden, und die Konfiguration des **Zuordnung (Allgemein) benutzerdefiniert** Modellzuordnung als Standardkonfiguration ausgewählt wurde, verwendete das ausgeführte ER-Format die Kopie **Zuordnung (Allgemein)** Modellzuordnung der Konfiguration **Zuordnung (Allgemein) benutzerdefiniert** als Datenquelle. Daher enthält die heruntergeladene Datei den Text **Generische Funktionalität 1 benutzerdefiniert**.

### <a name="define-the-france-specific-mapping-configuration-as-the-default-configuration"></a>Definieren Sie die Frankreich-spezifische Zuordnung als Standardkonfiguration.

Führen Sie diese Schritte aus, um die benutzerdefinierte **Zuordnung (FR)** Modellzuordnungskonfiguration als Standardkonfiguration zu definieren. Beachten Sie, dass diese Zuordnung spezifisch für Frankreich ist und daher als Standardzuordnung zwischen allen Modellzuordnungskonfigurationen betrachtet wird, bei denen der Ländercode **FR** im Feld **ISO Länder-/Regionscodes** angegeben ist.

1.  Wählen Sie auf der Seite **Konfigurationen** im Konfigurationsbaum **Zuordnung (FR)**.
2.  Wählen Sie bei Bedarf **Bearbeiten**, um die aktuelle Seite für die Bearbeitung bereit zu machen.
3.  Hier können Sie die Option **Standard für Modellzuordnung** auf **Ja** festlegen.
4.  Wählen Sie **Speichern** aus.

![EB-Konfigurationsseite.](./media/RCS-Context-specific-mapping-TreeFRDefault.PNG)

### <a name="run-the-configured-format"></a>Ausführen des konfigurierten Formats

1.  Wählen Sie auf der Seite **Konfigurationen** im Konfigurationsbaum **Format, um Zuordnung zu lernen**.
2.  Wählen Sie im Inforegister **Versionen** **Ausführen** aus.
3.  Wählen Sie **OK**.

Beachten Sie, dass die Ausführung des ausgewählten ER-Formats erfolgreich ist. Der Webbrowser bietet den Download der Textdatei an, die durch das ausgeführte ER-Format erzeugt wurde. Da dieses Format konfiguriert wurde, um die Definition des **Eingangspunkts 1** zu verwenden, und die Konfiguration des **Zuordnung (FR)**-Modellzuordnung als Standardkonfiguration ausgewählt wurde, verwendete das ausgeführte ER-Format das **Zuordnung (FR)**-Modellzuordnung der Konfiguration des **Zuordnung (FR)** als Datenquelle. Daher enthält die heruntergeladene Datei den Text **FR-Funktionalität 1**.

> [!NOTE]
> Wenn Sie die Firma, bei der Sie derzeit angemeldet sind, ändern und dieses ER-Format erneut ausführen, hängt die Ausgabe vom Länder-/Regionskontext des ausgewählten Unternehmens ab.

## <a name="other-model-mapping-cases"></a>Andere Modellzuordnungsfälle

Wie Sie gesehen haben, funktioniert die Auswahl einer Modellzuordnung für die Ausführung eines ER-Formats wie folgt:

- Die Modellzuordnungsdefinition, die ein ER-Format verwendet, wird angegeben (**Eingabepunkt 1** in den Beispielen in diesem Thema).
- Alle Zuordnungskonfigurationen, die eine Zuordnung enthalten, die die angegebene Definition hat und die alle konfigurierten Kontextbeschränkungen für Länder und Regionen erfüllen, können potenziell zur Ausführung des ER-Formats verwendet werden (**Zuordnung (Allgemein)**, **Zuordnung (Allgemein) benutzerdefiniert**, und **Zuordnung (FR)** in den Beispielen in diesem Thema).
- Jedes standardmäßige Modellzuordnung mit Kontextbeschränkungen für Länder und Regionen hat die höchste Priorität für die Auswahl (**Zuordnung (FR)** in den Beispielen in diesem Thema).
- Alle Standardmodellzuordnungen, die keine Kontextbeschränkungen für Länder und Regionen haben, haben die nächsthöhere Priorität für die Auswahl (**Zuordnung (Allgemein) benutzerdefiniert**).
- Alle Modellzuordnungen, die Kontextbeschränkungen für Länder und Regionen haben, haben eine höhere Priorität für die Auswahl als Modellzuordnungen, die keine Kontextbeschränkungen für Länder und Regionen haben.

Die folgende Tabelle gibt Auskunft über die Ergebnisse der Modellzuordnungsauswahl für alle möglichen Fälle von Modellzuordnungseinstellungen:

- Spalte 1 zeigt an, ob die erste Modellzuordnung, die keine Kontextbeschränkungen für Länder/Regionen aufweist (z.B. die gemeinsame Zuordnung **Zuordnung (Allgemein)**) dargestellt wird und, wenn ja, ob die Option **Standard für Modellzuordnung** auf **Ja** gesetzt ist.
- Spalte 2 zeigt an, ob die zweite Modellabbildung, die keine Kontextbeschränkungen für Länder/Regionen aufweist (z.B. die gemeinsame **Zuordnung (allgemein) benutzerdefiniert**-Zuordnung), dargestellt wird und, wenn ja, ob die Option **Standard für Zuordnung** auf **Ja** für sie gesetzt ist.
- Spalte 3 zeigt an, ob die erste Modellzuordnung mit Kontextbeschränkungen für Land/Region A (z.B. das Frankreich-spezifische **Zuordnung (FR)** Zuordnung) dargestellt wird und, wenn ja, ob die Option **Standard für Modellzuordnung** auf **Ja** gesetzt ist.
- Spalte 4 zeigt an, ob die zweite Modellzuordnung mit Kontextbeschränkungen für Land/Region A dargestellt wird und, wenn ja, ob die Option **Standard für Modellzuordnung** auf **Ja** für sie gesetzt ist.
- Spalte 5 zeigt das Ergebnis einer Modellzuordnungsauswahl für die Ausführung eines ER-Formats unter der Kontrolle eines Unternehmens, das einen Kontext zwischen Land und Region A hat.
- Spalte 6 zeigt das Ergebnis einer Modellzuordnungsauswahl für die Ausführung eines ER-Formats unter der Kontrolle eines Unternehmens, das den Kontext Land / Region B hat.

In der Tabelle zeigt ein Pluszeichen (+) das Vorhandensein einer Modellzuordnungskonfiguration in der aktuellen Instanz des Dienstes Microsoft Azure an, der zum Ausführen eines ER-Formats (entweder Finance oder RCS) verwendet wird.

| Behälter | Modellzuordnung 1 ohne Länder-/Regionskontext (MM1) | Modellzuordnung 2 ohne Länder-/Regionskontext (MM2) | Modellzuordnung 1 mit Land/Region A Kontext (MM1A) | Modellzuordnung 2 mit Land/Region A-Kontext (MM2A) | Unter der Kontrolle eines Unternehmens ausführen, das einen Kontext zwischen Land/Region A hat. | Unter der Kontrolle eines Unternehmens ausführen, das den Kontext Land / Region B hat. |
|---------|---------|---------|---------|---------|---------------------------|----------------------------|
|         |     1   |     2   |    3    |    4    |           5               |            6               |
|     1   |         |         |         |         | Fehler (fehlende Zuordnung)   | Fehler (fehlende Zuordnung)    |
|     2   |     +   |         |         |         | MM1                       | MM1                        |
|     3   |     +   |     +   |         |         | Fehler (mehrere Zuordnungen) | Fehler (mehrere Zuordnungen)  |
|     4   |     +   |         |    +    |         | MM1A                      | MM1                        |
|     5   |     +   |         |    +    |    +    | Fehler (mehrere Zuordnungen) | MM1                        |
|     6   |     +   | Standard |    +    |    +    | MM2                       | MM2                        |
|     7   |     +   |         | Standard |         | MM1A                      | MM1                        |
|     8   |     +   |         | Standard |    +    | MM1A                      | MM1                        |
|     9   |     +   |         | Standard | Standard | Fehler (mehrere Zuordnungen) | MM1                        |
|    10   | Standard |         |         |         | MM1                       | MM1                        |
|    11   | Standard |    +    |         |         | MM1                       | MM1                        |
|    12   | Standard |         |    +    |         | MM1                       | MM1                        |
|    13   | Standard | Standard |         |         | Fehler (mehrere Zuordnungen) | Fehler (mehrere Zuordnungen)  |
|    14   | Standard |         | Standard |         | MM1A                      | MM1                        |
|    15   | Standard |         | Standard | Standard | MM1A                      | MM2A                       |
|    16   |         |         |    +    |    +    | MM1A                      | MM2A                       |
|    17   |         |         | Standard | Standard | MM1A                      | MM2A                       |

## <a name="learn-what-mapping-was-used-in-the-execution-of-an-er-format"></a>Erfahren Sie, mit welcher Zuordnung ein ER-Format ausgeführt wurde.

### <a name="configure-er-user-parameters"></a>Benutzerparameter der elektronischen Berichterstellung konfigurieren

1.  Wählen Sie auf der Seite **Konfigurationen**, im Aktionsbereich, auf der Registerkarte **KONFIGURATIONEN** **Benutzerparameter**.
2.  Legen Sie die Option **In Debugmodus ausführen** auf **Ja** fest.
4.  Wählen Sie **Ok**.

### <a name="run-the-configured-format"></a>Ausführen des konfigurierten Formats

1.  Wählen Sie auf der Seite **Konfigurationen** im Konfigurationsbaum **Format, um Zuordnung zu lernen**.
2.  Wählen Sie im Inforegister **Versionen** **Ausführen** aus.
3.  Wählen Sie **Ok**.

### <a name="review-the-er-debug-log"></a>Überprüfen Sie das ER-Debug-Protokoll.

1.  Gehen Sie im Navigationsbereich zu **Module \> Organisationsverwaltung \> Elektronische Berichterstattung \> Konfiguration Debug-Log**.
2.  Wählen Sie die Schaltfläche **Diese Seite neu laden**.

![EB-Ausführungsprotokolle-Seite.](./media/RCS-Context-specific-mapping-DebugLog.PNG)

Beachten Sie, dass dem ER-Debug-Protokoll für das ausgeführte ER-Format ein neuer Datensatz hinzugefügt wurde. Da das Feld **Level** dieses Datensatzes auf **Info** gesetzt ist, ist der Datensatz informativ. Da das Feld Formatkomponente auf **Zuordnugnskonfiguration** gesetzt ist, informiert Sie der Datensatz über ein Model-Zuordnung, das während der Ausführung des **Formats zum Erlernen von Zuordnungen** ER-Format verwendet wurde (ausgewählt im Feld **Konfigurationsname**). Der Inhalt des Feldes **Generierter Text** informiert Sie darüber, dass die Zuordnungs-Komponente **Zuordnung (FR)**, die sich in der Konfiguration **Zuordnung (FR)** befindet, zur Ausführung dieses Berichts verwendet wurde.

## <a name="appendix-1"></a><a name="appendix1"></a> Anhang 1

### <a name="configure-a-sample-data-model"></a>Konfigurieren eines Beispieldatenmodells

Melden Sie sich bei Ihrer RCS-Instanz an.

In diesem Beispiel erstellen Sie eine Konfiguration für die Musterfirma Litware, Inc. Um diese Schritte abzuschließen, müssen Sie zunächst im RCS die Schritte in der Prozedur [Anlegen eines Konfigurationsanbieters durchführen und ihn als aktiv](tasks/er-configuration-provider-mark-it-active-2016-11.md) markieren.

#### <a name="create-an-er-data-model-configuration"></a>Erstellen einer ER-Datenmodell-Konfiguration

1.  Wählen Sie im Standard-Dashboard **Elektronische Berichterstellung** aus.
2.  Wählen Sie die Kachel **Berichtskonfigurationen**.
3.  Wählen Sie auf der Seite **Konfigurationen** **Konfiguration erstellen**.
4.  Geben Sie im Dropdown-Dialogfeld im Feld **Name** **Modell ein, um Zuordnungen zu lernen**.
5.  Wählen Sie **Konfiguration erstellen**.
6.  Wählen Sie die Option **Konfigurationskomponenten** Inforegister.

Beachten Sie, dass der Entwurf der Version 1 dieser ER-Konfiguration zur Bearbeitung bereit ist. Diese Version enthält die Datenmodellkomponente.

#### <a name="design-a-sample-data-model"></a>Entwurf eines Beispieldatenmodells

1.  Wählen Sie auf der Seite **Konfigurationen** **Designer**.
2.  Wählen Sie **Neu** aus.
3.  Geben Sie im Dropdown-Dialogfeld im Feld **Name** **Eingabepunkt 1** ein.
4.  Wählen Sie **Hinzufügen** aus.
5.  Wählen Sie **Neu** aus.
6.  Geben Sie im Dropdown-Dialogfeld im Feld **Name** **Funktionsbeschreibung** ein.
7.  Wählen Sie **Hinzufügen** aus.
8.  Wählen Sie **Neu** aus.
9.  Wählen Sie im Dropdown-Dialogfeld in der Feldgruppe **Neuer Knoten** die Option **Modellstamm**.
10. Geben Sie im Feld **Name** **Eingabepunkt 2** ein.
11. Wählen Sie **Eingabepunkt 2**.
12. Wählen Sie **Hinzufügen** aus.
13. Wählen Sie **Neu** aus.
14. Geben Sie im Dropdown-Dialogfeld im Feld **Name** **Funktionsbeschreibung** ein.
15. Wählen Sie **Hinzufügen** aus.

    ![EB-Datenmodelldesignerseite.](./media/RCS-Context-specific-mapping-Model.PNG)

16. Wählen Sie **Speichern** aus.
17. Schließen Sie die Seite.

#### <a name="complete-the-modified-version-of-the-model-configuration"></a>Vervollständigen Sie die modifizierte Version der Modellkonfiguration.

1.  Wählen Sie auf der Seite **Konfigurationen**, auf der Seite **Versionen** Inforegister **Status ändern**.

    > Ändern Sie den Status der entworfenen Modellkonfiguration von **Entwurf** auf **Erledigt**, so dass damit die erforderlichen Modellzuordnungen und Formate entworfen werden können.

2.  Wählen Sie **Abgeschlossen** aus.
3.  Wählen Sie **OK**.

Beachten Sie, dass die von Ihnen erstellte Konfiguration als fertige Version 1 gespeichert wird.

### <a name="configure-a-sample-model-mapping"></a>Konfigurieren einer exemplarischen Modellzuordnung

#### <a name="create-an-er-model-mapping-configuration"></a>Erstellen einer ER-Modellzuordnung Konfiguration

1.  Wählen Sie auf der Seite **Konfigurationen** **Konfiguration erstellen**.
2.  Wählen Sie im Dropdown-Dialogfeld in der Feldgruppe **Neu** die Option **Modellzuordnung basierend auf dem Datenmodell Modell, um Zuordnungen zu lernen**.
3.  Geben Sie im Feld **Name** **Zuordnung (Allgemein)** ein.
4.  Wählen Sie im Feld **Datenmodelldefinition** **Eingabepunkt 1**.
5.  Wählen Sie **Konfiguration erstellen**.

Beachten Sie, dass der Entwurf der Version 1 dieser ER-Konfiguration zur Bearbeitung bereit ist. Diese Version enthält die Modellzuordnungskomponente.

#### <a name="design-a-sample-model-mapping"></a>Entwurf einer exemplarischen Modellzuordnung

1.  Wählen Sie auf der Seite **Konfigurationen** die Option **Designer** aus.

    Beachten Sie, dass die Modellzuordnung des Richtungstyps **Zum Modell** für die Definition von **Eingangspunkt 1** automatisch zu dieser Komponente hinzugefügt wurde.
    
2.  Wählen Sie **Designer**, um mit der Bearbeitung der hinzugefügten Modellzuordnung zu beginnen.
3.  Wählen Sie im Abschnitt **Datenmodell** **Bearbeiten**.
4.  Geben Sie im Feld **Formel** **„Generische Funktionalität 1“** ein.
5.  Wählen Sie **Speichern**.
6.  Schließen Sie die Seite **Formeldesigner**.

    ![Seite „EB-Modellzuordnungsdesigner“.](./media/RCS-Context-specific-mapping-Mapping1.PNG)

7.  Wählen Sie **Speichern** aus.
8.  Schließen Sie die Seite **Modellzuordnungsdesigner**.
9.  Wählen Sie **Neu** aus.
10. Wählen Sie im Feld **Definition** **Eingabepunkt 2**.
11. Geben Sie im Feld **Name** **Zuordnung (Allgemein) 2** ein.
12. Wählen Sie **Designer** aus.
13. Wählen Sie im Abschnitt **Datenmodell** **Bearbeiten**.
14. Geben Sie im Feld **Formel** **„Generische Funktionalität 2“** ein.
15. Wählen Sie **Speichern**.
16. Schließen Sie die Seite **Formeldesigner**.

    ![Seite „EB-Modellzuordnungsdesigner“.](./media/RCS-Context-specific-mapping-Mapping2.PNG)

17. Wählen Sie **Speichern** aus.
18. Schließen Sie die Seite **Modellzuordnungsdesigner**.

    ![Seite mit den Zuordnungen von EB-Modellen.](./media/RCS-Context-specific-mapping-Mappings.PNG)

19. Schließen Sie die Seite **Modellzuordnungen**.

#### <a name="complete-the-modified-version-of-the-model-mapping-configuration"></a>Vervollständigen Sie die modifizierte Version der Modellzuordnungskonfiguration.

1.  Wählen Sie auf der Seite **Konfigurationen**, auf der Seite **Versionen** Inforegister **Status ändern**.

    > Ändern Sie den Status der Konfiguration der entworfenen Modellzuordnung von **Entwurf** auf **Abgeschlossen**, so dass sie von ER-Formaten verwendet werden kann.

2.  Wählen Sie **Abgeschlossen** aus.
3.  Wählen Sie **OK**.

Beachten Sie, dass die erstellte Konfiguration als fertige Version 1 gespeichert wird.

### <a name="configure-a-sample-format"></a>Konfigurieren eines Beispielformats

#### <a name="create-an-er-format-configuration"></a>Erstellen einer ER-Format-Konfiguration

1.  Wählen Sie auf der Seite **Konfigurationen** im Konfigurationsbaum **Modell, um Zuordnungen zu lernen**.
2.  Wählen Sie **Konfiguration erstellen**.
3.  Wählen Sie im Dropdown-Dialogfeld in der Feldgruppe **Neu** die Option **Format basierend auf dem Datenmodell Modell, um Zuordnungen zu lernen**.
4.  Geben Sie im Feld **Name** **Format ein, um Zuordnungen zu lernen**.
5.  Wählen Sie im Feld **Datenmodelldefinition** **Eingabepunkt 1**.
6.  Wählen Sie **Konfiguration erstellen**.

Beachten Sie, dass der Entwurf der Version 1 dieser ER-Konfiguration zur Bearbeitung bereit ist. Diese Version enthält die Formatkomponente.

#### <a name="design-a-sample-format"></a>Entwurf eines Musterformats

1.  Wählen Sie auf der Seite **Konfigurationen** die Option **Designer** aus.
2.  Wählen Sie **Stamm hinzufügen** aus.
3.  Wählen Sie in der Gruppe **Text** das Element **String**.
4.  Wählen Sie **OK**.

#### <a name="bind-format-elements-to-a-data-source"></a>Binden von Formatelementen an eine Datenquelle

1.  Erweitern Sie auf der Seite **Format Designer**, auf der Registerkarte **Zuordnung** die Modelldatenquelle.
2.  Wählen Sie das Feld **Funktionsbeschreibung**.
3.  Wählen Sie **Bindung** aus.

    ![EB-Formatdesignerseite.](./media/RCS-Context-specific-mapping-Format.PNG)

4.  Wählen Sie **Speichern** aus.
5.  Schließen Sie die Seite.

## <a name="appendix-2"></a><a name="appendix2"></a> Anhang 2

### <a name="configure-a-sample-model-mapping-for-general-customization"></a>Konfigurieren einer exemplarischen Modellzuordnung für allgemeine Anpassungen

Möglicherweise möchten Sie eine Modellzuordnung anpassen, die Ihnen ein Konfigurationsanbieter (Partner) zur Verfügung gestellt hat, und dann die angepasste Version als Datenquelle für Ihre ER-Formate verwenden. In diesem Fall müssen Sie eine benutzerdefinierte ER-Modellzuordnungskonfiguration erstellen, um die erforderlichen Änderungen an bestehenden Modellzuordnungen vorzunehmen. Die Verfahren in diesem Anhang verwenden als Beispiel das **Zuordnung (Allgemein)** Modellzuordnung.

#### <a name="create-an-er-model-mapping-configuration"></a>Erstellen einer ER-Modellzuordnung Konfiguration

1.  Wählen Sie auf der Seite **Konfigurationen** im Konfigurationsbaum **Zuordnung (Allgemein)**.
2.  Wählen Sie **Konfiguration erstellen**.
3.  Wählen Sie im Dropdown-Dialogfeld in der Feldgruppe **Neu** die Option **Aus Name ableiten: Zuordnung (Allgemein), Litware, Inc.**.
4.  Geben Sie im Feld **Name** **Zuordnung (Allgemein) benutzerdefiniert** ein.
5.  Wählen Sie **Konfiguration erstellen**.

Beachten Sie, dass der Entwurf der Version 1 dieser ER-Konfiguration zur Bearbeitung bereit ist.

#### <a name="design-a-sample-model-mapping"></a>Entwurf einer exemplarischen Modellzuordnung

1.  Wählen Sie auf der Seite **Konfigurationen** die Option **Designer** aus.

    > Beachten Sie, dass die Modellzuordnungen der Basiskonfiguration automatisch in diese Konfiguration kopiert wurden.

2.  Wählen Sie die Zuordnung **Zuordnung (Allgemein) Kopie**.
3.  Wählen Sie **Designer** aus.
4.  Wählen Sie im Abschnitt **Datenmodell** **Bearbeiten**.
5.  Geben Sie im Feld **Formel** **„Allgemeine Funktionalität 1 benutzerdefiniert“** ein.
6.  Wählen Sie **Speichern** aus.
7.  Schließen Sie die Seite.

    ![Seite „EB-Modellzuordnungsdesigner“.](./media/RCS-Context-specific-mapping-Mapping1Custom.PNG)

8.  Wählen Sie **Speichern** aus.
9.  Schließen Sie die Seite.
10. Wählen Sie die Zuordnung **Zuordnung (Allgemein) 2 Kopie** Zuordnung.
11. Wählen Sie **Designer** aus.
12. Wählen Sie im Abschnitt **Datenmodell** **Bearbeiten**.
13. Geben Sie im Feld **Formel** **„Allgemeine Funktionalität 2 benutzerdefiniert“** ein.
14. Wählen Sie **Speichern** aus.
15. Schließen Sie die Seite.

    ![Seite „EB-Modellzuordnungsdesigner“.](./media/RCS-Context-specific-mapping-Mapping2Custom.PNG)

16. Wählen Sie **Speichern** aus.
17. Schließen Sie die Seite.

    ![Seite mit den Zuordnungen von EB-Modellen.](./media/RCS-Context-specific-mapping-MappingsCustom.PNG)

18. Schließen Sie die Seite.

#### <a name="complete-the-modified-version-of-the-model-mapping-configuration"></a>Vervollständigen Sie die modifizierte Version der Modellzuordnungskonfiguration.

1.  Wählen Sie auf der Seite **Konfigurationen**, auf der Seite **Versionen** Inforegister **Status ändern**.

    > Ändern Sie den Status der Konfiguration der entworfenen Modellzuordnung von **Entwurf** auf **Abgeschlossen**, so dass sie von ER-Formaten verwendet werden kann.

2.  Wählen Sie **Abgeschlossen** aus.
3.  Wählen Sie **OK**.

Beachten Sie, dass die erstellte Konfiguration als fertige Version 1 gespeichert wird.

## <a name="appendix-3"></a><a name="appendix3"></a> Anhang 3

### <a name="configure-a-sample-model-mapping-for-countryregion-specific-customization"></a>Konfigurieren Sie eine Mustermodellzuordnung für länder- und regionalspezifische Anpassungen.

Für einige ER-Formate gibt es möglicherweise länderspezifische Anforderungen an die Datenaufbereitung. In diesem Fall können Sie eine separate ER-Modellzuordnungskonfiguration verwalten und die Umsetzung dieser länder- und regionalspezifischen Anforderungen von der allgemeinen Implementierung trennen. Die Verfahren in diesem Anhang verwenden das **Format, um Zuordnungen zu lernen** ER-Format und französisch-spezifische Anforderungen als Beispiel.

#### <a name="create-an-er-model-mapping-configuration"></a>Erstellen einer ER-Modellzuordnung Konfiguration

Erstellen Sie zunächst eine neue ER-Modellzuordnungskonfiguration, um die länder- und regionalspezifischen Anforderungen zu implementieren. Verwenden Sie Ihre benutzerdefinierte ER-Modellzuordnungskonfiguration als Basis.

1.  Wählen Sie auf der Seite **Konfigurationen** im Konfigurationsbaum **Zuordnung (Allgemein) benutzerdefiniert**.
2.  Wählen Sie **Konfiguration erstellen**.
3.  Wählen Sie im Dropdown-Dialogfeld in der Feldgruppe **Neu** die Option **Aus Name ableiten: Zuordnung (allgemein) benutzerdefiniert, Litware, Inc**.
4.  Geben Sie im Feld **Name** **Zuordnung(FR)** ein.
5.  Wählen Sie **Konfiguration erstellen**.

Beachten Sie, dass der Entwurf der Version 1 dieser ER-Konfiguration zur Bearbeitung bereit ist.

#### <a name="design-a-sample-model-mapping"></a>Entwurf einer exemplarischen Modellzuordnung

1.  Wählen Sie auf der Seite **Konfigurationen** die Option **Designer** aus.

    > Beachten Sie, dass Modell-Zuordnungs der Basiskonfiguration automatisch in diese Konfiguration kopiert wurden.

2.  Wählen Sie die Zuordnung **Zuordnung(Allgemein) Kopie Kopie**.
3.  Benennen Sie es um **Zuordnung (FR)**.
4.  Wählen Sie **Designer** aus.
5.  Wählen Sie im Abschnitt **Datenmodell** **Bearbeiten**.
6.  Geben Sie im Feld **Formel** **„FR Funktionalität 1“** ein.
7.  Wählen Sie **Speichern** aus.
8.  Schließen Sie die Seite.

    ![Seite „EB-Modellzuordnungsdesigner“.](./media/RCS-Context-specific-mapping-Mapping1FR.PNG)

9.  Wählen Sie **Speichern** aus.
10. Schließen Sie die Seite.
11. Wählen Sie die Zuordnung **Zuordnung (Allgemein) 2 Kopie Kopie Kopie**.
12. Benennen Sie es um **Zuordnung (FR) 2**.
13. Wählen Sie **Designer** aus.
14. Wählen Sie im Abschnitt **Datenmodell** **Bearbeiten**.
15. Geben Sie im Feld **Formel** **„FR-Funktionalität 2“** ein.
16. Wählen Sie **Speichern** aus.
17. Schließen Sie die Seite.

    ![Seite „EB-Modellzuordnungsdesigner“.](./media/RCS-Context-specific-mapping-Mapping2FR.PNG)

18. Wählen Sie **Speichern** aus.
19. Schließen Sie die Seite.

    ![Seite mit den Zuordnungen von EB-Modellen.](./media/RCS-Context-specific-mapping-MappingsFR.PNG)

20. Schließen Sie die Seite.

#### <a name="specify-countryregion-context-restrictions-for-use"></a>Spezifizieren Sie Kontextbeschränkungen für Länder/Regionen für die Verwendung.

1.  Wählen Sie auf der Seite **Konfigurationen**, auf der Seite **ISO Länder-/Regionscodes** Inforegister **Neu**.
2.  Wählen Sie im Feld **ISO** **FR**.
3.  Wählen Sie **Speichern**.

Beachten Sie, dass Sie sich bei einer bestimmten Firma in Finance anmelden müssen, um ein ER-Format auszuführen. Daher kann dieses Unternehmen als eine Partei betrachtet werden, die sowohl die Ausführung des ER-Formats als auch die Auswahl des richtigen ER-Modells für die Zuordnung des Basis-ER-Datenmodells steuert. Durch Hinzufügen des Ländercodes **FR** legen Sie fest, dass diese Modellzuordnung nur dann zur Auswahl durch ein ER-Format des Basisdatenmodells zur Verfügung steht, wenn dieses Format unter der Kontrolle eines Unternehmens mit französischem Länder/Regionalkontext ausgeführt wird.

Sie können mehrere Länder-/Regionscodes für eine einzelne Version einer ER-Modellzuordnungskonfiguration hinzufügen. Auf diese Weise können Modellzuordnungen, die sich in dieser Modellzuordnungskonfiguration befinden, für ein ER-Format verwendet werden, das unter der Kontrolle von Unternehmen mit einem anderen Länder-/Regionskontext ausgeführt wird.

Beachten Sie, dass die Liste der Länder-/Regionscodes für jede Version einer ER-Modellzuordnungskonfiguration angegeben ist und von Version zu Version variieren kann.

#### <a name="complete-the-modified-version-of-the-model-mapping-configuration"></a>Vervollständigen Sie die modifizierte Version der Modellzuordnungskonfiguration.

1.  Wählen Sie auf der Seite **Konfigurationen**, auf der Seite **Versionen** Inforegister **Status ändern**.

    > Ändern Sie den Status der Konfiguration der entworfenen Modellzuordnung von **Entwurf** auf **Abgeschlossen**, so dass sie von ER-Formaten verwendet werden kann.

2.  Wählen Sie **Abgeschlossen** aus.
3.  Wählen Sie **OK**.

Beachten Sie, dass die erstellte Konfiguration als fertige Version 1 gespeichert wird.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Überblick über die elektronische Berichterstellung (Electronic reporting, ER)](general-electronic-reporting.md)

[ER-Modellzuordnungen in separaten ER-Konfigurationen verwalten](./tasks/er-manage-model-mapping-configurations-july-2017.md)

[Landes-/Regionskontext anwenden](../lcs-solutions/apply-country-context.md)

## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen

#### <a name="i-configured-two-shared-er-model-mapping-configurations-in-rcs-and-marked-one-of-them-as-the-default-model-mapping-configuration-i-successfully-ran-an-er-format-that-was-created-for-the-same-base-er-data-model-configuration-to-test-model-mappings-i-then-imported-the-whole-er-solution-er-data-model-two-er-model-mapping-configurations-and-er-format-configuration-into-finance-why-do-i-receive-an-error-message-when-i-try-to-run-the-same-er-format-in-finance"></a>Ich habe zwei gemeinsame ER-Modellzuordnungskonfigurationen in RCS konfiguriert und eine davon als Standardmodellzuordnungskonfiguration markiert. Ich habe erfolgreich ein ER-Format ausgeführt, das für die gleiche Basis-ER-Datenmodellkonfiguration erstellt wurde, um Modellzuordnungen zu testen. Dann importierte ich die gesamte ER-Lösung (ER-Datenmodell, zwei ER-Modellzuordnungskonfigurationen und ER-Format-Konfiguration) in Finance. Warum erhalte ich eine Fehlermeldung, wenn ich versuche, das gleiche ER-Format in Finance auszuführen?
Die Standardeinstellung für die Modellzuordnung ist umgebungsspezifisch. Es ist in RCS konfiguriert, wird aber nicht nach Finance exportiert. Um dieses ER-Format erfolgreich ausführen zu können, müssen Sie auch in Finance eine der ER-Modellzuordnungskonfigurationen als Standard-Modellzuordnungskonfiguration markieren.

#### <a name="i-configured-one-model-mapping-as-a-shared-model-mapping-and-completed-the-draft-version-of-it-i-then-added-a-new-model-mapping-configuration-for-same-data-model-and-configured-it-as-french-specific-why-is-the-shared-model-mapping-selected-when-i-run-an-er-format-even-though-this-er-format-uses-the-correct-root-definition-and-execution-is-done-under-the-control-of-the-company-that-has-french-countryregion-context"></a>Ich habe eine Modellzuordnung als Shared Model Zuordnung konfiguriert und den Entwurf der Version abgeschlossen. Dann habe ich eine neue Modellzuordnungskonfiguration für dasselbe Datenmodell hinzugefügt und als französisch-spezifisch konfiguriert. Warum wird das Shared Model Zuordnung ausgewählt, wenn ich ein ER-Format verwende, obwohl dieses ER-Format die richtige Root-Definition verwendet und die Ausführung unter der Kontrolle des Unternehmens erfolgt, das den französischen Länder/Regionen-Kontext hat?
Stellen Sie sicher, dass die Konfiguration der gemeinsamen Modellzuordnung nicht als Standardkonfiguration der Modellzuordnung gekennzeichnet ist. Andernfalls hat es bei der Zuordnungsauswahl eine höhere Priorität. Stellen Sie außerdem sicher, dass die französisch-spezifische Modellzuordnungskonfiguration berücksichtigt wird, wenn während der Ausführung des ER-Formats eine Zuordnung ausgewählt wird. Eine ER-Modellzuordnungskonfiguration steht nur dann zur Auswahl, wenn mindestens eine der folgenden Bedingungen erfüllt ist:
- Mindestens eine Version der ER-Modellzuordnungskonfiguration hat entweder den Status **Abgeschlossen** oder **Gemeinsam**. In diesem Fall wird die Version mit der höchsten Versionsnummer für die Ausführung des ER-Formats verwendet.
- Die Option **Entwurf ausführen** für die Konfiguration der ER-Modellzuordnung ist aktiviert. In diesem Fall wird die Version mit dem Status **Entwurf** für die Ausführung des ER-Formats verwendet.
> Die Option **Entwurf ausführen** wird auf der Seite **Konfigurationen** für jede ER-Modellzuordnungskonfiguration verfügbar, wenn der Benutzerparameter **Einstellung ausführen** ER eingeschaltet ist.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]