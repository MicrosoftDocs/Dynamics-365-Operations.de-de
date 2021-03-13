---
title: Wartezeiträume konfigurieren
description: In Microsoft Dynamics 365 Human Resources legen Wartezeiten einen Meilenstein zur Verwendung für Vergütungspläne fest.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 07ceed65a0346912d4be012a5cec502b0f0a6149
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112592"
---
# <a name="configure-waiting-periods"></a><span data-ttu-id="a2b0c-103">Wartezeiträume konfigurieren</span><span class="sxs-lookup"><span data-stu-id="a2b0c-103">Configure waiting periods</span></span>

<span data-ttu-id="a2b0c-104">In Microsoft Dynamics 365 Human Resources legen Wartezeiten einen Meilenstein zur Verwendung für Vergütungspläne fest.</span><span class="sxs-lookup"><span data-stu-id="a2b0c-104">In Microsoft Dynamics 365 Human Resources, waiting days establish a milestone to use for benefit plans.</span></span> <span data-ttu-id="a2b0c-105">Mögliche Beispiele: drei Monate ab dem Einstellungsdatum, der erste eines jeden Monats oder sechs Monate.</span><span class="sxs-lookup"><span data-stu-id="a2b0c-105">For example, three months from hire date, the first of each month, or six months.</span></span>   

1. <span data-ttu-id="a2b0c-106">Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Einstellungen** die Option **Wartezeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="a2b0c-106">In the **Benefits management** workspace, under **Setup**, select **Waiting periods**.</span></span>

2. <span data-ttu-id="a2b0c-107">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="a2b0c-107">Select **New**.</span></span>

3. <span data-ttu-id="a2b0c-108">Geben Sie Werte für die folgenden Felder an:</span><span class="sxs-lookup"><span data-stu-id="a2b0c-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="a2b0c-109">Feld</span><span class="sxs-lookup"><span data-stu-id="a2b0c-109">Field</span></span> | <span data-ttu-id="a2b0c-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a2b0c-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="a2b0c-111">**Wartecode**</span><span class="sxs-lookup"><span data-stu-id="a2b0c-111">**Waiting code**</span></span> | <span data-ttu-id="a2b0c-112">Ein eindeutiger Bezeichner für die Wartezeit.</span><span class="sxs-lookup"><span data-stu-id="a2b0c-112">A unique identifier for the waiting period.</span></span> |
   | <span data-ttu-id="a2b0c-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a2b0c-113">**Description**</span></span> | <span data-ttu-id="a2b0c-114">Eine kurze Beschreibung der Wartezeit.</span><span class="sxs-lookup"><span data-stu-id="a2b0c-114">A description of the waiting period.</span></span> |
   | <span data-ttu-id="a2b0c-115">**Wartemethode**</span><span class="sxs-lookup"><span data-stu-id="a2b0c-115">**Waiting method**</span></span> | <span data-ttu-id="a2b0c-116">Wählen Sie aus der Dropdownliste der Werte die entsprechende Wartemethode aus.</span><span class="sxs-lookup"><span data-stu-id="a2b0c-116">Select the appropriate waiting method from the drop-down list of values.</span></span> <span data-ttu-id="a2b0c-117">Die Optionen sind „Netto“, „Aktueller Monat“, „Aktuelles Quartal“, „Aktuelles Jahr“ und „Aktuelle Woche“</span><span class="sxs-lookup"><span data-stu-id="a2b0c-117">Options are Net, Current month, Current quarter, Current year, and Current week.</span></span> |
   | <span data-ttu-id="a2b0c-118">**Monate**</span><span class="sxs-lookup"><span data-stu-id="a2b0c-118">**Months**</span></span> | <span data-ttu-id="a2b0c-119">Geben Sie hier die Anzahl der Monate ein, die zum Berechnen des Wartedatums zur Wartemethode addiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a2b0c-119">Enter the number of months to add to the waiting method to calculate the waiting date.</span></span> |
   | <span data-ttu-id="a2b0c-120">**Tage**</span><span class="sxs-lookup"><span data-stu-id="a2b0c-120">**Days**</span></span> | <span data-ttu-id="a2b0c-121">Geben Sie hier die Anzahl der Tage ein, die zum Berechnen des Wartedatums zur Wartemethode addiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a2b0c-121">Enter the number of days to add to the waiting method to calculate the waiting date.</span></span> |
   | <span data-ttu-id="a2b0c-122">**Wartetag**</span><span class="sxs-lookup"><span data-stu-id="a2b0c-122">**Waiting day**</span></span> | <span data-ttu-id="a2b0c-123">Wählen Sie einen Wartetag zum Berechnen des Wartedatums aus.</span><span class="sxs-lookup"><span data-stu-id="a2b0c-123">Select the waiting day to use to calculate the waiting date.</span></span> |

4. <span data-ttu-id="a2b0c-124">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="a2b0c-124">Select **Save**.</span></span>
