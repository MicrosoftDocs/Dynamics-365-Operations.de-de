---
title: Einrichten von Anlagenbuchungsprofilen
description: Mit dieser Aufgabenanleitung werden "Anlagenbuchungsprofile" eingerichtet.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 286c8732c1f2c92d0f16582b0b9de41990280e5a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "351101"
---
# <a name="set-up-fixed-asset-posting-profiles"></a><span data-ttu-id="a2d06-103">Einrichten von Anlagenbuchungsprofilen</span><span class="sxs-lookup"><span data-stu-id="a2d06-103">Set up fixed asset posting profiles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a2d06-104">Mit dieser Aufgabenanleitung werden "Anlagenbuchungsprofile" eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="a2d06-104">This task guide will set up Fixed asset posting profiles.</span></span>  <span data-ttu-id="a2d06-105">Dabei werden die "Buchhalterrolle" und die Demodaten für die juristische Person USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="a2d06-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>  <span data-ttu-id="a2d06-106">Die Beispiele, die in der Aufgabenanleitung angegeben sind, sind für ein grundlegendes Buchungsprofil, obwohl Buchungsprofile für Ihren speziellen Kontenplans und Ihre Finanzberichterstellungsanforderungen erstellt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="a2d06-106">Examples given in the task guide are for a basic posting profile, though posting profiles must be created for your specific chart of accounts and financial reporting requirements.</span></span>

1. <span data-ttu-id="a2d06-107">Wechseln Sie zu Anlagen > Einstellungen > Anlagenbuchungsprofile.</span><span class="sxs-lookup"><span data-stu-id="a2d06-107">Go to Fixed assets > Setup > Fixed asset posting profiles.</span></span>
2. <span data-ttu-id="a2d06-108">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="a2d06-108">Click New.</span></span>
3. <span data-ttu-id="a2d06-109">Geben Sie im Feld "Buchungsprofil" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="a2d06-109">In the Posting profile field, type a value.</span></span>
4. <span data-ttu-id="a2d06-110">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="a2d06-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="a2d06-111">Sie müssen ein Buchungsprofil für jeden Anlagentransaktionstyp erstellen, den Sie beim Arbeiten mit Anlagen verwenden.</span><span class="sxs-lookup"><span data-stu-id="a2d06-111">You will need to create a posting profile for each fixed asset transaction type you will be using when working with fixed assets.</span></span>  <span data-ttu-id="a2d06-112">Diese Aufgabenanleitung beginnt mit dem Transaktionstyp "Anschaffung".</span><span class="sxs-lookup"><span data-stu-id="a2d06-112">This task guide will start with the Acquisition transaction type.</span></span>  
5. <span data-ttu-id="a2d06-113">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="a2d06-113">Click Add.</span></span>
6. <span data-ttu-id="a2d06-114">Geben Sie im Feld 'Buch' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="a2d06-114">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="a2d06-115">Das Feld "Gruppierungen" ermöglicht es Ihnen, das Buchungsprofil hinunter zur "Tabelle" (ein Konto, das für jede Anlage eingerichtet wird) oder "Gruppe" (ein Konto, das für jede Anlagengruppe eingerichtet ist) zu definieren.</span><span class="sxs-lookup"><span data-stu-id="a2d06-115">The Groupings field allows you to define the posting profile down to the Table (one account set up for each fixed asset) or Group (one account set up for each fixed asset group).</span></span>  <span data-ttu-id="a2d06-116">Für diesen Aufgabenleitfaden lasse ich den Wert auf „Alle” festgelegt, damit er für alle Anlagen mit dem angegebenen Buch angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="a2d06-116">For this task guide I will leave the value set to “All” to apply to all fixed assets with the specified Book.</span></span>  
7. <span data-ttu-id="a2d06-117">Geben Sie im Feld "Hauptkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="a2d06-117">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="a2d06-118">Für "Anschaffungen" können Sie ein Gegenkonto eingeben oder es leer lassen, damit es für die spezielle Transaktion ausgefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="a2d06-118">For Acquisitions, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>    
8. <span data-ttu-id="a2d06-119">Wählen Sie im Feld "Transaktionstyp" die Option "Anschaffungsregulierung" aus.</span><span class="sxs-lookup"><span data-stu-id="a2d06-119">In the Transaction type field, select 'Acquisition adjustment'.</span></span>
    * <span data-ttu-id="a2d06-120">Für "Anschaffungsregulierungstransaktionen" verwenden wir dieselben Konten, die für "Anschaffungstransaktionen" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a2d06-120">For Acquisition adjustment transactions, we will use the same accounts as used for Acquisition transactions.</span></span>  
9. <span data-ttu-id="a2d06-121">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="a2d06-121">Click Add.</span></span>
10. <span data-ttu-id="a2d06-122">Geben Sie im Feld 'Buch' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="a2d06-122">In the Book field, enter or select a value.</span></span>
11. <span data-ttu-id="a2d06-123">Geben Sie im Feld "Hauptkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="a2d06-123">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="a2d06-124">Für "Anschaffungsregulierungen" können Sie ein Gegenkonto eingeben oder es leer lassen, damit es für die spezielle Transaktion ausgefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="a2d06-124">For Acquisition adjustments, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>    
12. <span data-ttu-id="a2d06-125">Wählen Sie im Feld "Transaktionstyp" die Option "Abschreibung" aus.</span><span class="sxs-lookup"><span data-stu-id="a2d06-125">In the Transaction type field, select 'Depreciation'.</span></span>
13. <span data-ttu-id="a2d06-126">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="a2d06-126">Click Add.</span></span>
14. <span data-ttu-id="a2d06-127">Geben Sie im Feld 'Buch' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="a2d06-127">In the Book field, enter or select a value.</span></span>
15. <span data-ttu-id="a2d06-128">Geben Sie im Feld "Hauptkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="a2d06-128">In the Main account field, specify the desired values.</span></span>
16. <span data-ttu-id="a2d06-129">Geben Sie im Feld "Gegenkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="a2d06-129">In the Offset account field, specify the desired values.</span></span>
17. <span data-ttu-id="a2d06-130">Wählen Sie im Feld "Transaktionstyp" die Option "Abschreibungsregulierung" aus.</span><span class="sxs-lookup"><span data-stu-id="a2d06-130">In the Transaction type field, select 'Depreciation adjustment'.</span></span>
    * <span data-ttu-id="a2d06-131">Für "Abschreibungsregulierungstransaktionen" verwenden wir dieselben Konten, die für "Abschreibungstransaktionen" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a2d06-131">For Depreciation adjustment transactions, we will use the same accounts as used for Depreciation transactions.</span></span>  
18. <span data-ttu-id="a2d06-132">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="a2d06-132">Click Add.</span></span>
19. <span data-ttu-id="a2d06-133">Geben Sie im Feld 'Buch' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="a2d06-133">In the Book field, enter or select a value.</span></span>
20. <span data-ttu-id="a2d06-134">Geben Sie im Feld "Hauptkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="a2d06-134">In the Main account field, specify the desired values.</span></span>
21. <span data-ttu-id="a2d06-135">Geben Sie im Feld "Gegenkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="a2d06-135">In the Offset account field, specify the desired values.</span></span>
22. <span data-ttu-id="a2d06-136">Wählen Sie im Feld "Transaktionstyp" die Option "Veräußerung" aus.</span><span class="sxs-lookup"><span data-stu-id="a2d06-136">In the Transaction type field, select 'Disposal - sale'.</span></span>
23. <span data-ttu-id="a2d06-137">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="a2d06-137">Click Add.</span></span>
24. <span data-ttu-id="a2d06-138">Geben Sie im Feld 'Buch' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="a2d06-138">In the Book field, enter or select a value.</span></span>
25. <span data-ttu-id="a2d06-139">Geben Sie im Feld "Hauptkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="a2d06-139">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="a2d06-140">Für "Veräußerungen" können Sie ein Gegenkonto eingeben oder es leer lassen, damit es für die spezielle Transaktion ausgefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="a2d06-140">For Disposals, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>  
26. <span data-ttu-id="a2d06-141">Wählen Sie im Feld "Transaktionstyp" die Option "Verschrottung" aus.</span><span class="sxs-lookup"><span data-stu-id="a2d06-141">In the Transaction type field, select 'Disposal - scrap'.</span></span>
    * <span data-ttu-id="a2d06-142">Wir verwenden dieselben Konten für "Veräußerung" und "Verschrottung".</span><span class="sxs-lookup"><span data-stu-id="a2d06-142">We will use the same accounts for Disposal sale and Disposal scrap.</span></span>  
27. <span data-ttu-id="a2d06-143">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="a2d06-143">Click Add.</span></span>
28. <span data-ttu-id="a2d06-144">Geben Sie im Feld 'Buch' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="a2d06-144">In the Book field, enter or select a value.</span></span>
29. <span data-ttu-id="a2d06-145">Geben Sie im Feld "Hauptkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="a2d06-145">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="a2d06-146">Für "Veräußerungen" können Sie ein Gegenkonto eingeben oder es leer lassen, damit es für die spezielle Transaktion ausgefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="a2d06-146">For Disposals, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>  
30. <span data-ttu-id="a2d06-147">Erweitern Sie den Abschnitt „Abgang”.</span><span class="sxs-lookup"><span data-stu-id="a2d06-147">Expand the Disposal section.</span></span>
    * <span data-ttu-id="a2d06-148">Sie müssen Veräußerungsbuchungsprofile sowohl für Veräußerung als auch Verschrottung einrichten.</span><span class="sxs-lookup"><span data-stu-id="a2d06-148">You must set up disposal posting profiles for both sale and scrap.</span></span>  <span data-ttu-id="a2d06-149">Wir beginnen mit Veräußerungsverkaufstransaktionen.</span><span class="sxs-lookup"><span data-stu-id="a2d06-149">We will start with disposal sale transactions.</span></span>  
31. <span data-ttu-id="a2d06-150">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="a2d06-150">Click Add.</span></span>
32. <span data-ttu-id="a2d06-151">Geben Sie im Feld 'Buch' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="a2d06-151">In the Book field, enter or select a value.</span></span>
33. <span data-ttu-id="a2d06-152">Wählen Sie im Feld "Buchungswert" die Option "Anschaffungswert" aus.</span><span class="sxs-lookup"><span data-stu-id="a2d06-152">In the Post value field, select 'Acquisition value'.</span></span>
    * <span data-ttu-id="a2d06-153">Anschaffungswert adressiert Anschaffungs- und Anschaffungsregulierungswerte für alle Jahre.</span><span class="sxs-lookup"><span data-stu-id="a2d06-153">Acquisition value will address Acquisition and Acquisition adjustment values for all years.</span></span>  <span data-ttu-id="a2d06-154">Sie können auch Konten für diese Transaktionsarten getrennt definieren.</span><span class="sxs-lookup"><span data-stu-id="a2d06-154">You can also define accounts for these transaction types separately.</span></span>  
    * <span data-ttu-id="a2d06-155">Sie können den Veräußerungsprozess so festlegen, dass er verschiedene Konten verwendet, je nachdem, ob die Veräußerung einen Gewinn oder Verlust ergibt.</span><span class="sxs-lookup"><span data-stu-id="a2d06-155">You can set the disposal process to use different accounts depending upon if the disposal results in a gain or loss.</span></span>  <span data-ttu-id="a2d06-156">Ich werde den "Verkaufswerttyp" auf "Alle" festlegen, um die gleichen Konten für alle Typen von Veräußerungen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="a2d06-156">I will set the Sales value type to “All” to use the same accounts for all types of disposals.</span></span>  
34. <span data-ttu-id="a2d06-157">Geben Sie im Feld "Hauptkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="a2d06-157">In the Main account field, specify the desired values.</span></span>
35. <span data-ttu-id="a2d06-158">Geben Sie im Feld "Gegenkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="a2d06-158">In the Offset account field, specify the desired values.</span></span>
36. <span data-ttu-id="a2d06-159">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="a2d06-159">Click Add.</span></span>
37. <span data-ttu-id="a2d06-160">Geben Sie im Feld 'Buch' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="a2d06-160">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="a2d06-161">Wählen Sie im Feld "Wert buchen" die Option "Abschreibung (frühere Jahre)" aus.</span><span class="sxs-lookup"><span data-stu-id="a2d06-161">In the Post value field, select 'Depreciation (prior years)'.</span></span>  
38. <span data-ttu-id="a2d06-162">Geben Sie im Feld "Hauptkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="a2d06-162">In the Main account field, specify the desired values.</span></span>
39. <span data-ttu-id="a2d06-163">Geben Sie im Feld "Gegenkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="a2d06-163">In the Offset account field, specify the desired values.</span></span>
40. <span data-ttu-id="a2d06-164">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="a2d06-164">Click Add.</span></span>
41. <span data-ttu-id="a2d06-165">Geben Sie im Feld 'Buch' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="a2d06-165">In the Book field, enter or select a value.</span></span>
42. <span data-ttu-id="a2d06-166">Wählen Sie im Feld "Wert buchen" die Option "Abschreibung (dieses Jahr)" aus.</span><span class="sxs-lookup"><span data-stu-id="a2d06-166">In the Post value field, select 'Depreciation (this year)'.</span></span>
43. <span data-ttu-id="a2d06-167">Geben Sie im Feld "Hauptkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="a2d06-167">In the Main account field, specify the desired values.</span></span>
44. <span data-ttu-id="a2d06-168">Geben Sie im Feld "Gegenkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="a2d06-168">In the Offset account field, specify the desired values.</span></span>
45. <span data-ttu-id="a2d06-169">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="a2d06-169">Click Add.</span></span>
46. <span data-ttu-id="a2d06-170">Geben Sie im Feld 'Buch' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="a2d06-170">In the Book field, enter or select a value.</span></span>
47. <span data-ttu-id="a2d06-171">Wählen Sie im Feld "Wert buchen" die Option "Abschreibungsregulierungen (frühere Jahre)" aus.</span><span class="sxs-lookup"><span data-stu-id="a2d06-171">In the Post value field, select 'Depreciation adjustments (prior years)'.</span></span>
48. <span data-ttu-id="a2d06-172">Geben Sie im Feld "Hauptkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="a2d06-172">In the Main account field, specify the desired values.</span></span>
49. <span data-ttu-id="a2d06-173">Geben Sie im Feld "Gegenkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="a2d06-173">In the Offset account field, specify the desired values.</span></span>
50. <span data-ttu-id="a2d06-174">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="a2d06-174">Click Add.</span></span>
51. <span data-ttu-id="a2d06-175">Geben Sie im Feld 'Buch' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="a2d06-175">In the Book field, enter or select a value.</span></span>
52. <span data-ttu-id="a2d06-176">Wählen Sie im Feld "Wert buchen" die Option "Abschreibungsregulierungen (dieses Jahr)" aus.</span><span class="sxs-lookup"><span data-stu-id="a2d06-176">In the Post value field, select 'Depreciation adjustments (this year)'.</span></span>
53. <span data-ttu-id="a2d06-177">Geben Sie im Feld "Hauptkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="a2d06-177">In the Main account field, specify the desired values.</span></span>
54. <span data-ttu-id="a2d06-178">Geben Sie im Feld "Gegenkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="a2d06-178">In the Offset account field, specify the desired values.</span></span>
55. <span data-ttu-id="a2d06-179">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="a2d06-179">Click Add.</span></span>
56. <span data-ttu-id="a2d06-180">Geben Sie im Feld 'Buch' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="a2d06-180">In the Book field, enter or select a value.</span></span>
57. <span data-ttu-id="a2d06-181">Wählen Sie im Feld "Buchungswert" die Option "Nettobuchwert" aus.</span><span class="sxs-lookup"><span data-stu-id="a2d06-181">In the Post value field, select 'Net book value'.</span></span>
58. <span data-ttu-id="a2d06-182">Geben Sie im Feld "Hauptkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="a2d06-182">In the Main account field, specify the desired values.</span></span>
59. <span data-ttu-id="a2d06-183">Geben Sie im Feld "Gegenkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="a2d06-183">In the Offset account field, specify the desired values.</span></span>
60. <span data-ttu-id="a2d06-184">Wählen Sie im Feld "Veräußerung oder Verschrottung" die Option "Verschrottung" aus.</span><span class="sxs-lookup"><span data-stu-id="a2d06-184">In the Sale or scrap field, select 'Scrap'.</span></span>
61. <span data-ttu-id="a2d06-185">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="a2d06-185">Click Add.</span></span>
62. <span data-ttu-id="a2d06-186">Geben Sie im Feld 'Buch' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="a2d06-186">In the Book field, enter or select a value.</span></span>
63. <span data-ttu-id="a2d06-187">Wählen Sie im Feld "Buchungswert" die Option "Anschaffungswert" aus.</span><span class="sxs-lookup"><span data-stu-id="a2d06-187">In the Post value field, select 'Acquisition value'.</span></span>
64. <span data-ttu-id="a2d06-188">Geben Sie im Feld "Hauptkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="a2d06-188">In the Main account field, specify the desired values.</span></span>
65. <span data-ttu-id="a2d06-189">Geben Sie im Feld "Gegenkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="a2d06-189">In the Offset account field, specify the desired values.</span></span>
66. <span data-ttu-id="a2d06-190">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="a2d06-190">Click Add.</span></span>
67. <span data-ttu-id="a2d06-191">Geben Sie im Feld 'Buch' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="a2d06-191">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="a2d06-192">Wählen Sie im Feld "Wert buchen" die Option "Abschreibung (frühere Jahre)" aus.</span><span class="sxs-lookup"><span data-stu-id="a2d06-192">In Post value field, select 'Depreciation (prior years)'.</span></span>  
68. <span data-ttu-id="a2d06-193">Geben Sie im Feld "Hauptkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="a2d06-193">In the Main account field, specify the desired values.</span></span>
69. <span data-ttu-id="a2d06-194">Geben Sie im Feld "Gegenkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="a2d06-194">In the Offset account field, specify the desired values.</span></span>
70. <span data-ttu-id="a2d06-195">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="a2d06-195">Click Add.</span></span>
71. <span data-ttu-id="a2d06-196">Geben Sie im Feld 'Buch' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="a2d06-196">In the Book field, enter or select a value.</span></span>
72. <span data-ttu-id="a2d06-197">Wählen Sie im Feld "Wert buchen" die Option "Abschreibung (dieses Jahr)" aus.</span><span class="sxs-lookup"><span data-stu-id="a2d06-197">In the Post value field, select 'Depreciation (this year)'.</span></span>
73. <span data-ttu-id="a2d06-198">Geben Sie im Feld "Hauptkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="a2d06-198">In the Main account field, specify the desired values.</span></span>
74. <span data-ttu-id="a2d06-199">Geben Sie im Feld "Gegenkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="a2d06-199">In the Offset account field, specify the desired values.</span></span>
75. <span data-ttu-id="a2d06-200">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="a2d06-200">Click Add.</span></span>
76. <span data-ttu-id="a2d06-201">Geben Sie im Feld 'Buch' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="a2d06-201">In the Book field, enter or select a value.</span></span>
77. <span data-ttu-id="a2d06-202">Wählen Sie im Feld "Wert buchen" die Option "Abschreibungsregulierungen (frühere Jahre)" aus.</span><span class="sxs-lookup"><span data-stu-id="a2d06-202">In the Post value field, select 'Depreciation adjustments (prior years)'.</span></span>
78. <span data-ttu-id="a2d06-203">Geben Sie im Feld "Hauptkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="a2d06-203">In the Main account field, specify the desired values.</span></span>
79. <span data-ttu-id="a2d06-204">Geben Sie im Feld "Gegenkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="a2d06-204">In the Offset account field, specify the desired values.</span></span>
80. <span data-ttu-id="a2d06-205">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="a2d06-205">Click Add.</span></span>
81. <span data-ttu-id="a2d06-206">Geben Sie im Feld 'Buch' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="a2d06-206">In the Book field, enter or select a value.</span></span>
82. <span data-ttu-id="a2d06-207">Wählen Sie im Feld "Wert buchen" die Option "Abschreibungsregulierungen (dieses Jahr)" aus.</span><span class="sxs-lookup"><span data-stu-id="a2d06-207">In the Post value field, select 'Depreciation adjustments (this year)'.</span></span>
83. <span data-ttu-id="a2d06-208">Geben Sie im Feld "Hauptkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="a2d06-208">In the Main account field, specify the desired values.</span></span>
84. <span data-ttu-id="a2d06-209">Geben Sie im Feld "Gegenkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="a2d06-209">In the Offset account field, specify the desired values.</span></span>
85. <span data-ttu-id="a2d06-210">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="a2d06-210">Click Add.</span></span>
86. <span data-ttu-id="a2d06-211">Geben Sie im Feld 'Buch' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="a2d06-211">In the Book field, enter or select a value.</span></span>
87. <span data-ttu-id="a2d06-212">Wählen Sie im Feld "Buchungswert" die Option "Nettobuchwert" aus.</span><span class="sxs-lookup"><span data-stu-id="a2d06-212">In the Post value field, select 'Net book value'.</span></span>
88. <span data-ttu-id="a2d06-213">Geben Sie im Feld "Hauptkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="a2d06-213">In the Main account field, specify the desired values.</span></span>
89. <span data-ttu-id="a2d06-214">Geben Sie im Feld "Gegenkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="a2d06-214">In the Offset account field, specify the desired values.</span></span>

