---
title: Beschaffungs- und Bezugsquellenparameter für Gesamttransportkosten
description: Dieses Thema beschreibt, wie Sie die relevanten Beschaffungs- und Bezugsquellenparameter festlegen, wenn Sie das Modul Gesamttransportkosten verwenden.
author: sherry-zheng
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
ms.openlocfilehash: df91fcb97794be32924707fcecf2b5fb34844596
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833928"
---
# <a name="procurement-and-sourcing-parameters-for-landed-cost"></a><span data-ttu-id="57bf9-103">Beschaffungs- und Bezugsquellenparameter für Gesamttransportkosten</span><span class="sxs-lookup"><span data-stu-id="57bf9-103">Procurement and sourcing parameters for Landed cost</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="57bf9-104">Die Seite **Beschaffungs- und Bezugsquellenparameter** enthält einige Einstellungen, die besonders relevant sind, wenn Sie das Modul **Gesamttransportkosten** verwenden.</span><span class="sxs-lookup"><span data-stu-id="57bf9-104">The **Procurement and sourcing parameters** page has a few settings that are especially relevant when you use the **Landed cost** module.</span></span> <span data-ttu-id="57bf9-105">Verwenden Sie das Dialogfeld **Bestellzeilen aktualisieren**, das von der Seite **Beschaffungs- und Bezugsquellenparameter** geöffnet wird, um festzulegen, ob die Zeilen der Einkaufsbestellung automatisch aktualisiert werden sollen, wenn Änderungen am Kopf der Bestellung vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="57bf9-105">Use the **Update order lines** dialog box that is opened from the **Procurement and sourcing parameters** page to specify whether purchase order lines should automatically be updated when changes are made on the purchase order header.</span></span>

<span data-ttu-id="57bf9-106">Gehen Sie wie folgt vor, um diese Einrichtung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="57bf9-106">To complete this setup, follow these steps.</span></span>

1. <span data-ttu-id="57bf9-107">Gehen Sie zu **Beschaffung und Ursproung\> Einstellungen \> Beschaffungs- und Ursprungsparameter**.</span><span class="sxs-lookup"><span data-stu-id="57bf9-107">Go to **Procurement and sourcing \> Setup \> Procurement and sourcing parameters**.</span></span>
1. <span data-ttu-id="57bf9-108">Wählen Sie auf der Registerkarte **Allgemein** den Link **Bestellzeilen aktualisieren**.</span><span class="sxs-lookup"><span data-stu-id="57bf9-108">On the **General** tab, select the **Update order lines** link.</span></span>
1. <span data-ttu-id="57bf9-109">Das Dialogfeld **Bestellzeilen aktualisieren** listet die Felder im Bestellkopf auf, die auch automatische Aktualisierungen auf Bezugsfelder in den Bestellzeilen anwenden können.</span><span class="sxs-lookup"><span data-stu-id="57bf9-109">The **Update order lines** dialog box lists the fields on the order header that can also apply automatic updates to related fields on the order lines.</span></span> <span data-ttu-id="57bf9-110">Legen Sie jedes Feld in der Liste auf einen der folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="57bf9-110">Set each field in the list to one of the following values:</span></span>

    - <span data-ttu-id="57bf9-111">**Immer** - Die Auftragszeilen sollen automatisch aktualisiert werden, wenn der Auftragskopf aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="57bf9-111">**Always** – The order lines should automatically be updated when the order header is updated.</span></span>
    - <span data-ttu-id="57bf9-112">**Nie** - Die Auftragszeilen sollen nie aktualisiert werden, wenn der Auftragskopf aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="57bf9-112">**Never** – The order lines should never be updated when the order header is updated.</span></span>
    - <span data-ttu-id="57bf9-113">**Aufforderung** - Der Benutzer wird aufgefordert, auszuwählen, ob die Auftragszeilen aktualisiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="57bf9-113">**Prompt** – The user will be prompted to select whether the order lines should be updated.</span></span>
