---
title: Eine Mehrwertsteuerzahlung erstellen
description: Bei der Einzelvorgangsprozedur zum Abrechnen und Buchen der Mehrwertsteuer werden Mehrwertsteuersalden zu den Mehrwertsteuerkonten ausgeglichen und sie werden für einen angegebenen Zeitraum zum Mehrwertsteuer-Abrechnungskonto gegengebucht.
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
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9b5e3e26e19bd0a9dbf878626328da267b61964f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968703"
---
# <a name="create-a-sales-tax-payment"></a><span data-ttu-id="0da65-103">Eine Mehrwertsteuerzahlung erstellen</span><span class="sxs-lookup"><span data-stu-id="0da65-103">Create a sales tax payment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0da65-104">Bei der Einzelvorgangsprozedur zum Abrechnen und Buchen der Mehrwertsteuer werden Mehrwertsteuersalden zu den Mehrwertsteuerkonten ausgeglichen und sie werden für einen angegebenen Zeitraum zum Mehrwertsteuer-Abrechnungskonto gegengebucht.</span><span class="sxs-lookup"><span data-stu-id="0da65-104">The settle and post sales tax job procedure settles sales tax balances on the sales tax accounts, and offsets them to the sales tax settlement account for a given period.</span></span>

1. <span data-ttu-id="0da65-105">Wechseln Sie zu **Steuer > Erklärungen > Mehrwertsteuer > Mehrwertsteuer abrechnen und buchen**.</span><span class="sxs-lookup"><span data-stu-id="0da65-105">Go to **Tax > Declarations > Sales tax > Settle and post sales tax**.</span></span>
2. <span data-ttu-id="0da65-106">Klicken Sie im Feld **Abrechnungszeitraum** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="0da65-106">In the **Settlement period** field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="0da65-107">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="0da65-107">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="0da65-108">Geben Sie im Feld **Von Datum** ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="0da65-108">In the **From date** field, enter a date.</span></span>
    * <span data-ttu-id="0da65-109">Wenn Sie die Option **Korrekturen einbeziehen** nicht auf der Seite **Hauptbuchparameter** auswählen, kann die Abrechnung für verschiedene Versionen verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="0da65-109">If you don't select the **Include corrections** option on the **General ledger parameters** page, the settlement can be processed for different versions.</span></span> <span data-ttu-id="0da65-110">Das Original ist die erste Abrechnung für ein Periodenintervall und kann nur einmal für ein Periodenintervall verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="0da65-110">Original is the first settlement for a period interval and can be processed only once for a period interval.</span></span> <span data-ttu-id="0da65-111">Mit den neuesten Korrekturen werden Mehrwertsteuertransaktionen abgerechnet, die gebucht wurden, nachdem die Originalversion erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="0da65-111">The latest corrections will settle sales tax transactions which have been posted after the original version has been created.</span></span>   
5. <span data-ttu-id="0da65-112">Geben Sie im Feld **Transaktionsdatum** ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="0da65-112">In the **Transaction date** field, enter a date.</span></span>
6. <span data-ttu-id="0da65-113">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="0da65-113">Click **OK**.</span></span>

