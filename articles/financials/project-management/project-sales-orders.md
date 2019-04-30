---
title: Projektaufträge
description: In diesem Thema wird erläutert, wie Projekt basierte Auträge für Zeit- und Materialprojekte erstellt werden.
author: KimANelson
manager: AnnBe
ms.date: 04/05/2019
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
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 1d54c98a08dc7cccb5cafbbe401d0ce25a276c25
ms.sourcegitcommit: 9796d022a8abf5c07abcdee6852ee34f06d2eb57
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/12/2019
ms.locfileid: "976660"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a>Projekt-Aufträge für Zeit- und Materialprojekte

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

In diesem Thema wird beschrieben, wie ein Auftrag für ein Projekt erstellt wird. Aufträge können ausschließlich für Projekte vom Typ **Zeit oder 'Material** erstellt werden.

Wenn ein Zeit- und Materialprojekt mehrere Finanzierungsquellen im Projektvertrag hat, müssen Sie die Parameter **Aufträge für Projekte mit mehreren Finanzierungsquellen zulassen** auf der Seite **Projektmanagement und Buchhaltungsparameter** aktivieren. 

> [!NOTE]
> - Unterstützung für Projektaufträge mit mehreren Finanzierungsquellen ist verfügbar beginnend mit Anwendung 10.0.2 und höher.
> - Der Parameter, um den Support für Projektaufträge mit mehreren Finanzierungsquellen zu aktivieren wird in der im April 2020 geplanten Aktualisierung entfernt und die Funktion wird danach immer aktiviert sein.

Sie können Projekt basierte Aufträge auf zwei Arten erstellen:

- Gehen Sie zum Projekt selber. Klicken Sie im Aktivitätsbereich auf **Verwalten > Artikelaufgaben > Auftrag**. Die Projektinformationen werden standardmäßig dem Auftrag aus dem Projekt hinzugefügt. Hat der Projektvertrag mehrere Finanzierungsquellen, müssen Sie die Finanzierungsquelle auswählen, um den Debitor für den Auftrag festzulegen. Wenn es nur eine Finanzierungsquelle für das Projekt gibt, wird der Debitor automatisch festgelegt.
- Gehen Sie zur Listenseite **alle Aufträge** und erstellen Sie einen neuen Auftrag. Sie müssen das Projekt für den Auftrag auswählen. Nachdem das Projekt ausgewählt ist, wird der Debitor von der Finanzierungsquelle festgelegt, oder Sie müssen die Finanzierungsquelle auswählen, wenn der Projektvertrag mehrere Finanzierungsquellen aufweist.

