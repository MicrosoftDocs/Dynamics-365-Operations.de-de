---
title: Qualität der Waren inspizieren
description: Dieses Thema beschreibt, wie Sie Qualitätsprüfungsaufträge verarbeiten.
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ec67e7864db12178c0f3cfe8b93d510a46e8a0d4
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956133"
---
# <a name="inspect-the-quality-of-goods"></a><span data-ttu-id="74bea-103">Qualität der Waren inspizieren</span><span class="sxs-lookup"><span data-stu-id="74bea-103">Inspect the quality of goods</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="74bea-104">Dieses Thema beschreibt, wie Sie Qualitätsprüfungsaufträge verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="74bea-104">This topic describes how to process quality orders.</span></span> <span data-ttu-id="74bea-105">Qualitätsprüfungen werden normalerweise von einem Qualitätssachbearbeiter durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="74bea-105">Quality inspections are typically done by a quality clerk.</span></span>

<span data-ttu-id="74bea-106">Wenn die Standard-Demodaten installiert sind, können Sie sie verwenden, um die Verfahren in diesem Thema abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="74bea-106">If the standard demo data is installed, you can use it to complete the procedures in this topic.</span></span> <span data-ttu-id="74bea-107">Um die Demo-Daten zu verwenden, wählen Sie vorher die *USMF* juristische Entität aus.</span><span class="sxs-lookup"><span data-stu-id="74bea-107">To use the demo data, select the *USMF* legal entity before you begin.</span></span> <span data-ttu-id="74bea-108">Anschließend müssen Sie die Bestellung *000016* bestätigen und einen Wareneingang buchen.</span><span class="sxs-lookup"><span data-stu-id="74bea-108">You must then confirm purchase order *000016* and post a product receipt.</span></span> <span data-ttu-id="74bea-109">Ein Qualitätsprüfungsauftrag wird automatisch generiert.</span><span class="sxs-lookup"><span data-stu-id="74bea-109">A quality order is automatically generated.</span></span>

## <a name="step-1-select-a-quality-order"></a><span data-ttu-id="74bea-110">Schritt 1: Wählen Sie einen Qualitätsprüfungsauftrag</span><span class="sxs-lookup"><span data-stu-id="74bea-110">Step 1: Select a quality order</span></span>

<span data-ttu-id="74bea-111">Um einen Qualitätsprüfungsauftrag auszuwählen, führen Sie diese Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="74bea-111">To select a quality order, follow these steps.</span></span>

1. <span data-ttu-id="74bea-112">Wechseln Sie zu **Bestandsverwaltung \> Periodische Aufgaben \> Qualitätsmanagement \> Qualitätsprüfungsaufträge**.</span><span class="sxs-lookup"><span data-stu-id="74bea-112">Go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>
1. <span data-ttu-id="74bea-113">Wählen Sie den Qualitätsprüfungsauftrag, der erzeugt wurde, bevor Sie diesen Vorgang gestartet haben.</span><span class="sxs-lookup"><span data-stu-id="74bea-113">Select the quality order that was generated before you started this procedure.</span></span>

## <a name="step-2-record-test-results"></a><span data-ttu-id="74bea-114">Schritt 2: Testergebnisse aufzeichnen</span><span class="sxs-lookup"><span data-stu-id="74bea-114">Step 2: Record test results</span></span>

<span data-ttu-id="74bea-115">Um Testergebnisse zu protokollieren, führen Sie diese Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="74bea-115">To record test results, follow these steps.</span></span>

1. <span data-ttu-id="74bea-116">Wählen Sie **Ergebnisse** aus.</span><span class="sxs-lookup"><span data-stu-id="74bea-116">Select **Results**.</span></span>
1. <span data-ttu-id="74bea-117">Wählen Sie **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="74bea-117">Select **Edit**.</span></span>
1. <span data-ttu-id="74bea-118">Geben Sie im Feld **Ergebnismenge** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="74bea-118">In the **Result quantity** field, enter a number.</span></span>
1. <span data-ttu-id="74bea-119">Wählen Sie im Feld **Ergebnis** den gewünschten Datensatz.</span><span class="sxs-lookup"><span data-stu-id="74bea-119">In the **Outcome** field, select the desired record.</span></span> <span data-ttu-id="74bea-120">In diesem Beispiel basiert das Ergebnis auf einem vordefinierten Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="74bea-120">In this example, the result is based on a predefined outcome.</span></span> <span data-ttu-id="74bea-121">Normalerweise werden Sie einen spezifischeren Datensatz erfassen, z. B. eine Größe oder eine andere Dimension.</span><span class="sxs-lookup"><span data-stu-id="74bea-121">Usually, you will record a more specific test result, such as a size or other dimension.</span></span>
1. <span data-ttu-id="74bea-122">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="74bea-122">Select **Save**.</span></span>
1. <span data-ttu-id="74bea-123">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="74bea-123">Close the page.</span></span>

## <a name="step-3-validate-the-quality-order"></a><span data-ttu-id="74bea-124">Schritt 3: Validieren des Qualitätsprüfungsauftrags</span><span class="sxs-lookup"><span data-stu-id="74bea-124">Step 3: Validate the quality order</span></span>

<span data-ttu-id="74bea-125">Gehen Sie folgendermaßen vor, um den Qualitätsprüfungsauftrag zu validieren.</span><span class="sxs-lookup"><span data-stu-id="74bea-125">To validate the quality order, follow these steps.</span></span>

1. <span data-ttu-id="74bea-126">Wählen Sie **Überprüfen** aus.</span><span class="sxs-lookup"><span data-stu-id="74bea-126">Select **Validate**.</span></span>
1. <span data-ttu-id="74bea-127">Wählen Sie im Feld **Gültig gemacht von** den Benutzer aus, der die Überprüfung durchführt.</span><span class="sxs-lookup"><span data-stu-id="74bea-127">In the **Validated by** field, select the user who is doing the inspection.</span></span>
1. <span data-ttu-id="74bea-128">Wählen Sie **Auswählen**.</span><span class="sxs-lookup"><span data-stu-id="74bea-128">Select **Select**.</span></span>
1. <span data-ttu-id="74bea-129">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="74bea-129">Select **OK**.</span></span>
1. <span data-ttu-id="74bea-130">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="74bea-130">Close the page.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
