---
title: Fehlerbehebung in Planungsoptimierung
description: In diesem Thema wird beschrieben, wie Sie Probleme beheben, die bei der Arbeit mit Planungsoptimierung auftreten können.
author: ChristianRytt
manager: tfehr
ms.date: 05/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-5-7
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 8e67a6faf52b51264555b06f56b289d19ca580d6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992494"
---
# <a name="troubleshoot-planning-optimization"></a>Fehlerbehebung in Planungsoptimierung 

[!include [banner](../../includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie allgemeine Probleme beheben, die bei der Arbeit mit Planungsoptimierung auftreten können.

## <a name="installation-of-the-planning-optimization-add-in-doesnt-complete"></a>Die Installation des Planungsoptimierungs-Add-Ins wird nicht abgeschlossen

Die Voraussetzung für die Planungsoptimierung ist eine LCS-fähige (Lifecycle Services) Hochverfügbarkeitsumgebung, Ebene 2 oder höher (keine OneBox-Umgebung) mit Dynamics 365 Supply Chain Management Version 10.0.7 oder höher. Wenn Sie versuchen, das Add-In in einer OneBox-Umgebung zu installieren, wird die Installation nicht abgeschlossen.

**Beheben**: Brechen Sie die Installation ab, und verwenden Sie eine Hochverfügbarkeitsumgebung, Tier 2 oder höher (keine OneBox-Umgebung).

## <a name="planning-of-batch-jobs-fails-when-planning-optimization-is-enabled"></a>Die Planung von Stapeljobs schlägt fehl, wenn die Planungsoptimierung aktiviert ist

Wenn Sie die Planungsoptimierung aktivieren, wird das integrierte Masterplanungsmodul automatisch deaktiviert. Planungs-Batchjobs, die für das eingebaute Supply Chain Management-Planungsmodul erstellt wurden, werden fehlschlagen, wenn sie ausgelöst werden, während die Planungsoptimierung aktiviert ist. Möglicherweise erhalten Sie eine Fehlermeldung wie *Dieser Vorgang löste eine Masterplanung aus, die nicht unterstützt wird, wenn die Planungsoptimierung aktiviert ist*.

**Beheben**: Brechen Sie alle Masterplanungs-Batchjobs ab, die für das integrierte Supply Chain Management-Planungsmodul erstellt wurden.

## <a name="planning-optimization-results-are-different-from-earlier-results"></a>Die Ergebnisse der Planungsoptimierung unterscheiden sich von früheren Ergebnissen

Die Planungsoptimierung unterscheidet sich in einigen Bereichen vom integrierten Masterplanungsdesign. Dies kann auch durch ausstehende Funktionen verursacht werden.

**Beheben**: Führen Sie die Anpassungsanalyse für die Planungsoptimierung durch, und analysieren Sie dann die Ergebnisse, während Sie die zugehörige Dokumentation lesen, um die Auswirkungen zu verstehen. Weitere Informationen finden Sie unter [Planungsoptimierung Fit-Analyse](planning-optimization-fit-analysis.md).

## <a name="master-planning-doesnt-respect-the-coverage-time-fence"></a>Die Masterplanung berücksichtigt nicht den Zeitrahmen für die Abdeckung

Dies wird durch eine ausstehende Funktion für die Planungsoptimierung verursacht.

**Beheben**: Filtern oder löschen Sie geplante Aufträge, bis die Funktion „Ausstehend“ verfügbar ist, um Liefervorschläge außerhalb des Zeitrahmens für die Abdeckung zu entfernen.

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
