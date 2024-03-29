---
title: Modellverwaltungslebenszyklus
description: In diesem Artikel werden Möglichkeiten zum Verwalten der Machine Learning-Modelle Ihrer Organisation beschrieben, um die von ihnen generierten Vorhersagen zu optimieren.
author: ShivamPandey-msft
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 526916929e4bc079f9cea82d8ea9f80813e89b83
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880873"
---
# <a name="model-management-lifecycle"></a>Modellverwaltungslebenszyklus

[!include [banner](../includes/banner.md)]

In diesem Artikel werden Möglichkeiten zum Verwalten der Machine Learning-Modelle Ihrer Organisation beschrieben, um die von ihnen generierten Vorhersagen zu optimieren.

Wir empfehlen, dass Sie das KI-Modell in einer Sandbox-Umgebung trainieren und dann verwaltete Lösungen verwenden, um es in einer Produktionsumgebung bereitzustellen. Dieser Ansatz trägt dazu bei, sicherzustellen, dass die richtigen Kontrollen für die Verwaltung des Modelllebenszyklus vorhanden sind.

Da das KI-Modell auf den verfügbaren Rechnungs- und Kundendaten basiert, ist es wichtig, dass die Sandbox-Umgebung über eine aktuelle Kopie der Produktionsdaten verfügt. Sie können mit dem Trainieren Ihres Modells beginnen, indem Sie die Schritte in [Vorhersagen für Kundenzahlungen verwenden](use-customer-payment-predictions.md) befolgen. Nachdem das Modell neu trainiert wurde, bewerten Sie die Ergebnisse wie in [Bewerten des anfänglichen Kundenzahlungsvorhersagemodells](evaluate-payment-prediction.md) beschrieben. Verwenden Sie die Informationen in [Vorhersagemodell verbessern](improve-model.md), um mit Funktions- und Filterkombinationen zu experimentieren, die zur Verbesserung des Modells beitragen können.

Wenn Sie mit den Trainingsergebnissen zufrieden sind, befolgen Sie die Schritte in [Verteilen Ihres KI-Modells](/ai-builder/distribute-model), um das Modell in Ihre Produktionsumgebung zu übertragen.
