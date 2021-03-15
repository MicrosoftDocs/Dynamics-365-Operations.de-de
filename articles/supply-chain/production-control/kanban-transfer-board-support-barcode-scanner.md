---
title: Unterstützung der Kanban-Übertragungskarte für Strichcodescanner
description: Die Kanban-Umlagerungsübersicht unterstützt die Scanner-Eingabe von einem Widgetstrichcodescanner bei der Auswahl, dem Starten, dem Abschluss und dem Leeren eines Kanban-Einzelvorgangs.
author: ChristianRytt
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19391
ms.assetid: a426f645-d59b-4c98-8d78-eba8d64a562e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aedfe7ef96d62401b1d0de0f2cd035036c68e51a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007065"
---
# <a name="kanban-transfer-board-support-for-barcode-scanners"></a>Unterstützung der Kanban-Übertragungskarte für Strichcodescanner

[!include [banner](../includes/banner.md)]

Die Kanban-Umlagerungsübersicht unterstützt die Scanner-Eingabe von einem Widgetstrichcodescanner bei der Auswahl, dem Starten, dem Abschluss und dem Leeren eines Kanban-Einzelvorgangs.

<a name="registration-modes"></a>Erfassungsmodi
------------------

Auf dem Inforegister **Scanner-Erfassung** können Sie den Registrierungsmodus auswählen, der die Aktivität steuert, wenn Sie eine Kanban-Kartennummer scannen oder manuell im Nummernfeld eingeben.

| Erfassungsmodus festlegen | Beschreibung                                                                                     |
|-----------------------|-------------------------------------------------------------------------------------------------|
| Start                 | Registriert einen Kanban-Umlagerungseinzelvorgang als 'In Bearbeitung'.                                                 |
| Abgeschlossen              | Registriert einen Kanban-Umlagerungseinzelvorgang als 'Abgeschlossen'.                                                   |
| Leer                 | Registriert die Handhabungseinheit, auf die von der Kanban-Karte verwiesen wird, als leer.              |
| Auswählen                | Registriert eine Kanban-Kartennummer und wählt automatisch den Einzelvorgang in der Kanban-Einzelvorgangsliste aus. |

 
<a name="registration-mode-select"></a>Erfassungsmodusauswahl
------------------------

Wenn Sie einen Barcodeleser verwenden, um einen Einzelvorgang auszuwählen, ändert sich der Ansichtsmodus der Kanban-Übersicht. In diesem Modus gelten folgende Bedingungen:

-   Nur der gescannte Kanban-Einzelvorgang wird angezeigt.
-   Die Details des gewählten Einzelvorgangs werden auf dem Inforegister **Details** angezeigt.
-   Das Inforegister **Meldungen** zeigt nur Nachrichten für den ausgewählten Einzelvorgang an.
-   Sie können den Status des Einzelvorgangs ändern, indem Sie die Funktionen verwenden, die im Aktivitätsbereich verfügbar sind. Die Kanban-Übertragungskarte zeigt weiterhin nur einen einzelnen Einzelvorgang für diesen Zeitraum an.
-   Sie können die Informationen in der Liste der Einzelvorgänge manuell aktualisieren, indem Sie auf **Aktualisieren** (UMSCHALT+F5) im Aktivitätsbereich klicken. Nachdem Sie die Informationen aktualisiert haben, werden die vollständigen Ergebnisse für den Einzelvorgangsfilter wieder angezeigt.

## <a name="job-status-and-possible-actions"></a>Einzelvorgangsstatus und mögliche Maßnahmen
Der Status des ausgewählten Einzelvorgangs und der Status sämtlicher angeschlossenen Einzelvorgänge für Ereignis-Kanbans bestimmt, ob Sie den Einzelvorgang weiter bearbeiten können. Die folgende Tabelle enthält Informationen zu diesen Status und Aufgaben:
-   Die Status, die für Einzelvorgänge verfügbar sind, oder für die Handhabungseinheiten, auf die von den Einzelvorgängen verwiesen wird.
-   Jede Aufgabe, die Sie für den Einzelvorgang ausführen können.

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th>Einzelvorgangstyp</th>
<th>Einzelvorgangsstatus oder Status der Handhabungseinheit</th>
<th>Entnahmeliste aktualisieren</th>
<th>Start</th>
<th>Registrierung aktualisieren</th>
<th>Abgeschlossen</th>
<th>Leer</th>
<th>Ereignis-Kanbans erstellen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Umlagerung</td>
<td><ul>
<li>Nicht geplant</li>
<li>Keine angeschlossenen Einzelvorgänge oder angeschlossenen Einzelvorgänge sind "Abgeschlossen"</li>
</ul></td>
<td>Ja</td>
<td>Ja</td>
<td>Ja</td>
<td>Ja</td>
<td>Nein</td>
<td>Ja</td>
</tr>
<tr class="even">
<td>Umlagerung</td>
<td><ul>
<li>Nicht geplant</li>
<li>Der angeschlossene Einzelvorgang ist nicht "Abgeschlossen"</li>
</ul></td>
<td>Ja</td>
<td>Nein</td>
<td>Ja</td>
<td>Nein</td>
<td>Nein</td>
<td>Nein</td>
</tr>
<tr class="odd">
<td>Umlagerung</td>
<td>In Bearbeitung</td>
<td>Ja</td>
<td>Nein</td>
<td>Ja</td>
<td>Ja</td>
<td>Nein</td>
<td>Nein</td>
</tr>
<tr class="even">
<td>Umlagerung</td>
<td>Abgeschlossen</td>
<td>Nein</td>
<td>Nein</td>
<td>Nein</td>
<td>Nein</td>
<td>Ja</td>
<td>Nein</td>
</tr>
<tr class="odd">
<td>Übertragung oder Prozess</td>
<td>Leer</td>
<td>Nein</td>
<td>Nein</td>
<td>Nein</td>
<td>Nein</td>
<td>Nein</td>
<td>Nein</td>
</tr>
<tr class="even">
<td>Übertragung oder Prozess</td>
<td>Eine Kanban-Karte wurde nicht gefunden</td>
<td>Nein</td>
<td>Nein</td>
<td>Nein</td>
<td>Nein</td>
<td>Nein</td>
<td>Nein</td>
</tr>
<tr class="odd">
<td>Übertragung oder Prozess</td>
<td>Eine Kanban-Karte wurde gefunden, aber keinem Kanban zugewiesen</td>
<td>Nein</td>
<td>Nein</td>
<td>Nein</td>
<td>Nein</td>
<td>Nein</td>
<td>Nein</td>
</tr>
<tr class="even">
<td>Verarbeiten</td>
<td><ul>
<li>Nicht geplant</li>
<li>Vorbereitet</li>
<li>In Bearbeitung</li>
</ul></td>
<td>Nein</td>
<td>Nein</td>
<td>Nein</td>
<td>Nein</td>
<td>Nein</td>
<td>Nein</td>
</tr>
<tr class="odd">
<td>Verarbeiten</td>
<td>Abgeschlossen</td>
<td>Nein</td>
<td>Nein</td>
<td>Nein</td>
<td>Nein</td>
<td>Nein</td>
<td>Nein</td>
</tr>
</tbody>
</table>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]