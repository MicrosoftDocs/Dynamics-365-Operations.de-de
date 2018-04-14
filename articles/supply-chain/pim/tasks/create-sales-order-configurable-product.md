--- 
title: "Auftrag für ein konfigurierbares Produkt erstellen"
description: "Dieses Verfahren zeigt, wie die Konfigurationsvorlage für das Produkt auf einem Auftrag angewendet wird."
author: YuyuScheller
manager: AnnBe
ms.date: 10/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: db06eef916b1298470e51b8674fc0dee15184473
ms.contentlocale: de-de
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-sales-order-for-a-configurable-product"></a><span data-ttu-id="24110-103">Auftrag für ein konfigurierbares Produkt erstellen</span><span class="sxs-lookup"><span data-stu-id="24110-103">Create a sales order for a configurable product</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="24110-104">Dieses Verfahren zeigt, wie die Konfigurationsvorlage für das Produkt auf einem Auftrag angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="24110-104">This procedure shows how to apply a configuration template to a product on a sales order.</span></span> <span data-ttu-id="24110-105">Dieses Beispiel verwendet das Lausprechermodell D0006 im Demodatenunternehmen USMF.</span><span class="sxs-lookup"><span data-stu-id="24110-105">This example uses the D0006 speaker model in the USMF demo data company.</span></span> <span data-ttu-id="24110-106">Diese Aufgaben werden normalerweise von einem Auftragsbearbeiter ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="24110-106">Typically, a sales order processor uses this procedure.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="24110-107">Auftrag erstellen</span><span class="sxs-lookup"><span data-stu-id="24110-107">Create a sales order</span></span>
1. <span data-ttu-id="24110-108">Klicken Sie auf "Auftragsverarbeitung und -abfrage".</span><span class="sxs-lookup"><span data-stu-id="24110-108">Click Sales order processing and inquiry.</span></span>
2. <span data-ttu-id="24110-109">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="24110-109">Click New.</span></span>
3. <span data-ttu-id="24110-110">Klicken Sie auf "Auftrag".</span><span class="sxs-lookup"><span data-stu-id="24110-110">Click Sales order.</span></span>
4. <span data-ttu-id="24110-111">Wählen Sie im Feld Debitorenkonto US-001 aus.</span><span class="sxs-lookup"><span data-stu-id="24110-111">In the Customer account field, select US-001.</span></span> 
5. <span data-ttu-id="24110-112">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="24110-112">Click OK.</span></span>
6. <span data-ttu-id="24110-113">Wählen Sie im Feld "Artikelnummer" die Zeichenfolge "D0006" aus.</span><span class="sxs-lookup"><span data-stu-id="24110-113">In the Item number field, select D0006.</span></span>
    * <span data-ttu-id="24110-114">Für diese Aufgabe müssen Sie ein konfigurierbares Produkt auswählen.</span><span class="sxs-lookup"><span data-stu-id="24110-114">For this task, you must select a configurable product.</span></span>  
7. <span data-ttu-id="24110-115">Klicken Sie auf "Produkt und Beschaffung".</span><span class="sxs-lookup"><span data-stu-id="24110-115">Click Product and supply.</span></span>
8. <span data-ttu-id="24110-116">Klicken Sie auf Klicken Sie auf die Zeile Konfigurieren..</span><span class="sxs-lookup"><span data-stu-id="24110-116">Click Configure line.</span></span>
    * <span data-ttu-id="24110-117">Beachten Sie, dass der Preis geändert wurde, gemäß der ausgewählten Konfiguration, und dass das Feld "Inkl. Kabel" jetzt Wahr ist.</span><span class="sxs-lookup"><span data-stu-id="24110-117">Note that the price has changed, based on the configuration that was selected, and that the Include cable field is now set to True.</span></span>  
    * <span data-ttu-id="24110-118">Beachten Sie den Standardpreis und die Einstellungen, die für das Kabel ausgewählt sind.</span><span class="sxs-lookup"><span data-stu-id="24110-118">Note the default price and the settings that are selected for the cable.</span></span>  
9. <span data-ttu-id="24110-119">Klicken Sie auf Vorlage laden..</span><span class="sxs-lookup"><span data-stu-id="24110-119">Click Load template.</span></span>
    * <span data-ttu-id="24110-120">Dieses Beispiel verdeutlicht, wie Sie eine Vorlage verwenden können, um eine vordefinierte Konfiguration auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="24110-120">This example shows how you can apply a template to select a predefined configuration.</span></span> <span data-ttu-id="24110-121">Wenn Sie dieses Verfahren als Aufgabenleitfaden verwenden, und andere die Attributwerte angezeigt werden sollen, die verfügbar sind, müssen Sie auf die Schaltfläche "Sperrung aufheben" klicken.</span><span class="sxs-lookup"><span data-stu-id="24110-121">If you’re using this procedure as a task guide and want to see the other attribute values that are available, you must click the Unlock button.</span></span>  
10. <span data-ttu-id="24110-122">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="24110-122">Click OK.</span></span>
11. <span data-ttu-id="24110-123">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="24110-123">Click OK.</span></span>
12. <span data-ttu-id="24110-124">Erweitern Sie den Abschnitt "Positionsdetails".</span><span class="sxs-lookup"><span data-stu-id="24110-124">Expand the Line details section.</span></span>
13. <span data-ttu-id="24110-125">Klicken Sie auf die Registerkarte "Produkt".</span><span class="sxs-lookup"><span data-stu-id="24110-125">Click the Product tab.</span></span>
    * <span data-ttu-id="24110-126">Die Konfiguration des Artikels wird jetzt unter Produktdimensionen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="24110-126">The configuration of the item is now listed under the product dimensions.</span></span>  
14. <span data-ttu-id="24110-127">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="24110-127">Close the page.</span></span>

## <a name="select-the-product-configuration"></a><span data-ttu-id="24110-128">Wählen der Produktkonfiguration</span><span class="sxs-lookup"><span data-stu-id="24110-128">Select the product configuration</span></span>


