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
ms.openlocfilehash: 2d3f1bc2526eeacb4bd6338a0679eadd95a75989
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024955"
---
# <a name="enable-product-recommendations"></a>Produktempfehlungen aktivieren

[!include [banner](includes/banner.md)]

In diesem Thema wird erläutert, wie Produktempfehlungen erstellt werden, die auf dem künstlichen Intelligenz-Maschinenlernen basieren (AI-ML) die für Microsoft Dynamics 365 Commerce Kunden zur Verfügung stehen. Weitere Informationen zu Produktempfehlungslisten finden Sie im [Produktempfehlungsüberblick](product-recommendations.md).

## <a name="recommendations-pre-check"></a>Produktempfehlungen Vor-Prüfung

Vor dem Aktivieren beachten Sie, dass Produktempfehlungen nur für Commerce-Kunden unterstützt werden, die ihren Speicher für die Nutzung von Azure Data Lake Storage (ADLS) migriert haben. 

Schritte zum Aktivieren von ADLS finden Sie unter [So aktivieren Sie ADLS in einer Dynamics 365-Umgebung](enable-ADLS-environment.md).

Außerdem stellen Sie sicher, dass RetailSale-Messungen aktiviert wurden. Weitere Informationen über diesen Einrichtungsprozess finden Sie [hier.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)


## <a name="turn-on-recommendations"></a>Empfehlungen aktivieren

Um Produktempfehlungen zu aktivieren, gehen Sie folgendermaßen vor:

1. Gehen Sie zu **Retail und Commerce &gt; Produktempfehlungen &gt; Empfehlungsparameter**.
1. In der Liste der freigegebenen Parameter wählen Sie **Empfehlungs-Listen** aus.
1. Legen Sie die Option **Empfehlungen aktivieren** auf **Ja** fest.

![Produktempfehlungen aktivieren](./media/enableproductrecommendations.png)

> [!NOTE]
> Diese Verfahren startet den Vorgang zum Generieren von Produktempfehlungslisten. Bis zu mehreren Stunden können erforderlich sein, bevor die Listen zur Verfügung stehen und können an der Verkaufsstelle (POS) oder in Dynamics 365 Commerce angezeigt werden.

## <a name="configure-recommendation-list-parameters"></a>Konfigurieren Sie Empfehlungslistenparameter

Standardmäßig enthält die AI-ML-basierte Produktempfehlungsliste vorgeschlagene Werte. Sie können die vorgeschlagenen Standardwerte ändern, um dem Ablauf Ihres Unternehmens zu entsprechen. Um mehr darüber zu erfahren, wie die Standardparameter geändert werden, gehen Sie zu [Verwalten Sie AI-ML-basierte Produktempfehlungsergebnisse](modify-product-recommendation-results.md).

## <a name="show-recommendations-on-pos-devices"></a>Empfehlungen für POS-Geräte anzeigen

Nachdem Empfehlungen im Commerce-Back-Office aktiviert wurden, muss der Empfehlungsbereich zum Bildschirm der POS-Steuerung über das Layouttool hinzugefügt werden. Informationen zu diesem Vorgang finden Sie unter [Hinzufügen eines Empfehlungssteuerelements zum Transaktionsbildschirm auf POS-Geräten](add-recommendations-control-pos-screen.md). 

## <a name="enable-personalized-recommendations"></a>Personalisierte Produktempfehlungen aktivieren

Weitere Informationen zum Empfangen personalisierter Empfehlungen finden Sie unter [Personalisierte Produktempfehlungen aktivieren](personalized-recommendations.md).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Überblick über Produktempfehlungen](product-recommendations.md)

[Personalisierte Produktempfehlungen aktivieren](personalized-recommendations.md)

[Hinzufügen von Produktempfehlungslisten zu Seiten](add-reco-list-to-page.md)

[Fügen Sie Empfehlungsbereich für POS-Geräten hinzu](add-recommendations-control-pos-screen.md)

[Übersicht über Produktsammelmodule](product-collection-module-overview.md)

[Aktivieren von ADLS in einer Dynamics 365-Umgebung](enable-ADLS-environment.md)

