---
title: Kostenobjektdimensionen
description: Wenn Sie Kosten analysieren, verwenden Sie Kostenelementdimensionen, um zu bestimmen, wohin Kosten fließen. Sie verwenden Kostenträgerdimensionen, um zu bestimmen, wo Sie Kosten zuweisen sollten. Dieser Artikel bietet Informationen über Kostenträgerdimensionen.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimensionMember, CAMCostObject
audience: Application User
ms.reviewer: twheeloc
ms.custom: 223174
ms.assetid: 2a1cdd35-30cb-41e7-9506-67fd04a537c5
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: twheeloc
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 3ee481b9dafe202e0a850a31b6ab036d52a20547
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874637"
---
# <a name="cost-object-dimensions"></a>Kostenträgerdimensionen

[!include [banner](../includes/banner.md)]

Wenn Sie Kosten analysieren, verwenden Sie Kostenelementdimensionen, um zu bestimmen, wohin Kosten fließen. Sie verwenden Kostenträgerdimensionen, um zu bestimmen, wo Sie Kosten zuweisen sollten. Dieser Artikel bietet Informationen über Kostenträgerdimensionen.

Ein Kostenträger kann jeder Typ von Objekt sein, den Sie vorkalkulieren möchten, dem Sie Kosten zuteilen möchten oder den sie direkt messen möchten. Typische Kostenträger sind unter Anderem Produkte, Projekte, Ressourcen, Abteilungen, Kostenstellen und geografische Regionen. Die Verwaltung verwendet Kostenträger, um Kosten mengenmäßig zu bestimmen und auch um die Rentabilitätsanalyse voranzutreiben.

## <a name="cost-object-dimensions-and-cost-object-dimension-members"></a>Kostenträgerdimensionen und Kostenträger-Dimensionsmitglieder
Kostenträger werden als *Kostenträgerdimensionen* bezeichnet. Nachdem Sie sich entschieden haben, auf welche Entität die Kostenträgerdimension verweisen soll, müssen Sie die einzelnen Dimensionswerte angeben oder sie in die Kostenrechnung aus anderen Quellsystemen importieren. Diese einzelnen Dimensionswerte sind als *Kostenträger-Dimensionsmitglieder* bekannt. Sie möchten beispielsweise die Finanzdimension, die als „Kostenstelle” bezeichnet wird, als die Kostenträgerdimension verwenden. Um zu sehen, wie Kosten zu einzelnen Kostenstellen fließen, müssen Sie die Kostenträger-Dimensionsmitglieder importieren. In diesem Fall sind die Kostenträger-Dimensionsmitglieder die Istkostenstellen, beispielsweise Vertrieb, Produktion, Verwaltung und geografische Orte. Das folgende Screenshot zeigt ein Beispiel von Kostenstellen als die Kostenträgerdimension mit ihren Istkostenstellen als Kostenträger-Dimensionsmitglieder an. 

[![Screenshot mit Kostenstellen als Kostenträgerdimension.](./media/cost-object-dimensions.png)](./media/cost-object-dimensions.png)

## <a name="import-cost-object-dimension-members-through-data-connectors"></a>Kostenträger-Dimensionsmitglieder über Datenkonnektoren importieren
Um den Import von den Kostenträgerdimensionsmitgliedern zu erleichtern, verwenden Sie Datenkonnektoren, um die Werte aus den Entitäten abzurufen, die Sie als Kostenträgerdimensionen verwenden möchten. Sie können entweder die bereits erstellten Datenkonnektoren oder benutzerdefinierte Datenkonnektoren, die Sie erstellen, verwenden.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
