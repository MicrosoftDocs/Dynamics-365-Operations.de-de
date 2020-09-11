---
title: Unterstützte Szenarien für die Dual-Write-Einrichtung
description: In diesem Thema werden die Szenarien beschrieben, die für die Dual-Write-Einrichtung unterstützt werden.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 08/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 275d24d8f32fd1d2d15356d14c5c6591e8503c65
ms.sourcegitcommit: ec4df354602c20f48f8581bfe5be0c04c66d2927
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "3706251"
---
# <a name="supported-scenarios-for-dual-write-setup"></a><span data-ttu-id="d43f9-103">Unterstützte Szenarien für die Dual-Write-Einrichtung</span><span class="sxs-lookup"><span data-stu-id="d43f9-103">Supported scenarios for dual-write setup</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="d43f9-104">Sie können eine Dual-Write-Verbindung zwischen einer Finance and Operations-Umgebung und einer Common Data Service-Umgebung einrichten.</span><span class="sxs-lookup"><span data-stu-id="d43f9-104">You can set up a dual-write connection between a Finance and Operations environment and a Common Data Service environment.</span></span>

+ <span data-ttu-id="d43f9-105">Eine **Finance and Operations-Umgebung** bietet die zugrunde liegende Plattform für **Finance and Operations-Apps** (z.B. Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management und Dynamics 365 Retail).</span><span class="sxs-lookup"><span data-stu-id="d43f9-105">A **Finance and Operations environment** provides the underlying platform for **Finance and Operations apps** (for example, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, and Dynamics 365 Retail).</span></span>
+ <span data-ttu-id="d43f9-106">Eine **Common Data Service-Umgebung** bietet die zugrunde liegende Plattform für **modellgesteuerte Anwendungen in Dynamics 365** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing und Dynamics 365 Project Service Automation).</span><span class="sxs-lookup"><span data-stu-id="d43f9-106">A **Common Data Service environment** provides the underlying platform for **model-driven apps in Dynamics 365** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing, and Dynamics 365 Project Service Automation).</span></span>

>[!IMPORTANT]
><span data-ttu-id="d43f9-107">Human Resources in Finance and Operations unterstützt Verbindungen für duales Schreiben, aber die Dynamics 365 Human Resources-App nicht.</span><span class="sxs-lookup"><span data-stu-id="d43f9-107">Human Resources in Finance and Operations supports dual-write connections, but the Dynamics 365 Human Resources app doesn't.</span></span>

<span data-ttu-id="d43f9-108">Der Einrichtungsmechanismus variiert je nach Ihrem Abonnement und der Umgebung.</span><span class="sxs-lookup"><span data-stu-id="d43f9-108">The setup mechanism varies, depending on your subscription and the environment.</span></span>

+ <span data-ttu-id="d43f9-109">Bei neuen Instanzen von Finance and Operations Anwendungen beginnt die Einrichtung einer Dual-Write-Verbindung in Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="d43f9-109">For new instances of Finance and Operations apps, the setup of a dual-write connection begins in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="d43f9-110">Wenn Sie eine Lizenz für Microsoft Power Platform haben, erhalten Sie eine neue Common Data Service-Umgebung, wenn Ihr Mandant keine hat.</span><span class="sxs-lookup"><span data-stu-id="d43f9-110">If you have a license for Microsoft Power Platform, you will get a new Common Data Service environment if your tenant doesn't have one.</span></span>
+ <span data-ttu-id="d43f9-111">Für bestehende Instanzen von Finance and Operations-Anwendungen beginnt die Einrichtung einer Dual-Write-Verbindung in der Finance and Operations-Umgebung.</span><span class="sxs-lookup"><span data-stu-id="d43f9-111">For existing instances Finance and Operations apps, the setup of a dual-write connection begins in the Finance and Operations environment.</span></span>

<span data-ttu-id="d43f9-112">Die folgenden Einrichtungsszenarien werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="d43f9-112">The following setup scenarios are supported:</span></span>

+ [<span data-ttu-id="d43f9-113">Eine neue Finance and Operations-Anwendungsinstanz und eine neue modellgesteuerte Anwendungsinstanz</span><span class="sxs-lookup"><span data-stu-id="d43f9-113">A new Finance and Operations app instance and a new model-driven app instance</span></span>](#new-new)
+ [<span data-ttu-id="d43f9-114">Eine neue Finance and Operations App-Instanz und eine bestehende modellgetriebene App-Instanz</span><span class="sxs-lookup"><span data-stu-id="d43f9-114">A new Finance and Operations app instance and an existing model-driven app instance</span></span>](#new-existing)
+ [<span data-ttu-id="d43f9-115">Eine neue Finance and Operations-Anwendungsinstanz, die über Demodaten und eine neue modellgesteuerte Anwendungsinstanz verfügt</span><span class="sxs-lookup"><span data-stu-id="d43f9-115">A new Finance and Operations app instance that has demo data and a new model-driven app instance</span></span>](#new-demo-new)
+ [<span data-ttu-id="d43f9-116">Eine neue Finance and Operations App-Instanz, die über Demodaten verfügt, und eine bestehende modellgetriebene App-Instanz</span><span class="sxs-lookup"><span data-stu-id="d43f9-116">A new Finance and Operations app instance that has demo data and an existing model-driven app instance</span></span>](#new-demo-existing)
+ [<span data-ttu-id="d43f9-117">Eine bestehende Finance and Operations App-Instanz und eine neue oder bestehende modellgetriebene App-Instanz</span><span class="sxs-lookup"><span data-stu-id="d43f9-117">An existing Finance and Operations app instance and a new or existing model-driven app instance</span></span>](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-model-driven-app-instance"></a><a id="new-new"></a><span data-ttu-id="d43f9-118">Eine neue Finance and Operations App-Instanz und eine neue modellgetriebene App-Instanz</span><span class="sxs-lookup"><span data-stu-id="d43f9-118">A new Finance and Operations app instance and a new model-driven app instance</span></span>

<span data-ttu-id="d43f9-119">Um eine Dual-Write-Verbindung zwischen einer neuen Instanz einer Finance and Operations-Anwendung, die keine Daten hat, und einer neuen Instanz einer modellgesteuerten Anwendung in Dynamics 365 einzurichten, folgen Sie den Schritten in [Dual-Write-Setup von Lifecycle Services](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="d43f9-119">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and a new instance of a model-driven app in Dynamics 365, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="d43f9-120">Wenn der Verbindungsaufbau abgeschlossen ist, werden die folgenden Aktionen automatisch ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="d43f9-120">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="d43f9-121">Eine neue, leere Finance and Operations-Umgebung wird bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="d43f9-121">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="d43f9-122">Es wird eine neue, leere Instanz einer modellgesteuerten Anwendung bereitgestellt, in der die CRM-Prime-Lösung installiert wird.</span><span class="sxs-lookup"><span data-stu-id="d43f9-122">A new, empty instance of a model-driven app is provisioned, where the CRM prime solution is installed.</span></span>
- <span data-ttu-id="d43f9-123">Eine Dual-Write-Verbindung wird für DAT-Firmendaten hergestellt.</span><span class="sxs-lookup"><span data-stu-id="d43f9-123">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="d43f9-124">Entitätszuordnungen werden für die Live-Synchronisierung aktiviert.</span><span class="sxs-lookup"><span data-stu-id="d43f9-124">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="d43f9-125">Beide Umgebungen sind dann für die Live-Datensynchronisierung bereit.</span><span class="sxs-lookup"><span data-stu-id="d43f9-125">Both environments are then ready for live data synchronization.</span></span>

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-model-driven-app-instance"></a><a id="new-existing"></a><span data-ttu-id="d43f9-126">Eine neue Finance and Operations-Anwendungsinstanz und eine vorhandene modellgesteuerte Anwendungsinstanz</span><span class="sxs-lookup"><span data-stu-id="d43f9-126">A new Finance and Operations app instance and an existing model-driven app instance</span></span>

<span data-ttu-id="d43f9-127">Um eine Dual-Write-Verbindung zwischen einer neuen Instanz einer Finance and Operations-Anwendung, die keine Daten hat, und einer bestehenden Instanz einer modellgesteuerten Anwendung in Dynamics 365 einzurichten, folgen Sie den Schritten in [Dual-Write-Setup von Lifecycle Services](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="d43f9-127">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and an existing instance of a model-driven app in Dynamics 365, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="d43f9-128">Wenn der Verbindungsaufbau abgeschlossen ist, werden die folgenden Aktionen automatisch ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="d43f9-128">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="d43f9-129">Eine neue, leere Finance and Operations-Umgebung wird bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="d43f9-129">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="d43f9-130">Eine Dual-Write-Verbindung wird für DAT-Firmendaten hergestellt.</span><span class="sxs-lookup"><span data-stu-id="d43f9-130">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="d43f9-131">Entitätszuordnungen werden für die Live-Synchronisierung aktiviert.</span><span class="sxs-lookup"><span data-stu-id="d43f9-131">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="d43f9-132">Beide Umgebungen sind dann für die Live-Datensynchronisierung bereit.</span><span class="sxs-lookup"><span data-stu-id="d43f9-132">Both environments are then ready for live data synchronization.</span></span>

<span data-ttu-id="d43f9-133">Um die vorhandenen Common Data Service-Daten mit der Finance and Operations-Anwendung zu synchronisieren, folgen Sie diesen Schritten.</span><span class="sxs-lookup"><span data-stu-id="d43f9-133">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="d43f9-134">Erstellen Sie ein neues Unternehmen in der Finance and Operations-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="d43f9-134">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="d43f9-135">Fügen Sie das Unternehmen zum Dual-Write-Verbindungsaufbau hinzu.</span><span class="sxs-lookup"><span data-stu-id="d43f9-135">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="d43f9-136">[Bootstrap](bootstrap-company-data.md) die Common Data Service-Daten unter Verwendung eines aus drei Buchstaben bestehenden Buchungscodees der International Organization for Standardization (ISO).</span><span class="sxs-lookup"><span data-stu-id="d43f9-136">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter International Organization for Standardization (ISO) company code.</span></span>

<span data-ttu-id="d43f9-137">Da sich Dual-Write im Live-Synchronisationsmodus befindet, beginnen die Daten von Common Data Service automatisch in die Finance and Operations-Anwendung zu fließen.</span><span class="sxs-lookup"><span data-stu-id="d43f9-137">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-a-new-model-driven-app-instance"></a><a id="new-demo-new"></a><span data-ttu-id="d43f9-138">Eine neue Finance and Operations-Anwendungsinstanz, die über Demodaten und eine neue modellgesteuerte Anwendungsinstanz verfügt.</span><span class="sxs-lookup"><span data-stu-id="d43f9-138">A new Finance and Operations app instance that has demo data and a new model-driven app instance</span></span>

<span data-ttu-id="d43f9-139">Um eine Dual-Write-Verbindung zwischen einer neuen Instanz einer Finance and Operations-Anwendung, die über Demodaten verfügt, und einer neuen Instanz einer modellgesteuerten Anwendung in Dynamics 365 einzurichten, folgen Sie den Schritten im Abschnitt [Eine neue Finance and Operations-Anwendungsinstanz und eine neue modellgesteuerte Anwendungsinstanz](#new-new) weiter oben in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="d43f9-139">To set up a dual-write connection between a new instance of a Finance and Operations app that has demo data and a new instance of a model-driven app in Dynamics 365, follow the steps in the [A new Finance and Operations app instance and a new model-driven app instance](#new-new) section earlier in this topic.</span></span> <span data-ttu-id="d43f9-140">Wenn der Verbindungsaufbau abgeschlossen ist und Sie die Demodaten mit der modellgesteuerten Anwendung synchronisieren möchten, folgen Sie diesen Schritten.</span><span class="sxs-lookup"><span data-stu-id="d43f9-140">When the connection setup is completed, if you want to sync the demo data to the model-driven app, follow these steps.</span></span>

1. <span data-ttu-id="d43f9-141">Öffnen Sie die Anwendung Finance and Operations von der LCS-Seite, melden Sie sich an und gehen Sie dann zu **Datenverwaltung \> Dual-write**.</span><span class="sxs-lookup"><span data-stu-id="d43f9-141">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="d43f9-142">Führen Sie die Funktionalität **Initiale Synchronisation** für die Entitäten aus, für die Sie Daten synchronisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="d43f9-142">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-an-existing-model-driven-app-instance"></a><a id="new-demo-existing"></a><span data-ttu-id="d43f9-143">Eine neue Finance and Operations-Anwendungsinstanz, die über Demodaten und eine bestehende modellgesteuerte Anwendungsinstanz verfügt.</span><span class="sxs-lookup"><span data-stu-id="d43f9-143">A new Finance and Operations app instance that has demo data and an existing model-driven app instance</span></span>

<span data-ttu-id="d43f9-144">Um eine Dual-Write-Verbindung zwischen einer neuen Instanz einer Finance and Operations-Anwendung, die über Demodaten verfügt, und einer bestehenden Instanz einer modellgesteuerten Anwendung in Dynamics 365 herzustellen, folgen Sie den Schritten im Abschnitt [Eine neue Finance and Operations-Anwendungsinstanz und eine bestehende modellgesteuerte Anwendungsinstanz](#new-existing) weiter oben in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="d43f9-144">To set up a dual-write connection between a new instance of a Finance and Operations app that has demo data and an existing instance of a model-driven app in Dynamics 365, follow the steps in the [A new Finance and Operations app instance and an existing model-driven app instance](#new-existing) section earlier in this topic.</span></span> <span data-ttu-id="d43f9-145">Wenn der Verbindungsaufbau abgeschlossen ist und Sie die Demodaten mit der modellgesteuerten Anwendung synchronisieren möchten, folgen Sie diesen Schritten.</span><span class="sxs-lookup"><span data-stu-id="d43f9-145">When the connection setup is completed, if you want to sync the demo data to the model-driven app, follow these steps.</span></span>

1. <span data-ttu-id="d43f9-146">Öffnen Sie die Anwendung Finance and Operations von der LCS-Seite, melden Sie sich an und gehen Sie dann zu **Datenverwaltung \> Dual-write**.</span><span class="sxs-lookup"><span data-stu-id="d43f9-146">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="d43f9-147">Führen Sie die Funktionalität **Initiale Synchronisation** für die Entitäten aus, für die Sie Daten synchronisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="d43f9-147">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="d43f9-148">Um die vorhandenen Common Data Service-Daten mit der Finance and Operations-Anwendung zu synchronisieren, folgen Sie diesen Schritten.</span><span class="sxs-lookup"><span data-stu-id="d43f9-148">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="d43f9-149">Erstellen Sie ein neues Unternehmen in der Finance and Operations-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="d43f9-149">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="d43f9-150">Fügen Sie das Unternehmen zum Dual-Write-Verbindungsaufbau hinzu.</span><span class="sxs-lookup"><span data-stu-id="d43f9-150">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="d43f9-151">[Bootstrap](bootstrap-company-data.md) der Common Data Service-Daten unter Verwendung eines dreibuchstabigen ISO-Buchungscodees.</span><span class="sxs-lookup"><span data-stu-id="d43f9-151">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>

<span data-ttu-id="d43f9-152">Da sich Dual-Write im Live-Synchronisationsmodus befindet, beginnen die Daten von Common Data Service automatisch in die Finance and Operations-Anwendung zu fließen.</span><span class="sxs-lookup"><span data-stu-id="d43f9-152">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-or-existing-model-driven-app-instance"></a><a id="existing-existing"></a><span data-ttu-id="d43f9-153">Eine bestehende Finance and Operations-Anwendungsinstanz und eine neue oder bestehende modellgetriebene Anwendungsinstanz</span><span class="sxs-lookup"><span data-stu-id="d43f9-153">An existing Finance and Operations app instance and a new or existing model-driven app instance</span></span>

<span data-ttu-id="d43f9-154">Die Einrichtung einer Dual-Write-Verbindung zwischen einer bestehenden Instanz einer Finance and Operations-Anwendung und einer neuen oder bestehenden Instanz einer modellgesteuerten Anwendung in Dynamics 365 erfolgt in der Finance and Operation-Umgebung.</span><span class="sxs-lookup"><span data-stu-id="d43f9-154">The setup of a dual-write connection between an existing instance of a Finance and Operations app and a new or existing instance of a model-driven app in Dynamics 365 occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="d43f9-155">Richten Sie die Verbindung von der Finance and Operations-Anwendung aus ein.</span><span class="sxs-lookup"><span data-stu-id="d43f9-155">Set up the connection from the Finance and Operations app.</span></span>
2. <span data-ttu-id="d43f9-156">Um die vorhandenen Common Data Service-Daten mit der Finance and Operations-Anwendung zu synchronisieren, [Bootstrap](bootstrap-company-data.md) die Common Data Service-Daten unter Verwendung eines dreibuchstabigen ISO-Buchungskreises.</span><span class="sxs-lookup"><span data-stu-id="d43f9-156">To sync the existing Common Data Service data to the Finance and Operations app, [bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>

<span data-ttu-id="d43f9-157">Da sich Dual-Write im Live-Synchronisationsmodus befindet, beginnen die Daten von Common Data Service automatisch in die Finance and Operations-Anwendung zu fließen.</span><span class="sxs-lookup"><span data-stu-id="d43f9-157">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>
