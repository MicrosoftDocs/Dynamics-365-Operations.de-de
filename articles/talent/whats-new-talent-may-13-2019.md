---
title: Neuerungen oder Änderungen in Dynamics 365 for Talent (13. Mai 2019)
description: In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 for Talent entweder neu oder geändert sind.
author: Darinkramer
manager: AnnBe
ms.date: 05/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-05-13
ms.dyn365.ops.version: Talent
ms.openlocfilehash: ffeeb3e2f5279a84c4c060b04fe46836b778f6c5
ms.sourcegitcommit: 1bf6a8b2f872394a4f242f9ff13c67e8e1ae8f65
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/03/2019
ms.locfileid: "1856447"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-may-13-2019"></a><span data-ttu-id="ce948-103">Neuerungen oder Änderungen in Dynamics 365 for Talent (13. Mai 2019)</span><span class="sxs-lookup"><span data-stu-id="ce948-103">What's new or changed in Dynamics 365 for Talent (May 13, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ce948-104">In diesem Thema werden die Funktionen beschrieben, die in Dynamics 365 for Talent neu oder geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="ce948-104">This topic describes features that are either new or changed in Dynamics 365 for Talent.</span></span>

## <a name="coming-soon-in-attract"></a><span data-ttu-id="ce948-105">Bald verfügbar in Attract</span><span class="sxs-lookup"><span data-stu-id="ce948-105">Coming soon in Attract</span></span>

### <a name="job-approvals-on-home-page"></a><span data-ttu-id="ce948-106">Stellengenehmigungen auf Startseite</span><span class="sxs-lookup"><span data-stu-id="ce948-106">Job approvals on home page</span></span>

<span data-ttu-id="ce948-107">Genehmigungen werden im Abschnitt **Genehmigungen** im Dashboard angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ce948-107">Approvals appear in an **Approvals** section on the dashboard.</span></span> <span data-ttu-id="ce948-108">Genehmiger können ihre Genehmigungen unter **Ihnen zugewiesen** überprüfen, wo die Stellen-ID, Titel, andere Genehmiger und Datum der Zuweisung angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ce948-108">Approvers can review their approvals under **Assigned to you**, which displays the job ID, title, other approvers, and date assigned.</span></span> <span data-ttu-id="ce948-109">Benutzer, die eine Stelle zur Genehmigung übermitteln, können ihre Stellen unter **Von Ihnen angefordert** überprüfen. Dort werden die Genehmiger angezeigt, die immer noch die übermittelte Stelle genehmigen müssen.</span><span class="sxs-lookup"><span data-stu-id="ce948-109">Users who submit a job for approval can review their jobs under **Requested by you**, which displays the approvers who still need to approve the submitted job.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="ce948-110">Änderungen in Onboard</span><span class="sxs-lookup"><span data-stu-id="ce948-110">Changes in Onboard</span></span>

<span data-ttu-id="ce948-111">Diese Version enthält kleinere Fehlerkorrekturen für Dynamics 365 Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="ce948-111">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="ce948-112">Core HR-Änderungen</span><span class="sxs-lookup"><span data-stu-id="ce948-112">Changes in Core HR</span></span>

<span data-ttu-id="ce948-113">Die in diesem Abschnitt beschriebenen Änderungen gelten für Buildnummer 8.1.2297.</span><span class="sxs-lookup"><span data-stu-id="ce948-113">Changes described in this section apply to build number 8.1.2297.</span></span> <span data-ttu-id="ce948-114">Die Zahlen in Klammern in einigen Überschriften beziehen sich auf Supportnummern in Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="ce948-114">The numbers in parentheses in some headings refer to support numbers in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

### <a name="indicate-instance-type-when-provisioning-talent"></a><span data-ttu-id="ce948-115">Geben Sie den Instanztyp an, wenn Sie Talent bereitstellen</span><span class="sxs-lookup"><span data-stu-id="ce948-115">Indicate instance type when provisioning Talent</span></span>

<span data-ttu-id="ce948-116">Wenn Sie eine neue Talent-Instanz bereitstellen, können Sie angeben, ob der Instanztyp **Produktion** oder **Sandkasten** lautet. Dies ermöglicht frühes Testen neuer Funktionen.</span><span class="sxs-lookup"><span data-stu-id="ce948-116">When provisioning a new instance of Talent, you can indicate whether the instance type is **Production** or **Sandbox**, which allows for early testing of new features.</span></span> <span data-ttu-id="ce948-117">Alle vorhandenen Talent-Instanzen werden zum Instanztyp **Produktion** aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="ce948-117">All existing Talent instances will be updated to the **Production** instance type.</span></span> <span data-ttu-id="ce948-118">Wenn eine der vorhandenen Instanzen auf den Instanztyp **Sandbox** aktualisiert werden soll, wenden Sie sich an den [Support](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support), um die Änderungsanforderung zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="ce948-118">If you want one of your existing instances to be updated to the **Sandbox** instance type, please contact [Support](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) to initiate the change request.</span></span>

### <a name="common-data-service-entity-support-for-custom-fields"></a><span data-ttu-id="ce948-119">Common Data Service-Entitätssupport für benutzerdefinierte Felder</span><span class="sxs-lookup"><span data-stu-id="ce948-119">Common Data Service entity support for custom fields</span></span>

<span data-ttu-id="ce948-120">In der Version dieser Woche unterstützen die folgenden Entitäten von Common Data Service nun benutzerdefinierte Felder: Anstellung, Vergütungsberechnungshäufigkeit, Vergütungsberechnungssatz, Vergütungstyp, Arbeitskalender, Arbeitskalenderfeiertag und Kennungstyp.</span><span class="sxs-lookup"><span data-stu-id="ce948-120">In this week's release, the following Common Data Service entities now support custom fields: Employment, Benefit calc frequency, Benefit calc rate, Work calendar holiday, and Identification type.</span></span>

### <a name="common-data-service-integration-page"></a><span data-ttu-id="ce948-121">Common Data Service-Integrationsseite</span><span class="sxs-lookup"><span data-stu-id="ce948-121">Common Data Service integration page</span></span>

<span data-ttu-id="ce948-122">Diese Version bietet eine neue Option in **Systemverwaltung verknüpft > Links > Integrationen > Common Data Service-Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="ce948-122">This release provides a new option in **System Administration > Links > Integrations > Common Data Service configuration**.</span></span> <span data-ttu-id="ce948-123">Die Option **Common Data Service-Konfiguration** ermöglicht einem Administrator oder Datenverwaltungsadministrator etwas Flexibilität und Einblicke mit dem Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="ce948-123">The **Common Data Service configuration** option allows an administrator or data management administrator some flexibility and insights with the Common Data Service.</span></span> <span data-ttu-id="ce948-124">Mit dieser Option können Sie Common Data Service-Integration in eine Talent-Instanz aktivieren oder deaktivieren und die Synchronisierungsdetails zwischen der Talent-Instanz und dem Common Data Service anzeigen.</span><span class="sxs-lookup"><span data-stu-id="ce948-124">With this option, you can enable or disable Common Data Service integration with a Talent instance and view the sync details between the Talent instance and the Common Data Service.</span></span>

### <a name="import-performance-data-with-final-employee-rating-316710"></a><span data-ttu-id="ce948-125">Leistungsdaten Sie mit abschließender Mitarbeiterbewertung importieren (316710 )</span><span class="sxs-lookup"><span data-stu-id="ce948-125">Import performance data with final employee rating (316710)</span></span>

<span data-ttu-id="ce948-126">In dieser Version können Sie historische Mitarbeiterbewertungsdaten importieren.</span><span class="sxs-lookup"><span data-stu-id="ce948-126">In this release, you can import historical employee rating data.</span></span> <span data-ttu-id="ce948-127">Das Feld **FinalEmployeeRatingId** hat jetzt eine Schreibberechtigung.</span><span class="sxs-lookup"><span data-stu-id="ce948-127">The **FinalEmployeeRatingId** field now has write permission.</span></span>

### <a name="cant-create-worker-address-in-common-data-service-and-sync-it-with-talent-317555"></a><span data-ttu-id="ce948-128">Arbeitskraftadresse kann in Common Data Service nicht erstellt und mit Talent synchronisiert werden (317555 )</span><span class="sxs-lookup"><span data-stu-id="ce948-128">Can't create Worker address in Common Data Service and sync it with Talent (317555)</span></span>

<span data-ttu-id="ce948-129">Diese Änderung ermöglicht die Synchronisierung von Adressdaten, die in Common Data Service erstellt wurden, mit Talent.</span><span class="sxs-lookup"><span data-stu-id="ce948-129">This change allows address data created in Common Data Service to sync with Talent.</span></span>

## <a name="in-preview"></a><span data-ttu-id="ce948-130">Vorschau</span><span class="sxs-lookup"><span data-stu-id="ce948-130">In preview</span></span>

### <a name="new-page-to-validate-position-hierarchy-data"></a><span data-ttu-id="ce948-131">Neue Seite zur Bestätigung der Positionshierarchiedaten</span><span class="sxs-lookup"><span data-stu-id="ce948-131">New page to validate position hierarchy data</span></span>

<span data-ttu-id="ce948-132">Personalverwaltung und Administratoren können nun die Verwaltungshierarchie für alle Zirkelbezüge prüfen, die möglicherweise versehentlich importiert wurden.</span><span class="sxs-lookup"><span data-stu-id="ce948-132">Human resources (HR) and administrators can validate the managerial hierarchy for any circular references that might have been inadvertently imported.</span></span> <span data-ttu-id="ce948-133">Sie können auf diese neue Seite von **Organisatorische Verwaltung > Links > Positionen > Positionshierarchieprüfung** aus zugreifen.</span><span class="sxs-lookup"><span data-stu-id="ce948-133">You can access this new page from **Organizational administration > Links > Positions > Position hierarchy validation**.</span></span>

### <a name="specify-reason-codes-on-leave-types"></a><span data-ttu-id="ce948-134">Geben Sie Ursachencodes bei Sonderurlaubstypen an</span><span class="sxs-lookup"><span data-stu-id="ce948-134">Specify reason codes on leave types</span></span>

<span data-ttu-id="ce948-135">Organisationen brauchen möglicherweise zusätzliche Informationen zu Freizeitanforderungen.</span><span class="sxs-lookup"><span data-stu-id="ce948-135">Organizations might require additional information about time-off requests.</span></span> <span data-ttu-id="ce948-136">Sie können nun Ursachencodes für Sonderurlaubstypen definieren und Mitarbeiter aktivieren, damit sie einen Ursachencode für ihre Freizeitanforderungen auszuwählen können.</span><span class="sxs-lookup"><span data-stu-id="ce948-136">You can now specify reason codes for leave types and let employees select a reason code on their time-off requests.</span></span>

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a><span data-ttu-id="ce948-137">Erfordert Ursachencodes für bestimmte Urlaubstypen bei Freizeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="ce948-137">Require reason codes for specific leave types on time-off requests</span></span>

<span data-ttu-id="ce948-138">Organisationen brauchen ggf. bestimmte Ursachencodes für Sonderurlaubstypen, wenn Mitarbeiter Freizeit beantragen.</span><span class="sxs-lookup"><span data-stu-id="ce948-138">Organizations might require reason codes for specific leave types when employees submit time-off requests.</span></span> <span data-ttu-id="ce948-139">Diese Anforderung ist möglicherweise aufgrund der Unternehmensrichtlinie oder der gesetzlichen Vorgaben vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ce948-139">This requirement might exist because of company policy or regulatory requirements.</span></span> <span data-ttu-id="ce948-140">Sie können nun angeben, welche Sonderurlaubstypen einen Ursachencode erfordern und Sie können von Mitarbeitern verlangen, dass sie einen Ursachencode für den Sonderurlaubstyp für ihre Abwesenheitsanforderungen angeben.</span><span class="sxs-lookup"><span data-stu-id="ce948-140">You can specify which leave types require a reason code, and you can require that employees provide a reason code for the leave type on their time-off requests.</span></span>

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a><span data-ttu-id="ce948-141">Erstellen Sie eine Urlaub- und Abwesenheitsbuchungsliste für die Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="ce948-141">Provide a leave and absence transaction list for HR</span></span>

<span data-ttu-id="ce948-142">Die Möglichkeit zum Nachverfolgen von Mitarbeiterfreizeit und ein Verständnis dafür, wie Freizeit berechnet wird, hilft nicht nur der Personalverwaltung, Fragen von Mitarbeitern zu beantworten sondern stellt auch sicher, dass die Freizeit für Mitarbeiter korrekt ist.</span><span class="sxs-lookup"><span data-stu-id="ce948-142">The ability to track employee time off and understand how time off is calculated not only helps HR answer employee questions, but also helps ensure accurate time-off awards for employees.</span></span> <span data-ttu-id="ce948-143">Personalverwaltung besitzt nun eine neue Anzeige für die Transaktionen (Zuschüsse, Abgrenzungen, Regulierungen und Anforderungen), sodass die Mitarbeiter der Personalverwaltung die Gründe hinter den Abwesenheitssalden anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="ce948-143">HR now has a new view into the transactions (grants, accruals, adjustments, and requests), so that HR staff can view the reasons behind time-off balances.</span></span>
