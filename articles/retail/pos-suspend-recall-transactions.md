---
title: Transaktionen in der Verkaufsstelle (POS) anhalten und fortsetzen
description: "In diesem Thema wird erläutert, wie Transaktionen unterbrochen und später fortgesetzt werden können oder sie in einem anderen Register fortsetzen können mithilfe von Microsoft Dynamics 365 for Retail."
author: jblucher
manager: AnnBe
ms.date: 11/27/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 261234
ms.assetid: 7cd68ecc-cc09-48ab-8cb8-48d5c304effa
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: ffb04609318c7de4b9ef729a8e03a7f9395806b8
ms.contentlocale: de-de
ms.lasthandoff: 01/04/2019

---

# <a name="suspend-and-resume-transactions-in-the-point-of-sale-pos"></a><span data-ttu-id="ba1bb-103">Transaktionen in der Verkaufsstelle (POS) anhalten und fortsetzen</span><span class="sxs-lookup"><span data-stu-id="ba1bb-103">Suspend and resume transactions in the point of sale (POS)</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="ba1bb-104">Benutzer von Verkaufsstelle (POS) können laufende Buchungen unterbrechen und sie später fortsetzen oder in einem anderen Register fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="ba1bb-104">Point of sale (POS) users can suspend in-progress transactions, and then resume them later or on a different register.</span></span> <span data-ttu-id="ba1bb-105">Buchungen erfolgen häufig unterbrochen, um ein Register für eine andere Aufgabe schnell freizugeben, ohne einen Status für die aktuelle Buchung zu verlieren.</span><span class="sxs-lookup"><span data-stu-id="ba1bb-105">Transactions are often suspended to quickly free up a register for a different task without losing any progress on the current transaction.</span></span> <span data-ttu-id="ba1bb-106">Beispielsweis beginnt ein Shopangestellter eine Kundentransaktion auf einem mobilen Gerät aber muss diese an einer Kasste mit Geldlade ausführen.</span><span class="sxs-lookup"><span data-stu-id="ba1bb-106">For example, a store associate starts to process a customer's transaction on a mobile device but must complete it on a register that has a cash drawer.</span></span> <span data-ttu-id="ba1bb-107">In diesem Fall muss der Shop die Buchung im mobilen Gerät gestoppt werden und diese dann auf einer Kasse wieder aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="ba1bb-107">In this case, the store associate can suspend the transaction on the mobile device, and then recall and resume it on a register.</span></span>

## <a name="configure-suspend-and-resume-functionality"></a><span data-ttu-id="ba1bb-108">Funktionen unterbrechen und wieder aufnehmen konfigurieren</span><span class="sxs-lookup"><span data-stu-id="ba1bb-108">Configure suspend and resume functionality</span></span>

### <a name="pos-operations"></a><span data-ttu-id="ba1bb-109">POS-Vorgänge</span><span class="sxs-lookup"><span data-stu-id="ba1bb-109">POS operations</span></span>

<span data-ttu-id="ba1bb-110">Zwei [POS-Vorgängen](pos-operations.md) können die POS-Support Szenarien unterbrechen und fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="ba1bb-110">Two [POS operations](pos-operations.md) let the POS support suspend and resume scenarios.</span></span> <span data-ttu-id="ba1bb-111">Sie können diese Arbeitsgänge auf dem [Schaltflächenraster](pos-screen-layouts.md) der Buchungsseite oder der Willkommensseite zuweisen.</span><span class="sxs-lookup"><span data-stu-id="ba1bb-111">You can assign these operations to [button grids](pos-screen-layouts.md) on the transaction page or the welcome page.</span></span>

- <span data-ttu-id="ba1bb-112">503: Transaktion aussetzen</span><span class="sxs-lookup"><span data-stu-id="ba1bb-112">503: Suspend transaction</span></span>
- <span data-ttu-id="ba1bb-113">504: Transaktion zurückrufen</span><span class="sxs-lookup"><span data-stu-id="ba1bb-113">504: Recall transaction</span></span>

### <a name="receipt-template"></a><span data-ttu-id="ba1bb-114">Zugangsvorlage</span><span class="sxs-lookup"><span data-stu-id="ba1bb-114">Receipt template</span></span>

<span data-ttu-id="ba1bb-115">Der POS kann so konfiguriert werden, dass er einen gedruckten Beleg generiert, wenn eine Buchung unterbroche wird.</span><span class="sxs-lookup"><span data-stu-id="ba1bb-115">The POS can be configured to generate a printed slip when a transaction is suspended.</span></span> <span data-ttu-id="ba1bb-116">Dieser Beleg kann dann verwendet werden, um die Buchung zu erkennen und später zurückzurufen.</span><span class="sxs-lookup"><span data-stu-id="ba1bb-116">That slip can then be used to quickly identify and recall the transaction later.</span></span>

<span data-ttu-id="ba1bb-117">Um dem POS die Möglichkeit zu geben, einen Beleg zu drucken, müssen Sie das Belegformat **Transaktion unterbrechen** dem Shopprofil zuweisen.</span><span class="sxs-lookup"><span data-stu-id="ba1bb-117">To enable the POS to print a slip, you must add the **Suspended transaction** receipt format to the store's receipt profile.</span></span> <span data-ttu-id="ba1bb-118">Sie können das Belegformat entwerfen, dass bestimmte Details zur Transaktion enthält.</span><span class="sxs-lookup"><span data-stu-id="ba1bb-118">You can design the receipt format so that it includes or excludes specific details about the transaction.</span></span> <span data-ttu-id="ba1bb-119">Beispielsweise kann das Format eines Strichcodes enthalten, um das Scannen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ba1bb-119">For example, the format can include a barcode to support scanning.</span></span>

### <a name="receipt-numbering"></a><span data-ttu-id="ba1bb-120">Bonnummerierung</span><span class="sxs-lookup"><span data-stu-id="ba1bb-120">Receipt numbering</span></span>

<span data-ttu-id="ba1bb-121">Wei bei POS-Buchungs-Typen, die für einen gedruckten Beleg generiert wurden, können Sie einen Nummernkreis für unterbrochene Buchungen im Abschnitt **Belegnummerierung** des Funktionsprofils der Filiale definieren.</span><span class="sxs-lookup"><span data-stu-id="ba1bb-121">As for other POS transaction types that generate a printed receipt, you can define a number sequence for suspended transactions in the **Receipt numbering** section of the store's functionality profile.</span></span>

### <a name="void-when-closing-shift"></a><span data-ttu-id="ba1bb-122">Stornieren, wenn Schicht geschlossen wird</span><span class="sxs-lookup"><span data-stu-id="ba1bb-122">Void when closing shift</span></span>

<span data-ttu-id="ba1bb-123">Sie können **Stornieren Sie, wenn Schicht endet** Option verwenden, um festzulegen, dass Benutzer entweder alle unterbrochenen Buchungen unterbrechen oder stornieren, bevor sie ihre Schicht schließen.</span><span class="sxs-lookup"><span data-stu-id="ba1bb-123">You can use the **Void when closing shift** option to require that users either complete or void any suspended transactions before they close their shift.</span></span> <span data-ttu-id="ba1bb-124">Während dem **Schicht schließen** Arbeitsgangs forder der POS Benutzer auf, unterbrochene Buchungen anzuzeigen oder zu stornieren.</span><span class="sxs-lookup"><span data-stu-id="ba1bb-124">During the **Close shift** operation, the POS will prompt users to either view or void any outstanding suspended transactions.</span></span>

## <a name="suspend-and-resume-a-transaction"></a><span data-ttu-id="ba1bb-125">Transaktionen anhalten und fortsetzen</span><span class="sxs-lookup"><span data-stu-id="ba1bb-125">Suspend and resume a transaction</span></span>

### <a name="suspend-a-transaction"></a><span data-ttu-id="ba1bb-126">Transaktion aussetzen</span><span class="sxs-lookup"><span data-stu-id="ba1bb-126">Suspend a transaction</span></span>

<span data-ttu-id="ba1bb-127">Benutzer, die über die entsprechenden Rechte verfügen und die eingeben Bildschirmlayout haben, das den Arbeitsgang **Buchung aussetzen** enthält, können eine Buchung fortsetzen, damit sie an einer anderen Kasse später zurückgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="ba1bb-127">Users who have sufficient privileges, and who have a screen layout that includes the **Suspend transaction** operation, can suspend a transaction so that it can be recalled later or on a different register.</span></span>

<span data-ttu-id="ba1bb-128">Buchungen können unterbrochen werden, wenn sie **nicht** die folgenden Rückvergütungstypen enthalten:</span><span class="sxs-lookup"><span data-stu-id="ba1bb-128">Transactions can be suspended only if they do **not** contain the following types of lines:</span></span>

- <span data-ttu-id="ba1bb-129">Aktive Zahlungspositionen</span><span class="sxs-lookup"><span data-stu-id="ba1bb-129">Active payment lines</span></span>
- <span data-ttu-id="ba1bb-130">Geschenkkartepositionen (entweder eine Geschenkkarte ausstellen oder Geschenkkartensaldo hinzufügen)</span><span class="sxs-lookup"><span data-stu-id="ba1bb-130">Gift card lines (either to issue a gift card or to add to the gift card balance)</span></span>

<span data-ttu-id="ba1bb-131">Eine unterbrochene Buchung hat keine Verkaufsinformations- oder Bestandsverfügbarkeit-Informationen für den Shop.</span><span class="sxs-lookup"><span data-stu-id="ba1bb-131">A suspended transaction doesn't affect sales information or inventory availability information for the store.</span></span>

### <a name="resume-a-suspended-transaction"></a><span data-ttu-id="ba1bb-132">Ruft eine ausgesetzte Transaktion zurück.</span><span class="sxs-lookup"><span data-stu-id="ba1bb-132">Resume a suspended transaction</span></span>

<span data-ttu-id="ba1bb-133">Unterbrochene Transaktionen können in denselben Shop von jedem Benutzer erneut aufgerufen und fortgesetzt werden, der über die entsprechenden Rechte hat und der ebenfalls ein Layout, hat das den Arbeitsgang **Transaktlion zurückrufen** umfasst.</span><span class="sxs-lookup"><span data-stu-id="ba1bb-133">Suspended transactions can be recalled and resumed in the same store by any user who has sufficient privileges, and who also has a layout that includes the **Recall transaction** operation.</span></span>

<span data-ttu-id="ba1bb-134">Um schnell und einfach eine unterbrochene Buchung aufzurufen, scannen Sie den Strichcode auf dem gedruckten Beleg, während Sie die Liste der Buchungen vom Arbeitsgang anzeigen **Buchung zurückrufen**.</span><span class="sxs-lookup"><span data-stu-id="ba1bb-134">To quickly and easily recall a suspended transaction, scan the barcode on the printed slip while you're viewing the list of transactions from the **Recall transaction** operation.</span></span>

### <a name="considerations-for-offline-mode"></a><span data-ttu-id="ba1bb-135">Betrachtungen für Offlinemodus</span><span class="sxs-lookup"><span data-stu-id="ba1bb-135">Considerations for offline mode</span></span>

- <span data-ttu-id="ba1bb-136">Buchungen, die unterbrochen wurden, während der POS im Online-Modus ist, kann nicht im Offline-Modus fortgesetzt werden, weil die Daten nicht mit der Offline-Datenbank synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="ba1bb-136">Any transaction that is suspended while the POS is in online mode can't be resumed in offline mode, because the data isn't synced to the offline database.</span></span>
- <span data-ttu-id="ba1bb-137">Wenn Sie eine Buchung unterbrechen, während der POS im Offline-Modus ist, können Sie sie im Offline-Modus zurückrufen, vorausgesetzt, dass der Betrag vom POS nicht in rechnerabhängigem Betrieb geändert wurde, seit die Buchung unterbrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="ba1bb-137">If you suspend a transaction while the POS is in offline mode, you can recall it in offline mode, provided that the POS wasn't switched back to online mode at any time since you suspended the transaction.</span></span> <span data-ttu-id="ba1bb-138">Wenn der POS wieder im Online-Modus ist, werden die Daten zu unterbrochene Buchungen verschoben udn von der Offline-Datenbank entfernt.</span><span class="sxs-lookup"><span data-stu-id="ba1bb-138">When the POS is switched back to online mode, data about suspended transactions is moved to the online database and removed from the offline database.</span></span> <span data-ttu-id="ba1bb-139">Daher können Sie die Transaktionen nur im Online-Modus fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="ba1bb-139">Therefore, the transactions can be resumed only in online mode.</span></span> <span data-ttu-id="ba1bb-140">Wenn Sie vom POS wieder in den Offline-Modus wechseln, sind Sie nicht mehr in der Lage, die unterbrochene Transaktionen fortzusetzen, da sie bereits offline aus der Datenbank entfernt wurden.</span><span class="sxs-lookup"><span data-stu-id="ba1bb-140">If you switch the POS back to offline mode, you won't be able to resume those suspended transaction, because they have already been removed from the offline database.</span></span>

### <a name="void-a-suspended-transaction"></a><span data-ttu-id="ba1bb-141">Ausgesetzte Buchung stornieren</span><span class="sxs-lookup"><span data-stu-id="ba1bb-141">Void a suspended transaction</span></span>

<span data-ttu-id="ba1bb-142">Sie können unterbrochene Buchungen stornieren, indem Sie die Buchung zuerst erneut aufrufen und dann **Transaktion stornieren** ausführen oder die Buchung in der Liste **Transaktion zurückrufen** auswählen und **Storniert** auf der App-Leiste auswählen.</span><span class="sxs-lookup"><span data-stu-id="ba1bb-142">You can void suspended transactions either by recalling the transaction and then performing the **Void transaction** operation, or by selecting the transaction in the **Recall transaction** list and selecting **Void** on the app bar.</span></span> <span data-ttu-id="ba1bb-143">Alternativ kann der Shop konfiguriert werden, damit Benutzer aufgefordert werden, unterbrochene Transaktionen zu stornieren, wenn sie ihre Schicht schließen.</span><span class="sxs-lookup"><span data-stu-id="ba1bb-143">Alternatively, the store can be configured to prompt users to void suspended transactions when they close their shift.</span></span>
