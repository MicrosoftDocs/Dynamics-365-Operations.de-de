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
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 457be741dfd3b44cb963db37857d6a7bceecc14e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994664"
---
# <a name="create-accrual-schemes"></a><span data-ttu-id="f5071-103">Abgrenzungsschemata erstellen</span><span class="sxs-lookup"><span data-stu-id="f5071-103">Create accrual schemes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f5071-104">In diesem Thema wird erläutert, wie Sie ein Abgrenzungsschema erstellen.</span><span class="sxs-lookup"><span data-stu-id="f5071-104">This topic explains how to create an accrual scheme.</span></span> <span data-ttu-id="f5071-105">Für diese Aufgabe wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="f5071-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="f5071-106">Wechseln Sie zu **Navigationsbereich > Module > Hauptbuch > Erfassungseinstellungen > Abgrenzungsschemata**.</span><span class="sxs-lookup"><span data-stu-id="f5071-106">Go to **Navigation pane > Modules > General ledger > Journal setup > Accrual schemes**.</span></span>
2. <span data-ttu-id="f5071-107">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="f5071-107">Select **New**.</span></span>
3. <span data-ttu-id="f5071-108">Geben Sie im Feld **Abgrenzungskennung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="f5071-108">In the **Accrual identification** field, type a value.</span></span>
4. <span data-ttu-id="f5071-109">Geben Sie im Feld **Beschreibung des Abgrenzungsschemas** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="f5071-109">In the **Description of accrual scheme** field, type a value.</span></span>
5. <span data-ttu-id="f5071-110">Geben Sie im Feld **Soll** die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="f5071-110">In the **Debit** field, specify the desired values.</span></span> <span data-ttu-id="f5071-111">Das Hauptkonto ersetzt das Sollhauptkonto auf der Erfassungsbelegposition und es wird auch für die Rückbuchung der Stundung auf Grundlage die Sachkontoabgrenzungsbuchungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="f5071-111">The main account defined will replace the debit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
6. <span data-ttu-id="f5071-112">Geben Sie im Feld **Haben** die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="f5071-112">In the **Credit** field, specify the desired values.</span></span> <span data-ttu-id="f5071-113">Das Hauptkonto ersetzt das Habenhauptkonto auf der Erfassungsbelegposition und es wird auch für die Rückbuchung der Stundung auf Grundlage die Sachkontoabgrenzungsbuchungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="f5071-113">The main account defined will replace the credit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
7. <span data-ttu-id="f5071-114">Wählen Sie im Feld **Beleg** aus, wie der spezifischen Beleg festgelegt werden soll, wenn die Buchungen gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="f5071-114">In the **Voucher** field, select how you want the voucher determined when the transactions are posted.</span></span>
8. <span data-ttu-id="f5071-115">Geben Sie im Feld **Beschreibung** einen Wert ein, um die Buchungen zu beschreiben, die gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="f5071-115">In the **Description** field, type a value to describe the transactions that will be posted.</span></span>
9. <span data-ttu-id="f5071-116">Wählen Sie im Feld **Periodenhäufigkeit** aus, wie häufig die Buchungen erfolgen sollen.</span><span class="sxs-lookup"><span data-stu-id="f5071-116">In the **Period frequency** field, select how often the transactions should occur.</span></span>
10. <span data-ttu-id="f5071-117">Geben Sie im Feld **Anzahl der Vorkommen nach Periode** eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="f5071-117">In the **Number of occurrences by period** field, enter a number.</span></span>
11. <span data-ttu-id="f5071-118">Wählen Sie im Feld **Transaktionen buchen** aus, wann die Buchungen gebucht werden sollen (z. B. **Monatlich**).</span><span class="sxs-lookup"><span data-stu-id="f5071-118">In the **Post transactions** field, select when the transactions should be posted, such as **Monthly**.</span></span>

