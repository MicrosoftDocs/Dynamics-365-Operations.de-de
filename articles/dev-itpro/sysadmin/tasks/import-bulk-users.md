--- 
title: "Importbenutzer in großer Stückzahl"
description: Diese Prozedur kann von Systemadministratoren verwendet werden, um viele Benutzer aus dem Azure Active Directory zu importieren.
author: maertenm
manager: AnnBe
ms.date: 07/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 046b06f663f2fa4b503bcfff15c9fd7675d6acdd
ms.contentlocale: de-de
ms.lasthandoff: 04/13/2018

---
# <a name="import-users-in-bulk"></a><span data-ttu-id="f30a2-103">Importbenutzer in großer Stückzahl</span><span class="sxs-lookup"><span data-stu-id="f30a2-103">Import users in bulk</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f30a2-104">Diese Prozedur kann von Systemadministratoren verwendet werden, um viele Benutzer aus dem Azure Active Directory zu importieren.</span><span class="sxs-lookup"><span data-stu-id="f30a2-104">This procedure can be used by system administrators to import a large number of users from Azure Active Directory.</span></span>


## <a name="run-as-a-batch-job"></a><span data-ttu-id="f30a2-105">Als Batchauftrag ausführen</span><span class="sxs-lookup"><span data-stu-id="f30a2-105">Run as a batch job</span></span>
1. <span data-ttu-id="f30a2-106">Wechseln Sie zu "Systemverwaltung" > "Benutzer" > "Benutzer".</span><span class="sxs-lookup"><span data-stu-id="f30a2-106">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="f30a2-107">Stapelimportpfade anklicken.</span><span class="sxs-lookup"><span data-stu-id="f30a2-107">Click Batch import.</span></span>
3. <span data-ttu-id="f30a2-108">Erweitern Sie den Abschnitt "Ausführen im Hintergrund".</span><span class="sxs-lookup"><span data-stu-id="f30a2-108">Expand the Run in the background section.</span></span>
4. <span data-ttu-id="f30a2-109">Wählen Sie "Ja" im Feld "Stapelverarbeitung" aus.</span><span class="sxs-lookup"><span data-stu-id="f30a2-109">Select Yes in the Batch processing field.</span></span>
5. <span data-ttu-id="f30a2-110">«»Geben Sie im Feld Elementbeschreibung einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="f30a2-110">In the Task description field, type a value.</span></span>
6. <span data-ttu-id="f30a2-111">Geben Sie im Feld "Chargengruppenfeld" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="f30a2-111">In the Batch group field, enter or select a value.</span></span>
    * <span data-ttu-id="f30a2-112">Dieser Schritt ist optional.</span><span class="sxs-lookup"><span data-stu-id="f30a2-112">This is an optional step.</span></span>  
7. <span data-ttu-id="f30a2-113">Wählen Sie "Ja" im Feld "Privat" aus.</span><span class="sxs-lookup"><span data-stu-id="f30a2-113">Select Yes in the Private field.</span></span>
    * <span data-ttu-id="f30a2-114">Dieser Schritt ist optional.</span><span class="sxs-lookup"><span data-stu-id="f30a2-114">This is an optional step.</span></span>  
8. <span data-ttu-id="f30a2-115">Wählen Sie "Ja" im Feld "Kritische Aufgabe".</span><span class="sxs-lookup"><span data-stu-id="f30a2-115">Select Yes in the Critical Job field.</span></span>
    * <span data-ttu-id="f30a2-116">Dieser Schritt ist optional.</span><span class="sxs-lookup"><span data-stu-id="f30a2-116">This is an optional step.</span></span>  
9. <span data-ttu-id="f30a2-117">Wählen Sie im Feld "Kategorie überwachen" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="f30a2-117">In the Monitoring category field, select an option.</span></span>
10. <span data-ttu-id="f30a2-118">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="f30a2-118">Click OK.</span></span>

## <a name="run-in-a-sandbox-environment"></a><span data-ttu-id="f30a2-119">Eine Sandkastenumgebung ausführen</span><span class="sxs-lookup"><span data-stu-id="f30a2-119">Run in a sandbox environment</span></span>
1. <span data-ttu-id="f30a2-120">Stapelimportpfade anklicken.</span><span class="sxs-lookup"><span data-stu-id="f30a2-120">Click Batch import.</span></span>
2. <span data-ttu-id="f30a2-121">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="f30a2-121">Click OK.</span></span>


