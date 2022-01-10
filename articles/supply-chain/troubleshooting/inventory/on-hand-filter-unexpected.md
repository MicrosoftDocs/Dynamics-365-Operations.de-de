---
title: Der Filterbereich auf der Seite „Liste des verfügbaren Lagerbestands“ funktioniert nicht wie erwartet
description: Die Filter im Filterbereich auf der Seite „Lagerbestand“ filtern die Ergebnisse nicht so, wie Sie es erwarten.
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
ms.openlocfilehash: 2b2b233e22378c8710a63dce83d168bfd89eba7f
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920497"
---
# <a name="the-filter-pane-on-the-on-hand-list-page-doesnt-work-as-expected"></a>Der Filterbereich auf der Seite „Liste des verfügbaren Lagerbestands“ funktioniert nicht wie erwartet

## <a name="symptoms"></a>Symptome

Die Filter im Filterbereich auf der Seite **Lagerbestand** filtern die Ergebnisse nicht so, wie Sie es erwarten.

## <a name="resolution"></a>Lösung

Die Seite **Bestandsliste** wird aus einer detaillierten Bestandstabelle zusammengestellt, die alle verfügbaren Dimensionen enthält. Die Liste auf dieser Seite ist jedoch eine Zusammenfassung. Daher können Zeilen aus der Quelltabelle kombiniert werden, indem Werte gemäß den angezeigten Dimensionen aggregiert werden.

Filter, die im Filterbereich festgelegt werden, gelten für die Quelltabelle, nicht für die aggregierte Liste. Dieses Verhalten kann manchmal zu unerwarteten Ergebnissen führen, wie in [diesen Beispielen](/dynamics365/supply-chain/inventory/inventory-on-hand-list.md#examples) zu sehen ist.

Die [Filter, die im Raster bereitgestellt werden,](/dynamics365/supply-chain/inventory/inventory-on-hand-list.md#grid-filters) *gelten jedoch* für die aggregierte Liste. Diese Filter enthalten sowohl QuickFilter am oberen Rand des Rasters als auch den Filter für jede Spaltenüberschrift.
