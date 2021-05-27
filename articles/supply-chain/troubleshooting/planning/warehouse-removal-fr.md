---
title: Sie können die Lagerort-Bedarfsplanungsdimension nicht aus den Planungspositionen entfernen
description: Sie können die Lagerort-Bedarfsplanungsdimension nicht aus den Planungspositionen entfernen.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6b643c4fe51ae6ce73b34ab81d4e458dcd5032df
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026544"
---
# <a name="you-cant-remove-the-warehouse-demand-forecast-dimension-from-forecast-lines"></a>Sie können die Lagerort-Bedarfsplanungsdimension nicht aus den Planungspositionen entfernen

KB-Nummer: 4614408

## <a name="symptoms"></a>Symptome

Dieses Problem tritt auf, wenn die Dimension **Lagerort** nicht auf der Registerkarte **Planungsdimensionen** der Seite **Bedarfsplanungsparameter** zugewiesen ist. Trotzdem ist die Spalte **Lagerplatz** auf der Seite **Bedarfsplanung** angezeigt (**Produktprogrammplanung \> Prognose \> Manuelle Planungseinheit \> Bedarfsplanungspositionen**).

## <a name="resolution"></a>Lösung

Die Einstellungen auf der Registerkarte **Planungsdimensionen** der Seite **Bedarfsplanungsparameter** beeinflussen die Seite **Bedarfsplanung** nicht. Sie steuern die Grundplanung, die generiert und in der angepassten Bedarfsplanung angezeigt wird. Sie steuern jedoch nicht die Dimensionen, die für die „echte“ Bedarfsplanung erforderlich sind. Durch die Autorisierung der Datensätze, die auf der Seite **Angepasste Bedarfsplanung** angezeigt werden, können Sie sie in „echte“ Planungseinträge für ein Planungsmodell konvertieren. Dieses Modell kann dann für die Produktprogrammplanung verwendet werden.

Auf der Seite **Bedarfsplanung** sind die Dimensionen für die „echte“ Planung, die in den Bedarfsplanungspositionen angezeigt werden, Teil der Bedarfsdimensionen. (Dieses Verhalten ähnelt dem Verhalten für Auftragspositionen.) Wenn Ihr System nicht für die Verwendung des **Lagerorts** als obligatorische Bedarfsdimension eingerichtet ist, können Sie die Seite so anpassen, dass die Spalte ausgeblendet wird.
