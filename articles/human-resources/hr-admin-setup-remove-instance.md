---
title: Instanz entfernen
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5c5f875ad9361c31af4fbe863488b881cdd97a6e
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009099"
---
# <a name="remove-an-instance"></a><span data-ttu-id="7fb76-102">Instanz entfernen</span><span class="sxs-lookup"><span data-stu-id="7fb76-102">Remove an instance</span></span>

<span data-ttu-id="7fb76-103">Diese Artikel führt Sie durch den Prozess des Entfernens eine Testversions- oder Produktionsumgebung für Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="7fb76-103">This article walks you through the process of removing a test drive or production environment for Microsoft Dynamics 365 Human Resources.</span></span>

## <a name="remove-a-test-drive-environment"></a><span data-ttu-id="7fb76-104">Testversionsumgebung entfernen</span><span class="sxs-lookup"><span data-stu-id="7fb76-104">Remove a test drive environment</span></span>

<span data-ttu-id="7fb76-105">Human Resources-Testversionen werden mit einer 60-Tage-Ablaufrichtlinie bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="7fb76-105">Human Resources test drives are provisioned with a 60-day expiration policy.</span></span> <span data-ttu-id="7fb76-106">Aber Eigentümer von Testumgebungen haben die Option, ihren Versuch früh zu beenden, indem Sie die folgenden Schritte ausführen.</span><span class="sxs-lookup"><span data-stu-id="7fb76-106">However, owners of test drive environments have the option to end their trial early by completing the following steps.</span></span> 

1. <span data-ttu-id="7fb76-107">Zum [Power Apps Admin Center](https://admin.businessplatform.microsoft.com/) navigieren.</span><span class="sxs-lookup"><span data-stu-id="7fb76-107">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="7fb76-108">Wählen Sie **Umgebungen** aus.</span><span class="sxs-lookup"><span data-stu-id="7fb76-108">Select **Environments**.</span></span>
3. <span data-ttu-id="7fb76-109">Wählen Sie die Testversionsumgebung aus, die ein Benennungsmuster hat, das mit diesem vergleichbar ist: TestDrive - alias@domain</span><span class="sxs-lookup"><span data-stu-id="7fb76-109">Select the test drive environment, which has a naming pattern similar to this: TestDrive - alias@domain</span></span>
4. <span data-ttu-id="7fb76-110">Wählen Sie **Löschen** aus, und bestätigen Sie die Entscheidung.</span><span class="sxs-lookup"><span data-stu-id="7fb76-110">Select **Delete** and confirm the decision.</span></span> 

<span data-ttu-id="7fb76-111">Die vorhandene Testversionsumgebung wird entfernt.</span><span class="sxs-lookup"><span data-stu-id="7fb76-111">The existing test drive environment will be removed.</span></span> <span data-ttu-id="7fb76-112">Wenn sie entfernt wird, können Sie sich für eine neue Testversionsumgebung anmelden.</span><span class="sxs-lookup"><span data-stu-id="7fb76-112">When it is removed, you can sign up for a new test drive environment.</span></span> 

## <a name="remove-a-production-environment"></a><span data-ttu-id="7fb76-113">Produktionsumgebung entfernen</span><span class="sxs-lookup"><span data-stu-id="7fb76-113">Remove a production environment</span></span>

<span data-ttu-id="7fb76-114">Für diesen Artikel wird vorausgesetzt, dass Sie Human Resources über einen Cloud-Lösungsanbieter (CSP) oder eine Unternehmensarchitekturvereinbarung erworben haben.</span><span class="sxs-lookup"><span data-stu-id="7fb76-114">This article assumes that you've purchased Human Resources through a Cloud Solution Provider (CSP) or an enterprise architecture (EA) agreement.</span></span> 

<span data-ttu-id="7fb76-115">Da eine einzelne Human Resources-Umgebung innerhalb einer einzelnen Power Apps-Umgebung „enthalten“ ist, sind zwei Optionen zu bedenken.</span><span class="sxs-lookup"><span data-stu-id="7fb76-115">Since a single Human Resources environment is contained within a single Power Apps environment, there are two options to consider.</span></span> <span data-ttu-id="7fb76-116">Die erste Option entfernt die gesamte Power Apps-Umgebung, die zweite Option entfernt nur Human Resources.</span><span class="sxs-lookup"><span data-stu-id="7fb76-116">The first option involves removing the entire Power Apps environment; the second option involves removing only Human Resources.</span></span> <span data-ttu-id="7fb76-117">Die erste Option wird bevorzugt, wenn Sie eine Power Apps-Umgebung speziell für den Zweck der Bereitstellung von Human Resources erstellt haben und wenn Sie gerade erst mit der Implementierung begonnen haben oder wenn Sie keine eingerichteten Integrationen haben.</span><span class="sxs-lookup"><span data-stu-id="7fb76-117">The first option is preferred when you have created a Power Apps environment expressly for the purpose of provisioning Human Resources, and you've just begun implementation, or you don’t have any established integrations.</span></span> <span data-ttu-id="7fb76-118">Die zweite Option ist sinnvoll, wenn Sie eine etablierte Power Apps-Umgebung mit umfangreichen Daten haben, die in Power Apps und Power Automate genutzt wird.</span><span class="sxs-lookup"><span data-stu-id="7fb76-118">The second option is appropriate when you have an established Power Apps environment populated with rich data that's leveraged in Power Apps and Power Automate.</span></span>

> [!Important]
> <span data-ttu-id="7fb76-119">Bevor Sie die Power Apps-Umgebung entfernen, stellen Sie sicher, dass sie nicht für Ihr Datenintegrationen außerhalb der Bereich von Human Resources verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7fb76-119">Before removing the Power Apps environment, ensure it is not being used for rich data integrations outside the scope of Human Resources.</span></span> <span data-ttu-id="7fb76-120">Standardmäßig kann die Power Apps-Umgebung nicht entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="7fb76-120">Also note that the default Power Apps environments cannot be removed.</span></span> 

<span data-ttu-id="7fb76-121">So entfernen Sie die gesamte Power Apps-Umgebung, einschließlich Human Resources und zugehörige Anwendungen und Flows:</span><span class="sxs-lookup"><span data-stu-id="7fb76-121">To remove the entire Power Apps environment, including Human Resources and the associated apps and flows:</span></span>

1. <span data-ttu-id="7fb76-122">Zum [Power Apps Admin Center](https://admin.businessplatform.microsoft.com/) navigieren.</span><span class="sxs-lookup"><span data-stu-id="7fb76-122">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="7fb76-123">Wählen Sie **Umgebungen** aus.</span><span class="sxs-lookup"><span data-stu-id="7fb76-123">Select **Environments**.</span></span>
3. <span data-ttu-id="7fb76-124">Wählen Sie die zu entfernende Umgebung aus.</span><span class="sxs-lookup"><span data-stu-id="7fb76-124">Select the environment to be removed.</span></span>
4. <span data-ttu-id="7fb76-125">Wählen Sie **Löschen** aus, und bestätigen Sie die Entscheidung.</span><span class="sxs-lookup"><span data-stu-id="7fb76-125">Select **Delete** and confirm the decision.</span></span> 
5. <span data-ttu-id="7fb76-126">Warten Sie, bis der Löschvorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="7fb76-126">Wait until the deletion is complete.</span></span>
6. <span data-ttu-id="7fb76-127">Melden Sie sich an bei [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS), indem Sie das Konto verwenden, das Sie verwendet haben, um Human Resources zu abonnieren.</span><span class="sxs-lookup"><span data-stu-id="7fb76-127">Sign in to [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) using the account that you used to subscribe to Human Resources.</span></span> 
7. <span data-ttu-id="7fb76-128">Wählen Sie das Human Resources-Projekt aus, das die Umgebung enthält.</span><span class="sxs-lookup"><span data-stu-id="7fb76-128">Select the Human Resources Project that contains the environment.</span></span> 
8. <span data-ttu-id="7fb76-129">In Ihrem LCS-Projekt wählen Sie die Kachel **Human Resources App-Verwaltung** aus.</span><span class="sxs-lookup"><span data-stu-id="7fb76-129">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
9. <span data-ttu-id="7fb76-130">Wählen Sie die zu entfernende Instanz aus.</span><span class="sxs-lookup"><span data-stu-id="7fb76-130">Select the instance to remove.</span></span> 
10. <span data-ttu-id="7fb76-131">Wählen Sie **Instanz entfernen** aus, und bestätigen Sie Ihre Entscheidung.</span><span class="sxs-lookup"><span data-stu-id="7fb76-131">Select **Remove instance** and confirm your decision.</span></span>  

<span data-ttu-id="7fb76-132">Um eine Human Resources-Umgebung aus einer vorhandenen Power Apps-Umgebung zu entfernen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="7fb76-132">To remove a Human Resources environment from an existing Power Apps environment, complete the following steps.</span></span> <span data-ttu-id="7fb76-133">Beachten Sie, dass die Anforderung, Support einzubeziehen und das Human Resources DevOps-Team zu kontaktieren temporär ist, nachdem diese Funktion direkt in LCS aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="7fb76-133">Note that the need to involve support and contact the Human Resources DevOps team is temporary until this feature is enabled directly in LCS.</span></span>

1. <span data-ttu-id="7fb76-134">Kontaktaufnahme von Support, um eine Entfernung einer Anforderung zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="7fb76-134">Contact Support to initiate a removal request.</span></span>
2. <span data-ttu-id="7fb76-135">Das Supportteam initiiert eine Entfernungsanforderung mit dem Human Resources DevOps-Team.</span><span class="sxs-lookup"><span data-stu-id="7fb76-135">The Support team will initiate a removal request with the Human Resources DevOps team.</span></span> 
3. <span data-ttu-id="7fb76-136">Fahren Sie fort, nachdem Sie wissen, dass die Umgebung entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="7fb76-136">Continue after you receive word that the environment has been removed.</span></span>
4.  <span data-ttu-id="7fb76-137">Melden Sie sich an bei LCS indem Sie das Konto verwenden, das Sie verwenden, um Human Resources zu abonnieren.</span><span class="sxs-lookup"><span data-stu-id="7fb76-137">Sign in to LCS using the account that you used to subscribe to Human Resources.</span></span> 
5. <span data-ttu-id="7fb76-138">Wählen Sie das Human Resources-Projekt aus, das die Umgebung enthält.</span><span class="sxs-lookup"><span data-stu-id="7fb76-138">Select the Human Resources project that contains the environment.</span></span> 
6. <span data-ttu-id="7fb76-139">In Ihrem LCS-Projekt wählen Sie die Kachel **Human Resources App-Verwaltung** aus.</span><span class="sxs-lookup"><span data-stu-id="7fb76-139">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
7. <span data-ttu-id="7fb76-140">Wählen Sie die Instanz aus, die Sie entfernen möchten, die mit dem Bereitstellungsstatus **Fehler** markiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="7fb76-140">Select the instance you would like to remove, which should be marked with a Deployment status of **Failed**.</span></span>
8. <span data-ttu-id="7fb76-141">Wählen Sie **Instanz entfernen** aus, und bestätigen Sie Ihre Entscheidung.</span><span class="sxs-lookup"><span data-stu-id="7fb76-141">Select **Remove instance** and confirm your decision.</span></span> 
