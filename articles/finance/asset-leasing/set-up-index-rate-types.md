---
title: Indexraten einrichten
description: In diesem Thema wird erläutert, wie Sie Indexraten einrichten. Indexsätze sind erforderlich, wenn Ihre Organisation Mietzahlungsbeträge mit einer Reihe von Indexraten verknüpft.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 6424248e8d01d04720ad65e80aaa543b42abccc6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823022"
---
# <a name="set-up-index-rates"></a><span data-ttu-id="17668-104">Indexraten einrichten</span><span class="sxs-lookup"><span data-stu-id="17668-104">Set up index rates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="17668-105">Wenn Mietzahlungen von einem Index abhängen, können die Indexzinsarten hinzugefügt und im System verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="17668-105">If lease payments depend on an index, the index rate types can be added and maintained in the system.</span></span> <span data-ttu-id="17668-106">Um die Mietzahlungen von der **Indexratentyp**-Seite neu zu bewerten, verwendet der Indexsatz-Neubewertungsprozess den neuesten Indexsatz ab dem Datum der Neubewertung.</span><span class="sxs-lookup"><span data-stu-id="17668-106">To revalue the lease payments from the **Index rate type** page, the index rate revaluation process uses the most recent index rate from the date of revaluation.</span></span>

<span data-ttu-id="17668-107">Führen Sie die folgenden Schritte aus, um Indexratentypen und Indexraten hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="17668-107">To add index rate types and index rates, follow these steps.</span></span>

1. <span data-ttu-id="17668-108">Wechseln Sie zu **Anlagenleasing \> Einrichtung \> Indexratentypen**.</span><span class="sxs-lookup"><span data-stu-id="17668-108">Go to **Asset leasing \> Setup \> Index rate type**.</span></span>
2. <span data-ttu-id="17668-109">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="17668-109">Select **New**.</span></span>
3. <span data-ttu-id="17668-110">Geben Sie in die entsprechenden Felder den Ratentyp und den Namen der Indexrate ein.</span><span class="sxs-lookup"><span data-stu-id="17668-110">In the appropriate fields, enter the rate type and the name of the index rate.</span></span>
4. <span data-ttu-id="17668-111">Um einen neuen Indexratenwert hinzuzufügen, wählen Sie den Indexratentyp aus dann **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="17668-111">To add a new index rate value, select the index rate type, and then select **Add**.</span></span>
5. <span data-ttu-id="17668-112">Wählen Sie das effektive Startdatum der Rate und den Ratenwert.</span><span class="sxs-lookup"><span data-stu-id="17668-112">Select the effective start date of the rate, and select the rate value.</span></span>

<span data-ttu-id="17668-113">Sie müssen entweder **Indexratenwertdifferenz** oder **Indexratenwert** als Indexratenmethode auswählen.</span><span class="sxs-lookup"><span data-stu-id="17668-113">You must select either **Index rate value difference** or **Index rate value** as the index rate method.</span></span>

- <span data-ttu-id="17668-114">Wählen Sie die **Indexratenwertdifferenz**-Methode zur Berechnung einer neuen Mietzahlung basierend auf der Differenz zwischen der Indexrate am Startdatum und der letzten Indexrate aus.</span><span class="sxs-lookup"><span data-stu-id="17668-114">Select the **Index rate value difference** method to calculate a new lease payment, based on the difference between the index rate on the start date and the most recent index rate.</span></span> <span data-ttu-id="17668-115">Die Indexrate wird im **Indexrate (%)**-Feld definiert.</span><span class="sxs-lookup"><span data-stu-id="17668-115">The index rate is defined in the **Index rate (%)** field.</span></span>
- <span data-ttu-id="17668-116">Wählen Sie die **Indexratenwert**-Methode zur Berechnung der Mietzahlung unter Verwendung des im Feld **Indexrate (%)** Prozentsatzes aus.</span><span class="sxs-lookup"><span data-stu-id="17668-116">Select the **Index rate value** method to calculate the lease payment by using the percentage that is specified in the **Index rate (%)** field.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]