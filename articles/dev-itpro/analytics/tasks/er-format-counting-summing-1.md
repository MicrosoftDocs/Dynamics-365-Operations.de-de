--- 
title: "Format zum Zählen und Summieren erstellen"
description: "In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Format zur Inventarisierung und Summierung basierend auf der bereits generierten Textausgabe."
author: NickSelin
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 7613b78d4a9ab63f5be9773a8699fe3ed94636eb
ms.contentlocale: de-de
ms.lasthandoff: 04/13/2018

---
# <a name="create-format-for-counting-and-summing"></a><span data-ttu-id="a72ed-103">Format zum Zählen und Summieren erstellen</span><span class="sxs-lookup"><span data-stu-id="a72ed-103">Create format for counting and summing</span></span> 

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a72ed-104">In den folgenden Schritten wird erläutert, wie ein Benutzer mit der Rolle Systemadministrator oder Entwickler für elektronische Berichterstellung ein ER-Format zur Inventarisierung und Summierung basierend auf der bereits generierten Textausgabe.</span><span class="sxs-lookup"><span data-stu-id="a72ed-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="a72ed-105">Diese Schritte können in jedem Unternehmen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a72ed-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="a72ed-106">Um diese Schritte auszuführen, müssen Sie zunächst die Schritte unter "Konfigurationsanbieter erstellen und als aktiv markieren" abschließen.</span><span class="sxs-lookup"><span data-stu-id="a72ed-106">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

<span data-ttu-id="a72ed-107">Diese Prozedur ist eine Funktion, die in Dynamics 365 for Operations, Version 1611 hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="a72ed-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="a72ed-108">Zugriff auf die Liste von Microsoft bereitgestellte von den Konfigurationen erhalten</span><span class="sxs-lookup"><span data-stu-id="a72ed-108">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="a72ed-109">Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.</span><span class="sxs-lookup"><span data-stu-id="a72ed-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="a72ed-110">Überprüfen Sie, ob "Litware, Inc."</span><span class="sxs-lookup"><span data-stu-id="a72ed-110">Make sure that the “Litware, Inc.”</span></span> <span data-ttu-id="a72ed-111">Anbieter ist verfügbar und markiert als aktiv.</span><span class="sxs-lookup"><span data-stu-id="a72ed-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="a72ed-112">Wählen Sie den "Litware, Inc."-</span><span class="sxs-lookup"><span data-stu-id="a72ed-112">Select the “Litware, Inc.”</span></span> <span data-ttu-id="a72ed-113">Anbieter.</span><span class="sxs-lookup"><span data-stu-id="a72ed-113">provider.</span></span>
3. <span data-ttu-id="a72ed-114">Klicken Sie auf Repositorys.</span><span class="sxs-lookup"><span data-stu-id="a72ed-114">Click Repositories.</span></span>
    * <span data-ttu-id="a72ed-115">Wenn ein Repository des Typs "Operations-Ressourcen" vorhanden ist, überspringen Sie die übrigen Schritte der aktuellen Unteraufgabe.</span><span class="sxs-lookup"><span data-stu-id="a72ed-115">If a repository of the "Operations resources" type already exists, skip the remaining steps of the current sub-task.</span></span>  
4. <span data-ttu-id="a72ed-116">Klicken Sie zum Öffnen des Ablage-Dialogfelds auf "Hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="a72ed-116">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="a72ed-117">Geben Sie im Feld "Konfigurationsrepository-Typ" die Bezeichnung "Betriebliche Ressourcen" ein.</span><span class="sxs-lookup"><span data-stu-id="a72ed-117">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="a72ed-118">Klicken Sie auf "Repository erstellen".</span><span class="sxs-lookup"><span data-stu-id="a72ed-118">Click Create repository.</span></span>
7. <span data-ttu-id="a72ed-119">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="a72ed-119">Click OK.</span></span>

## <a name="get-the-intrastat-configurations-provided-by-microsoft"></a><span data-ttu-id="a72ed-120">Intrastat-Konfigurationen von Microsoft erhalten</span><span class="sxs-lookup"><span data-stu-id="a72ed-120">Get the Intrastat configurations provided by Microsoft</span></span>
1. <span data-ttu-id="a72ed-121">Klicken Sie auf "Öffnen".</span><span class="sxs-lookup"><span data-stu-id="a72ed-121">Click Open.</span></span>
2. <span data-ttu-id="a72ed-122">Wählen Sie in der Strukturdarstellung "Intrastatmodel\Intrastat (DE)" aus.</span><span class="sxs-lookup"><span data-stu-id="a72ed-122">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
3. <span data-ttu-id="a72ed-123">Klicken Sie auf Import.</span><span class="sxs-lookup"><span data-stu-id="a72ed-123">Click Import.</span></span>
    * <span data-ttu-id="a72ed-124">Klicken Sie auf "Importieren" für Version 1.1 der ausgewählten Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="a72ed-124">Click Import for version 1.1 of the selected configuration.</span></span>  
4. <span data-ttu-id="a72ed-125">Klicken Sie auf "Ja".</span><span class="sxs-lookup"><span data-stu-id="a72ed-125">Click Yes.</span></span>
5. <span data-ttu-id="a72ed-126">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="a72ed-126">Close the page.</span></span>
6. <span data-ttu-id="a72ed-127">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="a72ed-127">Close the page.</span></span>
7. <span data-ttu-id="a72ed-128">Klicken Sie auf "Berichterstellungskonfigurationen".</span><span class="sxs-lookup"><span data-stu-id="a72ed-128">Click Reporting configurations.</span></span>
8. <span data-ttu-id="a72ed-129">Erweitern Sie 'Intrastatmodell' in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="a72ed-129">In the tree, expand 'Intrastat model'.</span></span>
9. <span data-ttu-id="a72ed-130">Wählen Sie in der Strukturdarstellung "Intrastatmodel\Intrastat (DE)" aus.</span><span class="sxs-lookup"><span data-stu-id="a72ed-130">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>


