--- 
title: "Zuordnen von Komponenten des erstellten Formats zu Datenmodellelementen für elektronische Berichterstellung"
description: "Die folgende Prozedur zeigt, wie ein Benutzer entweder in der Rolle „Systemadministrator” oder der Rolle „Entwickler für elektronische Berichterstellung” Datenmodellelemente Komponenten der erstellten Elektronischen Berichterstellungs-(ER)-Konfiguration zuordnen kann, die ein elektronisches Dokumentformat für die Zahlungsgeschäftsdomäne definiert."
author: NickSelin
manager: AnnBe
ms.date: 02/27/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1c81a1268a56164e0d4465359a0f9ec425ee7c31
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="map-components-of-the-created-format-to-data-model-elements-for-electronic-reporting-er"></a><span data-ttu-id="a4fa9-103">Zuordnen von Komponenten des erstellten Formats zu Datenmodellelementen für elektronische Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="a4fa9-103">Map components of the created format to data model elements for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a4fa9-104">Die folgende Prozedur zeigt, wie ein Benutzer entweder in der Rolle „Systemadministrator” oder der Rolle „Entwickler für elektronische Berichterstellung” Datenmodellelemente Komponenten der erstellten Elektronischen Berichterstellungs-(ER)-Konfiguration zuordnen kann, die ein elektronisches Dokumentformat für die Zahlungsgeschäftsdomäne definiert.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-104">The following procedure shows how a user in either the System administrator or Electronic reporting developer role can map data model elements to components of the created Electronic reporting (ER) configuration, which defines an electronic document format for the payments business domain.</span></span> <span data-ttu-id="a4fa9-105">Dieses Format wird später verwendet, um elektronische Dokumente zur Verarbeitung von Zahlungen zu generieren.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-105">This format will be used later to generate electronic documents for processing payments.</span></span> <span data-ttu-id="a4fa9-106">In diesem Beispiel erstellen Sie eine Formatkonfiguration für das Beispielunternehmen „Litware, Inc.”.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-106">In this example, you will create a format configuration for the sample company, ‘Litware, Inc.’.</span></span> <span data-ttu-id="a4fa9-107">Diese Schritte können an einem beliebigen Unternehmen ausgeführt werden, da die ER-Konfiguration von allen Unternehmen genutzt werden.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-107">These steps can be performed in any company as ER configurations are shared for all companies.</span></span> <span data-ttu-id="a4fa9-108">Um diese Schritte abzuschließen, müssen Sie zuerst die Schritte im Aufgabenleitfaden „Eine Formatkonfiguration erstellen” abschließen.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-108">To complete these steps, you must first complete the steps in the “Create a format configuration” task guide.</span></span>


## <a name="select-a-format-configuration"></a><span data-ttu-id="a4fa9-109">Eine Formatkonfiguration auswählen</span><span class="sxs-lookup"><span data-stu-id="a4fa9-109">Select a format configuration</span></span>
1. <span data-ttu-id="a4fa9-110">Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="a4fa9-111">Klicken Sie auf "Berichterstellungskonfigurationen".</span><span class="sxs-lookup"><span data-stu-id="a4fa9-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="a4fa9-112">Erweitern Sie "Zahlungen (vereinfachtes Modell)" in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-112">In the tree, expand 'Payments (simplified model)'.</span></span>
4. <span data-ttu-id="a4fa9-113">Wählen Sie "Zahlungen (vereinfachtes Modell)\BACS (Großbritannien, fiktiv)" in der Struktur aus.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-113">In the tree, select 'Payments (simplified model)\BACS (UK fictitious)'.</span></span>
5. <span data-ttu-id="a4fa9-114">Klicken Sie auf Designer.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-114">Click Designer.</span></span>

## <a name="map-format-components-to-data-model-elements"></a><span data-ttu-id="a4fa9-115">Weisen Sie Formatkomponenten für das Zuordnen zu den Datenmodellelementen zu</span><span class="sxs-lookup"><span data-stu-id="a4fa9-115">Map format components to data model elements</span></span>
1. <span data-ttu-id="a4fa9-116">Klicken Sie „Erweitern/reduzieren”.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-116">Click Expand/collapse.</span></span>
2. <span data-ttu-id="a4fa9-117">Klicken Sie auf die Registerkarte Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-117">Click the Mapping tab.</span></span>
3. <span data-ttu-id="a4fa9-118">Erweitern Sie in der -Struktur den Knoten 'Modell'.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-118">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="a4fa9-119">Wählen Sie in der Struktur „XML\Nachricht\ProcessingDate\DateTime” aus.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-119">In the tree, select 'Xml\Message\ProcessingDate\DateTime'.</span></span>
5. <span data-ttu-id="a4fa9-120">Wählen Sie „Modell\ProcessingDateTime” in der Struktur aus.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-120">In the tree, select 'model\ProcessingDateTime'.</span></span>
6. <span data-ttu-id="a4fa9-121">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-121">Click Bind.</span></span>
7. <span data-ttu-id="a4fa9-122">Wählen Sie in der Struktur „XML\Nachricht\MessageId\Zeichenfolge” aus.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-122">In the tree, select 'Xml\Message\MessageId\String'.</span></span>
8. <span data-ttu-id="a4fa9-123">Wählen Sie in der Struktur „Modell\MessageIdentification” aus.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-123">In the tree, select 'model\MessageIdentification'.</span></span>
9. <span data-ttu-id="a4fa9-124">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-124">Click Bind.</span></span>
10. <span data-ttu-id="a4fa9-125">Erweitern Sie 'Modell\Zahlungen' in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-125">In the tree, expand 'model\Payments'.</span></span>
11. <span data-ttu-id="a4fa9-126">Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel\Betrag\Zeichenfolge” aus.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-126">In the tree, select 'Xml\Message\Payments\Item\Amount\String'.</span></span>
12. <span data-ttu-id="a4fa9-127">Wählen Sie „Modell\Zahlungen\InstructedAmount” in der Struktur aus.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-127">In the tree, select 'model\Payments\InstructedAmount'.</span></span>
13. <span data-ttu-id="a4fa9-128">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-128">Click Bind.</span></span>
14. <span data-ttu-id="a4fa9-129">Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel\TransDate\DateTime” aus.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-129">In the tree, select 'Xml\Message\Payments\Item\TransDate\DateTime'.</span></span>
15. <span data-ttu-id="a4fa9-130">Wählen Sie „Modell\Zahlungen\TransactionDate” in der Struktur aus.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-130">In the tree, select 'model\Payments\TransactionDate'.</span></span>
16. <span data-ttu-id="a4fa9-131">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-131">Click Bind.</span></span>
17. <span data-ttu-id="a4fa9-132">Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel\Beschreibung\Zeichenfolge” aus.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-132">In the tree, select 'Xml\Message\Payments\Item\Description\String'.</span></span>
18. <span data-ttu-id="a4fa9-133">Wählen Sie 'Modell\Zahlungen\Beschreibung' in der Struktur aus.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-133">In the tree, select 'model\Payments\Description'.</span></span>
19. <span data-ttu-id="a4fa9-134">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-134">Click Bind.</span></span>
20. <span data-ttu-id="a4fa9-135">Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel\Währung\Zeichenfolge” aus.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-135">In the tree, select 'Xml\Message\Payments\Item\Currency\String'.</span></span>
21. <span data-ttu-id="a4fa9-136">Wählen Sie in der Struktur "Modell\Zahlungen\Währung" aus.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-136">In the tree, select 'model\Payments\Currency'.</span></span>
22. <span data-ttu-id="a4fa9-137">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-137">Click Bind.</span></span>
23. <span data-ttu-id="a4fa9-138">Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel\ID” aus.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-138">In the tree, select 'Xml\Message\Payments\Item\Id'.</span></span>
24. <span data-ttu-id="a4fa9-139">Wählen Sie in der Struktur „Modell\Zahlungen\End2EndID” aus.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-139">In the tree, select 'model\Payments\End2EndID'.</span></span>
25. <span data-ttu-id="a4fa9-140">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-140">Click Bind.</span></span>
26. <span data-ttu-id="a4fa9-141">Erweitern Sie 'Modell\Payments\Creditor' in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-141">In the tree, expand 'model\Payments\Creditor'.</span></span>
27. <span data-ttu-id="a4fa9-142">In der Struktur erweitern Sie "Modell\Zahlungen\Kreditor\Konto".</span><span class="sxs-lookup"><span data-stu-id="a4fa9-142">In the tree, expand 'model\Payments\Creditor\Account'.</span></span>
28. <span data-ttu-id="a4fa9-143">In der Struktur erweitern Sie "Modell\Zahlungen\Kreditor\Agent".</span><span class="sxs-lookup"><span data-stu-id="a4fa9-143">In the tree, expand 'model\Payments\Creditor\Agent'.</span></span>
29. <span data-ttu-id="a4fa9-144">Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel\Kreditor\Name\Zeichenfolge” aus.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-144">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name\String'.</span></span>
30. <span data-ttu-id="a4fa9-145">Wählen Sie 'Modell\Payments\Creditor\Account\Name' in der Struktur aus.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-145">In the tree, select 'model\Payments\Creditor\Name'.</span></span>
31. <span data-ttu-id="a4fa9-146">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-146">Click Bind.</span></span>
32. <span data-ttu-id="a4fa9-147">Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel\Kreditor\Bank\RoutingNumber\Zeichenfolge” aus.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-147">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber\String'.</span></span>
33. <span data-ttu-id="a4fa9-148">Wählen Sie in der Struktur Folgendes aus: „Modell\Zahlungen\Kreditor\Agent\RoutingNumber”.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-148">In the tree, select 'model\Payments\Creditor\Agent\RoutingNumber'.</span></span>
34. <span data-ttu-id="a4fa9-149">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-149">Click Bind.</span></span>
35. <span data-ttu-id="a4fa9-150">Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel\Kreditor\Bank\AccountNumber\Zeichenfolge” aus.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-150">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\AccountNumber\String'.</span></span>
36. <span data-ttu-id="a4fa9-151">Wählen Sie 'Modell\Payments\Creditor\Account\Number' in der Struktur aus.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-151">In the tree, select 'model\Payments\Creditor\Account\Number'.</span></span>
37. <span data-ttu-id="a4fa9-152">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-152">Click Bind.</span></span>
38. <span data-ttu-id="a4fa9-153">Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel\Zahlender\Name\Zeichenfolge” aus.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-153">In the tree, select 'Xml\Message\Payments\Item\Payer\Name\String'.</span></span>
39. <span data-ttu-id="a4fa9-154">Erweitern Sie 'Modell\Payments\Debtor' in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-154">In the tree, expand 'model\Payments\Debtor'.</span></span>
40. <span data-ttu-id="a4fa9-155">In der Struktur erweitern Sie "Modell\Zahlungen\Debtor\Konto".</span><span class="sxs-lookup"><span data-stu-id="a4fa9-155">In the tree, expand 'model\Payments\Debtor\Account'.</span></span>
41. <span data-ttu-id="a4fa9-156">Erweitern Sie 'Modell\Payments= Transactions\Agent' in der Struktur.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-156">In the tree, expand 'model\Payments\Debtor\Agent'.</span></span>
42. <span data-ttu-id="a4fa9-157">Wählen Sie 'Modell\Payments\Debtor\Account\Name' in der Struktur aus.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-157">In the tree, select 'model\Payments\Debtor\Name'.</span></span>
43. <span data-ttu-id="a4fa9-158">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-158">Click Bind.</span></span>
44. <span data-ttu-id="a4fa9-159">Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel\Zahlender\Bank\RoutingNumber\Zeichenfolge” aus.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-159">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\RoutingNumber\String'.</span></span>
45. <span data-ttu-id="a4fa9-160">Wählen Sie in der Struktur Folgendes aus: „Modell\Zahlungen\Debitor\Agent\RoutingNumber”.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-160">In the tree, select 'model\Payments\Debtor\Agent\RoutingNumber'.</span></span>
46. <span data-ttu-id="a4fa9-161">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-161">Click Bind.</span></span>
47. <span data-ttu-id="a4fa9-162">Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel\Zahlender\Bank\AccountNumber\Zeichenfolge” aus.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-162">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\AccountNumber\String'.</span></span>
48. <span data-ttu-id="a4fa9-163">Wählen Sie 'Modell\Payments\Debtor\Account\Number' in der Struktur aus.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-163">In the tree, select 'model\Payments\Debtor\Account\Number'.</span></span>
49. <span data-ttu-id="a4fa9-164">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-164">Click Bind.</span></span>
50. <span data-ttu-id="a4fa9-165">Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel” aus.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-165">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
51. <span data-ttu-id="a4fa9-166">Wählen Sie 'Modell\Zahlungen' in der Struktur aus.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-166">In the tree, select 'model\Payments'.</span></span>
52. <span data-ttu-id="a4fa9-167">Klicken Sie auf Binden.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-167">Click Bind.</span></span>
53. <span data-ttu-id="a4fa9-168">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="a4fa9-168">Click Save.</span></span>

## <a name="validate-format-mapping"></a><span data-ttu-id="a4fa9-169">Formatzuordnung überprüfen</span><span class="sxs-lookup"><span data-stu-id="a4fa9-169">Validate format mapping</span></span>
1. <span data-ttu-id="a4fa9-170">Klicken Sie auf "Überprüfen".</span><span class="sxs-lookup"><span data-stu-id="a4fa9-170">Click Validate.</span></span>
    * <span data-ttu-id="a4fa9-171">Überprüft die neue Zuordnung, um sicherzustellen, dass alle Bindungen in Ordnung sind.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-171">Validate the new mapping to ensure that all bindings are okay.</span></span>  
2. <span data-ttu-id="a4fa9-172">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-172">Close the page.</span></span>

## <a name="change-status-of-the-current-version-of-format-configuration"></a><span data-ttu-id="a4fa9-173">Ändern Sie den Status der aktuellen Version der Format-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="a4fa9-173">Change status of the current version of format configuration</span></span>
    * <span data-ttu-id="a4fa9-174">In den nächsten Schritten ändern Sie den Status der Formatkonfiguration von „Entwurf” zu „Abgeschlossen”, um sie für die Zahlungsdokumentgenerierung verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-174">In the next steps, you’ll change the status of the format configuration from Draft to Completed to make it available for payment document generation.</span></span>  
1. <span data-ttu-id="a4fa9-175">Klicken Sie auf "Status ändern".</span><span class="sxs-lookup"><span data-stu-id="a4fa9-175">Click Change status.</span></span>
2. <span data-ttu-id="a4fa9-176">Klicken Sie auf "Abgeschlossen".</span><span class="sxs-lookup"><span data-stu-id="a4fa9-176">Click Complete.</span></span>
3. <span data-ttu-id="a4fa9-177">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-177">In the Description field, type a value.</span></span>
    * <span data-ttu-id="a4fa9-178">Beispielsweise „Version 1”.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-178">For example, 'version 1'.</span></span>  
4. <span data-ttu-id="a4fa9-179">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="a4fa9-179">Click OK.</span></span>
5. <span data-ttu-id="a4fa9-180">Wählen Sie die abgeschlossene Version der aktuellen Konfiguration aus.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-180">Select completed version of the current configuration.</span></span>
    * <span data-ttu-id="a4fa9-181">Beachten Sie, dass die Konfiguration als abgeschlossene Version 1.1 gespeichert wird: Version 1 des Formats basierend auf der Version 1 des Datenmodells.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-181">Note that the configuration is saved as completed version 1.1: version 1 of the format based on the version 1 of the data model.</span></span>  

## <a name="define-effective-date-for-completed-version-of-format"></a><span data-ttu-id="a4fa9-182">Definieren Sie Gültigkeitsdatum für abgeschlossene Version des Formats</span><span class="sxs-lookup"><span data-stu-id="a4fa9-182">Define effective date for completed version of format</span></span>
    * <span data-ttu-id="a4fa9-183">Jede Formatversion kann so konfiguriert werden, wie verfügbar für die Verwendung, die von einem bestimmten Datum startet.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-183">Each format version can be configured as available for usage starting from a certain date.</span></span> <span data-ttu-id="a4fa9-184">Wenn mehr als eine Formatversion an einem bestimmten Datum aktiv ist, wird das neueste Format (auf Grundlage der Versionsnummer) für die Verwendung ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-184">When more than one format version is active on a certain date, the latest format (based on version number) will be selected for usage.</span></span> <span data-ttu-id="a4fa9-185">Der Sitzungsdatumswert wird für die richtige Versionsauswahl verwendet.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-185">The session date value is used for proper version selection.</span></span>  

## <a name="restrict-access-to-created-format-from-companies"></a><span data-ttu-id="a4fa9-186">Einschränken des Zugriffs auf erstelltes Format von Unternehmen</span><span class="sxs-lookup"><span data-stu-id="a4fa9-186">Restrict access to created format from companies</span></span>
1. <span data-ttu-id="a4fa9-187">Erweitern Sie den Abschnitt „ISO-Land-/Regionencode”.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-187">Expand the ISO Country/region codes section.</span></span>
    * <span data-ttu-id="a4fa9-188">Jeder Formatzugriff kann beschränkt werden, indem bestimmte Länder/Regionen angibt, in denen ein Format anwendbar ist.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-188">Each format access can be restricted by identifying particular countries/regions in which a format is applicable.</span></span> <span data-ttu-id="a4fa9-189">Wenn die Länder-/Regionenliste für ein bestimmtes Format leer ist, kann dieses Format in einem beliebigen Unternehmen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-189">When the list of countries/regions for particular format is empty, this format can be used in any company.</span></span> <span data-ttu-id="a4fa9-190">Wenn mehrere ISO-Länder-/Regionscodes in die Länder-/Regionenliste eingefügt werden, kann dieses Format nur in Unternehmen verwendet werden, wenn die primäre Adresse sich in dem Land/der Region befindet.</span><span class="sxs-lookup"><span data-stu-id="a4fa9-190">When some ISO country/region codes are inserted in the list of countries/regions, the format can only be use in companies if the primary address is in the country/region.</span></span>  


