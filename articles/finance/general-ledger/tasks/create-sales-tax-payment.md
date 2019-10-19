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
ms.openlocfilehash: ee69cfee672be1571fd5cc630e33601bb5a48eac
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186163"
---
# <a name="create-a-sales-tax-payment"></a><span data-ttu-id="a571c-103">Eine Mehrwertsteuerzahlung erstellen</span><span class="sxs-lookup"><span data-stu-id="a571c-103">Create a sales tax payment</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a571c-104">Beim Einzelvorgang zum Abrechnen und Buchen der Mehrwertsteuer werden Mehrwertsteuersalden zu den Mehrwertsteuerkonten ausgeglichen und sie werden für einen angegebenen Zeitraum zum Mehrwertsteuer-Abrechnungskonto gegengebucht.</span><span class="sxs-lookup"><span data-stu-id="a571c-104">The settle and post sales tax job settles sales tax balances on the sales tax accounts and offsets them to the sales tax settlement account for a given period.</span></span>

1. <span data-ttu-id="a571c-105">Wechseln Sie zu "Steuer" > "Erklärungen" > "Mehrwertsteuer" > "Mehrwertsteuer abrechnen und buchen".</span><span class="sxs-lookup"><span data-stu-id="a571c-105">Go to Tax > Declarations > Sales tax > Settle and post sales tax.</span></span>
2. <span data-ttu-id="a571c-106">Klicken Sie im Feld "Abrechnungszeitraum" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="a571c-106">In the Settlement period field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="a571c-107">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="a571c-107">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="a571c-108">Geben Sie in das Feld "Von Datum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="a571c-108">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="a571c-109">Wenn die Option "Korrekturen einbeziehen" nicht auf der Seite "Hauptbuchparameter" ausgewählt ist, kann die Abrechnung für verschiedene Versionen verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="a571c-109">If the Include corrections option is not selected on the General ledger parameters page, the settlement can be processed for different versions.</span></span> <span data-ttu-id="a571c-110">Das Original ist die erste Abrechnung für ein Periodenintervall und kann nur einmal für ein Periodenintervall verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="a571c-110">Original is the first settlement for a period interval and can only processed once for a period interval.</span></span> <span data-ttu-id="a571c-111">Mit den neuesten Korrekturen werden Mehrwertsteuertransaktionen abgerechnet, die gebucht wurden, nachdem die Originalversion erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="a571c-111">Latest corrections will settle sales tax transactions which have been posted after the original version has been created.</span></span>   
5. <span data-ttu-id="a571c-112">Geben Sie im Feld "Transaktionsdatum" ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="a571c-112">In the Transaction date field, enter a date.</span></span>
6. <span data-ttu-id="a571c-113">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="a571c-113">Click OK.</span></span>

