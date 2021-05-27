---
title: Sie können einen Artikel nicht mithilfe der Entität „Freigegebene Produkte V2“ importieren
description: Sie können einen Artikel nicht mithilfe der Entität „Freigegebene Produkte V2“ importieren.
author: t-benebo
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: EcoResProductDetailsExtended, DataManagementWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 8182f2f83f6a3e4cf54fe6fa64b25a2f461ff541
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026533"
---
# <a name="you-cant-import-an-item-by-using-the-released-products-v2-entity"></a><span data-ttu-id="418c2-103">Sie können einen Artikel nicht mithilfe der Entität „Freigegebene Produkte V2“ importieren</span><span class="sxs-lookup"><span data-stu-id="418c2-103">You can't import an item by using the Released products V2 entity</span></span>

<span data-ttu-id="418c2-104">KB-Nummer: 4611825</span><span class="sxs-lookup"><span data-stu-id="418c2-104">KB number: 4611825</span></span>

## <a name="symptoms"></a><span data-ttu-id="418c2-105">Symptome</span><span class="sxs-lookup"><span data-stu-id="418c2-105">Symptoms</span></span>

<span data-ttu-id="418c2-106">Wenn Sie versuchen, einen Artikel mithilfe der Entität *Freigegebene Produkte V2* zu importieren, erhalten Sie eine Fehlermeldung, die dem folgenden Beispiel ähnelt:</span><span class="sxs-lookup"><span data-stu-id="418c2-106">When you try to import an item by using the *Released products V2* entity, you receive an error message that resembles the following example:</span></span>

> <span data-ttu-id="418c2-107">In „Artikel – Rückverfolgungsangabengruppen“ kann kein Datensatz erstellt werden (EcoResTrackingDimensionGroupItem).</span><span class="sxs-lookup"><span data-stu-id="418c2-107">Cannot create a record in Items - tracking dimension groups (EcoResTrackingDimensionGroupItem).</span></span> <span data-ttu-id="418c2-108">Artikelnummer: 2040663, Charge.</span><span class="sxs-lookup"><span data-stu-id="418c2-108">Item number: 2040663, Batch.</span></span> <span data-ttu-id="418c2-109">Der Datensatz ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="418c2-109">The record already exists.</span></span>

## <a name="resolution"></a><span data-ttu-id="418c2-110">Lösung</span><span class="sxs-lookup"><span data-stu-id="418c2-110">Resolution</span></span>

<span data-ttu-id="418c2-111">Um neu freigegebene Produkte zu importieren, müssen Sie die Entität *Erstellung eines freigegebenen Produkts V2* anstelle der Entität *Freigegebene Produkte V2* verwenden.</span><span class="sxs-lookup"><span data-stu-id="418c2-111">To import new released products, you must use the *Released product creation V2* entity instead of the *Released products V2* entity.</span></span>
