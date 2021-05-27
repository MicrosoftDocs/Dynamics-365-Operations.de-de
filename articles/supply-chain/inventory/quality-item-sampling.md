---
title: Qualitätsmanagement Artikelmusteraufnahme
description: Dieses Thema beschreibt, wie Sie eine Artikelmusteraufnahme festlegen.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventItemSampling
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ae8bfd329ca0d7c30adcd93a759ee6bea7b76278
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022227"
---
# <a name="quality-management-item-sampling"></a><span data-ttu-id="77224-103">Qualitätsmanagement Artikelmusteraufnahme</span><span class="sxs-lookup"><span data-stu-id="77224-103">Quality management item sampling</span></span>

<span data-ttu-id="77224-104">Die Artikelmusteraufnahme wird als Teil einer Qualitätsassoziation verwendet.</span><span class="sxs-lookup"><span data-stu-id="77224-104">Item sampling is used as part of a quality association.</span></span> <span data-ttu-id="77224-105">Es definiert die Menge des aktuellen physischen Bestandes, der geprüft werden muss.</span><span class="sxs-lookup"><span data-stu-id="77224-105">It defines the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="77224-106">Die Probenahme kann auf festen Mengen, einem Prozentsatz oder einem vollständigen Ladungsträger basieren.</span><span class="sxs-lookup"><span data-stu-id="77224-106">Sampling can be based on fixed quantities, a percentage, or a full license plate.</span></span>

## <a name="set-up-item-sampling"></a><span data-ttu-id="77224-107">"Artikelmusteraufnahme" einrichten</span><span class="sxs-lookup"><span data-stu-id="77224-107">Set up item sampling</span></span>

<span data-ttu-id="77224-108">Führen Sie diese Schritte aus, um die Artikelmusteraufnahme festzulegen.</span><span class="sxs-lookup"><span data-stu-id="77224-108">Follow these steps to set up item sampling.</span></span>

1. <span data-ttu-id="77224-109">Wechseln Sie zu **Lagerverwaltung \> Einstellungen \> Qualitätskontrolle \> Artikelmusteraufnahme**.</span><span class="sxs-lookup"><span data-stu-id="77224-109">Go to **Inventory management \> Setup \> Quality control \> Item sampling**.</span></span>
1. <span data-ttu-id="77224-110">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="77224-110">Select **New**.</span></span>
1. <span data-ttu-id="77224-111">Geben Sie im Feld **Artikelmusteraufnahme** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="77224-111">In the **Item sampling** field, enter a value.</span></span>
1. <span data-ttu-id="77224-112">Geben Sie im Feld **Beschreibung** einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="77224-112">In the **Description** field, enter a value.</span></span>
1. <span data-ttu-id="77224-113">Geben Sie im Feld **Wert** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="77224-113">In the **Value** field, enter a number.</span></span> <span data-ttu-id="77224-114">Dieser Wert bezieht sich auf den Wert der Mengenangabe, der im benachbarten Feld ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="77224-114">This value is related to the quantity specification value that is selected in the adjacent field.</span></span>
1. <span data-ttu-id="77224-115">Aktivieren Sie im Abschnitt **Verarbeiten** das Kontrollkästchen **Vollsperrung**, wenn bei einem fehlgeschlagenen Test die gesamte Los- oder Auftragszeilenmenge gesperrt werden soll.</span><span class="sxs-lookup"><span data-stu-id="77224-115">In the **Process** section, select the **Full blocking** check box if the whole lot or order line quantity should be blocked if a test is failed.</span></span> <span data-ttu-id="77224-116">Wenn dieses Kontrollkästchen deaktiviert ist, werden nur die Elemente im Qualitätsprüfungsauftrag gesperrt, wenn ein Test fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="77224-116">If this check box is cleared, only the items in the quality order will be blocked if a test is failed.</span></span>
1. <span data-ttu-id="77224-117">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="77224-117">Select **Save**.</span></span>
1. <span data-ttu-id="77224-118">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="77224-118">Close the page.</span></span>

> [!NOTE]
> <span data-ttu-id="77224-119">Die Funktion *Qualitätsmanagement für Lagerortprozesse* bietet zusätzliche Funktionen für die Artikelmusteraufnahme.</span><span class="sxs-lookup"><span data-stu-id="77224-119">The *Quality management for warehouse processes* feature provides additional item sampling capabilities.</span></span> <span data-ttu-id="77224-120">Es fügt das Konzept des *Artikelmusteraufnahme-Umfangs* hinzu und lässt Sie einen vollständigen Ladungsträger als Mengenangabe definieren.</span><span class="sxs-lookup"><span data-stu-id="77224-120">It adds the concept of *item sampling scope* and lets you define a full license plate as the quantity specification.</span></span> <span data-ttu-id="77224-121">Wenn Sie diese Funktion aktiviert haben, lesen Sie [Qualitätsmanagement für Lagerortprozesse](quality-management-for-warehouses-processes.md).</span><span class="sxs-lookup"><span data-stu-id="77224-121">If you've turned on this feature, see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
