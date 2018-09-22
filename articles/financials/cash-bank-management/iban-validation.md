---
title: "Verwalten Sie die Kontoprüfung (IBAN) der internationalen Bankkontonummer"
description: "Dieses Thema erklärt, wie Sie die internationale Bankkontonummer (IBAN) prüfen."
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.translationtype: HT
ms.sourcegitcommit: 98ed3378ab05c0c69c9e5b2a82310113a81c2264
ms.openlocfilehash: e091aab70a98e0f4b96c41c1ee48926947539105
ms.contentlocale: de-de
ms.lasthandoff: 08/31/2018

---

# <a name="manage-international-bank-account-number-iban-account-validation"></a><span data-ttu-id="bc94a-103">Verwalten Sie die Kontoprüfung (IBAN) der internationalen Bankkontonummer</span><span class="sxs-lookup"><span data-stu-id="bc94a-103">Manage International Bank Account Number (IBAN) account validation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bc94a-104">Internationale Bankkontonummer (IBAN) Kontoüberprüfung erhöht den Betrag der Prüfung, die  ausgeführt wird, wenn Sie eine IBAN einem Bankkonto hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="bc94a-104">International Bank Account Number (IBAN) account validation increases the amount of validation that is done when you add an IBAN to a bank account.</span></span>

<span data-ttu-id="bc94a-105">Die Struktur der IBAN wird in Microsoft Dynamics 365 for Finance and Operations gespeichert und automatisch beim Verwenden der IBAN auf Bankkonten geladen.</span><span class="sxs-lookup"><span data-stu-id="bc94a-105">The structure of the IBAN is stored in Microsoft Dynamics 365 for Finance and Operation, and is automatically loaded when you first use the IBAN on bank accounts.</span></span> <span data-ttu-id="bc94a-106">Die Kontonummer ist Teil der Struktur, die für eine IBAN-Nummer definiert wird.</span><span class="sxs-lookup"><span data-stu-id="bc94a-106">The bank account number is part of the structure defined for an IBAN number.</span></span> <span data-ttu-id="bc94a-107">Basierend auf dieser Struktur wenn die Position und die Länge der Kontonummer der IBAN nicht mit der Position übereinstimmen, die in der Struktur für jedes Land oder jede Region definiert wird, werden Warnungsnachrichten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bc94a-107">Based on that structure, if the position and length of the account number in the IBAN don't match the position that is defined in the structure for each country or region, you will receive warning messages.</span></span>

## <a name="set-up-iban-structures"></a><span data-ttu-id="bc94a-108">Einrichten der IBAN-Struktur</span><span class="sxs-lookup"><span data-stu-id="bc94a-108">Set up IBAN structures</span></span>

1. <span data-ttu-id="bc94a-109">Gehen Sie zu **Bargeld- und Bankverwaltung \> Einrichten \> IBAN-Struktur**.</span><span class="sxs-lookup"><span data-stu-id="bc94a-109">Go to **Cash and bank management \> Setup \> IBAN structures**.</span></span>
2. <span data-ttu-id="bc94a-110">Beachten Sie, dass die IBAN-Strukturen für jedes Land oder jede Region automatisch installiert wurden.</span><span class="sxs-lookup"><span data-stu-id="bc94a-110">Notice that the IBAN structures for each country or region have been set up automatically.</span></span>
3. <span data-ttu-id="bc94a-111">Wenn Sie Strukturen für ein bestimmtes Land oder eine Region anpassen möchten, können Sie sie bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="bc94a-111">If you must customize the structures for a specific country or region, you can edit them.</span></span>
4. <span data-ttu-id="bc94a-112">Die Strukturdefinitionen sind Teil einer neuen Version.</span><span class="sxs-lookup"><span data-stu-id="bc94a-112">The structure definitions will be a part of each new release.</span></span> <span data-ttu-id="bc94a-113">Sie können das Menü **Rücksetzungsstrukturen** verwenden, um die neuesten Definitionen nach jeder Aktualisierung zu laden.</span><span class="sxs-lookup"><span data-stu-id="bc94a-113">You can use the **Reset structures** menu to load the latest definitions after each update.</span></span>

## <a name="validate-the-iban-structure-in-a-bank-account"></a><span data-ttu-id="bc94a-114">Überprüfen Sie die IBAN-Struktur auf einem Bankkonto</span><span class="sxs-lookup"><span data-stu-id="bc94a-114">Validate the IBAN structure in a bank account</span></span>

1. <span data-ttu-id="bc94a-115">Gehen Sie zu**Bargeld- und Bankverwaltung \> Bankkonten \> Bankkonten**.</span><span class="sxs-lookup"><span data-stu-id="bc94a-115">Go to **Cash and bank management \> Bank accounts \> Bank accounts**.</span></span>
2. <span data-ttu-id="bc94a-116">Bankkonto erstellen.</span><span class="sxs-lookup"><span data-stu-id="bc94a-116">Create a bank account.</span></span>
3. <span data-ttu-id="bc94a-117">Auf dem Inforegister **Zusätzliche Informationen** können Sie eine IBAN-Nummer eingeben.</span><span class="sxs-lookup"><span data-stu-id="bc94a-117">On the **Additional information** FastTab, enter an IBAN.</span></span>

    <span data-ttu-id="bc94a-118">Basierend auf dieser Struktur wenn die Position und die Länge der Kontonummer der IBAN nicht mit der Position übereinstimmen, die in der Struktur für jedes Land oder jede Region definiert wird, werden Warnungsnachrichten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bc94a-118">If the position and length of the account number in the IBAN don't match the position that is defined in the structure for each country or region, you receive a message.</span></span> <span data-ttu-id="bc94a-119">Sie können nicht fortfahren, wenn die Länge der IBAN nicht der Länge in der IBAN-Struktur entspricht.</span><span class="sxs-lookup"><span data-stu-id="bc94a-119">You can't continue if the length of the IBAN doesn't match the length in the IBAN structure.</span></span>

    <span data-ttu-id="bc94a-120">Es wird auch geprüft, ob die Bankkontonummer mit dem Teil der IBAN übereinstimmt, die die Bankkontonummer darstellt.</span><span class="sxs-lookup"><span data-stu-id="bc94a-120">The validation also verifies that the bank account number matches the part of the IBAN that represents the bank account number.</span></span> <span data-ttu-id="bc94a-121">Wenn die Kontonummer nicht übereinstimmt, erhalten Sie eine Warnmeldung.</span><span class="sxs-lookup"><span data-stu-id="bc94a-121">If the bank account number doesn't match, you receive a warning message.</span></span> <span data-ttu-id="bc94a-122">Eine Warnmeldung wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bc94a-122">This message is only a warning.</span></span> <span data-ttu-id="bc94a-123">Sie können fortfahren, selbst wenn die Kontonummer nicht übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="bc94a-123">You can continue even if the bank account number doesn't match.</span></span>

