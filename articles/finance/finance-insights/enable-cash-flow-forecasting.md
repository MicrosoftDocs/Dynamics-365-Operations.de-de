---
title: Cashflow-Planung aktivieren (Vorschau)
description: In diesem Thema wird erläutert, wie Sie die Funktion „Cashflow-Planung“ in Finance Insights aktivieren.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 1977dac4a3ab66cca2248dc0124d3a06d6963f40
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4978763"
---
# <a name="enable-cash-flow-forecasting-preview"></a>Cashflow-Planung aktivieren (Vorschau)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

In diesem Thema wird erläutert, wie Sie die Funktion „Cashflow-Planung“ in Finance Insights aktivieren.

> [!NOTE]
> Um Zahlungsvorhersagen im Cashflow zu verwenden, müssen Sie die Funktion „Debitorenzahlungsvorhersagen“ wie unter [Debitorenzahlungsvorhersagen aktivieren](enable-cust-paymnt-prediction.md) beschrieben einrichten.

1. Verwenden Sie Informationen von der Umgebungsseite in Microsoft Dynamics Lifecycle Services (LCS), um eine Verbindung mit der primären Instanz von Azure-SQL für diese Umgebung herzustellen. Führen Sie den folgenden Transact-SQL-Befehl (T-SQL) aus, um Flights für die Sandboxumgebung zu aktivieren. (Möglicherweise müssen Sie den Zugriff für Ihre IP-Adresse in LCS aktivieren, bevor Sie eine Remoteverbindung mit Application Object Server \[AOS\] herstellen können.)

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('CashflowInsightsFeature', 1)`

    > [!NOTE]
    > Wenn es sich bei Ihrer Bereitstellung von Microsoft Dynamics 365 Finance um eine Service Fabric-Bereitstellung handelt, können Sie diesen Schritt überspringen. Das Finance Insights-Team sollte das Flight bereits für Sie aktiviert haben. Wenn die Funktionen nicht im **Funktionsverwaltung**-Arbeitsbereich angezeigt werden, oder wenn Sie Probleme beim Aktivieren haben, wenden Sie sich an <fiap@microsoft.com>.
  
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

## <a name="privacy-notice"></a>Datenschutzhinweis

Vorschauen (1) wenden möglicherweise weniger Datenschutz- und Sicherheitsmaßnahmen an als der Dynamics 365 Finance and Operations-Dienst, (2) sind nicht in der Service Level Agreement (SLA) für diesen Dienst enthalten, (3) sollten nicht zur Verarbeitung personenbezogener Daten oder anderer Daten verwendet werden, die gesetzlichen oder behördlichen Compliance-Anforderungen unterliegen, und (4) hat begrenzten Support.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]