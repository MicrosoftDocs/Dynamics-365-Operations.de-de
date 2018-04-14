---
title: "Erstellen von Konsolidierungskontengruppen und zusätzlicher Konsolidierungskonten"
description: "Dieses Thema enthält Informationen zu Konsolidierungskontogruppen und zusätzlichen Konsolidierungskonten und erläutert, wie sie in Microsoft Dynamics 365 for Finance and Operations verwendet werden."
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerConsolidateAccountGroup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 265544
ms.assetid: 71c31df7-b655-46a8-8844-4f92a8bd71b0
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 08c86a6ed55c6c88d35800d7a2b68dc09adbf394
ms.contentlocale: de-de
ms.lasthandoff: 04/13/2018

---

# <a name="consolidation-account-groups-and-additional-consolidation-accounts"></a><span data-ttu-id="a117a-103">Erstellen von Konsolidierungskontengruppen und zusätzlicher Konsolidierungskonten</span><span class="sxs-lookup"><span data-stu-id="a117a-103">Consolidation account groups and additional consolidation accounts</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="a117a-104">Dieses Thema enthält Informationen zu Konsolidierungskontogruppen und zusätzlichen Konsolidierungskonten und erläutert, wie sie in Microsoft Dynamics 365 for Finance and Operations verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a117a-104">This topic provides information about consolidation account groups and additional consolidation accounts, and explains how they are used in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<a name="consolidation-account-groups"></a><span data-ttu-id="a117a-105">Konsolidierungskontogruppen</span><span class="sxs-lookup"><span data-stu-id="a117a-105">Consolidation account groups</span></span>
----------------------------

<span data-ttu-id="a117a-106">Mit Konsolidierungskontogruppen können Sie Gruppen von Konten erstellen, die Sie verwenden möchten, um Daten konsolidieren zu können.</span><span class="sxs-lookup"><span data-stu-id="a117a-106">Consolidation account groups let you create groups of the accounts that you want to use to consolidate data.</span></span> <span data-ttu-id="a117a-107">Meistens stellt eine Konsolidierungskontogruppe einen von Behörden vorgegebenen Kontenplan dar oder führt Konten in einer Gruppe zusammen, die vom Hauptsitz des Unternehmens definiert wird.</span><span class="sxs-lookup"><span data-stu-id="a117a-107">Most often, a consolidation account group represents a government-mandated chart of accounts or maps accounts to a group that is defined by the company's headquarters.</span></span> <span data-ttu-id="a117a-108">Sie finden die Konsolidierungskontogruppen im Bereich **Einstellungen** im Modul **Konsolidierungen**.</span><span class="sxs-lookup"><span data-stu-id="a117a-108">You can find consolidation account groups in the **Setup** area of the **Consolidations** module.</span></span> <span data-ttu-id="a117a-109">Wenn Sie eine neue Gruppe hinzufügen, geben Sie eine eindeutige Kennung für die Kontengruppe und einen Namen ein.</span><span class="sxs-lookup"><span data-stu-id="a117a-109">When you add a new group, you enter a unique identifier for the account group and a name.</span></span>

## <a name="additional-consolidation-accounts"></a><span data-ttu-id="a117a-110">Zusätzliche Konsolidierungskonten</span><span class="sxs-lookup"><span data-stu-id="a117a-110">Additional consolidation accounts</span></span>
<span data-ttu-id="a117a-111">Zusätzliche Konsolidierungskonten können einem Konto aus einem vorhandenen Kontenplan einer Konsolidierungskontogruppe zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="a117a-111">Additional consolidation accounts let you assign an account from an existing chart of accounts to a consolidation account group.</span></span> <span data-ttu-id="a117a-112">Sie können einen Konsolidierungskontowert und dann einen Namen angeben.</span><span class="sxs-lookup"><span data-stu-id="a117a-112">You can then specify a consolidation account value and name.</span></span> 

<span data-ttu-id="a117a-113">Sie finden die zusätzlichen Konsolidierungskontogruppen im Bereich **Einstellungen** im Modul **Konsolidierungen**.</span><span class="sxs-lookup"><span data-stu-id="a117a-113">You can find additional consolidation accounts in the **Setup** area of the **Consolidations** module.</span></span> <span data-ttu-id="a117a-114">Wenn Sie ein neues Konsolidierungskonto erstellen, müssen Sie die folgenden Informationen angeben:</span><span class="sxs-lookup"><span data-stu-id="a117a-114">When you create a new consolidation account, you must specify the following information:</span></span>

-   <span data-ttu-id="a117a-115">**Hauptkonto** – Dieses Feld ist ein Suchfeld, das alle Hauptkonten anzeigt, die auf dem Kontenplan basieren, den Sie auf der Seite ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="a117a-115">**Main account** – This field is a lookup that shows all the main accounts that are based on the chart of accounts that you selected on the page.</span></span> <span data-ttu-id="a117a-116">Wenn Sie ein Konto auswählen, wird der Name automatisch im Feld **Name des Hauptkontos** eingegeben.</span><span class="sxs-lookup"><span data-stu-id="a117a-116">When you select an account, the name is automatically entered in the **Main account name** field.</span></span>
-   <span data-ttu-id="a117a-117">**Konsolidierungskontogruppe** – Verwenden Sie dieses Feld, um die Gruppe anzugeben, der das Konto zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="a117a-117">**Consolidation account group** – Use this field to specify the group to assign the account to.</span></span> <span data-ttu-id="a117a-118">Wenn Sie auf zwei unterschiedliche Arten konsolidieren, müssen Sie dasselbe Konto allen vier Konsolidierungskontogruppen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="a117a-118">If you consolidate in two different ways, you must add the same account to all four consolidation account groups.</span></span>
-   <span data-ttu-id="a117a-119">**Konsolidierungskonto** – Geben Sie den Wert des Konsolidierungskontos ein.</span><span class="sxs-lookup"><span data-stu-id="a117a-119">**Consolidation account** – Enter the value of the consolidation account.</span></span> <span data-ttu-id="a117a-120">Dieser Wert muss kein Konto in einem Kontenplan. sein</span><span class="sxs-lookup"><span data-stu-id="a117a-120">This value doesn't have to be an account from a chart of accounts.</span></span> <span data-ttu-id="a117a-121">Es kann jeder Wert sein, den Sie benötigen.</span><span class="sxs-lookup"><span data-stu-id="a117a-121">It can be any value that you require.</span></span>
-   <span data-ttu-id="a117a-122">**Konsolidierungskontoname**– Geben Sie den Namen des Kontos an, das auf Anfragen und Berichten angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a117a-122">**Consolidation account name** – Enter the name of account as you want it to appear on inquiries and reports.</span></span>
-   <span data-ttu-id="a117a-123">**Sat-Ebene**– Dieses Feld wird verwendet, um Kontoauszüge der mexikanischen Steuerbehörde zu melden.</span><span class="sxs-lookup"><span data-stu-id="a117a-123">**SAT level** – This field is used to report account statements to the Mexican tax authorities.</span></span> 

<span data-ttu-id="a117a-124">Wenn Sie mit dem Erstellen der Konsolidierungskontogruppen und der zusätzlichen Konsolidierungskonten fertig sind, können Sie die Gruppe im Oline-Konsolidierungsprozess auswählen.</span><span class="sxs-lookup"><span data-stu-id="a117a-124">When you've finished creating your consolidation account groups and additional consolidation accounts, you can select the group in the Consolidate online process.</span></span>


<span data-ttu-id="a117a-125">Weitere Informationen finden Sie unter [Konsolidierungsgruppen und zusätzliche Konsolidierungskonten erstellen](../general-ledger/tasks/create-consolidation-groups.md)</span><span class="sxs-lookup"><span data-stu-id="a117a-125">For more information, see [Create consolidation groups and additional consolidation accounts](../general-ledger/tasks/create-consolidation-groups.md).</span></span> 




