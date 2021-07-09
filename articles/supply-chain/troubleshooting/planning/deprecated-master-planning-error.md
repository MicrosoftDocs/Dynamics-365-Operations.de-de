---
title: Sie erhalten einen Fehler, wenn Sie die integrierte Produktprogrammplanung ausführen
description: Wenn Sie die außer Betrieb genommene integrierte Masterplanungs-Engine ausführen, erhalten Sie eine Fehlermeldung.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: Dialog_ReqCalcScheduleItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 9c950292a4f43319d21a7deafdfb341b7bef15d8
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294084"
---
# <a name="you-receive-an-error-when-running-the-built-in-master-planning-engine"></a>Sie erhalten einen Fehler, wenn Sie die integrierte Produktprogrammplanung ausführen

Fehlercode: ReqCalcScheduleItemTablePlanningOptimizationFitError

## <a name="symptoms"></a>Symptome

Wenn Sie die Produktprogrammplanung mit der veralteten, integrierten Masterplan-Engine ausführen, erhalten Sie die folgende Fehlermeldung:

> Sie erhalten diese Fehlermeldung, weil die eingebaute Produktprogrammplanung für Szenarien verwendet wurde, die von der Planungsoptimierung unterstützt werden. Sie sollten jetzt zur Planungsoptimierung migrieren, da die derzeitige eingebaute Produktprogrammplanung außer Betrieb genommen wird. Beachten Sie, dass dieser Lauf der Produktprogrammplanung erfolgreich abgeschlossen wurde. Falls Ihre Migration starke Abhängigkeiten von anstehenden Funktionen hat, kann eine Ausnahme zur weiteren Verwendung der eingebauten Produktprogrammplanung beantragt werden. Bitte füllen Sie den folgenden Fragebogen aus, um die Migration zur Planungsoptimierung zu starten und ggf. eine Ausnahme zu beantragen. [Fragebogen zur Migration zur Planungsoptimierung und zur Ausnahme](https://go.microsoft.com/fwlink/?linkid=2144962)

## <a name="cause"></a>Ursache

Wenn Sie die Planung ausführen und keine Funktionen zur Produktionssteuerung verwenden, sollten Sie eine Migration auf Planungsoptimierung in Betracht ziehen. Die eingebaute Masterplanplanung wird außer Betrieb genommen. Wenn Sie sie also weiterhin verwenden möchten, ohne die Fehlermeldung zu erhalten, müssen Sie eine Ausnahme bei Microsoft beantragen.

## <a name="resolution"></a>Lösung

Weitere Informationen zur Migration zur Planungsoptimierung oder zur Beantragung einer Ausnahme, damit Sie stattdessen weiterhin die veraltete integrierte Planungs-Engine verwenden können, finden Sie unter [Migration zur Planungsoptimierung für die Masterplanung](/dynamics365/supply-chain/master-planning/new-master-planning-engine).
