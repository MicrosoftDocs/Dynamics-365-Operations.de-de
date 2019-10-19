---
title: Bewerber- und Anwendungsdaten manuell eingeben
description: Im folgenden Verfahren, wird dargestellt, wie Sie Informationen über Bewerber und deren Bewerbung manuell verwalten.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmApplicant, LogisticsContactInfoGrid, HRMApplication,  DirPartyTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ea61e3c1d76ade6e0d694b4b521e4be76fc8799d
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178012"
---
# <a name="enter-applicant-and-application-data-manually"></a><span data-ttu-id="0a830-103">Bewerber- und Anwendungsdaten manuell eingeben</span><span class="sxs-lookup"><span data-stu-id="0a830-103">Enter applicant and application data manually</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0a830-104">Im folgenden Verfahren, wird dargestellt, wie Sie Informationen über Bewerber und deren Bewerbung manuell verwalten.</span><span class="sxs-lookup"><span data-stu-id="0a830-104">This procedure shows how to manually maintain information about applicants and their application.</span></span>   <span data-ttu-id="0a830-105">Sie können die persönlichen Daten, Befragungsdatumsangaben und -zeiten, Referenzen, Kompetenzen und Anpassungsersuchen für Bewerber eingeben und verwalten.</span><span class="sxs-lookup"><span data-stu-id="0a830-105">You can enter and maintain personal information, interview dates and times, references, competencies, and accommodation requests for applicants.</span></span> <span data-ttu-id="0a830-106">Sie können außerdem den Status der Bewerbungen der Bewerber aktualisieren und Briefe oder E-Mail-Nachrichten für die Kommunikation mit Bewerbern erstellen.</span><span class="sxs-lookup"><span data-stu-id="0a830-106">You can also update the status of applicants’ applications for employment and create letters or email messages to communicate with applicants.</span></span> <span data-ttu-id="0a830-107">Wenn Sie einen Bewerberdatensatz erstellen, wird ein Personendatensatz für diesen Bewerber im globalen Adressbuch erstellt.</span><span class="sxs-lookup"><span data-stu-id="0a830-107">When you create an applicant record, a person record for that applicant is created in the global address book.</span></span>       <span data-ttu-id="0a830-108">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="0a830-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-new-applicant-record"></a><span data-ttu-id="0a830-109">Neuen Bewerberdatensatz erstellen</span><span class="sxs-lookup"><span data-stu-id="0a830-109">Create a new applicant record</span></span>
1. <span data-ttu-id="0a830-110">Wechseln Sie zu "Personalverwaltung" > "Personalbeschaffung" > "Bewerber" > "Bewerber".</span><span class="sxs-lookup"><span data-stu-id="0a830-110">Go to Human resources > Recruitment > Applicants > Applicants.</span></span>
2. <span data-ttu-id="0a830-111">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="0a830-111">Click New.</span></span>
3. <span data-ttu-id="0a830-112">Geben Sie im Feld "Vorname" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="0a830-112">In the First name field, type a value.</span></span>
4. <span data-ttu-id="0a830-113">Geben Sie im Feld "Nachname" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="0a830-113">In the Last name field, type a value.</span></span>
    * <span data-ttu-id="0a830-114">Sie können zusätzliche Bewerberinformationen eingeben, sofern solche vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="0a830-114">You can enter additional applicant information if it's available.</span></span> <span data-ttu-id="0a830-115">So können Informationen zum höchsten Abschluss des Bewerbers, den Titel der aktuellen Position oder den früheren Arbeitgeber angeben.</span><span class="sxs-lookup"><span data-stu-id="0a830-115">For example, information can include the applicant's highest degree, current job title, or previous employer.</span></span>  
5. <span data-ttu-id="0a830-116">Schalten Sie die Erweiterung des Abschnitts "Kontaktinformationen" ein/aus.</span><span class="sxs-lookup"><span data-stu-id="0a830-116">Toggle the expansion of the Contact information section.</span></span>
6. <span data-ttu-id="0a830-117">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="0a830-117">Click Add.</span></span>
7. <span data-ttu-id="0a830-118">Geben Sie im Feld "Beschreibung" "E-Mail-Kommunikation" ein.</span><span class="sxs-lookup"><span data-stu-id="0a830-118">In the Description field, type 'Communications email'.</span></span>
8. <span data-ttu-id="0a830-119">Wählen Sie im Feld "Typ" eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="0a830-119">In the Type field, select an option.</span></span>
9. <span data-ttu-id="0a830-120">Geben Sie im Feld "Kontaktnummer/-adresse" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="0a830-120">In the Contact number/address field, type a value.</span></span>
    * <span data-ttu-id="0a830-121">Diese E-Mail-Adresse wird verwendet, um E-Mail-Kommunikation mit dem Bewerber zu generieren.</span><span class="sxs-lookup"><span data-stu-id="0a830-121">This email address will be used to generate email communication with the applicant.</span></span>  
10. <span data-ttu-id="0a830-122">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="0a830-122">Click Add.</span></span>
11. <span data-ttu-id="0a830-123">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="0a830-123">In the Description field, type a value.</span></span>
12. <span data-ttu-id="0a830-124">Geben Sie im Feld "Kontaktnummer/-adresse" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="0a830-124">In the Contact number/address field, type a value.</span></span>
    * <span data-ttu-id="0a830-125">Persönliche Daten des Bewerbers.</span><span class="sxs-lookup"><span data-stu-id="0a830-125">Applicant personal information.</span></span>  
    * <span data-ttu-id="0a830-126">Sie können nach Bedarf zusätzliche persönliche Informationen für den Bewerber eingeben.</span><span class="sxs-lookup"><span data-stu-id="0a830-126">You can enter additional personal information for the applicant, if needed.</span></span> <span data-ttu-id="0a830-127">Dies kann beispielsweise Geburtsdatum, Nationalität, Geschlecht oder Familienstand umfassen.</span><span class="sxs-lookup"><span data-stu-id="0a830-127">For example, this can include birth date, ethnic origin, gender, or marital status.</span></span>  
13. <span data-ttu-id="0a830-128">Klicken Sie im Aktivitätsbereich auf "Kompetenzen".</span><span class="sxs-lookup"><span data-stu-id="0a830-128">On the Action Pane, click Competencies.</span></span>
    * <span data-ttu-id="0a830-129">Sie können das Kompetenzprofil des Bewerbers eingeben, einschließlich dessen Qualifikationen, Berufserfahrungen, Ausbildung, Tests oder Bescheinigungen.</span><span class="sxs-lookup"><span data-stu-id="0a830-129">You can enter the applicant's competency profile, including their skills, professional experiences, education, tests, or certificates.</span></span>  
    * <span data-ttu-id="0a830-130">Diese Informationen können verwendet werden, um die Qualifikationen des Bewerbers den Fähigkeiten zuzuordnen, die mit den Einzelvorgängen verknüpft sind, die in den Ihren Daten des Unternehmens definiert werden.</span><span class="sxs-lookup"><span data-stu-id="0a830-130">This information can be used to map the applicant's skills to the skills associated with the jobs defined in your company's data.</span></span>   

## <a name="create-an-application-for-the-applicant"></a><span data-ttu-id="0a830-131">Erstellen Sie eine Bewerbung für einen Bewerber.</span><span class="sxs-lookup"><span data-stu-id="0a830-131">Create an application for the applicant</span></span>
1. <span data-ttu-id="0a830-132">Klicken Sie auf "Bewerbungen".</span><span class="sxs-lookup"><span data-stu-id="0a830-132">Click Applications.</span></span>
2. <span data-ttu-id="0a830-133">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="0a830-133">Click New.</span></span>
3. <span data-ttu-id="0a830-134">Klicken Sie im Feld "Personalbeschaffungsprojekt" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="0a830-134">In the Recruitment project field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="0a830-135">Wenn Sie ein Personalbeschaffungsprojekt auswählen, wird der Bewerber einer bestimmten Eröffnung zugeordnet, die in diesem Personalbeschaffungsprojekt enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="0a830-135">By selecting a recruitment project, the applicant will be associated with a specific opening included in that recruitment project.</span></span>  
4. <span data-ttu-id="0a830-136">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="0a830-136">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="0a830-137">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="0a830-137">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="0a830-138">Standardmäßig basieren der Einzelvorgang und die Abteilung auf dem ausgewählten Personalbeschaffungsprojekt.</span><span class="sxs-lookup"><span data-stu-id="0a830-138">By default, the job and department are based on the selected recruitment project.</span></span>  
6. <span data-ttu-id="0a830-139">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="0a830-139">Click Save.</span></span>
    * <span data-ttu-id="0a830-140">Nachdem Sie die Bewerbung gespeichert haben, können Sie Dokumente anfügen, einschließlich Dokumente zur Erfahrung des Bewerbers, zu Auszeichnungen und das Anschreiben.</span><span class="sxs-lookup"><span data-stu-id="0a830-140">After saving the application, you can attach documents to it, including the applicant's experience, awards, and cover letter.</span></span>  

