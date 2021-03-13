---
title: Erste Schritte mit dem Kostenrechnungsdienst (private Vorschau)
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
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 1f602116edabc424b6cbee541e268df017912d3c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011846"
---
# <a name="get-started-with-the-cost-accounting-service-private-preview"></a><span data-ttu-id="9558c-103">Erste Schritte mit dem Kostenrechnungsdienst (private Vorschau)</span><span class="sxs-lookup"><span data-stu-id="9558c-103">Get started with the cost accounting service (private preview)</span></span>

[!INCLUDE [banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="9558c-104">Die in diesem Abschnitt genannten Funktionen stehen im Rahmen einer privaten Vorschauversion zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="9558c-104">The functionality that is described in this topic is available as part of a private preview release.</span></span> <span data-ttu-id="9558c-105">Der Inhalt dieses Themas und die darin beschriebenen Funktionen können sich ändern.</span><span class="sxs-lookup"><span data-stu-id="9558c-105">The content of this topic and the functionality that it describes are subject to change.</span></span> <span data-ttu-id="9558c-106">Weitere Informationen zu Vorschauversionen finden Sie in den [FAQ zu Dienstupdates für eine Version](../../fin-ops-core/fin-ops/get-started/one-version.md).</span><span class="sxs-lookup"><span data-stu-id="9558c-106">For more information about preview releases, see [One version service updates FAQ](../../fin-ops-core/fin-ops/get-started/one-version.md).</span></span>

<span data-ttu-id="9558c-107">Mit dem Kostenrechnungsservice können Sie mehrere Bestandsbuchungen in den von Ihnen eingerichteten Kostenrechnungsbüchern durchführen.</span><span class="sxs-lookup"><span data-stu-id="9558c-107">The cost accounting service lets you do multiple inventory accounting in the cost accounting ledgers that you've set up.</span></span> <span data-ttu-id="9558c-108">Sie verknüpfen jedes Kostenrechnungsbuch mit einer *Konvention*.</span><span class="sxs-lookup"><span data-stu-id="9558c-108">You associate each cost accounting ledger with a *convention*.</span></span> <span data-ttu-id="9558c-109">Eine Konvention ist eine Sammlung der folgenden Arten von Rechnungslegungsgrundsätzen:</span><span class="sxs-lookup"><span data-stu-id="9558c-109">A convention is a collection of the following types of accounting policies:</span></span>

- <span data-ttu-id="9558c-110">Kostenobjekt</span><span class="sxs-lookup"><span data-stu-id="9558c-110">Cost object</span></span>
- <span data-ttu-id="9558c-111">Messungsgrundlage für Eingabe</span><span class="sxs-lookup"><span data-stu-id="9558c-111">Input measurement basis</span></span>
- <span data-ttu-id="9558c-112">Kostenflussannahme</span><span class="sxs-lookup"><span data-stu-id="9558c-112">Cost flow assumption</span></span>
- <span data-ttu-id="9558c-113">Kostenelement</span><span class="sxs-lookup"><span data-stu-id="9558c-113">Cost element</span></span>

> [!NOTE]
> <span data-ttu-id="9558c-114">Auch nach dem Aktivieren des Kostenrechnungsdienstes können Sie die Bestandsabrechnung in Microsoft Dynamics 365 Supply Chain Management wie gewöhnlich durchführen.</span><span class="sxs-lookup"><span data-stu-id="9558c-114">Even after you've turned on the cost accounting service, you can still do  inventory accounting in Microsoft Dynamics 365 Supply Chain Management, as usual.</span></span>

<span data-ttu-id="9558c-115">Der Kostenrechnungsdienst ist ein Add-In.</span><span class="sxs-lookup"><span data-stu-id="9558c-115">The cost accounting service is an add-in.</span></span> <span data-ttu-id="9558c-116">Um seine Funktionen verfügbar zu machen, müssen Sie es über Microsoft Dynamics Lifecycle Services (LCS) installieren.</span><span class="sxs-lookup"><span data-stu-id="9558c-116">To makes its features available, you must install it from Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="9558c-117">Daher können Sie es in einer Testumgebung auswerten, bevor Sie es für Produktionsumgebungen aktivieren.</span><span class="sxs-lookup"><span data-stu-id="9558c-117">Therefore, you can choose to evaluate it in a test environment before you turn it on for production environments.</span></span>

<span data-ttu-id="9558c-118">Der Kostenrechnungsdienst unterstützt derzeit nicht alle integrierten Kostenmanagementfunktionen von Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="9558c-118">The cost accounting service doesn't currently support all the cost management features that are built into Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="9558c-119">Daher ist es wichtig, dass Sie prüfen, ob der derzeit verfügbare Funktionsumfang Ihren Anforderungen entspricht.</span><span class="sxs-lookup"><span data-stu-id="9558c-119">Therefore, it's important that you evaluate whether the set of features that is currently available will meet your requirements.</span></span>

## <a name="how-to-get-the-cost-accounting-service-private-preview"></a><a name="sign-up"></a><span data-ttu-id="9558c-120">Abrufen des Kostenrechnungsdiensts (private Vorschau)</span><span class="sxs-lookup"><span data-stu-id="9558c-120">How to get the cost accounting service (private preview)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9558c-121">Um den Kostenrechnungsdienst nutzen zu können, müssen Sie über eine LCS-fähige Hochverfügbarkeitsumgebung (keine OneBox-Umgebung) verfügen und Dynamics 365 Supply Chain Management in der Version 10.0.11 oder höher muss ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="9558c-121">To use the cost accounting service, you must have an LCS-enabled high-availability environment (not a OneBox environment), and you must be running Dynamics 365 Supply Chain Management version 10.0.11 or later.</span></span>

<span data-ttu-id="9558c-122">Um sich für die private Vorschau des Kostenrechnungsdiensts anzumelden, senden Sie bitte Ihre LCS-Umgebungs-ID per E-Mail an [Kostenrechnungsdienst (private Vorschau)](mailto:aevengir@microsoft.com?subject=Cost%20accounting%20service%20%28private%20preview%29).</span><span class="sxs-lookup"><span data-stu-id="9558c-122">To sign up for the cost accounting service private preview, please send your LCS environment ID by email to [Cost accounting service (private preview)](mailto:aevengir@microsoft.com?subject=Cost%20accounting%20service%20%28private%20preview%29).</span></span> <span data-ttu-id="9558c-123">Nach der Genehmigung für das Programm senden wir Ihnen eine Folge-E-Mail mit einem Beta-Schlüssel für den Kostenrechnungsservice.</span><span class="sxs-lookup"><span data-stu-id="9558c-123">On approving you for the program, we will send you a follow up email that contains a cost accounting service beta key.</span></span> <span data-ttu-id="9558c-124">Nach Erhalt des Beta-Schlüssels können Sie fortfahren, indem Sie das [Add-In installieren](#install).</span><span class="sxs-lookup"><span data-stu-id="9558c-124">On receiving the beta key, you can proceed by [installing the add-in](#install).</span></span>

## <a name="licensing"></a><span data-ttu-id="9558c-125">Lizenzierung</span><span class="sxs-lookup"><span data-stu-id="9558c-125">Licensing</span></span>

<span data-ttu-id="9558c-126">Der Kostenrechnungsdienst wird zusammen mit den Standardfunktionen der Bestandsbuchhaltung lizenziert, die für das Supply Chain Management verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="9558c-126">The cost accounting service is licensed together with the standard features of inventory accounting that are available for Supply Chain Management.</span></span> <span data-ttu-id="9558c-127">Sie müssen keine zusätzliche Lizenz erwerben, um den Kostenrechnungsdienst nutzen zu können.</span><span class="sxs-lookup"><span data-stu-id="9558c-127">You don't have to purchase an additional license to use the cost accounting service.</span></span>

## <a name="install-the-add-in"></a><a name="install"></a><span data-ttu-id="9558c-128">Installieren des Add-Ins</span><span class="sxs-lookup"><span data-stu-id="9558c-128">Install the add-in</span></span>

<span data-ttu-id="9558c-129">Um den Kostenrechnungsdienst zu verwenden, installieren Sie das Kostenrechnungsdienst-Add-In für Supply Chain Management wie im folgenden Verfahren beschrieben.</span><span class="sxs-lookup"><span data-stu-id="9558c-129">To use the cost accounting service, install the cost accounting service add-in for Supply Chain Management as described in the following procedure.</span></span>

1. <span data-ttu-id="9558c-130">[Anmelden](#sign-up) für den Kostenrechnungsdiensts (private Vorschau).</span><span class="sxs-lookup"><span data-stu-id="9558c-130">[Sign up](#sign-up) for the cost accounting service (private preview).</span></span>

1. <span data-ttu-id="9558c-131">Melden Sie sich bei LCS an.</span><span class="sxs-lookup"><span data-stu-id="9558c-131">Sign in to LCS.</span></span>

1. <span data-ttu-id="9558c-132">Navigieren Sie zu **Verwaltung von Vorschaufunktionen**.</span><span class="sxs-lookup"><span data-stu-id="9558c-132">Go to **Preview feature management**.</span></span>

1. <span data-ttu-id="9558c-133">Wählen Sie das Pluszeichen (**+**).</span><span class="sxs-lookup"><span data-stu-id="9558c-133">Select the plus sign (**+**).</span></span>

1. <span data-ttu-id="9558c-134">Im Feld **Code** geben Sie Ihren Add-In-Beta-Schlüssel für den Kostenrechnungsdienst ein.</span><span class="sxs-lookup"><span data-stu-id="9558c-134">In the **Code** field, enter your add-in beta key for the cost accounting service.</span></span> <span data-ttu-id="9558c-135">(Sie sollten Ihren Schlüssel per E-Mail erhalten haben.)</span><span class="sxs-lookup"><span data-stu-id="9558c-135">(You should have received your key by email.)</span></span>

1. <span data-ttu-id="9558c-136">Wählen Sie **Entsperren** aus.</span><span class="sxs-lookup"><span data-stu-id="9558c-136">Select **Unblock**.</span></span>

1. <span data-ttu-id="9558c-137">Öffnen Sie die LCS-Umgebung, in der Sie den Dienst hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="9558c-137">Open the LCS environment where you want to add the service.</span></span>

1. <span data-ttu-id="9558c-138">Gehen Sie zu **Vollständige Details**.</span><span class="sxs-lookup"><span data-stu-id="9558c-138">Go to **Full details**.</span></span>

1. <span data-ttu-id="9558c-139">Scrollen Sie zum Inforegister **Umgebungs-Add-Ins**.</span><span class="sxs-lookup"><span data-stu-id="9558c-139">Scroll down to the **Environment add-ins** FastTab.</span></span>

1. <span data-ttu-id="9558c-140">Wählen Sie **Installieren Sie ein neues Add-In**.</span><span class="sxs-lookup"><span data-stu-id="9558c-140">Select **Install a new add-in**.</span></span>

1. <span data-ttu-id="9558c-141">Wählen Sie **Kostenrechnungsdienst**.</span><span class="sxs-lookup"><span data-stu-id="9558c-141">Select **Cost accounting service**.</span></span>

1. <span data-ttu-id="9558c-142">Befolgen Sie die Installationsanleitung und erklären Sie sich mit den Allgemeinen Geschäftsbedingungen einverstanden.</span><span class="sxs-lookup"><span data-stu-id="9558c-142">Follow the installation guide, and agree to the terms and conditions.</span></span>

1. <span data-ttu-id="9558c-143">Wählen Sie **Installieren**.</span><span class="sxs-lookup"><span data-stu-id="9558c-143">Select **Install**.</span></span>

1. <span data-ttu-id="9558c-144">Auf dem Inforegister **Umgebungs-Add-Ins** sollten Sie sehen, dass der Kostenrechnungsdienst installiert wird.</span><span class="sxs-lookup"><span data-stu-id="9558c-144">On the **Environment add-ins** FastTab, you should see that the cost accounting service is being installed.</span></span> <span data-ttu-id="9558c-145">Nach einigen Minuten sollte sich der Status von **Installieren** in **Installiert** ändern.</span><span class="sxs-lookup"><span data-stu-id="9558c-145">After a few minutes, the status should change from **Installing** to **Installed**.</span></span> <span data-ttu-id="9558c-146">(Möglicherweise müssen Sie die Seite aktualisieren, um diese Änderung zu sehen.) Zu diesem Zeitpunkt ist der Kostenrechnungsdienst einsatzbereit.</span><span class="sxs-lookup"><span data-stu-id="9558c-146">(You might have to refresh the page to see this change.) At that point, the cost accounting service is ready for use.</span></span>

## <a name="set-up-the-integration"></a><span data-ttu-id="9558c-147">Einrichten der Integration</span><span class="sxs-lookup"><span data-stu-id="9558c-147">Set up the integration</span></span>

<span data-ttu-id="9558c-148">Einrichten der Integration zwischen dem Kostenrechnungsdienst und Dynamics 365 Supply Chain Management:</span><span class="sxs-lookup"><span data-stu-id="9558c-148">To set up the integration between the cost accounting service and Dynamics 365 Supply Chain Management:</span></span>

1. <span data-ttu-id="9558c-149">Gehen Sie zu **Systemverwaltung > Funktionsverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="9558c-149">Go to **System administration > Feature Management**.</span></span>

1. <span data-ttu-id="9558c-150">Wählen Sie **Nach Updates suchen**.</span><span class="sxs-lookup"><span data-stu-id="9558c-150">Select **Check for updates**.</span></span>

1. <span data-ttu-id="9558c-151">Öffnen Sie die Registerkarte **Alle** und suchen Sie nach der genannten Funktion *Kostenrechnungsdienst*.</span><span class="sxs-lookup"><span data-stu-id="9558c-151">Open the **All** tab and search for the feature named *Cost accounting service*.</span></span>

1. <span data-ttu-id="9558c-152">Wählen Sie **Jetzt aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="9558c-152">Select **Enable now**.</span></span>

1. <span data-ttu-id="9558c-153">Gehen Sie zu **Kostenverwaltung > Kostenrechnungsdienst > Setup > Kostenrechnungsdienstparameter > Integrationsparameter**.</span><span class="sxs-lookup"><span data-stu-id="9558c-153">Go to **Cost management > Cost accounting service > Setup > Cost accounting service parameters > Integrations parameters**.</span></span>

1. <span data-ttu-id="9558c-154">Im Feld **Anwendungs-ID** geben Sie den folgenden Code ein:</span><span class="sxs-lookup"><span data-stu-id="9558c-154">In the **Application ID** field, enter the following code:</span></span><br> <span data-ttu-id="9558c-155">08231eb2-a501-4edb-b3c5-aede5e5e0c3f</span><span class="sxs-lookup"><span data-stu-id="9558c-155">08231eb2-a501-4edb-b3c5-aede5e5e0c3f</span></span>

1. <span data-ttu-id="9558c-156">Im Feld **Datendienst-Endpunkt** geben Sie die folgende URL ein:</span><span class="sxs-lookup"><span data-stu-id="9558c-156">In the **Data service endpoint** field, enter the following URL:</span></span><br>https://operationsdataservice.operations365.dynamics.com/

1. <span data-ttu-id="9558c-157">Im Feld **Kostenrechnungsdienst-Endpunkt** geben Sie die folgende URL ein:</span><span class="sxs-lookup"><span data-stu-id="9558c-157">In the **Cost accounting service endpoint** field, enter the following URL:</span></span><br>https://costaccountingservice.operations365.dynamics.com/

1. <span data-ttu-id="9558c-158">Der Kostenrechnungsdienst ist jetzt einsatzbereit.</span><span class="sxs-lookup"><span data-stu-id="9558c-158">The cost accounting service is now ready for use.</span></span>

## <a name="related-resources"></a><span data-ttu-id="9558c-159">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="9558c-159">Related resources</span></span>

[<span data-ttu-id="9558c-160">Startseite für den Kostenrechnungsdienst</span><span class="sxs-lookup"><span data-stu-id="9558c-160">Cost accounting service home page</span></span>](cost-accounting-service-home.md)
