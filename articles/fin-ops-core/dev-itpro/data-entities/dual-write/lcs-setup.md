---
title: Einrichtung von dualem Schreiben aus Lifecycle Services
description: In diesem Thema wird erläutert, wie Sie eine Verbindung für duales Schreiben über Microsoft Dynamics Lifecycle Services (LCS) einrichten.
author: RamaKrishnamoorthy
ms.date: 05/11/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: eb4170ef6cb09c862f6a4163670c519d5d8077fb
ms.sourcegitcommit: 365092f735310990e82516110141d42aaf04e654
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "6103568"
---
# <a name="dual-write-setup-from-lifecycle-services"></a><span data-ttu-id="49be9-103">Einrichtung von dualem Schreiben aus Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="49be9-103">Dual-write setup from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="49be9-104">In diesem Thema wird erläutert, wie Sie eine Verbindung für duales Schreiben über Microsoft Dynamics Lifecycle Services (LCS) aktivieren.</span><span class="sxs-lookup"><span data-stu-id="49be9-104">This topic explains how to enable dual-write from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="49be9-105">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="49be9-105">Prerequisites</span></span>

<span data-ttu-id="49be9-106">Sie müssen die Power Platform Integration wie in den folgenden Themen beschrieben ausfüllen:</span><span class="sxs-lookup"><span data-stu-id="49be9-106">You must complete the Power Platform integration as described in the following topics:</span></span>

+ [<span data-ttu-id="49be9-107">Power Platform Integration – Aktivieren Sie diese Option während der Bereitstellung der Umgebung</span><span class="sxs-lookup"><span data-stu-id="49be9-107">Power Platform Integration - Enable during environment deployment</span></span>](../../power-platform/overview.md#enable-during-environment-deployment)
+ [<span data-ttu-id="49be9-108">Power Platform Integration – Richten Sie diese Option nach der Bereitstellung der Umgebung ein</span><span class="sxs-lookup"><span data-stu-id="49be9-108">Power Platform integration - Set up after environment deployment</span></span>](../../power-platform/overview.md#set-up-after-environment-deployment)

## <a name="set-up-dual-write-for-new-dataverse-environments"></a><span data-ttu-id="49be9-109">Richten Sie duales Schreiben für neue Dataverse Umgebungen ein</span><span class="sxs-lookup"><span data-stu-id="49be9-109">Set up dual-write for new Dataverse environments</span></span>

<span data-ttu-id="49be9-110">Befolgen Sie diese Schritte, um duales Schreiben von der LCS -Seite **Umgebungsdetails** einzurichten:</span><span class="sxs-lookup"><span data-stu-id="49be9-110">Follow these steps to set up dual-write from LCS **Environment Details** page:</span></span>

1. <span data-ttu-id="49be9-111">Auf der Seite **Umgebungsdetails** erweitern Sie den Abschnitt **Power Platform Integration**.</span><span class="sxs-lookup"><span data-stu-id="49be9-111">On the **Environment Details** page, expand the **Power Platform Integration** section.</span></span>

2. <span data-ttu-id="49be9-112">Wählen Sie die Schaltfläche **Duale Schreibanwendung** aus.</span><span class="sxs-lookup"><span data-stu-id="49be9-112">Select the **Dual-write application** button.</span></span>

    ![Power Platform-Integration](media/powerplat_integration_step2.png)

3. <span data-ttu-id="49be9-114">Lesen Sie die allgemeinen Geschäftsbedingungen und wählen Sie **Konfigurieren** aus.</span><span class="sxs-lookup"><span data-stu-id="49be9-114">Review the terms and conditions, and then select **Configure**.</span></span>

4. <span data-ttu-id="49be9-115">Wählen Sie **OK**, um fortzufahren.</span><span class="sxs-lookup"><span data-stu-id="49be9-115">Select **OK** to continue.</span></span>

5. <span data-ttu-id="49be9-116">Sie können den Fortschritt überwachen, indem Sie die Seite mit den Umgebungsdetails regelmäßig aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="49be9-116">You can monitor the progress by periodically refreshing the environment details page.</span></span> <span data-ttu-id="49be9-117">Die Einrichtung dauert normalerweise 30 Minuten oder weniger.</span><span class="sxs-lookup"><span data-stu-id="49be9-117">Setup typically takes 30 minutes or less.</span></span>  

6. <span data-ttu-id="49be9-118">Nach Abschluss der Einrichtung werden Sie in einer Meldung darüber informiert, ob der Vorgang erfolgreich war oder ob ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="49be9-118">When the setup is complete, a message will inform you if the process was successful or if there was a failure.</span></span> <span data-ttu-id="49be9-119">Wenn die Einrichtung fehlgeschlagen ist, wird eine entsprechende Fehlermeldung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="49be9-119">If the setup failed, then a related error message is displayed.</span></span> <span data-ttu-id="49be9-120">Sie müssen alle Fehler beheben, bevor Sie mit dem nächsten Schritt fortfahren können.</span><span class="sxs-lookup"><span data-stu-id="49be9-120">You must fix any errors before moving to the next step.</span></span>

7. <span data-ttu-id="49be9-121">Wählen Sie **Link zur Power Platform Umgebung**, um eine Verbindung zwischen Dataverse und der aktuellen Umgebung der Datenbank zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="49be9-121">Select **Link to Power Platform environment** to create a link between Dataverse and the current environment's databases.</span></span> <span data-ttu-id="49be9-122">Diese Einrichtung dauert normalerweise 5 Minuten oder weniger.</span><span class="sxs-lookup"><span data-stu-id="49be9-122">This typically takes less than 5 minutes.</span></span>

    :::image type="content" source="media/powerplat_integration_step3.png" alt-text="Link zur Power Platform Umgebung":::

8. <span data-ttu-id="49be9-124">Wenn die Verknüpfung abgeschlossen ist, wird ein Hyperlink angezeigt.</span><span class="sxs-lookup"><span data-stu-id="49be9-124">When the linking is complete, a hyperlink is displayed.</span></span> <span data-ttu-id="49be9-125">Verwenden Sie den Link, um sich im Verwaltungsbereich mit zwei Schreibvorgängen in der Finance and Operations Umgebung zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="49be9-125">Use the link to sign in to the dual-write administration area in the Finance and Operations environment.</span></span> <span data-ttu-id="49be9-126">Von dort aus können Sie Entitätszuordnungen einrichten.</span><span class="sxs-lookup"><span data-stu-id="49be9-126">From there, you can set up entity mappings.</span></span>

## <a name="set-up-dual-write-for-an-existing-dataverse-environment"></a><span data-ttu-id="49be9-127">Richten Sie duales Schreiben für eine bestehende Dataverse Umgebung ein</span><span class="sxs-lookup"><span data-stu-id="49be9-127">Set up dual-write for an existing Dataverse environment</span></span>

<span data-ttu-id="49be9-128">Um duales Schreiben für eine vorhandene Dataverse Umgebung einzurichten, müssen Sie ein Microsoft [Supportticket](../../lifecycle-services/lcs-support.md) erstellen.</span><span class="sxs-lookup"><span data-stu-id="49be9-128">To set up dual-write for an existing Dataverse environment, you must create a Microsoft [support ticket](../../lifecycle-services/lcs-support.md).</span></span> <span data-ttu-id="49be9-129">Das Ticket muss enthalten:</span><span class="sxs-lookup"><span data-stu-id="49be9-129">The ticket must include:</span></span>

+ <span data-ttu-id="49be9-130">Ihre Finance and Operations Umgebungs-ID.</span><span class="sxs-lookup"><span data-stu-id="49be9-130">Your Finance and Operations environment ID.</span></span>
+ <span data-ttu-id="49be9-131">Ihr Umgebungsname von Lifecycle Services.</span><span class="sxs-lookup"><span data-stu-id="49be9-131">Your environment name from Lifecycle Services.</span></span>
+ <span data-ttu-id="49be9-132">Die Dataverse Organisations-ID oder Power Platform Umgebungs-ID vom Power Platform Admin Center.</span><span class="sxs-lookup"><span data-stu-id="49be9-132">The Dataverse organization ID or Power Platform Environment ID from Power Platform Admin Center.</span></span> <span data-ttu-id="49be9-133">Fordern Sie in Ihrem Ticket an, dass die ID die Instanz ist, die für die Power Platform Integration verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="49be9-133">In your ticket, request that the ID be the instance used for Power Platform integration.</span></span>

> [!NOTE]
> <span data-ttu-id="49be9-134">Sie können die Verknüpfung von Umgebungen mit LCS nicht aufheben.</span><span class="sxs-lookup"><span data-stu-id="49be9-134">You can't unlink environments by using LCS.</span></span> <span data-ttu-id="49be9-135">Um die Verknüpfung einer Umgebung aufzuheben, öffnen Sie den **Datenintegration** Arbeitsbereich in der Finance and Operations Umgebung und wählen Sie dann **Verknüpfung aufheben**.</span><span class="sxs-lookup"><span data-stu-id="49be9-135">To unlink an environment, open the **Data integration** workspace in the Finance and Operations environment, and then select **Unlink**.</span></span>

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
