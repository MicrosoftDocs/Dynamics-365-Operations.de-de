---
title: Kreditorenrechnungsrichtlinien einrichten
description: In diesem Thema wird erläutert, wie Richtlinien für Kreditorenrechnungen eingerichtet werden.
author: ShivamPandey-msft
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c088f6e3fea7c218cfd2108d0f279bccf1292772
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816195"
---
# <a name="set-up-vendor-invoice-policies"></a><span data-ttu-id="eed69-103">Kreditorenrechnungsrichtlinien einrichten</span><span class="sxs-lookup"><span data-stu-id="eed69-103">Set up vendor invoice policies</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="eed69-104">In diesem Thema wird erläutert, wie Richtlinien für Kreditorenrechnungen eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="eed69-104">This topic explains how to set up vendor invoice policies.</span></span> <span data-ttu-id="eed69-105">Kreditorenrechnungsrichtlinien werden ausgeführt, wenn Sie mit der Seite "Kreditorenrechnung" eine Kreditorenrechnung buchen und wenn Sie die Seite "Richtlinienverstöße" der Kreditorenrechnung öffnen.</span><span class="sxs-lookup"><span data-stu-id="eed69-105">Vendor invoice policies are run when you post a vendor invoice by using the Vendor invoice page and when you open the vendor invoice Policy violations page.</span></span> <span data-ttu-id="eed69-106">Sie können auch den Workflow für Kreditorenrechnungen konfigurieren, sodass Kreditorenrechnungsrichtlinien immer ausgeführt werden, wenn eine Rechnung an den Workflow übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="eed69-106">You can also configure the vendor invoice workflow to run vendor invoice policies every time that you submit an invoice to workflow.</span></span> 

- <span data-ttu-id="eed69-107">Kreditorenrechnungsrichtlinien werden nicht auf Rechnungen angewendet, die im Rechnungsbuch oder in einer Rechnungserfassung erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="eed69-107">Vendor invoice policies do not apply to invoices that were created in the invoice register or invoice journal.</span></span>  
- <span data-ttu-id="eed69-108">Für die Rechnungsabgleichüberprüfung werden keine Kreditorenrechnungsrichtlinien verwendet. Stattdessen wird die Prüfung auf der Seite "Kreditorenkontenparameter" eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="eed69-108">Invoice matching validation does not use vendor invoice policies, but is instead set up in the Accounts payable parameters page.</span></span>  
- <span data-ttu-id="eed69-109">Für diese Erfassung wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="eed69-109">This recording uses the USMF demo company.</span></span> <span data-ttu-id="eed69-110">Die Kreditorenleiter- oder Buchhaltungsleiterrolle würde diese Schritte ausführen.</span><span class="sxs-lookup"><span data-stu-id="eed69-110">The accounts payable manager or accounting manager role would perform these steps.</span></span> <span data-ttu-id="eed69-111">Stellen Sie zu Beginn sicher, dass der Konfigurationsschlüssel "Rechnungsabgleich" ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="eed69-111">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span>


## <a name="prepare-to-create-vendor-invoice-policies"></a><span data-ttu-id="eed69-112">Vorbereitung zum Erstellen von Kreditorenrechnungsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="eed69-112">Prepare to create vendor invoice policies</span></span>
1. <span data-ttu-id="eed69-113">Wechseln Sie zu **Navigationsbereich > Module > Kreditoren > Einstellung > Kreditorenkontenparameter**.</span><span class="sxs-lookup"><span data-stu-id="eed69-113">Go to **Navigation pane > Modules > Accounts payable > Setup > Accounts payable parameters**.</span></span>
2. <span data-ttu-id="eed69-114">Wählen Sie die Registerkarte **Rechnungsprüfung**.</span><span class="sxs-lookup"><span data-stu-id="eed69-114">Select the **Invoice validation** tab.</span></span>
3. <span data-ttu-id="eed69-115">Aktivieren oder deaktivieren Sie das Kontrollkästchen **Rechnungskopfstatus automatisch aktualisieren**.</span><span class="sxs-lookup"><span data-stu-id="eed69-115">Select or clear the **Automatically update invoice header** status check box.</span></span>
4. <span data-ttu-id="eed69-116">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="eed69-116">Select **OK**.</span></span>
5. <span data-ttu-id="eed69-117">Wählen Sie im Feld **Rechnung mit Abweichungen buchen** eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="eed69-117">In the **Post invoice with discrepancies** field, select an option.</span></span>
6. <span data-ttu-id="eed69-118">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="eed69-118">Close the page.</span></span>
7. <span data-ttu-id="eed69-119">Wechseln Sie zu **Navigationsbereich > Module > Kreditoren > Richtlinieneinstellungen > Richtlinien für Kreditorenrechnung**.</span><span class="sxs-lookup"><span data-stu-id="eed69-119">Go to **Navigation pane > Modules > Accounts payable > Policy setup > Vendor invoice policies**.</span></span>
8. <span data-ttu-id="eed69-120">Wählen Sie **Parameter** aus.</span><span class="sxs-lookup"><span data-stu-id="eed69-120">Select **Parameters**.</span></span>
9. <span data-ttu-id="eed69-121">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="eed69-121">Select **Add**.</span></span>
10. <span data-ttu-id="eed69-122">Schließen Sie die Seite, um zur Startseite zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="eed69-122">Close the page to return to the home page.</span></span>

## <a name="create-policy-rule-types-for-vendor-invoices"></a><span data-ttu-id="eed69-123">Erstellen von Richtlinienregeltypen für Kreditorenrechnungen</span><span class="sxs-lookup"><span data-stu-id="eed69-123">Create policy rule types for vendor invoices</span></span>
1. <span data-ttu-id="eed69-124">Wechseln Sie zu **Navigationsbereich > Module > Kreditoren > Richtlinieneinstellungen > Richtlinienregeltypen für Kreditorenrechnungen**.</span><span class="sxs-lookup"><span data-stu-id="eed69-124">Go to **Navigation pane > Modules > Accounts payable > Policy setup > Vendor invoice policy rule types**.</span></span>
2. <span data-ttu-id="eed69-125">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="eed69-125">Select **New**.</span></span>
3. <span data-ttu-id="eed69-126">Geben Sie in den Feldern **Regelname** und **Beschreibung** Werte ein.</span><span class="sxs-lookup"><span data-stu-id="eed69-126">In the **Rule name** and **Description** fields, type values.</span></span>
4. <span data-ttu-id="eed69-127">Wählen Sie im Feld **Abfragename** die Dropdown-Schaltfläche aus, um die Suche zu öffnen, und wählen Sie dann den gewünschten Datensatz aus.</span><span class="sxs-lookup"><span data-stu-id="eed69-127">In the **Query name** field, select the drop-down button to open the lookup, then select the desired record.</span></span>
5. <span data-ttu-id="eed69-128">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="eed69-128">Select **Save**.</span></span>
6. <span data-ttu-id="eed69-129">Schließen Sie die Seite, um zur Startseite zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="eed69-129">Close the page to return to the home page.</span></span>

## <a name="define-a-vendor-invoice-policy"></a><span data-ttu-id="eed69-130">Definieren einer Kreditorenrechnungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="eed69-130">Define a vendor invoice policy</span></span>
1. <span data-ttu-id="eed69-131">Wechseln Sie zu **Navigationsbereich > Module > Kreditoren > Richtlinieneinstellungen > Richtlinien für Kreditorenrechnung**.</span><span class="sxs-lookup"><span data-stu-id="eed69-131">Go to **Navigation pane > Modules > Accounts payable > Policy setup > Vendor invoice policies**.</span></span>
2. <span data-ttu-id="eed69-132">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="eed69-132">Select **New**.</span></span>
3. <span data-ttu-id="eed69-133">Geben Sie in den Feldern **Name** und **Beschreibung** Werte ein.</span><span class="sxs-lookup"><span data-stu-id="eed69-133">In the **Name** and **Description** fields, type values.</span></span>
4. <span data-ttu-id="eed69-134">Erweitern oder reduzieren Sie den Abschnitt **Richtlinienorganisationen**.</span><span class="sxs-lookup"><span data-stu-id="eed69-134">Expand or collapse the **Policy organizations** section.</span></span>
5. <span data-ttu-id="eed69-135">Wählen Sie in der Struktur **Contoso Unterhaltungsanlagen USA** aus.</span><span class="sxs-lookup"><span data-stu-id="eed69-135">In the tree, select **Contoso Entertainment System USA**.</span></span>
6. <span data-ttu-id="eed69-136">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="eed69-136">Select **Add**.</span></span>
7. <span data-ttu-id="eed69-137">Erweitern oder reduzieren Sie den Abschnitt **Richtlinienregeln**.</span><span class="sxs-lookup"><span data-stu-id="eed69-137">Expand or collapse the **Policy rules** section.</span></span>
8. <span data-ttu-id="eed69-138">Wählen Sie **Richtlinienregel erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="eed69-138">Select **Create policy rule**.</span></span>
9. <span data-ttu-id="eed69-139">Geben Sie im Feld **Beschreibung der Richtlinienregel** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="eed69-139">In the **Policy rule description** field, type a value.</span></span>
10. <span data-ttu-id="eed69-140">Wählen Sie **Filter** aus.</span><span class="sxs-lookup"><span data-stu-id="eed69-140">Select **Filter**.</span></span>
11. <span data-ttu-id="eed69-141">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="eed69-141">Select **Add**.</span></span> <span data-ttu-id="eed69-142">Wählen Sie den gewünschten Datensatz aus.</span><span class="sxs-lookup"><span data-stu-id="eed69-142">Select the desired record.</span></span>
12. <span data-ttu-id="eed69-143">Wählen Sie in den Feldern **Tabelle**, **Abgeleitete Tabelle** und **Feld** Optionen aus den Dropdownmenüs aus, oder geben Sie Werte ein..</span><span class="sxs-lookup"><span data-stu-id="eed69-143">In the **Table**, **Derived table**, and **Field** fields, select or enter options from the drop-down menus.</span></span>
13. <span data-ttu-id="eed69-144">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="eed69-144">Close the page.</span></span>
14. <span data-ttu-id="eed69-145">Geben Sie im Feld **Kriterien** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="eed69-145">In the **Criteria** field, type a value.</span></span>
15. <span data-ttu-id="eed69-146">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="eed69-146">Select **OK**.</span></span>
16. <span data-ttu-id="eed69-147">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="eed69-147">Select **OK**.</span></span>
17. <span data-ttu-id="eed69-148">Schließen Sie die Seiten, um zur Startseite zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="eed69-148">Close the pages to return to the home page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]