---
title: Eine Kostenelementdimension zuordnen
description: Ein Kostencontroller kann diesen Schritt verwenden, um eine Kostenfaktordimension zu einer Kostenfaktordimension der MXMF-juristischen Person zuzuordnen.
author: ShylaThompson
ms.date: 06/28/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 845ab27a09905f42c905f9018f9f176a64f8785a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841044"
---
# <a name="map-a-cost-element-dimension"></a><span data-ttu-id="43838-103">Eine Kostenelementdimension zuordnen</span><span class="sxs-lookup"><span data-stu-id="43838-103">Map a cost element dimension</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="43838-104">Ein Kostencontroller kann diesen Schritt verwenden, um eine Kostenfaktordimension zu einer Kostenfaktordimension der MXMF-juristischen Person zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="43838-104">A cost controller can use this procedure to map a cost element dimension to a cost element dimension in the MXMF legal entity.</span></span> <span data-ttu-id="43838-105">Für diese Aufzeichnung wird das Demo-Datenunternehmen USP2 verwendet.</span><span class="sxs-lookup"><span data-stu-id="43838-105">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="43838-106">Wechseln Sie zu den Kostenrechnung > Dimensionen > Kostenelementdimensionen.</span><span class="sxs-lookup"><span data-stu-id="43838-106">Go to Cost accounting > Dimensions > Cost element dimensions.</span></span>
2. <span data-ttu-id="43838-107">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="43838-107">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="43838-108">Wählen Sie für dieses Beispiel die Option "Kostenelemente" aus.</span><span class="sxs-lookup"><span data-stu-id="43838-108">For this example, select Cost elements.</span></span>  
3. <span data-ttu-id="43838-109">Dimensionszuordnungen anklicken.</span><span class="sxs-lookup"><span data-stu-id="43838-109">Click Dimension mappings.</span></span>
4. <span data-ttu-id="43838-110">Zuordnungen aus dieser Dimension konfigurieren anklicken.</span><span class="sxs-lookup"><span data-stu-id="43838-110">Click Configure mappings from this dimension.</span></span>
5. <span data-ttu-id="43838-111">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="43838-111">Click New.</span></span>
6. <span data-ttu-id="43838-112">Geben Sie im Feld 'Dimensionsname' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="43838-112">In the To dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="43838-113">Wählen Sie für dieses Beispiel das MXMF-Kostenelemente aus.</span><span class="sxs-lookup"><span data-stu-id="43838-113">For this example, select MXMF Cost elements.</span></span>  
7. <span data-ttu-id="43838-114">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="43838-114">Click New.</span></span>
8. <span data-ttu-id="43838-115">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="43838-115">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="43838-116">Geben Sie im Feld "Von Dimensionsmitglied" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="43838-116">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="43838-117">Wählen Sie für dieses Beispiel die Option Dimensionsmitglied 606400 Telefon- Faxausgaben.</span><span class="sxs-lookup"><span data-stu-id="43838-117">For this example, select dimension member 606400 Telephone & Fax Expense.</span></span>  
10. <span data-ttu-id="43838-118">Geben Sie im Feld "Dimensionsmitglied" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="43838-118">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="43838-119">Wählen Sie für dieses Beispiel die Option Dimensionsmitglied 6001004 Telefono aus.</span><span class="sxs-lookup"><span data-stu-id="43838-119">For this example, select dimension member 6001004 Telefono.</span></span>  
11. <span data-ttu-id="43838-120">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="43838-120">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]