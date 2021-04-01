---
title: Zuständige Wartungsarbeiter
description: In diesem Thema wird erläutert, wie zuständige Wartungsarbeiter in Asset Management eingerichtet werden.
author: josaw1
manager: tfehr
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkerResponsible
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ad6b1757952fb0e5b970f82f75d99919a7f0745e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5261164"
---
# <a name="responsible-maintenance-workers"></a><span data-ttu-id="49d61-103">Zuständige Wartungsarbeiter</span><span class="sxs-lookup"><span data-stu-id="49d61-103">Responsible maintenance workers</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="49d61-104">Zuständige Wartungsarbeiter können Anlagentypen, Anlagen, funktionalen Standorten, Wartungsauftragstyp-Kategorien, Wartungsauftragstypen, Wartungsauftragstyp-Varianten und Facharbeiten zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="49d61-104">Responsible maintenance workers can be related to asset types, assets, functional locations, maintenance job type categories, maintenance job types, maintenance job type variants, and trades.</span></span> <span data-ttu-id="49d61-105">Sie können in Arbeitsaufträgen und Wartungsanfragen verwendet werden, um eine Präferenz bzgl. des Wartungsarbeiters anzugeben, der für einen Arbeitsauftrag zuständig sein soll.</span><span class="sxs-lookup"><span data-stu-id="49d61-105">They can be used on work orders and maintenance requests to indicate a preference about the maintenance workers who should be responsible for a work order.</span></span> <span data-ttu-id="49d61-106">(Jedoch sind diese Wartungsarbeiter nicht zwangsläufig die gleichen Arbeitskräfte, die für die Ausführung des Arbeitsauftrags eingeplant werden.) Die Nutzung dieser Funktion ist optional.</span><span class="sxs-lookup"><span data-stu-id="49d61-106">(However, those maintenance workers aren't necessarily the same workers who are scheduled to carry out the work order.) Use of this functionality is optional.</span></span> <span data-ttu-id="49d61-107">Beispielsweise kann sie verwendet werden, um zuständige Arbeitskräfte oder Arbeitskraftgruppen für bestimmte Arbeitstypen oder Arbeitsbereiche auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="49d61-107">For example, it can be used to select responsible workers or worker groups for specific work types or work areas.</span></span>

<span data-ttu-id="49d61-108">Während eines Arbeitsauftrag-Lebenszyklus oder eines Wartungsanfrage-Lebenszyklus können die zuständigen Wartungsarbeiter geändert oder aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="49d61-108">During a work order lifecycle or a maintenance request lifecycle, responsible maintenance workers can be changed or updated.</span></span> <span data-ttu-id="49d61-109">Diese Änderung oder Aktualisierung kann z. B. mit einer Änderung des Wartungsanfrage-Lebenszyklusstatus oder des Arbeitsauftrag-Lebenszyklusstatus in Zusammenhang stehen.</span><span class="sxs-lookup"><span data-stu-id="49d61-109">This change or update might be related to, for example, a change in the maintenance request lifecycle state or the work order lifecycle state.</span></span>

<span data-ttu-id="49d61-110">Die Einstellungen auf der Seite **Zuständige Wartungsarbeiter** werden während der Arbeitsauftragsplanung *nicht* verwendet.</span><span class="sxs-lookup"><span data-stu-id="49d61-110">The setup on the **Responsible maintenance workers** page is *not* used during work order scheduling.</span></span>

> [!NOTE]
> <span data-ttu-id="49d61-111">In Asset Management können Sie auch *bevorzugte* Wartungsarbeiter einrichten, die Arbeitsaufträgen während der Arbeitsauftragsplanung zugewiesen werden können.</span><span class="sxs-lookup"><span data-stu-id="49d61-111">In Asset Management, you can also set up *preferred* maintenance workers who might be allocated to work orders during work order scheduling.</span></span>

<span data-ttu-id="49d61-112">Bevor Sie zuständige Wartungsarbeiter einrichten können, müssen Sie die Arbeitskräfte und Wartungsarbeitergruppen einrichten, die zur Auswahl verfügbar sein sollen.</span><span class="sxs-lookup"><span data-stu-id="49d61-112">Before you can set up responsible maintenance workers, you must set up the workers and maintenance worker groups that should be available for selection.</span></span> <span data-ttu-id="49d61-113">Informationen darüber, wie Sie Arbeitskräfte und Wartungsarbeitergruppen einrichten, finden Sie unter [Wartungsarbeiter und Arbeitskräftegruppen](../setup-for-objects/workers-and-worker-groups.md).</span><span class="sxs-lookup"><span data-stu-id="49d61-113">For information about how to set up workers and maintenance worker groups, see [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).</span></span>

## <a name="set-up-responsible-maintenance-workers"></a><span data-ttu-id="49d61-114">Zuständige Wartungsarbeiter einrichten</span><span class="sxs-lookup"><span data-stu-id="49d61-114">Set up responsible maintenance workers</span></span>

1. <span data-ttu-id="49d61-115">Wählen Sie **Anlagenverwaltung** \> **Einstellungen** \> **Arbeitskräfte** \> **Zuständige Wartungsarbeiter** aus.</span><span class="sxs-lookup"><span data-stu-id="49d61-115">Select **Asset management** \> **Setup** \> **Workers** \> **Responsible maintenance workers**.</span></span>
2. <span data-ttu-id="49d61-116">Wählen Sie **Neu** aus, um einen Datensatz zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="49d61-116">Select **New** to create a record.</span></span>
3. <span data-ttu-id="49d61-117">Erstellen Sie zuerst eine Standardkonfiguration eines zuständigen Wartungsarbeiters oder einer zuständige Wartungsarbeitergruppe, in der Sie nur das Feld **Zuständige Wartungsarbeitergruppe** und/oder das Feld **Zuständige Arbeitskraft** festlegen.</span><span class="sxs-lookup"><span data-stu-id="49d61-117">First create a default responsible maintenance worker or responsible maintenance worker group setup, where you set only the **Responsible maintenance worker group** field and/or the **Responsible worker** field.</span></span> <span data-ttu-id="49d61-118">Lassen Sie die restlichen Felder leer.</span><span class="sxs-lookup"><span data-stu-id="49d61-118">Leave the remaining fields blank.</span></span> <span data-ttu-id="49d61-119">Diese Standardkonfiguration wird während der Arbeitsauftragsplanung verwendet, wenn keine andere, spezifischere Kombination dem Inhalt des Arbeitsauftrags entspricht.</span><span class="sxs-lookup"><span data-stu-id="49d61-119">This default setup will be used during work order scheduling if no other, more specific combination matches the contents of the work order.</span></span>

    > [!NOTE]
    > <span data-ttu-id="49d61-120">Wenn während der Erstellung einer Wartungsanfrage ein zuständiger Wartungsarbeiter oder eine zuständiger Wartungsarbeitergruppe zur Auswahl auf der Seite **Alle Wartungsanfragen** bereitgestellt wird, durchsucht Asset Management alle zuständigen Wartungsarbeiterdatensätze nach einer möglichen Übereinstimmung.</span><span class="sxs-lookup"><span data-stu-id="49d61-120">During creation of a maintenance request, when a responsible maintenance worker or responsible maintenance worker group is made available for selection on the **All maintenance requests** page, Asset Management goes through all responsible maintenance worker records to check for a possible match.</span></span> <span data-ttu-id="49d61-121">Die spezifischste Kombination wird immer zuerst geprüft.</span><span class="sxs-lookup"><span data-stu-id="49d61-121">It always checks the most specific combination first.</span></span> <span data-ttu-id="49d61-122">Das bedeutet, Asset Management sucht als Erstes nach einer Übereinstimmung für das Feld **Facharbeit**.</span><span class="sxs-lookup"><span data-stu-id="49d61-122">In other words, Asset Management first checks for a match for the **Trade** field.</span></span> <span data-ttu-id="49d61-123">Wenn keine Übereinstimmung gefunden wird, sucht es nach einer Übereinstimmung für das Feld **Wartungsauftragstyp-Variante**.</span><span class="sxs-lookup"><span data-stu-id="49d61-123">If no match is found, it checks for a match for the **Maintenance job type variant** field.</span></span> <span data-ttu-id="49d61-124">Wenn keine Übereinstimmung gefunden wird, sucht es nach einer Übereinstimmung für das Feld **Wartungsauftragstyp** usw.</span><span class="sxs-lookup"><span data-stu-id="49d61-124">If no match is found, it checks for a match for the **Maintenance job type** field, and so on.</span></span> <span data-ttu-id="49d61-125">Wie Sie im Layout der Seite sehen können, bedeutet dieses Verhalten, dass Asset Management auf der Suche nach der spezifischsten Kombination jeden Datensatz von rechts nach links auf eine Übereinstimmung überprüft (zuerst **Facharbeit**, dann **Wartungsauftragstyp-Variante**, dann **Wartungsauftragstyp**, dann **Wartungsauftragstyp-Kategorie**, dann **Funktionaler Standort**, dann **Anlage** und schließlich **Anlagentyp**).</span><span class="sxs-lookup"><span data-stu-id="49d61-125">As you can see in the layout of the page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match (first **Trade**, then **Maintenance job type variant**, then **Maintenance job type**, then **Maintenance job type category**, then **Functional location**, then **Asset**, and finally **Asset type**).</span></span> <span data-ttu-id="49d61-126">Wenn keine Übereinstimmung gefunden wird, wird der Standarddatensatz, der keine Auswahl in diesen sieben Feldern hat, verwendet.</span><span class="sxs-lookup"><span data-stu-id="49d61-126">If no match is found, the default record that has no selections in those seven fields is used.</span></span>

<span data-ttu-id="49d61-127">Die folgende Abbildung zeigt ein Beispiel der Seite **Zuständige Wartungsarbeiter**.</span><span class="sxs-lookup"><span data-stu-id="49d61-127">The following illustration shows an example of the **Responsible maintenance workers** page.</span></span>

![Seite „Zuständige Wartungsarbeiter“](media/08-setup-for-requests.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]