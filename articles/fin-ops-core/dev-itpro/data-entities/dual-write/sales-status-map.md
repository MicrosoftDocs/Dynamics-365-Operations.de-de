---
title: Einrichten eines Mappings für die Auftragsstatusfelder
description: In diesem Thema wird erläutert, wie Sie die Auftragsstatusfelder für duales Schreiben einrichten.
author: dasani-madipalli
manager: tonyafehr
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: damadipa
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-06-25
ms.openlocfilehash: dce4b6310e2f6d31a115302efa7fbc132799e48f
ms.sourcegitcommit: 4ba10abe5be8a21b95370cd970a622e954970984
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/22/2020
ms.locfileid: "3829284"
---
# <a name="set-up-the-mapping-for-the-sales-order-status-fields"></a><span data-ttu-id="48f5b-103">Einrichten eines Mappings für die Auftragsstatusfelder</span><span class="sxs-lookup"><span data-stu-id="48f5b-103">Set up the mapping for the sales order status fields</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="48f5b-104">Die Felder, die den Auftragsstatus angeben, haben in Microsoft Dynamics 365 Supply Chain Management und Dynamics 365 Sales unterschiedliche Aufzählungswerte.</span><span class="sxs-lookup"><span data-stu-id="48f5b-104">The fields that indicate sales order status have different enumeration values in Microsoft Dynamics 365 Supply Chain Management and Dynamics 365 Sales.</span></span> <span data-ttu-id="48f5b-105">Zusätzliche Einstellungen sind erforderlich, um diese Felder in dualem Schreiben abzubilden.</span><span class="sxs-lookup"><span data-stu-id="48f5b-105">Additional setup is required to map these fields in dual-write.</span></span>

## <a name="fields-in-supply-chain-management"></a><span data-ttu-id="48f5b-106">Felder in Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="48f5b-106">Fields in Supply Chain Management</span></span>

<span data-ttu-id="48f5b-107">In Supply Chain Management spiegeln zwei Felder den Status des Auftrags wider.</span><span class="sxs-lookup"><span data-stu-id="48f5b-107">In Supply Chain Management, two fields reflect the status of the sales order.</span></span> <span data-ttu-id="48f5b-108">Die Felder, die Sie zuordnen müssen, sind **Status** und **Dokumentstatus**.</span><span class="sxs-lookup"><span data-stu-id="48f5b-108">The fields that you must map are **Status** and **Document Status**.</span></span>

<span data-ttu-id="48f5b-109">Die **Status**-Aufzählung gibt den Gesamtstatus der Bestellung an.</span><span class="sxs-lookup"><span data-stu-id="48f5b-109">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="48f5b-110">Dieser Status wird im Auftragskopf angezeigt.</span><span class="sxs-lookup"><span data-stu-id="48f5b-110">This status is shown on the order header.</span></span>

<span data-ttu-id="48f5b-111">Die **Status**-Aufzählung hat die folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="48f5b-111">The **Status** enumeration has the following values:</span></span>

- <span data-ttu-id="48f5b-112">Offene Bestellung</span><span class="sxs-lookup"><span data-stu-id="48f5b-112">Open Order</span></span>
- <span data-ttu-id="48f5b-113">Geliefert</span><span class="sxs-lookup"><span data-stu-id="48f5b-113">Delivered</span></span>
- <span data-ttu-id="48f5b-114">Fakturiert</span><span class="sxs-lookup"><span data-stu-id="48f5b-114">Invoiced</span></span>
- <span data-ttu-id="48f5b-115">Storniert</span><span class="sxs-lookup"><span data-stu-id="48f5b-115">Cancelled</span></span>

<span data-ttu-id="48f5b-116">Die **Dokumentstatus**-Aufzählung gibt das letzte Dokument an, das für die Bestellung generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="48f5b-116">The **Document Status** enumeration specifies the most recent document that was generated for the order.</span></span> <span data-ttu-id="48f5b-117">Wenn die Bestellung beispielsweise bestätigt wird, handelt es sich bei diesem Dokument um eine Auftragsbestätigung.</span><span class="sxs-lookup"><span data-stu-id="48f5b-117">For example, if the order is confirmed, this document is a sales order confirmation.</span></span> <span data-ttu-id="48f5b-118">Wenn ein Kundenauftrag teilweise in Rechnung gestellt wird und dann die verbleibende Position bestätigt wird, bleibt der Belegstatus **Rechnung** erhalten, weil die Rechnung später im Prozess generiert wird.</span><span class="sxs-lookup"><span data-stu-id="48f5b-118">If a sales order is partially invoiced, and then the remaining line is confirmed, the document status remains **Invoice**, because the invoice is generated later in the process.</span></span>

<span data-ttu-id="48f5b-119">Die **Dokumentstatus**-Aufzählung hat die folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="48f5b-119">The **Document Status** enumeration has the following values:</span></span>

- <span data-ttu-id="48f5b-120">Bestätigung</span><span class="sxs-lookup"><span data-stu-id="48f5b-120">Confirmation</span></span>
- <span data-ttu-id="48f5b-121">Kommissionierliste</span><span class="sxs-lookup"><span data-stu-id="48f5b-121">Picking List</span></span>
- <span data-ttu-id="48f5b-122">Lieferschein</span><span class="sxs-lookup"><span data-stu-id="48f5b-122">Packing Slip</span></span>
- <span data-ttu-id="48f5b-123">Rechnung</span><span class="sxs-lookup"><span data-stu-id="48f5b-123">Invoice</span></span>

## <a name="fields-in-sales"></a><span data-ttu-id="48f5b-124">Felder im Sales</span><span class="sxs-lookup"><span data-stu-id="48f5b-124">Fields in Sales</span></span>

<span data-ttu-id="48f5b-125">In Sales spiegeln geben zwei Felder den Status der Bestellung an.</span><span class="sxs-lookup"><span data-stu-id="48f5b-125">In Sales, two fields indicate the status of the order.</span></span> <span data-ttu-id="48f5b-126">Die Felder, die Sie zuordnen müssen, sind **Status** und **Verarbeitungsstatus**.</span><span class="sxs-lookup"><span data-stu-id="48f5b-126">The fields that you must map are **Status** and **Processing Status**.</span></span>

<span data-ttu-id="48f5b-127">Die **Status**-Aufzählung gibt den Gesamtstatus der Bestellung an.</span><span class="sxs-lookup"><span data-stu-id="48f5b-127">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="48f5b-128">Es weist die folgenden Werte auf:</span><span class="sxs-lookup"><span data-stu-id="48f5b-128">It has the following values:</span></span>

- <span data-ttu-id="48f5b-129">Aktiv</span><span class="sxs-lookup"><span data-stu-id="48f5b-129">Active</span></span>
- <span data-ttu-id="48f5b-130">Übermittelt</span><span class="sxs-lookup"><span data-stu-id="48f5b-130">Submitted</span></span>
- <span data-ttu-id="48f5b-131">Erfüllt</span><span class="sxs-lookup"><span data-stu-id="48f5b-131">Fulfilled</span></span>
- <span data-ttu-id="48f5b-132">Fakturiert</span><span class="sxs-lookup"><span data-stu-id="48f5b-132">Invoiced</span></span>
- <span data-ttu-id="48f5b-133">Storniert</span><span class="sxs-lookup"><span data-stu-id="48f5b-133">Cancelled</span></span>

<span data-ttu-id="48f5b-134">Die Aufzählung **Verarbeitungsstatus** wurde eingeführt, damit der Status genau auf Supply Chain Management zugeordnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="48f5b-134">The **Processing Status** enumeration was introduced so that the status can be mapped more accurately with Supply Chain Management.</span></span>

<span data-ttu-id="48f5b-135">Die folgende Tabelle zeigt die Zuordnung von **Verarbeitungsstatus** auf Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="48f5b-135">The following table shows the mapping of **Processing Status** in Supply Chain Management.</span></span>

| <span data-ttu-id="48f5b-136">Verarbeitungsstatus</span><span class="sxs-lookup"><span data-stu-id="48f5b-136">Processing Status</span></span>   | <span data-ttu-id="48f5b-137">Status in Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="48f5b-137">Status in Supply Chain Management</span></span> | <span data-ttu-id="48f5b-138">Dokumentstatus in Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="48f5b-138">Document Status in Supply Chain Management</span></span> |
|---------------------|-----------------------------------|--------------------------------------------|
| <span data-ttu-id="48f5b-139">Aktiv</span><span class="sxs-lookup"><span data-stu-id="48f5b-139">Active</span></span>              | <span data-ttu-id="48f5b-140">Offene Bestellung</span><span class="sxs-lookup"><span data-stu-id="48f5b-140">Open Order</span></span>                        | <span data-ttu-id="48f5b-141">Keines</span><span class="sxs-lookup"><span data-stu-id="48f5b-141">None</span></span>                                       |
| <span data-ttu-id="48f5b-142">Bestätigt</span><span class="sxs-lookup"><span data-stu-id="48f5b-142">Confirmed</span></span>           | <span data-ttu-id="48f5b-143">Offene Bestellung</span><span class="sxs-lookup"><span data-stu-id="48f5b-143">Open Order</span></span>                        | <span data-ttu-id="48f5b-144">Bestätigung</span><span class="sxs-lookup"><span data-stu-id="48f5b-144">Confirmation</span></span>                               |
| <span data-ttu-id="48f5b-145">Entnommen</span><span class="sxs-lookup"><span data-stu-id="48f5b-145">Picked</span></span>              | <span data-ttu-id="48f5b-146">Offene Bestellung</span><span class="sxs-lookup"><span data-stu-id="48f5b-146">Open Order</span></span>                        | <span data-ttu-id="48f5b-147">Kommissionierliste</span><span class="sxs-lookup"><span data-stu-id="48f5b-147">Picking List</span></span>                               |
| <span data-ttu-id="48f5b-148">Teilweise geliefert</span><span class="sxs-lookup"><span data-stu-id="48f5b-148">Partially Delivered</span></span> | <span data-ttu-id="48f5b-149">Offene Bestellung</span><span class="sxs-lookup"><span data-stu-id="48f5b-149">Open Order</span></span>                        | <span data-ttu-id="48f5b-150">Lieferschein</span><span class="sxs-lookup"><span data-stu-id="48f5b-150">Packing Slip</span></span>                               |
| <span data-ttu-id="48f5b-151">Geliefert</span><span class="sxs-lookup"><span data-stu-id="48f5b-151">Delivered</span></span>           | <span data-ttu-id="48f5b-152">Geliefert</span><span class="sxs-lookup"><span data-stu-id="48f5b-152">Delivered</span></span>                         | <span data-ttu-id="48f5b-153">Lieferschein</span><span class="sxs-lookup"><span data-stu-id="48f5b-153">Packing Slip</span></span>                               |
| <span data-ttu-id="48f5b-154">Teilweise fakturiert</span><span class="sxs-lookup"><span data-stu-id="48f5b-154">Partially Invoiced</span></span>  | <span data-ttu-id="48f5b-155">Geliefert</span><span class="sxs-lookup"><span data-stu-id="48f5b-155">Delivered</span></span>                         | <span data-ttu-id="48f5b-156">Rechnung</span><span class="sxs-lookup"><span data-stu-id="48f5b-156">Invoice</span></span>                                    |
| <span data-ttu-id="48f5b-157">Fakturiert</span><span class="sxs-lookup"><span data-stu-id="48f5b-157">Invoiced</span></span>            | <span data-ttu-id="48f5b-158">Fakturiert</span><span class="sxs-lookup"><span data-stu-id="48f5b-158">Invoiced</span></span>                          | <span data-ttu-id="48f5b-159">Rechnung</span><span class="sxs-lookup"><span data-stu-id="48f5b-159">Invoice</span></span>                                    |
| <span data-ttu-id="48f5b-160">Storniert</span><span class="sxs-lookup"><span data-stu-id="48f5b-160">Cancelled</span></span>           | <span data-ttu-id="48f5b-161">Storniert</span><span class="sxs-lookup"><span data-stu-id="48f5b-161">Cancelled</span></span>                         | <span data-ttu-id="48f5b-162">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="48f5b-162">Not applicable</span></span>                             |

<span data-ttu-id="48f5b-163">Die folgende Tabelle zeigt die Zuordnung von **Verarbeitungsstatus** zwischen Sales und Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="48f5b-163">The following table shows the mapping of **Processing Status** between Sales and Supply Chain Management.</span></span>

| <span data-ttu-id="48f5b-164">Verarbeitungsstatus</span><span class="sxs-lookup"><span data-stu-id="48f5b-164">Processing Status</span></span>   | <span data-ttu-id="48f5b-165">Status in Sales</span><span class="sxs-lookup"><span data-stu-id="48f5b-165">Status in Sales</span></span> | <span data-ttu-id="48f5b-166">Status in Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="48f5b-166">Status in Supply Chain Management</span></span> |
|---------------------|-----------------|-----------------------------------|
| <span data-ttu-id="48f5b-167">Aktiv</span><span class="sxs-lookup"><span data-stu-id="48f5b-167">Active</span></span>              | <span data-ttu-id="48f5b-168">Aktiv</span><span class="sxs-lookup"><span data-stu-id="48f5b-168">Active</span></span>          | <span data-ttu-id="48f5b-169">Offene Bestellung</span><span class="sxs-lookup"><span data-stu-id="48f5b-169">Open Order</span></span>                        |
| <span data-ttu-id="48f5b-170">Bestätigt</span><span class="sxs-lookup"><span data-stu-id="48f5b-170">Confirmed</span></span>           | <span data-ttu-id="48f5b-171">Übermittelt</span><span class="sxs-lookup"><span data-stu-id="48f5b-171">Submitted</span></span>       | <span data-ttu-id="48f5b-172">Offene Bestellung</span><span class="sxs-lookup"><span data-stu-id="48f5b-172">Open Order</span></span>                        |
| <span data-ttu-id="48f5b-173">Entnommen</span><span class="sxs-lookup"><span data-stu-id="48f5b-173">Picked</span></span>              | <span data-ttu-id="48f5b-174">Übermittelt</span><span class="sxs-lookup"><span data-stu-id="48f5b-174">Submitted</span></span>       | <span data-ttu-id="48f5b-175">Offene Bestellung</span><span class="sxs-lookup"><span data-stu-id="48f5b-175">Open Order</span></span>                        |
| <span data-ttu-id="48f5b-176">Teilweise geliefert</span><span class="sxs-lookup"><span data-stu-id="48f5b-176">Partially Delivered</span></span> | <span data-ttu-id="48f5b-177">Aktiv</span><span class="sxs-lookup"><span data-stu-id="48f5b-177">Active</span></span>          | <span data-ttu-id="48f5b-178">Offene Bestellung</span><span class="sxs-lookup"><span data-stu-id="48f5b-178">Open Order</span></span>                        |
| <span data-ttu-id="48f5b-179">Teilweise fakturiert</span><span class="sxs-lookup"><span data-stu-id="48f5b-179">Partially Invoiced</span></span>  | <span data-ttu-id="48f5b-180">Aktiv</span><span class="sxs-lookup"><span data-stu-id="48f5b-180">Active</span></span>          | <span data-ttu-id="48f5b-181">Offene Bestellung</span><span class="sxs-lookup"><span data-stu-id="48f5b-181">Open Order</span></span>                        |
| <span data-ttu-id="48f5b-182">Teilweise fakturiert</span><span class="sxs-lookup"><span data-stu-id="48f5b-182">Partially Invoiced</span></span>  | <span data-ttu-id="48f5b-183">Erfüllt</span><span class="sxs-lookup"><span data-stu-id="48f5b-183">Fulfilled</span></span>       | <span data-ttu-id="48f5b-184">Geliefert</span><span class="sxs-lookup"><span data-stu-id="48f5b-184">Delivered</span></span>                         |
| <span data-ttu-id="48f5b-185">Fakturiert</span><span class="sxs-lookup"><span data-stu-id="48f5b-185">Invoiced</span></span>            | <span data-ttu-id="48f5b-186">Fakturiert</span><span class="sxs-lookup"><span data-stu-id="48f5b-186">Invoiced</span></span>        | <span data-ttu-id="48f5b-187">Fakturiert</span><span class="sxs-lookup"><span data-stu-id="48f5b-187">Invoiced</span></span>                          |
| <span data-ttu-id="48f5b-188">Storniert</span><span class="sxs-lookup"><span data-stu-id="48f5b-188">Cancelled</span></span>           | <span data-ttu-id="48f5b-189">Storniert</span><span class="sxs-lookup"><span data-stu-id="48f5b-189">Cancelled</span></span>       | <span data-ttu-id="48f5b-190">Storniert</span><span class="sxs-lookup"><span data-stu-id="48f5b-190">Cancelled</span></span>                         |

## <a name="setup"></a><span data-ttu-id="48f5b-191">Setup</span><span class="sxs-lookup"><span data-stu-id="48f5b-191">Setup</span></span>

<span data-ttu-id="48f5b-192">Um die Zuordnung für die Auftragsstatusfelder einzurichten, müssen Sie die **IsSOPIntegrationEnabled** und **isIntegrationUser**-Attribute aktivieren.</span><span class="sxs-lookup"><span data-stu-id="48f5b-192">To set up the mapping for the sales order status fields, you must enable the **IsSOPIntegrationEnabled** and **isIntegrationUser** attributes.</span></span>

<span data-ttu-id="48f5b-193">Um das **IsSOPIntegrationEnabled**-Attribut zu aktivieren, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="48f5b-193">To enable the **IsSOPIntegrationEnabled** attribute, follow these steps.</span></span>

1. <span data-ttu-id="48f5b-194">Gehen Sie in einem Webbrowser zu `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`.</span><span class="sxs-lookup"><span data-stu-id="48f5b-194">In a browser, go to `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`.</span></span> <span data-ttu-id="48f5b-195">Ersetzen Sie **\<test-name\>** durch den Link Ihres Unternehmens zu Sales.</span><span class="sxs-lookup"><span data-stu-id="48f5b-195">Replace **\<test-name\>** with your company's link to Sales.</span></span>
2. <span data-ttu-id="48f5b-196">Suchen Sie auf der geöffneten Seite **organisationid** und notieren Sie sich den Wert.</span><span class="sxs-lookup"><span data-stu-id="48f5b-196">On the page that is opened, find **organizationid**, and make a note of the value.</span></span>

    ![Suchen von organizationid](media/sales-map-orgid.png)

3. <span data-ttu-id="48f5b-198">Öffnen Sie in Sales die Browserkonsole und führen Sie das folgende Skript aus.</span><span class="sxs-lookup"><span data-stu-id="48f5b-198">In Sales, open the browser console, and run following script.</span></span> <span data-ttu-id="48f5b-199">Verwenden Sie den **organisationid**-Wert aus Schritt 2.</span><span class="sxs-lookup"><span data-stu-id="48f5b-199">Use the **organizationid** value from step 2.</span></span>

    ```javascript
    Xrm.WebApi.updateRecord("organization",
    "d9a7c5f7-acbf-4aa9-86e8-a891c43f748c", {"issopintegrationenabled" :
    true}).then(
        function success(result) {
            console.log("Account updated");
            // perform operations on record update
        },
        function (error) {
            console.log(error.message);
            // handle error conditions
        }
    );
    ```

    ![JavaScript-Code in der Browserkonsole](media/sales-map-script.png)

4. <span data-ttu-id="48f5b-201">Überprüfen Sie, ob **IsSOPIntegrationEnabled** auf **true** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="48f5b-201">Verify that **IsSOPIntegrationEnabled** is set to **true**.</span></span> <span data-ttu-id="48f5b-202">Verwenden Sie die URL aus Schritt 1, um den Wert zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="48f5b-202">Use the URL from step 1 to check the value.</span></span>

    ![Auf true festgelegtes IsSOPIntegrationEnabled](media/sales-map-integration-enabled.png)

<span data-ttu-id="48f5b-204">Um das **isIntegrationUser**-Attribut zu aktivieren, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="48f5b-204">To enable the **isIntegrationUser** attribute, follow these steps.</span></span>

1. <span data-ttu-id="48f5b-205">Gehen Sie in Sales zu **Einstellung \> Anpassung \> System anpassen**, wählen Sie **Benutzerentität** aus und öffnen Sie dann **Formular \> Benutzer**.</span><span class="sxs-lookup"><span data-stu-id="48f5b-205">In Sales, go to **Setting \> Customization \> Customize the System**, select **User entity**, and then open **Form \> User**.</span></span>

    ![Öffnen des Benutzerformulars](media/sales-map-user.png)

2. <span data-ttu-id="48f5b-207">Suchen Sie im Feld-Explorer **Integrationsbenutzermodus** und klicken Sie zweimal darauf, um es dem Formular hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="48f5b-207">In Field Explorer, find **Integration user mode**, and double-click it to add it to the form.</span></span> <span data-ttu-id="48f5b-208">Speichern Sie die Änderung.</span><span class="sxs-lookup"><span data-stu-id="48f5b-208">Save your change.</span></span>

    ![Hinzufügen des Felds „Integrationsbenutzermodus“ zum Formular](media/sales-map-field-explorer.png)

3. <span data-ttu-id="48f5b-210">Gehen Sie in Sales zu **Einstellung \> Sicherheit \> Benutzer** und ändern Sie die Ansicht von **Aktivierte Benutzer** zu **Anwendungsbenutzer**.</span><span class="sxs-lookup"><span data-stu-id="48f5b-210">In Sales, go to **Setting \> Security \> Users**, and change the view from **Enabled Users** to **Application Users**.</span></span>

    ![Ändern der Ansicht von „Aktivierte Benutzer“ zu „Anwendungsbenutzer“](media/sales-map-enabled-users.png)

4. <span data-ttu-id="48f5b-212">Wählen Sie die beiden Einträge für **DualWrite IntegrationUser** aus.</span><span class="sxs-lookup"><span data-stu-id="48f5b-212">Select the two entries for **DualWrite IntegrationUser**.</span></span>

    ![Liste der Anwendungsbenutzer](media/sales-map-user-mode.png)

5. <span data-ttu-id="48f5b-214">Ändern Sie den Wert des **Integrationsbenutzermodus**-Felds auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="48f5b-214">Change the value of the **Integration user mode** field to **Yes**.</span></span>

    ![Ändern des Werts des Integrationsbenutzermodus-Felds](media/sales-map-user-mode-yes.png)

<span data-ttu-id="48f5b-216">Ihre Aufträge sind jetzt zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="48f5b-216">Your sales orders are now mapped.</span></span>
