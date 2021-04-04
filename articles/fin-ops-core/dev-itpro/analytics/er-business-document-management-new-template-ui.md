---
title: Neue Benutzeroberfläche für Dokumente in der Geschäftsdokumentenverwaltung
description: Dieses Thema enthält Informationen zur Verwendung der neuen Benutzeroberfläche in der Geschäftsdokumentverwaltung-Funktion des Frameworks für elektronische Berichterstellung (EB).
author: v-anamir
manager: AnnBe
ms.date: 05/12/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-anamir
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7f8099f2f6872c34c30de918a6fc5fd27bcde958
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565709"
---
# <a name="new-document-user-interface-in-business-document-management"></a><span data-ttu-id="ec616-103">Neue Benutzeroberfläche für Dokumente in der Geschäftsdokumentenverwaltung</span><span class="sxs-lookup"><span data-stu-id="ec616-103">New document user interface in Business document management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ec616-104">Mit der Geschäftsdokumentverwaltung können geschäftliche Benutzer Geschäftsdokumentvorlagen mit einem Microsoft 365-Dienst oder der entsprechenden Microsoft Office-Desktopanwendung bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="ec616-104">Business document management lets business users edit business document templates by using a Microsoft 365 service or the appropriate Microsoft Office desktop application.</span></span> <span data-ttu-id="ec616-105">Bearbeitungen können Entwurfsänderungen oder neue Bereitstellungen umfassen. Benutzer können auch Platzhalter hinzufügen, um zusätzliche Daten aufzunehmen, ohne den Quellcode ändern zu müssen.</span><span class="sxs-lookup"><span data-stu-id="ec616-105">Edits might include design changes or new deployments, or users might add placeholders to include additional data without having to change the source code.</span></span> <span data-ttu-id="ec616-106">Weitere Informationen zum Arbeiten mit der Geschäftsdokumentenverwaltung finden Sie unter [Überblick über die Geschäftsdokumentverwaltung](er-business-document-management.md).</span><span class="sxs-lookup"><span data-stu-id="ec616-106">For more information about how to work with Business document management, see [Business document management overview](er-business-document-management.md).</span></span>

<span data-ttu-id="ec616-107">Die neue Benutzeroberfläche für Dokumente ist übersichtlicher und benutzerfreundlicher.</span><span class="sxs-lookup"><span data-stu-id="ec616-107">The new document user interface (UI) is clearer and more comfortable to use.</span></span> <span data-ttu-id="ec616-108">Der **Geschäftsdokument**-Bereich zeigt nur die Vorlagen, die für den aktuellen Anbieter verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="ec616-108">The **Business document** area shows only the templates that are available for the current provider.</span></span>

<span data-ttu-id="ec616-109">Mit der Schaltfläche **Neues Dokument** können Benutzer eine Vorlage in einer ER-Formatkonfiguration bearbeiten, die von einem anderen Anbieter bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="ec616-109">The **New document** button lets users create and edit a template in an Electronic reporting (ER) format configuration that is provided by another provider.</span></span> <span data-ttu-id="ec616-110">Im Beispiel dieses Themas ist der Anbieter Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ec616-110">In the example in this topic, the provider is Microsoft.</span></span>

## <a name="make-the-new-document-ui-in-business-document-management-available"></a><span data-ttu-id="ec616-111">Neue Benutzeroberfläche für die Geschäftsdokumentverwaltung zur Verfügung stellen</span><span class="sxs-lookup"><span data-stu-id="ec616-111">Make the new document UI in Business document management available</span></span>

<span data-ttu-id="ec616-112">Um die neue Dokument-Benutzeroberfläche in der Geschäftsdokumentverwaltung zu verwenden, müssen Sie die Funktion **Office-ähnliche UI-Erfahrung für Geschäftsdokumentverwaltung** im Arbeitsbereich **Funktionsverwaltung** aktivieren.</span><span class="sxs-lookup"><span data-stu-id="ec616-112">To start to use the new document UI in Business document management, you must turn on the **Office-like UI experience for Business document management** feature in the **Feature management** workspace.</span></span>

<span data-ttu-id="ec616-113">Befolgen Sie diese Schritte, um diese Funktion für alle juristischen Personen zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="ec616-113">Follow these steps to turn on this feature for all legal entities.</span></span>

1. <span data-ttu-id="ec616-114">Wählen Sie im Arbeitsbereich **Funktionsverwaltung** auf der Registerkarte **Neu** die Funktion **Office-ähnliche UI-Erfahrung für Geschäftsdokumentverwaltung** aus der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="ec616-114">In the **Feature management** workspace, on the **New** tab, select the **Office-like UI experience for Business document management** feature in the list.</span></span>
2. <span data-ttu-id="ec616-115">Wählen Sie **Jetzt aktivieren** aus, um die ausgewählte Fähigkeit zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="ec616-115">Select **Enable now** to turn on the selected feature.</span></span>
3. <span data-ttu-id="ec616-116">Aktualisieren Sie die Seite, um auf die neue Funktion zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="ec616-116">Refresh the page to access the new feature.</span></span>

### <a name="edit-templates-that-are-owned-by-other-providers"></a><span data-ttu-id="ec616-117">Vorlagen anderer Anbieter bearbeiten</span><span class="sxs-lookup"><span data-stu-id="ec616-117">Edit templates that are owned by other providers</span></span>

1. <span data-ttu-id="ec616-118">Wählen Sie im Arbeitsbereich **Geschäftsdokumentverwaltung** **Neues Dokument** aus.</span><span class="sxs-lookup"><span data-stu-id="ec616-118">In the **Business document management** workspace, select **New document**.</span></span>

    ![Arbeitsbereich Geschäftsdokumentenverwaltung](./media/BDM_overview_new_template1.png)

2. <span data-ttu-id="ec616-120">Wählen Sie im Dialogfeld das Dokument aus, das als Vorlage verwendet werden soll, und wählen Sie **Dokument erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="ec616-120">In the dialog box, select the document to use as a template, and then select **Create document**.</span></span>

    ![Dialogfeld „Geschäftsdokumente“](./media/BDM_overview_new_template2.png)

3. <span data-ttu-id="ec616-122">Ändern Sie im neuen Dialogfeld im Feld **Titel** den Titel nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="ec616-122">In the new dialog box, in the **Title** field, change the title as you require.</span></span> <span data-ttu-id="ec616-123">Der Titeltext wird zum Benennen der neuen ER-Formatkonfiguration verwendet, die automatisch erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="ec616-123">The title text is used to name the new ER format configuration that is automatically created.</span></span> <span data-ttu-id="ec616-124">Die Entwurfsversion dieser Konfiguration (**Debitoren-FTI-Bericht (GER) – Kopie**) enthält die bearbeitete Vorlage und wird verwendet, um dieses ER-Format für den aktuellen Benutzer auszuführen.</span><span class="sxs-lookup"><span data-stu-id="ec616-124">The draft version of this configuration (**Customer FTI report (GER) Copy**) will contain the edited template and will be used to run this ER format for the current user.</span></span> <span data-ttu-id="ec616-125">Die ursprüngliche Vorlage von der Basis-ER-Formatkonfiguration wird verwendet, um dieses ER-Format für jeden anderen Benutzer auszuführen.</span><span class="sxs-lookup"><span data-stu-id="ec616-125">The original template from the base ER format configuration will be used to run this ER format for every other user.</span></span>
4. <span data-ttu-id="ec616-126">Ändern Sie im Feld **Name** den Namen der ersten Überarbeitung der bearbeitbaren Vorlage, die automatisch erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="ec616-126">In the **Name** field, change the name of the first revision of the editable template that will be automatically created.</span></span>
5. <span data-ttu-id="ec616-127">Aktualisieren Sie im Feld **Kommentar** die Anmerkungen für die Überarbeitung der bearbeitbaren Vorlage, die automatisch erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="ec616-127">In the **Comment** field, update the remarks for the revision of the editable template that will be automatically created.</span></span>
6. <span data-ttu-id="ec616-128">Wählen Sie **OK** aus, um den Beginn des Bearbeitungsprozesses zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="ec616-128">Select **OK** to confirm the start of the editing process.</span></span>

    ![Dialogfeld zur Dokumentenerstellung](./media/BDM_overview_new_template3.png)

<span data-ttu-id="ec616-130">Die Schaltfläche **Neues Dokument** wird verwendet, um eine Vorlage in einer ER-Formatkonfiguration zu erstellen und zu bearbeiten, die von einem anderen Anbieter bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="ec616-130">The **New document** button is used to create and edit a template in an ER format configuration that is provided by another provider.</span></span> <span data-ttu-id="ec616-131">In diesem Beispiel ist der Anbieter Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ec616-131">In this example, the provider is Microsoft.</span></span> <span data-ttu-id="ec616-132">Wenn Sie auf **Neues Dokument** klicken, sehen Sie alle Vorlagen, die sich im Besitz aktueller und anderer Anbieter befinden.</span><span class="sxs-lookup"><span data-stu-id="ec616-132">When you select **New document**, you can view all the templates that are owned by current and other providers.</span></span> <span data-ttu-id="ec616-133">Nachdem Sie die Vorlage ausgewählt haben, wird sie zur Bearbeitung geöffnet.</span><span class="sxs-lookup"><span data-stu-id="ec616-133">After you select the template, it's opened for editing.</span></span> <span data-ttu-id="ec616-134">Die bearbeitete Vorlage wird dann in einer neuen ER-Formatkonfiguration gespeichert, die automatisch generiert wird.</span><span class="sxs-lookup"><span data-stu-id="ec616-134">The edited template will then be stored in a new ER format configuration that is automatically generated.</span></span>

<span data-ttu-id="ec616-135">Weitere Informationen finden Sie unter [Überblick über die Geschäftsdokumentverwaltung](er-business-document-management.md).</span><span class="sxs-lookup"><span data-stu-id="ec616-135">For more information, see [Business document management overview](er-business-document-management.md).</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]