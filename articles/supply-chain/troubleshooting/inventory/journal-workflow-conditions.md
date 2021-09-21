---
title: Die Bedingungen für den Bestandserfassungs-Workflow gelten auf Erfassungsebene, nicht auf Positionsebene.
description: Die Workflowbedingungen für Bestandserfassungen gelten nur auf Erfassungsebene, nicht auf Positionsebene.
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 46bdde7f09c639fbefd46162431762b056d521ae
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476443"
---
# <a name="inventory-journal-workflow-conditions-apply-at-the-journal-level-not-line-level"></a>Die Bedingungen für den Bestandserfassungs-Workflow gelten auf Erfassungsebene, nicht auf Positionsebene.

## <a name="symptoms"></a>Symptome

Dieses Problem kann auftreten, wenn Sie beispielsweise versuchen, eine Workflowbedingung für die Bestandserfassung für den Kostenbetrag einzurichten. Sie richten die Bedingung so ein, dass Schritt 1 nur ausgeführt wird, wenn der Kostenbetrag kleiner als 100 ist. Anschließend richten Sie eine weitere Bedingung so ein, dass Schritt 2 nur ausgeführt wird, wenn der Kostenbetrag größer als oder gleich 100 ist. Wenn der Workflow ausgeführt wird, zeigt die Workflowhistorie nur eine Position an und die erste Bedingung wird immer als *True* ausgewertet, unabhängig vom übermittelten Wert.

## <a name="workaround"></a>Problemumgehung

Im aktuellen Release gelten die Workflowbedingungen für Bestandserfassungen nur auf Erfassungsebene, nicht auf Positionsebene. Dieses Verhalten ist beabsichtigt. Wir empfehlen, dass Sie Ihre Bedingungskriterien nur für Attribute auf Erfassungsebene festlegen.
