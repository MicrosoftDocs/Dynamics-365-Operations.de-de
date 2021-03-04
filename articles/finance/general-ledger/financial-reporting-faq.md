---
title: Häufig gestellte Fragen zur Finanzberichterstellung
description: In diesem Artikel werden Fragen anderer Benutzer zur Finanzberichterstellung beantwortet.
author: jiwo
manager: tfehr
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 3f9381f5b656d0cc0b46c8828b2ef9d024e296b0
ms.sourcegitcommit: 14785208d84b2c1efd30f140c52df35a2ccd1577
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/27/2021
ms.locfileid: "5070216"
---
# <a name="financial-reporting-faq"></a><span data-ttu-id="c3b00-103">Häufig gestellte Fragen zur Finanzberichterstellung</span><span class="sxs-lookup"><span data-stu-id="c3b00-103">Financial reporting FAQ</span></span> 

<span data-ttu-id="c3b00-104">In diesem Artikel werden Fragen anderer Benutzer zur Finanzberichterstellung beantwortet.</span><span class="sxs-lookup"><span data-stu-id="c3b00-104">This topic lists questions related to financial reporting that other users have had.</span></span> 


## <a name="how-do-i-restrict-access-to-a-report-using-tree-security"></a><span data-ttu-id="c3b00-105">Wie beschränke ich den Zugriff auf einen Bericht mithilfe der Baumstruktursicherheit?</span><span class="sxs-lookup"><span data-stu-id="c3b00-105">How do I restrict access to a report using Tree security?</span></span>

<span data-ttu-id="c3b00-106">Szenario: Das Demounternehmen USMF hat eine Bilanz erstellt, die nicht alle Benutzer der Finanzberichterstellung in Dynamics 365 einsehen sollen.</span><span class="sxs-lookup"><span data-stu-id="c3b00-106">Scenario: The USMF demo company has a Balance sheet report that it doesn’t want all Financial reporting users to be able to view in D365.</span></span> <span data-ttu-id="c3b00-107">Lösung: Mithilfe der Baumstruktursicherheit können Sie den Zugriff auf einzelne Berichte so einschränken, damit nur bestimmte Benutzer die Berichte aufrufen können.</span><span class="sxs-lookup"><span data-stu-id="c3b00-107">Solution: You can utilize Tree security to restrict access to a single report so that only certain users can access the report.</span></span> 

1.  <span data-ttu-id="c3b00-108">Im Berichts-Designer der Finanzberichterstellung anmelden</span><span class="sxs-lookup"><span data-stu-id="c3b00-108">Log into Financial Reporter Report Designer</span></span>

2.  <span data-ttu-id="c3b00-109">Neue Baumdefinition erstellen (Datei | Neu | Baumdefinition) a.</span><span class="sxs-lookup"><span data-stu-id="c3b00-109">Create a new Tree Definition (File | New | Tree Definition) a.</span></span>    <span data-ttu-id="c3b00-110">Doppelklicken Sie in der Spalte **Einheitssicherheit** auf **Zusammenfassung**.</span><span class="sxs-lookup"><span data-stu-id="c3b00-110">Double-click the **Summary** line in the **Unit Security** column.</span></span>
  <span data-ttu-id="c3b00-111">i.</span><span class="sxs-lookup"><span data-stu-id="c3b00-111">i.</span></span>    <span data-ttu-id="c3b00-112">Klicken Sie auf „Benutzer und Gruppen“.</span><span class="sxs-lookup"><span data-stu-id="c3b00-112">Click Users and Groups.</span></span>  
          <span data-ttu-id="c3b00-113">1. Wählen Sie den/die Benutzer oder die Gruppe aus, die auf diesen Bericht zugreifen möchte.</span><span class="sxs-lookup"><span data-stu-id="c3b00-113">1.    Select the User(s) or Group that would like to access this report.</span></span> 
          
<span data-ttu-id="c3b00-114">[![Benutzerbildschirm](./media/FR-FAQ_users.png)](./media/FR-FAQ_users.png)</span><span class="sxs-lookup"><span data-stu-id="c3b00-114">[![user screen](./media/FR-FAQ_users.png)](./media/FR-FAQ_users.png)</span></span>

<span data-ttu-id="c3b00-115">[![Sicherheitsbildschirm](./media/FR-FAQ_security.jpg)](./media/FR-FAQ_security.jpg)</span><span class="sxs-lookup"><span data-stu-id="c3b00-115">[![security screen](./media/FR-FAQ_security.jpg)](./media/FR-FAQ_security.jpg)</span></span>

  <span data-ttu-id="c3b00-116">b.</span><span class="sxs-lookup"><span data-stu-id="c3b00-116">b.</span></span>    <span data-ttu-id="c3b00-117">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="c3b00-117">Click **Save**.</span></span>
  
<span data-ttu-id="c3b00-118">[![Schaltfläche „Speichern“](./media/FR-FAQ_save.png)](./media/FR-FAQ_save.png)</span><span class="sxs-lookup"><span data-stu-id="c3b00-118">[![save button](./media/FR-FAQ_save.png)](./media/FR-FAQ_save.png)</span></span>

3.  <span data-ttu-id="c3b00-119">Neue Baumdefinition in der Berichtsdefinition ergänzen</span><span class="sxs-lookup"><span data-stu-id="c3b00-119">In your Report Definition add your new Tree Definition</span></span>

<span data-ttu-id="c3b00-120">[![Formular „Baumdefinition“](./media/FR-FAQ_tree-definition.jpg)](./media/FR-FAQ_tree-definition.jpg)</span><span class="sxs-lookup"><span data-stu-id="c3b00-120">[![tree definition form](./media/FR-FAQ_tree-definition.jpg)](./media/FR-FAQ_tree-definition.jpg)</span></span>

<span data-ttu-id="c3b00-121">A.</span><span class="sxs-lookup"><span data-stu-id="c3b00-121">A.</span></span>  <span data-ttu-id="c3b00-122">Klicken Sie in der Baumdefinition auf „Einstellung“ und danach unter „Auswahl der Berichtseinheit“ auf „Alle Einheiten einschließen“.</span><span class="sxs-lookup"><span data-stu-id="c3b00-122">While in the Tree Definition click on Setting and under “Reporting unit selection” check “Include all units”</span></span>

<span data-ttu-id="c3b00-123">[![Formular zur Auswahl der Berichtseinheit](./media/FR-FAQ_reporting-unit-selection.jpg)](./media/FR-FAQ_reporting-unit-selection.jpg)</span><span class="sxs-lookup"><span data-stu-id="c3b00-123">[![reporting unit selection form](./media/FR-FAQ_reporting-unit-selection.jpg)](./media/FR-FAQ_reporting-unit-selection.jpg)</span></span>

<span data-ttu-id="c3b00-124">**Vorher:** [![Screenshot „Vorher“](./media/FR-FAQ_before.png)](./media/FR-FAQ_before.png)</span><span class="sxs-lookup"><span data-stu-id="c3b00-124">**Before:** [![before screenshot](./media/FR-FAQ_before.png)](./media/FR-FAQ_before.png)</span></span>

<span data-ttu-id="c3b00-125">**Nachher:** [![Screenshot „Nachher“](./media/FR-FAQ_after.png)](./media/FR-FAQ_after.png)</span><span class="sxs-lookup"><span data-stu-id="c3b00-125">**After:** [![after screenshot](./media/FR-FAQ_after.png)](./media/FR-FAQ_after.png)</span></span>

<span data-ttu-id="c3b00-126">Hinweis: Die obige Meldung wird angezeigt, weil der Benutzer nach Übernahme der Einheitssicherheit keinen Zugriff mehr auf den Bericht hat.</span><span class="sxs-lookup"><span data-stu-id="c3b00-126">Note: Reason for the above message is my user does not have access to that report after applying Unit Security</span></span>



## <a name="how-do-i-determine-which-accounts-do-not-matching-my-balances-in-d365"></a><span data-ttu-id="c3b00-127">Wie finde ich heraus, welche Konten nicht mit meinen Saldo in D365 übereinstimmen?</span><span class="sxs-lookup"><span data-stu-id="c3b00-127">How do I determine which account(s) do not matching my balances in D365?</span></span>

<span data-ttu-id="c3b00-128">Wenn ein Bericht in D365 nicht den Erwartungen entspricht, können Sie Konten und Abweichungen wie folgt ermitteln.</span><span class="sxs-lookup"><span data-stu-id="c3b00-128">When you have a report that doesn't match what you would expect in D365, here are some steps you could take to identify those accounts and the variances.</span></span> 

### <a name="in-financial-reporter-report-designer"></a><span data-ttu-id="c3b00-129">Im Berichts-Designer der Finanzberichterstellung</span><span class="sxs-lookup"><span data-stu-id="c3b00-129">In Financial Reporter Report Designer</span></span>

1.  <span data-ttu-id="c3b00-130">Neue Zeilendefinition erstellen a.</span><span class="sxs-lookup"><span data-stu-id="c3b00-130">Create a new Row Definition a.</span></span>    <span data-ttu-id="c3b00-131">Auf „Bearbeiten“ | „Zeilen aus Dimensionen einfügen“ i.</span><span class="sxs-lookup"><span data-stu-id="c3b00-131">Click Edit | Insert Rows from Dimensions i.</span></span>  <span data-ttu-id="c3b00-132">„MainAccount“ auswählen [![Hauptbildschirm auswählen](./media/FR-FAQ_selectmain_.png)](./media/FR-FAQ_selectmain_.png)</span><span class="sxs-lookup"><span data-stu-id="c3b00-132">Select MainAccount [![Select Main screen_](./media/FR-FAQ_selectmain_.png)](./media/FR-FAQ_selectmain_.png)</span></span>
    
    <span data-ttu-id="c3b00-133">ii.</span><span class="sxs-lookup"><span data-stu-id="c3b00-133">ii.</span></span> <span data-ttu-id="c3b00-134">Auf „OK“ klicken b.</span><span class="sxs-lookup"><span data-stu-id="c3b00-134">Click Ok b.</span></span>    <span data-ttu-id="c3b00-135">Zeilendefinition speichern</span><span class="sxs-lookup"><span data-stu-id="c3b00-135">Save the Row Definition</span></span>

2.  <span data-ttu-id="c3b00-136">Eine neue Spaltendefinition erstellen     [![Eine neue Spaltendefinition erstellen](./media/FR-FAQ_column.png)](./media/FR-FAQ_column.png)</span><span class="sxs-lookup"><span data-stu-id="c3b00-136">Create a new Column Definition     [![Create a new column definition](./media/FR-FAQ_column.png)](./media/FR-FAQ_column.png)</span></span>

3.  <span data-ttu-id="c3b00-137">Eine neue Berichtsdefinition erstellen a.</span><span class="sxs-lookup"><span data-stu-id="c3b00-137">Create a new Report Definition a.</span></span>    <span data-ttu-id="c3b00-138">Auf „Einstellungen“ klicken und das Kontrollkästchen [![Einstellungsformular](./media/FR-FAQ_settings.png)](./media/FR-FAQ_settings.png) deaktivieren</span><span class="sxs-lookup"><span data-stu-id="c3b00-138">Click Settings and uncheck [![Settings form](./media/FR-FAQ_settings.png)](./media/FR-FAQ_settings.png)</span></span>
   
4.  <span data-ttu-id="c3b00-139">Erstellen Sie den Bericht.</span><span class="sxs-lookup"><span data-stu-id="c3b00-139">Generate the Report.</span></span> 

5.  <span data-ttu-id="c3b00-140">Exportieren Sie den Bericht in Excel.</span><span class="sxs-lookup"><span data-stu-id="c3b00-140">Export the Report to Excel.</span></span>

### <a name="in-d365"></a><span data-ttu-id="c3b00-141">In D365:</span><span class="sxs-lookup"><span data-stu-id="c3b00-141">In D365:</span></span> 
1.  <span data-ttu-id="c3b00-142">Auf „Hauptbuch“ | „Anfragen und Berichte“ | „Zwischenbilanz“ klicken a.</span><span class="sxs-lookup"><span data-stu-id="c3b00-142">Click General Ledger | Inquiries and Reports | Trial Balance a.</span></span>    <span data-ttu-id="c3b00-143">Parameter i.</span><span class="sxs-lookup"><span data-stu-id="c3b00-143">Parameters i.</span></span>  <span data-ttu-id="c3b00-144">Ab Datum: Beginn des Geschäftsjahres ii.</span><span class="sxs-lookup"><span data-stu-id="c3b00-144">From Date: Start of Fiscal Year ii.</span></span> <span data-ttu-id="c3b00-145">Bis Datum: Datum, zu dem der Bericht erstellt wurde iii.</span><span class="sxs-lookup"><span data-stu-id="c3b00-145">To Date: Date you generated the report for iii.</span></span>    <span data-ttu-id="c3b00-146">Finanzdimensionssatz, „Hauptkonto“ festgelegt [![Hauptkontoformular](./media/FR-FAQ_mainacct.png)](./media/FR-FAQ_mainacct.png)</span><span class="sxs-lookup"><span data-stu-id="c3b00-146">Financial Dimension Set “Main Account set” [![Main Account Form](./media/FR-FAQ_mainacct.png)](./media/FR-FAQ_mainacct.png)</span></span>
      
  <span data-ttu-id="c3b00-147">b.</span><span class="sxs-lookup"><span data-stu-id="c3b00-147">b.</span></span>    <span data-ttu-id="c3b00-148">Auf „Berechnen“ klicken</span><span class="sxs-lookup"><span data-stu-id="c3b00-148">Click Calculate</span></span>

2.  <span data-ttu-id="c3b00-149">Bericht in Excel exportieren</span><span class="sxs-lookup"><span data-stu-id="c3b00-149">Export the report to Excel</span></span>

<span data-ttu-id="c3b00-150">Sie sollten nun in der Lage sein, die Daten aus dem Excel-Bericht in der Finanzberichterstellung in den D365-Zwischenbilanzbericht zu kopieren und die Spalten mit der Abschlussbilanz zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="c3b00-150">You should now be able to copy the data from the FR Excel Report and to the D365 Trial Balance report and compare the “Closing Balance” columns.</span></span>
