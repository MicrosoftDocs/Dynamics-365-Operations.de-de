--- 
title: Einrichten von Anlagenbuchungsprofilen
description: Mit dieser Aufgabenanleitung werden "Anlagenbuchungsprofile" eingerichtet.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 286c8732c1f2c92d0f16582b0b9de41990280e5a
ms.contentlocale: de-de
ms.lasthandoff: 09/14/2018

---
# <a name="set-up-fixed-asset-posting-profiles"></a><span data-ttu-id="d53fe-103">Einrichten von Anlagenbuchungsprofilen</span><span class="sxs-lookup"><span data-stu-id="d53fe-103">Set up fixed asset posting profiles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d53fe-104">Mit dieser Aufgabenanleitung werden "Anlagenbuchungsprofile" eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="d53fe-104">This task guide will set up Fixed asset posting profiles.</span></span>  <span data-ttu-id="d53fe-105">Dabei werden die "Buchhalterrolle" und die Demodaten für die juristische Person USMF verwendet.</span><span class="sxs-lookup"><span data-stu-id="d53fe-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>  <span data-ttu-id="d53fe-106">Die Beispiele, die in der Aufgabenanleitung angegeben sind, sind für ein grundlegendes Buchungsprofil, obwohl Buchungsprofile für Ihren speziellen Kontenplans und Ihre Finanzberichterstellungsanforderungen erstellt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="d53fe-106">Examples given in the task guide are for a basic posting profile, though posting profiles must be created for your specific chart of accounts and financial reporting requirements.</span></span>

1. <span data-ttu-id="d53fe-107">Wechseln Sie zu Anlagen > Einstellungen > Anlagenbuchungsprofile.</span><span class="sxs-lookup"><span data-stu-id="d53fe-107">Go to Fixed assets > Setup > Fixed asset posting profiles.</span></span>
2. <span data-ttu-id="d53fe-108">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="d53fe-108">Click New.</span></span>
3. <span data-ttu-id="d53fe-109">Geben Sie im Feld "Buchungsprofil" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="d53fe-109">In the Posting profile field, type a value.</span></span>
4. <span data-ttu-id="d53fe-110">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="d53fe-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="d53fe-111">Sie müssen ein Buchungsprofil für jeden Anlagentransaktionstyp erstellen, den Sie beim Arbeiten mit Anlagen verwenden.</span><span class="sxs-lookup"><span data-stu-id="d53fe-111">You will need to create a posting profile for each fixed asset transaction type you will be using when working with fixed assets.</span></span>  <span data-ttu-id="d53fe-112">Diese Aufgabenanleitung beginnt mit dem Transaktionstyp "Anschaffung".</span><span class="sxs-lookup"><span data-stu-id="d53fe-112">This task guide will start with the Acquisition transaction type.</span></span>  
5. <span data-ttu-id="d53fe-113">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d53fe-113">Click Add.</span></span>
6. <span data-ttu-id="d53fe-114">Geben Sie im Feld 'Buch' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="d53fe-114">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="d53fe-115">Das Feld "Gruppierungen" ermöglicht es Ihnen, das Buchungsprofil hinunter zur "Tabelle" (ein Konto, das für jede Anlage eingerichtet wird) oder "Gruppe" (ein Konto, das für jede Anlagengruppe eingerichtet ist) zu definieren.</span><span class="sxs-lookup"><span data-stu-id="d53fe-115">The Groupings field allows you to define the posting profile down to the Table (one account set up for each fixed asset) or Group (one account set up for each fixed asset group).</span></span>  <span data-ttu-id="d53fe-116">Für diesen Aufgabenleitfaden lasse ich den Wert auf „Alle” festgelegt, damit er für alle Anlagen mit dem angegebenen Buch angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="d53fe-116">For this task guide I will leave the value set to “All” to apply to all fixed assets with the specified Book.</span></span>  
7. <span data-ttu-id="d53fe-117">Geben Sie im Feld "Hauptkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="d53fe-117">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="d53fe-118">Für "Anschaffungen" können Sie ein Gegenkonto eingeben oder es leer lassen, damit es für die spezielle Transaktion ausgefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="d53fe-118">For Acquisitions, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>    
8. <span data-ttu-id="d53fe-119">Wählen Sie im Feld "Transaktionstyp" die Option "Anschaffungsregulierung" aus.</span><span class="sxs-lookup"><span data-stu-id="d53fe-119">In the Transaction type field, select 'Acquisition adjustment'.</span></span>
    * <span data-ttu-id="d53fe-120">Für "Anschaffungsregulierungstransaktionen" verwenden wir dieselben Konten, die für "Anschaffungstransaktionen" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d53fe-120">For Acquisition adjustment transactions, we will use the same accounts as used for Acquisition transactions.</span></span>  
9. <span data-ttu-id="d53fe-121">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d53fe-121">Click Add.</span></span>
10. <span data-ttu-id="d53fe-122">Geben Sie im Feld 'Buch' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="d53fe-122">In the Book field, enter or select a value.</span></span>
11. <span data-ttu-id="d53fe-123">Geben Sie im Feld "Hauptkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="d53fe-123">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="d53fe-124">Für "Anschaffungsregulierungen" können Sie ein Gegenkonto eingeben oder es leer lassen, damit es für die spezielle Transaktion ausgefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="d53fe-124">For Acquisition adjustments, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>    
12. <span data-ttu-id="d53fe-125">Wählen Sie im Feld "Transaktionstyp" die Option "Abschreibung" aus.</span><span class="sxs-lookup"><span data-stu-id="d53fe-125">In the Transaction type field, select 'Depreciation'.</span></span>
13. <span data-ttu-id="d53fe-126">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d53fe-126">Click Add.</span></span>
14. <span data-ttu-id="d53fe-127">Geben Sie im Feld 'Buch' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="d53fe-127">In the Book field, enter or select a value.</span></span>
15. <span data-ttu-id="d53fe-128">Geben Sie im Feld "Hauptkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="d53fe-128">In the Main account field, specify the desired values.</span></span>
16. <span data-ttu-id="d53fe-129">Geben Sie im Feld "Gegenkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="d53fe-129">In the Offset account field, specify the desired values.</span></span>
17. <span data-ttu-id="d53fe-130">Wählen Sie im Feld "Transaktionstyp" die Option "Abschreibungsregulierung" aus.</span><span class="sxs-lookup"><span data-stu-id="d53fe-130">In the Transaction type field, select 'Depreciation adjustment'.</span></span>
    * <span data-ttu-id="d53fe-131">Für "Abschreibungsregulierungstransaktionen" verwenden wir dieselben Konten, die für "Abschreibungstransaktionen" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d53fe-131">For Depreciation adjustment transactions, we will use the same accounts as used for Depreciation transactions.</span></span>  
18. <span data-ttu-id="d53fe-132">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d53fe-132">Click Add.</span></span>
19. <span data-ttu-id="d53fe-133">Geben Sie im Feld 'Buch' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="d53fe-133">In the Book field, enter or select a value.</span></span>
20. <span data-ttu-id="d53fe-134">Geben Sie im Feld "Hauptkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="d53fe-134">In the Main account field, specify the desired values.</span></span>
21. <span data-ttu-id="d53fe-135">Geben Sie im Feld "Gegenkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="d53fe-135">In the Offset account field, specify the desired values.</span></span>
22. <span data-ttu-id="d53fe-136">Wählen Sie im Feld "Transaktionstyp" die Option "Veräußerung" aus.</span><span class="sxs-lookup"><span data-stu-id="d53fe-136">In the Transaction type field, select 'Disposal - sale'.</span></span>
23. <span data-ttu-id="d53fe-137">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d53fe-137">Click Add.</span></span>
24. <span data-ttu-id="d53fe-138">Geben Sie im Feld 'Buch' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="d53fe-138">In the Book field, enter or select a value.</span></span>
25. <span data-ttu-id="d53fe-139">Geben Sie im Feld "Hauptkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="d53fe-139">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="d53fe-140">Für "Veräußerungen" können Sie ein Gegenkonto eingeben oder es leer lassen, damit es für die spezielle Transaktion ausgefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="d53fe-140">For Disposals, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>  
26. <span data-ttu-id="d53fe-141">Wählen Sie im Feld "Transaktionstyp" die Option "Verschrottung" aus.</span><span class="sxs-lookup"><span data-stu-id="d53fe-141">In the Transaction type field, select 'Disposal - scrap'.</span></span>
    * <span data-ttu-id="d53fe-142">Wir verwenden dieselben Konten für "Veräußerung" und "Verschrottung".</span><span class="sxs-lookup"><span data-stu-id="d53fe-142">We will use the same accounts for Disposal sale and Disposal scrap.</span></span>  
27. <span data-ttu-id="d53fe-143">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d53fe-143">Click Add.</span></span>
28. <span data-ttu-id="d53fe-144">Geben Sie im Feld 'Buch' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="d53fe-144">In the Book field, enter or select a value.</span></span>
29. <span data-ttu-id="d53fe-145">Geben Sie im Feld "Hauptkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="d53fe-145">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="d53fe-146">Für "Veräußerungen" können Sie ein Gegenkonto eingeben oder es leer lassen, damit es für die spezielle Transaktion ausgefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="d53fe-146">For Disposals, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>  
30. <span data-ttu-id="d53fe-147">Erweitern Sie den Abschnitt „Abgang”.</span><span class="sxs-lookup"><span data-stu-id="d53fe-147">Expand the Disposal section.</span></span>
    * <span data-ttu-id="d53fe-148">Sie müssen Veräußerungsbuchungsprofile sowohl für Veräußerung als auch Verschrottung einrichten.</span><span class="sxs-lookup"><span data-stu-id="d53fe-148">You must set up disposal posting profiles for both sale and scrap.</span></span>  <span data-ttu-id="d53fe-149">Wir beginnen mit Veräußerungsverkaufstransaktionen.</span><span class="sxs-lookup"><span data-stu-id="d53fe-149">We will start with disposal sale transactions.</span></span>  
31. <span data-ttu-id="d53fe-150">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d53fe-150">Click Add.</span></span>
32. <span data-ttu-id="d53fe-151">Geben Sie im Feld 'Buch' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="d53fe-151">In the Book field, enter or select a value.</span></span>
33. <span data-ttu-id="d53fe-152">Wählen Sie im Feld "Buchungswert" die Option "Anschaffungswert" aus.</span><span class="sxs-lookup"><span data-stu-id="d53fe-152">In the Post value field, select 'Acquisition value'.</span></span>
    * <span data-ttu-id="d53fe-153">Anschaffungswert adressiert Anschaffungs- und Anschaffungsregulierungswerte für alle Jahre.</span><span class="sxs-lookup"><span data-stu-id="d53fe-153">Acquisition value will address Acquisition and Acquisition adjustment values for all years.</span></span>  <span data-ttu-id="d53fe-154">Sie können auch Konten für diese Transaktionsarten getrennt definieren.</span><span class="sxs-lookup"><span data-stu-id="d53fe-154">You can also define accounts for these transaction types separately.</span></span>  
    * <span data-ttu-id="d53fe-155">Sie können den Veräußerungsprozess so festlegen, dass er verschiedene Konten verwendet, je nachdem, ob die Veräußerung einen Gewinn oder Verlust ergibt.</span><span class="sxs-lookup"><span data-stu-id="d53fe-155">You can set the disposal process to use different accounts depending upon if the disposal results in a gain or loss.</span></span>  <span data-ttu-id="d53fe-156">Ich werde den "Verkaufswerttyp" auf "Alle" festlegen, um die gleichen Konten für alle Typen von Veräußerungen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="d53fe-156">I will set the Sales value type to “All” to use the same accounts for all types of disposals.</span></span>  
34. <span data-ttu-id="d53fe-157">Geben Sie im Feld "Hauptkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="d53fe-157">In the Main account field, specify the desired values.</span></span>
35. <span data-ttu-id="d53fe-158">Geben Sie im Feld "Gegenkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="d53fe-158">In the Offset account field, specify the desired values.</span></span>
36. <span data-ttu-id="d53fe-159">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d53fe-159">Click Add.</span></span>
37. <span data-ttu-id="d53fe-160">Geben Sie im Feld 'Buch' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="d53fe-160">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="d53fe-161">Wählen Sie im Feld "Wert buchen" die Option "Abschreibung (frühere Jahre)" aus.</span><span class="sxs-lookup"><span data-stu-id="d53fe-161">In the Post value field, select 'Depreciation (prior years)'.</span></span>  
38. <span data-ttu-id="d53fe-162">Geben Sie im Feld "Hauptkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="d53fe-162">In the Main account field, specify the desired values.</span></span>
39. <span data-ttu-id="d53fe-163">Geben Sie im Feld "Gegenkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="d53fe-163">In the Offset account field, specify the desired values.</span></span>
40. <span data-ttu-id="d53fe-164">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d53fe-164">Click Add.</span></span>
41. <span data-ttu-id="d53fe-165">Geben Sie im Feld 'Buch' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="d53fe-165">In the Book field, enter or select a value.</span></span>
42. <span data-ttu-id="d53fe-166">Wählen Sie im Feld "Wert buchen" die Option "Abschreibung (dieses Jahr)" aus.</span><span class="sxs-lookup"><span data-stu-id="d53fe-166">In the Post value field, select 'Depreciation (this year)'.</span></span>
43. <span data-ttu-id="d53fe-167">Geben Sie im Feld "Hauptkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="d53fe-167">In the Main account field, specify the desired values.</span></span>
44. <span data-ttu-id="d53fe-168">Geben Sie im Feld "Gegenkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="d53fe-168">In the Offset account field, specify the desired values.</span></span>
45. <span data-ttu-id="d53fe-169">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d53fe-169">Click Add.</span></span>
46. <span data-ttu-id="d53fe-170">Geben Sie im Feld 'Buch' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="d53fe-170">In the Book field, enter or select a value.</span></span>
47. <span data-ttu-id="d53fe-171">Wählen Sie im Feld "Wert buchen" die Option "Abschreibungsregulierungen (frühere Jahre)" aus.</span><span class="sxs-lookup"><span data-stu-id="d53fe-171">In the Post value field, select 'Depreciation adjustments (prior years)'.</span></span>
48. <span data-ttu-id="d53fe-172">Geben Sie im Feld "Hauptkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="d53fe-172">In the Main account field, specify the desired values.</span></span>
49. <span data-ttu-id="d53fe-173">Geben Sie im Feld "Gegenkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="d53fe-173">In the Offset account field, specify the desired values.</span></span>
50. <span data-ttu-id="d53fe-174">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d53fe-174">Click Add.</span></span>
51. <span data-ttu-id="d53fe-175">Geben Sie im Feld 'Buch' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="d53fe-175">In the Book field, enter or select a value.</span></span>
52. <span data-ttu-id="d53fe-176">Wählen Sie im Feld "Wert buchen" die Option "Abschreibungsregulierungen (dieses Jahr)" aus.</span><span class="sxs-lookup"><span data-stu-id="d53fe-176">In the Post value field, select 'Depreciation adjustments (this year)'.</span></span>
53. <span data-ttu-id="d53fe-177">Geben Sie im Feld "Hauptkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="d53fe-177">In the Main account field, specify the desired values.</span></span>
54. <span data-ttu-id="d53fe-178">Geben Sie im Feld "Gegenkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="d53fe-178">In the Offset account field, specify the desired values.</span></span>
55. <span data-ttu-id="d53fe-179">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d53fe-179">Click Add.</span></span>
56. <span data-ttu-id="d53fe-180">Geben Sie im Feld 'Buch' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="d53fe-180">In the Book field, enter or select a value.</span></span>
57. <span data-ttu-id="d53fe-181">Wählen Sie im Feld "Buchungswert" die Option "Nettobuchwert" aus.</span><span class="sxs-lookup"><span data-stu-id="d53fe-181">In the Post value field, select 'Net book value'.</span></span>
58. <span data-ttu-id="d53fe-182">Geben Sie im Feld "Hauptkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="d53fe-182">In the Main account field, specify the desired values.</span></span>
59. <span data-ttu-id="d53fe-183">Geben Sie im Feld "Gegenkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="d53fe-183">In the Offset account field, specify the desired values.</span></span>
60. <span data-ttu-id="d53fe-184">Wählen Sie im Feld "Veräußerung oder Verschrottung" die Option "Verschrottung" aus.</span><span class="sxs-lookup"><span data-stu-id="d53fe-184">In the Sale or scrap field, select 'Scrap'.</span></span>
61. <span data-ttu-id="d53fe-185">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d53fe-185">Click Add.</span></span>
62. <span data-ttu-id="d53fe-186">Geben Sie im Feld 'Buch' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="d53fe-186">In the Book field, enter or select a value.</span></span>
63. <span data-ttu-id="d53fe-187">Wählen Sie im Feld "Buchungswert" die Option "Anschaffungswert" aus.</span><span class="sxs-lookup"><span data-stu-id="d53fe-187">In the Post value field, select 'Acquisition value'.</span></span>
64. <span data-ttu-id="d53fe-188">Geben Sie im Feld "Hauptkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="d53fe-188">In the Main account field, specify the desired values.</span></span>
65. <span data-ttu-id="d53fe-189">Geben Sie im Feld "Gegenkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="d53fe-189">In the Offset account field, specify the desired values.</span></span>
66. <span data-ttu-id="d53fe-190">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d53fe-190">Click Add.</span></span>
67. <span data-ttu-id="d53fe-191">Geben Sie im Feld 'Buch' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="d53fe-191">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="d53fe-192">Wählen Sie im Feld "Wert buchen" die Option "Abschreibung (frühere Jahre)" aus.</span><span class="sxs-lookup"><span data-stu-id="d53fe-192">In Post value field, select 'Depreciation (prior years)'.</span></span>  
68. <span data-ttu-id="d53fe-193">Geben Sie im Feld "Hauptkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="d53fe-193">In the Main account field, specify the desired values.</span></span>
69. <span data-ttu-id="d53fe-194">Geben Sie im Feld "Gegenkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="d53fe-194">In the Offset account field, specify the desired values.</span></span>
70. <span data-ttu-id="d53fe-195">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d53fe-195">Click Add.</span></span>
71. <span data-ttu-id="d53fe-196">Geben Sie im Feld 'Buch' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="d53fe-196">In the Book field, enter or select a value.</span></span>
72. <span data-ttu-id="d53fe-197">Wählen Sie im Feld "Wert buchen" die Option "Abschreibung (dieses Jahr)" aus.</span><span class="sxs-lookup"><span data-stu-id="d53fe-197">In the Post value field, select 'Depreciation (this year)'.</span></span>
73. <span data-ttu-id="d53fe-198">Geben Sie im Feld "Hauptkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="d53fe-198">In the Main account field, specify the desired values.</span></span>
74. <span data-ttu-id="d53fe-199">Geben Sie im Feld "Gegenkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="d53fe-199">In the Offset account field, specify the desired values.</span></span>
75. <span data-ttu-id="d53fe-200">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d53fe-200">Click Add.</span></span>
76. <span data-ttu-id="d53fe-201">Geben Sie im Feld 'Buch' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="d53fe-201">In the Book field, enter or select a value.</span></span>
77. <span data-ttu-id="d53fe-202">Wählen Sie im Feld "Wert buchen" die Option "Abschreibungsregulierungen (frühere Jahre)" aus.</span><span class="sxs-lookup"><span data-stu-id="d53fe-202">In the Post value field, select 'Depreciation adjustments (prior years)'.</span></span>
78. <span data-ttu-id="d53fe-203">Geben Sie im Feld "Hauptkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="d53fe-203">In the Main account field, specify the desired values.</span></span>
79. <span data-ttu-id="d53fe-204">Geben Sie im Feld "Gegenkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="d53fe-204">In the Offset account field, specify the desired values.</span></span>
80. <span data-ttu-id="d53fe-205">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d53fe-205">Click Add.</span></span>
81. <span data-ttu-id="d53fe-206">Geben Sie im Feld 'Buch' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="d53fe-206">In the Book field, enter or select a value.</span></span>
82. <span data-ttu-id="d53fe-207">Wählen Sie im Feld "Wert buchen" die Option "Abschreibungsregulierungen (dieses Jahr)" aus.</span><span class="sxs-lookup"><span data-stu-id="d53fe-207">In the Post value field, select 'Depreciation adjustments (this year)'.</span></span>
83. <span data-ttu-id="d53fe-208">Geben Sie im Feld "Hauptkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="d53fe-208">In the Main account field, specify the desired values.</span></span>
84. <span data-ttu-id="d53fe-209">Geben Sie im Feld "Gegenkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="d53fe-209">In the Offset account field, specify the desired values.</span></span>
85. <span data-ttu-id="d53fe-210">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d53fe-210">Click Add.</span></span>
86. <span data-ttu-id="d53fe-211">Geben Sie im Feld 'Buch' einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="d53fe-211">In the Book field, enter or select a value.</span></span>
87. <span data-ttu-id="d53fe-212">Wählen Sie im Feld "Buchungswert" die Option "Nettobuchwert" aus.</span><span class="sxs-lookup"><span data-stu-id="d53fe-212">In the Post value field, select 'Net book value'.</span></span>
88. <span data-ttu-id="d53fe-213">Geben Sie im Feld "Hauptkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="d53fe-213">In the Main account field, specify the desired values.</span></span>
89. <span data-ttu-id="d53fe-214">Geben Sie im Feld "Gegenkonto" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="d53fe-214">In the Offset account field, specify the desired values.</span></span>


