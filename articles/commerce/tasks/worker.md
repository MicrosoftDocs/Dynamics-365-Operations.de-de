---
title: " Eine Arbeitskraft konfigurieren"
description: Diese Prozedur zeigt, wie eine Arbeitskraft als Verkäufer konfiguriert wird, der im POS für Provisionen freigegeben ist.
author: jblucher
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CommissionSalesGroup, CommissionSalesMember, DirPartyLookup, HcmWorker
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 120705200f223e31c72290059e8634e7db6f9fdd
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232616"
---
# <a name="configure-a-worker"></a><span data-ttu-id="0f8e6-103"> Eine Arbeitskraft konfigurieren</span><span class="sxs-lookup"><span data-stu-id="0f8e6-103">Configure a worker</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0f8e6-104">Diese Prozedur zeigt, wie eine Arbeitskraft als Verkäufer konfiguriert wird, der im POS für Provisionen freigegeben ist.</span><span class="sxs-lookup"><span data-stu-id="0f8e6-104">This procedure demonstrates how to configure a worker as a sales representative who is eligible for commission on sales in POS.</span></span> <span data-ttu-id="0f8e6-105">Für diese Prozedur wird das Demo-Datenunternehmen USRT verwendet.</span><span class="sxs-lookup"><span data-stu-id="0f8e6-105">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-commission-sales-group-for-the-worker"></a><span data-ttu-id="0f8e6-106">Verkaufsprovisionsgruppe für die Arbeitskraft erstellen</span><span class="sxs-lookup"><span data-stu-id="0f8e6-106">Create a commission sales group for the worker</span></span>
1. <span data-ttu-id="0f8e6-107">Wechseln Sie zu Vertrieb und Marketing > Provisionen > Vertriebsgruppen.</span><span class="sxs-lookup"><span data-stu-id="0f8e6-107">Go to Sales and marketing > Commissions > Sales groups.</span></span>
    * <span data-ttu-id="0f8e6-108">Arbeitskräfte können mindestens einer Verkaufsgruppe zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="0f8e6-108">Workers can be assigned to one or more sales groups.</span></span> <span data-ttu-id="0f8e6-109">In POS können Sie eine Verkaufsgruppe auswählen, die den Arbeitskräften des Adressbuchs des Shops enthält.</span><span class="sxs-lookup"><span data-stu-id="0f8e6-109">In POS, you can choose any sales group that contains workers from the store's address book.</span></span>  
2. <span data-ttu-id="0f8e6-110">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="0f8e6-110">Click New.</span></span>
3. <span data-ttu-id="0f8e6-111">Geben Sie im Feld "Gruppe" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="0f8e6-111">In the Group field, type a value.</span></span>
4. <span data-ttu-id="0f8e6-112">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="0f8e6-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="0f8e6-113">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="0f8e6-113">Click Save.</span></span>
6. <span data-ttu-id="0f8e6-114">Klicken Sie im Aktivitätsbereich auf "Allgemein".</span><span class="sxs-lookup"><span data-stu-id="0f8e6-114">On the Action Pane, click General.</span></span>
7. <span data-ttu-id="0f8e6-115">Klicken Sie auf "Verkäufer".</span><span class="sxs-lookup"><span data-stu-id="0f8e6-115">Click Sales rep.</span></span>
    * <span data-ttu-id="0f8e6-116">Eine Verkaufsgruppe kann mehr als einer Arbeitskraft enthalten.</span><span class="sxs-lookup"><span data-stu-id="0f8e6-116">A sales group can contain more than one worker.</span></span> <span data-ttu-id="0f8e6-117">Provisionen können aufgeteilt werden zwischen Arbeitskräften basierend auf dem, was Sie in der Provisionsfreigabe definieren.</span><span class="sxs-lookup"><span data-stu-id="0f8e6-117">Commissions can be split between workers based on how you define the commission share.</span></span>  
8. <span data-ttu-id="0f8e6-118">Geben Sie im Feld "Name" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="0f8e6-118">In the Name field, enter or select a value.</span></span>
9. <span data-ttu-id="0f8e6-119">Geben Sie im Feld 'Provisionsanteil' eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="0f8e6-119">In the Commission share field, enter a number.</span></span>
10. <span data-ttu-id="0f8e6-120">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="0f8e6-120">Click Save.</span></span>
11. <span data-ttu-id="0f8e6-121">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="0f8e6-121">Close the page.</span></span>
12. <span data-ttu-id="0f8e6-122">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="0f8e6-122">Close the page.</span></span>

## <a name="assign-the-workers-default-sales-group"></a><span data-ttu-id="0f8e6-123">Standardverkaufsgruppe der Arbeitskraft zuweisen</span><span class="sxs-lookup"><span data-stu-id="0f8e6-123">Assign the workers default sales group</span></span>
1. <span data-ttu-id="0f8e6-124">Navigieren Sie zu Einzelhandel und Handel > Mitarbeiter > Arbeitskräfte.</span><span class="sxs-lookup"><span data-stu-id="0f8e6-124">Go to Retail and Commerce > Employees > Workers.</span></span>
2. <span data-ttu-id="0f8e6-125">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="0f8e6-125">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="0f8e6-126">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="0f8e6-126">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="0f8e6-127">Klicken Sie auf die Registerkarte Commerce.</span><span class="sxs-lookup"><span data-stu-id="0f8e6-127">Click the Commerce tab.</span></span>
    * <span data-ttu-id="0f8e6-128">Eine Arbeitskraft kann einer Standardverkaufsgruppe zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="0f8e6-128">A worker can be assigned to a default sales group.</span></span> <span data-ttu-id="0f8e6-129">Die Standardverkaufsgruppe wird automatisch zu Verkaufspositionen in POS hinzugefügt, wenn die Option im Funktionsprofil für die Filiale aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="0f8e6-129">The default sales group will be automatically added to sales lines in POS if the option is enabled in the functionality profile for the store.</span></span>  
5. <span data-ttu-id="0f8e6-130">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="0f8e6-130">Click Edit.</span></span>
6. <span data-ttu-id="0f8e6-131">Geben Sie im Feld "Standardgruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="0f8e6-131">In the Default group field, enter or select a value.</span></span>
7. <span data-ttu-id="0f8e6-132">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="0f8e6-132">Click Save.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]