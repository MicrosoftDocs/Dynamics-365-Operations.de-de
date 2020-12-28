---
title: Verwenden von Phasenursachencodes
description: Ursachencodes dienen zum Angeben der Ursache für die Stornierung einer Vereinbarung zum Servicelevel (Service Level Agreement, SLA) oder für die Überschreitung des durch eine Vereinbarung zum Servicelevel angegebenen Zeitlimits.
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 74594871e9eeed86ae2914d1e5a08c0af28ab643
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428857"
---
# <a name="use-stage-reason-codes"></a><span data-ttu-id="f9aec-103">Verwenden von Phasenursachencodes</span><span class="sxs-lookup"><span data-stu-id="f9aec-103">Use stage reason codes</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="f9aec-104">Ursachencodes dienen zum Angeben der Ursache für die Stornierung einer Vereinbarung zum Servicelevel (Service Level Agreement, SLA) oder für die Überschreitung des durch eine Vereinbarung zum Servicelevel angegebenen Zeitlimits.</span><span class="sxs-lookup"><span data-stu-id="f9aec-104">You use a reason code to indicate why a service level agreement (SLA) has been canceled, or why a service order has exceeded the time limit that is you define in the SLA.</span></span>

<span data-ttu-id="f9aec-105">Sie können auch angeben, dass ein Ursachencode erforderlich ist, wenn eine Vereinbarung zum Servicelevel storniert wird oder wenn das Zeitlimit die Zeit überschreitet, die in der Vereinbarung zum Servicelevel für den Serviceauftrag angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="f9aec-105">You can also specify that a reason code is required when an SLA is canceled, or when the time limit exceeds the time that is specified in the SLA for the service order.</span></span>

<span data-ttu-id="f9aec-106">Wenn Sie angegeben haben, dass ein Ursachencode erforderlich ist, müssen Sie einen Ursachencode in folgenden Situationen eingeben:</span><span class="sxs-lookup"><span data-stu-id="f9aec-106">If you have specified that a reason code is required, you must enter a reason code in the following situations:</span></span>

  - <span data-ttu-id="f9aec-107">Wenn ein Serviceauftrag in eine Phase eintritt, in der keine SLA-Zeitaufzeichnung für den Serviceauftrag mehr stattfindet.</span><span class="sxs-lookup"><span data-stu-id="f9aec-107">When a service order is moved to a stage that stops time recording against the SLA for the service order.</span></span>

  - <span data-ttu-id="f9aec-108">Der Serviceauftrag wird abgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="f9aec-108">When the service order is signed off.</span></span>

  - <span data-ttu-id="f9aec-109">Wenn die Zeitaufzeichnung manuell beendet wird.</span><span class="sxs-lookup"><span data-stu-id="f9aec-109">When time recording is manually stopped.</span></span>

## <a name="set-up-reason-codes"></a><span data-ttu-id="f9aec-110">Ursachencodes einrichten</span><span class="sxs-lookup"><span data-stu-id="f9aec-110">Set up reason codes</span></span>

1.  <span data-ttu-id="f9aec-111">Klicken auf **Serviceverwaltung** \> **Einrichtung** \> **Serviceaufträge** \> **Phasenursachencodes**.</span><span class="sxs-lookup"><span data-stu-id="f9aec-111">Click **Service management** \> **Setup** \> **Service orders** \> **Stage reason codes**.</span></span>

2.  <span data-ttu-id="f9aec-112">Klicken Sie im Formular **Phasenursachencodes** auf **Neu**, um einen neuen Phasenursachencode zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f9aec-112">In the **Stage reason codes** form, click **New** to create a new reason code.</span></span>

3.  <span data-ttu-id="f9aec-113">Geben Sie im Feld **Phasenursachencodes** einen eindeutigen Phasenursachencode ein.</span><span class="sxs-lookup"><span data-stu-id="f9aec-113">In the **Stage reason code** field, enter a unique stage reason code.</span></span>

4.  <span data-ttu-id="f9aec-114">Geben Sie im Feld **Beschreibung** eine Beschreibung für den Phasenursachencode ein.</span><span class="sxs-lookup"><span data-stu-id="f9aec-114">In the **Description** field, enter a description of the stage reason code.</span></span>

5.  <span data-ttu-id="f9aec-115">Schließen Sie das Formular, um Ihre Änderungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="f9aec-115">Close the form to save your changes.</span></span>

## <a name="require-reason-codes-when-a-service-level-agreement-is-canceled"></a><span data-ttu-id="f9aec-116">Erzwingen von Ursachencodes beim Stornieren einer Vereinbarung zum Servicelevel</span><span class="sxs-lookup"><span data-stu-id="f9aec-116">Require reason codes when a service level agreement is canceled</span></span>

1.  <span data-ttu-id="f9aec-117">Klicken Sie auf **Serviceverwaltung** \> **Einrichtung** \> **Serviceverwaltungsparameter**.</span><span class="sxs-lookup"><span data-stu-id="f9aec-117">Click **Service management** \> **Setup** \> **Service management parameters**.</span></span>

2.  <span data-ttu-id="f9aec-118">In der **Serviceverwaltungsparameter** Formular klicken Sie auf den Link **Allgemein**, und aktivieren Sie dann das Kontrollkästchen **Ursachencode bei Storno**.</span><span class="sxs-lookup"><span data-stu-id="f9aec-118">In the **Service management parameters** form, click the **General** link, and then select the **Reason code on canceling** check box.</span></span>

## <a name="require-reason-codes-when-the-a-service-order-exceeds-the-time-limit-that-is-set-by-the-service-level-agreement"></a><span data-ttu-id="f9aec-119">Verlangen Sie Ursachencodes bei Überschreitung des in der Vereinbarung zum Servicelevel angegebenen Zeitlimits</span><span class="sxs-lookup"><span data-stu-id="f9aec-119">Require reason codes when the a service order exceeds the time limit that is set by the service level agreement</span></span>

1.  <span data-ttu-id="f9aec-120">Klicken Sie auf **Serviceverwaltung** \> **Einrichtung** \> **Serviceverwaltungsparameter**.</span><span class="sxs-lookup"><span data-stu-id="f9aec-120">Click **Service management** \> **Setup** \> **Service management parameters**.</span></span>

2.  <span data-ttu-id="f9aec-121">In der **Serviceverwaltungsparameter** Formular klicken Sie auf den Link **Allgemein**, und aktivieren Sie dann das Kontrollkästchen **Ursachencode bei Zeitüberschreitung**.</span><span class="sxs-lookup"><span data-stu-id="f9aec-121">In the **Service management parameters** form, click the **General** link, and then select the **Reason code on exceeding time** check box.</span></span>

## <a name="see-also"></a><span data-ttu-id="f9aec-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f9aec-122">See also</span></span>

[<span data-ttu-id="f9aec-123">Starten und Beenden der Zeitaufzeichnung für einen Serviceauftrag</span><span class="sxs-lookup"><span data-stu-id="f9aec-123">Start and stop time recording on a service order</span></span>](start-and-stop-time-recording-on-a-service-order.md)

  


