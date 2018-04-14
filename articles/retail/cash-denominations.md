---
title: "Konfigurieren Sie Bargeldnennwerte für POS"
description: "Bargeldnennwerte für Banknoten und Münzen können Backoffice definiert werde, um von den Kassierern, von den Vertriebsmitarbeitern und von Managern in Ihrem Unternehmen in POS verwendet zu werden."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailStoreTable, RetailStoreCashDeclarationTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 4a7d80783368b6b39d48f80a3329d4053169c464
ms.contentlocale: de-de
ms.lasthandoff: 04/13/2018

---

# <a name="configure-cash-denominations-for-pos"></a><span data-ttu-id="90277-103">Konfigurieren Sie Bargeldnennwerte für POS</span><span class="sxs-lookup"><span data-stu-id="90277-103">Configure cash denominations for POS</span></span>

[!INCLUDE [banner](includes/banner.md)]

<span data-ttu-id="90277-104">Bargeldnennwerte für Banknoten und Münzen können Backoffice definiert werde, um von den Kassierern, von den Vertriebsmitarbeitern und von Managern in Ihrem Unternehmen in POS verwendet zu werden.</span><span class="sxs-lookup"><span data-stu-id="90277-104">Cash denominations for notes and coins can be defined in the back office to be used by cashiers, sales associates, and managers at the store from within the POS.</span></span> <span data-ttu-id="90277-105">Diese Nennwerte können verwendet werden, um bei der Bargeld-Inventur für die Berechnung des Tagesumsatzes oder für ein schelles Produktangebot verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="90277-105">These denominations can be used to aid in counting cash for end of day tender declarations or for quickly tendering a sale.</span></span>

## <a name="define-denominations"></a><span data-ttu-id="90277-106">Nennwerte definieren</span><span class="sxs-lookup"><span data-stu-id="90277-106">Define denominations</span></span>
<span data-ttu-id="90277-107">Die Nennwerte werden pro Shop auf der Seite **Einstellungen** > **Bargelddeklarationsoption von der Shopeigenschaft** eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="90277-107">The denominations are set up per store on the **Set up** > **Cash declaration option from the store property** page.</span></span> 

![Bargeld-Denominationen](./media/image1-denomination.png)

<span data-ttu-id="90277-109">Nennwerte definieren:</span><span class="sxs-lookup"><span data-stu-id="90277-109">To define a denomination:</span></span>
1. <span data-ttu-id="90277-110">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="90277-110">Click **New**.</span></span>
1. <span data-ttu-id="90277-111">Geben Sie den Typ an (Banknote oder Münzen).</span><span class="sxs-lookup"><span data-stu-id="90277-111">Specify the type (coin or note).</span></span>
1. <span data-ttu-id="90277-112">Geben Sie den Betrag ein (Wert).</span><span class="sxs-lookup"><span data-stu-id="90277-112">Specify the amount (value).</span></span>

![Bargeld-Denominationen](./media/image2-denomination.png)

## <a name="configure-the-functionality-profile"></a><span data-ttu-id="90277-114">Funktionsprofil konfigurieren</span><span class="sxs-lookup"><span data-stu-id="90277-114">Configure the functionality profile</span></span>
<span data-ttu-id="90277-115">Wenn in bar am POS bezahlt wird, kann der Benutzer die Währungen rasch verwenden, um den vom Kunden bezahlten Betrag einzugeben.</span><span class="sxs-lookup"><span data-stu-id="90277-115">When paying by cash in POS, the user can use the note denominations to quickly enter the amount paid by the customer.</span></span> <span data-ttu-id="90277-116">Im Funktionsprofil können Sie die beiden Optionen für die Anzeige für den Nennwert in POS sperren konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="90277-116">In the functionality profile, you can configure the two options for showing the denomination in POS.</span></span>

<span data-ttu-id="90277-117">**Größer oder gleich fälligen Betrag**: Standardmäßig zeigt POS nur die Hinweisnennwerte an, die größer als der fällige Betrag sind, der das Einnotenanbieten zulässt.</span><span class="sxs-lookup"><span data-stu-id="90277-117">**Greater or equal to amount due**: By default, POS will only show the note denominations that are greater than the amount due, which allows for one-touch tendering.</span></span> <span data-ttu-id="90277-118">Wenn beispielsweise der fällige Betrag $7,50 POS ist, würden die folgenden Nennwerte angezeigt: EUR 10, 20, 50 und 100.</span><span class="sxs-lookup"><span data-stu-id="90277-118">For example, if the amount due is $7.50, POS would show the following denominations: $10, $20, $50, and $100.</span></span> <span data-ttu-id="90277-119">Wenn Sie einen dieser Beträge berühren, wird automatisch das Zahlungsmittel des Verkaufs für diesen Betrag ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="90277-119">Touching any of these amounts will automatically tender the sale for that amount.</span></span> <span data-ttu-id="90277-120">Die $1 und $5 Noten werden nicht angezeigt, da diese Beträge kleiner sind als der fällige Betrag.</span><span class="sxs-lookup"><span data-stu-id="90277-120">The $1 and $5 notes are not shown since these amounts are less than the amount due.</span></span>

<span data-ttu-id="90277-121">**Alle Nennwerte**: Wählen Sie diese Option aus, um alle Hinweisnennwerte in POS, unabhängig vom fälligen Betrag immer anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="90277-121">**All denominations**: Select this option to always show all note denominations in POS, regardless of the amount due.</span></span> <span data-ttu-id="90277-122">Das bedeutet, dass der Benutzer eine Kombination von Hinweisen verwenden kann, um den fälligen Betrag zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="90277-122">This means that the user can use a combination of notes to reach the amount due.</span></span> <span data-ttu-id="90277-123">Wenn beispielsweise der fällige Betrag $25.00 ist, kann der Benutzer $20 und $5 wählen, um den Verkauf abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="90277-123">For example, if the amount due is $25.00, the user can choose $20 and $5 to complete the sale.</span></span>

