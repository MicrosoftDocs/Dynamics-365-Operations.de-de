---
title: Gewicht muss positiv sein
description: Gewicht muss positiv sein
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSContainerCloseDiag_canClose
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: dcbcde3143cb509b68b277cb7c709263e2659b5b
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924302"
---
# <a name="weight-must-be-positive"></a><span data-ttu-id="c5292-103">Gewicht muss positiv sein</span><span class="sxs-lookup"><span data-stu-id="c5292-103">Weight must be positive</span></span>

<span data-ttu-id="c5292-104">Fehlercode: WeightMustBePositive</span><span class="sxs-lookup"><span data-stu-id="c5292-104">Error code: WeightMustBePositive</span></span>

## <a name="symptoms"></a><span data-ttu-id="c5292-105">Symptome</span><span class="sxs-lookup"><span data-stu-id="c5292-105">Symptoms</span></span>

<span data-ttu-id="c5292-106">Das System zeigt die folgende Fehlermeldung an:</span><span class="sxs-lookup"><span data-stu-id="c5292-106">The system shows the following error message:</span></span>

> <span data-ttu-id="c5292-107">Das Gewicht muss positiv sein.</span><span class="sxs-lookup"><span data-stu-id="c5292-107">Weight must be positive.</span></span>

## <a name="cause"></a><span data-ttu-id="c5292-108">Ursache</span><span class="sxs-lookup"><span data-stu-id="c5292-108">Cause</span></span>

<span data-ttu-id="c5292-109">Das Feld **Bruttogewicht** wird auf *0* (Null) oder einen negativen Wert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c5292-109">The **Gross Weight** field is set to *0* (zero) or a negative value.</span></span>

## <a name="resolution"></a><span data-ttu-id="c5292-110">Lösung</span><span class="sxs-lookup"><span data-stu-id="c5292-110">Resolution</span></span>

<span data-ttu-id="c5292-111">Um eine Gewichtung festzulegen, führen Sie einen der folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="c5292-111">To specify a weight, follow one of these steps.</span></span>

- <span data-ttu-id="c5292-112">Legen Sie im Feld **Bruttogewicht** einen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="c5292-112">In the **Gross weight** field, set a value.</span></span> <span data-ttu-id="c5292-113">Wählen Sie dann eine Einheit in der Dropdown-Liste.</span><span class="sxs-lookup"><span data-stu-id="c5292-113">Then select a unit in the drop-down list.</span></span>
- <span data-ttu-id="c5292-114">Wählen Sie **Systemgewicht abrufen**, um den Wert **Bruttogewicht** zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="c5292-114">Select **Get system weight** to calculate the **Gross weight** value.</span></span>
