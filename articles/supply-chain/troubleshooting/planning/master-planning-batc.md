---
title: Sie können Masterplanungselemente nicht nach den zugehörigen Abdeckungsgruppenwerten filtern
description: Sie können Masterplanungselemente nicht nach den zugehörigen Abdeckungsgruppenwerten filtern.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: fa0b614b6710c65811add8725a0e255ce2c34b88
ms.sourcegitcommit: 3c15a26e9708adc9a75082dc551f0a3a0a7d89f4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049469"
---
# <a name="you-cant-filter-master-planning-items-by-their-related-coverage-group-values"></a><span data-ttu-id="1dd51-103">Sie können Masterplanungselemente nicht nach den zugehörigen Abdeckungsgruppenwerten filtern</span><span class="sxs-lookup"><span data-stu-id="1dd51-103">You can't filter master planning items by their related coverage group values</span></span>

<span data-ttu-id="1dd51-104">KB-Nummer: 4612572</span><span class="sxs-lookup"><span data-stu-id="1dd51-104">KB number: 4612572</span></span>

## <a name="symptoms"></a><span data-ttu-id="1dd51-105">Symptome</span><span class="sxs-lookup"><span data-stu-id="1dd51-105">Symptoms</span></span>

<span data-ttu-id="1dd51-106">Sie möchten die Elemente filtern, die in einem Masterplanungs-Chargeneinzelvorgang enthalten sind, basierend auf den Werten der zugehörigen Datensätze aus der Elementabdeckungstabelle.</span><span class="sxs-lookup"><span data-stu-id="1dd51-106">You want to filter the items that will be included in a master planning batch job, based on the values of related records from the item coverage table.</span></span> <span data-ttu-id="1dd51-107">(Zum Beispiel möchten Sie Elemente nach ihrem Wert **Verkäufer** und/oder **Abdeckungsgruppe** filtern).</span><span class="sxs-lookup"><span data-stu-id="1dd51-107">(For example, you want to filter items by their **Vendor** and/or **Coverage group** value).</span></span> <span data-ttu-id="1dd51-108">Mit der Filter-Einrichtung für den Chargeneinzelvorgang können Sie eine Verknüpfung aus der Tabelle **Artikel** zur Tabelle **Artikelabdeckung** erstellen; geben Sie dann Feldwerte aus der Elementabdeckungstabelle in Ihrer Abfrage an.</span><span class="sxs-lookup"><span data-stu-id="1dd51-108">The filter setup for the batch job lets you create a join from the **Items** table to the **Item coverage** table, and then specify field values from the item coverage table in your query.</span></span> <span data-ttu-id="1dd51-109">Nach Abschluss dieser Einrichtung erstellt das System jedoch weiterhin Planaufträge für die gesamte Artikelabdeckung, nicht nur für die Artikel, die den angegebenen Feldwerten aus der Artikelabdeckungstabelle entsprechen.</span><span class="sxs-lookup"><span data-stu-id="1dd51-109">However, after you complete this setup, the system still creates planned orders for the whole item coverage, not just for the items that match the specified field values from the item coverage table.</span></span>

## <a name="resolution"></a><span data-ttu-id="1dd51-110">Lösung</span><span class="sxs-lookup"><span data-stu-id="1dd51-110">Resolution</span></span>

<span data-ttu-id="1dd51-111">Der Chargeneinzelvorgang kann nur nach Elementen filtern.</span><span class="sxs-lookup"><span data-stu-id="1dd51-111">The batch job filter can filter only on items.</span></span> <span data-ttu-id="1dd51-112">Obwohl Sie der Tabelle **Artikelabdeckung** eine Verknüpfung hinzufügen können, werden Filtereinstellungen, die Sie für diese Tabelle vornehmen, sich nicht auf die Abfrageausgabe auswirken.</span><span class="sxs-lookup"><span data-stu-id="1dd51-112">Although you can add a join to the **Item coverage** table, filter settings that you make against that table won't affect the query output.</span></span> <span data-ttu-id="1dd51-113">Zur Laufzeit führt das System eine Planung für alle Abdeckungsgruppen und alle Variationen der gefilterten Elemente aus.</span><span class="sxs-lookup"><span data-stu-id="1dd51-113">At runtime, the system runs planning for all the coverage groups and all the variations that the filtered items have.</span></span> <span data-ttu-id="1dd51-114">Nachdem ein Artikel bereits im Lauf enthalten ist, wirken sich alle im Artikelfilter enthaltenen Abdeckungsgruppen nicht auf die Planungsausgabe aus.</span><span class="sxs-lookup"><span data-stu-id="1dd51-114">After an item is already included in the run, any coverage groups that are included in the item filter a won't affect the planning output.</span></span>
