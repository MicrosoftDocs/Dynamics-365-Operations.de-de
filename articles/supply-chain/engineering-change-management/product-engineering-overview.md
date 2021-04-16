---
title: Überblick über die Verwaltung für technische Änderungen
description: Dieses Thema bietet einen Überblick über die Verwaltung für technische Änderungen, die Sie bei der Planung und Verwaltung der Produktversionsverwaltung sowie bei der Verwaltung von Produktlebenszyklen und technischen Änderungen unterstützt.
author: t-benebo
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 964db71efc9dc81d60199e37de8668de9d667496
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842080"
---
# <a name="engineering-change-management-overview"></a>Überblick über die Verwaltung für technische Änderungen

[!include [banner](../includes/banner.md)]

## <a name="feature-summary"></a>Funktionszusammenfassung

Heutige Hersteller benötigen ein starkes Produktdatenmanagement, eine Versionskontrolle und eine Verwaltung für technische Änderungen, um in einer Welt ständig kürzer werdender Produktlebenszyklen, erhöhter Qualitäts- und Zuverlässigkeitsanforderungen und eines verstärkten Fokus auf die Produktsicherheit erfolgreich zu sein.

Die Verwaltung für technische Änderungen bringt Struktur und Disziplin in den Prozess der Produktdatenverwaltung und ermöglicht es, Produkte auf kontrollierte Weise zu definieren, freizugeben und zu überarbeiten, die durch Workflows unterstützt wird. Mit Hilfe von Produktversionen und der Verwaltung für technische Änderungen können Sie technische Änderungen während des gesamten Lebenszyklus eines Produkts dokumentieren, deren Auswirkungen bewerten und anwenden.

Die Verwaltung für technische Änderungen unterstützt Sie bei der Planung und Verwaltung von Produktversionen sowie bei der Verwaltung von Produktlebenszyklen und technischen Änderungen. Hier ist eine Liste der wichtigsten Funktionen:

- Produktversionsverwaltung
- Erweiterte Produktfreigabefunktionalität, mit der Sie Produktstammdaten in einer juristischen Entität (der Engineering-Firma) pflegen und das vollständig konfigurierte freigegebene Produkt an andere juristische Entitäten veröffentlichen können
- Regeln zur Überprüfung, ob erforderliche Informationen eingegeben wurden, bevor eine Produktversion aktiviert wird (Bereitschaftsprüfungen)
- Verbessertes Produktlebenszyklus-Management durch fein abgestufte Kontrolle darüber, wann ein freigegebenes Produkt in bestimmten Geschäftsprozessen verwendet werden kann
- Technische Änderungsanforderungen, die durch Workflows unterstützt werden
- Technische Änderungsaufträge, die durch Workflows unterstützt werden

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4HE6B]

Das vorhergehende Video ([Funktionalitäten der Änderungsverwaltung in Dynamics 365 Supply Chain Management](https://youtu.be/N313FqvRuBc)) ist in der [Finance and Operations-Wiedergabeliste](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) enthalten, die auf YouTube verfügbar ist.

## <a name="turn-on-the-engineering-change-management-and-version-dimension-features-for-your-system"></a>Schalten Sie die Funktionen für technische Änderungen Verwaltung für technische Änderungen und Versionsverwaltung für Ihr System ein

Bevor Sie die Verwaltung für technische Änderungen nutzen können, müssen Sie sowohl die Funktion *Verwaltung für technische Änderungen* als auch deren Konfigurationsschlüssel aktivieren. Wenn Sie auch die Versionsdimension von Produkten in Transaktionen verfolgen wollen (optional), dann müssen Sie auch die Funktion *Produktversionsdimension* und deren Konfigurationsschlüssel aktivieren.

Schalten Sie zunächst die Funktionen ein, indem Sie diese Schritte ausführen.

1. Navigieren Sie zu [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
1. Suchen Sie nach Updates.
1. Schalten Sie die Funktion ein, die **Verwaltung für technische Änderungen** genannt wird.
1. Wenn Sie sie verwenden wollen, dann schalten Sie auch die Funktion ein, die **Produktdimension Version** heißt.

Als nächstes schalten Sie die Konfigurationstasten ein, indem Sie diese Schritte befolgen.

1. Legen Sie Ihr System in den Wartungsmodus ein, wie in [Wartungsmodus](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) beschrieben.
1. Gehen Sie zu **Systemadministration \> Einrichten \> Lizenzkonfiguration**.
1. Erweitern Sie den Knoten **Handel**
1. Aktivieren Sie das Kontrollkästchen **Verwaltung für technische Änderungen**.
1. Wenn Sie es verwenden möchten, dann aktivieren Sie auch das Kontrollkästchen **Produktdimension - Version**.
1. Schalten Sie den Wartungsmodus aus, wie in [Wartungsmodus](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) beschrieben.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
