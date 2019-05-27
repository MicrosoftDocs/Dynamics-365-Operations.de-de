---
title: Mobile Rechnungsgenehmigungen
description: Dieses Thema soll einen praktischen Ansatz zum Entwerfen von mobilen Szenarien in Dynamics 365 for Finance and Operations bereitstellen, indem es mobile Kreditorenrechnungsgenehmigungen als Anwendungsfall zeigt.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 5a48ea7b0c1faf5726de21a246e3d8b4d98f166a
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1511659"
---
# <a name="mobile-invoice-approvals"></a><span data-ttu-id="360c1-103">Mobile Rechnungsgenehmigungen</span><span class="sxs-lookup"><span data-stu-id="360c1-103">Mobile invoice approvals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="360c1-104">Mithilfe der mobilen Funktionen in Microsoft Dynamics 365 for Finance and Operations können Geschäftsbenutzer mobile Erfahrungen entwerfen.</span><span class="sxs-lookup"><span data-stu-id="360c1-104">Mobile capabilities in Microsoft Dynamics 365 for Finance and Operations let a business user design mobile experiences.</span></span> <span data-ttu-id="360c1-105">Bei erweiterten Szenarien ermöglicht die Plattform auch Entwickler die Funktionen zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="360c1-105">For advanced scenarios, the platform also lets developers extend the capabilities as they desire.</span></span> <span data-ttu-id="360c1-106">Die effektivste Möglichkeit, einige der neuen mobilen Konzepten kennenzulernen, ist, den Prozess des Entwurfs einiger Szenarios durchzulaufen.</span><span class="sxs-lookup"><span data-stu-id="360c1-106">The most effective way to learn some of the new concepts on mobile is to go through the process of designing a few scenarios.</span></span> <span data-ttu-id="360c1-107">Dieses Thema soll einen praktischen Ansatz zum Entwerfen von mobilen Szenarien bereitstellen, indem es mobile Kreditorenrechnungsgenehmigungen als Anwendungsfall zeigt.</span><span class="sxs-lookup"><span data-stu-id="360c1-107">This topic is intended to provide a practical approach to designing mobile scenarios by taking vendor invoice approvals for mobile as a use case.</span></span> <span data-ttu-id="360c1-108">Dieses Thema soll helfen, andere der Szenarien zu entwerfen und kann auch auf anderen Szenarios angewendet werden, die nicht den Kreditorenrechnungen zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="360c1-108">This topic should help you design other variations of the scenarios and can also be applied to other scenarios that aren’t related to vendor invoices.</span></span>

<a name="prerequisites"></a><span data-ttu-id="360c1-109">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="360c1-109">Prerequisites</span></span>
-------------

| <span data-ttu-id="360c1-110">Voraussetzung</span><span class="sxs-lookup"><span data-stu-id="360c1-110">Prerequisite</span></span>                                                                                            | <span data-ttu-id="360c1-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="360c1-111">Description</span></span>                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="360c1-112">Vorbereitung</span><span class="sxs-lookup"><span data-stu-id="360c1-112">Mobile handbook pre-read</span></span>                                                                                |[<span data-ttu-id="360c1-113">Mobile Plattform</span><span class="sxs-lookup"><span data-stu-id="360c1-113">Mobile platform</span></span>](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md)                                                                                                  |
| <span data-ttu-id="360c1-114">Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="360c1-114">Dynamics 365 for Finance and Operations</span></span>                                                                             | <span data-ttu-id="360c1-115">Eine Umgebung mit Microsoft Dynamics 365 for Operations Version 1611 und Microsoft Dynamics for Operations-Plattform – Update 3 (November 2016)</span><span class="sxs-lookup"><span data-stu-id="360c1-115">An environment that has Microsoft Dynamics 365 for Operations version 1611 and Microsoft Dynamics for Operations platform update 3 (November 2016)</span></span>                   |
| <span data-ttu-id="360c1-116">Hotfix KB 3204341 installieren.</span><span class="sxs-lookup"><span data-stu-id="360c1-116">Install hotfix KB 3204341.</span></span>                                                                              | <span data-ttu-id="360c1-117">Die Aufgabenaufzeichnung kann fälschlicherweise zwei Scließen-Befehle für Dropdowndialogfelder erfassen, die in Dynamics 365 for Operation Update 3 (November 2016) einbezogen sind.</span><span class="sxs-lookup"><span data-stu-id="360c1-117">Task recorder can erroneously record two Close commands for dropdown dialogs this is included in Dynamics 365 for Operation platform update 3 (November 2016 update)</span></span> |
| <span data-ttu-id="360c1-118">Hotfix KB 3207800 installieren.</span><span class="sxs-lookup"><span data-stu-id="360c1-118">Install hotfix KB 3207800.</span></span>                                                                              | <span data-ttu-id="360c1-119">Dieser Hotfix ermöglicht das Anzeigen von Anhängen im mobilen Client, der in Dynamics 365 for Operation Update 3 (November 2016) enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="360c1-119">This hotfix enables attachments to be viewed on the mobile client this is included in Dynamics 365 for Operation platform update 3 (November 2016 update).</span></span>           |
| <span data-ttu-id="360c1-120">Hotfix KB 3208224 installieren.</span><span class="sxs-lookup"><span data-stu-id="360c1-120">Install hotfix KB 3208224.</span></span>                                                                              | <span data-ttu-id="360c1-121">Anwendungscode für die mobile Kreditorenrechnungs-Genehmigungsanwendung ist in der Microsoft Dynamics AX-Anwendung 7.0.1 (Mai 2016) enthalten.</span><span class="sxs-lookup"><span data-stu-id="360c1-121">Application code for the mobile vendor invoice approval application this is included in Microsoft Dynamics AX application 7.0.1 (May 2016).</span></span>                          |
| <span data-ttu-id="360c1-122">Ein Android- oder iOS- oder Windows-Gerät, auf dem die mobile App für Finance and Operations installiert wurde</span><span class="sxs-lookup"><span data-stu-id="360c1-122">An Android or iOS or a Windows device that has the mobile app installed for Finance and Operations</span></span> | <span data-ttu-id="360c1-123">Suchen Sie die App im entsprechenden App-Store.</span><span class="sxs-lookup"><span data-stu-id="360c1-123">Search for the app in the appropriate app store.</span></span>                                                                                                                     |

## <a name="introduction"></a><span data-ttu-id="360c1-124">Einführung</span><span class="sxs-lookup"><span data-stu-id="360c1-124">Introduction</span></span>
<span data-ttu-id="360c1-125">Mobile Genehmigungen für Kreditorenrechnungen erfordern die drei Hotfixes, die im Abschnitt "Vorbereitung" angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="360c1-125">Mobile approvals for vendor invoices require the three hotfixes that are mentioned in the “Prerequisites” section.</span></span> <span data-ttu-id="360c1-126">Diese Hotfixes bieten keinen Arbeitsbereich für die Rechnungsgenehmigungen.</span><span class="sxs-lookup"><span data-stu-id="360c1-126">These hotfixes don’t provide a workspace for the invoice approvals.</span></span> <span data-ttu-id="360c1-127">Um zu lernen, was ein Arbeitsbereich im Rahmen des mobilen Clients ist, lesen Sie das Handbuch aus dem Abschnitt "Vorbereitung".</span><span class="sxs-lookup"><span data-stu-id="360c1-127">To learn what a workspace is in the context of mobile, read the mobile handbook that is mentioned in the “Prerequisites” section.</span></span> <span data-ttu-id="360c1-128">Der Rechnungsgenehmigungsarbeitsbereich muss konzipiert werden.</span><span class="sxs-lookup"><span data-stu-id="360c1-128">The invoice approvals workspace must be designed.</span></span> 

<span data-ttu-id="360c1-129">Jede Organisation definiert und nutzt eigene Geschäftsprozesse für Kreditorenrechnungen.</span><span class="sxs-lookup"><span data-stu-id="360c1-129">Every organization orchestrates and defines its business process for vendor invoices differently.</span></span> <span data-ttu-id="360c1-130">Bevor Sie eine mobile Erfahrung für Kreditorenrechnungsgenehmigungen entwerfen, müssen Sie die folgenden Aspekte des Geschäftsprozesses berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="360c1-130">Before you design a mobile experience for vendor invoice approvals, you should consider the following aspects of the business process.</span></span> <span data-ttu-id="360c1-131">Der Grundgedanke ist, diese Datenpunkten so weit wie möglich zu verwenden, um die Benutzerfreundlichkeit für das Gerät zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="360c1-131">The idea is to use these data points as much as possible to optimize the user experience on the device.</span></span>

-   <span data-ttu-id="360c1-132">Welche Felder aus dem Rechnungskopf wünschen die Benutzer in mobilen Umgebungen und in welcher Reihenfolge?</span><span class="sxs-lookup"><span data-stu-id="360c1-132">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span>
-   <span data-ttu-id="360c1-133">Welche Felder aus den Rechnungsposition wünschen die Benutzer in mobilen Umgebungen und in welcher Reihenfolge?</span><span class="sxs-lookup"><span data-stu-id="360c1-133">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span>
-   <span data-ttu-id="360c1-134">Wie viele Rechnungspositionen gibt es in einer Rechnung?</span><span class="sxs-lookup"><span data-stu-id="360c1-134">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="360c1-135">Wenden Sie die 80-20-Regel hier an, und optimieren Sie für 80 Prozent.</span><span class="sxs-lookup"><span data-stu-id="360c1-135">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span>
-   <span data-ttu-id="360c1-136">Möchten Benutzer Buchhaltungsverteilungen (Rechnungscodierung) auf dem mobilen Gerät sehen?</span><span class="sxs-lookup"><span data-stu-id="360c1-136">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span> <span data-ttu-id="360c1-137">Wenn die Antwort zu dieser Frage ja ist, beachten Sie die folgenden Fragen:</span><span class="sxs-lookup"><span data-stu-id="360c1-137">If the answer to this question is yes, consider the following questions:</span></span>
    -   <span data-ttu-id="360c1-138">Wie viele Buchhaltungsverteilungen (erweiterte Preis, Mehrwertsteuer, Belastungen, Teilungen, usw.) gibt es für eine Rechnungsposition?</span><span class="sxs-lookup"><span data-stu-id="360c1-138">How many accounting distributions (extended price, sales tax, charges, splits, and so on) are there for an invoice line?</span></span> <span data-ttu-id="360c1-139">Wieder gilt die Regel 80-20.</span><span class="sxs-lookup"><span data-stu-id="360c1-139">Again, apply the 80-20 rule.</span></span>
    -   <span data-ttu-id="360c1-140">Haben Rechnungen auch Buchhaltungsverteilungen im Rechnungskopf?</span><span class="sxs-lookup"><span data-stu-id="360c1-140">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="360c1-141">Falls ja sollen diese Buchhaltungsverteilungen im Gerät verfügbar sein?</span><span class="sxs-lookup"><span data-stu-id="360c1-141">If so, should these accounting distributions be available on the device?</span></span>

> [!NOTE]
> <span data-ttu-id="360c1-142">In diesem Thema wird nicht erläutert, wie Sie Buchhaltungsverteilungen bearbeitet, da diese Funktion nicht aktuell für mobile Szenarios unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="360c1-142">This topic doesn’t explain how to edit accounting distributions, because this functionality isn’t currently supported for mobile scenarios.</span></span>

-   <span data-ttu-id="360c1-143">Möchten Benutzer Anhänge für die Rechnung auf dem Gerät angezeigt?</span><span class="sxs-lookup"><span data-stu-id="360c1-143">Will users want to see attachments for the invoice on the device?</span></span>

<span data-ttu-id="360c1-144">Das Design der mobilen Erfahrung für Rechnungsgenehmigungen variiert, abhängig von den Antworten auf diese Fragen.</span><span class="sxs-lookup"><span data-stu-id="360c1-144">The design of the mobile experience for invoice approvals will differ, depending on the answers to these questions.</span></span> <span data-ttu-id="360c1-145">Die Zielsetzung ist, die Benutzerfreundlichkeit für den Geschäftsprozess auf Mobilgeräten in einer Organisation zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="360c1-145">The objective is to optimize the user experience for the business process on mobile in an organization.</span></span> <span data-ttu-id="360c1-146">Im Rest des Themas betrachten wir zwei Szenariovarianten die auf Grundlage unterschiedlicher Antworten auf Fragen vorhergehenden sind.</span><span class="sxs-lookup"><span data-stu-id="360c1-146">In the rest of this topic, we will look at two scenario variations that are based on different answers to the preceding questions.</span></span> 

<span data-ttu-id="360c1-147">Allgemeine, wenn mit dem mobilen Designer gearbeitet wird, vergewissern Sie sich, diese Änderungen veröffentlicht werden, um zu verhindern Aktualisierungen zu verlieren.</span><span class="sxs-lookup"><span data-stu-id="360c1-147">As a general guidance, when working with the mobile designer, make sure to 'publish' the changes to prevent losing the updates.</span></span>

## <a name="designing-a-simple-invoice-approval-scenario-for-contoso"></a><span data-ttu-id="360c1-148">Entwerfen eines einfachen Rechnungsgenehmigungsszenarios für Contoso</span><span class="sxs-lookup"><span data-stu-id="360c1-148">Designing a simple invoice approval scenario for Contoso</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="360c1-149">Szenarioattribut</span><span class="sxs-lookup"><span data-stu-id="360c1-149">Scenario attribute</span></span></th>
<th><span data-ttu-id="360c1-150">Antwort</span><span class="sxs-lookup"><span data-stu-id="360c1-150">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="360c1-151">Welche Felder aus dem Rechnungskopf wünschen die Benutzer in mobilen Umgebungen und in welcher Reihenfolge?</span><span class="sxs-lookup"><span data-stu-id="360c1-151">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="360c1-152">Kreditorenname</span><span class="sxs-lookup"><span data-stu-id="360c1-152">Vendor name</span></span></li>
<li><span data-ttu-id="360c1-153">Rechnungssumme</span><span class="sxs-lookup"><span data-stu-id="360c1-153">Invoice total</span></span></li>
<li><span data-ttu-id="360c1-154">Rechnungskonto</span><span class="sxs-lookup"><span data-stu-id="360c1-154">Invoice account</span></span></li>
<li><span data-ttu-id="360c1-155">Rechnungsnummer</span><span class="sxs-lookup"><span data-stu-id="360c1-155">Invoice number</span></span></li>
<li><span data-ttu-id="360c1-156">Rechnungsdatum</span><span class="sxs-lookup"><span data-stu-id="360c1-156">Invoice date</span></span></li>
<li><span data-ttu-id="360c1-157">Rechnungsbeschreibung</span><span class="sxs-lookup"><span data-stu-id="360c1-157">Invoice description</span></span></li>
<li><span data-ttu-id="360c1-158">Fälligkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="360c1-158">Due date</span></span></li>
<li><span data-ttu-id="360c1-159">Rechnungswährung</span><span class="sxs-lookup"><span data-stu-id="360c1-159">Invoice currency</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="360c1-160">Welche Felder aus den Rechnungsposition wünschen die Benutzer in mobilen Umgebungen und in welcher Reihenfolge?</span><span class="sxs-lookup"><span data-stu-id="360c1-160">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="360c1-161">Beschaffungskategorie</span><span class="sxs-lookup"><span data-stu-id="360c1-161">Procurement category</span></span></li>
<li><span data-ttu-id="360c1-162">Leistung</span><span class="sxs-lookup"><span data-stu-id="360c1-162">Quantity</span></span></li>
<li><span data-ttu-id="360c1-163">Preis je Einheit</span><span class="sxs-lookup"><span data-stu-id="360c1-163">Unit price</span></span></li>
<li><span data-ttu-id="360c1-164">Nettobetrag der Position</span><span class="sxs-lookup"><span data-stu-id="360c1-164">Line net amount</span></span></li>
<li><span data-ttu-id="360c1-165">Steuerbetrag (US 1099)</span><span class="sxs-lookup"><span data-stu-id="360c1-165">1099 amount</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="360c1-166">Wie viele Rechnungspositionen gibt es in einer Rechnung?</span><span class="sxs-lookup"><span data-stu-id="360c1-166">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="360c1-167">Wenden Sie die 80-20-Regel hier an, und optimieren Sie für 80 Prozent.</span><span class="sxs-lookup"><span data-stu-id="360c1-167">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span></td>
<td><span data-ttu-id="360c1-168">1</span><span class="sxs-lookup"><span data-stu-id="360c1-168">1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="360c1-169">Möchten Benutzer Buchhaltungsverteilungen (Rechnungscodierung) auf dem mobilen Gerät sehen?</span><span class="sxs-lookup"><span data-stu-id="360c1-169">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span></td>
<td><span data-ttu-id="360c1-170">Ja</span><span class="sxs-lookup"><span data-stu-id="360c1-170">Yes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="360c1-171">Wie viele Buchhaltungsverteilungen (erweiterte Preis, Mehrwertsteuer, Belastungen, usw.) gibt es für eine Rechnungsposition?</span><span class="sxs-lookup"><span data-stu-id="360c1-171">How many accounting distributions (extended price, sales tax, charges, and so on) are there for an invoice line?</span></span> <span data-ttu-id="360c1-172">Wieder gilt die Regel 80-20.</span><span class="sxs-lookup"><span data-stu-id="360c1-172">Again, apply the 80-20 rule.</span></span></td>
<td><span data-ttu-id="360c1-173">Erweiterter Preis: 2 Mehrwertsteuer: 0 Zuschläge: 0</span><span class="sxs-lookup"><span data-stu-id="360c1-173">Extended price: 2 Sales tax: 0 Charges: 0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="360c1-174">Haben Rechnungen auch Buchhaltungsverteilungen im Rechnungskopf?</span><span class="sxs-lookup"><span data-stu-id="360c1-174">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="360c1-175">Falls ja sollen diese Buchhaltungsverteilungen im Gerät verfügbar sein?</span><span class="sxs-lookup"><span data-stu-id="360c1-175">If so, should these accounting distributions be available on the device?</span></span></td>
<td><span data-ttu-id="360c1-176">Nicht verwendet</span><span class="sxs-lookup"><span data-stu-id="360c1-176">Not used</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="360c1-177">Möchten Benutzer Anhänge für die Rechnung auf dem Gerät angezeigt?</span><span class="sxs-lookup"><span data-stu-id="360c1-177">Will users want to see attachments for the invoice on the device?</span></span></td>
<td><span data-ttu-id="360c1-178">Ja</span><span class="sxs-lookup"><span data-stu-id="360c1-178">Yes</span></span></td>
</tr>
</tbody>
</table>

### <a name="create-the-workspace"></a><span data-ttu-id="360c1-179">Arbeitsbereich erstellen</span><span class="sxs-lookup"><span data-stu-id="360c1-179">Create the workspace</span></span>

1.  <span data-ttu-id="360c1-180">Öffnen Sie Finance and Operations in einem Browser, und melden sich an.</span><span class="sxs-lookup"><span data-stu-id="360c1-180">In a browser, open Finance and Operations, and sign in.</span></span>
2.  <span data-ttu-id="360c1-181">Nachdem Sie angemeldet sind, hängen Sie **&mode=mobile** an die URL wie im folgenden Beispiel an und aktualisieren die Seite: https://&lt;yoururl&gt;/?cmp=usmf&mi=DefaultDashboard **&mode=mobile**</span><span class="sxs-lookup"><span data-stu-id="360c1-181">After you’ve signed in, append **&mode=mobile** to the URL as shown in the following example, and refresh the page: https://&lt;yoururl&gt;/?cmp=usmf&mi=DefaultDashboard **&mode=mobile**</span></span>
3.  <span data-ttu-id="360c1-182">Klicken Sie auf **Einstellungen** (Zahnrad) in der oberen rechten Ecke der Seite und klicken dann auf **Mobile App**.</span><span class="sxs-lookup"><span data-stu-id="360c1-182">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**.</span></span> <span data-ttu-id="360c1-183">Der Designer für mobile Apps wird wie die Aufgabenaufzeichnung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="360c1-183">The mobile app designer must show up just as Task recorder shows up.</span></span>
4.  <span data-ttu-id="360c1-184">Klicken Sie auf **Hinzufügen** um einen neuen Arbeitsbereich zu erstellen</span><span class="sxs-lookup"><span data-stu-id="360c1-184">Click **Add** to create a new workspace.</span></span> <span data-ttu-id="360c1-185">Im vorliegenden Beispiel ist Name des Arbeitsbereichs **Meine Genehmigungen**.</span><span class="sxs-lookup"><span data-stu-id="360c1-185">For this example, name the workspace **My approvals**.</span></span>
5.  <span data-ttu-id="360c1-186">Geben Sie eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="360c1-186">Enter a description.</span></span>
6.  <span data-ttu-id="360c1-187">Arbeitsbereichsfarbe auswählen.</span><span class="sxs-lookup"><span data-stu-id="360c1-187">Select a workspace color.</span></span> <span data-ttu-id="360c1-188">Die Arbeitsbereichfarbe wird für den Gesamtstil der mobilen Erfahrung für den Arbeitsbereich verwendet.</span><span class="sxs-lookup"><span data-stu-id="360c1-188">The workspace color will be used for the overall style of the mobile experience for this workspace.</span></span>
7.  <span data-ttu-id="360c1-189">Wählen Sie ein Symbol für den Arbeitsbereich aus.</span><span class="sxs-lookup"><span data-stu-id="360c1-189">Select an icon for the workspace.</span></span>
8.  <span data-ttu-id="360c1-190">Klicken Sie auf **Fertig.**</span><span class="sxs-lookup"><span data-stu-id="360c1-190">Click **Done**</span></span>
9.  <span data-ttu-id="360c1-191">Klicken Sie auf **Arbeitsbereich veröffentlichen**, um die Änderungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="360c1-191">Click **Publish workspace** to save the changes</span></span>

### <a name="vendor-invoices-assigned-to-me"></a><span data-ttu-id="360c1-192">Mir zugewiesene Kreditorenrechnungen</span><span class="sxs-lookup"><span data-stu-id="360c1-192">Vendor invoices assigned to me</span></span>

<span data-ttu-id="360c1-193">Die erste mobile Seite soll die Liste der Rechnungen, die dem Benutzer zur Genehmigung zugewiesen werden zeigen.</span><span class="sxs-lookup"><span data-stu-id="360c1-193">The first mobile page that you should design is the list of invoices that are assigned to the user for review.</span></span> <span data-ttu-id="360c1-194">Um diese mobile Seite zu entwerfen verwenden Sie die **VendMobileInvoiceAssignedToMeListPage**-Seite in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="360c1-194">To design this mobile page, use the **VendMobileInvoiceAssignedToMeListPage** page in Finance and Operations.</span></span> <span data-ttu-id="360c1-195">Bevor Sie dieses Verfahren ausführen, stellen Sie sicher, dass mindestens eine Kreditorenrechnung zur Prüfung Ihnen zugewiesen ist und die Rechnungsposition zwei Verteilungen hat.</span><span class="sxs-lookup"><span data-stu-id="360c1-195">Before you complete this procedure, make sure that at least one vendor invoice is assigned to you for review, and that the invoice line has two distributions.</span></span> <span data-ttu-id="360c1-196">Diese Einstellung erfüllt die Bedingungen für dieses Szenarios.</span><span class="sxs-lookup"><span data-stu-id="360c1-196">This setup meets the requirements for this scenario.</span></span>

1.  <span data-ttu-id="360c1-197">In der Finance and Operations-URL ersetzen Sie den Namen der Menüoption durch **VendMobileInvoiceAssignedToMeListPage**, um die mobile Version der Listenseite **Ausstehende Kreditorenrechnungen – mir zugewiesen** im **Kreditor**-Modul zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="360c1-197">In the Finance and Operations URL, replace the name of the menu item with **VendMobileInvoiceAssignedToMeListPage** to open the mobile version of the **Pending vendor invoices assigned to me** list page in the **Accounts payable** module.</span></span> <span data-ttu-id="360c1-198">Je nach der Anzahl von Rechnungen, die Sie in Ihrem System besitzen, das Ihnen zugeordnet ist, wird auf dieser Seite die Rechnungen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="360c1-198">Depending on the number of invoices that you have in your system assigned to you, this page will show those invoices.</span></span> <span data-ttu-id="360c1-199">Sie können den Filter links verwenden um eine bestimmte Rechnung zu suchen.</span><span class="sxs-lookup"><span data-stu-id="360c1-199">To find a specific invoice, you can use the filter on the left.</span></span> <span data-ttu-id="360c1-200">Allerdings benötigen wir keine bestimmte Rechnung für dieses Beispiel.</span><span class="sxs-lookup"><span data-stu-id="360c1-200">However, we don’t require a specific invoice for this example.</span></span> <span data-ttu-id="360c1-201">Es benötigen nur eine Rechnung, die Ihnen zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="360c1-201">We just require some invoice assigned to you which is going to allow you to design the mobile page.</span></span> <span data-ttu-id="360c1-202">Die neuen Seiten, die verfügbar sind, wurden insbesondere zum Entwickeln von mobilen Szenarien für Kreditorenrechnung entworfen.</span><span class="sxs-lookup"><span data-stu-id="360c1-202">The new pages that are available have been designed specifically for developing mobile scenarios for vendor invoice.</span></span> <span data-ttu-id="360c1-203">Daher müssen Sie diesen Seiten nutzen.</span><span class="sxs-lookup"><span data-stu-id="360c1-203">Therefore, you must use these pages.</span></span> <span data-ttu-id="360c1-204">Die URL muss der folgenden URL ähneln. Nachdem Sie sie eingeben haben, muss die Seite, die in der Abbildung dargestellt wird, angezeigt werden: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile [![Zu meiner Seite zugewiesene ausstehende Kreditorenrechnungen](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)</span><span class="sxs-lookup"><span data-stu-id="360c1-204">The URL should resemble the following URL, and after you enter it, the page that is shown in the illustration must appear: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile [![Pending vendor invoices assigned to me page](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)</span></span>
2.  <span data-ttu-id="360c1-205">Klicken Sie auf **Einstellungen** (Zahnrad) in der oberen rechten Ecke der Seite und klicken dann auf **Mobile App**.</span><span class="sxs-lookup"><span data-stu-id="360c1-205">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**</span></span>
3.  <span data-ttu-id="360c1-206">Wählen Sie einen und Arbeitsbereich aus und klicken sie **Bearbeiten**</span><span class="sxs-lookup"><span data-stu-id="360c1-206">Select your workspace and click **Edit**</span></span>
4.  <span data-ttu-id="360c1-207">Klicken Sie auf **Seite hinzufügen**, um die ersten mobilen Seite zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="360c1-207">Click **Add page** to create the first mobile page.</span></span>
5.  <span data-ttu-id="360c1-208">Geben Sie einen Namen ein, z.B. meine **Meine Kreditorrechungen** und eine Beschreibung ein, z.B. **Mir zur Genehmigung zugeweisene Kreditorenrechnungen**.</span><span class="sxs-lookup"><span data-stu-id="360c1-208">Enter a name, such as **My vendor invoices**, and a description, such as **Vendor invoices assigned to me for review**.</span></span>
6.  <span data-ttu-id="360c1-209">Klicken Sie auf **Fertig**.</span><span class="sxs-lookup"><span data-stu-id="360c1-209">Click **Done**.</span></span>
7.  <span data-ttu-id="360c1-210">Im mobilen Designer auf der Registerkarte **Felder** klicken Sie auf **Felder wählen**.</span><span class="sxs-lookup"><span data-stu-id="360c1-210">In the mobile designer, on the **Fields** tab, click **Select fields**.</span></span> <span data-ttu-id="360c1-211">Die Spalten auf der Listenseite müssen der folgenden Abbildung ähneln.</span><span class="sxs-lookup"><span data-stu-id="360c1-211">The columns on the list page must resemble the following illustration.</span></span> <span data-ttu-id="360c1-212">[![Spalten auf der Seite "Mir zugeweisene ausstehenden Kreditorenrechnungen"](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)</span><span class="sxs-lookup"><span data-stu-id="360c1-212">[![Columns on the Pending vendor invoices assigned to me page](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)</span></span>
8.  <span data-ttu-id="360c1-213">Fügen Sie die erforderlichen Spalten von der Listenseite hinzu, die für Benutzern in der mobilen Seite angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="360c1-213">Add the required columns from the list page that must be shown to the users in the mobile page.</span></span> <span data-ttu-id="360c1-214">Die Reihenfolge, in der Sie hinzufügen, entspricht der Reihenfolge, in der die Felder an Endbenutzer angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="360c1-214">The order in which you add is the order in which the fields will be displayed to the end user.</span></span> <span data-ttu-id="360c1-215">Die einzige Methode, die Reihenfolge der Felder zu ändern ist, indem alle Felder erneut auswählen.</span><span class="sxs-lookup"><span data-stu-id="360c1-215">The only way to change the ordering of the fields will be by re-selecting all the fields.</span></span> <span data-ttu-id="360c1-216">Basierend auf den Anforderungen für dieses Szenarios, sind die folgenden acht Felder obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="360c1-216">Based on the requirements for this scenario, the following eight fields are required.</span></span> <span data-ttu-id="360c1-217">Allerdings erachten mehrere Benutzer acht Felder für zu viele Informationen, die auf einem mobilen Gerät zu haben.</span><span class="sxs-lookup"><span data-stu-id="360c1-217">However, some users might consider eight fields too much information to have on a mobile device.</span></span> <span data-ttu-id="360c1-218">Daher werden nur die wichtigsten Felder in der mobilen Listenansicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="360c1-218">Therefore, we will show only the most important fields in the mobile list view.</span></span> <span data-ttu-id="360c1-219">Die übrigen Felder erscheinen in der Detailansicht, die Sie später entwerfen.</span><span class="sxs-lookup"><span data-stu-id="360c1-219">The remaining fields will appear in the details view that we will design later.</span></span> <span data-ttu-id="360c1-220">Jetzt fügen Sie nur die folgenden Felder hinzu.</span><span class="sxs-lookup"><span data-stu-id="360c1-220">For now, we will add the following fields.</span></span> <span data-ttu-id="360c1-221">Klicken Sie auf das Pluszeichen (**+**) in den Spalten die Sie zum mobilen Seite hinzuzufügen wollen.</span><span class="sxs-lookup"><span data-stu-id="360c1-221">Click the plus sign (**+**) in these columns to add to the mobile page.</span></span>
    - <span data-ttu-id="360c1-222">Kreditorenname</span><span class="sxs-lookup"><span data-stu-id="360c1-222">Vendor name</span></span>
    - <span data-ttu-id="360c1-223">Rechnungssumme</span><span class="sxs-lookup"><span data-stu-id="360c1-223">Invoice total</span></span>
    - <span data-ttu-id="360c1-224">Rechnungskonto</span><span class="sxs-lookup"><span data-stu-id="360c1-224">Invoice account</span></span>
    - <span data-ttu-id="360c1-225">Rechnungsnummer</span><span class="sxs-lookup"><span data-stu-id="360c1-225">Invoice number</span></span>
    - <span data-ttu-id="360c1-226">Rechnungsdatum</span><span class="sxs-lookup"><span data-stu-id="360c1-226">Invoice date</span></span>

    <span data-ttu-id="360c1-227">Nachdem die Felder hinzugefügt sind, muss die mobile Seite der folgenden Abbildung ähneln.</span><span class="sxs-lookup"><span data-stu-id="360c1-227">After the fields are added, the mobile page must resemble the following illustration.</span></span> 
    <span data-ttu-id="360c1-228">[![Seite nach Felder hinzugefügt](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)</span><span class="sxs-lookup"><span data-stu-id="360c1-228">[![Page after fields are added](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)</span></span>
9.  <span data-ttu-id="360c1-229">Sie müssen außerdem die folgenden Spalten hinzufügen, sodass wir Workflowaktivitäten später aktivieren können.</span><span class="sxs-lookup"><span data-stu-id="360c1-229">You must also add the following columns now, so that we can enable workflow actions later.</span></span>
    - <span data-ttu-id="360c1-230">Abgeschlossene Aufgabe anzeigen</span><span class="sxs-lookup"><span data-stu-id="360c1-230">Show complete task</span></span>
    - <span data-ttu-id="360c1-231">Delegataufgabe anzeigen</span><span class="sxs-lookup"><span data-stu-id="360c1-231">Show delegate task</span></span>
    - <span data-ttu-id="360c1-232">Zurückrufene Aufgabe anzeigen</span><span class="sxs-lookup"><span data-stu-id="360c1-232">Show recall task</span></span>
    - <span data-ttu-id="360c1-233">Abgelehnte Aufgabe anzeigen</span><span class="sxs-lookup"><span data-stu-id="360c1-233">Show reject task</span></span>
    - <span data-ttu-id="360c1-234">Abschlussanforderung Aufgabe anzeigen</span><span class="sxs-lookup"><span data-stu-id="360c1-234">Show request completion task</span></span>
    - <span data-ttu-id="360c1-235">Aufgabe erneut übermitteln anzeigen</span><span class="sxs-lookup"><span data-stu-id="360c1-235">Show resubmit task</span></span>

10. <span data-ttu-id="360c1-236">Klicken Sie auf **Fertig**, um den Bearbeitungsmodus zu verlassen.</span><span class="sxs-lookup"><span data-stu-id="360c1-236">Click **Done** to exit edit mode.</span></span>
11. <span data-ttu-id="360c1-237">Klicken Sie auf **Zurück** und **Fertig**, um den Arbeitsbereich zu beenden</span><span class="sxs-lookup"><span data-stu-id="360c1-237">Click **Back** and then **Done** to exit the workspace</span></span>
12. <span data-ttu-id="360c1-238">Klicken Sie auf **Arbeitsbereich veröffentlichen**, um die Arbeit zu speichern.</span><span class="sxs-lookup"><span data-stu-id="360c1-238">Click **Publish workspace** to save your work.</span></span>
13. <span data-ttu-id="360c1-239">Aktivieren Sie **Rechnungssumme in Kreditorenrechnungsliste anzeigen** im Formular Kreditorparameter unter **Rechnung**.</span><span class="sxs-lookup"><span data-stu-id="360c1-239">Enable **Display invoice total on pending vendor invoices list** in accounts payable parameters form under **Invoice**.</span></span> <span data-ttu-id="360c1-240">Beachten Sie, dass, nur, indem Sie diesen Parameter aktiviert, Rechnungssummen berechnet werden, der auf Kreditorenrechnungslistenseite ausstehenden angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="360c1-240">Note that, only by enabling this parameter, invoice totals will be calculated to be displayed on the pending vendor invoices list page.</span></span> <span data-ttu-id="360c1-241">Dies ist eine neue Funktion als Teil des erforderlichen Hotfixes 3208224.</span><span class="sxs-lookup"><span data-stu-id="360c1-241">This is a new capability as part of the pre-requisite hot fix 3208224.</span></span>

### <a name="vendor-invoice-details"></a><span data-ttu-id="360c1-242">Details der Kreditorenrechnung</span><span class="sxs-lookup"><span data-stu-id="360c1-242">Vendor invoice details</span></span>

<span data-ttu-id="360c1-243">Um die Rechnungsdetailseite für die mobile App zu entwerfen, verwenden Sie die **VendMobileInvoiceHeaderDetails**-Seite in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="360c1-243">To design the invoice details page for mobile, use the **VendMobileInvoiceHeaderDetails** page in Finance and Operations.</span></span> <span data-ttu-id="360c1-244">Beachten Sie diese, abhängig von der Anzahl der Rechnungen, die Sie in Ihrem System gibt, enthält dieser Seite die älteste Rechnung (die Rechnung, die zuerst erstellt wurde).</span><span class="sxs-lookup"><span data-stu-id="360c1-244">Note that, depending on the number of invoices that you have in your system, this page shows the oldest invoice (the invoice that was created first).</span></span> <span data-ttu-id="360c1-245">Sie können den Filter links verwenden um eine bestimmte Rechnung zu suchen.</span><span class="sxs-lookup"><span data-stu-id="360c1-245">To find a specific invoice, you can use the filter on the left.</span></span> <span data-ttu-id="360c1-246">Allerdings benötigen wir keine bestimmte Rechnung für dieses Beispiel.</span><span class="sxs-lookup"><span data-stu-id="360c1-246">However, we don’t require a specific invoice for this example.</span></span> <span data-ttu-id="360c1-247">Es müssen nur einige Rechnungsinformationen, sodass wir die mobile Seite zu entwerfen.</span><span class="sxs-lookup"><span data-stu-id="360c1-247">We just require some invoice data so that we can design the mobile page.</span></span> <span data-ttu-id="360c1-248">[![Workflowseite](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)</span><span class="sxs-lookup"><span data-stu-id="360c1-248">[![Workflow page](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)</span></span>

1. <span data-ttu-id="360c1-249">In der Finance and Operations-URL ersetzen Sie den Namen der Menüoption durch **VendMobileInvoiceHeaderDetails**, um das Formular zu öffnen</span><span class="sxs-lookup"><span data-stu-id="360c1-249">In the Finance and Operations URL, replace the name of the menu item with **VendMobileInvoiceHeaderDetails** to open the form</span></span>
2. <span data-ttu-id="360c1-250">Öffnen Sie den Designer von mobilen **Einstellungen** (Zahnrad) Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="360c1-250">Open the mobile designer from the **Settings** (gear) button.</span></span>
3. <span data-ttu-id="360c1-251">Klicken Sie auf die **Bearbeiten** Schaltfläche, um im Bearbeitungsmodus Arbeitsbereich zu starten.</span><span class="sxs-lookup"><span data-stu-id="360c1-251">Click the **Edit** button to start edit mode in the workspace.</span></span>
4. <span data-ttu-id="360c1-252">Wählen Sie die Seite **Meine Kreditorenrechnungen** aus, die Sie zuvor erstellt haben, und klicken Sie dann auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="360c1-252">Select the **My vendor invoices** page that you created earlier, and then click **Edit**.</span></span>
5. <span data-ttu-id="360c1-253">Auf der **Felder** Registerkarte klicken Sie auf die Spaltenüberschrift **Raster**</span><span class="sxs-lookup"><span data-stu-id="360c1-253">On the **Fields** tab, click the **Grid** column heading.</span></span>
6. <span data-ttu-id="360c1-254">Klicken Sie auf **Eigenschaften &gt; Seite hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="360c1-254">Click **Properties &gt; Add page**.</span></span> <span data-ttu-id="360c1-255">**Hinweis:** Wenn Sie auf das **Raster** Überschrift klicken und eine Seite hinzufügen, wird die Beziehung zur Detailseite automatisch bestimmt.</span><span class="sxs-lookup"><span data-stu-id="360c1-255">**Note:** When you click the **Grid** heading and add a page, the relationship with the details page is established automatically.</span></span>
7. <span data-ttu-id="360c1-256">Geben Sie einen Seitentitel, z.B. **Rechnungsdetails** und einer Beschreibung, wie ein **Ansichtsrechnungskopf und Positionsdetails**.</span><span class="sxs-lookup"><span data-stu-id="360c1-256">Enter a page title, such as **Invoice details**, and a description, such as **View invoice header and line details**.</span></span>
8. <span data-ttu-id="360c1-257">Klicken Sie auf **Felder auswählen**.</span><span class="sxs-lookup"><span data-stu-id="360c1-257">Click **Select fields**.</span></span> <span data-ttu-id="360c1-258">Die Reihenfolge, in der Sie hinzufügen, entspricht der Reihenfolge, in der die Felder an Endbenutzer angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="360c1-258">Note that, the order in which you add is the order in which the fields will be displayed to the end user.</span></span> <span data-ttu-id="360c1-259">Die einzige Methode, die Reihenfolge der Felder zu ändern ist, indem alle Felder erneut auswählen.</span><span class="sxs-lookup"><span data-stu-id="360c1-259">The only way to change the ordering of the fields will be by re-selecting all the fields.</span></span> 
9. <span data-ttu-id="360c1-260">Fügen Sie die folgenden Felder aus dem Auftragskopf, basierend auf den Anforderungen für dieses Szenarios hinzu:</span><span class="sxs-lookup"><span data-stu-id="360c1-260">Add the following fields from the header, based on the requirements for this scenario:</span></span>
   - <span data-ttu-id="360c1-261">Kreditorenname</span><span class="sxs-lookup"><span data-stu-id="360c1-261">Vendor name</span></span>
   - <span data-ttu-id="360c1-262">Rechnungssumme</span><span class="sxs-lookup"><span data-stu-id="360c1-262">Invoice total</span></span>
   - <span data-ttu-id="360c1-263">Rechnungskonto</span><span class="sxs-lookup"><span data-stu-id="360c1-263">Invoice account</span></span>
   - <span data-ttu-id="360c1-264">Rechnungsnummer</span><span class="sxs-lookup"><span data-stu-id="360c1-264">Invoice number</span></span>
   - <span data-ttu-id="360c1-265">Rechnungsdatum</span><span class="sxs-lookup"><span data-stu-id="360c1-265">Invoice date</span></span>
   - <span data-ttu-id="360c1-266">Rechnungsbeschreibung</span><span class="sxs-lookup"><span data-stu-id="360c1-266">Invoice description</span></span>
   - <span data-ttu-id="360c1-267">Fälligkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="360c1-267">Due date</span></span>
   - <span data-ttu-id="360c1-268">Rechnungswährung</span><span class="sxs-lookup"><span data-stu-id="360c1-268">Invoice currency</span></span>

10. <span data-ttu-id="360c1-269">Fügen Sie die folgenden Felder aus Positionsraster auf der Seite hinzu:</span><span class="sxs-lookup"><span data-stu-id="360c1-269">Add the following fields from the lines grid on the page:</span></span>
    - <span data-ttu-id="360c1-270">Beschaffungskategorie</span><span class="sxs-lookup"><span data-stu-id="360c1-270">Procurement category</span></span>
    - <span data-ttu-id="360c1-271">Leistung</span><span class="sxs-lookup"><span data-stu-id="360c1-271">Quantity</span></span>
    - <span data-ttu-id="360c1-272">Preis je Einheit</span><span class="sxs-lookup"><span data-stu-id="360c1-272">Unit price</span></span>
    - <span data-ttu-id="360c1-273">Nettobetrag der Position</span><span class="sxs-lookup"><span data-stu-id="360c1-273">Line net amount</span></span>
    - <span data-ttu-id="360c1-274">Steuerbetrag (US 1099)</span><span class="sxs-lookup"><span data-stu-id="360c1-274">1099 amount</span></span>

11. <span data-ttu-id="360c1-275">Nachdem alle Felder aus den früheren zwei Schritten hinzugefügt wurden, klicken Sie auf **Fertig**.</span><span class="sxs-lookup"><span data-stu-id="360c1-275">After all the fields from the previous two steps have been added, click **Done**.</span></span> <span data-ttu-id="360c1-276">Die müssen der folgenden Abbildung ähneln.</span><span class="sxs-lookup"><span data-stu-id="360c1-276">The page must resemble the following illustration.</span></span>
    <span data-ttu-id="360c1-277">[![Seite nach Felder hinzugefügt](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)</span><span class="sxs-lookup"><span data-stu-id="360c1-277">[![Page after fields are added](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)</span></span>
12. <span data-ttu-id="360c1-278">Klicken Sie auf **Fertig**, um den Bearbeitungsmodus zu verlassen.</span><span class="sxs-lookup"><span data-stu-id="360c1-278">Click **Done** to exit edit mode.</span></span>
13. <span data-ttu-id="360c1-279">Klicken Sie auf **Zurück** und **Fertig**, um den Arbeitsbereich zu beenden</span><span class="sxs-lookup"><span data-stu-id="360c1-279">Click **Back** and then **Done** to exit the workspace</span></span>
14. <span data-ttu-id="360c1-280">Klicken Sie auf **Arbeitsbereich veröffentlichen**, um die Arbeit zu speichern.</span><span class="sxs-lookup"><span data-stu-id="360c1-280">Click **Publish workspace** to save your work</span></span>

### <a name="workflow-actions"></a><span data-ttu-id="360c1-281">Workflowaktivitäten</span><span class="sxs-lookup"><span data-stu-id="360c1-281">Workflow actions</span></span>

<span data-ttu-id="360c1-282">Um Workflowaktivitäten hinzuzufügen, verwenden Sie die **VendMobileInvoiceHeaderDetails**-Seite in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="360c1-282">To add workflow actions, use the **VendMobileInvoiceHeaderDetails** page in Finance and Operations.</span></span> <span data-ttu-id="360c1-283">Um diese Seite zu öffnen, ersetzen Sie Name der Menüoption in die URL, wie Sie eben geschehen ist.</span><span class="sxs-lookup"><span data-stu-id="360c1-283">To open this page, replace the name of the menu item in the URL, as you did earlier.</span></span> <span data-ttu-id="360c1-284">Öffnen Sie den Designer von mobilen **Einstellungen** (Zahnrad) Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="360c1-284">Then open the mobile designer from the **Settings** (gear) button.</span></span> <span data-ttu-id="360c1-285">Gehen Sie folgendermaßen vor, um die Detailseite auf Workflowaktivitäten hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="360c1-285">Follow these steps to add workflow actions on the details page.</span></span> <span data-ttu-id="360c1-286">Sie müssen Rechnungen haben, die Ihnen zugewiesen wurden, die sich in einem angemessenen Status befinden, damit Ihnen die Workflowaktivitäten zur Verfügung stehen, für die Sie entwerfen möchten.</span><span class="sxs-lookup"><span data-stu-id="360c1-286">You must have invoices assigned to you that are in the appropriate state to make the workflow actions available to you that you are going to design for.</span></span>

#### <a name="record-workflow-actions"></a><span data-ttu-id="360c1-287">Workflowaktivitäten erfassen</span><span class="sxs-lookup"><span data-stu-id="360c1-287">Record workflow actions</span></span>
1.  <span data-ttu-id="360c1-288">Klicken Sie auf die **Bearbeiten** Schaltfläche, um im Bearbeitungsmodus Arbeitsbereich zu starten.</span><span class="sxs-lookup"><span data-stu-id="360c1-288">Click the **Edit** button to start edit mode in the workspace.</span></span>
2.  <span data-ttu-id="360c1-289">Wählen Sie die **Rechnungsdetails** Seite, die Sie eben erstellt haben, und klicken Sie dann **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="360c1-289">Select the **Invoice details** page that you created earlier, and then click **Edit**.</span></span>
3.  <span data-ttu-id="360c1-290">Klicken Sie auf der Registerkarte **Aktionen** auf **Aktion hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="360c1-290">On the **Actions** tab, click **Add action**.</span></span>
4.  <span data-ttu-id="360c1-291">Geben Sie einen Aktivitätstitel, z. B. **Genehmigen** und eine Beschreibung ein, z.B. **Rechnung genehmigen**.</span><span class="sxs-lookup"><span data-stu-id="360c1-291">Enter an action title, such as **Approve**, and a description, such as **Approve invoice**.</span></span> <span data-ttu-id="360c1-292">Beachten Sie, dass der Aktivitätstitel, den Sie hier eingeben, der Name der Aktivität ist, den Benutzer in der Zeit-App mobilen die angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="360c1-292">Note that the action title that you enter here becomes the name of the action that is shown to the user in the mobile app.</span></span>
5.  <span data-ttu-id="360c1-293">Klicken Sie auf **Fertig**.</span><span class="sxs-lookup"><span data-stu-id="360c1-293">Click **Done**.</span></span>
6.  <span data-ttu-id="360c1-294">Klicken Sie auf **Felder auswählen**.</span><span class="sxs-lookup"><span data-stu-id="360c1-294">Click **Select fields**.</span></span>
7.  <span data-ttu-id="360c1-295">Führen des Workflowprozesses auf der **VendMobileInvoiceHeaderDetails** Seite durch, und schließen Sie die Aktivität aus, die Sie erfassen. Ihren Planungen zufolge</span><span class="sxs-lookup"><span data-stu-id="360c1-295">Go through the workflow process on the **VendMobileInvoiceHeaderDetails** page, and complete the action that you wanted to record.</span></span> <span data-ttu-id="360c1-296">Überprüfen Sie, ob Sie Workflowkommentare während dieses Vorgangs ein eingegeben werden, damit auch im Kommentarfeld mobilen Erfahrung enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="360c1-296">Make sure that you enter workflow comments during this process, so that a comments field is also included in the mobile experience.</span></span>
8.  <span data-ttu-id="360c1-297">Nachdem die Workflowaktivität ausgeführt ist, klicken Sie auf **Fertig**, um die Felder auswählen-Aufgabe abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="360c1-297">After the workflow action is run, click **Done** to complete the Select fields task.</span></span>
9.  <span data-ttu-id="360c1-298">Klicken Sie auf **Fertig**, um den Bearbeitungsmodus zu verlassen.</span><span class="sxs-lookup"><span data-stu-id="360c1-298">Click **Done** to exit edit mode.</span></span>
10. <span data-ttu-id="360c1-299">Klicken Sie auf **Zurück** und **Fertig**, um den Arbeitsbereich zu beenden</span><span class="sxs-lookup"><span data-stu-id="360c1-299">Click **Back** and then **Done** to exit the workspace</span></span>
11. <span data-ttu-id="360c1-300">Klicken Sie auf **Arbeitsbereich veröffentlichen**, um die Arbeit zu speichern.</span><span class="sxs-lookup"><span data-stu-id="360c1-300">Click **Publish workspace** to save your work</span></span>
12. <span data-ttu-id="360c1-301">Wiederholen Sie die vorherigen Schritte, um alle erforderlichen Workflowaktivitäten zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="360c1-301">Repeat the previous steps to record all the required workflow actions.</span></span> 

#### <a name="create-a-js-file"></a><span data-ttu-id="360c1-302">Erstellen Sie eine JS-Datei.</span><span class="sxs-lookup"><span data-stu-id="360c1-302">Create a .js file</span></span>
1. <span data-ttu-id="360c1-303">Öffnen Sie den Editor oder Microsoft Visual Studio, und fügen Sie den folgenden Code ein.</span><span class="sxs-lookup"><span data-stu-id="360c1-303">Open Notepad or Microsoft Visual Studio, and paste the following code.</span></span> <span data-ttu-id="360c1-304">Speichern Sie die Datei als .js-Datei.</span><span class="sxs-lookup"><span data-stu-id="360c1-304">Save the file as a .js file.</span></span> <span data-ttu-id="360c1-305">Diese Code bewirkt Folgendes:</span><span class="sxs-lookup"><span data-stu-id="360c1-305">This code does the following:</span></span>
    - <span data-ttu-id="360c1-306">Er blendet die zusätzlichen workflowbezogenen Spalten aus, die wir früher mobilen auf der Listenseite hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="360c1-306">It hides the extra workflow-related columns that we added earlier on the mobile list page.</span></span> <span data-ttu-id="360c1-307">Es werden diesen Spalten hinzufügen, sodass der Zeit-App dass Informationen im Zusammenhang hat und die nächsten Schritt ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="360c1-307">We added these columns so that the app has that information in context and can do the next step.</span></span>
    - <span data-ttu-id="360c1-308">Anhand des Workflowschritt, die aktiv ist, wendet sie Logik, um nur die Vorgänge anzeigen.</span><span class="sxs-lookup"><span data-stu-id="360c1-308">Based on the workflow step that is active, it applies logic to show only those actions.</span></span>

> [!NOTE]
> <span data-ttu-id="360c1-309">Die Namen der Seiten und andere Steuerelemente im Code müssen mit den Namen im Arbeitsbereich identisch sein.</span><span class="sxs-lookup"><span data-stu-id="360c1-309">The name of the pages and other controls in the code must be the same as the names in the workspace.</span></span>

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

2.  <span data-ttu-id="360c1-310">Laden Sie die Codedatei dem Arbeitsbereich hohe, indem Sie die **Logik** Registerkarte auswählen</span><span class="sxs-lookup"><span data-stu-id="360c1-310">Upload the code file to the workspace by selecting the **Logic** tab</span></span>
3.  <span data-ttu-id="360c1-311">Klicken Sie auf **Fertig**, um den Bearbeitungsmodus zu verlassen.</span><span class="sxs-lookup"><span data-stu-id="360c1-311">Click **Done** to exit edit mode.</span></span>
4.  <span data-ttu-id="360c1-312">Klicken Sie auf **Zurück** und **Fertig**, um den Arbeitsbereich zu beenden</span><span class="sxs-lookup"><span data-stu-id="360c1-312">Click **Back** and then **Done** to exit the workspace</span></span>
5.  <span data-ttu-id="360c1-313">Klicken Sie auf **Arbeitsbereich veröffentlichen**, um die Arbeit zu speichern.</span><span class="sxs-lookup"><span data-stu-id="360c1-313">Click **Publish workspace** to save your work</span></span>

### <a name="vendor-invoice-attachments"></a><span data-ttu-id="360c1-314">Kreditorenrechungsanhänge</span><span class="sxs-lookup"><span data-stu-id="360c1-314">Vendor invoice attachments</span></span>

1. <span data-ttu-id="360c1-315">Klicken Sie auf **Einstellungen** (Zahnrad) in der oberen rechten Ecke der Seite und klicken dann auf **Mobile App**.</span><span class="sxs-lookup"><span data-stu-id="360c1-315">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**</span></span>
2. <span data-ttu-id="360c1-316">Klicken Sie auf die **Bearbeiten** Schaltfläche, um im Bearbeitungsmodus Arbeitsbereich zu starten.</span><span class="sxs-lookup"><span data-stu-id="360c1-316">Click the **Edit** button to start edit mode in the workspace.</span></span>
3. <span data-ttu-id="360c1-317">Wählen Sie die Seite <strong>Rechnungsdetails **aus, die Sie zuvor erstellt haben, und klicken Sie dann auf** Bearbeiten</strong>.</span><span class="sxs-lookup"><span data-stu-id="360c1-317">Select the <strong>Invoice details \*\*page that you created earlier, and then click \*\*Edit</strong>.</span></span>
4. <span data-ttu-id="360c1-318">Legen Sie die **Dokumentverwaltung** Option **Ja** wie weiter unten) fest.</span><span class="sxs-lookup"><span data-stu-id="360c1-318">Set the **Document management** option to **Yes** as shown below.</span></span> <span data-ttu-id="360c1-319">**Hinweis:** Wenn keine Anforderungen gibt, Zuordnungen im mobilen Gerät angezeigt werden, können Sie diese Option **Nein**, mit der die Standardeinstellung ist.</span><span class="sxs-lookup"><span data-stu-id="360c1-319">**Note:** If there are no requirements to show attachments on the mobile device, you can leave this option set to **No**, which is the default setting.</span></span>
   <span data-ttu-id="360c1-320">![Dokumentverwaltung](./media/docmanagement-216x300.png)</span><span class="sxs-lookup"><span data-stu-id="360c1-320">![Document management](./media/docmanagement-216x300.png)</span></span>
5. <span data-ttu-id="360c1-321">Klicken Sie auf **Fertig**, um den Bearbeitungsmodus zu verlassen.</span><span class="sxs-lookup"><span data-stu-id="360c1-321">Click **Done** to exit edit mode.</span></span>
6. <span data-ttu-id="360c1-322">Klicken Sie auf **Zurück** und **Fertig**, um den Arbeitsbereich zu beenden</span><span class="sxs-lookup"><span data-stu-id="360c1-322">Click **Back** and then **Done** to exit the workspace</span></span>
7. <span data-ttu-id="360c1-323">Klicken Sie auf **Arbeitsbereich veröffentlichen**, um die Arbeit zu speichern.</span><span class="sxs-lookup"><span data-stu-id="360c1-323">Click **Publish workspace** to save your work</span></span>

### <a name="vendor-invoice-line-distributions"></a><span data-ttu-id="360c1-324">Kreditorrechungspositionsverteilungen</span><span class="sxs-lookup"><span data-stu-id="360c1-324">Vendor invoice line distributions</span></span>

<span data-ttu-id="360c1-325">Die Anforderungen für dieses Szenarios bestätigen, dass nur Verteilungen auf Positionsebene sind und dass eine Rechnung immer nur eine Position ist.</span><span class="sxs-lookup"><span data-stu-id="360c1-325">The requirements for this scenario confirm that there will be only line-level distributions, and that an invoice will always have only one line.</span></span> <span data-ttu-id="360c1-326">Da dieses Szenario ist einfach, muss die Benutzerfreundlichkeit auf dem auch einfach mobilen Gerät genug sein, dem der Benutzer nicht mehrere Ebenen muss Detailinformationen anzeigen, damit die Verteilungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="360c1-326">Because this scenario is simple, the user experience on the mobile device must also be simple enough that the user doesn’t have to drill down several levels to view the distributions.</span></span> <span data-ttu-id="360c1-327">Kreditorenrechnungen in Finance and Operations enthalten die Option des Anzeigens aller Verteilungen aus dem Rechnungskopf.</span><span class="sxs-lookup"><span data-stu-id="360c1-327">Vendor invoices in Finance and Operations include the option of showing all distributions from the invoice header.</span></span> <span data-ttu-id="360c1-328">Diese Umgebung ist was wir für das mobile Szenario benötigen.</span><span class="sxs-lookup"><span data-stu-id="360c1-328">This experience is what we need for the mobile scenario.</span></span> <span data-ttu-id="360c1-329">Daher verwenden Sie die **VendMobileInvoiceAllDistributionTree** Seite, um diesen Teil des mobilen Szenarios zu entwerfen.</span><span class="sxs-lookup"><span data-stu-id="360c1-329">Therefore, we will use the **VendMobileInvoiceAllDistributionTree** page to design this part of the mobile scenario.</span></span> 

> [!NOTE] 
> <span data-ttu-id="360c1-330">Das Kennen der Anforderungen können uns, entscheiden, die die betreffende genau zu verwenden Seite, und wie die mobile Erfahrung des Benutzers optimiert, wenn Sie das Szenario entwerfen.</span><span class="sxs-lookup"><span data-stu-id="360c1-330">Knowing the requirements helps us decide which specific page to use and how exactly to optimize the mobile experience for the user when we design the scenario.</span></span> <span data-ttu-id="360c1-331">Im zweiten Szenario können wir eine andere Seite, damit die Verteilungen anzuzeigen, weil die Anforderungen für dieses Szenarios unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="360c1-331">In the second scenario, we will use a different page to show the distributions, because the requirements for that scenario differ.</span></span>

1.  <span data-ttu-id="360c1-332">In der URL ersetzten Sie den Name der Menüoption.</span><span class="sxs-lookup"><span data-stu-id="360c1-332">In the URL, replace the name of the menu item, as you did before.</span></span> <span data-ttu-id="360c1-333">Die Seite, die angezeigt wird, sollte der folgenden Abbildung ähneln.</span><span class="sxs-lookup"><span data-stu-id="360c1-333">The page that appears should resemble the following illustration.</span></span>
<span data-ttu-id="360c1-334">[![Alle Verteilungen-Seite](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)</span><span class="sxs-lookup"><span data-stu-id="360c1-334">[![All distributions page](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)</span></span>
2.  <span data-ttu-id="360c1-335">Öffnen Sie den Designer von mobilen **Einstellungen** (Zahnrad) Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="360c1-335">Open the mobile designer from the **Settings** (gear) button.</span></span>
3.  <span data-ttu-id="360c1-336">Klicken Sie auf die **Bearbeiten** Schaltfläche, um im Bearbeitungsmodus Arbeitsbereich zu starten.</span><span class="sxs-lookup"><span data-stu-id="360c1-336">Click the **Edit** button to start edit mode in the workspace.</span></span> <span data-ttu-id="360c1-337">**Hinweis:** Sie sehen, dass zwei neue Seiten automatisch erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="360c1-337">**Note:** You will see that two new pages were created automatically.</span></span> <span data-ttu-id="360c1-338">Das System diese Seiten erstellt, da Sie die Dokumentverwaltung im vorherigen Abschnitt einschalteten.</span><span class="sxs-lookup"><span data-stu-id="360c1-338">The system creates these pages, because you turned on document management in the previous section.</span></span> <span data-ttu-id="360c1-339">Sie können diese Seiten neuen ignorieren.</span><span class="sxs-lookup"><span data-stu-id="360c1-339">You can ignore these new pages.</span></span>
4.  <span data-ttu-id="360c1-340">Klicken Sie auf **Seite hinzufügen.**</span><span class="sxs-lookup"><span data-stu-id="360c1-340">Click **Add page**.</span></span>
5.  <span data-ttu-id="360c1-341">Geben Sie einen Seitentitel, wie **Ansichtsbuchhaltung** und eine Beschreibung ein, z.B. **Ansicht für die Rechnung** ein.</span><span class="sxs-lookup"><span data-stu-id="360c1-341">Enter a page title, such as **View accounting**, and a description, such as **View accounting for the invoice**.</span></span>
6.  <span data-ttu-id="360c1-342">Klicken Sie auf **Fertig**.</span><span class="sxs-lookup"><span data-stu-id="360c1-342">Click **Done**.</span></span>
7.  <span data-ttu-id="360c1-343">Auf der Registerkarte **Felder** wählen Sie **Felder auswählen**, die folgenden Felder aus der Verteilungsseite aus und klicken dann **Fertig**.</span><span class="sxs-lookup"><span data-stu-id="360c1-343">On the **Fields** tab, click **Select fields**, select the following fields from the distributions page, and then click **Done**:</span></span>
    1.  <span data-ttu-id="360c1-344">Betrag</span><span class="sxs-lookup"><span data-stu-id="360c1-344">Amount</span></span>
    2.  <span data-ttu-id="360c1-345">Währung</span><span class="sxs-lookup"><span data-stu-id="360c1-345">Currency</span></span>
    3.  <span data-ttu-id="360c1-346">Sachkonto</span><span class="sxs-lookup"><span data-stu-id="360c1-346">Ledger account</span></span>

    > [!NOTE] 
    > <span data-ttu-id="360c1-347">Es können die **Beschreibung** Spalte im Verteilungsraster aus, weil die Anforderungen für dieses Szenarios bestätigten, dass der erweiterte Preis der einzige Betrag ist, dass für Verteilungen gibt.</span><span class="sxs-lookup"><span data-stu-id="360c1-347">We didn’t select the **Description** column from the distributions grid, because the requirements for this scenario confirmed that the extended price is the only amount that there will be distributions for.</span></span> <span data-ttu-id="360c1-348">Daher fordert der Benutzer kein anderes Feld, den Betragstyp festzustellen, ob die Verteilung für ist.</span><span class="sxs-lookup"><span data-stu-id="360c1-348">Therefore, the user won’t require another field to determine the amount type that the distribution is for.</span></span> <span data-ttu-id="360c1-349">Allerdings im folgenden Szenario verwenden, wir **werden** Sie diese Informationen, weil die Anforderungen für dieses Szenarios angeben, dass andere Betragsart Verteilungen haben (z, Mehrwertsteuer).</span><span class="sxs-lookup"><span data-stu-id="360c1-349">However, in the next scenario, we **will** use this information, because the requirements for that scenario specify that other amount types have distributions (for example, sales tax).</span></span>
8.  <span data-ttu-id="360c1-350">Klicken Sie auf **Fertig**, um den Bearbeitungsmodus zu verlassen.</span><span class="sxs-lookup"><span data-stu-id="360c1-350">Click **Done** to exit edit mode.</span></span>
9.  <span data-ttu-id="360c1-351">Klicken Sie auf **Zurück** und **Fertig**, um den Arbeitsbereich zu beenden</span><span class="sxs-lookup"><span data-stu-id="360c1-351">Click **Back** and then **Done** to exit the workspace</span></span>
10. <span data-ttu-id="360c1-352">Klicken Sie auf **Arbeitsbereich veröffentlichen**, um die Arbeit zu speichern.</span><span class="sxs-lookup"><span data-stu-id="360c1-352">Click **Publish workspace** to save your work</span></span>

> [!NOTE] 
> <span data-ttu-id="360c1-353">Die mobile Seite **Buchhaltung anzeigen** ist derzeit mit keiner mobilen Seiten verknüpft, die wir bisher entworfen haben.</span><span class="sxs-lookup"><span data-stu-id="360c1-353">The **View accounting** mobile page isn’t currently linked to any of the mobile pages that we have designed so far.</span></span> <span data-ttu-id="360c1-354">Da der Benutzer in der Lage sein soll, die Seite **Buchhaltung anzeigen** aus der **Rechnungsdetails** Seite im mobilen Gerät zu navigieren, müssen Sie zuvor aus der **Rechnungsdetails** Seite der **Buchhaltung anzeigen** Seite bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="360c1-354">Because the user should be able to navigate to the **View accounting** page from the **Invoice details** page on the mobile device, we must provide navigation from the **Invoice details** page to the **View accounting** page.</span></span> <span data-ttu-id="360c1-355">Wir legen die Navigationsverknüpfung ein, indem wir Zusatzlogik zu JavaScript verwenden.</span><span class="sxs-lookup"><span data-stu-id="360c1-355">We establish this navigation by using additional logic via JavaScript.</span></span>

1.  <span data-ttu-id="360c1-356">Öffnen Sie die JS-Datei, die Sie eben erstellt haben, und fügen Sie die Positionen hinzu, die im folgenden Code hervorgehoben werden.</span><span class="sxs-lookup"><span data-stu-id="360c1-356">Open the .js file that you created earlier, and add the lines that are highlighted in the following code.</span></span> <span data-ttu-id="360c1-357">Dieser Code mach zwei Dinge:</span><span class="sxs-lookup"><span data-stu-id="360c1-357">This code does two things:</span></span>
    1.  <span data-ttu-id="360c1-358">Er wird sichergestellt, dass Benutzer nicht direkt über der Arbeitsbereich **Buchhaltung anzeigen** Seite Navigation können.</span><span class="sxs-lookup"><span data-stu-id="360c1-358">It helps guarantee that users can’t navigate directly from the workspace to the **View accounting** page.</span></span>
    2.  <span data-ttu-id="360c1-359">Er wird ein Navigationssteuerelement der **Rechnungsdetails** Seite der **Buchhaltung anzeigen** Seite ein.</span><span class="sxs-lookup"><span data-stu-id="360c1-359">It establishes a navigation control from the **Invoice details** page to the **View accounting** page.</span></span>

> [!NOTE] 
> <span data-ttu-id="360c1-360">Die Namen der Seiten und andere Steuerelemente im Code müssen mit den Namen im Arbeitsbereich identisch sein.</span><span class="sxs-lookup"><span data-stu-id="360c1-360">The name of the pages and other controls in the code must be the same as the names in the workspace.</span></span>

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

2.  <span data-ttu-id="360c1-361">Laden Sie die Codedatei dem Arbeitsbereich hohe, indem Sie die **Logik** Registerkarte zum Überschreiben des Codes auswählen</span><span class="sxs-lookup"><span data-stu-id="360c1-361">Upload the code file to the workspace by selecting the **Logic** tab to overwrite the previous code</span></span>
3.  <span data-ttu-id="360c1-362">Klicken Sie auf **Fertig**, um den Bearbeitungsmodus zu verlassen.</span><span class="sxs-lookup"><span data-stu-id="360c1-362">Click **Done** to exit edit mode.</span></span>
4.  <span data-ttu-id="360c1-363">Klicken Sie auf **Zurück** und **Fertig**, um den Arbeitsbereich zu beenden</span><span class="sxs-lookup"><span data-stu-id="360c1-363">Click **Back** and then **Done** to exit the workspace</span></span>
5.  <span data-ttu-id="360c1-364">Klicken Sie auf **Arbeitsbereich veröffentlichen**, um die Arbeit zu speichern.</span><span class="sxs-lookup"><span data-stu-id="360c1-364">Click **Publish workspace** to save your work</span></span>

### <a name="validation"></a><span data-ttu-id="360c1-365">Prüfung</span><span class="sxs-lookup"><span data-stu-id="360c1-365">Validation</span></span>

<span data-ttu-id="360c1-366">Öffnen Sie auf Ihrem mobilen Gerät die App, und stellen Sie eine Verbindung mit Ihrer Finance and Operations-Instanz her.</span><span class="sxs-lookup"><span data-stu-id="360c1-366">From your mobile device, open the app, and connect to your Finance and Operations instance.</span></span> <span data-ttu-id="360c1-367">Überprüfen Sie, ob Sie in das Unternehmen ein, in dem Kreditorenrechnungen Ihnen zur Prüfung zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="360c1-367">Make sure that you sign in to the company where vendor invoices are assigned to you for review.</span></span> <span data-ttu-id="360c1-368">Sie sollten in der Lage sein, die folgenden Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="360c1-368">You should be able to perform the following actions:</span></span>

-   <span data-ttu-id="360c1-369">Siehe den **Meine Genehmigungen** Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="360c1-369">See the **My approvals** workspace.</span></span>
-   <span data-ttu-id="360c1-370">Öffnen Sie den **Meine Genehmigungen** Arbeitsbereich und sehen Sie die **Meine Kreditorenrechnungen** Seite.</span><span class="sxs-lookup"><span data-stu-id="360c1-370">Drill into the **My approvals** workspace and see the **My vendor invoices** page.</span></span>
-   <span data-ttu-id="360c1-371">Öffnen Sie die **Meine Kreditorenrechnungen** Seite und erscheinen die Liste der Rechnungen, die Ihnen zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="360c1-371">Drill into the **My vendor invoices** page and see the list of invoices that are assigned to you.</span></span>
-   <span data-ttu-id="360c1-372">Öffnen Sie eine der Rechnungen und die Rechnungskopfdetails finden und -Positionsdetails.</span><span class="sxs-lookup"><span data-stu-id="360c1-372">Drill into one of the invoices, and see the invoice header details and line details.</span></span>
-   <span data-ttu-id="360c1-373">Auf der Detailseite finden Sie einen Link zu den Anlagen, und verwenden Sie diesen Link, die der Anhangliste zu navigieren und die Anhänge anzeigen.</span><span class="sxs-lookup"><span data-stu-id="360c1-373">On the details page, see a link to attachments, and use this link to navigate to the attachments list and view the attachments.</span></span>
-   <span data-ttu-id="360c1-374">Auf der Detailseite finden Sie einen Link zur Seite **Buchhaltung anzeigen** und verwenden Sie diesen Link, um zur Verteilungsseite zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="360c1-374">On the details page, see a link to the **View accounting** page, and use this link to navigate to the distributions page and view the distributions.</span></span>
-   <span data-ttu-id="360c1-375">Auf der Detailseite klicken Sie auf das Menü **Aktivitäten** unten, und lassen Workflowaktivitäten aus, die z Workflowschritt gültig sind.</span><span class="sxs-lookup"><span data-stu-id="360c1-375">On the details page, click the **Actions** menu at the bottom, and perform workflow actions that are applicable to the workflow step.</span></span>

## <a name="designing-a-complex-invoice-approval-scenario-for-fabrikam"></a><span data-ttu-id="360c1-376">Entwerfen eines komplexen Rechnungsgenehmigungsszenarios für Fabrikam</span><span class="sxs-lookup"><span data-stu-id="360c1-376">Designing a complex invoice approval scenario for Fabrikam</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="360c1-377">Szenarioattribut</span><span class="sxs-lookup"><span data-stu-id="360c1-377">Scenario attribute</span></span></th>
<th><span data-ttu-id="360c1-378">Antwort</span><span class="sxs-lookup"><span data-stu-id="360c1-378">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="360c1-379">Welche Felder aus dem Rechnungskopf wünschen die Benutzer in mobilen Umgebungen und in welcher Reihenfolge?</span><span class="sxs-lookup"><span data-stu-id="360c1-379">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="360c1-380">Kreditorenname</span><span class="sxs-lookup"><span data-stu-id="360c1-380">Vendor name</span></span></li>
<li><span data-ttu-id="360c1-381">Rechnungsbetrag</span><span class="sxs-lookup"><span data-stu-id="360c1-381">Invoice amount</span></span></li>
<li><span data-ttu-id="360c1-382">Rechnungskonto</span><span class="sxs-lookup"><span data-stu-id="360c1-382">Invoice account</span></span></li>
<li><span data-ttu-id="360c1-383">Rechnungsnummer</span><span class="sxs-lookup"><span data-stu-id="360c1-383">Invoice number</span></span></li>
<li><span data-ttu-id="360c1-384">Rechnungsdatum</span><span class="sxs-lookup"><span data-stu-id="360c1-384">Invoice date</span></span></li>
<li><span data-ttu-id="360c1-385">Rechnungsbeschreibung</span><span class="sxs-lookup"><span data-stu-id="360c1-385">Invoice description</span></span></li>
<li><span data-ttu-id="360c1-386">Fälligkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="360c1-386">Due date</span></span></li>
<li><span data-ttu-id="360c1-387">Rechnungswährung</span><span class="sxs-lookup"><span data-stu-id="360c1-387">Invoice currency</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="360c1-388">Welche Felder aus den Rechnungsposition wünschen die Benutzer in mobilen Umgebungen und in welcher Reihenfolge?</span><span class="sxs-lookup"><span data-stu-id="360c1-388">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="360c1-389">Beschaffungskategorie</span><span class="sxs-lookup"><span data-stu-id="360c1-389">Procurement category</span></span></li>
<li><span data-ttu-id="360c1-390">Leistung</span><span class="sxs-lookup"><span data-stu-id="360c1-390">Quantity</span></span></li>
<li><span data-ttu-id="360c1-391">Preis je Einheit</span><span class="sxs-lookup"><span data-stu-id="360c1-391">Unit price</span></span></li>
<li><span data-ttu-id="360c1-392">Nettobetrag der Position</span><span class="sxs-lookup"><span data-stu-id="360c1-392">Line net amount</span></span></li>
<li><span data-ttu-id="360c1-393">Steuerbetrag (US 1099)</span><span class="sxs-lookup"><span data-stu-id="360c1-393">1099 amount</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="360c1-394">Wie viele Rechnungspositionen gibt es in einer Rechnung?</span><span class="sxs-lookup"><span data-stu-id="360c1-394">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="360c1-395">Wenden Sie die 80-20-Regel hier an, und optimieren Sie für 80 Prozent.</span><span class="sxs-lookup"><span data-stu-id="360c1-395">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span></td>
<td><span data-ttu-id="360c1-396">5</span><span class="sxs-lookup"><span data-stu-id="360c1-396">5</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="360c1-397">Möchten Benutzer Buchhaltungsverteilungen (Rechnungscodierung) auf dem mobilen Gerät sehen?</span><span class="sxs-lookup"><span data-stu-id="360c1-397">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span></td>
<td><span data-ttu-id="360c1-398">Ja</span><span class="sxs-lookup"><span data-stu-id="360c1-398">Yes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="360c1-399">Wie viele Buchhaltungsverteilungen (erweiterte Preis, Mehrwertsteuer, Belastungen, usw.) gibt es für eine Rechnungsposition?</span><span class="sxs-lookup"><span data-stu-id="360c1-399">How many accounting distributions (extended price, sales tax, charges, and so on) are there for an invoice line?</span></span> <span data-ttu-id="360c1-400">Wieder gilt die Regel 80-20.</span><span class="sxs-lookup"><span data-stu-id="360c1-400">Again, apply the 80-20 rule.</span></span></td>
<td><span data-ttu-id="360c1-401">Erweiterter Preis: 2 Mehrwertsteuer: 2 Zuschläge: 2</span><span class="sxs-lookup"><span data-stu-id="360c1-401">Extended price: 2 Sales tax: 2 Charges: 2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="360c1-402">Haben Rechnungen auch Buchhaltungsverteilungen im Rechnungskopf?</span><span class="sxs-lookup"><span data-stu-id="360c1-402">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="360c1-403">Falls ja sollen diese Buchhaltungsverteilungen im Gerät verfügbar sein?</span><span class="sxs-lookup"><span data-stu-id="360c1-403">If so, should these accounting distributions be available on the device?</span></span></td>
<td><span data-ttu-id="360c1-404">Nicht verwendet</span><span class="sxs-lookup"><span data-stu-id="360c1-404">Not used</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="360c1-405">Möchten Benutzer Anhänge für die Rechnung auf dem Gerät angezeigt?</span><span class="sxs-lookup"><span data-stu-id="360c1-405">Will users want to see attachments for the invoice on the device?</span></span></td>
<td><span data-ttu-id="360c1-406">Ja</span><span class="sxs-lookup"><span data-stu-id="360c1-406">Yes</span></span></td>
</tr>
</tbody>
</table>

### <a name="next-steps"></a><span data-ttu-id="360c1-407">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="360c1-407">Next steps</span></span>

<span data-ttu-id="360c1-408">Die folgenden Abweichungen für Szenario 1, basierend auf den Anforderungen für Szenario 2.</span><span class="sxs-lookup"><span data-stu-id="360c1-408">The following variations can be done for scenario 1, based on the requirements for scenario 2.</span></span> <span data-ttu-id="360c1-409">Sie können in diesem Bereich verwenden, um Ihre Erfahrung mit der mobilen App zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="360c1-409">You can use this section to improve your mobile app experience.</span></span>

1.  <span data-ttu-id="360c1-410">Da weitere Rechnungspositionen in Szenario 2 erwartet werden, können folgende Änderungen zum Entwurf, die Benutzererfahrung im mobilen Gerät zu optimieren:</span><span class="sxs-lookup"><span data-stu-id="360c1-410">Because more invoice lines are expected in scenario 2, the following changes to the design will help optimize the user experience on the mobile device:</span></span>
    1.  <span data-ttu-id="360c1-411">Anstelle der Betrachtungsrechnungspositionen auf Detailseite der (z.B. in Szenario 1), Benutzer festlegen, dass Positionen einer separaten mobilen Seite anzeigen.</span><span class="sxs-lookup"><span data-stu-id="360c1-411">Instead of viewing invoice lines on the details page (as in scenario 1), users can choose to view lines on a separate mobile page.</span></span>
    2.  <span data-ttu-id="360c1-412">Da mehrere Rechnungsposition in diesem Szenario erwartet wird, wenn die **VendMobileInvoiceAllDistributionTree** Seite verwendet wird, um die Verteilungsseite für Datenschutzerklärung zu entwerfen (wie in Szenario 1), kann es verwirrend, damit der Benutzer Positionen mit Verteilungen aufeinander umfasst.</span><span class="sxs-lookup"><span data-stu-id="360c1-412">Because more than one invoice line is expected in this scenario, if the **VendMobileInvoiceAllDistributionTree** page is used to design the distributions page for mobile (as in scenario 1), it might be confusing for the user to correlate lines to distributions.</span></span> <span data-ttu-id="360c1-413">Daher verwenden Sie die **VendMobileInvoiceLineDistributionTree** Seite, um die Verteilungsseite zu entwerfen.</span><span class="sxs-lookup"><span data-stu-id="360c1-413">Therefore, use the **VendMobileInvoiceLineDistributionTree** page to design the distributions page.</span></span>
    3.  <span data-ttu-id="360c1-414">Im Idealfall sollten die Verteilungen im Kontext einer Rechnungsposition in diesem Szenario angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="360c1-414">Ideally, the distributions should be shown in the context of an invoice line in this scenario.</span></span> <span data-ttu-id="360c1-415">Daher müssen Sie unbedingt, ob der Benutzer in einer Position richten bohren kann, um die Verteilungsseite anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="360c1-415">Therefore, make sure that the user can drill into a line to see the distributions page.</span></span> <span data-ttu-id="360c1-416">Verwenden Sie die Seitenlinkfunktion, den Drillthrough einzurichten, wie Sie für den Kopf und die Detailseiten in Szenario 1. ".</span><span class="sxs-lookup"><span data-stu-id="360c1-416">Use the page link capability to establish the drill-through, just as you did for the header and details pages in scenario 1.</span></span>

2.  <span data-ttu-id="360c1-417">Da mehrere ein Betragsart für die Verteilungen in Szenario 2 (Mehrwertsteuer, Belastungen usw.) erwartet wird, ist es hilfreich, die Beschreibung des Betrags Typ anzeigen.</span><span class="sxs-lookup"><span data-stu-id="360c1-417">Because more than one amount type is expected on the distributions in scenario 2 (sales tax, charges, and so on), it will be useful to show the description of the amount type.</span></span> <span data-ttu-id="360c1-418">(Wir haben diese Informationen in Szenario 1 ausgelassen.)</span><span class="sxs-lookup"><span data-stu-id="360c1-418">(We omitted this information in scenario 1.)</span></span>




