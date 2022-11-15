---
title: Planung mit unendlicher Kapazität
description: Dieser Artikel enthält Informationen über unbegrenzte Kapazitätsplanung. Außerdem werden aktuelle Funktionseinschränkungen beschrieben.
author: t-benebo
ms.date: 08/09/2022
ms.topic: article
ms.search.form: RouteInventProd
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-06-09
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 7249734e5d2644145a36276dbc818a40b5962805
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740004"
---
# <a name="scheduling-with-infinite-capacity"></a>Planung mit unendlicher Kapazität

[!include [banner](../../includes/banner.md)]

Die Funktion *Unendliche Kapazitätsplanung für die Planungsoptimierung* führt eine Planung auf Basis von Arbeitsplaninformationen ein. Sie können Aufträge basierend auf einer Vielzahl von Arbeitsplankonfigurationen planen. Die Planung umfasst häufig verwendete Arbeitsplaneinstellungen, einschließlich der Arbeitsplan-Arbeitsgangsequenz oder Anforderungen an Arbeitsplan-Arbeitsgangressourcen.

## <a name="turn-the-infinite-capacity-scheduling-feature-on-or-off"></a>Die Planungsfunktion für unbegrenzte Kapazitäten aktivieren oder deaktivieren

Um diese Funktion nutzen zu können, muss sie für Ihr System aktiviert werden. Ab Supply Chain Management Version 10.0.29 ist die Funktion standardmäßig aktiviert. Administratoren können diese Funktionalität an- oder ausschalten, indem Sie nach der Funktion zur *Endloskapazitätsplanung zur Planungsoptimierung* im Arbeitsbereich [Funktionsverwaltung](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) suchen.

Weitere Informationen zu dieser Funktion finden Sie unter [Planung mit Ressourcenauswahl basierend auf der Funktion](capability-based-scheduling.md).

## <a name="added-functionality"></a>Hinzugefügte Funktionalität

Die Funktion *Unendliche Kapazitätsplanung für die Planungsoptimierung* ermöglicht die Auftragsplanung auf Basis von Arbeitsplaninformationen. Daher können Arbeitsplaneinstellungen verwendet werden, um Produktionsprozesse zu planen. Obwohl diese Funktion einige Einschränkungen aufweist, die das veraltete Produktprogrammplanungsmodul nicht hat, unterstützt sie die gängigsten Funktionen, die für Fertigungsszenarien erforderlich sind.

Die Funktion berücksichtigt sowohl *einfache Arbeitspläne* als auch *Arbeitsplan-Netzwerke*. Durch die Verwendung des Felds **Weiter** für einen Arbeitsplan-Arbeitsgang können Sie komplexe Arbeitspläne mit mehreren Ausgangspunkten und mehreren parallel laufenden Arbeitsgängen einrichten. Das System berücksichtigt bei der Planung komplexe Arbeitsplanstrukturen dieser Art.

Darüber hinaus unterstützt die Funktion *parallele Arbeitsgänge* bei Arbeitsplänen. Durch die Verwendung der Optionen *Primär* und *Sekundär* im Feld **Priorität** auf Arbeitsplan-Arbeitsgängen können Sie eine Arbeitsplanstruktur definieren, bei der ein Arbeitsplan-Arbeitsgang der primäre Vorgang und ein anderer Vorgang sekundär ist. In diesem Fall berücksichtigt das System bei der Planung die Arbeitsplanstruktur.

Bei des Planungsprozesses berücksichtigt das System auch die *Ressourcenanforderungen*, die für einen Arbeitsgang angegeben sind. Das System verwendet Ressourcenanforderungen, um zu bestimmen, welche Ressourcen zum Ausführen des Arbeitsgangs erforderlich sind. Derzeit unterstützt die Funktion *Unendliche Kapazitätsplanung für die Planungsoptimierung* die folgenden Arten von Ressourcenanforderungen:

- Ressourcentyp
- Ressource
- Ressourcengruppe
- Funktion (Weitere Informationen finden Sie unter [Planung mit Ressourcenauswahl basierend auf der Funktion](capability-based-scheduling.md)).

> [!NOTE]
>
> - Wenn die Ressource und/oder die Ressourcengruppe auf unbegrenzte Kapazität eingestellt sind, betrachtet die Hauptplanung sie als unbegrenzte Kapazität.
> - Anforderungen, die sich auf die Personalverwaltung beziehen, wie z. B. Fähigkeiten oder Zertifikatsanforderungen, werden noch nicht unterstützt.

Die Funktion unterstützt auch die **Rüstzeit** und die **Runtime** betriebliche Eigenschaften. Wenn Sie diese Eigenschaften für einen Arbeitsplan-Arbeitsgang festlegen, erstellt der Planungsprozess die entsprechenden Einrichtungs- und Verarbeitungsvorgänge.

Zusammenfassend lässt sich sagen, dass die Planung die am häufigsten verwendeten Szenarien unterstützt. Sie können die Arbeitsgänge erstellen, primäre und sekundäre Vorgänge hinzufügen, die nächsten Vorgänge definieren, Ressourcenanforderungen hinzufügen und Rüstzeit und Runtime hinzufügen. Das System berücksichtigt diese Informationen dann bei der Planung.

## <a name="limitations"></a>Einschränkungen

Die folgenden Einschränkungen gelten, wenn Sie die Funktion *Unbegrenzte Kapazitäsplanung für die Planungsoptimierung* verwenden:

- Die Funktion unterstützt nur unendliche Kapazität.
- Die Funktion unterstützt keine Funktionalität der Ressourcenauslastung.
- Die Funktion berücksichtigt keinen Arbeitsplanausschuss.
- Die Funktion unterstützt *Dauer* nur als primäre Ressourcenauswahl.
