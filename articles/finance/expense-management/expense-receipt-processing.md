---
title: Ausgabenbelegverarbeitung
description: Dieses Thema enthält Informationen zur optischen Zeichenerkennung (OCR) für Belege. Diese Funktion wurde entwickelt, um die Benutzerfreundlichkeit bei der Erstellung von Spesenabrechnungen in Microsoft Dynamics 365 Finance zu verbessern.
author: stevensporen
manager: AnnBe
ms.date: 11/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 1ead9039de63e2cf4f3a7faddd1702b9614d7f99
ms.sourcegitcommit: 6aceca43c53c4dde46954c0b6b855d488eb44ed2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2020
ms.locfileid: "3027902"
---
# <a name="public-preview-expense-receipt-processing"></a><span data-ttu-id="48341-104">Öffentliche Vorschau: Verarbeitung von Ausgabenbelegen</span><span class="sxs-lookup"><span data-stu-id="48341-104">Public Preview: Expense receipt processing</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


<span data-ttu-id="48341-105">Die Ausgabenerfassung wurde durch die Einführung der OCR-Verarbeitung für Belege erweitert.</span><span class="sxs-lookup"><span data-stu-id="48341-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="48341-106">Diese Funktion wurde entwickelt, um die Benutzerfreundlichkeit bei der Erstellung von Spesenabrechnungen zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="48341-106">This feature is designed to improve the user experience when expense reports are created.</span></span>

## <a name="key-features"></a><span data-ttu-id="48341-107">Schlüsselfeatures</span><span class="sxs-lookup"><span data-stu-id="48341-107">Key features</span></span>

- <span data-ttu-id="48341-108">Der Händlername, das Datum und der Gesamtbetrag werden aus den Belegen extrahiert.</span><span class="sxs-lookup"><span data-stu-id="48341-108">The merchant name, date, and total amount are extracted from receipts.</span></span>
- <span data-ttu-id="48341-109">Die Funktion versucht, nicht angehängte Belege mit nicht angehängten Ausgabenbuchungen abzugleichen.</span><span class="sxs-lookup"><span data-stu-id="48341-109">The feature tries to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="48341-110">Benutzer können manuell eingegebene Ausgabenbuchungen aus Belegen erstellen.</span><span class="sxs-lookup"><span data-stu-id="48341-110">Users can create manually entered expense transactions from receipts.</span></span>

## <a name="usage-examples"></a><span data-ttu-id="48341-111">Anwendungsbeispiele</span><span class="sxs-lookup"><span data-stu-id="48341-111">Usage examples</span></span>

- <span data-ttu-id="48341-112">**Belege mit Kreditkartenbuchungen automatisch anhängen, wenn ein Spesenbericht erstellt wird.**</span><span class="sxs-lookup"><span data-stu-id="48341-112">**Automatically attach receipts that include credit card transactions when an expense report is created.**</span></span>

    1. <span data-ttu-id="48341-113">Öffnen Sie den Arbeitsbereich **Ausgabenverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="48341-113">Open the **Expense management** workspace.</span></span>
    2. <span data-ttu-id="48341-114">Überprüfen Sie auf der Registerkarte für **Belege**, ob nicht angehängte Belege vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="48341-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="48341-115">Sie können Belege auch auf die Registerkarte **Belege** hochladen.</span><span class="sxs-lookup"><span data-stu-id="48341-115">You can also upload receipts on the **Receipts** tab.</span></span>
    3. <span data-ttu-id="48341-116">Überprüfen Sie auf der Registerkarte **Ausgaben**, ob nicht angehängte Ausgaben vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="48341-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="48341-117">In der Regel importiert der Ausgabenadministrator diese Ausgaben vom Kreditkartenanbieter.</span><span class="sxs-lookup"><span data-stu-id="48341-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
    4. <span data-ttu-id="48341-118">Wählen Sie **Neue Spesenabrechnung**.</span><span class="sxs-lookup"><span data-stu-id="48341-118">Select **New expense report**.</span></span> <span data-ttu-id="48341-119">Beachten Sie, dass Sie beim Erstellen einer Spesenabrechnung jetzt auch Ausgaben und Belege einschließen können.</span><span class="sxs-lookup"><span data-stu-id="48341-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="48341-120">Wenn Sie sowohl Ausgaben als auch Belege hinzufügen, wird ein automatischer Abgleich der Belege mit den Ausgaben durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="48341-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

- <span data-ttu-id="48341-121">**Erstellen einer Ausgabe oder Abgleichen einer Ausgabe aus einem Beleg.**</span><span class="sxs-lookup"><span data-stu-id="48341-121">**Create an expense, or match an expense from a receipt.**</span></span>

    1. <span data-ttu-id="48341-122">Fügen Sie bei einer Spesenabrechnung auf der Registerkarte **Belege** einen Beleg hinzu, indem Sie **Belege hinzufügen** auswählen.</span><span class="sxs-lookup"><span data-stu-id="48341-122">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
    2. <span data-ttu-id="48341-123">Beachten Sie unter dem hochgeladenen Bild des Belegs die Optionen **Erstellen** und **Abgleichen**.</span><span class="sxs-lookup"><span data-stu-id="48341-123">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

        - <span data-ttu-id="48341-124">Wählen Sie **Erstellen** aus, um eine manuell eingegebene Ausgabenbuchung zu erstellen, und geben Sie die aus dem Beleg extrahierten Werte ein.</span><span class="sxs-lookup"><span data-stu-id="48341-124">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
        - <span data-ttu-id="48341-125">Wenn Sie **Abgleichen** auswählen, versucht das System, dem Beleg eine vorhandene Ausgabe zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="48341-125">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="48341-126">Installation</span><span class="sxs-lookup"><span data-stu-id="48341-126">Installation</span></span>

<span data-ttu-id="48341-127">Diese Funktion funktioniert in Kombination mit der Funktion **Spesenabrechnungen neu gestaltet**, um die Erfahrung mit der Ausgabenverarbeitung zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="48341-127">This feature works in combination with the **Expense reports re-imagined** feature to help simplify the expense experience.</span></span>

<span data-ttu-id="48341-128">Wenn Sie diese erweiterten Ausgabenfunktionen nutzen möchten, installieren Sie das Add-In für den Spesenverwaltungsdienst für Microsoft Dynamics 365 Finance und aktivieren Sie die Funktionen in Ihrer Instance.</span><span class="sxs-lookup"><span data-stu-id="48341-128">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="48341-129">Sie können auf das Add-In über Ihr Projekt in Microsoft Dynamics Lifecycle Services (LCS) zugreifen.</span><span class="sxs-lookup"><span data-stu-id="48341-129">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="48341-130">Melden Sie sich bei LCS an und öffnen Sie die gewünschte Umgebung.</span><span class="sxs-lookup"><span data-stu-id="48341-130">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="48341-131">Gehen Sie zu **Vollständige Details**.</span><span class="sxs-lookup"><span data-stu-id="48341-131">Go to **Full details**.</span></span>
3. <span data-ttu-id="48341-132">Wählen Sie **Beibehalten**, oder scrollen Sie nach unten zu den **Umgebungs-Add-Ins** Inforegister.</span><span class="sxs-lookup"><span data-stu-id="48341-132">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="48341-133">Wählen Sie **Installieren Sie ein neues Add-In**.</span><span class="sxs-lookup"><span data-stu-id="48341-133">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="48341-134">Wählen Sie **Spesenverwaltungsdienst** aus.</span><span class="sxs-lookup"><span data-stu-id="48341-134">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="48341-135">Befolgen Sie die Installationsanleitung und erklären Sie sich mit den Allgemeinen Geschäftsbedingungen einverstanden.</span><span class="sxs-lookup"><span data-stu-id="48341-135">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="48341-136">Wählen Sie **Installieren**.</span><span class="sxs-lookup"><span data-stu-id="48341-136">Select **Install**.</span></span>

<span data-ttu-id="48341-137">Aktivieren Sie im Arbeitsbereich **Funktionsverwaltung** die folgenden Funktionen:</span><span class="sxs-lookup"><span data-stu-id="48341-137">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="48341-138">Spesenabrechnungen neu gestaltet</span><span class="sxs-lookup"><span data-stu-id="48341-138">Expense reports re-imagined</span></span>
- <span data-ttu-id="48341-139">Automatisch abgleichen und Ausgaben aus Beleg erstellen</span><span class="sxs-lookup"><span data-stu-id="48341-139">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="48341-140">Wenn Sie diese Funktionen aktivieren, werden die folgenden Aktivitäten ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="48341-140">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="48341-141">Der vorhandene Arbeitsbereich **Ausgabenverwaltung** wird durch den neuen ersetzt.</span><span class="sxs-lookup"><span data-stu-id="48341-141">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="48341-142">Ein neues Menüelement für Ausgabenenfeldsichtbarkeit wird hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="48341-142">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="48341-143">Sie können weiterhin die vorherige Seite **Spesenabrechnungen** aufrufen, indem Sie zu **Ausgabenverwaltung > Meine Ausgaben > Spesenabrechnungen** navigieren.</span><span class="sxs-lookup"><span data-stu-id="48341-143">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="48341-144">Abläufe und alle Genehmigungen führen Sie weiterhin zur bestehenden Ausgabenberichtsseite.</span><span class="sxs-lookup"><span data-stu-id="48341-144">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="48341-145">Belege werden durch die Microsoft Azure Cognitive Services verarbeitet und Metadaten werden extrahiert und hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="48341-145">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="48341-146">Es wird eine Option hinzugefügt, mit der Sie eine Spesenabrechnung erstellen können, die übereinstimmende nicht angehängte Belege enthält.</span><span class="sxs-lookup"><span data-stu-id="48341-146">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="48341-147">Mit einer Option, die zu den Spesenabrechnungen hinzugefügt wurde, können Sie eine Ausgabenzeile aus einem Beleg erstellen oder einen vorhandenen Beleg mit einer vorhandenen Ausgabenzeile abgleichen.</span><span class="sxs-lookup"><span data-stu-id="48341-147">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

<span data-ttu-id="48341-148">Weitere Informationen zur Funktion „Spesenabrechnungen neu gestaltet“ finden Sie unter [Spesenabrechnungen neu gestaltet](ExpenseWorkspaceNew.md).</span><span class="sxs-lookup"><span data-stu-id="48341-148">For more information about the Expense reports re-imagined feature, see [Expense reports reimagined](ExpenseWorkspaceNew.md).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="48341-149">Häufig gestellte Fragen</span><span class="sxs-lookup"><span data-stu-id="48341-149">Frequently asked questions</span></span>

<span data-ttu-id="48341-150">**Verwendet Microsoft meine Daten für seine Modelle?**</span><span class="sxs-lookup"><span data-stu-id="48341-150">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="48341-151">Nein, Microsoft hat ein allgemeines Machine Learning-Modell für seinen Dienst zur Belegverarbeitung.</span><span class="sxs-lookup"><span data-stu-id="48341-151">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="48341-152">Dieses Modell basiert nicht auf den von Ihnen hochgeladenen Belegen.</span><span class="sxs-lookup"><span data-stu-id="48341-152">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="48341-153">**Wo ist diese Funktion verfügbar und wo wird sie verarbeitet?**</span><span class="sxs-lookup"><span data-stu-id="48341-153">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="48341-154">Derzeit wird diese für die USA unterstützt.</span><span class="sxs-lookup"><span data-stu-id="48341-154">Currently, the United States is supported.</span></span>

<span data-ttu-id="48341-155">**Wohin gehen meine Belege?**</span><span class="sxs-lookup"><span data-stu-id="48341-155">**Where do my receipts go?**</span></span>

<span data-ttu-id="48341-156">Finance wird sich mit Cognitive Services in Verbindung setzen, um die Felddaten zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="48341-156">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="48341-157">Cognitive Services bewahrt eine Kopie Ihres Belegs bis zu 24 Stunden lang auf, während die Verarbeitung erfolgt.</span><span class="sxs-lookup"><span data-stu-id="48341-157">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="48341-158">Nach Abschluss der Verarbeitung entfernt Cognitive Services den Beleg.</span><span class="sxs-lookup"><span data-stu-id="48341-158">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="48341-159">Belege werden weiterhin in Finance gespeichert.</span><span class="sxs-lookup"><span data-stu-id="48341-159">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="48341-160">Weitere Informationen finden Sie unter [Ermöglichen des Verstehens von Belegen mit der neuen Funktion der Formularerkennung das Verstehen von Belegen](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="48341-160">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>
