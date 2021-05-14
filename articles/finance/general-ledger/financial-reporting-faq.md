---
title: Häufig gestellte Fragen zur Finanzberichterstellung
description: In diesem Artikel werden Fragen anderer Benutzer zur Finanzberichterstellung beantwortet.
author: jiwo
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 023354b0e2973f63411bf81cbeb0344333c49112
ms.sourcegitcommit: d63e7e0593084a61362a6cad3937b1fd956c384f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "5923024"
---
# <a name="financial-reporting-faq"></a><span data-ttu-id="d3c0a-103">Häufig gestellte Fragen zur Finanzberichterstellung</span><span class="sxs-lookup"><span data-stu-id="d3c0a-103">Financial reporting FAQ</span></span> 

<span data-ttu-id="d3c0a-104">Dieser Artikel gibt Antwort auf häufig gestellte Fragen zur Finanzberichterstattung.</span><span class="sxs-lookup"><span data-stu-id="d3c0a-104">This topic provides answers to frequently asked questions about financial reporting.</span></span> 

## <a name="how-do-i-restrict-access-to-a-report-using-tree-security"></a><span data-ttu-id="d3c0a-105">Wie beschränke ich den Zugriff auf einen Bericht mithilfe der Baumstruktursicherheit?</span><span class="sxs-lookup"><span data-stu-id="d3c0a-105">How do I restrict access to a report using tree security?</span></span>

<span data-ttu-id="d3c0a-106">Das folgende Beispiel zeigt, wie der Zugriff auf einen Bericht mithilfe der Baumstruktursicherheit eingeschränkt werden kann.</span><span class="sxs-lookup"><span data-stu-id="d3c0a-106">The following example shows how to restrict access to a report using tree security.</span></span>

<span data-ttu-id="d3c0a-107">Auf den Bilanzbericht des USMF-Demounternehmens sollen nicht alle Benutzer der Finanzberichterstellung zugreifen dürfen.</span><span class="sxs-lookup"><span data-stu-id="d3c0a-107">The USMF demo company has a Balance sheet report that not all Financial reporting users should have access to.</span></span> <span data-ttu-id="d3c0a-108">Mithilfe der Baumstruktursicherheit können Sie den Zugriff auf einzelne Berichte so einschränken, damit nur bestimmte Benutzer die Berichte aufrufen können.</span><span class="sxs-lookup"><span data-stu-id="d3c0a-108">To restrict access, you can use tree security to restrict access to a single report so that only certain users can access the report.</span></span> <span data-ttu-id="d3c0a-109">So schränken Sie den Zugriff ein:</span><span class="sxs-lookup"><span data-stu-id="d3c0a-109">Follow these steps to restrict access:</span></span> 

1. <span data-ttu-id="d3c0a-110">Melden Sie sich in Financial Reporter Report Designer an.</span><span class="sxs-lookup"><span data-stu-id="d3c0a-110">Sign in to Financial Reporter Report Designer.</span></span>
2. <span data-ttu-id="d3c0a-111">Erstellen Sie eine neue Baumdefinition.</span><span class="sxs-lookup"><span data-stu-id="d3c0a-111">Create a new tree definition.</span></span> <span data-ttu-id="d3c0a-112">Wählen Sie **Datei > Neu > Baumdefinition** aus.</span><span class="sxs-lookup"><span data-stu-id="d3c0a-112">Go to **File > New > Tree Definition**.</span></span>
3. <span data-ttu-id="d3c0a-113">Doppelklicken Sie in der Spalte **Einheitssicherheit** auf **Zusammenfassung**.</span><span class="sxs-lookup"><span data-stu-id="d3c0a-113">Double-click the **Summary** line in the **Unit Security** column.</span></span>
4. <span data-ttu-id="d3c0a-114">Klicken Sie auf **Benutzer und Gruppen**.</span><span class="sxs-lookup"><span data-stu-id="d3c0a-114">Select **Users and Groups**.</span></span>  
5. <span data-ttu-id="d3c0a-115">Wählen Sie die Benutzer oder Gruppen aus, die auf diesen Bericht zugreifen dürfen.</span><span class="sxs-lookup"><span data-stu-id="d3c0a-115">Select the users or groups that need access to this report.</span></span> 
6. <span data-ttu-id="d3c0a-116">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="d3c0a-116">Select **Save**.</span></span>
7. <span data-ttu-id="d3c0a-117">Ergänzen Sie die neue Baumdefinition in der Berichtsdefinition.</span><span class="sxs-lookup"><span data-stu-id="d3c0a-117">In the report definition, add your new tree definition.</span></span>
8. <span data-ttu-id="d3c0a-118">Wählen Sie in der Baumdefinition **Einstellung** aus.</span><span class="sxs-lookup"><span data-stu-id="d3c0a-118">In the tree definition, select **Setting**.</span></span> <span data-ttu-id="d3c0a-119">Wählen Sie unter **Auswahl der Berichtseinheit** die Option **Alle Einheiten einschließen** aus.</span><span class="sxs-lookup"><span data-stu-id="d3c0a-119">Under **Reporting unit selection**, select **Include all units**.</span></span>

## <a name="how-do-i-identify-which-accounts-do-not-match-my-balances"></a><span data-ttu-id="d3c0a-120">Wie finde ich heraus, welche Konten nicht mit meinen Salden übereinstimmen?</span><span class="sxs-lookup"><span data-stu-id="d3c0a-120">How do I identify which accounts do not match my balances?</span></span>

<span data-ttu-id="d3c0a-121">Bei einem Bericht, in dem die Salden nicht übereinstimmen, können Sie die einzelnen Konten und Abweichungen in folgenden Schritten ermitteln.</span><span class="sxs-lookup"><span data-stu-id="d3c0a-121">If you have a report that doesn't have matching balances, here are some steps you can take to identify each of the accounts and variances.</span></span> 

<span data-ttu-id="d3c0a-122">**Financial Reporter Report Designer**</span><span class="sxs-lookup"><span data-stu-id="d3c0a-122">**Financial Reporter Report Designer**</span></span>
1. <span data-ttu-id="d3c0a-123">Erstellen Sie in Financial Reporter Report Designer eine neue Zeilendefinition.</span><span class="sxs-lookup"><span data-stu-id="d3c0a-123">In Financial Reporter Report Designer, create a new row definition.</span></span> 
2. <span data-ttu-id="d3c0a-124">Wählen Sie **Bearbeiten > Zeilen aus Dimensionen einfügen** aus.</span><span class="sxs-lookup"><span data-stu-id="d3c0a-124">Select **Edit > Insert Rows from Dimensions**.</span></span>
3. <span data-ttu-id="d3c0a-125">Wählen Sie **Hauptkonto** aus.</span><span class="sxs-lookup"><span data-stu-id="d3c0a-125">Select **MainAccount**.</span></span>  
4. <span data-ttu-id="d3c0a-126">Wählen Sie **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="d3c0a-126">Select **OK**.</span></span>
5. <span data-ttu-id="d3c0a-127">Speichern Sie die Zeilendefinition.</span><span class="sxs-lookup"><span data-stu-id="d3c0a-127">Save the row definition.</span></span>
6. <span data-ttu-id="d3c0a-128">Neue Spaltendefinition erstellen</span><span class="sxs-lookup"><span data-stu-id="d3c0a-128">Create a new column definition</span></span>
7. <span data-ttu-id="d3c0a-129">Erstellen Sie eine neue Berichtsdefinition.</span><span class="sxs-lookup"><span data-stu-id="d3c0a-129">Create a new report definition.</span></span>
8. <span data-ttu-id="d3c0a-130">Wählen Sie **Einstellungen** aus, und deaktivieren Sie diese Option.</span><span class="sxs-lookup"><span data-stu-id="d3c0a-130">Select **Settings** and unmark this option.</span></span>  
9. <span data-ttu-id="d3c0a-131">Erstellen Sie den Bericht.</span><span class="sxs-lookup"><span data-stu-id="d3c0a-131">Generate the report.</span></span> 
10. <span data-ttu-id="d3c0a-132">Exportieren Sie den Bericht in Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="d3c0a-132">Export the report to Microsoft Excel.</span></span>

<span data-ttu-id="d3c0a-133">**Dynamics 365 Finance**</span><span class="sxs-lookup"><span data-stu-id="d3c0a-133">**Dynamics 365 Finance**</span></span> 
1. <span data-ttu-id="d3c0a-134">Wählen Sie in Dynamics 365 Finance die Optionen **Hauptbuch > Anfragen und Berichte > Zwischenbilanz** aus.</span><span class="sxs-lookup"><span data-stu-id="d3c0a-134">In Dynamics 365 Finance, go to **General Ledger > Inquiries and Reports > Trial Balance**.</span></span>
2. <span data-ttu-id="d3c0a-135">Legen Sie die folgenden Parameter fest:</span><span class="sxs-lookup"><span data-stu-id="d3c0a-135">Set the following parameters:</span></span>
   - <span data-ttu-id="d3c0a-136">**Ab Datum**: Geben Sie den Beginn des Geschäftsjahres ein.</span><span class="sxs-lookup"><span data-stu-id="d3c0a-136">**From Date** - Enter the start of the fiscal year.</span></span>
   - <span data-ttu-id="d3c0a-137">**Bis Datum**: Geben Sie das Datum ein, zu dem der Bericht erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="d3c0a-137">**To Date** - Enter the date you are generating the report for.</span></span>
   - <span data-ttu-id="d3c0a-138">**Finanzdimension**: Setzen Sie dieses Feld auf **Hauptkonto festgelegt**.</span><span class="sxs-lookup"><span data-stu-id="d3c0a-138">**Financial Dimension** - Set this field to **Main Account set**.</span></span>
 3. <span data-ttu-id="d3c0a-139">Wählen Sie **Berechnen** aus.</span><span class="sxs-lookup"><span data-stu-id="d3c0a-139">Select **Calculate**.</span></span>
 4. <span data-ttu-id="d3c0a-140">Exportieren Sie den Bericht in Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="d3c0a-140">Export the report to Microsoft Excel.</span></span>

<span data-ttu-id="d3c0a-141">Nun sollten sich die Daten aus dem Excel-Bericht in der Finanzberichterstellung in den Bericht zur Zwischenbilanz kopieren lassen, damit Sie die Spalten zur **Abschlussbilanz** vergleichen können.</span><span class="sxs-lookup"><span data-stu-id="d3c0a-141">You should now be able to copy the data from the Financial Reporter Excel report to the Trial Balance report, so you can compare the **Closing Balance** columns.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]