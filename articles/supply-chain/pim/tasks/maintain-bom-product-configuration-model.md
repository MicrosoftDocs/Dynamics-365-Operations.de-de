---
title: Stückliste für ein Produktkonfigurationsmodell verwalten
description: Die Ausführung dieser Prozedur erfordert ein vorhandenes Produktkonfigurationsmodell.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCBOMLineDetails, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b4ad73265e321b6339c061a7866b55cb2769954b
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921316"
---
# <a name="maintain-bom-for-a-product-configuration-model"></a><span data-ttu-id="5b09e-103">Stückliste für ein Produktkonfigurationsmodell verwalten</span><span class="sxs-lookup"><span data-stu-id="5b09e-103">Maintain BOM for a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5b09e-104">Die Ausführung dieser Prozedur erfordert ein vorhandenes Produktkonfigurationsmodell.</span><span class="sxs-lookup"><span data-stu-id="5b09e-104">Running this procedure requires an existing product configuration model.</span></span> <span data-ttu-id="5b09e-105">Das Spitzenlautsprechermodell im Vorführungsunternehmen USMF wird verwendet, um diese Prozedur zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5b09e-105">The High end speaker model in the demo company USMF is used to create this procedure.</span></span>

## <a name="add-a-bom-line"></a><span data-ttu-id="5b09e-106">Hinzufügen einer Stücklistenposition</span><span class="sxs-lookup"><span data-stu-id="5b09e-106">Add a BOM line</span></span>

1. <span data-ttu-id="5b09e-107">Wechseln Sie zu **Produktinformationsmanagement \> Produkte \> Produktkonfigurationsmodelle**.</span><span class="sxs-lookup"><span data-stu-id="5b09e-107">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="5b09e-108">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="5b09e-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="5b09e-109">Wählen Sie den Spitzenlautsprecher für diese Prozedur aus.</span><span class="sxs-lookup"><span data-stu-id="5b09e-109">Select the High end speaker for this procedure.</span></span>  
1. <span data-ttu-id="5b09e-110">Wählen Sie in der Liste den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="5b09e-110">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="5b09e-111">Erweitern Sie den Abschnitt **Stücklisten**.</span><span class="sxs-lookup"><span data-stu-id="5b09e-111">Expand the **BOM lines** section.</span></span>
1. <span data-ttu-id="5b09e-112">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="5b09e-112">Select **Add**.</span></span>
1. <span data-ttu-id="5b09e-113">Geben Sie im Feld **Name** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="5b09e-113">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="5b09e-114">Geben Sie im Feld **Beschreibung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="5b09e-114">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="5b09e-115">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="5b09e-115">Select **Save**.</span></span>

## <a name="add-bom-line-details"></a><span data-ttu-id="5b09e-116">Hinzufügen von Stücklistenpositionsdetails</span><span class="sxs-lookup"><span data-stu-id="5b09e-116">Add BOM line details</span></span>

1. <span data-ttu-id="5b09e-117">Wählen Sie **Stücklisten-Zeilen-Details**.</span><span class="sxs-lookup"><span data-stu-id="5b09e-117">Select **BOM line details**.</span></span>
2. <span data-ttu-id="5b09e-118">Geben Sie im Feld **Artikelnummer** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="5b09e-118">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="5b09e-119">Sie können beispielsweise Artikel "M0055" auswählen.</span><span class="sxs-lookup"><span data-stu-id="5b09e-119">For example, you can select the item M0055.</span></span>  
    * <span data-ttu-id="5b09e-120">Für jede Stücklistenpositionseigenschaft können Sie festlegen, ob ein fester Wert oder ein Attribut zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="5b09e-120">For each BOM line property, you can select if it takes a fixed value or is mapped to an attribute.</span></span>  
3. <span data-ttu-id="5b09e-121">Aktivieren Sie das Kontrollkästchen **Setzen**.</span><span class="sxs-lookup"><span data-stu-id="5b09e-121">Select the **Set** check box.</span></span>
4. <span data-ttu-id="5b09e-122">Wählen Sie *Ja* im Feld **Berechnung**.</span><span class="sxs-lookup"><span data-stu-id="5b09e-122">Select *Yes* in the **Calculation** field.</span></span>
    * <span data-ttu-id="5b09e-123">Das Festlegen der Eigenschaft **Berechnung** auf *Ja* stellt sicher, dass die Zeile der Stückliste in die Kalkulation einbezogen wird.</span><span class="sxs-lookup"><span data-stu-id="5b09e-123">Setting the **Calculation** property to *Yes* ensures that the BOM line is included in cost calculations.</span></span>  
5. <span data-ttu-id="5b09e-124">Wählen Sie die Registerkarte **Einrichten**.</span><span class="sxs-lookup"><span data-stu-id="5b09e-124">Select the **Setup** tab.</span></span>
6. <span data-ttu-id="5b09e-125">Aktivieren Sie das Kontrollkästchen **Setzen**.</span><span class="sxs-lookup"><span data-stu-id="5b09e-125">Select the **Set** check box.</span></span>
7. <span data-ttu-id="5b09e-126">Geben Sie im Feld **Menge** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="5b09e-126">In the **Quantity** field, enter a number.</span></span>
    * <span data-ttu-id="5b09e-127">Das Feld "Menge" bestimmt die Menge des Artikels, der in der Stückliste enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="5b09e-127">The quantity field determines how much of the item that will be included in the BOM.</span></span> <span data-ttu-id="5b09e-128">Dieser könnte ein offensichtlicher Kandidat für eine Attributzuordnung sein.</span><span class="sxs-lookup"><span data-stu-id="5b09e-128">This could be an obvious candidate for an attribute mapping.</span></span>  
8. <span data-ttu-id="5b09e-129">Wählen Sie die Registerkarte **Dimension**.</span><span class="sxs-lookup"><span data-stu-id="5b09e-129">Select the **Dimension** tab.</span></span>
    * <span data-ttu-id="5b09e-130">Überprüfen Sie, ob vorhandene Produktdimensionen aktiv sind und daher ein Wert oder ein Attribut zugewiesen sein muss..</span><span class="sxs-lookup"><span data-stu-id="5b09e-130">Verify if any of the product dimensions are active,  and therefore must have a value or attribute assigned.</span></span>  
9. <span data-ttu-id="5b09e-131">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b09e-131">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]