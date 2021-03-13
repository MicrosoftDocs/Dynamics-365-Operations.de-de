---
title: Eine Quellensteuerzahlung erstellen
description: Die Einzelvorgangsprozedur zur Quellensteuerzahlung gleicht Quellensteuersalden von Kreditorenkonten auf Quellensteuerkonten aus, und sie werden für einen angegebenen Zeitraum gegen das Quellensteuersteuerverrechnungskonto gebucht. In diesem Thema werden die Schritte zum Einrichten einer Quellensteuerzahlung aufgeführt.
author: roschlom
manager: AnnBe
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: e522711340b663bd849825b3d4dd2b7e78e4737c
ms.sourcegitcommit: 630a0b3f800f36ced49b79156dd52132904fef75
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2021
ms.locfileid: "5060742"
---
# <a name="create-a-withholding-tax-payment"></a><span data-ttu-id="fb92e-104">Eine Quellensteuerzahlung erstellen</span><span class="sxs-lookup"><span data-stu-id="fb92e-104">Create a withholding tax payment</span></span>

<span data-ttu-id="fb92e-105">Die Einzelvorgangsprozedur zur Quellensteuerzahlung gleicht Quellensteuersalden von Kreditorenkonten auf Quellensteuerkonten aus, und sie werden für einen angegebenen Zeitraum gegen das Quellensteuersteuerverrechnungskonto gebucht.</span><span class="sxs-lookup"><span data-stu-id="fb92e-105">The Withholding tax payment job procedure settles withholding tax balances from Accounts payable on withholding tax accounts, and offsets them to the withholding tax settlement account for a given period.</span></span> <span data-ttu-id="fb92e-106">In diesem Thema werden die Schritte zum Einrichten einer Quellensteuerzahlung aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="fb92e-106">This topic lists the steps for setting up a withholding tax payment.</span></span>

> [!NOTE] 
> <span data-ttu-id="fb92e-107">Die Quellensteuerverrechnung (von Debitorenkonten) wird bei der Berechnung einer Quellensteuerzahlung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="fb92e-107">Withholding tax offset (from accounts receivable) is not taken into account when a withholding tax payment is calculated.</span></span>

1. <span data-ttu-id="fb92e-108">Rufen Sie **Navigationsbereich > Module > Steuer > Erklärungen > Quellensteuer > Quellensteuerzahlung** auf.</span><span class="sxs-lookup"><span data-stu-id="fb92e-108">Go to **Navigation pane > Modules > Tax > Declarations > Withholding tax > Withholding tax payment**.</span></span>
2. <span data-ttu-id="fb92e-109">Klicken Sie im Feld **Abrechnungszeitraum** auf die Dropdown-Schaltfläche, um die Suche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="fb92e-109">In the **Settlement period** field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="fb92e-110">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="fb92e-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="fb92e-111">Geben Sie im Feld **Von Datum** ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="fb92e-111">In the **From date** field, enter a date.</span></span>
5. <span data-ttu-id="fb92e-112">Geben Sie im Feld **Transaktionsdatum** ein Datum ein.</span><span class="sxs-lookup"><span data-stu-id="fb92e-112">In the **Transaction date** field, enter a date.</span></span>
6. <span data-ttu-id="fb92e-113">Wählen Sie **Aktualisieren** aus, um den Quellensteuerzahlungsbeleg auf das Quellensteuerverrechnungskonto zu buchen.</span><span class="sxs-lookup"><span data-stu-id="fb92e-113">Select **Update** to post withholding tax payment voucher to the withholding tax settlement account.</span></span>
7. <span data-ttu-id="fb92e-114">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="fb92e-114">Click **OK**.</span></span>

![Parameter für die Quellensteuerzahlung](media/withholding-tax-payment.png)
