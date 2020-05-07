---
title: Erste Schritte mit dem Kostenrechnungsdienst
description: Dieses Thema enthält Lizenzdetails und Installationsanweisungen für den Kostenrechnungsdienst.
author: AndersGirke
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: cbbce7eaac264973bf0b95ad5175bf70ed2b4ae9
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "3276920"
---
# <a name="get-started-with-the-cost-accounting-service"></a><span data-ttu-id="595dc-103">Erste Schritte mit dem Kostenrechnungsdienst</span><span class="sxs-lookup"><span data-stu-id="595dc-103">Get started with the cost accounting service</span></span>

[!INCLUDE [banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="595dc-104">Die in diesem Abschnitt genannten Funktionen stehen im Rahmen einer privaten Vorschauversion zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="595dc-104">The functionality that is described in this topic is available as part of a private preview release.</span></span> <span data-ttu-id="595dc-105">Der Inhalt dieses Themas und die darin beschriebenen Funktionen können sich ändern.</span><span class="sxs-lookup"><span data-stu-id="595dc-105">The content of this topic and the functionality that it describes are subject to change.</span></span> <span data-ttu-id="595dc-106">Weitere Informationen zu Vorschauversionen finden Sie in den [FAQ zu Dienstupdates für eine Version](../../fin-ops-core/fin-ops/get-started/one-version.md).</span><span class="sxs-lookup"><span data-stu-id="595dc-106">For more information about preview releases, see [One version service updates FAQ](../../fin-ops-core/fin-ops/get-started/one-version.md).</span></span>

<span data-ttu-id="595dc-107">Mit dem Kostenrechnungsservice können Sie mehrere Bestandsbuchungen in den von Ihnen eingerichteten Kostenrechnungsbüchern durchführen.</span><span class="sxs-lookup"><span data-stu-id="595dc-107">The cost accounting service lets you do multiple inventory accounting in the cost accounting ledgers that you've set up.</span></span> <span data-ttu-id="595dc-108">Sie verknüpfen jedes Kostenrechnungsbuch mit einer *Konvention*.</span><span class="sxs-lookup"><span data-stu-id="595dc-108">You associate each cost accounting ledger with a *convention*.</span></span> <span data-ttu-id="595dc-109">Eine Konvention ist eine Sammlung der folgenden Arten von Rechnungslegungsgrundsätzen:</span><span class="sxs-lookup"><span data-stu-id="595dc-109">A convention is a collection of the following types of accounting policies:</span></span>

- <span data-ttu-id="595dc-110">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="595dc-110">Cost object</span></span>
- <span data-ttu-id="595dc-111">Messungsgrundlage für Eingabe</span><span class="sxs-lookup"><span data-stu-id="595dc-111">Input measurement basis</span></span>
- <span data-ttu-id="595dc-112">Kostenflussannahme</span><span class="sxs-lookup"><span data-stu-id="595dc-112">Cost flow assumption</span></span>
- <span data-ttu-id="595dc-113">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="595dc-113">Cost element</span></span>

> [!NOTE]
> <span data-ttu-id="595dc-114">Auch nach dem Aktivieren des Kostenrechnungsdienstes können Sie die Bestandsabrechnung in Microsoft Dynamics 365 Supply Chain Management wie gewöhnlich durchführen.</span><span class="sxs-lookup"><span data-stu-id="595dc-114">Even after you've turned on the cost accounting service, you can still do  inventory accounting in Microsoft Dynamics 365 Supply Chain Management, as usual.</span></span>

<span data-ttu-id="595dc-115">Der Kostenrechnungsdienst ist ein Add-In.</span><span class="sxs-lookup"><span data-stu-id="595dc-115">The cost accounting service is an add-in.</span></span> <span data-ttu-id="595dc-116">Um seine Funktionen verfügbar zu machen, müssen Sie es über Microsoft Dynamics Lifecycle Services (LCS) installieren.</span><span class="sxs-lookup"><span data-stu-id="595dc-116">To makes its features available, you must install it from Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="595dc-117">Daher können Sie es in einer Testumgebung auswerten, bevor Sie es für Produktionsumgebungen aktivieren.</span><span class="sxs-lookup"><span data-stu-id="595dc-117">Therefore, you can choose to evaluate it in a test environment before you turn it on for production environments.</span></span>

<span data-ttu-id="595dc-118">Der Kostenrechnungsdienst unterstützt derzeit nicht alle integrierten Kostenmanagementfunktionen von Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="595dc-118">The cost accounting service doesn't currently support all the cost management features that are built into Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="595dc-119">Daher ist es wichtig, dass Sie prüfen, ob der derzeit verfügbare Funktionsumfang Ihren Anforderungen entspricht.</span><span class="sxs-lookup"><span data-stu-id="595dc-119">Therefore, it's important that you evaluate whether the set of features that is currently available will meet your requirements.</span></span>

## <a name="licensing"></a><span data-ttu-id="595dc-120">Lizenzierung</span><span class="sxs-lookup"><span data-stu-id="595dc-120">Licensing</span></span>

<span data-ttu-id="595dc-121">Der Kostenrechnungsdienst wird zusammen mit den Standardfunktionen der Bestandsbuchhaltung lizenziert, die für das Supply Chain Management verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="595dc-121">The cost accounting service is licensed together with the standard features of inventory accounting that are available for Supply Chain Management.</span></span> <span data-ttu-id="595dc-122">Sie müssen keine zusätzliche Lizenz erwerben, um den Kostenrechnungsdienst nutzen zu können.</span><span class="sxs-lookup"><span data-stu-id="595dc-122">You don't have to purchase an additional license to use the cost accounting service.</span></span>

## <a name="install-the-add-in"></a><span data-ttu-id="595dc-123">Installieren des Add-Ins</span><span class="sxs-lookup"><span data-stu-id="595dc-123">Install the add-in</span></span>

> [!IMPORTANT]
> <span data-ttu-id="595dc-124">Um den Kostenrechnungsdienst nutzen zu können, müssen Sie über eine LCS-fähige Hochverfügbarkeitsumgebung (keine OneBox-Umgebung) verfügen und Dynamics 365 Supply Chain Management in der Version 10.0.11 oder höher muss ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="595dc-124">To use the cost accounting service, you must have an LCS-enabled high-availability environment (not a OneBox environment), and you must be running Dynamics 365 Supply Chain Management version 10.0.11 or later.</span></span>

<span data-ttu-id="595dc-125">Um den Kostenrechnungsdienst zu verwenden, installieren Sie das Kostenrechnungsdienst-Add-In für Supply Chain Management wie im folgenden Verfahren beschrieben.</span><span class="sxs-lookup"><span data-stu-id="595dc-125">To use the cost accounting service, install the cost accounting service add-in for Supply Chain Management as described in the following procedure.</span></span>

1. <span data-ttu-id="595dc-126">Melden Sie sich bei LCS an.</span><span class="sxs-lookup"><span data-stu-id="595dc-126">Sign in to LCS.</span></span>

1. <span data-ttu-id="595dc-127">Navigieren Sie zu **Verwaltung von Vorschaufunktionen**.</span><span class="sxs-lookup"><span data-stu-id="595dc-127">Go to **Preview feature management**.</span></span>

1. <span data-ttu-id="595dc-128">Wählen Sie das Pluszeichen (**+**).</span><span class="sxs-lookup"><span data-stu-id="595dc-128">Select the plus sign (**+**).</span></span>

1. <span data-ttu-id="595dc-129">Im Feld **Code** geben Sie Ihren Add-In-Beta-Schlüssel für den Kostenrechnungsdienst ein.</span><span class="sxs-lookup"><span data-stu-id="595dc-129">In the **Code** field, enter your add-in beta key for the cost accounting service.</span></span> <span data-ttu-id="595dc-130">(Sie sollten Ihren Schlüssel per E-Mail erhalten haben.)</span><span class="sxs-lookup"><span data-stu-id="595dc-130">(You should have received your key by email.)</span></span>

1. <span data-ttu-id="595dc-131">Wählen Sie **Entsperren** aus.</span><span class="sxs-lookup"><span data-stu-id="595dc-131">Select **Unblock**.</span></span>

1. <span data-ttu-id="595dc-132">Öffnen Sie die LCS-Umgebung, in der Sie den Dienst hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="595dc-132">Open the LCS environment where you want to add the service.</span></span>

1. <span data-ttu-id="595dc-133">Gehen Sie zu **Vollständige Details**.</span><span class="sxs-lookup"><span data-stu-id="595dc-133">Go to **Full details**.</span></span>

1. <span data-ttu-id="595dc-134">Scrollen Sie zum Inforegister **Umgebungs-Add-Ins**.</span><span class="sxs-lookup"><span data-stu-id="595dc-134">Scroll down to the **Environment add-ins** FastTab.</span></span>

1. <span data-ttu-id="595dc-135">Wählen Sie **Installieren Sie ein neues Add-In**.</span><span class="sxs-lookup"><span data-stu-id="595dc-135">Select **Install a new add-in**.</span></span>

1. <span data-ttu-id="595dc-136">Wählen Sie **Kostenrechnungsdienst**.</span><span class="sxs-lookup"><span data-stu-id="595dc-136">Select **Cost accounting service**.</span></span>

1. <span data-ttu-id="595dc-137">Befolgen Sie die Installationsanleitung und erklären Sie sich mit den Allgemeinen Geschäftsbedingungen einverstanden.</span><span class="sxs-lookup"><span data-stu-id="595dc-137">Follow the installation guide, and agree to the terms and conditions.</span></span>

1. <span data-ttu-id="595dc-138">Wählen Sie **Installieren**.</span><span class="sxs-lookup"><span data-stu-id="595dc-138">Select **Install**.</span></span>

1. <span data-ttu-id="595dc-139">Auf dem Inforegister **Umgebungs-Add-Ins** sollten Sie sehen, dass der Kostenrechnungsdienst installiert wird.</span><span class="sxs-lookup"><span data-stu-id="595dc-139">On the **Environment add-ins** FastTab, you should see that the cost accounting service is being installed.</span></span> <span data-ttu-id="595dc-140">Nach einigen Minuten sollte sich der Status von **Installieren** in **Installiert** ändern.</span><span class="sxs-lookup"><span data-stu-id="595dc-140">After a few minutes, the status should change from **Installing** to **Installed**.</span></span> <span data-ttu-id="595dc-141">(Möglicherweise müssen Sie die Seite aktualisieren, um diese Änderung zu sehen.) Zu diesem Zeitpunkt ist der Kostenrechnungsdienst einsatzbereit.</span><span class="sxs-lookup"><span data-stu-id="595dc-141">(You might have to refresh the page to see this change.) At that point, the cost accounting service is ready for use.</span></span>

## <a name="set-up-the-integration"></a><span data-ttu-id="595dc-142">Einrichten der Integration</span><span class="sxs-lookup"><span data-stu-id="595dc-142">Set up the integration</span></span>

<span data-ttu-id="595dc-143">Einrichten der Integration zwischen dem Kostenrechnungsdienst und Dynamics 365 Supply Chain Management:</span><span class="sxs-lookup"><span data-stu-id="595dc-143">To set up the integration between the cost accounting service and Dynamics 365 Supply Chain Management:</span></span>

1. <span data-ttu-id="595dc-144">Gehen Sie zu **Systemverwaltung > Funktionsverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="595dc-144">Go to **System administration > Feature Management**.</span></span>

1. <span data-ttu-id="595dc-145">Wählen Sie **Nach Updates suchen**.</span><span class="sxs-lookup"><span data-stu-id="595dc-145">Select **Check for updates**.</span></span>

1. <span data-ttu-id="595dc-146">Öffnen Sie die Registerkarte **Alle** und suchen Sie nach der genannten Funktion *Kostenrechnungsdienst*.</span><span class="sxs-lookup"><span data-stu-id="595dc-146">Open the **All** tab and search for the feature named *Cost accounting service*.</span></span>

1. <span data-ttu-id="595dc-147">Wählen Sie **Jetzt aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="595dc-147">Select **Enable now**.</span></span>

1. <span data-ttu-id="595dc-148">Gehen Sie zu **Kostenverwaltung > Kostenrechnungsdienst > Setup > Kostenrechnungsdienstparameter > Integrationsparameter**.</span><span class="sxs-lookup"><span data-stu-id="595dc-148">Go to **Cost management > Cost accounting service > Setup > Cost accounting service parameters > Integrations parameters**.</span></span>

1. <span data-ttu-id="595dc-149">Im Feld **Anwendungs-ID** geben Sie den folgenden Code ein:</span><span class="sxs-lookup"><span data-stu-id="595dc-149">In the **Application ID** field, enter the following code:</span></span><br> <span data-ttu-id="595dc-150">08231eb2-a501-4edb-b3c5-aede5e5e0c3f</span><span class="sxs-lookup"><span data-stu-id="595dc-150">08231eb2-a501-4edb-b3c5-aede5e5e0c3f</span></span>

1. <span data-ttu-id="595dc-151">Im Feld **Datendienst-Endpunkt** geben Sie die folgende URL ein:</span><span class="sxs-lookup"><span data-stu-id="595dc-151">In the **Data service endpoint** field, enter the following URL:</span></span><br>https://operationsdataservice.operations365.dynamics.com/

1. <span data-ttu-id="595dc-152">Im Feld **Kostenrechnungsdienst-Endpunkt** geben Sie die folgende URL ein:</span><span class="sxs-lookup"><span data-stu-id="595dc-152">In the **Cost accounting service endpoint** field, enter the following URL:</span></span><br>https://costaccountingservice.operations365.dynamics.com/

1. <span data-ttu-id="595dc-153">Der Kostenrechnungsdienst ist jetzt einsatzbereit.</span><span class="sxs-lookup"><span data-stu-id="595dc-153">The cost accounting service is now ready for use.</span></span>

## <a name="related-resources"></a><span data-ttu-id="595dc-154">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="595dc-154">Related resources</span></span>

[<span data-ttu-id="595dc-155">Startseite für den Kostenrechnungsdienst</span><span class="sxs-lookup"><span data-stu-id="595dc-155">Cost accounting service home page</span></span>](cost-accounting-service-home.md)
