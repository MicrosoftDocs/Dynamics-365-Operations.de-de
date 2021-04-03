---
title: " Finanzdimensionen für POS-Register erstellen und in Registern konfigurieren"
description: Diese Prozedur führt Sie Schritt für Schritt durch das Erstellen von Finanzdimensionen für Verkaufsstellen (POS)-Register, und zeigt, wie Finanzdimensionswerte für Register konfiguriert werden.
author: jashanno
manager: AnnBe
ms.date: 11/14/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4042fb9da0fe38de50ad7e0c8e64b98925ea1188
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5265958"
---
# <a name="create-financial-dimensions-for-pos-registers-and-configure-dimension-values-on-registers"></a><span data-ttu-id="e48e8-103"> Finanzdimensionen für POS-Register erstellen und in Registern konfigurieren</span><span class="sxs-lookup"><span data-stu-id="e48e8-103">Create financial dimensions for POS registers and configure dimension values on registers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e48e8-104">Diese Prozedur führt Sie Schritt für Schritt durch das Erstellen von Finanzdimensionen für Verkaufsstellen (POS)-Register, und zeigt, wie Finanzdimensionswerte für Register konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="e48e8-104">This procedure walks through creating financial dimensions for point of sale (POS) registers, and demonstrates how to configure financial dimension values on registers.</span></span> <span data-ttu-id="e48e8-105">Diese Prozedur umfasst keine anderen zugehörigen Schritte, wie Erstellen von Dimensionssätzen und Kontostrukturen.</span><span class="sxs-lookup"><span data-stu-id="e48e8-105">This procedure doesn't include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="e48e8-106">Diese Aufgaben werden in anderen Themen behandelt.</span><span class="sxs-lookup"><span data-stu-id="e48e8-106">Those tasks can be found in other topics.</span></span> <span data-ttu-id="e48e8-107">Für diese Erfassung wird das Demo-Unternehmen USRT verwendet.</span><span class="sxs-lookup"><span data-stu-id="e48e8-107">This recording uses USRT demo company.</span></span>

1. <span data-ttu-id="e48e8-108">Wechseln Sie zu Hauptbuch >; Kontenplan > Dimensionen > Finanzdimensionen.</span><span class="sxs-lookup"><span data-stu-id="e48e8-108">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="e48e8-109">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="e48e8-109">Click New.</span></span>
3. <span data-ttu-id="e48e8-110">Wählen Sie eine Option im Feld "Werte verwenden aus" aus.</span><span class="sxs-lookup"><span data-stu-id="e48e8-110">In the Use values from field, select an option.</span></span>
4. <span data-ttu-id="e48e8-111">Geben Sie im Feld "Dimensionsname" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="e48e8-111">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="e48e8-112">Klicken Sie auf Aktivieren.</span><span class="sxs-lookup"><span data-stu-id="e48e8-112">Click Activate.</span></span>
6. <span data-ttu-id="e48e8-113">Klicken Sie auf "Schließen".</span><span class="sxs-lookup"><span data-stu-id="e48e8-113">Click Close.</span></span>
7. <span data-ttu-id="e48e8-114">Klicken Sie auf Aktivieren.</span><span class="sxs-lookup"><span data-stu-id="e48e8-114">Click Activate.</span></span>
8. <span data-ttu-id="e48e8-115">Klicken Sie auf "Dimensionswerte".</span><span class="sxs-lookup"><span data-stu-id="e48e8-115">Click Dimension values.</span></span>
9. <span data-ttu-id="e48e8-116">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="e48e8-116">Close the page.</span></span>
10. <span data-ttu-id="e48e8-117">Klicken Sie auf Speichern.</span><span class="sxs-lookup"><span data-stu-id="e48e8-117">Click Save.</span></span>
11. <span data-ttu-id="e48e8-118">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="e48e8-118">Close the page.</span></span>
12. <span data-ttu-id="e48e8-119">Wechseln Sie zu Einzelhandel und Handel > Kanaleinstellungen > POS-Einstellungen > Register.</span><span class="sxs-lookup"><span data-stu-id="e48e8-119">Go to Retail and Commerce > Channel setup > POS setup > Registers.</span></span>
13. <span data-ttu-id="e48e8-120">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="e48e8-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="e48e8-121">Schalten Sie die Erweiterung des Abschnitts "Finanzdimensionen" ein/aus.</span><span class="sxs-lookup"><span data-stu-id="e48e8-121">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="e48e8-122">Klicken Sie auf Bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="e48e8-122">Click Edit.</span></span>
16. <span data-ttu-id="e48e8-123">Klicken Sie im Feld "Terminal" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="e48e8-123">In the Terminal field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="e48e8-124">Wählen Sie in der Liste den Dimensionswert für das Register aus, das aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="e48e8-124">In the list, find and select the dimension value for the register being updated.</span></span>
18. <span data-ttu-id="e48e8-125">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="e48e8-125">Click Save.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]