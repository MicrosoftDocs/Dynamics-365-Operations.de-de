---
title: Beurlaubung verwalten
description: Diese Prozedur führt Sie Schritt für Schritt durch die Erstellung von Sonderurlaubs-Datensätzen für Mitarbeiter.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmWorker, HcmEmploymentLeave
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 002700ae7f6474b48fbe09cb3aaa72e9516b8224
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143545"
---
# <a name="manage-leave-of-absence"></a><span data-ttu-id="8e235-103">Beurlaubung verwalten</span><span class="sxs-lookup"><span data-stu-id="8e235-103">Manage leave of absence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8e235-104">Diese Prozedur führt Sie Schritt für Schritt durch die Erstellung von Sonderurlaubs-Datensätzen für Mitarbeiter.</span><span class="sxs-lookup"><span data-stu-id="8e235-104">This procedure walks through the creation of employee leave records.</span></span> <span data-ttu-id="8e235-105">Sie können Abwesenheitszeit nach Ursachen nachverfolgen. Dazu gehören medizinischen, pädagogischen oder elterliche Aktivitäten.</span><span class="sxs-lookup"><span data-stu-id="8e235-105">You can track leave time for reasons that include medical, educational, or parental activities.</span></span> <span data-ttu-id="8e235-106">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="8e235-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="8e235-107">Wechseln Sie zu "Personalverwaltung" > "Arbeitskräfte" > "Mitarbeiter".</span><span class="sxs-lookup"><span data-stu-id="8e235-107">Go to Human resources > Workers > Employees.</span></span>
2. <span data-ttu-id="8e235-108">Wählen Sie in der Liste einen Mitarbeiter aus.</span><span class="sxs-lookup"><span data-stu-id="8e235-108">In the list, select an employee.</span></span>
3. <span data-ttu-id="8e235-109">Zeigen Sie detaillierte Informationen für den ausgewählten Mitarbeiter an, indem Sie den Namen des Mitarbeiters auswählen.</span><span class="sxs-lookup"><span data-stu-id="8e235-109">Display detailed information for the selected employee by selecting the employee's name.</span></span>
4. <span data-ttu-id="8e235-110">Klicken Sie auf die Registerkarte "Anstellung".</span><span class="sxs-lookup"><span data-stu-id="8e235-110">Click the Employment tab.</span></span>
5. <span data-ttu-id="8e235-111">Klicken Sie auf "Sonderurlaub".</span><span class="sxs-lookup"><span data-stu-id="8e235-111">Click Leave.</span></span>
6. <span data-ttu-id="8e235-112">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="8e235-112">Click New.</span></span>
7. <span data-ttu-id="8e235-113">Klicken Sie im Feld "Sonderurlaubstyp" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8e235-113">In the Leave type field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="8e235-114">Sie können einen Sonderurlaubstyp einem Einkommenscode im Formular "Sonderurlaubstypen" zuordnen.</span><span class="sxs-lookup"><span data-stu-id="8e235-114">You can associate a leave type to an earning code in the Leave types form.</span></span> <span data-ttu-id="8e235-115">Wenn ein Sonderurlaubstyp einem Einkommenscode zugeordnet ist, wird eine Einkommensposition mit dem zugeordneten Einkommenscode während der Sonderurlaubsperiode, die Sie eingeben, generiert.</span><span class="sxs-lookup"><span data-stu-id="8e235-115">If a leave type is associated with an earning code, an earning line will be generated with the associated earning code during the leave period that you enter.</span></span>  
8. <span data-ttu-id="8e235-116">Wählen Sie in der Liste einen Sonderurlaubstyp aus.</span><span class="sxs-lookup"><span data-stu-id="8e235-116">In the list, select a leave type.</span></span> 
    * <span data-ttu-id="8e235-117">Beispiel: Annahme</span><span class="sxs-lookup"><span data-stu-id="8e235-117">For example: Adoption</span></span>  
9. <span data-ttu-id="8e235-118">Geben Sie das Datum ein, an dem der Sonderurlaub beginnen soll.</span><span class="sxs-lookup"><span data-stu-id="8e235-118">Enter the date that the leave will start.</span></span> <span data-ttu-id="8e235-119">Beispiel: "26.10.2015"</span><span class="sxs-lookup"><span data-stu-id="8e235-119">Example: '2015-10-26'</span></span>
    * <span data-ttu-id="8e235-120">Beispiel: 26.10.2015</span><span class="sxs-lookup"><span data-stu-id="8e235-120">For example:  2015-10-26</span></span>  
10. <span data-ttu-id="8e235-121">Geben Sie das Datum ein, an dem der Sonderurlaub beginnen soll.</span><span class="sxs-lookup"><span data-stu-id="8e235-121">Enter the date that the leave will start.</span></span> 
    * <span data-ttu-id="8e235-122">Beispiel: 20.11.2015</span><span class="sxs-lookup"><span data-stu-id="8e235-122">For example:  2015-11-20</span></span>  
11. <span data-ttu-id="8e235-123">Geben Sie im Hinweisfeld eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="8e235-123">In the note field, enter a description.</span></span>
    * <span data-ttu-id="8e235-124">Beispiel: Sonderurlaub zur Annahme</span><span class="sxs-lookup"><span data-stu-id="8e235-124">For example: Leave for adoption</span></span>  
12. <span data-ttu-id="8e235-125">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="8e235-125">Click Save.</span></span>

