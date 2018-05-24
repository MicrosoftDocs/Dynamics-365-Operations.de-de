---
title: Feldbeschreibungen anzeigen und exportieren
description: "Dieser Artikel erläutert, wie eine Feldbeschreibung angezeigt und die Seite \"Feldbeschreibungen\" verwendet wird, um eine Beschreibung zu exportieren."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: FieldDescriptions
audience: Application User, Developer, IT Pro
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.custom: 11534
ms.assetid: e2795f51-a8a7-4c74-bdb9-b1be93bdd358
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: d1ee87dbe9dab089a893d9c69d2573a4c4b11b58
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---

# <a name="view-and-export-field-descriptions"></a><span data-ttu-id="d7684-103">Feldbeschreibungen anzeigen und exportieren</span><span class="sxs-lookup"><span data-stu-id="d7684-103">View and export field descriptions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d7684-104">Dieser Artikel erläutert, wie eine Feldbeschreibung angezeigt und die Seite "Feldbeschreibungen" verwendet wird, um eine Beschreibung zu exportieren.</span><span class="sxs-lookup"><span data-stu-id="d7684-104">This article describes how to view field descriptions and how to use the Field descriptions page to export descriptions.</span></span>

<span data-ttu-id="d7684-105">Microsoft Dynamics 365 for Finance and Operations stellt Beschreibungen für einige der komplexeren Felder bereit.</span><span class="sxs-lookup"><span data-stu-id="d7684-105">Microsoft Dynamics 365 for Finance and Operations has descriptions for some of the more complex fields.</span></span> <span data-ttu-id="d7684-106">Diese Beschreibungen werden angezeigt, wenn Sie den Mauszeiger über ein Feld bewegen.</span><span class="sxs-lookup"><span data-stu-id="d7684-106">These descriptions appear when you hover over a field.</span></span> <span data-ttu-id="d7684-107">Sie können Bescheibungen auf der Seite **Feldbeschreibungen** anzeigen und exportieren.</span><span class="sxs-lookup"><span data-stu-id="d7684-107">You can also view and export descriptions on the **Field descriptions** page.</span></span> 

<span data-ttu-id="d7684-108">Nicht alle Seiten haben Feldbeschreibungen.</span><span class="sxs-lookup"><span data-stu-id="d7684-108">Not all pages have field descriptions.</span></span> <span data-ttu-id="d7684-109">Wir möchten Beschreibungen nur für die komplexeren Felder bereitstellen, und nicht für Felder, bei denen die Verwendung offensichtlich ist.</span><span class="sxs-lookup"><span data-stu-id="d7684-109">We want to provide descriptions only for the more complex fields, not where the use of the field is obvious.</span></span> <span data-ttu-id="d7684-110">Daher verfügen einige Seiten über keine Feldbeschreibungen, andere über ein paar und komplexeren Seiten, wie ein Großteil der Parameter-Seiten, verfügen über viele Beschreibungen.</span><span class="sxs-lookup"><span data-stu-id="d7684-110">Therefore, some pages don't have any field descriptions, some pages have a few descriptions, and some of the more complex pages, such as many of the parameters pages, have many descriptions.</span></span> 

<span data-ttu-id="d7684-111">Wenn Sie Zugriff auf die Entwicklungsumgebung von Finance and Operations haben, können Sie neue Feldbeschreibungen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d7684-111">If you have access to the Finance and Operations development environment, you can add new field descriptions and customize existing descriptions.</span></span> <span data-ttu-id="d7684-112">Beispielsweise können Sie einer Feldbeschreibung unternehmensspezifische Informationen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d7684-112">For example, you can add company-specific information to a field description.</span></span> <span data-ttu-id="d7684-113">Weitere Informationen finden Sie unter [Feldhilfe anpassen](../../dev-itpro/user-interface/customize-field-help.md).</span><span class="sxs-lookup"><span data-stu-id="d7684-113">For more information, see [Customize field help](../../dev-itpro/user-interface/customize-field-help.md).</span></span>

## <a name="see-field-descriptions-in-the-user-interface"></a><span data-ttu-id="d7684-114">Siehe hierzu auch die Feldbeschreibungen auf der Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="d7684-114">See field descriptions in the user interface</span></span>
<span data-ttu-id="d7684-115">Sie können Felder anzeigen, indem Sie über ein Feld fahren.</span><span class="sxs-lookup"><span data-stu-id="d7684-115">You can view field descriptions by hovering over a field.</span></span> <span data-ttu-id="d7684-116">Ist keine Beschreibung verfügbar, sehen Sie den Feldnamen beim Bewegen über das Feld.</span><span class="sxs-lookup"><span data-stu-id="d7684-116">If no description is available, you see the field name when you hover over the field.</span></span> <span data-ttu-id="d7684-117">(Hinweis: In Dynamics AX, Version 7.0 (Februar 2016) können Feldbeschreibungen nur auf der Seite **Feldbeschreibungen** angezeigt werden). Die folgende Abbildung zeigt die Feldbeschreibung, die angezeigt wird, wenn Sie mit dem Mauszeiger über das Feld **Artikel während der Inventur sperren** fahren.</span><span class="sxs-lookup"><span data-stu-id="d7684-117">(Note: In Dynamics AX 7.0 (February 2016), field descriptions can be viewed only on the **Field descriptions** page.) The following illustration shows the field description that appears when you hover over the **Lock items during count** field.</span></span> 

<span data-ttu-id="d7684-118">[![Beispiel einer Feldbeschreibung](./media/field-description.png)](./media/field-description.png)</span><span class="sxs-lookup"><span data-stu-id="d7684-118">[![Example of a field description](./media/field-description.png)](./media/field-description.png)</span></span>

## <a name="use-the-field-descriptions-page-to-view-and-export-field-help"></a><span data-ttu-id="d7684-119">Verwenden Sie die Seite "Feldbeschreibung", um Feldhilfe anzuzeigen und zu exportieren.</span><span class="sxs-lookup"><span data-stu-id="d7684-119">Use the Field descriptions page to view and export field help</span></span>
<span data-ttu-id="d7684-120">Die Seite **Feldbeschreibungen** ermöglicht es Ihnen, Feldbeschreibungen anzuzeigen und zu exportieren.</span><span class="sxs-lookup"><span data-stu-id="d7684-120">The **Field descriptions** page lets you view and export field descriptions.</span></span> <span data-ttu-id="d7684-121">Sie können die Beschreibungen finden, die für eine Seite jeweils verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="d7684-121">You can see the descriptions that are available for one page at a time.</span></span>

### <a name="view-the-descriptions-for-a-page"></a><span data-ttu-id="d7684-122">Die Beschreibungen für eine Seite anzeigen</span><span class="sxs-lookup"><span data-stu-id="d7684-122">View the descriptions for a page</span></span>

<span data-ttu-id="d7684-123">Um die Beschreibungen einer Seite anzuzeigen, führen Sie diesen Schritt aus:</span><span class="sxs-lookup"><span data-stu-id="d7684-123">To view the descriptions for a page, follow this step.</span></span>

-   <span data-ttu-id="d7684-124">Geben Sie im Feld **Eine Seite auswählen** den Namen der Seite ein.</span><span class="sxs-lookup"><span data-stu-id="d7684-124">In the **Select a page** field, type the name of the page.</span></span> <span data-ttu-id="d7684-125">Alternativ klicken Sie auf den Pfeil, um eine Liste aller Seiten öffnen und dann die Liste zu durchsuchen oder zu filtern.</span><span class="sxs-lookup"><span data-stu-id="d7684-125">Alternatively, click the arrow to open a list of all the pages, and then browse or filter the list.</span></span>

<span data-ttu-id="d7684-126">Sie können beispielsweise den Namen der Seite verwenden, der in der Benutzeroberfläche (UI)angezeigt wird (z. B. **Debitoren**) oder den Codename (AOT-Name), der verfügbar ist, wenn man mit der rechten Maustaste auf eine Seite klickt (z. B. **CustTable**).</span><span class="sxs-lookup"><span data-stu-id="d7684-126">You can use either the name of the page that is shown in the user interface (UI) (for example, **Customers**) or the code name (AOT name) that's available when you right-click a page (for example, **CustTable**).</span></span> 

<span data-ttu-id="d7684-127">Informationen über die verschiedenen Methoden zum Filtern der Seitenliste finden Sie Abschnitt "Nach einer Seite suchen" weiter unten in diesem Artikel.</span><span class="sxs-lookup"><span data-stu-id="d7684-127">For information about the various ways to filter the list of pages, see the "Searching for a page" section later in this article.</span></span> 

<span data-ttu-id="d7684-128">Wenn Sie die Option **Felder ohne eine Beschreibung einbeziehen** auf **Ja** festlegen, werden alle Felder auf der Seite angezeigt, unabhängig davon, ob sie eine Feldbeschreibung haben.</span><span class="sxs-lookup"><span data-stu-id="d7684-128">If you set the **Include fields without a description** option to **Yes**, all the fields on the page are shown, even if they don't have a field description.</span></span>

### <a name="export-the-descriptions-for-a-page"></a><span data-ttu-id="d7684-129">Die Beschreibungen für eine Seite exportieren</span><span class="sxs-lookup"><span data-stu-id="d7684-129">Export the descriptions for a page</span></span>

<span data-ttu-id="d7684-130">Um die Beschreibungen einer Seite zu exportieren, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="d7684-130">To export the descriptions for a page, follow these steps.</span></span>

1.  <span data-ttu-id="d7684-131">Wählen Sie im Feld **Eine Seite auswählen** eine Seite aus.</span><span class="sxs-lookup"><span data-stu-id="d7684-131">In the **Select a page** field, select a page.</span></span>
2.  <span data-ttu-id="d7684-132">Klicken Sie auf die Schaltfläche **In Microsoft Office öffnen** in der oberen rechten Ecke und dann auf **FieldDescriptionTmp**.</span><span class="sxs-lookup"><span data-stu-id="d7684-132">Click the **Open in Microsoft Office** button in the upper-right corner, and then click **FieldDescriptionTmp**.</span></span>

### <a name="searching-for-a-page"></a><span data-ttu-id="d7684-133">Nach einer Seite suchen</span><span class="sxs-lookup"><span data-stu-id="d7684-133">Searching for a page</span></span>

<span data-ttu-id="d7684-134">Es gibt mehrere Möglichkeiten, im Feld **Eine Seite auswählen** eine Seite zu suchen.</span><span class="sxs-lookup"><span data-stu-id="d7684-134">There are several ways to search for a page in the **Select a page** field.</span></span> <span data-ttu-id="d7684-135">In vielen Fällen müssen Sie auf den Pfeil im Feld **Eine Seite auswählen** klicken, um die Dropdownliste zu öffnen und aus einer gefilterten Liste von Seiten auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="d7684-135">In many cases, you must click the arrow in the **Select a page** field to open the drop-down list, and then select from a filtered list of pages.</span></span>

-   <span data-ttu-id="d7684-136">Geben Sie einen Teil des Namens ein, und öffnen Sie dann die Dropdownliste, um aus einer gefilterten Liste von Seiten auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="d7684-136">Type part of the name, and then open the drop-down list to select from a filtered list of pages.</span></span>
-   <span data-ttu-id="d7684-137">Öffnen Sie die Dropdownliste und klicken Sie entweder auf die Überschrift **Seitenname** oben auf der Liste oder auf die Überschrift **AOT-Name der Seite**.</span><span class="sxs-lookup"><span data-stu-id="d7684-137">Open the drop-down list, and then click either the **Page name** heading at the top of the list or the **Page AOT name** heading.</span></span> <span data-ttu-id="d7684-138">Dadurch wird ein Dialogfeld geöffnet, in dem Sie erweiterte Filteroptionen verwenden können, wie **Seitenname beginnt mit**.</span><span class="sxs-lookup"><span data-stu-id="d7684-138">A dialog box appears, where you can use advanced filtering options, such as **Page name begins with**.</span></span>
-   <span data-ttu-id="d7684-139">Geben Sie den vollständigen Namen der Seite ein.</span><span class="sxs-lookup"><span data-stu-id="d7684-139">Type the full name of the page.</span></span> <span data-ttu-id="d7684-140">Wenn Sie diese Option verwenden, empfiehlt es sich, die Dropdownliste zu öffnen, um zu sehen, was noch in der Liste ist, auch wenn Feldbeschreibungen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d7684-140">When you use this option, it's best to open the drop-down list and see what else is in the list, even if field descriptions are shown.</span></span>
    -   <span data-ttu-id="d7684-141">Wenn es eine einzelne exakte Entsprechung des Namens gibt, werden die Feldbeschreibungen für diese Seite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d7684-141">If there is a single exact match to the name, the field descriptions for that page are shown.</span></span>
    -   <span data-ttu-id="d7684-142">Wenn mehr als eine exakte Übereinstimmung vorliegt, werden keine Beschreibungen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d7684-142">If there is more than one exact match, no descriptions are shown.</span></span> <span data-ttu-id="d7684-143">Öffnen Sie die Dropdownliste, und wählen Sie die gewünschte Seite.</span><span class="sxs-lookup"><span data-stu-id="d7684-143">You must open the drop-down list and select the page that you want.</span></span>
    -   <span data-ttu-id="d7684-144">Wenn der Name, den Sie eingeben, Teil des Namens einer anderen Seite ist, werden die Beschreibung für Ihre Seite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d7684-144">If the name that you typed is part of the name of another page, you see the descriptions for your page.</span></span> <span data-ttu-id="d7684-145">Wenn Sie aber die Liste öffnen, sehen Sie zusätzliche Seiten, die diesen Namen beinhalten.</span><span class="sxs-lookup"><span data-stu-id="d7684-145">However, if you open the drop-down list, you see additional pages that contain that name.</span></span>

<span data-ttu-id="d7684-146">Es werden beispielsweise keine Beschreibungen angezeigt, wenn Sie im Feld <strong><em>Eine Seite auswählen</em></strong> <strong>*Inventur*</strong> eingeben.</span><span class="sxs-lookup"><span data-stu-id="d7684-146">For example, no descriptions are shown when you type <strong>Counting</strong> in the *<strong><em>Select a page</em></strong>* field.</span></span> <span data-ttu-id="d7684-147">Wenn Sie die Dropdownliste öffnen, sehen Sie, dass es zwei Seiten mit der Bezeichnung <strong>Inventur</strong> gibt, sowie mehrere Seiten, die das Wort "Inventur" im Namen enthalten.</span><span class="sxs-lookup"><span data-stu-id="d7684-147">You open the drop-down list, and see that there are two pages that have the name <strong>Counting</strong> and several pages that contain the word "Counting" in the name.</span></span> <span data-ttu-id="d7684-148">Wenn Sie die Seite auswählen, die den AOT-Namen <strong>InventJournalCount</strong> hat, werden die Feldbeschreibungen für diese Seite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d7684-148">If you select the page that has the AOT name <strong>InventJournalCount</strong>, the field descriptions are shown for that page.</span></span> <span data-ttu-id="d7684-149">Wenn Sie jedoch die Dropdownliste erneut öffnen, werden Sie sehen, dass die Liste jetzt alle Seiten enthält, die "InventJournalCount" als Teil ihres AOT-Seitennamens haben.</span><span class="sxs-lookup"><span data-stu-id="d7684-149">However, if you open the drop-down list again, you will see that the list now contains all pages that have "InventJournalCount" as part of their AOT name.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="d7684-150">Problembehandlung</span><span class="sxs-lookup"><span data-stu-id="d7684-150">Troubleshooting</span></span>
<span data-ttu-id="d7684-151">In den folgenden Abschnitten finden Sie Informationen, zur Behebung von Problem, die auftreten können, wenn Sie Feldbeschreibungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="d7684-151">This section provides information to help you troubleshoot issues that you might encounter when you use field descriptions.</span></span>

### <a name="i-cant-find-a-field-description"></a><span data-ttu-id="d7684-152">Ich kann eine Feldbeschreibung nicht finden</span><span class="sxs-lookup"><span data-stu-id="d7684-152">I can't find a field description</span></span>

<span data-ttu-id="d7684-153">Wir sind daran, Beschreibungen für die komplexeren Felder hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="d7684-153">We’re in the process of adding descriptions for the more complex fields.</span></span> <span data-ttu-id="d7684-154">Wenn Sie Hilfe zu einem bestimmten Feld benötigen, informieren Sie uns, indem Sie diesem Thema einen Kommentar hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d7684-154">If you require help for a particular field, let us know by adding a comment for this topic.</span></span>

### <a name="the-field-description-isnt-helpful"></a><span data-ttu-id="d7684-155">Die Feldbeschreibung ist nicht hilfreich</span><span class="sxs-lookup"><span data-stu-id="d7684-155">The field description isn't helpful</span></span>

<span data-ttu-id="d7684-156">Informieren Sie uns, indem Sie diesem Thema einen Kommentar hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d7684-156">Let us know by adding a comment for this topic.</span></span> <span data-ttu-id="d7684-157">Wenn möglich, beschreiben Sie die zusätzlichen Informationen, die Sie benötigen.</span><span class="sxs-lookup"><span data-stu-id="d7684-157">If you can, describe the additional information that you require.</span></span>

### <a name="i-cant-find-a-field-on-the-field-descriptions-page"></a><span data-ttu-id="d7684-158">Ich kann ein Feld auf der Seite "Feldbeschreibung" nicht finden</span><span class="sxs-lookup"><span data-stu-id="d7684-158">I can't find a field on the Field descriptions page</span></span>

<span data-ttu-id="d7684-159">Um alle Felder auf einer Seite anzuzeigen, setzen Sie die Option **Inklusive-Felder ohne eine Beschreibung** auf **Ja** fest.</span><span class="sxs-lookup"><span data-stu-id="d7684-159">To show all the fields on a page, set the **Include fields without a description** option to **Yes**.</span></span> <span data-ttu-id="d7684-160">Klicken Sie auf das Feld **Seite auswählen**, um sicherzustellen, dass Sie die richtige Seite ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="d7684-160">Click the **Select a page** field to verify that you've selected the correct page.</span></span> <span data-ttu-id="d7684-161">Wenn der eingegebene Name Teil eines anderen Feldnamens ist, haben Sie möglicherweise die Seite mit dem längeren Namen ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="d7684-161">If the name that you typed is part of another field name, you might have selected the page that has the longer name.</span></span>

### <a name="i-cant-find-a-page-on-the-field-descriptions-page"></a><span data-ttu-id="d7684-162">Ich kann eine Seite auf der Seite "Feldbeschreibung" nicht finden</span><span class="sxs-lookup"><span data-stu-id="d7684-162">I can't find a page on the Field descriptions page</span></span>

<span data-ttu-id="d7684-163">Informationen über die verschiedenen Methoden zum Suchen von Seiten finden Sie Abschnitt "Nach einer Seite suchen" weiter oben in diesem Artikel.</span><span class="sxs-lookup"><span data-stu-id="d7684-163">For information about the various way to find pages, see the "Searching for pages" section earlier in this article.</span></span> <span data-ttu-id="d7684-164">Wenn Sie den genauen Namen der Seite eingegeben haben, werden die Feldbeschreibungen möglicherweise nicht angezeigt, wenn mehr als eine Seite gleichen Namens vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="d7684-164">If you've typed the exact name of the page, the field descriptions might not be shown if more than one page has the same name.</span></span> <span data-ttu-id="d7684-165">Klicken Sie auf den Pfeil im Feld **Eine Seite auswählen**, um eine gefilterte Liste der verfügbaren Seiten zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="d7684-165">Click the arrow in the **Select a page** field to open a filtered list of the pages that are available.</span></span>

<a name="additional-resources"></a><span data-ttu-id="d7684-166">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d7684-166">Additional resources</span></span>
--------

[<span data-ttu-id="d7684-167">Feldhilfe anpassen</span><span class="sxs-lookup"><span data-stu-id="d7684-167">Customize field help</span></span>](../../dev-itpro/user-interface/customize-field-help.md)





