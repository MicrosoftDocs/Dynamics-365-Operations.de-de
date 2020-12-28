---
title: Vorteilsmanagement- und Mitarbeiter-Self-Service-Parameter für alle Unternehmen festlegen
description: Konfigurieren Sie Vorteilsmanagement- und Mitarbeiter-Self-Service-Parameter für alle Unternehmen in Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 12/07/2020
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
ms.openlocfilehash: b50c4f71789c34f08ce810312f3c3198303b031e
ms.sourcegitcommit: fd097f6f76f0d8428038fa3655b3188bf093b517
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "4692696"
---
# <a name="set-benefits-management-and-employee-self-service-parameters-for-all-companies"></a><span data-ttu-id="29851-103">Vorteilsmanagement- und Mitarbeiter-Self-Service-Parameter für alle Unternehmen festlegen</span><span class="sxs-lookup"><span data-stu-id="29851-103">Set Benefits management and Employee self-service parameters for all companies</span></span>

<span data-ttu-id="29851-104">Bevor Sie Vorteilspläne in Microsoft Dynamics 365 Human Resources einrichten können, müssen Sie die Vorteilsverwaltungsparameter konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="29851-104">Before you can set up benefit plans in Microsoft Dynamics 365 Human Resources, you must configure Benefits management parameters.</span></span> <span data-ttu-id="29851-105">Diese Parameter legen Standardwerte, Ursachencodes und andere Optionen fest.</span><span class="sxs-lookup"><span data-stu-id="29851-105">These parameters set default values, reason codes, and other options.</span></span> 

## <a name="configure-general-parameters"></a><span data-ttu-id="29851-106">Allgemeine Parameter konfigurieren</span><span class="sxs-lookup"><span data-stu-id="29851-106">Configure general parameters</span></span>

1. <span data-ttu-id="29851-107">Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Setup** die Option **Gemeinsam genutzte Parameter der Personalverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="29851-107">In the **Benefits management** workspace, under **Setup**, select **Human Resources Shared Parameters**.</span></span>

2. <span data-ttu-id="29851-108">Definieren Sie auf der Registerkarte **Vergütungsverwaltung** die Werte für die folgenden Felder:</span><span class="sxs-lookup"><span data-stu-id="29851-108">In the **Benefits management** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="29851-109">Feld</span><span class="sxs-lookup"><span data-stu-id="29851-109">Field</span></span> | <span data-ttu-id="29851-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="29851-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="29851-111">**Land/Region**</span><span class="sxs-lookup"><span data-stu-id="29851-111">**Country/region**</span></span> | <span data-ttu-id="29851-112">Das Feld **Land/Region** bestimmt die Anzeigereihenfolge der Postleitzahlen/Staaten.</span><span class="sxs-lookup"><span data-stu-id="29851-112">The **Country/region** field determines the display order of ZIP codes/states.</span></span> <span data-ttu-id="29851-113">Das ausgewählte Land wird zuerst in der Dropdown-Liste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="29851-113">The selected country displays first in the dropdown list.</span></span> |
   | <span data-ttu-id="29851-114">**Registrierungsursachencode**</span><span class="sxs-lookup"><span data-stu-id="29851-114">**Enrollment reason code**</span></span> | <span data-ttu-id="29851-115">Wählen Sie einen Standardursachencode aus, der verwendet werden soll, wenn Mitarbeiterpläne während der offenen Registrierungsverarbeitung erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="29851-115">Select a default reason code to use when employee plans are created during open enrollment processing.</span></span> |
   | <span data-ttu-id="29851-116">**Stornierungsursachencode**</span><span class="sxs-lookup"><span data-stu-id="29851-116">**Cancellation reason code**</span></span> | <span data-ttu-id="29851-117">Der Ursachencode, der verwendet wird, wenn ein Mitarbeitervorteilsplan storniert wird.</span><span class="sxs-lookup"><span data-stu-id="29851-117">The reason code to use when an employee benefit plan is canceled.</span></span> <span data-ttu-id="29851-118">Er wird beim Stornierungsvorgang in einem Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="29851-118">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="29851-119">Benutzer können ihn im Feld **Stornierungsursachencode** bei Bedarf ändern.</span><span class="sxs-lookup"><span data-stu-id="29851-119">Users can change it the **Cancellation reason code** if necessary.</span></span> |
   | <span data-ttu-id="29851-120">**Ursachencode erneut öffnen**</span><span class="sxs-lookup"><span data-stu-id="29851-120">**Reopen reason code**</span></span> | <span data-ttu-id="29851-121">Der Ursachencode, der verwendet wird, wenn ein Mitarbeitervorteilsplan erneut geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="29851-121">The reason code to use when an employee benefit plan is reopened.</span></span> <span data-ttu-id="29851-122">Er wird beim Stornierungsvorgang in einem Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="29851-122">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="29851-123">Benutzer können ihn im Feld **Ursachencode erneut öffnen** bei Bedarf ändern.</span><span class="sxs-lookup"><span data-stu-id="29851-123">Users can change the **Reopen reason code** if necessary.</span></span> | 
   | <span data-ttu-id="29851-124">**Ursachencode für Lebensereignis**</span><span class="sxs-lookup"><span data-stu-id="29851-124">**Life event reason code**</span></span> | <span data-ttu-id="29851-125">Der zu verwendende Ursachencode, wenn ein Lebensereignis eintritt.</span><span class="sxs-lookup"><span data-stu-id="29851-125">The reason code to use when a life event occurs.</span></span> |
   | <span data-ttu-id="29851-126">**Ursachencode für Satzänderung**</span><span class="sxs-lookup"><span data-stu-id="29851-126">**Rate change reason code**</span></span> | <span data-ttu-id="29851-127">Der Ursachencode, der beim Stornieren und erneuten Öffnen eines Personalvorteilsplans verwendet werden soll, wenn die Satzänderung aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="29851-127">The reason code to use when canceling and reopening an employee benefit plan during the rate change update process.</span></span> <span data-ttu-id="29851-128">Er zeigt an, welche Datensätze durch die Aktualisierung der Satzänderung geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="29851-128">It indicates which records were changed by the rate change update process.</span></span> |
   | <span data-ttu-id="29851-129">**Vergütungsjahresgehalt**</span><span class="sxs-lookup"><span data-stu-id="29851-129">**Benefits annual salary**</span></span> | <span data-ttu-id="29851-130">Ermöglicht das Festlegen eines Betrags **Jahresgehalt für Vorteile** für einen Mitarbeiter.</span><span class="sxs-lookup"><span data-stu-id="29851-130">Enables you to set a **Benefits annual salary** amount for an employee.</span></span> <span data-ttu-id="29851-131">Die Personalverwaltung wird den Betrag **Jahresgehalt für Vorteile** verwenden, wenn Deckungssummen festgelegt werden, anstatt eines festen jährlichen Vergütungsbetrags.</span><span class="sxs-lookup"><span data-stu-id="29851-131">Human Resources will use the **Benefits annual salary** amount when determining coverage amounts, instead of the fixed compensation annual amount.</span></span> |
   | <span data-ttu-id="29851-132">**Neueinstellung möglich**</span><span class="sxs-lookup"><span data-stu-id="29851-132">**New hire eligible**</span></span> | <span data-ttu-id="29851-133">Gibt an, ob Neueinstellungen zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="29851-133">Specifies whether new hires are eligible.</span></span> |
   | <span data-ttu-id="29851-134">**Registrierungsperiode für Neueinstellungen**</span><span class="sxs-lookup"><span data-stu-id="29851-134">**New hire enrollment period**</span></span> | <span data-ttu-id="29851-135">Die Periode, für die die Registrierung einer Neueinstellung zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="29851-135">The period of time the new hire enrollment is allowed.</span></span></br></br><span data-ttu-id="29851-136">**Hinweis**: Diese Einstellung überschreibt jede Registrierungsperiode für Neueinstellungen, die Sie in der Planberechtigungsregel festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="29851-136">**Note**: This setting overrides any new hire enrollment period you set on the plan eligibility rule.</span></span> |
   | <span data-ttu-id="29851-137">**Standard-Zahlungshäufigkeit**</span><span class="sxs-lookup"><span data-stu-id="29851-137">**Default pay frequency**</span></span> | <span data-ttu-id="29851-138">Die Standardzahlungshäufigkeit, die verwendet wird, wenn neue Mitarbeiter hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="29851-138">The default pay frequency to use when new workers are added.</span></span> |
   | <span data-ttu-id="29851-139">**Lebensereignisse aktiviert**</span><span class="sxs-lookup"><span data-stu-id="29851-139">**Life events enabled**</span></span> | <span data-ttu-id="29851-140">Aktiviert Lebensereignisse.</span><span class="sxs-lookup"><span data-stu-id="29851-140">Enables life events.</span></span> |
   | <span data-ttu-id="29851-141">**Legacy-Vergütungsformulare ausblenden**</span><span class="sxs-lookup"><span data-stu-id="29851-141">**Hide legacy benefit forms**</span></span> | <span data-ttu-id="29851-142">Ermöglicht das Ausblenden von Legacy-Vergütungsformularen.</span><span class="sxs-lookup"><span data-stu-id="29851-142">Allows you to hide legacy benefit forms.</span></span> |
   | <span data-ttu-id="29851-143">**Vorteilsüberprüfung**</span><span class="sxs-lookup"><span data-stu-id="29851-143">**Benefit verification**</span></span> | <span data-ttu-id="29851-144">Der Überprüfungstext, der beim Auschecken der Self-Service-Vorteile verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="29851-144">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="29851-145">**Beauftragten automatisch auswählen**</span><span class="sxs-lookup"><span data-stu-id="29851-145">**Auto select designees**</span></span> | <span data-ttu-id="29851-146">Gibt an, ob Unterhaltsberechtigte und Begünstigte ausgehend von ihrem Anspruch für Planoptionen automatisch ausgewählt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="29851-146">Specifies whether to automatically select dependents and beneficiaries, based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="29851-147">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="29851-147">Select **Save**.</span></span>

## <a name="configure-employee-self-service-parameters"></a><span data-ttu-id="29851-148">Mitarbeiter-Self-Service-Parameter konfigurieren</span><span class="sxs-lookup"><span data-stu-id="29851-148">Configure Employee self-service parameters</span></span>

1. <span data-ttu-id="29851-149">Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Setup** die Option **Personalverwaltungsparameter**.</span><span class="sxs-lookup"><span data-stu-id="29851-149">In the **Benefits management** workspace, under **Setup**, select **Human Resources Parameters**.</span></span>

2. <span data-ttu-id="29851-150">Definieren Sie auf der Registerkarte **Vergütungsverwaltung** die Werte für die folgenden Felder:</span><span class="sxs-lookup"><span data-stu-id="29851-150">In the **Benefits management** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="29851-151">Feld</span><span class="sxs-lookup"><span data-stu-id="29851-151">Field</span></span> | <span data-ttu-id="29851-152">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="29851-152">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="29851-153">**Vorteilsüberprüfung**</span><span class="sxs-lookup"><span data-stu-id="29851-153">**Benefit verification**</span></span> | <span data-ttu-id="29851-154">Der Überprüfungstext, der beim Auschecken der Self-Service-Vorteile verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="29851-154">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="29851-155">**Beauftragten automatisch auswählen**</span><span class="sxs-lookup"><span data-stu-id="29851-155">**Auto select designees**</span></span> | <span data-ttu-id="29851-156">Gibt an, ob Unterhaltsberechtigte und Begünstigte basierend auf ihrer Berechtigung für Planoptionen automatisch ausgewählt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="29851-156">Specifies whether to automatically select dependents and beneficiaries based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="29851-157">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="29851-157">Select **Save**.</span></span>


