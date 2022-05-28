---
title: Definitionen für Berichtsbaumstrukturen in Finanzberichten
description: Dieser Artikel beschreibt Definitionen für Berichtsbaumstrukturen. Eine Definition für Berichtsbaumstrukturen ist eine Berichtskomponente, die die Struktur einer Organisation definiert.
author: jinniew
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 57592
ms.assetid: 747faa47-9a23-4277-bc11-8d0a1267c3a4
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: cf5062cfc7ce47a2356c72462da805e8d0d6a756
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2022
ms.locfileid: "8727789"
---
# <a name="reporting-tree-definitions-in-financial-reports"></a>Definitionen für Berichtsbaumstrukturen in Finanzberichten

[!include [banner](../includes/banner.md)]

Dieser Artikel enthält Informationen zu Berichtsstruktur-Definitionen. Eine Berichtsstruktur-Definition ist eine Berichtkomponente oder ein Baustein, die/der Sie dabei unterstützt, die Struktur und die Hierarchie Ihrer Organisation zu definieren.

Finanzberichte unterstützen die flexible Berichterstellung, damit Änderungen einfach vorgenommen werden können, wenn sich die Geschäftsstruktur ändert. Berichte basieren auf verschiedenen Komponenten oder Bausteinen. Einer dieser Bausteine ist eine Berichtsstruktur-Definition. Die Berichtsstruktur-Definition hilft, die Struktur und die Hierarchie Ihrer Organisation zu definieren. Es ist eine dimensionsübergreifende hierarchische Struktur, die auf den dimensionalen Beziehungen in den Finanzdaten basieren. Sie stellt Informationen für alle Einheiten in der Struktur auf der Berichtseinheitenebene und auf einer Zusammenfassungsebene bereit. Berichtsstruktur-Definitionen können mit Spaltendefinitionen und Berichtsdefinitionen kombiniert werden, um eine Bausteingruppe zu erstellen, die von mehreren Unternehmen verwendet werden kann. Eine Berichtseinheit wird für jedes Feld in einem Organigramm verwendet. Eine Berichtseinheit kann eine einzelne Abteilung in den Finanzdaten sein oder eine Zusammenfassungseinheit einer höherer Ebene, die Informationen aus anderen Berichtseinheiten zusammenführt. Für eine Berichtsdefinition, die eine Berichtsbaumstruktur umfasst, wird ein Bericht für jede Berichtseinheit und für die zusammenfassende Ebene generiert. Alle diese Berichte verwenden die Zeilen- und Spaltendefinitionen, die in der Berichtsdefinition angegeben werden, es sei denn, die Berichtsdefinition gibt an, die Berichtstruktur der Zeilendefinition zu verwenden. Zeilen- und Spaltendefinitionen sind wichtige Komponenten im Entwurf und in der Funktion von Finanzberichten. Berichtsbaumstrukturen erhöhen die Leistung der Komponenten und unterstützen flexible Berichterstellung, wenn sich die Geschäftsstruktur ändert. Finanzberichte, die nicht auf einer Berichtstruktur basieren, verwenden nur einige der Funktionen des Finanzberichterstellung. Sie können mehrere Berichtstruktur-Definitionen mit der gleichen Zeilen- und Spaltendefinitionen verwenden, um die Daten Ihrer Organisation auf verschiedene Arten anzuzeigen.

## <a name="reporting-tree-best-practices"></a>Bewährte Methoden bei Berichtsbaumstrukturen
Bevor Sie eine Berichtstruktur erstellen, ziehen die folgenden bewährten Methoden in Betracht:

- Bestimmen Sie zunächst, welche Berichterstellungsdimensionen die juristische Person oder das Unternehmen benötigt.
- Berücksichtigen Sie, wie Sie Ihre Struktur eingerichtet haben, und erstellen Sie anschließend ein Organigramm Ihres Unternehmens. Mit dem Organigramm können Sie sich eine bessere Vorstellung davon machen, wie die Berichtseinheiten in einer oder mehreren Berichtsbaumstrukturen gruppiert werden müssen.
- Erste Schritte mit der niedrigsten verfügbaren Detailebene, wie der Abteilungen und den Projekten, die in den Finanzdaten definiert werden. Fügen Sie der Detailstufe so viele Felder hinzu, wie nötig, um übergeordnete Abteilungen oder Regionen anzuzeigen. Jedes Feld stellt eine mögliche Berichtseinheit in einer beliebigen Berichtsbaumstruktur dar,die Sie selbst erstellt haben.
- Sie müssen sich auch für die beste Methode entscheiden, in der Sie Ihre Strukturen erstellen. Sie können einen automatischen Erstellungsprozess generieren, um eine Berichtstruktur zu erstellen, oder Sie können diese manuell erstellen. Es ist wichtig, dass Sie beide Methoden verstehen, bevor Sie Ihre Strukturen entwerfen.
- Sie können die Berichtseinheiten verwenden, die in Ihrem Finanzdatensystem definiert werden, um der Berichtsbaumstruktur-Definition Berichtseinheiten hinzuzufügen.

## <a name="create-multiple-reporting-trees"></a>Erstellen mehrerer Berichtsbaumstrukturen
Sie können eine unbegrenzte Anzahl von Berichtsbaumstrukturen erstellen, um die Daten der Organisation auf verschiedene Weise anzuzeigen. Jede Berichtsbaumstruktur kann eine beliebige Kombination von Abteilungen und Konsolidierungseinheiten enthalten. Eine Berichtsdefinition kann eine Verknüpfung mit nur einer Berichtsbaumstruktur nach einander enthalten. Wenn Sie die Struktur der Berichtseinheiten neu anordnen, können Sie verschiedene Berichtsbaumstrukturen erstellen. Sie können nun dieselben Zeilen- und Spaltendefinitionen für jede Berichtstruktur verwenden. Auf diese Weise können Sie schnell unterschiedliche Finanzbericht-Layouts erstellen. Wenn Sie mehrere verschiedene Berichtstrukturen erstellen, können Sie jeden Monat eine Serie von Finanzaufstellungen drucken, die die Arbeitsgänge des Unternehmens auf unterschiedliche Weise analysieren und darstellen. Weitere Informationen finden Sie in den Beispielen zu Berichtseinheitenstrukturen am Ende dieses Artikels.

## <a name="create-a-reporting-tree-definition"></a>Erstellen einer Berichtsbaumstruktur-Definition
Die Berichtstruktur-Definition enthält die Spalten, die in der folgenden Tabelle beschrieben werden.

| Berichtsbaumstrukturspalte | Beschreibung |
|-----------------------|-------------|
| Firma               | Der Unternehmensname für die Berichtseinheit. Der **\@ANY**-Wert, der normalerweise nur auf der Zusammenfassungsebene zugewiesen wird, ermöglicht die Verwendung der Berichtsbaumstruktur für alle Unternehmen. Allen untergeordneten Verzweigungen ist ein Unternehmen zugewiesen. |
| Einheitenname             | Der Code, der diese Berichtserstellungseinheit in der grafischen Berichtsbaumstruktur identifiziert. Stellen Sie sicher, dass ein konsistentes und eindeutiges Kodierungssystem festgelegt ist, das für den Benutzer leicht verständlich ist. |
| Einheitenbeschreibung      | Der Berichtseinheitentitel wird in der Kopf- oder Fußzeile des Berichts angezeigt, wenn Sie **UnitDesc** als Code auf der Registerkarte **Kopf- und Fußzeilen** eingeben. Der Titel wird in der Berichtszeilenbeschreibung angezeigt, wenn Sie **UnitDesc** in der Zelle **Beschreibung** der Zeilendefinition eingeben. |
| Dimensionen            | Eine Berichtserstellungseinheit, die Informationen direkt aus den Finanzdaten bezieht. Sie definiert den logische Standort und die Längen für das Konto und die zugehörigen Segmente. Jede Berichtseinheitszeile muss eine Dimension in dieser Spalte enthalten. Sie können eine Dimension auch in einer zusammengefassten Einheitszeile festlegen (z. B. für die Ausgaben, die dieser Einheit direkt zugeordnet sind). Wenn Sie eine Dimension in einer zusammengefassten Einheitszeile eingeben, sollten Konten, die in den untergeordneten Einheiten verwendet werden nicht in den untergeordneten Einheiten verwendet werden. Andernfalls könnten Beträge dupliziert werden. |
| Zeilendefinitionen       | Der Name der Zeilendefinition für die Berichtserstellungseinheit. Dieselbe Zeilendefinition wird für jede Einheit der Berichtsbaumstruktur verwendet. Wenn Sie einen Bericht generieren, wird diese Zeilendefinition für jede Berichtseinheit verwendet. Die Zeilendefinition kann mehrere Finanzdimensionsverknüpfung enthalten. Wenn eine Zeilendefinition in der Berichtstruktur angegeben ist, aktivieren Sie das Kontrollkästchen **Zeilendefinition aus Berichtstruktur verwenden** auf der Registerkarte **Bericht** der Berichtsdefinition. |
| Finanzdimensionenlink| Der Finanzdimensionenlink, der für die Berichtseinheit verwendet werden soll. Finanzdimensionenlinks sind für die Zeilendefinition festgelegt, um die Finanzdimensionen zu kennzeichnen, zu denen eine Verknüpfung hergestellt wird. |
| Seitenoptionen          | Diese Spalte steuert, ob die Details der Berichterstattungseinheit unterdrückt werden, wenn der Bericht angezeigt oder gedruckt wird. |
| Rollup %              | Der Prozentsatz der Berichtserstellungseinheit, der der übergeordneten Einheit zugewiesen werden soll. Der Prozentsatz, den Sie in diese Spalte eingeben, gilt für jede Zeile der Zeilendefinition, bevor der Wert in der Zeile dem übergeordneten Bericht hinzugefügt wird. Wenn beispielsweise eine untergeordnete Einheit gleichmäßig zwischen zwei Abteilungen aufgeteilt werden muss, werden die Beträge in jeder Zeile mit 50 Prozent multipliziert, bevor der Wert dem Abteilungsbericht hinzugefügt werden. Eine Berichtseinheit kann keine zwei übergeordnete Einheiten haben. Um die Beträge aus einer Berichtseinheit zwei übergeordneten Einheiten zuzuweisen, erstellen Sie eine weitere Berichtseinheit mit derselben Dimension für einen Rollup der zusätzlichen 50 Prozent. Geben Sie gesamte Prozentsätze ohne Dezimalstellen ein. Beispielsweise stellt **25** eine 25 Prozent-Zuteilung zum übergeordneten Objekt dar. Wenn Sie eine Nachkommastelle angeben (**0,25**), werden dem übergeordneten Objekt 0,25 Prozent zugeordnet. Zum Verwenden eines Prozentsatzes, der unter einem Prozent liegt, können Sie die Option **Rollup zulassen &lt;1 %** in der Berichtsdefinition verwenden. Diese Option befindet sich auf der Registerkarte **Weitere Optionen** im Dialogfeld **Berichtseinstellungen**. Rufen Sie dieses Dialogfeld über die Schaltfläche **Sonstiges** auf der Registerkarte **Einstellungen** der Berichtsdefinition auf. |
| Einheitssicherheit         | Beschränkungen der Benutzer und Gruppen, die auf Informationen der Berichtseinheit zugreifen können. |
| Weiterer Text       | Text, den der Bericht beinhaltet. |

Um eine Berichtstruktur-Definition zu erstellen, führen Sie die folgenden Schritte aus:

1. Öffnen Sie den Berichts-Designer.
2. Klicken Sie auf **Datei** &gt; **Neu** &gt; **Berichtsbaumstruktur Definition**.
3. Klicken Sie auf **Bearbeiten** &gt; **Berichtseinheiten aus Dimensionen einfügen**.
4. Wählen Sie im Dialogfeld **Berichtseinheiten aus Dimensionen einfügen** das Kontrollkästchen für jede Dimension aus, die in die Berichtsbaumstruktur-Definition enthalten sein soll. Das Dialogfeld **Berichtseinheiten aus Dimensionen einfügen** enthält die folgenden Abschnitte.

    | Abschnitt                          | Beschreibung |
    |----------------------------------|-------------|
    | Segmentierung von Berichtserstellungsdimensionen | Mithilfe der Schaltflächen **Segmente teilen** und **Segmente kombinieren** können Sie die Anzahl und Länge der Segmente ändern.<blockquote>[!NOTE] Sie können nur Segmente kombinieren, die Sie teilen müssen. Verwenden Sie Platzhalterzeichen in den Dimensionswerten, um mehrere Dimensionen zu kombinieren.</blockquote> |
    | Einschließen/Zeichenposition       | Dieser Abschnitt listet die Dimensionen auf, die in den Finanzdaten definiert werden und gibt die Anzahl der Zeichen im längsten Wert an, der für jede Dimension definiert wurde. Wählen Sie ein Kontrollkästchen für eine Dimension aus, um diese Dimension in die Berichtstruktur-Hierarchie einzuschließen. |
    | Segmenthierarchie und -bereiche     | Dieser Abschnitt zeigt die Dimensionshierarchie. Sie können die Dimensionen in der Liste verschieben, um die Reihenfolge ihre Berichterstellung zu ändern. In den Feldern **Ausgangsdimension** und **Zieldimension** können Sie den Wertebereich jeder Dimension angeben. Wenn Sie keinen Bereich angeben, werden alle Dimensionswerte in die Berichtsstruktur eingefügt.<blockquote>[!NOTE] Falls Sie mehr als eine Dimension verwenden, werden nur Dimensionskombinationen, in denen Buchungen vorgenommen wurden, in den Ergebnissen zurückgegeben.</blockquote> |

    Eine Abbildung, die ein Beispiel für das Dialogfenster **Berichtseinheiten aus Dimensionen einfügen** zeigt, finden Sie im Abschnitt „Beispiel für das Dialogfenster „Berichtseinheiten aus Dimensionen einfügen““ weiter unten in diesem Artikel.

5. Um zusätzliche Segmente zu erstellen (z. B. durch das Teilen eines Segments in zwei kürzere Segmente), klicken Sie auf die richtige Position in einem **Zeichenposition**-Feld, und klicken Sie auf **Segmente teilen**.
6. Um zwei Segmente in einem Segment zusammenführen, klicken Sie in jedes der Segmentfelder, die zusammengeführt werden sollen, und klicken Sie anschließend auf **Segmente kombinieren**.
7. Die Hierarchie definiert, wie die Dimensionen einen gegenseitigen Bericht erstellen, und den Bereich für jede Dimension. Um die Hierarchie der Dimensionen im Bereich **Segmenthierarchie und -bereiche** zu ändern, wählen Sie die Dimension aus, die verschoben werden sollen, und klicken Sie dann auf **Nach oben** oder **Nach unten**.
8. Um einen Bereich der Dimensionswerte anzugeben, die der neuen Berichtsbaumstruktur im Bereich **Segmenthierarchie und -bereiche** hinzugefügt werden sollen, führen Sie die folgenden Schritte aus:

    1. Geben Sie im Feld **Ausgangsdimension** für diese Dimension den ersten Wert des Bereichs ein.
    2. Geben Sie im Feld **Zieldimension** für diese Dimension den letzten Wert des Bereichs ein.

9. Wiederholen Sie die Schritte 7 und 8 für jede Dimension im Bereich **Segmenthierarchie und -bereiche**.
10. Nachdem Sie definiert haben, wie Ihre Berichtseinheiten in die neue Berichtstruktur integriert werden, klicken Sie auf **OK**.
11. Klicken Sie auf **Datei** &gt; **Speichern**, um die Berichtstruktur zu speichern. Geben Sie im Formular einen eindeutigen Namen und eine Beschreibung für die Berichterstattungsstruktur ein, und klicken Sie dann auf **OK**.

### <a name="open-an-existing-reporting-tree-definition"></a>Öffnen einer vorhandene Berichtsbaumstruktur-Definition

1. Klicken Sie im Berichts-Designer im Navigationsbereich auf **Berichtsbaumstruktur-Definitionen**.
2. Doppelklicken Sie auf einen Namen in der Berichtsbaumstrukturliste, um sie zu öffnen.
3. Um alle Bausteine anzuzeigen, die der Berichtsbaumstruktur zugeordnet sind, klicken Sie mit der rechten Maustaste auf die Berichtsbaumstruktur-Definition, und wählen Sie dann **Zuordnungen** aus.

### <a name="roll-up-data-in-a-reporting-tree"></a>Rollup der Daten in einer Berichtserstellungsstruktur

Unter Verwendung einer Berichtstruktur können Sie Beträge aus untergeordneten Berichtseinheiten auf der übergeordneten Berichtseinheitenebene zusammenführen. Diese Zusammenfassung wird auch als Daten-Rollup bezeichnet. Die folgenden Regeln werden für ein Rollup der Beträge auf übergeordnete Einheiten in einer Berichtsbaumstruktur verwendet:

- In einer Berichtstruktur müssen untergeordnete Einheiten Dimensionen enthalten, es sei denn, es handelt sich um eine Struktur mit nur einer Ebene. Übergeordnete Einheiten enthalten in einer Berichtstruktur normalerweise keine Dimensionen.

    > [!NOTE]
    > Wenn Sie Dimensionen für untergeordnete Einheiten und übergeordnete Einheiten angeben, könnten Daten im Bericht dupliziert werden.

- Berichtseinheiten, die Dimensionen in der Berichtsbaumstruktur enthalten, entsprechen den Dimensionen, die in den Zeilen- und in den Spaltendefinitionen verwendet werden. Die Kombination der Dimensionen bestimmt die Beträge, die für diese Einheit zurückgegeben werden. So geben in Beispiel 2 weiter unten in diesem Artikel die Positionen 6 und 7 jeweils nur die Werte für Abteilung 00 und 01 zurück.
- Die Beträge für übergeordnete Berichtseinheiten, die keine Dimensionen in der Berichtstruktur enthalten, werden vom untergeordneten Einheitsbericht bestimmt und führen einen Rollup des Betrags auf der angegebenen übergeordneten Einheit durch. Wenn z. B. die übergeordnete Einheit (siehe Contoso-USA in Beispiel 2 des Daten-Rollup-Beispiels) zwei untergeordnete Einheiten (022 und 023) aufweist und keine Dimensionen enthält, wird ein Bericht für jedes untergeordnete und das übergeordnete Element generiert. Die übergeordnete Summe ist die Summe der zwei untergeordneten Beträge.

### <a name="manage-reporting-units"></a>Verwalten von Berichtseinheiten

Jede Berichtstruktur-Definition wird als individuelle Ansicht angezeigt. Es gibt eine grafische Ansicht, die die über- und untergeordneten Hierarchie darstellt und eine Arbeitsblattansicht, die die spezifischen Informationen für jede Berichtseinheit anzeigt. Die grafische Ansicht und die Arbeitsblattansicht werden verbunden. Wenn Sie eine Berichtseinheit in einer Ansicht auswählen, wird diese auch in der anderen Ansicht ausgewählt. Sie können dimensionsübergreifende Hierarchien auf Grundlage der Dimensionsbeziehungen in den Finanzdaten aufbauen. Wenn Sie eine Berichtstruktur-Definition erstellen, können Sie dieselben Zeilendefinitionen mehrfach verwenden, egal ob Sie eine Einkommensaufstellung aller Abteilungen oder eine konsolidierte zusammenfassende Einkommensaufstellung generieren. Die Dimensionen, die in der Zeilendefinition festgelegt werden, können mit Dimensionen in der Berichtstruktur-Definition kombiniert werden, um eine Vielzahl von Ansichten der Leistung Ihrer Organisation bereitzustellen.

### <a name="reporting-unit-structure"></a>Berichtseinheitenstruktur

Folgende Typen von Berichtseinheiten werden in der Finanzberichterstellung verwendet:

- Eine Detaileinheit bezieht die Informationen direkt aus den Finanzdaten.
- Eine zusammengefasste Einheit fasst Daten von Einheiten auf niedrigerer Ebene zusammen.

Eine übergeordnete Berichtseinheit ist eine zusammengefasste Einheit, die zusammengefasste Informationen aus einer Detaileinheit zusammengefasst. Eine zusammengefasste Einheit kann eine Detaileinheit und eine zusammengefasste Einheit sein. Das bedeutet, dass eine zusammengefasste Einheit Informationen aus einer unteren Einheit oder den Finanzdaten beziehen kann. Eine übergeordnete Einheit kann die untergeordnete Einheit für eine übergeordnete Einheit einer höheren Ebene sein. Eine untergeordnete Berichtseinheit kann eine Detaileinheit sein, die Informationen direkt aus den Finanzdaten bezieht. Eine untergeordnete Berichtseinheit kann auch eine zwischenzeitlich zusammengefasste Einheit sein. Das bedeutet, es kann also die übergeordnete Einheit einer niedrigeren Einheit sowie die untergeordnete Einheit einer Einheit auf höherer Ebene sein. Im häufigsten Szenario für Berichtseinheiten ist in einer übergeordnete Einheit die Zelle in der Spalte **Dimensionen** leer und die untergeordnete Einheit enthält Links zu bestimmten oder Platzhalter-Dimensionskombinationen.

### <a name="organize-reporting-units"></a>Organisieren von Berichtseinheiten

Sie können die Organisationsstruktur einer Berichtsbaumstruktur-Definition anpassen, indem Sie in der grafischen Ansicht die Berichtseinheiten verschieben. Sie können Berichtseinheiten auch auf einer höheren Ebene in der Berichtstruktur einstufen oder sie zu einer niedrigeren Ebene herunterstufen.

1. Öffnen Sie die zu ändernde Berichtsbaumstruktur-Definition im Berichts-Designer.
2. Wählen Sie in der grafischen Ansicht der Berichtsbaumstruktur-Definition eine Berichtseinheit aus.
3. Ziehen Sie die Einheit an eine neue Position. Alternativ klicken Sie mit der rechten Maustaste auf die Einheit, und wählen dann **Berichtseinheit höherstufen** oder **Berichtseinheit herunterstufen** aus.
4. Klicken Sie auf **Datei** &gt; **Speichern**, um die Änderungen zu speichern.

### <a name="add-text-about-a-reporting-unit"></a>Hinzufügen von Text über eine Berichtseinheit

Eine Zusatztexteingabe ist eine statische Textzeichenfolge von bis zu 255 Zeichen, die Informationen zu der Berichtstruktur-Definition hinzufügt. Beispielsweise kann der Zusatztext eine kurze Unternehmensbeschreibung sein. Sie können bis zu zehn Zusatztexteingaben für jede Berichtseinheit in einer Berichtsbaumstruktur-Definition erstellen. Der Zusatztext wird im Bericht für die Berichtseinheit angezeigt, der der Text zugewiesen ist. Sie können Texteinträge aus der Spalte **Beschreibung** der Zeilendefinition hinzufügen und der Registerkarte **Kopf- und Fußzeilen** in der Berichtsdefinition.

1. Öffnen Sie die zu ändernde Berichtsbaumstruktur-Definition im Berichts-Designer.
2. Doppelklicken Sie auf die Zelle **Zusätzlicher Text** der Berichtseinheitszeile.
3. Geben Sie im Dialogfeld **Zusätzlicher Text** den Text in der ersten leeren Zeile ein. Die erste Zeile, die Text enthält, wird als UnitText1 bezeichnet, ungeachtet seiner Position im Dialogfeld **Zusätzlicher Text**.
4. Wenn Sie mehr Texteingaben für diese Berichtseinheit hinzuzufügen möchten, geben Sie den Text in einer leeren Zeile ein.
5. Klicken Sie auf **OK**.

### <a name="remove-additional-text-from-a-reporting-unit"></a>Entfernen von zusätzlichem Text aus einer Berichtseinheit

1. Öffnen Sie zur Bearbeitung die Berichtsbaumstrukturdefinition im Berichts-Designer.
2. Doppelklicken Sie auf die Zelle **Zusätzlicher Text** der Zeile der Berichtseinheit.
3. Wählen Sie im Dialogfeld **Zusätzlicher Text** den zu entfernenden Eintrag aus, und klicken Sie anschließend auf **Löschen**. Alternativ klicken Sie mit der rechten Maustaste auf den Eintrag und wählen **Ausschneiden** aus.
4. Klicken Sie auf **OK**.

### <a name="restrict-access-to-a-reporting-unit"></a>Beschränken des Zugriffs auf eine Berichtseinheit

Sie können den Zugriff bestimmter Benutzer und Gruppen auf einer Berichtseinheit verhindern. Sie können auch Beschränkung definieren, die auf untergeordnete Einheiten der Berichtseinheit angewendet werden.

1. Öffnen Sie die zu ändernde Berichtsbaumstruktur-Definition im Berichts-Designer.
2. Doppelklicken Sie für die Zeile der Berichtseinheit, für die der Zugriff eingeschränkt werden soll, auf die Zelle **Einheitssicherheit** .
3. Klicken Sie im Dialogfeld **Einheitssicherheit** auf **Benutzer und Gruppen**.
4. Wählen Sie die Benutzer oder die Gruppen aus, die Zugriff auf die Berichtseinheit haben sollen, und klicken Sie anschließend auf **OK**.
5. Um den Zugriff auf die untergeordneten Berichtseinheiten zu beschränken, aktivieren Sie das Kontrollkästchen **Sicherheit zu untergeordneten Berichtserstellungseinheiten hinzufügen**.
6. Klicken Sie auf **OK**.

### <a name="remove-access-to-a-reporting-unit"></a>Entfernen des Zugriffs auf eine Berichtseinheit

1. Öffnen Sie die zu ändernde Berichtsbaumstruktur-Definition im Berichts-Designer.
2. Doppelklicken Sie auf die Zelle **Einheitssicherheit** der Berichtseinheitszeile, um den Zugriff zu entfernen.
3. Wählen Sie im Dialogfeld **Einheitssicherheit** einen Namen aus, und klicken Sie dann auf **Entfernen**.
4. Klicken Sie auf **OK**.

## <a name="examples"></a>Beispiele
### <a name="reporting-unit-structure--example-1"></a>Berichtseinheitsstruktur - Beispiel 1

Die Berichtseinheitenstruktur in der folgenden Berichtstruktur ist wie folgt:

- Die Contoso Japan-Berichtseinheit ist eine übergeordnete Einheit der untergeordneten Einheiten Contoso Japan Sales und Contoso Japan Consulting.
- Die Bereichseinheit Contoso Japan Sales ist sowohl eine untergeordnete Einheit der Contoso Japan-Einheit als auch eine übergeordnete Einheit der Home Sales- und Auto Sales-Einheiten.
- Die Detailberichtseinheiten der niedrigsten Ebene (Home Sales, Auto Sales, Client Services, und Operations) stellen Abteilungen in den Finanzdaten dar. Diese Berichtseinheiten befinden sich im schattierten Bereich des Diagramms.
- Die zusammengefassten Einheiten auf höherer Ebene fassen Informationen aus den Detaileinheiten zusammen.

[![Contoso-Zusammenfassungsberichtsstruktur – Beispiel 1.](./media/contosoentertainmentsummaryreportstructure.png)](./media/contosoentertainmentsummaryreportstructure.png)

### <a name="reporting-unit-structure--example-2"></a>Berichtseinheitsstruktur - Beispiel 2

Das folgende Diagramm zeigt eine Berichtstruktur mit eine Organisationsstruktur, die nach Unternehmensfunktion aufgeteilt ist.

[![Contoso-Zusammenfassungsberichtsstruktur – Beispiel 2.](./media/summaryofallunitscontoso.png)](./media/summaryofallunitscontoso.png)

### <a name="example-of-the-insert-reporting-units-from-dimensions-dialog-box"></a>Beispiel für das Dialogfeld "Berichtseinheiten aus Dimensionen einfügen"

Die folgende Abbildung zeigt ein Beispiel für das Dialogfeld **Berichtseinheiten aus Dimensionen einfügen**. In diesem Beispiel ist das Ergebnis eine Kombination aus Unternehmenseinheiten, Kostenstellen und Abteilungen.

[![Berichtseinheiten einfügen.](./media/insertreportingunits.png)](./media/insertreportingunits.png)

Die resultierende Berichtstruktur-Definition ist nach Geschäftseinheit, dann nach Kostenstelle und dann nach Abteilung sortiert. Die Dimension für die fünfte Berichtseinheit ist **Unternehmenseinhet = \[001\] Kostenstelle =\[\], Abteilung = \[022\]**, und identifiziert eine Berichtseinheit für Konten die spezifisch für die Unternehmenseinheit 001 und Abteilung 022 sind.

[![Abbildung des Berichtsbaums.](./media/reportingtree-1024x646.png)](./media/reportingtree.png)

### <a name="examples-of-data-roll-up"></a>Beispiele für Daten-Rollup

Die folgenden Beispiele zeigen mögliche Informationen an, die in einer Berichtsstruktur-Definition als ein Beispiel für Daten-Rollup verwendet werden.

#### <a name="example-1"></a>Beispiel 1

[![Roll-up für mehrere Unternehmen.](./media/mutlicompanyrollup.png)](./media/mutlicompanyrollup.png)

#### <a name="example-2"></a>Beispiel 2

[![Abteilungsübergreifendes Roll-up.](./media/crosscompanydepartmentrollup.png)](./media/crosscompanydepartmentrollup.png)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Finanzberichterstellung](financial-reporting-intro.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
