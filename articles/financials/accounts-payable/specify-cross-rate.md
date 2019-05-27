---
title: Angeben des Kreuzkurses
description: Dieses Thema enthält allgemeine Informationen zu Kreuzkurse in Microsoft Dynamics 365 for Finance and Operations.
author: abruer
manager: AnnBe
ms.date: 05/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 112f77738b33aae94babe0cf8e9e61ff2ea3d004
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1546063"
---
# <a name="specify-the-cross-rate"></a><span data-ttu-id="9299f-103">Angeben des Kreuzkurses</span><span class="sxs-lookup"><span data-stu-id="9299f-103">Specify the cross rate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9299f-104">In diesem Thema wird der Zweck eines Kreuzkurses erklärt, und wie der Kreuzkurs angegeben wird, wenn Sie eine Zahlung mit einer Rechnung ausgleichen.</span><span class="sxs-lookup"><span data-stu-id="9299f-104">This topic explains the purpose of a cross rate, and how to specify the cross rate when you settle a payment with an invoice.</span></span> <span data-ttu-id="9299f-105">Verwenden Sie einen Kreuzkurs, wenn alle folgenden Kriterien zutreffen:</span><span class="sxs-lookup"><span data-stu-id="9299f-105">Use a cross rate when all of the following criteria apply:</span></span> 
-   <span data-ttu-id="9299f-106">Sie gleichen eine Zahlung mit einer Rechnung aus.</span><span class="sxs-lookup"><span data-stu-id="9299f-106">You are settling a payment with an invoice.</span></span> 
-   <span data-ttu-id="9299f-107">Die Zahlungsposition und die Rechnungsposition verwenden verschiedene Währungen.</span><span class="sxs-lookup"><span data-stu-id="9299f-107">The payment line and the invoice line use different currencies.</span></span> 
-   <span data-ttu-id="9299f-108">Keine dieser Währungen ist die Buchhaltungswährung.</span><span class="sxs-lookup"><span data-stu-id="9299f-108">Neither currency is the accounting currency.</span></span> 

<span data-ttu-id="9299f-109">Der Kreuzkurs wird nicht verwendet, um die Zahlungsbuchungswährungsübersetzung der Buchhaltungswährung für die Zahlung zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="9299f-109">The cross rate is not used to calculate the payment transaction currency translation to the payment accounting currency.</span></span> <span data-ttu-id="9299f-110">Stattdessen werden die Wechselkurse aus den Wechselkurstabellen abgerufen, um den Wert des Zahlungsbuchungswährungsbetrags und des Zahlungsbuchhaltungswährungsbetrags zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="9299f-110">Instead, the exchange rates from the exchange rate tables are retrieved to calculate the value of the payment transaction currency amount and the payment accounting currency amount.</span></span> 

<span data-ttu-id="9299f-111">Beispielsweise ist die Buchhaltungswährung USD, die Rechnungswährung ist CAD, und die Zahlungswährung ist EUR.</span><span class="sxs-lookup"><span data-stu-id="9299f-111">For example, the accounting currency is USD, the invoice currency is CAD, and the payment currency is EUR.</span></span> <span data-ttu-id="9299f-112">Mit dem Kreuzkurs können Sie einen Wechselkurs eingeben, um direkt zwischen CAD und EUR zu übersetzen, ohne in EUR zu übersetzen.</span><span class="sxs-lookup"><span data-stu-id="9299f-112">The cross rate lets you enter an exchange rate to translate directly between CAD and EUR, and not have to translate through USD.</span></span> <span data-ttu-id="9299f-113">Beim Auswählen einer Rechnung und einer Primärzahlung besteht die Möglichkeit zum Eingeben eines Kreuzkurses für die Rechungsposition.</span><span class="sxs-lookup"><span data-stu-id="9299f-113">When you select an invoice and a primary payment, you can enter a cross rate for the invoice line.</span></span> <span data-ttu-id="9299f-114">Bei diesem Kreuzkurs handelt es sich um den Wechselkurs zwischen den Währungen zum Ausgleichsdatum.</span><span class="sxs-lookup"><span data-stu-id="9299f-114">The cross rate is the exchange rate between the currencies for those transactions, as of the settlement date.</span></span>

1.  <span data-ttu-id="9299f-115">Gehen Sie zu den folgenden Seiten:</span><span class="sxs-lookup"><span data-stu-id="9299f-115">Go to one of the following pages:</span></span>
- <span data-ttu-id="9299f-116">**Klicken Sie auf Debitoren  Allgemein  Kunden  Alle Kunden**</span><span class="sxs-lookup"><span data-stu-id="9299f-116">**Accounts receivable > Common > Customers > All customers**</span></span> 
- <span data-ttu-id="9299f-117">**Gehen Sie zu "Kreditorenkonten" > "Allgemein" > "Händler" > alle Händler**</span><span class="sxs-lookup"><span data-stu-id="9299f-117">**Accounts payable > Common > Vendors > All vendors**</span></span> 
- <span data-ttu-id="9299f-118">**Klicken Sie auf Beschaffung > Gemeinsam > Kreditoren > Alle Kreditoren**</span><span class="sxs-lookup"><span data-stu-id="9299f-118">**Procurement and sourcing > Common > Vendors > All vendors**</span></span>
2.  <span data-ttu-id="9299f-119">Wählen Sie den Debitor oder Kreditor aus, dessen offene Posten ausgeglichen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9299f-119">Select the customer or vendor whose open transactions you are settling.</span></span> 
3.  <span data-ttu-id="9299f-120">Für einen Debitor auf der Listenseite **Alle Debitoren** gehen Sie zu **Sammeln > Offene Buchungen ausgleichen**.</span><span class="sxs-lookup"><span data-stu-id="9299f-120">For a customer, on the **All customers** list page, go to **Collect > Settle open transactions**.</span></span> <span data-ttu-id="9299f-121">Für einen Debitor auf der Listenseite **Alle Debitoren** gehen Sie zu **Sammeln > Offene Buchungen ausgleichen**.</span><span class="sxs-lookup"><span data-stu-id="9299f-121">For a vendor, on the **All vendors** list page, go to **Invoice > Settle open transactions**.</span></span> 
4.  <span data-ttu-id="9299f-122">Wählen Sie die Buchung aus, bei der es sich um die primäre Zahlung handelt, und klicken Sie auf die Schaltfläche **Zahlung markieren** .</span><span class="sxs-lookup"><span data-stu-id="9299f-122">Select the transaction that is the primary payment, and then click **Mark payment**.</span></span> <span data-ttu-id="9299f-123">Das Kontrollkästchen in der Spalte **Markieren** wird aktiviert, und in der Spalte **Primäre Zahlung** wird ein Informationssymbol angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9299f-123">The check box in the **Mark** column is selected, and an information icon is shown in the **Primary payment** column.</span></span> 
5.  <span data-ttu-id="9299f-124">Geben Sie im Feld **Kreuzkurs** den Wechselkurs zwischen der Rechnungs- und der Zahlungswährung zum Ausgleichsdatum ein.</span><span class="sxs-lookup"><span data-stu-id="9299f-124">In the **Cross rate** field, enter the exchange rate between the invoice currency and the payment currency, as of the settlement date.</span></span> 
