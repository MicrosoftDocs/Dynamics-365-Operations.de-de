---
title: Häufig gestellte Fragen zur Finanzberichterstellung
description: Dieser Artikel gibt Antwort auf einige häufig gestellte Fragen zur Finanzberichterstellung.
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
ms.openlocfilehash: e1b67f86446403933005008a9a1e2cc6739dc516
ms.sourcegitcommit: ecabf43282a3e55f1db40341aa3f3c7950b9e94c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/16/2021
ms.locfileid: "6266632"
---
# <a name="financial-reporting-faq"></a><span data-ttu-id="0611d-103">Häufig gestellte Fragen zur Finanzberichterstellung</span><span class="sxs-lookup"><span data-stu-id="0611d-103">Financial reporting FAQ</span></span>

<span data-ttu-id="0611d-104">Dieser Artikel gibt Antwort auf häufig gestellte Fragen zur Finanzberichterstellung.</span><span class="sxs-lookup"><span data-stu-id="0611d-104">This topic provides answers to frequently asked questions about Financial reporting.</span></span>

## <a name="how-do-i-restrict-access-to-a-report-by-using-tree-security"></a><span data-ttu-id="0611d-105">Wie beschränke ich den Zugriff auf einen Bericht mithilfe der Baumstruktursicherheit?</span><span class="sxs-lookup"><span data-stu-id="0611d-105">How do I restrict access to a report by using tree security?</span></span>

<span data-ttu-id="0611d-106">Das folgende Beispiel zeigt, wie der Zugriff auf einen Bericht mithilfe der Baumstruktursicherheit eingeschränkt werden kann.</span><span class="sxs-lookup"><span data-stu-id="0611d-106">The following example shows how to restrict access to a report by using tree security.</span></span>

<span data-ttu-id="0611d-107">Auf den **Bilanzbericht** des USMF-Demounternehmens sollen nicht alle Benutzer der Finanzberichterstellung zugreifen dürfen.</span><span class="sxs-lookup"><span data-stu-id="0611d-107">The USMF demo company has a **Balance sheet** report that not all Financial reporting users should have access to.</span></span> <span data-ttu-id="0611d-108">Mithilfe der Baumstruktursicherheit können Sie den Zugriff auf einzelne Berichte so einschränken, damit nur bestimmte Benutzer Zugriff erhalten.</span><span class="sxs-lookup"><span data-stu-id="0611d-108">You can use tree security to restrict access to a single report so that only specific users can access it.</span></span>

1. <span data-ttu-id="0611d-109">Melden Sie sich bei Financial Reporter Report Designer an.</span><span class="sxs-lookup"><span data-stu-id="0611d-109">Sign in to Financial Reporter Report Designer.</span></span>
2. <span data-ttu-id="0611d-110">Wählen Sie **Datei \> Neu \> Baumdefinition** aus, um eine neue Baumdefinition zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0611d-110">Select **File \> New \> Tree Definition** to create a new tree definition.</span></span>
3. <span data-ttu-id="0611d-111">Doppeltippen oder -klicken Sie in der Spalte **Einheitssicherheit** auf **Zusammenfassung**.</span><span class="sxs-lookup"><span data-stu-id="0611d-111">Double-tap (or double-click) the **Summary** line in the **Unit Security** column.</span></span>
4. <span data-ttu-id="0611d-112">Wählen Sie **Benutzer und Gruppen** aus.</span><span class="sxs-lookup"><span data-stu-id="0611d-112">Select **Users and Groups**.</span></span>
5. <span data-ttu-id="0611d-113">Wählen Sie die Benutzer oder Gruppen aus, die auf diesen Bericht zugreifen müssen.</span><span class="sxs-lookup"><span data-stu-id="0611d-113">Select the users or groups that require access to the report.</span></span>
6. <span data-ttu-id="0611d-114">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="0611d-114">Select **Save**.</span></span>
7. <span data-ttu-id="0611d-115">Ergänzen Sie die neue Baumdefinition in der Berichtsdefinition.</span><span class="sxs-lookup"><span data-stu-id="0611d-115">In the report definition, add your new tree definition.</span></span>
8. <span data-ttu-id="0611d-116">Wählen Sie in der Baumdefinition **Einstellung** aus.</span><span class="sxs-lookup"><span data-stu-id="0611d-116">In the tree definition, select **Setting**.</span></span> <span data-ttu-id="0611d-117">Wählen Sie dann unter **Auswahl der Berichtseinheit** die Option **Alle Einheiten einschließen** aus.</span><span class="sxs-lookup"><span data-stu-id="0611d-117">Then, under **Reporting unit selection**, select **Include all units**.</span></span>

## <a name="how-do-i-identify-which-accounts-dont-match-my-balances"></a><span data-ttu-id="0611d-118">Wie finde ich heraus, welche Konten nicht mit meinen Salden übereinstimmen?</span><span class="sxs-lookup"><span data-stu-id="0611d-118">How do I identify which accounts don't match my balances?</span></span>

<span data-ttu-id="0611d-119">Bei einem Bericht, in dem die Salden nicht übereinstimmen, verwenden Sie die folgenden Verfahren, um die einzelnen Konten und Abweichungen zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="0611d-119">If you have a report that doesn't have matching balances, use the following procedures to identify each account and variance.</span></span>

### <a name="in-financial-reporter-report-designer"></a><span data-ttu-id="0611d-120">In Financial Reporter Report Designer</span><span class="sxs-lookup"><span data-stu-id="0611d-120">In Financial Reporter Report Designer</span></span>

1. <span data-ttu-id="0611d-121">Erstellen Sie eine neue Zeilendefinition.</span><span class="sxs-lookup"><span data-stu-id="0611d-121">Create a new row definition.</span></span>
2. <span data-ttu-id="0611d-122">Wählen Sie **Bearbeiten \> Zeilen aus Dimensionen einfügen** aus.</span><span class="sxs-lookup"><span data-stu-id="0611d-122">Select **Edit \> Insert Rows from Dimensions**.</span></span>
3. <span data-ttu-id="0611d-123">Wählen Sie **MainAccount** aus.</span><span class="sxs-lookup"><span data-stu-id="0611d-123">Select **MainAccount**.</span></span>
4. <span data-ttu-id="0611d-124">Wählen Sie **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="0611d-124">Select **OK**.</span></span>
5. <span data-ttu-id="0611d-125">Speichern Sie die Zeilendefinition.</span><span class="sxs-lookup"><span data-stu-id="0611d-125">Save the row definition.</span></span>
6. <span data-ttu-id="0611d-126">Erstellen Sie eine neue Spaltendefinition.</span><span class="sxs-lookup"><span data-stu-id="0611d-126">Create a new column definition.</span></span>
7. <span data-ttu-id="0611d-127">Erstellen Sie eine neue Berichtsdefinition.</span><span class="sxs-lookup"><span data-stu-id="0611d-127">Create a new report definition.</span></span>
8. <span data-ttu-id="0611d-128">Wählen Sie **Einstellungen** aus, und deaktivieren Sie diese Option.</span><span class="sxs-lookup"><span data-stu-id="0611d-128">Select **Settings** and unmark this option.</span></span>
9. <span data-ttu-id="0611d-129">Erstellen Sie den Bericht.</span><span class="sxs-lookup"><span data-stu-id="0611d-129">Generate the report.</span></span> 
10. <span data-ttu-id="0611d-130">Exportieren Sie den Bericht in Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="0611d-130">Export the report to Microsoft Excel.</span></span>

### <a name="in-dynamics-365-finance"></a><span data-ttu-id="0611d-131">In Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="0611d-131">In Dynamics 365 Finance</span></span>

1. <span data-ttu-id="0611d-132">Wechseln Sie zu **Hauptbuch \> Anfragen und Berichte \> Zwischenbilanz** aus.</span><span class="sxs-lookup"><span data-stu-id="0611d-132">Go to **General ledger \> Inquiries and reports \> Trial balance**.</span></span>
2. <span data-ttu-id="0611d-133">Stellen Sie die folgenden Felder ein:</span><span class="sxs-lookup"><span data-stu-id="0611d-133">Set the following fields:</span></span>

    - <span data-ttu-id="0611d-134">**Ab Datum** – Geben Sie das Startdatum des Geschäftsjahres ein.</span><span class="sxs-lookup"><span data-stu-id="0611d-134">**From Date** – Enter the start date of the fiscal year.</span></span>
    - <span data-ttu-id="0611d-135">**Bis Datum** – Geben Sie das Datum ein, zu dem der Bericht erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="0611d-135">**To Date** – Enter the date that you're generating the report for.</span></span>
    - <span data-ttu-id="0611d-136">**Finanzdimension** – Setzen Sie dieses Feld auf **Hauptkonto festgelegt**.</span><span class="sxs-lookup"><span data-stu-id="0611d-136">**Financial Dimension** – Set this field to **Main Account set**.</span></span>

3. <span data-ttu-id="0611d-137">Wählen Sie **Berechnen** aus.</span><span class="sxs-lookup"><span data-stu-id="0611d-137">Select **Calculate**.</span></span>
4. <span data-ttu-id="0611d-138">Exportieren Sie den Bericht in Excel.</span><span class="sxs-lookup"><span data-stu-id="0611d-138">Export the report to Excel.</span></span>

<span data-ttu-id="0611d-139">Nun sollten sich die Daten aus dem Excel-Bericht in Financial Reporter in den Bericht zur **Zwischenbilanz** kopieren lassen, damit Sie die Spalten zur **Abschlussbilanz** vergleichen können.</span><span class="sxs-lookup"><span data-stu-id="0611d-139">You should now be able to copy the data from the Financial Reporter Excel report to the **Trial Balance** report, so that you can compare the **Closing Balance** columns.</span></span>

## <a name="when-i-design-a-report-in-report-designer-or-when-i-generate-a-financial-report-i-received-the-following-message-the-operation-could-not-be-completed-due-to-a-problem-in-the-data-provider-framework-how-should-i-respond"></a><span data-ttu-id="0611d-140">Beim Entwerfen eines Berichts im Report Designer oder beim Generieren eines Finanzberichts erhalten ich die folgende Meldung: „Der Vorgang konnte aufgrund eines Problems im Datenanbieter-Framework nicht abgeschlossen werden.“</span><span class="sxs-lookup"><span data-stu-id="0611d-140">When I design a report in Report Designer, or when I generate a financial report, I received the following message: "The operation could not be completed due to a problem in the data provider framework."</span></span> <span data-ttu-id="0611d-141">Wie soll ich reagieren?</span><span class="sxs-lookup"><span data-stu-id="0611d-141">How should I respond?</span></span>

<span data-ttu-id="0611d-142">Die Nachricht weist darauf hin, dass ein Fehler aufgetreten ist, als das System versucht hat, Finanzmetadaten aus dem Data Mart abzurufen, während Sie die Finanzberichterstellung verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="0611d-142">The message indicates that an issue occurred when the system tried to retrieve financial metadata from the data mart while you were using Financial reporting.</span></span> <span data-ttu-id="0611d-143">Es gibt zwei Möglichkeiten, auf dieses Problem zu reagieren:</span><span class="sxs-lookup"><span data-stu-id="0611d-143">There are two ways to respond to this issue:</span></span>

- <span data-ttu-id="0611d-144">Überprüfen Sie den Integrationsstatus der Daten, indem Sie in Report Designer zu **Extras \> Integrationsstatus** wechseln.</span><span class="sxs-lookup"><span data-stu-id="0611d-144">Review the integration status of the data by going to **Tools \> Integration status** in Report Designer.</span></span> <span data-ttu-id="0611d-145">Wenn die Integration unvollständig ist, warten Sie, bis sie abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="0611d-145">If the integration is incomplete, wait for it to be completed.</span></span> <span data-ttu-id="0611d-146">Wiederholen Sie dann den Vorgang, bei dem Sie die Nachricht erhalten haben.</span><span class="sxs-lookup"><span data-stu-id="0611d-146">Then retry what you were doing when you received the message.</span></span>
- <span data-ttu-id="0611d-147">Wenden Sie sich an den Support, um das Problem zu identifizieren und zu beheben.</span><span class="sxs-lookup"><span data-stu-id="0611d-147">Contact Support to identify and work through the issue.</span></span> <span data-ttu-id="0611d-148">Möglicherweise sind inkonsistente Daten im System vorhanden.</span><span class="sxs-lookup"><span data-stu-id="0611d-148">There might be inconsistent data in the system.</span></span> <span data-ttu-id="0611d-149">Supporttechniker können Ihnen helfen, dieses Problem auf dem Server zu identifizieren und die spezifischen Daten zu finden, die möglicherweise aktualisiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="0611d-149">Support engineers can help you identify that issue on the server and find the specific data that might require an update.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
