---
title: Debitorenkreditgruppen
description: Dieses Thema enthält Informationen zu Debitorenkreditgruppen.
author: mikefalkner
manager: AnnBe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 76b1e93d562e66cb8d4c5819a749459ea8783b1e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5237541"
---
# <a name="customer-credit-groups"></a><span data-ttu-id="ba4ef-103">Debitorenkreditgruppen</span><span class="sxs-lookup"><span data-stu-id="ba4ef-103">Customer credit groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ba4ef-104">Sie können Debitorengruppen mit geteilten Kreditlimit definieren.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-104">You can define groups of customers who have a shared credit limit.</span></span> <span data-ttu-id="ba4ef-105">Das auf dem Debitorenrechnungskonto festgelegte individuelle Kreditlimit wird ebenfalls berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-105">The individual credit limit that is defined on the customer invoice account is also considered.</span></span>

<span data-ttu-id="ba4ef-106">Mitglieder einer Debitorenkreditgruppe können aus verschiedenen juristischen Personen ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-106">Members of a customer credit group can be selected from different legal entities.</span></span> <span data-ttu-id="ba4ef-107">Wenn Sie der Liste der Debitoren in der Debitorenkreditgruppe einen Debitor hinzufügen, wird das Ablaufdatum des Kreditlimits für jeden Debitor in das Ablaufdatum geändert, das der Gruppe zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-107">When you add a customer to the list of customers in the customer credit group, the expiration date of the credit limit for each customer is changed to the expiration date that is assigned to the group.</span></span>

<span data-ttu-id="ba4ef-108">Sie können Debitorengruppen auf der Seite **Debitorenkreditgruppen** einrichten (**Kreditmanagement \> Debitorenkreditgruppen \> Debitorenkreditgruppen**).</span><span class="sxs-lookup"><span data-stu-id="ba4ef-108">You can set up customer credit groups on the **Customer credit groups** page (**Credit management \> Customer credit groups \> Customer credit groups**).</span></span>

1. <span data-ttu-id="ba4ef-109">Geben Sie in den Feldern **Gruppennummer** und **Beschreibung** einen Bezeichner und eine Beschreibung für die Gruppe ein.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-109">In the **Group number** and **Description** fields, enter an identifier and description for the group.</span></span>
2. <span data-ttu-id="ba4ef-110">Geben Sie in die Felder **Kreditlimit** und **Währung** das Kreditlimit und die Währung ein, die verwendet werden sollen, wenn das System das Kreditlimit für ein Mitglied der Gruppe überprüft.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-110">In the **Credit limit** and **Currency** fields, enter the credit limit and currency that should be used when the system checks the credit limit for any member of the group.</span></span>
3. <span data-ttu-id="ba4ef-111">Geben Sie im Feld **Kreditlimit bis Datum** das Datum ein, an dem das Kreditlimit abläuft.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-111">In the **Credit limit to date** field, enter the date when the credit limit expires.</span></span> <span data-ttu-id="ba4ef-112">Die Kreditorenkreditgruppen müssen ein Ablaufdatum haben.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-112">Customer credit groups must have an expiration date.</span></span>

<span data-ttu-id="ba4ef-113">Nachdem Sie eine Kreditorenkreditgruppe eingerichtet haben, können Sie Kreditoren hinzufügen, indem Sie deren juristische Person und Kreditorenkonto-ID angeben.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-113">After you've finished setting up a customer credit group, you can add customers to it by specifying their legal entity and customer account ID.</span></span> <span data-ttu-id="ba4ef-114">Wenn Sie einer Kreditorenkreditgruppe einen neuen Kreditor hinzufügen, sucht das System unter allen juristischen Personen nach demselben Kreditorenkonto und fordert Sie auf, es der Kreditorenkreditgruppe hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-114">When you add a new customer to a customer credit group, the system searches for the same customer account across all legal entities and prompts you to add it to the customer credit group.</span></span>

<span data-ttu-id="ba4ef-115">Verwenden Sie das Menü **Saldenrückblick**, um die Details des Saldenrückblicks für alle Rechnungskreditoren in einer Kreditorenkreditgruppe anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-115">Use the **Aged balances** menu to view the details of the aging balance for all invoice customers in a customer credit group.</span></span> <span data-ttu-id="ba4ef-116">Die Seite **Saldenrückblick** zeigt eine Zusammenfassung der Saldenrückblicke für die Rechnungskreditorenkonten.</span><span class="sxs-lookup"><span data-stu-id="ba4ef-116">The **Aging balance** page shows a summary of the aged balances for the invoice customer accounts.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]