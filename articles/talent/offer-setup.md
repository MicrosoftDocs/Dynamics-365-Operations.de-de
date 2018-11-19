---
title: Einrichten der Angebotsverwaltung
description: In diesem Thema wird beschrieben, wie Angebote in Talent eingerichtet werden.
author: josaw
manager: AnnBe
ms.date: 10/18/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-10-18
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: fa2f2f9f67562524961352a87a7db49992776e46
ms.contentlocale: de-de
ms.lasthandoff: 10/22/2018

---
# <a name="set-up-offer-management"></a><span data-ttu-id="58da7-103">Einrichten der Angebotsverwaltung</span><span class="sxs-lookup"><span data-stu-id="58da7-103">Set up offer management</span></span> 

[!include [banner](includes/banner.md)]

<span data-ttu-id="58da7-104">Wenn ein Kandidat auf die Angebotphase in Dynamics 365 for Talent verschoben werden soll: Attract, Sie müssen sicherstellen, dass die Angebote für den Kandidaten schnell nach Bedarf erstellt werden, genehmigt sind und den Kandidaten gesendet werden können.</span><span class="sxs-lookup"><span data-stu-id="58da7-104">When a candidate is moved to the offer stage in Dynamics 365 for Talent: Attract, you need to ensure that the offers can be quickly created for the candidate, approved as necessary, and sent out to the candidate.</span></span> <span data-ttu-id="58da7-105">Da die meisten Angebote standardmäßig sind, können Sie aus wiederverwendbaren Vorlagen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="58da7-105">Because most offers are standard, they can be created from reusable templates.</span></span> <span data-ttu-id="58da7-106">In Attract werden alle Angebote in ein Angebotspaket verschoben, das eine Zusammenstellung eines oder mehrerer Angebotsunterlagen ist.</span><span class="sxs-lookup"><span data-stu-id="58da7-106">In Attract, all offers are rolled into an offer package, which is a collection of one or more offer documents.</span></span> 

<span data-ttu-id="58da7-107">Dieses Thema führt alle Schritte auf, denen ein Attract-Administrator folgen würde, um verschiedene Angebotpaketvorlagen als Teil der Angebotsverwaltung einzurichten in Attract.</span><span class="sxs-lookup"><span data-stu-id="58da7-107">This topic lists all the steps that an Attract administrator would follow to set up different offer package templates as part of the offer management capability in Attract.</span></span> <span data-ttu-id="58da7-108">Benutzer mit Nicht-Administrator-Rollen haben keinen Zugriff zu diesen Funktionen.</span><span class="sxs-lookup"><span data-stu-id="58da7-108">Users with non-administrator roles will not have access to these capabilities.</span></span>

>[!NOTE]
> <span data-ttu-id="58da7-109">Angebotsverwaltungsfunktionen werden als Teil für das Einstellungsadd-on verfügbar.</span><span class="sxs-lookup"><span data-stu-id="58da7-109">Offer management capabilities are available as part of the Comprehensive Hiring Add-On.</span></span>

## <a name="offer-data"></a><span data-ttu-id="58da7-110">Angebotsdaten</span><span class="sxs-lookup"><span data-stu-id="58da7-110">Offer data</span></span> 

<span data-ttu-id="58da7-111">Angebotdaten sind die kleinste Einheit in der Angebotpaketvorlage.</span><span class="sxs-lookup"><span data-stu-id="58da7-111">Offer data is the smallest unit inside the offer package template.</span></span> <span data-ttu-id="58da7-112">Ein typisches Angebot besteht aus Standardtext und aus einer Gruppe von Werten.</span><span class="sxs-lookup"><span data-stu-id="58da7-112">A typical offer consists of standard text and a set of values.</span></span> <span data-ttu-id="58da7-113">Die Gruppen der Werte sind die einzelnen Bestandteile, die zwischen Angeboten ändern können.</span><span class="sxs-lookup"><span data-stu-id="58da7-113">The sets of values are the only pieces that could change between offers.</span></span> <span data-ttu-id="58da7-114">Während der Angeboterstellung ist der wichtigste Aspekt, auf den sich der Angebotersteller fokussieren kann, die Liste der Angebotdatenenplatzhaltern, die in einer Angebotpaketvorlage vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="58da7-114">During the offer creation, the most important aspect that the offer creator can focus on is the list of offer data placeholders present in an offer package template.</span></span> <span data-ttu-id="58da7-115">Um Angebotdaten einzurichten, gehen Sie folgendermaßen vor.</span><span class="sxs-lookup"><span data-stu-id="58da7-115">To set up offer data, do the following.</span></span>

1.  <span data-ttu-id="58da7-116">Gehen Sie zu **Management anbieten**.</span><span class="sxs-lookup"><span data-stu-id="58da7-116">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="58da7-117">Erweitern Sie den Bereich **Bibliothek** im linken Navigationsbereich, und fahren Sie mit **Angebotdaten** fort.</span><span class="sxs-lookup"><span data-stu-id="58da7-117">Expand the **Library** section in the left navigation pane, then go to **Offer data**.</span></span>

    >[!NOTE]
    > <span data-ttu-id="58da7-118">Auf der Seite **Daten anbieten** werden die Abschnitte **Kandidatendetails** und **Stellendetails** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="58da7-118">On the **Offer data** page are the **Candidate details** and **Job details** sections.</span></span> <span data-ttu-id="58da7-119">Attract stellt einige Daten-Platzhalterstandards bereit.</span><span class="sxs-lookup"><span data-stu-id="58da7-119">Attract provides a few offer data placeholders out-of-the-box.</span></span>
    
    > <span data-ttu-id="58da7-120">Es gibt Abschnitte auf der Seite, um die verschiedenen Angebotsdatenenplatzhalter zusammen mit den logischen Gruppen zu organisieren.</span><span class="sxs-lookup"><span data-stu-id="58da7-120">There are sections on the page to organize different offer data placeholders together in logical groups.</span></span> <span data-ttu-id="58da7-121">Diese Bereiche können bei der Verwaltung von Angebotdaten und beim Auffüllen von Daten während des Angebotserstellungsprozesses helfen.</span><span class="sxs-lookup"><span data-stu-id="58da7-121">These sections can help with maintenance of offer data and population of data during the offer creation process.</span></span>

1.  <span data-ttu-id="58da7-122">Zum Erstellen eines neuen Angebotsdatenabschnittes klicken Sie auf **Fügen Sie einen Abschnitt hinzu**, und geben Sie einen eindeutigen Namen für den Bereich ein.</span><span class="sxs-lookup"><span data-stu-id="58da7-122">To create a new offer data section, click **Add a section** and enter a unique name for the section.</span></span>

1.  <span data-ttu-id="58da7-123">Um Angebotsdatenenplatzhalter jedem Bereich hinzuzufügen, klicken Sie auf **Fügen Sie Angebotsdaten hinzu** und geben Sie einen eindeutigen Namen für den Platzhalter ein.</span><span class="sxs-lookup"><span data-stu-id="58da7-123">To add offer data placeholders to any section, click **Add offer data** and enter a unique name for the placeholder.</span></span>

1.  <span data-ttu-id="58da7-124">Wenn Sie den Namen eines Abschnitts bearbeiten, fahren Sie über den Abschnittsnamen und aktualisieren Sie den Namen.</span><span class="sxs-lookup"><span data-stu-id="58da7-124">To edit the name of any section, hover over the section name and update the name.</span></span>

1.  <span data-ttu-id="58da7-125">Um den Namen aller vorhandenen Angebotsdatenenplatzhalter zu bearbeiten, sollten Sie zunächst sicherstellen, dass der Platzhalter nicht bereits Teil einer Vorlage ist.</span><span class="sxs-lookup"><span data-stu-id="58da7-125">To edit the name of any existing offer data placeholder, first make sure that the placeholder is not already part of any template.</span></span> <span data-ttu-id="58da7-126">Anschließend fahren Sie über den Namen der Angebotsdatenplatzhalter und aktualisieren Sie den Namen nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="58da7-126">Then, hover over the name of the offer data placeholder and update the name as needed.</span></span>

1. <span data-ttu-id="58da7-127">Um den Namen aller vorhandenen Angebotsdatenenplatzhalter zu löschen, sollten Sie zunächst sicherstellen, dass der Platzhalter nicht bereits Teil einer anderen Vorlage ist.</span><span class="sxs-lookup"><span data-stu-id="58da7-127">To delete an existing offer data placeholder, first make sure that the placeholder is not part of any other template.</span></span> <span data-ttu-id="58da7-128">Anschließend fahren Sie mit dem Mauszeigers über den Platzhalter und wenn das Abfalleimersymbol erscheint, klicken Sie auf den Abfalleimer, um den Angebotsdatenenplatzhalter zu löschen.</span><span class="sxs-lookup"><span data-stu-id="58da7-128">Then, hover over the placeholder and when the trash can icon appears, click the trash can to delete the offer data placeholder.</span></span>
    >[!NOTE]
    > <span data-ttu-id="58da7-129">Sie können sehen, wie viele Vorlagen ein Angebotsdatenenplatzhalter Teil vom Nummerindikator neben den Angebotsdaten ist.</span><span class="sxs-lookup"><span data-stu-id="58da7-129">You can see how many templates an offer data placeholder is part of by the number indicator next to each offer data.</span></span> 

1. <span data-ttu-id="58da7-130">Wenn Sie einen Abschnitt löschen, fahren Sie über den Namen.</span><span class="sxs-lookup"><span data-stu-id="58da7-130">To delete any section, hover over the name.</span></span> <span data-ttu-id="58da7-131">Wenn keine der Angebotdatenenplatzhalter innerhalb des Bereichs in jeder Vorlage angezeigt werden, können Sie auf das Abfalleimersymbol klicken, um sie zu löschen.</span><span class="sxs-lookup"><span data-stu-id="58da7-131">If none of the offer data placeholders inside the section appear in any template, you can click the trash can icon to delete it.</span></span> 
    >[!NOTE]
    > <span data-ttu-id="58da7-132">Mit dem Löschen des Abschnitts werden auch alle Angebotsdaten-Platzhalter im Bereich gelöscht.</span><span class="sxs-lookup"><span data-stu-id="58da7-132">Deleting the section will also delete all the offer data placeholders inside that section.</span></span>

<span data-ttu-id="58da7-133">Nachdem die Angebotdatenenplatzhalter eingerichtet wurden, können Sie diese zu einer beliebigen Dokumentvorlage verwenden.</span><span class="sxs-lookup"><span data-stu-id="58da7-133">After the offer data placeholders have been set up, you can use them across any document template.</span></span> <span data-ttu-id="58da7-134">Angebotdatenenplatzhalter werden nicht auf eine bestimmte Vorlage beschränkt -- dieselbe Definition kann für alle Vorlagen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="58da7-134">Offer data placeholders are not restricted to a specific template -- the same set can be used across all templates.</span></span>

## <a name="offer-data-rules"></a><span data-ttu-id="58da7-135">Angebotdatenregeln</span><span class="sxs-lookup"><span data-stu-id="58da7-135">Offer data rules</span></span>

<span data-ttu-id="58da7-136">Die meisten Organisation haben Regeln dazu, wie Angebote erstellt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="58da7-136">Most organization have rules for how offers must be created.</span></span> <span data-ttu-id="58da7-137">Zum Beispiel möchte eine Organisation, dass das maximale Angebot des jährlichen Gehalts für einen bestimmten Standort und ein bestimmtes Dienstalters innerhalb eines bestimmten Bereichs liegt oder dass nur wenige bestimmte Werte für die Angebotsebene für den neuen Mitarbeiter möglich sind.</span><span class="sxs-lookup"><span data-stu-id="58da7-137">For example, an organization may want to require that the maximum annual salary offer for a specific location and seniority level combination has to be within a certain range, or that there are only a few specific values possible for the offer level for the new hire.</span></span> <span data-ttu-id="58da7-138">Attract unterstützt derzeit all diese Datenregeln mithilfe einer CSV-Datei.</span><span class="sxs-lookup"><span data-stu-id="58da7-138">Attract currently supports all such data rules using a CSV file.</span></span>

<span data-ttu-id="58da7-139">Um die Datenregeln für die CSV-Datei zu erstellen, gehen Sie folgendermaßen vor.</span><span class="sxs-lookup"><span data-stu-id="58da7-139">To prepare the data rules CSV file, do the following.</span></span>

1.  <span data-ttu-id="58da7-140">Festlegen der Angebotdatenenplatzhalter für die Regelsammlung.</span><span class="sxs-lookup"><span data-stu-id="58da7-140">Determine the offer data placeholder for the rule set.</span></span> <span data-ttu-id="58da7-141">Zum Beispiel **Jährliches Gehalt**.</span><span class="sxs-lookup"><span data-stu-id="58da7-141">For example, **Annual Salary**.</span></span>

1.  <span data-ttu-id="58da7-142">Definieren Sie die Angebotsdaten-Platzhalterwerte.</span><span class="sxs-lookup"><span data-stu-id="58da7-142">Identify the dependent offer data placeholder values.</span></span> <span data-ttu-id="58da7-143">Zum Beispiel **Arbeitsort** und **Ebene**.</span><span class="sxs-lookup"><span data-stu-id="58da7-143">For example, **Job Location** and **Level**.</span></span>

1.  <span data-ttu-id="58da7-144">Geben Sie Spalten 1 und 2 als **Arbeitsort** und **Ebene** an.</span><span class="sxs-lookup"><span data-stu-id="58da7-144">Specify columns 1 and 2 as **Job Location** and **Level**.</span></span>

1.  <span data-ttu-id="58da7-145">Um einen Bereichswert hochzuladen, machen Sie Spalten 3 und 4 für **Jährliches Gehalt**.</span><span class="sxs-lookup"><span data-stu-id="58da7-145">To upload a range value, make columns 3 and 4 **Annual Salary**.</span></span> <span data-ttu-id="58da7-146">Um einen bestimmten Wert anstelle eines Bereichs hochladen, lassen Sie nur Spalte 3**Jährliches Gehalt**.</span><span class="sxs-lookup"><span data-stu-id="58da7-146">To upload a specific value instead of a range, only make column 3 **Annual Salary**.</span></span>

1.  <span data-ttu-id="58da7-147">Aktualisieren Sie die Microsoft Excel-Dateien auf Grundlage der notwendigen Rollen.</span><span class="sxs-lookup"><span data-stu-id="58da7-147">Populate the Microsoft Excel file based on your required roles.</span></span>

1.  <span data-ttu-id="58da7-148">Sicherstellen, dass jede Zeile eine eindeutige Kombination aller Werte ist, die zusammengestellt werden.</span><span class="sxs-lookup"><span data-stu-id="58da7-148">Ensure that each row is a unique combination of all the values put together.</span></span>

1.  <span data-ttu-id="58da7-149">Speichern Sie die Datei als CSV-Format.</span><span class="sxs-lookup"><span data-stu-id="58da7-149">Save the file as a CSV format.</span></span>

<span data-ttu-id="58da7-150">Um die Datenregeln für die CSV-Datei zu erstellen, gehen Sie folgendermaßen vor.</span><span class="sxs-lookup"><span data-stu-id="58da7-150">To upload the offer data rules file, do the following.</span></span>

1.  <span data-ttu-id="58da7-151">Gehen Sie zu **Management anbieten**.</span><span class="sxs-lookup"><span data-stu-id="58da7-151">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="58da7-152">Erweitern Sie den Bereich **Bibliothek** im linken Navigationsbereich, und fahren Sie mit **Angebotdatenregeln** fort.</span><span class="sxs-lookup"><span data-stu-id="58da7-152">Expand the **Library** section in the left navigation panel, then go to **Offer data rules**.</span></span>

1.  <span data-ttu-id="58da7-153">Klicken Sie auf **Neuer Datensatz**, um das Dialogfeld **Hochladen** anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="58da7-153">Click **New data set** to display the **Upload** dialog box.</span></span>

1.  <span data-ttu-id="58da7-154">Geben Sie einen eindeutigen Namen für den Regelsatz an und laden Sie dann die gespeicherte CSV-Datei hoch.</span><span class="sxs-lookup"><span data-stu-id="58da7-154">Specify a unique name for the rule set and then upload the saved CSV file.</span></span>

1.  <span data-ttu-id="58da7-155">Klicken Sie auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="58da7-155">Click **Add**.</span></span>
    <span data-ttu-id="58da7-156">Die Regelsammlung wird im Hintergrund verarbeitet und Sie sind InApp gemeldete und per E-Mail, sobald diese ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="58da7-156">The rule set will be processed in the background and you will be notified in-app and via email once it completes.</span></span>

    <span data-ttu-id="58da7-157">Sie werden benachrichtigt, wenn es Fehler beim Verarbeiten des Uploads gibt.</span><span class="sxs-lookup"><span data-stu-id="58da7-157">You will be notified if there are errors while processing the upload.</span></span> <span data-ttu-id="58da7-158">Sie können das Fehlerprotokoll dann herunterladen, die Datei reparieren und erneut hochladen.</span><span class="sxs-lookup"><span data-stu-id="58da7-158">You can then download the error log, fix the file, and upload it again.</span></span>

1.  <span data-ttu-id="58da7-159">Verwenden Sie die Optionsschaltfläche der Auslassungspunkte (**...**), wenn Sie den Regelsatz herunterladen und die Werte aktualisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="58da7-159">Use the ellipses button (**…**) option if you want to download the rule set and update the set of values.</span></span> <span data-ttu-id="58da7-160">Nach der Aktualisierung können Sie die Datei erneut hochladen.</span><span class="sxs-lookup"><span data-stu-id="58da7-160">After updating, you can upload the file again.</span></span>

1.  <span data-ttu-id="58da7-161">Sie können einen vorhandenen Regelsatzupload löschen, wenn der Platzhalter, der definiert ist, von keiner anderen Dokumentvorlage verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="58da7-161">You can delete an existing rule set upload if the placeholder being defined is not being used in another document template.</span></span>

>[!NOTIZEN]
> - <span data-ttu-id="58da7-163">Jeder Platzhalter kann einen eindeutigen Satz Spalten haben, der davon abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="58da7-163">Each placeholder can only have one unique set of columns that it is dependent on.</span></span> <span data-ttu-id="58da7-164">Wenn beispielsweise **Jährliches Gehalt** **Arbeitsort** **Ebene** abhängig ist, können Sie einen anderen Regelsatz nicht hochgeladen, **Jährliches Gehalt** aus einem anderen Satz Spalten abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="58da7-164">For example, if **Annual Salary** is dependent on **Job Location** and **Level**, you can't upload another rule set where **Annual Salary** is dependent on a different set of columns.</span></span>

> - <span data-ttu-id="58da7-165">Sie können Beispielangebotdatenregelsätze auf der Registerkarte **Beispiele** auf der Seite **Angebotdatenregeln** herunterladen.</span><span class="sxs-lookup"><span data-stu-id="58da7-165">You can download sample offer data rule sets on the **Samples** tab on the **Offer data rules** page.</span></span>

> - <span data-ttu-id="58da7-166">Wenn ein Angebotersteller die Werte überschreibt, die von der Angebotsdatenregeln empfohlen werden, wird das Angebot als Nicht-Standard gekennzeichnet und die Genehmigung des Angebotsgenehmigungsworkflows wird vorgegeben.</span><span class="sxs-lookup"><span data-stu-id="58da7-166">When an offer creator overrides the values that are recommended by the offer data rules, the offer is flagged as non-standard and offer approval workflow will be mandated.</span></span>

## <a name="document-templates"></a><span data-ttu-id="58da7-167">Dokumentvorlagen</span><span class="sxs-lookup"><span data-stu-id="58da7-167">Document templates</span></span>

<span data-ttu-id="58da7-168">Eine Angebotsunterlagevorlage kann Administratoren helfen, Angebotsschreiben zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="58da7-168">An offer document template can help administrators create offer letters.</span></span> <span data-ttu-id="58da7-169">Die Angebotsunterlagevorlage ist eine Kombination des Texts, der ein Bestandteil des Angebots und ein  definierter Angebotdatenenplatzhalter ist.</span><span class="sxs-lookup"><span data-stu-id="58da7-169">The offer document template is a combination of the text that will be part of the offer as well as the defined offer data placeholders.</span></span> 

<span data-ttu-id="58da7-170">Um eine Angebotsunterlagevorlage zu erstellen, gehen Sie folgendermaßen vor.</span><span class="sxs-lookup"><span data-stu-id="58da7-170">To create an offer document template, do the following.</span></span>

1.  <span data-ttu-id="58da7-171">Gehen Sie zu **Management anbieten**.</span><span class="sxs-lookup"><span data-stu-id="58da7-171">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="58da7-172">Erweitern Sie den Bereich **Bibliothek** im linken Navigationsbereich, und fahren Sie mit **Vorlage** fort.</span><span class="sxs-lookup"><span data-stu-id="58da7-172">Expand the **Library** section in the left navigation pane and go to **Templates**.</span></span>

    <span data-ttu-id="58da7-173">Die Seite **Vorlagen** zeigt eine Liste der Dokumentvorlagen an, die bereits geladen wurden.</span><span class="sxs-lookup"><span data-stu-id="58da7-173">The **Templates** page will display a list of document templates that have already been defined.</span></span>

1.  <span data-ttu-id="58da7-174">**Klicken Sie auf "Neue Vorlage", um eine neue Vorlage für Freitextrechnungen zu erstellen.**</span><span class="sxs-lookup"><span data-stu-id="58da7-174">To create a new document template, click **New Template**.</span></span>

1.  <span data-ttu-id="58da7-175">Klicken Sie auf **Erstellen**, und geben Sie einen eindeutigen Namen für das Kriterium ein.</span><span class="sxs-lookup"><span data-stu-id="58da7-175">Enter a unique name for the template and click **Create**.</span></span>

1.  <span data-ttu-id="58da7-176">Verwenden Sie den Rich-Text-Editor, um den Angebotsunterlageinhalt einzufügen oder zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="58da7-176">Use the rich text editor to insert or edit the offer document content.</span></span> <span data-ttu-id="58da7-177">Sie können Tabellen, Bilder und Links unter Verwendung der Optionen einfügen, die oben im Text-Editors verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="58da7-177">You can insert tables, images, and hyperlinks using the options available at the top of the text editor.</span></span>

1.  <span data-ttu-id="58da7-178">Sie können Angebotdatenenplatzhalter im Angebotvorlagendokument wie folgt eingefügt:</span><span class="sxs-lookup"><span data-stu-id="58da7-178">You can insert offer data placeholders in the offer template document by:</span></span>

    - <span data-ttu-id="58da7-179">Drag & Drop vom rechten Bereich.</span><span class="sxs-lookup"><span data-stu-id="58da7-179">Dragging and dropping from the right pane.</span></span>

    - <span data-ttu-id="58da7-180">Hashtag der Angebotdatenenplatzhalter direkt in Position.</span><span class="sxs-lookup"><span data-stu-id="58da7-180">Hashtag the offer data placeholder directly into position.</span></span> <span data-ttu-id="58da7-181">Typ **\#** und dann starten Sie das Eingeben des Namens des Angebotsdatenenplatzhalters.</span><span class="sxs-lookup"><span data-stu-id="58da7-181">Type **\#** and then start typing the name of the offer data placeholder.</span></span> <span data-ttu-id="58da7-182">Wählen Sie in der Dropdownliste eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="58da7-182">Options will appear in the drop-down list.</span></span> <span data-ttu-id="58da7-183">Klicken Sie oder drücken Sie **Eingeben**, um den Angebotdatenenplatzhalter einzufügen.</span><span class="sxs-lookup"><span data-stu-id="58da7-183">Click or press **Enter** to insert the offer data placeholder.</span></span>

    >[!NOTIZEN]
    > - <span data-ttu-id="58da7-185">Um einen Platzhalter der Angebotsunterlagevorlage zuzuordnen ohne den Wert dem Kandidaten zu zeigen, gehen Sie zu Ddatenenplatzhalter und klicken Sie auf das Symbol **Anheften**.</span><span class="sxs-lookup"><span data-stu-id="58da7-185">To associate a placeholder to the offer document template without exposing its value to the candidate, hover over the offer data placeholder and click the **Pin** icon.</span></span> <span data-ttu-id="58da7-186">Dies überträgt den einzufügenden dem Abschnitt **Fixierte Angebotdaten** der Angebotsunterlagevorlage.</span><span class="sxs-lookup"><span data-stu-id="58da7-186">This will push the placeholder to the **Pinned offer data** section of the offer document template.</span></span> <span data-ttu-id="58da7-187">Zum Aufheben, führen Sie die selben Schritte aus aber klicken Sie **Markierung aufheben** in der Liste der Angebotsdatenenplatzhalter.</span><span class="sxs-lookup"><span data-stu-id="58da7-187">To unpin, follow the same steps but click **Unpin** in the list of offer data placeholders.</span></span>

    > - <span data-ttu-id="58da7-188">Um die Liste aktiver Angebotdatenenplatzhalter anzuzeigen, wechseln Sie zur Registerkarte **Aktiv** im rechten Bereich.</span><span class="sxs-lookup"><span data-stu-id="58da7-188">To view the list of active offer data placeholders, switch to the **Active** tab in the right pane.</span></span>

    > - <span data-ttu-id="58da7-189">Wenn Sie einen Platzhalter einfügen, der durch eine Angebotdatenregelsatz gesteuert wird, können Sie diese Abhängigkeit dieses Angebotdatenenplatzhalters auf anderen Werten finden.</span><span class="sxs-lookup"><span data-stu-id="58da7-189">If you insert a placeholder that is driven by an offer data rule set, you can see the dependency of that offer data placeholder on other values.</span></span>

    > - <span data-ttu-id="58da7-190">Sie können den Inhalt von einer .doxc-Datei auf Ihren lokalen Rechner **Importieren** und nach Bedarf bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="58da7-190">Alternatively, you can **Import** the content from a .docx file on your local machine and edit as required.</span></span> <span data-ttu-id="58da7-191">Deshalb müssen Sie auch den gesamten Inhalt im Editor nicht eingeben.</span><span class="sxs-lookup"><span data-stu-id="58da7-191">That way, you don’t have to type in all the content in the editor.</span></span>

1. <span data-ttu-id="58da7-192">Um die Angebotsunterlage in der Vorschau anzuzeigen, können Sie die Option **Vorschau** oben auf der Seite nutzen.</span><span class="sxs-lookup"><span data-stu-id="58da7-192">To preview the offer document, use the **Preview** option at the top of the page.</span></span>

1. <span data-ttu-id="58da7-193">Wenn Sie steuern, ob ein Angebotersteller die Angebotsunterlageinhalte bearbeiten kann, können Sie die Option **Verwalten Sie die Berechtigung** oben der Seite nutzen.</span><span class="sxs-lookup"><span data-stu-id="58da7-193">To control whether an offer creator can edit the offer document content, use the **Manage permission** option at the top of the page.</span></span> <span data-ttu-id="58da7-194">Wenn Sie möchten, dass der Angebotersteller nur Platzhalterwerte einfügen und keine Texte bearbeiten kann, legen Sie den Berechtigungswert auf **Nein** fest.</span><span class="sxs-lookup"><span data-stu-id="58da7-194">If you want the offer creator to only insert placeholder values and not edit text, set the permission value to **No**.</span></span>

1. <span data-ttu-id="58da7-195">Klicken Sie auf **Speichern**, um den Fortschritt zu speichern.</span><span class="sxs-lookup"><span data-stu-id="58da7-195">Click **Save** to save your progress.</span></span> <span data-ttu-id="58da7-196">Die Vorlage wird in einem Entwurfstatus gespeichert.</span><span class="sxs-lookup"><span data-stu-id="58da7-196">The template will be saved in a draft state.</span></span>

1. <span data-ttu-id="58da7-197">Um das Dokument fertigzustellen und es als veröffentlicht zu markieren, klicken Sie auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="58da7-197">To finalize and mark the document as published, click **Finish**.</span></span>

1. <span data-ttu-id="58da7-198">Sie können sehen, welche Dokumentvorlagen derzeit aktiv nd s usind im Entwurfmodus und archiviert wurden und nicht mehr in der Dokumentvorlagenbibliotheks-Landungserfahrung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="58da7-198">You can see which document templates are currently active, in draft mode, and have been archived and are no longer in use on the document templates library landing experience.</span></span>

>[!NOTE]
> <span data-ttu-id="58da7-199">Sie können jede Angebotsunterlagenvorlage löschen, die nicht Teil einer vorhandenen Angebotpaketvorlage ist.</span><span class="sxs-lookup"><span data-stu-id="58da7-199">You can delete any offer document template that is not part of an existing offer package template.</span></span>


## <a name="offer-package-templates"></a><span data-ttu-id="58da7-200">Angebotsvorlagenpaket</span><span class="sxs-lookup"><span data-stu-id="58da7-200">Offer package templates</span></span>

<span data-ttu-id="58da7-201">Angebotpakete sind die Angebotartefakte, die mit den Kandidaten geteilt werden und aus einer Kombination von einer oder mehrer Angebotsvorlagen besteht.</span><span class="sxs-lookup"><span data-stu-id="58da7-201">Offer packages are the offer artifacts that are shared with the candidate and consist of a combination of one or more offer document templates.</span></span> <span data-ttu-id="58da7-202">Um eine Angebotsvorlage zu erstellen, gehen Sie folgendermaßen vor.</span><span class="sxs-lookup"><span data-stu-id="58da7-202">To create an offer package, do the following.</span></span>

1.  <span data-ttu-id="58da7-203">Gehen Sie zu **Management anbieten**.</span><span class="sxs-lookup"><span data-stu-id="58da7-203">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="58da7-204">Gehen Sie zu **Pakete** im linken Navigationsbereich.</span><span class="sxs-lookup"><span data-stu-id="58da7-204">Go to **Packages** from the left navigation pane.</span></span>

    <span data-ttu-id="58da7-205">Eine Liste aktiver Paketvorlagen, die für Angebotersteller zur Nutzung verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="58da7-205">A list of active package templates that are available for offer creators to use is displayed.</span></span>

1.  <span data-ttu-id="58da7-206">Wenn Sie ein neues Angebotpaket erstellen, klicken Sie auf **Neues Paket**</span><span class="sxs-lookup"><span data-stu-id="58da7-206">To create a new offer package, click **New Package**.</span></span>

1.  <span data-ttu-id="58da7-207">Geben Sie einen eindeutigen Namen ein und klicken Sie auf **Erstellen**.</span><span class="sxs-lookup"><span data-stu-id="58da7-207">Enter a unique name and click **Create**.</span></span>

1.  <span data-ttu-id="58da7-208">Klicken Sie auf **Vorlage hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="58da7-208">Click **Add template**.</span></span>

    >[!NOTIZEN]
    > - <span data-ttu-id="58da7-210">Sie können eine vorhandenen Vorlage auswählen, um eine neue Vorlage zu erstellen oder eine bestehende verwenden.</span><span class="sxs-lookup"><span data-stu-id="58da7-210">You can choose to create a new template or choose from an existing one.</span></span>

    > - <span data-ttu-id="58da7-211">Wenn Sie sich entschieden haben, eine vorhandene Vorlage hinzuzufügen, müssen Sie prüfen, ob die Angebotsunterlagevorlage gespeichert, abgeschlossen oder als aktiv markiert wurde.</span><span class="sxs-lookup"><span data-stu-id="58da7-211">If you choose to add an existing template, you need to make sure that the   offer document template was saved, finalized, and marked as   active.</span></span>
    
    > - <span data-ttu-id="58da7-212">Sie können beliebig viele Dokumentvorlagen auswählen.</span><span class="sxs-lookup"><span data-stu-id="58da7-212">You can choose as many document templates as you want.</span></span> 
    
1.  <span data-ttu-id="58da7-213">Klicken Sie auf **Fertig**, um zur **Paketverwaltung** zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="58da7-213">Click **Done** to return to **Package management**.</span></span>

    <span data-ttu-id="58da7-214">Sie können die Sequenz von Dokumenten konfigurieren und auch festlegen, ob die Angebotsunterlage für bestimmte Angeboterstellungen erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="58da7-214">You can configure the sequence of the documents and also mark whether the specific offer document is required during offer creation.</span></span> <span data-ttu-id="58da7-215">Der Angebotersteller hat die Option, Dokumente zu löschen, die als **Nicht erforderlich** markiert sind.</span><span class="sxs-lookup"><span data-stu-id="58da7-215">The offer creator will have an option to delete the documents marked as **Not required**.</span></span>

1. <span data-ttu-id="58da7-216">Um die Angebotpaketvorlage zu speichern, damit sie von anderen Angebotersteller verwendbar ist, klicken Sie auf **Speichern und Veröffentlichen**.</span><span class="sxs-lookup"><span data-stu-id="58da7-216">To save the offer package template so that it's usable by all offer creators, click **Save and publish**.</span></span>

   <span data-ttu-id="58da7-217">Um Entwurf-Paketvorlagen anzuzeigen, navigieren Sie zur Registerkarte **Entwürfe**.  Wenn eine Änderung an der Angebotpaketvorlage vorgenommen wird, muss sie erneut gespeichert und veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="58da7-217">To view draft offer package templates, go to the **Drafts** tab. If a change is made to the offer package template, it must be  saved and republished.</span></span>

## <a name="configure-an-offer-process"></a><span data-ttu-id="58da7-218">Konfigurieren eines Angebotsprozesses</span><span class="sxs-lookup"><span data-stu-id="58da7-218">Configure an offer process</span></span>

<span data-ttu-id="58da7-219">Es gibt verschiedene Teile des Angeboterstellungsprozesses, der von einem Attract-Administrator konfiguriert werden kann.</span><span class="sxs-lookup"><span data-stu-id="58da7-219">There are several parts of the offer creation process that can be configured by an Attract administrator.</span></span>

- <span data-ttu-id="58da7-220">**Angebotgenehmigungen** - Wählen Sie, ob Angebotgenehmigungen erforderlich sind, bevor das Angebot an den Kandidaten gesendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="58da7-220">**Offer approvals** - Choose whether offer approvals are required before the offer can be sent to the candidate.</span></span> <span data-ttu-id="58da7-221">Als Administrator können Sie auch festlegen, ob alle Angebotgenehmigungen in einer Sequenzkennung  oder einem parallelen Genehmigungsworkflow geschehen.</span><span class="sxs-lookup"><span data-stu-id="58da7-221">As an administrator, you can also decide whether all offer approvals will happen in a sequential manner or parallel approval workflow.</span></span> <span data-ttu-id="58da7-222">Sie können vorgeben, ob auch Angebotgenehmiger einen Kommentar zusammen mit der Angebotgenehmigung hinzufügen müssen.</span><span class="sxs-lookup"><span data-stu-id="58da7-222">You can also mandate whether offer approvers must add a comment along with their offer approval.</span></span> <span data-ttu-id="58da7-223">Angebotgenehmigungen sind für alle Angebote zwingend, die nicht Standard sind.</span><span class="sxs-lookup"><span data-stu-id="58da7-223">Offer approvals are mandatory for all non-standard offers.</span></span>

- <span data-ttu-id="58da7-224">**Angeboterfahrung des Kandidaten** - Als Administrator, können Sie auswählen, ob alle Angebote ein Ablaufdatum haben, und falls ja, wofür das Standardgegenkonto für das Ablaufdatum sein soll.</span><span class="sxs-lookup"><span data-stu-id="58da7-224">**Candidate’s offer experience** - As administrator, you can choose to set whether all offers have an expiration date, and if so, what the default offset for the expiration date should be.</span></span> <span data-ttu-id="58da7-225">Sie können auch konfigurieren, ob Kandidaten ein Angebot ablehnen können.</span><span class="sxs-lookup"><span data-stu-id="58da7-225">You can also configure whether candidates can decline an offer.</span></span>

- <span data-ttu-id="58da7-226">**E-Unterschriften** - Zurzeit ist die einzige verfügbare Option für die elektronischen Signatur, dass Kandidaten ihren Namen im Angebotpaket bei Annahme des Angebots eingeben.</span><span class="sxs-lookup"><span data-stu-id="58da7-226">**e-Signatures** - Currently, the only electronic signature option available is for candidates to type their name in the offer package while accepting the offer.</span></span> <span data-ttu-id="58da7-227">Wir lancieren Partnersintegrationen mit anderen Anbietern der elektronischen Signatur in der Zukunft.</span><span class="sxs-lookup"><span data-stu-id="58da7-227">We will introduce partner integrations with other electronic signature providers in the future.</span></span>


<span data-ttu-id="58da7-228">Weitere Informationen zu den Angeboterstellungsprozessund  finden Sie unter [Erstellen, genehmigen und unterzeichnen von Angeboten ](./creating-offers.md).</span><span class="sxs-lookup"><span data-stu-id="58da7-228">To learn more about the offer creation process, see [Creating, approving, and signing offers](./creating-offers.md).</span></span>

