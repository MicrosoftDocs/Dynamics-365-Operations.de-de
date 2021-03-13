---
title: Formeldesigner
description: In diesem Thema wird erläutert, wie der Formel-Designer verwendet wird, um Formeln in einer Strukturansicht zu analysieren und zu verwalten.
author: cvocph
manager: tfehr
ms.date: 06/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PlanActivity, ReqSupplyDemandSchedule
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 49ec2ac0ce32da13239f3b7789d6f73f22f6e61b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007199"
---
# <a name="formula-designer"></a>Formeldesigner

[!include [banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie der Formel-Designer verwendet wird, um Formeln in einer Strukturansicht zu analysieren und zu verwalten.

Wenn die Seite **Formeldesigner** auf der Seite **Freigegebene Produkte** öffnen, zeigt die Struktur im linken Fensterbereich die Liste von Kuppelprodukte und der Substanzhierarchie für das freigegebene Produkt. Die Struktur wird von der Hierarchie von Formeln abgeleitet, die aktiv und für den ausgewählten Artikel, und die zugehörigen Substanzen, die standardmäßigen Bestellwebsite des Artikels und das tatsächlichen Datum genehmigt sind.

Klicken Sie auf **Einrichten**, um verschiedene Konfigurationen auszuwählen und festzulegen, welche Informationen in den Positionen der Struktur enthalten sein sollen.

Klicken Sie auf **Filtern**, um die erste Auswahl in der Ansicht zu ändern. Wenn Sie das Anzeigeprinzip auf **Ausgewählt/Aktiv** oder **Ausgewählt** festlegen, können Sie einzelne Formeln oder Arbeitsplanversionen aktivieren, um sie in der Ansicht zu verwenden. Sie können nicht genehmigte und nicht aktive Formelversionen auswählen, um sie im Formel-Designer anzuzeigen oder zu verwalten.  

> [!NOTE]
> Hinweis: Wenn Sie die Seite **Formel-Designer** über die Listenseite **Stücklisten** öffnen, werden keine Arbeitsplandaten angezeigt. Momentan gilt die Auswahl einer Formel bzw. die Arbeitsplanversion für alle Instanzen des Formel-Designers.  

In den folgenden Abschnitten werden die Funktionen beschrieben, die im Stücklisten-Designers verfügbar sind.

## <a name="analyze-a-formula-structure-by-using-the-formula-designer"></a>Analysieren einer Formelstruktur mit dem Formel-Designer
Der Formel-Designer verfügt über zwei Abschnitte:

-   Die Strukturansicht der Formel-Struktur.
-   Der Detailabschnitt, der Details der ausgewählten Daten anzeigt. Wenn Sie einen Knoten in der Strukturansicht auswählen, werden die Inforegister im Detailabschnitt auf diesem Knoten aktualisiert:
    -   **Formellistenpositionsdetails** – Zeigen Sie die Details der Formellistenposition an, der in der Strukturansicht aktiviert ist.
    -   **Artikeldaten** – Zeigen Sie die Details des Hauptartikels oder des Artikels an, der im ausgewählten Knoten verwendet wird. Sie können auf **Freigegebenes Produkt bearbeiten** klicken, um den ausgewählten Artikel zu verwalten.
    -   **Formel** – Zeigen Sie die Kopfzeile der Formel in Zusammenhang mit dem ausgewählten Knoten an.
    -   **Arbeitsplan** – Zeigen Sie den Kopf des Arbeitsplans an, der sich auf den ausgewählten Knoten bezieht.
    -   **Arbeitsplan-Arbeitsgänge** – Zeigen Sie eine Vorschau der Arbeitsgänge für den Arbeitsplan an. Wenn eine Stücklistenposition, die mit einem bestimmten Arbeitsgang zugewiesen ist, ausgewählt ist, wird der Arbeitsgang als **Komponente benötigt bei Arbeitsgängen** markiert.

## <a name="select-a-formula-and-route"></a>Formel und Arbeitsplan auswählen
Der Filter, der für die Formel und den Arbeitsplan angewendet wird, wird im Kopf des Formel-Designers angezeigt. Sie können den Filter ändern, indem Sie das Dialogfeld **Filtern** verwenden. In der folgenden Tabelle werden die Felder in diesem Dialogfeld beschrieben.

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
<td>Wenn das ausgewählte Fertigprodukt ein Produktmaster ist, können Sie die aktiven Produktdimensionen für die Hauptauswahl definieren. Beachten Sie, dass beim Öffnen des Formel-Designers für ein Produkt, das kein Produktmaster ist, im Dialogfeld <strong>Filtern</strong> keine Produktdimensionen ausgewählt werden können.</p></td>
</tr>
<tr class="even">
<td>Standort</td>
<td>Ändern Sie den Standort, für den die Substanzstruktur angezeigt wird. Der Standardstandort ist der standardmäßige Lagerstandort des Artikels.</td>
</tr>
<tr class="odd">
<td>Prinzip anzeigen</td>
<td><p>Wählen Sie das Prinzip für die Versionsanzeige aus, das für die aktuelle Formelstruktur sowie für den aktuellen Arbeitsplan gilt:</p>
<ul>
<li>Wird das Prinzip auf <strong>Aktiv</strong> oder <strong>Ausgewählt/Aktiv</strong> festgelegt, wird die gültige Formel bzw. die Arbeitsplanversion für das entsprechende Datum gefunden.</li>
<li>Wird das Prinzip auf <strong>Ausgewählt/Aktiv</strong> oder <strong>Ausgewählt</strong> festgelegt ist, können Sie eine Formellistenversion oder eine Arbeitsplanversion auswählen, indem Sie auf <strong>Formel</strong> &gt; <strong>Formelversionen</strong> oder <strong>Arbeitsplan</strong> &gt; <strong>Arbeitsplanversionen</strong> klicken.</li>
</ul></td>
</tr>
<tr class="even">
<td>Versionsdatum</td>
<td>Dient zum Eingeben des Versionsdatums für Formel und Arbeitsplan. Die Version bestimmt, welche Formelversion gemäß den Versionsdatumsangaben in den Formelversionseinstellungen an einem bestimmten Datum verwendet wird.</td>
</tr>
<tr class="odd">
<td>Von Menge</td>
<td>Filtert die Versionen, indem Sie eine bestimmte &quot;von&quot;-Menge auswählen. Wenn Sie einen Wert festlegen, könnten andere Formel- und Arbeitsplanversionen ausgewählt werden.</td>
</tr>
<tr class="even">
<td>Nur Gültige anzeigen</td>
<td>Aktivieren Sie dieses Kontrollkästchen, zeigt die Strukturdarstellung ausschließlich Formelpositionen mit gültigem Datum an. Klicken Sie entweder doppelt oder mit der rechten Maustaste auf eine Formelposition, um die Seite <strong>Formelposition bearbeiten</strong> zu öffnen und die Gültigkeitsdaten für diese Formelposition anzuzeigen.</td>
</tr>
</tbody>
</table>

Wenn Sie den Formel-Designer verwenden, um Formeln zu prüfen oder zu bearbeiten, die aus einer oder mehreren Ebenen von Phantomen bestehen, umfasst der Arbeitsplan, der dem obersten Artikel zugeordnet ist, in der Regel die vollständige Formelhierarchie. Um die Übersicht zu vereinfachen, können Sie den Arbeitsplan der obersten Ebene sperren. Klicken Sie dazu auf **Anzeige** &gt; **Arbeitsplan sperren**. Wenn Sie den Arbeitsplan entsperren möchten, klicken Sie auf **Ansicht** &gt; **Arbeitsplan entsperren**.

## <a name="add-and-edit-formulas-and-formula-lines"></a>Hinzufügen und Bearbeiten von Formeln und Formelpositionen
Verwenden Sie die Funktionen **Formelpositionen** oder **Formel**, um Formelpositionen oder die Stückliste zu ändern. Wenn Sie einen Knoten in der Struktur auswählen, bestimmt der Typ des Knotens die Funktionen, die zur Verfügung stehen.

| Funktion                            | Beschreibung                                                                                               | Knotentyp und Bedingungen |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|--------------------------|
| Stücklistenpositionen &gt; Bearbeiten                 | Öffnet ein Dialogfeld, in dem Sie die Formelpositionsattribute bearbeiten können.                                         | Diese Funktion ist verfügbar, wenn ein Formelpositionsknoten aktiviert ist. |
| Stücklistenpositionen &gt; Löschen               | Löschen Sie eine Formelposition aus der ausgewählten Formel.                                                          | Diese Funktion ist nur verfügbar, wenn ein Formelpositionsknoten ausgewählt wurde und die Formel nicht für die Bearbeitung gesperrt ist. |
| Stücklistenpositionen &gt; Vor Position hinzufügen      | Öffnet ein Dialogfeld, in dem Sie eine Produktvariante auswählen können, die vor der ausgewählten Formelposition eingefügt werden soll.     | Diese Funktion ist verfügbar, wenn ein Formelpositionsknoten aktiviert ist. |
| Stücklistenpositionen &gt; Zur Komponenten-Stückliste hinzufügen | Öffnet ein Dialogfeld, in dem Sie eine Produktvariante auswählen können, die am Ende der ausgewählten Formel eingefügt werden soll.   | Diese Funktion ist verfügbar, wenn der ausgewählte Knoten eine ausgewählte Formel hat. Wenn diese Funktion nicht verfügbar ist, fehlt möglicherweise eine Formelversion für die ausgewählte Artikelvariante. In diesem Fall können Sie auf **Formel** &gt; **Version erstellen** klicken, um die fehlende Version für den ausgewählten Knoten zu erstellen. |
| Stücklistenpositionen &gt; Nach Position hinzufügen       | Öffnet ein Dialogfeld, in dem Sie eine Produktvariante auswählen können, die nach der ausgewählten Formelposition eingefügt werden soll.      | Diese Funktion ist verfügbar, wenn ein Formelpositionsknoten aktiviert ist. |
| Formel &gt; Version erstellen         | Erstellen einer neuen Formelversion oder einer Formel für die Produktvariante des ausgewählten Knotens.                     | Diese Funktion ist nur verfügbar, wenn der Formelpositionsknoten, der ausgewählt ist, in einen Artikel verknüpft ist, dessen Produktionstyp **Stückliste** oder **Formel** ist. |
| Formel &gt; Berechnung            | Öffnet ein Dialogfeld, in dem Sie die Kosten- oder Verkaufspreisberechnung für die ausgewählte Produktvariante ausführen können. | Diese Funktion ist verfügbar, wenn der ausgewählte Knoten sich auf eine Formelversion bezieht. |
| Formel &gt; Überprüfen                  | Validieren und überprüfen Sie die ausgewählte Formel.                                                                  | Diese Funktion ist verfügbar, wenn der ausgewählte Knoten sich auf eine Formelversion bezieht. |

## <a name="configuring-the-tree-view"></a>Konfigurieren der Strukturansicht
Klicken Sie auf **Einstellungen**, um die Informationen anzupassen, die in der Formelansicht des Stücklisten-Designers angezeigt werden.


| Feldgruppe |                                                                          Beschreibung                                                                          |
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
|     Stückliste     | Verwenden Sie die Kontrollkästchen, um die Kriterien auszuwählen, die in der Strukturansicht angezeigt werden sollen. Im Formeldesigner werden die ausgewählten Kriterien am unteren Rand der beiden Registerkarten angezeigt. |
|    Arbeitsplan    |                                           Verwenden Sie die Kontrollkästchen, um die Kriterien auszuwählen, die für die Arbeitspläne angezeigt werden sollen.                                           |

