---
title: Vorteilsverwaltung – Übersicht
description: Übersicht über die Vorschaufunktion für die Vorteilsverwaltung in Dynamics 365 Human Resources. Bieten Sie Ihren Mitarbeitern erweiterte Vorteilsoptionen mit einer benutzerfreundlichen Online-Erfahrung.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
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
ms.openlocfilehash: 4157cb1f83d686d435f3d04e47c578df455376c9
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429260"
---
# <a name="benefits-management-overview"></a><span data-ttu-id="a06da-104">Vorteilsverwaltung – Übersicht</span><span class="sxs-lookup"><span data-stu-id="a06da-104">Benefits management overview</span></span>

<span data-ttu-id="a06da-105">Um wettbewerbsfähig zu bleiben, müssen Sie zahlreiche Vorteile bieten, um die besten Mitarbeiter anzuwerben und zu halten.</span><span class="sxs-lookup"><span data-stu-id="a06da-105">To remain competitive, you must offer a rich set of benefits to attract and retain your best employees.</span></span> <span data-ttu-id="a06da-106">Zusätzlich zu den Standardleistungen wie Kranken‑ und Zahnzusatzversicherung möchten Sie möglicherweise auch erweiterte Dienstleistungen wie Adoptionsunterstützung, Freizeitprogramme und Aufwandsentschädigungen anbieten.</span><span class="sxs-lookup"><span data-stu-id="a06da-106">In addition to standard benefits like medical and dental coverage, you might also want to offer expanded services like adoption assistance, recreation programs, and clothing allowances.</span></span> <span data-ttu-id="a06da-107">Die Leistungsverwaltung in Microsoft Dynamics 365 Human Resources bietet Ihnen eine flexible Lösung, die eine Vielzahl von Vorteilsoptionen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a06da-107">Benefits management in Microsoft Dynamics 365 Human Resources provides you with a flexible solution that supports a wide variety of benefit options.</span></span> <span data-ttu-id="a06da-108">Human Resources umfasst auch eine benutzerfreundliche Mitarbeitererfahrung, die Ihre Angebote vorstellt.</span><span class="sxs-lookup"><span data-stu-id="a06da-108">Human Resources also includes an easy-to-use employee experience that showcases your offerings.</span></span>

- <span data-ttu-id="a06da-109">Mit erweiterten Vorteilsplänen können Sie einzigartige Vorteilspläne erstellen und verwalten sowie komplexe Vorteilssatztabellen und verschachtelte Stufen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="a06da-109">Enhanced benefits plans let you create and manage unique benefit plans and support complex benefit rate tables and nested tiers.</span></span> <span data-ttu-id="a06da-110">Sie können auf einfache Weise Vorteilsprogramme, Bündel und Regeln für die automatische Registrierung erstellen, um die Mitarbeitererfahrung zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="a06da-110">You can easily create benefit programs, bundles, and auto-enrollment rules for an easier employee experience.</span></span>

- <span data-ttu-id="a06da-111">Mit Flexguthabenprogrammen können Sie die Altersvorsorge und andere Lebensereignisse anteilig unterstützen.</span><span class="sxs-lookup"><span data-stu-id="a06da-111">Flex credit programs let you prorate to support retirement and other life events.</span></span>

- <span data-ttu-id="a06da-112">Umfangreiche Berechtigungsregeln stellen sicher, dass Sie den richtigen Mitarbeitern die richtigen Vorteile zur Verfügung stellen.</span><span class="sxs-lookup"><span data-stu-id="a06da-112">Extensive eligibility rules ensure you make the right benefits available to the right employees.</span></span>

- <span data-ttu-id="a06da-113">Die Online-Vorteilsregistrierung bietet Ihren Mitarbeitern eine einfache Erfahrung.</span><span class="sxs-lookup"><span data-stu-id="a06da-113">Online benefits enrollment provides an easy experience for your employees.</span></span>

- <span data-ttu-id="a06da-114">Qualifizierte Lebensereignisverarbeitung unterstützt zukünftige Lebensereignisse.</span><span class="sxs-lookup"><span data-stu-id="a06da-114">Qualified life event processing supports future life events.</span></span>

<span data-ttu-id="a06da-115">Wenn Sie auf die Demodaten zugreifen möchten, müssen Sie Ihre Sandkastenumgebung erneut bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="a06da-115">If you would like to access the demo data, you'll need to redeploy your sandbox environment.</span></span>

## <a name="benefits-management-known-issues"></a><span data-ttu-id="a06da-116">Bekannte Probleme bei der Vorteilsverwaltung</span><span class="sxs-lookup"><span data-stu-id="a06da-116">Benefits management known issues</span></span>

### <a name="flex-credit-programs"></a><span data-ttu-id="a06da-117">Flexible Gutschriftprogramme</span><span class="sxs-lookup"><span data-stu-id="a06da-117">Flex credit programs</span></span>

<span data-ttu-id="a06da-118">Der für ein flexibles Kreditprogramm definierte Gesamtkreditwert wird im nicht im Formular **Vorsorgepläne für Arbeitnehmer** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a06da-118">The total credit value defined for a flex credit program doesn't display in the **Worker benefit plans** form.</span></span> <span data-ttu-id="a06da-119">Auch wenn Sie ein flexibles Kreditprogramm so einstellen, dass es eine Prorationsregel von **Keiner** hat, erhalten Sie einen Fehler im Formular **Vorsorgeplan für Arbeitnehmer** bei der Auswahl und Bestätigung von Plänen.</span><span class="sxs-lookup"><span data-stu-id="a06da-119">Also, if you set a flex credit program to have a proration rule of **None**, you get an error in the **Worker benefit plan** form when selecting and confirming plans.</span></span>

## <a name="enable-benefits-management"></a><span data-ttu-id="a06da-120">Vorteilsverwaltung aktivieren</span><span class="sxs-lookup"><span data-stu-id="a06da-120">Enable Benefits management</span></span>

<span data-ttu-id="a06da-121">Dieser Artikel beschreibt, wie Sie die Vorschaufunktionen in Human Resources aktivieren.</span><span class="sxs-lookup"><span data-stu-id="a06da-121">This article describes how to turn on features in Human Resources.</span></span> <span data-ttu-id="a06da-122">Er zeigt auch, welche vorhandenen Funktionen in Human Resources die Vorteilsverwaltung ersetzt oder deaktiviert, sobald Sie die Vorteilsverwaltung aktivieren.</span><span class="sxs-lookup"><span data-stu-id="a06da-122">It also tells which existing features in Human Resources that Benefits management replaces or are disabled once you turn on Benefits management.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a06da-123">Nachdem Sie die Leistungsverwaltung in einer **Produktions** Umgebung aktiviert haben, können Sie diese nicht mehr deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="a06da-123">After you enable Benefits management in a **Production** environment, you can't disable it.</span></span> <span data-ttu-id="a06da-124">Wir empfehlen, das Leistungsmanagement in einer **Sandkasten** Umgebung zu aktivieren und zu testen, bevor Sie es in einer aktivieren **Produktion** Umgebung aktivieren.</span><span class="sxs-lookup"><span data-stu-id="a06da-124">We recommend enabling and testing Benefits management in a **Sandbox** environment before enabling it in a **Production** environment.</span></span> <span data-ttu-id="a06da-125">Es gibt erhebliche Unterschiede zwischen der alten Leistungs-Funktionalität und der neuen Leistungsverwaltungs-Funktionalität, die zusätzliche Einstellungen erfordern und vor der Inbetriebnahme getestet werden sollten.</span><span class="sxs-lookup"><span data-stu-id="a06da-125">There are significant differences between the legacy Benefit functionality and new Benefits management functionality that require additional setup and should be tested prior to being placed into production.</span></span>

- [<span data-ttu-id="a06da-126">Funktionen verwalten</span><span class="sxs-lookup"><span data-stu-id="a06da-126">Manage features</span></span>](hr-admin-manage-features.md)

## <a name="configure-employee-information"></a><span data-ttu-id="a06da-127">Mitarbeiterdaten konfigurieren</span><span class="sxs-lookup"><span data-stu-id="a06da-127">Configure employee information</span></span>

<span data-ttu-id="a06da-128">Bevor Sie Mitarbeiter für Leistungen anmelden können, müssen Sie die erforderlichen Informationen angeben.</span><span class="sxs-lookup"><span data-stu-id="a06da-128">Before you can enroll employees in benefits, you must provide required information.</span></span> <span data-ttu-id="a06da-129">Sie müssen einen Mitarbeiter bei seinem Eintrittsdatum in einem **Festen Vergütungsplan** erfassen und Sie müssen die **Häufigkeit der Leistungsbezüge** unter **Beschäftigungs-Details** im Formular **Arbeitskraft** auswählen.</span><span class="sxs-lookup"><span data-stu-id="a06da-129">You must enroll an employee in a **Fixed compensation plan** on their start date, and you must select a **Benefit pay frequency** in **Employment details** on the **Worker** form.</span></span>

<span data-ttu-id="a06da-130">Wenn Sie einen Leistungsplan erstellen, der Sätze verwendet, die auf Geschlecht oder Alter basieren, müssen Sie ein Geburtsdatum und ein Geschlecht eingeben, damit der Mitarbeiter die Leistungskosten berechnen kann.</span><span class="sxs-lookup"><span data-stu-id="a06da-130">When you create a benefit plan that uses rates that are based on gender or age, you must enter a birth date and gender for the employee to calculate the benefit cost.</span></span>

## <a name="configure-benefits-management"></a><span data-ttu-id="a06da-131">Vorteilsverwaltung konfigurieren</span><span class="sxs-lookup"><span data-stu-id="a06da-131">Configure Benefits management</span></span>

<span data-ttu-id="a06da-132">Bevor Sie Vorteilspläne für Ihre Mitarbeiter erstellen können, müssen Sie Optionen für die Pläne konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="a06da-132">Before you can create benefit plans for your employees, you need to configure options for the plans.</span></span>

- [<span data-ttu-id="a06da-133">Vorteilsverwaltungsparameter festlegen</span><span class="sxs-lookup"><span data-stu-id="a06da-133">Set Benefits management parameters</span></span>](hr-benefits-setup-parameters.md)
- [<span data-ttu-id="a06da-134">Berechtigungsregeln und -optionen konfigurieren</span><span class="sxs-lookup"><span data-stu-id="a06da-134">Configure eligibility rules and options</span></span>](hr-benefits-setup-eligibility-rules.md)
- [<span data-ttu-id="a06da-135">Berechtigungsoptionen für persönliche Kontakte konfigurieren</span><span class="sxs-lookup"><span data-stu-id="a06da-135">Configure personal contact eligibility options</span></span>](hr-benefits-setup-contact-eligibility-options.md)
- [<span data-ttu-id="a06da-136">Abdeckungsoptionen erstellen</span><span class="sxs-lookup"><span data-stu-id="a06da-136">Create coverage options</span></span>](hr-benefits-setup-coverage-options.md)
- [<span data-ttu-id="a06da-137">Zahlungshäufigkeiten einrichten</span><span class="sxs-lookup"><span data-stu-id="a06da-137">Set up payment frequencies</span></span>](hr-benefits-setup-payment-frequencies.md)
- [<span data-ttu-id="a06da-138">Lebensereignistypen konfigurieren</span><span class="sxs-lookup"><span data-stu-id="a06da-138">Configure life event types</span></span>](hr-benefits-setup-life-event-types.md)
- [<span data-ttu-id="a06da-139">Plantypen erstellen</span><span class="sxs-lookup"><span data-stu-id="a06da-139">Create plan types</span></span>](hr-benefits-setup-plan-types.md)
- [<span data-ttu-id="a06da-140">Ursachencodes einrichten</span><span class="sxs-lookup"><span data-stu-id="a06da-140">Set up reason codes</span></span>](hr-benefits-setup-reason-codes.md)
- [<span data-ttu-id="a06da-141">Schichtcodes einrichten</span><span class="sxs-lookup"><span data-stu-id="a06da-141">Set up tier codes</span></span>](hr-benefits-setup-tier-codes.md)
- [<span data-ttu-id="a06da-142">Sätze konfigurieren</span><span class="sxs-lookup"><span data-stu-id="a06da-142">Configure rates</span></span>](hr-benefits-setup-rates.md)
- [<span data-ttu-id="a06da-143">Abzüge konfigurieren</span><span class="sxs-lookup"><span data-stu-id="a06da-143">Configure deductions</span></span>](hr-benefits-setup-deductions.md)
- [<span data-ttu-id="a06da-144">Wartezeiten konfigurieren</span><span class="sxs-lookup"><span data-stu-id="a06da-144">Configure waiting days</span></span>](hr-benefits-setup-waiting-days.md)
- [<span data-ttu-id="a06da-145">Wartezeiträume konfigurieren</span><span class="sxs-lookup"><span data-stu-id="a06da-145">Configure waiting periods</span></span>](hr-benefits-setup-waiting-periods.md)
- [<span data-ttu-id="a06da-146">Rundungsregeln einrichten</span><span class="sxs-lookup"><span data-stu-id="a06da-146">Set up rounding rules</span></span>](hr-benefits-setup-rounding-rules.md)
- [<span data-ttu-id="a06da-147">Mitarbeiterkategorien erstellen</span><span class="sxs-lookup"><span data-stu-id="a06da-147">Create employment categories</span></span>](hr-benefits-setup-employment-categories.md)
- [<span data-ttu-id="a06da-148">Beschäftigungstypen einrichten</span><span class="sxs-lookup"><span data-stu-id="a06da-148">Set up employment types</span></span>](hr-benefits-setup-employment-types.md)
- [<span data-ttu-id="a06da-149">Mitarbeiter-Self-Service konfigurieren</span><span class="sxs-lookup"><span data-stu-id="a06da-149">Configure employee self service</span></span>](hr-benefits-setup-employee-self-service.md)

## <a name="create-benefit-plans"></a><span data-ttu-id="a06da-150">Vergütungspläne erstellen</span><span class="sxs-lookup"><span data-stu-id="a06da-150">Create benefit plans</span></span>

<span data-ttu-id="a06da-151">In diesen Artikeln wird gezeigt, wie Sie Vorteilspläne erstellen, einschließlich Bündeln und Flexguthabenprogrammen.</span><span class="sxs-lookup"><span data-stu-id="a06da-151">These articles show how to create benefit plans, including bundles and flex credit programs.</span></span>

- [<span data-ttu-id="a06da-152">Vergütungspläne einrichten</span><span class="sxs-lookup"><span data-stu-id="a06da-152">Set up benefit plans</span></span>](hr-benefits-plans-setup.md)
- [<span data-ttu-id="a06da-153">Programme für flexible Kredite einrichten</span><span class="sxs-lookup"><span data-stu-id="a06da-153">Set up flex credit programs</span></span>](hr-benefits-plans-flex-credit-programs.md)

## <a name="process-benefit-plans"></a><span data-ttu-id="a06da-154">Vergütungspläne verarbeiten</span><span class="sxs-lookup"><span data-stu-id="a06da-154">Process benefit plans</span></span>

<span data-ttu-id="a06da-155">Sie müssen einige Ihrer Änderungen verarbeiten, um sie zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="a06da-155">You need to process some of your changes to make them active.</span></span>

- [<span data-ttu-id="a06da-156">Vergütungsberechtigung verarbeiten</span><span class="sxs-lookup"><span data-stu-id="a06da-156">Process enrollment eligibility</span></span>](hr-benefits-process-enrollment-eligibility.md)
- [<span data-ttu-id="a06da-157">Lebensereignisse verarbeiten</span><span class="sxs-lookup"><span data-stu-id="a06da-157">Process life events</span></span>](hr-benefits-process-life-events.md)
- [<span data-ttu-id="a06da-158">Änderungen von Lebensereignissen verarbeiten</span><span class="sxs-lookup"><span data-stu-id="a06da-158">Process life event changes</span></span>](hr-benefits-process-life-event-changes.md)
- [<span data-ttu-id="a06da-159">Lebensereignisberechtigung verarbeiten</span><span class="sxs-lookup"><span data-stu-id="a06da-159">Process life event eligibility</span></span>](hr-benefits-process-life-event-eligibility.md)
- [<span data-ttu-id="a06da-160">Satzänderungen verarbeiten</span><span class="sxs-lookup"><span data-stu-id="a06da-160">Process rate changes</span></span>](hr-benefits-process-rate-changes.md)

