---
title: Verwalten Sie die Kontoprüfung (IBAN) der internationalen Bankkontonummer
description: Dieses Thema erklärt, wie Sie die internationale Bankkontonummer (IBAN) prüfen.
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 28abef376e8462c9a69dbd8e5033ea799b6a4b3a
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3977814"
---
# <a name="manage-international-bank-account-number-iban-account-validation"></a><span data-ttu-id="70c0a-103">Verwalten Sie die Kontoprüfung (IBAN) der internationalen Bankkontonummer</span><span class="sxs-lookup"><span data-stu-id="70c0a-103">Manage International Bank Account Number (IBAN) account validation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="70c0a-104">Internationale Bankkontonummer (IBAN) Kontoüberprüfung erhöht den Betrag der Prüfung, die  ausgeführt wird, wenn Sie eine IBAN einem Bankkonto hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="70c0a-104">International Bank Account Number (IBAN) validation increases the amount of validation that is done when you add an IBAN to a bank account.</span></span>

<span data-ttu-id="70c0a-105">Informationen zur Struktur der IBAN werden in Microsoft Dynamics 365 Finance gespeichert.</span><span class="sxs-lookup"><span data-stu-id="70c0a-105">Information about the structure of the IBAN is stored in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="70c0a-106">Diese Informationen werden beim erstmaligen Verwenden der IBAN automatisch auf Bankkonten geladen.</span><span class="sxs-lookup"><span data-stu-id="70c0a-106">That information is automatically loaded when you first use the IBAN on bank accounts.</span></span> <span data-ttu-id="70c0a-107">Sie enthält die Länge der IBAN, die Anfangspositionen der Bankkontonummer und die Routingnummer und die Länge der Kontonummer und die Routingnummer.</span><span class="sxs-lookup"><span data-stu-id="70c0a-107">It contains the length of the IBAN, the starting positions of the bank account number and the routing number, and the length of the bank account number and routing number.</span></span>

## <a name="set-up-iban-structures"></a><span data-ttu-id="70c0a-108">Einrichten der IBAN-Struktur</span><span class="sxs-lookup"><span data-stu-id="70c0a-108">Set up IBAN structures</span></span>

1. <span data-ttu-id="70c0a-109">Gehen Sie zu **Bargeld- und Bankverwaltung \> Einrichten \> IBAN-Struktur**.</span><span class="sxs-lookup"><span data-stu-id="70c0a-109">Go to **Cash and bank management \> Setup \> IBAN structures**.</span></span>
2. <span data-ttu-id="70c0a-110">Beachten Sie, dass die IBAN-Strukturen für jedes Land oder jede Region automatisch installiert wurden.</span><span class="sxs-lookup"><span data-stu-id="70c0a-110">Notice that the IBAN structures for each country or region have been set up automatically.</span></span>
3. <span data-ttu-id="70c0a-111">Wenn Sie Strukturen für ein bestimmtes Land oder eine Region anpassen möchten, können Sie sie bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="70c0a-111">If you want to customize the structures for a specific country or region, you can edit them.</span></span>
4. <span data-ttu-id="70c0a-112">Die Strukturdefinitionen sind Teil einer neuen Version.</span><span class="sxs-lookup"><span data-stu-id="70c0a-112">The structure definitions will be a part of each new release.</span></span> <span data-ttu-id="70c0a-113">Sie können das Menü **Rücksetzungsstrukturen** verwenden, um die neuesten Definitionen nach jeder Aktualisierung zu laden.</span><span class="sxs-lookup"><span data-stu-id="70c0a-113">You can use the **Reset structures** menu to load the latest definitions after each update.</span></span>

## <a name="validate-the-iban-structure-in-a-bank-account"></a><span data-ttu-id="70c0a-114">Überprüfen Sie die IBAN-Struktur auf einem Bankkonto</span><span class="sxs-lookup"><span data-stu-id="70c0a-114">Validate the IBAN structure in a bank account</span></span>

1. <span data-ttu-id="70c0a-115">Gehen Sie zu**Bargeld- und Bankverwaltung \> Bankkonten \> Bankkonten**.</span><span class="sxs-lookup"><span data-stu-id="70c0a-115">Go to **Cash and bank management \> Bank accounts \> Bank accounts**.</span></span>
2. <span data-ttu-id="70c0a-116">Bankkonto erstellen.</span><span class="sxs-lookup"><span data-stu-id="70c0a-116">Create a bank account.</span></span>
3. <span data-ttu-id="70c0a-117">Auf dem Inforegister **Zusätzliche Informationen** können Sie eine IBAN-Nummer eingeben.</span><span class="sxs-lookup"><span data-stu-id="70c0a-117">On the **Additional information** FastTab, enter an IBAN.</span></span>

    <span data-ttu-id="70c0a-118">Wenn die Länge der IBAN nicht mit der Länge übereinstimmt, die für jedes Land oder jede Region definiert ist, erhalten Sie eine Warnmeldung.</span><span class="sxs-lookup"><span data-stu-id="70c0a-118">If the length of the IBAN doesn't match the length that is defined for each country or region, you will receive a warning message.</span></span> <span data-ttu-id="70c0a-119">Sie können nicht fortfahren, wenn die Länge der IBAN nicht der Länge in der definierten IBAN-Struktur entspricht.</span><span class="sxs-lookup"><span data-stu-id="70c0a-119">You can't continue if the length of the IBAN doesn't match the length specified in the IBAN structure.</span></span>

    <span data-ttu-id="70c0a-120">Es wird auch geprüft, ob die Bankkontonummer mit dem Teil der IBAN übereinstimmt, die die Bankkontonummer darstellt.</span><span class="sxs-lookup"><span data-stu-id="70c0a-120">The validation also verifies that the bank account number matches the part of the IBAN that represents the bank account number.</span></span> <span data-ttu-id="70c0a-121">Wenn die Kontonummer nicht übereinstimmt, erhalten Sie eine Warnmeldung.</span><span class="sxs-lookup"><span data-stu-id="70c0a-121">If the bank account number doesn't match, you will receive a warning message.</span></span> <span data-ttu-id="70c0a-122">Eine Warnmeldung wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="70c0a-122">This message is only a warning.</span></span> <span data-ttu-id="70c0a-123">Sie können fortfahren, selbst wenn die Kontonummer nicht übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="70c0a-123">You can continue even if the bank account number doesn't match.</span></span>

    <span data-ttu-id="70c0a-124">Es wird auch geprüft, ob die Bankkontonummer mit dem Teil der IBAN übereinstimmt, die die Bankroutingnummer darstellt.</span><span class="sxs-lookup"><span data-stu-id="70c0a-124">The validation also verifies that the bank routing number matches the part of the IBAN that represents the bank routing number.</span></span> <span data-ttu-id="70c0a-125">Die Routingnummer enthält eine Banknummer und häufig eine zusätzliche Bankfiliale.</span><span class="sxs-lookup"><span data-stu-id="70c0a-125">The routing number includes a bank number and often an additional bank branch.</span></span> <span data-ttu-id="70c0a-126">Wenn die Bankroutingnummer nicht übereinstimmt, erhalten Sie eine Warnmeldung.</span><span class="sxs-lookup"><span data-stu-id="70c0a-126">If the bank routing number doesn't match, you will receive a warning message.</span></span> <span data-ttu-id="70c0a-127">Eine Warnmeldung wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="70c0a-127">This message is only a warning.</span></span> <span data-ttu-id="70c0a-128">Sie können fortfahren, selbst wenn die Bankroutingnummer nicht übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="70c0a-128">You can continue even if the bank routing number doesn't match.</span></span>
