--- 
title: " Machine-Learning-unterstützte Produktempfehlungen konfigurieren"
description: "Dieses Verfahren aktualisiert die Daten im Entitätsspeicher, der durch das Machine-Learning-System verwendet wird, das Produktempfehlungen unterstützt, und aktiviert dann Produktempfehlungen auf POS-Clients."
author: ashishmsft
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9b080ff46a0fbc73ed4f8fa3f03d71e9d758cc2
ms.openlocfilehash: 4d7e9b3afdae77246a8c30147e81f565bbc0fca5
ms.contentlocale: de-de
ms.lasthandoff: 01/17/2018

---
# <a name="configure-machine-learning-powered-product-recommendations"></a><span data-ttu-id="de2d6-103"> Machine-Learning-unterstützte Produktempfehlungen konfigurieren</span><span class="sxs-lookup"><span data-stu-id="de2d6-103">Configure machine learning-powered product recommendations</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="de2d6-104">Dieses Verfahren aktualisiert die Daten im Entitätsspeicher, der durch das Machine-Learning-System verwendet wird, das Produktempfehlungen unterstützt, und aktiviert dann Produktempfehlungen auf POS-Clients.</span><span class="sxs-lookup"><span data-stu-id="de2d6-104">This procedure refreshes the data in the Entity store that is used by the machine learning system that powers product recommendations, and then enables product recommendations on POS clients.</span></span> <span data-ttu-id="de2d6-105">Für diese Prozedur wird das Demo-Datenunternehmen USRT verwendet.</span><span class="sxs-lookup"><span data-stu-id="de2d6-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="de2d6-106">Gehen Sie zu Systemadministration > Einstellungen > Entitätsspeicher</span><span class="sxs-lookup"><span data-stu-id="de2d6-106">Go to System administration > Setup > Entity Store.</span></span>
2. <span data-ttu-id="de2d6-107">Suchen Sie in der Liste den Datensatz "RetailSales", und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="de2d6-107">In the list, find and select the record 'RetailSales'.</span></span>
3. <span data-ttu-id="de2d6-108">Klicken Sie auf Aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="de2d6-108">Click Refresh.</span></span>
4. <span data-ttu-id="de2d6-109">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="de2d6-109">Click OK.</span></span>
5. <span data-ttu-id="de2d6-110">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="de2d6-110">Close the page.</span></span>
6. <span data-ttu-id="de2d6-111">Navigieren Sie zu "Einzelhandel und Handel" > "Hauptsitz einrichten" > "Parameter" > "Einzelhandelsparameter".</span><span class="sxs-lookup"><span data-stu-id="de2d6-111">Go to Retail and commerce > Headquarters setup > Parameters > Retail parameters.</span></span>
7. <span data-ttu-id="de2d6-112">Klicken Sie auf die Registerkarte "Machine Learning".</span><span class="sxs-lookup"><span data-stu-id="de2d6-112">Click the Machine learning tab.</span></span>
8. <span data-ttu-id="de2d6-113">Wählen Sie "Ja" im Feld "Produktempfehlungen aktivieren" aus.</span><span class="sxs-lookup"><span data-stu-id="de2d6-113">Select 'Yes' in the Enable product recommendations field.</span></span>
    * <span data-ttu-id="de2d6-114">Wenn die Meldung erhalten "Die Empfehlungsmodelle konnten nicht abgerufen werden.", liegt dies daran, dass Sie den Entitätsspeicher vor kurzem aktualisiert haben und das System die Einbeziehung der neuen Daten nicht abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="de2d6-114">If you receive the message "The recommendation models couldn't be retrieved", it’s because you refreshed the Entity Store very recently and the system may not have finished assimilating the new data.</span></span> <span data-ttu-id="de2d6-115">Warten Sie 2-3 Stunden und versuchen Sie es erneut.</span><span class="sxs-lookup"><span data-stu-id="de2d6-115">Wait 2-3 hours and try again.</span></span>  
9. <span data-ttu-id="de2d6-116">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="de2d6-116">Click Save.</span></span>
10. <span data-ttu-id="de2d6-117">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="de2d6-117">Close the page.</span></span>


