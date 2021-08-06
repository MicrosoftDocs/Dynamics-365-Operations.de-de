---
title: Cashflow-Planung aktivieren (Vorschau)
description: In diesem Thema wird erläutert, wie Sie die Funktion „Cashflow-Planung“ in Finance Insights aktivieren.
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
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 29118557a1de4d3521f8125395b26471f7f48f3e
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/17/2021
ms.locfileid: "6638620"
---
# <a name="enable-cash-flow-forecasting-preview"></a>Cashflow-Planung aktivieren (Vorschau)

[!include [banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie die Funktion „Cashflow-Planung“ in Finance Insights aktivieren.

> [!NOTE]
> Um Zahlungsvorhersagen im Cashflow zu verwenden, müssen Sie die Funktion „Debitorenzahlungsvorhersagen“ wie unter [Debitorenzahlungsvorhersagen aktivieren](enable-cust-paymnt-prediction.md) beschrieben einrichten.

1. Verwenden Sie Informationen von der Umgebungsseite in Microsoft Dynamics Lifecycle Services (LCS), um eine Verbindung mit der primären Instanz von Azure-SQL für diese Umgebung herzustellen. Führen Sie den folgenden Transact-SQL-Befehl (T-SQL) aus, um Flights für die Sandboxumgebung zu aktivieren. (Möglicherweise müssen Sie den Zugriff für Ihre IP-Adresse in LCS aktivieren, bevor Sie eine Remoteverbindung mit Application Object Server \[AOS\] herstellen können.)

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('CashflowInsightsFeature', 1)`

    > [!NOTE]
    > Überspringen Sie diesen Schritt, wenn Sie Version 10.0.20 oder höher verwenden oder wenn Sie eine Service Fabric-Bereitstellung verwenden. Das Finance Insights-Team sollte das Flight bereits für Sie aktiviert haben. Wenn die Funktion nicht im **Funktionsverwaltung**-Arbeitsbereich angezeigt wird, oder wenn Sie Probleme beim Aktivieren haben, wenden Sie sich an <fiap@microsoft.com>.
  
2. Öffnen Sie den **Funktionsverwaltung**-Arbeitsbereich, und befolgen Sie diese Schritte:

    1. Wählen Sie **Nach Updates suchen**.
    2. Aktivieren Sie die folgenden Funktionen:

        - Neues Rastersteuerelement
        - Gruppierung in Rastern (Vorschau) 
        - Zahlungsvorhersagen für Debitoren (Vorschau)
        - Cashflow-Planungen (Vorschau)

3. Gehen Sie zu **Bargeld- und Bankverwaltung \> Einrichtung der Cashflow-Planung** und fügen Sie die Liquiditätskonten hinzu, die in den Planungen enthalten sein sollen.

    > [!NOTE]
    > Wenn keine Liquiditätskonten eingerichtet sind, kann der Cashflow nicht generiert werden.

4. Gehen Sie zu **Bargeld- und Bankverwaltung \> Einrichten \> Finance Insights (Vorschau) \> Cashflow-Planungen (Vorschau)** und befolgen Sie diese Schritte:

    1. Auf der **Cashflow-Planung**-Registerkarte wählen Sie **Funktion aktivieren**.
    2. Wählen Sie **Vorhersagemodell erstellen**.

Weitere Informationen dazu, wie die Cashflow-Planungsfunktion eingerichtet wird, finden Sie unter [Cashflow-Planung](cash-flow-forecast-intro.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
