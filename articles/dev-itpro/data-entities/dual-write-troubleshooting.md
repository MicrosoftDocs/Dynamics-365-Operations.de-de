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
ms.openlocfilehash: ca62a6b3aa64ec2383ee3ded3b7bbf4650a41166
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797274"
---
# <a name="troubleshooting-guide-for-data-integration"></a><span data-ttu-id="3ae31-103">Leitfaden zur Problembehandlung für die Datenintegration</span><span class="sxs-lookup"><span data-stu-id="3ae31-103">Troubleshooting guide for data integration</span></span>

## <a name="enable-plugin-trace-in-common-data-service-and-check-the-dual-write-plugin-error-details"></a><span data-ttu-id="3ae31-104">Aktivieren der Plug-In-Ablaufverfolgung in Common Data Service und Überprüfen der Plug-In-Fehlerdetails für duales Schreiben</span><span class="sxs-lookup"><span data-stu-id="3ae31-104">Enable Plugin Trace in Common Data Service and check the dual-write Plugin error details</span></span>

<span data-ttu-id="3ae31-105">Wenn Sie bei der Synchronisierung des dualen Schreibens ein Problem haben oder ein Fehler auftritt, können Sie die Fehler im Ablaufverfolgungsprotokoll überprüfen:</span><span class="sxs-lookup"><span data-stu-id="3ae31-105">If you are facing an issue or error with dual-write synchronization, you can inspect the errors in the trace log:</span></span>

1. <span data-ttu-id="3ae31-106">Bevor Sie die Fehler überprüfen können, müssen Sie die Plug-In-Ablaufverfolgung mithilfe der Anweisungen unter [Plug-In registrieren](https://docs.microsoft.com/en-us/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs) aktivieren.</span><span class="sxs-lookup"><span data-stu-id="3ae31-106">Before you can inspect the errors, you must enable Plugin trace using the instructions in [Register plug-in](https://docs.microsoft.com/en-us/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs) to enable Plugin trace.</span></span> <span data-ttu-id="3ae31-107">Jetzt können Sie die Fehler überprüfen.</span><span class="sxs-lookup"><span data-stu-id="3ae31-107">Now you can inspect the errors.</span></span>
2. <span data-ttu-id="3ae31-108">Melden Sie sich bei Dynamics 365 for Sales an.</span><span class="sxs-lookup"><span data-stu-id="3ae31-108">Login to Dynamics 365 for Sales.</span></span>
3. <span data-ttu-id="3ae31-109">Klicken Sie auf das Einstellungssymbol (ein Zahnrad), und wählen Sie **Erweiterte Einstellungen** aus.</span><span class="sxs-lookup"><span data-stu-id="3ae31-109">Click on the Settings icon (a gear), and select **Advanced Settings**.</span></span>
4. <span data-ttu-id="3ae31-110">Wählen Sie im Menü **Einstellungen** die Option **Anpassung > Plug-In-Ablaufverfolgungsprotokoll** aus.</span><span class="sxs-lookup"><span data-stu-id="3ae31-110">In the **Settings** menu, choose **Customization > Plug-In Trace Log**.</span></span>
5. <span data-ttu-id="3ae31-111">Klicken Sie auf den Typnamen **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin**, um die Fehlerdetails anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="3ae31-111">Click the type name **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** to display the error details.</span></span>

## <a name="check-dual-write-synchronization-errors-in-finance-and-operations"></a><span data-ttu-id="3ae31-112">Überprüfen von Synchronisierungsfehlern beim dualen Schreiben in Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="3ae31-112">Check dual-write synchronization errors in Finance and Operations</span></span>

<span data-ttu-id="3ae31-113">Sie können die Fehler während des Testens überprüfen, indem Sie die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="3ae31-113">You can check the errors during testing by following these steps:</span></span>

+ <span data-ttu-id="3ae31-114">Melden Sie sich bei LifeCycle Services (LCS) an.</span><span class="sxs-lookup"><span data-stu-id="3ae31-114">Login to LifeCycle Services (LCS).</span></span>
+ <span data-ttu-id="3ae31-115">Öffnet das LCS-Projekt, das Sie ausgewählt haben, um das Testing für das duale Schreiben durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="3ae31-115">Open the LCS project that you chose to perform dual-write testing.</span></span>
+ <span data-ttu-id="3ae31-116">Gehen Sie zu den in der Cloud gehosteten Umgebungen.</span><span class="sxs-lookup"><span data-stu-id="3ae31-116">Go to Cloud Hosted Environments.</span></span>
+ <span data-ttu-id="3ae31-117">Stellen Sie über Remotedesktop eine Verbindung zum Finance and Operations-VM mithilfe des lokalen Kontos her, das in LCS angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="3ae31-117">Remote desktop to Finance and Operations VM using local account that is displayed in LCS.</span></span>
+ <span data-ttu-id="3ae31-118">Öffnen Sie die Ereignisanzeige.</span><span class="sxs-lookup"><span data-stu-id="3ae31-118">Open the event viewer.</span></span> 
+ <span data-ttu-id="3ae31-119">Navigieren Sie zu **Anwendungs- und Dienstprotokolle > Microsoft > Dynamics > AX-DualWriteSync > Operativ**.</span><span class="sxs-lookup"><span data-stu-id="3ae31-119">Navigate to **Applications and Services logs > Microsoft > Dynamics > AX-DualWriteSync > Operational**.</span></span> <span data-ttu-id="3ae31-120">Die Fehler und Details werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3ae31-120">The errors and details are displayed.</span></span>

## <a name="how-to-unlink-and-link-another-common-data-service-environment-from-finance-and-operations"></a><span data-ttu-id="3ae31-121">Vorgehensweise zum Herstellen und Aufhaben einer Verknüpfung zu einer anderen Common Data Service-Umgebung von Finance and Operations aus</span><span class="sxs-lookup"><span data-stu-id="3ae31-121">How to unlink and link another Common Data Service environment from Finance and Operations</span></span>

<span data-ttu-id="3ae31-122">Sie können Links aktualisieren, indem Sie die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="3ae31-122">You can update links by following these steps:</span></span>

+ <span data-ttu-id="3ae31-123">Navigieren Sie zur Finance and Operations-Umgebung.</span><span class="sxs-lookup"><span data-stu-id="3ae31-123">Navigate to the Finance and Operations environment.</span></span>
+ <span data-ttu-id="3ae31-124">Öffnen Sie die Datenverwaltung.</span><span class="sxs-lookup"><span data-stu-id="3ae31-124">Open Data Management.</span></span>
+ <span data-ttu-id="3ae31-125">Klicken Sie auf **Verknüpfung zu CDS für Apps**.</span><span class="sxs-lookup"><span data-stu-id="3ae31-125">Click on **Link to CDS for apps**.</span></span>
+ <span data-ttu-id="3ae31-126">Wählen Sie alle ausgeführten Zuordnungen aus, und klicken Sie auf **Beenden**.</span><span class="sxs-lookup"><span data-stu-id="3ae31-126">Select all the running mappings and click **Stop**.</span></span> 
+ <span data-ttu-id="3ae31-127">Wählen Sie alle Zuordnungen aus, und klicken Sie auf **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="3ae31-127">Select all the mappings and click **Delete**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3ae31-128">Die Option **Löschen** wird nicht angezeigt, wenn die Vorlage **CustomerV3-Account** ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="3ae31-128">The **Delete** option will not appear if **CustomerV3-Account** template is selected.</span></span> <span data-ttu-id="3ae31-129">Heben Sie die Auswahl bei Bedarf auf.</span><span class="sxs-lookup"><span data-stu-id="3ae31-129">Unselect it if needed.</span></span> <span data-ttu-id="3ae31-130">**CustomerV3-Account** ist eine ältere bereitgestellte Vorlage und funktioniert mit der Prospect to Cash-Lösung.</span><span class="sxs-lookup"><span data-stu-id="3ae31-130">**CustomerV3-Account** is an older provisioned template and works with the Prospect to Cash solution.</span></span> <span data-ttu-id="3ae31-131">Da es global veröffentlicht wird, wird es unter allen Vorlagen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3ae31-131">Because it is globally released, it shows up under all templates.</span></span>

+ <span data-ttu-id="3ae31-132">Klicken Sie auf **Verknüpfung für Umgebung aufheben**.</span><span class="sxs-lookup"><span data-stu-id="3ae31-132">Click **Unlink environment**.</span></span>
+ <span data-ttu-id="3ae31-133">Klicken Sie zur Bestätigung auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="3ae31-133">Click **Yes** for confirmation.</span></span>
+ <span data-ttu-id="3ae31-134">Um die neue Umgebung zu verknüpfen, führen Sie die Schritte unter [Installationsleitfaden](https://aka.ms/dualwrite-docs) aus.</span><span class="sxs-lookup"><span data-stu-id="3ae31-134">To link the new environment, follow the steps in the [installation guide](https://aka.ms/dualwrite-docs).</span></span>

