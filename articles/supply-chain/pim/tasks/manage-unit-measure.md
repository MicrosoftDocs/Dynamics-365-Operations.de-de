---
title: Verwalten von Maßeinheiten
description: Dieses Thema beschreibt, wie Sie eine Maßeinheit definieren, Übersetzungen für die Einheit und ihre Beschreibung bereitstellen und Umrechnungsregeln für verwandte Einheiten definieren.
author: sorenva
ms.date: 04/09/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup, UnitOfMeasureCalculator, UnitOfMeasureWizard, UnitOfMeasureLookupTest
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d36839cd8e3398225d3421bf0f268068599ca49f
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921340"
---
# <a name="manage-units-of-measure"></a><span data-ttu-id="8b9b6-103">Verwalten von Maßeinheiten</span><span class="sxs-lookup"><span data-stu-id="8b9b6-103">Manage units of measure</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8b9b6-104">Dieses Thema beschreibt, wie Sie eine Maßeinheit definieren, Übersetzungen für die Einheit und ihre Beschreibung bereitstellen und Umrechnungsregeln für verwandte Einheiten definieren.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-104">This topic describes how to define a unit of measure, provide translations for the unit and its description, and define conversion rules for related units.</span></span>

## <a name="open-the-units-page"></a><span data-ttu-id="8b9b6-105">Öffnen Sie die Seite Einheiten</span><span class="sxs-lookup"><span data-stu-id="8b9b6-105">Open the Units page</span></span>

<span data-ttu-id="8b9b6-106">Um die Maßeinheiten zu erstellen und mit ihnen zu arbeiten, die in Ihrem System verfügbar sind, gehen Sie zu **Organisationsverwaltung \> Einrichten \> Einheiten \> Einheiten**.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-106">To create and work with the units of measure that are available in your system, go to **Organization administration \> Setup \> Units \> Units**.</span></span>

<span data-ttu-id="8b9b6-107">Die restlichen Abschnitte dieses Themas beschreiben, was Sie auf der Seite **Einheiten** tun können.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-107">The remaining sections of this topic describe what you can do on the **Units** page.</span></span>

## <a name="create-standard-units-and-conversions"></a><span data-ttu-id="8b9b6-108">Erstellen Sie Standardeinheiten und Umrechnungen</span><span class="sxs-lookup"><span data-stu-id="8b9b6-108">Create standard units and conversions</span></span>

<span data-ttu-id="8b9b6-109">Wenn Ihr System nicht bereits die am häufigsten verwendeten Maßeinheiten für das metrische System und/oder das US Customary System (USCS) enthält, kann der Assistent zum Einrichten von Einheiten Ihnen helfen, schnell mit den grundlegenden Definitionen und Umrechnungen von Maßeinheiten zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-109">If your system doesn't already include the most commonly used units of measure for the metric system and/or the US customary system (USCS), the unit setup wizard can help you quickly get started with basic unit definitions and conversions.</span></span> <span data-ttu-id="8b9b6-110">Um den Assistenten abzuschließen, wählen Sie **Assistent zur Erstellung von Einheiten** im Aktivitätsbereich und folgen dann den Anweisungen auf dem Bildschirm.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-110">To complete the wizard, select **Unit creation wizard** on the Action Pane, and then follow the on-screen instructions.</span></span>

## <a name="create-or-edit-a-unit-of-measure"></a><span data-ttu-id="8b9b6-111">Erstellen oder bearbeiten Sie eine Maßeinheit</span><span class="sxs-lookup"><span data-stu-id="8b9b6-111">Create or edit a unit of measure</span></span>

<span data-ttu-id="8b9b6-112">Um eine Maßeinheit zu erstellen oder zu bearbeiten, gehen Sie folgendermaßen vor.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-112">To create or edit a unit of measure, follow these steps.</span></span>

1. <span data-ttu-id="8b9b6-113">Führen Sie einen dieser Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="8b9b6-113">Follow one of these steps:</span></span>

    - <span data-ttu-id="8b9b6-114">Um eine vorhandene Einheit zu bearbeiten, wählen Sie sie im Listenbereich aus.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-114">To edit an existing unit, select it in the list pane.</span></span>
    - <span data-ttu-id="8b9b6-115">Um eine neue Einheit zu erstellen, wählen Sie **Neu** im Aktivitätsbereich.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-115">To create a new unit, select **New** on the Action Pane.</span></span>

1. <span data-ttu-id="8b9b6-116">Legen Sie in der Kopfzeile des Datensatzes die folgenden Felder fest:</span><span class="sxs-lookup"><span data-stu-id="8b9b6-116">On the header of the record, set the following fields:</span></span>

    - <span data-ttu-id="8b9b6-117">**Einheit** – Geben Sie die ID oder das Symbol ein, das verwendet werden soll, um auf die Einheit in der Systemsprache zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-117">**Unit** – Enter the ID or symbol to use to refer to the unit in the system language.</span></span> <span data-ttu-id="8b9b6-118">Diese ID oder dieses Symbol ist normalerweise eine allgemeine Abkürzung für die Einheit, z. B. *ea* für jedes oder *cm* für Zentimeter.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-118">This ID or symbol is usually a common abbreviation for the unit, such as *ea* for each or *cm* for centimeter.</span></span>
    - <span data-ttu-id="8b9b6-119">**Beschreibung** – Geben Sie einen beschreibenden Namen für die Einheit in der Systemsprache ein.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-119">**Description** – Enter a descriptive name for the unit in the system language.</span></span> <span data-ttu-id="8b9b6-120">Dieser Name ist normalerweise der vollständige Name der Einheit, z. B. *Einheit* oder *Zentimeter*.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-120">This name is usually the full name of the unit, such as *Each* or *Centimeter*.</span></span>

1. <span data-ttu-id="8b9b6-121">Legen Sie im Inforegister **Allgemein** die folgenden Felder fest:</span><span class="sxs-lookup"><span data-stu-id="8b9b6-121">On the **General** FastTab, set the following fields:</span></span><!-- KFM: confirm this:    - **Fixed unit assignment** and **Fixed unit** – These fields have an effect only if you're using the Microsoft Retail Essentials product. If the current unit can be mapped to one of the fixed units that are used by Retail Essentials, set the **Fixed unit assignment** option to *Yes*. Then select the fixed unit in the **Fixed unit** field. -->

    - <span data-ttu-id="8b9b6-122">**Einheitsklasse** – Wählen Sie die Eigenschaft, die die Einheit misst (z. B. Länge, Fläche, Masse oder Menge).</span><span class="sxs-lookup"><span data-stu-id="8b9b6-122">**Unit class** – Select the property that the unit measures (such as length, area, mass, or quantity).</span></span>
    - <span data-ttu-id="8b9b6-123">**System der Einheiten** – Wählen Sie das Messsystem, zu dem die Einheit gehört (*Metrische Einheiten* oder *Gewöhnliche Einheiten der Vereinigten Staaten*).</span><span class="sxs-lookup"><span data-stu-id="8b9b6-123">**System of units** – Select the measurement system that the unit belongs to (*Metric units* or *United States customary units*).</span></span>
    - <span data-ttu-id="8b9b6-124">**Basiseinheit** – Legen Sie diese Option auf *Ja* fest, um die aktuelle Einheit als Basiseinheit für ihre Einheitenklasse zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-124">**Base unit** – Set this option to *Yes* to use the current unit as the base unit for its unit class.</span></span> <span data-ttu-id="8b9b6-125">In diesem Fall müssen Sie nur den Umrechnungsfaktor zwischen der Basiseinheit und jeder zusätzlichen Einheit in der Einheitenklasse angeben.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-125">In this case, you only have to specify the conversion factor between the base unit and each additional unit in the unit class.</span></span> <span data-ttu-id="8b9b6-126">Das System kann dann zwischen allen Einheiten in dieser Einheitenklasse umrechnen.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-126">The system can then convert between all units in that unit class.</span></span> <span data-ttu-id="8b9b6-127">Daher ist es einfacher, Konvertierungen festzulegen.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-127">Therefore, it's easier to set up conversions.</span></span>

        <span data-ttu-id="8b9b6-128">Wenn z.B. Gallone die Basiseinheit für die Einheitenklasse *Volumen* ist, müssen Sie nur Umrechnungsfaktoren von Quart zu Gallone und von Pint zu Gallone festlegen.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-128">For example, if gallon is the base unit for the *Volume* unit class, you only have to set up conversion factors from quart to gallon and from pint to gallon.</span></span> <span data-ttu-id="8b9b6-129">Das System kann dann auch von quart in pint umrechnen.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-129">The system can then also convert from quart to pint.</span></span>

        <span data-ttu-id="8b9b6-130">Sie können nur eine Basiseinheit pro Einheitenklasse haben.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-130">You can have only one base unit per unit class.</span></span>

    - <span data-ttu-id="8b9b6-131">**Systemeinheit** – Legen Sie diese Option auf *Ja* fest, um die aktuelle Einheit als angenommene Einheit für alle nicht spezifizierten Messungen in ihrer Einheitenklasse zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-131">**System unit** – Set this option to *Yes* to use the current unit as the assumed unit for all unspecified measurements in its unit class.</span></span> <span data-ttu-id="8b9b6-132">Wenn z. B. ein Feld, das zur Eingabe einer Menge verwendet wird, die Angabe einer Einheit nicht zulässt (oder wenn der Benutzer keine Einheit auswählt), verwendet das System die Einheit, die als Systemeinheit für die Einheitenklasse *Menge* festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-132">For example, if a field that is used to enter a quantity doesn't allow a unit to be specified (of if the user doesn't select a unit), the system uses the unit that is set as the system unit for the *Quantity* unit class.</span></span> <span data-ttu-id="8b9b6-133">Sie können nur eine Systemeinheit pro Einheitenklasse haben.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-133">You can have only one system unit per unit class.</span></span>
    - <span data-ttu-id="8b9b6-134">**Dezimalpräzision** – Geben Sie die Anzahl der Dezimalstellen an, auf die Werte, die für die aktuelle Einheit angegeben oder in diese umgerechnet werden, gerundet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-134">**Decimal precision** – Specify the number of decimal places that values that are specified for the current unit or converted to it should be rounded to.</span></span>

1. <span data-ttu-id="8b9b6-135">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-135">On the Action Pane, select **Save**.</span></span>

## <a name="define-unit-translations"></a><span data-ttu-id="8b9b6-136">Einheitenübersetzungen definieren</span><span class="sxs-lookup"><span data-stu-id="8b9b6-136">Define unit translations</span></span>

<span data-ttu-id="8b9b6-137">Um Übersetzungen für die ID oder das Symbol und die Beschreibung für eine Maßeinheit zu definieren, gehen Sie wie folgt vor.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-137">To define translations for the ID or symbol and the description for a unit of measure, follow these steps.</span></span>

1. <span data-ttu-id="8b9b6-138">Erstellen oder wählen Sie die Einheit, für die Sie Übersetzungen erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-138">Create or select the unit to create translations for.</span></span>
1. <span data-ttu-id="8b9b6-139">Wählen Sie im Aktivitätsbereich **Einheiten-Texte**.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-139">On the Action Pane, select **Unit texts**.</span></span>

    <span data-ttu-id="8b9b6-140">Die Seite **Einheitentexte** erscheint.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-140">The **Unit texts** page appears.</span></span> <span data-ttu-id="8b9b6-141">Sie verwenden diese Seite, um Übersetzungen für die ID oder das Symbol für die gewählte Einheit zu definieren.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-141">You use this page to define translations for the ID or symbol for the selected unit.</span></span> <span data-ttu-id="8b9b6-142">Diese Übersetzungen können dann auf externen Dokumenten in kunden- oder kreditorenspezifischen Sprachen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-142">Those translations can then be used on external documents in customer-specific or vendor-specific languages.</span></span>

1. <span data-ttu-id="8b9b6-143">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-143">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="8b9b6-144">Wählen Sie im Feld **Sprache** die Sprache aus, in die die ID oder das Symbol der Einheit übersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-144">In the **Language** field, select the language to translate the unit ID or symbol to.</span></span>
1. <span data-ttu-id="8b9b6-145">Geben Sie im Feld **Text** die Übersetzung der ID oder des Symbols der Einheit in der gewählten Sprache ein.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-145">In the **Text** field, enter the translation of the unit ID or symbol in the selected language.</span></span>
1. <span data-ttu-id="8b9b6-146">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-146">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="8b9b6-147">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-147">Close the page.</span></span>
1. <span data-ttu-id="8b9b6-148">Wählen Sie auf der Seite **Aktivitätsbereich** die Option **Übersetzte Einheitenbeschreibungen**.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-148">On the **Action Pane**, select **Translated unit descriptions**.</span></span>

    <span data-ttu-id="8b9b6-149">Die Seite **Übersetzte Einheitenbeschreibungen** erscheint.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-149">The **Translated unit descriptions** page appears.</span></span> <span data-ttu-id="8b9b6-150">Sie verwenden diese Seite, um sprachspezifische Beschreibungen für die ausgewählte Einheit zu definieren.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-150">You use this page to define language-specific descriptions for the selected unit.</span></span>

1. <span data-ttu-id="8b9b6-151">Wählen Sie im Aktivitätsbereich **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-151">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="8b9b6-152">Wählen Sie im Feld **Sprache** die Sprache, in die die Beschreibung der Einheit übersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-152">In the **Language** field, select the language to translate the unit description to.</span></span>
1. <span data-ttu-id="8b9b6-153">Geben Sie im Feld **Beschreibung** die Übersetzung der Beschreibung der Einheit in der gewählten Sprache ein.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-153">In the **Description** field, enter the translation of the unit description in the selected language.</span></span>
1. <span data-ttu-id="8b9b6-154">Wählen Sie im Aktionsbereich **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-154">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="8b9b6-155">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-155">Close the page.</span></span>

## <a name="define-unit-conversion-rules"></a><span data-ttu-id="8b9b6-156">Definieren Sie Einheitenumrechnungsregeln</span><span class="sxs-lookup"><span data-stu-id="8b9b6-156">Define unit conversion rules</span></span>

<span data-ttu-id="8b9b6-157">Um Regeln für Umrechnungen zwischen Maßeinheiten zu definieren, folgen Sie diesen Schritten.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-157">To define rules for conversions between units of measure, follow these steps.</span></span>

1. <span data-ttu-id="8b9b6-158">Erstellen oder wählen Sie die Einheit, für die Sie Umrechnungsregeln definieren wollen.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-158">Create or select the unit to define conversion rules for.</span></span>
1. <span data-ttu-id="8b9b6-159">Wählen Sie im Aktivitätsbereich **Einheiten-Umwandlungen**.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-159">On the Action Pane, select **Unit conversions**.</span></span>

    <span data-ttu-id="8b9b6-160">Die Seite **Einheiten-Umrechnungen** erscheint.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-160">The **Unit conversions** page appears.</span></span> <span data-ttu-id="8b9b6-161">Sie verwenden diese Seite, um Regeln für die Konvertierung der ausgewählten Einheit in und aus anderen Einheiten der Einheitenklasse zu definieren.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-161">You use this page to define rules for converting the selected unit to and from other units in the unit class.</span></span>

1. <span data-ttu-id="8b9b6-162">Wählen Sie eine der folgenden Registerkarten, je nach Art der Konvertierung, die Sie festlegen wollen:</span><span class="sxs-lookup"><span data-stu-id="8b9b6-162">Select one of the following tabs, depending on the type of conversion that you want to set up:</span></span>

    - <span data-ttu-id="8b9b6-163">**Standard-Konvertierungen** – Legen Sie Standard-Konvertierungsregeln für alle Produkte fest.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-163">**Standard conversions** – Set up standard conversion rules for all products.</span></span>
    - <span data-ttu-id="8b9b6-164">**Klassenübergreifende Konvertierungen** – Legen Sie produktspezifische Konvertierungsregeln für Einheiten in derselben Einheitsklasse fest.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-164">**Intra-class conversions** – Set up product-specific conversion rules for units in the same unit class.</span></span>
    - <span data-ttu-id="8b9b6-165">**Klassenübergreifende Umrechnungen** – Legen Sie produktspezifische Umrechnungsregeln für Einheiten über Einheitenklassen hinweg fest.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-165">**Inter-class conversions** – Set up product-specific conversion rules for units across unit classes.</span></span>

1. <span data-ttu-id="8b9b6-166">Führen Sie einen dieser Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="8b9b6-166">Follow one of these steps:</span></span>

    - <span data-ttu-id="8b9b6-167">Um eine neue Konvertierung zu erstellen, wählen Sie **Neu** in der Symbolleiste.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-167">To create a new conversion, select **New** on the toolbar.</span></span>
    - <span data-ttu-id="8b9b6-168">Um eine vorhandene Konvertierung zu bearbeiten, wählen Sie die Konvertierung im Raster aus und wählen dann **Bearbeiten** in der Symbolleiste.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-168">To edit an existing conversion, select the conversion in the grid, and then select **Edit** on the toolbar.</span></span>

1. <span data-ttu-id="8b9b6-169">Legen Sie in der erscheinenden Dropdown-Dialogbox die folgenden Felder fest:</span><span class="sxs-lookup"><span data-stu-id="8b9b6-169">In the drop-down dialog box that appears, set the following fields:</span></span>

    - <span data-ttu-id="8b9b6-170">**Produkt** – Wählen Sie das spezifische Produkt, für das die Konvertierung gilt.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-170">**Product** – Select the specific product that the conversion applies to.</span></span> <span data-ttu-id="8b9b6-171">Dieses Feld ist nur für klasseninterne und klassenübergreifende Konvertierungen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-171">This field is available only for intra-class and inter-class conversions.</span></span>
    - <span data-ttu-id="8b9b6-172">**Formelauslegung** – Lassen Sie dieses Feld auf *Einfach* festgelegt, um eine einfache Umrechnung mit einem einzigen Faktor anzugeben.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-172">**Formula layout** – Leave this field set to *Simple* to specify a simple conversion that has a single factor.</span></span> <span data-ttu-id="8b9b6-173">Legen Sie es auf *Erweitert* fest, um eine komplexere Gleichung einzurichten.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-173">Set it to *Advanced* to set up a more complex equation.</span></span> <span data-ttu-id="8b9b6-174">Das Format für erweiterte Gleichungen variiert je nach Einheitenklasse.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-174">The format for advanced equations varies, depending on the unit class.</span></span>
    - <span data-ttu-id="8b9b6-175">**Aus Einheit** – In diesem Feld wird die gewählte Einheit angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-175">**From unit** – This field shows the selected unit.</span></span> <span data-ttu-id="8b9b6-176">Normalerweise sollten Sie den Wert nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-176">Usually, you should not change the value.</span></span> <span data-ttu-id="8b9b6-177">(Wenn Sie den Wert ändern, müssen Sie die Seite **Einheiten-Umrechnungen** für die gewählte Einheit öffnen, um Ihre neue Umrechnung nach dem Speichern zu sehen.)</span><span class="sxs-lookup"><span data-stu-id="8b9b6-177">(If you do change the value, you must open the **Unit conversions** page for the selected unit to view your new conversion after you save it.)</span></span>
    - <span data-ttu-id="8b9b6-178">**Zur Einheit** – Wählen Sie die Einheit, in die umgerechnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-178">**To unit** – Select the unit to convert to.</span></span>
    - <span data-ttu-id="8b9b6-179">**Rundung** – Wählen Sie, wie Brüche gerundet werden sollen, basierend auf dem **Dezimalpräzisionswert** der ausgewählten Einheit (*Zum nächsten*, *Aufwärts* oder *Abwärts*).</span><span class="sxs-lookup"><span data-stu-id="8b9b6-179">**Rounding** – Select how fractions should be rounded, based on the **Decimal precision** value of the selected unit (*To nearest*, *Up*, or *Down*).</span></span>
    - <span data-ttu-id="8b9b6-180">**Umrechnungsformel** – Geben Sie in den übrigen Feldern oben im Dropdown-Dialogfeld die Formel für die Umrechnung zwischen den beiden Einheiten an.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-180">**Conversion formula** – Use the remaining fields at the top of the drop-down dialog box to specify the formula for converting between the two units.</span></span> <span data-ttu-id="8b9b6-181">Die verfügbaren Felder variieren, abhängig von der gewählten Einheitsklasse und dem Formel-Layout.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-181">The available fields vary, depending on the unit class and formula layout that you've selected.</span></span>

1. <span data-ttu-id="8b9b6-182">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-182">Select **OK**.</span></span>
1. <span data-ttu-id="8b9b6-183">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-183">Close the page.</span></span>

> [!TIP]
> <span data-ttu-id="8b9b6-184">Sie können auch Einheiten-Umrechnungen pro Produktvariante festlegen.</span><span class="sxs-lookup"><span data-stu-id="8b9b6-184">You can also set up unit conversions per product variant.</span></span> <span data-ttu-id="8b9b6-185">Weitere Informationen finden Sie unter [Umrechnung von Maßeinheiten pro Produktvariante](../uom-conversion-per-product-variant.md).</span><span class="sxs-lookup"><span data-stu-id="8b9b6-185">For more information, see [Unit of measure conversion per product variant](../uom-conversion-per-product-variant.md).</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
