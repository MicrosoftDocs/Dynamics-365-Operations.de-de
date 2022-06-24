---
title: Fehlerbehebung in Planungsoptimierung
description: In diesem Artikel wird beschrieben, wie Sie Probleme beheben, die bei der Arbeit mit Planungsoptimierung auftreten können.
author: t-benebo
ms.date: 05/07/2020
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
ms.author: benebotg
ms.search.validFrom: 2020-5-7
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: f078fda02a11eb2073738d59b45f81698b707653
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8889518"
---
# <a name="troubleshoot-planning-optimization"></a>Fehlerbehebung in Planungsoptimierung 

[!include [banner](../../includes/banner.md)]

In diesem Artikel wird beschrieben, wie Sie allgemeine Probleme beheben, die bei der Arbeit mit Planungsoptimierung auftreten können.

## <a name="installation-of-the-planning-optimization-add-in-doesnt-complete"></a>Die Installation des Planungsoptimierungs-Add-Ins wird nicht abgeschlossen

Die Voraussetzung für die Planungsoptimierung ist eine LCS-fähige (Lifecycle Services) Hochverfügbarkeitsumgebung, Ebene 2 oder höher (keine OneBox-Umgebung) mit Dynamics 365 Supply Chain Management Version 10.0.7 oder höher. Wenn Sie versuchen, das Add-In in einer OneBox-Umgebung zu installieren, wird die Installation nicht abgeschlossen.

**Beheben**: Brechen Sie die Installation ab, und verwenden Sie eine Hochverfügbarkeitsumgebung, Tier 2 oder höher (keine OneBox-Umgebung).

## <a name="planning-of-batch-jobs-fails-when-planning-optimization-is-enabled"></a>Die Planung von Stapeljobs schlägt fehl, wenn die Planungsoptimierung aktiviert ist

Wenn Sie die Planungsoptimierung aktivieren, wird das integrierte Masterplanungsmodul automatisch deaktiviert. Planungs-Batchjobs, die für das eingebaute Supply Chain Management-Planungsmodul erstellt wurden, werden fehlschlagen, wenn sie ausgelöst werden, während die Planungsoptimierung aktiviert ist. Möglicherweise erhalten Sie eine Fehlermeldung wie *Dieser Vorgang löste eine Masterplanung aus, die nicht unterstützt wird, wenn die Planungsoptimierung aktiviert ist*.

**Beheben**: Brechen Sie alle Masterplanungs-Batchjobs ab, die für das integrierte Supply Chain Management-Planungsmodul erstellt wurden.

## <a name="planning-optimization-results-are-different-from-earlier-results"></a>Die Ergebnisse der Planungsoptimierung unterscheiden sich von früheren Ergebnissen

Die Planungsoptimierung unterscheidet sich in einigen Bereichen vom integrierten Masterplanungsdesign. Dies kann auch durch ausstehende Funktionen verursacht werden.

**Beheben**: Führen Sie die Anpassungsanalyse für die Planungsoptimierung durch, und analysieren Sie dann die Ergebnisse, während Sie die zugehörige Dokumentation lesen, um die Auswirkungen zu verstehen. Weitere Informationen finden Sie unter [Planungsoptimierung Fit-Analyse](planning-optimization-fit-analysis.md).

## <a name="cant-enable-planning-optimization"></a>Die Planungsoptimierung kann nicht aktiviert werden

Der **Verbindungsstatus** muss **Verbunden** sein, bevor Sie **Planungsoptimierung verwenden** auf **Ja** setzen können. Weitere Informationen finden Sie unter [Erststart mit Planungsoptimierung](get-started.md).

**Beheben**: Stellen Sie sicher, dass das Plannungsoptimierungs-Add-In erfolgreich installiert wurde.

## <a name="error-message-is-shown-during-ctp"></a>Während der CTP wird eine Fehlermeldung angezeigt

Wenn Sie versuchen, CTP (Verfügbarkeitszusage) aus einem Kaufauftrag auszuführen, wenn die Planungsoptimierung aktiviert ist, wird die folgende Fehlermeldung angezeigt: *Dieser Vorgang löste eine Masterplanung aus, die nicht unterstützt wird, wenn die Planungsoptimierung aktiviert ist*.

Dies hängt mit einer ausstehenden Funktion zusammen, die im Rahmen der Unterstützung von Fertigungsaufträgen geplant ist.

**Beheben**: Vermeiden Sie CTP-Berechnungen, wenn die Planungsoptimierung aktiviert ist, bis die CTP-Unterstützung verfügbar ist.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Erste Schritte mit der Planungsoptimierung](get-started.md)

[Passanalyse zu Planungsoptimierung](planning-optimization-fit-analysis.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]