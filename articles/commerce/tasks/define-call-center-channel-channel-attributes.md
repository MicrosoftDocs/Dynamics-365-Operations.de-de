---
title: Erstellen von Callcenter-Kanälen und Definieren von Kanalattributen
description: Dieses Verfahren führt Sie durch das Anlegen eines neuen Channels und das Definieren von Channel-Attributen.
author: mugunthanm
manager: AnnBe
ms.date: 05/22/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 59193d5d6a54fba89394e9700beb3b9596c47391
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976563"
---
# <a name="create-call-center-channels-and-define-channel-attributes"></a><span data-ttu-id="81ee4-103">Erstellen von Callcenter-Kanälen und Definieren von Kanalattributen</span><span class="sxs-lookup"><span data-stu-id="81ee4-103">Create call center channels and define channel attributes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="81ee4-104">Diese Prozedur führt Sie Schritt für Schritt durch das Erstellen eines neuen Kanals und das Konfigurieren von Kanalattributen.</span><span class="sxs-lookup"><span data-stu-id="81ee4-104">This procedure walks through creating a new commerce channel and defining channel attributes.</span></span> <span data-ttu-id="81ee4-105">Das Demodatenunternehmen, das verwendet wird, um diese Aufgabe zu erstellen, ist USRT.</span><span class="sxs-lookup"><span data-stu-id="81ee4-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="81ee4-106">Diese Prozedur ist für die Commerce-IT-Rolle bestimmt.</span><span class="sxs-lookup"><span data-stu-id="81ee4-106">This procedure is intended for the Commerce IT role.</span></span>


## <a name="create-new-store"></a><span data-ttu-id="81ee4-107">Neuen Shop erstellen</span><span class="sxs-lookup"><span data-stu-id="81ee4-107">Create new store</span></span>
1. <span data-ttu-id="81ee4-108">Wechseln Sie zu Alle Arbeitsbereiche > Kanalbereitstellung.</span><span class="sxs-lookup"><span data-stu-id="81ee4-108">Go to All workspaces > Channel deployment.</span></span>
2. <span data-ttu-id="81ee4-109">Neue Kanaldatenbank anklicken.</span><span class="sxs-lookup"><span data-stu-id="81ee4-109">Click New channel.</span></span>
3. <span data-ttu-id="81ee4-110">Shop anklicken.</span><span class="sxs-lookup"><span data-stu-id="81ee4-110">Click Store.</span></span>
4. <span data-ttu-id="81ee4-111">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="81ee4-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="81ee4-112">Geben Sie im Feld "Shopummer" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="81ee4-112">In the Store number field, type a value.</span></span>
6. <span data-ttu-id="81ee4-113">Klicken Sie im Feld "Lagerort" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="81ee4-113">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="81ee4-114">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="81ee4-114">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="81ee4-115">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="81ee4-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="81ee4-116">Wählen Sie im Feld "Zeitzone des Shops" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="81ee4-116">In the Store time zone field, select an option.</span></span>
10. <span data-ttu-id="81ee4-117">Klicken Sie im Feld Kanalprofil auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="81ee4-117">In the Channel profile field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="81ee4-118">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="81ee4-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="81ee4-119">Klicken Sie im Feld Sprache auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="81ee4-119">In the Language field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="81ee4-120">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="81ee4-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="81ee4-121">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="81ee4-121">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="81ee4-122">Klicken Sie im Feld "Mehrwertsteuergruppe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="81ee4-122">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="81ee4-123">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="81ee4-123">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="81ee4-124">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="81ee4-124">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="81ee4-125">Klicken Sie im Feld "Kundenadressbuch" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="81ee4-125">In the Customer address book field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="81ee4-126">Wählen Sie das Adressbuch, das verwendet wird, um Debitoren mit dieser Filiale zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="81ee4-126">Select the address book used to link customers to this store.</span></span>  
19. <span data-ttu-id="81ee4-127">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="81ee4-127">In the list, find and select the desired record.</span></span>
20. <span data-ttu-id="81ee4-128">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="81ee4-128">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="81ee4-129">Klicken Sie auf Auswählen.</span><span class="sxs-lookup"><span data-stu-id="81ee4-129">Click Select.</span></span>
22. <span data-ttu-id="81ee4-130">Klicken Sie im Feld "Mitarbeiteradressbuch" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="81ee4-130">In the Employee address book field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="81ee4-131">Wählen Sie das Adressbuch, das verwendet wird, um Debitoren mit dieser Filiale zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="81ee4-131">Select the address book used to link cashiers to this channel.</span></span>  
23. <span data-ttu-id="81ee4-132">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="81ee4-132">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="81ee4-133">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="81ee4-133">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="81ee4-134">Klicken Sie auf Auswählen.</span><span class="sxs-lookup"><span data-stu-id="81ee4-134">Click Select.</span></span>
26. <span data-ttu-id="81ee4-135">Klicken Sie im Feld "Standarddebitor" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="81ee4-135">In the Default customer field, click the drop-down button to open the lookup.</span></span>
27. <span data-ttu-id="81ee4-136">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="81ee4-136">In the list, click the link in the selected row.</span></span>
28. <span data-ttu-id="81ee4-137">Erweitern oder reduzieren Sie den Abschnitt Bildschirmlayout.</span><span class="sxs-lookup"><span data-stu-id="81ee4-137">Expand or collapse the Screen layout section.</span></span>
29. <span data-ttu-id="81ee4-138">Klicken Sie im Feld Bildschirmlayaut-ID auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="81ee4-138">In the Screen layout ID field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="81ee4-139">Wählen Sie das Standard-POS-Bildschirmlayout für diesen Shop aus.</span><span class="sxs-lookup"><span data-stu-id="81ee4-139">Select the default POS screen layout for this store.</span></span>  
30. <span data-ttu-id="81ee4-140">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="81ee4-140">In the list, find and select the desired record.</span></span>
31. <span data-ttu-id="81ee4-141">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="81ee4-141">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="81ee4-142">Klicken Sie im Aktivitätsbereich auf "Einrichten".</span><span class="sxs-lookup"><span data-stu-id="81ee4-142">On the Action Pane, click Set up.</span></span>
33. <span data-ttu-id="81ee4-143">Kanalattribute anklicken.</span><span class="sxs-lookup"><span data-stu-id="81ee4-143">Click Channel attributes.</span></span>
34. <span data-ttu-id="81ee4-144">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="81ee4-144">Click New.</span></span>
35. <span data-ttu-id="81ee4-145">Klicken Sie im Feld "Name" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="81ee4-145">In the Name field, click the drop-down button to open the lookup.</span></span>
36. <span data-ttu-id="81ee4-146">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="81ee4-146">In the list, find and select the desired record.</span></span>
37. <span data-ttu-id="81ee4-147">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="81ee4-147">In the list, click the link in the selected row.</span></span>
38. <span data-ttu-id="81ee4-148">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="81ee4-148">Click Save.</span></span>
39. <span data-ttu-id="81ee4-149">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="81ee4-149">Close the page.</span></span>
40. <span data-ttu-id="81ee4-150">Klicken Sie im Aktivitätsbereich auf "Einrichten".</span><span class="sxs-lookup"><span data-stu-id="81ee4-150">On the Action Pane, click Set up.</span></span>
41. <span data-ttu-id="81ee4-151">Klicken Sie auf "Zahlungsmethoden".</span><span class="sxs-lookup"><span data-stu-id="81ee4-151">Click Payment methods.</span></span>
42. <span data-ttu-id="81ee4-152">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="81ee4-152">Click New.</span></span>
43. <span data-ttu-id="81ee4-153">Klicken Sie im Feld "Zahlungsmethode" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="81ee4-153">In the Payment method field, click the drop-down button to open the lookup.</span></span>
44. <span data-ttu-id="81ee4-154">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="81ee4-154">In the list, click the link in the selected row.</span></span>
45. <span data-ttu-id="81ee4-155">Erweitern oder reduzieren Sie den Abschnitt ''Buchung".</span><span class="sxs-lookup"><span data-stu-id="81ee4-155">Expand or collapse the Posting section.</span></span>
46. <span data-ttu-id="81ee4-156">Geben Sie im Feld "Kontonummer" die gewünschten Werte an.</span><span class="sxs-lookup"><span data-stu-id="81ee4-156">In the Account number field, specify the desired values.</span></span>
47. <span data-ttu-id="81ee4-157">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="81ee4-157">Click Save.</span></span>
48. <span data-ttu-id="81ee4-158">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="81ee4-158">Close the page.</span></span>
49. <span data-ttu-id="81ee4-159">Klicken Sie im Aktivitätsbereich auf "Einrichten".</span><span class="sxs-lookup"><span data-stu-id="81ee4-159">On the Action Pane, click Set up.</span></span>
50. <span data-ttu-id="81ee4-160">Bargelddeklarationseinstellungen anklicken.</span><span class="sxs-lookup"><span data-stu-id="81ee4-160">Click Cash declaration.</span></span>
51. <span data-ttu-id="81ee4-161">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="81ee4-161">Click New.</span></span>
52. <span data-ttu-id="81ee4-162">Geben Sie eine Zahl in das Feld "Betrag in Währung" ein.</span><span class="sxs-lookup"><span data-stu-id="81ee4-162">In the Amount in transaction currency field, enter a number.</span></span>
53. <span data-ttu-id="81ee4-163">Klicken Sie im Feld "Währung" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="81ee4-163">In the Currency field, click the drop-down button to open the lookup.</span></span>
54. <span data-ttu-id="81ee4-164">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="81ee4-164">In the list, find and select the desired record.</span></span>
55. <span data-ttu-id="81ee4-165">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="81ee4-165">In the list, click the link in the selected row.</span></span>
56. <span data-ttu-id="81ee4-166">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="81ee4-166">Click Save.</span></span>
57. <span data-ttu-id="81ee4-167">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="81ee4-167">Close the page.</span></span>
58. <span data-ttu-id="81ee4-168">Klicken Sie im Aktivitätsbereich auf "Einrichten".</span><span class="sxs-lookup"><span data-stu-id="81ee4-168">On the Action Pane, click Set up.</span></span>
59. <span data-ttu-id="81ee4-169">Shoplokatort - Gruppenzuweisung anklicken.</span><span class="sxs-lookup"><span data-stu-id="81ee4-169">Click Store locator group assignment.</span></span>
60. <span data-ttu-id="81ee4-170">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="81ee4-170">Click New.</span></span>
61. <span data-ttu-id="81ee4-171">Markieren Sie in der Liste die ausgewählte Zeile.</span><span class="sxs-lookup"><span data-stu-id="81ee4-171">In the list, mark the selected row.</span></span>
62. <span data-ttu-id="81ee4-172">Klicken Sie im Feld Shoplokatorgruppe auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="81ee4-172">In the Locator group field, click the drop-down button to open the lookup.</span></span>
63. <span data-ttu-id="81ee4-173">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="81ee4-173">In the list, find and select the desired record.</span></span>
64. <span data-ttu-id="81ee4-174">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="81ee4-174">In the list, click the link in the selected row.</span></span>
65. <span data-ttu-id="81ee4-175">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="81ee4-175">Click Save.</span></span>
66. <span data-ttu-id="81ee4-176">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="81ee4-176">Close the page.</span></span>

