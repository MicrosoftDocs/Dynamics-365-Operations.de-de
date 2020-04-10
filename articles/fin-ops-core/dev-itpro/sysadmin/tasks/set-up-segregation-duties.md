---
title: Regeln für Aufgabentrennung einrichten
description: Sie können Regeln einrichten, Aufgaben abzugrenzen, die von unterschiedlichen Benutzern ausgeführt werden müssen.
author: maertenm
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 712cc90bef4f3ad56291e99edd9f963ae88add48
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143511"
---
# <a name="set-up-segregation-of-duties"></a><span data-ttu-id="7e010-103">Regeln für Aufgabentrennung einrichten</span><span class="sxs-lookup"><span data-stu-id="7e010-103">Set up segregation of duties</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7e010-104">Sie können Regeln einrichten, Aufgaben abzugrenzen, die von unterschiedlichen Benutzern ausgeführt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="7e010-104">You can set up rules to separate tasks that must be performed by different users.</span></span> <span data-ttu-id="7e010-105">Dieses Konzept wird Aufgabentrennung benannt.</span><span class="sxs-lookup"><span data-stu-id="7e010-105">This concept is named segregation of duties.</span></span> <span data-ttu-id="7e010-106">Beispielsweise kann die gleiche Person des Eingangs von Waren bestätigen und Zahlung an den Kreditor nicht verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="7e010-106">For example, you might not want the same person both to acknowledge the receipt of goods and to process payment to the vendor.</span></span> <span data-ttu-id="7e010-107">Aufgabentrennungshilfen reduzieren Sie das Risiko des Betrugs und es auch Hilfsprogrammen, die Sie Fehler oder Unregelmäßigkeiten erkennen.</span><span class="sxs-lookup"><span data-stu-id="7e010-107">Segregation of duties helps you reduce the risk of fraud, and it also helps you detect errors or irregularities.</span></span> <span data-ttu-id="7e010-108">Sie können Aufgabentrennung auch verwenden, um Richtlinien der internen Kontrolle zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="7e010-108">You can also use segregation of duties to enforce internal control policies.</span></span> <span data-ttu-id="7e010-109">Gehen Sie zum Erstellen einer Regel folgendermaßen vor.</span><span class="sxs-lookup"><span data-stu-id="7e010-109">Complete the following procedure to create a rule.</span></span> <span data-ttu-id="7e010-110">Sie müssen ein -Systemadministrator sein, um dieses Verfahren auszuführen.</span><span class="sxs-lookup"><span data-stu-id="7e010-110">You must be a system administrator to complete the procedure.</span></span> <span data-ttu-id="7e010-111">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist DAT.</span><span class="sxs-lookup"><span data-stu-id="7e010-111">The demo data company used to create this procedure is DAT.</span></span> 

1. <span data-ttu-id="7e010-112">Wechseln Sie zu **Navigationsbereich > Module > Systemverwaltung > Sicherheit > Aufgabentrennung > Aufgabentrennungsregeln**.</span><span class="sxs-lookup"><span data-stu-id="7e010-112">Go to **Navigation pane > Modules > System administration > Security > Segregation of duties > Segregation of duties rules**.</span></span>
2. <span data-ttu-id="7e010-113">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="7e010-113">Click **New**.</span></span>
3. <span data-ttu-id="7e010-114">Geben Sie im Feld **Name** einen Wert für die Regel ein.</span><span class="sxs-lookup"><span data-stu-id="7e010-114">In the **Name** field, type a value for the rule.</span></span>
4. <span data-ttu-id="7e010-115">Klicken Sie im Feld **Erste Aufgabe** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="7e010-115">In the **First duty** field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="7e010-116">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="7e010-116">In the list, find and select the desired record.</span></span> <span data-ttu-id="7e010-117">Wählen Sie die erste Aufgabe, die mit der Regel gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="7e010-117">Select the first duty that is controlled by the rule.</span></span>
6. <span data-ttu-id="7e010-118">Klicken Sie im Feld **Zweite Aufgabe** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="7e010-118">In the **Second duty** field, click the drop-down button to open the lookup.</span></span> 
7. <span data-ttu-id="7e010-119">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="7e010-119">In the list, find and select the desired record.</span></span> <span data-ttu-id="7e010-120">Wählen Sie die zweite Aufgabe, die mit der Regel gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="7e010-120">Select the second duty that is controlled by the rule.</span></span>
10. <span data-ttu-id="7e010-121">Wählen Sie im Feld **Schweregrad** eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="7e010-121">In the **Severity** field, select an option.</span></span> <span data-ttu-id="7e010-122">Wählen Sie hier den Schweregrad des Risikos aus, das auftritt, wenn der gleiche Benutzer oder die gleiche Rolle beide Aufgaben ausführt.</span><span class="sxs-lookup"><span data-stu-id="7e010-122">Select the severity of the risk that occurs when the same user or role performs both duties.</span></span>  
11. <span data-ttu-id="7e010-123">Geben Sie im Feld **Sicherheitsrisiko** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="7e010-123">In the **Security risk** field, type a value.</span></span> <span data-ttu-id="7e010-124">Beschreibung des Sicherheitsrisikos eingeben.</span><span class="sxs-lookup"><span data-stu-id="7e010-124">Enter a description of the security risk.</span></span>  
12. <span data-ttu-id="7e010-125">Geben Sie im Feld **Sicherheitsbehandlung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="7e010-125">In the **Security mitigation** field, type a value.</span></span> <span data-ttu-id="7e010-126">Geben Sie eine Beschreibung der Aktivitäten ein, die Sie nehmen, um das Sicherheitsrisiko zu minimieren.</span><span class="sxs-lookup"><span data-stu-id="7e010-126">Enter a description of the actions that you take to mitigate the security risk.</span></span> <span data-ttu-id="7e010-127">So können Sie das Risiko minimieren, indem Sie detailliertere Überprüfung des Prozesses durchführen, indem Sie einen Monatsverwaltungsreview tätigen oder indem Sie Ressourcen mit anderen Abteilungen freigeben.</span><span class="sxs-lookup"><span data-stu-id="7e010-127">For example, you can mitigate the risk by conducting more detailed reviews of the process, by conducting a monthly managerial review, or by sharing resources with other departments.</span></span>     
13. <span data-ttu-id="7e010-128">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="7e010-128">Click **Save**.</span></span>

