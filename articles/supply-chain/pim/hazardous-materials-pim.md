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
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: kamaybac
ms.search.validFrom: 2019-10-14
ms.dyn365.ops.version: ''
ms.openlocfilehash: 156cd4ec3a1d1a08ba43832a93fde0d4f22ac2ed
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007640"
---
# <a name="hazardous-materials"></a><span data-ttu-id="054b1-103">Gefahrengüter</span><span class="sxs-lookup"><span data-stu-id="054b1-103">Hazardous materials</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="054b1-104">Informationen zu Gefahrstoffen werden in der Produktinformationsverwaltung eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="054b1-104">Information about hazardous materials is set up in Product information management.</span></span> <span data-ttu-id="054b1-105">Dieses Modul bietet auch Dokumente, die über die Lagerverwaltung gedruckt werden können.</span><span class="sxs-lookup"><span data-stu-id="054b1-105">This module also provides documents that can be printed through warehouse management.</span></span>

<span data-ttu-id="054b1-106">Wenn Sie Materialien versenden, die als Gefahrgut eingestuft sind, müssen der Sendung zusätzliche Unterlagen beigefügt werden.</span><span class="sxs-lookup"><span data-stu-id="054b1-106">When you ship materials that are classified as dangerous goods, additional paperwork must be included with the shipments.</span></span> <span data-ttu-id="054b1-107">Mit der Gefahrstofffunktionalität können Kunden Klassifizierungsinformationen speichern und zuweisen, um Artikel freizugeben.</span><span class="sxs-lookup"><span data-stu-id="054b1-107">The hazardous materials functionality lets customers store classification information and relate it to release items.</span></span> <span data-ttu-id="054b1-108">Diese Informationen können dann zur Vorbereitung der Versanddokumentation verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="054b1-108">This information can then be used to help prepare shipping documentation.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="054b1-109">Die Gefahrstoff-Funktionen in Microsoft Dynamics 365 Supply Chain Management bieten eine Sammlung nützlicher Produktinformationsfelder und verknüpfte Funktionen an, mit denen Sie Informationen erfassen und auf sie verweisen können, die sich auf Ihre Gefahrengüter beziehen.</span><span class="sxs-lookup"><span data-stu-id="054b1-109">The hazardous materials features in Microsoft Dynamics 365 Supply Chain Management provide a collection of useful product information fields and related functionality that can help you record and reference information that is related to your hazardous products.</span></span> <span data-ttu-id="054b1-110">Diese Funktionen können Ihnen auch beim Entwerfen und Drucken von Versanddokumenten helfen, die einige der gleichen Informationen zu gefährlichen Stoffen enthalten, die Sie versenden.</span><span class="sxs-lookup"><span data-stu-id="054b1-110">These features can also help you design and print shipment documents that include some of the same information about any hazardous materials that you're shipping.</span></span> <span data-ttu-id="054b1-111">Durch das System werden Sie jedoch nicht automatisch alle geltenden Bestimmungen in Ihrem Land oder Ihrer Region einhalten.</span><span class="sxs-lookup"><span data-stu-id="054b1-111">However, the system won't automatically make you compliant with all applicable regulations in your country or region.</span></span> <span data-ttu-id="054b1-112">Obwohl diese Tools Ihnen dabei helfen sollen, die gängigen Vorschriften einzuhalten, sind sie an sich weder ausreichend noch garantieren Sie deren vollständige Einhaltung.</span><span class="sxs-lookup"><span data-stu-id="054b1-112">Although these tools are intended to help you comply with common regulations, they are neither sufficient in themselves nor guaranteed to be so.</span></span> <span data-ttu-id="054b1-113">Ihre Organisation ist dafür verantwortlich, alle geltenden Vorschriften zu kennen und alle erforderlichen Schritte zu unternehmen, um diese einzuhalten.</span><span class="sxs-lookup"><span data-stu-id="054b1-113">Your organization is responsible for being aware of all applicable regulations and for taking all necessary steps to comply with them.</span></span>

<span data-ttu-id="054b1-114">Bevor Sie diese Funktionalität nutzen können, müssen Sie folgende Einstellungen vornehmen:</span><span class="sxs-lookup"><span data-stu-id="054b1-114">Before you can use this functionality, the following setup is required:</span></span>

- <span data-ttu-id="054b1-115">**Produktinformationsverwaltung:** Richten Sie Codes ein, die auf freigegebene Produkte angewendet werden können.</span><span class="sxs-lookup"><span data-stu-id="054b1-115">**Product information management:** Set up codes that can be applied to released products.</span></span>
- <span data-ttu-id="054b1-116">**Lagerortverwaltung:** Verwenden Sie zusätzliche Versanddokumente, um Versandinformationen auszudrucken.</span><span class="sxs-lookup"><span data-stu-id="054b1-116">**Warehouse management:** Use additional shipping documents to print shipment information.</span></span>

## <a name="product-information-management"></a><span data-ttu-id="054b1-117">Produktinformationsverwaltung</span><span class="sxs-lookup"><span data-stu-id="054b1-117">Product information management</span></span>

<span data-ttu-id="054b1-118">In der Produktinformationsverwaltung gibt es eine Reihe von Setup-Tabellen, in denen Sie die Referenzinformationen hinzufügen können, die in der Liste für Gefahrgüter für Straßen-, See- und Luftfracht enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="054b1-118">In Product information management, there is a range of setup tables where you can add the reference information that is provided in the dangerous goods lists for road, air, and sea freight.</span></span>

<span data-ttu-id="054b1-119">Nachfolgend einige der Bestimmungen, auf die oftmals verwiesen wird:</span><span class="sxs-lookup"><span data-stu-id="054b1-119">Here are some of the regulations that are often referenced:</span></span>

- <span data-ttu-id="054b1-120">**ADR** – Vorschriften, die sich auf die internationale Beförderung gefährlicher Güter auf dem Landweg beziehen</span><span class="sxs-lookup"><span data-stu-id="054b1-120">**ADR** – Regulations that are related to the international carriage of dangerous goods by road</span></span>
- <span data-ttu-id="054b1-121">**CFR 49** – Vorschriften der Vereinigten Staaten für die Beförderung gefährlicher Güter</span><span class="sxs-lookup"><span data-stu-id="054b1-121">**CFR 49** – Regulations in the United Sates for the carriage of dangerous goods</span></span>
- <span data-ttu-id="054b1-122">**IMDG** – Der IMDG-Code (International Marine Dangerous Goods)</span><span class="sxs-lookup"><span data-stu-id="054b1-122">**IMDG** – The International Marine Dangerous Goods (IMDG) code</span></span>
- <span data-ttu-id="054b1-123">**IATA** – Die Gefahrgutbestimmungen der International Air Transport Association (IATA)</span><span class="sxs-lookup"><span data-stu-id="054b1-123">**IATA** – The International Air Transport Association (IATA) dangerous goods regulations</span></span>

<span data-ttu-id="054b1-124">Jede dieser Bestimmungen enthält eine Gefahrgutliste mit Referenzcodes.</span><span class="sxs-lookup"><span data-stu-id="054b1-124">Each of these regulations has a dangerous goods list that includes reference codes.</span></span> <span data-ttu-id="054b1-125">Die Listen für die einzelnen Transporttypen werden in gemeinsamen internationalen Klassifikationen zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="054b1-125">The lists for each type of transport are combined on shared international classifications.</span></span> <span data-ttu-id="054b1-126">Supply Chain Management bietet eine Referenztabelle für die gemeinsam genutzten Codes in diesen Listen.</span><span class="sxs-lookup"><span data-stu-id="054b1-126">Supply Chain Management provides a reference table for the shared codes in those lists.</span></span> <span data-ttu-id="054b1-127">Jede Liste enthält auch eindeutig definierbare Codes.</span><span class="sxs-lookup"><span data-stu-id="054b1-127">Each list also has some unique codes that can be defined.</span></span>

<span data-ttu-id="054b1-128">Um mit der Konfiguration dieser Informationen zu beginnen, erstellen Sie eine Regelung, mit der Sie die Anfangsparameter konfigurieren können.</span><span class="sxs-lookup"><span data-stu-id="054b1-128">To start to configure this information, create a regulation that you can use to configure the initial parameters.</span></span>

## <a name="warehouse-management"></a><span data-ttu-id="054b1-129">Lagerortverwaltung</span><span class="sxs-lookup"><span data-stu-id="054b1-129">Warehouse management</span></span>

<span data-ttu-id="054b1-130">Wenn eine Lieferung vorbereitet ist, können mehrere neue Berichte gedruckt werden.</span><span class="sxs-lookup"><span data-stu-id="054b1-130">When a shipment is prepared, several new reports can be printed.</span></span> <span data-ttu-id="054b1-131">Für diese Berichte werden die Informationen verwendet, die Sie in der Produktinformationsverwaltung eingerichtet haben.</span><span class="sxs-lookup"><span data-stu-id="054b1-131">These reports use the information that you set up in Product information management.</span></span>
