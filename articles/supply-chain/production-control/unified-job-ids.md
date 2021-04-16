---
title: Vereinheitlichte Nummernkreise für Einzelvorgangskennungen
description: Diese Funktion bietet einen einzelnen, einheitliche Nummernkreis, die Auftrags-IDs für die Module Produktionssteuerung, Fertigungssteuerung sowie Zeit und Anwesenheit generieren.
author: johanhoffmann
ms.date: 03/25/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 00212803c46d898a39eafbc5c62016eb829535e2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824941"
---
# <a name="unified-number-sequence-for-job-ids"></a><span data-ttu-id="8069f-103">Vereinheitlichte Nummernkreise für Einzelvorgangskennungen</span><span class="sxs-lookup"><span data-stu-id="8069f-103">Unified number sequence for job IDs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8069f-104">Diese Funktion bietet einen einzelnen, einheitliche Nummernkreis, die Auftrags-IDs für die Module Produktionssteuerung, Fertigungssteuerung sowie Zeit und Anwesenheit generieren.</span><span class="sxs-lookup"><span data-stu-id="8069f-104">This feature provides a single, unified number sequence that generates job IDs for the Production control, Manufacturing execution, and Time and attendance modules.</span></span> <span data-ttu-id="8069f-105">Bisher konnten Sie für jedes dieser Module einen anderen Nummernkreis auswählen, was zu widersprüchlichen Auftrags-IDs führen kann, wenn zwei oder mehr dieser Kreise ein identisches Format verwenden.</span><span class="sxs-lookup"><span data-stu-id="8069f-105">Previously, you were able to choose a different number sequence for each of these modules, which could result in conflicting job IDs if two or more of these sequences used an identical format.</span></span> <span data-ttu-id="8069f-106">Ein solcher Konflikt kann zu Datenkorruption führen.</span><span class="sxs-lookup"><span data-stu-id="8069f-106">Such a conflict can cause data corruption.</span></span>

## <a name="turn-on-this-feature-for-your-system"></a><span data-ttu-id="8069f-107">Schalten Sie diese Funktion für Ihr System ein</span><span class="sxs-lookup"><span data-stu-id="8069f-107">Turn on this feature for your system</span></span>

<span data-ttu-id="8069f-108">Wenn Ihr System nicht bereits die in diesem Thema beschriebene Funktion enthält, gehen Sie zu [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) und schalten Sie die Funktion *Einheitliche Nummernkreise für Auftrags-IDs* ein.</span><span class="sxs-lookup"><span data-stu-id="8069f-108">If your system doesn't already include the feature described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) and turn on the *Unified number sequence for job IDs* feature.</span></span>

## <a name="set-up-the-unified-number-sequence-for-job-ids"></a><span data-ttu-id="8069f-109">Einheitliche Nummernkreise für Auftrags-IDs einrichten</span><span class="sxs-lookup"><span data-stu-id="8069f-109">Set up the unified number sequence for job IDs</span></span>

<span data-ttu-id="8069f-110">Nach dem Aktivieren dieser Funktion sind die vorhandenen Einstellungen für die **Auftragskennung** und Nummernkreise auf den Parameterseiten für die Module Produktionssteuerung, Fertigungssteuer sowie Zeit und Anwesenheit veraltet und ein neues Feld **Einheitliche Auftrags-ID** wird hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="8069f-110">After enabling this feature, the existing **Job identification** number-sequence settings located on the parameters pages for the Production control, Manufacturing execution, and Time and attendance modules will be deprecated and a new **Unified job ID** field will be added.</span></span> <span data-ttu-id="8069f-111">Der Wert **Einheitliche Auftrags-ID** wird von allen drei Modulen geteilt, wodurch sichergestellt wird, dass alle Module auf denselben Nummernkreis verweisen.</span><span class="sxs-lookup"><span data-stu-id="8069f-111">The **Unified job ID** value is shared by all three modules, thus ensuring that all modules reference the same number sequence.</span></span> <span data-ttu-id="8069f-112">Auftrags-IDs sind daher in allen drei Modulen eindeutig und es kommt nie zu Konflikten.</span><span class="sxs-lookup"><span data-stu-id="8069f-112">Job IDs will therefore be unique across all three modules and a conflict will never occur.</span></span>

<span data-ttu-id="8069f-113">Um einheitliche Nummernkreise für Auftrags-IDs einzurichten, gehen Sie wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="8069f-113">To set up the unified number sequence for job IDs:</span></span>

1. <span data-ttu-id="8069f-114">Aktivieren Sie die Funktion wie im vorherigen Abschnitt beschrieben.</span><span class="sxs-lookup"><span data-stu-id="8069f-114">Turn on the feature as described in the previous section.</span></span>
1. <span data-ttu-id="8069f-115">Identifizieren Sie entweder den Nummernkreis, den Sie für Ihre einheitlichen Auftrags-IDs verwenden möchten, oder erstellen Sie einen neuen.</span><span class="sxs-lookup"><span data-stu-id="8069f-115">Either identify the number sequence you want to use for your unified job IDs, or create a new one.</span></span> <span data-ttu-id="8069f-116">Weitere Informationen finden Sie unter [Übersicht über Nummernkreise](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md).</span><span class="sxs-lookup"><span data-stu-id="8069f-116">For more information, see [Number sequences overview](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md).</span></span>
1. <span data-ttu-id="8069f-117">Gehen Sie zur Seite **Produktionssteuerungsparameter**, **Fertigungssteuerungsparameter** oder **Zeit- und Anwesenheitsparameter**.</span><span class="sxs-lookup"><span data-stu-id="8069f-117">Go to the **Production control parameters**, **Manufacturing execution parameters**, or **Time and attendance parameters** page.</span></span> <span data-ttu-id="8069f-118">Es spielt keine Rolle, wofür Sie sich entscheiden, denn wenn Sie diese Einstellung auf einer dieser Seiten vornehmen, werden alle anderen Seiten automatisch aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="8069f-118">It doesn't matter which one you choose because when you make this setting on any of those pages, all of the other pages will update automatically.</span></span>
1. <span data-ttu-id="8069f-119">Öffnen Sie die Registerkarte **Nummernkreise** auf der Seite mit den ausgewählten Parametern.</span><span class="sxs-lookup"><span data-stu-id="8069f-119">Open the **Number sequences** tab on your selected parameters page.</span></span>
1. <span data-ttu-id="8069f-120">Weisen Sie den **Nummernkreiscode**, den Sie zuvor für die Zeile **Einheitliche Auftrags-IDs** des Rasters festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="8069f-120">Assign the **Number sequence code** that you identified previously to the **Unified job IDs** row of the grid.</span></span>
