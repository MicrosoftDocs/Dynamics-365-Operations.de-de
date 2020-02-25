---
title: Talent mit Power Apps und Power Automate erweitern
description: Dieser Artikel beschreibt einige Beispiele für Erweiterungsszenarien für Microsoft Dynamics 365 Talent - Attract, die Microsoft Power Apps und Microsoft Power Automate verwenden.
author: negudava
manager: Annbe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: Dynamics 365 Talent;PowerApps;Flow;Common Data Service
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent;Core;Experience Apps
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 1051fa4db16bb94cc9d60a91fc3637d7e5305cc2
ms.sourcegitcommit: 13c4a6f98ccce243d6befde90992aefcf562bdab
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029910"
---
# <a name="extend-talent-with-power-apps-and-power-automate"></a><span data-ttu-id="34ffc-103">Talent mit Power Apps und Power Automate erweitern</span><span class="sxs-lookup"><span data-stu-id="34ffc-103">Extend Talent with Power Apps and Power Automate</span></span>

<span data-ttu-id="34ffc-104">Dieser Artikel beschreibt einige Beispiele für Erweiterungsszenarien für Microsoft Dynamics 365 Talent: Attract, die Microsoft Power Apps und Microsoft Power Automate verwenden.</span><span class="sxs-lookup"><span data-stu-id="34ffc-104">This article describes some examples of extensibility scenarios for Microsoft Dynamics 365 Talent: Attract that use Microsoft Power Apps and Microsoft Power Automate.</span></span> <span data-ttu-id="34ffc-105">Sie können das Lösungspaket importieren, das jedem Beispiel in der Power Apps-Umgebung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="34ffc-105">You can import the solution package that is associated with each example into your Power Apps environment.</span></span> <span data-ttu-id="34ffc-106">Sie können entweder die Pakete als Anleitung oder als Startpunkte zu den Werkzeugszenarien verwenden, die der Organisation zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="34ffc-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="34ffc-107">Wenn Sie die Vorlagen und Apps verwenden möchten, die in diesem Artikel als „wie vorliegend“ beschrieben sind, müssen Sie diese unbedingt testen, um sicherzustellen, dass sie alle Szenarien beinhalten, die für Ihre Implementierung bestimmt sind.</span><span class="sxs-lookup"><span data-stu-id="34ffc-107">If you want to use the templates and app that are described in this article "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>


## <a name="prerequisites"></a><span data-ttu-id="34ffc-108">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="34ffc-108">Prerequisites</span></span>

- <span data-ttu-id="34ffc-109">Um Pakete zu importieren, müssen Benutzer die Berechtigung **Umgebungs-Hersteller** haben.</span><span class="sxs-lookup"><span data-stu-id="34ffc-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="34ffc-110">Um Apps zu exportierenden oder zu importieren, müssen Benutzer eine Lizenz für Power Apps Plan 2 oder eine Testlizenz für Power Apps-Plan 2 haben.</span><span class="sxs-lookup"><span data-stu-id="34ffc-110">To export or import apps, users must have a Power Apps Plan 2 license or a Power Apps Plan 2 trial license.</span></span>

## <a name="power-automate--form-connect"></a><span data-ttu-id="34ffc-111">Power Automate - Formular Verbinden</span><span class="sxs-lookup"><span data-stu-id="34ffc-111">Power Automate – Form Connect</span></span>

<span data-ttu-id="34ffc-112">Die Vorlage **Power Automate - Formular Verbinden** kann verwendet werden, um Daten aus Microsoft Forms zu lesen und in einer Common Data Service Einheit zu speichern.</span><span class="sxs-lookup"><span data-stu-id="34ffc-112">The **Power Automate – Form Connect** template can be used to read data from Microsoft Forms and store it in a Common Data Service entity.</span></span>

<span data-ttu-id="34ffc-113">Diese Vorlage kann auch erweitert werden, sodass sie für andere Szenarien verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="34ffc-113">This template can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="34ffc-114">Nachfolgend finden Sie einige Beispiele:</span><span class="sxs-lookup"><span data-stu-id="34ffc-114">Here are some examples:</span></span>

- <span data-ttu-id="34ffc-115">Kandidatenbewertungen aufzeichnen.</span><span class="sxs-lookup"><span data-stu-id="34ffc-115">Capture candidate assessments.</span></span>
- <span data-ttu-id="34ffc-116">Zeichnen Sie Ergebnisse aus Kursfragebögen auf.</span><span class="sxs-lookup"><span data-stu-id="34ffc-116">Capture results from course questionnaires.</span></span>
- <span data-ttu-id="34ffc-117">Kompilieren Sie eine Bibliothek von Gesprächsfragen für die Personalverwaltungs (HR)-Administratoren.</span><span class="sxs-lookup"><span data-stu-id="34ffc-117">Compile a library of interview questions for Human resources (HR) administrators.</span></span>
- <span data-ttu-id="34ffc-118">Zeichnen Sie die Bewertung des Kandidaten aus dem Gesprächsprozess auf</span><span class="sxs-lookup"><span data-stu-id="34ffc-118">Capture a candidate's evaluation of the interview process</span></span>

<span data-ttu-id="34ffc-119">In Microsoft Dynamics 365: Attract können Sie Formulare im Kandidatenportal nutzen, bei dem Kandidaten die Details selbst eingeben.</span><span class="sxs-lookup"><span data-stu-id="34ffc-119">In Microsoft Dynamics 365: Attract, you can use forms in the candidate portal, where candidates fill in details.</span></span> <span data-ttu-id="34ffc-120">Sie können Formulare auch als Aktivitäten in die Stellenvorlage einbetten.</span><span class="sxs-lookup"><span data-stu-id="34ffc-120">You can also embed forms as activities in a job template.</span></span>

<span data-ttu-id="34ffc-121">Wenn ein Kandidat ein Formular abschickt, erfasst Microsoft Power Automate die Formularabgabe, liest die Daten und speichert sie in der Entität Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="34ffc-121">When a candidate submits a form, Microsoft Power Automate captures the form submission, reads the data, and stores it in the Common Data Service entity.</span></span>

<span data-ttu-id="34ffc-122">Um die **Power Automate - Formular verbinden** Vorlage und benutzerdefinierte Entitätsstruktur herunterzuladen, gehen Sie zu [Power Automate - Formular verbinden](https://go.microsoft.com/fwlink/?linkid=2081988) im Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="34ffc-122">To download the **Power Automate – Form Connect** template and Custom Entity Structure, go to [Power Automate – Form Connect](https://go.microsoft.com/fwlink/?linkid=2081988) on the Microsoft Download Center.</span></span>

## <a name="power-automate--sharepoint-integration"></a><span data-ttu-id="34ffc-123">Power Automate - SharePoint Integration</span><span class="sxs-lookup"><span data-stu-id="34ffc-123">Power Automate – SharePoint Integration</span></span>

<span data-ttu-id="34ffc-124">Die Vorlage **Power Automate - SharePoint Integration** kann verwendet werden, um Daten aus einer Microsoft SharePoint-Liste zu lesen, die Liste mit Feldwerten für jede Common Data Service-Einheit zu vergleichen und die Ergebnisse des Vergleichs als Benachrichtigungs-E-Mail zu senden.</span><span class="sxs-lookup"><span data-stu-id="34ffc-124">The **Power Automate – SharePoint Integration** template can be used to read data from a Microsoft SharePoint list, compare the list with field values for any Common Data Service entity, and send the results of the comparison as a notification email.</span></span> 

<span data-ttu-id="34ffc-125">Eine Organisation hat möglicherweise eine Reihe von Fähigkeiten, die sie dringend benötigt.</span><span class="sxs-lookup"><span data-stu-id="34ffc-125">An organization might have a set of skills that it urgently requires.</span></span> <span data-ttu-id="34ffc-126">Diese Qualifikationen können in SharePoint als Liste SharePoint gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="34ffc-126">These skills can be stored in SharePoint as a SharePoint list.</span></span> <span data-ttu-id="34ffc-127">Wenn sich ein Kandidat für eine Stelle bewirbt, die Qualifikationen verlangt, die aufgelistet sind und wenn es eine erhebliche Übereinstimmung zwischen den Fähigkeiten des Kandidaten und den Qualifikationen gibt, die in SharePoint gespeichert sind, wird eine  Benachrichtigungs-E-Mail übermittelt.</span><span class="sxs-lookup"><span data-stu-id="34ffc-127">When a candidate applies for any job that a set of required skills is listed for, if there is a significant match between the candidate's skill and the skills that are stored in SharePoint, a notification email is sent.</span></span> <span data-ttu-id="34ffc-128">Auf diese Weise werden Positionen, die dringend erforderlich sind, schneller besetzt, da die Benachrichtigungen den Personalbeschaffern helfen, Kandidaten aus der gesamten Organisation zu finden.</span><span class="sxs-lookup"><span data-stu-id="34ffc-128">This helps fill positions that are urgently required faster, because the notifications help recruiters cross-hire candidates throughout the organization.</span></span>

<span data-ttu-id="34ffc-129">Diese Vorlage kann auch erweitert werden, sodass sie für ein beliebiges Szenario verwendet werden kann, das die SharePoint Integration betrifft.</span><span class="sxs-lookup"><span data-stu-id="34ffc-129">This template can be extended so that it can be used for any scenario that involves SharePoint integration.</span></span>

<span data-ttu-id="34ffc-130">Um die Vorlage **Power Automate - SharePoint Integration** herunterzuladen, gehen Sie zu [Power Automate - SharePoint Integration](https://go.microsoft.com/fwlink/?linkid=2082109) im Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="34ffc-130">To download the **Power Automate – SharePoint Integration** template, go to [Power Automate – SharePoint Integration](https://go.microsoft.com/fwlink/?linkid=2082109) on the Microsoft Download Center.</span></span>

## <a name="referral-app"></a><span data-ttu-id="34ffc-131">Bezugs-App</span><span class="sxs-lookup"><span data-stu-id="34ffc-131">Referral App</span></span>

<span data-ttu-id="34ffc-132">Sie können die Empfehlungs-App verwenden, um Kandidaten einer freigegebene Talentschmiede hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="34ffc-132">You can use the Referral App to add candidates to a shared talent pool.</span></span> <span data-ttu-id="34ffc-133">Der Verweiser kann **Vorname**, **Nachname**, **E-Mail** und **LinkedIn-URL** eingeben, wenn er den Kandidaten übermittelt.</span><span class="sxs-lookup"><span data-stu-id="34ffc-133">The referrer can enter **Firstname**, **Lastname**, **Email**, and **LinkedIn URL** when submitting a candidate.</span></span> <span data-ttu-id="34ffc-134">Die Kandidatenquellenmetadaten werden dann mit den Informationen des Empfehlers ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="34ffc-134">The candidate source metadata is then populated with the referrer’s information.</span></span>

<span data-ttu-id="34ffc-135">Sie können dieser App im Mitarbeiter-Self-Service für das Übermitteln von Empfehlungen einbetten oder Sie können sie als Verknüpfung im Unternehmensportal und als eigenständige App verwenden.</span><span class="sxs-lookup"><span data-stu-id="34ffc-135">You can embed this app in Employee self service for submitting referrals, or you can use it as a hyperlink in the corporate portal and run it as a stand-alone app.</span></span>

<span data-ttu-id="34ffc-136">Um die **Empfehlungs-App** herunterzuladen, gehen Sie zur [Dynamics 365 Talent Erweiterbarkeitslösung: Empfehlungs-App](https://www.microsoft.com/download/details.aspx?id=58497) im  Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="34ffc-136">To download **Referral App**, go to [Dynamics 365 Talent extensibility solution: Referral App](https://www.microsoft.com/download/details.aspx?id=58497) on the Microsoft Download Center.</span></span> <span data-ttu-id="34ffc-137">Sie können diese App importieren und anpassen, um weitere Funktionen hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="34ffc-137">You can import this app and customize it to add additional functionality.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="34ffc-138">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="34ffc-138">Additional resources</span></span>

[<span data-ttu-id="34ffc-139">Das Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="34ffc-139">The Microsoft Power Platform</span></span>](https://docs.microsoft.com/power-platform/admin/admin-documentation)</br>
[<span data-ttu-id="34ffc-140">Migrieren der App zwischen Mandanten und Umgebung</span><span class="sxs-lookup"><span data-stu-id="34ffc-140">Migrate app between tenants and environments</span></span>](https://docs.microsoft.com/power-platform/admin/environment-and-tenant-migration)
