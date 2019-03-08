---
title: Regeln für Aufgabentrennung einrichten
description: Sie können Regeln einrichten, Aufgaben abzugrenzen, die von unterschiedlichen Benutzern ausgeführt werden müssen.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 68e1a4419eaa11a59e1b634deb8e76a2bb9b6fdf
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "318786"
---
# <a name="set-up-segregation-of-duties"></a><span data-ttu-id="f1592-103">Regeln für Aufgabentrennung einrichten</span><span class="sxs-lookup"><span data-stu-id="f1592-103">Set up segregation of duties</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f1592-104">Sie können Regeln einrichten, Aufgaben abzugrenzen, die von unterschiedlichen Benutzern ausgeführt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="f1592-104">You can set up rules to separate tasks that must be performed by different users.</span></span> <span data-ttu-id="f1592-105">Dieses Konzept wird Aufgabentrennung benannt.</span><span class="sxs-lookup"><span data-stu-id="f1592-105">This concept is named segregation of duties.</span></span> <span data-ttu-id="f1592-106">Beispielsweise kann die gleiche Person des Eingangs von Waren bestätigen und Zahlung an den Kreditor nicht verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="f1592-106">For example, you might not want the same person both to acknowledge the receipt of goods and to process payment to the vendor.</span></span> <span data-ttu-id="f1592-107">Aufgabentrennungshilfen reduzieren Sie das Risiko des Betrugs und es auch Hilfsprogrammen, die Sie Fehler oder Unregelmäßigkeiten erkennen.</span><span class="sxs-lookup"><span data-stu-id="f1592-107">Segregation of duties helps you reduce the risk of fraud, and it also helps you detect errors or irregularities.</span></span> <span data-ttu-id="f1592-108">Sie können Aufgabentrennung auch verwenden, um Richtlinien der internen Kontrolle zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="f1592-108">You can also use segregation of duties to enforce internal control policies.</span></span> <span data-ttu-id="f1592-109">Gehen Sie zum Erstellen einer Regel folgendermaßen vor.</span><span class="sxs-lookup"><span data-stu-id="f1592-109">Complete the following procedure to create a rule.</span></span> <span data-ttu-id="f1592-110">Sie müssen ein -Systemadministrator sein, um dieses Verfahren auszuführen.</span><span class="sxs-lookup"><span data-stu-id="f1592-110">You must be a system administrator to complete the procedure.</span></span> <span data-ttu-id="f1592-111">Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist DAT.</span><span class="sxs-lookup"><span data-stu-id="f1592-111">The demo data company used to create this procedure is DAT.</span></span> 

1. <span data-ttu-id="f1592-112">Wechseln Sie zu Systemverwaltung > Sicherheit > Aufgabentrennung > Aufgabentrennungsregeln.</span><span class="sxs-lookup"><span data-stu-id="f1592-112">Go to System administration > Security > Segregation of duties > Segregation of duties rules.</span></span>
2. <span data-ttu-id="f1592-113">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="f1592-113">Click New.</span></span>
3. <span data-ttu-id="f1592-114">Geben Sie im Feld "Name" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="f1592-114">In the Name field, type a value.</span></span>
    * <span data-ttu-id="f1592-115">Namen für Regel eingeben.</span><span class="sxs-lookup"><span data-stu-id="f1592-115">Enter a name for the rule.</span></span>  
4. <span data-ttu-id="f1592-116">Klicken Sie im Feld "Erste Aufgabe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="f1592-116">In the First duty field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="f1592-117">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="f1592-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="f1592-118">Wählen Sie die erste Aufgabe, die mit der Regel gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="f1592-118">Select the first duty that is controlled by the rule.</span></span>  
6. <span data-ttu-id="f1592-119">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="f1592-119">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="f1592-120">Klicken Sie im Feld "Zweite Aufgabe" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="f1592-120">In the Second duty field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="f1592-121">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="f1592-121">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="f1592-122">Wählen Sie die zweite Aufgabe, die mit der Regel gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="f1592-122">Select the second duty that is controlled by the rule.</span></span>  
9. <span data-ttu-id="f1592-123">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="f1592-123">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="f1592-124">Wählen Sie im Feld Schweregrad eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="f1592-124">In the Severity field, select an option.</span></span>
    * <span data-ttu-id="f1592-125">Wählen Sie hier den Schweregrad des Risikos aus, das auftritt, wenn der gleiche Benutzer oder die gleiche Rolle beide Aufgaben ausführt.</span><span class="sxs-lookup"><span data-stu-id="f1592-125">Select the severity of the risk that occurs when the same user or role performs both duties.</span></span>  
11. <span data-ttu-id="f1592-126">Geben Sie im Feld Sicherheitsrisiko einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="f1592-126">In the Security risk field, type a value.</span></span>
    * <span data-ttu-id="f1592-127">Beschreibung des Sicherheitsrisikos eingeben.</span><span class="sxs-lookup"><span data-stu-id="f1592-127">Enter a description of the security risk.</span></span>  
12. <span data-ttu-id="f1592-128">Geben Sie im Feld Sicherheitsbehandlung einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="f1592-128">In the Security mitigation field, type a value.</span></span>
    * <span data-ttu-id="f1592-129">Geben Sie eine Beschreibung der Aktivitäten ein, die Sie nehmen, um das Sicherheitsrisiko zu minimieren.</span><span class="sxs-lookup"><span data-stu-id="f1592-129">Enter a description of the actions that you take to mitigate the security risk.</span></span> <span data-ttu-id="f1592-130">So können Sie das Risiko minimieren, indem Sie detailliertere Überprüfung des Prozesses durchführen, indem Sie einen Monatsverwaltungsreview tätigen oder indem Sie Ressourcen mit anderen Abteilungen freigeben.</span><span class="sxs-lookup"><span data-stu-id="f1592-130">For example, you can mitigate the risk by conducting more detailed reviews of the process, by conducting a monthly managerial review, or by sharing resources with other departments.</span></span>  
13. <span data-ttu-id="f1592-131">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="f1592-131">Click Save.</span></span>

