---
title: Releaseprozess und Releaseverlauf der Planungsoptimierung
description: Dieses Thema enthält Informationen zum Releaseprozess und zum Releaseverlauf für Planungsoptimierung.
author: crytt
ms.date: 7/28/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-28
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 64c8cd3ed6ff522a9ef90831ae502c5d50fbc05816aaa764d2a8e122934fc2bb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6722390"
---
# <a name="planning-optimization-release-process-and-release-history"></a>Releaseprozess und Releaseverlauf der Planungsoptimierung

[!include [banner](../../includes/banner.md)]

Microsoft aktualisiert die Planungsoptimierung monatlich. Je nach geschäftlichen Anforderungen veröffentlichen wir jedoch gelegentlich zusätzliche Updates zwischen den geplanten Releases.

Jedes Release wird in den einzelnen Regionen veröffentlicht, in denen die Planungsoptimierung verfügbar ist. Der Prozess dauert in der Regel drei Tage.

Während die Planungsoptimierung aktualisiert wird, läuft die Produktprogrammplanung möglicherweise etwas langsamer als gewöhnlich.

Umgebungen, die die Planungsoptimierung verwenden, erhalten automatisch die neueste Version. Es ist keine Benutzeraktion erforderlich: Der Dienst wird automatisch aktualisiert. Allerdings werden Breaking-Change-Funktionalitäten niemals automatisch in Umgebungen übertragen. Standardmäßig sind alle Änderungen, die als erheblich betrachtet werden, deaktiviert und müssen explizit mit der [Funktionsverwaltung](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) aktiviert werden. Daher werden diese Änderungen in Umgebungen erst angezeigt, wenn Sie sie aktivieren.

Da keine Benachrichtigungen angezeigt werden, wenn die Planungsoptimierung in Ihrer Umgebung aktualisiert wird, können Sie die Versionshinweise in der folgenden Tabelle überprüfen, um festzustellen, wann Änderungen veröffentlicht wurden und welche Funktionen sie eingeführt haben. Diese Tabelle zeigt die Änderungen, die für die Planungsoptimierung freigegeben wurden, ob diese Änderungen einer Funktion aus der Funktionsverwaltung zugeordnet sind und das Datum des Release.

| Änderungen | Funktionsverwaltungsdetails | Freigabedatum |
|---|---|---|
| <p>Ressourcentypanforderungen für die Zeitplanung mit unbegrenzter Kapazität</p><p>Ressourceneffizienz und Kalendereffizienz für die Zeitplanung mit unbegrenzter Kapazität</p><p>Weitere Informationen finden Sie unter [Zeitplanung mit unbegrenzter Kapazität](infinite-capacity-planning.md). | <p>Verfügbar in der Funktionsverwaltung ab Version 10.0.20.</p><p>Funktionsname: *Zeitplanung mit unbegrenzter Kapazität für Planungsoptimierung*</p> | 6. Juli 2021 |
| Allgemeine Qualitätsverbesserungen | Es ist keine Funktionsverwaltung erforderlich. | 6. Juli 2021 |

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
