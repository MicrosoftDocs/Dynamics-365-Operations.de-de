---
title: Talent-Umgebungen entfernen
description: Dieses Thema führt Sie durch den Prozess des Entfernens eine Testversions- oder Produktionsumgebung für Microsoft Dynamics 365 Talent.
author: andreabichsel
manager: AnnBe
ms.date: 11/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.openlocfilehash: d608ee3ad90d23279557e5e9be4d398ffac3a266
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/23/2019
ms.locfileid: "2010614"
---
# <a name="remove-talent-environments"></a><span data-ttu-id="1f5ef-103">Talent-Umgebungen entfernen</span><span class="sxs-lookup"><span data-stu-id="1f5ef-103">Remove Talent environments</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1f5ef-104">Dieses Thema führt Sie durch den Prozess des Entfernens eine Testversions- oder Produktionsumgebung für Microsoft Dynamics 365 Talent.</span><span class="sxs-lookup"><span data-stu-id="1f5ef-104">This topic walks you through the process of removing a test drive or production environment for Microsoft Dynamics 365 Talent.</span></span>

## <a name="removing-a-test-drive-environment"></a><span data-ttu-id="1f5ef-105">Entfernen einer Testversionsumgebung</span><span class="sxs-lookup"><span data-stu-id="1f5ef-105">Removing a test drive environment</span></span>

<span data-ttu-id="1f5ef-106">Talent-Testversionen werden mit einer 60-Tage-Ablaufrichtlinie bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="1f5ef-106">Talent test drives are provisioned with a 60-day expiration policy.</span></span> <span data-ttu-id="1f5ef-107">Aber Eigentümer von Testumgebungen haben die Option, ihren Versuch früh zu beenden, indem Sie die folgenden Schritte ausführen.</span><span class="sxs-lookup"><span data-stu-id="1f5ef-107">However, owners of test drive environments have the option to end their trial early by completing the following steps.</span></span> 

1. <span data-ttu-id="1f5ef-108">Zum [PowerApps Admin Center](https://admin.businessplatform.microsoft.com/) navigieren.</span><span class="sxs-lookup"><span data-stu-id="1f5ef-108">Navigate to the [PowerApps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="1f5ef-109">Wählen Sie **Umgebungen** aus.</span><span class="sxs-lookup"><span data-stu-id="1f5ef-109">Select **Environments**.</span></span>
3. <span data-ttu-id="1f5ef-110">Wählen Sie die Testversionsumgebung aus, die ein Benennungsmuster hat, das mit diesem vergleichbar ist: TestDrive - alias@domain</span><span class="sxs-lookup"><span data-stu-id="1f5ef-110">Select the test drive environment, which has a naming pattern similar to this: TestDrive - alias@domain</span></span>
4. <span data-ttu-id="1f5ef-111">Wählen Sie **Löschen** aus, und bestätigen Sie die Entscheidung.</span><span class="sxs-lookup"><span data-stu-id="1f5ef-111">Select **Delete** and confirm the decision.</span></span> 

<span data-ttu-id="1f5ef-112">Die vorhandene Testversionsumgebung wird entfernt.</span><span class="sxs-lookup"><span data-stu-id="1f5ef-112">The existing test drive environment will be removed.</span></span> <span data-ttu-id="1f5ef-113">Wenn sie entfernt wird, können Sie sich für eine neue Testversionsumgebung anmelden.</span><span class="sxs-lookup"><span data-stu-id="1f5ef-113">When it is removed, you can sign up for a new test drive environment.</span></span> 

## <a name="removing-a-production-environment"></a><span data-ttu-id="1f5ef-114">Entfernen einer Produktionsumgebung</span><span class="sxs-lookup"><span data-stu-id="1f5ef-114">Removing a production environment</span></span>

<span data-ttu-id="1f5ef-115">Für dieses Thema wird vorausgesetzt, dass Sie Talent über einen Cloud-Lösungsanbieter (CSP) oder eine Unternehmensarchitekturvereinbarung erworben haben.</span><span class="sxs-lookup"><span data-stu-id="1f5ef-115">This topic assumes that you've purchased Talent through a Cloud Solution Provider (CSP) or an enterprise architecture (EA) agreement.</span></span> 

<span data-ttu-id="1f5ef-116">Da eine einzelne Talent-Umgebung innerhalb einer einzelnen PowerApps-Umgebung „enthalten“ ist, sind zwei Optionen zu bedenken.</span><span class="sxs-lookup"><span data-stu-id="1f5ef-116">Since a single Talent environment is “contained” within a single PowerApps environment, there are two options to consider.</span></span> <span data-ttu-id="1f5ef-117">Die erste Option bezieht entfernt die gesamte PowerApps-Umgebung, die zweite Option entfernt nur Talent.</span><span class="sxs-lookup"><span data-stu-id="1f5ef-117">The first option involves removing the entire PowerApps environment; the second option involves removing only Talent.</span></span> <span data-ttu-id="1f5ef-118">Die erste Option wird bevorzugt, wenn Sie eine PowerApps-Umgebung speziell für den Zweck der Bereitstellung von Talent erstellt haben und wenn Sie gerade erst mit der Implementierung begonnen haben oder wenn Sie keine eingerichteten Integrationen haben.</span><span class="sxs-lookup"><span data-stu-id="1f5ef-118">The first option is preferred when you have created a PowerApps environment expressly for the purpose of provisioning Talent, and you've just begun implementation, or you don’t have any established integrations.</span></span> <span data-ttu-id="1f5ef-119">Die zweite Option ist passend, wenn Sie eine eingerichtete PowerApps-Umgebung haben, die mit aussagekräftigen Daten haben, die in PowerApps und Flows eingesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="1f5ef-119">The second option is appropriate when you have an established PowerApps environment populated with rich data that's leveraged in PowerApps and Flows.</span></span>

> [!Important]
> <span data-ttu-id="1f5ef-120">Bevor Sie die PowerApps-Umgebung entfernen, stellen Sie sicher, dass sie nicht für Ihr Datenintegrationen außerhalb der Bereich des Talents verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1f5ef-120">Before removing the PowerApps environment, ensure it is not being used for rich data integrations outside the scope of Talent.</span></span> <span data-ttu-id="1f5ef-121">Standardmäßig kann die PowerApps-Umgebung nicht entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="1f5ef-121">Also note that the default PowerApps environments cannot be removed.</span></span> 

<span data-ttu-id="1f5ef-122">So entfernen Sie die gesamte PowerApps-Umgebung, einschließlich Talent und den zugeordneten Apps und Flows:</span><span class="sxs-lookup"><span data-stu-id="1f5ef-122">To remove the entire PowerApps environment, including Talent and the associated Apps and Flows:</span></span>

1. <span data-ttu-id="1f5ef-123">Zum [PowerApps Admin Center](https://admin.businessplatform.microsoft.com/) navigieren.</span><span class="sxs-lookup"><span data-stu-id="1f5ef-123">Navigate to the [PowerApps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="1f5ef-124">Wählen Sie **Umgebungen** aus.</span><span class="sxs-lookup"><span data-stu-id="1f5ef-124">Select **Environments**.</span></span>
3. <span data-ttu-id="1f5ef-125">Wählen Sie die zu entfernende Umgebung aus.</span><span class="sxs-lookup"><span data-stu-id="1f5ef-125">Select the environment to be removed.</span></span>
4. <span data-ttu-id="1f5ef-126">Wählen Sie **Löschen** aus, und bestätigen Sie die Entscheidung.</span><span class="sxs-lookup"><span data-stu-id="1f5ef-126">Select **Delete** and confirm the decision.</span></span> 
5. <span data-ttu-id="1f5ef-127">Warten Sie, bis der Löschvorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="1f5ef-127">Wait until the deletion is complete.</span></span>
6. <span data-ttu-id="1f5ef-128">Melden Sie sich an bei [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS), indem Sie das Konto verwenden, das Sie verwendet haben, um Talent zu abonnieren.</span><span class="sxs-lookup"><span data-stu-id="1f5ef-128">Sign in to [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) using the account that you used to subscribe to Talent.</span></span> 
7. <span data-ttu-id="1f5ef-129">Wählen Sie das Talent-Projekt aus, das die Umgebung enthält.</span><span class="sxs-lookup"><span data-stu-id="1f5ef-129">Select the Talent Project that contains the environment.</span></span> 
8. <span data-ttu-id="1f5ef-130">In Ihrem LCS-Projekt wählen Sie die Kachel **Talent App-Verwaltung** aus.</span><span class="sxs-lookup"><span data-stu-id="1f5ef-130">In your LCS project, select the **Talent App Management** tile.</span></span> 
9. <span data-ttu-id="1f5ef-131">Wählen Sie die zu entfernende Instanz aus.</span><span class="sxs-lookup"><span data-stu-id="1f5ef-131">Select the instance to remove.</span></span> 
10. <span data-ttu-id="1f5ef-132">Wählen Sie **Instanz entfernen** aus, und bestätigen Sie Ihre Entscheidung.</span><span class="sxs-lookup"><span data-stu-id="1f5ef-132">Select **Remove instance** and confirm your decision.</span></span>  

<span data-ttu-id="1f5ef-133">Um eine Talent-Umgebung aus einer vorhandenen PowerApps-Umgebung zu entfernen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="1f5ef-133">To remove a Talent environment from an existing PowerApps environment, complete the following steps.</span></span> <span data-ttu-id="1f5ef-134">Beachten Sie, dass die Anforderung, Support einzubeziehen und das Talent DevOps-Team zu kontaktieren temporär ist, nachdem diese Funktion direkt in Kreditbriefen aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="1f5ef-134">Note that the need to involve support and contact the Talent DevOps team is temporary until this feature is enabled directly in LCS.</span></span>

1. <span data-ttu-id="1f5ef-135">Kontaktaufnahme von Support, um eine Entfernung einer Anforderung zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="1f5ef-135">Contact Support to initiate a removal request.</span></span>
2. <span data-ttu-id="1f5ef-136">Das Supportteam initiiert eine Entfernungsanforderung mit dem Talent DevOps-Team.</span><span class="sxs-lookup"><span data-stu-id="1f5ef-136">The Support team will initiate a removal request with the Talent DevOps team.</span></span> 
3. <span data-ttu-id="1f5ef-137">Fahren Sie fort, nachdem Sie wissen, dass die Umgebung entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="1f5ef-137">Continue after you receive word that the environment has been removed.</span></span>
4.  <span data-ttu-id="1f5ef-138">Melden Sie sich bei LCS an, indem Sie das Konto verwenden, das Sie verwendet haben, um Talent zu abonnieren.</span><span class="sxs-lookup"><span data-stu-id="1f5ef-138">Sign in to LCS using the account that you used to subscribe to Talent.</span></span> 
5. <span data-ttu-id="1f5ef-139">Wählen Sie das Talent-Projekt aus, das die Umgebung enthält.</span><span class="sxs-lookup"><span data-stu-id="1f5ef-139">Select the Talent project that contains the environment.</span></span> 
6. <span data-ttu-id="1f5ef-140">In Ihrem LCS-Projekt wählen Sie die Kachel **Talent App-Verwaltung** aus.</span><span class="sxs-lookup"><span data-stu-id="1f5ef-140">In your LCS project, select the **Talent App Management** tile.</span></span> 
7. <span data-ttu-id="1f5ef-141">Wählen Sie die Instanz aus, die Sie entfernen möchten, die mit dem Bereitstellungsstatus **Fehler** markiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="1f5ef-141">Select the instance you would like to remove, which should be marked with a Deployment status of **Failed**.</span></span>
8. <span data-ttu-id="1f5ef-142">Wählen Sie **Instanz entfernen** aus, und bestätigen Sie Ihre Entscheidung.</span><span class="sxs-lookup"><span data-stu-id="1f5ef-142">Select **Remove instance** and confirm your decision.</span></span> 

