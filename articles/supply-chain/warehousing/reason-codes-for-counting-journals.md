---
title: "Ursachencodes für Bestandszählungen anzeigen"
description: "In diesem Thema wird beschrieben, wie Ursachencodes für Inventuraufgaben eingerichtet werden."
author: Mirzaab
manager: AnnBe
ms.date: 03/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCountingReasonCodePolicy
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 2f4332432ad73861cd9b6b6452685d3175ace56b
ms.contentlocale: de-de
ms.lasthandoff: 08/07/2018

---

# <a name="reason-codes-for-inventory-counting"></a><span data-ttu-id="abf8c-103">Ursachencodes für Bestandszählungen anzeigen</span><span class="sxs-lookup"><span data-stu-id="abf8c-103">Reason codes for inventory counting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="abf8c-104">Ursachencodes lassen Sie die Ergebnisse einer Inventur und sämtliche Abweichungen analysieren, die während dieses Vorgangs auftreten.</span><span class="sxs-lookup"><span data-stu-id="abf8c-104">Reason codes let you analyze the results of a counting process and any discrepancies that occur during that process.</span></span> <span data-ttu-id="abf8c-105">Sie können den Grund für das Treffen der Anzahl, wie eine angebrochenes Palette oder einen vordefinierten Regulierung angeben, die auf Grundlage der Bestandsbeispiele liegt.</span><span class="sxs-lookup"><span data-stu-id="abf8c-105">You can specify the reason for doing the count, such as a broken pallet or a stock adjustment that is based on inventory samples.</span></span>

## <a name="recommendation"></a><span data-ttu-id="abf8c-106">Empfehlung</span><span class="sxs-lookup"><span data-stu-id="abf8c-106">Recommendation</span></span>

<span data-ttu-id="abf8c-107">Bevor Sie das System so einrichten, wird empfohlen, dass Sie eine Strategie für die Arbeit mit Ursachencodes definieren.</span><span class="sxs-lookup"><span data-stu-id="abf8c-107">Before you set up the system, we recommend that you define a strategy for working with reason codes.</span></span> <span data-ttu-id="abf8c-108">Beispielsweise versuchen Sie, die folgenden Fragen zu beantworten:</span><span class="sxs-lookup"><span data-stu-id="abf8c-108">For example, try to answer the following questions:</span></span>

- <span data-ttu-id="abf8c-109">Müssen für Lagerorte Ursachencodes erforderlich sein?</span><span class="sxs-lookup"><span data-stu-id="abf8c-109">Should reason codes be mandatory on warehouses?</span></span>
- <span data-ttu-id="abf8c-110">Müssen Ursachencodes für mehrere Artikel obligatorisch oder optional sein?</span><span class="sxs-lookup"><span data-stu-id="abf8c-110">Should reason codes be mandatory or optional on some items?</span></span>
- <span data-ttu-id="abf8c-111">Wie viele Ursachencodes brauchen Sie?</span><span class="sxs-lookup"><span data-stu-id="abf8c-111">How many reason codes do you require?</span></span>
- <span data-ttu-id="abf8c-112">Wie sollen Benutzer von Strichcodescannern Ursachencodes verwenden?</span><span class="sxs-lookup"><span data-stu-id="abf8c-112">How should users of barcode scanners use reason codes?</span></span> <span data-ttu-id="abf8c-113">Müssen die Ursachencodes vorgewählt, erforderlich oder nicht bearbeitbar sein?</span><span class="sxs-lookup"><span data-stu-id="abf8c-113">Should the reason codes be preselected, mandatory, or not editable?</span></span>
- <span data-ttu-id="abf8c-114">Brauchen Lagerarbeiter anderes Ursachencodeverhalten auf mobile Scannern?</span><span class="sxs-lookup"><span data-stu-id="abf8c-114">Do warehouse workers require different reason code behavior on mobile scanners?</span></span> <span data-ttu-id="abf8c-115">Wenn die Antwort ja ist, können Sie keine weiteren Menüoptionen erstellen und diese unterschiedlichen Person zuweisen.</span><span class="sxs-lookup"><span data-stu-id="abf8c-115">If the answer is yes, you can create more menu items and assign them to different people.</span></span>

## <a name="where-reason-codes-apply"></a><span data-ttu-id="abf8c-116">Wo Ursachencodes gelten</span><span class="sxs-lookup"><span data-stu-id="abf8c-116">Where reason codes apply</span></span>

<span data-ttu-id="abf8c-117">Sie können mehrere Ursachencoderichtlinien erstellen, und jede Ursachencoderichtlinie kann zwei zählende Ursachencoderichtlinien haben.</span><span class="sxs-lookup"><span data-stu-id="abf8c-117">You can create multiple reason code policies, and each reason code policy can have two counting reason code policies.</span></span> <span data-ttu-id="abf8c-118">Die Inventurursachenrichtlinien können verschiedene Lagerortebene oder Artikelebenen verwenden.</span><span class="sxs-lookup"><span data-stu-id="abf8c-118">The counting reason code policies can be used at the warehouse level or the item level.</span></span>

## <a name="set-up-reason-code-policies"></a><span data-ttu-id="abf8c-119">Richten Sie Ursachencodes ein.</span><span class="sxs-lookup"><span data-stu-id="abf8c-119">Set up reason code policies</span></span>

1. <span data-ttu-id="abf8c-120">Wählen Sie **Lagerverwaltung** \> **Einstellungen** \> **Lager** \> **Richtlinien Inventurursachencodes** aus, und erstellen Sie eine neue Ursachencoderichtlinie.</span><span class="sxs-lookup"><span data-stu-id="abf8c-120">Select **Inventory management** \> **Setup** \> **Inventory** \> **Counting reason code policies**, and create a new reason code policy.</span></span>
2. <span data-ttu-id="abf8c-121">Im Feld **Inventurursachencodetyp** wählen Sie entweder **Obligatorisch** oder **Fakultativ**, um anzugeben, ob die Auswahl eines Ursachencodes eine optionale oder erforderliche Aktivität in einer der folgenden Inventurerfassungen sollen:</span><span class="sxs-lookup"><span data-stu-id="abf8c-121">In the **Counting reason code type** field, select either **Mandatory** or **Optional** to specify whether selection of a reason code should be an optional or mandatory action in one of the following counting journals:</span></span>

    - <span data-ttu-id="abf8c-122">Inventur (mobilen Gerät)</span><span class="sxs-lookup"><span data-stu-id="abf8c-122">Cycle Count (mobile device)</span></span>
    - <span data-ttu-id="abf8c-123">Lagerplatzinventur (mobile Gerät)</span><span class="sxs-lookup"><span data-stu-id="abf8c-123">Spot Count (mobile device)</span></span>
    - <span data-ttu-id="abf8c-124">Schwelleninventur (mobile Gerät)</span><span class="sxs-lookup"><span data-stu-id="abf8c-124">Threshold Count (mobile device)</span></span>
    - <span data-ttu-id="abf8c-125">Regulierung in (mobiles Gerät)</span><span class="sxs-lookup"><span data-stu-id="abf8c-125">Adjustment In (mobile device)</span></span>
    - <span data-ttu-id="abf8c-126">Regulierung aus (mobiles Gerät)</span><span class="sxs-lookup"><span data-stu-id="abf8c-126">Adjustment Out (mobile device)</span></span>
    - <span data-ttu-id="abf8c-127">Inventurerfassung " Rich Client)</span><span class="sxs-lookup"><span data-stu-id="abf8c-127">Counting Journal (rich client)</span></span>

<span data-ttu-id="abf8c-128">Sie können Ursachencodes für einzelne Lagerorte und für Produkte einrichten.</span><span class="sxs-lookup"><span data-stu-id="abf8c-128">You can also set up reason codes for individual warehouses and for products.</span></span> <span data-ttu-id="abf8c-129">Die Ursachencodeeinstellung für Produkte Einstellung kann für Lagerorte missachten.</span><span class="sxs-lookup"><span data-stu-id="abf8c-129">The reason code setup for products can disregard the setup for warehouses.</span></span>

## <a name="mandatory-reason-codes"></a><span data-ttu-id="abf8c-130">Obligatorische Ursachencodes</span><span class="sxs-lookup"><span data-stu-id="abf8c-130">Mandatory reason codes</span></span>

<span data-ttu-id="abf8c-131">Wenn der Parameter **Obligatorisch** in der Konfiguration von Ursachencodes für Lagerorte oder Artikel festgelegt ist, kann die Inventurerfassung nicht abgeschlossen werden, bis ein Ursachencode angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="abf8c-131">If the **Mandatory** parameter is set in the configuration of reason codes for warehouses or items, the counting journal can't be completed and closed until a reason code is provided.</span></span>

### <a name="set-up-reason-codes-for-warehouses"></a><span data-ttu-id="abf8c-132">Ursachencodes für Lagerorte einrichten</span><span class="sxs-lookup"><span data-stu-id="abf8c-132">Set up reason codes for warehouses</span></span>

1. <span data-ttu-id="abf8c-133">Klicken Sie auf **Lagerverwaltung** \> **Einstellungen** \> **Lageraufschlüsselung** \> **Lagerorte**</span><span class="sxs-lookup"><span data-stu-id="abf8c-133">Select **Inventory Management** \> **Setup** \> **Inventory breakdown** \> **Warehouses**.</span></span>
2. <span data-ttu-id="abf8c-134">Auf der Registerkarte **Lagerort** im Feld **Inventurursachencoderichtlinie**, wählen Sie eine der folgenden Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="abf8c-134">On the **Warehouse** tab, in the **Counting reason code policy** field, select one of the following options:</span></span>

    - <span data-ttu-id="abf8c-135">**Leer** – Parameter, der der für den Artikel eingerichtet wurde, wird verwendet, um zu bestimmen, ob das Produkt für Inventurerfassungen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="abf8c-135">**Blank** – The parameter that is set up for the item is used to determine whether counting journals are mandatory for the product.</span></span>
    - <span data-ttu-id="abf8c-136">**Obligatorisch** – Ein Ursachencode ist immer auf für Inventurerfassungen für den Lagerort erforderlich.</span><span class="sxs-lookup"><span data-stu-id="abf8c-136">**Mandatory** – A reason code is always required on counting journals for the warehouse.</span></span>
    - <span data-ttu-id="abf8c-137">**Obligatorisch** – Ein Ursachencode ist immer für Inventurerfassungen für den Lagerort erforderlich.</span><span class="sxs-lookup"><span data-stu-id="abf8c-137">**Optional** – A reason code isn't required on counting journals for the warehouse.</span></span>

### <a name="set-up-reason-codes-for-products"></a><span data-ttu-id="abf8c-138">Ursachencodes für Lagerorte einrichten</span><span class="sxs-lookup"><span data-stu-id="abf8c-138">Set up reason codes for products</span></span>

1. <span data-ttu-id="abf8c-139">Wechseln Sie **Produktinformationsverwaltung** \> **Produkte** \> **Freigegebene Produkte**.</span><span class="sxs-lookup"><span data-stu-id="abf8c-139">Select **Product information management** \> **Products** \> **Released products**.</span></span>
2. <span data-ttu-id="abf8c-140">Auf der Registerkarte **Lagerort** im Feld **Inventurursachencoderichtlinie** wählen Sie eine der folgenden Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="abf8c-140">On the **Product** tab, select **Counting reason code policy**, and then select one of the following options:</span></span>

    - <span data-ttu-id="abf8c-141">**Leer** – Parameter, der für den Artikel eingerichtet wurde, wird verwendet, um zu bestimmen, ob das Produkt für Inventurerfassungen erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="abf8c-141">**Blank** – The parameter that is set up for the warehouse is used to determine whether counting journals are mandatory for the product.</span></span>
    - <span data-ttu-id="abf8c-142">**Obligatorisch** – Ein Ursachencode ist immer auch für Inventurerfassungen für das Produkt erforderlich.</span><span class="sxs-lookup"><span data-stu-id="abf8c-142">**Mandatory** – A reason code is always required on counting journals for the product.</span></span> <span data-ttu-id="abf8c-143">Diese Einstellung hat Priorität gegenüber Ursachencodeeinstellungen auf Lagerortebene.</span><span class="sxs-lookup"><span data-stu-id="abf8c-143">This setting overrides any reason code setting at the warehouse level.</span></span>
    - <span data-ttu-id="abf8c-144">**Obligatorisch** – Ein Ursachencode ist immer für Inventurerfassungen für das Produkt erforderlich.</span><span class="sxs-lookup"><span data-stu-id="abf8c-144">**Optional** – A reason code isn't required on counting journals for the product.</span></span> <span data-ttu-id="abf8c-145">Diese Einstellung hat Priorität gegenüber Ursachencodeeinstellungen auf Lagerortebene.</span><span class="sxs-lookup"><span data-stu-id="abf8c-145">This setting overrides any reason code setting at the warehouse level.</span></span>

### <a name="use-reason-codes-in-counting-journals"></a><span data-ttu-id="abf8c-146">Verwenden von Ursachencodes in den Inventurerfassungen</span><span class="sxs-lookup"><span data-stu-id="abf8c-146">Use reason codes in counting journals</span></span>

<span data-ttu-id="abf8c-147">In einer Inventurerfassung können Sie Ursachencodes für viele der folgenden Typen hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="abf8c-147">In a counting journal, you can add reason codes for counts of the following types:</span></span>

- <span data-ttu-id="abf8c-148">Inventurzählung</span><span class="sxs-lookup"><span data-stu-id="abf8c-148">Cycle Count</span></span>
- <span data-ttu-id="abf8c-149">Stellen-Anzahl</span><span class="sxs-lookup"><span data-stu-id="abf8c-149">Spot Count</span></span>
- <span data-ttu-id="abf8c-150">Schwellenzählung</span><span class="sxs-lookup"><span data-stu-id="abf8c-150">Threshold Count</span></span>
- <span data-ttu-id="abf8c-151">Regulierung eingehend</span><span class="sxs-lookup"><span data-stu-id="abf8c-151">Adjustment In</span></span>
- <span data-ttu-id="abf8c-152">Regulierung ausgehend</span><span class="sxs-lookup"><span data-stu-id="abf8c-152">Adjustment Out</span></span>

<span data-ttu-id="abf8c-153">Ursachencodes werden für Inventurerfassungen ine Erfassungspositionen im Typ **Inventurerfassung** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="abf8c-153">Reason codes are added to the journal lines in counting journals of the **Counting journal** type.</span></span>

1. <span data-ttu-id="abf8c-154">Wechseln Sie zu **Lagerverwaltung** \> **Erfassungseinträge** \> **Artikelinventur** \> **Inventur**.</span><span class="sxs-lookup"><span data-stu-id="abf8c-154">Select **Inventory management** \> **Journal entries** \> **Item counting** \> **Counting**.</span></span>
2. <span data-ttu-id="abf8c-155">In den Positionsdetails in der Inventurerfassung im Feld **Inventurursachencode** wählen Sie eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="abf8c-155">In the line details of the counting journal, in the **Counting reason code** field, select an option.</span></span>

### <a name="view-the-counting-history-as-its-recorded-by-reason-codes"></a><span data-ttu-id="abf8c-156">Die Inventurerfassung annzeigen, da diese nach Ursachencodes erfasst ist.</span><span class="sxs-lookup"><span data-stu-id="abf8c-156">View the counting history as it's recorded by reason codes</span></span>

- <span data-ttu-id="abf8c-157">Wählen Sie **Lagerverwaltung** \> **Abfragen und Berichte** \> **Inventurerfassung**, aus, und klicken Sie dann im Feld **Inventurursachencode** aus, geben die Inventurerfassung angezeigt, die über einen Ursachencode erfasst wurde.</span><span class="sxs-lookup"><span data-stu-id="abf8c-157">Select **Inventory management** \> **Inquiries and reports** \> **Counting history**, and then, in the **Counting reason code** field, view the counting history that has been recorded through a reason code.</span></span>

### <a name="use-a-reason-code-for-a-quantity-adjustment"></a><span data-ttu-id="abf8c-158">Verwenden Sie einen Ursachencode für eine Mengenanpassung</span><span class="sxs-lookup"><span data-stu-id="abf8c-158">Use a reason code for a quantity adjustment</span></span>

1. <span data-ttu-id="abf8c-159">Wählen Sie auf der Seite **Verfügbarer Lagerbestand** **Menge anpassen** aus.</span><span class="sxs-lookup"><span data-stu-id="abf8c-159">On the **On-hand inventory** page, select **Adjust quantity**.</span></span> <span data-ttu-id="abf8c-160">Sie können die Seite **Verfügbarer Lagerbestand** auf mehrere Arten öffnen</span><span class="sxs-lookup"><span data-stu-id="abf8c-160">You can open the **On-hand inventory** page in several ways.</span></span> <span data-ttu-id="abf8c-161">Wechseln Sie zu **Lagerverwaltung** \> **Abfragen und Berichte** \> **Verfügbarer Lagerbestand**.</span><span class="sxs-lookup"><span data-stu-id="abf8c-161">For example, select **Inventory management** \> **Inquiries and reports** \> **On-hand inventory**.</span></span>
2. <span data-ttu-id="abf8c-162">Wählen Sie **Menge anpassen**, und dann, im Feld **Inventurursachencode** wählen Sie einen Ursachencode aus.</span><span class="sxs-lookup"><span data-stu-id="abf8c-162">Select **Adjust quantity**, and then, in the **Counting reason code** field, select a reason code.</span></span>

### <a name="configure-reason-codes-for-mobile-device-menu-items"></a><span data-ttu-id="abf8c-163">Konfigurieren Sie Ursachencodes für Menüoptionen für das mobile Gerät</span><span class="sxs-lookup"><span data-stu-id="abf8c-163">Configure reason codes for mobile device menu items</span></span>

<span data-ttu-id="abf8c-164">Sie können Ursachencodes für alle Anzahlarten für eine Menüoption des mobilen Geräts konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="abf8c-164">You can configure reason codes for any type of count on a mobile device menu item.</span></span> <span data-ttu-id="abf8c-165">Die Variante der Menüoption des mobilen Geräts enthält die folgenden Informationen:</span><span class="sxs-lookup"><span data-stu-id="abf8c-165">The configuration of the mobile device menu item includes the following information:</span></span>

- <span data-ttu-id="abf8c-166">Ob der Ursachencode des mobilen Geräts während des Zählens angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="abf8c-166">Whether the reason code is shown to the mobile device worker during counting.</span></span>
- <span data-ttu-id="abf8c-167">Der Standardursachencode ein, der für eines Menüelements des mobilen Geräts angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="abf8c-167">The default reason code that is shown on a mobile device menu item.</span></span>
- <span data-ttu-id="abf8c-168">Ob der Benutzer den Ursachencode arbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="abf8c-168">Whether the user can edit the reason code.</span></span>

### <a name="set-up-reason-codes-on-a-mobile-device"></a><span data-ttu-id="abf8c-169">Einstellungsursachencodes auf einem mobilen Gerät</span><span class="sxs-lookup"><span data-stu-id="abf8c-169">Set up reason codes on a mobile device</span></span>

1. <span data-ttu-id="abf8c-170">Wählen Sie **Lagerortverwaltung** \> **Setup** \> **Mobiles Gerät** \> **Menüoptionen für mobiles Gerät** aus.</span><span class="sxs-lookup"><span data-stu-id="abf8c-170">Select **Warehouse management** \> **Setup** \> **Mobile device** \> **Mobile device menu items**.</span></span>
2. <span data-ttu-id="abf8c-171">Auf der Registerkarte **Inventuren** wählen Sie **Zykluszählung** aus.</span><span class="sxs-lookup"><span data-stu-id="abf8c-171">On the **Cycle count** tab, select **Cycle counting**.</span></span>
3. <span data-ttu-id="abf8c-172">Wählen Sie im Feld **Standardinventurursachencode** Sie legen den Standardursachencode ein, der beim Melden Inventurauftrag erfasst werden soll, jedoch wird, indem die Menüoption des mobilen Geräts verwendet.</span><span class="sxs-lookup"><span data-stu-id="abf8c-172">In the **Default counting reason code** field, set the default reason code that should be recorded when counting is done by using the mobile device menu item.</span></span>
4. <span data-ttu-id="abf8c-173">Wählen Sie im Feld **Hier werden Inventurursachencode an** **Position**, um die Ursachencodes anzeigen, nachdem eine Abweichung erfasst ist.</span><span class="sxs-lookup"><span data-stu-id="abf8c-173">In the **Display counting reason code** field, select **Line** to show the reason code after each variance is recorded.</span></span> <span data-ttu-id="abf8c-174">Aktivieren Sie **Ausblenden** wenn der Ursachencode nicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="abf8c-174">Alternatively, select **Hide** if the reason code shouldn't be shown.</span></span>
5. <span data-ttu-id="abf8c-175">Hier können Sie die Option **Bearbeiten Sie Inventurursachencode** auf entweder **Ja** oder **Nein** festlegen.</span><span class="sxs-lookup"><span data-stu-id="abf8c-175">Set the **Edit counting reason code** option to either **Yes** or **No**.</span></span> <span data-ttu-id="abf8c-176">Wenn Sie Option auf **Ja** setzen, kann die Arbeitskraft den Ursachencode bearbeiten, wenn er im mobilen Gerät während des Zählens dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="abf8c-176">If you set this option to **Yes**, the worker can edit the reason code when it's shown on the mobile device during counting.</span></span>

> [!NOTE]
> <span data-ttu-id="abf8c-177">Die Schaltfläche **Zykluszählung** kann auf einer beliebigen Menüoption des mobilen Geräts, die in die Inventur aktiviert werden ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="abf8c-177">The **Cycle counting** button can be enabled on any mobile device menu item where counting can be done.</span></span> <span data-ttu-id="abf8c-178">Beispiele umfassen die Menüoptionen für Stellenanzahlen, Benutzer-verwiesene Arbeit und System-verwiesene Arbeit.</span><span class="sxs-lookup"><span data-stu-id="abf8c-178">Example include the menu items for spot counts, user-directed work, and system-directed work.</span></span>

## <a name="cycle-count-approvals"></a><span data-ttu-id="abf8c-179">Inventur-Zykluszählungen</span><span class="sxs-lookup"><span data-stu-id="abf8c-179">Cycle count approvals</span></span>

<span data-ttu-id="abf8c-180">Bevor eine Anzahl genehmigt wurde, kann der Benutzer den Ursachencodes ändern, der der Anzahl zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="abf8c-180">Before a count is approved, the user can change the reason code that is associated with the count.</span></span> <span data-ttu-id="abf8c-181">Wenn die Anzahl genehmigt wird, wird der eingegebene Ursachencode für die Inventurerfassungspositionen.</span><span class="sxs-lookup"><span data-stu-id="abf8c-181">When the count is approved, the reason code is entered on the counting journal lines.</span></span>

### <a name="modify-cycle-count-approvals"></a><span data-ttu-id="abf8c-182">Inventur-Zykluszählungen bearbeiten</span><span class="sxs-lookup"><span data-stu-id="abf8c-182">Modify cycle count approvals</span></span>

1. <span data-ttu-id="abf8c-183">Wählen Sie **Lagerortverwaltung** \> **Zykluszählung** \> **Schwebende Prüfung der Gangzählungs-Arbeit** aus.</span><span class="sxs-lookup"><span data-stu-id="abf8c-183">Select **Warehouse management** \> **Cycle counting** \> **Cycle count work pending review**.</span></span>
2. <span data-ttu-id="abf8c-184">Wählen Sie **Zykluszählung**, und dann, im Feld **Inventurursachencode** wählen Sie einen Ursachencode aus.</span><span class="sxs-lookup"><span data-stu-id="abf8c-184">Select **Cycle counting**, and then, in the **Reason code** field, select a new reason code.</span></span>

### <a name="modify-the-mobile-device-menu-item-for-adjustment-in-and-adjustment-out"></a><span data-ttu-id="abf8c-185">Ändern Sie die Menüoption des mobilen Geräts für ein- und ausgehende Regulierung</span><span class="sxs-lookup"><span data-stu-id="abf8c-185">Modify the mobile device menu item for Adjustment in and Adjustment out</span></span>

1. <span data-ttu-id="abf8c-186">Wählen Sie **Lagerortverwaltung** \> **Einstellungen** \> **Mobiles Gerät** \> **Menüoptionen des mobilen Geräts**, und wählen Sie dann **Regulierung in und** aus.</span><span class="sxs-lookup"><span data-stu-id="abf8c-186">Select **Warehouse management** \> **Setup** \> **Mobile device** \> **Mobile device menu items**, and then select **Adjustment in and out**.</span></span>
2. <span data-ttu-id="abf8c-187">Legen Sie die **Vorhandene Arbeit verwenden**-Option mit **Nein** fest.</span><span class="sxs-lookup"><span data-stu-id="abf8c-187">Set the **Use existing work** option to **No**.</span></span>
3. <span data-ttu-id="abf8c-188">Wählen Sie im Feld **Bearbeiten Erstellungsprozess** **Regulierung in** aus.</span><span class="sxs-lookup"><span data-stu-id="abf8c-188">In the **Work creation process** field, select **Adjustment in**.</span></span>

<span data-ttu-id="abf8c-189">Die folgenden Felder werden der Menüoption des mobilen Geräts hinzugefügt, wenn **Regulierung in** oder **Regulierung aus** für den Arbeitserstellungsprozesses aktiviert ist:</span><span class="sxs-lookup"><span data-stu-id="abf8c-189">The following fields will be added to the mobile device menu item when **Adjustment in** or **Adjustment out** is selected during the work creation process:</span></span>

- <span data-ttu-id="abf8c-190">Standardursachencode für Zählungen</span><span class="sxs-lookup"><span data-stu-id="abf8c-190">Default counting reason code</span></span>
- <span data-ttu-id="abf8c-191">Ursachencode für Zählungen anzeigen</span><span class="sxs-lookup"><span data-stu-id="abf8c-191">Display counting reason code</span></span>
- <span data-ttu-id="abf8c-192">Ursachencode für Zählungen bearbeiten</span><span class="sxs-lookup"><span data-stu-id="abf8c-192">Edit counting reason code</span></span>

