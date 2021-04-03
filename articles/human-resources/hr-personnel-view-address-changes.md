---
title: Adressänderungen anzeigen und verwalten
description: In diesem Thema wird erläutert, wie Sie Adressänderungen in Dynamics 365 Human Resources anzeigen und verwalten können.
author: andreabichsel
manager: tfehr
ms.date: 08/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-08-07
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 27324b7705fe37ab00e169e8ea05c7768f32b120
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467336"
---
# <a name="view-and-manage-address-changes"></a><span data-ttu-id="6b93e-103">Adressänderungen anzeigen und verwalten</span><span class="sxs-lookup"><span data-stu-id="6b93e-103">View and manage address changes</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="6b93e-104">In diesem Thema wird erläutert, wie Sie Adressänderungen auf der Mitarbeiter-Self-Service-Seite **Persönliche Daten bearbeiten** oder der Detailseite **Arbeitskraft** in Dynamics 365 Human Resources anzeigen und verwalten können.</span><span class="sxs-lookup"><span data-stu-id="6b93e-104">This topic explains how you can view and manage address changes in the Employee self-service **Edit personal details** page or the **Worker** details page in Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="6b93e-105">Viele Unternehmen möchten, dass Mitarbeiter ihre persönlichen Daten über einen Self-Service verwalten.</span><span class="sxs-lookup"><span data-stu-id="6b93e-105">Many organizations want employees to manage their own personal details through a self-service experience.</span></span> <span data-ttu-id="6b93e-106">Sie können Benutzern erlauben, ihre Adresse im Arbeitsbereich **Mitarbeiter-Self-Service** zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="6b93e-106">You can allow users to update their address in the **Employee self service** workspace.</span></span> <span data-ttu-id="6b93e-107">Sie können diese Änderungen dann im Arbeitsbereich **Personalverwaltung** überwachen.</span><span class="sxs-lookup"><span data-stu-id="6b93e-107">You can then monitor these changes in the **Personnel management** workspace.</span></span> <span data-ttu-id="6b93e-108">Sie müssen die Anzahl der Tage angeben, an denen Sie Änderungen auf der Seite **Personalverwaltungsparameter** anzeigen möchten, um diese Funktion nutzen zu können.</span><span class="sxs-lookup"><span data-stu-id="6b93e-108">To use this feature, you must specify the number of days that you want to view changes in the **Human resources parameters** page.</span></span>

## <a name="configure-address-change-parameters"></a><span data-ttu-id="6b93e-109">Adressänderungsparameter konfigurieren</span><span class="sxs-lookup"><span data-stu-id="6b93e-109">Configure address change parameters</span></span>

<span data-ttu-id="6b93e-110">Führen Sie die folgenden Schritte aus, um die Anzahl der Tage, an denen Adressänderungen im Arbeitsbereich **Personalverwaltung** konfiguriert werden sollen, zu konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="6b93e-110">To configure the number of days that you want address changes to appear in the **Personnel management** workspace, follow these steps:</span></span>

1. <span data-ttu-id="6b93e-111">Wählen Sie im Navigationsbereich **Personalverwaltung** aus.</span><span class="sxs-lookup"><span data-stu-id="6b93e-111">On the navigation pane, select **Personnel management**.</span></span>

2. <span data-ttu-id="6b93e-112">Wählen Sie **Links** aus.</span><span class="sxs-lookup"><span data-stu-id="6b93e-112">Select **Links**.</span></span>

3. <span data-ttu-id="6b93e-113">Wählen Sie **Personalverwaltungsparameter** aus.</span><span class="sxs-lookup"><span data-stu-id="6b93e-113">Select **Human resources parameters**.</span></span>

4. <span data-ttu-id="6b93e-114">Geben Sie im Feld **Anzahl der Tage** unter **Adressänderung** die Anzahl der Tage ein, an denen Adressänderungen im Arbeitsbereich **Personalverwaltung** angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6b93e-114">In the **Number of days** field under **Address change**, enter the number of days that you want address changes to appear in the **Personnel management** workspace.</span></span>

5. <span data-ttu-id="6b93e-115">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="6b93e-115">Close the page.</span></span>

## <a name="create-or-change-an-employee-address"></a><span data-ttu-id="6b93e-116">Eine Mitarbeiteradresse erstellen oder ändern</span><span class="sxs-lookup"><span data-stu-id="6b93e-116">Create or change an employee address</span></span>

<span data-ttu-id="6b93e-117">Mitarbeiter können ihre eigene Adresse im Arbeitsbereich **Mitarbeiter-Self-Service** aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="6b93e-117">Employees can update their own address in the **Employee self service** workspace.</span></span> <span data-ttu-id="6b93e-118">Gehen Sie folgendermaßen vor, um eine Adresse zu erstellen oder zu ändern:</span><span class="sxs-lookup"><span data-stu-id="6b93e-118">Follow these steps to create or change an address:</span></span>

1. <span data-ttu-id="6b93e-119">Wählen Sie auf Ihrer Startseite die Kachel **Mitarbeiter-Self-Service** aus.</span><span class="sxs-lookup"><span data-stu-id="6b93e-119">Select the **Employee self-service** tile on your home page.</span></span>

2. <span data-ttu-id="6b93e-120">Wählen Sie **Persönliche Daten bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="6b93e-120">Select **Edit personal details**.</span></span>

3. <span data-ttu-id="6b93e-121">Wählen Sie **Hinzufügen** aus, um eine Adresse hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="6b93e-121">To add an address, select **Add**.</span></span> <span data-ttu-id="6b93e-122">Um eine vorhandene Adresse zu aktualisieren, wählen Sie die Adresse aus der Liste aus, und klicken Sie dann auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="6b93e-122">To update an existing address, select the address from the list and then select **Edit**.</span></span>

4. <span data-ttu-id="6b93e-123">Geben Sie den **Namen oder die Beschreibung** ein.</span><span class="sxs-lookup"><span data-stu-id="6b93e-123">Enter the **Name or description**.</span></span>

5. <span data-ttu-id="6b93e-124">Wählen Sie das Dropdownfeld **Zweck** und dann den Adresstyp aus.</span><span class="sxs-lookup"><span data-stu-id="6b93e-124">Select the **Purpose** drop-down box and then select the type of address.</span></span>

6. <span data-ttu-id="6b93e-125">Füllen Sie **Land/Region** aus.</span><span class="sxs-lookup"><span data-stu-id="6b93e-125">Enter the **Country/region**.</span></span>

7. <span data-ttu-id="6b93e-126">Geben Sie die **Postleitzahl** ein.</span><span class="sxs-lookup"><span data-stu-id="6b93e-126">Enter the **ZIP/postal code**.</span></span>

8. <span data-ttu-id="6b93e-127">Geben Sie die **Straße** ein.</span><span class="sxs-lookup"><span data-stu-id="6b93e-127">Enter the **Street**.</span></span>

9. <span data-ttu-id="6b93e-128">Geben Sie die **Stadt**, den **Staat** und den **Bezirk** ein.</span><span class="sxs-lookup"><span data-stu-id="6b93e-128">Enter the **City**, **State**, and **County**.</span></span> <span data-ttu-id="6b93e-129">In der Regel werden diese Felder automatisch basierend auf dem Feld **Postleitzahl** ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="6b93e-129">Typically, these fields are automatically set based on the **ZIP/postal code** field.</span></span>

10. <span data-ttu-id="6b93e-130">Wählen Sie optional das Feld **Primär** aus, um anzugeben, dass es sich um eine primäre Adresse handelt.</span><span class="sxs-lookup"><span data-stu-id="6b93e-130">Optionally, select the **Primary** field to indicate a primary address.</span></span> <span data-ttu-id="6b93e-131">Es kann nur eine Adresse als primäre Adresse markiert werden.</span><span class="sxs-lookup"><span data-stu-id="6b93e-131">Only one address can be marked as the primary.</span></span> <span data-ttu-id="6b93e-132">Wenn bereits eine andere Adresse als primäre Adresse markiert ist, müssen Sie bestätigen, dass Sie diese Adresse als primäre Adresse verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="6b93e-132">If another address is already marked as the primary address, you'll need to confirm that you want to use this address as the primary.</span></span>

11. <span data-ttu-id="6b93e-133">Wählen Sie optional das Feld **Privat** aus, um anzugeben, dass es sich um eine private Adresse handelt.</span><span class="sxs-lookup"><span data-stu-id="6b93e-133">Optionally, select the **Private** field to indicate that the address is private.</span></span> <span data-ttu-id="6b93e-134">Nur Benutzer mit ausdrücklicher Berechtigung zum Anzeigen privater Adressinformationen können diese Adresse anzeigen.</span><span class="sxs-lookup"><span data-stu-id="6b93e-134">Only users with explicit permission to view private address information can view this address.</span></span>

12. <span data-ttu-id="6b93e-135">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="6b93e-135">Select **OK**.</span></span>

## <a name="create-or-change-a-worker-address"></a><span data-ttu-id="6b93e-136">Eine Arbeitskraftadresse erstellen oder ändern</span><span class="sxs-lookup"><span data-stu-id="6b93e-136">Create or change a worker address</span></span>

<span data-ttu-id="6b93e-137">Sie können eine Adresse im Arbeitsbereich **Personalverwaltung** aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="6b93e-137">You can update an address in the **Personnel management** workspace.</span></span> <span data-ttu-id="6b93e-138">Gehen Sie folgendermaßen vor, um eine Adresse zu erstellen oder zu ändern:</span><span class="sxs-lookup"><span data-stu-id="6b93e-138">Follow these steps to create or change an address:</span></span>

1. <span data-ttu-id="6b93e-139">Wählen Sie im Arbeitsbereich **Personalverwaltung** **Links** und dann **Arbeitskräfte** aus.</span><span class="sxs-lookup"><span data-stu-id="6b93e-139">In the **Personnel management** workspace, select **Links**, and then select **Workers**.</span></span>

3. <span data-ttu-id="6b93e-140">Wählen Sie die Arbeitskraft aus, und klicken Sie anschließend auf **Adressen**.</span><span class="sxs-lookup"><span data-stu-id="6b93e-140">Select the worker, and then select **Addresses**.</span></span>

3. <span data-ttu-id="6b93e-141">Wählen Sie **Hinzufügen** aus, um eine Adresse hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="6b93e-141">To add an address, select **Add**.</span></span> <span data-ttu-id="6b93e-142">Um eine vorhandene Adresse zu aktualisieren, wählen Sie die Adresse aus der Liste aus, und klicken Sie dann auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="6b93e-142">To update an existing address, select the address from the list and then select **Edit**.</span></span>

4. <span data-ttu-id="6b93e-143">Geben Sie den **Namen oder die Beschreibung** ein.</span><span class="sxs-lookup"><span data-stu-id="6b93e-143">Enter the **Name or description**.</span></span>

5. <span data-ttu-id="6b93e-144">Wählen Sie das Dropdownfeld **Zweck** und dann den Adresstyp aus.</span><span class="sxs-lookup"><span data-stu-id="6b93e-144">Select the **Purpose** drop-down box and then select the type of address.</span></span>

6. <span data-ttu-id="6b93e-145">Füllen Sie **Land/Region** aus.</span><span class="sxs-lookup"><span data-stu-id="6b93e-145">Enter the **Country/region**.</span></span>

7. <span data-ttu-id="6b93e-146">Geben Sie die **Postleitzahl** ein.</span><span class="sxs-lookup"><span data-stu-id="6b93e-146">Enter the **ZIP/postal code**.</span></span>

8. <span data-ttu-id="6b93e-147">Geben Sie die **Straße** ein.</span><span class="sxs-lookup"><span data-stu-id="6b93e-147">Enter the **Street**.</span></span>

9. <span data-ttu-id="6b93e-148">Geben Sie die **Stadt**, den **Staat** und den **Bezirk** ein.</span><span class="sxs-lookup"><span data-stu-id="6b93e-148">Enter the **City**, **State**, and **County**.</span></span> <span data-ttu-id="6b93e-149">In der Regel werden diese Felder automatisch basierend auf dem Feld **Postleitzahl** ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="6b93e-149">Typically, these fields are automatically set based on the **ZIP/postal code** field.</span></span>

10. <span data-ttu-id="6b93e-150">Wählen Sie optional das Feld **Primär** aus, um anzugeben, dass es sich um eine primäre Adresse handelt.</span><span class="sxs-lookup"><span data-stu-id="6b93e-150">Optionally, select the **Primary** field to indicate a primary address.</span></span> <span data-ttu-id="6b93e-151">Es kann nur eine Adresse als primäre Adresse markiert werden.</span><span class="sxs-lookup"><span data-stu-id="6b93e-151">Only one address can be marked as the primary.</span></span> <span data-ttu-id="6b93e-152">Wenn bereits eine andere Adresse als primäre Adresse markiert ist, müssen Sie bestätigen, dass Sie diese Adresse als primäre Adresse verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="6b93e-152">If another address is already marked as the primary address, you'll need to confirm that you want to use this address as the primary.</span></span>

11. <span data-ttu-id="6b93e-153">Wählen Sie optional das Feld **Privat** aus, um anzugeben, dass es sich um eine private Adresse handelt.</span><span class="sxs-lookup"><span data-stu-id="6b93e-153">Optionally, select the **Private** field to indicate that the address is private.</span></span> <span data-ttu-id="6b93e-154">Nur Benutzer mit ausdrücklicher Berechtigung zum Anzeigen privater Adressinformationen können diese Adresse anzeigen.</span><span class="sxs-lookup"><span data-stu-id="6b93e-154">Only users with explicit permission to view private address information can view this address.</span></span>

12. <span data-ttu-id="6b93e-155">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="6b93e-155">Select **OK**.</span></span>
 
## <a name="create-a-future-change-for-an-address"></a><span data-ttu-id="6b93e-156">Eine zukünftige Änderung für eine Adresse erstellen</span><span class="sxs-lookup"><span data-stu-id="6b93e-156">Create a future change for an address</span></span>

<span data-ttu-id="6b93e-157">In einigen Fällen möchten Sie möglicherweise eine Adresse aktualisieren, um sie in Zukunft zu ändern.</span><span class="sxs-lookup"><span data-stu-id="6b93e-157">In some cases, you might want to update an address to change in the future.</span></span> <span data-ttu-id="6b93e-158">Dies wäre beispielsweise nützlich, wenn ein Mitarbeiter am 15. des folgenden Monats umzieht.</span><span class="sxs-lookup"><span data-stu-id="6b93e-158">For example, this would be useful if an employee is moving on the 15th of the following month.</span></span>

1. <span data-ttu-id="6b93e-159">Öffnen Sie die Seite **Adressen verwalten**, indem Sie **Weitere Optionen > Erweitert** aus einem beliebigen Adressraster auswählen.</span><span class="sxs-lookup"><span data-stu-id="6b93e-159">Open the **Manage addresses** page by selecting **More options > Advanced** from any address grid.</span></span>

2. <span data-ttu-id="6b93e-160">Wählen Sie **Neu** aus, um eine neue Adresse zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6b93e-160">Select **New** to create a new address.</span></span>

3. <span data-ttu-id="6b93e-161">Geben Sie die Details der Adresse ein.</span><span class="sxs-lookup"><span data-stu-id="6b93e-161">Enter the details of the address.</span></span>

4. <span data-ttu-id="6b93e-162">Wählen Sie das Inforegister **Allgemein** aus.</span><span class="sxs-lookup"><span data-stu-id="6b93e-162">Select the **General** FastTab.</span></span>

5. <span data-ttu-id="6b93e-163">Wählen Sie im Feld **Gültigkeitsdatum** das Datum aus, an dem die neue Adresse wirksam werden soll.</span><span class="sxs-lookup"><span data-stu-id="6b93e-163">In the **Effective date** field, select the date the new address will be effective.</span></span>

6. <span data-ttu-id="6b93e-164">Wählen Sie im Feld **Ablaufdatum** optional aus, wann die Adresse nicht mehr aktuell sein wird.</span><span class="sxs-lookup"><span data-stu-id="6b93e-164">In the **Expiration date** field, optionally select when the address will no longer be effective.</span></span>

7. <span data-ttu-id="6b93e-165">Schließen Sie die Seiten.</span><span class="sxs-lookup"><span data-stu-id="6b93e-165">Close the pages.</span></span>

## <a name="view-and-monitor-address-changes"></a><span data-ttu-id="6b93e-166">Adressänderungen anzeigen und überwachen</span><span class="sxs-lookup"><span data-stu-id="6b93e-166">View and monitor address changes</span></span>

<span data-ttu-id="6b93e-167">HR-Mitarbeiter können Adressänderungen über den Arbeitsbereich **Personalverwaltung** anzeigen und überwachen.</span><span class="sxs-lookup"><span data-stu-id="6b93e-167">HR personnel can view and monitor address changes from the **Personnel management** workspace.</span></span> <span data-ttu-id="6b93e-168">Öffnen Sie die Kachel **Personalverwaltung** auf der Seite **Home**, um die Adressänderungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="6b93e-168">To view the address changes, open the **Personnel management** tile from the **Home** page.</span></span> <span data-ttu-id="6b93e-169">Die Adressänderungen werden auf einer Kachel in der oberen rechten Ecke angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6b93e-169">The address changes display on a tile in the upper-right corner.</span></span> <span data-ttu-id="6b93e-170">Die Nummer über **Adressänderungen** zeigt an, wie viele Adressänderungen in der in der angegebenen Anzahl von Tagen auf der Seite **Personalverwaltungsparameter** vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="6b93e-170">The number above **Address changes** shows how many address changes occurred in the number of days specified in the **Human resources parameters** page.</span></span> 

<span data-ttu-id="6b93e-171">Wenn Sie die Kachel **Adressänderungen** auswählen, werden auf einer neuen Seite die Details aller Adressänderungen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6b93e-171">When you select the **Address changes** tile, a new page displays the details of any address changes.</span></span> <span data-ttu-id="6b93e-172">Sie können optional **Zukünftige Adressänderungen einschließen** in der oberen rechten Ecke auswählen, um Adressänderungen mit einem Datum in der Zukunft anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="6b93e-172">You can optionally select **Include future address changes** in the upper-right corner to display address changes with a future date.</span></span>

> [!NOTE]
> <span data-ttu-id="6b93e-173">Wenn Sie eine Warnung oder E-Mail über diese Adressänderungen erhalten möchten, können Sie eine neue Warnregel auf der Registerkarte **Optionen** im Aktionsbereich erstellen.</span><span class="sxs-lookup"><span data-stu-id="6b93e-173">If you want to receive an alert or email about these address changes, you can create a new alert rule on the **Options** tab in the Action Pane.</span></span> <span data-ttu-id="6b93e-174">Weitere Informationen zum Erstellen von Warnregeln finden Sie unter [Warnregeln erstellen](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/create-alerts).</span><span class="sxs-lookup"><span data-stu-id="6b93e-174">For more information about alert rules, see [Create alert rules](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/create-alerts).</span></span><br><br>

> <span data-ttu-id="6b93e-175">Wenn Sie einen Workflow für die Adressänderungen konfigurieren möchten, können Sie die auswählen Option **Extern senden** für Ihre Warnregel auswählen und dann Power Automate verwenden, um das Geschäftsereignis auszulösen und einen Workflow zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="6b93e-175">If you want to configure a workflow for the address changes, you can select the **Send externally** option on your alert rule, and then use Power Automate to trigger the business event and configure a workflow.</span></span> <span data-ttu-id="6b93e-176">Weitere Informationen finden Sie unter [Warnungen als Geschäftsereignisse](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/create-alerts#alerts-as-business-events).</span><span class="sxs-lookup"><span data-stu-id="6b93e-176">For more information, see [Alerts as business events](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/create-alerts#alerts-as-business-events).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]