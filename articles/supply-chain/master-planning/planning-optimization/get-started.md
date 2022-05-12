---
title: Erste Schritte mit der Planungsoptimierung
description: In diesem Thema wird erläutert, wie Sie mit der Verwendung der Funktionalität der Planungsoptimierung beginnen.
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
ms.openlocfilehash: a08128f9529e576294181bd70134b02caae54b90
ms.sourcegitcommit: 5130446fd5327595b2d67e67cbd1b5661bb2983c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2022
ms.locfileid: "8648708"
---
# <a name="get-started-with-planning-optimization"></a>Erste Schritte mit der Planungsoptimierung

[!include [banner](../../includes/banner.md)]

Wie [zuvor angekündigt](../../get-started/removed-deprecated-features-scm-updates.md#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios), soll die Planungsoptimierung die vorhandene integrierte Produktprogrammplanungs-Engine ersetzen.

Wenn Sie derzeit die integrierte Produktprogrammplanungs-Engine verwenden, sollten Sie jetzt mit der Planung Ihrer Migration zur Planungsoptimierung beginnen. Es ist wichtig, den Migrationsprozess sofort zu starten, da Ihre Vorgänge möglicherweise beeinträchtigt werden, wenn die Abschreibung erzwungen wird. Um Probleme in letzer Minute bei der Durchsetzung von Abschreibungen zu vermeiden, empfehlen wir Ihnen dringend, die Migration vor dem 1. Dezember 2020 abzuschließen. 

Die Funktionalität der Planungsoptimierung unterstützt derzeit nicht alle Funktionen, die in der Planungs-Engine verfügbar sind, die im Supply Chain Management integriert ist. Daher ist es wichtig, dass Sie prüfen, ob der derzeit in der Planungsoptimierung verfügbare Funktionsumfang Ihren Anforderungen entspricht. Die Planungsoptimierungsfunktion ist derzeit in Dynamics Lifecycle Services (LCS) nicht standardmäßig aktiviert, sodass Sie die Möglichkeit haben, Ihre Auswertung durchzuführen, bevor die Funktion aktiviert wird.

> [!NOTE]
> Sie müssen eine Ausnahme von der Migration zur Planungsoptimierung anfordern, wenn Ihr Produktprogrammplanungsprozesses keine Produktion enthält (Produktprogrammplanung hat geplante Produktionsaufträge generiert) und Sie die integrierte Produktprogrammplanungs-Engine über Version 10.0.15 hinaus benötigen. Ab Version 10.0.16 wird in Umgebungen ein Fehler angezeigt, wenn die integrierte Produktprogrammplanung ausgeführt wird, ohne dass geplante Produktionsaufträge generiert werden. Die Planungsoptimierung sollte für alle neuen Bereitstellungen verwendet werden, die während der Produktprogrammplanung keine geplanten Produktionsaufträge generieren. Besitzer vorhandener Umgebungen, in denen die integrierte Produktprogrammplanungs-Engine ohne Generierung geplanter Produktionsaufträge ausgeführt wird, erhalten eine E-Mail mit Details zum Ausnahmevorgang. Wir empfehlen, dass Sie mit einem Partner zusammenarbeiten, um die Migration zur Planungsoptimierung zu bewerten und zu planen.

Bevor Sie die Planungsoptimierung einschalten, empfehlen wir Ihnen dringend, die Ergebnisse der Anpassungsanalyse der Planungsoptimierung auszuwerten. Weitere Informationen finden Sie unter [Planungsoptimierung Fit-Analyse](planning-optimization-fit-analysis.md).

## <a name="availability"></a>Verfügbarkeit

Die Planungsoptimierung ist derzeit in den folgenden geografischen Azure-Regionen verfügbar: Vereinigte Staaten, Kanada, Brasilien, Europa, Vereinigtes Königreich, Australien, Asien-Pazifik, Japan und Indien. Wenn Sie versuchen, das Add-In aus einer anderen geografischen Region zu installieren, zeigt LCS die Meldung an, dass diese geografische Region nicht unterstützt wird. Weitere Informationen zu Azure-Geografien und den zugehörigen Regionen finden Sie unter [Azure-Geografien](https://azure.microsoft.com/global-infrastructure/geographies/#geographies).

Beachten Sie, dass Planungsoptimierung keine lokalen Bereitstellungen von Dynamics 365 Supply Chain Management unterstützt.

## <a name="licensing"></a>Lizenzierung

Wenn Sie die Masterplanung mit Ihrer aktuellen Lizenz durchführen können, müssen Sie keine zusätzliche Lizenz kaufen, um mit der Planungsoptimierung zu beginnen.

## <a name="install-and-enable-planning-optimization"></a>Planungsoptimierung installieren und aktivieren

Um die Planungsoptimierung verwenden zu können, müssen Sie sicherstellen, dass auf Ihrem System alle Voraussetzungen vorhanden sind, den Lizenzschlüssel aktivieren und das Planungsoptimierungs-Add-In für Dynamics 365 Supply Chain Management installieren.

### <a name="prerequisites"></a>Voraussetzungen

Bevor Sie die das Planungsoptimierungs-Add-In installieren, müssen die folgenden Voraussetzungen erfüllt sein:

- Sie müssen Supply Chain Management in einer LCS-fähigen Hochverfügbarkeitsumgebung, Ebene 2 oder höher (keine OneBox-Umgebung) mit Dynamics 365 Supply Chain Management Version 10.0.7 oder höher ausführen. Wenn Sie versuchen, das Add-In in einer OneBox-Umgebung zu installieren, wird die Installation nicht abgeschlossen und Sie müssen die Installation abbrechen.

- Ihr System muss für die Power Platform-Integration eingerichtet sein. Weitere Informationen finden Sie unter [Microsoft Power Platform Integration mit Finance und Operations Apps](../../../fin-ops-core/dev-itpro/power-platform/overview.md).

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
| Verbindung getrennt | Es besteht keine Verbindung zum Service Planungsoptimierung. Die Verbindung kann vom LCS aus eingeschaltet werden, wie bereits in diesem Thema beschrieben. | Nein |
| Verbindung wird deaktiviert | Eine Aufforderung zum Deaktivieren der Verbindung zum Dienst Planungsoptimierung ist derzeit in Bearbeitung. | Nein |
| Status wird abgerufen... | Das System wartet auf Statusinformationen vom Service Planungsoptimierung. | Nein |

### <a name="the-use-planning-optimization-option"></a>Die Option Planungsoptimierung verwenden

Die Einstellung der Option **Verwendungsplanoptimierung** bestimmt, welche Planungs-Engine für die Masterplanung verwendet wird:

- **Ja** - Die Planungsoptimierung wird für die Masterplanung verwendet.
- **Nein** - Die eingebaute Supply Chain Management Planning Engine wird für die Masterplanung verwendet.

Diese Einstellung gilt für alle juristischen Entitäten (Firmen). Es ist nicht möglich, die Planungsoptimierung in einigen juristischen Entitäten und die integrierte Masterplanung in anderen juristischen Entitäten zu verwenden.

> [!NOTE]
> Wenn bestehende Planungs-Batchjobs, die für die eingebaute Supply Chain Management Planungs-Engine erstellt wurden, ausgelöst werden, während die Option **Verwendungsplanoptimierung** auf **Ja** gesetzt ist, werden diese Jobs fehlschlagen.

### <a name="integration-with-the-setup"></a>Integration mit dem Setup

Wenn die Planungsoptimierung eingeschaltet ist, wird die Produktprogrammplanung mit dem Planungsoptimierungs-Add-In durchgeführt. In diesem Fall sind die Ergebnisse und Merkmale der Masterplanung betroffen.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Allgemeine Geschäftsbedingungen für die Vorschau](https://go.microsoft.com/fwlink/?linkid=2015274)

[Übersicht zur Planungsoptimierung](planning-optimization-overview.md)

[Planungsoptimierung Fit-Analyse](planning-optimization-fit-analysis.md)

[Planhistorie und Planungsprotokolle anzeigen](plan-history-logs.md)

[Filter auf einen Plan anwenden](plan-filters.md)

[Abbrechen eines Planungsauftrags](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
