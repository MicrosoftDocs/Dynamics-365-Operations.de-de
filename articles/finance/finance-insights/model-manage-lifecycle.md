---
title: Modellverwaltungslebenszyklus (Vorschau)
description: In diesem Thema werden Möglichkeiten zum Verwalten der Machine Learning-Modelle Ihrer Organisation beschrieben, um die von ihnen generierten Vorhersagen zu optimieren.
author: ShivamPandey-msft
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: c84f0a6079d7e599ed1f3e44c26c625e548c06d5a91447c46fc722ce6a6cf414
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741559"
---
# <a name="model-management-lifecycle-preview"></a>Modellverwaltungslebenszyklus (Vorschau)

[!include [banner](../includes/banner.md)]

In diesem Thema werden Möglichkeiten zum Verwalten der Machine Learning-Modelle Ihrer Organisation beschrieben, um die von ihnen generierten Vorhersagen zu optimieren.

Wir empfehlen, dass Sie das KI-Modell in einer Sandbox-Umgebung trainieren und dann verwaltete Lösungen verwenden, um es in einer Produktionsumgebung bereitzustellen. Dieser Ansatz trägt dazu bei, sicherzustellen, dass die richtigen Kontrollen für die Verwaltung des Modelllebenszyklus vorhanden sind.

Da das KI-Modell auf den verfügbaren Rechnungs- und Kundendaten basiert, ist es wichtig, dass die Sandbox-Umgebung über eine aktuelle Kopie der Produktionsdaten verfügt. Sie können mit dem Trainieren Ihres Modells beginnen, indem Sie die Schritte in [Vorhersagen für Kundenzahlungen verwenden](use-customer-payment-predictions.md) befolgen. Nachdem das Modell neu trainiert wurde, bewerten Sie die Ergebnisse wie in [Bewerten des anfänglichen Kundenzahlungsvorhersagemodells](evaluate-payment-prediction.md) beschrieben. Verwenden Sie die Informationen in [Vorhersagemodell verbessern](improve-model.md), um mit Funktions- und Filterkombinationen zu experimentieren, die zur Verbesserung des Modells beitragen können.

Wenn Sie mit den Trainingsergebnissen zufrieden sind, befolgen Sie die Schritte in [Verteilen Ihres KI-Modells](https://docs.microsoft.com/ai-builder/distribute-model), um das Modell in Ihre Produktionsumgebung zu übertragen.
