---
title: Sie können aus Abstimmungsgründen nur das Hauptkonto als Habenkonto hinzufügen
description: Wenn Sie in der Transportverwaltung einen Abstimmungsgrund einrichten, können Sie nur das Hauptkonto als Habenkonto hinzufügen.
author: Henrikan
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: TMSFBDetailReconcile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 708081370b27fd51ef9a2329d8392f4515353dcb
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026527"
---
# <a name="you-can-add-only-the-main-account-as-the-credit-account-for-reconciliation-reasons"></a><span data-ttu-id="d4e98-103">Sie können aus Abstimmungsgründen nur das Hauptkonto als Habenkonto hinzufügen</span><span class="sxs-lookup"><span data-stu-id="d4e98-103">You can add only the main account as the credit account for reconciliation reasons</span></span>

<span data-ttu-id="d4e98-104">KB-Nummer: 4603538</span><span class="sxs-lookup"><span data-stu-id="d4e98-104">KB number: 4603538</span></span>

## <a name="symptoms"></a><span data-ttu-id="d4e98-105">Symptome</span><span class="sxs-lookup"><span data-stu-id="d4e98-105">Symptoms</span></span>

<span data-ttu-id="d4e98-106">Wenn Sie in der Transportverwaltung einen Abstimmungsgrund einrichten, können Sie nur das Hauptkonto als Habenkonto hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d4e98-106">When you set up a reconciliation reason in Transportation management, you can add only the main account as the credit account.</span></span> <span data-ttu-id="d4e98-107">Sie können keine Kostenstelle oder eine andere Dimension als Habenkonto hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d4e98-107">You can't add a cost center or any other dimension as the credit account.</span></span> <span data-ttu-id="d4e98-108">Über das Sollkonto können Sie jedoch andere Dimensionen auswählen.</span><span class="sxs-lookup"><span data-stu-id="d4e98-108">However, the debit account lets you select other dimensions.</span></span>

## <a name="resolution"></a><span data-ttu-id="d4e98-109">Lösung</span><span class="sxs-lookup"><span data-stu-id="d4e98-109">Resolution</span></span>

<span data-ttu-id="d4e98-110">Wenn die Abstimmung nicht zur Bezahlung des Kreditors, sondern zur Gutschrift auf ein bestimmtes Hauptkonto durchgeführt wird, können Sie beim Einrichten des Abstimmungsgrunds keine finanzielle Dimension für das Habenkonto auswählen.</span><span class="sxs-lookup"><span data-stu-id="d4e98-110">If the reconciliation isn't done to pay the vendor but to credit a specific main account, the system doesn't allow you to select a financial dimension for the credit account when you set up the reconciliation reason.</span></span>

<span data-ttu-id="d4e98-111">Wenn für die Kontostruktur ein bestimmter Wert für die Finanzdimension des Habenhauptkontos erforderlich ist, kann die resultierende Kreditorenerfassung nicht automatisch gebucht werden, da der Wert für die Finanzdimension fehlt.</span><span class="sxs-lookup"><span data-stu-id="d4e98-111">If the account structure requires a specific financial dimension value for the credit main account, the resulting vendor journal can't be posted automatically, because the financial dimension value is missing.</span></span> <span data-ttu-id="d4e98-112">Daher müssen Sie zuerst das Habenkonto manuell angeben, indem Sie die Seite **Rechnungserfassung** verwenden.</span><span class="sxs-lookup"><span data-stu-id="d4e98-112">Therefore, you must first manually specify the credit account by using the **Invoice journal** page.</span></span>

<span data-ttu-id="d4e98-113">Da für das Habenkonto ein Dimensionswert erforderlich ist, kann das Kreditoenrechnungserfassung nicht automatisch gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="d4e98-113">Because a dimension value is required for the credit account, the vendor invoice journal can't be automatically posted.</span></span> <span data-ttu-id="d4e98-114">Sie müssen sie manuell buchen, nachdem Sie den Dimensionswert manuell zum Hauptkonto für die Kreditlinie hinzugefügt haben.</span><span class="sxs-lookup"><span data-stu-id="d4e98-114">You must manually post it after you manually add the dimension value to the main account for the credit line.</span></span>
