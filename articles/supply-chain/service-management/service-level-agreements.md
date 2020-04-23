---
title: Übersicht über Service Level Agreements
description: In einer SLA stimmt der Debitor einer Mindestantwortzeit zu, basierend auf der Zeit zwischen der Aufzeichnung des Problems durch das Serviceunternehmen bis zum Beheben des Problems.
author: ShylaThompson
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServicelevelagreement
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 30b06e537b010b6b32799f76964cb85af892bc3f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216136"
---
# <a name="service-level-agreements-overview"></a><span data-ttu-id="58630-103">Übersicht über Service Level Agreements</span><span class="sxs-lookup"><span data-stu-id="58630-103">Service level agreements overview</span></span>       

[!include [banner](../includes/banner.md)]


<span data-ttu-id="58630-104">Eine Vereinbarung zum Servicelevel (Service Level Agreement, SLA) ist eine Vereinbarung zwischen einem Serviceunternehmen und einem Debitor.</span><span class="sxs-lookup"><span data-stu-id="58630-104">A service level agreement (SLA) is an agreement between a service company and a service customer.</span></span> <span data-ttu-id="58630-105">In einer SLA stimmt der Debitor einer Mindestantwortzeit zu, basierend auf der Zeit zwischen der Aufzeichnung des Problems durch das Serviceunternehmen bis zum Beheben des Problems.</span><span class="sxs-lookup"><span data-stu-id="58630-105">In a SLA, the customer agrees to a minimum response time based on when the service company records the issue and when the issue is resolved.</span></span>

<span data-ttu-id="58630-106">Eine SLA setzt einen Standard-Servicelevel durch, der Debitoren angeboten wird, und zeigt außerdem einem Serviceunternehmen an, wann ein Servicevorgang ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="58630-106">A SLA enforces a standard level of service that is offered to customers, and also makes it transparent to a service company when a service job should be completed.</span></span>

<span data-ttu-id="58630-107">Es kann eine beliebige Zahl von SLAs erstellt werden, um Debitoren verschiedene Servicelevels zu bieten.</span><span class="sxs-lookup"><span data-stu-id="58630-107">Any number of SLAs can be created to offer service customers different levels of service.</span></span>

## <a name="create-a-service-level-agreement"></a><span data-ttu-id="58630-108">Erstellen einer Vereinbarung zum Servicelevel</span><span class="sxs-lookup"><span data-stu-id="58630-108">Create a service level agreement</span></span>

1.  <span data-ttu-id="58630-109">Klicken Sie auf **Serviceverwaltung** \> **Einstellungen** \> **Servicevereinbarungen** \> **Vereinbarungen zum Servicelevel**.</span><span class="sxs-lookup"><span data-stu-id="58630-109">Click **Service management** \> **Setup** \> **Service agreements** \> **Service level agreements**.</span></span>

2.  <span data-ttu-id="58630-110">Geben Sie einen Namen für eine Vereinbarung zum Servicelevel im Feld **Vereinbarung zum Servicelevel** ein.</span><span class="sxs-lookup"><span data-stu-id="58630-110">Type a name for the service level agreement in the **Service level agreement** field.</span></span>

3.  <span data-ttu-id="58630-111">Geben Sie die Zeit ein, die Sie für die Ausführung von Serviceeinsätzen einräumen möchten, die der Vereinbarung zum Servicelevel zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="58630-111">Type the time that you want to allow for completion of service calls that are attached to the service level agreement.</span></span> <span data-ttu-id="58630-112">Wählen Sie dann einen Kalender aus, wenn die Vereinbarung zum Servicelevel auf einem bestimmten Kalender beruhen soll.</span><span class="sxs-lookup"><span data-stu-id="58630-112">Then select a calendar if you want to base the service level agreement on a specific calendar.</span></span>

## <a name="apply-a-service-level-agreement"></a><span data-ttu-id="58630-113">Anwenden einer Vereinbarung zum Servicelevel</span><span class="sxs-lookup"><span data-stu-id="58630-113">Apply a service level agreement</span></span>

<span data-ttu-id="58630-114">Die SLA wird direkt auf eine Servicevereinbarung angewendet.</span><span class="sxs-lookup"><span data-stu-id="58630-114">The SLA is applied directly to a service agreement.</span></span>

<span data-ttu-id="58630-115">Serviceaufträge, die Sie manuell erstellen und einer Servicevereinbarung zuordnen, die eine SLA hat, werden anhand dieser SLA gemessen.</span><span class="sxs-lookup"><span data-stu-id="58630-115">Service orders that you create manually and attach to a service agreement that has an SLA are measured against that SLA.</span></span>

<span data-ttu-id="58630-116">Automatisch erstellte Serviceaufträge werden keiner Vereinbarung zum Servicelevel zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="58630-116">Service orders that you create automatically are not attached to an SLA.</span></span>

## <a name="apply-the-service-level-agreement-to-the-service-agreement"></a><span data-ttu-id="58630-117">Anwenden der Vereinbarung zum Servicelevel auf die Servicevereinbarung</span><span class="sxs-lookup"><span data-stu-id="58630-117">Apply the service level agreement to the service agreement</span></span>

1.  <span data-ttu-id="58630-118">Klicken Sie auf den Bereichsseitenknoten: **Serviceverwaltung** \> **Gemeinsam** \> **Servicevereinbarungen** \> **Servicevereinbarungen**.</span><span class="sxs-lookup"><span data-stu-id="58630-118">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span> <span data-ttu-id="58630-119">Wählen Sie die Servicevereinbarung aus, auf die Sie die SLA anwenden möchten, und klicken Sie anschließend im **Aktivitätsbereich** auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="58630-119">Select the service agreement that you want to apply the SLA to, and then click **Edit** on the **Action Pane**.</span></span>

2.  <span data-ttu-id="58630-120">Wählen Sie im **Vereinbarung zum Servicelevel** Feld die Vereinbarung zum Servicelevel, die Sie zuordnen möchten.</span><span class="sxs-lookup"><span data-stu-id="58630-120">In the **Service level agreement** field, select the SLA that you want to assign.</span></span>

## <a name="apply-the-service-level-agreement-to-the-service-agreement-group"></a><span data-ttu-id="58630-121">Anwenden der Vereinbarung zum Servicelevel auf die Servicevereinbarungsgruppe</span><span class="sxs-lookup"><span data-stu-id="58630-121">Apply the service level agreement to the service agreement group</span></span>

1.  <span data-ttu-id="58630-122">Klicken Sie auf **Serviceverwaltung** \> **Einstellungen** \> **Servicevereinbarungen** \> **Serviceverinbarungsgruppen**.</span><span class="sxs-lookup"><span data-stu-id="58630-122">Click **Service management** \> **Setup** \> **Service agreements** \> **Service agreement groups**.</span></span>

2.  <span data-ttu-id="58630-123">Wählen Sie im **Vereinbarung zum Servicelevel** Feld die Vereinbarung zum Servicelevel, die Sie zuordnen möchten.</span><span class="sxs-lookup"><span data-stu-id="58630-123">In the **Service level agreement** field, select the SLA that you want to assign.</span></span>

## <a name="track-time-on-a-service-order-against-an-sla"></a><span data-ttu-id="58630-124">Zeiterfassung für einen Serviceauftrag anhand der Vereinbarung zum Servicelevel</span><span class="sxs-lookup"><span data-stu-id="58630-124">Track time on a service order against an SLA</span></span>

<span data-ttu-id="58630-125">Wenn Sie einen neuen Serviceauftrag für eine Servicevereinbarung erstellen, der eine SLA zugewiesen ist, wird das Zeitintervall für die Lieferung des Services gestartet, und das System beginnt mit der Erfassung der Lieferzeit.</span><span class="sxs-lookup"><span data-stu-id="58630-125">When you create a new service order for a service agreement that an SLA is assigned to, the time interval for the delivery of the service is initiated, and the system starts to track the delivery time.</span></span> <span data-ttu-id="58630-126">Darüber hinaus können Sie die folgenden Optionen festlegen:</span><span class="sxs-lookup"><span data-stu-id="58630-126">Additionally, you can set the following options:</span></span>

  - <span data-ttu-id="58630-127">Sie können die Zeitaufzeichnung für den Serviceauftrag starten und anhalten, um die Gesamtzeit für Serviceaufträge zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="58630-127">You can start and stop time recording on the service order to register the total amount of time that is spent on service orders.</span></span>

  - <span data-ttu-id="58630-128">Sie können die Einhaltung des in der Vereinbarung zum Servicelevel festgelegten Zeitrahmens überwachen.</span><span class="sxs-lookup"><span data-stu-id="58630-128">You can monitor compliance with the time interval that is set in the service level agreement.</span></span>

  - <span data-ttu-id="58630-129">Sie können Ursachencodes definieren, die festgelegt sein müssen, wenn der Zeitrahmen der Vereinbarung zum Servicelevel überschritten wird.</span><span class="sxs-lookup"><span data-stu-id="58630-129">You can define reason codes that must be set if the time interval of the service level agreement is exceeded.</span></span>

## <a name="see-also"></a><span data-ttu-id="58630-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="58630-130">See also</span></span>

[<span data-ttu-id="58630-131">Anzeigen der Konformität mit Vereinbarungen zum Servicelevel</span><span class="sxs-lookup"><span data-stu-id="58630-131">View compliance with service level agreements</span></span>](view-compliance-with-service-level-agreements.md)

  


