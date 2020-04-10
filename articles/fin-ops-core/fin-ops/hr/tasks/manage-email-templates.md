---
title: E-Mail-Vorlagen verwalten
description: In diesem Thema wird erläutert, wie Sie E-Mail-Vorlagen verwalten.
author: andreabichsel
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMApplicationWordBookmark, HRMApplicationEmailTemplate
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9a911fea9e7d1009160a021e53533c0ce49efbfe
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143695"
---
# <a name="manage-email-templates"></a><span data-ttu-id="b8b0c-103">E-Mail-Vorlagen verwalten</span><span class="sxs-lookup"><span data-stu-id="b8b0c-103">Manage email templates</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b8b0c-104">Sie können Informationen aus der Datenbank Ihrer Organisation in die Lesezeichen in einem neuen Dokument übertragen und in Vorlagen verwenden, die Sie bei der Kommunikation mit Bewerbern und Kandidaten unterstützen.</span><span class="sxs-lookup"><span data-stu-id="b8b0c-104">You can transfer information from your organization's database to the bookmarks in a new document and use it in templates that help you communicate efficiently with applicants and candidates.</span></span> <span data-ttu-id="b8b0c-105">Hierfür muss eine Vorlage mit Standardtext und einigen Lesezeichen an den Positionen erstellt werden, an denen die Systemdaten eingefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b8b0c-105">To do this, you create a template that contains standard text and some bookmarks where the system data should be inserted.</span></span> <span data-ttu-id="b8b0c-106">So können Sie z. B. Adresse und Kontaktinformationen für einen Bewerber in ein Microsoft Word-Dokument einfügen, das Sie bei der Kommunikation mit diesem Bewerber verwenden können.</span><span class="sxs-lookup"><span data-stu-id="b8b0c-106">For example, you can insert address and contact information for an applicant into a Microsoft Word document that you can use when communicating with that applicant.</span></span> <span data-ttu-id="b8b0c-107">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="b8b0c-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="select-which-bookmarks-to-use-in-your-email-templates"></a><span data-ttu-id="b8b0c-108">Auswählen der Lesezeichen für die E-Mail-Vorlagen</span><span class="sxs-lookup"><span data-stu-id="b8b0c-108">Select which bookmarks to use in your email templates</span></span>
1. <span data-ttu-id="b8b0c-109">Gehen Sie im Navigationsbereich zu **Module > Human Resources > Recruitment > Communication > Application bookmarks**.</span><span class="sxs-lookup"><span data-stu-id="b8b0c-109">In the navigation pane, go to **Modules > Human Resources > Recruitment > Communication > Application bookmarks**.</span></span>
2. <span data-ttu-id="b8b0c-110">Suchen Sie in der Liste die gewünschten Korrespondenzaktivität, und wählen Sie sie aus.</span><span class="sxs-lookup"><span data-stu-id="b8b0c-110">In the list, find and select the desired correspondence action.</span></span>
3. <span data-ttu-id="b8b0c-111">Wählen Sie **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="b8b0c-111">Select **Edit**.</span></span>
4. <span data-ttu-id="b8b0c-112">Wählen Sie die Felder aus, die Sie in einer E-Mail-Vorlage für die ausgewählte Korrespondenzaktivität verwenden möchten, und verschieben Sie sie in die Lesezeichenfelder.</span><span class="sxs-lookup"><span data-stu-id="b8b0c-112">Select the fields you would like to be able to use in an email template for the selected Correspondence action and move them to the Bookmark fields.</span></span>  
5. <span data-ttu-id="b8b0c-113">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="b8b0c-113">Close the page.</span></span>

## <a name="create-an-email-template"></a><span data-ttu-id="b8b0c-114">E-Mail-Vorlage erstellen</span><span class="sxs-lookup"><span data-stu-id="b8b0c-114">Create an email template</span></span>
1. <span data-ttu-id="b8b0c-115">Gehen Sie im Navigationsbereich zu **Module > Personal > Personalwesen > Personalbeschaffung > Kommunikation > Vorlagen für Bewerbungs-E-Mails**.</span><span class="sxs-lookup"><span data-stu-id="b8b0c-115">In the navigation pane, go to **Modules > Human resources > Recruitment > Communication > Application e-mail templates**.</span></span>
2. <span data-ttu-id="b8b0c-116">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="b8b0c-116">Select **New**.</span></span>
3. <span data-ttu-id="b8b0c-117">Wählen Sie im Feld **Korrespondenzaktion** **Interview**.</span><span class="sxs-lookup"><span data-stu-id="b8b0c-117">In the **Correspondence action** field, select **Interview**.</span></span> <span data-ttu-id="b8b0c-118">Wählen Sie die Korrespondenzaktivität aus, die Lesezeichen enthält, die für diese Art der E-Mail-Kommunikation verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b8b0c-118">Select the correspondence action that contains the bookmarks to use for this type of email communication.</span></span>  
4. <span data-ttu-id="b8b0c-119">Geben Sie in das Feld **E-Mail-Vorlage** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="b8b0c-119">In the **E-mail template** field, type a value.</span></span>
5. <span data-ttu-id="b8b0c-120">Geben Sie in das Feld **Subjekt** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="b8b0c-120">In the **Subject** field, type a value.</span></span>
6. <span data-ttu-id="b8b0c-121">Geben Sie im Feld **Text** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="b8b0c-121">In the **Text** field, type a value.</span></span>
7. <span data-ttu-id="b8b0c-122">Suchen Sie in der Liste das gewünschte Lesezeichenfeld, und wählen Sie es aus.</span><span class="sxs-lookup"><span data-stu-id="b8b0c-122">In the list, find and select the desired bookmark field.</span></span>
8. <span data-ttu-id="b8b0c-123">Setzen Sie die Eingabe der E-Mail-Nachricht fort, und fügen Sie die Lesezeichenfelder an den gewünschten Positionen ein.</span><span class="sxs-lookup"><span data-stu-id="b8b0c-123">Continue typing your email message, inserting the bookmark fields where you need them.</span></span>
9. <span data-ttu-id="b8b0c-124">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="b8b0c-124">Select **Save**.</span></span>

