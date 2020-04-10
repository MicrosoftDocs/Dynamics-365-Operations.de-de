---
title: Finanzdimensionen für Einzelhandelskanäle erstellen und Dimensionswerte in Geschäften konfigurieren
description: Diese Prozedur führt Sie Schritt für Schritt durch das Erstellen einer Commerce-Kanalfinanzdimension mit Dimensionswerten und Schritten zum Konfigurieren von Finanzdimensionswerten für Einzelhandelsgeschäfte.
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ea36732023092f714b3a783d98b512c0fea7dade
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141406"
---
# <a name="create-financial-dimensions-for-retail-channels-and-configure-dimension-values-on-stores"></a><span data-ttu-id="85e41-103">Finanzdimensionen für Einzelhandelskanäle erstellen und Dimensionswerte in Geschäften konfigurieren</span><span class="sxs-lookup"><span data-stu-id="85e41-103">Create financial dimensions for retail channels and configure dimension values on stores</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="85e41-104">Diese Prozedur führt Sie Schritt für Schritt durch das Erstellen einer Commerce-Kanalfinanzdimension mit Dimensionswerten und Schritten zum Konfigurieren von Finanzdimensionswerten für Einzelhandelsgeschäfte.</span><span class="sxs-lookup"><span data-stu-id="85e41-104">This procedure walks through creating a commerce channel financial dimension with dimension values and steps to configure financial dimension values on stores.</span></span> <span data-ttu-id="85e41-105">Das Thema umfasst keine anderen zugehörigen Schritte, wie Erstellen von Dimensionssätzen und Kontostrukturen.</span><span class="sxs-lookup"><span data-stu-id="85e41-105">The topic does not include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="85e41-106">Für diese Prozedur wird das Demo-Datenunternehmen USRT verwendet.</span><span class="sxs-lookup"><span data-stu-id="85e41-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="85e41-107">Wechseln Sie zu Hauptbuch >; Kontenplan > Dimensionen > Finanzdimensionen.</span><span class="sxs-lookup"><span data-stu-id="85e41-107">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="85e41-108">Klicken Sie auf Neu.</span><span class="sxs-lookup"><span data-stu-id="85e41-108">Click New.</span></span>
3. <span data-ttu-id="85e41-109">Wählen Sie im Feld „Werte verwenden aus“ die Option „Commerce-Kanäle“ aus.</span><span class="sxs-lookup"><span data-stu-id="85e41-109">In the Use values from field, select 'Commerce channels'.</span></span>
4. <span data-ttu-id="85e41-110">Geben Sie im Feld "Dimensionsname" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="85e41-110">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="85e41-111">Klicken Sie auf Aktivieren.</span><span class="sxs-lookup"><span data-stu-id="85e41-111">Click Activate.</span></span>
6. <span data-ttu-id="85e41-112">Klicken Sie auf "Schließen".</span><span class="sxs-lookup"><span data-stu-id="85e41-112">Click Close.</span></span>
7. <span data-ttu-id="85e41-113">Klicken Sie auf Aktivieren.</span><span class="sxs-lookup"><span data-stu-id="85e41-113">Click Activate.</span></span>
8. <span data-ttu-id="85e41-114">Klicken Sie auf "Dimensionswerte".</span><span class="sxs-lookup"><span data-stu-id="85e41-114">Click Dimension values.</span></span>
9. <span data-ttu-id="85e41-115">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="85e41-115">Close the page.</span></span>
10. <span data-ttu-id="85e41-116">Klicken Sie auf Speichern.</span><span class="sxs-lookup"><span data-stu-id="85e41-116">Click Save.</span></span>
11. <span data-ttu-id="85e41-117">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="85e41-117">Close the page.</span></span>
12. <span data-ttu-id="85e41-118">Navigieren Sie zu Einzelhandel und Commerce > Kanäle > Geschäfte > Alle Einzelhandelsgeschäfte.</span><span class="sxs-lookup"><span data-stu-id="85e41-118">Go to Retail and Commerce > Channels > Stores > All stores.</span></span>
13. <span data-ttu-id="85e41-119">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="85e41-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="85e41-120">Schalten Sie die Erweiterung des Abschnitts "Finanzdimensionen" ein/aus.</span><span class="sxs-lookup"><span data-stu-id="85e41-120">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="85e41-121">Klicken Sie auf Bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="85e41-121">Click Edit.</span></span>
16. <span data-ttu-id="85e41-122">Klicken Sie im Feld Commerce-Kanal auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="85e41-122">In the Commerce channel field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="85e41-123">Wählen Sie in der Liste den Dimensionswert für den Shop aus, der aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="85e41-123">In the list, find and select the dimension value for the store being updated.</span></span>
18. <span data-ttu-id="85e41-124">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="85e41-124">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="85e41-125">Klicken Sie im Feld "Kostenstelle" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="85e41-125">In the CostCenter field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="85e41-126">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="85e41-126">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="85e41-127">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="85e41-127">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="85e41-128">Klicken Sie im Feld "Abteilung" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="85e41-128">In the Department field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="85e41-129">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="85e41-129">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="85e41-130">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="85e41-130">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="85e41-131">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="85e41-131">Click Save.</span></span>

