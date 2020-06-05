---
title: IoT-Intelligenz-Add-In in LCS installieren
description: In diesem Thema wird erläutert, wie Sie das IoT-Intelligenz-Add-In in Microsoft Dynamics Lifecycle Services (LCS) installieren.
author: robinarh
manager: AnnBe
ms.date: 08/16/2019
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
ms.openlocfilehash: 04333b3659f090b15cc0d0ee216f14dabc588883
ms.sourcegitcommit: 261b70ea358b2c231e20f320ed8bd6adc1e7d715
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/19/2020
ms.locfileid: "3386517"
---
# <a name="install-the-iot-intelligence-add-in-in-lcs"></a><span data-ttu-id="87b70-103">IoT-Intelligenz-Add-In in LCS installieren</span><span class="sxs-lookup"><span data-stu-id="87b70-103">Install the IoT Intelligence add-in in LCS</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="87b70-104">In diesem Thema wird erläutert, wie Sie das IoT-Intelligenz-Add-In in Microsoft Dynamics Lifecycle Services (LCS) installieren.</span><span class="sxs-lookup"><span data-stu-id="87b70-104">This topic explains how to install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="87b70-105">Bevor Sie das Add-In installieren können, müssen Sie die [Azure-Ressourcen erstellen](iot-azure-setup.md).</span><span class="sxs-lookup"><span data-stu-id="87b70-105">Before you can install the add-in, you must [create the Azure resources](iot-azure-setup.md).</span></span>

## <a name="set-up-the-lcs-environment"></a><span data-ttu-id="87b70-106">LCS-Umgebung einrichten</span><span class="sxs-lookup"><span data-stu-id="87b70-106">Set up the LCS environment</span></span>

1. <span data-ttu-id="87b70-107">Öffnen Sie LCS, und wechseln Sie zu Ihrer Microsoft Dynamics 365 Supply Chain Management-Umgebung.</span><span class="sxs-lookup"><span data-stu-id="87b70-107">Open LCS, and go to your Microsoft Dynamics 365 Supply Chain Management environment.</span></span>
2. <span data-ttu-id="87b70-108">Scrollen Sie zum Abschnitt **Umgebungs-Add-Ins**.</span><span class="sxs-lookup"><span data-stu-id="87b70-108">Scroll to the **Environment add-ins** section.</span></span>
3. <span data-ttu-id="87b70-109">Wählen Sie **Neues Add-In installieren** aus, um die Liste der Add-Ins anzuzeigen, die für die Umgebung aktiviert wurden.</span><span class="sxs-lookup"><span data-stu-id="87b70-109">Select **Install a new add-in** to show the list of add-ins that have been enabled for the environment.</span></span>
4. <span data-ttu-id="87b70-110">Wählen Sie im Dialogfeld **Zu installierendes Add-In auswählen** die Option **IoT-Intelligenz** aus.</span><span class="sxs-lookup"><span data-stu-id="87b70-110">In the **Select an add-in to install** dialog box, select **IoT Intelligence**.</span></span>
5. <span data-ttu-id="87b70-111">Geben Sie im Dialogfeld **Add-In einrichten** die Details Ihres IoT-Hubs und Redis-Caches an.</span><span class="sxs-lookup"><span data-stu-id="87b70-111">In the **Setup add-in** dialog box, provide the details of your IoT hub and Redis cache.</span></span> <span data-ttu-id="87b70-112">Sie finden die erforderlichen Werte im Schlüsseltresor, den Sie unter [Azure-Ressourcen erstellen](iot-azure-setup.md) erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="87b70-112">You can find the required values in the key vault that you created in [Create Azure resources](iot-azure-setup.md).</span></span>

    + <span data-ttu-id="87b70-113">**Mandanten-ID** – Wechseln Sie im Azure-Portal zum Schlüsseltresor, wählen Sie dann im linken Navigationsbereich **Übersicht** aus, und kopieren Sie den Wert **Verzeichnis-ID**.</span><span class="sxs-lookup"><span data-stu-id="87b70-113">**Tenant ID** – In the Azure portal, go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **Directory ID** value.</span></span> <span data-ttu-id="87b70-114">Fügen Sie diesen Wert in das Dialogfeld **Add-In einrichten** ein.</span><span class="sxs-lookup"><span data-stu-id="87b70-114">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="87b70-115">**Schlüsseltresor-URI des IoT-Event Hub-kompatiblen Endpunkts** – Wechseln Sie zum Schlüsseltresor, wählen Sie dann im linken Navigationsbereich **Übersicht** aus, und kopieren Sie den Wert für **DNS-Name**.</span><span class="sxs-lookup"><span data-stu-id="87b70-115">**IoT Event Hub-compatible endpoint Key Vault URI** – Go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **DNS name** value.</span></span> <span data-ttu-id="87b70-116">Fügen Sie diesen Wert in das Dialogfeld **Add-In einrichten** ein.</span><span class="sxs-lookup"><span data-stu-id="87b70-116">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="87b70-117">**Geheimer Schlüssel des IoT-Event-Hub-kompatiblen Endpunkts** – Wechseln Sie zum Schlüsseltresor, wählen Sie dann im linken Navigationsbereich **Geheime Schlüssel** aus, und kopieren Sie den Namen des geheimen Schlüssels, in dem die Event-Hub-Verbindungszeichenfolge für den IoT-Hub gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="87b70-117">**IoT Event Hub-compatible endpoint secret name** – Go to the key vault, and then, in the left navigation pane, select **Secrets**, and copy the name of the secret where the event hub connection string for the IoT hub is stored.</span></span> <span data-ttu-id="87b70-118">Fügen Sie diesen Wert in das Dialogfeld **Add-In einrichten** ein.</span><span class="sxs-lookup"><span data-stu-id="87b70-118">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="87b70-119">**Schlüsseltresor-URI des Redis-Caches** – Wechseln Sie zum Schlüsseltresor, wählen Sie dann im linken Navigationsbereich **Übersicht** aus, und kopieren Sie den Wert für **DNS-Name**.</span><span class="sxs-lookup"><span data-stu-id="87b70-119">**Redis cache key vault URI** – Go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **DNS name** value.</span></span> <span data-ttu-id="87b70-120">Fügen Sie diesen Wert in das Dialogfeld **Add-In einrichten** ein.</span><span class="sxs-lookup"><span data-stu-id="87b70-120">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="87b70-121">**Name des geheimen Schlüssels des Redis-Cache-Endpunkts** – Wechseln Sie zum Schlüsseltresor, wählen Sie dann im linken Navigationsbereich **Geheime Schlüssel** aus, und kopieren Sie den Namen des geheimen Schlüssels, in dem die Event-Hub-Verbindungszeichenfolge für den Redis-Cache gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="87b70-121">**Redis cache endpoint secret name** – Go to the key vault, and then, in the left navigation pane, select **Secrets**, and copy the name of the secret where the connection string for the Redis cache is stored.</span></span> <span data-ttu-id="87b70-122">Fügen Sie diesen Wert in das Dialogfeld **Add-In einrichten** ein.</span><span class="sxs-lookup"><span data-stu-id="87b70-122">Paste that value in the **Setup add-in** dialog box.</span></span>

6. <span data-ttu-id="87b70-123">Aktivieren Sie das Kontrollkästchen, um die allgemeinen Geschäftsbedingungen zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="87b70-123">Select the check box to accept the terms and conditions.</span></span>
7. <span data-ttu-id="87b70-124">Wählen Sie **Installieren**.</span><span class="sxs-lookup"><span data-stu-id="87b70-124">Select **Install**.</span></span>
8. <span data-ttu-id="87b70-125">Es wird ein Meldungsfeld mit dem Inhalt „Add-In wurde erfolgreich für die Installation ausgelöst“ angezeigt.</span><span class="sxs-lookup"><span data-stu-id="87b70-125">A message box appears that states, "Add-in has been successfully triggered for installation."</span></span> <span data-ttu-id="87b70-126">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="87b70-126">Select **OK**.</span></span>

<span data-ttu-id="87b70-127">Die LCS-Einrichtung ist nun abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="87b70-127">LCS setup is now completed.</span></span> <span data-ttu-id="87b70-128">Als Nächstes muss der Schritt [Szenarien einrichten](iot-scenario-setup.md) ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="87b70-128">The next step is to [set up the scenarios](iot-scenario-setup.md).</span></span>

## <a name="uninstall-the-add-in"></a><a id="uninstall-addin"></a><span data-ttu-id="87b70-129">Add-In deinstallieren</span><span class="sxs-lookup"><span data-stu-id="87b70-129">Uninstall the add-in</span></span>

1. <span data-ttu-id="87b70-130">Führen Sie in Supply Chain Management den Schritt [Szenarien deaktivieren](iot-scenario-setup.md#how-to-disable-a-scenario) aus.</span><span class="sxs-lookup"><span data-stu-id="87b70-130">In Supply Chain Management, [disable the scenarios](iot-scenario-setup.md#how-to-disable-a-scenario).</span></span>
2. <span data-ttu-id="87b70-131">Wechseln Sie in LCS zu den Details Ihrer Supply Chain Management-Umgebung.</span><span class="sxs-lookup"><span data-stu-id="87b70-131">In LCS, go to your Supply Chain Management environment details.</span></span>
3. <span data-ttu-id="87b70-132">Scrollen Sie zum Abschnitt **Umgebungs-Add-Ins**.</span><span class="sxs-lookup"><span data-stu-id="87b70-132">Scroll to the **Environment add-ins** section.</span></span>
4. <span data-ttu-id="87b70-133">Wählen Sie für das IoT-Intelligenz-Add-In **Deinstallieren** aus.</span><span class="sxs-lookup"><span data-stu-id="87b70-133">Select **Uninstall** for the IoT Intelligence add-in.</span></span>
