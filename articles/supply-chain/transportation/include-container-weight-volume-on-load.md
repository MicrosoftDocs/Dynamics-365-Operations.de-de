---
title: "Containergewicht und -volumen bei Auslastung einschließen"
description: In diesem Thema wird beschrieben, wie die Funktion zum Einbezug von Containergewicht und Volumen eingerichtet wird.
author: pjacobse
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TMSRateRouteWorkbench, TMSDriverLogListPage, TMSTransportationTender
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: adbaa379889d373d597b2f6882b78f82bd71ae57
ms.contentlocale: de-de
ms.lasthandoff: 08/07/2018

---

# <a name="include-container-weight-and-volume-on-load"></a><span data-ttu-id="e2a03-103">Containergewicht und -volumen bei Auslastung einschließen</span><span class="sxs-lookup"><span data-stu-id="e2a03-103">Include container weight and volume on load</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e2a03-104">Die Funktionen zum Einschließen des Containergewichts und -Volumens auf eine Auslastung geben eine Darstellung des Gesamtgewichts und des Volumens der Container und der Artikel, die auf einer Auslastung sind.</span><span class="sxs-lookup"><span data-stu-id="e2a03-104">The functionality for including the container weight and volume on a load gives a clear representation of the total weight and volume of containers and items that are going on a load.</span></span>

<span data-ttu-id="e2a03-105">Eine Auslastung enthält eine einzelne Lieferung oder mehrere Lieferungen und diese Lieferungen enthalten eindeutige Artikel, die zu einem einzelnen Auftrag oder mehreren Aufträgen gehören.</span><span class="sxs-lookup"><span data-stu-id="e2a03-105">A load contains a single shipment or multiple shipments, and these shipments contain distinct items that belong to a single sales order or multiple sales orders.</span></span> <span data-ttu-id="e2a03-106">Die Artikel werden innerhalb eines Containers gelagert und die Container werden auf eine Auslastung  geladen.</span><span class="sxs-lookup"><span data-stu-id="e2a03-106">The items are stored inside a container, and containers are loaded on a load.</span></span> <span data-ttu-id="e2a03-107">Artikel, die außerhalb eines Containers sind, können auch Teil einer Kapazität sein.</span><span class="sxs-lookup"><span data-stu-id="e2a03-107">Items that are outside a container can also be part of a load.</span></span> <span data-ttu-id="e2a03-108">Basierend auf diesen Bedingungen berechnet das System Werte für das Gewicht und das Volumen für die Auslastung, indem das Gewicht und das Volumen von Containern und Artikeln berücksichtigt wird.</span><span class="sxs-lookup"><span data-stu-id="e2a03-108">Based on these conditions, the system calculates values for the weight and volume on the load by considering the weight and volume of both containers and items.</span></span>

<span data-ttu-id="e2a03-109">Wenn die berechneten Werte nicht präzis sind, können Sie sie regulieren, indem Sie den Istwerten auf das Gewicht und das Volumen für die Last eingeben.</span><span class="sxs-lookup"><span data-stu-id="e2a03-109">If the calculated values aren’t precise, you can adjust them by entering the actual values for the weight and volume on the load.</span></span> <span data-ttu-id="e2a03-110">Die Werte für das Gewicht und das Volumen werden in den Transportverwaltungsprozessen verwendet.</span><span class="sxs-lookup"><span data-stu-id="e2a03-110">The values for the weight and volume are used in transportation management processes.</span></span> <span data-ttu-id="e2a03-111">Beispielsweise werden die Werte im Routenworkbench-Satz verwendet, wo sie den Satz und für in den Arbeitsplan definieren, und sie werden auch für Transportzahlungsmittel und Fahrereinchecken verwendet.</span><span class="sxs-lookup"><span data-stu-id="e2a03-111">For example, the values are used in the rate route workbench, where they help define the rate and route for loads, and they are also used for transportation tenders and driver check-in.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="e2a03-112">Wofür es angewendet wird</span><span class="sxs-lookup"><span data-stu-id="e2a03-112">Where it applies</span></span>

<span data-ttu-id="e2a03-113">Die Funktionen zum Einschließen des Containergewichts und -Volumens auf eine Auslastung gelten in den Transportverwaltungsprozessen, wie der Routenworkbench-Satz, die Transportzahlungsmitteln und Fahrer einchecken.</span><span class="sxs-lookup"><span data-stu-id="e2a03-113">The functionality for including the container weight and volume on a load applies in transportation management processes, such as the rate route workbench, transportation tenders, and driver check-in.</span></span>

## <a name="how-it-is-set-up"></a><span data-ttu-id="e2a03-114">Wie er installiert wird</span><span class="sxs-lookup"><span data-stu-id="e2a03-114">How it is set up</span></span>

<span data-ttu-id="e2a03-115">Die Anzahl an Containern, die für eine Auslastung berücksichtigt werden sollen, wird anhand des Gewichts und des Volumens der Container und auf dem Prozentsatz der Containers berechnet.</span><span class="sxs-lookup"><span data-stu-id="e2a03-115">The number of containers that should be considered for a load is calculated based on the weight and volume of the container, and on the percentage of the container is used.</span></span>

-   <span data-ttu-id="e2a03-116">Um das Gewicht und das Volumen für einen Container festzulegen, klicken Sie auf **Lagerortverwaltung** \> **Einstellungen** \> **Container** \> **Containertypen**.</span><span class="sxs-lookup"><span data-stu-id="e2a03-116">To set the weight and volume for a container, click **Warehouse management** \> **Setup** \> **Containers** \> **Container types**.</span></span>

-   <span data-ttu-id="e2a03-117">Um den Containernutzungsprozentsatz einzurichten, klicken Sie auf **Lagerortverwaltung** \> **Einstellungen** \> **Container** \> **Containergruppen** und geben einen Wert in das Feld **Containernutzungsprozentsatz** ein.</span><span class="sxs-lookup"><span data-stu-id="e2a03-117">To set the container utilization percentage, click **Warehouse management** \> **Setup** \> **Containers** \> **Container groups**, and then enter a value in the **Container utilization percentage** field.</span></span>

