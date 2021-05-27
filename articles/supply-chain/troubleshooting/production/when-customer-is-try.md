---
title: Die Chargennummer wird gelöscht, wenn eine neue Loskennung ausgewählt wird
description: Wenn Sie eine Erfassungsposition für eine Kommissionierliste überprüfen, wird der Wert im Feld „Chargennummer“ gelöscht, wenn Sie im Feld „Loskennung“ einen neuen Wert auswählen.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdJournalTransBOM
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: datra
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 71977a04adb066a8b51c9bf7b8c5a4e752ca902e
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026526"
---
# <a name="batch-number-is-cleared-when-a-new-lot-id-is-selected"></a><span data-ttu-id="2e5c4-103">Die Chargennummer wird gelöscht, wenn eine neue Loskennung ausgewählt wird</span><span class="sxs-lookup"><span data-stu-id="2e5c4-103">Batch number is cleared when a new lot ID is selected</span></span>

<span data-ttu-id="2e5c4-104">KB-Nummer: 4613107</span><span class="sxs-lookup"><span data-stu-id="2e5c4-104">KB number: 4613107</span></span>

## <a name="symptoms"></a><span data-ttu-id="2e5c4-105">Symptome</span><span class="sxs-lookup"><span data-stu-id="2e5c4-105">Symptoms</span></span>

<span data-ttu-id="2e5c4-106">Wenn Sie eine Erfassungsposition für eine Kommissionierliste überprüfen, wird der Wert im Feld **Chargennummer** gelöscht, wenn Sie im Feld **Loskennung** einen neuen Wert auswählen.</span><span class="sxs-lookup"><span data-stu-id="2e5c4-106">When you're reviewing a picking list journal line, the value in the **Batch number** field is cleared if you select a new value in the **Lot ID** field.</span></span>

## <a name="resolution"></a><span data-ttu-id="2e5c4-107">Lösung</span><span class="sxs-lookup"><span data-stu-id="2e5c4-107">Resolution</span></span>

<span data-ttu-id="2e5c4-108">Das System verhält sich wie vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="2e5c4-108">The system is behaving as designed.</span></span> <span data-ttu-id="2e5c4-109">Wenn Sie die Loskennung ändern, ändern Sie den Artikelkontext.</span><span class="sxs-lookup"><span data-stu-id="2e5c4-109">If you change the lot ID, you change the item context.</span></span> <span data-ttu-id="2e5c4-110">Daher wird die Chargennummer zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="2e5c4-110">Therefore, the batch number is reset.</span></span>

<span data-ttu-id="2e5c4-111">Um die Chargennummer einer Loskennung zuzuordnen, müssen Sie zuerst die Loskennung festlegen.</span><span class="sxs-lookup"><span data-stu-id="2e5c4-111">To associate the batch number with a lot ID, you must set the lot ID first.</span></span>
