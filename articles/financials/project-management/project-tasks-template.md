---
title: Synchronisieren von Projektaufgaben direkt aus Project Service Automation mit Finance and Operations
description: Dieses Thema beschreibt die Vorlage und die zugrunde liegende Aufgaben, die verwendet wird, um die Projektaufgaben direkt aus Microsoft Dynamics 365 for Project Service Automation mit Microsoft Dynamics 365 for Finance and Operations zu synchronisieren.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 53e4eab0d455af4ac1e17754f31d46458db742c3
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "355172"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a>Synchronisieren von Projektaufgaben direkt aus Project Service Automation mit Finance and Operations

[!include[banner](../includes/banner.md)]

Dieses Thema beschreibt die Vorlage und die zugrunde liegende Aufgaben, die verwendet wird, um die Projektaufgaben direkt aus Microsoft Dynamics 365 for Project Service Automation mit Microsoft Dynamics 365 for Finance and Operations zu synchronisieren.

> [!NOTE]
> - Projektaufgaben-Integration, Ausgabenbuchungskategorien, Stundenschätzungen, Ausgabenenschätzungen und Funktionenssperre sind in Microsoft Dynamics 365 for Finance and Operations, Version 8.0 verfügbar.
> - Wenn Sie Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0 verwenden und KB 4132657 und 4132660 KB einrichten, sind Sie in der Lage, die Vorlagen zu verwenden, um Projektaufgaben, Ausgabentransaktionskategorien, geschätzte Stunden, geschätzte Ausgaben und aktuelle Kosten zu integrieren und die Funktionalitätssperre zu konfigurieren. Wenn Sie die Buchhaltungsverteilungen zurücksetzen müssen, wird empfohlen, dass Sie auch KB 4131710 installieren.
> - Integration von Ist-Werten ist in Microsoft Dynamics 365 for Finance and Operations, Version 8.0.1 oder höher verfügbar.

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Datenfluss für Project Service Automation zu Finance and Operations

Die Project Service Automation zu Finance and Operations Integrationslösung nutzt die Datenenintegrationsfunktion, um Daten in Instanzen von Project Service Automation und Finance and Operations zu synchronisieren. Die Integrationsvorlage, die der Datenenintegrationsfunktion verfügbar ist, ermöglicht den Datenfluss zu Projektaufgaben von Project Service Automation zu Finance and Operations.

Die folgende Abbildung zeigt, wie Daten als Teil der Integration zwischen Project Service Automation und Finance and Operations synchronisiert werden.

[![Datenfluss für Project Service Automation Integration mit Finance and Operations](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>Vorlage und Aufgabe

Wenn Sie auf die Vorlage im Microsoft PowerApps-Admin Center zugreifen möchten, wählen Sie **Projekte**, und klicken Sie dann in der oberen rechten Ecke auf **Neues Projekt**, um die öffentliche Vorlage auszuwählen.

Die folgende Vorlage und zugrunde liegende Aufgabe werden verwendet, um Projektaufgaben von Project Service Automation mit Finance and Operations zu synchronisieren:

- **Name der Vorlage in der Datenintegration:** Projektaufgaben (PSA zu Fin und Ops)
- **Name der Aufgabe im Projekt:** Projektaufgaben

Vor der Synchronisierung von Projektaufgaben müssen Sie zunächst Projektverträge und Projekte synchronisieren.

## <a name="entity-set"></a>Entitätssatz

| Project Service Automation | Finance and Operations              |
|----------------------------|-------------------------------------|
| Projekt-Aufgaben              | Integrationsentität für Projektaufgabe |

## <a name="entity-flow"></a>Entitätsfluss

Projektaufgaben werden in der Project Service Automation verwaltet und nach Finance and Operations als Projektaktivitäten verwaltet.

## <a name="prerequisites-and-mapping-setup"></a>Voraussetzungen und Zuordnungseinrichtung

Vor der Synchronisierung von Projektaufgaben müssen Sie zunächst Projektverträge und Projekte synchronisieren.

## <a name="power-query"></a>Powerabfrage

Sie müssen Microsoft Power Query für Excel verwenden, um Daten zu filtern, wenn diese Bedingung erfüllt ist:

- Sie haben ressourcenspezifische Datensätze in einer Projektaufgabe.

Wenn Sie Power Query verwenden müssen, folgen Sie dieser Richtlinie:

- Die Projektaufgabenvorlage (PSA zu Fin and Opss) weist einen Standardfilter auf, der ressourcenspezifisce Datensätze aus einer Projektaufgabe ausschließt, indem der Filter in **IsLineTask** auf **Falsch** festgelegt wird. Wenn Sie Ihre eigenen Vorlagen erstellen, müssen Sie diese dem Filter hinzufügen.

## <a name="template-mapping-in-data-integration"></a>Vorlagenzuordnung in Datenintegration

Die folgenden Abbildungen zeigen ein Beispiel für eine Vorlagenaufgabenzuordnung im Datenintegrator. Die Zuordnung zeigt, welche Feldinformationen von Project Service Automation zu Finance and Operations synchronisiert werden.

[![Vorlagenzuordnung](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)
