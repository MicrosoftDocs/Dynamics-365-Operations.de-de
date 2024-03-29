---
title: Berichtskomponente im Berichts-Designer organisieren
description: Dieser Artikel erläutert, wie vorhandene Berichte, Bausteine und Objekte im Berichts-Designer organisiert werden.
author: aprilolson
ms.date: 11/22/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: twheeloc
ms.custom: 59161
ms.assetid: 32e728c5-3b06-4049-8070-ade01e951d49
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a94a88114072792243026e441e6c5a62ee80fc56
ms.sourcegitcommit: d27fef61593c6d1e9e26d5c9fad21411bc52fabc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/23/2022
ms.locfileid: "9802687"
---
# <a name="organize-report-components-in-report-designer"></a>Organisieren von Berichtskomponenten im Berichtsdesigner

[!include [banner](../includes/banner.md)]

Nachdem Sie Bausteine und generierte Berichte entworfen haben, ist es hilfreich, diese Objekte zu organisieren, sodass sie vom Benutzer leichter gefunden werden können. Dieser Artikel erläutert, wie vorhandene Berichte, Bausteine und Objekte im Berichts-Designer organisiert werden.

Sie können Ordner, Berichte, Bausteine und andere Objekte im Report Designer umbenennen, um Ihre Dateien besser zu organisieren. Je nach Art des Objekts, das Sie umbenennen, müssen Sie möglicherweise Zuordnungen für das Objekt aktualisieren.

## <a name="rename-a-folder-or-building-block-in-report-designer"></a>Umbenennen eines Ordner oder Bausteins im Report Designer
Im Report Designer können Sie Ordner, Berichtsdefinitionen, Zeilendefinitionen, Spaltendefinitionen und Berichtsbaumstruktur-Definitionen umbenennen.

### <a name="rename-a-folder-or-building-block-in-report-designer"></a>Umbenennen eines Ordner oder Bausteins im Report Designer

1. Suchen Sie im Report Designer im Navigationsbereich nach dem umzubenennenden Ordner oder Objekt.
2. Klicken Sie mit der rechten Maustaste auf den Ordner oder das Objekt, und klicken Sie dann auf **Umbenennen**. Das Feld **Name** im Navigationsbereich ist nun verfügbar.
3. Geben Sie einen neuen Namen ein, und drücken Sie die **Eingabetaste**.
4. Wenn der Baustein eine Zeilendefinition, eine Spaltendefinition oder eine Berichtstruktur-Definition ist, müssen Sie weitere Bausteine, die dem Artikel zugeordnet sind, aktualisieren. Klicken Sie mit der rechten Maustaste auf den Baustein, den Sie in Schritt 3 umbenannt haben, wählen Sie **Zuordnungen**, und wählen Sie dann den Artikel in der Liste, um ihn zu aktualisieren.
5. Wiederholen Sie Schritt 4, bis alle zugeordneten Artikel aktualisiert wurden.

## <a name="create-and-manage-report-groups"></a>Erstellen und Verwalten von Berichtsgruppen
Sie können Berichtsdefinitionen gruppieren, um mehrere Berichte gleichzeitig zu generieren. Zum Erstellen, Ändern, Löschen und Generieren von Berichtsgruppen müssen Sie die Designer- oder Administrator-Rolle haben. Benutzer mit der Generator-Rolle können Berichtsgruppen generieren und anzeigen und die Benutzerberichtsdefinitions-Einstellungen für Berichtsgruppen ändern.

### <a name="create-a-report-group"></a>Erstellen einer Berichtsgruppe

1. Klicken Sie im Navigationsbereich des Report Designers auf **Berichtsgruppen**.
2. Klicken Sie im Menü **Datei** auf **Neu** &gt; **Berichtsgruppendefinition**, um eine neue Berichtsgruppe im Viewer-Fenster öffnen. Klicken Sie alternativ auf die Schaltfläche **Berichtsgruppe** ![Berichtsgruppe.](media/report-group.gif "Berichtsgruppe") auf der Symbolleiste.
3. Klicken Sie auf die Registerkarte **Berichtsgruppe**. Um die Informationen zu den einzelnen Berichtsdefinitionen für die Generierung dieses Berichts zu überschreiben, aktivieren Sie das Kontrollkästchen **Überschreiben von Unternehmen, Details und Datumseinstellungen von einzelnen Berichtsdefinitionen**. Die Felder Unternehmensname, Detailebene, vorläufige Einstellungen und Datumsinformationen werden automatisch ausgefüllt, aber Sie können Aktualisierungen vornehmen.
4. Um mehrere Berichte zu generieren, die die Berichtswährung anzeigen, aktivieren Sie das Kontrollkästchen **Alle Berichtswährungen einschließen**. Es sind mehrere Ansichten verfügbar, wenn Sie den Bericht anzeigen und auf die Schaltfläche **Währung** im Web-Viewer klicken.
5. Klicken Sie im Feld **Berichte in Gruppe** auf **Hinzufügen**, um die Berichte zu wählen, die in die Berichtsgruppe einbezogen werden sollen. Um mehrere Berichte im Dialogfeld **Hinzufügen** auszuwählen, halten Sie STRG-Taste gedrückt, während Sie Berichte auswählen. Wenn Sie die Berichtsauswahl abgeschlossen haben, klicken Sie auf **OK**.
6. Klicken Sie auf **Datei** &gt; **Speichern**, um die neue Berichtsgruppe zu speichern.

### <a name="modify-a-report-group"></a>Ändern einer Berichtsgruppe

1. Klicken Sie im Navigationsbereich des Report Designers auf **Berichtsgruppen**.
2. Doppelklicken Sie auf die zu ändernde Berichtsgruppe.
3. Nehmen Sie auf der Registerkarte **Berichtsgruppe** die gewünschten Änderungen vor.
4. Klicken Sie im Menü **Datei** auf **Speichern**, um die geänderte Berichtsgruppe zu speichern. Alternativ klicken Sie auf die Schaltfläche **Speichern** ![Speichern](media/save.gif "Speichern") auf der Symbolleiste.

> [NOTE] Wenn Sie einen Zeitplan für die Berichtserstellung haben, können Sie diese Einstellungen überschreiben und einen Bericht sofort generieren.

### <a name="generate-a-report-group-report"></a>Generieren eines Berichtsgruppenberichts

1. Klicken Sie im Navigationsbereich des Report Designers auf **Berichtsgruppen**.
2. Öffnen Sie die zu generierende Berichtsgruppe.
3. Klicken Sie auf die Schaltfläche **Bericht generieren** ![Bericht generieren](media/generate-report.gif "Bericht generieren"), um Berichte zu generieren.

### <a name="delete-a-report-group"></a>Löschen einer Berichtsgruppe

1. Klicken Sie im Navigationsbereich des Report Designers auf **Berichtsgruppen**.
2. Zum Löschen klicken Sie im Navigationsbereich mit der rechten Maustaste auf die Berichtsgruppe, und wählen Sie dann **Löschen** aus.
3. Wenn eine Bestätigungsmeldung angezeigt wird, klicken Sie auf **Ja**.

## <a name="report-group-tab-controls"></a>Berichtsgruppen-Registerkartensteuerelemente
In der folgenden Tabelle werden die Steuerelemente der Registerkarte **Berichtsgruppen** beschrieben.

<table>
<thead>
<tr>
<th>Steuerung</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>Überschreiben von Unternehmen, Details und Datumseinstellungen von einzelnen Berichtsdefinitionen</td>
<td>Aktivieren Sie dieses Kontrollkästchen, um einzelne Berichtsdefinitionen der Berichte in dieser Berichtsgruppe für die Generierung dieser Berichte zu überschreiben.</td>
</tr>
<tr>
<td>Unternehmensname</td>
<td>Wählen Sie das Unternehmen für die Berichte aus.</td>
</tr>
<tr>
<td>Detailebene</td>
<td>Spezifizieren Sie die für den Bericht gewünschte Detailstufe.
<ul>
<li><strong>Financial</strong> − Ein übergeordneter Zusammenfassungsbericht. Sie können keine Detailinformationen zu Konten und Dimensionen durchführen, ausgenommen derer, die Sie über die Berichtstruktur hinzugefügt haben.</li>
<li><strong>Finanzen &amp; Konto</strong> − Ein Bericht, der eine übergeordnete Zusammenfassung und Kontodetails enthält.</li>
<li><strong>Finanzen, Konto &amp; Buchung</strong> − Ein Bericht, der eine übergeordnete Zusammenfassung und Buchungsdetails enthält.</li>
</ul></td>
</tr>
<tr>
<td>Vorläufig</td>
<td>Spezifizieren Sie die für den Bericht gewünschten Aktivitätstypen.
<ul>
<li><strong>Nur gebuchte Aktivität</strong> − Enthält nur die Buchungen und Salden, die in den Finanzdaten gebucht wurden.</li>
<li><strong>Gebuchte und nicht gebuchte Aktivität</strong> − Enthält alle Buchungen und Salden, die in den Finanzdaten eingegeben und gebucht wurden.</li>
<li><strong>Nur nicht gebuchte Aktivität</strong> − Enthält nur Buchungen, die in die Finanzdaten eingegeben, aber noch nicht gebucht wurden.</li>
</ul></td>
</tr>
<tr>
<td>Alle Berichtswährungen einschließen</td>
<td>Alle zusätzlichen Berichtswährungen, die in Ihrem Microsoft Dynamics 365 Finance konfiguriert sind, werden hier aufgeführt. Wählen Sie dieses Kontrollkästchen aus, um zusätzliche Berichte in den angegebenen Währungen zu generieren. Sie können dann im Web-Viewer angezeigt werden, indem Sie auf die Schaltfläche <strong>Währung</strong> klicken und eine Währung auswählen.</td>
</tr>
<tr>
<td>Nicht mit Berichtsdefinition gespeicherte Datumsinformationen</td>
<td><ul>
<li>Basisperiode</li>
<li>Basisjahr</li>
<li>Berücksichtigter Zeitraum</li>
</ul>
Nur Einstellungen zum Standardbasiszeitraum werden mit der Berichtsdefinition gespeichert.</td>
</tr>
<tr>
<td>Mit Berichtsdefinition gespeicherte Datumsinformationen</td>
<td><ul>
<li>Berichtsdatum</li>
<li>Standardbasiszeitraum</li>
</ul></td>
</tr>
<tr>
<td>Berichte in Gruppe</td>
<td>Fügen Sie Berichte in der Berichtsgruppe hinzu, entfernen Sie sie aus dieser oder sortieren Sie sie neu.
<ul>
<li>Doppelklicken Sie zum Hinzufügen von Berichtsdefinitionen zur Berichtsgruppe auf die Berichtsgruppe, um sie zu öffnen, und klicken Sie dann auf <strong>Hinzufügen</strong>. Wählen Sie die Berichte aus, die in die Berichtsgruppe eingefügt werden sollen, und klicken Sie dann auf <strong>OK</strong>.</li>
<li>Wählen Sie zum Entfernen eines Berichts aus der Berichtsgruppe den Bericht aus, und klicken Sie dann auf <strong>Entfernen</strong>.</li>
<li>Um die Reihenfolge zu ändern, in der die Berichte generiert werden, wählen Sie einen Bericht in der Liste aus, und klicken anschließend auf <strong>Nach oben verschieben</strong> oder <strong>Nach unten verschieben</strong>.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Finanzberichterstellung](financial-reporting-intro.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
