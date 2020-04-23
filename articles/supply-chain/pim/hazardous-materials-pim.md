---
title: Gefahrengüter
description: Dieses Thema bietet Informationen über Gefahrgutdokumente und Informationen, die in Ihrer Umgebung gespeichert sind.
author: lachlancashMS
manager: tfehr
ms.date: 01/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations, Retail
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: conradv
ms.search.validFrom: 2019-10-14
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5006f06d90ddcc314a51878e9e21337de7d493e7
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208460"
---
# <a name="hazardous-materials"></a><span data-ttu-id="ef416-103">Gefahrengüter</span><span class="sxs-lookup"><span data-stu-id="ef416-103">Hazardous materials</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ef416-104">Informationen zu Gefahrstoffen werden in der Produktinformationsverwaltung eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="ef416-104">Information about hazardous materials is set up in Product information management.</span></span> <span data-ttu-id="ef416-105">Dieses Modul bietet auch Dokumente, die über die Lagerverwaltung gedruckt werden können.</span><span class="sxs-lookup"><span data-stu-id="ef416-105">This module also provides documents that can be printed through warehouse management.</span></span>

<span data-ttu-id="ef416-106">Wenn Sie Materialien versenden, die als Gefahrgut eingestuft sind, müssen der Sendung zusätzliche Unterlagen beigefügt werden.</span><span class="sxs-lookup"><span data-stu-id="ef416-106">When you ship materials that are classified as dangerous goods, additional paperwork must be included with the shipments.</span></span> <span data-ttu-id="ef416-107">Mit der Gefahrstofffunktionalität können Kunden Klassifizierungsinformationen speichern und zuweisen, um Artikel freizugeben.</span><span class="sxs-lookup"><span data-stu-id="ef416-107">The hazardous materials functionality lets customers store classification information and relate it to release items.</span></span> <span data-ttu-id="ef416-108">Diese Informationen können dann zur Vorbereitung der Versanddokumentation verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ef416-108">This information can then be used to help prepare shipping documentation.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ef416-109">Zur Erleichterung der Verwaltung von Gefahrgutlieferungen ermöglicht Microsoft Dynamics 365 Supply Chain Management Ihnen, zusätzliche Referenzinformationen einzurichten, die sich auf Produkte beziehen.</span><span class="sxs-lookup"><span data-stu-id="ef416-109">To help manage shipments of dangerous goods, Microsoft Dynamics 365 Supply Chain Management lets you set up additional reference information that is related to products.</span></span> <span data-ttu-id="ef416-110">Sie können auch zusätzliche Versanddokumente einrichten.</span><span class="sxs-lookup"><span data-stu-id="ef416-110">You can also set up additional shipment documents.</span></span> <span data-ttu-id="ef416-111">Das System entspricht jedoch nicht automatisch den Bestimmungen Ihres Landes oder Ihrer Region.</span><span class="sxs-lookup"><span data-stu-id="ef416-111">However, the system isn't automatically compliant with your country's or region's regulations.</span></span> <span data-ttu-id="ef416-112">Stattdessen kommt ein Tool zum Einsatz, das Ihr Programm insgesamt unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ef416-112">Instead, it's a tool that can help your overall program.</span></span>

<span data-ttu-id="ef416-113">Bevor Sie diese Funktionalität nutzen können, müssen Sie folgende Einstellungen vornehmen:</span><span class="sxs-lookup"><span data-stu-id="ef416-113">Before you can use this functionality, the following setup is required:</span></span>

- <span data-ttu-id="ef416-114">**Produktinformationsverwaltung:** Richten Sie Codes ein, die auf freigegebene Produkte angewendet werden können.</span><span class="sxs-lookup"><span data-stu-id="ef416-114">**Product information management:** Set up codes that can be applied to released products.</span></span>
- <span data-ttu-id="ef416-115">**Lagerortverwaltung:** Verwenden Sie zusätzliche Versanddokumente, um Versandinformationen auszudrucken.</span><span class="sxs-lookup"><span data-stu-id="ef416-115">**Warehouse management:** Use additional shipping documents to print shipment information.</span></span>

## <a name="product-information-management"></a><span data-ttu-id="ef416-116">Produktinformationsverwaltung</span><span class="sxs-lookup"><span data-stu-id="ef416-116">Product information management</span></span>

<span data-ttu-id="ef416-117">In der Produktinformationsverwaltung gibt es eine Reihe von Setup-Tabellen, in denen Sie die Referenzinformationen hinzufügen können, die in der Liste für Gefahrgüter für Straßen-, See- und Luftfracht enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="ef416-117">In Product information management, there is a range of setup tables where you can add the reference information that is provided in the dangerous goods lists for road, air, and sea freight.</span></span>

<span data-ttu-id="ef416-118">Nachfolgend einige der Bestimmungen, auf die oftmals verwiesen wird:</span><span class="sxs-lookup"><span data-stu-id="ef416-118">Here are some of the regulations that are often referenced:</span></span>

- <span data-ttu-id="ef416-119">**ADR** – Vorschriften, die sich auf die internationale Beförderung gefährlicher Güter auf dem Landweg beziehen</span><span class="sxs-lookup"><span data-stu-id="ef416-119">**ADR** – Regulations that are related to the international carriage of dangerous goods by road</span></span>
- <span data-ttu-id="ef416-120">**CFR 49** – Vorschriften der Vereinigten Staaten für die Beförderung gefährlicher Güter</span><span class="sxs-lookup"><span data-stu-id="ef416-120">**CFR 49** – Regulations in the United Sates for the carriage of dangerous goods</span></span>
- <span data-ttu-id="ef416-121">**IMDG** – Der IMDG-Code (International Marine Dangerous Goods)</span><span class="sxs-lookup"><span data-stu-id="ef416-121">**IMDG** – The International Marine Dangerous Goods (IMDG) code</span></span>
- <span data-ttu-id="ef416-122">**IATA** – Die Gefahrgutbestimmungen der International Air Transport Association (IATA)</span><span class="sxs-lookup"><span data-stu-id="ef416-122">**IATA** – The International Air Transport Association (IATA) dangerous goods regulations</span></span>

<span data-ttu-id="ef416-123">Jede dieser Bestimmungen enthält eine Gefahrgutliste mit Referenzcodes.</span><span class="sxs-lookup"><span data-stu-id="ef416-123">Each of these regulations has a dangerous goods list that includes reference codes.</span></span> <span data-ttu-id="ef416-124">Die Listen für die einzelnen Transporttypen werden in gemeinsamen internationalen Klassifikationen zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="ef416-124">The lists for each type of transport are combined on shared international classifications.</span></span> <span data-ttu-id="ef416-125">Supply Chain Management bietet eine Referenztabelle für die gemeinsam genutzten Codes in diesen Listen.</span><span class="sxs-lookup"><span data-stu-id="ef416-125">Supply Chain Management provides a reference table for the shared codes in those lists.</span></span> <span data-ttu-id="ef416-126">Jede Liste enthält auch eindeutig definierbare Codes.</span><span class="sxs-lookup"><span data-stu-id="ef416-126">Each list also has some unique codes that can be defined.</span></span>

<span data-ttu-id="ef416-127">Um mit der Konfiguration dieser Informationen zu beginnen, erstellen Sie eine Regelung, mit der Sie die Anfangsparameter konfigurieren können.</span><span class="sxs-lookup"><span data-stu-id="ef416-127">To start to configure this information, create a regulation that you can use to configure the initial parameters.</span></span>

## <a name="warehouse-management"></a><span data-ttu-id="ef416-128">Lagerortverwaltung</span><span class="sxs-lookup"><span data-stu-id="ef416-128">Warehouse management</span></span>

<span data-ttu-id="ef416-129">Wenn eine Lieferung vorbereitet ist, können mehrere neue Berichte gedruckt werden.</span><span class="sxs-lookup"><span data-stu-id="ef416-129">When a shipment is prepared, several new reports can be printed.</span></span> <span data-ttu-id="ef416-130">Für diese Berichte werden die Informationen verwendet, die Sie in der Produktinformationsverwaltung eingerichtet haben.</span><span class="sxs-lookup"><span data-stu-id="ef416-130">These reports use the information that you set up in Product information management.</span></span>
