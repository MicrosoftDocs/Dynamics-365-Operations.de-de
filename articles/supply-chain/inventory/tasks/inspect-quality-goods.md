---
title: Qualität der Waren inspizieren
description: In diesem Thema wird erläutert, wie Sie einen Qualitätsprüfungsauftrag verarbeiten.
author: perlynne
manager: AnnBe
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 10acb9aadfeb11ede1d66dd525ace7b70db3bd1c
ms.sourcegitcommit: fbaccf72df82e6b6927f0c9f0d35af0ca3ecbc2d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/02/2019
ms.locfileid: "1855685"
---
# <a name="inspect-the-quality-of-goods"></a><span data-ttu-id="f0caa-103">Qualität der Waren inspizieren</span><span class="sxs-lookup"><span data-stu-id="f0caa-103">Inspect the quality of goods</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f0caa-104">In diesem Thema wird erläutert, wie Sie einen Qualitätsprüfungsauftrag verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="f0caa-104">This topic explains how to process a quality order.</span></span> <span data-ttu-id="f0caa-105">Sie können diese Anleitung im Demodatenunternehmen USMF ausführen.</span><span class="sxs-lookup"><span data-stu-id="f0caa-105">You can run this guide in demo data company USMF.</span></span> <span data-ttu-id="f0caa-106">Bevor Sie diese Beispielprozedur beginnen, müssen Sie Bestellung "000016 " bestätigen und einen Produktzugang buchen.</span><span class="sxs-lookup"><span data-stu-id="f0caa-106">Before you start this example procedure, you need to confirm purchase order “000016” and post a product receipt.</span></span> <span data-ttu-id="f0caa-107">Dies erstellt automatisch einen Qualitätsprüfungsauftrag.</span><span class="sxs-lookup"><span data-stu-id="f0caa-107">This will automatically create a quality order.</span></span> <span data-ttu-id="f0caa-108">Qualitätsinspektionen werden normalerweise von einem Sachbearbeiter für die Qualitätskontrolle ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f0caa-108">Quality inspections are typically carried out by a quality clerk.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="f0caa-109">Wählen Sie einen Qualitätsprüfungsauftrag aus.</span><span class="sxs-lookup"><span data-stu-id="f0caa-109">Select a quality order</span></span>
1. <span data-ttu-id="f0caa-110">Wechseln Sie im Navigationsbereich zu **Module > Lagerverwaltung > Periodische Aufgaben > Qualitätsmanagement > Qualitätsprüfungsaufträge**.</span><span class="sxs-lookup"><span data-stu-id="f0caa-110">In the navigation pane, go to **Modules > Inventory management > Periodic tasks > Quality management > Quality orders**.</span></span>
2. <span data-ttu-id="f0caa-111">Wählen Sie den Qualitätsprüfungsauftrag, der erstellt wurde, bevor Sie dieses Verfahren gestartet haben.</span><span class="sxs-lookup"><span data-stu-id="f0caa-111">Select the quality order that was created before you started this procedure.</span></span>  

## <a name="record-test-results"></a><span data-ttu-id="f0caa-112">Erfassen von Testergebnissen</span><span class="sxs-lookup"><span data-stu-id="f0caa-112">Record test results</span></span>
1. <span data-ttu-id="f0caa-113">Wählen Sie **Ergebnisse** aus.</span><span class="sxs-lookup"><span data-stu-id="f0caa-113">Select **Results**.</span></span>
2. <span data-ttu-id="f0caa-114">Wählen Sie **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="f0caa-114">Select **Edit**.</span></span>
3. <span data-ttu-id="f0caa-115">Geben Sie im Feld **Ergebnismenge** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="f0caa-115">In the **Result quantity** field, enter a number.</span></span>
4. <span data-ttu-id="f0caa-116">Wählen Sie im Feld **Ergebnis** den gewünschten Datensatz im Dropdownmenü aus.</span><span class="sxs-lookup"><span data-stu-id="f0caa-116">In the **Outcome** field, select the desired record in the drop-down menu.</span></span>  
- <span data-ttu-id="f0caa-117">In diesem Beispiel basiert das Ergebnis auf einem vordefinierten Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="f0caa-117">In this example the result is based on a pre-defined outcome.</span></span> <span data-ttu-id="f0caa-118">Normalerweise erfassen Sie ein spezifischeres Testergebnis, z. B. eine Größe oder eine andere Dimension.</span><span class="sxs-lookup"><span data-stu-id="f0caa-118">Normally you would record a more specific test result, for example a size or other dimension.</span></span>  
5. <span data-ttu-id="f0caa-119">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="f0caa-119">Select **Save**.</span></span>
6. <span data-ttu-id="f0caa-120">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="f0caa-120">Close the page.</span></span>

## <a name="validate-the-quality-order"></a><span data-ttu-id="f0caa-121">Qualitätsprüfungsauftrag überprüfen</span><span class="sxs-lookup"><span data-stu-id="f0caa-121">Validate the quality order</span></span>
1. <span data-ttu-id="f0caa-122">Wählen Sie **Überprüfen** aus.</span><span class="sxs-lookup"><span data-stu-id="f0caa-122">Select **Validate**.</span></span>
2. <span data-ttu-id="f0caa-123">Wählen Sie im Feld **Geprüft von** im Dropdownfeld den Benutzer aus, der die Prüfung ausführt.</span><span class="sxs-lookup"><span data-stu-id="f0caa-123">In the **Validated by** field, select the user performing the inspection from the drop-down menu.</span></span>  
3. <span data-ttu-id="f0caa-124">Klicken Sie auf **Auswählen**.</span><span class="sxs-lookup"><span data-stu-id="f0caa-124">Click **Select**.</span></span>
4. <span data-ttu-id="f0caa-125">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="f0caa-125">Select **OK**.</span></span>
5. <span data-ttu-id="f0caa-126">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="f0caa-126">Close the page.</span></span>

