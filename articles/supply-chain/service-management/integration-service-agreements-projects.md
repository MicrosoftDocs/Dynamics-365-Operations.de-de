---
title: Integration von Servicevereinbarungen und Projekten
description: 'Bei der Arbeit mit Servicevereinbarungen und Servicevereinbarungspositionen werden Daten aus den folgenden Bereichen des Moduls Projektverwaltung und -buchhaltung verwendet:'
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 6bd2fb1f54a3decb77f019db6b2016cebdcaddb9
ms.contentlocale: de-de
ms.lasthandoff: 08/07/2018

---

# <a name="integration-for-service-agreements-and-projects"></a><span data-ttu-id="6234e-103">Integration von Servicevereinbarungen und Projekten</span><span class="sxs-lookup"><span data-stu-id="6234e-103">Integration for service agreements and projects</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="6234e-104">Bei der Arbeit mit Servicevereinbarungen und Servicevereinbarungspositionen werden Daten aus den folgenden Bereichen des Moduls **Projektverwaltung und -buchhaltung** verwendet:</span><span class="sxs-lookup"><span data-stu-id="6234e-104">When you work with service agreements and service agreement lines, you use data that is set up in the following areas in **Project management and accounting**.</span></span>

## <a name="project-prices"></a><span data-ttu-id="6234e-105">Projektpreise</span><span class="sxs-lookup"><span data-stu-id="6234e-105">Project prices</span></span>

<span data-ttu-id="6234e-106">Der Einstands- und der Verkaufspreis für eine Servicevereinbarungsbuchung werden aus den Einstandspreiseinstellungen abgeleitet, die für das Projekt gelten, das der Servicevereinbarung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="6234e-106">The cost and the sales price for a service agreement transaction are derived from the cost price setup that applies to the project that is attached to the service agreement.</span></span> <span data-ttu-id="6234e-107">Einstands- und Verkaufspreis können für ein Projekt, für einen Mitarbeiter oder für eine Kategorie eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="6234e-107">Cost and sales prices can be set up by project, employee, and category.</span></span> 

## <a name="project-validation"></a><span data-ttu-id="6234e-108">Projektprüfung</span><span class="sxs-lookup"><span data-stu-id="6234e-108">Project validation</span></span>

<span data-ttu-id="6234e-109">Die Projekte, Mitarbeiter und Kategorien, die in einer Servicevereinbarungsposition zur Auswahl stehen, können mithilfe der Prüfungseinstellungen im Modul **Projektverwaltung und -buchhaltung** eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="6234e-109">The projects, employees, and categories that are available for selection on a service agreement line can be limited by the validation setup in **Project management and accounting**.</span></span> <span data-ttu-id="6234e-110">Die Prüfungseinstellungen ermöglichen das Kombinieren von Mitarbeitern, Projekten und Kategorien für die Zugriffsteuerung.</span><span class="sxs-lookup"><span data-stu-id="6234e-110">By using the validation setup, you can combine employees, projects, and categories for control access.</span></span> 

## <a name="project-line-properties"></a><span data-ttu-id="6234e-111">Projektpositionseigenschaften</span><span class="sxs-lookup"><span data-stu-id="6234e-111">Project line properties</span></span>

<span data-ttu-id="6234e-112">Servicevereinbarungspositionen werden automatisch mit einem Abrechnungscode versehen.</span><span class="sxs-lookup"><span data-stu-id="6234e-112">A line property is entered automatically for a service agreement line.</span></span>

<span data-ttu-id="6234e-113">Abrechnungscodes werden im Modul **Abrechnungscodes** im Formular **Projektverwaltung und -buchhaltung** erstellt.</span><span class="sxs-lookup"><span data-stu-id="6234e-113">Line properties are created in the **Line properties** form in **Project management and accounting**.</span></span> <span data-ttu-id="6234e-114">Der für eine Servicevereinbarung eingegebene Abrechnungscode ist dem Projekt zugeordnet, das für die Servicevereinbarung ausgewählt ist, und wird in der Servicevereinbarungsposition übernommen.</span><span class="sxs-lookup"><span data-stu-id="6234e-114">The line property that is entered on a service agreement is attached to the project that is selected for the service agreement and inherited subsequently by the service agreement line.</span></span> 

## <a name="default-offset-accounts"></a><span data-ttu-id="6234e-115">Standardgegenkonten</span><span class="sxs-lookup"><span data-stu-id="6234e-115">Default offset accounts</span></span>

<span data-ttu-id="6234e-116">Wenn Sie eine Ausgabenbuchung eingeben, wird für die Buchung automatisch ein standardmäßiges Ausgabengegenkonto ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="6234e-116">If you enter an expense transaction, a default expense offset account is selected automatically for the transaction.</span></span> <span data-ttu-id="6234e-117">Das standardmäßige Ausgabenkonto wird für das Projekt eingerichtet, das der aktuellen Servicevereinbarung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="6234e-117">The default expense account is set up for the project that is attached to the current service agreement.</span></span>

## <a name="project-categories"></a><span data-ttu-id="6234e-118">Projektkategorien</span><span class="sxs-lookup"><span data-stu-id="6234e-118">Project categories</span></span>

<span data-ttu-id="6234e-119">Die Kategorien, die für die Servicevereinbarungspositionen zur Verfügung stehen, werden im Bereich **Projektkategorien** im Formular **Projektverwaltung und -buchhaltung** eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="6234e-119">The categories that are available for service agreement lines are set up in the **Project categories** form in **Project management and accounting**.</span></span> 

> [!NOTE]
> <P><span data-ttu-id="6234e-120">Kategorien, bei denen im Formular <STRONG>Projektkategorien</STRONG> auf der Registerkarte <STRONG>Projekt</STRONG> das Kontrollkästchen <STRONG>Aktiv in Erfassungen</STRONG> aktiviert ist, können ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="6234e-120">Categories that have the <STRONG>Active in journals</STRONG> check box selected on the <STRONG>Project</STRONG> tab in the <STRONG>Project categories</STRONG> form are available for selection.</span></span> <span data-ttu-id="6234e-121">Ist dagegen im Formular <STRONG>Projektverwaltungs- und -verrechnungsparameter</STRONG> auf der Registerkarte <STRONG>Erfasssungen</STRONG> das Kontrollkästchen <STRONG>Inaktive Kategorien</STRONG> aktiviert, stehen alle Kategorien zur Auswahl.</span><span class="sxs-lookup"><span data-stu-id="6234e-121">However, if the <STRONG>Inactive categories</STRONG> check box is selected on the <STRONG>Journals</STRONG> tab in the <STRONG>Project management and accounting parameters</STRONG> form, all categories are available for selection.</span></span></P>

## <a name="project-parameters"></a><span data-ttu-id="6234e-122">Projektparameter</span><span class="sxs-lookup"><span data-stu-id="6234e-122">Project parameters</span></span>

<span data-ttu-id="6234e-123">Wenn das Feld **Ausgeschiedene Arbeitskräfte** auf der Registerkarte **Erfassungen** im Formular **Projektverwaltungs- und Buchhaltungsparameter** aktiviert wird, können sowohl aktive als auch inaktive Mitarbeiter Mitarbeiter in den Formularen **Serviceverträge** und **Serviceaufträge** auswählen.</span><span class="sxs-lookup"><span data-stu-id="6234e-123">If the **Terminated workers** field on the **Journals** tab in the **Project management and accounting parameters** form is selected, you can select inactive employees and active employees in the **Service agreements** and **Service orders** forms.</span></span>

<span data-ttu-id="6234e-124">Darüber hinaus können Sie im Formular **Serviceaufträge** auf der Registerkarte **Projekt** die Kontrollkästchen **Startzeit** und **Endzeit** aktivieren, um in den Serviceauftragspositionen eine Start- und eine Endzeit einzugeben.</span><span class="sxs-lookup"><span data-stu-id="6234e-124">Also, you can enable the **Start time** and **End time** fields on the **Project** tab in the **Service orders** form to enter starting and ending times on service order lines.</span></span>

## <a name="enable-the-starting-and-ending-time-feature-for-service-orders"></a><span data-ttu-id="6234e-125">Aktivieren der Funktion für die Start- und Endzeit von Serviceaufträgen</span><span class="sxs-lookup"><span data-stu-id="6234e-125">Enable the starting and ending time feature for service orders</span></span>

1.  <span data-ttu-id="6234e-126">Klicken Sie auf **Projektverwaltung und Buchhaltung** \> **Setup** \> **Projektverwaltungs- und Buchhaltungsparameter**.</span><span class="sxs-lookup"><span data-stu-id="6234e-126">Click **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>

2.  <span data-ttu-id="6234e-127">Klicken Sie auf die Registerkarte **Erfassungen**, und aktivieren Sie dann das Kontrollkästchen **Start-/Endzeiten anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="6234e-127">Click the **Journals** tab, and then select the **Show start/end times** check box.</span></span>

3.  <span data-ttu-id="6234e-128">Klicken auf **Projektverwaltung und -buchhaltung** \> **Einrichtung** \> **Erfassungen** \> **Erfassungsnamen**</span><span class="sxs-lookup"><span data-stu-id="6234e-128">Click **Project management and accounting** \> **Setup** \> **Journals** \> **Journal names**.</span></span>

4.  <span data-ttu-id="6234e-129">Wählen Sie das Journal aus, das dem Serviceauftrag zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="6234e-129">Select the journal name that is attached to the service order.</span></span>

5.  <span data-ttu-id="6234e-130">Klicken Sie auf die Registerkarte **Allgemein**, und aktivieren Sie dann das Kontrollkästchen **Start-/Endzeiten anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="6234e-130">Click the **General** tab, and then select the **Show start/end times** check box.</span></span>


> [!NOTE]
> <P><span data-ttu-id="6234e-131">wählen Sie den Erfassungnamen für den Serviceauftragen im Feld <STRONG>Stunde</STRONG> auf der Registerkarte <STRONG>Erfassungen</STRONG> im Formular <STRONG>Serviceverwaltungsparameter</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="6234e-131">Select the journal name for the service order in the <STRONG>Hour</STRONG> field on the <STRONG>Journals</STRONG> tab in the <STRONG>Service management parameters</STRONG> form.</span></span></P>






