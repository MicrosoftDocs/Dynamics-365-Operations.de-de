---
title: Verwendung von DATA COLLECTION Datenquellen in elektronischen Berichtsformaten
description: In diesem Thema wird erklärt, wie Sie Datenquellen von DATA COLLECTION in elektronischen Berichtsformaten (ER) verwenden können.
author: NickSelin
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-01-01
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: 185fb9a33cb4cc655dfdf640b4c239d617426c64
ms.sourcegitcommit: d5d6b81bd8b08de20cc018c2251436065982489e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/17/2022
ms.locfileid: "8323900"
---
# <a name="use-data-collection-data-sources-in-electronic-reporting-formats"></a>Verwendung von DATA COLLECTION Datenquellen in elektronischen Berichtsformaten

[!include [banner](../includes/banner.md)]

Sie können den Vorgangsdesigner des Frameworks für die [Elektronische Berichterstellung (EB)](general-electronic-reporting.md) verwenden, um die Formatkomponente einer EB-Lösung zu konfigurieren, die dazu dient, ausgehende Belege in verschiedenen Formaten zu erzeugen. Die hierarchische Struktur der konfigurierten Formatkomponente besteht aus verschiedenen Typen von Formatelementen. Diese Formatelemente werden verwendet, um generierte Dokumente zur Laufzeit mit den erforderlichen Informationen zu füllen. Wenn Sie ein ER-Format ausführen, werden die Formatelemente standardmäßig in der Reihenfolge ausgeführt, in der sie in der Formathierarchie dargestellt sind: einzeln, von oben nach unten.

Wenn ER ein Formatelement ausführt, das eine Bindung enthält, wird die Formel dieser Bindung ausgeführt, und das Formatelement fügt den Wert zu einem generierten Beleg hinzu. Die Bindung kann zum Beispiel den Wert eines Datenmodell-Feldes an ein Formatelement übergeben. Sie können eine Datenquelle DATA COLLECTION so konfigurieren, dass sie Werte von Datenmodellfeldern zur Laufzeit sammelt, eine Wertesummierung durchführt und ein generiertes Dokument mit den gesammelten Werten füllt. Um diesen Ansatz zu verwenden, ändern Sie die initiale Bindung so, dass die konfigurierte Datenquelle DATA COLLECTION verwendet wird, um den Wert eines Datenmodellfelds an ein Formatelement zu übergeben. Durch die Übergabe von Werten über die Datenquelle DATA COLLECTION können Sie erforderliche Details zur weiteren Verwendung sammeln.

Wenn Sie eine DATA COLLECTION-Datenquelle konfigurieren, geben Sie einen Wertetyp an, der in der Datenquelle verwaltet werden soll. Die folgenden [Datentypen](er-formula-supported-data-types-primitive.md) werden derzeit für das Sammeln von Werten unterstützt:

- Aktiv
- Datum
- DateTime
- GUID
- Int64
- Ganzzahl
- Gleitkommazahl
- Zeichenfolge
- Uhrzeit

Sie können die `Collect(Value)`-Methode einer DATA COLLECTION-Datenquelle verwenden, um einen Wert zur Sammlung an eine Datenquelle zu übergeben. In dieser Methode ist das `Value`-Argument entweder eine Konstante oder der gültige Pfad eines Datenquellenfelds des betreffenden Datentyps.

Verwenden Sie die Eigenschaft `Result` einer Datenquelle DATA COLLECTION, um auf die Liste der gesammelten Werte zuzugreifen. Diese Eigenschaft gibt eine [Datensatzliste](er-formula-supported-data-types-composite.md#record-list) zurück. Die Datensätze der Datensatzliste enthalten das Feld `Value`, über das Sie auf die gesammelten Werte zugreifen können.

Standardmäßig sammelt eine DATA COLLECTION-Datenquelle nur eindeutige Werte.

Um alle Werte zu sammeln, legen Sie das Feld **Alle Werte sammeln** der konfigurierten DATA COLLECTION Datenquelle auf **Ja** fest. Wenn das Feld **Alle Werte sammeln** auf **Ja** festgelegt ist, wird die parametrisierte Eigenschaft `Sum(Flag)` verfügbar. Sie können diese Eigenschaft verwenden, um die Gesamtsumme aller aktuell gesammelten Werte zu erhalten. In dieser Eigenschaft ist das Argument `Flag` ein [Boolescher](er-formula-supported-data-types-primitive.md#boolean) Wert, mit dem angegeben wird, ob der Gesamtwert zurückgesetzt werden muss.

- Wenn der Wert **Falsch** angegeben wird, wird die Summierung ab dem zuvor gesammelten Betrag fortgesetzt.
- Wenn der Wert **True** bereitgestellt wird, wird eine neue Summierung gestartet.

Die folgenden Datentypen werden derzeit für die Summierung unterstützt:

- Int64
- Ganzzahl
- Gleitkommazahl

Um mehr über diese Funktion zu erfahren, führen Sie das folgende Beispiel aus.

## <a name="example-configure-an-er-format-to-do-counting-and-summing-by-using-a-data-collection-data-source"></a>Beispiel: Konfigurieren eines ER-Formats zum Zählen und Summieren unter Verwendung einer DATA COLLECTION-Datenquelle

Dieses Beispiel zeigt, wie ein Benutzer in der Rolle Systemadministrator oder Funktionsberater für elektronisches Reporting ein ER-Format konfigurieren kann, das über eine Datenquelle DATA COLLECTION verfügt, die zum Berechnen laufender Summen und zum Sammeln summierter Werte verwendet wird.

Die Vorgänge in diesem Beispiel können in der Firma USMF in Microsoft Dynamics 365 Finance abgeschlossen werden.

### <a name="upload-and-use-the-provided-er-solution"></a>Laden Sie die bereitgestellte ER-Lösung hoch und verwenden Sie sie

1. [Importieren Sie die EB-Beispielkonfigurationen](er-defer-sequence-element.md#import-the-sample-er-configurations).
2. [Aktivieren eines Konfigurationsanbieters](er-defer-sequence-element.md#activate-a-configurations-provider).
3. [Überprüfen Sie die importierte Modellzuordnung](er-defer-sequence-element.md#review-the-imported-model-mapping).
4. [Überprüfen Sie das importierte Format](er-defer-sequence-element.md#review-the-imported-format).
5. [Führen Sie das importierte Format aus](er-defer-sequence-element.md#run-the-imported-format).

### <a name="run-the-format-of-the-provided-er-solution"></a>Führen Sie das Format der bereitgestellten ER-Lösung aus

1. Wählen Sie auf der Seite **Formatdesigner** die Option **Ausführen** aus.
2. Wählen Sie im Dialogfeld **Elektronische Berichtsparameter** die Option **OK** aus.
3. Laden Sie die vom Webbrowser angebotene Datei herunter und öffnen Sie sie zur Überprüfung.

    ![Heruntergeladene Datei, die die Ergebnisse der ersten Formatausführung enthält](./media/er-data-collection-data-sources-01.png)

### <a name="modify-the-format-of-the-er-solution-to-calculate-the-running-tax-total"></a>Ändern Sie das Format der ER-Lösung, um die laufende Steuersumme zu berechnen

Wenn das Volumen der Transaktionen viel größer ist als im aktuellen Beispiel, kann sich die Zeit, die das Summieren benötigt, erhöhen und zu Leistungsproblemen führen. Indem Sie die Einstellungen des Formats festlegen, können Sie dazu beitragen, diese Leistungsprobleme zu vermeiden. Da Sie auf die Steuerwerte zugreifen, um sie in den generierten Bericht aufzunehmen, können Sie diese Informationen wiederverwenden, um die Steuerwerte zu summieren.

1. Wählen Sie auf der Seite **Formatdesigner** auf der Registerkarte **Zuordnung** die Option **Wurzel hinzufügen**.
2. Im Dialogfeld **Datenquelle hinzufügen** wählen Sie **Funktionen** \> **Datensammlung**.
3. Gehen Sie in der Dialogbox **Eigenschaften der Datenquelle "Datensammlung"** wie folgt vor:

    1. Geben Sie in das Feld **Name** **CollectedTaxValues** ein.
    2. Wählen Sie im Feld **Artikeltyp** **Gleitkommazahl** aus.
    3. Wählen Sie im Feld **Alle Werte sammeln** die Option **Ja**.
    4. Wählen Sie **OK** aus.

4. Wählen Sie das numerische Formatelement **Bericht\\Zeilen\\Datensatz\\TaxAmount**.

    > [!NOTE]
    > Derzeit ist für dieses Element die Bindung `@.Value` konfiguriert. Daher wird ein generierter Beleg, wenn er mit Steuerwerten aus dem Feld `model.Data.List.Value` gefüllt wird.

5. Wählen Sie **Formel bearbeiten** aus.
6. Gehen Sie auf der Seite **Formulardesigner** wie folgt vor:

    1. Ersetzen Sie im Feld **Formel** `@.Value` durch `CollectedTaxValues.Collect(@.Value)`.
    2. Speichern Sie Ihre Änderungen und schließen Sie die Seite.

    > [!NOTE]
    > Die neue Bindung wird die gleichen Steuerwerte an einen generierten Beleg übergeben. Allerdings werden diese Werte auch in der Datenquelle **CollectedTaxValues** gesammelt.

7. Wählen Sie das numerische Formatelement **Bericht\\Zeilen\\Datensatz\\RunningTotal**.
8. Wählen Sie **Formel bearbeiten** aus.
9. Gehen Sie auf der Seite **Formulardesigner** wie folgt vor:

    1. Geben Sie im Feld **Formel** eine `CollectedTaxValues.Sum(false)` ein.
    2. Speichern Sie Ihre Änderungen und schließen Sie die Seite.

    > [!NOTE]
    > Die neue Bindung übergibt an einen generierten Beleg den Gesamtbetrag der bereits eingegebenen Steuerwerte.

    ![Numerische Elemente, deren Bindungen auf der Seite Formatdesigner aktualisiert wurden](./media/er-data-collection-data-sources-02.png)

10. Wählen Sie **Speichern** und dann **Ausführen** aus.
11. Wählen Sie im Dialogfeld **Elektronische Berichtsparameter** die Option **OK** aus.
12. Laden Sie die vom Webbrowser angebotene Datei herunter und öffnen Sie sie zur Überprüfung.

    ![Heruntergeladene Datei, die die Ergebnisse der modifizierten Formatausführung enthält](./media/er-data-collection-data-sources-03.png)

### <a name="modify-the-format-to-evaluate-the-list-of-collected-tax-values"></a>Ändern Sie das Format, um die Liste der erfassten Steuerwerte auszuwerten

1. Wählen Sie auf der Seite **Formatdesigner** auf der Registerkarte **Format** das numerische Formatelement **Bericht\\Zeilen\\Datensatz\\RunningTotal** und führen Sie dann die folgenden Schritte aus:

    1. Ändern Sie im Feld **Numerischer Typ** den Wert von **Real** auf **Ganzzahl**.
    2. Ändern Sie im Feld **Numerisches Format** den Wert von **F2** auf **F0**.

3. Wählen Sie auf der Registerkarte **Zuordnung** die Option **Formel bearbeiten**.
4. Gehen Sie auf der Seite **Formulardesigner** wie folgt vor:

    1. Geben Sie im Feld **Formel** eine `COUNT(CollectedTaxValues.Result)` ein.
    2. Speichern Sie Ihre Änderungen und schließen Sie die Seite.

    > [!NOTE]
    > Die neue Bindung übergibt an einen generierten Beleg die Anzahl der Datensätze in der Liste, in der die Steuerwerte gesammelt werden.

5. Wählen Sie **Speichern** und dann **Ausführen** aus.
6. Wählen Sie im Dialogfeld **Elektronische Berichtsparameter** die Option **OK** aus.
7. Laden Sie die vom Webbrowser angebotene Datei herunter und öffnen Sie sie zur Überprüfung.

    ![Heruntergeladene Datei, die Ergebnisse einer anderen modifizierten Formatausführung enthält](./media/er-data-collection-data-sources-04.png)

## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen

### <a name="if-i-have-to-calculate-running-totals-and-collect-data-what-is-the-difference-between-using-a-data-collection-data-source-and-using-the-built-in-data-collection-functions"></a>Wenn ich laufende Summen berechnen und Daten sammeln muss, was ist der Unterschied zwischen der Verwendung einer DATA COLLECTION Datenquelle und der Verwendung der integrierten DATA COLLECTION Funktionen?

Sowohl eine DATA COLLECTION-Datenquelle als auch die integrierten [DATA COLLECTION](er-functions-category-data-collection.md)-Funktionen können zum Sammeln, Summieren und Zählen von Daten verwendet werden, basierend auf Informationen, die an einen generierten ausgehenden Beleg übergeben werden. Bei der Entscheidung, welche Technik Sie verwenden sollen, müssen Sie jedoch die folgenden Punkte berücksichtigen.

| Datenquelle | Eingebaute Funktionen |
|-------------| ------------------ |
| Es werden nur Werte gesammelt. | <p>Es werden benannte Werte gesammelt. Daher können Summen für einzelne Gruppen von Werten berechnet werden.</p><p>Außerdem können Gruppen als Liste extrahiert werden.</p><p>Es können auch Textwerte gesammelt werden.</p> |
| Eindeutige Werte werden automatisch gesammelt. | Es sind zusätzliche Einstellungen erforderlich, um eine Liste eindeutiger Werte aus den gesammelten Werten zu extrahieren. |
| Die Leistung hängt von der Menge der gesammelten Werte ab. | In der Praxis hängt die Leistung nicht von der Menge der gesammelten Werte ab. |
| Diese Technik funktioniert für alle Arten von ausgehenden Belegen. | Diese Technik funktioniert nur für Text- und XML-Dokumente. |

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Konfigurieren des Formats für Inventuren und Summierungen](./tasks/er-format-counting-summing-1.md)
- [Ausführung von Sequenz-Elementen in ER-Formaten verzögern](er-defer-sequence-element.md#Example)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
