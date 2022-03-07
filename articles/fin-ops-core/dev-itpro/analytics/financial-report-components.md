---
title: Finanzberichtkomponenten
description: Dieser Artikel beschreibt die Verwendung der Komponenten, der Bausteine oder Berichtsdefinitionen in der Finanzberichterstellung.
author: aprilolson
ms.date: 10/27/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 59071
ms.assetid: a201cfcb-1672-45f6-897d-2db2dd181d9a
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 8512559ea33f16f3558b277999cc86240ee8277d1b3b0d6bf2aecba32df8e09f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6761439"
---
# <a name="financial-report-components"></a>Finanzberichtkomponenten

[!include [banner](../includes/banner.md)]

Dieser Artikel beschreibt die Verwendung der Komponenten, der Bausteine oder Berichtsdefinitionen in der Finanzberichterstellung. Diese Bausteine beinhalten Zeilendefinitionen, Spaltendefinitionen und Berichtstruktur-Definitionen. Der Artikel beschreibt, wie Sie Bausteine organisieren und sperren.

Die Designphilosophie hinter dem Finanzberichtdesigner ist, Informationen in kleinste Komponenten oder Grundbausteine zu zerteilen, sie zu mischen und nach Bedarf zusammenzufügen. Daher ist die Berichtsformatierung von Ihren Finanzdaten getrennt, und Sie können das Design eines Berichts ändern, ohne die Finanzdaten in Ihrem Microsoft Dynamics ERP-System zu ändern. Mithilfe dieses Bausteinansatzes können Sie Text, Beträge und Berechnungen kombinieren, um die Berichte zu erstellen, die Sie benötigen. Zudem fördert diese Flexibilität die Kreativität, indem es das Anzeigen Ihrer Arbeitsgänge auf unterschiedliche Arten erleichtert. Die einzelnen Bausteine einer Berichtsdefinition sind einem dreidimensionalen Arbeitsblatt ähnlich, sie bieten jedoch mehr Leistung. Eine Berichtsdefinition gibt die Zeilendefinition, die Spaltendefinition und die optionale Berichtstruktur-Definition an, die für den Bericht verwendet werden sollte. Sie umfasst auch Informationen zum Speicherort des generierten Berichts und wie er formatiert wird.

## <a name="building-blocks-of-a-report"></a>Bausteine eines Berichts

| Baustein            | Beschreibung | Weitere Informationen |
|---------------------------|-------------|----------------------|
| Zeilendefinition            | Eine Zeilendefinition definiert die beschreibenden Positionen (z. B. Löhne oder Verkäufe), in einem Bericht. Sie listet auch Segmentwerte oder Dimensionen auf, die die Werte für jeden Positionsartikel enthalten und schließt Zeilenformatierung und Berechnungen ein. | [Zeilendefinitionen](row-definitions-financial-reporting.md) |
| Spaltendefinition         | Eine Spaltendefinition definiert die Periode, die verwendet werden soll, wenn Daten aus den Finanzdimensionen extrahiert werden. Sie umfasst auch Spaltenformatierung und Berechnungen. | [Spaltendefinitionen](column-definitions-financial-reports.md) |
| Berichtsbaumstruktur-Definition | Eine Berichtsbaumstruktur-Definition ähnelt einem Organigramm. Sie enthält einzelne Berichtseinheiten, die jedes Feld im Diagramm darstellen. Die Einheiten können entweder einzelne Abteilungen aus den Finanzdaten oder ranghöhere Einheiten sein, die Daten aus anderen Berichtseinheiten zusammenfassen. | [Berichtsbaumstruktur-Definitionen](financial-reporting-tree-definitions.md) |
| Berichtsdefinition         | Eine Berichtsdefinition verwendet eine Zeilendefinition, eine Spaltendefinition und eine optionale Berichtsbaumstruktur-Definition, um den Bericht zu erstellen. Sie bietet auch zusätzliche Optionen und Einstellungen, die Sie verwenden können, um einen Bericht anzupassen. | [Berichtsdefinition](design-financial-report-definitions.md) |

Wenn das Entwerfen von Berichten neu für Sie ist, ist es hilfreich, den Berichts-Assistenten zu verwenden, um schnell eine Berichtsdefinition zu erstellen, die Sie später anpassen können. Wenn Sie Erfahrung im Entwerfen von Berichten haben und mehr Flexibilität in der Berichtserstellung möchten, können Sie neue oder vorhandene Bausteine kombinieren, um eine neue Berichtsdefinition zu erstellen. Sie müssen nicht alle verfügbaren Berichtsdefinitionsoptionen vollständig verstehen, um Qualitätsberichte zu erzeugen. Während Sie mit dem Entwerfen von Berichten vertraut sind, können Sie Ihre Berichtsdefinitionen erweitern, um weitere erweiterte Funktionalität nutzen zu können. Nachdem Sie einen einfachen Bericht erstellt haben, können Sie die Berichtsdefinition und alle der Bausteine in der Berichtsdefinition anpassen.

## <a name="organize-the-building-blocks"></a>Organisieren der Bausteine
Verwenden Sie Ordner, um die Bausteine im Berichts-Designer zu organisieren. Alle Ordner sind für den Typ des Bausteins, den sie enthalten, spezifisch. Beispielsweise befinden sich alle Ordner, die Zeilendefinitionen enthalten, im Bereich **Zeilendefinitionen** des Berichts-Designers.

### <a name="create-a-folder"></a>Erstellen eines Ordners

1. Im Berichts-Designer wählen Sie den Typ des Bausteins aus, der im Navigationsbereich organisiert werden soll. Beispielsweise klicken Sie zum Sortieren eine Zeilendefinition auf **Zeilendefinitionen**.
2. Wählen Sie im Navigationsbereich den vorhandenen Ordner, unter dem der neue Ordner erstellt wird, und führen Sie dann die folgenden Schritte aus:

    - Klicken Sie mit der rechten Maustaste auf den übergeordneten Ordner, und wählen Sie dann **Neuer Ordner** aus.
    - Wählen Sie den übergeordneten Ordner aus, klicken dann auf **Datei** und anschließend auf **Neuer Ordner**.

3. Wenn der neue Ordner angezeigt wird, geben Sie den Namen des neuen Ordners ein und drücken die Eingabetaste.

## <a name="lock-a-building-block"></a> Einen Baustein sperren
Sie können ein Kennwort erstellen, um einen Baustein zu schützen und zu sperren. Auf diese Wiese wird einer Berichtskomponente eine Sicherheitsstufe hinzugefügt, ohne das gesamte System zu sichern. Ein Passwort kann Bausteininformationen schützen, die für Ihren Berichterstellungsprozess am Monatsende von Bedeutung sind. Ein Benutzer in einer beliebigen Rolle kann einen Baustein sperren. Für andere Benutzer ist der Zugriff auf eine gesperrte Komponente jedoch immer schreibgeschützt. Benutzer können die gesperrte Komponente öffnen, ändern und unter neuem Namen speichern. Ein Benutzer, der die Rolle "Administrator" hat, hat immer Zugriff und kann einen gesperrten Baustein ändern.

1. Öffnen Sie im Berichts-Designer die zu schützende Berichtskomponente, wie eine Zeilendefinition, eine Spaltendefinition, eine Berichtsdefinition oder eine Berichtstruktur-Definition.
2. Klicken Sie im Menü **Extras** auf **Schützen/Schutz aufheben**. Sie können auch in der Symbolleiste auf **Schützen/Schutz aufheben** (das Schlosssymbol) klicken.
3. Geben Sie im Dialogfeld **Schützen** ein Passwort ein, bestätigen es und klicken dann auf **OK**. Das Schlosssymbol in der Symbolleiste wird hervorgehoben, wenn ein offener Baustein gesperrt ist.

Um einen gesperrten Baustein zu entsperren, öffnen Sie den Baustein, und klicken Sie anschließend auf **Schützen/Schutz aufheben** in der Symbolleiste. Oder klicken Sie im Menü **Extras** auf **Schutz aufheben**.

## <a name="building-block-groups"></a>Baustein-Gruppen

Bausteine sind die Zeilendefinitionen, Spaltendefinitionen, Berichtsbaumstruktur-Definitionen und Berichtsdefinitionen, die Sie für einen Bericht erstellen. Bausteingruppen sind Sammlungen der Definitionen und Dimensionssätze.

### <a name="view-a-building-block-group"></a>Anzeigen einer Bausteingruppe

Sie können alle Bausteine anzeigen, die einer Bausteingruppe zugewiesen sind. Sie können auch eine Bausteingruppe exportieren oder importieren.

1. Klicken Sie im Berichts-Designer im Menü **Unternehmen** auf **Bausteingruppen**.
2. Wählen Sie im Dialogfeld **Baustein-Gruppen** den Baustein aus, der angezeigt werden soll.
3. Klicken Sie auf **Anzeigen**, um das Dialogfeld **Bausteingruppe anzeigen** zu öffnen und den Inhalt der Bausteingruppe anzuzeigen.
4. Klicken Sie auf **Schließen**, um die Dialogfelder zu schließen.

### <a name="export-a-building-block-group"></a>Exportieren einer Bausteingruppe

Sie können eine Bausteingruppe oder bestimmte Berichtsbausteine innerhalb einer Bausteingruppe exportieren. Sie können die exportierte Bausteingruppe als Sicherung verwenden. Sie können auch die exportierten Daten zwischen Installationen kopieren. Der Berichtsdesigner umfasst die referenzierten Schriftschnitte und Dimensionssätze zusammen mit der Bausteingruppe.

1. Klicken Sie im Berichts-Designer im Menü **Unternehmen** auf **Bausteingruppen**.
2. Wählen Sie im Dialogfeld **Bausteingruppen** die Bausteingruppe aus, die exportiert werden soll, und klicken Sie dann auf **Exportieren**.
3. Wählen Sie im Dialogfeld **Exportieren** die Berichtsdefinitionen aus, die exportiert werden soll:

    - Um alle Ihre Berichtsdefinitionen und die zugeordneten Bausteine zu exportieren, klicken Sie auf **Alles auswählen**.
    - Um bestimmte Berichte, Zeilen, Spalten, Strukturen oder Dimensionssätze zu exportieren, klicken Sie auf die entsprechende Registerkarte und wählen die Artikel aus, die exportiert werden sollen. Halten Sie die STRG-Taste gedrückt, um mehrere Artikel in einer Registerkarte auszuwählen.

    > [!NOTE]
    > Wenn Sie Berichte für den Export auswählen, werden die zugeordneten Zeilen, Spalten, Strukturen und Dimensionssätze ausgewählt.

4. Wenn Sie die Artikel ausgewählt haben, die Sie exportieren möchten, klicken Sie auf **Exportieren**.
5. Wählen Sie im Dialogfeld **Speichern unter** einen Speicherort aus, an den die Bausteingruppe exportiert wird.
6. Geben Sie im Feld **Dateiname** einen Namen für die Datei ein. Der Berichts-Designer fügt automatisch eine .tdbx-Dateinamenerweiterung hinzu.
7. Klicken Sie auf **Speichern**. Die Bausteingruppe wird an dem Speicherort gespeichert, der von Ihnen angegeben wurde.

### <a name="import-a-building-block-group"></a> Eine Baustein-Gruppe importieren

Sie können eine Bausteingruppe in eine vorhandene Bausteingruppe importieren. Alle importierten Bausteingruppen behalten ihre ursprünglichen Schriftarten und Unternehmensreferenzen bei und enthalten die entsprechenden Dimensionssätze.

1. Klicken Sie im Berichts-Designer im Menü **Unternehmen** auf **Bausteingruppen**.
2. Wählen Sie im Dialogfeld **Bausteingruppen** den Baustein aus, in den Sie eine Bausteingruppe importieren möchten, und klicken Sie dann auf **Importieren**.
3. Wählen Sie im Dialogfeld **Öffnen** die zu importierende Bausteingruppe aus, und klicken Sie dann auf **Öffnen**.
4. Wählen Sie im Dialogfeld **Importieren** die Berichtsdefinitionen aus, die importiert werden soll:

    - Um alle Berichtsdefinitionen und die unterstützenden Bausteine zu importieren, klicken Sie auf **Alles auswählen**.
    - Um bestimmte Berichte, Zeilen, Spalten, Baumstrukturen oder Dimensionssätze zu importieren, wählen Sie die Berichte, Zeilen, Spalten, Baumstrukturen oder Dimensionssätze aus, die importiert werden sollen.

5. Wenn Sie die Artikel ausgewählt haben, die Sie importieren möchten, klicken Sie auf **Importieren**.

### <a name="undo-a-checkout-of-a-building-block"></a>Das Auschecken eines Bausteins rückgängig machen

Wenn Sie einen Baustein öffnen, können andere Benutzer auf diesen Baustein nur im schreibgeschützten Modus zugreifen. Manchmal vergisst ein Benutzer, einen Baustein zu schließen oder schaltet das System ab, ohne den Baustein zu schließen. Dadurch bleibt der Baustein ausgecheckt und kein anderer Benutzer kann ihn öffnen. In diesen Fällen kann ein Administrator von Financial Reporting das Dialogfeld **Ausgecheckte Elemente** verwenden, um Bausteine einzuchecken, die ein Benutzer in einem ausgecheckten Zustand zurückgelassen hat.

> [!NOTE]
> Sie müssen die Rolle eines Administrators aufweisen, um Bausteine aus dem Dialogfeld **Ausgecheckte Elemente** einzuchecken.

1. Klicken Sie im Berichts-Designer im Menü **Extras** auf **Ausgecheckte Elemente**.
2. Aktivieren Sie im Dialogfeld **Ausgecheckte Elemente** das Kontrollkästchen **Elemente aller Benutzer anzeigen**. Die Liste wird aktualisiert und zeigt alle ausgecheckten Bausteine sowie die Benutzer an, die sie ausgecheckt haben.
3. Wählen Sie einen Baustein aus, und klicken Sie dann auf **Auschecken rückgängig machen**.
4. Klicken Sie auf **Ja**, um den Baustein einzuchecken.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Finanzberichterstellung](financial-reporting-intro.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]