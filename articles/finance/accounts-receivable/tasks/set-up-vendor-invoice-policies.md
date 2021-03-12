---
title: Kreditorenrechnungsrichtlinien einrichten
description: In diesem Thema wird erläutert, wie Richtlinien für Kreditorenrechnungen eingerichtet werden.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 79cbabba74fdb76d8fcc0553d39e0f140aacf03e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995449"
---
# <a name="set-up-vendor-invoice-policies"></a><span data-ttu-id="5b3e8-103">Kreditorenrechnungsrichtlinien einrichten</span><span class="sxs-lookup"><span data-stu-id="5b3e8-103">Set up vendor invoice policies</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5b3e8-104">In diesem Thema wird erläutert, wie Richtlinien für Kreditorenrechnungen eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="5b3e8-104">This topic explains how to set up vendor invoice policies.</span></span> <span data-ttu-id="5b3e8-105">Kreditorenrechnungsrichtlinien werden ausgeführt, wenn Sie mit der Seite "Kreditorenrechnung" eine Kreditorenrechnung buchen und wenn Sie die Seite "Richtlinienverstöße" der Kreditorenrechnung öffnen.</span><span class="sxs-lookup"><span data-stu-id="5b3e8-105">Vendor invoice policies are run when you post a vendor invoice by using the Vendor invoice page and when you open the vendor invoice Policy violations page.</span></span> <span data-ttu-id="5b3e8-106">Sie können auch den Workflow für Kreditorenrechnungen konfigurieren, sodass Kreditorenrechnungsrichtlinien immer ausgeführt werden, wenn eine Rechnung an den Workflow übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="5b3e8-106">You can also configure the vendor invoice workflow to run vendor invoice policies every time that you submit an invoice to workflow.</span></span> 

- <span data-ttu-id="5b3e8-107">Kreditorenrechnungsrichtlinien werden nicht auf Rechnungen angewendet, die im Rechnungsbuch oder in einer Rechnungserfassung erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="5b3e8-107">Vendor invoice policies do not apply to invoices that were created in the invoice register or invoice journal.</span></span>  
- <span data-ttu-id="5b3e8-108">Für die Rechnungsabgleichüberprüfung werden keine Kreditorenrechnungsrichtlinien verwendet. Stattdessen wird die Prüfung auf der Seite "Kreditorenkontenparameter" eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="5b3e8-108">Invoice matching validation does not use vendor invoice policies, but is instead set up in the Accounts payable parameters page.</span></span>  
- <span data-ttu-id="5b3e8-109">Für diese Erfassung wird das Demo-Unternehmen USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="5b3e8-109">This recording uses the USMF demo company.</span></span> <span data-ttu-id="5b3e8-110">Die Kreditorenleiter- oder Buchhaltungsleiterrolle würde diese Schritte ausführen.</span><span class="sxs-lookup"><span data-stu-id="5b3e8-110">The accounts payable manager or accounting manager role would perform these steps.</span></span> <span data-ttu-id="5b3e8-111">Stellen Sie zu Beginn sicher, dass der Konfigurationsschlüssel "Rechnungsabgleich" ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="5b3e8-111">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span>


## <a name="prepare-to-create-vendor-invoice-policies"></a><span data-ttu-id="5b3e8-112">Vorbereitung zum Erstellen von Kreditorenrechnungsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="5b3e8-112">Prepare to create vendor invoice policies</span></span>
1. <span data-ttu-id="5b3e8-113">Wechseln Sie zu **Navigationsbereich > Module > Kreditoren > Einstellung > Kreditorenkontenparameter**.</span><span class="sxs-lookup"><span data-stu-id="5b3e8-113">Go to **Navigation pane > Modules > Accounts payable > Setup > Accounts payable parameters**.</span></span>
2. <span data-ttu-id="5b3e8-114">Wählen Sie die Registerkarte **Rechnungsprüfung**.</span><span class="sxs-lookup"><span data-stu-id="5b3e8-114">Select the **Invoice validation** tab.</span></span>
3. <span data-ttu-id="5b3e8-115">Aktivieren oder deaktivieren Sie das Kontrollkästchen **Rechnungskopfstatus automatisch aktualisieren**.</span><span class="sxs-lookup"><span data-stu-id="5b3e8-115">Select or clear the **Automatically update invoice header** status check box.</span></span>
4. <span data-ttu-id="5b3e8-116">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b3e8-116">Select **OK**.</span></span>
5. <span data-ttu-id="5b3e8-117">Wählen Sie im Feld **Rechnung mit Abweichungen buchen** eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="5b3e8-117">In the **Post invoice with discrepancies** field, select an option.</span></span>
6. <span data-ttu-id="5b3e8-118">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="5b3e8-118">Close the page.</span></span>
7. <span data-ttu-id="5b3e8-119">Wechseln Sie zu **Navigationsbereich > Module > Kreditoren > Richtlinieneinstellungen > Richtlinien für Kreditorenrechnung**.</span><span class="sxs-lookup"><span data-stu-id="5b3e8-119">Go to **Navigation pane > Modules > Accounts payable > Policy setup > Vendor invoice policies**.</span></span>
8. <span data-ttu-id="5b3e8-120">Wählen Sie **Parameter** aus.</span><span class="sxs-lookup"><span data-stu-id="5b3e8-120">Select **Parameters**.</span></span>
9. <span data-ttu-id="5b3e8-121">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="5b3e8-121">Select **Add**.</span></span>
10. <span data-ttu-id="5b3e8-122">Schließen Sie die Seite, um zur Startseite zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="5b3e8-122">Close the page to return to the home page.</span></span>

## <a name="create-policy-rule-types-for-vendor-invoices"></a><span data-ttu-id="5b3e8-123">Erstellen von Richtlinienregeltypen für Kreditorenrechnungen</span><span class="sxs-lookup"><span data-stu-id="5b3e8-123">Create policy rule types for vendor invoices</span></span>
1. <span data-ttu-id="5b3e8-124">Wechseln Sie zu **Navigationsbereich > Module > Kreditoren > Richtlinieneinstellungen > Richtlinienregeltypen für Kreditorenrechnungen**.</span><span class="sxs-lookup"><span data-stu-id="5b3e8-124">Go to **Navigation pane > Modules > Accounts payable > Policy setup > Vendor invoice policy rule types**.</span></span>
2. <span data-ttu-id="5b3e8-125">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="5b3e8-125">Select **New**.</span></span>
3. <span data-ttu-id="5b3e8-126">Geben Sie in den Feldern **Regelname** und **Beschreibung** Werte ein.</span><span class="sxs-lookup"><span data-stu-id="5b3e8-126">In the **Rule name** and **Description** fields, type values.</span></span>
4. <span data-ttu-id="5b3e8-127">Wählen Sie im Feld **Abfragename** die Dropdown-Schaltfläche aus, um die Suche zu öffnen, und wählen Sie dann den gewünschten Datensatz aus.</span><span class="sxs-lookup"><span data-stu-id="5b3e8-127">In the **Query name** field, select the drop-down button to open the lookup, then select the desired record.</span></span>
5. <span data-ttu-id="5b3e8-128">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="5b3e8-128">Select **Save**.</span></span>
6. <span data-ttu-id="5b3e8-129">Schließen Sie die Seite, um zur Startseite zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="5b3e8-129">Close the page to return to the home page.</span></span>

## <a name="define-a-vendor-invoice-policy"></a><span data-ttu-id="5b3e8-130">Definieren einer Kreditorenrechnungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="5b3e8-130">Define a vendor invoice policy</span></span>
1. <span data-ttu-id="5b3e8-131">Wechseln Sie zu **Navigationsbereich > Module > Kreditoren > Richtlinieneinstellungen > Richtlinien für Kreditorenrechnung**.</span><span class="sxs-lookup"><span data-stu-id="5b3e8-131">Go to **Navigation pane > Modules > Accounts payable > Policy setup > Vendor invoice policies**.</span></span>
2. <span data-ttu-id="5b3e8-132">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="5b3e8-132">Select **New**.</span></span>
3. <span data-ttu-id="5b3e8-133">Geben Sie in den Feldern **Name** und **Beschreibung** Werte ein.</span><span class="sxs-lookup"><span data-stu-id="5b3e8-133">In the **Name** and **Description** fields, type values.</span></span>
4. <span data-ttu-id="5b3e8-134">Erweitern oder reduzieren Sie den Abschnitt **Richtlinienorganisationen**.</span><span class="sxs-lookup"><span data-stu-id="5b3e8-134">Expand or collapse the **Policy organizations** section.</span></span>
5. <span data-ttu-id="5b3e8-135">Wählen Sie in der Struktur **Contoso Unterhaltungsanlagen USA** aus.</span><span class="sxs-lookup"><span data-stu-id="5b3e8-135">In the tree, select **Contoso Entertainment System USA**.</span></span>
6. <span data-ttu-id="5b3e8-136">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="5b3e8-136">Select **Add**.</span></span>
7. <span data-ttu-id="5b3e8-137">Erweitern oder reduzieren Sie den Abschnitt **Richtlinienregeln**.</span><span class="sxs-lookup"><span data-stu-id="5b3e8-137">Expand or collapse the **Policy rules** section.</span></span>
8. <span data-ttu-id="5b3e8-138">Wählen Sie **Richtlinienregel erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="5b3e8-138">Select **Create policy rule**.</span></span>
9. <span data-ttu-id="5b3e8-139">Geben Sie im Feld **Beschreibung der Richtlinienregel** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="5b3e8-139">In the **Policy rule description** field, type a value.</span></span>
10. <span data-ttu-id="5b3e8-140">Wählen Sie **Filter** aus.</span><span class="sxs-lookup"><span data-stu-id="5b3e8-140">Select **Filter**.</span></span>
11. <span data-ttu-id="5b3e8-141">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="5b3e8-141">Select **Add**.</span></span> <span data-ttu-id="5b3e8-142">Wählen Sie den gewünschten Datensatz aus.</span><span class="sxs-lookup"><span data-stu-id="5b3e8-142">Select the desired record.</span></span>
12. <span data-ttu-id="5b3e8-143">Wählen Sie in den Feldern **Tabelle**, **Abgeleitete Tabelle** und **Feld** Optionen aus den Dropdownmenüs aus, oder geben Sie Werte ein..</span><span class="sxs-lookup"><span data-stu-id="5b3e8-143">In the **Table**, **Derived table**, and **Field** fields, select or enter options from the drop-down menus.</span></span>
13. <span data-ttu-id="5b3e8-144">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="5b3e8-144">Close the page.</span></span>
14. <span data-ttu-id="5b3e8-145">Geben Sie im Feld **Kriterien** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="5b3e8-145">In the **Criteria** field, type a value.</span></span>
15. <span data-ttu-id="5b3e8-146">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b3e8-146">Select **OK**.</span></span>
16. <span data-ttu-id="5b3e8-147">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b3e8-147">Select **OK**.</span></span>
17. <span data-ttu-id="5b3e8-148">Schließen Sie die Seiten, um zur Startseite zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="5b3e8-148">Close the pages to return to the home page.</span></span>

