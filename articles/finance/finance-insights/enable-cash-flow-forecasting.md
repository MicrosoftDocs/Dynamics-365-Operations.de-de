---
title: Cashflow-Vorhersage aktivieren
description: In diesem Thema wird erläutert, wie Sie die Funktion „Cashflow-Planung“ in Finance Insights aktivieren.
author: ShivamPandey-msft
ms.date: 11/03/2021
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
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: cfcdbe76d640d1786b4622febf9157f5fb1c42f9
ms.sourcegitcommit: 133aa728b8a795eaeaef22544f76478da2bd1df9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/13/2022
ms.locfileid: "7969136"
---
# <a name="enable-cash-flow-forecasting"></a>Cashflow-Vorhersage aktivieren

[!include [banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie die Funktion „Cashflow-Planung“ in Finance Insights aktivieren.

> [!NOTE]
> Um Zahlungsvorhersagen im Cashflow zu verwenden, müssen Sie die Funktion „Debitorenzahlungsvorhersagen“ wie unter [Debitorenzahlungsvorhersagen aktivieren](enable-cust-paymnt-prediction.md) beschrieben einrichten.
  
1. Öffnen Sie den **Funktionsverwaltung**-Arbeitsbereich, und befolgen Sie diese Schritte:

    1. Wählen Sie **Nach Updates suchen**.
    2. Suchen Sie auf der Registerkarte **Alle** nach **Cashflow-Planungen**. Wenn Sie diese Funktion nicht finden, suchen Sie nach **(Vorschau) Cashflow-Planungen**. 
    3. Aktivieren Sie die Funktion.

2. Gehen Sie zu **Bargeld- und Bankverwaltung \> Einrichtung der Cashflow-Planung** und fügen Sie die Liquiditätskonten hinzu, die in den Planungen enthalten sein sollen. Richten Sie auch das Liquiditätskonto für Zahlungen auf den Registerkarten **Debitorenkonten** und **Kreditorenkonten**. Stellen Sie sicher, dass Sie die Cashflow-Planung neu berechnen.

    > [!NOTE]
    > Wenn keine Liquiditätskonten eingerichtet sind, kann der Cashflow nicht generiert werden.
    >
    > Weitere Informationen dazu, wie Cashflow-Planungen eingerichtet wird, finden Sie unter [Cashflow-Planung](../cash-bank-management/cash-flow-forecasting.md).

3. Gehen Sie zu **Bargeld- und Bankverwaltung \> Einrichten \> Finance Insights (Vorschau) \> Cashflow-Planungen (Vorschau)** und befolgen Sie diese Schritte:

    1. Auf der **Cashflow-Planung**-Registerkarte wählen Sie **Funktion aktivieren**.
    2. Wählen Sie **Vorhersagemodell erstellen**.

Weitere Informationen dazu, wie die Cashflow-Planungsfunktion eingerichtet wird, finden Sie unter [Cashflow-Planung](cash-flow-forecast-intro.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
