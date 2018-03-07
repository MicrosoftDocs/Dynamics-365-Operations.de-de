---
title: Benutzerdefinierte Felder
description: "In diesem Thema wird gezeigt, wie Microsoft Dynamics 365 for Finance and Operations es mehreren Benutzern ermöglicht, benutzerdefinierten Felder zu erstellen, um die Anwendung für ihre geschäftlichen Bedürfnisse anzupassen."
author: jasongre
manager: AnnBe
ms.date: 01/19/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: SysCustomFieldManageFields
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: Platform update 13
ms.translationtype: HT
ms.sourcegitcommit: ad59346f88b7a5984e16418e2aade7ccaedf180b
ms.openlocfilehash: 142c66c189d6401cfb3db128e45fea6c071e99bf
ms.contentlocale: de-de
ms.lasthandoff: 02/28/2018

---

# <a name="custom-fields"></a><span data-ttu-id="b002c-103">Benutzerdefinierte Felder</span><span class="sxs-lookup"><span data-stu-id="b002c-103">Custom fields</span></span>

[!include[banner](../includes/banner.md)] 

[!include[banner](../includes/pre-release.md)] 

<span data-ttu-id="b002c-104">Während Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, einen umfangreichen Satz von vorkonfigurierten Feldern bietet, um eine große Bandbreite von Geschäftsprozessen zu verwalten, besteht manchmal für ein Unternehmen der Bedarf, zusätzliche Informationen im System nachzuverfolgen.</span><span class="sxs-lookup"><span data-stu-id="b002c-104">While Microsoft Dynamics 365 for Finance and Operations, Enterprise edition provides an extensive set of fields out-of-the-box for managing a broad range of business processes, sometimes there is a need for a company to track additional information in the system.</span></span> <span data-ttu-id="b002c-105">Um diese Anforderung zu erfüllen, ermöglicht es Finance and Operations Ihnen, benutzerdefinierte Felder zu erstellen, um die Anwendung so anzupassen, dass sie zu Ihrem Unternehmen passt, vorausgesetzt Sie haben Berechtigungen für die Funktion.</span><span class="sxs-lookup"><span data-stu-id="b002c-105">To accommodate this need, Finance and Operations allows you to create custom fields to tailor the application to fit your business, provided you have permissions to the feature.</span></span>

<span data-ttu-id="b002c-106">Dieses Video zeigt, wie einfach es ist, ein benutzerdefiniertes Feld einer Seite hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="b002c-106">This video shows how easy it is to add a custom field to a page.</span></span>


> [!Video https://www.youtube.com/embed/gWSGZI9Vtnc]

## <a name="creating-custom-fields"></a><span data-ttu-id="b002c-107">Erstellen benutzerdefinierter Felder</span><span class="sxs-lookup"><span data-stu-id="b002c-107">Creating custom fields</span></span>
<span data-ttu-id="b002c-108">Nachdem Sie zusätzliche Informationen identifiziert haben, die Sie in der Anwendung nachverfolgen möchten, können Sie ein benutzerdefiniertes Feld in der entsprechenden Tabelle erstellen und dieses Feld auf einer Seite verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="b002c-108">After you’ve identified additional information that you would like to track in the application, you can create the custom field on the appropriate table and expose that new field on a page.</span></span>   

<span data-ttu-id="b002c-109">In den folgenden Schritten wird der Prozess zum Erstellen eines benutzerdefinierten Felds und der Platzierung dieses Felds in einem Formular beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b002c-109">The following steps describe the process for creating a custom field and placing that field on a form.</span></span>  

1.   <span data-ttu-id="b002c-110">Navigieren Sie zum Formular, in dem das neue Feld benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="b002c-110">Navigate to the form where the new field is needed.</span></span> 
2.   <span data-ttu-id="b002c-111">Da es das Endziel ist, das benutzerdefinierte Feld in einem Formular verfügbar zu machen, befindet sich der Einstiegspunkt zur Erstellung benutzerdefinierter Felder innerhalb der Personalisierungsoberfläche.</span><span class="sxs-lookup"><span data-stu-id="b002c-111">Because the end goal is to expose the custom field on a form, the entry point for creating custom fields exists inside the personalization experience.</span></span> <span data-ttu-id="b002c-112">Öffnen Sie die Personalisierungssymbolleiste, indem Sie **Optionen** auswählen und dann **Dieses Formular personalisieren**</span><span class="sxs-lookup"><span data-stu-id="b002c-112">Open the personalization toolbar by selecting **Options**, and then **Personalize this form**.</span></span> 
3.   <span data-ttu-id="b002c-113">Klicken Sie auf **Einfügen** und dann auf **Feld**.</span><span class="sxs-lookup"><span data-stu-id="b002c-113">Click **Insert** and then **Field**.</span></span>  
4.   <span data-ttu-id="b002c-114">Wählen Sie im Formular die Region aus, in der Sie das neue Feld verfügbar machen möchten.</span><span class="sxs-lookup"><span data-stu-id="b002c-114">Select the region of the form where you want to expose the new field.</span></span> <span data-ttu-id="b002c-115">Nach der Auswahl wird das Dialogfeld **Felder einfügen** eine Liste vorhandener Feldern anzeigen, die in die ausgewählte Region im Formular eingefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="b002c-115">After selection, the **Insert fields** dialog box will display a list of existing fields that can be inserted into the selected region of the form.</span></span>  
5.   <span data-ttu-id="b002c-116">Stellen Sie sicher, dass das Feld, das Sie interessiert sind, nicht bereits in der Liste vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="b002c-116">Ensure that the field you are interested in does not already exist in the list.</span></span> <span data-ttu-id="b002c-117">Wenn dies der Fall ist, können Sie einfach dieses Feld in der Liste auswählen und auf **Einfügen** klicken.</span><span class="sxs-lookup"><span data-stu-id="b002c-117">If it does, you can simply select that field in the list and click **Insert**.</span></span>   
6.   <span data-ttu-id="b002c-118">Klicken Sie auf die Schaltfläche **Neues Feld erstellen** über der Liste, um den Prozess der Erstellung eines benutzerdefinierten Felds zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="b002c-118">Click the **Create new field** button above the list to initiate the process of creating a custom field.</span></span> <span data-ttu-id="b002c-119">Dadurch wird das Dialogfeld **Neues Feld erstellen** geöffnet.</span><span class="sxs-lookup"><span data-stu-id="b002c-119">This will open the **Create new field** dialog box.</span></span> 

     <span data-ttu-id="b002c-120">Wenn Sie die Schaltfläche **Neues Feld erstellen** nicht sehen, haben Sie nicht die notwendigen Berechtigungen, um diese Funktion zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="b002c-120">If you do not see the **Create new field** button, you do not have the necessary permissions to use this feature.</span></span>  
     
7.   <span data-ttu-id="b002c-121">Geben Sie im Dialogfeld **Neues Feld erstellen** die folgenden Informationen ein.</span><span class="sxs-lookup"><span data-stu-id="b002c-121">In the **Create new field** dialog box, enter the following information.</span></span>
     1.   <span data-ttu-id="b002c-122">Wählen Sie die Datenbanktabelle aus, in der dieses Feld hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b002c-122">Select the database table where this field should be added.</span></span> <span data-ttu-id="b002c-123">Beachten Sie, dass in der Dropdownliste nur Tabellen angezeigt werden, die benutzerdefinierte Felder unterstützen.</span><span class="sxs-lookup"><span data-stu-id="b002c-123">Note that only tables that support custom fields will appear in the drop-down list.</span></span> <span data-ttu-id="b002c-124">Sehen Sie den Abschnitt unten für technische Details zu unterstützen Tabellen.</span><span class="sxs-lookup"><span data-stu-id="b002c-124">See the section below for technical details on supported tables.</span></span>  
     2.   <span data-ttu-id="b002c-125">Wählen Sie den Datentyp für das neue Feld aus.</span><span class="sxs-lookup"><span data-stu-id="b002c-125">Select the data type for the new field.</span></span> <span data-ttu-id="b002c-126">Die verfügbaren Datentypen sind Kontrollkästchen, Datum, Datum/Uhrzeit, Dezimal, Zahl, Auswahlliste und Text.</span><span class="sxs-lookup"><span data-stu-id="b002c-126">The available data types are checkbox, date, date time, decimal, number, picklist, and text.</span></span>   
          - <span data-ttu-id="b002c-127">Wenn Sie den Textdatentyp auswählen, können Sie auch die maximale Länge des Texts angeben, der in diesem Feld eingegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="b002c-127">If you choose the text data type, you can also specify the maximum length of the text that can be entered in this field.</span></span> 
          - <span data-ttu-id="b002c-128">Wenn Sie den Auswahllisten-Datentyp auswählen, können Sie auch die Gruppe mit gültigen Werte für das Feld auswählen.</span><span class="sxs-lookup"><span data-stu-id="b002c-128">If you choose the picklist data type, you can also select the set of valid values for the field.</span></span>  
     3.   <span data-ttu-id="b002c-129">Geben Sie einen Namen, eine Beschriftung und einen Hilfetext für das Feld an.</span><span class="sxs-lookup"><span data-stu-id="b002c-129">Provide a name, label, and help text for the field.</span></span> <span data-ttu-id="b002c-130">Der Name entspricht dem physischen Feldnamen in der Datenbank, wohingegen die Beschriftung und der Hilfetext der Text sind, der zur Darstellung dieses Felds in der Benutzeroberfläche verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b002c-130">The name corresponds to the physical field name in the database, whereas the label and help text are the text used to represent this field in the user interface.</span></span>  
8.   <span data-ttu-id="b002c-131">Wenn dies das einzige Feld ist, das Sie für dieses Formular erstellen müssen, klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="b002c-131">If this is the only field that you need to create for this form, click **Save**.</span></span> <span data-ttu-id="b002c-132">Wenn Sie zusätzliche Felder erstellen müssen, klicken Sie auf **Speichern und neu**, und kehren Sie zu Schritt 7 zurück.</span><span class="sxs-lookup"><span data-stu-id="b002c-132">If you need to create additional fields, click **Save and new** and go back to step 7.</span></span> <span data-ttu-id="b002c-133">Beachten Sie, dass es aktuell eine Begrenzung von **20 benutzerdefinierten Feldern pro Tabelle** gibt.</span><span class="sxs-lookup"><span data-stu-id="b002c-133">Note that there is currently a limit of **20 custom fields per table**.</span></span>
9.   <span data-ttu-id="b002c-134">Wenn Sie das Dialogfeld **Neues Feld erstellen** verlassen, kehren Sie zum Dialogfeld **Felder einfügen** zurück.</span><span class="sxs-lookup"><span data-stu-id="b002c-134">Leaving the **Create new field** dialog box will return you to the **Insert fields** dialog box.</span></span> <span data-ttu-id="b002c-135">Alle benutzerdefinierten Felder, die gerade erst hinzugefügt wurden, werden automatisch in der Feldliste markiert, um in das Formular eingefügt zu werden.</span><span class="sxs-lookup"><span data-stu-id="b002c-135">Any custom fields that were just added will be automatically marked in the field list to be inserted into the form.</span></span>  
10.   <span data-ttu-id="b002c-136">Klicken Sie auf **Einfügen**, um die markierten Felder in den ausgewählten Bereich des Formulars einzufügen.</span><span class="sxs-lookup"><span data-stu-id="b002c-136">Click **Insert** to insert the marked fields into the selected region of the form.</span></span> 
11.   <span data-ttu-id="b002c-137">**Optional:** Aktivieren Sie den Modus **Verschieben** aus der Personalisierungssymbolleiste, um die neuen Felder an die gewünschte Position im ausgewählten Bereich zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="b002c-137">**Optional:** Enable **Move** mode from the personalization toolbar to move the new fields to their desired location in the selected region.</span></span> <span data-ttu-id="b002c-138">Weitere Informationen darüber, wie die verschiedenen Personalisierungsfunktionen verwendet werden, um ein Formular für Ihre persönliche Verwendung zu optimieren, finden Sie unter [Die Benutzeroberfläche personalisieren](personalize-user-experience.md).</span><span class="sxs-lookup"><span data-stu-id="b002c-138">See [Personalize the user experience](personalize-user-experience.md) for more information about how to use the various personalization capabilities to optimize a form for your personal usage.</span></span>  

## <a name="sharing-custom-fields-with-other-users"></a><span data-ttu-id="b002c-139">Benutzerdefinierte Felder für andere Benutzer freigeben</span><span class="sxs-lookup"><span data-stu-id="b002c-139">Sharing custom fields with other users</span></span>
<span data-ttu-id="b002c-140">Nachdem Sie ein benutzerdefiniertes Feld erstellt haben und es auf einem Formular verfügbar gemacht haben, möchten Sie vielleicht diese aktualisierte Seitenansicht bereitstellen, die das neue Feld für andere Benutzer im System enthält.</span><span class="sxs-lookup"><span data-stu-id="b002c-140">After you have created a custom field and exposed it on a form, you might want to provide this updated page view that includes the new field to other users in the system.</span></span> <span data-ttu-id="b002c-141">Dies kann auf zwei unterschiedliche Arten mithilfe der Personalisierungsfunktionen des Produkts ausgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="b002c-141">This can be accomplished in two different ways using the personalization capabilities of the product:</span></span>

-   <span data-ttu-id="b002c-142">Die empfohlene Vorgehensweise erfolgt über den Systemadministrator, der eine Personalisierung an alle Benutzer oder einer Teilmenge der Benutzer mithilfe von Push übertragen kann.</span><span class="sxs-lookup"><span data-stu-id="b002c-142">The recommended route is through the system administrator, who can push a personalization to all users or a subset of users.</span></span> <span data-ttu-id="b002c-143">Weitere Informationen finden Sie unter [Personalisieren der Benutzeroberfläche](personalize-user-experience.md).</span><span class="sxs-lookup"><span data-stu-id="b002c-143">See [Personalize the user experience](personalize-user-experience.md) for more details.</span></span> 

-   <span data-ttu-id="b002c-144">Alternativ können Sie Ihre Änderungen exportieren (genannt *Personalisierungen*), sie an einen oder mehrere Benutzer übermitteln und jeden dieser Benutzer dazu veranlassen, Ihre Änderungen zu importieren.</span><span class="sxs-lookup"><span data-stu-id="b002c-144">Alternatively, you can export your changes (called *personalizations*), send them to one or more users, and have each of those users import your changes.</span></span> <span data-ttu-id="b002c-145">Die Option **Verwalten** in der Personalisierungssymbolleiste ermöglich es Ihnen, Personalisierungen zu exportieren und importieren.</span><span class="sxs-lookup"><span data-stu-id="b002c-145">The **Manage** option on the personalization toolbar enables you to export and import personalizations.</span></span>

## <a name="managing-custom-fields"></a><span data-ttu-id="b002c-146">Benutzerdefinierte Felder verwalten</span><span class="sxs-lookup"><span data-stu-id="b002c-146">Managing custom fields</span></span>

<span data-ttu-id="b002c-147">Verwaltung aller benutzerdefinierten Felder im System kann über die Seite **Benutzerdefinierte Felder** im Systemverwaltungsmodul erfolgen.</span><span class="sxs-lookup"><span data-stu-id="b002c-147">Management of all the custom fields in the system can be accomplished through the **Custom fields** page in the System administration module.</span></span>  <span data-ttu-id="b002c-148">Diese Seite ermöglicht Benutzern den Zugriff auf viele Funktionen, einschließlich:</span><span class="sxs-lookup"><span data-stu-id="b002c-148">This page allows users access to many capabilities, including:</span></span> 
-   <span data-ttu-id="b002c-149">Anzeigen einer Liste aller benutzerdefinierten Felder im System.</span><span class="sxs-lookup"><span data-stu-id="b002c-149">Viewing a list of all custom fields in the system.</span></span>
-   <span data-ttu-id="b002c-150">Begrenzte Bearbeitung vorhandener benutzerdefinierter Felder.</span><span class="sxs-lookup"><span data-stu-id="b002c-150">Limited editing of existing custom fields.</span></span>
-   <span data-ttu-id="b002c-151">Löschen benutzerdefinierter Felder.</span><span class="sxs-lookup"><span data-stu-id="b002c-151">Deleting custom fields.</span></span>
-   <span data-ttu-id="b002c-152">Benutzerdefinierte Feldern in Datenentitäten verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="b002c-152">Exposing custom fields on data entities.</span></span>
-   <span data-ttu-id="b002c-153">Bereitstellen von Übersetzungen benutzerdefinierter Feldbeschriftungen und von Hilfetext.</span><span class="sxs-lookup"><span data-stu-id="b002c-153">Providing translations of custom field labels and help text.</span></span>

### <a name="viewing-all-custom-fields"></a><span data-ttu-id="b002c-154">Anzeigen aller benutzerdefinierten Felder</span><span class="sxs-lookup"><span data-stu-id="b002c-154">Viewing all custom fields</span></span>
<span data-ttu-id="b002c-155">Die Seite **Benutzerdefinierte Felder** bietet Sichtbarkeit für alle benutzerdefinierten Felder, die im System definiert wurden.</span><span class="sxs-lookup"><span data-stu-id="b002c-155">The **Custom fields** page provides visibility to all the custom fields that have been defined in the system.</span></span> <span data-ttu-id="b002c-156">Wählen Sie einfach die Tabelle aus, an der Sie interessiert sind, und die Seite wird aktualisiert, damit sie eine Liste der benutzerdefinierten Felder anzeigt, die dieser Tabelle zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="b002c-156">Simply select the table that you are interested in, and the page will update to show a list of the custom fields associated with that table.</span></span> <span data-ttu-id="b002c-157">Das Auswählen eines benutzerdefinierten Felds aus der Liste ermöglicht es Ihnen, alle Details über das Feld anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b002c-157">Choosing a custom field from the list will allow you to view all the details about the field.</span></span>

### <a name="editing-custom-fields"></a><span data-ttu-id="b002c-158">Benutzerdefinierter Felder bearbeiten</span><span class="sxs-lookup"><span data-stu-id="b002c-158">Editing custom fields</span></span>
<span data-ttu-id="b002c-159">Nachdem ein benutzerdefiniertes Feld erstellt wurde, können nur bestimmte Informationen über das benutzerdefinierte Feld auf der Seite **Benutzerdefinierte Felder** geändert werden.</span><span class="sxs-lookup"><span data-stu-id="b002c-159">After a custom field has been created, only certain pieces of information about the custom field can be modified on the **Custom fields** page.</span></span>   

<span data-ttu-id="b002c-160">Sie *können* diese Attribute ändern:</span><span class="sxs-lookup"><span data-stu-id="b002c-160">You *can* modify these attributes:</span></span> 
-   <span data-ttu-id="b002c-161">Beschriftung</span><span class="sxs-lookup"><span data-stu-id="b002c-161">Label</span></span> 
-   <span data-ttu-id="b002c-162">Hilfetext</span><span class="sxs-lookup"><span data-stu-id="b002c-162">Help text</span></span>
-   <span data-ttu-id="b002c-163">Länge, für Textfelder</span><span class="sxs-lookup"><span data-stu-id="b002c-163">Length, for Text fields</span></span>

<span data-ttu-id="b002c-164">Sie *können nicht* die folgenden Attribute ändern:</span><span class="sxs-lookup"><span data-stu-id="b002c-164">You *cannot* edit the following attributes:</span></span> 
-   <span data-ttu-id="b002c-165">Feldname</span><span class="sxs-lookup"><span data-stu-id="b002c-165">Field name</span></span>
-   <span data-ttu-id="b002c-166">Datentyp</span><span class="sxs-lookup"><span data-stu-id="b002c-166">Data type</span></span>

<span data-ttu-id="b002c-167">Darüber hinaus kann bei Auswahllistenfelder der Satz gültiger Werte für das benutzerdefinierte Feld neu angeordnet werden und neue Werte können hinzugefügt werden. Vorhandene Werte für das Auswahllistenfeld können jedoch nicht entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="b002c-167">Additionally, for picklist fields, the set of valid values for the custom field can be reordered, and new values can be added; however, existing values for the picklist field cannot be removed.</span></span> <span data-ttu-id="b002c-168">Denken Sie daran, auf **Änderungen anwenden** zu klicken, wenn Sie mit der Bearbeitung von Feldern für eine bestimmte Tabelle fertig sind, damit die Änderungen gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="b002c-168">Remember to click **Apply changes** when you are done editing fields for a particular table so the changes are saved.</span></span> 

### <a name="exposing-custom-fields-on-data-entities"></a><span data-ttu-id="b002c-169">Benutzerdefinierte Felder in Datenentitäten verfügbar machen</span><span class="sxs-lookup"><span data-stu-id="b002c-169">Exposing custom fields on data entities</span></span>
<span data-ttu-id="b002c-170">Gegebenenfalls ist es auch wichtig, zuzulassen, dass benutzerdefinierte Felder in Datenentitäten sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="b002c-170">It may also be important to allow custom fields to be visible on data entities.</span></span> <span data-ttu-id="b002c-171">Datenentitäten werden sowohl in der Funktion [In Office öffnen](../../dev-itpro/office-integration/office-integration.md) als auch bei Szenarien des Datenimports/-exports verwendet.</span><span class="sxs-lookup"><span data-stu-id="b002c-171">Data entities are utilized in the [Open in Office](../../dev-itpro/office-integration/office-integration.md) feature, as well as for data import/export scenarios.</span></span>  

<span data-ttu-id="b002c-172">Folgen Sie diesen Schritten, um ein benutzerdefiniertes Feld in einer Datenentität verfügbar zu machen:</span><span class="sxs-lookup"><span data-stu-id="b002c-172">Follow these steps to expose a custom field on a data entity:</span></span> 
1.   <span data-ttu-id="b002c-173">Wählen Sie das benutzerdefinierte Feld im Formular **Benutzerdefinierte Felder** aus.</span><span class="sxs-lookup"><span data-stu-id="b002c-173">Select the custom field on the **Custom fields** form.</span></span> 
2.   <span data-ttu-id="b002c-174">Erweitern Sie den Bereich **Entitäten**, um den Satz relevanter Entitäten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b002c-174">Expand the **Entities** section to view the set of relevant entities.</span></span>  
3.   <span data-ttu-id="b002c-175">Klicken Sie auf die Schaltfläche **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="b002c-175">Click the **Edit** button.</span></span>
4.   <span data-ttu-id="b002c-176">Ändern Sie das Feld **Aktiviert**, das für jede Entität ausgewählt werden muss, die dieses Feld verfügbar machen soll.</span><span class="sxs-lookup"><span data-stu-id="b002c-176">Modify the **Enabled** field to be selected for each entity that should expose this field.</span></span>  
5.   <span data-ttu-id="b002c-177">Klicken Sie auf **Änderungen anwenden**, um Ihre Auswahlen zu speichern</span><span class="sxs-lookup"><span data-stu-id="b002c-177">Click **Apply changes** to save your selections.</span></span>  

### <a name="allowing-custom-fields-to-be-displayed-in-other-languages"></a><span data-ttu-id="b002c-178">Die Anzeige von benutzerdefinierten Feldern in anderen Sprachen zulassen</span><span class="sxs-lookup"><span data-stu-id="b002c-178">Allowing custom fields to be displayed in other languages</span></span>
<span data-ttu-id="b002c-179">Da auf benutzerdefinierte Felder möglicherweise von Benutzern in einer Vielzahl von Sprachen zugegriffen werden muss, bietet die Seite **Benutzerdefinierte Felder** einen Mechanismus, der es ermöglicht, dass die Beschriftung und der Hilfetext eines benutzerdefinierten Felds in andere Sprachen übersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="b002c-179">Because custom fields may need to be accessed by users in a variety of languages, the **Custom fields** page provides a mechanism to allow the label and help text for a custom field to be translated into other languages.</span></span>  

<span data-ttu-id="b002c-180">In den folgenden Schritten wird der Prozess zum Übersetzen von benutzerdefinierten Felder in andere Sprachen beschrieben:</span><span class="sxs-lookup"><span data-stu-id="b002c-180">The following steps describe the process for translating custom fields in other languages:</span></span> 
1.   <span data-ttu-id="b002c-181">Wählen Sie das benutzerdefinierte Feld auf der Seite **Benutzerdefinierte Felder** aus.</span><span class="sxs-lookup"><span data-stu-id="b002c-181">Select the custom field on the **Custom fields** page.</span></span> 
2.   <span data-ttu-id="b002c-182">Aktivieren Sie die Schaltfläche **Übersetzungen** im Aktivitätsbereich.</span><span class="sxs-lookup"><span data-stu-id="b002c-182">Select the **Translations** button in the Action Pane.</span></span> <span data-ttu-id="b002c-183">Dadurch wird ein Dropdownmenü mit vorhandenen Übersetzungen für dieses Feld geöffnet.</span><span class="sxs-lookup"><span data-stu-id="b002c-183">This will open a drop-down menu with existing translations for this field.</span></span>
3.   <span data-ttu-id="b002c-184">Im Dropdownmenü **Sprache** wird die Gruppe von Sprachen angezeigt, für die bereits Übersetzungen bereitgestellt wurden.</span><span class="sxs-lookup"><span data-stu-id="b002c-184">The **Language** drop-down menu shows the set of languages for which translations have already been provided.</span></span> 
     1.   <span data-ttu-id="b002c-185">Wenn Sie eine vorhandene Übersetzung bearbeiten möchten, wählen Sie die gewünschte Sprache im Menü aus und ändern Sie die Werte für die Beschriftung und den Hilfetext.</span><span class="sxs-lookup"><span data-stu-id="b002c-185">If you want to edit an existing translation, select the desired language from the menu and modify the values for the label and help text.</span></span>  
     2.   <span data-ttu-id="b002c-186">Andernfalls klicken Sie auf die Schaltfläche **Sprache hinzufügen**, wählen Sie die gewünschte Sprache im Menü aus, und geben Sie dann übersetzte Werte für die Beschriftung und den Hilfetext an.</span><span class="sxs-lookup"><span data-stu-id="b002c-186">Otherwise, click the **Add language** button, select the desired language from the menu, and then provide translated values for the label and help text.</span></span>  
4.   <span data-ttu-id="b002c-187">Klicken Sie auf **OK**, wenn Sie fertig sind.</span><span class="sxs-lookup"><span data-stu-id="b002c-187">Click **OK** when you are finished.</span></span>  

### <a name="deleting-custom-fields"></a><span data-ttu-id="b002c-188">Benutzerdefinierte Felder löschen</span><span class="sxs-lookup"><span data-stu-id="b002c-188">Deleting custom fields</span></span>
<span data-ttu-id="b002c-189">In einigen seltenen Fällen entscheiden Sie sich möglicherweise, dass ein benutzerdefiniertes Feld nicht mehr erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="b002c-189">In some rare cases, you may decide that a custom field is no longer needed.</span></span> <span data-ttu-id="b002c-190">Wenn dies geschieht, kann ein Systemadministrator beschließen, das Feld aus der Seite **Benutzerdefinierte Felder** zu löschen.</span><span class="sxs-lookup"><span data-stu-id="b002c-190">When this occurs, a system administrator can choose to delete the field from the **Custom fields** page.</span></span> <span data-ttu-id="b002c-191">Stellen Sie dazu sicher, dass das korrekte Feld ausgewählt ist, klicken Sie auf **Löschen**, klicken Sie auf **Ja**, um den Löschvorgang zu bestätigen, und klicken Sie schließlich auf **Änderungen anwenden**.</span><span class="sxs-lookup"><span data-stu-id="b002c-191">To do this, ensure the correct field is selected, click **Delete**, click **Yes** to confirm the deletion, and finally click **Apply changes**.</span></span> 

> [!Note]
> <span data-ttu-id="b002c-192">Diese Aktivität kann nicht rückgängig gemacht werden und führt dazu, dass die Daten, die diesem Feld zugeordnet sind, dauerhaft aus der Datenbank gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="b002c-192">This action cannot be undone, and will result in the data associated with the field being permanently deleted from the database.</span></span> 

## <a name="appendix"></a><span data-ttu-id="b002c-193">Anhang</span><span class="sxs-lookup"><span data-stu-id="b002c-193">Appendix</span></span> 
### <a name="who-can-create-custom-fields"></a><span data-ttu-id="b002c-194">Wer kann benutzerdefinierte Felder erstellen?</span><span class="sxs-lookup"><span data-stu-id="b002c-194">Who can create custom fields?</span></span>
<span data-ttu-id="b002c-195">Als Schutzvorrichtung für das System, können standardmäßig nur Systemadministratoren benutzerdefinierte Felder erstellen.</span><span class="sxs-lookup"><span data-stu-id="b002c-195">As a safeguard to the system, only system administrators are able to create custom fields by default.</span></span> <span data-ttu-id="b002c-196">Allerdings kann denjenigen Powerusern, die die Organisation für notwendig erachtet, Rechte erteilt werden, um benutzerdefinierte Felder durch einen Systemadministrator zu erstellen, indem die Sicherheitsrolle **Laufzeitanpassungs-Poweruser** verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b002c-196">However, those power users whom the organization deems necessary can be given rights to create custom fields by a system administrator using the **Runtime customization power user** security role.</span></span> <span data-ttu-id="b002c-197">Benutzer ohne diese Sicherheitsrolle sind nicht in der Lage, benutzerdefinierte Felder zu erstellen, sie können jedoch trotzdem benutzerdefinierte Felder, die von anderen Benutzern im System hinzugefügt wurden, anzeigen und mit ihnen interagieren.</span><span class="sxs-lookup"><span data-stu-id="b002c-197">Users without this security role will not be able to create custom fields, but will still be able to see and interact with custom fields added by other users in the system.</span></span>    

### <a name="what-tables-support-custom-fields"></a><span data-ttu-id="b002c-198">Welche Tabellen unterstützen benutzerdefinierte Felder?</span><span class="sxs-lookup"><span data-stu-id="b002c-198">What tables support custom fields?</span></span>
<span data-ttu-id="b002c-199">Aus Gründen der Leistung und technischen Gründen ist es nur bei Tabellen, die die folgenden Bedingungen erfüllen, aktuell zulässig, benutzerdefinierte Felder hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="b002c-199">For performance and technical reasons, only tables that meet the following conditions currently allow custom fields to be added.</span></span>

- <span data-ttu-id="b002c-200">Die Tabelle muss als eine dieser Gruppen markiert sein:</span><span class="sxs-lookup"><span data-stu-id="b002c-200">The table must be tagged as one of these groups:</span></span> 
     -   <span data-ttu-id="b002c-201">Gruppieren</span><span class="sxs-lookup"><span data-stu-id="b002c-201">Group</span></span>
     -   <span data-ttu-id="b002c-202">WorksheetHeader</span><span class="sxs-lookup"><span data-stu-id="b002c-202">WorksheetHeader</span></span>
     -   <span data-ttu-id="b002c-203">Haupttabelle</span><span class="sxs-lookup"><span data-stu-id="b002c-203">Main</span></span>
     -   <span data-ttu-id="b002c-204">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="b002c-204">Miscellaneous</span></span>
     -   <span data-ttu-id="b002c-205">Parameter</span><span class="sxs-lookup"><span data-stu-id="b002c-205">Parameter</span></span>
     -   <span data-ttu-id="b002c-206">Referenz</span><span class="sxs-lookup"><span data-stu-id="b002c-206">Reference</span></span>
     -   <span data-ttu-id="b002c-207">TransactionHeader</span><span class="sxs-lookup"><span data-stu-id="b002c-207">TransactionHeader</span></span>
- <span data-ttu-id="b002c-208">Die Tabelle kann keine andere Tabelle erweitern.</span><span class="sxs-lookup"><span data-stu-id="b002c-208">The table cannot not extend another table.</span></span>
- <span data-ttu-id="b002c-209">Die Tabelle kann nicht als Systemtabelle markiert werden.</span><span class="sxs-lookup"><span data-stu-id="b002c-209">The table cannot be marked as a system table.</span></span>
- <span data-ttu-id="b002c-210">Die Tabelle kann keine temporäre Tabelle sein.</span><span class="sxs-lookup"><span data-stu-id="b002c-210">The table cannot be a temporary table.</span></span>
