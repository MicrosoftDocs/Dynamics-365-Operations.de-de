---
title: Ergebnisse der Automatisierung von Lieferantenrechnungen anzeigen (Vorschau)
description: In diesem Thema wird erläutert, wie Sie den Status von Lieferantenrechnungen anzeigen, die sich im automatisierten Submit-to-Workflow-Prozess befinden.
author: abruer
manager: AnnBe
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ec49a621e24b6373532497b499e8b9d45c9bed14
ms.sourcegitcommit: 9e7ceb5604472f3088f611aa0360bd6a716db32b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4022612"
---
# <a name="view-vendor-invoice-automation-results"></a><span data-ttu-id="4bdf2-103">Ergebnisse der Automatisierung von Kreditorenrechnungen anzeigen</span><span class="sxs-lookup"><span data-stu-id="4bdf2-103">View vendor invoice automation results</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4bdf2-104">In diesem Thema wird erläutert, wie Sie den Status von Lieferantenrechnungen anzeigen, die sich im automatisierten Submit-to-Workflow-Prozess befinden.</span><span class="sxs-lookup"><span data-stu-id="4bdf2-104">This topic explains how to view the status of vendor invoices that are in the automated submit-to-workflow process.</span></span> <span data-ttu-id="4bdf2-105">Details zum Automatisierungsverlauf werden für jede importierte Lieferantenrechnung gepflegt.</span><span class="sxs-lookup"><span data-stu-id="4bdf2-105">Details of the automation history are maintained for each imported vendor invoice.</span></span> <span data-ttu-id="4bdf2-106">Abhängig von den Geschäftsprozessen, die Sie automatisiert haben, zeigt die Seite **Ausstehende Lieferantenrechnungen** die Werte **Status der automatisierten Belegübereinstimmung** und **Automatische Übermittlung an den Workflow-Status**.</span><span class="sxs-lookup"><span data-stu-id="4bdf2-106">Depending on the business processes that you've automated, the **Pending vendor invoices** page shows **Automated receipt match status** and **Automated submit to workflow status** values.</span></span> <span data-ttu-id="4bdf2-107">Sie können die Details anzeigen und einen Plan erstellen, um sich auf die Rechnungen zu konzentrieren, bei denen ein automatisierter Schritt fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="4bdf2-107">You can view the details and make a plan to focus on the invoices that failed an automated step.</span></span> <span data-ttu-id="4bdf2-108">Nachdem Sie das Problem behoben haben, können Sie den automatisierten Prozess für die importierte Rechnung fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="4bdf2-108">Then, after you correct the issue, you can resume the automated process for the imported invoice.</span></span>

<span data-ttu-id="4bdf2-109">Bevor Sie eine übermittelte Rechnung bearbeiten können, müssen Sie die automatische Verarbeitung anhalten.</span><span class="sxs-lookup"><span data-stu-id="4bdf2-109">Before you can edit an invoice that has been submitted, you must pause the automated processing.</span></span> <span data-ttu-id="4bdf2-110">Wenn eine Rechnung im automatisierten Submit-to-Workflow-Prozess angehalten werden muss, setzen Sie das Feld **In die automatisierte Verarbeitung einbeziehen** auf der Seite **Lieferantenrechnungen** auf **Nein**.</span><span class="sxs-lookup"><span data-stu-id="4bdf2-110">If an invoice in the automated submit-to-workflow process must be paused, set the **Include in Automated processing** field to **No** on the **Vendor invoices** page.</span></span> <span data-ttu-id="4bdf2-111">Die Automatisierung wird erst dann ausgeführt, wenn **In die automatisierte Verarbeitung einbeziehen** auf **Ja** gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="4bdf2-111">Automation then won't run until **Include in Automated processing** is set to **Yes**.</span></span> <span data-ttu-id="4bdf2-112">Eine Rechnung kann von der weiteren Automatisierung angehalten werden, wenn sie sich noch nicht im Workflow-System befindet und nicht vom automatisierten Prozess verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4bdf2-112">An invoice can be paused from further automation if it isn't yet in the workflow system and isn't used by the automated process.</span></span>

<span data-ttu-id="4bdf2-113">Wenn eine importierte Rechnung dem Workflow-Prozess unterworfen ist, können Sie sie ihren **Automatisierungsstatus** -Wert auf der **Lieferantenrechnungen** -Seite anzeigen.</span><span class="sxs-lookup"><span data-stu-id="4bdf2-113">If an imported invoice is subject to the submit-to-workflow process, you can view its **Automation status** value on the **Vendor invoices** page.</span></span> <span data-ttu-id="4bdf2-114">Folgende Status werden verfolgt:</span><span class="sxs-lookup"><span data-stu-id="4bdf2-114">The following statuses are tracked:</span></span>

- <span data-ttu-id="4bdf2-115">**Inbegriffen** – Die automatisierten Prozesse, die auf der Seite **Kreditorenkontenparameter** definiert sind, laufen korrekt, sind aber noch nicht abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="4bdf2-115">**Included** – The automated processes that are defined on the **Accounts payable parameters** page are running correctly but haven't yet been completed.</span></span>
- <span data-ttu-id="4bdf2-116">**Pausiert** – Die automatisierten Prozesse, die auf der Seite **Kreditorenkontoparameter** definiert sind, wurden ausgeführt, aber mindestens ein Schritt in diesem Prozess ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="4bdf2-116">**Paused** – The automated processes that are defined on the **Accounts payable parameters** page have run, but at least one step in the process failed.</span></span> <span data-ttu-id="4bdf2-117">Der Status **Pausiert** wird auch angewendet, wenn das Feld **In die automatisierte Verarbeitung einbeziehen** auf **Nein** gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="4bdf2-117">The **Paused** status is also applied if the **Include in automated processing** field is set to **No**.</span></span> <span data-ttu-id="4bdf2-118">Sie können die Fehler anzeigen, indem Sie die Schaltfläche **Letzte Ergebnisse anzeigen** wählen.</span><span class="sxs-lookup"><span data-stu-id="4bdf2-118">You can view the failures by selecting **View most recent results**.</span></span>
- <span data-ttu-id="4bdf2-119">**Im Workflow** – Die importierte Rechnung wurde entweder automatisch oder manuell an das Workflow-System übermittelt.</span><span class="sxs-lookup"><span data-stu-id="4bdf2-119">**In workflow** – The imported invoice has been submitted to the workflow system, either by the automated submit-to-workflow process or manually.</span></span>
- <span data-ttu-id="4bdf2-120">**Workflow abgeschlossen** – Der Workflow-Prozess für die importierte Rechnung wurde abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="4bdf2-120">**Workflow complete** – The workflow process has been completed for the imported invoice.</span></span>
