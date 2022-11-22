---
title: Erste Schritte mit der Produktprogrammplanung
description: In diesem Artikel wird erläutert, wie Sie mit der Verwendung der Funktionalität der Produktprogrammplanung in Dynamics 365 Supply Chain Management beginnen.
author: t-benebo
ms.date: 05/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 4b986461e90b356580da8a136c1da95e7dc64696
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780410"
---
# <a name="get-started-with-master-planning"></a>Erste Schritte mit der Produktprogrammplanung

[!include [banner](../../includes/banner.md)]

Die Hauptplanung in Supply Chain Management wird von einem externen Dienst namens Planning Optimization Add-In für Dynamics 365 Supply Chain Management bereitgestellt wird. In diesem Thema wird erklärt, wie Sie diesen Service erhalten und einrichten.

## <a name="availability"></a>Verfügbarkeit

Die Planungsoptimierung ist derzeit in den folgenden Azure-Gebieten verfügbar: Vereinigte Staaten, Kanada, Brasilien, Europa, Frankreich, Vereinigtes Königreich, Norwegen, Schweiz, Australien, Asien-Pazifik, Japan und Indien. Wenn Sie versuchen, das Add-In aus einer anderen geografischen Region zu installieren, zeigt LCS die Meldung an, dass diese geografische Region nicht unterstützt wird. Weitere Informationen zu Azure-Geografien und den zugehörigen Regionen finden Sie unter [Azure-Geografien](https://azure.microsoft.com/global-infrastructure/geographies/#geographies).

Beachten Sie, dass Planungsoptimierung keine lokalen Bereitstellungen von Dynamics 365 Supply Chain Management unterstützt.

## <a name="licensing"></a>Lizenzierung

Wenn Sie die Masterplanung mit Ihrer aktuellen Lizenz durchführen können, müssen Sie keine zusätzliche Lizenz kaufen, um mit der Planungsoptimierung zu beginnen.

## <a name="install-and-enable-planning-optimization"></a>Planungsoptimierung installieren und aktivieren

Um die Planungsoptimierung verwenden zu können, müssen Sie sicherstellen, dass auf Ihrem System alle Voraussetzungen vorhanden sind, den Lizenzschlüssel aktivieren und das Planungsoptimierungs-Add-In für Dynamics 365 Supply Chain Management installieren.

### <a name="prerequisites"></a>Voraussetzungen

Bevor Sie die das Planungsoptimierungs-Add-In installieren, müssen die folgenden Voraussetzungen erfüllt sein:

- Sie müssen Supply Chain Management in einer LCS-fähigen Hochverfügbarkeitsumgebung, Ebene 2 oder höher (keine OneBox-Umgebung) mit Dynamics 365 Supply Chain Management Version 10.0.7 oder höher ausführen. Wenn Sie versuchen, das Add-In in einer OneBox-Umgebung zu installieren, wird die Installation nicht abgeschlossen und Sie müssen die Installation abbrechen.

- Ihr System muss für die Power Platform-Integration eingerichtet sein. Weitere Informationen finden Sie unter [Microsoft Power Platform Integration mit Finanz- und Betriebs-Apps](../../../fin-ops-core/dev-itpro/power-platform/overview.md).

### <a name="enable-the-planning-optimization-license"></a>Planungsoptimierungslizenz aktivieren

Um die Planungsoptimierung verwenden zu können, müssen Sie den Konfigurationsschlüssel aktivieren. Führen Sie folgende Schritte durch:

1. Legen Sie Ihr System in den Wartungsmodus ein, wie in [Wartungsmodus](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) beschrieben.
1. Gehen Sie zu **Systemadministration \> Einrichten \> Lizenzkonfiguration**.
1. Auf der Registerkarte **Konfigurationsschlüssel** aktivieren Sie das Kontrollkästchen für **Planungsoptimierung**.
1. Schalten Sie den Wartungsmodus aus, wie in [Wartungsmodus](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) beschrieben.

### <a name="install-the-planning-optimization-add-in"></a>Planungsoptimierungs-Add-In installieren

Sie müssen das Add-In aus Ihrem LCS-Projekt installieren und dann die Funktionalität der Planungsoptimierung über die Benutzeroberfläche von Supply Chain Management aktivieren.

So installieren Sie das Planungsoptimierungs-Add-In:

1. Melden Sie sich bei LCS an und öffnen Sie die gewünschte Umgebung.
1. Gehen Sie zu **Vollständige Details**.
1. Scrollen Sie zum Inforegister **Umgebungs-Add-Ins**.
1. Wählen Sie **Installieren Sie ein neues Add-In**.
1. Wählen Sie **Planungsoptimierung**.
1. Befolgen Sie die Installationsanleitung und erklären Sie sich mit den Allgemeinen Geschäftsbedingungen einverstanden.
1. Wählen Sie **Installieren**.
1. Auf dem Inforegister **Umgebungs-Add-Ins** sollte die Installation der Planungsoptimierung angezeigt werden.
1. Nach ein paar Minuten sollte sich **Wird installiert ...** in **Installiert** ändern (möglicherweise müssen Sie die Seite aktualisieren). Nach der Installation können Sie die Planungsoptimierung in Dynamics 365 Supply Chain Management aktivieren.

Der Hauptzweck der Installation des Add-Ins Planungsoptimierung besteht darin, den Dienst und die Umgebung miteinander zu verbinden. Daher müssen Sie das Add-In in jeder Umgebung, in der Sie die Planungsoptimierung verwenden werden, separat installieren, unabhängig davon, ob Code zwischen den Umgebungen verschoben wird.

## <a name="integrate-planning-optimization-with-your-system"></a>Integrieren der Planungsoptimierung in Ihr System

Um zu konfigurieren, ob das Planungsoptimierungs-Add-In für die Masterplanung verwendet werden soll, gehen Sie zu **Produktprogrammplanung** \> **Setup** \> **Parameter für Planungsoptimierung**.

### <a name="connection-status"></a>Verbindungsstatus

Der Verbindungsstatus zeigt den aktuellen Status der Verbindung zwischen Supply Chain Management und dem Service Planungsoptimierung an. Die folgende Tabelle zeigt die möglichen Werte.

| Verbindungsstatus | Beschreibung | Kann die Planungsoptimierung genutzt werden? |
|---|---|---|
| Verbindung hergestellt | Es wurde eine Verbindung zwischen dem Service Planungsoptimierung und dem Supply Chain Management hergestellt. | Ja |
| Aktivieren der Verbindung | Eine Aufforderung zum Einschalten der Verbindung zum Dienst Planungsoptimierung ist derzeit in Bearbeitung. | Nein |
| Verbindung getrennt | Es besteht keine Verbindung zum Service Planungsoptimierung. Die Verbindung kann vom LCS aus eingeschaltet werden, wie bereits in diesem Artikel beschrieben. | Nein |
| Verbindung wird deaktiviert | Eine Aufforderung zum Deaktivieren der Verbindung zum Dienst Planungsoptimierung ist derzeit in Bearbeitung. | Nein |
| Status wird abgerufen... | Das System wartet auf Statusinformationen vom Service Planungsoptimierung. | Nein |

### <a name="the-use-planning-optimization-option"></a>Die Option Planungsoptimierung verwenden

Die Einstellung der Option **Verwendungsplanoptimierung** bestimmt, welche Planungs-Engine für die Masterplanung verwendet wird:

- **Ja** - Die Planungsoptimierung wird für die Masterplanung verwendet.
- **Nein** - Das veraltete Produktplanungsmodul wird für die Masterplanung verwendet.

Diese Einstellung gilt für alle juristischen Entitäten (Firmen). Es ist nicht möglich, die Planungsoptimierung in einigen juristischen Entitäten und das veraltete Masterplanungsmodul in anderen juristischen Entitäten zu verwenden.

> [!NOTE]
> Wenn bestehende Planungs-Batchjobs, die für die veraltete Masterplanungs-Engine erstellt wurden, ausgelöst werden, während die Option **Verwendungsplanoptimierung** auf **Ja** gesetzt ist, werden diese Jobs fehlschlagen.

### <a name="integration-with-the-setup"></a>Integration mit dem Setup

Wenn die Planungsoptimierung eingeschaltet ist, wird die Produktprogrammplanung mit dem Planungsoptimierungs-Add-In durchgeführt. In diesem Fall sind die Ergebnisse und Merkmale der Masterplanung betroffen.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
