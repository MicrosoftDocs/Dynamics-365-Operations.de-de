---
title: Vorteilsverwaltungsparameter festlegen
description: Konfigurieren Sie Parameter für die Vorteilsverwaltung in Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
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
ms.openlocfilehash: 3e001c08751ea9c8bcab0e11a04b6cf639e51d1d
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429985"
---
# <a name="set-benefits-management-parameters"></a><span data-ttu-id="68769-103">Vorteilsverwaltungsparameter festlegen</span><span class="sxs-lookup"><span data-stu-id="68769-103">Set Benefits management parameters</span></span>

<span data-ttu-id="68769-104">Bevor Sie Urlaubspläne in Microsoft Dynamics 365 Human Resources einrichten können, müssen Sie die Vorteilsverwaltungsparameter konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="68769-104">Before you can set up leave plans in Microsoft Dynamics 365 Human Resources, you must configure Benefits management parameters.</span></span> <span data-ttu-id="68769-105">Diese Parameter legen Standardwerte, Ursachencodes und andere Optionen fest.</span><span class="sxs-lookup"><span data-stu-id="68769-105">These parameters set default values, reason codes, and other options.</span></span>

## <a name="configure-general-parameters"></a><span data-ttu-id="68769-106">Allgemeine Parameter konfigurieren</span><span class="sxs-lookup"><span data-stu-id="68769-106">Configure general parameters</span></span>

1. <span data-ttu-id="68769-107">Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Einstellungen** die Option **Parameter**.</span><span class="sxs-lookup"><span data-stu-id="68769-107">In the **Benefits management** workspace, under **Setup**, select **Parameters**.</span></span>

2. <span data-ttu-id="68769-108">Definieren Sie auf der Registerkarte **Allgemeines** die Werte für die folgenden Felder:</span><span class="sxs-lookup"><span data-stu-id="68769-108">In the **General** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="68769-109">Feld</span><span class="sxs-lookup"><span data-stu-id="68769-109">Field</span></span> | <span data-ttu-id="68769-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="68769-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="68769-111">**Land/Region**</span><span class="sxs-lookup"><span data-stu-id="68769-111">**Country/region**</span></span> | <span data-ttu-id="68769-112">Das Feld **Land/Region** bestimmt die Anzeigereihenfolge der Postleitzahlen/Staaten.</span><span class="sxs-lookup"><span data-stu-id="68769-112">The **Country/region** field determines the display order of ZIP codes/states.</span></span> <span data-ttu-id="68769-113">Das ausgewählte Land wird zuerst in der Dropdown-Liste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="68769-113">The selected country displays first in the dropdown list.</span></span> |
   | <span data-ttu-id="68769-114">**Registrierungsursachencode**</span><span class="sxs-lookup"><span data-stu-id="68769-114">**Enrollment reason code**</span></span> | <span data-ttu-id="68769-115">Wählen Sie einen Standardursachencode aus, der verwendet werden soll, wenn Mitarbeiterpläne während der offenen Registrierungsverarbeitung erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="68769-115">Select a default reason code to use when employee plans are created during open enrollment processing.</span></span> |
   | <span data-ttu-id="68769-116">**Stornierungsursachencode**</span><span class="sxs-lookup"><span data-stu-id="68769-116">**Cancellation reason code**</span></span> | <span data-ttu-id="68769-117">Der Ursachencode, der verwendet wird, wenn ein Mitarbeitervorteilsplan storniert wird.</span><span class="sxs-lookup"><span data-stu-id="68769-117">The reason code to use when an employee benefit plan is canceled.</span></span> <span data-ttu-id="68769-118">Er wird beim Stornierungsvorgang in einem Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="68769-118">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="68769-119">Benutzer können ihn im Feld **Stornierungsursachencode** bei Bedarf ändern.</span><span class="sxs-lookup"><span data-stu-id="68769-119">Users can change it the **Cancellation reason code** if necessary.</span></span> |
   | <span data-ttu-id="68769-120">**Ursachencode erneut öffnen**</span><span class="sxs-lookup"><span data-stu-id="68769-120">**Reopen reason code**</span></span> | <span data-ttu-id="68769-121">Der Ursachencode, der verwendet wird, wenn ein Mitarbeitervorteilsplan erneut geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="68769-121">The reason code to use when an employee benefit plan is reopened.</span></span> <span data-ttu-id="68769-122">Er wird beim Stornierungsvorgang in einem Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="68769-122">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="68769-123">Benutzer können ihn im Feld **Ursachencode erneut öffnen** bei Bedarf ändern.</span><span class="sxs-lookup"><span data-stu-id="68769-123">Users can change the **Reopen reason code** if necessary.</span></span> | 
   | <span data-ttu-id="68769-124">**Ursachencode für Lebensereignis**</span><span class="sxs-lookup"><span data-stu-id="68769-124">**Life event reason code**</span></span> | <span data-ttu-id="68769-125">Der zu verwendende Ursachencode, wenn ein Lebensereignis eintritt.</span><span class="sxs-lookup"><span data-stu-id="68769-125">The reason code to use when a life event occurs.</span></span> |
   | <span data-ttu-id="68769-126">**Ursachencode für Satzänderung**</span><span class="sxs-lookup"><span data-stu-id="68769-126">**Rate change reason code**</span></span> | <span data-ttu-id="68769-127">Der Ursachencode, der beim Stornieren und erneuten Öffnen eines Personalvorteilsplans verwendet werden soll, wenn die Satzänderung aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="68769-127">The reason code to use when canceling and reopening an employee benefit plan during the rate change update process.</span></span> <span data-ttu-id="68769-128">Er zeigt an, welche Datensätze durch die Aktualisierung der Satzänderung geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="68769-128">It indicates which records were changed by the rate change update process.</span></span> |
   | <span data-ttu-id="68769-129">**Neueinstellung möglich**</span><span class="sxs-lookup"><span data-stu-id="68769-129">**New hire eligible**</span></span> | <span data-ttu-id="68769-130">Gibt an, ob Neueinstellungen zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="68769-130">Specifies whether new hires are eligible.</span></span> |
   | <span data-ttu-id="68769-131">**Registrierungsperiode für Neueinstellungen**</span><span class="sxs-lookup"><span data-stu-id="68769-131">**New hire enrollment period**</span></span> | <span data-ttu-id="68769-132">Die Periode, für die die Registrierung einer Neueinstellung zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="68769-132">The period of time the new hire enrollment is allowed.</span></span></br></br><span data-ttu-id="68769-133">**Hinweis**: Diese Einstellung überschreibt jede Registrierungsperiode für Neueinstellungen, die Sie in der Planberechtigungsregel festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="68769-133">**Note**: This setting overrides any new hire enrollment period you set on the plan eligibility rule.</span></span> | 
   | <span data-ttu-id="68769-134">**Lebensereignisse aktiviert**</span><span class="sxs-lookup"><span data-stu-id="68769-134">**Life events enabled**</span></span> | <span data-ttu-id="68769-135">Aktiviert Lebensereignisse.</span><span class="sxs-lookup"><span data-stu-id="68769-135">Enables life events.</span></span> |
   | <span data-ttu-id="68769-136">**Legacy-Vergütungsformulare ausblenden**</span><span class="sxs-lookup"><span data-stu-id="68769-136">**Hide legacy benefit forms**</span></span> | <span data-ttu-id="68769-137">Ermöglicht das Ausblenden von Legacy-Vergütungsformularen.</span><span class="sxs-lookup"><span data-stu-id="68769-137">Allows you to hide legacy benefit forms.</span></span> |

3. <span data-ttu-id="68769-138">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="68769-138">Select **Save**.</span></span>

## <a name="configure-employee-self-service-parameters"></a><span data-ttu-id="68769-139">Mitarbeiter-Self-Service-Parameter konfigurieren</span><span class="sxs-lookup"><span data-stu-id="68769-139">Configure Employee self service parameters</span></span>

1. <span data-ttu-id="68769-140">Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Einstellungen** die Option **Parameter**.</span><span class="sxs-lookup"><span data-stu-id="68769-140">In the **Benefits management** workspace, under **Setup**, select **Parameters**.</span></span>

2. <span data-ttu-id="68769-141">Definieren Sie auf der Registerkarte **Mitarbeiter-Self-Service** die Werte für die folgenden Felder:</span><span class="sxs-lookup"><span data-stu-id="68769-141">In the **Employee self service** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="68769-142">Feld</span><span class="sxs-lookup"><span data-stu-id="68769-142">Field</span></span> | <span data-ttu-id="68769-143">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="68769-143">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="68769-144">**Vorteilsüberprüfung**</span><span class="sxs-lookup"><span data-stu-id="68769-144">**Benefit verification**</span></span> | <span data-ttu-id="68769-145">Der Überprüfungstext, der beim Auschecken der Self-Service-Vorteile verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="68769-145">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="68769-146">**Beauftragten automatisch auswählen**</span><span class="sxs-lookup"><span data-stu-id="68769-146">**Auto select designees**</span></span> | <span data-ttu-id="68769-147">Gibt an, ob Unterhaltsberechtigte und Begünstigte basierend auf ihrer Berechtigung für Planoptionen automatisch ausgewählt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="68769-147">Specifies whether to automatically select dependents and beneficiaries based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="68769-148">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="68769-148">Select **Save**.</span></span>
