---
title: Eine Frage stellen, die von der Antwort auf die vorherige Frage abhängt
description: Bedingte Fragen bieten die Möglichkeit, basierend auf der vorhergehenden Antwort anzugeben, welche nachfolgende Frage einem Befragungsteilnehmer angezeigt wird.
author: andreabichsel
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KMCollection, KMCollectionQuestion, KMCollectionQuestionTree, HcmLearningWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 39da0418f60273a82cb51e5cf3aad60e4efdb234
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6056659"
---
# <a name="make-a-question-dependent-on-the-answer-of-the-previous-question"></a><span data-ttu-id="2bfb3-103">Eine Frage stellen, die von der Antwort auf die vorherige Frage abhängt</span><span class="sxs-lookup"><span data-stu-id="2bfb3-103">Make a question dependent on the answer of the previous question</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



<span data-ttu-id="2bfb3-104">Bedingte Fragen bieten die Möglichkeit, basierend auf der vorhergehenden Antwort anzugeben, welche nachfolgende Frage einem Befragungsteilnehmer angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="2bfb3-104">Conditional questions allow you to specify what follow-up question will be presented to a respondent, based on the answer to the preceding question.</span></span> <span data-ttu-id="2bfb3-105">Wenn Sie zum Beispiel "Bevorzugen Sie Kaffee oder Tee?" fragen, kann eine logische nachfolgende Frage abhängig davon ermittelt werden, ob der Befragte Kaffee oder Tee als Antwort auswählt.</span><span class="sxs-lookup"><span data-stu-id="2bfb3-105">For example, if you ask "Do you prefer coffee or tea," a logical follow-up question can be determined depending on whether the respondent selects coffee or tea as their answer.</span></span> <span data-ttu-id="2bfb3-106">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF.</span><span class="sxs-lookup"><span data-stu-id="2bfb3-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="find-the-existing-questionnaire"></a><span data-ttu-id="2bfb3-107">Durchsuchen des vorhandenen Fragebogens</span><span class="sxs-lookup"><span data-stu-id="2bfb3-107">Find the existing questionnaire</span></span>
1. <span data-ttu-id="2bfb3-108">Wechseln Sie zu "Fragebogen" > "Entwurf" > "Fragebögen".</span><span class="sxs-lookup"><span data-stu-id="2bfb3-108">Go to Questionnaire > Design > Questionnaires.</span></span>
2. <span data-ttu-id="2bfb3-109">Wählen Sie den WorkFH-Fragebogen in der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="2bfb3-109">In the list, select the WorkFH questionnaire.</span></span>

## <a name="add-all-questions-and-sub-questions-to-the-questionnaire"></a><span data-ttu-id="2bfb3-110">Alle Fragen und Unterfragen zum Fragebogen hinzufügen</span><span class="sxs-lookup"><span data-stu-id="2bfb3-110">Add all questions and sub-questions to the Questionnaire</span></span>
1. <span data-ttu-id="2bfb3-111">Klicken Sie auf "Fragen".</span><span class="sxs-lookup"><span data-stu-id="2bfb3-111">Click Questions.</span></span>
2. <span data-ttu-id="2bfb3-112">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="2bfb3-112">Click New.</span></span>
3. <span data-ttu-id="2bfb3-113">Wählen Sie im Feld "Frage" die Fragenummer 00016 aus.</span><span class="sxs-lookup"><span data-stu-id="2bfb3-113">In the Question field, select question number 00016.</span></span>
4. <span data-ttu-id="2bfb3-114">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="2bfb3-114">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="2bfb3-115">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="2bfb3-115">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="2bfb3-116">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="2bfb3-116">Click Save.</span></span>
7. <span data-ttu-id="2bfb3-117">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="2bfb3-117">Close the page.</span></span>

## <a name="set-the-questionnaire-sequence-to-conditional-and-make-the-question-dependent-on-the-appropriate-question"></a><span data-ttu-id="2bfb3-118">Legen Sie die Fragebogensequenz auf "Bedingt" fest und machen Sie die Frage abhängig von der entsprechenden Frage</span><span class="sxs-lookup"><span data-stu-id="2bfb3-118">Set the Questionnaire Sequence to Conditional and make the question dependent on the appropriate question</span></span>
1. <span data-ttu-id="2bfb3-119">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="2bfb3-119">Click Edit.</span></span>
2. <span data-ttu-id="2bfb3-120">Erweitern Sie den Abschnitt 'Einstellungen'.</span><span class="sxs-lookup"><span data-stu-id="2bfb3-120">Expand the Setup section.</span></span>
3. <span data-ttu-id="2bfb3-121">Wählen Sie im Feld "Reihenfolge Fragen" "Bedingt" aus.</span><span class="sxs-lookup"><span data-stu-id="2bfb3-121">In the Question order field, select 'Conditional'.</span></span>
4. <span data-ttu-id="2bfb3-122">Klicken Sie auf "Bedingte Frage".</span><span class="sxs-lookup"><span data-stu-id="2bfb3-122">Click Conditional question.</span></span>
5. <span data-ttu-id="2bfb3-123">Wählen Sie in der Struktur "Fragen\Erläutern Sie, warum Sie die vorherige Frage so beantwortet haben?" aus.</span><span class="sxs-lookup"><span data-stu-id="2bfb3-123">In the tree, select 'Questions\Explain why you answered the previous question the way you did?'.</span></span>
6. <span data-ttu-id="2bfb3-124">Wählen Sie im Feld "Primäre Frage" die Frage 00009 aus.</span><span class="sxs-lookup"><span data-stu-id="2bfb3-124">In the Primary question field, select question 00009</span></span>
7. <span data-ttu-id="2bfb3-125">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="2bfb3-125">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="2bfb3-126">Geben Sie im Feld "Antwort" die Antwortsequenzkennung der Antwortoption ein, von der die Frage abhängig sein soll.</span><span class="sxs-lookup"><span data-stu-id="2bfb3-126">In the Answer field, enter the answer sequence ID of the answer option you want to make the question dependent on.</span></span> <span data-ttu-id="2bfb3-127">Geben Sie beispielsweise 1 für die erste Antwortoption ein.</span><span class="sxs-lookup"><span data-stu-id="2bfb3-127">For example, enter 1 for the first answer option.</span></span>
9. <span data-ttu-id="2bfb3-128">Klicken Sie auf Speichern.</span><span class="sxs-lookup"><span data-stu-id="2bfb3-128">Click Save.</span></span>
10. <span data-ttu-id="2bfb3-129">Wählen Sie in der Struktur "Fragen\Ich werde angemessen für meine Arbeit bezahlt" aus.</span><span class="sxs-lookup"><span data-stu-id="2bfb3-129">In the tree, select 'Questions\I am paid fairly for the work I do.'.</span></span>
    * <span data-ttu-id="2bfb3-130">Beachten Sie, dass die Fragenstruktur aktualisiert wird, sodass die Abhängigkeit angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="2bfb3-130">Note that the question tree updated to show the dependency.</span></span>  



[!INCLUDE[footer-include](../includes/footer-banner.md)]