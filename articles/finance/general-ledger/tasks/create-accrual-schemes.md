---
title: Abgrenzungsschemata erstellen
description: In diesem Thema wird erläutert, wie Sie ein Abgrenzungsschema erstellen.
author: aprilolson
manager: AnnBe
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAccrualTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a83870c4cec4de2e51e90ff1889d4beff6c23f95
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145191"
---
# <a name="create-accrual-schemes"></a><span data-ttu-id="7d286-103">Abgrenzungsschemata erstellen</span><span class="sxs-lookup"><span data-stu-id="7d286-103">Create accrual schemes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7d286-104">In diesem Thema wird erläutert, wie Sie ein Abgrenzungsschema erstellen.</span><span class="sxs-lookup"><span data-stu-id="7d286-104">This topic explains how to create an accrual scheme.</span></span> <span data-ttu-id="7d286-105">Für diese Aufgabe wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="7d286-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="7d286-106">Wechseln Sie zu **Navigationsbereich > Module > Hauptbuch > Erfassungseinstellungen > Abgrenzungsschemata**.</span><span class="sxs-lookup"><span data-stu-id="7d286-106">Go to **Navigation pane > Modules > General ledger > Journal setup > Accrual schemes**.</span></span>
2. <span data-ttu-id="7d286-107">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="7d286-107">Select **New**.</span></span>
3. <span data-ttu-id="7d286-108">Geben Sie im Feld **Abgrenzungskennung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="7d286-108">In the **Accrual identification** field, type a value.</span></span>
4. <span data-ttu-id="7d286-109">Geben Sie im Feld **Beschreibung des Abgrenzungsschemas** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="7d286-109">In the **Description of accrual scheme** field, type a value.</span></span>
5. <span data-ttu-id="7d286-110">Geben Sie im Feld **Soll** die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="7d286-110">In the **Debit** field, specify the desired values.</span></span> <span data-ttu-id="7d286-111">Das Hauptkonto ersetzt das Sollhauptkonto auf der Erfassungsbelegposition und es wird auch für die Rückbuchung der Stundung auf Grundlage die Sachkontoabgrenzungsbuchungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="7d286-111">The main account defined will replace the debit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
6. <span data-ttu-id="7d286-112">Geben Sie im Feld **Haben** die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="7d286-112">In the **Credit** field, specify the desired values.</span></span> <span data-ttu-id="7d286-113">Das Hauptkonto ersetzt das Habenhauptkonto auf der Erfassungsbelegposition und es wird auch für die Rückbuchung der Stundung auf Grundlage die Sachkontoabgrenzungsbuchungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="7d286-113">The main account defined will replace the credit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
7. <span data-ttu-id="7d286-114">Wählen Sie im Feld **Beleg** aus, wie der spezifischen Beleg festgelegt werden soll, wenn die Buchungen gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="7d286-114">In the **Voucher** field, select how you want the voucher determined when the transactions are posted.</span></span>
8. <span data-ttu-id="7d286-115">Geben Sie im Feld **Beschreibung** einen Wert ein, um die Buchungen zu beschreiben, die gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="7d286-115">In the **Description** field, type a value to describe the transactions that will be posted.</span></span>
9. <span data-ttu-id="7d286-116">Wählen Sie im Feld **Periodenhäufigkeit** aus, wie häufig die Buchungen erfolgen sollen.</span><span class="sxs-lookup"><span data-stu-id="7d286-116">In the **Period frequency** field, select how often the transactions should occur.</span></span>
10. <span data-ttu-id="7d286-117">Geben Sie im Feld **Anzahl der Vorkommen nach Periode** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="7d286-117">In the **Number of occurrences by period** field, enter a number.</span></span>
11. <span data-ttu-id="7d286-118">Wählen Sie im Feld **Transaktionen buchen** aus, wann die Buchungen gebucht werden sollen (z. B. **Monatlich**).</span><span class="sxs-lookup"><span data-stu-id="7d286-118">In the **Post transactions** field, select when the transactions should be posted, such as **Monthly**.</span></span>

