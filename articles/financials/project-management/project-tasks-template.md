---
title: Synchronisieren Sie Projektaufgaben aus der der Project Service Automation
description: "Dieses Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Produkte direkt aus Microsoft Dynamics 365 for Project Service Automation in Dynamics 365 for Finance and Operations zu synchronisieren."
author: KimANelson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: 399b519ab0da4de405aeb06f3e7f4bf29a6c5cc3
ms.openlocfilehash: 89df0d99d780441ad08cd6bff3e1fd203694eb8e
ms.contentlocale: de-de
ms.lasthandoff: 05/30/2018

---

# <a name="synchronize-project-tasks-from-project-service-automation-directly-to-project-activities-in-finance-and-operations"></a>Synchronisieren Sie Projektaufgaben von der Project Service Automation direkt in Projektaktivitäten von Finance and Operations

Dieses Thema erläutert die Vorlagen und die zugrunde liegenden Aufgaben, die verwendet werden, um Produkte direkt aus Microsoft Dynamics 365 for Project Service Automation in Dynamics 365 for Finance and Operations zu synchronisieren.

> [!NOTE]
> Projektaufgaben-Integration, Ausgabenbuchungskategorien, StundensDynamics 365 for Finance and Operations version 8.0.chätzungen, Ausgabenenschätzungen und Funktionenssperre sind in Dynamics 365 for Finance and Operations Version 8.0 verfügbar.

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Datenfluss für Project Service Automation zu Finance and Operations

Die Project Service Automation zu Finance and Operations Integrationslösung nutzt die  Datenenintegrationsfunktion, um Daten in Instanzen von Project Service Automation und Finance and Operations zu synchronisieren. Die Integrationsvorlage, die der Datenenintegrationsfunktion verfügbar ist, ermöglicht den Datenfluss zu Projektaufgaben von Project Service Automation zu Finance and Operations.

Die folgende Abbildung zeigt, wie Daten als Teil der Integration zwischen Project Service Automation und Finance and Operations synchronisiert werden.

[![Datenfluss für Project Service Automation Integration mit Finance and Operations](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>Vorlage und Aufgabe

Wenn Sie auf die Vorlage im Microsoft PowerApps Admin Center zugreifen möchten, wählen Sie **Projekte**, und klicken Sie dann in der oberen rechten Ecke auf **Neues Projekt**, um die öffentliche Vorlage auszuwählen.

Die folgenden Vorlagen und zugrunde liegenden Aufgaben werden verwendet, um Projektaufgaben von Project Service Automation zu Finance and Operations zu synchronisieren:

-**Bezeichnung der Vorlage in der Datenintegration:** Projektaufgabe (PSA zu Fin and Ops) - **Name der Aufgabe im Projekt** Projektaufgaben

Vor der Synchronisierung von Projektaufgaben müssen Sie zunächst Projektverträge und Projekte synchronisieren.

## <a name="entity-set"></a>Entitätssatz

|Project Service Automation               | Finance and Operations                |
|-----------------------------------------|---------------------------------------|
| Projekt-Aufgaben                           | Integrationsentität für Projektaufgabe.   |

## <a name="entity-flow"></a>Entitätsfluss

Projektaufgaben werden in der Project Service Automation verwaltet und nach Finance and Operations als Projektaktivitäten verwaltet.

## <a name="prerequisites-and-mapping-setup"></a>Voraussetzungen und Zuordnungseinrichtung

Vor der Synchronisierung von Projektaufgaben müssen Sie zunächst Projektverträge und Projekte synchronisieren.

## <a name="power-query"></a>Powerabfrage

Sie müssen Microsoft Power Abfrage verwenden, um Daten zu filtern, wenn die Bedingungen erfüllt sind:

- Sie haben Ressourcen spezifische Datensätze innerhalb der Projektaufgabe.

Wenn Sie Power Query verwenden möchten, folgen Sie diesen Richtlinien:

- Die Projektaufgaben der Vorlage (PSA zu Fin and Opss) weist einen der Standardfilter auf, um bestimmte Datensätze der Ressource aus einer Projektaufgabe auszuschließen mithilfe des Filters im **IsLineTask** auf **Falsch**. Wenn Sie Ihre eigenen Vorlagen erstellen, müssen Sie diese dem Filter hinzufügen.

## <a name="template-mapping-in-data-integration"></a>Vorlagenzuordnung in Datenintegration

Die folgenden Abbildungen zeigen ein Beispiel für eine Vorlagenaufgabenzuordnung im Datenintegrator. Die Zuordnung zeigt, welche Feldinformationen von Project Service Automation zu Finance and Operations synchronisiert werden.

[![Vorlagenzuordnung](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)


