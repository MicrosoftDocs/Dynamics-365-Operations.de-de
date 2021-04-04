---
title: Beschaffungs- und Bezugsquellenparameter für Gesamttransportkosten
description: Dieses Thema beschreibt, wie Sie die relevanten Beschaffungs- und Bezugsquellenparameter festlegen, wenn Sie das Modul Gesamttransportkosten verwenden.
author: sherry-zheng
manager: tfehr
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SrmParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 49e046a1437917cfa866f690511789496fac2c53
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500741"
---
# <a name="procurement-and-sourcing-parameters-for-landed-cost"></a><span data-ttu-id="c26f4-103">Beschaffungs- und Bezugsquellenparameter für Gesamttransportkosten</span><span class="sxs-lookup"><span data-stu-id="c26f4-103">Procurement and sourcing parameters for Landed cost</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="c26f4-104">Die Seite **Beschaffungs- und Bezugsquellenparameter** enthält einige Einstellungen, die besonders relevant sind, wenn Sie das Modul **Gesamttransportkosten** verwenden.</span><span class="sxs-lookup"><span data-stu-id="c26f4-104">The **Procurement and sourcing parameters** page has a few settings that are especially relevant when you use the **Landed cost** module.</span></span> <span data-ttu-id="c26f4-105">Verwenden Sie das Dialogfeld **Bestellzeilen aktualisieren**, das von der Seite **Beschaffungs- und Bezugsquellenparameter** geöffnet wird, um festzulegen, ob die Zeilen der Einkaufsbestellung automatisch aktualisiert werden sollen, wenn Änderungen am Kopf der Bestellung vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="c26f4-105">Use the **Update order lines** dialog box that is opened from the **Procurement and sourcing parameters** page to specify whether purchase order lines should automatically be updated when changes are made on the purchase order header.</span></span>

<span data-ttu-id="c26f4-106">Gehen Sie wie folgt vor, um diese Einrichtung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="c26f4-106">To complete this setup, follow these steps.</span></span>

1. <span data-ttu-id="c26f4-107">Gehen Sie zu **Beschaffung und Ursproung\> Einstellungen \> Beschaffungs- und Ursprungsparameter**.</span><span class="sxs-lookup"><span data-stu-id="c26f4-107">Go to **Procurement and sourcing \> Setup \> Procurement and sourcing parameters**.</span></span>
1. <span data-ttu-id="c26f4-108">Wählen Sie auf der Registerkarte **Allgemein** den Link **Bestellzeilen aktualisieren**.</span><span class="sxs-lookup"><span data-stu-id="c26f4-108">On the **General** tab, select the **Update order lines** link.</span></span>
1. <span data-ttu-id="c26f4-109">Das Dialogfeld **Bestellzeilen aktualisieren** listet die Felder im Bestellkopf auf, die auch automatische Aktualisierungen auf Bezugsfelder in den Bestellzeilen anwenden können.</span><span class="sxs-lookup"><span data-stu-id="c26f4-109">The **Update order lines** dialog box lists the fields on the order header that can also apply automatic updates to related fields on the order lines.</span></span> <span data-ttu-id="c26f4-110">Legen Sie jedes Feld in der Liste auf einen der folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="c26f4-110">Set each field in the list to one of the following values:</span></span>

    - <span data-ttu-id="c26f4-111">**Immer** - Die Auftragszeilen sollen automatisch aktualisiert werden, wenn der Auftragskopf aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="c26f4-111">**Always** – The order lines should automatically be updated when the order header is updated.</span></span>
    - <span data-ttu-id="c26f4-112">**Nie** - Die Auftragszeilen sollen nie aktualisiert werden, wenn der Auftragskopf aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="c26f4-112">**Never** – The order lines should never be updated when the order header is updated.</span></span>
    - <span data-ttu-id="c26f4-113">**Aufforderung** - Der Benutzer wird aufgefordert, auszuwählen, ob die Auftragszeilen aktualisiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c26f4-113">**Prompt** – The user will be prompted to select whether the order lines should be updated.</span></span>
