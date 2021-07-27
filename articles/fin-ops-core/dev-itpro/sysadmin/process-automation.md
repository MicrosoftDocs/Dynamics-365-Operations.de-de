---
title: Prozessautomatisierung
description: Dieses Thema enthält Details dazu, wie die Prozessautomatisierung die einfache Planung von Prozessen ermöglicht, die vom Batch-Server ausgeführt werden.
author: RyanCCarlson2
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProcessScheduleSeries
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-06-30
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: a861710e29962e1222d95bfa8c4ef7407bd3401d
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6343983"
---
# <a name="process-automation"></a>Prozessautomatisierung

[!include[banner](../includes/banner.md)]

Prozessautomatisierung ermöglicht die einfache Planung von Prozessen, die vom Batch-Server ausgeführt werden. Die aktualisierte Kalenderansicht der geplanten Arbeit ermöglicht es Endbenutzern, geplante und abgeschlossene Arbeiten anzuzeigen und Maßnahmen zu ergreifen.

## <a name="administration"></a>Verwaltung

Die zentrale Administrationsseite für alle Prozessautomatisierungen finden Sie im Systemadministrationsmodul im Menü **Einrichtung**. Diese Seite listet alle automatisierten Prozesse (Serien) auf, die im System eingerichtet sind. Außerdem können Sie direkt von dieser Seite aus neue Prozessautomatisierungen hinzufügen. Nachdem eine Serie eingerichtet wurde, können Sie jede Serie aus dieser Liste verwalten. Sie können die gesamte Serie bearbeiten, löschen, alle Vorkommen in einer Listenansicht anzeigen oder die Serie deaktivieren, wenn Sie die geplante Arbeit für eine Weile anhalten möchten. 

Alle Prozesse, die in der Funktionsverwaltung deaktiviert sind, werden nicht angezeigt, wenn die Funktion deaktiviert ist. Darüber hinaus plant das Planungsmodul zur Prozessautomatisierung keine Vorkommen oder Hintergrundprozesse für eine deaktivierte Funktion. Durch erneutes Aktivieren der Funktion werden geplante Ereignisse oder Hintergrundprozesse aus der Vergangenheit sofort ausgeführt. Die Scheduling-Engine der Prozessautomatisierung stützt sich auf den Batchauftrag des Systems, **Prozessautomatisierungsabfrage-Systemjob**, um ausgeführt zu werden. Der Job sollte zu keiner Zeit verändert oder manipuliert werden. 

## <a name="calendar-view"></a>Kalenderansicht

Einer der Hauptvorteile der Prozessautomatisierung ist die Möglichkeit, die geplanten Arbeiten in einer einfachen Kalenderansicht anzuzeigen.  In dieser Ansicht können Sie die Arbeit für jeweils eine Woche anzeigen. Sie sehen diese Ansicht auf der rechten Seite der Seite **Prozessautomatisierung**. Sie wird mit der geplanten Arbeit für die ausgewählte Serie gefüllt. 

[![Prozessautomatisierungskalender.](./media/CalendarView2.png)](./media/CalendarView2.png)

## <a name="occurrence-changes"></a>Vorkommensänderungen

Jedes Vorkommen kann geändert werden, ohne dass dies Auswirkungen auf andere Vorkommen hat, die durch die Serie definiert sind, aus der sie stammen. Vorkommen geplanter Arbeiten können in der Kalenderansicht bearbeitet werden, indem die Schaltfläche **Anzeigen/Bearbeiten** und **Vorkommen** ausgewählt werden. Auf dieser Seite können Sie auf alle Einstellungen zugreifen, die ursprünglich im Serien-Setup-Assistenten angezeigt wurden, und Sie können eine einmalige Änderung für das ausgewählte Vorkommen vornehmen. Das Vorkommen geplanter Arbeiten kann auch deaktiviert werden, indem die Schaltfläche **Deaktivieren** in der Kalenderansicht ausgewählt wird.

## <a name="developer-documentation"></a>Entwicklerdokumentation

Mit dem Prozessautomatisierungs-Framework können Entwickler das Prozessautomatisierungs-Framework erweitern. Die Dokumentation [Prozessautomatisierungs-Framework](../process-automation/process-automation-framework.md) enthält Informationen darüber, wie Sie benutzerdefinierte Prozesse erstellen können, die von dem mit dem Prozessautomatisierungsassistenten geplanten Batch-Server ausgeführt werden müssen und automatisch in der Kalenderansicht angezeigt werden.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
