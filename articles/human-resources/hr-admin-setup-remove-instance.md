---
title: Eine Instanz entfernen
description: Diese Artikel führt Sie durch den Prozess des Entfernens eine Testversions- oder Produktionsumgebung für Microsoft Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 08/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 399c710b99c5721ff9867ce332b815bd362d6103
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795020"
---
# <a name="remove-an-instance"></a><span data-ttu-id="2f03c-103">Eine Instanz entfernen</span><span class="sxs-lookup"><span data-stu-id="2f03c-103">Remove an instance</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="2f03c-104">Diese Artikel führt Sie durch den Prozess des Entfernens eine Testversions- oder Produktionsumgebung für Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="2f03c-104">This article walks you through the process of removing a test drive or production environment for Microsoft Dynamics 365 Human Resources.</span></span>

## <a name="remove-a-test-drive-environment"></a><span data-ttu-id="2f03c-105">Testversionsumgebung entfernen</span><span class="sxs-lookup"><span data-stu-id="2f03c-105">Remove a test drive environment</span></span>

<span data-ttu-id="2f03c-106">Human Resources-Testversionen werden mit einer 60-Tage-Ablaufrichtlinie bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="2f03c-106">Human Resources test drives are provisioned with a 60-day expiration policy.</span></span> <span data-ttu-id="2f03c-107">Aber Eigentümer von Testumgebungen haben die Option, ihren Versuch früh zu beenden, indem Sie die folgenden Schritte ausführen.</span><span class="sxs-lookup"><span data-stu-id="2f03c-107">However, owners of test drive environments have the option to end their trial early by completing the following steps.</span></span> 

1. <span data-ttu-id="2f03c-108">Zum [Power Apps Admin Center](https://admin.businessplatform.microsoft.com/) navigieren.</span><span class="sxs-lookup"><span data-stu-id="2f03c-108">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="2f03c-109">Wählen Sie **Umgebungen** aus.</span><span class="sxs-lookup"><span data-stu-id="2f03c-109">Select **Environments**.</span></span>
3. <span data-ttu-id="2f03c-110">Wählen Sie die Testversionsumgebung aus, die ein Benennungsmuster hat, das mit diesem vergleichbar ist: TestDrive - alias@domain</span><span class="sxs-lookup"><span data-stu-id="2f03c-110">Select the test drive environment, which has a naming pattern similar to this: TestDrive - alias@domain</span></span>
4. <span data-ttu-id="2f03c-111">Wählen Sie **Löschen** aus, und bestätigen Sie die Entscheidung.</span><span class="sxs-lookup"><span data-stu-id="2f03c-111">Select **Delete** and confirm the decision.</span></span> 

<span data-ttu-id="2f03c-112">Die vorhandene Testversionsumgebung wird entfernt.</span><span class="sxs-lookup"><span data-stu-id="2f03c-112">The existing test drive environment will be removed.</span></span> <span data-ttu-id="2f03c-113">Wenn sie entfernt wird, können Sie sich für eine neue Testversionsumgebung anmelden.</span><span class="sxs-lookup"><span data-stu-id="2f03c-113">When it is removed, you can sign up for a new test drive environment.</span></span> 

## <a name="remove-a-production-environment"></a><span data-ttu-id="2f03c-114">Produktionsumgebung entfernen</span><span class="sxs-lookup"><span data-stu-id="2f03c-114">Remove a production environment</span></span>

<span data-ttu-id="2f03c-115">Für diesen Artikel wird vorausgesetzt, dass Sie Human Resources über einen Cloud-Lösungsanbieter (CSP) oder eine Unternehmensarchitekturvereinbarung erworben haben.</span><span class="sxs-lookup"><span data-stu-id="2f03c-115">This article assumes that you've purchased Human Resources through a Cloud Solution Provider (CSP) or an enterprise architecture (EA) agreement.</span></span> 

<span data-ttu-id="2f03c-116">Da eine einzelne Human Resources-Umgebung innerhalb einer einzelnen Power Apps-Umgebung „enthalten“ ist, sind zwei Optionen zu bedenken.</span><span class="sxs-lookup"><span data-stu-id="2f03c-116">Since a single Human Resources environment is contained within a single Power Apps environment, there are two options to consider.</span></span> <span data-ttu-id="2f03c-117">Die erste Option entfernt die gesamte Power Apps-Umgebung, die zweite Option entfernt nur Human Resources.</span><span class="sxs-lookup"><span data-stu-id="2f03c-117">The first option involves removing the entire Power Apps environment; the second option involves removing only Human Resources.</span></span> <span data-ttu-id="2f03c-118">Die erste Option wird bevorzugt, wenn Sie eine Power Apps-Umgebung speziell für den Zweck der Bereitstellung von Human Resources erstellt haben und wenn Sie gerade erst mit der Implementierung begonnen haben oder wenn Sie keine eingerichteten Integrationen haben.</span><span class="sxs-lookup"><span data-stu-id="2f03c-118">The first option is preferred when you have created a Power Apps environment expressly for the purpose of provisioning Human Resources, and you've just begun implementation, or you don’t have any established integrations.</span></span> <span data-ttu-id="2f03c-119">Die zweite Option ist sinnvoll, wenn Sie eine etablierte Power Apps-Umgebung mit umfangreichen Daten haben, die in Power Apps und Power Automate genutzt wird.</span><span class="sxs-lookup"><span data-stu-id="2f03c-119">The second option is appropriate when you have an established Power Apps environment populated with rich data that's leveraged in Power Apps and Power Automate.</span></span>

> [!Important]
> <span data-ttu-id="2f03c-120">Bevor Sie die Power Apps-Umgebung entfernen, stellen Sie sicher, dass sie nicht für Ihr Datenintegrationen außerhalb der Bereich von Human Resources verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2f03c-120">Before removing the Power Apps environment, ensure it is not being used for rich data integrations outside the scope of Human Resources.</span></span> <span data-ttu-id="2f03c-121">Standardmäßig kann die Power Apps-Umgebung nicht entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="2f03c-121">Also note that the default Power Apps environments cannot be removed.</span></span> 

<span data-ttu-id="2f03c-122">So entfernen Sie die gesamte Power Apps-Umgebung, einschließlich Human Resources und zugehörige Anwendungen und Flows:</span><span class="sxs-lookup"><span data-stu-id="2f03c-122">To remove the entire Power Apps environment, including Human Resources and the associated apps and flows:</span></span>

1. <span data-ttu-id="2f03c-123">Zum [Power Apps Admin Center](https://admin.businessplatform.microsoft.com/) navigieren.</span><span class="sxs-lookup"><span data-stu-id="2f03c-123">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="2f03c-124">Wählen Sie **Umgebungen** aus.</span><span class="sxs-lookup"><span data-stu-id="2f03c-124">Select **Environments**.</span></span>
3. <span data-ttu-id="2f03c-125">Wählen Sie die zu entfernende Umgebung aus.</span><span class="sxs-lookup"><span data-stu-id="2f03c-125">Select the environment to be removed.</span></span>
4. <span data-ttu-id="2f03c-126">Wählen Sie **Löschen** aus, und bestätigen Sie die Entscheidung.</span><span class="sxs-lookup"><span data-stu-id="2f03c-126">Select **Delete** and confirm the decision.</span></span> 
5. <span data-ttu-id="2f03c-127">Warten Sie, bis der Löschvorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="2f03c-127">Wait until the deletion is complete.</span></span>
6. <span data-ttu-id="2f03c-128">Melden Sie sich an bei [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS), indem Sie das Konto verwenden, das Sie verwendet haben, um Human Resources zu abonnieren.</span><span class="sxs-lookup"><span data-stu-id="2f03c-128">Sign in to [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) using the account that you used to subscribe to Human Resources.</span></span> 
7. <span data-ttu-id="2f03c-129">Wählen Sie das Human Resources-Projekt aus, das die Umgebung enthält.</span><span class="sxs-lookup"><span data-stu-id="2f03c-129">Select the Human Resources Project that contains the environment.</span></span> 
8. <span data-ttu-id="2f03c-130">In Ihrem LCS-Projekt wählen Sie die Kachel **Human Resources App-Verwaltung** aus.</span><span class="sxs-lookup"><span data-stu-id="2f03c-130">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
9. <span data-ttu-id="2f03c-131">Wählen Sie die zu entfernende Instanz aus.</span><span class="sxs-lookup"><span data-stu-id="2f03c-131">Select the instance to remove.</span></span> 
10. <span data-ttu-id="2f03c-132">Wählen Sie **Instanz entfernen** aus, und bestätigen Sie Ihre Entscheidung.</span><span class="sxs-lookup"><span data-stu-id="2f03c-132">Select **Remove instance** and confirm your decision.</span></span>  

<span data-ttu-id="2f03c-133">Um eine Human Resources-Umgebung aus einer vorhandenen Power Apps-Umgebung zu entfernen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="2f03c-133">To remove a Human Resources environment from an existing Power Apps environment, complete the following steps.</span></span> <span data-ttu-id="2f03c-134">Beachten Sie, dass die Anforderung, Support einzubeziehen und das Human Resources DevOps-Team zu kontaktieren temporär ist, nachdem diese Funktion direkt in LCS aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="2f03c-134">Note that the need to involve support and contact the Human Resources DevOps team is temporary until this feature is enabled directly in LCS.</span></span>

1. <span data-ttu-id="2f03c-135">Kontaktaufnahme von Support, um eine Entfernung einer Anforderung zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="2f03c-135">Contact Support to initiate a removal request.</span></span>
2. <span data-ttu-id="2f03c-136">Das Supportteam initiiert eine Entfernungsanforderung mit dem Human Resources DevOps-Team.</span><span class="sxs-lookup"><span data-stu-id="2f03c-136">The Support team will initiate a removal request with the Human Resources DevOps team.</span></span> 
3. <span data-ttu-id="2f03c-137">Fahren Sie fort, nachdem Sie wissen, dass die Umgebung entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="2f03c-137">Continue after you receive word that the environment has been removed.</span></span>
4. <span data-ttu-id="2f03c-138">Melden Sie sich an bei LCS indem Sie das Konto verwenden, das Sie verwenden, um Human Resources zu abonnieren.</span><span class="sxs-lookup"><span data-stu-id="2f03c-138">Sign in to LCS using the account that you used to subscribe to Human Resources.</span></span> 
5. <span data-ttu-id="2f03c-139">Wählen Sie das Human Resources-Projekt aus, das die Umgebung enthält.</span><span class="sxs-lookup"><span data-stu-id="2f03c-139">Select the Human Resources project that contains the environment.</span></span> 
6. <span data-ttu-id="2f03c-140">In Ihrem LCS-Projekt wählen Sie die Kachel **Human Resources App-Verwaltung** aus.</span><span class="sxs-lookup"><span data-stu-id="2f03c-140">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
7. <span data-ttu-id="2f03c-141">Wählen Sie die Instanz aus, die Sie entfernen möchten, die mit dem Bereitstellungsstatus **Gelöscht** markiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="2f03c-141">Select the instance you would like to remove, which should be marked with a Deployment status of **Deleted**.</span></span>
8. <span data-ttu-id="2f03c-142">Wählen Sie **Instanz entfernen** aus, und bestätigen Sie Ihre Entscheidung.</span><span class="sxs-lookup"><span data-stu-id="2f03c-142">Select **Remove instance** and confirm your decision.</span></span> 

## <a name="recover-a-soft-deleted-environment"></a><span data-ttu-id="2f03c-143">Eine nicht vollständig gelöschte Umgebung wiederherstellen</span><span class="sxs-lookup"><span data-stu-id="2f03c-143">Recover a soft-deleted environment</span></span>

<span data-ttu-id="2f03c-144">Wenn Sie die Power Apps Umgebung, mit der Ihre Human-Ressources-Umgebung verbunden ist, löschen, lautet der Status der Human-Ressources-Umgebung in Lifecycle Services **weich gelöscht**.</span><span class="sxs-lookup"><span data-stu-id="2f03c-144">If you delete the Power Apps environment that your Human Resources environment is connected to, the status of the Human Resources environment in Lifecycle Services will be **Soft deleted**.</span></span> <span data-ttu-id="2f03c-145">In diesem Fall können Benutzer keine Verbindung zu Human Ressources herstellen.</span><span class="sxs-lookup"><span data-stu-id="2f03c-145">In this case, users can't connect to Human Resources.</span></span>

<span data-ttu-id="2f03c-146">So stellen Sie die Umgebung wieder her:</span><span class="sxs-lookup"><span data-stu-id="2f03c-146">To restore the environment:</span></span>

1. <span data-ttu-id="2f03c-147">Folgen Sie den Anweisungen unter [Die Power Apps Umgebung wiederherstellen](/power-platform/admin/recover-environment.md).</span><span class="sxs-lookup"><span data-stu-id="2f03c-147">Follow the instructions in [Recover the Power Apps environment](/power-platform/admin/recover-environment.md).</span></span>

2. <span data-ttu-id="2f03c-148">Wenden Sie sich an den Support, um die Human-Resources-Umgebung wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="2f03c-148">Contact Support to restore the Human Resources environment.</span></span> <span data-ttu-id="2f03c-149">Weitere Informationen erhalten Sie über den [Support](hr-admin-troubleshooting-support.md).</span><span class="sxs-lookup"><span data-stu-id="2f03c-149">For more information, see [Get support](hr-admin-troubleshooting-support.md).</span></span>

> [!Warning]
> <span data-ttu-id="2f03c-150">Power Apps Umgebungen werden nach dem Löschen nur sieben Tage lang gespeichert.</span><span class="sxs-lookup"><span data-stu-id="2f03c-150">Power Apps environments are only saved for seven days after deletion.</span></span> <span data-ttu-id="2f03c-151">Sie müssen die Umgebung innerhalb dieser sieben Tage wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="2f03c-151">You must recover the environment within the seven day period.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]