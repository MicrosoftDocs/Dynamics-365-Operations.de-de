---
title: Neue Kanban-Regel durch Duplizieren einer vorhandenen Kanban-Regel erstellen
description: Ziel dieser Prozedur ist es, ein Duplikat einer vorhandenen Kanban-Regel zu erstellen.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d80bf0318234f858e51fb461894238894e01717c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829065"
---
# <a name="create-a-new-kanban-rule-by-duplicating-an-existing-kanban-rule"></a><span data-ttu-id="3401d-103">Neue Kanban-Regel durch Duplizieren einer vorhandenen Kanban-Regel erstellen</span><span class="sxs-lookup"><span data-stu-id="3401d-103">Create a new kanban rule by duplicating an existing kanban rule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3401d-104">Ziel dieser Prozedur ist es, ein Duplikat einer vorhandenen Kanban-Regel zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3401d-104">This procedure focuses on creating a duplicate of an existing kanban rule.</span></span> <span data-ttu-id="3401d-105">Dies ist hilfreich, wenn Sie neue Kanban-Regeln basierend auf vorhandenen Kanban-Regeln erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="3401d-105">This is useful if you want to create new kanban rules based on existing kanban rules.</span></span> <span data-ttu-id="3401d-106">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="3401d-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="3401d-107">Diese Vorgehensweise ist für den Verfahrenstechniker oder den Wertstrom-Manager vorgesehen, da dieser die Produktion für einen geänderten Produktionsfluss oder eine neue Auffüllungsregel vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="3401d-107">This procedure is intended for the process engineer or the value stream manager as they prepare production for a changed production flow or a new replenishment rule.</span></span>


## <a name="select-a-kanban-rule"></a><span data-ttu-id="3401d-108">Kanban-Regel auswählen</span><span class="sxs-lookup"><span data-stu-id="3401d-108">Select a kanban rule</span></span>
1. <span data-ttu-id="3401d-109">Wechseln Sie zu Kanban-Regeln.</span><span class="sxs-lookup"><span data-stu-id="3401d-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="3401d-110">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="3401d-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="3401d-111">Wählen Sie die Kanban-Regel 000017 für Produkt M0006 aus.</span><span class="sxs-lookup"><span data-stu-id="3401d-111">Select kanban rule 000017 for Product M0006.</span></span>  

## <a name="duplicate-a-kanban-rule"></a><span data-ttu-id="3401d-112">Kanban-Regel duplizieren</span><span class="sxs-lookup"><span data-stu-id="3401d-112">Duplicate a kanban rule</span></span>
1. <span data-ttu-id="3401d-113">Klicken Sie auf das Formular "Kanban-Regel duplizieren"</span><span class="sxs-lookup"><span data-stu-id="3401d-113">Click Duplicate kanban rule.</span></span>
    * <span data-ttu-id="3401d-114">Wird eine Kanban-Regel dupliziert, ist es möglich, Typ, Datum, Aktivitäten und die Produktauswahl zu ändern.</span><span class="sxs-lookup"><span data-stu-id="3401d-114">When duplicating a kanban rule, it is possible to change type, dates, activities, and the product selection.</span></span> <span data-ttu-id="3401d-115">Ändern Sie das Produkt für diese Prozedur im nächsten Schritt.</span><span class="sxs-lookup"><span data-stu-id="3401d-115">Change the product for this procedure in the next step.</span></span>  
2. <span data-ttu-id="3401d-116">Geben Sie im Feld "Produkt" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="3401d-116">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="3401d-117">Wählen Sie M0007 aus.</span><span class="sxs-lookup"><span data-stu-id="3401d-117">Select M0007.</span></span>  
3. <span data-ttu-id="3401d-118">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="3401d-118">Click OK.</span></span>
    * <span data-ttu-id="3401d-119">Beachten Sie, dass ein Duplikat von Kanban-Regel 000017 erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="3401d-119">Note that a duplicate of kanban rule 000017 is created.</span></span>    



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]