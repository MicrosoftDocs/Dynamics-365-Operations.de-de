---
title: Chargenattribute für ein Produkt erstellen
description: Im folgenden Verfahren wird dargestellt, wie ein Stapelverarbeitungsattribut erstellt, Standardwertbereiche zugeordnet und das Attribut in eine Gruppe einbezogen wird.
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PdsBatchAttrib
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 66757cdb93c67129c19ae226caa271a44c759206
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5218560"
---
# <a name="create-batch-attributes-for-a-product"></a><span data-ttu-id="b58e0-103">Chargenattribute für ein Produkt erstellen</span><span class="sxs-lookup"><span data-stu-id="b58e0-103">Create batch attributes for a product</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b58e0-104">Im folgenden Verfahren wird dargestellt, wie ein Stapelverarbeitungsattribut erstellt, Standardwertbereiche zugeordnet und das Attribut in eine Gruppe einbezogen wird.</span><span class="sxs-lookup"><span data-stu-id="b58e0-104">This procedure shows how to create a batch attribute, assign default value ranges, and include the attribute in a group.</span></span> <span data-ttu-id="b58e0-105">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist das Unternehmen USP2.</span><span class="sxs-lookup"><span data-stu-id="b58e0-105">The demo data company used to create this procedure is the USP2 Company.</span></span>

1. <span data-ttu-id="b58e0-106">Wechseln Sie zu "Lagerverwaltung" > "Einrichten" > "Charge" > "Stapelverarbeitungsattribut".</span><span class="sxs-lookup"><span data-stu-id="b58e0-106">Go to Inventory management > Setup > Batch > Batch attributes.</span></span>
2. <span data-ttu-id="b58e0-107">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="b58e0-107">Click New.</span></span>
3. <span data-ttu-id="b58e0-108">Geben Sie im Feld "Attribut" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="b58e0-108">In the Attribute field, type a value.</span></span>
4. <span data-ttu-id="b58e0-109">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="b58e0-109">In the Description field, type a value.</span></span>
5. <span data-ttu-id="b58e0-110">Wählen Sie im Feld "Attribut" "Bruch" aus.</span><span class="sxs-lookup"><span data-stu-id="b58e0-110">In the Attribute type field, select 'Fraction'.</span></span>
    * <span data-ttu-id="b58e0-111">Bei diesem Verfahren wird der Bruchtyp verwendet, um Dezimalwerte zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="b58e0-111">This procedure uses the Fraction type to enable decimal values.</span></span> <span data-ttu-id="b58e0-112">Sie können andere Attributtypen auswählen.</span><span class="sxs-lookup"><span data-stu-id="b58e0-112">You can select other attribute types.</span></span> <span data-ttu-id="b58e0-113">Wenn Sie den Enumerationstyp auswählen, müssen Sie Werte in der Enumerationsliste eingeben, bevor Sie einen Wert in das Feld "Ziel" eingeben können.</span><span class="sxs-lookup"><span data-stu-id="b58e0-113">If you select the Enumeration type, you must enter values in the enumeration list before you can enter a value in the Target field.</span></span>  
6. <span data-ttu-id="b58e0-114">Geben Sie im Feld "Minimum" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="b58e0-114">In the Minimum field, enter a number.</span></span>
7. <span data-ttu-id="b58e0-115">Geben Sie im Feld "Maximum" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="b58e0-115">In the Maximum field, enter a number.</span></span>
8. <span data-ttu-id="b58e0-116">Geben Sie im Feld "Inkrement" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="b58e0-116">In the Increment field, enter a number.</span></span>
9. <span data-ttu-id="b58e0-117">Geben Sie im Feld "Ziel" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="b58e0-117">In the Target field, type a value.</span></span>
10. <span data-ttu-id="b58e0-118">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="b58e0-118">Click Save.</span></span>
11. <span data-ttu-id="b58e0-119">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="b58e0-119">Close the page.</span></span>
12. <span data-ttu-id="b58e0-120">Wechseln Sie zu "Lagerverwaltung" > "Einrichten" > "Charge" > "Stapelverarbeitungsattributgruppen".</span><span class="sxs-lookup"><span data-stu-id="b58e0-120">Go to Inventory management > Setup > Batch > Batch attribute groups.</span></span>
13. <span data-ttu-id="b58e0-121">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="b58e0-121">Click New.</span></span>
14. <span data-ttu-id="b58e0-122">Geben Sie im Feld "Attributgruppe" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="b58e0-122">In the Attribute group field, type a value.</span></span>
15. <span data-ttu-id="b58e0-123">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="b58e0-123">In the Description field, type a value.</span></span>
16. <span data-ttu-id="b58e0-124">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="b58e0-124">Click Save.</span></span>
17. <span data-ttu-id="b58e0-125">Klicken Sie auf Gruppenattribute.</span><span class="sxs-lookup"><span data-stu-id="b58e0-125">Click Group attributes.</span></span>
18. <span data-ttu-id="b58e0-126">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="b58e0-126">Click New.</span></span>
19. <span data-ttu-id="b58e0-127">Klicken Sie im Feld "Attribut" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b58e0-127">In the Attribute field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="b58e0-128">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="b58e0-128">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="b58e0-129">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="b58e0-129">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b58e0-130">Ein Attribut kann in eine der Gruppen einbezogen werden.</span><span class="sxs-lookup"><span data-stu-id="b58e0-130">An attribute can be included in any of the groups.</span></span>  
22. <span data-ttu-id="b58e0-131">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="b58e0-131">Click Save.</span></span>
23. <span data-ttu-id="b58e0-132">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="b58e0-132">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]