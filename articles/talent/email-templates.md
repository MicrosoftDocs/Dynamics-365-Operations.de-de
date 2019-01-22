---
title: E-Mail-Vorlagen
description: "Dieses Thema enthält Informationen zu den E-Mail-Vorlagen, die Sie in Microsoft Dynamics 365 for Talent - Attract erstellen und verwenden können."
author: josaw
manager: AnnBe
ms.date: 10/19/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.translationtype: HT
ms.sourcegitcommit: 8166047a768c47219855c55a1008f3dd24cd5344
ms.openlocfilehash: e02912ad242186fe3e2dd8d7a4cc7312aec6015e
ms.contentlocale: de-de
ms.lasthandoff: 01/04/2019

---

# <a name="email-templates"></a><span data-ttu-id="95ac2-103">E-Mail-Vorlagen</span><span class="sxs-lookup"><span data-stu-id="95ac2-103">Email templates</span></span>
[!include[banner](../includes/banner.md)]

<span data-ttu-id="95ac2-104">Mithilfe der Email-Vorlagen-Bibliothek können Administratoren ein einheitliches Design und Branding für alle E-Mails erstellen, die von Microsoft Dynamics 365 for Talent: attract gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="95ac2-104">By using the email template library, admins can create a uniform theme and branding for all emails that are sent through Microsoft Dynamics 365 for Talent: Attract.</span></span> <span data-ttu-id="95ac2-105">Administratoren können auch eine Sammlung von E-Mail-Inhaltsvorlagen zusammenstellen, die von anderen E-Mail-Nutzern verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="95ac2-105">Admins can also curate a collection of email content templates that other users can consume.</span></span> <span data-ttu-id="95ac2-106">Das Einstellungsteam kann diese Vorlagen in ihrem Workflow verwenden, um E-Mail-Nachrichten effizienter zu senden.</span><span class="sxs-lookup"><span data-stu-id="95ac2-106">The hiring team can use these templates in their workflow to send emails more efficiently.</span></span> <span data-ttu-id="95ac2-107">Einige E-Mails werden in Attract so konfiguriert, dass sie automatisch gesendet werden, und der Administrator kann die Email-Vorlagen-Bibliothek verwenden, um den Inhalt für die E-Mails anzupassen.</span><span class="sxs-lookup"><span data-stu-id="95ac2-107">Some emails in Attract are configured to be sent automatically, and the admin can use the email template library to customize the content for those emails.</span></span>

> [!NOTE]
> <span data-ttu-id="95ac2-108">Um E-Mail-Vorlagen zu verwenden, muss die Organisation das Verständliche Einstellungsadd-on haben.</span><span class="sxs-lookup"><span data-stu-id="95ac2-108">To use Email templates, your organization must have the Comprehensive Hiring add-on.</span></span>

## <a name="global-template-configurations"></a><span data-ttu-id="95ac2-109">Globale Konfigurationsvorlagen</span><span class="sxs-lookup"><span data-stu-id="95ac2-109">Global template configurations</span></span>

<span data-ttu-id="95ac2-110">Um ein konsistentes Branding für die gesamte E-Mail-Kommunikation zu erstellen, muss der Administrator erst die globalen Kopf- und Fußzeilen für alle E-Mail-Vorlagen festlegen.</span><span class="sxs-lookup"><span data-stu-id="95ac2-110">To create consistent branding for all email communications, the admin must first set the global header and footer for all email templates.</span></span> <span data-ttu-id="95ac2-111">Im Administratorcenter kann der Administrator auf der Registerkarte **Email-Vorlagen-Einstellungen** im Abschnitt **Kopfzeile** ein Bild hochladen, das bei allen E-Mails als Kopfzeile oder Banner verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="95ac2-111">In the Admin center, on the **Email template settings** tab, in the **Header** section, the admin can upload an image to use as the header or banner for all emails.</span></span> <span data-ttu-id="95ac2-112">Das Bild kann ein Firmenlogo, ein Briefkopf oder jedes andere Repräsentativbild sein.</span><span class="sxs-lookup"><span data-stu-id="95ac2-112">The image might be a company logo, a letterhead, or any other representative image.</span></span> <span data-ttu-id="95ac2-113">Es wird empfohlen, dass die Breite zwischen 25 und 800 Pixel beträgt und die Höhe Pixel zwischen 25 und 150 Pixel, da diese Abmessungen für die meisten E-Mail-Clients wie Microsoft Outlook optimal sind.</span><span class="sxs-lookup"><span data-stu-id="95ac2-113">We recommend that the width be between 25 and 800 pixels, and that the height be between 25 and 150 pixels, because these dimensions are optimal for most email clients, such as Microsoft Outlook.</span></span> <span data-ttu-id="95ac2-114">Das Bild muss eine JPEG-, JPG-, PNG- oder SVG-Datei sein, und die Dateigröße muss kleiner als 1 Megabyte (MB) sein.</span><span class="sxs-lookup"><span data-stu-id="95ac2-114">The image must be a JPEG, JPG, PNG, or SVG file, and the file size must be less than 1 megabyte (MB).</span></span> <span data-ttu-id="95ac2-115">Nachdem ein Bild hochgeladen wurde, wird eine Vorschau der Kopfzeile generiert und angezeigt.</span><span class="sxs-lookup"><span data-stu-id="95ac2-115">After an image is uploaded, a preview of the header is generated and shown.</span></span> <span data-ttu-id="95ac2-116">Wenn das Kopfzeilenbild entfernt oder ersetzt werden muss, kann der Administrator die Option **Entfernen** über der Vorschau verwenden.</span><span class="sxs-lookup"><span data-stu-id="95ac2-116">If the header image must be removed or replaced, the admin can use the **Remove** option above the preview.</span></span>

<span data-ttu-id="95ac2-117">Im Abschnitt **Fußzeile** kann der Administrator Links zur Kommunikations-Datenschutzrichtlinie den Bedingungen des Unternehmens bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="95ac2-117">In the **Footer** section, the admin can provide links to the company's privacy policy for communications, and to the terms and conditions.</span></span> <span data-ttu-id="95ac2-118">Diese Links werden in eine Fußzeile integriert, die automatisch generiert wird.</span><span class="sxs-lookup"><span data-stu-id="95ac2-118">These links are incorporated into a footer that is automatically generated.</span></span> <span data-ttu-id="95ac2-119">Eine Vorschau der Fußzeile wird dann angezeigt.</span><span class="sxs-lookup"><span data-stu-id="95ac2-119">A preview of this footer is then shown.</span></span>

<span data-ttu-id="95ac2-120">Vergewissern Sie sich, dass Sie die Änderungen speichern, bevor Sie das Administratorcenter schließen.</span><span class="sxs-lookup"><span data-stu-id="95ac2-120">Be sure to save your changes before you close the Admin center.</span></span>

> [!NOTE] 
> <span data-ttu-id="95ac2-121">Die Kopf- und Fußzeilen sind globale Einstellungen für alle E-Mails.</span><span class="sxs-lookup"><span data-stu-id="95ac2-121">The header and footer are global settings for all emails.</span></span> <span data-ttu-id="95ac2-122">Daher werden sie in allen E-Mails angezeigt, die von über Attract gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="95ac2-122">Therefore, they will appear in all emails that are sent through Attract.</span></span> <span data-ttu-id="95ac2-123">Wenn die Einstellungen nicht konfiguriert werden, werden die Kopf- und Fußzeilen aus allen E-Mails weggelassen.</span><span class="sxs-lookup"><span data-stu-id="95ac2-123">If the settings aren't configured, the header and footer will be left out of all emails.</span></span>

## <a name="email-template-library"></a><span data-ttu-id="95ac2-124">E-Mail-Vorlagenbibliothek</span><span class="sxs-lookup"><span data-stu-id="95ac2-124">Email template library</span></span> 

<span data-ttu-id="95ac2-125">Nachdem die globalen Vorlagenkonfigurationen eingerichtet sind, kann der Administrator damit beginnen, Vorlagen für alle E-Mails zu erstellen und zusammenzustellen, die über Attract gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="95ac2-125">After the global template configurations are set up, the admin can start to create and curate templates for all emails that are sent from Attract.</span></span> <span data-ttu-id="95ac2-126">Die Email-Vorlagenbibliothek ist nur für Administratoren verfügbar.</span><span class="sxs-lookup"><span data-stu-id="95ac2-126">The email template library is available only to admins.</span></span> <span data-ttu-id="95ac2-127">Um die Bibliothek zu öffnen, wählen Sie im Hauptnavigationsmenü die Registerkarte **E-Mail-Vorlagen** aus. Die Bibliothek wird nach den unterschiedlichen Aktivitäten in Attract kategorisiert, für die E-Mails gesendet werden müssen, z. B. "Planung", "Bewertung" und "Joberstellung".</span><span class="sxs-lookup"><span data-stu-id="95ac2-127">To open the library, on the main navigation menu, select the **Email templates** tab. The library is categorized by the various activities in Attract that emails must be sent for, such as scheduling, assessment, and job creation.</span></span> <span data-ttu-id="95ac2-128">Der Administrator kann eine beliebige Kategorie auswählen, um alle E-Mail-Typen anzuzeigen, die der Aktivität zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="95ac2-128">The admin can select any category to view all the email types that are associated with the activity.</span></span> <span data-ttu-id="95ac2-129">Wählen Sie beispielsweise **Planung** aus, um die verschiedenen E-Mail-Typen anzuzeigen, die während des Planungsprozesses gesendet werden, und alle Vorlagen, die für jeden E-Mail-Typ verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="95ac2-129">For example, select **Scheduling** to view the various types of email that are sent during the scheduling process and all the templates that are available for each type of email.</span></span> <span data-ttu-id="95ac2-130">Jeder Unterabschnitt in einer Kategorie stellt einen E-Mail-Typ dar.</span><span class="sxs-lookup"><span data-stu-id="95ac2-130">Each subsection in a category represents a type of email.</span></span>

<span data-ttu-id="95ac2-131">Eine E-Mail-Typen können mehrere Empfänger haben.</span><span class="sxs-lookup"><span data-stu-id="95ac2-131">Some types of email can have more than one recipient.</span></span> <span data-ttu-id="95ac2-132">In der Kategorie **Planung** beispielsweise, werden die E-Mails, die gesendet werden, wenn die Gesprächsplanzusammenfassung benötigt wird, an Kandidaten und Gesprächsleiter gesendet.</span><span class="sxs-lookup"><span data-stu-id="95ac2-132">For example, in the **Scheduling** category, the emails that are sent when the interview schedule summary is needed, are sent to both candidates and interviewers.</span></span> <span data-ttu-id="95ac2-133">Jeder Abschnitt enthält zwei Hauptspalten: **Vorlagentitel** und **Empfänger**.</span><span class="sxs-lookup"><span data-stu-id="95ac2-133">Each section has two main columns: **Template Title** and **Recipient**.</span></span> <span data-ttu-id="95ac2-134">Jede Zeile in einem Abschnitt enthält eine einzelne Vorlage für einen E-Mail-Typ.</span><span class="sxs-lookup"><span data-stu-id="95ac2-134">Each row in a section represents a single template for a type of email.</span></span> <span data-ttu-id="95ac2-135">Zuerst wird ein Schlosssymbol in der Zeile für jede Vorlage angezeigt.</span><span class="sxs-lookup"><span data-stu-id="95ac2-135">At first, a lock symbol will appear in the row for every template.</span></span> <span data-ttu-id="95ac2-136">Dieses Symbol gibt an, dass die Vorlage die Standardvorlage ist, der von Attract bereitgestellt wird, und dass sie nicht gelöscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="95ac2-136">This symbol indicates that the template is the standard template that is provided with Attract, and that it can't be deleted.</span></span> <span data-ttu-id="95ac2-137">Für jede Vorlage kann der Administrator die Ellipsenschaltfläche (**…**) verwenden, um die Vorlage zu duplizieren, als eine Standardvorlage festzulegen oder sie zu löschen.</span><span class="sxs-lookup"><span data-stu-id="95ac2-137">For any template, the admin can use the ellipsis button (**...**) to duplicate the template, set it as a default template, or delete it.</span></span> <span data-ttu-id="95ac2-138">Wenn eine Vorlage als Standardvorlage festgelegt wird, kann eine der beiden Verhaltensweisen auftreten.</span><span class="sxs-lookup"><span data-stu-id="95ac2-138">When a template is set as a default template, one of two behaviors can occur.</span></span> <span data-ttu-id="95ac2-139">Das Verhalten wird durch die Kennkarte(n) angegeben, die in der Zeile für die Vorlage angezeigt werden:</span><span class="sxs-lookup"><span data-stu-id="95ac2-139">The behavior is indicated by the badge or badges that appear in the row for the template:</span></span>

- <span data-ttu-id="95ac2-140">**Standard** – Diese Kennkarte gibt an, dass die Vorlage die Standardvorlage für E-Mails ist, die gesendet werden, und dass Informationen eingegeben werden, wenn ein Benutzer E-Mails dieses bestimmten Typs sendet.</span><span class="sxs-lookup"><span data-stu-id="95ac2-140">**Default** – This badge indicates that the template is the default template for email that is sent, and that information will be entered in it when a user sends email of that specific type.</span></span>
- <span data-ttu-id="95ac2-141">**Standard** + **Automatisch übermittelt** – Diese Kennkartenkombination on weist darauf hin, dass die Vorlage die aktive Vorlage für vom System erstellte E-Mails ist, die automatisch gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="95ac2-141">**Default** + **Autosent** – This combination of badges indicates that the template is the active template for system-generated emails that are sent automatically.</span></span>

<span data-ttu-id="95ac2-142">Um eine Vorlage zu bearbeiten, wählen Sie die Zeilen aus und nehmen Änderungen an der Vorlage vor.</span><span class="sxs-lookup"><span data-stu-id="95ac2-142">To edit a template, select the row, and make changes to the template.</span></span>

> [!NOTE]
> <span data-ttu-id="95ac2-143">Jeder Empfänger eines bestimmten E-Mail-Typs hat eine Standardvorlage.</span><span class="sxs-lookup"><span data-stu-id="95ac2-143">Each recipient of a specific type of email has a default template.</span></span> <span data-ttu-id="95ac2-144">Alle Standardvorlage von Attract werden als Standardvorlagen festgelegt, bis der Administrator eine neue Vorlage für einen bestimmten E-Mail-Typ erstellt und als Standardvorlage festlegt.</span><span class="sxs-lookup"><span data-stu-id="95ac2-144">All the standard Attract templates are set as default templates until the admin creates a new template for a specific type of email and sets it as the default template.</span></span>

## <a name="create-a-template"></a><span data-ttu-id="95ac2-145">Eine Vorlage erstellen</span><span class="sxs-lookup"><span data-stu-id="95ac2-145">Create a template</span></span>

<span data-ttu-id="95ac2-146">Um eine Vorlage zu erstellen, wählen Sie in der oberen rechten Ecke der Email-Vorlagenbibliothek **+ Neue Vorlage** aus.</span><span class="sxs-lookup"><span data-stu-id="95ac2-146">To create a template, in the upper-right corner of the email template library, select **+ New template**.</span></span> <span data-ttu-id="95ac2-147">Um den E-Mail-Typ auszuwählen, für die Sie die Vorlage erstellen, wählen Sie den Empfänger, den Prozess und das Ereignis aus, für das die E-Mail gesendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="95ac2-147">To select the type of email that you're creating the template for, select the recipient, the process, and the event that email must be sent for.</span></span> <span data-ttu-id="95ac2-148">Wählen Sie dann **Erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="95ac2-148">Then select **Create**.</span></span>

<span data-ttu-id="95ac2-149">Die Vorlage wird in der Bearbeitungsansicht geöffnet, und Sie können die Vorlage benennen.</span><span class="sxs-lookup"><span data-stu-id="95ac2-149">The template is opened in editing view, and you can name the template.</span></span> <span data-ttu-id="95ac2-150">Soll die Vorlage beispielsweise an Kandidaten für eine US-Universität gesendet werden, aber der Inhalt ist in Französisch, geben Sie möglicherweise den Titel **Universität\_USA\_Francais** ein.</span><span class="sxs-lookup"><span data-stu-id="95ac2-150">For example, if the template is intended for candidates from a US university, but the content is written in French, you might enter **University\_US\_Francais** as the title.</span></span> <span data-ttu-id="95ac2-151">Der Titel, die Betreffzeile und der Textinhalt für jede Vorlage können Sprachen neben Englisch unterstützen.</span><span class="sxs-lookup"><span data-stu-id="95ac2-151">The title, subject line, and body content for any template can support languages besides English.</span></span>

<span data-ttu-id="95ac2-152">Das Feld **Für** für eine Vorlage kann nicht geändert werden, da Sie den Empfänger bereits ausgewählt haben, als Sie die Vorlage zuerst erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="95ac2-152">The **To** field for a template can't be edited, because you already selected the recipient when you first created the template.</span></span>

<span data-ttu-id="95ac2-153">Sie können Personen wie **Personalbeschaffungsmitarbeiter** oder **Zukünftiger Vorgesetzter** in der Kopiezeile (Cc) hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="95ac2-153">You can add personas such as **Recruiter** or **Hiring Manager** to the carbon copy (Cc) line.</span></span> <span data-ttu-id="95ac2-154">Wird die E-Mail gesendet wird, werden diese Rollen automatisch durch die entsprechenden Benutzer ersetzt, basierend auf dem Kontext der Stelle.</span><span class="sxs-lookup"><span data-stu-id="95ac2-154">When the email is sent, these roles are automatically replaced with the appropriate users, based on the context of the job.</span></span>

<span data-ttu-id="95ac2-155">Die Betreffzeile der der Textinhalt unterstützen Platzhalter.</span><span class="sxs-lookup"><span data-stu-id="95ac2-155">The subject line and body content support placeholders.</span></span> <span data-ttu-id="95ac2-156">Sie können Platzhalter einfügen, indem Sie **\#** eingeben und anschließend den entsprechenden Platzhalter in der Dropdownliste für automatische Vervollständigung auswählen.</span><span class="sxs-lookup"><span data-stu-id="95ac2-156">You can insert placeholders by typing **\#** and then selecting the appropriate placeholder in the autocomplete drop-down list.</span></span> <span data-ttu-id="95ac2-157">Die Liste der verfügbaren Platzhalter wird rechts neben der Seite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="95ac2-157">The list of available placeholders appears on the right side of the page.</span></span> <span data-ttu-id="95ac2-158">Wird die E-Mail gesendet, werden die Platzhalter automatisch ersetzt, basierend auf dem Kontext der Stelle und der Empfänger.</span><span class="sxs-lookup"><span data-stu-id="95ac2-158">When the email is sent, the placeholders are automatically replaced, based on the context of the job and the recipient.</span></span> <span data-ttu-id="95ac2-159">Zum Beispiel beinhaltet eine Vorlage für eine E-Mail, die an Kandidaten gesendet wird, den Platzhalter \#{Kandidat\_Name}.</span><span class="sxs-lookup"><span data-stu-id="95ac2-159">For example, a template for an email that is sent to candidates contains the placeholder \#{Candidate\_Name}.</span></span> <span data-ttu-id="95ac2-160">Wird die E-Mail einem Kandidaten gesendet wird, der Cameron heißt, wird dieser Platzhalter durch den Namen von Cameron ersetzt.</span><span class="sxs-lookup"><span data-stu-id="95ac2-160">When the email is sent to a candidate who is named Cameron, that placeholder will be replaced with Cameron's name.</span></span>

<span data-ttu-id="95ac2-161">Der Editor für Textinhalts ist ein Rich-Text-Editor, mit dem Sie Stil und Format des Text festlegen können.</span><span class="sxs-lookup"><span data-stu-id="95ac2-161">The body content editor is a rich text editor that lets you style and format text.</span></span> <span data-ttu-id="95ac2-162">Sie können auch Links und Anker einfügen.</span><span class="sxs-lookup"><span data-stu-id="95ac2-162">It also lets you insert hyperlinks and anchors.</span></span>

<span data-ttu-id="95ac2-163">Nachdem eine Vorlage für einen bestimmten E-Mail-Typ erstellt wurde, wählen Sie in der Zeile für die Vorlage die Ellipsenschaltfläche (**…**) aus, und legen sie als Standardvorlage fest.</span><span class="sxs-lookup"><span data-stu-id="95ac2-163">After a template is created for a specific type of email, select the ellipsis button (**...**) in the row for the template, and set it as the default template.</span></span>

## <a name="consume-templates"></a><span data-ttu-id="95ac2-164">Vorlagen nutzen</span><span class="sxs-lookup"><span data-stu-id="95ac2-164">Consume templates</span></span>

<span data-ttu-id="95ac2-165">Wenn das Einstellungsteam eine E-Mail sendet, kann es die vom Administrator erstellten Vorlagen nutzen.</span><span class="sxs-lookup"><span data-stu-id="95ac2-165">When the hiring team sends an email, it can use the templates that the admin created.</span></span> <span data-ttu-id="95ac2-166">Wenn mehrere Vorlagen für die E-Mail erstellt wurden, die ein Benutzer sendet, wird eine Dropdownliste im E-Mail-Anordnungsworkflow angezeigt.</span><span class="sxs-lookup"><span data-stu-id="95ac2-166">If multiple templates have been created for the email that a user is sending, a drop-down list appears in the email composition workflow.</span></span> <span data-ttu-id="95ac2-167">Die Standardvorlage wird automatisch eingegeben, aber der Benutzer kann eine andere Vorlage auswählen.</span><span class="sxs-lookup"><span data-stu-id="95ac2-167">The default template is entered automatically, but the user can select a different template.</span></span>

> [!NOTE] 
> <span data-ttu-id="95ac2-168">Für E-Mails, die automatisch gesendet werden, können mehrerer Vorlagen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="95ac2-168">For emails that are sent automatically, multiple templates can be created.</span></span> <span data-ttu-id="95ac2-169">Allerdings kann nur einer Vorlage als die aktive Vorlage festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="95ac2-169">However, only one template can be set as the active template.</span></span> <span data-ttu-id="95ac2-170">Da dieser Prozess durch Ereignisse ausgelöst wird, kann nur der Administrator festlegen, welche Vorlage anhand der Kombination der Kennkarten **Standard** und **Automatisch übermittelt** in der Vorlagenbibliothek verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="95ac2-170">Because this process is triggered by events, only the admin can determine which template should be used, based on the combination **Default** and **Autosent** badges in the template library.</span></span>
