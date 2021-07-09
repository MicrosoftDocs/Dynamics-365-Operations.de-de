---
title: Globale Bestandsbuchhaltung Sachkonto
description: Dieses Thema beschreibt die Sachkonten der Globalen Bestandsbuchhaltung, die durch eine Kombination aus einer Währung, einem Kalender, einer Konvention und einer Zuordnung zu einer juristischen Entität definiert sind.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ea3434675aa3b7f2304be93ef9b489747994fa9d
ms.sourcegitcommit: eceae470f4ae58000ec33fea34db34b7a7a1af43
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273160"
---
# <a name="global-inventory-accounting-ledger"></a><span data-ttu-id="de0c4-103">Globale Bestandsbuchhaltung Sachkonto</span><span class="sxs-lookup"><span data-stu-id="de0c4-103">Global Inventory Accounting ledger</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="de0c4-104">Die Globale Bestandsbuchhaltung hat ihre eigenen Sachkonten festgelegt.</span><span class="sxs-lookup"><span data-stu-id="de0c4-104">Global Inventory Accounting has its own set of ledgers.</span></span> <span data-ttu-id="de0c4-105">Jedes Mal, wenn eine bestandsbezogene Transaktion für eine relevante juristische Entität verarbeitet wird, kann das System diese Transaktion in einer beliebigen Anzahl von Sachkonten der Globalen Bestandsbuchhaltung verbuchen.</span><span class="sxs-lookup"><span data-stu-id="de0c4-105">Each time an inventory-related transaction is processed for a relevant legal entity, the system can account for that transaction in any number of Global Inventory Accounting ledgers, as required.</span></span>

<span data-ttu-id="de0c4-106">Ein Sachkonto ist ein Register mit Soll- und Haben-Messungen.</span><span class="sxs-lookup"><span data-stu-id="de0c4-106">A ledger is a register of debit and credit measures.</span></span> <span data-ttu-id="de0c4-107">Diese Kennzahlen werden mit Hilfe von Kostenarten und untergeordneten Sachkonten klassifiziert.</span><span class="sxs-lookup"><span data-stu-id="de0c4-107">These measures are classified by using cost elements and subledger accounts.</span></span> <span data-ttu-id="de0c4-108">Ein Sachkonto in der Globalen Bestandsbuchhaltung ist durch die Kombination einer Währung, eines Kalenders, einer Konvention und einer Zuordnung zu einer juristischen Entität definiert.</span><span class="sxs-lookup"><span data-stu-id="de0c4-108">A Global Inventory Accounting ledger is defined by its combination of a currency, a calendar, a convention, and an association with a legal entity.</span></span>

<span data-ttu-id="de0c4-109">Um Ihre Globale Bestandsbuchhaltung-Ledger einzurichten, gehen Sie auf **Globale Bestandsbuchhaltung \> Einrichten \> Globale Bestandsbuchhaltung-Ledger**.</span><span class="sxs-lookup"><span data-stu-id="de0c4-109">To set up your Global Inventory Accounting ledgers, go to **Global inventory accounting \> Setup \> Global inventory accounting ledgers**.</span></span> <span data-ttu-id="de0c4-110">Legen Sie für jedes Sachkonto die folgenden Felder fest:</span><span class="sxs-lookup"><span data-stu-id="de0c4-110">For each ledger, set the following fields:</span></span>

- <span data-ttu-id="de0c4-111">**Name** – Geben Sie den Namen des Sachkontos ein.</span><span class="sxs-lookup"><span data-stu-id="de0c4-111">**Name** – Enter the name of the ledger.</span></span>
- <span data-ttu-id="de0c4-112">**Beschreibung** – Geben Sie eine Beschreibung für das Sachkonto ein.</span><span class="sxs-lookup"><span data-stu-id="de0c4-112">**Description** – Enter a description of the ledger.</span></span>
- <span data-ttu-id="de0c4-113">**Fiskalkalender** – Geben Sie den Fiskalkalender für das Ledger an.</span><span class="sxs-lookup"><span data-stu-id="de0c4-113">**Fiscal calendar** – Specify the fiscal calendar for the ledger.</span></span>
- <span data-ttu-id="de0c4-114">**Währung und Exchange-Typ** – Verwenden Sie die Felder in diesem Inforegister, um die Buchhaltungswährung, die das Sachkonto verwendet, und den Exchange-Typ auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="de0c4-114">**Currency and exchange rate type** – Use the fields on this FastTab to select the accounting currency that the ledger uses, and the exchange rate type.</span></span> <span data-ttu-id="de0c4-115">Die von Ihnen gewählte Währung kann sich von der Währung der juristischen Entität unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="de0c4-115">The currency that you select can differ from the currency that the legal entity uses.</span></span> <span data-ttu-id="de0c4-116">In der Globalen Bestandsbuchhaltung können Benutzer so viele Sachkonten für die Kalkulation definieren, wie sie benötigen.</span><span class="sxs-lookup"><span data-stu-id="de0c4-116">In Global Inventory Accounting, users can define as many costing ledgers as they require.</span></span> <span data-ttu-id="de0c4-117">Die Globale Bestandsbuchhaltung unterstützt die Bestandsbuchhaltung in mehreren Währungen und in mehreren Bewertungen.</span><span class="sxs-lookup"><span data-stu-id="de0c4-117">Global Inventory Accounting supports inventory accounting in multiple currencies and in multiple valuations.</span></span> <span data-ttu-id="de0c4-118">Stellen Sie die folgenden Felder ein:</span><span class="sxs-lookup"><span data-stu-id="de0c4-118">Set the following fields:</span></span>

    - <span data-ttu-id="de0c4-119">**Währung** – Wählen Sie die Kalkulationswährung, in der bestandsbezogene Werte geführt werden.</span><span class="sxs-lookup"><span data-stu-id="de0c4-119">**Currency** – Select the costing currency that inventory-related values are maintained in.</span></span> <span data-ttu-id="de0c4-120">Zu diesen Werten gehören der Bestandswert, die Kosten der verkauften Waren, die Bestände in Zustellung und alle Arten von Abweichungen.</span><span class="sxs-lookup"><span data-stu-id="de0c4-120">These values include the inventory value, cost of goods sold, inventory in transit, and all kinds of variance.</span></span>
    - <span data-ttu-id="de0c4-121">**Wechselkurstyp** – Wählen Sie den Wechselkurs, den das System verwenden soll, um den Transaktionsbetrag in der Transaktionswährung und die Standardkosten der Elemente in die Kalkulationswährung umzurechnen.</span><span class="sxs-lookup"><span data-stu-id="de0c4-121">**Exchange rate type** – Select the exchange rate that the system should use to convert the transaction amount in the transaction currency and the standard cost of the items into the costing currency.</span></span>

- <span data-ttu-id="de0c4-122">**Konventionsname** – Geben Sie eine Konvention an.</span><span class="sxs-lookup"><span data-stu-id="de0c4-122">**Convention name** – Specify a convention.</span></span> <span data-ttu-id="de0c4-123">Eine Konvention ist eine Sammlung von Richtlinien, die festlegen, wie Kosten in diesem Sachkonto kalkuliert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="de0c4-123">A convention is a collection of policies that establish how costs will be accounted in this ledger.</span></span>
- <span data-ttu-id="de0c4-124">**Rechtliche Entität** – Das Sachkonto verbucht die Belege, die auf die ausgewählte juristische Entität gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="de0c4-124">**Legal entity** – The ledger will account the documents that are posted to the selected legal entity.</span></span>
- <span data-ttu-id="de0c4-125">**Priming** – Wählen Sie aus, ob Transaktionen im Bestand, die erstellt wurden, bevor das Sachkonto erstellt wurde, gemäß der Währung und Konvention im Ledger verarbeitet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="de0c4-125">**Priming** – Select whether inventory transactions that were created before the ledger was created should be processed according to the currency and convention in the ledger.</span></span> <span data-ttu-id="de0c4-126">Wählen Sie einen der folgenden Werte aus:</span><span class="sxs-lookup"><span data-stu-id="de0c4-126">Select one of the following values:</span></span>

    - <span data-ttu-id="de0c4-127">**Aktiviert** – Das Sachkonto soll Transaktionen verarbeiten, die erstellt wurden, bevor das Ledger erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="de0c4-127">**Activated** – The ledger should process transactions that were created before the ledger was created.</span></span>
    - <span data-ttu-id="de0c4-128">**Deaktiviert** – Das Sachkonto soll nur Transaktionen verarbeiten, die erstellt wurden, nachdem das Ledger erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="de0c4-128">**Deactivated** – The ledger should process only transactions that are created after the ledger was created.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="de0c4-129">Sie können **nicht** zurückkommen und dieses Feld festlegen, nachdem Sie neue Belege eingegeben haben.</span><span class="sxs-lookup"><span data-stu-id="de0c4-129">You will **not** be able to come back and set this field after you enter new documents.</span></span>

- <span data-ttu-id="de0c4-130">**Status** – Das System legt den Status von neu erstellten Sachkonten automatisch auf *Vorbereiten* fest.</span><span class="sxs-lookup"><span data-stu-id="de0c4-130">**Status** – The system automatically sets the status of newly created ledgers to *Prepare*.</span></span>
