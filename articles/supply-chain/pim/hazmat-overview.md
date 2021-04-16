---
title: Gefahrstoffübersicht
description: Dieses Thema bietet einen Überblick über Funktionen, die sich auf die Handhabung und Dokumentation gefährlicher Materialien während der Produktinformationsverwaltung und der Lagerverwaltung beziehen.
author: dasani-madipalli
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 15edf61cba03a57b9b4d2c939228fd064b797942
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829377"
---
# <a name="hazardous-materials-overview"></a><span data-ttu-id="f98ef-103">Gefahrstoffübersicht</span><span class="sxs-lookup"><span data-stu-id="f98ef-103">Hazardous materials overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f98ef-104">Um die Liefer- und Transportvorschriften einzuhalten, müssen Organisationen, die Materialien liefern, die als gefährliche Güter eingestuft sind, zusätzliche Papiere ihren Lieferungen beifügen.</span><span class="sxs-lookup"><span data-stu-id="f98ef-104">To remain compliant with shipping and transport regulations, organizations that ship materials that are classified as dangerous goods must include additional paperwork with their shipments.</span></span> <span data-ttu-id="f98ef-105">Mit der Gefahrstofffunktion können Kunden Informationen speichern, die sich auf zugelassene Artikel beziehen.</span><span class="sxs-lookup"><span data-stu-id="f98ef-105">The hazardous materials feature lets customers store information that is related to released items.</span></span> <span data-ttu-id="f98ef-106">Diese Informationen können dann zur Vorbereitung der Versanddokumentation verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f98ef-106">This information can then be used to help prepare shipping documentation.</span></span> <span data-ttu-id="f98ef-107">Eine Organisation, die gefährliche Güter versendet, muss über eigene Prozesse und Prozeduren zur Verwaltung des Lieferprozesses verfügen.</span><span class="sxs-lookup"><span data-stu-id="f98ef-107">An organization that ships dangerous goods must have its own processes and procedures for managing the shipping process.</span></span> <span data-ttu-id="f98ef-108">Microsoft Dynamics 365 Supply Chain Management ist nur ein Tool, mit dem Sie die erforderlichen Dokumente leichter erstellen können.</span><span class="sxs-lookup"><span data-stu-id="f98ef-108">Microsoft Dynamics 365 Supply Chain Management is just a tool that can help generate the required documents.</span></span>

<span data-ttu-id="f98ef-109">Das folgende Diagramm zeigt die Schritte, die zum Einrichten und Verwenden der Gefahrstofffunktion erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="f98ef-109">The following diagram illustrates the steps needed to set up and use the hazardous materials feature.</span></span>

<span data-ttu-id="f98ef-110">![Einrichtung und Verwendung der Gefahrstofffunktion](media/hazmat-overview.png "Einrichtung und Verwendung der Gefahrstofffunktion")</span><span class="sxs-lookup"><span data-stu-id="f98ef-110">![Setup and use of the hazardous materials feature](media/hazmat-overview.png "Setup and use of the hazardous materials feature")</span></span>

<span data-ttu-id="f98ef-111">Die Gefahrstofffunktion wird in der Produktinformationsverwaltung eingerichtet und bietet Dokumente, die über die Lagerverwaltung gedruckt werden können.</span><span class="sxs-lookup"><span data-stu-id="f98ef-111">The hazardous materials feature is set up in Product information management and provides documents that can be printed through Warehouse management.</span></span> <span data-ttu-id="f98ef-112">Daher sind diese Bereiche im Großen und Ganzen die beiden Hauptbereiche, in denen Sie die Funktionen dieser Funktion überprüfen, einrichten und verwenden:</span><span class="sxs-lookup"><span data-stu-id="f98ef-112">Therefore, broadly speaking, those areas are the two main areas where you will review, set up, and use this feature's functionality:</span></span>

- <span data-ttu-id="f98ef-113">**Produktinformationsverwaltung** – Richten Sie Codes ein, die auf ein freigegebenes Produkte angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="f98ef-113">**Product information management** – Set up the codes that will be applied to a released product.</span></span>
- <span data-ttu-id="f98ef-114">**Lagerverwaltung** – Arbeiten Sie mit zusätzlichen Lieferdokumenten, die für Lieferungen gedruckt werden.</span><span class="sxs-lookup"><span data-stu-id="f98ef-114">**Warehouse management** – Work with additional shipping documents that will be printed for shipments.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f98ef-115">Die Gefahrstoff-Funktionen in Supply Chain Management bieten eine Sammlung nützlicher Produktinformationsfelder und verknüpfte Funktionen an, mit denen Sie Informationen erfassen und auf sie verweisen können, die sich auf Ihre Gefahrengüter beziehen.</span><span class="sxs-lookup"><span data-stu-id="f98ef-115">The hazardous materials features in Supply Chain Management provide a collection of useful product information fields and related functionality that can help you record and reference information that is related to your hazardous products.</span></span> <span data-ttu-id="f98ef-116">Diese Funktionen können Ihnen auch beim Entwerfen und Drucken von Versanddokumenten helfen, die einige der gleichen Informationen zu gefährlichen Stoffen enthalten, die Sie versenden.</span><span class="sxs-lookup"><span data-stu-id="f98ef-116">These features can also help you design and print shipment documents that include some of the same information about any hazardous materials that you're shipping.</span></span> <span data-ttu-id="f98ef-117">Durch das System werden Sie jedoch nicht automatisch alle geltenden Bestimmungen in Ihrem Land oder Ihrer Region einhalten.</span><span class="sxs-lookup"><span data-stu-id="f98ef-117">However, the system won't automatically make you compliant with all applicable regulations in your country or region.</span></span> <span data-ttu-id="f98ef-118">Obwohl diese Tools Ihnen dabei helfen sollen, die gängigen Vorschriften einzuhalten, sind sie an sich weder ausreichend noch garantieren Sie deren vollständige Einhaltung.</span><span class="sxs-lookup"><span data-stu-id="f98ef-118">Although these tools are intended to help you comply with common regulations, they are neither sufficient in themselves nor guaranteed to be so.</span></span> <span data-ttu-id="f98ef-119">Ihre Organisation ist dafür verantwortlich, alle geltenden Vorschriften zu kennen und alle erforderlichen Schritte zu unternehmen, um diese einzuhalten.</span><span class="sxs-lookup"><span data-stu-id="f98ef-119">Your organization is responsible for being aware of all applicable regulations and for taking all necessary steps to comply with them.</span></span>

## <a name="product-information-management"></a><span data-ttu-id="f98ef-120">Produktinformationsverwaltung</span><span class="sxs-lookup"><span data-stu-id="f98ef-120">Product information management</span></span>

<span data-ttu-id="f98ef-121">Die Produktinformationsverwaltung bietet eine Reihe von Setup-Tabellen, in denen Sie die Referenzinformationen eingeben können für die verschiedenen Listen von Gefahrgütern für Straßen-, Luft- und Seefracht.</span><span class="sxs-lookup"><span data-stu-id="f98ef-121">Product information management provides a range of setup tables where you can enter reference information for the various dangerous goods lists for road, air, and sea freight.</span></span>

<span data-ttu-id="f98ef-122">Bei der Entwicklung dieser Funktionalität wurde auf die folgenden allgemeinen Vorschriften verwiesen:</span><span class="sxs-lookup"><span data-stu-id="f98ef-122">The following common regulations were referenced when this functionality was developed:</span></span>

- <span data-ttu-id="f98ef-123">**ADR** – Vorschriften, die sich auf die internationale Beförderung gefährlicher Güter auf dem Landweg beziehen</span><span class="sxs-lookup"><span data-stu-id="f98ef-123">**ADR** – Regulations that are related to the international carriage of dangerous goods by road</span></span>
- <span data-ttu-id="f98ef-124">**CFR 49** – Vorschriften der Vereinigten Staaten für die Beförderung gefährlicher Güter</span><span class="sxs-lookup"><span data-stu-id="f98ef-124">**CFR 49** – Regulations in the United Sates for the carriage of dangerous goods</span></span>
- <span data-ttu-id="f98ef-125">**IMDG** – Der IMDG-Code (International Marine Dangerous Goods)</span><span class="sxs-lookup"><span data-stu-id="f98ef-125">**IMDG** – The International Marine Dangerous Goods (IMDG) code</span></span>
- <span data-ttu-id="f98ef-126">**IATA** – Die Gefahrgutbestimmungen der International Air Transport Association (IATA)</span><span class="sxs-lookup"><span data-stu-id="f98ef-126">**IATA** – The International Air Transport Association (IATA) dangerous goods regulations</span></span>

<span data-ttu-id="f98ef-127">Jedes Regelwerk enthält standardisierte Listen gefährlicher Güter und Referenzcodes.</span><span class="sxs-lookup"><span data-stu-id="f98ef-127">Each set of regulations provides standardized lists of dangerous goods and reference codes.</span></span> <span data-ttu-id="f98ef-128">Supply Chain Management bietet daher eine Referenztabelle für die gemeinsam genutzten Codes in diesen Listen.</span><span class="sxs-lookup"><span data-stu-id="f98ef-128">Therefore, Supply Chain Management provides a reference table for the common codes on those lists.</span></span> <span data-ttu-id="f98ef-129">Jede Liste enthält auch eindeutig Codes, die Sie definieren können.</span><span class="sxs-lookup"><span data-stu-id="f98ef-129">Each list also has some unique codes that you can define.</span></span>

<span data-ttu-id="f98ef-130">Weitere Informationen zum Einrichten von Vorschriften und Werten für gefährliche Stoffe und zum Zuweisen der Werte zu relevanten Produkten finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="f98ef-130">For more information about how to set up regulations and values for hazardous materials, and how to assign the values to relevant products, see the following topics:</span></span>

- [<span data-ttu-id="f98ef-131">Gefahrengüter einrichten</span><span class="sxs-lookup"><span data-stu-id="f98ef-131">Set up hazardous materials</span></span>](hazmat-setup.md)
- [<span data-ttu-id="f98ef-132">Gefährliche Stoffe in Produkten, Bestellungen, Lieferungen und Ladungen</span><span class="sxs-lookup"><span data-stu-id="f98ef-132">Hazardous materials in products, orders, shipments, and loads</span></span>](hazmat-items.md)

## <a name="warehouse-management"></a><span data-ttu-id="f98ef-133">Lagerortverwaltung</span><span class="sxs-lookup"><span data-stu-id="f98ef-133">Warehouse management</span></span>

<span data-ttu-id="f98ef-134">Wenn Sie eine Lieferung in der Lagerverwaltung vorbereiten, können Sie mehrere neue Berichte drucken, die die Informationen verwenden, die Sie in der Produktinformationsverwaltung eingerichtet haben.</span><span class="sxs-lookup"><span data-stu-id="f98ef-134">When you prepare a shipment in Warehouse management, you will be able to print several new reports that use the information that you set up in Product information management.</span></span> <span data-ttu-id="f98ef-135">Weitere Informationen zu den verfügbaren Berichten und deren Verwendung finden Sie unter [Anfragen und Berichte zu Gefahrstoffen](hazmat-reports.md).</span><span class="sxs-lookup"><span data-stu-id="f98ef-135">For more information about the available reports and how to use them, see [Hazardous materials inquiries and reports](hazmat-reports.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]