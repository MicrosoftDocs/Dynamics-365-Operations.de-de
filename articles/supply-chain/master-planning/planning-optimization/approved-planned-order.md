---
title: Geplante Aufträge anzeigen, verwalten und genehmigen
description: In diesem Thema finden Sie Informationen zum Anzeigen, Verwalten und Genehmigen von geplanten Aufträgen in der Planungsoptimierung.
author: ChristianRytt
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-08-21
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 3b9b5274481e693f9fa05eb084ec5505ce5bc2eb
ms.sourcegitcommit: 9283caad2d0636f98579c995784abec19fda2e3f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "5935656"
---
# <a name="view-manage-and-approve-planned-orders"></a>Geplante Aufträge anzeigen, verwalten und genehmigen

[!include [banner](../../includes/banner.md)]

In diesem Thema finden Sie Informationen zum Anzeigen, Verwalten und Genehmigen von geplanten Aufträgen in der Planungsoptimierung.

## <a name="view-and-manage-planned-orders"></a><a name="view-planned-orders"></a>Geplante Aufträge anzeigen und verwalten

Sie können geplante Aufträge auf jeder Listenseite für geplante Aufträge anzeigen und verwalten. Gehen Sie zu einer der folgenden Stellen, je nach Art der geplanten Aufträge, mit denen Sie arbeiten wollen:

- Produktprogrammplanung \> Arbeitsbereiche \> Gesamtplanung
- Produktprogrammplanung \> Produktprogrammplanung \> Geplante Aufträge
- Produktion Steuerelement \> Produktionsaufträge \> Geplante Produktionsaufträge
- Beschaffung und Sourcing \> Bestellungen \> Geplante Aufträge
- Lagerbestand verwalten \> Eingehende Aufträge \> Geplante Umlagerungen
- Bestandsverwaltung \> Ausgehende Aufträge \> Geplante Umlagerungen

## <a name="view-and-edit-the-status-of-planned-orders"></a>Anzeigen und Bearbeiten des Status geplanter Aufträge

Sie können das Feld **Status** jedes geplanten Auftrags verwenden, um Ihren Fortschritt zu verfolgen oder zu ändern, wie ein geplanter Auftrag verarbeitet wird. Die folgenden **Status**-Werte sind verfügbar:

- **Unbearbeitet** – Wenn die Produktprogrammplanung geplanter Aufträge erzeugt, erhalten diese diesen Status. Geplante Aufträge, die diesen Status haben, werden beim nächsten Planungslauf gelöscht.
- **Erledigt** – Dieser Status zeigt an, dass der geplante Auftrag abgeschlossen ist. Wenn Sie sich entscheiden, einen geplanten Auftrag nicht zu sperren, können Sie seinen Status manuell auf *Erledigt* ändern. Beachten Sie, dass das System die Zustände *Unbearbeitet* und *Erledigt* gleich behandelt.
- **Genehmigt** – Dieser Status zeigt an, dass der geplante Auftrag zur Umwandlung genehmigt ist. Wenn Sie einen geplanten Auftrag fixieren wollen, können Sie seinen Status auf *Genehmigt* ändern. Wenn Sie die Änderungen, die an einem geplanten Auftrag vorgenommen wurden, beibehalten wollen oder wenn Sie planen, einen geplanten Auftrag zu fixieren, ändern Sie seinen Status auf *Genehmigt*. Geplante Aufträge, die den Status *Freigegeben* haben, werden von der Produktprogrammplanung als fixiert und erwartete Lieferung betrachtet. Daher werden sie bei späteren Ausführungen der Produktprogrammplanung nicht geändert oder gelöscht. Um dieses Verhalten zu erreichen, kopiert die Planungslogik während der Produktprogrammplanung geplanter Aufträge, die den Status *Genehmigt* haben, von der alten Planversion in die neue Planversion. Beachten Sie, dass geplanter Auftrag, der den Status *Bewilligt* hat, nur innerhalb des spezifischen Masterplans als Lieferung gilt.

Um den Status eines einzelnen geplanten Auftrags zu ändern, [öffnen Sie eine beliebige Listenseite für geplante Aufträge](#view-planned-orders), öffnen Sie den Auftrag und führen Sie dann einen der folgenden Schritte aus:

- Ändern Sie auf dem Inforegister **Allgemein** den Wert des Feldes **Status**.
- Im Aktivitätsbereich, auf der Registerkarte **Geplanter Auftrag**, in der Gruppe **Verarbeiten**, wählen Sie **Status ändern**.
- Wählen Sie im Aktivitätsbereich **Genehmigen**, um den Auftrag als genehmigt zu markieren.

Um den Status mehrerer geplanter Aufträge gleichzeitig zu ändern, [öffnen Sie eine beliebige Listenseite für geplante Aufträge](#view-planned-orders), aktivieren Sie das Kontrollkästchen für jeden Auftrag, den Sie ändern möchten, und folgen Sie dann einem der folgenden Schritte:

- Im Aktivitätsbereich, auf der Registerkarte **Geplanter Auftrag**, in der Gruppe **Verarbeiten**, wählen Sie **Status ändern**.
- Wählen Sie im Aktivitätsbereich **Freigeben**, um die Aufträge als genehmigt zu markieren.

## <a name="approve-planned-orders"></a>Auftragsvorschläge genehmigen

Die Genehmigung geplanter Aufträge ist ein optionaler Schritt im Prozess der Erstellung eines umgewandelten Auftrags aus einem geplanten Auftrag.

Die folgende Abbildung zeigt, wie Sie den Wert **Status**, der jedem geplanten Auftrag zugeordnet ist, zur Implementierung eines Genehmigungs-Workflows verwenden können. Um einen Genehmigungsprozess zu implementieren, passen Sie den **Status**-Wert für jeden geplanten Auftrag manuell an, wie im vorherigen Abschnitt beschrieben.

![Flow des Bestellvorschlags](media/approved-planned-orders-1.png)

> [!TIP]
> Wir empfehlen, dass Sie alle geänderten geplanten Aufträge genehmigen. Andernfalls werden die Bearbeitungen ignoriert und beim nächsten Planungslauf überschrieben.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Fest geplante Aufträge](planned-order-firming.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
