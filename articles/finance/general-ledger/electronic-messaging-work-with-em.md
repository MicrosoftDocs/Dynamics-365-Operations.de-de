---
title: Mit Funktionen der elektronischen Nachrichten arbeiten
description: In diesem Artikel erfahren Sie, wie Sie mit der Funktionalität für elektronische Nachrichten (EN) arbeiten.
author: AdamTrukawka
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 929d3d3aad249007264204a3fd51377c8bb42377
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279271"
---
# <a name="work-with-the-electronic-messages-functionality"></a>Arbeit mit Funktionen der elektronischen Nachrichten

[!include [banner](../includes/banner.md)]

Wenn Sie auf der Nachrichtenebene arbeiten, ist die Seite **Elektronische Nachrichten** (**Steuer** \> **Abfragen und Berichte** \> **Elektronische Nachrichten** \> **Elektronische Nachrichten**) nützlicher. Wenn Sie auf der Datensammlungs- oder Nachrichtenelementebene arbeiten, ist die Seite **Elektronische Nachrichtenelemente** (**Steuer** \> **Abfragen und Berichte** \> **Elektronische Nachrichten** \> **Elektronische Nachrichtenelemente**) nützlicher.

## <a name="electronic-messages"></a>Elektronische Nachrichten

Die Seite **Elektronische Nachrichten** zeigt die Verarbeitung an, die für Sie verfügbar ist, basierend auf Ihrer Rolle. Sicherheitsrollen werden mit der Verarbeitung in den Einstellungen dieser Verarbeitung zugeordnet. Für jede Verarbeitung, die für Sie verfügbar ist, zeigt die Seite elektronische Nachrichten sowie Informationen an, die ihnen zugeordnet ist.

Das Inforegister **Nachrichten** zeigt elektronische Nachrichten für die ausgewählte Verarbeitung an. Abhängig vom Status der ausgewählten Nachricht und der vordefinierten Verarbeitung, können Sie einige Aktivitäten ausführen, indem Sie die Schaltflächen über dem Raster verwenden:

- **Neu** – Diese Schaltfläche ist Aktivitäten vom Typ **Nachricht erstellen** zugeordnet.
- **Löschen** – Diese Schaltfläche ist verfügbar, wenn das Kontrollkästchen **Löschen ermöglichen** für den aktuellen Status der ausgewählten Nachricht aktiviert ist.
- **Daten erfassen** – Diese Schaltfläche wird Aktivitäten des Typs **Datensätze auffüllen** zugeordnet.
- **Bericht generieren** – Diese Schaltfläche ist Aktivitäten vom Typ **Elektronische Berichterstellungsexportnachricht** zugeordnet.
- **Bericht senden** – Diese Schaltfläche ist Aktivitäten vom Typ **Webdienst** zugeordnet.
- **Antwort importieren** – Diese Schaltfläche ist Aktivitäten vom Typ **Elektronischer Berichterstellungsimport** zugeordnet.
- **Status aktualisieren** – Diese Schaltfläche ist Aktivitäten vom Typ **Nachrichtenebenen-Benutzerverarbeitung** zugeordnet.
- **Nachrichtenelemente** – Öffnet die Seite **Elektronische Nachrichtenelemente**.

Das Inforegister **Aktivitätsprotokoll** zeigt Informationen zu allen Aktivitäten an, die für die ausgewählte Nachricht ausgeführt wurden. Wenn eine Aktivität zu einem Fehler geführt hat, werden Informationen zu dem Fehler an die entsprechende Position im Raster angefügt. Um die Informationen über den Fehler zu überprüfen, wählen Sie die Position im Raster aus, und wählen Sie dann die Schaltfläche **Anhang** (Büroklammersymbol) in der oberen rechten Ecke auf der Seite aus.

Das Inforegister **Zusätzliche Felder der Nachricht** zeigt alle zusätzlichen Felder an, die für Nachrichten in den Verarbeitungseinstellungen definiert sind. Das Inforegister enthält die Werte dieser zusätzlichen Felder an.

Das Inforegister **Nachrichtenelemente** zeigt alle Nachrichtenelemente an, die der ausgewählten Nachricht zugeordnet sind. Abhängig vom Status des ausgewählten Nachrichtenelements können Sie einige Aktivitäten ausführen, indem Sie die Schaltflächen über dem Raster verwenden:

- **Löschen** – Diese Schaltfläche ist verfügbar, wenn das Kontrollkästchen **Löschen ermöglichen** für den aktuellen Status des ausgewählten Nachrichtenelements aktiviert ist.
- **Status aktualisieren** – Diese Schaltfläche ist Aktivitäten vom Typ **Benutzerverarbeitung** zugeordnet.
- **Originaldokument** – Öffnen Sie eine Seite, die das Originaldokument für das ausgewählte Nachrichtenelement anzeigt.

Die Berichte, die für eine Nachricht bereits generiert und empfangen wurden, werden an diese Nachricht angehängt. Um die Anhänge zu überprüfen, die mit eine Nachricht verknüpft sind, wählen Sie die Nachricht aus, und wählen Sie dann die Schaltfläche **Anhang** (das Büroklammersymbol) in der oberen rechten Ecke der Seite aus.

![Schaltfläche „Anhang”](media/attachment-icon.png)

Die Seite **Anhänge** zeigt die Anhänge an, die dieser ausgewählten Nachricht zugeordnet sind. Um eine Datei anzuzeigen, wählen Sie diese in der Liste auf der linken Seite und dann im Aktivitätsbereich **Öffnen** aus.

![Schaltfläche „Öffnen”](media/open-button.png)

Sie können Anhänge überprüfen, die einer bestimmten Aktivität zugeordnet sind, die zuvor für eine Nachricht ausgeführt wurde. Wählen Sie auf der Seite **Elektronische Nachrichten** im Inforegister **Nachrichten** die Nachricht aus. Wählen Sie auf dem Inforegister **Aktivitätsprotokoll** die Aktivität und dann die Schaltfläche **Anhang** (Büroklammersymbol) in der oberen rechten Ecke der Seite aus.

Sie können die gesamte Verarbeitung oder nur eine bestimmte Aktivität ausführen, indem Sie **Verarbeitung ausführen** auswählen.

## <a name="electronic-message-items"></a>Elektronische Nachrichtenelemente

Die Seite **Elektronische Nachrichtenelemente** zeigt alle Nachrichtenelemente und ein Protokoll der Aktivitäten an, die für jedes Nachrichtenelement ausgeführt wurden. Die Seite zeigt auch die zusätzlichen Felder, die für die Nachrichtenelemente definiert sind sowie die Werte dieser zusätzlichen Felder.

In der folgenden Tabelle werden die Felder auf der Registerkarte **Nachrichtenelemente** beschrieben.

<table>
<thead>
<tr>
<th>Feld</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr>
<td>Bearbeitung</td>
<td>Der Name der Verarbeitung, die zum Erstellen des Nachrichtenelements verwendet wurde.</td>
</tr>
<tr>
<td>Nachrichtenelement</td>
<td>Die Kennung des Nachrichtenelements. Diese Kennung wird automatisch zugewiesen, basierend auf dem Nummernkreis <b>Nachrichtenelement</b>, der auf der Seite <b>Hauptbuchparameter</b> definiert ist.</td>
</tr>
<tr>
<td>Nachrichtenelementdatum</td>
<td>Das Datum, an dem das Nachrichtenelement erstellt wurde.</td>
</tr>
<tr>
<td>Nachrichtenelementtyp</td>
<td>Der Typ des Nachrichtenelements. Mehrere Typen von Nachrichtenelementen können für dieselbe Verarbeitung eingerichtet werden (beispielsweise <b>Eingehende Rechnungen</b> und <b>Ausgehende Rechnungen</b>). Dieses Feld kann nur automatisch festgelegt werden, wenn eine Rechnung der Tabelle „Nachrichtenelemente“ hinzugefügt wurde.</td>
</tr>
<tr>
<td>Nachrichtenelementstatus</td>
<td><p>Der tatsächliche Status des Nachrichtenelements. Die verfügbaren Status variieren, abhängig vom Typ des Nachrichtenelements. Nachfolgend finden Sie einige Beispiele:</p>
<ul>
<li><b>Aufgefüllt</b> – Ein Datensatz wurde der Tabelle „Nachrichtenelemente” hinzugefügt.</li>
<li><b>Ausgewertet</b> – Zusätzliche Attribute wurden für das Nachrichtenelement berechnet.</li>
<li><b>Berichtet</b> – Das Nachrichtenelement wurde erfolgreich zu einem Bericht hinzugefügt.</li>
<li><b>Ausgeschlossen</b> – Dieser Status ist nützlich, wenn einige Nachrichtenelemente aus einem Bericht ausgeschlossen werden, bevor er exportiert wird.</li>
</ul>
</td>
</tr>
<tr>
<td>Übermittlungsdatum</td>
<td>Zur Verarbeitung, die automatisch einen generierten Bericht außerhalb des Systems übermittelt, das Datum, an dem das Nachrichtenelement übermittelt wurde.</td>
</tr>
<tr>
<td>Dokumentnummer</td>
<td>Dieses Feld wird basierend auf den Einstellungen der Aktivität zum Auffüllen von Datensätzen automatisch festgelegt. Dieses Feld kann nur automatisch festgelegt werden, wenn eine Rechnung der Tabelle „Nachrichtenelemente“ hinzugefügt wurde.</td>
</tr>
<tr>
<td>Kontonummer</td>
<td>Die Kontonummer eines Kunden oder Lieferanten oder ein anderer Feldwert, abhängig vom Feld, das bei der Aktivität zum Auffüllen von Datensätzen definiert ist. Dieses Feld kann nur automatisch festgelegt werden, wenn eine Rechnung der Tabelle „Nachrichtenelemente“ hinzugefügt wurde.</td>
</tr>
<tr>
<td>Meldung</td>
<td>Die Nummer der Nachricht. Diese Zahl wird automatisch zugewiesen, basierend auf dem Nummernkreis <b>Nachricht</b>, der auf der Seite <b>Hauptbuchparameter</b> definiert ist.</td>
</tr>
<tr>
<td>Nachrichtenstatus</td>
<td>Der tatsächliche Status der elektronischen Nachricht.</td>
</tr>
<tr>
<td>Nächste Aktivität</td>
<td>Die nächsten Aktivitäten, die für den aktuellen Status des Nachrichtenelements gestartet werden können.</td>
</tr>
</tbody>
</table>

Die Registerkarte **Zusätzliche Felder** zeigt die zusätzlichen Felder für das ausgewählte Nachrichtenelement und deren Werte an.

### <a name="run-processing"></a>Verarbeitung ausführen

Wählen Sie im Aktivitätsbereich **Verarbeitung ausführen** aus, um die Verarbeitung für Nachrichtenelemente auszuführen. Um eine bestimmte Aktivität im Dialogfeld **Verarbeitung ausführen** auszuführen, legen Sie die Option **Aktivität wählen** auf **Ja** fest, und wählen Sie dann eine Aktivität aus. Um die gesamte Verarbeitung auszuführen, belassen Sie die Option **Aktivität wählen** auf **Nein** festgelegt.

### <a name="generate-report"></a>Bericht generieren

Wählen Sie im Aktivitätsbereich **Bericht generieren** aus. Diese Schaltfläche ist Aktivitäten vom Typ **Elektronischer Berichterstellungsexport** zugeordnet.

### <a name="update-status"></a>Status aktualisieren

Wählen Sie im Aktivitätsbereich **Status aktualisieren** aus, um den Status einer oder mehrerer Nachrichtenelemente zu aktualisieren. Im Dialogfeld **Status aktualisieren** verwenden Sie das Inforegister **Einzuschließende Datensätze**, um die Nachrichtenelemente für die Aktualisierung auszuwählen. Stellen Sie sicher, dass Sie die Auswahlkriterien richtig definieren, da Nachrichtenelementstatus gemäß dieser Kriterien, dem Anfangsstatus der ausgewählten Aktivität und dem Wert, den Sie im Feld **Neuer Status** angeben, aktualisiert werden. Nachdem eine Statusaktualisierung abgeschlossen ist, wird es schwierig zu bestimmen, welche Elemente aktualisiert wurden. Daher wird es schwierig sein, ein Rollback für das Statusupdate auszuführen.

### <a name="electronic-messages"></a>Elektronische Nachrichten

Wählen Sie im Aktivitätsbereich die Option **Elektronische Nachrichten** aus, um eine elektronische Nachricht zu überprüfen, die dem ausgewählten Nachrichtenelement zugeordnet ist.

Sie können auch die Dateien überprüfen, die einem bestimmten Nachrichtenelement zugeordnet sind. Wählen Sie das Feld **Nachricht** für das Nachrichtenelement aus, oder wählen Sie im Aktivitätsbereich **Elektronische Nachrichten** aus. Wählen Sie dann auf der Seite **Elektronische Nachricht** die Nachricht aus, nach der Sie Dateien überprüfen möchten, und wählen Sie dann die Schaltfläche **Anhang** (Büroklammersymbol) in der oberen rechten Ecke der Seite aus.

Die Seite **Anhänge** zeigt die Anhänge an, die dieser Nachricht zugeordnet sind. Um eine Datei anzuzeigen, wählen Sie diese in der Liste auf der linken Seite aus, und wählen Sie anschließend **Öffnen** im Aktionsbereich aus.

### <a name="original-document"></a>Originaldokument

Wählen Sie im Aktivitätsbereich **Originaldokument** aus, um das Originaldokument für das ausgewählte Nachrichtenelement zu öffnen.
