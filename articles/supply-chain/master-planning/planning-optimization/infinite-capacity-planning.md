---
title: Planung mit unendlicher Kapazität
description: Dieses Thema enthält Informationen zur Planung mit unbegrenzter Kapazität für die Planungsoptimierung. Außerdem werden aktuelle Funktionseinschränkungen beschrieben.
author: crytt
ms.date: 09/02/2021
ms.topic: article
ms.search.form: RouteInventProd
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-06-09
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 2e730340cddac107b04a6b5877e51b84f4dd7b21
ms.sourcegitcommit: a21166da59675e37890786ebf7e0f198507f7c9b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/03/2021
ms.locfileid: "7471667"
---
# <a name="scheduling-with-infinite-capacity"></a>Planung mit unendlicher Kapazität

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

Die Funktion *Unendliche Kapazitätsplanung für die Planungsoptimierung* führt eine Planung auf Basis von Arbeitsplaninformationen ein. Sie können Aufträge basierend auf einer Vielzahl von Arbeitsplankonfigurationen planen. Die Planung für die Planungsoptimierung umfasst häufig verwendete Arbeitsplaneinstellungen, einschließlich der Arbeitsplan-Arbeitsgangsequenz oder Anforderungen an Arbeitsplan-Arbeitsgangressourcen.

## <a name="turn-on-the-infinite-capacity-scheduling-feature"></a>Die Planungsfunktion für unbegrenzte Kapazitäten aktivieren

Wenn Ihr System noch nicht über die in diesem Thema beschriebene Funktion verfügt, öffnen Sie die [Funktionsverwaltung](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) und schalten Sie die Funktion *Unendliche Kapazitätsplanung für die Planungsoptimierung* ein.

## <a name="added-functionality"></a>Hinzugefügte Funktionalität

Die Funktion *Unendliche Kapazitätsplanung für die Planungsoptimierung* ermöglicht die Auftragsplanung auf Basis von Arbeitsplaninformationen. Daher können Arbeitsplaneinstellungen verwendet werden, um Produktionsprozesse zu planen. Obwohl diese Funktion einige Einschränkungen aufweist, die die integrierte Produktprogrammplanung nicht hat, unterstützt sie die gängigsten Funktionen, die für Fertigungsszenarien erforderlich sind.

Die Funktion berücksichtigt sowohl *einfache Arbeitspläne* als auch *Arbeitsplan-Netzwerke*. Durch die Verwendung des Felds **Weiter** für einen Arbeitsplan-Arbeitsgang können Sie komplexe Arbeitspläne mit mehreren Ausgangspunkten und mehreren parallel laufenden Arbeitsgängen einrichten. Das System berücksichtigt bei der Planung komplexe Arbeitsplanstrukturen dieser Art.

Darüber hinaus unterstützt die Funktion *parallele Arbeitsgänge* bei Arbeitsplänen. Durch die Verwendung der Optionen *Primär* und *Sekundär* im Feld **Priorität** auf Arbeitsplan-Arbeitsgängen können Sie eine Arbeitsplanstruktur definieren, bei der ein Arbeitsplan-Arbeitsgang der primäre Vorgang und ein anderer Vorgang sekundär ist. In diesem Fall berücksichtigt das System bei der Planung die Arbeitsplanstruktur.

Bei des Planungsprozesses berücksichtigt das System auch die *Ressourcenanforderungen*, die für einen Arbeitsgang angegeben sind. Das System verwendet Ressourcenanforderungen, um zu bestimmen, welche Ressourcen zum Ausführen des Arbeitsgangs erforderlich sind. Derzeit unterstützt die Funktion *Unendliche Kapazitätsplanung für die Planungsoptimierung* die folgenden Arten von Ressourcenanforderungen:

- Ressourcentyp
- Ressource
- Ressourcengruppe
- Fähigkeit

> [!NOTE]
> Anforderungen, die sich auf die Personalverwaltung beziehen, wie z. B. Fähigkeiten oder Zertifikatsanforderungen, werden noch nicht unterstützt.

Die Funktion unterstützt auch die **Rüstzeit** und die **Runtime** betriebliche Eigenschaften. Wenn Sie diese Eigenschaften für einen Arbeitsplan-Arbeitsgang festlegen, erstellt der Planungsprozess die entsprechenden Einrichtungs- und Verarbeitungsvorgänge.

Zusammenfassend lässt sich sagen, dass die Planung für die Planungsoptimierung die am häufigsten verwendeten Szenarien unterstützt. Sie können die Arbeitsgänge erstellen, primäre und sekundäre Vorgänge hinzufügen, die nächsten Vorgänge definieren, Ressourcenanforderungen hinzufügen und Rüstzeit und Runtime hinzufügen. Das System berücksichtigt diese Informationen dann bei der Planung.

## <a name="limitations"></a>Einschränkungen

Die folgenden Einschränkungen gelten, wenn Sie die Planung für die Planungsoptimierung verwenden:

- Die Funktion unterstützt nur die Auftragsplanung. Einstellungen, die sich auf die Arbeitsgangplanung beziehen, werden bei der Planung nicht berücksichtigt, unabhängig von der Planungsmethoden in Produktprogrammplänen.
- Die Funktion unterstützt nur unendliche Kapazität.
- Die Funktion unterstützt keine Funktionalität der Ressourcenauslastung.
- Die Funktion berücksichtigt keinen Arbeitsplanausschuss.
- Die Funktion unterstützt *Dauer* nur als primäre Ressourcenauswahl.

Bitte beachten Sie, dass die Funktion *Unendliche Kapazitätsplanung für die Planungsoptimierung* ständig verbessert wird. Microsoft geht davon aus, dass in zukünftigen Versionen die Unterstützung für zusätzliche Planungseinstellungen eingeführt wird.
