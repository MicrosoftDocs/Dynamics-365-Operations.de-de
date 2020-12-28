---
title: Angebotsmanagement in Attract einrichten
description: In diesem Thema wird beschrieben, wie Angebote in Microsoft Dynamics 365 Talent eingerichtet werden.
author: andreabichsel
manager: AnnBe
ms.date: 12/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-18
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bc91a83afd5ce1627376685bcf612d6998ddbc02
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461271"
---
# <a name="set-up-offer-management-in-attract"></a><span data-ttu-id="d31f8-103">Angebotsmanagement in Attract einrichten</span><span class="sxs-lookup"><span data-stu-id="d31f8-103">Set up offer management in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d31f8-104">Wenn ein Kandidat auf die Angebotsphase in Dynamics 365 Talent: Attract verschoben wird, müssen Sie sicherstellen, dass die Angebote für den Kandidaten schnell nach Bedarf erstellt, genehmigt und dem Kandidaten gesendet werden können.</span><span class="sxs-lookup"><span data-stu-id="d31f8-104">When a candidate is moved to the offer stage in Dynamics 365 Talent: Attract, you need to ensure that the offers can be quickly created for the candidate, approved as necessary, and sent out to the candidate.</span></span> <span data-ttu-id="d31f8-105">Da die meisten Angebote standardmäßig sind, können Sie aus wiederverwendbaren Vorlagen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d31f8-105">Because most offers are standard, they can be created from reusable templates.</span></span> <span data-ttu-id="d31f8-106">In Attract werden alle Angebote in ein Angebotspaket verschoben, das eine Zusammenstellung eines oder mehrerer Angebotsunterlagen ist.</span><span class="sxs-lookup"><span data-stu-id="d31f8-106">In Attract, all offers are rolled into an offer package, which is a collection of one or more offer documents.</span></span> 

<span data-ttu-id="d31f8-107">Dieses Thema führt alle Schritte auf, denen ein Attract-Administrator folgen würde, um verschiedene Angebotpaketvorlagen als Teil der Angebotsverwaltung einzurichten in Attract.</span><span class="sxs-lookup"><span data-stu-id="d31f8-107">This topic lists all the steps that an Attract administrator would follow to set up different offer package templates as part of the offer management capability in Attract.</span></span> <span data-ttu-id="d31f8-108">Benutzer mit Nicht-Administrator-Rollen haben keinen Zugriff zu diesen Funktionen.</span><span class="sxs-lookup"><span data-stu-id="d31f8-108">Users with non-administrator roles will not have access to these capabilities.</span></span>

>[!NOTE]
> <span data-ttu-id="d31f8-109">Angebotsverwaltungsfunktionen werden als Teil für das Einstellungsadd-on verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d31f8-109">Offer management capabilities are available as part of the Comprehensive Hiring Add-On.</span></span>

## <a name="offer-data"></a><span data-ttu-id="d31f8-110">Angebotsdaten</span><span class="sxs-lookup"><span data-stu-id="d31f8-110">Offer data</span></span> 

<span data-ttu-id="d31f8-111">Angebotdaten sind die kleinste Einheit in der Angebotpaketvorlage.</span><span class="sxs-lookup"><span data-stu-id="d31f8-111">Offer data is the smallest unit inside the offer package template.</span></span> <span data-ttu-id="d31f8-112">Ein typisches Angebot besteht aus Standardtext und aus einer Gruppe von Werten.</span><span class="sxs-lookup"><span data-stu-id="d31f8-112">A typical offer consists of standard text and a set of values.</span></span> <span data-ttu-id="d31f8-113">Die Gruppen der Werte sind die einzelnen Bestandteile, die zwischen Angeboten ändern können.</span><span class="sxs-lookup"><span data-stu-id="d31f8-113">The sets of values are the only pieces that could change between offers.</span></span> <span data-ttu-id="d31f8-114">Während der Angeboterstellung ist der wichtigste Aspekt, auf den sich der Angebotersteller fokussieren kann, die Liste der Angebotdatenenplatzhaltern, die in einer Angebotpaketvorlage vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="d31f8-114">During the offer creation, the most important aspect that the offer creator can focus on is the list of offer data placeholders present in an offer package template.</span></span> <span data-ttu-id="d31f8-115">Um Angebotdaten einzurichten, gehen Sie folgendermaßen vor.</span><span class="sxs-lookup"><span data-stu-id="d31f8-115">To set up offer data, do the following.</span></span>

1.  <span data-ttu-id="d31f8-116">Gehen Sie zu **Management anbieten**.</span><span class="sxs-lookup"><span data-stu-id="d31f8-116">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="d31f8-117">Erweitern Sie den Bereich **Bibliothek** im linken Navigationsbereich, und fahren Sie mit **Angebotdaten** fort.</span><span class="sxs-lookup"><span data-stu-id="d31f8-117">Expand the **Library** section in the left navigation pane, then go to **Offer data**.</span></span>

    >[!NOTE]
    > <span data-ttu-id="d31f8-118">Auf der Seite **Daten anbieten** werden die Abschnitte **Kandidatendetails** und **Stellendetails** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d31f8-118">On the **Offer data** page are the **Candidate details** and **Job details** sections.</span></span> <span data-ttu-id="d31f8-119">Attract stellt einige Daten-Platzhalterstandards bereit.</span><span class="sxs-lookup"><span data-stu-id="d31f8-119">Attract provides a few offer data placeholders out-of-the-box.</span></span>
    > 
    > <span data-ttu-id="d31f8-120">Es gibt Abschnitte auf der Seite, um die verschiedenen Angebotsdatenenplatzhalter zusammen mit den logischen Gruppen zu organisieren.</span><span class="sxs-lookup"><span data-stu-id="d31f8-120">There are sections on the page to organize different offer data placeholders together in logical groups.</span></span> <span data-ttu-id="d31f8-121">Diese Bereiche können bei der Verwaltung von Angebotdaten und beim Auffüllen von Daten während des Angebotserstellungsprozesses helfen.</span><span class="sxs-lookup"><span data-stu-id="d31f8-121">These sections can help with maintenance of offer data and population of data during the offer creation process.</span></span>
    > 
    > <span data-ttu-id="d31f8-122">Laden Sie zum Erstellen einer Werteliste für einen Platzhalter eine Excel-Tabelle hoch, die eine Spalte mit dem Platzhalter als Spaltentitel und der Auswahlliste in den Zeilen darunter enthält.</span><span class="sxs-lookup"><span data-stu-id="d31f8-122">To create a list of values for a placeholder, upload an Excel spreadsheet that has one column with the placeholder as the column title and the list of choices in the rows underneath.</span></span> <span data-ttu-id="d31f8-123">Wenn derselbe Platzhalter in einem anderen Datenregelsatz referenziert wird, stellen Sie sicher, dass diese einen gemeinsamen Wertesatz haben.</span><span class="sxs-lookup"><span data-stu-id="d31f8-123">If the same placeholder is referenced in another data rule set, ensure they have a common set of values.</span></span>
    
1.  <span data-ttu-id="d31f8-124">Zum Erstellen eines neuen Angebotsdatenabschnittes klicken Sie auf **Fügen Sie einen Abschnitt hinzu**, und geben Sie einen eindeutigen Namen für den Bereich ein.</span><span class="sxs-lookup"><span data-stu-id="d31f8-124">To create a new offer data section, click **Add a section** and enter a unique name for the section.</span></span>

1.  <span data-ttu-id="d31f8-125">Um Angebotsdatenenplatzhalter jedem Bereich hinzuzufügen, klicken Sie auf **Fügen Sie Angebotsdaten hinzu** und geben Sie einen eindeutigen Namen für den Platzhalter ein.</span><span class="sxs-lookup"><span data-stu-id="d31f8-125">To add offer data placeholders to any section, click **Add offer data** and enter a unique name for the placeholder.</span></span>

1.  <span data-ttu-id="d31f8-126">Wenn Sie den Namen eines Abschnitts bearbeiten, fahren Sie über den Abschnittsnamen und aktualisieren Sie den Namen.</span><span class="sxs-lookup"><span data-stu-id="d31f8-126">To edit the name of any section, hover over the section name and update the name.</span></span>

1.  <span data-ttu-id="d31f8-127">Um den Namen aller vorhandenen Angebotsdatenenplatzhalter zu bearbeiten, sollten Sie zunächst sicherstellen, dass der Platzhalter nicht bereits Teil einer Vorlage ist.</span><span class="sxs-lookup"><span data-stu-id="d31f8-127">To edit the name of any existing offer data placeholder, first make sure that the placeholder is not already part of any template.</span></span> <span data-ttu-id="d31f8-128">Anschließend fahren Sie über den Namen der Angebotsdatenplatzhalter und aktualisieren Sie den Namen nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="d31f8-128">Then, hover over the name of the offer data placeholder and update the name as needed.</span></span>

1. <span data-ttu-id="d31f8-129">Um den Namen aller vorhandenen Angebotsdatenenplatzhalter zu löschen, sollten Sie zunächst sicherstellen, dass der Platzhalter nicht bereits Teil einer anderen Vorlage ist.</span><span class="sxs-lookup"><span data-stu-id="d31f8-129">To delete an existing offer data placeholder, first make sure that the placeholder is not part of any other template.</span></span> <span data-ttu-id="d31f8-130">Anschließend fahren Sie mit dem Mauszeigers über den Platzhalter und wenn das Abfalleimersymbol erscheint, klicken Sie auf den Abfalleimer, um den Angebotsdatenenplatzhalter zu löschen.</span><span class="sxs-lookup"><span data-stu-id="d31f8-130">Then, hover over the placeholder and when the trash can icon appears, click the trash can to delete the offer data placeholder.</span></span>
    >[!NOTE]
    > <span data-ttu-id="d31f8-131">Sie können sehen, wie viele Vorlagen ein Angebotsdatenenplatzhalter Teil vom Nummerindikator neben den Angebotsdaten ist.</span><span class="sxs-lookup"><span data-stu-id="d31f8-131">You can see how many templates an offer data placeholder is part of by the number indicator next to each offer data.</span></span> 

1. <span data-ttu-id="d31f8-132">Wenn Sie einen Abschnitt löschen, fahren Sie über den Namen.</span><span class="sxs-lookup"><span data-stu-id="d31f8-132">To delete any section, hover over the name.</span></span> <span data-ttu-id="d31f8-133">Wenn keine der Angebotdatenenplatzhalter innerhalb des Bereichs in jeder Vorlage angezeigt werden, können Sie auf das Abfalleimersymbol klicken, um sie zu löschen.</span><span class="sxs-lookup"><span data-stu-id="d31f8-133">If none of the offer data placeholders inside the section appear in any template, you can click the trash can icon to delete it.</span></span> 
    >[!NOTE]
    > <span data-ttu-id="d31f8-134">Mit dem Löschen des Abschnitts werden auch alle Angebotsdaten-Platzhalter im Bereich gelöscht.</span><span class="sxs-lookup"><span data-stu-id="d31f8-134">Deleting the section will also delete all the offer data placeholders inside that section.</span></span>

<span data-ttu-id="d31f8-135">Nachdem die Angebotdatenenplatzhalter eingerichtet wurden, können Sie diese zu einer beliebigen Dokumentvorlage verwenden.</span><span class="sxs-lookup"><span data-stu-id="d31f8-135">After the offer data placeholders have been set up, you can use them across any document template.</span></span> <span data-ttu-id="d31f8-136">Angebotdatenenplatzhalter werden nicht auf eine bestimmte Vorlage beschränkt -- dieselbe Definition kann für alle Vorlagen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d31f8-136">Offer data placeholders are not restricted to a specific template -- the same set can be used across all templates.</span></span>

## <a name="offer-data-rules"></a><span data-ttu-id="d31f8-137">Angebotdatenregeln</span><span class="sxs-lookup"><span data-stu-id="d31f8-137">Offer data rules</span></span>

<span data-ttu-id="d31f8-138">Die meisten Organisation haben Regeln dazu, wie Angebote erstellt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="d31f8-138">Most organization have rules for how offers must be created.</span></span> <span data-ttu-id="d31f8-139">Zum Beispiel möchte eine Organisation, dass das maximale Angebot des jährlichen Gehalts für einen bestimmten Standort und ein bestimmtes Dienstalters innerhalb eines bestimmten Bereichs liegt oder dass nur wenige bestimmte Werte für die Angebotsebene für den neuen Mitarbeiter möglich sind.</span><span class="sxs-lookup"><span data-stu-id="d31f8-139">For example, an organization may want to require that the maximum annual salary offer for a specific location and seniority level combination has to be within a certain range, or that there are only a few specific values possible for the offer level for the new hire.</span></span> <span data-ttu-id="d31f8-140">Attract unterstützt derzeit all diese Datenregeln mithilfe einer CSV-Datei.</span><span class="sxs-lookup"><span data-stu-id="d31f8-140">Attract currently supports all such data rules using a CSV file.</span></span>

<span data-ttu-id="d31f8-141">Um die Datenregeln für die CSV-Datei zu erstellen, gehen Sie folgendermaßen vor.</span><span class="sxs-lookup"><span data-stu-id="d31f8-141">To prepare the data rules CSV file, do the following.</span></span>

1.  <span data-ttu-id="d31f8-142">Festlegen der Angebotdatenenplatzhalter für die Regelsammlung.</span><span class="sxs-lookup"><span data-stu-id="d31f8-142">Determine the offer data placeholder for the rule set.</span></span> <span data-ttu-id="d31f8-143">Zum Beispiel **Jährliches Gehalt**.</span><span class="sxs-lookup"><span data-stu-id="d31f8-143">For example, **Annual Salary**.</span></span>

1.  <span data-ttu-id="d31f8-144">Definieren Sie die Angebotsdaten-Platzhalterwerte.</span><span class="sxs-lookup"><span data-stu-id="d31f8-144">Identify the dependent offer data placeholder values.</span></span> <span data-ttu-id="d31f8-145">Zum Beispiel **Arbeitsort** und **Ebene**.</span><span class="sxs-lookup"><span data-stu-id="d31f8-145">For example, **Job Location** and **Level**.</span></span>

1.  <span data-ttu-id="d31f8-146">Geben Sie Spalten 1 und 2 als **Arbeitsort** und **Ebene** an.</span><span class="sxs-lookup"><span data-stu-id="d31f8-146">Specify columns 1 and 2 as **Job Location** and **Level**.</span></span>

1.  <span data-ttu-id="d31f8-147">Um einen Bereichswert hochzuladen, machen Sie Spalten 3 und 4 für **Jährliches Gehalt**.</span><span class="sxs-lookup"><span data-stu-id="d31f8-147">To upload a range value, make columns 3 and 4 **Annual Salary**.</span></span> <span data-ttu-id="d31f8-148">Um einen bestimmten Wert anstelle eines Bereichs hochladen, lassen Sie nur Spalte 3 **Jährliches Gehalt**.</span><span class="sxs-lookup"><span data-stu-id="d31f8-148">To upload a specific value instead of a range, only make column 3 **Annual Salary**.</span></span>

1.  <span data-ttu-id="d31f8-149">Füllen Sie die Microsoft Excel-Dateien auf Grundlage der notwendigen Rollen auf.</span><span class="sxs-lookup"><span data-stu-id="d31f8-149">Populate the Microsoft Excel file based on your required roles.</span></span>

1.  <span data-ttu-id="d31f8-150">Sicherstellen, dass jede Zeile eine eindeutige Kombination aller Werte ist, die zusammengestellt werden.</span><span class="sxs-lookup"><span data-stu-id="d31f8-150">Ensure that each row is a unique combination of all the values put together.</span></span>

1.  <span data-ttu-id="d31f8-151">Speichern Sie die Datei als CSV-Format.</span><span class="sxs-lookup"><span data-stu-id="d31f8-151">Save the file as a CSV format.</span></span>

<span data-ttu-id="d31f8-152">Um die Datenregeln für die CSV-Datei zu erstellen, gehen Sie folgendermaßen vor.</span><span class="sxs-lookup"><span data-stu-id="d31f8-152">To upload the offer data rules file, do the following.</span></span>

1.  <span data-ttu-id="d31f8-153">Gehen Sie zu **Management anbieten**.</span><span class="sxs-lookup"><span data-stu-id="d31f8-153">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="d31f8-154">Erweitern Sie den Bereich **Bibliothek** im linken Navigationsbereich, und fahren Sie mit **Angebotdatenregeln** fort.</span><span class="sxs-lookup"><span data-stu-id="d31f8-154">Expand the **Library** section in the left navigation panel, then go to **Offer data rules**.</span></span>

1.  <span data-ttu-id="d31f8-155">Klicken Sie auf **Neuer Datensatz**, um das Dialogfeld **Hochladen** anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d31f8-155">Click **New data set** to display the **Upload** dialog box.</span></span>

1.  <span data-ttu-id="d31f8-156">Geben Sie einen eindeutigen Namen für den Regelsatz an und laden Sie dann die gespeicherte CSV-Datei hoch.</span><span class="sxs-lookup"><span data-stu-id="d31f8-156">Specify a unique name for the rule set and then upload the saved CSV file.</span></span>

1.  <span data-ttu-id="d31f8-157">Klicken Sie auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="d31f8-157">Click **Add**.</span></span>
    <span data-ttu-id="d31f8-158">Die Regelsammlung wird im Hintergrund verarbeitet und Sie sind InApp gemeldete und per E-Mail, sobald diese ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="d31f8-158">The rule set will be processed in the background and you will be notified in-app and via email once it completes.</span></span>

    <span data-ttu-id="d31f8-159">Sie werden benachrichtigt, wenn es Fehler beim Verarbeiten des Uploads gibt.</span><span class="sxs-lookup"><span data-stu-id="d31f8-159">You will be notified if there are errors while processing the upload.</span></span> <span data-ttu-id="d31f8-160">Sie können das Fehlerprotokoll dann herunterladen, die Datei reparieren und erneut hochladen.</span><span class="sxs-lookup"><span data-stu-id="d31f8-160">You can then download the error log, fix the file, and upload it again.</span></span>

1.  <span data-ttu-id="d31f8-161">Verwenden Sie die Optionsschaltfläche der Auslassungspunkte (**...**), wenn Sie den Regelsatz herunterladen und die Werte aktualisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="d31f8-161">Use the ellipses button (**…**) option if you want to download the rule set and update the set of values.</span></span> <span data-ttu-id="d31f8-162">Nach der Aktualisierung können Sie die Datei erneut hochladen.</span><span class="sxs-lookup"><span data-stu-id="d31f8-162">After updating, you can upload the file again.</span></span>

1.  <span data-ttu-id="d31f8-163">Sie können einen vorhandenen Regelsatzupload löschen, wenn der Platzhalter, der definiert ist, von keiner anderen Dokumentvorlage verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d31f8-163">You can delete an existing rule set upload if the placeholder being defined is not being used in another document template.</span></span>

>[!NOTE]
> - <span data-ttu-id="d31f8-164">Jeder Platzhalter kann einen eindeutigen Satz Spalten haben, der davon abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="d31f8-164">Each placeholder can only have one unique set of columns that it is dependent on.</span></span> <span data-ttu-id="d31f8-165">Wenn beispielsweise **Jährliches Gehalt** **Arbeitsort** **Ebene** abhängig ist, können Sie einen anderen Regelsatz nicht hochgeladen, **Jährliches Gehalt** aus einem anderen Satz Spalten abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="d31f8-165">For example, if **Annual Salary** is dependent on **Job Location** and **Level**, you can't upload another rule set where **Annual Salary** is dependent on a different set of columns.</span></span>

> - <span data-ttu-id="d31f8-166">Sie können Beispielangebotdatenregelsätze auf der Registerkarte **Beispiele** auf der Seite **Angebotdatenregeln** herunterladen.</span><span class="sxs-lookup"><span data-stu-id="d31f8-166">You can download sample offer data rule sets on the **Samples** tab on the **Offer data rules** page.</span></span>

> - <span data-ttu-id="d31f8-167">Wenn ein Angebotersteller die Werte überschreibt, die von der Angebotsdatenregeln empfohlen werden, wird das Angebot als Nicht-Standard gekennzeichnet und die Genehmigung des Angebotsgenehmigungsworkflows wird vorgegeben.</span><span class="sxs-lookup"><span data-stu-id="d31f8-167">When an offer creator overrides the values that are recommended by the offer data rules, the offer is flagged as non-standard and offer approval workflow will be mandated.</span></span>

## <a name="document-templates"></a><span data-ttu-id="d31f8-168">Dokumentvorlagen</span><span class="sxs-lookup"><span data-stu-id="d31f8-168">Document templates</span></span>

<span data-ttu-id="d31f8-169">Eine Angebotsunterlagevorlage kann Administratoren helfen, Angebotsschreiben zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d31f8-169">An offer document template can help administrators create offer letters.</span></span> <span data-ttu-id="d31f8-170">Die Angebotsunterlagevorlage ist eine Kombination des Texts, der ein Bestandteil des Angebots und ein  definierter Angebotdatenenplatzhalter ist.</span><span class="sxs-lookup"><span data-stu-id="d31f8-170">The offer document template is a combination of the text that will be part of the offer as well as the defined offer data placeholders.</span></span> 

<span data-ttu-id="d31f8-171">Um eine Angebotsunterlagevorlage zu erstellen, gehen Sie folgendermaßen vor.</span><span class="sxs-lookup"><span data-stu-id="d31f8-171">To create an offer document template, do the following.</span></span>

1.  <span data-ttu-id="d31f8-172">Gehen Sie zu **Management anbieten**.</span><span class="sxs-lookup"><span data-stu-id="d31f8-172">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="d31f8-173">Erweitern Sie den Bereich **Bibliothek** im linken Navigationsbereich, und fahren Sie mit **Vorlage** fort.</span><span class="sxs-lookup"><span data-stu-id="d31f8-173">Expand the **Library** section in the left navigation pane and go to **Templates**.</span></span>

    <span data-ttu-id="d31f8-174">Die Seite **Vorlagen** zeigt eine Liste der Dokumentvorlagen an, die bereits geladen wurden.</span><span class="sxs-lookup"><span data-stu-id="d31f8-174">The **Templates** page will display a list of document templates that have already been defined.</span></span>

1.  <span data-ttu-id="d31f8-175">**Klicken Sie auf "Neue Vorlage", um eine neue Vorlage für Freitextrechnungen zu erstellen.**</span><span class="sxs-lookup"><span data-stu-id="d31f8-175">To create a new document template, click **New Template**.</span></span>

1.  <span data-ttu-id="d31f8-176">Klicken Sie auf **Erstellen**, und geben Sie einen eindeutigen Namen für das Kriterium ein.</span><span class="sxs-lookup"><span data-stu-id="d31f8-176">Enter a unique name for the template and click **Create**.</span></span>

1.  <span data-ttu-id="d31f8-177">Verwenden Sie den Rich-Text-Editor, um den Angebotsunterlageinhalt einzufügen oder zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="d31f8-177">Use the rich text editor to insert or edit the offer document content.</span></span> <span data-ttu-id="d31f8-178">Sie können Tabellen, Bilder und Links unter Verwendung der Optionen einfügen, die oben im Text-Editors verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="d31f8-178">You can insert tables, images, and hyperlinks using the options available at the top of the text editor.</span></span>

1.  <span data-ttu-id="d31f8-179">Sie können Angebotdatenenplatzhalter im Angebotvorlagendokument wie folgt eingefügt:</span><span class="sxs-lookup"><span data-stu-id="d31f8-179">You can insert offer data placeholders in the offer template document by:</span></span>

    - <span data-ttu-id="d31f8-180">Drag & Drop vom rechten Bereich.</span><span class="sxs-lookup"><span data-stu-id="d31f8-180">Dragging and dropping from the right pane.</span></span>

    - <span data-ttu-id="d31f8-181">Hashtag der Angebotdatenenplatzhalter direkt in Position.</span><span class="sxs-lookup"><span data-stu-id="d31f8-181">Hashtag the offer data placeholder directly into position.</span></span> <span data-ttu-id="d31f8-182">Typ **\#** und dann starten Sie das Eingeben des Namens des Angebotsdatenenplatzhalters.</span><span class="sxs-lookup"><span data-stu-id="d31f8-182">Type **\#** and then start typing the name of the offer data placeholder.</span></span> <span data-ttu-id="d31f8-183">Wählen Sie in der Dropdownliste eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="d31f8-183">Options will appear in the drop-down list.</span></span> <span data-ttu-id="d31f8-184">Klicken Sie oder drücken Sie **Eingeben**, um den Angebotdatenenplatzhalter einzufügen.</span><span class="sxs-lookup"><span data-stu-id="d31f8-184">Click or press **Enter** to insert the offer data placeholder.</span></span>

    >[!NOTE]
    > - <span data-ttu-id="d31f8-185">Um einen Platzhalter der Angebotsunterlagevorlage zuzuordnen ohne den Wert dem Kandidaten zu zeigen, gehen Sie zu Ddatenenplatzhalter und klicken Sie auf das Symbol **Anheften**.</span><span class="sxs-lookup"><span data-stu-id="d31f8-185">To associate a placeholder to the offer document template without exposing its value to the candidate, hover over the offer data placeholder and click the **Pin** icon.</span></span> <span data-ttu-id="d31f8-186">Dies überträgt den einzufügenden dem Abschnitt **Fixierte Angebotdaten** der Angebotsunterlagevorlage.</span><span class="sxs-lookup"><span data-stu-id="d31f8-186">This will push the placeholder to the **Pinned offer data** section of the offer document template.</span></span> <span data-ttu-id="d31f8-187">Zum Aufheben, führen Sie die selben Schritte aus aber klicken Sie **Markierung aufheben** in der Liste der Angebotsdatenenplatzhalter.</span><span class="sxs-lookup"><span data-stu-id="d31f8-187">To unpin, follow the same steps but click **Unpin** in the list of offer data placeholders.</span></span>

    > - <span data-ttu-id="d31f8-188">Um die Liste aktiver Angebotdatenenplatzhalter anzuzeigen, wechseln Sie zur Registerkarte **Aktiv** im rechten Bereich.</span><span class="sxs-lookup"><span data-stu-id="d31f8-188">To view the list of active offer data placeholders, switch to the **Active** tab in the right pane.</span></span>

    > - <span data-ttu-id="d31f8-189">Wenn Sie einen Platzhalter einfügen, der durch eine Angebotdatenregelsatz gesteuert wird, können Sie diese Abhängigkeit dieses Angebotdatenenplatzhalters auf anderen Werten finden.</span><span class="sxs-lookup"><span data-stu-id="d31f8-189">If you insert a placeholder that is driven by an offer data rule set, you can see the dependency of that offer data placeholder on other values.</span></span>

    > - <span data-ttu-id="d31f8-190">Sie können den Inhalt von einer .doxc-Datei auf Ihren lokalen Rechner **Importieren** und nach Bedarf bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="d31f8-190">Alternatively, you can **Import** the content from a .docx file on your local machine and edit as required.</span></span> <span data-ttu-id="d31f8-191">Deshalb müssen Sie auch den gesamten Inhalt im Editor nicht eingeben.</span><span class="sxs-lookup"><span data-stu-id="d31f8-191">That way, you don’t have to type in all the content in the editor.</span></span>

1. <span data-ttu-id="d31f8-192">Um die Angebotsunterlage in der Vorschau anzuzeigen, können Sie die Option **Vorschau** oben auf der Seite nutzen.</span><span class="sxs-lookup"><span data-stu-id="d31f8-192">To preview the offer document, use the **Preview** option at the top of the page.</span></span>

1. <span data-ttu-id="d31f8-193">Wenn Sie steuern, ob ein Angebotersteller die Angebotsunterlageinhalte bearbeiten kann, können Sie die Option **Verwalten Sie die Berechtigung** oben der Seite nutzen.</span><span class="sxs-lookup"><span data-stu-id="d31f8-193">To control whether an offer creator can edit the offer document content, use the **Manage permission** option at the top of the page.</span></span> <span data-ttu-id="d31f8-194">Wenn Sie möchten, dass der Angebotersteller nur Platzhalterwerte einfügen und keine Texte bearbeiten kann, legen Sie den Berechtigungswert auf **Nein** fest.</span><span class="sxs-lookup"><span data-stu-id="d31f8-194">If you want the offer creator to only insert placeholder values and not edit text, set the permission value to **No**.</span></span>

1. <span data-ttu-id="d31f8-195">Klicken Sie auf **Speichern**, um den Fortschritt zu speichern.</span><span class="sxs-lookup"><span data-stu-id="d31f8-195">Click **Save** to save your progress.</span></span> <span data-ttu-id="d31f8-196">Die Vorlage wird in einem Entwurfstatus gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d31f8-196">The template will be saved in a draft state.</span></span>

1. <span data-ttu-id="d31f8-197">Um das Dokument fertigzustellen und es als veröffentlicht zu markieren, klicken Sie auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="d31f8-197">To finalize and mark the document as published, click **Finish**.</span></span>

1. <span data-ttu-id="d31f8-198">Sie können sehen, welche Dokumentvorlagen derzeit aktiv nd s usind im Entwurfmodus und archiviert wurden und nicht mehr in der Dokumentvorlagenbibliotheks-Landungserfahrung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d31f8-198">You can see which document templates are currently active, in draft mode, and have been archived and are no longer in use on the document templates library landing experience.</span></span>

>[!NOTE]
> <span data-ttu-id="d31f8-199">Sie können jede Angebotsunterlagenvorlage löschen, die nicht Teil einer vorhandenen Angebotpaketvorlage ist.</span><span class="sxs-lookup"><span data-stu-id="d31f8-199">You can delete any offer document template that is not part of an existing offer package template.</span></span>


## <a name="offer-package-templates"></a><span data-ttu-id="d31f8-200">Angebotsvorlagenpaket</span><span class="sxs-lookup"><span data-stu-id="d31f8-200">Offer package templates</span></span>

<span data-ttu-id="d31f8-201">Angebotpakete sind die Angebotartefakte, die mit den Kandidaten geteilt werden und aus einer Kombination von einer oder mehrer Angebotsvorlagen besteht.</span><span class="sxs-lookup"><span data-stu-id="d31f8-201">Offer packages are the offer artifacts that are shared with the candidate and consist of a combination of one or more offer document templates.</span></span> <span data-ttu-id="d31f8-202">Um eine Angebotsvorlage zu erstellen, gehen Sie folgendermaßen vor.</span><span class="sxs-lookup"><span data-stu-id="d31f8-202">To create an offer package, do the following.</span></span>

1.  <span data-ttu-id="d31f8-203">Gehen Sie zu **Management anbieten**.</span><span class="sxs-lookup"><span data-stu-id="d31f8-203">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="d31f8-204">Gehen Sie zu **Pakete** im linken Navigationsbereich.</span><span class="sxs-lookup"><span data-stu-id="d31f8-204">Go to **Packages** from the left navigation pane.</span></span>

    <span data-ttu-id="d31f8-205">Eine Liste aktiver Paketvorlagen, die für Angebotersteller zur Nutzung verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="d31f8-205">A list of active package templates that are available for offer creators to use is displayed.</span></span>

1.  <span data-ttu-id="d31f8-206">Wenn Sie ein neues Angebotpaket erstellen, klicken Sie auf **Neues Paket**</span><span class="sxs-lookup"><span data-stu-id="d31f8-206">To create a new offer package, click **New Package**.</span></span>

1.  <span data-ttu-id="d31f8-207">Geben Sie einen eindeutigen Namen ein und klicken Sie auf **Erstellen**.</span><span class="sxs-lookup"><span data-stu-id="d31f8-207">Enter a unique name and click **Create**.</span></span>

1.  <span data-ttu-id="d31f8-208">Klicken Sie auf **Vorlage hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="d31f8-208">Click **Add template**.</span></span>

    >[!NOTE]
    > - <span data-ttu-id="d31f8-209">Sie können eine vorhandenen Vorlage auswählen, um eine neue Vorlage zu erstellen oder eine bestehende verwenden.</span><span class="sxs-lookup"><span data-stu-id="d31f8-209">You can choose to create a new template or choose from an existing one.</span></span>

    > - <span data-ttu-id="d31f8-210">Wenn Sie sich entschieden haben, eine vorhandene Vorlage hinzuzufügen, müssen Sie prüfen, ob die Angebotsunterlagevorlage gespeichert, abgeschlossen oder als aktiv markiert wurde.</span><span class="sxs-lookup"><span data-stu-id="d31f8-210">If you choose to add an existing template, you need to make sure that the   offer document template was saved, finalized, and marked as   active.</span></span>
    
    > - <span data-ttu-id="d31f8-211">Sie können beliebig viele Dokumentvorlagen auswählen.</span><span class="sxs-lookup"><span data-stu-id="d31f8-211">You can choose as many document templates as you want.</span></span> 
    
1.  <span data-ttu-id="d31f8-212">Klicken Sie auf **Fertig**, um zur **Paketverwaltung** zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="d31f8-212">Click **Done** to return to **Package management**.</span></span>

    <span data-ttu-id="d31f8-213">Sie können die Sequenz von Dokumenten konfigurieren und auch festlegen, ob die Angebotsunterlage für bestimmte Angeboterstellungen erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="d31f8-213">You can configure the sequence of the documents and also mark whether the specific offer document is required during offer creation.</span></span> <span data-ttu-id="d31f8-214">Der Angebotersteller hat die Option, Dokumente zu löschen, die als **Nicht erforderlich** markiert sind.</span><span class="sxs-lookup"><span data-stu-id="d31f8-214">The offer creator will have an option to delete the documents marked as **Not required**.</span></span>

1. <span data-ttu-id="d31f8-215">Um die Angebotpaketvorlage zu speichern, damit sie von anderen Angebotersteller verwendbar ist, klicken Sie auf **Speichern und Veröffentlichen**.</span><span class="sxs-lookup"><span data-stu-id="d31f8-215">To save the offer package template so that it's usable by all offer creators, click **Save and publish**.</span></span>

   <span data-ttu-id="d31f8-216">Um Entwurf-Paketvorlagen anzuzeigen, navigieren Sie zur Registerkarte **Entwürfe**.  Wenn eine Änderung an der Angebotpaketvorlage vorgenommen wird, muss sie erneut gespeichert und veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="d31f8-216">To view draft offer package templates, go to the **Drafts** tab. If a change is made to the offer package template, it must be  saved and republished.</span></span>

## <a name="configure-an-offer-process"></a><span data-ttu-id="d31f8-217">Konfigurieren eines Angebotsprozesses</span><span class="sxs-lookup"><span data-stu-id="d31f8-217">Configure an offer process</span></span>

<span data-ttu-id="d31f8-218">Es gibt verschiedene Teile des Angeboterstellungsprozesses, der von einem Attract-Administrator konfiguriert werden kann.</span><span class="sxs-lookup"><span data-stu-id="d31f8-218">There are several parts of the offer creation process that can be configured by an Attract administrator.</span></span>

- <span data-ttu-id="d31f8-219">**Angebotgenehmigungen** - Wählen Sie, ob Angebotgenehmigungen erforderlich sind, bevor das Angebot an den Kandidaten gesendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="d31f8-219">**Offer approvals** - Choose whether offer approvals are required before the offer can be sent to the candidate.</span></span> <span data-ttu-id="d31f8-220">Als Administrator können Sie auch festlegen, ob alle Angebotgenehmigungen in einer Sequenzkennung  oder einem parallelen Genehmigungsworkflow geschehen.</span><span class="sxs-lookup"><span data-stu-id="d31f8-220">As an administrator, you can also decide whether all offer approvals will happen in a sequential manner or parallel approval workflow.</span></span> <span data-ttu-id="d31f8-221">Sie können vorgeben, ob auch Angebotgenehmiger einen Kommentar zusammen mit der Angebotgenehmigung hinzufügen müssen.</span><span class="sxs-lookup"><span data-stu-id="d31f8-221">You can also mandate whether offer approvers must add a comment along with their offer approval.</span></span> <span data-ttu-id="d31f8-222">Angebotgenehmigungen sind für alle Angebote zwingend, die nicht Standard sind.</span><span class="sxs-lookup"><span data-stu-id="d31f8-222">Offer approvals are mandatory for all non-standard offers.</span></span>

- <span data-ttu-id="d31f8-223">**Angeboterfahrung des Kandidaten** - Als Administrator, können Sie auswählen, ob alle Angebote ein Ablaufdatum haben, und falls ja, wofür das Standardgegenkonto für das Ablaufdatum sein soll.</span><span class="sxs-lookup"><span data-stu-id="d31f8-223">**Candidate’s offer experience** - As administrator, you can choose to set whether all offers have an expiration date, and if so, what the default offset for the expiration date should be.</span></span> <span data-ttu-id="d31f8-224">Sie können auch konfigurieren, ob Kandidaten ein Angebot ablehnen können.</span><span class="sxs-lookup"><span data-stu-id="d31f8-224">You can also configure whether candidates can decline an offer.</span></span>

- <span data-ttu-id="d31f8-225">**E-Unterschriften** - Als Administrator, können Sie die Methode auswählen, die auch Kandidaten verwenden können, um Angebote zu signieren.</span><span class="sxs-lookup"><span data-stu-id="d31f8-225">**e-Signatures** - As an administrator, you can also choose the method that candidates can use to sign offers.</span></span>
    - <span data-ttu-id="d31f8-226">Adobe Sign- alle Angebotpakete werden auf Adobe Sign übermittelt und unterzeichnet.</span><span class="sxs-lookup"><span data-stu-id="d31f8-226">Adobe Sign - All offer packages will be sent and signed via Adobe Sign.</span></span> <span data-ttu-id="d31f8-227">Jeder Angebotersteller, der die Angebotanforderungen veröffentlicht, muss ein Adobe Sign-Konto haben, um sich mit Attract zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="d31f8-227">Each offer creator publishing the offer needs to have their Adobe Sign account connected to Attract.</span></span> <span data-ttu-id="d31f8-228">Für Adobe Sign-Lizenzen und eine kostenlose Testversion siehe [Link](https://acrobat.adobe.com/us/en/business/integrations/microsoft-dynamics-365-for-talent.html)</span><span class="sxs-lookup"><span data-stu-id="d31f8-228">For Adobe Sign licenses and a free Trial, please visit this [link](https://acrobat.adobe.com/us/en/business/integrations/microsoft-dynamics-365-for-talent.html).</span></span>

    - <span data-ttu-id="d31f8-229">DocuSign - alle Angebotpakete werden auf DocuSign übermittelt und unterzeichnet.</span><span class="sxs-lookup"><span data-stu-id="d31f8-229">DocuSign - All offer packages will be sent and signed via DocuSign.</span></span> <span data-ttu-id="d31f8-230">Jeder Angebotersteller, der die Angebotanforderungen veröffentlicht, muss ein DocuSign-Konto haben, um sich mit Attract zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="d31f8-230">Each offer creator publishing the offer needs to have their DocuSign account connected to Attract.</span></span> 
    
    - <span data-ttu-id="d31f8-231">ESign - Dies ist die Standardeinstellung, wo der Benutzer ein Angebot signieren kann, indem er Namen und Initialen eingibt.</span><span class="sxs-lookup"><span data-stu-id="d31f8-231">ESign - This is the default option, provided out of the box, where the user can sign an offer by typing their name and initials.</span></span>


<span data-ttu-id="d31f8-232">Weitere Informationen zum Prozess der Angebotserstellung finden Sie unter [Angebote erstellen, genehmigen und unterzeichnen](./creating-offers.md).</span><span class="sxs-lookup"><span data-stu-id="d31f8-232">To learn more about the offer creation process, see [Create, approve, and sign offers](./creating-offers.md).</span></span>
