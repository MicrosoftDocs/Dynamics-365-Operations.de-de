---
title: Transaktionen in der Verkaufsstelle (POS) anhalten und fortsetzen
description: In diesem Thema wird erläutert, wie Benutzer laufende Transaktionen aussetzen und sie später oder in einem anderen Register mit Dynamics 365 Commerce wiederaufnehmen können.
author: jblucher
manager: AnnBe
ms.date: 11/27/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: 261234
ms.assetid: 7cd68ecc-cc09-48ab-8cb8-48d5c304effa
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: fb92de200690b03a55a3a173fd433478c8e3175d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5231271"
---
# <a name="suspend-and-resume-a-transaction-in-the-point-of-sale-pos"></a><span data-ttu-id="56e9a-103">Transaktionen in der Verkaufsstelle (POS) anhalten und fortsetzen</span><span class="sxs-lookup"><span data-stu-id="56e9a-103">Suspend and resume a transaction in the point of sale (POS)</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="56e9a-104">Benutzer von Verkaufsstelle (POS) können laufende Buchungen unterbrechen und sie später fortsetzen oder in einem anderen Register fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="56e9a-104">Point of sale (POS) users can suspend in-progress transactions, and then resume them later or on a different register.</span></span> <span data-ttu-id="56e9a-105">Buchungen erfolgen häufig unterbrochen, um ein Register für eine andere Aufgabe schnell freizugeben, ohne einen Status für die aktuelle Buchung zu verlieren.</span><span class="sxs-lookup"><span data-stu-id="56e9a-105">Transactions are often suspended to quickly free up a register for a different task without losing any progress on the current transaction.</span></span> <span data-ttu-id="56e9a-106">Beispielsweis beginnt ein Shopangestellter eine Kundentransaktion auf einem mobilen Gerät aber muss diese an einer Kasste mit Geldlade ausführen.</span><span class="sxs-lookup"><span data-stu-id="56e9a-106">For example, a store associate starts to process a customer's transaction on a mobile device but must complete it on a register that has a cash drawer.</span></span> <span data-ttu-id="56e9a-107">In diesem Fall muss der Shop die Buchung im mobilen Gerät gestoppt werden und diese dann auf einer Kasse wieder aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="56e9a-107">In this case, the store associate can suspend the transaction on the mobile device, and then recall and resume it on a register.</span></span>

## <a name="configure-suspend-and-resume-functionality"></a><span data-ttu-id="56e9a-108">Funktionen unterbrechen und wieder aufnehmen konfigurieren</span><span class="sxs-lookup"><span data-stu-id="56e9a-108">Configure suspend and resume functionality</span></span>

### <a name="pos-operations"></a><span data-ttu-id="56e9a-109">POS-Vorgänge</span><span class="sxs-lookup"><span data-stu-id="56e9a-109">POS operations</span></span>

<span data-ttu-id="56e9a-110">Zwei [POS-Vorgängen](pos-operations.md) können die POS-Support Szenarien unterbrechen und fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="56e9a-110">Two [POS operations](pos-operations.md) let the POS support suspend and resume scenarios.</span></span> <span data-ttu-id="56e9a-111">Sie können diese Arbeitsgänge auf dem [Schaltflächenraster](pos-screen-layouts.md) der Buchungsseite oder der Willkommensseite zuweisen.</span><span class="sxs-lookup"><span data-stu-id="56e9a-111">You can assign these operations to [button grids](pos-screen-layouts.md) on the transaction page or the welcome page.</span></span>

- <span data-ttu-id="56e9a-112">503: Transaktion aussetzen</span><span class="sxs-lookup"><span data-stu-id="56e9a-112">503: Suspend transaction</span></span>
- <span data-ttu-id="56e9a-113">504: Transaktion zurückrufen</span><span class="sxs-lookup"><span data-stu-id="56e9a-113">504: Recall transaction</span></span>

### <a name="receipt-template"></a><span data-ttu-id="56e9a-114">Zugangsvorlage</span><span class="sxs-lookup"><span data-stu-id="56e9a-114">Receipt template</span></span>

<span data-ttu-id="56e9a-115">Der POS kann so konfiguriert werden, dass er einen gedruckten Beleg generiert, wenn eine Buchung unterbroche wird.</span><span class="sxs-lookup"><span data-stu-id="56e9a-115">The POS can be configured to generate a printed slip when a transaction is suspended.</span></span> <span data-ttu-id="56e9a-116">Dieser Beleg kann dann verwendet werden, um die Buchung zu erkennen und später zurückzurufen.</span><span class="sxs-lookup"><span data-stu-id="56e9a-116">That slip can then be used to quickly identify and recall the transaction later.</span></span>

<span data-ttu-id="56e9a-117">Um dem POS die Möglichkeit zu geben, einen Beleg zu drucken, müssen Sie das Belegformat **Transaktion unterbrechen** dem Shopprofil zuweisen.</span><span class="sxs-lookup"><span data-stu-id="56e9a-117">To enable the POS to print a slip, you must add the **Suspended transaction** receipt format to the store's receipt profile.</span></span> <span data-ttu-id="56e9a-118">Sie können das Belegformat entwerfen, dass bestimmte Details zur Transaktion enthält.</span><span class="sxs-lookup"><span data-stu-id="56e9a-118">You can design the receipt format so that it includes or excludes specific details about the transaction.</span></span> <span data-ttu-id="56e9a-119">Beispielsweise kann das Format eines Strichcodes enthalten, um das Scannen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="56e9a-119">For example, the format can include a barcode to support scanning.</span></span>

### <a name="receipt-numbering"></a><span data-ttu-id="56e9a-120">Bonnummerierung</span><span class="sxs-lookup"><span data-stu-id="56e9a-120">Receipt numbering</span></span>

<span data-ttu-id="56e9a-121">Wei bei POS-Buchungs-Typen, die für einen gedruckten Beleg generiert wurden, können Sie einen Nummernkreis für unterbrochene Buchungen im Abschnitt **Belegnummerierung** des Funktionsprofils der Filiale definieren.</span><span class="sxs-lookup"><span data-stu-id="56e9a-121">As for other POS transaction types that generate a printed receipt, you can define a number sequence for suspended transactions in the **Receipt numbering** section of the store's functionality profile.</span></span>

### <a name="void-when-closing-shift"></a><span data-ttu-id="56e9a-122">Stornieren, wenn Schicht geschlossen wird</span><span class="sxs-lookup"><span data-stu-id="56e9a-122">Void when closing shift</span></span>

<span data-ttu-id="56e9a-123">Sie können **Stornieren Sie, wenn Schicht endet** Option verwenden, um festzulegen, dass Benutzer entweder alle unterbrochenen Buchungen unterbrechen oder stornieren, bevor sie ihre Schicht schließen.</span><span class="sxs-lookup"><span data-stu-id="56e9a-123">You can use the **Void when closing shift** option to require that users either complete or void any suspended transactions before they close their shift.</span></span> <span data-ttu-id="56e9a-124">Während dem **Schicht schließen** Arbeitsgangs forder der POS Benutzer auf, unterbrochene Buchungen anzuzeigen oder zu stornieren.</span><span class="sxs-lookup"><span data-stu-id="56e9a-124">During the **Close shift** operation, the POS will prompt users to either view or void any outstanding suspended transactions.</span></span>

## <a name="suspend-and-resume-a-transaction"></a><span data-ttu-id="56e9a-125">Transaktionen anhalten und fortsetzen</span><span class="sxs-lookup"><span data-stu-id="56e9a-125">Suspend and resume a transaction</span></span>

### <a name="suspend-a-transaction"></a><span data-ttu-id="56e9a-126">Transaktion aussetzen</span><span class="sxs-lookup"><span data-stu-id="56e9a-126">Suspend a transaction</span></span>

<span data-ttu-id="56e9a-127">Benutzer, die über die entsprechenden Rechte verfügen und die eingeben Bildschirmlayout haben, das den Arbeitsgang **Buchung aussetzen** enthält, können eine Buchung fortsetzen, damit sie an einer anderen Kasse später zurückgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="56e9a-127">Users who have sufficient privileges, and who have a screen layout that includes the **Suspend transaction** operation, can suspend a transaction so that it can be recalled later or on a different register.</span></span>

<span data-ttu-id="56e9a-128">Buchungen können unterbrochen werden, wenn sie **nicht** die folgenden Rückvergütungstypen enthalten:</span><span class="sxs-lookup"><span data-stu-id="56e9a-128">Transactions can be suspended only if they do **not** contain the following types of lines:</span></span>

- <span data-ttu-id="56e9a-129">Aktive Zahlungspositionen</span><span class="sxs-lookup"><span data-stu-id="56e9a-129">Active payment lines</span></span>
- <span data-ttu-id="56e9a-130">Geschenkkartepositionen (entweder eine Geschenkkarte ausstellen oder Geschenkkartensaldo hinzufügen)</span><span class="sxs-lookup"><span data-stu-id="56e9a-130">Gift card lines (either to issue a gift card or to add to the gift card balance)</span></span>

<span data-ttu-id="56e9a-131">Eine unterbrochene Buchung hat keine Verkaufsinformations- oder Bestandsverfügbarkeit-Informationen für den Shop.</span><span class="sxs-lookup"><span data-stu-id="56e9a-131">A suspended transaction doesn't affect sales information or inventory availability information for the store.</span></span>

### <a name="resume-a-suspended-transaction"></a><span data-ttu-id="56e9a-132">Ruft eine ausgesetzte Transaktion zurück.</span><span class="sxs-lookup"><span data-stu-id="56e9a-132">Resume a suspended transaction</span></span>

<span data-ttu-id="56e9a-133">Unterbrochene Transaktionen können in denselben Shop von jedem Benutzer erneut aufgerufen und fortgesetzt werden, der über die entsprechenden Rechte hat und der ebenfalls ein Layout, hat das den Arbeitsgang **Transaktlion zurückrufen** umfasst.</span><span class="sxs-lookup"><span data-stu-id="56e9a-133">Suspended transactions can be recalled and resumed in the same store by any user who has sufficient privileges, and who also has a layout that includes the **Recall transaction** operation.</span></span>

<span data-ttu-id="56e9a-134">Um schnell und einfach eine unterbrochene Buchung aufzurufen, scannen Sie den Strichcode auf dem gedruckten Beleg, während Sie die Liste der Buchungen vom Arbeitsgang anzeigen **Buchung zurückrufen**.</span><span class="sxs-lookup"><span data-stu-id="56e9a-134">To quickly and easily recall a suspended transaction, scan the barcode on the printed slip while you're viewing the list of transactions from the **Recall transaction** operation.</span></span>

### <a name="considerations-for-offline-mode"></a><span data-ttu-id="56e9a-135">Betrachtungen für Offlinemodus</span><span class="sxs-lookup"><span data-stu-id="56e9a-135">Considerations for offline mode</span></span>

- <span data-ttu-id="56e9a-136">Buchungen, die unterbrochen wurden, während der POS im Online-Modus ist, kann nicht im Offline-Modus fortgesetzt werden, weil die Daten nicht mit der Offline-Datenbank synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="56e9a-136">Any transaction that is suspended while the POS is in online mode can't be resumed in offline mode, because the data isn't synced to the offline database.</span></span>
- <span data-ttu-id="56e9a-137">Wenn Sie eine Buchung unterbrechen, während der POS im Offline-Modus ist, können Sie sie im Offline-Modus zurückrufen, vorausgesetzt, dass der Betrag vom POS nicht in rechnerabhängigem Betrieb geändert wurde, seit die Buchung unterbrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="56e9a-137">If you suspend a transaction while the POS is in offline mode, you can recall it in offline mode, provided that the POS wasn't switched back to online mode at any time since you suspended the transaction.</span></span> <span data-ttu-id="56e9a-138">Wenn der POS wieder im Online-Modus ist, werden die Daten zu unterbrochene Buchungen verschoben udn von der Offline-Datenbank entfernt.</span><span class="sxs-lookup"><span data-stu-id="56e9a-138">When the POS is switched back to online mode, data about suspended transactions is moved to the online database and removed from the offline database.</span></span> <span data-ttu-id="56e9a-139">Daher können Sie die Transaktionen nur im Online-Modus fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="56e9a-139">Therefore, the transactions can be resumed only in online mode.</span></span> <span data-ttu-id="56e9a-140">Wenn Sie vom POS wieder in den Offline-Modus wechseln, sind Sie nicht mehr in der Lage, die unterbrochene Transaktionen fortzusetzen, da sie bereits offline aus der Datenbank entfernt wurden.</span><span class="sxs-lookup"><span data-stu-id="56e9a-140">If you switch the POS back to offline mode, you won't be able to resume those suspended transaction, because they have already been removed from the offline database.</span></span>

### <a name="void-a-suspended-transaction"></a><span data-ttu-id="56e9a-141">Ausgesetzte Buchung stornieren</span><span class="sxs-lookup"><span data-stu-id="56e9a-141">Void a suspended transaction</span></span>

<span data-ttu-id="56e9a-142">Sie können unterbrochene Buchungen stornieren, indem Sie die Buchung zuerst erneut aufrufen und dann **Transaktion stornieren** ausführen oder die Buchung in der Liste **Transaktion zurückrufen** auswählen und **Storniert** auf der App-Leiste auswählen.</span><span class="sxs-lookup"><span data-stu-id="56e9a-142">You can void suspended transactions either by recalling the transaction and then performing the **Void transaction** operation, or by selecting the transaction in the **Recall transaction** list and selecting **Void** on the app bar.</span></span> <span data-ttu-id="56e9a-143">Alternativ kann der Shop konfiguriert werden, damit Benutzer aufgefordert werden, unterbrochene Transaktionen zu stornieren, wenn sie ihre Schicht schließen.</span><span class="sxs-lookup"><span data-stu-id="56e9a-143">Alternatively, the store can be configured to prompt users to void suspended transactions when they close their shift.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]