---
title: Einrichten von Personalverwaltungsparametern in verschiedenen juristischen Personen
description: "Sie müssen gemeinsame Parameter für Datensätze einrichten, die über Unternehmen freigegeben werden, wie Positionsdatensätzen einrichten. Dieser Artikel beschreibt, wie Sie Personalverwaltungsparameter einrichten, die für alle juristischen Personen verwendet werden."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmSharedParameters
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 90d348f8b8414d6e31092cdd18760375dd283155
ms.contentlocale: de-de
ms.lasthandoff: 06/29/2017


---

# <a name="set-up-hr-parameters-across-legal-entities"></a><span data-ttu-id="402fa-104">Einrichten von Personalverwaltungsparametern in verschiedenen juristischen Personen</span><span class="sxs-lookup"><span data-stu-id="402fa-104">Set up HR parameters across legal entities</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="402fa-105">Sie müssen gemeinsame Parameter für Datensätze einrichten, die über Unternehmen freigegeben werden, wie Positionsdatensätzen einrichten.</span><span class="sxs-lookup"><span data-stu-id="402fa-105">You must set up shared parameters for records that are shared across companies, such as Position records.</span></span> <span data-ttu-id="402fa-106">Dieser Artikel beschreibt, wie Sie Personalverwaltungsparameter einrichten, die für alle juristischen Personen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="402fa-106">This article explains how to set up Human resources parameters across legal entities.</span></span>

<span data-ttu-id="402fa-107">Gewisse Datentypen wie Positionsdaten werden in den Unternehmen freigegeben.</span><span class="sxs-lookup"><span data-stu-id="402fa-107">Some types of records, such as Position records, are shared across companies.</span></span> <span data-ttu-id="402fa-108">Für diese Datensätze müssen Sie gemeinsame Parameter einrichten.</span><span class="sxs-lookup"><span data-stu-id="402fa-108">For these records, you must set up shared parameters.</span></span> <span data-ttu-id="402fa-109">Verwenden Sie beispielsweise die Seite **Freigegebene Parameter für Personalverwaltung**, um Personalverwaltungsparameter innerhalb der juristischen Personen einzurichten.</span><span class="sxs-lookup"><span data-stu-id="402fa-109">For example, you use the **Human resources shared parameters** page to set up Human resources parameters across legal entities.</span></span> 

<span data-ttu-id="402fa-110">Auf der Seite **Freigegebene Parameter für Personalverwaltung** werden Parameter basierend auf deren Funktionalität in Bereiche gruppiert.</span><span class="sxs-lookup"><span data-stu-id="402fa-110">On the **Human resources shared parameters** page, parameters are grouped into areas, based on their functionality.</span></span> 

### <a name="previously-released-functionality"></a><span data-ttu-id="402fa-111">Bereits freigegebene Funktionen</span><span class="sxs-lookup"><span data-stu-id="402fa-111">Previously released functionality</span></span>
<span data-ttu-id="402fa-112">Auf der Registerkarte **Kennung** müssen Sie die Kennungstypen wählen, die die Kennnummern darstellen, die auf der Seite aufgeführten werden.</span><span class="sxs-lookup"><span data-stu-id="402fa-112">On the **Identification** tab, you must select the identification types that represent the identification numbers that are listed on the page.</span></span> <span data-ttu-id="402fa-113">Sie müssen Ausweistypen einrichten, bevor Sie Kennungsinformationen für Arbeitskräfte eingeben können.</span><span class="sxs-lookup"><span data-stu-id="402fa-113">You must set up identification types before you can enter identification information for workers.</span></span> <span data-ttu-id="402fa-114">Informationen zur Sozialversicherungsnummer, zum Personalausweisnummer, Ausländernummer und persönlicher ID-Code wird auf der Seite **Kennungstyp** verwaltet.</span><span class="sxs-lookup"><span data-stu-id="402fa-114">Information about the Social Security number, national ID number, alien ID number, and personal ID code is maintained on the **Identification type** page.</span></span> <span data-ttu-id="402fa-115">Um einen neuen Kennungstyp zu definieren oder die Liste der vorhandenen Typen zu prüfen, klicken Sie **Personalverwaltung** &gt; **Re Links** &gt; **Einstellungen** &gt; **Kennungstypen**</span><span class="sxs-lookup"><span data-stu-id="402fa-115">To define a new identification type or review the list of existing types, click **Personnel management** &gt; **Links tab** &gt; **Setup** &gt; **Identification types**.</span></span> <span data-ttu-id="402fa-116">Sie können einen einfachen Code und eine Beschreibung eingeben.</span><span class="sxs-lookup"><span data-stu-id="402fa-116">You can enter a simple code and description.</span></span> 

### <a name="if-youre-using-dynamics-365-for-talent"></a><span data-ttu-id="402fa-117">Wenn Sie Dynamics 365 for Talent verwenden</span><span class="sxs-lookup"><span data-stu-id="402fa-117">If you're using Dynamics 365 for Talent</span></span>
<span data-ttu-id="402fa-118">Auf der Registerkarte **Kennung** müssen Sie die Kennungstypen wählen, die die Kennnummern darstellen, die auf der Seite aufgeführten werden.</span><span class="sxs-lookup"><span data-stu-id="402fa-118">On the **Identification** tab, you must select the identification types that represent the identification numbers that are listed on the page.</span></span> <span data-ttu-id="402fa-119">Sie müssen Ausweistypen einrichten, bevor Sie Kennungsinformationen für Arbeitskräfte eingeben können.</span><span class="sxs-lookup"><span data-stu-id="402fa-119">You must set up identification types before you can enter identification information for workers.</span></span> <span data-ttu-id="402fa-120">Informationen zur Sozialversicherungsnummer, zum Personalausweisnummer, Ausländernummer und persönlicher ID-Code wird auf der Seite **Kennungstyp** verwaltet.</span><span class="sxs-lookup"><span data-stu-id="402fa-120">Information about the Social Security number, national ID number, alien ID number, and personal ID code is maintained on the **Identification type** page.</span></span> <span data-ttu-id="402fa-121">Um einen neuen Kennungstyp zu definieren oder die Liste der vorhandenen Typen zu prüfen, klicken Sie **Personalverwaltung** &gt; **Einstellungen** &gt; **Kennungstypen** an.</span><span class="sxs-lookup"><span data-stu-id="402fa-121">To define a new identification type or review the list of existing types, click **Human resources** &gt; **Setup** &gt; **Identification types**.</span></span> <span data-ttu-id="402fa-122">Sie können einen einfachen Code und eine Beschreibung eingeben.</span><span class="sxs-lookup"><span data-stu-id="402fa-122">You can enter a simple code and description.</span></span> 

<span data-ttu-id="402fa-123">Auf der Registerkarte **Nummernkreise** können Sie die Nummernkreise auswählen, die für die folgenden Datensätze verwendet werden: Personalnummer, Position, Benutzeranforderungs-ID, I-9-Dokument, Bewerber, Diskussion, Vorteils-ID und Mitarbeiteraktivität (wenn dieser Datensatztyp. aktiviert ist).</span><span class="sxs-lookup"><span data-stu-id="402fa-123">On the **Number sequences** tab, you can select the number sequences that are used for the following records: Personnel number, Position, User request ID, I-9 document, Applicant, Discussion, Benefit ID, and Personnel action (if this record type is enabled).</span></span> <span data-ttu-id="402fa-124">Um Zahlenkreisreferenzen und -codes zu verwalten, verwenden Sie die Listenseite **Zahlensequenz**.</span><span class="sxs-lookup"><span data-stu-id="402fa-124">To maintain number sequence references and codes, use the **Number sequences** list page.</span></span> <span data-ttu-id="402fa-125">Um diese Seite zu suchen, verwenden Sie die Seiten-Suchfunktion.</span><span class="sxs-lookup"><span data-stu-id="402fa-125">To find this page, use the page search feature.</span></span> 

<span data-ttu-id="402fa-126">Geben Sie auf der Registerkarte **Positionen** an, ob neue Positionen für Zuweisung standardmäßig verfügbar sind:</span><span class="sxs-lookup"><span data-stu-id="402fa-126">On the **Positions** tab, indicate whether new positions are available for assignment by default:</span></span>

-   <span data-ttu-id="402fa-127">**Immer** – Sie können Arbeitskräfte den neuen Positionen zuordnen, wenn Positionen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="402fa-127">**Always** – You can assign workers to new positions when positions are created.</span></span> <span data-ttu-id="402fa-128">Wenn Positionen erstellt werden, werden das **Verfügbar für die Zuweisung** Datum und die Uhrzeit auf der Registerkarte " **Allgemein** der Seite **Position** automatisch auf das Datum und die Uhrzeit festgelegt.</span><span class="sxs-lookup"><span data-stu-id="402fa-128">When positions are created, the **Available for assignment** date and time on the **General** tab of the **Position** page are automatically set to the creation date and time.</span></span>
-   <span data-ttu-id="402fa-129">**Nie** – Sie können keine Arbeitskräfte den neuen Positionen zuordnen, wenn Positionen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="402fa-129">**Never** – You can't assign workers to new positions when positions are created.</span></span> <span data-ttu-id="402fa-130">Wenn Sie diese Option auswählen, müssen Sie die Seite **Position** für jede neu verfügbare Position öffnen und dann auf der Registerkarte **Allgemein** das Datum **Verfügbar für Zuweisung** eingeben, um die Arbeitskraftzuweisung zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="402fa-130">If you select this option, you must open the **Position** page for each new position as it becomes available, and then, on the **General** tab, enter the **Available for assignment** date to enable worker assignment.</span></span>


<a name="see-also"></a><span data-ttu-id="402fa-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="402fa-131">See also</span></span>
--------

[<span data-ttu-id="402fa-132">Einrichten von unternehmensspezifischen Personalverwaltungsparametern</span><span class="sxs-lookup"><span data-stu-id="402fa-132">Set up company specific HR parameters</span></span>](set-up-company-specific-hr-parameters.md)




