---
title: Anzeigen von Belastungen für einen produzierten Artikel
description: Die konstanten Kosten eines produzierten Artikels beinhalten die Arbeitsgangrüstzeiten sowie die Komponenten mit einer konstanten Menge oder einem konstanten Schrottwert.
author: AndersGirke
manager: tfehr
ms.date: 04/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion, InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.custom: 274483
ms.assetid: 6f5b851b-c5a7-43ef-b380-0d316667c1ef
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: f8d7fd7488630d9d24d5d7dc31ea39a10385a290
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5235507"
---
# <a name="display-charges-for-a-manufactured-item"></a><span data-ttu-id="7fe9b-103">Anzeigen von Belastungen für einen produzierten Artikel</span><span class="sxs-lookup"><span data-stu-id="7fe9b-103">Display charges for a manufactured item</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7fe9b-104">Die konstanten Kosten eines produzierten Artikels beinhalten die Arbeitsgangrüstzeiten sowie die Komponenten mit einer konstanten Menge oder einem konstanten Schrottwert.</span><span class="sxs-lookup"><span data-stu-id="7fe9b-104">The constant costs of a manufactured item reflect the operation setup times and the components that have a constant quantity or a constant scrap amount.</span></span>

<span data-ttu-id="7fe9b-105">Der berechnete Betrag der Belastungen eines Artikels kann zusammen mit den Einheitenkosten des Artikels angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="7fe9b-105">The calculated amount of an item's charges can be displayed with the item's unit costs.</span></span> <span data-ttu-id="7fe9b-106">Manchmal werden die Belastungen jedoch auch als separate Felder angezeigt und nicht in die Einheitenkosten des Artikels einbezogen.</span><span class="sxs-lookup"><span data-stu-id="7fe9b-106">However, the charges are sometimes displayed as separate fields, and they are not included in the item's unit costs.</span></span> <span data-ttu-id="7fe9b-107">Werden die Belastungen als separate Felder angezeigt, enthält eines der Felder den Gesamtbetrag der Belastungen und ein anderes Feld die Losgröße für die Nachkalkulation, die zur Amortisierung des Betrags verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="7fe9b-107">When the charges appear as separate fields, one field displays the total amount of charges, and another field displays the costing lot size that is used to amortize the amount.</span></span> <span data-ttu-id="7fe9b-108">Die Artikelpreisseite, zum Beispiel zeigt die Belastungen als zwei separate Felder.</span><span class="sxs-lookup"><span data-stu-id="7fe9b-108">The Item price page, for example, displays the charges as two separate fields.</span></span> <span data-ttu-id="7fe9b-109">Die Seite Abgeschlossen zeigt dagegen die Gesamtkosten des Artikels pro Einheit und die amortisierten Kosten sind bereits in den Einheitenkosten enthalten.</span><span class="sxs-lookup"><span data-stu-id="7fe9b-109">However, the Complete page displays the item's total cost per unit, and the amortized costs are included in the unit costs.</span></span>

<span data-ttu-id="7fe9b-110">Die Belastungen für einen produzierten Artikel werden zum Zwecke der Standardkosten immer in die Einheitenkosten des Artikels einbezogen.</span><span class="sxs-lookup"><span data-stu-id="7fe9b-110">The charges for a manufactured item are always included in the item's unit cost for standard cost purposes.</span></span> <span data-ttu-id="7fe9b-111">Sie können optional auch in geplante Kosten einbezogen werden.</span><span class="sxs-lookup"><span data-stu-id="7fe9b-111">They can optionally be included for planned cost purposes.</span></span> <span data-ttu-id="7fe9b-112">Die Einbeziehung der Belastungen in die Kosten eines produzierten Artikels wird durch eine Richtlinie in der Nachkalkulationsversion erzwungen.</span><span class="sxs-lookup"><span data-stu-id="7fe9b-112">A policy in the costing version enforces the inclusion of charges in the cost of a manufactured item.</span></span> <span data-ttu-id="7fe9b-113">Durch die Aktivierung des Kostendatensatzes eines Artikels werden die Belastungen in den im Formular  angezeigten Basiskosteninformationen des Artikels aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7fe9b-113">When you activate an item's cost record, you update the charges for the item's base cost information, which is displayed in the Item price page.</span></span> <span data-ttu-id="7fe9b-114">Die Belastungen werden in zwei separaten Feldern angezeigt und nicht in die Einheitenkosten des Artikels einbezogen.</span><span class="sxs-lookup"><span data-stu-id="7fe9b-114">The charges are displayed as two separate fields, and they are not included in the item's unit cost.</span></span> <span data-ttu-id="7fe9b-115">Bei jeder Aktivierung werden die Grundkosteninformationen des Artikels aktualisiert. Dies gilt auch, wenn durch die Aktivierung unterschiedliche Standorte berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="7fe9b-115">Each activation updates the item's base cost information, even if the activation reflects different sites.</span></span> <span data-ttu-id="7fe9b-116">Aus diesem Grund dürfen die Grundkosteninformationen lediglich als Referenzinformationen betrachtet werden.</span><span class="sxs-lookup"><span data-stu-id="7fe9b-116">Therefore, you should view the base cost information as reference information.</span></span>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]