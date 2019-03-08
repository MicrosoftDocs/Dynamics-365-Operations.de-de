---
title: Strichcodes einrichten
description: Dieser Artikel beschreibt, wie Sie die Strichcodes in Microsoft Dynamics 365 for Retail verwenden.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailBarcodeMaskCharacter, RetailBarcodeMaskSetup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15971
ms.assetid: 6b4b2ac2-0344-41aa-8818-62c30017d5ac
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 15d12abe32d3f5a47348016c67a4fb02d0a5d8e3
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "347352"
---
# <a name="set-up-bar-codes"></a><span data-ttu-id="35cfb-103">Strichcodes einrichten</span><span class="sxs-lookup"><span data-stu-id="35cfb-103">Set up bar codes</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="35cfb-104">Dieser Artikel beschreibt, wie Sie die Strichcodes in Microsoft Dynamics 365 for Retail verwenden.</span><span class="sxs-lookup"><span data-stu-id="35cfb-104">This article describes how to use bar codes in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="35cfb-105">Sie können mithilfe von Strichcodes Produkte erwerben und verkaufen, Produktvarianten nachverfolgen und Debitoren und Mitarbeiter einrichten.</span><span class="sxs-lookup"><span data-stu-id="35cfb-105">You can use bar codes to purchase and sell products, track product variants, and set up customers and employees.</span></span> <span data-ttu-id="35cfb-106">Sie können außerdem Strichcodes verwenden, um Coupons, Geschenkkarten und Gutschriften auszustellen und zu indossieren.</span><span class="sxs-lookup"><span data-stu-id="35cfb-106">You can also use bar codes to issue and endorse coupons, gift cards, and credit memos.</span></span> <span data-ttu-id="35cfb-107">Sie können Einzelhandelsprodukte entweder mit standardmäßigen Strichcodes oder mit benutzerdefinierten, firmeninternen Strichcodes einrichten.</span><span class="sxs-lookup"><span data-stu-id="35cfb-107">You can set up retail products so that they have standard bar codes or custom, in-house bar codes.</span></span> <span data-ttu-id="35cfb-108">Produkte können mehrere Strichcodes aufweisen.</span><span class="sxs-lookup"><span data-stu-id="35cfb-108">Products can have more than one bar code.</span></span> <span data-ttu-id="35cfb-109">Beispielsweise könnte ein Produkt mehrere Strichcodes haben, wenn es von verschiedenen Herstellern stammt oder wenn es über Varianten verfügt, hinsichtlich Größe, Stil oder Farbe.</span><span class="sxs-lookup"><span data-stu-id="35cfb-109">For example, a product might have multiple bar codes if it comes from various manufacturers, or if it has variants that are based on size, style, or color.</span></span> <span data-ttu-id="35cfb-110">Strichcodes können das Gewicht oder den Preis des Produkts enthalten.</span><span class="sxs-lookup"><span data-stu-id="35cfb-110">Bar codes can include the weight or price of the product.</span></span> <span data-ttu-id="35cfb-111">Strichcodemasken sind Vorlagen, die verwendet werden, um Strichcodes zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="35cfb-111">Bar code masks are templates that are used to create bar codes.</span></span>

> [!NOTE]
> <span data-ttu-id="35cfb-112">Wenn Sie einen eindeutigen Strichcodes für jede Variantenkombination zuweisen, können Sie den Strichcode am Register scannen und vom Programm feststellen lassen, welche Variante des Produkts verkauft wird.</span><span class="sxs-lookup"><span data-stu-id="35cfb-112">If you assign a unique bar code to each variant combination, you can scan the bar code at the register and let the program determine which variant of the product is being sold.</span></span> <span data-ttu-id="35cfb-113">Sie können außerdem Statistiken zu Verkäufen nach Varianten sammeln und anzeigen.</span><span class="sxs-lookup"><span data-stu-id="35cfb-113">You can also collect and view statistics about sales by variant.</span></span> <span data-ttu-id="35cfb-114">Jede Größen-, Farb- und Stilgruppe kann einer eindeutigen Nummer zugewiesen werden, durch die diese Gruppe im Strichcode gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="35cfb-114">Each size, color, and style group can be assigned a unique number that identifies that group in the bar code.</span></span> <span data-ttu-id="35cfb-115">Dynamics 365 for Retail verwendet die Strichcodemaske, um für jede Variantenkombination automatisch Strichcodes zu generieren.</span><span class="sxs-lookup"><span data-stu-id="35cfb-115">Dynamics 365 for Retail uses the bar code mask to automatically generate bar codes for each variant combination.</span></span> <span data-ttu-id="35cfb-116">Diese Funktion kann hilfreich sein, wenn es viele Größen, Farben und Stile gibt, da die Anzahl der Kombinationen mit jedem zusätzlichen Variantencode erheblich zunimmt.</span><span class="sxs-lookup"><span data-stu-id="35cfb-116">This functionality can be useful if there are many sizes, colors, and styles, because the number of combinations increases significantly as each variant code is added.</span></span> <span data-ttu-id="35cfb-117">Wird diese Funktion nicht verwendet, müssen die Strichcodes manuell jeder Kombination zugewiesen werden, die eine Produktvariante darstellt.</span><span class="sxs-lookup"><span data-stu-id="35cfb-117">If this functionality isn't used, bar codes must be manually assigned to each combination that represents a product variant.</span></span>

<span data-ttu-id="35cfb-118">Sie können Strichcodes manuell oder automatisch erstellen.</span><span class="sxs-lookup"><span data-stu-id="35cfb-118">You can create bar codes manually or automatically.</span></span> <span data-ttu-id="35cfb-119">Um Strichcodes zu erstellen, schließen Sie die folgenden Aufgaben im Auftrag ab, in dem sie aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="35cfb-119">To create bar codes, complete the following tasks in the order in which they are listed.</span></span>

1. <span data-ttu-id="35cfb-120">[Einrichten von Strichcode-Maskenzeichen](set-up-bar-code-masks.md).</span><span class="sxs-lookup"><span data-stu-id="35cfb-120">[Set up bar code mask characters](set-up-bar-code-masks.md).</span></span>
2. <span data-ttu-id="35cfb-121">[Einrichten von Strichcodemasken](set-up-bar-code-masks.md).</span><span class="sxs-lookup"><span data-stu-id="35cfb-121">[Set up bar code masks](set-up-bar-code-masks.md).</span></span>
3. <span data-ttu-id="35cfb-122">Konfigurieren Sie Strichcodeeinstellungen.</span><span class="sxs-lookup"><span data-stu-id="35cfb-122">Configure bar code setups.</span></span>
4. <span data-ttu-id="35cfb-123">Erstellen Sie Strichcodes für Produkte.</span><span class="sxs-lookup"><span data-stu-id="35cfb-123">Create bar codes for products.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="35cfb-124">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="35cfb-124">Additional resources</span></span>

[<span data-ttu-id="35cfb-125">Strichcodemasken einrichten</span><span class="sxs-lookup"><span data-stu-id="35cfb-125">Set up bar code masks</span></span>](set-up-bar-code-masks.md)
