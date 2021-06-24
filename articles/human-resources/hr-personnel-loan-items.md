---
title: Artikel verwalten, die an Arbeitskräfte ausgeliehen werden
description: Ausleihartikel sind Datensätze, die Managern helfen, die physischen Artikel zu verfolgen, die Ihr Unternehmen an Arbeitskräfte ausleiht.
author: andreabichsel
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmLoanItem, HcmLoanType, HcmPersonLoan, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 3581
ms.assetid: b14bdddb-f10e-4619-9f91-8c88439da862
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: e4109762a2db3114ad66882092d6729dd9b08364
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "6190207"
---
# <a name="manage-items-that-are-lent-to-workers"></a><span data-ttu-id="299eb-103">Artikel verwalten, die an Arbeitskräfte ausgeliehen werden</span><span class="sxs-lookup"><span data-stu-id="299eb-103">Manage items that are lent to workers</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="299eb-104">Ausleihartikel sind Datensätze, die Managern helfen, die physischen Artikel zu verfolgen, die Ihr Unternehmen an Arbeitskräfte ausleiht.</span><span class="sxs-lookup"><span data-stu-id="299eb-104">Loan items are records that help managers track the physical items that your company lends to its workers.</span></span> 

<span data-ttu-id="299eb-105">Einige Beispiele von Artikeln, die Unternehmen an Arbeitskräfte verleihen können, sind in der folgenden Liste enthalten:</span><span class="sxs-lookup"><span data-stu-id="299eb-105">The following points list examples of items that a company might lend to workers:</span></span>
-   <span data-ttu-id="299eb-106">Mobiltelefone</span><span class="sxs-lookup"><span data-stu-id="299eb-106">Mobile telephones</span></span>
-   <span data-ttu-id="299eb-107">Kraftfahrzeuge</span><span class="sxs-lookup"><span data-stu-id="299eb-107">Automobiles</span></span>
-   <span data-ttu-id="299eb-108">Computer und Peripheriegeräte</span><span class="sxs-lookup"><span data-stu-id="299eb-108">Computer equipment</span></span>

<span data-ttu-id="299eb-109">Jeder physische Artikel muss einen entsprechenden Ausleihartikel haben.</span><span class="sxs-lookup"><span data-stu-id="299eb-109">Each physical item must have a corresponding loan item.</span></span> <span data-ttu-id="299eb-110">Jeder Ausleihartikel-Datensatz beschreibt, was ausgeliehen wird, wer für das Ausleihen zuständig ist und die Anzahl von Tage, die der Artikel ausgeliehen werden kann.</span><span class="sxs-lookup"><span data-stu-id="299eb-110">Each loan item record should describe what is being loaned, who is responsible for the loan, and the number of days the item can loaned to a worker.</span></span> <span data-ttu-id="299eb-111">Sie können mehrere Ausleihartikel, wie Schlüssel, Zugangsberechtigungskarten oder Uniformen, gleichzeitig erstellen.</span><span class="sxs-lookup"><span data-stu-id="299eb-111">You can create multiple loan items, for items such as keys, access cards or uniforms, at the same time.</span></span> 

<span data-ttu-id="299eb-112">Erfassen Sie beim Ausleihen eines Artikels das Datum der Ausleihe und das geplante Rückgabedatum.</span><span class="sxs-lookup"><span data-stu-id="299eb-112">When loaning an item, enter the date that the item was loaned, and the planned return date.</span></span> <span data-ttu-id="299eb-113">Geben Sie bei der Rückgabe des Artikels das tatsächliche Rückgabedatum ein.</span><span class="sxs-lookup"><span data-stu-id="299eb-113">When the item is returned, enter the actual return date.</span></span>

<span data-ttu-id="299eb-114">Mitarbeiter können die Datensätze der Artikel anzeigen, die ihnen über den Arbeitsbereich "Mitarbeiter-Self-Service" ausgeliehen wurden.</span><span class="sxs-lookup"><span data-stu-id="299eb-114">Employees can view the records of the items that have been loaned to them using the Employee self-service workspace.</span></span> <span data-ttu-id="299eb-115">Sie können die vorhandenen Datensätze auch bearbeiten oder neuen Ausleihartikel eingeben, wenn sie weitere physikalische Artikel eingegangen sind.</span><span class="sxs-lookup"><span data-stu-id="299eb-115">They can also edit the existing records or enter new loan items, if they've received additional physical items.</span></span>  <span data-ttu-id="299eb-116">Workflow kann so eingerichtet werden, dass Änderungen für die neuen oder vorhandenen Ausleihartikeln durch einen Genehmigungsprozess weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="299eb-116">Workflow can be set up to route changes to new or existing loan items through an approval process.</span></span> 

<span data-ttu-id="299eb-117">Manager können ausgeliehene Artikel für ihre direkten Berichte anzeigen.</span><span class="sxs-lookup"><span data-stu-id="299eb-117">Managers can view loaned items for their direct reports.</span></span> <span data-ttu-id="299eb-118">Sie können auch Berechtigung gewähren, um neue Ausleihartikeln im Auftrag ihrer Mitarbeiter hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="299eb-118">They can also be granted permission to add new loan items on behalf of their employees.</span></span>

##  <a name="account-for-lost-or-misplaced-loan-items"></a><span data-ttu-id="299eb-119">Konto für verlorene oder verlegte Ausleihartikel</span><span class="sxs-lookup"><span data-stu-id="299eb-119">Account for lost or misplaced loan items</span></span>

<span data-ttu-id="299eb-120">Wenn ein Artikel beschädigt oder verlegt wurde, geben Sie einen fiktive Rückgabedatensatz ein.</span><span class="sxs-lookup"><span data-stu-id="299eb-120">If an item becomes damaged or misplaced, enter a fictitious return record.</span></span> <span data-ttu-id="299eb-121">Anschließend können Sie den Artikel entweder löschen oder im Überblick behalten und die Beschreibung ändern, um anzugeben, dass der Artikel nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="299eb-121">Then either delete the item or keep it in the overview and change the description to indicate that the item is not available.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="299eb-122">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="299eb-122">Additional resources</span></span>

[<span data-ttu-id="299eb-123">Personalverwaltung</span><span class="sxs-lookup"><span data-stu-id="299eb-123">Human resources</span></span>](index.md)





[!INCLUDE[footer-include](../includes/footer-banner.md)]