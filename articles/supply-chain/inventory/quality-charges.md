---
title: Belastungen für Qualitätsmangel-Vorgänge
description: Dieses Thema beschreibt, wie Sie Qualitätsbelastungen erstellen, die mit Vorgängen für eine Nichtkonformität verwendet werden können.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestMiscCharges
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 382890232bff47a885840af1eb7e91d27bb46cae
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022299"
---
# <a name="charges-for-nonconformance-operations"></a><span data-ttu-id="32615-103">Belastungen für Qualitätsmangel-Vorgänge</span><span class="sxs-lookup"><span data-stu-id="32615-103">Charges for nonconformance operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="32615-104">Dieses Thema beschreibt, wie Sie Qualitätsbelastungen erstellen, die mit Vorgängen für eine Nichtkonformität verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="32615-104">This topic describes how to create quality charges that can be used with operations for a nonconformance.</span></span>

<span data-ttu-id="32615-105">Sie verwenden die Seite **Qualitätsbelastungen**, um die Arten von Belastungen zu definieren, die zu Vorgängen für einen Qualitätsmangel hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="32615-105">You use the **Quality charges** page to define the types of charges that can be added to operations for a nonconformance.</span></span> <span data-ttu-id="32615-106">Mit Belastungen können Sie Details zu Gebühren oder Kosten verfolgen, die Sie einem Debitor für Qualitätsmängel schulden oder die ein Kreditor Ihnen für erhaltene Qualitätsmängel schuldet.</span><span class="sxs-lookup"><span data-stu-id="32615-106">Charges let you track details about fees or charges that you owe to a customer for nonconforming products, or that a vendor owes to you for nonconforming products that you received.</span></span> <span data-ttu-id="32615-107">Sie könnten auch Belastungen verwenden, um Kosten zu verfolgen, die für externe Kreditor oder Dienstleistungen zur Durchführung eines Vorgangs erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="32615-107">You might also use charges to track costs that are required for external vendors or services to perform an operation.</span></span>

## <a name="examples-of-quality-charges"></a><span data-ttu-id="32615-108">Beispiele für Qualitätsbelastungen</span><span class="sxs-lookup"><span data-stu-id="32615-108">Examples of quality charges</span></span>

<span data-ttu-id="32615-109">Sie arbeiten für eine produzierende Firma.</span><span class="sxs-lookup"><span data-stu-id="32615-109">You work for a manufacturing company.</span></span> <span data-ttu-id="32615-110">Ihre Firma hat Verträge mit mehreren Kreditor.</span><span class="sxs-lookup"><span data-stu-id="32615-110">Your company has contracts with several vendors.</span></span> <span data-ttu-id="32615-111">In diesen Verträgen werden Standards für die pünktliche Lieferung, Schäden und Produktqualität von Elementen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="32615-111">Those contracts outline standards for on-time shipment, damages, and product quality for items.</span></span> <span data-ttu-id="32615-112">Ebenso haben mehrere Ihrer Debitoren Vereinbarungen mit Ihrer Firma über Retouren, Schäden und Produktqualität.</span><span class="sxs-lookup"><span data-stu-id="32615-112">Likewise, several of your customers have agreements with your company about returns, damages, and product quality.</span></span>

<span data-ttu-id="32615-113">Eine Gebührenstruktur wird für jeden Umstand definiert und im Vertrag festgelegt.</span><span class="sxs-lookup"><span data-stu-id="32615-113">A fee structure is defined for each circumstance and specified in the contract.</span></span> <span data-ttu-id="32615-114">Sie können Qualitätsbelastungen konfigurieren, um die verschiedenen Arten von Belastungen zu umreißen, z. B. *Schäden*, *Verspätete Lieferung* und *Qualität*.</span><span class="sxs-lookup"><span data-stu-id="32615-114">You can configure quality charges to outline the various types of charges, such as *Damages*, *Late shipment*, and *Quality*.</span></span> <span data-ttu-id="32615-115">Wenn Sie dann einen Qualitätsmangel erstellen, fügen Sie einen oder mehrere Vorgänge hinzu.</span><span class="sxs-lookup"><span data-stu-id="32615-115">Then, when you create a nonconformance, you add one or more operations.</span></span> <span data-ttu-id="32615-116">Für jeden Vorgang wählen Sie **Gebühren**, um die Details zu den Gebühren zu definieren.</span><span class="sxs-lookup"><span data-stu-id="32615-116">For each operation, you select **Charges** to define the details about the fees.</span></span>

## <a name="create-a-quality-charge"></a><span data-ttu-id="32615-117">Erstellen Sie eine Qualitätsgebühr</span><span class="sxs-lookup"><span data-stu-id="32615-117">Create a quality charge</span></span>

1. <span data-ttu-id="32615-118">Gehen Sie zu **Bestandsverwaltung \> Einrichten \> Qualitätsmanagement \> Qualitätsbelastungen**.</span><span class="sxs-lookup"><span data-stu-id="32615-118">Go to **Inventory management \> Setup \> Quality management \> Quality charges**.</span></span>
1. <span data-ttu-id="32615-119">Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Zeile zum Raster hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="32615-119">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="32615-120">Legen Sie für die neue Zeile die folgenden Felder fest:</span><span class="sxs-lookup"><span data-stu-id="32615-120">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="32615-121">**Belastungen code** – Geben Sie eine eindeutige ID oder einen Namen für die Qualitätsgebühr ein.</span><span class="sxs-lookup"><span data-stu-id="32615-121">**Charges code** – Enter a unique ID or name for the quality charge.</span></span>
    - <span data-ttu-id="32615-122">**Beschreibung** – Geben Sie eine detaillierte Beschreibung der Qualitätsgebühr ein.</span><span class="sxs-lookup"><span data-stu-id="32615-122">**Description** – Enter a detailed description of the quality charge.</span></span>

1. <span data-ttu-id="32615-123">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="32615-123">Close the page.</span></span>

## <a name="add-a-quality-charge-to-an-operation-for-a-nonconformance"></a><span data-ttu-id="32615-124">Fügen Sie eine qualitative Belastung zu einem Vorgang für einen Qualitätsmangel hinzu</span><span class="sxs-lookup"><span data-stu-id="32615-124">Add a quality charge to an operation for a nonconformance</span></span>

<span data-ttu-id="32615-125">Details darüber, wie Sie Vorgänge zu einem Qualitätsmangel hinzufügen und ihnen Belastungen zuweisen, finden Sie unter [Vorgänge für Qualitätsmängel](quality-operations.md).</span><span class="sxs-lookup"><span data-stu-id="32615-125">For details about how to add operations to a nonconformance and apply charges to them, see [Operations for nonconformances](quality-operations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="32615-126">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="32615-126">Additional resources</span></span>

- [<span data-ttu-id="32615-127">Qualitätsmanagement – Übersicht</span><span class="sxs-lookup"><span data-stu-id="32615-127">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="32615-128">Qualitäts- und Qualitätsmangel-Management aktivieren</span><span class="sxs-lookup"><span data-stu-id="32615-128">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="32615-129">Mitarbeiter, der für die Genehmigung von Qualitätsmängeln verantwortlich ist</span><span class="sxs-lookup"><span data-stu-id="32615-129">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="32615-130">Quarantänezonen für Qualitätsmängel</span><span class="sxs-lookup"><span data-stu-id="32615-130">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="32615-131">Diagnosetypen für Qualitätsmängel</span><span class="sxs-lookup"><span data-stu-id="32615-131">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="32615-132">Qualitätsbelastungen für Qualitätsmängel</span><span class="sxs-lookup"><span data-stu-id="32615-132">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="32615-133">Vorgänge für Qualitätsmängel</span><span class="sxs-lookup"><span data-stu-id="32615-133">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="32615-134">Qualitätsmanagement für Lagerortprozesse</span><span class="sxs-lookup"><span data-stu-id="32615-134">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
