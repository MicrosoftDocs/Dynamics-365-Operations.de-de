--- 
title: " Machine-Learning-unterstützte Produktempfehlungen konfigurieren"
description: "Dieses Verfahren aktualisiert die Daten im Entitätsspeicher, der durch das Machine-Learning-System verwendet wird, das Produktempfehlungen unterstützt, und aktiviert dann Produktempfehlungen auf POS-Clients."
author: ashishmsft
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 277ffb879b80fe57deeaa2b52c1543baaf820274
ms.contentlocale: de-de
ms.lasthandoff: 02/07/2018

---
# <a name="configure-machine-learning-powered-product-recommendations"></a><span data-ttu-id="36c86-103"> Machine-Learning-unterstützte Produktempfehlungen konfigurieren</span><span class="sxs-lookup"><span data-stu-id="36c86-103">Configure machine learning-powered product recommendations</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="36c86-104">Dieses Verfahren aktualisiert die Daten im Entitätsspeicher, der durch das Machine-Learning-System verwendet wird, das Produktempfehlungen unterstützt, und aktiviert dann Produktempfehlungen auf POS-Clients.</span><span class="sxs-lookup"><span data-stu-id="36c86-104">This procedure refreshes the data in the Entity store that is used by the machine learning system that powers product recommendations, and then enables product recommendations on POS clients.</span></span> <span data-ttu-id="36c86-105">Für diese Prozedur wird das Demo-Datenunternehmen USRT verwendet.</span><span class="sxs-lookup"><span data-stu-id="36c86-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="36c86-106">Gehen Sie zu Systemadministration > Einstellungen > Entitätsspeicher</span><span class="sxs-lookup"><span data-stu-id="36c86-106">Go to System administration > Setup > Entity Store.</span></span>
2. <span data-ttu-id="36c86-107">Suchen Sie in der Liste den Datensatz "RetailSales", und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="36c86-107">In the list, find and select the record 'RetailSales'.</span></span>
3. <span data-ttu-id="36c86-108">Klicken Sie auf Aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="36c86-108">Click Refresh.</span></span>
4. <span data-ttu-id="36c86-109">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="36c86-109">Click OK.</span></span>
5. <span data-ttu-id="36c86-110">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="36c86-110">Close the page.</span></span>
6. <span data-ttu-id="36c86-111">Navigieren Sie zu "Einzelhandel und Handel" > "Hauptsitz einrichten" > "Parameter" > "Einzelhandelsparameter".</span><span class="sxs-lookup"><span data-stu-id="36c86-111">Go to Retail and commerce > Headquarters setup > Parameters > Retail parameters.</span></span>
7. <span data-ttu-id="36c86-112">Klicken Sie auf die Registerkarte "Machine Learning".</span><span class="sxs-lookup"><span data-stu-id="36c86-112">Click the Machine learning tab.</span></span>
8. <span data-ttu-id="36c86-113">Wählen Sie "Ja" im Feld "Produktempfehlungen aktivieren" aus.</span><span class="sxs-lookup"><span data-stu-id="36c86-113">Select 'Yes' in the Enable product recommendations field.</span></span>
    * <span data-ttu-id="36c86-114">Wenn die Meldung erhalten "Die Empfehlungsmodelle konnten nicht abgerufen werden.", liegt dies daran, dass Sie den Entitätsspeicher vor kurzem aktualisiert haben und das System die Einbeziehung der neuen Daten nicht abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="36c86-114">If you receive the message "The recommendation models couldn't be retrieved", it’s because you refreshed the Entity Store very recently and the system may not have finished assimilating the new data.</span></span> <span data-ttu-id="36c86-115">Warten Sie 2-3 Stunden und versuchen Sie es erneut.</span><span class="sxs-lookup"><span data-stu-id="36c86-115">Wait 2-3 hours and try again.</span></span>  
9. <span data-ttu-id="36c86-116">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="36c86-116">Click Save.</span></span>
10. <span data-ttu-id="36c86-117">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="36c86-117">Close the page.</span></span>


