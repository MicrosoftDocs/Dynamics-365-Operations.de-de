---
title: Arbeitskräfte, die für die Genehmigung von Qualitätsmängeln verantwortlich sind
description: Dieses Thema beschreibt, wie Sie Arbeitskräfte konfigurieren, die für die Genehmigung von Qualitätsmängeln zuständig sind.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5979cb33146a00c3ea49ada9577140b24c07928f
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956672"
---
# <a name="workers-responsible-for-approving-nonconformances"></a><span data-ttu-id="1aea3-103">Arbeitskräfte, die für die Genehmigung von Qualitätsmängeln verantwortlich sind</span><span class="sxs-lookup"><span data-stu-id="1aea3-103">Workers responsible for approving nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1aea3-104">Dieses Thema beschreibt, wie Sie Arbeitskräfte konfigurieren, die für die Genehmigung von Qualitätsmängeln zuständig sind.</span><span class="sxs-lookup"><span data-stu-id="1aea3-104">This topic describes how to configure workers that are responsible for approving nonconformances.</span></span>

<span data-ttu-id="1aea3-105">Qualitätsmängel müssen genehmigt werden, bevor Benutzer mit der Eingabe von Details wie Korrekturen oder Vorgängen beginnen können.</span><span class="sxs-lookup"><span data-stu-id="1aea3-105">Nonconformances must be approved before users can start to enter details such as corrections or operations.</span></span> <span data-ttu-id="1aea3-106">Bevor Benutzer Qualitätsmängel genehmigen oder ablehnen können, muss ihre Benutzer-ID (Benutzer-Datensatz) mit einem worker-Datensatz verknüpft sein.</span><span class="sxs-lookup"><span data-stu-id="1aea3-106">Before users can approve or reject nonconformances, their user ID (user record) must be linked to a worker record.</span></span> <span data-ttu-id="1aea3-107">Sie können optional Arbeitskräfte konfigurieren, die für die Qualität verantwortlich sind und dann zulassen, dass eine Arbeitskraft die Arbeit im Namen einer anderen Arbeitskraft genehmigt.</span><span class="sxs-lookup"><span data-stu-id="1aea3-107">You can optionally configure workers that are responsible for quality and then allow one worker to approve work on behalf of another worker.</span></span>

## <a name="enable-a-user-for-nonconformance-processing"></a><span data-ttu-id="1aea3-108">Aktivieren Sie einen Benutzer für die Verarbeitung von Qualitätsmängeln</span><span class="sxs-lookup"><span data-stu-id="1aea3-108">Enable a user for nonconformance processing</span></span>

<span data-ttu-id="1aea3-109">Bevor ein Benutzer Qualitätsmängel genehmigen oder ablehnen kann, müssen Sie seinen Datensatz mit einem worker-Datensatz verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="1aea3-109">Before a user can approve or reject nonconformances, you must link their user record to a worker record.</span></span> <span data-ttu-id="1aea3-110">Die Genehmigungsfelder können dann automatisch festgelegt werden, und der aktuelle Benutzer kann automatisch für den Stundenzettel ausgefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="1aea3-110">The approval fields can then be automatically set, and the current user can be automatically filled in for the timesheet.</span></span> <span data-ttu-id="1aea3-111">Bevor der Benutzer die Dokumentennotizen verwenden kann, müssen Sie die Dokumentenbearbeitung in seinen Benutzeroptionen aktivieren.</span><span class="sxs-lookup"><span data-stu-id="1aea3-111">Before the user can use the document notes, you must activate document handling in their user options.</span></span>

1. <span data-ttu-id="1aea3-112">Wechseln Sie zu **Systemverwaltung \> Benutzer \> Benutzer**.</span><span class="sxs-lookup"><span data-stu-id="1aea3-112">Go to **System administration \> Users \> Users**.</span></span>
1. <span data-ttu-id="1aea3-113">Suchen und öffnen Sie den Benutzer, der in der Lage sein soll, Qualitätsmängel zu genehmigen oder abzulehnen.</span><span class="sxs-lookup"><span data-stu-id="1aea3-113">Find and open the user who should be able to approve or reject nonconformances.</span></span>
1. <span data-ttu-id="1aea3-114">Legen Sie das Feld **Person** auf den Namen der Arbeitskraft fest, die mit dem aktuellen Datensatz des Benutzers verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="1aea3-114">Set the **Person** field to the name of the worker that is related to the current user record.</span></span>
1. <span data-ttu-id="1aea3-115">Wählen Sie im Aktivitätsbereich **Benutzeroptionen**.</span><span class="sxs-lookup"><span data-stu-id="1aea3-115">On the Action Pane, select **User options**.</span></span>
1. <span data-ttu-id="1aea3-116">Legen Sie auf der Seite **Optionen** für den aktuellen Datensatz auf der Registerkarte **Einstellungen** die Option **Dokumentenbehandlung aktivieren** auf *Ja* fest.</span><span class="sxs-lookup"><span data-stu-id="1aea3-116">On the **Options** page for the current user record, on the **Preferences** tab, set the **Enable document handling** option to *Yes*.</span></span>
1. <span data-ttu-id="1aea3-117">Schließen Sie die Seiten.</span><span class="sxs-lookup"><span data-stu-id="1aea3-117">Close the pages.</span></span>

## <a name="define-workers-that-are-responsible-for-quality"></a><span data-ttu-id="1aea3-118">Definieren Sie Arbeitskräfte, die für die Qualität verantwortlich sind</span><span class="sxs-lookup"><span data-stu-id="1aea3-118">Define workers that are responsible for quality</span></span>

1. <span data-ttu-id="1aea3-119">Übergehen zu **Bestandsmanagement \> Einrichten \> Qualitätskontrolle \> Qualitätsverantwortliche Arbeitskräfte**.</span><span class="sxs-lookup"><span data-stu-id="1aea3-119">Go to **Inventory management \> Setup \> Quality control \> Workers responsible for quality**.</span></span>
2. <span data-ttu-id="1aea3-120">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="1aea3-120">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="1aea3-121">Wählen Sie im Feld **Arbeiter** die Arbeitskraft aus, die Qualitätsdaten eingibt.</span><span class="sxs-lookup"><span data-stu-id="1aea3-121">In the **Worker** field, select the worker that enters quality data.</span></span>
4. <span data-ttu-id="1aea3-122">Wählen Sie im Feld **Verantwortliche Arbeitskraft** die Arbeitskraft aus, für die die ausgewählte Arbeitskraft die Arbeit eingibt.</span><span class="sxs-lookup"><span data-stu-id="1aea3-122">In the **Worker responsible** field, select the worker that the selected worker enters work on behalf of.</span></span> <span data-ttu-id="1aea3-123">Wenn Qualitätsmängel erstellt und aktualisiert werden, wird diese Arbeitskraft standardmäßig in die Felder **Arbeiter** eingetragen.</span><span class="sxs-lookup"><span data-stu-id="1aea3-123">When nonconformances are created and updated, this worker will be entered by default in **Worker** fields.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1aea3-124">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1aea3-124">Additional resources</span></span>

- [<span data-ttu-id="1aea3-125">Qualitätsmanagement – Übersicht</span><span class="sxs-lookup"><span data-stu-id="1aea3-125">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="1aea3-126">Qualitäts- und Qualitätsmangel-Management aktivieren</span><span class="sxs-lookup"><span data-stu-id="1aea3-126">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="1aea3-127">Belastungen für Qualität</span><span class="sxs-lookup"><span data-stu-id="1aea3-127">Quality charges</span></span>](quality-charges.md)
- [<span data-ttu-id="1aea3-128">Quarantänezonen für Qualitätsmängel</span><span class="sxs-lookup"><span data-stu-id="1aea3-128">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="1aea3-129">Diagnosetypen für Qualitätsmängel</span><span class="sxs-lookup"><span data-stu-id="1aea3-129">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="1aea3-130">Qualitätsbelastungen für Qualitätsmängel</span><span class="sxs-lookup"><span data-stu-id="1aea3-130">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="1aea3-131">Vorgänge für Qualitätsmängel</span><span class="sxs-lookup"><span data-stu-id="1aea3-131">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="1aea3-132">Qualitätsmanagement für Lagerortprozesse</span><span class="sxs-lookup"><span data-stu-id="1aea3-132">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
