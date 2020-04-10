---
title: Eine Mehrwertsteuerzahlung erstellen
description: Beim Einzelvorgang zum Abrechnen und Buchen der Mehrwertsteuer werden Mehrwertsteuersalden zu den Mehrwertsteuerkonten ausgeglichen und sie werden für einen angegebenen Zeitraum zum Mehrwertsteuer-Abrechnungskonto gegengebucht.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 99059a8e5d6f4bf125266ad2a98cb73751529e6b
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3139921"
---
# <a name="create-a-sales-tax-payment"></a><span data-ttu-id="f6787-103">Eine Mehrwertsteuerzahlung erstellen</span><span class="sxs-lookup"><span data-stu-id="f6787-103">Create a sales tax payment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f6787-104">Beim Einzelvorgang zum Abrechnen und Buchen der Mehrwertsteuer werden Mehrwertsteuersalden zu den Mehrwertsteuerkonten ausgeglichen und sie werden für einen angegebenen Zeitraum zum Mehrwertsteuer-Abrechnungskonto gegengebucht.</span><span class="sxs-lookup"><span data-stu-id="f6787-104">The settle and post sales tax job settles sales tax balances on the sales tax accounts and offsets them to the sales tax settlement account for a given period.</span></span>

1. <span data-ttu-id="f6787-105">Wechseln Sie zu "Steuer" > "Erklärungen" > "Mehrwertsteuer" > "Mehrwertsteuer abrechnen und buchen".</span><span class="sxs-lookup"><span data-stu-id="f6787-105">Go to Tax > Declarations > Sales tax > Settle and post sales tax.</span></span>
2. <span data-ttu-id="f6787-106">Klicken Sie im Feld "Abrechnungszeitraum" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="f6787-106">In the Settlement period field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="f6787-107">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="f6787-107">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="f6787-108">Geben Sie in das Feld "Von Datum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="f6787-108">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="f6787-109">Wenn die Option "Korrekturen einbeziehen" nicht auf der Seite "Hauptbuchparameter" ausgewählt ist, kann die Abrechnung für verschiedene Versionen verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="f6787-109">If the Include corrections option is not selected on the General ledger parameters page, the settlement can be processed for different versions.</span></span> <span data-ttu-id="f6787-110">Das Original ist die erste Abrechnung für ein Periodenintervall und kann nur einmal für ein Periodenintervall verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="f6787-110">Original is the first settlement for a period interval and can only processed once for a period interval.</span></span> <span data-ttu-id="f6787-111">Mit den neuesten Korrekturen werden Mehrwertsteuertransaktionen abgerechnet, die gebucht wurden, nachdem die Originalversion erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="f6787-111">Latest corrections will settle sales tax transactions which have been posted after the original version has been created.</span></span>   
5. <span data-ttu-id="f6787-112">Geben Sie im Feld "Transaktionsdatum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="f6787-112">In the Transaction date field, enter a date.</span></span>
6. <span data-ttu-id="f6787-113">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="f6787-113">Click OK.</span></span>

