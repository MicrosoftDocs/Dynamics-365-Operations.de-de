---
title: Anlagen verschieben, ersetzen und installieren
description: In diesem Thema wird erläutert, wie Sie Anlagen in Asset Management verschieben, ersetzen und installieren.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectReplace, EntAssetObjectInstallLookup, EntAssetObjectMove, EntAssetObjectTableEditSubObjects
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 022ffc59b1b64913fedaf550f3fdb32141a94031
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/16/2021
ms.locfileid: "5020278"
---
# <a name="move-replace-and-install-assets"></a><span data-ttu-id="4a8db-103">Anlagen verschieben, ersetzen und installieren</span><span class="sxs-lookup"><span data-stu-id="4a8db-103">Move, replace, and install assets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="4a8db-104">In diesem Thema wird erläutert, wie Sie Anlagen in Asset Management verschieben, ersetzen und installieren.</span><span class="sxs-lookup"><span data-stu-id="4a8db-104">This topic explains how to move, replace, and install assets in Asset Management.</span></span> <span data-ttu-id="4a8db-105">Sie können einzelne Anlagen erstellen, die nicht in Beziehung zu anderen Anlagen stehen, oder Sie können eine Anlagenstruktur erstellen, die eine übergeordnete Anlage (Anlage der obersten Ebene) und zugehörige untergeordnete Anlagen (Sub-Anlagen) enthält.</span><span class="sxs-lookup"><span data-stu-id="4a8db-105">You can create individual assets that have no relations to other assets, or you can create an asset structure that includes a parent asset (top-level asset) and related child assets (sub-assets).</span></span> <span data-ttu-id="4a8db-106">In Asset Management gibt es drei Möglichkeiten zum Verschieben und Ändern des Standorts einer Anlage:</span><span class="sxs-lookup"><span data-stu-id="4a8db-106">In Asset Management, there are three approaches to moving and changing the location of an asset:</span></span>

- <span data-ttu-id="4a8db-107">**Verschieben** – Verschiebt eine Anlage entweder in eine andere Anlagenstruktur oder an einen anderen Standort in derselben Anlagenstruktur.</span><span class="sxs-lookup"><span data-stu-id="4a8db-107">**Move** – Move an asset either to another asset structure or to another location in the same asset structure.</span></span>
- <span data-ttu-id="4a8db-108">**Ersetzen** – Entfernt vorübergehend eine Anlage aus einer Anlagenstruktur, sodass sie repariert oder überholt werden kann, und fügen die überholte Anlage dann wieder in die Anlagenstruktur ein.</span><span class="sxs-lookup"><span data-stu-id="4a8db-108">**Replace** – Temporarily remove an asset from an asset structure so that it can be repaired or refurbished, and then add the refurbished asset back to the asset structure later.</span></span> <span data-ttu-id="4a8db-109">Alternativ können Sie eine verwendete Anlage dauerhaft durch eine neue Anlage ersetzen.</span><span class="sxs-lookup"><span data-stu-id="4a8db-109">Alternatively, permanently replace a used asset with a new asset.</span></span>
- <span data-ttu-id="4a8db-110">**Installieren** – Installieren Sie eine übergeordnete Anlage und alle zugehörigen untergeordneten Anlagen an einem funktionalen Standort.</span><span class="sxs-lookup"><span data-stu-id="4a8db-110">**Install** – Install a parent asset and any related child assets on a functional location.</span></span>

> [!NOTE]
> <span data-ttu-id="4a8db-111">Die Anlage, die Sie verschieben, ersetzen oder installieren, kann einem anderen funktionalen Standort zugeordnet sein.</span><span class="sxs-lookup"><span data-stu-id="4a8db-111">The asset that you move, replace, or install might be related to another functional location.</span></span> <span data-ttu-id="4a8db-112">In diesem Fall verwendet die Anlage möglicherweise Finanzdimensionen des funktionalen Standorts.</span><span class="sxs-lookup"><span data-stu-id="4a8db-112">In that case, the asset might use financial dimensions of the functional location.</span></span> <span data-ttu-id="4a8db-113">Auf der Seite **Funktionale Standorttypen** können Sie die Handhabung von Finanzdimensionen für funktionale Standorte einrichten.</span><span class="sxs-lookup"><span data-stu-id="4a8db-113">On the **Functional location types** page, you set up the handling of financial dimensions on functional locations.</span></span>

## <a name="move-asset"></a><span data-ttu-id="4a8db-114">Anlage verschieben</span><span class="sxs-lookup"><span data-stu-id="4a8db-114">Move asset</span></span>

<span data-ttu-id="4a8db-115">Verwenden Sie die Funktion **Anlage verschieben**, um eine Anlage entweder in eine andere Anlagenstruktur oder an einen anderen Standort in derselben Anlagenstruktur zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="4a8db-115">Use the **Move asset** function to move an asset either to another asset structure or to another location in the same asset structure.</span></span> <span data-ttu-id="4a8db-116">Sie können eine Anlage auch aus einer Anlagenstruktur verschieben, sodass sie zu einer eigenständigen Anlage wird, die keine Beziehung zu einer Struktur hat.</span><span class="sxs-lookup"><span data-stu-id="4a8db-116">You can also move an asset out of an asset structure so that it becomes a standalone asset that has no structure relations.</span></span>

> [!NOTE]
> <span data-ttu-id="4a8db-117">Verwenden Sie diese Funktion nicht, wenn Anlagen repariert oder vorübergehend ersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="4a8db-117">Don't use this function if assets are being repaired or temporarily replaced.</span></span> <span data-ttu-id="4a8db-118">Verwenden Sie stattdessen die Funktionen **Anlage ersetzen**, die weiter unten in diesem Thema beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="4a8db-118">Instead, use the **Replace asset** functionality that is described later in this topic.</span></span>

1. <span data-ttu-id="4a8db-119">Wählen Sie **Anlagenverwaltung** \> **Allgemeines** \> **Anlagen** \> **Alle Anlagen** oder **Aktive Anlagen**.</span><span class="sxs-lookup"><span data-stu-id="4a8db-119">Select **Asset management** \> **Common** \> **Assets** \> **All assets** or **Active assets**.</span></span>
2. <span data-ttu-id="4a8db-120">Wählen Sie in der Liste die zu verschiebende Anlage aus.</span><span class="sxs-lookup"><span data-stu-id="4a8db-120">In the list, select the asset to move.</span></span> <span data-ttu-id="4a8db-121">Wenn die Anlage untergeordnete Anlagen enthält, verschieben Sie auch diese Anlagen.</span><span class="sxs-lookup"><span data-stu-id="4a8db-121">If the asset has child assets, you also move those assets.</span></span>
3. <span data-ttu-id="4a8db-122">Wählen Sie **Anlage verschieben** aus.</span><span class="sxs-lookup"><span data-stu-id="4a8db-122">Select **Move asset**.</span></span>
4. <span data-ttu-id="4a8db-123">Um die Anlagen so zu verschieben, dass sie Teil einer Anlagenstruktur wird, wählen Sie die neue übergeordnete Anlage im Feld **Übergeordnete Anlage** aus.</span><span class="sxs-lookup"><span data-stu-id="4a8db-123">To move the asset so that it becomes part of an asset structure, select the new parent asset in the **Parent asset** field.</span></span> <span data-ttu-id="4a8db-124">Wenn Sie eine untergeordnete Anlage verschieben und sie zu einer eigenständige Anlage machen möchten, die keine Beziehungen zu einer Struktur hat, lassen Sie das Feld **Übergeordnete Anlage** leer.</span><span class="sxs-lookup"><span data-stu-id="4a8db-124">If you're moving a child asset, and you want to make it a standalone asset that has no structure relations, leave the **Parent asset** field blank.</span></span>
5. <span data-ttu-id="4a8db-125">Standardmäßig wird das Feld **Gültig** auf das aktuelle Datum und die Uhrzeit festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4a8db-125">By default, the **Effective** field is set to the current date and time.</span></span> <span data-ttu-id="4a8db-126">Sie können jedoch ein anderes Datum und eine andere Uhrzeit auswählen, wann das Verschieben der Anlagen gültig sein soll.</span><span class="sxs-lookup"><span data-stu-id="4a8db-126">However, you can select a different date and time that the asset move is valid from.</span></span>
6. <span data-ttu-id="4a8db-127">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="4a8db-127">Select **OK**.</span></span>

## <a name="replace-asset"></a><span data-ttu-id="4a8db-128">Anlage ersetzen</span><span class="sxs-lookup"><span data-stu-id="4a8db-128">Replace asset</span></span>

<span data-ttu-id="4a8db-129">Verwenden Sie die Funktion **Anlage ersetzen** im Zusammenhang mit Reparaturen, Renovierungen oder dauerhaftem Ersatz einer verbrauchten Anlage durch eine neue Anlage.</span><span class="sxs-lookup"><span data-stu-id="4a8db-129">Use the **Replace asset** function in connection with repairs, refurbishment, or permanent replacement of a worn-out asset by a new asset.</span></span> <span data-ttu-id="4a8db-130">Diese Funktion wird verwendet, um untergeordnete Anlagen in einer Anlagenstruktur zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="4a8db-130">This function is used to replace child assets in an asset structure.</span></span> <span data-ttu-id="4a8db-131">Bei übergeordneten Anlagen (d. h. Anlagen, die gerade keine übergeordnete Anlage haben) erfolgt das Ersetzen an einem funktionalen Standort.</span><span class="sxs-lookup"><span data-stu-id="4a8db-131">For parent assets (that is, assets that don't currently have a parent asset), this replacement is done on a functional location.</span></span> <span data-ttu-id="4a8db-132">Weitere Informationen dazu, wie übergeordnete Anlagen an einem funktionalen Standort ersetzt werden, finden Sie unter [Anlagen an funktionalen Standorten installieren](../functional-locations/install-objects-on-functional-locations.md).</span><span class="sxs-lookup"><span data-stu-id="4a8db-132">For more information about how to replace parent assets on a functional location, see [Install assets on functional locations](../functional-locations/install-objects-on-functional-locations.md).</span></span>

> [!NOTE]
> <span data-ttu-id="4a8db-133">Wenn eine Werkstatt einer Produktionsabteilung zugeordnet ist, können Sie funktionale Standorte wie **Reparatur**, **Ausschuss** und **Lager** erstellen, um die Reparatur und die Ersetzung von Anlagen zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="4a8db-133">If a repair shop is related to your production department, you can create functional locations such as **Repair**, **Scrap**, and **Storage** to handle the repair and replacement of assets.</span></span>

1. <span data-ttu-id="4a8db-134">Wählen Sie **Anlagenverwaltung** \> **Allgemeines** \> **Anlagen** \> **Alle Anlagen** oder **Aktive Anlagen**.</span><span class="sxs-lookup"><span data-stu-id="4a8db-134">Select **Asset management** \> **Common** \> **Assets** \> **All assets** or **Active assets**.</span></span>
2. <span data-ttu-id="4a8db-135">Wählen Sie in der Liste die zu ersetzende untergeordnete Anlage aus.</span><span class="sxs-lookup"><span data-stu-id="4a8db-135">In the list, select the child asset to replace.</span></span> <span data-ttu-id="4a8db-136">Wenn die Anlage untergeordnete Anlagen enthält, ersetzen Sie auch diese Anlagen.</span><span class="sxs-lookup"><span data-stu-id="4a8db-136">If the asset has child assets, you also replace those assets.</span></span>
3. <span data-ttu-id="4a8db-137">Wählen Sie **Anlage ersetzen** aus.</span><span class="sxs-lookup"><span data-stu-id="4a8db-137">Select **Replace asset**.</span></span>

    <span data-ttu-id="4a8db-138">Das Feld **Strukturänderung** zeigt das Datum und die Uhrzeit an, wann die ausgewählte Anlage und die zugehörigen untergeordneten Anlagen in die Anlagenstruktur verschoben wurden.</span><span class="sxs-lookup"><span data-stu-id="4a8db-138">The **Structure change** field shows the last date and time that the selected asset and related child assets were moved in the asset structure.</span></span>

4. <span data-ttu-id="4a8db-139">Wählen Sie im Abschnitt **Ausgewählte Anlage** im Feld **Funktionaler Standort als Ziel** den funktionalen Standort aus, an den die Anlage verschoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="4a8db-139">In the **Selected asset** section, in the **Target functional location** field, select the functional location to move the asset to.</span></span> <span data-ttu-id="4a8db-140">Wählen Sie beispielsweise den Standort **Reparatur** oder **Ausschuss** aus.</span><span class="sxs-lookup"><span data-stu-id="4a8db-140">For example, select the **Repair** or **Scrap** location.</span></span>

    <span data-ttu-id="4a8db-141">Im Abschnitt **Übergeordnete Anlage** zeigt das Feld **Gültig** das letzte Datum und die Uhrzeit an, wann die übergeordnete Anlage und die zugehörigen untergeordneten Anlagen installiert oder an den aktuellen funktionalen Standort verschoben wurden.</span><span class="sxs-lookup"><span data-stu-id="4a8db-141">In the **Parent asset** section, the **Effective** field shows the last date and time that the parent asset and related child assets were installed or moved on the current functional location.</span></span>

5. <span data-ttu-id="4a8db-142">Wählen Sie im Abschnitt **Neue Anlage** im Feld **Anlage** die Anlage aus, die als vorübergehender oder dauerhafter Ersatz für die ausgewählte Anlage eingefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4a8db-142">In the **New asset** section, in the **Asset** field, select the asset to insert as a temporary or permanent replacement for the selected asset.</span></span> <span data-ttu-id="4a8db-143">Diese Anlage befindet sich derzeit möglicherweise an einem anderen funktionalen Standort, z. B. **Lager**.</span><span class="sxs-lookup"><span data-stu-id="4a8db-143">This asset might currently be located on another functional location, such as **Storage**.</span></span>
7. <span data-ttu-id="4a8db-144">Im Abschnitt **Gültig ab** wird das Feld **Gültig** standardmäßig auf das aktuelle Datum und die aktuelle Uhrzeit festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4a8db-144">In the **Effective from** section, the **Effective** field is set to the current date and time by default.</span></span> <span data-ttu-id="4a8db-145">Sie können jedoch ein anderes Datum und eine andere Uhrzeit auswählen, wann das Ersetzen der Anlagen gültig sein soll.</span><span class="sxs-lookup"><span data-stu-id="4a8db-145">However, you can select a different date and time that the asset replacement is valid from.</span></span>
8. <span data-ttu-id="4a8db-146">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="4a8db-146">Select **OK**.</span></span>

## <a name="install-asset"></a><span data-ttu-id="4a8db-147">Anlage installieren</span><span class="sxs-lookup"><span data-stu-id="4a8db-147">Install asset</span></span>

<span data-ttu-id="4a8db-148">Verwenden Sie die Funktion **Anlage installieren**, um eine Anlagenstruktur an einen funktionalen Standort zu installieren.</span><span class="sxs-lookup"><span data-stu-id="4a8db-148">Use the **Install asset** function to install an asset structure on a functional location.</span></span>

> [!NOTE]
> <span data-ttu-id="4a8db-149">Wählen Sie immer eine übergeordnete Anlage aus.</span><span class="sxs-lookup"><span data-stu-id="4a8db-149">Always select a parent asset.</span></span> <span data-ttu-id="4a8db-150">Die übergeordnete Anlage und die zugehörigen untergeordneten Anlagen werden an den ausgewählten funktionalen Standort verschoben.</span><span class="sxs-lookup"><span data-stu-id="4a8db-150">The parent asset and related child assets will be moved to the selected functional location.</span></span>

1. <span data-ttu-id="4a8db-151">Wählen Sie **Anlagenverwaltung** \> **Allgemeines** \> **Anlagen** \> **Alle Anlagen** oder **Aktive Anlagen**.</span><span class="sxs-lookup"><span data-stu-id="4a8db-151">Select **Asset management** \> **Common** \> **Assets** \> **All assets** or **Active assets**.</span></span>
2. <span data-ttu-id="4a8db-152">Wählen Sie in der Liste die übergeordnete Anlage aus, die an einem anderen funktionalen Standort installiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="4a8db-152">In the list, select the parent asset to install on another functional location.</span></span>
3. <span data-ttu-id="4a8db-153">Wählen Sie **Anlage installieren** aus.</span><span class="sxs-lookup"><span data-stu-id="4a8db-153">Select **Install asset**.</span></span>

    <span data-ttu-id="4a8db-154">Der Abschnitt **Attribute** zeigt die Anlagenattribute, die für die übergeordnete Anlage eingerichtet sind.</span><span class="sxs-lookup"><span data-stu-id="4a8db-154">The **Attributes** section shows the asset attributes that are set up on the parent asset.</span></span>

4. <span data-ttu-id="4a8db-155">Wählen Sie im Feld **Funktionaler Standort** den neuen Standort aus.</span><span class="sxs-lookup"><span data-stu-id="4a8db-155">In the **Functional location** field, select the new location.</span></span>
5. <span data-ttu-id="4a8db-156">Standardmäßig wird das Feld **Gültig** auf das aktuelle Datum und die Uhrzeit festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4a8db-156">By default, the **Effective** field is set to the current date and time.</span></span> <span data-ttu-id="4a8db-157">Sie können jedoch ein anderes Datum und eine andere Uhrzeit auswählen, wann die Installation in der Anlagenstruktur gültig sein soll.</span><span class="sxs-lookup"><span data-stu-id="4a8db-157">However, you can select a different date and time that the installation on the asset structure is valid from.</span></span>
6. <span data-ttu-id="4a8db-158">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="4a8db-158">Select **OK**.</span></span>
