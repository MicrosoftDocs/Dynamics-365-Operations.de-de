---
title: Mobile Rechnungsgenehmigungen
description: Dieses Thema soll einen praktischen Ansatz zum Entwerfen von mobilen Szenarien bereitstellen, indem es mobile Kreditorenrechnungsgenehmigungen als Anwendungsfall zeigt.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 88ba96b1d9d2f722528a4a920eabe4ab64304a7a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4443528"
---
# <a name="mobile-invoice-approvals"></a><span data-ttu-id="59cf6-103">Mobile Rechnungsgenehmigungen</span><span class="sxs-lookup"><span data-stu-id="59cf6-103">Mobile invoice approvals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="59cf6-104">Mithilfe der mobilen Funktionen können Geschäftsbenutzer mobile Erfahrungen entwerfen.</span><span class="sxs-lookup"><span data-stu-id="59cf6-104">Mobile capabilities let a business user design mobile experiences.</span></span> <span data-ttu-id="59cf6-105">Bei erweiterten Szenarien ermöglicht die Plattform auch Entwickler die Funktionen zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="59cf6-105">For advanced scenarios, the platform also lets developers extend the capabilities as they desire.</span></span> <span data-ttu-id="59cf6-106">Die effektivste Möglichkeit, einige der neuen mobilen Konzepten kennenzulernen, ist, den Prozess des Entwurfs einiger Szenarios durchzulaufen.</span><span class="sxs-lookup"><span data-stu-id="59cf6-106">The most effective way to learn some of the new concepts on mobile is to go through the process of designing a few scenarios.</span></span> <span data-ttu-id="59cf6-107">Dieses Thema soll einen praktischen Ansatz zum Entwerfen von mobilen Szenarien bereitstellen, indem es mobile Kreditorenrechnungsgenehmigungen als Anwendungsfall zeigt.</span><span class="sxs-lookup"><span data-stu-id="59cf6-107">This topic is intended to provide a practical approach to designing mobile scenarios by taking vendor invoice approvals for mobile as a use case.</span></span> <span data-ttu-id="59cf6-108">Dieses Thema soll helfen, andere der Szenarien zu entwerfen und kann auch auf anderen Szenarios angewendet werden, die nicht den Kreditorenrechnungen zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="59cf6-108">This topic should help you design other variations of the scenarios and can also be applied to other scenarios that aren’t related to vendor invoices.</span></span>

<a name="prerequisites"></a><span data-ttu-id="59cf6-109">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="59cf6-109">Prerequisites</span></span>
-------------

| <span data-ttu-id="59cf6-110">Voraussetzung</span><span class="sxs-lookup"><span data-stu-id="59cf6-110">Prerequisite</span></span>                                                                                            | <span data-ttu-id="59cf6-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="59cf6-111">Description</span></span>                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59cf6-112">Vorbereitung</span><span class="sxs-lookup"><span data-stu-id="59cf6-112">Mobile handbook pre-read</span></span>                                                                                |[<span data-ttu-id="59cf6-113">Mobile Plattform</span><span class="sxs-lookup"><span data-stu-id="59cf6-113">Mobile platform</span></span>](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md)                                                                                                  |
| <span data-ttu-id="59cf6-114">Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="59cf6-114">Dynamics 365 Finance</span></span>                                                                              | <span data-ttu-id="59cf6-115">Eine Umgebung mit Version 1611 und Plattform-Update 3 (November 2016)</span><span class="sxs-lookup"><span data-stu-id="59cf6-115">An environment that has version 1611 and Platform update 3 (November 2016)</span></span>                   |
| <span data-ttu-id="59cf6-116">Hotfix KB 3204341 installieren.</span><span class="sxs-lookup"><span data-stu-id="59cf6-116">Install hotfix KB 3204341.</span></span>                                                                              | <span data-ttu-id="59cf6-117">Die Aufgabenaufzeichnung kann fälschlicherweise zwei Scließen-Befehle für Dropdowndialogfelder erfassen, die in Plattform-Update 3 (November 2016) einbezogen sind</span><span class="sxs-lookup"><span data-stu-id="59cf6-117">Task recorder can erroneously record two Close commands for dropdown dialogs; this is included in Platform update 3 (November 2016 update).</span></span> |
| <span data-ttu-id="59cf6-118">Hotfix KB 3207800 installieren.</span><span class="sxs-lookup"><span data-stu-id="59cf6-118">Install hotfix KB 3207800.</span></span>                                                                              | <span data-ttu-id="59cf6-119">Dieser Hotfix ermöglicht das Anzeigen von Anhängen im mobilen Client, der in Plattform-Update 3 (November 2016) enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="59cf6-119">This hotfix enables attachments to be viewed on the mobile client; this is included in Platform update 3 (November 2016 update).</span></span>           |
| <span data-ttu-id="59cf6-120">Hotfix KB 3208224 installieren.</span><span class="sxs-lookup"><span data-stu-id="59cf6-120">Install hotfix KB 3208224.</span></span>                                                                              | <span data-ttu-id="59cf6-121">Anwendungscode für die mobile Kreditorenrechnungs-Genehmigungsanwendung ist in der Version 7.0.1 (Mai 2016) enthalten.</span><span class="sxs-lookup"><span data-stu-id="59cf6-121">Application code for the mobile vendor invoice approval application; this is included in version 7.0.1 (May 2016).</span></span>                          |
| <span data-ttu-id="59cf6-122">Ein Android- oder iOS- oder Windows-Gerät, auf dem die mobile App installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="59cf6-122">An Android or iOS or a Windows device that has the mobile app installed.</span></span> | <span data-ttu-id="59cf6-123">Suchen Sie die App im entsprechenden App-Store.</span><span class="sxs-lookup"><span data-stu-id="59cf6-123">Search for the app in the appropriate app store.</span></span>                                                                                                                     |

## <a name="introduction"></a><span data-ttu-id="59cf6-124">Einführung</span><span class="sxs-lookup"><span data-stu-id="59cf6-124">Introduction</span></span>
<span data-ttu-id="59cf6-125">Mobile Genehmigungen für Kreditorenrechnungen erfordern die drei Hotfixes, die im Abschnitt "Vorbereitung" angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="59cf6-125">Mobile approvals for vendor invoices require the three hotfixes that are mentioned in the “Prerequisites” section.</span></span> <span data-ttu-id="59cf6-126">Diese Hotfixes bieten keinen Arbeitsbereich für die Rechnungsgenehmigungen.</span><span class="sxs-lookup"><span data-stu-id="59cf6-126">These hotfixes don’t provide a workspace for the invoice approvals.</span></span> <span data-ttu-id="59cf6-127">Um zu lernen, was ein Arbeitsbereich im Rahmen des mobilen Clients ist, lesen Sie das Handbuch aus dem Abschnitt "Vorbereitung".</span><span class="sxs-lookup"><span data-stu-id="59cf6-127">To learn what a workspace is in the context of mobile, read the mobile handbook that is mentioned in the “Prerequisites” section.</span></span> <span data-ttu-id="59cf6-128">Der Rechnungsgenehmigungsarbeitsbereich muss konzipiert werden.</span><span class="sxs-lookup"><span data-stu-id="59cf6-128">The invoice approvals workspace must be designed.</span></span> 

<span data-ttu-id="59cf6-129">Jede Organisation definiert und nutzt eigene Geschäftsprozesse für Kreditorenrechnungen.</span><span class="sxs-lookup"><span data-stu-id="59cf6-129">Every organization orchestrates and defines its business process for vendor invoices differently.</span></span> <span data-ttu-id="59cf6-130">Bevor Sie eine mobile Erfahrung für Kreditorenrechnungsgenehmigungen entwerfen, müssen Sie die folgenden Aspekte des Geschäftsprozesses berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="59cf6-130">Before you design a mobile experience for vendor invoice approvals, you should consider the following aspects of the business process.</span></span> <span data-ttu-id="59cf6-131">Der Grundgedanke ist, diese Datenpunkten so weit wie möglich zu verwenden, um die Benutzerfreundlichkeit für das Gerät zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="59cf6-131">The idea is to use these data points as much as possible to optimize the user experience on the device.</span></span>

-   <span data-ttu-id="59cf6-132">Welche Felder aus dem Rechnungskopf wünschen die Benutzer in mobilen Umgebungen und in welcher Reihenfolge?</span><span class="sxs-lookup"><span data-stu-id="59cf6-132">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span>
-   <span data-ttu-id="59cf6-133">Welche Felder aus den Rechnungsposition wünschen die Benutzer in mobilen Umgebungen und in welcher Reihenfolge?</span><span class="sxs-lookup"><span data-stu-id="59cf6-133">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span>
-   <span data-ttu-id="59cf6-134">Wie viele Rechnungspositionen gibt es in einer Rechnung?</span><span class="sxs-lookup"><span data-stu-id="59cf6-134">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="59cf6-135">Wenden Sie die 80-20-Regel hier an, und optimieren Sie für 80 Prozent.</span><span class="sxs-lookup"><span data-stu-id="59cf6-135">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span>
-   <span data-ttu-id="59cf6-136">Möchten Benutzer Buchhaltungsverteilungen (Rechnungscodierung) auf dem mobilen Gerät sehen?</span><span class="sxs-lookup"><span data-stu-id="59cf6-136">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span> <span data-ttu-id="59cf6-137">Wenn die Antwort zu dieser Frage ja ist, beachten Sie die folgenden Fragen:</span><span class="sxs-lookup"><span data-stu-id="59cf6-137">If the answer to this question is yes, consider the following questions:</span></span>
    -   <span data-ttu-id="59cf6-138">Wie viele Buchhaltungsverteilungen (erweiterte Preis, Mehrwertsteuer, Belastungen, Teilungen, usw.) gibt es für eine Rechnungsposition?</span><span class="sxs-lookup"><span data-stu-id="59cf6-138">How many accounting distributions (extended price, sales tax, charges, splits, and so on) are there for an invoice line?</span></span> <span data-ttu-id="59cf6-139">Wieder gilt die Regel 80-20.</span><span class="sxs-lookup"><span data-stu-id="59cf6-139">Again, apply the 80-20 rule.</span></span>
    -   <span data-ttu-id="59cf6-140">Haben Rechnungen auch Buchhaltungsverteilungen im Rechnungskopf?</span><span class="sxs-lookup"><span data-stu-id="59cf6-140">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="59cf6-141">Falls ja sollen diese Buchhaltungsverteilungen im Gerät verfügbar sein?</span><span class="sxs-lookup"><span data-stu-id="59cf6-141">If so, should these accounting distributions be available on the device?</span></span>

    > [!NOTE]
    > <span data-ttu-id="59cf6-142">In diesem Thema wird nicht erläutert, wie Sie Buchhaltungsverteilungen bearbeitet, da diese Funktion nicht aktuell für mobile Szenarios unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="59cf6-142">This topic doesn’t explain how to edit accounting distributions, because this functionality isn’t currently supported for mobile scenarios.</span></span>

-   <span data-ttu-id="59cf6-143">Möchten Benutzer Anhänge für die Rechnung auf dem Gerät angezeigt?</span><span class="sxs-lookup"><span data-stu-id="59cf6-143">Will users want to see attachments for the invoice on the device?</span></span>

<span data-ttu-id="59cf6-144">Das Design der mobilen Erfahrung für Rechnungsgenehmigungen variiert, abhängig von den Antworten auf diese Fragen.</span><span class="sxs-lookup"><span data-stu-id="59cf6-144">The design of the mobile experience for invoice approvals will differ, depending on the answers to these questions.</span></span> <span data-ttu-id="59cf6-145">Die Zielsetzung ist, die Benutzerfreundlichkeit für den Geschäftsprozess auf Mobilgeräten in einer Organisation zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="59cf6-145">The objective is to optimize the user experience for the business process on mobile in an organization.</span></span> <span data-ttu-id="59cf6-146">Im Rest des Themas betrachten wir zwei Szenariovarianten die auf Grundlage unterschiedlicher Antworten auf Fragen vorhergehenden sind.</span><span class="sxs-lookup"><span data-stu-id="59cf6-146">In the rest of this topic, we will look at two scenario variations that are based on different answers to the preceding questions.</span></span> 

<span data-ttu-id="59cf6-147">Allgemeine, wenn mit dem mobilen Designer gearbeitet wird, vergewissern Sie sich, diese Änderungen veröffentlicht werden, um zu verhindern Aktualisierungen zu verlieren.</span><span class="sxs-lookup"><span data-stu-id="59cf6-147">As a general guidance, when working with the mobile designer, make sure to 'publish' the changes to prevent losing the updates.</span></span>

## <a name="designing-a-simple-invoice-approval-scenario-for-contoso"></a><span data-ttu-id="59cf6-148">Entwerfen eines einfachen Rechnungsgenehmigungsszenarios für Contoso</span><span class="sxs-lookup"><span data-stu-id="59cf6-148">Designing a simple invoice approval scenario for Contoso</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="59cf6-149">Szenarioattribut</span><span class="sxs-lookup"><span data-stu-id="59cf6-149">Scenario attribute</span></span></th>
<th><span data-ttu-id="59cf6-150">Antwort</span><span class="sxs-lookup"><span data-stu-id="59cf6-150">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="59cf6-151">Welche Felder aus dem Rechnungskopf wünschen die Benutzer in mobilen Umgebungen und in welcher Reihenfolge?</span><span class="sxs-lookup"><span data-stu-id="59cf6-151">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="59cf6-152">Kreditorenname</span><span class="sxs-lookup"><span data-stu-id="59cf6-152">Vendor name</span></span></li>
<li><span data-ttu-id="59cf6-153">Rechnungssumme</span><span class="sxs-lookup"><span data-stu-id="59cf6-153">Invoice total</span></span></li>
<li><span data-ttu-id="59cf6-154">Rechnungskonto</span><span class="sxs-lookup"><span data-stu-id="59cf6-154">Invoice account</span></span></li>
<li><span data-ttu-id="59cf6-155">Rechnungsnummer</span><span class="sxs-lookup"><span data-stu-id="59cf6-155">Invoice number</span></span></li>
<li><span data-ttu-id="59cf6-156">Rechnungsdatum</span><span class="sxs-lookup"><span data-stu-id="59cf6-156">Invoice date</span></span></li>
<li><span data-ttu-id="59cf6-157">Rechnungsbeschreibung</span><span class="sxs-lookup"><span data-stu-id="59cf6-157">Invoice description</span></span></li>
<li><span data-ttu-id="59cf6-158">Fälligkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="59cf6-158">Due date</span></span></li>
<li><span data-ttu-id="59cf6-159">Rechnungswährung</span><span class="sxs-lookup"><span data-stu-id="59cf6-159">Invoice currency</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="59cf6-160">Welche Felder aus den Rechnungsposition wünschen die Benutzer in mobilen Umgebungen und in welcher Reihenfolge?</span><span class="sxs-lookup"><span data-stu-id="59cf6-160">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="59cf6-161">Beschaffungskategorie</span><span class="sxs-lookup"><span data-stu-id="59cf6-161">Procurement category</span></span></li>
<li><span data-ttu-id="59cf6-162">Leistung</span><span class="sxs-lookup"><span data-stu-id="59cf6-162">Quantity</span></span></li>
<li><span data-ttu-id="59cf6-163">Preis je Einheit</span><span class="sxs-lookup"><span data-stu-id="59cf6-163">Unit price</span></span></li>
<li><span data-ttu-id="59cf6-164">Nettobetrag der Position</span><span class="sxs-lookup"><span data-stu-id="59cf6-164">Line net amount</span></span></li>
<li><span data-ttu-id="59cf6-165">Steuerbetrag (US 1099)</span><span class="sxs-lookup"><span data-stu-id="59cf6-165">1099 amount</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="59cf6-166">Wie viele Rechnungspositionen gibt es in einer Rechnung?</span><span class="sxs-lookup"><span data-stu-id="59cf6-166">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="59cf6-167">Wenden Sie die 80-20-Regel hier an, und optimieren Sie für 80 Prozent.</span><span class="sxs-lookup"><span data-stu-id="59cf6-167">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span></td>
<td><span data-ttu-id="59cf6-168">1</span><span class="sxs-lookup"><span data-stu-id="59cf6-168">1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="59cf6-169">Möchten Benutzer Buchhaltungsverteilungen (Rechnungscodierung) auf dem mobilen Gerät sehen?</span><span class="sxs-lookup"><span data-stu-id="59cf6-169">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span></td>
<td><span data-ttu-id="59cf6-170">Ja</span><span class="sxs-lookup"><span data-stu-id="59cf6-170">Yes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="59cf6-171">Wie viele Buchhaltungsverteilungen (erweiterte Preis, Mehrwertsteuer, Belastungen, usw.) gibt es für eine Rechnungsposition?</span><span class="sxs-lookup"><span data-stu-id="59cf6-171">How many accounting distributions (extended price, sales tax, charges, and so on) are there for an invoice line?</span></span> <span data-ttu-id="59cf6-172">Wieder gilt die Regel 80-20.</span><span class="sxs-lookup"><span data-stu-id="59cf6-172">Again, apply the 80-20 rule.</span></span></td>
<td><span data-ttu-id="59cf6-173">Erweiterter Preis: 2 Mehrwertsteuer: 0 Zuschläge: 0</span><span class="sxs-lookup"><span data-stu-id="59cf6-173">Extended price: 2 Sales tax: 0 Charges: 0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="59cf6-174">Haben Rechnungen auch Buchhaltungsverteilungen im Rechnungskopf?</span><span class="sxs-lookup"><span data-stu-id="59cf6-174">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="59cf6-175">Falls ja sollen diese Buchhaltungsverteilungen im Gerät verfügbar sein?</span><span class="sxs-lookup"><span data-stu-id="59cf6-175">If so, should these accounting distributions be available on the device?</span></span></td>
<td><span data-ttu-id="59cf6-176">Nicht verwendet</span><span class="sxs-lookup"><span data-stu-id="59cf6-176">Not used</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="59cf6-177">Möchten Benutzer Anhänge für die Rechnung auf dem Gerät angezeigt?</span><span class="sxs-lookup"><span data-stu-id="59cf6-177">Will users want to see attachments for the invoice on the device?</span></span></td>
<td><span data-ttu-id="59cf6-178">Ja</span><span class="sxs-lookup"><span data-stu-id="59cf6-178">Yes</span></span></td>
</tr>
</tbody>
</table>

### <a name="create-the-workspace"></a><span data-ttu-id="59cf6-179">Arbeitsbereich erstellen</span><span class="sxs-lookup"><span data-stu-id="59cf6-179">Create the workspace</span></span>

1.  <span data-ttu-id="59cf6-180">In einem Browser und melden Sie sich in der Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="59cf6-180">In a browser, and sign in to the application.</span></span>
2.  <span data-ttu-id="59cf6-181">Nachdem Sie angemeldet sind, hängen Sie **&mode=mobile** an die URL wie im folgenden Beispiel an und aktualisieren die Seite: https://&lt;yoururl&gt;/?cmp=usmf&mi=DefaultDashboard **&mode=mobile**</span><span class="sxs-lookup"><span data-stu-id="59cf6-181">After you’ve signed in, append **&mode=mobile** to the URL as shown in the following example, and refresh the page: https://&lt;yoururl&gt;/?cmp=usmf&mi=DefaultDashboard **&mode=mobile**</span></span>
3.  <span data-ttu-id="59cf6-182">Klicken Sie auf **Einstellungen** (Zahnrad) in der oberen rechten Ecke der Seite und klicken dann auf **Mobile App**.</span><span class="sxs-lookup"><span data-stu-id="59cf6-182">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**.</span></span> <span data-ttu-id="59cf6-183">Der Designer für mobile Apps wird wie die Aufgabenaufzeichnung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="59cf6-183">The mobile app designer must show up just as Task recorder shows up.</span></span>
4.  <span data-ttu-id="59cf6-184">Klicken Sie auf **Hinzufügen** um einen neuen Arbeitsbereich zu erstellen</span><span class="sxs-lookup"><span data-stu-id="59cf6-184">Click **Add** to create a new workspace.</span></span> <span data-ttu-id="59cf6-185">Im vorliegenden Beispiel ist Name des Arbeitsbereichs **Meine Genehmigungen**.</span><span class="sxs-lookup"><span data-stu-id="59cf6-185">For this example, name the workspace **My approvals**.</span></span>
5.  <span data-ttu-id="59cf6-186">Geben Sie eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="59cf6-186">Enter a description.</span></span>
6.  <span data-ttu-id="59cf6-187">Arbeitsbereichsfarbe auswählen.</span><span class="sxs-lookup"><span data-stu-id="59cf6-187">Select a workspace color.</span></span> <span data-ttu-id="59cf6-188">Die Arbeitsbereichfarbe wird für den Gesamtstil der mobilen Erfahrung für den Arbeitsbereich verwendet.</span><span class="sxs-lookup"><span data-stu-id="59cf6-188">The workspace color will be used for the overall style of the mobile experience for this workspace.</span></span>
7.  <span data-ttu-id="59cf6-189">Wählen Sie ein Symbol für den Arbeitsbereich aus.</span><span class="sxs-lookup"><span data-stu-id="59cf6-189">Select an icon for the workspace.</span></span>
8.  <span data-ttu-id="59cf6-190">Klicken Sie auf **Fertig.**</span><span class="sxs-lookup"><span data-stu-id="59cf6-190">Click **Done**</span></span>
9.  <span data-ttu-id="59cf6-191">Klicken Sie auf **Arbeitsbereich veröffentlichen**, um die Änderungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="59cf6-191">Click **Publish workspace** to save the changes</span></span>

### <a name="vendor-invoices-assigned-to-me"></a><span data-ttu-id="59cf6-192">Mir zugewiesene Kreditorenrechnungen</span><span class="sxs-lookup"><span data-stu-id="59cf6-192">Vendor invoices assigned to me</span></span>

<span data-ttu-id="59cf6-193">Die erste mobile Seite soll die Liste der Rechnungen, die dem Benutzer zur Genehmigung zugewiesen werden zeigen.</span><span class="sxs-lookup"><span data-stu-id="59cf6-193">The first mobile page that you should design is the list of invoices that are assigned to the user for review.</span></span> <span data-ttu-id="59cf6-194">Um diese mobile Seite zu entwerfen verwenden Sie die **VendMobileInvoiceAssignedToMeListPage**-Seite.</span><span class="sxs-lookup"><span data-stu-id="59cf6-194">To design this mobile page, use the **VendMobileInvoiceAssignedToMeListPage** page.</span></span> <span data-ttu-id="59cf6-195">Bevor Sie dieses Verfahren ausführen, stellen Sie sicher, dass mindestens eine Kreditorenrechnung zur Prüfung Ihnen zugewiesen ist und die Rechnungsposition zwei Verteilungen hat.</span><span class="sxs-lookup"><span data-stu-id="59cf6-195">Before you complete this procedure, make sure that at least one vendor invoice is assigned to you for review, and that the invoice line has two distributions.</span></span> <span data-ttu-id="59cf6-196">Diese Einstellung erfüllt die Bedingungen für dieses Szenarios.</span><span class="sxs-lookup"><span data-stu-id="59cf6-196">This setup meets the requirements for this scenario.</span></span>

1.  <span data-ttu-id="59cf6-197">In der URL ersetzen Sie den Namen der Menüoption durch **VendMobileInvoiceAssignedToMeListPage**, um die mobile Version der Listenseite **Ausstehende Kreditorenrechnungen – mir zugewiesen** im **Kreditor**-Modul zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="59cf6-197">In the URL, replace the name of the menu item with **VendMobileInvoiceAssignedToMeListPage** to open the mobile version of the **Pending vendor invoices assigned to me** list page in the **Accounts payable** module.</span></span> <span data-ttu-id="59cf6-198">Je nach der Anzahl von Rechnungen, die Sie in Ihrem System besitzen, das Ihnen zugeordnet ist, wird auf dieser Seite die Rechnungen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="59cf6-198">Depending on the number of invoices that you have in your system assigned to you, this page will show those invoices.</span></span> <span data-ttu-id="59cf6-199">Sie können den Filter links verwenden um eine bestimmte Rechnung zu suchen.</span><span class="sxs-lookup"><span data-stu-id="59cf6-199">To find a specific invoice, you can use the filter on the left.</span></span> <span data-ttu-id="59cf6-200">Allerdings benötigen wir keine bestimmte Rechnung für dieses Beispiel.</span><span class="sxs-lookup"><span data-stu-id="59cf6-200">However, we don’t require a specific invoice for this example.</span></span> <span data-ttu-id="59cf6-201">Es benötigen nur eine Rechnung, die Ihnen zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="59cf6-201">We just require some invoice assigned to you which is going to allow you to design the mobile page.</span></span> <span data-ttu-id="59cf6-202">Die neuen Seiten, die verfügbar sind, wurden insbesondere zum Entwickeln von mobilen Szenarien für Kreditorenrechnung entworfen.</span><span class="sxs-lookup"><span data-stu-id="59cf6-202">The new pages that are available have been designed specifically for developing mobile scenarios for vendor invoice.</span></span> <span data-ttu-id="59cf6-203">Daher müssen Sie diesen Seiten nutzen.</span><span class="sxs-lookup"><span data-stu-id="59cf6-203">Therefore, you must use these pages.</span></span> <span data-ttu-id="59cf6-204">Die URL muss der folgenden URL ähneln. Nachdem Sie sie eingeben haben, muss die Seite, die in der Abbildung dargestellt wird, angezeigt werden: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile</span><span class="sxs-lookup"><span data-stu-id="59cf6-204">The URL should resemble the following URL, and after you enter it, the page that is shown in the illustration must appear: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile</span></span> 

    <span data-ttu-id="59cf6-205">[![Seite „Ausstehende Kreditorenrechnungen – mir zugewiesen“](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)</span><span class="sxs-lookup"><span data-stu-id="59cf6-205">[![Pending vendor invoices assigned to me page](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)</span></span>
    
2.  <span data-ttu-id="59cf6-206">Klicken Sie auf **Einstellungen** (Zahnrad) in der oberen rechten Ecke der Seite und klicken dann auf **Mobile App**.</span><span class="sxs-lookup"><span data-stu-id="59cf6-206">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**</span></span>
3.  <span data-ttu-id="59cf6-207">Wählen Sie einen und Arbeitsbereich aus und klicken sie **Bearbeiten**</span><span class="sxs-lookup"><span data-stu-id="59cf6-207">Select your workspace and click **Edit**</span></span>
4.  <span data-ttu-id="59cf6-208">Klicken Sie auf **Seite hinzufügen**, um die ersten mobilen Seite zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="59cf6-208">Click **Add page** to create the first mobile page.</span></span>
5.  <span data-ttu-id="59cf6-209">Geben Sie einen Namen ein, z.B. meine **Meine Kreditorrechungen** und eine Beschreibung ein, z.B. **Mir zur Genehmigung zugeweisene Kreditorenrechnungen**.</span><span class="sxs-lookup"><span data-stu-id="59cf6-209">Enter a name, such as **My vendor invoices**, and a description, such as **Vendor invoices assigned to me for review**.</span></span>
6.  <span data-ttu-id="59cf6-210">Klicken Sie auf **Fertig**.</span><span class="sxs-lookup"><span data-stu-id="59cf6-210">Click **Done**.</span></span>
7.  <span data-ttu-id="59cf6-211">Im mobilen Designer auf der Registerkarte **Felder** klicken Sie auf **Felder wählen**.</span><span class="sxs-lookup"><span data-stu-id="59cf6-211">In the mobile designer, on the **Fields** tab, click **Select fields**.</span></span> <span data-ttu-id="59cf6-212">Die Spalten auf der Listenseite müssen der folgenden Abbildung ähneln.</span><span class="sxs-lookup"><span data-stu-id="59cf6-212">The columns on the list page must resemble the following illustration.</span></span> 

    <span data-ttu-id="59cf6-213">[![Spalten auf der Seite "Mir zugeweisene ausstehenden Kreditorenrechnungen"](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)</span><span class="sxs-lookup"><span data-stu-id="59cf6-213">[![Columns on the Pending vendor invoices assigned to me page](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)</span></span>
    
8.  <span data-ttu-id="59cf6-214">Fügen Sie die erforderlichen Spalten von der Listenseite hinzu, die für Benutzern in der mobilen Seite angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="59cf6-214">Add the required columns from the list page that must be shown to the users in the mobile page.</span></span> <span data-ttu-id="59cf6-215">Die Reihenfolge, in der Sie hinzufügen, entspricht der Reihenfolge, in der die Felder an Endbenutzer angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="59cf6-215">The order in which you add is the order in which the fields will be displayed to the end user.</span></span> <span data-ttu-id="59cf6-216">Die einzige Methode, die Reihenfolge der Felder zu ändern ist, indem alle Felder erneut auswählen.</span><span class="sxs-lookup"><span data-stu-id="59cf6-216">The only way to change the ordering of the fields will be by re-selecting all the fields.</span></span> <span data-ttu-id="59cf6-217">Basierend auf den Anforderungen für dieses Szenarios, sind die folgenden acht Felder obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="59cf6-217">Based on the requirements for this scenario, the following eight fields are required.</span></span> <span data-ttu-id="59cf6-218">Allerdings erachten mehrere Benutzer acht Felder für zu viele Informationen, die auf einem mobilen Gerät zu haben.</span><span class="sxs-lookup"><span data-stu-id="59cf6-218">However, some users might consider eight fields too much information to have on a mobile device.</span></span> <span data-ttu-id="59cf6-219">Daher werden nur die wichtigsten Felder in der mobilen Listenansicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="59cf6-219">Therefore, we will show only the most important fields in the mobile list view.</span></span> <span data-ttu-id="59cf6-220">Die übrigen Felder erscheinen in der Detailansicht, die Sie später entwerfen.</span><span class="sxs-lookup"><span data-stu-id="59cf6-220">The remaining fields will appear in the details view that we will design later.</span></span> <span data-ttu-id="59cf6-221">Jetzt fügen Sie nur die folgenden Felder hinzu.</span><span class="sxs-lookup"><span data-stu-id="59cf6-221">For now, we will add the following fields.</span></span> <span data-ttu-id="59cf6-222">Klicken Sie auf das Pluszeichen (**+**) in den Spalten die Sie zum mobilen Seite hinzuzufügen wollen.</span><span class="sxs-lookup"><span data-stu-id="59cf6-222">Click the plus sign (**+**) in these columns to add to the mobile page.</span></span>
    - <span data-ttu-id="59cf6-223">Kreditorenname</span><span class="sxs-lookup"><span data-stu-id="59cf6-223">Vendor name</span></span>
    - <span data-ttu-id="59cf6-224">Rechnungssumme</span><span class="sxs-lookup"><span data-stu-id="59cf6-224">Invoice total</span></span>
    - <span data-ttu-id="59cf6-225">Rechnungskonto</span><span class="sxs-lookup"><span data-stu-id="59cf6-225">Invoice account</span></span>
    - <span data-ttu-id="59cf6-226">Rechnungsnummer</span><span class="sxs-lookup"><span data-stu-id="59cf6-226">Invoice number</span></span>
    - <span data-ttu-id="59cf6-227">Rechnungsdatum</span><span class="sxs-lookup"><span data-stu-id="59cf6-227">Invoice date</span></span>

    <span data-ttu-id="59cf6-228">Nachdem die Felder hinzugefügt sind, muss die mobile Seite der folgenden Abbildung ähneln.</span><span class="sxs-lookup"><span data-stu-id="59cf6-228">After the fields are added, the mobile page must resemble the following illustration.</span></span> 
    
    <span data-ttu-id="59cf6-229">[![Seite nach Felder hinzugefügt](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)</span><span class="sxs-lookup"><span data-stu-id="59cf6-229">[![Page after fields are added](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)</span></span>

9.  <span data-ttu-id="59cf6-230">Sie müssen außerdem die folgenden Spalten hinzufügen, sodass wir Workflowaktivitäten später aktivieren können.</span><span class="sxs-lookup"><span data-stu-id="59cf6-230">You must also add the following columns now, so that we can enable workflow actions later.</span></span>
    - <span data-ttu-id="59cf6-231">Abgeschlossene Aufgabe anzeigen</span><span class="sxs-lookup"><span data-stu-id="59cf6-231">Show complete task</span></span>
    - <span data-ttu-id="59cf6-232">Delegataufgabe anzeigen</span><span class="sxs-lookup"><span data-stu-id="59cf6-232">Show delegate task</span></span>
    - <span data-ttu-id="59cf6-233">Zurückrufene Aufgabe anzeigen</span><span class="sxs-lookup"><span data-stu-id="59cf6-233">Show recall task</span></span>
    - <span data-ttu-id="59cf6-234">Abgelehnte Aufgabe anzeigen</span><span class="sxs-lookup"><span data-stu-id="59cf6-234">Show reject task</span></span>
    - <span data-ttu-id="59cf6-235">Abschlussanforderung Aufgabe anzeigen</span><span class="sxs-lookup"><span data-stu-id="59cf6-235">Show request completion task</span></span>
    - <span data-ttu-id="59cf6-236">Aufgabe erneut übermitteln anzeigen</span><span class="sxs-lookup"><span data-stu-id="59cf6-236">Show resubmit task</span></span>

10. <span data-ttu-id="59cf6-237">Klicken Sie auf **Fertig**, um den Bearbeitungsmodus zu verlassen.</span><span class="sxs-lookup"><span data-stu-id="59cf6-237">Click **Done** to exit edit mode.</span></span>
11. <span data-ttu-id="59cf6-238">Klicken Sie auf **Zurück** und **Fertig**, um den Arbeitsbereich zu beenden</span><span class="sxs-lookup"><span data-stu-id="59cf6-238">Click **Back** and then **Done** to exit the workspace</span></span>
12. <span data-ttu-id="59cf6-239">Klicken Sie auf **Arbeitsbereich veröffentlichen**, um die Arbeit zu speichern.</span><span class="sxs-lookup"><span data-stu-id="59cf6-239">Click **Publish workspace** to save your work.</span></span>
13. <span data-ttu-id="59cf6-240">Aktivieren Sie **Rechnungssumme in Kreditorenrechnungsliste anzeigen** im Formular Kreditorparameter unter **Rechnung**.</span><span class="sxs-lookup"><span data-stu-id="59cf6-240">Enable **Display invoice total on pending vendor invoices list** in accounts payable parameters form under **Invoice**.</span></span> <span data-ttu-id="59cf6-241">Beachten Sie, dass, nur, indem Sie diesen Parameter aktiviert, Rechnungssummen berechnet werden, der auf Kreditorenrechnungslistenseite ausstehenden angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="59cf6-241">Note that, only by enabling this parameter, invoice totals will be calculated to be displayed on the pending vendor invoices list page.</span></span> <span data-ttu-id="59cf6-242">Dies ist eine neue Funktion als Teil des erforderlichen Hotfixes 3208224.</span><span class="sxs-lookup"><span data-stu-id="59cf6-242">This is a new capability as part of the pre-requisite hot fix 3208224.</span></span>

### <a name="vendor-invoice-details"></a><span data-ttu-id="59cf6-243">Details der Kreditorenrechnung</span><span class="sxs-lookup"><span data-stu-id="59cf6-243">Vendor invoice details</span></span>

<span data-ttu-id="59cf6-244">Um die Rechnungsdetailseite für die mobile App zu entwerfen, verwenden Sie die **VendMobileInvoiceHeaderDetails**-Seite.</span><span class="sxs-lookup"><span data-stu-id="59cf6-244">To design the invoice details page for mobile, use the **VendMobileInvoiceHeaderDetails** page.</span></span> <span data-ttu-id="59cf6-245">Beachten Sie diese, abhängig von der Anzahl der Rechnungen, die Sie in Ihrem System gibt, enthält dieser Seite die älteste Rechnung (die Rechnung, die zuerst erstellt wurde).</span><span class="sxs-lookup"><span data-stu-id="59cf6-245">Note that, depending on the number of invoices that you have in your system, this page shows the oldest invoice (the invoice that was created first).</span></span> <span data-ttu-id="59cf6-246">Sie können den Filter links verwenden um eine bestimmte Rechnung zu suchen.</span><span class="sxs-lookup"><span data-stu-id="59cf6-246">To find a specific invoice, you can use the filter on the left.</span></span> <span data-ttu-id="59cf6-247">Allerdings benötigen wir keine bestimmte Rechnung für dieses Beispiel.</span><span class="sxs-lookup"><span data-stu-id="59cf6-247">However, we don’t require a specific invoice for this example.</span></span> <span data-ttu-id="59cf6-248">Es müssen nur einige Rechnungsinformationen, sodass wir die mobile Seite zu entwerfen.</span><span class="sxs-lookup"><span data-stu-id="59cf6-248">We just require some invoice data so that we can design the mobile page.</span></span> 

<span data-ttu-id="59cf6-249">[![Workflowseite](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)</span><span class="sxs-lookup"><span data-stu-id="59cf6-249">[![Workflow page](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)</span></span>

1. <span data-ttu-id="59cf6-250">In der URL ersetzen Sie den Namen der Menüoption durch **VendMobileInvoiceHeaderDetails**, um das Formular zu öffnen</span><span class="sxs-lookup"><span data-stu-id="59cf6-250">In the URL, replace the name of the menu item with **VendMobileInvoiceHeaderDetails** to open the form</span></span>

2. <span data-ttu-id="59cf6-251">Öffnen Sie den Designer von mobilen **Einstellungen** (Zahnrad) Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="59cf6-251">Open the mobile designer from the **Settings** (gear) button.</span></span>

3. <span data-ttu-id="59cf6-252">Klicken Sie auf die **Bearbeiten** Schaltfläche, um im Bearbeitungsmodus Arbeitsbereich zu starten.</span><span class="sxs-lookup"><span data-stu-id="59cf6-252">Click the **Edit** button to start edit mode in the workspace.</span></span>

4. <span data-ttu-id="59cf6-253">Wählen Sie die Seite **Meine Kreditorenrechnungen** aus, die Sie zuvor erstellt haben, und klicken Sie dann auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="59cf6-253">Select the **My vendor invoices** page that you created earlier, and then click **Edit**.</span></span>

5. <span data-ttu-id="59cf6-254">Auf der **Felder** Registerkarte klicken Sie auf die Spaltenüberschrift **Raster**</span><span class="sxs-lookup"><span data-stu-id="59cf6-254">On the **Fields** tab, click the **Grid** column heading.</span></span>

6. <span data-ttu-id="59cf6-255">Klicken Sie auf **Eigenschaften &gt; Seite hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="59cf6-255">Click **Properties &gt; Add page**.</span></span> <span data-ttu-id="59cf6-256">**Hinweis:** Wenn Sie auf das **Raster** Überschrift klicken und eine Seite hinzufügen, wird die Beziehung zur Detailseite automatisch bestimmt.</span><span class="sxs-lookup"><span data-stu-id="59cf6-256">**Note:** When you click the **Grid** heading and add a page, the relationship with the details page is established automatically.</span></span>

7. <span data-ttu-id="59cf6-257">Geben Sie einen Seitentitel, z.B. **Rechnungsdetails** und einer Beschreibung, wie ein **Ansichtsrechnungskopf und Positionsdetails**.</span><span class="sxs-lookup"><span data-stu-id="59cf6-257">Enter a page title, such as **Invoice details**, and a description, such as **View invoice header and line details**.</span></span>

8. <span data-ttu-id="59cf6-258">Klicken Sie auf **Felder auswählen**.</span><span class="sxs-lookup"><span data-stu-id="59cf6-258">Click **Select fields**.</span></span> <span data-ttu-id="59cf6-259">Die Reihenfolge, in der Sie hinzufügen, entspricht der Reihenfolge, in der die Felder an Endbenutzer angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="59cf6-259">Note that, the order in which you add is the order in which the fields will be displayed to the end user.</span></span> <span data-ttu-id="59cf6-260">Die einzige Methode, die Reihenfolge der Felder zu ändern ist, indem alle Felder erneut auswählen.</span><span class="sxs-lookup"><span data-stu-id="59cf6-260">The only way to change the ordering of the fields will be by re-selecting all the fields.</span></span> 

9. <span data-ttu-id="59cf6-261">Fügen Sie die folgenden Felder aus dem Auftragskopf, basierend auf den Anforderungen für dieses Szenarios hinzu:</span><span class="sxs-lookup"><span data-stu-id="59cf6-261">Add the following fields from the header, based on the requirements for this scenario:</span></span>
   - <span data-ttu-id="59cf6-262">Kreditorenname</span><span class="sxs-lookup"><span data-stu-id="59cf6-262">Vendor name</span></span>
   - <span data-ttu-id="59cf6-263">Rechnungssumme</span><span class="sxs-lookup"><span data-stu-id="59cf6-263">Invoice total</span></span>
   - <span data-ttu-id="59cf6-264">Rechnungskonto</span><span class="sxs-lookup"><span data-stu-id="59cf6-264">Invoice account</span></span>
   - <span data-ttu-id="59cf6-265">Rechnungsnummer</span><span class="sxs-lookup"><span data-stu-id="59cf6-265">Invoice number</span></span>
   - <span data-ttu-id="59cf6-266">Rechnungsdatum</span><span class="sxs-lookup"><span data-stu-id="59cf6-266">Invoice date</span></span>
   - <span data-ttu-id="59cf6-267">Rechnungsbeschreibung</span><span class="sxs-lookup"><span data-stu-id="59cf6-267">Invoice description</span></span>
   - <span data-ttu-id="59cf6-268">Fälligkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="59cf6-268">Due date</span></span>
   - <span data-ttu-id="59cf6-269">Rechnungswährung</span><span class="sxs-lookup"><span data-stu-id="59cf6-269">Invoice currency</span></span>

10. <span data-ttu-id="59cf6-270">Fügen Sie die folgenden Felder aus Positionsraster auf der Seite hinzu:</span><span class="sxs-lookup"><span data-stu-id="59cf6-270">Add the following fields from the lines grid on the page:</span></span>
    - <span data-ttu-id="59cf6-271">Beschaffungskategorie</span><span class="sxs-lookup"><span data-stu-id="59cf6-271">Procurement category</span></span>
    - <span data-ttu-id="59cf6-272">Leistung</span><span class="sxs-lookup"><span data-stu-id="59cf6-272">Quantity</span></span>
    - <span data-ttu-id="59cf6-273">Preis je Einheit</span><span class="sxs-lookup"><span data-stu-id="59cf6-273">Unit price</span></span>
    - <span data-ttu-id="59cf6-274">Nettobetrag der Position</span><span class="sxs-lookup"><span data-stu-id="59cf6-274">Line net amount</span></span>
    - <span data-ttu-id="59cf6-275">Steuerbetrag (US 1099)</span><span class="sxs-lookup"><span data-stu-id="59cf6-275">1099 amount</span></span>

11. <span data-ttu-id="59cf6-276">Nachdem alle Felder aus den früheren zwei Schritten hinzugefügt wurden, klicken Sie auf **Fertig**.</span><span class="sxs-lookup"><span data-stu-id="59cf6-276">After all the fields from the previous two steps have been added, click **Done**.</span></span> <span data-ttu-id="59cf6-277">Die müssen der folgenden Abbildung ähneln.</span><span class="sxs-lookup"><span data-stu-id="59cf6-277">The page must resemble the following illustration.</span></span>
    
    <span data-ttu-id="59cf6-278">[![Seite nach Felder hinzugefügt](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)</span><span class="sxs-lookup"><span data-stu-id="59cf6-278">[![Page after fields are added](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)</span></span>

12. <span data-ttu-id="59cf6-279">Klicken Sie auf **Fertig**, um den Bearbeitungsmodus zu verlassen.</span><span class="sxs-lookup"><span data-stu-id="59cf6-279">Click **Done** to exit edit mode.</span></span>

13. <span data-ttu-id="59cf6-280">Klicken Sie auf **Zurück** und **Fertig**, um den Arbeitsbereich zu beenden</span><span class="sxs-lookup"><span data-stu-id="59cf6-280">Click **Back** and then **Done** to exit the workspace</span></span>

14. <span data-ttu-id="59cf6-281">Klicken Sie auf **Arbeitsbereich veröffentlichen**, um die Arbeit zu speichern.</span><span class="sxs-lookup"><span data-stu-id="59cf6-281">Click **Publish workspace** to save your work</span></span>

### <a name="workflow-actions"></a><span data-ttu-id="59cf6-282">Workflowaktivitäten</span><span class="sxs-lookup"><span data-stu-id="59cf6-282">Workflow actions</span></span>

<span data-ttu-id="59cf6-283">Um Workflow-Aktionen hinzuzufügen, verwenden Sie die Seite **VendMobileInvoiceHeaderDetails**.</span><span class="sxs-lookup"><span data-stu-id="59cf6-283">To add workflow actions, use the **VendMobileInvoiceHeaderDetails** page.</span></span> <span data-ttu-id="59cf6-284">Um diese Seite zu öffnen, ersetzen Sie Name der Menüoption in die URL, wie Sie eben geschehen ist.</span><span class="sxs-lookup"><span data-stu-id="59cf6-284">To open this page, replace the name of the menu item in the URL, as you did earlier.</span></span> <span data-ttu-id="59cf6-285">Öffnen Sie den Designer von mobilen **Einstellungen** (Zahnrad) Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="59cf6-285">Then open the mobile designer from the **Settings** (gear) button.</span></span> <span data-ttu-id="59cf6-286">Gehen Sie folgendermaßen vor, um die Detailseite auf Workflowaktivitäten hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="59cf6-286">Follow these steps to add workflow actions on the details page.</span></span> <span data-ttu-id="59cf6-287">Sie müssen Rechnungen haben, die Ihnen zugewiesen wurden, die sich in einem angemessenen Status befinden, damit Ihnen die Workflowaktivitäten zur Verfügung stehen, für die Sie entwerfen möchten.</span><span class="sxs-lookup"><span data-stu-id="59cf6-287">You must have invoices assigned to you that are in the appropriate state to make the workflow actions available to you that you are going to design for.</span></span>

#### <a name="record-workflow-actions"></a><span data-ttu-id="59cf6-288">Workflowaktivitäten erfassen</span><span class="sxs-lookup"><span data-stu-id="59cf6-288">Record workflow actions</span></span>
1.  <span data-ttu-id="59cf6-289">Klicken Sie auf die **Bearbeiten** Schaltfläche, um im Bearbeitungsmodus Arbeitsbereich zu starten.</span><span class="sxs-lookup"><span data-stu-id="59cf6-289">Click the **Edit** button to start edit mode in the workspace.</span></span>
2.  <span data-ttu-id="59cf6-290">Wählen Sie die **Rechnungsdetails** Seite, die Sie eben erstellt haben, und klicken Sie dann **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="59cf6-290">Select the **Invoice details** page that you created earlier, and then click **Edit**.</span></span>
3.  <span data-ttu-id="59cf6-291">Klicken Sie auf der Registerkarte **Aktionen** auf **Aktion hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="59cf6-291">On the **Actions** tab, click **Add action**.</span></span>
4.  <span data-ttu-id="59cf6-292">Geben Sie einen Aktivitätstitel, z. B. **Genehmigen** und eine Beschreibung ein, z.B. **Rechnung genehmigen**.</span><span class="sxs-lookup"><span data-stu-id="59cf6-292">Enter an action title, such as **Approve**, and a description, such as **Approve invoice**.</span></span> <span data-ttu-id="59cf6-293">Beachten Sie, dass der Aktivitätstitel, den Sie hier eingeben, der Name der Aktivität ist, den Benutzer in der Zeit-App mobilen die angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="59cf6-293">Note that the action title that you enter here becomes the name of the action that is shown to the user in the mobile app.</span></span>
5.  <span data-ttu-id="59cf6-294">Klicken Sie auf **Fertig**.</span><span class="sxs-lookup"><span data-stu-id="59cf6-294">Click **Done**.</span></span>
6.  <span data-ttu-id="59cf6-295">Klicken Sie auf **Felder auswählen**.</span><span class="sxs-lookup"><span data-stu-id="59cf6-295">Click **Select fields**.</span></span>
7.  <span data-ttu-id="59cf6-296">Führen des Workflowprozesses auf der **VendMobileInvoiceHeaderDetails** Seite durch, und schließen Sie die Aktivität aus, die Sie erfassen. Ihren Planungen zufolge</span><span class="sxs-lookup"><span data-stu-id="59cf6-296">Go through the workflow process on the **VendMobileInvoiceHeaderDetails** page, and complete the action that you wanted to record.</span></span> <span data-ttu-id="59cf6-297">Überprüfen Sie, ob Sie Workflowkommentare während dieses Vorgangs ein eingegeben werden, damit auch im Kommentarfeld mobilen Erfahrung enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="59cf6-297">Make sure that you enter workflow comments during this process, so that a comments field is also included in the mobile experience.</span></span>
8.  <span data-ttu-id="59cf6-298">Nachdem die Workflowaktivität ausgeführt ist, klicken Sie auf **Fertig**, um die Felder auswählen-Aufgabe abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="59cf6-298">After the workflow action is run, click **Done** to complete the Select fields task.</span></span>
9.  <span data-ttu-id="59cf6-299">Klicken Sie auf **Fertig**, um den Bearbeitungsmodus zu verlassen.</span><span class="sxs-lookup"><span data-stu-id="59cf6-299">Click **Done** to exit edit mode.</span></span>
10. <span data-ttu-id="59cf6-300">Klicken Sie auf **Zurück** und **Fertig**, um den Arbeitsbereich zu beenden</span><span class="sxs-lookup"><span data-stu-id="59cf6-300">Click **Back** and then **Done** to exit the workspace</span></span>
11. <span data-ttu-id="59cf6-301">Klicken Sie auf **Arbeitsbereich veröffentlichen**, um die Arbeit zu speichern.</span><span class="sxs-lookup"><span data-stu-id="59cf6-301">Click **Publish workspace** to save your work</span></span>
12. <span data-ttu-id="59cf6-302">Wiederholen Sie die vorherigen Schritte, um alle erforderlichen Workflowaktivitäten zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="59cf6-302">Repeat the previous steps to record all the required workflow actions.</span></span> 

#### <a name="create-a-js-file"></a><span data-ttu-id="59cf6-303">Erstellen Sie eine JS-Datei.</span><span class="sxs-lookup"><span data-stu-id="59cf6-303">Create a .js file</span></span>
1. <span data-ttu-id="59cf6-304">Öffnen Sie den Editor oder Microsoft Visual Studio, und fügen Sie den folgenden Code ein.</span><span class="sxs-lookup"><span data-stu-id="59cf6-304">Open Notepad or Microsoft Visual Studio, and paste the following code.</span></span> <span data-ttu-id="59cf6-305">Speichern Sie die Datei als .js-Datei.</span><span class="sxs-lookup"><span data-stu-id="59cf6-305">Save the file as a .js file.</span></span> <span data-ttu-id="59cf6-306">Diese Code bewirkt Folgendes:</span><span class="sxs-lookup"><span data-stu-id="59cf6-306">This code does the following:</span></span>
    - <span data-ttu-id="59cf6-307">Er blendet die zusätzlichen workflowbezogenen Spalten aus, die wir früher mobilen auf der Listenseite hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="59cf6-307">It hides the extra workflow-related columns that we added earlier on the mobile list page.</span></span> <span data-ttu-id="59cf6-308">Es werden diesen Spalten hinzufügen, sodass der Zeit-App dass Informationen im Zusammenhang hat und die nächsten Schritt ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="59cf6-308">We added these columns so that the app has that information in context and can do the next step.</span></span>
    - <span data-ttu-id="59cf6-309">Anhand des Workflowschritt, die aktiv ist, wendet sie Logik, um nur die Vorgänge anzeigen.</span><span class="sxs-lookup"><span data-stu-id="59cf6-309">Based on the workflow step that is active, it applies logic to show only those actions.</span></span>

    > [!NOTE]
    > <span data-ttu-id="59cf6-310">Die Namen der Seiten und andere Steuerelemente im Code müssen mit den Namen im Arbeitsbereich identisch sein.</span><span class="sxs-lookup"><span data-stu-id="59cf6-310">The name of the pages and other controls in the code must be the same as the names in the workspace.</span></span>

    ```javascript
    function main(metadataService, dataService, cacheService, $q) {
           return {
               appInit: function (appMetadata) {
                   // Hide controls that need to be present, but not visible
                   metadataService.configureControl('My-vendor-invoices', 'ShowAccept', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowApprove', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowReject', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowDelegate', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowRequestChange', { hidden: true });
                 metadataService.configureControl('My-vendor-invoices', 'ShowRecall', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowComplete', { hidden: true });
               metadataService.configureControl('My-vendor-invoices', 'ShowResubmit', { hidden: true });
               },
               pageInit: function (pageMetadata, params) {
        if (pageMetadata.Name == 'Invoice-details') {
                       // Show/hide workflow actions based on workflow step
                       metadataService.configureAction('Accept', { visible: true });
                       metadataService.configureAction('Approve', { visible: true });
                       metadataService.configureAction('Reject', { visible: true });
                       metadataService.configureAction('Delegate', { visible: true });
                       metadataService.configureAction('Request-change', { visible: true });
                       metadataService.configureAction('Recall', { visible: true });
                       metadataService.configureAction('Complete', { visible: true });
                       metadataService.configureAction('Resubmit', { visible: true });

                       var entityContextParts = params.pageContext.split(':');
                       var data = dataService.getEntityData(entityContextParts[0], entityContextParts[1]);

                       var acceptControl = data.getPropertyValue('VendInvoiceInfoTable/showAccept');
                       var approveControl = data.getPropertyValue('VendInvoiceInfoTable/showApprove');
                       var rejectControl = data.getPropertyValue('VendInvoiceInfoTable/showReject');
                       var delegateControl = data.getPropertyValue('VendInvoiceInfoTable/showDelegate');
                       var requestChangeControl = data.getPropertyValue('VendInvoiceInfoTable/showRequestChange');
                       var recallControl = data.getPropertyValue('VendInvoiceInfoTable/showRecall');
                       var completeControl = data.getPropertyValue('VendInvoiceInfoTable/showComplete');
                       var resubmitControl = data.getPropertyValue('VendInvoiceInfoTable/showResubmit');

                       var showAcceptControl = Boolean(acceptControl == 1);
                       var showApproveControl = Boolean(approveControl == 1);
                       var showRejectControl = Boolean(rejectControl == 1);
                      var showDelegateControl = Boolean(delegateControl == 1);
                       var showRequestChangeControl = Boolean(requestChangeControl == 1);
                       var showRecallControl = Boolean(recallControl == 1);
                       var showCompleteControl = Boolean(completeControl == 1);
                       var showResubmitControl = Boolean(resubmitControl == 1);

                       metadataService.configureAction('Accept', { visible: showAcceptControl });
                       metadataService.configureAction('Approve', { visible: showApproveControl });
                       metadataService.configureAction('Reject', { visible: showRejectControl });
                       metadataService.configureAction('Delegate', { visible: showDelegateControl });
                       metadataService.configureAction('Request-change', { visible: showRequestChangeControl });
                       metadataService.configureAction('Recall', { visible: showRecallControl });
                       metadataService.configureAction('Complete', { visible: showCompleteControl });
                     metadataService.configureAction('Resubmit', { visible: showResubmitControl });
                   }
                 },
           };
        }
    ```

2.  <span data-ttu-id="59cf6-311">Laden Sie die Codedatei dem Arbeitsbereich hohe, indem Sie die **Logik** Registerkarte auswählen</span><span class="sxs-lookup"><span data-stu-id="59cf6-311">Upload the code file to the workspace by selecting the **Logic** tab</span></span>
3.  <span data-ttu-id="59cf6-312">Klicken Sie auf **Fertig**, um den Bearbeitungsmodus zu verlassen.</span><span class="sxs-lookup"><span data-stu-id="59cf6-312">Click **Done** to exit edit mode.</span></span>
4.  <span data-ttu-id="59cf6-313">Klicken Sie auf **Zurück** und **Fertig**, um den Arbeitsbereich zu beenden</span><span class="sxs-lookup"><span data-stu-id="59cf6-313">Click **Back** and then **Done** to exit the workspace</span></span>
5.  <span data-ttu-id="59cf6-314">Klicken Sie auf **Arbeitsbereich veröffentlichen**, um die Arbeit zu speichern.</span><span class="sxs-lookup"><span data-stu-id="59cf6-314">Click **Publish workspace** to save your work</span></span>

### <a name="vendor-invoice-attachments"></a><span data-ttu-id="59cf6-315">Kreditorenrechungsanhänge</span><span class="sxs-lookup"><span data-stu-id="59cf6-315">Vendor invoice attachments</span></span>

1. <span data-ttu-id="59cf6-316">Klicken Sie auf **Einstellungen** (Zahnrad) in der oberen rechten Ecke der Seite und klicken dann auf **Mobile App**.</span><span class="sxs-lookup"><span data-stu-id="59cf6-316">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**</span></span>

2. <span data-ttu-id="59cf6-317">Klicken Sie auf die **Bearbeiten** Schaltfläche, um im Bearbeitungsmodus Arbeitsbereich zu starten.</span><span class="sxs-lookup"><span data-stu-id="59cf6-317">Click the **Edit** button to start edit mode in the workspace.</span></span>

3. <span data-ttu-id="59cf6-318">Wählen Sie die Seite <strong>Rechnungsdetails **aus, die Sie zuvor erstellt haben, und klicken Sie dann auf** Bearbeiten</strong>.</span><span class="sxs-lookup"><span data-stu-id="59cf6-318">Select the <strong>Invoice details \*\*page that you created earlier, and then click \*\*Edit</strong>.</span></span>

4. <span data-ttu-id="59cf6-319">Legen Sie die **Dokumentverwaltung** Option **Ja** wie weiter unten fest.</span><span class="sxs-lookup"><span data-stu-id="59cf6-319">Set the **Document management** option to **Yes** as shown below.</span></span> <span data-ttu-id="59cf6-320">**Hinweis:** Wenn keine Anforderungen gibt, Zuordnungen im mobilen Gerät angezeigt werden, können Sie diese Option **Nein**, mit der die Standardeinstellung ist.</span><span class="sxs-lookup"><span data-stu-id="59cf6-320">**Note:** If there are no requirements to show attachments on the mobile device, you can leave this option set to **No**, which is the default setting.</span></span>
   
   ![Dokumentverwaltung](./media/docmanagement-216x300.png)

5. <span data-ttu-id="59cf6-322">Klicken Sie auf **Fertig**, um den Bearbeitungsmodus zu verlassen.</span><span class="sxs-lookup"><span data-stu-id="59cf6-322">Click **Done** to exit edit mode.</span></span>

6. <span data-ttu-id="59cf6-323">Klicken Sie auf **Zurück** und **Fertig**, um den Arbeitsbereich zu beenden</span><span class="sxs-lookup"><span data-stu-id="59cf6-323">Click **Back** and then **Done** to exit the workspace</span></span>

7. <span data-ttu-id="59cf6-324">Klicken Sie auf **Arbeitsbereich veröffentlichen**, um die Arbeit zu speichern.</span><span class="sxs-lookup"><span data-stu-id="59cf6-324">Click **Publish workspace** to save your work</span></span>

### <a name="vendor-invoice-line-distributions"></a><span data-ttu-id="59cf6-325">Kreditorrechungspositionsverteilungen</span><span class="sxs-lookup"><span data-stu-id="59cf6-325">Vendor invoice line distributions</span></span>

<span data-ttu-id="59cf6-326">Die Anforderungen für dieses Szenarios bestätigen, dass nur Verteilungen auf Positionsebene sind und dass eine Rechnung immer nur eine Position ist.</span><span class="sxs-lookup"><span data-stu-id="59cf6-326">The requirements for this scenario confirm that there will be only line-level distributions, and that an invoice will always have only one line.</span></span> <span data-ttu-id="59cf6-327">Da dieses Szenario ist einfach, muss die Benutzerfreundlichkeit auf dem auch einfach mobilen Gerät genug sein, dem der Benutzer nicht mehrere Ebenen muss Detailinformationen anzeigen, damit die Verteilungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="59cf6-327">Because this scenario is simple, the user experience on the mobile device must also be simple enough that the user doesn’t have to drill down several levels to view the distributions.</span></span> <span data-ttu-id="59cf6-328">Kreditorenrechnungen enthalten die Option des Anzeigens aller Verteilungen aus dem Rechnungskopf.</span><span class="sxs-lookup"><span data-stu-id="59cf6-328">Vendor invoices include the option of showing all distributions from the invoice header.</span></span> <span data-ttu-id="59cf6-329">Diese Umgebung ist was wir für das mobile Szenario benötigen.</span><span class="sxs-lookup"><span data-stu-id="59cf6-329">This experience is what we need for the mobile scenario.</span></span> <span data-ttu-id="59cf6-330">Daher verwenden Sie die **VendMobileInvoiceAllDistributionTree** Seite, um diesen Teil des mobilen Szenarios zu entwerfen.</span><span class="sxs-lookup"><span data-stu-id="59cf6-330">Therefore, we will use the **VendMobileInvoiceAllDistributionTree** page to design this part of the mobile scenario.</span></span> 

> [!NOTE] 
> <span data-ttu-id="59cf6-331">Das Kennen der Anforderungen können uns, entscheiden, die die betreffende genau zu verwenden Seite, und wie die mobile Erfahrung des Benutzers optimiert, wenn Sie das Szenario entwerfen.</span><span class="sxs-lookup"><span data-stu-id="59cf6-331">Knowing the requirements helps us decide which specific page to use and how exactly to optimize the mobile experience for the user when we design the scenario.</span></span> <span data-ttu-id="59cf6-332">Im zweiten Szenario können wir eine andere Seite, damit die Verteilungen anzuzeigen, weil die Anforderungen für dieses Szenarios unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="59cf6-332">In the second scenario, we will use a different page to show the distributions, because the requirements for that scenario differ.</span></span>

1.  <span data-ttu-id="59cf6-333">In der URL ersetzten Sie den Name der Menüoption.</span><span class="sxs-lookup"><span data-stu-id="59cf6-333">In the URL, replace the name of the menu item, as you did before.</span></span> <span data-ttu-id="59cf6-334">Die Seite, die angezeigt wird, sollte der folgenden Abbildung ähneln.</span><span class="sxs-lookup"><span data-stu-id="59cf6-334">The page that appears should resemble the following illustration.</span></span>

    <span data-ttu-id="59cf6-335">[![Alle Verteilungen-Seite](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)</span><span class="sxs-lookup"><span data-stu-id="59cf6-335">[![All distributions page](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)</span></span>

2.  <span data-ttu-id="59cf6-336">Öffnen Sie den Designer von mobilen **Einstellungen** (Zahnrad) Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="59cf6-336">Open the mobile designer from the **Settings** (gear) button.</span></span>

3.  <span data-ttu-id="59cf6-337">Klicken Sie auf die **Bearbeiten** Schaltfläche, um im Bearbeitungsmodus Arbeitsbereich zu starten.</span><span class="sxs-lookup"><span data-stu-id="59cf6-337">Click the **Edit** button to start edit mode in the workspace.</span></span> <span data-ttu-id="59cf6-338">**Hinweis:** Sie sehen, dass zwei neue Seiten automatisch erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="59cf6-338">**Note:** You will see that two new pages were created automatically.</span></span> <span data-ttu-id="59cf6-339">Das System diese Seiten erstellt, da Sie die Dokumentverwaltung im vorherigen Abschnitt einschalteten.</span><span class="sxs-lookup"><span data-stu-id="59cf6-339">The system creates these pages, because you turned on document management in the previous section.</span></span> <span data-ttu-id="59cf6-340">Sie können diese Seiten neuen ignorieren.</span><span class="sxs-lookup"><span data-stu-id="59cf6-340">You can ignore these new pages.</span></span>

4.  <span data-ttu-id="59cf6-341">Klicken Sie auf **Seite hinzufügen.**</span><span class="sxs-lookup"><span data-stu-id="59cf6-341">Click **Add page**.</span></span>

5.  <span data-ttu-id="59cf6-342">Geben Sie einen Seitentitel, wie **Ansichtsbuchhaltung** und eine Beschreibung ein, z.B. **Ansicht für die Rechnung** ein.</span><span class="sxs-lookup"><span data-stu-id="59cf6-342">Enter a page title, such as **View accounting**, and a description, such as **View accounting for the invoice**.</span></span>

6.  <span data-ttu-id="59cf6-343">Klicken Sie auf **Fertig**.</span><span class="sxs-lookup"><span data-stu-id="59cf6-343">Click **Done**.</span></span>

7.  <span data-ttu-id="59cf6-344">Auf der Registerkarte **Felder** wählen Sie **Felder auswählen**, die folgenden Felder aus der Verteilungsseite aus und klicken dann **Fertig**.</span><span class="sxs-lookup"><span data-stu-id="59cf6-344">On the **Fields** tab, click **Select fields**, select the following fields from the distributions page, and then click **Done**:</span></span>
    1.  <span data-ttu-id="59cf6-345">Betrag</span><span class="sxs-lookup"><span data-stu-id="59cf6-345">Amount</span></span>
    2.  <span data-ttu-id="59cf6-346">Währung</span><span class="sxs-lookup"><span data-stu-id="59cf6-346">Currency</span></span>
    3.  <span data-ttu-id="59cf6-347">Sachkonto</span><span class="sxs-lookup"><span data-stu-id="59cf6-347">Ledger account</span></span>

    > [!NOTE] 
    > <span data-ttu-id="59cf6-348">Es können die **Beschreibung** Spalte im Verteilungsraster aus, weil die Anforderungen für dieses Szenarios bestätigten, dass der erweiterte Preis der einzige Betrag ist, dass für Verteilungen gibt.</span><span class="sxs-lookup"><span data-stu-id="59cf6-348">We didn’t select the **Description** column from the distributions grid, because the requirements for this scenario confirmed that the extended price is the only amount that there will be distributions for.</span></span> <span data-ttu-id="59cf6-349">Daher fordert der Benutzer kein anderes Feld, den Betragstyp festzustellen, ob die Verteilung für ist.</span><span class="sxs-lookup"><span data-stu-id="59cf6-349">Therefore, the user won’t require another field to determine the amount type that the distribution is for.</span></span> <span data-ttu-id="59cf6-350">Allerdings im folgenden Szenario verwenden, wir **werden** Sie diese Informationen, weil die Anforderungen für dieses Szenarios angeben, dass andere Betragsart Verteilungen haben (z, Mehrwertsteuer).</span><span class="sxs-lookup"><span data-stu-id="59cf6-350">However, in the next scenario, we **will** use this information, because the requirements for that scenario specify that other amount types have distributions (for example, sales tax).</span></span>

8.  <span data-ttu-id="59cf6-351">Klicken Sie auf **Fertig**, um den Bearbeitungsmodus zu verlassen.</span><span class="sxs-lookup"><span data-stu-id="59cf6-351">Click **Done** to exit edit mode.</span></span>

9.  <span data-ttu-id="59cf6-352">Klicken Sie auf **Zurück** und **Fertig**, um den Arbeitsbereich zu beenden</span><span class="sxs-lookup"><span data-stu-id="59cf6-352">Click **Back** and then **Done** to exit the workspace</span></span>

10. <span data-ttu-id="59cf6-353">Klicken Sie auf **Arbeitsbereich veröffentlichen**, um die Arbeit zu speichern.</span><span class="sxs-lookup"><span data-stu-id="59cf6-353">Click **Publish workspace** to save your work</span></span>

#### <a name="adding-navigation-to-view-accounting-page"></a><span data-ttu-id="59cf6-354">Hinzufügen der Navigation zur Seite „Buchhaltung anzeigen“.</span><span class="sxs-lookup"><span data-stu-id="59cf6-354">Adding navigation to "View accounting" page</span></span>

<span data-ttu-id="59cf6-355">Die mobile Seite **Buchhaltung anzeigen** ist derzeit mit keiner mobilen Seiten verknüpft, die wir bisher entworfen haben.</span><span class="sxs-lookup"><span data-stu-id="59cf6-355">The **View accounting** mobile page isn’t currently linked to any of the mobile pages that we have designed so far.</span></span> <span data-ttu-id="59cf6-356">Da der Benutzer in der Lage sein soll, die Seite **Buchhaltung anzeigen** aus der **Rechnungsdetails** Seite im mobilen Gerät zu navigieren, müssen Sie zuvor aus der **Rechnungsdetails** Seite der **Buchhaltung anzeigen** Seite bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="59cf6-356">Because the user should be able to navigate to the **View accounting** page from the **Invoice details** page on the mobile device, we must provide navigation from the **Invoice details** page to the **View accounting** page.</span></span> <span data-ttu-id="59cf6-357">Wir legen die Navigationsverknüpfung ein, indem wir Zusatzlogik zu JavaScript verwenden.</span><span class="sxs-lookup"><span data-stu-id="59cf6-357">We establish this navigation by using additional logic via JavaScript.</span></span>

1.  <span data-ttu-id="59cf6-358">Öffnen Sie die JS-Datei, die Sie eben erstellt haben, und fügen Sie die Positionen hinzu, die im folgenden Code hervorgehoben werden.</span><span class="sxs-lookup"><span data-stu-id="59cf6-358">Open the .js file that you created earlier, and add the lines that are highlighted in the following code.</span></span> <span data-ttu-id="59cf6-359">Dieser Code mach zwei Dinge:</span><span class="sxs-lookup"><span data-stu-id="59cf6-359">This code does two things:</span></span>
    1.  <span data-ttu-id="59cf6-360">Er wird sichergestellt, dass Benutzer nicht direkt über der Arbeitsbereich **Buchhaltung anzeigen** Seite Navigation können.</span><span class="sxs-lookup"><span data-stu-id="59cf6-360">It helps guarantee that users can’t navigate directly from the workspace to the **View accounting** page.</span></span>
    2.  <span data-ttu-id="59cf6-361">Er wird ein Navigationssteuerelement der **Rechnungsdetails** Seite der **Buchhaltung anzeigen** Seite ein.</span><span class="sxs-lookup"><span data-stu-id="59cf6-361">It establishes a navigation control from the **Invoice details** page to the **View accounting** page.</span></span>

    > [!NOTE] 
    > <span data-ttu-id="59cf6-362">Die Namen der Seiten und andere Steuerelemente im Code müssen mit den Namen im Arbeitsbereich identisch sein.</span><span class="sxs-lookup"><span data-stu-id="59cf6-362">The name of the pages and other controls in the code must be the same as the names in the workspace.</span></span>

    ```javascript
    function main(metadataService, dataService, cacheService, $q) {
           return {
               appInit: function (appMetadata) {
                   // Hide controls that need to be present, but not visible
                   metadataService.configureControl('My-vendor-invoices', 'ShowAccept', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowApprove', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowReject', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowDelegate', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowRequestChange', { hidden: true });
                 metadataService.configureControl('My-vendor-invoices', 'ShowRecall', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowComplete', { hidden: true });
               metadataService.configureControl('My-vendor-invoices', 'ShowResubmit', { hidden: true });
                   // Hide pages not applicable for root navigation
                   metadataService.hideNavigation('View-accounting');
                   //Link to view accounting
                   metadataService.addLink('Invoice-details', 'View-accounting', 'View-accounting-nav-control', 'View accounting', true);
               },
               pageInit: function (pageMetadata, params) {
        if (pageMetadata.Name == 'Invoice-details') {
                       // Show/hide workflow actions based on workflow step
                       metadataService.configureAction('Accept', { visible: true });
                       metadataService.configureAction('Approve', { visible: true });
                       metadataService.configureAction('Reject', { visible: true });
                       metadataService.configureAction('Delegate', { visible: true });
                       metadataService.configureAction('Request-change', { visible: true });
                       metadataService.configureAction('Recall', { visible: true });
                       metadataService.configureAction('Complete', { visible: true });
                       metadataService.configureAction('Resubmit', { visible: true });

                       var entityContextParts = params.pageContext.split(':');
                       var data = dataService.getEntityData(entityContextParts[0], entityContextParts[1]);

                       var acceptControl = data.getPropertyValue('VendInvoiceInfoTable/showAccept');
                       var approveControl = data.getPropertyValue('VendInvoiceInfoTable/showApprove');
                       var rejectControl = data.getPropertyValue('VendInvoiceInfoTable/showReject');
                       var delegateControl = data.getPropertyValue('VendInvoiceInfoTable/showDelegate');
                       var requestChangeControl = data.getPropertyValue('VendInvoiceInfoTable/showRequestChange');
                       var recallControl = data.getPropertyValue('VendInvoiceInfoTable/showRecall');
                       var completeControl = data.getPropertyValue('VendInvoiceInfoTable/showComplete');
                       var resubmitControl = data.getPropertyValue('VendInvoiceInfoTable/showResubmit');

                       var showAcceptControl = Boolean(acceptControl == 1);
                       var showApproveControl = Boolean(approveControl == 1);
                     var showRejectControl = Boolean(rejectControl == 1);
                       var showDelegateControl = Boolean(delegateControl == 1);
                       var showRequestChangeControl = Boolean(requestChangeControl == 1);
                       var showRecallControl = Boolean(recallControl == 1);
                       var showCompleteControl = Boolean(completeControl == 1);
                       var showResubmitControl = Boolean(resubmitControl == 1);

                       metadataService.configureAction('Accept', { visible: showAcceptControl });
                       metadataService.configureAction('Approve', { visible: showApproveControl });
                       metadataService.configureAction('Reject', { visible: showRejectControl });
                       metadataService.configureAction('Delegate', { visible: showDelegateControl });
                       metadataService.configureAction('Request-change', { visible: showRequestChangeControl });
                       metadataService.configureAction('Recall', { visible: showRecallControl });
                       metadataService.configureAction('Complete', { visible: showCompleteControl });
                       metadataService.configureAction('Resubmit', { visible: showResubmitControl });
        }
                 },
           };
        }
    ```
    
2.  <span data-ttu-id="59cf6-363">Laden Sie die Codedatei dem Arbeitsbereich hohe, indem Sie die **Logik** Registerkarte zum Überschreiben des Codes auswählen</span><span class="sxs-lookup"><span data-stu-id="59cf6-363">Upload the code file to the workspace by selecting the **Logic** tab to overwrite the previous code</span></span>
3.  <span data-ttu-id="59cf6-364">Klicken Sie auf **Fertig**, um den Bearbeitungsmodus zu verlassen.</span><span class="sxs-lookup"><span data-stu-id="59cf6-364">Click **Done** to exit edit mode.</span></span>
4.  <span data-ttu-id="59cf6-365">Klicken Sie auf **Zurück** und **Fertig**, um den Arbeitsbereich zu beenden</span><span class="sxs-lookup"><span data-stu-id="59cf6-365">Click **Back** and then **Done** to exit the workspace</span></span>
5.  <span data-ttu-id="59cf6-366">Klicken Sie auf **Arbeitsbereich veröffentlichen**, um die Arbeit zu speichern.</span><span class="sxs-lookup"><span data-stu-id="59cf6-366">Click **Publish workspace** to save your work</span></span>

### <a name="validation"></a><span data-ttu-id="59cf6-367">Überprüfung</span><span class="sxs-lookup"><span data-stu-id="59cf6-367">Validation</span></span>

<span data-ttu-id="59cf6-368">Öffnen Sie auf Ihrem mobilen Gerät die App, und stellen Sie eine Verbindung mit Ihrer Instanz her.</span><span class="sxs-lookup"><span data-stu-id="59cf6-368">From your mobile device, open the app, and connect to your instance.</span></span> <span data-ttu-id="59cf6-369">Überprüfen Sie, ob Sie in das Unternehmen ein, in dem Kreditorenrechnungen Ihnen zur Prüfung zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="59cf6-369">Make sure that you sign in to the company where vendor invoices are assigned to you for review.</span></span> <span data-ttu-id="59cf6-370">Sie sollten in der Lage sein, die folgenden Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="59cf6-370">You should be able to perform the following actions:</span></span>

-   <span data-ttu-id="59cf6-371">Siehe den **Meine Genehmigungen** Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="59cf6-371">See the **My approvals** workspace.</span></span>
-   <span data-ttu-id="59cf6-372">Öffnen Sie den **Meine Genehmigungen** Arbeitsbereich und sehen Sie die **Meine Kreditorenrechnungen** Seite.</span><span class="sxs-lookup"><span data-stu-id="59cf6-372">Drill into the **My approvals** workspace and see the **My vendor invoices** page.</span></span>
-   <span data-ttu-id="59cf6-373">Öffnen Sie die **Meine Kreditorenrechnungen** Seite und erscheinen die Liste der Rechnungen, die Ihnen zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="59cf6-373">Drill into the **My vendor invoices** page and see the list of invoices that are assigned to you.</span></span>
-   <span data-ttu-id="59cf6-374">Öffnen Sie eine der Rechnungen und die Rechnungskopfdetails finden und -Positionsdetails.</span><span class="sxs-lookup"><span data-stu-id="59cf6-374">Drill into one of the invoices, and see the invoice header details and line details.</span></span>
-   <span data-ttu-id="59cf6-375">Auf der Detailseite finden Sie einen Link zu den Anlagen, und verwenden Sie diesen Link, die der Anhangliste zu navigieren und die Anhänge anzeigen.</span><span class="sxs-lookup"><span data-stu-id="59cf6-375">On the details page, see a link to attachments, and use this link to navigate to the attachments list and view the attachments.</span></span>
-   <span data-ttu-id="59cf6-376">Auf der Detailseite finden Sie einen Link zur Seite **Buchhaltung anzeigen** und verwenden Sie diesen Link, um zur Verteilungsseite zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="59cf6-376">On the details page, see a link to the **View accounting** page, and use this link to navigate to the distributions page and view the distributions.</span></span>
-   <span data-ttu-id="59cf6-377">Auf der Detailseite klicken Sie auf das Menü **Aktivitäten** unten, und lassen Workflowaktivitäten aus, die z Workflowschritt gültig sind.</span><span class="sxs-lookup"><span data-stu-id="59cf6-377">On the details page, click the **Actions** menu at the bottom, and perform workflow actions that are applicable to the workflow step.</span></span>

## <a name="designing-a-complex-invoice-approval-scenario-for-fabrikam"></a><span data-ttu-id="59cf6-378">Entwerfen eines komplexen Rechnungsgenehmigungsszenarios für Fabrikam</span><span class="sxs-lookup"><span data-stu-id="59cf6-378">Designing a complex invoice approval scenario for Fabrikam</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="59cf6-379">Szenarioattribut</span><span class="sxs-lookup"><span data-stu-id="59cf6-379">Scenario attribute</span></span></th>
<th><span data-ttu-id="59cf6-380">Antwort</span><span class="sxs-lookup"><span data-stu-id="59cf6-380">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="59cf6-381">Welche Felder aus dem Rechnungskopf wünschen die Benutzer in mobilen Umgebungen und in welcher Reihenfolge?</span><span class="sxs-lookup"><span data-stu-id="59cf6-381">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="59cf6-382">Kreditorenname</span><span class="sxs-lookup"><span data-stu-id="59cf6-382">Vendor name</span></span></li>
<li><span data-ttu-id="59cf6-383">Rechnungsbetrag</span><span class="sxs-lookup"><span data-stu-id="59cf6-383">Invoice amount</span></span></li>
<li><span data-ttu-id="59cf6-384">Rechnungskonto</span><span class="sxs-lookup"><span data-stu-id="59cf6-384">Invoice account</span></span></li>
<li><span data-ttu-id="59cf6-385">Rechnungsnummer</span><span class="sxs-lookup"><span data-stu-id="59cf6-385">Invoice number</span></span></li>
<li><span data-ttu-id="59cf6-386">Rechnungsdatum</span><span class="sxs-lookup"><span data-stu-id="59cf6-386">Invoice date</span></span></li>
<li><span data-ttu-id="59cf6-387">Rechnungsbeschreibung</span><span class="sxs-lookup"><span data-stu-id="59cf6-387">Invoice description</span></span></li>
<li><span data-ttu-id="59cf6-388">Fälligkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="59cf6-388">Due date</span></span></li>
<li><span data-ttu-id="59cf6-389">Rechnungswährung</span><span class="sxs-lookup"><span data-stu-id="59cf6-389">Invoice currency</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="59cf6-390">Welche Felder aus den Rechnungsposition wünschen die Benutzer in mobilen Umgebungen und in welcher Reihenfolge?</span><span class="sxs-lookup"><span data-stu-id="59cf6-390">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="59cf6-391">Beschaffungskategorie</span><span class="sxs-lookup"><span data-stu-id="59cf6-391">Procurement category</span></span></li>
<li><span data-ttu-id="59cf6-392">Leistung</span><span class="sxs-lookup"><span data-stu-id="59cf6-392">Quantity</span></span></li>
<li><span data-ttu-id="59cf6-393">Preis je Einheit</span><span class="sxs-lookup"><span data-stu-id="59cf6-393">Unit price</span></span></li>
<li><span data-ttu-id="59cf6-394">Nettobetrag der Position</span><span class="sxs-lookup"><span data-stu-id="59cf6-394">Line net amount</span></span></li>
<li><span data-ttu-id="59cf6-395">Steuerbetrag (US 1099)</span><span class="sxs-lookup"><span data-stu-id="59cf6-395">1099 amount</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="59cf6-396">Wie viele Rechnungspositionen gibt es in einer Rechnung?</span><span class="sxs-lookup"><span data-stu-id="59cf6-396">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="59cf6-397">Wenden Sie die 80-20-Regel hier an, und optimieren Sie für 80 Prozent.</span><span class="sxs-lookup"><span data-stu-id="59cf6-397">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span></td>
<td><span data-ttu-id="59cf6-398">5</span><span class="sxs-lookup"><span data-stu-id="59cf6-398">5</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="59cf6-399">Möchten Benutzer Buchhaltungsverteilungen (Rechnungscodierung) auf dem mobilen Gerät sehen?</span><span class="sxs-lookup"><span data-stu-id="59cf6-399">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span></td>
<td><span data-ttu-id="59cf6-400">Ja</span><span class="sxs-lookup"><span data-stu-id="59cf6-400">Yes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="59cf6-401">Wie viele Buchhaltungsverteilungen (erweiterte Preis, Mehrwertsteuer, Belastungen, usw.) gibt es für eine Rechnungsposition?</span><span class="sxs-lookup"><span data-stu-id="59cf6-401">How many accounting distributions (extended price, sales tax, charges, and so on) are there for an invoice line?</span></span> <span data-ttu-id="59cf6-402">Wieder gilt die Regel 80-20.</span><span class="sxs-lookup"><span data-stu-id="59cf6-402">Again, apply the 80-20 rule.</span></span></td>
<td><span data-ttu-id="59cf6-403">Erweiterter Preis: 2 Mehrwertsteuer: 2 Zuschläge: 2</span><span class="sxs-lookup"><span data-stu-id="59cf6-403">Extended price: 2 Sales tax: 2 Charges: 2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="59cf6-404">Haben Rechnungen auch Buchhaltungsverteilungen im Rechnungskopf?</span><span class="sxs-lookup"><span data-stu-id="59cf6-404">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="59cf6-405">Falls ja sollen diese Buchhaltungsverteilungen im Gerät verfügbar sein?</span><span class="sxs-lookup"><span data-stu-id="59cf6-405">If so, should these accounting distributions be available on the device?</span></span></td>
<td><span data-ttu-id="59cf6-406">Nicht verwendet</span><span class="sxs-lookup"><span data-stu-id="59cf6-406">Not used</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="59cf6-407">Möchten Benutzer Anhänge für die Rechnung auf dem Gerät angezeigt?</span><span class="sxs-lookup"><span data-stu-id="59cf6-407">Will users want to see attachments for the invoice on the device?</span></span></td>
<td><span data-ttu-id="59cf6-408">Ja</span><span class="sxs-lookup"><span data-stu-id="59cf6-408">Yes</span></span></td>
</tr>
</tbody>
</table>

### <a name="next-steps"></a><span data-ttu-id="59cf6-409">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="59cf6-409">Next steps</span></span>

<span data-ttu-id="59cf6-410">Die folgenden Abweichungen für Szenario 1, basierend auf den Anforderungen für Szenario 2.</span><span class="sxs-lookup"><span data-stu-id="59cf6-410">The following variations can be done for scenario 1, based on the requirements for scenario 2.</span></span> <span data-ttu-id="59cf6-411">Sie können in diesem Bereich verwenden, um Ihre Erfahrung mit der mobilen App zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="59cf6-411">You can use this section to improve your mobile app experience.</span></span>

1.  <span data-ttu-id="59cf6-412">Da weitere Rechnungspositionen in Szenario 2 erwartet werden, können folgende Änderungen zum Entwurf, die Benutzererfahrung im mobilen Gerät zu optimieren:</span><span class="sxs-lookup"><span data-stu-id="59cf6-412">Because more invoice lines are expected in scenario 2, the following changes to the design will help optimize the user experience on the mobile device:</span></span>
    1.  <span data-ttu-id="59cf6-413">Anstelle der Betrachtungsrechnungspositionen auf Detailseite der (z.B. in Szenario 1), Benutzer festlegen, dass Positionen einer separaten mobilen Seite anzeigen.</span><span class="sxs-lookup"><span data-stu-id="59cf6-413">Instead of viewing invoice lines on the details page (as in scenario 1), users can choose to view lines on a separate mobile page.</span></span>
    2.  <span data-ttu-id="59cf6-414">Da mehrere Rechnungsposition in diesem Szenario erwartet wird, wenn die **VendMobileInvoiceAllDistributionTree** Seite verwendet wird, um die Verteilungsseite für Datenschutzerklärung zu entwerfen (wie in Szenario 1), kann es verwirrend, damit der Benutzer Positionen mit Verteilungen aufeinander umfasst.</span><span class="sxs-lookup"><span data-stu-id="59cf6-414">Because more than one invoice line is expected in this scenario, if the **VendMobileInvoiceAllDistributionTree** page is used to design the distributions page for mobile (as in scenario 1), it might be confusing for the user to correlate lines to distributions.</span></span> <span data-ttu-id="59cf6-415">Daher verwenden Sie die **VendMobileInvoiceLineDistributionTree** Seite, um die Verteilungsseite zu entwerfen.</span><span class="sxs-lookup"><span data-stu-id="59cf6-415">Therefore, use the **VendMobileInvoiceLineDistributionTree** page to design the distributions page.</span></span>
    3.  <span data-ttu-id="59cf6-416">Im Idealfall sollten die Verteilungen im Kontext einer Rechnungsposition in diesem Szenario angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="59cf6-416">Ideally, the distributions should be shown in the context of an invoice line in this scenario.</span></span> <span data-ttu-id="59cf6-417">Daher müssen Sie unbedingt, ob der Benutzer in einer Position richten bohren kann, um die Verteilungsseite anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="59cf6-417">Therefore, make sure that the user can drill into a line to see the distributions page.</span></span> <span data-ttu-id="59cf6-418">Verwenden Sie die Seitenlinkfunktion, den Drillthrough einzurichten, wie Sie für den Kopf und die Detailseiten in Szenario 1. ".</span><span class="sxs-lookup"><span data-stu-id="59cf6-418">Use the page link capability to establish the drill-through, just as you did for the header and details pages in scenario 1.</span></span>

2.  <span data-ttu-id="59cf6-419">Da mehrere ein Betragsart für die Verteilungen in Szenario 2 (Mehrwertsteuer, Belastungen usw.) erwartet wird, ist es hilfreich, die Beschreibung des Betrags Typ anzeigen.</span><span class="sxs-lookup"><span data-stu-id="59cf6-419">Because more than one amount type is expected on the distributions in scenario 2 (sales tax, charges, and so on), it will be useful to show the description of the amount type.</span></span> <span data-ttu-id="59cf6-420">(Wir haben diese Informationen in Szenario 1 ausgelassen.)</span><span class="sxs-lookup"><span data-stu-id="59cf6-420">(We omitted this information in scenario 1.)</span></span>




