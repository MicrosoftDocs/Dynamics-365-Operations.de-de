---
title: Project Service Automation
description: "Diese Lösung verwendet Datenintegration, um Daten über Instanzen von Microsoft Dynamics 365 for Finance and Operations und Microsoft Dynamics 365 for Project Service Automation über Common Data Service (CDC) zu synchronisieren."
author: KimANelson
manager: AnnBe
ms.date: 11/27/2017
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 0ad9e6ba7fe8dd915681da8e671ff210de887b1e
ms.contentlocale: de-de
ms.lasthandoff: 05/29/2018

---

# <a name="project-service-automation"></a>Project Service Automation

Die Project Service Automation zur Finance and Operations Integrationslösung nutzt die Datenintegrationsfunktion, um Daten über Instanzen von Microsoft Dynamics 365 for Finance and Operations und Microsoft Dynamics 365 for Project Service Automation über Common Data Service (CDC) zu synchronisieren. Die Integrationsvorlagen, die in der Daten-Integrationsfunktion verfügbar sind, aktivieren den Fluss von Projekten, von Projektverträgen, Projektvertragspositionen, Projektvertragszeilen-Meilensteinen,  Projektaufgaben, Ausgabenbuchungskategorien, Stundenschätzungen und von Ausgabenschätzungen von Project Service Automation zu Finance and Operations.

> [!NOTE] 
> Wenn Sie Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3.0 verwenden, müssen Sie auch KB 4074835 installieren. Dadurch wird es Ihnen ermöglicht, Festpreisprojekte zu integrieren.
>
> Wenn Sie Dynamics 365 for Finance and Operations 8,0 verwenden, sind Sie in der Lage, Projektaufgaben-Integration, Ausgabenbuchungskategorien, Stundenschätzungen, Ausgabenenschätzungen und Funktionenssperre zu verwenden.
>
> Wenn Sie Dynamics 365 for Finance and Operations 8.0.1 verwenden, sind Sie in der Lage, aktuelle Verhältnisse zu synchronisieren.
>
> Wenn Sie Dynamics 365  for Finance and Operations, Enterprise edition 7.3.0,verwenden und KB 4132657 und 4132660 KB einrichten, sind Sie in der Lage, die Vorlagen zu verwenden, um Projektaufgaben,  Ausgabentransaktionskategorien, geschätzte Stunden, geschätzte Ausgaben und aktuelle Kosten zu integrieren und die Funktionalitätssperre zu konfigurieren. Wenn Sie die Buchhaltungsverteilungen zurücksetzen müssen, wird empfohlen, dass Sie auch 4131710 KB einrichten.

Bevor Sie Project Service Automation mit Finance and Operations integrieren können, müssen Sie auch die Project Service Automation mit Finance and Operations integrieren. Weitere Informationen finden Sie unter Project Service Automation Integrationsparameter.

Diese Integrationslösung bietet direkte Synchronisation in den folgenden Szenarien:

- Verwalten Sie Projektverträge in der Project Service Automation und synchronisieren Sie direkt von der Project Service Automation zu Finance Finanzen und Arbeitsgänge.
- Erstellen Sie Projektverträge in der Project Service Automation und synchronisieren Sie direkt von der Project Service Automation zu Finance
- Verwalten Sie Projektvertragszeilen in der Project Service Automation und synchronisieren Sie direkt von der Project Service Automation zu Finance and Operations.
- Verwalten Sie Projektvertragszeiln-Meilensteine in der Project Service Automation und synchronisieren Sie direkt von der Project Service Automation zu Finance and Operations.
- Verwalten Sie Projektaufgaben in der Project Service Automation und synchronisieren Sie direkt von der Project Service Automation zu Finance Finanzen und Arbeitsgänge.
- Verwalten Sie Ausgabentransaktionskategorien in Finance and Operations und synchronisieren Sie direkt von Finance and Operations zu Project Service Automation.
- Erstellen Sie Projektstundenschätzungen in der Project Service Automation und synchronisieren Sie direkt von der Project Service Automation zu Finance and Operations.
- Erstellen Sie Projektausgabenschätzungen in der Project Service Automation und synchronisieren Sie direkt von der Project Service Automation zu Finance and Operations.

## <a name="data-synchronization"></a>Datensynchronisierung
Die folgende Abbildung zeigt, wie Daten als Teil der Integration zwischen Project Service Automation und Finance and Operations synchronisiert werden.

> [!NOTE]
> Nicht alle Vorlagen sind derzeit verfügbar. Vorlagen werden freigegeben, wenn diese abgeschlossen werden.

[![Project Service Automation Integration mit Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance-and-operations"></a>Systemanforderungen für Finance and Operations

Um die Project Service Automation zu Finance and Operations Integrationslösung zu verwenden, müssen Sie Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition mit 7.3 Plattformaktualisierung 12 oder später einrichten.

## <a name="system-requirements-for-project-service-automation"></a>Systemanforderungen für Project Service Automation

Um die Project Service Automation zu Finance and Operations-Integrationslösung zu verwenden, müssen Sie die folgenden Komponenten installieren:

- Microsoft Dynamics 365 for Project Service Automation Version 9.0.0.0 oder höher.
- Interessent zu Bargeld-Lösung für Dynamics 365 for Sales, Version 1.14.0.0 (v14) oder höher.
- roject Service Automation to Operations-Lösung für Dynamics 365 for Project Service Automation Version 1.0.0.0 oder höher.

## <a name="install-the-project-service-automation-to-finance-and-operations-integration-solution-in-your-project-service-automation-instance"></a>Installieren Sie die Project Service Automation to Finance and Operations Integrationslösung in Project Service Automation Instanz



