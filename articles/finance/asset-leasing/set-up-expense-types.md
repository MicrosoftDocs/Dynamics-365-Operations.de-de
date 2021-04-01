---
title: Ausgabentypen einrichten
description: In diesem Thema wird erläutert, wie Sie in Ausgabenarten im Anlageleasing einrichten.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2019-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 1538826f140393eec59be9ff4df5242d5ced9d8f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249748"
---
# <a name="set-up-expense-types"></a><span data-ttu-id="54103-103">Ausgabentypen einrichten</span><span class="sxs-lookup"><span data-stu-id="54103-103">Set up expense types</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="54103-104">In diesem Thema wird erläutert, wie Sie in Ausgabenarten im Anlageleasing einrichten.</span><span class="sxs-lookup"><span data-stu-id="54103-104">This topic explains how to set up expense types in Asset leasing.</span></span> <span data-ttu-id="54103-105">Kosten, die nicht im Zahlungsplan enthalten sind, werden als *Ausgabenkosten* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="54103-105">Costs that aren't represented by the payment schedule are known as *expense costs*.</span></span> <span data-ttu-id="54103-106">Beispiele für diese Kosten sind Grundsteuern, Wartungskosten für Gemeinschaftsräume und Versicherungskosten.</span><span class="sxs-lookup"><span data-stu-id="54103-106">Examples of these costs include property taxes, common area maintenance costs, and insurance expenses.</span></span>

## <a name="add-an-administrative-expense-type"></a><span data-ttu-id="54103-107">Einen Verwaltungsausgabentyp hinzufügen</span><span class="sxs-lookup"><span data-stu-id="54103-107">Add an administrative expense type</span></span>

1. <span data-ttu-id="54103-108">Wechseln Sie zu **Anlagenleasing \> Einrichtung \> Ausgabentypen**.</span><span class="sxs-lookup"><span data-stu-id="54103-108">Go to **Asset leasing \> Setup \> Expense types**.</span></span>
2. <span data-ttu-id="54103-109">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="54103-109">Select **New**.</span></span>
3. <span data-ttu-id="54103-110">Geben Sie in die entsprechenden Felder den neuen Ausgabentyp und eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="54103-110">In the appropriate fields, enter the new expense type and a description.</span></span>

## <a name="assign-accounts-to-administrative-costs"></a><span data-ttu-id="54103-111">Konten den Verwaltungskosten zuweisen</span><span class="sxs-lookup"><span data-stu-id="54103-111">Assign accounts to administrative costs</span></span>

<span data-ttu-id="54103-112">Als Nächstes sollten Sie den Ausgabentypen Konten zuordnen.</span><span class="sxs-lookup"><span data-stu-id="54103-112">Next, you should associate accounts with the expense types.</span></span> <span data-ttu-id="54103-113">Diese Konten werden belastet, wenn Einträge des Ausgabenplans gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="54103-113">These accounts will be debited when expense schedule entries are posted.</span></span> <span data-ttu-id="54103-114">Das Gegenkonto ist auf den **Zahlungsplan für Nebenkosten beim Leasing**-Zeilen auf jedem Mietvertrag angegeben.</span><span class="sxs-lookup"><span data-stu-id="54103-114">The offset account is specified on the **Executory costs payment schedule** lines on each lease.</span></span>

1. <span data-ttu-id="54103-115">Wechseln Sie zu **Anlagenleasing \> Einrichtung \> Anlagenleasing-Parameter**.</span><span class="sxs-lookup"><span data-stu-id="54103-115">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="54103-116">Wählen Sie auf der **Konten**-Registerkarte auf dem **Nebenkosten beim Leasing Ausführungskosten**-Inforegister im **Ausgabentyp**-Feld den Ausgabentyp aus.</span><span class="sxs-lookup"><span data-stu-id="54103-116">On the **Accounts** tab, on the **Executory costs** FastTab, in the **Expense type** field, select the expense type.</span></span>
3. <span data-ttu-id="54103-117">Wählen Sie **Hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="54103-117">Select **Add**.</span></span>
4. <span data-ttu-id="54103-118">Wählen Sie im **Buchtyp**-Feld den Buchtyp aus, der mit den Verwaltungskosten verknüpft werden soll.</span><span class="sxs-lookup"><span data-stu-id="54103-118">In the **Book type** field, select the book type to link to the administrative costs.</span></span>

    > [!NOTE]
    > <span data-ttu-id="54103-119">Mehrere Bucharten können mit demselben Ausgabenkonto verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="54103-119">Multiple book types can be linked to the same expense account.</span></span>

5. <span data-ttu-id="54103-120">Geben Sie im Feld **Kontocode** an, auf welche Mietverträge das Buch angewendet werden soll:</span><span class="sxs-lookup"><span data-stu-id="54103-120">In the **Account code** field, specify which leases the book should be applied to:</span></span>

    - <span data-ttu-id="54103-121">**Alle** – Das Buch für alle Mietverträge anwenden.</span><span class="sxs-lookup"><span data-stu-id="54103-121">**All** – Apply the book to all leases.</span></span>
    - <span data-ttu-id="54103-122">**Gruppe** – Das Buch auf eine bestimmte Gruppe von Mietverträgen anwenden.</span><span class="sxs-lookup"><span data-stu-id="54103-122">**Group** – Apply the book to a specific group of leases.</span></span>
    - <span data-ttu-id="54103-123">**Tabelle** – Das Buch für bestimmte Mietverträge anwenden.</span><span class="sxs-lookup"><span data-stu-id="54103-123">**Table** – Apply the book to specific leases.</span></span>

6. <span data-ttu-id="54103-124">Wenn Sie **Gruppe** oder **Tabelle** im Feld **Kontocode** gewählt haben, wählen Sie eine Kontonummer oder Gruppennummer im Feld **Konto-/Gruppennummer** aus.</span><span class="sxs-lookup"><span data-stu-id="54103-124">If you selected **Group** or **Table** in the **Account code** field, select an account number or group number in the **Account/Group number** field.</span></span>
7. <span data-ttu-id="54103-125">Wählen Sie in den entsprechenden Feldern das Hauptkonto für Finanzierungsleasing und das Hauptkonto für Ausrüstungs-Leasingvertrag aus.</span><span class="sxs-lookup"><span data-stu-id="54103-125">In the appropriate fields, select the finance lease main account and the operating lease main account.</span></span>

<span data-ttu-id="54103-126">Wenn Sie diese Schritte ausgeführt haben, können Sie Ausgaben über **Zahlungsplan für Nebenkosten beim Leasing**-Zeilen auf der **Mietvertragsdetails**-Seite eines ausgewählten Mietvertrags hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="54103-126">When you've completed these steps, you can add expenses through the **Executory costs payment schedule** lines on the **Lease details** page of a selected lease.</span></span> <span data-ttu-id="54103-127">Alternativ können Sie beim Erstellen eines neuen Mietvertrags Kosten hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="54103-127">Alternatively, you can add expenses when you create a new lease.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]