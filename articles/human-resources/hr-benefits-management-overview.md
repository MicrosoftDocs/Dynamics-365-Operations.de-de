---
title: Vorteilsverwaltung – Übersicht
description: Übersicht über die Vorschaufunktion für die Vorteilsverwaltung in Dynamics 365 Human Resources. Bieten Sie Ihren Mitarbeitern erweiterte Vorteilsoptionen mit einer benutzerfreundlichen Online-Erfahrung.
author: andreabichsel
ms.date: 09/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 34b0916e0bf618590bcc56a9a3bc7c61576361cc
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805777"
---
# <a name="benefits-management-overview"></a><span data-ttu-id="12fc6-104">Vorteilsverwaltung – Übersicht</span><span class="sxs-lookup"><span data-stu-id="12fc6-104">Benefits management overview</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="12fc6-105">Um wettbewerbsfähig zu bleiben, müssen Sie zahlreiche Vorteile bieten, um die besten Mitarbeiter anzuwerben und zu halten.</span><span class="sxs-lookup"><span data-stu-id="12fc6-105">To remain competitive, you must offer a rich set of benefits to attract and retain your best employees.</span></span> <span data-ttu-id="12fc6-106">Zusätzlich zu den Standardleistungen wie Kranken‑ und Zahnzusatzversicherung möchten Sie möglicherweise auch erweiterte Dienstleistungen wie Adoptionsunterstützung, Freizeitprogramme und Aufwandsentschädigungen anbieten.</span><span class="sxs-lookup"><span data-stu-id="12fc6-106">In addition to standard benefits like medical and dental coverage, you might also want to offer expanded services like adoption assistance, recreation programs, and clothing allowances.</span></span> <span data-ttu-id="12fc6-107">Die Leistungsverwaltung in Microsoft Dynamics 365 Human Resources bietet Ihnen eine flexible Lösung, die eine Vielzahl von Vorteilsoptionen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="12fc6-107">Benefits management in Microsoft Dynamics 365 Human Resources provides you with a flexible solution that supports a wide variety of benefit options.</span></span> <span data-ttu-id="12fc6-108">Human Resources umfasst auch eine benutzerfreundliche Mitarbeitererfahrung, die Ihre Angebote vorstellt.</span><span class="sxs-lookup"><span data-stu-id="12fc6-108">Human Resources also includes an easy-to-use employee experience that showcases your offerings.</span></span>

- <span data-ttu-id="12fc6-109">Mit erweiterten Vorteilsplänen können Sie einzigartige Vorteilspläne erstellen und verwalten sowie komplexe Vorteilssatztabellen und verschachtelte Stufen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="12fc6-109">Enhanced benefits plans let you create and manage unique benefit plans and support complex benefit rate tables and nested tiers.</span></span> <span data-ttu-id="12fc6-110">Sie können auf einfache Weise Vorteilsprogramme, Bündel und Regeln für die automatische Registrierung erstellen, um die Mitarbeitererfahrung zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="12fc6-110">You can easily create benefit programs, bundles, and auto-enrollment rules for an easier employee experience.</span></span>

- <span data-ttu-id="12fc6-111">Mit Flexguthabenprogrammen können Sie die Altersvorsorge und andere Lebensereignisse anteilig unterstützen.</span><span class="sxs-lookup"><span data-stu-id="12fc6-111">Flex credit programs let you prorate to support retirement and other life events.</span></span>

- <span data-ttu-id="12fc6-112">Umfangreiche Berechtigungsregeln stellen sicher, dass Sie den richtigen Mitarbeitern die richtigen Vorteile zur Verfügung stellen.</span><span class="sxs-lookup"><span data-stu-id="12fc6-112">Extensive eligibility rules ensure you make the right benefits available to the right employees.</span></span>

- <span data-ttu-id="12fc6-113">Die Online-Vorteilsregistrierung bietet Ihren Mitarbeitern eine einfache Erfahrung.</span><span class="sxs-lookup"><span data-stu-id="12fc6-113">Online benefits enrollment provides an easy experience for your employees.</span></span>

- <span data-ttu-id="12fc6-114">Qualifizierte Lebensereignisverarbeitung unterstützt zukünftige Lebensereignisse.</span><span class="sxs-lookup"><span data-stu-id="12fc6-114">Qualified life event processing supports future life events.</span></span>

<span data-ttu-id="12fc6-115">Wenn Sie auf die Demodaten zugreifen möchten, müssen Sie Ihre Sandkastenumgebung erneut bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="12fc6-115">If you would like to access the demo data, you'll need to redeploy your sandbox environment.</span></span>

## <a name="enable-benefits-management"></a><span data-ttu-id="12fc6-116">Vorteilsverwaltung aktivieren</span><span class="sxs-lookup"><span data-stu-id="12fc6-116">Enable Benefits management</span></span>

<span data-ttu-id="12fc6-117">Dieses Thema beschreibt, wie Sie die Vorschaufunktionen in Human Resources aktivieren.</span><span class="sxs-lookup"><span data-stu-id="12fc6-117">This topic describes how to turn on features in Human Resources.</span></span> <span data-ttu-id="12fc6-118">Er zeigt auch, welche vorhandenen Funktionen in Human Resources die Vorteilsverwaltung ersetzt oder deaktiviert, sobald Sie die Vorteilsverwaltung aktivieren.</span><span class="sxs-lookup"><span data-stu-id="12fc6-118">It also tells which existing features in Human Resources that Benefits management replaces or are disabled once you turn on Benefits management.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="12fc6-119">Nachdem Sie die Leistungsverwaltung in einer **Produktions** Umgebung aktiviert haben, können Sie diese nicht mehr deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="12fc6-119">After you enable Benefits management in a **Production** environment, you can't disable it.</span></span> <span data-ttu-id="12fc6-120">Wir empfehlen, das Leistungsmanagement in einer **Sandkasten** Umgebung zu aktivieren und zu testen, bevor Sie es in einer aktivieren **Produktion** Umgebung aktivieren.</span><span class="sxs-lookup"><span data-stu-id="12fc6-120">We recommend enabling and testing Benefits management in a **Sandbox** environment before enabling it in a **Production** environment.</span></span> <span data-ttu-id="12fc6-121">Es gibt erhebliche Unterschiede zwischen der alten Leistungs-Funktionalität und der neuen Leistungsverwaltungs-Funktionalität, die zusätzliche Einstellungen erfordern und vor der Inbetriebnahme getestet werden sollten.</span><span class="sxs-lookup"><span data-stu-id="12fc6-121">There are significant differences between the legacy Benefit functionality and new Benefits management functionality that require additional setup and should be tested prior to being placed into production.</span></span>

- [<span data-ttu-id="12fc6-122">Funktionen verwalten</span><span class="sxs-lookup"><span data-stu-id="12fc6-122">Manage features</span></span>](hr-admin-manage-features.md)

## <a name="configure-employee-information"></a><span data-ttu-id="12fc6-123">Mitarbeiterdaten konfigurieren</span><span class="sxs-lookup"><span data-stu-id="12fc6-123">Configure employee information</span></span>

<span data-ttu-id="12fc6-124">Bevor Sie Mitarbeiter für Leistungen anmelden können, müssen Sie die erforderlichen Informationen angeben.</span><span class="sxs-lookup"><span data-stu-id="12fc6-124">Before you can enroll employees in benefits, you must provide required information.</span></span> <span data-ttu-id="12fc6-125">Sie müssen einen Mitarbeiter bei seinem Eintrittsdatum in einem **Festen Vergütungsplan** erfassen und Sie müssen die **Häufigkeit der Leistungsbezüge** unter **Beschäftigungs-Details** im Formular **Arbeitskraft** auswählen.</span><span class="sxs-lookup"><span data-stu-id="12fc6-125">You must enroll an employee in a **Fixed compensation plan** on their start date, and you must select a **Benefit pay frequency** in **Employment details** on the **Worker** form.</span></span>

<span data-ttu-id="12fc6-126">Wenn Sie einen Mitarbeiter haben, der eine zusätzliche Vergütung wie Provisionen erhält, können Sie einen Betrag **Jahresgehalt für Vorteile** aus dem Mitarbeiterdatensatz hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="12fc6-126">If you have an employee who receives supplemental compensation like commissions, you can add a **Benefits annual salary** amount from the employee record.</span></span> <span data-ttu-id="12fc6-127">Die Personalverwaltung wird den Betrag **Jahresgehalt für Vorteile** verwenden, wenn Deckungssummen festgelegt werden, anstatt eines festen jährlichen Vergütungsbetrags.</span><span class="sxs-lookup"><span data-stu-id="12fc6-127">Human Resources will use the **Benefits annual salary** amount when determining coverage amounts, instead of the fixed compensation annual amount.</span></span> <span data-ttu-id="12fc6-128">Die **Jahresgehalt für Vorteile** müssen ab dem Startdatum des Mitarbeiters oder dem Beginn des Vorteilszeitraums gültig sein, je nachdem, welcher Zeitpunkt der letzte ist.</span><span class="sxs-lookup"><span data-stu-id="12fc6-128">The **Benefits annual salary** must be valid as of the employee’s start date or the beginning of the benefit period, whichever is latest.</span></span> <span data-ttu-id="12fc6-129">Wenn für einen Mitarbeiter sowohl eine feste Vergütung als auch einen Betrag des Jahresgehalts für Vorteile erfasst ist, wird das Jahresgehalt für Vorteile verwendet, um die Deckungssummen zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="12fc6-129">If both a fixed compensation and benefits annual salary amount is recorded for an employee, the benefits annual salary will be used in determining coverage amounts.</span></span>

<span data-ttu-id="12fc6-130">Wenn Sie einen Leistungsplan erstellen, der Sätze verwendet, die auf Geschlecht oder Alter basieren, müssen Sie ein Geburtsdatum und ein Geschlecht eingeben, damit der Mitarbeiter die Leistungskosten berechnen kann.</span><span class="sxs-lookup"><span data-stu-id="12fc6-130">When you create a benefit plan that uses rates that are based on gender or age, you must enter a birth date and gender for the employee to calculate the benefit cost.</span></span>

## <a name="configure-benefits-management"></a><span data-ttu-id="12fc6-131">Vorteilsverwaltung konfigurieren</span><span class="sxs-lookup"><span data-stu-id="12fc6-131">Configure Benefits management</span></span>

<span data-ttu-id="12fc6-132">Bevor Sie Vorteilspläne für Ihre Mitarbeiter erstellen können, müssen Sie Optionen für die Pläne konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="12fc6-132">Before you can create benefit plans for your employees, you need to configure options for the plans.</span></span>

- [<span data-ttu-id="12fc6-133">Vorteilsverwaltungsparameter festlegen</span><span class="sxs-lookup"><span data-stu-id="12fc6-133">Set Benefits management parameters</span></span>](hr-benefits-setup-parameters.md)
- [<span data-ttu-id="12fc6-134">Berechtigungsregeln und -optionen konfigurieren</span><span class="sxs-lookup"><span data-stu-id="12fc6-134">Configure eligibility rules and options</span></span>](hr-benefits-setup-eligibility-rules.md)
- [<span data-ttu-id="12fc6-135">Berechtigungsoptionen für persönliche Kontakte konfigurieren</span><span class="sxs-lookup"><span data-stu-id="12fc6-135">Configure personal contact eligibility options</span></span>](hr-benefits-setup-contact-eligibility-options.md)
- [<span data-ttu-id="12fc6-136">Abdeckungsoptionen erstellen</span><span class="sxs-lookup"><span data-stu-id="12fc6-136">Create coverage options</span></span>](hr-benefits-setup-coverage-options.md)
- [<span data-ttu-id="12fc6-137">Zahlungshäufigkeiten einrichten</span><span class="sxs-lookup"><span data-stu-id="12fc6-137">Set up payment frequencies</span></span>](hr-benefits-setup-payment-frequencies.md)
- [<span data-ttu-id="12fc6-138">Lebensereignistypen konfigurieren</span><span class="sxs-lookup"><span data-stu-id="12fc6-138">Configure life event types</span></span>](hr-benefits-setup-life-event-types.md)
- [<span data-ttu-id="12fc6-139">Plantypen erstellen</span><span class="sxs-lookup"><span data-stu-id="12fc6-139">Create plan types</span></span>](hr-benefits-setup-plan-types.md)
- [<span data-ttu-id="12fc6-140">Ursachencodes einrichten</span><span class="sxs-lookup"><span data-stu-id="12fc6-140">Set up reason codes</span></span>](hr-benefits-setup-reason-codes.md)
- [<span data-ttu-id="12fc6-141">Schichtcodes einrichten</span><span class="sxs-lookup"><span data-stu-id="12fc6-141">Set up tier codes</span></span>](hr-benefits-setup-tier-codes.md)
- [<span data-ttu-id="12fc6-142">Sätze konfigurieren</span><span class="sxs-lookup"><span data-stu-id="12fc6-142">Configure rates</span></span>](hr-benefits-setup-rates.md)
- [<span data-ttu-id="12fc6-143">Abzüge konfigurieren</span><span class="sxs-lookup"><span data-stu-id="12fc6-143">Configure deductions</span></span>](hr-benefits-setup-deductions.md)
- [<span data-ttu-id="12fc6-144">Wartezeiten konfigurieren</span><span class="sxs-lookup"><span data-stu-id="12fc6-144">Configure waiting days</span></span>](hr-benefits-setup-waiting-days.md)
- [<span data-ttu-id="12fc6-145">Wartezeiträume konfigurieren</span><span class="sxs-lookup"><span data-stu-id="12fc6-145">Configure waiting periods</span></span>](hr-benefits-setup-waiting-periods.md)
- [<span data-ttu-id="12fc6-146">Rundungsregeln einrichten</span><span class="sxs-lookup"><span data-stu-id="12fc6-146">Set up rounding rules</span></span>](hr-benefits-setup-rounding-rules.md)
- [<span data-ttu-id="12fc6-147">Mitarbeiterkategorien erstellen</span><span class="sxs-lookup"><span data-stu-id="12fc6-147">Create employment categories</span></span>](hr-benefits-setup-employment-categories.md)
- [<span data-ttu-id="12fc6-148">Beschäftigungstypen einrichten</span><span class="sxs-lookup"><span data-stu-id="12fc6-148">Set up employment types</span></span>](hr-benefits-setup-employment-types.md)
- [<span data-ttu-id="12fc6-149">Mitarbeiter-Self-Service konfigurieren</span><span class="sxs-lookup"><span data-stu-id="12fc6-149">Configure employee self service</span></span>](hr-benefits-setup-employee-self-service.md)

## <a name="create-benefit-plans"></a><span data-ttu-id="12fc6-150">Vergütungspläne erstellen</span><span class="sxs-lookup"><span data-stu-id="12fc6-150">Create benefit plans</span></span>

<span data-ttu-id="12fc6-151">In diesen Artikeln wird gezeigt, wie Sie Vorteilspläne erstellen, einschließlich Bündeln und Flexguthabenprogrammen.</span><span class="sxs-lookup"><span data-stu-id="12fc6-151">These articles show how to create benefit plans, including bundles and flex credit programs.</span></span>

- [<span data-ttu-id="12fc6-152">Vergütungspläne einrichten</span><span class="sxs-lookup"><span data-stu-id="12fc6-152">Set up benefit plans</span></span>](hr-benefits-plans-setup.md)
- [<span data-ttu-id="12fc6-153">Programme für flexible Kredite einrichten</span><span class="sxs-lookup"><span data-stu-id="12fc6-153">Set up flex credit programs</span></span>](hr-benefits-plans-flex-credit-programs.md)

## <a name="process-benefit-plans"></a><span data-ttu-id="12fc6-154">Vergütungspläne verarbeiten</span><span class="sxs-lookup"><span data-stu-id="12fc6-154">Process benefit plans</span></span>

<span data-ttu-id="12fc6-155">Sie müssen einige Ihrer Änderungen verarbeiten, um sie zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="12fc6-155">You need to process some of your changes to make them active.</span></span>

- [<span data-ttu-id="12fc6-156">Vergütungsberechtigung verarbeiten</span><span class="sxs-lookup"><span data-stu-id="12fc6-156">Process enrollment eligibility</span></span>](hr-benefits-process-enrollment-eligibility.md)
- [<span data-ttu-id="12fc6-157">Lebensereignisse verarbeiten</span><span class="sxs-lookup"><span data-stu-id="12fc6-157">Process life events</span></span>](hr-benefits-process-life-events.md)
- [<span data-ttu-id="12fc6-158">Änderungen von Lebensereignissen verarbeiten</span><span class="sxs-lookup"><span data-stu-id="12fc6-158">Process life event changes</span></span>](hr-benefits-process-life-event-changes.md)
- [<span data-ttu-id="12fc6-159">Lebensereignisberechtigung verarbeiten</span><span class="sxs-lookup"><span data-stu-id="12fc6-159">Process life event eligibility</span></span>](hr-benefits-process-life-event-eligibility.md)
- [<span data-ttu-id="12fc6-160">Satzänderungen verarbeiten</span><span class="sxs-lookup"><span data-stu-id="12fc6-160">Process rate changes</span></span>](hr-benefits-process-rate-changes.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]