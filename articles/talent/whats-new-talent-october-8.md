---
title: "Neuheiten oder Änderungen in Dynamics 365 for Talent Core HR (1. Oktober 2018)"
description: "In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 for Talent Core HR entweder neu oder geändert sind."
author: Darinkramer
manager: AnnBe
ms.date: 10/07/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-07
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: 657c19896b20a514dc5308bf7fb086085b482fec
ms.openlocfilehash: 92eb1508905309294e17b770829b1c5a22be1316
ms.contentlocale: de-de
ms.lasthandoff: 10/08/2018

---

# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-october-8-2018"></a><span data-ttu-id="6ff43-103">Neuheiten oder Änderungen in Dynamics 365 for Talent Core HR (8. Oktober 2018)</span><span class="sxs-lookup"><span data-stu-id="6ff43-103">What's new or changed in Dynamics 365 for Talent Core HR (October 8, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6ff43-104">**Build 8.1.1050.0**</span><span class="sxs-lookup"><span data-stu-id="6ff43-104">**Build 8.1.1050.0**</span></span>

<span data-ttu-id="6ff43-105">In diesem Thema werden die Funktionen beschrieben, die in Core HR entweder neu oder geändert sind.</span><span class="sxs-lookup"><span data-stu-id="6ff43-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="allow-other-dates-to-be-used-on-leave-tier-basis-leave-management"></a><span data-ttu-id="6ff43-106">Gestatten Sie andere Daten, die für Urlaubsebenengrundlagen (Urlaubs-Verwaltung )verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6ff43-106">Allow other dates to be used on leave tier basis (Leave Management)</span></span>

<span data-ttu-id="6ff43-107">Wenn den Mitarbeitern Sonderurlaub bewilligt wird, bestimmt die Prämienebenengrundlage, wie viel Freizeit für einen Mitarbeiter anfällt.</span><span class="sxs-lookup"><span data-stu-id="6ff43-107">When awarding leave to employees, the award tier basis determines how much time off an employee accrues.</span></span> <span data-ttu-id="6ff43-108">Aktuell basieren diese Ebenen auf Grundlage von Mitarbeiterstartdatum und Dienstalter.</span><span class="sxs-lookup"><span data-stu-id="6ff43-108">Currently, these tiers are based on employee start date and seniority date.</span></span> <span data-ttu-id="6ff43-109">In einigen Szenarien brauchen Organisationen diese Ebenen, die auf anderen Daten basieren, wie Jahrestagsdatum oder ursprüngliches Einstellungsdatum.</span><span class="sxs-lookup"><span data-stu-id="6ff43-109">In some scenarios, organizations need these tiers to be based on other dates, like anniversary date or original hire date.</span></span> <span data-ttu-id="6ff43-110">Diese Datumsangaben werden bereits im Urlaubplan, die bestimmen, wann Abgrenzungen finden statt, die Möglichkeit verwendet, sodass diese gleichen Daten verwendet werden können, wenn ein Mitarbeiter in einem Plan wurden hinzugefügt, um dem Abgrenzungsbetrag zu bestimmen registriert.</span><span class="sxs-lookup"><span data-stu-id="6ff43-110">These dates are already used on the leave plan to determine when accruals happen, the ability for these same dates to be used when an employee is enrolled in a plan have been added to determine the accrual amount.</span></span> 

## <a name="other-changes"></a><span data-ttu-id="6ff43-111">Andere Änderungen</span><span class="sxs-lookup"><span data-stu-id="6ff43-111">Other changes</span></span>
<span data-ttu-id="6ff43-112">Verschiedene Korrekturen sind in dieser Version berücksichtigt worden.</span><span class="sxs-lookup"><span data-stu-id="6ff43-112">Miscellanous fixes have been included in this release.</span></span>

## <a name="known-issue"></a><span data-ttu-id="6ff43-113">Bekannte Probleme</span><span class="sxs-lookup"><span data-stu-id="6ff43-113">Known issue</span></span>

<span data-ttu-id="6ff43-114">**Problem:** Wenn einer Arbeitskraft ein neuer Anhang hinzugefügt wird, werden die Schaltflächen **Neu** und **Bearbeiten** abgeblendet. **Problemumgehung:**, Bevor die Anhangsseite geöffnet wird, überprüfen Sie, dass die Infoboxen **Arbeitskraft** geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="6ff43-114">**Issue:** When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out. **Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="6ff43-115">Wenn die Infoboxen geschlossen werden, wenn die **Arbeitskraft**-Seite geladen wird, werden die Anhangschaltflächen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="6ff43-115">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="6ff43-116">(Dieses Problem wird in der folgenden Plattformaktualisierung korrigiert.)</span><span class="sxs-lookup"><span data-stu-id="6ff43-116">(This issue will be fixed in the next platform update.)</span></span>

