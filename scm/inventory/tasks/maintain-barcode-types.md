---
title: Strichcodetypen verwalten
description: Dieses Verfahren zeigt Ihnen, wie eine neue Strichcodedefinition eingerichtet wird, die dann als Teil des Kommissionierlistenberichts verwendet werden kann.
author: perlynne
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0e7f66cccd76e5326fce75d1a13aff294c16fb9b
ms.openlocfilehash: 45323206550d1b0ed66d89f4be7b995c60af63fc
ms.contentlocale: de-de
ms.lasthandoff: 09/12/2017

---
# <a name="maintain-bar-code-types"></a><span data-ttu-id="ccc2c-103">Strichcodetypen verwalten</span><span class="sxs-lookup"><span data-stu-id="ccc2c-103">Maintain bar code types</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ccc2c-104">Dieses Verfahren zeigt Ihnen, wie eine neue Strichcodedefinition eingerichtet wird, die dann als Teil des Kommissionierlistenberichts verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="ccc2c-104">This procedure shows you how to set up a new barcode definition which can then be used as part of the picking list report.</span></span> <span data-ttu-id="ccc2c-105">Sie können diese Prozedur Schritt für Schritt im Demodatenunternehmen USMF durchführen oder können Ihre eigenen Daten verwenden.</span><span class="sxs-lookup"><span data-stu-id="ccc2c-105">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="ccc2c-106">Wenn Sie USMF verwenden, können Sie die Beispielswerte verwenden, die angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ccc2c-106">If you are using USMF you can use the example values that are shown.</span></span> <span data-ttu-id="ccc2c-107">Diese Aufgaben werden normalerweise von einem Lagerortleiter ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ccc2c-107">These tasks would typically be carried out by a warehouse manager.</span></span>

1. <span data-ttu-id="ccc2c-108">Wechseln Sie zu Strichcodes.</span><span class="sxs-lookup"><span data-stu-id="ccc2c-108">Go to Bar codes.</span></span>
2. <span data-ttu-id="ccc2c-109">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="ccc2c-109">Click New.</span></span>
3. <span data-ttu-id="ccc2c-110">Geben Sie im Feld "Strichcodeeinstellung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="ccc2c-110">In the Barcode setup field, type a value.</span></span>
4. <span data-ttu-id="ccc2c-111">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="ccc2c-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ccc2c-112">Wählen Sie im Feld "Strichcodetyp " eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="ccc2c-112">In the Bar code type field, select an option.</span></span>
    * <span data-ttu-id="ccc2c-113">Wenn Sie USMF verwenden, können Sie "Code 39" auswählen.</span><span class="sxs-lookup"><span data-stu-id="ccc2c-113">If you're using USMF, you can select 'Code 39'.</span></span>  
6. <span data-ttu-id="ccc2c-114">Geben Sie im Feld "Größe" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="ccc2c-114">In the Size field, enter a number.</span></span>
7. <span data-ttu-id="ccc2c-115">Geben Sie im Feld "Höchstlänge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="ccc2c-115">In the Maximum length field, enter a number.</span></span>
8. <span data-ttu-id="ccc2c-116">Klicken Sie auf Speichern.</span><span class="sxs-lookup"><span data-stu-id="ccc2c-116">Click Save.</span></span>
9. <span data-ttu-id="ccc2c-117">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="ccc2c-117">Close the page.</span></span>
10. <span data-ttu-id="ccc2c-118">Wechseln Sie zu "Parameter für Lager- und Lagerortverwaltung".</span><span class="sxs-lookup"><span data-stu-id="ccc2c-118">Go to Inventory and warehouse management parameters.</span></span>
11. <span data-ttu-id="ccc2c-119">Geben Sie im Feld 'Strichcodeeinstellung' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="ccc2c-119">In the Barcode setup field, enter or select a value.</span></span>
    * <span data-ttu-id="ccc2c-120">Wählen Sie die Strichcodeeinrichtung, die Sie vorher erstellt haben. Beachten Sie ab, dass das Strichcodeformat mit dem Format des eindeutigen Bezeichners für den Datensatz in Fertigung übereinstimmen muss.</span><span class="sxs-lookup"><span data-stu-id="ccc2c-120">Select the barcode setup that you created before, but be aware that the bar code format must match the format of the unique identifier for the record type used in the process.</span></span> <span data-ttu-id="ccc2c-121">Für Entnahmerouten sollte das Strichcodeformat zum Beispiel mit dem Format der Entnahmeroutenreferenz übereinstimmen (üblicherweise ein Nummernkreis).</span><span class="sxs-lookup"><span data-stu-id="ccc2c-121">For example, for picking routes, the bar code format should match the format of the picking route reference, which is typically a number sequence.</span></span>  
12. <span data-ttu-id="ccc2c-122">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="ccc2c-122">Click Save.</span></span>
13. <span data-ttu-id="ccc2c-123">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="ccc2c-123">Close the page.</span></span>

