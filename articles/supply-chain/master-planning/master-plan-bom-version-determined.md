---
title: Stücklistenversion ermitteln
description: Wenn während der Bedarfsauflösung für einen Artikel ein Standard-Bestellvorschlagtyp zur Produktion festgelegt ist, sucht das Planungsmodul eine gültige Stücklistenversion auf Grundlage des Standorts.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMConsistOf, BOMDesigner, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2534
ms.assetid: a5b64301-a011-4469-afaf-e4c9164ef9c6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a90a257debe8f24e149ddca1738d8376b2124012
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966979"
---
# <a name="determine-the-bom-version"></a><span data-ttu-id="ae24d-103">Stücklistenversion ermitteln</span><span class="sxs-lookup"><span data-stu-id="ae24d-103">Determine the BOM version</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ae24d-104">Wenn während der Bedarfsauflösung für einen Artikel ein Standard-Bestellvorschlagtyp zur Produktion festgelegt ist, sucht das Planungsmodul eine gültige Stücklistenversion auf Grundlage des Standorts.</span><span class="sxs-lookup"><span data-stu-id="ae24d-104">During a demand explosion, if an item has a default order type of Production, the planning engine finds a valid BOM version based on the site.</span></span> 

<span data-ttu-id="ae24d-105">Der Standortgröße ist immer bekannt und in der Bedarfsbuchung angegeben.</span><span class="sxs-lookup"><span data-stu-id="ae24d-105">The site dimension is always known and is stated on the demand transaction.</span></span> <span data-ttu-id="ae24d-106">Der folgende Prozess wird verwendet, um die zu verwendende Stücklistenversion zu bestimmen:</span><span class="sxs-lookup"><span data-stu-id="ae24d-106">The following process is used to determine the BOM version to use:</span></span>

-   <span data-ttu-id="ae24d-107">Wenn eine Stücklistenversion für den Artikel am Bedarfsstandort festgelegt ist, wird die standortspezifische Stückliste verwendet.</span><span class="sxs-lookup"><span data-stu-id="ae24d-107">If there is a BOM version defined for the item at the demand site, the site-specific BOM is used.</span></span>
-   <span data-ttu-id="ae24d-108">Falls für einen Artikel am Bedarfsstandort keine standortspezifische Stücklistenversion festgelegt ist, wird eine allgemeine Stückliste verwendet.</span><span class="sxs-lookup"><span data-stu-id="ae24d-108">If there is no site-specific BOM version defined for an item at the demand site, a general BOM is used.</span></span> <span data-ttu-id="ae24d-109">Eine allgemeine Stückliste gibt keinen Standort an und gilt für mehrere Standorte.</span><span class="sxs-lookup"><span data-stu-id="ae24d-109">A general BOM does not state a site, and it is valid for multiple sites.</span></span> <span data-ttu-id="ae24d-110">Wenn eine allgemeine Stückliste vorhanden ist, wird sie verwendet.</span><span class="sxs-lookup"><span data-stu-id="ae24d-110">If there is a general BOM, it is used.</span></span>
-   <span data-ttu-id="ae24d-111">Falls es keine zu verwendende allgemeine Stücklistenversion gibt, wird die Bedarfsauflösung an diesem Punkt gestoppt.</span><span class="sxs-lookup"><span data-stu-id="ae24d-111">If there is no general BOM version to use, the demand explosion stops at this point.</span></span>

<span data-ttu-id="ae24d-112">Eine gültige Stücklistenversion, egal ob standortspezifisch oder allgemein, muss die erforderlichen Kriterien für Datum und Menge erfüllen.</span><span class="sxs-lookup"><span data-stu-id="ae24d-112">A valid BOM version, whether site-specific or general, must meet the required criteria for date and quantity.</span></span>





