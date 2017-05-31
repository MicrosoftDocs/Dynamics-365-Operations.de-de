---
title: "Funktionen des Stücklisten-Designers"
description: "In diesem Artikel wird beschrieben, wie Sie die Stücklisten-Designer-Seite verwenden können, um Strukturdarstellungen für Stücklisten (BOMs) zu entwerfen und anzuwenden. Sie können verschiedene Konfigurationen auswählen und festlegen, welche Informationen in den Positionen der Struktur enthalten sein sollen."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMDesigner
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 20981
ms.assetid: 2b92eec1-d28c-4965-9086-939c77b3c62b
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: c871cf4e5ee7f359010aac1fa0fef81e0e0df564
ms.contentlocale: de-de
ms.lasthandoff: 05/25/2017


---

# <a name="bom-designer-functionality"></a>Funktionen des Stücklisten-Designers

[!include[banner](../includes/banner.md)]


In diesem Artikel wird beschrieben, wie Sie die Stücklisten-Designer-Seite verwenden können, um Strukturdarstellungen für Stücklisten (BOMs) zu entwerfen und anzuwenden. Sie können verschiedene Konfigurationen auswählen und festlegen, welche Informationen in den Positionen der Struktur enthalten sein sollen.

Wenn Sie die Seite **Freigegebene Produkte** über die Seite **Stücklisten-Designer** öffnen, zeigt sie die Hierarchie der Stücklisten (BOMs) an, die aktiv und genehmigt sind für den ausgewählten Artikel, die standardmäßige Bestellwebsite des Artikels und das tatsächliche Datum.  

Klicken Sie auf **Filtern**, um die erste Auswahl in der Ansicht zu ändern. Wenn Sie das Anzeigeprinzip auf **Ausgewählt/Aktiv oder Ausgewählt** festlegen, können Sie einzelne Stückliste oder Arbeitsplanversionen aktivieren, um sie in der Ansicht zu verwenden. Sie können nicht genehmigte und nicht aktive Stücklistenversionen auswählen, um sie im Stücklisten-Designer anzuzeigen oder zu verwalten.  

**Hinweis:** Wenn Sie den Stücklisten-Designer über die Listenseite **Stücklisten** öffnen, werden keine Arbeitsplandaten angezeigt. Momentan ist die Auswahl einer Stücklisten- oder Arbeitsplanversion eine Eigenschaft der Stückliste und der Arbeitsplanversion, und gilt für alle Instanzen des Stücklisten-Designers.  

In den folgenden Abschnitten werden die Funktionen beschrieben, die auf verschiedenen Registerkarten des Stücklisten-Designers verfügbar sind.

## <a name="analyzing-a-bom-structure-by-using-the-bom-designer"></a>Eine Stücklistenstruktur mithilfe des Stücklisten-Designers analysieren
Der Stücklisten-Designer verfügt über zwei Abschnitte:

-   Die Strukturansicht der Stücklisten-Struktur.
-   Der Detailabschnitt, der Details der ausgewählten Daten anzeigt. Wenn Sie einen Knoten in der Strukturansicht auswählen, werden die Inforegister im Detailabschnitt auf diesem Knoten aktualisiert:
    -   **Stücklistenpositionsdetails** - Zeigt die Details der Stücklistenposition, der in der Strukturansicht aktiviert ist.
    -   **Artikeldaten** - Zeigt die Details des Hauptartikels oder des Artikels, der im ausgewählten Knoten verwendet wird. Sie können auf **Freigegebenes Produkt bearbeiten** klicken, um den ausgewählten Artikel zu verwalten.
    -   **Stückliste** - Zeigt den Kopf der Stückliste, die sich auf den ausgewählten Knoten bezieht.
    -   **Arbeitsplan** - Zeigt den Kopf des Arbeitsplans, der sich auf den ausgewählten Knoten bezieht.
    -   **Arbeitsplan-Arbeitsgänge** - Zeigt eine Vorschau der Arbeitsgänge für den Arbeitsplan. Wenn eine Stücklistenposition, die mit einem bestimmten Arbeitsgang zugewiesen ist, ausgewählt ist, wird der Arbeitsgang als **Komponente benötigt bei Arbeitsgängen** markiert.

## <a name="selecting-a-bom-and-route"></a>Auswählen einer Stückliste und des Arbeitsplans
Der Filter, der für die Stückliste und Arbeitsplan angewendet wird, wird im Kopf des Stücklisten-Designers angezeigt. Sie können den Filter ändern, indem Sie das Dialogfeld **Filtern** verwenden. In der folgenden Tabelle werden die Felder in diesem Dialogfeld beschrieben.

<table>
<thead>
<tr class="header">
<th>Feld</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Produktdimensionen</td>
<td>Wenn das ausgewählte Produkt ein Produktmaster ist, können Sie die aktiven Produktdimensionen für die Hauptauswahl definieren.<strong>Hinweis:</strong> Wenn Sie den Stücklisten-Designer für ein Produkt öffnen, das kein Produktmaster ist, können keine Produktdimensionen im Dialogfeld <strong>Filtern</strong> ausgewählt werden.</td>
</tr>
<tr class="even">
<td>Standort</td>
<td>Ändern Sie den Standort, für den die Stücklistenstruktur angezeigt wird. Der Standardstandort ist der standardmäßige Lagerstandort des Artikels.</td>
</tr>
<tr class="odd">
<td>Prinzip anzeigen</td>
<td>Wählen Sie das Prinzip für die Versionsanzeige aus, das für die aktuelle Stückliste sowie für den aktuellen Arbeitsplan gilt:
<ul>
<li>Wird das Prinzip auf <strong>Aktiv oder Ausgewählt/Aktiv</strong> festgelegt, wird die gültige Stückliste bzw. die Arbeitsplanversion für das entsprechende Datum gefunden.</li>
<li>Wird das Prinzip auf <strong>Ausgewählt/Aktiv oder Ausgewählt </strong>festgelegt ist, können Sie eine Stücklistenversion oder eine Arbeitsplanversion auswählen, indem Sie auf <strong>Stückliste </strong> &gt; <strong>Stücklistenversionen</strong> oder <strong>Arbeitsplan</strong> &gt;  <strong>Arbeitsplanversionen </strong>klicken.</li>
</ul></td>
</tr>
<tr class="even">
<td>Versionsdatum</td>
<td>Geben Sie hier das Versionsdatum für Stückliste und Arbeitsplan an. Mit der Version wird – gemäß den Versionsdaten in den Einstellungen zur Stücklistenversion – bestimmt, welche Stücklistenversion an einem bestimmten Datum verwendet werden soll.</td>
</tr>
<tr class="odd">
<td>Von Menge</td>
<td>Filtert die Versionen, indem Sie einen bestimmten Eintrag von der Menge auswählen. Wenn Sie einen Wert festlegen, könnten andere Stücklisten- und Arbeitsplanversionen ausgewählt werden.</td>
</tr>
<tr class="even">
<td>Nur Gültige anzeigen</td>
<td>Aktivieren Sie dieses Kontrollkästchen, zeigt die Strukturdarstellung ausschließlich Stücklistenpositionen mit gültigem Datum an. Klicken Sie entweder doppelt oder mit der rechten Maustaste auf eine Stücklistenposition, um die Seite <strong>Stücklistenposition bearbeiten</strong> zu öffnen und die Gültigkeitsdaten für diese Stücklistenposition anzuzeigen.</td>
</tr>
</tbody>
</table>

Wenn Sie den Stücklisten-Designer verwenden, um Stücklisten zu prüfen oder zu bearbeiten, die aus einer oder mehreren Ebenen von Phantomen bestehen, umfasst der Arbeitsplan, der dem obersten Artikel zugeordnet ist, in der Regel die vollständige Stücklistenhierarchie. Um die Übersicht zu vereinfachen, können Sie den Arbeitsplan der obersten Ebene sperren. Klicken Sie dazu auf **Anzeige**&gt; **Arbeitsplan sperren**. Wenn Sie den Arbeitsplan entsperren möchten, klicken Sie auf **Ansicht** &gt; **Arbeitsplan entsperren**.

## <a name="adding-and-editing-boms-and-bom-lines"></a>Stücklisten und Stücklistenpositionen hinzufügen und bearbeiten
Verwenden Sie die Funktionen **Stücklistenpositionen**oder **Stückliste**, um Stücklistenpositionen oder die Stückliste zu ändern. Wenn Sie einen Knoten in der Struktur auswählen, bestimmt der Typ des Knotens die Funktionen, die zur Verfügung stehen.

| Funktion                            | Beschreibung                                                                                               | Knotentyp und Bedingungen                                                                                                                                                                                                                                                                       |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Stücklistenpositionen &gt; Bearbeiten                 | Öffnet ein Dialogfeld, in dem Sie die Stücklistenpositionsattribute bearbeiten können.                                             | Diese Funktion ist verfügbar, wenn ein Stücklistenpositionsknoten aktiviert ist.                                                                                                                                                                                                                                   |
| Stücklistenpositionen &gt; Löschen               | Eine Stücklistenposition aus der ausgewählten Stückliste löschen.                                                                  | Diese Funktion ist nur verfügbar, wenn ein Stücklistenpositionsknoten ausgewählt wurde und die Stückliste nicht für die Bearbeitung gesperrt ist.                                                                                                                                                                                             |
| Stücklistenpositionen &gt; Vor Position hinzufügen      | Öffnet ein Dialogfeld, in dem Sie eine Produktvariante auswählen können, die vor der ausgewählten Stücklistenposition eingefügt werden soll.         | Diese Funktion ist verfügbar, wenn ein Stücklistenpositionsknoten aktiviert ist.                                                                                                                                                                                                                                   |
| Stücklistenpositionen &gt; Zur Komponenten-Stückliste hinzufügen | Öffnet ein Dialogfeld, in dem Sie eine Produktvariante auswählen können, die am Ende der ausgewählten Stückliste eingefügt werden soll.       | Diese Funktion ist verfügbar, wenn der ausgewählte Knoten eine ausgewählte Stückliste hat. Wenn diese Funktion nicht verfügbar ist, fehlt möglicherweise eine Stücklistenversion für die ausgewählte Artikelvariante. In diesem Fall können Sie auf **Stückliste**&gt; **Version erstellen** klicken, um die fehlende Version für den ausgewählten Knoten zu erstellen. |
| Stücklistenpositionen &gt; Nach Position hinzufügen       | Öffnet ein Dialogfeld, in dem Sie eine Produktvariante auswählen können, die nach der ausgewählten Stücklistenposition eingefügt werden soll.          | Diese Funktion ist verfügbar, wenn ein Stücklistenpositionsknoten aktiviert ist.                                                                                                                                                                                                                                   |
| Stückliste &gt; Version erstellen             | Erstellen einer neuen Stücklistenversion oder einer Stückliste für die Produktvariante des ausgewählten Knotens.                             | Diese Funktion ist nur verfügbar, wenn der Stücklistenpositionsknoten, der ausgewählt ist, in einen Artikel verknüpft ist, dessen Produktionstyp **Stückliste** oder **Formel** ist.                                                                                                                                                  |
| Stücklisten &gt;Kalkulation                | Öffnet ein Dialogfeld, in dem Sie die Kosten- oder Verkaufspreisberechnung für die ausgewählte Produktvariante ausführen können. | Diese Funktion ist verfügbar, wenn der ausgewählte Knoten sich auf eine Stücklistenversion bezieht.                                                                                                                                                                                                         |
| Stücklisten &gt; Prüfen                      | Validieren und überprüfen Sie die ausgewählte Stückliste.                                                                      | Diese Funktion ist verfügbar, wenn der ausgewählte Knoten sich auf eine Stücklistenversion bezieht.                                                                                                                                                                                                         |

## <a name="configuring-the-tree-view"></a>Konfigurieren der Strukturansicht
Klicken Sie auf **Einstellungen**, um die Informationen anzupassen, die in der Strukturansicht des Stücklisten-Designers angezeigt werden.

| Feldgruppe | Beschreibung                                                                                                                                                  |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Stückliste         | Verwenden Sie die Kontrollkästchen, um die Kriterien auszuwählen, die in der Strukturansicht angezeigt werden sollen. Die ausgewählten Kriterien werden im Stücklisten-Designer am unteren Rand der beiden Registerkarten angezeigt. |
| Route       | Verwenden Sie die Kontrollkästchen, um die Kriterien auszuwählen, die für die Arbeitspläne angezeigt werden sollen.                                                                                    |






