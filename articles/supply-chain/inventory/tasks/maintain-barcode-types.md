---
title: Strichcodetypen verwalten
description: Dieses Verfahren zeigt Ihnen, wie eine neue Strichcodedefinition eingerichtet wird, die dann als Teil des Kommissionierlistenberichts verwendet werden kann.
author: perlynne
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BarcodeSetup, InventParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 71bbc090d928cb80d19db33655ec9c9cc8e654bd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011496"
---
# <a name="maintain-barcode-types"></a><span data-ttu-id="0f804-103">Strichcodetypen verwalten</span><span class="sxs-lookup"><span data-stu-id="0f804-103">Maintain barcode types</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0f804-104">Dieses Verfahren zeigt Ihnen, wie eine neue Strichcodedefinition eingerichtet wird, die dann als Teil des Kommissionierlistenberichts verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="0f804-104">This procedure shows you how to set up a new barcode definition which can then be used as part of the picking list report.</span></span> <span data-ttu-id="0f804-105">Sie können diese Prozedur Schritt für Schritt im Demodatenunternehmen USMF durchführen oder können Ihre eigenen Daten verwenden.</span><span class="sxs-lookup"><span data-stu-id="0f804-105">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="0f804-106">Wenn Sie USMF verwenden, können Sie die Beispielswerte verwenden, die angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="0f804-106">If you are using USMF you can use the example values that are shown.</span></span> <span data-ttu-id="0f804-107">Diese Aufgaben werden normalerweise von einem Lagerortleiter ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0f804-107">These tasks would typically be carried out by a warehouse manager.</span></span>

1. <span data-ttu-id="0f804-108">Wechseln Sie zu Strichcodes.</span><span class="sxs-lookup"><span data-stu-id="0f804-108">Go to Bar codes.</span></span>
2. <span data-ttu-id="0f804-109">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="0f804-109">Click New.</span></span>
3. <span data-ttu-id="0f804-110">Geben Sie im Feld "Strichcodeeinstellung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="0f804-110">In the Barcode setup field, type a value.</span></span>
4. <span data-ttu-id="0f804-111">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="0f804-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="0f804-112">Wählen Sie im Feld "Strichcodetyp " eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="0f804-112">In the Bar code type field, select an option.</span></span>
    * <span data-ttu-id="0f804-113">Wenn Sie USMF verwenden, können Sie "Code 39" auswählen.</span><span class="sxs-lookup"><span data-stu-id="0f804-113">If you're using USMF, you can select 'Code 39'.</span></span>  
6. <span data-ttu-id="0f804-114">Geben Sie im Feld "Größe" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="0f804-114">In the Size field, enter a number.</span></span>
7. <span data-ttu-id="0f804-115">Geben Sie im Feld "Höchstlänge" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="0f804-115">In the Maximum length field, enter a number.</span></span>
8. <span data-ttu-id="0f804-116">Klicken Sie auf Speichern.</span><span class="sxs-lookup"><span data-stu-id="0f804-116">Click Save.</span></span>
9. <span data-ttu-id="0f804-117">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="0f804-117">Close the page.</span></span>
10. <span data-ttu-id="0f804-118">Wechseln Sie zu "Parameter für Lager- und Lagerortverwaltung".</span><span class="sxs-lookup"><span data-stu-id="0f804-118">Go to Inventory and warehouse management parameters.</span></span>
11. <span data-ttu-id="0f804-119">Geben Sie im Feld 'Strichcodeeinstellung' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="0f804-119">In the Barcode setup field, enter or select a value.</span></span>
    * <span data-ttu-id="0f804-120">Wählen Sie die Strichcodeeinrichtung, die Sie vorher erstellt haben. Beachten Sie ab, dass das Strichcodeformat mit dem Format des eindeutigen Bezeichners für den Datensatz in Fertigung übereinstimmen muss.</span><span class="sxs-lookup"><span data-stu-id="0f804-120">Select the barcode setup that you created before, but be aware that the bar code format must match the format of the unique identifier for the record type used in the process.</span></span> <span data-ttu-id="0f804-121">Für Entnahmerouten sollte das Strichcodeformat zum Beispiel mit dem Format der Entnahmeroutenreferenz übereinstimmen (üblicherweise ein Nummernkreis).</span><span class="sxs-lookup"><span data-stu-id="0f804-121">For example, for picking routes, the bar code format should match the format of the picking route reference, which is typically a number sequence.</span></span>  
12. <span data-ttu-id="0f804-122">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="0f804-122">Click Save.</span></span>
13. <span data-ttu-id="0f804-123">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="0f804-123">Close the page.</span></span>

