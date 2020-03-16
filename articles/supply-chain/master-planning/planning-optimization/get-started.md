---
title: Erste Schritte mit der Planungsoptimierung
description: In diesem Thema wird erläutert, wie Sie mit der Verwendung der Funktionalität der Planungsoptimierung beginnen.
author: ChristianRytt
manager: AnnBe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 3e64699005387adcc92e2e7c9fefad68a9de85c0
ms.sourcegitcommit: a688c864fc609e35072ad8fd2c01d71f6a5ee7b9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "3076131"
---
# <a name="get-started-with-planning-optimization"></a>Erste Schritte mit der Planungsoptimierung

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

Die Funktionalität der Planungsoptimierung unterstützt derzeit nicht alle Funktionen, die in der in Microsoft Dynamics 365 Supply Chain Management integrierten Planungs-Engine verfügbar sind. Daher ist es wichtig, dass Sie prüfen, ob der derzeit in der Planungsoptimierung verfügbare Funktionsumfang Ihren Anforderungen entspricht. Standardmäßig ist die Funktionalität der Planungsoptimierung in Dynamics Lifecycle Services (LCS) nicht standardmäßig aktiviert. Daher haben Sie die Möglichkeit, Ihre Bewertung durchzuführen, bevor sie eingeschaltet wird.

Schließlich wird die Planungsoptimierung die bestehende integrierte Supply Chain Management Planungs-Engine ersetzen.

Bevor Sie die Planungsoptimierung einschalten, empfehlen wir Ihnen dringend, die Ergebnisse der Anpassungsanalyse der Planungsoptimierung auszuwerten. Weitere Informationen finden Sie unter [Planungsoptimierung Fit-Analyse](planning-optimization-fit-analysis.md).

### <a name="licensing"></a>Lizenzierung

Wenn Sie die Masterplanung mit Ihrer aktuellen Lizenz durchführen können, müssen Sie keine zusätzliche Lizenz kaufen, um mit der Planungsoptimierung zu beginnen.

### <a name="install-the-add-in"></a>Installieren des Add-Ins

Um die Planungsoptimierung zu nutzen, installieren Sie das Add-In Planungsoptimierung für Dynamics 365 Supply Chain Management. Sie können auf das Add-In aus Ihrem LCS-Projekt zugreifen und die Funktionalität der Planungsoptimierung über die Benutzeroberfläche (UI) von Supply Chain Management einschalten.

> [!NOTE]
> Die Voraussetzung für die Planungsoptimierung ist eine LCS-fähige Hochverfügbarkeitsumgebung (keine OneBox-Umgebung) mit Dynamics 365 Supply Chain Management Version 10.0.7 oder höher.

1. Melden Sie sich bei LCS an und öffnen Sie die gewünschte Umgebung.
1. Gehen Sie zu **Vollständige Details**.
1. Scrollen Sie zum Inforegister **Umgebungs-Add-Ins**.
1. Wählen Sie **Installieren Sie ein neues Add-In**.
1. Wählen Sie **Planungsoptimierung**.
1. Befolgen Sie die Installationsanleitung und erklären Sie sich mit den Allgemeinen Geschäftsbedingungen einverstanden.
1. Wählen Sie **Installieren**.
1. Auf dem Inforegister **Umgebungs-Add-Ins** sollte die Installation der Planungsoptimierung angezeigt werden.
1. Nach ein paar Minuten sollte sich **Wird installiert ...** in **Installiert** ändern (möglicherweise müssen Sie die Seite aktualisieren). Nach der Installation können Sie die Planungsoptimierung in Dynamics 365 Supply Chain Management aktivieren.

### <a name="planning-optimization-integration"></a>Integration der Planungsoptimierung

Um zu konfigurieren, ob das Planungsoptimierungs-Add-In für die Masterplanung verwendet werden soll, gehen Sie zu **Produktprogrammplanung** \> **Setup** \> **Parameter für Planungsoptimierung**.

#### <a name="connection-status"></a>Verbindungsstatus

Der Verbindungsstatus zeigt den aktuellen Status der Verbindung zwischen Supply Chain Management und dem Service Planungsoptimierung an. Die folgende Tabelle zeigt die möglichen Werte.

| Verbindungsstatus | Beschreibung | Kann die Planungsoptimierung genutzt werden? |
|---|---|---|
| Verbindung hergestellt | Es wurde eine Verbindung zwischen dem Service Planungsoptimierung und dem Supply Chain Management hergestellt. | Ja |
| Aktivieren der Verbindung | Eine Aufforderung zum Einschalten der Verbindung zum Dienst Planungsoptimierung ist derzeit in Bearbeitung. | Nein |
| Verbindung getrennt | Es besteht keine Verbindung zum Service Planungsoptimierung. Die Verbindung kann vom LCS aus eingeschaltet werden, wie bereits in diesem Thema beschrieben. | Nein |
| Verbindung wird deaktiviert | Eine Aufforderung zum Deaktivieren der Verbindung zum Dienst Planungsoptimierung ist derzeit in Bearbeitung. | Nein |
| Status wird abgerufen... | Das System wartet auf Statusinformationen vom Service Planungsoptimierung. | Nein |

#### <a name="the-use-planning-optimization-option"></a>Die Option Planungsoptimierung verwenden

Die Einstellung der Option **Verwendungsplanoptimierung** bestimmt, welche Planungs-Engine für die Masterplanung verwendet wird:

- **Ja** - Die Planungsoptimierung wird für die Masterplanung verwendet.
- **Nein** - Die eingebaute Supply Chain Management Planning Engine wird für die Masterplanung verwendet.

> [!NOTE]
> Wenn bestehende Planungs-Batchjobs, die für die eingebaute Supply Chain Management Planungs-Engine erstellt wurden, ausgelöst werden, während die Option **Verwendungsplanoptimierung** auf **Ja** gesetzt ist, werden diese Jobs fehlschlagen.

### <a name="integration-with-the-setup"></a>Integration mit dem Setup

Wenn die Vorschau der Planungsoptimierung eingeschaltet ist, erfolgt die Masterplanung mit Hilfe des Add-Ins Planungsoptimierung. In diesem Fall sind die Ergebnisse und Merkmale der Masterplanung betroffen.

## <a name="related-resources"></a>Zugehörige Ressourcen

[Allgemeine Geschäftsbedingungen für die Vorschau](https://go.microsoft.com/fwlink/?linkid=2015274)

[Planungsoptimierung – Übersicht](planning-optimization-overview.md)

[Planungsoptimierung Fit-Analyse](planning-optimization-fit-analysis.md)

[Planhistorie und Planungsprotokolle anzeigen](plan-history-logs.md)

[Filter auf einen Plan anwenden](plan-filters.md)

[Abbrechen eines Planungsauftrags](cancel-planning-job.md)
