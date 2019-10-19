---
title: Project Service Automation – Übersicht
description: Dieses Thema bietet Informationen über die Integrationslösung Dynamics 365 Project Service Automation zu Dynamics 365 Finance.
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
ms.openlocfilehash: 31d72591041f8d8cc327aa7c6578c15731ba13c5
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250552"
---
# <a name="project-service-automation-overview"></a>Project Service Automation – Übersicht

[!include[banner](../includes/banner.md)]

Die Integrationslösung Project Service Automation to Finance nutzt die Datenintegrationsfunktion, um Daten über Instanzen von Dynamics 365 Finance und Dynamics 365 Project Service Automation über Common Data Service zu synchronisieren. Die Integrationsvorlagen, die mit der Datenintegrationsfunktion verfügbar sind, ermöglichen den Fluss von Projekten, Projektverträgen, Projektvertragspositionen, Projektvertragspositions-Meilensteinen, Projektaufgaben, Ausgabenbuchungskategorien, Stundenvorkalkulationen und Ausgabenvorkalkulationen von Project Service Automation zu Finance.

> [!NOTE]
> - Wenn Sie Version7.3.0 verwenden, müssen Sie KB 4074835 installieren. Dadurch wird es Ihnen dann ermöglicht, Festpreisprojekte zu integrieren.
> - Wenn Sie Version 7.3.0 verwenden und Gebührenbuchungen aus Project Service Automation übernehmen, müssen Sie KB 4345320 installieren, um diese Gebühren in der Projektrechnung einzuschließen.
> - Wenn Sie Version 8.0 verwenden, sind Sie in der Lage, Projektaufgaben-Integration, Ausgabenbuchungskategorien, Stundenschätzungen, Ausgabenenschätzungen und Funktionenssperre zu verwenden.
> - Wenn Sie Version 8.0.1 oder höher verwenden, sind Sie in der Lage, Ist-Werte zu synchronisieren.

Bevor Sie Project Service Automation Finance integrieren können, müssen Sie auch die Project Service Automation mit Finance and Operations integrieren. Weitere Informationen finden Sie unter [Project Service Automation-Integrationsparameter](PSA-parameters.md).

Diese Integrationslösung bietet direkte Synchronisation in den folgenden Szenarien:

- Verwalten Sie Projektverträge in der Project Service Automation und synchronisieren Sie direkt von der Project Service Automation zu Finance.
- Erstellen Sie Projektverträge in der Project Service Automation und synchronisieren Sie direkt von der Project Service Automation zu Finance
- Verwalten Sie Projektvertragspositionen in der Project Service Automation und synchronisieren Sie direkt von der Project Service Automation zu Finance.
- Verwalten Sie Projektvertragspositionsmeilensteine in der Project Service Automation und synchronisieren Sie direkt von der Project Service Automation zu Finance.
- Verwalten Sie Projektaufträge in der Project Service Automation und synchronisieren Sie direkt von der Project Service Automation zu Finance.
- Verwalten Sie Ausgabentransaktionskategorien in Finance und synchronisieren Sie direkt von Finance zu Project Service Automation.
- Erstellen Sie Projektstundenschätzungen in der Project Service Automation und synchronisieren Sie direkt von der Project Service Automation zu Finance.
- Erstellen Sie Projektausgabenschätzungen in der Project Service Automation und synchronisieren Sie direkt von der Project Service Automation zu Finance.
- Erstellen Sie Projektzeit, Ausgaben und Gebühren-Ist-Werte in Project Service Automation und erstellen Sie Projekttransaktionen in der Project Service Automation-Integrationserfassung, damit sie in Finance gebucht werden können.

## <a name="data-synchronization"></a>Datensynchronisierung

Die folgende Abbildung zeigt, wie Daten als Teil der Integration zwischen Project Service Automation und Finance synchronisiert werden.

> [!NOTE]
> Nicht alle Vorlagen sind derzeit verfügbar. Vorlagen werden freigegeben, wenn diese abgeschlossen werden.

[![Project Service Automation-Integration in Finance](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance"></a>Systemanforderungen für Finance

Um die Project Service Automation zu Finance Integrationslösung zu verwenden, müssen Sie , Enterprise Edition 7.3 mit Plattformaktualisierung 12 oder höher einrichten.

## <a name="system-requirements-for-project-service-automation"></a>Systemanforderungen für Project Service Automation

Um die Project Service Automation zu Finance-Integrationslösung zu verwenden, müssen Sie die folgenden Komponenten installieren:

- Dynamics 365 Project Service Automation Version 9.0.0.0 oder höher
- Interessent zu Bargeld-Lösung für Dynamics 365 Sales, Version 1.14.0.0 (v14) oder höher.
- Project Service Automation zu Finance-Integrationslösung für Dynamics 365 Project Service Automation Version1.0.0.0 oder höher

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a>Installieren Sie die Project Service Automation zu Finance Integrationslösung in Project Service Automation Instanz

Laden Sie die Project Service Automation-zu-Finance-Integrationslösung von [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016) herunter, und befolgen Sie die Anweisungen, die in der Lösung enthalten sind.
