---
title: Eine angepasste Planung autorisieren
description: Nicht alle Planungsdaten müssen sofort autorisiert werden. In diesem Artikel wird beschrieben, wie Sie die Periode angeben können, für die eine Planung autorisiert ist. Er erläutert auch, wie Sie die Planung für bestimmte Unternehmen und Planzahlenmodelle autorisieren können.
author: t-benebo
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanImportForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72734
ms.assetid: cb8fd809-605a-4a8b-a390-636edfec21f9
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4954b70e56482e419d81485b544cb5d0b4e4a3ce
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740710"
---
# <a name="authorize-an-adjusted-forecast"></a>Eine angepasste Planung autorisieren

[!include [banner](../includes/banner.md)]

Nicht alle Planungsdaten müssen sofort autorisiert werden. In diesem Artikel wird beschrieben, wie Sie die Periode angeben können, für die eine Planung autorisiert ist. Er erläutert auch, wie Sie die Planung für bestimmte Unternehmen und Planzahlenmodelle autorisieren können.

Nicht alle Planungsdaten müssen sofort autorisiert werden. Sie können das Start- und Enddatum der Periode angeben, für die die Planung autorisiert ist. Diese Funktion lässt Sie bestimmte Zeitrahmen einfrieren. 

Das Start- und Enddatum, das Sie angeben, muss dem Start- und Enddatum der Liste entsprechen, in der die Planung generiert wird. Das System setzt diese Einschränkung durch und reguliert automatisch die Daten, wenn eine Regulierung erforderlich ist. 

Auf der Registerkarte **Details** der Seite **Autorisierung** können Sie Details zur Planung anzeigen, die zuletzt generiert wurde. 

Sie können die Unternehmen und die Planzahlenmodelle auswählen, um die Planung für die Verwendung zu autorisieren. Standardmäßig umfasst das Raster alle Unternehmen, für die der Planungsbedarf erstellt wurde. Für jedes Unternehmen wird das Planzahlenmodell, das dem aktuellen Absatzplan entspricht, der in den Produktprogrammplanungsparametern eingerichtet ist, vorab ausgefüllt. Sie können dieses Planzahlenmodell jedoch in ein beliebiges anderes Planzahlenmodell ändern, das zu diesem Unternehmen gehört. Wenn keine Bedarfsplanungsdaten für ein ausgewähltes Unternehmen generiert wurden, wird beim Import eine Warnmeldung angezeigt. 

Es ist außerordentlich wichtig, dass Sie verstehen, wie das Kontrollkästchen **Manuelle Anpassungen der Grundbedarfsplanung speichern** funktioniert. Wenn Sie die manuelle Anpassungen an der statistischen Grundplanung vorgenommen haben, werden die angepassten Werte autorisiert, auch wenn dieses Kontrollkästchen deaktiviert ist. Allerdings werden die Änderungen nach der Autorisierung verworfen. Daher ist beim nächsten Generieren einer Planung diese Planung nur eine statistische Planung und hat keine Korrekturmöglichkeiten, auch wenn **Manuelle Anpassungen auf Bedarfsplanung übertragen** aktiviert ist. Daher können Sie das Kontrollkästchen **Manuelle Anpassungen der Grundbedarfsplanung speichern** als einen Mechanismus ansehen, mit dem Sie alle manuellen Änderungen beibehalten oder verwerfen können.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Manuelle Anpassungen an der Grundplanung](manual-adjustments-baseline-forecast.md)
- [Planungsgenauigkeit überwachen](monitor-forecast-accuracy.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]