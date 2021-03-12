---
title: Problembehandlung bei Einrichtung der Cashflow-Planung
description: Dieses Thema enthält Antworten auf Fragen, die Sie möglicherweise haben, wenn Sie die Cashflow-Planung konfigurieren. Behandelt werden häufig gestellte Fragen (FAQ) zur Einrichtung des Cashflows sowie zu Aktualisierungen des Cashflows und des Power BI-Cashflows.
author: panolte
manager: AnnBe
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2020-12-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 89eb2f1bcfc73a6a7171a275532b2356e858e87c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985286"
---
# <a name="troubleshoot-cash-flow-forecasting-setup"></a><span data-ttu-id="e70bf-104">Problembehandlung bei Einrichtung der Cashflow-Planung</span><span class="sxs-lookup"><span data-stu-id="e70bf-104">Troubleshoot cash flow forecasting setup</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e70bf-105">Dieses Thema enthält Antworten auf Fragen, die Sie möglicherweise haben, wenn Sie die Cashflow-Planung konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="e70bf-105">This topic provides answers to questions that you might have when you configure cash flow forecasting.</span></span> <span data-ttu-id="e70bf-106">Behandelt werden häufig gestellte Fragen (FAQ) zur Einrichtung des Cashflows sowie zu Aktualisierungen des Cashflows und des Power BI-Cashflows.</span><span class="sxs-lookup"><span data-stu-id="e70bf-106">It addresses frequently asked questions (FAQ) about the setup for cash flow, updates to cash flow, and cash flow Power BI.</span></span>

## <a name="why-is-cash-flow-shown-for-only-one-legal-entity"></a><span data-ttu-id="e70bf-107">Warum wird der Cashflow nur für eine juristische Person angezeigt?</span><span class="sxs-lookup"><span data-stu-id="e70bf-107">Why is cash flow shown for only one legal entity?</span></span>

<span data-ttu-id="e70bf-108">Die Cashflow-Planung wird pro juristischer Person konfiguriert und berechnet.</span><span class="sxs-lookup"><span data-stu-id="e70bf-108">Cash flow forecasting is configured and calculated per legal entity.</span></span> <span data-ttu-id="e70bf-109">Power BI-Berichte und die Funktion zur Cashflow-Planung in Finance Insights zeigen die Ergebnisse an.</span><span class="sxs-lookup"><span data-stu-id="e70bf-109">Power BI reports and the cash flow forecasts capability in Finance insights show the results.</span></span>

<span data-ttu-id="e70bf-110">Die Cashflow-Planung muss für jede juristische Person eingerichtet werden, für die Sie sich eine Planung anzeigen lassen möchten.</span><span class="sxs-lookup"><span data-stu-id="e70bf-110">Cash flow forecasting must be set up for each legal entity that you want to see a forecast for.</span></span> <span data-ttu-id="e70bf-111">Überprüfen Sie die Konfiguration der Cashflow-Planung in allen Ihren juristischen Personen.</span><span class="sxs-lookup"><span data-stu-id="e70bf-111">Review the configuration of cash flow forecasting in all your legal entities.</span></span> <span data-ttu-id="e70bf-112">Überprüfen Sie alternativ die Konfiguration aller juristischen Personen für die Cashflow-Planung, und stellen Sie sicher, dass sie wie beabsichtigt festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="e70bf-112">Alternatively, review the configuration of all the legal entities for cash flow forecasting, and make sure that they are set as you intended.</span></span>

## <a name="why-doesnt-power-bi-show-all-the-cash-flow-data"></a><span data-ttu-id="e70bf-113">Warum zeigt Power BI nicht alle Cashflow-Daten an?</span><span class="sxs-lookup"><span data-stu-id="e70bf-113">Why doesn't Power BI show all the cash flow data?</span></span>

<span data-ttu-id="e70bf-114">Es müssen mehrere Schritte ausgeführt werden, bevor Cashflow-Planungen in Power BI-Ansichten angezeigt werden können.</span><span class="sxs-lookup"><span data-stu-id="e70bf-114">Several steps must be completed before cash flow forecasts can appear in Power BI views.</span></span> <span data-ttu-id="e70bf-115">Überprüfen Sie die folgende Checkliste, und stellen Sie sicher, dass jeder Schritt abgeschlossen wurde:</span><span class="sxs-lookup"><span data-stu-id="e70bf-115">Review the following checklist, and make sure that every step has been completed:</span></span>

- <span data-ttu-id="e70bf-116">Richten Sie den Cashflow für jede juristische Person ein.</span><span class="sxs-lookup"><span data-stu-id="e70bf-116">Set up cash flow for each legal entity.</span></span>
- <span data-ttu-id="e70bf-117">Legen Sie in den Hauptbuchparametern die Systemwährung und den -wechselkurstyp fest.</span><span class="sxs-lookup"><span data-stu-id="e70bf-117">In General ledger parameters, set the system currency and the system exchange rate type.</span></span>
- <span data-ttu-id="e70bf-118">Legen Sie die Buchhaltungswährung für Sachkonto sowie den Wechselkurstyp fest.</span><span class="sxs-lookup"><span data-stu-id="e70bf-118">Set the ledger accounting currency and the exchange rate type.</span></span>
- <span data-ttu-id="e70bf-119">Geben Sie die Wechselkurse zwischen der Buchungswährung und der Buchhaltungswährung ein.</span><span class="sxs-lookup"><span data-stu-id="e70bf-119">Enter exchange rates between the transaction currency and the accounting currency.</span></span>
- <span data-ttu-id="e70bf-120">Geben Sie die Wechselkurse zwischen der Buchhaltungswährung und der Systemwährung ein.</span><span class="sxs-lookup"><span data-stu-id="e70bf-120">Enter exchange rates between the accounting currency and the system currency.</span></span>
- <span data-ttu-id="e70bf-121">Geben Sie die Wechselkurse zwischen der Buchhaltungswährung und jeder Bankwährung ein.</span><span class="sxs-lookup"><span data-stu-id="e70bf-121">Enter exchange rates between the accounting currency and each bank currency.</span></span>

## <a name="why-did-cash-flow-power-bi-work-in-previous-versions-but-is-now-blank"></a><span data-ttu-id="e70bf-122">Warum funktionierte der Cashflow-Power BI in früheren Versionen, ist jetzt aber leer?</span><span class="sxs-lookup"><span data-stu-id="e70bf-122">Why did cash flow Power BI work in previous versions but is now blank?</span></span>

<span data-ttu-id="e70bf-123">Stellen Sie sicher, dass die Messungen „Cashflow Measure V2“ und „LedgerCovLiquidityMeasurement“ aus dem Entitätsspeicher konfiguriert wurden.</span><span class="sxs-lookup"><span data-stu-id="e70bf-123">Verify that the "Cash flow measure V2" and "LedgerCovLiquidityMeasurement" measurements from Entity store have been configured.</span></span> <span data-ttu-id="e70bf-124">Weitere Informationen zum Arbeiten mit Daten im Entitätsspeicher finden Sie unter [Power BI-Integration mit Entitätsspeicher](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md). Stellen Sie sicher, dass alle Schritte zum Anzeigen von Power BI-Inhalten abgeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="e70bf-124">For more information about how to work with data in Entity store, see [Power BI integration with Entity store](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md) Verify that all the steps that are required to view Power BI content have been completed.</span></span> <span data-ttu-id="e70bf-125">Weitere Informationen finden Sie unter [Bargelübersicht Power BI Inhalt](Cash-Overview-Power-BI-content.md).</span><span class="sxs-lookup"><span data-stu-id="e70bf-125">For more information, see [Cash overview Power BI content](Cash-Overview-Power-BI-content.md).</span></span>

## <a name="have-the-entity-store-entities-been-refreshed"></a><span data-ttu-id="e70bf-126">Wurden die Entitätsspeicher-Entitäten aktualisiert?</span><span class="sxs-lookup"><span data-stu-id="e70bf-126">Have the Entity store entities been refreshed?</span></span>

<span data-ttu-id="e70bf-127">Sie müssen Ihre Entitäten regelmäßig aktualisieren, um sicherzustellen, dass die Daten aktuell und korrekt sind.</span><span class="sxs-lookup"><span data-stu-id="e70bf-127">You must periodically refresh your entities to ensure that the data is current and accurate.</span></span> <span data-ttu-id="e70bf-128">Rufen Sie **Systemverwaltung \> Einrichtung \> Entitätsspeicher** auf. Wählen Sie die Entität und anschließend **Aktualisieren** aus, um eine bestimmte Entität manuell zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="e70bf-128">To manually refresh a specific entity, go to **System administration \> Setup \> Entity store**, select the entity, and then select **Refresh**.</span></span> <span data-ttu-id="e70bf-129">Die Daten können auch automatisch aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="e70bf-129">The data can also be updated automatically.</span></span> <span data-ttu-id="e70bf-130">Setzen Sie auf der Seite **Entitätsspeicher** die Option **Automatische Aktualisierung aktiviert** auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="e70bf-130">On the **Entity store** page, set the **Automatic refresh enabled** option to **Yes**.</span></span>
