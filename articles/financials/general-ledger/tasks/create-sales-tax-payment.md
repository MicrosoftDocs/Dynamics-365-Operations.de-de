--- 
title: Eine Mehrwertsteuerzahlung erstellen
description: "Beim Einzelvorgang zum Abrechnen und Buchen der Mehrwertsteuer werden Mehrwertsteuersalden zu den Mehrwertsteuerkonten ausgeglichen und sie werden für einen angegebenen Zeitraum zum Mehrwertsteuer-Abrechnungskonto gegengebucht."
author: twheeloc
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 6ee84da7fd055c8b0b50c43f134c0fc048ecfaeb
ms.contentlocale: de-de
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-sales-tax-payment"></a><span data-ttu-id="647fd-103">Eine Mehrwertsteuerzahlung erstellen</span><span class="sxs-lookup"><span data-stu-id="647fd-103">Create a sales tax payment</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="647fd-104">Beim Einzelvorgang zum Abrechnen und Buchen der Mehrwertsteuer werden Mehrwertsteuersalden zu den Mehrwertsteuerkonten ausgeglichen und sie werden für einen angegebenen Zeitraum zum Mehrwertsteuer-Abrechnungskonto gegengebucht.</span><span class="sxs-lookup"><span data-stu-id="647fd-104">The settle and post sales tax job settles sales tax balances on the sales tax accounts and offsets them to the sales tax settlement account for a given period.</span></span>

1. <span data-ttu-id="647fd-105">Wechseln Sie zu "Steuer" > "Erklärungen" > "Mehrwertsteuer" > "Mehrwertsteuer abrechnen und buchen".</span><span class="sxs-lookup"><span data-stu-id="647fd-105">Go to Tax > Declarations > Sales tax > Settle and post sales tax.</span></span>
2. <span data-ttu-id="647fd-106">Klicken Sie im Feld "Abrechnungszeitraum" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="647fd-106">In the Settlement period field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="647fd-107">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="647fd-107">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="647fd-108">Geben Sie in das Feld "Von Datum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="647fd-108">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="647fd-109">Wenn die Option "Korrekturen einbeziehen" nicht auf der Seite "Hauptbuchparameter" ausgewählt ist, kann die Abrechnung für verschiedene Versionen verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="647fd-109">If the Include corrections option is not selected on the General ledger parameters page, the settlement can be processed for different versions.</span></span> <span data-ttu-id="647fd-110">Das Original ist die erste Abrechnung für ein Periodenintervall und kann nur einmal für ein Periodenintervall verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="647fd-110">Original is the first settlement for a period interval and can only processed once for a period interval.</span></span> <span data-ttu-id="647fd-111">Mit den neuesten Korrekturen werden Mehrwertsteuertransaktionen abgerechnet, die gebucht wurden, nachdem die Originalversion erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="647fd-111">Latest corrections will settle sales tax transactions which have been posted after the original version has been created.</span></span>   
5. <span data-ttu-id="647fd-112">Geben Sie im Feld "Transaktionsdatum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="647fd-112">In the Transaction date field, enter a date.</span></span>
6. <span data-ttu-id="647fd-113">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="647fd-113">Click OK.</span></span>


