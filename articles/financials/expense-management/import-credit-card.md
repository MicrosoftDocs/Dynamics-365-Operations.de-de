---
title: Kreditkartenbuchungen importieren und verwalten
description: "In diesem Thema wird erläutert, wie ausgabenbezogenen Kreditkartenbuchungen importiert und verwaltet werden. Diese Transaktionen können so eingerichtet werden, dass Sie automatische nach einem sich wiederholenden Zeitplan importiert werden sollen, oder Sie können die Buchungen nach Bedarf manuell importieren."
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: knelson
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e640c9e44add5599be4a2e381b4ffd81f212889c
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="import-and-maintain-credit-card-transactions"></a><span data-ttu-id="79b5c-104">Kreditkartenbuchungen importieren und verwalten</span><span class="sxs-lookup"><span data-stu-id="79b5c-104">Import and maintain credit card transactions</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="79b5c-105">Ausgabenbezogenen Kreditkartenbuchungen können eingerichtet werden, damit sie automatisch auf wiederkehrender Basis die Daten importieren.</span><span class="sxs-lookup"><span data-stu-id="79b5c-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="79b5c-106">Alternativ können die Buchungen manuell importiert werden, wenn diese benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="79b5c-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="79b5c-107">Die Kreditkartentransaktionen werden über Kreditkartenbuchungs-Entität importiert.</span><span class="sxs-lookup"><span data-stu-id="79b5c-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

<span data-ttu-id="79b5c-108">Weitere Informationen zu den Daten-Entitäten finden Sie unter [Daten-Entitäten](../../dev-itpro/data-entities/data-entities.md).</span><span class="sxs-lookup"><span data-stu-id="79b5c-108">For more information about data entities, see [Data entities](../../dev-itpro/data-entities/data-entities.md).</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="79b5c-109">Kreditkartenbuchungen importieren</span><span class="sxs-lookup"><span data-stu-id="79b5c-109">Import credit card transactions</span></span>

1. <span data-ttu-id="79b5c-110">Wählen Sie auf der Seite **Kreditkartenbuchungen** **Buchungen importieren** aus.</span><span class="sxs-lookup"><span data-stu-id="79b5c-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="79b5c-111">Wenn Sie die Datenverwaltung zum ersten Mal öffnen, muss das System die Liste der Datenentitäten aktualisieren, bevor Sie den Vorgang fortsetzen können.</span><span class="sxs-lookup"><span data-stu-id="79b5c-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="79b5c-112">Geben Sie im Feld **Name** ggf. eine kurze Beschreibung des Import-Vorgangs ein.</span><span class="sxs-lookup"><span data-stu-id="79b5c-112">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="79b5c-113">Im Feld **Quelldatenformat** wählen Sie das Format der Datei aus, die die zu importierende Kreditkartentranskation enthält.</span><span class="sxs-lookup"><span data-stu-id="79b5c-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="79b5c-114">Wählen Sie **Hochladen** aus und anschließend "Suchen" und wählen die Datei aus, die importiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="79b5c-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="79b5c-115">Nachdem die Datei hochgeladen wurde, überprüfen Sie die Zuordnung der Kreditkartenbuchungsdatei und die Spalten der Kreditkartenbuchungsdatenentität, indem Sie den Link auswählen **Zuordnung anzeigen** auf der Kachel.</span><span class="sxs-lookup"><span data-stu-id="79b5c-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="79b5c-116">Beim Auftreten von Zuordnungsfehlern oder wenn Sie die Verteilung ändern möchten, nehmen Sie die Registerkarte **Zuordnungsvisualisierung** oder **Zuordnungsdetails**.</span><span class="sxs-lookup"><span data-stu-id="79b5c-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="79b5c-117">Um die Kreditkartenbuchungen zu automatisieren, wählen Sie **Erstellen von sich wiederholenden Dateneneinzelvorgängen** aus.</span><span class="sxs-lookup"><span data-stu-id="79b5c-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="79b5c-118">Sie können anschließend die Wiederholung festlegen, um festzulegen, wie oft Kreditkartenbuchungen importiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="79b5c-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="79b5c-119">Klicken Sie abschließend auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="79b5c-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="79b5c-120">Um die ausgewählte Datei nun zu importieren, wählen Sie **Importieren** aus.</span><span class="sxs-lookup"><span data-stu-id="79b5c-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="79b5c-121">Wenn Fehler beim Import auftreten, können Sie das Ausführungsprotokoll oder die Bereitstellungsdaten anzeigen, um die Fehler anzuzeigen, die Sie korrigieren möchten, um einen erfolgreichen Import sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="79b5c-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="79b5c-122">Wenn Sie mehr als ein Dateiformat importieren möchten, müssen Sie separate Importeinzelvorgänge für jeden Formattyp erstellen.</span><span class="sxs-lookup"><span data-stu-id="79b5c-122">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="79b5c-123">Kreditkartenbuchungen für ausgeschiedenen Mitarbeiter neu zuweisen.</span><span class="sxs-lookup"><span data-stu-id="79b5c-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="79b5c-124">Nachdem ein Mitarbeiterdatensatz beendet ist, wird das Konto Active Directory-Domain Services (AD DS) des Mitarbeiters deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="79b5c-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="79b5c-125">Allerdings gibt es möglicherweise aktive Kreditkartenbuchungen, die noch bezahlt und erstattet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="79b5c-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="79b5c-126">Sie können nun die Seite **Kreditkartenbuchungen** verwenden, um den Mitarbeiter für eine Kreditkartenbuchung neu zuzuweisen, wo der zugeordnete Mitarbeiter ausgeschieden ist.</span><span class="sxs-lookup"><span data-stu-id="79b5c-126">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="79b5c-127">Wählen Sie mindestens eine Kreditkartenbuchung aus, und wählen Sie dann **Weisen Sie Buchungen neu zu** aus.</span><span class="sxs-lookup"><span data-stu-id="79b5c-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="79b5c-128">Sie können dann einen anderen Mitarbeiter auswählen, dem die Kreditkartenbuchungen zugewiesen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="79b5c-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="79b5c-129">Nachdem die Kreditkartenbuchung neu zugewiesen wurde, kann die Buchung für eine Spesenabrechnung ausgewählt werden und über den regulären Prozess für Spesenabrechnungsrückerstattung bezahlt werden.</span><span class="sxs-lookup"><span data-stu-id="79b5c-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>

