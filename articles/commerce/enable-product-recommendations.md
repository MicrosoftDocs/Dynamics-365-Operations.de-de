---
title: Produktempfehlungen aktivieren
description: In diesem Thema wird erläutert, wie Produktempfehlungen erstellt werden, die auf dem künstlichen Intelligenz-Maschinenlernen basieren (AI-ML) die für Microsoft Dynamics 365 Commerce Kunden zur Verfügung stehen.
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ecda571a356c6968196d09cc19923105cf4544ab
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770138"
---
# <a name="enable-product-recommendations"></a>Produktempfehlungen aktivieren

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

In diesem Thema wird erläutert, wie Produktempfehlungen erstellt werden, die auf dem künstlichen Intelligenz-Maschinenlernen basieren (AI-ML) die für Microsoft Dynamics 365 Commerce Kunden zur Verfügung stehen. Weitere Informationen zu Produktempfehlungslisten finden Sie im [Produktempfehlungsüberblick](product-recommendations.md).

## <a name="recommendations-pre-check"></a>Produktempfehlungen Vor-Prüfung
Vor dem Aktivieren beachten Sie, dass Produktempfehlungen nur für F&O-Debitoren unterstützt werden, die 10.0.6 Builds unterstützen und die Lagerung unter Verwendung von BDL migriert haben. 

Außerdem stellen Sie sicher, dass RetailSale-Messungen aktiviert wurden. Weitere Informationen über diesen Einrichtungsprozess finden Sie [hier.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)


## <a name="turn-on-recommendations"></a>Empfehlungen aktivieren

Um Produktempfehlungen zu aktivieren, gehen Sie folgendermaßen vor:

1. Gehen Sie zu **Einzelhandel** &gt; **Produktempfehlungen** &gt; **Empfehlungsparameter**.
1. In der Liste mit freigegebenen Retailparametern, wählen Sie **Empfehlungs-Listen** aus.
1. Legen Sie die Option **Empfehlungen aktivieren** auf **Ja** fest.

![Produktempfehlungen aktivieren](./media/enableproductrecommendations.png)

> [!NOTE]
> Diese Verfahren startet den Vorgang zum Generieren von Produktempfehlungslisten. Bis zu mehreren Stunden können erforderlich sein, bevor die Listen zur Verfügung stehen und können an der Verkaufsstelle (POS) oder in Dynamics 365 for Commerce angezeigt werden.

## <a name="configure-recommendation-list-parameters"></a>Konfigurieren Sie Empfehlungslistenparameter
Standardmäßig enthält die AI-ML-basierte Produktempfehlungsliste vorgeschlagene Werte. Sie können die vorgeschlagenen Standardwerte ändern, um dem Ablauf Ihres Unternehmens zu entsprechen. Um mehr darüber zu erfahren, wie die Standardparameter geändert werden, gehen Sie zu [Verwalten Sie AI-ML-basierte Produktempfehlungsergebnisse](modify-product-recommendation-results.md).

## <a name="show-recommendations-on-pos-devices"></a>Empfehlungen für POS-Geräte anzeigen
Nachdem Empfehlungen im Back Office aktiviert wurden, muss der Empfehlungsbereich auf dem Bildschirm der POS-STeuerung über das Layouttool hinzugefügt werden. Weitere Informationen über diesen Prozess finden Sie [hier.](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)


## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Überblick über Produktempfehlungen](product-recommendations.md)

[Hinzufügen von Produktempfehlungslisten zu Seiten](add-reco-list-to-page.md)

[Fügen Sie Empfehlungsbereich für POS-Geräten hinzu](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)


