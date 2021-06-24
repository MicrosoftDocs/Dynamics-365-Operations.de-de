---
title: Cashflow-Planung aktivieren (Vorschau)
description: In diesem Thema wird erläutert, wie Sie die Funktion „Cashflow-Planung“ in Finance Insights aktivieren.
author: ShivamPandey-msft
ms.date: 06/03/2021
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
ms.openlocfilehash: ba8acb2191291e2abed5cabf234c19fe09e6c8ff
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222557"
---
# <a name="enable-cash-flow-forecasting-preview"></a><span data-ttu-id="cb93b-103">Cashflow-Planung aktivieren (Vorschau)</span><span class="sxs-lookup"><span data-stu-id="cb93b-103">Enable cash flow forecasting (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="cb93b-104">In diesem Thema wird erläutert, wie Sie die Funktion „Cashflow-Planung“ in Finance Insights aktivieren.</span><span class="sxs-lookup"><span data-stu-id="cb93b-104">This topic explains how to turn on the Cash flow forecasts feature in Finance Insights.</span></span>

> [!NOTE]
> <span data-ttu-id="cb93b-105">Um Zahlungsvorhersagen im Cashflow zu verwenden, müssen Sie die Funktion „Debitorenzahlungsvorhersagen“ wie unter [Debitorenzahlungsvorhersagen aktivieren](enable-cust-paymnt-prediction.md) beschrieben einrichten.</span><span class="sxs-lookup"><span data-stu-id="cb93b-105">To use payment predictions in the cash flow, you must set up the Customer payment predictions feature as described in [Enable customer payment predictions](enable-cust-paymnt-prediction.md).</span></span>

1. <span data-ttu-id="cb93b-106">Verwenden Sie Informationen von der Umgebungsseite in Microsoft Dynamics Lifecycle Services (LCS), um eine Verbindung mit der primären Instanz von Azure-SQL für diese Umgebung herzustellen.</span><span class="sxs-lookup"><span data-stu-id="cb93b-106">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="cb93b-107">Führen Sie den folgenden Transact-SQL-Befehl (T-SQL) aus, um Flights für die Sandboxumgebung zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="cb93b-107">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="cb93b-108">(Möglicherweise müssen Sie den Zugriff für Ihre IP-Adresse in LCS aktivieren, bevor Sie eine Remoteverbindung mit Application Object Server \[AOS\] herstellen können.)</span><span class="sxs-lookup"><span data-stu-id="cb93b-108">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('CashflowInsightsFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="cb93b-109">Überspringen Sie diesen Schritt, wenn Sie Version 10.0.20 oder höher verwenden oder wenn Sie eine Service Fabric-Bereitstellung verwenden.</span><span class="sxs-lookup"><span data-stu-id="cb93b-109">Skip this step if you're using version 10.0.20 or later, or if you're using a Service Fabric deployment.</span></span> <span data-ttu-id="cb93b-110">Das Finance Insights-Team sollte das Flight bereits für Sie aktiviert haben.</span><span class="sxs-lookup"><span data-stu-id="cb93b-110">The Finance insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="cb93b-111">Wenn die Funktion nicht im **Funktionsverwaltung**-Arbeitsbereich angezeigt wird, oder wenn Sie Probleme beim Aktivieren haben, wenden Sie sich an <fiap@microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="cb93b-111">If you don't see the feature in the **Feature management** workspace, or if you experience issues when you try to turn it on, contact <fiap@microsoft.com>.</span></span>
  
2. <span data-ttu-id="cb93b-112">Öffnen Sie den **Funktionsverwaltung**-Arbeitsbereich, und befolgen Sie diese Schritte:</span><span class="sxs-lookup"><span data-stu-id="cb93b-112">Open the **Feature management** workspace, and follow these steps:</span></span>

    1. <span data-ttu-id="cb93b-113">Wählen Sie **Nach Updates suchen**.</span><span class="sxs-lookup"><span data-stu-id="cb93b-113">Select **Check for updates**.</span></span>
    2. <span data-ttu-id="cb93b-114">Aktivieren Sie die folgenden Funktionen:</span><span class="sxs-lookup"><span data-stu-id="cb93b-114">Turn on the following features:</span></span>

        - <span data-ttu-id="cb93b-115">Neues Rastersteuerelement</span><span class="sxs-lookup"><span data-stu-id="cb93b-115">New grid control</span></span>
        - <span data-ttu-id="cb93b-116">Gruppierung in Rastern (Vorschau)</span><span class="sxs-lookup"><span data-stu-id="cb93b-116">Grouping in grids (preview)</span></span> 
        - <span data-ttu-id="cb93b-117">Zahlungsvorhersagen für Debitoren (Vorschau)</span><span class="sxs-lookup"><span data-stu-id="cb93b-117">Customer payment predictions (preview)</span></span>
        - <span data-ttu-id="cb93b-118">Cashflow-Planungen (Vorschau)</span><span class="sxs-lookup"><span data-stu-id="cb93b-118">Cash flow forecasts (preview)</span></span>

3. <span data-ttu-id="cb93b-119">Gehen Sie zu **Bargeld- und Bankverwaltung \> Einrichtung der Cashflow-Planung** und fügen Sie die Liquiditätskonten hinzu, die in den Planungen enthalten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="cb93b-119">Go to **Cash and bank management \> Cash flow forecast setup**, and add the liquidity accounts that should be included in the forecasts.</span></span>

    > [!NOTE]
    > <span data-ttu-id="cb93b-120">Wenn keine Liquiditätskonten eingerichtet sind, kann der Cashflow nicht generiert werden.</span><span class="sxs-lookup"><span data-stu-id="cb93b-120">If liquidity accounts aren't set up, the cash flow can't be generated.</span></span>

4. <span data-ttu-id="cb93b-121">Gehen Sie zu **Bargeld- und Bankverwaltung \> Einrichten \> Finance Insights (Vorschau) \> Cashflow-Planungen (Vorschau)** und befolgen Sie diese Schritte:</span><span class="sxs-lookup"><span data-stu-id="cb93b-121">Go to **Cash and bank management \> Setup \> Finance Insights (preview) \> Cash flow forecasts (preview)**, and follow these steps:</span></span>

    1. <span data-ttu-id="cb93b-122">Auf der **Cashflow-Planung**-Registerkarte wählen Sie **Funktion aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="cb93b-122">On the **Cash flow forecast** tab, select **Enable feature**.</span></span>
    2. <span data-ttu-id="cb93b-123">Wählen Sie **Vorhersagemodell erstellen**.</span><span class="sxs-lookup"><span data-stu-id="cb93b-123">Select **Create prediction model**.</span></span>

<span data-ttu-id="cb93b-124">Weitere Informationen dazu, wie die Cashflow-Planungsfunktion eingerichtet wird, finden Sie unter [Cashflow-Planung](cash-flow-forecast-intro.md).</span><span class="sxs-lookup"><span data-stu-id="cb93b-124">For more information about the cash flow forecasting capability, see [Cash flow forecasting](cash-flow-forecast-intro.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
