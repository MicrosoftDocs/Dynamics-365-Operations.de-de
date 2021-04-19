---
title: Zuordnung für die Kundenauftragsstatusspalten einrichten
description: In diesem Thema wird erläutert, wie Sie die Auftragsstatusspalten für duales Schreiben einrichten.
author: dasani-madipalli
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: damadipa
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-06-25
ms.openlocfilehash: 9afa64df73aa17e7a15a0ee4f4529ac74bcd3c67
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750713"
---
# <a name="set-up-the-mapping-for-the-sales-order-status-columns"></a><span data-ttu-id="33ee2-103">Zuordnung für die Kundenauftragsstatusspalten einrichten</span><span class="sxs-lookup"><span data-stu-id="33ee2-103">Set up the mapping for the sales order status columns</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="33ee2-104">Die Spalten, die den Auftragsstatus angeben, haben in Microsoft Dynamics 365 Supply Chain Management und Dynamics 365 Sales unterschiedliche Aufzählungswerte.</span><span class="sxs-lookup"><span data-stu-id="33ee2-104">The columns that indicate sales order status have different enumeration values in Microsoft Dynamics 365 Supply Chain Management and Dynamics 365 Sales.</span></span> <span data-ttu-id="33ee2-105">Zusätzliche Einstellungen sind erforderlich, um diese Spalten in Dual-Write abzubilden.</span><span class="sxs-lookup"><span data-stu-id="33ee2-105">Additional setup is required to map these columns in dual-write.</span></span>

## <a name="columns-in-supply-chain-management"></a><span data-ttu-id="33ee2-106">Spalten in Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="33ee2-106">columns in Supply Chain Management</span></span>

<span data-ttu-id="33ee2-107">In Supply Chain Management spiegeln zwei Spalten den Status des Auftrags wider.</span><span class="sxs-lookup"><span data-stu-id="33ee2-107">In Supply Chain Management, two columns reflect the status of the sales order.</span></span> <span data-ttu-id="33ee2-108">Die Spalten, die Sie zuordnen müssen, sind **Status** und **Dokumentstatus**.</span><span class="sxs-lookup"><span data-stu-id="33ee2-108">The columns that you must map are **Status** and **Document Status**.</span></span>

<span data-ttu-id="33ee2-109">Die **Status**-Aufzählung gibt den Gesamtstatus der Bestellung an.</span><span class="sxs-lookup"><span data-stu-id="33ee2-109">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="33ee2-110">Dieser Status wird im Auftragskopf angezeigt.</span><span class="sxs-lookup"><span data-stu-id="33ee2-110">This status is shown on the order header.</span></span>

<span data-ttu-id="33ee2-111">Die **Status**-Aufzählung hat die folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="33ee2-111">The **Status** enumeration has the following values:</span></span>

- <span data-ttu-id="33ee2-112">Offene Bestellung</span><span class="sxs-lookup"><span data-stu-id="33ee2-112">Open Order</span></span>
- <span data-ttu-id="33ee2-113">Geliefert</span><span class="sxs-lookup"><span data-stu-id="33ee2-113">Delivered</span></span>
- <span data-ttu-id="33ee2-114">Fakturiert</span><span class="sxs-lookup"><span data-stu-id="33ee2-114">Invoiced</span></span>
- <span data-ttu-id="33ee2-115">Storniert</span><span class="sxs-lookup"><span data-stu-id="33ee2-115">Cancelled</span></span>

<span data-ttu-id="33ee2-116">Die **Dokumentstatus**-Aufzählung gibt das letzte Dokument an, das für die Bestellung generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="33ee2-116">The **Document Status** enumeration specifies the most recent document that was generated for the order.</span></span> <span data-ttu-id="33ee2-117">Wenn die Bestellung beispielsweise bestätigt wird, handelt es sich bei diesem Dokument um eine Auftragsbestätigung.</span><span class="sxs-lookup"><span data-stu-id="33ee2-117">For example, if the order is confirmed, this document is a sales order confirmation.</span></span> <span data-ttu-id="33ee2-118">Wenn ein Kundenauftrag teilweise in Rechnung gestellt wird und dann die verbleibende Position bestätigt wird, bleibt der Belegstatus **Rechnung** erhalten, weil die Rechnung später im Prozess generiert wird.</span><span class="sxs-lookup"><span data-stu-id="33ee2-118">If a sales order is partially invoiced, and then the remaining line is confirmed, the document status remains **Invoice**, because the invoice is generated later in the process.</span></span>

<span data-ttu-id="33ee2-119">Die **Dokumentstatus**-Aufzählung hat die folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="33ee2-119">The **Document Status** enumeration has the following values:</span></span>

- <span data-ttu-id="33ee2-120">Bestätigung</span><span class="sxs-lookup"><span data-stu-id="33ee2-120">Confirmation</span></span>
- <span data-ttu-id="33ee2-121">Kommissionierliste</span><span class="sxs-lookup"><span data-stu-id="33ee2-121">Picking List</span></span>
- <span data-ttu-id="33ee2-122">Lieferschein</span><span class="sxs-lookup"><span data-stu-id="33ee2-122">Packing Slip</span></span>
- <span data-ttu-id="33ee2-123">Rechnung</span><span class="sxs-lookup"><span data-stu-id="33ee2-123">Invoice</span></span>

## <a name="columns-in-sales"></a><span data-ttu-id="33ee2-124">Spalten in Sales</span><span class="sxs-lookup"><span data-stu-id="33ee2-124">columns in Sales</span></span>

<span data-ttu-id="33ee2-125">In Sales geben zwei Felder den Status der Bestellung an.</span><span class="sxs-lookup"><span data-stu-id="33ee2-125">In Sales, two columns indicate the status of the order.</span></span> <span data-ttu-id="33ee2-126">Die Spalten, die Sie zuordnen müssen, sind **Status** und **Verarbeitungsstatus**.</span><span class="sxs-lookup"><span data-stu-id="33ee2-126">The columns that you must map are **Status** and **Processing Status**.</span></span>

<span data-ttu-id="33ee2-127">Die **Status**-Aufzählung gibt den Gesamtstatus der Bestellung an.</span><span class="sxs-lookup"><span data-stu-id="33ee2-127">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="33ee2-128">Es weist die folgenden Werte auf:</span><span class="sxs-lookup"><span data-stu-id="33ee2-128">It has the following values:</span></span>

- <span data-ttu-id="33ee2-129">Aktiv</span><span class="sxs-lookup"><span data-stu-id="33ee2-129">Active</span></span>
- <span data-ttu-id="33ee2-130">Übermittelt</span><span class="sxs-lookup"><span data-stu-id="33ee2-130">Submitted</span></span>
- <span data-ttu-id="33ee2-131">Erfüllt</span><span class="sxs-lookup"><span data-stu-id="33ee2-131">Fulfilled</span></span>
- <span data-ttu-id="33ee2-132">Fakturiert</span><span class="sxs-lookup"><span data-stu-id="33ee2-132">Invoiced</span></span>
- <span data-ttu-id="33ee2-133">Storniert</span><span class="sxs-lookup"><span data-stu-id="33ee2-133">Cancelled</span></span>

<span data-ttu-id="33ee2-134">Die Aufzählung **Verarbeitungsstatus** wurde eingeführt, damit der Status genau auf Supply Chain Management zugeordnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="33ee2-134">The **Processing Status** enumeration was introduced so that the status can be mapped more accurately with Supply Chain Management.</span></span>

<span data-ttu-id="33ee2-135">Die folgende Tabelle zeigt die Zuordnung von **Verarbeitungsstatus** auf Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="33ee2-135">The following table shows the mapping of **Processing Status** in Supply Chain Management.</span></span>

| <span data-ttu-id="33ee2-136">Verarbeitungsstatus</span><span class="sxs-lookup"><span data-stu-id="33ee2-136">Processing Status</span></span>   | <span data-ttu-id="33ee2-137">Status in Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="33ee2-137">Status in Supply Chain Management</span></span> | <span data-ttu-id="33ee2-138">Dokumentstatus in Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="33ee2-138">Document Status in Supply Chain Management</span></span> |
|---------------------|-----------------------------------|--------------------------------------------|
| <span data-ttu-id="33ee2-139">Aktiv</span><span class="sxs-lookup"><span data-stu-id="33ee2-139">Active</span></span>              | <span data-ttu-id="33ee2-140">Offene Bestellung</span><span class="sxs-lookup"><span data-stu-id="33ee2-140">Open Order</span></span>                        | <span data-ttu-id="33ee2-141">Keines</span><span class="sxs-lookup"><span data-stu-id="33ee2-141">None</span></span>                                       |
| <span data-ttu-id="33ee2-142">Bestätigt</span><span class="sxs-lookup"><span data-stu-id="33ee2-142">Confirmed</span></span>           | <span data-ttu-id="33ee2-143">Offene Bestellung</span><span class="sxs-lookup"><span data-stu-id="33ee2-143">Open Order</span></span>                        | <span data-ttu-id="33ee2-144">Bestätigung</span><span class="sxs-lookup"><span data-stu-id="33ee2-144">Confirmation</span></span>                               |
| <span data-ttu-id="33ee2-145">Entnommen</span><span class="sxs-lookup"><span data-stu-id="33ee2-145">Picked</span></span>              | <span data-ttu-id="33ee2-146">Offene Bestellung</span><span class="sxs-lookup"><span data-stu-id="33ee2-146">Open Order</span></span>                        | <span data-ttu-id="33ee2-147">Kommissionierliste</span><span class="sxs-lookup"><span data-stu-id="33ee2-147">Picking List</span></span>                               |
| <span data-ttu-id="33ee2-148">Teilweise geliefert</span><span class="sxs-lookup"><span data-stu-id="33ee2-148">Partially Delivered</span></span> | <span data-ttu-id="33ee2-149">Offene Bestellung</span><span class="sxs-lookup"><span data-stu-id="33ee2-149">Open Order</span></span>                        | <span data-ttu-id="33ee2-150">Lieferschein</span><span class="sxs-lookup"><span data-stu-id="33ee2-150">Packing Slip</span></span>                               |
| <span data-ttu-id="33ee2-151">Geliefert</span><span class="sxs-lookup"><span data-stu-id="33ee2-151">Delivered</span></span>           | <span data-ttu-id="33ee2-152">Geliefert</span><span class="sxs-lookup"><span data-stu-id="33ee2-152">Delivered</span></span>                         | <span data-ttu-id="33ee2-153">Lieferschein</span><span class="sxs-lookup"><span data-stu-id="33ee2-153">Packing Slip</span></span>                               |
| <span data-ttu-id="33ee2-154">Teilweise fakturiert</span><span class="sxs-lookup"><span data-stu-id="33ee2-154">Partially Invoiced</span></span>  | <span data-ttu-id="33ee2-155">Geliefert</span><span class="sxs-lookup"><span data-stu-id="33ee2-155">Delivered</span></span>                         | <span data-ttu-id="33ee2-156">Rechnung</span><span class="sxs-lookup"><span data-stu-id="33ee2-156">Invoice</span></span>                                    |
| <span data-ttu-id="33ee2-157">Fakturiert</span><span class="sxs-lookup"><span data-stu-id="33ee2-157">Invoiced</span></span>            | <span data-ttu-id="33ee2-158">Fakturiert</span><span class="sxs-lookup"><span data-stu-id="33ee2-158">Invoiced</span></span>                          | <span data-ttu-id="33ee2-159">Rechnung</span><span class="sxs-lookup"><span data-stu-id="33ee2-159">Invoice</span></span>                                    |
| <span data-ttu-id="33ee2-160">Storniert</span><span class="sxs-lookup"><span data-stu-id="33ee2-160">Cancelled</span></span>           | <span data-ttu-id="33ee2-161">Storniert</span><span class="sxs-lookup"><span data-stu-id="33ee2-161">Cancelled</span></span>                         | <span data-ttu-id="33ee2-162">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="33ee2-162">Not applicable</span></span>                             |

<span data-ttu-id="33ee2-163">Die folgende Tabelle zeigt die Zuordnung von **Verarbeitungsstatus** zwischen Sales und Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="33ee2-163">The following table shows the mapping of **Processing Status** between Sales and Supply Chain Management.</span></span>

| <span data-ttu-id="33ee2-164">Verarbeitungsstatus</span><span class="sxs-lookup"><span data-stu-id="33ee2-164">Processing Status</span></span>   | <span data-ttu-id="33ee2-165">Status in Sales</span><span class="sxs-lookup"><span data-stu-id="33ee2-165">Status in Sales</span></span> | <span data-ttu-id="33ee2-166">Status in Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="33ee2-166">Status in Supply Chain Management</span></span> |
|---------------------|-----------------|-----------------------------------|
| <span data-ttu-id="33ee2-167">Aktiv</span><span class="sxs-lookup"><span data-stu-id="33ee2-167">Active</span></span>              | <span data-ttu-id="33ee2-168">Aktiv</span><span class="sxs-lookup"><span data-stu-id="33ee2-168">Active</span></span>          | <span data-ttu-id="33ee2-169">Offene Bestellung</span><span class="sxs-lookup"><span data-stu-id="33ee2-169">Open Order</span></span>                        |
| <span data-ttu-id="33ee2-170">Bestätigt</span><span class="sxs-lookup"><span data-stu-id="33ee2-170">Confirmed</span></span>           | <span data-ttu-id="33ee2-171">Übermittelt</span><span class="sxs-lookup"><span data-stu-id="33ee2-171">Submitted</span></span>       | <span data-ttu-id="33ee2-172">Offene Bestellung</span><span class="sxs-lookup"><span data-stu-id="33ee2-172">Open Order</span></span>                        |
| <span data-ttu-id="33ee2-173">Entnommen</span><span class="sxs-lookup"><span data-stu-id="33ee2-173">Picked</span></span>              | <span data-ttu-id="33ee2-174">Übermittelt</span><span class="sxs-lookup"><span data-stu-id="33ee2-174">Submitted</span></span>       | <span data-ttu-id="33ee2-175">Offene Bestellung</span><span class="sxs-lookup"><span data-stu-id="33ee2-175">Open Order</span></span>                        |
| <span data-ttu-id="33ee2-176">Teilweise geliefert</span><span class="sxs-lookup"><span data-stu-id="33ee2-176">Partially Delivered</span></span> | <span data-ttu-id="33ee2-177">Aktiv</span><span class="sxs-lookup"><span data-stu-id="33ee2-177">Active</span></span>          | <span data-ttu-id="33ee2-178">Offene Bestellung</span><span class="sxs-lookup"><span data-stu-id="33ee2-178">Open Order</span></span>                        |
| <span data-ttu-id="33ee2-179">Teilweise fakturiert</span><span class="sxs-lookup"><span data-stu-id="33ee2-179">Partially Invoiced</span></span>  | <span data-ttu-id="33ee2-180">Aktiv</span><span class="sxs-lookup"><span data-stu-id="33ee2-180">Active</span></span>          | <span data-ttu-id="33ee2-181">Offene Bestellung</span><span class="sxs-lookup"><span data-stu-id="33ee2-181">Open Order</span></span>                        |
| <span data-ttu-id="33ee2-182">Teilweise fakturiert</span><span class="sxs-lookup"><span data-stu-id="33ee2-182">Partially Invoiced</span></span>  | <span data-ttu-id="33ee2-183">Erfüllt</span><span class="sxs-lookup"><span data-stu-id="33ee2-183">Fulfilled</span></span>       | <span data-ttu-id="33ee2-184">Geliefert</span><span class="sxs-lookup"><span data-stu-id="33ee2-184">Delivered</span></span>                         |
| <span data-ttu-id="33ee2-185">Fakturiert</span><span class="sxs-lookup"><span data-stu-id="33ee2-185">Invoiced</span></span>            | <span data-ttu-id="33ee2-186">Fakturiert</span><span class="sxs-lookup"><span data-stu-id="33ee2-186">Invoiced</span></span>        | <span data-ttu-id="33ee2-187">Fakturiert</span><span class="sxs-lookup"><span data-stu-id="33ee2-187">Invoiced</span></span>                          |
| <span data-ttu-id="33ee2-188">Storniert</span><span class="sxs-lookup"><span data-stu-id="33ee2-188">Cancelled</span></span>           | <span data-ttu-id="33ee2-189">Storniert</span><span class="sxs-lookup"><span data-stu-id="33ee2-189">Cancelled</span></span>       | <span data-ttu-id="33ee2-190">Storniert</span><span class="sxs-lookup"><span data-stu-id="33ee2-190">Cancelled</span></span>                         |

## <a name="setup"></a><span data-ttu-id="33ee2-191">Einstellung</span><span class="sxs-lookup"><span data-stu-id="33ee2-191">Setup</span></span>

<span data-ttu-id="33ee2-192">Um die Zuordnung für die Auftragsstatusspalten einzurichten, müssen Sie die Attribute **IsSOPIntegrationEnabled** und **isIntegrationUser** aktivieren.</span><span class="sxs-lookup"><span data-stu-id="33ee2-192">To set up the mapping for the sales order status columns, you must enable the **IsSOPIntegrationEnabled** and **isIntegrationUser** attributes.</span></span>

<span data-ttu-id="33ee2-193">Um das **IsSOPIntegrationEnabled**-Attribut zu aktivieren, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="33ee2-193">To enable the **IsSOPIntegrationEnabled** attribute, follow these steps.</span></span>

1. <span data-ttu-id="33ee2-194">Gehen Sie in einem Webbrowser zu `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`.</span><span class="sxs-lookup"><span data-stu-id="33ee2-194">In a browser, go to `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`.</span></span> <span data-ttu-id="33ee2-195">Ersetzen Sie **\<test-name\>** durch den Link Ihres Unternehmens zu Sales.</span><span class="sxs-lookup"><span data-stu-id="33ee2-195">Replace **\<test-name\>** with your company's link to Sales.</span></span>
2. <span data-ttu-id="33ee2-196">Suchen Sie auf der geöffneten Seite **organisationid** und notieren Sie sich den Wert.</span><span class="sxs-lookup"><span data-stu-id="33ee2-196">On the page that is opened, find **organizationid**, and make a note of the value.</span></span>

    ![Suchen von organizationid](media/sales-map-orgid.png)

3. <span data-ttu-id="33ee2-198">Öffnen Sie in Sales die Browserkonsole und führen Sie das folgende Skript aus.</span><span class="sxs-lookup"><span data-stu-id="33ee2-198">In Sales, open the browser console, and run following script.</span></span> <span data-ttu-id="33ee2-199">Verwenden Sie den **organisationid**-Wert aus Schritt 2.</span><span class="sxs-lookup"><span data-stu-id="33ee2-199">Use the **organizationid** value from step 2.</span></span>

    ```javascript
    Xrm.WebApi.updateRecord("organization",
    "d9a7c5f7-acbf-4aa9-86e8-a891c43f748c", {"issopintegrationenabled" :
    true}).then(
        function success(result) {
            console.log("Account updated");
            // perform operations on row update
        },
        function (error) {
            console.log(error.message);
            // handle error conditions
        }
    );
    ```

    ![JavaScript-Code in der Browserkonsole](media/sales-map-script.png)

4. <span data-ttu-id="33ee2-201">Überprüfen Sie, ob **IsSOPIntegrationEnabled** auf **true** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="33ee2-201">Verify that **IsSOPIntegrationEnabled** is set to **true**.</span></span> <span data-ttu-id="33ee2-202">Verwenden Sie die URL aus Schritt 1, um den Wert zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="33ee2-202">Use the URL from step 1 to check the value.</span></span>

    ![Auf true festgelegtes IsSOPIntegrationEnabled](media/sales-map-integration-enabled.png)

<span data-ttu-id="33ee2-204">Um das **isIntegrationUser**-Attribut zu aktivieren, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="33ee2-204">To enable the **isIntegrationUser** attribute, follow these steps.</span></span>

1. <span data-ttu-id="33ee2-205">Wechseln Sie in Sales zu **Einstellung \> Anpassung \> System anpassen**, wählen Sie **Benutzertabelle** aus und öffnen Sie dann **Formular \> Benutzer**.</span><span class="sxs-lookup"><span data-stu-id="33ee2-205">In Sales, go to **Setting \> Customization \> Customize the System**, select **User table**, and then open **Form \> User**.</span></span>

    ![Öffnen des Benutzerformulars](media/sales-map-user.png)

2. <span data-ttu-id="33ee2-207">Suchen Sie im Feld-Explorer **Integrationsbenutzermodus** und klicken Sie zweimal darauf, um es dem Formular hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="33ee2-207">In Field Explorer, find **Integration user mode**, and double-click it to add it to the form.</span></span> <span data-ttu-id="33ee2-208">Speichern Sie die Änderung.</span><span class="sxs-lookup"><span data-stu-id="33ee2-208">Save your change.</span></span>

    ![Hinzufügen der Spalte „Integrationsbenutzermodus“ zum Formular](media/sales-map-field-explorer.png)

3. <span data-ttu-id="33ee2-210">Gehen Sie in Sales zu **Einstellung \> Sicherheit \> Benutzer** und ändern Sie die Ansicht von **Aktivierte Benutzer** zu **Anwendungsbenutzer**.</span><span class="sxs-lookup"><span data-stu-id="33ee2-210">In Sales, go to **Setting \> Security \> Users**, and change the view from **Enabled Users** to **Application Users**.</span></span>

    ![Ändern der Ansicht von „Aktivierte Benutzer“ zu „Anwendungsbenutzer“](media/sales-map-enabled-users.png)

4. <span data-ttu-id="33ee2-212">Wählen Sie die beiden Einträge für **DualWrite IntegrationUser** aus.</span><span class="sxs-lookup"><span data-stu-id="33ee2-212">Select the two entries for **DualWrite IntegrationUser**.</span></span>

    ![Liste der Anwendungsbenutzer](media/sales-map-user-mode.png)

5. <span data-ttu-id="33ee2-214">Ändern Sie den Wert der Spalte **Integrationsbenutzermodus** in **Ja**.</span><span class="sxs-lookup"><span data-stu-id="33ee2-214">Change the value of the **Integration user mode** column to **Yes**.</span></span>

    ![Ändern des Werts der Spalte „Integrationsbenutzermodus“](media/sales-map-user-mode-yes.png)

<span data-ttu-id="33ee2-216">Ihre Aufträge sind jetzt zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="33ee2-216">Your sales orders are now mapped.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]