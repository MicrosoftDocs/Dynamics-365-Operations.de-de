--- 
title: " Eine Arbeitskraft konfigurieren"
description: "Dieses Verfahren zeigt, wie eine Einzelhandelsarbeitskraft als Verkäufer konfiguriert wird, der im POS für Provisionen freigegeben ist."
author: jblucher
manager: AnnBe
ms.date: 02/22/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: 721c075aa7bbe9d1ed439a84cae907e3db3aafa8
ms.contentlocale: de-de
ms.lasthandoff: 01/19/2018

---
# <a name="configure-a-worker"></a><span data-ttu-id="1a5cb-103"> Eine Arbeitskraft konfigurieren</span><span class="sxs-lookup"><span data-stu-id="1a5cb-103">Configure a worker</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="1a5cb-104">Dieses Verfahren zeigt, wie eine Einzelhandelsarbeitskraft als Verkäufer konfiguriert wird, der im POS für Provisionen freigegeben ist.</span><span class="sxs-lookup"><span data-stu-id="1a5cb-104">This procedure demonstrates how to configure a retail worker as a sales representative who is eligible for commission on sales in POS.</span></span> <span data-ttu-id="1a5cb-105">Für diese Prozedur wird das Demo-Datenunternehmen USRT verwendet.</span><span class="sxs-lookup"><span data-stu-id="1a5cb-105">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-commission-sales-group-for-the-worker"></a><span data-ttu-id="1a5cb-106">Verkaufsprovisionsgruppe für die Arbeitskraft erstellen</span><span class="sxs-lookup"><span data-stu-id="1a5cb-106">Create a commission sales group for the worker</span></span>
1. <span data-ttu-id="1a5cb-107">Wechseln Sie zu Vertrieb und Marketing > Provisionen > Vertriebsgruppen.</span><span class="sxs-lookup"><span data-stu-id="1a5cb-107">Go to Sales and marketing > Commissions > Sales groups.</span></span>
    * <span data-ttu-id="1a5cb-108">Arbeitskräfte können mindestens einer Verkaufsgruppe zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="1a5cb-108">Workers can be assigned to one or more sales groups.</span></span> <span data-ttu-id="1a5cb-109">In POS können Sie eine Verkaufsgruppe auswählen, die den Arbeitskräften des Adressbuchs des Shops enthält.</span><span class="sxs-lookup"><span data-stu-id="1a5cb-109">In POS, you can choose any sales group that contains workers from the store's address book.</span></span>  
2. <span data-ttu-id="1a5cb-110">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="1a5cb-110">Click New.</span></span>
3. <span data-ttu-id="1a5cb-111">Geben Sie im Feld "Gruppe" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="1a5cb-111">In the Group field, type a value.</span></span>
4. <span data-ttu-id="1a5cb-112">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="1a5cb-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="1a5cb-113">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="1a5cb-113">Click Save.</span></span>
6. <span data-ttu-id="1a5cb-114">Klicken Sie im Aktivitätsbereich auf "Allgemein".</span><span class="sxs-lookup"><span data-stu-id="1a5cb-114">On the Action Pane, click General.</span></span>
7. <span data-ttu-id="1a5cb-115">Klicken Sie auf "Verkäufer".</span><span class="sxs-lookup"><span data-stu-id="1a5cb-115">Click Sales rep.</span></span>
    * <span data-ttu-id="1a5cb-116">Eine Verkaufsgruppe kann mehr als einer Arbeitskraft enthalten.</span><span class="sxs-lookup"><span data-stu-id="1a5cb-116">A sales group can contain more than one worker.</span></span> <span data-ttu-id="1a5cb-117">Provisionen können aufgeteilt werden zwischen Arbeitskräften basierend auf dem, was Sie in der Provisionsfreigabe definieren.</span><span class="sxs-lookup"><span data-stu-id="1a5cb-117">Commissions can be split between workers based on how you define the commission share.</span></span>  
8. <span data-ttu-id="1a5cb-118">Geben Sie im Feld "Name" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="1a5cb-118">In the Name field, enter or select a value.</span></span>
9. <span data-ttu-id="1a5cb-119">Geben Sie im Feld 'Provisionsanteil' eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="1a5cb-119">In the Commission share field, enter a number.</span></span>
10. <span data-ttu-id="1a5cb-120">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="1a5cb-120">Click Save.</span></span>
11. <span data-ttu-id="1a5cb-121">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="1a5cb-121">Close the page.</span></span>
12. <span data-ttu-id="1a5cb-122">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="1a5cb-122">Close the page.</span></span>

## <a name="assign-the-workers-default-sales-group"></a><span data-ttu-id="1a5cb-123">Standardverkaufsgruppe der Arbeitskraft zuweisen</span><span class="sxs-lookup"><span data-stu-id="1a5cb-123">Assign the workers default sales group</span></span>
1. <span data-ttu-id="1a5cb-124">Navigieren Sie zu Einzelhandel und Handel > Mitarbeiter > Arbeitskräfte.</span><span class="sxs-lookup"><span data-stu-id="1a5cb-124">Go to Retail and commerce > Employees > Workers.</span></span>
2. <span data-ttu-id="1a5cb-125">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="1a5cb-125">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="1a5cb-126">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="1a5cb-126">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="1a5cb-127">Klicken Sie auf die Registerkarte Einzelhandel.</span><span class="sxs-lookup"><span data-stu-id="1a5cb-127">Click the Retail tab.</span></span>
    * <span data-ttu-id="1a5cb-128">Eine Arbeitskraft kann einer Standardverkaufsgruppe zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="1a5cb-128">A worker can be assigned to a default sales group.</span></span> <span data-ttu-id="1a5cb-129">Die Standardverkaufsgruppe wird automatisch zu Verkaufspositionen in POS hinzugefügt, wenn die Option im Funktionsprofil für die Filiale aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="1a5cb-129">The default sales group will be automatically added to sales lines in POS if the option is enabled in the functionality profile for the store.</span></span>  
5. <span data-ttu-id="1a5cb-130">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="1a5cb-130">Click Edit.</span></span>
6. <span data-ttu-id="1a5cb-131">Geben Sie im Feld "Standardgruppe" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="1a5cb-131">In the Default group field, enter or select a value.</span></span>
7. <span data-ttu-id="1a5cb-132">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="1a5cb-132">Click Save.</span></span>


