---
title: IoT-Intelligenz-Add-In in LCS installieren
description: In diesem Thema wird erläutert, wie Sie das IoT-Intelligenz-Add-In in Microsoft Dynamics Lifecycle Services (LCS) installieren.
author: robinarh
manager: tfehr
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: ''
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d2bcbf69362e4ca3a156d1d404e15489ddb3f0d0
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597215"
---
# <a name="install-the-iot-intelligence-add-in-in-lcs"></a><span data-ttu-id="320c1-103">IoT-Intelligenz-Add-In in LCS installieren</span><span class="sxs-lookup"><span data-stu-id="320c1-103">Install the IoT Intelligence add-in in LCS</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="320c1-104">In diesem Thema wird erläutert, wie Sie das IoT-Intelligenz-Add-In in Microsoft Dynamics Lifecycle Services (LCS) installieren.</span><span class="sxs-lookup"><span data-stu-id="320c1-104">This topic explains how to install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="320c1-105">Beachten Sie, dass Add-Ins nicht in einer Demo-/Testversionsumgebung installiert werden können.</span><span class="sxs-lookup"><span data-stu-id="320c1-105">Note that add-ins cannot be installed on a demo/trial environment.</span></span> <span data-ttu-id="320c1-106">Bevor Sie das Add-In installieren können, müssen Sie die [Azure-Ressourcen erstellen](iot-azure-setup.md).</span><span class="sxs-lookup"><span data-stu-id="320c1-106">Before you can install the add-in, you must [create the Azure resources](iot-azure-setup.md).</span></span>

## <a name="set-up-the-lcs-environment"></a><span data-ttu-id="320c1-107">LCS-Umgebung einrichten</span><span class="sxs-lookup"><span data-stu-id="320c1-107">Set up the LCS environment</span></span>

1. <span data-ttu-id="320c1-108">Öffnen Sie LCS, und wechseln Sie zu Ihrer Microsoft Dynamics 365 Supply Chain Management-Umgebung.</span><span class="sxs-lookup"><span data-stu-id="320c1-108">Open LCS, and go to your Microsoft Dynamics 365 Supply Chain Management environment.</span></span>
2. <span data-ttu-id="320c1-109">Scrollen Sie zum Abschnitt **Umgebungs-Add-Ins**.</span><span class="sxs-lookup"><span data-stu-id="320c1-109">Scroll to the **Environment add-ins** section.</span></span>
3. <span data-ttu-id="320c1-110">Wählen Sie **Neues Add-In installieren** aus, um die Liste der Add-Ins anzuzeigen, die für die Umgebung aktiviert wurden.</span><span class="sxs-lookup"><span data-stu-id="320c1-110">Select **Install a new add-in** to show the list of add-ins that have been enabled for the environment.</span></span>
4. <span data-ttu-id="320c1-111">Wählen Sie im Dialogfeld **Zu installierendes Add-In auswählen** die Option **IoT-Intelligenz** aus.</span><span class="sxs-lookup"><span data-stu-id="320c1-111">In the **Select an add-in to install** dialog box, select **IoT Intelligence**.</span></span>
5. <span data-ttu-id="320c1-112">Geben Sie im Dialogfeld **Add-In einrichten** die Details Ihres IoT-Hubs und Redis-Caches an.</span><span class="sxs-lookup"><span data-stu-id="320c1-112">In the **Setup add-in** dialog box, provide the details of your IoT hub and Redis cache.</span></span> <span data-ttu-id="320c1-113">Sie finden die erforderlichen Werte im Schlüsseltresor, den Sie unter [Azure-Ressourcen erstellen](iot-azure-setup.md) erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="320c1-113">You can find the required values in the key vault that you created in [Create Azure resources](iot-azure-setup.md).</span></span>

    + <span data-ttu-id="320c1-114">**Mandanten-ID** – Wechseln Sie im Azure-Portal zum Schlüsseltresor, wählen Sie dann im linken Navigationsbereich **Übersicht** aus, und kopieren Sie den Wert **Verzeichnis-ID**.</span><span class="sxs-lookup"><span data-stu-id="320c1-114">**Tenant ID** – In the Azure portal, go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **Directory ID** value.</span></span> <span data-ttu-id="320c1-115">Fügen Sie diesen Wert in das Dialogfeld **Add-In einrichten** ein.</span><span class="sxs-lookup"><span data-stu-id="320c1-115">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="320c1-116">**Schlüsseltresor-URI des IoT-Event Hub-kompatiblen Endpunkts** – Wechseln Sie zum Schlüsseltresor, wählen Sie dann im linken Navigationsbereich **Übersicht** aus, und kopieren Sie den Wert für **DNS-Name**.</span><span class="sxs-lookup"><span data-stu-id="320c1-116">**IoT Event Hub-compatible endpoint Key Vault URI** – Go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **DNS name** value.</span></span> <span data-ttu-id="320c1-117">Fügen Sie diesen Wert in das Dialogfeld **Add-In einrichten** ein.</span><span class="sxs-lookup"><span data-stu-id="320c1-117">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="320c1-118">**Geheimer Schlüssel des IoT-Event-Hub-kompatiblen Endpunkts** – Wechseln Sie zum Schlüsseltresor, wählen Sie dann im linken Navigationsbereich **Geheime Schlüssel** aus, und kopieren Sie den Namen des geheimen Schlüssels, in dem die Event-Hub-Verbindungszeichenfolge für den IoT-Hub gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="320c1-118">**IoT Event Hub-compatible endpoint secret name** – Go to the key vault, and then, in the left navigation pane, select **Secrets**, and copy the name of the secret where the event hub connection string for the IoT hub is stored.</span></span> <span data-ttu-id="320c1-119">Fügen Sie diesen Wert in das Dialogfeld **Add-In einrichten** ein.</span><span class="sxs-lookup"><span data-stu-id="320c1-119">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="320c1-120">**Schlüsseltresor-URI des Redis-Caches** – Wechseln Sie zum Schlüsseltresor, wählen Sie dann im linken Navigationsbereich **Übersicht** aus, und kopieren Sie den Wert für **DNS-Name**.</span><span class="sxs-lookup"><span data-stu-id="320c1-120">**Redis cache key vault URI** – Go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **DNS name** value.</span></span> <span data-ttu-id="320c1-121">Fügen Sie diesen Wert in das Dialogfeld **Add-In einrichten** ein.</span><span class="sxs-lookup"><span data-stu-id="320c1-121">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="320c1-122">**Name des geheimen Schlüssels des Redis-Cache-Endpunkts** – Wechseln Sie zum Schlüsseltresor, wählen Sie dann im linken Navigationsbereich **Geheime Schlüssel** aus, und kopieren Sie den Namen des geheimen Schlüssels, in dem die Event-Hub-Verbindungszeichenfolge für den Redis-Cache gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="320c1-122">**Redis cache endpoint secret name** – Go to the key vault, and then, in the left navigation pane, select **Secrets**, and copy the name of the secret where the connection string for the Redis cache is stored.</span></span> <span data-ttu-id="320c1-123">Fügen Sie diesen Wert in das Dialogfeld **Add-In einrichten** ein.</span><span class="sxs-lookup"><span data-stu-id="320c1-123">Paste that value in the **Setup add-in** dialog box.</span></span>

6. <span data-ttu-id="320c1-124">Aktivieren Sie das Kontrollkästchen, um die allgemeinen Geschäftsbedingungen zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="320c1-124">Select the check box to accept the terms and conditions.</span></span>
7. <span data-ttu-id="320c1-125">Wählen Sie **Installieren**.</span><span class="sxs-lookup"><span data-stu-id="320c1-125">Select **Install**.</span></span>
8. <span data-ttu-id="320c1-126">Es wird ein Meldungsfeld mit dem Inhalt „Add-In wurde erfolgreich für die Installation ausgelöst“ angezeigt.</span><span class="sxs-lookup"><span data-stu-id="320c1-126">A message box appears that states, "Add-in has been successfully triggered for installation."</span></span> <span data-ttu-id="320c1-127">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="320c1-127">Select **OK**.</span></span>

<span data-ttu-id="320c1-128">Die LCS-Einrichtung ist nun abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="320c1-128">LCS setup is now completed.</span></span> <span data-ttu-id="320c1-129">Als Nächstes muss der Schritt [Szenarien einrichten](iot-scenario-setup.md) ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="320c1-129">The next step is to [set up the scenarios](iot-scenario-setup.md).</span></span>

## <a name="uninstall-the-add-in"></a><a id="uninstall-addin"></a><span data-ttu-id="320c1-130">Add-In deinstallieren</span><span class="sxs-lookup"><span data-stu-id="320c1-130">Uninstall the add-in</span></span>

1. <span data-ttu-id="320c1-131">Führen Sie in Supply Chain Management den Schritt [Szenarien deaktivieren](iot-scenario-setup.md#how-to-disable-a-scenario) aus.</span><span class="sxs-lookup"><span data-stu-id="320c1-131">In Supply Chain Management, [disable the scenarios](iot-scenario-setup.md#how-to-disable-a-scenario).</span></span>
2. <span data-ttu-id="320c1-132">Wechseln Sie in LCS zu den Details Ihrer Supply Chain Management-Umgebung.</span><span class="sxs-lookup"><span data-stu-id="320c1-132">In LCS, go to your Supply Chain Management environment details.</span></span>
3. <span data-ttu-id="320c1-133">Scrollen Sie zum Abschnitt **Umgebungs-Add-Ins**.</span><span class="sxs-lookup"><span data-stu-id="320c1-133">Scroll to the **Environment add-ins** section.</span></span>
4. <span data-ttu-id="320c1-134">Wählen Sie für das IoT-Intelligenz-Add-In **Deinstallieren** aus.</span><span class="sxs-lookup"><span data-stu-id="320c1-134">Select **Uninstall** for the IoT Intelligence add-in.</span></span>
