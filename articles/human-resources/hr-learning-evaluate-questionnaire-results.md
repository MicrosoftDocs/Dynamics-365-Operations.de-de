---
title: Anzeigen und Auswerten der Ergebnisse eines Fragebögen
description: In diesem Artikel wird beschrieben, wie Sie die Ergebnisse von Fragebögen anzeigen und bewerten können, die die Befragten abgeschlossen haben.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMCollection, KMKnowledgeCollectorCollection, KMKnowledgeCollectorUserResults, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 17444
ms.assetid: 6570206a-b2c4-4025-8715-432fe6652b78
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: ceb21af75dca2756d8e07f315ddee0246554c854
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4418735"
---
# <a name="view-and-evaluate-the-results-of-questionnaires"></a><span data-ttu-id="9c3a8-103">Anzeigen und Auswerten der Ergebnisse eines Fragebögen</span><span class="sxs-lookup"><span data-stu-id="9c3a8-103">View and evaluate the results of questionnaires</span></span>

<span data-ttu-id="9c3a8-104">In diesem Artikel wird beschrieben, wie Sie die Ergebnisse von Fragebögen anzeigen und bewerten können, die die Befragten abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="9c3a8-104">This article explains how you can view and evaluate the results of questionnaires that respondents complete.</span></span> 

<span data-ttu-id="9c3a8-105">Nachdem die Befragungsteilnehmer einen Fragebogen ausgefüllt haben, können Sie die Fragebogenergebnisse folgendermaßen anzeigen und auswerten:</span><span class="sxs-lookup"><span data-stu-id="9c3a8-105">After respondents complete a questionnaire, you can view and evaluate the questionnaire results in the following ways:</span></span>

-   <span data-ttu-id="9c3a8-106">**Ausgefüllte Antwortsitzungen** - Anzeigen von Details zu ausgefüllten Fragebögen der Befragten und Generieren von Berichten, um Antworten zusammenzufassen, auch zu den erworbenen Punkten.</span><span class="sxs-lookup"><span data-stu-id="9c3a8-106">**Completed answer sessions** – View details about the questionnaires that respondents have completed, and generate reports to summarize answers and any points that were earned.</span></span>
-   <span data-ttu-id="9c3a8-107">**Ergebnisgruppen** - Anzeigen von Ergebnisgruppedetails und -statistiken für Fragebögen.</span><span class="sxs-lookup"><span data-stu-id="9c3a8-107">**Result groups** – View result group details and statistics for questionnaires.</span></span> <span data-ttu-id="9c3a8-108">Die Ergebnisgruppenstatistik kann für eine einzelne Antwortsitzung oder für alle Beantwortungssitzungen eines Fragebogens generiert werden.</span><span class="sxs-lookup"><span data-stu-id="9c3a8-108">Result group statistics can be generated for either a single answer session  of a questionnaire or all answer sessions.</span></span>
-   <span data-ttu-id="9c3a8-109">**Fragebogenstatistik** - Angeben von Kriterien für die Berechnung von Statistiken für eine bestimmte Gruppe von Teilnehmern.</span><span class="sxs-lookup"><span data-stu-id="9c3a8-109">**Questionnaire statistics** – Specify criteria to calculate statistics for a specific group of respondents.</span></span>

<span data-ttu-id="9c3a8-110">Es können auch verschiedene Berichte generiert werden, um Ergebnisse nach Person, Antwortsitzung oder Ergebnisgruppe sortiert anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9c3a8-110">You can also generate various reports to view results that are sorted by person, answer session, or result group.</span></span> <span data-ttu-id="9c3a8-111">Die folgenden Berichte zu ausgefüllten Fragebögen sind verfügbar:</span><span class="sxs-lookup"><span data-stu-id="9c3a8-111">The following reports that are related to completed questionnaires are available:</span></span>

-   <span data-ttu-id="9c3a8-112">Antworten</span><span class="sxs-lookup"><span data-stu-id="9c3a8-112">Answers</span></span>
-   <span data-ttu-id="9c3a8-113">Antworten pro Fragebogen</span><span class="sxs-lookup"><span data-stu-id="9c3a8-113">Answers per questionnaire</span></span>
-   <span data-ttu-id="9c3a8-114">Antworten pro Person</span><span class="sxs-lookup"><span data-stu-id="9c3a8-114">Answers per person</span></span>
-   <span data-ttu-id="9c3a8-115">Rückmeldungsanalyse</span><span class="sxs-lookup"><span data-stu-id="9c3a8-115">Feedback analysis</span></span>

## <a name="answer-session-results"></a><span data-ttu-id="9c3a8-116">Antwortsitzungsergebnisse</span><span class="sxs-lookup"><span data-stu-id="9c3a8-116">Answer session results</span></span>

<span data-ttu-id="9c3a8-117">Nachdem die Teilnehmer einen Fragebogen ausgefüllt haben, können Sie die Ergebnisse abgeschlossener Antwortsitzungen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="9c3a8-117">After respondents complete a questionnaire, you can view the results of the completed answer sessions.</span></span> <span data-ttu-id="9c3a8-118">Eine Antwortsitzung ist die Beantwortung eines Fragebogens durch einen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="9c3a8-118">An answer session is one user’s response to a questionnaire.</span></span> <span data-ttu-id="9c3a8-119">Sie können Details zu abgeschlossenen Antwortsitzungen auf der Seite **Antworten** anzeigen.</span><span class="sxs-lookup"><span data-stu-id="9c3a8-119">You can view details about completed answer sessions on the **Answers** page.</span></span> <span data-ttu-id="9c3a8-120">Die Antwortsitzungen, die auf der Seite **Antworten** enthalten sind, werden auf verschiedene Weise gefiltert, abhängig davon, wie Sie die Seite öffnen:</span><span class="sxs-lookup"><span data-stu-id="9c3a8-120">The answer sessions that are included on the **Answers** page are filtered in various ways, depending on how you open the page:</span></span>

-   <span data-ttu-id="9c3a8-121">Alle Fragebögen</span><span class="sxs-lookup"><span data-stu-id="9c3a8-121">All questionnaires</span></span>
-   <span data-ttu-id="9c3a8-122">Ein bestimmter Fragebogen</span><span class="sxs-lookup"><span data-stu-id="9c3a8-122">A specific questionnaire</span></span>
-   <span data-ttu-id="9c3a8-123">Eine bestimmte Person</span><span class="sxs-lookup"><span data-stu-id="9c3a8-123">A specific person</span></span>

<span data-ttu-id="9c3a8-124">Auf der Seite **Antworten** können Sie Details zu Antworten, erzielten Punkten, den Antworten eines Teilnehmers in jeder Ergebnisgruppe und zur Fragenhierarchie anzeigen, die im ausgewählten Fragebogen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9c3a8-124">From the **Answers** page, you can view details about answers, points that were earned, a respondent’s responses in each result group, and the question hierarchy that was used on the selected questionnaire, if a question hierarchy was used.</span></span> <span data-ttu-id="9c3a8-125">Sie können auch die folgenden Berichte generieren und drucken:</span><span class="sxs-lookup"><span data-stu-id="9c3a8-125">You can also generate and print the following reports:</span></span>

-   <span data-ttu-id="9c3a8-126">**Ergebnisbericht** - Dieser Bericht zeigt eine grafische Darstellung der Punkte, die pro Ergebnisgruppe für die ausgewählte Antwortsitzung erzielt wurden.</span><span class="sxs-lookup"><span data-stu-id="9c3a8-126">**Results report** – This report shows a graphical representation of the points that were earned per result group for the selected answer session.</span></span>
-   <span data-ttu-id="9c3a8-127">**Antwortbericht** - In diesem Bericht werden die Antworten angezeigt, die der Befragte für jede Frage zum Fragebogen ausgewählt hat.</span><span class="sxs-lookup"><span data-stu-id="9c3a8-127">**Answer report** – This report shows the answers that the respondent selected for each question on the questionnaire.</span></span>
-   <span data-ttu-id="9c3a8-128">**Falsche Antworten** - Dieser Bericht werden Informationen zu den falschen Antworten des Befragten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9c3a8-128">**Incorrect answers** – This report shows information that is related to the incorrect answers that the respondent selected.</span></span>

> [!NOTE]
> <span data-ttu-id="9c3a8-129">Der Bericht **Ergebnisse** ist nur verfügbar, wenn Sie Ergebnisgruppen auf dem Fragebogen verwenden und wenn Sie die Seite **Ergebnisse** auf der Seite **Fragebögen** ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="9c3a8-129">The **Results** report is available only if you use results groups on the questionnaire, and if you selected **Results page** on the **Questionnaires** page.</span></span> <span data-ttu-id="9c3a8-130">Der **Antwort**-Bericht und der **Falsche Antworten**-Bericht sind nur verfügbar, wenn Sie auf der Seite **Antwortbericht** der Seite **Fragebögen** ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="9c3a8-130">The **Answer** report and the **Incorrect answers** report are available only if you selected **Answer report** on the **Questionnaires** page.</span></span>

## <a name="questionnaire-statistics"></a><span data-ttu-id="9c3a8-131">Fragebogenstatistik</span><span class="sxs-lookup"><span data-stu-id="9c3a8-131">Questionnaire statistics</span></span>

<span data-ttu-id="9c3a8-132">Mithilfe der Fragebogenstatistik können Sie die Ergebnisse eines ausgefüllten Fragebogen analysieren, der auf den Berechnungen beruht, die Sie definieren.</span><span class="sxs-lookup"><span data-stu-id="9c3a8-132">You can use questionnaire statistics to analyze the results of a completed questionnaire, based on calculations that you define.</span></span> <span data-ttu-id="9c3a8-133">Um Berechnungen zu definieren, müssen Sie die folgenden Aufgaben ausführen:</span><span class="sxs-lookup"><span data-stu-id="9c3a8-133">To define calculations, you must complete the following tasks:</span></span>

-   <span data-ttu-id="9c3a8-134">Wählen Sie Kriterien aus, um die Statistik zu berechnen und anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9c3a8-134">Select criteria to calculate and display the statistics.</span></span>
    -   <span data-ttu-id="9c3a8-135">Sie können Statistiken nach Fragebogen, Fragen, Fragenzeilen oder Ergebnisgruppen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="9c3a8-135">You can show statistics by questionnaire, questions, question rows, or results groups.</span></span>
    -   <span data-ttu-id="9c3a8-136">Wählen Sie den Diagrammtyp aus, der verwendet wird, wenn Sie Ergebnisse anzeigen.</span><span class="sxs-lookup"><span data-stu-id="9c3a8-136">Select the type of chart that will be used when you view results.</span></span>
    -   <span data-ttu-id="9c3a8-137">Wählen Sie die Typen von Personen im Netzwerk aus, z. B. Mitarbeiter, Kontaktperson oder Bewerber, deren Antworten einbezogen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9c3a8-137">Select the types of people from the network, such as employees, contact persons, or applicants, to include answers for.</span></span> <span data-ttu-id="9c3a8-138">Sie können auch Antworten von Fragebögen einbeziehen, die anonym ausgefüllt wurden.</span><span class="sxs-lookup"><span data-stu-id="9c3a8-138">You can also include answers from questionnaires that were completed anonymously.</span></span>
    -   <span data-ttu-id="9c3a8-139">Richten Sie Intervalle ein, die auf dem Alter oder Dienstalter beruhen, um die Ergebnisse zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="9c3a8-139">Set up intervals that are based on age or seniority to analyze results.</span></span>
-   <span data-ttu-id="9c3a8-140">Hier können Sie Einstellungen auswählen oder anzeigen, mit denen das Thema der Statistik enger eingegrenzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="9c3a8-140">Select or verify settings that refine the subject of the statistics.</span></span> <span data-ttu-id="9c3a8-141">Wenn Sie z. B. eine Postleitzahl auswählen, können Sie die Ergebnisse für alle Befragten im betreffenden geografischen Gebiet analysieren.</span><span class="sxs-lookup"><span data-stu-id="9c3a8-141">For example, by selecting a ZIP Code or postal code, you can analyze results for all respondents within a specific geographic area.</span></span>
-   <span data-ttu-id="9c3a8-142">Wählen Sie Kriterien aus, oder zeigen Sie Kriterien an, um die Ergebnisse nach Merkmalen des Befragten oder des Fragebogens zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="9c3a8-142">Select or verify criteria to analyze results by respondent or questionnaire characteristics.</span></span> <span data-ttu-id="9c3a8-143">Wenn Sie z. B. die **Postleitzahl** auswählen, können Sie die Korrelation zwischen dem Standort eines Befragten und den richtigen Antworten analysieren.</span><span class="sxs-lookup"><span data-stu-id="9c3a8-143">For example, by selecting **ZIP/postal code**, you can analyze the correlation between a respondent’s location and correct answers.</span></span>

<span data-ttu-id="9c3a8-144">Die festgelegten Einstellungen werden gespeichert und können zur regelmäßigen Neuberechnung der Ergebnisse verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9c3a8-144">The settings that you define are saved and can be used to periodically recalculate results.</span></span>