---
title: Importbenutzer in großer Stückzahl
description: Diese Prozedur kann von Systemadministratoren verwendet werden, um viele Benutzer aus Azure Active Directory zu importieren.
author: maertenm
manager: AnnBe
ms.date: 07/07/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7d8b55895c9dfaf1c69cd319697f1e0da5990daf
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144086"
---
# <a name="import-users-in-bulk"></a><span data-ttu-id="1dde6-103">Massenimport von Benutzern</span><span class="sxs-lookup"><span data-stu-id="1dde6-103">Import users in bulk</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1dde6-104">Diese Prozedur kann von Systemadministratoren verwendet werden, um viele Benutzer aus Azure Active Directory zu importieren.</span><span class="sxs-lookup"><span data-stu-id="1dde6-104">This procedure can be used by system administrators to import a large number of users from Azure Active Directory.</span></span>


## <a name="run-as-a-batch-job"></a><span data-ttu-id="1dde6-105">Als Batchauftrag ausführen</span><span class="sxs-lookup"><span data-stu-id="1dde6-105">Run as a batch job</span></span>
1. <span data-ttu-id="1dde6-106">Wechseln Sie zu "Systemverwaltung" > "Benutzer" > "Benutzer".</span><span class="sxs-lookup"><span data-stu-id="1dde6-106">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="1dde6-107">Stapelimportpfade anklicken.</span><span class="sxs-lookup"><span data-stu-id="1dde6-107">Click Batch import.</span></span>
3. <span data-ttu-id="1dde6-108">Erweitern Sie den Abschnitt "Ausführen im Hintergrund".</span><span class="sxs-lookup"><span data-stu-id="1dde6-108">Expand the Run in the background section.</span></span>
4. <span data-ttu-id="1dde6-109">Wählen Sie "Ja" im Feld "Stapelverarbeitung" aus.</span><span class="sxs-lookup"><span data-stu-id="1dde6-109">Select Yes in the Batch processing field.</span></span>
5. <span data-ttu-id="1dde6-110">«»Geben Sie im Feld Elementbeschreibung einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="1dde6-110">In the Task description field, type a value.</span></span>
6. <span data-ttu-id="1dde6-111">Geben Sie im Feld "Chargengruppenfeld" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="1dde6-111">In the Batch group field, enter or select a value.</span></span>
    * <span data-ttu-id="1dde6-112">Dieser Schritt ist optional.</span><span class="sxs-lookup"><span data-stu-id="1dde6-112">This is an optional step.</span></span>  
7. <span data-ttu-id="1dde6-113">Wählen Sie "Ja" im Feld "Privat" aus.</span><span class="sxs-lookup"><span data-stu-id="1dde6-113">Select Yes in the Private field.</span></span>
    * <span data-ttu-id="1dde6-114">Dieser Schritt ist optional.</span><span class="sxs-lookup"><span data-stu-id="1dde6-114">This is an optional step.</span></span>  
8. <span data-ttu-id="1dde6-115">Wählen Sie "Ja" im Feld "Kritische Aufgabe".</span><span class="sxs-lookup"><span data-stu-id="1dde6-115">Select Yes in the Critical Job field.</span></span>
    * <span data-ttu-id="1dde6-116">Dieser Schritt ist optional.</span><span class="sxs-lookup"><span data-stu-id="1dde6-116">This is an optional step.</span></span>  
9. <span data-ttu-id="1dde6-117">Wählen Sie im Feld "Kategorie überwachen" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="1dde6-117">In the Monitoring category field, select an option.</span></span>
10. <span data-ttu-id="1dde6-118">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="1dde6-118">Click OK.</span></span>

## <a name="run-in-a-sandbox-environment"></a><span data-ttu-id="1dde6-119">Eine Sandkastenumgebung ausführen</span><span class="sxs-lookup"><span data-stu-id="1dde6-119">Run in a sandbox environment</span></span>
1. <span data-ttu-id="1dde6-120">Stapelimportpfade anklicken.</span><span class="sxs-lookup"><span data-stu-id="1dde6-120">Click Batch import.</span></span>
2. <span data-ttu-id="1dde6-121">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="1dde6-121">Click OK.</span></span>

