---
title: Callcenterkataloge
description: "Dieser Artikel beschreibt die spezifische Funktionalität für Callcenters für Kataloge in Microsoft Dynamics 365 for Retail."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailMCRChannelDetailPage, RetailCatalogDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 99f66e975cf5875f357af095ead66529b9784eff
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---

# <a name="call-center-catalogs"></a><span data-ttu-id="663fb-103">Callcenterkataloge</span><span class="sxs-lookup"><span data-stu-id="663fb-103">Call center catalogs</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="663fb-104">Dieser Artikel beschreibt die spezifische Funktionalität für Callcenters für Kataloge in Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="663fb-104">This article describes the call center–specific functionality for catalogs in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="663fb-105">In einem Callcenter können Sie Einzelhandelsproduktkataloge verwenden, um die Produkte zu identifizieren, die Sie Kunden anbieten möchten.</span><span class="sxs-lookup"><span data-stu-id="663fb-105">In a call center, you can use product catalogs to identify the products that you want to offer to customers.</span></span> <span data-ttu-id="663fb-106">Callcenter verwenden in der Regel gedruckte Kataloge.</span><span class="sxs-lookup"><span data-stu-id="663fb-106">Call centers typically use printed catalogs.</span></span> <span data-ttu-id="663fb-107">Der Entwurf und die Produktion eines gedruckten Katalogs wird außerhalb von Microsoft Dynamics 365 for Retail behandelt.</span><span class="sxs-lookup"><span data-stu-id="663fb-107">The design and production of a printed catalog is handled outside Dynamics 365 for Retail.</span></span> <span data-ttu-id="663fb-108">Sie können jedoch ein digitales Formular eines Katalogs erstellen und speichern, indem Sie die gleichen Seiten verwenden, die Sie verwenden, um Online-Einzelhandelskataloge einzurichten.</span><span class="sxs-lookup"><span data-stu-id="663fb-108">However, you can create and store a digital form of a catalog by using the same pages that you use to set up online retail catalogs.</span></span> <span data-ttu-id="663fb-109">Bevor Sie einen Katalog erstellen können, müssen Sie Sortimente einrichten und die Sortimente einem Callcenter zuweisen.</span><span class="sxs-lookup"><span data-stu-id="663fb-109">Before you can create a catalog, you must set up product assortments and assign the assortments to a call center.</span></span> <span data-ttu-id="663fb-110">Anschließend fügen Sie Produkte dem Katalog hinzu, indem Sie Produkte aus diesen Sortiment auswählen.</span><span class="sxs-lookup"><span data-stu-id="663fb-110">You then add products to the catalog by selecting products from these assortments.</span></span> <span data-ttu-id="663fb-111">Nachdem Produkte dem Katalog hinzugefügt wurden und der Katalog abgeschlossen ist, müssen Sie den Katalog überprüfen, ob die Daten zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="663fb-111">After products have been added to the catalog, and the catalog is complete, you must validate the catalog to verify the data.</span></span> <span data-ttu-id="663fb-112">Übermitteln Sie dann den Katalog zur Prüfung und Genehmigung.</span><span class="sxs-lookup"><span data-stu-id="663fb-112">You must then submit the catalog for review and approval.</span></span> <span data-ttu-id="663fb-113">Nachdem der Katalog genehmigt wurde, kann er veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="663fb-113">After the catalog is approved, it can be published.</span></span> <span data-ttu-id="663fb-114">Wenn ein Callcenterkatalog erstellt wird, können Sie eine Momentaufnahme der Katalogdaten zum Zeitpunkt erstellen, an dem der Katalog veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="663fb-114">When a call center catalog is created, you can take a snapshot of the catalog data at the time that the catalog is published.</span></span> <span data-ttu-id="663fb-115">Mit dieser Momentaufnahmefunktionen können Sie auf eine bestimmte Version des Katalogs zugreifen, auch wenn der Katalog später geändert und aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="663fb-115">This snapshot functionality lets you access a particular version of the catalog even if the catalog is later changed and updated.</span></span> <span data-ttu-id="663fb-116">Callcenterkataloge können auch eingerichtet werden, um die folgenden optionalen Funktionen einzubeziehen:</span><span class="sxs-lookup"><span data-stu-id="663fb-116">Call center catalogs can also be set up to include the following optional features:</span></span>

-   <span data-ttu-id="663fb-117">**Quellcodes** – Quellcodes, die verwendet werden, um die Debitorenreaktion auf bestimmte Katalogmailings zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="663fb-117">**Source codes** – Source codes are used to track the customer response to specific catalog mailings.</span></span>
-   <span data-ttu-id="663fb-118">**Kostenlose Produkte** – Produkte, die in einem Kundenauftrag ohne zusätzliche Gebühr enthalten sein können.</span><span class="sxs-lookup"><span data-stu-id="663fb-118">**Free products** – Products can be included in a customer's order at no additional charge.</span></span> <span data-ttu-id="663fb-119">Diese Produkte werden dem Auftrag automatisch hinzugefügt, wenn der Quellcode für den Katalog in den Auftrag eingegeben wird.</span><span class="sxs-lookup"><span data-stu-id="663fb-119">These products are automatically added to an order when the source code for the catalog is entered into the order.</span></span>
-   <span data-ttu-id="663fb-120">**Skripts** – Skripts sind Texte, die eine Callcenterarbeitskraft einem Debitor vorliest, wenn ein Auftrag erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="663fb-120">**Scripts** – Scripts are texts that a call center worker reads to a customer when a sales order is being created.</span></span> <span data-ttu-id="663fb-121">Skripts können Grüße oder Einkaufvorschläge enthalten.</span><span class="sxs-lookup"><span data-stu-id="663fb-121">Scripts can include greetings or purchase suggestions.</span></span>
-   <span data-ttu-id="663fb-122">**Seitenlayout** – Ein Seitenlayout zeichnet die Seitenposition von Produkten im gedruckten Katalog auf.</span><span class="sxs-lookup"><span data-stu-id="663fb-122">**Page layout** – A page layout captures the page position of products in the printed catalog.</span></span> <span data-ttu-id="663fb-123">Diese Informationen werden für den Katalogbereich-Analysebericht verwendet.</span><span class="sxs-lookup"><span data-stu-id="663fb-123">This information is used for the catalog area analysis report.</span></span>





