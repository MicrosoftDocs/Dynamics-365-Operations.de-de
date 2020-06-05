---
title: Intercompany-Ausgaben
description: Eine Arbeitskraft, die von einer juristischen Personen in einer Organisation beschäftigt wird, kann möglicherweise Arbeit für eine andere juristische Person in derselben Organisation ausführen. In diesem Fall können Sie die Intercompany-Ausgabenfunktion verwenden, um die Ausgaben der Arbeitskraft der juristischen Person zuzuweisen, für die die Arbeit ausgeführt wurde.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 07e425707eb20730f10246a27799f4deeef93f97
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/21/2020
ms.locfileid: "3390883"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="f6016-104">Intercompany-Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f6016-104">Intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f6016-105">Eine Arbeitskraft, die von einer juristischen Personen in einer Organisation beschäftigt wird, kann möglicherweise Arbeit für eine andere juristische Person in derselben Organisation ausführen.</span><span class="sxs-lookup"><span data-stu-id="f6016-105">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="f6016-106">In diesem Fall können Sie die Intercompany-Ausgabenfunktion verwenden, um die Ausgaben der Arbeitskraft der juristischen Person zuzuweisen, für die die Arbeit ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="f6016-106">In this situation, you can use the intercompany expense feature to assign the worker’s expenses to the legal entity for which the work was performed.</span></span> <span data-ttu-id="f6016-107">Die juristische Person, die die Arbeitskraft verwendet, wird als verleihende juristische Person bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="f6016-107">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="f6016-108">Die juristische Person, für die die Arbeitskraft Ausgaben verursacht, wird als ausleihende juristische Person bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="f6016-108">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="f6016-109">Bevor eine Arbeitskraft Ausgaben für die Arbeit erstellen und übermitteln kann, die für eine andere juristische Person ausgeführt wurde, wählen Sie in der verleihenden juristischen Person auf der Seite **Ausgabenverwaltungsparameter** die Option **Intercompany-Ausgabenpositionen zulassen** aus.</span><span class="sxs-lookup"><span data-stu-id="f6016-109">Before a worker can create and submit expenses for work that is performed for a different legal entity, in the loaning legal entity, on the **Expense management parameters** page, select the **Allow intercompany expense lines** option.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="f6016-110">Steuerbuchung für Intercompany-Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f6016-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f6016-111">Wenn Sie in Ihrer Spesenabrechnung Steuergruppen verwenden möchten, die der verleihenden juristischen Person (Quelle) anstelle der ausleihenden juristischen Person (Ziel) zugeordnet sind, müssen Sie dies in der eingerichteten Mehrwertsteuer des Hauptbuchs konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="f6016-111">If you want to use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you will need to configure this in the General ledger sales tax set up.</span></span> <span data-ttu-id="f6016-112">Wenn der Hauptbuchparameter **Juristische Person für Intercompany-Steuerbuchung** auf **Quelle** und **Mehrwertsteuerregeln anwenden** auf **Nein** festgelegt ist, wird die Steuerkombination für die verleihende juristische Person verwendet.</span><span class="sxs-lookup"><span data-stu-id="f6016-112">When the General ledger parameter, **Legal entity for intercompany tax posting** is set to **Source** and **Apply sales tax taxation rules** is set to **No**, the tax combination for the loaning legal entity will be used.</span></span> <span data-ttu-id="f6016-113">Wenn derselbe Parameter auf **Ziel** festgelegt ist, wird die Steuerkombination für die ausleihende juristische Person verwendet.</span><span class="sxs-lookup"><span data-stu-id="f6016-113">When the same parameter is set to **Destination**, the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="f6016-114">Für juristische Personen in den USA muss das Feld **Vorsteuer** auch auf der neuen Seite **Sachkontobuchungsgruppen** konfiguriert werden, wenn der Parameter auf **Quelle** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f6016-114">For legal entities in the United States, when the parameter is set to **Source**, the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="f6016-115">Die Buchhaltungs-Engine verwendet die Informationen aus diesem Feld für steuerbezogene Buchhaltungseinträge.</span><span class="sxs-lookup"><span data-stu-id="f6016-115">The accounting engine will use the information from this field for tax related accounting entry.</span></span>   
<span data-ttu-id="f6016-116">Das Verhalten ist für Ausgabenpositionen, die mit oder ohne Projekt gebucht wurden, konsistent.</span><span class="sxs-lookup"><span data-stu-id="f6016-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  
