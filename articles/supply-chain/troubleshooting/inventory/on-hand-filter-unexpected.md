---
title: Der Filterbereich auf der Seite „Liste des verfügbaren Lagerbestands“ funktioniert nicht wie erwartet
description: Die Filter im Filterbereich auf der Seite „Bestandsliste“ filtert die Ergebnisse nicht wie erwartet.
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: df11b1c1e7de36fa0458cd931d4be7f84a15d143
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476473"
---
# <a name="the-filter-pane-on-the-on-hand-list-page-doesnt-work-as-expected"></a>Der Filterbereich auf der Seite „Liste des verfügbaren Lagerbestands“ funktioniert nicht wie erwartet

## <a name="symptoms"></a>Symptome

Die Filter im Filterbereich auf der Seite **Bestandsliste**  filtert die Ergebnisse nicht wie erwartet.

## <a name="resolution"></a>Lösung

Die Seite  **Bestandsliste**  wird aus einer detaillierten Bestandstabelle zusammengestellt, die alle verfügbaren Dimensionen enthält. Die Liste auf dieser Seite ist jedoch eine Zusammenfassung. Daher können Zeilen aus der Quelltabelle kombiniert werden, indem Werte gemäß den angezeigten Dimensionen aggregiert werden.

Filter, die im Filterereich eingerichet werden, gelten für die Quelltabelle und nicht für die aggregierte Liste. Dieses Verhalten kann manchmal zu unerwarteten Ergebnissen führen, wie in [diesen Beispielen](/dynamics365/supply-chain/inventory/inventory-on-hand-list.md#examples) zu sehen ist.

Die  [Filter, die im Raster bereitgestellt werden](/dynamics365/supply-chain/inventory/inventory-on-hand-list.md#grid-filters) *, gelten*  jedoch für die aggregierte Liste. Diese Filter enthalten sowohl QuickFilter am oberen Rand des Rasters als auch den Filter für jede Spaltenüberschrift.
