---
title: Einzelhandelspreisberichte
description: Dieses Thema bietet einen Überblick über die Preisberichtfunktion, mit der Sie die bevorstehenden Preisänderungen für die sortierten Produkte anzeigen können.
author: shajain
manager: AnnBe
ms.date: 01/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2019-01-18
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: 6db6d1c6b6eb1d69b40fe75d97eeb71564986707
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "353056"
---
# <a name="retail-price-reports"></a><span data-ttu-id="0d645-103">Einzelhandelspreisberichte</span><span class="sxs-lookup"><span data-stu-id="0d645-103">Retail price reports</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]


<span data-ttu-id="0d645-104">Um ihren Kunden konkurrenzfähige Preise anbieten zu können, ändern die Einzelhändler oft die Preise der Produkte.</span><span class="sxs-lookup"><span data-stu-id="0d645-104">In order to provide competitive prices to their customers, retailers often change prices of products.</span></span> <span data-ttu-id="0d645-105">Shopleiter wollen die Möglichkeit haben, auf aktuelle oder bevorstehende Preisänderungen leicht zuzugreifen, so dass sie für die benötigten Ressourcen planen können, um die in den Regalen der Filialen angezeigten Preisschilder zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="0d645-105">Store managers want the ability to easily access recent or upcoming price changes so that they can plan for the required resources to update the price labels displayed on the store shelves.</span></span> <span data-ttu-id="0d645-106">Mit der Version 10.0 von Dynamics 365 for Retail kann ein Shopleiter den Bericht **Preis** öffnen, indem er zu **Alle Einzelhandelsgeschäfte \> Shop \> Preisbericht** navigiert und die aktualisierten Preise für die mit dem Shop verbundenen Produkte anzeigt.</span><span class="sxs-lookup"><span data-stu-id="0d645-106">With release 10.0 of Dynamics 365 for Retail, a store manager can open the **Price** report by navigating to **All retail stores \> Store \> Price report** and viewing the updated prices for the products associated to the store.</span></span> 

<span data-ttu-id="0d645-107">Um den Preisbericht zu aktivieren, muss der Parameter **Preisbericht für Einzelhandelsgeschäft aktivieren** aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="0d645-107">To enable the price report, the **Enable price report for Retail store** parameter must be turned on.</span></span> <span data-ttu-id="0d645-108">Dieser Parameter befindet sich auf der Registerkarte **Einzelhandelsparameter \> Rabatte \> Sonstige**. Wenn Sie die Seite **Preisbericht** öffnen, wird ein Dialogfeld mit verschiedenen Konfigurationen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0d645-108">This parameter is located on the **Retail parameters \> Discounts \> Miscellaneous** tab. Opening the **Price report** page displays a dialog box with various configurations.</span></span> <span data-ttu-id="0d645-109">Die verfügbaren Konfigurationen sind nachfolgend aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="0d645-109">The available configurations are listed below.</span></span>

| <span data-ttu-id="0d645-110">Variante</span><span class="sxs-lookup"><span data-stu-id="0d645-110">Configuration</span></span> | <span data-ttu-id="0d645-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0d645-111">Description</span></span> |
|---|---|
| <span data-ttu-id="0d645-112">Von Datum / Bis Datum</span><span class="sxs-lookup"><span data-stu-id="0d645-112">From date / To date</span></span>| <span data-ttu-id="0d645-113">Der Datumsbereich, für den der Preisbericht erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0d645-113">The date range for which the price report should be generated.</span></span> <span data-ttu-id="0d645-114">Die Dauer ist derzeit auf 7 Tage begrenzt.</span><span class="sxs-lookup"><span data-stu-id="0d645-114">The duration is currently limited to 7 days.</span></span> |
| <span data-ttu-id="0d645-115">Kanal</span><span class="sxs-lookup"><span data-stu-id="0d645-115">Channel</span></span>| <span data-ttu-id="0d645-116">Der Einzelhandelsshop, für den der Preisbericht erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0d645-116">The retail store for which the price report should be generated.</span></span> |
| <span data-ttu-id="0d645-117">Produkte mit verfügbarem Lagerbestand anzeigen</span><span class="sxs-lookup"><span data-stu-id="0d645-117">Display products with available inventory</span></span>| <span data-ttu-id="0d645-118">Wenn Sie dies auf **Ja** setzen, werden die Preise für nur die Produkte angezeigt, für die derzeit in einem Shop physischer Bestand vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="0d645-118">Setting this to **Yes** will show the prices for only those products which currently have physical inventory available in the store.</span></span> |
| <span data-ttu-id="0d645-119">Preise für Varianten anzeigen</span><span class="sxs-lookup"><span data-stu-id="0d645-119">Display prices for variants</span></span> | <span data-ttu-id="0d645-120">Wenn Sie dies auf **Ja** einstellen, werden die Preise der Varianten zusammen mit den Produktmastern angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0d645-120">Setting this to **Yes** will display the prices of the variants along with the product masters.</span></span> <span data-ttu-id="0d645-121">Dies sollte nur dann **Aktiviert** werden, wenn Sie variantenspezifische Preise haben, da die Anzahl der Zeilen sehr groß wird.</span><span class="sxs-lookup"><span data-stu-id="0d645-121">This should only be turned **On** if you have variant-specific prices, because the number of rows grows very large.</span></span> <span data-ttu-id="0d645-122">In künftigen Versionen werden wir die dimensionsbasierten Preise aktivieren, so dass der Shopleiter die Dimensionen auswählen kann, für die die Preise angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0d645-122">In future releases, we will enable the dimensions-based prices so that the store manager can choose the dimensions for which the prices should be displayed.</span></span> |
| <span data-ttu-id="0d645-123">Produkte mit Preisänderungen anzeigen</span><span class="sxs-lookup"><span data-stu-id="0d645-123">Display products with price changes</span></span> | <span data-ttu-id="0d645-124">Wenn Sie dies auf **Ja** einstellen, werden die Preise nur für die Daten angezeigt, bei denen der Preis geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="0d645-124">Setting this to **Yes** will display the prices for only those dates on which the price has been changed.</span></span> <span data-ttu-id="0d645-125">Der Preis für *einen Tag vor* dem ausgewählten **Von Datum** wird immer angezeigt, sodass der Shopleiter die Produkte, die die Preise für die gesamte gewählte Zeitspanne nicht geändert haben, leicht identifizieren kann und auch den aktuellen Preis einsehen kann.</span><span class="sxs-lookup"><span data-stu-id="0d645-125">The price for *one day before* the selected **From date** will always be displayed, so that the store manager can easily identity the products which have not changed prices for the entire selected duration, and can also view the current price.</span></span> |

<span data-ttu-id="0d645-126">Nach der Erstellung des Berichts kann die Excel-Datei für zusätzliche Filterzwecke heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="0d645-126">After the report is generated, the Excel file can be downloaded for any additional filtering needs.</span></span> <span data-ttu-id="0d645-127">Der Preisbericht kann auch verwendet werden, um die historischen Preise von Produkten für vergangene Termine zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="0d645-127">The price report can also be used to check the historical prices of products for past dates.</span></span>