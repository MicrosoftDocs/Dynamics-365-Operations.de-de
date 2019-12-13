---
title: Synchronisieren von Projektaufgaben direkt aus Project Service Automation mit Finance and Operations
description: Dieses Thema beschreibt die Vorlage und die zugrunde liegende Aufgaben, die verwendet wird, um die Projektaufgaben direkt aus Microsoft Dynamics 365 Project Service Automation mit Dynamics 365 Finance zu synchronisieren.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: ba475721b69e7c75dfd2197597b54050a3598d37
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770265"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a>Synchronisieren von Projektaufgaben direkt aus Project Service Automation mit Finance and Operations

[!include[banner](../includes/banner.md)]

Dieses Thema beschreibt die Vorlage und die zugrunde liegende Aufgaben, die verwendet wird, um die Projektaufgaben direkt aus Dynamics 365 Project Service Automation mit Dynamics 365 Finance zu synchronisieren.

> [!NOTE]
> - Projektaufgaben-Integration, Ausgabenbuchungskategorien, Stundenschätzungen, Ausgabenenschätzungen und Funktionenssperre sind in Version 8.0 verfügbar.
> - Wenn Sie Enterprise Edition 7.3.0 verwenden und KB 4132657 und 4132660 KB einrichten, sind Sie in der Lage, die Vorlagen zu verwenden, um Projektaufgaben, Ausgabentransaktionskategorien, geschätzte Stunden, geschätzte Ausgaben und aktuelle Kosten zu integrieren und die Funktionalitätssperre zu konfigurieren. Wenn Sie die Buchhaltungsverteilungen zurücksetzen müssen, wird empfohlen, dass Sie auch KB 4131710 installieren.
> - Integration von Ist-Werten ist in Version 8.0.1 oder höher verfügbar.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Datenfluss für Project Service Automation zu Finance

Die Project Service Automation nach Finance-Integrationslösung nutzen die Datenenintegrationsfunktion, um Daten in Instanzen von Project Service Automation und Finance zu synchronisieren. Die Integrationsvorlage, die der Datenenintegrationsfunktion verfügbar ist, ermöglicht den Datenfluss zu Projektaufgaben von Project Service Automation zu Finance.

Die folgende Abbildung zeigt, wie Daten als Teil der Integration zwischen Project Service Automation und Finance synchronisiert werden.

[![Datenfluss für Project Service Automation Integration mit Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>Vorlage und Aufgabe

Wenn Sie auf die Vorlage im Microsoft Power Apps-Admin Center zugreifen möchten, wählen Sie **Projekte**, und klicken Sie dann in der oberen rechten Ecke auf **Neues Projekt**, um die öffentliche Vorlage auszuwählen.

Die folgende Vorlage und zugrunde liegende Aufgabe werden verwendet, um Projektaufgaben von Project Service Automation mit Finance zu synchronisieren:

- **Name der Vorlage in der Datenintegration:** Projektaufgaben (PSA zu Fin und Ops)
- **Name der Aufgabe im Projekt:** Projektaufgaben

Vor der Synchronisierung von Projektaufgaben müssen Sie zunächst Projektverträge und Projekte synchronisieren.

## <a name="entity-set"></a>Entitätssatz

| Project Service Automation | Finanzen                             |
|----------------------------|-------------------------------------|
| Projekt-Aufgaben              | Integrationsentität für Projektaufgabe |

## <a name="entity-flow"></a>Entitätsfluss

Projektaufgaben werden in der Project Service Automation verwaltet und nach Finance als Projektaktivitäten verwaltet.

## <a name="prerequisites-and-mapping-setup"></a>Voraussetzungen und Zuordnungseinrichtung

Vor der Synchronisierung von Projektaufgaben müssen Sie zunächst Projektverträge und Projekte synchronisieren.

## <a name="power-query"></a>Powerabfrage

Sie müssen Microsoft Power Query für Excel verwenden, um Daten zu filtern, wenn diese Bedingung erfüllt ist:

- Sie haben ressourcenspezifische Datensätze in einer Projektaufgabe.

Wenn Sie Power Query verwenden müssen, folgen Sie dieser Richtlinie:

- Die Projektaufgabenvorlage (PSA zu Fin and Opss) weist einen Standardfilter auf, der ressourcenspezifisce Datensätze aus einer Projektaufgabe ausschließt, indem der Filter in **IsLineTask** auf **Falsch** festgelegt wird. Wenn Sie Ihre eigenen Vorlagen erstellen, müssen Sie diese dem Filter hinzufügen.

## <a name="template-mapping-in-data-integration"></a>Vorlagenzuordnung in Datenintegration

Die folgenden Abbildungen zeigen ein Beispiel für eine Vorlagenaufgabenzuordnung im Datenintegrator. Die Zuordnung zeigt, welche Feldinformationen von Project Service Automation zu Finance synchronisiert werden.

[![Vorlagenzuordnung](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)
