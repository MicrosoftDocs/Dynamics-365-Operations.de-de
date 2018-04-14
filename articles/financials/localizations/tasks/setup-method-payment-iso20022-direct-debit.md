--- 
title: "Zahlungsmethode für ISO20022-Direktbelastung einrichten"
description: "Dieses Verfahren zeigt, wie ISO20022-Direktbelastung für die Debitorenzahlungsmethode Banküberweisung oder einen anderen Zahlungstyp über eine elektronischen Berichterstellung verwendet wird."
author: mrolecki
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: aa159fdf8a8ef543c338546a389d37e1644676a3
ms.contentlocale: de-de
ms.lasthandoff: 04/13/2018

---
# <a name="set-up-method-of-payment-for-iso20022-direct-debit"></a><span data-ttu-id="5302e-103">Zahlungsmethode für ISO20022-Direktbelastung einrichten</span><span class="sxs-lookup"><span data-stu-id="5302e-103">Set up method of payment for ISO20022 direct debit</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5302e-104">Dieses Verfahren zeigt, wie ISO20022-Direktbelastung für die Debitorenzahlungsmethode Banküberweisung oder einen anderen Zahlungstyp über eine elektronischen Berichterstellung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5302e-104">This procedure shows how to set up the customer method of payment for ISO20022 direct debit or any other payment type using electronic reporting.</span></span> 



<span data-ttu-id="5302e-105">Bevor Sie diese Aufgabe abschließen, müssen Sie Exportformatkonfigurations- und Zahlungskonteneinstellung eingerichtet haben.</span><span class="sxs-lookup"><span data-stu-id="5302e-105">Before you complete this task, you must set up export format configurations and payment accounts.</span></span>



<span data-ttu-id="5302e-106">Diese Prozedur wurde mit dem Demodatenunternehmen DEMF erstellt.</span><span class="sxs-lookup"><span data-stu-id="5302e-106">This procedure was created using the demo data company DEMF.</span></span>



<span data-ttu-id="5302e-107">Dies ist die dritte von sechs Aufgaben, die das Verfahren für Debitorenzahlungen über elektronischen Berichterstellungskonfigurationen zeigen.</span><span class="sxs-lookup"><span data-stu-id="5302e-107">This is the third of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>

1. <span data-ttu-id="5302e-108">Wechseln Sie zu "Debitoren" > "Zahlungseinstellungen" > "Zahlungsmethoden".</span><span class="sxs-lookup"><span data-stu-id="5302e-108">Go to Accounts receivable > Payments setup > Methods of payment.</span></span>
2. <span data-ttu-id="5302e-109">Verwenden Sie den Schnellfilter, um Datensätze zu suchen.</span><span class="sxs-lookup"><span data-stu-id="5302e-109">Use the Quick Filter to find records.</span></span> <span data-ttu-id="5302e-110">Filtern Sie beispielsweise im Feld "Zahlungsmethode" mit dem Wert "ELEKTRONISCH".</span><span class="sxs-lookup"><span data-stu-id="5302e-110">For example, filter on the Method of payment field with a value of 'ELECTRONIC'.</span></span>
3. <span data-ttu-id="5302e-111">Klicken Sie auf Bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="5302e-111">Click Edit.</span></span>
4. <span data-ttu-id="5302e-112">Geben Sie im Feld "Zahlungskonto" die Werte "DEMF OPER" an.</span><span class="sxs-lookup"><span data-stu-id="5302e-112">In the Payment account field, specify the values 'DEMF OPER'.</span></span>
5. <span data-ttu-id="5302e-113">Erweitern Sie den Abschnitt 'Dateiformate'.</span><span class="sxs-lookup"><span data-stu-id="5302e-113">Expand the File formats section.</span></span>
6. <span data-ttu-id="5302e-114">Wählen Sie "Ja" im Feld "Generische elektronische Berichterstellung" aus.</span><span class="sxs-lookup"><span data-stu-id="5302e-114">Select Yes in the Generic electronic reporting field.</span></span>
7. <span data-ttu-id="5302e-115">Wählen Sie im Feld "Formatkonfiguration exportieren" einen Wert aus oder geben Sie ihn ein.</span><span class="sxs-lookup"><span data-stu-id="5302e-115">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="5302e-116">Wählen Sie in der Liste "ISO20022 Direktbelastung (DE)" aus.</span><span class="sxs-lookup"><span data-stu-id="5302e-116">In the list, select ISO20022 Direct debit (DE).</span></span>  <span data-ttu-id="5302e-117">Wenn die Liste leer ist, bedeutet dies, dass es keine importierte und aktive Debitorenzahlungs-Exportformatkonfiguration gibt.</span><span class="sxs-lookup"><span data-stu-id="5302e-117">If the list is empty, the customer payment export format configuration has not been imported and active.</span></span>  
8. <span data-ttu-id="5302e-118">Wählen Sie "Ja" im Feld "Mandat anfordern" aus.</span><span class="sxs-lookup"><span data-stu-id="5302e-118">Select Yes in the Require mandate field.</span></span>
    * <span data-ttu-id="5302e-119">Wählen Sie den Parameter "Mandat anfordern" für Debitorenzahlungsformate, die Vollmachtsinformationen in der Zahlungsnachricht benötigen, wie SEPA-Direktbelastung.</span><span class="sxs-lookup"><span data-stu-id="5302e-119">Select the Require mandate parameter for customer payment formats, which require including mandate information in the payment message, like SEPA direct debit.</span></span>  
9. <span data-ttu-id="5302e-120">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="5302e-120">Click Save.</span></span>


