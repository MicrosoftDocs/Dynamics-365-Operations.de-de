---
title: Planungsoptimierung – Übersicht
description: Dieses Thema gibt einen Überblick über die Funktionalität der Planungsoptimierung.
author: ChristianRytt
manager: tfehr
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: f88ee8067fdd816ba6890ee28bafe8fa4d3b3ac5
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208730"
---
# <a name="planning-optimization-overview"></a>Planungsoptimierung – Übersicht

[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

Das Planning Optimization Add-in für Microsoft Dynamics 365 Supply Chain Management ermöglicht die Berechnung der Masterplanung außerhalb von Dynamics 365 Supply Chain Management und der zugehörigen SQL-Datenbank. Zu den Vorteilen, die mit der Funktionalität der Planungsoptimierung verbunden sind, gehören eine verbesserte Leistung und minimale Auswirkungen auf die SQL-Datenbank während der Durchführung der Masterplanung. Schnelle Planungsläufe können auch während der Bürozeiten durchgeführt werden, so dass der Planer sofort auf Bedarfs- oder Parameteränderungen reagieren kann.

Um die Planungsoptimierung nutzen zu können, müssen Sie das Add-In Planungsoptimierung aus Ihrem Projekt in Microsoft Dynamics Lifecycle Services (LCS) installieren und die Funktionalität der Planungsoptimierung im Supply Chain Management einschalten. Weitere Informationen finden Sie unter [Erststart mit Planungsoptimierung](get-started.md).

Die folgende Abbildung zeigt den Vorteil der Planungsoptimierung während der Bürozeiten.

![Vorteil der laufenden Planungsoptimierung während der Bürozeiten](media/PlanningOptimization1.png)

## <a name="improved-performance"></a>Verbesserte Leistung

Die Planungsoptimierung kann in Szenarien eingesetzt werden, die langlaufende Masterpläne beinhalten. Es wurde speziell für sehr schnelle Berechnungen mit sehr großen Datenmengen entwickelt. Da es sich um einen hyperskalierbaren mandantenfähigen Dienst handelt, können mehrere Instanzen gleichzeitig zusammenarbeiten, um den Plan zu berechnen. Darüber hinaus entfernt der Planungsservice die Last der Masterplanung aus Ihrem System und arbeitet mit einem Datenstrom, der die Serverlast minimiert.

Die Planungsoptimierung kann Ihnen helfen, die folgenden Ziele zu erreichen:

- Verbessern Sie die Planungsleistung durch eine kürzere Laufzeit.
- Reduzieren Sie die Auswirkungen auf andere Prozesse während des Masterplanungslaufs.
- Führen Sie häufigere Planungsläufe durch. (Sie sind nicht auf tägliche Läufe beschränkt.)
- Seien Sie zuversichtlich, dass das zukünftige Geschäftswachstum das Planungssystem nicht überlastet.

## <a name="architecture-and-data-flow"></a>Architektur und Datenfluss

Wenn das Planungsoptimierung Add-In aus dem LCS installiert wird, wird eine sichere Verbindung zum Dienst Planungsoptimierung hergestellt. Der Service befindet sich im selben Land oder in derselben Region des Rechenzentrums wie die zugehörige Supply Chain Management Instanz. Nach dem Einrichten der Planungsoptimierung werden zur Laufzeit der Masterplanung Stamm- und Bewegungsdaten aus dem Supply Chain Management an den Service Planungsoptimierung gesendet.

Wenn das Add-In Planungsoptimierung deinstalliert wird, werden alle zugehörigen Daten im Service Planungsoptimierung entfernt.

### <a name="high-level-data-flow-for-regeneration-runs"></a>Hochwertiger Datenfluss für Regenerationsläufe

1. Der Supply Chain Management Client sendet ein Signal, um von der Planungsoptimierung einen Planungslauf anzufordern.
2. Die Planungsoptimierung fordert über den integrierten Konnektor die erforderlichen Daten an.
3. Die SQL-Datenbank sendet die angeforderten Informationen über Setup-, Master- und Transaktionsdaten über den Konnektor an die Planungsoptimierung. Der Konnektor übersetzt Informationen zwischen Supply Chain Management und dem Service Planungsoptimierung.
4. Der Service Planungsoptimierung hält planungsrelevante Daten im Speicher und führt die erforderlichen Berechnungen durch.
5. Das Planungsergebnis wird über den Konnektor an die Supply Chain Management Datenbank gesendet. Zu den Ergebnissen gehören Informationen wie Planaufträge und Verursacherinformationen. Die Planungsoptimierung sendet ein Signal an das Supply Chain Management, um anzuzeigen, dass der Planungslauf abgeschlossen ist. Es sendet auch alle relevanten Meldungen und Warnungen.

Die folgende Abbildung zeigt den Datenfluss.

![Datenfluss für Regenerationsläufe](media/PlanningOptimization2.png)

## <a name="related-resources"></a>Zugehörige Ressourcen

[Erste Schritte mit der Planungsoptimierung](get-started.md)

[Planungsoptimierung Fit-Analyse](planning-optimization-fit-analysis.md)

[Planhistorie und Planungsprotokolle anzeigen](plan-history-logs.md)

[Filter auf einen Plan anwenden](plan-filters.md)

[Abbrechen eines Planungsauftrags](cancel-planning-job.md)
