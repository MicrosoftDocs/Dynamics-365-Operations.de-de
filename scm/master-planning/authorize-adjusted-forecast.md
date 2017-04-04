---
title: Autorisieren Sie einer regulierten Planung
description: "Nicht alle Planungsdaten müssen sofort autorisiert werden. In diesem Artikel wird beschrieben, wie Sie die Periode angeben können, für die eine Planung autorisiert ist. Er erläutert auch, wie Sie die Planung für bestimmte Unternehmen und Planzahlenmodelle autorisieren können."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqDemPlanImportForecastDialog
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72734
ms.assetid: cb8fd809-605a-4a8b-a390-636edfec21f9
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: f151f4b4290df0b2bf1b5d1159654bd248a439b1
ms.lasthandoff: 03/31/2017


---

# <a name="authorize-an-adjusted-forecast"></a>Autorisieren Sie einer regulierten Planung

Nicht alle Planungsdaten müssen sofort autorisiert werden. In diesem Artikel wird beschrieben, wie Sie die Periode angeben können, für die eine Planung autorisiert ist. Er erläutert auch, wie Sie die Planung für bestimmte Unternehmen und Planzahlenmodelle autorisieren können.

Nicht alle Planungsdaten müssen sofort autorisiert werden. Sie können das Start- und Enddatum der Periode angeben, für die die Planung autorisiert ist. Diese Funktion lässt Sie bestimmte Zeitrahmen einfrieren. 

Das Start- und Enddatum, den Sie angeben, muss z Start- und Enddatum des Buckets entsprechen, dass die Planung generiert wird. Das System setzt diese Einschränkung und reguliert automatisch die Daten, wenn Regulierung erforderlich ist. 

Auf der Registerkarte **Details** der Seite **Autorisierung** können Sie Details zur Planung anzeigen, die zuletzt generiert wurde. 

Sie können die Unternehmen und die Planzahlenmodelle auswählen, um die Planung für die Verwendung zu autorisieren. Standardmäßig umfasst das Raster alle Unternehmen, für die der Planungsbedarf erstellt wurde. Für jedes Unternehmen wird das Planzahlenmodell, das dem aktuellen Absatzplan entspricht, der in den Produktprogrammplanungsparametern eingerichtet ist, vorab ausgefüllt. Sie können dieses Planzahlenmodell jedoch in ein beliebiges anderes Planzahlenmodell ändern, das zu diesem Unternehmen gehört. Wenn keine Bedarfsplanungsdaten für ein ausgewähltes Unternehmen generiert wurden, wird beim Import eine Warnmeldung angezeigt. 

Es ist außerordentlich wichtig, dass Sie verstehen, wie das Kontrollkästchen **Manuelle Anpassungen der Grundbedarfsplanung speichern** funktioniert. Wenn Sie die manuelle Anpassungen der statistischen Grundplanung vorgenommen haben, werden die angepassten Werte dar laut berechtigt, auch wenn dieses Kontrollkästchen deaktiviert ist. Allerdings werden die Änderungen nach der Autorisierung verworfen. Daher ist beim nächsten Generieren einer Planung diese Planung nur eine statistische Planung und hat keine Korrekturmöglichkeiten, auch wenn **Manuelle Anpassungen auf Bedarfsplanung übertragen** aktiviert ist. Daher können Sie das Kontrollkästchen **Manuelle Anpassungen der Grundbedarfsplanung speichern** als einen Mechanismus ansehen, mit dem Sie alle manuellen Änderungen beibehalten oder verwerfen können.

<a name="see-also"></a>Siehe auch
--------

[Making manual adjustments to the baseline forecast](manual-adjustments-baseline-forecast.md)

[Monitoring forecast accuracy](monitor-forecast-accuracy.md)


