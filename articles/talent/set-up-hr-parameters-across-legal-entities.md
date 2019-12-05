---
title: Einrichten von Personalverwaltungsparametern bei verschiedenen juristischen Personen
description: Sie müssen gemeinsame Parameter für Datensätze einrichten, die über Unternehmen freigegeben werden, wie Positionsdatensätzen einrichten. Dieser Artikel beschreibt, wie Sie Personalverwaltungsparameter einrichten, die für alle juristischen Personen verwendet werden.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmSharedParameters
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: 9c205973097c82a4b131a3784392fa8d8cb5ecba
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812809"
---
# <a name="set-up-human-resources-hr-parameters-across-legal-entities"></a><span data-ttu-id="cec8f-104">Einrichten von Personalverwaltungsparametern bei verschiedenen juristischen Personen</span><span class="sxs-lookup"><span data-stu-id="cec8f-104">Set up Human resources (HR) parameters across legal entities</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cec8f-105">Sie müssen gemeinsame Parameter für Datensätze einrichten, die über Unternehmen freigegeben werden, wie Positionsdatensätzen einrichten.</span><span class="sxs-lookup"><span data-stu-id="cec8f-105">You must set up shared parameters for records that are shared across companies, such as Position records.</span></span> <span data-ttu-id="cec8f-106">Dieser Artikel beschreibt, wie Sie Personalverwaltungsparameter einrichten, die für alle juristischen Personen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cec8f-106">This article explains how to set up Human resources parameters across legal entities.</span></span>

<span data-ttu-id="cec8f-107">Gewisse Datentypen wie Positionsdaten werden in den Unternehmen freigegeben.</span><span class="sxs-lookup"><span data-stu-id="cec8f-107">Some types of records, such as Position records, are shared across companies.</span></span> <span data-ttu-id="cec8f-108">Für diese Datensätze müssen Sie gemeinsame Parameter einrichten.</span><span class="sxs-lookup"><span data-stu-id="cec8f-108">For these records, you must set up shared parameters.</span></span> <span data-ttu-id="cec8f-109">Verwenden Sie beispielsweise die Seite **Freigegebene Parameter für Personalverwaltung**, um Personalverwaltungsparameter innerhalb der juristischen Personen einzurichten.</span><span class="sxs-lookup"><span data-stu-id="cec8f-109">For example, you use the **Human resources shared parameters** page to set up Human resources parameters across legal entities.</span></span> 

<span data-ttu-id="cec8f-110">Auf der Seite **Freigegebene Parameter für Personalverwaltung** werden Parameter basierend auf deren Funktionalität in Bereiche gruppiert.</span><span class="sxs-lookup"><span data-stu-id="cec8f-110">On the **Human resources shared parameters** page, parameters are grouped into areas, based on their functionality.</span></span> 

### <a name="previously-released-functionality"></a><span data-ttu-id="cec8f-111">Bereits freigegebene Funktionen</span><span class="sxs-lookup"><span data-stu-id="cec8f-111">Previously released functionality</span></span>
<span data-ttu-id="cec8f-112">Auf der Registerkarte **Kennung** müssen Sie die Kennungstypen wählen, die die Kennnummern darstellen, die auf der Seite aufgeführten werden.</span><span class="sxs-lookup"><span data-stu-id="cec8f-112">On the **Identification** tab, you must select the identification types that represent the identification numbers that are listed on the page.</span></span> <span data-ttu-id="cec8f-113">Sie müssen Ausweistypen einrichten, bevor Sie Kennungsinformationen für Arbeitskräfte eingeben können.</span><span class="sxs-lookup"><span data-stu-id="cec8f-113">You must set up identification types before you can enter identification information for workers.</span></span> <span data-ttu-id="cec8f-114">Informationen zur Sozialversicherungsnummer, zum Personalausweisnummer, Ausländernummer und persönlicher ID-Code wird auf der Seite **Kennungstyp** verwaltet.</span><span class="sxs-lookup"><span data-stu-id="cec8f-114">Information about the Social Security number, national ID number, alien ID number, and personal ID code is maintained on the **Identification type** page.</span></span> <span data-ttu-id="cec8f-115">Um einen neuen Kennungstyp zu definieren oder die Liste der vorhandenen Typen zu prüfen, klicken Sie **Personalverwaltung** &gt; **Re Links** &gt; **Einstellungen** &gt; **Kennungstypen**</span><span class="sxs-lookup"><span data-stu-id="cec8f-115">To define a new identification type or review the list of existing types, click **Personnel management** &gt; **Links tab** &gt; **Setup** &gt; **Identification types**.</span></span> <span data-ttu-id="cec8f-116">Sie können einen einfachen Code und eine Beschreibung eingeben.</span><span class="sxs-lookup"><span data-stu-id="cec8f-116">You can enter a simple code and description.</span></span> 

### <a name="if-youre-using-dynamics-365-talent"></a><span data-ttu-id="cec8f-117">Wenn Sie Dynamics 365 Talent verwenden:</span><span class="sxs-lookup"><span data-stu-id="cec8f-117">If you're using Dynamics 365 Talent</span></span>
<span data-ttu-id="cec8f-118">Auf der Registerkarte **Kennung** müssen Sie die Kennungstypen wählen, die die Kennnummern darstellen, die auf der Seite aufgeführten werden.</span><span class="sxs-lookup"><span data-stu-id="cec8f-118">On the **Identification** tab, you must select the identification types that represent the identification numbers that are listed on the page.</span></span> <span data-ttu-id="cec8f-119">Sie müssen Ausweistypen einrichten, bevor Sie Kennungsinformationen für Arbeitskräfte eingeben können.</span><span class="sxs-lookup"><span data-stu-id="cec8f-119">You must set up identification types before you can enter identification information for workers.</span></span> <span data-ttu-id="cec8f-120">Informationen zur Sozialversicherungsnummer, zum Personalausweisnummer, Ausländernummer und persönlicher ID-Code wird auf der Seite **Kennungstyp** verwaltet.</span><span class="sxs-lookup"><span data-stu-id="cec8f-120">Information about the Social Security number, national ID number, alien ID number, and personal ID code is maintained on the **Identification type** page.</span></span> <span data-ttu-id="cec8f-121">Um einen neuen Kennungstyp zu definieren oder die Liste der vorhandenen Typen zu prüfen, klicken Sie **Personalverwaltung** &gt; **Einstellungen** &gt; **Kennungstypen** an.</span><span class="sxs-lookup"><span data-stu-id="cec8f-121">To define a new identification type or review the list of existing types, click **Human resources** &gt; **Setup** &gt; **Identification types**.</span></span> <span data-ttu-id="cec8f-122">Sie können einen einfachen Code und eine Beschreibung eingeben.</span><span class="sxs-lookup"><span data-stu-id="cec8f-122">You can enter a simple code and description.</span></span> 

<span data-ttu-id="cec8f-123">Auf der Registerkarte **Nummernkreise** können Sie die Nummernkreise auswählen, die für die folgenden Datensätze verwendet werden: Personalnummer, Position, Benutzeranforderungs-ID, I-9-Dokument, Bewerber, Diskussion, Vorteils-ID und Mitarbeiteraktivität (wenn dieser Datensatztyp. aktiviert ist).</span><span class="sxs-lookup"><span data-stu-id="cec8f-123">On the **Number sequences** tab, you can select the number sequences that are used for the following records: Personnel number, Position, User request ID, I-9 document, Applicant, Discussion, Benefit ID, and Personnel action (if this record type is enabled).</span></span> <span data-ttu-id="cec8f-124">Um Zahlenkreisreferenzen und -codes zu verwalten, verwenden Sie die Listenseite **Zahlensequenz**.</span><span class="sxs-lookup"><span data-stu-id="cec8f-124">To maintain number sequence references and codes, use the **Number sequences** list page.</span></span> <span data-ttu-id="cec8f-125">Um diese Seite zu suchen, verwenden Sie die Seiten-Suchfunktion.</span><span class="sxs-lookup"><span data-stu-id="cec8f-125">To find this page, use the page search feature.</span></span> 

<span data-ttu-id="cec8f-126">Geben Sie auf der Registerkarte **Positionen** an, ob neue Positionen für Zuweisung standardmäßig verfügbar sind:</span><span class="sxs-lookup"><span data-stu-id="cec8f-126">On the **Positions** tab, indicate whether new positions are available for assignment by default:</span></span>

-   <span data-ttu-id="cec8f-127">**Immer** – Sie können Arbeitskräfte den neuen Positionen zuordnen, wenn Positionen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="cec8f-127">**Always** – You can assign workers to new positions when positions are created.</span></span> <span data-ttu-id="cec8f-128">Wenn Positionen erstellt werden, werden das **Verfügbar für die Zuweisung** Datum und die Uhrzeit auf der Registerkarte " **Allgemein** der Seite **Position** automatisch auf das Datum und die Uhrzeit festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cec8f-128">When positions are created, the **Available for assignment** date and time on the **General** tab of the **Position** page are automatically set to the creation date and time.</span></span>
-   <span data-ttu-id="cec8f-129">**Nie** – Sie können keine Arbeitskräfte den neuen Positionen zuordnen, wenn Positionen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="cec8f-129">**Never** – You can't assign workers to new positions when positions are created.</span></span> <span data-ttu-id="cec8f-130">Wenn Sie diese Option auswählen, müssen Sie die Seite **Position** für jede neu verfügbare Position öffnen und dann auf der Registerkarte **Allgemein** das Datum **Verfügbar für Zuweisung** eingeben, um die Arbeitskraftzuweisung zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="cec8f-130">If you select this option, you must open the **Position** page for each new position as it becomes available, and then, on the **General** tab, enter the **Available for assignment** date to enable worker assignment.</span></span>


<a name="additional-resources"></a><span data-ttu-id="cec8f-131">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="cec8f-131">Additional resources</span></span>
--------

[<span data-ttu-id="cec8f-132">Unternehmensspezifische Personalverwaltungsparameter einrichten</span><span class="sxs-lookup"><span data-stu-id="cec8f-132">Set up company-specific Human resources (HR) parameters</span></span>](set-up-company-specific-hr-parameters.md)



