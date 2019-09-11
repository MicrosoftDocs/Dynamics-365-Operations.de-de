---
title: Project Service Automation Übersicht
description: Dieses Thema enthält Informationen über die Project Service Automation-zu-Finance and Operations-Integrationslösung. Diese Integrationslösung nutzt die Datenintegrationsfunktion, um Daten über Instanzen von Microsoft Dynamics 365 for Finance and Operations und Microsoft Dynamics 365 for Project Service Automation über Common Data Service zu synchronisieren.
author: KimANelson
manager: AnnBe
ms.date: 07/25/2019
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
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 85dde35033122ad234ec8efd1bddf64b950578ef
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2019
ms.locfileid: "1865627"
---
# <a name="project-service-automation-overview"></a>Project Service Automation Übersicht

[!include[banner](../includes/banner.md)]

Die Integrationslösung Project Service Automation to Finance and Operations nutzt die Datenintegrationsfunktion, um Daten über Instanzen von Microsoft Dynamics 365 for Finance and Operations und Microsoft Dynamics 365 for Project Service Automation über Common Data Service zu synchronisieren. Die Integrationsvorlagen, die mit der Datenintegrationsfunktion verfügbar sind, ermöglichen den Fluss von Projekten, Projektverträgen, Projektvertragspositionen, Projektvertragspositions-Meilensteinen, Projektaufgaben, Ausgabenbuchungskategorien, Stundenvorkalkulationen und Ausgabenvorkalkulationen von Project Service Automation zu Finance and Operations.

> [!NOTE]
> - Wenn Sie Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0 verwenden und KB 4132657 und 4132660 KB einrichten, sind Sie in der Lage, die Vorlagen zu verwenden, um Projektaufgaben, Ausgabentransaktionskategorien, geschätzte Stunden, geschätzte Ausgaben und aktuelle Kosten zu integrieren und die Funktionalitätssperre zu konfigurieren. Wenn Sie die Buchhaltungsverteilungen zurücksetzen müssen, wird empfohlen, dass Sie auch 4131710 KB einrichten.
> - Wenn Sie Finance and Operations 7.3.0 verwenden, müssen Sie KB 4074835 installieren. Dadurch wird es Ihnen dann ermöglicht, Festpreisprojekte zu integrieren.
> - Wenn Sie Finance and Operations 7.3.0 verwenden und Gebührenbuchungen aus Project Service Automation übernehmen, müssen Sie KB 4345320 installieren, um diese Gebühren in der Projektrechnung einzuschließen.
> - Wenn Sie Microsoft Dynamics 365 for Finance and Operations Version 8.0 verwenden, sind Sie in der Lage, Projektaufgaben-Integration, Ausgabenbuchungskategorien, Stundenschätzungen, Ausgabenenschätzungen und Funktionenssperre zu verwenden.
> - Wenn Sie Microsoft Dynamics 365 for Finance and Operations Version 8.0.1 oder höher verwenden, sind Sie in der Lage, Ist-Werte zu synchronisieren.

Bevor Sie Project Service Automation mit Finance and Operations integrieren können, müssen Sie auch die Project Service Automation mit Finance and Operations integrieren. Weitere Informationen finden Sie unter [Project Service Automation-Integrationsparameter](PSA-parameters.md).

Diese Integrationslösung bietet direkte Synchronisation in den folgenden Szenarien:

- Verwalten Sie Projektverträge in der Project Service Automation und synchronisieren Sie direkt von der Project Service Automation zu Finance Finanzen und Arbeitsgänge.
- Erstellen Sie Projektverträge in der Project Service Automation und synchronisieren Sie direkt von der Project Service Automation zu Finance
- Verwalten Sie Projektvertragszeilen in der Project Service Automation und synchronisieren Sie direkt von der Project Service Automation zu Finance and Operations.
- Verwalten Sie Projektvertragszeiln-Meilensteine in der Project Service Automation und synchronisieren Sie direkt von der Project Service Automation zu Finance and Operations.
- Verwalten Sie Projektaufgaben in der Project Service Automation und synchronisieren Sie direkt von der Project Service Automation zu Finance Finanzen und Arbeitsgänge.
- Verwalten Sie Ausgabentransaktionskategorien in Finance and Operations und synchronisieren Sie direkt von Finance and Operations zu Project Service Automation.
- Erstellen Sie Projektstundenschätzungen in der Project Service Automation und synchronisieren Sie direkt von der Project Service Automation zu Finance and Operations.
- Erstellen Sie Projektausgabenschätzungen in der Project Service Automation und synchronisieren Sie direkt von der Project Service Automation zu Finance and Operations.
- Erstellen Sie Projektzeit, Ausgaben und Gebühren-Ist-Werte in Project Service Automation und erstellen Sie Projekttransaktionen in der Project Service Automation-Integrationserfassung, damit sie in Finance and Operations gebucht werden können.

## <a name="data-synchronization"></a>Datensynchronisierung

Die folgende Abbildung zeigt, wie Daten als Teil der Integration zwischen Project Service Automation und Finance and Operations synchronisiert werden.

> [!NOTE]
> Nicht alle Vorlagen sind derzeit verfügbar. Vorlagen werden freigegeben, wenn diese abgeschlossen werden.

[![Project Service Automation Integration mit Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance-and-operations"></a>Systemanforderungen für Finance and Operations

Um die Project Service Automation zu Finance and Operations Integrationslösung zu verwenden, müssen Sie Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3 mit Plattformaktualisierung 12 oder höher einrichten.

## <a name="system-requirements-for-project-service-automation"></a>Systemanforderungen für Project Service Automation

Um die Project Service Automation zu Finance and Operations-Integrationslösung zu verwenden, müssen Sie die folgenden Komponenten installieren:

- Microsoft Dynamics 365 for Project Service Automation Version 9.0.0.0 oder höher
- Prospect to Cash-Lösung für Microsoft Dynamics 365 for Sales, Version 1.14.0.0 (v14) oder höher.
- Project Service Automation to Finance and Operations Integrationslösung für Microsoft Dynamics 365 for Project Service Automation Version1.0.0.0 oder höher

## <a name="install-the-project-service-automation-to-finance-and-operations-integration-solution-in-your-project-service-automation-instance"></a>Installieren Sie die Project Service Automation to Finance and Operations Integrationslösung in Project Service Automation Instanz

Laden Sie die Project Service Automation-zu-Finance and Operations-Integrationslösung von [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016) herunter, und befolgen Sie die Anweisungen, die in der Lösung enthalten sind.
