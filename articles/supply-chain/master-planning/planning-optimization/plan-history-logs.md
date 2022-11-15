---
title: Planhistorie und Planungsprotokolle einsehen
description: In diesem Artikel wird erläutert, wie Sie den Verlauf von Planungsaufträgen anzeigen.
author: t-benebo
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MPSPlanRegenerationJobList, MPSPlanRegenerationJobLogs
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: ab469686a009364bf53cb963506fd2107075a283
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740930"
---
# <a name="view-plan-history-and-planning-logs"></a>Planhistorie und Planungsprotokolle einsehen

[!include [banner](../../includes/banner.md)]

In diesem Artikel wird erläutert, wie Sie den Verlauf von Planungsaufträgen in Microsoft Dynamics 365 Supply Chain Management anzeigen.

Um die Historie für einen Plan anzuzeigen, öffnen Sie den Plan, indem Sie zu **Masterplanung** \> **Einrichtung** \> **Pläne** \> **Masterpläne** gehen und **Historie** auswählen. Die Historie listet alle Aufträge für den ausgewählten Plan auf. Die Liste enthält erledigte und aktive Aufträge.

Das System speichert maximal 60 Verlaufsdatensätze pro Masterplan und löscht Datensätze, die älter als 30 Tage sind. Jedes Mal, wenn Sie eine neue Hauptplanungsberechnung ausführen, fügt das System einen neuen Verlaufsdatensatz hinzu und bereinigt dann die ältesten Datensätze nach Bedarf.

Sie können nicht nur die Startzeit und den Status der Jobs einsehen, sondern auch das Protokoll für einen bestimmten Job anzeigen. Das Protokoll enthält zusätzliche Informationen und Warnungen. Nicht alle Aufträge haben ein Protokoll. Um das Protokoll für einen Auftrag anzuzeigen, wählen Sie **Protokoll**. Log-Einträge werden nur 30 Tage nach Auftragsende gespeichert und danach automatisch gelöscht.

Wenn die **tapelverarbeitung** Option im Inforegister **Im Hintergrund laufen** beim Einrichten der Hauptplanungsverarbeitung aktiviert wurde, zeigt das Batch-Job-Protokoll weitere Informationen zu Warnungen und Fehlern, die während des Hauptplanungslaufs generiert wurden. Beispielsweise werden Fehler bei der automatischen Fixierung nur im Batch-Jobprotokoll erfasst. Sie werden nicht in Protokollen auf der **Verlauf** Seite angezeigt.

Führen Sie die folgenden Schritte aus, um Fehler bei der automatischen Fixierung und andere Warnungen oder Fehler anzuzeigen, die während eines Hauptplanungslaufs aufgetreten sind.

1. Gehen Sie zu **Systemverwaltung \> Anfragen \> Batch-Jobs**.
1. Suchen Sie den Datensatz, der den Masterplanungslauf darstellt, an dem Sie interessiert sind, und wählen Sie ihn aus. (Zum Beispiel der Wert vom **Arbeitsbeschreibung** Feld könnte beginnen mit *Masterplanung* .)
1. Befolgen Sie einen dieser Schritte, je nachdem, ob Sie das *erweiterte Form* oder das *altes (unerweiterte) Formular* für die **Batch-Jobs** Seite verwenden:

    - Wenn Sie das erweiterte Formular verwenden: Wählen Sie im Aktivitätsbereich **Batch-Jobverlauf**. Dann auf der **Batch-Jobverlauf** Seite, wählen Sie im Aktivitätsbereich **Protokoll**.
    - Wenn Sie das alte Formular verwenden: Wählen Sie im Aktivitätsbereich **Batch-Job** **Protokoll** aus.

1. **Nachrichtendetails** auswählen, um den **Nachrichtendetails** Bereich zu öffnen, in dem Sie alle Warnungen und Fehler anzeigen können, die während der Verarbeitung erfasst wurden.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
