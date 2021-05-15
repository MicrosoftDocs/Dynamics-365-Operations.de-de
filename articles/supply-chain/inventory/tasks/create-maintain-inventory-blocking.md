---
title: Dient zum Erstellen und Verwalten einer Sperrung von Lagerbestand
description: Dieses Thema beschreibt, wie Sie eine Bestandssperre verwenden können, um zu verhindern, dass physische Lagerbestände durch andere ausgehende Quelldokumente reserviert werden.
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e9aa38ca52da577fff258bb330922ad7f4044330
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956157"
---
# <a name="create-and-maintain-an-inventory-blocking"></a><span data-ttu-id="798bb-103">Dient zum Erstellen und Verwalten einer Sperrung von Lagerbestand</span><span class="sxs-lookup"><span data-stu-id="798bb-103">Create and maintain an inventory blocking</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="798bb-104">Dieses Thema beschreibt, wie Sie eine Bestandssperre verwenden können, um zu verhindern, dass physische Lagerbestände durch andere ausgehende Quelldokumente reserviert werden.</span><span class="sxs-lookup"><span data-stu-id="798bb-104">This topic describes how to use an inventory blocking to prevent physical on-hand inventory from being reserved by other outbound source documents.</span></span> <span data-ttu-id="798bb-105">Bevor Sie die Vorgänge in diesem Thema starten, müssen Sie ein Element haben, für das physischer Lagerbestand vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="798bb-105">Before you start the procedures in this topic, you must have an item that physical on-hand inventory is available for.</span></span>

## <a name="block-inventory"></a><span data-ttu-id="798bb-106">Lagerbestand sperren</span><span class="sxs-lookup"><span data-stu-id="798bb-106">Block inventory</span></span>

<span data-ttu-id="798bb-107">Um einen Datensatz zur Bestandssperrung zu erstellen, so dass der Bestand gesperrt wird, folgen Sie diesen Schritten.</span><span class="sxs-lookup"><span data-stu-id="798bb-107">To create an inventory blocking record so that inventory is blocked, follow these steps.</span></span>

1. <span data-ttu-id="798bb-108">Gehen Sie zu **Bestandsverwaltung \> Periodische Aufgaben \> Bestandssperrung**.</span><span class="sxs-lookup"><span data-stu-id="798bb-108">Go to **Inventory management \> Periodic tasks \> Inventory blocking**.</span></span>
1. <span data-ttu-id="798bb-109">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="798bb-109">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="798bb-110">Legen Sie in der Kopfzeile des neuen Bestandssperrungs-Datensatzes das Feld **Elementnummer** auf das Element fest, das Sie sperren wollen, und geben Sie eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="798bb-110">On the header of the new blocking record, set the **Item number** field to the item that you want to block, and enter a description.</span></span>
1. <span data-ttu-id="798bb-111">Geben Sie auf der Registerkarte **Allgemein** Inforegister im Feld **Menge** die Anzahl der zu blockierenden Elemente ein.</span><span class="sxs-lookup"><span data-stu-id="798bb-111">On the **General** FastTab, in the **Quantity** field, enter the number of items to block.</span></span>
1. <span data-ttu-id="798bb-112">Geben Sie auf dem Inforegister **Bestandsdimensionen** den Standort und den Lagerort an, an dem sich die zu sperrenden Elemente derzeit befinden.</span><span class="sxs-lookup"><span data-stu-id="798bb-112">On the **Inventory dimensions** FastTab, specify the site and warehouse where the items that you want to block are currently located.</span></span>
1. <span data-ttu-id="798bb-113">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="798bb-113">On the Action Pane, select **Save**.</span></span>

## <a name="update-the-conditions-of-the-inventory-blocking"></a><span data-ttu-id="798bb-114">Aktualisieren Sie die Bedingungen der Sperrung von Lagerbestand</span><span class="sxs-lookup"><span data-stu-id="798bb-114">Update the conditions of the inventory blocking</span></span>

<span data-ttu-id="798bb-115">Um einen Datensatz zur Bestandssperrung zu aktualisieren, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="798bb-115">To update an inventory blocking record, follow these steps.</span></span>

1. <span data-ttu-id="798bb-116">Gehen Sie zu **Bestandsverwaltung \> Periodische Aufgaben \> Bestandssperrung**.</span><span class="sxs-lookup"><span data-stu-id="798bb-116">Go to **Inventory management \> Periodic tasks \> Inventory blocking**.</span></span>
1. <span data-ttu-id="798bb-117">Wählen Sie im Listenbereich den entsprechenden Bestandssperrungs-Datensatz aus.</span><span class="sxs-lookup"><span data-stu-id="798bb-117">In the list pane, select the relevant blocking record.</span></span>
1. <span data-ttu-id="798bb-118">Bearbeiten Sie den Datensatz wie gewünscht.</span><span class="sxs-lookup"><span data-stu-id="798bb-118">Edit the record as required.</span></span> <span data-ttu-id="798bb-119">Sie können z. B. den Wert des Feldes **Erwartetes Datum** ändern, um anzugeben, wann der gesperrte Bestand voraussichtlich für die Reservierung verfügbar sein wird.</span><span class="sxs-lookup"><span data-stu-id="798bb-119">For example, you might change the value of the **Expected date** field to indicate when the blocked inventory is expected to become available for reservation.</span></span> <span data-ttu-id="798bb-120">Wenn die Option **Erwartete Zugänge** ausgewählt ist, wird das Datum auf der erwarteten Transaktion angezeigt.</span><span class="sxs-lookup"><span data-stu-id="798bb-120">If the **Expected receipts** option is selected, the date will appear on the expected transaction.</span></span> <span data-ttu-id="798bb-121">(Die Option **Erwartete Zugänge** ist standardmäßig ausgewählt, wenn Sie einen Datensatz für die Bestandssperrung manuell erstellen.)</span><span class="sxs-lookup"><span data-stu-id="798bb-121">(The **Expected receipts** option is selected by default when you manually create a blocking record.)</span></span>
1. <span data-ttu-id="798bb-122">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="798bb-122">On the Action Pane, select **Save**.</span></span>

## <a name="unblock-inventory"></a><span data-ttu-id="798bb-123">Bestand entsperren</span><span class="sxs-lookup"><span data-stu-id="798bb-123">Unblock inventory</span></span>

<span data-ttu-id="798bb-124">Um einen Bestandssperrungs-Datensatz zu entfernen, so dass der Bestand freigegeben wird, gehen Sie wie folgt vor.</span><span class="sxs-lookup"><span data-stu-id="798bb-124">To remove an inventory blocking record so that inventory is unblocked, follow these steps.</span></span>

1. <span data-ttu-id="798bb-125">Gehen Sie zu **Bestandsverwaltung \> Periodische Aufgaben \> Bestandssperrung**.</span><span class="sxs-lookup"><span data-stu-id="798bb-125">Go to **Inventory management \> Periodic tasks \> Inventory blocking**.</span></span>
1. <span data-ttu-id="798bb-126">Wählen Sie im Listenbereich den entsprechenden Bestandssperrungs-Datensatz aus.</span><span class="sxs-lookup"><span data-stu-id="798bb-126">In the list pane, select the relevant blocking record.</span></span>
1. <span data-ttu-id="798bb-127">Wählen Sie im Aktivitätsbereich **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="798bb-127">On the Action Pane, select **Delete**.</span></span>
1. <span data-ttu-id="798bb-128">Sie werden aufgefordert, den Vorgang zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="798bb-128">You're prompted to confirm the operation.</span></span> <span data-ttu-id="798bb-129">Wählen Sie **Ja** aus, um fortzufahren.</span><span class="sxs-lookup"><span data-stu-id="798bb-129">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="798bb-130">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="798bb-130">Close the page.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
