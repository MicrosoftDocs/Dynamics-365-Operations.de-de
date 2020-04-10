---
title: Eine Kostenelementdimension zuordnen
description: Ein Kostencontroller kann diesen Schritt verwenden, um eine Kostenfaktordimension zu einer Kostenfaktordimension der MXMF-juristischen Person zuzuordnen.
author: ShylaThompson
manager: AnnBe
ms.date: 06/28/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1a5805b7d86979389f1eb7496a63e3f4e7056c92
ms.sourcegitcommit: c69926b4285cb2ec2d9ce1ad72d1cb852024dd5e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3137867"
---
# <a name="map-a-cost-element-dimension"></a><span data-ttu-id="7b141-103">Eine Kostenelementdimension zuordnen</span><span class="sxs-lookup"><span data-stu-id="7b141-103">Map a cost element dimension</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7b141-104">Ein Kostencontroller kann diesen Schritt verwenden, um eine Kostenfaktordimension zu einer Kostenfaktordimension der MXMF-juristischen Person zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="7b141-104">A cost controller can use this procedure to map a cost element dimension to a cost element dimension in the MXMF legal entity.</span></span> <span data-ttu-id="7b141-105">Für diese Aufzeichnung wird das Demo-Datenunternehmen USP2 verwendet.</span><span class="sxs-lookup"><span data-stu-id="7b141-105">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="7b141-106">Wechseln Sie zu den Kostenrechnung > Dimensionen > Kostenelementdimensionen.</span><span class="sxs-lookup"><span data-stu-id="7b141-106">Go to Cost accounting > Dimensions > Cost element dimensions.</span></span>
2. <span data-ttu-id="7b141-107">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="7b141-107">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="7b141-108">Wählen Sie für dieses Beispiel die Option "Kostenelemente" aus.</span><span class="sxs-lookup"><span data-stu-id="7b141-108">For this example, select Cost elements.</span></span>  
3. <span data-ttu-id="7b141-109">Dimensionszuordnungen anklicken.</span><span class="sxs-lookup"><span data-stu-id="7b141-109">Click Dimension mappings.</span></span>
4. <span data-ttu-id="7b141-110">Zuordnungen aus dieser Dimension konfigurieren anklicken.</span><span class="sxs-lookup"><span data-stu-id="7b141-110">Click Configure mappings from this dimension.</span></span>
5. <span data-ttu-id="7b141-111">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="7b141-111">Click New.</span></span>
6. <span data-ttu-id="7b141-112">Geben Sie im Feld 'Dimensionsname' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="7b141-112">In the To dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="7b141-113">Wählen Sie für dieses Beispiel das MXMF-Kostenelemente aus.</span><span class="sxs-lookup"><span data-stu-id="7b141-113">For this example, select MXMF Cost elements.</span></span>  
7. <span data-ttu-id="7b141-114">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="7b141-114">Click New.</span></span>
8. <span data-ttu-id="7b141-115">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="7b141-115">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="7b141-116">Geben Sie im Feld "Von Dimensionsmitglied" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="7b141-116">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="7b141-117">Wählen Sie für dieses Beispiel die Option Dimensionsmitglied 606400 Telefon- Faxausgaben.</span><span class="sxs-lookup"><span data-stu-id="7b141-117">For this example, select dimension member 606400 Telephone & Fax Expense.</span></span>  
10. <span data-ttu-id="7b141-118">Geben Sie im Feld "Dimensionsmitglied" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="7b141-118">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="7b141-119">Wählen Sie für dieses Beispiel die Option Dimensionsmitglied 6001004 Telefono aus.</span><span class="sxs-lookup"><span data-stu-id="7b141-119">For this example, select dimension member 6001004 Telefono.</span></span>  
11. <span data-ttu-id="7b141-120">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="7b141-120">Click Save.</span></span>

