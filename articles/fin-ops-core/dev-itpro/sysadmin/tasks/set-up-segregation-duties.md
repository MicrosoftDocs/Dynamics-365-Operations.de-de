---
title: Regeln für Aufgabentrennung einrichten
description: Sie können Regeln einrichten, Aufgaben abzugrenzen, die von unterschiedlichen Benutzern ausgeführt werden müssen.
author: peakerbl
manager: AnnBe
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1c1521d6bbbe12964fef0942fcc4943f12a4360a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562496"
---
# <a name="set-up-segregation-of-duties"></a><span data-ttu-id="fee81-103">Regeln für Aufgabentrennung einrichten</span><span class="sxs-lookup"><span data-stu-id="fee81-103">Set up segregation of duties</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fee81-104">Sie können Regeln einrichten, Aufgaben abzugrenzen, die von unterschiedlichen Benutzern ausgeführt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="fee81-104">You can set up rules to separate tasks that must be performed by different users.</span></span> <span data-ttu-id="fee81-105">Dieses Konzept wird Aufgabentrennung benannt.</span><span class="sxs-lookup"><span data-stu-id="fee81-105">This concept is named segregation of duties.</span></span> <span data-ttu-id="fee81-106">Beispielsweise kann es sein, dass Sie nicht möchten, dass dieselbe Person den Wareneingang bestätigt und sich um die Bezahlung des Lieferanten kümmert.</span><span class="sxs-lookup"><span data-stu-id="fee81-106">For example, you might not want the same person to acknowledge the receipt of goods and to process payment to the vendor.</span></span> <span data-ttu-id="fee81-107">Aufgabentrennungshilfen reduzieren Sie das Risiko des Betrugs und es auch Hilfsprogrammen, die Sie Fehler oder Unregelmäßigkeiten erkennen.</span><span class="sxs-lookup"><span data-stu-id="fee81-107">Segregation of duties helps you reduce the risk of fraud, and it also helps you detect errors or irregularities.</span></span> <span data-ttu-id="fee81-108">Sie können Aufgabentrennung auch verwenden, um Richtlinien der internen Kontrolle zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="fee81-108">You can also use segregation of duties to enforce internal control policies.</span></span> <span data-ttu-id="fee81-109">Gehen Sie zum Erstellen einer Regel folgendermaßen vor.</span><span class="sxs-lookup"><span data-stu-id="fee81-109">Complete the following procedure to create a rule.</span></span> <span data-ttu-id="fee81-110">Sie müssen ein -Systemadministrator sein, um dieses Verfahren auszuführen.</span><span class="sxs-lookup"><span data-stu-id="fee81-110">You must be a system administrator to complete the procedure.</span></span>

1. <span data-ttu-id="fee81-111">Wechseln Sie zu **Systemverwaltung** > **Sicherheit** > **Aufgabentrennung** > **Aufgabentrennungsregeln**.</span><span class="sxs-lookup"><span data-stu-id="fee81-111">Go to **System administration** > **Security** > **Segregation of duties** > **Segregation of duties rules**.</span></span>
2. <span data-ttu-id="fee81-112">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="fee81-112">Click **New**.</span></span>
3. <span data-ttu-id="fee81-113">Geben Sie im Feld **Name** einen Wert für die Regel ein.</span><span class="sxs-lookup"><span data-stu-id="fee81-113">In the **Name** field, type a value for the rule.</span></span>
4. <span data-ttu-id="fee81-114">Klicken Sie im Feld **Erste Aufgabe** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="fee81-114">In the **First duty** field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="fee81-115">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="fee81-115">In the list, find and select the desired record.</span></span> <span data-ttu-id="fee81-116">Wählen Sie die erste Aufgabe, die mit der Regel gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="fee81-116">Select the first duty that is controlled by the rule.</span></span>
6. <span data-ttu-id="fee81-117">Klicken Sie im Feld **Zweite Aufgabe** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="fee81-117">In the **Second duty** field, click the drop-down button to open the lookup.</span></span> 
7. <span data-ttu-id="fee81-118">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="fee81-118">In the list, find and select the desired record.</span></span> <span data-ttu-id="fee81-119">Wählen Sie die zweite Aufgabe, die mit der Regel gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="fee81-119">Select the second duty that is controlled by the rule.</span></span>
10. <span data-ttu-id="fee81-120">Wählen Sie im Feld **Schweregrad** eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="fee81-120">In the **Severity** field, select an option.</span></span> <span data-ttu-id="fee81-121">Wählen Sie hier den Schweregrad des Risikos aus, das auftritt, wenn der gleiche Benutzer oder die gleiche Rolle beide Aufgaben ausführt.</span><span class="sxs-lookup"><span data-stu-id="fee81-121">Select the severity of the risk that occurs when the same user or role performs both duties.</span></span>  
11. <span data-ttu-id="fee81-122">Geben Sie im Feld **Sicherheitsrisiko** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="fee81-122">In the **Security risk** field, type a value.</span></span> <span data-ttu-id="fee81-123">Beschreibung des Sicherheitsrisikos eingeben.</span><span class="sxs-lookup"><span data-stu-id="fee81-123">Enter a description of the security risk.</span></span>  
12. <span data-ttu-id="fee81-124">Geben Sie im Feld **Sicherheitsbehandlung** einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="fee81-124">In the **Security mitigation** field, type a value.</span></span> <span data-ttu-id="fee81-125">Geben Sie eine Beschreibung der Aktivitäten ein, die Sie nehmen, um das Sicherheitsrisiko zu minimieren.</span><span class="sxs-lookup"><span data-stu-id="fee81-125">Enter a description of the actions that you take to mitigate the security risk.</span></span> <span data-ttu-id="fee81-126">So können Sie das Risiko minimieren, indem Sie detailliertere Überprüfung des Prozesses durchführen, indem Sie einen Monatsverwaltungsreview tätigen oder indem Sie Ressourcen mit anderen Abteilungen freigeben.</span><span class="sxs-lookup"><span data-stu-id="fee81-126">For example, you can mitigate the risk by conducting more detailed reviews of the process, by conducting a monthly managerial review, or by sharing resources with other departments.</span></span>     
13. <span data-ttu-id="fee81-127">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="fee81-127">Click **Save**.</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="fee81-128">Die Einhaltung der Regeln für die Aufgabentrennung wird beim Erstellen einer Regel nicht überprüft.</span><span class="sxs-lookup"><span data-stu-id="fee81-128">Compliance with the rules for segregation of duties is not verified when you create a rule.</span></span> <span data-ttu-id="fee81-129">Sie können eine Regel erstellen, die einen Konflikt für vorhandene Rollen erstellt.</span><span class="sxs-lookup"><span data-stu-id="fee81-129">You can create a rule that creates a conflict for existing roles.</span></span> <span data-ttu-id="fee81-130">Bestehende Benutzerrollenzuweisungen können ebenfalls im Widerspruch zur neuen Regel stehen.</span><span class="sxs-lookup"><span data-stu-id="fee81-130">Existing user role assignments can also be in conflict with the new rule.</span></span> <span data-ttu-id="fee81-131">Sie müssen die Einhaltung überprüfen, nachdem Sie eine Regel erstellt oder geändert haben.</span><span class="sxs-lookup"><span data-stu-id="fee81-131">You must validate compliance after you create or modify a rule.</span></span> <span data-ttu-id="fee81-132">Weitere Informationen finden Sie unter [Konflikte bei der Aufgabentrennung erkennen und beheben](identify-resolve-conflicts-segregation-duties.md).</span><span class="sxs-lookup"><span data-stu-id="fee81-132">For more information, see [Identify and resolve conflicts in segregation of duties](identify-resolve-conflicts-segregation-duties.md)</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]