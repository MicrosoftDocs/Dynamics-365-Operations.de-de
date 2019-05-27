---
title: Einen vordatierten Scheck für einen Debitor erfassen und buchen
description: Sie können die Details eines vordatierten Schecks erfassen, den Sie von einem Debitor erhalten haben.
author: kweekley
manager: AnnBe
ms.date: 10/26/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 131e4f364c62d03b95fb4b77f472828b9483d5e1
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566086"
---
# <a name="register-and-post-a-postdated-check-for-a-customer"></a><span data-ttu-id="dc98c-103">Einen vordatierten Scheck für einen Debitor erfassen und buchen</span><span class="sxs-lookup"><span data-stu-id="dc98c-103">Register and post a postdated check for a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dc98c-104">Sie können die Details eines vordatierten Schecks erfassen, den Sie von einem Debitor erhalten haben.</span><span class="sxs-lookup"><span data-stu-id="dc98c-104">You can register details of a postdated check received from a customer.</span></span> <span data-ttu-id="dc98c-105">Sie können den vordatierten Scheck buchen und Finanzbuchungen erstellen.</span><span class="sxs-lookup"><span data-stu-id="dc98c-105">You can also post the postdated check and generate financial transactions.</span></span>   <span data-ttu-id="dc98c-106">Führen Sie die folgenden Schritte aus, bevor Sie einen vordatierten Scheck erfasst und gebucht, der von einem Debitor erhalten haben:   • Einrichten von vordatierten Schecks in bar und in der Bankwesenseite • Einrichten einer Zahlungsmethode für vordatierte Schecks, für die der Rolle für diesen Schritt Schatzmeister ist.</span><span class="sxs-lookup"><span data-stu-id="dc98c-106">Complete the following tasks before you register and post a postdated check received from a customer:   • Set up postdated check in the Cash and bank management page • Set up a method of payment for postdated checks   The role for this procedure is Treasurer.</span></span> <span data-ttu-id="dc98c-107">Für diese Prozedur wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="dc98c-107">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="dc98c-108">Wechseln Sie zu "Debitoren" > "Zahlungen" > "Zahlungserfassung".</span><span class="sxs-lookup"><span data-stu-id="dc98c-108">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="dc98c-109">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="dc98c-109">Click New.</span></span>
3. <span data-ttu-id="dc98c-110">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="dc98c-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="dc98c-111">Klicken Sie auf "Positionen".</span><span class="sxs-lookup"><span data-stu-id="dc98c-111">Click Lines.</span></span>
5. <span data-ttu-id="dc98c-112">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="dc98c-112">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="dc98c-113">Geben Sie im Feld "Konto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="dc98c-113">In the Account field, specify the desired values.</span></span>
7. <span data-ttu-id="dc98c-114">Geben Sie im Feld "Kredit" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="dc98c-114">In the Credit field, enter a number.</span></span>
    * <span data-ttu-id="dc98c-115">Geben Sie den im vordatierten Scheck angegebene Betrag an.</span><span class="sxs-lookup"><span data-stu-id="dc98c-115">Enter the amount specified in the postdated check.</span></span>  
8. <span data-ttu-id="dc98c-116">Klicken Sie auf die Registerkarte Zahlung.</span><span class="sxs-lookup"><span data-stu-id="dc98c-116">Click the Payment tab.</span></span>
9. <span data-ttu-id="dc98c-117">Geben Sie im Feld "Zahlungsmethode" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="dc98c-117">In the Method of payment field, type a value.</span></span>
    * <span data-ttu-id="dc98c-118">Wählen Sie die Zahlungsmethode für den vordatierten Scheck aus.</span><span class="sxs-lookup"><span data-stu-id="dc98c-118">Select the method of payment for the postdated check.</span></span>  
10. <span data-ttu-id="dc98c-119">Klicken Sie auf die Registerkarte "Vordatierte Schecks".</span><span class="sxs-lookup"><span data-stu-id="dc98c-119">Click the Postdated checks tab.</span></span>
11. <span data-ttu-id="dc98c-120">Geben Sie im Feld "Fälligkeitsdatum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="dc98c-120">In the Maturity date field, enter a date.</span></span>
    * <span data-ttu-id="dc98c-121">Geben Sie das Datum an, an dem der vordatierte Scheck zur Zahlung fällig ist.</span><span class="sxs-lookup"><span data-stu-id="dc98c-121">Enter the date when the postdated check is due for payment.</span></span>  
12. <span data-ttu-id="dc98c-122">Geben Sie im Feld "Ausstellende Bankfiliale" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="dc98c-122">In the Issuing bank branch field, type a value.</span></span>
    * <span data-ttu-id="dc98c-123">Geben Sie die Details der Bank auf dem vordatierten Scheck ein.</span><span class="sxs-lookup"><span data-stu-id="dc98c-123">Enter the bank details of the postdated check.</span></span>  
13. <span data-ttu-id="dc98c-124">Geben Sie im Feld "Schecknummer" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="dc98c-124">In the check number field, type a value.</span></span>
14. <span data-ttu-id="dc98c-125">Geben Sie im Feld "Ausstellender Bankname" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="dc98c-125">In the Issuing bank name field, type a value.</span></span>
    * <span data-ttu-id="dc98c-126">Geben Sie die Details der Bank auf dem vordatierten Scheck ein.</span><span class="sxs-lookup"><span data-stu-id="dc98c-126">Enter the bank details of the postdated check.</span></span>  
15. <span data-ttu-id="dc98c-127">Klicken Sie auf "Buchen".</span><span class="sxs-lookup"><span data-stu-id="dc98c-127">Click Post.</span></span>
16. <span data-ttu-id="dc98c-128">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="dc98c-128">Close the page.</span></span>

