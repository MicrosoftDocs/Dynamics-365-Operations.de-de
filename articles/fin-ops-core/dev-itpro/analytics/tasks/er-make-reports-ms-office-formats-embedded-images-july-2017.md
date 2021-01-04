---
title: Konfigurationen zum Generieren von Berichten im Office-Format entwerfen, die eingebettete Bilder haben
description: Die Schritte in diesem Thema enthalten Informationen darüber, wie die Konfigurationen zur elektronischen Berichterstattung (EB) entworfen werden, die elektronische Dokumente in Microsoft Office-Formaten (Excel und Word) generieren, die eingebettete Bilder enthalten.
author: NickSelin
manager: AnnBe
ms.date: 01/23/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0145565ba060308162620f29a42499b0bffe6496
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684401"
---
# <a name="design-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="2c390-103">Konfigurationen zum Generieren von Berichten im Office-Format entwerfen, die eingebettete Bilder haben</span><span class="sxs-lookup"><span data-stu-id="2c390-103">Design configurations to generate reports in Office format that have embedded images</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2c390-104">Um dies Schritte in dieser Prozedur auszuführen, müssen Sie zuerst die Prozedur „ER – Konfigurationsanbieter erstellen und als aktiv markieren“ abschließen.</span><span class="sxs-lookup"><span data-stu-id="2c390-104">To complete the steps in this procedure, first complete the procedure, "ER Create a configuration provider and mark it as active."</span></span> <span data-ttu-id="2c390-105">Mit dieser Prozedur wird erklärt, wie die Konfigurationen zur elektronischen Berichterstellung (EB) entworfen werden, um ein Microsoft Excel- oder Word-Dokument zu generieren, das eingebettete Bilder enthält.</span><span class="sxs-lookup"><span data-stu-id="2c390-105">This procedure explains how to design Electronic reporting (ER) configurations to generate a Microsoft Excel or Word document that contains embedded images.</span></span> <span data-ttu-id="2c390-106">In dieser Prozedur erstellen Sie die erforderlichen EB-Konfigurationen für das Beispielunternehmen Litware, Inc.. Diese Schritte können mithilfe des USMF-Datasets abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="2c390-106">In this procedure, you will create the required ER configurations for the sample company, Litware, Inc. These steps can be completed using the USMF dataset.</span></span> <span data-ttu-id="2c390-107">Diese Prozedur ist für Benutzer bestimmt, die die Rolle des Systemadministrators oder des elektronischen Berichtsentwicklers haben, die ihnen zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="2c390-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="2c390-108">Bevor Sie beginnen, laden Sie die im Hilfethema aufgeführten Dateien herunter und speichern Sie sie, [Betten Sie Bilder und Formen in Dokumente ein, die Sie mit ER](../electronic-reporting-embed-images-shapes.md) erzeugen.</span><span class="sxs-lookup"><span data-stu-id="2c390-108">Before you begin, download and save the files listed in the Help topic, [Embed images and shapes in documents that you generate by using ER](../electronic-reporting-embed-images-shapes.md).</span></span> <span data-ttu-id="2c390-109">Die Dateien sind: Modell für Schecks.xml, Druckformat für Schecks.xml, Unternehmenslogo.png, Signaturbild.png, Signaturbild 2.png und Scheckvorlage Word.docx.</span><span class="sxs-lookup"><span data-stu-id="2c390-109">The files are: Model for cheques.xml, Cheques printing format.xml, Company logo.png, Signature image.png, Signature image 2.png, and Cheque template Word.docx.</span></span>

## <a name="verify-prerequisites"></a><span data-ttu-id="2c390-110">Überprüfung der erforderlichen Software</span><span class="sxs-lookup"><span data-stu-id="2c390-110">Verify prerequisites</span></span>  
 1. <span data-ttu-id="2c390-111">Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.</span><span class="sxs-lookup"><span data-stu-id="2c390-111">Go to Organization administration > Workspaces > Electronic reporting.</span></span>  
 2. <span data-ttu-id="2c390-112">Überprüfen Sie, dass der Konfigurationsanbieter für Beispielunternehmen „Litware, Inc.” verfügbar und als aktiv markiert ist.</span><span class="sxs-lookup"><span data-stu-id="2c390-112">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="2c390-113">Wenn Sie diesen Konfigurationsanbieter nicht sehen, müssen Sie zuerst die Schritte in der Prozedur „Konfigurationsanbieter erstellen und als aktiv markieren“ abschließen.</span><span class="sxs-lookup"><span data-stu-id="2c390-113">If you don't see this configuration provider, complete the steps in the procedure, "Create a configuration provider and mark it as active."</span></span>   
 3. <span data-ttu-id="2c390-114">Klicken Sie auf "Berichterstellungskonfigurationen".</span><span class="sxs-lookup"><span data-stu-id="2c390-114">Click Reporting configurations.</span></span>  
 
## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="2c390-115">Neue ER-Modellkonfiguration hinzufügen</span><span class="sxs-lookup"><span data-stu-id="2c390-115">Add a new ER model configuration</span></span>  
 1. <span data-ttu-id="2c390-116">Anstatt ein neues Modell zu erstellen, können Sie die EB-Modellkonfigurationsdatei laden (Modelle für Schecks.xml), die Sie vorher gespeichert hatten.</span><span class="sxs-lookup"><span data-stu-id="2c390-116">Instead of creating a new model, you can load the ER model configuration file (Model for cheques.xml) that you saved earlier.</span></span> <span data-ttu-id="2c390-117">Diese Datei enthält das Beispieldatenmodell für Zahlungsschecks und die Zuordnung des Datenmodells zu den Datenkomponenten der Dynamics 365 for Operations-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="2c390-117">This file contains the sample data model for payment cheques and the mapping of the data model to the data components of the Dynamics 365 for Operations application.</span></span>   
 2. <span data-ttu-id="2c390-118">Klicken Sie im Versionen-Inforegister auf „Austauschen”.</span><span class="sxs-lookup"><span data-stu-id="2c390-118">On the Versions FastTab, click Exchange.</span></span>   
 3. <span data-ttu-id="2c390-119">Klicken Sie auf „Aus XML-Datei laden”.</span><span class="sxs-lookup"><span data-stu-id="2c390-119">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="2c390-120">Klicken Sie auf „Durchsuchen”, und wählen Sie dann „Modell” für „Schecks.xml” aus.</span><span class="sxs-lookup"><span data-stu-id="2c390-120">Click Browse, and then select Model for cheques.xml.</span></span>   
 5. <span data-ttu-id="2c390-121">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="2c390-121">Click OK.</span></span>  
 6. <span data-ttu-id="2c390-122">Das geladene Modell wird als Datenquelle von Informationen verwendet, um Dokumente zu generieren, die Bilder in Excel und in Word enthalten.</span><span class="sxs-lookup"><span data-stu-id="2c390-122">The loaded model will be used as a data source of information to generate documents that contain images in Excel and Word.</span></span>  

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="2c390-123">Neues ER-Modellformat hinzufügen</span><span class="sxs-lookup"><span data-stu-id="2c390-123">Add a new ER format configuration</span></span>  
 1. <span data-ttu-id="2c390-124">Anstatt ein neues Format zu erstellen, können Sie die EB-Formatkonfigurationsdatei laden (Scheckdruckformat.xml), die Sie vorher gespeichert hatten.</span><span class="sxs-lookup"><span data-stu-id="2c390-124">Instead of creating a new format, you can load the ER format configuration file (Cheques printing format.xml) that you saved earlier.</span></span> <span data-ttu-id="2c390-125">Diese Datei enthält das Beispiellayout des Formats, um Schecks mithilfe des vorgedruckten Formulars zu drucken und der Zuordnung dieses Formats zum Datenmodell „Modell für Schecks“.</span><span class="sxs-lookup"><span data-stu-id="2c390-125">This file contains the sample layout of the format to print cheques using the pre-printed form and the mapping of this format to the 'Model for cheques' data model.</span></span>   
 2. <span data-ttu-id="2c390-126">Klicken Sie auf „Austauschen”.</span><span class="sxs-lookup"><span data-stu-id="2c390-126">Click Exchange.</span></span>  
 3. <span data-ttu-id="2c390-127">Klicken Sie auf „Aus XML-Datei laden”.</span><span class="sxs-lookup"><span data-stu-id="2c390-127">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="2c390-128">Klicken Sie auf „Durchsuchen”, und wählen Sie die Datei „Scheckdruckformat.xml” aus.</span><span class="sxs-lookup"><span data-stu-id="2c390-128">Click Browse and select the Cheques printing format.xml file.</span></span>   
 5. <span data-ttu-id="2c390-129">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="2c390-129">Click OK.</span></span>  
 6. <span data-ttu-id="2c390-130">Wählen Sie in der Struktur erweitern 'Modell für Cheques.</span><span class="sxs-lookup"><span data-stu-id="2c390-130">In the tree, expand 'Model for cheques'.</span></span>  
 7. <span data-ttu-id="2c390-131">Wählen Sie in der Strukturdarstellung "Modell für Cheques\Cheques-Druckformat.</span><span class="sxs-lookup"><span data-stu-id="2c390-131">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>  
 8. <span data-ttu-id="2c390-132">Das geladene Format wird verwendet, um Dokumente zu generieren, die Bilder in Excel und in Word enthalten.</span><span class="sxs-lookup"><span data-stu-id="2c390-132">The loaded format will be used to generate documents that contain images in Excel and Word.</span></span>   

## <a name="configure-er-user-parameters"></a><span data-ttu-id="2c390-133">Benutzerparameter der elektronischen Berichterstellung konfigurieren</span><span class="sxs-lookup"><span data-stu-id="2c390-133">Configure ER user parameters</span></span>  
 1. <span data-ttu-id="2c390-134">Klicken Sie im Aktivitätsbereich auf Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="2c390-134">On the Action Pane, click Configurations.</span></span>  
 2. <span data-ttu-id="2c390-135">Klicken Sie auf Benutzerparameter.</span><span class="sxs-lookup"><span data-stu-id="2c390-135">Click User parameters.</span></span>  
 3. <span data-ttu-id="2c390-136">Wählen Sie "Ja" im Feld "Testlaufeinstellungen".</span><span class="sxs-lookup"><span data-stu-id="2c390-136">Select Yes in the Run settings field.</span></span>  
  <span data-ttu-id="2c390-137">Aktivieren Sie die Markierung „Entwurf ausführen“, um die Entwurfsversion des ausgewählten Formats zu starten, anstelle der abgeschlossenen Version.</span><span class="sxs-lookup"><span data-stu-id="2c390-137">Turn on the 'Run draft' flag to start the draft version of the selected format instead of the completed one.</span></span>  
 4. <span data-ttu-id="2c390-138">Klicken Sie auf "OK".</span><span class="sxs-lookup"><span data-stu-id="2c390-138">Click OK.</span></span>  

## <a name="configure-cash--bank-management-parameters"></a><span data-ttu-id="2c390-139">Bargeld- und Bankverwaltungsparameter konfigurieren</span><span class="sxs-lookup"><span data-stu-id="2c390-139">Configure Cash & bank management parameters</span></span>  
 1. <span data-ttu-id="2c390-140">Gehen Sie zu "Bargeld- und Bankverwaltung" > Bankkonten > Bankkonten.</span><span class="sxs-lookup"><span data-stu-id="2c390-140">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>  
 2. <span data-ttu-id="2c390-141">Verwenden Sie den Schnellfilter, um im Feld "Bankkonto" nach dem Wert "USMF OPER" zu filtern.</span><span class="sxs-lookup"><span data-stu-id="2c390-141">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>  
 3. <span data-ttu-id="2c390-142">Klicken Sie im Aktivitätsbereich auf "Einrichten".</span><span class="sxs-lookup"><span data-stu-id="2c390-142">On the Action Pane, click Set up.</span></span>  
 4. <span data-ttu-id="2c390-143">Klicken Sie auf "Prüfen".</span><span class="sxs-lookup"><span data-stu-id="2c390-143">Click Check.</span></span>  
 5. <span data-ttu-id="2c390-144">Erweitern Sie den Abschnitt 'Einstellungen'.</span><span class="sxs-lookup"><span data-stu-id="2c390-144">Expand the Setup section.</span></span>  
 6. <span data-ttu-id="2c390-145">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="2c390-145">Click Edit.</span></span>  
 7. <span data-ttu-id="2c390-146">Wählen Sie „Ja” im Feld „Unternehmenslogo” aus.</span><span class="sxs-lookup"><span data-stu-id="2c390-146">Select Yes in the Company logo field.</span></span>  
 8. <span data-ttu-id="2c390-147">Klicken Sie auf „Unternehmenslogo”.</span><span class="sxs-lookup"><span data-stu-id="2c390-147">Click Company logo.</span></span>  
 9. <span data-ttu-id="2c390-148">Klicken Sie auf "Ändern".</span><span class="sxs-lookup"><span data-stu-id="2c390-148">Click Change.</span></span>  
 10. <span data-ttu-id="2c390-149">Klicken Sie auf „Durchsuchen”, und wählen die Datei aus, die Sie vorher heruntergeladen haben, nämlich „Unternehmenslogo.png”.</span><span class="sxs-lookup"><span data-stu-id="2c390-149">Click Browse and select the file that you downloaded earlier, Company logo.png.</span></span>   
 11. <span data-ttu-id="2c390-150">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="2c390-150">Click Save.</span></span>  
 12. <span data-ttu-id="2c390-151">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="2c390-151">Close the page.</span></span>  
 13. <span data-ttu-id="2c390-152">Erweitern Sie den Abschnitt "Unterschrift".</span><span class="sxs-lookup"><span data-stu-id="2c390-152">Expand the Signature section.</span></span>  
 14. <span data-ttu-id="2c390-153">Wählen Sie „Ja” im Feld „Erste Unterschrift drucken” aus.</span><span class="sxs-lookup"><span data-stu-id="2c390-153">Select Yes in the Print first signature field.</span></span>  
 15. <span data-ttu-id="2c390-154">Klicken Sie auf "Ändern".</span><span class="sxs-lookup"><span data-stu-id="2c390-154">Click Change.</span></span>  
 16. <span data-ttu-id="2c390-155">Klicken Sie auf „Durchsuchen”, und wählen die Datei aus, die Sie vorher heruntergeladen haben, nämlich „Unterschriftsbild.png”.</span><span class="sxs-lookup"><span data-stu-id="2c390-155">Click Browse and select the file that you downloaded earlier, Signature image.png.</span></span>   
 17. <span data-ttu-id="2c390-156">Erweitern Sie den Abschnitt Kopien.</span><span class="sxs-lookup"><span data-stu-id="2c390-156">Expand the Copies section.</span></span>  
 18. <span data-ttu-id="2c390-157">Wählen Sie im Feld „Wasserzeichen” eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="2c390-157">In the Watermark field, select an option.</span></span>  
 19. <span data-ttu-id="2c390-158">Wählen Sie „Ja” im Feld „Generisches elektronisches Exportformat” aus.</span><span class="sxs-lookup"><span data-stu-id="2c390-158">Select Yes in the Generic electronic Export format field.</span></span>  
 20. <span data-ttu-id="2c390-159">Wählen Sie die Konfiguration „Scheckausdruckformular” aus.</span><span class="sxs-lookup"><span data-stu-id="2c390-159">Select 'Cheques printing form' configuration.</span></span>  
 21. <span data-ttu-id="2c390-160">Nun wird das ausgewählte EB-Format für das Drucken von Schecks verwendet.</span><span class="sxs-lookup"><span data-stu-id="2c390-160">Now the selected ER format will be used for printing cheques.</span></span>  
 22. <span data-ttu-id="2c390-161">Klicken Sie auf Anhänge.</span><span class="sxs-lookup"><span data-stu-id="2c390-161">Click Attach.</span></span>  
 23. <span data-ttu-id="2c390-162">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="2c390-162">Click New.</span></span>  
 24. <span data-ttu-id="2c390-163">Klicken Sie auf "Datei".</span><span class="sxs-lookup"><span data-stu-id="2c390-163">Click File.</span></span>  
 25. <span data-ttu-id="2c390-164">Klicken Sie auf „Durchsuchen”, und wählen die Datei aus, die Sie vorher heruntergeladen haben, nämlich „Unterschriftsbild 2.png”.</span><span class="sxs-lookup"><span data-stu-id="2c390-164">Click Browse and select the file that you downloaded earlier, Signature image 2.png.</span></span>   
 26. <span data-ttu-id="2c390-165">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="2c390-165">Close the page.</span></span>  
 27. <span data-ttu-id="2c390-166">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="2c390-166">Close the page.</span></span>  
 28. <span data-ttu-id="2c390-167">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="2c390-167">Close the page.</span></span>  
 29. <span data-ttu-id="2c390-168">Wechseln Sie zu "Kasse und Bankverwaltung > Einstellungen > Parameter für Kasse- und Bankverwaltung.</span><span class="sxs-lookup"><span data-stu-id="2c390-168">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>  
 30. <span data-ttu-id="2c390-169">Wählen Sie „Ja” im Feld „Erstellung von Testtransaktionen für inaktive Bankkonten zulassen:” aus.</span><span class="sxs-lookup"><span data-stu-id="2c390-169">Select Yes in the Allow prenote creation on inactive bank accounts: field.</span></span>  
 31. <span data-ttu-id="2c390-170">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="2c390-170">Click Save.</span></span>  
 32. <span data-ttu-id="2c390-171">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="2c390-171">Close the page.</span></span>  
