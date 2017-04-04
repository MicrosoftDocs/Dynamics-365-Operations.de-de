---
title: Finanzberichtkomponenten
description: "Dieser Artikel beschreibt die Verwendung der Komponenten, der Bausteine oder Berichtsdefinitionen in der Finanzberichterstellung. Diese Bausteine beinhalten Zeilendefinitionen, Spaltendefinitionen und Berichtstruktur-Definitionen. Dieser Artikel erläutert, wie Bausteine organisiert und gesperrt werden, und wie Sie mit Bausteingruppen arbeiten."
author: RobinARH
manager: AnnBe
ms.date: 2016-03-07 18 - 54 - 02
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 59071
ms.assetid: a201cfcb-1672-45f6-897d-2db2dd181d9a
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: a423dff4d8796f454c9c4db03c8ceb2b8c3d6456
ms.lasthandoff: 03/30/2017


---

# <a name="financial-report-components"></a>Finanzberichtkomponenten

Dieser Artikel beschreibt die Verwendung der Komponenten, der Bausteine oder Berichtsdefinitionen in der Finanzberichterstellung. Diese Bausteine beinhalten Zeilendefinitionen, Spaltendefinitionen und Berichtstruktur-Definitionen. Dieser Artikel erläutert, wie Bausteine organisiert und gesperrt werden, und wie Sie mit Bausteingruppen arbeiten. 

Die Designphilosophie hinter dem Finanzberichtdesigner ist, Informationen in kleinste Komponenten oder Grundbausteine zu zerteilen, sie zu mischen und nach Bedarf zusammenzufügen. Daher ist die Berichtsformatierung von Ihren finanziellen Daten geetrennt, und Sie können das Design eines Berichts ändern, ohne die Finanzdaten in Ihrem Microsoft Dynamics ERP-System zu ändern. Mithilfe dieses Bausteinansatzes können Sie Text, Beträge und Berechnungen kombinieren, um die Berichte zu erstellen, die Sie benötigen. Zudem fördert diese Flexibilität die Kreativität, indem es das Anzeigen Ihrer Arbeitsgänge auf unterschiedliche Arten erleichtert. Die einzelnen Bausteine einer Berichtsdefinition sind einem dreidimensionalen Arbeitsblatt ähnlich, sie bieten jedoch mehr Leistung. Eine Berichtsdefinition gibt die Zeilendefinition, die Spaltendefinition und die optionale Berichtstruktur-Definition an, die für den Bericht verwendet werden sollte. Sie umfasst auch Informationen zum Speicherort des generierten Berichts und wie er formatiert wird. Zur besseren Wiederverwendung und Freigabe können Sie eine Baustein-Gruppe erstellen, die eine Sammlung vorhandener Berichtsdefinitionen, Zeilendefinitionen, Spaltendefinitionen, Berichtstruktur-Definitionen und Dimensionssätze ist, die einem Unternehmen zugeordnet sind.

## <a name="building-blocks-of-a-report"></a> Bausteine eines Berichts
| Baustein            | Beschreibung                                                                                                                                                                                                                                                                              | Weitere Informationen                                                                                                 |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Zeilendefinition            | Eine Zeilendefinition definiert die beschreibenden Positionen (z. B. Löhne oder Verkäufe), in einem Bericht. Sie listet auch Segmentwerte oder Dimensionen auf, die die Werte für jeden Positionsartikel enthalten und schließt Zeilenformatierung und Berechnungen ein.                                                    | [Zeilendefinitionen](row-definitions-financial-reporting.md)                       |
| Spaltendefinition         | Eine Spaltendefinition definiert die Periode, die verwendet werden soll, wenn Daten aus den Finanzdimensionen extrahiert werden. Sie umfasst auch Spaltenformatierung und Berechnungen.                                                                                                                                 | [Spaltendefinitionen](column-definitions-financial-reports.md)         |
| Berichtsbaumstruktur-Definition | Eine Berichtsbaumstruktur-Definition ähnelt einem Organigramm. Sie enthält einzelne Berichtseinheiten, die jedes Feld im Diagramm darstellen. Die Einheiten können entweder einzelne Abteilungen aus den Finanzdaten oder Einheiten auf einer höheren Ebene sein, die Daten aus anderen Berichtseinheiten zusammenfassen. | [Berichtsbaumstruktur-Definitionen](financial-reporting-tree-definitions.md) |
| Berichtsdefinition         | Eine Berichtsdefinition verwendet eine Zeilendefinition, eine Spaltendefinition und eine optionale Berichtsbaumstruktur-Definition, um den Bericht zu erstellen. Sie bietet auch zusätzliche Optionen und Einstellungen, die Sie verwenden können, um einen Bericht anzupassen.                                                                    | [Berichtsdefinition](design-financial-report-definitions.md)                  |

Wenn das Entwerfen von Berichten neu für Sie ist, ist es hilfreich, den Berichts-Assistenten zu verwenden, um schnell eine Berichtsdefinition zu erstellen, die Sie später anpassen können. Wenn Sie Erfahrung im Entwerfen von Berichten haben und mehr Flexibilität in der Berichtserstellung möchten, können Sie neue oder vorhandene Bausteine kombinieren, um eine neue Berichtsdefinition zu erstellen. Sie müssen nicht alle verfügbaren Berichtsdefinitionsoptionen vollständig verstehen, um Qualitätsberichte zu erzeugen. Während Sie mit dem Entwerfen von Berichten vertraut sind, können Sie Ihre Berichtsdefinitionen erweitern, um weitere erweiterte Funktionalität nutzen zu können. Nachdem Sie einen einfachen Bericht erstellt haben, können Sie die Berichtsdefinition und alle der Bausteine in der Berichtsdefinition anpassen.

## <a name="organize-the-building-blocks"></a>Organisieren der Bausteine
Verwenden Sie Ordner, um die Bausteine im Berichts-Designer zu organisieren. Alle Ordner sind für den Typ des Bausteins, den sie enthalten, spezifisch. Beispielsweise befinden sich alle Ordner, die Zeilendefinitionen enthalten, im Bereich **Zeilendefinitionen** des Berichts-Designers.

### <a name="create-a-folder"></a>Erstellen eines Ordners

1.  Im Berichts-Designer wählen Sie den Typ des Bausteins aus, der im Navigationsbereich organisiert werden soll. Beispielsweise klicken Sie zum Sortieren eine Zeilendefinition auf **Zeilendefinitionen**.
2.  Wählen Sie im Navigationsbereich den vorhandenen Ordner, unter dem der neue Ordner erstellt wird, und führen Sie dann die folgenden Schritte aus:
    -   Klicken Sie mit der rechten Maustaste auf den übergeordneten Ordner, und wählen Sie dann **Neuer Ordner** aus.
    -   Wählen Sie den übergeordneten Ordner aus, klicken dann auf **Datei** und anschließend auf **Neuer Ordner**.

3.  Wenn der neue Ordner angezeigt wird, geben Sie den Namen des neuen Ordners ein und drücken die Eingabetaste.

## <a name="lock-a-building-block"></a> Einen Baustein sperren
Sie können ein Kennwort erstellen, um einen Baustein zu schützen und zu sperren. Auf diese Wiese wird einer Berichtskomponente eine Sicherheitsstufe hinzugefügt, ohne das gesamte System zu sichern. Ein Passwort kann Bausteininformationen schützen, die für Ihren Berichterstellungsprozess am Monatsende von Bedeutung sind. Ein Benutzer in einer beliebigen Rolle kann einen Baustein sperren. Andere Benutzer haben jedoch lediglich Lese-Zugriff auf eine gesperrte Komponente. Benutzer können die gesperrte Komponente öffnen, ändern und unter neuem Namen speichern. Ein Benutzer, der die Rolle "Administrator" hat, hat immer Zugriff und kann einen gesperrten Baustein ändern.
1.  Öffnen Sie im Berichts-Designer die zu schützende Berichtskomponente, wie eine Zeilendefinition, eine Spaltendefinition, eine Berichtsdefinition oder eine Berichtstruktur-Definition.
2.  Klicken Sie im Menü **Extras** auf **Schützen/Schutz aufheben**. Sie können auch in der Symbolleiste auf **Schützen/Schutz aufheben** (das Schlosssymbol) klicken.
3.  Geben Sie im Dialogfeld **Schützen** ein Passwort ein, bestätigen es und klicken dann auf **OK**. Das Schlosssymbol in der Symbolleiste wird hervorgehoben, wenn ein offener Baustein gesperrt ist.

Um einen gesperrten Baustein zu entsperren, öffnen Sie den Baustein, und klicken Sie anschließend auf **Schützen/Schutz aufheben** in der Symbolleiste. Oder klicken Sie im Menü **Extras** auf **Schutz aufheben**.

## <a name="building-block-groups"></a>Baustein-Gruppen

Bausteine sind die Zeilendefinitionen, Spaltendefinitionen, Berichtsbaumstruktur-Definitionen und Berichtsdefinitionen, die Sie für einen Bericht erstellen. Bausteingruppen sind Sammlungen der Definitionen und Dimensionssätze, die einem Unternehmen zugeordnet sind. Bausteingruppen können unternehmensspezifisch sein, oder mehrere Unternehmen können die gleiche Gruppe von Bausteinen teilen. Wenn einige Ihrer Unternehmen unterschiedliche Kontenpläne haben, möchten Sie möglicherweise für jedes Unternehmen eine andere Bausteingruppe verwenden. Alternativ können Sie alle Ihre einzelnen Bausteine benennen, um anzugeben, mit welchem Unternehmen sie kompatibel sind.
### <a name="create-a-building-block-group"></a>Eine Baustein-Gruppe erstellen

1.  Im Berichts-Designer klicken Sie im Menü **Unternehmen** auf **Bausteingruppen**.
2.  Klicken Sie im Dialogfeld **Bausteingruppen** auf **Neu**.
3.  Geben Sie einen eindeutigen Namen und eine Beschreibung für die Bausteingruppe ein. Jedes Feld kann maximal 256 Zeichen enthalten. (Diese Nummer enthält Leerzeichen.)
4.  Klicken Sie auf **OK**, um die neue Bausteingruppe zu erstellen.

### <a name="assign-a-building-block-group"></a>Eine Baustein-Gruppe zuweisen

Nachdem Sie ein Bausteingruppe erstellt haben, muss sie mindestens einem Unternehmen zugewiesen werden. Sie können nun Berichts-, Zeilen-, Spalten- und Berichtsstruktur-Definitionen erstellen und in der Bausteingruppe speichern. Sie müssen alle Bausteine schließen, bevor Sie das folgende Verfahren beginnen.
1.  Klicken Sie im Berichts-Designer im Menü **Unternehmen** auf **Unternehmen**.
2.  Wählen Sie im Dialogfeld **Unternehmen** das Unternehmen aus, dem Sie eine Bausteingruppe zuweisen.
3.  Klicken Sie auf **Ändern**.
4.  Wählen Sie im Dialogfeld **Unternehmen ändern** im Feld **Bausteingruppe** die Bausteingruppe aus, die dem Unternehmen zugewiesen wird, oder klicken Sie auf **Neu**, um eine Bausteingruppe zu erstellen.
5.  Klicken Sie auf **OK**, um die neue Bausteingruppe zuzuweisen.
6.  Klicken Sie auf **Schließen**, um das Dialogfeld **Unternehmen** zu schließen. Die Bausteingruppe, die Sie ausgewählt haben, wird nun dem Unternehmen zugewiesen. Jetzt sind alle neu erstellten Zeilendefinitionen, Spaltendefinitionen, usw., Teil der Bausteingruppe, die diesem Unternehmen zugewiesen wurde. Sie können auch eine .tdbx-Datei oder einen Bericht von einem anderen System importieren.

### <a name="view-a-building-block-group"></a> Eine Baustein-Gruppe anzeigen

Nachdem eine Baustein-Gruppe erstellt wurde und verwendet wird, können Sie die Bausteine sehen, die ihm zugewiesen sind. Sie können auch Bausteingruppen exportieren oder importieren und zusätzlich verwalten.
1.  Klicken Sie im Berichts-Designer im Menü **Unternehmen** auf **Bausteingruppen**.
2.  Wählen Sie im Dialogfeld **Baustein-Gruppen** den Baustein aus, der angezeigt werden soll.
3.  Klicken Sie auf **Anzeigen**, um das Dialogfeld **Bausteingruppe anzeigen** zu öffnen und den Inhalt der Bausteingruppe anzuzeigen.
4.  Klicken Sie auf **Schließen**, um die Dialogfelder zu schließen.

### <a name="save-a-building-block-group-under-a-new-name"></a>Eine Bausteingruppe unter neuem Namen speichern

Sie können eine vorhandene Bausteingruppe unter einen neuen Namen speichern. Anschließend können Sie die neue Bausteingruppe ändern, ohne die ursprüngliche Bausteingruppe zu ändern.
1.  Klicken Sie im Berichts-Designer im Menü **Unternehmen** auf **Bausteingruppen**.
2.  Wählen Sie im Dialogfeld **Bausteingruppen** die Bausteingruppe aus, die unter einem neuen Namens gespeichert werden soll.
3.  Klicken Sie auf **Speichern unter**.
4.  Geben Sie einen neuen Namen und eine Beschreibung für die Bausteingruppe ein.
5.  Klicken Sie auf **OK**. Die neue Bausteingruppe erscheint im Dialogfeld **Baustein-Gruppen**.

### <a name="export-a-building-block-group"></a> Eine Baustein-Gruppe exportieren

Sie können eine Bausteingruppe oder bestimmte Berichtsbausteine innerhalb einer Bausteingruppe exportieren. Sie können die exportierte Bausteingruppe als Sicherung verwenden. Auf der exportierten Daten zwischen Bausteingruppen oder Dynamics 365 für Arbeitsgangsinstallationen Ziele kopieren. Berichts-Designer schließt die verwiesen Schriftschnitte und Dimensionssätze zusammen mit der Bausteingruppe ein.
1.  Klicken Sie im Berichts-Designer im Menü **Unternehmen** auf **Bausteingruppen**.
2.  Wählen Sie im Dialogfeld **Baustein-Gruppen** die Bausteingruppe aus, die exportiert werden soll, und klicken Sie auf **Exportieren**.
3.  Wählen Sie im Dialogfeld **Exportieren** die Berichtsdefinitionen aus, die exportiert werden soll:
    -   Um alle Ihre Berichtsdefinitionen und die zugeordneten Bausteine zu exportieren, klicken Sie auf **Alles auswählen**.
    -   Um bestimmte Berichte, Zeilen, Spalten, Strukturen oder Dimensionssätze zu exportieren, klicken Sie auf die entsprechende Registerkarte und wählen die Artikel aus, die exportiert werden sollen. Halten Sie die STRG-Taste gedrückt, um mehrere Artikel in einer Registerkarte auszuwählen. **Hinweis**: Wenn Sie Berichte zum Exportieren auswählen, werden die zugeordneten Zeilen, Spalten, Strukturen und Dimensionssätze ausgewählt.

4.  Wenn Sie die Artikel ausgewählt haben, die Sie exportieren möchten, klicken Sie auf **Exportieren**.
5.  Wählen Sie im Dialogfeld **Speichern unter** einen Speicherort aus, an den die Bausteingruppe exportiert wird.
6.  Geben Sie im Feld **Dateiname** einen Namen für die Datei ein. Der Berichts-Designer fügt automatisch eine .tdbx-Dateinamenerweiterung hinzu.
7.  Klicken Sie auf **Speichern**. Die Bausteingruppe wird an dem Speicherort gespeichert, der von Ihnen angegeben wurde.

### <a name="import-a-building-block-group"></a> Eine Baustein-Gruppe importieren

Sie können eine Bausteingruppe in eine bereits bestehende Bausteingruppe importieren oder eine neue Bausteingruppe für die Daten erstellen. Alle importierten Bausteingruppen behalten ihre ursprünglichen Schriftarten und Unternehmensreferenzen bei und enthalten die entsprechenden Dimensionssätze.
1.  Klicken Sie im Berichts-Designer im Menü **Unternehmen** auf **Bausteingruppen**.
2.  Wählen Sie im Dialogfeld **Baustein-Gruppen** die Bausteingruppe aus, in die eine Bausteingruppe importiert werden soll, und klicken Sie auf **Importieren**.
3.  Wählen Sie im Dialogfeld **Öffnen** die Bausteingruppe aus, die importiert werden soll, und klicken Sie auf **Öffnen**.
4.  Wählen Sie im Dialogfeld **Importieren** die Berichtsdefinitionen aus, die importiert werden soll:
    -   Um alle Berichtsdefinitionen und die unterstützenden Bausteine zu importieren, klicken Sie auf **Alles auswählen**.
    -   Um bestimmte Berichte, Zeilen, Spalten, Baumstrukturen oder Dimensionssätze zu importieren, wählen Sie die Berichte, Zeilen, Spalten, Baumstrukturen oder Dimensionssätze aus, die importiert werden sollen.

5.  Wenn Sie die Artikel ausgewählt haben, die Sie importieren möchten, klicken Sie auf **Importieren**.

### <a name="undo-a-checkout-of-a-building-block"></a>Das Auschecken eines Bausteins rückgängig machen

Wenn Sie einen Baustein öffnen, können andere Benutzer auf diesen Baustein nur im schreibgeschützten Modus zugreifen. Manchmal vergisst ein Benutzer, einen Baustein zu schließen oder schaltet das System ab, ohne den Baustein zu schließen. Dadurch bleibt der Baustein ausgecheckt und kein anderer Benutzer kann ihn öffnen. In diesen Fällen kann ein Finanzbericht-Administrator das Dialogfeld **Ausgecheckte Elemente** verwenden, um Bausteine einzuchecken, die ein Benutzer in einem ausgecheckten Zustand zurückgelassen hat. **Hinweis**: Sie müssen die Administrator-Rolle haben, um Bausteine vom Dialogfeld **Ausgecheckte Elemente** einzuchecken.
1.  Klicken Sie im Berichts-Designer im Menü **Extras** auf **Ausgecheckte Elemente**.
2.  Wählen Sie im Dialogfeld **Ausgecheckte Elemente** die Option **Elemente aller Benutzer anzeigen** aus. Die Liste wird aktualisiert, um alle Bausteine anzuzeigen, die ausgecheckt sind, sowie die Benutzer, die sie ausgecheckt haben.
3.  Wählen Sie einen Baustein aus, und klicken Sie anschließend **Auschecken rückgängig machen**.
4.  Klicken auf **Ja**, um den Bausteins einzuchecken.

# <a name="see-also"></a>Siehe auch

[Finanzberichterstellung in Microsoft Dynamics ERP](financial-reporting-intro.md)


