---
title: Leitfaden zur Problembehandlung für die Datenintegration
description: Dieses Thema enthält Problembehandlungsinformationen zur Datenintegration zwischen Microsoft Dynamics 365 for Finance and Operations und Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
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
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 5e71729dafd2ad85a01b055363d1c7056b5558b2
ms.sourcegitcommit: 3f05ede8b8acdf0550240a83a013e093b4ad043d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2019
ms.locfileid: "1873104"
---
# <a name="troubleshooting-guide-for-data-integration"></a><span data-ttu-id="abebf-103">Leitfaden zur Problembehandlung für die Datenintegration</span><span class="sxs-lookup"><span data-stu-id="abebf-103">Troubleshooting guide for data integration</span></span>

## <a name="enable-plug-in-trace-logs-in-common-data-service-and-inspect-the-dual-write-plug-in-error-details"></a><span data-ttu-id="abebf-104">Aktivieren der Plug-In-Ablaufverfolgungsprotokolle in Common Data Service und Überprüfen der Plug-In-Fehlerdetails für duales Schreiben</span><span class="sxs-lookup"><span data-stu-id="abebf-104">Enable plug-in trace logs in Common Data Service and inspect the dual-write plug-in error details</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="abebf-105">Sollte ein Problem oder Fehler bei der Synchronisierung des dualen Schreibens auftreten, führen Sie die folgenden Schritte aus, um die Fehler im Ablaufverfolgungsprotokoll zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="abebf-105">If you experience an issue or error during dual-write synchronization, follow these steps to inspect the errors in the trace log.</span></span>

1. <span data-ttu-id="abebf-106">Bevor Sie die Fehler überprüfen können, müssen Sie Plug-In-Ablaufverfolgungsprotokolle aktivieren.</span><span class="sxs-lookup"><span data-stu-id="abebf-106">Before you can inspect the errors, you must enable plug-in trace logs.</span></span> <span data-ttu-id="abebf-107">Anweisungen finden Sie im Abschnitt „Ablaufverfolgungsprotokolle anzeigen“ im [Tutorial: Schreiben und Registrieren eines Plug-Ins](https://docs.microsoft.com/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs).</span><span class="sxs-lookup"><span data-stu-id="abebf-107">For instructions, see the "View trace logs" section of [Tutorial: Write and register a plug-in](https://docs.microsoft.com/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs).</span></span>

    <span data-ttu-id="abebf-108">Jetzt können Sie die Fehler überprüfen.</span><span class="sxs-lookup"><span data-stu-id="abebf-108">You can now inspect the errors.</span></span>

2. <span data-ttu-id="abebf-109">Melden Sie sich bei Microsoft Dynamics 365 for Sales an.</span><span class="sxs-lookup"><span data-stu-id="abebf-109">Sign in to Microsoft Dynamics 365 for Sales.</span></span>
3. <span data-ttu-id="abebf-110">Wählen Sie die Schaltfläche **Einstellungen** (das Zahnradsymbol) aus, und wählen Sie dann **Erweiterte Einstellungen** aus.</span><span class="sxs-lookup"><span data-stu-id="abebf-110">Select the **Settings** button (the gear symbol), and then select **Advanced Settings**.</span></span>
4. <span data-ttu-id="abebf-111">Wählen Sie im Menü **Einstellungen** die Option **Anpassung \> Plug-In-Ablaufverfolgungsprotokoll**.</span><span class="sxs-lookup"><span data-stu-id="abebf-111">On the **Settings** menu, select **Customization \> Plug-In Trace Log**.</span></span>
5. <span data-ttu-id="abebf-112">Wählen Sie **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** als Typnamen aus, um die Fehlerdetails anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="abebf-112">Select **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** as the type name to show the error details.</span></span>

## <a name="inspect-dual-write-synchronization-errors-in-finance-and-operations"></a><span data-ttu-id="abebf-113">Überprüfen von Synchronisierungsfehlern beim dualen Schreiben in Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="abebf-113">Inspect dual-write synchronization errors in Finance and Operations</span></span>

<span data-ttu-id="abebf-114">Gehen Sie folgendermaßen vor, um während des Testens Fehler zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="abebf-114">Follow these steps to inspect errors during testing.</span></span>

1. <span data-ttu-id="abebf-115">Melden Sie sich bei Microsoft Dynamics Lifecycle Services (LCS) an.</span><span class="sxs-lookup"><span data-stu-id="abebf-115">Sign in to Microsoft Dynamics Lifecycle Services (LCS).</span></span>
2. <span data-ttu-id="abebf-116">Öffnen Sie das LCS-Projekt, wofür der Test für das duale Schreiben durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="abebf-116">Open the LCS project to do dual-write testing for.</span></span>
3. <span data-ttu-id="abebf-117">Wählen Sie **In der Cloud gehostete Umgebungen** aus.</span><span class="sxs-lookup"><span data-stu-id="abebf-117">Select **Cloud-hosted environments**.</span></span>
4. <span data-ttu-id="abebf-118">Stellen Sie eine Remote Desktop-Verbindung mit dem virtuellen Dynamics 365 for Finance and Operations-Computer her, indem Sie lokales Konto verwenden, das in LCS angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="abebf-118">Make a Remote desktop connection to the Dynamics 365 for Finance and Operations virtual machine (VM) by using local account that is shown in LCS.</span></span>
5. <span data-ttu-id="abebf-119">Öffnen Sie die Ereignisanzeige.</span><span class="sxs-lookup"><span data-stu-id="abebf-119">Open Event Viewer.</span></span> 
6. <span data-ttu-id="abebf-120">Gehen Sie zu **Anwendungs- und Dienstprotokolle \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operativ**.</span><span class="sxs-lookup"><span data-stu-id="abebf-120">Go to **Applications and Services Logs \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operational**.</span></span> <span data-ttu-id="abebf-121">Die Fehler und Details werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="abebf-121">The errors and details are shown.</span></span>

## <a name="unlink-one-common-data-service-environment-from-finance-and-operations-and-link-another-environment"></a><span data-ttu-id="abebf-122">Aufheben einer Common Data Service-Umgebungs-Verknüpfung von Finance and Operations und Verknüpfung einer anderen Umgebung</span><span class="sxs-lookup"><span data-stu-id="abebf-122">Unlink one Common Data Service environment from Finance and Operations and link another environment</span></span>

<span data-ttu-id="abebf-123">Um Verknüpfungen zu aktualisieren, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="abebf-123">Follow these steps to update links.</span></span>

1. <span data-ttu-id="abebf-124">Gehen Sie zur Finance and Operations-Umgebung.</span><span class="sxs-lookup"><span data-stu-id="abebf-124">Go to the Finance and Operations environment.</span></span>
2. <span data-ttu-id="abebf-125">Öffnen Sie die Datenverwaltung.</span><span class="sxs-lookup"><span data-stu-id="abebf-125">Open Data Management.</span></span>
3. <span data-ttu-id="abebf-126">Wählen Sie **Verknüpfung zu CDS für Apps** aus.</span><span class="sxs-lookup"><span data-stu-id="abebf-126">Select **Link to CDS for apps**.</span></span>
4. <span data-ttu-id="abebf-127">Wählen Sie alle Zuordnungen aus, die ausgeführt werden, und wählen Sie dann **Beenden** aus.</span><span class="sxs-lookup"><span data-stu-id="abebf-127">Select all the mappings that are running, and then select **Stop**.</span></span>
5. <span data-ttu-id="abebf-128">Wählen Sie alle Zuordnungen und dann **Löschen** aus.</span><span class="sxs-lookup"><span data-stu-id="abebf-128">Select all the mappings, and then select **Delete**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="abebf-129">Die Option **Löschen** ist nicht verfügbar, wenn die Vorlage **CustomerV3-Account** ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="abebf-129">The **Delete** option isn't available if the **CustomerV3-Account** template is selected.</span></span> <span data-ttu-id="abebf-130">Heben Sie die Auswahl dieser Vorlage nach Bedarf auf.</span><span class="sxs-lookup"><span data-stu-id="abebf-130">Clear the selection of this template as required.</span></span> <span data-ttu-id="abebf-131">**CustomerV3-Account** ist eine ältere bereitgestellte Vorlage und funktioniert mit der Prospect to Cash-Lösung.</span><span class="sxs-lookup"><span data-stu-id="abebf-131">**CustomerV3-Account** is an older provisioned template and works with the Prospect to Cash solution.</span></span> <span data-ttu-id="abebf-132">Da es global veröffentlicht wird, wird es unter allen Vorlagen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="abebf-132">Because it's globally released, it appears under all templates.</span></span>

6. <span data-ttu-id="abebf-133">Wählen Sie **Verknüpfung für Umgebung aufheben** aus.</span><span class="sxs-lookup"><span data-stu-id="abebf-133">Select **Unlink environment**.</span></span>
7. <span data-ttu-id="abebf-134">Wählen Sie **Ja** aus, um den Vorgang zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="abebf-134">Select **Yes** to confirm the operation.</span></span>
8. <span data-ttu-id="abebf-135">Um die neue Umgebung zu verknüpfen, führen Sie die Schritte unter [Installationsleitfaden](https://aka.ms/dualwrite-docs) aus.</span><span class="sxs-lookup"><span data-stu-id="abebf-135">To link the new environment, follow the steps in the [installation guide](https://aka.ms/dualwrite-docs).</span></span>
