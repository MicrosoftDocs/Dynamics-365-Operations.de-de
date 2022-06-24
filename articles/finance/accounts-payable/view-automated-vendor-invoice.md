---
title: Ergebnisse der Automatisierung von Lieferantenrechnungen anzeigen (Vorschau)
description: In diesem Artikel wird erläutert, wie Sie den Status von Lieferantenrechnungen anzeigen, die sich im automatisierten Submit-to-Workflow-Prozess befinden.
author: abruer
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: dd9b74d2ed34399aff455563504c296a5a25a874
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895166"
---
# <a name="view-vendor-invoice-automation-results"></a>Ergebnisse der Automatisierung von Kreditorenrechnungen anzeigen

[!include [banner](../includes/banner.md)]

In diesem Artikel wird erläutert, wie Sie den Status von Lieferantenrechnungen anzeigen, die sich im automatisierten Submit-to-Workflow-Prozess befinden. Details zum Automatisierungsverlauf werden für jede importierte Lieferantenrechnung gepflegt. Abhängig von den Geschäftsprozessen, die Sie automatisiert haben, zeigt die Seite **Ausstehende Lieferantenrechnungen** die Werte **Status der automatisierten Belegübereinstimmung** und **Automatische Übermittlung an den Workflow-Status**. Sie können die Details anzeigen und einen Plan erstellen, um sich auf die Rechnungen zu konzentrieren, bei denen ein automatisierter Schritt fehlgeschlagen ist. Nachdem Sie das Problem behoben haben, können Sie den automatisierten Prozess für die importierte Rechnung fortsetzen.

Bevor Sie eine übermittelte Rechnung bearbeiten können, müssen Sie die automatische Verarbeitung anhalten. Wenn eine Rechnung im automatisierten Submit-to-Workflow-Prozess angehalten werden muss, setzen Sie das Feld **In die automatisierte Verarbeitung einbeziehen** auf der Seite **Lieferantenrechnungen** auf **Nein**. Die Automatisierung wird erst dann ausgeführt, wenn **In die automatisierte Verarbeitung einbeziehen** auf **Ja** gesetzt ist. Eine Rechnung kann von der weiteren Automatisierung angehalten werden, wenn sie sich noch nicht im Workflow-System befindet und nicht vom automatisierten Prozess verwendet wird.

Wenn eine importierte Rechnung dem Workflow-Prozess unterworfen ist, können Sie sie ihren **Automatisierungsstatus**-Wert auf der **Lieferantenrechnungen**-Seite anzeigen. Folgende Status werden verfolgt:

- **Inbegriffen** – Die automatisierten Prozesse, die auf der Seite **Kreditorenkontenparameter** definiert sind, laufen korrekt, sind aber noch nicht abgeschlossen.
- **Pausiert** – Die automatisierten Prozesse, die auf der Seite **Kreditorenkontoparameter** definiert sind, wurden ausgeführt, aber mindestens ein Schritt in diesem Prozess ist fehlgeschlagen. Der Status **Pausiert** wird auch angewendet, wenn das Feld **In die automatisierte Verarbeitung einbeziehen** auf **Nein** gesetzt ist. Sie können die Fehler anzeigen, indem Sie die Schaltfläche **Letzte Ergebnisse anzeigen** wählen.
- **Im Workflow** – Die importierte Rechnung wurde entweder automatisch oder manuell an das Workflow-System übermittelt.
- **Workflow abgeschlossen** – Der Workflow-Prozess für die importierte Rechnung wurde abgeschlossen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
