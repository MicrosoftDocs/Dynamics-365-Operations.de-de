---
title: Neuerungen oder Änderungen in Dynamics 365 Talent (7. Januar 2020)
description: Dieser Artikel beschreibt Funktionen, die in Microsoft Dynamics 365 Talent neu oder geändert wurden.
author: Darinkramer
manager: AnnBe
ms.date: 01/07/2020
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
ms.search.validFrom: 2020-01-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e227c614fdbfe6f3dd410f1a533c593979abf1ec
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461288"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-7-2020"></a><span data-ttu-id="c7530-103">Neuerungen oder Änderungen in Dynamics 365 Talent (7. Januar 2020)</span><span class="sxs-lookup"><span data-stu-id="c7530-103">What's new or changed in Dynamics 365 Talent (January 7, 2020)</span></span>

<span data-ttu-id="c7530-104">Dieser Artikel beschreibt Funktionen, die entweder neu oder geändert in Dynamics 365 Talent sind.</span><span class="sxs-lookup"><span data-stu-id="c7530-104">This article describes features that are either new or changed in Dynamics 365 Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="c7530-105">Änderungen in Attract</span><span class="sxs-lookup"><span data-stu-id="c7530-105">Changes in Attract</span></span>

<span data-ttu-id="c7530-106">Diese Version enthält kleinere Fehlerkorrekturen für Dynamics 365 Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="c7530-106">This release includes minor bug fixes for Dynamics 365 Talent: Attract.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="c7530-107">Änderungen in Onboard</span><span class="sxs-lookup"><span data-stu-id="c7530-107">Changes in Onboard</span></span>

<span data-ttu-id="c7530-108">Diese Version enthält kleinere Fehlerkorrekturen für Dynamics 365 Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="c7530-108">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="c7530-109">Core HR-Änderungen</span><span class="sxs-lookup"><span data-stu-id="c7530-109">Changes in Core HR</span></span>

<span data-ttu-id="c7530-110">Die in diesem Abschnitt beschriebenen Änderungen gelten für Buildnummer 8.1.2697.</span><span class="sxs-lookup"><span data-stu-id="c7530-110">Changes described in this section apply to build number 8.1.2697.</span></span> <span data-ttu-id="c7530-111">Die Zahlen in Klammern in einigen Überschriften beziehen sich auf Supportnummern in Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="c7530-111">The numbers in parentheses in some headings refer to support numbers in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

 
### <a name="cant-delete-workers-that-dont-have-employment-records---386157"></a><span data-ttu-id="c7530-112">Kann keine Arbeitskräfte löschen, die keine Beschäftigungsdatensätze haben – (386157)</span><span class="sxs-lookup"><span data-stu-id="c7530-112">Can't delete workers that don't have employment records - (386157)</span></span>

<span data-ttu-id="c7530-113">Diese Änderung fügt eine Löschoption im Formular **Arbeitskräfte ohne Beschäftigung** hinzu.</span><span class="sxs-lookup"><span data-stu-id="c7530-113">This change adds a delete option in the **Workers without employment** form.</span></span> <span data-ttu-id="c7530-114">Arbeitskräfte erscheinen in dieser Form, wenn für die Arbeitskraft keine zukünftigen, aktiven oder historischen Beschäftigungen existieren.</span><span class="sxs-lookup"><span data-stu-id="c7530-114">Workers appear in this form when no future, active, or historical employments exist for the worker.</span></span> <span data-ttu-id="c7530-115">In dieser Version ist das Löschen nur für Systemadministratoren aktiviert.</span><span class="sxs-lookup"><span data-stu-id="c7530-115">In this release, delete is only enabled for System Administrators.</span></span> <span data-ttu-id="c7530-116">In der Version nächste Woche wird jedoch die Sicherheit so aktualisiert, dass alle Benutzer mit der Rolle des Personalassistenten Mitarbeiter ohne Beschäftigung entfernen können.</span><span class="sxs-lookup"><span data-stu-id="c7530-116">However, in next week's release, security will be updated to allow all users with the HR assistant role to remove employees without employments.</span></span> <span data-ttu-id="c7530-117">Sie können diese Änderungen auch manuell vornehmen, indem Sie die folgenden Schritte ausführen.</span><span class="sxs-lookup"><span data-stu-id="c7530-117">You can also make these changes manually by following the following steps.</span></span>

1. <span data-ttu-id="c7530-118">Gehen Sie zu **Sicherheitskonfiguration**.</span><span class="sxs-lookup"><span data-stu-id="c7530-118">Go to **Security configuration**.</span></span>
2. <span data-ttu-id="c7530-119">Filtern Sie in der Registerkarte **Privilegien** die Liste der **Privilegien** nach **Arbeitskräfte pflegen**.</span><span class="sxs-lookup"><span data-stu-id="c7530-119">In the **Privileges** tab, filter the **Privileges** list to **Maintain workers**.</span></span>
3. <span data-ttu-id="c7530-120">Wählen Sie in der Spalte **Verweise** **Menüpunkte anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="c7530-120">In the **References** column, select **Display menu items**.</span></span>
4. <span data-ttu-id="c7530-121">Wählen Sie in **Menüpunkte anzeigen** **HCM-Arbeitskräfte ohne Beschäftigung**.</span><span class="sxs-lookup"><span data-stu-id="c7530-121">In **Display menu items**, select **HcmWOrkersWithoutEmployment**.</span></span>
5. <span data-ttu-id="c7530-122">Stellen Sie die Erlaubnis zum **Löschen** auf Erteilen.</span><span class="sxs-lookup"><span data-stu-id="c7530-122">Set the **Delete** permission to Grant.</span></span>
6. <span data-ttu-id="c7530-123">Wählen Sie die Registerkarte **Unveröffentlichte Objekte** aus.</span><span class="sxs-lookup"><span data-stu-id="c7530-123">Select the **Unpublished objects** tab.</span></span>
7. <span data-ttu-id="c7530-124">Wählen Sie **Alle veröffentlichen** aus.</span><span class="sxs-lookup"><span data-stu-id="c7530-124">Select **Publish all**.</span></span>
